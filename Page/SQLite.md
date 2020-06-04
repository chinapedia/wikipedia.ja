> この記事は[SQLite](https://ja.wikipedia.org/wiki/SQLite)から翻訳されています。


**SQLite**（エスキューライト\[1\]\[2\]、エスキューエライト\[3\]\[4\]）は、[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")の軽量な[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) である。

## 概要

[サーバ](../Page/サーバ.md "wikilink")としてではなく[アプリケーションに組み込んで利用される](../Page/アプリケーションソフトウェア.md "wikilink")[データベース](../Page/データベース.md "wikilink")である\[5\]。 一般的なRDBMSと違い、[APIは単純に](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")を呼び出すだけであり、データの保存に単一の[ファイルのみを使用することが特徴である](../Page/ファイル_\(コンピュータ\).md "wikilink")。バージョン3.3.8からは[全文検索](../Page/全文検索.md "wikilink")のFTS1モジュールがサポートされた。その後 FTS2 - FTS3 と強化を続けバージョン3.7.4からはFTS4モジュールがサポートされている。

## 特徴

  - [SQL](../Page/SQL.md "wikilink")92の機能の多くを実装
  - 著作権を放棄し[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")に帰している
  - サーバではなくライブラリ
      - ライブラリは数百KB程度のフットプリント
      - Cランタイム以外の別途ライブラリを必要としない
      - 管理ツールによるセットアップやメンテナンスを必要としない
      - [コマンドラインツールも使える](../Page/コマンドラインインタプリタ.md "wikilink")
  - [バイトオーダに依存しない](https://ja.wikipedia.org/wiki/エンディアン "wikilink")（2.6.3以降）、可搬性のある単一ファイル
      - 最大128TiBまで
      - ファイルを使わない、揮発性の[インメモリデータベース](https://ja.wikipedia.org/wiki/インメモリデータベース "wikilink")としても利用可能
  - [データ型](../Page/データ型.md "wikilink")を指定する必要がない
      - サポートしている型は、Null/Integer/Real/Text/BLOBのみ
      - [Unicode](../Page/Unicode.md "wikilink")のサポート
      - BLOBはメモリの許す限り
      - ROWIDを持っている（ただし3.6.18以前は外部制約キーの仕組みがない）
  - [トランザクション](../Page/トランザクション.md "wikilink")のサポート
      - [スレッドセーフ](../Page/スレッドセーフ.md "wikilink")である（[バイナリ](../Page/バイナリ.md "wikilink")による配布ではリコンパイルが必要な場合もある）
  - ビューのサポート
  - トリガーのサポート
  - [C言語](../Page/C言語.md "wikilink")を使って関数を追加できる
  - [Tcl](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")[バインディングを配布キットに標準添付している](../Page/束縛_\(情報工学\).md "wikilink")
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")5、[Python](../Page/Python.md "wikilink") 2.5、[Adobe AIRで標準サポート](https://ja.wikipedia.org/wiki/Adobe_AIR "wikilink")
  - その他、[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[D](../Page/D言語.md "wikilink")、[Curl](../Page/Curl_\(プログラミング言語\).md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Delphi](../Page/Delphi.md "wikilink")など多数の[プログラミング言語](../Page/プログラミング言語.md "wikilink")用のバインディング
  - [全文検索](../Page/全文検索.md "wikilink")のFTS1[モジュール](../Page/モジュール.md "wikilink")がサポートされ、[SQL](../Page/SQL.md "wikilink")文で[全文検索](../Page/全文検索.md "wikilink")インデックスに対して検索できる
  - [Android](../Page/Android.md "wikilink")端末の標準ライブラリとして採用されている

## 解説

SQLiteは本体[プログラムに対して](../Page/プログラム_\(コンピュータ\).md "wikilink")、直接リンクした[ライブラリ](../Page/ライブラリ.md "wikilink")もしくは[共有ライブラリ](https://ja.wikipedia.org/wiki/共有ライブラリ "wikilink")や[ダイナミックリンクライブラリ](../Page/ダイナミックリンクライブラリ.md "wikilink")の形で利用できる、組み込み型データベースエンジンである。その特徴として、おおむね600kb前後のフットプリントでフルセットのSQLステートメントと型束縛のないデータセットを利用することができる。データベースストレージに対するアクセスも内蔵しており、ファイル及び[インメモリストレージに対応している](https://ja.wikipedia.org/wiki/インメモリデータベース "wikilink")。ファイルを共有することで複数のアプリケーションがデータベースインスタンスを共有することも可能であり、サーバ・クライアントモデルではないアプリケーションローカルで使用するデータベースエンジンとしては合理的な設計となっている。

SQLiteのもう一つの特徴は、バイトオーダーに依存しない、アーキテクチャ非依存のストレージを採用していることである。このため、データベースインスタンスを格納したストレージとなったファイルは再利用性が高い。ストレージバージョンにさえ注意を払えば、アプリケーションからストレージを取り出し、別のOSやアーキテクチャで動作している別のアプリケーションにデータを変換することなく移すことができる。

ストレージまでネイティブコードで直接実行し、間になんらかのプロトコルやプロセス間通信を伴わないことにより、単一のトランザクション内におけるレイテンシをある程度削減することに成功している。一度トランザクションを開始するとストレージはロックされ、トランザクション中のセッションはキャッシュを有効利用して動作するため、高速にデータベースにアクセスすることができる。これは応答性が重要な、かつ多数のトランザクションが並行しないような規模のアプリケーションでは重要な要素となり、SQLiteをサーバとの中間にキャッシュとして採用する事例や、アプリケーション組み込みデータベースエンジンとしての採用を促す理由ともなっている。

標準で搭載しているデータセットの型は整数型 (INTEGER)、文字列型 (TEXT)、無制限スカラ型 (BLOB) の3種類である。

後述の[CUIベースの管理ツールを標準で備える他](../Page/キャラクタユーザインタフェース.md "wikilink")、複数の[GUIベース管理ソフトウエアが存在する](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。またストレージ仕様がアーキテクチャに依存しないため、管理ツールの直接実行が難しいシステム（組み込みソフトウエア開発等）においても、ストレージを取り出して[Windowsマシン等でデータを確認したりSQLステートメントを実行することが可能である](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 管理ツール

  - 「sqlite」または「sqlite3」という[コマンドラインユーティリティーが付属しており](../Page/コマンドラインインタプリタ.md "wikilink")、[CUIでSQLiteのデータを操作できる](../Page/キャラクタユーザインタフェース.md "wikilink")。
  - [「Navicat for SQLite」](https://jp.navicat.com/products/navicat-for-sqlite)はデータの編集やSQLクエリ、データモデリングのツールを備え、データ転送、インポート/エクスポート、データの同期、レポートなどの機能が提供されている。
  - [DB Browser for SQLite](http://sqlitebrowser.org) Windows, Mac OS, Linux, FreeBSD に対応したGUI管理ツール。ライセンスは Mozilla Public License Version 2。
  - [PupSQLite .NET Framework4](https://www.eonet.ne.jp/~pup/software.html) Windows対応のGUI管理ツール。フリーソフト。.NET Framework4 のインストールが必要。

## ODBC

SQLiteの[ODBC](../Page/Open_Database_Connectivity.md "wikilink")[ドライバが](../Page/デバイスドライバ.md "wikilink")[サードパーティー](../Page/サードパーティー.md "wikilink")から提供されている。SQLite 2とSQLite 3のバージョンがあり、SQLite 2向けには、さらに[UTF-8](../Page/UTF-8.md "wikilink")対応版がある。

## 脚注

## 関連項目

  - [Apache Derby](../Page/Apache_Derby.md "wikilink")
  - [H2 Database](../Page/H2_Database.md "wikilink")

## 書籍

  - *The Definitive Guide to SQLite* 2006/06/19, ISBN 1-59059-673-0
  - *SQLite 入門* 2005/09, ISBN 4-7981-0943-6
  - *PHP+SQLite実践サンプルブック* 2005/07, ISBN 4-88337-429-7
  - *改訂版PHPポケットリファレンス* 2005/09, ISBN 4-7741-2502-4
  - *SQLite 入門 第2版* 2009/05, ISBN 978-4-7981-1944-1
  - *SQLiteポケットリファレンス* 2010/10, ISBN 978-4-7741-4394-1
  - *Android UIデザイン＆データベースプログラミング* 2011/06, ISBN 978-4-88337-761-9

## 外部リンク

  - [SQLite Home Page](https://www.sqlite.org/)
  - [SQLite ODBC Driver](http://www.ch-werner.de/sqliteodbc/)
  - [SQLite Developer home page](http://www.sqlitedeveloper.com/)
  - [SQLiteManager home page](http://www.sqlitemanager.org/)
  - [SQLiteSpy](http://www.yunqa.de/delphi/sqlitespy/). [Win32](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink"), [Unicode](../Page/Unicode.md "wikilink").
  - [Database Master](http://www.nucleonsoftware.com)
  - [DaDaBIK Database Interfaces Kreator](http://www.dadabik.org)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:パブリックドメイン](https://ja.wikipedia.org/wiki/Category:パブリックドメイン "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink")

1.
2.
3.
4.
5.  Bill Lubanovic 著『入門Python3』、斉藤康毅 監訳 ・長尾高弘 訳、株式会社オライリー・ジャパン発行、オーム社 発売、2017年2月3日 初版 第6刷、246ページ