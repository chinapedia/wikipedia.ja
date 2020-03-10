> この記事は[ZigBee](https://ja.wikipedia.org/wiki/ZigBee)から翻訳されています。


[Eazix_numbered.jpg](https://ja.wikipedia.org/wiki/File:Eazix_numbered.jpg "fig:Eazix_numbered.jpg") **ZigBee**（じぐびー）とは、[センサーネットワーク](https://ja.wikipedia.org/wiki/センサーネットワーク "wikilink")を主目的とする近距離[無線通信](../Page/無線通信.md "wikilink")規格の一つ。この通信規格は、転送可能距離が短く[転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")も非常に低速である代わりに、安価で消費電力が少ないという特徴を持つ。従って、電池駆動可能な超小型機器への実装に向いている。基礎部分の（電気的な）仕様は[IEEE 802.15.4として規格化されている](../Page/IEEE_802.15.md "wikilink")。論理層以上の機器間の通信[プロトコル](../Page/プロトコル.md "wikilink")については「[ZigBeeアライアンス](https://ja.wikipedia.org/wiki/ZigBeeアライアンス "wikilink")（ZigBee Alliance）」が仕様の策定を行っている。

なお、ZigBeeの名称は[ミツバチ](../Page/ミツバチ.md "wikilink")（Bee）が[ジグザグに飛び回る行動にちなんで名付けられた](https://ja.wikipedia.org/wiki/ミツバチのダンス "wikilink")\[1\]。

## 概要

データ[転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")は20Kbps-250kbps。使用する[無線](../Page/無線.md "wikilink")[周波数](../Page/周波数.md "wikilink")帯によって異なり、[2.4GHz](https://ja.wikipedia.org/wiki/2.4GHz "wikilink")では250Kbps、902-928MHzでは40Kbps、868-870MHzでは20Kbpsとなる。[900MHz帯](https://ja.wikipedia.org/wiki/900MHz帯 "wikilink")を用いたものは主に米国向け、[800MHz帯](https://ja.wikipedia.org/wiki/800MHz帯 "wikilink")を用いたものは主に欧州向けの仕様であり、[電波法](../Page/電波法.md "wikilink")の関係から日本国内で利用できるのはISMとして開放されている2.4GHz帯を用いた仕様のみである。

日本企業各社の実験によれば、実測の通信速度は、192Kbpsまでとされており、安定した通信を行うためには144Kbps程度の情報伝達に限定されるとの報告もある。

日本でZigBee機器を使用するには、その機器の性能が特定無線設備として[技術基準適合証明](https://ja.wikipedia.org/wiki/技術基準適合証明 "wikilink")または[工事設計認証](https://ja.wikipedia.org/wiki/工事設計認証 "wikilink")により、電波法で定められた技術基準を満たしていることの証明が必要である。この証明の無い機器を無免許で使用することは法令に抵触する。評価や実験などで、証明の無い機器を使用する場合は、外部に電波の漏れないシールドルーム内で行う必要がある。

ZigBee端末には中継機能があり、中継を繰り返す事でZigBee素子同士が通信を行える限り情報を伝える事が出来る。

送受信の頻度にもよるが、[乾電池](../Page/乾電池.md "wikilink")程度の電力で100日～数年間稼動し、電源も含めて完全に無配線で家電ネットワークを構築する事が出来る。

ひとつのZigBeeネットワークには、最大で65,536個(アドレスで0x0000～0xFFFF)のZigBee端末を接続することが出来る。これは単にアドレスの割り振り最大値であり、ひとつのZigBeeネットワークで実用的に使用できる端末数は通信頻度等に依存するため個々の最終商品によって異なる。

なおZigBeeアライアンスが認定した製品が正式なZigBeeであり、市場では802.15.4部分のみを利用した製品や準拠しただけの非認定製品に対してZigBeeの表現が用いられる事がある。ZigBeeの名称はZigBeeアライアンスの[商標](../Page/商標.md "wikilink")であるため、それら製品は商標権を犯したことになるので、使用する場合は注意することが望ましい。 また、準拠品や電波法無認可品が見られるが、実際に使用する時はユーザー側でそれら取得を行う必要がある。

## ZigBeeのネットワーク構成

ZigBeeの端末は以下の3種類に分類される。

  - ZigBee Coordinator(ZC):ネットワーク内に1台存在し、ネットワークの制御を行う端末。
    IEEE 802.15.4-2003ではPAN coordinatorとしてのFFD(Full-Function Device)にあたる。
  - ZigBee Router(ZR):データ中継機能を含むZigBee端末。
    IEEE 802.15.4-2003ではCoordinatorとしてのFFDにあたる。
  - ZigBee End Device(ZED):データ中継機能を持たないZigBee端末。
    IEEE 802.15.4-2003ではRFD(Reduced-Function Device)、またはFFDにあたる。

ZigBeeの特徴は、[メッシュ型やツリー型のネットワークを構成し](https://ja.wikipedia.org/wiki/メッシュネットワーク "wikilink")、ZigBee Routerがデータを中継することで、直接電波の届かない端末間でも通信が可能な点にある。これにより一部の端末が停止した場合にも、迂回経路を使って通信を継続できる他、低消費電力で広範囲で通信を行う事が出来る。

## ZigBeeのレイヤ構造

ZigBeeのレイヤは以下の5種類に分類される。

  - APL層:使用者が作成
    APS層:ZigBee Allianceが規定
    NWK層:ZigBee Allianceが規定
    MAC層:IEEE 802.15.4-2003を使用
    PHY層:IEEE 802.15.4-2003を使用

## APSプリミティブ

  - APSDE-DATA
  - APSME-BIND
  - APSME-GET
  - APSME-SET
  - APSME-UNBIND
  - APEME-ESTABLISH-KEY
  - APSME-TRANSPORT-KEY
  - APSME-UPDATE-DEVICE
  - APSME-REMOVE-DEVICE
  - APSME-REQUEST-KEY
  - APSME-SWITCH-KEY

ZigBee 2006で追加：

  - APSME-ADD-GROUP
  - APSME-REMOVE-GROUP
  - APSME-REMOVE-ALL-GROUPS

## NWKプリミティブ

  - NLDE-DATA
  - NLME-NETWORK-DISCOVERY
  - NLME-NETWORK-FORMATION
  - NLME-PERMIT-JOINING
  - NLME-START-ROUTER
  - NLME-JOIN
  - NLME-DIRECT-JOIN
  - NLME-LEAVE
  - NLME-RESET
  - NLME-SYNC
  - NLME-GET
  - NLME-SET

ZigBee 2006で追加：

  - NLME-ROUTE-ERROR
  - NLME-ROUTE-DISCOVERY

ZigBee 2007で追加：

  - NLME-ED-SCAN
  - NLME-SYNC-LOSS

ZigBee 2007で変更：

  - NLME-NWK-STATUS ← NLME-ROUTE-ERROR

## Information Base

  - APS Information Base(AIB)
  - NWK Information Base(NIB)
  - MAC PAN Information Base(MAC PIB)
  - PHY PAN Information Base(PHY PIB)

## プロファイル

  - Public Application Profile：**Smart Energy(SE)**、**Home Automation(HA)**
  - Stack Profile：**Network Specific(0x00)**、**ZigBee Feature Set(0x01)**、**ZigBee PRO Feature Set(0x02)**

## 接続手順の実際

1.  ZCがNLME-NETWORK-FORMATIONを発行し、PANを開始する
2.  ZCはNLME-PERMIT-JOININGを発行することでAssociationPermit=TRUEの状態にして他デバイスの参加を受け付ける
3.  ZRやZEDがNLME-NETWORK-DISCOVERYを発行し、AssociationPermit=TRUEのPANを探す
4.  ZRやZEDはNLME-JOINを発行し、PANに参加する
5.  ZRが中継機能を動作させる場合にはNLME-START-ROUTERを発行する
6.  ZRが他デバイスの参加を受け付ける場合には中継機能を動作させた上で、NLME-PERMIT-JOININGを発行する

## バージョン

  - ZigBee-2004 Specification(v.1.0)

<!-- end list -->

  -
    Document 053474r06

<!-- end list -->

  - ZigBee-2006 Specification

<!-- end list -->

  -
    Document 053474r13

<!-- end list -->

  - ZigBee-2007 Specification

<!-- end list -->

  -
    Document 053474r17

## 日本国電波法認証取得済・ZigBeeアライアンス認証済みモジュール

  - [エー・アンド・デイ](../Page/エー・アンド・デイ.md "wikilink") AD1321-1MW : 1mW（0.001262W/MHz, 007WWCUL0412）
  - [エー・アンド・デイ](../Page/エー・アンド・デイ.md "wikilink") AD1321-10MW : 10mW（0.010000W/MHz, 007WWCUL0459）
  - [ルネサス販売](https://ja.wikipedia.org/wiki/ルネサス販売 "wikilink") YCSCZB2A2NN : 1mW（0.0013W/MHz, 001NYCA1390）
  - [ルネサス販売](https://ja.wikipedia.org/wiki/ルネサス販売 "wikilink") YCSCZB3A2NN : 1mW（0.0007W/MHz, 001WWCA1018）
  - [Digi](https://ja.wikipedia.org/wiki/Digi "wikilink") XBee : 2mW（0.7 mW/MHz,201WW07215214）
  - [Digi](https://ja.wikipedia.org/wiki/Digi "wikilink") XBee-PRO : 10mW（5.63 mW/MHz,201WW08215111　又は0.00362W/MHz, 005WWCA0079）
  - Wireless Glue Networks ZCC-2431-M:(0.00057W/MHz,005WWCA0176)

上記説明 メーカー（販売）名、品名、メーカー名称値、（認証値、認証番号）

## 脚注

<references/>

## 関連項目

  - [RF4CE](https://ja.wikipedia.org/wiki/RF4CE "wikilink")

## 外部リンク

  - [ZigBee Alliance](http://www.zigbee.org/)
  - [ZigBee SIGジャパン](http://www.zbsigj.org/)
  - [ZigBee 2007 仕様書 (ZigBee Alliance)※登録が必要](http://www.zigbee.org/Products/DownloadZigBeeTechnicalDocuments.aspx)
  - [ZigBee和訳仕様書 (ZigBee SIGジャパン)](http://www.zbsigj.org/download.htm)
  - [IEEE 802.15.4-2003 仕様書 (Get IEEE 802)](http://standards.ieee.org/getieee802/download/802.15.4-2003.pdf)
  - [ZigBee Specification Comparison Matrix (Daintree Networks Resources)](http://www.daintree.net/resources/spec-matrix.php)
  - [フィールドバスの色々 ZigBee (マイコミジャーナル)※間違いが多いので注意](https://news.mynavi.jp/column/sopinion/158/index.html)
  - [5分で絶対に分かるZigBee (@IT)※間違いが多いので注意](http://www.atmarkit.co.jp/frfid/special/5minzb/01.html)
  - [FreakLabs Open Source Zigbee Protocol Stack Blog](http://www.freaklabs.org)

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink") [Category:ホームオートメーション](https://ja.wikipedia.org/wiki/Category:ホームオートメーション "wikilink") [Category:ビルオートメーション](https://ja.wikipedia.org/wiki/Category:ビルオートメーション "wikilink") [Category:メッシュネットワーク](https://ja.wikipedia.org/wiki/Category:メッシュネットワーク "wikilink")

1.  ["ZigBee Wireless Networking"](http://www.eetimes.com/design/embedded-internet-design/4201087/ZigBee-applications--Part-1-Sending-and-receiving-data/), Drew Gislason (via EETimes)