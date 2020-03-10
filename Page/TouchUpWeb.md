> この記事は[TouchUpWeb](https://ja.wikipedia.org/wiki/TouchUpWeb)から翻訳されています。


**TouchUpWeb**(タッチアップウェブ)とは、[IPAの](../Page/情報処理推進機構.md "wikilink")[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")度下期[オープンソースソフトウェア活用基盤整備事業](https://ja.wikipedia.org/wiki/オープンソースソフトウェア活用基盤整備事業 "wikilink")に採択され、開発されたソフトウェア自体、あるいはそのプロジェクトのこと。2009年4月7日にサービスを終了した。

[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") 1.5以降で利用できる[拡張機能である](../Page/拡張機能_\(Mozilla\).md "wikilink")。この拡張機能を使えば、Mozilla Firefoxで閲覧が不可能であった[ウェブサイト](../Page/ウェブサイト.md "wikilink")をMozilla Firefoxで問題なく閲覧することができるようになる。ただし、それぞれのウェブサイト用に作成されたスクリプトを用いるという仕組みであるため、あらゆるウェブサイトに対する対策とはならない。

ソフトウェアの構成は、Mozilla Firefoxにインストールされた拡張機能がサーバに修正のためのスクリプトを取得しにいくようになっている。なお、それぞれのソフトウェアは[MPL](../Page/Mozilla_Public_License.md "wikilink") 1.1にて提供されている[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアである。

## 開発の背景

学校へのLinux導入実験や自治体に対するアンケート結果などでは、[Microsoft Internet Explorerでしか閲覧できないウェブサイトが](https://ja.wikipedia.org/wiki/Microsoft_Internet_Explorer "wikilink")、オープンソース環境の導入障壁の一つとして挙げられている。この障壁へのアプローチとして、[ウェブスタンダードプロジェクト](https://ja.wikipedia.org/wiki/ウェブスタンダードプロジェクト "wikilink")や[もじら組](../Page/もじら組.md "wikilink")が推進している[ウェブ標準](https://ja.wikipedia.org/wiki/ウェブ標準 "wikilink")への啓蒙活動がある。しかし、啓蒙活動だけでは短期間でその障壁を無くすことは非常に困難である。そのため、TouchUpWebプロジェクトでは、既存のウェブサイトに対して動的にスクリプトを適用し、閲覧状況を改善するという[対症療法](https://ja.wikipedia.org/wiki/対症療法 "wikilink")的アプローチを採用した。「[\#プロジェクトへの非難](https://ja.wikipedia.org/wiki/#プロジェクトへの非難 "wikilink")」セクションに後述するように、このようなアプローチに対する非難も存在する。

## ソフトウェアの構成

TouchUpWebソフトウェアは、[Mozilla Firefox用](../Page/Mozilla_Firefox.md "wikilink")[拡張機能](https://ja.wikipedia.org/wiki/拡張機能 "wikilink")とサーバソフトウェアによって構成される。

### TouchUpWeb機能拡張

Mozilla Firefox 1.5以降に対応した拡張機能。別途インストールする[Greasemonkey](https://ja.wikipedia.org/wiki/Greasemonkey "wikilink")という拡張機能連携して、ウェブサイト閲覧状況を改善する機能を有する。以下のような機能を持つ。

  - サイトに適用可能なスクリプトを検索し、ダウンロードする機能
  - スクリプト情報の表示機能
  - 適用状況のフィードバック機能

なお、ユーザ操作でのみ、サーバとの通信が行われる。

### TouchUpWebサーバ

[Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink") 5.5上で動作するWebアプリケーション。管理システムとWebサービス機能から構成される。

  - スクリプト管理機能
  - 配信履歴検索機能
  - スクリプト配信機能
  - ユーザサイトにスレーブサーバを構成し、マスターサーバから定期的に情報を受け取る機能
  - イントラネット用構成が可能

## プロジェクトへの批判

このソフトウェアが有効な場合は、主に[Microsoft Internet Explorerでしか閲覧できないウェブサイトを閲覧するときである](https://ja.wikipedia.org/wiki/Microsoft_Internet_Explorer "wikilink")。このため、「ウェブ標準に準拠しないウェブサイトの作成を増進させる可能性がある」という非難もある。

## 脚注

<references/>

## 外部リンク

### プロジェクト関連公式サイト

  -
  - [TouchUpWeb Bugzilla](http://bugzilla.touchupweb.org)

  - [TouchUpWebプロジェクト(SourceForge.net)](https://sourceforge.net/projects/touchupweb)

  - [PickUpWeb(非Firefoxユーザ用サービス)](http://intranet.touchupweb.org/TouchUpWeb/services/pickupweb.tuw)

### 関連記事

  - [CodeZine「不完全なHTMLを動的にタッチアップ」](https://codezine.jp/article/detail/534)
  - [CodeZine「Firefox拡張機能の基礎を実例で学ぶ」](https://codezine.jp/article/detail/679)
  - [スラッシュドットジャパン「特定ブラウザ依存性への挑戦『TouchUpWeb』プロジェクト」](https://srad.jp/story/06/09/14/0253254/)

[Category:Mozilla_Firefox](https://ja.wikipedia.org/wiki/Category:Mozilla_Firefox "wikilink") [Category:拡張機能_(Mozilla)](https://ja.wikipedia.org/wiki/Category:拡張機能_\(Mozilla\) "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ウェブアクセシビリティ](https://ja.wikipedia.org/wiki/Category:ウェブアクセシビリティ "wikilink")