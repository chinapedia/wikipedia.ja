> この記事は[GNUの派生](https://ja.wikipedia.org/wiki/GNUの派生)から翻訳されています。


**GNUの派生**（**GNU ディストリビューション**または**GNU ディストロ**とも呼ばれる）は、[GNU](../Page/GNU.md "wikilink") [OS](../Page/OS.md "wikilink")（[Hurd](https://ja.wikipedia.org/wiki/Hurd "wikilink")カーネル、GNU Cライブラリ、システムライブラリ、GNU Coreutils、[bash](https://ja.wikipedia.org/wiki/bash "wikilink")、[GNOME](../Page/GNOME.md "wikilink")、[GNU Guixなど](../Page/GNU_Guix.md "wikilink")）をベースとした[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")である\[1\]\[2\]\[3\]\[4\]\[5\]。GMUプロジェクトによると、これには[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")を使うオペレーティングシステムの大部分と、多少の[BSD](../Page/BSD.md "wikilink")ベースのカーネルを使うオペレーティングシステムが含まれる\[6\]\[7\]。

GNUのユーザーは、通常OSをダウンロードして用いるが、このOSは、組み込みデバイスからPC、スーパーコンピューターにいたるまで、様々なシステムで利用可能である。

## Hurdカーネル

[Gnu_hurd_debian_1.png](https://ja.wikipedia.org/wiki/File:Gnu_hurd_debian_1.png "fig:Gnu_hurd_debian_1.png").\]\] Hurdは、[Linux-libre](https://ja.wikipedia.org/wiki/Linux-libre "wikilink")が公式のGNUパッケージとなる以前は、公式な形で、GNUシステムのために、GNU自身によって開発されているカーネルであった。[Debian GNU/Hurdは](https://ja.wikipedia.org/wiki/Debian_GNU/Hurd "wikilink")、Debian 7.0（Wheezy）において、テクノロジープレビューとしてリリースされることが議論されたが、これはシステムが充分に成熟していなかったため、実現しなかった\[8\]。しかしながら、Debian GNU/Hurdのメンテナは、非公式のリリースをDebian 7.0のリリース日に合わせて公開することを決断している。Debian GNU/Hurdは、依然として実務に使うためにはパフォーマンスと安定性の問題があると考えられており、同時に、JavaやX.orgのGUIとグラフィックドライバの実装が不十分であるという問題もある\[9\]。Debianパッケージのうち、3分の2がHurdに移植されている\[10\]。

Arch Hurdは、Arch Linuxの派生ディストリビューションで、これはArchをP6アーキテクチャに最適化されたパッケージとセットでGNU Hurdシステムに移植したものである。このプロジェクトのゴールは、BSDスタイルの[init](https://ja.wikipedia.org/wiki/init "wikilink")や、pacman、ローリングリリース、シンプルなセットアップなどのArch的なユーザー環境をGNU Hurdにおいて提供することであり、一時的にシステムを利用する分には充分に安定していた。しかしながら、プロジェクトは[2018年](../Page/2018年.md "wikilink")に中止された。プロジェクトは、評価目的のための[LiveCD](https://ja.wikipedia.org/wiki/LiveCD "wikilink")と、インストール利用のための文書を提供していた。

## Linuxカーネル

[Parabola_GNU+Linux-libre+GNOME+Emacs.png](https://ja.wikipedia.org/wiki/File:Parabola_GNU+Linux-libre+GNOME+Emacs.png "fig:Parabola_GNU+Linux-libre+GNOME+Emacs.png")\]\]  GNU/LinuxまたはGNU+Linuxという単語は、[FSF](https://ja.wikipedia.org/wiki/FSF "wikilink")とその支援者によって使われているが、これはLinuxカーネルとともにGNUのシステムソフトウェアを用いていることを表すためのものである。そのようなディストリビューションにおいては、Linuxカーネルに加えて、基本的なGNUパッケージとプログラムがインストールされている。これらのディストリビューションのうち、GNU/Linuxという単語を使うもので最も有名なのが[Debian GNU/Linuxである](../Page/Debian.md "wikilink")。

## BSDカーネル

[Debian_GNU_kFreeBSD_6.0_ja_JP.png](https://ja.wikipedia.org/wiki/File:Debian_GNU_kFreeBSD_6.0_ja_JP.png "fig:Debian_GNU_kFreeBSD_6.0_ja_JP.png")\]\] [Debian GNU/kFreeBSDは](https://ja.wikipedia.org/wiki/Debian_GNU/kFreeBSD "wikilink")、[IA-32](../Page/IA-32.md "wikilink")と[x86-64](https://ja.wikipedia.org/wiki/x86-64 "wikilink")アーキテクチャのコンピュータのためのOSで、[FreeBSD](../Page/FreeBSD.md "wikilink")のカーネルに、[Debian](../Page/Debian.md "wikilink")のパッケージ管理システムとGNUのソフトウェアを組み合わせた構成となっている。kFreeBSDのkは、カーネル（kernel）の省略で\[11\]、FreeBSDからはカーネルのみ完全な形で利用していることを反映している。OSは、[2011年](../Page/2011年.md "wikilink")[2月6日](../Page/2月6日.md "wikilink")にDebian Squeeze（6.0）として公式にリリースされている\[12\]。

Debian GNU/NetBSDは、GNUのユーザーランドを[NetBSD](../Page/NetBSD.md "wikilink")に移植した実験的なシステムで、公式なリリースはなされていない。IA-32\[13\]とDEC Alpha\[14\]の両アーキテクチャへの移植が進められていたが、[2002年](../Page/2002年.md "wikilink")からメンテナンスは行われておらず、現在はダウンロードも不可能である\[15\]。

## OpenSolaris (Illumos) カーネル

[Nexenta OSは](../Page/Nexenta_OS.md "wikilink")、[OpenSolaris](../Page/OpenSolaris.md "wikilink")のカーネルに、Debianのパッケージ管理システムとGNUのユーザーランド（ただし[libc](https://ja.wikipedia.org/wiki/libc "wikilink")はOpenSolarisのものが使われている）を結びつけた最初のディストリビューションである。Nexentaは、IA-32とx86-64の両アーキテクチャ向けに利用可能である。このプロジェクトはNexenta Systems Incによって始動され、また開発に対する継続的な支援がなされた\[16\]。また、先に述べたように、NexentaはOpenSolarisのlibcを用いているため、GNUの派生とは見られれないこともある。複数の[Illumos](https://ja.wikipedia.org/wiki/Illumos "wikilink")ディストリビューションはGNUのユーザーランドを標準で用いている\[17\]。

## Darwinカーネル

## Windowsカーネル

[Cygwin](../Page/Cygwin.md "wikilink")プロジェクトは、[Microsoft Windowsにおいて](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[POSIX](../Page/POSIX.md "wikilink") [API](https://ja.wikipedia.org/wiki/API "wikilink")の機能性をCライブラリの形態で提供する[互換レイヤ](https://ja.wikipedia.org/wiki/互換レイヤ "wikilink")のプロジェクトで、[GNU](../Page/GNU.md "wikilink")や他の[Unix系](../Page/Unix系.md "wikilink")のプログラムも合わせて提供されている。最初のリリースは、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に現在[Red Hatの一部であるCygnus](https://ja.wikipedia.org/wiki/Red_Hat "wikilink") Solutionsによってなされた。

[2016年](../Page/2016年.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[カノニカル](https://ja.wikipedia.org/wiki/カノニカル "wikilink")は、公式に、LinuxカーネルのシステムコールをWindows NTのものに翻訳する互換レイヤを[Windows 10に加えた](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")。これは、Windowsで[ELF](https://ja.wikipedia.org/wiki/ELF "wikilink")形式の実行ファイルを実行可能にするものであり、Web開発向けにGNUのユーザーランドを提供することを意図していた\[18\]\[19\]\[20\]。しばしば、これは"Linux for Windows"と呼ばれるが、これはLinuxカーネルを欠いたものである。

## 関連項目

  - [GNU](../Page/GNU.md "wikilink")
  - [GNU/Linux名称論争](https://ja.wikipedia.org/wiki/GNU/Linux名称論争 "wikilink")

## 脚注

### 出典

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [List of potential release architektures for Debian Wheezy](http://release.debian.org/wheezy/arch_qualify.html)
9.  [GNU Hurd news](https://www.gnu.org/software/hurd/news.html)
10. [Debian Wiki: Debian GNU/Hurd](http://wiki.debian.org/Debian_GNU/Hurd)
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.