> この記事は[STREAMS](https://ja.wikipedia.org/wiki/STREAMS)から翻訳されています。


**STREAMS**は、[UNIX System V](../Page/UNIX_System_V.md "wikilink") の[キャラクタデバイス](https://ja.wikipedia.org/wiki/キャラクタデバイス "wikilink")の実装フレームワークである。

STREAMS は、[カーネル](../Page/カーネル.md "wikilink")やユーザ空間プロセスと[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")との全二重双方向のキャラクタI/Oを実装するモジュール性の高いアーキテクチャとして設計された。端末I/Oやネットワークサブシステムの開発によく使われた。System V Release 4 では、全ての端末インタフェースがSTREAMSを使って実装された\[1\]。

STREAMS は、プロトコルスタックを実装するための[カーネル](../Page/カーネル.md "wikilink")内の仕組みである。たとえば、TCP/IPでは、TCP や IP がそれぞれSTREAMSモジュールとして実装される。STREAMSモジュールには上位層への双方向接続ポートと下位層への双方向接続ポートを持つ。STREAMSモジュールは基本的には上位層や下位層のことを全く知らなくてもよい構造になっていて、TCPモジュールのルーチンがIPのルーチンを直接コールすることはない。

STREAMS は[BSD](../Page/BSD.md "wikilink")の[ソケット](../Page/ソケット_\(BSD\).md "wikilink")[APIと対抗する技術だが](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、STREAMSを使ったシステムでは常にソケットのインタフェースも提供された。STREAMS はソケットよりも複雑だが、柔軟性も高い。

## 歴史

STREAMS は[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")が [Version 8 Unix](../Page/Research_Unix.md "wikilink") に導入したのが最初であり、その時点で端末[I/Oと](../Page/入出力.md "wikilink")[TCP/IPプロトコルに使われていた](../Page/インターネット・プロトコル・スイート.md "wikilink")。当時のUNIXの入出力[システムコール](../Page/システムコール.md "wikilink")（*open*、*close*、*read*、*write*、*ioctl*）に新たな機能を導入しようとする試みであったが\[2\]、その応用は端末I/Oとパイプ状のI/O意味論を提供するプロトコル群に限定されていた。その後、Robert Israel、Gil McGrath、Dave Olander、Her-Daw Che、 Maury Bach らが System V Release 3 に移植し、様々なトランスポート層プロトコル（TCP/IP、ISO Class 4 transport、[SNA](../Page/Systems_Network_Architecture.md "wikilink") LU 6.2、[RFS](https://ja.wikipedia.org/wiki/Remote_File_System "wikilink") で使う [AT\&T](../Page/AT&T.md "wikilink") NPACK protocol）を STREAMS で実装できるよう拡張された\[3\]。これはまず、UNIX System V Release 3 の Network Support Utilities (NSU) パッケージと共にリリースされた\[4\]。この時点で、*putmsg*、*getmsg*、*poll* という[システムコール](../Page/システムコール.md "wikilink")が追加された。これらはそれぞれ、BSDソケットの *send*、*recv*、*select* システムコールに相当するが\[5\]、名前空間の衝突を避けるために別の名前を付けている\[6\]。System V Release 4 では、STREAMS は端末I/Oフレームワークや[パイプの実装にも使われ](../Page/パイプ_\(コンピュータ\).md "wikilink")、双方向パイプや[ファイル記述子](../Page/ファイル記述子.md "wikilink")の受け渡しといった便利な機能が追加された\[7\]。[UNICOS](https://ja.wikipedia.org/wiki/UNICOS "wikilink")への移植も行われている。

[ベル研究所](../Page/ベル研究所.md "wikilink")によるオリジナルの実装\[8\]は遅いという悪評があったが、SVR3 やその後の実装では特に性能が悪いという話はない。

SVR3への移植と並行して、[AT\&T](../Page/AT&T.md "wikilink") は[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の各層（2層から4層まで）についてのSTREAMSメッセージパッシングの（プロトコルに依存しない）ガイドラインを開発した。

  - [データリンク層](../Page/データリンク層.md "wikilink") - DLPI (Data Link Provider Interface)\[9\]
  - [ネットワーク層](../Page/ネットワーク層.md "wikilink") - NPI (Network Provider Interface)\[10\]
  - [トランスポート層](../Page/トランスポート層.md "wikilink") - TPI (Transport Provider Interface)\[11\]

しかし、ネットワーク層とトランスポート層の間は[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")の実装に依存する部分が大きく、また上位層 (5-7) は[カーネル](../Page/カーネル.md "wikilink")では実装されないことから、[データリンク層](../Page/データリンク層.md "wikilink")\[12\]と[トランスポート層](../Page/トランスポート層.md "wikilink")\[13\]がそれぞれの上位層に見せるSTREAMSインタフェースだけが後に[X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink")によって標準化された。トランスポート層の実装に依存しないメッセージパッシング型のAPIとして [Transport Layer Interface](../Page/Transport_Layer_Interface.md "wikilink") (TLI) が定義され、後に [X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink") Transport Interface (XLI) として採用された。また、[セッション層](../Page/セッション層.md "wikilink")、[プレゼンテーション層](../Page/プレゼンテーション層.md "wikilink")、[アプリケーション層](../Page/アプリケーション層.md "wikilink")をサポートするライブラリが定義され\[14\]、後に [The Open Groupが標準化した](../Page/The_Open_Group.md "wikilink")\[15\]。

STREAMS は [Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") のバージョン1（UNIX95）とバージョン2（UNIX98）では必須とされていたが、[BSD](../Page/BSD.md "wikilink")や[Linux](../Page/Linux.md "wikilink")では採用されなかったためバージョン3（UNIX03）ではオプションとなっている。

## 実装

STREAMS は主に System V 系 UNIX で使われたが、他にも以下のような実装が存在する。

  - [Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink") も当初は STREAMS によるネットワーク機能を持っていたが、第3版へ移行する過程で単純なI/Oキューに変更された。
  - Mentat という企業がSTREAMSの実装を開発している。
      - [ノベルは](../Page/ノベル_\(企業\).md "wikilink")[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")のTCP/IPスタックの実装にMentat版のSTREAMSを使っていた。
      - [アップルコンピュータは](../Page/アップル_\(企業\).md "wikilink") Mentatの実装したSTREAMSのライセンス提供を受け、MacのOS 漢字Talk 7.5.2以降にネットワークシステム [Open Transport](../Page/Open_Transport.md "wikilink") の一部として導入した。STREAMS アーキテクチャは [Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") の[Classic環境に残っている](../Page/Classic_\(ソフトウェア\).md "wikilink")（ただし、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")ネイティヴのネットワークアーキテクチャは[BSD](../Page/BSD.md "wikilink")の[socketである](../Page/ソケット_\(BSD\).md "wikilink")）。
  - [Linuxカーネル](../Page/Linuxカーネル.md "wikilink")では、開発者らが STREAMS 技術を不適切と見ているため実装されていない。代わりに STREAMS 操作をソケット操作に変換する[互換レイヤー](../Page/互換レイヤー.md "wikilink")が存在する\[16\]。
      - [Linux](../Page/Linux.md "wikilink") での STREAMS 実装として、LiS (Linux STREAMS)\[17\] や OpenSS7 Fast STREAMS がある\[18\]。
  - [FreeBSD](../Page/FreeBSD.md "wikilink") はSVR4とのバイナリ互換性のためにSTREAMS関連システムコールをサポートしている。
  - [Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") のカーネルにはSTREAMSの完全移植版である streams.sys があった。DDK文書にはSTREAMSについての章があったが、NT4のDDKでは obsolete とされていた。

## 脚注

## 参考文献

  -
  -
  -
  -
  -
  -
## 外部リンク

  - [The original stream(4) manual from Unix 8th Edition](http://man.cat-v.org/unix_8th/4/stream)
  - [Digital UNIX STREAMS](http://alpha-supernova.dev.filibeto.org/lib/rel/4.0B/HTML/AA-PS2WD-TET1_html/netprog6.html)
  - [Sun STREAMS Programming Guide](http://docs.sun.com/app/docs/doc/806-6546) Oracle

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:System_V](https://ja.wikipedia.org/wiki/Category:System_V "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:プロセス間通信](https://ja.wikipedia.org/wiki/Category:プロセス間通信 "wikilink")

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
16. [Alan Cox](https://ja.wikipedia.org/wiki/アラン・コックス "wikilink"), [Streams and Linux](http://lkml.org/lkml/1998/6/28/138), Linux Kernel Mailing List, 28 June 1998
17. [LiS: Linux STREAMS](http://www2.linuxjournal.com/article/3086), Francisco Ballesteros, *Linux Journal*, Sat 01 May 1999
18. [OpenSS7 download page](http://www.openss7.org/download.html)