> この記事は[Graphics Processing Unit](https://ja.wikipedia.org/wiki/Graphics_Processing_Unit)から翻訳されています。


**Graphics Processing Unit**（グラフィックス プロセッシング ユニット、略して**GPU**）は、[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")に代表されるリアルタイム[画像処理](../Page/画像処理.md "wikilink")に特化した[演算装置](../Page/演算装置.md "wikilink")あるいは[プロセッサ](../Page/プロセッサ.md "wikilink")である。[グラフィックコントローラ](../Page/グラフィックコントローラ.md "wikilink")などと呼ばれる、コンピュータが画面に表示する映像を描画するための処理を行うICから発展した。特にリアルタイム[3DCGなどに必要な](../Page/3次元コンピュータグラフィックス.md "wikilink")、定形かつ大量の演算を並列にパイプライン処理する[グラフィックスパイプライン](../Page/グラフィックスパイプライン.md "wikilink")性能を重視している。現在の高機能GPUは高速のビデオメモリ（[VRAM](../Page/VRAM.md "wikilink")）と接続され、頂点処理およびピクセル処理などの座標変換やグラフィックス陰影計算（[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")）に特化したプログラム可能な演算器（プログラマブルシェーダーユニット）を多数搭載している。[プロセスルール](https://ja.wikipedia.org/wiki/プロセスルール "wikilink")の微細化が鈍化していることから[ムーアの法則](../Page/ムーアの法則.md "wikilink")は限界に達しつつあるが、設計が複雑で並列化の難しい[CPU](../Page/CPU.md "wikilink")と比較して、個々の演算器の設計が単純で並列計算に特化したGPUは微細化の恩恵を得やすい。さらに[HPC分野では](../Page/高性能計算.md "wikilink")、[CPU](../Page/CPU.md "wikilink")よりも並列演算性能にすぐれたGPUのハードウェアを、より一般的な計算に活用する「[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")」がさかんに行われるようになっており、そういった分野向けに映像出力端子を持たない専用製品や、[深層学習](https://ja.wikipedia.org/wiki/深層学習 "wikilink")ベースの[AI向けに特化した演算器を搭載したハイエンド製品も現れている](../Page/人工知能.md "wikilink")。

[thumb](https://ja.wikipedia.org/wiki/ファイル:6600GT_GPU.jpg "wikilink")

## 歴史

### 1970年代〜1980年代

[コンシューマ](https://ja.wikipedia.org/wiki/コンシューマ "wikilink")PC向けGPUの起源は[1970年代](../Page/1970年代.md "wikilink")から[1980年代](../Page/1980年代.md "wikilink")のグラフィックコントローラにさかのぼる。当時のグラフィックコントローラは、[矩形](https://ja.wikipedia.org/wiki/矩形 "wikilink")や[多角形](../Page/多角形.md "wikilink")の領域を単純に塗り潰したり、BitBlt（[Bit Block Transfer](../Page/Bit_Block_Transfer.md "wikilink")、ビット単位でのブロック転送）などにより、2次元画像に対して簡単な描画処理を行うだけであり、その[機能](https://ja.wikipedia.org/wiki/機能 "wikilink")と[能力](https://ja.wikipedia.org/wiki/能力 "wikilink")は限定的だった。

グラフィックコントローラの中には、いくつかの命令を[ディスプレイリスト](https://ja.wikipedia.org/wiki/ディスプレイリスト "wikilink")としてまとめて実行したり、[DMA転送を用いることでメイン](../Page/Direct_Memory_Access.md "wikilink")[CPU](../Page/CPU.md "wikilink")の[負荷](https://ja.wikipedia.org/wiki/負荷 "wikilink")を減らしたりするものもあった。このような専用のグラフィックコントローラを用いずに、DMAコントローラで処理したり、汎用CPUをグラフィック処理専用に割り当てたグラフィック[サブシステム](https://ja.wikipedia.org/wiki/サブシステム "wikilink")を充てるコンピュータも存在した。汎用的なグラフィックス・[コプロセッサ](../Page/コプロセッサ.md "wikilink")は古くから開発されてきたが、当時の技術的な制約から安価な製品では機能や[性能](https://ja.wikipedia.org/wiki/性能 "wikilink")に乏しく、また高機能なものは[回路](https://ja.wikipedia.org/wiki/回路 "wikilink")の規模が増大し非常に高価なものとならざるを得ず、結果的にパーソナルコンピュータへ広く採用されることはなかった。

1980年代から[1990年代](../Page/1990年代.md "wikilink")前半にかけてはBit Block Transferをサポートするチップと、描画を高速化するチップは別々のチップとして実装されていたが、チップ処理技術が進化するとともに安価になり、VGAカードをはじめとする[グラフィックカード](https://ja.wikipedia.org/wiki/グラフィックカード "wikilink")上に実装され、普及していった。1987年の[VGA発表とともにリリースされたIBMの](../Page/Video_Graphics_Array.md "wikilink")8514グラフィックスシステムは、[2Dの基本的な描画機能をサポートした最初のPC用](../Page/2次元コンピュータグラフィックス.md "wikilink")[グラフィックアクセラレータ](../Page/グラフィックアクセラレータ.md "wikilink")となった。[Amiga](../Page/Amiga.md "wikilink")はビデオハードウエアにBlitterを搭載した最初のコンシューマ向けコンピュータであった。

1980年代後半から1990年代前半の日本国内で広く普及していたPCとして[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")があるが、同シリーズのグラフィックの描画に関連するチップには[GDCと](https://ja.wikipedia.org/wiki/μPD7220 "wikilink")、GRCG・EGCがある（CRTCなどもあるが、描画には関係しない）。GDCには直線・[円弧](https://ja.wikipedia.org/wiki/円弧 "wikilink")・四角塗りつぶしなどの[図形](https://ja.wikipedia.org/wiki/図形 "wikilink")描画機能があり、この記事で扱っているタイプのLSIである。GDCは登場時点では比較的高機能・高性能であったが、CPUの性能向上によりその利点は薄くなっていった（そのため、当時の開発者でもそれを正確に把握していない者も多い）。GRCGは複数プレーンへの同時描画（98ではプレーンごとにセグメントアドレスを動かす必要があり面倒だった）や描画時のマスク操作などをハードウェアで行えるもので、EGCはGRCGの強化版（Enhanced Graphic Charger）である。EGCはEPSONが比較的後期まで追随しなかったことや、NECがハードウェアの仕様の公開に非積極的になった以降ということもあり、あまりよく知られていない。さらに、AGDC（Advanced 〜）やEEGC（あるいはE<sup>2</sup>GC）といったチップに至っては、非公開情報を集めた文献にもその名前以外には殆ど全く情報がない。

### 1990年代

1990年代に入ると、[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink") (SGI) が自社の[グラフィックワークステーション](https://ja.wikipedia.org/wiki/グラフィックワークステーション "wikilink")用のグラフィック[ライブラリ](../Page/ライブラリ.md "wikilink")として[開発](../Page/開発.md "wikilink")・[実装](../Page/実装.md "wikilink")したが[OpenGL](../Page/OpenGL.md "wikilink")に発展して[標準化](../Page/標準化.md "wikilink")され、標準化されたグラフィックライブラリとその[APIに対応したハードウェアアクセラレータ](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、という図式が登場する。

実装当初のIRIS GLは[ソフトウェア](../Page/ソフトウェア.md "wikilink")によるものであったが、SGIでは当初よりこのAPIをハードウェアによって高速処理させる ([ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")を行う) ことを念頭に設計しており、程なくIRIS GLアクセラレータを搭載したワークステーションが登場する。ただし、当初のIRIS GLアクセラレータはまだ単体の半導体[プロセッサ](../Page/プロセッサ.md "wikilink")ではなく、グラフィック[サブシステム](https://ja.wikipedia.org/wiki/サブシステム "wikilink")は巨大な[基板](../Page/基板.md "wikilink")であった。

1990年代の初めごろ、[Microsoft Windowsの普及とともに](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[グラフィックアクセラレータ](../Page/グラフィックアクセラレータ.md "wikilink")へのニーズが高まり、WindowsのグラフィックスAPIである[GDIに対応したグラフィックアクセラレータが開発された](../Page/Graphics_Device_Interface.md "wikilink")。

[1991年](../Page/1991年.md "wikilink")に[S3 Graphicsが開発した](../Page/S3_Graphics.md "wikilink")"S3 86C911"は、最初のワンチップ2Dグラフィック・アクセラレータであった。"86C911"という名は設計者がその速さを標榜するため[ポルシェ911にちなんで名付けた](../Page/ポルシェ・911.md "wikilink")。86C911を皮切りとして数々のグラフィック・アクセラレータが発売された。

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")には[3Dlabs](https://ja.wikipedia.org/wiki/3Dlabs "wikilink")がOpenGLアクセラレータのワンチップ化に成功し、低価格化と高[パフォーマンス](https://ja.wikipedia.org/wiki/パフォーマンス "wikilink")化が加速度的に進行し始める。また同年に登場したインテルの[Pentium Proプロセッサの処理能力は同時代の](../Page/Pentium_Pro.md "wikilink")[RISC](../Page/RISC.md "wikilink")プロセッサの領域に差し掛かっており、この[CPU](../Page/CPU.md "wikilink")とワンチップ化によって価格を下げたOpenGLアクセラレータのセットは、それまで[メーカー](https://ja.wikipedia.org/wiki/メーカー "wikilink")に高収益をもたらしていたグラフィックワークステーションという[カテゴリー](https://ja.wikipedia.org/wiki/カテゴリー "wikilink")に[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")から価格破壊を仕掛ける原動力となった。

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")までには、あらゆる主要なPCグラフィックチップメーカーが2Dアクセラレータを開発し、とうとう汎用グラフィックス・[コプロセッサ](../Page/コプロセッサ.md "wikilink")は市場から消滅した。

1995年に[3dfx](../Page/3dfx.md "wikilink")により[Voodooという](../Page/3dfx.md "wikilink")3Dアクセラレータが発売された。家庭用PCの性能上のボトルネックを考慮してゲーム用に最適化されたGlideというAPIも用意され、家庭用PC上で当時のアーケードゲームに匹敵する品質のグラフィックを実現した。Voodooシリーズは、1990年代後半の家庭用PCゲームの品質向上を牽引したシリーズとなった。

1995年に[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Windows95とともに開発したゲーム作成及び](../Page/Microsoft_Windows_95.md "wikilink")[マルチメディア](../Page/マルチメディア.md "wikilink")再生用のAPI群[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")ではさらにグラフィック・アクセラレータの性能が強化された。DirectXのコンポートネントのひとつ[Direct3D](../Page/Direct3D.md "wikilink")は[3Dグラフィック](https://ja.wikipedia.org/wiki/3Dグラフィック "wikilink")処理の[ハードウェア](../Page/ハードウェア.md "wikilink")化を想定したレンダリング・[パイプラインを持っていた](../Page/パイプライン処理.md "wikilink")。

1997年当時のグラフィック・アクセラレータは[レンダリングのみしかサポートしていなかったが](../Page/レンダリング_\(コンピュータ\).md "wikilink")、この頃から[Zバッファ](../Page/Zバッファ.md "wikilink")、[アルファブレンディング](https://ja.wikipedia.org/wiki/アルファブレンディング "wikilink")、フォグ、[ステンシルバッファ](https://ja.wikipedia.org/wiki/ステンシルバッファ "wikilink")、[テクスチャマッピング](../Page/テクスチャマッピング.md "wikilink")、[テクスチャフィルタリング](../Page/テクスチャフィルタリング.md "wikilink")などの機能を次々搭載し、3Dグラフィック表示機能を競うようになった。[DVD-Video](../Page/DVD-Video.md "wikilink")再生支援機能を備えるチップも現れた。

[VDP](../Page/VDP.md "wikilink")等の汎用グラフィック・プロセッサについては、[カーナビ](https://ja.wikipedia.org/wiki/カーナビ "wikilink")等の表示用に使用され新たな市場を形成している。90年代後半からは、[携帯電話](../Page/携帯電話.md "wikilink")に多色表示がもちいられるようになり、その分野においても有用な市場を形成している。

一方、システムの低価格化を目的に、[チップセット](../Page/チップセット.md "wikilink")の[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")にグラフィックコアの統合を行った、[統合チップセットが](https://ja.wikipedia.org/wiki/チップセット#統合チップセット "wikilink")[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")ころから登場し始める。[1999年](../Page/1999年.md "wikilink")の「[Intel 810](../Page/Intel_810.md "wikilink")」チップセットの登場で、低価格機には統合チップセットの使用が定着し始めた。

ハードウェアによる座標変換・陰影計算処理（; ハードウェアT\&L）は1999年にリリースされたDirectX 7にて標準化され\[1\]、またこのハードウェアT\&Lを世界で初めて実装して製品化した[NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink") 256を定義する言葉として「**GPU**」という名称が提唱されることとなった。ハードウェアT\&Lの実装によって、NVIDIA社製品は他社製品と比較して突出した高性能を発揮するようになった。これ以後、[3dfx Voodooシリーズも目立って高性能とは言えなくなった](../Page/3dfx.md "wikilink")。

### 2000年代

[thumb](https://ja.wikipedia.org/wiki/ファイル:三次元グラフィックス_描画パイプライン.PNG "wikilink") DirectX 8世代では、[グラフィックスパイプライン](../Page/グラフィックスパイプライン.md "wikilink")中の一部の処理をユーザープログラマーが自由に記述できる[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")が導入されるようになった。プログラマブルシェーダーは[頂点シェーダー](https://ja.wikipedia.org/wiki/頂点シェーダー "wikilink") (Vertex Shader) と[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink") (Pixel Shader) の2種類が用意され、頂点シェーダーは頂点座標や光源ベクトルの頂点単位での座標変換および頂点単位での陰影計算（シェーディング）を、ピクセルシェーダーはピクセル単位での陰影計算をそれぞれ担当する設計だった。特に従来の固定機能シェーダーでは[ポリゴン](../Page/ポリゴン.md "wikilink")単位（頂点単位）でしか陰影計算を実行できなかったのに対し、[ピクセル](../Page/ピクセル.md "wikilink")単位での陰影計算もできるプログラマブル[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")の導入により、表現の自由度と解像度（精細度・品質）が飛躍的に向上した。ただし、シェーダープログラムの記述に使える言語は原始的なアセンブリ言語が基本であり、記述可能なプログラム長（命令数）もごく限られていたため、開発効率や再利用性などの面で課題を抱えていた。なお、頂点シェーダープログラムとピクセルシェーダープログラムを実行するハードウェアユニット（演算器）のことを、それぞれ頂点シェーダーおよびピクセルシェーダーとも呼んでいた。

また、この世代になるとマルチ[テクスチャ](https://ja.wikipedia.org/wiki/テクスチャ "wikilink")、[キューブマップ](https://ja.wikipedia.org/wiki/キューブマップ "wikilink")、アニソトロピック（[異方性](https://ja.wikipedia.org/wiki/異方性 "wikilink")）フィルタ、ボリュームテクスチャなどが新たにサポートされ、[HDRI](https://ja.wikipedia.org/wiki/HDRI "wikilink")によるレンダリングや動的な[環境マッピング](https://ja.wikipedia.org/wiki/環境マッピング "wikilink")の生成が可能になった。[動画](../Page/動画.md "wikilink")の再生や[圧縮にシェーダーを使う技術も搭載された](../Page/データ圧縮.md "wikilink") ([Intel Clear Video](https://ja.wikipedia.org/wiki/Intel_Clear_Video "wikilink")、[PureVideo](https://ja.wikipedia.org/wiki/PureVideo "wikilink")、[AVIVO](https://ja.wikipedia.org/wiki/AVIVO "wikilink")、[Chromotion](https://ja.wikipedia.org/wiki/Chromotion "wikilink"))。

DirectX 9世代になると、このプログラマブルシェーダーがさらに進化し、シェーダーのプログラムを書くための専用の[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")である[Cg](../Page/Cg_\(プログラミング言語\).md "wikilink")、[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")、[GLSL](../Page/GLSL.md "wikilink")などが開発され、シェーダーを[物理演算](https://ja.wikipedia.org/wiki/物理演算 "wikilink")などゲームでの3Dグラフィック表示以外の演算に使うことも多くなった。[Windows Vistaに搭載された機能のひとつ](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")「[Windows Aero](../Page/Windows_Aero.md "wikilink")」 ([Desktop Window Manager](https://ja.wikipedia.org/wiki/Desktop_Window_Manager "wikilink")) は画面表示にプログラマブルシェーダー（ピクセルシェーダー2.0）を利用するので\[2\]、この世代のビデオチップが必須になっている（Windows Aero Glassを使用しなければDirectX 8世代以前のビデオチップでもWindows Vista自体は稼働する）。また、[Mac OS Xの](https://ja.wikipedia.org/wiki/macOS "wikilink")[Core Imageでは](../Page/Core_Image.md "wikilink")[OpenGL](../Page/OpenGL.md "wikilink")のプログラマブルシェーダーを利用して2Dグラフィックのフィルタ処理を行っている。

[thumb](https://ja.wikipedia.org/wiki/ファイル:GeForce_8800の内部構造.PNG "wikilink")

DirectX 10世代ではさらに自由度が増し、「[シェーダーモデル](https://ja.wikipedia.org/wiki/シェーダーモデル "wikilink")4.0」 (SM 4.0) に基づく[グラフィックスパイプライン](../Page/グラフィックスパイプライン.md "wikilink")が導入され、頂点シェーダーとピクセルシェーダーの間で[ジオメトリシェーダー](https://ja.wikipedia.org/wiki/ジオメトリシェーダー "wikilink") (Geometry Shader) によるプリミティブ増減処理を行なえるようになった。ジオメトリシェーダーはOpenGL 3.2でも標準化されている。

グラフィックス描画処理では3次元空間を構成する表現のために[三角形](../Page/三角形.md "wikilink")を色付けする[ピクセル](../Page/ピクセル.md "wikilink")シェーディング処理の[負荷](https://ja.wikipedia.org/wiki/負荷 "wikilink")が、精細度や特殊処理などによって大きく変化するため、固定のハードウェアパイプライン構成では[ボトルネック](../Page/ボトルネック.md "wikilink")になることが多かった。この制約を解消するために、DirectX 10世代では演算ユニットを汎用化する**統合型シェーダーアーキテクチャ** ([:en:unified shader architecture](https://ja.wikipedia.org/wiki/:en:unified_shader_architecture "wikilink")) によって固定のパイプラインの一部をより柔軟な構成に変更した。頂点シェーダーとジオメトリシェーダー、そしてピクセルシェーダーの機能をあわせもつ**統合型シェーダー** (Unified Shader) \[3\]を多数搭載して動的に処理を振り分けることによってプログラムの自由度と共にボトルネックを解消し、演算回路数の増加に比例した画像描画処理速度の向上を得た\[4\]日経エレクトロニクス 2007/10/8 「プロセサはマルチ×マルチへ」</ref>。なお、この統合型シェーダーアーキテクチャによるハードウェアレベルでの汎用化が、GPUにおける汎用演算（[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")）の発展と普及を加速させていくことになる。

統合型シェーダーアーキテクチャを採用した[NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink") 8シリーズではWindows / Mac OS X / [Linux](../Page/Linux.md "wikilink")用の標準的な汎用[Cコンパイラ環境](../Page/C言語.md "wikilink") ([CUDA](../Page/CUDA.md "wikilink")) が提供され、一方[ATI Radeon](https://ja.wikipedia.org/wiki/ATI_Radeon "wikilink") HD 2000シリーズではハードウェアに直接アクセスできる環境 () が、そしてRadeon HD 4000シリーズ以降では[ATI Stream](https://ja.wikipedia.org/wiki/ATI_Stream "wikilink")（Brook+言語と抽象化レイヤーであるCAL）によるアクセス手段が用意されている\[5\]。これにより[科学技術計算](https://ja.wikipedia.org/wiki/科学技術計算 "wikilink")や[シミュレーション](../Page/シミュレーション.md "wikilink")、[画像認識](https://ja.wikipedia.org/wiki/画像認識 "wikilink")、[音声認識](../Page/音声認識.md "wikilink")など、GPUの演算能力を汎用的な用途へ広く利用できるようになった（[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")）。また、特定のハードウェアベンダーやプラットフォームに依存しない[OpenCL](../Page/OpenCL.md "wikilink")というヘテロジニアス計算環境向け標準規格に続き、米[マイクロソフト](../Page/マイクロソフト.md "wikilink")社からDirectX 11 APIの一部として[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")用APIである[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")（コンピュートシェーダー）がリリースされた（のちにDirectComputeをバックエンドとする[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")向け[C++言語](https://ja.wikipedia.org/wiki/C++言語 "wikilink")拡張・ライブラリとして[C++ AMPも登場した](https://ja.wikipedia.org/wiki/C++_AMP "wikilink")\[6\]）。DirectX 11のシェーダーモデル5.0では、前述のコンピュートシェーダーに加え、頂点シェーダーとジオメトリシェーダーの間に、ポリゴンの細分割・詳細化（[サブディビジョンサーフェイス](https://ja.wikipedia.org/wiki/サブディビジョンサーフェス "wikilink")）をGPUで行なう[テッセレーション](https://ja.wikipedia.org/wiki/テッセレーション "wikilink")シェーダー（ハルシェーダー、固定機能テッセレータ、ドメインシェーダー）が追加された\[7\]。テッセレーションシェーダーはOpenGL 4.0、コンピュートシェーダーはOpenGL 4.3でも標準化されている。

なお、主に[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")に最適化されたGeForceやRadeonなど3Dゲーム向け製品と異なり、業務用[ワークステーション](../Page/ワークステーション.md "wikilink")など高い信頼性や耐久性が必要とされる業務用途に特化して設計された[NVIDIA Quadroシリーズ](../Page/NVIDIA_Quadro.md "wikilink")、および[AMD FireProシリーズが存在する](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")。これら業務用製品は[Direct3D](../Page/Direct3D.md "wikilink")よりも[OpenGL](../Page/OpenGL.md "wikilink")およびOpenGL対応アプリケーションに最適化されており、[CAD](../Page/CAD.md "wikilink")、[HPC](../Page/高性能計算.md "wikilink")、[金融](../Page/金融機関.md "wikilink")、[CG映像](../Page/コンピュータグラフィックス.md "wikilink")、建築/設計、[DTP](../Page/DTP.md "wikilink")、[研究開発](../Page/研究開発.md "wikilink")分野において採用されている。そのほか、[NVIDIA Teslaシリーズや](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink")[AMD FireStreamシリーズ](https://ja.wikipedia.org/wiki/AMD_FireStream "wikilink")（のちに[AMD FireProに統合](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")）といった、[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")専用製品も登場している。

### 2010年代

主な[CPU](../Page/CPU.md "wikilink")メーカーは、従来のCPU機能だけにとどまらず、1つのCPUチップ内に複数のCPUコア（[マルチコア](../Page/マルチコア.md "wikilink")）を搭載すると同時に、画像出力専用回路としてGPUコアも統合した製品を提供するようになった。例えば、米[AMDでは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")「[AMD Fusion](https://ja.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit "wikilink")」構想において1つのダイ上に2つ以上のCPUとGPUを統合し\[8\]\[9\]、米[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社でも[Core i5](https://ja.wikipedia.org/wiki/Intel_Core_i5 "wikilink")、[Core i7](https://ja.wikipedia.org/wiki/Intel_Core_i7 "wikilink")、[Core i3での](https://ja.wikipedia.org/wiki/Intel_Core_i3 "wikilink")[Sandy Bridge世代から](https://ja.wikipedia.org/wiki/Sandy_Bridge "wikilink")、同様の製品を提供している\[10\]\[11\]\[12\]。なお、従来型の[UMA](../Page/ユニファイドメモリアーキテクチャ.md "wikilink")、つまり単にCPUとGPUのチップを統合して物理メモリを共有するだけでは、CPUとGPUのメモリ空間が統一されることにはつながらない。におけるhUMAなどのように、CPUとGPUのメモリ空間を統一するために[メモリ一貫性](https://ja.wikipedia.org/wiki/メモリ一貫性 "wikilink")を確保する仕組みが用意されることで初めて、CPU-GPU間のメモリ転送作業が不要となる。また、CPUとGPUの外部メモリが共用されるため、CPUチップの外部メモリ[バスにはCPUのアクセス帯域に加えてGPUのアクセス帯域も加わる](../Page/バス_\(コンピュータ\).md "wikilink")。このため、仮にCPUチップに極めて高い性能のGPUを統合しても、統合チップのメモリアクセス帯域も相応に増強されないと、それが[ボトルネック](../Page/ボトルネック.md "wikilink")となって性能向上は望めない。

GPU用のメモリ規格として長らく[DDR](https://ja.wikipedia.org/wiki/DDR "wikilink")系および[GDDR](https://ja.wikipedia.org/wiki/GDDR "wikilink")系が採用されてきたが、2015年6月に発売された[AMD Radeon](../Page/AMD_Radeon.md "wikilink") R9 Fury Xでは、新しい規格系統の[High Bandwidth Memory](https://ja.wikipedia.org/wiki/High_Bandwidth_Memory "wikilink") (HBM) \[13\]が世界で初めて採用された\[14\] \[15\] \[16\]。しかし、高性能だが高価格なHBMの採用はコンシューマー用途では進まず、[GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")の後継規格である[GDDR5X](https://ja.wikipedia.org/wiki/GDDR5X "wikilink")や[GDDR6](https://ja.wikipedia.org/wiki/GDDR6 "wikilink")が採用されるようになっている。

2010年代後半に[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")という手法が広く普及したことで、[HPC分野でもGPUを多用するようになった](../Page/高性能計算.md "wikilink")。特に深層学習（[ディープラーニング](https://ja.wikipedia.org/wiki/ディープラーニング "wikilink")）ベースのAI用途にGPUの需要が高まっている。VRAMに関しては費用対効果の面から、HPC用途ではたとえ高コストでも広帯域・大容量のHBM、ゲームなどのコンシューマー用途ではたとえ低帯域でも低コストのGDDRという棲み分けが起きている\[17\]。

一方グラフィックスAPIに関しては、[Mantleを皮切りとして](https://ja.wikipedia.org/wiki/Mantle_\(API\) "wikilink")、[Metal](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")、DirectX 12および[Vulkanのように](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")、ハードウェアにより近い制御を可能とするローレベル (low-level) APIが出現することとなった。ローレベルAPIはいずれも[ハードウェア抽象化レイヤーを薄くすることによるオーバーヘッドの低減や描画効率の向上を目的としており](../Page/Hardware_Abstraction_Layer.md "wikilink")、またマルチコアCPUの活用を前提とした描画あるいは演算コマンドリストの非同期実行といった機能を備えている。また、GPUでリアルタイム[レイトレーシング](../Page/レイトレーシング.md "wikilink")を実現する動きも加速しつつある。2009年に\[18\]\[19\]\[20\]が、2011年にの\[21\]が、そして2018年に[マイクロソフト](../Page/マイクロソフト.md "wikilink")の (DXR) と[アップルの](../Page/アップル_\(企業\).md "wikilink")[Metal Ray Tracingが発表された](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")。NVIDIA GeForce RTXシリーズはDXRのハードウェアアクセラレーションに対応する最初のGPUである。

## GPUの構造

DirectX 10世代以降のGPUは統合型シェーダーアーキテクチャに基づいて設計されており、[Intel GMAなどの一部を除きGPGPUにも対応している](https://ja.wikipedia.org/wiki/Intel_GMA "wikilink")。

### NVIDIA Fermiアーキテクチャの例

NVIDIAのGPUは、統合型シェーダーアーキテクチャを採用したGeForce 8 (G80) シリーズ以降、Warp単位（32ハードウェアスレッド）での並列処理実行が特徴となっている\[22\] \[23\]。NVIDIAのGT200アーキテクチャでは、単精度CUDAコア (SPCC) と倍精度ユニット (DPU) が分かれていた\[24\]が、Fermiでは単精度CUDAコア16個を2グループ組み合わせ、倍精度演算器16個と見立てて実行している\[25\]。

  - ホストインターフェース\[26\]

  - GigaThreadスケジューラ\[27\]

  - グラフィックスプロセッシングクラスタ (GPC)\[28\]

      - ラスタライザ\[29\]
      - ストリーミングマルチプロセッサ (SM)
          - 命令キャッシュ (I-Cache)\[30\]
          - Warpスケジューラ\[31\]
          - 命令ディスパッチユニット\[32\]
          - レジスタファイル\[33\]
          - Uniformキャッシュ\[34\]
          - ジオメトリコントローラ\[35\]
          - ストリーミングマルチプロセッサコントローラ (SMC)\[36\]
          - CUDAコア\[37\]
              - ディスパッチポート\[38\]
              - 命令コントローラ\[39\]
              - 浮動小数点ユニット (FP Unit)\[40\]
              - 整数ユニット (INT Unit)\[41\]
              - 結果キュー\[42\]
          - LOAD/STOREユニット (LD/ST)\[43\]
          - 特殊関数ユニット (SFU)\[44\] - [超越関数](../Page/超越関数.md "wikilink")の実行を行なう
          - 共有メモリ / L1キャッシュ \[45\]
          - テクスチャユニット\[46\]
              - テクスチャL1キャッシュ\[47\]
      - テッセレータ (PolyMorph Engine)\[48\] \[49\]

  - [相互接続ネットワーク](https://ja.wikipedia.org/wiki/相互接続ネットワーク "wikilink")

  - (ROP)\[50\]

  - L2キャッシュ\[51\]

  - メモリコントローラ\[52\]

### AMD GCNアーキテクチャの例

AMDのGPUは、[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink") HD 2000～HD 6000シリーズにおいて[VLIW](../Page/VLIW.md "wikilink")を採用していたが、HD 7000シリーズ以降では、グラフィックスだけでなくGPGPUでも性能を発揮できるようにするために、非[VLIW](../Page/VLIW.md "wikilink")な[SIMD](../Page/SIMD.md "wikilink")とスカラー演算ユニットにより構成された[Graphics Core Next](https://ja.wikipedia.org/wiki/Graphics_Core_Next "wikilink") (GCN) アーキテクチャを採用している\[53\]。AMD GPUではWavefront単位（64ハードウェアスレッド）での並列処理実行が特徴となっている。

  - リクエスト調停\[54\]
  - スカラーL1キャッシュ\[55\]
  - 命令L1キャッシュ\[56\]
  - コンピュートエンジン
      - 非同期コンピュートエンジン (ACE)\[57\]
      - コンピュートシェーダー (CS) パイプ\[58\]
  - スケーラブルグラフィックスエンジン\[59\]
      - グラフィックス (GFX) コマンドプロセッサー (GCP)\[60\]
      - ワークディストリビュータ\[61\]
      - コンピュートシェーダー (CS) パイプ\[62\]
      - プリミティブパイプ\[63\]
          - ハイオーダーサーフィス (HOS)\[64\]
          - テッセレート\[65\]
          - ジオメトリ\[66\]
      - ピクセルパイプ\[67\]
          - スキャンコンバーション\[68\]
          - レンダーバックエンド (RB)\[69\]
  - コンピュートユニット (CU)\[70\] / 統合シェーダーコア\[71\]
      - 命令フェッチ (IF) 調停\[72\]
      - SIMDプログラムカウンタ (PC) &命令バッファ (IB)\[73\]
      - 命令調停 (Instruction Arbitration)\[74\]
      - 分岐&メッセージユニット\[75\]
      - 送出/グローバルデータ共有 (GDS) デコード\[76\]
      - ベクターメモリデコード\[77\]
      - スカラーデコード\[78\]
      - スカラー[演算装置](../Page/演算装置.md "wikilink") (Scalar ALU)\[79\]
          - レジスタ\[80\]
          - 演算装置 (ALU)\[81\]
      - ベクターデコード\[82\]
      - 混合精度SIMDユニット (MP SIMD Unit)\[83\]
          - レジスタ\[84\]
          - 混合精度ベクター演算装置 (MP Vector ALU)\[85\]
      - ローカルデータ共有 (LDS) デコード\[86\]
      - ローカルデータ共有メモリ\[87\]
      - データL1キャッシュ\[88\]
          - アドレスユニット\[89\]
          - L1ベクターデータキャッシュ\[90\]
          - データ返却ユニット\[91\]
  - クロスバー (XBAR)\[92\]
  - L2キャッシュ\[93\]
  - メモリコントローラ\[94\]

## 組み込みシステム

### ゲーム機

ゲーム業界においても、1990年代後半から3D描画能力の向上が求められ、[ゲーム機](../Page/ゲーム機.md "wikilink")（ゲームコンソール）ベンダーはGPUメーカーと共同で専用のGPUを開発するようになった。汎用機であるパーソナル・コンピュータ（PC）用GPUより先行した新機能や[eDRAM](https://ja.wikipedia.org/wiki/eDRAM "wikilink")の搭載で差別化したものが多い。また、汎用化・共通化のための分厚い[抽象化](https://ja.wikipedia.org/wiki/抽象化 "wikilink")層がほとんど不要な専用[APIや専用](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[マシン語](https://ja.wikipedia.org/wiki/マシン語 "wikilink")が使えることもあいまって、同世代における下位や中位のPC用GPUよりも画像処理性能においては高性能である。

本節ではハードウェアT\&Lあるいはそれに類する3次元コンピュータグラフィックスパイプラインを有するもののみを列挙する。

  - [PlayStationに搭載されたGeometric](../Page/PlayStation_\(ゲーム機\).md "wikilink") Transfer Engine (GTE)

<!-- end list -->

  -
    [SCE製](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink")。ハードウェア[ジオメトリエンジン](https://ja.wikipedia.org/wiki/ジオメトリエンジン "wikilink")をPC用GPUより4年ほど先行して搭載している。CPU内のコプロセッサとして動作する。
    なおGTEとは別に、GPUと呼ばれるフレームバッファを扱う2Dグラフィックス処理用のチップも搭載している\[95\]。

<!-- end list -->

  - [PlayStation 2に搭載された](../Page/PlayStation_2.md "wikilink")[Graphics Synthesizer](https://ja.wikipedia.org/wiki/Emotion_Engine#Graphics_Synthesizer "wikilink") (GS)

<!-- end list -->

  -
    SCE製。GPUに[eDRAM](https://ja.wikipedia.org/wiki/eDRAM "wikilink")をVRAMとしてオンダイで混載し、2560bitという広[帯域](https://ja.wikipedia.org/wiki/帯域 "wikilink")な内部[バスを実現した](../Page/バス_\(コンピュータ\).md "wikilink")。[eDRAM](https://ja.wikipedia.org/wiki/eDRAM "wikilink")はゲーム機用GPUに多用されるようになった。

<!-- end list -->

  - [PlayStation 3に搭載された](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")[RSX Reality Synthesizer](https://ja.wikipedia.org/wiki/RSX_Reality_Synthesizer "wikilink") (RSX)

<!-- end list -->

  -
    [NVIDIA](../Page/NVIDIA.md "wikilink")とSCEが共同開発した。G70ベースであると説明されている\[96\]。

<!-- end list -->

  - [PlayStation Vitaに搭載された](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink")[PowerVR](../Page/PowerVR.md "wikilink") SGX543MP4+

<!-- end list -->

  -
    Imagination TechnologiesとSCEが共同開発した\[97\]。

<!-- end list -->

  - [NINTENDO64](../Page/NINTENDO64.md "wikilink")に搭載されたRCP

<!-- end list -->

  -
    [SGI](../Page/シリコングラフィックス.md "wikilink")（現[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")）製。[座標](../Page/座標.md "wikilink")計算や[音声処理](https://ja.wikipedia.org/wiki/音声処理 "wikilink")を全て内蔵[DSPによる](../Page/デジタルシグナルプロセッサ.md "wikilink")[SIMD](../Page/SIMD.md "wikilink")演算で行う構造で、これは現代で言えば[頂点シェーダー](https://ja.wikipedia.org/wiki/頂点シェーダー "wikilink")による[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")を行うことに相当する先鋭的なもの。

<!-- end list -->

  - [ニンテンドーゲームキューブ](../Page/ニンテンドーゲームキューブ.md "wikilink")に搭載されたFLIPPER

<!-- end list -->

  -
    [ATI](../Page/ATI_Technologies.md "wikilink")（現AMD）製。旧[ArtX](https://ja.wikipedia.org/wiki/ArtX "wikilink")が担当、[NEC製造](../Page/日本電気.md "wikilink")。

<!-- end list -->

  - [Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")に搭載されたHollywood

<!-- end list -->

  -
    AMD製。NEC製造。

<!-- end list -->

  - [Wii Uに搭載されたRadeon](https://ja.wikipedia.org/wiki/Wii_U "wikilink") HD

<!-- end list -->

  -
    AMD製。Radeon HD 4000世代\[98\]。

<!-- end list -->

  - [ニンテンドー3DS](https://ja.wikipedia.org/wiki/ニンテンドー3DS "wikilink")に搭載された[PICA200](https://ja.wikipedia.org/wiki/PICA200 "wikilink")

<!-- end list -->

  -
    ディジタルメディアプロフェッショナルが開発した\[99\]。

<!-- end list -->

  - [ドリームキャスト](../Page/ドリームキャスト.md "wikilink")、[NAOMI](../Page/NAOMI.md "wikilink")に搭載された[PowerVR](../Page/PowerVR.md "wikilink")2

<!-- end list -->

  -
    VideoLogic製。NEC製造。。

<!-- end list -->

  - [Xboxに搭載されたXGPU](../Page/Xbox_\(ゲーム機\).md "wikilink")

<!-- end list -->

  -
    NVIDIA製。GeForce3と4の中間世代のアーキテクチャ\[100\]。Xboxは世界で最初にプログラマブルシェーダー対応のGPUを搭載したゲーム機となった。

<!-- end list -->

  - [Xbox 360に搭載されたXenos](../Page/Xbox_360.md "wikilink")

<!-- end list -->

  -
    AMD製。統合型シェーダーアーキテクチャをPC用GPUより先行して搭載している\[101\]。[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 9世代とDirectX 10世代の中間に相当する。

<!-- end list -->

  - [Nintendo Switchに搭載された](https://ja.wikipedia.org/wiki/Nintendo_Switch "wikilink")[NVIDIA Tegraのカスタマイズ品](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink")

<!-- end list -->

  -
    NVIDIA製。カスタム品であることは公式発表されている\[102\]が、ベースとなったGPUがどの世代なのかは非公表である。
    Vulkan 1.1、OpenGL 4.5以降、OpenGL ES 3.2に対応\[103\]。

なお[Xbox One](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")、[PlayStation 4においては](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")、それぞれAMD製の[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")互換[APUのカスタマイズ版が搭載されており](https://ja.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit "wikilink")、[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")の活用とPCゲームからの移植性を重視したアーキテクチャとなっている\[104\]。

### その他

、[携帯電話](../Page/携帯電話.md "wikilink")や[カーナビゲーションシステム](https://ja.wikipedia.org/wiki/カーナビゲーションシステム "wikilink")の表示機能の高度化が著しく、[組み込みシステム](../Page/組み込みシステム.md "wikilink")において用いられていた[VDP](../Page/VDP.md "wikilink")に代わって、[OpenGL ES対応の](../Page/OpenGL_ES.md "wikilink")[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")を搭載したGPUが採用されることが増えてきている。特に使用メモリと[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")を抑える要求から、。

## 「GPU」という名前

「GPU」は、1999年に[NVIDIA Corporationが](../Page/NVIDIA.md "wikilink")、[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink") 256の発表時に提唱した呼称である\[105\] \[106\]。それまでビデオカード上の処理装置は「ビデオチップ」と呼ばれていたが、GeForce 256はハードウェアT\&Lを世界で初めて搭載し、3次元コンピュータグラフィックスの内部計算および描画処理におけるCPU側の負荷を大幅に軽減するコプロセッサとしての地位を確立したことから、NVIDIA社は「Graphics Processing Unit」と命名した。

GPUと同様の名称として、**Visual Processing Unit** (VPU) が存在する。「VPU」は、[3Dlabs](https://ja.wikipedia.org/wiki/3Dlabs "wikilink") Inc.が、[Wildcat](https://ja.wikipedia.org/wiki/Wildcat "wikilink") VP（）の発表時に命名した\[107\]。なお、VPUの呼称に関しては、[ATI Technologiesが](../Page/ATI_Technologies.md "wikilink")[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink") 9500/9700の発表時に提唱したと誤解されることがある\[108\]が、実際は、3DlabsのWildcat VPの発表が先行している。また、ATIがVPUの呼称を使ったのは、当時は3Dlabsと提携していたからでもある。

現在はAMD (旧ATI) も主にGPUの呼称を使用している。

## 統合GPU

一般に、[チップセット](../Page/チップセット.md "wikilink")および[CPU](../Page/CPU.md "wikilink")内蔵GPU（統合GPU、iGPU）のグラフィック機能は単体チップ型のGPU（ディスクリートGPU、dGPU）に劣るが、消費電力やコスト面では有利である。このため、[オフィススイート](../Page/オフィススイート.md "wikilink")やネットアクセスなどを中心とした高性能が必要ない用途が想定され、低価格が求められる業務用端末（クライアント）機向けや、低発熱・低消費電力が求められる[ノートパソコン](../Page/ノートパソコン.md "wikilink")などでは単体チップのGPUではなく、統合GPUが多く搭載されている。比較的高性能なGPUを使用するゲーム機でもコストダウンを目的としてGPUの統合化が進んでいる。

高性能なGPUの利用を前提とする[Aeroを搭載した](../Page/Windows_Aero.md "wikilink")[Windows Vistaの登場以降](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、チップセット内、およびCPUパッケージ内に統合されているGPUコアの性能が向上してきたため、GPU単体の製品は[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")の物から[3D](../Page/3D.md "wikilink")ゲームの快適なプレイや[CAD](../Page/CAD.md "wikilink")オペレーション・[3DCG](https://ja.wikipedia.org/wiki/3DCG "wikilink")制作におけるプレビュー用途を想定した、比較的高価で高性能なものへとシフトしている。

## GPU 開発企業

  - [AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")

  -
  - [Matrox](../Page/Matrox.md "wikilink")

  - [NVIDIA](../Page/NVIDIA.md "wikilink")

  - [S3 Graphics](../Page/S3_Graphics.md "wikilink")

### チップセットまたはCPU統合GPUのみ手がけている企業

  - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") (かつては単体製品も提供していた)
  - [SiS](https://ja.wikipedia.org/wiki/SiS "wikilink") (かつては単体製品も提供していた)

### 他社へのライセンス供与のみを行なう企業

  - （旧。1994年に社名変更\[109\]。組み込み市場に特化し、他社への設計のライセンス供与を行なっている）

  - [ARM](https://ja.wikipedia.org/wiki/ARMホールディングス "wikilink")

  - [DMP](https://ja.wikipedia.org/wiki/ディジタルメディアプロフェッショナル "wikilink")

### 過去にGPUまたはビデオチップを手がけていた企業

  - [3dfx](../Page/3dfx.md "wikilink") (2000年末に[NVIDIA](../Page/NVIDIA.md "wikilink")に買収された)
  - [3Dlabs](https://ja.wikipedia.org/wiki/3Dlabs "wikilink")（現在は低消費電力のメディアプロセッサを手がける）
  - [ATI Technologies](../Page/ATI_Technologies.md "wikilink") (2006年に[AMDに買収された](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")。ATIブランドは買収後しばらく存続していたがAMDブランドに統一された\[110\])
  - [Chips\&Technologies](https://ja.wikipedia.org/wiki/Chips&Technologies "wikilink")
  - [Cirrus Logic](../Page/シーラス・ロジック.md "wikilink")（グラフィック部門を売却）
  - [Intergraph](https://ja.wikipedia.org/wiki/Intergraph "wikilink")（グラフィックハードウェア生産部門であるINTENSE 3Dを3DLabsに売却後、[ヘキサゴンに買収される](https://ja.wikipedia.org/wiki/ヘキサゴン_\(スウェーデンの企業\) "wikilink")）
  - [NeoMagic](../Page/NeoMagic.md "wikilink")（小型デバイス用メディアプロセッサ事業などを行っており、PC向けからは撤退）
  - [Number Nine Visual Technology](https://ja.wikipedia.org/wiki/ナンバー・ナイン・ビジュアル・テクノロジー "wikilink")
  - [Trident Microsystems](https://ja.wikipedia.org/wiki/Trident_Microsystems "wikilink")
  - [Tseng Labs](https://ja.wikipedia.org/wiki/Tseng_Labs "wikilink")（グラフィック部門をATIに売却）
  - [Weitek](../Page/Weitek.md "wikilink")（ロックウェルに買収される）
  - [XGI Technology Inc.](../Page/XGI_Technology_Inc..md "wikilink")

## 出典

<references/>

## 関連項目

  - [CPU](../Page/CPU.md "wikilink")
  - [VRAM](../Page/VRAM.md "wikilink")
      - [GDDR3](../Page/GDDR3.md "wikilink")
      - [GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")
  - リアルタイム[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")[API](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")
      - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") ([Direct3D](../Page/Direct3D.md "wikilink"))
      - [OpenGL](../Page/OpenGL.md "wikilink"), [OpenGL ES](../Page/OpenGL_ES.md "wikilink")
      - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")
      - [Metal (API)](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")
  - [GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")
  - [ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")
  - [ビデオカード](../Page/ビデオカード.md "wikilink")
  - [グラフィックアクセラレータ](../Page/グラフィックアクセラレータ.md "wikilink")
  - [グラフィックコントローラ](../Page/グラフィックコントローラ.md "wikilink")
  - [オンボードグラフィック](../Page/オンボードグラフィック.md "wikilink")
  - [Integrated Graphics Processor](../Page/Integrated_Graphics_Processor.md "wikilink")

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink")

1.  [Microsoft releases DirectX 7.0 | Windows Server content from Windows IT Pro](http://windowsitpro.com/windows-server/microsoft-releases-directx-70)
2.
3.  [【レビュー】初の統合型シェーダーアーキテクチャ「GeForce 8800シリーズ」を試す (1) 新アーキテクチャで登場したG80 | マイナビニュース](http://news.mynavi.jp/articles/2006/11/09/g80/)
4.
5.  [AMDのGPGPU戦略は新章へ - ATI Streamの展望、DirectX Compute Shaderの衝撃 (1) Radeon HD 4000シリーズでネイティブGPGPU | マイナビニュース](http://news.mynavi.jp/articles/2008/11/27/stream/)
6.  [MicrosoftがGPGPU開発向けC++の拡張「C++ AMP」を発表](http://pc.watch.impress.co.jp/docs/news/event/20110617_453939.html) － 多和田新也（AFDSレポート）、PC Watch、Impress（2011年6月17日付配信、2012年3月24日閲覧）
7.  [テッセレーションの概要](http://msdn.microsoft.com/ja-jp/library/ee417841.aspx)
8.  [現実路線へ修正されたAMDのFUSION](http://pc.watch.impress.co.jp/docs/2007/1225/kaigai409.htm) - 後藤弘茂のWeekly海外ニュース、PC Watch、Impress（2007年12月25日付配信、2012年3月24日閲覧）
9.
10. [Intelの次期CPU「Ivy Bridge(アイビーブリッジ)」を裸にする](http://pc.watch.impress.co.jp/docs/column/kaigai/20120302_516173.html) - 後藤弘茂のWeekly海外ニュース、PC Watch、Impress（2012年3月2日付配信、2012年3月24日閲覧）
11. [Intel NehalemとAMD FUSION 両社のCPU+GPU統合の違い](http://pc.watch.impress.co.jp/docs/2007/1011/kaigai392.htm) - 後藤弘茂のWeekly海外ニュース、PC Watch、Impress（2007年10月11日付配信、2012年3月24日閲覧）
12. [CPUとGPUの境界がなくなる時代が始まる2009年のプロセッサ](http://pc.watch.impress.co.jp/docs/2008/1202/kaigai478.htm) - 後藤弘茂のWeekly海外ニュース、PC Watch、Impress（2008年12月2日付配信、2012年3月24日閲覧）
13. [5981_High_Bandwidth_Memory_HBM_FNL - High-Bandwidth-Memory-HBM.pdf](https://www.amd.com/Documents/High-Bandwidth-Memory-HBM.pdf)
14. [【レビュー】初のHBM搭載ビデオカード「Radeon R9 Fury X」を試す - PC Watch](http://pc.watch.impress.co.jp/docs/topic/review/20150630_709424.html)
15. [これが“4096”の性能だ：“Fiji”と“HBM”の実力を「Radeon R9 Fury X」で知る (1/5) - ITmedia PC USER](http://www.itmedia.co.jp/pcuser/articles/1506/30/news139.html)
16. [Hot Chips 27 - AMDの次世代GPU「Fury」 (1) HBMを採用したAMDのGPU「Radeon R9 Fury」 | マイナビニュース](http://news.mynavi.jp/series/hotchips27_fury/001/)
17.
18. [NVIDIA® OptiX アプリケーション・エンジン | NVIDIA](http://www.nvidia.co.jp/object/optix_jp.html)
19. [NVIDIA® OptiX Application Acceleration Engine | NVIDIA](https://developer.nvidia.com/optix)
20. [GTC - NVIDIA「OptiX」を解説、レイトレーシングはインタラクティブの時代へ (1) なぜ、今、レイトレーシングなのか | マイナビニュース](https://news.mynavi.jp/article/20091014-gtc06/)
21. [4Gamer.net ― PowerVRのImaginationが“ハイエンドGPU”の設計に着手。ハイブリッドレンダリングハードウェア，そして新API「OpenRL」とは？](http://www.4gamer.net/games/017/G001762/20110920023/)
22. [NVIDIA TESLA: A UNIFIED GRAPHICS AND COMPUTING ARCHITECTURE](http://people.cs.umass.edu/~emery/classes/cmpsci691st/readings/Arch/gpu.pdf) P.44 IEEE 2008年
23. [ホワイトペーパー; NVIDIA の次世代 CUDA™コンピュートアーキテクチャ： Fermi™](http://www.nvidia.co.jp/docs/IO/81860/NVIDIA_Fermi_Architecture_Whitepaper_FINAL_J.pdf)
24. [An Introduction to Modern GPU Architecture](http://http.download.nvidia.com/developer/cuda/seminar/TDCI_Arch.pdf) P.44 NVIDIA
25. [NVIDIA GPUの構造とCUDAスレッディングモデル](https://www.softek.co.jp/SPG/Pgi/TIPS/public/accel/gpu-accel2.html)
26.
27.
28.
29. [■後藤弘茂のWeekly海外ニュース■ DirectX 11でも強力なNVIDIAの新GPU「GF100」](http://pc.watch.impress.co.jp/docs/column/kaigai/20100119_343153.html) PC Watch 2010年1月19日
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.
49. [4Gamer.net ― NVIDIA，Fermi世代の次期GeForce「GF100」グラフィックスアーキテクチャを発表](http://www.4gamer.net/games/099/G009929/20100117001/)
50.
51. [GPU Computing Applications](http://www.eso.org/sci/php/meetings/adass2011/Slides/PDF/All/ADASS_XXI_I15_Ziegler.pdf) P.42 NVIDIA 2011年
52.
53. [AMD's Graphics Core Next Preview: AMD's New GPU, Architected For Compute](http://www.anandtech.com/show/4455/amds-graphics-core-next-preview-amd-architects-for-compute/3) P.3 2011年12月21日
54.
55.
56.
57.
58.
59.
60.
61.
62.
63.
64. [AMD GRAPHIC CORE NEXT](http://developer.amd.com/wordpress/media/2013/06/2620_final.pdf) P.39 AMD 2011年7月
65.
66.
67.
68.
69.
70.
71.
72.
73.
74.
75.
76.
77.
78.
79.
80.
81.
82.
83. [AMD GRAPHIC CORE NEXT](http://developer.amd.com/wordpress/media/2013/06/2620_final.pdf) P.10 AMD 2011年7月
84.
85.
86.
87.
88.
89. [AMD GRAPHIC CORE NEXT](http://developer.amd.com/wordpress/media/2013/06/2620_final.pdf) P.24 AMD 2011年7月
90.
91.
92. [AMD GRAPHIC CORE NEXT](http://developer.amd.com/wordpress/media/2013/06/2620_final.pdf) P.33 AMD 2011年7月
93.
94.
95. [【特別企画】歴代家庭用ゲーム機を軒並み分解――TGS2008「ゲーム科学博物館」より（7ページ目） | 日経 xTECH（クロステック）](https://tech.nikkeibp.co.jp/dm/article/NEWS/20081009/159404/?P=7)
96. [後藤弘茂のWeekly海外ニュース - PLAYSTATION 3のグラフィックスエンジンRSX](https://pc.watch.impress.co.jp/docs/2005/0701/kaigai195.htm)
97. [PS Vitaで採用されるGPUコア「PowerVR SGX543MP4＋」のImaginationに聞く「＋」の意味。PowerVRは次世代ゲーム機への採用も目指す\!? - 4Gamer.net](https://www.4gamer.net/games/144/G014402/20111125078/)
98. [【西川善司】Wii UのGPU性能と新型コントローラに秘められた「コアゲーマー求心」の裏戦略 - 4Gamer.net](https://www.4gamer.net/games/095/G009575/20110624034/)
99. [［CEDEC 2012］3DSはまだその実力を100％発揮できていない\!? 3DSが搭載するGPUコア「PICA200」の詳細 - 4Gamer.net](https://www.4gamer.net/games/017/G001762/20120822007/)
100. [後藤弘茂のWeekly海外ニュース - NVIDIAチーフ・サイエンティスト インタビュー(下)](https://pc.watch.impress.co.jp/docs/2002/0410/kaigai01.htm)
101. [3Dグラフィックス・マニアックス (5) GPUとシェーダ技術の基礎知識(5) | マイナビニュース](https://news.mynavi.jp/column/graphics/005/)
102. [NVIDIA Gaming Technology Powers Nintendo Switch | NVIDIA Blog](https://blogs.nvidia.com/blog/2016/10/20/nintendo-switch/)
103. [Conformant Products - The Khronos Group Inc](https://www.khronos.org/conformance/adopters/conformant-products)
104. [【後藤弘茂のWeekly海外ニュース】PlayStation 4のAPUアーキテクチャの秘密 - PC Watch](http://pc.watch.impress.co.jp/docs/column/kaigai/20131028_621178.html)
105. [CreativeからGeForce 256搭載ビデオカードが登場 - AKIBA PC Hotline\! 1999年10月9日号](http://akiba-pc.watch.impress.co.jp/hotline/991009/geforce256.html)
106. [GeForce 256](http://www.nvidia.co.jp/page/geforce256.html)
107. [3Dlabs Wildcat VP760 Datasheet](http://www.3dlabs.com/legacy/Datasheets/wcvp760.pdf)
108. [ATIがDirectX 9に対応したVPU「RADEON 9700」をリリース](http://pc.watch.impress.co.jp/docs/2002/0718/ati.htm)
109. [Appleから利用停止宣告を受けたImaginationの今 - EE Times Japan](https://eetimes.jp/ee/articles/1808/29/news037.html)
110. [4Gamer.net ― ATIにお別れ。AMD，ATIブランドを統合し，GPUは「AMD Radeon」に](http://www.4gamer.net/games/101/G010106/20100830033/)