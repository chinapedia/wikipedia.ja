> この記事は[GLSL](https://ja.wikipedia.org/wiki/GLSL)から翻訳されています。


**GLSL** ([OpenGL](../Page/OpenGL.md "wikilink") Shading Language) は**GLslang**としても知られ、[C言語](../Page/C言語.md "wikilink")をベースとした高レベル[シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")である。これは[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")やハードウェアに依存した言語を使わないで、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")開発者が[グラフィックスパイプライン](../Page/グラフィックスパイプライン.md "wikilink")を直接制御できるようにOpenGL ARB (Architecture Review Board) \[1\]で策定された。

## 背景

Direct3D 7までの時代、すなわち1990年代までのリアルタイム3Dコンピューターグラフィックスは、OpenGLや[Direct3D](../Page/Direct3D.md "wikilink")といった[APIを通して](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")上のチップ（[GPU](../Page/Graphics_Processing_Unit.md "wikilink")）にあらかじめ用意された固定のレンダリングパイプライン上で、固定機能のシェーダー（頂点トランスフォームや陰影計算を専門に担当するユニット）を組み合わせることで実現されていた。Direct3D 8が登場した2000年以降は、GPUの進化・性能向上に伴い、新機能はハードウェア実装による固定機能ではなく、アプリケーション開発者がソフトウェアプログラム（[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")）によって頂点レベル・フラグメントレベル（ピクセルレベル）での制御・カスタマイズを行ない、レンダリングパイプライン内での柔軟性や表現力を増すことができる形で追加されることが多くなっている。

元々、このプログラマブルシェーディング機能は複雑で直感的でない[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれたシェーダーを使わないと実現できなかった。OpenGL ARBは、[OpenGL](../Page/OpenGL.md "wikilink")をグラフィックス産業の歴史の中で[オープンスタンダード](https://ja.wikipedia.org/wiki/オープンスタンダード "wikilink")なものにしていく中で、グラフィックス処理を行うプログラミングをより直感的・効率的にできる方法として、OpenGL Shading Languageを作り出した。

OpenGL Shading Languageは2003年に発表されたOpenGL 1.5の拡張機能として導入された\[2\]が、OpenGL ARBはOpenGL 2.0にGLSLを含めることを正式に決定した。OpenGL 2.0は[1992年](../Page/1992年.md "wikilink")に発表されたOpenGL 1.0から数えて初のメジャーバージョンアップである。

初期のOpenGLプログラマブルシェーダーは、頂点単位のトランスフォームや陰影計算を行なう**バーテックスシェーダー** (vertex shader) と、フラグメント（ピクセル）単位の陰影計算を行なう**フラグメントシェーダー** (fragment shader) のみが利用可能であった。その後、プリミティブの増減や変更などを実行できる**ジオメトリシェーダー** (geometry shader) がOpenGL 3.2/GLSL 1.5にて標準化された。またOpenGL 4.0で固定機能シェーダーであるテッセレーションステージが追加されるに伴い、**テッセレーション・コントロールシェーダー** (tessellation control shader) と、**テッセレーション・エバリュエーションシェーダー** (tessellation evaluation shader)、これら2つのプログラマブルなシェーダーがGLSLの仕様に追加された。フラグメントシェーダーもサンプルレベルでの制御が可能となった。

なお、OpenGLと同様の3DグラフィックスAPIである[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")（[Direct3D](../Page/Direct3D.md "wikilink")）およびそのシェーディング言語である[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")にはバージョン11以降、GPUにおける汎用的なコンピューティング（[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")）を可能とするDirectX Compute Shader（[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")）が追加されているが、OpenGLおよびGLSLのバージョン4.0時点ではこれに相当するシェーダーは含まれていなかった。しかし、バージョン4.3においてOpenGL**コンピュートシェーダー** (compute shader) として同等機能が導入されることになった。なお、コンピュートシェーダーの導入以前からOpenGLの管轄を行なっているクロノスが同様にオープン仕様として策定している、GPUを汎用コンピューティングに用いることのできるAPIとして[OpenCL](../Page/OpenCL.md "wikilink")が存在するが、こちらはCPUやGPU等あらゆる計算資源を計算に用いることのできる異種計算資源混在（ヘテロジニアス）環境向けのAPIであり、グラフィックスパイプラインとの連携を主目的としたコンピュートシェーダーとは得意分野が若干異なる。

GLSLを使うメリットとして、

  - レンダリングアルゴリズムの柔軟なカスタマイズや再利用性が増すことで、従来のハードウェア固定機能にとらわれない、柔軟でユニークかつ高品質なリアルタイム3DCGシーンの構築が可能となる。
  - [Macintosh](../Page/Macintosh.md "wikilink")や[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")を含む複数の[OS間での互換性を確保できる](../Page/オペレーティングシステム.md "wikilink")。
  - アセンブリ言語を用いるよりもコードの再利用性やメンテナンス性が増す。
  - OpenGL Shading LanguageをサポートするどんなハードウェアベンダーのGPU上でも動作するシェーダーを書くことができる能力を持つ。
  - それぞれのハードウェアベンダーは[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")内にGLSL[コンパイラ](../Page/コンパイラ.md "wikilink")を含めることができるので、そのGPUのアーキテクチャに最適化されたコードを生成することができる。

などが挙げられる。 従来の固定機能シェーダーに対するデメリットとしては、

  - シェーダーのコンパイルおよびアタッチなど、レンダリングのための準備作業が増える。
  - OpenGL APIの他に、GLSLの学習コストがかかる。
  - GPU特性やハードウェア仕様を把握してGLSLコードを記述する必要があり、CPUと比較してチューニングが難しい。

などが挙げられる。

なお、GLSLの派生規格として、組み込み環境向けの[OpenGL ES用のシェーダー言語](../Page/OpenGL_ES.md "wikilink")「GLSL ES」が存在する。これはESSLと呼ばれることもある\[3\]。

[Webブラウザ](https://ja.wikipedia.org/wiki/Webブラウザ "wikilink")向けのOpenGL ES派生規格として[WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink")が存在するが、WebGLでもGLSLが使用される。

クロノスが策定しているローレベルグラフィックスAPIである[Vulkanは](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")、シェーダープログラムの中間表現SPIR-Vを入力として受け付けるが、SPIR-Vを出力するオフラインシェーダーコンパイラ**glslangValidator**において最初にサポートされた上位レベルシェーディング言語はGLSLである。のちにSPIR-VはOpenGL 4.6にも導入された。

## 詳細

### データ型

OpenGL Shading Language 1.50の仕様では64の基本データ型を定義している。いくつかはC言語内で使われていたものとまったく同じものであるが、一方他のものはグラフィックス処理に特化している。 例えば以下のような型が定義されている\[4\]。

  - `void` 値を返さない関数に用いる
  - `bool` 条件型。値はtrueかfalseのどちらかをとる
  - `int` 符号付32bit整数
  - `float` 単精度浮動小数点数
  - `vec2` 2要素を持つ単精度浮動小数点数[ベクトル](../Page/ベクトル.md "wikilink")
  - `vec3` 3要素を持つ単精度浮動小数点数ベクトル
  - `vec4` 4要素を持つ単精度浮動小数点数ベクトル
  - `bvec2` 2要素を持つ論理型ベクトル
  - `bvec3` 3要素を持つ論理型ベクトル
  - `bvec4` 4要素を持つ論理型ベクトル
  - `ivec2` 2要素を持つ符号付32bit整数ベクトル
  - `ivec3` 3要素を持つ符号付32bit整数ベクトル
  - `ivec4` 4要素を持つ符号付32bit整数ベクトル
  - `mat2` 2x2要素を持つ単精度浮動小数点数[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")
  - `mat3` 3x3要素を持つ単精度浮動小数点数行列
  - `mat4` 4x4要素を持つ単精度浮動小数点数行列
  - `sampler1D` 1次元のテクスチャにアクセスするためのハンドル
  - `sampler2D` 2次元のテクスチャにアクセスするためのハンドル
  - `sampler3D` 3次元のテクスチャにアクセスするためのハンドル
  - `samplerCube` キューブマップテクスチャにアクセスするためのハンドル
  - `sampler1DShadow` 1次元のデプステクスチャにアクセスするためのハンドル
  - `sampler2DShadow` 2次元のデプステクスチャにアクセスするためのハンドル

なお、符号なし32bit整数のサポートはOpenGL 3.0 (GLSL 1.3) で標準化され、また科学計算などの分野で必要とされることの多い[倍精度浮動小数点数](../Page/倍精度浮動小数点数.md "wikilink")のサポートはOpenGL 4.0 (GLSL 4.0) で標準化されている。

### 演算子

OpenGL Shanding LanguageはホストプログラムにC言語がよく使われていることを背景にして、それによく似た多くの演算子、加えてベクトル演算に特化した特殊な演算子（Tupleを返すSwizzle演算など）も提供している。このことにより、シェーダー開発者はシェーダーを柔軟にかつ効率よく書くことができる。GLSLは[ポインタを除くCや](../Page/ポインタ_\(プログラミング\).md "wikilink")[C++](../Page/C++.md "wikilink")での演算子を含んでいる。

### 関数と制御構造

C言語に似ているということは、もちろんGLSLは、[`if/else``   ``if/else`](../Page/If文.md "wikilink")`、`[`for`](../Page/For文.md "wikilink")`、`[`while`](https://ja.wikipedia.org/wiki/while文 "wikilink")`、`[`do-while`](https://ja.wikipedia.org/wiki/do-while文 "wikilink")`、`[`break`](../Page/Break文.md "wikilink")`、`[`continue`](../Page/Continue文.md "wikilink")などの繰り返しや分岐といった制御文をサポートしている。

ユーザ定義関数もサポートしており、ビルトイン関数と同様広く使われている。このことにより、GPUベンダーは、ハードウェアレベルでそれらの組み込み関数を任意で最適化することができる。これらの関数の多くは`exp()`や`abs()`のようなC言語の標準ライブラリで見られるものとよく似ているが、一方で[`smoothstep`](https://ja.wikipedia.org/wiki/smoothstep "wikilink")`()`や`texture2D()`のようなグラフィックス[プログラミングに特化しているようなものもある](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。

### 変数

GLSLコード内における変数の宣言・使用方法は、C言語でのそれに似ている。

変数の修飾子は4つある（以下バーテックスシェーダー、ジオメトリシェーダー、フラグメントシェーダーをそれぞれVS, GS, FSと示す）。

  - `const` 変化しない。
  - `uniform` 全てのシェーダーで使用可能なグローバルな読み出し専用変数。
  - `in` 入力変数。VSではOpenGLから渡される頂点情報セットを表す（旧`attribute`）。GSではVSによって計算された頂点情報セット、FSではVSまたはGSによって計算された頂点情報が補間された値を表す（旧`varying`）。
  - `out` 出力変数。 VSではGSまたはFSへ（旧`varying`）、GSではFSへ渡す頂点情報セットを表す。FSでは最終的にピクセル単位で出力する色情報を表す。
  - `inout` 入出力変数。

### コンパイルと実行

GLSLシェーダープログラムは単体の[アプリケーションではない](../Page/アプリケーションソフトウェア.md "wikilink")。シェーダーの実行にはOpenGL APIを利用するホストアプリケーションが必要である。ホストアプリケーションを記述する言語には、OpenGL APIをサポートする第一級言語である[C言語](../Page/C言語.md "wikilink")および[C++](../Page/C++.md "wikilink")、あるいはWebGLをサポートする[JavaScript](../Page/JavaScript.md "wikilink")などがよく利用される。

GLSLシェーダー自身は単純にOpenGL APIのエントリポイント（API[関数](../Page/サブルーチン.md "wikilink")）経由で、ハードウェアベンダーの[デバイスドライバー](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")に対してソースコード文字列が渡されるだけである。シェーダープログラムのソースコードはホストプログラム上の文字列リテラルとして記述されたり、アプリケーション実行時に外部テキストファイルなどから読み込まれたりしたものがメモリ上の文字列データとして実体化されるが、オフラインの事前コンパイル方式ではなく、あくまでドライバーにはソースコード文字列の形式で送られ、ドライバーが実行時にシェーダーのソースコードをコンパイルして「シェーダープログラムオブジェクト」を生成する。なお、OpenGL 4.1で標準化されたGL_ARB_get_program_binaryにより、コンパイル済みバイナリのシリアライズ・逆シリアライズがサポートされるようになったが、バイナリがベンダー間で互換性のある中間形式であるかどうかは保証されない。デバイスドライバーがGLSLコンパイラを内蔵していることから、ドライバーによってシェーダープログラムのコンパイル結果や実行結果が異なる可能性があるなどの品質問題も抱えている。OpenGL 4.6では中間表現SPIR-Vがサポートされるようになり、オフラインコンパイルが可能になったことから、OpenGLでプログラマブルシェーダーを利用するために必ずしもGLSLを利用する必要はなくなった。なお、[Direct3D](../Page/Direct3D.md "wikilink")のシェーディング言語である[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")はリリース当初から、コンパイル結果はベンダー非依存の[バイトコード](../Page/バイトコード.md "wikilink")となり、またコンパイル済みバイナリの読み込みもサポートしていた。

### 単純なGLSLバーテックスシェーダーの例

これは固定機能パイプラインと同様に入力頂点を変換する。

``` glsl
void main(void)
{
    gl_Position = ftransform();
}
```

`ftransform()`はGLSL 1.40とGLSL ES 1.0からはサポートされない。代わりに、プログラマは新しいOpenGL 3.1標準に従いモデルビュー行列と投影行列を明示的に指定する必要がある。

``` glsl
#version 140
uniform mat4 projectionMatrix;
uniform mat4 modelviewMatrix;
in vec3 position;

void main(void)
{
    gl_Position = projectionMatrix * modelviewMatrix * vec4(position, 1.0);
}
```

### 単純なGLSLジオメトリシェーダーの例

``` glsl
layout(triangles) in;
layout(triangle_strip, max_vertices = 3) out;

in Input
{
    vec4 Position;
} VSout[3];

void main(void)
{
    for(int i = 0; i < 3; i++)
    {
        gl_Position = VSout[i].Position;
        EmitVertex();
    }
    EndPrimitive();
}
```

### 単純なGLSLフラグメントシェーダーの例

``` glsl
void main(void)
{
    gl_FragColor = vec4(1.0, 0.0, 0.0, 1.0); // Red.
}
```

### バージョン

GLSLはOpenGL仕様とともにバージョンアップされている。OpenGL 3.2までは、対応するGLSLのバージョン番号はOpenGL本体のバージョン番号と無関係にナンバリングされていたが、OpenGL 3.3以降は同一の番号が割り当てられるようになった。

| OpenGLバージョン | GLSLバージョン | \#versionディレクティブ |
| ----------- | --------- | ---------------- |
| 1.5         | 1.0       |                  |
| 2.0         | 1.1       | \#version 110    |
| 2.1         | 1.2       | \#version 120    |
| 3.0         | 1.3       | \#version 130    |
| 3.1         | 1.4       | \#version 140    |
| 3.2         | 1.5       | \#version 150    |
| 3.3         | 3.3       | \#version 330    |
| 4.0         | 4.0       | \#version 400    |
| 4.1         | 4.1       | \#version 410    |
| 4.2         | 4.2       | \#version 420    |
| 4.3         | 4.3       | \#version 430    |
| 4.4         | 4.4       | \#version 440    |
| 4.5         | 4.5       | \#version 450    |
| 4.6         | 4.6       | \#version 460    |
|             |           |                  |

### ツール

GLSLシェーダーは単独で動作するプログラムではなく、シェーダープログラムをGPU上で走らせるためには、まずC/C++などで書かれたホストアプリケーションに入力する必要がある。具体的にはOpenGL APIを使ってシェーダープログラムをコンパイル・リンクしたのち、OpenGLレンダリングコンテキストにプログラムオブジェクトをバインドしてからプリミティブのレンダリングを実行する必要があるが、それらの一連の処理を簡略化するためにいくつかのGLSL開発者・デザイナー用ツール（[オーサリング](https://ja.wikipedia.org/wiki/オーサリング "wikilink")ツール）が存在する。

  - [RenderMonkey](https://gpuopen.com/archive/gamescgi/rendermonkey-toolsuite/) - [ATIによって開発された](../Page/ATI_Technologies.md "wikilink")。[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")シェーダーと同様にGLSLシェーダーを作成、コンパイル、デバッグできるインタフェースを提供している。[Microsoft Windows上でのみ実行できる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。に移管されているが、開発およびサポートは終了している。
  - GLSLEditorSample - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")上でのみ実行できるCocoaアプリケーション。シェーダーの作成とコンパイルはできるがデバッガ機能は組み込まれていない。
  - [Lumina](http://lumina.sourceforge.net/) - 新しいGLSL開発ツール。プラットフォーム独立でインタフェースに[Qt](../Page/Qt.md "wikilink")を使っている。
  - [Blender](http://www.blender.org/) - GPLライセンスのモデリングおよびアニメーション作成パッケージで、バージョン2.4.1で内蔵しているゲームエンジンがGLSLをサポートするようになった。
  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") - 開発者向けツールとして、[WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink")用のバーテックスシェーダー・フラグメントシェーダーを参照・編集できる"シェーダーエディター"が実装されている\[5\]。

## 脚注

## 関連項目

  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [OpenGL ES](../Page/OpenGL_ES.md "wikilink")
  - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")
  - [WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink")
  - [HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")
  - [Cg (プログラミング言語)](../Page/Cg_\(プログラミング言語\).md "wikilink")
  - [シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")
  - [Core Image](../Page/Core_Image.md "wikilink")

[Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink") [Category:OpenGL](https://ja.wikipedia.org/wiki/Category:OpenGL "wikilink")

1.  [About the OpenGL Architecture Review Board Working Group](https://www.opengl.org/archives/about/arb/)
2.  ["The OpenGL(R) Graphics System: A Specification (Version 1.5)", p.294](https://www.opengl.org/registry/doc/glspec15.pdf)
3.  [Shader Compiler Technologies - OpenGL, ESSL, GLSL Shaders](https://www.lunarg.com/shader-compiler-technologies/)
4.  [Data Type (GLSL) - OpenGL Wiki](https://www.khronos.org/opengl/wiki/Data_Type_\(GLSL\))
5.  [シェーダーエディター - 開発ツール | MDN](https://developer.mozilla.org/ja/docs/Tools/Shader_Editor)