> この記事は[Ingres](https://ja.wikipedia.org/wiki/Ingres)から翻訳されています。


**Ingres**（イングレス）は、商用サポートのある、オープンソースの[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink")である。Ingres は 1970年代初めから1980年代初めにかけて、[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")での研究プロジェクトで開発された。オリジナルのコードは、バークレーの他のプロジェクトと同様、[BSDライセンスにより最小限のコストで入手可能である](https://ja.wikipedia.org/wiki/BSD_License "wikilink")。1980年代中ごろから Ingres に基づいた商用データベース製品がいくつも生まれた。例えば、[Sybase](../Page/Sybase.md "wikilink")、[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、[NonStop SQL](https://ja.wikipedia.org/wiki/NonStop_SQL "wikilink") などがある。Postgres（**Post** In**gres**）は 1980年代中ごろから開始されたプロジェクトで、後に [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink") へと発展した。Ingres はコンピュータ関連の研究プロジェクトとしては最も影響の大きいものの1つに数えられる。

## 歴史

### Ingres

1973年、[IBM](../Page/IBM.md "wikilink")で[System Rプロジェクトが始まり](https://ja.wikipedia.org/wiki/System_R "wikilink")、構築中のシステムに関する一連の論文が公表された。バークレーの2人の科学者 [マイケル・ストーンブレーカー](../Page/マイケル・ストーンブレーカー.md "wikilink")とEugene Wongはこれを読んでそのコンセプトに惹かれ、リレーショナルデータベース研究プロジェクトを自ら始めることを決意した。

彼らはバークレーの経済学部から**Ingres**（INteractive Graphics REtrieval System）と名づけた地理情報データベースシステム研究のための資金を得ていた。この資金でリレーショナルデータベース研究を行うことにした。さらなる資金を得るため、ストーンブレーカーは[DARPAに接触した](../Page/国防高等研究計画局.md "wikilink")。当時のDARPAはコンピュータ研究開発の資金提供元として有名だった。しかし、DARPA も海軍研究局（ONR）も既に他所のデータベース研究に資金提供していたため、ストーンブレーカーの提案は門前払いとなった。ストーンブレーカーは他の政府機関にもあたり、同僚たちの協力もあって、[米国科学財団](https://ja.wikipedia.org/wiki/米国科学財団 "wikilink")と3つの軍関係機関（空軍科学研究局、陸軍研究局、海軍電子システム司令部）から多少の援助を得ることとなった。

資金を得ると、Ingresは1970年中ごろ学生を使って開発が進められた。IngresはSystem Rと同様の発展を続け、1974年の初期のプロトタイプを始まりとして、次々と機能を追加したリビジョンがリリースされた。Ingresは草の根的にあちこちで使われ、そこから新しいアイデアを含むフィードバックがあり、開発チームがそれらを取り入れていった。Ingresは概念的にはSystem Rとほぼ同じだったが、[DECのマシン上の](https://ja.wikipedia.org/wiki/デジタル・イクイップメント・コーポレーション "wikilink")[UNIX](../Page/UNIX.md "wikilink")で動作する[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")のシステムを指向していた。

### 商業化

System Rとは異なり、Ingresのソースコードは（テープ形式で）実費で誰でも入手可能だった。1980年までに数千のコピーが主に大学を中心に配布された。バークレー出身の学生や他の大学で Ingresのソースコードを使った経験のある学生によって様々な商用データベース製品が生み出されることとなった。

バークレーの学生Jerry Held（後にはKarel Youseffiも）は[タンデムコンピューターズ](../Page/タンデムコンピューターズ.md "wikilink")に入社し、後に[NonStop SQLとなるシステムを開発した](https://ja.wikipedia.org/wiki/NonStop_SQL "wikilink")。このタンデムのシステムはIngres技術の再実装に他ならない。[並列システム上で効率的に動作するよう改良され](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")、データの分散、処理の分散、そしてかなり難しい[分散トランザクション](https://ja.wikipedia.org/wiki/分散トランザクション "wikilink")を実現していた。システムのコンポーネントは1970年代末に最初にリリースされた。1989年までに[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")を並列に実行できるようになり、この製品はプロセッサ数に比例して性能が向上する数少ないデータベースとして有名になった。NonStop SQLのサーバに2つめのCPUを追加すると、性能はほぼ2倍に向上した。タンデムは後に[コンパック](../Page/コンパック.md "wikilink")に買収され、2000年からこの製品の書き換えが行われた。なお、この製品は現在では[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")のものとなっている。

バークレー在籍時にIngresプロジェクトのチーフプログラマだったRobert Epsteinは、同じくプロジェクトに学生として関わったPaula HawthorneとMike Ubellと共にBritton-Leeという会社を設立した。後にEric Allmanも参加している。後に彼らは[サイベース](https://ja.wikipedia.org/wiki/サイベース "wikilink")を設立。サイベースは1980年代から1990年代にかけて、一時期[Oracleに次ぐシェアを誇る製品を持っていたが](../Page/Oracle_Database.md "wikilink")、どこからともなくInformix が登場して1997年にその地位を奪われた。サイベースの製品は[マイクロソフト](../Page/マイクロソフト.md "wikilink")にも1992年にライセンス提供され、マイクロソフトはそれを[Microsoft SQL Serverとして販売した](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")。この関係は1990年代後半になって破綻し、現在ではSQL Serverはサイベースの製品よりも幅広く売れている。

いくつかの企業がIngresのソースコードを使って製品を開発した。最も成功した企業としてRelational Technology (RTI) があり、これは1980年にストーンブレーカーとWongがもう1人のバークレーの教授[Lawrence A. Roweと共に創設したものである](https://ja.wikipedia.org/wiki/:en:User:Larry.Rowe "wikilink")。RTIは1980年代中ごろにイングレス (Ingres Corporation) へと改称。同社はコードをDECの[VMS](https://ja.wikipedia.org/wiki/VMS "wikilink")向けに移植し、データベースの作成/操作用のフロントエンドツール群（例えば、報告書印刷、フォームエントリ/更新など）や[アプリケーション開発ツール群を開発した](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")。ソースコードは更新されていき、機能が追加され（例えば、複数文トランザクション、[SQL](../Page/SQL.md "wikilink")、[B木](../Page/B木.md "wikilink")アクセス法など）、性能が強化された（例えば、コンパイルされたクエリ、マルチスレッド化サーバなど）。同社は1990年11月、ASK Corporationに買収された。創設者たちはその後数ヶ月以内に同社を去った。1994年、ASK/イングレスは[CAに買収され](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink")、その後もIngres系の製品が販売された（OpenIngres、Ingres II、Advantage Ingresなど）。

[2004年](../Page/2004年.md "wikilink")、CAはIngres r3を[オープンソース](../Page/オープンソース.md "wikilink")ライセンスでリリースした。コードにはDBMSサーバとユーティリティ、テキストベースのフロントエンド、アプリケーション開発ツールが含まれている。つまり、GUIベースの開発環境OpenROAD以外は全て含まれている。2005年11月、Garnett\&Helfrich CapitalはCAと共同でIngres Corporationを新たに設立し、IngresとOpenROAD、それらの関連製品のサポートとサービスを同社が行うようになった。

2006年2月、Ingres Corporationは[GPLライセンスでIngres](../Page/GNU_General_Public_License.md "wikilink") 2006をリリースした。

### Postgres

Postgresプロジェクトは[関係モデル](../Page/関係モデル.md "wikilink")を使った既存のデータベース管理の実装の限界に対処することを目的として開始された。最重要課題は、ユーザーが新たな定義域（ドメイン、データ型）を既存の単純な定義域から定義できない点だった。プロジェクトは他にも追記型メディア（[Write Once Read Manyメディア](../Page/Write_Once_Read_Many.md "wikilink")。光ディスクなど）への対応、大容量記憶装置への対応、推論、オブジェクト指向型データモデルなどを取り入れた。実装上も、データベースとアプリケーションの新たなインタフェースが導入された。

プロジェクトの成果は**Postgres**と呼ばれ、完全な型サポートに必要な最小限の機能だけを導入した。型定義機能だけでなく、関係を完全に記述できる機能も持っている。これは広く使われたが、メンテナンスはユーザーに任されていた。Postgresではデータベースが関係を「理解」すると言われ、「規則」に従って自然な方法で関連する表から情報を得ることができる。詳細は[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")を参照されたい。

1990年代になるとストーンブレーカーはPostgresの商業化のために新たな会社**[Illustra](https://ja.wikipedia.org/wiki/Illustra "wikilink")**を設立した。同社とその技術は後に[Informix](../Page/Informix.md "wikilink")が買収した。

## 関連項目

  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")

## 管理ツール

  - [Database Master](http://www.nucleonsoftware.com)

## 外部リンク

*記事など*:

  - [The Design and Implementation of INGRES](http://www.cs.wisc.edu/~nil/764/root/3_p189-stonebraker.pdf)
  - [Retrospection on a Database System](http://www-it.et.tudelft.nl/~arjen/IN4144/1/retrospection-DB.pdf)
  - [Ingres FAQ](http://www.bizyx.com/ingres/faq.htm)

*コミュニティ*:

  - [North American Ingres Users Association](http://www.naiua.org)
  - [German Ingres User Association](http://www.giua.de)
  - [Ingres UserGroup Nederland](http://www.iugn.nl)
  - [UK Ingres Users Association](http://www.iua.org.uk)
  - [Ingres User Group Brazil](http://www.iug-br.org)

*製品*:

  - [Ingres Corp.](http://www.ingres.com/)
  - [University INGRES,Version 8.9](http://s2k-ftp.cs.berkeley.edu:8000/ingres/)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")