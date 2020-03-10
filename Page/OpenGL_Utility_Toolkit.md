> この記事は[OpenGL Utility Toolkit](https://ja.wikipedia.org/wiki/OpenGL_Utility_Toolkit)から翻訳されています。


**OpenGL Utility Toolkit** (**GLUT**) とは、リアルタイム[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")用[APIのひとつである](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")[OpenGL](../Page/OpenGL.md "wikilink")のバージョン1.1\[1\]に準拠したユーティリティツールキット（[ライブラリ](../Page/ライブラリ.md "wikilink")）である。GLUTは[C言語](../Page/C言語.md "wikilink")形式の関数群で構成されている。

[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink") (SGI) や（）によって開発された。

[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")などの[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) で使用できる。

## 概要

OpenGL向けの基本的な拡張ライブラリとしては、[同次変換](https://ja.wikipedia.org/wiki/同次変換 "wikilink")行列の生成などを補助するGLU () が存在するが、GLUTはGLUにない下記の機能を持つ。

  - OpenGL描画のための複数ウィンドウ
  - [コールバック](https://ja.wikipedia.org/wiki/コールバック "wikilink")形式のイベント処理
  - マウスやキーボードなどの基本入力デバイス対応
  - アイドリングとタイマー
  - シンプルな[ポップアップメニュー](https://ja.wikipedia.org/wiki/ポップアップメニュー "wikilink")
  - ソリッド／[ワイヤーフレーム](https://ja.wikipedia.org/wiki/ワイヤーフレーム "wikilink")の基本図形（[球](../Page/球面.md "wikilink")、[立方体](https://ja.wikipedia.org/wiki/立方体 "wikilink")、[円錐](../Page/円錐.md "wikilink")、[トーラス](../Page/トーラス.md "wikilink")、および[ティーポット](https://ja.wikipedia.org/wiki/Utah_teapot "wikilink")）の生成機能
  - ビットマップ／ストローク[フォント](../Page/フォント.md "wikilink")
  - その他のウィンドウ管理関数

GLUTは単なるユーティリティにとどまらず、フレームワーク的な機能も併せて持っており、シンプルな構成でありながら初学者にとって面倒なウィンドウ[ウィジェット](https://ja.wikipedia.org/wiki/ウィジェット "wikilink")の生成処理などを自動化してくれるため、OpenGLの補助ライブラリの中でも特に広く使用されており、グラフィックスプログラムのプロトタイピングや入門書などでも用いられている\[2\]。

OpenGL関数に`gl`プレフィックスが付けられているのと同様に、GLU関数には`glu`プレフィックスが、またGLUT関数には`glut`プレフィックスがそれぞれ付けられている。

GLUTはソースコードが公式サイトにて公開されている。[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")ではなく、また無保証だが、ライセンス料を支払うことなく無償で利用できる\[3\]。

なお、[Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") ([Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")) 用のGLUT風フレームワークライブラリとして、DXUTが存在する\[4\]。DXUTは[C++](../Page/C++.md "wikilink")専用で、GLUTのようなコールバック形式のフレームワークに加えて、ボタンやドロップダウンリストなどの[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")部品もサポートしている。

## 問題点

GLUTはメインループに突入した後、終了時にウィンドウをクローズする際にメインループから抜け出す手段が用意されておらず、exit関数を使うなどして半強制終了するしかない。 また、マウスホイールなどのサポートがない。 GLUTからフォークし、これらの欠点を改善したFreeGLUTなどの派生ライブラリが開発されている。

なお、GLUTは最終版3.7のリリースが1998年であるが、その後[グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")の進化とともに廃止されたOpenGL固定機能（OpenGL 3.1以降で廃止）に依存している。そのため、最新のOpenGL機能を利用するときに、OpenGLレンダリングコンテキストの作成処理が隠ぺいされているGLUTでは不都合がある\[5\]。 レンダリングコンテキストの作成時にプロファイル種別を指定できるなどの新しい後発ライブラリやツールキットによって、GLUTはとって代わられつつある。

## 脚注

## 関連項目

  - [OpenGL](../Page/OpenGL.md "wikilink")

## 外部リンク

  - [GLUT documentation](http://www.opengl.org/documentation/specs/glut/spec3/spec3.html)
  - [OpenGLUT](http://openglut.sourceforge.net/)
  - [FreeGLUT](http://freeglut.sourceforge.net/)
  - [GLUTによる「手抜き」OpenGL入門](http://www.wakayama-u.ac.jp/~tokoi/opengl/libglut.html)

[Category:OpenGL](https://ja.wikipedia.org/wiki/Category:OpenGL "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  GLUT 3.7同梱のREADMEを参照のこと。
2.
3.  GLUT 3.7同梱のNOTICEを参照のこと。
4.  [DXUT プログラミング ガイド](https://msdn.microsoft.com/ja-jp/library/bb173316.aspx)
5.  [床井研究室 - (1) GLFW で OpenGL を使う](http://marina.sys.wakayama-u.ac.jp/~tokoi/?date=20120906)