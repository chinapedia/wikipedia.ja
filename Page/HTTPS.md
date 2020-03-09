> この記事は[HTTPS](https://ja.wikipedia.org/wiki/HTTPS)から翻訳されています。


**HTTPS** (Hypertext Transfer Protocol Secure) は、[HTTPによる通信をより安全に](../Page/Hypertext_Transfer_Protocol.md "wikilink")（[セキュアに](../Page/コンピュータセキュリティ.md "wikilink")）行うためのプロトコルおよび[URIスキームである](https://ja.wikipedia.org/wiki/Uniform_Resource_Identifier "wikilink")。厳密に言えば、HTTPS自体はプロトコルではなく、[SSL/TLSプロトコルによって提供されるセキュアな接続の上でHTTP通信を行うことをHTTPSと呼んでいる](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink")。

## 概要

HTTP通信において[認証](../Page/認証.md "wikilink")や暗号化を行うために、[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")によって開発された。当初、[World Wide Web上での個人情報の送信や](../Page/World_Wide_Web.md "wikilink")[電子決済](https://ja.wikipedia.org/wiki/電子決済 "wikilink")など、セキュリティが重要となる通信で使用されるようになった。その後、[公衆無線LAN](https://ja.wikipedia.org/wiki/公衆無線LAN "wikilink")の普及による[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")のリスクの増加\[1\]、[PRISMによる大規模な](https://ja.wikipedia.org/wiki/PRISM_\(監視プログラム\) "wikilink")[盗聴](https://ja.wikipedia.org/wiki/盗聴 "wikilink")、[ネット検閲](https://ja.wikipedia.org/wiki/ネット検閲 "wikilink")への対抗などを要因として、あらゆるHTTP通信をHTTPSに置き換える動きが活発になっている\[2\]\[3\]\[4\]\[5\]。

HTTPSは、メッセージを[平文](https://ja.wikipedia.org/wiki/平文 "wikilink")のままで送受信する標準のHTTPと異なり、[SSL/TLSプロトコルを用いて](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink")、サーバの認証・通信内容の[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")・[改竄検出](https://ja.wikipedia.org/wiki/改竄検出 "wikilink")などを行う。これによって、[なりすまし](https://ja.wikipedia.org/wiki/なりすまし "wikilink")・[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")・[盗聴](https://ja.wikipedia.org/wiki/盗聴 "wikilink")などの攻撃を防ぐことができる。HTTPSでは、[ウェルノウンポート番号として](https://ja.wikipedia.org/wiki/TCPやUDPにおけるポート番号の一覧#ウェルノウンポート番号_\(0–1023\) "wikilink")443が使われる。

HTTPSによるセキュリティ保護の強度は、Webサーバやブラウザで用いられるSSL/TLSの実装の正確性や、使用する暗号アルゴリズムに依存する（[TLSを参照](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink")）。

[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")サーバを介してインターネットにアクセスする場合、HTTPSのSSL/TLS通信時に[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")サーバを[トンネリング](https://ja.wikipedia.org/wiki/トンネリング "wikilink")する必要がある場合がある。その場合は**CONNECTメソッド**を使用する。

### メリット／デメリット

HTTPSを利用するメリット・デメリットは、以下のとおりである。

メリット

  - 通信が暗号化されるため、[改竄](https://ja.wikipedia.org/wiki/改竄 "wikilink")、[盗聴](https://ja.wikipedia.org/wiki/盗聴 "wikilink")などの攻撃を防ぐことができる。
  - [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")対応でブラウザ表示が高速化される。
  - [SEOに有利になる](https://ja.wikipedia.org/wiki/検索エンジン最適化 "wikilink")。検索エンジン最大手のGoogleがHTTPSの導入を推進するため、自社検索サービスにおいてHTTPSの使用するウェブサイトを優遇することを発表していることによる\[6\]\[7\]。

デメリット

  - 無料発行サービスを除き、導入に費用がかかる。
  - SSL証明書を定期的(90日/一年など)に更新する必要がある。
  - https非対応のツールや広告、ブログパーツなどが非表示になる。
  - 暗号化/復号が必要になるため、クライアントとサーバ共に負荷が上がる（但し、前述のHTTP/2を併用することで負荷を表示速度で相殺できる場合もある）。
  - 古い[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")から閲覧ができなくなる。

## 仕様

HTTPSの仕様が最初に標準化されたのは HTTP Over TLSである。TLS上でのHTTP通信について、ホスト名の検証（証明書の (subjectAltName)またはCommon Nameが接続しているURLのホスト名またはIPアドレスに合致することの判定）やhttps URIスキームなどの規定が明文化された。その後、規定の一部は以下のように更新されている。

  - https URIスキームの規定は、HTTP/1.1ので更新されている (2.7.2. https URI Scheme)。
  - TLS接続上でのHTTP/2通信は、HTTP/2ので規定されている (3.3. Starting HTTP/2 for "https" URIs)。

このほか、HTTPSには以下の仕様が関係している。

  - [X.509](https://ja.wikipedia.org/wiki/X.509 "wikilink") (PKIX)では、証明書に対する要件が規定されている。特にHTTPSに特有のものとして以下がある (RFC 5280 4.2.1.12. Extended Key Usage)。
      - サーバー証明書を表す拡張鍵用途: TLS WWWサーバー認証 (OID 1.3.6.1.5.5.7.3.1)。
      - クライアント証明書を表す拡張鍵用途: TLS WWWクライアント認証 (OID 1.3.6.1.5.5.7.3.2)。
  - [Application-Layer Protocol Negotiationを用いる場合](https://ja.wikipedia.org/wiki/Application-Layer_Protocol_Negotiation "wikilink")、識別子http/1.1 (RFC 7301 6.IANA Considerations)またはh2 (RFC 7540 11.1. Registration of HTTP/2 Identification Strings)を使用する 。
  - [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")では、TLSに対する追加の要件を課している (RFC 7540 9.2. Use of TLS Features)。

このほか、[認証局](https://ja.wikipedia.org/wiki/認証局 "wikilink")に対する要求として、がBaseline Requirementsを定めている\[8\]\[9\]。

## その他の方式

https URIスキームのURLを対象とする通信では、前述のTLS上でHTTPを用いる方法のほか、以下のプロトコルを使用する事例も存在する。

  - [SPDY](https://ja.wikipedia.org/wiki/SPDY "wikilink")
  - [QUIC](https://ja.wikipedia.org/wiki/QUIC "wikilink")

## https通信の手順

1.  クライアントがhttpsサーバにリクエストを送る。
2.  サーバはサポートしているSSL/TLSのバージョンと公開鍵を返し、鍵交換の手順を開始する。その結果、クライアントとサーバーは共通鍵**Z**を得る。
3.  以降は、共通鍵***Z***を使用して、GET/POSTなどの通信を行う。

## 情報の保護における誤解

HTTPSを用いた保護に関するよくある誤解に、「HTTPSによる通信は入力した情報にかかわる全ての処理を完全に保護する」というものがある。HTTPSは名前の通りアプリケーションレイヤのHTTPを保護するプロトコルでありWebブラウザとWebサーバの間の通信を暗号化して、[盗聴](https://ja.wikipedia.org/wiki/盗聴 "wikilink")や[改竄](https://ja.wikipedia.org/wiki/改竄 "wikilink")を防いでいるに過ぎず、IPsecのようなネットワークレイヤの保護を行うプロトコルではない。

情報を受け取ったサイトは、送信された情報のうち必要最小限のデータのみを安全に保管することが期待されるが、重要な個人情報がサイトのデータベースに格納されない保証はなく、さらにデータベースはしばしば外部からの攻撃の標的にされる。また、こうした情報が人為的に不当に流用されたり、事故によって漏洩する可能性もある\[10\]。

このように通信が完全に保護されていたとしても、利用者が期待する安全性が確保されているとは言えない場合がある。現在のインターネットでは、

## 統計

2016年から2017年にかけて、HTTPSのシェアが50%を超えたという複数の調査結果が明らかになっている\[11\]\[12\]。

2017年末、66%のシェアという調査報告がされた\[13\]。

2018年末、httparchive.orgの調査によると、79.9%のトラフィックという調査報告がされた\[14\]\[15\]\[16\]。

## 検閲

HTTPS通信は暗号化されているため、通信内容を読み取ったり[改竄](https://ja.wikipedia.org/wiki/改竄 "wikilink")したりすることはできない。そのため、基本的に通信内容を検閲することはできない。

HTTPSによる検閲対策に対抗する措置として、[中華人民共和国](../Page/中華人民共和国.md "wikilink")では、暗号化技術の利用が許可制になっている\[17\]。また、[ウィキペディア](https://ja.wikipedia.org/wiki/ウィキペディア "wikilink")に不適切な記述を含むページがあり、ロシアがこれを検閲しようとしたが、ウィキペディアがHTTPSを用いているため問題のページ単体を検閲できず、ロシアがウィキペディア全体をブロックし、ロシア国内からウィキペディアを閲覧できなくなったこともあった\[18\]。

## 類似のプロトコル

このほかに、TLS上でのHTTP通信に関するプロトコルが2つ存在する。いずれもURIスキームはhttpを用いる。

  - RFC 2817 Upgrading to TLS Within HTTP/1.1は、HTTPのUpgradeヘッダーを用いることで、HTTPと同じTCP 80番ポートでHTTP over TLS通信を行う方式を規定している。HTTPにおける[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")に相当する。
  - RFC 8164 Opportunistic Security for HTTP/2は、http URLに対する通信における[日和見暗号化](https://ja.wikipedia.org/wiki/日和見暗号化 "wikilink")を提供するものである。

## その他

RFC 2660 が規定する**S-HTTP** (Secure HTTP: )は、httpsスキームで用いられるHTTP over SSL/TLSとは別のプロトコルである。S-HTTPに対応するURIスキームはshttpである。

## 脚注

## 関連項目

  - [HTTP Strict Transport Security](https://ja.wikipedia.org/wiki/HTTP_Strict_Transport_Security "wikilink")

  - [Extended Validation 証明書](https://ja.wikipedia.org/wiki/Extended_Validation_証明書 "wikilink")

  -
## 外部リンク

  - RFC 2818（HTTP over TLS）

      - [HTTP オーバー TLS (HTTP Over TLS)](https://www.ipa.go.jp/security/rfc/RFC2818JA.html) — [IPAによる日本語訳](https://ja.wikipedia.org/wiki/情報処理推進機構 "wikilink")

  - [SSL/TLS 暗号化: はじめに - Apache HTTP サーバ バージョン 2.4](https://httpd.apache.org/docs/2.4/ja/ssl/ssl_intro.html)

  -
  - [IANAに登録されたURIスキーム](https://www.iana.org/assignments/uri-schemes.html)

### 利用統計

  - [Let's Encrypt Growth](https://letsencrypt.org/stats/) - [Let's Encrypt](https://ja.wikipedia.org/wiki/Let's_Encrypt "wikilink")
  - [State of the Web](https://httparchive.org/reports/state-of-the-web#pctHttps)
  - [HTTPS encryption on the web](https://transparencyreport.google.com/https/overview) - [Google](https://ja.wikipedia.org/wiki/Google "wikilink")

### S-HTTP

S-HTTPは、HTTPSとは別の暗号化通信用プロトコル。HTTPの拡張。

  - RFC 2660 - The Secure HyperText Transfer Protocol：S-HTTP

  -
[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink") [Category:Transport_Layer_Security](https://ja.wikipedia.org/wiki/Category:Transport_Layer_Security "wikilink") [Category:暗号化プロトコル](https://ja.wikipedia.org/wiki/Category:暗号化プロトコル "wikilink")

1.
2.
3.
4.
5.
6.
7.  [HTTPS をランキング シグナルに使用します](https://webmaster-ja.googleblog.com/2014/08/https-as-ranking-signal.html)
8.
9.
10.
11.
12.
13.
14. <https://httparchive.org/reports/state-of-the-web#pctHttps>
15. <https://letsencrypt.org/stats/>
16. <https://etherealmind.com/percentage-of-https-tls-encrypted-traffic-on-the-internet/>
17.
18.