> この記事は[XML署名](https://ja.wikipedia.org/wiki/XML署名)から翻訳されています。


**XML署名**（エックスエムエルしょめい、）は、[デジタル署名](../Page/デジタル署名.md "wikilink")のための[XML構文を規定する](../Page/Extensible_Markup_Language.md "wikilink")[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")である。XMLDSig、XML-DSig、XML-Sigとも呼ぶ。機能的には[PKCS](../Page/PKCS.md "wikilink")\#7と共通の部分が多くあるが、XML文書に対する署名に適応するための拡張を備える。[SOAPや](../Page/SOAP_\(プロトコル\).md "wikilink")[SAMLなど](../Page/Security_Assertion_Markup_Language.md "wikilink")、様々な[ウェブ技術で使われている](../Page/World_Wide_Web.md "wikilink")。

## 目的

XML署名は任意の種類の[リソース](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")（典型的にはXML文書）に署名を行うために用いる。

  - 署名
    署名を含むXML文書の外のリソースに対して用いられる署名
  - 署名
    署名を含むXML文書の一部分に対して用いられる署名
  - 署名
    自身の中に署名するデータを含む署名

## 構造

XML署名は、名前空間`http://www.w3.org/2000/09/xmldsig#`のSignature要素で構成される。その基本構造は次のようになる。

`Signature`
`  SignedInfo`
`    SignatureMethod`
`    CanonicalizationMethod`
`    Reference`
`      Transforms`
`      DigestMethod`
`      DigestValue`
`    Reference ...`
`  SignatureValue`
`  KeyInfo`
`  Object`

SignedInfo要素は署名の対象および使用するアルゴリズムを指定する。SignatureMethodおよびCanonicalizationMethod要素はSignatureValue要素により使用され、改竄（かいざん）から保護するためにSignedInfoに含まれる。

Reference要素のリストは署名されるリソースを[URIによって指定する](../Page/Uniform_Resource_Identifier.md "wikilink")。Transforms要素において[ハッシュ](https://ja.wikipedia.org/wiki/ハッシュ "wikilink")を計算する前にリソースに対し適用する全ての変換を、(DigestMethod要素において)ダイジェスト(ハッシュ)アルゴリズムを、リソースに対して適用した結果(これはDigestValue要素において[Base64](../Page/Base64.md "wikilink")エンコードされている)を指定する。

SignatureValue要素は署名のBase64エンコードされた値である。この値は、SignedInfo要素をCanonicalizationMethod要素で指定されたアルゴリズムによりシリアル化した後の(SignatureMethodの指定により生成される)署名である。(正規化に関する詳細は[XML正規化の節を参照のこと](https://ja.wikipedia.org/wiki/#XML正規化 "wikilink"))

KeyInfo要素は、署名の受信者に対し署名を検証するのに必要となる鍵を取得できるようにするオプション要素である。一般的には一連の[X.509](../Page/X.509.md "wikilink")証明書を入れることができる。存在しない場合、受信者はデータの内容から鍵を特定することが求められる。

Object要素は署名の場合に対象となるデータを保持するのに用いる。

## 検証とセキュリティ考察

XML署名を検証する際に、**コア検証 ()**と呼ばれる手続きは以下のようになる。

1.  **リファレンス検証**\[1\]: 個々のReference要素のダイジェスト値は関連するリソースを取得し、指定された全ての変換を適用し、指定されたダイジェストアルゴリズムを適用することにより検証される。結果は登録されたDigestValueと比較する。一致しない場合、検証失敗となる。
2.  **署名検証**\[2\]: SignedInfo要素はCanonicalizationMethod要素で指定された正規化方式でシリアル化され、KeyInfo要素や他の方法を用いて鍵データを取得し、SignatureMethod要素で指定された方式を用いて署名を検証する。

この手続き、主張する組織により本当にリソースが署名されたものかどうか立証する。しかしながら、正規化と変換方法の拡張性により、検証側の組織では実際に何に対して署名されたり、ハッシュ計算されたのか、言い換えれば、そこで使われたアルゴリズムが署名されたデータの意味を変更しないことを信頼できるかもまた確認しなければならない。

## XML正規化 ()

XML署名の生成は、通常のデジタル署名の生成よりも少し複雑である。何故なら、与えられたXML文書\[3\]は、一つ以上の正式なシリアル化された表現が存在するかもしれないからである。例えば、タグの中の空白は文法的に区別されないので、<Elem >は文法的には<Elem>と同じである。

デジタル署名はシリアル化されたXML文書に対し[暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")\[4\]を実行した結果に対して、暗号化に[非対称鍵アルゴリズム](https://ja.wikipedia.org/wiki/非対称鍵アルゴリズム "wikilink")\[5\]を用いることにより生成されるので、1バイトの違いによりデジタル署名は大きく変化する。

このような問題を回避し、論理的に同一であるXML文書が同一の署名値を生成することを保証するために、XML文書を署名する際には、ほぼ常に[XML正規化が実行される](https://ja.wikipedia.org/wiki/Canonical_XML "wikilink")(`SignedInfo`にを署名する際には正規化は必須である)。これらのアルゴリズムは、論理的に同一のドキュメントが、全く同一のシリアル化された表現を生成することを保証している。

デフォルトの正規化アルゴリズムが名前空間を扱う方式のために、また別の大きな問題がある。しばしば、署名されるXMLドキュメントは他のドキュメントを組み込む必要がある。この場合、オリジナルの正規化アルゴリズムではドキュメント単体で扱う時と同じ結果にはならない。このような理由により排他的正規化\[6\]と呼ばれる周囲のXMLに依存せず[XML名前空間](https://ja.wikipedia.org/wiki/XML名前空間 "wikilink")の定義をシリアル化する方式が開発された。

## 批評

XMLデータへの署名や暗号化のための前処理としてXML正規化を用いることについて、その複雑さ、固有の処理要件、低いパフォーマンス特性による批判がある。XML正規化を行うと、過度の待ち時間が発生し、単純にトランザクションや、パフォーマンスの影響が大きいSOAアプリケーションでは、解決することが難しいという議論がある。

## 脚注

<references/>

## 関連項目

  - [Canonical XML](https://ja.wikipedia.org/wiki/Canonical_XML "wikilink")
  - [XML暗号化](https://ja.wikipedia.org/wiki/XML暗号化 "wikilink")
  - [XAdES](../Page/XAdES.md "wikilink") () - ヨーロッパにおける電子署名に係る指針で定めた高度電子署名で利用できるXML署名の拡張

## 外部リンク

  - [Performance of Web Services Security](http://grids.ucs.indiana.edu/ptliupages/publications/WSSPerf.pdf)
  - [W3C workshop presentation on XML security](http://www.ximpleware.com/security/)
  - [Performance Comparison of Security Mechanisms for Grid Services](http://www.extreme.indiana.edu/xgws/papers/sec-perf.pdf)
  - [Why XML canonicalization is bad for Web Services Security](http://www.javaworld.com/javaworld/jw-01-2007/jw-01-vtd.html)
  - [XML-Signature Syntax and Processing (W3C)](http://www.w3.org/TR/xmldsig-core/)
  - [Canonical XML](http://www.w3.org/TR/2001/REC-xml-c14n-20010315)
  - [Exclusive XML Canonicalization](http://www.w3.org/TR/xml-exc-c14n/)
  - [Why XML Security is Broken](http://www.cs.auckland.ac.nz/~pgut001/pubs/xmlsec.txt)
  - [XMLSignatures Java binding](http://xmlbeans.googlepages.com/) for [XMLBeans](https://ja.wikipedia.org/wiki/XMLBeans "wikilink") and [JAXB](https://ja.wikipedia.org/wiki/JAXB "wikilink").

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:暗号技術](https://ja.wikipedia.org/wiki/Category:暗号技術 "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.
2.
3.  XML開発者の間では一般に「」と呼ぶ。
4.  一般的には[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")
5.  一般的には[RSA](../Page/RSA暗号.md "wikilink")
6.