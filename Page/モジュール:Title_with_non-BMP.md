> この記事は[モジュール:Title with non-BMP](https://ja.wikipedia.org/wiki/モジュール:Title_with_non-BMP)から翻訳されています。


getNonBmp = function(str)

`   local nonbmp = {}`
`   for c in mw.ustring.gcodepoint(str) do`
`       if c > 0xFFFF then  -- BMP外の文字である`
`           table.insert(nonbmp, c)`
`       end`
`   end`
`   return nonbmp`

end

return {

`   main = function(frame) `
`       local title = mw.title.getCurrentTitle()`
`       local nonbmp = getNonBmp(title.text)`
`       if (title.namespace == 2) or (title.namespace == 3) then    -- 利用者名前空間もしくは利用者‐会話名前空間`
`           return ""   -- 空の文字列を返す`
`       end`
`       if #nonbmp == 0 then    -- BMP外の文字が存在しない`
`           return frame:expandTemplate{`
`               title="Error",`
`               args={ "ページ名に`[`基本多言語面`](../Page/基本多言語面.md "wikilink")`(U+0000からU+FFFFまで)の範囲外にある文字が含まれていません。" }`
`               } .. ""`
`       end`
`       if title.isRedirect then    -- リダイレクトである`
`           for i = 1, #nonbmp do`
`               nonbmp[i] = mw.ustring.format(`
`                   '`<span style="font-size:large">`「`[`&#x%X;`](https://ja.wikipedia.org/wiki/wikt:&#x%X; "wikilink")`」`</span>`(U+%X)',`
`                   nonbmp[i], nonbmp[i], nonbmp[i])`
`           end`
`           return mw.ustring.format(`
`               "* [[:Category:Unicode基本多言語面外の文字を含むリダイレクト|" ..`
`                   "Unicode基本多言語面外の文字を含むリダイレクト]]: " ..`
`                   "このリダイレクトのタイトルにはUnicodeの`[`基本多言語面`](../Page/基本多言語面.md "wikilink")にない文字`%sを含んでいます。" .. `
`                   "",`
`               table.concat(nonbmp, "、"))`
`       else    -- リダイレクトでない`
`           return ""`
`       end`
`   end`

}

[Category:テンプレート呼び出しエラーのあるページ/Template:Title_with_non-BMP](https://ja.wikipedia.org/wiki/Category:テンプレート呼び出しエラーのあるページ/Template:Title_with_non-BMP "wikilink") [Category:Unicode基本多言語面外の文字を含むリダイレクト](https://ja.wikipedia.org/wiki/Category:Unicode基本多言語面外の文字を含むリダイレクト "wikilink") [Category:Unicode基本多言語面外の文字を含むページ名](https://ja.wikipedia.org/wiki/Category:Unicode基本多言語面外の文字を含むページ名 "wikilink")