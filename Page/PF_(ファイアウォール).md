> この記事は[PF \(ファイアウォール\)](https://ja.wikipedia.org/wiki/PF_\(ファイアウォール\))から翻訳されています。


**PF** (**Packet Filter**) とは、[パケットフィルターである](../Page/ファイアウォール.md "wikilink")。元々は、[OpenBSD](../Page/OpenBSD.md "wikilink")用に開発されたが、現在ではその他の[BSDの子孫](../Page/BSDの子孫.md "wikilink")や[Windowsでも使うことが出来る](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 概要

**PF** は、Daniel Hartmeierによって[OpenBSD](../Page/OpenBSD.md "wikilink")用に開発された、ステートフルなパケットフィルターである。

PFが作成されたのは、Darren Reedが作った[IPFilter](https://ja.wikipedia.org/wiki/IPFilter "wikilink")にあるライセンス上の問題を回避するためである。このライセンス上の問題とは、Darren Reed以外の人間にIPFilterのソースコード改変を許さないというものである。IPFilterの代替品が早急に必要だったため、PFは短期間で開発された。

[IPFilter](https://ja.wikipedia.org/wiki/IPFilter "wikilink")が削除されたとき、[テオ・デ・ラート](../Page/テオ・デ・ラート.md "wikilink")は「OpenBSDが使ったり配布したりするソフトウェアはあらゆることに対して自由でなくてはならない。...そして、それはどんな目的に対してでも自由であるべきだ...その目的が改変、利用、漏洩、子供の根囲いをする機械やオーストラリアに落とされる核爆弾に対する実装であったとしても」と語った。このことからもわかるように、OpenBSD開発者チームはこの手の問題に対して無駄な交渉を続けていくよりも、ソフトウェアを置き換えることを選ぶ。

現在、PFはOpenBSDだけでなく、[NetBSD](../Page/NetBSD.md "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")、[DragonFly BSDでも利用することが出来る](../Page/DragonFly_BSD.md "wikilink")。また、[Windowsでも](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Core forceという名前でOpenBSDの実装を使うことが出来る](https://ja.wikipedia.org/wiki/Core_force "wikilink")。

PFは、他の[ファイアウォール](../Page/ファイアウォール.md "wikilink")に無い利点を持つ。PFを使って[ネットワークアドレス変換](../Page/ネットワークアドレス変換.md "wikilink") (NAT) や[Quality of Service](../Page/Quality_of_Service.md "wikilink") (QoS) 制御を行うことが出来る。なお、QoS制御はキューイング機構である[ALTQ](https://ja.wikipedia.org/wiki/ALTQ "wikilink")で実装されており、PFの設定で指定することで利用できるようになる。

また、PFでは[pfsync](https://ja.wikipedia.org/wiki/pfsync "wikilink")や[CARPという](https://ja.wikipedia.org/wiki/Common_Address_Redundancy_Protocol "wikilink")[フェイルオーバー](https://ja.wikipedia.org/wiki/フェイルオーバー "wikilink")や冗長化のための機構や、authpfというセッション認証の機構、ftp-proxyというファイアウォールで扱いにくいプロトコルであるFTPを扱うための機構を使うことが出来る。

PF用の設定ファイル (pf.conf) の文法は、わかりやすい書き方に少し改変したところをのぞき、IPFilterの設定ファイルの文法によく似ている。

PFのログ出力は他のパケットフィルターと全く違っている。 ログ出力のルールはpf.confにて決めることが出来、**pflog**という仮想ネットワークインタフェースから得ることが出来る。 ログは[tcpdump](https://ja.wikipedia.org/wiki/tcpdump "wikilink")のような一般的なユーティリティで調査することが出来る。 なお、OpenBSDはこの目的のために[tcpdump](https://ja.wikipedia.org/wiki/tcpdump "wikilink")を拡張している。 また、**pflogd**というデーモンを使って改変した[tcpdump](https://ja.wikipedia.org/wiki/tcpdump "wikilink")/pcap形式でログを保存することも出来る。

## pf.conf ファイルの記述例

**`##``   ``マクロ`**

`# 内向けインタフェース (ローカルネットワークに接続).`
`int_if="xl0"`

**`##``   ``Options`**

`# blockした通信にデフォルトでRSTを返すかICMPを返すかを設定`
`set block-policy return`

`# ループバックインタフェースについては完全に無視する`
`set skip on lo0`

**`##``   ``アドレス変換規則`**

`# ローカルネットワークから`[`デフォルトルート`](https://ja.wikipedia.org/wiki/デフォルトルート "wikilink")として指定されているインタフェースである
`# `*`egress`*`インタフェースを通るところで`[`NAT`](https://ja.wikipedia.org/wiki/NAT "wikilink")を行う`。`
`nat on egress from $int_if:network to any -> (egress)`

**`##``   ``フィルタリングルール`**

`# すべてのパケットを遮断（block）し、ログに残す`
`block log all`

`# ローカルネットワークからのすべてのパケットを許可する。`*`quick`*`を使うと後で`
`# これにマッチするルールがあったとしても無視される。ローカルの通信をさらに厳しく`
`# 評価するようなルールもあるかもしれない。`
`pass quick on $int_if all`

`# 外に出て行くすべてのトラフィックを許可する。そして、それらのパケットへの返事が自動的に`
`# 許可されるように、状態を記憶する。そうしないと、外部向けの（egress）インタフェースから`
`# 出て行く通信や入ってくる通信に対して多くのルールをここに記述することになる。`
`pass out keep state`

## 関連項目

  - [通信プロトコル](../Page/通信プロトコル.md "wikilink")
  - [TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")
  - [ネットワークアドレス変換](../Page/ネットワークアドレス変換.md "wikilink")

## 外部リンク

  - [OpenBSD's pfctl man page](http://www.openbsd.org/cgi-bin/man.cgi?query=pfctl&sektion=8)
  - [The OpenBSD PF guide](http://www.openbsd.org/faq/pf/)
  - [The OpenBSD 3.6 release song](http://www.openbsd.org/lyrics.html#36) with background information on PF's creation
  - [PF section on Daniel Hartmeier's site](http://www.benzedrine.cx/pf.html)
  - [PF tutorial by Peter N. M. Hansteen](http://www.bgnett.no/~peter/pf/)

[Category:OpenBSD](https://ja.wikipedia.org/wiki/Category:OpenBSD "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:ファイアウォールソフトウェア](https://ja.wikipedia.org/wiki/Category:ファイアウォールソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")