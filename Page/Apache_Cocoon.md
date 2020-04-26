> この記事は[Apache Cocoon](https://ja.wikipedia.org/wiki/Apache_Cocoon)から翻訳されています。


**Apache Cocoon**（アパッチ・コクーン）は、[ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/ウェブアプリケーションフレームワーク "wikilink")であり、[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")、[関心の分離](../Page/関心の分離.md "wikilink")、[コンポーネントベースの](../Page/ソフトウェアコンポーネント.md "wikilink")[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")開発といった概念に基づいたものである。単に Cocoon と呼ばれることが多い。Cocoonフレームワークは[XMLと](../Page/Extensible_Markup_Language.md "wikilink")[XSLTによる出版に焦点をおいており](../Page/XSL_Transformations.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で開発されている。 XML技術を基盤としてXML技術を積極的に活用することにより高い柔軟性を持っており、[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[WMLなどさまざまな形式での迅速な文書](../Page/Wireless_Markup_Language.md "wikilink") (コンテンツ) の出版が可能である。コンテンツ管理システムである Apache Lenya と Daisy は、Apache Cocoon を基盤として開発されている。Cocoonはまた、[データウェアハウス](../Page/データウェアハウス.md "wikilink")の[ETL](https://ja.wikipedia.org/wiki/ETL "wikilink") (抽出: Extract、変換: Transform、ロード: Load) のツールとしても使われており、[情報システム](../Page/情報システム.md "wikilink")間のデータ転送のための[ミドルウェア](../Page/ミドルウェア.md "wikilink")としても使われている。

## サイトマップ

Apache Cocoon の中心部分にサイトマップ (sitemap.xmapファイル) が存在する。サイトマップにおいて、[ウェブサイト](../Page/ウェブサイト.md "wikilink")の開発者が、さまざまな Cocoon のコンポーネントを環境設定し、[クライアントサーバの相互作用を定義する](../Page/クライアントサーバモデル.md "wikilink")。このクライアントサーバ相互作用において、CocoonはXML変換言語によるXMLパイプラインとして参照する。

## コンポーネント

Cocoonのコンポーネントは、機能ごとに分類される。

### matchers

matchersの用途は、利用者の[URLや](../Page/Uniform_Resource_Locator.md "wikilink")[cookieなどの](../Page/HTTP_cookie.md "wikilink")[HTTPリクエスト情報が](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[ワイルドカードや](../Page/ワイルドカード_\(情報処理\).md "wikilink")[正規表現](../Page/正規表現.md "wikilink")のパターンに対して、一致するものをみつけることである。利用者のHTTPリクエストのおのおのは、Cocoonを使った[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")に送信され、パターンに対して一致するものをみつける処理が行われる。その後におのおののリクエストに対する処理が行われる。

### generators

generatorsは、高度な処理のための[ストリームを生成する](../Page/ストリーム_\(プログラミング\).md "wikilink")。 このストリームは、配置された[XML文書をもとに生成することができる](../Page/Extensible_Markup_Language.md "wikilink")。generatersとしては、ディレクトリ構造や画像データなどサーバに関する何らかのデータを表現するために、一からXML文書を生成できるものも存在する。

### transformers

transformersは、データのストリームを取得して、何らかの方法でデータストリームの内容の変更を行う。多くの場合に共通して使われる変更方法は、[XSLT](../Page/XSL_Transformations.md "wikilink") (XSL Transformations) の[スタイルシート](../Page/スタイルシート.md "wikilink")である。XSLTスタイルシートは、あるXML文書の構造を別の構造に変換する技術であり、XSLTスタイルシート自身もXMLで記述される。他の形式で記述されたデータを取得して変更を行うtransformersも存在する (例えば[SQL](../Page/SQL.md "wikilink")など) 。

### serializers

一つのserializerは、一つのデータストリームを取得し、データストリームに対して必要な何らかの変更を行い、変更後の内容をクライアント側 (利用者側) に配信する。さまざまな種類の形式でデータを配信するserializersが存在する。Cocoonで配信可能なデータの形式としては、例えば、[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[RTF](../Page/Rich_Text_Format.md "wikilink")、[SVG](../Page/Scalable_Vector_Graphics.md "wikilink")、[WML](../Page/Wireless_Markup_Language.md "wikilink")、[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")がある。

### selectors

selectorsは[switch文](https://ja.wikipedia.org/wiki/switch文 "wikilink")と同じことができる。selectorsを使うことで、HTTPリクエストから特定の要素を選びだして、HTTPリクエストを処理するために使うための正しいパイプライン部を選択することができる。

### views

viewsの用途は主としてテストである。一つのviewは一つのパイプラインの終了場所である。この終了場所までに生成されたXMLデータストリームを出力することができる。このためウェブアプリケーションが正しく動作しているかどうかを、viewsを使って調べることができる。

### readers

readersはデータのパースを行わないでデータを配信する。つまりreadersはXML技術に基づいた処理は行わない。画像データのようなデータに対して使われる。

### actions

actionsは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[クラスであり](../Page/クラス_\(コンピュータ\).md "wikilink")、このクラスが何らかの[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")を実行したり新しいコンテンツの生成を管理したりする。

**XSP page** [1](http://cocoon.apache.org/1.x/xsp.html) とは、Cocoon XML 文書であり、このXML文書はタグに基づいた命令 (ディレクティブ) を含む。XSP page に含まれる命令は、HTTPリクエストを受けたときにどのようにして動的な文書を生成するかを指定する。

Cocoonでの処理において、こうした命令は生成された文書に置き換えられる。その結果として、対象となるXML文書に対して高度な処理を行うことができる ([XSLT](../Page/XSL_Transformations.md "wikilink")[スタイルシート](../Page/スタイルシート.md "wikilink")による変換処理を行うことが多い) 。

XSP page は、Cocoon の文書生成機構によって変換処理が行われる。XSP page を扱う際の Cocoon の文書生成機構は、Javaのクラスである場合が多い。ただし何らかの[スクリプト言語](../Page/スクリプト言語.md "wikilink")があり、そのスクリプト言語の処理機構がJavaで実装されている場合、そのスクリプト言語を文書生成機構として使うこともできる。

XSP page に含まれる命令は、XSP組込みの処理タグである場合と、開発者が定義したライブラリタグである場合とがある。

  - XSP組込みのタグの用途は、手続き的なロジックの埋め込み、式の置き換え、そして動的なXMLのノードの構築である。
  - 開発者が定義したライブラリタグは、おのおのの動的なタグの内にコード化された情報をもとにしてプログラムコードを生成する方法を指示する雛型として役割を果たす。

## パイプライン

パイプラインの用途は、さまざまな Cocoon コンポーネントがさまざまな[HTTPリクエストと相互作用してHTTPレスポンスを生成する方法を定義することである](../Page/Hypertext_Transfer_Protocol.md "wikilink")。

[XProc](http://xproc.org/)モデルと標準化も参照。

## 関連項目

  - Reactor Pattern - Cocoon が基にしている[デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - XML pipeline
  - [XSLT](../Page/XSL_Transformations.md "wikilink") (XSL Transformations) - Cocoon が文書の変換方法を格納するために使う[XMLの](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")

## 外部リンク

  - [The Apache Cocoon プロジェクト](http://cocoon.apache.org/)
  - [Cocoon 2.1 文書](http://cocoon.apache.org/2.1/)
  - [Apacheソフトウェア財団](http://www.apache.org/)
  - [Cocoon サンプルプログラム](http://cocoon.zones.apache.org/demos/release/samples/)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")