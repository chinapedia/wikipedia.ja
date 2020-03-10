> この記事は[Magento](https://ja.wikipedia.org/wiki/Magento)から翻訳されています。


**Magento**（マジェント）は、[PHP](https://ja.wikipedia.org/wiki/PHP "wikilink")で書かれた[電子商取引を構成するための](https://ja.wikipedia.org/wiki/Eコマース "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[プラットフォームであり](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、世界で最も著名な電子商取引システムのうちの一つである。

[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")のExperience Cloudのラインナップに統合されている。

無償のオープンソース版と有償のMagento Commerce、Magento Commerce Cloudがあり、Magento Commerceは[オンプレミス](https://ja.wikipedia.org/wiki/オンプレミス "wikilink")型で提供され、Magento Commerce Cloudは[SaaS](../Page/SaaS.md "wikilink")型の[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")システムとして提供される。

100,000以上の電子商取引サイトで利用されており、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")数としては250万回を超え、2019年の中でMagentoを使用して総額115億ドル（の取引が行われている。2017年までは世界の電子商取引サイト総数の中で30%のシェアを獲得していた。

2015年11月17日にMagento2.0がリリースされ、テーブルロックの問題の解消、ページキャッシングの向上、エンタープライズ領域のサイトに対する[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")の強化、[構造化データの対応](https://ja.wikipedia.org/wiki/Google_検索#リッチスニペット "wikilink")、ファイル構造を整理することによるカスタマイズ性の向上、[LESS](https://ja.wikipedia.org/wiki/LESS "wikilink")を[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")とする[CSS](../Page/CSS.md "wikilink")、パフォーマンスの向上といった変更が加えられた。

[RDBMSには](../Page/関係データベース管理システム.md "wikilink")[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")または[MariaDB](https://ja.wikipedia.org/wiki/MariaDB "wikilink")が採用され、[プログラミング言語](../Page/プログラミング言語.md "wikilink")としてはPHP、そして一部[Zend frameworkが使用されている](https://ja.wikipedia.org/wiki/Zend_Framework "wikilink")。これは[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")型プログラミングと[MVCが採用されていることが伺える](../Page/Model_View_Controller.md "wikilink")。EAV（Entry Attribute Value）と呼ばれるデータモデルが採用されている。フロントエンドには[JavaScript](../Page/JavaScript.md "wikilink")ライブラリのうちの1つつである[KnockoutJSが採用されている](https://ja.wikipedia.org/wiki/Knockout.js "wikilink")。

Magento 2.3.3\[1\]のバージョンには、よりモバイル機器での操作性向上を実現するPWA Studio 4.0.0や[GraphQL](https://ja.wikipedia.org/wiki/GraphQL "wikilink")の対応が追加され、[ヘッドレスアーキテクチャ（デカップルドアーキテクチャ）実現のための対応が強化されている](https://ja.wikipedia.org/wiki/:en:Headless_content_management_system "wikilink")。

## 特徴

  - ウェブサイト、ストア、ストアビューという3層構造の構成が可能であり、1つのMagentoにおいて、複数のウェブサイト・ストア・ストアビューの構成が可能である。
  - ストアビューごとに言語指定することで、多言語の切り替え表示が可能である。これが多言語対応と称される。
  - ウェブサイト単位で標準の通貨を指定し、決済通貨及び商品価格通貨として利用される。標準通貨から換算した他の通貨を表示する切り替えが可能であり、これが多通貨対応と称される。
  - 多くの[サードパーティ](https://ja.wikipedia.org/wiki/サードパーティ "wikilink")ー製の拡張プログラムに当たるエクステンションや、電子商取引向けサービスが提供されている。
  - 画面デザインを構成するテーマが[Themeforest](https://themeforest.net/category/ecommerce/magento)などにより多く公開されている。
  - 大量の商品データを高速処理するためのデータモデルの採用や、大量のアクセスに対応するための[Redis](https://ja.wikipedia.org/wiki/Redis "wikilink")や[Varnish Cacheと言ったミドルウェアに標準対応している](https://ja.wikipedia.org/wiki/Varnish_Cache "wikilink")。
  - [PCIデータセキュリティスタンダード](../Page/PCIデータセキュリティスタンダード.md "wikilink")認証のレベル1を取得している\[2\]。

## 歴史

[2007年](../Page/2007年.md "wikilink")に開発が開始され、7ヶ月後の2007年8月31日にはじめのベータバージョンがリリースされる。当初[osCommerceからフォークされたコードで作られていたが](https://ja.wikipedia.org/wiki/:en:osCommerce "wikilink")、後に全て書き換えられる。

Best of Open Source Software Awardsと[SourceForge](../Page/SourceForge.net.md "wikilink") Community Choice Awards\[3\]に表彰される。

[2011年](../Page/2011年.md "wikilink")2月、[eBay](https://ja.wikipedia.org/wiki/eBay "wikilink")が2010年にMagentoの会社のうち49%のシェアを獲得したと発表する。2011年6月にeBayはMagentoの残りのシェアを買収し、X.Commerceイニシアチブに参加すると発表。MagentoのCEOおよび共同設立者であるRoy Rubinは、Magentoのブログで「マジェントは引き続きロサンゼルスから事業を展開し、Yoav Kutnerと私をリーダーとして運営していく。」と書いている。

[2012年](../Page/2012年.md "wikilink")4月にYoav Kutnerが去る。

[2015年](../Page/2015年.md "wikilink")11月3日Magentoは[Permira](https://ja.wikipedia.org/wiki/:en:Permira "wikilink") private eauityの出資を得てeBayから独立し、独立企業となる。

[2018年](../Page/2018年.md "wikilink")16.8億ドルでアドビシステムズに買収\[4\]され、Experience Cloudに統合されると発表され、2018年11月19日に買収が完了される。

## 脚注

## 関連項目

  - [アドビシステムズ](../Page/アドビシステムズ.md "wikilink")
  - [電子商取引](../Page/電子商取引.md "wikilink")
  - [ECサイト](https://ja.wikipedia.org/wiki/ECサイト "wikilink")
  - [コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")
  - [越境EC](https://ja.wikipedia.org/wiki/越境EC "wikilink")

## 外部リンク

  - [Magento公式サイト](https://magento.com/)
  - [Adobe Commerce Cloud](https://www.adobe.com/jp/commerce/magento.html)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:電子商取引](https://ja.wikipedia.org/wiki/Category:電子商取引 "wikilink") [Category:電子商取引サイト](https://ja.wikipedia.org/wiki/Category:電子商取引サイト "wikilink") [Category:アドビシステムズ](https://ja.wikipedia.org/wiki/Category:アドビシステムズ "wikilink") [Category:アメリカ合衆国のソフトウェア会社](https://ja.wikipedia.org/wiki/Category:アメリカ合衆国のソフトウェア会社 "wikilink") [Category:eBay](https://ja.wikipedia.org/wiki/Category:eBay "wikilink") [Category:ウェブサイトの構成](https://ja.wikipedia.org/wiki/Category:ウェブサイトの構成 "wikilink") [Category:Webオーサリングソフト](https://ja.wikipedia.org/wiki/Category:Webオーサリングソフト "wikilink") [Category:アプリケーションソフト](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト "wikilink")

1.  [Magento Open Source 2.3.3 Release Notes 2019/10/8](https://devdocs.magento.com/guides/v2.3/release-notes/release-notes-2-3-3-open-source.html)
2.  [MAGENTO'S APPROACH TO PCI COMPLIANCE](https://magento.com/pci-compliance)
3.  [The Community Choice Awards Winners 2018/06/25](https://sourceforge.net/blog/the-community-choice-awards-winners/)
4.  [アドビ、Magento Commerceを買収 2018/05/22](https://www.adobe.com/jp/news-room/news/201805/20180522-magento-commerce.html)