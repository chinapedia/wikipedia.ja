> この記事は[SYN flood](https://ja.wikipedia.org/wiki/SYN_flood)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Tcp_normal.svg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Tcp_synflood.png "wikilink")

**SYN flood攻撃** (スィン・フラッドこうげき) とは、[インターネット](../Page/インターネット.md "wikilink")における[DoS攻撃](../Page/DoS攻撃.md "wikilink")（サービス拒否攻撃）のひとつ。インターネット上に公開されている[ウェブサーバなどの負荷を増大させ](../Page/Webサーバ.md "wikilink")、対象となるサイトを一時的に利用不能に陥らせてしまう効果がある。

## 原理

一般に、インターネット上の [TCP接続は次のような手順で行われる](../Page/Transmission_Control_Protocol.md "wikilink") ([3ウェイ・ハンドシェイク](../Page/3ウェイ・ハンドシェイク.md "wikilink")):

1.  [クライアントが](../Page/クライアント_\(コンピュータ\).md "wikilink")、[サーバ](../Page/サーバ.md "wikilink")に対して TCP [SYN](https://ja.wikipedia.org/wiki/SYN "wikilink") パケットを送信する。
2.  SYN パケットを受けとったサーバは、そのクライアントの接続を許可する SYN ACK パケットを送信する。同時にサーバは接続を準備するために、そのクライアントとのTCP接続用の情報を記憶する領域を割り当てる。
3.  SYN ACK パケットを受けとったクライアントは、接続開始をあらわす [ACK](https://ja.wikipedia.org/wiki/ACK "wikilink")パケットを送信し、サーバとの通信を開始する。

SYN flood 攻撃は、クライアント側がこの 3. の操作を意図的に行わないようにして、サーバを「中途半端な」状態にすることである。SYN flood攻撃をおこなう (悪意ある) クライアントは、サーバに大量の SYN パケットを送ったあと、サーバから返された SYN ACK パケットを無視して、そのまま放置する。サーバ側からすれば、クライアントから ACK パケットが届かないということは、ネットワークに障害が発生しているか、あるいは通信速度が非常に遅いかのどちらかである。このような場合、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink") ではサーバはクライアントからの ACK パケットを一定時間 (数十秒) のあいだ待たなければならないと決められている。しかし、サーバは待っている間もクライアントの情報を保持しつづけなければならないので、SYN パケットをひとつ受けとるたびに使用するメモリ領域は増大する。この現象がきわめて短時間のうちに大量に発生すると、サーバは TCP接続のために使えるメモリをすべて使いはたしてしまい、新たな TCP接続がひとつも準備できなくなってしまう。このときサーバはいわゆる[ライブロック状態に陥っており](https://ja.wikipedia.org/wiki/排他制御#留意すべき現象と性質 "wikilink")、継続して動作はしているものの、他のクライアントから TCP接続要求を送っても反応しないため、完全にダウンしてしまったように見える。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")によっては、最悪の場合システムが[クラッシュしてしまうこともある](https://ja.wikipedia.org/wiki/クラッシュ_\(コンピュータ\) "wikilink")。

### サーバへの負荷

SYN flood 攻撃はサーバ上のメモリをどれくらい消費するのだろうか。サーバが帯域 1Gbps の[イーサネット](../Page/イーサネット.md "wikilink")でインターネットと接続されていると仮定すると、外部から送られてくるデータ量は最大約 100メガバイト/秒である。通常の TCP SYN パケットの大きさは 60バイトであるので、1秒間に外部から送信されうる TCP SYN パケットは最大約 200万個になる。SYN flood攻撃では、これらの接続元アドレスは通常すべて異なるアドレスに偽装されているので、サーバは SYN パケットがひとつくるごとに最低でも 16バイトの情報を必要とする。したがって 1Gbps の帯域をフル活用した SYN flood 攻撃がおこなわれた場合、1秒間にサーバが消費するメモリは約 30メガバイトである。さらにサーバは各 SYN パケットを最大 30秒間にわたって保持しなければならない。すると、サーバが持たねばならない合計記憶容量は 900メガバイトになる。SYN flood 攻撃が継続して行われている間は 30秒ごとにこれらの記憶領域がほぼ全面的に書き換えられるうえ、サーバは新しいパケットがくるたびにそれがこれらの情報と一致しているかどうか照合しなければならない。このための処理能力やメモリアクセス速度は現在のほとんどの PC の能力を超えており、このような大規模な SYN flood 攻撃を通常の方法で[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")するためには高い能力と[TCAM](https://ja.wikipedia.org/wiki/TCAM "wikilink")などの専用メモリをもった非常に高価な[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")が必要である。

## 対策

SYN flood 攻撃は、[1996年](../Page/1996年.md "wikilink")に米国の大手[プロバイダ](https://ja.wikipedia.org/wiki/プロバイダ "wikilink") Panix のメールサーバがこの攻撃によってダウンしてからよく知られるようになった。当初、この攻撃に対する効果的な防御は存在しないと考えられていた。理由としては攻撃者は TCP SYN パケットの IPアドレスを偽装することができたためである。サーバから見ると、これは単にランダムな IPアドレスから大量の接続要求が来ているだけで、そのうちのどれが本当に応答すべきでないパケットなのか判断することはできない。しかしその後 [SYN cookies](../Page/SYN_cookies.md "wikilink") や [SYN cache](https://ja.wikipedia.org/wiki/SYN_cache "wikilink") といった手法が考案され、SYN flood 時でも正当なクライアントからの接続をある程度処理できるようになった。また、最近はプロバイダによる[Ingress フィルタリングも普及してきたため](https://ja.wikipedia.org/wiki/Ingress_フィルタリング "wikilink")、偽装されたパケットによる攻撃は難しくなっている。

## この攻撃法による被害

2007年2月20日〜22日までに、この攻撃法によって、[ニコニコ動画](../Page/ニコニコ動画.md "wikilink")のWebサーバ、メッセージサーバなどが攻撃され、23日11:20分よりサービスが停止される被害に遭った。 始めは、30台程度による小規模な攻撃であったが、その後増大。 結果、3000台以上による攻撃となり、サービスを停止した。

## 関連項目

  - [肯定応答](https://ja.wikipedia.org/wiki/肯定応答 "wikilink") (ACK)
  - [3ウェイ・ハンドシェイク](../Page/3ウェイ・ハンドシェイク.md "wikilink")
  - [ウィンドウサイズ](https://ja.wikipedia.org/wiki/ウィンドウサイズ "wikilink") - [スライディングウィンドウ](https://ja.wikipedia.org/wiki/スライディングウィンドウ "wikilink") - [フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")

## 外部リンク

  - [SYN flood攻撃に関する当時の CERT アドバイザリ](http://www.cert.org/advisories/CA-1996-21.html)

[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:DoS攻撃](https://ja.wikipedia.org/wiki/Category:DoS攻撃 "wikilink") [Category:Transmission_Control_Protocol](https://ja.wikipedia.org/wiki/Category:Transmission_Control_Protocol "wikilink")