> この記事は[Direct Memory Access](https://ja.wikipedia.org/wiki/Direct_Memory_Access)から翻訳されています。


[AMD_DirectGMA.svg](https://ja.wikipedia.org/wiki/File:AMD_DirectGMA.svg "fig:AMD_DirectGMA.svg")

**Direct Memory Access**（DMA）とは、[プログラムされた](../Page/プログラム_\(コンピュータ\).md "wikilink")[機械語](../Page/機械語.md "wikilink")の命令群の実行によって[アキュムレータなどを介する方法によらず](../Page/アキュムレータ_\(コンピュータ\).md "wikilink")、[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")とメモリまたはメモリと[I/Oデバイスの間で直接データを](../Page/入出力.md "wikilink")[転送](https://ja.wikipedia.org/wiki/転送 "wikilink")することである。

専用回路のことを **DMAC**（DMA Controller）と言う。

## 概要

現代でのDMAの重要性は、つまるところCPUの転送速度の枷を外したところにある。DMAの技術が発生する以前は、CPUはデータの転送時間のあいだ待たなくてはならず、その間は他の作業をこなすことはできなかった。外部入出力（I/O）の転送速度はRAMよりも遅かったことがこの原因である。DMAがあれば、CPUは転送時間を有意にタスクへと割くことができる。この利点は組み込み向けプロセッサにおいても同様に効果があった。ただし、転送バスは一部使用中となる。したがって、DMAによって転送時間を有効に使えるとしても、それはプログラムがまさに今DMA転送中のデータを使用しないときに限られてしまう。

DMA転送は、CPUによって行われるものではない。CPUはDMA転送命令を実行するが、これはつまるところ、[マザーボード](../Page/マザーボード.md "wikilink")の[チップセット](../Page/チップセット.md "wikilink")に内蔵されたDMAコントローラに、転送開始を指示しているだけである。この形式は過去のISAバスによってみられた方式であるが、現代のPCIバスにはより優れた設計思想が組み込まれており、「Bus mastering DMA」、すなわち、I/O機器の側がPCIバスの制御を任され、DMA転送をすべて司る。一方組込デバイスでは、CPU内でバスに直結されたDMAエンジンがチップ内のバスを操作してDMAを実現する。

DMAの利点は、継続的な読み出しを必要とする、ネットワークのパケット送信や音楽再生やビデオ配信などの機能を、データ通信のためにリソースを割くことなく行うため、その専用の組み込みチップで使われている。また同様に、CPUの多コア化にもとても有効である。１チップ上での多コア化だけでなく、大規模なコンピュータでのクラスタ化にも有用である。この際、DMA通信の状態通知ピンとして、受信状態を示すHOLDピンと、送信状態を示すHLDAピンが存在する。

## 歴史

DMAは[PDPシリーズ](../Page/PDPシリーズ.md "wikilink")において採用されている。後年の数MHzで動作する[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")では、[CPU](../Page/CPU.md "wikilink")による[データ転送](https://ja.wikipedia.org/wiki/データ転送 "wikilink")で[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")等の10MB/秒程度の転送速度を発揮する事は困難であったため、専用のコントローラでデータ転送を行う必要があった。このコントローラは、データ転送を高速に行う機能に特化したCPUであったともいえる。例として、[Z80](../Page/Z80.md "wikilink")にはZ80DMA、[MC68000](../Page/MC68000.md "wikilink")には、MC68450などのDMAコントローラ（DMAC）が存在した。そのほか、日立の[H8](../Page/H8.md "wikilink")マイコンにDMACが存在している。

Intelの[i80286](../Page/Intel_80286.md "wikilink")（APX286）などでは、当時通常のI/Oを制御するためには充分な動作速度だった事、主流の[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")において、i8249等の低速なDMACしか搭載されておらず、他に適当なDMACが存在しなかった事などから、DMAはあまり使用されなくなった。

CPUの世代が[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")になり、充分に高速になると、今度は、低速なI/Oの管理が[ボトルネック](../Page/ボトルネック.md "wikilink")となったため、いわゆる[チップセット](../Page/チップセット.md "wikilink")にI/O専用の高速なDMACが搭載されたり、周辺機器制御LSIが簡単なDMA機能を持つようになり、再度DMAが活用されるようになった。Pentium以降主流となった[PCIバスでは](../Page/Peripheral_Component_Interconnect.md "wikilink")、[バスマスタリング](https://ja.wikipedia.org/wiki/バスマスタリング "wikilink")としてDMAが実装されている。

## 高機能DMAC

初期のDMACは単純に指定されたアドレス範囲を指定されたメモリもしくはポートに入出力する機能のみを備えていた。しかし[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が普及し、ハードディスクへのI/OにDMACを使う様になってから、DMACには「データブロックを分割する（スキャッタリング）」「データブロックを集約する（ギャザリング）」を行う機能を要求された。MC63450 DMAC等には、DMACがリンクリストを読み取って転送内容を分割したり集約する機能が搭載されている。[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")向けの[SCSI](../Page/Small_Computer_System_Interface.md "wikilink")[ホストアダプタ](https://ja.wikipedia.org/wiki/ホストアダプタ "wikilink")カード等では、コントローラチップに集積されているDMACがこの機能を担当していた。スキャッタリング・ギャザリング機能が無い場合CPUは最低でも1セクタ分ずつメモリ・メモリ間転送を行わなければならず、またDMACに読み取らせるメモリ領域が転送完了するまで使用できないため、I/O時のCPU負荷上昇とI/O待ち時間が発生しシステム性能に悪影響を与えた。

## DMAの方式

  - バーストモードDMA
    CPUから制御を奪い、データを一気に転送する方法。
  - サイクルスチールモードDMA
    CPUがメモリにアクセスしていない時にDMAを行なう方法。

## 代表的なDMAC、DMA機能を持つLSI

  - Z80DMA
  - MC68450
  - i430など、PentiumCPU以降対応のチップセット

## 関連項目

  - [バスマスタリング](https://ja.wikipedia.org/wiki/バスマスタリング "wikilink")
  - [Remote Direct Memory Access](https://ja.wikipedia.org/wiki/Remote_Direct_Memory_Access "wikilink")
  - [PIO病](https://ja.wikipedia.org/wiki/PIO病 "wikilink")

## 外部リンク

  - [Microcomputer Interfacing](http://chc61.fgcu.edu/PDFs/DirectMemoryAccess.pdf)（英文）（PDFファイル）

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:記憶装置](https://ja.wikipedia.org/wiki/Category:記憶装置 "wikilink") [Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink") [Category:マザーボード](https://ja.wikipedia.org/wiki/Category:マザーボード "wikilink")