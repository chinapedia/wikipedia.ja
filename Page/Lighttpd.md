> この記事は[Lighttpd](https://ja.wikipedia.org/wiki/Lighttpd)から翻訳されています。


**lighttpd** （ライティ\[1\]）は高速性の重視される環境に最適化された、安全・高速で標準に準拠し、柔軟であることを指向して設計された[Webサーバ](../Page/Webサーバ.md "wikilink")である。

[C10K問題](https://ja.wikipedia.org/wiki/C10K問題 "wikilink")の概念実証としてJan Kneschke によって書かれた。名称の由来は「light」と「httpd」との[かばん語](../Page/かばん語.md "wikilink")である。

メモリ消費量が少なく、[CPU](../Page/CPU.md "wikilink")負荷の少ない高速動作が目的となっているため、負荷が問題な場合や、静的コンテンツを動的コンテンツと区別して送信する場合などに適しているとされる。

## 前提

他の[Webサーバ](../Page/Webサーバ.md "wikilink")と比較して\[2\]、[CPU](../Page/CPU.md "wikilink")の負荷が小さく、速度が最適化されており\[3\]、負荷の問題がある[サーバ](../Page/サーバ.md "wikilink")、または動的コンテンツとは別に静的メディアを提供するサーバーにlighttpd が適している。lighttpd は無料の[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")であり、[BSDライセンス](../Page/BSDライセンス.md "wikilink")の下で配布されている。[Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Unix系オペレーティングシステム "wikilink")と[Microsoft Windowsでネイティブに実行できる](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。\[4\]\[5\]

## アプリケーションサポート

lighttpd は外部プログラムへの[FastCGI](../Page/FastCGI.md "wikilink")、[SCGI](https://ja.wikipedia.org/wiki/Simple_Common_Gateway_Interface "wikilink")、[CGIインターフェースをサポートしているため](../Page/Common_Gateway_Interface.md "wikilink")、あらゆる[プログラミング言語](../Page/プログラミング言語.md "wikilink")で書かれた[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")を[サーバ](../Page/サーバ.md "wikilink")で使用できる。特に人気のある言語として、[PHP (プログラミング言語)のパフォーマンスは特に注目されている](../Page/PHP_\(プログラミング言語\).md "wikilink")。lighttpd の[FastCGI](../Page/FastCGI.md "wikilink")は、[オペコードキャッシュ](https://ja.wikipedia.org/wiki/オペコードキャッシュ "wikilink")([APC](../Page/APC.md "wikilink") 等)を使用して[PHP (プログラミング言語)を適切かつ効率的にサポートするように構成できる](../Page/PHP_\(プログラミング言語\).md "wikilink")。さらに、[Python](../Page/Python.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、および[Lua](../Page/Lua.md "wikilink")コミュニティでの人気からも注目されている。lighttpdは、データベース駆動型[Webサイトを構築するために設計された復元力のある](https://ja.wikipedia.org/wiki/WEBサイト "wikilink")[インメモリデータベース](https://ja.wikipedia.org/wiki/インメモリデータベース "wikilink")であるもサポートしている。これは[Catalyst (ソフトウェア)および](../Page/Catalyst_\(ソフトウェア\).md "wikilink")[Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink") Webフレームワーク用の一般的なWebサーバである。lighttpd は[ISAPI](../Page/ISAPI.md "wikilink")をサポートしていない。

## 特徴

  - [サーバロードバランス](../Page/サーバロードバランス.md "wikilink")、[FastCGI](../Page/FastCGI.md "wikilink")、[SCGI](https://ja.wikipedia.org/wiki/Simple_Common_Gateway_Interface "wikilink")、および[HTTPプロキシ](https://ja.wikipedia.org/wiki/HTTPプロキシ "wikilink")のサポート
  - [`chroot`](https://ja.wikipedia.org/wiki/chroot "wikilink")システムコールの使用
  - Webサーバーイベントメカニズムのパフォーマンス-`select()`, `poll()`, `epoll()`
  - [`kqueue`](https://ja.wikipedia.org/wiki/kqueue "wikilink")や[`epoll`](https://ja.wikipedia.org/wiki/epoll "wikilink")などのより効率的なイベント通知スキームのサポート
  - 条件判定による[URLの書換え](https://ja.wikipedia.org/wiki/URL_rewriting "wikilink")(mod_rewrite)
  - [OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")を介した[SNI](https://ja.wikipedia.org/wiki/SNI "wikilink")サポート付きの[TLS/SSL](../Page/Transport_Layer_Security.md "wikilink")
  - [LDAPによる認証](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")
  - [RRDtool](https://ja.wikipedia.org/wiki/RRDtool "wikilink")による統計情報
  - ルールで管理されたダウンロード
  - Server Side Includes (サーバー側のCGIは含まれません)\[6\]
  - バーチャルホスト
  - モジュール機構
  - キャッシュメタ言語(現在mod_magnet に置き換えられています)\[7\] [Lua](../Page/Lua.md "wikilink")を使用
  - 最小限のWebDAVのサポート
  - [サーブレット](https://ja.wikipedia.org/wiki/サーブレット "wikilink")(AJP)サポート(バージョン1.5.x以降)
  - mod_compress および新しいmod_deflate (1.4.42)を使用したHTTP圧縮
  - 軽量(1MB未満)\[8\]
  - 複数のスレッドのみを使用する単一プロセス設計 - 接続ごとにプロセスまたはスレッドは開始されない

## 制限事項

1.4.40より前のバージョンは、X-Sendfileが使用されない限り、[CGI](../Page/Common_Gateway_Interface.md "wikilink")、[FastCGI](../Page/FastCGI.md "wikilink")、または[プロキシ](../Page/プロキシ.md "wikilink")\[9\]からの大きなファイルの送信を公式にサポートしていない。 この制限はlighttpd 1.4.40で削除された\[10\]。

[HTTP/2](https://ja.wikipedia.org/wiki/HTTP/2 "wikilink")または[HTTP/3](https://ja.wikipedia.org/wiki/HTTP/3 "wikilink")のサポートなし

## 使用法・事例

lighttpd は多くのトラフィックの多い[WEBサイト](https://ja.wikipedia.org/wiki/WEBサイト "wikilink")で使用されており、その中には[Bloglines](../Page/Bloglines.md "wikilink")と[Xkcd](https://ja.wikipedia.org/wiki/Xkcd "wikilink")がある\[11\]。過去に[Meebo](https://ja.wikipedia.org/wiki/Meebo "wikilink")と[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")で使用されていた\[12\]。[ウィキメディア財団](../Page/ウィキメディア財団.md "wikilink")はlighttpd サーバも実行している\[13\]\[14\]\[15\]\[16\]。

## 参照

  - [Webサーバソフトウェアの比較](https://ja.wikipedia.org/wiki/Webサーバソフトウェアの比較 "wikilink")
  - [インターネットキャッシュプロトコル](https://ja.wikipedia.org/wiki/インターネットキャッシュプロトコル "wikilink")
  - [プロキシサーバ](https://ja.wikipedia.org/wiki/プロキシサーバ "wikilink") - クライアント側プロキシについての説明
  - [リバースプロキシ](../Page/リバースプロキシ.md "wikilink") - オリジン側プロキシについての説明
  - [トラフィックサーバ](https://ja.wikipedia.org/wiki/トラフィックサーバ "wikilink")
  - [Webアクセラレータ](https://ja.wikipedia.org/wiki/Webアクセラレータ "wikilink") - ホストベースのHTTPアクセラレーションについての説明

## 脚注

<references />

## 外部リンク

  - lighttpd の公式[Webサイト](https://www.lighttpd.net/)、[ドキュメント](https://redmine.lighttpd.net/projects/lighttpd/wiki/Docs)、[ブログ](https://blog.lighttpd.net/)
  - [Lighttpd for Windows (Windowsに移植されたlighttpd)](https://www.kevinworthington.com/category/computers/lighttpd/)
  - [freshmeatのページ](http://freshmeat.net/projects/lighttpd/)
  - [lighttpdを知っていますか？ | Think IT（シンクイット）](https://thinkit.co.jp/article/119/1)
  - [lighttpdでユーザー認証を行うには（Digest認証編） － ＠IT](https://www.atmarkit.co.jp/flinux/rensai/linuxtips/850lighttpddigest.html)
  - [Webサーバ「lighttpd」でWebDAVを使うには － ＠IT](https://www.atmarkit.co.jp/flinux/rensai/linuxtips/848lighttpddav.html)

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  .
2.  .
3.  Gabriel Kerneis and Juliusz Chroboczek. [*Are events fast?*](http://www.pps.jussieu.fr/~jch/research/cpc-bench.pdf). PPS technical report, University of Paris 7. 2009.
4.  .
5.
6.  [Lighttpd - Bug \#1101: SSI include virtual does not run cgi](http://redmine.lighttpd.net/issues/show/1101) – lighty labs
7.  <http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModMagnet>
8.
9.
10.
11.
12.
13.
14.
15.
16.