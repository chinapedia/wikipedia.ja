> この記事は[Data Distribution Service](https://ja.wikipedia.org/wiki/Data_Distribution_Service)から翻訳されています。


**Data Distribution Service** for Real-time Systems（**DDS**）は、[CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink")に欠けていたデータ中心の出版-購読型仕様を求める声に応じて作成された[分散システムの](../Page/分散コンピューティング.md "wikilink")[出版-購読型ミドルウェアの仕様である](https://ja.wikipedia.org/wiki/出版-購読型モデル "wikilink")。それまでもいくつかの独自なDDSソリューションはあったが、2004年に主要DDSベンダー2社（[Real-Time Innovations](http://www.rti.com)と[Thales](http://www.thalesgroup.com)）が共同でDDSの標準仕様を策定し、[Object Management Group](https://ja.wikipedia.org/wiki/Object_Management_Group "wikilink")(OMG)がこれを承認したものである。 なお、通信プロトコルとしては[RTPS](http://www.omg.org/spec/DDSI/2.1)プロトコル(2008年末時点ではRev 2.1)を使用することが規定されている。

## バージョン履歴

  - [Data Distribution Service 1.4 Beta](http://www.omg.org/spec/DDS/1.4/Beta2/PDF) - DDS 1.4Beta 審議完了、近日ドキュメントの正式版がリリース。現在1.5に向けてRequest募集中。
  - [DDS 1.2](http://www.omg.org/spec/DDS/1.2l) — DDS 1.2 ([2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink"))
  - **DDS 1.1** （[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[12月4日](../Page/12月4日.md "wikilink")）
  - **DDS 1.0**

DDS仕様では2種類のインターフェイスを規定している:

  - 低レベルのDCPS（Data-Centric Publish-Subscribe）は、適切な受領者への適切な情報の効率的な配信を目的としたものである。
  - オプションの高レベルなDLRL（Data Local Reconstruction Layer）は、DDSをアプリケーション層に簡単に統合するためのインターフェイスである。これは元々CORBAベースアプリケーションの移植性を上げるために提唱された仕様であるが、現実にはCCM(CORBA Compatibility Model)経由でDDS APIを使用する応用例が多いため、提唱ベンダー以外の製品では対応していない。

Version 1.4ではDLRLはDDS-DLRLとして標準規格から分離された。今後"DDS"として呼ばれるのは従来の"DDS-DCPS"の部分のみとなる。

  - [DDSI-RTPS 2.3 RTF](http://www.omg.org/techprocess/meetings/schedule/Data_Distribution_Service_1.4_RTF.html) - RTPS 2.3 現在審議中。リンク先はOMG会員のみアクセス可能
  - [Real-time Publish-Subscribe Wire Protocol DDS Interoperability Wire Protocol](http://www.omg.org/spec/DDSI-RTPS) - RTPS2.2 RTPSプロトコルの現行最新版

<!-- end list -->

  - [Web-Enabled DDS, 1.0 Beta 1](http://www.omg.org/spec/DDS-WEB/1.0/Beta1/PDF) Web Enabled DDS 1.0 Beta DDSとWebとの親和性を高める規格。また、QoSのXML定義についても記述。

<!-- end list -->

  - [DDS-DLRL 1.4 Beta](http://www.omg.org/spec/DDS-DLRL/1.4/Beta2/PDF) DDS-DLRL DDS Version 1.2まではDDS規格のextensionとされていた規格。DDS規格本体から分離された。

<!-- end list -->

  - [DDS-XTYPES 1.2 RTF](http://www.omg.org/techprocess/meetings/schedule/DDS-XTYPES_1.2_RTF.html) - DDS-XTypesの次期版。現在審議中。リンク先はOMG会員のみアクセス可能
  - [Extensible and Dynamic Topic Types for DDS](http://www.omg.org/spec/DDS-XTypes) - DDS-XTypes。Topic形式を変更可能にする拡張仕様

<!-- end list -->

  - [DDS Security 1.0 FTF](http://www.omg.org/techprocess/meetings/schedule/DDS_Security_1.0_FTF.html) - DDS-SECURITY 1.0 現在審議中。リンク先はOMG会員のみアクセス可能
  - [DDS-SECURITY](http://www.omg.org/spec/DDS-SECURITY) - DDS-SECURITY セキュア用拡張仕様。リンク先は6月にリリースされた仕様β版

<!-- end list -->

  - [DDS-PSM-Cxx v1.1 RTF](http://www.omg.org/techprocess/meetings/schedule/DDS-PSM-Cxx_v1.1_RTF.html) - DDS-PSM-Cxx C++ 2003対応API 1.1。 現在審議中。リンク先はOMG会員のみアクセス可能
  - [ISO/IEC C++ 2003 Language DDS PSM 1.0](http://www.omg.org/spec/DDS-PSM-Cxx/1.0/PDF) - DDS-PSM-Cxx C++ 1.0 2003 STL 対応API。

<!-- end list -->

  - [Remote Procedure Calls (RPC) over Data Distribution Service (DDS) RFP](http://doc.omg.org/mars/2012-6-29) - DDS API上に構築されたRPC。市場からの要求に従いベンダーが構築したものを叩き台に現在審議中。リンク先はOMG会員のみアクセス可能

## アーキテクチャ

### DDS構成要素

  - DDS Publisher
    データ配信を行うDDSオブジェクト。publisher は様々なデータを出版（publish）する。
  - DDS DataWriter
    アプリケーションが publisher と通信する際に使用するDDSオブジェクト。特定の型のデータオブジェクトを表す。
  - DDS Subscriber
    出版されたデータを受信し、アプリケーションが利用できるようにするDDSオブジェクト。subscriber は様々なデータを受信してディスパッチする。
  - DDS DataReader
    subscriber に付属するDDSオブジェクトで、受信データにアプリケーションがアクセスできるようにする。

### DDSモデル

DDS は複雑な[コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")に関連した[プログラミングを単純化するネットワーキング](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")[ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")である。ノード間のデータ/イベント/コマンドの送受信を出版-購読型モデルで実装している。情報を生み出すノード（publisher）は「トピック; topics」を生成し、「サンプル; samples」を出版する。DDS はそのトピックに興味があると宣言した全購読者（subscriber）がサンプルを受け取れるように働く。

DDS は転送に関わる雑事を全て引き受ける。メッセージのアドレッシング、[データのマーシャリング](../Page/シリアライズ.md "wikilink")（従って subscriber と publisher は異なるプラットフォームでもよい）、配布、フロー制御、再送などである。各ノードは publisher にも subscriber にもなれるし、同時に両方の役目を果たすこともできる。

DDS の出版-購読型モデルでは分散アプリケーションで複雑なネットワークプログラミングをしなくてもよい。

DDS は基本的な出版-購読型モデル以上の機構をサポートする。特に重要な利点は、DDSを通信に利用するアプリケーション群は完全に切り離されているという点である。アプリケーション間の相互作用について設計時に時間をかける必要はない。特に、あるアプリケーションが別のアプリケーションの情報を必要とすることはなく、場所も存在するか否かさえも知る必要がないのである。DDS は以下のようなメッセージ配信のあらゆる面を自動制御し、ユーザーアプリケーションがそれに関わる必要は全くない。

  - メッセージを受信すべき相手の決定
  - 受信側がどこにあるか
  - メッセージを配信できないときに発生する事象

このため、DDSに対してユーザーアプリケーションが[Quality of Service](https://ja.wikipedia.org/wiki/Quality_of_Service "wikilink")(QoS)パラメータを指定でき、自動検出機構の設定をしたり、メッセージ送受信時の動作を指定したりできる。このような機構は最初に設定されたらユーザー側が後で何かをする必要は無い。完全に匿名でのメッセージ交換を行うことで DDS は分散アプリケーションの設計を大幅に単純化し、モジュール化され良く構造化されたプログラム作成を可能としている。

DDS は publisher の二重化によるホットスワップも制御する。ホットスワップ中も subscriber は常に有効な高優先度データのサンプルを受け取る（有効とは、publisherの指定した有効期限内であるという意味）。障害から回復した一次 publisher への復旧も自動的に行われる。DDS は以下にあるようなベンダーから実装された製品が出ており、[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[APIが利用可能である](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

## DDSプロバイダー実装

  - [RTI Connext DDS](http://www.rti.com/products/dds/index.html) — Real-Time Innovations, Inc. の[COTS](https://ja.wikipedia.org/wiki/商用オフザシェルフ "wikilink") [リアルタイム](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink") DDS API（C言語、C++、Java言語）。[組み込みシステム](../Page/組み込みシステム.md "wikilink")を含む各種プラットフォーム用。派生品として"RTI Connext DDS Secure"(DDS Secure対応), "Connext DDS Micro"(組込み向け縮小版), "Connext DDS Cert" (Connext DDS Micro にDO-178C Level A認証取得用資料を加えたもの)が用意されている。
  - [OpenSplice](http://www.prismtech.com/opensplice) 欧州一の軍需メーカー Thales で開発されていたDDS。その後Prismtechに売却された。DDS市場ではRTI(シェア70%程度)に次ぐ製品(シェア10～15%)。
  - [DDS for TAO](http://www.ociweb.com/products/dds) — Object Computing, Inc (OCI) の[オープンソース](../Page/オープンソース.md "wikilink") DDS 実装。CORBA上に構築されたACE/TAOフレームワークに基づいている。
  - [Open-Source Java-based DDS](http://www-adele.imag.fr/~donsez/dev/dds/readme.html) — ADELE Team の[オープンソース](../Page/オープンソース.md "wikilink") Javaベース DDS 実装（CORBA上に構築）。
  - [MilSOFT DDS](http://dds.milsoft.com.tr) — MilSOFT の [COTS](https://ja.wikipedia.org/wiki/商用オフザシェルフ "wikilink") DDS 実装。

## 採用事例

代表的なものとして、米海軍オープンアーキテクチャ(Naval Open Architecture: 略称OA)に採用され、その後OA毎米国防総省全体の調達規格(COTS)に組み込まれた。この影響で旧西側同盟諸国を始めとする各国で軍用・民生用を問わずに採用されている。(米海軍強襲揚陸艦 LPD-17を皮切りに米海軍個艦防衛システム"SSDS"、艦内ネットワーク"SWAN"、AEGISシステムを構成するレーダー・ソナー・FCS・各種兵装、"SWAN"を更新した"TSCEi"(Zumwalt DDG 1000等)、カナダ航空管制システム、欧州航空管制システム(西側でRTI Connext、東側でOpenSpliceが採用されている)、スゥエーデン SAAV 9LVなどに採用。

OACE、COTSでの実績をもとに、航空機器用ソフトウェア標準規格"FACE"の通信ミドルウェアにDDS採用されている。\*[U.S. Army, General Dynamics Advanced Information Systems and RTI Announce Framework for Development of Avionics Systems That Extends the Value of Technology and Reduces Costs](http://www.rti.com/company/news/face-tss-us-army.html)

相互接続・運用性、実効帯域幅の広さ、PnPなどの特性から、産業向けInternet of things "IIOT" の通信ミドルウェアとして有望視されている。\*[The Industrial Internet of Things](http://www.rti.com/industries/iot.html) \*[PrismTech Announces General Availability of Vortex, the Intelligent Data Sharing Platform for the Industrial Internet of Things](http://www.prismtech.com/news/prismtech-announces-general-availability-vortex-intelligent-data-sharing-platform)

## 関連項目

  - [ミドルウェア](https://ja.wikipedia.org/wiki/ミドルウェア "wikilink")

## 外部リンク

  - [The OMG DDS portal](http://portals.omg.org/dds)
  - [Data Distribution Service for Real-time Systems, v1.1](http://www.omg.org/technology/documents/formal/data_distribution.htm)
  - [DDS resources](http://www.rti.com/resources.html) — DDSに関する一般情報、デモアプリケーション、技術文書など
  - [Data-Centric Architecture for Mission Critical Systems](http://www.milcotsdigest.com/Articles/2006/November/prism/default.htm)
  - [CORBA and DDS, competing or complementary technologies?](http://www.omg.org/news/meetings/workshops/RT_2005/03-1_Karoui.pdf)

[Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink")