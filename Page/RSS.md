> この記事は[RSS](https://ja.wikipedia.org/wiki/RSS)から翻訳されています。


**RSS**（バージョンによってRich Site Summary, [RDF](../Page/Resource_Description_Framework.md "wikilink") Site Summary, Really Simple Syndication）は、[ニュース](../Page/ニュース.md "wikilink")や[ブログ](../Page/ブログ.md "wikilink")など各種の[ウェブサイト](../Page/ウェブサイト.md "wikilink")の更新情報を配信するための文書[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")の総称である。

## 概要

RSSには、歴史的経緯によりそれぞれ記述方法や用途が異なる2つの規格が存在している。

[ブログ](../Page/ブログ.md "wikilink")での更新情報の配信として用いられている場合が大半を占めているが、ニュース配信サイトでは最新ニュースを、放送局では番組情報を、その他各種企業においてプレスリリースや新製品情報、サポート情報を、RSSを使ったヘッドライン情報として配信する事例も増えている。また、[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")[データ](../Page/データ.md "wikilink")[ファイルを公開するための方法である](../Page/ファイル_\(コンピュータ\).md "wikilink")[ポッドキャスティング](https://ja.wikipedia.org/wiki/ポッドキャスティング "wikilink")にも使われている。

また、RSSに対応しているウェブサイトではRSSに対応していることを明確にするために下記のような表示が使われていることが多い。

  - [16px](https://ja.wikipedia.org/wiki/ファイル:Feed-icon.svg "wikilink")
  - [ファイル:RSS_icon.svg](https://ja.wikipedia.org/wiki/ファイル:RSS_icon.svg "wikilink")
  - [ファイル:XML_icon.svg](https://ja.wikipedia.org/wiki/ファイル:XML_icon.svg "wikilink")

## RSSフォーマットの歴史と変遷

RSSはRDFの採用をめぐって現在分裂状態にあり、1.0と2.0の2つの系列に分かれている。当初、0.9はRDFをベースにしたデータ形式を利用していたが、0.91ではシンプル化するためにRDFを利用しなくなった。その後、1.0では0.9の系列を引継ぎ、複雑なRDFを採用することで応用性の高いデータを利用できるようにした。これに対して、2.0は0.91を引継ぎ、コンテンツ配信に特化することで複雑なRDFを排除している。

### RSS 0.9

最初のRSSであるRSS 0.9は、として、[1999年](../Page/1999年.md "wikilink")3月に米国[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")が自社の[ポータルサイト](../Page/ポータルサイト.md "wikilink")「」において、「チャンネル」の詳細を記すために策定したものである。RDF構文を用いたことから、と呼ばれる。

その後ネットスケープコミュニケーションズはRDF構文の利用を止め、独自の[XMLフォーマットを用いて要素を拡張し](../Page/Extensible_Markup_Language.md "wikilink")、よりリッチな情報を提供できるようにしたRSS 0.91を開発した。

### RSS 0.91

と改名されたRSS 0.91は、RSS 0.9に要素を拡張する目的で作られ、1999年7月にこのバージョンがリリースされた。RDFを用いず、独自の[XMLで記述される](../Page/Extensible_Markup_Language.md "wikilink")。

ユーザーランド・ソフトウェア社（）の「スクリプティングニュース」（）から[著作権](../Page/著作権.md "wikilink")、日付情報などいくつかの要素を取り入れ拡張された。それまでのRSS 0.9より多くの情報を配信できるようになったため、と呼ばれ、その後派生したRSS 0.92、RSS 2.0のベースとなっている。

### Netscape社の撤退

RSS 0.91のリリース後、8年間にわたってNetscape社はRSSの開発から撤退してしまう。新しくオーナーになった[AOL](../Page/AOL.md "wikilink")社による会社再編の中で、Netscape社は2001年4月にMy.Netscape.ComでRSSサポートを終了し、RSSのドキュメントや支援ツール類も削除してしまった\[1\]。

RSS 0.91の登場以降、RSSが持つ「[コンテンツ](../Page/コンテンツ.md "wikilink")配信」機能に対しての需要がさらに高まっていた。そのときにNetscape社が撤退して空白が生じてしまった。この後、よりリッチなコンテンツ配信を目指そうとする制作者たちが、独自の要素をRSSに追加してしまうなど、フォーマットの拡張における混乱がおこることとなった。

この「空白」を埋めようと、二つのグループが立ち上がってきた。いずれのグループもNetscape社の助力や承認は得ていない。一つは[RSS-DEV Working Groupのグループであり](https://ja.wikipedia.org/wiki/RSS-DEV_Working_Group "wikilink")、もう一つは[Dave Winerと](https://ja.wikipedia.org/wiki/Dave_Winer "wikilink")[UserLand Software社のグループである](https://ja.wikipedia.org/wiki/UserLand_Software "wikilink")。UserLand Software社はNetscape社外で作られたものとしては最初のものとなる、RSSの読み書きが可能な出版ツールを公開した。

### RSS 1.0の系統

こうした混乱のなかで、RSSでよく使われる語彙や使われる要素群を「コア」として定義し、それ以外は拡張する側が独自の語彙を「モジュール」として定義することで、中核語彙と拡張性を保証させようとする提案が RSS-DEV ワーキンググループ内で起こり、その成果として[2000年](../Page/2000年.md "wikilink")12月にRSS 1.0がリリースされた。

RSS 1.0は0.9時代に用いられていたRDFを再び採用し、RSSが持つ「[メタデータ](../Page/メタデータ.md "wikilink")記述」としての側面を主眼に置いたフォーマットとなっている。

また、RSSコアモジュールの他に公式なモジュールとして、 モジュール、 モジュール及び  モジュールが定められた。これにより RSS 0.9の不満であった語彙の乏しさを解消させ、またコンテンツ配信手段としてRSS 1.0を採用する道を残すものとなった。

RSS 1.0 の登場は、（メタデータ記述技術としての）RSSの中核語彙及び拡張性を保証するものとなった。しかしRDFを再び採用したこと、モジュールによるXML名前空間の複雑化はすべてのRSS配信者を満足させず、RSS 0.91 系のフォーマットを拡張する動きが再びみられることとなった。

### RSS 0.92 から RSS 2.0 の系統

RSS 1.0の取る道は必ずしも誰もが好むものではなかった、とはいえRSS 0.91以降に起きていたフォーマット拡張の混乱は避ける必要があった。そのため拡張をオプションとして提供し、かつRSS 0.91への互換性を持たせる方法が提案され、それを受けて2000年12月にユーザーランド・ソフトウェア社からRSS 0.92が発表された。

ユーザーランド・ソフトウェア社はその後も互換性を維持したままRSS 0.93、RSS 0.94の素案を公表したが、その後撤回し、[2002年](../Page/2002年.md "wikilink")8月にRSS 0.91 からRSS 0.94までのすべてのフォーマットに対する互換性を保証したRSS 2.0を策定し、これをと名付けた。

RSS 2.0はあくまで0.9x系の流れを汲む規格であって、RSS 1.0の後継ではない。それぞれの目指す方向性は同じではないため、場面に応じて使い分けられている。

[2003年](../Page/2003年.md "wikilink")7月に、RSS 2.0制定の中心人物、[デイヴ・ウィナー](https://ja.wikipedia.org/wiki/デイヴ・ウィナー "wikilink")（）の移籍と併せ、仕様も[ハーヴァード大学](https://ja.wikipedia.org/wiki/ハーヴァード大学 "wikilink")ロースクールのバークマンセンターに移管された。

### Atom

WinerとRSS-DEV Working GroupのいずれもNetscapeの関与を受けていないため、両者ともにRSSの名前や形式について、公的な正統性を主張できなかった。これが配信開発コミュニティで現在でも尾を引いている、「RSS」の管理元としてどちらが適切なのかという論争の元となってきた。

この論争の副産物ともいえるのが、2003年7月から開発が始まった新しい配信形式[Atomである](../Page/Atom_\(ウェブコンテンツ配信\).md "wikilink")\[2\] 。Atom配信形式の開発の動機の一つは、RSSを取り巻く問題から離れて、しがらみのない所で始めたいという動機もあった。Atomは[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink")の提案標準として採択された。

## 利用

RSSの取得・講読には**RSSリーダー**（[フィードリーダー](../Page/フィードリーダー.md "wikilink")とも）と呼ばれるソフトウェアを使う。また、RSSを作成・追加するためのソフトウェアもあるが、比較的シンプルなXML形式なので手作業でも可能である。

## 衰退

RSS 1.0 と RSS 2.0 の関係について、バージョンを表す数値の大小関係から、前者が旧規格で後者が後継規格であるという誤解が見受けられるが、これは事実ではない。RSS 2.0 はシンプルさの代償として RSS 1.0 の備える（RDFによる）強力な表現力を放棄したため、RSS 1.0 を置き換えるものではない。

一方、RSS 2.0 に代わるコンテンツ配信技術として、IBMのサム・ルビー () などが中心となり、 と呼ばれる新しい規格が策定された。 にはウェブログ・ツールの開発元の社やスタンフォード大学法学部の[ローレンス・レッシグ](../Page/ローレンス・レッシグ.md "wikilink")教授、XML開発者のティム・ブレイ () などが支持を表明し、また[Google](../Page/Google.md "wikilink")も自社のサービスにて、メールの内容をフィードで提供するサービスを行った。

その後、RSS 1.0、RSS 2.0 そして  は、いずれにも集約されることなく各々が広く普及していた。RSSリーダーの多くはそれら全てに対応しており、一方のウェブサイト側も、フィード配信のためにそれらのうち複数を利用することも珍しくなかった。しかし、[SNSや](../Page/ソーシャル・ネットワーキング・サービス.md "wikilink")[キュレーションアプリの普及に伴い](../Page/まとめサイト.md "wikilink")、RSS的な技術そのものの需要が減少していき、[2013年](../Page/2013年.md "wikilink")には[Googleリーダー](https://ja.wikipedia.org/wiki/Googleリーダー "wikilink")が\[3\]、[2017年](../Page/2017年.md "wikilink")には[Live Dwango Readerがいずれも利用者数減少を理由にサービスを終了](../Page/Live_Dwango_Reader.md "wikilink")\[4\]、次いで[2018年](../Page/2018年.md "wikilink")には主要ブラウザである[Mozilla FirefoxもRSS](../Page/Mozilla_Firefox.md "wikilink")/Atomのサポートを廃止した\[5\]。

## 図書館におけるRSS

情報を扱う専門機関としての図書館においてもRSSの活用サービス例は増えている。お知らせの配信などはもっとも活用されている例である。京都大学図書館機構などでは、学生や研究者向けにRSSについての概要や活用方法などをまとめている。また、農林水産研究情報センターでは、新着雑誌、新着図書情報などもRSSによって配信している。

## 参考文献

  - 水野貴明『詳解RSS～RSSを利用したサービスの理論と実践』、ディー・アート、[2005年](../Page/2005年.md "wikilink") ISBN 4-88648-746-7

## 脚注

### 注釈

### 出典

## 関連項目

  - [セマンティックウェブ](https://ja.wikipedia.org/wiki/セマンティックウェブ "wikilink")
  - [Resource Description Framework](../Page/Resource_Description_Framework.md "wikilink") (RDF)
  - [フィード](../Page/フィード.md "wikilink")
  - [Atom (ウェブコンテンツ配信)](../Page/Atom_\(ウェブコンテンツ配信\).md "wikilink")
  - [フィードリーダー](../Page/フィードリーダー.md "wikilink")
  - [RSS作成ツール](https://ja.wikipedia.org/wiki/RSS作成ツール "wikilink")

## 外部リンク

  - [RSS -- サイト情報の要約と公開](https://www.kanzaki.com/docs/sw/rss.html) - [The Web KANZAKI](https://www.kanzaki.com/)によるRSS 1.0の解説
  - [RSS 1.0仕様](http://web.resource.org/rss/1.0/) / [1](http://www.net.intap.or.jp/INTAP/s-web/data/TR/1-1.html)（和訳）
  - [RSS 0.92仕様](http://backend.userland.com/rss092)
  - [RSS 2.0仕様](http://www.rssboard.org/rss-specification)
  - \[ ウィキペディア日本語版の「最近更新されたページ」のRSS\]
  - [Feed Icons](http://www.feedicons.com/) - 標準フィードアイコン
  - [フィードアイコンガイドライン](https://www.mozilla.org/ja/foundation/feed-icon-guidelines/) - Mozillaによる、標準フィードアイコンの使用に関する推奨ガイドライン

[Category:RSS](https://ja.wikipedia.org/wiki/Category:RSS "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:メタデータ](https://ja.wikipedia.org/wiki/Category:メタデータ "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.
2.
3.
4.
5.