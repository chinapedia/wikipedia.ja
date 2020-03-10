> この記事は[Gtk-vnc](https://ja.wikipedia.org/wiki/Gtk-vnc)から翻訳されています。


**gtk-vnc**とは、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")を用いた[VNC](https://ja.wikipedia.org/wiki/Virtual_Network_Computing "wikilink") Viewerライブラリを提供する[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトで、 VNC用の共通[APIを提供する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。 このライブラリを使うことにより、VNC viewerを数十行程度で実装することが出来る。

また、通常のVNCの認証プロトコルに加えて、 IPv6のサポートや、 VeNCrypt拡張によるTLS/SSLによる暗号化通信がサポートされている。

現在は、C言語及びPythonから本APIを呼び出すことが出来る。 また、他の使い方としては、VNC viewerのプラグインとして、Webブラウザから使うことが出来る。

本ライブラリを使っているアプリケーションとしては、Vinagre、[Virtual_Machine_Manager](https://ja.wikipedia.org/wiki/virt-manager "wikilink")、KVM Testなどがある。また、gtkvnc配布パッケージに添付されているCとPythonで書かれたgvncviewerもある。

本プロジェクトのメンテナーは、Anthony Ligori、Daniel Berrange、John Wendellである。

## ステータス

gtk-vncは、以下のエンコーディングをサポートしている。

  - Raw
  - Copyrect
  - RRE
  - Hextile
  - ZRLE
  - Tight

さらに、以下の擬エンコーディングをサポートしている。

  - DesktopResize
  - PointerChangeType
  - RichCursor
  - XCursor
  - ExtendedKeyEvent

以下のセキュリティタイプ(認証)をサポートしている。

  - None
  - VNC Auth
  - VeNCrypt

RFBプロトコルは、3.3, 3.7, そして3.8をサポートしている。

## TODOリスト

  - リモートゲストとのAudio/USB/Dataをやり取りする機能追加
  - スケールするフレームバッファサポート
  - スループットを向上するために動的にプロトコル(圧縮等)を変更できる機能追加
  - APIドキュメント
  - サムネイル(小さい描画)サポート
  - フレームバッファをN秒以上の間隔で要求する'Quiesced' モードサポート(サムネイルサポート用)

## ソフトウェア構成

ソフトウェアの構成は、大まかに言って、3つに分かれている。一つは、examples/gvncviewer.cであり、VNC viewerのメインルーチンである。次は、GTK-VNC widgetとなるsrc/vncdisplay.cである。最後は、vnc_coroutine()@src/vncdisplay.cから呼び出されるsrc/gvnc.cというVNCのネットワーク通信プロトコル層である。このvnc_coroueine()は、メインとは別スレッド([コルーチン](https://ja.wikipedia.org/wiki/コルーチン "wikilink"))として稼働している。 また、ソフトウェア規模は、1万行程度であり、比較的小さい。

動作は、2つのスレッドが、交互に動く形になっている。1つは、グラフィックインターフェースのメインスレッドであり、もう1つはネットワーク通信のvnc_coroutine()である。 vnc_coroutine()は、coroutine_yieldでCPUを離し、メインスレッドにCPUを譲る。そして、I/O割り込みが上がったり、メインスレッドの処理が一段落しCPUが空くなどのある一定条件を満たすと、coroutine_yieldto()が実行され、メインスレッドからCPUを奪う過程を繰り返す。

## 外部リンク

  - [gtk-vncの本家ページ](http://gtk-vnc.sourceforge.net/)
      - [開発コード](http://gtk-vnc.codemonkey.ws/hg/outgoing.hg/)
      - [デイリービルド状況](http://builder.virt-manager.org/module-gtk-vnc--devel.html)
      - [Windowsでのサポート状況](https://bugzilla.redhat.com/show_bug.cgi?id=467421)
  - [Vinagre(GNOME)](http://www.gnome.org/projects/vinagre/)
  - [VeNCrypt](http://sourceforge.net/projects/vencrypt)

### メンテナ

  - [Anthony Ligoriのページ](http://blog.codemonkey.ws/)
  - [Berrangeのページ](http://berrange.com)
  - [John Wendell](http://www.bani.com.br/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")