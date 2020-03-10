> この記事は[IWarp](https://ja.wikipedia.org/wiki/IWarp)から翻訳されています。


**iWarp**は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")と[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink") (CMU) の共同プロジェクトとして開発された実験的な[並列](../Page/並列計算.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")である。 プロジェクトは、CMUの研究プロジェクトの後継として、ひとつの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")に[並列計算](../Page/並列計算.md "wikilink")に必要な機能([メモリと通信機能](../Page/主記憶装置.md "wikilink"))を内蔵することを目標として1988年に始まった。そういう意味では、iWarpは[トランスピュータ](../Page/トランスピュータ.md "wikilink")や[nCUBE](https://ja.wikipedia.org/wiki/nCUBE "wikilink")に非常によく似ている\[1\]。

インテルは1989年にiWarpシステムを製品として発表した。最初の試作品はカーネギーメロン大学に1990年夏に納入され、秋には64セルの製品版が、1991年には追加の2台が納入されている。1992年夏にはインテル内にスーパーコンピューティングシステム部門が創設され、iWarpは製品とマージされひとつのシリーズとされた。インテルはiWarpを製品として残したが、積極的なマーケティングはやめた\[2\]。現在は製造されていない。

iWarpの各[CPU](../Page/CPU.md "wikilink")は20MHzで動作し、[32ビット](../Page/32ビット.md "wikilink")[ALUと](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")[FPU](../Page/FPU.md "wikilink")を備えている。単純なパイプライン構造で1サイクルに1[命令を実行するので](../Page/命令_\(コンピュータ\).md "wikilink")、性能は 20[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")である（[浮動小数点は](../Page/浮動小数点数.md "wikilink")[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")で20[M](../Page/メガ.md "wikilink")[FLOPS](../Page/FLOPS.md "wikilink")、[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")で10MFLOPS）\[3\]\[4\]。通信はチップ上の別ユニットで制御され、40MB/sの4本の[シリアルチャネルを装備している](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")。このチャネルはハードウェアで20本の仮想チャネルとして扱うことが可能(INMOS T9000 に追加された機能と類似)。

CPUは基板上にメモリと共に実装されるが、インテルは高速で高価な[SRAMを使った](../Page/Static_Random_Access_Memory.md "wikilink")。ひとつの基板には4つのCPUと512K～4Mバイトのメモリが実装される。

iWarpでは [ハイパーキューブではなくN](../Page/超立方体.md "wikilink")×Mの[トーラス](../Page/トーラス.md "wikilink")型のネットワークでノードを接続した。典型的なシステムでは64個のCPUが 8×8のトーラスを構成している。この構成で最高 1.2[GFLOPSを記録している](../Page/ギガ.md "wikilink")。

iWArpプロジェクトを指揮したアーキテクトはジョージ・コックスである。（後のマイクロソフト副社長で、反トラスト法違反の裁判で証人として出廷したことがある）は、iWarpが完成する以前から使用可能な革新的な開発環境を作った。これはノードに対応する[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のワークステーションを[LAN上で相互接続し](../Page/Local_Area_Network.md "wikilink")、iWarpのノード間通信プロトコルを[ソケット上でシミュレートしたものである](../Page/ソケット_\(BSD\).md "wikilink")。チップレベルのシミュレータではないが、並列ソフトウェア開発のスタート地点としては役立った。

iWarp向けにはCとFORTRANのコンパイラが開発されている。まず[AT\&T](../Page/AT&T.md "wikilink")のUNIX向け pcc コンパイラがインテルとの契約に基づいて移植され、その後インテルが独自に修正・拡張を施した\[5\]。

## 脚注

## 関連項目

  - [トランスピュータ](../Page/トランスピュータ.md "wikilink")
  - [nCUBE](https://ja.wikipedia.org/wiki/nCUBE "wikilink")

## 外部リンク

  - [iWarp Project (英語)](http://www-2.cs.cmu.edu/afs/cs/project/iwarp/archive/WWW-pages/iwarp.html)

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink")

1.  Encyclopedia of Parallel Computing, Padua, David (Ed.), 2011, ISBN 978-0-387-09765-7
2.  Thomas Gross and David R. O'Hallaron. iWarp: anatomy of a parallel computing system, MIT Press, Cambridge, MA, 1998.
3.  Shekhar Borkar, Robert Cohn, George Cox, Sha Gleason, and Thomas Gross. iWarp: an integrated solution of high-speed parallel computing, Proceedings of the 1988 ACM/IEEE conference on Supercomputing, p.330-339, November 12-17, 1988.
4.  Intel Corp. iWarp Microprocessor (Part Number 318153), Hillsboro, Oregon, 1991. Technical Information, Order Number 281006.
5.  Ali-Reza Adl-Tabatabai, Thomas Gross, Guei-Yuan Lueh and James Reinders. Modeling Instruction-Level Parallelism for Software Pipelining. In Proceedings of the IFIP WG10.3 Working Conference on Architectures and Compilation Techniques for Fine and Medium Grain Parallelism, Orlando, FL, pages 321-330.