> この記事は[High Level Shading Language](https://ja.wikipedia.org/wiki/High_Level_Shading_Language)から翻訳されています。


**High Level Shading Language**（ハイレベル シェーディング ランゲージ、略称: **HLSL**）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")によって開発された、[Direct3D](../Page/Direct3D.md "wikilink") ([DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")) で使われる[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")のための[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[シェーディング言語](../Page/シェーディング言語.md "wikilink")である。かつては **High Level Shader Language** という呼び方もされていた\[1\]。ただしMSDNの日本語版では、Direct3D 11がリリースされた後でも**上位レベル シェーダー言語**（じょういれべるシェーダーげんご）という訳語を使用している\[2\] \[3\]。

HLSLは[OpenGL](../Page/OpenGL.md "wikilink")で使われるシェーディング言語である[GLSL](../Page/GLSL.md "wikilink")と（機能的には）類似の物である。また、[NVIDIA](../Page/NVIDIA.md "wikilink")と協力して開発されたことから、言語文法が[Cg](../Page/Cg_\(プログラミング言語\).md "wikilink")（C for Graphics）言語に非常によく似ている。

## 開発経緯

Direct3D 7まではグラフィックスカードに実装された固定パイプラインおよびハードウェア機能を駆使して3Dグラフィックスシーンを構築していたが、グラフィックス表現の柔軟性を向上させるべく、Direct3D 8では[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")が搭載された\[4\]。これによって、グラフィックスアプリケーション開発者がグラフィックス描画アルゴリズムをソフトウェアによってカスタマイズすることが可能となった。しかし、Direct3D 8で使用できるシェーダー言語は[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")（[低級言語](https://ja.wikipedia.org/wiki/低級言語 "wikilink")）であったため、開発効率やプログラムコードの再利用性に限界があった。それを解消するべく、[C言語](../Page/C言語.md "wikilink")風の宣言文や制御文などの記法を可能とした高級言語HLSLが開発されることとなった。HLSLはDirect3D 9で初めて導入され、その後もDirect3Dとともに機能拡張が続けられている。

[GDC](../Page/Game_Developers_Conference.md "wikilink") 2016ではDirectX 12の今後の発展、そして新たな次期DirectXとシェーダーモデル6の開発に関して言及があり、HLSL言語仕様にも大きな機能追加が予定されていることが発表された\[5\]。シェーダーモデル6.0では*Wave*と呼ばれるスレッドグループの概念と各グループ内でのデータ交換のための組み込み命令が導入され、NVIDIA GPUの*Warp*およびAMD GPUの*Wavefront*を標準化することが予定されている\[6\]。

## プログラマブルパイプラインステージ

HLSLによってプログラム可能なグラフィックスパイプラインステージは、対応するDirect3Dのバージョンおよびシェーダーモデル（後述）によって異なる。

  - Direct3D 9の場合（シェーダーモデル1.x-3.0）は、[頂点シェーダー](https://ja.wikipedia.org/wiki/頂点シェーダー "wikilink")（[バーテックスシェーダー](https://ja.wikipedia.org/wiki/バーテックスシェーダー "wikilink")）および[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")（OpenGLにおける[フラグメントシェーダー](https://ja.wikipedia.org/wiki/フラグメントシェーダー "wikilink")に相当）の2つである。
  - Direct3D 10.xの場合（シェーダーモデル4.x）は、頂点シェーダー、[ジオメトリシェーダー](https://ja.wikipedia.org/wiki/ジオメトリシェーダー "wikilink")（OpenGLではプリミティブシェーダーとも呼ばれる）、そして[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")の3つである。
  - Direct3D 11.x/12の場合（シェーダーモデル5.x）は、頂点シェーダー、ハルシェーダー（OpenGLにおける[テッセレーション](https://ja.wikipedia.org/wiki/テッセレーション "wikilink")制御シェーダーに相当）、ドメインシェーダー（OpenGLにおける[テッセレーション](https://ja.wikipedia.org/wiki/テッセレーション "wikilink")評価シェーダーに相当）、[ジオメトリシェーダー](https://ja.wikipedia.org/wiki/ジオメトリシェーダー "wikilink")、[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")、そして[コンピュートシェーダー](https://ja.wikipedia.org/wiki/コンピュートシェーダー "wikilink")（計算シェーダー、演算シェーダー）の6つである。ただしコンピュートシェーダーだけはグラフィックスパイプラインとは独立して動作させることができる。

頂点シェーダーはアプリケーションによって提供（入力）される頂点それぞれについて実行され、主にオブジェクト空間から視空間への頂点座標変換やテクスチャ座標の生成、また頂点の接線や従法線や法線ベクトルのような光線の係数の計算などの処理を担当する。頂点シェーダーを通して頂点のグループ (三角形であれば通常は3個) が入力された時、出力座標はその領域内で画面上のピクセルを決めるために補間される。この処理は[ラスタライゼーション](https://ja.wikipedia.org/wiki/ラスタライゼーション "wikilink")として知られている。これらのピクセルそれぞれがピクセルシェーダーを通ることで、結果としてスクリーン上の各点の色が計算される。

また、Direct3D 10/11/12対応ハードウェアにおいてDirect3D 10/11/12インターフェイスを使うアプリケーションは、頂点シェーダーステージの後にジオメトリシェーダーを指定することもできる。ジオメトリシェーダーはラスタライズの前にプリミティブの増減や種類の変更を行なうことができる。

なお、HLSLで使用可能な[パーリンノイズ](../Page/パーリンノイズ.md "wikilink")生成関数であるnoise()は、テクスチャシェーダーと呼ばれる特殊なシェーダーステージでのみ利用が可能となっている。

## 言語機能

HLSLの基本的な文法はC/C++に準ずるが、グラフィックスプログラムを記述するのに適した専用のベクトル・行列型や関数を備えている。数学関数の中にはC/C++標準ライブラリと同様のものも含まれる。また、Direct3D 10ではAPIの大幅な設計変更が行なわれたこともあり、Direct3D 9用のHLSLと比較して、Direct3D 10以降用のHLSLでは[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")に基づいた言語仕様の再設計がなされ、多数の仕様変更が加えられている\[7\]。

Direct3D 10以降ではHLSLにて[クラスを定義し](../Page/クラス_\(コンピュータ\).md "wikilink")、C++のようにデータ（メンバー変数）と振る舞い（メンバー関数）を関連付けることが可能だが、アクセス指定子による[カプセル化](../Page/カプセル化.md "wikilink")や[継承および仮想関数といった機能は備えていない](../Page/継承_\(プログラミング\).md "wikilink")。

Direct3D 11ではシェーダーの[組み合わせ爆発](https://ja.wikipedia.org/wiki/組み合わせ爆発 "wikilink")問題を解消するべく、HLSLにて[インターフェイスの定義と実装による](../Page/インタフェース_\(情報技術\).md "wikilink")[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")を疑似的に実現する「動的シェーダーリンク（Dynamic Shader Linkage）」と呼ばれる機能が追加された\[8\]。

## コード例

以下にDirect3D 10/11向けHLSLを用いた、単純な[Half Lambert照明モデルおよび](../Page/ランバート反射.md "wikilink")[Phong照明モデル](../Page/Phongの反射モデル.md "wikilink")（Blinn-Phong）の頂点シェーダーおよびピクセルシェーダーのプログラムを示す。なお分岐によって照明モデルを切り替えているが、これはいわゆるウーバーシェーダー（uber-shader）なので、実行速度効率などは考慮していないことに注意されたい。

``` cpp
// Shader Constants.
matrix TrWorldViewProj;
matrix TrWorld;
float4 LightPosition;
float3 EyePosition;
float4 DiffuseColor;
float4 SpecularColor;
float SpecularPower;
bool IsPhongModel;

struct BasicVSOutput
{
    float4 Pos : SV_POSITION;
    float3 WPos : TEXCOORD1;
    float3 WNormal : NORMAL0;
};
typedef BasicVSOutput BasicPSInput;

// Vertex Shader Program.
BasicVSOutput BasicVS(float3 pos : POSITION0, float3 normal : NORMAL0)
{
    BasicVSOutput output = (BasicVSOutput)0;
    output.Pos = mul(float4(pos, 1), TrWorldViewProj);
    output.WPos = mul(float4(pos, 1), TrWorld).xyz;
    output.WNormal = mul(normal, (float3x3)TrWorld);
    return output;
}

float4 CalcLambert(float3 light, float3 wnormal)
{
    // Half Lambert.

    float lambert = dot(light, wnormal);
    lambert = lambert * 0.5f + 0.5f;
    lambert *= lambert;
    return lambert * DiffuseColor;
}

float4 BasicLambert(BasicPSInput input)
{
    const float3 light = normalize(LightPosition.xyz - input.WPos);
    const float3 normal = normalize(input.WNormal);
    return CalcLambert(light, normal);
}

float4 BasicPhong(BasicPSInput input)
{
    // Phong lighting with specular.

    const float3 eye = normalize(EyePosition - input.WPos);
    const float3 light = normalize(LightPosition.xyz - input.WPos);
    const float3 halfway = normalize(light + eye);
    const float3 normal = normalize(input.WNormal);
    const float specular = pow(max(dot(normal, halfway), 0.0), SpecularPower);
    return CalcLambert(light, normal) + specular * SpecularColor;
}

// Pixel Shader Program.
float4 BasicPS(BasicPSInput input) : SV_TARGET0
{
    if (IsPhongModel)
    {
        return BasicPhong(input);
    }
    else
    {
        return BasicLambert(input);
    }
}
```

例のように、ピクセルシェーダーによってピクセル単位の正規化法線ベクトルを求めることにより、Direct3D 7以前の固定機能シェーダーでは実現が難しかったPer-Pixelライティングが容易に実装可能となっている。 もちろん、使用するシェーダーモデルおよび対応するハードウェアによっては、より複雑で長大なアルゴリズムを実装することもできる。リアルタイムグラフィックスゆえにハードウェア性能に応じたトレードオフにはなるが、単純な局所照明（[ローカルイルミネーション](https://ja.wikipedia.org/wiki/ローカルイルミネーション "wikilink")）だけでなく、より厳密な物理ベースのに基づいた、大域照明（[グローバルイルミネーション](https://ja.wikipedia.org/wiki/グローバルイルミネーション "wikilink")）モデルをHLSLによるプログラマブルシェーダーで実装することで、より現実に近いリアルタイム3Dコンピューターグラフィックスを実現することも可能となる。さらに、Direct3D 11 ([DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")) ではコンピュートシェーダーを使って、GPUにグラフィックス用途以外の汎用計算を行なわせる[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")プログラムをHLSLで記述することも可能となる。

なお、HLSLソースファイルには通例.hlsl拡張子が付けられ、ヘッダーファイルには.hlsli拡張子が付けられる\[9\]。

## 対応環境

HLSLプログラムは主にホストとなるC++アプリケーションプログラムコードからDirect3D APIを使って入力と出力を管理する必要があるので、単体で動作させることはできない。なお、単体のコンパイラはマイクロソフトから無償提供されている[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") SDK（あるいはバージョン8.0以降のWindows SDK）に付属する。プロプライエタリなHLSLコンパイラfxc.exeによって出力されるのは、グラフィックスハードウェアのベンダーに依存しない共通[バイトコード](../Page/バイトコード.md "wikilink")であるため、一度コンパイルしておけば異なるハードウェアであっても（コンパイル時に想定されていた機能を満たす限り）動作させることができる\[10\]。HLSLプログラムをサポートするのはDirect3D 9以降をサポートするシステムに限られるため、2015年1月現在では[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink") OS、[Xbox 360および](../Page/Xbox_360.md "wikilink")[Xbox Oneが主な動作環境である](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")。

アプリケーションの実行時にHLSLソースコードをコンパイルしてバイトコードを生成する機能を組み込むためのD3DCompilerランタイムも提供されている\[11\]。

他に、ゲームエンジンの[Unityでは](https://ja.wikipedia.org/wiki/Unity_\(ゲームエンジン\) "wikilink")、Windows上で[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")ベース (DirectX 11ベース) のコンピュートシェーダーを使用することができるが、コンピュートシェーダーの記述にはCgではなくHLSLを用いる\[12\]。UnityはCg/HLSLからGLSLへのトランスレーションが可能なため、OpenGL 4.3や[OpenGL ES](../Page/OpenGL_ES.md "wikilink") 3.1のコンピュートシェーダーを用いる場合でもGLSLではなくHLSLを使用することが推奨されている。

[LLVM](../Page/LLVM.md "wikilink")/[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")ベースのHLSLコンパイラdxc.exeも[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")上で開発が進められている\[13\]。こちらはDirectX Intermediate Language (DXIL) と呼ばれる別の中間言語コードを生成するが、これまでのfxc.exeが生成するバイトコードとは互換性がない。

## エフェクト

HLSL自体は、シェーダー関数および各シェーダーステージのエントリーポイント（いわゆるメイン関数）を記述するために使われるが、この複数のシェーダーステージをまとめて管理・適用する「エフェクト」と呼ばれる仕組みも存在する。つまり、例えば2つの頂点シェーダーエントリーポイントVS1(), VS2()と2つのピクセルシェーダーエントリーポイントPS1(), PS2()を単一のHLSLソースプログラムファイル（通例.fx拡張子が付けられ、エフェクトファイルと呼ばれる）に記述し、さらにVS1+PS1, VS2+PS2, VS1+PS2, VS2+PS1といったシェーダーステージの組み合わせ（パス）のほか、各種レンダリングステートの設定をエフェクトファイル中に記述して関連付けることができる。エフェクトを扱う[APIはDirect](../Page/アプリケーションプログラミングインタフェース.md "wikilink")3D 10のコアライブラリもしくはDirect3D 9/11のエクステンションライブラリ（D3DX）に用意されており、レンダリングパイプラインの管理をC++コードから分離することができる。

## WPFエフェクト

Windowsデスクトップアプリケーションフレームワークの1つである[WPFでは](../Page/Windows_Presentation_Foundation.md "wikilink")、グラフィックスのレンダリングにDirect3Dが使用されているが、GUIウィジェットにブラー（ぼかし）やドロップシャドウといったエフェクト（フィルター）を適用することが可能となっている。さらにWPFではユーザープログラマーがHLSLで作成したピクセルシェーダーを使用してカスタムエフェクトを適用することもできる\[14\]。

WPF 3.5まではシェーダーモデル2.0のピクセルシェーダーのみがサポートされていたが、WPF 4ではシェーダーモデル3.0のピクセルシェーダーも使用できるようになった\[15\] \[16\]。

## Direct2Dエフェクト

DirectXファミリーの1つ、[2次元コンピュータグラフィックス](../Page/2次元コンピュータグラフィックス.md "wikilink")APIである[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")では、バージョン1.1にてエフェクト機能が実装されたが、HLSLによるカスタムエフェクトを作成・利用することも可能となっている\[17\]。

## シェーダーモデル

Direct3Dプログラマブルシェーダーを実行するには、Direct3D 8以降に対応したハードウェアが必要となる。ただし、Direct3D 9までの場合、頂点シェーダーだけはソフトウェアすなわちCPUでエミュレートすることもできる（`D3DCREATE_SOFTWARE_VERTEXPROCESSING`）ため、固定機能ピクセルシェーダーと組み合わせることによりDirect3D 7以前の古いハードウェアでプログラマブルシェーダーを実行することも可能である。また、Direct3D 10.1以降では比較的高速なソフトウェアレンダリングエンジンであるWARPデバイスも実装されているため、GPUが対応していなくてもCPUにDirect3Dレンダリングを実行させることもできる。

Direct3D対応ハードウェア（[グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")）の世代によって、GPU上にてハードウェアレベルで実行可能なシェーダープログラムの仕様（制約、機能など）が異なる。この仕様は**シェーダーモデル**と呼ばれ、新しい世代のシェーダーモデルをサポートするハードウェアは基本的に古い世代のシェーダーモデルもサポートする\[18\]が、ベンダーごとに拡張された2.0a/2.0bなどの例外も存在する。 なおHLSLがDirect3Dに搭載されたのはバージョン9以降だが、シェーダーモデル2.0以降でないとHLSLを使えないというようなことはなく、HLSLを使用してシェーダーモデル1.xレベルのプログラムを記述することも可能である。また、Direct3D 10では、アセンブリ言語によるシェーダープログラム開発が廃止され、シェーダーの記述にはHLSLのみが使用できるようになった\[19\]。

シェーダーモデル3.0には頂点テクスチャフェッチ（Vertex Texture Fetch, VTF）と呼ばれる機能が存在するが、DirectX 9.0c世代で対応したのはNVIDIAのハードウェアのみで、[ATIのハードウェアではサポートされなかった](../Page/ATI_Technologies.md "wikilink")。逆に、浮動小数点バッファにおけるアンチエイリアス機能は、NVIDIAハードウェアではサポートされず、ATIハードウェアのみでの対応となっていた\[20\] \[21\]。他にも、（DirectX 11で標準化される前の）[テッセレーション](https://ja.wikipedia.org/wiki/テッセレーション "wikilink")機能\[22\]がATIハードウェア上のみでサポートされる\[23\] \[24\] \[25\]など、シェーダーモデル3.0までは（たとえDirectX 9.0c対応を謳っていても）機能面において各社の足並みがそろわない状態にあり、これらの機能を利用するアプリケーション開発者は使用したい機能が実際にハードウェアでサポートされているかどうかをあらかじめDirect3DのCaps (Capabilities) 取得APIを使って一つ一つ調べなければならなかった。このようにベンダーごとに各機能の対応レベルがバラバラとなっていた悲惨な状況は、次のバージョンのDirect3D 10以降で要求仕様が厳格化されたことで、ある程度解消されることになる\[26\]。

なお、Direct3D 10.1 APIでは4.xプロファイルのシェーダープログラムに加えてダウンレベルの2.0プロファイルが使用可能であり、Direct3D 11/12 APIでは5.xおよび4.xプロファイルに加えてダウンレベルの2.0プロファイルが使用可能だが、いずれも3.0プロファイルに関しては使用できない\[27\] \[28\] \[29\] \[30\]。

### DirectXバージョンと各シェーダーステージ

以下の表はハードウェアが対応しているDirectXバージョンと、そのハードウェアがサポートする各シェーダーステージの最上位バージョン（プロファイル）間の関係を示している。 後述するように、実行可能なシェーダープログラムの最大命令数やレジスタ数、リソーススロット数などは新しいバージョンのほうが大きくなり、より柔軟で長大なプログラムを記述することができるようになる。

| DirectX Version | Pixel Shader  | Vertex Shader | Geometry Shader | Hull Shader | Domain Shader | Compute Shader |
| --------------- | ------------- | ------------- | --------------- | ----------- | ------------- | -------------- |
| 8.0             | 1.0, 1.1      | 1.0           | \-              | \-          | \-            | \-             |
| 8.1             | 1.2, 1.3, 1.4 | 1.1           | \-              | \-          | \-            | \-             |
| 9.0             | 2.0           | 2.0           | \-              | \-          | \-            | \-             |
| 9.0a            | 2.0a          | 2.0a          | \-              | \-          | \-            | \-             |
| 9.0b            | 2.0b          | 2.0           | \-              | \-          | \-            | \-             |
| 9.0c            | 3.0           | 3.0           | \-              | \-          | \-            | \-             |
| 10.0            | 4.0           | 4.0           | 4.0             | \-          | \-            | 4.0            |
| 10.1            | 4.1           | 4.1           | 4.1             | \-          | \-            | 4.1            |
| 11.0-11.2       | 5.0           | 5.0           | 5.0             | 5.0         | 5.0           | 5.0            |
| 11.3, 12        | 5.1           | 5.1           | 5.1             | 5.1         | 5.1           | 5.1            |
| 12              | 6.0           | 6.0           | 6.0             | 6.0         | 6.0           | 6.0            |

なおコンピュートシェーダー（[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")）はDirectX 11にて導入されたステージであり、DirectX 10 APIを経由して利用することはできないが、ドライバーが対応していればDirectX 10.x世代のハードウェア上でもDirectX 11 APIを経由してダウンレベル（機能制限付き）のコンピュートシェーダーを実行することが可能となる。

シェーダーモデル5.1\[31\]はDirectX 12 APIをドライバーレベルでサポートするすべてのハードウェア（機能レベル11_0以上が必須）で使用可能だが、Root Signatureに関する機能はDirectX 11.3では使用できず、DirectX 12専用の機能となる\[32\]。また、ROV (Rasterizer Order View) に関するオブジェクトは、ROV対応ハードウェアでしか使用できない\[33\]。

シェーダーモデル6.0\[34\]の組み込み関数は機能レベル12_0の要件として追加されている。

### ピクセルシェーダーの比較

|                                                              | PS 1.0-1.3 | PS 1.4    | PS 2.0  | PS 2.0a | PS 2.0b | PS 3.0\[35\] | PS 4.0\[36\], 4.1, 5.0 |
| ------------------------------------------------------------ | ---------- | --------- | ------- | ------- | ------- | ------------ | ---------------------- |
| 依存テクスチャ制限                                                    | 4          | 6         | 8       | 無制限     | 4       | 無制限          | 無制限                    |
| テクスチャ命令制限                                                    | 4          | 6\*2      | 32      | 無制限     | 無制限     | 無制限          | 無制限                    |
| Position register                                            | No         | No        | No      | No      | No      | Yes          | Yes                    |
| 命令スロット数                                                      | 8 + 4      | 8 + 4     | 32 + 64 | 512     | 512     | ≥ 512        | ≥ 65536                |
| 実行命令数                                                        | 8+4        | 6\*2+8\*2 | 32 + 64 | 512     | 512     | 65536        | 無制限                    |
| テクスチャの[間接参照](https://ja.wikipedia.org/wiki/間接参照 "wikilink")数 | 4          | 4         | 4       | 無制限     | 4       | 無制限          | 無制限                    |
| Interpolated registers                                       | 2 + 8      | 2 + 8     | 2 + 8   | 2 + 8   | 2 + 8   | 10           | 32                     |
| 命令予測                                                         | No         | No        | No      | Yes     | No      | Yes          | No                     |
| Index input registers                                        | No         | No        | No      | No      | No      | Yes          | Yes                    |
| 一時レジスタ(Temp registers)                                       | 2          | 6         | 12から32  | 22      | 32      | 32           | 4096                   |
| 定数レジスタ(Constant registers)                                   | 8          | 8         | 32      | 32      | 32      | 224          | 16x4096                |
| Arbitrary                                                    | No         | No        | No      | Yes     | No      | Yes          | Yes                    |
| Gradient instructions                                        | No         | No        | No      | Yes     | No      | Yes          | Yes                    |
| Loop count register                                          | No         | No        | No      | No      | No      | Yes          | Yes                    |
| Face register (2-sided lighting)                             | No         | No        | No      | No      | No      | Yes          | Yes                    |
| 動的フロー制御                                                      | No         | No        | No      | No      | No      | 24           | Yes                    |
| ビット演算                                                        | No         | No        | No      | No      | No      | No           | Yes                    |
| 整数演算                                                         | No         | No        | No      | No      | No      | No           | Yes                    |

  - **PS 2.0** = DirectX 9.0オリジナルの**シェーダーモデル2.0**仕様。
  - **PS 2.0a** = [NVIDIA GeForce](../Page/NVIDIA_GeForce.md "wikilink") FXに最適化されたモデル。
  - **PS 2.0b** = [ATI Radeon X700, X800, X850のシェーダーモデル](https://ja.wikipedia.org/wiki/AMD_Radeon#R400_世代_\(X7xx/X8xx\) "wikilink")（DirectX 9.0b）。
  - **PS 3.0** = **シェーダーモデル3.0**に含まれる。
  - **PS 4.0** = **シェーダーモデル4.0**に含まれる。
  - **PS 4.1** = **シェーダーモデル4.1**に含まれる。
  - **PS 5.0** = **シェーダーモデル5.0**に含まれる。

*実行命令数*において"32 + 64"というのは"32のテクスチャ命令と64の算術命令"を意味する。

### 頂点シェーダーの比較

|                                                                                             | VS 1.1 | VS 2.0 | VS 2.0a | VS 3.0\[37\] | VS 4.0\[38\], 4.1, 5.0 |
| ------------------------------------------------------------------------------------------- | ------ | ------ | ------- | ------------ | ---------------------- |
| 命令スロット数                                                                                     | 128    | 256    | 256     | ≥ 512        | 4096                   |
| 最大命令実行数                                                                                     | 不明     | 65536  | 65536   | 65536        | 65536                  |
| 命令予測                                                                                        | No     | No     | Yes     | Yes          | Yes                    |
| 一時レジスタ(Temp registers)                                                                      | 12     | 12     | 13      | 32           | 4096                   |
| 定数レジスタ(Constant registers)                                                                  | ≥ 96   | ≥ 256  | ≥ 256   | ≥ 256        | 16x4096                |
| 静的フロー制御                                                                                     | 不明     | Yes    | Yes     | Yes          | Yes                    |
| 動的フロー制御                                                                                     | No     | No     | Yes     | Yes          | Yes                    |
| 動的フロー制御の深度                                                                                  | No     | No     | 24      | 24           | Yes                    |
| Vertex Texture Fetch                                                                        | No     | No     | No      | Yes          | Yes                    |
| テクスチャサンプラーの数                                                                                | N/A    | N/A    | N/A     | 4            | 128                    |
| [Geometry instancing](https://ja.wikipedia.org/wiki/Geometry_instancing "wikilink") support | No     | No     | No      | Yes          | Yes                    |
| ビット演算                                                                                       | No     | No     | No      | No           | Yes                    |
| 整数演算                                                                                        | No     | No     | No      | No           | Yes                    |

  - **VS 2.0** = DirectX 9.0オリジナルの**シェーダーモデル2.0**仕様。
  - **VS 2.0a** = NVIDIA GeForce FXに最適化されたモデル。
  - **VS 3.0** = **シェーダーモデル3.0**に含まれる。
  - **VS 4.0** = **シェーダーモデル4.0**に含まれる。
  - **VS 4.1** = **シェーダーモデル4.1**に含まれる。
  - **VS 5.0** = **シェーダーモデル5.0**に含まれる。

なおVS 2.0bは存在しない\[39\]。

### 対応ハードウェアの概略

以下の表はDirect3Dプログラマブルシェーダーに対応している各社グラフィックスカードの概略であり、対応するピクセルシェーダーバージョンとDirectXのバージョンを示している。グラフィックスチップは前述のとおり、一般的には上位[互換性](../Page/互換性.md "wikilink")がある。例えばPS 3.0対応のチップはPS 2.0やPS 1.1にも対応している。

なお開発に専用APIやOpenGL/GLSLを使用するゲーム専用機やモバイル機器は、たとえプログラマブルシェーダー対応であってもDirect3D/HLSLに対応しているとは限らないが、グラフィックスチップの世代を示すときは便宜上シェーダーモデルを使うことがある。

| PS version | [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") version | [3Dlabs](https://ja.wikipedia.org/wiki/3Dlabs "wikilink")                          | [AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") (旧[ATI](../Page/ATI_Technologies.md "wikilink")) | [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")                                               | [Matrox](../Page/Matrox.md "wikilink")                            | [NVIDIA](../Page/NVIDIA.md "wikilink")                                                                                                                                       | [S3 Graphics](../Page/S3_Graphics.md "wikilink")                                                                                                                                                    | [SiS](https://ja.wikipedia.org/wiki/SiS "wikilink") | [XGI](../Page/XGI_Technology_Inc..md "wikilink")                                                                                 |
| ---------- | ------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| 1.0/1.1    | 8.0                                                                 | \-                                                                                 | \-                                                                                                                 | \-                                                                                                  | \-                                                                | [GeForce 3 series](https://ja.wikipedia.org/wiki/GeForce#GeForce3 "wikilink")                                                                                                | \-                                                                                                                                                                                                  | Xabre-Series                                        | \-                                                                                                                               |
| 1.2        | 8.0a                                                                | [Wildcat VP](https://ja.wikipedia.org/wiki/3DLabs_Wildcat_VP "wikilink")           | \-                                                                                                                 | \-                                                                                                  | \-                                                                | \-                                                                                                                                                                           | \-                                                                                                                                                                                                  | \-                                                  | \-                                                                                                                               |
| 1.3        | 8.0a                                                                | \-                                                                                 | \-                                                                                                                 | \-                                                                                                  | [Parhelia](../Page/Parhelia.md "wikilink")-Series                 | [GeForce 4 Ti/Go series](https://ja.wikipedia.org/wiki/GeForce#GeForce4 "wikilink")                                                                                          | \-                                                                                                                                                                                                  | Mirage 2（ソフトウェアエミュレーションで対応）                         | \-                                                                                                                               |
| 1.4        | 8.1                                                                 | \-                                                                                 | [Radeon R200 (8500-9250)](../Page/AMD_Radeon.md "wikilink")                                                        | \-                                                                                                  | \-                                                                | \-                                                                                                                                                                           | \-                                                                                                                                                                                                  | Mirage 3                                            | [Volari V3 series](https://ja.wikipedia.org/wiki/XGI_Volari "wikilink") （V3XTを除く）                                                |
| 2.0        | 9.0                                                                 | [Wildcat Realizm](https://ja.wikipedia.org/wiki/3DLabs_Wildcat_Realizm "wikilink") | [Radeon R300 (9500-9800, X300-X600)](../Page/AMD_Radeon.md "wikilink")                                             | [Intel GMA](https://ja.wikipedia.org/wiki/Intel_GMA "wikilink") 900                                 | \-                                                                | [GeForce FX Series](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_FX "wikilink")                                                                                      | [DeltaChrome](../Page/S3_Chrome.md "wikilink"), [GammaChrome](../Page/S3_Chrome.md "wikilink"), [Chrome S2x series](../Page/S3_Chrome.md "wikilink"), [Chrome9 HC](../Page/S3_Chrome.md "wikilink") | Mirage 3+                                           | [Volari V3XT, Volari V5 series, Volari V8 series, Volari 8300, Volari XP10](https://ja.wikipedia.org/wiki/XGI_Volari "wikilink") |
| 2.0a       | 9.0a                                                                | \-                                                                                 | \-                                                                                                                 | \-                                                                                                  | \-                                                                | [GeForce FX Series](https://ja.wikipedia.org/wiki/NVIDIA_GeForce#GeForce_FX "wikilink")                                                                                      | \-                                                                                                                                                                                                  | \-                                                  | \-                                                                                                                               |
| 2.0b       | 9.0b                                                                | \-                                                                                 | [Radeon R420 (X700-X850)](../Page/AMD_Radeon.md "wikilink")                                                        | \-                                                                                                  | \-                                                                | \-                                                                                                                                                                           | \-                                                                                                                                                                                                  | \-                                                  | \-                                                                                                                               |
| 3.0        | 9.0c                                                                | \-                                                                                 | [Radeon X1xxx](https://ja.wikipedia.org/wiki/RADEON#DirectX_9.0c世代のRADEON "wikilink")                              | [Intel GMA](https://ja.wikipedia.org/wiki/Intel_GMA "wikilink") 950（3.0はソフトウェアエミュレーション）, 3000, 3100 | [M Series](https://ja.wikipedia.org/wiki/Matrox_Mシリーズ "wikilink") | [GeForce 6 series](https://ja.wikipedia.org/wiki/GeForce#GeForce_6_Series "wikilink"), [GeForce 7 series](https://ja.wikipedia.org/wiki/GeForce#GeForce_7_Series "wikilink") | \-                                                                                                                                                                                                  | \-                                                  | \-                                                                                                                               |
| 4.0        | 10                                                                  | \-                                                                                 | [Radeon HD 2xxx](https://ja.wikipedia.org/wiki/RADEON#DirectX_10世代のRADEON "wikilink")                              | [Intel GMA](https://ja.wikipedia.org/wiki/Intel_GMA "wikilink") X3100以降のシリーズ                        | \-                                                                | [GeForce 8 series](https://ja.wikipedia.org/wiki/GeForce#GeForce_8_Series "wikilink"), [GeForce 9 series](https://ja.wikipedia.org/wiki/GeForce#GeForce_9_Series "wikilink") | \-                                                                                                                                                                                                  | \-                                                  | \-                                                                                                                               |
| 4.1        | 10.1                                                                | \-                                                                                 | [Radeon HD 3xxx, Radeon HD 4xxx](https://ja.wikipedia.org/wiki/RADEON#DirectX_10.1世代のRADEON "wikilink")            | [HD Graphics 2000/3000](https://ja.wikipedia.org/wiki/Intel_HD_Graphics "wikilink")                 | \-                                                                | [GeForce GT 200 Series](https://ja.wikipedia.org/wiki/GeForce#GeForce_GT_200_Series "wikilink")                                                                              | [Chrome400/500](../Page/S3_Chrome.md "wikilink")                                                                                                                                                    | \-                                                  | \-                                                                                                                               |
| 5.0        | 11                                                                  | \-                                                                                 | [Radeon HD 5xxx](https://ja.wikipedia.org/wiki/AMD_Radeon#Evergreen_世代_\(HD_5xxx\) "wikilink")                     | [HD Graphics 2500/4000](https://ja.wikipedia.org/wiki/Intel_HD_Graphics "wikilink")                 | \-                                                                | [GeForce GTX 400 Series](https://ja.wikipedia.org/wiki/GeForce#GeForce_400_Series "wikilink")                                                                                | \-                                                                                                                                                                                                  | \-                                                  | \-                                                                                                                               |
|            |                                                                     |                                                                                    |                                                                                                                    |                                                                                                     |                                                                   |                                                                                                                                                                              |                                                                                                                                                                                                     |                                                     |                                                                                                                                  |

#### Shader Model 1.x

  - DirectX 8.x世代。
  - [NVIDIA](../Page/NVIDIA.md "wikilink")と[ATI](https://ja.wikipedia.org/wiki/ATI "wikilink")が際限なく機能拡張を行なった頃のモデル。1.1、1.2、1.3、1.4のマイナーバージョンが存在する。
  - 対応GPU: [AMD Radeonは](../Page/AMD_Radeon.md "wikilink")8xxx、[NVIDIA GeForceは](../Page/NVIDIA_GeForce.md "wikilink")3-4Tiシリーズ。
  - ゲーム機である[Xbox用GPUはSM](../Page/Xbox_\(ゲーム機\).md "wikilink")1.x、またはその派生版と見られる。

#### Shader Model 2.0

  - DirectX 9世代。

  - 。

  - NVIDIA拡張である2.0aと、ATI拡張である2.0bが存在する。

  - 対応GPU: Radeonは9500-X850、GeForceはFX 5xxxシリーズ。

#### Shader Model 3.0

  - DirectX 9.0c世代。
  - このバージョンより、シェーダープログラム長の制限がほぼ無くなった。
  - 対応GPU: RadeonはX1000シリーズ、GeForceは6、7シリーズ。
  - ゲーム機である[Xbox 360](../Page/Xbox_360.md "wikilink")、[プレイステーション3用GPUは](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")、SM3.0またはその派生版と思われる。

#### Shader Model 4.x

  - DirectX 10.x世代。
  - 統合型シェーダーアーキテクチャの採用。なお、GPGPU用APIの[CUDA](../Page/CUDA.md "wikilink")や[OpenCL](../Page/OpenCL.md "wikilink")に対応するのはSM 4.0世代以降である。
  - 定数レジスタ（定数バッファ）容量の大幅な拡張。
  - ジオメトリシェーダーの追加。
  - 追加のテクスチャ命令などをサポートするマイナーバージョン4.1が存在する\[40\]。
  - 対応GPU: RadeonはHD 2xxx-HD 4xxxシリーズ、GeForceは8xxx-GT 3xxシリーズ。
  - ゲーム機である[Wii U用GPUは](https://ja.wikipedia.org/wiki/Wii_U "wikilink")、SM4.0またはその派生版と思われる\[41\]。

#### Shader Model 5.0

  - DirectX 11.x世代。
  - ハルシェーダー、ドメインシェーダー、固定機能テッセレータが含まれるテッセレーションステージの追加、および[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")機能であるコンピュートシェーダー（[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")）の対応など。
  - 対応GPU: RadeonはHD 5xxx-HD 8xxx、Rx 2xx/3xxシリーズ、GeForceはFermi、Kepler、Maxwell第1世代。
  - ゲーム機である[Xbox One](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")、[PlayStation 4用GPUは](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")、SM5.0またはその派生版と思われる\[42\]。

#### Shader Model 6.0

  - DirectX 12世代。
  - 対応GPU: RadeonはGCN第2世代以降、GeForceはMaxwell第2世代以降。

なお[OpenGL](../Page/OpenGL.md "wikilink")対応レベルに関しては、ナンバリングがDirectXのバージョンやシェーダーモデルと正確に対応するわけではなく、細かい機能における差異が多数存在するが、世代としてはおおよそ下記の通りとなる。

  - OpenGL 2.x - Direct3D 9
  - OpenGL 3.x - Direct3D 10
  - OpenGL 4.x - Direct3D 11

## 関連項目

  - [Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")
  - [Direct3D](../Page/Direct3D.md "wikilink")
  - [DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")
  - [GLSL](../Page/GLSL.md "wikilink")
  - [Cg (プログラミング言語)](../Page/Cg_\(プログラミング言語\).md "wikilink")

## 脚注

## 外部リンク

  - \[<http://msdn.microsoft.com/en-us/library/windows/desktop/bb509561(v=vs.85>).aspx HLSL (Windows) - MSDN\]
  - [上位レベル シェーダ言語 - MSDN](http://msdn.microsoft.com/ja-jp/library/ff637626.aspx)
  - [HYPERでんち(shadermodel)](http://dench.flatlib.jp/shadermodel)
  - [Cutting Edge DX9 川西 裕幸のコラム](http://www.microsoft.com/japan/msdn/directx/japan/dx9/default.aspx)

[Category:DirectX](https://ja.wikipedia.org/wiki/Category:DirectX "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  [Writing HLSL Shaders in Direct3D 9 (Windows)](http://msdn.microsoft.com/en-us/library/windows/desktop/bb944006.aspx)
2.  [上位レベル シェーダ言語 - MSDN](http://msdn.microsoft.com/ja-jp/library/ff637626.aspx)
3.  [HLSL - MSDN](http://msdn.microsoft.com/ja-jp/library/ee418149.aspx)
4.  [Shader Models vs Shader Profiles - MSDN](http://msdn.microsoft.com/en-us/library/windows/desktop/bb509626.aspx)
5.  [［GDC 2016］シェーダモデル6.0がやってくる！ Microsoftが語った「次のDirectX」 - 4Gamer.net](http://www.4gamer.net/games/033/G003329/20160317117/)
6.  [HLSL Shader Model 6.0 (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/mt733232.aspx)
7.  [Direct3D 9 から Direct3D 10 への移行時の考慮事項 (Direct3D 10)](http://msdn.microsoft.com/ja-jp/library/bb205073.aspx)
8.  [動的リンク](https://msdn.microsoft.com/ja-jp/library/ee422094.aspx)
9.  [.hlsli Extension - List of programs that can open .hlsli files](http://extension.nirsoft.net/hlsli)
10. [Direct3D 9 でのシェーダーの使用](https://msdn.microsoft.com/ja-jp/library/ee418527.aspx)
11. [HLSL, FXC, and D3DCompile – Games for Windows and the DirectX SDK](https://blogs.msdn.microsoft.com/chuckw/2012/05/07/hlsl-fxc-and-d3dcompile/)
12. [Unity - Unity Manual](http://docs-jp.unity3d.com/Documentation/Manual/ComputeShaders.html)
13. [Microsoft/DirectXShaderCompiler: This repo hosts the source for the DirectX Shader Compiler which is based on LLVM/Clang.](https://github.com/Microsoft/DirectXShaderCompiler)
14. [ShaderEffect クラス (System.Windows.Media.Effects)](http://msdn.microsoft.com/ja-jp/library/system.windows.media.effects.shadereffect%28v=vs.90%29.aspx)
15. [ShaderEffect クラス (System.Windows.Media.Effects)](https://msdn.microsoft.com/ja-jp/library/system.windows.media.effects.shadereffect%28v=vs.100%29.aspx)
16. [WPF Version 4 の新機能](https://msdn.microsoft.com/ja-jp/library/bb613588%28v=vs.100%29.aspx)
17. [Effects (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/hh973240.aspx)
18. [シェーダー モデルとシェーダー プロファイル](http://msdn.microsoft.com/ja-jp/library/ee418332.aspx)
19. [Direct3D 10 でのシェーダーの使用](https://msdn.microsoft.com/ja-jp/library/bb509703.aspx)
20. [3Dグラフィックス・マニアックス (4) GPUとシェーダ技術の基礎知識(4) | マイナビニュース](http://news.mynavi.jp/column/graphics/004/)
21. [【4Gamer.net】［特集］ATIとNVIDIAが語る2005＆2006年 ATI編](http://www.4gamer.net/specials/2005-2006_ati/2005-2006_ati.shtml)
22. [テッセレーション (Direct3D 9)](https://msdn.microsoft.com/ja-jp/library/bb206188.aspx)
23. [4Gamer.net AMD，コードネーム「R600」こと「ATI Radeon HD 2000」を発表](http://www.4gamer.net/news/history/2007.05/20070514130104detail.html)
24. [［連載］［西川善司の3Dゲームエクスタシー］「ATI Radeon HD 2000」シリーズのGPUアーキテクチャ徹底解説](http://www.4gamer.net/specials/3de/radeon_hd_2000/radeon_hd_2000_04.shtml)
25. [Game Developers Conference（GDC） 2010現地レポート - GAME Watch](http://game.watch.impress.co.jp/docs/series/3dcg/20100310_353969.html)
26. ["PDC 2008: メインストリーム アプリケーション向け Direct3D10", Microsoft Corporation, 2008年10月](http://download.microsoft.com/download/6/1/4/6143C6AF-9173-41F3-8981-761AE28E85FD/PDC08_D3D10_for_Mainstream_Applications_JPN.docx)
27. [D3D_FEATURE_LEVEL enumeration](http://msdn.microsoft.com/en-us/library/windows/desktop/ff476329.aspx)
28. [Direct3D feature levels](http://msdn.microsoft.com/en-us/library/windows/desktop/ff476876.aspx)
29. [ダウンレベルのハードウェア上の Direct3D 11](http://msdn.microsoft.com/ja-jp/library/ee422082.aspx)
30. [10Level9 リファレンス](http://msdn.microsoft.com/ja-jp/library/ee416164.aspx)
31. [Shader Model 5.1](https://msdn.microsoft.com/en-us/library/windows/desktop/dn933277.aspx)
32. [HLSL Shader Model 5.1 Features for Direct3D 12](https://msdn.microsoft.com/en-us/library/windows/desktop/dn933267.aspx)
33. [Hardware Feature Levels](https://msdn.microsoft.com/en-us/library/windows/desktop/mt186615.aspx)
34. [HLSL Shader Model 6.0 (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/mt733232.aspx)
35. [Shader Model 3.0, Ashu Rege, NVIDIA Developer Technology Group, 2004.](ftp://download.nvidia.com/developer/presentations/2004/GPU_Jackpot/Shader_Model_3.pdf)
36. [The Direct3D 10 System, David Blythe, Microsoft Corporation, 2006.](http://www.cs.cmu.edu/afs/cs/academic/class/15869-f11/www/readings/blythe06_d3d10.pdf)
37.
38.
39. ["Shader Model 3.0 Unleashed", Randima (Randy) Fernando, NVIDIA Developer Technology Group](ftp://download.nvidia.com/developer/presentations/2004/SIGGRAPH/Shader_Model_3_Unleashed.pdf)
40. [テクスチャー オブジェクト (DirectX HLSL)](https://msdn.microsoft.com/ja-jp/library/bb509700.aspx)
41.
42.