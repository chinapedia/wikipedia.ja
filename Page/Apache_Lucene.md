> この記事は[Apache Lucene](https://ja.wikipedia.org/wiki/Apache_Lucene)から翻訳されています。


**Apache Lucene**（アパッチ ルシーン）は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で記述された[全文検索](../Page/全文検索.md "wikilink")ソフトウェアである。あらかじめ蓄積した大量のデータから、指定したキーワードを探し出す機能を持つ。Javaのクラスライブラリとして提供される。

## 概要

1000万ドキュメントくらいの規模まで1台のマシンで対応できる。それ以上を複数のマシンで分散検索できるようにする[Hadoop](https://ja.wikipedia.org/wiki/Hadoop "wikilink")というサブプロジェクトがある。

[検索エンジン](../Page/検索エンジン.md "wikilink")（ライブラリ）だけの提供であり、ウェブアプリとしての機能は**[Solr](https://ja.wikipedia.org/wiki/Solr "wikilink")**、クローラーの機能は[Nutch](https://ja.wikipedia.org/wiki/Nutch "wikilink")というサブプロジェクトで開発されている。またApache外でも、リアルタイム検索システムの[Elasticsearch](https://ja.wikipedia.org/wiki/Elasticsearch "wikilink")のベースシステムなどに採用されている\[1\]。

日本語のデータをインデックスするためには、CJKAnalyzerかJapaneseAnalyzerを使う。CJKAnalyzerは[bi-gram方式である](https://ja.wikipedia.org/wiki/全文検索#N-Gram "wikilink")。JapaneseAnalyzerを使うには[形態素解析](../Page/形態素解析.md "wikilink")エンジンを組み込む必要があり、2014年現在ではオープンソースの[Sen](https://ja.wikipedia.org/wiki/Sen "wikilink")([MeCab](../Page/MeCab.md "wikilink")のJava実装)ベースの「lucene-gosen」、同じくオープンソースのKuromojiベースの2種類の実装がある。また、 2007年1月に[Apacheのトップレベルプロジェクトになり](../Page/Apacheソフトウェア財団.md "wikilink")、現在はPMC (Project Management Committee) での開発スタイルをとっている。

## 書籍

  - Apache Lucene 入門 \~Java・オープンソース・全文検索システムの構築 - ISBN 4-7741-2780-9
  - Lucene In Action - ISBN 1-932394-28-1

## 脚注

## 外部リンク

  - [Lucene(本家)](http://lucene.apache.org/)
  - [Lucene-ja(日本語ローカライズ版)](https://sen.dev.java.net/servlets/ProjectDocumentList?folderID=755&expandFolder=755&folderID=0)
  - [Lucene(Wiki)](http://wiki.apache.org/jakarta-lucene/)
  - [Lucene(開発者)](http://lucene.apache.org/who.html)
  - [関口宏司のLuceneブログ](http://lucene.jugem.jp/)
  - [インデックス型全文検索ツール：Search++](http://www.searchplusplus.jp/)
  - [分散インデックス型 全文検索ソフト： Pokuda Search Pro](http://pokuda-tyoubun.blogspot.com/p/pokuda-search-pro.html)

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:全文検索](https://ja.wikipedia.org/wiki/Category:全文検索 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [what is elasticsearch?](http://www.elasticsearch.org/overview/elasticsearch) - elastic search