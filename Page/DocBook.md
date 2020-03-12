> この記事は[DocBook](https://ja.wikipedia.org/wiki/DocBook)から翻訳されています。


**DocBook**は技術文書のための[マークアップ言語](../Page/マークアップ言語.md "wikilink")である。元々の用途はコンピュータの[ハードウェア](../Page/ハードウェア.md "wikilink")や[ソフトウェア](../Page/ソフトウェア.md "wikilink")に関する技術文書の作成だったが、他の種類の[文書](../Page/文書.md "wikilink")のためにも使うことができる。

DocBookの利点のうち特に大きなものの一つは、文書内容の論理的な構造を表す、表示形式に依存しない文書の作成が可能となることである。そのようにして作った文書はユーザーが文書に手を入れることなく、[HTML](../Page/HyperText_Markup_Language.md "wikilink")・[EPUB](https://ja.wikipedia.org/wiki/EPUB "wikilink")・[PDF](../Page/Portable_Document_Format.md "wikilink")・[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")・[HTMLヘルプなどの様々なフォーマットで出力できる](../Page/Microsoft_Compiled_HTML_Help.md "wikilink")。

## 歴史

DocBookは[1991年](../Page/1991年.md "wikilink")に[HaL Computer SystemsとO](https://ja.wikipedia.org/wiki/HALコンピュータシステム "wikilink")'Reilly & Associates（現在の[オライリーメディア](../Page/オライリーメディア.md "wikilink")）の共同プロジェクトとして始まった。初期は独自の組織 (Davenport Group) のもとで管理されていたが、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にSGML Open、後の[OASIS](../Page/OASIS_\(組織\).md "wikilink")（構造化情報標準促進協会）の下に移行した。現在はOASISのDocBook Technical Committeeによって管理されている。

DocBookは[SGMLと](../Page/Standard_Generalized_Markup_Language.md "wikilink")[XMLの両形式のために](../Page/Extensible_Markup_Language.md "wikilink")[DTDが用意されている](../Page/Document_Type_Definition.md "wikilink")。XMLならば[RELAX NGと](../Page/RELAX_NG.md "wikilink")[XML Schemaも利用可能である](https://ja.wikipedia.org/wiki/XML_Schema "wikilink")。DocBook 5以降、RELAX NGが標準形式となり、他のフォーマットはRELAX NG版から生成されている。

DocBookはそもそもSGMLアプリケーションとして登場したが、等価なXMLアプリケーションが開発され、ほとんどの環境でXML版に置き換わっている。ちなみに、XMLのDTDはバージョン4から登場し、それ以降、SGMLのDTDはバージョンアップしていない。

初期は設計に関わった主要なソフトウェア会社の間で使われるだけだったが、その後、DocBookは[オープンソース](../Page/オープンソース.md "wikilink")コミュニティで多くのプロジェクトのドキュメント作成のデファクトスタンダードして受け入れられた。[FreeBSD](../Page/FreeBSD.md "wikilink")・[KDE](../Page/KDE.md "wikilink")・[GNOME](../Page/GNOME.md "wikilink")のドキュメント、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")の[APIリファレンス](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")やその他の[Linux](../Page/Linux.md "wikilink")関連ドキュメント、などが有名な例である。オープンソースコミュニティ以外での使用も増え続けている。また、DocBookに対する何らかのサポートを含む商用の文書作成ツールも多く出回っている。

DocBookのソースから出力文書を作り出すためのキーとなるアプリケーションは、ノーマン・ウォルシュら DocBookプロジェクトの開発チームがメンテナンスしている、[XSLスタイルシート](../Page/Extensible_Stylesheet_Language.md "wikilink")、およびレガシーな[DSSSLスタイルシートである](../Page/Document_Style_Semantics_and_Specification_Language.md "wikilink")。それらのスタイルシートを使えば、高品質なHTML・[XSL-FO](../Page/XSL_Formatting_Objects.md "wikilink")・PDFを出力することができ、また[RTF](../Page/Rich_Text_Format.md "wikilink")・manページ・HTMLヘルプなどのフォーマットでも出力することができる。ウォルシュはDocBookの公式ドキュメントである*DocBook: The Definitive Guide*の中心的な著者でもある。この本は出版物として以外にもオンラインで[GFDLの下で利用できる](../Page/GNU_Free_Documentation_License.md "wikilink")。[1](http://www.docbook.org/docs/)

DocBookはXMLであるので、どんなテキストエディタでも書くことができるが、よりシンプルに作業を進めることのできる多くの専用ツールが存在する。[Emacs](../Page/Emacs.md "wikilink")のXML modeにはDocBookのスキーマ情報が組み込みで付属し、ユーザーは素早く要素の追加や文書の検証などが行える。DocBook文書を、各要素を[CSSでスタイル付けすることで](../Page/Cascading_Style_Sheets.md "wikilink")、視覚的に表示する[WYSIWYG](../Page/WYSIWYG.md "wikilink")エディタも存在する。

## コード例

``` xml
<book id="simple_book">
  <title>Very simple book</title>
  <chapter id="chapter_1">
    <title>Chapter 1</title>
    <para>Hello world!</para>
    <para>I hope that your day is proceeding <emphasis>splendidly</emphasis>!</para>
  </chapter>
  <chapter id="chapter_2">
    <title>Chapter 2</title>
    <para>Hello again, world!</para>
  </chapter>
</book>
```

DocBookのフォーマットはXMLで書かれており、コンピュータと同様に人間にも可読である。そのフォーマットは「タグ」（<book>など）とテキストである内容（`Hello world!`など）から成る。タグは</book>のような「閉じタグ」と1対1で対応している。文書全体(`book`)は2つの章(`chapter`)に構造化されており、それぞれ1つのタイトル(`title`)と1つ以上の段落(`para`)から構成される。これは文書が任意の大きさになっても成り立つ。

注意しておかねばならないのは、タグはテキストの「構造」や「意味」を示しているのであって、「見栄え」ではないということである。つまり「この段落をボールドにしろ」「センタリングしろ」などの命令は存在しない。そういう設計なのである。1つのDocBookファイルから多くのフォーマットで出力を得ることができるが、それぞれ見た目が全く異なり、さらには要素の配置さえも異なることがある。

## Simplified DocBook

DocBookには多くの機能があるので、新規の利用者は圧倒されてしまうかもしれない。学習に長い時間をかけることなくDocBookを利用したい者のために、**Simplified DocBook**が設計された。DocBookの小さなサブセットであり、論文や記事などの単一の文書のために設計されている。つまり本(book)はサポートされない。Simplified DocBookのDTDは現在バージョン1.1である。[2](http://www.docbook.org/schemas/simplified)

## 脚注

### 出典

## 参考文献

  -
  -
  -
## 外部リンク

  - 英語
      - ["What is DocBook?"](http://www.oasis-open.org/docbook/intro.shtml) - Oasis-open.org
      - [DocBook Repository at OASIS](http://www.oasis-open.org/docbook/) - DocBookのスキーマ/DTDのオフィシャルサイト
      - [DocBook Project](http://sourceforge.net/projects/docbook/) - DocBookのXSLおよびDSSSLスタイルシートをメンテナンスしているSourceforgeプロジェクト
      - [DocBook validator、XML → HTML/PDF transformer](http://sourceforge.net/projects/validate/)
      - [DocBook to OpenDocument XSLT (docbook2odf)](http://open.comsultia.com/docbook2odf/) - DocBookのXSLTスタイルシート、OpenDocumentへの変換ユーティリティ
      - [EServer TC Library: DocBook](http://tc.eserver.org/dir/DocBook)
  - 日本語
      - [DocBookの概要](http://www.est.co.jp/ks/dish/9906st6/DocBook.ppt) (ppt) - 1999年作成

### チュートリアルおよびリファレンス

  - 英語
      - [DocBook.org](http://www.docbook.org) - Norman Walsh *DocBook: The Definitive Guide*のウェブサイト。Wiki、FAQなど。
      - [DocBook XSL: The Complete Guide](http://www.sagehill.net/docbookxsl/)
      - [Documention with DocBook on Win32](http://www.codeproject.com/winhelp/docbook_howto.asp)
      - [DocBook Demystification HOWTO](http://tldp.org/HOWTO/DocBook-Demystification-HOWTO/)
  - 日本語
      - [実用DocBook入門](http://archive.linux.or.jp/JF/JFdocs/docbook-intro/)
      - [DocBookで作るWindows Helpサンプル](http://www.kobu.com/docs/docbook/index.htm)
      - [DocBookによるドキュメント作成](http://japan.internet.com/developer/20080108/26.html)
      - [EclipseでDocBook XMLを構築する](http://www.ibm.com/developerworks/jp/opensource/library/os-eclipse-docbook/)

[Category:DTPソフト](https://ja.wikipedia.org/wiki/Category:DTPソフト "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")