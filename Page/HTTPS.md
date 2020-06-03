> この記事は[HTTPS](https://ja.wikipedia.org/wiki/HTTPS)から翻訳されています。


**HTTPS** (Hypertext Transfer Protocol Secure) は、[HTTPによる通信をより安全に](../Page/Hypertext_Transfer_Protocol.md "wikilink")（[セキュアに](../Page/コンピュータセキュリティ.md "wikilink")）行うためのプロトコルおよび[URIスキームである](../Page/Uniform_Resource_Identifier.md "wikilink")。厳密に言えば、HTTPS自体はプロトコルではなく、[SSL/TLSプロトコルによって提供されるセキュアな接続の上でHTTP通信を行うことをHTTPSと呼んでいる](../Page/Transport_Layer_Security.md "wikilink")。

## 概要

HTTP通信において[認証](../Page/認証.md "wikilink")や暗号化を行うために、[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")によって開発された。当初、[World Wide Web上での個人情報の送信や](../Page/World_Wide_Web.md "wikilink")[電子決済](https://ja.wikipedia.org/wiki/電子決済 "wikilink")など、セキュリティが重要となる通信で使用されるようになった。その後、[公衆無線LAN](../Page/公衆無線LAN.md "wikilink")の普及による[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")のリスクの増加\[1\]、[PRISMによる大規模な](https://ja.wikipedia.org/wiki/PRISM_\(監視プログラム\) "wikilink")[盗聴](../Page/盗聴.md "wikilink")、[ネット検閲](../Page/ネット検閲.md "wikilink")への対抗などを要因として、あらゆるHTTP通信をHTTPSに置き換える動きが活発になっている\[2\]\[3\]\[4\]\[5\]。

HTTPSは、メッセージを[平文](../Page/平文.md "wikilink")のままで送受信する標準のHTTPと異なり、[SSL/TLSプロトコルを用いて](../Page/Transport_Layer_Security.md "wikilink")、サーバの認証・通信内容の[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")・[改竄検出](https://ja.wikipedia.org/wiki/改竄検出 "wikilink")などを行う。これによって、[なりすまし](https://ja.wikipedia.org/wiki/なりすまし "wikilink")・[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")・[盗聴](../Page/盗聴.md "wikilink")などの攻撃を防ぐことができる。HTTPSでは、[ウェルノウンポート番号として](https://ja.wikipedia.org/wiki/TCPやUDPにおけるポート番号の一覧#ウェルノウンポート番号_\(0–1023\) "wikilink")443が使われる。

HTTPSによるセキュリティ保護の強度は、Webサーバやブラウザで用いられるSSL/TLSの実装の正確性や、使用する暗号アルゴリズムに依存する（[TLSを参照](../Page/Transport_Layer_Security.md "wikilink")）。

[プロキシ](../Page/プロキシ.md "wikilink")サーバを介してインターネットにアクセスする場合、HTTPSのSSL/TLS通信時に[プロキシ](../Page/プロキシ.md "wikilink")サーバを[トンネリング](../Page/トンネリング.md "wikilink")する必要がある場合がある。その場合は**CONNECTメソッド**を使用する。

### メリット／デメリット

HTTPSを利用するメリット・デメリットは、以下のとおりである。

メリット

  - 通信が暗号化されるため、[改竄](../Page/改竄.md "wikilink")、[盗聴](../Page/盗聴.md "wikilink")などの攻撃を防ぐことができる。
  - [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")対応でブラウザ表示が高速化される。
  - [SEOに有利になる](../Page/検索エンジン最適化.md "wikilink")。検索エンジン最大手のGoogleがHTTPSの導入を推進するため、自社検索サービスにおいてHTTPSの使用するウェブサイトを優遇することを発表していることによる\[6\]\[7\]。

デメリット

  - 無料発行サービスを除き、導入に費用がかかる。
  - SSL証明書を定期的(90日/一年など)に更新する必要がある。
  - https非対応のツールや広告、ブログパーツなどが非表示になる（後述する混在コンテンツに該当するため）。
  - 暗号化/復号が必要になるため、クライアントとサーバ共に負荷が上がる（但し、前述のHTTP/2を併用することで負荷を表示速度で相殺できる場合もある）。
  - 古い[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")から閲覧ができなくなる。

## ウェブブラウザでの扱い

[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")（[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")）では、対象のURLがhttpsであるなど、セキュアな通信経路であることが明らかであるか否かで動作を変える場合がある。これに関わる規定として、W3CのSecure Contexts（安全なコンテキスト）\[8\]やMixed Content（混在コンテンツ・混合コンテンツ）\[9\]\[10\]がある。

Secure Contextsでは、いくつかの条件を満たす場合に「secure contextである」とする規定がなされている。他の機能で、これを参照して挙動の変更に用いることを意図している。

Mixed contentは、セキュアな経路で取得したコンテンツ内で、非セキュアなデータの取り扱いに関する規定である。たとえば、https URLのHTMLドキュメント内でhttp URLのJavaScriptの実行は阻止される。

## 通信に関する仕様

HTTPSの仕様が最初に標準化されたのは HTTP Over TLSである。TLS上でのHTTP通信について、ホスト名の検証（証明書の (subjectAltName)またはCommon Nameが接続しているURLのホスト名またはIPアドレスに合致することの判定）やhttps URIスキームなどの規定が明文化された。その後、規定の一部は以下のように更新されている。

  - https URIスキームの規定は、HTTP/1.1ので更新されている (2.7.2. https URI Scheme)。
  - TLS接続上でのHTTP/2通信は、HTTP/2ので規定されている (3.3. Starting HTTP/2 for "https" URIs)。

このほか、HTTPSには以下の仕様が関係している。

  - [X.509](../Page/X.509.md "wikilink") (PKIX)では、証明書に対する要件が規定されている。特にHTTPSに特有のものとして以下がある (RFC 5280 4.2.1.12. Extended Key Usage)。
      - サーバー証明書を表す拡張鍵用途: TLS WWWサーバー認証 (OID 1.3.6.1.5.5.7.3.1)。
      - クライアント証明書を表す拡張鍵用途: TLS WWWクライアント認証 (OID 1.3.6.1.5.5.7.3.2)。
  - [Application-Layer Protocol Negotiationを用いる場合](https://ja.wikipedia.org/wiki/Application-Layer_Protocol_Negotiation "wikilink")、プロトコルIDとしてhttp/1.1 (RFC 7301 6. IANA Considerations)またはh2 (RFC 7540 11.1. Registration of HTTP/2 Identification Strings)を使用する。
      - RFCなどでプロトコルIDを登録する明示的な規定は存在しないものの、IANAの登録簿にはhttp/0.9とhttp/1.0も存在する\[11\]。
  - [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")では、TLSに対する追加の要件を課している。
      - TLS 1.2未満の使用禁止と、TLS 1.2に対する要件: RFC 7540 9.2. Use of TLS Features
      - TLS 1.3に対する要件: RFC 8740

このほか、[認証局](../Page/認証局.md "wikilink")に対する要求として、がBaseline Requirementsを定めている\[12\]\[13\]。

## その他の方式

https URIスキームのURLを対象とする通信では、前述のTLS上でHTTPを用いる方法のほか、以下のプロトコルを使用する事例も存在する。

  - [SPDY](https://ja.wikipedia.org/wiki/SPDY "wikilink")
  - [QUIC](https://ja.wikipedia.org/wiki/QUIC "wikilink")

## https通信の手順

1.  クライアントがhttpsサーバにリクエストを送る。
2.  サーバはサポートしているSSL/TLSのバージョンと公開鍵を返し、鍵交換の手順を開始する。その結果、クライアントとサーバーは共通鍵**Z**を得る。
3.  以降は、共通鍵***Z***を使用して、GET/POSTなどの通信を行う。

## 情報の保護における誤解

HTTPSを用いた保護に関するよくある誤解に、「HTTPSによる通信は入力した情報にかかわる全ての処理を完全に保護する」というものがある。HTTPSは名前の通りアプリケーションレイヤのHTTPを保護するプロトコルでありWebブラウザとWebサーバの間の通信を暗号化して、[盗聴](../Page/盗聴.md "wikilink")や[改竄](../Page/改竄.md "wikilink")を防いでいるに過ぎず、IPsecのようなネットワークレイヤの保護を行うプロトコルではない。

情報を受け取ったサイトは、送信された情報のうち必要最小限のデータのみを安全に保管することが期待されるが、重要な個人情報がサイトのデータベースに格納されない保証はなく、さらにデータベースはしばしば外部からの攻撃の標的にされる。また、こうした情報が人為的に不当に流用されたり、事故によって漏洩する可能性もある\[14\]。

このように通信が完全に保護されていたとしても、利用者が期待する安全性が確保されているとは言えない場合がある。現在のインターネットでは、

## 統計

2016年から2017年にかけて、HTTPSのシェアが50%を超えたという複数の調査結果が明らかになっている\[15\]\[16\]。

2017年末、66%のシェアという調査報告がされた\[17\]。

2018年末、httparchive.orgの調査によると、79.9%のトラフィックという調査報告がされた\[18\]\[19\]\[20\]。

## 検閲

HTTPS通信は暗号化されているため、通信内容を読み取ったり[改竄](../Page/改竄.md "wikilink")したりすることはできない。そのため、基本的に通信内容を検閲することはできない。

HTTPSによる検閲対策に対抗する措置として、[中華人民共和国](../Page/中華人民共和国.md "wikilink")では、暗号化技術の利用が許可制になっている\[21\]。また、[ウィキペディア](../Page/ウィキペディア.md "wikilink")に不適切な記述を含むページがあり、ロシアがこれを検閲しようとしたが、ウィキペディアがHTTPSを用いているため問題のページ単体を検閲できず、ロシアがウィキペディア全体をブロックし、ロシア国内からウィキペディアを閲覧できなくなったこともあった\[22\]。

## 類似のプロトコル

このほかに、TLS上でのHTTP通信に関するプロトコルが2つ存在する。いずれもURIスキームはhttpを用いる。

  - RFC 2817 Upgrading to TLS Within HTTP/1.1は、HTTPのUpgradeヘッダーを用いることで、HTTPと同じTCP 80番ポートでHTTP over TLS通信を行う方式を規定している。HTTPにおける[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS "wikilink")に相当する。
  - RFC 8164 Opportunistic Security for HTTP/2は、http URLに対する通信における[日和見暗号化](https://ja.wikipedia.org/wiki/日和見暗号化 "wikilink")を提供するものである。

## その他

RFC 2660 が規定する**S-HTTP** (Secure HTTP: )は、httpsスキームで用いられるHTTP over SSL/TLSとは別のプロトコルである。S-HTTPに対応するURIスキームはshttpである。

## 脚注

## 関連項目

  - [HTTP Strict Transport Security](https://ja.wikipedia.org/wiki/HTTP_Strict_Transport_Security "wikilink")

  - [Extended Validation 証明書](../Page/Extended_Validation_証明書.md "wikilink")

  -
## 外部リンク

  - RFC 2818（HTTP over TLS）

      - [HTTP オーバー TLS (HTTP Over TLS)](https://www.ipa.go.jp/security/rfc/RFC2818JA.html) — [IPAによる日本語訳](../Page/情報処理推進機構.md "wikilink")

  - [SSL/TLS 暗号化: はじめに - Apache HTTP サーバ バージョン 2.4](https://httpd.apache.org/docs/2.4/ja/ssl/ssl_intro.html)

  -
  - [IANAに登録されたURIスキーム](https://www.iana.org/assignments/uri-schemes.html)

### ウェブブラウザ側に関する規定

  - [Secure Contexts](https://w3c.github.io/webappsec-secure-contexts/): W3Cのドラフト文書
      - [Secure Contexts （日本語訳）](https://triple-underscore.github.io/webappsec-secure-contexts-ja.html)（非公式）
  - [Mixed Content](https://w3c.github.io/webappsec-mixed-content/): W3Cのドラフト文書
      - [Mixed Content（日本語訳）](https://triple-underscore.github.io/webappsec-mixed-content-ja.html)（非公式）
  - [Mixed Content Level 2](https://w3c.github.io/webappsec-mixed-content/level2.html): W3Cのドラフト文書
      - [Mixed Content Level 2（日本語訳）](https://triple-underscore.github.io/webappsec-mixed-content2-ja.html)（非公式）

### 利用統計

  - [Let's Encrypt Growth](https://letsencrypt.org/stats/) - [Let's Encrypt](https://ja.wikipedia.org/wiki/Let's_Encrypt "wikilink")
  - [State of the Web](https://httparchive.org/reports/state-of-the-web#pctHttps)
  - [HTTPS encryption on the web](https://transparencyreport.google.com/https/overview) - [Google](../Page/Google.md "wikilink")

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
11. [Transport Layer Security (TLS) Extensions, TLS Application-Layer Protocol Negotiation (ALPN) Protocol IDs](https://www.iana.org/assignments/tls-extensiontype-values/tls-extensiontype-values.xhtml#alpn-protocol-ids)
12.
13.
14.
15.
16.
17.
18. <https://httparchive.org/reports/state-of-the-web#pctHttps>
19. <https://letsencrypt.org/stats/>
20. <https://etherealmind.com/percentage-of-https-tls-encrypted-traffic-on-the-internet/>
21.
22.