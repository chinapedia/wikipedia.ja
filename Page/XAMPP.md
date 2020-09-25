> この記事は[XAMPP](https://ja.wikipedia.org/wiki/XAMPP)から翻訳されています。


**XAMPP**（**ザンプ**）とは、[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")の実行に必要な[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")を[パッケージとしてまとめたもので](../Page/パッケージソフトウェア.md "wikilink")、apachefriends.orgから提供されている。主として開発用あるいは学習用ではあるが、[イントラネット](../Page/イントラネット.md "wikilink")などにおいて[実運用環境として使われることもある](../Page/システム運用.md "wikilink")。

## 概要

[Apache](../Page/Apache_HTTP_Server.md "wikilink")（Webサーバ）、[MariaDB](https://ja.wikipedia.org/wiki/MariaDB "wikilink")（SQLデータベースサーバ；旧バージョンは[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")）と[Webプログラミング](../Page/Webプログラミング.md "wikilink")言語である[PHPや同目的で使われる](../Page/PHP_\(プログラミング言語\).md "wikilink")[Perl](../Page/Perl.md "wikilink")の4つの主要ソフトウェアと[phpMyAdmin](https://ja.wikipedia.org/wiki/phpMyAdmin "wikilink")などの管理ツール、さらに[SQLite](../Page/SQLite.md "wikilink")など、いくつかの補助的なソフトウェアと[ライブラリ](../Page/ライブラリ.md "wikilink")モジュールが含まれている。現在、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Solaris](../Page/Solaris.md "wikilink")で利用可能である。

本来、前述の複数のソフトウェアは個別に[インストール](../Page/インストール.md "wikilink")する必要があり、非常に手間がかかるが、XAMPPは一括してインストールするだけで、すぐに開発や運用が開始できる。パッケージとしての特性上、個々のソフトウエアのバージョンが必ずしも最新版で揃えられてはおらず、特にドライバモジュールに古いまま更新されていないものが含まれるが、開発用・学習用としては十分といえる。

XAMPPとは別に、ほぼ同趣旨の「[MAMP](https://ja.wikipedia.org/wiki/MAMP "wikilink")」がmamp.infoから提供されている。また[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")のサーバー版では、ほぼ同様のソフトウェア群を同梱して「[LAMP](https://ja.wikipedia.org/wiki/LAMP_\(ソフトウェアバンドル\) "wikilink")」として配布されることが多い。

また同様のWindows用サーバーソフト・インストーラーとして[VertrigoServ](https://ja.wikipedia.org/wiki/VertrigoServ "wikilink")もある。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")がこれらのソフトウェア群に対抗して[WISP](https://ja.wikipedia.org/wiki/WISP "wikilink")を示した。

## 名前の由来

XAMPPは以下の文字から構成されている。

  - X - Windows、Linux、macOS、Solarisのクロスプラットフォーム
  - A - ApacheのA
  - M - MariaDB（旧バージョンはMySQL）のM
  - P - PHPのP
  - P - PerlのP

元々は対応[OSは](../Page/オペレーティングシステム.md "wikilink")[Linux](../Page/Linux.md "wikilink")のみであり、その頭文字Lを付けLAMPPと称したが、後に複数のOSに対応したためLをXに変えXAMPPとなった。

## 他のRDBMSの利用

[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")については別にサーバを用意しておけば、PHPのpg関数が有効となり容易に接続できる。[Firebird](../Page/Firebird.md "wikilink")および[InterBase](../Page/InterBase.md "wikilink")については「php.ini」に手を加えれば、interbase関数が有効となり接続できる。[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")（2005以降）については、PHPのmssql関数（PDO経由を含む）が未対応で接続できないので、[ODBCの](../Page/Open_Database_Connectivity.md "wikilink")「SQL Native Client」ドライバを使ったDSNを作成しておき、そのDSN名をodbc関数のパラメータに指定すれば容易に接続できる。ただし日本語文字コードは[Shift-JIS](https://ja.wikipedia.org/wiki/Shift-JIS "wikilink")となる。

## バージョン情報

| XAMPP  | Apache | MariaDB | PHP    |
| ------ | ------ | ------- | ------ |
| 7.2.0  | 2.4.29 | 10.1.29 | 7.2.0  |
| 7.2.1  | 2.4.29 | 10.1.30 | 7.2.1  |
| 7.2.2  | 2.4.29 | 10.1.30 | 7.2.2  |
| 7.2.3  | 2.4.29 | 10.1.31 | 7.2.3  |
| 7.2.4  | 2.4.33 | 10.1.31 | 7.2.4  |
| 7.2.5  | 2.4.33 | 10.1.32 | 7.2.5  |
| 7.2.6  | 2.4.33 | 10.1.33 | 7.2.6  |
| 7.2.7  | 2.4.33 | 10.1.34 | 7.2.7  |
| 7.2.8  | 2.4.34 | 10.1.34 | 7.2.8  |
| 7.2.9  | 2.4.34 | 10.1.35 | 7.2.9  |
| 7.2.10 | 2.4.34 | 10.1.36 | 7.2.10 |
| 7.2.11 | 2.4.35 | 10.1.36 | 7.2.11 |
| 7.2.12 | 2.4.37 | 10.1.37 | 7.2.12 |
| 7.2.13 | 2.4.37 | 10.1.37 | 7.2.13 |
| 7.2.14 | 2.4.37 | 10.1.37 | 7.2.14 |
| 7.2.15 | 2.4.38 | 10.1.38 | 7.2.15 |
| 7.2.16 | 2.4.38 | 10.1.38 | 7.2.16 |
| 7.2.17 | 2.4.39 | 10.1.38 | 7.2.17 |
| 7.2.18 | 2.4.39 | 10.1.39 | 7.2.18 |
| 7.2.19 | 2.4.39 | 10.3.15 | 7.2.19 |
| 7.2.20 | 2.4.39 | 10.3.16 | 7.2.20 |
| 7.2.21 | 2.4.39 | 10.3.16 | 7.2.21 |
| 7.2.22 | 2.4.41 | 10.4.6  | 7.2.22 |
| 7.2.23 | 2.4.41 | 10.4.8  | 7.2.23 |
| 7.2.24 | 2.4.41 | 10.4.8  | 7.2.24 |
| 7.2.25 | 2.4.41 | 10.4.10 | 7.2.25 |
| 7.2.26 | 2.4.41 | 10.4.11 | 7.2.26 |
| 7.2.27 | 2.4.41 | 10.4.11 | 7.2.27 |
| 7.2.28 | 2.4.41 | 10.4.11 | 7.2.28 |
| 7.2.29 | 2.4.41 | 10.4.11 | 7.2.29 |
| 7.2.30 | 2.4.43 | 10.4.11 | 7.2.30 |
| 7.2.31 | 2.4.43 | 10.4.13 | 7.2.31 |
| 7.2.32 | 2.4.43 | 10.4.13 | 7.2.32 |
| 7.2.33 | 2.4.46 | 10.4.14 | 7.2.33 |
| 7.3.0  | 2.4.37 | 10.1.37 | 7.3.0  |
| 7.3.1  | 2.4.37 | 10.1.37 | 7.3.1  |
| 7.3.2  | 2.4.38 | 10.1.38 | 7.3.2  |
| 7.3.3  | 2.4.38 | 10.1.38 | 7.3.3  |
| 7.3.4  | 2.4.39 | 10.1.38 | 7.3.4  |
| 7.3.5  | 2.4.39 | 10.1.39 | 7.3.5  |
| 7.3.6  | 2.4.39 | 10.3.15 | 7.3.6  |
| 7.3.7  | 2.4.39 | 10.3.16 | 7.3.7  |
| 7.3.8  | 2.4.39 | 10.3.16 | 7.3.8  |
| 7.3.9  | 2.4.41 | 10.4.6  | 7.3.9  |
| 7.3.10 | 2.4.41 | 10.4.8  | 7.3.10 |
| 7.3.11 | 2.4.41 | 10.4.8  | 7.3.11 |
| 7.3.12 | 2.4.41 | 10.4.10 | 7.3.12 |
| 7.3.13 | 2.4.41 | 10.4.11 | 7.3.13 |
| 7.3.14 | 2.4.41 | 10.4.11 | 7.3.14 |
| 7.3.15 | 2.4.41 | 10.4.11 | 7.3.15 |
| 7.3.16 | 2.4.41 | 10.4.11 | 7.3.16 |
| 7.3.17 | 2.4.43 | 10.4.11 | 7.3.17 |
| 7.3.18 | 2.4.43 | 10.4.11 | 7.3.18 |
| 7.3.19 | 2.4.43 | 10.4.13 | 7.3.19 |
| 7.3.20 | 2.4.43 | 10.4.13 | 7.3.20 |
| 7.3.21 | 2.4.46 | 10.4.14 | 7.3.21 |
| 7.3.22 | 2.4.46 | 10.4.14 | 7.3.22 |
| 7.4.1  | 2.4.41 | 10.4.11 | 7.4.1  |
| 7.4.2  | 2.4.41 | 10.4.11 | 7.4.2  |
| 7.4.3  | 2.4.41 | 10.4.11 | 7.4.3  |
| 7.4.4  | 2.4.41 | 10.4.11 | 7.4.4  |
| 7.4.5  | 2.4.43 | 10.4.11 | 7.4.5  |
| 7.4.6  | 2.4.43 | 10.4.11 | 7.4.6  |
| 7.4.7  | 2.4.43 | 10.4.13 | 7.4.7  |
| 7.4.8  | 2.4.43 | 10.4.13 | 7.4.8  |
| 7.4.9  | 2.4.46 | 10.4.14 | 7.4.9  |
| 7.4.10 | 2.4.46 | 10.4.14 | 7.4.10 |

## 関連項目

  - [LAMP](https://ja.wikipedia.org/wiki/LAMP_\(ソフトウェアバンドル\) "wikilink")
  - [Apache](../Page/Apache_HTTP_Server.md "wikilink")
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")
  - [MariaDB](https://ja.wikipedia.org/wiki/MariaDB "wikilink")
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - [Perl](../Page/Perl.md "wikilink")

## 外部リンク

  - [XAMPP 日本語版](https://www.apachefriends.org/jp/index.html)
  - [MAMP（macOS 専用）、英語版](https://www.mamp.info/en/)

[Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")