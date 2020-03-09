> この記事は[Internet Protocol](https://ja.wikipedia.org/wiki/Internet_Protocol)から翻訳されています。


**Internet Protocol** （**インターネット・プロトコル**、**IP**） とは、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")における主要な[通信プロトコル](https://ja.wikipedia.org/wiki/通信プロトコル "wikilink")である。

ネットワークに接続されている全てのコンピュータに対して、[IPアドレス](../Page/IPアドレス.md "wikilink")と呼ばれる数字を付与し、その数字を用いて通信先の指定及び呼び出しを行う（この考え方は[電話番号](https://ja.wikipedia.org/wiki/電話番号 "wikilink")と似ている）。俗に[IPアドレス](../Page/IPアドレス.md "wikilink")を「IP」と呼ぶことがあるが、厳密には誤記・誤称である。

最初の主要なバージョンは[Internet Protocol Version 4](https://ja.wikipedia.org/wiki/IPv4 "wikilink") (IPv4) であり、最も普及しているが、[IPアドレスの枯渇問題により](../Page/IPアドレス枯渇問題.md "wikilink")、後継の [Internet Protocol Version 6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") (IPv6) への移行を推奨している人たちがいる\[1\]。

## 概要

IPは、[インターネット・プロトコル・スイート](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")に基づく[インターネットワークにおいて](https://ja.wikipedia.org/wiki/インターネットワーキング "wikilink")、[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")（または[パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")）を中継するのに使われる主要な[通信プロトコル](https://ja.wikipedia.org/wiki/通信プロトコル "wikilink")である。[インターネット層](https://ja.wikipedia.org/wiki/インターネット層 "wikilink")の主たるプロトコルであり、送信元[ホストから宛先ホストへ](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")[IPアドレス](../Page/IPアドレス.md "wikilink")に基づいてデータグラムを送付する役割を担っている。そのため、送付すべきデータを[カプセル化したデータグラム構造が定義されている](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。また、送信元と宛先を示すのに使われる[アドレッシング方法も定義されている](../Page/IPアドレス.md "wikilink")。

[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の[ネットワーク層](https://ja.wikipedia.org/wiki/ネットワーク層 "wikilink")にほぼ対応する機能を持つ。歴史的には、[ヴィントン・サーフ](https://ja.wikipedia.org/wiki/ヴィントン・サーフ "wikilink")と[ロバート・カーン](https://ja.wikipedia.org/wiki/ロバート・カーン "wikilink")が1974年に発表した Transmission Control Program の[コネクションレスのデータグラムサービス部分がIPとなった](https://ja.wikipedia.org/wiki/コネクションレス型通信 "wikilink")。一方のコネクション指向の部分は [Transmission Control Protocol](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol "wikilink") (TCP) となった。そのため、インターネット・プロトコル・スイートを[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")と呼ぶことが多い。

IPは、最も基本的な通信単位である[パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")を相手に送信する役割を担う。 パケットは、発信者、受信者（手紙でいう宛て先）などの情報を持つIPヘッダ（最小20[オクテット](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")、最大60オクテット）と、通信内容を格納するペイロードとで構成される。パケットのうちIPが受け持つネットワーク層の部分はデータグラムと呼ばれる。発信者、受信者は、IPアドレスにより特定する。

IPは自己のインタフェース（[ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")や[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")のこと）からパケットを送出するだけであり、相手まで確実にパケットが届くことに責任を持たない（保証しない）。 そのため、不慮の事故でパケットが失われた場合には単に到着しないだけである。確実な送受信を保証する必要がある場合には、IPより上位の[トランスポート層](https://ja.wikipedia.org/wiki/トランスポート層 "wikilink")のプロトコルである[TCPなどを使用する必要がある](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol "wikilink")。

現在主に利用されているのは32ビットのアドレス空間を持つ**[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")**であり、IPアドレスの不足が発生することが予測されることから128ビットのアドレス空間を持つ**[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")**が作られた。

なお、**IPv5**（ST）、**IPv7**（TP/IX）、**IPv8**（PIP）、**IPv9**（TUBA）というプロトコルも存在するが、いずれも実験的なプロトコルであり実用には至っていない。また、IPのバージョン番号は[IETFによる割り振りであり](https://ja.wikipedia.org/wiki/Internet_Engineering_Task_Force "wikilink")、優劣などの他意はない。

## IPの仕組み

IPでは、各々の[LANで通信可能な範囲を](../Page/Local_Area_Network.md "wikilink")[セグメント](https://ja.wikipedia.org/wiki/セグメント "wikilink")と呼び、セグメント内のコンピュータを[ホストと呼ぶ](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")。同じセグメントに属するホスト同士はそのLANで使用されている通信プロトコルを[データリンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")とし、その上のネットワーク層で稼動する。

つまり同じセグメントに属するホスト同士は、IP以前からそうであったように直接通信する。このため、。IPがその存在意義を発揮するのはセグメントの外と通信することが可能であり、そして何も変更せずに（全く同じ機器／ソフトウェア構成で）セグメント内とセグメント外との区別なく通信が可能となることである。そのため、最近はLAN内の通信なのにわざわざIPを使う[イントラネット](https://ja.wikipedia.org/wiki/イントラネット "wikilink")を採用することで、インターネット用のソフトウェア資産やノウハウをそのままLAN内通信に利用することが多くなってきている。

### 同じセグメント内の通信

同じセグメント内のホスト同士の通信では、そのLANで使われているプロトコルを使って通信する。そのためIPの各実装では、そのLANで使われているプロトコルから完全に独立することはできない。

まず、送信先となるIPアドレスを持つホストにデータリンク層のデータとして送信するために必要な情報を収集しなければならない。例えば[イーサネット](https://ja.wikipedia.org/wiki/イーサネット "wikilink")であれば、送信先となるIPアドレスを持つホストのインターフェースが持つ[MACアドレス](https://ja.wikipedia.org/wiki/MACアドレス "wikilink")である。そのために[ブロードキャスト](https://ja.wikipedia.org/wiki/ブロードキャスト "wikilink")によって「このIPアドレスの人は返事して！」とメッセージを送る。そのIPアドレスを持っているホストはそれに対して返答する。その返答の送信元が、送信先IPアドレスを持つホストのMACアドレスである。

一般にブロードキャストは負荷が高くLAN内の通信を阻害するため、こうして得られたMACアドレスは今後同じIPアドレスに送信するときにはブロードキャストせずに再利用できるように、[キャッシュ](https://ja.wikipedia.org/wiki/キャッシュ "wikilink")に控えておく。

IPの実装では、こうしたアドレス解決と実際の送受信部分だけはデータリンク層のプロトコルに依存することになる。しかしこの依存部分は、実際にその*データリンク層のプロトコル* を使うホストでだけ必要になるため、世界中に散らばる各セグメントとの通信の際には問題にならない。異なる*データリンク層のプロトコル* を使うセグメントに分かれたホスト同士の通信の場合は、後述するゲートウェイがこれを解決する。

### 異なるセグメント同士の相互通信

セグメントとセグメントの間、あるいはセグメントとWANの間には[ルーティング](https://ja.wikipedia.org/wiki/ルーティング "wikilink")を行なうための特別なホストであるルータがある。ルータにはあらかじめ、自身が繋がれているそれぞれのセグメントにいるホストのIPアドレスを教えてある。これは[ルーティングテーブル](https://ja.wikipedia.org/wiki/ルーティングテーブル "wikilink")と呼ばれる。ルータは、一方のセグメントのホストから他方のセグメントのホストにパケットが送られようとしていると、一旦後者のホストの代わりにパケットを（前者のLANのプロトコルで）受け取り、ルーティングテーブルを参照してどのセグメントに送ればいいかを選択し、そのパケットを後者のLANのプロトコルで後者のホストに送る。ルータはルーティングテーブルによって、あるIPアドレスに送るにはどのセグメントに送ればよいかを把握している。一部が破壊されても、このルーティングテーブルを書き換えるだけで破壊箇所を迂回することが可能になる。

ルータと似ているが、ルーティングテーブルを持たず、異なるLANのプロトコルを変換して互いに中継する[ブリッジと呼ばれるものがある](https://ja.wikipedia.org/wiki/ブリッジ_\(ネットワーク機器\) "wikilink")。しかしブリッジはIPより下位の層（OSI参照モデルのデータリンク層）の機器であり、IPとは関係なく動作する。

また特に、異なるプロトコルを用いるセグメント同士の間をつなぐルータはゲートウェイ（門）と呼ばれる。本来ゲートウェイはOSI参照モデルのネットワーク層におけるブリッジに相当するルータの基本機能の一部なのだが、セグメントのほとんどがイーサネットになっているため、特にセグメントとWANとの間にあるルータだけがゲートウェイであることが多い。またルータが知らないIPアドレスは（ルーティング処理の一環として）全て[デフォルトゲートウェイ](https://ja.wikipedia.org/wiki/デフォルトゲートウェイ "wikilink")と呼ばれる特別なゲートウェイに送られる。デフォルトゲートウェイは通常WANとの接続部分にあるため、未知のIPアドレスへのパケットは全てWAN側（外の世界）のルータにパケットを送信することになる。そしてWANのルータが送信先となるIPアドレスの存在するセグメントのゲートウェイにパケットを送信し、ゲートウェイが送信先となるIPアドレスを持つホストにパケットを送信することで世界中のホストと通信が行なわれる。

## 機能

Internet Protocol は、ホストのアドレッシングとデータグラム（パケット）の送信元ホストから宛先ホストまでの1つまたは複数のIPネットワークをまたいだルーティングを担当する。このために、ホストの識別と論理的位置サービスの提供という2つの機能を持つアドレッシング体系を定義している。これは、標準データグラムと標準アドレッシング体系を定義することでなされる。

### データグラムの構成

[thumb](https://ja.wikipedia.org/wiki/ファイル:UDP_encapsulation.svg "wikilink") からリンク層プロトコルのフレームまで、アプリケーションのデータをカプセル化する例\]\] データグラムはヘッダとペイロードで構成される。IPヘッダには、送信元IPアドレス、宛先IPアドレス、データグラムのルーティングや転送に必要なメタデータが含まれる。ペイロードは転送すべきデータである。このようにデータ・ペイロードにパケットのヘッダを付与して入れ子状に構成していくことをカプセル化と呼ぶ。

### IPアドレッシングとルーティング

IPの最も複雑な部分が[IPアドレッシングと](../Page/IPアドレス.md "wikilink")[ルーティング](https://ja.wikipedia.org/wiki/ルーティング "wikilink")である。アドレッシングとは、各ホストにIPアドレスを割り当てる方法であり、IP[ホストアドレス](https://ja.wikipedia.org/wiki/ホストアドレス "wikilink")群を分割・グループ化してサブネットワークを形成する方法である。IPルーティングは全てのホストが行うが、最も重要な部分は[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")が担っており、経路を決定するのに [Interior Gateway Protocol](https://ja.wikipedia.org/wiki/Interior_Gateway_Protocol "wikilink") (IGP) または [Exterior Gateway Protocol](https://ja.wikipedia.org/wiki/Exterior_Gateway_Protocol "wikilink") (EGP) を使用する。

## 信頼性

IPの設計原理は、ネットワーク基盤はどのネットワーク要素や伝送媒体をとっても本質的に信頼できないと仮定しており、リンクやノードの可用性の面でも一定でないと仮定している。ネットワークの状態を追跡し維持する集中監視機能や性能測定機能は存在しない。ネットワークを単純化するため、知的な部分は意図的に各データ転送の端点であるノードに担わせ、これを[エンドツーエンド原理](https://ja.wikipedia.org/wiki/エンドツーエンド原理 "wikilink")と呼ぶ。転送経路の途中に位置する[ルーター](https://ja.wikipedia.org/wiki/ルーター "wikilink")は、宛先アドレスのルーティングプレフィックスにマッチする最も近いゲートウェイにパケットを転送するだけである。

このような設計の結果、IPは[ベストエフォート](https://ja.wikipedia.org/wiki/ベストエフォート "wikilink")式配送のみを提供し、「信頼できない」と見なされている。ネットワークアーキテクチャとしては「コネクションレス」プロトコルであり、コネクション指向の転送モードとは対照的である。信頼性がないため、、パケットを消失したり、パケットが複製されたり、パケットの順序が入れ替わって受信されたりする。ルーティングはパケット毎に動的に行われ、ネットワークは以前のパケットが通った経路についても状態情報を保持しない。そのため一部のパケットが他より長い経路を通ることがあり、受信側でパケットを受信する順序がおかしくなる可能性がある。

信頼性のないIPv4で唯一確かなのは、IPパケットのヘッダには誤りがないという点である。ルーティングするノードは、パケットの[チェックサム](https://ja.wikipedia.org/wiki/チェックサム "wikilink")を計算する。もしチェックサムが合わない場合、そのノードはそのパケットを捨てる。そのノードは送信元にも宛先にも捨てたことを通知しないが、[Internet Control Message Protocol](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol "wikilink") (ICMP) でそのような通知をすることも可能である。一方、IPv6ではルーティングの高速化を優先してチェックサム計算をやめた。

[上位層プロトコル](https://ja.wikipedia.org/wiki/上位層プロトコル "wikilink")は、この信頼性問題への対処を担う。例えば、アプリケーションにデータを渡す前にデータをキャッシュして正しい順序に並べ替えたりする。

信頼性問題に加え、動的性質とインターネットおよびその構成要素の多様性に関連し、データ転送経路のうちどれが適当かは全く保証できない。技術的制約の1つとして、リンクごとにデータパケットのサイズ上限が異なる。アプリケーションは適切な伝送特性を使うことを保証しなければならない。この責任の一端は、IPとアプリケーションの中間に位置する上位層プロトコル群にもある。ローカルなリンクにおける [Maximum Transmission Unit](https://ja.wikipedia.org/wiki/Maximum_Transmission_Unit "wikilink") (MTU) のサイズを調べるファシリティがあり、IPv6の場合は宛先までの経路全体を考慮したMTUサイズを調べるファシリティもある。IPv4には元のデータグラムを自動的に[断片化する機能がある](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")。この場合、IPは断片化されたパケット群の到着順序を正しく保つ必要がある\[2\]。

例えば [Transmission Control Protocol](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol "wikilink") (TCP) はセグメントサイズをMTUより小さく調整するプロトコルである。[User Datagram Protocol](../Page/User_Datagram_Protocol.md "wikilink") (UDP) と [Internet Control Message Protocol](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol "wikilink") (ICMP) はMTUサイズを無視するので、必要ならIPが断片化を行う\[3\]。

## バージョンと歴史

1974年5月、[Institute of Electrical and Electronic Engineers](../Page/IEEE.md "wikilink") (IEEE) が "A Protocol for Packet Network Intercommunication" と題した論文を公表した\[4\]。この論文で筆者[ヴィントン・サーフ](https://ja.wikipedia.org/wiki/ヴィントン・サーフ "wikilink")と[ロバート・カーン](https://ja.wikipedia.org/wiki/ロバート・カーン "wikilink")は、ノード間のパケット交換を使ってリソースを共有するインターネットワーキング・プロトコルを記述した。このモデルの中心となる制御コンポーネントが "Transmission Control Program" (TCP) で、コネクション指向のリンクとデータグラムサービスの両方を含んでいた。モノリシックな Transmission Control Program は後にモジュール化され、コネクション指向層の [Transmission Control Protocol](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol "wikilink") とインターネットワーキング（データグラム）層の Internet Protocol に分けられた。このモデルが一般に TCP/IP と呼ばれ、正式には[インターネット・プロトコル・スイート](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")と呼ばれている。

Internet Protocol は[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")を定義する要素の1つである。[インターネット層](https://ja.wikipedia.org/wiki/インターネット層 "wikilink")におけるインターネットワーキング・プロトコルで2012年現在主に使われているのは[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")である。この4という番号はプロトコルのバージョン番号で、全てのIPデータグラムの先頭に書かれている。IPv4は RFC 791 (1981) で記述されている。

IPv4の後継が[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")である。バージョン4からの最大の変更点はアドレッシング体系である。IPv4は[32ビット](https://ja.wikipedia.org/wiki/32ビット "wikilink")のアドレス（約40億、4.3×10<sup>9</sup>）を使っていたが、IPv6では[128ビット](https://ja.wikipedia.org/wiki/128ビット "wikilink")のアドレス（約 3.4×10<sup>38</sup>）を使っている。IPv6の採用はゆっくりとしていたが、2008年6月、[アメリカ合衆国連邦政府](https://ja.wikipedia.org/wiki/アメリカ合衆国連邦政府 "wikilink")がバックボーンレベルのみではあるが全システムでIPv6をサポートしてみせた\[5\]。

IPのバージョン0から3まではIPv4の開発途中のバージョンで、1977年から1979年までに使われた\[6\]。バージョン5は実験的なストリーミング用プロトコル  で使われた。バージョン6から9までは、IPv4の後継として提案された各種プロトコルである。このうちバージョン6とされた SIPP (Simple Internet Protocol Plus) が IPv6 として採用されることになった。7から9は IP/IX (RFC 1475)、PIP (RFC 1621)、TUBA (TCP and UDP with Bigger Addresses, RFC 1347) である。

他にも IPv9 や IPv8 を名乗ったプロトコルが提案されたことがあるが、全く支持されていない\[7\]。

1994年4月1日、[IETFは](https://ja.wikipedia.org/wiki/Internet_Engineering_Task_Force "wikilink")[エイプリルフール](https://ja.wikipedia.org/wiki/エイプリルフール "wikilink")のジョークとしてIPv9を発表したことがある\[8\]。

## 脆弱性

IPは様々な攻撃に対して脆弱である。網羅的な脆弱性アセスメントが対策の提案と共に2008年に公表され\[9\]、その後[IETF内で対策を検討中である](https://ja.wikipedia.org/wiki/Internet_Engineering_Task_Force "wikilink")\[10\]。

## 脚注

## 関連項目

  - [インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")
  - [インターネット標準](https://ja.wikipedia.org/wiki/インターネット標準 "wikilink")
  - [パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")
  - [ATM](https://ja.wikipedia.org/wiki/Asynchronous_Transfer_Mode "wikilink")
  - [IANA](https://ja.wikipedia.org/wiki/Internet_Assigned_Numbers_Authority "wikilink")
  - [IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")
  - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")
  - [IPアドレス](../Page/IPアドレス.md "wikilink")
  - [IPアドレス枯渇問題](../Page/IPアドレス枯渇問題.md "wikilink")
  - [Next Generation Network](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink")
  - [SCTP](https://ja.wikipedia.org/wiki/SCTP "wikilink")
  - [TCP/IP](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")
  - [TCPやUDPにおけるポート番号の一覧](https://ja.wikipedia.org/wiki/TCPやUDPにおけるポート番号の一覧 "wikilink")
  - [TDM](https://ja.wikipedia.org/wiki/時分割多重化 "wikilink")
  - [Transmission Control Protocol](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol "wikilink")

## 外部リンク

  - RFC

<!-- end list -->

  - RFC 791 -
  - RFC 1112 -
  - RFC 1518 -
  - RFC 1519 -
  - RFC 1817 -
  - RFC 2101 -

<!-- end list -->

  - その他

<!-- end list -->

  - [Data Communication Lectures of Manfred Lindner - Part IP Technology Basics](http://www.ict.tuwien.ac.at/lva/384.081/infobase/L30-IP_Technology_Basics_v4-6.pdf)
  - [Data Communication Lectures of Manfred Lindner - Part IP Technology Details](http://www.ict.tuwien.ac.at/lva/384.081/infobase/L31-IP_Technology_Details_v4-7.pdf)
  - [Data Communication Lectures of Manfred Lindner - Part IPv6](http://www.ict.tuwien.ac.at/lva/384.081/infobase/L80-IPv6_v4-6.pdf)
  - [IPv6.com - Knowledge Center for Next Generation Internet IPv6](http://www.ipv6.com)

[Category:Internet_Protocol](https://ja.wikipedia.org/wiki/Category:Internet_Protocol "wikilink") [Category:インターネット層プロトコル](https://ja.wikipedia.org/wiki/Category:インターネット層プロトコル "wikilink") [Category:ネットワーク層プロトコル](https://ja.wikipedia.org/wiki/Category:ネットワーク層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  IPv4 アドレスの枯渇に際して <http://www.wide.ad.jp/News/2011/20110204.html>
2.  Siyan, Karanjit. *Inside TCP/IP*, New Riders Publishing, 1997. ISBN 1-56205-714-6
3.  [Basic Journey of a Packet](http://www.securityfocus.com/infocus/1870)
4.  Vinton G. Cerf, Robert E. Kahn, "A Protocol for Packet Network Intercommunication", IEEE Transactions on Communications, Vol. 22, No. 5, May 1974 pp. 637-648
5.  [CIO council adds to IPv6 transition primer](http://www.gcn.com/print/25_16/41051-1.html), gcn.com
6.  RFC 750: "ASSIGNED INTERNET MESSAGE VERSIONS". Sep 28, 1978
7.  [China disowns IPv9 hype](http://www.theregister.co.uk/2004/07/06/ipv9_hype_dismissed/) Theregister.com
8.  RFC 1606: *A Historical Perspective On The Usage Of IP Version 9*. April 1, 1994.
9.  [Security Assessment of the Internet Protocol (IP)(archived version)](http://web.archive.org/web/20100211145721/http://www.cpni.gov.uk/Docs/InternetProtocol.pdf)
10. [Security Assessment of the Internet Protocol version 4 (IPv4)](http://tools.ietf.org/html/draft-ietf-opsec-ip-security)