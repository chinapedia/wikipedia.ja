> この記事は[Resource Description Framework](https://ja.wikipedia.org/wiki/Resource_Description_Framework)から翻訳されています。


**Resource Description Framework** (リソース・ディスクリプション・フレームワーク、**RDF**、) は、[ウェブ上にある](../Page/World_Wide_Web.md "wikilink")[リソースの](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")[メタデータ](../Page/メタデータ.md "wikilink")を記述するための枠組みであり、[W3Cにより](../Page/World_Wide_Web_Consortium.md "wikilink")[1999年](../Page/1999年.md "wikilink")2月に規格化されている。邦訳：電子ネットワーク協議会。RDFは、[セマンティック・ウェブ](../Page/セマンティック・ウェブ.md "wikilink")を実現するための技術的な構成要素の1つとなっており、代表例として[Linked Open Dataがある](https://ja.wikipedia.org/wiki/Linked_Open_Data "wikilink")。

RDFは、[RSS](../Page/RSS.md "wikilink")（）や[FOAF](../Page/Friend_of_a_Friend.md "wikilink")（）などに用いられている。また、RDFを[XHTML](https://ja.wikipedia.org/wiki/XHTML "wikilink")に埋め込む規格としてがある。

## 構造

### トリプル

RDFのメタデータのモデルでは、主語（）述語（）目的語（）の3つの要素で[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")に関する関係情報を表現し、これを**トリプル**（）と呼ぶ。主語は記述対象のリソースである。述語は主語の特徴や主語と目的語との関係を示す。目的語は主語との関係のある物や述語の値である。通常([文法学](https://ja.wikipedia.org/wiki/文法学 "wikilink")上)の意味での、主語・述語・目的語の意味とは異なる使い方になる場合もあることに注意が必要である。例えば、RDFにおいて「空の色は青い」という情報を表現しようとした場合、「空は青という色を持つ」と情報を整理した後、「空」を主語、「（～という）色を持つ」を述語（述部）、「青」を目的語として扱う。

[lang=ja](https://ja.wikipedia.org/wiki/ファイル:Basic_RDF_Graph.svg "wikilink") このトリプルは[グラフ理論](../Page/グラフ理論.md "wikilink")におけるグラフで表現できる。通常リソースのノードを丸で示し、テキストのノードを四角で示す。トリプルの関係はこれらのノードを述語を重みとしたエッジで結ぶことで表現する。このグラフはRDFに記述される全てのトリプルを可視化して表現することになる。このグラフは[RDF Validation Service](https://www.w3.org/RDF/Validator/)といったバリデータなど描かせることができる。

RDFが定義しているのはこのトリプルに基づく[抽象構文](https://ja.wikipedia.org/wiki/抽象構文 "wikilink")である。具象構文としては[XMLを利用した](../Page/Extensible_Markup_Language.md "wikilink")[RDF/XML](https://ja.wikipedia.org/wiki/RDF/XML "wikilink")が別に定義されている。

また、トリプルを表す[簡易表記方法として](../Page/軽量マークアップ言語.md "wikilink")\[1\]\[2\]、\[3\]、\[4\]などがある。

  -

      -
        1行ごとに1つのトリプルを、主語・述語・目的語の順にスペースで区切って表記するフォーマット。

  -

      -

        を拡張し、XMLのような 接頭辞+ローカル名 に基づく表記や、実験的に推論規則なども可能としたフォーマット。

  -

      -

        に、 の便利な書式を取り入れたフォーマット。

### リソースの識別

RDFにおける主語は、[URIで示されたリソースか](../Page/Uniform_Resource_Identifier.md "wikilink")、URIを持たず直接参照できない空白ノードのどちらかである。述語はURIで示される。目的語は[Unicode](../Page/Unicode.md "wikilink")の文字列か（URIで示された）リソースか空白ノードのいずれかである。

RDFを元とした[RSS](../Page/RSS.md "wikilink")や[FOAFなどにおいてはウェブ上に実際に存在しているデータを指し示すURIが使われることが普通である](../Page/Friend_of_a_Friend.md "wikilink")。一般にRDFにおいてはインターネットにおける参照可能なメタデータだけを扱うものに限らずにURIを扱うことができ、リソースのURIが参照が不能なものであっても問題はない。このリソースのURIが何らかの抽象的表現を表す場合もある。この参照不能なURIをRDFで用いる場合、予めその意味を決めておく必要がある。RDF自体はそのような語彙の共通に使える取り決めはしていないが、[Dublin Coreなど共通に使える語彙も提供されている](../Page/Dublin_Core.md "wikilink")。

## 例

例文「[門前仲町](../Page/門前仲町.md "wikilink")の[略語](../Page/略語.md "wikilink")は“モンナカ”である。」のトリプルはそれぞれ

  - 主語「門前仲町」 - 統一資源識別子，
  - 述語「略語である」- 統一資源識別子，
  - 目的語「モンナカ」- 文字列[直値](../Page/リテラル.md "wikilink")

となる。RDFで表現するときは、目的語は単なる文字列でも良いが、主語と述語は[URI](https://ja.wikipedia.org/wiki/URI "wikilink")で表現されたリソースでなければならない。ここで仮に上のようにURIを対応すると、RDF/XMLで表記すると次のようになる。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Rdf-grf-ex-monnaka.svg "wikilink")

もうひとつの例として、Wikipedia英語版の「」のページ「http://en.wikipedia.org/wiki/Tony_Benn」に関して、タイトルが「」、発行元が「」という情報があるとする。ここで、ひとつの主語に対して複数のトリプルが表現されているが、シンプルに次のようにRDF/XMLで表記する。

``` xml
<rdf:RDF
 xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
 xmlns:dc="http://purl.org/dc/elements/1.1/">
  <rdf:Description rdf:about="http://en.wikipedia.org/wiki/Tony_Benn">
    <dc:title>Tony Benn</dc:title>
    <dc:publisher>Wikipedia</dc:publisher>
  </rdf:Description>
</rdf:RDF>
```

[frame](https://ja.wikipedia.org/wiki/ファイル:Rdf-graph-example-TonyBenn.png "wikilink")

ここで、このリソースのタイトルが「」であることがRDFに記述されているのでコンピュータもそのように理解できる。特に[Dublin Coreの基本語彙である](../Page/Dublin_Core.md "wikilink")`http://purl.org/dc/elements/1.1/title`が理解できるソフトウェアならば、称号や権利といった意味ではなく、リソース自体の題名ということが認識できる。

## 供給例

  - [Open Directory Project](https://ja.wikipedia.org/wiki/Open_Directory_Project "wikilink")

## 脚注

### 注釈

### 出典

## 関連項目

  -
  - [OWL](../Page/OWL.md "wikilink")

  - [RSS](../Page/RSS.md "wikilink")

  - [マイクロフォーマット](../Page/マイクロフォーマット.md "wikilink")

  - [RDFクエリ言語](../Page/RDFクエリ言語.md "wikilink") - [SPARQL](../Page/SPARQL.md "wikilink")

  - [トピックマップ](https://ja.wikipedia.org/wiki/トピックマップ "wikilink")

## 外部リンク

  - 資料
      - [W3C公式RDFサイト](https://www.w3.org/RDF/)
      - [RDF Primer](https://www.w3.org/TR/rdf-primer/)
      - [RDF Primer（和訳）](https://www.asahi-net.or.jp/~ax2s-kmtn/internet/rdf/rdf-primer.html)
      - [What is RDF?](https://www.xml.com/pub/a/2001/01/24/rdf.html)
      - [RDF/XML構文の簡単な説明](https://www.kanzaki.com/docs/sw/rdf-xml.html) - [神崎正英](https://www.kanzaki.com/info/who)によるRDFの解説
  - 一般的な語彙
      - [Dublin Core Metadata Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)
      - [FOAF Vocabulary Specification](http://xmlns.com/foaf/0.1/)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink") [Category:セマンティック・ウェブ](https://ja.wikipedia.org/wiki/Category:セマンティック・ウェブ "wikilink") [Category:モデリング言語](https://ja.wikipedia.org/wiki/Category:モデリング言語 "wikilink") [Category:知識表現](https://ja.wikipedia.org/wiki/Category:知識表現 "wikilink")

1.
2.
3.
4.