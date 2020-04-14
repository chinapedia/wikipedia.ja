> この記事は[モジュール:Vorlage:Pressemappe](https://ja.wikipedia.org/wiki/モジュール:Vorlage:Pressemappe)から翻訳されています。


\--\[=\[ Vorlage:Pressemappe \]=\]

\-- Export local p = { }

p.folderID = function ( frame )

`   local s = frame.args[ 1 ]`
`   local r`
`   if s then`
`       local subject, since, second = s:match( "^(%l%l)/(%d+)(,?%d*)$" )`
`       if subject then`
`           if subject == "co"  or  subject == "pe" then`
`               if second == "" then`
`                   if #since ~= 6 then`
`                       r = "Zahl unerlaubt: " .. since`
`                   end`
`               else`
`                   r = "Zweite Zahl unerwartet: " .. second`
`               end`
`           elseif subject == "sh"  or  subject == "wa" then`
`               if second:match( "^,%d+$" ) then`
`                   if #since ~= 6 then`
`                       r = "Zahl unerlaubt: " .. since`
`                   elseif #second ~= 7 then`
`                       r = "Zweite Zahl unerlaubt: " .. second:sub( 2 )`
`                   end`
`               else`
`                   r = "Details fehlerhaft"`
`               end`
`           else`
`               r = "Sachgebiet unbekannt: " .. subject`
`           end`
`       else`
`           r = "Strukturfehler"`
`       end`
`   else`
`       r = "Kein Parameter"`
`   end`
`   return  r or ""`

end

return p