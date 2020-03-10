> この記事は[OTRS](https://ja.wikipedia.org/wiki/OTRS)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:otrs-2.0.4-queueview.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:otrs-2.0.4-answer.png "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:otrs-2.0.4-faqsearch.png "wikilink") **OTRS**は、オープンソース・チケット・リクエスト・システム (Open-source Ticket Request System) の略で、会社や組織や団体が、受け取った個々の質問とそれに対して会社等が行なった対応の履歴を「チケット」と呼ばれる単位でまとめて管理できる、[オープンソース](../Page/オープンソース.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")パッケージである。

## 概要

OTRSによって発行された全てのチケットは、それに関連する履歴や事象が共に保存され、表示できる。似たような事例のチケットをまとめて管理できるため、一つの不具合が多数の顧客に影響し、似たような問い合わせを大量に受けたような場合に、対応を管理するのが格段に容易になる。またマルチユーザーシステムであるため、複数のOTRSの利用者が同一案件に対して同時に対処でき、受信メッセージの確認、整理、回答といった対応をすることができる。OTRSは[スケーラブル](https://ja.wikipedia.org/wiki/スケーラブル "wikilink")であり、1日に何千ものチケットを扱うことができ、同時に操作できる利用者の数もほぼ無限である。日本語ウィキペディアを含めてウィキメディア財団の各プロジェクトも外部からの問い合わせ等にこのシステムを利用している。

OTRSは[FAQ](../Page/FAQ.md "wikilink")の文を作成・編集・検索するための統合された機能を持つ。利用者は、チケットに関連する回答の中にFAQの文を埋め込んでもよい。

OTRSは[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")から操作されるので、利用者のコンピュータ等の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が何であっても、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")さえ動作すれば操作ができる。会社等の関係者以外の者が、OTRSにアクセスし、チケットに情報を追加できるようにすることもできる。

OTRSは、機能の骨組みを提供する。例えば、ドイツの[BSIという組織が使っているSIRIOSというシステムは](https://ja.wikipedia.org/wiki/:en:Bundesamt_für_Sicherheit_in_der_Informationstechnik "wikilink")、OTRSを基にして作られている。

## 歴史

OTRS.orgのプロジェクトは、マルティン・エデンホファーによって、2001年に創設された。OTRSは現在全世界で2万回以上インストールされている。

| バージョン | 日付         | 備考                                                                                                                                                                                                                        |
| ----- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0.5   | 2002-04-09 | OTRSの最初の公式版の公開。コアシステムが公開され、動作した。                                                                                                                                                                                          |
| 1.0   | 2003-02-14 | 開発から2年経過、最初の安定版の公開。                                                                                                                                                                                                       |
| 1.1   | 2003-05-01 | バックエンドとユーザーインターフェースに多くの改良。                                                                                                                                                                                                |
| 1.2   | 2004-02-16 | 5つの新しい言語、新しいFAQデータベース、UTF-8サポート、シングルサインオン。                                                                                                                                                                                |
| 1.3   | 2004-09-22 | 新しい統計構成とタイムゾーン対応。                                                                                                                                                                                                         |
| 2.0   | 2005-08-01 | 開発から5年でOTRS 2.0の公開。19言語に対応。[PGPと](../Page/Pretty_Good_Privacy.md "wikilink")[S/MIME](https://ja.wikipedia.org/wiki/S/MIME "wikilink")、XMLデータベースインターフェース、ウェブに保管されたものを通じて追加アプリケーションをインストールするためのウェブアプリケーションパッケージマネージャーが主な特色。 |
| 2.1   | 2006-10-05 | 総合的には10%、検索については50%のパフォーマンスの改良を獲得。 Microsoft SQLサーバーのサポートの改良、カレンダーの改良、LDAP サポートの改良、PDF出力サポートの追加、ペルシャ語のサポート。                                                                                                               |
| 2.2   | 2007-06-19 | サービス・SLAのサポート、ネイティブなチケットタイプのサポート、複数の認証基盤のサポート。                                                                                                                                                                            |
| 2.3   | 2008-07-22 | 性能向上、検索機能の向上、チケットのズーム・移動のサポート。                                                                                                                                                                                            |
| 2.4   | 2009-07-22 | 新しいダッシュボード、HTMLメールのサポート、Ajaxに基づくカスタマサーチ・自動補完などが主な特色。ライセンスをAGPL version3に変更。                                                                                                                                               |
|       |            |                                                                                                                                                                                                                           |

'''OTRSのバージョン '''

## OTRSの開発

OTRSは開発当初よりプログラミング言語[Perl](../Page/Perl.md "wikilink")で実行されている。ウェブインターフェースは[JavaScript](../Page/JavaScript.md "wikilink")を使うことでユーザーにより使いやすく作られている（セキュリティー上の理由からそれをオフにすることもできる）。OTRSの異なる機能面は再利用できるバックエンドモジュールとして実行されている。従って、OTRSシステムの機能面を拡張するために自分のモジュールを書くことが簡単である。

ウェブインターフェースそれ自体はダイナミックテンプレートランゲージ (DTL) と呼ばれる独特のテンプレートメカニズムを使って、システム出力データの表示を容易にしている。

最初、OTRSは[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")データベース上でのみ動作した。後に、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、[Oracle Database](../Page/Oracle_Database.md "wikilink")、[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、[Microsoft SQL Serverのサポートが追加された](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")。OTRSは[Windows上だけではなく](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（[Linux](../Page/Linux.md "wikilink"), [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink")など）数多くの[UNIX](../Page/UNIX.md "wikilink")や[Unix系](../Page/Unix系.md "wikilink")プラットフォーム上でも使える。

OTRSシステムの能力は、[Apache HTTP Serverのためのmod](../Page/Apache_HTTP_Server.md "wikilink")_perlを使うことや、データベースとウェブサーバーシステムを分けることにより高めることができる。これによって、大量の同時操作者や大量のチケット数をこなすことができる。

UNIXや類似の環境ではOTRSは、メール転送エージェントの[Postfix](../Page/Postfix.md "wikilink")のようなシステムプログラムやメールフィルターのprocmailと親和性高く動作する。

## 外部リンク

  - [OTRS.org](http://otrs.org/) – プロジェクトサイト

<!-- end list -->

  - [OTRS GmbH](http://otrs.com/) – OTRS社

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink")