> この記事は[Thunar](https://ja.wikipedia.org/wiki/Thunar)から翻訳されています。


**Thunar**（ソナー）は[Linux](../Page/Linux.md "wikilink")その他の[Unix系](../Page/Unix系.md "wikilink")システム用の[ファイルマネージャ](../Page/ファイルマネージャ.md "wikilink")であり、[GTK+ 2ツールキットを用いており](https://ja.wikipedia.org/wiki/GTK+ "wikilink")、[Xfce](../Page/Xfce.md "wikilink") version 4.4 RC1 以降に同梱されている。Thunar は Benedikt Meurer によって開発されており、もともとは Xfce のファイルマネージャであった XFFM を置き換えることを目的としていた。Thunar は当初は Filer と呼ばれていた。しかし名称の重なりを避けるために Thunar に改名された。

Thunar プロジェクトの主な目標は、軽快でクリーンで使い易いファイルマネージャを作ることである。[ファイル (GNOME)](../Page/ファイル_\(GNOME\).md "wikilink") や [Konqueror](../Page/Konqueror.md "wikilink") など他のいくつかの Linux ファイルマネージャよりも素早く起動し反応が良いように設計されている\[1\]。アクセシビリティは、プロジェクトのもうひとつの目標であり、（例えば[GNOME Accessibility Toolkitなどの](https://ja.wikipedia.org/wiki/Accessibility_Toolkit "wikilink")）ユーザ支援技術を使って達成されている。Xfce の他の部分同様、Thunar は [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") などで示されている標準に基づくように設計されている\[2\]。Thunar の設計はシンプルで軽量だとはいえ、その機能はプラグインによって拡張することができる。

Thunar は[北欧神話](../Page/北欧神話.md "wikilink")の雷神[トール](../Page/トール.md "wikilink")（Thor）に因んで名付けられた。

## インタフェース

Thunar は [Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")の世界における無数のツリー表示によるファイルマネージャとは違った[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink") の構築を意図している。

そのインタフェースは Thunar の核となるコードが書かれるより前に開発された。初めに、最小限に動作するソフトウェアの原型が[Python](../Page/Python.md "wikilink")で書かれた。機能が追加されユーザインタフェース要素がユーザ試験に応じて繰り返し変更された。

## API

Thunar ではサードパーティの開発者のために [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") が提供されている：

  - "thunar-vfs" は高度なファイルシステム操作のための高機能クロスプラットフォーム API を提供する。
  - "thunarx" はファイルマネージャ自体の機能拡張を構築するためのライブラリを提供する。

また、様々なファイル形式でのコンテキストメニューに配置されるスクリプトを書くことでも Thunar を拡張できる。

[Thunar-about-logo.png](https://ja.wikipedia.org/wiki/File:Thunar-about-logo.png "fig:Thunar-about-logo.png")

## 出典

<references />

## 外部リンク

  - [xfce:thunar:start ［Xfce Docs］](http://docs.xfce.org/xfce/thunar/start)

[Category:ファイルマネージャ](https://ja.wikipedia.org/wiki/Category:ファイルマネージャ "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [Thunar Memory Usage](http://thunar.xfce.org/wiki/memory_usage)
2.  [ThunarWiki: Standards](http://thunar.xfce.org/wiki/requirements:standards)