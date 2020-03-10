> この記事は[Lighttpd](https://ja.wikipedia.org/wiki/Lighttpd)から翻訳されています。


**lighttpd** （ライティ\[1\]）は高速性の重視される環境に最適化された、安全・高速で標準に準拠し、柔軟であることを指向して設計された[Webサーバ](../Page/Webサーバ.md "wikilink")である。

メモリ消費量が少なく、[CPU](../Page/CPU.md "wikilink")負荷の少ない高速動作が目的となっているため、負荷が問題な場合や、静的コンテンツを動的コンテンツと区別して送信する場合などに適しているとされる。

## 特徴

  - [FastCGI](https://ja.wikipedia.org/wiki/FastCGI "wikilink")、[SCGI](https://ja.wikipedia.org/wiki/Simple_Common_Gateway_Interface "wikilink")、[CGI](../Page/Common_Gateway_Interface.md "wikilink")
  - FastCGIとSCGIの[ロードバランシング](https://ja.wikipedia.org/wiki/ロードバランシング "wikilink")
  - [メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")使用量の安定性
  - [`chroot`](https://ja.wikipedia.org/wiki/chroot "wikilink")システムコールの使用
  - `select`や`poll`システムコールの使用
  - より効率的な`kqueue`や`epoll`のようなイベント通知のスキーム
  - 条件判定によるURLの書換え
  - [TLS通信](../Page/Transport_Layer_Security.md "wikilink")
  - [LDAPサーバによる](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")[認証](../Page/認証.md "wikilink")
  - [rrdtool](https://ja.wikipedia.org/wiki/rrdtool "wikilink")による統計情報
  - [ルール](https://ja.wikipedia.org/wiki/ルール "wikilink")で管理されたダウンロード
  - [Server Side Includes](https://ja.wikipedia.org/wiki/Server_Side_Includes "wikilink")
  - バーチャルホスト
  - モジュール機構
  - [Cache Meta Language](https://ja.wikipedia.org/wiki/Cache_Meta_Language "wikilink")
  - 最小限の[WebDAV](../Page/WebDAV.md "wikilink")のサポート

## 脚注

<references />

## 外部リンク

  - lighttpdの[Webサイト](http://www.lighttpd.net/)、[フォーラム](http://forum.lighttpd.net/forum/1)、[ブログ](http://blog.lighttpd.net/)
  - [WLMP Project](http://en.wlmp-project.net/) LightTPDのWindows用パッケージを頒布する
  - [Lighttpd for Windows (Windowsに移植されたlighttpd)](http://www.kevinworthington.com/category/computers/lighttpd/)
  - [freshmeatのページ](http://freshmeat.net/projects/lighttpd/)

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  .