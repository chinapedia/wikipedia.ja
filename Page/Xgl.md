> この記事は[Xgl](https://ja.wikipedia.org/wiki/Xgl)から翻訳されています。


**Xgl**（エックスジーエル）は[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")を[OpenGL](../Page/OpenGL.md "wikilink")を使って描画する[X Window Systemのアーキテクチャの](../Page/X_Window_System.md "wikilink")1つ。Xサーバを現在のピクセル描画モデルからベクトル描画モデルに移行するものである。[ノベル](https://ja.wikipedia.org/wiki/ノベル "wikilink")社のデビッド・レイブマン (David Reveman) によって開発された。

最近の[PCは](../Page/パーソナルコンピュータ.md "wikilink")3D機能付きの[グラフィックカードを搭載しているため](../Page/ビデオカード.md "wikilink")、Xglを使用することによりX上で高速で多彩なエフェクトが使用できる。しかしながら、[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")や[ATI](https://ja.wikipedia.org/wiki/ATI "wikilink")のようなグラフィックカードベンダーは[オープンソース](../Page/オープンソース.md "wikilink")のドライバーをほとんど提供していないので、現在のXサーバがサポートする全てのマシン上でXglが動作するわけではない\[1\]。

2005年に、非常に閉鎖的な開発のされ方が問題になり、一部の開発コミュニティで論争が起こったことがある。しかし、2006年のX開発者カンファレンスで実装が発表されてからは好意的に受け入れられた。

## バックエンド

OpenGL自体にはディスプレイを初期化したり、描画のコンテキストを操作する機能はない。そこでウィンドウシステム自体にこれらの指示を与えるようなバックエンドが必要になる。今のところこれには2つの実装があるが、初期化担当の部分を除けば違いはほとんどない。

### Xglx

*Xglx*は最初に実装されたXglバックエンドである。現在使用している[Xサーバ](https://ja.wikipedia.org/wiki/Xサーバ "wikilink")の上で動作し、XのOpenGL拡張によって描画する。これはちょうど、[Xnest](../Page/Xnest.md "wikilink")の機能と同じようなものである。しかし、このような動作方法だと3Dゴーグルやデュアルモニタのサポートが難しくなるということが、2006年のX開発者カンファレンスで[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")社によって指摘されている\[2\]。将来的には、これは開発者だけが使用するものになる予定である。

### Xegl

*Xegl*は将来のXglバックエンドである。描画担当のコードはXglxとほとんど違いはないが、OpenGL描画のための初期化と描画コンテキスト管理を、[Embedded GLのAPIによって行う](https://ja.wikipedia.org/wiki/Embedded_GL "wikilink")。現在の実装では[MesaによってLinuxフレームバッファーか](../Page/Mesa_3D.md "wikilink")[DRIによるグラフィックカードへの描画を行っている](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink")。2005年の段階では[RADEON](https://ja.wikipedia.org/wiki/RADEON "wikilink") R200上でしか動作しない。現在も開発中である。

## 類似の技術

  - [cairo](https://ja.wikipedia.org/wiki/cairo "wikilink")はXでベクトル描画を行うためのライブラリである。現在はXgl同様、[glitz](https://ja.wikipedia.org/wiki/glitz "wikilink")経由で動いているが、cairoをXgl上で動かすこともできる。また、[Qt](https://ja.wikipedia.org/wiki/Qt "wikilink") 4.0はArthurというベクトル描画システムを備えているが、これも同様にXgl上でも動かすことができる。
  - [GNUstep](https://ja.wikipedia.org/wiki/GNUstep "wikilink")では[DisplayGhostscript](https://ja.wikipedia.org/wiki/DisplayGhostscript "wikilink")によってデスクトップのベクトル描画が可能である。
  - [AIGLX](https://ja.wikipedia.org/wiki/AIGLX "wikilink")はX上でOpenGLによるエフェクトを可能にするためのプロジェクトである。[Fedora Projectによって開発された](https://ja.wikipedia.org/wiki/Fedora_Project "wikilink")。XglがXサーバを完全に置き換えてしまうのに対し、こちらはXの一部を拡張し、プロトコルを追加している。しかし、AIGLXはXglのバックエンドの一つになる可能性が高いと言われている。
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")では、OpenGLによるデスクトップの描画は[Quartz Extremeと呼ばれる技術によって使用されている](https://ja.wikipedia.org/wiki/Quartz_Extreme "wikilink")。
  - [Windows Vistaにおいても同様の技術が](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[Desktop Window Manager](https://ja.wikipedia.org/wiki/Desktop_Window_Manager "wikilink") (DWM) という名前で搭載されている。こちらはOpenGLではなく[DirectXを使っている](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")。
  - [Project Looking Glassは](https://ja.wikipedia.org/wiki/:en:Project_Looking_Glass "wikilink")[Javaによる](../Page/Javaプラットフォーム.md "wikilink")3Dデスクトップ環境である。Xglと同様、OpenGLによるハードウェアアクセラレーションを利用している。

## Compiz

[Compiz](https://ja.wikipedia.org/wiki/Compiz "wikilink")はXglを利用した最初の[ウィンドウマネージャ](https://ja.wikipedia.org/wiki/ウィンドウマネージャ "wikilink")である。デスクトップをキューブのように回転させたり、ウィンドウ動作をゼリーのように震わせる機能が特徴である。開発者はXglと同じである。現在はAIGLXの上でも動作する。

## 外部リンク

  - [Xgl](http://www.freedesktop.org/wiki/Software_2fXgl)
  - [Xegl](http://www.freedesktop.org/wiki/Xegl)
  - [X.orgメーリングリストでのアナウンスメント](http://lists.freedesktop.org/pipermail/xorg/2004-November/004358.html)
  - [openSUSE wiki: Xgl](http://www.opensuse.org/Xgl)　（[日本語](http://en.opensuse.org/JA-Xgl)）
  - [openSUSE wiki: Compiz](http://www.opensuse.org/compiz)
  - [Embedded GL 仕様書](http://www.khronos.org/opengles/spec.html)

<!-- end list -->

  - [ノベルのXglプレスリリース](http://xgl.opensuse.org/)
  - ノベルの[ポッドキャスト](https://ja.wikipedia.org/wiki/ポッドキャスト "wikilink")、[開発者デビッド・レイブマンが語るXglの基礎と未来](http://www.novell.com/podcast/Detailpage.jsp?id=55)

<!-- end list -->

  - [Videos of XGL on Novell Linux Desktop 10](http://www.linuxedge.org/?q=node/55)
  - [Slides, screenshots and a video with more effects](http://www.linuxedge.org/?q=node/58)
      - [Compizのデモムービー（avi）](http://www.freedesktop.org/~davidr/xgl-demo1.xvid.avi)
  - [勢いづくXグラフィックス](http://sourceforge.jp/magazine/06/02/10/0759255) japan.linux.com ([SourceForge.JP](https://ja.wikipedia.org/wiki/SourceForge.JP "wikilink") Magazine)

<!-- end list -->

  - [Article: The State of Linux Graphics](http://www.freedesktop.org/~jonsmirl/graphics.html) - 現在のXサーバ周りの技術の歴史と概要（[一部日本語訳](http://satek.org/dr/?q=node/2)）
  - [How Xgl works](http://principe.homelinux.net/) - Xglの動作原理解説。（[一部日本語訳](http://linux2ch.bbzone.net/index.php?HowXglWorks)）

<!-- end list -->

  - [Gentoo Linux XGL HowTo](http://gentoo-wiki.com/XGL)
  - [Ubuntu Linux XGL HowTo](http://chromakode.blogsome.com/2006/02/16/howto-compiz-xgl-on-ubuntu-for-the-morbidly-lazy-2) - Ubuntu 6.06LTS 向けXGL/Compizのインストール方法（英文）

<!-- end list -->

  - [Kororaa Linux](http://www.kororaa.org/) Xglを搭載したLinuxディストリビューション。ライブCDにより環境を汚さずXglが体験できる。

## 脚注

[Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:OpenGL](https://ja.wikipedia.org/wiki/Category:OpenGL "wikilink")

1.  [動作するグラフィックカードのリスト](http://gentoo-wiki.com/HARDWARE_Video_Card_Support_Under_XGL)
2.  [Using the Existing XFree86/X.Org Loadable Driver Framework to Achieve a Composited X Desktop](http://download.nvidia.com/developer/presentations/2006/xdevconf/compositing-with-current-framework.pdf)