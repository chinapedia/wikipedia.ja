> この記事は[Bugzilla](https://ja.wikipedia.org/wiki/Bugzilla)から翻訳されています。


**Bugzilla**（バグジラ）は、[Mozilla Foundationが開発](../Page/Mozilla_Foundation.md "wikilink")、使用してきた[ウェブベースの](../Page/World_Wide_Web.md "wikilink")[バグ管理システム](../Page/バグ管理システム.md "wikilink")。元々[Netscape社が社内で使ってきたシステムであったが](../Page/ネットスケープコミュニケーションズ.md "wikilink")、後に公開。極めて初期のバージョンは[Tclで記述されていたが](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")、オープンソース・プロジェクトになってからのソースコードは、Perlで記述されている。現在では、オープンソース、[プロプライエタリ問わず](../Page/プロプライエタリ・ソフトウェア.md "wikilink")、数百のプロジェクトでバグ管理ツールとして選択されている。

Bugzillaでの[バグ](../Page/バグ.md "wikilink")はソフトウェアに対する問題点、要望、議論などのすべてを表し、機能拡張リクエストにも利用される。

NetscapeがNetscape Webブラウザのソースコードを公開する際にmozilla.orgで使うツールとして、Bonsaiと共に公開されたものが現在のBugzillaの原型である。

## 機能

### プロジェクト

開始に当たって、プロジェクトに応じたさまざまな属性を設定できる。これにより、カテゴリ、コンポーネント別にバグを整理でき、また、非常に多様な問題に対応できる。

### 登録

バグを登録する際に、そのバグにまつわるさまざまな要素を付加することができる。また、登録作業軽減のためのヘルパーも用意され、これにより、初心者でも簡単にバグを登録できる。

### バグに関する議論

問題点一つに対して、一つのバグを発行し、それについて議論しあう仕組みを持っている。それらを貫くために各種キーワードを登録することもでき、これにより、関連するバグを見つけやすくすることが出来る。相互に依存するバグを登録することで、問題解決に必要な要素を分割して、作業を軽減することが出来る。

### バグの検索

Bugzillaは、標準でバグをカテゴリ別、ステータス別、登録者別に検索する機能を持っており、これによって、大量のバグの中から、該当するバグを見つけることが出来る。

## 要件

Bugzillaを利用するにあたって必要なソフトウェアは、以下の通りである。

  - 対応するデータベースサーバ（[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink") または [Oracle](../Page/Oracle_Database.md "wikilink")）。要求されるバージョンはbugzillaのバージョンにより異なる
  - 適切な[Perl](../Page/Perl.md "wikilink")5
  - 各種Perlモジュール
  - Apacheのような対応するウェブサーバ（CGIが動くウェブサーバであれば使える）
  - [Sendmail](../Page/Sendmail.md "wikilink")、[qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")、[Postfix](../Page/Postfix.md "wikilink")、あるいは[Exim](https://ja.wikipedia.org/wiki/Exim "wikilink")といった適切な[メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")

## 出典

## 関連項目

  - [Mozilla Foundation](../Page/Mozilla_Foundation.md "wikilink")

## 外部リンク

  -

  -

  - [日本Bugzillaユーザグループ](http://bug-ja.org/)

  - [Bugzilla-ja - MDC](https://developer.mozilla.org/ja/Bugzilla-ja)

<!-- end list -->

  - [Open Directory - Bug Tracking Software](http://dmoz.org/Computers/Software/Configuration_Management/Bug_Tracking/)
  - [Bugzilla Installation List Tops 400](http://weblogs.mozillazine.org/gerv/archives/008446.html)

### 日本語での稼動例

  - [もじら組 Bugzilla-jp](http://bugzilla.mozilla.gr.jp/)
  - [Mozilla Communities' Network in Japan の Bugzilla](http://bugzilla.jpmoz.net/)

[Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink") [Category:バグ管理システム](https://ja.wikipedia.org/wiki/Category:バグ管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1998年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1998年のソフトウェア "wikilink")