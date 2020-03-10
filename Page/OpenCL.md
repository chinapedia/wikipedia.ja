> この記事は[OpenCL](https://ja.wikipedia.org/wiki/OpenCL)から翻訳されています。


**OpenCL**（オープンシーエル、）は、[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")[CPU](../Page/CPU.md "wikilink")や[GPU](../Page/Graphics_Processing_Unit.md "wikilink")、[Cellプロセッサ](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")、[DSPなどによる異種混在の](https://ja.wikipedia.org/wiki/デジタルシグナルプロセッサ "wikilink")[計算資源](../Page/計算資源.md "wikilink")（ヘテロジニアス環境、[ヘテロジニアス・コンピューティング](https://ja.wikipedia.org/wiki/ヘテロジニアス・コンピューティング "wikilink")、）を利用した[並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")のための[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な[APIである](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")。主な用途は科学技術計算や[画像処理](https://ja.wikipedia.org/wiki/画像処理 "wikilink")に代表される[高性能計算](https://ja.wikipedia.org/wiki/高性能計算 "wikilink")のための[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")の高速化（[ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")）であり、シミュレーション可視化に用いるリアルタイム[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")APIとの連携も拡張機能として標準化されている。[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")や[サーバ](../Page/サーバ.md "wikilink")、[ワークステーション](../Page/ワークステーション.md "wikilink")や[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")のほか、[携帯機器](../Page/携帯機器.md "wikilink")などでの利用も想定されており、[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けに必要条件を下げたOpenCL Embedded Profileが存在する。

## 仕様

OpenCLの仕様は[アップルによって提案されたのち](../Page/アップル_\(企業\).md "wikilink")、標準化団体[クロノス・グループ](https://ja.wikipedia.org/wiki/クロノス・グループ "wikilink")の作業部会（旧）によって策定されている。仕様は[ロイヤリティフリー](https://ja.wikipedia.org/wiki/ロイヤリティフリー "wikilink")な[オープン標準](../Page/オープン標準.md "wikilink")として公開されており、仕様に基づいたフレームワークの[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")は[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")によって行われる。ただし、実装されたフレームワークに対して許諾される商標ライセンスに必要な仕様一致性テストには、（名目上の手数料）が必要である\[1\]。

## 特徴

OpenCLには次のような特徴がある。

  - CPU（CL_DEVICE_TYPE_CPU）、GPU（CL_DEVICE_TYPE_GPU）、およびCell/[FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")/[Xeon Phi](https://ja.wikipedia.org/wiki/Xeon_Phi "wikilink")\[2\]など（CL_DEVICE_TYPE_ACCELERATOR）の各種計算資源のサポート

  - [C言語](../Page/C言語.md "wikilink")（ISO [C99](../Page/C99.md "wikilink")規格）をベースにしたOpenCL C、あるいは[C++](../Page/C++.md "wikilink")言語（ISO [C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")規格）をベースにしたOpenCL C++[プログラミング言語](../Page/プログラミング言語.md "wikilink")による[カーネル記述](https://ja.wikipedia.org/wiki/ストリーム・プロセッシング "wikilink")

      - 組み込みの[ベクトル](https://ja.wikipedia.org/wiki/ベクトル "wikilink")型およびベクトル演算のサポート（float2型、float4型などや、Swizzle演算など）
      - オンラインのOpenCL C[コンパイラ](../Page/コンパイラ.md "wikilink")

  - およびSPIR-V中間表現のサポート (SPIR 1.2/2.0 for OpenCL 1.2/2.0, SPIR-V 1.0 for OpenCL 2.1)

  - [データ並列および](https://ja.wikipedia.org/wiki/データ並列性 "wikilink")[タスク並列のプログラミングモデルのサポート](https://ja.wikipedia.org/wiki/タスク並列性 "wikilink")

  - [同期](../Page/同期.md "wikilink")ポイント以外での内容の一貫性 (consistency) を保証しない、緩和型一貫性共有メモリモデル ()

  - 同期ポイントおよびOpenCLアトミック操作でのホスト・デバイス間のメモリ一貫性を保証する共有仮想メモリ (shared virtual memory: SVM, OpenCL 2.0)\[3\]

  - [IEEE 754準拠の単精度](https://ja.wikipedia.org/wiki/IEEE_754 "wikilink")[浮動小数点数](../Page/浮動小数点数.md "wikilink")（float型）演算のサポート

      - [ポインタ渡しおよびfloat型との相互変換関数経由でのアクセスに限定される](../Page/ポインタ_\(プログラミング\).md "wikilink")[IEEE 754-2008準拠の](https://ja.wikipedia.org/wiki/IEEE_754r "wikilink")[半精度浮動小数点数](https://ja.wikipedia.org/wiki/半精度浮動小数点数 "wikilink")（half型）
          - OpenCL 1.0においては、half型の直接演算は拡張 (cl_khr_fp16) による任意サポートに留まる
      - OpenCL 1.0においては、[倍精度浮動小数点数](https://ja.wikipedia.org/wiki/倍精度浮動小数点数 "wikilink")（double型）は拡張 (cl_khr_fp64) による任意サポートに留まる

  - 1次元/2次元/3次元のイメージオブジェクトのサポート（1次元イメージはOpenCL 1.2以降\[4\]）

  - [OpenGL](../Page/OpenGL.md "wikilink")および[OpenGL ESの](../Page/OpenGL_ES.md "wikilink")[バッファ](https://ja.wikipedia.org/wiki/バッファ "wikilink")、[テクスチャ](https://ja.wikipedia.org/wiki/テクスチャ "wikilink")、レンダーバッファとの連携（cl_gl.h、OpenCL 1.0以降の拡張\[5\]）

  - [OpenGL ESのイメージ](../Page/OpenGL_ES.md "wikilink")、ディスプレイ、同期オブジェクトとの連携（cl_egl.h、OpenCL 1.2以降の拡張）

  - [Direct3D 10のバッファおよびテクスチャとの連携](https://ja.wikipedia.org/wiki/Direct3D "wikilink")（cl_d3d10.h、OpenCL 1.0以降の拡張）

  - [Direct3D 11のバッファおよびテクスチャとの連携](https://ja.wikipedia.org/wiki/Direct3D "wikilink")（cl_d3d11.h、OpenCL 1.2以降の拡張）

  - [DirectX 9のメディアサーフェイス連携](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")（cl_dx9_media_sharing.h、OpenCL 1.2以降の拡張）

### グラフィックスAPIとの関連性および相互運用性

OpenCL類似技術に[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")の[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")（後述）が存在するが、OpenCLにはCUDA同様に、3Dグラフィックス[APIであるOpenGL](../Page/アプリケーションプログラミングインタフェース.md "wikilink")（[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")）およびDirect3D（[Windowsプラットフォーム専用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）との相互運用性（）がAPIレベルで確保されている。

なお、OpenCLの動作ターゲットとしての用件を満たしたGPU（主にDirectX 10世代以上の[統合型シェーダーアーキテクチャ](https://ja.wikipedia.org/wiki/統合型シェーダーアーキテクチャ "wikilink")を採用したGPU）で使用できるDirect3D API（Direct3D 10およびDirect3D 11）との相互運用機能は、クロノスが管理しているOpenCL API公式拡張でサポートされるが、旧来のDirect3D 9との相互運用機能は、OpenCL 2.0時点でもベンダーごとの拡張機能依存となっている（cl_d3d9_ext.h）。

OpenCLでのhalf/double型のサポート状況は、CUDAなどのほかのAPIとよく似ている\[6\]。また、OpenGL/Direct3Dでは浮動小数点テクスチャすなわちデータストレージのフォーマットとしてFP32形式のほかにFP16形式を選択できるが、通例GPUが得意とする演算精度は単精度であるため、シェーダープログラム中で利用できる演算精度は一般的には単精度となり、倍精度や半精度はオプション扱いとなる。

### プラットフォームとデバイス

OpenCL実行環境であるオペレーティングシステム上には、Installable Client Driver (ICD) Loaderという仕組みにより、複数のベンダーによるOpenCL実装を混在させることができる（cl_khr_icd）\[7\]。各ベンダーのOpenCL実装は「プラットフォーム」として抽象化され、OpenCL APIを通じて列挙・選択することができる。

またOpenCLはカーネルコードの実行ハードウェアを「デバイス」として抽象化する。各OpenCLプラットフォームは複数のOpenCLデバイスを持つことができ、OpenCL APIを通じて列挙・選択できる。

## 歴史

2008年6月10日（日本時間）の[Worldwide Developers Conferenceにおいて](https://ja.wikipedia.org/wiki/Worldwide_Developers_Conference "wikilink")、[Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") [Snow Leopard](../Page/Mac_OS_X_v10.6.md "wikilink")（[v10.5 Leopardの次期メジャーバージョンとされる](../Page/Mac_OS_X_v10.5.md "wikilink")）に搭載される予定の技術の1つとして初めて発表された\[8\]。

標準化団体[クロノス・グループ](https://ja.wikipedia.org/wiki/クロノス・グループ "wikilink")の2008年6月16日に発足した作業部会 において、[アップルによってOpenCLの仕様草案が提案された](../Page/アップル_\(企業\).md "wikilink")\[9\]。CWGはGPUとCPUのヘテロジニアス（異種混在）な計算技術の[ロイヤリティフリー](https://ja.wikipedia.org/wiki/ロイヤリティフリー "wikilink")な標準化を目的としており、発足時点では[3Dlabs](https://ja.wikipedia.org/wiki/3Dlabs "wikilink")、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、アップル、[ARM](https://ja.wikipedia.org/wiki/ARMホールディングス "wikilink")、[Codeplay](https://ja.wikipedia.org/wiki/Codeplay "wikilink")、[エリクソン](https://ja.wikipedia.org/wiki/エリクソン "wikilink")、[フリースケール・セミコンダクタ](https://ja.wikipedia.org/wiki/フリースケール・セミコンダクタ "wikilink")、[Graphic Remedy](https://ja.wikipedia.org/wiki/Graphic_Remedy "wikilink")、[IBM](../Page/IBM.md "wikilink")、、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[ノキア](https://ja.wikipedia.org/wiki/ノキア "wikilink")、[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")、[モトローラ](../Page/モトローラ.md "wikilink")、[QNX](https://ja.wikipedia.org/wiki/QNX "wikilink")、[クアルコム](https://ja.wikipedia.org/wiki/クアルコム "wikilink")、[サムスン](https://ja.wikipedia.org/wiki/サムスングループ "wikilink")、[Seaweed](https://ja.wikipedia.org/wiki/Seaweed "wikilink")、[テキサス・インスツルメンツ](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink")、スウェーデン・[ウメオ大学](../Page/ウメオ大学.md "wikilink")が参加している。

2008年8月の[SIGGRAPH](https://ja.wikipedia.org/wiki/SIGGRAPH "wikilink") 2008および同年11月のにおいて、仕様策定の進捗状況が発表され、同時期には名称をと改められ、新たに[アクティビジョン・ブリザード](https://ja.wikipedia.org/wiki/アクティビジョン・ブリザード "wikilink")、[バルコ](https://ja.wikipedia.org/wiki/BArco "wikilink")、[ブロードコム](https://ja.wikipedia.org/wiki/ブロードコム "wikilink")、[エレクトロニック・アーツ](https://ja.wikipedia.org/wiki/エレクトロニック・アーツ "wikilink")、[エイチアイ](https://ja.wikipedia.org/wiki/エイチアイ "wikilink")、[ケストレル研究所](https://ja.wikipedia.org/wiki/ケストレル研究所 "wikilink")、[Movidia](https://ja.wikipedia.org/wiki/Movidia "wikilink")、、TAKUMIが参加している。11月10日にはRapidMindが自社の並列コンピューティング開発環境においてOpenCLを採用すると発表した\[10\]。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[12月9日](../Page/12月9日.md "wikilink")のSIGGRAPH Asia 2008において、正式版となるOpenCL 1.0の仕様が発表された\[11\]。またほぼ同時期に、AMDとNVIDIAはそれぞれ自社の[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")技術である[ATI Streamおよび](https://ja.wikipedia.org/wiki/ATI_Stream "wikilink")[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")においてOpenCL 1.0をサポートすると発表した\[12\]\[13\]。OpenCL 1.0対応の最初のプラットフォームとして、[Mac OS X Snow Leopardが](../Page/Mac_OS_X_v10.6.md "wikilink")[2009年](../Page/2009年.md "wikilink")[8月28日](../Page/8月28日.md "wikilink")にリリースされた。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[6月14日](../Page/6月14日.md "wikilink")、OpenCL 1.1を正式発表\[14\]。 float3型の追加、clSetKernelArg()関数以外のスレッドセーフ化\[15\]など。

[2011年](../Page/2011年.md "wikilink")[11月15日](../Page/11月15日.md "wikilink")、OpenCL 1.2を正式発表\[16\]。 分割コンパイル＆リンク対応、SubDeviceの追加、SPIR 1.2拡張機能、3Dイメージの書き込み拡張機能\[17\]など。

[2013年](../Page/2013年.md "wikilink")[7月22日](../Page/7月22日.md "wikilink")、OpenCL 2.0を正式発表\[18\]。 read_write修飾子\[19\]、共有仮想メモリ (Shared Virtual Memory) や動的並列処理 (Dynamic Parallelism) 対応など。

[2015年](../Page/2015年.md "wikilink")[11月16日](https://ja.wikipedia.org/wiki/11月16日 "wikilink")、OpenCL 2.1を正式発表\[20\]。 SPIR-V[中間言語](../Page/中間言語.md "wikilink")による[Vulkan](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink") API (OpenGL Next Generation, glNext) とのプログラミング基盤共通化など。2015年3月3日の暫定仕様の発表時点でカーネル記述言語への[C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink")サブセット導入も予定されていた\[21\]が、OpenCL 2.1正式仕様の発表とともに、OpenCL C++のリリースは早くて2016年半ばとアナウンスされた。

[2017年](../Page/2017年.md "wikilink")[5月16日](../Page/5月16日.md "wikilink")、OpenCL 2.2を正式発表\[22\]。2016年4月18日の暫定仕様の発表時点でアナウンスされていた、OpenCL C++言語、SYCL 2.2フレームワーク\[23\]に加えて、中間表現SPIR-V 1.2などが導入された。

## 類似技術

OpenCLのように異種プロセッサをバックエンドとして活用するAPIは、GPGPU黎明期のものや、GPU専用のもの、特定のベンダー専用のもの、そして仕様が標準化されていないものまで含めると多数存在する。

  - [CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")（）
    NVIDIAによる[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink") / [Quadro](https://ja.wikipedia.org/wiki/Quadro "wikilink") / [Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink") / [TegraシリーズGPU用のGPGPU開発](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink")・実行環境。[C言語](../Page/C言語.md "wikilink")を拡張したCUDA Cによる開発を可能にする（Ver.2.2以降は[C++](../Page/C++.md "wikilink")言語を拡張したCUDA C++による開発も可能となっている）。NVIDIAによるコンパイラ実装*nvcc*だけでなく、オープンソースコンパイラのLLVMでもCUDAコンパイラの実装が始まっている\[24\] \[25\]。また、PGI社からはCUDA Fortran Compilerが提供されている\[26\]。

  - （）
    AMD社による[ATI系GPUのストリームプロセッサインターフェイス](https://ja.wikipedia.org/wiki/ATI_Technologies "wikilink")。ハードウェアに近いローレベル制御を可能とする\[27\]。

  - [AMD Stream](https://ja.wikipedia.org/wiki/AMD_Stream "wikilink")（旧[ATI Stream](https://ja.wikipedia.org/wiki/ATI_Stream "wikilink")）
    AMDによる[ATI系GPU用のGPGPU開発](https://ja.wikipedia.org/wiki/ATI_Technologies "wikilink")・実行環境。CTMをCompute Abstraction Layer（CAL）\[28\]によって抽象化し、Brook言語をCAL用に拡張したBrook+言語による開発を可能にする。なおAMDは「GPGPUでDirectX 11およびOpenCLをフルサポートする」と発表し\[29\] \[30\]、。

    その後、同社はHSA推進とともに、独自規格ではなくOpenCLをヘテロジニアス戦略の中核とする方向に舵を切り直した。AMDによるCPU/GPU/APU対応の総合基盤テクノロジーは「[AMD Accelerated Parallel Processing](https://ja.wikipedia.org/wiki/AMD_Accelerated_Parallel_Processing "wikilink")」（AMD APP）と呼ばれており、SDKの名称もATI Stream SDKからAMD APP SDKに変更・統一されている。

  -  (libsh)
    [ウォータールー大学](https://ja.wikipedia.org/wiki/ウォータールー大学 "wikilink")コンピュータグラフィックス研究室の成果に基づいた、RapidMindによる[シェーダー](../Page/シェーダー.md "wikilink")プログラミングおよびGPGPUのための[メタプログラミング](https://ja.wikipedia.org/wiki/メタプログラミング "wikilink")技術。C++言語による開発を可能にする。[LGPLライセンスで公開されている](../Page/GNU_Lesser_General_Public_License.md "wikilink")。

  - [RapidMind](https://ja.wikipedia.org/wiki/RapidMind "wikilink")

    による商用並列コンピューティング開発環境。GPU／[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")CPU／[Cellプロセッサを](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")に利用できる。C++言語による開発を可能にする。

  -  (Brook for GPU)
    [スタンフォード大学](../Page/スタンフォード大学.md "wikilink")コンピュータグラフィックス研究室によるストリーム・コンピューティング開発環境。GPUおよび[OpenMP](../Page/OpenMP.md "wikilink")によるマルチコアCPU演算をバックエンドに利用できる。C言語 (ANSI C) を拡張したBrook言語による開発を可能にする。[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")および[GPLライセンスで公開されている](../Page/GNU_General_Public_License.md "wikilink")。

  - [PeakStream](https://ja.wikipedia.org/wiki/PeakStream "wikilink")
    [PeakStream](https://ja.wikipedia.org/wiki/PeakStream "wikilink")による商用ストリーム・コンピューティング開発環境。GPU / マルチコアCPU / Cellプロセッサをバックエンドに利用できる。PeakStreamは2007年6月頃までに[Google](../Page/Google.md "wikilink")によって買収されている。

  - [DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")
    [マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発・配布している[DirectXテクノロジーのひとつであり](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、DirectX 11/DirectX 12セットに含まれるGPGPU向けのAPI。GPGPU向けのシェーダーステージとして導入されたCompute Shaderを利用する。[HLSLをカーネル記述言語とする](https://ja.wikipedia.org/wiki/High_Level_Shading_Language "wikilink")。グラフィックス連携用途を重視している\[31\]。動作環境は[Windows Vista以降のWindowsおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[Xbox One](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")。

  - [C++ AMP](https://ja.wikipedia.org/wiki/C++_AMP "wikilink")
    ハードウェアアクセラレートされた並列処理をC++言語で記述できるようにする高レベルのライブラリ・言語拡張。DirectComputeを[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")とする[Microsoft Visual C++実装のほか](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink")、OpenCLなどをバックエンドとするLinux向けのC++ AMPオープン実装もある\[32\] \[33\]。

  - [OpenGL](../Page/OpenGL.md "wikilink") Compute Shader
    DirectXに搭載されている前述のCompute Shader同様、OpenGLでもバージョン4.3でGPGPU向けのシェーダーステージが標準化された。[GLSL](../Page/GLSL.md "wikilink")をカーネル記述言語とする。

  - [OpenMP](../Page/OpenMP.md "wikilink") LEO (Language Extensions for Offload)
    [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")によるIntel MIC (Many Integrated Core) およびGFXへオフロードするための[OpenMP](../Page/OpenMP.md "wikilink")拡張。ICC ([Intel C++ Compiler](../Page/Intel_C++_Compiler.md "wikilink")) に実装されている\[34\]。

  - OpenMP 4.0以降
    offloadに対応している。[OpenMP](../Page/OpenMP.md "wikilink")®/[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")はoffloadに未対応\[35\]。[GCC](../Page/GNUコンパイラコレクション.md "wikilink") 5.0はMICへのオフロードに対応する予定\[36\]。

  - [OpenACC](https://ja.wikipedia.org/wiki/OpenACC "wikilink")
    [OpenMP](../Page/OpenMP.md "wikilink")のようにコード中にディレクティブを挿入することで、並列処理のハードウェアアクセラレートを行なえるようにする規格\[37\]。PGIが開発した技術で、同社のPGIコンパイラに初めて搭載された\[38\]。そのほかには、[GCC](../Page/GNUコンパイラコレクション.md "wikilink") 5.0に搭載される\[39\]。

  - SPMD Programming Language
    インテルによって開発された、C言語を拡張した対応言語であり、Intel SPMD Program Compiler (ISPC) でコンパイル可能\[40\]。ISPCはオープンソースであり、バックエンドにLLVMを使用している\[41\]。IntelのCPUやXeon Phiだけでなく、NVIDIA Kepler GPUにも対応している\[42\]。ISPCを導入している例としては、オープンソースの[レイトレーシング](../Page/レイトレーシング.md "wikilink")エンジンであるEmbreeがある\[43\]。

## 関連技術

  - SASS
    NVIDIAのGPUで使われるハードウェア依存の低級アセンブリ言語\[44\]。NVIDIA Nsight開発環境がSASSレベルでのデバッグに対応している\[45\]。SASSのアセンブラは、asfermi\[46\]やMaxAs\[47\]などがある。 SASS言語で書かれた例としては、NervanaGPUがある\[48\]\[49\]。
  - PTX ([Parallel Thread Execution](https://ja.wikipedia.org/wiki/Parallel_Thread_Execution "wikilink"))
    NVIDIAのGPU向けのハードウェア非依存な擬似アセンブリ言語\[50\]。PTXのアセンブラは、ptxasがある\[51\]。asm文によって、CUDAやOpenCLのコードにPTXのコードを埋め込むことも可能\[52\]\[53\]。
    LLVM/ClangにはOpenCLのフロントエンド\[54\]およびPTXのバックエンド\[55\]が含まれており、OpenCLからLLVM IRを通してPTXへと変換し、CUDA Driver APIで実行したり\[56\]、ptxasでSASSへと変換することが可能\[57\]。
  - AMD Intermediate Language (AMD IL)
    AMDのGPU向けのハードウェア非依存な擬似アセンブリ言語\[58\]。コンパイルは、CAL (Compute Abstraction Layer) APIのcalclCompile関数で行なう\[59\]。 。なおAMD ILのサブセットはローレベルグラフィックスAPIである[Mantleでも利用されている](https://ja.wikipedia.org/wiki/Mantle_\(API\) "wikilink")\[60\]。
  - AMD Instruction Set Architecture (AMD ISA)
    AMDのGPUで使われるハードウェア依存の低級アセンブリ言語。LLVMが(VLIW4/5) および[GCNアーキテクチャに対応するR](https://ja.wikipedia.org/wiki/Graphics_Core_Next "wikilink")600バックエンドを持っており\[61\]\[62\]、LLVM/ClangでOpenCLからAMD ISAアセンブリへと変換したり、AMD ISAアセンブリからllvm-asでバイナリ化したりすることが可能。アセンブルしたバイナリはOpenCL APIのclCreateProgramWithBinary関数で実行する。
  - intel-gen4asm
    Intel GPU向けのアセンブラ\[63\]。オープンソース。
  - TGSI (Tungsten Graphics Shader Infrastructure)
    オープンソースなハードウェア非依存の[中間言語](../Page/中間言語.md "wikilink")\[64\]。オープンソースGPUドライバである[Mesa 3D](../Page/Mesa_3D.md "wikilink")/[Gallium3D](https://ja.wikipedia.org/wiki/Gallium3D "wikilink")の中間表現形式として使われている。2013年現在、Gallium3D OpenCL実装のために、LLVMのTGSIバックエンドが開発中となっている\[65\]。GPGPUだけでなく、グラフィックスにも対応している。
  -  (Standard Portable Intermediate Representation)
    [クロノス・グループ](https://ja.wikipedia.org/wiki/クロノス・グループ "wikilink")によって、OpenCLのために開発された中間言語。OpenCL 1.2とともにSPIR 1.2が、そしてOpenCL 2.0とともにSPIR 2.0が策定された。OpenCL 2.1および[Vulkanとともに策定されるSPIR](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")-Vでは、GPGPUだけでなく、グラフィックスにも対応している\[66\]。
  - HSAIL
    HSA Foundationで標準化された(HSA) 向けのハードウェア非依存な中間言語。AMDやLLVMのOpenCL実装がHSAIL中間表現形式の出力に対応している\[67\]。異種コア間のスケジューリングを前提としており、グラフィックスには非対応\[68\]。

## OpenCL開発環境

OpenCLを使用したクライアント プログラムを開発するための代表的な[ソフトウェア開発キット](https://ja.wikipedia.org/wiki/ソフトウェア開発キット "wikilink")（SDK）として、主に各ハードウェア ベンダーから下記のSDKが提供されている。

  - [NVIDIA CUDA Toolkit](https://developer.nvidia.com/cuda-toolkit)
    Windows, Linux, [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用が提供されている。かつてNVIDIAのOpenCL SDKは"NVIDIA GPU Computing SDK"に含まれていて、CUDA SDKとは独立していたが、CUDA 5.0からはCUDA Toolkitにすべて含まれるようになった。以前のバージョンのGPU Computing SDKはアーカイブとして公開されているが、CUDA Toolkitのページから直接たどることはできない\[69\] \[70\]。"CUDA Toolkit 7.5"時点でOpenCL 1.2に対応している\[71\] \[72\] \[73\]。
  - [AMD Accelerated Parallel Processing SDK](http://developer.amd.com/tools-and-sdks/opencl-zone/amd-accelerated-parallel-processing-app-sdk/)
    Windows, Linux用が提供されている。"AMD APP SDK 3.0"時点でOpenCL 2.0、 1.2に対応している\[74\] \[75\] \[76\]。
  - [Intel® SDK for OpenCL™ Applications](https://software.intel.com/en-us/intel-opencl/download), [Intel Integrated Native Developer Experience (Intel INDE)](https://software.intel.com/en-us/intel-inde)
    Windows, Linux, [Android](../Page/Android.md "wikilink") 用が提供されている。単独の "Intel SDK for OpenCL" (Intel OpenCL SDK) のほか、2015年からは統合ツールとして Intel INDE も提供されている。OpenCL 2.0、 1.2をサポートしている\[77\] \[78\]。

<!-- end list -->

  - [Qualcomm Adreno SDK](https://developer.qualcomm.com/mobile-development/maximize-hardware/mobile-gaming-graphics-adreno/tools-and-resources)
    [Snapdragon](https://ja.wikipedia.org/wiki/Snapdragon "wikilink") 向け
  - [ARM Mali OpenCL SDK](http://malideveloper.arm.com/develop-for-mali/sdks/mali-opencl-sdk/)
    [ARM](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink") を採用した[SoC向け](https://ja.wikipedia.org/wiki/System-on-a-chip "wikilink")。SDK v1.1時点でOpenCL 1.1に対応している。
  - [Imagination PowerVR SDK](http://community.imgtec.com/developers/powervr/)
    Apple の SoC 等で使われている [PowerVR](../Page/PowerVR.md "wikilink") 向け
  - [IBM OpenCL SDK](http://www.alphaworks.ibm.com/tech/opencl)
    Linux (x86, [PowerPC](../Page/PowerPC.md "wikilink")) 用が提供されている。
  - Beignet (Intel)
    Linux用。オープンソース。[LLVM](../Page/LLVM.md "wikilink")ベース。
  - [OpenCL for macOS](https://developer.apple.com/opencl/)
    macOSの標準機能としてOpenCLをサポートしている\[79\]。OpenCL 1.2までをサポートするが、対応バージョンはハードウェアにもよる\[80\]。
  - [Altera SDK for OpenCL](http://www.altera.co.jp/products/software/opencl/opencl-index.html)
    [FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")上で動作するOpenCLプログラムを開発することができる。[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")プロセッサ対応の[エミュレータ](../Page/エミュレータ.md "wikilink")も提供されている。
  - [Xilinx SDAccel](http://japan.xilinx.com/products/design-tools/sdx/sdaccel.html)
    [FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")上で動作するOpenCLプログラムを開発することができる。

各SDKには、標準OpenCL API用のC/C++言語用ヘッダーなどのほか、ベンダーごとに拡張された機能を使うためのライブラリなども含まれるため、ハードウェア ベンダーやOSに依存しないOpenCLプログラムを開発する場合は注意が必要となる。

OpenCLのプログラムは、[GLSL](../Page/GLSL.md "wikilink")を利用したOpenGLプログラムとほぼ同じ要領で開発することができ、CUDAプログラムのような専用オフライン コンパイラ（nvcc）を必要としないため、様々なプラットフォームへの展開が容易となることが利点である。ただし初回の実行時コンパイル（オンライン コンパイル）に時間がかかるなどのデメリットも存在する。この点に関しては、実運用時にはclCreateProgramWithSource()関数によるオンライン コンパイルは行なわず、clGetProgramInfo()関数とclCreateProgramWithBinary()関数を用いてコンパイル済みバイナリからプログラムオブジェクトを生成する方法もある\[81\] \[82\] \[83\] \[84\]（ただしベンダーごとのOpenCLバイナリ間における互換性は保証されない）。なお、OpenCL 1.2、2.0、2.1では、およびSPIR-Vと呼ばれる中間表現（[中間言語](../Page/中間言語.md "wikilink")、[バイトコード](../Page/バイトコード.md "wikilink")）をサポートすることにより、ベンダーに依存しないカーネルコードをコンパイル・実行することができるようになる\[85\]。ただし、SPIR 1.2およびSPIR 2.0はOpenCL 1.2およびOpenCL 2.0の拡張機能（cl_khr_spir\[86\]）となっており、サポート必須の機能ではない。一方、SPIR-VはOpenCL 2.1のコア機能となる\[87\]。

### OpenCLプロファイラー

OpenCL対応の[プロファイラー](https://ja.wikipedia.org/wiki/プロファイラー "wikilink")が各社からリリースされている。従来の非並列プログラムと比較するとOpenCLプログラムは[デバッグ](../Page/デバッグ.md "wikilink")や[チューニング](https://ja.wikipedia.org/wiki/チューニング "wikilink")が難しく、プロファイラーは性能ボトルネックの特定やコード改善に有効なツールである。

  - [Intel VTune Amplifier](https://software.intel.com/en-us/intel-vtune-amplifier-xe/)（有償）
    マルチコアCPU対応のプロファイラーだが、OpenCL\[88\]のほか、DirectXにも対応している\[89\]。
  - [AMD CodeXL](http://developer.amd.com/tools-and-sdks/opencl-zone/codexl/)（無償）
    CPU/GPUのデバッギング／プロファイリング用ツール。OpenCLのほか、OpenGLやDirect3D (DirectCompute) 開発にも使用できる\[90\]。
  - [NVIDIA Nsight](http://www.nvidia.com/object/nsight.html)（無償）
    OpenCLのほか、CUDA、Direct3D (DirectCompute)、およびOpenGLに対応している\[91\]。

### OpenCLシミュレータ／エミュレータ

  - [GPGPU-Sim](http://www.gpgpu-sim.org/)（無償）
    GPUのサイクルレベルシミュレータ。CUDAおよびOpenCLに対応している。Linux専用であり、また実行にはNVIDIAドライバーが必要となる\[92\]。
  - [AMD OpenCL™ Emulator-Debugger (ocl-emu)](http://developer.amd.com/tools-and-sdks/opencl-zone/opencl-emulator-debugger/)（無償）
    AMDによるOpenCLソフトウェアエミュレータの[オープンソース](../Page/オープンソース.md "wikilink")実装。2012年10月12日版において、OpenCL 1.2に対応している。対応OSは[Microsoft Windows XP以降で](../Page/Microsoft_Windows_XP.md "wikilink")、ビルドに[Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") 2008/2010を必要とし、また実行プラットフォームとして[AMD Accelerated Parallel Processing](https://ja.wikipedia.org/wiki/AMD_Accelerated_Parallel_Processing "wikilink") (AMD APP) SDKを必要とする\[93\]。

## ラッパー

Khronosが公開しているOpenCL APIはC/C++言語向けのヘッダーおよびC++言語用ラッパークラスのヘッダー（cl.hpp）のみだが、各種言語用にラッパーライブラリがオープンソースコミュニティなどによって開発されている。

  - [C++](../Page/C++.md "wikilink")
      - [Bolt C++ Template Library](http://developer.amd.com/tools-and-sdks/opencl-zone/bolt-c-template-library/)
      - [Boost::Compute](https://boostorg.github.io/compute/)
      - [C++ AMP](https://ja.wikipedia.org/wiki/C++_AMP "wikilink")
      - [VexCL](http://ddemidov.github.io/vexcl/)
  - [C\#](../Page/C_Sharp.md "wikilink")
      -
      -
  - [D言語](../Page/D言語.md "wikilink")
      - [cl4d](http://bitbucket.org/trass3r/cl4d)
  - [ECMAScript](../Page/ECMAScript.md "wikilink") ([JavaScript](../Page/JavaScript.md "wikilink"))
      - [WebCL](https://ja.wikipedia.org/wiki/WebCL "wikilink")
          - [node-webcl](https://www.npmjs.com/package/node-webcl)
          - Nokia ([Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")) - <http://webcl.nokiaresearch.com/>
          - Samsung ([WebKit](https://ja.wikipedia.org/wiki/WebKit "wikilink")) - <https://github.com/SRA-SiliconValley/webkit-webcl>
      - [River Trail](https://github.com/IntelLabs/RiverTrail)
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
      - [Aparapi](http://code.google.com/p/aparapi/)
      - [JogAmp](http://jogamp.org/) - OpenCL, [OpenGL](../Page/OpenGL.md "wikilink"), [OpenAL](https://ja.wikipedia.org/wiki/OpenAL "wikilink"), [OpenMAX](https://ja.wikipedia.org/wiki/OpenMAX "wikilink") の [Java](https://ja.wikipedia.org/wiki/Java "wikilink") ラッパー
      - [LWJGL](https://ja.wikipedia.org/wiki/LWJGL "wikilink") - OpenCL, OpenGL, OpenAL などの Java ラッパー
  - [LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")系
      - [Harlan](https://github.com/eholk/harlan)
  - [Python](../Page/Python.md "wikilink")
      - [PyOpenCL](http://mathema.tician.de/software/pyopencl/)

      -
  - [Ruby](../Page/Ruby.md "wikilink")
      - [Ruby-OpenCL](http://ruby-opencl.rubyforge.org/)
  - thinBasic
      - [OpenCL 1.1 headers](http://www.thinbasic.com/community/showthread.php?10159-OpenCL-Headers-Updated-Sep-15-2011)

## ベンチマーク

  - LuxMark - 定番のレンダリングベンチマーク。
  - x264 OpenCL - Phoronix Test Suiteに含まれるベンチマークの一つ\[94\]。
  - CompuBench CL
  - Rodinia Benchmark Suite - 多種のベンチマークがある。
  - OpenDwarfs
  - Parboil Benchmarks
  - PolyBench/GPU
  - SHOC benchmark suite

## 採用事例

画像処理/映像処理においては、OpenCLもしくはCUDAによるGPGPU対応が進んでいる。また、3DCGの物理演算およびレンダリングも同様である。。

  - [Adobe Premiere](https://ja.wikipedia.org/wiki/Adobe_Premiere "wikilink") Pro CS6 \[95\]

  - [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink") CC \[96\]

  - [Blender](../Page/Blender.md "wikilink") \[97\]

  - [LuxRender](https://ja.wikipedia.org/wiki/LuxRender "wikilink")

  - [V-Ray](https://ja.wikipedia.org/wiki/V-Ray "wikilink") \[98\] \[99\] \[100\] \[101\]

  - [OpenCV](../Page/OpenCV.md "wikilink") - OpenCV 2.4.3\[102\]でOpenCLを使ったアクセラレータoclモジュールが追加された。

  - [アルテラ](https://ja.wikipedia.org/wiki/アルテラ "wikilink") [オプティカルフロー](https://ja.wikipedia.org/wiki/オプティカルフロー "wikilink") - 車載[FPGA](https://ja.wikipedia.org/wiki/FPGA "wikilink")を利用した物体検知システム\[103\] \[104\]。

  - [OpenSubdiv](https://ja.wikipedia.org/wiki/OpenSubdiv "wikilink") \[105\]

  - [ImageMagick](../Page/ImageMagick.md "wikilink")

  - [FFmpeg](../Page/FFmpeg.md "wikilink") \[106\] - 一部のフィルタのみ。

  - [x264](https://ja.wikipedia.org/wiki/x264 "wikilink") \[107\] - lookahead処理にOpenCLを使うことができる。

  - [Bullet](https://ja.wikipedia.org/wiki/Bullet "wikilink") 3.x

  -
## macOSでの非推奨化

2018年6月5日、Appleは[WWDC](https://ja.wikipedia.org/wiki/WWDC "wikilink") 2018でOpenGL/OpenCLの非推奨化を発表し、[macOS Mojaveにおいて](https://ja.wikipedia.org/wiki/macOS_Mojave "wikilink")（サポートはまだ打ち切られないものの）OpenGL/OpenCLは非推奨APIとなった。macOSがネイティブにサポートするOpenCLのバージョンは1.2が最後となっている\[108\]。

OpenCLの代替として推奨されているAPIは[Metalであり](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")、[コンピュートシェーダー](https://ja.wikipedia.org/wiki/コンピュートシェーダー "wikilink")をカーネルの記述に用いる。[iOSではOpenCLはサポートされていないが](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、Metalを用いることでmacOS同様にGPGPUを実行することが可能となっている。

## 関連項目

  - [ストリーム・プロセッシング](https://ja.wikipedia.org/wiki/ストリーム・プロセッシング "wikilink")
  - [並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")
  - [高性能計算](https://ja.wikipedia.org/wiki/高性能計算 "wikilink")
  - [GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")
  - [WebCL](https://ja.wikipedia.org/wiki/WebCL "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")
  - [Cell Broadband Engine](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine "wikilink")
  - [Xeon Phi](https://ja.wikipedia.org/wiki/Xeon_Phi "wikilink")
  - [OsiriX](https://ja.wikipedia.org/wiki/OsiriX "wikilink") - [アップルコンピュータの支援のもと](../Page/アップル_\(企業\).md "wikilink")、技術公開とほぼ同時にOpenCLへ対応した[DICOM](https://ja.wikipedia.org/wiki/DICOM "wikilink")ビューア。

## 脚注

## 外部リンク

  - Khronos Group
      - [OpenCL - The open standard for parallel programming of heterogeneous systems](https://www.khronos.org/opencl/)
      - [Khronos OpenCL Registry](https://www.khronos.org/registry/cl/)
      - [Khronos SPIR Registry](https://www.khronos.org/registry/spir/)
      - [Khronos SPIR-V Registry](https://www.khronos.org/registry/spir-v/)

[Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink") [Category:GPGPUライブラリー](https://ja.wikipedia.org/wiki/Category:GPGPUライブラリー "wikilink")

1.  、2008年12月
2.  [The OpenCL\* Platform on Intel(R) Processors](https://software.intel.com/sites/landingpage/ioclsdk/2013XE/UG/The_OpenCL_Platform_on_Intel_Processors.htm)
3.  [The OpenCL Specification Version: 2.0; Document Revision: 29](http://www.khronos.org/registry/cl/specs/opencl-2.0.pdf)
4.  [Other Built-in Data Types](https://www.khronos.org/registry/cl/sdk/1.2/docs/man/xhtml/otherDataTypes.html)
5.  [Khronos OpenCL Registry](https://www.khronos.org/registry/cl/)
6.  [Accelerating GPU computation through mixed-precision methods](http://www.nvidia.com/content/PDF/sc_2010/CUDA_Tutorial/SC10_Accelerating_GPU_Computation_Through_Mixed-Precision_Methods.pdf)
7.  [OpenCL Installable Client Driver (ICD) Loader - khronos.org news](https://www.khronos.org/news/permalink/opencl-installable-client-driver-icd-loader)
8.  [アップル、Mac OS X Snow Leopardをデベロッパにプレビュー](http://www.apple.com/jp/news/2008/jun/10leopard.html)、2008年6月10日
9.  [Khronos Launches Heterogeneous Computing Initiative](http://www.khronos.org/news/press/releases/khronos_launches_heterogeneous_computing_initiative/)、2008年6月16日
10. [RapidMind Embraces Open Source and Standards Projects to Increase Focus on Simplifying Parallel Programming for Application Developers](http://www.rapidmind.net/News-Nov10-08-LLVM-OpenCL.php)、2008年11月10日
11. [The Khronos Group Releases OpenCL 1.0 Specification](https://www.khronos.org/news/press/2008/12)
12. [AMD Adopts OpenCL™ 1.0 Specification Ratified Today by The Khronos™ Group, Reaffirms Commitment to Open Standards for CPU+GPU Compute](http://www.businesswire.com/news/home/20081208006480/en)、2008年12月8日
13. [NVIDIA Adds OpenCL To Its Industry Leading GPU Computing Toolkit](http://www.nvidia.com/object/io_1228825271885.html)、2008年12月9日
14. [Khronos Drives Momentum of Parallel Computing Standard with Release of OpenCL 1.1 Specification - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-group-releases-opencl-1-1-parallel-computing-standard)
15. [clSetKernelArg](https://www.khronos.org/registry/cl/sdk/1.1/docs/man/xhtml/clSetKernelArg.html)
16. [Khronos Releases OpenCL 1.2 Specification - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-opencl-1.2-specification)
17. [write_image (3D)](https://www.khronos.org/registry/cl/sdk/1.2/docs/man/xhtml/write_image3d.html)
18. [Khronos Releases OpenCL 2.0 - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-opencl-2.0)
19. [Access Qualifiers: read_writeはCUDA SurfaceやDirectCompute RWTextureといったDirectX 11世代の機能に相当する。](https://www.khronos.org/registry/cl/sdk/2.0/docs/man/xhtml/accessQualifiers.html)
20. [Khronos Releases OpenCL 2.1 and SPIR-V 1.0 Specifications for Heterogeneous Parallel Programming - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-opencl-2.1-and-spir-v-1.0-specifications-for-heterogeneous)
21. [Khronos Releases OpenCL 2.1 Provisional Specification for Public Review - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-opencl-2.1-provisional-specification-for-public-review)
22. [Khronos Releases OpenCL 2.2 With SPIR-V 1.2 - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-opencl-2.2-with-spir-v-1.2)
23. [Khronos Releases OpenCL 2.2 Provisional Specification with OpenCL C++ Kernel Language - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-opencl-2.2-provisional-spec-opencl-c-kernel-language)
24.
25.
26. [NVIDIAのCUDAアーキテクチャGPUにおけるFortranサポート](http://www.nvidia.co.jp/object/fortran_jp.html)
27. [AMDのGPGPU戦略は新章へ - ATI Streamの展望、DirectX Compute Shaderの衝撃 (2) ATI Streamとは? | マイナビニュース](http://news.mynavi.jp/articles/2008/11/27/stream/001.html)
28. ["Close to the Metal", Justin Hensley, AMD Graphics Product Group](http://gpgpu.org/static/s2007/slides/07-CTM-overview.pdf)
29. [AMD、DirectX 11/OpenCLのGPGPUをフルサポートへ](http://pc.watch.impress.co.jp/docs/2008/0807/amd.htm)
30. [AMD Drives Adoption of Industry Standards in GPGPU Software Development](http://www.amd.com/us-en/Corporate/VirtualPressRoom/0,,51_104_543~127451,00.html)
31. [後藤弘茂のWeekly海外ニュース](http://pc.watch.impress.co.jp/docs/2009/0330/kaigai497.htm)
32. [AMDとMS，GPU演算用途向けのコンパイラ「C＋＋ AMP v1.2」を発表 - 4Gamer.net](http://www.4gamer.net/games/032/G003263/20140828031/)
33. [multicoreware / cppamp-driver-ng / wiki / Home — Bitbucket](https://bitbucket.org/multicoreware/cppamp-driver-ng/wiki/Home)
34. [Initiating an Offload on Intel® Graphics Technology](https://software.intel.com/en-us/node/512524) Intel
35. [OpenMP®/Clang](http://clang-omp.github.io/)
36. [OpenMP 4.0 Offloading For Intel MIC Lands In GCC 5](http://www.phoronix.com/scan.php?page=news_item&px=MTgzNzk) Phoronix 2014年11月13日
37. [OpenACC ディレクティブによるプログラミング by PGI Compilers](http://www.softek.co.jp/SPG/Pgi/OpenACC/)
38. [OpenACC ディレクティブによるプログラミング by PGI Compilers](http://www.softek.co.jp/SPG/Pgi/OpenACC/)
39. [OpenACC Changes Merged Today For GCC 5](http://www.phoronix.com/scan.php?page=news_item&px=GCC-5-OpenACC-Stage-3-Closing) Phoronix 2015年1月15日
40.
41. [Intel SPMD Program Compiler - Overview](https://ispc.github.io/index.html) Intel Corporation
42. [Intel SPMD Program Compiler User's Guide - Compiling For The NVIDIA Kepler GPU](https://ispc.github.io/ispc.html#compiling-for-the-nvidia-kepler-gpu) Intel Corporation
43. [Embree Overview](https://embree.github.io/) Intel Corporation
44. [PTX and SASS Assembly Debugging](http://http.developer.nvidia.com/NsightVisualStudio/3.0/Documentation/UserGuide/HTML/Content/PTX_SASS_Assembly_Debugging.htm) NVIDIA
45.
46. [Kernelet: High-Throughput GPU Kernel Executions with Dynamic Slicing and Scheduling](http://arxiv.org/pdf/1303.5164.pdf) ( arXiv:1303.5164v1 \[cs.DC\] ) Jianlong Zhong, Bingsheng He
47. [maxas - Getting Started](https://github.com/NervanaSystems/maxas/wiki/Getting-Started) Nervana Systems
48. [MaxAs](https://github.com/NervanaSystems/maxas) Nervana Systems
49. [nervanagpu/nervanagpu/kernels/sass at master · NervanaSystems/nervanagpu · GitHub](https://github.com/NervanaSystems/nervanagpu/tree/master/nervanagpu/kernels/sass) Nervana Systems
50. [NVIDIA Compute - PTX: Parallel Thread Execution](http://www.nvidia.com/content/CUDA-ptx_isa_1.4.pdf) NVIDIA
51.
52. [Inline PTX Assembly in CUDA](http://docs.nvidia.com/cuda/inline-ptx-assembly/index.html) NVIDIA
53. [NVIDIA OpenCL SDK Code Samples](http://developer.download.nvidia.com/compute/cuda/4_2/rel/sdk/website/OpenCL/html/samples.html) NVIDIA
54. [Clang 3.0 Release Notes](http://llvm.org/releases/3.0/docs/ClangReleaseNotes.html) LLVM Project
55. [User Guide for NVPTX Back-end](http://llvm.org/docs/NVPTXUsage.html) LLVM Project
56.
57. [User Guide for NVPTX Back-end - Running the Kernel](http://llvm.org/docs/NVPTXUsage.html#running-the-kernel) LLVM Project
58.
59. [AMD CAL Programming Guide](http://developer.amd.com/wordpress/media/2012/10/AMD_CAL_Programming_Guide_v2.0.pdf)
60. [Mantle Programming Guide and API Reference; Revision 1.0; March 6, 2015](http://www.amd.com/Documents/Mantle-Programming-Guide-and-API-Reference.pdf)
61. [LLVM 3.3 Release Notes](http://llvm.org/releases/3.3/docs/ReleaseNotes.html) LLVM Project
62. [A Detailed Look at the R600 Backend](http://llvm.org/devmtg/2013-11/slides/Stellard-R600.pdf) AMD
63. [Fedora Package DB - intel-gen4asm](https://admin.fedoraproject.org/pkgdb/package/intel-gen4asm/) Red Hat
64. [TGSI — Gallium 0.4 documentation](http://gallium.readthedocs.org/en/latest/tgsi.html)
65.
66. [The first open standard intermediate language for parallel compute and graphics](https://www.khronos.org/spir) Khronos Group
67.
68. [【後藤弘茂のWeekly海外ニュース】 AMD GPUとモバイルGPUで同じプログラムを走らせるHSA構想](http://pc.watch.impress.co.jp/docs/column/kaigai/20120719_547768.html)
69. [CUDA Toolkit 4.1 - archive](https://developer.nvidia.com/cuda-toolkit-41-archive)
70. [CUDA Toolkit 4.2 - archive](https://developer.nvidia.com/cuda-toolkit-42-archive)
71. CUDA Toolkit 7.0以前のバージョンに含まれるのはOpenCL 1.1対応のヘッダーとライブラリのみである。また、Fermi世代以前のハードウェアではOpenCL 1.1どまりとなる。
72. [Release 349 Graphics Drivers for Windows, Version 350.12; RN-W35012-01v01 | April 13, 2015; Windows Vista / Windows 7 / Windows 8 / Windows 8.1](http://us.download.nvidia.com/Windows/350.12/350.12-win8-win7-winvista-desktop-release-notes.pdf) KeplerおよびMaxwell世代以降のGeForceはWindows用350.12ドライバーでOpenCL 1.2に正式対応している。
73. [Release 352 Quadro, NVS, Tesla, GRID, & Notebook Drivers - Version 353.06; RN-WQ35306-01_v01 | June 1, 2015; Windows 7, Windows 8, & Windows 8.1; Release Notes](http://us.download.nvidia.com/Windows/Quadro_Certified/353.06/353.06-win8-win7-winvista-quadro-grid-release-notes.pdf) KeplerおよびMaxwell世代以降のQuadroおよびTeslaはWindows用353.06ドライバーでOpenCL 1.2に正式対応している。
74. [AMD's APP SDK 3.0 Beta with OpenCL 2.0 support](http://developer.amd.com/community/blog/2014/12/09/amd-app-sdk-3-0-beta/)
75. [AMD APP SDK v3.0 Beta Developer Release Notes](http://amd-dev.wpengine.netdna-cdn.com/wordpress/media/2013/12/AMD_APP_SDK_Release_Notes_Developer1.pdf)
76. [AMD OpenCL™ 2.0 Driver](http://support.amd.com/en-us/kb-articles/Pages/OpenCL2-Driver.aspx) AMD OpenCL 2.0ドライバーはGCN第1世代以降のAMDグラフィックス製品と互換性がある。
77. [Intel® OpenCL™ Code Builder | Intel® Developer Zone](https://software.intel.com/en-us/opencl-code-builder)
78. [OpenCL\* 2.0 の不均等なワークグループ | iSUS](http://www.isus.jp/article/visual-computing/opencl-20-non-uniform-work-groups/) Broadwell世代以降のIntel CoreシリーズはOpenCL 2.0に対応している。
79. [インテル® SDK for OpenCL Applications 2013 よくある問い合わせ | iSUS](http://www.isus.jp/article/idz/opencl-sdk-xe_faq/#q17)
80. [OpenGL および OpenCL グラフィックスを扱う Mac コンピュータ - Apple サポート](https://support.apple.com/ja-jp/HT202823)
81. [clGetProgramInfo](https://www.khronos.org/registry/cl/sdk/1.0/docs/man/xhtml/clGetProgramInfo.html)
82. [clCreateProgramWithBinary](https://www.khronos.org/registry/cl/sdk/1.0/docs/man/xhtml/clCreateProgramWithBinary.html)
83. [OpenCL meets FPGA \#1 入門編 - Qiita](http://qiita.com/iitaku/items/6c20ebb1099e595f3371)
84. [Knowledge Base - AMD](http://developer.amd.com/knowledge-base/?ID=115)
85. [クロノス・グループ、SPIR 2.0の暫定仕様を公開 - 日刊工業新聞 Business Line - 企業発表](http://www.nikkan.co.jp/newrls/rls20140815o-03.html)
86. [cl_khr_spir](https://www.khronos.org/registry/cl/sdk/2.0/docs/man/xhtml/cl_khr_spir.html)
87. [SPIR - The first open standard intermediate language for parallel compute and graphics](https://www.khronos.org/spir)
88. [Intel® VTune™ Amplifier XE: Getting started with OpenCL\* performance analysis on Intel® HD Graphics | Intel® Developer Zone](https://software.intel.com/en-us/articles/intel-vtune-amplifier-xe-getting-started-with-opencl-performance-analysis-on-intel-hd-graphics)
89. [インテル® VTune™ Amplifier XE | iSUS](http://www.isus.jp/article/intel-software-dev-products/intel-vtune-amplifier-xe/)
90. [CodeXL for game developers: How to analyze your HLSL for GCN - AMD](http://developer.amd.com/community/blog/2014/05/16/codexl-game-developers-analyze-hlsl-gcn/)
91. [NVIDIA Nsight Visual Studio Edition](https://developer.nvidia.com/nvidia-nsight-visual-studio-edition)
92. [gpgpu-sim/gpgpu-sim_distribution · GitHub](https://github.com/gpgpu-sim/gpgpu-sim_distribution)
93. [OpenCL Emu Documentation](http://amd-dev.wpengine.netdna-cdn.com/wordpress/media/2012/10/OpenCL-Emu-Documentation-2.pdf)
94.
95. [CUDA/OpenCL/Mercury Playback Engine について（Adobe Premiere Pro）](http://helpx.adobe.com/jp/premiere-pro/kb/cpsid_89467.html)
96. [Photoshop CC および CC 2014 GPU FAQ](http://helpx.adobe.com/jp/photoshop/kb/photoshop-cs6-gpu-faq1.html)
97. [Dev:2.6/Source/Render/Cycles/OpenCL - BlenderWiki](http://wiki.blender.org/index.php/Dev:2.6/Source/Render/Cycles/OpenCL)
98. [V-Ray Japanese official website - Chaos Group / Chaos Software / OakCorp.](http://v-ray.jp/rtgpu.shtml)
99. [V-Ray Japanese official website - Chaos Group / Chaos Software / OakCorp.](http://v-ray.jp/news2011.shtml)
100. [V-Ray RT and GPU rendering](http://help.chaosgroup.com/vray/help/rt100/render_gpu.htm)
101. [GPUレイトレーシング | NVIDIA](http://www.nvidia.co.jp/object/gpu-ray-tracing-jp.html)
102. [OpenCV 2.2 Released - ROS robotics news](http://www.ros.org/news/2010/12/opencv-22-released.html)
103. [アルテラ、国際カーエレクトロクス技術展（カーエレJAPAN）に出展](http://www.altera.co.jp/corporate/news_room/releases/2015/products/nr-altera-car-ele-japan-2015.html)
104. [オートモーティブワールド2015 開催直前情報：アルテラが披露するFPGAを活用した“今すぐ使える”車載向けソリューション - MONOist（モノイスト）](http://monoist.atmarkit.co.jp/mn/articles/1501/13/news030.html)
105. [PixarAnimationStudios/OpenSubdiv · GitHub](https://github.com/PixarAnimationStudios/OpenSubdiv)
106. [FFmpeg 2.0 Released With OpenCL, Many Changes](http://www.phoronix.com/scan.php?page=news_item&px=MTQwNzM) Phoronix 2013年7月10日
107. [Trying Intel OpenCL On Linux For Video Encoding](http://www.phoronix.com/scan.php?page=news_item&px=MTc3ODc) Phoronix 2014年9月2日
108.