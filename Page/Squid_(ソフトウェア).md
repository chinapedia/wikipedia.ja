> この記事は[Squid \(\)](https://ja.wikipedia.org/wiki/Squid_\(\))から翻訳されています。


**Squid**（スクウィッド）は[プロキシ](../Page/プロキシ.md "wikilink") (Proxy) [サーバ](../Page/サーバ.md "wikilink")、ウェブキャッシュサーバなどに利用される[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")。[GPLでライセンスされている](../Page/GNU_General_Public_License.md "wikilink")。 Squidの用途は、重複リクエストに対したキャッシュ応答によるウェブサーバの高速化や、ネットワーク資源を共有する人々が行う[World Wide Webや](../Page/World_Wide_Web.md "wikilink")[DNSなどの様々な](../Page/Domain_Name_System.md "wikilink")[ネットワーククエリのキャッシュなど](../Page/コンピュータネットワーク.md "wikilink")、多岐にわたる。元来は[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")系のコンピュータで動作させる目的で設計されている。

Squidは長く開発が続けられてきた\[1\]。多様なプロトコルをサポートしているが、主に[HTTPと](../Page/Hypertext_Transfer_Protocol.md "wikilink")[FTPで利用される](../Page/File_Transfer_Protocol.md "wikilink")。 [TLS/SSL](../Page/Transport_Layer_Security.md "wikilink")、[HTTPS](../Page/HTTPS.md "wikilink")などのセキュリティで保護された通信のサポートも行われている\[2\]。

当初は[C言語](../Page/C言語.md "wikilink")で書かれていたが、バージョン3以降では多くのソースが[C++](../Page/C++.md "wikilink")で書かれたものに置き換えられている。

## ウェブプロキシ

[キャッシングは](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")、リクエストされたWebページやWebページ上の画像などインターネット上の様々な情報を[クライアント](https://ja.wikipedia.org/wiki/クライアント "wikilink")側から見てネットワーク上の近傍にあるコンピュータに貯蔵しておく技術である。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")はSquidをHTTPのプロキシサーバとして利用し、ネットワーク帯域を節約するとともに、目的のページに高速にアクセスすることができる。 これは[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")が加入利用者のインターネットアクセスを高速化するのに、あるいは[LAN内でインターネット接続を共有するのに有効な手法である](../Page/Local_Area_Network.md "wikilink")。プロキシ（実質的なクライアントの代理としてクライアントとして目的の情報にアクセスする）でもあることから、匿名性や安全性も提供するはたらきを持っている。

プロキシサーバの利用は、ブラウザ等のクライアントのソフトウェアで利用したいプロキシサーバの指定を明示的に行う方法か、もしくは[透過プロキシ](https://ja.wikipedia.org/wiki/透過プロキシ "wikilink")と呼ばれる特に設定を必要としない方法によって行われる。明示的な設定を行う方法はインターネットサービスプロバイダの利用者等に、透過プロキシは企業内のLANの設定等でしばしば用いられる。

Squidは、クライアントが生成するヘッダを書き換えるなどの方法によって、匿名による接続の機能も提供する。詳細は、Squidのドキュメンテーションの`header_access`および`header_replace`の項に記載されている。

## リバースプロキシ(Reverse Proxy)

前項で述べたような、特定少数のクライアントのために不特定多数のサーバのキャッシュを提供する形態のプロキシが、伝統的な利用法である。

もう一方の利用法は、**[リバースプロキシ](../Page/リバースプロキシ.md "wikilink")**\[3\]あるいは**ウェブサーバアクセラレーション**と呼ばれる（`httpd_accel_host`の設定を用いる）。 この利用法では、不特定多数のクライアントに対して特定少数のサーバのキャッシュを提供する。

実際に[コンテンツ](../Page/コンテンツ.md "wikilink")を持っているウェブサーバを*slow.example.com*、Squidによるリバースプロキシを*www.example.com*とする。 *www.example.com*上のあるコンテンツに対するリクエストが最初に行われた際に、実際のコンテンツは*slow.example.com*から取り出されるが、一定期間中（期間は設定により異なる）、2回目以降のアクセスにはこの際に取り出されたコピーがリバースプロキシから送出されるようになる。 結果として*slow.example.com*へのアクセス数を低く抑えることができ、*slow.example.com*の負荷やネットワークの帯域を節約できる。

一つのSquidサーバを通常のプロキシとリバースプロキシ両方の機能で稼働させることも可能である。

## 移植性

[LAMP_software_bundle.svg](https://ja.wikipedia.org/wiki/File:LAMP_software_bundle.svg "fig:LAMP_software_bundle.svg")-based software bundle [LAMP](https://ja.wikipedia.org/wiki/LAMP_\(ソフトウェアバンドル\) "wikilink") here additionally with Squid as web cache\]\]

Squidは以下の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上で動作可能である。

  - [Linux](../Page/Linux.md "wikilink")
  - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [OpenBSD](../Page/OpenBSD.md "wikilink")
  - [NetBSD](../Page/NetBSD.md "wikilink")
  - [BSDI](https://ja.wikipedia.org/wiki/BSDI "wikilink")
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - OSF and Digital Unix
  - [IRIX](../Page/IRIX.md "wikilink")
  - SunOS/[Solaris](../Page/Solaris.md "wikilink")
  - [NeXTStep](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")
  - [SCO Unix](https://ja.wikipedia.org/wiki/OpenServer "wikilink")
  - [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")
  - [HP-UX](../Page/HP-UX.md "wikilink")
  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")

ウィキペディアのupload.wikimedia.orgでも使用されていた\[4\]。

## 脚注

## 外部リンク

### Information

  -
  - [Squid + PF](http://www.benzedrine.cx/transquid.html) - SquidとPFを用いた透過プロキシ

  - [Logfile Analysis](http://www.squid-cache.org/Scripts/) - ログファイル解析スクリプトの一覧

  - [Squid Support](http://squid.visolve.com/squid/): マニュアル、設定のヒント集など

  - [Squid cache Configuration](http://www.visolve.com/squid/whitepapers/): マニュアル、設定のヒント集など

### アドオン

  - [Squidguard](http://www.squidguard.org) - フィルタリングのためのプラグイン
  - [DansGuardian](http://dansguardian.org) - フィルタリング(Smart filtering)のためのプラグイン
  - [Calamaris](http://cord.de/tools/squid/calamaris/Welcome.html.en) - ログファイルの解析ツール
  - [Squeezer2](http://www.rraz.net/squeezer2/) - ログファイルの解析ツール
  - [SARG Squid Analysis Report Generator](http://sarg.sourceforge.net/) - ログファイルの解析ツール

### キャッシュ動作の確認が可能なWebページ

  - [web-caching.com](http://www.web-caching.com/cgi-web-caching/cacheability.py): check page cacheability
  - [analyze.forret.com](http://analyze.forret.com): analyze HTTP headers and compare to Squid policy

[Category:ファイアウォールソフトウェア](https://ja.wikipedia.org/wiki/Category:ファイアウォールソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink")

1.  1990年代前期に開発されたHarvest Cache Daemonに基づいている、とする記述が見える。
2.  [SquidのFAQページより（英語）](http://www.squid-cache.org/Doc/FAQ/FAQ-1.html#ss1.12)
3.
4.