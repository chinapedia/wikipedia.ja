> この記事は[+Lhaca](https://ja.wikipedia.org/wiki/+Lhaca)から翻訳されています。


**+Lhaca**（ラカ）とはMicrosoft Windowsで動作する[Lhasa](../Page/Lhasa.md "wikilink")系の[圧縮解凍ソフトウェアである](../Page/データ圧縮.md "wikilink")。

[DLLが不要であり解凍だけでなく圧縮も](../Page/ダイナミックリンクライブラリ.md "wikilink")[ドラッグ&ドロップ操作で可能となっているため](../Page/ドラッグ・アンド・ドロップ.md "wikilink")、インストールや使用時の操作が簡素である。また多くのパソコン関連雑誌、書籍の付録[CD-ROM](../Page/CD-ROM.md "wikilink")にも収録された実績もある。

## バリエーション

\+Lhacaにはいくつかのバリエーションがある。

  - \+Lhaca 0.7x系
    [LHA](../Page/LHA.md "wikilink")と[ZIPに機能を特化した](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")、シンプルで[バイナリ](../Page/バイナリ.md "wikilink")も小さいもの。
  - \+Lhaca 0.9x系（機能拡張版）
    0.7x系に自己解凍形式の生成、パスワード付きZIPなどに対応したもの。
  - \+Lhaca 1.2x系（デラックス版）
    0.9x系に[CAB](../Page/CAB.md "wikilink")、[GZ](https://ja.wikipedia.org/wiki/gzip "wikilink")、[Z](https://ja.wikipedia.org/wiki/Z_\(ファイルフォーマット\) "wikilink")、[BZ2](../Page/Bzip2.md "wikilink")、[TAR](https://ja.wikipedia.org/wiki/tar "wikilink")、[TGZ](https://ja.wikipedia.org/wiki/gzip "wikilink")、[TAZ](https://ja.wikipedia.org/wiki/tar "wikilink")、[TBZ](https://ja.wikipedia.org/wiki/TBZ "wikilink")、[JAR](https://ja.wikipedia.org/wiki/Jar "wikilink")、[ARJ](https://ja.wikipedia.org/wiki/ARJ "wikilink")、[RAR](../Page/RAR.md "wikilink")の解凍、CAB、TGZ、TBZ、TARの圧縮などを追加したもの。

## バッファオーバーフロー問題

\+Lhaca 1.20に[バッファオーバーフローによる脆弱性が発見された](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")\[1\]。これを利用してアタックするLHAファイルの実在も確認されている。その後、これを対策した1.23が[2007年](../Page/2007年.md "wikilink")[7月13日](../Page/7月13日.md "wikilink")にリリースされた。翌日、2007年[7月14日](../Page/7月14日.md "wikilink")に0.7系や0.9系に同様の問題に対策されたバージョン0.76と0.97がリリースされた。+Lhaca公式サイトにて配布されている全ての+Lhacaはバッファオーバーフローの脆弱性の問題に対策済みとの発表がされている。

なお[Lhaplus](../Page/Lhaplus.md "wikilink")にも同様と思われるバッファオーバーフローが存在した\[2\]が、2007年[11月21日](../Page/11月21日.md "wikilink")にリリースされた1.56ですでに対策されている。

## 脚注

<div class="references-small">

<references />

</div>

## 外部リンク

  - [+Lhaca](http://park8.wakwak.com/~app/Lhaca/index.html)

[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:解凍ソフト](https://ja.wikipedia.org/wiki/Category:解凍ソフト "wikilink")

1.  [Symantec Security Response Weblog Beware of LZH](https://www.symantec.com/connect/blogs/beware-lzh)
2.  [Lhaca におけるバッファオーバーフローの脆弱性](http://vuln.sg/lhaca121-jp.html)