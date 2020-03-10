> この記事は[SYN cookies](https://ja.wikipedia.org/wiki/SYN_cookies)から翻訳されています。


**SYN cookies (スィン・クッキーズ)** とは、TCP [SYN flood攻撃を防ぐために開発された手法のひとつ](../Page/SYN_flood.md "wikilink")。1996年、[ダニエル・J・バーンスタインらにより考案された](../Page/ダニエル・バーンスタイン.md "wikilink")。

## 原理

SYN flood 攻撃の問題点は、[TCP](../Page/Transmission_Control_Protocol.md "wikilink") 接続が開始する前から[サーバ](../Page/サーバ.md "wikilink")が[クライアントの](../Page/クライアント_\(コンピュータ\).md "wikilink") [SYN](https://ja.wikipedia.org/wiki/SYN "wikilink") パケットによって記憶領域を消費してしまう点にあった。通常この記憶領域には、クライアント側の[IPアドレス](../Page/IPアドレス.md "wikilink")と[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")、接続に使うシーケンス番号、およびクライアントが指定してきた TCP接続に関する様々な設定 ([TCPウィンドウ](https://ja.wikipedia.org/wiki/TCPウィンドウ "wikilink")の大きさなど) が格納される。また、サーバは SYN パケットを受けとった後、クライアントに対して SYN ACK パケットを返す。ここにはその TCP 接続に関連づけられた[TCPシーケンス番号](https://ja.wikipedia.org/wiki/TCPシーケンス番号 "wikilink")が含まれている。TCPシーケンス番号はこれ以降の TCP通信の中で、クライアントおよびサーバが共通して使用する。そのためクライアントはサーバが返した SYN ACK パケットにあるシーケンス番号を ACK パケットの中に含めてくるはずである。この性質を利用して、もしサーバが本来メモリ上に記憶するべき情報を返りの SYN ACK パケットの中のシーケンス番号の中に埋めこむことができれば、サーバ側は SYN を受けとった直後に記憶領域を消費する必要はなくなり、ACK パケットが来てからはじめて TCP 接続用の領域を割り当てればよくなる。大量の SYN flood を行うほとんどの攻撃元ホストは IP アドレスを偽装しているため、このシーケンス番号を受けとることはできず、したがってサーバに正しい ACK パケットを送ることができない。その結果、サーバは正当なホストからの接続要求のみに対応 (メモリ割り当て) することができる。このアイデアを進めたものが SYN cookies である。

## 実装手法

SYN cookies を使ったサーバは、通常の (SYN flood 攻撃を受けていない) 状態では他のサーバと同じようにふるまい、SYN パケットがひとつくるごとに記憶領域を割り当てる。しかし他のサーバは SYN flood 状態 (割り当てるべき領域が不足した状態) になるとクライアントからの SYN パケットを捨ててしまうのに対して、SYN cookies を使ったサーバは SYN flood 状態になると **記憶領域を割り当てずに** SYN ACK パケットを返す。このとき SYN ACK に含まれる TCP シーケンス番号は以下のような特別な方法で計算される:

  - 最初の5ビット: *t* mod 32 の値 (*t* は 現在までの経過時間を表すカウンタで、64秒ごとに増加する)。
  - 次の 3ビット: その TCP 接続に利用する MSS ([Maximum Segment Size](https://ja.wikipedia.org/wiki/Maximum_Segment_Size "wikilink")) 値をエンコードしたもの。あらかじめサーバで取り決めておいた 8種類の値からクライアントの要求にもっとも近いものを使用する。
  - 次の 24ビット: クライアント・サーバの各IPアドレスと TCPポート番号、および *t* の値をサーバ側の[一方向ハッシュ関数で](../Page/一方向性関数.md "wikilink")[ハッシュ化](https://ja.wikipedia.org/wiki/ハッシュ化 "wikilink")したもの。このサーバ側の関数はクライアントからは知ることができない。

この方法で計算されたシーケンス番号は、サーバ側の *t* を含んだ一方向ハッシュ関数で計算された値を含んでいるため、クライアントが勝手に偽装することはできない (クライアントはハッシュを計算するための秘密の初期値を探索せねばならず、しかもこの値は時間によって変化するので値を大量に収集し記憶しても約 1分後には使えなくなってしまう)。また、この番号は TCP の MSS値に関する情報を含んでいるので、クライアントが正しく ACKパケットを返してきた際には、サーバはたとえ元のクライアントの MSS 要求値を覚えていなくても、それに近い値を利用することができる (ただし、MSS 以外の TCP 関連のオプションはすべて無視されてしまう)。さらに、ここで *t* は 64秒間のあいだ不変であるので、t の変わらない間に返されてきた ACK パケットのシーケンス番号であれば、(クライアントとサーバが同じ *t* を共有しているため) サーバはシーケンス番号を正しくチェックできる。こうしてサーバが記憶領域を割り当てなくても、安全な TCP 接続が可能になる。

## 問題点

SYN cookies の問題点として、以下のようなものが指摘されている:

1.  クライアントが指定してきた MSS の値を正しく記憶できない (近似値のみ)。
2.  クライアントが指定してきた TCP オプションをすべて無視せざるを得ないこと。
3.  一方向ハッシュ関数は計算に時間がかかるため、サーバ側の負荷が増大すること。
4.  サーバ側に状態を保持しないため、サーバ側が先に反応を返すプロトコルにおいては、クライアント側がハングする可能性があること。

1\. および 2. の問題による弊害は、通信の性能が低下することである。しかし SYN flood 攻撃を受けている場合は多少の速度を犠牲にしても、正当なクライアントが正しくサーバに接続できるようにすることのほうが重要であるため、性能の低下はさほど問題とはならないことが多い。だが通常の状態ではこのようなふるまいは望ましいとはいえないので、SYN cookies が使われるのは SYN flood 攻撃が起きているときのみである。3. については、最近ではコンピュータの処理速度が上がっているためにほとんど問題とはならないことが多い。 4. は、[SMTPや](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[SSHのように](../Page/Secure_Shell.md "wikilink")、コネクション確立後、サーバ側が先に反応を返すプロトコルで問題となる。SYN cookies ではコネクションを確立するまでサーバ側では状態を保持しない。このためTCP [3ウェイ・ハンドシェイク](https://ja.wikipedia.org/wiki/3ウェイ・ハンドシェイク "wikilink")の3番目のパケットが失われた場合、本来であればサーバ側が行なうべきSYN-ACKパケットの再送が起きず、クライアント側に接続状態のコネクションが残ったままとなる。対話的な利用ばかりではなく計算機間の通信に使われる SMTP のようなプロトコルの場合、これは計算機資源のリークという結果を招く可能性があるので、SYN cookies の利用は危険である。

## 実装

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")上の TCPスタックでは、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")2月から エリック・シェンク (Eric Schenk) による SYN cookies の機能が実装されている。ほとんどの Linux ディストリビューションではこの機能はデフォルト状態で有効になっている。`/proc/sys/net/ipv4/tcp_syncookies` の値を 1 にすることで SYN flood時に SYN cookies が有効になる。

## 外部リンク

  - [ダニエル・J・バーンスタインによる SYN cookies の解説](http://cr.yp.to/syncookies.html)
  - [Bill Sommerfeld による問題点の指摘](http://mail-index.netbsd.org/tech-kern/2001/04/18/0006.html)

[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:Transmission_Control_Protocol](https://ja.wikipedia.org/wiki/Category:Transmission_Control_Protocol "wikilink")