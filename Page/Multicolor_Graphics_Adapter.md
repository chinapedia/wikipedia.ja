> この記事は[Multicolor Graphics Adapter](https://ja.wikipedia.org/wiki/Multicolor_Graphics_Adapter)から翻訳されています。


**Multi-Color Graphics Array** (**MCGA**) は、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に発売された[IBM PS/2下位モデルに搭載された](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")[ビデオサブシステムである](../Page/ビデオカード.md "wikilink")。

MCGAはPS/2 上位モデルに標準搭載された[VGAの機能限定版で](../Page/Video_Graphics_Array.md "wikilink")、[CGA上位互換の表示モードや](../Page/Color_Graphics_Adapter.md "wikilink")、VGAと同じ解像度のモノクロ表示モードなどを持つが、[EGAの表示モードは持たない](../Page/Enhanced_Graphics_Adapter.md "wikilink")。

## 概要

MCGAは、1987年4月2日に発表された IBM PS/2 モデル 30と、同年8月に発表されたモデル 25の[マザーボード](../Page/マザーボード.md "wikilink")に組み込まれたビデオサブシステムで、単体のビデオカードとしては販売されなかった\[1\]。

MCGAはCGAの全ての表示モードに加え、640x480 モノクロと、320x200 同時256色（262,144色中）の追加された表示モードをサポートするが、[MDAのモノクロテキストモードはサポートしない](../Page/Monochrome_Display_Adapter.md "wikilink")。アナログディスプレイ用のコネクタは[DE-15であった](../Page/D-subminiature.md "wikilink")。MCGAは、同時256色の表示モードや、640x480解像度の表示モード、またDE-15のコネクタを使用している点ではVGAと類似しているが、VGAとは異なり既存のEGAとの上位互換性や、VGAの 640x480 カラーなどの表示モードは持っていない。MCGAの同時256色のモードはゲーム用に広く使用された。

MCGAの任期は短く、1992年にモデル30, 25が販売停止となった後は、互換機では[Epson Equity](https://ja.wikipedia.org/wiki/:en:Epson_Equity "wikilink") Ie \[2\]以外には採用は無く、MCGAの上位互換であるVGAが[業界標準](https://ja.wikipedia.org/wiki/業界標準 "wikilink")となった。

## 表示モード

MCGAは以下の表示モード（ビデオモード）をサポートする。ビデオモードは[BIOS割り込み](https://ja.wikipedia.org/wiki/BIOS割り込みルーチン "wikilink")(INT 10h, AH=00h, AL=ビデオモード)で切替できる。

  - MCGA独自モード
      - 640x480 モノクロノーム (Mode 11h)
      - 320x200 同時256色（262,144色中） (Mode 13h)
  - CGA互換モード
      - 40桁x25行 テキストモード（8x8 フォント、320x200相当） (Mode 0/1h)
      - 80桁x25行 テキストモード（8x8 フォント、640x200相当） (Mode 2/3h)
      - 320x200 同時4色（16色中） (Mode 4/5h)
      - 640x200 同時2色 (Mode 6h)

## 脚注

## 関連項目

  - [IBM PC](../Page/IBM_PC.md "wikilink")
  - [IBM PS/2](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")
  - [ビデオカード](../Page/ビデオカード.md "wikilink")
  - [画面解像度](../Page/画面解像度.md "wikilink")

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.
2.  <https://files.support.epson.com/pdf/e1e___/e1e___ps.pdf>