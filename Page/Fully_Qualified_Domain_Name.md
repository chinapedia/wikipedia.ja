> この記事は[Fully Qualified Domain Name](https://ja.wikipedia.org/wiki/Fully_Qualified_Domain_Name)から翻訳されています。


**Fully Qualified Domain Name**（フリー・クオリファイド・ドメイン・ネーム、訳して**完全修飾ドメイン名**（かんぜんしゅうしょくドメインめい））とは、[Domain Name System](../Page/Domain_Name_System.md "wikilink")（DNS）における「[TLDまで完全に指定された](../Page/トップレベルドメイン.md "wikilink")」[ホスト名](../Page/ホスト名.md "wikilink")のことである。一般には**FQDN**と略され、このFQDNで指定された[ホストは](https://ja.wikipedia.org/wiki/ホスト_\(ネットワーク\) "wikilink")、基本的にはそのDNS階層構造（例えば、インターネット）の中で唯一特定することができる、などと不正確に説明されているが正確にはホストは必ずしも一意に定まらない（[\#FQDNとホストは一対一対応ではない](https://ja.wikipedia.org/wiki/#FQDNとホストは一対一対応ではない "wikilink")を参照）。

技術的に特に「世界で唯一に指定される」ことが重要である場合に「[ホスト名](../Page/ホスト名.md "wikilink")」や「[ドメイン名](../Page/ドメイン名.md "wikilink")」と区別して用いるが、一般にはわざわざ区別することはない。

FQDNは[Domain Name Systemに関わる技術用語の一つであるため](../Page/Domain_Name_System.md "wikilink")、詳細に関しては[Domain Name Systemを参照のこと](../Page/Domain_Name_System.md "wikilink")。

## 概要

例えば、`ja.wikipedia.org`がFQDNである。これはドメインが「住所」に例えられることからすれば、国名から番地階数部屋番号まですべてを書くことに相当する（なお、しばしば「インターネット上の住所」という表現がなされているが、インターネット上の住所（インターネットプロトコル（IP）における「住所」）に相当するのはどちらかといえば[IPアドレス](../Page/IPアドレス.md "wikilink")であり、多少なりとも不正確な表現である）。

一般には当然のようにFQDNを使用するが、[イントラネット](../Page/イントラネット.md "wikilink")で組織内のサーバに接続する場合等ではFQDNを使用しないこともある。これは市内に[郵便](https://ja.wikipedia.org/wiki/郵便 "wikilink")を出す場合、宛先をいきなり「朝日町何番地○○」と書いても到着するようなものである。しかし日本全国に[朝日町は沢山あるので一般に住所は県名から記載するであろう](https://ja.wikipedia.org/wiki/朝日町_\(曖昧さ回避\) "wikilink")。インターネットでも同様に、一般にはFQDNを使用する。

厳密には、FQDNには`ja.wikipedia.org.`のように最後にルートを示すドットを付与しなければならない、という説明が見られることがあるが、そもそもFQDNの厳密な定義というものがあるわけではないので正確ではない。RFC の中にもドットをセパレータとする説明がある（RFC 1035の§2.3.1のBNFを参照）。BINDのような[Domain Name Systemの設定や検証をするソフトウェアなどの設定ファイル](../Page/Domain_Name_System.md "wikilink")、その内部のデータベースなどで、ドメイン`wikipedia.org`とそのサブドメイン`ja.wikipedia.org`を設定するのに、`wikipedia.org.`と`ja`のように終端にドットを付けてトップレベルからのドメインを、終端にドットを付けずにサブドメインを指定する、という便法（参考: RFC 1034 §3.1、RFC 1035 §3.5・§5 、ユーザーがよく見るものではdigコマンドの応答）があり、終端にドットを付けるものをRFC 1035ではabsoluteと呼んでおり、『DNS\&BIND』（通称：バッタ本）では、絶対ドメイン名をFQDNとも呼ぶ、と説明している。

LAN内のマシンをfully qualifiedでないホスト名だけでアクセスしたり、`org.`をTLDと認識したりするのは、基本的にはクライアントないしリゾルバの内部での（たとえばUnixならresolv.confのdomainオプションなどの設定による）処理によるものである。

## FQDNとホストは一対一対応ではない

そもそも「FQDNとホストは一対一対応ではない」以前に、ネットワークインタフェースを複数持っているようなホストのことを考えれば、[IPアドレス](../Page/IPアドレス.md "wikilink")とホストですら一対一対応ではない。よって「FQDNとホストは一対一対応ではない」ということについての説明は、それだけで基本的には終了する。

厳密に言うとFQDNは、[Domain Name Systemに対して問い合わせを行なう際に使用する](../Page/Domain_Name_System.md "wikilink")**単なる名前**である。Domain Name Systemが回答としてIPアドレスを返せるなら、ドメインの管理責任者が望むどんなことでも可能である。

部屋に例えれば、同じ部屋に「菊の間」と「薔薇の間」との複数の名前を与えることもでき、また複数の部屋全てを「VIPルーム」という同じ名前にすることもできる。

### バーチャルホスト

バーチャルホストとは、一つのホストを複数のFQDNに対応付ける技術である。システムを構成するサーバの台数が少ない場合にホストを増やしたように見せかけることができることから、将来的にはホストを増設することを視野に入れた上で初期投資を少なくする手段としても多用されている。例えるなら、社長が一人で営業と経理と人事をこなしているような会社に届く郵便物の宛先に「経理ご担当者様」と書いてあるようなものである。

なお、一つのホストに複数のIPアドレスを与えるのもバーチャルホストという場合がある。これは[マルチホーム](https://ja.wikipedia.org/wiki/マルチホーム "wikilink")とは異なる概念である。

### DNSラウンドロビン

DNSラウンドロビンとは、一つのFQDNを複数のホスト（≒IPアドレス）に対応させて毎回違うIPアドレスを返答するようにした技術である。一見意味不明な技術であるが、慎重に計画した上で実施すれば有効な[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")となる。例えるなら、会社に届いた郵便物の宛先が「経理ご担当者様」となっていたとしても、実際に経理課の誰が読むかはわからない（が誰が読んでも問題は起こらないようになっている）ような状態である。

特に[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")における[Webサーバ層で威力を発揮する](https://ja.wikipedia.org/wiki/アプリケーションサーバ#Web3層構成 "wikilink")。

## 関連項目

  - [Domain Name System](../Page/Domain_Name_System.md "wikilink")
  - [BIND](../Page/BIND.md "wikilink")
  - [トップレベルドメイン](../Page/トップレベルドメイン.md "wikilink")
  - [国際化ドメイン名](../Page/国際化ドメイン名.md "wikilink")
  - [サーバ](../Page/サーバ.md "wikilink")

[de:Domain\#Fully Qualified Domain Name (FQDN)](https://ja.wikipedia.org/wiki/de:Domain#Fully_Qualified_Domain_Name_\(FQDN\) "wikilink")

[Category:Domain_Name_System](https://ja.wikipedia.org/wiki/Category:Domain_Name_System "wikilink") [Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink")