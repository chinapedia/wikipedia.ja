> この記事は[Direct3D](https://ja.wikipedia.org/wiki/Direct3D)から翻訳されています。


**Direct3D**は、[3Dグラフィックスを描画するための](../Page/3次元コンピュータグラフィックス.md "wikilink")[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")の一部であり、様々な[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（主に[Windows 95以上](../Page/Microsoft_Windows_95.md "wikilink")）で動作し、さらに、家庭用ゲーム機である[Xbox](../Page/Xbox_\(ゲーム機\).md "wikilink")、[Xbox 360および](../Page/Xbox_360.md "wikilink")[Xbox OneのグラフィックスAPIのベースでもある](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")。略称として**D3D**がよく使われる。

## 概要

Direct3Dはゲームのようなパフォーマンスが重要なアプリケーションで利用される。そのためもあり、ウィンドウ表示だけでなく全画面（フルスクリーン）表示での実行も可能となっている。[グラフィックスボード](https://ja.wikipedia.org/wiki/グラフィックスボード "wikilink")や[CPU](../Page/CPU.md "wikilink")内蔵[GPUなど](../Page/Graphics_Processing_Unit.md "wikilink")、Direct3Dに対応したグラフィックスデバイスが搭載されているシステムであれば、[ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")を利用し、3Dのレンダリングパイプラインの全体または一部がハードウェアによって高速化される。Direct3Dは[Zバッファ](../Page/Zバッファ.md "wikilink")、ステンシルバッファ、裏面カリング、視錐台 (frustum) カリング、[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")、[アルファチャンネル](../Page/アルファチャンネル.md "wikilink")、[アルファブレンディング](https://ja.wikipedia.org/wiki/アルファブレンディング "wikilink")、[ミップマップ](https://ja.wikipedia.org/wiki/ミップマップ "wikilink")、パースペクティブ補正[テクスチャマッピング](../Page/テクスチャマッピング.md "wikilink")、[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")、[テッセレーション](https://ja.wikipedia.org/wiki/テッセレーション "wikilink")といった3Dグラフィックスハードウェアの先進的なグラフィックス機能を利用できる。他のDirectXのテクノロジとの統合により、インタラクティブなメディアタイトルで2Dと3Dを用いて、ビデオマッピング、2Dの[オーバーレイ](https://ja.wikipedia.org/wiki/オーバーレイ "wikilink")プレーンへのハードウェア3Dレンダリング、[スプライトといったような機能をDirect](../Page/スプライト_\(映像技術\).md "wikilink")3Dは実行できる。

Direct3Dは[3D](../Page/3次元コンピュータグラフィックス.md "wikilink") APIである。つまり、3Dレンダリングのための様々なコマンドが含まれるということであるが、Direct3Dのバージョン8より、古い[DirectDraw](../Page/DirectDraw.md "wikilink")のフレームワークと置き換えられ、また[2Dグラフィックスの機能も引き継いでいる](../Page/2次元コンピュータグラフィックス.md "wikilink")\[1\]\[2\]。マイクロソフトは3Dグラフィックスカードで利用できる最新のテクノロジをサポートすべくDirect3Dを継続して更新し続けている。Direct3Dは完全な頂点処理のソフトウェアエミュレーションを提供するが、ハードウェアがサポートしていないピクセル処理のソフトウェアエミュレーションはない。例えば、もしDirect3Dを使ってプログラムされたソフトウェアが[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")を必要として、そしてユーザーのコンピュータのビデオカードがその機能をサポートしないなら、Direct3Dはそれを[エミュレートしない](../Page/エミュレータ.md "wikilink")。代わりに、APIは一般的なグラフィックスカードをCPUで完全エミュレートするリファレンスラスタライザ（またはREFデバイス）を定義する。ただし、[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")をCPUでエミュレーションするのはどんなアプリケーションでも使用に耐えないくらい遅く、製品版アプリケーションでの使用は想定されていない\[3\]。一方、Direct3D 10.1 API以降は比較的高速なソフトウェアデバイスとしてが実装されており、グラフィックスハードウェアがDirect3Dの機能レベルを十分にサポートしない場合でもカジュアルな用途であれば実用に耐えうるDirect3Dアプリケーションを作成・実行できる\[4\]。

Direct3D 11.xまでの主な競合相手は[OpenGL](../Page/OpenGL.md "wikilink")である。2つのAPIには考え方の合わない数多くの機能と問題がある。[:en:Comparison of Direct3D and OpenGLを参照のこと](https://ja.wikipedia.org/wiki/:en:Comparison_of_Direct3D_and_OpenGL "wikilink")。OpenGL 4以降はDirect3Dからの移植を容易にするため、Direct State AccessなどのDirect3Dの設計思想に近い機能も取り入れるようになっている。Direct3D 12はハードウェア抽象化層を薄くしたローレベルAPIとして大幅に再設計され、競合は[Metalや](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")[Vulkanである](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")。

## アーキテクチャ

[thumb](https://ja.wikipedia.org/wiki/ファイル:D3D_Abstract_Layer_\(en\).png "wikilink") Direct3DはMicrosoftの[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") APIのサブシステムコンポーネントである。グラフィックスアプリケーションとグラフィックハードウェアデバイスの間の通信を抽象化することがDirect3Dの目的である。これは[GDIと比較して薄い](../Page/Graphics_Device_Interface.md "wikilink")[抽象化レイヤー](../Page/抽象化レイヤー.md "wikilink")となっている（図参照）。[COMベースのアーキテクチャによりDirect](../Page/Component_Object_Model.md "wikilink")3Dはディスプレイドライバと直接接続しており、GDIと比べてレンダリングのパフォーマンスで優れた結果を得られるところがGDIとDirect3Dの最も大きな違いである。なお、図は[Windows XP](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")/Direct3D 9までの古いモデル (XPDM) であり、[Windows Vista](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")/Direct3D 9Ex以降ではさらにDirectX/Direct3DがOSのグラフィックス根幹機能へと昇格され、GDIはすでにDirectX/Direct3Dと独立・同列ではなくなり、DirectXランタイム（[DXGIと呼ばれるDirect](https://ja.wikipedia.org/wiki/DirectX_Graphics_Infrastructure "wikilink")3Dベースのグラフィックス基盤）上にて動作することになる ([WDDM](https://ja.wikipedia.org/wiki/Windows_Display_Driver_Model "wikilink"))\[5\]。

Direct3Dは"イミディエイトモード"（IM: 直接モード）のグラフィックスAPIである。これは各ビデオカードの3D機能（[平行移動](https://ja.wikipedia.org/wiki/平行移動 "wikilink")、クリッピング、光源、マテリアル、テクスチャ、[深度バッファなど](../Page/Zバッファ.md "wikilink")）に低レベルなインターフェイスを提供する。またDirect3D 7までは"リテインドモード"（RM: 保持モード）という高レベルのコンポーネントもあった\[6\]が、Direct3D 8以降では廃止されている。

Direct3Dのイミディエイトモードは「デバイス」、「リソース」、「スワップチェーン」の3つの主要な抽象化を提供する（図参照）。「デバイス」は描画に必要な処理を行うソフトウェア・ハードウェアを指す概念であり、アプリケーションは「デバイスタイプ」\[7\]を指定することにより、デバイスにアクセスすることができる。

  - **HAL** (*hardware abstraction layer*) デバイス\[8\]
    ユーザーのコンピュータに搭載されたハードウェアアクセラレータを使用して処理を行う。ハードウェアアクセラレーションをサポートする場合、Direct3Dのコードはハードウェアの速度で動作可能。

[thumb](https://ja.wikipedia.org/wiki/ファイル:D3D_Device_\(en\).png "wikilink")

  - リファレンスデバイス
    Direct3Dのほとんどの機能を忠実に実装しているが、パフォーマンスが非常に低いソフトウェアレンダラーを選択する。このデバイスタイプを利用するためにはDirect3Dの[SDKを事前にインストールする必要がある](../Page/ソフトウェア開発キット.md "wikilink")。
  - ヌルリファレンスデバイス
    これは何もせず真っ暗な画面を表示する。このデバイスはSDKがインストールされていないのにリファレンスデバイスが要求された場合に使用される。
  - プラグ可能ソフトウェアデバイス
    ソフトウェアラスタライゼーションを実行するために利用される。ソフトウェアレンダラーはDirect3Dには内蔵されていないため、アプリケーションはこれを選択するには独自のソフトウェアレンダラーをDirect3Dに登録する必要がある\[9\]。マイクロソフトが公式にソフトウェアレンダラーを配布している\[10\]。

各デバイスは最低1つの「スワップチェーン」を含む。スワップチェーンは1つ以上のバック[バッファ](../Page/バッファ.md "wikilink")サーフェス（ピクセルデータの長方形の集合と、そのピクセルの色、深さ、ステンシル、アルファ、テクスチャなどの属性）で構成される。Direct3D描画コマンドによってレンダリングはバックバッファのどこかに行なわれ、最後にPresent処理によってバックバッファからフロントバッファにピクセルデータが転送されることで画面表示が完了する。

さらにデバイスもまた「リソース」のコレクションを含む。リソースはレンダリング中に使用される特定のデータである。各リソースは4つの属性を持つ。

  - Type
    サーフェス、ボリューム、テクスチャ、キューブテクスチャ、ボリュームテクスチャ、サーフェステクスチャ、インデックスバッファ、頂点バッファなど、リソースの種類を定義する。

  - Pool\[11\]<ref>{{cite web

|url=<http://www.toymaker.info/Games/html/d3d_resources.html#MemoryPool> |title=Direct3D Resources - Memory pool|accessdate=2008-05-04 }}</ref>

  -
    実行時にリソースがどのように管理され、どこに保存されるのかを定義する。**Default**プールはリソースがデバイスメモリ内にのみ存在することを意味している。**Managed**プールはリソースがシステムメモリに確保され必要時にデバイスへ送られることを意味している。**System Memory**プールはリソースがシステムメモリ内にのみ存在することを意味している。**Scratch**プールはシステムメモリプールと同一であるが、この場合はリソースがハードウェアの制約に縛られない。

  - Format
    リソースのメモリ内でのレイアウト、主にピクセルデータのレイアウトを定義する。例えば*D3DFMT_R8G8B8*フォーマットは24ビットの[色深度](../Page/色深度.md "wikilink")を意味する（赤8bit、緑8bit、青8bit）。

  - Usage:[フラグビットの集合によりアプリケーションがリソースをどのように使うのかを定義する](../Page/フラグ_\(コンピュータ\).md "wikilink")。これらのフラグはリソースを動的にアクセスするのか静的にアクセスするのかを知るために利用される。静的リソースの値はロード後に変更できないのに対し、動的リソースの値は繰り返し変更することができる。

## パイプライン

[thumb](https://ja.wikipedia.org/wiki/ファイル:D3D_Pipeline.svg "wikilink") Direct3D 10のパイプライン\[12\] は下記のステージで構成される\[13\]\[14\]。

1.  **インプット アセンブラー**: パイプラインにデータを提供する。
2.  **[バーテックスシェーダー](https://ja.wikipedia.org/wiki/バーテックスシェーダー "wikilink")**: 行列演算、スキニング、頂点ライティングといった単一の頂点処理を実行する。頂点シェーダーとも呼ばれる。
3.  **[ジオメトリシェーダー](https://ja.wikipedia.org/wiki/ジオメトリシェーダー "wikilink")**: 頂点シェーダーの出力である、プリミティブ全体（三角形、直線または頂点）を処理する。それらのエッジ隣接プリミティブを処理することもある。プリミティブが与えられ、このステージでこれを取り除いたり新しいプリミティブを生成したりする。
4.  **ストリーム アウトプット**: 前のステージの結果をメモリに保存する。データをリサイクルしてパイプラインに戻すことは有用である。
5.  **ラスタライザー**: プリミティブをピクセルにラスタライズし、見えないところはクリッピングする。
6.  **[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")**: ラスタライザーの出力、すなわち各ピクセルの色などを制御・決定する。ライティングをこのピクセルシェーダーで行なうこともある（[:en:Per-pixel lighting](https://ja.wikipedia.org/wiki/:en:Per-pixel_lighting "wikilink")、ピクセル単位ライティング）。
7.  **アウトプット マージャー**: 最終結果を生成するために様々な形式の出力データ（[ピクセルシェーダ](https://ja.wikipedia.org/wiki/ピクセルシェーダ "wikilink")ーやデプス、ステンシル等）を合成する。

全てのパイプラインステージは自由に組み合わせることができる。

## コード記述例

Direct3DはCOMで実装されており、オブジェクト指向インターフェイスを利用してアプリケーションコードを書くことになる。

  - Direct3D 7（固定機能）で三角形を描画する例。

<!-- end list -->

``` cpp
// 3頂点のポリゴンを表す頂点配列を定義。
// X, Y, Z, Color, Specular, Tu, Tv の順。
// https://msdn.microsoft.com/en-us/library/ms896912.aspx
D3DLVERTEX v[3];
v[0] = D3DLVERTEX(D3DVECTOR(0.0f, +1.0f, 0.5f), 0x00FF0000, 0, 0, 0);
v[1] = D3DLVERTEX(D3DVECTOR(+1.0f, 0.0f, 0.5f), 0x0000FF00, 0, 0, 0);
v[2] = D3DLVERTEX(D3DVECTOR(-1.0f, 0.0f, 0.5f), 0x000000FF, 0, 0, 0);
// 三角形を描画するメソッドの呼び出し。
// pD3DDevice は IDirect3DDevice7 インターフェイスへのポインタ。
pD3DDevice->DrawPrimitive(D3DPT_TRIANGLELIST, D3DFVF_LVERTEX, v, 3, 0);
```

  - Direct3D 9（固定機能）で三角形を描画する例。

<!-- end list -->

``` cpp
// ひとつのカスタム頂点情報を表す構造体。
struct MyLVertex {
  D3DXVECTOR3 Position; // float x3
  D3DCOLOR Color; // unsigned long x1, B8G8R8A8
};

// 3頂点のポリゴンを表す頂点配列を定義。
const MyLVertex vertexArray[] = {
  { D3DXVECTOR3(0.0f, +1.0f, 0.5f), D3DCOLOR_ARGB(255, 255, 0, 0) },
  { D3DXVECTOR3(+1.0f, 0.0f, 0.5f), D3DCOLOR_ARGB(255, 0, 255, 0) },
  { D3DXVECTOR3(-1.0f, 0.0f, 0.5f), D3DCOLOR_ARGB(255, 0, 0, 255) },
};
// 三角形を描画するメソッドの呼び出し。
// pD3DDevice は IDirect3DDevice9 インターフェイスへのポインタ。
pD3DDevice->SetRenderState(D3DRS_LIGHTING, FALSE);
pD3DDevice->SetFVF(D3DFVF_XYZ | D3DFVF_DIFFUSE); // FVF = Flexible Vertex Format の設定。
pD3DDevice->DrawPrimitiveUP(D3DPT_TRIANGLELIST, 1, vertexArray, sizeof(MyLVertex));
```

Direct3D 7では定義済み頂点フォーマットとしていくつかの組み込みの構造体型が準備されていたが、Direct3D 9ではユーザープログラマーによる定義が必須となる。

固定機能グラフィックスでは組み込みのマテリアル特性に応じた陰影計算\[15\]\[16\]やスムージング（[グーローシェーディング](https://ja.wikipedia.org/wiki/グーローシェーディング "wikilink")\[17\]）、ライトの減衰\[18\]あるいはフォグ\[19\]のような大気効果 (atmospheric effects) といった、いくつかのエフェクトをサポートする。

### プログラマブルシェーダー

Direct3D 9のプログラマブルシェーダーを利用する場合は、[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")言語等を使いシェーダープログラムを別途作成して、あらかじめデバイスにセットしてから描画メソッドを呼び出す必要がある。ただし、Direct3D 9の場合は、プログラマブル頂点シェーダーと固定機能ピクセルシェーダーを組み合わせることも可能である。

また、Direct3D 10およびDirect3D 11においてはFVF、ユーザーポインタ頂点配列 (UP) および固定機能シェーダーが存在しないので、必ず頂点レイアウト、頂点バッファおよびシェーダープログラムを作成する必要がある（シーンを描画するためには少なくとも頂点シェーダーとピクセルシェーダーの2つを作成する必要があるが、深度ステンシルのみのレンダリングであればラスタライザーを無効にして頂点シェーダーだけでレンダリングすることもできる\[20\]）。テッセレーションシェーダー（ハルシェーダー、ドメインシェーダー）およびジオメトリシェーダーに関しては必須ではなくオプションであり、またコンピュートシェーダーに関しては描画パイプラインと独立している。

Direct3D 12ではオーバーヘッド低減のため、シェーダープログラムオブジェクトの個別設定は廃止され、パイプラインステートオブジェクト (PSO) としてグラフィックスパイプラインあるいはコンピュートパイプラインごとにすべてのシェーダーステージを各種ステートとともにまとめて事前作成してから設定する方式に変更された\[21\]\[22\]。もちろん固定機能シェーダーは存在しない。

## ディスプレイモード

Direct3Dは2つの異なるディスプレイモードがある。

  - エクスクルーシブモード（排他モード）
    Direct3Dとディスプレイドライバを直接接続するため、Direct3Dデバイスは全画面表示が可能である。アプリケーションがエクスクルーシブモードである間はディスプレイデバイスの使用要求は失敗する。
  - ウィンドウモード
    ウィンドウ内の領域に結果が表示される。Direct3Dは画面を完成させるために[GDIと通信する必要がある](../Page/Graphics_Device_Interface.md "wikilink")。

ウィンドウモードはエクスクルーシブモードよりも若干遅いが、画面を占有しないためその他のGUIと共存させることが可能なほか、外部GUIを必要としない場合においてもデバッグに役立つ。

## 変遷

  - Direct3D (DirectX3～DirectX5)
    レンダリングパイプラインアーキテクチャを採用し、ハードウェア抽象化レイヤー (HAL) とハードウェアエミュレーションレイヤー (HEL) の二種類のレイヤーを持ち、ハードウェア支援が得られない場合もソフトウェアのエミュレーションによって機能するよう設計された。この当時のハードウェアはレンダリングパイプラインのうち、ラスタライズのみがハードウェア化されていた。
  - Direct3D 6.0
    [ドリームキャスト](../Page/ドリームキャスト.md "wikilink")にも採用されたバージョンで、環境バンプマップやトライリニアフィルタリング、ミップマップ、テクスチャ圧縮などをサポートしていた。
  - Direct3D 7.0
    ハードウェアによる座標変換とライティングを行うハードウェアT\&L、一枚のポリゴンに複数のテクスチャを同時に貼るマルチテクスチャやキューブマップをサポートした。
  - Direct3D 8.0
    [Xboxなどに採用されたバージョンで](../Page/Xbox_\(ゲーム機\).md "wikilink")、原始的なプログラマブルシェーダー（アセンブラ）を初めてサポートした。その他にも、ボリュームテクスチャ、マルチサンプルレンダリングをサポート。リファレンスラスタライザ以外のソフトウェアレンダラを廃止。
  - Direct3D 8.1
    [Windows XPに標準搭載されている](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")。プログラマブルシェーダー1.1、1.2、1.3、および1.4をサポートする。
  - Direct3D 9.0
    浮動小数点実数テクスチャ、およびプログラマブルシェーダー2.0をサポートした。また、プログラマブルシェーダーを記述するための高級言語「[HLSL](https://ja.wikipedia.org/wiki/HLSL "wikilink")」に対応した。
  - Direct3D 9.0c
    プログラマブルシェーダー3.0をサポートした。プログラマブルシェーダー3.0は、頂点シェーダーからテクスチャマップにアクセス (VTF) することができるため、ディスプレースメントマッピングなどが実現できる。[Xbox 360](../Page/Xbox_360.md "wikilink") GPUの機能はほぼこのバージョンに準ずる。
  - Direct3D 9.0Ex
    [Windows Vista以降に搭載された](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、[Windows Display Driver Model](https://ja.wikipedia.org/wiki/Windows_Display_Driver_Model "wikilink") (WDDM) に対応するように変更が施されたバージョン。Vistaのデスクトップ描画 (Windows Aero) にはこのD3D 9Exが使用されている。
  - Direct3D 10.0
    共通層であるDirectX グラフィックス インフラストラクチャー (DXGI) を導入したバージョン。Windows Vista以降で動作する。ジオメトリシェーダーなどプログラマブルシェーダー4.0をサポートする一方、固定機能シェーダーおよびCaps (Capabilities) ビットなどを廃止し、またDirect3D 10非対応のハードウェア上では動作しない。
  - Direct3D 10.1
    Direct3D 10.0のマイナーチェンジ。Windows Vista SP1以降で動作する。CapsビットがFeature Levelの形で限定的に復活し、ハードウェアの対応度に応じたFeature Levelで動作させることができる。プログラマブルシェーダー4.1をサポートする。DXGI 1.1に対応した[Windows 7のデスクトップ描画にはこのD](../Page/Microsoft_Windows_7.md "wikilink")3D 10.1が使用されている[1](http://ascii.jp/elem/000/000/438/438414/)。なお、Windows 7に標準搭載されている高速2D描画APIである[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")は、このD3D 10.1上に構築された高レベルラッパーライブラリである。
  - Direct3D 11.0
    Windows Vista SP2 Platform UpdateおよびWindows 7以降で動作する。DXGIのバージョンは1.1となる[2](http://msdn.microsoft.com/ja-jp/library/ee417025.aspx)。プログラマブルシェーダー5.0をサポートし、頂点シェーダーとジオメトリシェーダーの間に、ハードウェア[テッセレーション](https://ja.wikipedia.org/wiki/テッセレーション "wikilink")（[サブディビジョンサーフェイス](https://ja.wikipedia.org/wiki/細分割曲面 "wikilink")）を実現するステージとして、新たにハルシェーダー・テッセレータ・ドメインシェーダーが追加されている。また、[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")用途のシェーダーステージとして、コンピュートシェーダー ([DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")) が追加されている。ハルシェーダーおよびドメインシェーダーはDirect3D 11対応のGPUでなければ使用できないが、コンピュートシェーダーは制限付きでDirect3D 10.x世代のGPUでも実行可能である[3](http://msdn.microsoft.com/ja-jp/library/ee422083.aspx)。
  - Direct3D 11.1
    Direct3D 11.0のマイナーチェンジ。[Windows 8に標準搭載されている](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")。DXGIのバージョンは1.2となる[4](http://msdn.microsoft.com/en-us/library/windows/desktop/hh404490.aspx)。なお、Windows 8に標準搭載される、新しいバージョンのDirect2D (D2D 1.1) は、このD3D 11.1上に構築された高レベルラッパーライブラリである[5](http://msdn.microsoft.com/en-us/library/windows/desktop/hh802478.aspx)。シェーダーモデルのバージョンは11.0と同じく5.0となる[6](http://msdn.microsoft.com/en-us/library/windows/desktop/ff476876.aspx#Overview)。Direct3D 11.1は機能追加よりも性能強化に重点が置かれたマイナーバージョンアップとなっている。また、Direct3D 11はWindows 7リリース後にWindows Vistaに対して完全な形でバックポートされたが、Direct3D 11.1のWindows 7へのバックポートは完全ではなく、限定的な形にとどまっている[7](http://blogs.msdn.com/b/chuckw/archive/2012/11/14/directx-11-1-and-windows-7.aspx)。
  - Direct3D 11.2
    Direct3D 11.1のマイナーチェンジ。[Windows 8.1および](https://ja.wikipedia.org/wiki/Windows_8.1 "wikilink")[Xbox Oneに標準搭載される](https://ja.wikipedia.org/wiki/Xbox_One "wikilink")[8](http://www.4gamer.net/games/033/G003329/20130627026/)。DXGIのバージョンは1.3となる[9](http://msdn.microsoft.com/ja-jp/library/windows/apps/dn448914.aspx)。Windows 8.1に標準搭載される、新しいバージョンのDirect2D (D2D 1.2) は、このD3D 11.2上に構築された高レベルラッパーライブラリである[10](http://msdn.microsoft.com/en-us/library/windows/desktop/hh802478.aspx)。Direct3D 11.2はタイルリソース（いわゆるメガテクスチャ）などをサポートする[11](http://msdn.microsoft.com/en-us/library/windows/desktop/dn312084.aspx)。なお、Direct3D 11.2はWindows 8およびそれ以前のOSにはバックポートされていない。
  - Direct3D 11.3
    Direct3D 12に搭載される新機能は、同時期に提供される従来からの高レベルAPIのマイナーチェンジとなるDirect3D 11.3にも搭載される\[23\]\[24\]\[25\]。DXGIのバージョンは1.4となる\[26\]。
  - Direct3D 11.4
    Windows 10 November 2015 Update (version 1511, build 10586) にてDXGI 1.5とともに導入された\[27\]。
  - Direct3D 12
    高レベルだがオーバーヘッドの大きかったDirect3D 11までと比べて、Direct3D 12はよりハードウェアに近いローレベルな制御を可能とするAPIとなった\[28\]。[Windows 10のほか](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")、Xbox OneおよびWindows Phoneにも対応予定\[29\]。
    Windows 10 Anniversary Update (version 1607, build 14393) にてWDDM 2.1が導入され、Direct3D 12も更新された\[30\]。[UWPアプリケーションにおける可変リフレッシュレートのサポートも追加されている](https://ja.wikipedia.org/wiki/ユニバーサルWindowsプラットフォーム "wikilink")\[31\]。
    Windows 10 October 2018 Update (version 1809, build 17763) にて、 (DXR) に対応した。
    2019年3月、一部のゲームに関して、Windows 7上でDirectX 12 (Direct3D 12) を動作させるためのユーザーモードのランタイムがマイクロソフトから提供されることになった\[32\]。これにより、Direct3D 12にカーネルレベルで完全対応しているWindows 10ほどではないが、Windows 7上でもDirect3D 12のマルチスレッドレンダリングなどによるフレームレート向上の恩恵を得ることができると説明されている。2019年8月にはD3D12onWin7の[NuGet](https://ja.wikipedia.org/wiki/NuGet "wikilink")パッケージが一般公開された\[33\]。

## オープンソース実装

[Wine](../Page/Wine.md "wikilink")では、[Unix系](../Page/Unix系.md "wikilink")OSで[OpenGL](../Page/OpenGL.md "wikilink")をバックエンドに用いてDirect3D APIを実装している。オープンソースのグラフィックスライブラリ[Mesaでは](../Page/Mesa_3D.md "wikilink")、OpenGLを経由しないDirect3Dのネイティブ実装（Gallium NineによるDirect3D 9のネイティブ実装、[Gallium3D](https://ja.wikipedia.org/wiki/Gallium3D "wikilink")によるDirect3D 10/11のネイティブ実装\[34\]）も利用可能となっている。Wine 4.0以降では、変換ライブラリvkd3dを利用して[Vulkan上にDirect](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")3D 12 APIを実現している\[35\]\[36\]。

## 参考文献

<references />

## 関連項目

  - [High Level Shading Language](https://ja.wikipedia.org/wiki/High_Level_Shading_Language "wikilink") - HLSL
  - [Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") - Direct3Dを含むマルチメディアAPIの集合
  - [OpenGL](../Page/OpenGL.md "wikilink") - Direct3Dの競合となるクロスプラットフォームグラフィックスAPI
  - [DirectDraw](../Page/DirectDraw.md "wikilink")
  - [DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")
  - [Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")
  - [DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")
  - [WPF](../Page/Windows_Presentation_Foundation.md "wikilink")
  - [Windows Display Driver Model](https://ja.wikipedia.org/wiki/Windows_Display_Driver_Model "wikilink")
  - [3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")
  - [Metal (API)](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")
  - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")
  - [:en:Direct3D](https://ja.wikipedia.org/wiki/:en:Direct3D "wikilink")
  - [:en:Feature levels in Direct3D](https://ja.wikipedia.org/wiki/:en:Feature_levels_in_Direct3D "wikilink")
  - [Mantle (API)](https://ja.wikipedia.org/wiki/Mantle_\(API\) "wikilink")

## 外部リンク

  - [Microsoft Docs](https://ja.wikipedia.org/wiki/Microsoft_Docs "wikilink")（旧[MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink")ライブラリ）
      - [Direct3D 9 Graphics - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics)
      - [Direct3D 10 Graphics - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d10/d3d10-graphics)
          - [Direct3D 10.1 Features - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d10/d3d10-graphics-programming-guide-10-1)
      - [Direct3D 11 Graphics - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d11/atoc-dx-graphics-direct3d-11)
          - [Direct3D 11.1 Features - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d11/direct3d-11-1-features)
          - [Direct3D 11.2 Features - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d11/direct3d-11-2-features)
          - [Direct3D 11.3 Features - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d11/direct3d-11-3-features)
          - [Direct3D 11.4 Features - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d11/direct3d-11-4-features)
      - [Direct3D 12 graphics - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d12/direct3d-12-graphics)
  - [DirectX Developer Blog](https://devblogs.microsoft.com/directx/)
  - [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")
      - [Microsoft/DirectX-Graphics-Samples · GitHub](https://github.com/Microsoft/DirectX-Graphics-Samples)
      - [Microsoft/DirectXTK · GitHub](https://github.com/Microsoft/DirectXTK)
      - [Microsoft/DirectXTex · GitHub](https://github.com/Microsoft/DirectXTex)
      - [Microsoft/DirectXMesh · GitHub](https://github.com/Microsoft/DirectXMesh)

[Category:DirectX](https://ja.wikipedia.org/wiki/Category:DirectX "wikilink") [Category:3DCG](https://ja.wikipedia.org/wiki/Category:3DCG "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.  [Microsoft DirectX SDK Readme (October 2006)](http://msdn.microsoft.com/directx/sdk/readmepage/default.aspx)
2.  [DirectX 8.0 の紹介](https://msdn.microsoft.com/ja-jp/library/dd148689.aspx)
3.  [D3D_DRIVER_TYPE](https://msdn.microsoft.com/ja-jp/library/ee417659.aspx)
4.  [Windows Advanced Rasterization Platform (WARP) Guide (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/gg615082.aspx)
5.  [Windows Vista のグラフィック API](https://msdn.microsoft.com/ja-jp/library/bb173477.aspx)
6.  [Direct3D Retained Mode for Visual Basic](https://msdn.microsoft.com/ja-jp/library/dd188518.aspx)
7.  [D3DDEVTYPE](https://msdn.microsoft.com/ja-jp/library/bb172547.aspx)
8.  [DirectX 用語集](https://msdn.microsoft.com/ja-jp/library/cc351166.aspx)
9.  [IDirect3D9::RegisterSoftwareDevice](https://msdn.microsoft.com/ja-jp/library/ee421620.aspx)
10.
11. [D3DPOOL](https://msdn.microsoft.com/ja-jp/library/bb172584.aspx)
12.
13.
14. [パイプライン ステージ (Direct3D 10)](https://msdn.microsoft.com/ja-jp/library/ee415715.aspx)
15. [Materials (Direct3D 9) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d9/materials)
16. [Mathematics of Lighting (Direct3D 9) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d9/mathematics-of-lighting)
17. [Shading State (Direct3D 9) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d9/shading-state)
18. [Light Properties (Direct3D 9) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d9/light-properties)
19. [Fog Types (Direct3D 9) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/direct3d9/fog-types)
20. [ラスタライザー ステージ (Direct3D 10)](https://msdn.microsoft.com/ja-jp/library/ee415718.aspx)
21. [Direct3D 12 概要 パート 2: パイプライン状態オブジェクト | iSUS](http://www.isus.jp/article/game-special/direct3d-12-overview-part-2-pipeline-state-object/)
22. [Managing Graphics Pipeline State in Direct3D 12 (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/dn899196)
23. [DirectX 12's new rendering features are coming to DirectX 11.3 too | PC Gamer](http://www.pcgamer.com/2014/09/19/directx-12s-new-rendering-features-are-coming-to-directx-11-3-too/)
24. [DirectX 12 Lights Up NVIDIA’s Maxwell Launch - DirectX Developer Blog - Site Home - MSDN Blogs](http://blogs.msdn.com/b/directx/archive/2014/09/18/directx-12-lights-up-nvidia-s-maxwell-editor-s-day.aspx)
25. [西川善司の3DGE：新しく来るDirectXは「12」だけじゃない。突如浮上した「DirectX 11.3」とは何か？ - 4Gamer.net](http://www.4gamer.net/games/033/G003329/20141020017/)
26. [PC Games for Windows 10](http://video.ch9.ms/files/GDC2015-PCGamesforWindows10.pptx)
27. [Windows 10 SDK (November 2015) – Games for Windows and the DirectX SDK](https://blogs.msdn.microsoft.com/chuckw/2015/11/30/windows-10-sdk-november-2015/)
28. [Direct3D 12 特集 | iSUS](http://www.isus.jp/article/game-special/directx-12/)
29. [【後藤弘茂のWeekly海外ニュース】GPUの進化に対応したMicrosoftの次世代API「DirectX 12」の背景 - PC Watch](http://pc.watch.impress.co.jp/docs/column/kaigai/20140325_641071.html)
30. [New Releases (Windows)](https://msdn.microsoft.com/en-us/library/mt748631.aspx)
31. [Variable refresh rate displays (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/mt742104.aspx)
32. [World of Warcraft uses DirectX 12 running on Windows 7 | DirectX Developer Blog](https://devblogs.microsoft.com/directx/world-of-warcraft-uses-directx-12-running-on-windows-7/)
33. [Porting DirectX 12 games to Windows 7 | DirectX Developer Blog](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
34. [Direct3D 10/11 Is Now Natively Implemented On Linux\! - Phoronix](https://www.phoronix.com/scan.php?page=article&item=mesa_gallium3d_d3d11&num=1)
35. [「Wine 4.0」リリース、VulkanとDirect3D 12をサポート | OSDN Magazine](https://mag.osdn.jp/19/01/24/160000)
36. [source.winehq.org Git - vkd3d.git/summary](https://source.winehq.org/git/vkd3d.git/)