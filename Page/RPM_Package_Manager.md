> この記事は[RPM Package Manager](https://ja.wikipedia.org/wiki/RPM_Package_Manager)から翻訳されています。


**RPM**（アールピーエム、**R**PM **P**ackage **M**anager）は[レッドハット](../Page/レッドハット.md "wikilink")が開発した[ソフトウェア](../Page/ソフトウェア.md "wikilink")のパッケージを管理するためのシステム ([パッケージ管理システム](../Page/パッケージ管理システム.md "wikilink"))、及びコマンド。以前は**R**ed Hat **P**ackage **M**anagerの略だった。"[.rpm](https://ja.wikipedia.org/wiki/RPM_\(ファイルフォーマット\) "wikilink")"拡張子のファイルを利用する。

## 概要

主に[Linux](../Page/Linux.md "wikilink")の[ディストリビューションのうち](../Page/Linuxディストリビューション.md "wikilink")、[レッドハット](../Page/レッドハット.md "wikilink")が提供するものだけでなく、独自のカスタマイズを含めながら[SUSE Linux](../Page/SUSE.md "wikilink")、[Vine Linuxなどの](../Page/Vine_Linux.md "wikilink")[RPM系ディストリビューションで使われる](https://ja.wikipedia.org/wiki/Linuxディストリビューション#主なLinuxディストリビューション "wikilink")。

RPMは、パッケージを[cpio](https://ja.wikipedia.org/wiki/cpio "wikilink")形式で[アーカイブしており](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\)#アーカイブファイル "wikilink")、その中には、独自のspec[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")、及び[バイナリ](../Page/バイナリ.md "wikilink")、または[ソースコード](../Page/ソースコード.md "wikilink")が含まれている。パッケージ管理のための[データベース](../Page/データベース.md "wikilink")には[Berkeley DBを採用しており](../Page/Berkeley_DB.md "wikilink")、[インストール](../Page/インストール.md "wikilink")時、削除時、パッケージの問い合わせ時にはこのデータベースが利用される。データベース管理のためのコマンドオプションもrpmコマンドに含まれている。\[1\]

specファイルには、パッケージの名前、概要、依存するパッケージ、バイナリパッケージのインストールパス、インストール前に実行するスクリプト、インストール後に実行するスクリプトなどが書かれている。インストール時には、記載されたスクリプトを実行して、サーバの停止及び復帰、システムユーザーの追加などを行い、システムの安全性を保つ。

specファイルは、宣言部と実行部に分かれている。宣言部には、パッケージの説明的な詳細を書き、実行部は、スクリプトとしての役割を果たしている。

パッケージのインストールには、ローカルパッケージ、及び[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[FTPを通じたネットワークからのパッケージに対応している](../Page/File_Transfer_Protocol.md "wikilink")。ただし、依存性の解決は行わず、依存性に欠如があった場合は、ユーザーが独自にパッケージをインストールするか、[YUM](https://ja.wikipedia.org/wiki/Yellow_dog_Updater,_Modified "wikilink")、[APT](../Page/APT.md "wikilink") for rpmといった別のツールを使って解決しなければいけない。独自にソースコードからインストールした場合は、パッケージ管理の対象にならず、この場合は、依存性の解決には利用されない。

RPMは、通常はバイナリのインストールに使われるが、ソースコードからのパッケージ作成もサポートしている。パッケージをspecファイルに従ってその場で作成し、インストールすることになる。

RPMは、[C言語](../Page/C言語.md "wikilink")で書かれ、C言語、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")などの[言語バインディング](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")も提供、または独自に作成されており、これにより、コマンド以外からもRPMのパッケージを扱うことが出来る。\[2\]

## 関連項目

  - [Linux Standard Base](../Page/Linux_Standard_Base.md "wikilink")
  - [APT](../Page/APT.md "wikilink")

## 出典

## 外部リンク

  - [rpm.org](http://www.rpm.org/)
  - [rpm package manager](http://rpm5.org/)

[Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:フリーパッケージ管理システム](https://ja.wikipedia.org/wiki/Category:フリーパッケージ管理システム "wikilink")

1.
2.