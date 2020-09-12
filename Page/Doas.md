> この記事は[Doas](https://ja.wikipedia.org/wiki/Doas)から翻訳されています。


**doas**（“do as”）は、[Unix](../Page/UNIX.md "wikilink") および [Unix 系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[プログラムである](../Page/プログラム_\(コンピュータ\).md "wikilink")。ユーザーが別のユーザーの権限レベルでプログラムを実行することを可能にする。多機能な [sudo](https://ja.wikipedia.org/wiki/sudo "wikilink") とは対照的に、小サイズでシンプルなプログラムである。

## 概要

doas は、設定ファイルに従って、指定されたコマンドを指定されたユーザに実行する権限を与える、というシンプルな機能を提供する。

doas は [OpenBSD](../Page/OpenBSD.md "wikilink") プロジェクトの成果物の一つである。OpenBSD で標準とされている他、[FreeBSD](../Page/FreeBSD.md "wikilink") や [NetBSD](../Page/NetBSD.md "wikilink") 等の [BSD ファミリー](../Page/BSDの子孫.md "wikilink") でも導入できる。ソースからビルドすることで [Linux](../Page/Linux.md "wikilink") でも使用できる。また派生として [Linux](../Page/Linux.md "wikilink") 向けのポータブルバージョン [OpenDoas](https://github.com/nholstein/OpenDoas) も別で開発されている。

## 設定ファイルの記述例

設定ファイル /etc/doas.conf で権限の定義を行う。公式マニュアルは [doas.conf.5](https://man.openbsd.org/doas.conf.5) 。

\#1. user1 に root での procmap 実行をパスワード入力無しで行える権限を与える場合

`permit nopass user1 as root cmd /usr/sbin/procmap`

\#2. user2 に完全な root 権限を与える場合（ただしパスワードが必要）

`permit user2 as root`

## 歴史

doas は 2015 年 10 月の OpenBSD 5.8 のリリースにおいて公開された。リリースノートで「base システムの sudo を [doas (1)](https://man.openbsd.org/doas) で置き換えました。sudo を使用する場合はパッケージから取得できます。」と説明された。\[1\]

doas は Ted Unangst によって開発された。\[2\] 「シンプルでセキュアなものをデフォルトにする」という OpenBSD プロジェクトの理念が反映されたものになっている。

## 脚注

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink")

1.
2.