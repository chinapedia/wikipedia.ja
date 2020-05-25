> この記事は[Lightweight Directory Access Protocol](https://ja.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol)から翻訳されています。


**Lightweight Directory Access Protocol**（ライトウェイト ディレクトリ アクセス プロトコル、**LDAP**：エルダップ）は、[ディレクトリ・サービス](../Page/ディレクトリ・サービス.md "wikilink")に接続するために使用される[通信プロトコル](../Page/通信プロトコル.md "wikilink")の一つ。

## 概要

[ITU勧告](../Page/国際電気通信連合.md "wikilink")[X.500](../Page/X.500.md "wikilink")モデルをサポートする[ディレクトリ](../Page/ディレクトリ.md "wikilink")に対するアクセスを提供するために設計された。 一方で、X.500ディレクトリアクセスプロトコル(Directory Access Protocol : DAP)の資源要求は課されない。 本プロトコルは、特にディレクトリに対する対話的な読み込み/書き込み(read/write)アクセスを提供する管理アプリケーションやブラウザアプリケーションを対象とする。 X.500プロトコルをサポートするディレクトリと共に使用する際に、X.500のDAPを補完するものとなることが意図されている。

[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")では、ネットワークを構成する機器が多くなるにつれて扱うべきネットワーク・リソースが増大する。 DAP が登場した背景には、個々に異なる[ディレクトリ・サービス](../Page/ディレクトリ・サービス.md "wikilink")を扱うよりも、統一されたプロトコルで拡張可能な情報にアクセスする方法が求められるようになったことが挙げられる。 上述の X.500 シリーズは、分散可能な統合案内サービスとして優れた機能を有していたものの、DAP が複雑なため処理が重たく、[TCP/IP](../Page/インターネット・プロトコル・スイート.md "wikilink") による[インターネット](../Page/インターネット.md "wikilink")では使用されにくいという欠点があった。

「X.500の90%の機能を10%のコストで実現する」というキャッチフレーズのもと、DAPの問題点を洗い出し、再設計が行われたLDAPv2が[IETFによって](../Page/Internet_Engineering_Task_Force.md "wikilink") RFC 1777 として標準化された。LDAPv2 では、LDAP サーバは X.500 の[フロントエンド](../Page/フロントエンド.md "wikilink")として機能し、分散化は X.500 が担っている。

LDAPv2は、その後分散化を実現するLDAPv2+、さらに国際化やセキュリティ強化がなされたLDAPv3（RFC 2251）へと進化している。

LDAP の処理系は、[OpenLDAP](https://ja.wikipedia.org/wiki/OpenLDAP "wikilink") により、[オープンソース](../Page/オープンソース.md "wikilink")で提供されているものをはじめ、各種の製品が存在している。

## LDAPとX.500の違い

LDAPはX.500のDAPを軽量化したものである。

しかし、X.500ではDAP以外にDSP,DOP,DISPといったプロトコルが規定されている。

つまりLDAPにはこの3つのプロトコルが存在しないことになる。

  - DUA(Directory User Agent):ディレクトリの利用者に代わってディレクトリにアクセスする機能（プログラムやコマンド、ライブラリ）
  - DSA(Directory Service Agent):ディレクトリ情報を管理する個々のシステム。ディレクトリはDSAの集合体として構成される。
  - DAP(Directory Access Protocol):DSAがDUAに対してディレクトリサービスを提供するためのプロトコル
  - DSP(Directory System Protocol):DSA間で分散協調動作（連鎖や紹介）を行うためのプロトコル
  - DOP(Directory Operational binding management Protocol):ディレクトリ運用結合管理プロトコル。DSA間の運用結合の規定内容や状態の交換に用いられるプロトコル
  - DISP(Directory Information Shadowing Protocol):DSA間で複製情報を交換するためのプロトコル

X.500のDAPはOSI各層の標準プロトコルを使用する。

LDAPはTCP/IPの上に実装されるため、DAPにあるROSE,RTSE,ACSEを実装していない。

（これらの機能はTCP/IPの中で実装されているのでLDAPでは不要）

  - ROSE(Remote Operation Service Element):遠隔操作サービス要素、処理の依頼と結果の通知という通信メカニズムを実現するプロトコル要素
  - RTSE(Reliable Transfer Service Element):高信頼転送サービス要素、通信経路障害などによって情報の欠落や重複が起きないようにするプロトコル要素
  - ACSE(Association Control Service Element):アソシエーション制御サービス要素、コネクションの確立、正常開放、異常解放を行うサービス要素

## 代表的なLDAP実装

  - [NetIQ eDirectory](https://ja.wikipedia.org/wiki/NetIQ_eDirectory "wikilink") ([NetIQ](https://ja.wikipedia.org/wiki/NetIQ "wikilink"))
  - [Oracle Internet Directory](http://otn.oracle.co.jp/products/oid/index.html)（[オラクル](../Page/オラクル_\(企業\).md "wikilink")）
  - [Sun Java System Directory Server](http://jp.sun.com/practice/software/identity/jp/directory_srvr_ee/)（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）
  - [Sun OpenDS](http://www.opends.org/)（サン・マイクロシステムズ）
  - StarDirectory（[日本電気](../Page/日本電気.md "wikilink")）
  - 389 Directory Server（[レッドハット](../Page/レッドハット.md "wikilink")）
  - InfoDirectory（[富士通](../Page/富士通.md "wikilink")）
  - [Sendmail Directory Server](http://www.proofpoint.com/us/node/4053)
  - [OpenLDAP](https://ja.wikipedia.org/wiki/OpenLDAP "wikilink")
  - [Tivoli](../Page/Tivoli.md "wikilink") Directory Server ([IBM](../Page/IBM.md "wikilink"))
  - [Active Directory](../Page/Active_Directory.md "wikilink")（[マイクロソフト](../Page/マイクロソフト.md "wikilink")）

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")