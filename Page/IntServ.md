> この記事は[IntServ](https://ja.wikipedia.org/wiki/IntServ)から翻訳されています。


**IntServ** (**イントサーブ**、**Integrated Services**) とは、[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")において[通信フロー](https://ja.wikipedia.org/wiki/通信フロー "wikilink")ごとに[帯域などの](https://ja.wikipedia.org/wiki/通信帯域 "wikilink")[ネットワーク資源](https://ja.wikipedia.org/wiki/ネットワーク資源 "wikilink")を確保することによって [QoS](../Page/Quality_of_Service.md "wikilink") (通信品質) を確保しようとする QoS 保証通信サービスである。[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") の RFC 1633 などの標準ドキュメントによって規定されている。

## 概要

IntServ には次の 2 つのサービスモデルがある。

  - 品質保証型サービス (Guaranteed Service) - 帯域と最大[遅延を保証するサービス](https://ja.wikipedia.org/wiki/通信遅延 "wikilink")。
  - 負荷制御型サービス (Controlled Load Service) - 遅延の目標値を持ち、流量をみずから制御する適応型[アプリケーションを想定したサービス](../Page/アプリケーションソフトウェア.md "wikilink")。ネットワークが混雑している場合であっても、利用率が低い[ベストエフォート](../Page/ベストエフォート.md "wikilink")・ネットワークと同等程度に動作することを目指している。

[実時間のアプリケーションの](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink") QoS 保証には帯域、遅延のほかに[ジッター](../Page/ジッター.md "wikilink") (遅延のばらつき) に関する保証も必要だが、IntServ の機構ではその実現は困難であり、保証項目としてふくまれていない。

上記のサービスを実現するため、IntServ においてはアプリケーションが特定のフローに対する保証を要求する[プロトコル](../Page/プロトコル.md "wikilink")として [RSVP](https://ja.wikipedia.org/wiki/RSVP "wikilink") (リソース予約プロトコル、Resource reSerVation Protocol) が用意されている。また、RSVP のメッセージがそのフローと同じパスを通過することを保証し、そのメッセージが通過する際に資源を予約することによって、要求されたサービスが実現されるようにしている。IntServ はコア[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")のオーバヘッドが大きいために普及しなかったが、RSVP の複雑さなどの問題点も普及を妨げる原因となっていたと考えられる。RSVP に代わるプロトコルを設計してそれらの問題点を解決しようという試みも行われている。

## 問題点

Intserv とくに RSVP は次のような理由から実際にはあまり利用されてこなかった。

  - スケーラブルでない。すなわち中間ルータにおいてフローごとの状態を記憶することが必要であり、バックボーンにおいては状態数が膨大になるためスケールしない。
  - 技術主導であり、現状とのギャップが大きかった。メカニズムが複雑すぎ、システム管理が困難であり、課金やコスト等のビジネスモデルと整合しないなど、実際の運用には多くの問題点があった。
  - シグナリングが本質的に難しい。動的な通信状態管理は本質的に解決が難しい問題をいろいろと持っていることがわかった。

これらの問題点を解決する QoS 保証法として [DiffServ](../Page/DiffServ.md "wikilink") が提案された。IntServ が普及しなかったのに比べて DiffServ はひろく使用されているが、次節でのべるように、問題点もあり、IntServ と組み合わせて使用する方法が提案されている。

## DiffServ との組合せ

前記のようにフロー単位の制御をおこなう IntServ はスケールせず、大規模なネットワークにおいて使用できないという問題点がある。それに対してフローをクラスにまとめて制御する [DiffServ](../Page/DiffServ.md "wikilink") は精密な制御ができないため、トラフィック量が限界にちかづくにつれて QoS が保証されないことが多くなるという問題点がある。そこで、LAN やアクセス網においては IntServ を使用し、コアネットワークにおいては DiffServ を使用するという方法 (たとえば "IntServ over DiffServ" とよばれる方法) が工夫された。

このような方法の多くにおいては RSVP が使用され、そのメッセージがコア網も通過するが、コア網においてはそのメッセージによる資源予約はおこなわれない。そのかわり、エッジルータによってフローごとの要求がクラスごとに束ねられ、コア網においてはクラスごとに資源が確保される。RSVP はもともとこのように端点間のパスのなかの一部だけで動作することができるように設計されている。この方法は、コアネットワークのおおくは余裕があって ([オーバープロビジョン](https://ja.wikipedia.org/wiki/オーバープロビジョン "wikilink")されていて) DiffServ がうまくはたらくが、アクセス網においてはしばしば輻輳が発生するという現状に合っていると考えられる。

## 参考文献

  - RFC 1633 - Integrated Services in the Internet Architecture: an Overview, IETF.
  - RFC 2211 - Specification of the Controlled-Load Network Element Service, IETF.
  - RFC 2212 - Specification of Guaranteed Quality of Service, IETF.
  - RFC 2215 - General Characterization Parameters for Integrated Service Network Elements, IETF.
  - RFC 2205 - Resource ReSerVation Protocol (RSVP), IETF.

## 関連項目

  - [Quality of Service](../Page/Quality_of_Service.md "wikilink") (QoS)
  - [リソース予約プロトコル](../Page/Resource_Reservation_Protocol.md "wikilink") (RSVP)
  - [DiffServ](../Page/DiffServ.md "wikilink") (ディフサーブ)

[Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")