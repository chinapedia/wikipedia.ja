> この記事は[XHTML Mobile Profile](https://ja.wikipedia.org/wiki/XHTML_Mobile_Profile)から翻訳されています。


**XHTML Mobile Profile**（**XHTML MP**）は、[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")型[コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")の規格であり、[携帯電話](../Page/携帯電話.md "wikilink")などのリソースの限られた機器で利用することを目的として設計された。

[オープン・モバイル・アライアンス](https://ja.wikipedia.org/wiki/オープン・モバイル・アライアンス "wikilink") (OMA) が定義した [XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") [DTD](../Page/Document_Type_Definition.md "wikilink") である。XHTML MP は XHTML Basic 1.0 に XHTML Modules を追加したものであり、その後さらにモジュールが追加されている。しかし一部のモジュールは XHTML MP 規格では実装を強制されていないため、XHTML MP 準拠ブラウザが全てのモジュールを実装しているとは限らない。最新の勧告である XHTML MP 1.2 DTD は、2008年3月に完成した。

## DOCTYPE

XHTML MP 準拠を名のるには、仕様のバージョンに応じて、以下のいずれかの DTD あるいは DOCTYPE を含まなければならない。

``` xml
<!DOCTYPE html PUBLIC "-//WAPFORUM//DTD XHTML Mobile 1.0//EN"
"http://www.wapforum.org/DTD/xhtml-mobile10.dtd">

<!DOCTYPE html PUBLIC "-//WAPFORUM//DTD XHTML Mobile 1.1//EN"
"http://www.openmobilealliance.org/tech/DTD/xhtml-mobile11.dtd">

<!DOCTYPE html PUBLIC "-//WAPFORUM//DTD XHTML Mobile 1.2//EN"
"http://www.openmobilealliance.org/tech/DTD/xhtml-mobile12.dtd">
```

なお、一連のリビジョンは以前のDTDの技術的問題を解決すべく発行されている。また、DTDフォーマットは標準のHTMLに比較すると複雑であり、あまり広くサポートされているとは言えない。

## MIMEタイプ

XHTML Mobile Profile の[MIMEタイプは](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink") "application/vnd.wap.xhtml+xml" である。準拠している[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")は "application/xhtml+xml" と "text/html" を受理すべきとされる。XML MIMEタイプが指定される場合、多くのデスクトップのブラウザは表示の際に XHTML MP 有効にするだけである。

## バージョン

  - Version 1.0 - XHTML Basic 1.0 に表示要素をいくつか追加し、基本的なスクリプトをサポート
  - Version 1.1 - 完全なスクリプトサポート（[ECMAScript Mobile Profile](../Page/ECMAScript.md "wikilink")）
  - Version 1.2 - Forms と Object のサポートを追加

## サポートモジュール

XHTML MP 1.2 のサポートするモジュールは以下の通り。

  - Structure
  - Texts
  - Hypertext
  - List
  - Forms
  - Basic Tables
  - Image
  - Object
  - Metainformation
  - Scripting
  - Style Sheet
  - Style Attribute
  - Link
  - Base

XHTML-MP 1.2 は、以下を部分的にサポートしている。

  - Presentation
  - Intrinsic Events
  - Legacy

version 1.2 には、OMA独自モジュール ("Text Input Modes") も含まれており、携帯電話での各種入力モードを扱っている。

## 開発時の注意点

XHTMLで書かれたコンテンツを様々な機器で表示させようとすると、多くの問題が生じる。例えば[CSSで指定された色を守るものもあれば](../Page/Cascading_Style_Sheets.md "wikilink")、そうでない機器もあり、テーブルを正しく描画できるものもあれば、そうでないものもある。適応型アプリケーションの構築とは、機器の持つ機能によってコンテンツを変えることを意味する。しかし、市場には様々なハードウェア（画面サイズ、色機能、ボタン、メモリ、性能）と[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")があり、これらを考慮することは大変な複雑さとなる。携帯機器でのブラウザの更新はデスクトップのブラウザほど容易なものではないので、問題のあるブラウザでもその携帯機器が廃棄されるまで使われ続けることになる。

様々な団体がこの問題への対策を提案している。その多くは[WAPコンテンツを書く独自言語を提供し](../Page/Wireless_Application_Protocol.md "wikilink")、機器に対応して様々なコンテンツ（XHTML MP、[WML](../Page/Wireless_Markup_Language.md "wikilink")、[CHTMLなど](https://ja.wikipedia.org/wiki/Compact_HTML "wikilink")）を渡すというものである。[FLOSS](https://ja.wikipedia.org/wiki/FLOSS "wikilink")コミュニティでの関連標準として[WURFL](https://ja.wikipedia.org/wiki/WURFL "wikilink")がある。これは階層型[XML設定ファイルを使って数百のデバイス機能をマッピングし](../Page/Extensible_Markup_Language.md "wikilink")、マークアップをその機器がサポートするものに変換する "Wireless Abstraction Layer" (WALL) も設けたものである。[W3C](../Page/World_Wide_Web_Consortium.md "wikilink") Device Description Working Group (DDWG) は、機器の機能情報のリポジトリへのアクセスをコンテンツ適応技術のフレームワークの一部として標準化する仕様を作成している。

## 例

完全に妥当かつ整形式の例を以下に示す。

>
>
>     <nowiki>
>     <?xml version="1.0" encoding="UTF-8"?>
>     <!DOCTYPE html PUBLIC "-//WAPFORUM//DTD XHTML Mobile 1.1//EN"
>       "http://www.openmobilealliance.org/tech/DTD/xhtml-mobile11.dtd">
>     <html ns="http://www.w3.org/1999/xhtml" xml:lang="en">
>       <head>
>         <title>Hello</title>
>       </head>
>       <body>
>         <p>Hello <a href="http://example.org/">world</a>.</p>
>       </body>
>     </html>
>     </nowiki>

ただし、MIMEタイプは "application/xhtml+xml" または "application/vnd.wap.xhtml+xml" である。

## 外部リンク

  - [www.openmobilealliance.org](http://www.openmobilealliance.org/)
  - W3C勧告 [XHTML 1.1](http://www.w3.org/TR/xhtml11/)
  - W3C勧告 [Modularization of XHTML](http://www.w3.org/TR/2001/REC-xhtml-modularization-20010410/) （2001年4月10日）
  - [An Overview of Mobile Versions of XHTML](http://www.littlespringsdesign.com/design/xhtmlinfo/)
  - [XHTML-MP Authoring Practices](http://www.passani.it/gap/)

[Category:携帯電話ブラウジング](https://ja.wikipedia.org/wiki/Category:携帯電話ブラウジング "wikilink")