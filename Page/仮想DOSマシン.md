> この記事は[仮想DOSマシン](https://ja.wikipedia.org/wiki/仮想DOSマシン)から翻訳されています。


**仮想DOSマシン**(Virtual DOS Machine:VDM)とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Windows等に実装された](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[IA-32](../Page/IA-32.md "wikilink")の[仮想86モード](../Page/仮想86モード.md "wikilink")を利用した[MS-DOS](../Page/MS-DOS.md "wikilink")システムコールが利用可能な環境のことである。

## Windows 9x系での仮想DOSマシン

Windowsには仮想マシンと呼ばれる概念があり、これは一般的によく使われているハードウェアエミュレーションを行う仮想マシンとは別のものである。Windows 9xには「システム仮想マシン」と「仮想DOSマシン」と呼ばれる２つのタイプの仮想マシンが存在する。システム仮想マシンは一つだけ作成され、OSとすべてのWin16アプリとWin32アプリはシステム仮想マシン上で動作する。（なおWin32アプリはそれぞれ独立してメモリアドレス空間で動作し、16ビットWindowsアプリは互換性のためにすべてのアプリケーションでメモリアドレス空間を共有している。）\[1\] \[2\]

Windows 9x系は一部を除きOSは32ビットされており、OS自体がMS-DOSのシステムコールを直接呼び出すことはない。ただし必要な場合はMS-DOSの機能をレガシードライバとして利用することが出来る。Windows 9x系でDOSプロンプトを起動するとDOSプロンプトごとに独立した仮想DOSマシンが作成され[command.com](https://ja.wikipedia.org/wiki/command.com "wikilink")が実行される。この仮想DOSマシンの環境からMS-DOSの機能を使うことが出来る。

## NT系での仮想DOSマシン

[Windows NT系のOSに於いては](../Page/Windows_NT系.md "wikilink")、カーネルとユーザランドにおいて完全に32ビット化されておりMS-DOSの機能は完全に含まれていない。この上で、DOSアプリケーションを動作させる場合や16ビットWindowsアプリケーションを実行する場合、NTVDMと呼ばれるアプリケーションが起動し、そのプロセス内に仮想空間が作られ16ビットアプリケーションが実行される。なおCPUを64ビットそのモードで動作させた場合は仮想86モードが使えないため、64ビット版WindowsにはNTVDMは存在しない。

NTVDMはINT 21h/AH=30(Get DOS VERSION)では5.00を返す\[3\]。

なお、64ビットのWindowsが動くCPU及びそのモードでは仮想86モードが使えないため、64ビット版WindowsにはNTVDMは存在しない。

## OS/2での仮想DOSマシン

[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")バージョン1.xでは、DOSアプリケーションはリアルモードで動作し、同時に１つのDOSアプリケーションしか動作しない。正確には仮想DOSマシンではない。OS/2 1.xのDOS BOXはINT 21h/AH=30(Get DOS VERSION)では10.xを返す\[4\]。

[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")バージョン2.0以降では、仮想DOSマシンは[仮想86モード](../Page/仮想86モード.md "wikilink")を使用し、同時に複数のDOSアプリケーションを動作させることができる。MVDM（マルチ仮想DOSマシン）と呼ばれた。OS/2 1.xからDOS互換性が大幅に向上したため、IBMは、MVDMのことを"A Better DOS Than DOS"と呼んでいた。 OS/2 2.xのMVDMはINT 21h/AH=30(Get DOS VERSION)では20.xを返す\[5\]。

## 脚注

**出典**

<references />

## 関連項目

  - [DPMI](../Page/DPMI.md "wikilink")

[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.  <https://www.atmarkit.co.jp/fwin2k/special/win9xorwin2k/windows9xknlover.html>
2.  <https://www.informit.com/articles/article.aspx?p=131307&seqNum=4>
3.  [GET DOS VERSION](http://www.ctyme.com/intr/rb-2711.htm)
4.
5.