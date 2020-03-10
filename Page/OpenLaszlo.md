> この記事は[OpenLaszlo](https://ja.wikipedia.org/wiki/OpenLaszlo)から翻訳されています。


**OpenLaszlo**(オープンラズロ)は[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")/[Flashで動作する](../Page/Adobe_Flash.md "wikilink")[リッチインターネットアプリケーション](https://ja.wikipedia.org/wiki/リッチインターネットアプリケーション "wikilink")の開発及び配布を行うための[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアである。

一種類の言語体系で[Flashコンテンツや](../Page/Adobe_Flash.md "wikilink")[DHTML](https://ja.wikipedia.org/wiki/DHTML "wikilink")([Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink"))コンテンツを出力できるマルチ[ランタイム機能が最大の特徴](../Page/ランタイムライブラリ.md "wikilink")。

OpenLaszloアプリケーションの開発には独自の[XMLベース言語](../Page/Extensible_Markup_Language.md "wikilink")**LZX**と[JavaScript](../Page/JavaScript.md "wikilink")を使用するため、[HTMLと](../Page/HyperText_Markup_Language.md "wikilink")[JavaScript](../Page/JavaScript.md "wikilink")に慣れ親しんだWebアプリケーション開発者にとって親しみやすい言語設計になっている。

開発環境に必要なOpenLaszloサーバは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[サーブレット](https://ja.wikipedia.org/wiki/サーブレット "wikilink")であり、[Tomcat等の](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")[Webコンテナ](../Page/Webコンテナ.md "wikilink")上で動作する。実行環境では必ずしもOpenLaszloサーバを必要としない。Flashコンテンツとしてコンパイルした場合、swfファイルが一つ生成されるので通常のFlashコンテンツと同様の使い方ができる。

## Hello World

OpenLaszloのHello Worldのソースコード例。

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<canvas>
  <text>Hello World</text>
</canvas>
```

## ライセンス

[ライセンス](../Page/ライセンス.md "wikilink")は[Open Source Initiative認定の](../Page/Open_Source_Initiative.md "wikilink")[Common Public Licenseである](https://ja.wikipedia.org/wiki/Common_Public_License "wikilink")。

## プロジェクトヒストリー

OpenLaszloは当初Laszlo Presentation Server(LPS)と呼ばれていた。LPSの開発が始まったのは2001年の秋で、最初のプレビューリリースは2002年前半であった。2004年10月、Laszlo SystemsはLPSをオープンソース化し、OpenLaszloコミュニティを立ち上げた。2005年のバージョン3.0リリースに伴い、LPSはOpenLaszloと名前を変えた。

  - 2000: プロトタイピング開始
  - 2001: 開発開始
  - 2002: LPSプレビュー版リリース
  - 2003: LPS 1.0, 1.1 リリース
  - 2004: LPS 2.0, 2.1, 2.2 リリース; LPSオープンソース化
  - 2004/11/08: LPS 2.2.1 リリース
  - 2005/04/26: OpenLaszlo 3.0リリース ; OpenLaszloに改名
  - 2005/07/13: OpenLaszlo 3.0.2リリース
  - 2005/11/17: OpenLaszlo 3.1リリース ;swf8に対応
  - 2005/12/22: OpenLaszlo 3.1.1リリース
  - 2006/03/24: OpenLaszlo 3.2リリース
  - 2006/05/21: OpenLaszlo 3.3リリース
  - 2006/06/07: OpenLaszlo 3.3.1リリース
  - 2006/07/19: OpenLaszlo 3.3.3リリース
  - 2007/03/14: OpenLaszlo 3.4.0リリース
  - 2007/03/20: OpenLaszlo 4.0.0リリース ;DHTML(Ajax)に対応
  - 2007/05/18: OpenLaszlo 4.0.2リリース
  - 2007/07/27: OpenLaszlo 4.0.3リリース
  - 2007/09/19: OpenLaszlo 4.0.5リリース
  - 2007/10/15: OpenLaszlo 4.0.6リリース
  - 2007/11/19: OpenLaszlo 4.0.7リリース
  - 2008/01/14: OpenLaszlo 4.0.8リリース
  - 2008/01/28: OpenLaszlo 4.0.9リリース
  - 2008/02/21: OpenLaszlo 4.0.10リリース
  - 2008/03/28: OpenLaszlo 4.0.11リリース
  - 2008/04/14: OpenLaszlo 4.0.12リリース
  - 2008/06/30: OpenLaszlo 4.1リリース
  - 2008/07/11: OpenLaszlo 4.1.1リリース
  - 2008/12/20: OpenLaszlo 4.2リリース ;swf9に対応
  - 2009/02/20: OpenLaszlo 4.2.0.1リリース
  - 2009/03/11: OpenLaszlo 4.2.0.2リリース
  - 2009/04/02: OpenLaszlo 4.3.0リリース ;swf10に対応
  - 2009/06/29: OpenLaszlo 4.4.0リリース
  - 2009/07/18: OpenLaszlo 4.4.1リリース
  - 2009/08/07: OpenLaszlo 4.5.0リリース
  - 2009/08/10: OpenLaszlo 4.5.1リリース
  - 2009/09/18: OpenLaszlo 4.6.1リリース
  - 2010/01/16: OpenLaszlo 4.7.0リリース
  - 2010/02/16: OpenLaszlo 4.7.1リリース
  - 2010/04/19: OpenLaszlo 4.7.2リリース
  - 2010/06/07: OpenLaszlo 4.7.3リリース
  - 2010/07/01: OpenLaszlo 4.8.0リリース
  - 2010/07/29: OpenLaszlo 4.8.1リリース
  - 2010/10/21: OpenLaszlo 4.9.0リリース ;swf8/swf10/HTML5

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")