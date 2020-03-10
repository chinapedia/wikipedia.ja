> この記事は[Interstage Shunsaku Data Manager](https://ja.wikipedia.org/wiki/Interstage_Shunsaku_Data_Manager)から翻訳されています。


**Interstage Shunsaku Data Manager**とは、[富士通](../Page/富士通.md "wikilink")の[ネイティブXMLデータベース](https://ja.wikipedia.org/wiki/ネイティブXMLデータベース "wikilink")製品。同社の[Interstage](../Page/Interstage.md "wikilink")シリーズの中のIntegration系製品に相当する。2005年12月現在の最新のバージョンはV7。以下の説明ではとくに注記のない限りV7製品について記述する。

## 概要

Shunsakuの特徴としてインデックスレスであるためインデックスの再作成などの手間がかからないことがある。またハードウェアの増設や縮退などでデータベースをとめる時も、数十秒程度の時間で済ませられるようにしてある。

現代的なDBとしてトランザクション制御、障害直前までのリカバリ機能を備えている。

### 構成

Shunsakuはディレクタサーバ、サーチサーバの二階層の構造になっており、ディレクタサーバが検索要求を管理し、一般に複数設置するサーチサーバが実際の検索を行うことで、管理の容易さと信頼性やスケーラビリティを可能にする工夫を行っている。運用中にサーチサーバがハードウェア障害などで停止した場合でも、自動縮退によって運用が継続されるようになっているのである。また、サーチサーバの増設もデータを自動的に再配置するので容易に行うことができる。

ディレクタサーバには[Solaris](../Page/Solaris.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、サーチサーバにはLinuxおよびWindows版が存在する。ディレクタサーバとサーチサーバのOSはあわせる必要がある。（Solarisディレクタサーバの場合はサーチサーバにはLinuxを利用する）

### 検索性能

Shunsakuは[九州大学](../Page/九州大学.md "wikilink")の[有川節夫](https://ja.wikipedia.org/wiki/有川節夫 "wikilink")教授らが開発したSIGMA検索アルゴリズムを採用している。SIGMAは複数の検索条件のもとで一定の検索スピードを達成するためのアルゴリズムである。また、SIGMAはインデックスを不要にするため、Shunsakuもインデックスレスになっている。

SIGMA検索アルゴリズムにより、複数の検索要求を複数条件の一個の検索に統合し結果を別々に返すということが可能になっている。これによりトラフィックの負荷が高くなった場合でも、一定の検索速度が期待できる。

### 他DBとの連携

Shunsakuは入力データとXMLとの対応を定義したマッピングデータを用意することで、他データベースや[CSV形式のデータを](../Page/Comma-Separated_Values.md "wikilink")[XML形式のデータに変換して格納することができる](../Page/Extensible_Markup_Language.md "wikilink")。対応データベースは[Symfoware Server](https://ja.wikipedia.org/wiki/Symfoware_Server "wikilink")、[PowerGRES Plus](https://ja.wikipedia.org/wiki/PowerGRES_Plus "wikilink")、[Oracle Database](../Page/Oracle_Database.md "wikilink")、[Microsoft SQL Serverなどが利用できる](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")。

同じ富士通製品であるSymfoware Serverとは特に連携性が良く、SymfowareのレベルがEnterprise Edition以上ならコマンド一行でShunsakuに適したXML形式でデータ抽出を行うことができる。

## 関連項目

  - [山手線方式](https://ja.wikipedia.org/wiki/山手線方式 "wikilink")

## 外部リンク

  - [Interstage Shunsaku Data Manager（富士通）](http://interstage.fujitsu.com/jp/shunsaku/)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:XML](https://ja.wikipedia.org/wiki/Category:XML "wikilink")