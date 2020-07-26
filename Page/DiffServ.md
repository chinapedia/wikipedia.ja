> この記事は[DiffServ](https://ja.wikipedia.org/wiki/DiffServ)から翻訳されています。


**DiffServ** (**ディフサーブ**、**Differentiated Services**) は [IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")において [IntServ](../Page/IntServ.md "wikilink") のように[通信フロー](https://ja.wikipedia.org/wiki/通信フロー "wikilink")ごとに [QoS](../Page/Quality_of_Service.md "wikilink") 保証 (通信品質保証) を行うのでなく、複数のフローをまとめて (アグリゲートして) 数個程度のクラスを作り、クラスごとに決まった QoS 保証法の組合せを適用する 統合型QoS 保証法である。[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") の RFC 2474 などの標準ドキュメントによって規定されている。

## 概要

ネットワークが混雑すると、全ての種類の[トラフィック](https://ja.wikipedia.org/wiki/トラフィック "wikilink")に対して平等に QoS を保証することはできなくなる。そこで、DiffServ においてはトラフィックをいくつかのクラスに分け、それらを優先度付けするなど、差をつけて扱う。このようなサービスとして最も有名なのは[オリンピック・サービス](https://ja.wikipedia.org/wiki/オリンピック・サービス "wikilink")である．オリンピック・サービスにおいては金、銀、銅というクラスを設けて、金のトラフィックを最優先で、銀のトラフィックをそれに次ぐ優先度で転送する。また、[Web](../Page/World_Wide_Web.md "wikilink")、音声、画像など、[メディア](../Page/メディア.md "wikilink")の種類ごとに異なるクラスを割り当てることもできる。

DiffServ を実現するには、第 1 に DiffServ を適用するネットワークの入口[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink") (ingress router) においてフローの種類に基づくクラス分けを行い、IP [パケット](../Page/パケット.md "wikilink")の [DSフィールド](https://ja.wikipedia.org/wiki/DSフィールド "wikilink")にその結果 ([DSCP](https://ja.wikipedia.org/wiki/DSCP "wikilink"), DiffServ Code Point) を書きこむ。これをマーキングという。クラス分けのためには[クラシファイアを使用する](https://ja.wikipedia.org/wiki/パケット・クラシファイア "wikilink")。第 2 にネットワークのコア[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")において DS フィールドの値に基づいて[パケット・スケジューリング](../Page/パケット・スケジューリング.md "wikilink")などの処理を行う。

## ホップごとの振舞い (PHB)

DiffServ における 1 台の[コアルータ](https://ja.wikipedia.org/wiki/コアルータ "wikilink")による転送処理を**[ホップごとの振舞い](https://ja.wikipedia.org/wiki/ホップ_\(ネットワーク\) "wikilink")** (Per-Hop Behavior, **PHB**) という。PHB ごとに、そのために使用する DSCP の値が決められている。 IETF において標準化された PHB として、つぎの 4 種類がある。

  - Expedited Forwarding PHB (EF) - 端点間の帯域保証をおこなう仮想専用線サービスのための PHB である。DiffServ ネットワークの[エッジルータ](https://ja.wikipedia.org/wiki/エッジルータ "wikilink")において契約分のみのトラフィックを通過させ、コアルータにおいては契約分の総和を上回る帯域を確保する ([オーバープロビジョン](https://ja.wikipedia.org/wiki/オーバープロビジョン "wikilink")する)。コアルータでは、[優先キューイング](https://ja.wikipedia.org/wiki/優先キューイング "wikilink")を用いて[トラフィックを制御する](https://ja.wikipedia.org/wiki/ネットワーク・トラフィック "wikilink")。EF においては 1 個だけの DSCP を使用する。
  - Assured Forwarding PHBs (AF) - EF よりゆるい保証サービス、すなわち最低帯域保証つきの[ベストエフォート](../Page/ベストエフォート.md "wikilink")・サービスのための PHB である。DiffServ ネットワークのエッジルータにおいて契約分をこえたトラフィックに属するパケットにマークをつけ、コアルータが混雑した場合にはマークがついたパケットを優先的に破棄する。AF のためには AF1 ～ AF4 という 4 つのクラスが標準化されているが、各 AF クラスは 3 個の DSCP を使用する。したがって、DSCP の値としては AF11 ～ AF43 という 12 個が使用される。
  - Default Forwarding PHB (DF) - 最小限の資源を割り当てる条件があることを除いて、ベストエフォートを意味する。Best Effort PHB (BE) と呼ばれることもある。DF のための DSCP は 0 (だけ) である。
  - Class Selecor PHB (CS) - Cisco が実装している [IP優先度](https://ja.wikipedia.org/wiki/IP優先度 "wikilink") (IP precedence) を使用する QoS 保証法と互換性のある PHB である。CS のためには 8 個の DSCP が割り当てられている。

DiffServ においては、計測の結果として違反がみつかれば、いったんマーキングされたパケットに対して優先度が低い別のマークに付けかえる処理を行う場合がある。このような処理を[リマーキング](https://ja.wikipedia.org/wiki/リマーキング "wikilink")という。

## 静的なサービスと動的なサービス

DiffServ を固定的なサービスとして実施するのであれば、各ユーザとネットワーク・オペレータ ([ISP](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、[通信事業者など](../Page/電気通信事業者.md "wikilink")) との間であらかじめ[サービス水準合意](https://ja.wikipedia.org/wiki/サービス水準合意 "wikilink") (SLA) を結び、それに従ってネットワークを固定的に設定しておけばよい。しかし、ユーザの要求はときによって変化するから、その都度必要な[サービスレベル仕様](https://ja.wikipedia.org/wiki/サービスレベル仕様 "wikilink") (SLS) を指定できるほうがネットワークをより柔軟に利用することができる。

このようにユーザが動的に SLS を指定する相手を[帯域ブローカ](https://ja.wikipedia.org/wiki/帯域ブローカ "wikilink") (Bandwidth Broker)\[1\] という。帯域ブローカはネットワーク資源を管理し、[アドミッション制御](https://ja.wikipedia.org/wiki/アドミッション制御 "wikilink")をおこなう。帯域ブローカへの資源要求のためのプロトコルとして [RSVP](https://ja.wikipedia.org/wiki/RSVP "wikilink") (リソース予約プロトコル、Resource reSerVation Protocol) を使用することもできるが、[COPS](https://ja.wikipedia.org/wiki/COPS "wikilink") (Common Open Policy Service) などのプロトコルによって帯域ブローカに直接要求することもできる。帯域ブローカは、高速な研究・教育用のネットワーク最先端技術を開発してきた [Internet2](../Page/Internet2.md "wikilink") プロジェクトなどで研究されてきた。

このような DiffServ のための資源管理の方法として、Westberg, Karagiannis ら\[2\]は RMD (Resource Management in DiffServ) を提案し、RMD を [QoS-NSLP](https://ja.wikipedia.org/wiki/QoS-NSLP "wikilink") によって実現するために、QoS-NSLP のための QoS 仕様記述法 (QSPEC) のひとつとして RMD-QOSM\[3\] を IETF に提案している。RMD においてはシグナリング方式として RSVP やそれに近いものが使用される。RMD は IntServ と DiffServ とを組み合わせた QoS 保証法のひとつだとかんがえられるが、このような IntServ との組合せについては [IntServ](../Page/IntServ.md "wikilink") の項を参照。

## 参考文献

  - RFC 2474 — Definition of the Differentiated Services Field (DS Field) in the IPv4 and IPv6 Headers
  - RFC 2475 — An Architecture for Differentiated Services
  - RFC 2597 — Assured Forwarding PHB Group
  - RFC 3140 — Per Hop Behavior Identification Codes (Obsoletes RFC 2836)
  - RFC 3246 — An Expedited Forwarding PHB (Obsoletes RFC 2598)
  - RFC 3260 - New Terminology and Clarifications for Diffserv

<references />

## 外部リンク

  - IETF [DiffServ Working Group](http://www.ietf.org/html.charters/OLD/diffserv-charter.html) page
  - Cisco Whitepaper — [DiffServ-The Scalable End-to-End Quality of Service Model](http://www.cisco.com/en/US/products/ps6610/products_white_paper09186a00800a3e2f.shtml)

## 関連項目

  - [Quality of Service](../Page/Quality_of_Service.md "wikilink") (QoS)
  - [サービス水準合意](https://ja.wikipedia.org/wiki/サービス水準合意 "wikilink") (SLA)
  - [IntServ](../Page/IntServ.md "wikilink") (イントサーブ)
  - [トラフィックシェーピング](../Page/トラフィックシェーピング.md "wikilink")
  - [ランダム初期検知](https://ja.wikipedia.org/wiki/ランダム初期検知 "wikilink")

[Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  Sohail, S. and Jha, S., “The Survey of Bandwidth Broker”, Technical Report UNSQ-CSE-TR-0206, University of New South Wales, Sydney, Australia, May 2002.
2.  Westberg, L, Csaszar, A., Karagiannis, G., Marquetant, A., Partain, D., Pop, O., Rexhepi, V., Szabo, R., and Takacs, A., "Resource management in Diffserv (RMD): A Functionality and Performance Behavior Overview," 7th IFIP/IEEE Workshop on Protocols for High-Speed Networks (PfHSN’2002).
3.  Báder, A., Westberg, L, Karagiannis, G., Kappler, C., and Phelan, T., "RMD-QOSM - The Resource Management in Diffserv QOS Model", work in progress, IETF.