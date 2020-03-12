> この記事は[JDBC](https://ja.wikipedia.org/wiki/JDBC)から翻訳されています。


**Java Database Connectivity**\[1\] (**JDBC**)は、 と[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")の接続のための[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[ODBCをベースに](../Page/Open_Database_Connectivity.md "wikilink")[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")および  が共同で開発していると言われている。そのためドライバのデフォルトの自動コミットの有効化など似ている点も多々ある。

において[SQL](../Page/SQL.md "wikilink")を使用して、[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) などと接続する機能を標準化（抽象化）している。

元は[JDK](../Page/Java_Development_Kit.md "wikilink") 1.0の拡張APIという位置付けであったが、JDK 1.1で正式にJavaの基本SDKに同梱されるようになった。標準的な機能 (API) は  に含まれている。JDBCの規格は  とは独立して行われており、APIのアップデートは随時行われている。

## ドライバ

JDBCを利用する為には、100%  製の  が同梱されている  以降のSDK\[2\]を除き、各DBMS用のJDBCドライバを用意する必要がある。現在開発が行われているほとんどのデータベースではJDBCドライバが用意されている。 これらのドライバを管理するのが JDBC ドライバ・マネージャーである。JDBC ドライバ・マネージャーを用いると、複数のJDBCドライバを同時に利用することができる。JDBCを使うユーザーは、JDBCドライバをロードし（多くはメソッドを利用して呼び出される。また、JDBC4.0以降であればドライバの自動解決が機能するため、メソッドを使うことができる。これらのメソッドを利用した場合[コンパイラ](../Page/コンパイラ.md "wikilink")によるそのドライバの依存チェックが行われない為、コンパイル時にドライバをあらかじめ参照できる様に設定しなくて良いなどの利点がある）、JDBC ドライバ・マネージャーを使ってデータベースドライバを取得し、データベースと接続を行って、データベースアプリケーションを記述する事になる。 また、 の[オブジェクト指向言語の特性を生かして](../Page/オブジェクト指向プログラミング.md "wikilink")、各ドライバはJDBCの基本APIに無い機能を同梱する事もできる。この場合、JDBC APIのスーパーセットのクラスを呼び出すことでこれらの機能を利用可能にすることができる。

たとえば、初期の[オラクル社の](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")  () 用JDBCドライバは、当時の JDBC API が [BLOB](https://ja.wikipedia.org/wiki/バイナリ・ラージ・オブジェクト "wikilink")、[CLOBに対応していなかったため](https://ja.wikipedia.org/wiki/キャラクタ・ラージ・オブジェクト "wikilink")、独自に機能拡張をしてBLOBとCLOBに対応していた。

## JDBC ドライバのタイプ

JDBCドライバは4つのタイプに分類されている。

  - タイプ1
    JDBC-ODBC ブリッジ JDBCからのクエリー要求を、[ODBCを経由して受け渡し](../Page/Open_Database_Connectivity.md "wikilink")、データベースとアクセスするもの。ODBCドライバが必須であり、[ハードウェア](../Page/ハードウェア.md "wikilink")と[OSに依存する](../Page/オペレーティングシステム.md "wikilink")。 までに標準で添付されているドライバでもある。Java7では非推奨となり、Java8では標準から削除された。\[3\]
  - タイプ2
    ネイティブ API ドライバ JDBCからのクエリー要求を、オペーレーティングシステム上の[DLLや専用ライブラリに受け渡し](../Page/ダイナミックリンクライブラリ.md "wikilink")、そこからデータベースにアクセスするもの。Type1に比べて階層が薄く済むため高速化が期待できる点と[TCP/IPに依存しない利点があるが](../Page/インターネット・プロトコル・スイート.md "wikilink")、やはりハードウェアとオペレーティングシステムに依存する。オラクルでいうとOCIドライバがこれに該当する。
  - タイプ3
    [通信プロトコル](../Page/通信プロトコル.md "wikilink")ドライバ JDBCからのクエリー要求を  で記述されたのドライバ内で独自のプロトコルに変換し、それをアプリケーションサーバを通じてデータベースにアクセスするもの。機種依存・データベース依存をせずに軽量なドライバが作成可能だが、中間サーバを挟むためにパフォーマンスに問題が起きる。
  - タイプ4
    ネイティブプロトコルドライバJDBCからのクエリー要求をすべて  上で処理してしまうもの。 上にデータベースにアクセスするためのすべての機能を乗せる為、ドライバのサイズが大きくなる、パフォーマンスが若干低下する。基本的にTCP/IPでしか利用できないなどの欠点があるがハードウェアとオペレーティングシステムに依存しないため移植性に優れている。オラクルでいうと  ドライバがこれ該当する。

タイプ1、タイプ2はDBMSのDLLファイルやライブラリファイルを呼び出す形となるため、JVMのメモリー管理外となる。タイプ3、タイプ4についてはJVM上で  のクラスとして実装されているためJVM上の[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")の対象となり管理が行いやすく、流れとしてはTYPE4が主流となっている。

##  とデータベース

後に大規模システム開発において、 による[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")開発が一般的になるきっかけとなったのは、関係データベースアクセスを  から行う JDBC が発表されてからである。

さらに  で大規模エンタープライズシステムを開発するための仕様「」には、関係データベースの[表（テーブル）の行データを](https://ja.wikipedia.org/wiki/表_\(データベース\) "wikilink")、 の[オブジェクトに](../Page/オブジェクト_\(プログラミング\).md "wikilink")1対1に対応させ、オブジェクト内容の[永続化](https://ja.wikipedia.org/wiki/永続化 "wikilink")＝行データの保存というデータのリンクと、オブジェクトの[メソッド呼び出し](../Page/メソッド_\(計算機科学\).md "wikilink")＝データベースへのトランザクション処理を同期させる特殊な  を動作・管理する機構である「[エンタープライズ {{lang](../Page/Enterprise_JavaBeans.md "wikilink")｣ の「エンティティ・ビーン」が導入された。

EJB 2.1までは、オブジェクト-関係の間にある[インピーダンスミスマッチ](https://ja.wikipedia.org/wiki/インピーダンスミスマッチ "wikilink")により関係データベースの機能を十分に生かせないことや性能面の問題があったが、EJB 3.0以後の仕様により改善されてきている。

EJB 3.2で「エンティティ・ビーン」が廃止され、[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") および [Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") 共通向けの、独立した永続化フレームワーク「[Java Persistence API](../Page/Java_Persistence_API.md "wikilink")」（JPA）に進化した。

## JDBC ドライバの供給元

  - オラクルは、[JDBC ドライバと供給元のリスト](http://www.oracle.com/technetwork/java/index-136695.html) を提供している。
  - [Simba Technologies](https://ja.wikipedia.org/wiki/Simba_Technologies "wikilink") は、外部データソースのカスタム JDBC ドライバを開発できる SDK を出荷している。
  - CData Software は、[様々なアプリケーション、データベース、Web API のタイプ4の JDBC ドライバ](https://www.cdata.com/jp/jdbc/)を出荷している。

## 脚注

<references />

## 関連項目

  - [Java Transaction API](../Page/Java_Transaction_API.md "wikilink")

## 外部リンク

  - [JDBC](http://java.sun.com/javase/technologies/database/)

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.  [Java JDBC API](https://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/index.html)
2.  JavaDB(Apache Derby)は、エンドユーザ向けのJREには同梱されないため、アプリケーションとともに再配布する必要がある。
3.  <http://docs.oracle.com/javase/7/docs/technotes/guides/jdbc/bridge.html>