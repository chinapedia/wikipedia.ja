> この記事は[Extensible Markup Language](https://ja.wikipedia.org/wiki/Extensible_Markup_Language)から翻訳されています。


**Extensible Markup Language**（エクステンシブル マークアップ ランゲージ）は、基本的な構文規則を共通とすることで、任意の用途向けの言語に拡張することを容易としたことが特徴の[マークアップ言語](../Page/マークアップ言語.md "wikilink")の総称である。一般的に**XML**（エックスエムエル）と略称で呼ばれる。[JISによる訳語は](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")「**拡張可能なマーク付け言語**」と定義している。

[SGMLからの移行を目的として開発された](../Page/Standard_Generalized_Markup_Language.md "wikilink")。文法はSGMLの構文解析器と互換性を保つようにSGMLのサブセットに定められシンプルになり、機能はSGMLに無いものが追加されている。

XML の仕様は、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) により策定・勧告されている。1998年2月に XML 1.0 が勧告された。2010年4月現在、XML 1.0 と XML 1.1 の2つのバージョンが勧告されている（[\#バージョン](https://ja.wikipedia.org/wiki/#バージョン "wikilink")）。

ちなみに、「e**X**tensible **M**arkup **L**anguage の略である」と書かれることがあるが、これは間違いであり、**X**は**Ex**の発音を表している\[1\]。

## 概要

### 基礎的概念と利用目的

XMLは、個別の目的に応じた[マークアップ言語](../Page/マークアップ言語.md "wikilink")群を創るために汎用的に使える。マークアップ言語とは、[コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")の一種で（広義の「[コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")」であり、[プログラミング言語](../Page/プログラミング言語.md "wikilink")ではない[データ記述言語](../Page/データ記述言語.md "wikilink")などを含む意味）あるが、詳細は「[マークアップ言語](../Page/マークアップ言語.md "wikilink")」の記事を参照のこと。XMLは、その「入子状にタグで囲まれたもの」という構文を共通としたことで、拡張が容易であるとして「extensible」と主張している。

上記の理由もあって、しばしば「あらゆる目的に使える」などと主張されるが、プログラム自体の構造としては入れ子構造（木構造）であって、より入り組んだネットワーク構造（[グラフ構造](../Page/グラフ_\(データ構造\).md "wikilink")）を直接扱うことは不可能である（[XLink](../Page/XLink.md "wikilink")などの提案はあるが）。

XMLの最も重要な目的は、異なる[情報システム](../Page/情報システム.md "wikilink")の間で、特に[インターネット](../Page/インターネット.md "wikilink")を介して、構造化された文書や構造化されたデータの共有を、容易にすることである\[2\]。XMLを使うと、文書を構造化して記述できるし、[コンピュータ](../Page/コンピュータ.md "wikilink")のデータを[直列化](../Page/シリアライズ.md "wikilink") （シリアライズ） できる。データを直列化する用途でXMLを使う際には、XMLは、[JavaScript Object Notation](../Page/JavaScript_Object_Notation.md "wikilink") (JSON) や[YAML](../Page/YAML.md "wikilink")などの、[テキストを基にした他の直列化言語と比較衡量できる](../Page/プレーンテキスト.md "wikilink")\[3\]。

### HTMLとXMLの違い

XMLは、ユーザが定義したタグを用いて文章構造を記述するマークアップ言語である。HTMLが、Webページを記述するための言語であるのに対して、XMLは、データ交換のための汎用のデータ形式である。HTMLで使用するタグはあらかじめ定義済みのものだが、XMLではユーザが新しくタグを定義して、データの意味や構造を記述することが可能である。

### XMLを基盤とするマークアップ言語とスキーマ言語

XMLで文書の論理的構造を規定する制約を追加することによって、XMLを適用したマークアップ言語を[実装](../Page/実装.md "wikilink")できる。XMLを適用したマークアップ言語は非常に多く存在している （[\#XMLの応用](https://ja.wikipedia.org/wiki/#XMLの応用 "wikilink")の節を参照）。例えば、[Extensible HyperText Markup Language](../Page/Extensible_HyperText_Markup_Language.md "wikilink") (XHTML)\[4\]、[DocBook](../Page/DocBook.md "wikilink")、[RSS](../Page/RSS.md "wikilink")、[Mathematical Markup Language](../Page/Mathematical_Markup_Language.md "wikilink") (MathML)、[ebXML](https://ja.wikipedia.org/wiki/ebXML "wikilink")、[Scalable Vector Graphics](../Page/Scalable_Vector_Graphics.md "wikilink") (SVG)、[MusicXML](../Page/MusicXML.md "wikilink") などがある。さらにXMLは、そういった個別のXMLについての構文規則を示すための[スキーマ言語](../Page/スキーマ言語.md "wikilink")も用意している。スキーマ自体もXMLの[XML Schemaの他](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")、XMLではない記法でとても簡潔に大変わかりやすく書ける、Compact Syntaxも用意されている[RELAX NGもある](../Page/RELAX_NG.md "wikilink")。

### オープンな仕様

XMLは、同じく汎用的に使えるマークアップ言語である [Standard Generalized Markup Language](../Page/Standard_Generalized_Markup_Language.md "wikilink") (SGML) の、簡素化されたサブセットとして、人間にとっても比較的判読しやすいように設計された （[\#歴史](https://ja.wikipedia.org/wiki/#歴史 "wikilink")を参照）。XMLの仕様は、XMLワーキンググループなどにより設計が行われ、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) により勧告 （策定） されている。XMLは無償で使える[オープン標準](../Page/オープン標準.md "wikilink")の技術である。XML仕様のW3C勧告ではXMLの文法とXMLプロセサ （[XMLパーサ](https://ja.wikipedia.org/wiki/XMLパーサ "wikilink")、XML文書の[構文解析器](../Page/構文解析器.md "wikilink")） のための要件を定めている。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")2月に XML 1.0 が勧告され、2004年2月に XML 1.1 が勧告された（[\#バージョン](https://ja.wikipedia.org/wiki/#バージョン "wikilink")参照）。

### 正当性水準について

XML文書の正当性の水準には、整形式XML文書と妥当なXML文書の、2つの水準がある （[\#整形式XML文書と妥当なXML文書](https://ja.wikipedia.org/wiki/#整形式XML文書と妥当なXML文書 "wikilink")を参照）。XML文書のマークアップ規則に従って記述されていることだけが問題とされる文脈で、スキーマ言語を使わずに、XML文書のマークアップ規則に従って記述された文書を、「整形式XML文書」 (well-formed XML document) という （[\#XMLの構文と整形式XML文書](https://ja.wikipedia.org/wiki/#XMLの構文と整形式XML文書 "wikilink")を参照）。さらに、XML文書をより厳密に構造化した文書やデータとして扱いたい場合は、XML文書の構造を[スキーマ言語](../Page/スキーマ言語.md "wikilink")によって定義することができ、XMLプロセサでそのXML文書（XMLインスタンス）に対してその文書構造に従っていることを検証する（妥当性検証を行う）というように、XML技術を使うこともできる （[\#XML文書の論理的構造と妥当なXML文書](https://ja.wikipedia.org/wiki/#XML文書の論理的構造と妥当なXML文書 "wikilink")を参照）。 XML文書に対して妥当性検証を行うことにより、従来[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")で行ってきた、XML文書の構造の検査や、XML文書に含まれるデータに対する[データ型](../Page/データ型.md "wikilink")のチェックや値の範囲のチェックが、可能となる。スキーマ言語としては [Document Type Definition](../Page/Document_Type_Definition.md "wikilink") (DTD、文書型定義)、[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") XML Schema、RELAX NG （[文書スキーマ定義言語](../Page/文書スキーマ定義言語.md "wikilink"): DSDL）などがある。XML文書の構造がスキーマ言語によって定義され、XML文書の妥当性を検証する[ソフトウェア](../Page/ソフトウェア.md "wikilink")によって妥当性が検証されたXML文書のことを「妥当なXML文書」 (valid XML document) という。整形式XML文書は、妥当なXML文書である場合と、妥当なXML文書ではない場合とがある。スキーマ言語を採用して妥当性検証を行う方法でXMLを使うこともできるし、スキーマ言語を採用せず妥当性検証を行わないで手軽にXMLを使うこともできる。

### 幅広い人間言語のサポート

XML勧告では、XMLプロセサがサポートすべき[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")（[文字コード](../Page/文字コード.md "wikilink")）として[UTF-8](../Page/UTF-8.md "wikilink")と[UTF-16](../Page/UTF-16.md "wikilink") ([Unicode](../Page/Unicode.md "wikilink")) を定めているため、英語以外の言語も扱いやすくなっている （[\#多言語環境で使う](https://ja.wikipedia.org/wiki/#多言語環境で使う "wikilink")を参照）。また、UTF-8とUTF-16以外の文字コード（[UCS-4](https://ja.wikipedia.org/wiki/UCS-4 "wikilink")、[EUC-JP](../Page/EUC-JP.md "wikilink")、[Shift_JIS](../Page/Shift_JIS.md "wikilink")、[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")など）を用いることも可能である\[5\]。

### 補完技術

XMLだけでは最低限の書式しか決められていないため、XMLの力を引き出す各種の関連技術が別途標準化されている （[\#XMLの拡張](https://ja.wikipedia.org/wiki/#XMLの拡張 "wikilink")および[\#XML文書をプログラムで処理する](https://ja.wikipedia.org/wiki/#XML文書をプログラムで処理する "wikilink")、[\#XML文書を視覚的に表示する](https://ja.wikipedia.org/wiki/#XML文書を視覚的に表示する "wikilink")、[\#XML情報集合](https://ja.wikipedia.org/wiki/#XML情報集合 "wikilink")を参照）。 以下に挙げるものをはじめとして、現在も多くの関連技術の標準化作業が行われている。

  - [プログラムからXML文書を処理する方法として](../Page/プログラム_\(コンピュータ\).md "wikilink")、[Document Object Model](../Page/Document_Object_Model.md "wikilink") (DOM) や [Simple API for XML](../Page/Simple_API_for_XML.md "wikilink") (SAX) などの[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (API) が標準化されている\[6\]。

<!-- end list -->

  - XML文書のスタイルを指定する技術（[スタイルシート](../Page/スタイルシート.md "wikilink")）として [Extensible Stylesheet Language](../Page/Extensible_Stylesheet_Language.md "wikilink") (XSL) や [Cascading Style Sheets](../Page/Cascading_Style_Sheets.md "wikilink") (CSS) などがある。

<!-- end list -->

  - XML文書を非[テキスト形式](../Page/テキストファイル.md "wikilink")（[バイナリ](../Page/バイナリ.md "wikilink")）で効率的に表現する方法として、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) は [Efficient XML Interchange](https://ja.wikipedia.org/wiki/Efficient_XML_Interchange "wikilink") (EXI) フォーマットを定義した。

### XMLの普及とXMLへの批評

XMLは現在、広く普及している技術であるが、その技術的な有用性などについて、肯定的に評価する人々が多い一方で、批判的に評価する人々も多い （[\#XMLに対する支持と批判](https://ja.wikipedia.org/wiki/#XMLに対する支持と批判 "wikilink")を参照）。

## 整形式XML文書と妥当なXML文書

XML文書の正当性の水準には、整形式XML文書と妥当なXML文書の、2つの水準がある。なおXML文書に対して、整形式XML文書としての検査のみを行うXMLプロセサを**非検証XMLプロセサ**といい、整形式XML文書としての検査に加えて妥当なXML文書としての検査を行うXMLプロセサを**検証XMLプロセサ**という。

  - 整形式XML文書
    整形式XML文書 (well-formed XML document) は、XMLの構文の規則のすべてに準拠している。例えば、文書中のある要素が開始タグが有るが対応する終了タグが欠落している場合、その文書は**整形式** (well-formed) ではない。整形式ではない文書はXML文書とはみなされない。非検証XMLプロセサおよび検証XMLプロセサは、整形式ではない文書を処理することはできない (処理を試みるとエラーになる)。
  - 妥当なXML文書
    妥当なXML文書 (valid XML document) は、整形式XML文書としての条件を満たしていることに加えて、文書の論理的構造を規定する何らかの規則に準拠している。このような規則は、RELAX NG や XML Schema、Document Type Definition (DTD、文書型定義) などの[スキーマ言語](../Page/スキーマ言語.md "wikilink")で定義されたスキーマで定める。例えば、あるXML文書がスキーマに定義されていない要素 (タグ) を含んでいた場合、検証XMLプロセサは、そのXML文書を処理することはできない。検証XMLプロセサによって検証されたXML文書は、**妥当** (valid) であると位置づけられる。なお、妥当な文書であっても、非検証XMLプロセサでは[実体の定義を確認しないため](https://ja.wikipedia.org/wiki/#実体参照 "wikilink")、仕様で定められている実体参照(\<、\>など)以外の私的な実体参照を用いている場合、非検証XMLプロセサは当該実体を参照できず致命的なエラーとなる。

## XMLの構文と整形式XML文書

整形式XML文書が満たすべき構文の規則を説明する。

整形式XML文書としての条件が満たされることのみを考慮する場合 (スキーマ言語を使わずに手軽にXMLを使う場合) においても、XMLは、大量の文書やもしくは[木構造として表現することができるデータを格納するための](../Page/木構造_\(データ構造\).md "wikilink")、一般的な枠組みとしての役割を果たすことができる。

XML文書は、**要素** (element) と**属性** (attribute) が複数集まって、構成されている。 要素は内部に子要素を含むことができる。属性は要素に付随し、属性の内部に子要素を含むことはできない。要素は開始タグと終了タグで内容を挟むことで表現する。 開始タグは「<要素名>」、終了タグは「</要素名>」で記述する。

一つの要素を記述するための基本的な構文を次に示す。

``` xml
<要素名 属性="値">内容</要素名>
```

ここで、\<要素名 属性="値"\> をこの要素の開始タグといい、\</要素名\> を終了タグという。「内容」は何らかのテキストである。

次に示す例は整形式XML文書である。

``` xml
<書籍 出版日="2007-10-31">これは書籍です.... </書籍>
```

この例は、書籍という要素を一つもつXML文書である。<書籍> が書籍要素の開始タグであり、</書籍> が書籍要素の終了タグである。「出版日="2007-10-31"」は書籍要素の属性である。この属性の名前 （属性名） は「出版日」であり、この属性の値 （属性値） は "2007-10-31" である。「これは書籍です.... 」は、書籍要素の内容である。

要素の内容を構成するテキストはまた、さらに任意の数の要素を含むことができる （なお、このように一つの要素内に文字列データと子要素が混在するものを、「混合内容」と呼ぶ\[7\]）。 すなわち、一般的なXML文書は[木構造をなす](../Page/木構造_\(データ構造\).md "wikilink")。 この点において、XMLは[プログラミング言語](../Page/プログラミング言語.md "wikilink")[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の[S式](https://ja.wikipedia.org/wiki/S式 "wikilink")と似ている。 S式でも木構造を記述する。S式の木構造のおのおのの節は、自分自身のプロパティリストをもつことができる。

要素は内部に別の要素を含むことができる。構造化したXML文書の例を示す。

``` xml
 <レシピ 名前="パン" 準備時間="5分" 調理時間="3時間">
   <料理>基本的なパン</料理>
   <材料 量='3' 単位='カップ'>小麦粉</材料>
   <材料 量='0.25' 単位='オンス'>イースト</材料>
   <材料 量='1.5' 単位='カップ' 状態="温かい">水</材料>
   <材料 量="1" 単位="ティースプーン">食塩</材料>
   <要領>
     <手順>全ての材料を一緒にして混ぜます。</手順>
     <手順>十分にこねます。</手順>
     <手順>布で覆い、暖かい部屋で1時間そのままにしておきます。</手順>
     <手順>もう一度こねます。</手順>
     <手順>パン焼きの容器に入れます</手順>
     <手順>布で覆い、暖かい部屋で1時間そのままにしておきます。</手順>
     <手順>オーブンに入れて温度を180℃にして30分間焼きます。</手順>
   </要領>
 </レシピ>
```

要素の属性の値は、必ずシングルクォート (') かダブルクォート (") で括らなければならない。そして要素内にある属性は、互いに属性名が異なっていなければならない。XML文書では要素は正しく入れ子になっていなければならない。要素は決してオーバーラップしていてはならない。

例えば、次の文書は整形式XML文書ではない。なぜなら `書名` 要素と `著者` 要素がオーバーラップしているからである。

``` xml
<!-- 正しくありません! 整形式XML文書ではありません! -->
<書籍目録> <書名>XML入門<著者>筒井<書名>続・XML入門<著者>小松</書名></著者></書名></著者> </書籍目録>
```

次の2つの文書は整形式XML文書である。

``` xml
<!-- 正しい整形式XML文書です -->
<書籍目録> <書名>XML入門</書名> <著者>筒井</著者> <書名>続・XML入門</書名> <著者>小松</著者> </書籍目録>
```

``` xml
<!-- もう一つの正しい整形式XML文書です -->
<書籍目録> <書名>XML入門</書名> <著者>筒井<書名>続・XML入門<著者>小松</著者></書名></著者> </書籍目録>
```

整形式XML文書においては、XML文書は正確に一つの**ルート要素** （**文書要素**; document element とも呼ばれる） をもたなければならない。ルート要素とは、XML文書の要素の階層構造において最上位の要素のことをいう。最上位の要素は一つでなければならない。最上位の要素が複数ある文書は、整形式XML文書ではない。 整形式XML文書が一つのルート要素をもたなければならないという条件が意味することは、整形式XML文書のテキストは、ルート要素の開始タグと対応する終了タグの間に、収められなければならないということである。ルート要素の開始タグと終了タグの間に収められたテキストは、任意の数の要素や文字列データを含むことができる。

ルート要素の前に、必要に応じて、**XML宣言** (XML declaration) をおくことができる。このXML宣言は、XMLのどのバージョンが使われているか （現時点ではバージョン1.0であることが多い） などを示す。XML宣言では、XMLのバージョンの他に、[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink") （[文字コード](../Page/文字コード.md "wikilink")） の指定や、他のXML文書との依存関係についての指定を、行うこともできる。

  - XML文書の文字符号化方式が[UTF-8](../Page/UTF-8.md "wikilink")か[UTF-16](../Page/UTF-16.md "wikilink")の場合は、XML宣言をおいてもよいし、XML宣言をおかなくてもよい。
  - XML文書の文字符号化方式がUTF-8でもUTF-16でもない場合は、XML宣言をおいて文字符号化方式を明示する必要がある。

XML宣言を含んだXML文書の例を示す。

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<書籍 出版日="2007-10-31">これは書籍です.... </書籍>
```

XML仕様では、**XMLプロセサ** （[XMLパーサ](https://ja.wikipedia.org/wiki/XMLパーサ "wikilink")、XML文書の[構文解析器](../Page/構文解析器.md "wikilink")） が、[Unicode](../Page/Unicode.md "wikilink")の文字符号化方式である[UTF-8](../Page/UTF-8.md "wikilink")および[UTF-16](../Page/UTF-16.md "wikilink")で記述されたXML文書を処理できることを、**必須**条件としている （[UCS-4](https://ja.wikipedia.org/wiki/UCS-4 "wikilink")は必須条件ではない）。XMLプロセサは、UTF-8およびUTF-16の他にも、いくつかの任意の文字符号化方式の文書を処理できるようにして良い。例えば、[UCS-4](https://ja.wikipedia.org/wiki/UCS-4 "wikilink")、[EUC-JP](../Page/EUC-JP.md "wikilink")、[Shift_JIS](../Page/Shift_JIS.md "wikilink")、[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")などの文字符号化方式の文書を処理できるXMLプロセサが、広く普及し、使われている。

**[コメント](../Page/コメント_\(コンピュータ\).md "wikilink")**はXML文書の木構造のどこにでもおくことができる。 コメントは、" " で終わる。 なお、コメント内に "--" を含むことはできない。

コメントを含むXML文書の例を示す。

``` xml
<書籍 出版日="2007-10-31">
 <!-- これはコメントです.... -->
 これは書籍です....
</書籍>
```

内容のない要素を**空要素** (empty element) という。XMLでは、空要素を表現するために特別な構文を使うことができる。開始タグを書きその直後に終了タグを書くこともできるが、その代わりに空要素のタグを使うことができるのである。空要素タグは開始タグと似ているが、閉じ括弧の直前にスラッシュをおく。

次の3つの例は、XMLでは同等である。

``` xml
<foo></foo>
<foo/>
<foo />
```

空要素タグは属性を含むことができる。

``` xml
<情報 著者="小松左京" 分類="サイエンスフィクション" 日付="2009-01-01"/>
```

### 多言語環境で使う

XML文書ではどの[Unicode](../Page/Unicode.md "wikilink")の文字も （XMLで特別な意味をもつ、開き山括弧 "\<" のような文字を除いて）、要素名として、属性名として、コメント内容として、文字データとして、[処理命令](https://ja.wikipedia.org/wiki/#処理命令 "wikilink") （後述） として、直接に使うことができる。このため、[漢字](../Page/漢字.md "wikilink")と[キリル文字](../Page/キリル文字.md "wikilink")を共に含む次の文書も、整形式XML文書である。

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<俄語>Данные</俄語>
```

### 文書型宣言

XML文書 （あるいは[SGML文書](../Page/Standard_Generalized_Markup_Language.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")[ウェブページ](../Page/ウェブページ.md "wikilink")を含む） において、**文書型宣言** （**DOCTYPE宣言**、Document Type Declaration） は、その文書を特定の Document Type Definition(DTD、文書型定義) のスキーマと関連づけることを記述するものである。なお、Document Type Definition (DTD、文書型定義)は、XMLで使うことができる[スキーマ言語](../Page/スキーマ言語.md "wikilink")の一つである。文書型宣言は、その文書が特定のスキーマに準拠していることを宣言する。

XML文書では文書型宣言を記述してもよいし、記述しなくてもよい。DTDをスキーマ言語として妥当性検証を行うことを想定しているのであれば、文書型宣言の記述は必須となるであろう。DTDで妥当性検証を行わない場合でも、後述する[実体参照などを文書中で使うのであれば](https://ja.wikipedia.org/wiki/#実体参照 "wikilink")、文書型宣言において文書中で使う実体を宣言することができる。

文書型宣言は、その文書が特定のスキーマに準拠していること （妥当なXML文書であること） を、保証しているわけではない。文書型宣言に記されたスキーマに準拠しているかどうかを判断するには、検証XMLプロセサでその文書を検証する必要がある。

文書型宣言の一般的な構文は次のとおりである。

`<!DOCTYPE ルート要素名 [SYSTEM もしくは PUBLIC 公開識別子] 外部サブセット参照 [`
` <!-- 随意に内部サブセットを記述する -->`
`]>`

ここで**外部サブセット**とは、そのXML文書のDTDを構成する （要素の型の宣言、後述する実体の宣言などの） 宣言群のうち、別ファイルに記述された宣言群のことである。また**内部サブセット**とは、そのXML文書のDTDを構成する宣言群のうち、文書型宣言内に直接記述された宣言群のことである\[8\]。

[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") 1.0 Strict に準拠したXML文書での文書型宣言は、次のとおりである。

`<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" `
`     "`<http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd>`">`

XML文書においては、ルート要素がその文書の最初の要素である （例えば、XHTMLではルート要素は `html` である）。`SYSTEM` キーワードと `PUBLIC` キーワードは、その文書型 （文書の構造） の種類を指定する。一般に広く知られていないDTDを使う場合は、`SYSTEM` キーワードを使う。一般に広く知られているDTDを使う場合 （XHTMLなど） は、`PUBLIC` キーワードを使う。

  - `SYSTEM` キーワードを使う際は、その後に続けて、その文書が準拠するDTDのファイルの[URIを](../Page/Uniform_Resource_Identifier.md "wikilink")、外部サブセット参照として記述する。
  - `PUBLIC` キーワードを使う際は、その後に続けて、その文書が準拠するDTDの公開識別子 (public identifier) を指定しなければならない （例えば XHTML 1.0 の公開識別子は、"-//W3C//DTD XHTML 1.0 Strict//EN" である）。公開識別子を記述した後に続けて、SYSTEM キーワードを使う場合と同様に、その文書が準拠するDTDのファイルのURIを、外部サブセット参照として記述する。

内部サブセットは必要に応じて記述する。 内部サブセットとして、DTDの一部分もしくはDTDの全体を記述することができる。 なお、内部サブセットとしてDTDの全体を記述する場合は、`SYSTEM`キーワード・`PUBLIC`キーワード・外部サブセット参照は、いずれも記述しない。

### 実体参照

**実体参照** (entity reference) は、実体を表現するプレースホルダである。

XMLにおける**[実体](https://ja.wikipedia.org/wiki/SGML実体 "wikilink")** (entity) とは、[SGMLにおける実体と同じように](../Page/Standard_Generalized_Markup_Language.md "wikilink")、名前の付けられたデータの本体である。具体的には、ファイルもしくは置換文字列のように、何らかの形でXML文書の一部となるデータを格納しているもののことである\[9\]。 置換文字列を使う事例としては、次のような場合がある。

  - キーボードから簡単には入力できない文字をXML文書中に表現したい場合。
  - 決まった単語の並びがXML文書中に何度も出現する場合。

実体参照の構成は、まず最初に[アンパサンド](../Page/アンパサンド.md "wikilink") ("`&`") があり、その後に実体の名前が続き、[セミコロン](../Page/セミコロン.md "wikilink") ("`;`") で終わる。

XMLには、事前宣言された実体として次の表に示す5つの実体がある。

| 実体参照 | 実体 | 実体の説明                                                                    |
| ---- | -- | ------------------------------------------------------------------------ |
| `&`  | &  | [アンパサンド](../Page/アンパサンド.md "wikilink") (ampersand)                       |
| `<`  | \< | 小なり (less than)                                                          |
| `>`  | \> | 大なり (greater than)                                                       |
| `'`  | '  | [アポストロフィ](https://ja.wikipedia.org/wiki/アポストロフィ "wikilink") (apostrophe) |
| `"`  | "  | クォーテーションマーク (quotation mark)                                             |

「AT\&T」の名前で[アンパサンド](../Page/アンパサンド.md "wikilink")を表現するために、事前宣言されたXMLの実体を使う例を示す。

``` xml
<会社名称>AT&T</会社名称>
```

事前宣言された実体以外の実体を宣言する必要がある場合、XML文書の Document Type Definition （DTD、文書型定義） の内部で宣言する。

XML文書の内部に定義されたDTDを使って、置換文字列としての実体を宣言して、実体参照を使う例を次に示す。宣言された実体は、一つの文字であっても良いし、テキストの断片であっても良いし、他の実体への参照を含むテキストであっても良い。

``` xml
<?xml version='1.0' encoding='UTF-8'?>
<!DOCTYPE 例 [
    <!ENTITY copy "©">
    <!ENTITY copyright-notice "Copyright © 2007 平成新報社">
]>
<例>
    &copyright-notice;
</例>
```

XMLに準拠した[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")を使うと、先のXML文書は次のように表示される。

`     Copyright © 2007 平成新報社`

ファイルの実体を参照するXML文書の例を示す。

``` xml
<?xml version='1.0' encoding='UTF-8'?>
<!DOCTYPE 文章 [
    <!ENTITY tsutsui-yasutaka SYSTEM "another-file.xml">
]>
<文章>
 <文>星新一はSF作家である。</文>
 <文>小松左京はSF作家である。</文>
 &tsutsui-yasutaka;
</文章>
```

なお、別ファイル `another-file.xml` には次の内容が記されていることとする。

``` xml
 <文>筒井康隆はSF作家である。</文>
```

XMLに準拠したブラウザでこのXML文書を表示すると、次のようになる。

`星新一はSF作家である。小松左京はSF作家である。筒井康隆はSF作家である。`

### 文字参照

**文字参照** (character reference) は、文字をXML文書内でコード番号を指定して記述する記法である。文字参照は、実体参照と似ているが、実体参照では名前を使うのに対し、文字参照ではその部分で始めに "`#`" 文字を記述し続けて数字を記述する。

文字参照で使う数字は、[符号化文字集合](https://ja.wikipedia.org/wiki/符号化文字集合 "wikilink")の国際規格である [ISO/IEC 10646](https://ja.wikipedia.org/wiki/ISO/IEC_10646 "wikilink") (および[Unicode](../Page/Unicode.md "wikilink")) のコード番号である。文字参照で使うことができる数字は、十進数であるか "`x`" を前につけた十六進数である。文字参照は、実体参照とは異なり、事前宣言されているわけでもなく、XML文書のDTD内部で宣言されているわけでもない。文字参照は、簡単には符号化できない文字を表現するために使われることが多い。例えば、[欧州のコンピュータ上で作成するXML文書で](../Page/ヨーロッパ.md "wikilink")[アラビア語](../Page/アラビア語.md "wikilink")の文字を使う場合などである。「AT\&T」の例の内のアンパサンドは、この場合に似ているともいえる。十進数の38と十六進数の26は、共に ISO/IEC 10646 の "&" 文字のコード番号である。つまり「AT\&T」はXML文書では次のように記述することができる。

``` xml
<会社名称>AT&T</会社名称>
<会社名称>AT&T</会社名称>
```

### 処理命令

**処理命令** (processing instruction) は、XML文書の構成要素であり、XML文書を扱う[ソフトウェア](../Page/ソフトウェア.md "wikilink")に対する何らかの処理を行う命令を、記述する内容が、処理命令である。

次に処理命令の構文を示す。

``` xml
<?処理命令ターゲット 処理内容?>
```

処理命令は ?\> の文字列を除き任意の処理内容を記述することができる。処理命令には、処理内容として擬似属性 (pseudo attribute) を記述することがある。擬似属性は、記述のしかたが属性名と属性値のペアに似ている。しかしXMLプロセサは擬似属性を、属性として解釈せず、処理命令の処理内容として解釈する。

擬似属性を使った処理命令の例を次に示す。 これはXML文書に[カスケーディングスタイルシート](../Page/Cascading_Style_Sheets.md "wikilink") (CSS) と関連づけるという処理命令である。

``` xml
<?xml-stylesheet type="text/css" href="monobook.css"?>
```

あるXML文書内に記述された特定の処理命令について、その処理命令をプログラマーが意図したとおりの処理を実行させるためには、そのXML文書を処理するアプリケーションソフトウェア側がその処理命令に対応する必要がある。

### CDATAセクション

XML文書 （およびSGML文書） において**CDATAセクション**とは、文字列データのみで構成されておりマークアップされたデータは含まれていないと、XMLプロセサが解釈するようマークされた、要素の内容を構成する文字列データの一部である。CDATAセクションは、文字列データを表現するための単なる代替構文である。 CDATAセクションとして宣言された文字列データと、"`<`" と "`&`" を "`<`" と "`&`" で表現する通常の構文で記述した文字列データとの間に、意味的な違いはない。

#### CDATAセクションの構文と解釈

CDATAセクションは次の記述で始まる。

`<![CDATA[`

そしてCDATAセクションの内容が続き、次の記述が最初に出現したところでCDATAセクションは終わる。

`]]>`

CDATAセクションの内容の文字列は全て文字列データとして解釈され、マークアップや実体参照や文字参照として解釈されることはない。

次の例で「送信者」の開始タグと終了タグはマークアップとして解釈される。

<送信者>`星新一`</送信者>

しかし次のように記述した場合は、

`<![CDATA[<送信者>星新一</送信者>]]>`

次のように記述したものと同等に解釈される。

`<送信者>星新一</送信者>`

すなわち、「送信者」タグは「星新一」の文字列と同列に位置づけられ、いずれも文字列データとして解釈される。

文字参照 `ð` が要素の内容で出現した場合は、一つの[Unicode](../Page/Unicode.md "wikilink")文字  ("ð") として解釈される。しかしCDATAセクション内で出現した場合は、8つの文字からなる文字列として解釈される。 すなわち、アンパサンド、\#マーク、文字x、数字0、数字0、文字F、数字0、セミコロンの8つの文字からなる文字列として解釈される。

### 整形式XML文書を書くために

整形式XML文書は、とりわけ、次に示す規則に適合しなければならない。

  - 空要素ではない要素は開始タグと終了タグの両方によって境界が定められる。
  - 空要素は空要素タグ （自分自身で開始タグと終了タグの2つの機能を兼ねるタグ） で記述することができる。例えば <私は空です/> のように記述することができる。この例は <私は空です></私は空です> と意味的に同等である。
  - 属性値は全てシングルクォート (') かダブルクォート (") のいずれかで括る。シングルクォートで始められた属性値はシングルクォートで終わり、ダブルクォートで始められた属性値はダブルクォートで終わる。
  - タグは入れ子の構造をとることができる。ただしタグがオーバーラップしてはならない。ルート要素ではない要素のおのおのは、必ず別の要素に含まれる。
  - XML文書は宣言された[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink") （[文字コード](../Page/文字コード.md "wikilink")） にしたがって記述される。文字符号化方式は、 XML文書が[HTTPを介して転送される場合に](../Page/Hypertext_Transfer_Protocol.md "wikilink") "Content-Type" ヘッダをつけるように暗黙的にXML文書の外部で指定しても良いし、XML文書の内部で文書の先頭のXML宣言内で宣言しても良い。このような宣言がない場合、[Unicode](../Page/Unicode.md "wikilink")の文字符号化方式が使われていると仮定される。XML文書の最初の[バイトをみて](../Page/バイト_\(情報\).md "wikilink")、[UTF-16](../Page/UTF-16.md "wikilink")の[バイト順マークと合致すればUTF](https://ja.wikipedia.org/wiki/バイトオーダーマーク "wikilink")-16であると仮定する。合致しない場合は[UTF-8](../Page/UTF-8.md "wikilink")であると仮定する。

要素の名前ではアルファベットの大文字と小文字とが区別される。 例えば、次の例は整形式である。

<Abc>` ... `</Abc>

しかし次の例は整形式ではない。

<ABC>` ... `</abc>

XML文書のスキーマを設計する際に、XMLの要素の名前を注意深く選択すると、そのスキーマに準拠したXML文書のデータの意味を、第三者に伝えるために有効であろう。XMLの要素の名前を注意深く選択することにより、そのスキーマに準拠したXML文書は、人間にとって読みやすいものとなる。

XMLの要素と属性の名前を、体が名を表すように注意深く選択決定することで、人間がXML文書を読む際に、要素と属性の意味を、外部の説明文書を参照することなく、よりよく理解できるようになる利点が生まれる。 ただしこのような作業を行うことは、XML文書の冗長性が増えることでもある。 人によっては、XML文書を書く際の労力が増えることを、好まない場合がある。またファイルサイズも大きくなることになる。 ただし[圧縮技術をXML文書に適用してファイルサイズを小さくすることは可能である](../Page/可逆圧縮.md "wikilink")。

整形式XML文書を正確に書くためには、ここまで述べたことよりずっと多くの規則にしたがう必要がある。例えば、[XML名前空間を使うことや](https://ja.wikipedia.org/wiki/#XML名前空間 "wikilink")、XMLでの「名前」として使うことができる正確な文字集合を使って、XML文書を書くことなどである。とはいえ、ここまで述べた整形式文書に関する概略を理解しておけば、多くのXML文書を読み理解しあるいは多くのXML文書を書くために必要な基礎は、身についたといえる。

### 自動的に検査する

XML文書の正当性を自動的に検査するための方法を説明する。

あるXML文書が、整形式XML文書としての条件のみを満たした文書であるか、それとも妥当なXML文書としての条件をも満たした文書であるかを、判別することは、比較的容易である。というのも、整形式XML文書であるための規則と、XMLの妥当性検証のしくみについては、XML文書を扱うツールの[移植性](../Page/移植性.md "wikilink")を考慮して設計されているからである。つまりこの設計方針は、XML文書を扱うツールであれば、どのようなXML文書でも扱うことができるということである。

独立したツールを使い、XML文書の正当性を自動的に検査する例を示す。

  - XML文書を扱える[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")で、例えば [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") や [Internet Explorer](../Page/Internet_Explorer.md "wikilink") などで、XML文書をロードする。
  - xmlwf のようなツールを使う （XMLプロセサの実装の一つである  に通常は同梱されている）。
  - 何らかの[プログラミング言語](../Page/プログラミング言語.md "wikilink")を使って文書を構文解析する。例えばプログラミング言語[Rubyでは次のようになる](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")。

`irb> require "rexml/document"`
`irb> include REXML`
`irb> doc = Document.new(File.new("test.xml")).root`

## XML文書の論理的構造と妥当なXML文書

妥当なXML文書について詳しく説明する。

XMLでは、要素に名前を付けることができ、階層構造をとることができ、[スキーマ言語](../Page/スキーマ言語.md "wikilink") (Document Type Definition など) により用途に沿うように定義されたスキーマを使うことで要素と属性の意味を公開し説明することができる。XMLのこうした特徴により、目的に応じたXMLに準拠した[マークアップ言語](../Page/マークアップ言語.md "wikilink")を創るための、構文的な基礎が成り立っている。

スキーマは、制約の集合を記述することにより、XML文書の構文上の規則を単に補足するのみである。スキーマは、多くの場合、要素と属性の名前を限定し、各要素が内容とするものの階層構造を規定し、属性の内容を規定する。例えば、「誕生日」という名前の要素では、「月」という名前の一つの要素と「日」という名前の一つの要素をもつことができ、「月」要素と「日」要素のそれぞれは文字列データのみをもつことができる。

スキーマに定義された制約には、[データ型](../Page/データ型.md "wikilink")の割り当てを含むことができる場合がある。 データ型を割り当てることにより、データ型が割り当てられた情報がどのように処理できるかを、規定することができる。 例えば、「月」要素の文字列データは、そのXML文書で採用したスキーマ言語の機能に準拠して、「1」から「12」までの数字のみが妥当であるという形で、定義することができる可能性がある。ここでスキーマ言語の (データ型に関する) 機能とは、おそらく特定の方法で形式にしたがって記述しなければならないということだけでなく、別のデータ型の値であるかのように処理されることを未然に防ぐことを、意味する。

何らかのスキーマに準拠したXML文書は、整形式であるということに加えて、**妥当** (valid) であるということが成り立つ。

XMLのスキーマは、XMLの文書型 (文書の種類、文書の論理的構造) を記述したものである。 多くの場合スキーマは、その文書の構造と内容に関する制約という形で表現される。XMLのスキーマは、XML仕様で規定されている、整形式XML文書としての基本的な制約に加え、それ以上の制約をXML文書に課すことができる。XMLのスキーマ言語は、標準規格のものもプロプライエタリなものも含めて、こうしたスキーマを表現するという目的のもと、数多く存在している。いくつかのスキーマ言語では、スキーマ自身をXML文書として記述する。

スキーマ言語の記述能力はスキーマ言語ごとにさまざまである。例えばスキーマ言語の一つである Document Type Definition (DTD) では、XML文書がとるべき構造の主な規則として、そのDTDに準拠したXML文書で使うことができる要素の名前、要素の内容モデル、要素で指定できる属性の名前、属性の値のデータ型を、記述することができる\[10\]。

なお、要素の**内容モデル**とは、要素の内容に出現可能な要素やデータとその順番、および要素の出現回数を規定したもののことをいう\[11\]。

[Standard Generalized Markup Language](../Page/Standard_Generalized_Markup_Language.md "wikilink") (SGML) やXMLなどの汎用的なデータ記述言語が世に出る前は、ソフトウェア設計者は、複数の[プログラムの間でデータの受け渡しをするために](../Page/プログラム_\(コンピュータ\).md "wikilink")、自分自身で[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")を定義するか、ちょっとした[コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")を定義しなければならなかった。このため受け渡しするデータの詳細な仕様やその他の文書を書かなければならなかったし、文書の書き手を別途に確保しなければならないこともあった。

XMLが一定の構造をもち厳密な構文解析の規則をもつことで、ソフトウェア設計者は構文解析の作業を標準的な[ソフトウェア](../Page/ソフトウェア.md "wikilink")ツール (妥当性検証器、バリデータ) に任せることができる。そしてXMLには、用途に特有の言語を開発するための一般的な、[データモデル](../Page/データモデル.md "wikilink")指向の枠組みがある。 このためソフトウェア開発者は、比較的高水準の抽象度において、自分たちが扱うデータの規則の開発に専念するだけでよい。

XML文書をスキーマに照らして妥当性検証を行うための、十分にテストされたツールが、数多く存在している。XML文書をスキーマに照らして妥当性検証を行うためのツールを、妥当性検証器 (バリデータ) という。妥当性検証器は、スキーマに表現された制約にXML文書が準拠しているかについて、自動的に妥当性検証を行う。 妥当性検証器は、XMLプロセサ ([XMLパーサ](https://ja.wikipedia.org/wiki/XMLパーサ "wikilink")) に含まれていることもあれば、XMLプロセサとは別に提供されていることもある。

これまでに述べたスキーマの使い方とは別の使い方も存在する。 例えば、XMLエディタは、XML文書の編集を支援するためにスキーマを使うことができる。こうしたXMLエディタでは、妥当な要素名や妥当な属性名を提示することなどができる。

### Document Type Definition (DTD、文書型定義)

XMLのための最も歴史の古いスキーマ言語は Document Type Definition (DTD、文書型定義) である。DTDは、XMLの前身である[SGMLから引き継がれた](../Page/Standard_Generalized_Markup_Language.md "wikilink")。DTDは XML 1.0 標準に含められているため、ほとんどあらゆるXMLプロセサがDTDを扱うことができる。しかし2007年現在ではDTDを使うことは限定的な範囲にとどまっているようである。その理由は次のとおりである。

  - DTDではXMLで新しく開発された機能を使うことができない。特に[XML名前空間を扱えないことが厳しい](https://ja.wikipedia.org/wiki/#XML名前空間 "wikilink")。
  - DTDは表現力が乏しい。DTDではいくつかの形式的な視点からXML文書を扱うことができない。
  - DTDによるスキーマはXMLではない独自の構文で記述する。この構文は、XMLの前身であるSGMLから引き継いでいるという、経緯がある。XML 1.0 の制定当時はDTD以外のスキーマ言語は存在しなかった。

DTDは現在も多くの用途で使われている。その理由は、一定の人々にとってはDTDは他の新しいスキーマ言語よりも読みやすく書きやすいと考えられているからである。

#### XML Schema

XML Schema は、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) により開発された、DTDの後継となる新しいスキーマ言語である。 非公式には、**XSD**と呼ばれることもある。XSDは、XML Schema の[インスタンス](../Page/インスタンス.md "wikilink") (スキーマ) を意味する "XML Schema Definition" の[頭字語](../Page/頭字語.md "wikilink")である。

XML Schema は、豊富な[データ型](../Page/データ型.md "wikilink")を扱うことができるスキーマ言語である。XML文書の論理的構造について、DTDより詳細な制約を記述することができる。そしてDTDより詳細な妥当性検証の枠組みのもとで、妥当性検証が行われる。他にも、XMLによるマークアップ言語のスキーマの記述能力において、DTDと比べて非常に高いという長所も備えている。

また、XML Schema によるスキーマ自体を、XMLに準拠した形式を使って記述する。XML Schema のスキーマ自体がXMLに準拠することで、スキーマを編集したりスキーマに何らかの処理を行うために、普通のXMLツールを使うことができるようになる。

ただし、XML Schema の妥当性検証器を実装する作業には、単にXML文書を読むことができる能力よりも、非常に多くの知識と能力を必要とする。

XML Schema に対しては賛否両論がある。XML Schema に対する批判の一部を示す。

  - XML Schema の仕様は非常に膨大な分量がある。そのため XML Schema を理解することは難しい。またそのため XML Schema の妥当性検証器を実装することも難しい。
  - XML Schema でスキーマを記述する際、XMLに準拠した構文で記述する (記述しなければならない) のは、冗長である。このことが XML Schema のスキーマを理解することやスキーマを記述することを、DTDよりしんどい作業にしてしまっている。
  - XML文書の構文解析をした後に行う、XML Schema のスキーマによる妥当性検証は、費用が高くつく可能性がある。特にサイズの大きいXML文書の妥当性検証を行う際には、深刻な問題になる可能性がある。
  - XML Schema の[データモデリング](https://ja.wikipedia.org/wiki/データモデリング "wikilink")能力は非常に限られている。属性の内容によってその要素の内容モデルを変更することはできない。
  - XML Schema における型派生モデルは、非常に限られた能力しかない。特に拡張による派生は、かなり使いにくい。
  - [データベース](../Page/データベース.md "wikilink")と連携するためのデータ転送機能は、不可解な考え方によって実現されている。nillability ([SQL](../Page/SQL.md "wikilink")データベース用語でいう[NULLに相当する状態をとることが可能であるという特性](https://ja.wikipedia.org/wiki/Null "wikilink")) は備えているが、出版業界の要件は満たしていない。
  - key/keyref/uniqueness の機構は、データ型を考慮していない。
  - スキーマ検証後[情報集合](https://ja.wikipedia.org/wiki/#XML情報集合 "wikilink") (PSVI、Post Schema Validation Infoset) の概念は、標準のXML表現や[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (API) をもたない。このため、妥当性の再検証を行わない場合、ベンダ非依存の考え方に反する ([\#情報集合への追加情報](https://ja.wikipedia.org/wiki/#情報集合への追加情報 "wikilink")を参照)。

#### RELAX NG

RELAX NGは人気のあるもう一つの新しいスキーマ言語である。2001年12月に[OASIS](../Page/OASIS_\(組織\).md "wikilink") (構造化情報標準促進協会) で仕様が策定された。[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") (国際標準化機構) にて定められた国際標準でもある。ISOでは、[文書スキーマ定義言語](../Page/文書スキーマ定義言語.md "wikilink") (DSDL) の一部分を構成する仕様として位置づけられている。

RELAX NGのスキーマの記述方法は、2つの形式がある。XMLに準拠した構文 ([XML構文](https://ja.wikipedia.org/wiki/RELAX_NG#XML構文 "wikilink")、xml syntax) と、XMLに準拠しない[短縮構文](https://ja.wikipedia.org/wiki/RELAX_NG#短縮構文 "wikilink") (compact syntax) である。短縮構文は、読みやくすることとより書きやすくすることを目指している。ただし、短縮構文で記述されたスキーマをXML構文のスキーマに変換する方法と、その逆の変換を行う方法は、予め定義されているので、[ジェームズ・クラークが開発した](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink") [Trang conversion tool](http://www.thaiopensource.com/relaxng/trang.html) を使えば、標準のXMLツールを使う利便を享受することができる。

RELAX NGはXML Schemaよりも簡潔なスキーマ定義と簡潔な妥当性検証の枠組みを、備えている。そのためRELAX NGは、XML Schema と比べて、使いやすく、またRELAX NGの妥当性検証器を実装することも容易になっている。

RELAX NGもまた、[データ型](../Page/データ型.md "wikilink")フレームワークプラグインを使う機能を備えている。 RELAX NG でスキーマを記述する人は、例えば、XML文書でXML Schemaのデータ型の定義に適合させたいと考えるかもしれない。 そして RELAX NG では、データ型フレームワークプラグインを使うことにより可能となっている。

#### ISO 文書スキーマ定義言語

[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") [文書スキーマ定義言語](../Page/文書スキーマ定義言語.md "wikilink") (DSDL; Document Schema Description Languages) 標準は、小規模なスキーマ言語の広範なセットを共に提供する。DSDLを構成する複数の仕様のそれぞれが、特定の問題に対応するために特化されている。DSDLはRELAX NGのXML構文と短縮構文、[スキマトロン](../Page/スキマトロン.md "wikilink")、データ型ライブラリ言語、文字レパートリ記述言語、文書スキーマ再命名言語、名前空間に基づく検証委譲言語 (NVDL) を、含んでいる。DSDLスキーマ言語群はXML Schemasを支持するベンダの支援は2007年の時点ではまだ受けていない。DSDLは[出版](../Page/出版.md "wikilink")のための機能が欠如していることに対する、出版業界の一定の草の根の反応でもある。

### XML文書を検証する過程でXML情報集合を変更することについて

いくつかのスキーマ言語では、特定のXML文書の構造を記述する能力に加えて、個々のXML文書をその特定のXML文書構造に適合するように変換する機能も、限定的ながら備えている。

DTDとXML Schemaはこの変換機能を備えている。 DTDと XML Schema では、XML文書に属性の既定値を与えることができる。RELAX NGとスキマトロンは、意図的にこの機能を外している。 例えば、[XML情報集合を正確に扱うことが](https://ja.wikipedia.org/wiki/#XML情報集合 "wikilink")、RELAX NGとスキマトロンの仕様策定時に変換機能を外した理由の一つである。

## XML文書を視覚的に表示する

XML文書を視覚的に表示するための方法を説明する。

XML文書は、その文書の内容をどのように視覚的に表示するかという情報を、一切含んでいない。 [Cascading Style Sheets](../Page/Cascading_Style_Sheets.md "wikilink") (CSS) や [Extensible Stylesheet Language](../Page/Extensible_Stylesheet_Language.md "wikilink") (XSL) のようなXMLのための[スタイルシート言語](https://ja.wikipedia.org/wiki/スタイルシート言語 "wikilink")を使うのでなければ、ほとんどの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")は普通のXML文書を生のXMLテキストとして描画する。いくつかのウェブブラウザは「ハンドル」をつけて表示する (例えば、余白に + と - の符号を表示する)。ハンドルを使うことにより、XML文書構造の部分木を、マウスクリックで展開したり折りたたんだりすることができる。

CSSを使って[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")でXML文書を描画するためには、XML文書は次のような要領で[スタイルシート](../Page/スタイルシート.md "wikilink")への参照を含めなければならない (XMLの[処理命令を使ってスタイルシートを使って描画する旨を指定している](https://ja.wikipedia.org/wiki/#処理命令 "wikilink"))。

``` xml
<?xml-stylesheet type="text/css" href="myStyleSheet.css"?>
```

この方法は、[HTML文書におけるスタイルシート指定の方法とは異なる](../Page/HyperText_Markup_Language.md "wikilink")。HTML文書では <link/> 要素を使ってスタイルシートを指定する。

XML文書を視覚的に表示するために、[Extensible Stylesheet Language](../Page/Extensible_Stylesheet_Language.md "wikilink")（XSL、拡張可能なスタイルシート言語）を使うこともできる。XSLを使う場合は、XML文書を[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")/HTML文書の構造に変換するか、もしくはウェブブラウザで視覚的に表示することができる他の文書の構造に変換する。

クライアント側で[XSL Transformations](../Page/XSL_Transformations.md "wikilink") (XSLT) のスタイルシートを指定するためには、XML文書に次のようにXSLTスタイルシートへの参照を含めることが、必要である（XMLの処理命令を使って実現している）。

``` xml
<?xml-stylesheet type="text/xsl" href="myTransform.xslt"?>
```

クライアント側のXSLTスタイルシート処理機能は、現在では多くのウェブブラウザが備えている。

別の方法として、このような利用者が常用しているウェブブラウザの能力に依存する方法を採らずに、サーバ側でXSLを使ってXML文書を視覚化可能な形式に変換する方法も、行われている。利用者は、「舞台の裏側で」何が行われているかを、意識する必要はない。実際に目にするものは、よく整形され視覚化された文書だけである。

## XMLの拡張

XMLを拡張する技術を説明する。

  - [XML Path Language](../Page/XML_Path_Language.md "wikilink") (XPath)
    XML Path Language (XPath) を使うと、XML文書の個々の部分を参照することができるようになる。XPathは、[XSLT](../Page/XSL_Transformations.md "wikilink")、[XSL-FO](../Page/XSL_Formatting_Objects.md "wikilink")、[XQuery](../Page/XQuery.md "wikilink") などの他の技術に対して、XML文書のデータに対する[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")を行う機能を、提供する。XPathで記述された式は、XML文書を構成するXML要素、属性、処理命令、コメントなどの内側の、テキスト、データ、値を参照することができる。XPathの式は、要素の名前と属性の名前にアクセスすることもできる。Xpathは、妥当なXML文書に対しても整形式XML文書に対しても使うことができる。また名前空間が定義されたXML文書に対しても、名前空間が定義されていないXML文書に対しても使うことができる。
  - [XML Inclusions](https://ja.wikipedia.org/wiki/XML_Inclusions "wikilink") (XInclude)
    XML Inclusions (XInclude) の仕様は、XML文書内に外部ファイルの全内容もしくは外部ファイルの一部の内容を含める機能を、定義している。XML文書においてXIncludeの処理が終了すると、XInclude処理終了後の[XML情報集合にはXIncludeの要素はなく](https://ja.wikipedia.org/wiki/#XML情報集合 "wikilink")、XIncludeの要素の代わりにそこに外部の文書もしくは文書の一部の複製が、最終的な情報集合に含まれている。XIncludeでは、外部文書の一部をXML文書に含める際に、外部文書の複製対象の領域を参照するためにXPathを使っている。
  - [XQuery](../Page/XQuery.md "wikilink")
    XQueryは、XMLにおいて、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")にとっての[SQL](../Page/SQL.md "wikilink")や[PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")に相当する、[問い合わせ言語](https://ja.wikipedia.org/wiki/問い合わせ言語 "wikilink")としての機能を提供する。XML文書にアクセスし、XML文書を操作（編集）し、その結果をXML文書の形で返す。
  - [XML名前空間](https://ja.wikipedia.org/wiki/#XML名前空間 "wikilink") (Namespaces in XML)
    XML名前空間 (Namespaces in XML) を使うことで、同一のXML文書内で異なる複数の[ボキャブラリ](../Page/語彙.md "wikilink")（スキーマ）に由来する要素と属性を、名前の衝突を発生させることなく、含めることができる。[後述する](https://ja.wikipedia.org/wiki/#XML名前空間 "wikilink")。
  - [XML Signature](https://ja.wikipedia.org/wiki/XML署名 "wikilink")
    XML Signature の仕様は、XML文書の内容に対して[電子署名](../Page/電子署名.md "wikilink")を生成するための構文と処理規則を定義する。
  - [XML Encryption](https://ja.wikipedia.org/wiki/XML暗号化 "wikilink")
    XML Encryption の仕様は、XML文書の内容に対して[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")を行うための構文と処理規則を定義する。
  - [XML Pointer Language](https://ja.wikipedia.org/wiki/XPointer "wikilink") (XPointer)
    XML Pointer Language (XPointer) は、XMLに基づいたインターネットメディアのコンポーネントを指し示す体系である。

### MIMEタイプ

XML文書はさまざまな[MIMEタイプで配布することができる](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")。RFC 3023 は、"application/xml" および "text/xml" のMIMEタイプを定義する。 "application/xml" と "text/xml" のMIMEタイプは、そのデータがXML文書の形式をとっているということのみを述べているだけであり、そのXML文書の論理的構造については何も述べていない。 "text/xml" を使うことに対しては、符号化に関する問題が生じる可能性があるとの批判があり、現在では非推奨とされている\[12\]。RFC 3023 では、加えて、XML文書を "application/" で始まり、"+xml" で終わるMIMEタイプで配布することを勧めている。例えば、[AtomのXMLデータに対しては](../Page/Atom_\(ウェブコンテンツ配信\).md "wikilink")、"application/atom+xml" のMIMEタイプで配布するのである。

### XML名前空間

**XML名前空間** (**Namespaces in XML**) は、一つXML文書内で、異なる複数の[ボキャブラリ](../Page/語彙.md "wikilink")（スキーマ）に由来する要素と属性を、名前の衝突を発生させることなく、含めることができるようにするための仕様である。[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) から、1999年1月14日に Namespaces in XML 1.0 が勧告された。XML文書に異なる複数のボキャブラリに由来する要素と属性を含める場合、ボキャブラリのそれぞれに[名前空間](../Page/名前空間.md "wikilink")をわりあてることにより、要素名の衝突と属性名の衝突の問題を、解決することができる。

一つの名前空間において定義された要素の名前は、一意でなければならない。

顧客への参照と注文された商品への参照を含む簡単なXML文書の例を考える。顧客要素と商品要素は、ともに「識別番号」という名前の子要素をもつことがあるだろう。識別番号要素への参照は、顧客要素の子要素の識別番号要素も商品要素の子要素の識別番号要素も同じ要素名をもつので、あいまいである。しかし2つのボキャブラリを区別する2つの名前空間のもとで識別番号要素を使う場合、顧客要素の子要素の識別番号要素と商品要素の子要素の識別番号要素は意味的に明確に異なる2種類の要素となる。

#### 名前空間の宣言

名前空間は、XMLの予約属性である `xmlns` を使って宣言される。`xmlns`属性の属性値は[IRI](../Page/Internationalized_Resource_Identifier.md "wikilink") (Internationalized Resource Identifier) である必要があり、通常は[URI](../Page/Uniform_Resource_Identifier.md "wikilink") (Uniform Resource Identifier) である。

例を示す。

`ns="http://www.w3.org/1999/xhtml"`

この例の "http://www.w3.org/1999/xhtml" を名前空間名という。ここで注意すべきこととしては、名前空間の宣言で記述されたURIは、実際にインターネット上の住所として解釈されるわけではないということである(自由に考えよう、URIほど便利なものが必ずインターネットのアドレスをささなければいけないなどと、誰が決めたのか)。例えば、\[<http://www.w3.org/1999/xhtml> [http://www.w3.org/1999/xhtml\]自体には何のコードもない。このURIの文書では、人間の読者に対して](http://www.w3.org/1999/xhtml%5D自体には何のコードもない。このURIの文書では、人間の読者に対して)[XHTMLについて簡単に説明しているだけである](../Page/Extensible_HyperText_Markup_Language.md "wikilink")。 ("http://www.w3.org/1999/xhtml" のような) URIを名前空間の識別子として使うことで、（"xhtml" のような）単純な文字列を名前空間名として使うよりも、異なる名前空間が意図せずして同じ名前空間名を使ってしまう危険性を低減する。名前空間の識別子は、ウェブの住所（アドレス）の慣習にしたがう必要はない。

名前空間の宣言は短い接頭辞を含むことができる。この名前空間接頭辞を使うことで、異なるボキャブラリに由来する要素と属性を識別することができる。

名前空間接頭辞を使う例を示す。

`xmlns:xhtml="http://www.w3.org/1999/xhtml"`

XML名前空間を使ったXML文書の例を示す。

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0" ns="http://www.w3.org/1999/xhtml">
 <xsl:template match="/社員名簿">
  <html>
   <head>
    <title>XML文書をXHTML文書に変換する例</title>
   </head>
   <body>
    <h1>社員名簿</h1>
    <ul>
     <xsl:apply-templates select="社員">
      <xsl:sort select="姓"/>
     </xsl:apply-templates>
    </ul>
   </body>
  </html>
 </xsl:template>
 <xsl:template match="社員">
  <li>
   <xsl:value-of select="姓"/> <xsl:value-of select="名"/>
  </li>
 </xsl:template>
</xsl:stylesheet>
```

このXML文書は、次の2つの名前空間のボキャブラリから構成されている。

  - [XSLTのボキャブラリ](../Page/XSL_Transformations.md "wikilink"): xslの名前空間接頭辞をもち、名前空間名は "http://www.w3.org/1999/XSL/Transform"。
  - [XHTMLのボキャブラリ](../Page/Extensible_HyperText_Markup_Language.md "wikilink"): 名前空間接頭辞をもたないデフォルトの名前空間であり、名前空間名は "http://www.w3.org/1999/xhtml"。

なおこのXML文書は、あるXML文書をXHTML文書に変換するXSLTスタイルシートである。

XML名前空間を使う場合、そのXML名前空間のボキャブラリが定義されていることが必要であるわけではない。しかしXML文書でXML名前空間を使う場合に、そのXML名前空間のボキャブラリを定義しておくことは、そのXML名前空間のURIのもとで正しい文書構造を定義しているスキーマに関連づけるために、行われることが多い。

## XML文書をプログラムで処理する

[プログラマ](../Page/プログラマ.md "wikilink")や[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")がXML文書を処理する手段としては、これまで次に示す3つの技法が伝統的に使われてきた。なお、この節の説明で使うAPIとは[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink")のことをさす。

  - [プログラミング言語](../Page/プログラミング言語.md "wikilink")と [SAX](../Page/Simple_API_for_XML.md "wikilink") API を使う。
  - プログラミング言語と [DOM](../Page/Document_Object_Model.md "wikilink") API を使う。
  - 変換エンジンと[フィルタを使う](../Page/フィルタ_\(ソフトウェア\).md "wikilink")。

さらに、近年に開発され使われるようになった、XML文書を処理する技法を示す。

  - Pull Parsing
  - データバインディング

### Simple API for XML (SAX)

Simple API for XML (SAX) は、[字句解析](../Page/字句解析.md "wikilink")を行い[イベント駆動で処理を行う](../Page/イベント駆動型プログラミング.md "wikilink") API である。SAXを使うとXML文書は文書の最初から順次読み込まれ、その内容は[プログラマ](../Page/プログラマ.md "wikilink")が実装したハンドラ[オブジェクトの様々な](../Page/オブジェクト_\(プログラミング\).md "wikilink")[メソッドへの](../Page/メソッド_\(計算機科学\).md "wikilink")[コールバックとして報告される](../Page/コールバック_\(情報工学\).md "wikilink")。SAXを使ったXML文書処理は高速であり、少ないコンピュータ資源を効率的に使って非常にサイズの大きいXML文書を処理することが可能である。

SAXを使うことに伴う問題は、XML文書に対して[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")を行って情報を取り出すことが難しいことである。そのため、SAXを使うに際し、[プログラマ](../Page/プログラマ.md "wikilink")はXML文書のどの部分が現在処理対象となっているか把握する為の機構を実装しなければならない。

SAXは、処理対象となるXML文書中のある種類の情報がどの部分に出現するかに依らず、常に同じように処理されると保証できる場合に用いるのが望ましい。

### Document Object Model (DOM)

Document Object Model (DOM) は、[インタフェース指向の](../Page/インタフェース_\(情報技術\).md "wikilink")[APIであり](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、XML文書のおのおのの部分を表現する節[オブジェクトの集まりからなる](../Page/オブジェクト_\(プログラミング\).md "wikilink")[木構造であるかのように](../Page/木構造_\(データ構造\).md "wikilink")、XML文書全体に対してナビゲーションを行うことを想定している。DOMでは、XML文書に対して[ランダムアクセス](../Page/ランダムアクセス.md "wikilink")を行って情報を取り出すことが、簡単にできる。

DOMにおけるXML文書全体に相当する `Document` オブジェクトは、XML文書をXMLプロセサが処理することにより生成することもできるし、プログラマがプログラミングすることによって生成することもできる。DOMにおける `Node` (節) のさまざまな型の[データ型](../Page/データ型.md "wikilink")は、DOM仕様においては抽象的にインタフェースとして定義されている。`Node` のデータ型の[実装](../Page/実装.md "wikilink")は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")に固有の言語バインディングを提供する。 DOMの実装は、サイズの大きいXML文書を扱う場合はたくさんのメモリを使う。なぜならDOMの実装は、一般的にはXML文書全体からオブジェクトの木構造を構築してメモリにロード（展開）し、その後にDOMを介した処理をできるようにしているからである。

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")では、標準ライブラリを構成するいくつかのパッケージでDOMが実装されており、Javaの[プログラマ](../Page/プログラマ.md "wikilink")は標準ライブラリのDOMを使うことができる。DOMの仕様は、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) で策定されているため、DOMで中核をなす `Node` や`Document` などのインタフェースや、[直列化](https://ja.wikipedia.org/wiki/直列化 "wikilink") (出力) などの機能を提供するためのインタフェースはパッケージ `org.w3c.dom.*` に収められている。 \[13\]

### 変換エンジンとフィルタ

[Extensible Stylesheet Language](../Page/Extensible_Stylesheet_Language.md "wikilink") (XSL) 技術における[フィルタは](../Page/フィルタ_\(ソフトウェア\).md "wikilink")、XML文書に対して、視覚的に出力したり印刷出力できるよう変換処理を行うことができる。

  - [XSL Formatting Objects](../Page/XSL_Formatting_Objects.md "wikilink") (XSL-FO)
    XSL Formatting Objects (XSL-FO) は、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) が策定した、XMLに準拠した宣言的なページ整形 ([組版](../Page/組版.md "wikilink")) 言語である。XSL-FO処理系を使うと、XSL-FO文書を他の非XML形式 ([PDFなど](../Page/Portable_Document_Format.md "wikilink")) に変換出力することができる。
  - [XSL Transformations](../Page/XSL_Transformations.md "wikilink") (XSLT)
    XSL Transformations (XSLT)は、W3Cが策定した、XMLに準拠した宣言的な文書[変換言語](https://ja.wikipedia.org/wiki/変換言語 "wikilink")である。XSLT処理系を使うと、XSLT[スタイルシート](../Page/スタイルシート.md "wikilink")を指示書として、XML文書として表現されたあるデータの木構造を、別の木構造に変換することができる。変換後の文書として、XML (例えば、XSL-FO文書やXHTML文書など)、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")などの形式にすることができる。またXSLT処理系によってはこの他の形式に変換できるものもある。
  - [XQuery](../Page/XQuery.md "wikilink")
    XQueryは、W3Cが策定した、XML文書に対する、問い合わせ、構築、変換を行うための、コンピュータ言語 ([問い合わせ言語](https://ja.wikipedia.org/wiki/問い合わせ言語 "wikilink")) である。
  - [XML Path Language](../Page/XML_Path_Language.md "wikilink") (XPath)
    XML Path Language (XPath) は、W3Cが策定した、XML文書中のデータを取得するための、DOMに似たノードの集まりからなる木構造を[データモデル](../Page/データモデル.md "wikilink")とするパス式言語である。 XSLTおよびXQueryの技術はXPathを使って実現されている。XPathの実装はまた、便利な[関数](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")を含んでおり使うことができる。

### Pull Parsing

Pull Parsing は、XML文書を、最初から順番に読み込み、[Iterator パターン](https://ja.wikipedia.org/wiki/Iterator_パターン "wikilink") の[デザインパターンを使って項目](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink") (item) の一連の流れとして扱う、近年に徐々に普及してきた技法である\[14\]\[15\]。 Pull Parsing の技法により、再帰下降パーサを実装することができる。 再帰下降パーサでは、パースを実行するプログラムは、パースの対象となるXML文書の構造と似ている。 そしてパースの中間結果を取得することができる。

パースの中間結果を、パースを実行する[メソッド内の局所変数](../Page/メソッド_\(計算機科学\).md "wikilink") (ローカル変数) として使うことができる。 あるいは、低水準のメソッドの引数として渡したり、高水準のメソッドへの戻り値として返すことができる。 Pull Parsing の技法を提供する実装としては次のものがある。

  - [Streaming API for XML](../Page/Streaming_API_for_XML.md "wikilink") (StAX) - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - SimpleXML - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - `System.Xml.XmlReader` - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")

例えば、JavaのStAXフレームワークでは、本質的な「[反復子](../Page/イテレータ.md "wikilink")」 (イテレータ) を作成して使うことができる。

Pull Parsing で作成される「反復子」はXML文書中のさまざまな要素、属性、データを順番に訪れる。 「反復子」を使うプログラムは、処理中に現在の項目 (例えば、要素の開始、要素の終了、テキスト) を調べ、その特性 (例えば、要素の 名前、名前空間、属性値、テキスト内容) を調査する。 そして反復子に「次の」項目へ移動するよう指示することもできる。 プログラムは、このようにXML文書を走査するようにして、文書から情報を取り出すことができる。

Pull Parsing の技法の特筆すべき長所は、XML文書をパースする DOMの技法と比べて非常に高速であり、メモリ使用が非常に少ないことである。 もう一つの長所は、再帰下降の手法は、パースを実行するプログラム内で、データを型づけされた変数として保持することに適していることである。 SAXでは、例えば、プログラマが自分で処理中の要素の祖先となる要素群を格納する[スタック](../Page/スタック.md "wikilink")内に中間データを保持するコードをプログラミングする必要があることが多い。 これに対し、Pull Parsing の技法を使ってXML文書を処理するプログラムは、SAXを使うプログラムよりも、非常に単純で理解し易く保守が容易になることが多い。

### データバインディング

XML文書を処理するもう一つのAPIは、XMLデータバインディングであり、XMLデータバインディングを使うと、XML文書を、その文書型に対応した、強く型づけされたプログラミング言語データ構造 ([プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")) を、生成することができる。インタフェース指向のDOMとは対照的な手法である。データバインディングの実現例を次に示す。

  - Relaxer\[16\]
  - [Java Architecture for XML Binding](../Page/Java_Architecture_for_XML_Binding.md "wikilink") (JAXB)\[17\]

### XMLに準拠したアプリケーションソフトウェアとエディタ

[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")、[AbiWord](../Page/AbiWord.md "wikilink")、および[アップルの](../Page/アップル_\(企業\).md "wikilink")[iWork](https://ja.wikipedia.org/wiki/iWork "wikilink")などの[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")のネイティブ[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")は、XMLである。

従前、[オフィススイート](../Page/オフィススイート.md "wikilink")には各ソフトの特有の[バイナリ](../Page/バイナリ.md "wikilink")形式として[データ](../Page/データ.md "wikilink")が保存されていた。しかしながらこれでは互換性が低く、様々な情報を[データベース](../Page/データベース.md "wikilink")として利用するオフィススイートでは不都合が生じていた。 そのため、データの標準化を進めて互換性を高めるため、各オフィススイートはXML形式でデータを出力する機能や、そもそも標準保存形式をXMLベースとするものが増えてきた。

[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")はXMLベースの保存形式を当初より標準としていた（英語版バージョン1.0は2002年5月1日リリース）。また、OpenOffice.orgに限らず、どのオフィススイートでも利用できる[OpenDocument](../Page/OpenDocument.md "wikilink")形式が[国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")（ISO）によって標準規格として認定されている。

もう一つのオフィススイート用の保存形式である [Office Open XML](../Page/Office_Open_XML.md "wikilink") も、ISOにより標準規格として認定されている。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")の [Microsoft Office](../Page/Microsoft_Office.md "wikilink") では Microsoft Office XP のバージョンからXML形式への対応を始め、Microsoft Office 2003 で独自の定義の XML Schema がサポートされるに至った。 Microsoft Office 2007 ではデフォルトの保存方式がXMLとなった（Office Open XML）。Microsoft Office 2007 のいくつかの機能では、XMLファイルを利用者が指定したスキーマ (ただしDTDではない) に沿って編集することができるようになっている。 またマイクロソフトは、Microsoft Office 2003 のためのファイルフォーマット互換性キットを公開している。 この互換性キットを使うことにより、以前のバージョンの Microsoft Office で作成された文書をXMLに準拠した新しいフォーマットで保存することができる。

エディタについては現在、多くのXMLエディタが使えるようになっている。

## XML情報集合

**XML情報集合**\[18\]\[19\] (—じょうほうしゅうごう，, ) は、XML文書の抽象的な[データモデル](../Page/データモデル.md "wikilink")を「情報項目」 (information item) の集合を使って規定している。 [World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) から、2001年10月24日にXML情報集合仕様が勧告された。 XML情報集合の仕様における定義は、整形式XML文書内の情報を参照する必要がある他の仕様において使われることが想定されている。

一つのXML文書には、そのXML文書が整形式でありかつXML名前空間の制約に準拠している場合、一つのXML情報集合がある。 XML情報集合を構成するためには、そのXML文書が妥当なXML文書であることは、必須要件ではない。

一つのXML情報集合には、次に示す11種類の情報項目がある。

  - 文書情報項目
  - 要素情報項目
  - 属性情報項目
  - 処理命令情報項目
  - 展開されなかった実体情報項目
  - 文字情報項目
  - コメント情報項目
  - 文書型宣言情報項目
  - 解析対象外実体情報項目
  - 記法情報項目
  - 名前空間情報項目

XML情報集合の Second Edition (第2版) が2004年2月4日に勧告された。

### 情報集合への追加情報

情報集合への追加情報すなわち情報集合に対する改変は、スキーマによる妥当性検証を行う際に、情報集合を改変することをいう。 例えば、情報集合に属性の既定値 (デフォルト値) を追加することなどがある。情報を追加された情報集合は、スキーマ検証後情報集合あるいはPSVI (post-schema-validation infoset) と呼ばれる\[20\]。

情報集合への追加情報については、賛否両論がある。 情報集合に情報を追加することに否定的な見解としては、情報集合への追加情報はモジュール性を侵害し相互運用性の面での問題を引き起こす危険があるとする。 なぜなら、同じXML文書を扱う複数のアプリケーションソフトウェアは、受け取る情報が妥当性検証を行うかどうかに依存してしまうからである。 アプリケーションソフトウェアが、妥当性検証を行う場合に受け取る情報と、妥当性検証を行わない場合に受け取る情報が、異なってしまうのである\[21\]。

XML Schema は、XML情報集合への追加情報を扱うことができる。 RELAX NGは、情報集合への追加情報を扱わない。 RELAX NG では、情報集合への追加情報に否定的な立場をとっている。

## 歴史

デジタルメディアの出版を行ってきた人々は、1980年の後半—[インターネット](../Page/インターネット.md "wikilink")が広く使われるようになるより前の時期—には既に、動的に情報を視覚化するための技術として、汎用的な[マークアップ言語](../Page/マークアップ言語.md "wikilink")である [Standard Generalized Markup Language](../Page/Standard_Generalized_Markup_Language.md "wikilink") (SGML) が多くの用途に適していることを、理解していた\[22\]\[23\]。 SGMLはいくつかの分野で普及していたが、仕様が複雑で[処理系](https://ja.wikipedia.org/wiki/処理系 "wikilink")の開発が難しく、またSGML文書の処理が重いという欠点があった。1990年代半ばまでには、SGMLを実際に使っていた一定の人々は、新しく現れた [World Wide Web](../Page/World_Wide_Web.md "wikilink") (ウェブ) を経験した。 そうした人々は、ウェブが発展することにより直面するいくつかの問題に対して、SGMLが解決策を提供すると、強く考えるようになった。 Dan Connolly は、自分が1995年に[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) のスタッフになった時に、SGMLをW3Cのアクティビティの一覧に追加した。 このアクティビティの作業は、1996年の中頃に[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のジョン・ボサックが、このアクティビティに関する宣言を起草しアクティビティの共同作業者を募ることで、始まった。 ボサックは、SGMLとウェブの双方を経験していた人々の小さなコミュニティと良好な関係を築いていた。 ボサックは、自分の作業において[マイクロソフト](../Page/マイクロソフト.md "wikilink")から支援を受けた。

XMLの仕様は、11人のメンバーからなるワーキンググループにより編集され\[24\]、だいたい150人から構成される Interest Group のメンバーから支援を受けて作成された。 技術的な論議が Interest Group の[メーリングリスト](../Page/メーリングリスト.md "wikilink")で提起され、提起された論議は合意形成により解決された。合意形成ができなかった場合は、ワーキンググループのメンバーの投票による多数により解決された。 このアクティビティで行われた設計上の決定とその根拠の記録は、Michael Sperberg-McQueen が1997年12月4日に編集した\[25\]。 このアクティビティでは[ジェームズ・クラークが技術リーダとして貢献した](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink")。 クラークの貢献として特筆されるのは、空要素 "<empty />" の導入と、この技術の名称 "Extensible Markup Language" (XML) の命名である。 この技術の名称として、他に提案され吟味されたものの一部を次に示す。

  - MAGMA (Minimal Architecture for Generalized Markup Applications)
  - SLIM (Structured Language for Internet Markup)
  - MGML (Minimal Generalized Markup Language)

XML仕様のワーキンググループではジョン・ボサックが議長を務めた。 このワーキンググループではジェームズ・クラークが技術リーダを務めた。 ワーキンググループの共同エディタは、もともとはティム・ブレイと Michael Sperberg-McQueen であった。 このアクティビティのプロジェクトの途中で、ブレイは[ネットスケープ・コミュニケーションズ](https://ja.wikipedia.org/wiki/ネットスケープ・コミュニケーションズ "wikilink")とのコンサルティングの契約を結んだ。 このブレイとネットスケープの契約に対しては、マイクロソフトが強く抗議した。 ブレイは、エディタの役割を一時的に辞することを要請された。 このことに関して、ワーキンググループでは激しい議論が行われた。 この議論は、最終的にはマイクロソフトの Jean Paoli が第3の共同エディタに就くことで解決した。 なおXMLワーキンググループには、日本人としてはただ一人[村田真](../Page/村田真.md "wikilink")がメンバーとして1997年に参加した。

XMLワーキンググループは、直接会って活動したことは数回しかなかった（最初の会議は1997年8月22日）。 XML仕様の設計は、電子メールと週に一度の電話会議の双方を有機的に活用することにより、成し遂げられた。 XML仕様の設計では、SGMLの欠点を解決すべく文法を簡素化した。 XML仕様における設計上のいくつかの大きな決定は、1996年の7月から11月までの間の12週間の真剣な作業のなかで行われた。 この12週間の作業の後 (1996年11月) に、XMLの最初のワーキングドラフトが公表された\[26\]。 その後も1997年をとおして設計作業は続けられ、XML 1.0 は、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[2月10日](../Page/2月10日.md "wikilink")に[W3Cの勧告となった](../Page/World_Wide_Web_Consortium.md "wikilink")\[27\]。

XML 1.0 は、ワーキンググループが目標としていた次の目標を達成したと、評価する人々が多い。

  - [インターネット](../Page/インターネット.md "wikilink")環境での使いやすさ
  - 汎用的な用途での使いやすさ
  - [SGMLとの互換性](../Page/Standard_Generalized_Markup_Language.md "wikilink")
  - XML文書を扱う[ソフトウェア](../Page/ソフトウェア.md "wikilink")の開発を容易にする機能
  - オプショナルな機能の最小化
  - XML文書の読みやすさ
  - 形式に即していること (formality)
  - 簡潔さ
  - XML文書の作成・編集の容易さ

技術者にとってはXMLはSGMLよりも習得しやすい技術であり、また処理系の開発が容易になったことで低い費用でXML技術を利用できるようになった。 現在ではXMLは広く普及している技術である。

XMLの前身であるSGMLと同様にXMLでも、いくつかの冗長な構文要素があり、要素記述子の繰り返しを仕様に含んでいる。 文書を短くすることは、XMLワーキンググループでは、XMLの構造において本質的な問題とは見なされなかった。

### 起源

XMLは、[ISO標準](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") [Standard Generalized Markup Language](../Page/Standard_Generalized_Markup_Language.md "wikilink") (SGML) のサブセットである。 XMLのほとんどはSGMLから変更されずに採り入れられている。 XMLがSGMLから採り入れられている技術的な要素には次のものが含まれる。

  - 論理的な構造と物理的な構造を分離する (要素と実体)
  - 文法に基づいた妥当性検証 (Document Type Definition (DTD、文書型定義))
  - データと[メタデータ](../Page/メタデータ.md "wikilink")を分離する (要素と属性)
  - 混合内容 (mixed content、要素の内容として子要素と文字列データが混在する内容モデル)
  - 表現から処理を分離する ([処理命令](https://ja.wikipedia.org/wiki/#処理命令 "wikilink"); processing instruction)
  - 山括弧の構文

XMLがSGMLから採り入れなかった技術要素としては、SGML宣言がある (XMLでは 文書の[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink")として[UTF-8](../Page/UTF-8.md "wikilink")と[UTF-16](../Page/UTF-16.md "wikilink")を採用している)。

XMLの他の技術的起源としては、次の3つが挙げられる。

  - [Text Encoding Initiative](https://ja.wikipedia.org/wiki/Text_Encoding_Initiative "wikilink") (TEI)
    Text Encoding Initiative (TEI、[:en:Text Encoding Initiative](https://ja.wikipedia.org/wiki/:en:Text_Encoding_Initiative "wikilink")) は、「転送構文」として使うためのSGMLのプロファイルを定義している。
  - [HyperText Markup Language](../Page/HyperText_Markup_Language.md "wikilink") (HTML)
    HyperText Markup Language (HTML) では、 文書の文字符号化集合はリソースの文字符号化方式と分離されている。
  - Extended Reference Concrete Syntax (ERCS)
    Extended Reference Concrete Syntax (ERCS) から、XML 1.0 の命名規則が採用された。ERCSは、十六進数の文字参照を導入しており、全ての[Unicode](../Page/Unicode.md "wikilink")の文字を使うことができるようにするために参照の概念を導入している。

XML仕様の設計に関する議論のなかで開発された革新的な考え方には、次のものが含まれる。

  - XML文書の[文字符号化方式](https://ja.wikipedia.org/wiki/文字符号化方式 "wikilink") ([文字コード](../Page/文字コード.md "wikilink")) の決定の[アルゴリズム](../Page/アルゴリズム.md "wikilink")と、XML宣言における文字符号化方式の指定
  - [処理命令のターゲット](https://ja.wikipedia.org/wiki/#処理命令 "wikilink")
  - xml:space 属性
  - 空要素のタグのための新しい要素終了区切り

### バージョン

2010年1月現在の時点では、XMLには2つのバージョンがある。

  - XML 1.0
    XML 1.0 が最初に策定されたのは1998年2月10日であった。1998年の策定後、数度の改訂 (修正) を経ている。この数度の改訂については新しいバージョン番号は割り当てられていない。現在の時点では、Fifth Edition（第5版）が最新版である。XML 1.0 Fifth Edition は、2008年11月26日にW3Cから公開された。XML 1.0 は、多くの処理系が実装され、現在においても一般的な用途に対しては採用が勧められるとされている。日本ではJIS X 4159:2005としてJIS規格化されている。
  - XML 1.1
    XML 1.1 が最初に策定されたのは2004年2月4日であり、XML 1.0 Third Edition が公開された日と同じ日であった。現在の時点では、Second Edition (第2版) が最新版である。XML 1.1 Second Edition は、2006年8月16日にW3Cから公開された。XML 1.1 にはいくつかの機能が追加されている。XML 1.1 で追加された機能については議論の対象となっている。XML 1.1 で追加された機能は、XML をいくつかの状況で使い易くすることを目指している\[28\]。XML 1.1 で追加された主な機能は次のとおりである。
      - [EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink") プラットフォームで使われている行終端文字を使えるようにする。
      - [Unicode](../Page/Unicode.md "wikilink") 2.0 の文字集合に含まれない文字を使えるようにする。
    XML 1.1 を実装している XML の処理系は、あまり多くない。XML 1.1 は、XML 1.1 特有の機能を必要とする状況においてのみ、採用を勧められるとされている\[29\]。

XML 1.0 と XML 1.1 は、要素名と属性名に使うことができる[文字集合](../Page/文字集合.md "wikilink")において異なっている。XML 1.0 では、 Unicode 2.0 で定義された文字集合のみ要素名および属性名として使うことができる。Unicode 2.0 の文字集合には、世界で使われているほとんどの文字が含まれている。しかし Unicode 2.0 の文字集合には Unicode 2.0 より新しいバージョンで追加された文字は含まれていない。こうした Unicode の新しいバージョンで追加された文字としては、[モンゴル語](https://ja.wikipedia.org/wiki/モンゴル語 "wikilink")、[クメール語](../Page/クメール語.md "wikilink") (カンボジア語)、[アムハラ語](https://ja.wikipedia.org/wiki/アムハラ語 "wikilink")、[ビルマ語](../Page/ビルマ語.md "wikilink")などの文字が、含まれる。

XML 1.1 においては、ほとんどのUnicode文字をXML文書の文字列データや属性値として使うことができる。また Unicode の現在のバージョンで定義されていない文字でさえ、使うことができる。 XML 1.1 の方式では、いくつかの文字については使うことができないが、その他の全ての文字は使うことができる。 一方で XML 1.0 では、仕様で明示的に規定された文字集合のみを、XML文書の文字列データや属性値として使うことができる。 このため XML 1.0 では、Unicode の新しいバージョンで追加される文字を扱うことはできない。

XML文書の文字列データや属性値について、XML 1.1 では XML 1.0 より多くの[制御文字](../Page/制御文字.md "wikilink")を使うことができる。 しかし「堅牢性」の観点から、XML 1.1 で使えるようになった制御文字の多くは、[文字参照としてXML文書内に記述しなければならない](https://ja.wikipedia.org/wiki/#文字参照 "wikilink")。 XML 1.1 で使えるようになった制御文字には、2つの改行コードが含まれる。 この2つの改行コードは、XML 1.1 の処理系では空白記号として扱われる。 制御文字のうちこの空白記号として扱われる制御文字のみが、XML 1.1 で文字参照を使わずに直接にXML文書に記述することができる。

現在、XML 2.0 に関する議論が行われている 。 [XML-SW](http://www.textuality.com/xml/xmlSW.html) (SW は、skunk works [スカンクワークス](../Page/スカンクワークス.md "wikilink")の意味) が、XMLの最初の設計者の一人によって書かれた。 XML-SW には、XML 2.0 はどのようなものかということについての、いくつかの提案を含んでいる。 その内容は次のとおりである。

  - Document Type Definition (DTD、文書型定義) をXMLの構文から排除する。
  - [XML名前空間](https://ja.wikipedia.org/wiki/#XML名前空間 "wikilink")、[XML Base](https://ja.wikipedia.org/wiki/XML_Base "wikilink") および[XML情報集合](https://ja.wikipedia.org/wiki/#XML情報集合 "wikilink") (情報集合) をXML仕様に統合する。

[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) では、XML Binary Characterization (XMLバイナリ表現) のワーキンググループが活動しており、同ワーキンググループでは、XML情報集合をバイナリ形式に符号化するために、[ユースケース](../Page/ユースケース.md "wikilink")と特性を調査する予備研究を行っている。 このワーキンググループは、公的な標準を制定することが認可されているわけではない。 XMLは定義上明確に[テキストに基づいているため](../Page/プレーンテキスト.md "wikilink")、[ITU-T](../Page/ITU-T.md "wikilink")と[ISOは](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、それぞれが定めるバイナリインフォメーションセットに対して、混乱を避けるために [Fast Infoset](http://asn1.elibel.tm.fr/xml/finf.htm) の名前を使っている (参照: ITU-T Rec. X.891 | ISO/IEC 24824-1)。

### 特許の主張

2005年の10月に、Scientigoという小さな企業が、XMLの使用に対して同企業の2つの特許 [U.S. Patent 5,842,213](http://patft.uspto.gov/netacgi/nph-Parser?patentnumber=5842213) と [U.S. Patent 6,393,426](http://patft.uspto.gov/netacgi/nph-Parser?patentnumber=6393426) の対象になるという主張を、公的に表明した。 この2つの特許は、「特定の『階層構造ではない』統合されていない中立的な形式での、\[データの\]モデリングと格納と転送」を対象としている。 特許申請によると、この2つの特許は1997年と1999年に出願された。 Scientigoの最高経営責任者 (CEO) である Doyal Bryant は、この2つの特許を「金銭に換える」という願望を述べたが、同社は「世界を敵にするつもりはない」と言明した。 Bryant は、Scientigoは自社の2つの特許についていくつかの大企業と話し合っていると述べた\[30\]。

XMLを使う人々や企業に在籍していない専門家たちは、Scientigoの主張に対して懐疑的で批判的な立場で反応した。 一定の人々は、Scientigoを[パテント・トロール](../Page/パテント・トロール.md "wikilink")であると述べた。 ティム・ブレイは、この2つの特許がXMLを対象とするという主張は「 ばかげている」と述べた\[31\]。

XMLに関係する多くの先行技術が[SGMLを含めて存在している](../Page/Standard_Generalized_Markup_Language.md "wikilink") 。

## XMLに対する支持と批判

多くの論者がXMLに対してさまざまな批判を行ってきた。 こうした批判は、XMLの長所と潜在的な欠点に対する言及を含んでいる\[32\]。

### XMLの長所

  - XMLは[テキストに基づいた技術である](../Page/プレーンテキスト.md "wikilink")。
  - XMLは[Unicode](../Page/Unicode.md "wikilink")の[文字集合](../Page/文字集合.md "wikilink")を扱える。Unicodeを採用したことにより、どのような自然言語の書き言葉であってもほとんどの情報を通信の対象にできる。
  - XMLは汎用的に[コンピュータ科学](https://ja.wikipedia.org/wiki/コンピュータ科学 "wikilink")の[データ構造](../Page/データ構造.md "wikilink")を表現できる。例えば、レコード（[構造体](../Page/構造体.md "wikilink")）、[リスト](../Page/リスト_\(抽象データ型\).md "wikilink")、[木構造などを表現できる](../Page/木構造_\(データ構造\).md "wikilink")。
  - XMLの自己文書化という形式は、構造とフィールド名とともに値も記述できる。
  - XMLの厳密な構文と[構文解析](../Page/構文解析.md "wikilink")の要件があるため、XMLプロセサ (XML[パーサ](../Page/構文解析器.md "wikilink")) のアルゴリズムは非常に簡潔で効率よく一貫性のあるものとなる。
  - XMLは文書データベースおよび文書処理のための技術として、[スタンドアロン](https://ja.wikipedia.org/wiki/スタンドアロン "wikilink")環境においても[ネットワーク環境においても](../Page/コンピュータネットワーク.md "wikilink")、非常によく活用されている。
  - XMLは国際標準に基づいている。

<!-- end list -->

  - XMLでは、RELAX NG や[スキマトロン](../Page/スキマトロン.md "wikilink")のような[スキーマ言語](../Page/スキーマ言語.md "wikilink")を使うことで妥当性検証を行える。こうした妥当性検証の機構は次のことを容易にする。
      - 有効な単体テスト
      - 有効な防火壁 (ファイアウォール)
      - 有効な受け入れテスト
      - 契約に基づく有効な仕様
      - 有効な[ソフトウェア構築](../Page/ソフトウェア開発.md "wikilink")
  - XMLの[階層構造](../Page/階層構造.md "wikilink")は、(全てではないが) ほとんどの種類の文書の表現に向いている。
  - XMLは[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")として表現される。プレーンテキストは、他のプロプライエタリな文書形式と比べて制限が少ない。
  - XMLは[プラットフォーム独立である](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。このため技術の移り変わりによる影響に比較的強い。
  - XML文書は、スキーマが変更されても、前方互換性と後方互換性を保持することは、比較的容易である。
  - XMLの前身である[SGMLは](../Page/Standard_Generalized_Markup_Language.md "wikilink")、1986年から使われつづけている。そのため大量に蓄積された経験やソフトウェアを活用できる。
  - 整形式XML文書の要素の断片もまた、整形式のXML文書である。

### XMLの短所

  - XML文書の構文は、同じ情報を表すバイナリ表現と比べて、冗長でサイズが大きい<ref name="Elliotte001">

XML文書はバイナリと比べて冗長である</ref>\[33\]。

  - XML文書は冗長であり、記憶装置、転送、処理のコストの面で、効率的な運用に悪い影響を与える可能性がある\[34\]<ref name="Elliotte000">

XML文書はとても冗長であり、高速であることが必要な大規模なデータベースシステムで情報の探索を行うには効率が悪い。</ref>\[35\]。

  - XML文書の構文は、 他の「テキストに基づく」データ転送形式と比べて冗長である<ref name="Bierman000">

XMLの構文は、いくつかの用途においては、人間が読むにはとても冗長である。人間にとっての読みやすさを改善するために dual syntax を提案する</ref>\[36\]。

  - XMLはその前身である[SGMLよりも簡素化されたとはいえ](../Page/Standard_Generalized_Markup_Language.md "wikilink")、その処理は決して軽くはなく、インターネット上のプロトコルなど速度と軽さが要求される分野では、採用が見送られることがしばしばある\[37\]。

<!-- end list -->

  - XMLが表現形式として採用している[階層型モデルは](https://ja.wikipedia.org/wiki/階層型データモデル "wikilink")、[関係モデル](../Page/関係モデル.md "wikilink")や[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")グラフと比べると制限が大きい\[38\]<ref name="Lim000">

固定的な階層構造を採用することに伴ういくつかの制限について議論する。2002年12月にシンガポールで開催された 5th International Conference on Asian Digital Libraries, ICADL 2002 の議事録より。</ref>。

  - オーバーラップする (階層構造ではない) 節 (ノード) の関連を表現するには、余分な努力が必要である\[39\]。
  - XML名前空間を使うことには問題がともなう。名前空間を正しく扱うXMLプロセサを実装することは、難しい作業になる可能性がある\[40\]。
  - XMLは、「自己文書化」として表現されることが多い。しかしこの表現では、重大なあいまいさがあることを考慮していない\[41\]\[42\]。
  - XML文書における内容と属性の区別は、一定の人々にとっては不自然に感じられる。XMLのデータ構造の設計を難しくする要因となっている。\[43\]

## 標準化

先述した[ISOの標準群のほかに](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、XML関連では次の文書が発行されている。

  - ISO/IEC 8825-4:2002 *Information technology -- [ASN.1](../Page/Abstract_Syntax_Notation_One.md "wikilink") encoding rules: XML Encoding Rules (XER)*
  - ISO/IEC 8825-5:2004 *Information technology -- ASN.1 encoding rules: Mapping W3C XML schema definitions into ASN.1*
  - ISO/IEC 9075-14:2006 *Information technology -- [Database languages](../Page/データベース言語.md "wikilink") -- [SQL](../Page/SQL.md "wikilink") -- Part 14: XML-Related Specifications (SQL/XML)*

<!-- end list -->

  - ISO 10303-28:2007 *Industrial automation systems and integration -- Product data representation and exchange -- Part 28: Implementation methods: XML representations of EXPRESS schemas and data, using XML schemas*
  - ISO/IEC 13250-3:2007 *Information technology -- [Topic Maps](https://ja.wikipedia.org/wiki/トピックマップ "wikilink") -- Part 3: XML syntax*
  - ISO/IEC 13522-5:1997 *Information technology -- Coding of multimedia and hypermedia information -- Part 5: Support for base-level interactive applications*
  - ISO/IEC 13522-8:2001 *Information technology -- Coding of multimedia and hypermedia information -- Part 8: XML notation for ISO/IEC 13522-5*
  - ISO/IEC 18056:2007 *Information technology -- Telecommunications and information exchange between systems -- XML Protocol for Computer Supported Telecommunications Applications (CSTA) Phase III*
  - ISO/IEC 19503:2005 *Information technology -- [XML Metadata Interchange (XMI)](../Page/XML_Metadata_Interchange.md "wikilink")*
  - ISO/IEC 19776-1:2005 ''Information technology -- Computer graphics, image processing and environmental data representation -- Extensible 3D (X3D) encodings -- Part 1: Extensible Markup Language (XML) encoding

<!-- end list -->

  - ISO/IEC 22537:2006 *Information technology -- [ECMAScript for XML (E4X)](https://ja.wikipedia.org/wiki/ECMAScript_for_XML "wikilink") specification*
  - ISO 22643:2003 *Space data and information transfer systems -- Data entity dictionary specification language (DEDSL) -- XML/DTD Syntax*
  - ISO/IEC 23001-1:2006 *Information technology -- [MPEG](../Page/Moving_Picture_Experts_Group.md "wikilink") systems technologies -- Part 1: Binary MPEG format for XML*
  - ISO 24531:2007 *Intelligent transport systems -- System architecture, taxonomy and terminology -- Using XML in ITS standards, data registries and data dictionaries*

## 脚注

### 注釈

### 出典

## 参考文献

  -
  -
## 関連項目

### XML関係の仕様

  - [スキーマ言語](../Page/スキーマ言語.md "wikilink")
      - [Document Type Definition](../Page/Document_Type_Definition.md "wikilink")(DTD、文書型定義)
      - [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")
      - [Regular Language description for XML](https://ja.wikipedia.org/wiki/Regular_Language_description_for_XML "wikilink") (RELAX)
      - [TREX](https://ja.wikipedia.org/wiki/TREX "wikilink")
      - [文書スキーマ定義言語](../Page/文書スキーマ定義言語.md "wikilink") (DSDL: Document Schema Definition Languages)
          - [RELAX NG](../Page/RELAX_NG.md "wikilink")
          - [スキマトロン](../Page/スキマトロン.md "wikilink")
  - [スタイルシート](../Page/スタイルシート.md "wikilink")
      - [Extensible Stylesheet Language](../Page/Extensible_Stylesheet_Language.md "wikilink") (XSL)
          - [XSL Formatting Objects](../Page/XSL_Formatting_Objects.md "wikilink") (XSL-FO)
          - [XSL Transformations](../Page/XSL_Transformations.md "wikilink") (XSLT)
      - [Cascading Style Sheets](../Page/Cascading_Style_Sheets.md "wikilink") (CSS)
      - [Document Style Semantics and Specification Language](../Page/Document_Style_Semantics_and_Specification_Language.md "wikilink") (DSSSL)
  - [XML Path Language](../Page/XML_Path_Language.md "wikilink") (XPath)
  - [XML Linking Language](../Page/XLink.md "wikilink") (XLink)
  - [XQuery](../Page/XQuery.md "wikilink")

### 関連する団体

  - [World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) - [標準化団体の一つ](../Page/標準化団体_\(コンピュータと通信\).md "wikilink")。
  - [OASIS](../Page/OASIS_\(組織\).md "wikilink") - 標準化団体の一つ。
  - [Apache XML](../Page/Apache_XML.md "wikilink") - [Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")のプロジェクト。
  - [Apache XML Graphics](../Page/Apache_XML_Graphics.md "wikilink") - Apacheソフトウェア財団のもう一つのプロジェクト。

### XMLと関連する技術

  - [Abstract Syntax Notation One](../Page/Abstract_Syntax_Notation_One.md "wikilink") (ASN.1) - 電気通信やコンピュータネットワークでのデータ構造の表現・エンコード・転送・デコードを記述する記法
  - [JavaScript Object Notation](../Page/JavaScript_Object_Notation.md "wikilink") (JSON) - JavaScriptにおけるオブジェクトの表記法をベースとした軽量なデータ記述言語
  - [YAML](../Page/YAML.md "wikilink") - 構造化データやオブジェクトを文字列に直列化（シリアライズ）するためのデータ形式
  - [Broadcast Markup Language](../Page/Broadcast_Markup_Language.md "wikilink") - XMLベースのデータ放送向け記述言語

## 外部リンク

  - [W3C XML 公式ホームページ](https://www.w3.org/XML/)
  - [W3C XML 1.0 仕様](https://www.w3.org/TR/REC-xml)
  - [W3C XML 1.1 仕様](https://www.w3.org/TR/xml11/)
  - <https://validator.w3.org/> XML構文チェックサイト

[Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:データシリアライゼーションフォーマット](https://ja.wikipedia.org/wiki/Category:データシリアライゼーションフォーマット "wikilink") [Category:データモデリング](https://ja.wikipedia.org/wiki/Category:データモデリング "wikilink") [Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:セマンティック・ウェブ](https://ja.wikipedia.org/wiki/Category:セマンティック・ウェブ "wikilink") [Category:JIS](https://ja.wikipedia.org/wiki/Category:JIS "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:プレゼンテーション層プロトコル](https://ja.wikipedia.org/wiki/Category:プレゼンテーション層プロトコル "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  ["XML stands for Extensible Markup Language. The X is for the first syllable of Extensible. eXtensible is a spelling error."](http://lists.xml.org/archives/xml-dev/200802/msg00313.html)
2.
3.  [JavaScript Object Notation](../Page/JavaScript_Object_Notation.md "wikilink") (JSON) と[YAML](../Page/YAML.md "wikilink")は、XMLと比べて、他の[テキストを基にした直列化言語との中でも](../Page/プレーンテキスト.md "wikilink")、一般に、軽量であり、冗長性の少ないという、特徴をもつと言及されることが多い。 この項目の[\#XMLに対する支持と批判](https://ja.wikipedia.org/wiki/#XMLに対する支持と批判 "wikilink")の節を参照。
4.  [Extensible HyperText Markup Language](../Page/Extensible_HyperText_Markup_Language.md "wikilink") (XHTML) は、[マークアップ言語](../Page/マークアップ言語.md "wikilink") [HyperText Markup Language](../Page/HyperText_Markup_Language.md "wikilink") (HTML) を簡素化しその一貫性を改良しようという試みである。なお、HTMLは、[Standard Generalized Markup Language](../Page/Standard_Generalized_Markup_Language.md "wikilink") (SGML) に基づいたマークアップ言語である。
5.  XMLプロセサを利用する際には、XML文書で用いている文字コードをサポートしたものを選択することになる。
6.  他の方法でXML文書を処理することも可能である
7.  一つの要素の内容として文字列データのみを含むものは、混合内容ではない。また内容のない「空要素」も混合内容ではない。一つの要素の内容がいくつかの子要素だけから構成されるものも、混合内容ではない。
8.  株式会社日本ユニテック、中山幹敏、奥井康弘、2001年、p.132
9.  株式会社日本ユニテック、中山幹敏、奥井康弘、2001年、p.139
10. 株式会社日本ユニテック、中山幹敏、奥井康弘、2001年、pp.28-29
11. 株式会社日本ユニテック、中山幹敏、奥井康弘、2001年、p.29
12. [xml-dev - Fw: An I-D for text/xml, application/xml, etc](http://lists.xml.org/archives/xml-dev/200407/msg00208.html)
13. [JavaプラットフォームAPI仕様](http://java.sun.com/javase/ja/6/docs/ja/api/)
14.
15. [Push, Pull, Next\!](http://www.xml.com/pub/a/2005/07/06/tr.html) - Bob DuCharme, XML.com
16. <http://www.asahi-net.or.jp/~DP8T-ASM/java/tools/Relaxer/index_ja.html>
17. <http://java.sun.com/xml/jaxb/>
18.
19. [**JIS X 4160**](https://webdesk.jsa.or.jp/books/W11M0090/index/?bunsyo_id=JIS%20X%204160:2007):2007「XMLパス言語」附属書 B
20. [XML Schema 1.1 Part 1: Structures](http://www.w3.org/TR/xmlschema11-1/)
21. [*RELAX NG and W3C XML Schema*](http://www.imc.org/ietf-xml-use/mail-archive/msg00217.html), [James Clark](../Page/ジェームズ・クラーク_\(ソフトウェア技術者\).md "wikilink"), 4 Jun 2002
22.
23.
24. このワーキンググループはもともとは "Editorial Review Board" と呼ばれていた。このワーキンググループの最初のメンバーとXML仕様の first edition が完成するまでに加わっていた7人のメンバーは、XML 1.0 first edition のW3C勧告の最後に一覧して掲載されている。参照: <http://www.w3.org/TR/1998/REC-xml-19980210#sec-xml-wg>
25. [Reports From the W3C SGML ERB to the SGML WG And from the W3C XML ERB to the XML SIG](http://www.w3.org/XML/9712-reports.html)
26. [Extensible Markup Language (XML) - W3C Working Draft 14-Nov-96](http://www.w3.org/TR/WD-xml-961114.html)
27.
28.
29.
30. [Small company makes big claims on XML patents - CNET News.com](http://archive.is/20120712154124/http://news.com.com/Small+company+makes+big+claims+on+XML+patents/2100-1014_3-5905949.html)
31. [XML co-inventor Bray responds to patent assault | Between the Lines | ZDNet.com](http://blogs.zdnet.com/BTL/?p=2052)
32. 例えば、 [XML-QL Proposal discussing XML benefits](http://www.w3.org/TR/NOTE-xml-ql/)、 [When to use XML](http://www.25hoursaday.com/weblog/PermaLink.aspx?guid=dada27bf-2af0-400d-94c9-5575546f5664)、 ["XML Sucks" on c2.com](http://c2.com/cgi/wiki?XmlSucks)、[Daring to Do Less with XML](http://www.xml.com/pub/a/2001/05/02/champion.html)
33. [*Efficient XML Interchange Evaluation*](http://www.w3.org/TR/exi-evaluation/), W3C Working Draft, 7 April 2009。W3C は、XML を非テキスト形式（バイナリ）で効率的に表現する方法を別途定義している。
34.
35. ただし、Binary XML の試みは、XML文書のバイナリ表現を使うことでこうした問題を軽減するべく努力している。例えば、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")による Fast Infoset 標準の[リファレンス実装](../Page/リファレンス実装.md "wikilink")では、構文解析 (パース) の速度は [Apache Xerces](../Page/Apache_Xerces.md "wikilink") Java と比べて10倍速く、Javaによる最も高速なXMLプロセサの一つである[Piccolo driver](http://piccolo.sourceforge.net/) と比べて4倍速い[1](https://fi.dev.java.net/reports/parsing/report.html)。
36. 世間で言われているところによれば、XMLより「冗長性の小さい」多くのテキストフォーマットが、XMLに刺激を受けかつ先行的な業績としてXMLを位置づけ言及している。 例えば次のページを参照: <http://yaml.org/spec/current.html>、 <http://innig.net/software/sweetxml/index.html>、 <http://www.json.org/xml.html>
37. XMLの汎用性とそれに伴う重さはしばしば揶揄の対象とされることもある。[IP](../Page/Internet_Protocol.md "wikilink")、[TCP](../Page/Transmission_Control_Protocol.md "wikilink")、[UDPをXMLで定義するというジョーク](../Page/User_Datagram_Protocol.md "wikilink")[RFC](../Page/Request_for_Comments.md "wikilink") ( RFC 3252 ) が存在する。
38. 階層型モデルは[木構造の固定的な単一の視点による見方しか提供しない](../Page/木構造_\(データ構造\).md "wikilink")。例えば、役者が映画の下位に位置づけられるか、映画が役者の下位に位置づけられるかのいずれかであり、双方の視点を両立することはできない。
39. オーバーラップする要素を表現する代替システムを提案する。
40. 例えば次のページを参照: <http://www-128.ibm.com/developerworks/library/x-abolns.html>
41.
42. 例えば [多義語](../Page/多義語.md "wikilink")を参照
43. ("8. Complexity: Attributes and Content" を参照)