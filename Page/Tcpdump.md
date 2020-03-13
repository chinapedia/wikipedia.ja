> この記事は[Tcpdump](https://ja.wikipedia.org/wiki/Tcpdump)から翻訳されています。


**tcpdump**とは、[コマンドライン上で利用する一般的な計算機ネットワーク調査ツールである](../Page/コマンドラインインタプリタ.md "wikilink")。 tcpdumpにより、利用者はコマンドを実行した計算機がつながっているネットワーク上を流れる[TCP/IPなどのパケットを横取って](../Page/インターネット・プロトコル・スイート.md "wikilink")、表示させることが出来る。 このプログラムは開発当時にローレンス・バークリー研究所ネットワーク研究グループに所属していた[バン・ジェイコブソン](https://ja.wikipedia.org/wiki/バン・ジェイコブソン "wikilink")、Craig Leres、Steven McCanneによって書かれた。

tcpdumpはほとんどの[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上で動作する。 たとえば、[BSD系Unix](../Page/BSDの子孫.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink")、[AIX](../Page/AIX.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")などで動作する。 これらのシステムでは、tcpdumpは[pcap](https://ja.wikipedia.org/wiki/pcap "wikilink")ライブラリ上に構築されている。

[Windowsにも](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、WinDumpというソフトウェアがある。 これは、tcpdumpをWindows上で動くようにしたものである。

Unix系オペレーティングシステムやその他の多くのオペレーティングシステムでは、 tcpdumpを使うには[スーパーユーザー](../Page/スーパーユーザー.md "wikilink")になる必要がある。 なぜなら、tcpdumpは[プロミスキャス・モード](../Page/プロミスキャス・モード.md "wikilink")を利用するからである。 -Z オプションを使うことで、キャプチャをセットアップした後で[スーパーユーザー](../Page/スーパーユーザー.md "wikilink")権限を破棄することができる。 また別のUnix系オペレーティングシステムでは[スーパーユーザー](../Page/スーパーユーザー.md "wikilink")権限なしでパケットキャプチャのメカニズムを利用できるように設定できる。

tcpdumpを使うときには、 いくつかのフィルターを出力に適応して見ることが出来る。 こうすることで、大量の通信が行われているようなネットワークでもより簡単にパケットの調査をすることができるようになる。

## tcpdumpの主な利用目的

  - ネットワーク通信を行うプログラムのデバッグを行うため。
  - ネットワーク設定の確認のため。具体的には、必要なルーティングが正確に行われているかを調べ、問題を特定するのに使うことができる。
  - 他の利用者や計算機の通信を横取り、表示するため。[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink")や[HTTPのようなプロトコルはネットワークに平文で情報を流すため](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[ルーター](../Page/ルーター.md "wikilink")や[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")の管理者はtcpdumpを用いてログインIDやパスワード、URLなどの様々な情報を得ることが出来る。

## 参考

  - [Wireshark](../Page/Wireshark.md "wikilink")とは[GUIのフロントエンドを持った同様のツールであり](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、様々なフォーマット、ソート、表示方法に対応している
  - [tshark](https://ja.wikipedia.org/wiki/tshark "wikilink")はWiresharkのCLIフロントエンドである
  - [Ethereal](https://ja.wikipedia.org/wiki/Ethereal "wikilink")はWiresharkの元になったプログラムである
  - [snoopは](https://ja.wikipedia.org/wiki/snoop_\(software\) "wikilink")[Solaris](../Page/Solaris.md "wikilink")上で利用できる同様のプログラムである
  - [Packet sniffer](https://ja.wikipedia.org/wiki/Packet_sniffer "wikilink")

## 脚注

## 外部リンク

  - [tcpdump (および libpcap)オフィシャルサイト](https://www.tcpdump.org/)
  - [WinDumpオフィシャルサイト](https://www.winpcap.org/windump/)
  - [ngrep](http://ngrep.sourceforge.net/)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:ネットワーク・アナライザ](https://ja.wikipedia.org/wiki/Category:ネットワーク・アナライザ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")