> この記事は[Localhost](https://ja.wikipedia.org/wiki/Localhost)から翻訳されています。


[コンピュータ](../Page/コンピュータ.md "wikilink")では、**localhost**は現在使用しているシステムを指す。これは、[IPv4](https://ja.wikipedia.org/wiki/IPv4 "wikilink")では**127.0.0.0/8** に、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では**::1/128** に割り当てられた[ループバック](https://ja.wikipedia.org/wiki/ループバック "wikilink")デバイスである。[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")が必要に応じて自身と通信するために使用される。

ローカルマシンがまるでリモートマシンであるかのように通信することが出来るというのは、テスト目的には便利なことである。また、リモートであることが予期されているが、実際にはローカルマシンに存在するサービス（[コンピュータゲーム](../Page/コンピュータゲーム.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")など）との通信にも役立つ。

## IETFでの関連記載

IETFドキュメント"Special-Use IPv4 Addresses" (RFC 5735)には、**127.0.0.0/8**はループバック用に予約された[IPv4アドレスであると記載されている](../Page/IPアドレス.md "wikilink")。

このアドレスはどの組織やISPにも割り当てられていない。このアドレスブロック'127.0.0.0/8'宛のパケットはホストシステム外へは出ない。ホストシステム内部では、[ループバック](https://ja.wikipedia.org/wiki/ループバック "wikilink")インターフェースは一般的にアドレス'127.0.0.1'に対し[サブネットマスク](https://ja.wikipedia.org/wiki/サブネットマスク "wikilink")'255.0.0.0'を割り当てる。これは、ローカルシステムの[ルーティングテーブル](../Page/ルーティングテーブル.md "wikilink")にルーティングエントリー'127.0.0.0/8'を設定するので、'127.0.0.0/8'のどのアドレス宛のパケットもシステム内部にルーティングされる。

一方で、RFC 4291に記載されているIPv6アドレスアーキテクチャでは、たった1つの[IPv6アドレス](https://ja.wikipedia.org/wiki/IPv6アドレス "wikilink")**::1/128**のみが**ループバックアドレス**に指定されている。

RFC 4291では、以下のように述べられている："ループバックアドレスは、単一ノードの外側に送信する IPv6パケットの送信元アドレスとして使用してはならない。ループバックの宛先アドレスを持つIPv6パケットは、単一ノードの外側に送信してはならず、IPv6ルータは転送してはならない。ループバックの宛先アドレスを持つインタフェース上で受信したパケットは落とさなければならない。"

## localhostのいたずら

初心者や[スクリプトキディ](https://ja.wikipedia.org/wiki/スクリプトキディ "wikilink")につけ込んだ典型的な[IRCのいたずらに](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")、インターネット接続を切断させるために127ブロックのIPアドレスを与えるというものがある\[1\]。

## 注意事項

[IPアドレス](../Page/IPアドレス.md "wikilink")の[逆引き](../Page/逆引き.md "wikilink")で**localhost**を返すサーバもあるため、[アクセス制御](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")で**localhost**を設定する場合は注意が必要である。

## 参考

<references/>

## 外部リンク

  - RFC 5735: "特別に使用するIPv4アドレス"
  - RFC 4291: "インターネットプロトコルバージョン6(IPv6)のアドレスアーキテクチャ"

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink")

1.  ["Dangerous hacker\!: the Bitchchecker story"](http://www.totalillusions.net/forum/index.php?showtopic=328), *Total Illusions*, forum post. Accessed April 30, 2006.