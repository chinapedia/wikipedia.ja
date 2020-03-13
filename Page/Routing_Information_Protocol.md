> この記事は[Routing Information Protocol](https://ja.wikipedia.org/wiki/Routing_Information_Protocol)から翻訳されています。


*' Routing Information Protocol*' (ルーティング・インフォメーション・プロトコル、略称：**RIP**) とは[UDP](../Page/User_Datagram_Protocol.md "wikilink")/[IP上で動作する](../Page/Internet_Protocol.md "wikilink")[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")である。

## 概要

[自律システム](../Page/自律システム_\(インターネット\).md "wikilink") (AS) 内の[ルーティング](../Page/ルーティング.md "wikilink")を行う[Interior Gateway Protocol](../Page/Interior_Gateway_Protocol.md "wikilink")（IGP）の[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。 また、[距離ベクトル型](https://ja.wikipedia.org/wiki/ルーティング#DVA "wikilink")（DVA）の[ルーティング](../Page/ルーティング.md "wikilink")を行う[距離ベクトル型ルーティングプロトコル](https://ja.wikipedia.org/wiki/距離ベクトル型ルーティングプロトコル "wikilink")（ディスタンスベクタルーティング）である。

RIPは、経由する可能性のある[ルータを](../Page/ルーター.md "wikilink")**[ホップ数](https://ja.wikipedia.org/wiki/ホップ数 "wikilink")**という値で数値化し、 (Distance Vector Algorithm)という[アルゴリズム](../Page/アルゴリズム.md "wikilink")で隣接[ホストとの経路を動的に交換する事で](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")、パケットが目的の[ネットワークアドレス](https://ja.wikipedia.org/wiki/ネットワークアドレス "wikilink")にたどり着くまでの最短経路を決定する。 また、有効経路を2つまで採用し、固定メトリック値を与えることで、同一ホップ数の経路がある場合に優先する経路を制御することが可能である。

目的ネットワークアドレス、次のホップ先IPアドレス、目的ネットワークまでのホップ数などの情報は、ルーター内のルーティング・データベースに記録され、ルータ間で定期的に情報交換が行われる。 その中から有効な経路を抽出したテーブルが[ルーティング・テーブルと呼ばれている](../Page/ルーティングテーブル.md "wikilink")。

ネットワーク全体の[ネットワーク・トポロジー](../Page/ネットワーク・トポロジー.md "wikilink")を考慮する必要がないため、計算負荷が非常に低いメリットがある。 しかし、ネットワーク全体の経路が完全に収束するまでの時間が長いデメリットがある。 また、さらに重大なデメリットとして、リンクダウンが起きると、そのリンクと関係した経路のメトリックが無限大に発散するCount-to-Infinity問題が起きる可能性があり、実際に起きた場合には、無駄な経路情報が流れ続ける状態に陥ってしまう。 ([RFC2453(RIP Version 2)](https://tools.ietf.org/html/rfc2453)のPage14-Page15でも言及されている) 一旦、1箇所でもこの問題が起きれば、その周辺のルータの経路表の特定の送信先に関する経路のメトリックも無制限に増加して行く。

1990年代半ばまでは計算機の能力に余裕がなく、[OSPF対応ルータは高価であり](../Page/Open_Shortest_Path_First.md "wikilink")、上記の問題への対応よりも計算負荷の低さのメリットが優先されたためにRIPの運用が広く行われていた。

2000年以降の計算機の性能向上により、上記の問題を全て解決したリンクステート型の[OSPFで用いるダイクストラ法の計算負荷は大きな問題ではなくなった](../Page/Open_Shortest_Path_First.md "wikilink")。 現在は[RIP](https://ja.wikipedia.org/wiki/RIP "wikilink")専用ルータから[OSPF対応ルータへと置き換えが進んだことで](../Page/Open_Shortest_Path_First.md "wikilink")、[RIP](https://ja.wikipedia.org/wiki/RIP "wikilink")は利用可能な計算資源が非常に少ない場合を除いて全く使用されなくなった。

### ホップ数と固定メトリック

RIPv1が実装されているホストは、基本的に自己に接続されるネットワークについて、同一ネットワーク内に存在する他のホストに対して[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")する。RIPv2では、送信先IPアドレス224.0.0.9に向かって[マルチキャスト](../Page/マルチキャスト.md "wikilink")で送信する。オリジナルの経路情報(ホップ0)を他のホストで受信した場合、これに経路ホップ数を1追加していく。このホップ数が16以上になると、無限遠として扱われ、有効経路として採用されなくなる。

### メリット

  - 経路計算アルゴリズムが極めて簡素であるため、ルータにかかる負荷が少ない。そのため、計算性能の低いルータにも実装が可能である。
  - 使い方が容易で、少しのコマンドを覚えるだけで簡単に設定が行える。

### デメリット

  - 前述の通り、ホップ数15の経路は有効経路として採用されないため、ルータを複数個使用するような大規模ネットワークには不向きであると言われる。(しかし、日本から米国Yahoo\!までであってもホップ数は13ホップ程度である。大きな半径を持つリング状トポロジのような、特殊なネットワークを作らない限り、単一組織内であれば全く問題ではないといえる。)
  - 他のルータと情報交換を行う際、ブロードキャストを用いて[ルーティングテーブル](../Page/ルーティングテーブル.md "wikilink")を転送するため、トラフィックを圧迫しやすい。
  - ホップ数が同じルートが複数該当する場合、ルータは[ラウンドロビン方式](https://ja.wikipedia.org/wiki/ラウンドロビン方式 "wikilink")で交互にパケットの転送を行うが、片方のルートがもう一方に比べて著しく[帯域幅](../Page/帯域幅.md "wikilink")が狭い場合、[輻輳](../Page/輻輳.md "wikilink")が発生する恐れがある。
  - バージョン1では[サブネットマスク](../Page/サブネットマスク.md "wikilink")をルート情報に含めることができない([クラスフルなルーティングプロトコル](https://ja.wikipedia.org/wiki/IPアドレス#アドレスクラス "wikilink"))ため、VLSM・[CIDRをサポートしない](https://ja.wikipedia.org/wiki/Classless_Inter-Domain_Routing "wikilink")。このため、正しくネットワーク・IPアドレス空間の設計を行わないと、他のネットワークに分断されたり(不連続ネットワーク)、サブネットマスクが異なるネットワークへのパケット転送ができない。この問題はバージョン2では解消されている。

## バージョンと互換性

2007年現在、主に使われているのはRIP Version 2である。小さなネットワークで使用する前提で、簡易的に経路制御プロトコルを実装しているルーターなどは、いまだにRIP Version 1が多い。バージョン互換性が高く、[ベンダ独自の仕様も少ないが](https://ja.wikipedia.org/wiki/ベンダー "wikilink")、RIP Version 2を用いて構築されたネットワークで詳細なオプションが指定されている場合は、互換性は低いものとなる。

### バージョン

RIP には3つのバージョンがある。RIPv1はRFC 1058で、RIPv2はRFC 2453で、RIPngはRFC 2080で定義される。

### バージョン2で追加された機能

  - Multicast アドレスによるRIPパケット送出 - この場合に利用されるMulticast アドレスは、**224.0.0.9**である。
  - PlainTextによる認証機能(追ってRFC 2082でMD5認証、RFC 4822でSHA-1認証がサポートされた)
  - Netmask([CIDR](https://ja.wikipedia.org/wiki/Classless_Inter-Domain_Routing "wikilink"))のサポート - ゆえに、RIPバージョン2はクラスレスなルーティングプロトコルである。
      - 不連続サブネットにも対応可能
  - Nexthopアドレスのサポート - 特定の送信先への経路のリダイレクトが可能である。

## 関連規約

[IPv4](../Page/IPv4.md "wikilink")向け

  - RFC 1058 - Routing Information Protocol
  - RFC 2453 - RIP Version 2
  - RFC 2082 - RIP-2 MD5 Authentication
  - RFC 4822 - RIPv2 Cryptographic Authentication

[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")向け

  - RFC 2080 - RIPng for IPv6

## 出典・脚注

## 参考文献

  -
[Category:ルーティングプロトコル](https://ja.wikipedia.org/wiki/Category:ルーティングプロトコル "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")