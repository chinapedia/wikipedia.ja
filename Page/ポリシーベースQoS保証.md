> この記事は[QoS](https://ja.wikipedia.org/wiki/QoS)から翻訳されています。


[ポリシーベース管理](../Page/ポリシーベース管理.md "wikilink")の手法にもとづいて [QoS](https://ja.wikipedia.org/wiki/Quality_of_Service "wikilink") (サービス品質、とくに通信品質) を保証することを**ポリシーベースQoS保証**という。

## ポリシー規則の例

QoS 保証のためのポリシー規則の例をあげる。

if (Source_IP_address == 192.168.0.1) { Priority = “high”; }

この規則は対象の機器があつかう各 [IP](../Page/Internet_Protocol.md "wikilink") [パケット](../Page/パケット.md "wikilink")に適用され、そのパケットが [IPアドレス](../Page/IPアドレス.md "wikilink") 192.168.0.1 を始点とするパケットならば高い優先度をあたえることを意味する。このようにこの規則をふくむポリシーをポリシーサーバが [IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上の[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")に配布することにより、上記の[通信フロー](https://ja.wikipedia.org/wiki/通信フロー "wikilink")が優先配送される。すなわち、このフローを他のフローより優先することによって QoS を保証することを意図している。このようにフローをクラスわけして QoS に差をつける QoS 保証サービスを [DiffServ](../Page/DiffServ.md "wikilink") という。

## ポリシーベース管理のためのプロトコル

[ポリシーベース管理](../Page/ポリシーベース管理.md "wikilink")におけるポリシーの配布とその要求のためにプロトコルとして、2000 年に [IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") において [COPS](https://ja.wikipedia.org/wiki/COPS "wikilink") (Common Open Policy Service) が標準化された。ポリシーベース QoS 保証においても COPS を使用することができる。たとえば、DiffServ のためのポリシー表現法 (ポリシー情報ベース) として Diffserv PIB (Policy Information Base) が 2003 年に IETF において標準化されている。COPS のひとつの用法 (COPS-PR) を Diffserv PIB と組み合わせて使用することによって、Diffserv ポリシーの配布と要求を行うことができる。

## ポリシーベース QoS の実装

製品化された QoS 保証のためのポリシーサーバの例としてつぎのようなものがある。

  - IP Highway 社 (現在は存在しない) の Open Policy System

<!-- end list -->

  - Cisco 社 の QoS Policy Manager (QPM)

<!-- end list -->

  - Hewlett Packard 社と日立との協業によって開発された PolicyXpert

これらのなかで Open Policy System と PolicyXpert は限定的ではあるが COPS-PR を使用している。

## ポリシーベース QoS 保証とくに COPS の将来

ポリシー管理に関する標準化は IETF においてルータへの DiffServ の設定などネットワーク下層を中心にすすみ、それに基づいてポリシーサーバ等の製品が開発されてきた。しかし、標準化はこれまで必ずしも成功していない。PCIM はこれらの製品において重要な位置にはないし、ポリシー管理の有力な適用先と考えられてきた QoS においては Diffserv PIB が複雑で扱いにくいものになっている。そのため COPS が今後大きく普及するとは考えにくい。しかし、[NGN](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink") においては [3GPP](https://ja.wikipedia.org/wiki/3GPP "wikilink") などがポリシー設定等のためのプロトコルとして COPS を採用しているため、一部で使用されることになるであろう。

## 関連項目

  - [ポリシー](https://ja.wikipedia.org/wiki/ポリシー "wikilink")
  - [ポリシーベース・ネットワーク管理](https://ja.wikipedia.org/wiki/ポリシーベース・ネットワーク管理 "wikilink")
  - [ポリシーベース管理](../Page/ポリシーベース管理.md "wikilink")

[Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink")