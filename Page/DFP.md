> この記事は[DFP](https://ja.wikipedia.org/wiki/DFP)から翻訳されています。


**DFP**(Digital Flat Panel Port)は、[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")と[パソコンの間における信号伝送方式で](../Page/パーソナルコンピュータ.md "wikilink")、[デジタル](../Page/デジタル.md "wikilink")[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")のひとつである。

DFPは、ATI、Compaq、Appleなどから成るDFPグループによって策定され、1999年3月に[VESA](../Page/VESA.md "wikilink")で正式に採用された。

## 概要

ディスプレイ用インタフェースとして、[CRT用の](../Page/ブラウン管.md "wikilink")[RGB](../Page/RGB.md "wikilink")の[アナログ信号](https://ja.wikipedia.org/wiki/アナログ信号 "wikilink")を伝達する[VGA端子](https://ja.wikipedia.org/wiki/VGA端子 "wikilink")があるが、液晶ディスプレイなどのフラットパネルディスプレイ装置にとっては、[デジタル信号](../Page/デジタル信号.md "wikilink")を伝送するほうが好ましい。

アナログRGB信号を液晶ディスプレイに表示する場合は、

`ビデオカード(ディジタル信号→アナログ信号)`
`    |`
`VGA端子(アナログ信号)`
`    |`
`VGAケーブル(アナログ信号)`
`    |`
`VGA端子(アナログ信号)`
`    |`
`液晶ディスプレイ(アナログ信号→ディジタル信号)`

のような構成になるため、装置が複雑になることでコストの増加や、複数のアナログ⇔ディジタル変換とアナログ信号での伝送を行うため、性能劣化の要因となりうる。

そこで、各メーカ独自のデジタルインタフェースを搭載したグラフィックカード/液晶ディスプレイが存在した。これは、アナログ変換を行なわないため、ディスプレイ本来の表示性能を発揮できるが、それぞれのメーカーの製品間での互換性がなかった。

このことから、DFPグループが'98年にリリースした「Digital Flat Panel Port（DFP）Specification」は、PCのディスプレイ出力を[TMDS](https://ja.wikipedia.org/wiki/TMDS "wikilink")（[Transmission Minimized Differential Signaling](https://ja.wikipedia.org/wiki/Transmission_Minimized_Differential_Signaling "wikilink"), PanelLink）という伝送方式を使ってデジタルのまま伝送する規格を策定した。後述の[DVIの策定後](https://ja.wikipedia.org/wiki/Digital_Visual_Interface "wikilink")、ディスプレイのデジタルインタフェースとして、統一された規格に収束していった。

DFPは、TMDSと[VESA DDCの信号を含み](https://ja.wikipedia.org/wiki/VESA_Display_Data_Channel "wikilink")、コネクタには一般的な20接点のセントロニクスハーフコネクタを使用する。

DVI-Dと互換性があり、コネクタ形状の変換のみを行う\[1\]ことで、そのまま利用できる製品が多いものの、[2014年](../Page/2014年.md "wikilink")現在は規格を正しく守っていない商品が発売されているため、注意が必要である\[2\]。

また、日本向けに生産されたごく一部のモニターに限り、DFPを拡張した形でモニターにUSBハブ同等の機能も持たせ、20接点を超えるコネクタを採用した独自規格も作られている\[3\]\[4\]。

Image:DFP_connector.jpg|DFPコネクタ Image:Adapter_DVI_DFP.jpg|DVI-DFP変換アダプタ Image:DFP connector.png|ピンアサイン

## 関連項目

  - [Digital Visual Interface](https://ja.wikipedia.org/wiki/Digital_Visual_Interface "wikilink")

## 脚注

### 出典

## 外部リンク

  - [DFP Group（英文）](http://www.dfp-group.org/)
  - [TMDS（PanelLink）](http://pc.watch.impress.co.jp/docs/article/980723/key39.htm)

[Category:映像端子](https://ja.wikipedia.org/wiki/Category:映像端子 "wikilink") [Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink")

1.  [DFPインターフェースの液晶を使う](http://yutaka.web5.jp/PC/dfp/)
2.  [一般ユーザーの人柱報告](https://twitter.com/rance_dog/status/541967761736339456)
3.  [玄人志向 DVI-FJ30A：富士通デジタル液晶用変換BOX](http://www.kuroutoshikou.com/product/old_series/old_graphics_bord/old_graphic_accesories/old_graphic_accesories_kiwamono/dvi-fj30a/)
4.  [VAIO 専用モニタ改造 Reference](http://homepage2.nifty.com/holiday/doc/)