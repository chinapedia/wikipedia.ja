> この記事は[Color Graphics Adapter](https://ja.wikipedia.org/wiki/Color_Graphics_Adapter)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:CGA_CompVsRGB_Text.png "wikilink") **Color Graphics Adapter** (CGA) は、[IBM PC用に](../Page/IBM_PC.md "wikilink")[1981年](../Page/1981年.md "wikilink")に開発された、PC用カラーグラフィックスカードであり、後の標準となったカードである。

CGAは16Kibytesのメモリを搭載し、80x25・40x25のテキスト16色か、640x200 2色、320x200 4色の表示モードを持つ。また、テキストモードは[MDAと上位互換性を持つ](../Page/Monochrome_Display_Adapter.md "wikilink")。コントローラにはMDA同様[モトローラ](../Page/モトローラ.md "wikilink")MC6845を用いている。

出力は15.75kHz/60HzのTTLレベル[RGB](../Page/RGB.md "wikilink")Iである。転じて15kHz系のRGB映像信号や、640x200などの15kHzで使用される解像度を俗に「CGA」と呼ぶようにもなった。IBM純正のカードは[NTSC](../Page/NTSC.md "wikilink")準拠の[コンポジット映像出力もできる](../Page/コンポジット映像信号.md "wikilink")。コンポジット映像出力で80x25・640x200表示をすると滲みが出る。

## INT 10h ビデオモード一覧

| INT 10h ビデオモード | テキスト解像度 | [画面解像度](../Page/画面解像度.md "wikilink") | 色数     | QBasic                               |
| -------------- | ------- | ------------------------------------ | ------ | ------------------------------------ |
| 00h            | 40x25   | テキストモード                              | 2      | \-                                   |
| 01h            | 40x25   | テキストモード                              | 16     | Screen 0; Mode Con: Lines=25 Cols=40 |
| 02h            | 80x25   | テキストモード                              | 2      | \-                                   |
| 03h            | 80x25   | テキストモード                              | 16     | Screen 0; Mode Con: Lines=25 Cols=80 |
| 04h            | 40x25   | 320x200                              | 4      | Screen 1                             |
| 05h            | 40x25   | 320x200                              | 4 (白黒) | \-                                   |
| 06h            | 80x25   | 640x200                              | 2      | Screen 2                             |

## コネクタ

CGAのコネクタは [DE-9である](https://ja.wikipedia.org/wiki/D-subminiature#9pin（DE-9コネクタ） "wikilink")。9ピンの[VGA端子](../Page/VGA端子.md "wikilink")とはピンアサインが異なり互換性は無い\[1\]。

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

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.  [EGA/CGA/VGA9 DB9 Connector](http://info-coach.fr/atari/hardware/interfaces.php#EGA_DB9_Connector)