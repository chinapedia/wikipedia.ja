> この記事は[XForms](https://ja.wikipedia.org/wiki/XForms)から翻訳されています。


**XForms**（XMLフォーム言語） は、[Webフォームなどの](https://ja.wikipedia.org/wiki/フォーム_\(ウェブ\) "wikilink")[XMLデータのための](../Page/Extensible_Markup_Language.md "wikilink")[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")やデータ処理モデルを定義するXMLフォーマットの仕様である。[HTML](../Page/HyperText_Markup_Language.md "wikilink") / [XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") のフォームの代替となるべく[W3C](https://ja.wikipedia.org/wiki/W3C "wikilink")によって設計されたものだが、Webに限らず汎用的に[データ](../Page/データ.md "wikilink")操作タスクのユーザインタフェースを記述する能力を有する。

策定が中止されたXHTML 2.0 と似ており、また XHTML 2.0 に XForms 自体が組み込まれる予定だった。現状の XHTML とは名前空間や構文が異なる。XForms は企業品質のWebフォームを比較的簡単に作れると言われている。

現在の XForms 1.1は2009年10月20日に[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")となった。最初の XForms 1.0 が[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")となったのは、2003年10月14日である。

XForms 1.0は2007年にJIS X 4178:2007として[JIS規格化もされている](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")。

## HTMLフォームとの違い

HTMLフォームとは異なり、XForms は [Model View Controller](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink") アプローチを採用している。この場合の「モデル」は、フォームデータおよびそのデータに関する制約を記述する1つ以上のXFormsモデルから成る。「ビュー」は、フォームにおけるコントロールは何か、どのようにグループ化されるか、結び付けられるデータは何かを記述する。フォームの見た目の記述には [CSS](../Page/Cascading_Style_Sheets.md "wikilink") を使うことができる。

あまり複雑なことをしない限り XForms 文書は単純なHTMLフォームと大差ないが、XForms には多数の最新機能がある。例えば、新たなデータを要求し、動作中にフォームを更新することができ、[XMLHttpRequest](https://ja.wikipedia.org/wiki/XMLHttpRequest "wikilink")/[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink") に似ているがスクリプトを必要としない。フォーム作者はユーザーデータを [XML Schema](https://ja.wikipedia.org/wiki/XML_Schema "wikilink") のデータ型に照らして妥当性を検証でき、特定のデータを要求したり、入力コントロールを入力不可にしたり、状況によってフォームの一部を変更したり、データ間に何らかの関係を強制したり、任意個数のデータを入力可能にしたり、フォームデータから計算した値を出力したり、XML文書を使ってエントリを予め埋めたり、（サブミット時ではなく）リアルタイムにアクションに反応したり、表示に使っている機器（デスクトップか携帯機器かなど）に応じてコントロールのスタイルを修正したりできる。大抵の場合、[JavaScript](../Page/JavaScript.md "wikilink") などのスクリプト言語を使う必要がない。

従来のフォームと同様、XForms は XML以外のサブミットプロトコル（multipart/form-data、[application/x-www-form-urlencoded](https://ja.wikipedia.org/wiki/パーセントエンコーディング#application/x-www-form-urlencoded "wikilink")）を使うことができるが、XForms の新機能の1つとしてXML形式によるサーバへのデータ送信がある。XML文書をフォームの既定値データとして埋め込んでおくこともできる。XMLを扱うツールは多数存在するため、XMLを使ったサブミッションではその解析や編集が容易であり、従来のように場当たり的に[構文解析](../Page/構文解析.md "wikilink")が必要になるようなことはない。XForms 自身もXMLの方言であるため、XML文書を[XSLTを使ってXForms文書に変換したり](../Page/XSL_Transformations.md "wikilink")、逆にXForms文書からXML文書に変換可能である。[XML変換言語](../Page/XML変換言語.md "wikilink")を使えば、XFormsを[スキーマ言語](https://ja.wikipedia.org/wiki/スキーマ言語 "wikilink")から生成したり、XForms を従来のHTMLフォームに変換したりできる。実際、今日のサーバ側のXformsは基本的にはそのようにして動作している。

## ソフトウェアサポート

本項目執筆時点では、XForms をネイティブでサポートしている一般的[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")は存在しない。しかし、各種ブラウザ用プラグインとクライアント側での拡張が存在する。クライアント側での実装の一覧を以下に示す。

  - [Firefox](../Page/Mozilla_Firefox.md "wikilink") XForms extension [1](https://developer.mozilla.org/en-US/docs/Archive/Web/XForms) - Mozilla Project の一部であり、Firefox および Mozilla で利用可能。一部未実装の仕様がある。
  - [IBM Lotus Forms](http://www-06.ibm.com/jp/software/lotus/products/forms/index.html)
  - [formsPlayer](http://www.formsPlayer.com/) - Internet Explorer 6 以上を拡張し、XForms 以外にも [DOM](../Page/Document_Object_Model.md "wikilink")、[XPath](https://ja.wikipedia.org/wiki/XML_Path_Language "wikilink") などを実装。
  - [FormFaces](http://www.formfaces.com/) - 純粋な [JavaScript](../Page/JavaScript.md "wikilink") プロセッサ。XForms+HTML が直接ブラウザに送られ、JavaScript が XForms を HTML フォームに変換する。XHTML 1.0、ECMAScript-262 第三版、DOM Level 2 に対応したブラウザで使用可能（[Internet Explorer](../Page/Internet_Explorer.md "wikilink"), [Mozilla](../Page/Mozilla.md "wikilink"), [Firefox](../Page/Mozilla_Firefox.md "wikilink"), [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink"), [Konqueror](../Page/Konqueror.md "wikilink"), [Safari](../Page/Safari.md "wikilink"), [NetFront](https://ja.wikipedia.org/wiki/NetFront_Browser "wikilink")）。
  - Convex - IE6 用拡張。Java アプレットを使った実装で、[オープンソース](../Page/オープンソース.md "wikilink")プロジェクト Chiba の一部。

以下は、純粋なクライアント側の実装であり、ブラウザに対する拡張ではない。

  - IBM Lotus Forms にはブラウザ拡張以外にスタンドアロンのクライアントも含まれる。
  - [OpenOffice.org](../Page/OpenOffice.org.md "wikilink") versions 2.0 以降 XForms をサポート [2](http://marketing.openoffice.org/ooocon2004/presentations/friday/vogelheim_XForms.pdf)
  - [X-Smiles](http://www.xsmiles.org) - [オープンソース](../Page/オープンソース.md "wikilink")のJavaによるクライアント実装（XMLブラウザ）。XForms 以外にも [XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、[CSS](../Page/Cascading_Style_Sheets.md "wikilink")、[SVG](../Page/Scalable_Vector_Graphics.md "wikilink") などをサポート。
  - [DENG](http://deng.com.br/) - XForms 対応の軽量XMLブラウザエンジン。CSS-3 と XForms をサポート。
  - [PicoForms](http://www.picoforms.com) - XForms 対応のブラウザエンジン。デモ版は XHTML, CSS, XML Events, XForms をサポートし、[Java ME](../Page/Java_Platform,_Micro_Edition.md "wikilink") 搭載携帯機器で動作。
  - [DataMovil](http://www.datamovil.info) - 携帯機器用

XForms は、サーバ側でHTMLフォームや他のウィジェット（通常 [Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink") を利用）に変換する形で即座に利用可能である。以下のような実装がある。

  - Chiba（[オープンソース](../Page/オープンソース.md "wikilink")）
  - [Orbeon Forms](http://www.orbeon.com/) （[オープンソース](../Page/オープンソース.md "wikilink")）

以下は、XHTML/XForms 文書から HTML と JavaScript のコードを生成するサーバ側で利用するコンパイラ型の実装である。

  - IBM Lotus Forms WebForm Server
  - [AJAXForms](http://ajaxforms.sourceforge.net) - XHTML/XForms を HTML と JavaScript に変換（[オープンソース](../Page/オープンソース.md "wikilink") - 2006年11月以降活動休止状態）
  - [XSLTForms](http://www.agencexml.com/xsltforms/) - XHTML/XForms を XHTML と JavaScript （[Internet Explorer](../Page/Internet_Explorer.md "wikilink"), [Mozilla](../Page/Mozilla.md "wikilink"), [Firefox](../Page/Mozilla_Firefox.md "wikilink"), [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")）。
  - [eXtremeBuilder (Korean only)](http://www.tomatosystem.co.kr/tomato/client.contents.serv?ID=3-1)

## 実装技術の比較

FormFaces、AJAXForms、XSLTForms、Chiba、Orbeon Forms は[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")技術に基づいている。サーバ側およびクライアント側の処理は実装によって様々である。例えば、FormFaces はクライアント側を完全な XForms 処理とし、XForms 標準に基づく純粋な Ajax 処理によってデータモデルを更新する。その他は、サーバ側でJavaによるXFormsのAjaxマークアップへの変換を行ってから、ブラウザにコンテンツを配信する。どちらの技術も複数種のブラウザで動作する。それぞれの実装は、依存関係、[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")、性能、ライセンス、完成度、ネットワークトラフィック、オフライン機能、ブラウザ間の互換性などに違いがある。

FormsPlayer のようなクライアント側プラグイン技術にもいくつかの利点がある。ブラウザに組み込まれるため、既存のサーバアーキテクチャで動作でき、応答性がよく、サーバのフェッチ回数が少なくて済む。例えば、ブラウザがサポートしていないコントロールを表示できるなどのユーザフレンドリな利点もあるが、JavaScript によるウィジェットでも同じことが可能であるため、固有の長所とは言えない。

サーバ側での実装とクライアントでのプラグイン実装のトレードオフは、どこでソフトウェアを保守するかにある。どちらにしても、クライアントに要求されたプラグインをインストールするか、サーバ側でXForms変換エンジンを実装する必要がある。理論的には両方の手法を混合することも可能であり、クライアント側にXForms機能が実装されているかを調べ、実装されていたらサーバ側はXFormsでコンテンツを送信し、そうでない場合はサーバ側で変換するということが考えられる。

FormFaces はサーバ側にもクライアント側にも新たなソフトウェアを加える必要がない。クライアント側には新たなプラグインをインストールする必要はないし、サーバ側はアーキテクチャを変更する必要がない。これは、FormFaces が完全に Ajax で書かれているためである。しかしこの場合、他の手法よりもクライアントに多くの JavaScript コードがダウンロードされ（クライアント側でキャッシュされる）、XML Schema の検証はまだサポートされていない。

どの XForms 実装でも、Web 2.0 API（[Google Maps](http://maps.google.com/)、[Yahoo Traffic Alerts](http://developer.yahoo.com/traffic/index.html)、[Kiko Calendar](http://www.kiko.com/)、[Skype Voice Service](http://www.skype.com/partners/voice/) など）を組み込み可能である。

## 携帯機器用 XForms

### 利点

XForms は特に携帯機器で使われた場合に、以下のような利点がある。

  - HTML 4 のフォームよりも XForms を使ったユーザインタフェースの方がサーバとのやり取りが少なくて済む。
  - 携帯機器の機能は様々である。その結果、各種機器向けに各種ユーザインタフェースを生成する必要があり、モバイル業界ではそれが重要となっている。XForms はフォームを機器の機能とは独立に記述できるよう設計されており、各種機器対応の作業を減らすことができる。
  - XForms は JavaScript を必要とする場面を削減でき、携帯機器では JavaScript の実装にばらつきがあって信頼できないことが多いため、一種の利点になりうる。また、セキュリティ上の懸念から JavaScript を実行不可としたシステムでも利用できる可能性がある。

### 実装

上述のような利点はあるが、携帯機器での XForms 利用はまだ発展途上である。これまでに以下のような実装が登場している。

  - [PicoForms Micro Edition Browser](http://www.picoforms.com) - MIDP 2.0 および CLDC 1.x に対応した携帯電話で動作。Palm や Pocket PC もサポート。
  - [DataMovil](http://www.datamovil.info) - XForms プロセッサを組み込んだ携帯用アプリケーションの開発プラットフォーム。各種携帯機器で動作する。Java ME ベース。
  - [IBM Forms for Mobile Devices](http://www.alphaworks.ibm.com/tech/ifmd)
  - [Oracle Wireless Client](http://www.oracle.com/technology/tech/wireless/mobilebrowser.htm) - 2004年3月にプレビューリリース。ただし名前に反して、携帯機器上で動作するソフトウェアは含まれておらず、Internet Explorer のプラグインになっていた（そのためプレビューと称していたと思われる）。XForms をサポート。
  - [FormFaces Mobile Solution](http://www.formfaces.com) - [NetFront Browser](https://ja.wikipedia.org/wiki/NetFront_Browser "wikilink") で動作する 100% JavaScript 実装。

## 関連項目

  - [W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")
  - [日本工業規格（情報処理）の一覧](https://ja.wikipedia.org/wiki/日本工業規格（情報処理）の一覧 "wikilink")

## 参考文献

  -
  - （テキスト自体は[GFDLで公開されている](../Page/GNU_Free_Documentation_License.md "wikilink")）

## 外部リンク

  - [W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink") (W3C Recommendation)
      - [XForms 1.0](http://www.w3.org/TR/2003/REC-xforms-20031014/)
      - [XForms 1.0 (Second Edition)](http://www.w3.org/TR/2006/REC-xforms-20060314/)
      - [XForms 1.0 (Third Edition)](http://www.w3.org/TR/2007/REC-xforms-20071029/)
      - [XForms 1.1](http://www.w3.org/TR/2009/REC-xforms-20091020/)
      - [XForms 2.0 (Working Draft)](http://www.w3.org/MarkUp/Forms/wiki/XForms_2.0)
  - W3C にある XForms 関連資料
      - [The Forms Working Group](http://www.w3.org/MarkUp/Forms/)
      - [The XForms Users Community Group](http://www.w3.org/community/xformsusers/)
      - [XForms 1.0 Frequently Asked Questions](http://www.w3.org/MarkUp/Forms/2003/xforms-faq.html)
      - [XForms for HTML Authors](http://www.w3.org/MarkUp/Forms/2003/xforms-for-html-authors.html) by Steven Pemberton（チュートリアル）
      - [XForms Quick Reference](http://www.w3.org/MarkUp/Forms/2006/xforms-qr.html)
  - XForms 関連フォーラムとニュースリリース
      - [Planet XForms](http://planetxforms.org/)
      - [XForms Central](http://news.xforms.org/)
  - ツール
      - [XFV XForms Validator tool](http://xformsinstitute.com/validator)
      - [AJAXForms](http://ajaxforms.sourceforge.net)
      - [XSLTForms](http://www.agencexml.com/xsltforms/)
      - [XHTML to XForms converter](http://sourceforge.net/projects/xhtml-to-xforms) （[XSLT](../Page/XSL_Transformations.md "wikilink") スタイルシートを使って、[XHTMLフォームを](../Page/Extensible_HyperText_Markup_Language.md "wikilink") XForms 文書に変換する）
      - [Nuxeo's XForms engine](http://blogs.nuxeo.com/sections/blogs/eric_barroca/2006_02_14_eclipse-apogee-xforms-engine-released) [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink")/[SWTコンポーネント](../Page/Standard_Widget_Toolkit.md "wikilink")
  - フォーム例
      - [Mozilla XForms Project - Sample Forms](http://www.mozilla.org/projects/xforms/samples.html)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")