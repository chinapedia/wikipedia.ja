> この記事は[Seasar](https://ja.wikipedia.org/wiki/Seasar)から翻訳されています。


The **Seasar** Projectは、日本の[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトの1つ。当初、比嘉康雄を中心とするメンバーによるSeasar2(正確にはS2Container)と呼ばれる[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のための[DI (Dependency Injection)](https://ja.wikipedia.org/wiki/依存性の注入 "wikilink") と[AOP (Aspect Oriented Programming)](../Page/アスペクト指向プログラミング.md "wikilink") をサポートした軽量コンテナの開発を進めるプロジェクトであったが、現在は特定非営利法人[Seasarファウンデーション](https://ja.wikipedia.org/wiki/Seasarファウンデーション "wikilink")の元、The Seasar ProjectというS2Containerを中心としたコミュニティを形成し、Java、PHP、.NETなど多種多様な言語のためのオープンソースプロジェクトと発展している。なお、一般にSeasarおよびSeasar2と表記した場合、S2Containerを指すことが多い。

## 歴史

Seasarは、初め2003年8月にJettyと[HSQLDB](https://ja.wikipedia.org/wiki/HSQLDB "wikilink")を使ったアプリケーションサーバとして、SourceForge.jp上で公開された。 その名前は、比嘉氏の出身地である沖縄の象徴的な生き物である[シーサー](https://ja.wikipedia.org/wiki/シーサー "wikilink")に因んで名付けられた。

2004年3月、SeasarはSeasar2と名を変えて、DI・AOPコンテナとして再公開された。しかし、Seasarの開発は停止する(最終版は、Seasar2のサイトからまだダウンロードできる)。2005年4月、Seasar2はOSCJ.netの支援を受けて、SourceForge.jpから移動する。

2016年9月26日、Seasarプロジェクトが提供するプロダクトの多くはEOL(End of Life)となる。 例外については外部リンクのSeasar project を参照のこと。

## 概要

その他のDIコンテナと同じように、コンポーネントは、外部XMLファイルに定義する。データーベースの設定や、[JUnit](https://ja.wikipedia.org/wiki/JUnit "wikilink")によるユニットテストの支援についても同様に定義する。

その他のフレームワークとの主な違いは、「設定よりも規約」という概念のサポートである。それは、[Spring Framework等で必要なXMLによる設定の減少である](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")。 開発者にフレームワークを動作させるための規約に従わせ、設定ファイルを減らすか除去することを目的とする。

例えばもし、プロパティの型が、ただ一つの実装を持つインターフェースならば、依存関係はコンテナによって自動的に設定される。 もし、テストクラスのメソッドの末尾が、"Tx"ならば、トランザクションは、テスト実行前に初期化され、テスト終了後にロールバックされる。

## 外部リンク

  - [The Seasar Project](http://www.seasar.org/)
  - [特定非営利活動法人Seasarファウンデーション](http://www.seasarfoundation.org/)

[Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink")