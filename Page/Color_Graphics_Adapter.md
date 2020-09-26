> この記事は[Color Graphics Adapter](https://ja.wikipedia.org/wiki/Color_Graphics_Adapter)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:CGA_CompVsRGB_Text.png "wikilink") **Color Graphics Adapter** (CGA) は、[1981年](../Page/1981年.md "wikilink")に[IBM PC用に販売された](../Page/IBM_PC.md "wikilink")、[IBM](../Page/IBM.md "wikilink")の[カラーグラフィックスカードで](../Page/ビデオカード.md "wikilink")、後の標準となった。

CGAは4つのテキストモードと2つのグラフィックモードの、計6つの表示モードを持つ。後継の[EGA](../Page/Enhanced_Graphics_Adapter.md "wikilink")、[MCGA](../Page/Multicolor_Graphics_Adapter.md "wikilink")、[VGA等はCGAの全ての表示モードを持ち](../Page/Video_Graphics_Array.md "wikilink")、[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")である。

## 概要

CGA(Color Graphics Adapter)は1981年のオリジナルのIBM PC用の最初のグラフィックカードとして登場し、初期には *Color/Graphics Adapter* や *IBM Color/Graphics Monitor Adapter* とも呼ばれた\[1\] 。

CGAは16K[バイト](https://ja.wikipedia.org/wiki/バイト "wikilink")の[ビデオメモリを備え](../Page/VRAM.md "wikilink")、[IBM 5153などのカラーディスプレイモニタに接続することも](https://ja.wikipedia.org/wiki/:en:IBM_5153 "wikilink")、[NTSC](../Page/NTSC.md "wikilink")互換の[テレビ](../Page/テレビ.md "wikilink")に[コンポジット映像出力することもできる](../Page/コンポジット映像信号.md "wikilink")\[2\]。なおコンポジット映像出力で80x25・640x200表示をすると滲みが出る。またコントローラにはMDA同様[モトローラ](../Page/モトローラ.md "wikilink")MC6845を用いている。出力は15.75kHz/60HzのTTLレベル[RGB](../Page/RGB.md "wikilink")Iである。転じて15kHz系のRGB映像信号や、640x200などの15kHzで使用される解像度を俗に「CGA」と呼ぶようにもなった。

1984年に発売された[IBM PCjrには](https://ja.wikipedia.org/wiki/IBM_PCjr "wikilink") CGA Plus がシステムボードに搭載された。後継規格のEGA, MCGA, VGA, SVGA, XGA等は全てCGA上位互換でもある。

## 表示モード

CGAは4つのテキストモードと2つのグラフィックモードの、計6つの表示モード（ビデオモード）をサポートする。ビデオモードは[BIOS割り込み](https://ja.wikipedia.org/wiki/BIOS割り込みルーチン "wikilink")(INT 10h, AH=00h, AL=ビデオモード)で切替できる。

| ビデオモード | テキスト解像度 | [画面解像度](../Page/画面解像度.md "wikilink") | 色数     | QBasic                               |
| ------ | ------- | ------------------------------------ | ------ | ------------------------------------ |
| 00h    | 40x25   | テキストモード                              | 2      | \-                                   |
| 01h    | 40x25   | テキストモード                              | 16     | Screen 0; Mode Con: Lines=25 Cols=40 |
| 02h    | 80x25   | テキストモード                              | 2      | \-                                   |
| 03h    | 80x25   | テキストモード                              | 16     | Screen 0; Mode Con: Lines=25 Cols=80 |
| 04h    | 40x25   | 320x200                              | 4      | Screen 1                             |
| 05h    | 40x25   | 320x200                              | 4 (白黒) | \-                                   |
| 06h    | 80x25   | 640x200                              | 2      | Screen 2                             |

また CGA Plus は、CGAのサブセットに独自のモードを追加したもので、以下の表示モードを持つ。

  - CGA標準の4つのビデオモード
      - 40x25 16色 テキストモード
      - 80x25 16色 テキストモード
      - 320x200 4色 グラフィックモード
      - 640x200 2色 グラフィックモード
  - 新しい3つのビデオモード
      - 160x200 16色 グラフィックモード
      - 320x200 16色 グラフィックモード
      - 640x200 4色 グラフィックモード

## コネクタ

CGAのコネクタは [DE-9である](https://ja.wikipedia.org/wiki/D-subminiature#9pin（DE-9コネクタ） "wikilink")。9ピンの[VGA端子](../Page/VGA端子.md "wikilink")とはピンアサインが異なり互換性は無い\[3\]。

[DE9_Diagram.svg](https://ja.wikipedia.org/wiki/File:DE9_Diagram.svg "fig:DE9_Diagram.svg")

| **ピン番号** | **機能** |
| -------- | ------ |
| 1        | GND    |
| 2        | GND    |
| 3        | 赤      |
| 4        | 緑      |
| 5        | 青      |
| 6        | 輝度     |
| 7        | （予約済）  |
| 8        | 水平同期   |
| 9        | 垂直同期   |
|          |        |

**ピン配置**

## 信号

| 方式      | TTLレベル                      |
| ------- | --------------------------- |
| 解像度     | 640ドットx200ライン、320ドットx200ライン |
| 水平同期周波数 | 15.75 kHz                   |
| 垂直同期周波数 | 60 Hz                       |
| 色数      | 16                          |

## 脚注

## 関連項目

  - [IBM PC](../Page/IBM_PC.md "wikilink")
  - [ビデオカード](../Page/ビデオカード.md "wikilink")
  - [解像度](../Page/解像度.md "wikilink")

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.  [1](http://vintageibm.net/yahoo_site_admin/assets/docs/techrefv202.zip); cf. section 1-133, "Color/Graphics Adapter", page 143 of ibm_techref_v202_1.pdf
2.
3.  [EGA/CGA/VGA9 DB9 Connector](http://info-coach.fr/atari/hardware/interfaces.php#EGA_DB9_Connector)