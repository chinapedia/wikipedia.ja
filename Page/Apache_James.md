> この記事は[Apache James](https://ja.wikipedia.org/wiki/Apache_James)から翻訳されています。


**Apache James**（アパッチ・ジェームズ）は、[Apacheプロジェクト内の電子メールアプリケーションサーバを開発するサブプロジェクトである](https://ja.wikipedia.org/wiki/Apacheソフトウェア財団 "wikilink")。Jamesというプロジェクト名は、**J**ava **A**pache **M**ail **E**nterprise **S**erver の頭文字をとったものである。

Webアプリケーションサーバとして有名な、同プロジェクトの[Apache Tomcatの](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")[電子メール](../Page/電子メール.md "wikilink")版である。

Apache Jamesは、[BSDライセンスをベースとした](https://ja.wikipedia.org/wiki/BSD_License "wikilink")[Apache Licenseであり](https://ja.wikipedia.org/wiki/Apache_License "wikilink")、商用利用も多くされている。

Apache Jamesは、[Apache Avalon](https://ja.wikipedia.org/wiki/Apache_Avalon "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")を元に開発されていたので、[Apache Avalonが解散したときは](https://ja.wikipedia.org/wiki/Apache_Avalon "wikilink")、どうしたらよいか混乱した。

そして、Apache James 2.\*系以前は、[Apache Avalon](https://ja.wikipedia.org/wiki/Apache_Avalon "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")を使用していたが、Apache James3.0系から、[OSGi](../Page/OSGi.md "wikilink")を元にして、[Spring Framework](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")を使用している。

## Mailet

Jamesの各機能は、[電子メール](../Page/電子メール.md "wikilink")サーバ上（James）で、メイレット（Mailet）と呼ばれる[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で記述可能なロジック群により構成されている。メイレットはTomcatでいう[サーブレット](https://ja.wikipedia.org/wiki/サーブレット "wikilink")と同様のものであり、James自体はTomcatと同じくコンテナである。よってJames自体には、実際に電子メールプロトコルに関する各機能は実装されていないが、電子メールサーバとして最低限必要となるであろう、[SMTPや](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")[POP3](https://ja.wikipedia.org/wiki/POP3 "wikilink")、[IMAP4](https://ja.wikipedia.org/wiki/IMAP4 "wikilink")などを扱う部分は、メイレットのサンプル/リファレンス実装としてJamesに添付され提供されており、これらはそのまま使用しても差し支えないほどの完成度を誇っている。このメイレットを駆使することにより、簡単に機能の追加などを可能にし、通常の電子メールサーバを凌駕する電子メールアプリケーションサーバとして機能するというモノである。

## MailetとMatcherについて

Mailetは、メールを送信するために必要な処理をする。

Matcherは、メールをいろいろな条件を元に振り分ける処理をする。

## James 2.\*系以前のアプリケーションフレームワークについて

James 1.\*系またはJames 2.\*系は、[Apache Avalon](https://ja.wikipedia.org/wiki/Apache_Avalon "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")で開発されている。

## James 3.0系アプリケーションフレームワークについて　

James 3.0系は、[OSGi](../Page/OSGi.md "wikilink")を元にして、[Spring Framework](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")で開発されている。

## JAMES Project

  - Hupa
    Hupaは、[GWT](https://ja.wikipedia.org/wiki/GWT "wikilink")で作成され[IMAP](https://ja.wikipedia.org/wiki/IMAP "wikilink")を基本に作成した[Webメール](../Page/Webメール.md "wikilink")。
  - IMAP
    [IMAP](https://ja.wikipedia.org/wiki/IMAP "wikilink")は、メールサーバー上の電子メールにアクセスし操作するためのプロトコル。
  - jSieve
    jSieveは、Javaで記述された電子メールをする時に不要なメールを削除する等の[フィルタリング](https://ja.wikipedia.org/wiki/フィルタリング "wikilink")の機能を提供するための言語。
  - jSPF
    jSPFは、Javaで記述された送信者を判別して[フィルタリング](https://ja.wikipedia.org/wiki/フィルタリング "wikilink")をする[SPF](https://ja.wikipedia.org/wiki/SPF "wikilink")。
  - Mime4j
    Mime4jは、電子メールでいろいろな書式を扱えるようにした[MIME](https://ja.wikipedia.org/wiki/MIME "wikilink")。
  - Mailet API
    Mailet APIは、電子メールを送信するために必要な処理をできるようにする[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。
  - Mailbox
    Mailboxは、柔軟な[メールボックス](https://ja.wikipedia.org/wiki/メールボックス "wikilink")の[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")を[メール](https://ja.wikipedia.org/wiki/メール "wikilink")（[IMAP4](https://ja.wikipedia.org/wiki/IMAP4 "wikilink")、[POP3](https://ja.wikipedia.org/wiki/POP3 "wikilink")、[SMTP](https://ja.wikipedia.org/wiki/SMTP "wikilink")、および他のプロトコル)で提供するライブラリ。
  - MPT
    MPTは、ApacheのJamesのメールテスト用プロトコルのためのフレームワーク。
  - Protocols
    Protocolsは、メールプロトコルの実装、および拡張性に優れた軽量なフレームワークを提供。
  - Server
    Serverは、ApacheのJamesのメールサーバー本体。
  - Postage
    Postageは、電子メールの交通整理をする、[MTA](https://ja.wikipedia.org/wiki/MTA "wikilink")の機能をするもの。
  - jDKIM
    jDKIMは、Javaで記述された[DKIM](https://ja.wikipedia.org/wiki/DKIM "wikilink")の実装ライブラリ。

## Apache Jamesのサブプロジェクト

## 脚注

<references/>

## 外部リンク

  -
[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:メール転送エージェント](https://ja.wikipedia.org/wiki/Category:メール転送エージェント "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")