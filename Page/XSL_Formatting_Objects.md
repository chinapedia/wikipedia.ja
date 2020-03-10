> この記事は[XSL Formatting Objects](https://ja.wikipedia.org/wiki/XSL_Formatting_Objects)から翻訳されています。


**XSL Formatting Objects** (**XSL-FO** ) は、[XSL](../Page/Extensible_Stylesheet_Language.md "wikilink") (XML Stylesheet Language) の一部で、[組版](../Page/組版.md "wikilink")の制御・指示のための仕様である。狭義にはXSL仕様で定義されている組版対象オブジェクトのことである。XSLは、XSL-FOの他、[XSLTと](../Page/XSL_Transformations.md "wikilink")[XPathから構成される](../Page/XML_Path_Language.md "wikilink")。XSLはXML文書の変換と組版を行うために開発された。XSLの構成要素の一つであるXSL-FOでは、視覚的媒体だけでなく、聴覚的媒体に関する制御も規定している。XSL-FOを含むXSL関連仕様は[標準化団体](https://ja.wikipedia.org/wiki/標準化団体_\(コンピュータと通信\) "wikilink") [W3C](../Page/World_Wide_Web_Consortium.md "wikilink") (World Wide Web Consortium) で開発され勧告として公表されている。

  - 1999年11月16日に XSLT 1.0 と XPath 1.0 が勧告となり公表された。
  - 2001年10月15日に XSL (XSL-FO) 1.0 の勧告が公表された。
  - 2006年12月5日に XSL (XSL-FO) 1.1 の勧告が公表された。
  - 2007年1月23日に XSLT 2.0 と XPath 2.0 の勧告が公表された。
  - 2014年4月8日に XPath 3.0 の勧告が公表された。
  - 2017年3月21日に XPath 3.1 の勧告が公表された。
  - 2017年6月8日に XSLT 3.0 の勧告が公表された。

## 概要

[thumbnail文書を](https://ja.wikipedia.org/wiki/画像:XSL.png "wikilink")[XSLT](../Page/XSL_Transformations.md "wikilink")/[XPathで変換してXSL](../Page/XML_Path_Language.md "wikilink")-FO文書を生成し、XSL-FO処理系によって人間に理解しやすい形式に変換する\]\]

XSL-FO文書も、（[XSLTにより](../Page/XSL_Transformations.md "wikilink")） XSL-FO形式に変換する前の文書も、ともに[XMLに準拠した](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。このことは、[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")/[HTML](../Page/HyperText_Markup_Language.md "wikilink") と [CSS](../Page/Cascading_Style_Sheets.md "wikilink") を組み合わせて使う場合とは対照的である。XHTML/HTML は XML/[SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink") に準拠しているが、CSS は独自の構文で記述する言語でありXMLに準拠していない。

XSL-FOでは、XHTMLとは異なり、意味に基づいたマークアップは行わず、組版で必要となるマークアップのみを行う。また、XSL-FO文書自身に組版の対象となる文書データが全て格納される。一方で CSS は、別の XML もしくは XHTML 文書の既定の表現を変更する方法を採っている。

視覚的表現のための他の手段には、XHTML、[DocBook](../Page/DocBook.md "wikilink") および TEI などの利用がある。XSL は、XSLT が任意の XML を処理可能であるため、どのような XML 文書に対しても適用できる。また出力手段も XSL-FO に限らず、XSLT によって XHTML などに変換する（XMLベースであればなんでも）、といったことも可能である。

XSL では、まず[XSLT](../Page/XSL_Transformations.md "wikilink")[スタイルシート](../Page/スタイルシート.md "wikilink")を使うことが多い。このXSLTスタイルシートは対象となるXML文書の文書型 （スキーマ） にあわせて記述される。XSLTスタイルシートは、組版を行う人自身が記述する場合もあるが、文書型にあわせて作成された既製のものを使うこともできる。このXSLTスタイルシートを適用することにより、対象となるXML文書は、XSL-FO文書に変換される。

XSL-FOでは、XML文書の一般的な作成者は、普通のXML文書を作成するのであり、直接にXSL-FO形式のXML文書を作成することは、想定していない。XSL-FOでは、XML文書の作成者が作成したXML文書をXSLTを使ってXSL-FO形式のXML文書に変換すると、想定している。XSLTのスタイルシートは、作成したXML文書とは別途作成する場合と、XML文書自身に埋め込む場合がある。XSL-FO文書の生成は、XSLTによる変換によって行うことができるが、適切なXSL-FO形式に生成できるのであれば、XSLTを使わずに任意の手段で生成して構わない。

XSLTは、当初はXSL-FOへの変換という用途のみが想定されていたが、XML文書の汎用的な変換に使用可能である。現時点では、多くの[ソフトウェア](../Page/ソフトウェア.md "wikilink")技術者（[プログラマ](../Page/プログラマ.md "wikilink")）はXSLTをXML文書の汎用的な変換言語として認識しており（認識の問題ではなく、汎用であるということは単なる事実であるが）、XML文書をXSL-FO文書に変換するという用途はあまり認識されていない。

XSLTの変換は非常に強力である（チューリング完全である）。XSLTを使うことによって自動的に、文書の目次を生成したり、参考文献とのリンクを設定したり、索引を生成するなど、非常に多様な能力をもつ。

XSL-FO形式の文書が生成されると、XSL-FOの処理系がそのXSL-FO文書を処理して組版する。XSL-FO処理系は、XSL-FO文書を入力として、一般の人々にとって読みやすい[ファイル形式ないしは印刷](../Page/ファイルフォーマット.md "wikilink")/表示可能な媒体を、出力する。出力可能な形式の種類は、XSL-FO処理系の[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")により異なる。現在、XSL-FOで最も一般的な出力形式は[PDFである](../Page/Portable_Document_Format.md "wikilink")。実装によっては、[PostScript](../Page/PostScript.md "wikilink")や[RTFなどの他の形式での出力も可能であるし](https://ja.wikipedia.org/wiki/Rich_Text_Format "wikilink")、ファイルを作成せずに直接にコンピュータ画面に表示したり、直接印刷することもできる。

## XSL-FOの基本的な考え方

XSL-FOは、複数のページで構成される媒体を想定して設計された。一方[HTMLと](../Page/HyperText_Markup_Language.md "wikilink")[CSSは](../Page/Cascading_Style_Sheets.md "wikilink")、ページの概念が無い媒体 （コンピュータ画面など） を想定して設計されている。XSL-FOにおいてページの概念は不可欠な要素である。[XMLを扱う人々にとって](../Page/Extensible_Markup_Language.md "wikilink")、XSL-FOの処理系は、複数のページで情報を表示する際には強力なツールである。

XSL-FOの基本的な考え方は、[コンピュータ](../Page/コンピュータ.md "wikilink")による[組版](../Page/組版.md "wikilink")である。XSL-FO文書には、印刷対象となる文書データと文書データに対する組版の制約情報が含まれている。このXSL-FOをもとに、XSL-FO処理系は組版を行う。XSL-FOはこうした仕組みに基づいているため、あるXSL-FO処理系による出力と、別のXSL-FO処理系による出力が、一致しないことがある。しかしXSL-FOの一般的な目的は、複数のページで構成された組版された媒体を生成することであるため、あまり問題にはならない。XSL-FOの使い方としては、紙などに印刷された文書や[PDFファイルの生成が](../Page/Portable_Document_Format.md "wikilink")、一般的である （PDFファイルもその性質は印刷された文書に近い） 。

XSL-FOは、「内容駆動」(content-driven) と呼ばれる設計による組版に非常に適している。この組版の設計は、書籍や論文、法的文書などで標準的な方法である。この組版設計は、一つの連なったテキストに対応する単一の流し込み （フロー） 領域をもち、ページの余白にさまざまな情報を配置することができる。この設計は、「割り付け駆動」(layout-driven) の設計とは、対義的な設計方法である。割り付け駆動の組版の設計方法は、新聞や雑誌などで使われている。割り付け駆動の設計では、ある文書内容に必要な空間を充分に確保できなかった場合、割り付けを調整して充分に確保しない限り、文書内容は途中までしか印字できない。XSL-FOでは、新聞や雑誌におけるこのような窮屈な制約を制御することは、簡単なことではない。実際にXSL-FOでは、多くの場合、先述のような割り付けの形式を表現する機能がいくつか欠如している。

XSL-FOは基本的にこのように設計されているが、非常に豊富な表現力をもつ。表、リスト、側浮動体 （本文とは分離した領域） 、その他さまざまな機能を備えており使うことができる。XSL-FOのこうした多くの機能はCSSの組版機能と互換性がある。

## XSL-FO文書の構造

XSL-FO文書は[XML文書であるが](../Page/Extensible_Markup_Language.md "wikilink")、明示的な[DTDないしスキーマに従う必要は無く](../Page/Document_Type_Definition.md "wikilink")、[XSL仕様においてXSL](../Page/Extensible_Stylesheet_Language.md "wikilink")-FO文書の構文が定義されている。

XSL-FO文書は、大きく分けて2つの必須の部分から構成される。

  - 最初の部分で、ページのレイアウトを詳しく定義する。レイアウトは1つまたは複数定義することができる。各レイアウトには名前をつける。
  - 次の部分で、一連の文書データを記述する。文書データにはXSL-FOで規定されたマークアップを行う。このマークアップにより、文書データを構成する内容が、先の部分で定義したページレイアウトのうち、どのページレイアウトによって表現されるかを指定する。

最初の部分 （layout-master-set要素） のページレイアウト定義では、ページの特徴を定義する。

  - テキストの表記方向を定義することができる。「右から左に文章を進める」「上から下に文章を進める」「左から右に文章を進める」など、言語に固有の重要な慣習に沿うように指定することができる。
  - ページの縦横の長さやページの余白 （マージン） の長さを指定することができる。
  - ページの連なりについて定義することができる。例えば、奇数ページと偶数ページとで余白などの指定を変えることが可能である。

例えば、印刷するために大きな余白を確保するようページレイアウトの定義をすることができる。 製本するためにさらに大きく余白をとることもできる。

次の部分 （page-sequence要素） では、文書データを分割して複数のフローに再構成する。

  - おのおののフローは、ページレイアウト定義と関連付けられる。
  - フローは、複数のブロックを含むことができる。
  - 各ブロックには、順番に、テキストデータ、インライン要素、およびテキストデータとインライン要素の混合内容を、含めることができる。
  - ページの余白の部分にも、ページ番号や章見出しなどを、印字することができる。

XSL-FOと[CSSは](../Page/Cascading_Style_Sheets.md "wikilink")、良く似ている概念を採用しているが、いくつかの違いもある。 ブロックとインライン要素の概念は、CSSと非常に良く似ている。 間隔 (padding) と余白 (margin) の規則のいくつかは、CSSと異なる。 表記方向 (direction) に関しては、XSL-FO ではページの特性に沿って全て指定することができる。

  - インラインのテキストなどの表記方向 （「左から右へ」「上から下へ」など）
  - ブロック内のテキスト行などの流し込みの方向 （「上から下へ」「右から左へ」など）

このXSL-FOでの表記方向の指定機能により、英語とは異なる方向で文章を記述する慣習のある言語にも対応している。 日本語などの[縦書きにも対応している](https://ja.wikipedia.org/wiki/縦書きと横書き "wikilink")。 ただしXSL-FO処理系の実装としては、少なくとも1つの表記方向に対応することが必須であり、全ての表記方向に対応する必要は無い。 XSL-FOの仕様では、CSS2.1とは異なり、方向に関して表記方向に基づいた用語を採用している。 start （前） や end （後） などを使い、left （左） や right （右） などは、出力媒体に直接関わる場合を除いて、使われない。

XSL-FOの基本的な文書内容のマークアップは、CSSおよびそのカスケーディング規則を基にしている。 そのためXSL-FO文書で記述した要素の多くの属性は、明示的に上書きしない限り、子要素に継承される。

## XSL-FOの機能

XSL-FOには非常に多くの機能がある。 先に述べたことに加え、XSL-FOでは次のような機能を仕様で規定している。

### 段組

複数の段数で[段組](https://ja.wikipedia.org/wiki/段組 "wikilink")のページを記述することができる。 段組のページを記述する場合、 既定ではブロックはある段から次の段へと流し込まれる。 あるブロックを全ての段をまたがって配置することができる。 その場合はページ中に本文の区切りを入れる。 この区切りより前の本文は、この区切りより前方の各段に順に流し込まれる。 区切りより後の本文についても、区切りより後方の各段に順に流し込まれる。 ただしこの場合は区切りをまたがって、区切りの前の部分から区切りの後の部分にかけて、文章を流し込むことはできない。

段組で記述されたページでも、XSL-FOの全ての機能は有効である。

### リスト

XSL-FOのリストは、他のリストと同様にリスト要素が複数並んだものとして構成される。 リスト要素は、要素のラベルと要素の本体から構成される。 リスト要素のラベルには、明示的な順序つきリストであれば数字かアルファベットが含まれ、明示的な順序なしのリストであれば中黒が含まれ、定義リストであれば簡単な文字列 （定義の対象となる用語） が含まれることになるだろう。 リスト要素の本体には、要素の実質的な内容が記述される。 リストのラベルと本体をどのように配置するかは、XSL-FO文書のページレイアウトの記述に依存する。

  - [日本語](../Page/日本語.md "wikilink")や[英語](../Page/英語.md "wikilink")などで[横書きで書く場合](https://ja.wikipedia.org/wiki/縦書きと横書き "wikilink")、リスト要素のラベルを左側に、リスト要素の本体を右側に配置して、組版する。
  - [アラビア語](../Page/アラビア語.md "wikilink")などで書く場合は、逆にリストのラベルを右側に、リスト要素の本体を左側に配置して、組版する。

あるリスト要素で、そのラベルもしくは本体が「ブロックコンテナ」を含む可能性がある。 ブロックコンテナとは、複数のブロックを含む要素をいう。

### ページ付け制御

XSL-FOでは、ブロックあるいはフロー自体に対して、段落の途中で改ページを行うことになった場合、前のページに最低限残すべき行数と、後のページに最低限印字すべき行数を指定することができる。 この指定は、そのブロックが子ブロックを含む場合は継承される。 また、ブロック全体を分割せずに1ページ内に収めるよう、指定することもできる。 例えば、画像のブロックとその画像の説明文が、別々のページに分割されることは望ましくない。 XSL-FO処理系は、例えページ中に大きな空白部分を作ることになっても、これらの指定に従うように努める。

### 脚注

XSL-FOでは、ページの後辺に[脚注](https://ja.wikipedia.org/wiki/脚注 "wikilink")をつけることができる。 脚注の文章は、XSL-FO文書の主となるフローの脚注への参照が置かれる箇所に記述する。 組版した文書においては、脚注への参照はインラインに記載される （ただし必須ではない） 。 脚注の本体は1つ以上のブロックから構成され、XSL-FO処理系によりページの後辺に配置される。

### 表

XSL-FOの表は、[HTML](../Page/HyperText_Markup_Language.md "wikilink")/[CSSの表](../Page/Cascading_Style_Sheets.md "wikilink") （テーブル） と非常によく似ている。 表の各データを、各々の枠内に配置することができる。 また、表の各々の列に対して背景色などのスタイル情報を指定することができる。 表の最初の行を、見出し行として指定することができ、見出し行に対しては他の行とは異なる固有のスタイル情報を指定することができる。

XSL-FO処理系は、各列の幅の長さを厳密に計算して組版することができる。 あるいは、表内にうまく収まるように枠内のテキストを調整して組版することもできる。

### その他

  - ページ番号の引用。特定のタグを含むページをXSL-FO文書のテキストから引用することができ、XSL-FO処理系は引用をしている箇所にそのページ番号を設定する。
  - ブロックの枠線へのさまざまなスタイルの適用。
  - 背景色、画像の配置
  - その他のインライン要素

## XSL-FO文書の例

XSL-FO文書の例を示す。 この例では、A4サイズのページに "Hello world\!" を印字する。

``` xml
<?xml version="1.0"?>
<fo:root xmlns:fo="http://www.w3.org/1999/XSL/Format">
 <fo:layout-master-set>
  <fo:simple-page-master master-name="A4" page-width="210mm" page-height="297mm">
   <fo:region-body region-name="xsl-region-body" margin="2cm"/>
  </fo:simple-page-master>
 </fo:layout-master-set>
 <fo:page-sequence master-reference="A4">
  <fo:flow flow-name="xsl-region-body">
   <fo:block>Hello world!</fo:block>
  </fo:flow>
 </fo:page-sequence>
</fo:root>
```

## XSL-FOの特長

XSL-FO文書は[XMLに準拠した文書であるため](../Page/Extensible_Markup_Language.md "wikilink")、適切な[XSLT](../Page/XSL_Transformations.md "wikilink")[スタイルシート](../Page/スタイルシート.md "wikilink")を用意してXSLT処理系を適用すれば、どのような文書型のXML文書でも、XSL-FO文書を生成することができる。 そのためXSLTスタイルシートとXSLT処理系を使えば、XMLに準拠したTEI文書や[DocBook](../Page/DocBook.md "wikilink")文書をもとにして、[ウェブで閲覧できる](../Page/World_Wide_Web.md "wikilink")[XHTML文書を生成することは容易に実現できる](../Page/Extensible_HyperText_Markup_Language.md "wikilink") （この場合はXSL-FO文書を生成する必要は無い） し、さらにXSL-FO処理系を使えば印刷向けの[PDF文書を生成することができる](../Page/Portable_Document_Format.md "wikilink")。 実際に、既存のTEI文書やDocBook文書の多くが、XSLT/XSL-FOにより、XHTMLやPDFなど人間にとって理解しやすい形式に変換されてきた。

またXSL-FO文書はXMLに準拠しているが、明示的なスキーマや[DTDが定義されていないため](../Page/Document_Type_Definition.md "wikilink")、XSL-FO文書にはXML形式の何らかのデータを格納することができる。 このようなXML形式のデータとして最もよく使われるのは、おそらく[画像](../Page/画像.md "wikilink")形式である[SVGであろう](../Page/Scalable_Vector_Graphics.md "wikilink")。 多くのXSL-FO処理系が、SVGデータが埋め込まれたXSL-FO文書を解釈し、SVGの画像データを埋め込んだ出力を生成することができる。

XSL-FOの非常に多くの機能は、[CSSに基づいている](../Page/Cascading_Style_Sheets.md "wikilink")。  あるXSL-FO文書の特定の部分を見てその部分がどのように[組版](../Page/組版.md "wikilink")されるかを認識することは、多くの場合は簡単である。 このXSL-FOの特長は、[TeX](../Page/TeX.md "wikilink")のような組版[ソフトウェア](../Page/ソフトウェア.md "wikilink")パッケージの場合と比べると際立っている。

## XSL-FOの課題

XSL-FOの課題の一つは、2006年12月現在ではXSL-FO処理機能を備えた[ソフトウェア](../Page/ソフトウェア.md "wikilink") （XSL-FOの処理系） が少ないことである。 また、XSL-FO 1.0 の公式仕様では非常に多くの機能が規定されており、そのため仕様に100%準拠した処理系は実際には存在しない。 XSL-FO処理系が少ない理由は、現時点ではXSL-FOに対する需要があまり多くないからであるとの見解がある。 [TeX](../Page/TeX.md "wikilink")とそのマクロパッケージ群 （[LaTeX](../Page/LaTeX.md "wikilink")など） は、[組版](../Page/組版.md "wikilink")向け言語として既に長い間その地位を確立している。 そしてTeXを使う人々は、TeXに替えてXSL-FOを採用する必要性をほとんど感じていない。

もう一つの課題は、XSL-FO文書を読んで内容を理解することは簡単であるが、XSL-FO文書を手作業などで記述することは、難しいことであり非常に冗長な作業となることである。 [XSLTは](../Page/XSL_Transformations.md "wikilink")、XSL-FO文書を簡単に生成することができるように設計された。 そのためXSL-FO自体には、XSL-FOを簡潔な作業で生成するという観点は考慮されていない （XSLTを使えば簡潔な作業で生成できる） 。 この問題は別の問題を提起する。 XSL-FOの初学者は、XSL-FO文書を記述する方法を一通り学ぶだけでなく、場合によってはXSLTによる変換の方法も学ばなければならないということになる。 このことは当然ながら、標準化された[XML文書を変換する既製のXSLTスタイルシートが使える場合は](../Page/Extensible_Markup_Language.md "wikilink")、問題とはならない。

## XSL-FOのバージョン

2006年12月現在、XSLの最新バージョンは[1.1](http://www.w3.org/TR/2006/REC-xsl11-20061205/)である。XSLが2001年10月に勧告になってからいくつかのXSL-FO処理系が登場したが、XSL-FO V1.0の勧告では、ユーザが望む機能が不足していたため、処理系それぞれが独自拡張を行って機能を追加してしまった。このため、W3CのXSL ワーキンググループでは、処理系の実装を調査して共通の機能を標準化することを優先的に行ってきた。その作業成果がXSL-FO V1.1であり、V1.1で標準化されたそれらの機能には、巻末索引、改訂バー、PDFにおけるしおり、財務諸表における部分和への対応などに必要となる表中における条件付テキスト指標、ページグループ内での最終ページ番号の検出、単一ページ内での複数方向への記述、がある。

## XSL-FO処理系の実装

現在、XSL-FO処理系の[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")は、あまり多くはないが、利用することができる。 XSL-FO処理系は、XSL-FO文書を実際に視覚的な形式 （[PDFなど](../Page/Portable_Document_Format.md "wikilink")） に組版もしくは聴覚的媒体に出力する。 XSL-FOの仕様では非常に多くの機能を規定しているため、多くの処理系の実装はXSL-FO仕様で規定された機能を全て実装するには至っていない。 主な実装を次に示す。

  - [Apache FOP](../Page/Apache_FOP.md "wikilink") - [Apache XML Graphics](../Page/Apache_XML_Graphics.md "wikilink") プロジェクトによる[オープンソース](../Page/オープンソース.md "wikilink")の実装。PDFを含むさまざまな出力形式に対応している。
  - PassiveTeX パッケージ - [TeX](../Page/TeX.md "wikilink")を使い、XSL-FOで記述された文書をPDF形式に変換する。
  - [XSL Formatter](../Page/XSL_Formatter.md "wikilink") - [アンテナハウス](../Page/アンテナハウス.md "wikilink")社による商用の実装。

XSL-FO処理系の出力形式としては、さまざまな[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")がある。 実際に出力可能なフォーマットは、XSL-FO処理系の実装により異なる。実装によってはファイルを作成せずに、直接にコンピュータ画面に表示したり、直接印刷することもできる。

  - [PDF](../Page/Portable_Document_Format.md "wikilink")
  - [PostScript](../Page/PostScript.md "wikilink")
  - [SVG](../Page/Scalable_Vector_Graphics.md "wikilink")
  - [MIF](https://ja.wikipedia.org/wiki/MIF "wikilink")
  - [PCL](../Page/PCL.md "wikilink")
  - [プレーンテキスト](../Page/プレーンテキスト.md "wikilink")

## 関連項目

  - [OpenDocument](../Page/OpenDocument.md "wikilink")
  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [スタイルシート](../Page/スタイルシート.md "wikilink")
      - [XSL](../Page/Extensible_Stylesheet_Language.md "wikilink")
          - [XSLT](../Page/XSL_Transformations.md "wikilink")
          - [XPath](../Page/XML_Path_Language.md "wikilink")
      - [CSS](../Page/Cascading_Style_Sheets.md "wikilink")
      - [DSSSL](../Page/Document_Style_Semantics_and_Specification_Language.md "wikilink")
  - [TeX](../Page/TeX.md "wikilink")
      - [LaTeX](../Page/LaTeX.md "wikilink")

## 外部リンク

  - [The Extensible Stylesheet Language Family (XSL)](http://www.w3.org/Style/XSL/) - [W3CのXSLのページ](../Page/World_Wide_Web_Consortium.md "wikilink")
  - [XSL-FO 処理系の現状報告](http://www.w3.org/Style/XSL/2006/01/xsl11-implementation) - [W3CのXSLワーキンググループへ報告された実装レポート](../Page/World_Wide_Web_Consortium.md "wikilink")
  - [アンテナハウス](../Page/アンテナハウス.md "wikilink")社のページ （日本語）
      - [XSL Formatter](http://www.antenna.co.jp/AHF/) - アンテナハウス社による商用のXSL-FO処理系
      - [XSL-FO の基礎 第2版 - XML を組版するためのレイアウト仕様](http://www.antenna.co.jp/AHF/ahf_publication/index.html#fo-basis)
          - [XMLからXSL-FOに変換するためのXSLTスタイルシートの作成方法](http://www.antenna.co.jp/AHF/ahf_samples/#XSLT)
  - [Apache FOP](http://xmlgraphics.apache.org/fop/) - [Apache XML](../Page/Apache_XML.md "wikilink") プロジェクトによる[オープンソース](../Page/オープンソース.md "wikilink")のXSL-FO処理系。[PDF](../Page/Portable_Document_Format.md "wikilink")/[SVG](../Page/Scalable_Vector_Graphics.md "wikilink")/[TXTなどへの変換が可能](../Page/プレーンテキスト.md "wikilink")
  - [XSL-FO Visual Designer](http://www.ecrion.com/Products/XFDesigner/Overview.aspx) on Ecrion.com
  - [What is XSL-FO?](http://www.xml.com/pub/a/2002/03/20/xsl-fo.html) - O'REILLY XML.com
  - [XSL-FO: Ready for Prime Time?](http://www.gilbane.com/gilbane_report.pl/94/XSLFO_Ready_for_Prime_Time.html) on the Gilbane Report
  - [A Tool for editing and testing XSL Formatting Objects](http://www.editix.com)
  - [Data2Type](http://www.data2type.de/xml/XSL-FO.html) (german) XSL-FO informations
  - [XSL Formatting Objects Tutorial](http://www.renderx.com/tutorial.html) on RenderX
  - [XSL-FO Tutorial and Samples HTML](http://www.ecrion.com/XF/TechnicalResources/XSL-FOTutorial/toc.xml.html) or [PDF](http://www.ecrion.com/XF/PDF/XSL-FOTutorial.pdf) (PDF, 476 KB) on Ecrion.com
  - [XSL-FO Editor](http://www.oxygenxml.com/fo_editor.html)
  - [Stampa Reports System - XSL-FO Visual Editor](http://www.e-dynamica.com)
  - [XSL-FO Editor](http://www.xmlblueprint.com)

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:スタイルシート言語](https://ja.wikipedia.org/wiki/Category:スタイルシート言語 "wikilink")