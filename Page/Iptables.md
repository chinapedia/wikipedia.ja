> この記事は[Iptables](https://ja.wikipedia.org/wiki/Iptables)から翻訳されています。


**iptables**は、[Linux](../Page/Linux.md "wikilink")に実装された[パケットフィルタリングおよび](../Page/ファイアウォール.md "wikilink")[ネットワークアドレス変換](../Page/ネットワークアドレス変換.md "wikilink") (NAT) 機能であるNetfilter（複数の[Netfilter](https://ja.wikipedia.org/wiki/Netfilter "wikilink")モジュールとして実装されている）の設定を操作するコマンドのこと。Netfilterは、いわゆる[ファイアウォール](../Page/ファイアウォール.md "wikilink")や[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")としての役割を果たす。[IPv4](https://ja.wikipedia.org/wiki/IPv6 "wikilink") 用の実装が **iptables** で、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") 用の実装が **ip6tables** である。

## Linuxのバージョンとパケットフィルタ

[Netfilter-packet-flow.svg](https://ja.wikipedia.org/wiki/File:Netfilter-packet-flow.svg "fig:Netfilter-packet-flow.svg") Linux[カーネル](../Page/カーネル.md "wikilink")2.4以降では、[Netfilter](https://ja.wikipedia.org/wiki/Netfilter "wikilink")というパケット処理のためのフレームワークをもっており、これの設定を操作するツールがiptablesである。

Linuxカーネル2.2系列以前では[ipchains](https://ja.wikipedia.org/wiki/ipchains "wikilink")または[ipfwadm](https://ja.wikipedia.org/wiki/ipfwadm "wikilink")といった実装が使われていた。netfilterとiptablesはこれらを完全に置き換えるものである。

## iptablesの構成

iptablesでは、フィルタリングする対象を選ぶ「テーブル」と、各テーブルにおいて、どのタイミングで処理するかを示す「チェイン」で構成されている。

  - filterテーブルはパケットの出入り自体を制御できる
  - natテーブルはパケットの中身を書き換えることを制御できる、主に[ネットワークアドレス変換](../Page/ネットワークアドレス変換.md "wikilink")やIPマスカレード(LinuxのNAPT実装)向けに用いられる。

filterテーブルでは、初期状態で次のチェインが用意されている。

  - パケットが入る際に利用するINPUTチェイン
  - パケットが出ていく際に利用するOUTPUTチェイン
  - インターフェース間をまたぐ際に利用するFORWARDチェイン

natテーブルでは、主にパケットを書換えるタイミングに影響する次のチェインが用意されている。これらのチェインは管理者であれば自由に追加、削除が可能となっている。

  - PREROUTINGチェイン
  - POSTROUTINGチェイン

## チェインの編集

iptablesは各テーブル内のチェインを書換えることにより、パケットフィルタリングができる。

### パケットフィルタリングの例

チェインを編集するには例えば、次のようにiptablesコマンドを用いる。

    iptables -t filter -I INPUT -p tcp -s 123.123.123.123 --dport 80 -j DROP

  - \-t filter でfilterテーブルを操作
  - \-I INPUT でINPUTチェインに追加(-Iでチェイン内ルールの先頭に、-Aで末尾に)
  - \-p tcp でTCPプロトコル限定
  - \-s 123.123.123.123 で送信元IPアドレスを指定、
  - \--dport 80 で 80番ポート(80/tcp = http)を指定
  - 上記ルールにマッチしたパケットを-j DROPで破棄

まとめると*filterテーブルのINPUTチェインの先頭に以下のルールを追加：IP 123.123.123.123から80/tcp(http)に入ろうとしているパケットは送信元(123.123.123.123)に通知することなく破棄(DROP)*ということになる。

### ネットワークアドレス変換の例

下記の例で、例えば、LAN内に 192.168.0.10:8080 で公開しているウェブサーバーがあり、それを 80 番ポートで公開することが出来る。

`iptables --table nat --append PREROUTING --protocol tcp --destination-port 80 \`
`  --jump DNAT --to-destination 192.168.0.10:8080`

## 関連項目

  - [Firestarter](https://ja.wikipedia.org/wiki/Firestarter "wikilink")
  - [Firewalld](https://ja.wikipedia.org/wiki/Firewalld "wikilink")

## 外部リンク

  - [Manpage of iptables](http://linuxjm.sourceforge.jp/html/iptables/man8/iptables.8.html) (JM Projectによる日本語訳)
  - [Manpage of ip6tables](http://linuxjm.sourceforge.jp/html/iptables/man8/ip6tables.8.html)
  - [Iptablesチュートリアル](http://www.asahi-net.or.jp/~aa4t-nngk/ipttut/output/index.html)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:ファイアウォールソフトウェア](https://ja.wikipedia.org/wiki/Category:ファイアウォールソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")