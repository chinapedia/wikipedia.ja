> この記事は[Write-combining](https://ja.wikipedia.org/wiki/Write-combining)から翻訳されています。


**Write-combining** （WC）とは、[バス技術のひとつである](../Page/バス_\(コンピュータ\).md "wikilink")。バスを流れるデータは、結合されて[バッファ](../Page/バッファ.md "wikilink")（**write combine buffer**（WCB））に一時的に保存される。[データ](../Page/データ.md "wikilink")は、単一のビットや小さなまとまりとしてすぐに書き込む代わりに、後で[バーストモードでまとめて書き込まれる](https://ja.wikipedia.org/wiki/バーストモード_（コンピュータ） "wikilink")。

## 概要

**Write-combining** は、「弱い順序付け（Weak Ordering）」であるため、一般的なメモリアクセス（データや[コード領域](../Page/プログラム_\(コンピュータ\).md "wikilink")）には使用できない。 Write-combining では、読み書きの組み合わせが正しい順序で完了することが保証されない。例えば、特定のアドレスに対して Write → Read → Write の組み合わせで処理するとき、 Read → Write → Write というふうに Write-combining された順序になる。この場合、最初の読み込みのときに、本来なら書き込まれているはずのデータが書き込まれる前の間違った値を取得するおそれがある。そのため、この技術は[ビデオカード](../Page/ビデオカード.md "wikilink")の[フレームバッファのような](https://ja.wikipedia.org/wiki/VRAM#フレームバッファ "wikilink")「強い順序付け（Strong Ordering）」（常に正しい順序）を必要としないメモリに対してのみ使用できる。

## 関連項目

  - [MTRR](https://ja.wikipedia.org/wiki/MTRR "wikilink") （Memory Type Range Register）

## 外部リンク

  - [FAST v1.10](http://www.mdgx.com/files/FASTV110.ZIP) Enable Write Combining for Pentium Pro/2 on Win9x
  - [CTU by Rob Mueller](http://www.k6plus.com/index.php?name=Downloads&req=getit&lid=9) Enable Write Combining for K6-X on Win9x

## 翻訳元

*[:en:Write-combining](https://ja.wikipedia.org/wiki/:en:Write-combining "wikilink") 2007-07-18 09:51 UTCより翻訳。著者 : Widefox ほか*

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink") [Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink")