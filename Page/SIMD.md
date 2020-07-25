> この記事は[SIMD](https://ja.wikipedia.org/wiki/SIMD)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:SIMD.svg "wikilink") （シングルインストラクション・マルチプルデータ、**SIMD**\[1\]）とはコンピューターの演算処理に関する[フリンの分類](../Page/フリンの分類.md "wikilink")のひとつで、1つの命令を同時に複数のデータに適用する[並列化の形態を指す](../Page/並列計算.md "wikilink")\[2\]。この手法にもとづく演算を**ベクトル演算** () と呼ぶこともある。通例、SIMD命令により同時処理するのに適したデータ構造あるいはデータ型を利用するため、命令実行の前に処理対象のデータ列はいったん結合（パック）され、処理完了後に分解（アンパック）される。結合されたデータは（パックデータ、パックトデータ）と呼ばれる。

## 解説

同一の演算を繰り返すような操作を[スカラー計算機](https://ja.wikipedia.org/wiki/スカラー計算機 "wikilink")のように逐次的に行なうのではなく、一度に行なうものである。

例えば、4次元ベクトル同士の加算を実行する場合、X, Y, Z, Wの成分ごとに加算処理を行なう。

\[\left\{
\begin{array}{l}
c_x \leftarrow a_x + b_x
\\
c_y \leftarrow a_y + b_y
\\
c_z \leftarrow a_z + b_z
\\
c_w \leftarrow a_w + b_w
\end{array}
\right.\]

ここで、それぞれの成分を32ビットの[単精度浮動小数点数](../Page/単精度浮動小数点数.md "wikilink")で表すとする。[32ビット](../Page/32ビット.md "wikilink")のレジスタ幅を持ち、1命令で32ビットのデータを1組だけ処理できる[プロセッサ](../Page/プロセッサ.md "wikilink")の場合、成分ごとの加算処理すなわち4回の加算命令を逐次実行する必要がある。一方、[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")のレジスタ幅を持ち、1命令で32ビットのデータ4組を同時に処理できるSIMD命令セットをサポートするプロセッサの場合、1回の命令で全成分をまとめて演算することができ、処理にかかる理論上の消費サイクル数は1/4になる。多くの場合、128ビットを使い切るデータはあまりなく、一般に128ビットを2分割し[64ビット](../Page/64ビット.md "wikilink")×2として使ったり、4分割し32ビット×4として使ったり、8分割し16ビット×8として使ったり、16分割し8ビット×16として使ったりするが、結局それぞれ1回のサイクルで2倍、4倍、8倍、16倍の[データ処理](../Page/データ処理.md "wikilink")が可能になり、結果として相対的に低いクロック周波数でも高い性能を引き出しやすい。

例えば音声データ全体の音量を倍にしたいとする。[デジタル](../Page/デジタル.md "wikilink")データではある瞬間の音量が数値として記録されているので、全ての値を倍にすればよい。このように大量のデータに同じ処理を施すときに性能を発揮するため、一般には[マルチメディア](../Page/マルチメディア.md "wikilink")の処理に向いているとされる。

SIMD型で、複数の[演算装置](../Page/演算装置.md "wikilink")を並列に使用する計算を初期に試みたコンピュータとしては、[ILLIAC IVがある](../Page/ILLIAC_IV.md "wikilink")。これに対し、[Cray-1](../Page/Cray-1.md "wikilink")のような典型的な[ベクトル型](../Page/ベクトル計算機.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")では並列に計算するのではなく、[パイプライン処理](../Page/パイプライン処理.md "wikilink")により1個の演算装置を休ませることなく計算させ続ける。ただしベクトル演算という用語は、広義には1命令で複数の要素を計算させるものについて、同時（並列）に計算するものも、パイプラインで計算するものも指すが、ベクトル計算機と言った場合は主として、20世紀のスーパーコンピュータに多く採用されていたパイプライン型を指すことが多い。

他の技術と同じく[1990年代](../Page/1990年代.md "wikilink")後半から[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")の[CPU](../Page/CPU.md "wikilink")/[GPU](../Page/Graphics_Processing_Unit.md "wikilink")、[ゲーム機](../Page/ゲーム機.md "wikilink")等にも応用された。

なお、SIMD命令を使ったとしても、プロセッサの命令実装形態によっては演算性能が向上しないケースもある。例えば256ビットSIMD命令に対応したプロセッサであっても、256ビット幅の命令を1サイクルで実行できるとは限らず、128ビットの演算器を使って2サイクルで実行する実装になっていることもある。

全ての処理をSIMDで行なえないこともないが、32ビット幅で十分な整数スカラー演算や論理演算の場合、本数の多い従来の汎用レジスタを有効利用するため、SIMDユニットは使わず通常の[ALUを使うことが多い](https://ja.wikipedia.org/wiki/演算装置#ALU "wikilink")。また、[コンペア・アンド・スワップ](../Page/コンペア・アンド・スワップ.md "wikilink")のような特殊命令は汎用レジスタとメモリの間でデータ交換をするため、SIMDレジスタは使えない。このような演算内容やプロセッサに合わせた最適化を[コンパイラ](../Page/コンパイラ.md "wikilink")が行なってくれることも多い。

## 例

### マイクロプロセッサ

#### 命令拡張

  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")の[MMX](../Page/MMX.md "wikilink")・[3DNow\!](../Page/3DNow!.md "wikilink")・[ストリーミングSIMD拡張命令](../Page/ストリーミングSIMD拡張命令.md "wikilink") (SSE)
  - [x64](https://ja.wikipedia.org/wiki/x64 "wikilink")の[AVX](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#Intel_AVX "wikilink")
  - [PowerPC](../Page/PowerPC.md "wikilink")の[AltiVec](../Page/AltiVec.md "wikilink") (VMX)
  - [ARMのNEONなど](../Page/ARMアーキテクチャ.md "wikilink")（[ARMアーキテクチャ\#SIMD](https://ja.wikipedia.org/wiki/ARMアーキテクチャ#SIMD "wikilink")）
  - [SPARC](../Page/SPARC.md "wikilink")のVIS ([:en:Visual Instruction Set](https://ja.wikipedia.org/wiki/:en:Visual_Instruction_Set "wikilink"))
  - [MIPSのMIPS](../Page/MIPSアーキテクチャ.md "wikilink")-3D ([:en:MIPS-3D](https://ja.wikipedia.org/wiki/:en:MIPS-3D "wikilink"))・MDMX ([:en:MDMX](https://ja.wikipedia.org/wiki/:en:MDMX "wikilink"))
  - [PA-RISC](../Page/PA-RISC.md "wikilink")の MAX ([:en:Multimedia Acceleration eXtensions](https://ja.wikipedia.org/wiki/:en:Multimedia_Acceleration_eXtensions "wikilink"))
  - [Emotion EngineのCPUコア](../Page/Emotion_Engine.md "wikilink")

#### 演算装置

演算装置自体がSIMD型のもの

  - [Cell Broadband Engine\#Synergistic Processor Element](https://ja.wikipedia.org/wiki/Cell_Broadband_Engine#Synergistic_Processor_Element "wikilink")

### GPU

[GPUはSIMD型がほとんどである](../Page/Graphics_Processing_Unit.md "wikilink")。ただし、[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")対応が進むにつれて、1プロセッサで複数のデータを扱うSIMDだけではなく、複数のプロセッサを用いて実現されるハードウェアマルチ[スレッドに対して同一の命令を発行することで複数のデータを同時に処理する](../Page/スレッド_\(コンピュータ\).md "wikilink")の併用が主流となっている。

もともとGPUはXYZW/RGBA（各成分は32ビット[単精度浮動小数点数](../Page/単精度浮動小数点数.md "wikilink")）を同時に演算する128ビットの4-way SIMDが主流だったが、1サイクルで1回の単精度浮動小数点数もしくは32ビット整数の融合[積和演算](../Page/積和演算.md "wikilink") (FMA) を行なうスカラー型プロセッサを複数束ねるSIMTが主流となった。しかしその後、単精度演算器にて半精度浮動小数点数演算を2回行なう2-way SIMDや、8ビット整数演算を4回行なう4-way SIMDをサポートするGPUも出現し、SIMDとSIMTの併用が始まっている\[3\]。

  - [NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink")、[NVIDIA Quadro](../Page/NVIDIA_Quadro.md "wikilink")、[NVIDIA Teslaシリーズなど](https://ja.wikipedia.org/wiki/NVIDIA_Tesla "wikilink")

<!-- end list -->

  -
    [NVIDIA](../Page/NVIDIA.md "wikilink")製GPUでは32個のハードウェアスレッド集合を*Warp*と呼ぶ。

<!-- end list -->

  - [AMD Radeon](../Page/AMD_Radeon.md "wikilink")、[AMD FireProシリーズなど](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink")

<!-- end list -->

  -
    [AMD製GPUでは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")64個のハードウェアスレッド集合を*Wavefront*と呼ぶ。

### 物理演算プロセッサ

3Dゲームに必要な物理演算を高速化するため、SIMDを利用。

  - [PhysX](../Page/PhysX.md "wikilink")（用のチップ）

### 汎用アクセラレータ

[PCI Express接続の汎用SIMDアクセラレータ](../Page/PCI_Express.md "wikilink")。[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")の[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算を高速に行う目的で、[ワークステーション](../Page/ワークステーション.md "wikilink")、[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")などに搭載される。

  - CSX600 - [クリアスピードによるメニーコアSIMD演算ユニット](https://ja.wikipedia.org/wiki/クリアスピード・テクノロジー "wikilink")

## コンパイラサポート

SIMD命令を利用するには、各プロセッサの固有命令を[アセンブラで直接記述するほか](../Page/アセンブリ言語.md "wikilink")、高水準言語の[コンパイラ](../Page/コンパイラ.md "wikilink")に実装されている (intrinsics/intrinsic functions) を利用する方法もある。通例[C言語](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")コンパイラには各プロセッサ固有の組み込み関数を定義したヘッダーファイルが用意されており、組み込み関数を呼び出すことで、アセンブラを使用することなく対応するSIMD命令を利用したソースコードを記述することができる。ただしSIMD命令セットおよび組み込み関数はプロセッサによって異なるため、このように手動でベクトル化するとソースコードの[移植性](../Page/移植性.md "wikilink")が低下するという問題がある。また、本来のアルゴリズムとは関係のない下位レベルのコードを記述しなければならないため、メンテナンス性も低下する。

コンパイラの中には、SIMD命令による自動ベクトル化に対応しているものもある。自動ベクトル化は[コンパイラ最適化](../Page/コンパイラ最適化.md "wikilink")の一種であり、特定のデータ型の連続したメモリ領域に対する同一の演算の繰り返しなど、特定のパターンに合致する処理を、SIMD命令を使ったベクトル演算に置き換えて高速化する\[4\]\[5\]。自動ベクトル化は手動ベクトル化と比較してきめ細やかな制御は難しく、高速化の度合いはコンパイラの解析能力に左右されるが、ソースコードの移植性やメンテナンス性を維持したまま高速化できるというメリットもある。

[OpenMP](../Page/OpenMP.md "wikilink") 4.0ではSIMDベクトル化のプラグマ指令が導入された\[6\]。

[.NET Coreおよび](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 4.6以降の64ビット版[実行時コンパイラ](../Page/実行時コンパイラ.md "wikilink") (RyuJIT) は、`System.Numerics`名前空間に含まれるSIMD対応型を使って記述された[マネージコード](../Page/マネージコード.md "wikilink")を、SIMD命令で並列化されたネイティブ機械語コードにJITコンパイルすることができる\[7\]。

## ビット演算

[ビット演算](../Page/ビット演算.md "wikilink") () の命令は、複数のビットを同時に処理することのできる並列性を持つため、広義のSIMDとして[並列計算](../Page/並列計算.md "wikilink")に利用されることもある。

## 脚注

<references/>

## 関連項目

  - [マルチプロセッシング](../Page/マルチプロセッシング.md "wikilink")
  - [ベクトル計算機](../Page/ベクトル計算機.md "wikilink")
  - [フリンの分類](../Page/フリンの分類.md "wikilink")
  - [ベクトル化](../Page/ベクトル化.md "wikilink")

[Category:SIMDコンピューティング](https://ja.wikipedia.org/wiki/Category:SIMDコンピューティング "wikilink") [Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:フリンの分類](https://ja.wikipedia.org/wiki/Category:フリンの分類 "wikilink")

1.  [英語](../Page/英語.md "wikilink")では「シムディー」のように読まれる。日本では「シムド」と呼ぶことがある。
2.  [SIMD（Single Instruction/Multiple Data）とは - IT用語辞典 e-Words](http://e-words.jp/w/SIMD.html)
3.  [【後藤弘茂のWeekly海外ニュース】NVIDIA次世代SoC「Xavier」は進化版DenverとVoltaを搭載 - PC Watch](http://pc.watch.impress.co.jp/docs/column/kaigai/1023668.html)
4.  [Auto-Vectorizer in Visual Studio 2012 – Overview – Parallel Programming in Native Code](https://blogs.msdn.microsoft.com/nativeconcurrency/2012/04/12/auto-vectorizer-in-visual-studio-2012-overview/)
5.  [インテル® C++ コンパイラーのベクトル化ガイド - Compiler_AutoVectorization_Guide.pdf](https://jp.xlsoft.com/documents/intel/compiler/Compiler_AutoVectorization_Guide.pdf)
6.  [OpenMP 4.0 を使用してプログラムで SIMD を有効にする | iSUS](https://www.isus.jp/products/c-compilers/enabling-simd-in-program-using-openmp40/)
7.  [.NET における数値 | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/standard/numerics)