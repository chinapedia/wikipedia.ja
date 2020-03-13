> この記事は[CUDA](https://ja.wikipedia.org/wiki/CUDA)から翻訳されています。


とは、[NVIDIA](../Page/NVIDIA.md "wikilink")が開発・提供している、[GPU向けの汎用](../Page/Graphics_Processing_Unit.md "wikilink")[並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")プラットフォーム（並列コンピューティングアーキテクチャ）およびプログラミングモデルである\[1\]\[2\]\[3\]。専用の[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")[コンパイラ](../Page/コンパイラ.md "wikilink") (nvcc) や[ライブラリ](../Page/ライブラリ.md "wikilink") ([API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")) などが提供されている。なおNVIDIA製GPUにおいては、OpenCL/DirectComputeなどの類似APIコールは、すべて共通の[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")プラットフォームであるCUDAを経由することになる\[4\]。

## 概要

[thumb|300px|right|**CUDAの処理の流れ**
<small> 1. メインメモリ（ホストメモリ）からデータをGPU用メモリ（デバイスメモリ）にコピーする。
2\. CPUがGPUに対して処理を指示する。
3\. GPUが必要なデータを取り込み各コアで並列実行する。
4\. 結果をGPU用メモリからメインメモリにコピーする。
</small>\[5\] \[6\]](https://ja.wikipedia.org/wiki/ファイル:CUDAの処理の流れ.PNG "wikilink")

もともとリアルタイムグラフィックス表示用途、特にゲームグラフィックス用途に特化したGPUを開発していたのがNVIDIAや[ATI](../Page/ATI_Technologies.md "wikilink") (現[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")) であるが、[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")の発展によるプログラマビリティの向上を受け、その高い処理性能をグラフィックス以外にも活用できるようにするためにNVIDIAが開発した技術がCUDAである。このような汎用コンピューティング向けのGPU活用技術を[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink") (General-Purpose computing on Graphics Processing Units) と呼ぶ。

GPU向けのプログラミング環境としては[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")や[GLSL](../Page/GLSL.md "wikilink")、[NVIDIA Cgを用いたものもあるが](../Page/Cg_\(プログラミング言語\).md "wikilink")、こちらは[Direct3D](../Page/Direct3D.md "wikilink")もしくは[OpenGL](../Page/OpenGL.md "wikilink")をバックエンドとするリアルタイム[CG](https://ja.wikipedia.org/wiki/CG "wikilink")描画専用のプログラミング環境となっており、[変数の](../Page/変数_\(プログラミング\).md "wikilink")[型にGPU特有の型しか使えない](../Page/データ型.md "wikilink")（特に出力として用いるテクスチャメモリのフォーマットに制約が大きい）など汎用的なプログラムの記述は困難である。CUDAでは、HLSLやGLSLと異なり、よりC言語に近い構文（ポインタなどを含む）を採用しており、またDirect3D/OpenGLといったバックエンドを使うことなくプログラムロジックを記述できるため、汎用コンピューティングに適している。

GPUはシンプルな演算ユニットを多数搭載しており、ピーク理論演算性能 ([FLOPS](../Page/FLOPS.md "wikilink")) は同一価格帯の[CPU](../Page/CPU.md "wikilink")をしのぐものもある。そのため、[並列性](https://ja.wikipedia.org/wiki/並列性 "wikilink")や演算密度の高い処理を行なう場合、少数で複雑な構成を備えた同規模の[CPU](../Page/CPU.md "wikilink")と比べて高い処理性能が出せる。 その逆に複雑な分岐処理（演算密度の低い処理）はCPUと比較して苦手であり、またGPUへ入力データを供給する、あるいはGPUによる演算結果をCPU側へリードバックするには接続バス ([PCI-Express](https://ja.wikipedia.org/wiki/PCI-Express "wikilink")) を通してデータを転送する必要があり、これがボトルネックとなりうる可能性もあるため、適用分野や問題を解くアルゴリズムを慎重に選ぶ必要がある\[7\]。

また、CUDAで作成したプログラムを最大限最適化するためには、Warpや共有メモリなどのNVIDIA GPUデバイスアーキテクチャに関する深い知識も必要となる\[8\]。

なお、CUDAの発表は2006年11月\[9\]、CUDA 1.0の提供開始は2007年7月\[10\]であり、後発の[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")関連技術には[OpenCL](../Page/OpenCL.md "wikilink") (1.0仕様公開は2008年\[11\]) や[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink") ([DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")コンピュートシェーダー。[Windows 7](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")/[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 11.0と同時に2009年に一般提供開始\[12\]) などが存在するが、それぞれ技術用語は異なるものの全体としてはCUDAに非常に似通った特徴を持つ。先発技術であるCUDAは、2014年時点で教育・研究機関での採用事例が多い\[13\]ほか、機械学習などの分野で産業界でも採用への取り組みが進んでいる\[14\]。

## 対応言語

CUDA C は[C言語](../Page/C言語.md "wikilink")と[C++](../Page/C++.md "wikilink")の一部の構文のみ対応。C言語を拡張している。CUDA C/C++のソースコードの拡張子には通例.cuが使われ、ヘッダーの拡張子には.cuhが使われる\[15\]。[BLAS](https://ja.wikipedia.org/wiki/BLAS "wikilink")[インターフェイス](https://ja.wikipedia.org/wiki/インターフェイス "wikilink")経由で[ベクトル](../Page/ベクトル.md "wikilink")・[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算が可能（cuBLAS\[16\]）。[FFTライブラリ](../Page/高速フーリエ変換.md "wikilink")（cuFFT\[17\]）も付属する。SDKとなるCUDA Toolkitには、CUDA実装によるC++向けのテンプレートベース並列アルゴリズムライブラリ「Thrust」も付属する\[18\]。

なおCUDAバージョン7では、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")規格のサポートが強化され、デバイスコードにおける[ラムダ式](https://ja.wikipedia.org/wiki/ラムダ式 "wikilink")の利用などが可能となっている\[19\] \[20\]。 CUDAバージョン8では、[機械学習](../Page/機械学習.md "wikilink")向けのライブラリが強化され、Pascalアーキテクチャの固有機能を利用した拡張が多数追加された\[21\]\[22\]。

CUDA [Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink") は [The Portland Group](https://ja.wikipedia.org/wiki/The_Portland_Group "wikilink") (PGI) から提供されている\[23\]。[Fortran 2003](https://ja.wikipedia.org/wiki/FORTRAN#Fortran_2003 "wikilink") を拡張している\[24\]。

NVIDIAのCUDAコンパイラ*nvcc*自体は[LLVM](../Page/LLVM.md "wikilink")ベースであり、新しいプログラミング言語や新しいプロセッサのサポートを追加するコンパイラSDKも提供されている\[25\]。

### 言語バインディング

C言語以外からCUDAを呼べるようにしたバインディングがある。

  - [Python](../Page/Python.md "wikilink") - [PyCUDA](http://mathema.tician.de/software/pycuda)
  - [Perl](../Page/Perl.md "wikilink") - [KappaCUDA](http://psilambda.com/download/kappa-for-perl)、[CUDA::Minimal](https://github.com/run4flat/perl-CUDA-Minimal)
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") - [Hoopoe jCUDA](http://www.hoopoe-cloud.com/Solutions/jCUDA/Default.aspx)、[JCuda.org](http://www.jcuda.org/jcuda/JCuda.html)、[JCublas](http://www.jcuda.org/jcuda/jcublas/JCublas.html)、[JCufft](http://www.jcuda.org/jcuda/jcufft/JCufft.html)
  - [.NET](https://ja.wikipedia.org/wiki/.NET "wikilink") - [Hoopoe CUDA.NET](http://www.hoopoe-cloud.com/Solutions/CUDA.NET/Default.aspx)

他にも、[Ruby](../Page/Ruby.md "wikilink"), [Lua](../Page/Lua.md "wikilink"), [MATLAB](../Page/MATLAB.md "wikilink"), [IDL](https://ja.wikipedia.org/wiki/Interactive_Data_Language "wikilink"), [Mathematica](../Page/Mathematica.md "wikilink") などもある。

## OpenGL/Direct3D相互運用

CUDAにはOpenGLおよびDirect3D 9/10/11との連携を可能にする相互運用APIが用意されている。詳しくは [CUDA Runtime API :: CUDA Toolkit Documentation - 3.10. OpenGL Interoperability](http://docs.nvidia.com/cuda/cuda-runtime-api/group__CUDART__OPENGL.html#group__CUDART__OPENGL), [CUDA Runtime API :: CUDA Toolkit Documentation - 3.16. Direct3D 11 Interoperability](http://docs.nvidia.com/cuda/cuda-runtime-api/group__CUDART__D3D11.html#group__CUDART__D3D11) などを参照のこと。

## 開発ツール

CUDA Toolkitには*Visual Profiler*と呼ばれるパフォーマンス計測ツールが付属し、アプリケーションにおけるGPUの処理時間などの情報を収集して、性能改善に役立てることができる\[26\]。CUDA Toolkit 7.5では命令レベルでのプロファイリングがサポートされた\[27\]。*Nsight* (旧称Parallel Nsight) と呼ばれる統合開発環境向けのアドインも提供されている。

## メリット・デメリット

ここでは従来のCPUベースのプログラミングとの比較ではなく、類似の[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")関連技術とCUDAとの比較を行なう。

### メリット

CUDAはNVIDIAが独自に開発を進めている[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")技術であり、NVIDIA製のハードウェア性能を最大限引き出せるように設計されている\[28\]。CUDAを利用することで、NVIDIA製GPUに新しく実装されたハードウェア機能をいち早く活用することができる。例えばKepler世代以降のGPUで使用可能なWarpシャッフル命令を使用することで、共有メモリを介するよりもさらに高速な並列リダクションを実行することができる\[29\] \[30\]。CUDA同様の類似GPGPU技術として代表的なものは[OpenCL](../Page/OpenCL.md "wikilink")や[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")が挙げられるが、いずれもハードウェアアーキテクチャを標準化しベンダーの違いを吸収する[API層であるため](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、CUDAと比較すると抽象化の度合いは低いローレベルAPIではあるものの、ハードウェア特有の先進的機能を使った細やかなチューニングによりそのハードウェアの限界性能を引き出すのは難しい\[31\]。

また、OpenCLやDirectComputeでは、カーネルと呼ばれるデバイス用並列処理プログラムコード片（並列実行の最小単位）を専用のOpenCL-Cや[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")といった言語で記述した上で、OpenCL APIや[Direct3D](../Page/Direct3D.md "wikilink") APIを使用してカーネルを発行する必要があるため、準備のための手間が必要となるが、CUDAの場合はより抽象化されており、カーネルコードの発行をC/C++における通常の関数呼び出しに近い形で記述できるなど、より本質的なアプリケーションコードやアルゴリズムの実装のみに注力できるようになっている。

### デメリット

ハードウェアベンダーに依存しないOpenCLやDirectComputeと比較すると、CUDAはNVIDIA製のGPUでしか使えないという制約がある。このため、CUDAの機能に過度に依存したプログラムを書くと、アプリケーションの[ポーティング・移植が困難になる可能性がある](../Page/移植_\(ソフトウェア\).md "wikilink")（[ベンダーロックイン](../Page/ベンダーロックイン.md "wikilink")）\[32\]。AMDはCUDAアプリケーションをAMDおよび他のGPUプラットフォーム向けにソースコードレベルで移植しやすくするためのC++用APIとして、HIP (Heterogeneous-Compute Interface for Portability) の提供を開始した\[33\]\[34\]が、CUDAと完全な互換性を持っているわけではない。

また、最初からグラフィックス連携用途を想定して設計されたDirectComputeと比較すると、（相互運用APIが用意されているとはいえ）GPU演算結果をグラフィックス用途に直接利用する場合はオーバーヘッドが大きくなる\[35\]。

## 対応環境

### ハードウェア

[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 10世代の統合型シェーダーアーキテクチャを採用した[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink") 8シリーズ以上 (ネットブック/トップ用の[NVIDIA IONを含む](https://ja.wikipedia.org/wiki/NVIDIA_ION "wikilink")) もしくは [NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink") や [NVIDIA Quadro](../Page/NVIDIA_Quadro.md "wikilink") (Teslaはハイパフォーマンスコンピューティング用、Quadroはワークステーション用) 。モバイル向けの統合型プロセッサでは、Keplerアーキテクチャを採用している[NVIDIA Tegra](https://ja.wikipedia.org/wiki/NVIDIA_Tegra "wikilink") K1以降となる。実行には専用の[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を必要とする。詳細は、 [CUDA GPUs | NVIDIA Developer Zone](https://developer.nvidia.com/cuda-gpus) を参照。なお、ハードウェアの世代／アーキテクチャ（Compute Capability, CC）によって利用可能なGPU命令やリソースサイズ上限、[倍精度浮動小数点](https://ja.wikipedia.org/wiki/倍精度浮動小数点 "wikilink")対応可否などの制約が異なる。また、上位のCCを持つハードウェアでは、下位のCC向けにコンパイルされたCUDAコードを実行できるが、その逆は不可能となっている。

#### PTX (Parallel Thread Execution)

CUDAは実行環境デバイスの世代（Compute Capability）に応じた専用バイナリコードを生成できるほかに、PTX ([Parallel Thread Execution](https://ja.wikipedia.org/wiki/Parallel_Thread_Execution "wikilink")) と呼ばれるNVIDIA独自のGPU中間命令（[中間言語](../Page/中間言語.md "wikilink")）を生成することができる。PTXを利用することで、実行時にCUDAドライバーによって実行環境に合わせた最適なコードを生成することができるようになる\[36\]。

### OS

CUDA Toolkit 6.5の対応[OSは](../Page/オペレーティングシステム.md "wikilink")、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") (32bit版のみ)、[Windows 7](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")、[Windows 8.1](https://ja.wikipedia.org/wiki/Windows_8.1 "wikilink")、[Windows Server 2008 R2](https://ja.wikipedia.org/wiki/Windows_Server_2008_R2 "wikilink")、[Windows Server 2012 R2](https://ja.wikipedia.org/wiki/Windows_Server_2012_R2 "wikilink")、[Fedora](../Page/Fedora.md "wikilink") 20、[OpenSUSE](https://ja.wikipedia.org/wiki/OpenSUSE "wikilink") 13.1、RHEL ([Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink")) 5/6、[CentOS](../Page/CentOS.md "wikilink") 5/6、SLES ([SUSE Linux](https://ja.wikipedia.org/wiki/SUSE_Linux "wikilink") Enterprise Server) 11-SP3、[Ubuntu](../Page/Ubuntu.md "wikilink") 12.04/14.04、[Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") 10.8/10.9/10.10である\[37\]。

CUDA Toolkit 7.0の対応OSは、Windows 7、Windows 8.1、Windows Server 2008 R2、Windows Server 2012 R2、Fedora 21、OpenSUSE 13.1/13.2、RHEL 6/7、CentOS 6/7、SLES 11/12、Ubuntu 12.04/14.04/14.10、[OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") 10.9/10.10である\[38\]。

CUDA Toolkit 7.5の対応OSは、Windows 7、Windows 8.1、[Windows 10](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")、Windows Server 2008 R2、Windows Server 2012 R2、Fedora 21、OpenSUSE 13.2、RHEL 6/7、CentOS 6/7、SLES 11/12、[SteamOS](https://ja.wikipedia.org/wiki/SteamOS "wikilink") 1.0-beta、Ubuntu 14.04/15.04、OS X 10.9/10.10/10.11である\[39\]。

CUDA Toolkit 8.0 GA2の対応OSは、Windows 7、Windows 8.1、Windows 10、Windows Server 2008 R2、Windows Server 2012 R2、[Windows Server 2016](https://ja.wikipedia.org/wiki/Windows_Server_2016 "wikilink")、Fedora 23、OpenSUSE 13.2、RHEL 6/7、CentOS 6/7、SLES 11/12、Ubuntu 14.04/16.04、OS X 10.11/10.12である\[40\]。

CUDA Toolkit 9.2の対応OSは、Windows 7、Windows 8.1、Windows 10、Windows Server 2012 R2、Windows Server 2016、Fedora 27、OpenSUSE 42.3、RHEL 6/7、CentOS 6/7、SLES 12、Ubuntu 16.04/17.10、OS X 10.13である\[41\]。

## NVIDIA OptiX

CUDA基盤上に実装されたプログラマブルGPU[レイトレーシング](../Page/レイトレーシング.md "wikilink")エンジンとして、NVIDIAはを公開している\[42\]。OptiXはFermi世代以降のNVIDIA GPU上で利用可能。なお、[After Effects](https://ja.wikipedia.org/wiki/After_Effects "wikilink") CCではレイトレーシングエンジンにOptiXを採用している\[43\]。

## 対応ソフトウェア

CUDAの演算処理技術を利用するには、上述のハードウェア・OSのサポートに加えて、アプリケーションが対応していることが必要。一部アプリケーションベンダーより対応ソフトが出ている。

  - [Freemake Video Converter](https://ja.wikipedia.org/wiki/Freemake_Video_Converter "wikilink") ([Free Make](https://ja.wikipedia.org/wiki/Free_Make "wikilink")) (フリーソフトウェア)
  - [MediaCoder](../Page/MediaCoder.md "wikilink") ([MediaCoder](../Page/MediaCoder.md "wikilink")) (フリーソフトウェア)
  - [LoiLoTouch](https://ja.wikipedia.org/wiki/LoiLoTouch "wikilink") ([LoiLo](https://ja.wikipedia.org/wiki/LoiLo "wikilink"))
  - [Super LoiLoScope](https://ja.wikipedia.org/wiki/Super_LoiLoScope "wikilink") ([LoiLo](https://ja.wikipedia.org/wiki/LoiLo "wikilink"))
  - [PowerDirector](../Page/PowerDirector.md "wikilink") ([CyberLink](https://ja.wikipedia.org/wiki/CyberLink "wikilink"))\[44\] - 同社の[SVRT](https://ja.wikipedia.org/wiki/SVRT "wikilink")テクノロジーとは排他利用である\[45\]。

<!-- end list -->

  - [PowerDVD](../Page/PowerDVD.md "wikilink") ([CyberLink](https://ja.wikipedia.org/wiki/CyberLink "wikilink"))
  - [VideoStudio Pro X3](https://ja.wikipedia.org/wiki/VideoStudio_Pro_X3 "wikilink") ([COREL](https://ja.wikipedia.org/wiki/COREL "wikilink"))
  - [VideoStudio Ultimate X3](https://ja.wikipedia.org/wiki/VideoStudio_Ultimate_X3 "wikilink") ([COREL](https://ja.wikipedia.org/wiki/COREL "wikilink"))
  - [TMPGEnc](../Page/TMPGEnc.md "wikilink") (ペガシス)
  - [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink") CS4 ([Adobe](https://ja.wikipedia.org/wiki/Adobe "wikilink")) \[46\]
  - [Adobe After Effects](../Page/Adobe_After_Effects.md "wikilink") CS4 ([Adobe](https://ja.wikipedia.org/wiki/Adobe "wikilink"))
  - [Adobe Premiere](../Page/Adobe_Premiere.md "wikilink") Pro CS4 ([Adobe](https://ja.wikipedia.org/wiki/Adobe "wikilink")) \[47\]\[48\]
  - [Blender](../Page/Blender.md "wikilink") ([GPL](https://ja.wikipedia.org/wiki/GPL "wikilink")ライセンスのフリーソフトウェア) \[49\]
  - [Vegas Pro](https://ja.wikipedia.org/wiki/Vegas_Pro "wikilink") 10 ([Sony Creative Software](https://ja.wikipedia.org/wiki/Sony_Creative_Software "wikilink"))
  - [パスゲッター](https://ja.wikipedia.org/wiki/パスゲッター "wikilink") ([インターナル](https://ja.wikipedia.org/wiki/インターナル "wikilink"))
  - [Any Video Converter](https://ja.wikipedia.org/wiki/Any_Video_Converter "wikilink") (フリーソフトウェア・シェアソフトウェア)

### 分散コンピューティング

これらは[BOINCクライアント上でCUDAを利用する](../Page/Berkeley_Open_Infrastructure_for_Network_Computing.md "wikilink")。

  - [SETI@Home](https://ja.wikipedia.org/wiki/SETI@Home "wikilink")
  - [MilkyWay@home](https://ja.wikipedia.org/wiki/MilkyWay@home "wikilink")
  - [GPUGRID](https://ja.wikipedia.org/wiki/GPUGRID "wikilink") (PS3GRID)
  - [AQUA@home](https://ja.wikipedia.org/wiki/AQUA@home "wikilink")
  - [Folding@Home](https://ja.wikipedia.org/wiki/Folding@Home "wikilink")（このプロジェクトのみ、オリジナルのクライアントで動作）

### MATLAB

[MATLAB](../Page/MATLAB.md "wikilink")とのコラボレーションもサポートされている。MATLABではParallel Computing Toolboxを介してGPUを使用できる\[50\]。重いプログラムスクリプト実行の高速化に寄与する。ただしCUDAの初期化およびメインメモリ-[VRAM](../Page/VRAM.md "wikilink")間のデータ転送に時間がかかるため、短いスクリプトの場合は逆にトータル処理時間でみるとCPUだけ使用するときよりも遅くなる場合もある。[Intel Xeon](https://ja.wikipedia.org/wiki/Intel_Xeon "wikilink") X5650を使った場合と比べて、[NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink") C2050を使うことで[FFTが最大](../Page/高速フーリエ変換.md "wikilink")3.5倍高速化されたとの説明がある\[51\]。

### OpenCV

[OpenCV](../Page/OpenCV.md "wikilink") 2.2\[52\]でCUDAを使ったアクセラレータであるgpuモジュールが追加された。OpenCV 3.0ではcudaモジュールに改称された。

## 出典

<references/>

## 関連項目

  - [NVIDIA](../Page/NVIDIA.md "wikilink")
  - [NVIDIA Tesla](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink")
  - [NVIDIA Quadro](../Page/NVIDIA_Quadro.md "wikilink")
  - [NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink")
  - [ハイパフォーマンスコンピューティング](https://ja.wikipedia.org/wiki/ハイパフォーマンスコンピューティング "wikilink")
  - [コンパイラ](../Page/コンパイラ.md "wikilink")
  - [GPU](../Page/Graphics_Processing_Unit.md "wikilink")
  - [GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")
  - [OpenCL](../Page/OpenCL.md "wikilink")
  - [DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")
  - [Metal (API)](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")
  - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")
  - [AMD Stream](https://ja.wikipedia.org/wiki/AMD_Stream "wikilink") (旧[ATI Stream](https://ja.wikipedia.org/wiki/ATI_Stream "wikilink")) - [AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") (旧[ATI社](../Page/ATI_Technologies.md "wikilink")) の[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink")、[FirePro](https://ja.wikipedia.org/wiki/FirePro "wikilink")、[FireStream](https://ja.wikipedia.org/wiki/FireStream "wikilink")を使用したGPGPUの競合テクノロジー

## 関連書籍

  -
  -
  -
  -
## 外部リンク

  - [CUDA Zone | NVIDIA Developer](https://developer.nvidia.com/cuda-zone)

[Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink") [Category:GPGPUライブラリー](https://ja.wikipedia.org/wiki/Category:GPGPUライブラリー "wikilink") [Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:NVIDIA](https://ja.wikipedia.org/wiki/Category:NVIDIA "wikilink")

1.  [What Is CUDA | NVIDIA Official Blog](https://blogs.nvidia.com/blog/2012/09/10/what-is-cuda-2/)
2.  [Accelerated Computing | NVIDIA Developer](https://developer.nvidia.com/hpc)
3.  [開発者向けのCUDA並列コンピューティングプラットフォーム | NVIDIA](http://www.nvidia.co.jp/object/cuda-parallel-computing-platform-jp.html)
4.  [第3回 CUDAとGPUコンピューティングの広がり | Think IT](https://thinkit.co.jp/story/2010/07/30/1678)
5.  日経エレクトロニクス 2007/10/8 「プロセサはマルチ×マルチへ」
6.  [第７回　CUDAプログラミングモデル② | G-DEP:](http://www.gdep.jp/page/view/254)
7.  [HPCシンポジウムで見えたTSUBAME2.0の設計思想 (1) ポストペタスケールへ向けGPUをどう活用していくのか](http://news.mynavi.jp/articles/2011/02/22/hpcsympo2011_tsubame2/)
8.  [第６回　CUDAプログラミングモデル① | G-DEP](http://www.gdep.jp/page/view/253)
9.  [Press Release | NVIDIA](http://www.nvidia.com/object/IO_37226.html)
10. [NVIDIA CUDA 1.0、GPUコンピューティング向けに機能を強化 | NVIDIA](http://www.nvidia.co.jp/object/IO_44226.html)
11. [並列プログラミング規格「OpenCL 1.0」が標準として批准 － ＠IT](http://www.atmarkit.co.jp/news/200812/10/opencl.html)
12. [西川善司の3Dゲームファンのためのグラフィックス講座。台頭するDirectCompute技術 - GAME Watch](http://game.watch.impress.co.jp/docs/series/3dcg/20110301_430375.html)
13. [NVIDIA GPUコンピューティング応用事例のご紹介](http://www.nec.co.jp/seminar/110929hpc/images/NVIDIA.pdf)
14. [【GTC2014】NVIDIA、基調講演でCUDAを自動車にもたらす開発キット「JETSON TK1」の提供開始など発表 / NVLink、3Dメモリで、帯域幅問題を解消する新GPU「Pascal（パスカル）」も計画 - Car Watch](http://car.watch.impress.co.jp/docs/news/20140326_641290.html)
15. [第４回　実際にCUDAを使ってみる | G-DEP](http://www.gdep.jp/page/view/251)
16. [cuBLAS - NVIDIA CUDA ZONE](https://developer.nvidia.com/cuBLAS)
17. [cuFFT - NVIDIA CUDA ZONE](https://developer.nvidia.com/cufft)
18. [Thrust - NVIDIA CUDA ZONE](https://developer.nvidia.com/Thrust)
19. [NVIDIA Pushes CUDA 7 RC With C++11 Features, Runtime Compilation - Phoronix](http://www.phoronix.com/scan.php?page=news_item&px=NVIDIA-CUDA-7-Features)
20. [The Power of C++11 Programming in CUDA 7 | Parallel Forall](http://devblogs.nvidia.com/parallelforall/power-cpp11-cuda-7/)
21. [CUDA 8 PERFORMANCE OVERVIEW - November 2016, NVIDIA](http://developer.download.nvidia.com/compute/cuda/compute-docs/cuda-performance-report.pdf)
22. [CUDA 8.0 新機能のご紹介 - GTC Japan 2016](https://www.gputechconf.jp/assets/files/1010.pdf)
23. [NVIDIAのCUDAアーキテクチャGPUにおけるFortranサポート](http://www.nvidia.co.jp/object/fortran_jp.html)
24. [PGI CUDA Fortran のコンパイル・オプション](http://www.softek.co.jp/SPG/Pgi/TIPS/opt_cudaF.html)
25. [CUDA LLVM Compiler | NVIDIA Developer](https://developer.nvidia.com/cuda-llvm-compiler)
26. [第3回 CUDAとGPUコンピューティングの広がり | Think IT（シンクイット）](http://thinkit.co.jp/story/2010/07/30/1678/page/0/1)
27. [CUDA 7.5: Pinpoint Performance Problems with Instruction-Level Profiling | Parallel Forall](http://devblogs.nvidia.com/parallelforall/cuda-7-5-pinpoint-performance-problems-instruction-level-profiling/)
28. [コンパイラ、そしてもっと：アクセラレーター・プログラミング](http://www.hpcwire.jp/archives/3214)
29. [Faster Parallel Reductions on Kepler | Parallel Forall](http://devblogs.nvidia.com/parallelforall/faster-parallel-reductions-kepler/)
30. [Kepler GPUアーキテクチャとプログラム最適化 (10) Keplerから搭載されたレジスタ内のデータの入れ替え命令 | マイナビニュース](http://news.mynavi.jp/series/kepler_gpu/010/)
31. [第3回 CUDAとGPUコンピューティングの広がり | Think IT](http://thinkit.co.jp/story/2010/07/30/1678/page/0/1)
32. [ASCII.jp：OpenCLでCUDAを追撃\!?　AMD「ATI Stream」が狙うものは](http://ascii.jp/elem/000/000/197/197866/)
33. [AMDがSC15にて、「Boltzmann Initiative」を発表 – AMD GPU用C++とCUDAコンパイラー - 株式会社エーキューブ](http://acube-corp.com/whats-new/press-release/boltzmanninitiative)
34. [HIP : C++ Heterogeneous-Compute Interface for Portability - GPUOpen](http://gpuopen.com/compute-product/hip-convert-cuda-to-portable-c-code/)
35. [SIGGRAPH ASIA 2009 - 非プラットフォーム依存パラレルの本命、「OpenCL」最新事情 (6) OpenCLはCUDAやDirectComputeと競合するのか | マイナビニュース](http://news.mynavi.jp/articles/2009/12/25/siggraph02/005.html)
36. ["GeForceの父" David Kirk博士、東大で並列コンピューティングについて講演 (4) CUDAの動作の仕組み | マイナビニュース](http://news.mynavi.jp/articles/2007/09/13/nvidia/003.html)
37. [CUDA Toolkit 6.5](https://developer.nvidia.com/cuda-toolkit-65)
38. [CUDA 7.0 Downloads | NVIDIA Developer](https://developer.nvidia.com/cuda-toolkit-70)
39. [CUDA 7.5 Downloads Archive | NVIDIA Developer](https://developer.nvidia.com/cuda-75-downloads-archive)
40. [CUDA Toolkit 8.0 - Feb 2017 | NVIDIA Developer](https://developer.nvidia.com/cuda-80-ga2-download-archive)
41. [CUDA Toolkit 9.2 Download | NVIDIA Developer](https://developer.nvidia.com/cuda-92-download-archive)
42. [NVIDIA® OptiX™ Ray Tracing Engine](https://developer.nvidia.com/optix)
43. [GPU changes (for CUDA and OpenGL) in After Effects CC (12.1) | After Effects region of interest](http://blogs.adobe.com/aftereffects/2013/09/gpu-changes-for-cuda-and-opengl-in-after-effects-cc-12-1.html)
44. [PowerDirector 7|NVIDIA](http://www.nvidia.co.jp/object/applications_powerdirector7_jp.html)
45. [CyberLink カスタマーサポート](http://support.jp.cyberlink.com/showdoc.asp?f=/common/pdr.7/faq/0001)
46. [4Gamer.net ― NVIDIA製GPUが「Photoshop」「After Effects」「Premiere Pro」の最新版「CS4」アクセラレーションをサポート。ムービーでその効果をチェック](http://www.4gamer.net/games/032/G003263/20080925009/)
47. Premiere Pro CCでは、2基の[NVIDIA Quadro](../Page/NVIDIA_Quadro.md "wikilink") M6000上でCUDAを活用することで、1基の[Intel Xeon](https://ja.wikipedia.org/wiki/Intel_Xeon "wikilink") E5-2697 v3を用いる場合と比較して、最大で24倍の速度性能向上を提供できるとしている。[Adobe Premiere Pro CC – さらにスピーディーなビデオ編集 | NVIDIA](http://www.nvidia.co.jp/object/adobe-premiere-pro-cc-jp.html)
48. ただし、CUDAによって必ずしも処理が高速化するわけではない。[CUDA/OpenCL/Mercury Playback Engine について（Adobe Premiere Pro）](https://helpx.adobe.com/jp/premiere-pro/kb/cpsid_89467.html)
49. [Doc:JA/2.6/Manual/Render/Cycles/GPU Rendering - BlenderWiki](http://wiki.blender.org/index.php/Doc:JA/2.6/Manual/Render/Cycles/GPU_Rendering)
50. [NVIDIA CUDA に対応した GPU に対する MATLAB GPU 演算のサポート - MATLAB & Simulink](https://jp.mathworks.com/discovery/matlab-gpu.html)
51. [Using GPUs in MATLAB » Loren on the Art of MATLAB](https://blogs.mathworks.com/loren/2012/02/06/using-gpus-in-matlab/)
52. [OpenCV 2.2 Released - ROS robotics news](http://www.ros.org/news/2010/12/opencv-22-released.html)