> この記事は[BACnet](https://ja.wikipedia.org/wiki/BACnet)から翻訳されています。


**BACnet** は、[インテリジェントビル](../Page/インテリジェントビル.md "wikilink")用ネットワークのための[通信プロトコル](../Page/通信プロトコル.md "wikilink")規格である。[ASHRAE](../Page/アメリカ暖房冷凍空調学会.md "wikilink")、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")、[ISOでの標準規格とされている](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")。*Building Automation and Control Networking protocol* の略。[空調](../Page/空気調和設備.md "wikilink")、[照明](../Page/照明.md "wikilink")、[アクセス制御](../Page/アクセス制御.md "wikilink")、[火気検出などの総合的制御に使われる](https://ja.wikipedia.org/wiki/火災報知器 "wikilink")。BACnet プロトコルは、各種機器がメーカー固有の仕様であっても、共通なインタフェースを介することですべて接続し、監視できる。

## 歴史

BACnet プロトコルは1987年6月、[テネシー州](../Page/テネシー州.md "wikilink")[ナッシュビル](https://ja.wikipedia.org/wiki/ナッシュビル "wikilink")で行われた Standard Project Committee (SPC) の会合が発端となって開発された。同委員会の初代委員長であった H. Michael Newman がその会合での議長を務めた。その会合で良いプロトコルに求められる次のような条件が生み出され、それに基づいて BACnet が開発された。

  - 相互運用性
  - 効率性
  - オーバヘッドが低いこと
  - 公約数ではなく公倍数であること
  - 他のアプリケーションやネットワークとの互換性
  - [OSI参照モデル](../Page/OSI参照モデル.md "wikilink")のような階層化されたネットワーク
  - 柔軟性
  - 拡張性
  - 費用効果性
  - 転送の信頼性
  - リアルタイム処理に適用可能であること
  - なるべく単純性を保つこと
  - 優先度制御が可能であること
  - 媒体アクセスの平等性
  - 実際の状況での安定性

同委員会は、標準策定のための作業を複数のワーキンググループで行うことで合意した。ワーキンググループは特定の分野に注力し、委員会に情報と勧告案を提出する。当初結成されたワーキンググループは、データ型と属性に関するワーキンググループ、基本データ形式に関するワーキンググループ、アプリケーションサービスに関するワーキンググループであった。

BACnet は、1995年に ASHRAE/ANSI Standard 135、および2003年に ISO 16484-5 として採用された。BACnet 準拠であることの検証手法は2003年、BSR/ASHRAE Standard 135.1 として公表された。BACnet についてはその後も ASHRAE Standing Standard Project Committee 135 が保守を行っている。

BACnet は空調設備業界では即座に影響があり、1996年には[シーメンス](../Page/シーメンス.md "wikilink")（[Siemens Building Technologies](http://www.buildingtechnologies.siemens.com/)）が採用した。それ以前にもいくつかの企業が BACnet 対応機器を開発していたが、同じ1996年、Alerton が空調制御に関する総合的な BACnet 製品群を発表。Automated Logic Corporation と Delta Controls がこれに即座に追随した。他にも現在では、Johnson Controls、Teletrol Systems、TAC、KMC、Reliable Controls などが BACnet 製品を発売している。

[コーネル大学](../Page/コーネル大学.md "wikilink")の H. Michael Newman は2000年6月まで BACnet 委員会の委員長を務め、後任には[NISTの](../Page/アメリカ国立標準技術研究所.md "wikilink") Steven Bushby が就任した。Bushby が委員長を務める間の4年間に BACnet 標準は2回改版され（2001年と2004年）、新たな機能が追加されていった。2001年版では、特に火災などの安全関係のシステムへの拡張が行われた。2004年6月、新たに Alerton の William Swan が委員長に就任。彼の在任中にワーキンググループは11に増やされ、照明、アクセス制御、電力設備、無線通信などへの対応が検討されるようになった。

2006年1月、BACnet Manufacturers Association と BACnet Interest Group of North America が合併し、BACnet International が結成された。BACnet International には関連する様々な組織が加盟しており、BACnet の普及推進を行っている。

ANSI/ASHRAE 135-1995 以降、ANSI/ASHRAE 135-2001, 135-2004, 135-2008, 135-2010, 135-2012 が発行され、2019年10月時点の最新は 135-2016 である\[1\]。

テスト版の規格に ANSI/ASHRAE 135.1があり、ANSI/ASHRAE 135.1-2003 以降、ANSI/ASHRAE 135.1-2007, 2009, 2011, 2013 が発行され、2019年10月時点の最新は 2019 である\[2\]。

## 日本での普及

日本では、電気設備学会（IEIEJ）が BACnet の ASHRAE/ANSI Standard 135-1995 に、積算、電力デマンド等の独自の拡張を加えた「BAS標準インタフェース」（IEIEJ-P-0003:2000）を発行した（通称、IEIEJp）\[3\]。しかし、BACnet との相互接続ができない仕様であったため、2002年にアデンダムA（IEIEIJ-P-003:2000-a）を策定した（通称、IEIEJp-A）。しかし、IEIEJp-A を使っても完全な相互運用性は達成できておらず、問題を残している。\[4\]

2006年9月に、電気設備学会は、ASHRAE/ANSI Standard 135-2004 をベースにした、「BACnetシステムインターオペラビリティガイドライン」（IEIEJ-G-0006:2006）を発行している。2017年3月に ASHRAE 135-2012 に対応する改定を行った（IEIEJ-G-0006:2017）。2019年5月に、ANSI/ASHRAE Standard 135-2016 の対応を追加する、「BACnetシステムインターオペラビリティガイドライン(追補)」（IEIEJ-G-0008:2019）を発行している。

## プロトコルの概要

BACnet プロトコルは、各種機器間の通信で使われるサービスを定義している。プロトコルサービスには、Who-Is、I-Am、Who-Has、I-Have といった機器およびオブジェクト発見に使われるものもある。Read-Property、Write-Property といったサービスはデータ共有に使われる。

サービスを使って動作するオブジェクトも各種定義されている。Analog Input、Analog Output、Analog Value、Binary Input、Binary Output、Binary Value、Multi-State Input、Multi-State Output、Calendar、Event-Enrollment、File、Notification-Class、Group、Loop、Program、Schedule、Command、Device などである。

[データリンク層](../Page/データリンク層.md "wikilink")と[物理層](../Page/物理層.md "wikilink")はいくつかの定義があり、[アークネット](https://ja.wikipedia.org/wiki/アークネット "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")、BACnet/IP、P2P over [RS-232](../Page/RS-232.md "wikilink")、[マスタースレーブ](https://ja.wikipedia.org/wiki/マスタースレーブ "wikilink")/[トークンパッシング](https://ja.wikipedia.org/wiki/トークンパッシング "wikilink") over [RS-485](../Page/EIA-485.md "wikilink")、[LonTalk](../Page/LONWORKS.md "wikilink") などがある。

BACnetでは、UDPポート番号「47808」が使われる。ちなみに、「47808」を16進数に変換すると「**BAC**0」になる。

## BACnetテスト

BACnetテストラボは、承諾および相互運用性テストサポートを提供するためにBACnet Internationalにより設立された。これは、BTLのマネージャーおよびBTL-WGで構成されている。 BTL活動は以下のようになっている。

  - BTLユーザー・ガイドに関する報告を発表
  - 毎年、BACnet International sponsored Interoperabilityワークショップを組織する
  - BACnetデバイスとして承認するためにBTLラボに賞を与えられた
  - BTL-WGの活動を支える
  - テストパッケージの問題があったらBTL-WGの助けによってBACnetチームを提供
  - BTLのテストのためのテストラボを承認する

またBTLは、BACnetラボでテストサービスを提供している。BACnet InternationalとBTLは、BACnet機器\[5\]のテストラボを設立・支援することで[SoftDEL Systems](https://ja.wikipedia.org/wiki/SoftDEL_Systems "wikilink") と合意に達した。SoftDEL\[6\] の本部はインド・プネーにあり、最先端の研究施設やBAC-netテストラボなど世界レベルの革新的な設備を有している。

## 脚注

## 外部リンク

  - [BACnet公式サイト](http://www.bacnet.org)
  - [BACnet International](http://www.bacnetinternational.org)
  - [BACnet Interest Group Europe](http://www.big-eu.org)
  - [BACnet Test Lab - SoftDEL Systems](http://www.softdel.com/)

### BACnetワーキンググループ

  - [Internet Protocol](http://groups.yahoo.com/group/bacnet-ip-wg/)
  - [Life Safety and Security](http://groups.yahoo.com/group/Security_extensions/)
  - [Lighting Applications](http://groups.yahoo.com/group/BACnetLighting/)
  - [MS/TP](http://groups.yahoo.com/group/bacnet-mstpwg/)
  - [Network Security](http://groups.yahoo.com/group/BACnetNS/)
  - [Objects and Services](http://groups.yahoo.com/group/bacnet-oswg/)
  - [Testing and Intoperability](http://groups.yahoo.com/group/bacnettiwg/)
  - [Utility Integration](http://groups.yahoo.com/group/BACnetUI/)
  - [Wireless Networking](http://groups.yahoo.com/group/BACnet-ZB-WG/)
  - [XML](http://groups.yahoo.com/group/BACnet-XML-WG/)
  - [Broadcast Reduction](http://groups.yahoo.com/group/bacnet-br-wg/)

### BACnetソフトウェア

  - [Open Source BACnet Protocol Stack](http://bacnet.sourceforge.net/)
  - [VTS - BACnet Test Software (Public Domain)](http://sourceforge.net/projects/vts/)
  - [BACmove - BACnet Explorer and HMI application](https://bacmove.com/)

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:設備](https://ja.wikipedia.org/wiki/Category:設備 "wikilink") [Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:製造](https://ja.wikipedia.org/wiki/Category:製造 "wikilink") [Category:スマートグリッド](https://ja.wikipedia.org/wiki/Category:スマートグリッド "wikilink") [Category:ビルオートメーション](https://ja.wikipedia.org/wiki/Category:ビルオートメーション "wikilink")

1.
2.
3.  [電気設備学会標準規格リスト](http://www.ieiej.or.jp/standard/index.html) 電気設備学会
4.  [BACnet(1)](http://www.m-system.co.jp/mstoday/plan/mame/2006-2007/0708/index.html) エムエスツデー、2007年8月号
5.  ["BACnet test lab at SoftDEL" 4 April 2006](http://www.csemag.com/article/179148-New_BACnet_Test_Lab_Established.php)
6.  ["BACnet product testing - SoftDEL Systems"](http://www.softdel.com/)