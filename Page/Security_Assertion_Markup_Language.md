> この記事は[Security Assertion Markup Language](https://ja.wikipedia.org/wiki/Security_Assertion_Markup_Language)から翻訳されています。


**Security Assertion Markup Language**（セキュリティ アサーション マークアップ ランゲージ、略称**SAML**、読み： *sam-el*\[1\]）は[OASISで標準として策定された](../Page/OASIS_\(組織\).md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")で、主に[シングルサインオン](../Page/シングルサインオン.md "wikilink")や[ID連携で利用されている](https://ja.wikipedia.org/wiki/連合アイデンティティ "wikilink")\[2\]。メッセージの送受信には[HTTPや](../Page/Hypertext_Transfer_Protocol.md "wikilink")[SOAPが使われる](../Page/SOAP_\(プロトコル\).md "wikilink")\[3\]。

## 概要

同様の技術として Securant Technologies社が発表した[AuthXML](https://ja.wikipedia.org/wiki/AuthXML "wikilink")とNetegrity社 が発表した[S2ML](https://ja.wikipedia.org/wiki/S2ML "wikilink")という規格があり、SAML はこの二つの規格を統合したものである。

2016年現在の最新版は2005年3月に策定されたSAML v2.0である\[4\]。

SAMLの標準では、[認証](../Page/認証.md "wikilink")、[属性](../Page/属性.md "wikilink")、[権限の認可を](https://ja.wikipedia.org/wiki/認可_\(セキュリティ\) "wikilink")[XMLで](../Page/Extensible_Markup_Language.md "wikilink")**アサーション**（assertion, 直訳：表明）する方法と、これらの情報を伝送するためのプロトコルとに関する[文法と](../Page/形式文法.md "wikilink")[意味論](../Page/意味論.md "wikilink")を定義している\[5\]。

## 概要

### アサーション

**アサーション**(assertion, 直訳：表明)は、SAMLにおける最も基礎的な概念の一つで、これはユーザの[認証](../Page/認証.md "wikilink")情報、[属性](../Page/属性.md "wikilink")、ユーザへの[権限の認可といったセキュリティ情報を](https://ja.wikipedia.org/wiki/認可_\(セキュリティ\) "wikilink")[XML文法で記載したものである](../Page/Extensible_Markup_Language.md "wikilink")\[6\]\[7\]。複数のエンティティの間でアサーションをやり取りする事で前述した[シングルサインオン](../Page/シングルサインオン.md "wikilink")や[ID連携を実現する](https://ja.wikipedia.org/wiki/連合アイデンティティ "wikilink")。

SAMLの標準はアサーションの詳細と、アサーションを伝送するためのプロトコルとに関する[文法と](../Page/形式文法.md "wikilink")[意味論](../Page/意味論.md "wikilink")を定義している\[8\]。

アサーションは**サブジェクト**（subject）に対する**ステートメント**（statements）という形式でセキュリティ情報を記述できる\[9\]。

ここでサブジェクトは何らかの「セキュリティ領域」（security domain）にいるエンティティで、アサートされる対象である\[10\]。サブジェクトは人間であっても会社やコンピューターなどでもよい\[11\]。

ステートメントには以下の三種類がある：

  - **認証ステートメント**（Authentication statements）: ユーザを認証したエンティティが作るステートメントで、例えば認証時刻や認証が行われた場所などの情報を含む\[12\]。
  - **属性ステートメント**（Attribute statements）: サブジェクトの属性に関するステートメント\[13\]。例えばサブジェクトの名前、年齢、性別、ゴールドカードの保持者\[14\]である等。
  - **認可決定ステートメント**（Authorization decision statements）：サブジェクトに何らかの権限を与えた事を表すステートメント\[15\]。例えば特定のファイルへのアクセス権限や、特定の品物を買う事ができる権限\[16\]など。

### パーティとロール

SAMLのユースケースでは最低限以下の２つのパーティが関わる：アサーションを発行する**SAMLアサーションパーティ**（SAML asserting party、直訳：SAML表明当事者）と、アサーションを受信してそれを用いる**SAMLリライングパーティ**（SAML relying party、直訳：SAML依拠当事者）という\[17\]。SAMLアサーションパーティは**SAMLオーソリティ**（SAML authority、直訳：SAML権限者）ともいう\[18\]

多くのユースケースではさらに**ユーザ**が関わる。このユーザ自身がSAMLアサーションパーティであることもある。

上述の２つのパーティやユーザ、もしくはそれ以外のパーティがアサーションの送信を他のパーティに要求するとき、その要求するパーティを**SAMLリクエスター**（SAML requester、直訳：SAML要求者）といい、それに応じてアサーションを送信するパーティを**SAMLレスポンダー**（SAML responder、直訳：SAML応答者）という\[19\]。

SAMLの関係者は様々な**ロール**（役割）を担う。例えばシングルサインオンにSAMLを使う場合にはアイデンティティプロバイダというロールとサービスプロバイダーというロールがある\[20\]。

### シングルサインオンでの利用

**[シングルサインオン](../Page/シングルサインオン.md "wikilink")**は、ユーザが一度認証を受けるだけで複数のサービスやアプリケーションを利用できるようになる仕組みのことである。

SAMLをシングルサインオンで用いるには、ユーザが最初に認証を受けるサイトが**アイデンティティプロバイダ**（identity provider、 **IdP**）というロールを担う\[21\]。そのサイトでのユーザの認証情報やログインセッションのようなセキュリティ情報を**セキュリティコンテクスト**(security context)と呼ぶ\[22\]。

一方、IdPにおけるユーザの認証情報を信頼してサービスやアプリケーションを提供するサイトは**サービスプロバイダー**（service provider、**SP**）というロールを担う\[23\]。

IdPとSPは事前に両者で用いるユーザIDを対応付けることで、IdPのどのユーザがSPのどのユーザと対応しているかを明らかにしておく（すなわち[ID連携しておく](https://ja.wikipedia.org/wiki/連合アイデンティティ "wikilink")）必要がある\[24\]。

ユーザがIdPで認証を受けたあと、SPのサービスを利用しようとすると、IdPはユーザのセキュリティ・コンテクストからアサーションを作成し、アサーションをSPに送る\[25\]。

アサーションには例えばユーザに関する以下の情報が載っている\[26\]：

  - IdPとSPのユーザリストに載っている
  - IdPとの認証で受理された
  - SPが必要とするユーザの属性（年齢、性別、ゴールドカードのメンバーである等）

上で説明したユースケースではユーザはSPにアクセスする前にIdPに認証を受けるフロー（IdP-initiated flow）を説明したが、逆にSPにアクセスした後にIdPから認証を受けるフロー（SP-initiated flow）のほうがより一般的である。というのも検索サイトやブックマークなどから直接SPのサイトにアクセスした場合は、IdPからの認証を受ける前にユーザがSPにアクセスする事になるからである。このためSAMLは両方のフローに対応している\[27\]。

### ID連携での利用

[saml-tech-overview](https://ja.wikipedia.org/wiki/#saml-tech-overview "wikilink")　3.3 Identity Federation Use Caseを参照。

## 関連項目

  - [連合アイデンティティ](https://ja.wikipedia.org/wiki/連合アイデンティティ "wikilink")

  - [OpenID](../Page/OpenID.md "wikilink")

  -
## 外部リンク・参考文献

  -
  -
## 出典

[Category:アイデンティティ管理](https://ja.wikipedia.org/wiki/Category:アイデンティティ管理 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.  [saml-tech-overview](https://ja.wikipedia.org/wiki/#saml-tech-overview "wikilink")　2.1 Drivers of SAML Adoption
3.  [IT用語辞典e-words SAML 【 Security Assertion Markup Language 】](http://e-words.jp/w/SAML.html) 2016年8月10日閲覧
4.  [OASIS Standards](https://www.oasis-open.org/standards#samlv2.0) 2016年8月10日閲覧
5.  [saml-core-2.0-os](https://ja.wikipedia.org/wiki/#saml-core-2.0-os "wikilink") Abstract
6.  [saml-core-2.0-os](https://ja.wikipedia.org/wiki/#saml-core-2.0-os "wikilink") Abstract
7.  [saml-tech-overview](https://ja.wikipedia.org/wiki/#saml-tech-overview "wikilink") 4.3 SAML Components
8.  [saml-core-2.0-os](https://ja.wikipedia.org/wiki/#saml-core-2.0-os "wikilink") Abstract
9.
10.
11.
12.
13.
14.
15.
16.
17. [saml-tech-overview](https://ja.wikipedia.org/wiki/#saml-tech-overview "wikilink")　3.1 SAML Participants
18.
19.
20.
21. [saml-tech-overview](https://ja.wikipedia.org/wiki/#saml-tech-overview "wikilink")　3.2 Web Single Sign-On Use Case
22.
23.
24.
25.
26.
27.