> この記事は[Dublin Core](https://ja.wikipedia.org/wiki/Dublin_Core)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/画像:DCMI-logo.svg "wikilink") **Dublin Core**（ダブリン・コア、略称: **DC**）とは、メタデータ記述に使う語彙の通称。その語彙が共通の認識となるように、慎重な設計がされた基本語彙セットおよびそれらをサポートするメタデータ語彙が公開されている。

## 概要

名前の由来は、[OCLC](https://ja.wikipedia.org/wiki/OCLC "wikilink")主催で情報学やWeb技術の専門家によるメタデータに関する第1回会合が開かれた[アメリカ](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[オハイオ州](../Page/オハイオ州.md "wikilink")の町[ダブリンによる](../Page/ダブリン_\(オハイオ州\).md "wikilink")。

[WWW上におけるリソースに関する情報を記述して有用な情報の探索](../Page/World_Wide_Web.md "wikilink")・発見に役立てる目的で作られた。 特に、Webページの作者など専門家でなくとも簡単に記述できることを目指して、簡易なメタデータを作成するとの意図から作られたため、必ず記述しなければならない必須項目や、各項目の記述順序は無く、同一項目を複数回使用することも自由である。

Dublin Coreはメタデータを記す際に用いられる[RDFや](../Page/Resource_Description_Framework.md "wikilink")、[HTMLのhead要素などに埋め込むことにより](../Page/HyperText_Markup_Language.md "wikilink")、メタデータの共通化を計ることが可能になるという利点がある。

またDublin Coreの基本語彙は、[RSS (RDF Site Summary)の公式モジュールとして採用されたり](../Page/RSS.md "wikilink")（一部の要素はコアモジュールに取り込まれている）、[FOAF (Friend of a Friend)などでよく使われ](../Page/Friend_of_a_Friend.md "wikilink")、[Semantic Web関連技術のサポートに貢献している](https://ja.wikipedia.org/wiki/Semantic_Web "wikilink")。

## 規格化

### 国際標準

Dublin Core Metadata Initiative によって提唱され、2003年には ISO 15836\[1\] 及び NISO Z39.85\[2\] によって国際標準となった。

### 日本工業規格

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")においては国際規格の技術的内容を変更しない日本語訳が，**[JIS](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink") X 0836**:2005『ダブリンコアメタデータ基本記述要素集合』として規格化されている\[3\]。

## 基本記述要素一覧

Dublin Coreには15の基本記述要素がある。また基本語彙にあわせて、より詳細な情報を記述するための修飾子などが用意されている。 語彙の日本語訳はJIS X 0836:2005の表示名及び参考に拠った。

ここでは基本語彙のみを記す。

  - タイトル・表題 (Title)
    資源に与えられた名称。通常はある資源が公式に知られる名前を指す。
    例:
  - 作成者 (Creator)
    資源の内容に責任を負う実体。人や組織などがあげられ、その名前を記すことが常となっている。
    例:
  - キーワード・主題 (Subject)
    資源の内容の話題。まとめられた語彙の中から使うことが望ましい。
    例:
  - 内容記述 (Description)
    資源の内容の説明・記述。要約、目次など形式は定められていない。
    例:
    例:
  - 公開者・公表者・出版者 (Publisher)
    資源の公開に責任を負う実体。Creatorに同じく人や組織などがあげられ、その名前を記すことが常である。
    例:
  - 寄与者・貢献者 (Contributor)
    資源の作成に協力・貢献した実体。人や組織などの名前を示す。
  - 日付 (Date)
    資源に関する主要な出来事が起こった日付（更新日、作成日など）を記述する。[ISO 8601](../Page/ISO_8601.md "wikilink")（又は**JIS X 0301**）の書式に則ることが推奨される。
    例:
  - 資源タイプ (Type)
    資源の内容が持つカテゴリ、ジャンルなど。まとめられた語彙から使うことが推奨されている。なお、物理的/デジタル化されているものには、format要素を用いることが定められている。
    例:
  - 記録形式 (Format)
    資源が持つ物理的/デジタル化されている性質。メディアタイプなどがあげられ、資源を処理するソフトウェアやハードウェアを知るための手がかりとすることができる。[メディアタイプ](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")など、メディアフォーマットとして定められた語彙を使用することが望まれる。
    例:
  - 資源識別子 (Identifier)
    曖昧さのないものが必要とされる。URIやISBNなどが相当する。
    例:
  - 出処 (Source)
    資源が参照しているもの。公式な識別システムに従っている文字列や番号が望ましい。
    例:
  - 言語 (Language)
    資源がどの言語で書かれているのかを、RFC 3066の言語コード書式で書くのが望ましい。
    例:
  - 関係 (Relation)
    関連資源を公式な識別システムに従っている文字列や番号で記述するのが望ましい。
    例:
  - 時空間範囲・空間的範囲・時間的範囲 (Coverage)
    地名や緯度経度などで表記されるものや、日付、管理している範囲など。地名や時代の名前が緯度経度や日付より推奨される。
    例:
    例:
  - 権利管理 (Rights)
    著作権や知的所有権などの権利に関する情報を記述する。この要素が記述されていない場合に資源の権利情報を推測しても、それは何も意味しないことに注意すること。
    例:
    例:

## 外部リンク

  - [Dublin Core Metadata Initiative](http://dublincore.org/) Dublin Coreの本家
  - [Dublin Core: メタデータを記述するボキャブラリ](http://www.kanzaki.com/docs/sw/dublin-core.html) Dublin Coreについての説明や、RDF、XMLやHTMLとの関連づけについて書かれている。

### 要素セット

  - [DCMI Metadata Terms](http://dublincore.org/documents/dcmi-terms/) より詳細な情報を記述するための修飾子と、先述したMetadata Elemten Setおよび後述するDCMI Type Vocabularyも含んでいる。
  - [DCMI Abstract Model](http://dublincore.org/documents/abstract-model/) メタデータの抽象化モデル。
  - [DCMI Type Vocabulary](http://dublincore.org/documents/dcmi-type-vocabulary/) データを表現する際に用いられる、クロスドメインな「型」が定義されている。
  - [Dublin Core Metadata Element Set](http://dublincore.org/documents/dces/) 基本となる15の要素。

#### 規格

<references/>

### 文書一覧

  - [Expressing Simple Dublin Core in RDF/XML](http://dublincore.org/documents/dcmes-xml/) RDF/XMLで要素セットを使用する際のガイドラインや例など。
  - [Guidelines for implementing Dublin Core in XML](http://dublincore.org/documents/dc-xml-guidelines/) XML文書で使用する際のガイドライン。
  - [Expressing Dublin Core metadata using the Resource Description Framework (RDF)](http://dublincore.org/documents/dc-rdf/) 修飾子をRDFで使用する際のガイドライン。
  - [Expressing Dublin Core in HTML/XHTML meta and link elements](http://dublincore.org/documents/dcq-html/) HTMLやXHTML文書でメタデータを表す際のガイドライン。[RFC2371](http://www.ietf.org/rfc/rfc2731.txt)の新しいバージョンと位置づけられている。

## 関連項目

  - [RDF](../Page/Resource_Description_Framework.md "wikilink")
  - [セマンティックデスクトップ](https://ja.wikipedia.org/wiki/セマンティックデスクトップ "wikilink")

[Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink") [Category:ISO標準](https://ja.wikipedia.org/wiki/Category:ISO標準 "wikilink") [Category:セマンティック・ウェブ](https://ja.wikipedia.org/wiki/Category:セマンティック・ウェブ "wikilink")

1.  [ISO 15836:2003](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=37629)
2.  [ANSI/NISO Z39.85 - The Dublin Core Metadata Element Set](http://www.niso.org/kst/reports/standards?step=2&gid=&project_key=9b7bffcd2daeca6198b4ee5a848f9beec2f600e5)National Information Standards Organization
3.