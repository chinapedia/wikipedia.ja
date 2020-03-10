> この記事は[Transport Layer Interface](https://ja.wikipedia.org/wiki/Transport_Layer_Interface)から翻訳されています。


**Transport Layer Interface** (TLI、トランスポート層インタフェース)とは、1987年に[AT\&T](../Page/AT&T.md "wikilink")の [UNIX System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") Release 3.0 で提供されたネットワーク用[APIであり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")\[1\]、Release 4 (SVR4) でもサポートが継続された\[2\]。

## 概要

[BSD](../Page/BSD.md "wikilink")の[ソケットに対抗した](../Page/ソケット_\(BSD\).md "wikilink") System V のAPIである。TLI は後に [The Open Group](../Page/The_Open_Group.md "wikilink") が **XTI** ([X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink") Transport Interface) として標準化した\[3\]。実装は下位に位置するキャラクタ型入出力機構である[STREAMS](../Page/STREAMS.md "wikilink")と密接に関連している。

当時、[OSIプロトコルが](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink") TCP/IP に取って代わると予測されていたため、TLI は [OSI参照モデル](../Page/OSI参照モデル.md "wikilink")に準拠したプロトコルから独立した仕様になっており、OSI の[トランスポート層](https://ja.wikipedia.org/wiki/トランスポート層 "wikilink")に対応している\[4\]。XTI/TLIを使ったプログラムは、[Transmission Control Protocol](../Page/Transmission_Control_Protocol.md "wikilink") (TCP)、 (XNS)、[Systems Network Architecture](https://ja.wikipedia.org/wiki/Systems_Network_Architecture "wikilink") (SNA)、[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")、[Asynchronous Transfer Mode](../Page/Asynchronous_Transfer_Mode.md "wikilink") (ATM) など[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の第4層の機能を提供する様々なトランスポート層プロバイダ上で動作可能である\[5\]。

APIとしては[ソケットと同様の機能を提供しているが](../Page/ソケット_\(BSD\).md "wikilink")、ソケットが[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")と密接に関連しているのに対し、XTI/TLIはプロトコルから独立している\[6\]。XTIは、連携する[STREAMS](../Page/STREAMS.md "wikilink")モジュール、ライブラリ[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、ヘッダファイル群、XTIプロセスの動作に関する規則や制限で構成されている\[7\]。

TLIとXTIは UNIX 98 まではPOSIXソケットAPIよりも好まれ、広く使われていた\[8\]。TLIとXTIは、[Solaris](../Page/Solaris.md "wikilink")などSVR4から派生した[OSや](../Page/オペレーティングシステム.md "wikilink")[UNIX](../Page/UNIX.md "wikilink")ブランド (UNIX 95, UNIX 98, UNIX03 [Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink")) 準拠のOSでは今もサポートされている。また、[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink") でも [Open Transport](../Page/Open_Transport.md "wikilink") という名称で使われた。UNIX 95 (XPG4) と UNIX 98 (XPG5.2) ではXTIがサポート推奨APIとなっていた\[9\]\[10\]。その後 [Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") において[STREAMS](../Page/STREAMS.md "wikilink")を実装していない[BSD](../Page/BSD.md "wikilink")や[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")を考慮すべきだという議論が起き、UNIX 03 では[STREAMS](../Page/STREAMS.md "wikilink")とXTIをオプションとし、POSIXソケットをサポート推奨APIとした。

## プロトコル独立性

XTI/TLIはプロトコルから独立している。しかし、どのプロトコルを使うかを指定する必要があるため、結局アプリケーションは使用するプロトコルについて知っている必要がある\[11\]。使用するプロトコルに関する知識もアプリケーションから排除するには、Network Selection Facilities を使用する。これはXTI/TLIライブラリ (libnsl) の一部となっている\[12\]。

## XTI/TLI とソケットの比較

XTI/TLIとBSDソケットは似ているが、完全に同じというわけではなく、同じ役割の関数が異なる振る舞いをすることも多い。UNIX SVR3\[13\] と SVR4\[14\] ではTLIとソケットが[STREAMS](../Page/STREAMS.md "wikilink")の Transport Service Interface の上に実装されている。

下記の表はPOSIXでのXTIとソケットのインタフェースを比較したものである。

| XTI/TLI インタフェース                 | ソケットインタフェース                          | 意味論的に同一か                                                                                                                            |
| ------------------------------- | ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| t_open                         | socket                               | イエス。ただし t_open はオープン時に t_getinfo を実行可能                                                                                            |
| \-                              | socketpair                           | \-                                                                                                                                  |
| t_getinfo                      | \-                                   | \-                                                                                                                                  |
| t_getprotaddr                  | getsockname, getpeername             | イエス。しかし t_getprotaddr は対応する2つの機能を1つで実行可能                                                                                           |
| t_bind                         | bind, listen                         | イエス。ただし t_bind は対応する2つの機能を1回のコールで実施可能                                                                                              |
| t_optmgmt                      | getsockopt, setsockopt               | イエス。ただし t_optmgmt はデフォルト値と調停値を取得できるのに対し、getsockopt と setsockopt は現在値しか取得/更新できない。                                                   |
| t_unbind                       | bind                                 | イエス。ソケットの場合 AF_UNSPEC を指定することで unbind 相当になる。                                                                                       |
| t_close                        | close                                | イエス。ただし、t_close では常にアボート的切断になるのに対し、close は終了を待ち合わせて解放することもある。                                                                      |
| t_getstate                     | \-                                   | \-                                                                                                                                  |
| t_sync                         | \-                                   | \-                                                                                                                                  |
| t_alloc                        | \-                                   | \-                                                                                                                                  |
| t_free                         | \-                                   | \-                                                                                                                                  |
| t_look                         | select, getsockopt                   | select と getsockopt(SO_ERROR) は t_lock の全機能をカバーしていない。                                                                             |
| t_error                        | perror                               | イエス。ただし XTI は通常のerrnoに追加的に t_errno を使用し、トランスポート層のエラーだけでなくUNIXシステムのエラーも示すことができる。                                                    |
| t_strerror                     | strerror                             | イエス                                                                                                                                 |
| t_connect                      | connect                              | t_connect の前に t_bind が必須である。                                                                                                      |
| t_rcvconnect                   | select                               | t_rcvconnect は、select で O_NONBLOCK を指定した場合と同等である。                                                                                 |
| t_listen, t_accept, t_snddis | accept                               | accept は接続を拒否できないが、t_listen で受け付けた接続要求はその後の t_accept で初めて許可され、t_snddis を使えば拒否できる。                                                |
| t_snd, t_sndv                 | send, sendto, sendmsg                | イエス。しかし t_snd と t_sndv はコネクションモードのトランスポートでのみ使用。                                                                                   |
| t_rcv, t_rcvv                 | recv, recvfrom, recvmsg              | イエス。ただし t_rcv と t_rcvv はコネクションモードのトランスポートでのみ使用。                                                                                   |
| t_snddis                       | close, shutdown                      | t_snddis を発行後も接続要求を listen し続けることができ、t_connect で接続を再確立することもできる。close はソケットのファイル記述子を解放してしまう。通信を続ける場合、ソケットでは新たに接続を確立する準備をしなければならない。 |
| t_rcvdis                       | ENOTCONN, ECONNRESET, EPIPE, SIGPIPE | イエス。ただし、ソケットではエラーまたはシグナルで通知。                                                                                                        |
| t_sndrel, t_sndreldata        | shutdown                             | イエス。しかし shutdown には通常解放時にデータを送信する機能はなく、t_sndreldata は通常解放時にデータを送信できる。t_sndrel は単にシャットダウンだけを行う。                                    |
| t_rcvrel, t_rcvreldata        | \-                                   | \-                                                                                                                                  |
| t_sndudata, t_sndvudata       | sendmsg                              | イエス。しかし t_sndudata と t_sndvudata は[コネクションレス](https://ja.wikipedia.org/wiki/コネクションレス型通信 "wikilink")・モードでのみ使用。                      |
| t_rcvudata, t_rcvvudata       | recvmsg                              | イエス。しかし t_rcvudata と t_rcvvudata はコネクションレス・モードでのみ使用。                                                                              |
| t_rcvuderr                     | \-                                   | \-                                                                                                                                  |
| read, write                     | read, write                          | XTI/TLI では read/write を使用する前に tirdwr モジュールをSTREAMSにプッシュする必要がある。                                                                     |

ライブラリ関数には呼び出し順序の規定があるため、XTI/TLIは状態インジケータを使用しており、ソケットAPIにも同様の仕組みがある。ただし、ソケットのAPI関数は複数の状態で呼び出せることがあるのに対し、XTIのAPI関数は特定の状態でないと呼び出せないようになっている。

## XTI/TLI 非同期モード

XTI/TLIには非同期モードがあり、リアルタイム性が要求されるアプリケーションで利用できる。非同期モードでない場合、データを待ち続けてずっとブロックされる可能性がある。初期化の際に O_NONBLOCK というパラメータを指定すると非同期モードになる。その場合、接続要求、新規データ到着、タイムアウトなどのイベントを非同期にアプリケーションに通知する。

## XTIでの改良点

XTIでTLIから改良した点として、エラーメッセージの追加、フロー制御のためのイベント追加、パラメータ指定の簡素化（オープンの際はデフォルトでリード・ライトとなるなど）がある。また、t_listen でずっとブロックしてしまうのを防ぐため qlen の値をチェックするようになった。さらに *t_strerror()* と *t_getprotaddr()* というインタフェースが追加された。

## 実装

XTI/TLIは [UNIX System V](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") で実装されているが、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")向けの OpenSS7 などの実装例もある。

## 脚注

## 参考文献

  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
## 関連項目

  - [X/Open Protability Guide](https://ja.wikipedia.org/wiki/X/Open "wikilink") (XPG) - [POSIX](../Page/POSIX.md "wikilink")の前身
  - [コンピュータネットワーク](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")

## 外部リンク

  - [The Open Group's XTI standard](http://www.opengroup.org/bookstore/catalog/c523.htm)
  - [Networking Services (XNS) Issue 5.2, The Open Group, January 2000](http://www.opengroup.org/bookstore/catalog/c438.htm)
  - [Example client-server application working on Solaris and Linux](http://gim.org.pl/uczelnia/PSI/7.XTI_TLI/)

[Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11. [Introduction to Networking Technologies](http://www.redbooks.ibm.com/abstracts/GG244338.html?Open) IBM redbooks
12.
13.
14.