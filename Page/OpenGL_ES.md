> この記事は[OpenGL ES](https://ja.wikipedia.org/wiki/OpenGL_ES)から翻訳されています。


**OpenGL ES**（OpenGL for Embedded Systems）は、主に[携帯電話](../Page/携帯電話.md "wikilink")などの[組み込みシステム](../Page/組み込みシステム.md "wikilink")で使用されている[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")用 [API](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink") である。

OpenGL ESは、従来から存在する（主に[デスクトップPC](https://ja.wikipedia.org/wiki/デスクトップPC "wikilink")や[ワークステーション](../Page/ワークステーション.md "wikilink")向けの）クロスプラットフォームなリアルタイム3DグラフィックスAPIである [OpenGL](../Page/OpenGL.md "wikilink") のサブセットである。OpenGL同様、グラフィックスハードウェア（[GPU](../Page/Graphics_Processing_Unit.md "wikilink")）の機能および性能を活用した高速なグラフィックス描画が可能となる。OpenGL ESはオープン仕様でロイヤリティフリーであり、適合試験にパスすれば誰でもOpenGL ES実装を謳えるため、[iOSや](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")[Android](https://ja.wikipedia.org/wiki/Android "wikilink")、[Symbian OSなどの携帯端末向けオペレーティングシステムで採用されているほか](https://ja.wikipedia.org/wiki/Symbian_OS "wikilink")、[プレイステーション3や](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")[ニンテンドー3DS](https://ja.wikipedia.org/wiki/ニンテンドー3DS "wikilink")にも採用されており、[ゲーム開発でも使用されている](../Page/ゲームプログラミング.md "wikilink")。OpenGL ESの仕様は、OpenGLと同様に[クロノス・グループ](https://ja.wikipedia.org/wiki/クロノス・グループ "wikilink")によって管理されている。

## バージョン

OpenGL ES 1.x系には1.0と1.1の2つが存在する。1.x系は、[グラフィックスパイプライン](../Page/グラフィックスパイプライン.md "wikilink")処理が固定された[シェーダー](https://ja.wikipedia.org/wiki/シェーダー "wikilink")（固定機能シェーダー）のみに対応しており、プログラム可能なシェーディング機能（[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")）には対応していない。このため、[フラットシェーディング](https://ja.wikipedia.org/wiki/フラットシェーディング "wikilink")あるいは[グーローシェーディング](https://ja.wikipedia.org/wiki/グーローシェーディング "wikilink")といった、カスタマイズ不可能な頂点単位の[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")（陰影計算）や質感表現のみがサポートされている。[ハードウェアアクセラレーション](https://ja.wikipedia.org/wiki/ハードウェアアクセラレーション "wikilink")がサポートされていない複雑な陰影処理や各種エフェクトなどの高度な特殊効果を実現する場合にはGPU側の支援は受けられなくなるため、 でない限りは動作速度は 。

OpenGL ES 2.0は、[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")に対応した仕様であり、シェーディング言語[GLSL](../Page/GLSL.md "wikilink") ESに対応する一方で固定機能シェーダーは削除されている。OpenGL ES 2.0は1.x系との完全な後方[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")はない。陰影計算・質感表現をプログラマブルシェーダーで記述することによって、GPUによる支援が受けられるようになる。

### OpenGL ES 1.0

OpenGL ES 1.0はOpenGL 1.3のサブセットとして[2003年](../Page/2003年.md "wikilink")に登場した。[Symbian OS](https://ja.wikipedia.org/wiki/Symbian_OS "wikilink") と [Android](https://ja.wikipedia.org/wiki/Android "wikilink") プラットフォームの公式3DグラフィックスAPIとして採用されている。また、[SCEによるOpenGL](https://ja.wikipedia.org/wiki/ソニー・コンピュータエンタテインメント "wikilink") ES 1.0の拡張版（）が[プレイステーション3の公式グラフィックスAPIの](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")１つとしてサポートされている\[1\]。

### OpenGL ES 1.1

OpenGL ES 1.1はOpenGL 1.5のサブセットとして、[2004年](../Page/2004年.md "wikilink")[8月9日](../Page/8月9日.md "wikilink")に発表。[Android](https://ja.wikipedia.org/wiki/Android "wikilink") 1.6、[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")、[iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")、[iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")等で広くサポートされている。1.0世代のハードウェアでもドライバーレベルのアップデートで1.1に対応可能とされる。

以下の機能がOpenGL ES 1.0に追加になっている。

  - バッファオブジェクト
  - 自動ミップマップ生成
  - 拡張テクスチャ処理
  - 頂点スキニング機能
  - ユーザー定義クリッププレーン
  - 拡張ポイントスプライト、ポイントスプライト配列
  - 静的・動的状態クエリー
  - テクスチャ描画
  - 新しいコア追加、プロファイル拡張

### OpenGL ES 2.0

OpenGL ES 2.0はOpenGL 2.0のサブセットとして[2007年](../Page/2007年.md "wikilink")に公開された。 iPhoneの3GS以降、iPod Touchの第3世代以降、iPad、Androidのバージョン2.2以降などでサポートされている。 プログラマブルシェーダーステージは[バーテックスシェーダー](https://ja.wikipedia.org/wiki/バーテックスシェーダー "wikilink")（[頂点シェーダー](https://ja.wikipedia.org/wiki/頂点シェーダー "wikilink")）と[フラグメントシェーダー](https://ja.wikipedia.org/wiki/フラグメントシェーダー "wikilink")（[ピクセルシェーダー](https://ja.wikipedia.org/wiki/ピクセルシェーダー "wikilink")）の2つをサポートする。頂点単位やピクセル単位の陰影計算・質感表現の制御がGPUにより支援される。

シェーディング言語はGLSL ES 1.0をサポートする。

なお、本家OpenGLはバージョン4.1でOpenGL ES 2.0互換プロファイルを扱うことができるようになっている (GL_ARB_ES2_compatibility)。

[WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink") 1.0は、ブラウザ上で利用できるOpenGL ES 2.0の派生規格であるが、細部に違いがある\[2\]。

### OpenGL ES 3.0

OpenGL ES 3.0は[2012年](../Page/2012年.md "wikilink")に発表された。2.0との後方[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")あり。 [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink") 10 ([Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink") 10) やOpenGL 3.2の[ジオメトリシェーダー](https://ja.wikipedia.org/wiki/ジオメトリシェーダー "wikilink")はサポートされないが、マルチレンダーターゲット機能やマルチサンプル[アンチエイリアス](https://ja.wikipedia.org/wiki/アンチエイリアス "wikilink")（MSAA）を標準サポートするようになり、またUniform BlockやTransform FeedbackなどのDirectX 10世代（[統合型シェーダーアーキテクチャ](https://ja.wikipedia.org/wiki/統合型シェーダーアーキテクチャ "wikilink")世代）の機能を多数サポートする。

シェーディング言語はGLSL ES 3.0をサポートする。

なお、本家OpenGLはバージョン4.3でOpenGL ES 3.0互換プロファイルを扱うことができるようになっている (GL_ARB_ES3_compatibility)。

WebGL 2.0は、ブラウザ上で利用できるOpenGL ES 3.0の派生規格であるが、細部に違いがある\[3\]。

### OpenGL ES 3.1

OpenGL ES 3.1は[2014年](../Page/2014年.md "wikilink")[3月17日](../Page/3月17日.md "wikilink")に発表された。ジオメトリシェーダーおよびDirectX 11 (Direct3D 11) やOpenGL 4.0の[テッセレーション](https://ja.wikipedia.org/wiki/テッセレーション "wikilink")シェーダーはサポートされないが、本家OpenGL 4.3で採用された[コンピュートシェーダー](https://ja.wikipedia.org/wiki/コンピュートシェーダー "wikilink")などを導入している\[4\]。3.0世代のハードウェアでもドライバーレベルのアップデートで3.1に対応可能とされる\[5\]。

シェーディング言語はGLSL ES 3.1をサポートする。

なお、本家OpenGLはバージョン4.5でOpenGL ES 3.1互換プロファイルを扱うことができるようになっている (GL_ARB_ES3_1_compatibility)。

### OpenGL ES 3.2

OpenGL ES 3.2は[2015年](../Page/2015年.md "wikilink")[8月10日](../Page/8月10日.md "wikilink")に発表された。**Google Android Extension Pack** (AEP) にて拡張として定義されていた機能\[6\]、すなわちジオメトリシェーダーおよびテッセレーションシェーダー、そしてテクスチャ圧縮技術であるのサポートが標準化されたほか、本家OpenGL 4シリーズ同等の機能が多数追加される\[7\]。

シェーディング言語はGLSL ES 3.2をサポートする。

なお、本家OpenGLは2015年8月に追加されたARB拡張により、OpenGL ES 3.2互換プロファイルを扱うことができるようになっている (GL_ARB_ES3_2_compatibility)。

## iOS/tvOSでの非推奨化

[アップルは](../Page/アップル_\(企業\).md "wikilink")[WWDC](https://ja.wikipedia.org/wiki/WWDC "wikilink") 2018で自社プラットフォームにおけるOpenGL/OpenCLの非推奨化を発表し、[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") 12および[tvOS](https://ja.wikipedia.org/wiki/tvOS "wikilink") 12において（サポートはまだ打ち切られないものの）OpenGL ESは非推奨APIとなった\[8\]\[9\]。iOSがネイティブにサポートするOpenGL ESのバージョンは3.0が最後となっている\[10\]。

OpenGL ESの代替として推奨されているAPIは[Metalだが](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")、MetalはOpenGL ESよりもハードウェア層に近い下位レベルのAPIであり、基本的に[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")開発向けではなく[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")開発向けである。Metal APIを利用してOpenGL ESを実現する**MoltenGL**ライブラリが[Brenwill Workshop](http://brenwill.com/)によって開発されている\[11\]。

## 出典

<references/>

## 関連項目

  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [GLSL](../Page/GLSL.md "wikilink")
  - [WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink")
  - [Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")
  - [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")
  - [Metal (API)](https://ja.wikipedia.org/wiki/Metal_\(API\) "wikilink")
  - [Vulkan (API)](https://ja.wikipedia.org/wiki/Vulkan_\(API\) "wikilink")

## 外部リンク

  - [公式ウェブサイト](http://www.khronos.org/opengles/)（英語）

[Category:OpenGL](https://ja.wikipedia.org/wiki/Category:OpenGL "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  [西川善司の3DゲームファンのためのPS3アーキテクチャ講座](http://game.watch.impress.co.jp/docs/20060329/3dps3.htm)
2.  [WebGL Specification](https://www.khronos.org/registry/webgl/specs/latest/1.0/)
3.  [WebGL 2 Specification](https://www.khronos.org/registry/webgl/specs/latest/2.0/)
4.  [Khronos，「OpenGL ES 3.1」を発表。OpenGL 4.xとの親和性を高める改良を施す - 4Gamer.net](http://www.4gamer.net/games/107/G010729/20140318012/)
5.  [What’s New in OpenGL ES](https://www.khronos.org/assets/uploads/developers/library/2014-gdc/Khronos-OpenGL-ES-GDC-Mar14.pdf)
6.  [スマホでPS4世代のグラフィックスを実現？ OpenGL ES 3.1の拡張機能「Google AEP」や次世代OpenGLの話をKhronos Group代表に聞いてみた - 4Gamer.net](http://www.4gamer.net/games/107/G010729/20140827118/)
7.  [Khronos Expands Scope of 3D Open Standard Ecosystem - Khronos Group Press Release](https://www.khronos.org/news/press/khronos-expands-scope-of-3d-open-standard-ecosystem)
8.  [iOSの新機能 - Apple Developer](https://developer.apple.com/jp/ios/whats-new/)
9.  [tvOSの新機能 - Apple Developer](https://developer.apple.com/jp/tvos/whats-new/)
10. [OpenGL ES | Apple Developer Documentation](https://developer.apple.com/documentation/opengles/)
11. [MoltenGL | Metal performance with OpenGL ES](https://moltengl.com/moltengl/)