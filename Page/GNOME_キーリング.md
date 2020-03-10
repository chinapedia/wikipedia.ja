> この記事は[GNOME ](https://ja.wikipedia.org/wiki/GNOME_)から翻訳されています。


**GNOME キーリング**は、ユーザー名\[1\]やパスワード\[2\]、認証キーを適切なメタデータとともに保存するソフトウェア・アプリケーションである。センシティブなデータは、暗号化され、ユーザーのホームディレクトリにファイルの形で保存される。デフォルトのキーリングは、ログインパスワードを暗号化に用いるため、ユーザーは別のパスワードを新たに覚える必要がない\[3\]。[2009年](../Page/2009年.md "wikilink")、GNOME キーリングは、[OpenSolaris](../Page/OpenSolaris.md "wikilink")のデスクトップ環境の一部となった\[4\]。

GNOME キーリングは、*gnome-keyring-daemon*と名付けられたプロセスを用いるデーモンとして実装されている。アプリケーションは、*libgnome-keyring*というライブラリを用いることによって、パスワードの保存とリクエストを行うことができる。

GNOME キーリングは、[GNOME](../Page/GNOME.md "wikilink")デスクトップ環境の一部である。[2006年](../Page/2006年.md "wikilink")の時点で、GNOME キーリングは、[NetworkManager](https://ja.wikipedia.org/wiki/NetworkManager "wikilink")に統合され、[WEP](https://ja.wikipedia.org/wiki/WEP "wikilink")パスワードを保存することができた\[5\]。GNOME WebとEメールクライアントのGearyは、GNOME キーリングをパスワードの保存に用いている\[6\]。また、GNOME キーリングが存在するシステムでは、[Vala](https://ja.wikipedia.org/wiki/Vala "wikilink")で書かれたソフトウェアはパスワードの保存と取得が可能である\[7\]。

[2009年](../Page/2009年.md "wikilink")、[RHEL](https://ja.wikipedia.org/wiki/RHEL "wikilink")に含まれるパッケージに関する統計的報告によると、GNOME キーリングに依存するパッケージは、*kdelibs*パッケージに依存しているソフトウェアよりも脆弱性を持つことが少ない\[8\]。

## GNOME キーリングマネージャ

GNOME キーリングマネージャ（gnome-keyring-manager）は、GNOME キーリングのためのユーザーインターフェースである。GNOME2.22の時点で、このソフトは過去のものとなり、完全に[Seahorse](https://ja.wikipedia.org/wiki/Seahorse "wikilink")に置き換えられた\[9\]。

## 関連項目

  - [Seahorse](https://ja.wikipedia.org/wiki/Seahorse "wikilink")
  - [パスワードマネージャー](https://ja.wikipedia.org/wiki/パスワードマネージャー "wikilink")

## 脚注

## 外部リンク

  - [GNOME Keyring ウィキページ](https://wiki.gnome.org/Projects/GnomeKeyring) on wiki.gnome.org
  - [GNOME Keyring git](https://gitlab.gnome.org/GNOME/gnome-keyring/tree/master/) on git.gnome.org

[Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.