> この記事は[Cg \(\)](https://ja.wikipedia.org/wiki/Cg_\(\))から翻訳されています。


**Cg**は[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")が開発していた、リアルタイム[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")における[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")のための[シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")である。[2012年](../Page/2012年.md "wikilink")を最後にバージョンアップは終了している。[GPUプログラミングのために特化](../Page/Graphics_Processing_Unit.md "wikilink")・最適化されており、[CG](https://ja.wikipedia.org/wiki/CG "wikilink")描画に向いている。この言語名の由来は「グラフィックスのためのC言語」(C for Graphics) であり、[C言語](../Page/C言語.md "wikilink") ([ANSI C](https://ja.wikipedia.org/wiki/ANSI_C "wikilink")) をベースとした[文法](../Page/文法.md "wikilink")を持つ。また、[C++](../Page/C++.md "wikilink")言語の類似機能も一部取り入れている。

## 背景

GPUの技術的な発展にともない、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")のプログラマーが陰影計算処理（[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")）を[プログラミング可能なハードウェアが開発されるようになった](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")。しかし最初期のGPUプログラミングは[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")をベースとしたもので、開発が難しく生産性や[可搬性](https://ja.wikipedia.org/wiki/可搬性 "wikilink")も低かった。そのため、GPU向けの[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")が必要とされるようになり、Cgが開発された。

なお、類似のGPU用高級言語として、[OpenGL](../Page/OpenGL.md "wikilink")ネイティブの[GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")および[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")（[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")）ネイティブの[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")が存在するが、Cgはどちらかというと（[マイクロソフト](../Page/マイクロソフト.md "wikilink")とNVIDIAが共同開発した）HLSLにより近い文法となっている。

GLSLはOpenGL専用であり、またHLSLはDirect3D専用であるが、Cg言語およびCgランタイムライブラリは両方のAPIに対応しているという特徴を持っている。つまり、OpenGLおよびDirect3Dの両方を、Cgシェーダープログラムを実行する基盤として利用することができる。

NVIDIAの[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")開発・実行環境である[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")用に拡張されたC/C++では、Cgによく似たデータ型や組み込み関数が実装されているなど、Cgは後発の言語にも影響を及ぼしている。

## 詳細

### データ型

Cgは6つの[基本データ型](https://ja.wikipedia.org/wiki/基本データ型 "wikilink")を持っている。

  - `float` - 32ビット浮動小数点型
  - `half` - 16ビット浮動小数点型
  - `int` - 32ビット整数型
  - `fixed` - 12ビット固定小数点型
  - `bool` - 論理型
  - `sampler*` - テクスチャオブジェクト型

Cgにはその他にも、`float3`や`float4x4`のように、[ベクトル](https://ja.wikipedia.org/wiki/ベクトル "wikilink")や[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")そのものを扱う型がある。これらは3次元のコンピュータグラフィックス計算において多用される型である。また、[配列](../Page/配列.md "wikilink")や[構造体](../Page/構造体.md "wikilink")も用意されている。[ポインタをサポートしない代わりに](../Page/ポインタ_\(プログラミング\).md "wikilink")、配列は[第一級オブジェクト](https://ja.wikipedia.org/wiki/第一級オブジェクト "wikilink")である\[1\]。

### 演算子

Cgは[C言語](../Page/C言語.md "wikilink")で用いられる[算術演算子](https://ja.wikipedia.org/wiki/算術演算子 "wikilink")や[論理演算子](https://ja.wikipedia.org/wiki/論理演算子 "wikilink")をサポートしている。算術演算子はベクトル型や行列型にも適用できるものがあり、（C++言語の演算子オーバーロードのように）プログラムの可読性を高め、直感的に理解しやすいグラフィックスプログラムを書くことができるようになっている。

### 関数と制御構造

CgはC言語と同様の[制御構造](https://ja.wikipedia.org/wiki/制御構造 "wikilink")を記述するための構文を持つ。[関数を定義することもできる](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")。パラメータは既定で値渡しであり、`in`/`out`/`inout`/`uniform`の修飾子を指定することもできる。

### 標準ライブラリ

C言語と同様に、CgにはGPUプログラミングのための[標準ライブラリ](https://ja.wikipedia.org/wiki/標準ライブラリ "wikilink")がある。`abs()`や`sin()`など、C言語の標準ライブラリと共通の数学関数がある一方で、[テクスチャマッピング](https://ja.wikipedia.org/wiki/テクスチャマッピング "wikilink")のための`tex1D()`や`tex2D()`など、GPUプログラミングに特化した関数も用意されている\[2\]。

### ランタイムライブラリ

Cgによるプログラムは基本的に頂点やピクセルの[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")を行うためのものであり、そのほかのレンダリングプロセスや入出力を扱うためのC/C++ホストプログラムを必要とする。Cgは[OpenGL](../Page/OpenGL.md "wikilink")や[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")の[API基盤上で動作させることができるが](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、Cgシェーダープログラムを各APIと連携・バインドさせるためのライブラリがNVIDIAから提供されている。

### 対応プロファイル

Cgで使用可能なシェーダープログラムのプロファイル、すなわちOpenGLやDirectXにおけるシェーダーモデルのバージョンは、2012年2月リリースのCg Toolkit 3.1時点では、リファレンスマニュアルによると下記のようになっている。

  - OpenGL
      - NVIDIA Vertex Program 5.0 まで
      - NVIDIA Fragment Program 5.0 まで
      - NVIDIA Geometry Program 5.0 まで
      - NVIDIA Tessellation Control Program 5.0 まで
      - NVIDIA Tessellation Evaluation Program 5.0 まで
  - DirectX 11.0
      - HLSL Vertex Shader 5.0 まで
      - HLSL Pixel Shader 5.0 まで
      - HLSL Geometry Shader 5.0 まで
      - HLSL Hull Shader 5.0 まで
      - HLSL Domain Shader 5.0 まで
  - DirectX 10.0
      - HLSL Vertex Shader 4.0 まで
      - HLSL Pixel Shader 4.0 まで
      - HLSL Geometry Shader 4.0 まで
  - DirectX 9.0c
      - HLSL Vertex Shader 3.0 まで
      - HLSL Pixel Shader 3.0 まで

なお、OpenGLはバージョン4.3で、DirectXはバージョン11でCompute Shaderを導入しているが、Cgはバージョン3.1時点ではまだそれらに対応していない。

### CgFX

Cg言語は複数のシェーダープログラムを組み合わせた一連の処理パイプライン（Pass）およびそれらの入出力をまとめてひとつの「Technique」として管理することのできるEffectフレームワーク「CgFX」も同時に備えている。これはDirect3D 9やDirect3D 11の拡張ライブラリ（D3DX9、D3DX11）およびDirect3D 10のコアライブラリでサポートされているEffectフレームワークとよく似ており、個別にパイプラインステージごとのシェーダープログラムおよびその入出力を管理するよりもずっとシェーダープログラムのパイプラインを構築しやすくなる。 Effectには複数のTechniqueを含むことができ、Techniqueには複数のPassを含むことができる。

### サンプルコード

``` cpp
// input vertex
struct VertIn {
    float4 pos   : POSITION;
    float4 color : COLOR0;
};

// output vertex
struct VertOut {
    float4 pos   : POSITION;
    float4 color : COLOR0;
};

// vertex shader main entry
VertOut main(VertIn input, uniform float4x4 modelViewProj) {
    VertOut output;
    output.pos     = mul(modelViewProj, input.pos); // calculate output coords
    output.color   = input.color; // copy input color to output
    output.color.z = 1.0f; // blue component of color = 1.0f
    return output;
}
```

## FX Composer

Cgを使ったシェーダーオーサリングツールとして、FX Composerと呼ばれるソフトウェアがNVIDIAによって開発・提供されていたが、DirectX 10に対応するv2.5を最後に開発が終了している\[3\]。

## nvFX

Cgは2012年4月リリースのバージョン3.1.0013を最後に更新がなされておらず、開発が終了している。 なお開発者へのCgランタイム自体の提供自体は継続されるものの、将来の新しいハードウェア機能をサポートしないため、新規開発での採用は推奨されていない\[4\]。 後継のクロスプラットフォームなシェーダーエフェクトフレームワークとして、NVIDIAによってnvFXが開発されている \[5\]\[6\]。 nvFXはHLSLやGLSLをバックエンドとするが、[OpenGL ESもサポートし](https://ja.wikipedia.org/wiki/OpenGL_ES "wikilink")、モバイルなどの組み込み機器もターゲットとなる。

## 採用例・実績

  - [LightWave](../Page/LightWave.md "wikilink") - LightWaveはバージョン11.6でCgFXを採用している。CgFXによってリアルタイムプレビュー時の法線マッピング機能などが追加されるほか、ユーザーが独自のカスタムシェーダーを実装して利用することができるようになる\[7\]。
  - [Maya](https://ja.wikipedia.org/wiki/Maya "wikilink") \[8\]
  - [PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink") \[9\]
  - [Adobe Photoshop](../Page/Adobe_Photoshop.md "wikilink") \[10\]
  - [Unity (ゲームエンジン)](https://ja.wikipedia.org/wiki/Unity_\(ゲームエンジン\) "wikilink") \[11\]
  - [Far Cry](https://ja.wikipedia.org/wiki/Far_Cry "wikilink") \[12\]

## 関連項目

  - [コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")
  - [GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")
  - [HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")
  - [CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")
  - [Crystal Space](https://ja.wikipedia.org/wiki/Crystal_Space "wikilink")
  - [OGRE](https://ja.wikipedia.org/wiki/OGRE "wikilink")

## 参照

## 外部リンク

  -
[Category:NVIDIA](https://ja.wikipedia.org/wiki/Category:NVIDIA "wikilink") [Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink") [Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink")

1.  [Cg language | NVIDIA Developer Zone](https://developer.download.nvidia.com/cg/Cg_language.html)
2.  [Cg Standard Library Documentation | NVIDIA Developer Zone](https://developer.download.nvidia.com/cg/index_stdlib.html)
3.  [FX Composer](https://developer.nvidia.com/fx-composer)
4.  [Cg Toolkit: "Cg 3.1 is our last release and while we continue to make it available to developers, we do not recommend using it in new development projects because future hardware features may not be supported."](https://developer.nvidia.com/cg-toolkit)
5.  [nvFX: A New Scene and Material Effect Framework for OpenGL and DirectX](http://on-demand.gputechconf.com/gtc/2012/presentations/SB117-nvFX-OpenGL-DirectX.pdf)
6.  [tlorach/nvFX: Generic Effect system for Graphic API's (OpenGL and DirectX)](https://github.com/tlorach/nvFX)
7.  [LightWave - LightWave 3D Group Unveils LightWave 116](https://www.lightwave3d.com/news/article/lightwave-3d-group-unveils-lightwave-116/)
8.  [Maya ユーザ ガイド: CgFX シェーダを操作する](http://download.autodesk.com/global/docs/maya2014/ja_jp/index.html?url=files/Asts_Work_with_CgFX_shaders.htm,topicNumber=d30e534637)
9.  [NVIDIAに聞く、GPUプログラミングの最新動向：CodeZine](https://codezine.jp/article/detail/1822)
10. Windows版Photoshop CS5には、cg.dllおよびcgGL.dllランタイム 2.0.0015が同梱されている。
11. [Cg Programming/Unity - Wikibooks, open books for an open world](https://en.wikibooks.org/wiki/Cg_Programming/Unity)
12. [Cg - OpenGL.org](https://www.opengl.org/wiki/Cg)