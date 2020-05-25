> この記事は[Cosminexus](https://ja.wikipedia.org/wiki/Cosminexus)から翻訳されています。


**Cosminexus**（コズミネクサス）は、[日立製作所](../Page/日立製作所.md "wikilink")が提供する[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")を構築・[運用するための](../Page/システム運用.md "wikilink")[ミドルウェア](../Page/ミドルウェア.md "wikilink")製品。[JavaEE 7に対応したシステム構築が可能となっている](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。最新のバージョンは10.0である。

## 概要

J2EEに対応したアプリケーション実行環境を構築するためのApplicationServer、Windows上でアプリケーションの開発環境を構築するためのDeveloper、Cosminexusおよびその他ミドルウェアで開発したアプリケーションを統合してサービス提供を行うプラットフォーム環境を構築するためのService Platformなどの製品が提供されており、それぞれ[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[AIX](../Page/AIX.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")各種環境で動作させることが可能となる。 [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink")、[Tomcatといったオープンソースソフトウェアを元に独自の修正](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")・制限や機能拡張を行い提供している また、これらの各種環境すべてに対して日立独自の拡張を施した[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")を提供している。

## 歴史

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にCosminexusの前身として「日立アプリケーションサーバ」がリリース。[EAI](https://ja.wikipedia.org/wiki/EAI "wikilink")をサポートし、アプリケーション開発負荷の軽減などを目指した製品提供がなされた。[2000年](../Page/2000年.md "wikilink")には製品の名称をCosminexusに変更した[JRun](https://ja.wikipedia.org/wiki/JRun "wikilink")をベースにVer3をリリース。これは[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")で初めてJ2EEブランドを取得したアプリケーションサーバとして知られている。Ver5で独自の[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")をサポート、Version9にてインメモリデータグリッドをサポートした。また[2014年](../Page/2014年.md "wikilink")にVersion10をリリース。これは[2014年](../Page/2014年.md "wikilink")時点で[JavaEE 7に準拠した世界で初めての商用製品である](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。([Java EE 7 Full Platform Compatible Implementations](http://www.oracle.com/technetwork/java/javaee/overview/compatibility-jsp-136984.html))

## 特徴

  - 独自のメモリ管理でFullGCを抑止（8.0以降）\[1\]
  - 独自に性能への影響を低減した上で、障害解析/性能解析を容易にするPRFトレース機能
  - OLTP技術を利用した優先制御、流量制御、負荷分散
  - 仮想化ソフトとの連携（8.5以降）

## 他製品との連携

[Oracle](../Page/Oracle_Database.md "wikilink")、[HiRDB](../Page/HiRDB.md "wikilink")、[SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、[XDMなどの各種データベースソフトウェアとの連携が可能](https://ja.wikipedia.org/wiki/XDM_\(データベース\) "wikilink")。また[クラスタリング](../Page/クラスタリング.md "wikilink")ソフトウェアと連携して大規模で信頼度の高いアプリケーション環境を提供することもできる。

## 脚注

## 関連項目

  - [ミドルウェア](../Page/ミドルウェア.md "wikilink")
  - 日立オープンミドルウェアシリーズ
      - [JP1](../Page/JP1.md "wikilink")：統合システム運用管理
      - [OpenTP1](../Page/OpenTP1.md "wikilink")：オンライントランザクション処理ソフトウェア
      - [HiRDB](../Page/HiRDB.md "wikilink")：スケーラブルデータベース
      - [COBOL2002](https://ja.wikipedia.org/wiki/COBOL2002 "wikilink")：ビジネスアプリケーション環境開発
      - [Groupmax](https://ja.wikipedia.org/wiki/Groupmax "wikilink")：[グループウェア](../Page/グループウェア.md "wikilink")
      - [EUR](https://ja.wikipedia.org/wiki/EndUserReporting "wikilink")：[帳票](https://ja.wikipedia.org/wiki/帳票 "wikilink")システム構築支援ソフトウェア
      - [DocumentBroker](https://ja.wikipedia.org/wiki/DocumentBroker "wikilink")：文書管理ソフトウェア

## 外部リンク

  - [日立製作所-Cosminexus](http://www.hitachi.co.jp/Prod/comp/soft1/cosminexus/)

[Category:日立製作所](https://ja.wikipedia.org/wiki/Category:日立製作所 "wikilink")

1.  [FullGCレス機能紹介](http://www.itmedia.co.jp/enterprise/articles/0811/04/news005.html)