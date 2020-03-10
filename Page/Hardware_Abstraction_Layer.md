> この記事は[Hardware Abstraction Layer](https://ja.wikipedia.org/wiki/Hardware_Abstraction_Layer)から翻訳されています。


**Hardware Abstraction Layer** (**HAL**、ハードウェア抽象化レイヤー) とは、[コンピュータ](../Page/コンピュータ.md "wikilink")の[ハードウェア](../Page/ハードウェア.md "wikilink")とそのコンピュータ上で動作する[ソフトウェア](../Page/ソフトウェア.md "wikilink")の間に存在する、ソフトウェアで実装した[抽象化レイヤー](https://ja.wikipedia.org/wiki/抽象化レイヤー "wikilink")である。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の[カーネル](../Page/カーネル.md "wikilink")からハードウェア毎に異なる差異を隠蔽する機能を持ち、それによってカーネルコードは異なるハードウェアのシステム上で動作してもほとんど変更する必要がなくなる。[PCにおいては](../Page/パーソナルコンピュータ.md "wikilink")、HALは基本的に[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")用ドライバの形態をとり、上位のプログラムがハードウェアに直接アクセスする下位のコンポーネントに指示できるようにする。

## 概要

多数存在する[CPU](../Page/CPU.md "wikilink")アーキテクチャ毎の動作の違いなどがあっても、適切に設計されたHALを用意すれば動作できる。そのため、システムを開発するときにハードウェアの差異を意識することなく設計できる。これらは[NTベースのOSで用いられる技術である](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink")。[NTベースのOSには](https://ja.wikipedia.org/wiki/Windows_NT系 "wikilink")、カーネル空間にHALがあり、カーネルやドライバや実行サービスとハードウェアの仲介をする\[1\]\[2\]。これにより、Windows NT のカーネルモードのコードは各種の異なる[メモリ管理ユニット](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink")のアーキテクチャのプロセッサに移植でき、各種I/O[バスアーキテクチャのシステムに移植できるようになっている](../Page/バス_\(コンピュータ\).md "wikilink")。コードの大部分はそれらシステム上で、単にその[命令セット](https://ja.wikipedia.org/wiki/命令セット "wikilink")アーキテクチャに[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")するだけでソースコードを修正することなく実行することができる。例えば、[SGIの](../Page/シリコングラフィックス.md "wikilink") Intel x86 ベースのワークステーションは[IBM PC 互換ではないが](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")、HALのおかげで NT を実行することができた。

[BSD](../Page/BSD.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")、[DOS](../Page/DOS_\(OS\).md "wikilink")、[Solaris](../Page/Solaris.md "wikilink") といったオペレーティングシステムにもHALに相当する部分は存在しているが、明確にHALとして認識・区別されていない。Linuxなどでは、動作中のカーネルに対して[Adeos](https://ja.wikipedia.org/wiki/Adeos "wikilink")のようなHALを後から挿入することができる。[NetBSD](../Page/NetBSD.md "wikilink")はHAL層を明確に区別しており、非常に移植性が高い。このシステムは [`uvm(9)`](http://netbsd.gw.com/cgi-bin/man-cgi?uvm+9+NetBSD-current)、[`pmap(9)`](http://netbsd.gw.com/cgi-bin/man-cgi?pmap+9+NetBSD-current)、[`bus_space(9)`](http://netbsd.gw.com/cgi-bin/man-cgi?bus_space+9+NetBSD-current)、[`bus_dma(9)`](http://netbsd.gw.com/cgi-bin/man-cgi?bus_dma+9+NetBSD-current) といったサブシステムから構成される。[ISA](../Page/Industry_Standard_Architecture.md "wikilink")、[EISA](../Page/Extended_Industry_Standard_Architecture.md "wikilink")、[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")、[PCI-Eなど](https://ja.wikipedia.org/wiki/PCI_Express "wikilink")、複数のアーキテクチャで使われているI/Oバスも抽象化されており、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")も最小限の修正だけで移植可能である。

HALの極端な例として、[System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink")や[AS/400のアーキテクチャがある](https://ja.wikipedia.org/wiki/System_i "wikilink")。これらシステム上の[コンパイラ](../Page/コンパイラ.md "wikilink")の多くは抽象化された機械語コードを生成する。Licensed Internal Code (LIC) はそれを動作中のシステムのプロセッサ用コードに変換し実行させる。LIC層より上のアプリケーションやOSのコードはSystem/38からAS/400に移行する際に全く修正も再コンパイルも不要だった（System/38とAS/400では少なくとも3種類の全く異なるプロセッサが使われている）。

HALは、[カーネル](../Page/カーネル.md "wikilink")の代わりにハードウェアと直接やり取りするものであるため、そのインタフェースはOSの[APIよりも下位に存在する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。したがって、HALの処理にかかる時間はAPI（[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")）にかかる時間よりも短くなければならない。

HALが定義されたOSは各種ハードウェアに容易に移植可能である。これは非常に様々なプラットフォーム上で動作することを要求される[組み込みシステム](../Page/組み込みシステム.md "wikilink")では特に重要である。

## [DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")

Windows向けのリアルタイム[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")APIである[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")においても、[ビデオカード](../Page/ビデオカード.md "wikilink")などのグラフィックスハードウェアを抽象化するためのHALデバイス\[3\]が用意されている。ベンダー間の差異を吸収する層であるHALデバイスを利用することにより、ベンダー共通のDirect3D APIを用いてハードウェアの機能にアクセスできる。

なお、[DirectDraw](https://ja.wikipedia.org/wiki/DirectDraw "wikilink")にはドライバーを[ユーザーモード](https://ja.wikipedia.org/wiki/ユーザーモード "wikilink")でエミュレーションするためのHardware Emulation Layer (HEL) が用意されていた\[4\]。

## 脚注

## 関連項目

  - [HAL (ソフトウェア)](https://ja.wikipedia.org/wiki/HAL_\(ソフトウェア\) "wikilink")
  - [Adeos](https://ja.wikipedia.org/wiki/Adeos "wikilink")
  - [Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")
  - [ACPI](https://ja.wikipedia.org/wiki/ACPI "wikilink")
  - [UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")
  - [BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")

[Category:オペレーティングシステムの仕組み](https://ja.wikipedia.org/wiki/Category:オペレーティングシステムの仕組み "wikilink")

1.
2.
3.  [DirectX 用語集](https://msdn.microsoft.com/ja-jp/library/cc351166.aspx)
4.  [Hardware Emulation Layer (Windows Drivers)](https://msdn.microsoft.com/en-us/library/windows/hardware/ff567254.aspx)