> この記事は[DNSサーバ](https://ja.wikipedia.org/wiki/DNSサーバ)から翻訳されています。


**DNSサーバ**（ディーエヌエスサーバ）は、[コンピュータ・ネットワークにおいて](../Page/コンピュータネットワーク.md "wikilink")、[Domain Name System](../Page/Domain_Name_System.md "wikilink")（DNS）の「名前解決」機能が実装された[サーバ](../Page/サーバ.md "wikilink")である。

## 概要

DNSサーバには、後述するように2種類があり、それぞれ全く異なる働きをするので、「DNSサーバはこのようなことを行う」と説明することはできない。そのためここでは、Domain Name Systemの役割をまず説明する。

インターネットでの通信に際し、URLの中やメールアドレスの中などでの相手先は、[IPアドレス](../Page/IPアドレス.md "wikilink")が直接指定されることはまず無く、[ドメイン名](../Page/ドメイン名.md "wikilink")などといった「名前」が使われている。そういった名前から、IPアドレスなど\[1\]を得る「解決」を行うシステムがDomain Name Systemである。

あるコンピューターが他のコンピュータと[インターネットプロトコル](https://ja.wikipedia.org/wiki/インターネットプロトコル "wikilink")（IP）を介して通信する際には、通信の相手となるコンピュータに付与されたIPアドレスを知る必要がある。一方、URLなどには（IPアドレスを、直接指定することもできるが）、もっぱら[ドメイン名](../Page/ドメイン名.md "wikilink")を使って対象を記述する。ドメイン名から、IPアドレスなどといった必要な情報を得る（名前を解決する）ために、ネットワーク上で情報を提供する仕組みがDomain Name Systemであり、それを担う各サーバがDNSサーバである。

DNSサーバは[分散型データベース](https://ja.wikipedia.org/wiki/分散型データベース "wikilink")の1ノードとして機能している。DNSサーバには以下の2種類がある。

  - [\#DNSコンテンツサーバ](https://ja.wikipedia.org/wiki/#DNSコンテンツサーバ "wikilink") - 自らの「ゾーン」（ドメイン名空間）について、情報を管理し問い合わせに回答する。独自のドメイン名をドメインレジストラで登録する際、「そのドメイン名を管理するDNSサーバ」として指定するのがDNSコンテンツサーバである。
      - 社内専用など、一般に公開しないゾーンを管理するコンテンツサーバというようなものもある。当然ながら、レジストラへの登録の必要はない。
      - コンテンツサーバについては、「権威DNSサーバ」という用語もある。コンテンツサーバという語は上記のような役割のサーバ全般の総称であるのに対し、権威DNSサーバは例えば「wikipedia.orgドメインの（wikipedia.orgドメインが管理・委譲している情報を持っている（それに関して権威がある））権威DNSサーバ」といったように、個々のドメインとの関係を意味する。
  - [\#DNSキャッシュサーバ](https://ja.wikipedia.org/wiki/#DNSキャッシュサーバ "wikilink") - 依頼された問い合わせに応じて、コンテンツサーバへ必要な問い合わせを行い、結果を依頼元に返す。結果を再利用できるよう、一定期間自らキャッシュする。
      - フルリゾルバ・フルサービスリゾルバ・キャッシュDNSサーバとも呼ばれる。

DNSサーバが持つ「**ゾーン情報**」（ゾーンファイル）を他のDNSサーバから取得し、同期する仕組みを「**[DNSゾーン転送](https://ja.wikipedia.org/wiki/DNSゾーン転送 "wikilink")**」と言う。

## コンテンツサーバとキャッシュサーバ

DNSサーバは、ドメインの持ち主が情報を提供するための「**DNSコンテンツサーバ**」と、ネットワークの利用者（ドメイン名システム（DNS）の利用者）が名前解決に利用するための「**DNSキャッシュサーバ**」の２種類に大別できる。

**両者は全く違うもの**なので**混同してはならない**し、コンテンツサーバはドメインの持ち主が管理することもできるが、多くの場合、プロバイダやレンタルサーバ業者などが提供しているものを利用する\[2\]。キャッシュサーバは、接続プロバイダなどがほとんどの場合に用意しており、「インターネットを利用するための機器の設定」にその設定が含まれていたり、あるいはDHCPでIPアドレス等と一緒に自動的に設定してしまうことが専らであるが、ユーザのLAN内に（あるいは端末自身の中のサーバとして）用意して、そちらを使うこともできる（分散システム的な観点からは、そのほうが望ましい）。DNSの仕組み上キャッシュすることが前提の設計になっているため、キャッシュを持っていて「キャッシュサーバ」と専ら呼ばれるのであるが、中継するのみでキャッシュしない、いわゆるプロキシ的な動作をするものもある。

## DNSコンテンツサーバ

DNSコンテンツサーバの役割は、[Domain Name Systemにおいて](../Page/Domain_Name_System.md "wikilink")、ドメインの管理情報、すなわち、自ゾーンの管理するサーバのIPアドレスなどの各種リソースレコード(RR)と、ドメインの委任に関する情報を保持し、問い合わせ要求があったときに応答することである。

DNSサーバが保持する「ゾーン情報」（ゾーンファイル）内の**リソースレコード**（資源レコード）の種類の例を以下に示す。

  - リソースレコードの例

<!-- end list -->

  - Aレコード

<!-- end list -->

  -
    名前に対する[IPv4](../Page/IPv4.md "wikilink")アドレス

<!-- end list -->

  - AAAAレコード

<!-- end list -->

  -
    名前に対する[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")アドレス

<!-- end list -->

  - PTRレコード

<!-- end list -->

  -
    逆引き（IPアドレスに対する名前）たとえば 198.51.100.234 というIPアドレスを逆引きするには 234.100.51.198.in-addr.arpa という名前のPTRレコードを問い合わせればよい

<!-- end list -->

  - NSレコード

<!-- end list -->

  -
    そのゾーンの権威あるDNSコンテンツサーバの名前

<!-- end list -->

  - MXレコード

<!-- end list -->

  -

    そのゾーンのメールサーバの名前

<!-- end list -->

  - SOAレコード

<!-- end list -->

  -
    ゾーンそのものの情報

<!-- end list -->

  - CNAMEレコード

<!-- end list -->

  -
    　その名前に対する別名

<!-- end list -->

  - TXTレコード

<!-- end list -->

  -
    テキスト情報

<!-- end list -->

  - DNSKEYレコード/RRSIGレコード

<!-- end list -->

  -
    [DNSSECのための公開錠](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink")/署名

など。

  - wikipedia.orgのDNSコンテンツサーバの例
    このDNSコンテンツサーバは、ja.wikipedia.orgやwww.wikipedia.orgなどwikipedia.orgゾーンの各種リソースレコードを保持している。ただし、orgゾーンに保持されているIPアドレスは知らない（間違った設定によってorgのNSレコードをキャッシュで答えてしまうサーバも実際には多く存在する）。このDNSコンテンツサーバは、ja.wikipedia.orgのIPアドレスを教えるよう要求を受けると、自らが保持しているコンテンツから、ja.wikipedia.orgのIPアドレスを探し、その情報を含めた返答を返す。

なお、[ドメイン名](../Page/ドメイン名.md "wikilink")から[IPアドレス](../Page/IPアドレス.md "wikilink")を検索する事を[正引き](https://ja.wikipedia.org/wiki/正引き "wikilink")と呼び、反対にIPアドレスからドメイン名を検索することを[逆引き](../Page/逆引き.md "wikilink")と呼ぶ。

### プライマリサーバとセカンダリサーバ

コンテンツサーバの役割での「プライマリサーバ」と「セカンダリサーバ」は、マスタとスレーブの関係にある。類似の用語である、オペレーティングシステムのネットワーク構成で指定する「DNSサーバ設定」の「優先」「代替」とは全く無関係であり、混同しないよう注意したい（[\#OSで指定する「DNSサーバ」](https://ja.wikipedia.org/wiki/#OSで指定する「DNSサーバ」 "wikilink")）。

  - プライマリサーバ:ゾーン情報を自ら管理し、自らのゾーン情報に関する問い合わせに回答したり、セカンダリサーバへ配信したりする。[Windows Server同梱のDNSサービスにある動作モード](../Page/Windows_Server.md "wikilink")「[Active Directory統合ゾーン](../Page/Active_Directory.md "wikilink")」は、プライマリサーバとしての役割に機能拡張\[3\]がされたものである。
    セカンダリサーバ:担当するゾーンに関する問い合わせに回答するが、自らはゾーン情報を管理せずプライマリサーバから受け取ったゾーン情報を保持している。

### セキュリティ

DNSサーバが応答不能になれば、管理しているゾーン内のコンピューターが提供しているサービスを利用できなくなり、誤った情報を回答するとクライアントコンピューターは意図していないノードにアクセスしてしまう\[4\]ことになる。

健全な利用環境を確保するために、DNSサーバのリソースレコードの改ざんや[DoS攻撃](../Page/DoS攻撃.md "wikilink")を防ぐよう、DNSサーバソフトウエアおよびOSの設定やセキュリティ更新プログラムの適用、コンテンツサーバの多重化（セカンダリサーバを公開し、プライマリサーバは非公開とするなど）、[ファイアウォール](../Page/ファイアウォール.md "wikilink")や[侵入防止システム](https://ja.wikipedia.org/wiki/侵入防止システム "wikilink")の導入などにより対策を講じる必要がある。

電子署名を用いてDNSの応答が正しいことを検証する「[DNSSEC](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink")」機能が提供されている。

#### KSKロールオーバー問題

DNSSECにおいて、電子署名の正当性検証に使われる最上位の暗号鍵である「ルートゾーンKSK」を更新する際に、EDNSによるIPフラグメンテーションが発生するほどのサイズの応答データが発生するが、通信設定が対応できていないDNSで通信ができず、DNSSECによる正当性検証ができなくなり、インターネットの利用に問題が発生する。

これは、「ルートゾーンKSK」が2016年まで更新されてこなかったために問題になっていなかったが、2016年10月から2018年3月にかけて、 順次変更を行うことになったために顕在化した問題である。特に2017/09/19、2017/12/20、2018/01/11から始まる更新では、IPフラグメンテーションが発生しない1280bytesを超える1414～1424Bytesの応答データが発生するために、問題が発生する。

基本的には、DNSの運用責任者がソフトウェアのアップデートや設定変更で対応すべきものであるが、一般消費者向けのルータに内蔵されているDNS Proxyでも問題が発生する可能性があり、インターネットの利用に問題が発生する場合がある。

## DNSキャッシュサーバ

DNSキャッシュサーバの役割は、DNSクライアント（ウェブブラウザなど、ドメイン名を利用する何らかのアプリケーション等）からの再帰的問い合わせによって名前解決の依頼を受け、非再帰的問い合わせを行い名前を解決することである。たとえば、Webブラウザで、www.wikipedia.orgなどを入力した際、そのコンピュータがまず名前解決しに行くのがDNSキャッシュサーバである。

DNSキャッシュサーバ自身については、直接なんらかの方法でそのIPアドレスを設定する。近年のLinux環境などでの典型としては、ネットワークインタフェースの立ち上げ時に、[DHCPによって受け取ったかネットワーク設定スクリプトに書き込まれているものが](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、設定ファイル（典型的には `/etc/resolv.conf` ）に書き込まれる。あるいは古典的には `/etc/resolv.conf` は静的な設定ファイルであった。

### 再帰的問い合わせと非再帰的問い合わせ

名前解決における問い合わせには、再帰的問い合わせと非再帰的問い合わせ（反復問い合わせ）の2種類がある。典型的で単純な例で説明すると、ユーザプログラムからlibcの `gethostbyname` (3) を通して、`/etc/resolv.conf` で設定されたDNSキャッシュサーバへの問い合わせが再帰的問い合わせで、キャッシュサーバが行う、DNSコンテンツサーバ群への繰返しの問い合わせが非再帰的問い合わせである。

  - 再帰的問い合わせ:名前解決がされたのであれば、その完全な結果を、できなかった場合は「存在しない」とするやはり完全な結果を求める問い合わせである。ユーザのパーソナルコンピュータなどといった端末から、DNSキャッシュサーバに対して送られる。

<!-- end list -->

  - 非再帰的問い合わせ:反復問い合わせとも。この問い合わせを受けたDNSコンテンツサーバは、自分自身が持っている情報であればそれを、委任している情報であればそのこと（委任情報）を返す。DNSキャッシュサーバはその内容に応じて次々と問い合わせを反復する（一般的には[ルートサーバ](../Page/ルートサーバ.md "wikilink")から順にドメインツリーをたどる）。

## 実装

代表的なDNSサーバソフトウエアは次のものがある。 DNSサーバの中には、DNSコンテンツサーバとDNSキャッシュサーバが別々になっているものもあれば、両方機能を搭載するものもある。

  - [BIND](../Page/BIND.md "wikilink")
  - [djbdns](https://ja.wikipedia.org/wiki/djbdns "wikilink") - コンテンツサーバであるtinydnsとキャッシュサーバであるdnscacheからなる
  - [Dnsmasq](https://ja.wikipedia.org/wiki/Dnsmasq "wikilink")
  - [Microsoft DNS Server](https://ja.wikipedia.org/wiki/Microsoft_DNS_Server "wikilink")
  - [NSD](https://ja.wikipedia.org/wiki/NSD_\(ソフトウェア\) "wikilink")
  - [Unbound](https://ja.wikipedia.org/wiki/Unbound "wikilink")
  - [Knot DNS](https://ja.wikipedia.org/wiki/Knot_DNS "wikilink")
  - [PowerDNS](../Page/PowerDNS.md "wikilink")
  - [Yadifa](https://ja.wikipedia.org/wiki/Yadifa "wikilink")
  - XACK DNS - 国産のDNS製品

## 端末で指定する「DNSサーバ」

PCに搭載される[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、携帯端末に搭載される[IOSや](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink")[Androidをはじめとする](../Page/Android_\(オペレーティングシステム\).md "wikilink")、ネットワーク通信可能なオペレーティングシステムには、ネットワーク関連の設定に「DNSサーバ」のIPアドレスを指定する項目がある\[5\]。一般に gethostbyname(3) といったようなライブラリ関数による処理の中で\[6\]、これらの設定に従い、DNSキャッシュサーバへの問い合わせ等が行われる。

これらの情報は、DHCPによる管理下にあるネットワークでは、[DHCP](https://ja.wikipedia.org/wiki/DHCP "wikilink")サーバから（割当IPアドレス情報とあわせて）受け取ることが可能である場合もある\[7\]。管理ポリシーによっては、それに従うよう要求されている場合もある。

大抵、複数のDNSサーバを指定可能になっている。DNSサーバへ問い合わせる際に優先順位の高い順に行い、応答がない場合（該当DNSサーバが停止、通信経路で障害発生など）に次位（代替）以降のDNSサーバへ問い合わせを行うようになっている。

## 脚注

<references />

## 外部リンク

  - [情報処理推進機構：DNSキャッシュポイズニングの脆弱性に関する注意喚起](https://www.ipa.go.jp/security/vuln/documents/2008/200809_DNS.html)
  - [日本DNSオペレーターズグループ](https://dnsops.jp/)
  - [JP DNS Web Page](http://www.dns.jp/)

## 関連項目

  - [Domain Name System](../Page/Domain_Name_System.md "wikilink")
  - [ダイナミックドメインネームシステム](../Page/ダイナミックドメインネームシステム.md "wikilink")
  - [リゾルバ](../Page/リゾルバ.md "wikilink")
  - [DNSルートゾーン](https://ja.wikipedia.org/wiki/DNSルートゾーン "wikilink")
  - [DNS over HTTPS](https://ja.wikipedia.org/wiki/DNS_over_HTTPS "wikilink")
  - [DNS64](https://ja.wikipedia.org/wiki/DNS64 "wikilink")
  - [1.1.1.1](https://ja.wikipedia.org/wiki/1.1.1.1 "wikilink")
  - [OpenDNS](https://ja.wikipedia.org/wiki/OpenDNS "wikilink")
  - [Google Public DNS](https://ja.wikipedia.org/wiki/Google_Public_DNS "wikilink")

[de:Domain Name System\#Nameserver](https://ja.wikipedia.org/wiki/de:Domain_Name_System#Nameserver "wikilink")

[Category:Domain_Name_System](https://ja.wikipedia.org/wiki/Category:Domain_Name_System "wikilink") [Category:サーバ](https://ja.wikipedia.org/wiki/Category:サーバ "wikilink")

1.  MXレコードなどはIPアドレス以外に解決される。他にも近年はメイルの返信元の真正性確認などに使われるTXTフィールドなどがある。設計上は任意の拡張が容易なように作られている（たとえば、IPv6のために追加されたAAAAレコードなど）。
2.  特に、可用性を上げるためのセカンダリサーバは、上流のネットワークなどができるだけ別系統であることが望ましく、2系統のネットワークを持たない場合などには外部に出すのが現実的なことが多い。
3.  <http://technet.microsoft.com/ja-jp/library/cc731204.aspx>
4.  フィッシングサイトなど悪意のあるウェブサーバへ誘導されてしまったり、メールの転送先を変更され窃取されたりすることになる。
5.  Windowsでは、[コントロールパネル](https://ja.wikipedia.org/wiki/コントロールパネル "wikilink")のネットワーク設定、macOSでは「システム環境設定」の「ネットワーク」、Unix系では`/etc/resolve.conf`など
6.  「オペレーティングシステムが名前解決を必要とした際」ではない。
7.  DHCPサーバから得た情報で設定する場合の指定項目は「DNSサーバのアドレスを自動的に取得する」などと表現されている。