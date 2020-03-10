> この記事は[VCPI](https://ja.wikipedia.org/wiki/VCPI)から翻訳されています。


**VCPI** (Virtual Control Program Interface) は[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")の[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を使用してソフトウェア的に実現したEMSマネージャーとプロテクトモードアプリケーション(主として[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink"))を共存させるための規格である。

## 概要

[MS-DOS](../Page/MS-DOS.md "wikilink")では、アクセス可能な[アドレス空間](https://ja.wikipedia.org/wiki/アドレス空間 "wikilink")（コンベンショナルメモリ）は、最大でも640KB (IBM PC互換機および[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")等) から768KB (PC-H98等) であった。やがてメモリ容量が不足してくると、ハードウェアによる[バンク切り換え](https://ja.wikipedia.org/wiki/バンク切り換え "wikilink")機能を持つ専用メモリカードを利用して[EMS等のメモリ拡張方法が利用され始めた](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")。一方、[80286](https://ja.wikipedia.org/wiki/80286 "wikilink")上位互換のCPUでは[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")が利用できるために、メモリ不足を補う方法としてソフトウェアエミュレーション技術を使用した[EMS](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink") (ソフトウェアEMS) や[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")が登場した。

ところが、[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")の[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を使用したソフトウェアEMSの環境下では、次のような問題が発生したためにDOSエクステンダを動作することが出来なかった。

  - [MS-DOS](../Page/MS-DOS.md "wikilink")が[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")で動作しているために、[リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")から[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")への切替えを想定されて開発された[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")は、特権命令を使用できないため[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")へ切替える方法が無かった。
  - ソフトウェアEMSが全ての[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")を獲得してしまうために[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")が利用可能な[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")が存在しなかった。
  - [プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")環境下では、割り込みコントローラーは[リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")と異なる設定をしなくてはならないが、標準的な管理方法が無かった。

そこでこれらの問題を解決して、[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を使用した[EMSマネージャーとDOSエクステンダを共存させるための規格が](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")、EMSマネージャーのメーカである Quarterdeck Office Systems とDOSエクステンダのメーカーである Phar Lap Software, Inc. の間で策定された。

これが VCPI である。

VCPIはLIM-EMS 4.0 規格の int 67h ファンクションコールを拡張する形でEMSマネージャーにVCPI サーバが実装され、VCPIサーバのファンクションコールをDOSエクステンダが呼び出すことにより、DOSエクステンダは[プロテクトメモリ](https://ja.wikipedia.org/wiki/プロテクトメモリ "wikilink")の獲得、割り込みコントローラーの設定、[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")と[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")間のモード遷移を行う。

VCPIは極めて簡素であるために EMSマネージャー、[DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")の両者共に最小限の修正で実現が可能だった。しかしながら、VCPI は[プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")アプリケーションを特権レベル0で動作をさせてしまうために、[マルチタスク](../Page/マルチタスク.md "wikilink")OSの[仮想DOSマシン](https://ja.wikipedia.org/wiki/仮想DOSマシン "wikilink")でサポートする規格としてはセキュリティー等の問題があるために不適だった。

## 関連項目

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [EMS](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink") (Expanded Memory Specification)
  - [XMS](https://ja.wikipedia.org/wiki/XMS "wikilink") (Extended Memory Specification)
  - [DPMI](https://ja.wikipedia.org/wiki/DPMI "wikilink") (DOS Protected Mode Interface)
  - [DOSエクステンダ](https://ja.wikipedia.org/wiki/DOSエクステンダ "wikilink")
  - [プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")

## 参考文献

  - 『MS-DOSメモリ管理ソフト技法-メモリ常駐ソフト&拡張メモリ活用プログラミング』（CQ出版、1990年）, ISBN 978-4789834841
  - 「インターフェース 1990年9月号」（CQ出版）
  - 「インターフェース 1993年10月号」（CQ出版）
  - [Duncan, Ray](https://ja.wikipedia.org/wiki/Duncan,_Ray "wikilink") (1992). *Extending-DOS*:A Programmer's Guide to Protected-Mode DOS (Addison-Wesley), ISBN 0-201-56798-9

## 外部リンク

  - [VCPI Specification version 1.0](http://standards.mithrill.org/vcpi.doc)

[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")