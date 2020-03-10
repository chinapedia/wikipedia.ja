> この記事は[PhpBB](https://ja.wikipedia.org/wiki/PhpBB)から翻訳されています。


**phpBB**（ピーエイチピービービー）は、[GPLに基づいて開発された](../Page/GNU_General_Public_License.md "wikilink")[電子掲示板](../Page/電子掲示板.md "wikilink")。[PHP言語で制作されたシステムである](../Page/PHP_\(プログラミング言語\).md "wikilink")。多言語化が比較的簡単で日本語版も複数のサイトで配布されている。

## 概要

現在では、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")や[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")のような定番のデータベースに加え、 [Microsoft SQL Serverや](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[Oracle](../Page/Oracle_Database.md "wikilink")、[SQLite](../Page/SQLite.md "wikilink")、[Firebird](../Page/Firebird.md "wikilink")などにも対応している。

[CAPTCHA](../Page/CAPTCHA.md "wikilink")が標準搭載されている。[CMS](../Page/コンテンツ管理システム.md "wikilink") ([Joomla\!](https://ja.wikipedia.org/wiki/Joomla! "wikilink")) の電子掲示板モジュールとして利用される場合もあるが、それ自身CMSとしての機能を備えている。故にモジュールとして利用されるよりも、それ単体でフォーラムサイトの構築またはサイト内コンテンツの1つとして利用される場合がより一般的である。[フォーラム管理](../Page/インターネットコミュニティ.md "wikilink")、パーミッション設定、[アバター](../Page/アバター.md "wikilink")、ユーザー登録、ユーザーグループ、[BBコード](../Page/BBコード.md "wikilink")、[プライベートメッセージ](https://ja.wikipedia.org/wiki/プライベートメッセージ "wikilink")、投票、モデレータ管理、メール通知など様々な機能がある。デザインも[HTMLで構成されたテンプレートにより変更できる](../Page/HyperText_Markup_Language.md "wikilink")。また、phpBB2ではアップロード機能を利用するにはMOD（[機能拡張](https://ja.wikipedia.org/wiki/機能拡張 "wikilink")）を追加する必要があったが、phpBB3より標準で搭載された。

MOD のインストールは基本的には本体ソースファイルの修正である。phpBB3ではAutoMODというツールが用意されており、これを利用すれば MOD のインストール及びアンインストールは自動で行ってくれる。他の CMS 等と違い、phpBBにおいてはMODはあくまでファイルの修正 (modification) を意味しており[モジュール](../Page/モジュール.md "wikilink") (module) ではない。そのため MOD 同士の相性によっては競合が起こりインストールエラーが発生する可能性がある。また、PHPのフレームワークである[Symfony](https://ja.wikipedia.org/wiki/Symfony "wikilink")が使われている

## 歴史

  - [2000年](../Page/2000年.md "wikilink") - phpBB公開。
  - [2002年](../Page/2002年.md "wikilink") - phpBB2公開。
  - [2004年](../Page/2004年.md "wikilink") - phpBB2の[セキュリティホール](../Page/セキュリティホール.md "wikilink")を突いて[Webサーバ](../Page/Webサーバ.md "wikilink")に感染する[ワーム](../Page/ワーム_\(コンピュータ\).md "wikilink")「[Santy](https://ja.wikipedia.org/wiki/Santy "wikilink")」が発見された。
  - [2006年](../Page/2006年.md "wikilink") - 中頃よりphpBB3のベータが公開された。さらに、次期バージョンのphpBB3では[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、[Oracle](../Page/Oracle_Database.md "wikilink")、[SQLite](../Page/SQLite.md "wikilink")、[Firebird](../Page/Firebird.md "wikilink")にも対応する予定である。
  - [2007年](../Page/2007年.md "wikilink") - [12月13日](https://ja.wikipedia.org/wiki/12月13日 "wikilink")にphpBB3.0.0 "Olympus" 公開。
  - [2009年](../Page/2009年.md "wikilink") - [1月1日](../Page/1月1日.md "wikilink")にphpBB2のサポートが終了

## 使用方法

### インストール

最新版 (3.0.9) を日本語化してインストールするには、本体ソースのほか日本語のランゲージパックをダウンロードし、ランゲージパック内の language フォルダと styles フォルダをそのままphpBB3ルートフォルダ直下へ上書きコピーする。[XAMPP](../Page/XAMPP.md "wikilink")（[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") および [Linux](../Page/Linux.md "wikilink")）ならば、phpBB3フォルダごとhtdocsフォルダ内にコピーして、その[URLをブラウザからアクセスし](../Page/Uniform_Resource_Locator.md "wikilink")、日本語ガイダンスに従って作業を進めれば比較的簡単にインストールできる。PHP拡張モジュール mbstring のサポートは必須ではない。最低必要なディスクスペースは9MBであり、受け皿となるデータベースとデータベースへのアクセス権を持つユーザーは先に用意しておく必要がある。文字コードはデフォルトで[UTF-8](../Page/UTF-8.md "wikilink")となる。

### アップデート

phpBB3をアップデートするには、アップデートパッケージをダウンロードし、アップデートパッケージ内の install フォルダをサーバ上phpBB3ルートディレクトリ直下へアップロードし、その URL をブラウザからアクセスし、日本語ガイダンスに従って作業を進めていけばアップデートは完了する。

## 日本語使用時の問題点

phpBB2ではメールや投稿記事の日本語文章が文字化けしてしまう可能性が常に存在していたが、phpBB3では文字化けの問題はほぼ解決されている。 現在 (3.0.9)、日本語文字を使用した時の問題点としては、

  - 日本語でキーワード検索してもうまくヒットしてくれない（ただし日本語用の検索MODをインストールすればこの問題はある程度は解決される）。
  - 日本語文字を含むURL ([IRI](../Page/Internationalized_Resource_Identifier.md "wikilink")) をリンク化できない。

が存在する。

記事の投稿はもとより、日本語名ファイルのアップロード、ユーザー名の長さの最大・最小、言語フィルタ、データコンバート、ユーザー名ソート等は日本語であっても問題なく動作する。

## 脚注

## 外部リンク

  - [phpBB Group](https://phpbb.com/)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:PHP](https://ja.wikipedia.org/wiki/Category:PHP "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")