> この記事は[Freedesktop.org](https://ja.wikipedia.org/wiki/Freedesktop.org)から翻訳されています。


**freedesktop.org**（フリーデスクトップドットオルグ。**fd.o**（エフディードットオー）などと略されることもある）は、[Unix系](../Page/Unix系.md "wikilink")の[システム](../Page/システム.md "wikilink")の環境の[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")（もっぱら[X Window Systemを利用する](../Page/X_Window_System.md "wikilink")）の、相互運用性の向上と共通基盤技術の整備を目指したプロジェクトである。[CDEのライセンスが](../Page/Common_Desktop_Environment.md "wikilink")、しがらみのため自由になるのに時間を要していた（2012年に至ってやっとLGPLv2となったが、もはやほとんどニュースにならなかった）ために乱立気味であったUnix系のデスクトップ環境において、無用な重複と、混乱を招くだけの無用な差異を無くすことなどが主な目的である。2000年3月、[ハヴォック・ペニントン](https://ja.wikipedia.org/wiki/ハヴォック・ペニントン "wikilink")が設立した。

開発などはユーザの視点で行われている。[KDE](../Page/KDE.md "wikilink")と[GNOME](../Page/GNOME.md "wikilink")に代表される各デスクトップ環境を統一した唯一の環境、といったようなものを作る、というような目的ではなく、各開発フレームワーク間の差異（非本質的な）がユーザから見えないようにすること、などといった共通化を目的としている。また、特にGNOMEとKDEは、このプロジェクトと密接に連携している。[Xfce](../Page/Xfce.md "wikilink")も、4.0版以降では準拠とした。

2006年に、デスクトップ環境の共通インタフェースを集めた[Portland](https://ja.wikipedia.org/wiki/Portland_Project "wikilink") 1.0 (`xdg-utils`) をリリースしている\[1\]。

かつて**X Desktop Group**と名乗っていたため、"XDG" という省略形も、ディレクトリ名などあちこちにいまだによく使われている。

## 傘下プロジェクト

[Free_and_open-source-software_display_servers_and_UI_toolkits.svg](https://ja.wikipedia.org/wiki/File:Free_and_open-source-software_display_servers_and_UI_toolkits.svg "fig:Free_and_open-source-software_display_servers_and_UI_toolkits.svg") freedesktop.orgはいくつかの関連プロジェクトを傘下におさめている\[2\]\[3\]。以下に主なものを挙げる:

  - *[X.Org Server](../Page/X.Org_Server.md "wikilink")*: X11の公式[リファレンス実装](../Page/リファレンス実装.md "wikilink")。現在のバージョンは、ライセンスを変える前の[XFree86](../Page/XFree86.md "wikilink")から分岐したもの。
  - [D-BUS](../Page/D-Bus.md "wikilink"): KDEの[DCOP](../Page/DCOP.md "wikilink")やGNOMEの[Bonobo](../Page/Bonobo.md "wikilink")のようなメッセージバス
  - *[ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")*: X11のドラッグ・アンド・ドロップは一貫した手法が確立していない。
  - [Hardware Abstract Layer](https://ja.wikipedia.org/wiki/Hardware_Abstract_Layer "wikilink") ([HAL](../Page/HAL_\(ソフトウェア\).md "wikilink")): [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に依存する部分を層として切り出すプロジェクト。
  - [fontconfig](https://ja.wikipedia.org/wiki/fontconfig "wikilink"): フォント検索などを行うライブラリ
  - *[Xft](https://ja.wikipedia.org/wiki/Xft "wikilink")*: [FreeType](../Page/FreeType.md "wikilink")ライブラリを使った新たなフォントライブラリ
  - [cairo](https://ja.wikipedia.org/wiki/cairo "wikilink"): デバイスに依存しない[ベクトルグラフィックスライブラリ](https://ja.wikipedia.org/wiki/ベクトル画像 "wikilink")
  - [ダイレクト・レンダリング・インフラストラクチャ](https://ja.wikipedia.org/wiki/ダイレクト・レンダリング・インフラストラクチャ "wikilink") (DRI): Xサーバを経由しないでユーザーアプリケーションがグラフィックハードウェアにアクセスするためのインタフェース
  - [GStreamer](../Page/GStreamer.md "wikilink"): クロスプラットフォームマルチメディアフレームワーク
  - [Mesa 3D](../Page/Mesa_3D.md "wikilink"): [OpenGL](../Page/OpenGL.md "wikilink")実装の1つ
  - [XCB](../Page/XCB.md "wikilink"): [Xlib](https://ja.wikipedia.org/wiki/Xlib "wikilink")の新たな実装
  - [GTK-Qt](https://ja.wikipedia.org/wiki/GTK-Qt "wikilink")エンジン: [Qt](../Page/Qt.md "wikilink")を使って[ウィジェットを描画するGTK](https://ja.wikipedia.org/wiki/ウィジェット_\(GUI\) "wikilink")+ 2エンジン。GTK+ 2アプリケーションの[ルック・アンド・フィールをKDEと同じにする](https://ja.wikipedia.org/wiki/Look_and_feel "wikilink")。
  - [Poppler](https://ja.wikipedia.org/wiki/Poppler "wikilink"): PDFレンダリングライブラリ
  - [Wayland](https://ja.wikipedia.org/wiki/Wayland "wikilink"): Linuxデスクトップのための、完璧なGUI体験（テアリング、ラグ、再描画、フリッカーをユーザーは決して目にしない）を提供することを目的とした軽量ディスプレイサーバー
  - [Avahi](../Page/Avahi.md "wikilink"): フリーな[Zeroconf](https://ja.wikipedia.org/wiki/Zeroconf "wikilink")実装。ただし、現在はfreedesktop.org傘下ではない。

## 目的

このプロジェクトは定式化された標準規格を定めることが目的ではない。むしろ、なるべく早く相互運用性の問題を明らかにし、対処することを目的としている。

1.  既存の仕様、標準、Xデスクトップの相互運用性に関する文書を集め、広く利用できる形で保管する。
2.  Xデスクトップに共通な新たな仕様や標準規格の開発を促進する。
3.  デスクトップ環境の標準規格を、[Linux Standard Base](../Page/Linux_Standard_Base.md "wikilink")、[ICCCMなどの全体的な標準規格とするべく努力する](../Page/Inter-Client_Communication_Conventions_Manual.md "wikilink")。
4.  特定のXデスクトップでそれら標準規格の実装を行う。
5.  Xデスクトップ技術に関するアイデアを共有するための中立組織として働く。
6.  Xデスクトップの相互運用性とフリーなXデスクトップの普及促進のための技術実装を行う。
7.  Xデスクトップとその標準をアプリケーション開発者に普及させるべく働く。
8.  フリーなオペレーティングシステムのカーネル開発者、X Window System自体の開発者、OSディストリビューションなどとデスクトップ関連問題について話し合う。
9.  以上のような目的に沿ったプロジェクトに対して、[CVS](../Page/Concurrent_Versions_System.md "wikilink")、Webホスティング、メーリングリストなどのリソースを提供する。

## 出典

<references />

## 参考文献

  - [The Big freedesktop.org Interview](http://osnews.com/story.php?news_id=5215)（Rayiner Hashem & Eugenia Loli-Queru, OSNews, [2003年](../Page/2003年.md "wikilink")[11月24日](../Page/11月24日.md "wikilink")）

## 関連項目

  - [OSSホスティングサービスの比較](https://ja.wikipedia.org/wiki/OSSホスティングサービスの比較 "wikilink")

## 外部リンク

  - [freedesktop.org - Home (wiki)](http://freedesktop.org/)

[Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink") [Category:フリーソフトウェアのプロジェクト](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアのプロジェクト "wikilink") [Category:オープンソース文化・運動](https://ja.wikipedia.org/wiki/Category:オープンソース文化・運動 "wikilink")

1.  [Portland points desktop Linux at $10 billion market](http://desktoplinux.com/news/NS7435528984.html), *DesktopLinux.com*, 2006年10月11日
2.  [freedesktop.org - FreedesktopProjects](http://freedesktop.org/wiki/FreedesktopProjects)
3.  [freedesktop.org - Software](http://freedesktop.org/wiki/Software)