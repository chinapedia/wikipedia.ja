> この記事は[Native POSIX Thread Library](https://ja.wikipedia.org/wiki/Native_POSIX_Thread_Library)から翻訳されています。


**Native POSIX Thread Library**（**NPTL**）とは、[POSIXスレッド](https://ja.wikipedia.org/wiki/POSIXスレッド "wikilink")を使ったプログラムを[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")上で効率的に動作可能とするソフトウェア機能である。

評価結果によると、[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")上で2秒間で10万[スレッドを起動できる](../Page/スレッド_\(コンピュータ\).md "wikilink")。同じ事を NPTL を使わないで行うと、約15分かかった\[1\]\[2\]。

## 歴史

Linuxカーネル 2.4 以前では、[プロセス](../Page/プロセス.md "wikilink")がスケジュール対象であり、[スレッドはカーネルでは扱われていなかった](../Page/スレッド_\(コンピュータ\).md "wikilink")。しかし、2.6 で `clone()` [システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")がサポートされ、アドレス空間を共有したプロセスのコピーを作成できるようになった。[LinuxThreads](https://ja.wikipedia.org/wiki/LinuxThreads "wikilink")プロジェクトはこのシステムコールを使って、カーネルレベルのスレッドをサポートした（それ以前のLinuxでは、POSIXスレッドは[ユーザーランド](https://ja.wikipedia.org/wiki/ユーザーランド "wikilink")で実装されていた）。しかし、POSIXに完全準拠するには問題が多く、特に[シグナル制御](https://ja.wikipedia.org/wiki/シグナル_\(Unix\) "wikilink")、[スケジューリング](../Page/スケジューリング.md "wikilink")、プロセス間[同期プリミティブ](https://ja.wikipedia.org/wiki/同期プリミティブ "wikilink")に問題があった。

LinuxThreads の改善には、カーネルサポートとスレッドライブラリの書き換えが必要であることは明らかであった。この要求を満たすべく、2つの競合するプロジェクトが開始された。NGPT（Next Generation POSIX Threads）は[IBM](../Page/IBM.md "wikilink")を中心とするチームが行い、NPTL は[レッドハット](../Page/レッドハット.md "wikilink")が行った。NGPT は[2003年](../Page/2003年.md "wikilink")中ごろに中止となり、同じころ NPTL がリリースされた。

NPTL は Red Hat Linux 9 で最初にリリースされた。従来の Linux でのPOSIXスレッドは、プロセッサが空いていても使えないことがあり、Windows の方が実装としては優れているとされていた。レッドハットは NPTL がこの問題を解決したと[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に関するウェブサイトの記事で主張した。

NPTL は [Red Hat Enterprise Linux](https://ja.wikipedia.org/wiki/Red_Hat_Enterprise_Linux "wikilink") のバージョン3から搭載され、現在では [GNU Cライブラリの一部となっている](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink")。

## 設計

NPTL では、カーネルには依然としてプロセスをスケジューリング対象としているように見せ、スレッドを `clone()` [システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")で生成する（NPTLライブラリから呼び出す）。ただし、カーネルサポートが必要な同期プリミティブなどを新たに追加している。このプリミティブを futex と呼ぶ。

NPTL は、いわゆる 1×1 スレッドライブラリであり、ユーザーが `pthread_create()` で生成するスレッドは全てカーネル内のプロセスに対応している。これはスレッド実装としては最も単純である。

NPTL の 1×1 モデル以外に、m×n モデルがあり、その場合はユーザーランドのスレッド数がカーネル内でスケジュール対象となるスレッド数よりも多くなる。この場合、スレッドライブラリがユーザースレッドのスケジューリングを行う。スレッド間の[コンテキストスイッチ](https://ja.wikipedia.org/wiki/コンテキストスイッチ "wikilink")が非常に高速になるが、ユーザーランドとカーネルの二段階でスケジュールを管理することで複雑さが増し、[優先順位の逆転](https://ja.wikipedia.org/wiki/優先順位の逆転 "wikilink")も起きやすくなる。

## 関連項目

  - [ライブラリ](../Page/ライブラリ.md "wikilink")

## 脚注

## 外部リンク

  - [NPTL Trace Tool](http://nptltracetool.sourceforge.net/) NPTLを使ったマルチスレッド・アプリケーションのトレースおよびデバッグツール（オープンソース）
  - [Linux threading models compared: LinuxThreads and NPTL](http://www-128.ibm.com/developerworks/linux/library/l-threading.html?ca=dgr-lnxw07LinuxThreadsAndNPTL)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")

1.  [Introducing the 2.6 Kernel](http://www.linuxjournal.com/article/6530) LINUX Journal、2003年5月1日
2.  [The Native POSIX Thread Library for Linux](http://people.redhat.com/drepper/nptl-design.pdf) Red Hat, Inc. 2005年2月21日