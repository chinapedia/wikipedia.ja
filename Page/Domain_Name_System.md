> この記事は[Domain Name System](https://ja.wikipedia.org/wiki/Domain_Name_System)から翻訳されています。


**Domain Name System**（ドメイン・ネーム・システム、**DNS**）とは、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")を使った階層的な分散型[データベース](../Page/データベース.md "wikilink")システムである。[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")に[Information Sciences Institute](https://ja.wikipedia.org/wiki/Information_Sciences_Institute "wikilink")（ISI）の[ポール・モカペトリス](https://ja.wikipedia.org/wiki/ポール・モカペトリス "wikilink")と[ジョン・ポステル](https://ja.wikipedia.org/wiki/ジョン・ポステル "wikilink")により開発された。

現在では、主にインターネット上の[ホスト名](https://ja.wikipedia.org/wiki/ホスト名 "wikilink")や[電子メール](https://ja.wikipedia.org/wiki/電子メール "wikilink")に使われる[ドメイン名](https://ja.wikipedia.org/wiki/ドメイン名 "wikilink")と、[IPアドレス](https://ja.wikipedia.org/wiki/IPアドレス "wikilink")との対応づけ（[正引き](https://ja.wikipedia.org/wiki/正引き "wikilink")、[逆引き](https://ja.wikipedia.org/wiki/逆引き "wikilink")）を管理するために使用されている。

## 概要

インターネットに接続されているすべてのコンピュータは、固有の[IPアドレス](https://ja.wikipedia.org/wiki/IPアドレス "wikilink")を持っている。たとえば、ウィキペディア日本語版の[webサーバ](https://ja.wikipedia.org/wiki/webサーバ "wikilink")の持つIPアドレスは、2012年10月現在では`208.80.154.225`である。インターネット上のどのコンピュータにアクセスする際にも最終的にはそのコンピュータの IPアドレスを知る必要がある。しかし、IPアドレスは0から255までの数値を4つ組み合わせ（IPv4の場合）表現されるため、人間には記憶しにくい。そのため、IPアドレスを人間が覚えやすい名前で扱うことができるような機構として、[インターネットドメイン名が考案された](https://ja.wikipedia.org/wiki/ドメイン名 "wikilink")。このような、ドメイン名からIPアドレスを引き出す機能（[正引き](https://ja.wikipedia.org/wiki/正引き "wikilink")）が、DNSの代表的な機能である。このほか、ドメイン名に関連するメールサーバ情報なども取り扱っている。

## 動作

DNSは、ホスト名（たとえば`ja.wikipedia.org`）の入力に対して、[DNSサーバ](https://ja.wikipedia.org/wiki/DNSサーバ "wikilink")と呼ばれるコンピュータを参照し、そのホストが持つIP アドレス（たとえば`130.94.122.197`）を[検索](https://ja.wikipedia.org/wiki/検索 "wikilink")するシステムである。喩えるならば、DNSは氏名から電話番号を自動で調べる電話帳のようなものである。

たとえば、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")に[URIを入力してネットワークにアクセスする際](https://ja.wikipedia.org/wiki/Uniform_Resource_Identifier "wikilink")、ブラウザはURIを解析して、アクセスすべきWebサーバのホスト名を取り出し、後述のリゾルバ[APIに渡す](https://ja.wikipedia.org/wiki/アプリケーションプログラミングインタフェース "wikilink")。リゾルバAPI（通常は[OS内部での働き](../Page/オペレーティングシステム.md "wikilink")）は、Webサーバのホスト名をDNSサーバに問い合わせて返ってきたIPアドレスにより、ホスト名をIPアドレスに変換してブラウザに返す。ブラウザは、得られたIPアドレスを使用して、Webサーバとの通信を開始する。このようにしてブラウザはインターネットにアクセスする。

ホスト名から、そのホストにアクセスするためのIPアドレスを得ることを、ホスト名の「**[解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")**」（resolve）と呼び、これを行うためのクライアント側のしくみやプログラムを「**[リゾルバ](https://ja.wikipedia.org/wiki/リゾルバ "wikilink")**」（resolver）または「**ネームリゾルバ**」という。

DNSに格納されている情報を「**レコード**」（DNSレコード、リソースレコード）と呼ぶ。レコードは格納する情報によって種類が分類分けされている。レコードの種類は「[DNSレコードタイプの一覧](https://ja.wikipedia.org/wiki/DNSレコードタイプの一覧 "wikilink")」を参照。

ただし現実の電話帳との違いは、この情報がインターネット上のいくつものコンピュータ（DNSサーバ）に分散して格納されているところにある。インターネットには莫大な数のコンピュータが接続されており、これらのホスト名と IPアドレスは日々更新されつづけているため、インターネット上の**すべての**ホスト名を一台のコンピュータで集中管理することは現実的ではなかった。そのためインターネット上のコンピュータをある単位で区分けして、それぞれのグループがもつデータをグループごとのコンピュータに別々に管理させるようにした。これが DNS の基本的なアイデアである。このグループを**ドメイン**と呼ぶ。各グループには英数字とハイフン（ `-` ）からなるラベル（[ドメイン名](https://ja.wikipedia.org/wiki/ドメイン名 "wikilink")）がつけられており、異なるドメインの情報は異なるコンピュータに格納される。

今でこそDNSはホスト名とIPアドレスの対応づけに使用されるのがほとんどだが、もともとは[電子メール](https://ja.wikipedia.org/wiki/電子メール "wikilink")の配送方法やコンピュータの機種名を登録するなどといった用途も考えられていた。

ドメイン名は階層的な構造をもっている。たとえば`ja.wikipedia.org`というホスト名は`ja`、`wikipedia`、`org`という3つの階層に区切ることができる。`ja.wikipedia.org`というホストは`wikipedia.org`ドメインに所属しており、このドメインはさらに`org`ドメインに所属している。ドメイン名は一個の巨大な[木構造をなしており](https://ja.wikipedia.org/wiki/木構造_\(データ構造\) "wikilink")、この構造を[ドメイン名前空間](https://ja.wikipedia.org/wiki/ドメイン名前空間 "wikilink")（Domain Name Space）と呼ぶ。ドメイン名前空間は頂点に`.`（ルート）ノードを持ち、そこから[`.com`](https://ja.wikipedia.org/wiki/.com "wikilink")、[`.org`](https://ja.wikipedia.org/wiki/.org "wikilink")、[`.jp`](https://ja.wikipedia.org/wiki/.jp "wikilink") などの各[トップレベルドメイン](https://ja.wikipedia.org/wiki/トップレベルドメイン "wikilink")（TLD）が分かれている。

各ドメインはゾーンと呼ばれる管轄に分けて管理されている。ゾーンはドメイン名前空間上のある一部分に相当し、それぞれのゾーンは独立した[DNSコンテンツサーバ](https://ja.wikipedia.org/wiki/DNSコンテンツサーバ "wikilink")と呼ばれるコンピュータによって管理されている（[ドメイン名の委譲](https://ja.wikipedia.org/wiki/ドメイン名の委譲 "wikilink")）。DNSコンテンツサーバは、管理しているゾーンのホスト名とIPアドレスの組を記述したデータベースを持っており、クライアントマシン（あるいは[DNSキャッシュサーバ](https://ja.wikipedia.org/wiki/DNSキャッシュサーバ "wikilink")）からの要求に応じて、あるホスト名に対応するIPアドレスを返す。DNSクライアントはルートサーバからいくつものDNSサーバをたどっていき、最終的なホスト名のIPアドレスを得る（DNSの再帰検索）。

### DNSサーバの役割

具体的な例として、`ja.wikipedia.org`というホスト名の IPアドレスを検索することを考えると、再帰検索は、[トップレベルドメイン](https://ja.wikipedia.org/wiki/トップレベルドメイン "wikilink")を[ルートサーバ](https://ja.wikipedia.org/wiki/ルートサーバ "wikilink")に問い合わせることからはじまる。`ja.wikipedia.org`というホスト名は`wikipedia.org`ドメインに属し、また`wikipedia.org`ドメインは`org`ドメインに属するため、クライアントは最初に`org`ドメインのDNSサーバ（ネームサーバ）の[IPアドレス](https://ja.wikipedia.org/wiki/IPアドレス "wikilink")を得なければならない。

まず、クライアントは適当なルートサーバをひとつ選ぶ。ここでは `A.ROOT-SERVERS.NET`（`198.41.0.4`）とする。現在、[ルートサーバ](https://ja.wikipedia.org/wiki/ルートサーバ "wikilink")に登録されている`org`ドメインのネームサーバは9つあり、そのうちのひとつは`a7.nstld.com`（`192.5.6.36`）である。

つぎにクライアントは、このネームサーバに`wikipedia.org`ドメインのネームサーバの IPアドレスを問い合わせる。するとそのネームサーバのホスト名は`dns34.register.com`（`216.21.226.87`）であることがわかる。

最後に、このネームサーバに`ja.wikipedia.org`のIPアドレスを問い合わせる。するとこのサーバは最終的な答`130.94.122.197`を返す。こうして目的とするホスト名のIPアドレスを検索できる。

## DNS over HTTPS (DoH)

DNSデータを、[HTTPS](https://ja.wikipedia.org/wiki/HTTPS "wikilink")上でやりとりする\[1\]ことで、セキュリティとプライバシーを向上させる。これは RFC 8484 で定義され、[MIMEタイプとして](https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions "wikilink")`application/dns-message`を使う。

## 存在意義

DNSは、ほとんどのインターネット利用者が普段意識していない透過的なシステムだが、その役割は非常に重要である。あるドメインを管理している[DNSサーバ](https://ja.wikipedia.org/wiki/DNSサーバ "wikilink")が停止してしまうと、そのドメイン内のホストを示す[URL](https://ja.wikipedia.org/wiki/URL "wikilink")や[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")の名前解決などができなくなり、ネットワークが利用者とつながっていてもそのドメイン内のサーバ類には事実上アクセスできなくなる。そのため、重要なDNSサーバは[二重化されていることが多い](https://ja.wikipedia.org/wiki/冗長化 "wikilink")。

また[DNS偽装](https://ja.wikipedia.org/wiki/DNS偽装 "wikilink")を行うと、情報を容易に盗聴・偽装することができてしまう。情報レコードの不正な書き換えを防止するため、コンテンツサーバのマスタ（プライマリ）はインターネット（外部）から隠匿し、インターネットには特定のマスタのコピー（ゾーン転送）を受け取るスレーブ（セカンダリ）を公開するなどの構成を組んで、防衛手段を講じる。

## 関連語句

  - [DNSサーバ](https://ja.wikipedia.org/wiki/DNSサーバ "wikilink")
      - [Dynamic Domain Name System](https://ja.wikipedia.org/wiki/ダイナミックドメインネームシステム "wikilink")（ダイナミックDNS、DDNS）

      - [リゾルバ](https://ja.wikipedia.org/wiki/リゾルバ "wikilink")

      - [djbdns](https://ja.wikipedia.org/wiki/djbdns "wikilink") - DNSサーバ用ソフトウェア。

      - [BIND](https://ja.wikipedia.org/wiki/BIND "wikilink")

      - [unbound](https://ja.wikipedia.org/wiki/unbound "wikilink") - オープンソースのDNSキャッシュサーバ

      - [DNSルートゾーン](https://ja.wikipedia.org/wiki/DNSルートゾーン "wikilink")

      - [DNSゾーン転送](https://ja.wikipedia.org/wiki/DNSゾーン転送 "wikilink")

      - [DNSレコードタイプの一覧](https://ja.wikipedia.org/wiki/DNSレコードタイプの一覧 "wikilink")

          - [MXレコード](https://ja.wikipedia.org/wiki/MXレコード "wikilink")

          -
          - [Glue Record](https://ja.wikipedia.org/wiki/Glue_Record "wikilink")

      - [DNSBL](https://ja.wikipedia.org/wiki/DNSBL "wikilink")（DNSブラックリスト）

      - [DNSラウンドロビン](https://ja.wikipedia.org/wiki/DNSラウンドロビン "wikilink")

      - (extension mechanisms for DNS version 0)
  - [ドメイン名](https://ja.wikipedia.org/wiki/ドメイン名 "wikilink")
      - [トップレベルドメイン](https://ja.wikipedia.org/wiki/トップレベルドメイン "wikilink") (TLD)
      - [国際化ドメイン名](https://ja.wikipedia.org/wiki/国際化ドメイン名 "wikilink")
      - [Fully Qualified Domain Name](https://ja.wikipedia.org/wiki/Fully_Qualified_Domain_Name "wikilink")（FQDN）
  - [地域インターネットレジストリ](https://ja.wikipedia.org/wiki/地域インターネットレジストリ "wikilink")
      - [レジストラ](https://ja.wikipedia.org/wiki/レジストラ "wikilink")
  - [TCP/IP](https://ja.wikipedia.org/wiki/インターネット・プロトコル・スイート "wikilink")
  - [名前解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")
      - [正引き](https://ja.wikipedia.org/wiki/正引き "wikilink")
      - [逆引き](https://ja.wikipedia.org/wiki/逆引き#逆引き（DNS） "wikilink")
  - [ディレクトリ・サービス](https://ja.wikipedia.org/wiki/ディレクトリ・サービス "wikilink")
  - [DNS偽装](https://ja.wikipedia.org/wiki/DNS偽装 "wikilink")
  - [誕生日攻撃](https://ja.wikipedia.org/wiki/誕生日攻撃 "wikilink")
  - [DNS-Pinning](https://ja.wikipedia.org/wiki/DNS-Pinning "wikilink") ([DNSリバインディング](https://ja.wikipedia.org/wiki/DNSリバインディング "wikilink"))
  - [DNS Security Extensions](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink") (DNSSEC)
  - [エニーキャスト](https://ja.wikipedia.org/wiki/エニーキャスト "wikilink")

## 関連プロトコル

  - [STD0013](https://tools.ietf.org/html/std13)
      - RFC 1034 : DOMAIN NAMES - CONCEPTS AND FACILITIES
      - RFC 1035 : DOMAIN NAMES - IMPLEMENTATION AND SPECIFICATION
  - RFC 8310: Usage Profiles for DNS over TLS and DNS over DTLS - [TLS](https://ja.wikipedia.org/wiki/Transport_Layer_Security "wikilink")（TCPを使用）および[DTLS](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink")（UDPを使用）上でDNSメッセージのやり取りを行うプロトコルの規定。セキュリティやプライバシー保護の向上を意図している。
  - RFC 8484: DNS Queries over HTTPS - [HTTPS](https://ja.wikipedia.org/wiki/HTTPS "wikilink")上でDNSメッセージのやり取りを行うプロトコルの規定。使用するHTTPのバージョンとしては[HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")が推奨されている。こちらも、セキュリティやプライバシー保護の向上を意図している。
  - [マルチキャストDNS](https://ja.wikipedia.org/wiki/マルチキャストDNS "wikilink") - mDNS とも表現される
  - [LLMNR](https://ja.wikipedia.org/wiki/LLMNR "wikilink") - Link Local Multicast Name Resolution

## 脚注

## 外部リンク

  - [日本DNSオペレーターズグループ](https://dnsops.jp/)
  - [Google Public DNS](https://dns.google.com/)

[Category:Domain_Name_System](https://ja.wikipedia.org/wiki/Category:Domain_Name_System "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  つまり、ポート53を使わずにポート443を使う。