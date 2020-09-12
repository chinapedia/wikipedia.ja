> この記事は[PowerVR](https://ja.wikipedia.org/wiki/PowerVR)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Matrox_m3D_\(Rev_757-00B\).png "wikilink") m3D\]\] **PowerVR**（パワーブイアール）は、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の[ファブレス](../Page/ファブレス.md "wikilink")企業である[ビデオロジック](https://ja.wikipedia.org/wiki/ビデオロジック "wikilink")（現：）が開発した、[グラフィックコントローラ](../Page/グラフィックコントローラ.md "wikilink")[IPコア](../Page/IPコア.md "wikilink")およびそれを[集積回路](../Page/集積回路.md "wikilink")として実装したグラフィックチップである。チップ製造は[NECや](../Page/日本電気.md "wikilink")[STマイクロエレクトロニクス](../Page/STマイクロエレクトロニクス.md "wikilink")\[1\]等が行なってきた。当初、メインターゲットとされていた[パソコン用](../Page/パーソナルコンピュータ.md "wikilink")[ビデオカード](../Page/ビデオカード.md "wikilink")としては、ほとんど普及しなかったが、比較的メモリへの負荷が少ないというその特徴から、家庭用[ゲーム機](../Page/ゲーム機.md "wikilink")および[アーケードゲーム基板](../Page/アーケードゲーム基板.md "wikilink")、[携帯電話](../Page/携帯電話.md "wikilink")、[携帯情報端末](../Page/携帯情報端末.md "wikilink") (PDA)、[カーナビゲーション](../Page/カーナビゲーション.md "wikilink")といった[組み込みシステム](../Page/組み込みシステム.md "wikilink")に広く採用されている。

また [Intel Atom](../Page/Intel_Atom.md "wikilink")、Apple Axシリーズ、[Texas Instruments OMAP](../Page/Texas_Instruments_OMAP.md "wikilink") などに GPU として組み込まれ、携帯電話・タブレットなどに広く採用されている。

特徴は、[Zバッファ](../Page/Zバッファ.md "wikilink")法で通常行なうような「手前にある物体は上書きする」という方式を採らず、「一番手前の物体しか描画しない」という手法により、Zバッファ用のメモリをほぼ不要にした点である。タイル単位でこの処理を行なうことから "tile-based deferred rendering" と呼んでおり、TBDRと略す（詳細は[w:Tiled renderingを参照](https://ja.wikipedia.org/wiki/w:Tiled_rendering "wikilink")）。2009年現在、[OpenGL ESの](../Page/OpenGL_ES.md "wikilink")[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")や、[H.264](../Page/H.264.md "wikilink")や[MPEG-2](../Page/MPEG-2.md "wikilink")、[MPEG-4](../Page/MPEG-4.md "wikilink")などの動画コーデックに対応した高機能な製品をリリースしている。

## ラインナップ

  - PowerVR シリーズ1 (PCX1, μPD62010およびPCX2, μPD62011)
    1996年、秒間30万ポリゴンのPCX1発表。1997年、性能が秒間45万ポリゴンに向上したPCX2発表。これらは3D演算機能と4MBの専用RAMのみ搭載したPCIバスのボードで、表示には別途ビデオカードが必要となる。ビデオキャプチャボードのオーバーレイ機能と同様に、DirectDrawを経由し、ビデオカードのVRAMに直接表示データを書き込む。グラフィックライブラリはDirect3Dのほか、オリジナルのSGL (Super Graphics Library) が利用できる。
  - PowerVR シリーズ2 (PowerVR2)
    1998年2月23日発表。2D表示機能を搭載し、単独で使用できる2D/3Dビデオカードとなった。[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")に搭載されているほか、PC用のAGPカードも存在したが、日本ではほとんど普及しなかった。

[PowerVR3 KYRO II](https://ja.wikipedia.org/wiki/画像:STMicroelectronics_STG4500_\(PowerVR_Kyro_II\).png "wikilink")

  - PowerVR シリーズ3
    2000年、[KYRO](../Page/KYRO.md "wikilink")発表。KYRO IIは2001年発表。KYROのバグフィックスとクロックアップ。
  - PowerVR シリーズ4
    PowerVR シリーズ5
    PowerVR VXD370
    HD（[ハイディフィニション](https://ja.wikipedia.org/wiki/ハイディフィニション "wikilink")) 品質のデコードなどに向けた[IPコア](../Page/IPコア.md "wikilink")。
  - PowerVR M2VXファミリー
    SD（標準精細度）品質のデコードなどに向けたIPコア。
  - PowerVR MVED1
    モバイル機器に向けたIPコア。

## PowerVR チップセットの一覧

  - <sup>\[1\]</sup> 公式 Imgtec データ
  - <sup>\[2\]</sup> USSE (Universal Scalable Shader Engine) pipes/TMUs
  - <sup>\[3\]</sup> USSE2 (Universal Scalable Shader Engine 2) pipes/TMUs
  - 全モデル Tile based deferred rendering (TBDR) 対応

### Series 1

  - 全モデル [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 3.0 サポート

| モデル    | Launch   | Fab (nm)   | メモリ (MiB) | コアクロック (MHz) | メモリクロック (MHz) | 設定コア<sup>1</sup>                       | [フィルレート](https://ja.wikipedia.org/wiki/フィルレート "wikilink") | メモリ |
| ------ | -------- | ---------- | --------- | ------------ | ------------- | -------------------------------------- | --------------------------------------------------------- | --- |
| メガ命令/s | メガピクセル/s | MTextels/s | メガ頂点/s    | 帯域 (GB/s)    | バス種別          | バス幅 ([ビット](../Page/ビット.md "wikilink")) |                                                           |     |
| PCX1   | 1996     | 500        | 4         | 60           | 60            | 1:0:1:1                                | 60                                                        | 60  |
| PCX2   | 1997     | 350        | 4         | 66           | 66            | 1:0:1:1                                | 66                                                        | 66  |
|        |          |            |           |              |               |                                        |                                                           |     |

  - <sup>1</sup> ピクセルシェーダ : 頂点シェーダ : テクスチャマッピングユニット : レンダー出力ユニット

### Series 2

  - 全モデル 250 nm プロセスで製造
  - 全モデル [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 6.0 対応。PMX1 は Mini-GL 対応。

| モデル    | Launch   | メモリ (MiB)  | コアクロック (MHz) | メモリクロック (MHz) | 設定コア<sup>1</sup> | フィルレート                                 | メモリ |
| ------ | -------- | ---------- | ------------ | ------------- | ---------------- | -------------------------------------- | --- |
| メガ命令/s | メガピクセル/s | MTextels/s | メガ頂点/s       | 帯域 (GB/s)     | バス種別             | バス幅 ([ビット](../Page/ビット.md "wikilink")) |     |
| CLX2   | 1998     | 8          | 100          | 100           | 1:0:1:1          | 100                                    | 100 |
| PMX1   | 1999     | 32         | 125          | 125           | 1:0:1:1          | 125                                    | 125 |
|        |          |            |              |               |                  |                                        |     |

  - <sup>1</sup> ピクセルシェーダ : 頂点シェーダ : テクスチャマッピングユニット : レンダー出力ユニット

### Series 3

  - 全モデル [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 6.0 対応

| モデル     | Launch         | Fab (nm)   | メモリ (MiB) | コアクロック (MHz) | メモリクロック (MHz) | 設定コア<sup>1</sup>                       | フィルレート | メモリ  |
| ------- | -------------- | ---------- | --------- | ------------ | ------------- | -------------------------------------- | ------ | ---- |
| メガ命令/s  | メガピクセル/s       | MTextels/s | メガ頂点/s    | 帯域 (GB/s)    | バス種別          | バス幅 ([ビット](../Page/ビット.md "wikilink")) |        |      |
| STG4000 | 2000           | 250        | 32/64     | 115          | 115           | 2:0:2:2                                | 230    | 230  |
| STG4500 | 2001           | 180        | 32/64     | 175          | 175           | 2:0:2:2                                | 350    | 350  |
| STG4800 | Never Released | 180        | 64        | 200          | 200           | 2:0:2:2                                | 400    | 400  |
| STG5500 | Never Released | 130        | 64        | 250          | 250           | 4:0:4:4                                | 1000   | 1000 |
|         |                |            |           |              |               |                                        |        |      |

  - <sup>1</sup> ピクセルシェーダ : 頂点シェーダ : テクスチャマッピングユニット : レンダー出力ユニット

### Series 4

| モデル                     | 年                        | ダイサイズ (mm<sup>2</sup>)<sup>\[1\]</sup>                      | 設定コア                                   | フィルレート (@ 200 MHz) | バス幅 ([ビット](../Page/ビット.md "wikilink")) | [API](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink") (version) |
| ----------------------- | ------------------------ | ----------------------------------------------------------- | -------------------------------------- | ------------------ | -------------------------------------- | ------------------------------------------------------------------------------------------- |
| メガ三角形/s<sup>\[1\]</sup> | メガピクセル/s<sup>\[1\]</sup> | [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") | [OpenGL](../Page/OpenGL.md "wikilink") |                    |                                        |                                                                                             |
| MBX Lite                | Feb 2001                 | 4@130 nm?                                                   | 0/1/1/1                                | 1.0                | 100                                    | 64                                                                                          |
| MBX                     | Feb 2001                 | 8@130 nm?                                                   | 0/1/1/1                                | 1.68               | 150                                    | 64                                                                                          |

### Series 5

| モデル                     | 年                        | ダイサイズ (mm<sup>2</sup>)<sup>\[1\]</sup>                      | 設定コア<sup>\[2\]</sup>                   | フィルレート (@ 200 MHz)                           | バス幅 ([ビット](../Page/ビット.md "wikilink")) | [API](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink") (version) | GFLOPS(@ 200 MHz) |
| ----------------------- | ------------------------ | ----------------------------------------------------------- | -------------------------------------- | -------------------------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------- | ----------------- |
| メガ三角形/s<sup>\[1\]</sup> | メガピクセル/s<sup>\[1\]</sup> | [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") | [OpenGL](../Page/OpenGL.md "wikilink") | [OpenGL ES](../Page/OpenGL_ES.md "wikilink") |                                        |                                                                                             |                   |
| SGX520                  | Jul 2005                 | 2.6@65 nm                                                   | 1/1                                    | 7                                            | 250                                    | 64                                                                                          | N/A               |
| SGX530                  | Jul 2005                 | 7.2@65 nm                                                   | 2/1                                    | 14                                           | 500                                    | 64                                                                                          | N/A               |
| SGX531                  | Oct 2006                 | 65 nm                                                       | 2/1                                    | 14                                           | 500                                    | 64                                                                                          | N/A               |
| SGX535                  | Nov 2007                 | 65 nm                                                       | 2/2                                    | 14                                           | 500                                    | 64                                                                                          | 9.0L              |
| SGX540                  | Nov 2007                 | 65 nm                                                       | 4/2                                    | 20                                           | 1000                                   | 64                                                                                          | N/A               |
| SGX545                  | Jan 2010                 | 12.5@65 nm                                                  | 4/2                                    | 40                                           | 1000                                   | 64                                                                                          | 10.1              |

### Series 5XT

| モデル                     | 日時                       | コア                                                          | ダイサイズ (mm<sup>2</sup>)<sup>\[1\]</sup> | 設定コア<sup>\[3\]</sup>                   | フィルレート (@ 200 MHz) | バス幅 ([ビット](../Page/ビット.md "wikilink")) | API (version) | GFLOPS(@ 200 MHz,per core) |
| ----------------------- | ------------------------ | ----------------------------------------------------------- | -------------------------------------- | -------------------------------------- | ------------------ | -------------------------------------- | ------------- | -------------------------- |
| メガ三角形/s<sup>\[1\]</sup> | メガピクセル/s<sup>\[1\]</sup> | [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") | [OpenGL](../Page/OpenGL.md "wikilink") | [OpenCL](../Page/OpenCL.md "wikilink") |                    |                                        |               |                            |
| SGX543                  | Jan 2009                 | 1-16                                                        | 5.4@40nm                               | 4/2                                    | 35                 | 1000                                   | 64            | 9.0L                       |
| SGX544                  | Jun 2010                 | 1-16                                                        | 5.4@40nm                               | 4/2                                    | 35                 | 1000                                   | 64            | 9.0                        |
| SGX554                  | Dec 2010                 | 1-16                                                        | 8.7@40nm                               | 8/2                                    | 〜50                | 1000                                   | 64            | 9.0                        |

これらの GPU はシングルコアでもマルチコアでも利用可能。\[2\]

### Series 6

| モデル      | 日時       | コア                                                          | ダイサイズ (mm<sup>2</sup>)                 | 設定コア<sup>\[3\]</sup> | フィルレート (@600MHz) | バス幅 ([ビット](../Page/ビット.md "wikilink")) | API (バージョン) | G[FLOPS](../Page/FLOPS.md "wikilink") (@600MHz) |
| -------- | -------- | ----------------------------------------------------------- | -------------------------------------- | -------------------- | ---------------- | -------------------------------------- | ----------- | ----------------------------------------------- |
| メガポリゴン/s | メガピクセル/s | [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") | [OpenGL](../Page/OpenGL.md "wikilink") | OpenGL ES            |                  |                                        |             |                                                 |
| G6100    | Feb 2013 | 1                                                           | ??@20 nm                               | 1/1                  | ?                | ?                                      | ?           | 9.0 L3                                          |
|          |          |                                                             |                                        |                      |                  |                                        |             |                                                 |
| G6200    | Jan 2012 | 1                                                           | ??@20 nm                               | 2/1                  | 175              | 2.5(effective fill rate 6.5)           | ?           | 10.1/11.1                                       |
| G6230    | Jun 2012 | 1                                                           | ??@20 nm                               | 2/1                  | 175              | 2.5(effective fill rate 6.5)           | ?           | 10.1/11.1                                       |
| G6400    | Jan 2012 | 1                                                           | ??@20 nm                               | 4/2                  | 350              | 5(effective fill rate 13)              | ?           | 10.1/11.1                                       |
| G6430    | Jun 2012 | 1                                                           | ??@20 nm                               | 4/2                  | 350              | 5(effective fill rate 13)              | ?           | 10.1/11.1                                       |
| G6630    | Nov 2012 | 1                                                           | ??@20 nm                               | 6/3                  | 525              | 7.5(effective fill rate 19.5)          | ?           | 10.1/11.1                                       |

USSEx, 第6世代TBDR\[3\]

### Series 6XE

[2014年](../Page/2014年.md "wikilink")[1月6日](../Page/1月6日.md "wikilink")発表。\[4\]\[5\]

<table>
<thead>
<tr class="header">
<th><p>Model</p></th>
<th><p>Date</p></th>
<th><p>Clusters</p></th>
<th><p>Die Size (mm<sup>2</sup>)</p></th>
<th><p>Config core<sup>[4]</sup></p></th>
<th><p>SIMD lane</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Fillrate" title="wikilink">Fillrate</a></p></th>
<th><p>Bus width<br />
(<a href="https://ja.wikipedia.org/wiki/bit" title="wikilink">bit</a>)</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Heterogeneous_System_Architecture" title="wikilink">HSA</a>-features</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Application_programming_interface" title="wikilink">API</a> (version)</p></th>
<th><p>GFLOPS(@ 650 MHz)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>MPolygons/s</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Pixel" title="wikilink">GP</a>/s)</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Texel_(graphics)" title="wikilink">GT</a>/s)</p></td>
<td><p><a href="../Page/OpenGL_ES.md" title="wikilink">OpenGL ES</a></p></td>
<td><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></td>
<td><p><a href="../Page/OpenCL.md" title="wikilink">OpenCL</a></p></td>
<td><p><a href="../Page/Direct3D.md" title="wikilink">Direct3D</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>G6050</p></td>
<td><p>Jan 2014</p></td>
<td><p>0.5</p></td>
<td><p>??@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>G6060</p></td>
<td><p>Jan 2014</p></td>
<td><p>0.5</p></td>
<td><p>??@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>G6100 (XE)</p></td>
<td><p>Jan 2014</p></td>
<td><p>1</p></td>
<td><p>??@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>G6110</p></td>
<td><p>Jan 2014</p></td>
<td><p>1</p></td>
<td><p>??@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### Series 6XT

[2014年](../Page/2014年.md "wikilink")[1月6日](../Page/1月6日.md "wikilink")発表。\[6\]\[7\]

<table>
<thead>
<tr class="header">
<th><p>Model</p></th>
<th><p>Date</p></th>
<th><p>Clusters</p></th>
<th><p>Die Size (mm<sup>2</sup>)</p></th>
<th><p>Config core<sup>[4]</sup></p></th>
<th><p>SIMD lane</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Fillrate" title="wikilink">Fillrate</a></p></th>
<th><p>Bus width<br />
(<a href="https://ja.wikipedia.org/wiki/bit" title="wikilink">bit</a>)</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Heterogeneous_System_Architecture" title="wikilink">HSA</a>-features</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Application_programming_interface" title="wikilink">API</a> (version)</p></th>
<th><p>GFLOPS(@ 650 MHz)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>MPolygons/s</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Pixel" title="wikilink">GP</a>/s)</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Texel_(graphics)" title="wikilink">GT</a>/s)</p></td>
<td><p><a href="../Page/OpenGL_ES.md" title="wikilink">OpenGL ES</a></p></td>
<td><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></td>
<td><p><a href="../Page/OpenCL.md" title="wikilink">OpenCL</a></p></td>
<td><p><a href="../Page/Direct3D.md" title="wikilink">Direct3D</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GX6240</p></td>
<td><p>Jan 2014</p></td>
<td><p>2</p></td>
<td><p>??@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GX6250</p></td>
<td><p>Jan 2014</p></td>
<td><p>2</p></td>
<td><p>??@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GX6450</p></td>
<td><p>Jan 2014</p></td>
<td><p>4</p></td>
<td><p>19.1mm2@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GX6650</p></td>
<td><p>Jan 2014</p></td>
<td><p>6</p></td>
<td><p>??@28 nm</p></td>
<td><p>?/?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>??</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### Series 7XE

[2014年](../Page/2014年.md "wikilink")[11月10日](../Page/11月10日.md "wikilink")発表。\[8\]

<table>
<thead>
<tr class="header">
<th><p>Model</p></th>
<th><p>Date</p></th>
<th><p>Clusters</p></th>
<th><p>Die Size (mm<sup>2</sup>)</p></th>
<th><p>Config core<sup>[4]</sup></p></th>
<th><p>SIMD lane</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Fillrate" title="wikilink">Fillrate</a></p></th>
<th><p>Bus width<br />
(<a href="https://ja.wikipedia.org/wiki/bit" title="wikilink">bit</a>)</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Heterogeneous_System_Architecture" title="wikilink">HSA</a>-features</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Application_programming_interface" title="wikilink">API</a> (version)</p></th>
<th><p>GFLOPS(@ 650 MHz)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>MPolygons/s</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Pixel" title="wikilink">GP</a>/s)</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Texel_(graphics)" title="wikilink">GT</a>/s)</p></td>
<td><p><a href="../Page/OpenGL_ES.md" title="wikilink">OpenGL ES</a></p></td>
<td><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></td>
<td><p><a href="../Page/OpenCL.md" title="wikilink">OpenCL</a></p></td>
<td><p><a href="../Page/Direct3D.md" title="wikilink">Direct3D</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GE7400</p></td>
<td><p>Nov 2014</p></td>
<td><p>0.5</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GE7800</p></td>
<td><p>Nov 2014</p></td>
<td><p>1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### Series 7XT

[2014年](../Page/2014年.md "wikilink")[11月10日](../Page/11月10日.md "wikilink")発表。\[9\]

<table>
<thead>
<tr class="header">
<th><p>Model</p></th>
<th><p>Date</p></th>
<th><p>Clusters</p></th>
<th><p>Die Size (mm<sup>2</sup>)</p></th>
<th><p>Config core<sup>[4]</sup></p></th>
<th><p>SIMD lane</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Fillrate" title="wikilink">Fillrate</a></p></th>
<th><p>Bus width<br />
(<a href="https://ja.wikipedia.org/wiki/bit" title="wikilink">bit</a>)</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Heterogeneous_System_Architecture" title="wikilink">HSA</a>-features</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Application_programming_interface" title="wikilink">API</a> (version)</p></th>
<th><p>GFLOPS(@ 650 MHz)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>MPolygons/s</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Pixel" title="wikilink">GP</a>/s)</p></td>
<td><p>(<a href="https://ja.wikipedia.org/wiki/Texel_(graphics)" title="wikilink">GT</a>/s)</p></td>
<td><p><a href="../Page/OpenGL_ES.md" title="wikilink">OpenGL ES</a></p></td>
<td><p><a href="../Page/OpenGL.md" title="wikilink">OpenGL</a></p></td>
<td><p><a href="../Page/OpenCL.md" title="wikilink">OpenCL</a></p></td>
<td><p><a href="../Page/Direct3D.md" title="wikilink">Direct3D</a></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GT7200</p></td>
<td><p>Nov 2014</p></td>
<td><p>2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GT7400</p></td>
<td><p>Nov 2014</p></td>
<td><p>4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GT7600</p></td>
<td><p>Nov 2014</p></td>
<td><p>6</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>GT7800</p></td>
<td><p>Nov 2014</p></td>
<td><p>8</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>GT7900</p></td>
<td><p>Nov 2014</p></td>
<td><p>16</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 搭載製品

### ビデオカード

  - [日本電気ホームエレクトロニクス](../Page/日本電気ホームエレクトロニクス.md "wikilink") PC 3DEngine(PCX1)およびPC 3DEngine2(PCX2) - PowerVR搭載の3Dビデオカード。
  - [Matrox](../Page/Matrox.md "wikilink") m3D 4MB PCI - PowerVR(PCX2)搭載、3D専用ビデオカード。
  - [メルコ](../Page/バッファロー_\(パソコン周辺機器\).md "wikilink") TGP-VR4 - PowerVR(PCX1)搭載、3D専用ビデオカード。
  - [アイ・オー・データ機器](../Page/アイ・オー・データ機器.md "wikilink") GA-PVR3D4/PCI - PowerVR(PCX1)搭載、3D専用ビデオカード。
  - [PowerColor](https://ja.wikipedia.org/wiki/PowerColor "wikilink") EVIL KYRO 32MB AGP - PowerVR3 KYRO搭載ビデオカード。
  - Hercules 3D PROPHET 4500 - PowerVR3 KYROII(STG4500-X)搭載ビデオカード\[10\]

### 家庭用ゲーム機およびアーケードゲーム機

[代替文=](https://ja.wikipedia.org/wiki/ファイル:Dreamcast-Console-Set.png "wikilink")

  - [ドリームキャスト](../Page/ドリームキャスト.md "wikilink")
  - [NAOMI](../Page/NAOMI.md "wikilink")
  - [NAOMI2](https://ja.wikipedia.org/wiki/NAOMI2 "wikilink")
  - [ATOMISWAVE](../Page/ATOMISWAVE.md "wikilink")
  - [PlayStation Vita](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink")/[PlayStation Vita TV](https://ja.wikipedia.org/wiki/PlayStation_Vita_TV "wikilink")(SGX543MP4+)\[11\]\[12\]
  - [プレイステーション クラシック](https://ja.wikipedia.org/wiki/プレイステーション_クラシック "wikilink")

### 携帯電話

  - [富士通](../Page/富士通.md "wikilink") [FOMA](../Page/FOMA.md "wikilink") [F902i](../Page/F902i.md "wikilink")、[F901i](https://ja.wikipedia.org/wiki/F901i "wikilink")、[F702iD](../Page/F702iD.md "wikilink")、[F902iS](../Page/F902iS.md "wikilink")
  - [三菱電機](../Page/三菱電機.md "wikilink") FOMA [D702i](../Page/D702i.md "wikilink")、[D901i](../Page/D901i.md "wikilink")、[D901iS](../Page/D901iS.md "wikilink")、[D902i](../Page/D902i.md "wikilink")、[D902iS](../Page/D902iS.md "wikilink")、[MUSIC PORTER X](../Page/MUSIC_PORTER_X.md "wikilink")
  - [日本電気](../Page/日本電気.md "wikilink") FOMA [N902i](../Page/N902i.md "wikilink")、[N902iS](../Page/N902iS.md "wikilink")、[N902iX HIGH-SPEED](../Page/N902iX_HIGH-SPEED.md "wikilink")
  - [パナソニック モバイルコミュニケーションズ](../Page/パナソニック_モバイルコミュニケーションズ.md "wikilink") FOMA [P702iS](https://ja.wikipedia.org/wiki/P702iS "wikilink")、[P902i](../Page/P902i.md "wikilink")、[P902iS](../Page/P902iS.md "wikilink")
  - [シャープ](../Page/シャープ.md "wikilink") [SH702iD](../Page/SH702iD.md "wikilink")、[SH702iS](../Page/SH702iS.md "wikilink")、[SH902i](../Page/SH902i.md "wikilink")、[SH902iS](../Page/SH902iS.md "wikilink")、[DOLCE SL](../Page/DOLCE_SL.md "wikilink")
  - [ソニー・エリクソン・モバイルコミュニケーションズ](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ "wikilink") [P990](https://ja.wikipedia.org/wiki/P990 "wikilink")、[M600](https://ja.wikipedia.org/wiki/M600 "wikilink")、[W950](https://ja.wikipedia.org/wiki/W950 "wikilink")、FOMA [SO902iWP+](../Page/SO902iWP+.md "wikilink")、[M600i](https://ja.wikipedia.org/wiki/M600i "wikilink")
  - [京セラ](../Page/京セラ.md "wikilink") [WX04K](https://ja.wikipedia.org/wiki/WX04K "wikilink")、[SoftBank 101K](https://ja.wikipedia.org/wiki/SoftBank_101K "wikilink")
  - [モトローラ](../Page/モトローラ.md "wikilink") [MS550](https://ja.wikipedia.org/wiki/MS550 "wikilink")
  - [SKテレテック](https://ja.wikipedia.org/wiki/SKテレテック "wikilink") [IM-8300](https://ja.wikipedia.org/wiki/IM-8300 "wikilink")
  - [Pepperpad](https://ja.wikipedia.org/wiki/Pepperpad "wikilink")
  - [Helio Hero](https://ja.wikipedia.org/wiki/Helio_Hero "wikilink")
  - [アップル](../Page/アップル_\(企業\).md "wikilink") [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")
  - [ASUS](../Page/ASUS.md "wikilink") [ZenFone2](https://ja.wikipedia.org/wiki/ZenFone2 "wikilink")

### PDA・モバイル端末

  - [デル](../Page/デル.md "wikilink") [Axim](../Page/Axim.md "wikilink") X50v、X51v
  - アップル [iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")、[iPad mini](https://ja.wikipedia.org/wiki/iPad_mini "wikilink")、[iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")、[Apple TV](../Page/Apple_TV.md "wikilink")

### カーナビゲーション

  - [クラリオン](../Page/クラリオン.md "wikilink") MAX960
  - 三菱電機 HDD Navi H9000、H9700
  - [パイオニア](https://ja.wikipedia.org/wiki/パイオニア "wikilink") Cybernavi AVIC-VH009

### その他

  - アイ・オー・データ機器 IF-SEGA2/PCI(PCX2) - セガサターン周辺機器用インターフェイスボード。ISA-PCIブリッジとしてPowerVRが利用されている。\[13\]

## 脚注

### 注釈

### 出典

## 外部リンク

  - [イマジネーションテクノロジーズ](http://www.imgteckk.com/) - [PowerVR ビジュアルIPコア](http://www.imgteckk.com/powervr/products/)

[Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink")

1.  パソコン用グラフィックチップからは撤退 <http://us.st.com/stonline/press/news/year2002/c1146h.htm>
2.  [TI Announces OMAP4470 and Specs: PowerVR SGX544, 1.8 GHz Dual Core Cortex-A9](http://www.anandtech.com/show/4413/ti-announces-omap-4470-and-specs-powervr-sgx544-18-ghz-dual-core-cortexa9), by Brian Klug, 6/2/2011, AnandTech, Inc.
3.  <http://www.engadget.com/2012/06/15/imagination-powervr-g6230-g6430/>
4.  [Imagination Technologies Announces Entry-Level PowerVR Series6XE GPU Family](http://www.anandtech.com/show/7630/imagination-technologies-announces-entrylevel-powervr-series6xe-gpu-family), January 6, 2014, AnandTech
5.  [Imagination drives highly-advanced PowerVR Series6 architecture into all key entry-level mobile and consumer segments](http://www.imgtec.com/news/Release/index.asp?NewsID=822), January 6, 2014, Imagination
6.  [Imagination’s new generation PowerVR Series6XT architecture delivers up to 50% higher performance and advanced power management](http://www.imgtec.com/news/Release/index.asp?NewsID=821)
7.  [Imagination Technologies Announces PowerVR Series6XT Architecture](http://www.anandtech.com/show/7629/imagination-technologies-announces-powervr-series6xt-architecture-available-for-immediate-licensing)
8.  [New PowerVR Series7XE family targets the next billion mobile and embedded GPUs](http://blog.imgtec.com/powervr/new-powervr-series7xe-family-targets-the-next-billion-mobile-and-embedded-gpus)
9.  [PowerVR Series7XT GPUs push graphics and compute performance to the max](http://blog.imgtec.com/powervr/powervr-series7xt-gpus-push-graphics-and-compute-performance)
10. [:<File:3D_Prophet_4500.jpg>](https://ja.wikipedia.org/wiki/:File:3D_Prophet_4500.jpg "wikilink")
11. <http://game.watch.impress.co.jp/docs/news/20110127_423061.html>
12. <http://game.watch.impress.co.jp/docs/series/3dcg/20100316_355022.html>
13. 発売前の製品写真にはメモリが搭載されたものが使われていたものの、実際の製品ではメモリが搭載されておらず、ビデオチップとして使用できない。また、デバイスとしてはPowerVRが検出されるため他のPowerVRボードとの併用は出来ない。