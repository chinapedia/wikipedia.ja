> この記事は[Firebird](https://ja.wikipedia.org/wiki/Firebird)から翻訳されています。


**Firebird**（**ファイアバード**）は、[InterBase](https://ja.wikipedia.org/wiki/InterBase "wikilink")から派生した[オープンソース](../Page/オープンソース.md "wikilink")の[関係データベース管理システム](https://ja.wikipedia.org/wiki/関係データベース管理システム "wikilink") (RDBMS)。[オープンソース](../Page/オープンソース.md "wikilink")で開発されており、[Mozilla Public Licenseを元にしたIPL](https://ja.wikipedia.org/wiki/Mozilla_Public_License "wikilink")([InterBase Public License](https://ja.wikipedia.org/wiki/InterBase_Public_License "wikilink"))と IDPL ([Initial Developer's Public License](https://ja.wikipedia.org/wiki/Initial_Developer's_Public_License "wikilink"))（商用・非商用問わず利用できるが、オリジナル〈ここではFirebirdを指す〉のソースコードを改変したプログラムを利用する場合は、その変更箇所のコードを公開しなくてはならない）によってライセンスされている。

## 特徴

[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")の[MVCC](https://ja.wikipedia.org/wiki/MVCC "wikilink")（多版同時実行制御）と同様の[MGA](https://ja.wikipedia.org/wiki/InterBase#マルチ・ジェネレーション・アーキテクチャー "wikilink")（マルチ・ジェネレーション・アーキテクチャー）による高度なトランザクション管理機能を有する。[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")や、[トリガー](https://ja.wikipedia.org/wiki/トリガー "wikilink")、UDF（[ユーザー定義関数](https://ja.wikipedia.org/wiki/ユーザー定義関数 "wikilink")）等の商用データベースに通常備わっている機能を網羅している。ただしオブジェクトの命名則が厳しい、プライマリキーのAUTO INCREMENTが用意されていないなど、やや旧式な仕様もある。なお[PHPなどアプリケーションからの接続には](../Page/PHP_\(プログラミング言語\).md "wikilink")、InterBase対応の関数・ライブラリを流用できる。

2007年6月に開催された「[オープンソースカンファレンス](https://ja.wikipedia.org/wiki/オープンソースカンファレンス "wikilink")2007.DB」で行われた公開ベンチマークテストでは高評価を得ているが\[1\]、解説書籍の出版が少ない、[レンタルサーバではサポートされていないなど日本国内での認知度はまだまだ低い](https://ja.wikipedia.org/wiki/ホスティングサーバ "wikilink")。

特筆すべき機能として、有償ではあるが米IBフェニックス社の「IBPレプリケータ」を導入し、[GUI上から設定することにより](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")、[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")で接続された複数のFirebird同士で同期処理を行なうことが可能となる。これはトリガーの機能を応用したもので、更新された箇所を同期処理用のテーブルに蓄積し、蓄積内容を設定された別のFirebirdに対し定期的に送信すると言うものである。この他にも、Firebirdのレプリケーションソフトは多数存在する。

また、RDBMS側からクライアントへのコールバックを実現する、イベントアラータはFirebirdの初期開発者である[Jim Starkeyの発案によるものである](https://ja.wikipedia.org/wiki/Jim_Starkey "wikilink")。

Firebirdは一般的なC/S(Client Server)のデータベースとしての利用のほか、データベースライブラリとしても利用でき、生成されるデータベースファイルも一つのOSファイルであるため、アプリケーションへの組み込みが容易である。組み込んだ例としてはLibreOffice Baseの4.2以降でFirebird Embeddedが利用できる。

## インストール

[Windows版には専用のインストーラが用意されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")版もダウンロードパッケージに含まれる「install.sh」を実行すれば自動的に「/opt」以下にインストールされる。ただしisqlコマンドを使う場合、実行環境（Fedoraなど）によっては同名の全く別のプログラムが起動してしまうので、「isql2」など重複しない別名のシンボリックリンクを作成しておく必要がある。

## 歴史

2000年6月25日、[ボーランド](https://ja.wikipedia.org/wiki/ボーランド "wikilink")から [InterBase](https://ja.wikipedia.org/wiki/InterBase "wikilink") 6.0のソースコードが公開され\[2\]\[3\]、それから1週間のうちに[SourceForgeにFirebirdプロジェクトが登録された](https://ja.wikipedia.org/wiki/ソースフォージ "wikilink")\[4\]\[5\]。

2002年3月11日、Firebird 1.0が Linux、Windows、[Mac OS X向けにリリースされた](https://ja.wikipedia.org/wiki/macOS "wikilink")\[6\]。それから2ヵ月後には、[Solaris](../Page/Solaris.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink") 4、[HP-UX](https://ja.wikipedia.org/wiki/HP-UX "wikilink")へも移植された\[7\]。

[Mozilla Foundationの新ブラウザが登場した際](../Page/Mozilla_Foundation.md "wikilink")、一時期 "Mozilla Firebird" の名称を使用したため多少の混乱があったが、2004年2月10日にmozilla.orgがブラウザの名称を[Mozilla Firefoxに変更したことで決着した](https://ja.wikipedia.org/wiki/Mozilla_Firefox "wikilink")。[1](http://www.mozilla-japan.org/projects/firefox/firefox-name-faq.html)

2004年2月23日、Firebird 1.5がリリースされた\[8\]。ポーティングのため2000年よりソースコードを[C言語](../Page/C言語.md "wikilink")から[C++](../Page/C++.md "wikilink")へ変更する開発が行われてきたが、このリリースは初めてC++コードベースを使った安定版である。[クエリ最適化](https://ja.wikipedia.org/wiki/クエリ最適化 "wikilink")の改良、[SQL](https://ja.wikipedia.org/wiki/SQL "wikilink")92準拠の式、[SQL:1999](https://ja.wikipedia.org/wiki/SQL:1999 "wikilink")準拠の[SAVEPOINT](https://ja.wikipedia.org/wiki/SAVEPOINT_\(SQL\) "wikilink")、明示的なロックが追加された\[9\]。

2006年11月12日、Firebird 2.0がリリースされた\[10\]。[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")アーキテクチャのサポート、FROM句での入れ子テーブル、ロック時のタイムアウトでの式の利用が追加された\[11\]。さらに、バージョン 2.1にて、[データベーストリガ](https://ja.wikipedia.org/wiki/データベーストリガ "wikilink")、[再帰クエリ](https://ja.wikipedia.org/wiki/再帰クエリ "wikilink")、[SQL:2003](https://ja.wikipedia.org/wiki/SQL:2003 "wikilink")準拠の[MERGE文が追加された](https://ja.wikipedia.org/wiki/MERGE_\(SQL\) "wikilink")\[12\]。

2010年10月4日、Firebird 2.5がリリースされた\[13\]。これまでスレッドモデルで実装されたSuper Serverと、プロセスモデルで実装されたClassic Serverの2つのサーバーモデルを並行して開発してきたが、バージョン2.5では新たにSuper Classicと称するサーバーモデルが追加される。Super Classic版では、Super Server版のボトルネックとなっていた統合型キャッシュを見直し、スレッド毎にキャッシュバッファを実装することで、これまで弱点とされてきたSMPへの対応を強化し、スケーラビリティが向上する予定である。その他に、[正規表現](../Page/正規表現.md "wikilink")や外部データベースへの接続が追加された\[14\]。

2016年04月19日、Firebird 3.0がリリースされた\[15\]。これまでスレッドモデルで実装されたSuper Serverと、プロセスモデルで実装された Classic Serverの2つのサーバーモデルを並行して開発し、バージョン 2.5では新たにSuper Classicと称するサーバーモデルが追加されたがFirebird 3.0実行形式ファイルの単一化が施された（デフォルトはSuper Server）。さらにウィンドウ関数や統計関数がサポートされ、各種制限の緩和、データベースごとのコンフィグレーション、スクローラブルカーソル、パッケージなどが追加された\[16\]。

## 管理ツール

  - [FlameRobin](http://www.flamerobin.org/)
  - [Database Master](http://www.nucleonsoftware.com)
  - [ibWebAdmin](http://sourceforge.net/projects/ibwebadmin/)

## 受賞

  - 2009\. SourceForge Community Choice Award: Best Project for enterprise. Finalist on Best Project and Best Project for Government.
  - 2007\. SourceForge Community Choice Award: Best Project for enterprise, Best user support.

## 外部リンク

  - [Firebirdプロジェクトホーム](http://www.firebirdsql.org/)
  - [Firebird日本ユーザー会](http://tech.firebird.gr.jp/firebird/index.php)
  - [FirebirdSQL Foundation](http://firebird.sourceforge.net/ff/foundation/)
  - [有志によるFirebird SQLリファレンス](http://firebird.00i.org/wiki/FrontPage)
  - [FIREBIRD WIKI](http://firebirdwiki.jp/)

## 脚注

<references/>

[Category:フリーデータベース管理システム](https://ja.wikipedia.org/wiki/Category:フリーデータベース管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  <http://itpro.nikkeibp.co.jp/article/NEWS/20070624/275673/>
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.