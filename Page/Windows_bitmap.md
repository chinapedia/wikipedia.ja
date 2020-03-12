> この記事は[Windows bitmap](https://ja.wikipedia.org/wiki/Windows_bitmap)から翻訳されています。


**BMP**（ビーエムピー、Microsoft Windows **B**it**m**a**p** Image）または**DIB**（ディーアイビー、**D**evice **I**ndependent **B**itmap、デバイス独立ビットマップ）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[IBM](../Page/IBM.md "wikilink")が[Windowsと](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")にわかれる前の[OSを共同で開発していた頃に作られた](../Page/オペレーティングシステム.md "wikilink")[画像](../Page/画像.md "wikilink")ファイル形式。[圧縮の方法についても定義されているが](../Page/データ圧縮.md "wikilink")、Windowsが標準では無圧縮のファイルを生成するため、他のアプリケーションにおいても無指定時は、[圧縮はされていない場合が多い](../Page/データ圧縮.md "wikilink")。

ファイル形式の細部の変更が何度か行われており、その結果としてWindowsとOS/2で多少ファイル形式が異なることがある。

機械独立のファイル形式として設計されたため、実際に存在する画像表示装置（[ディスプレイ](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")）や印刷装置（[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")）が、画像を上方から処理するものがほぼ全てであるにもかかわらず、[幾何学](../Page/幾何学.md "wikilink")的なX軸、Y軸方向に座標を指定する形式となっている。その結果、画像を下から上に向かって記録するボトムアップ形式 (bottom-up) となっていることが特徴であるが、後に高さに負の値を指定することでその他大多数の画像ファイル形式と同じように画像を上から下へ向かって記録するトップダウン形式 (top-down) を使用することもできるようになった。しかし互換性の面からProgramming Windowsではトップダウン形式のビットマップの作成を推奨していない。また、トップダウン形式では後述の圧縮をすることができない。

なお、[ビットマップという呼称は画像データの表現方式のひとつであり](../Page/ビットマップ画像.md "wikilink")、本項で述べている*マイクロソフト独自のファイル形式*を必ずしも指すわけではない\[1\]。

## ファイル構造

ビットマップファイルは、以下のブロックに分かれている。

  - ファイル[ヘッダ](https://ja.wikipedia.org/wiki/ヘッダ_\(コンピュータ\) "wikilink")
    ビットマップファイルについての一般的な情報が格納されている。
  - 情報ヘッダ
    ビットマップイメージについての詳細な情報が格納されている。
  - カラーマスク
    ビットフィールド形式のビットマップで使用されるデータが格納される。
  - カラーパレット
    [インデックスカラー](../Page/インデックスカラー.md "wikilink")ビットマップの場合に使用される色の定義が格納されている。
    [ダイレクトカラー](https://ja.wikipedia.org/wiki/ダイレクトカラー "wikilink")ビットマップの場合は減色時に優先される色が格納される。
  - ビットマップデータ
    実際のイメージが[ピクセル](../Page/ピクセル.md "wikilink")ごとに格納されている。
  - [カラープロファイル](https://ja.wikipedia.org/wiki/カラープロファイル "wikilink")
    [ICCプロファイル](https://ja.wikipedia.org/wiki/ICCプロファイル "wikilink")データそのものか、プロファイルデータのファイルパスが格納される。

[BMPfileFormat.png](https://ja.wikipedia.org/wiki/File:BMPfileFormat.png "fig:BMPfileFormat.png")

### 主な構造

#### OS/2 1.1

|                       |
| :-------------------: |
|  BITMAPFILEHEADER構造体  |
|  BITMAPCOREHEADER構造体  |
| カラーパレット（RGBTRIPLE構造体） |
|         画像データ         |

#### OS/2 2.x

|                      |
| :------------------: |
| BITMAPFILEHEADER2構造体 |
| BITMAPINFOHEADER2構造体 |
|   カラーパレット（RGB2構造体）   |
|        画像データ         |

#### Windows 3.0以降

|                      |
| :------------------: |
| BITMAPFILEHEADER構造体  |
| BITMAPINFOHEADER構造体  |
| カラーマスク（ビットフィールド形式のみ） |
| カラーパレット（RGBQUAD構造体）  |
|        画像データ         |

#### Windows 95以降採用

|                     |
| :-----------------: |
| BITMAPFILEHEADER構造体 |
|  BITMAPV4HEADER構造体  |
| カラーパレット（RGBQUAD構造体） |
|        画像データ        |

#### Windows 98以降採用

|                     |
| :-----------------: |
| BITMAPFILEHEADER構造体 |
|  BITMAPV5HEADER構造体  |
| カラーパレット（RGBQUAD構造体） |
|        画像データ        |
|      カラープロファイル      |

### ファイルヘッダ

#### BITMAPFILEHEADER

14バイトからなる、ビットマップファイルのファイルヘッダである。

| オフセット  | サイズ                                       | 格納する情報  | 値・備考                                                                                               |
| ------ | ----------------------------------------- | ------- | -------------------------------------------------------------------------------------------------- |
| 0x0000 | 2 [バイト](../Page/バイト_\(情報\).md "wikilink") | ファイルタイプ | 常に**BM (0x42, 0x4d)**（[マジックナンバー](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")） |
| 0x0002 | 4バイト                                      | ファイルサイズ | ビットマップファイルのサイズを格納する（単位はバイト）。                                                                       |
| 0x0006 | 2バイト                                      | 予約領域1   | 常に0                                                                                                |
| 0x0008 | 2バイト                                      | 予約領域2   | 常に0                                                                                                |
| 0x000a | 4バイト                                      | オフセット   | ファイルヘッダの先頭アドレスからビットマップデータの先頭アドレスまでのオフセット（単位はバイト）。                                                  |

参考URL

  - [tagBITMAPFILEHEADER | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/wingdi/ns-wingdi-tagbitmapfileheader)

#### BITMAPFILEHEADER2

OS/2 2.xで使用されたファイルヘッダ。BITMAPFILEHEADERを拡張したものだがサイズは同じ。

<table>
<thead>
<tr class="header">
<th><p>オフセット</p></th>
<th><p>サイズ</p></th>
<th><p>格納する情報</p></th>
<th><p>値・備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x0000</p></td>
<td><p>2<a href="../Page/バイト_(情報).md" title="wikilink">バイト</a></p></td>
<td><p>ファイルタイプ</p></td>
<td><p><strong>BM (0x42, 0x4d)</strong>（ビットマップ）<br />
<strong>IC (0x49, 0x43)</strong>（モノクロアイコン）<br />
<strong>CI (0x43, 0x49)</strong>（カラーアイコン）<br />
<strong>PT (0x50, 0x54)</strong>（モノクロポインタ）<br />
<strong>CP (0x43, 0x50)</strong>（カラーポインタ）</p></td>
</tr>
<tr class="even">
<td><p>0x0002</p></td>
<td><p>4バイト</p></td>
<td><p>ヘッダサイズ</p></td>
<td><p>ファイルヘッダと情報ヘッダの合計サイズを格納する。単位はバイト。</p></td>
</tr>
<tr class="odd">
<td><p>0x0006</p></td>
<td><p>2バイト</p></td>
<td><p>ホットスポットx</p></td>
<td><p>ポインタのホットスポットのx座標</p></td>
</tr>
<tr class="even">
<td><p>0x0008</p></td>
<td><p>2バイト</p></td>
<td><p>ホットスポットy</p></td>
<td><p>ポインタのホットスポットのy座標</p></td>
</tr>
<tr class="odd">
<td><p>0x000a</p></td>
<td><p>4バイト</p></td>
<td><p>オフセット</p></td>
<td><p>ファイルヘッダの先頭アドレスからビットマップデータの先頭アドレスまでのオフセット。単位はバイト。</p></td>
</tr>
</tbody>
</table>

  - モノクロアイコン、モノクロポインタは1bitモノクロ画像のみサポートしている。
  - カラーアイコン、カラーポインタは1ファイル内に透過位置を示す1bitモノクロ画像とカラー情報を表す画像を併せ持つ特殊なファイル構造をしている。

### 情報ヘッダ

このブロックは、アプリケーションが画像を描画するための画像の詳細な情報が書かれており、14バイト目から始まる。

14-17 (eh-11h) バイト目は、ヘッダのサイズが書かれている。最大値は、

  - 40 - Windows V3
  - 108 - Windows V4
  - 124 - Windows V5
  - 12 - OS/2 V1
  - 64 - OS/2 V2

#### BITMAPCOREHEADER

OS/2のビットマップで使われる情報ヘッダで、12バイトある。coreヘッダと呼ばれる。

| オフセット  | サイズ                                      | 格納する情報        | 値・備考     |
| ------ | ---------------------------------------- | ------------- | -------- |
| 0x000e | 4[バイト](../Page/バイト_\(情報\).md "wikilink") | ヘッダサイズ        | 12       |
| 0x0012 | 2バイト                                     | ビットマップの横幅     | 単位はピクセル  |
| 0x0014 | 2バイト                                     | ビットマップの縦幅     | 単位はピクセル  |
| 0x0016 | 2バイト                                     | プレーン数         | 常に1      |
| 0x0018 | 2バイト                                     | 1ピクセルあたりのビット数 | 1,4,8,24 |

参考URL

  - [tagBITMAPCOREHEADER | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/wingdi/ns-wingdi-tagbitmapcoreheader)
  - <http://www.programmers@heaven.com/mb/graphics/148346/152845/re-planes/?S=B20000>

（スパムフィルターに引っかかるため[アドレスに](../Page/Uniform_Resource_Locator.md "wikilink")[@](https://ja.wikipedia.org/wiki/@ "wikilink")を入れています。@を除くこと）

#### BITMAPINFOHEADER

Windowsのビットマップで使われる情報ヘッダで、40バイトある。多くのビットマップがこの形式で保存されている。infoヘッダと呼ばれる。

| オフセット  | サイズ                                      | 格納する情報                                     | 値・備考                                |
| ------ | ---------------------------------------- | ------------------------------------------ | ----------------------------------- |
| 0x000e | 4[バイト](../Page/バイト_\(情報\).md "wikilink") | ヘッダサイズ                                     | 40                                  |
| 0x0012 | 4バイト                                     | ビットマップの横幅                                  | 単位はピクセル                             |
| 0x0016 | 4バイト                                     | ビットマップの縦幅                                  | 単位はピクセル。値が負の場合はトップダウン画像となる          |
| 0x001a | 2バイト                                     | プレーン数                                      | 常に1                                 |
| 0x001c | 2バイト                                     | 1ピクセルあたりの[ビット](../Page/ビット.md "wikilink")数 | 0,1,4,8,16,24,32                    |
| 0x001e | 4バイト                                     | 圧縮形式                                       | 0,1,2,3,4,5 ※1                      |
| 0x0022 | 4バイト                                     | 画像データサイズ                                   | 単位はバイト                              |
| 0x0026 | 4バイト                                     | 水平方向の解像度                                   | 単位はピクセル/m                           |
| 0x002a | 4バイト                                     | 垂直方向の解像度                                   | 単位はピクセル/m                           |
| 0x002e | 4バイト                                     | 使用する色数                                     | ビットマップで実際に使用するカラーパレット内のカラーインデックスの数。 |
| 0x0032 | 4バイト                                     | 重要な色数                                      | ビットマップを表示するために必要なカラーインデックスの数。       |

参考URL

  - [BITMAPINFOHEADER (wingdi.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader)

#### BITMAPINFOHEADER2

OS/2 V2以降対応した情報ヘッダである。サイズは可変であり、最大64バイト。Windowsでは対応していない。 \[<http://www.warpspeed.com.au/cgi-bin/inf2html.cmd>?..%5Chtml%5Cbook%5CToolkt40%5CMMREF3.INF+899\]

| オフセット  | サイズ                                      | 格納する情報         | 値・備考                                                                                                                      |
| ------ | ---------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------- |
| 0x000e | 4[バイト](../Page/バイト_\(情報\).md "wikilink") | ヘッダサイズ         | 16～64（可変長）                                                                                                                |
| 0x0012 | 4バイト                                     | ビットマップの横幅      | 単位はピクセル                                                                                                                   |
| 0x0016 | 4バイト                                     | ビットマップの縦幅      | 単位はピクセル                                                                                                                   |
| 0x001a | 2バイト                                     | プレーン数          | 常に1                                                                                                                       |
| 0x001c | 2バイト                                     | 1ピクセルあたりのビット数  | 1,4,8,24                                                                                                                  |
| 0x001e | 4バイト                                     | 圧縮形式           | 0（非圧縮）,1（8bit [RLE](../Page/連長圧縮.md "wikilink")）,2（4bit RLE）,3（1bit[ハフマン符号](../Page/ハフマン符号.md "wikilink")圧縮）,4（24bit RLE） |
| 0x0022 | 4バイト                                     | 画像データサイズ       | 単位はバイト。非圧縮の場合は0を入れても良い                                                                                                    |
| 0x0026 | 4バイト                                     | 水平方向の解像度       | 単位は「解像度の単位」で指定される                                                                                                         |
| 0x002a | 4バイト                                     | 垂直方向の解像度       |                                                                                                                           |
| 0x002e | 4バイト                                     | 使用する色数         | ビットマップで実際に使用するカラーパレット内のカラーインデックスの数。                                                                                       |
| 0x0032 | 4バイト                                     | 重要な色数          | ビットマップを表示するために必要なカラーインデックスの数。                                                                                             |
| 0x0036 | 2バイト                                     | 解像度の単位         | 0（ピクセル/m）                                                                                                                 |
| 0x0038 | 2バイト                                     | 予約領域           | 常に0                                                                                                                       |
| 0x003a | 2バイト                                     | 記録方式           | 0（ボトムアップ）                                                                                                                 |
| 0x003c | 2バイト                                     | ハーフトーンの方式      | 0（ハーフトーンなし）, 1（誤差拡散法）, 2（PANDA）, 3（Super Circle）                                                                          |
| 0x003e | 4バイト                                     | ハーフトーン時のパラメータ1 |                                                                                                                           |
| 0x0042 | 4バイト                                     | ハーフトーン時のパラメータ2 | 誤差拡散法の場合は無視される                                                                                                            |
| 0x0046 | 4バイト                                     | 符号化方式          | 0（RGB2、RGBQUADに相当）                                                                                                        |
| 0x004a | 4バイト                                     | 識別子            | アプリケーションが独自に使用してもよい領域                                                                                                     |

#### BITMAPV3INFOHEADER

Adobe Photoshopで使用されていた情報ヘッダ。infoヘッダにRGBとα成分のカラーマスクを取り込んだ56バイトのヘッダで、便宜上V3ヘッダと呼ばれる。

Adobe社によると、V3ヘッダの仕様は、過去にMicrosoftから取り寄せた文書に記載されていたそうである\[2\]。

#### BITMAPV4HEADER

Windows 95、Windows NT 4.0から対応した情報ヘッダ。V4ヘッダと呼ばれる。

<table>
<thead>
<tr class="header">
<th><p>オフセット</p></th>
<th><p>サイズ</p></th>
<th><p>格納する情報</p></th>
<th><p>値・備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x000e</p></td>
<td><p>4<a href="../Page/バイト_(情報).md" title="wikilink">バイト</a></p></td>
<td><p>ヘッダサイズ</p></td>
<td><p>108</p></td>
</tr>
<tr class="even">
<td><p>0x0012</p></td>
<td><p>4バイト</p></td>
<td><p>ビットマップの横幅</p></td>
<td><p>infoヘッダと同等</p></td>
</tr>
<tr class="odd">
<td><p>0x0016</p></td>
<td><p>4バイト</p></td>
<td><p>ビットマップの縦幅</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x001a</p></td>
<td><p>2バイト</p></td>
<td><p>プレーン数</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>0x001c</p></td>
<td><p>2バイト</p></td>
<td><p>1ピクセルあたりのビット数</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x001e</p></td>
<td><p>4バイト</p></td>
<td><p>圧縮形式</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>0x0022</p></td>
<td><p>4バイト</p></td>
<td><p>画像データサイズ</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x0026</p></td>
<td><p>4バイト</p></td>
<td><p>水平方向の解像度</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>0x002a</p></td>
<td><p>4バイト</p></td>
<td><p>垂直方向の解像度</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x002e</p></td>
<td><p>4バイト</p></td>
<td><p>使用する色数</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>0x0032</p></td>
<td><p>4バイト</p></td>
<td><p>重要な色数</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x0036</p></td>
<td><p>4バイト</p></td>
<td><p>赤成分のカラーマスク</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>0x003a</p></td>
<td><p>4バイト</p></td>
<td><p>緑成分のカラーマスク</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x003e</p></td>
<td><p>4バイト</p></td>
<td><p>青成分のカラーマスク</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>0x0042</p></td>
<td><p>4バイト</p></td>
<td><p>α成分のカラーマスク</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x0046</p></td>
<td><p>4バイト</p></td>
<td><p>色空間</p></td>
<td><p>0(ヘッダ内で定義)</p></td>
</tr>
<tr class="odd">
<td><p>0x004a</p></td>
<td><p>36バイト</p></td>
<td><p>CIEXYZTRIPLE構造体</p></td>
<td><p>色空間が0の場合のみ有効</p></td>
</tr>
<tr class="even">
<td><p>0x006e</p></td>
<td><p>4バイト</p></td>
<td><p>赤成分のガンマ値</p></td>
<td><p>色空間が0の場合のみ有効<br />
16.16の固定小数点数</p></td>
</tr>
<tr class="odd">
<td><p>0x0072</p></td>
<td><p>4バイト</p></td>
<td><p>緑成分のガンマ値</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0x0076</p></td>
<td><p>4バイト</p></td>
<td><p>青成分のガンマ値</p></td>
<td></td>
</tr>
</tbody>
</table>

参考URL

  - [BITMAPV4HEADER (wingdi.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/wingdi/ns-wingdi-bitmapv4header)

#### BITMAPV5HEADER

Windows 98、Windows 2000から対応した情報ヘッダ。V5ヘッダと呼ばれる。

| オフセット  | サイズ                                      | 格納する情報          | 値・備考                                                                                       |
| ------ | ---------------------------------------- | --------------- | ------------------------------------------------------------------------------------------ |
| 0x000e | 4[バイト](../Page/バイト_\(情報\).md "wikilink") | ヘッダサイズ          | 124                                                                                        |
| 0x0012 | 4バイト                                     | ビットマップの横幅       | infoヘッダと同等                                                                                 |
| 0x0016 | 4バイト                                     | ビットマップの縦幅       |                                                                                            |
| 0x001a | 2バイト                                     | プレーン数           |                                                                                            |
| 0x001c | 2バイト                                     | 1ピクセルあたりのビット数   |                                                                                            |
| 0x001e | 4バイト                                     | 圧縮形式            |                                                                                            |
| 0x0022 | 4バイト                                     | 画像データサイズ        |                                                                                            |
| 0x0026 | 4バイト                                     | 水平方向の解像度        |                                                                                            |
| 0x002a | 4バイト                                     | 垂直方向の解像度        |                                                                                            |
| 0x002e | 4バイト                                     | 使用する色数          |                                                                                            |
| 0x0032 | 4バイト                                     | 重要な色数           |                                                                                            |
| 0x0036 | 4バイト                                     | 赤成分のカラーマスク      | V4ヘッダと同等                                                                                   |
| 0x003a | 4バイト                                     | 緑成分のカラーマスク      |                                                                                            |
| 0x003e | 4バイト                                     | 青成分のカラーマスク      |                                                                                            |
| 0x0042 | 4バイト                                     | α成分のカラーマスク      |                                                                                            |
| 0x0046 | 4バイト                                     | 色空間             | 0(ヘッダ内で定義), 0x73524742('sRGB'), 0x57696e20('Win '), 0x4c494e4b('LINK'), 0x4d424544('MBED') |
| 0x006a | 36バイト                                    | CIEXYZTRIPLE構造体 | V4ヘッダと同等                                                                                   |
| 0x006e | 4バイト                                     | 赤成分のガンマ値        |                                                                                            |
| 0x0072 | 4バイト                                     | 緑成分のガンマ値        |                                                                                            |
| 0x0076 | 4バイト                                     | 青成分のガンマ値        |                                                                                            |
| 0x007a | 4バイト                                     | レンダリングの意図       | 1,2,4,8                                                                                    |
| 0x007e | 4バイト                                     | プロファイルデータのオフセット | 情報ヘッダの先頭アドレスからプロファイルデータの先頭アドレスまでのオフセット。単位はバイト                                              |
| 0x0082 | 4バイト                                     | プロファイルデータのサイズ   | 単位はバイト                                                                                     |
| 0x0086 | 4バイト                                     | 予約領域            | 常に0                                                                                        |

参考URL

  - [BITMAPV5HEADER (wingdi.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header)

#### 各フィールドの詳細

##### プレーン数

過去に、EGAやVGAディスプレイカードで使われていた概念で、現在は全く使われない。

この概念が使われていた頃は、実際の色深度を「1ピクセルあたりのビット数×プレーン数」で算出する必要があった。

##### 圧縮形式

※1 数値と定義されている圧縮形式の関係は以下の通り\[3\]

  - 0 - 無圧縮（識別子はBI_RGB）
  - 1 - 8ビット/ピクセル [RLE](../Page/連長圧縮.md "wikilink")（識別子はBI_RLE8）
  - 2 - 4ビット/ピクセル RLE（識別子はBI_RLE4）
  - 3 - ビットフィールド（識別子はBI_BITFIELDS）
  - 4 - [JPEG](../Page/JPEG.md "wikilink")画像（識別子はBI_JPEG）
  - 5 - [PNG画像](../Page/Portable_Network_Graphics.md "wikilink")（識別子はBI_PNG）

上記以外の圧縮形式は以下の通り

  - 3 - 1ビットハフマン符号化（OS/2 2.x、識別子はHUFFMAN_1D）
  - 4 - 24ビット/ピクセル RLE（OS/2 2.x、識別子はRLE_24）
  - 6 - アルファチャンネル付きビットフィールド（[Windows CE 5.0](https://ja.wikipedia.org/wiki/Windows_CE_5.0 "wikilink")、識別子はBI_ALPHABITFIELDS）

##### 水平・垂直方向の解像度

画像の表示に適したデバイスの解像度を指定する。この値を設定することで、例えばソフトウェアが画面の解像度に合った最適なサイズの画像を選択できるようになる。

##### 色空間

V4ヘッダで、'Win 'と'sRGB'が使用できるというドキュメントが存在する。

### カラーマスク

カラーマスクはビットフィールド形式が使用されているビットマップから各色成分を取り出す際に使用されるデータである。赤成分、緑成分、青成分の順で書かれており、それぞれ4バイト、合計12バイトである。 Windows CEで圧縮形式に「アルファチャンネル付きビットフィールド」を使用した場合は、この後ろにα成分のカラーマスクが置かれ合計16バイトになる。

カラーマスクブロックは、情報ヘッダがINFOヘッダかつビットフィールド形式が使用されている場合に必ず存在する。 V4、V5ヘッダの場合は、ヘッダ内に値が格納されるためこのブロックは置く必要がない。

1ピクセルあたりのビット数とカラーマスクの組み合わせが以下である場合は、圧縮形式を非圧縮に設定し、カラーマスクブロックを省略できる。

|            | 16ビット      | 32ビット      |
| ---------- | ---------- | ---------- |
| 赤成分のカラーマスク | 0x00007C00 | 0x00FF0000 |
| 緑成分のカラーマスク | 0x000003E0 | 0x0000FF00 |
| 青成分のカラーマスク | 0x0000001F | 0x000000FF |

### カラーパレット

このブロックは、画像内で使用される色を定義している。上述の通り、ビットマップ画像はピクセルごとに保存されている。各ピクセルは、1バイト以上を使用して値を保持している。したがって、各値と実際の色の関係を、アプリケーションに教えることがカラーパレットの目的である。

典型的なビットマップファイルは[RGB](../Page/RGB.md "wikilink")カラーモデルを使用している。このモデルにおいて、色は[赤](../Page/赤.md "wikilink") (R)、[緑](../Page/緑.md "wikilink") (G)、[青](../Page/青.md "wikilink") (B) のそれぞれの強さ (0-255) で表される。

#### RGBTRIPLE

1色3バイトで表記する形式。情報ヘッダがcoreヘッダの場合のみ使用される。

| バイト数 | 情報 | 値・備考  |
| ---- | -- | ----- |
| 1バイト | 青  | 0-255 |
| 1バイト | 緑  | 0-255 |
| 1バイト | 赤  | 0-255 |

#### RGBQUAD

1色4バイトで表記する形式、OS/2ビットマップにおけるRGB2もこちらに相当する。

| バイト数 | 情報   | 値・備考  |
| ---- | ---- | ----- |
| 1バイト | 青    | 0-255 |
| 1バイト | 緑    | 0-255 |
| 1バイト | 赤    | 0-255 |
| 1バイト | 予約領域 |       |

### ビットマップデータ

このブロックは、イメージを各ピクセルごとに記述する。ピクセルは通常、左下から右下へ、これを下から上に向かって保存する。各ピクセルは1バイト以上で記述されている。直接RGBデータが置かれる場合のデータ順は、上項カラーパレットに準ずる。水平方向のバイト数が[4](https://ja.wikipedia.org/wiki/4 "wikilink")の[倍数](../Page/倍数.md "wikilink")ではないときは、0x00で埋めて4の倍数にする。

### カラープロファイル

このブロックは、情報ヘッダの「色空間」が'LINK'の場合はカラープロファイルデータのファイルパスが、'MBED'の場合はデータそのものが格納される。 ファイルヘッダの「オフセット」の値によってはビットマップデータよりも前に格納することも出来る。

## BMPを取り扱うプログラムライブラリ

プログラムでBMP画像を平易に扱うためのライブラリも数多く存在している。

  - [Windows API](../Page/Windows_API.md "wikilink") ([GDI](../Page/Graphics_Device_Interface.md "wikilink")), HBITMAP\[4\]

<!-- end list -->

  -
    ビットマップデータを管理するオブジェクトハンドル。BMP形式画像をファイルやリソースから読み込んでHBITMAPを生成することのできる各種[C言語](../Page/C言語.md "wikilink")形式関数が用意されている。Windowsデスクトップアプリケーション専用。

<!-- end list -->

  - [Microsoft Foundation Class](../Page/Microsoft_Foundation_Class.md "wikilink") (MFC), CBitmapクラス\[5\]

<!-- end list -->

  -
    マイクロソフトが提供している開発環境である[Visual C++に付属する](https://ja.wikipedia.org/wiki/Visual_C++ "wikilink")、ビットマップ操作クラス。Win32 APIのラッパー。Windowsデスクトップアプリケーション専用。

<!-- end list -->

  - [Active Template Library](../Page/Active_Template_Library.md "wikilink") (ATL), ATL::CImageクラス\[6\]

<!-- end list -->

  -
    マイクロソフトが提供している開発環境である[Visual C++に付属する](https://ja.wikipedia.org/wiki/Visual_C++ "wikilink")、ビットマップ操作クラス。Win32 APIおよびGDI+のラッパー。Windowsデスクトップアプリケーション専用。

<!-- end list -->

  - [GDI+](https://ja.wikipedia.org/wiki/GDI+ "wikilink"), Gdiplus::Bitmapクラス\[7\]

<!-- end list -->

  -
    [Windows SDKに付属する](https://ja.wikipedia.org/wiki/Windows_SDK "wikilink")、[C++](../Page/C++.md "wikilink")言語専用のビットマップ操作クラス。Windowsデスクトップアプリケーション専用。

<!-- end list -->

  - [Windows Imaging Component](https://ja.wikipedia.org/wiki/Windows_Imaging_Component "wikilink") (WIC)

<!-- end list -->

  -
    [COMベースの画像ライブラリ](../Page/Component_Object_Model.md "wikilink")。Windowsデスクトップアプリケーション/[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリから利用可能。

<!-- end list -->

  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink"), System.Drawing\[8\]

<!-- end list -->

  -
    GDI+のマネージラッパー。Windowsデスクトップアプリケーション専用。
    [Monoにも互換実装が存在する](../Page/Mono_\(ソフトウェア\).md "wikilink")\[9\]。

<!-- end list -->

  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink"), System.Windows.Media.Imaging\[10\]

<!-- end list -->

  -
    WICのマネージラッパー。Windowsデスクトップアプリケーション/[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリから利用可能。

サードパーティ製のライブラリに関しての各詳細は、外部リンクの項に記載している。

## 脚注

## 関連項目

  - [ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")
  - [ビットマップ画像](../Page/ビットマップ画像.md "wikilink")

## 外部リンク

  - [libbmp24](http://doscoy.github.io/libbmp24) C++で書かれたオープンソースライブラリ。1つのヘッダーファイルのみで構成されており組み込みが容易。
  - [Imager](http://imager.perl.org/) [Perl](../Page/Perl.md "wikilink")用モジュール。ほとんどの画像形式に対応しており、他ライブラリとの依存も少なく高速に動作する画像ライブラリ。

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:ラスターグラフィックス・ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ラスターグラフィックス・ファイルフォーマット "wikilink")

1.  より一般的な意味合いについては[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")の項を参考。
2.  [Invalid BMP Format with Alpha channel](https://forums.adobe.com/message/3272950)
3.  [\[MS-WMF](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4e588f70-bd92-4a6f-b77f-35d0feaf7a57): Compression Enumeration | Microsoft Docs\]
4.  [Windows Data Types - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/WinProg/windows-data-types)
5.  [CBitmap Class | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/mfc/reference/cbitmap-class)
6.  [CImage Class | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/atl-mfc-shared/reference/cimage-class)
7.  [Bitmap (gdiplusheaders.h) | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)
8.  [System.Drawing Namespace | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.drawing)
9.  [Drawing | Mono](https://www.mono-project.com/docs/gui/drawing/)
10. [System.Windows.Media.Imaging Namespace | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.windows.media.imaging)