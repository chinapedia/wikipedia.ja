> この記事は[DPMI](https://ja.wikipedia.org/wiki/DPMI)から翻訳されています。


**DPMI** () は、[マルチタスク](../Page/マルチタスク.md "wikilink")OS（又は擬似マルチタスクOS）の[仮想DOSマシン](https://ja.wikipedia.org/wiki/仮想DOSマシン "wikilink")の環境下で[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")（主として[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")）の実行環境を提供する規格である。

## 概要

[MS-DOS](../Page/MS-DOS.md "wikilink")の次世代OSとなる[マルチタスク](../Page/マルチタスク.md "wikilink")OS（又は擬似マルチタスクOS）の仮想DOSマシンの環境下で、メモリ保護等のマルチタスク環境で必須のシステム保護を行った上でプロテクトモードアプリケーションの実行環境を提供する規格がDPMIである。

[マルチタスク](../Page/マルチタスク.md "wikilink")OSの環境下では、メモリ上に複数のアプリケーションを同時に読み込むことが出来るが、そのためにはメモリ領域の棲み分けをする以外に、バグや悪意のあるアプリケーションがメモリ上に読み込まれたとしても、他のアプリケーションのためのメモリ領域等のシステムリソースを破壊しないようにOSレベルでのシステム保護が必要である。

DPMIはシステム保護という目的を達成するためにプロテクトモードアプリケーションを特権レベル1‐3で実行させる。DPMIアプリケーションは特権命令を直接利用することが出来ないので、DPMIサーバーが全てのプロテクトモードに関する管理を引き受けるため、[VCPI](../Page/VCPI.md "wikilink")と比べて多くのファンクションコールを提供する。結果としてDPMIは[VCPI](../Page/VCPI.md "wikilink")よりもかなり重い環境になった。

しかしながら、DPMIサーバーが重くなった反面、DPMI専用クライアントはそれまでの一般的な[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")より遥かに軽くなったというメリットもあった。

なお、DPMIはVCPIを拡張した規格であるという誤解が一部にあるが、DPMIは実際にはVCPIとの互換性は無く独立した規格である。VCPI (**Virtual** Control Program Interface) は文字通り[i386の](../Page/Intel_80386.md "wikilink")[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を利用した規格であるため386以上のCPU ([IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")) 搭載が必須であるが、DPMIは一部の機能を除き[80286上でも動作する規格である](../Page/Intel_80286.md "wikilink")。

## DPMIの問題点

DPMIの最大の問題点は、登場時期が遅すぎたことである。

DPMI0.9の最初の実装は、[Windows 3.0](../Page/Microsoft_Windows_3.x.md "wikilink") である。

Windows は[GUIばかりでは無く](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、プロテクトメモリへのアクセスもアプリケーションに提供した。MS-DOS のメモリ不足の解消方法の選択肢に Windows アプリケーションが加わったのである。このため、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")のあるアプリケーションを新規に開発する場合には、わざわざDPMIアプリケーションとして開発するのではなく、Windowsアプリケーションとして開発する方がその将来性を考えて望ましい時期に入っていた。

（ただし既存のDOSエクステンダや既存のプロテクトモードアプリケーションをDPMIに対応させることは、それらの製品寿命を延ばす意味があるので価値があった。また[コンパイラ](../Page/コンパイラ.md "wikilink")やリンカー等のようにファイルしかアクセスしないアプリケーションを新規に開発することにも意味があった）

また、最初に公開された仕様のバージョンが0.9であるということも問題であった。DPMIの最初の仕様が1.0では無く0.9であった理由は、機能不足であったためである。事実、DPMI 0.9公開後、各DOSエクステンダのベンダは、自社のDOSエクステンダをDPMI 0.9に対応させたが、DPMI 0.9の機能不足を補うために、[仮想デバイスドライバ](https://ja.wikipedia.org/wiki/仮想デバイスドライバ "wikilink") (VxD) を同時に開発したところが少なくなかった。

例えば PharLap社は、386|DOS-Extenderをバージョン4.0からDPMIをサポートするようになったが、386|DOS-ExtenderをWindowsで動作させる時に起こる問題に対応するためにVxDドライバ PHARLAP.386を同時に開発した。

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")
  - [VCPI](../Page/VCPI.md "wikilink") (Virtual Control Program Interface)
  - [EMS](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink") (Expanded Memory Specification)
  - [XMS](https://ja.wikipedia.org/wiki/XMS "wikilink") (Extended Memory Specification)
  - [プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")

## 参考文献

  - 『MS-DOSメモリ管理ソフト技法-メモリ常駐ソフト&拡張メモリ活用プログラミング』 (CQ出版、1990年), ISBN 978-4-7898-3484-1
  - 「インターフェース 1990年9月号」（CQ出版）
  - 「インターフェース 1993年10月号」（CQ出版）
  - [Duncan, Ray](https://ja.wikipedia.org/wiki/Duncan,_Ray "wikilink") (1992). *Extending-DOS*:A Programmer's Guide to Protected-Mode DOS (Addison-Wesley), ISBN 0-201-56798-9

[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")