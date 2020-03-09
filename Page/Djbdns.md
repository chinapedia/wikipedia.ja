> この記事は[Djbdns](https://ja.wikipedia.org/wiki/Djbdns)から翻訳されています。


**djbdns**は[ダニエル・バーンスタイン](https://ja.wikipedia.org/wiki/ダニエル・バーンスタイン "wikilink")により開発された[DNSサーバ](https://ja.wikipedia.org/wiki/DNSサーバ "wikilink")用[ソフトウェア](../Page/ソフトウェア.md "wikilink")。

## 概要

[DNSキャッシュサーバ](https://ja.wikipedia.org/wiki/DNSキャッシュサーバ "wikilink")のdnscacheと[DNSコンテンツサーバ](https://ja.wikipedia.org/wiki/DNSコンテンツサーバ "wikilink")のtinydnsを2つの柱として構成されている。[BIND](https://ja.wikipedia.org/wiki/BIND "wikilink")とは違い非常にシンプルかつ堅牢な構造をしており、バーンスタインは djbdns の[セキュリティホール](https://ja.wikipedia.org/wiki/セキュリティホール "wikilink")の第一発見者へ1000[ドル](https://ja.wikipedia.org/wiki/ドル "wikilink")の懸賞金を与えることを発表していた\[1\]。2009年2月に Matthew Dempsky により[キャッシュ](https://ja.wikipedia.org/wiki/キャッシュ "wikilink")汚染攻撃が可能であることが発見され\[2\]、Dempsky は懸賞金を獲得した\[3\]。2009年3月現在、発見されたセキュリティホールはこの1個のみである。

2007年冬、[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")となる\[4\]。

## 特徴

キャッシュサーバとコンテンツサーバの分離が djbdns の大きな特徴である。BIND では、このふたつのサーバ機能を単一の named と呼ばれる[デーモンで管理していた](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")。キャッシュサーバである dnscache の機能は、クライアントからのクエリを受付けて再帰検索を行い、[名前解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")を行い、得た情報をキャッシュすること、コンテンツサーバである tinydns の機能は、回答すべきゾーン情報を管理し、問い合わせに答えるという機能をもつ。コンテンツサーバはあくまでも自ゾーン情報を公開するためのもので、DNS情報のキャッシュや再帰検索は行わない。キャッシュサーバとコンテンツサーバの機能はまったく別であり、同一サーバでこのふたつのデーモンを稼働させることは推奨されていない。また、組織外に公開すべきではないキャッシュサーバをうっかり公開してしまうミスを防ぐこともできる。

djbdns は、デーモンだけでなく、各種のツールも単機能のプログラムが協調して動く設定になっている。また、可能な限り root 権限を使用せず、デーモンは、[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink") して動作する。設定ファイルも簡素である。djbdns はその管理に、[daemontools](https://ja.wikipedia.org/wiki/daemontools "wikilink") と呼ばれるミドルウェアを使用する。tinydns の DNSデータベースの格納には、[cdb](https://ja.wikipedia.org/wiki/cdb "wikilink")と呼ばれる高速なハッシュ化データベースが使用される。

djbdns では、CNAME の使用は可能だが推奨されてはいない。Aレコードを使用することが推奨されている。

## コンポーネント

  - dnscache - DNSキャッシュサーバ
  - tinydns - DNSコンテンツサーバ
  - axfrdns -[ゾーン転送用](https://ja.wikipedia.org/wiki/DNSゾーン転送 "wikilink")[TCP版DNSコンテンツサーバ](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol "wikilink")
  - walldns - [ファイアウォール](https://ja.wikipedia.org/wiki/ファイアウォール "wikilink")で使用するための、匿名の逆引き用DNSコンテンツサーバ
  - rbldns - リアルタイムブラックホールリストのためのデーモン
  - dnsライブラリ - libresolvに代わるDNSクエリのためのライブラリ

## パッチによる保守

djbdnsは2001年にバージョン1.0.5がリリースされて以来、公式の改良は行われていない。このため、[DNSSECなどの新しい機能には対応していない](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink")。また、ダニエル・バーンスタインが[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")の導入や普及に対して懐疑的な立場である\[5\]ことから、IPv6に対応していない。これに対して、有志によるパッチが提供されているが、以下の点が問題として考えられる。

  - 将来性 - DNSSECやIPv6に対応していないことなど、DNSサーバとしての機能の不足は否めない
  - 安全性 - 公式配布の状態では堅牢であるが、実用上パッチの適用が必要であり、パッチを当てた状態での堅牢性については誰も保証しない

## 関連項目

  - [qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")
  - [daemontools](https://ja.wikipedia.org/wiki/daemontools "wikilink")
  - [dbndns](https://ja.wikipedia.org/wiki/dbndns "wikilink")
  - [Unbound](https://ja.wikipedia.org/wiki/Unbound "wikilink")

## 脚注

<div class="references-small">

<references />

</div>

## 外部リンク

  - [djbdnsホームページ](https://cr.yp.to/djbdns.html) (英語)

[Category:DNSソフトウェア](https://ja.wikipedia.org/wiki/Category:DNSソフトウェア "wikilink") [Category:サーバ](https://ja.wikipedia.org/wiki/Category:サーバ "wikilink")

1.
2.
3.
4.
5.