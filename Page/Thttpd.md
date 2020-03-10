> この記事は[Thttpd](https://ja.wikipedia.org/wiki/Thttpd)から翻訳されています。


**thttpd** (tiny/turbo/throttling HTTP server) は[オープンソース](../Page/オープンソース.md "wikilink")の[Webサーバ](../Page/Webサーバ.md "wikilink")で、シンプルで使用メモリが少なく高速に動作するように設計されている。開発は[ACME Laboratories](https://ja.wikipedia.org/wiki/ACME_Laboratories "wikilink")。より高機能なWebサーバの単純置き換えとして使えるが、静的データへの大量のリクエストをあつかうのにとても適している。例えば、画像置き場サーバ。 最初の文字の"t" は tiny、turbo、throttling を表している。

thttpd は[Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink") を初めとする他の[オープンソース](../Page/オープンソース.md "wikilink")のWebサーバソフトウェアにはない[帯域幅調整](../Page/帯域幅調整.md "wikilink")機能を持っている(Apacheでは[アドインモジュール](http://www.snert.com/Software/mod_throttle/)で帯域幅調整を使うことも出来る)。 この機能を使うと、ある特定のファイルタイプを持つファイルの最大転送速度を制限することが出来る。 例えば、サーバ管理者は[JPEG](../Page/JPEG.md "wikilink")画像ファイルを最大20[キロバイト](https://ja.wikipedia.org/wiki/キロバイト "wikilink")/秒に制限することが可能だ。こうすることで接続が飽和状態に陥るのを防ぐことができ、ファイル転送速度の減少と引き替えに、高負荷がかかった状態でもなおレスポンス可能な状態を保てる。

thttpdには兄弟プロジェクトとして[mini_httpd](https://ja.wikipedia.org/wiki/mini_httpd "wikilink") と [micro_httpd](https://ja.wikipedia.org/wiki/micro_httpd "wikilink") がある。

## 脚注

<references />

## 外部リンク

  - [thttpd web site](http://www.acme.com/software/thttpd/)
  - [Description of throttling in thttpd documentation](http://www.acme.com/software/thttpd/thttpd_man.html#THROTTLING)
  - [thttpd, unofficial resources (links, patches, etc.)](http://xoomer.virgilio.it/adefacc/httpd/thttpd/)
  - [Rob's THTTPD Changes](http://rekl.yi.org/thttpd/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink")