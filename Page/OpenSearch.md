> この記事は[OpenSearch](https://ja.wikipedia.org/wiki/OpenSearch)から翻訳されています。


**OpenSearch**は[シンジケーションと](https://ja.wikipedia.org/wiki/フィード "wikilink")[アグリゲーションに適する形式で](https://ja.wikipedia.org/wiki/アグリゲータ "wikilink")[検索結果を発行することを可能にする技術群である](https://ja.wikipedia.org/wiki/情報検索 "wikilink")。これは[ウェブサイト](../Page/ウェブサイト.md "wikilink")と[検索エンジン](../Page/検索エンジン.md "wikilink")が標準的でアクセス可能な形式で検索結果を発行する方法である。OpenSearchは[Amazon.com](../Page/Amazon.com.md "wikilink")の子会社[A9によって開発され](https://ja.wikipedia.org/wiki/A9.com "wikilink")、最初のバージョンである、OpenSearch 1.0は2005年5月のWeb 2.0において[ジェフ・ベゾス](https://ja.wikipedia.org/wiki/ジェフ・ベゾス "wikilink")により公開された。OpenSearch 1.1のドラフトバージョンは2005年11月から12月にかけてリリースされた。OpenSearch仕様はクリエイティブ・コモンズ・ライセンス下で、A9によりライセンスされている。

## 概要

OpenSearchは以下から構成される:

1.  OpenSearch Descriptionファイル: 検索エンジンを特定し、説明する[XMLファイル](../Page/Extensible_Markup_Language.md "wikilink")。
      - OpenSearch Query Syntax: 検索結果を取得できる場所の記述
2.  OpenSearch RSS（OpenSearch 1.0）またはOpenSearch Response（OpenSearch 1.1）: open search結果を供給するための形式。
3.  OpenSearch Aggregators: OpenSearch結果を表示するサイト。

OpenSearch Description Documentsは特定のウェブサイト/ツールのための結果レスポンスを一覧にする。仕様のバージョン1.0では、[RSS](../Page/RSS.md "wikilink")形式で、一つのレスポンスのみを許した。しかしながら、バージョン1.1では何らかの形式の、複数のレスポンスのサポートを提供している。[HTMLなどの他の形式も完全に許容されるが](../Page/HyperText_Markup_Language.md "wikilink")、しかしながらRSSと[Atomだけが正式にOpenSearchアグリゲータで正式にサポートされる唯一の形式である](https://ja.wikipedia.org/wiki/Atom_\(ウェブコンテンツ配信\) "wikilink")。

## OpenSearchをサポートする検索エンジンとソフトウェア

  - [A9.com](https://ja.wikipedia.org/wiki/A9.com "wikilink")
  - [Live Search](https://ja.wikipedia.org/wiki/Live_Search "wikilink")
  - [Yahoo\!](https://ja.wikipedia.org/wiki/Yahoo! "wikilink")検索
  - [Nuvvo e-Learning](https://ja.wikipedia.org/wiki/Nuvvo "wikilink")
  - [OSFeed](http://osfeed.com)
  - [Bargainstriker RSS Shopping](http://www.bargainstriker.com/about.do)
  - [Internet Explorer](../Page/Internet_Explorer.md "wikilink") 7, 8
  - [Windows 7](../Page/Microsoft_Windows_7.md "wikilink")
  - [Microsoft SharePoint](https://ja.wikipedia.org/wiki/Microsoft_SharePoint "wikilink")
  - [Microsoft Search Server](https://ja.wikipedia.org/wiki/Microsoft_Search_Server "wikilink")
  - [Eluta.ca](https://ja.wikipedia.org/wiki/Eluta.ca "wikilink")
  - [WWW::OpenSearch](http://search.cpan.org/~miyagawa/WWW-OpenSearch-0.04/lib/WWW/OpenSearch.pm) - [Perl](../Page/Perl.md "wikilink")モジュール
  - [textualize's opensearch](http://www.textualize.com/opensearch) -- [Python](../Page/Python.md "wikilink")モジュール
  - [Kwiki::OpenSearch](http://search.cpan.org/~miyagawa/Kwiki-OpenSearch-0.02/lib/Kwiki/OpenSearch.pm) - *Kwiki*[ウィキ](../Page/ウィキ.md "wikilink")エンジンで使用するためのPerlモジュール。
  - [PEAR Services_OpenSearch](http://pear.php.net/package/Services_OpenSearch) - PHP OpenSearch APIライブラリ
  - [Search Addons](http://searchaddons.com) - ブラウザの検索ボックスのための検索エンジンリストおよびプロバイダ。
  - [OpenSearch Klip](http://www.edazzle.net/os/) - [Klipfolio](http://www.serence.com/)ソフトウェアで使用
  - [searchplugins.net](http://www.searchplugins.net/) - [IE7](http://www.microsoft.com/windows/ie/downloads/default.mspx)およびFirefox2 ([Minefield](http://www.mozilla.org/projects/minefield/)または[Bon Echo](http://www.mozilla.org/projects/bonecho/))ビルドで使うためのOpenSearchプラグインの作成
  - [Mozdex.com OpenSearch](http://www.mozdex.com/developer/)
  - [Nestoria](http://www.nestoria.co.uk/) - UK Property Search Engine.
  - [Nurse Web Search](http://www.nursewebsearch.com/) - Health Internet Search Engine.
  - [Drupal.org OpenSearch Module](http://drupal.org/project/opensearch) (Steven Wittens)
  - [YaCy](https://ja.wikipedia.org/wiki/YaCy "wikilink")
  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") 2.0 - OpenSearchを実装し、MozSearchと名づけられた実装。MozSearchはFirefox関連プロジェクトだけのためのもので、Webでの使用を意図していない。Mozsearchからの拡張機能は、XML名前空間プレフィクスを含むOpenSearchファイルで使用できる。
  - [nutch](http://lucene.apache.org/nutch/) - オープン・ソースのWeb検索ソフトウェア
  - [Yandex](https://ja.wikipedia.org/wiki/Yandex "wikilink") - ロシアの検索エンジン
  - [Xapian](https://ja.wikipedia.org/wiki/Xapian "wikilink")の"opensearch" OmegaScriptを含むOmegaサーチフロントエンド。
  - [BoardReader](http://boardreader.com) 検索エンジンフォーラム
  - [Zoom Search Engine](http://www.wrensoft.com/zoom/) - OpenSearch互換の検索結果を提供する検索エンジン。
  - [Alfresco](https://ja.wikipedia.org/wiki/Alfresco_\(software\) "wikilink") - エンタープライズ・コンテンツ・マネジメント・システム。
  - [AirportLinger.com](http://airportlinger.com) - 空港検索エンジン。
  - [greensear.ch](http://greensear.ch) - Environmentally responsible search engine that donates ad revenue to national non-profits
  - [pathtraq.com](http://pathtraq.com) - 旬な話題や人気のサイトを検索出来るランキングサイト
  - [CiNii](https://ja.wikipedia.org/wiki/CiNii "wikilink") - [国立情報学研究所](https://ja.wikipedia.org/wiki/国立情報学研究所 "wikilink")が提供する論文検索データベース[1](http://ci.nii.ac.jp/info/ja/if_opensearch.html)
  - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") - OpenSearch Description Documentへのリンクを持っているサイトでユーザーが検索を行った場合、自動的に検索プロバイダに登録し、OmniBoxと呼ばれるアドレスバーと検索ボックスなどを統合したバーでタブキーを用いた検索が可能となる。

## OpenSearchフィードのディレクトリ

A9の[OpenSearch Description Documents](http://opensearch.a9.com/spec/opensearchdescription/1.0/)の公共のオープンディレクトリが、2005年8月5日に利用可能になった。このディレクトリは[HTML search](http://a9.com/blog?a=oB000813UB2)、[OpenSearch RSS feed](http://a9.com/-/opensearch/search/B000813UB2/blog)、またはこれらの基盤である[Description Document](http://a9.com/-/opensearch/public/osd)経由でアクセスできる。

## ブログコンテンツをOpenSearch APIに利用可能にするプラグイン

  - [ROME OpenSearch Java Module (Beta)](http://wiki.java.net/bin/view/Javawsxml/OpenSearch) - Rome A9 OpenSearch 1.1 API for Java (Michael Nassif)
  - [Movable Type](http://hublog.hubmed.org/archives/001212.html) - OpenSearch 1.1 (Alf Eaton)
  - [Movable Type](http://www.niallkennedy.com/blog/archives/2005/03/opensearch_stan.html) - OpenSearch 1.0 (Niall Kennedy)
  - [WordPress](http://www.williamsburger.com/wb/archives/opensearch-v-1-0) (Chris Fairbanks)

## 関連項目

  - [Z39.50](https://ja.wikipedia.org/wiki/Z39.50 "wikilink")
  - [SRU](https://ja.wikipedia.org/wiki/Search/Retrieve_via_URL "wikilink")
  - [フィード](https://ja.wikipedia.org/wiki/フィード "wikilink")

## 外部リンク

  - [OpenSearch.org](https://github.com/dewitt/opensearch) -- 公式のウェブサイト、仕様書がある
  - [OpenSearch.a9.com](http://opensearch.a9.com/) -- a9.comへの検索登録のためのサイト
  - [Ready2Search](https://ready.to/search/jp/) -- Web上でのOpenSearchプラグインエディタ
  - [OpenSearch 1.1 (ドラフト4) 仕様書](http://sites.google.com/site/tsukamoto/doc/opensearch/spec-1-1-draft4) -- 仕様のバージョン1.1のドラフトの日本語訳

[Category:検索エンジン](https://ja.wikipedia.org/wiki/Category:検索エンジン "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink")