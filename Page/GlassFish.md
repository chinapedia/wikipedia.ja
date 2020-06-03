> この記事は[GlassFish](https://ja.wikipedia.org/wiki/GlassFish)から翻訳されています。


**GlassFish**は、[サンを中心とした](../Page/サン・マイクロシステムズ.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")・コミュニティと、同コミュニティで開発された[Java EE準拠の](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")の名称である。その後、サンを買収した[オラクルによってコミュニティが継続された](../Page/オラクル_\(企業\).md "wikilink")。2017年、[Java EEの策定がEclipse](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") Foundationに移管されることになり、それに伴いGlassFishも同組織に寄贈された。

本項では以降、特別な断りのない限りアプリケーションサーバのことを指すものとし、コミュニティについてはGlassFishコミュニティと呼称する。

GlassFishは設計・開発・テストのすべてをオープンソース・コミュニティ上で行っている。かつては、オラクル（サン）による商用サポート（商用版にはロードバランサなどオープンソースではないコンポーネントが追加されている）も同時に行われていたが、GlassFish 4.0を機に廃止され、開発者向けのJava EEの参照実装としての位置になっている\[1\]。GlassFishは[Eclipse Public License](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink") (EPL)と、クラスパス例外を含む[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) の二重ライセンスである。

## 歴史

### GlassFish v1

GlassFishは、Sun Java System Application Server 8.xの後継製品であり、サン最初のオープンソース・アプリケーションサーバとして開発が開始された。GlassFishプロジェクトは[2005年](../Page/2005年.md "wikilink")6月6日に発足し、[2006年](../Page/2006年.md "wikilink")5月4日に最初のバージョン (GlassFish v1) をリリースした。GlassFish v1の概要は下記の通りである。

  - Java EE 5準拠（参照実装）である。
  - オープンソースである（ライセンスは[CDDLと](https://ja.wikipedia.org/wiki/Common_Development_and_Distribution_License "wikilink")[GPL](../Page/GNU_General_Public_License.md "wikilink")）。
  - 他のグループから多数の優れたコンポーネントを採用している。例えばMetro () や[JAXBなど](../Page/Java_Architecture_for_XML_Binding.md "wikilink")。この中にはオラクルから提供を受けたも含まれる。
  - 年間330万ダウンロード以上を目標とする。
  - Sun Java System Application Server 9.0として、サンによる商用サポートを提供する。

GlassFish v1は1回のアップデートリリース（無償）と5回のパッチリリース（サンの有償サポートによる）がリリースされた\[2\]。

### GlassFish v2

GlassFish v1はJava EE 5の参照実装としての色合いが強く、単一インスタンスに特化していた。2つめのメジャーリリース (GlassFish v2) ではその点を大幅に改善したものとなった。GlassFish v2の新機能は以下の通りである\[3\]。

  - クラスタリングおよびHADBの提供。JXTAベースのインメモリ・レプリケーション・メカニズムが含まれる。
  - 商用レベルの管理・監視機能の提供。これには管理コンソール（Webベース）、ドキュメント、CLIの監視機能が含まれる。
  - オールインワン。SJS AS 8.xには複数のエディションがあったが、GlassFish v2ではそれらが統合された。
  - Metro Webサービスフレームワークと[マイクロソフト](../Page/マイクロソフト.md "wikilink")製品 (.NET Framework 3.0) との相互接続性の保証。
  - パフォーマンスの向上。オープンソース・アプリケーションサーバで唯一SPECjAppServer 2004ベンチマークを実施し、[BEA](../Page/BEAシステムズ.md "wikilink") WebLogicと[IBM](../Page/IBM.md "wikilink") [WebSphereを凌ぐ結果を出した](../Page/WebSphere_Application_Server.md "wikilink")。

GlassFish v2の最初のリリースは[2007年](../Page/2007年.md "wikilink")9月17日に行われた。このバージョンのサンにおける名称はSun Java System Application Server 9.1である。 GlassFish v2は[2011年](../Page/2011年.md "wikilink")1月時点で4回のアップデートリリース（無償）と21回のパッチリリース（サン/オラクルの有償サポートによる）がリリースされており、今後もパッチリリースが予定されている。 \[4\] なお、GlassFish v2.1において、サンにおける名称がSun GlassFish Enterprise Server 2.1に変更され、以降バージョン番号がコミュニティ版と商用版で統一された。

#### SailFin

サンと[エリクソン](../Page/エリクソン.md "wikilink")による「Communication Application Server」を構築するプロジェクトで、2007年5月8日にGlassFishのサブプロジェクト[SailFin](http://sailfin.dev.java.net/)としてJava Oneで発表された。SailFinは、エリクソンから提供された[SIP](../Page/Session_Initiation_Protocol.md "wikilink") Servlet \[5\]をGlassFish v2.1へ統合したものである。SailFin 1.0はGlassFish v2.1と同時の[2009年](../Page/2009年.md "wikilink")1月26日にリリースされた。サンによる商用版はSun Java System Communication Application Serverである。

### GlassFish v3

その次のメジャーリリースとなるGlassFish v3は、Java EE 6の参照実装であると同時に、アーキテクチャを抜本的に見直し、[OSGi](../Page/OSGi.md "wikilink")モジュールサブシステムに対応した。機能を使われるときに初期化することで非常に高速な起動を実現し、また再起動の待ち時間を大幅に減少させることに成功している。この新しいアーキテクチャはGlassFish v3 Preludeとして先行してリリースされている。また、GlassFish v3ではJava EE以外のスクリプト言語にも本格的に対応しており、GlassFish上で動作するスクリプト言語実装も増加している。

#### GlassFish v3 Prelude

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")11月6日にリリースされた最初のv3系がGlassFish v3 Preludeである。この製品はJava EE 5のサブセットを提供し、一部Java EE 6の機能を取り込んだものであった。Java EEには準拠していないが、サンによる商用サポートが提供されていた。

#### GlassFish v3

[2009年](../Page/2009年.md "wikilink")12月10日、GlassFish v3がリリースされた。これはJava EE 6に準拠した最初のアプリケーションサーバである。当初予定していたクラスタ機能がGlassFish v3.1へ先送りとなったが、サンによる商用サポートは引き続き提供された。GlassFish v3の主な機能は以下の通りである。

  - Java EE 6の参照実装の提供。
  - OSGiモジュール化サブシステムに対応（を採用）
  - Metro Webサービスフレームワークと[マイクロソフト](../Page/マイクロソフト.md "wikilink")製品 (.NET Framework 3.5) との相互接続性の保証。
  - 非同期I/O ([Comet](../Page/Comet.md "wikilink")) に対応
  - 従来からの管理コンソール、CLIの管理ツールに加え、RESTful管理チャネルが追加された。これにより、JAX-RSアプリケーションからサーバの管理・監視ができるようになった。
  - インストーラ版に加え、ZIPアーカイブ版による配布が開始された。ZIPアーカイブ版はあらかじめデフォルトでサーバが構成された状態で配布されるため、アーカイブを展開してすぐに利用可能である。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")1月27日にオラクルによるサンの買収が完了すると、GlassFishのサポートはオラクルに引き継がれた。2010年6月18日、GlassFishバージョン3.0.1がリリースされた。このリリースでは100のバグの修正と多言語化が実施されると同時に、ブランドがサンからオラクルに移行したのに伴い、オープンソース版がGlassFish Server Open Source Edition、オラクル製品版がOracle GlassFish Serverへと名称変更となった。またこのリリースからが正式サポートされるようになった。2010年10月8日には製品版のパッチリリースが行われた。

#### GlassFish v3.1

GlassFish v3リリースで先送りされたクラスタなどの高可用性機能を実装したものがGlassFish v3.1である。このバージョンにより前メジャーバージョンで提供されていた機能が一通り揃うことになった。GlassFish v3.1は[2011年](../Page/2011年.md "wikilink")2月28日にリリースされた。 GlassFish v3.1の主な機能は以下の通りである。

  - クラスタ対応。方式としてGlassFish v2に存在していたNode Agentを廃止し、新たに[SSHプロビジョニングを採用する](../Page/Secure_Shell.md "wikilink")。SSHプロビジョニング方式では、クラスタノード側でSSHのサーバプロセス（デーモン）を起動しておくだけで、ドメイン管理サーバがシステムの初期化とドメイン管理サーバへの登録を行う。ノード側ではGlassFishをインストールする必要もなく、ドメイン管理サーバが自らのインスタンスをアーカイブしてノードに転送しリモートインストールを実行する。v3.1.2以降、Windowsプラットフォームに限りSSHの代替として[DCOMの](../Page/Distributed_Component_Object_Model.md "wikilink")[RPCを使用することが可能となっている](../Page/遠隔手続き呼出し.md "wikilink")。
  - アプリケーションのバージョニング対応。サーバ上に同じアプリケーションの複数のバージョン（例えば開発版、リリース候補版、製品版など）を同時に配備しておき、その中から1つのバージョンを選んで稼働させることができる。配備できるアプリケーション数とバージョン数は事実上無制限である。
  - ドメイン管理サーバの高可用性
  - HTML5 [WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")対応
  - 管理・監視機能の強化。[DTrace](../Page/DTrace.md "wikilink")によるモニタリングが正式サポートされる。
  - WebLogicとの互換性の提供（WebLogicのデプロイメント記述子をサポートする）。

2011年7月28日にはバージョン3.1.1がリリースされた。主な変更点はJDK7対応、[AIX](../Page/AIX.md "wikilink")サポートの追加およびバグフィックスである。2012年2月にリリースされたバージョン3.1.2ではバグフィックスに加え、開発中止となったバージョン3.2の一部機能（[DCOMプロビジョニングによるクラスタ構成など](../Page/Distributed_Component_Object_Model.md "wikilink")）が追加されている。 バージョン3.1.x系列の最新版は2012年7月15日にリリースされた3.1.2.2である。

#### GlassFish 3.2

GlassFish 3.1のアップデート版としてGlassFish 4と並行して開発が進められていた。GlassFish 4までの橋渡しとしていくつかの新機能を実装するプラットフォームとなる予定だったが、GlassFish 4に注力するため開発は中止された。実装予定の新機能の多くはGlassFish 4で実現されたが、既に完成していた機能についてはバージョン3.1.2にバックポートされる形で取り込まれた。

### GlassFish 4.0

GlassFish 4.0は[2013年](../Page/2013年.md "wikilink")6月11日にリリースされたメジャーバージョンであり、Java EE 7の参照実装でもある。GlassFish 3.xのアーキテクチャをベースとしている。開発段階では[PaaS型のクラウドへの対応を予定しており](../Page/Platform_as_a_Service.md "wikilink")\[6\]、従来の管理コンソールに加え、PaaS環境の管理・監視を行うためのPaaSコンソールを有していた。この機能はPaaS対応がJava EE 8へ延期となったことからリリースからは除外されている。このバージョンはJava EE 7の参照実装としての位置づけであり、Oracleによるサポート対象からは除外されている。

#### GlassFish 4.1

GlassFish 4.x系列のアップデートは、当初コミュニティ向けのGlassFish 4.0.1と商用サポートを含むGlassFish 4.1の二本立てで計画されていた。しかし、OracleによるGlassFish 4.x系列の商用サポート打ち切りが発表され、GlassFishの開発は継続されるものの再び開発者向けのJava EEの参照実装であると位置づけられることとなった。Oracleでは商用サポートが必要な場合は同社の別のアプリケーションサーバーであるに移行するよう呼びかけている。\[7\] さらに当初のGlassFish 4.1はキャンセルされ、GlassFish 4.0.1のみ開発が継続された。 それに追い打ちをかけるようにGlassFish 4.0.1の開発は停滞し、当初予定していた[2013年](../Page/2013年.md "wikilink")終わりにはリリースできなかった。その間にコンポーネント単位でのアップデートは急速に進み、最終的にはGlassFish 4.1とバージョンを変えて[2014年](../Page/2014年.md "wikilink")9月9日にリリースされた。

#### GlassFish 4.1.1

[2015年](../Page/2015年.md "wikilink")9月24日にリリースされたGlassFish 4.x系列の2番目のアップデートであり、当初はGlassFish 4.2と呼称されていたが、開発の途中でGlassFish 4.1.1に変更された。主な変更点はコンポーネントのさらなるアップデートである。なお、GlassFishの開発Trunkは、このバージョンのリリースをもってGlassFish 5系列に移行している。

#### GlassFish 4.1.2

2017年3月31日にリリースされた。

### GlassFish 5.0

[2017年](../Page/2017年.md "wikilink")9月21日にJava EE 8の参照実装としてリリースされた。

#### GlassFish 5.1

[2019年](../Page/2019年.md "wikilink")1月29日にリリースされた。Eclipse Foundation寄贈後の最初のリリース\[8\]\[9\]。

## 技術

### モジュールサブシステム (GlassFish v3)

GlassFish v3はGlassFish [OSGi](../Page/OSGi.md "wikilink")ランタイムとGlassFish Kernel (HK2: Hundred-Kilobyte Kernel) の2つのモジュールサブシステムによりサーバ全体をモジュール化している。GlassFish OSGiランタイムはOSGi Release 4に準拠したランタイムを利用可能で、組み込みのランタイムとしてが採用されている（ただし、やなども利用可能である）。

GlassFish KernelはHK2と略される、JSR-277ベースのモジュールサブシステムである。HK2はOSGiランタイムだけでは補えないモジュール管理機能を担当している。OSGi対応前はすべての機能をHK2のモジュールとして作成していたため、今でもGlassFishのモジュール（OSGiバンドル）の実装にはHK2のAPIが使用される。

GlassFish上では任意のOSGiバンドルを利用可能なため、例えば[Spring](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink") DMとJava EEを連携させるような運用も可能である。

### Nucleus

GlassFish v3のカーネルと主要部分はNucleusと呼ばれている。構成は以下の通り。

  - Config Framework - 設定情報ファイル (domain.xml) とそれを管理するフレームワーク
  - CLI Framework - コマンドライン・インタフェース
  - Grizzly - リクエスト・ディスパッチャ（後述）
  - Monitoring Framework - 監視フレームワーク
  - Security Service - SSL等のサポート
  - REST Backend - REST管理チャネル

### IPS

IPS (: pkg(5)) は、OpenSolarisプロジェクトで開発されたパッケージのインストール、アップグレード、削除などのソフトウェアのライフサイクル管理のために提供されるフレームワークである。\[10\] IPSは[OpenMQ](https://ja.wikipedia.org/wiki/OpenMQ "wikilink")をGlassFish 2.1.1に統合する際にGlassFish v2に追加され、GlassFish v3以降は標準の更新ツールとして採用されている。GlassFish v3のオープンソース版と商用版のライセンス切り替えに伴う実装の変更は、IPSのコマンドにより比較的容易に実施できる。

### Grizzly

GlassFishで採用されているハイパフォーマンスなリクエストディスパッチャがGrizzlyである。GrizzlyはGlassFishのHTTPサーバ実装プロジェクトとして2004年から開発が始められ、現在ではマルチプロトコル対応のネットワークサーバエンジンとなっている。Grizzlyは当初、サンのアプリケーションサーバで使用していた[Apache TomcatのCoyoteエンジンではGlassFishの要求性能を満たせなかったことから](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")、Java NIOを用いて試験的に実装されたものであった。その後、TCP/UDP/SSLなどのマルチプロトコルに対応できる汎用性が注目され、GlassFish v2.1向け実装 (Gryzzly 1.0.x) からアーキテクチャを大幅に変更し、SailFinのSIPにも容易に対応している。

GrizzlyはJava NIOによる非ブロッキングI/Oを活用することで、1リクエスト当たりのスレッド生成数を抑えることに成功している。GlassFish v3ではOSGiバンドルとして再実装されたGrizzly 1.9.18以降、v4ではさらに性能が向上したGrizzly 2.3.3以降が採用されている。

GlassFishでは、サーブレットコンテナとしてもGrizzlyが用いられているが、一部の処理にはTomcat 5.5に由来するコードが使用されている。

### CLI Framework

### Monitoring Framework

### REST Backend

### 高可用性

## Java EE参照実装（サブプロジェクト）

Java EE参照実装は、サブプロジェクトであるMetro ()、Jersey ()、Mojarra ([JSF](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink"))、OpenMQ ([JMS](../Page/Java_Message_Service.md "wikilink"))、Tyrus ([WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink") API)、JSON Processing でそれぞれ開発されている。また、Weld ([CDI](https://ja.wikipedia.org/wiki/CDI "wikilink"))、Hibernate Validator (Bean Validation)、EclipseLink ([JPA](../Page/Java_Persistence_API.md "wikilink"))、JBatchなど外部の有力な参照実装を採用している。

### Metro

JAX-WSの参照実装であり、[Apache Axis2より](../Page/Apache_Axis2.md "wikilink")90%高速である。\[11\] [SOAP通信において](../Page/SOAP_\(プロトコル\).md "wikilink")、Microsoft .NET Framework 3.0および3.5との相互接続性が保証されている。

### Jersey

JAX-RSの参照実装である。 GlassFish v3ではREST Backendの基盤でありNucleusに含まれている。そのため他のJava EEサーバと異なり、GlassFish v3ではJAX-RS実装であるJerseyをサーバ本体から切り離すことができない。

### Mojarra

### OpenMQ

### Tyrus

### JSON Processing

## 多国語版

GlassFish v2より英語の他、日本語、簡体字中国語、繁体字中国語、ハングル、スペイン語、フランス語、ドイツ語を含む多国語版リリースが行われている。GlassFish 4.1以降、再び他言語版の配布がなくなり更新ツールによる対応に戻された。

## サードパーティーによる商用サポート

GlassFish自体はOracleによる商用サポートを外されたが、いくつかのベンダーやコンサルティングファームによるサードパーティー・サポートが継続されている。中でも初期からサポートを行っているC2B2社の[Payara](https://ja.wikipedia.org/wiki/Payara "wikilink")は、GlassFishおよび同社によるGlassFishの派生版であるPayaraの双方のサポートを提供している。

## 脚注

### 注釈

### 出典

## 関連項目

  - [Java Platform, Enterprise Edition](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") (Java EE)

  - [OpenMQ](https://ja.wikipedia.org/wiki/OpenMQ "wikilink")

  - [Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")

  -
## 外部リンク

  -

[Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink") [Category:Eclipse_Foundation](https://ja.wikipedia.org/wiki/Category:Eclipse_Foundation "wikilink")

1.
2.  <http://blogs.sun.com/GlassFishForBusiness/entry/sjs_as_9_0_gf1>
3.  <http://blogs.sun.com/pelegri/entry/overview_of_glassfish_v2>
4.  <http://blogs.sun.com/GlassFishForBusiness/entry/overview_of_sjs_as_9>
5.  <http://jcp.org/en/jsr/detail?id=289、当初はhttp://jcp.org/en/jsr/detail?id=116>
6.  <http://glassfish.java.net/javaone2011/index.html>
7.
8.
9.
10. <http://dlc.sun.com/osol/g11n/content/2009.06/IMGPACKAGESYS/ja/>
11. <http://blogs.sun.com/theaquarium_ja/entry/metro_90_better_performing_than>