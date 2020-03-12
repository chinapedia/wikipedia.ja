> この記事は[VRAM](https://ja.wikipedia.org/wiki/VRAM)から翻訳されています。


'''VRAM '''（ブイラム, **Video RAM**）は、[コンピュータ](../Page/コンピュータ.md "wikilink")などにおける、ディスプレイに対するビデオ（動画像）表示部分のメモリ（[記憶装置](../Page/記憶装置.md "wikilink")）として使われる[RAM](../Page/Random_Access_Memory.md "wikilink")。**グラフィックスメモリ**または**ビデオメモリ**\[1\]とも呼ばれる。専用のデュアルポートのものもあれば、[メインメモリ](https://ja.wikipedia.org/wiki/メインメモリ "wikilink")と同じ[DRAMや](../Page/Dynamic_Random_Access_Memory.md "wikilink")[SRAMを利用したものもある](../Page/Static_Random_Access_Memory.md "wikilink")。かつて、グラフィックス用フレームバッファの為に用意したメモリをG-RAMと表記していた時期もあるが、意味としては等価である。[GPU上で汎用計算を行なう](../Page/Graphics_Processing_Unit.md "wikilink")[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")が普及してからは、グラフィックス用途に限らないデータの処理用途にも転用されている。

## 概要

通常のDRAMをVRAMとして使用する場合、[グラフィックコントローラ](https://ja.wikipedia.org/wiki/グラフィックコントローラ "wikilink") ([CRTC](../Page/CRTC_\(LSI\).md "wikilink")、[VDP](../Page/VDP.md "wikilink")など) とCPUで同時にVRAMをアクセスすることによる競合を避ける必要がある。この解決策としてグラフィックコントローラがバスの空きをチェックして競合を避ける[サイクルスチール](https://ja.wikipedia.org/wiki/サイクルスチール "wikilink")という技法が使われた。また、CPUとグラフィックコントローラで同時にアクセス可能な[デュアルポートRAM](https://ja.wikipedia.org/wiki/デュアルポートRAM "wikilink")と呼ばれるメモリがVRAMとして使われることもあった\[2\]。 、本来の言葉の意味からすると誤用ではあるが、動画像処理用途ではなくともデュアルポートRAMのことをVRAMと呼ぶ用例が過去には多くみられた\[3\] 。広義のデュアルポートRAMとしては1995年にサムスン電子が開発したWRAM (Window RAM) がある。WRAMはデュアルポート構成なだけでなく、チップ上に描画向けの簡単な演算機能を持っており、描画の高速化に一役買っていた。WRAMは[Matrox MillenniumやMillennium](../Page/Matrox_Millennium.md "wikilink") IIで採用されたが、それ以後はデュアルポートRAMは主流ではなくなっている。

2000年台以降ではVRAMの高速化が進み、[GDDR](https://ja.wikipedia.org/wiki/GDDR "wikilink")と呼ばれる高速処理専用のメモリ規格が登場\[4\]。[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")描画における莫大なデータの高速転送を実現している。主な規格として、[GDDR3](../Page/GDDR3.md "wikilink")、、[GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")などが[ビデオカード](../Page/ビデオカード.md "wikilink")に搭載されている。GDDR系統とは別に、根本的なブレイクスルーとなるTB/secの[帯域幅](../Page/帯域幅.md "wikilink")を実現するメモリ規格であるHBM ([High Bandwidth Memory](https://ja.wikipedia.org/wiki/High_Bandwidth_Memory "wikilink")) が考案され、2015年6月にリリースされた[AMD Radeon](../Page/AMD_Radeon.md "wikilink") R9 Fury XにHBM第1世代が世界で初めて搭載された\[5\]。一方で、GDDR5の後継規格として、技術的に従来の延長線上にある[GDDR5X](https://ja.wikipedia.org/wiki/GDDR5X "wikilink")や、[GDDR6も考案されている](https://ja.wikipedia.org/wiki/GDDR6_SDRAM "wikilink")。[コストパフォーマンス](https://ja.wikipedia.org/wiki/コストパフォーマンス "wikilink")の観点から、オフィス用途では[DDR3などの](../Page/DDR3_SDRAM.md "wikilink")[DDR系統が](../Page/DDR_SDRAM.md "wikilink")、ゲーム用途ではGDDR系統が主に用いられている一方、高性能だが高価なHBMはプロフェッショナルグラフィックス用途や[HPC用途](../Page/高性能計算.md "wikilink")（特に人工知能の研究開発で顕著）を中心に利用されている。

その主な用途は[レンダリングした画面を](../Page/レンダリング_\(コンピュータ\).md "wikilink")[走査](../Page/走査.md "wikilink")するまでの[バッファ](../Page/バッファ.md "wikilink")であるが、レンダリングに際して用いる頂点データや[テクスチャ](https://ja.wikipedia.org/wiki/テクスチャ "wikilink")などの素材をバッファリングしたりするなど、中間の処理にも用いられる。これらの構成は各機種の[アーキテクチャによって大きく異なる](../Page/コンピュータ・アーキテクチャ.md "wikilink")。

VRAMを用いたシステムの[メモリ空間](https://ja.wikipedia.org/wiki/メモリ空間 "wikilink")は、[主記憶装置](../Page/主記憶装置.md "wikilink")と同じ[アドレス空間](../Page/アドレス空間.md "wikilink")を持つ場合と、[グラフィックコントローラ](https://ja.wikipedia.org/wiki/グラフィックコントローラ "wikilink")が独立したアドレス空間を持つ場合がある。

VRAMにカラー[ピクセル](../Page/ピクセル.md "wikilink")(画素)を配置する方法としては、カラーコードのビットごとに配置するプレーンドアクセス方式（フレームアクセス方式/水平型VRAM）、カラーコードのバイトごとに配置するパックドピクセル方式（[ビットマップ](https://ja.wikipedia.org/wiki/ビットマップ "wikilink")方式/垂直型VRAM）、キャラクタ単位で配置する[キャラクタグラフィック](../Page/キャラクタ_\(コンピュータ\).md "wikilink")、プログラマブル・キャラクタ・ジェネレータなどがある。

## 素材のバッファ

VRAMの用途のひとつに、レンダリングに用いる素材のバッファリングがある。設計や用途にも依存するが、レンダリングに際してはグラフィックコントローラーからこれら素材に対して頻繁にアクセスする場合が多く、VRAMの重要な用途のひとつとなっている。なお、近代的なグラフィックスデバイスでは必ずしも用途（メモリタイプ）ごとに専用のハードウェアメモリ領域があるというわけではなく、後述するレンダリングバッファ・ランダムアクセスバッファを含め、物理的には均等なハードウェアメモリ領域を必要に応じて切り出して、ドライバーレベルで用途別（読み取り専用／書き込み専用／読み書き両用）に最適化したアクセス方法がなされることになる。

### テキストVRAM

コンピュータにおけるRAMの容量が小さかった時代では、文字のグリフのような高度なグラフィックスデータをそのまま保持しておくことは困難だった。そこで初期のコンピュータでは、キャラクタ（文字）のみの描写に特化したテキスト（文章）画面を持っていた。これは画面上に表示する文字のキャラクタコードのみをVRAMに記憶し、走査時にCRTコントローラがVRAMの値を元にあらかじめキャラクタジェネレータROM内に用意された[フォント](../Page/フォント.md "wikilink")データを文字として展開するものである。

国産機種の場合、CG-ROM内には、ASCIIコードに含まれる英数字の他、空き部分には、カタカナ、記号等が割り当てられ、記号は機種によって異なったほか、平仮名のフォントを持っている機種も存在した。通常、書き込む値は、ASCIIコードと一致していたが、[MZ-80](../Page/MZ-80.md "wikilink")シリーズと、その後継機はディスプレイコードという特殊な並びのデータを書き込むようになっており、テキストモードしか持たない同機では、キャラクタコードの一部を4×4のピクセルに見立て、その組み合わせである空白を除いた15個のパターンを割り当て、80×50ピクセルのビットマップパターンとして見立てる様になっており、擬似的に超低解像度のビットマップを実現していた。広告では「セミグラフィック」と記述されている。

テキストVRAMには、その文字の属性、色等を示すアトリビュートエリアが文字そのもの以外の領域として多くの機種が持っていた。グラフィックスプレーンを兼用する場合は、その場所のデータをどう扱うかというものや、純粋にテキスト用のエリアであっても、複数の文字単位ないし、文字単位で、文字色、背景色、ブリンク、キャラクタテーブルの指定等を行えるようになっていた。これらの構造は、ハードウェア的にキャラクタディスプレイの機能を持たない機種であっても、サブプロセッサ領域内に相当する領域が設けられており、少ないデータによって文字列を処理することを可能にしていた。

また、キャラクタジェネレータROMは、単色、256パターンのフォントを書き込まれたROMであることが多かったが、この部分をRAMにし、物によっては、カラーでデータを持てるようにしたものが、[PCGである](https://ja.wikipedia.org/wiki/キャラクタ_\(コンピュータ\)#PCG "wikilink")。ワープロや、一部機種の外字、ゲーム機のBG画面のパターン等も同様の機能と利便性を提供する。

これらの実装では、1文字に付き、文字種の指定が1バイトとなっており、空白を含め、256種しか取り扱えず、英語圏では有用ではあったものの、日本語の文字情報を取り扱うには仕様として不足していた。そこで、テキストVRAMのテキストを取り扱う部分自体を拡張した、漢字テキストVRAMをハードウェア的に持つようになった機種も生まれた。8ビット機では、[X1turbo](https://ja.wikipedia.org/wiki/X1turbo "wikilink")、[MZ-2500](https://ja.wikipedia.org/wiki/MZ-2500 "wikilink")。16ビット機では[PC-9801](https://ja.wikipedia.org/wiki/PC-9801 "wikilink")シリーズがこれらの仕組みを持っており、グラフィックスプレーンにソフトウェア的に処理するよりも格段に早く、快適な日本語のテキスト処理を可能としていた。

その後、ハードウェアの進化に伴い、日本語処理もソフトウェア的に処理する[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")や、文字の座標が不定である[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")など、速度的に問題がなくなったり、ハードウェアによって表示座標や文字種、フォントが固定されることが問題になる実装が出てくると、ハードウェアによるテキスト処理は見られなくなっていった。ゲーム機などにおけるタイルパターン等の実装も、[ポリゴン](../Page/ポリゴン.md "wikilink")と[テクスチャマッピング](../Page/テクスチャマッピング.md "wikilink")を基準とした構造のハードウェアが増えるにつれ、前述のような構成・機能を持つことは無くなった。

2019年5月現在の[PCでもPOST画面等](../Page/パーソナルコンピュータ.md "wikilink")、最低限のシステムで文字情報が表示できるよう、同じ手順で文字を表示する仕組みを備えている。

### テクスチャバッファ

[ポリゴン](../Page/ポリゴン.md "wikilink")に[テクスチャマッピング](../Page/テクスチャマッピング.md "wikilink")を施す際、その素材となるテクスチャのデータを格納するための領域である。

画像の高精細化にともない、テクスチャのデータも大容量化の傾向にあるため、の[GPUなどはテクスチャバッファに対してデータを自動的に圧縮格納してVRAMを節約する機能を持っていることが多い](../Page/Graphics_Processing_Unit.md "wikilink")（例：[S3TC](https://ja.wikipedia.org/wiki/S3TC "wikilink")やなど）。

### Zバッファ・ステンシルバッファ

画面上へポリゴンを重ね合わせる際に、その優先順位を決定するための深度情報およびその格納領域が[Zバッファ](../Page/Zバッファ.md "wikilink")である。概念についての詳細は該当項目を参照のこと。

初期のポリゴン描画システムでは、**[Zソート](https://ja.wikipedia.org/wiki/Zソート "wikilink")**という簡易的な方式を用いていた。これはポリゴン1枚ごとに深度情報（[Zインデックス](https://ja.wikipedia.org/wiki/Zインデックス "wikilink")）を持たせるものだが、ポリゴン同士が絡み合うように配置された場合には描画結果が意図されたような重ね合わせにならない場合があった。Zバッファはこれを改め、[ピクセル](../Page/ピクセル.md "wikilink")ごとに深度情報を持たせたものである。比較的正確な表示が可能になった一方、情報量や処理負荷は増大したため、GPUの近傍にデータの格納領域が必要となった。

その他、マスク情報を格納するがあり、ステンシルバッファを活用することで描画領域のクリッピングなどを行なうことができる。Zバッファとステンシルバッファは1つの領域にまとめて格納・管理されることもある\[6\] \[7\]。

### 頂点バッファ・インデックスバッファ・定数バッファ

ポリゴンの各頂点の位置情報や色情報などを配列形式でビデオメモリに格納しておき、レンダリングする際に高速参照できるようにするのが頂点バッファである。

また、レンダリングの際に頂点バッファ（頂点配列）中の特定のインデックスを指定して、プリミティブを構成するためのデータを参照することがしばしば行なわれるが、そのインデックス配列を格納するのがインデックスバッファである。

さらに、ワールド座標空間で定義されたポリゴンを画面座標に変換する際に必要となる変換行列、ポリゴン単位やメッシュオブジェクト単位の材質情報、あるいは光源（ライト）の色や減衰係数といった特性情報を格納するのが定数バッファ（定数レジスタ）である。[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")が導入された[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 8以降では、定数バッファ（定数レジスタ）の用途やレイアウトはアプリケーションプログラマーが明示的に制御する。DirectX 9.0cまでは、[頂点シェーダー](https://ja.wikipedia.org/wiki/頂点シェーダー "wikilink")の定数レジスタ数が256あるいはそれ以上、[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")の定数レジスタ数が最大224と制限されていた\[8\]が、DirectX 10以降では定数バッファ（定数レジスタ）が14スロット×4096ベクトルに拡張されるなど、制限が大幅に緩和されている\[9\]。なお、DirectX 11.1以降ではさらに定数バッファのサイズ制限が緩和されている\[10\] \[11\]。

## レンダリングバッファ

レンダリングにかかる時間は、描画の内容やハードウェアの構成によって大きく異なる一方、画面の走査は特定のタイミングでおこなわれる。レンダリングされた画像（レンダリングの過程も含まれる場合がある）を走査するまでの間保持しておくメモリがレンダリングバッファである。

### ラインバッファ

小容量の時代であっても高度なグラフィックスを描く方法が工夫されていた。それは[走査](../Page/走査.md "wikilink")線1本分のみのグラフィックデータを保持するラインバッファである。これは低価格のハードウェアで高速に描画する必要のあった[ゲーム機](../Page/ゲーム機.md "wikilink")などに多用された。[スプライト](../Page/スプライト_\(映像技術\).md "wikilink")、[スクロール](../Page/スクロール.md "wikilink")面、BG面などの画面情報を読み出し、それをVDPが走査線ごとにレンダリングしていた。

走査線1本分のみのデータなので容量が少なくても済む一方、レンダリングのタイミングが厳しく、処理が間に合わないとスプライトなどの表示が欠けてしまう場合がしばしば見られた。

これもRAMの大容量化にともない消えていった。

### フレームバッファ

画面の1[フレーム分をまるごとバッファリングするもの](../Page/コマ_\(映画・漫画\).md "wikilink")。

汎用性の求められるコンピュータでは、画面の表示欠けが許されないとされる場合が多かった。これを解決するために、画面1フレームをまるごとバッファリングすることのできるフレームバッファが多くの機種で採用された。描画処理の時間や順序に多少の融通ができるため、レンダリング処理が間に合わない事態を防ぐ効果がある。ただし能力の限界を超えて描画しようとすると、ラインバッファと同様に表示欠けを生じたり、見た目の[フレームレート](../Page/フレームレート.md "wikilink")が低下（いわゆる[処理落ち](../Page/処理落ち.md "wikilink")）したりする。

初期のパソコンでも中級機以上のものはフレームバッファに似た**グラフィックVRAM**を保有していた。現代から見れば色数が少なかったもののVRAMの使用量は比較的多く、それらがゲーム機や[ホビーパソコン](../Page/ホビーパソコン.md "wikilink")などに比べて非常に高価な理由のひとつとなった。

ゲーム機でも、RAMの容量価格比が増大するとフレームバッファが使われるようになり、本格的な3D描画が可能となった。

高いフレームレートでちらつきのない高度なレンダリングをおこなうため、しばしば**ダブルバッファ**という方式が採られる。これはフレームバッファを2フレーム分用意し、片方がレンダリングの結果を出力している間、もう片方にレンダリングを重ねていくものである。原理上表示欠けは発生しないが、レンダリングに時間がかかると処理落ちを生じてしまう。高度なグラフィックスをリアルタイムで動かすゲームのCGにとって重要な技術だが、VRAMを大量に消費するためゲーム機では容量が不足しやすいといったジレンマがある。プレイステーション2ではこの対策として、[インターレース画面の](https://ja.wikipedia.org/wiki/走査#インターレース方式とプログレッシブ方式 "wikilink")1フレームを2フィールドに分け、片方のフィールドを[走査](../Page/走査.md "wikilink")する間にもう片方のフィールドにレンダリングするという、簡易的なダブルバッファを用いることが多い。この場合プログレッシブ走査が不可能となり、そのためPS2ではプログレッシブ走査に対応したソフトが少ない。

## ランダムアクセスバッファ

レンダリング結果を画面に表示することなく一時的に保存して、同一フレーム内で素材として再利用する場合、書き込み可能な一時テクスチャバッファ（レンダーターゲット）へのレンダリングを行なうといった手法が従来から採用されてきた。DirectX 9では、同一フォーマットの複数レンダーターゲットに対して同時にレンダリングを行なう、マルチレンダーターゲットが標準化された\[12\]。

しかし、GPUを汎用計算に利用する[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")では、出力先には制限・制約の多いテクスチャではなく、[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")（任意インデックスによる読み書き）が可能なバッファのほうが都合がよい。GPGPUのための[APIとして開発](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")・策定された、[NVIDIA CUDA](https://ja.wikipedia.org/wiki/NVIDIA_CUDA "wikilink")、[OpenCL](../Page/OpenCL.md "wikilink")、[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")では、それぞれランダムアクセス可能なバッファが標準化されている。

## VRAMのバスアーキテクチャ

VRAMはその用途から高速性が求められるため、しばしば通常のRAMとは異なる工夫がなされる。

### デュアルポートRAM

VRAMの主用途はバッファであるため、入力用の[バスと出力用のバスを独立させることによって](../Page/バス_\(コンピュータ\).md "wikilink")[スループット](../Page/スループット.md "wikilink")を改善させたものである。[半導体素子](../Page/半導体素子.md "wikilink")が持つ能力の割に高速な処理が可能となるが、[I/O回路が複雑となるため通常のRAMよりも割高である](../Page/入出力ポート.md "wikilink")。

かつてはVRAMといえばデュアルポートRAMが主流だったが、低コストの機種ではデュアルポートRAMを採用しないものも多かった。[SDRAM](../Page/SDRAM.md "wikilink")などシングルポートRAMの高速化技術が発展するとデュアルポートRAMの衰退は顕著となり、では[GDDR3](../Page/GDDR3.md "wikilink")、、[GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")といった高速シングルポートRAMにとって代わられている。

### UMA

描画を走査に間に合わせる必要があることから、VRAMは通常のワークRAM（メインメモリ）よりも高速なものを用いることが多いが、その分素子が高価となる。しかし全てのシステムが高速な描画を要求されているわけではなく、PCの[オンチップグラフィックスなど安価で描画能力を重視しないシステムでは](../Page/オンボードグラフィック.md "wikilink")、専用のVRAMを持たずにメインメモリから間借りする場合が多い。このように、メインメモリの領域から他用途のメモリを間借りすることをUMA（[ユニファイドメモリアーキテクチャ](../Page/ユニファイドメモリアーキテクチャ.md "wikilink")）という。

またUMAには、高速処理が必要な部分だけに高価な素子を用い、比較的低速でも構わない部分はメインメモリに間借りするといった方法もある。その代表例として[AGPが挙げられる](../Page/Accelerated_Graphics_Port.md "wikilink")。これは高速性を求められるフレームバッファのみをビデオカードに実装し、その他のメモリを[CPU](../Page/CPU.md "wikilink")のワークエリアから間借りして、[GPUとの間を専用のバスで繋ぐものである](../Page/Graphics_Processing_Unit.md "wikilink")。

逆に、描画密度の割に画素数の少ないシステムでは、テクスチャバッファなどへ専用VRAMを充当しつつ、フレームバッファのほうをUMAでまかなってしまうといった場合も存在する。

なお、[Xbox 360のように](../Page/Xbox_360.md "wikilink")、システムメモリとビデオメモリはUMAとして共有するものの、フレームバッファ専用に小容量だが高速な[eDRAM](https://ja.wikipedia.org/wiki/eDRAM "wikilink")を備えるアーキテクチャも存在する\[13\]。

では[hUMAとして](https://ja.wikipedia.org/wiki/ユニファイドメモリアーキテクチャ#hUMA "wikilink")、CPUとGPUでメモリマップを統合させている例もある。

## 脚注

## 関連項目

  - [主記憶装置](../Page/主記憶装置.md "wikilink")

  - [GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")

  - [GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")

  - [GDDR3](../Page/GDDR3.md "wikilink")

  -
  - [GDDR5](https://ja.wikipedia.org/wiki/GDDR5 "wikilink")

  - [High Bandwidth Memory](https://ja.wikipedia.org/wiki/High_Bandwidth_Memory "wikilink")

  - [eDRAM](https://ja.wikipedia.org/wiki/eDRAM "wikilink")

[Category:記憶装置](https://ja.wikipedia.org/wiki/Category:記憶装置 "wikilink")

[Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink")

1.  [ビデオメモリとは 【 VRAM 】 〔 グラフィックスメモリ 〕 - 意味/解説/説明/定義 ： IT用語辞典](http://e-words.jp/w/%E3%83%93%E3%83%87%E3%82%AA%E3%83%A1%E3%83%A2%E3%83%AA.html)
2.
3.  [VRAM - 通信用語の基礎知識](https://www.wdic.org/w/SCI/VRAM)
4.  [ASCII.jp：グラフィック専用メモリーの進化と不透明な今後 (1/3)｜ロードマップでわかる！当世プロセッサー事情](https://ascii.jp/elem/000/000/607/607606/)
5.  [【レビュー】初のHBM搭載ビデオカード「Radeon R9 Fury X」を試す - PC Watch](http://pc.watch.impress.co.jp/docs/topic/review/20150630_709424.html)
6.  [glTexImage2D - OpenGL 4 Reference Pages](https://www.khronos.org/registry/OpenGL-Refpages/gl4/html/glTexImage2D.xhtml)
7.  [D3DFORMAT - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3d9/d3dformat)
8.  [Shader Model 3.0; Ashu Rege, NVIDIA Developer Technology Group](ftp://download.nvidia.com/developer/presentations/2004/GPU_Jackpot/Shader_Model_3.pdf)
9.  [シェーダー定数 (DirectX HLSL)](https://msdn.microsoft.com/ja-jp/library/Ee418283.aspx)
10. [Direct3D 11.1 Features - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3d11/direct3d-11-1-features)
11. [Hardware Tiers - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3d12/hardware-support)
12. [Multiple Render Targets (Direct3D 9) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3d9/multiple-render-targets)
13. [CEDEC2005 - Xbox 360ハードウェアの詳細が明らかに (5) Xbox 360-GPUの仕組み(3) - eDRAMがXbox 360グラフィックスのキモとなる | マイナビニュース](http://news.mynavi.jp/articles/2005/09/09/cedec1/004.html)