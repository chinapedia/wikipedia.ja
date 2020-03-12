> この記事は[DNS](https://ja.wikipedia.org/wiki/DNS)から翻訳されています。


**DNSラウンドロビン** (**DNS round robin**)とは、一つのドメイン名に複数の[IPアドレス](../Page/IPアドレス.md "wikilink")を割り当てる[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")技術の一つである。

## 概要

トラフィック負荷を複数のIPアドレスに振り分けることにより、例えばHTTPサーバに対するアクセスをほぼ同量ずつ複数のサーバマシンに分配することができる。これは[BIND](../Page/BIND.md "wikilink")等DNSサーバのゾーン設定により容易に実現できる負荷分散方式である。 アクセス数に応じた負荷分散のほか、通信量、サーバの負荷（[CPU](../Page/CPU.md "wikilink")や[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")の使用率）、[応答時間](../Page/応答時間.md "wikilink")で負荷分散をすることができる。

後述するような問題点があることに加え、主に[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")における宛先アドレス選択アルゴリズムとして定義された「RFC3484」では、DNSが同一サーバ名に対し複数のIPアドレスを持つ場合に「自分のアドレスに近いアドレスを優先的に選択する」ことを定めており\[1\]、[Windows Vistaなど](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")製OSの一部や、最近の[Linux](../Page/Linux.md "wikilink")などではこのルールに従いDNSラウンドロビンがデフォルトで無効にされている\[2\]\[3\]。

このため、近年では他の負荷分散方式を用いたり、[クラスタリングを導入するケースが増えてきている](../Page/コンピュータ・クラスター.md "wikilink")。また[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")などが採用する「IPアドレスの上位プレフィックスを同じ値で揃える」方法など、RFC3484が有効な環境でもDNSラウンドロビンの効力を発揮させるテクニックも編み出されている\[4\]。

## メリット

  - 導入が容易である……ゾーンファイルの設定のみで導入できる
  - ネットワーク的に離れたサーバーに分散できる

## 問題点

  - 分散先サーバの通信継続性
    接続ごとに接続先が違うと、接続の継続性が求められるサーバの場合に問題が起きる可能性がある(Webアプリケーションのセッション管理や暗号化通信など)。
  - 分散先サーバの同期
    分散サーバのコンテンツの内容が同一でないと、接続に問題が起きる可能性がある(Webサーバでのリンクなど)。
  - DNSキャッシングの情報更新の際に生じる時差
    レコードの[TTLが長い場合](../Page/Time_to_live.md "wikilink")、変更前の情報を参照してしまう期間が長くなってしまう。後述のようにTTLを短めにした運用が一般的である。
  - トラフィック負荷を分散する際の予期せぬ偏り
    均等な負荷分散はできない。ヘビーユーザが一つの通信先に集中してアクセスを行う場合もある
  - 分散先サーバの障害検知が不可能
    DNSラウンドロビンでは、基本的に分散先サーバの状態が取得できないため分散先サーバが応答不可能な状態になっていても分散先として割り振ってしまう。
  - 512バイト問題
    同一のサーバ名に対し多くのIPアドレスを割り当てた結果、DNS Queryの結果が一般的なUDPパケットのサイズである512バイトを超えてしまう場合に、ソフトウェアによって正常な処理が行われない場合がある\[5\]。

## ゾーンファイル記述例

    <nowiki>
    hoge       IN  A  127.0.1.1
    hoge       IN  A  127.0.1.2
    hoge       IN  A  127.0.1.3
    </nowiki>

※実際に運用する際には

    <nowiki>
    hoge   30m  IN  A  127.0.1.1
    hoge   30m  IN  A  127.0.1.2
    hoge   30m  IN  A  127.0.1.3
    </nowiki>

のように、TTLを短めに設定して頻繁にリクエスト先を変えさせることが好ましい。

以前は、以下のようにCNAMEレコードを用いて記述されることがあったが、現在のDNSの仕様ではこの方法は禁止されている。

    <nowiki>
    hoge       IN  CNAME hoge1
               IN  CNAME hoge2
               IN  CNAME hoge3
    hoge1      IN  A     127.0.1.1
    hoge2      IN  A     127.0.1.2
    hoge3      IN  A     127.0.1.3
    </nowiki>

## 関連項目

  - [Domain Name System](../Page/Domain_Name_System.md "wikilink")
  - [プロキシ](../Page/プロキシ.md "wikilink")…[リバースプロキシ](https://ja.wikipedia.org/wiki/プロキシ#リバースプロキシ "wikilink")

## 脚注

[Category:Domain_Name_System](https://ja.wikipedia.org/wiki/Category:Domain_Name_System "wikilink")

1.  [RFC3484](http://www.ietf.org/rfc/rfc3484.txt)の「6.Destination Address Selection」→「Rule 9」を参照。
2.  [Windows Vista and Windows Server 2008 DNS clients do not honor DNS round robin by default](http://support.microsoft.com/kb/968920) - Microsoft KnowledgeBase
3.  [GETADDRINFO](http://linuxjm.osdn.jp/html/LDP_man-pages/man3/getaddrinfo.3.html) - Linux Programmer's Manual (3)
4.  [知ってますか？ DNSの浸透問題や親子同居問題、検閲の影響](http://www.atmarkit.co.jp/news/201209/07/dnssummerdays.html) - @IT・2012年9月7日
5.  [DNS ラウンドロビンのすすめ - その3](http://techblog.jword.jp/?eid=42) - JWord 開発者ブログ