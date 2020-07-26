> この記事は[Darwin Information Typing Architecture](https://ja.wikipedia.org/wiki/Darwin_Information_Typing_Architecture)から翻訳されています。


**Darwin Information Typing Architecture** (**DITA**)は、技術情報を制作・発行・配布するための[XMLに基づいたアーキテクチャ](../Page/Extensible_Markup_Language.md "wikilink")。DITAは、[OASIS](../Page/OASIS_\(組織\).md "wikilink")（構造化情報標準促進協会）の支援の下に[IBM](../Page/IBM.md "wikilink")が開発し、コミュニティに寄贈されたものである。2015年にOASIS標準として、1.3版が公開されている。

本アーキテクチャを特徴づけるのは、継承の概念を用いた「特殊化」である。DITAにより提供される各基本要素を特殊化することで、利用組織の目的に合わせた情報アーキテクチャを構築することが可能となる。特殊化においては、継承される親要素の情報を含むことにより、組織外において利用される場合でも、特殊化された要素を、基本要素に代替解釈して処理することが可能となる。本アーキテクチャに、[進化論](../Page/進化論.md "wikilink")の提唱者である[ダーウィンの名が冠せられているのは](../Page/チャールズ・ダーウィン.md "wikilink")、このような特徴による。

DITAでは、「トピック」と「マップ」が基本要素として定義されている。トピックは、自己完結したコンテンツ素材を示す単位である。一方、マップは、ある制作目的のために、必要なトピックへの参照を集めた文書を定義する。この一連のトピックとマップを、[XSLTなどの関連技術で処理することにより](../Page/XSL_Transformations.md "wikilink")、最終形式の著作物を生成する。

## DITAの特徴

  - 組織化の原則に基づいたトピック
  - コンテンツの参照を使用することによるトピック全体の再利用、またはトピックの部分的な再利用
  - 基本的なDITAの要素を特殊化することで、新しい要素の追加へ対応。特殊化を通じて、DITAは特定の産業または会社に要求される新しいトピックの型や要素の型として適用させることができる。
  - プロパティに基づいた処理
      - トピックを見つけやすくする拡張メタデータ
      - 読者やプラットホーム、製品、そのほかのプロパティに基づく条件分岐テキスト
  - [HTMLや](../Page/HyperText_Markup_Language.md "wikilink")[XHTMLのような一般的な言語に似た要素の名前と構造の使用](../Page/Extensible_HyperText_Markup_Language.md "wikilink")。

## 基本構成

DITAを構成する基本要素として、「トピック」と「マップ」がある。

### トピック

トピックは、異なる配布物で再利用できるようにコンテンツを分割した、小さくて自己完結した単位である。一つのトピックの子要素として別なトピックを含むことや、他のトピックを参照することも可能である。ただし、そのようなトピックの再利用性は低下する。DITAでは、利用組織ごとに特有の情報アーキテクチャを定義することを可能にするための「特殊化」と呼ばれる仕組みを提供する。これは、継承の概念に基づくものであり、本アーキテクチャの名前に\`Darwin'の語が冠せられている由来である。

トピック型は、タイトル要素や、メタデータ記述用の序文要素、本文要素を含む。本文要素は、[HTMLと同じように段落や表](../Page/HyperText_Markup_Language.md "wikilink")、リストの要素を含む。

DITAでは、標準で「概念(Concept)」「タスク(Task)」「参照情報(Reference)」「用語集(Glossary)」という、4つの特殊化されたトピック型を提供している。新たな情報アーキテクチャを構築する場合、汎用のトピック型の他に、これらの特殊化された型を継承し、独自の型を定義することができる。

  - 「概念」型はより客観的に、定義や規則、ガイドラインを表現するために用いる。
  - 「タスク」型は、どのように作業を完成させるかを説明する手順を表現するために用いる。タスクは、手順を示す一連のステップで構成される。これは順序性を持つものであり、例えば、操作手順のようなコンテンツの記述に利用する。
  - 「参照情報」型は、コマンドの構文やプログラムの命令などの説明、そのほか参照素材を表現するために用いる。例えば、APIリファレンスのようなコンテンツの記述に利用する。
  - 「用語集」型は、用語とその用語が表す意味の組を表現するために用いる。

### マップ

マップは、トピックへの参照を集めた文書を定義する。マップによって、トピックは順序化され、階層化された一つの成果物として制作、発行される。つまり、断片的なコンテンツ情報であるトピックを統合し、一つの著作物に仕立て上げることがマップの役割である。マップもまた、特殊化を行うことで、独自の情報アーキテクチャの一部として定義することが可能である。

DITAでは、特殊化されたマップとして、「書籍マップ(BookMap)」を提供している。これは、表紙や前付、後付など、書籍を構成する各要素に対応したものである。

## 特殊化と一般化

DITAにおける特殊化は、XMLやXML Schemaの仕様に準拠したものである。典型的な特殊化は、各タグのclass属性により行われる。たとえば以下に示す例では、appstepは、トピック型のliを祖先とし、タスク型のstepを親として定義されていることを示す。この定義は、例のように個別のタグに指定する方法の他に、DTDなどで定義することもできる。

<appstep class="- topic/li task/step bctask/appstep ">`A specialized step`</appstep>

なお、定義組織外において、このように定義されたappstepタグをどう処理すればよいか不明な状況がある。このような場合、DITAプロセッサは、継承を逆にたどり、stepまたはliタグとして解釈し、処理を行う。これを一般化という。

## 規格に基づいた出力物生成

DITAは終端間（エンド・ツゥー・エンド）のアーキテクチャとして発想されている。 [DITA の仕様](http://docs.oasis-open.org/dita/v1.1/OS/archspec/archspec.html)では、どんな要素や属性、規則がDITA言語の一部であるかを示すことに加えて、DITAのコンテンツを印刷物、HTML、[オンラインヘルプ](../Page/オンラインヘルプ.md "wikilink")、そのほかの形式で出力物を生成するための規則を含む。例えば、要素Aのconref属性が要素Bへのパスを含んでいるとすると、要素Bのコンテンツが要素Aの位置に表示されることをDITA仕様は示す。DITAに従った出力物生成ソリューションであるDITAプロセッサは、conref属性を指定された様式に従って扱う必要がある。規則には、条件分岐テキストや目次用の印、トピック間のリンクなどといった諸機能を処理するためのものもある。

DITAがXML規格として公開されたとき、[IBM](../Page/IBM.md "wikilink")は初のDITAに従ったプロセッサ、**DITA Open Toolkit**を公開した。このツールはDITAのコンテンツを、PDFやHTML、ヘルプのような出力形式に変換する。このツールは、任意の特殊化や出力形式を扱うための拡張ができる。また、以下に挙げるDITAの標準化された特殊化およびいくつかの出力形式を特別な設定なしに扱うことができる。

  - [PDF](../Page/Portable_Document_Format.md "wikilink")（[XSL-FO経由](../Page/XSL_Formatting_Objects.md "wikilink")）
  - [XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")
  - [HTML Help](../Page/Microsoft_Compiled_HTML_Help.md "wikilink")
  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") Help
  - [Java Help](https://ja.wikipedia.org/wiki/Java_Help "wikilink")
  - [Oracle Help](https://ja.wikipedia.org/wiki/Oracle_Help "wikilink")
  - [Rich Text Format](../Page/Rich_Text_Format.md "wikilink")

このツールキットは、DITAコンテンツで出力を生成するための基礎としての役割を果たしている。多くのDITAユーザが使用しており、DITA制作ツールやコンテンツ管理ツールのいくつかは現在、出力生成作業フローにこのツールキットの一部を統合している。

DITA Open Toolkitは、いくつかの会社が関与する、活動中のオープンソース・プロジェクトである。

## DITAの普及促進

DITAによるドキュメント制作は従来の[DTP](../Page/DTP.md "wikilink")などとは全く異なる方式であり、DITAの導入はドキュメント制作過程の革新を伴う。またコンピュータ支援によりドキュメントの制作を行なうためシステム初期投資額は決して小さくない。このため企業や団体にDITAを導入するのは大きな決断になる。そうした決断を容易にするために、個々の企業や団体の壁を超える情報・経験の集積と共有、導入支援、技術者の育成などの環境整備が望まれる。そこで日本の関係者の英知を結集してDITAの普及促進を図るために2009年2月に[DITAコンソーシアムジャパン](https://ja.wikipedia.org/wiki/DITAコンソーシアムジャパン "wikilink")が設立された。

## 関連項目

  - [DocBook](../Page/DocBook.md "wikilink")
  - [DITA Open Toolkit](https://ja.wikipedia.org/wiki/DITA_Open_Toolkit "wikilink")
  - [:en:S1000D](https://ja.wikipedia.org/wiki/:en:S1000D "wikilink")
  - [:en:List of document markup languages](https://ja.wikipedia.org/wiki/:en:List_of_document_markup_languages "wikilink")
  - [:en:Comparison of document markup languages](https://ja.wikipedia.org/wiki/:en:Comparison_of_document_markup_languages "wikilink")

## 参照

  - [DITA XML.org community site](http://dita.xml.org)
  - [DITA Version 1.1 Architectural Specification](http://docs.oasis-open.org/dita/v1.1/OS/archspec/archspec.html)
  - [DITA Version 1.1 Language Specification](http://docs.oasis-open.org/dita/v1.1/OS/langspec/ditaref-type.html)
  - [DITA Version 1.2 Specification](http://docs.oasis-open.org/dita/v1.2/spec/DITA1.2-spec.html)
  - [DITA Version 1.3 Specification (Part 3: All-Inclusive Edition)](http://docs.oasis-open.org/dita/dita/v1.3/os/part3-all-inclusive/dita-v1.3-os-part3-all-inclusive.html)
  - [OASIS DITA Technical Committee](http://www.oasis-open.org/committees/dita)

## 書籍

  -
  - 「DITA概説書」Comtech Services (著), DITA コンソーシアムジャパン (翻訳) 、2009年12月株式会社エスアイビー・アクセス発行、ISBN 978-4-434-13939-0

## 外部リンク

  - [DITAコンソーシアムジャパン](http://dita-jp.org/)
  - [DITA仕様書 日本語版](http://www.antenna.co.jp/XML/archspec-ja.html)
  - [DITA XML.org Focus Area](http://dita.xml.org)
  - [DITA World](http://www.ditaworld.com) ― Comprehensive list of DITA resources: articles, vendors, user groups and more
  - [IBM's Introduction to DITA](http://www-106.ibm.com/developerworks/xml/library/x-dita1/)
  - [DITA Open Toolkit Project Home](http://www.dita-ot.org/)
  - [Roadmap for DITA Development](http://wiki.oasis-open.org/dita/Roadmap_for_DITA_development), OASIS DITA Technical Committee
  - [DITA Users](http://www.ditausers.org) - Membership organization helping authors get started with topic-based structured writing
  - [DITA Infocenter](http://www.ditainfocenter.com) - Eclipse Help-based interface to DITA specifications and Open Toolkit

[Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")