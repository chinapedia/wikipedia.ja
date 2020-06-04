> この記事は[Caddy](https://ja.wikipedia.org/wiki/Caddy)から翻訳されています。


</ref> | 対応OS = [Windows](https://ja.wikipedia.org/wiki/Windows "wikilink"), [OS X](https://ja.wikipedia.org/wiki/OS_X "wikilink"), [Linux](../Page/Linux.md "wikilink"), [各種 BSD](../Page/BSD.md "wikilink"), [Android](../Page/Android.md "wikilink"), [Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink") | サポート状況 = 活動中 | 種別 = [Web サーバー](https://ja.wikipedia.org/wiki/Webサーバー "wikilink"), [リバースプロキシ](../Page/リバースプロキシ.md "wikilink")サーバー, [ロードバランサー](../Page/サーバロードバランス.md "wikilink") | ライセンス = [Apache 2](../Page/Apache_License.md "wikilink") | 公式サイト =  }} **Caddy** は オープンソース\[1\] の [HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink") に対応した Web サーバーである。**Caddy Web サーバー** と呼ばれることもある。

Caddy は [Go 言語で記述されており](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")、HTTP 機能には Go 標準ライブラリを使用している。

Caddy の特徴的な機能の 1 つに、デフォルトでの [HTTPS](../Page/HTTPS.md "wikilink") の有効化がある。\[2\] \[3\] \[4\]

開発者のマシュー・ホルト（Matthew Holt）は Caddy の開発を 2014 年 12 月に開始した。そして 2015 年 4 月にリリースした。\[5\] それから 200 人以上の開発者が加わり [QUIC](https://ja.wikipedia.org/wiki/QUIC "wikilink") のサポートを追加するなどして発展して来た。

Caddy はさまざまな Web 技術をサポートしている。

Caddy は、[i386](../Page/Intel_80386.md "wikilink") / [amd64](../Page/X64.md "wikilink") / [ARM](../Page/ARMアーキテクチャ.md "wikilink") [アーキテクチャに対応しており](../Page/コンピュータ・アーキテクチャ.md "wikilink")、多くのオペレーティングシステム（[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") / [Mac](../Page/MacOS.md "wikilink") / [Linux](../Page/Linux.md "wikilink") / [各種 BSD](../Page/BSDの子孫.md "wikilink") / [Android](../Page/Android.md "wikilink") / [Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink")）それぞれに向けて静的[コンパイルされた](../Page/コンパイラ.md "wikilink")[バイナリ](../Page/バイナリ.md "wikilink")の[実行ファイル](../Page/実行ファイル.md "wikilink")として使用できる。

## 特徴

Caddy では多数の Web サイト向け技術が利用できる。

Caddy は[リバースプロキシ](../Page/リバースプロキシ.md "wikilink")および[ロードバランサーとしても機能する](../Page/サーバロードバランス.md "wikilink")。

Caddy の機能のほとんどは、Go のライブラリ実装に由来する。しかし[ミドルウェア](../Page/ミドルウェア.md "wikilink")として提供されている拡張機能もある。それらは Caddyfile（Caddy の構成に使用されるテキストファイル）から[ディレクティブ](../Page/ディレクティブ.md "wikilink")で指定できる。\[6\]

機能の一覧

  - HTTP/1.1（プレーンテキストベースの HTTP 通信）および HTTP/2（デフォルトでの HTTPS 通信）への対応
  - HTTPS の自動有効化もしくは手動での設定
      - [TLS](../Page/Transport_Layer_Security.md "wikilink") 1.3（ただし古いプロトコルも一時的にサポートしている）\[7\]
      - [SNI](https://ja.wikipedia.org/wiki/Server_Name_Indication "wikilink")
      - [OCSP](../Page/Online_Certificate_Status_Protocol.md "wikilink") ステープリング
  - [仮想ホスト](../Page/バーチャルホスト.md "wikilink")（同一ポートを使用した複数サイトの構築）\[8\]
  - [IPv4](../Page/IPv4.md "wikilink") および [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") のネイティブサポート
  - 静的ファイル配信（可能であれば sendfile を使用）
  - Graceful な再起動 / リロード
  - リバースプロキシ（HTTP または [WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")）
  - ヘルスチェックによる[負荷分散](../Page/サーバロードバランス.md "wikilink")
  - [FastCGI](../Page/FastCGI.md "wikilink") プロキシ\[9\] \[10\]
  - テンプレート（[サーバーサイドインクルード](https://ja.wikipedia.org/wiki/Server_Side_Includes "wikilink") に近い）
  - [Markdown](https://ja.wikipedia.org/wiki/Markdown "wikilink") レンダリング
  - WebSocket を介した [CGI](../Page/Common_Gateway_Interface.md "wikilink")
  - [Gzip](../Page/Gzip.md "wikilink") 圧縮
  - [Basic 認証](../Page/Basic認証.md "wikilink")
  - URL リライト
  - [リダイレクト](../Page/リダイレクト_\(HTTP\).md "wikilink")
  - ファイル閲覧
  - [ログの取得](../Page/データログ.md "wikilink")：アクセス / エラー / プロセス レベル
  - QUIC のサポート（実験的）

## セキュリティ

Caddy は広く知られた数多の [CVE](https://ja.wikipedia.org/wiki/脆弱性情報データベース "wikilink")（脆弱性情報データベース）に関して安全である。ここには [Heartbleed](https://ja.wikipedia.org/wiki/ハートブリード "wikilink") / DROWN / [POODLE](https://ja.wikipedia.org/wiki/POODLE "wikilink") / [BEAST](../Page/Transport_Layer_Security.md "wikilink") なども含まれる。\[11\] さらに Caddy では TLS_FALLBACK_SCSV を使用することでプロトコルのダウングレード攻撃を防ぐこともできる。

2015 年 6 月 2 日に、バージョン 0.7.1 がリリースされた。これは Caddy の [Basic 認証ミドルウェアに対する](../Page/Basic認証.md "wikilink")[タイミング攻撃](https://ja.wikipedia.org/wiki/タイミング攻撃 "wikilink")の脆弱性に対してパッチを当てるためだった。\[12\]

プロトコルおよび暗号スイートに関して、Caddy は TLS 1.0 - 1.2 を使用し、且つ、AES-256 - GCM - SHA-384 による ECDHE - ECDSA（[楕円曲線ディフィー・ヘルマン鍵共有](../Page/ディフィー・ヘルマン鍵共有.md "wikilink") - [楕円曲線 DSA](https://ja.wikipedia.org/wiki/楕円曲線DSA "wikilink")） を標準としている。ただし他の多くの暗号もサポートしている。Caddy は [Cloudflare](https://ja.wikipedia.org/wiki/Cloudflare "wikilink") でも使用されており、実験的な TLS 1.3 通信の提供が行われている。\[13\]

[C 言語](../Page/C言語.md "wikilink") で記述された従来のプログラムに見られたような、まず完全な特権を与えてそれを必要に応じて段階的に絞って行くしくみは、[Go 言語](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink") のプログラムでは特殊な方法でしか実現できないかもしくはまったく不可能である。\[14\]

### HTTPS 通信の自動化

Caddy は、適正な[ドメイン名](../Page/ドメイン名.md "wikilink")（[ACME プロトコル](https://ja.wikipedia.org/wiki/Automated_Certificate_Management_Environment "wikilink") を介して TLS 証明書を要求できるドメイン名）を持つサイトでは、デフォルトで HTTPS 通信を有効化する。HTTP リクエストは HTTPS にリダイレクトされる。\[15\]

Caddy はサーバー起動時に、必要に応じて証明書を取得し、サーバー稼働中は証明書を更新し続ける。

デフォルトの認証局は [Let's Encrypt](https://ja.wikipedia.org/wiki/Let's_Encrypt "wikilink") である。2016 年第 1 四半期に、Caddy は Let's Encrypt が発行した証明書の約 2 % を占めていた。\[16\] また、ユーザーは、対象とする ACME 認証局 をカスタマイズすることもできる。この機能はサーバー構成をテストする時に有用である。

他の設定を採ることも可能である。「オンデマンド TLS」と呼ばれる機能である。この機能を用いると、Caddy は起動時ではなく TLS ハンドシェイク時に、必要な場合にのみ証明書を取得する。\[17\] この機能を有効にするには、ユーザーは、発行可能な証明書の最大数を指定する必要がある。オンデマンド TLS 機能が有効な場合、Caddy は、まだ証明書が無いホスト名に対するリクエストを受け取ると、取得した証明書をメモリにキャッシュしてディスクに保存しながら、ACME を介して新しい証明書を要求し、それをすぐに提供する。 通常、このプロセスには数秒掛かる。そのため転送[ビットレート](../Page/ビットレート.md "wikilink")の[制約は厳しくなる](../Page/スループット.md "wikilink")。

TLS 通信において、Caddy はセッションチケットキーを定期的に自動的にローテーションする。このことで転送する情報の完全な機密性を保持している。 \[18\]

## テレメトリー

バージョン 0.11 から、Caddy に[テレメトリー機能が搭載された](../Page/遠隔測定法.md "wikilink")。 \[19\] これは 公式 Webサイトから Caddy をダウンロードする場合はオプトイン（デフォルトで無効）となっている。一方、ソースからビルドする場合はオプトアウト（デフォルトで有効）である。\[20\]

## 影響

### CoreDNS

Miek Gieben は Caddy Web サーバーのフォークから CoreDNS を作成した。Caddy の単純な構成構文、プラグインアーキテクチャ、および Go 言語で記述されたコードが活用されている。 \[21\]

## 参考文献

## 外部リンク

  -
  -
[Category:Web_サーバー](https://ja.wikipedia.org/wiki/Category:Web_サーバー "wikilink") [Category:オープンソース](https://ja.wikipedia.org/wiki/Category:オープンソース "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:Go_言語_のソフトウェア](https://ja.wikipedia.org/wiki/Category:Go_言語_のソフトウェア "wikilink") [Category:オープンソースのサーバー](https://ja.wikipedia.org/wiki/Category:オープンソースのサーバー "wikilink") [Category:オープンソースのソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースのソフトウェア "wikilink") [Category:HTTP/2](https://ja.wikipedia.org/wiki/Category:HTTP/2 "wikilink") [Category:QUIC](https://ja.wikipedia.org/wiki/Category:QUIC "wikilink")

1.
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
17.
18.
19.
20.
21.