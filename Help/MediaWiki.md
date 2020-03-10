> この記事は[Help:MediaWiki](https://ja.wikipedia.org/wiki/Help:MediaWiki)から翻訳されています。


**[MediaWiki](https://ja.wikipedia.org/wiki/MediaWiki "wikilink")**というソフトウェアが、[ウィキペディアを含む](https://ja.wikipedia.org/wiki/Wikipedia:ウィキペディアについて "wikilink")[ウィキメディア・プロジェクトを動作させています](https://ja.wikipedia.org/wiki/Wikipedia:ウィキメディア・プロジェクト "wikilink")。[ウィキ](../Page/ウィキ.md "wikilink")の一種で、ブラウザを利用して[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")を簡単に複数の編集者で共同編集するためのシステムです。MediaWikiを用いて、編集や表示のための高度な環境を実現しています。

[\#外部リンク](https://ja.wikipedia.org/wiki/#外部リンク "wikilink")に、MediaWikiの仕様変更や機能更新の概要へのリンクがあります。

## MediaWiki概要

MediaWikiは、[オープンソース](../Page/オープンソース.md "wikilink")のウィキサイト構築用ソフトウェアであり、継続的に機能の改善（バージョンアップ）が進められています。もともとはウィキペディア用のソフトウェアとして開発されました。現在では、無償でインストールができることもあり、ウィキメディア・プロジェクト以外でもさまざまな個人・組織がMediaWikiを利用してウィキを立ち上げています。

MediaWikiの開発は [MediaWiki.org](https://ja.wikipedia.org/wiki/mw:MediaWiki/ja "wikilink") や [phabricator](https://ja.wikipedia.org/wiki/phabricator: "wikilink") にて[開発者が行っています](https://ja.wikipedia.org/wiki/mw:Developers "wikilink")。また、MediaWikiでは[拡張機能を追加することで](https://ja.wikipedia.org/wiki/mw:Manual:Extensions/ja "wikilink")、さまざまな機能を追加できますが、その開発や利用も主に同じ場所で多くはオープンソースとして行われています。

MediaWikiの利用や管理方法、また開発への参加などについては MediaWiki.org を参照してください。MediaWikiのダウンロードや、最新版リリースなどといったニュースの確認もここからできます。[Sites using MediaWiki](https://ja.wikipedia.org/wiki/mw:Sites_using_MediaWiki "wikilink")（また[同・日本語](https://ja.wikipedia.org/wiki/mw:Sites_using_MediaWiki/ja "wikilink")）には、MediaWikiを利用しているサイトの例が掲載されています。

MediaWikiやその拡張機能の日本語化は、MediaWikiの開発者である Nike と Siebrand が開設している [translatewiki.net](https://ja.wikipedia.org/wiki/betawiki:Main_Page "wikilink") というサイトで主に行われています。

## ウィキペディア日本語版の使用するMediaWiki

ウィキペディア日本語版で現在使用しているMediaWikiのバージョンは  です。[特別:バージョン情報](https://ja.wikipedia.org/wiki/特別:バージョン情報 "wikilink")では、さらに詳しいバージョン情報や追加されている拡張機能が表示できます。

ウィキペディアを含むウィキメディア・プロジェクトにおけるMediaWikiの設定やメンテナンスは、ウィキメディア財団の[システム管理者が行っています](https://ja.wikipedia.org/wiki/meta:System_administrators/ja "wikilink")。

ウィキペディアの機能は、そのほか[スタイルシート](../Page/スタイルシート.md "wikilink")やスクリプトによって追加・変更できます。例えば、[Mediawiki:Common.cssや](https://ja.wikipedia.org/wiki/MediaWiki:Common.css "wikilink")[Mediawiki:Common.jsの記述は](https://ja.wikipedia.org/wiki/MediaWiki:Common.js "wikilink")、すべての利用者の[外装](https://ja.wikipedia.org/wiki/Help:オプション#外装 "wikilink")（画面表示）に反映されます。スタイルシートやスクリプトは、[管理者が変更できます](https://ja.wikipedia.org/wiki/Wikipedia:管理者 "wikilink")。利用者個人で、スタイルシートやスクリプトを編集するには、[Help:外装の詳細設定を参照してください](https://ja.wikipedia.org/wiki/Help:外装の詳細設定 "wikilink")。

## ユーザー・インターフェース

[ユーザビリティ](https://ja.wikipedia.org/wiki/ユーザビリティ "wikilink")（使いやすさ）でいえば[ヤコブ・ニールセン](../Page/ヤコブ・ニールセン.md "wikilink")の原則や\[1\]\[2\]ウェブデザイン標準\[3\]が参照されています。ウィキメディアのユーザー・インタフェースの部品の標準化が行われており、ウィキペディアの記事、Mediawikiの文書、メタウィキなど、テンプレートやページなどをまたがって同じように見え理解できることを目的としています\[4\]。

[アクセシビリティ](https://ja.wikipedia.org/wiki/アクセシビリティ "wikilink")は[スクリーンリーダー](https://ja.wikipedia.org/wiki/スクリーンリーダー "wikilink")や[色覚異常](../Page/色覚異常.md "wikilink")でも大部分にアクセスできることです\[5\]。またモバイル機器のタッチスクリーンでも操作しやすいものを目標としています\[6\]。

また[ウィキペディア・ユーザビリティ・イニシアティブは](https://ja.wikipedia.org/wiki/Wikipedia:使用性改善 "wikilink")、使いやすさについての調査を行ってきており、その調査は以下のようなMediawikiの機能に関与してきました。

  - 「ベクター」という名の[外装](https://ja.wikipedia.org/wiki/Help:外装の詳細設定 "wikilink")：2010年に標準となった、サイトを表示するデザインです\[7\]。[検索機能も調査を基にボタンが統合され上部へ移動し](https://ja.wikipedia.org/wiki/Help:検索 "wikilink")、検索幅もニールセンの推奨する幅に近づいた\[8\]。
  - 改良型の[編集ツールバー](https://ja.wikipedia.org/wiki/Help:編集ツールバー "wikilink")：2010年に標準となった\[9\]。
  - [ビジュアルエディター](https://ja.wikipedia.org/wiki/Help:ビジュアルエディター "wikilink")：2013年より各言語版に導入されている\[10\]。日本語版では、ベータ版を経て2016年5月に広く導入されました。
  - [文字体裁の更新](https://ja.wikipedia.org/wiki/mw:Typography_refresh/ja "wikilink")：2014年、ベクターの文字表示が更新されました。可読性、端末によらない一貫性、アクセシビリティが考慮され、記事本文ではフォントサイズが読むのに不適な 0.8em ではなく、0.875em へと引き上げられました。文字色も「真っ黒」から「黒い灰色」へと変更されています。

## 機能の不具合報告や機能改善の提案

ウィキペディアで機能の不具合と思われる現象があった場合は、[Wikipedia:バグの報告を確認してください](https://ja.wikipedia.org/wiki/Wikipedia:バグの報告 "wikilink")。回避方法や修正の進ちょくなどが記載されているかもしれません。類似の現象についての記述がない場合は「バグの報告」に追加してください。バグであることが確認されれば、更に Bugzilla やメーリングリスト、チャットなどを通じてシステム管理者に連絡をします。

なお、バージョンアップやサーバーの不具合などといった理由で、一時的に閲覧・編集に支障が生じることがありますのでご了承下さい。アクセスが過剰な時などには、一時的に接続できず、エラー画面が表示されることがあります。このような時には、しばらく待ってから再接続してみてください。[サイドバーの表示などがおかしくなることもありますが](https://ja.wikipedia.org/wiki/Wikipedia:ウィキペディアを探検するには#サイドバー "wikilink")、これも一時的なもので、しばらくすると通常に戻ります。

また、機能改善の提案は[Wikipedia:井戸端で](https://ja.wikipedia.org/wiki/Wikipedia:井戸端 "wikilink")、類似の議論がないかを確認してから行ってください。

## 出典

<references />

## 関連ページ

  - [MediaWiki](https://ja.wikipedia.org/wiki/MediaWiki "wikilink") - 日本語版の記事、「歴史・変更点」節にバージョンごとの仕様の変更が書かれています。
  - [Wikipedia:データベースダウンロード](https://ja.wikipedia.org/wiki/Wikipedia:データベースダウンロード "wikilink") - 全コンテンツの一元化データ。
  - [Wikipedia:MediaWikiの変更](https://ja.wikipedia.org/wiki/Wikipedia:MediaWikiの変更 "wikilink")

## 外部リンク

  - [MediaWiki.org](https://ja.wikipedia.org/wiki/mw:MediaWiki/ja "wikilink") 公式ページ - マニュアル、拡張機能、ニュースなど、編集のためのMediaWikiの技術的な仕様が知りたい際の情報があるかもしれません。
      - [Wikimedia Engineering Goals](https://ja.wikipedia.org/wiki/mw:Wikimedia_Engineering/{{#expr:_{{CURRENTYEAR}}-1}}-{{#time:y}}_Goals "wikilink")  機能の改善や実装の状況の概要が記されています。

<!-- end list -->

  - [phabricator](https://ja.wikipedia.org/wiki/phabricator: "wikilink") 実際の実装や問題の報告はここでやり取りされています。

<!-- end list -->

  - [translatewiki.net](https://ja.wikipedia.org/wiki/betawiki:Main_Page "wikilink") 日本語化はここで行われています。ご参加ください。2004年までは[Wikipedia:LanguageJa.phpが使われていました](https://ja.wikipedia.org/wiki/Wikipedia:LanguageJa.php "wikilink")。

<!-- end list -->

  - [m:MediaWiki](https://ja.wikipedia.org/wiki/m:MediaWiki "wikilink") - [メタウィキメディアでの解説ページ](https://ja.wikipedia.org/wiki/Wikipedia:メタウィキメディア "wikilink")
      - [技術ニュースの最新号](https://ja.wikipedia.org/wiki/m:Special:MyLanguage/Tech/News/Latest/ja "wikilink")  週刊ニュースとなっており、最近の機能更新やお知らせの概要が示されています。未翻訳の場合もあります。
      - [m:Category:MediaWiki](https://ja.wikipedia.org/wiki/m:Category:MediaWiki "wikilink") - メタウィキにおけるMediaWikiのカテゴリー

<!-- end list -->

1.  [Heuristic evaluation of visual editing on iOS and Android phones](https://ja.wikipedia.org/wiki/mw:Heuristic_evaluation_of_visual_editing_on_iOS_and_Android_phones "wikilink") (Mediawiki, 22:09, 28 January 2016)
2.  [VisualEditor/Usability](https://ja.wikipedia.org/wiki/mw:VisualEditor/Usability "wikilink") (Mediawiki, 17:11, 14 May 2015)
3.
4.  [Wikimedia User Interface](https://ja.wikipedia.org/wiki/mw:Wikimedia_User_Interface "wikilink") (Mediawiki, 11:12, 2 March 2016‎)
5.
6.
7.  [Skin:ベクター](https://ja.wikipedia.org/wiki/mw:Skin:Vector/ja "wikilink") (Mediawiki, 04:06, 19 March 2016)
8.
9.  [m:Help:Edit toolbar](https://ja.wikipedia.org/wiki/m:Help:Edit_toolbar "wikilink") (Meta-wiki, 03:19, 16 February 2016‎)
10. [VisualEditor](https://ja.wikipedia.org/wiki/mw:VisualEditor "wikilink") (Mediawiki)