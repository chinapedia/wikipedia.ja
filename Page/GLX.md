> この記事は[GLX](https://ja.wikipedia.org/wiki/GLX)から翻訳されています。


[Linux_graphics_drivers_DRI_current.svg](https://ja.wikipedia.org/wiki/File:Linux_graphics_drivers_DRI_current.svg "fig:Linux_graphics_drivers_DRI_current.svg") versus [direct rendering](https://ja.wikipedia.org/wiki/Direct_Rendering_Infrastructure "wikilink").\]\] **GLX**（"Open**GL** Extension to the **X** Window System" の頭文字語）は [OpenGL](../Page/OpenGL.md "wikilink") と [X Window System](../Page/X_Window_System.md "wikilink") をつなぐ[バインディングを提供する](https://ja.wikipedia.org/wiki/束縛_\(情報工学\) "wikilink")。X Window System によって提供されたウィンドウ内でプログラムが OpenGL を使えるようにする。

## 歴史

GLX は[シリコングラフィックス](../Page/シリコングラフィックス.md "wikilink")によってつくられ現在バージョン1.4である。DRI と [Mesa](../Page/Mesa_3D.md "wikilink") の両方とともに GLX は X11R6.7.0 から [X.Org Foundation](../Page/X.Org_Server.md "wikilink") のバージョンの X Window System に、バージョン4.0より [XFree86 プロジェクトのバージョンに含まれている](../Page/XFree86.md "wikilink")。

## 機能

GLX は三つの部分からなる。

  - X Window System のアプリケーションに OpenGL の関数を提供する [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")
  - クライアント（OpenGL アプリケーション）が X サーバ（表示を担うソフトウェア）に3Dレンダリングコマンドを送れるようにする、X プロトコルの拡張。クライアントとサーバは異なるコンピュータで動作していてもよい。
  - レンダリングコマンドをクライアントから受け取りインストールされた OpenGL ライブラリに渡すという X サーバの拡張。もしハードウェアアクセラレーションの効いたライブラリが利用できなければ、通常 [Mesa 3D](../Page/Mesa_3D.md "wikilink") になり、これはソフトウェア内のすべてを扱えるが、通常ハードウェアアクセラレーションの効いたライブラリよりずっと遅い。

クライアントとサーバが同じコンピュータと、適切なドライバを使ったアクセラレーションの効いた3Dグラフィックスカード上で動作していれば、最初の二つのコンポーネントは [DRI](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink") によってバイパスできる。この場合、クライアントはグラフィックハードウェアに直接アクセスできる。

サーバのサポートする [GLX visual](https://ja.wikipedia.org/wiki/GLX_visual "wikilink") を含む GLX についての診断情報の多くは *glxinfo* コマンドを使って見つけられる。デモユーティリティ *glxgears* は3Dレンダリング設定の速さの大まかな見積もりを提供する。より新しいバージョンの glxgears では速さを見るには *-info* オプションを使う必要がある。しかし、glxgears はベンチマークツールではなく、そのように使うべきではない。ハードウェアアクセラレーションの効いたライブラリが正しくインストールされているのかを検証するために使うためだけのものである。

## 脚注

## 関連項目

  - [AIGLX](https://ja.wikipedia.org/wiki/AIGLX "wikilink")
  - [GLUT](../Page/OpenGL_Utility_Toolkit.md "wikilink")

## 外部リンク

  -
  -
[Category:OpenGL](https://ja.wikipedia.org/wiki/Category:OpenGL "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")