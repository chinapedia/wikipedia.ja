> この記事は[Maximum Transmission Unit](https://ja.wikipedia.org/wiki/Maximum_Transmission_Unit)から翻訳されています。


**Maximum Transmission Unit** (MTU)は、ネットワークにおいて1回の転送（1[フレーム](../Page/パケット.md "wikilink")）で送信できるデータの最大値を示す伝送単位のこと。

MTUの値は利用される通信メディアや[カプセル化の有無などによって変わる](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。たとえば[イーサネット](../Page/イーサネット.md "wikilink")では最大1,500[バイト](../Page/バイト_\(情報\).md "wikilink")（[オクテット](../Page/8ビット.md "wikilink")）が[IP通信に利用できる](../Page/Internet_Protocol.md "wikilink")。[PPPoE](../Page/PPPoE.md "wikilink")を使うとカプセル化のために8バイトを使うため、1,492バイトとなる。[WANではさらに別の制約が入る場合もあり](../Page/Wide_Area_Network.md "wikilink")、たとえば[NTT東日本および](../Page/東日本電信電話.md "wikilink")[NTT西日本が提供する](../Page/西日本電信電話.md "wikilink")[フレッツ](../Page/フレッツ.md "wikilink")シリーズのIP網は1,454バイトとなっている\[1\]。 MTUを超えた場合、断片化（[フラグメンテーション](../Page/フラグメンテーション.md "wikilink")、[IPフラグメンテーション](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")）して通信を行う。

## MTUと通信パフォーマンス

[パケット通信](../Page/パケット通信.md "wikilink")を用いて一定サイズのデータを送受信する場合、パケット長の決定が通信パフォーマンスに影響する。

通信中にデータが破損した場合、検出および再送はパケット単位で行なわれるのが普通である。したがって不安定な伝送路では、小さなパケットに分割して通信する方が、再送の負荷を軽減できる。反面、エラーがほとんど発生しないような伝送路では、パケット長を大きくして少数のパケットにまとめる方が、パケット化のオーバーヘッドを軽減できる。このような理由から、通信メディアは各々の特性に応じてMTUを設定されている。さらに前述のように、カプセル化もMTUを減少させる。

[インターネット](../Page/インターネット.md "wikilink")のようなWAN環境では、パケットが宛先に到着するまでの間に、様々なMTUの伝送路を通る可能性がある。もしフレーム長がMTUを超えていた場合、Internet Protocol（IP）のような上位層は通常、[パケットの断片化・再統合を行う](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")。しかし、このようなパケットの再構成はルーターの処理負荷増加および通信パフォーマンス低下の原因となるため、断片化の起こらないパケット長がわかっている場合は、あらかじめパケット長を制限して送信するという考え方もある。ただし、その値は宛先および経路によって異なるため、あらかじめ静的に設定しておくには、何らかの割り切りが必要になる可能性がある。[IPv4](../Page/IPv4.md "wikilink")で断片化した場合、IPv4のヘッダの「フラグ」にて断片化を管理する。

## 経路MTU探索

IPではRFC 1191で定義される経路MTU探索（Path MTU Discovery）を使うことで、終端まで断片化を行わずに転送できるMTUを動的に検出できる。これは、パケットに断片化禁止のフラグ（Don't Fragment = DFフラグ）を設定しておき、MTUの問題で転送できない経路に到達した際はその旨を[ICMPパケットで送信元に通知して](../Page/Internet_Control_Message_Protocol.md "wikilink")、フレーム長を再調整するという仕組みである。ICMPは、転送できなかったルーターから、送信元ホストへ送信される。

転送できなかったことを通知するICMPパケットは、Type 3（Destination Unreachable Message）のCode 4（fragmentation needed and DF set）である。「Datagram Too Big」などと呼ばれることもある。ただし元々RFC 792の形式では未使用となっていた領域に、RFC 1191では「Next-Hop MTU」を割り当てている。この値は、断片化を必要とした伝送路のMTUなので、送信元が再試行する際に経路MTUの次の候補値として使用できる。もしルータが古い形式にしか対応しておらず、Next-Hop MTUに未使用領域として0を格納している場合、次の候補値を選ぶためには、何らかの推測を行なうことになる。結果として、再試行の回数が増えたり、最適値より小さめのMTUを選択したりする可能性がある。

### 経路MTU探索に関する問題

経路MTU探索は、RFC 1191で定義されたとおりに動作すれば、断片化を必要としない最大のMTUを検出することができる。しかし現実には、設定の問題で正常に機能しない場合が珍しくない。問題がある場合の典型的な挙動は、通信を開始することはできるが、経路MTUより大きなサイズのフレームが現れた時点でタイムアウトするというものである。主な問題と対応策はRFC 2923にまとめられている。

いくつかある問題の中でも、Path MTU Discovery Black Hole（経路MTU探索ブラックホール）と呼ばれるケースは特に有名である。このケースは[ファイアウォール](../Page/ファイアウォール.md "wikilink")等でICMPパケットをフィルタしている場合に発生する。「Datagram Too Big」メッセージが送信元に届かないため、送信元はパケットが失われたことに気付かず、タイムアウトしてしまう。ICMPをフィルタする場合でも、少なくとも上記のType 3 Code 4のものだけは通す必要がある。もしそれができないのであれば、経路MTU探索をやめて断片化を許す設定に変更することになるだろう。

ただし現実には、自ホストの設定を変更することはできても、通信相手に問題を理解させて修正してもらうことは難しい。そこで、設定に問題がある場合でも通信するための回避策として、TCPの[Maximum Segment Size](https://ja.wikipedia.org/wiki/Maximum_Segment_Size "wikilink")（MSS）オプションを使う方法が知られている。TCPはコネクションを開始する際、自ホストが受信できる最大のセグメント長（TCPおよびIPのヘッダは除く）を通知することができる。通信相手からMSSオプションが送られてきた場合、その長さを超えるTCPデータグラムを送出してはならない。[IPv4](../Page/IPv4.md "wikilink")の場合、通常はTCPヘッダ20バイト、IPヘッダ20バイトなので、MSS + 40バイトがMTUに相当する。前述のフレッツ網を例にとると、MSSとして1414バイトを送っておけば、相手が経路MTU探索の候補とする値を1414 + 40 = 1454バイト以内に制限することができる。

MSSは本来、TCPコネクションの両端が設定する項目である。しかし最近のブロードバンドルーター等は、TCPセグメントの転送時にMSSオプションを書き換える機能を持っている。この機能を使えば、さらにMTUの小さな伝送路を通ったり、通信相手がMSSオプションを無視したりしない限り\[2\]、 経路MTU探索に由来する問題を回避できる。

## 脚注

## RFC

  - RFC 1191 - Path MTU Discovery
  - RFC 1812 - Requirements for IP Version 4 Routers
  - RFC 1981 - Path MTU Discovery for IP version 6
  - RFC 2923 - TCP Problems with Path MTU Discovery

## 関連項目

  - [最大セグメントサイズ](https://ja.wikipedia.org/wiki/最大セグメントサイズ "wikilink")（MSS）

## 参考文献

  -
[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:情報の単位](https://ja.wikipedia.org/wiki/Category:情報の単位 "wikilink")

1.
2.