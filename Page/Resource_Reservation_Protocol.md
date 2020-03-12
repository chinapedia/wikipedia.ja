> この記事は[Resource Reservation Protocol](https://ja.wikipedia.org/wiki/Resource_Reservation_Protocol)から翻訳されています。


**Resource Reservation Protocol**（リソース リザベーション プロトコル、訳：リソース予約プロトコル、略：**RSVP**）は、[通信プロトコル](../Page/通信プロトコル.md "wikilink")の一つ。[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")で送信元から送信先までの[帯域を事前に予約することで](../Page/帯域幅.md "wikilink")、ネットワーク上の通信路の品質保証を行なう[プロトコル](../Page/プロトコル.md "wikilink")である。[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") の RFC 2205 によって規定されている。

## 概要

RSVPは[インターネット・プロトコル](https://ja.wikipedia.org/wiki/インターネット・プロトコル "wikilink") (IP) または[UDP](../Page/User_Datagram_Protocol.md "wikilink") (User Datagram Protocol) の上位プロトコルとして機能し、2台のコンピュータが通信経路上における [CPU](../Page/CPU.md "wikilink")、[バッファ](../Page/バッファ.md "wikilink")、帯域などのリソースを確保し、[QoS](../Page/Quality_of_Service.md "wikilink")（通信品質）を保証する。RSVPは主に[IntServ](../Page/IntServ.md "wikilink")（イントサーブ）と呼ばれるQoS保証方式のために使用される。

RSVP においては、送受信を行う2台のコンピュータの間で[データ通信](../Page/データ通信.md "wikilink")開始時に制御メッセージをやりとりすることによって、両者を結ぶ経路上にある[ルーター](../Page/ルーター.md "wikilink")や[スイッチが伝送帯域を確保する](../Page/スイッチングハブ.md "wikilink")。テレビ会議やリアルタイムの動画像配信などでは即時性・連続性が求められ、RSVPはこれらの一定量のデータ伝送速度が連続的に必要なシステムのために開発されている。

*R*esource re*S*er*V*ation *P*rotocol という奇妙な略し方は、[欧米](../Page/欧米.md "wikilink")で手紙の末尾に書く "RSVP"（Répondez s'il vous plaît、[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink")で「ご返事をお願いします」）に合わせたものである。

なお、RSVPの問題点については[IntServ](../Page/IntServ.md "wikilink")の項を参照。

## RSVP に代わるプロトコルの開発

RSVP の問題点を解決するために様々なプロトコルが提案されてきたが、IETF において標準化されたものはなく、RSVP以上に広く使用されているものはない。

  - ST-II (The Internet Stream Protocol, version 2)\[1\] - RSVP に先立って開発されたプロトコルであるが、RSVP とは違って送信者が最初のメッセージを送信した (sender-initiated)。
  - YESSIR (YEt another Sender Session Internet Reservations)\[2\] - ST-IIと同様に送信者が最初のメッセージを送るプロトコルであり、[RTCP](../Page/Real-time_Transport_Control_Protocol.md "wikilink") (Real-time Transport Control Protocol) の拡張である。
  - Boomerang\[3\] - [ICMP](https://ja.wikipedia.org/wiki/ICMP "wikilink") (Internet Control Message Protocol) とともに使用する。

IETFのNSIS (Next-Step In Signaling) ワーキンググループにおいては，この解析結果に基づいてつぎのような新たなプロトコルを標準化しつつある．

  - QoS-NSLP - Bádler ら\[4\]は、RSVPの問題点すなわち常に受信者が最初のメッセージを送らなければならない、メッセージの伝達が遅い、階層的なネットワーク（例えば[Diffserv](https://ja.wikipedia.org/wiki/Diffserv "wikilink")との組合せ）に使用しにくいといった問題点を解決するため、NSISにおけるシグナリング・プロトコルである [NSLP](https://ja.wikipedia.org/wiki/NSLP "wikilink") (NSIS Signaling Layer Protocol) の一部として[QoS-NSLP](https://ja.wikipedia.org/wiki/QoS-NSLP "wikilink")を提案している。QoS-NSLPはさまざまな種類のQoS保証に対応するため、QoS仕様記述法の部分をQSPEC（QoS仕様）テンプレートとして分離している。

## 脚注

## 参考文献

  - RFC 2205 - Resource ReSerVation Protocol (RSVP), IETF.
  - RFC 2210 - The Use of RSVP with IETF Integrated Services, IETF.
  - RFC 2211 - Specification of the Controlled-Load Network Element Service, IETF.
  - RFC 2212 - Specification of Guaranteed Quality of Service, IETF.

## 関連項目

  - [Quality of Service](../Page/Quality_of_Service.md "wikilink") (QoS)
      - [IntServ](../Page/IntServ.md "wikilink")（イントサーブ）
      - [DiffServ](../Page/DiffServ.md "wikilink")（ディフサーブ）

[Category:トランスポート層プロトコル](https://ja.wikipedia.org/wiki/Category:トランスポート層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  Topolcic, C., Ed., “Experimental Internet Stream Protocol, Version 2 (ST-II)”, RFC 1190, IETF, October 1990.
2.  Pan, P. and Schulzrinne, H., “YESSIR: A Simple Reservation Mechanism for the Internet”, ACM SIGCOMM Computer Communication Review, Vol. 29, No. 2, April 1999.
3.  Feher, G., Nemeth, K., Maliosz, M., Cselenyi, I., Bergkvist, J., Ahlard, D., and Engborg, T., “Boomerang – A Simple Protocol for Resource Reservation in IP Networks”, IEEE Workshop on QoS Support for Real-Time Internet Applications, June 1999.
4.  Báder, A., Karagiannis, G., Westberg, L., Kappler, C., Phelan, T., Tschofenig, H., and Heijenk, G., “QoS Signaling Across Heterogeneous Wired/Wireless Networks: Resource Management in Diffserv Using the NSIS Protocol Suite”, 2nd Int’l Conference on Quality of Service in Heterogeneous Wired/Wireless Networks (QShine’05), pp. 51–51, Aug. 2005.