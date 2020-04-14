> この記事は[Monochrome Display Adapter](https://ja.wikipedia.org/wiki/Monochrome_Display_Adapter)から翻訳されています。


[IBM_PC_Original_Monochrome_Display_and_Parallel_Printer_Adapter.jpg](https://ja.wikipedia.org/wiki/File:IBM_PC_Original_Monochrome_Display_and_Parallel_Printer_Adapter.jpg "fig:IBM_PC_Original_Monochrome_Display_and_Parallel_Printer_Adapter.jpg") **Monochrome Display Adapter** (モノクローム ディスプレイ アダプター、**MDA**) は、[1981年](../Page/1981年.md "wikilink")に[IBM PC用に開発された標準](../Page/IBM_PC.md "wikilink")[ビデオカード](../Page/ビデオカード.md "wikilink")である。[CGAとともに](../Page/Color_Graphics_Adapter.md "wikilink")、IBM PCおよびその互換機用の最初の標準ビデオカードであった。

MDAには4K[バイトの](../Page/バイト_\(情報\).md "wikilink")[VRAM](../Page/VRAM.md "wikilink")が搭載され、80桁×25行のテキストを表示することができた。また、プリンタインターフェースを持っており、当時求められていた、テキスト表示とプリントアウトのための機能を考えると、お買い得であった。コントローラは、CGA同様モトローラ[MC6845](https://ja.wikipedia.org/wiki/MC6845 "wikilink")を用いている。

グラフィックスの解像度としては、720×350[ピクセル](../Page/ピクセル.md "wikilink")に相当するため、後にこの解像度でグラフィック表示を行える [Hercules Graphics Card](../Page/Hercules_Graphics_Card.md "wikilink") がHercules社から発売され、おりからの[スプレッドシート](https://ja.wikipedia.org/wiki/スプレッドシート "wikilink")ブームと相まって爆発的な売れ行きを示したと言う。

## 機能

MDAの合計画面解像度は720×350ピクセルで、9ピクセル幅が80字と14ピクセルの高さが25行の文字で構成される。しかし、MDAは各ピクセルを個別に扱うことはできず、各位置に256種類の文字を表示するテキストモードのみを備える。その始めの128字は標準的な[ASCII](../Page/ASCII.md "wikilink")文字セット。後の128字はアクセント文字、[ローマン体](../Page/ローマン体.md "wikilink")、数学記号やグラフィック文字を含んでおり、[拡張ASCII](../Page/拡張ASCII.md "wikilink")として知られる。この文字セットは[コードページ](../Page/コードページ.md "wikilink")437として知られる。[フォント](../Page/フォント.md "wikilink")パターンは8KBの[ROMに記憶されており](../Page/Read_only_memory.md "wikilink")、ソフトウェアから変更することはできない。[アスキーアート](../Page/アスキーアート.md "wikilink")が「グラフィカル」に表示を行う唯一の方法である。

## 文字アトリビュート

MDAによって生成される文字は、非表示、下線、通常、明瞭（ボールド）、反転、点滅の属性を持っている。いくつかの属性は組み合わせて使うことができる。

| 属性     | 表示例                |
| ------ | ------------------ |
| 非表示    | `非表示`              |
| 通常     | `通常`               |
| 下線     | <u>`下線`</u>        |
| 明瞭     | **`明瞭`**           |
| 明瞭・下線  | <u>**`明瞭・下線`**</u> |
| 反転     | `反転`               |
| 非表示・反転 | `非表示・反転`           |

## コネクタ

MDAのコネクタは [DE-9である](https://ja.wikipedia.org/wiki/D-subminiature#9pin（DE-9コネクタ） "wikilink")。ピン番号は順にソケット正面の右上から左上、右下から左下へ。

[DE9_Diagram.svg](https://ja.wikipedia.org/wiki/File:DE9_Diagram.svg "fig:DE9_Diagram.svg")

| **ピン番号** | **機能**    |
| -------- | --------- |
| 1        | GND       |
| 2        | GND       |
| 3        | （未使用）     |
| 4        | （未使用）     |
| 5        | （未使用）     |
| 6        | 輝度        |
| 7        | 映像信号      |
| 8        | 水平同期（正論理） |
| 9        | 垂直同期（負論理） |
|          |           |

**ピン配置**

## 信号

| 方式      | TTLレベル                   |
| ------- | ------------------------ |
| 解像度     | 80文字x25行、720ドットx350ライン相当 |
| 水平同期周波数 | 18.432 kHz               |
| 垂直同期周波数 | 50 Hz                    |
| 階調数     | 2-4                      |

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")