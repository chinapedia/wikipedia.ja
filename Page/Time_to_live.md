> この記事は[Time to live](https://ja.wikipedia.org/wiki/Time_to_live)から翻訳されています。


**Time to live** （時に **TTL** と省略される）は、[コンピュータ](../Page/コンピュータ.md "wikilink")と[コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")技術において、1単位のデータ（例えば一つの[パケット](../Page/パケット.md "wikilink")）が破棄される前に経過する可能性がある時間、もしくは繰り返し数すなわち[トランスミッション数の上限](../Page/伝送.md "wikilink")（余命）である。

## IPパケットのTime to live

[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")では、time to live (TTL) は、[インターネットプロトコル](https://ja.wikipedia.org/wiki/インターネットプロトコル "wikilink") (IP) ヘッダ内の8ビットフィールドである。それは、20[オクテット中の](../Page/8ビット.md "wikilink")9番目のオクテットである。Time to live の値は、IP[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")がインターネットシステムの中に存在することができる時間の上限として考えることができる。TTLフィールドはデータグラムの送り主が設定し、目的地までのルートの全ての[ホストによって減らされる](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")。データグラムがその目的地に到着する前にTTLフィールドがゼロになったならば、データグラムは破棄され、[ICMPエラーデータグラム](../Page/Internet_Control_Message_Protocol.md "wikilink") ([11 - Time Exceeded](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol#Time_Exceeded_Message（時間切れ通知） "wikilink")) が送り主に返される。TTLフィールドの目的は、配達不能のデータグラムがインターネットシステムを循環し続ける状況と最終的にはそのような不滅のデータグラムによるシステムの輻輳を回避することである。理論的には、time to live は秒で測られるが、データグラムが通過する全てのホストは少なくとも1単位だけTTLを減らさなければならない。実際には、TTLフィールドは、全てのごとに1だけ減らされる。このやり方を反映するために、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では、このフィールドは **hop limit** と呼ばれている。

Unixの[traceroute](https://ja.wikipedia.org/wiki/traceroute "wikilink")コマンド（Windowsの*tracert*）は、TTLフィールドの機能を利用する。

  - TTLのいくつかのデフォルト値
      - 0は同じホストに制限される
      - 1は同じサブネットに制限される
      - 32は同じサイトに制限される
      - 64は同じ地域に制限される
      - 128は同じ大陸に制限される
      - 255は無制限である

## DNSレコードのTime to live

[Domain Name System](../Page/Domain_Name_System.md "wikilink") (DNS) にもTTLの概念があり、DNSでは、Authoritative [name server](https://ja.wikipedia.org/wiki/ネームサーバ "wikilink") が特定のリソースレコードに対してTTLを設定する。（再帰的な）キャッシングネームサーバが Authoritative name server にリソースレコードについて問い合わせたとき、（再帰的な）キャッシングネームサーバはTTLによって指定される時間（秒単位で）の間その記録をキャッシュする。TTLが期限切れになる前に stub resolver が同じレコードをキャッシングネームサーバに問い合わせるならば、キャッシングサーバは再びそれを Authoritative name server に問い合わせるのではなく、単にすでにキャッシュされたリソースレコードを返す。ネームサーバは、[NXDOMAIN](https://ja.wikipedia.org/wiki/NXDOMAIN "wikilink")（ドメインが存在しないという確認応答）用に設定されたTTLを持っている場合がある。しかし、NXDOMAINのTTLは通常、持続時間が短い（最大でも3時間）。

短いTTLは Authoritative name server に重い負荷を引き起こすことがあるが、ウェブサーバあるいは[MXレコード](https://ja.wikipedia.org/wiki/MXレコード "wikilink")のような重要なサービスのアドレスを変更するときに役に立つ場合がある。したがってDNS管理者は、サービスを変更する前にしばしばTTLを低く設定し、中断を最小限にする。

使用される単位は、秒である。DNSのための共通のTTL値は86400秒であり、これは24時間である。86400というTTL値は、DNSレコードが変更されると、世界中のDNSサーバが、変更後最高24時間キャッシュから古い値を表示し続ける場合があることを意味する。

## 参照

  - [ping](https://ja.wikipedia.org/wiki/ping "wikilink")

  - [traceroute](https://ja.wikipedia.org/wiki/traceroute "wikilink")

  -
## 外部リンク

  - [Gnutella TTL and Hops header values used for preventing loops and monitoring of network topology](http://rfc-gnutella.sourceforge.net/developer/testing/messageArchitecture.html)
  - [TTL Interactive Tutorial](http://www.osischool.com/tools/ping/TTL/index.php)

### TTLの初期値のリスト

  - ~~<http://members.cox.net/~ndav1/self_published/TTL_values.html>~~
  - ~~<http://secfr.nerim.net/docs/fingerprint/en/ttl_default.html>~~

上記のページは、2011年5月現在、無効。

[Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink")