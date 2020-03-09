> この記事は[Enhanced Graphics Adapter](https://ja.wikipedia.org/wiki/Enhanced_Graphics_Adapter)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/File:IBM_EGA_card.jpg "fig:サムネイル") [サムネイル](https://ja.wikipedia.org/wiki/File:KL_Genoa_EGA.jpg "fig:サムネイル") **Enhanced Graphics Adapter**（エンハンスト グラフィックス アダプター、**EGA**）は、[IBM](../Page/IBM.md "wikilink")が[1984年](../Page/1984年.md "wikilink")に開発したディスプレイ規格である。グラフィックモードで640×350 64色中16色が表示可能。

## 歴史

EGAは1984年10月に[IBM](../Page/IBM.md "wikilink")より発表された\[1\]\[2\]。（[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")の発売直後だが、PC/AT専用ではない。）

EGA規格は1987年に[PS/2とともに発表された](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")[MCGAおよび](https://ja.wikipedia.org/wiki/Multicolor_Graphics_Adapter "wikilink")[VGAに置き換えられた](../Page/Video_Graphics_Array.md "wikilink")\[3\]。

VGAが発表される少し前に、ジェノア・システムズ (*Genoa Systems*) がプロプライエタリなチップセットを搭載したハーフサイズの[グラフィックカード](../Page/ビデオカード.md "wikilink")、*Super EGA*を発表した（後期のカードは[Super VGAと同様にVGAで拡張されたモードをサポートした](../Page/Super_Video_Graphics_Array.md "wikilink")）\[4\]。

## 設計

EGAは最大640x350ピクセルの[画面解像度](../Page/画面解像度.md "wikilink")で64色のパレットから16色を選択して同時に表示する。EGAカードは追加のグラフィック機能をサポートするシステム[BIOSの拡張のために](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")16KBの[ROMを搭載し](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、また、旧来のグラフィックコントローラー（MDA、CGA）でビデオタイミング信号を生成するのに使われていた[モトローラMC6845チップと後方互換のモードを持つカスタム](https://ja.wikipedia.org/wiki/CRTC_\(LSI\) "wikilink")[CRTCを搭載していた](https://ja.wikipedia.org/wiki/CRTC_\(LSI\) "wikilink")。\[5\]

640x350高解像度モードではピクセルあたり赤、緑、青の各2ビットずつ、それぞれの原色に4階調の輝度を設定でき、それらを組み合わせ可能なパレット（計64色）から16色を選択できた。EGAはCGAの640x200および320x200グラフィックモードのうち16色バージョンを搭載していた。EGA 4ビット（16色）グラフィックモードは[CPU](../Page/CPU.md "wikilink")の[ビット演算](https://ja.wikipedia.org/wiki/ビット演算 "wikilink")による\[6\]ビットプレーンとマスクレジスタ\[7\]の複雑な使用方法としても知られ、VGAや多くの互換ハードウェアに継承されることになる、早期の[グラフィックアクセラレータ](https://ja.wikipedia.org/wiki/グラフィックアクセラレータ "wikilink")を構成するものであった。

EGAは350ラインモード時に21.8kHz、200ラインモード時に15.7kHzで駆動するデュアルシンクである。オリジナルのCGAモードも存在するが、EGAはCGAとのハードウェア互換性は完全ではない。EGAはボード上のスイッチの設定を変えることでMDA用モニターを使用できるものの、この設定では640x350高解像度モノクログラフィックと標準MDAテキストモードのみが利用可能である。

EGAカードは[ISAバスを採用し](https://ja.wikipedia.org/wiki/Industry_Standard_Architecture "wikilink")、当初は[8ビット](https://ja.wikipedia.org/wiki/8ビット "wikilink")版および[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink")版が用意されていた。オリジナルのIBM製EGAカードは64KBの[オンボードRAMを持ち](../Page/VRAM.md "wikilink")、64KBを追加するためには[ドーターボード](https://ja.wikipedia.org/wiki/ドーターボード "wikilink")を必要とした。（64KBのEGAカードでは640x350モード時は4色に制限される。）ほとんどの[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")製カードは128KBが実装済みで、一部は256KBを搭載して複数のグラフィックページをサポートした。いくつかのサードパーティー製EGA互換品（特に[ATIテクノロジーズやパラダイス](https://ja.wikipedia.org/wiki/ATI_Technologies "wikilink")（現・[ウェスタン・ディジタル](https://ja.wikipedia.org/wiki/ウェスタン・デジタル "wikilink")）のボードが知られる）は640x400、640x480、720x540などの拡張されたグラフィックモード、モニター種別の自動検出、CGAモニターを使うための400ライン[インターレース](https://ja.wikipedia.org/wiki/インターレース "wikilink")モードをサポートしていた。

### 表示機能

[サムネイル](https://ja.wikipedia.org/wiki/File:VGA_text_sample_animation.gif "fig:サムネイル") [サムネイル](https://ja.wikipedia.org/wiki/File:Birds_ega.png "fig:サムネイル") テキストモード：

  - 40x25、8x8ピクセルフォント（有効解像度は320x200）
  - 80x25、8x8ピクセルフォント（有効解像度は640x200）
  - 80x25、8x14ピクセルフォント（有効解像度は640x350）
  - 80x43、8x8ピクセルフォント（有効解像度は640x344）

EGA グラフィックモード：

  - 640x350、16色（64色の6ビットパレット）、ピクセル[縦横比は](https://ja.wikipedia.org/wiki/アスペクト比 "wikilink")1:1.37
  - 640x350、2色、ピクセル縦横比は1:1.37
  - 640x200、16色、ピクセル縦横比は1:2.4
  - 320x200、16色、ピクセル縦横比は1:1.2

サードパーティー製ボードの拡張グラフィックモード：

  - 640x400
  - 640x480
  - 720x540

### カラーパレット

[サムネイル](https://ja.wikipedia.org/wiki/File:EGA_Table.PNG "fig:サムネイル") [サムネイル](https://ja.wikipedia.org/wiki/File:6-bit_RGB_uniform_palette_with_black_borders.svg "fig:サムネイル") [サムネイル](https://ja.wikipedia.org/wiki/File:Screen_color_test_EGA_16colors.png "fig:サムネイル") [サムネイル](https://ja.wikipedia.org/wiki/File:Screen_color_test_EGA_16colors_CGA.png "fig:サムネイル") EGAパレットは全ての16色CGAカラーを同時に使用することができ、これらの色はそれぞれ計64色から選んで置き換えることができた。これは追加のディスプレイハードウェア無しでCGA特有の茶色を表示させることも可能にした。後のVGA規格では64色をさらにカスタマイズすることができた。拡張カラーパレットは200ラインモードでは使用できなかった。

EGAパレットから色を選択するとき、赤、緑、青チャンネルに2ビットが使用される。これは各チャンネルが0、1、2、3の値を設定できることを意味する。[マゼンタ](https://ja.wikipedia.org/wiki/マゼンタ "wikilink")カラーを選択するには、赤と青の値を中輝度（十進数で2またはバイナリ値で10）として、緑の値をオフ（0）にセットする。64色EGAパレットで指定値を計算するとき、指定するバイナリ値の書式は"rgbRGB"、小文字をチャンネル輝度の最下位ビット、大文字を最上位ビットとする。マゼンタであれば、赤と青の最上位ビットは1なので、大文字のRとBの場所が1になる。残りの桁は全て0となり、マゼンタカラーを表すバイナリ値は"000101"となる。これは10進数で5となるから、パレット指定に5をセットすることでマゼンタが選択されたことになる。全てのデフォルト色のカラー値を次の表に記述する。

| 番号 | 色 | 16進数                     | rgbRGB   | 10進数   |
| -- | - | ------------------------ | -------- | ------ |
| 0  |   | Black                    | \#000000 | 000000 |
| 1  |   | Blue                     | \#0000aa | 000001 |
| 2  |   | Green                    | \#00aa00 | 000010 |
| 3  |   | Cyan                     | \#00aaaa | 000011 |
| 4  |   | Red                      | \#aa0000 | 000100 |
| 5  |   | Magenta                  | \#aa00aa | 000101 |
| 6  |   | Brown                    | \#aa5500 | 010100 |
| 7  |   | White / light gray       | \#aaaaaa | 000111 |
| 8  |   | Dark gray / bright black | \#555555 | 111000 |
| 9  |   | Bright blue              | \#5555ff | 111001 |
| 10 |   | Bright green             | \#55ff55 | 111010 |
| 11 |   | Bright cyan              | \#55ffff | 111011 |
| 12 |   | Bright red               | \#ff5555 | 111100 |
| 13 |   | Bright magenta           | \#ff55ff | 111101 |
| 14 |   | Bright yellow            | \#ffff55 | 111110 |
| 15 |   | Bright white             | \#ffffff | 111111 |

EGA 16色パレット（標準CGAカラーに設定した場合）

### 仕様

EGAはCGA端子と同じ9ピンメスの[Dサブ端子を使用する](https://ja.wikipedia.org/wiki/D-subminiature "wikilink")。ピン割り当てを含むハードウェア信号インターフェースはCGAとほぼ互換性がある。その違いは3つのピンがEGAのセカンダリRGB信号となっていること。詳しくは、CGAではピンとされていたのが、ピンとされていたのが、予約ピンとされていたのがに変更されている。EGAがCGAと同じ走査レートのモードで動作している場合、CGAモニターへの接続は正常に動作するが、モニターが2ピンをグラウンドに接続している場合はEGAの出力をグラウンドに短絡させることになり、EGAアダプターの損傷に繋がる恐れがある。

ほとんどのEGAカードはカード背面にモニター種別を選択するための[ディップスイッチ](https://ja.wikipedia.org/wiki/ディップスイッチ "wikilink")を持っており、CGAが選択されていると、カードは200ラインモードで動作し、テキストモードでは8x8ピクセルフォントが使用される。350ラインモードには切り替えることができず、拡張カラーパレットも使用できない。EGAが選択されると、カードは350ラインモードで動作し、8x14ピクセルフォントが使用される。しかし、グラフィックモードは640x350x2のみが使用できる。

IBM 5154 EGAモニターは特殊なIBM 5153 CGA互換モードを備えていて、CGA相当の同期信号で動作しているときは自動でCGAのピン割り当てに切り替え、先に述べた問題を回避するようになっている\[8\]。

### メモリ割り当て

EGAグラフィックモードはプレーンアクセス方式で、これはCGAや[Herculesモードとは対照的である](https://ja.wikipedia.org/wiki/Hercules_Graphics_Card "wikilink")。ビデオメモリは4ページに分割され（2ページを持つ530x350x2を除く）、それぞれRGBI色空間を持つ\[9\]。各ビットは1ピクセルを表す。赤ページの1ビットが有効にされると、他のページの同等のビットがセットされていなくても、画面上の指定位置に赤色のドットが現れる。同じピクセルの他のプレーン全てのビットも有効にすると、それは白色になる。各プレーンのサイズは、8KB（200ラインモードと640x350ピクセル2色）、16KB（64KBビデオRAMでの640x350ピクセル）、32KB（128KBビデオRAMでの640x350）となり、CPUアドレス空間のセグメントA000に割り当てられる。それらはバンク切り替え方式で、一度に1プレーンのみ読むことができるのだが、プログラマーは書き込み先のプレーンをEGAカードのコントロールレジスタにセットする手法をとっていた。したがって、読み込みは常に1プレーンのみだが、書き込みは全てのプレーンに一度に行うことができた。

後方互換性を確保するため、カラーテキストとCGAモードはセグメントB800、モノクロテキストはB000に割り当てられた。

### コネクタ

EGAでは[DE-9メスコネクタが使われている](https://ja.wikipedia.org/wiki/D-subminiature "wikilink")。ピン番号は上段が1-5、下段が6-9で、どちらも右から左に番号を割り当てた状態のピン割り当てを次に示す。

[DE9_Diagram.svg](https://ja.wikipedia.org/wiki/File:DE9_Diagram.svg "fig:DE9_Diagram.svg")

| **ピン** | **名称** | **役割**                      |
| ------ | ------ | --------------------------- |
| 1      | GND    | Ground                      |
| 2      | SR     | Secondary Red (Intensity)   |
| 3      | PR     | Primary Red                 |
| 4      | PG     | Primary Green               |
| 5      | PB     | Primary Blue                |
| 6      | SG     | Secondary Green (Intensity) |
| 7      | SB     | Secondary Blue (Intensity)  |
| 8      | H      | Horizontal Sync             |
| 9      | V      | Vertical Sync               |
|        |        |                             |

**ピン割り当て**

### 信号

<table>
<thead>
<tr class="header">
<th style="text-align: right;"><p>種別</p></th>
<th><p>デジタル、TTLレベル</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: right;"></td>
<td><p>640×350、他</p></td>
</tr>
<tr class="even">
<td style="text-align: right;"><p>水平同期周波数</p></td>
<td><p>15.7kHzまたは21.8 kHz</p></td>
</tr>
<tr class="odd">
<td style="text-align: right;"><p>垂直同期周波数</p></td>
<td><p>60 Hz</p></td>
</tr>
<tr class="even">
<td style="text-align: right;"><p>表現可能色数</p></td>
<td><p>6ビット（64色）</p></td>
</tr>
</tbody>
</table>

## 脚注

**注釈**  **出典**

## 参考文献

  - (IBM Part Number 6322509)

  -
## 関連項目

  - [ビデオカード](../Page/ビデオカード.md "wikilink")
  - [画面解像度](../Page/画面解像度.md "wikilink")

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.  High-Resolution Standard Is Latest Step in DOS Graphics Evolution, *InfoWorld*, June 26, 1989, p. 48
2.  News Briefs, Big Blue Turns Colors, *InfoWorld*, Oct 8, 1984
3.  Scott Mueller, *Upgrading and Repairing PCs, Tenth Edition*, Que,1998, 0-7897-1636-4 page 515
4.  Hardware, Genoa Systems Ready to Ship $449 Half-Size Graphics Card, *InfoWorld*, February 23, 1987
5.
6.
7.  [Complete Instructions to BLOAD and BSAVE EGA and VGA Screens](http://support.microsoft.com/kb/45699), [マイクロソフト](../Page/マイクロソフト.md "wikilink")
8.  IBM Options and Adapters, Volume 1, "Enhanced Color Display", Page 4: "When operating in Mode 1, the display maps the 4 input bits into 16 of the possible 64 colors as shown in the following chart.". August 2nd, 1984.
9.  1ページあたりにRGBI（赤、緑、青、輝度）の4プレーンを持つ。このうち、同時には1プレーンのみをCPUのアドレス空間に割り当てることができる。