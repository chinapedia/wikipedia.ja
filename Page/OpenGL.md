> この記事は[OpenGL](https://ja.wikipedia.org/wiki/OpenGL)から翻訳されています。


**OpenGL**（オープンジーエル、Open Graphics Library）は、[クロノス・グループ](https://ja.wikipedia.org/wiki/クロノス・グループ "wikilink") () が策定している、グラフィックスハードウェア向けの2次元/3次元[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")ライブラリである。[SGI社内で自社のCGワークステーション向けにクローズドに策定された](../Page/シリコングラフィックス.md "wikilink")[API仕様が改良されて公開され](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、後に大きなシェアを持つに至った。現在は多様な描画デバイスを包括するグラフィックスAPIの[オープン標準](https://ja.wikipedia.org/wiki/オープン標準 "wikilink")規格として策定が行なわれている。

## 概要

OpenGLは、SGIをはじめ、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") (HP)、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")（現[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")）、[IBM](../Page/IBM.md "wikilink")、[SONY-NEWSなどの](https://ja.wikipedia.org/wiki/NEWS_\(ソニー\) "wikilink")[UNIX](../Page/UNIX.md "wikilink")ワークステーションの他、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")などのPC UNIXに加え、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")等で使用できる[クロスプラットフォーム](https://ja.wikipedia.org/wiki/クロスプラットフォーム "wikilink")なグラフィックスAPIである。また、携帯電話、PDA（携帯情報端末）、家電など[組み込み用途向けのサブセット版である](../Page/組み込みシステム.md "wikilink")[OpenGL ES](https://ja.wikipedia.org/wiki/OpenGL_ES "wikilink") (OpenGL for Embedded Systems) 規格も存在する。

[オープン標準](https://ja.wikipedia.org/wiki/オープン標準 "wikilink")として公開され、幅広い処理系に対応しているため、家庭用・業務用問わず広く普及している。描画デバイスの実装を隠蔽する抽象化層として機能するため、移植性が高い。また、描画演算処理をOpenGLに対応する専用ハードウェア ([GPU](../Page/Graphics_Processing_Unit.md "wikilink")) に委ねることで非常に高速に動作し、[CPU](../Page/CPU.md "wikilink")のみによるソフトウェア描画と比較して高フレームレートかつ詳細に3D画像を描画できる。有償・無償の豊富な補助ライブラリがあるのも特色として挙げられる。Windows, Mac OS, Linux, BSD等の様々なOSの上で利用可能であり、個人でも無料のソフトウェア群のみでGPUの能力を最大限に利用できる3Dプログラミング環境を整備できる。開発・実行環境として広範なプラットフォームをサポートすることから、3次元コンピュータグラフィックスの学習や学術研究、クロスプラットフォームな[クローズドソース](https://ja.wikipedia.org/wiki/クローズドソース "wikilink")/[オープンソースソフトウェア](https://ja.wikipedia.org/wiki/オープンソースソフトウェア "wikilink")開発などにも適している。

OpenGL APIは[C言語](../Page/C言語.md "wikilink")関数群の形で提供され、またクロノスグループが策定・公開しているのは、OpenGL API仕様のドキュメントおよび[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")用のヘッダーファイルだが、[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの他言語向けのラッパー／バインディングも存在する\[1\]。

2004年に発表されたOpenGL 2.0で高級[シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink") ([GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")) を標準化するなど、GPUの進化に合わせて多様な機能を持つようになってきている。

。しかし、OpenGL 4.0のリリース以降はGPUの進化に合わせたOpenGL APIの対応が進み、主要な機能に関しては、OpenGL 4.3以降と[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 11 ([Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink") 11) 以降との差異はほとんど無くなっている。とはいえ、OpenGLとDirect3Dは、その設計思想の違いから1対1で対応するものではないため、移植性は完全ではなく、また性能面ではハードウェアおよびドライバーのOpenGL/Direct3D最適化レベルに依存する\[2\]ため、利用分野やプラットフォームに応じた住み分けも依然として根強く残っている。

なお、例えばOpenGL[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")を利用するには特定のバージョン以降のOpenGLに対応したハードウェアが必要であるなど、OpenGL対応を謳っているデバイスでも最新のOpenGL機能が使えるとは限らない。また、[Intel GMAや](https://ja.wikipedia.org/wiki/Intel_GMA "wikilink")[Intel HD Graphicsなどのように](https://ja.wikipedia.org/wiki/Intel_HD_Graphics "wikilink")、DirectX 9.0c（シェーダーモデル3.0）には対応するがOpenGL 2.0には対応しなかったり、DirectX 10（シェーダーモデル4.0）には対応するがOpenGL 3.2には対応しなかったり、DirectX 11（シェーダーモデル5.0）には対応するがOpenGL 4.3には対応しなかったり、さらにはOSによってOpenGLの対応バージョンに違いがあったり\[3\]と、DirectXと比べて同等世代のOpenGLへの対応が遅い環境も存在する。

## 歴史

元々はSGIが自社ワークステーションで使用していたというライブラリを改良し、移植性を高めたものである\[4\]。

[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")以降は、OpenGL Architecture Review Board (ARB) により監修される事となる。このARBには、[3Dlabs](https://ja.wikipedia.org/wiki/3Dlabs "wikilink")、[アップル](../Page/アップル_\(企業\).md "wikilink")、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")（旧[ATI](https://ja.wikipedia.org/wiki/ATI_Technologies "wikilink")）、[デル](https://ja.wikipedia.org/wiki/デル "wikilink")、[Evans & Sutherland](https://ja.wikipedia.org/wiki/Evans_&_Sutherland "wikilink")、HP、IBM、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[Matrox](https://ja.wikipedia.org/wiki/Matrox "wikilink")、[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")、シリコングラフィックス、サン・マイクロシステムズ（現オラクル）が参加している。2006年9月21日以降からは、100以上の企業で構成される[標準化団体](https://ja.wikipedia.org/wiki/標準化団体 "wikilink")[クロノス・グループ](https://ja.wikipedia.org/wiki/クロノス・グループ "wikilink") (The Khronos Group) へ管理が移行し、OpenGL ARB Working Group (OpenGL ARB WG) となった。

オープンな仕様であるため、各種OSに移植または互換GLが作成され、またグラフィックチップベンダーもオープンソースOS用のドライバを用意するなど汎用性に富むライブラリとなっている。ベンダー独自の機能にも、「拡張」（Extension）という形で柔軟に対応できるため、いち早く最新の3Dグラフィックスハードウェアによる先進技術を利用できる反面、ハードウェアを限定した汎用性のないアプリケーションも開発できてしまう。ベンダー拡張の中には、のちに標準仕様として取り込まれたものもある。

OpenGLの標準化はDirectX (Direct3D) と比較すると遅い傾向にある。OpenGL 3.0以降、仕様の更新頻度は高まってきており、テッセレーションの標準化（DirectX 11.0とOpenGL 4.0）に関してはリリース時期にそれほど時間差はなかったが、コンピュートシェーダーの標準化（DirectX 11.0とOpenGL 4.3）に関しては時間差が大きかった。しかし、OpenGLのほうが先行して導入・標準化し、のちにDirectXが追従した機能もいくつか存在する\[5\]。やのようにOpenGL/OpenGL ESでしかサポートされていないものもある\[6\]\[7\]\[8\]\[9\]。

## 特徴

[thumb](https://ja.wikipedia.org/wiki/ファイル:Pipeline_OpenGL.svg "wikilink") OpenGLは画面（[フレームバッファ](https://ja.wikipedia.org/wiki/フレームバッファ "wikilink")）に描画することを前提に設計されている。3DCGを描画できると言っても、オフラインレンダラー（[POV-Ray](../Page/POV-Ray.md "wikilink")など）のような[レイトレーシング](../Page/レイトレーシング.md "wikilink")法は標準ではサポートされておらず、[ポリゴン](../Page/ポリゴン.md "wikilink")などのプリミティブ形状をリアルタイムに順序をもって[ラスタライズ](https://ja.wikipedia.org/wiki/ラスタライズ "wikilink")（画素化）して合成する事で3DCGを描画する。そのため、形状同士が反映し合うような鏡のような反射、ガラスの屈折、投影、交差した半透明形状などを表現するには、そのためのアルゴリズムを実装する必要がある。効率良く描画を行わせるためには、アルゴリズムの特性を理解した高度なプログラミングが必要とされる。

柔軟な画像処理を行うために、奥行き情報を記録して[Zバッファ](https://ja.wikipedia.org/wiki/Zバッファ "wikilink")法などに利用できる「デプスバッファ」、形状のインデックスを記録してマスク処理などを行える「ステンシルバッファ」、高精度なカラー合成などを行える「蓄積バッファ」など、特殊な画素情報がサポートされている。また、元来OpenGLやGPU内で固定的に処理されてきた頂点データやフラグメント（ラスタライズにより生成される画素）の処理をGPUの強力な処理能力を活かしつつプログラミング可能にする[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")の登場と、それを制御する[シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")[GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")の採用により、さらに多種多様な表現が可能になった。

また、[パーティクル](https://ja.wikipedia.org/wiki/パーティクル "wikilink")機能を主眼に置いたポイントスプライトをサポートしている。一般的にパーティクルや2次元画像のオブジェクトを3次元空間に合成する場合は、平板なポリゴンに[テクスチャを張り](https://ja.wikipedia.org/wiki/テクスチャマッピング "wikilink")、常に視点と平行になるよう調整する「ビルボード」と呼ばれる手法が使われているが、ポイントスプライトを使うことでビルボードに代わり、座標計算やプログラミングのコストを軽減できる。

なお、OpenGL 2.xまではプリミティブの描画を記録・再生するDisplay Listと呼ばれる機能や、Begin/Endブロックによるプリミティブ描画コマンドのCPUベース記述モードといった高レベル機能が存在したが、OpenGL 3.0のコアプロファイルでは廃止予定の非推奨機能となった\[10\]。

## コード例

C/C++向けのOpenGLコード例を示す。

  - OpenGL 2.xまでの固定機能で三角形を描画する例。

<!-- end list -->

``` cpp
// Direct3D デバイス／デバイスコンテキストとは異なり、
// 描画ターゲットとなる OpenGL レンダリングコンテキストは暗黙のグローバルステートとなっており、
// 関数引数に対して明示的に指定しない。
glDisable(GL_LIGHTING);
glBegin(GL_TRIANGLES);
{
  glColor3f(1.0f, 0.0f, 0.0f);
  glVertex2f(0.0f, +1.0f);
  glColor3f(0.0f, 1.0f, 0.0f);
  glVertex2f(-1.0f, 0.0f);
  glColor3f(0.0f, 0.0f, 1.0f);
  glVertex2f(+1.0f, 0.0f);
}
glEnd();
```

他にも、ユーザーメモリ頂点配列／エレメント配列（CPU側データ）や、頂点バッファ／エレメントバッファ（GPU側データ）を利用した、より高速な描画方法がある。なお、Direct3Dの頂点宣言・頂点レイアウトに似た機能として Vertex Array Object (VAO) および Vertex Attribute \[[https://www.opengl.org/wiki/Vertex_Specification\]が存在するが、Direct3Dのように頂点バッファと頂点属性を完全に分離して扱えるものではない。頂点宣言・頂点レイアウトの互換機能](https://www.opengl.org/wiki/Vertex_Specification%5Dが存在するが、Direct3Dのように頂点バッファと頂点属性を完全に分離して扱えるものではない。頂点宣言・頂点レイアウトの互換機能) GL_ARB_vertex_attrib_binding \[[https://www.opengl.org/registry/specs/ARB/vertex_attrib_binding.txt\]が標準化されているのはOpenGL](https://www.opengl.org/registry/specs/ARB/vertex_attrib_binding.txt%5Dが標準化されているのはOpenGL) 4.3/ES 3.0以降である[1](http://wlog.flatlib.jp/item/1629)。

### プログラマブルシェーダー

プログラマブルシェーダーを利用する場合は、GLSL言語等を使いシェーダープログラムを別途作成して、glUseProgram()関数を使ってあらかじめレンダリングコンテキストにプログラムオブジェクトをセットしてから描画関数を呼び出す必要がある。

## 補助・拡張ライブラリ

OpenGLそのものは、ハードウェアおよび[デバイスドライバー](https://ja.wikipedia.org/wiki/デバイスドライバー "wikilink")層に近い低次のライブラリである。そのため、より[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")層に近い、多くの高次の補助・拡張ライブラリが存在する。主に、3D描画機能を簡易化・拡張するもの、ウインドウシステムをサポートするもの、グラフィックス面以外の機能を付加するものに分けられる。

### C/C++向け

  - \- カメラや球、円筒、曲面などの取り扱いを補助する

  - [GLX](https://ja.wikipedia.org/wiki/GLX "wikilink") - [X Window SystemでOpenGLを利用するためのライブラリ](../Page/X_Window_System.md "wikilink")

  - \- [Microsoft WindowsでOpenGLを利用するためのライブラリ](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") ([Windows APIおよび](https://ja.wikipedia.org/wiki/Windows_API "wikilink")[GDIの一部](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink"))

  - , , NSOpenGL ([Cocoa](../Page/Cocoa.md "wikilink")の一部) - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")でOpenGLを利用するためのライブラリ

  - \- [OpenGL ES](https://ja.wikipedia.org/wiki/OpenGL_ES "wikilink"), といったKhronosの描画APIと、下層のプラットフォーム固有ウィンドウシステムをつなぐインターフェイス\[11\]

  - [GLUT](https://ja.wikipedia.org/wiki/OpenGL_Utility_Toolkit "wikilink") - クロスプラットフォームのOpenGL対応[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")

  - \- GLUTの機能を強化した、上位互換ライブラリ\[12\]

  - \- GLUTをベースにした[ウィジェットライブラリ](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")

  - AUX - [ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")であるが、古くなっておりGLUTの使用が推奨されている

  - \- OpenGL拡張の使用を容易にするライブラリ。開発は停止しており、公式バージョンの配布もされていない\[13\]\[14\]。

  - \- [GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")などのOpenGL拡張の使用を容易にするライブラリ\[15\]。OpenGL 4.6に対応。

  - \- クロスプラットフォームのOpenGL対応フレームワークツールキット\[16\]。[OpenGL ESおよび](https://ja.wikipedia.org/wiki/OpenGL_ES "wikilink")[Vulkanにも対応](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")。

  - [GLUS](https://ja.wikipedia.org/wiki/GLUS "wikilink") (Graphic Library UtilitieS) - 公式のクロスプラットフォームなユーティリティ。[OpenGL ESにも対応](https://ja.wikipedia.org/wiki/OpenGL_ES "wikilink") \[17\]

  - [OpenGL Mathematics](https://ja.wikipedia.org/wiki/OpenGL_Mathematics "wikilink") (GLM) - GLSLライクに記述できるC++向けの算術ライブラリ\[18\]

  - [PLIB](https://ja.wikipedia.org/wiki/PLIB "wikilink") - OpenGLを利用したゲーム開発ライブラリ

  - [OpenSceneGraph](https://ja.wikipedia.org/wiki/OpenSceneGraph "wikilink")

  - [FLTK](https://ja.wikipedia.org/wiki/FLTK "wikilink") - クロスプラットフォームのOpenGL対応[ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/ウィジェット・ツールキット "wikilink")

  - [Open Inventor](https://ja.wikipedia.org/wiki/Open_Inventor "wikilink")

  - ToGL - [Valve Softwareが開発した](https://ja.wikipedia.org/wiki/Valve_Software "wikilink")、Direct3DからOpenGLへの変換レイヤー\[19\]

  - [SDL](../Page/SDL.md "wikilink") - クロスプラットフォームなマルチメディアライブラリ

### その他の言語向け

C/C++以外の主要なOpenGL言語バインディング（ラッパー）とライブラリには以下のようなものがある。

  - \- [C\#向けのローレベルなOpenGL](../Page/C_Sharp.md "wikilink")/OpenGL ES/[OpenAL](https://ja.wikipedia.org/wiki/OpenAL "wikilink")バインディング\[20\]

  - [Java OpenGL](https://ja.wikipedia.org/wiki/Java_OpenGL "wikilink") (JOGL) - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")向けのバインディング

      - [Java 3D](../Page/Java_3D.md "wikilink") - JOGL上に構築される[Java](https://ja.wikipedia.org/wiki/Java "wikilink")向けの[シーングラフ](https://ja.wikipedia.org/wiki/シーングラフ "wikilink")ベース高レベルライブラリ

  - [LWJGL](https://ja.wikipedia.org/wiki/LWJGL "wikilink") - Java向けのゲーム開発用ライブラリ

なお、[WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink")は[JavaScript](../Page/JavaScript.md "wikilink")向けの単なるラッパーや言語バインディングではなく、OpenGL ES派生の別規格である。

## バージョンの変遷

### OpenGL 1.1

テクスチャに対応。Windowsの標準ドライバーおよびWGLで標準サポートされているのは、このOpenGL 1.1である\[21\]。

### OpenGL 1.5

2003年にリリースされたOpenGL 1.5では、拡張機能として[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")のための高級言語（GLSL 1.0）に初めて対応した\[22\]。

### OpenGL 2.x

2004年にリリースされたOpenGL 2.0では、シェーディング言語GLSLのバージョン1.1対応が標準仕様として盛り込まれた。

### OpenGL 3.x

2008年にリリースされたOpenGL 3.0では、肥大化したOpenGL APIセット自体のシェイプアップを目的として2.x以前の世代を切り捨てる大幅なアップデートが行われ、多くの機能が非推奨・廃止予定になった。翌2009年3月に発表されたOpenGL 3.1では固定機能シェーダーが標準仕様から取り除かれ、拡張機能扱いとなった。また同年8月に発表されたOpenGL 3.2では、Direct3D 10で導入された[ジオメトリシェーダー](https://ja.wikipedia.org/wiki/ジオメトリシェーダー "wikilink")に正式対応した\[23\]。固定機能シェーダーの廃止やジオメトリシェーダーの対応などは、Direct3D 10の仕様と合致している。

### OpenGL 4.x

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[3月11日](../Page/3月11日.md "wikilink")に OpenGL 4.0 を発表\[24\]。Direct3D 11のハル シェーダー、テッセレータおよびドメイン シェーダーに相当する、テッセレーション制御シェーダー、テッセレーション プリミティブ ジェネレーターおよびテッセレーション評価シェーダーが搭載された\[25\]。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[7月26日](../Page/7月26日.md "wikilink")に OpenGL 4.1 を発表\[26\]。シェーダープログラムバイナリの取得やビューポート配列の対応など。

[2011年](../Page/2011年.md "wikilink")[8月8日](../Page/8月8日.md "wikilink")に OpenGL 4.2 を発表\[27\]。シェーダーにおけるアトミックカウンターの実装など。

[2012年](../Page/2012年.md "wikilink")[8月6日](../Page/8月6日.md "wikilink")に OpenGL 4.3 を発表\[28\]。Direct3D 11のコンピュート シェーダーと同様の[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")用演算シェーダーが追加搭載された\[29\]。また、次世代テクスチャ圧縮技術であるのサポートが公式拡張として定義された\[30\]。

[2013年](../Page/2013年.md "wikilink")[7月22日](../Page/7月22日.md "wikilink")に OpenGL 4.4 を発表\[31\]。バッファ制御や非同期クエリ対応など\[32\]。

[2014年](../Page/2014年.md "wikilink")[8月11日](../Page/8月11日.md "wikilink")に OpenGL 4.5 を発表\[33\]。Direct State Access (DSA) 対応など\[34\]。

[2015年](../Page/2015年.md "wikilink")[8月10日](../Page/8月10日.md "wikilink")にOpenGL 2015 ARB Extensionsとして、OpenGL ES 3.2互換機能やシェーダーの並列コンパイル機能などが拡張として追加された\[35\]。

[2017年](../Page/2017年.md "wikilink")[7月31日](../Page/7月31日.md "wikilink")に OpenGL 4.6 を発表\[36\]。SPIR-Vの導入、Vulkan/Direct3Dとの相互運用性の強化など。

以前はOpenGL仕様のアップデートの速度や頻度はDirect3Dに比べて非常にゆっくりとしたものであったが、OpenGL 4の機能の中にはDirect3D 11と同等あるいはそれ以上に素早く追加されたものもある。

### Vulkan

[SIGGRAPH](https://ja.wikipedia.org/wiki/SIGGRAPH "wikilink") 2014で、レガシーな設計が蓄積しているOpenGLをリセットし、ゼロから構築し直して刷新する、次世代の標準3D API規格（OpenGL Next Generation, glNext）の策定が始められることがアナウンスされた。このとき、[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")対応やシェーディング[中間言語](../Page/中間言語.md "wikilink")などの近代的な技術が導入されることが発表された\[37\]。

[GDC](https://ja.wikipedia.org/wiki/Game_Developers_Conference "wikilink") 2015では、新規格の名称が**"Vulkan"**（ドイツ語で"火山"）となることが発表され\[38\]、[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink") 12同様のコマンドキューベースのマルチスレッドレンダリング機能や、[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")とのプログラミング基盤共通化をもたらすSPIR-V中間表現\[39\]を導入することが明らかにされた。また、Vulkanには[AMD独自のローレベルグラフィックスAPIである](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[Mantleが要素技術として取り込まれることが発表された](https://ja.wikipedia.org/wiki/Mantle_\(API\) "wikilink")\[40\]。

2016年2月16日、Vulkan 1.0の正式仕様がリリースされた\[41\]。

なお、Vulkanはハードウェアの詳細な制御を可能とするローレベルAPIである一方、従来のOpenGLはCPU-GPU間の同期などの煩雑な処理を自動で行なってくれる上位層のAPIとして、今後もメンテナンスおよびアップデートが継続されることになっている\[42\]。

## 弱点

OpenGL 3.xで固定機能を分離するなどのシェイプアップは図られたが、しかしOpenGLは互換性維持という名目で、1.xや2.x時代に設計された古いAPI構造の大部分をいまだに踏襲している。一方で競合APIのDirect3Dは互換性を切り捨てながらも思い切った仕様変更により、APIをその当時の技術トレンドや先進技術に即した形で洗練してきた\[43\]。またDirect3Dは公式ドキュメントが充実していることや、習得がしやすいことも評価されている\[44\]。実際にOpenGL仕様そのものに対して、開発者から不満の声も上がっている\[45\] \[46\] \[47\]。ここではOpenGLの弱点や問題点、および不足機能に関して記述する。

### 文字列の描画

OpenGL単体では、Windows [GDIや](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")[Core Graphicsのような高レベルの文字列描画用APIが用意されていない](../Page/Quartz.md "wikilink")[2](http://www.opengl.org/archives/resources/faq/technical/fonts.htm) [3](http://en.wikibooks.org/wiki/OpenGL_Programming/Modern_OpenGL_Tutorial_Text_Rendering_01) \[[http://fractiousg.blogspot.jp/2012/04/rendering-text-in-opengl-on-android.html\]ため、あらかじめ文字が描画されたテクスチャを（画像ファイルから読み込むなどして）利用するか、プラットフォーム依存の高レベルAPI（例えばWindowsの場合はwglUseFontOutlines](http://fractiousg.blogspot.jp/2012/04/rendering-text-in-opengl-on-android.html%5Dため、あらかじめ文字が描画されたテクスチャを（画像ファイルから読み込むなどして）利用するか、プラットフォーム依存の高レベルAPI（例えばWindowsの場合はwglUseFontOutlines)()関数\[[http://msdn.microsoft.com/en-us/library/windows/desktop/dd374393.aspx\]など）と連携する必要がある（クロスプラットフォームのユーティリティライブラリであるGLUTなどを使用すると、文字・文字列を描画することができるが、その機能はごく限られており、あくまでデバッグ用途などの簡易的なサポートにとどまる](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374393.aspx%5Dなど）と連携する必要がある（クロスプラットフォームのユーティリティライブラリであるGLUTなどを使用すると、文字・文字列を描画することができるが、その機能はごく限られており、あくまでデバッグ用途などの簡易的なサポートにとどまる)）。[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")拡張としてはGL_NV_Path_Rendering[4](https://www.opengl.org/registry/specs/NV/path_rendering.txt)[5](http://developer.download.nvidia.com/assets/gamedev/files/GL_NV_path_rendering.txt)\[[http://www.nvidia.co.jp/object/adobe-illustrator-cc-gpu-accelerated-20140619-jp.html\]が存在し、高レベルなプリミティブ描画のGPUアクセラレーションや](http://www.nvidia.co.jp/object/adobe-illustrator-cc-gpu-accelerated-20140619-jp.html%5Dが存在し、高レベルなプリミティブ描画のGPUアクセラレーションや)[フォント](../Page/フォント.md "wikilink")もサポートするが、標準化はされていない。

なお、[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")も同様に文字列描画が弱点であるが、Direct3D 10.1以降では[Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")や[DirectWrite](https://ja.wikipedia.org/wiki/DirectWrite "wikilink")といった複雑な2D描画や文字列描画に特化した高レベル派生APIおよびDirect3Dとの相互運用・連携機能も整備されている。また、[WPF](https://ja.wikipedia.org/wiki/WPF "wikilink")ではハードウェアに応じてDirect3Dが使用されるが、Direct2D/DirectWriteのようにAPIが高レベルに抽象化されており、複雑な2D描画や文字列描画にはDirect3DやOpenGLを直接使用するよりも向いている。

### マルチGPU

Direct3Dでは[DXGI](https://ja.wikipedia.org/wiki/DXGI "wikilink")アダプターを列挙することで、複数のGPUを搭載したシステムにおいて任意のGPUを選択的に使用することが可能となっている[6](https://msdn.microsoft.com/ja-jp/library/bb205075.aspx)。これにより、（[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")や[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")のように）複数のGPUを利用して各々に[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")演算処理を分散実行させ、アプリケーションソフトウェアの並列処理性能を向上させるといった使い方ができる。一方、OpenGLで複数のGPUを選択的に使用したり、それぞれのGPUに対してレンダリングコンテキストやリソースを作成する機能はOpenGL 4.5時点でも標準化されていない。Windows環境においては、2006年に[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")からWGL_NV_gpu_affinity[7](https://www.opengl.org/registry/specs/NV/gpu_affinity.txt) [8](http://www.nvidia.com/content/nvision2008/tech_presentations/Professional_Visualization/NVISION08-8MP_HDR.pdf)、2009年に[AMDからWGL](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")_AMD_gpu_association\[[https://www.opengl.org/registry/specs/AMD/wgl_gpu_association.txt\]というWGL拡張がそれぞれ提供されているが、AMD拡張のほうは](https://www.opengl.org/registry/specs/AMD/wgl_gpu_association.txt%5DというWGL拡張がそれぞれ提供されているが、AMD拡張のほうは)[Radeon](https://ja.wikipedia.org/wiki/Radeon "wikilink")でも[FirePro](https://ja.wikipedia.org/wiki/FirePro "wikilink")でも使用できる\[[http://delphigl.de/glcapsviewer/gl_listreports.php?listreportsbyextension=WGL_AMD_gpu_association\]ものの、NVIDIA拡張のほうは](http://delphigl.de/glcapsviewer/gl_listreports.php?listreportsbyextension=WGL_AMD_gpu_association%5Dものの、NVIDIA拡張のほうは)[GeForce](https://ja.wikipedia.org/wiki/GeForce "wikilink")では使用できず、[Quadro](https://ja.wikipedia.org/wiki/Quadro "wikilink")のみの対応となっている[9](http://delphigl.de/glcapsviewer/gl_listreports.php?listreportsbyextension=WGL_NV_gpu_affinity)。Windows以外のプラットフォームではAMDによる[X Window System向けのGLX拡張GLX](../Page/X_Window_System.md "wikilink")_AMD_gpu_association\[[http://www.opengl.org/registry/specs/AMD/glx_gpu_association.txt\]のみで、NVIDIAからは提供されておらず、アプリケーション側からリソースを割り当てるGPUを個別に指定する手段がない](http://www.opengl.org/registry/specs/AMD/glx_gpu_association.txt%5Dのみで、NVIDIAからは提供されておらず、アプリケーション側からリソースを割り当てるGPUを個別に指定する手段がない)。

なお、NVIDIA [SLIに対応した複数のGPUを用いてSLI構成を行なうことによりGPUドライバー側で分散処理を実行させることはできるが](https://ja.wikipedia.org/wiki/Scalable_Link_Interface "wikilink")、SLIは主にOpenGLやDirect3Dにおけるグラフィックスフレームのレンダリングを自動的に分散処理して高速化する技術であり、SLI環境下での[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")分散処理を行なう場合は注意点や制約が存在する\[48\]（NVIDIA GPUにおける[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")はすべて[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")基盤を利用しているため、このSLI環境における制約は[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")/[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")/[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink")/OpenGL Compute Shaderを問わない）。また、AMDマルチGPU環境でOpenCLを利用したGPGPU分散処理を行なう場合、CrossFire ([CrossFireX](https://ja.wikipedia.org/wiki/CrossFireX "wikilink")) をOFFにすることが推奨されている\[49\]。なお、SLIやCrossFire/CrossFireXではメモリのミラーリングが行なわれるため、複数のGPUを搭載していても、使用できるメモリ総量は各GPUメモリの合計値とはならない。一方、DirectX 12（[WDDM](https://ja.wikipedia.org/wiki/WDDM "wikilink") 2.0）ではSLIやCrossFireといったベンダー独自技術に依存しない形でマルチGPUにネイティブ対応し、標準で分散レンダリングを可能とするほか、複数GPUのビデオメモリを単一のメモリプールに統合することも可能となっている\[50\] \[51\]。

また、[Adobe PhotoshopではバージョンCS](../Page/Adobe_Photoshop.md "wikilink")4以降、OpenGLによるハードウェアアクセラレーションが導入されている\[52\]が、マルチGPU環境は推奨されていない\[53\]。

### コンピュート機能（GPGPU機能）とウィンドウ／レンダリングコンテキスト

[DirectCompute](https://ja.wikipedia.org/wiki/DirectCompute "wikilink") (Direct3D 11) では[CUDA](https://ja.wikipedia.org/wiki/CUDA "wikilink")および[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")同様に、OSのウィンドウシステム（[ユーザーインターフェイス](https://ja.wikipedia.org/wiki/ユーザーインターフェイス "wikilink")）とは直接関連しない完全なオフスクリーンオブジェクトであるDirect3Dデバイスおよびデバイスコンテキストを作成するだけで、コンピュート機能を利用することが可能となっている（コンピュートシェーダーの実行つまりコンピュートカーネルの発行には、DXGIスワップチェーンの作成およびプレゼンテーションは不要）\[54\]。一方、OpenGL APIは必ずレンダリングコンテキストを作成してから使用する必要があり、また描画命令を発行するためにはレンダリングコンテキストをバインドするサーフェイスを、OSのウィンドウシステムに関与するAPIを利用して作成する必要がある（例えばWindowsの場合はウィンドウDCまたはメモリDCといった[GDIのデバイスコンテキストが必要](https://ja.wikipedia.org/wiki/Graphics_Device_Interface "wikilink")）\[55\]\[56\]。OpenGL 4.3では汎用計算向けのコンピュートシェーダーが搭載されたが、この制約のためにOpenGLでコンピュートシェーダーを利用する場合は必ずOSのウィンドウシステムへのアクセスが必要となってしまう。シミュレーションの可視化など、OpenGLコンピュートシェーダーを必ずグラフィックス連携用途に使うことを前提としている場合は大きな問題にならないが、完全なオフスクリーンで純粋にコンピュート機能を利用しようとする場合には障壁となりうる（OpenGL 4.5時点での代替策、すなわち完全オフスクリーンでのコンピュート実行はOpenCLに頼らざるを得ない）。

### マルチスレッド対応

Direct3D 11ではイミディエイトコンテキスト／ディファードコンテキストという形で、[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")CPUにおいて[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")を活用して描画パフォーマンスを向上する仕組みが導入され[10](https://msdn.microsoft.com/ja-jp/library/ee422107.aspx)、Direct3D 12ではさらにコマンドキューベースのマルチスレッドレンダリング機能による描画効率の向上が図られているが、OpenGLでは4.5時点で相当機能をサポートしていない。また、Direct3D 11ではデバイスインターフェイスのメソッド呼び出しがスレッドセーフであり、サブスレッドからのリソース生成や複数のスレッドからのリソース同時生成に標準で対応している（同時利用可能なスレッド数はドライバーに依存する[11](https://msdn.microsoft.com/ja-jp/library/ee422105.aspx)）が、OpenGLではレンダリングコンテキストを作成したスレッドのみがリソースを扱えるようになっているため、サブスレッドでリソース生成を行なうにはwglShareLists()関数\[[https://msdn.microsoft.com/en-us/library/dd374390.aspx\]やglXCreateContext](https://msdn.microsoft.com/en-us/library/dd374390.aspx%5DやglXCreateContext)()関数\[[https://www.opengl.org/sdk/docs/man2/xhtml/glXCreateContext.xml\]といったプラットフォーム依存のAPIを利用して明示的にコンテキスト共有を行なう必要がある](https://www.opengl.org/sdk/docs/man2/xhtml/glXCreateContext.xml%5Dといったプラットフォーム依存のAPIを利用して明示的にコンテキスト共有を行なう必要がある)。

### ドライバー品質とGLSLコンパイラー

Direct3D (Windows) にはWHQL (Windows Hardware Quality Lab) [12](https://msdn.microsoft.com/en-us/library/windows/hardware/ff553976.aspx%5Dというドライバー品質保証の仕組みが存在するが、OpenGLコミュニティ総体にはそういったドライバー認証システムは存在していなかった%5Bhttps://forums.autodesk.com/autodesk/attachments/autodesk/78/442801/1/autodesk_inventor_opengl_to_directx_evolution_788.pdf)。またDirect3Dとは違ってOpenGLおよびOpenGL ESドライバーはベンダーや個々の製品によって出来不出来の差が激しく、このドライバー品質問題に関して開発者やユーザーから不満の声が上がっていた\[57\] \[58\]。さらに、GLSLのリファレンスコンパイラー実装は[Khronos](https://ja.wikipedia.org/wiki/Khronos "wikilink")グループによって提供されている\[59\]ものの、OpenGL/OpenGL ESにおいてはシェーダープログラムの共通バイトコード仕様が定義されていないためにGLSLオフラインコンパイラーは存在せず、シェーダープログラムのコンパイルはベンダーごとのドライバーに実装されたGLSLオンラインコンパイラーによって実行時になされる。しかし、OpenGL仕様にはエラーハンドリングなどに関して厳密に規定されていないあいまいな部分が存在することから、現実問題としてベンダーごとにコンパイラーの挙動が異なるという処理系依存動作を許可してしまっているのが実態であり、これがアプリケーション開発者の負担増加につながり、またドライバーやアプリケーションプログラムにおけるバグの温床となってしまう\[60\] \[61\]。

OpenGL 4.4以降においては、[Khronos](https://ja.wikipedia.org/wiki/Khronos "wikilink")グループによる品質保証制度を新設し、品質問題の改善を進めることとなった\[62\]。また、OpenGLの後継APIとなるVulkanでは、前述のようにシェーダープログラムの中間言語としてSPIR-Vを採用している。OpenGL 4.6ではSPIR-Vのサポートがコア機能として組み込まれた。

なおプロジェクトのように、Windows上でDirect3D APIをラップしてOpenGL APIをエミュレートすることで、OpenGLドライバーの品質問題を回避しているものも存在する[13](http://qt-project.org/wiki/Qt_5_on_Windows_ANGLE_and_OpenGL_Japanese) [14](http://news.mynavi.jp/news/2010/03/19/034/?rt=na)。

## DirectXとの関係

OpenGLは3Dグラフィックスを専門的に扱うライブラリである。対して[Microsoft DirectXは](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、ゲーム開発での利用を主な用途としており、グラフィックスのみならずサウンドや入力関連のAPIを含んでいる点で性質が異なる。 なお、OpenGLと直接比較されるべきAPIは、DirectX製品の一部、グラフィックスを司る[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")である。

DirectXは主に[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Xbox](https://ja.wikipedia.org/wiki/Xbox "wikilink")プラットフォームでのゲーム開発等で多く用いられる（Linux上でDirectXを動作させるCedegaなどの例もある）。対してOpenGLはクロスプラットフォームであり、Windowsだけでなく様々なOSに実装が提供されている 。Windows環境ではDirectXとOpenGLを両立させる事も可能である。

発祥がワークステーションである事やクロスプラットフォームである事から、CADや工業デザイン、科学技術計算や医療での視覚化等の業務分野では、クロスプラットフォームなアプリケーションに限らずWindows専用アプリケーションであっても、[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")等のエンタテインメント用途重視のグラフィックスAPIよりもOpenGLが用いられる事が多い。そのため、ワークステーションや業務向けの[GPUや](../Page/Graphics_Processing_Unit.md "wikilink")[ビデオカード](../Page/ビデオカード.md "wikilink")製品には、OpenGLに最適化された仕様の物が販売される傾向がある。OpenGL向けと称されているGPUには[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")社の『[Quadro](https://ja.wikipedia.org/wiki/Quadro "wikilink")』シリーズや、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") (旧[ATI](https://ja.wikipedia.org/wiki/ATI_Technologies "wikilink")) の『[AMD FirePro](https://ja.wikipedia.org/wiki/AMD_FirePro "wikilink") (旧[ATI FirePro](https://ja.wikipedia.org/wiki/ATI_FirePro "wikilink")/FireGL)』シリーズが存在し、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を含めた仕様がOpenGL用に最適化されている。しかしその反面、これらの製品はDirectX (Direct3D) への最適化が甘く、DirectXを使用したアプリケーションにおける性能が芳しくない傾向もある[15](http://www.futuremark.com/hardware/gpu/NVIDIA+Quadro+K5000/review)。

なお、[Windowsだけでなく](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")および[Mac](../Page/Macintosh.md "wikilink") ([macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")) に対してもGPUベンダーからOpenGL対応のドライバが供給されているが、Macに関してはWindowsおよびLinuxと異なり、そもそもベンダーが正式対応しているハードウェアが限られている\[63\] \[64\] \[65\] \[66\] \[67\]。

シリコングラフィックスと[マイクロソフト](../Page/マイクロソフト.md "wikilink")はかつてOpenGLとDirect3Dの統合を目標として、[Fahrenheit](https://ja.wikipedia.org/wiki/Fahrenheit "wikilink")と呼ばれる3DグラフィックスAPIの共同開発を1997年に開始したことがあるが\[68\]、1999年の末までに計画は事実上頓挫している。また、マイクロソフト社はOpenGL ARBの設立時のメンバーでもあったが、2003年に脱退した。その後、シリコングラフィックスの倒産やOpenGL仕様の[Khronos](https://ja.wikipedia.org/wiki/Khronos "wikilink")グループへの移管など紆余曲折を経て、2014年にはOpenGL 4.5の発表とともに、マイクロソフトが[Khronos](https://ja.wikipedia.org/wiki/Khronos "wikilink")グループに参加することが明らかになった\[69\]。

## OpenCLとの関係

OpenGL仕様を管理している[Khronos](https://ja.wikipedia.org/wiki/Khronos "wikilink")グループによって同様に管理されているオープン仕様の[APIとして](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")を含む異種計算資源混在環境（ヘテロジニアス環境）用の[並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")APIである[OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")が存在する。OpenCLにはDirect3DおよびOpenGLのグラフィックスリソースを扱うことのできる相互運用機能が存在するが、一方でOpenGLはバージョン4.3でDirectX同様にGPGPU用の演算シェーダーを導入している。ただし、OpenCLは依然としてヘテロジニアス環境に特化した幅広いプラットフォーム対応APIであるが、OpenGLの演算シェーダーはよりグラフィックス用途に特化したGPGPU用のものとなり、競合するというよりはむしろ相補的な役割を担うことになる。

## macOSでの非推奨化

2018年6月5日、Appleは[WWDC](https://ja.wikipedia.org/wiki/WWDC "wikilink") 2018でOpenGL/OpenCLの非推奨化を発表し、[macOS Mojaveにおいて](https://ja.wikipedia.org/wiki/macOS_Mojave "wikilink")（サポートはまだ打ち切られないものの）OpenGL/OpenCLは非推奨APIとなった。macOSがネイティブにサポートするOpenGLのバージョンは4.1が最後となっている\[70\]。

OpenGLの代替として推奨されているAPIは[Metalであるが](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")、MetalはVulkan同様、OpenGLよりもハードウェア層に近いローレベルAPIであり、アプリケーション開発向けというよりミドルウェア開発向けに位置する。

## 脚注

## 関連項目

  - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")

  - [Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")

  - [Mantle (API)](https://ja.wikipedia.org/wiki/Mantle_\(API\) "wikilink")

  - [Metal (API)](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")

  - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")

  - [GLSL](https://ja.wikipedia.org/wiki/GLSL "wikilink")

  - [OpenCL](https://ja.wikipedia.org/wiki/OpenCL "wikilink")

  - [OpenAL](https://ja.wikipedia.org/wiki/OpenAL "wikilink")

  - [OpenGL ES](https://ja.wikipedia.org/wiki/OpenGL_ES "wikilink")

  - [OpenSL ES](https://ja.wikipedia.org/wiki/OpenSL_ES "wikilink")

  - [Mesa 3D](https://ja.wikipedia.org/wiki/Mesa_3D "wikilink")

  - [VirtualGL](https://ja.wikipedia.org/wiki/VirtualGL "wikilink")

  -
  -
## 外部リンク

  - [OpenGL公式サイト](https://www.opengl.org/)
  - [SGI公式サイト](http://www.sgi.com/)
  - Khronos Group
      - [The Khronos Group Inc.](https://www.khronos.org/)
      - [Khronos Group クロノスグループ日本語サイト](http://jp.khronos.org/)
      - [OpenGL - The Industry](https://www.khronos.org/opengl/)
      - [OpenVG - The Standard for Vector Graphics Acceleration](https://www.khronos.org/openvg/)
  - [OpenGL Programming Guide](http://glprogramming.com/red/) - 通称「赤本 (red book)」と呼ばれる解説書
  - [OpenGL Reference Manual](http://glprogramming.com/blue/) - 通称「青本 (blue book)」と呼ばれるリファレンス
  - [OpenGL.jp](http://opengl.jp/) - FAQ
  - [GLUTによる「手抜き」OpenGL入門](http://www.wakayama-u.ac.jp/~tokoi/opengl/libglut.html)

[Category:OpenGL](https://ja.wikipedia.org/wiki/Category:OpenGL "wikilink") [Category:GPGPU](https://ja.wikipedia.org/wiki/Category:GPGPU "wikilink") [Category:3DCG](https://ja.wikipedia.org/wiki/Category:3DCG "wikilink") [Category:グラフィックカード](https://ja.wikipedia.org/wiki/Category:グラフィックカード "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:1992年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1992年のソフトウェア "wikilink")

1.  [OpenGL Overview](https://www.opengl.org/about/)
2.  [QuadroとGeForceの違い ｜菱洋エレクトロ株式会社](https://web.archive.org/web/20160429193919/http://www.ryoyo.co.jp/product/supplier_list/p73/p81-04-02.html), [Internet Archive](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")
3.  [ホイール欲しい ハンドル欲しい » Intel HD Graphics 4000 GPU と OpenGL](http://wlog.flatlib.jp/item/1694)
4.  [日本SGI - OpenGL](https://web.archive.org/web/20160308193952/http://www.sgi.co.jp/visualization/opengl/), [Internet Archive](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")
5.  [［SIGGRAPH］ついにDirectX 11を凌駕した\!? Khronosに聞く「OpenGL 4.2」の正体 - 4Gamer.net](https://www.4gamer.net/games/107/G010729/20110821001/)
6.  [OpenGLはDirectX 11を超え，OpenGL ESは据え置き型ゲーム機と同等以上に。Khronosの最新動向レポート - 4Gamer.net](https://www.4gamer.net/games/107/G010729/20121015050/)
7.  かつてDirect3DでのASTCサポートが計画されていたが、2019年現在、実現には至っていない。
8.  \[<https://docs.microsoft.com/en-us/previous-versions/dn914593(v=vs.85>) Adaptive Scalable Texture Compression (Preliminary) | Microsoft Docs\]
9.  \[<https://docs.microsoft.com/en-us/previous-versions/dn894549(v=vs.85>) D3D11_ASTC_PROFILE enumeration (Preliminary) | Microsoft Docs\]
10. [The OpenGL® Graphics System: A Specification (Version 3.0 - August 11, 2008), Mark Segal, Kurt Akeley; Editor (version 1.1): Chris Frazier; Editor (versions 1.2-3.0): Jon Leech; Editor (version 2.0): Pat Brown](https://www.opengl.org/registry/doc/glspec30.20080811.pdf)
11. [EGL Overview - The Khronos Group Inc](https://www.khronos.org/egl)
12. [The freeglut Project :: About](http://freeglut.sourceforge.net/)
13. [OpenGL Loading Library - OpenGL Wiki](https://www.khronos.org/opengl/wiki/OpenGL_Loading_Library#GLee)
14. [SLUDGE Adventure Game Engine - Home](http://opensludge.github.io/#news)
15. [GLEW: The OpenGL Extension Wrangler Library](http://glew.sourceforge.net/)
16. [GLFW - An OpenGL library](https://www.glfw.org/)
17. [GLUS - Modern OpenGL, OpenGL ES and OpenVG Utilities now part of the OpenGL SDK - khronos.org news](https://www.khronos.org/news/permalink/glus-modern-opengl-opengl-es-and-openvg-utilities-now-part-of-the-opengl-sd)
18. [OpenGL Mathematics](https://glm.g-truc.net/)
19. [ValveSoftware/ToGL: Direct3D to OpenGL abstraction layer](https://github.com/ValveSoftware/ToGL)
20. [The Open Toolkit | OpenTK](https://opentk.github.io/)
21. [OpenGL - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/OpenGL/opengl)
22. ["The OpenGL(R) Graphics System: A Specification (Version 1.5)", p.294](https://www.opengl.org/registry/doc/glspec15.pdf)
23. [T.Teranishi:OpenGL:version](http://www.asahi-net.or.jp/~yw3t-trns/opengl/version/index.htm)
24. [Khronos Unleashes Cutting-Edge, Cross-Platform Graphics Acceleration with OpenGL 4.0 - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-unleashes-cutting-edge-cross-platform-graphics-acceleration-opengl4)
25. [Game Developers Conference（GDC） 2010現地レポート - GAME Watch](http://game.watch.impress.co.jp/docs/series/3dcg/20100312_354533.html)
26. [Khronos Drives Evolution of Cross-Platform 3D Graphics with Release of OpenGL 4.1 Specification - Khronos Group Press Release](https://www.khronos.org/news/press/opengl-4-1-released)
27. [Khronos Enriches Cross-Platform 3D Graphics with Release of OpenGL 4.2 Specification - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-enriches-cross-platform-3d-graphics-with-release-of-opengl-4.2-spec)
28. [Khronos Group Announces Key Advances in OpenGL Ecosystem - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-group-announces-key-advances-in-opengl-ecosystem)
29. [「OpenGL 4.3」および「OpenGL ES 3.0」が発表される | SourceForge.JP Magazine](http://sourceforge.jp/magazine/12/08/07/2046244)
30. [Khronos Releases ASTC Next-Generation Texture Compression Specification - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-atsc-next-generation-texture-compression-specification)
31. [Khronos Releases OpenGL 4.4 Specification - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-releases-opengl-4.4-specification)
32. [Khronos、シェアード・バーチャル・メモリなどをサポートするOpenCL 2.0 ～OpenGL 4.4の仕様も公開 - PC Watch](http://pc.watch.impress.co.jp/docs/news/20130724_608798.html)
33. [Khronos Group Announces Key Advances in OpenGL Ecosystem - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-group-announces-key-advances-in-opengl-ecosystem)
34. [OpenGL 4.5が正式リリース - Direct State Accessなどを追加 | マイナビニュース](http://news.mynavi.jp/news/2014/08/12/308/)
35. [Khronos Expands Scope of 3D Open Standard Ecosystem - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-expands-scope-of-3d-open-standard-ecosystem)
36. [Khronos Releases OpenGL 4.6 with SPIR-V Support - The Khronos Group Inc](https://www.khronos.org/news/press/khronos-releases-opengl-4.6-with-spir-v-support)
37. [OpenGL 3Dの次世代規格の策定作業がKhronos Groupの指揮下に始まる…ハードウェア重視、マルチスレッド、共通シェーディング言語など - TechCrunch](http://jp.techcrunch.com/2014/08/12/20140811khronos-group-starts-working-on-the-next-generation-of-its-opengl-3d-specs/)
38. [［GDC 2015］Khronos，新世代グラフィックスAPI「Vulkan」を正式発表。OpenGL時代のしがらみを捨てた，スリムでハイエンドなAPIに - 4Gamer.net](http://www.4gamer.net/games/293/G029343/20150304076/)
39. [SPIR - The first open standard intermediate language for parallel compute and graphics](https://www.khronos.org/spir)
40. [［GDC 2015］Khronos，新世代グラフィックスAPI「Vulkan」でAMDの「Mantle」を採用 - 4Gamer.net](http://www.4gamer.net/games/107/G010729/20150304002/)
41. [新世代の低オーバーヘッドなグラフィックスAPI「Vulkan」，ついに正式始動 - 4Gamer.net](http://www.4gamer.net/games/293/G029343/20160217055/)
42. [Vulkan on NVIDIA GPUs; Piers Daniell, Driver Software Engineer, OpenGL and Vulkan](http://on-demand.gputechconf.com/siggraph/2015/presentation/SIG1501-Piers-Daniell.pdf)
43. [Carmack: Direct3D is now better than OpenGL | bit-gamer.net](http://www.bit-tech.net/news/gaming/2011/03/11/carmack-directx-better-opengl/1)
44. [Valve: OpenGL is faster than DirectX - even on Windows - ExtremeTech](https://www.extremetech.com/gaming/133824-valve-opengl-is-faster-than-directx-even-on-windows)
45. [Rich Geldreich's Tech Blog: Things that drive me nuts about OpenGL](http://richg42.blogspot.jp/2014/05/things-that-drive-me-nuts-about-opengl.html)
46. [OpenGL/ES,GLSLのバグとKhronosの不備 - リンゴをかじれ](http://eyeballonly.com/blog/2014/02/26/glquality/)
47. [OpenGL Is Broken](http://www.joshbarczak.com/blog/?p=154)
48. [Programming Guide :: CUDA Toolkit Documentation](http://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html#sli-interoperability)
49. [Frequently Asked Questions AMD OpenCL™ Coding Competition : OpenCL Questions : 26. Does the AMD APP SDK v2.4 with OpenCL 1.1 support work on multiple GPUs (ATI CrossFire)?](http://community.topcoder.com/amdapp/faq-2/)
50. [AMD、Windows 10/DirectX 12への対応は万全とアピール - PC Watch](http://pc.watch.impress.co.jp/docs/news/20150729_713903.html)
51. [DirectX 12の異種混合GPU「EMA」でGeForceとRadeonをハイブリッドすると意外な結果に - GIGAZINE](http://gigazine.net/news/20160226-directx12-geforce-radeon-hybrid/)
52. [GPU と OpenGL の機能と制限（Photoshop CS4/CS5）](https://helpx.adobe.com/jp/photoshop/kb/234358.html)
53. [Photoshop CC GPU FAQ](https://helpx.adobe.com/jp/photoshop/kb/photoshop-graphics-processor-troubleshooting-faq.html)
54. [directx-sdk-samples/BasicCompute11.cpp at master · walbourn/directx-sdk-samples](https://github.com/walbourn/directx-sdk-samples/tree/master/BasicCompute11)
55. [wglCreateContext function (wingdi.h) - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-wglcreatecontext)
56. [wglMakeCurrent function (wingdi.h) - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/api/wingdi/nf-wingdi-wglmakecurrent)
57. [Dolphin Emulator - Dolphin Emulator and OpenGL drivers - Hall of Fame/Shame](https://ja.dolphin-emu.org/blog/2013/09/26/dolphin-emulator-and-opengl-drivers-hall-fameshame/?cr=ja)
58. [Rich Geldreich's Tech Blog: The Truth on OpenGL Driver Quality](http://richg42.blogspot.jp/2014/05/the-truth-on-opengl-driver-quality.html)
59. [Reference Compiler](https://www.khronos.org/opengles/sdk/tools/Reference-Compiler/)
60. [２年間ずっとわからなかったOpenGLのバグ - リンゴをかじれ](http://eyeballonly.com/blog/2014/02/24/openglbug01/)
61. [opengl:glsl \[HYPERでんち](http://dench.flatlib.jp/opengl/glsl)\]
62. [「OpenGL 4.4」および「OpenCL 2.0」が発表される | SourceForge.JP Magazine:](http://sourceforge.jp/magazine/13/07/24/190000)
63.
64. [Quadro K5000 for Mac GPUスペック、特徴、ドライバ、サポート | NVIDIA](http://www.nvidia.co.jp/object/quadro-k5000-mac-jp.html)
65. [EVGA | 記事 | EVGA GTX 680 Mac 版グラフィックカード](http://jp.evga.com/articles/00730/)
66. [Sapphire、Mac Pro向けのRadeon HD 7950ビデオカード ～Mac OS X向けのEFIとWindows向けのUEFIを切り替え可能 - PC Watch](http://pc.watch.impress.co.jp/docs/news/20130321_592604.html)
67. [ASCII.jp：パーツ換装でMac Pro（Mid 2012）を徹底パワーアップ！ (4/6)](http://ascii.jp/elem/000/000/986/986376/index-4.html)
68.
69. [Khronos Groupが「OpenGL 4.5」をリリース | SourceForge.JP Magazine](http://sourceforge.jp/magazine/14/08/13/095100)
70. [OpenGL および OpenCL グラフィックスを扱う Mac コンピュータ - Apple サポート](https://support.apple.com/ja-jp/HT202823)