> この記事は[Hercules Graphics Card](https://ja.wikipedia.org/wiki/Hercules_Graphics_Card)から翻訳されています。


[KL_Hercules_HGC.png](https://ja.wikipedia.org/wiki/File:KL_Hercules_HGC.png "fig:KL_Hercules_HGC.png") **Hercules Graphics Card** (ハーキュリーズ グラフィックス カード、**HGC**)は、[1980年代](../Page/1980年代.md "wikilink")中ごろのによる[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")用グラフィックスコントローラであり、当時、IBM純正品ではないにもかかわらず、標準的な地位を占めていた。MDA用モニタがそのまま利用できる。コントローラは、MDAやCGA同様モトローラ[MC6845を用いている](../Page/CRTC_\(LSI\).md "wikilink")。

HGCは、720x348 のモノクロ表示をサポートし、特に[スプレッドシート](https://ja.wikipedia.org/wiki/スプレッドシート "wikilink")の利用者に愛用された。

HGCは他のIBM標準のディスプレイアダプタと異なるアドレス([CGAが](../Page/Color_Graphics_Adapter.md "wikilink")0b800h・[VGAが](../Page/Video_Graphics_Array.md "wikilink")0a000h、HGCは0b000h)を用いるため共存が可能で、2画面を同時使用できる。 そのため、[CAD](../Page/CAD.md "wikilink")やプログラムのデバッグの時にも重宝されていた。

なお、[XFree86](../Page/XFree86.md "wikilink")の2.x世代でマルチディスプレイをサポートしていたのはVGA系とHGCの組み合わせのみであったのもこの伝統からであろう。

## 技術仕様

IBMの[MDAと同じように](../Page/Monochrome_Display_Adapter.md "wikilink")、HGCは[パラレルプリンタポートとビデオ出力端子の両方を搭載していた](../Page/パラレルポート.md "wikilink")\[1\]。

テキストモードは80x25字を表示でき、MDAと互換性があった。文字は7x11ピクセルフォントを使用して9x14ピクセルのボックス（文字間・行間の空白を含む）で描画した。これによりCGAよりも鮮明なテキストを表示することができた。このテキストモードの理論的な合計解像度は720x350ピクセルであった。

グラフィックモードは全てのピクセルをアドレス割り当てできるようにしている。技術的な理由により画面の高さが4の倍数をとる必要があったため、720x350ではなく720x348ピクセルに変換される。ピクセル[縦横比は](../Page/アスペクト比.md "wikilink")1:1.55。

## 脚注

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.