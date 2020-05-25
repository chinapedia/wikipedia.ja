> この記事は[仮想LANカード](https://ja.wikipedia.org/wiki/仮想LANカード)から翻訳されています。


**仮想LANカード(仮想NIC)**は、ソフトウェアによる[仮想化](../Page/仮想化.md "wikilink")技術を用いて、一般的な[ネットワークインタフェースカード](https://ja.wikipedia.org/wiki/ネットワークインタフェースカード "wikilink")(NIC)などのネットワーク機器をエミュレーションする仕組みや、その仕組みによって実装されたソフトウェアのことを示す。

ソフトウェアによっては、**仮想NIC**や**仮想インターフェイス**とも呼ばれる。

## 概要

LANカードをソフトウェアで仮想化することにより、仮想LANカードを作成する。すると、OSやアプリケーションソフトウェアからは、物理的なコンピュータに装着されているLANカードと同様に仮想LANカードが認識され扱われる。

これにより、以下のようなメリットが生ずる。

  - 本来、物理的なインターフェイスを持たない[バーチャルマシン](https://ja.wikipedia.org/wiki/バーチャルマシン "wikilink")(VM)内のOSが、物理的なLANカードを持っていると認識し、通信を行おうとする。実際には仮想LANカードに対してソフトウェア的に通信が行われるだけであるが、VM側でその通信内容をトラップすることにより、VMの内側と外側との通信が可能になる。
  - レイヤ2の[VPNを構築することが容易になる](../Page/Virtual_Private_Network.md "wikilink")。

## VMwareにおける実装例

[VMware](../Page/VMware.md "wikilink")では仮想LANカードが実装されており、実用的に動作する。VM内のOSには、汎用的な[Ethernet](https://ja.wikipedia.org/wiki/Ethernet "wikilink")コントローラのチップが搭載されたネットワークカードが計算機に装着されているように見える。しかし、実際にはそのネットワークカードは物理的には存在せず、VMによって仮想的にエミュレーションされたものである。VM内部のソフトウェアはそれに気が付かない。この仕組みにより、複数台のVM間やホスト計算機との間のEthernet通信が可能となる。

## PacketiX VPNにおける実装例

[PacketiX VPNでは仮想LANカードが実装されており](../Page/PacketiX_VPN.md "wikilink")、実用的に動作する。これにより、インターネットなどを経由して離れた場所にあるコンピュータ内の[仮想HUB](https://ja.wikipedia.org/wiki/仮想HUB "wikilink")にレイヤ2で仮想的に接続することができる。これを応用して、リモートアクセスVPNや拠点間接続VPNを柔軟に構築することができる。

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:ソフトウェア](https://ja.wikipedia.org/wiki/Category:ソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")