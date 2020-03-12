> この記事は[Synchronized Multimedia Integration Language](https://ja.wikipedia.org/wiki/Synchronized_Multimedia_Integration_Language)から翻訳されています。


**Synchronized Multimedia Integration Language**は、[WWW上で](../Page/World_Wide_Web.md "wikilink")[マルチメディア](../Page/マルチメディア.md "wikilink")[コンテンツ](../Page/コンテンツ.md "wikilink")を表現するための[マークアップ言語](../Page/マークアップ言語.md "wikilink")の一つである。静止画、動画、音声、文字（テキスト）などの、位置レイアウト、時間軸上でのレイアウトを、[Extensible Markup Language](../Page/Extensible_Markup_Language.md "wikilink") (XML) フォーマットで記述することで統合し、再生させることができる。略称は**SMIL**で、**スマイル**と読む。**同期マルチメディア統合言語**と[日本語](../Page/日本語.md "wikilink")訳されることもある。

SMILは、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink") (W3C) 勧告による仕様のひとつである。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に登場し、W3Cによって[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")6月に**SMIL 1.0**として仕様勧告となった\[1\]。その後**SMIL2.1**を経て、最新バージョンである**SMIL 3.0**が、2008年12月1日に勧告された。

## 記法

XMLフォーマットに準拠している。例として、異なるフォーマットの動画ファイルを縦に並べて同時に再生する記述を示す。

``` xml
<smil>
  <head>
    <meta name="title" content="Hello, World" />
    <layout>
      <root-layout width="320" height="480" />
      <region id="hello" width="320" height="240" left="0" top="0" />
      <region id="world" width="320" height="240" left="0" top="240" />
    </layout>
  </head>
  <body>
    <seq>
      <video src="hello.3gp" region="hello" />
      <video src="world.mpg" region="world" />
    </seq>
  </body>
</smil>
```

## 再生可能なソフトウェア・ハードウェア

  - [GRiNS Player](https://ja.wikipedia.org/wiki/GRiNS_Player "wikilink")
  - [SOJA](https://ja.wikipedia.org/wiki/SOJA "wikilink")（[Javaアプレット](../Page/Javaアプレット.md "wikilink")）
  - [X-Smiles browser](https://ja.wikipedia.org/wiki/X-Smiles_browser "wikilink")（XMLブラウザ）
  - [RealPlayer](../Page/RealPlayer.md "wikilink")
  - [au](../Page/Au_\(携帯電話\).md "wikilink") [CDMA 1X WIN](../Page/CDMA_1X_WIN.md "wikilink")[携帯電話](../Page/携帯電話.md "wikilink")[端末](../Page/端末.md "wikilink")（[W21H](../Page/W21H.md "wikilink")および[データ端末を除く](https://ja.wikipedia.org/wiki/CDMA_1X_WIN#データ端末 "wikilink")）

## オーサリングソフト

  - [SMIL Scenario Creator](https://ja.wikipedia.org/wiki/SMIL_Scenario_Creator "wikilink")（[KDDI研究所](https://ja.wikipedia.org/wiki/KDDI研究所 "wikilink")）
  - [SMIL Editor](https://ja.wikipedia.org/wiki/SMIL_Editor "wikilink")（[ドコモ・システムズ](https://ja.wikipedia.org/wiki/ドコモ・システムズ "wikilink")）
  - [SmilSmil](https://ja.wikipedia.org/wiki/SmilSmil "wikilink")
  - [RealSlideshow](https://ja.wikipedia.org/wiki/RealSlideshow "wikilink")
  - [Fluition](https://ja.wikipedia.org/wiki/Fluition "wikilink")
  - [GRiNS Editor](https://ja.wikipedia.org/wiki/GRiNS_Editor "wikilink")
  - [SMIL Composer](https://ja.wikipedia.org/wiki/SMIL_Composer "wikilink")

## 日本での応用事例

[auの](../Page/Au_\(携帯電話\).md "wikilink")[携帯電話](../Page/携帯電話.md "wikilink") [CDMA 1X WIN端末では](../Page/CDMA_1X_WIN.md "wikilink")、大容量番組配信サービスである[EZチャンネル](../Page/EZチャンネル.md "wikilink")でSMILの技術が利用されている。通話や[電子メール](../Page/電子メール.md "wikilink")など端末が持つ機能との連携や、配信における[著作権](../Page/著作権.md "wikilink")の保護に関する独自拡張も含む。

## 脚注

## 外部リンク

  - [W3Cによる勧告](http://www.w3.org/AudioVideo/)
  - [SMIL 1.0. 仕様書の和訳](http://www.doraneko.org/misc/smil10/)
  - [SMIL Scenario Creator](http://mmm.kddilabs.jp/ja/sc/index.html)

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.