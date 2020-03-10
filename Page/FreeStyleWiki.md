> この記事は[FreeStyleWiki](https://ja.wikipedia.org/wiki/FreeStyleWiki)から翻訳されています。


**FreeStyleWiki**（フリースタイルウィキ）は、[Perl](../Page/Perl.md "wikilink")で書かれた[ウィキ](../Page/ウィキ.md "wikilink")クローンである。略称は**FSWiki**。

## 概要

徹底的なモジュール構造により基本的なコア部分以外はプラグインで実装している\[1\]。また、プラグインAPIは公開されておりプラグインにより機能拡張をすることが可能。ピュアなPerlで書かれているため、同種の他のソフトウェアに比べて設置するサーバ環境を比較的選ばない。

公式サイトではユーザー開発のプラグインを公開する場も設けられている。スキンによりスタイルを変更可能。ユーザー管理機能やPDF作成機能まである\[2\]。

機能を一部制限し、設置の簡易化と動作の高速化を図った**[FSWikiLite](https://ja.wikipedia.org/wiki/FSWikiLite "wikilink")**もある。

## 特徴

  - 徹底されたモジュール化により、プラグインによる拡張が容易
  - [RDBMS](https://ja.wikipedia.org/wiki/RDBMS "wikilink")を使用しないため、[CGI](https://ja.wikipedia.org/wiki/CGI "wikilink")が動作する多くのサーバに設置可能
  - mod_perlでの動作にも対応(3.4.1以降)
  - 全ページ共通のヘッダ、フッタ、サイドバーを表示可能
  - ファイルの添付やPDFの生成などが可能
  - [tDiary](https://ja.wikipedia.org/wiki/tDiary "wikilink")のテーマを使用可能
  - 簡単なユーザ認証機能を備えている

## 公式サイト問題

かつては有志 [BitCoffee, Inc.](http://bitcoffee.com) の厚意により公式サイトとして <http://fswiki.org/> のドメインとホスティングが提供されていたが、2010年以降同社の別サイトへ、2011年1月31日時点では同社レンタルWikiサービス <http://fswiki.com/> への転送となっていた。それ以前に構築されたサイト(バージョン3.6.3以前)ではフッタの公式サイトリンクが <http://fswiki.org/> となっているが、2011年1月31日現在では公式サイトではないサイトにリンクされた状態となっていた。フッタの公式サイトリンクはバージョン3.6.4で修正されている。

なお、2010年3月の問題発覚時より作者とホスティング提供者との間で連絡がとれておらず\[3\]、転送先がFreeStyleWikiを利用した営利サービスとなっていることから、一種の[ドメインスクワッティングと考えられる](../Page/サイバースクワッティング.md "wikilink")。

2012年3月14日現在、経緯は不明ながら、ドメイン所有者は BitCoffee, Inc. のまま <http://fswiki.org> は新公式サイトへの転送となっている。 2018年4月9日現在、fswiki.org ドメインは所有者なしとなっており使用されていない。

## 外部リンク

  - <http://fswiki.osdn.jp/cgi-bin/wiki.cgi>
  - <https://osdn.net/projects/fswiki/>

## 脚注

### 注釈

[Category:ウィキクローン](https://ja.wikipedia.org/wiki/Category:ウィキクローン "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  大半の機能が同梱または外部プラグインによる実装。
2.  これもプラグインによる実装。
3.  <http://d.hatena.ne.jp/takezoe/20100323/p1>