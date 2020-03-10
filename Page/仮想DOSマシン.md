> この記事は[DOS](https://ja.wikipedia.org/wiki/DOS)から翻訳されています。


**仮想DOSマシン**(Virtual DOS Machine:VDM)とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Windows等に実装された](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")の[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を利用した[MS-DOS](../Page/MS-DOS.md "wikilink")システムコールが動作し、いくつかの周辺機器を[仮想化](https://ja.wikipedia.org/wiki/仮想化 "wikilink")した[仮想機械](../Page/仮想機械.md "wikilink")アーキテクチャである。

## 非NT系での仮想DOSマシン

非NT系のWindowsでは、いわゆる「[DOSプロンプト](https://ja.wikipedia.org/wiki/DOSプロンプト "wikilink")」で見た目には[COMMAND.COM](../Page/COMMAND.COM.md "wikilink")が起動されるが実際にはそれはシェルであり、その中身がこの環境である(こちらでは、シェル毎に仮想マシンが作られている)。[Windows 3.x](https://ja.wikipedia.org/wiki/Windows_3.x "wikilink")、[Windows 95等では](https://ja.wikipedia.org/wiki/Windows_95 "wikilink")、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")そのものに16ビットコードが残っており、ある機械で動いているWindowsのネイティブアプリケーションは全て、一つの仮想DOSマシンで動作していた。仮想マシンを実装する仮想マシンマネージャ(VMM)は、Windows3.xではWIN386.EXEでWindows 9x系ではVMM386.VXDである。この仮想DOSマシンに対して仮想的なデバイスを提供するのが、[仮想デバイスドライバ](../Page/仮想デバイスドライバ.md "wikilink")である。仮想DOSマシンにおいては、DOS自体も仮想化しており、多くの部分は調停の上DOSのシステムコールまたはデバイスへのリクエストに変換するが、一部のDOSのシステムコールは直接仮想デバイスドライバが取り扱う。代表的な例がWindows 95からサポートされたファイルシステム[VFAT](https://ja.wikipedia.org/wiki/VFAT "wikilink")である。

## NT系での仮想DOSマシン

[Windows NT系のOSに於いては](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink")、カーネルとユーザランドにおいて32ビット化されており、MS-DOSのシステムコールを使わない構成になっている。この上で、DOSアプリケーションを動作させる場合や16ビットWindowsアプリケーションを実行する場合、NTVDMと呼ばれるアプリケーションが起動し、そのプロセス内に仮想空間が作られ16ビットアプリケーションが実行される。DOSアプリケーションの場合は一つ一つ別のNTVDMが作られるが、Windowsアプリケーションの場合は、互換性のために、基本的には一つのNTVDM上で複数動作する。また安定性を重視するために別のNTVDMで動作させることも可能になった。いずれにせよ、Windows 95等との互換性は多少損なわれることになった。

NTVDMはINT 21h/AH=30(Get DOS VERSION)では5.00を返す\[1\]。

なお、64ビットのWindowsが動くCPU及びそのモードでは仮想86モードが使えないため、64ビット版WindowsにはNTVDMは存在しない。

## OS/2での仮想DOSマシン

[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")バージョン1.xでは、DOSアプリケーションはリアルモードで動作し、同時に１つのDOSアプリケーションしか動作しない。正確には仮想DOSマシンではない。OS/2 1.xのDOS BOXはINT 21h/AH=30(Get DOS VERSION)では10.xを返す\[2\]。

[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")バージョン2.0以降では、仮想DOSマシンは[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を使用し、同時に複数のDOSアプリケーションを動作させることができる。MVDM（マルチ仮想DOSマシン）と呼ばれた。OS/2 1.xからDOS互換性が大幅に向上したため、IBMは、MVDMのことを"A Better DOS Than DOS"と呼んでいた。 OS/2 2.xのMVDMはINT 21h/AH=30(Get DOS VERSION)では20.xを返す\[3\]。

## 脚注

**出典**

<references />

## 関連項目

  - [DPMI](../Page/DPMI.md "wikilink")

[Category:MS-DOS・Windows3.x・9x系](https://ja.wikipedia.org/wiki/Category:MS-DOS・Windows3.x・9x系 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.  [GET DOS VERSION](http://www.ctyme.com/intr/rb-2711.htm)
2.
3.