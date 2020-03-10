> この記事は[QEMM](https://ja.wikipedia.org/wiki/QEMM)から翻訳されています。


**QEMM** (*Quarterdeck Expanded Memory Manager*) は、[クォーターデック](https://ja.wikipedia.org/wiki/クォーターデック "wikilink")が開発した[MS-DOS](../Page/MS-DOS.md "wikilink")用[メモリマネージャ](https://ja.wikipedia.org/wiki/メモリマネージャ "wikilink")であり、[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")製のこの類の[プログラムとしては](../Page/プログラム_\(コンピュータ\).md "wikilink")（海外では）最も広く使われた。

## 製品

当初は**QEMM-386**と呼ばれ、これを補完する製品として**QRAM**があった。QRAMは[Intel 80286を使い](../Page/Intel_80286.md "wikilink")[チップス・アンド・テクノロジーズ](https://ja.wikipedia.org/wiki/チップス・アンド・テクノロジーズ "wikilink")の特定の[チップセット](../Page/チップセット.md "wikilink")を使ったマシンで同様の機能を提供した。[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink") が登場すると**386**は名称から消えた。QEMM-386と[DESQview](../Page/DESQview.md "wikilink")は連携して動作し、同梱して販売される場合は**DESQview 386**という製品名になっていた。

QEMMは、[UMA](https://ja.wikipedia.org/wiki/Upper_Memory_Area "wikilink")、[EMS](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")、[XMS](https://ja.wikipedia.org/wiki/XMS "wikilink")へのアクセスを提供する。DOSプログラムは大量のコンベンショナルメモリを必要とすることが多く、QEMMはプログラムを[UMBや](https://ja.wikipedia.org/wiki/XMS#UMB "wikilink")[HMAにロードすることで](https://ja.wikipedia.org/wiki/XMS#HMA "wikilink")[コンベンショナルメモリ](https://ja.wikipedia.org/wiki/コンベンショナルメモリ "wikilink")を空けることができる。[Lotus 1-2-3](../Page/Lotus_1-2-3.md "wikilink")、初期の[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、各種ゲームなど多数のプログラムがEMSやXMSメモリを使っていた。

## 競合製品

主な競合製品としては、海外ではBlueMax/386MAX、HeadRoom/NetRoomなどがあった。

1987年11月にリリースされた[コンパック](../Page/コンパック.md "wikilink")のDOS 3.31は、DOSとして初めてQEMM-386のような技術を導入した。これを[CEMM](https://ja.wikipedia.org/wiki/CEMM "wikilink")と呼んでいる。QEMMは世界初の[仮想86モード](https://ja.wikipedia.org/wiki/仮想86モード "wikilink")を使ったメモリマネージャ製品であった。

## DOSにおける同等機能

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は同等のやや単純化したメモリマネージャを1989年のMS-DOS 4.01でリリースした。XMS用のHIMEM.SYSとEMS 用の[EMM386](../Page/EMM386.md "wikilink").EXEである。それ以前の[Windows/386 2.1にもEMS機能は組み込まれていたが](https://ja.wikipedia.org/wiki/Microsoft_Windows_2.0 "wikilink")、Windowsセッション内でのDOSウィンドウでのみ使えるようになっていた。これらのバージョンでは[UMBを生成できなかった](https://ja.wikipedia.org/wiki/XMS#UMB "wikilink")。ベンダー固有でないDOSとして初めてUMB技術を提供したのは、[デジタルリサーチ](../Page/デジタルリサーチ.md "wikilink")の[DR-DOS](https://ja.wikipedia.org/wiki/DR-DOS "wikilink") 5.0（1990年）であった。MS-DOSがUMBを提供したのは、1991年の5.0が最初である。MS-DOSのEMM386は先にHIMEMをロードしておく必要があるが、DR-DOSのEMM386は両方の機能を備えており、独立したXMSドライバを必要としなかった。ただし、80286ベースのマシンではXMSドライバ (HIDOS.SYS) が必要とされていた。

DR-DOSとMS-DOSのメモリマネージャはどちらもQEMMに比較すると貧弱だった。例えば、どちらもUMBは手作業で発見して含める必要があったが、QEMMは自力でこれを行っていた。QEMMはEMSとXMSへのメモリ割り当てを事前に設定する必要がなく、立ち上げ時の設定をいじる必要がなかった。しかし、マイクロソフトはMS-DOS 6でUMBの最適化を自動化し、これによってQEMMの市場シェアは低下していった。

## Windowsへの移行

DOSプログラムが主流の時代はQEMMはよく使われたが、Windowsが主流になるにつれてあまり使われなくなっていった。最終版のQEMM 97は[Windows 95や後の](../Page/Microsoft_Windows_95.md "wikilink")[Windows 98](../Page/Microsoft_Windows_98.md "wikilink")/[MEとも互換性を保っていたが](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")、DOSアプリケーションそのものがほとんど使われなくなっていたため、DOS用のメモリマネージャもほとんど使われなくなった。

Windows 3.0以降、386エンハンストモードで起動されるようになったため、メモリマネージャはWindows起動時にシャットダウンされる。実際、複数のプロテクトモードの[カーネル](../Page/カーネル.md "wikilink")が同時に動作することはできない。従って、QEMMはWindowsと同時に動作しているわけではない。Windows立ち上げ時のシャットダウンシーケンスの中で、メモリマネージャはWindowsに対して特定の[VxD型デバイスドライバのロードを指示し](../Page/仮想デバイスドライバ.md "wikilink")、それがWindowsセッション内でのメモリマネージャ機能を提供する。例えば、QEMMにはWINHIRAM.VXDとWINSTLTH.VXDが同梱されていた。これらはWindowsに対して確立したメモリマッピング情報を通知し、Windowsがそれをインポートするようになっていた（これを*Global EMM import*と呼ぶ）。

QEMM 97では、Magna RAMというメモリ圧縮ソフトのサブセットが搭載されており、物理メモリの圧縮に加え、データを圧縮した状態でスワップアウトさせCPU負荷はかかるがバス帯域消費量は減るというアーキテクチャを採用していた。

また、Live Updateと呼ばれる自動オンラインアップデート機能は、その後CleanSweepを介して[ノートン・インターネットセキュリティ](https://ja.wikipedia.org/wiki/ノートン・インターネットセキュリティ "wikilink")などに搭載され、今なお活躍している。

## 関連項目

  - [CEMM](https://ja.wikipedia.org/wiki/CEMM "wikilink")
  - [リアルモード](https://ja.wikipedia.org/wiki/リアルモード "wikilink")
  - [プロテクトモード](https://ja.wikipedia.org/wiki/プロテクトモード "wikilink")
  - [コンベンショナルメモリ](https://ja.wikipedia.org/wiki/コンベンショナルメモリ "wikilink")
  - [XMS](https://ja.wikipedia.org/wiki/XMS "wikilink")
  - [EMS](https://ja.wikipedia.org/wiki/Expanded_Memory_Specification "wikilink")
  - [DESQview](../Page/DESQview.md "wikilink")

## 外部リンク

  - [QEMM download page](http://www.chsoft.com/dv.html)

[Category:X86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:X86アーキテクチャ "wikilink") [Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")