> この記事は[Extensible Resource Identifier](https://ja.wikipedia.org/wiki/Extensible_Resource_Identifier)から翻訳されています。


**Extensible Resource Identifier**（**XRI**）とは、[OASISの](https://ja.wikipedia.org/wiki/OASIS_\(組織\) "wikilink") [XRI Technical Committee](http://www.oasis-open.org/committees/xri) が策定中の規格であり、[Uniform Resource Identifier](../Page/Uniform_Resource_Identifier.md "wikilink") および [Internationalized Resource Identifier](https://ja.wikipedia.org/wiki/Internationalized_Resource_Identifier "wikilink") と互換性のある抽象識別子の方式と解決プロトコルである。XRIの目標は、ドメイン・地域・用途・転送手段によらない抽象化・構造化識別子の標準構文と探索フォーマットとなることであり、任意のドメイン、ディレクトリ、プロトコルをまたいで共有可能な識別子となることを意図している。

2008年5月のOASIS Standard Vote では、史上有数の投票率を見たが、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") Technical Architecture Group (TAG) などの反対によって\[1\]\[2\]、賛成73票に対し反対25票と1票差で否決された\[3\]\[4\]（賛成票が反対票の3倍なければ可決にならない）。論争の核心は、TAG は広く相互運用可能な [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") URI が抽象化・構造化識別子としても機能すると信じているのに対して\[5\]、XRI Technical Committee はそれに限界があるとし、その対処としてXRIがあるとしている点である\[6\]。

## 背景

[URI](../Page/Uniform_Resource_Identifier.md "wikilink") は[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上で広く使われている。しかし、Webの発展によって、標準のURI構文では容易には対応できないリソース識別子への要求が出てきた。特に重要な要求は「国際化」であり、[W3Cと](../Page/World_Wide_Web_Consortium.md "wikilink")[IETFはこれに応えるため](../Page/Internet_Engineering_Task_Force.md "wikilink")、URIを拡張した [Internationalized Resource Identifier](https://ja.wikipedia.org/wiki/Internationalized_Resource_Identifier "wikilink") (IRI) を策定した。IRIはURIで使用する文字セットを[Unicode](../Page/Unicode.md "wikilink")全体に拡大することで構築されている。

[XMLや](../Page/Extensible_Markup_Language.md "wikilink")[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")などによるWebの自動化（マシン同士の通信）が拡大すると共に、特定の物理ネットワーク経路、位置、プロトコルに依存せずにリソースを識別できることが重要になってきた。それは、以下のような理由による。

  - XML文書がドメインに依存しない[自己言及](https://ja.wikipedia.org/wiki/自己言及 "wikilink")的データフォーマットであるのと同じように、自己言及的「タグ」を持ち、ドメインをまたいで理解される構造化識別子を生成するため。
  - リソースのネットワーク上の位置が変化しても保持される永続的リンクを作るため。
  - 識別子の管理を代表セグメント（"xxx://" の直後に続くセグメント）だけで行うのではなく、識別子のパスのどこでも可能にするため。
  - あるドメインであるリソースを識別するのに使っている識別子を同じドメイン内での別名にマッピングしたり、他のドメインでの識別子とマッピングするため。

2003年初め、これらの要求を受けて[OASISが新たな技術委員会](https://ja.wikipedia.org/wiki/OASIS_\(組織\) "wikilink") (TC) を創設し、[IRI仕様に基づいて新たな識別子の仕様を策定することになった](https://ja.wikipedia.org/wiki/Internationalized_Resource_Identifier "wikilink")。XRI は、他にも HTTP(S) に基づく解決プロトコルと単純なXML文書仕様 [XRDS](https://ja.wikipedia.org/wiki/XRDS "wikilink") (Extensible Resource Descriptor Sequence) も策定した。

## 機能

  - [URIおよび](../Page/Uniform_Resource_Identifier.md "wikilink")[IRIとの互換性](https://ja.wikipedia.org/wiki/Internationalized_Resource_Identifier "wikilink") - XRIは URI や IRI が必要とされる場面で使うことができる。
  - 相互参照 - XRIは別のXRI（や URI）を含むことができ、何重にも入れ子可能である。これによって XML がドメイン間のデータ共有を可能にしているように、ドメイン間で識別子を共有可能にする構造化識別子を構築できる。
  - グローバルコンテキスト記号 - "="、"@"、"+"、"$"、"\!" といった記号で、[i-name](https://ja.wikipedia.org/wiki/i-name "wikilink") や [i-number](https://ja.wikipedia.org/wiki/i-number "wikilink") のグローバルコンテキストを人間にも分かりやすく示す。これは必須ではないが、その意味や使い方に合意したコミュニティで使われる。
  - [Peer to Peer](../Page/Peer_to_Peer.md "wikilink") アドレッシング - XRI構文規則では、2つのネットワークノード間で相互にXRIを割り当て、相互解決する能力をサポートしている。すなわち、トップレベルの名前空間オーソリティを第三者が割り当てた名前で参照できることを意味する。これにより、組織間やコミュニティ間で名前空間の連合を可能にする。
  - 分散化 - XRI は集中型アドレッシングシステム（例えば、IPアドレスとDNS）で運用することもできるし、分散型のオーソリティと Peer to Peer のアドレッシングで運用することもできる。
  - 委任 - 名前空間を他の名前空間オーソリティに委任することができる。
  - 連合 - 任意のレベルでそれぞれ独立に定義された名前空間を階層的または並立的に結合することができ、解決可能にできる。
  - 永続性 - XRIの一部（または全部）が永久的な識別子であって決して再割り当てされないと意思表示することができる。
  - 人間が扱いやすいフォーマットと機械が扱いやすいフォーマット - 人間が覚えやすい形式の識別子（[i-name](https://ja.wikipedia.org/wiki/i-name "wikilink")）と機械が処理しやすいよう最適化された形式の識別子（[i-number](https://ja.wikipedia.org/wiki/i-number "wikilink")）がある。
  - 単純で拡張可能な解決 - HTTP と単純なXML文書仕様 XRDS を使った軽量な解決手法を提供している。
  - Trusted Resolution - XRI解決プロトコルには、3つの信頼できるバージョンがある（HTTPS、[SAML](https://ja.wikipedia.org/wiki/Security_Assertion_Markup_Language "wikilink")、両方）。
  - Multiple resolution options - XRIの解決はDNSとは独立に実施できる。
  - [IRI仕様を包含しているので](https://ja.wikipedia.org/wiki/Internationalized_Resource_Identifier "wikilink")、[国際化を実現している](../Page/国際化と地域化.md "wikilink")。
  - 特定の転送プロトコルや機構に制限されない。

## XRI 相互参照構文の例

ISBN名前空間にURNを使ったライブラリシステムで、本を特定しその本がある図書館のDNSサブドメインを特定する。HTTP URI 構文では、図書館を表すDNS名のコンテキストでは、本の題名をURNで表す標準的方法は存在しない。XRI相互参照は、任意の図書館にある任意の本を特定するためのXRIをプログラム的に構築できる。以下に例を示す。

` `<xri://broadview.library.example.com/(urn:isbn:0-395-36341-1>`)`
` `<xri://shoreline.library.example.com/(urn:isbn:0-395-36341-1>`)`
` `<xri://northgate.library.example.com/(urn:isbn:0-395-36341-1>`)`

これを自己言及的識別子に拡張することができる。例えば、それぞれの本の形態を示したいとする。その場合は、以下のようにメタデータを含むXRIにする。

` `<xri://broadview.library.example.com/(urn:isbn:0-395-36341-1)/(+hardcover)>
` `<xri://broadview.library.example.com/(urn:isbn:0-395-36341-1)/(+softcover)>
` `<xri://broadview.library.example.com/(urn:isbn:0-395-36341-1)/(+reference)>

## XRI 2.0 構文の例

以下の例では、"<xri://>" というプレフィックスがないが、XRI では URI 正規形でない場合はプレフィックスはオプションとされている。つまり、これらはXRI形式とURI形式の間の変換をしたものではない。

全体が再割り当て可能なセグメントで構成されているXRIの例:

` =Mary.Jones`
` @Jones.and.Company`
` +phone.number`
` +phone.number/(+area.code)`
` =Mary.Jones/(+phone.number)`
` @Jones.and.Company/(+phone.number)`
` @Jones.and.Company/((+phone.number)/(+area.code))`

全体が永続性セグメントで構成されているXRIの例:

` =!13cf.4da5.9371.a7c5`
` @!280d.3822.17bf.ca48!78d2/!12`

永続性セグメントと再割り当て可能セグメントが混在するXRIの例:

` =!13cf.4da5.9371.a7c5/(+phone.number)`
` @Jones.and.Company!78d2/!12/(+area.code)`

## 応用

XRI基盤を使って開発されている応用の例:

  - [OpenID](../Page/OpenID.md "wikilink") 2.0 の 識別子発見 (identifier discovery) では XRI を根幹技術とし、[XRDS](https://ja.wikipedia.org/wiki/XRDS "wikilink") を使う。
  - [Higgins Project](https://ja.wikipedia.org/wiki/:en:Higgins_project "wikilink") は、XRI と XRDS を採用している。
  - [XDI.org](http://www.xdi.org) の [i-name](https://ja.wikipedia.org/wiki/i-name "wikilink") および [i-number](https://ja.wikipedia.org/wiki/i-number "wikilink") というデジタルアイデンティティ・アドレッシングサービス
  - [XDI](https://ja.wikipedia.org/wiki/XDI "wikilink") データ共有プロトコル（OASIS [XDI Technical Committee](http://www.oasis-open.org/committees/xdi) で開発中）

## ライセンス

XRI Technical Committee は [RF on Limited Terms Mode of the OASIS IPR policy](http://www.oasis-open.org/committees/xri/ipr.php) で運営されている。

一部の人々が指摘しているように、XRI で使われている技術には特許権が設定されているものがあり、それら特許のライセンス権は非営利組織である [XDI.org](http://www.xdi.org) に与えられ、その組織が特許の非独占的使用権を本来の特許所有者が許可した組織にライセンス供与している。

## 脚注

## 関連項目

  - [i-name](https://ja.wikipedia.org/wiki/i-name "wikilink")
  - [ザナドゥ計画](https://ja.wikipedia.org/wiki/ザナドゥ計画 "wikilink")

## 外部リンク

  - [OASIS XRI Technical Committee](http://www.oasis-open.org/committees/xri):
      - [XRI Syntax 2.0 Committee Specification](http://www.oasis-open.org/committees/download.php/15377)
      - [XRI Resolution 2.0 Committee Specification](http://docs.oasis-open.org/xri/2.0/specs/xri-resolution-V2.0.html)
      - [XRI 2.0 FAQ](http://www.oasis-open.org/committees/xri/faq.php)
      - [XRI Requirements and Glossary 1.0](http://www.oasis-open.org/committees/download.php/2523/xri-requirements-and-glossary-v1.0.doc)（Word文書）
  - [W3C Internationalized Resource Identifier (IRI)](http://www.w3.org/International/O-URL-and-ident)
  - [XDI.org](http://www.xdi.org) - XRIグローバルレジストリサービスを管理している公益組織
      - [XDI.org Global Services Specifications](http://gss.xdi.org/moin.cgi)
      - [XDI.org I-Services Specifications](http://iss.xdi.org/moin.cgi)
  - [XRI and XRDS](http://iiw.idcommons.net/index.php/XRI) Internet Identity Workshop One-Pager
  - [FSF's Dispute with OASIS patent policies](http://www.fsf.org/news/oasis.html) and on [FSF's Support for OASIS RF on Limited Terms IPR Policy](http://www.fsf.org/campaigns/odf-oasis.html), which is used for ODF.
  - [EqualsDrummond](http://equalsdrummond.name) - Drummond Reed によるXRIやインターネット識別子についてのブログ。Drummond Reed は OASIS XRI TC の副委員長であり、[Cordance](http://www.cordance.net) のチーフアーキテクト。現在は [XDI.org](http://www.xdi.org) から委託を受けて XRI レジストリサービスを運営。

[Category:識別子](https://ja.wikipedia.org/wiki/Category:識別子 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.  [Time for OASIS XRI TC and W3C TAG to Sit Down Together](http://www.equalsdrummond.name/?p=130)
2.  [TAG recommends against XRI](http://lists.w3.org/Archives/Public/www-tag/2008May/0078.html)
3.  [Failed OASIS Standard Ballot of XRI Syntax v2.0](http://lists.oasis-open.org/archives/xri/200806/msg00001.html)
4.  [Failed OASIS Standard Ballot of XRI Resolution v2.0](http://lists.oasis-open.org/archives/xri/200806/msg00000.html)
5.  [URNs, Namespaces and Registries](http://www.w3.org/2001/tag/doc/URNsAndRegistries-50.xml)
6.  [Xri Solves Real Problems](http://wiki.oasis-open.org/xri/XriSolvesRealProblems)