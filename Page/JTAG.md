> この記事は[JTAG](https://ja.wikipedia.org/wiki/JTAG)から翻訳されています。


**JTAG**（ジェイタグ、）は、[集積回路](../Page/集積回路.md "wikilink")や[基板](https://ja.wikipedia.org/wiki/基板 "wikilink")の[検査](https://ja.wikipedia.org/wiki/検査 "wikilink")、[デバッグ](../Page/デバッグ.md "wikilink")などに使える、[バウンダリスキャンテスト](https://ja.wikipedia.org/wiki/バウンダリスキャンテスト "wikilink")やテストアクセスポートの標準 [IEEE](../Page/IEEE.md "wikilink") 1149.1 の通称である。本来はこの検査方式を定めた[業界団体](https://ja.wikipedia.org/wiki/業界団体 "wikilink")（Joint European Test Action Group）の名称の略。当初JETAGであったがEuropeanが抜けJTAGとなった。

## 概要

[半導体](../Page/半導体.md "wikilink")[技術](../Page/技術.md "wikilink")の進歩により集積回路チップの[ピン間隔も狭くなり](https://ja.wikipedia.org/wiki/端子 "wikilink")[プローブ](https://ja.wikipedia.org/wiki/プローブ "wikilink")を立てての検査が困難になってきている。表面実装の[BGAなどの](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#BGA_\(Ball_grid_array\) "wikilink")[パッケージに至っては](../Page/パッケージ_\(電子部品\).md "wikilink")、物理的に不可能である。そのため検査時に、チップ内部の回路を数珠繋ぎにし、内部状態を順番に読み出すしくみ（）が考え出された。これをバウンダリスキャンテスト（boundary scan test）といい、それを[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")化したのがJTAGである。[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に[IEEE](../Page/IEEE.md "wikilink") 1149.1として[標準化](../Page/標準化.md "wikilink")されている。

近年、検査目的だけではなく、[組み込みシステム](../Page/組み込みシステム.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[デバッグ](../Page/デバッグ.md "wikilink")などの目的で、[ICEの一種として](https://ja.wikipedia.org/wiki/インサーキット・エミュレータ "wikilink")、[CPU](../Page/CPU.md "wikilink")や[FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")にアクセスする手段としてJTAGが用いられるようになってきている。その場合、本来のICEの機能である[リアルタイム性の](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")[観測](../Page/観測.md "wikilink")は、再現できない場合もある。

## 電気的特性

### デイジーチェーン接続のJTAG (IEEE 1149.1)

1.  **TDI** (Test Data In)
2.  **TDO** (Test Data Out)
3.  **TCK** (Test Clock)
4.  **TMS** (Test Mode Select)
5.  **TRST** (Test Reset) optional.

[Jtag_chain.svg](https://ja.wikipedia.org/wiki/File:Jtag_chain.svg "fig:Jtag_chain.svg")

## 関連項目

  - [半導体工学](../Page/半導体工学.md "wikilink")
  - [集積回路](../Page/集積回路.md "wikilink")
  - [オンチップ・エミュレータ](https://ja.wikipedia.org/wiki/オンチップ・エミュレータ "wikilink")
  - [インサーキット・エミュレータ](https://ja.wikipedia.org/wiki/インサーキット・エミュレータ "wikilink")
  - [Open JTAG](https://ja.wikipedia.org/wiki/:en:Open_JTAG "wikilink")

## 外部リンク

  - [JTAGチュートリアル](http://translate.googleusercontent.com/translate_c?hl=en&langpair=en%7Cja&rurl=translate.google.com&u=http://www.corelis.com/education/JTAG_Tutorial.htm&usg=ALkJrhjAD3ElMWEK2HHaKksn2z7dyeEy1A) JTAGアーキテクチャと新技術動向の概要
  - [IEEE 1149.1 Working Group](http://grouper.ieee.org/groups/1149/1/) IEEEオフィシャルワーキング・グループ
  - [IEEE STANDARD ASSOCIATION](https://standards.ieee.org/findstds/standard/1149.1-1990.html) IEEE 1149.1規格書
  - [IEEE 1149.1 Testability](http://fieldbus.feld.cvut.cz/cs/system/files/files/cs/vyuka/predmety/x38dcz/ieee1149.pdf) IEEE 1149.1によるテスト手法

[Category:半導体製造](https://ja.wikipedia.org/wiki/Category:半導体製造 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink") [Category:電子部品](https://ja.wikipedia.org/wiki/Category:電子部品 "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink")