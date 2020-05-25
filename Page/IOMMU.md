> この記事は[IOMMU](https://ja.wikipedia.org/wiki/IOMMU)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:MMU_and_IOMMU.svg "wikilink") (**MMU**)\]\] **IOMMU** (**Input/Output Memory Management Unit**、**IOMMU**) とは[DMA可能なI](../Page/Direct_Memory_Access.md "wikilink")/O[バスと](../Page/バス_\(コンピュータ\).md "wikilink")[主記憶装置](../Page/主記憶装置.md "wikilink")を接続する[メモリ管理ユニット](../Page/メモリ管理ユニット.md "wikilink") (MMU) である。MMU が[CPU](../Page/CPU.md "wikilink")に見える[仮想アドレスを](../Page/仮想記憶.md "wikilink")[物理アドレス](https://ja.wikipedia.org/wiki/物理アドレス "wikilink")に変換するように、IOMMU は周辺機器から見える仮想アドレス（デバイスアドレスとかI/Oアドレスと呼ぶ）を物理アドレスに変換する。周辺機器の誤動作からメモリを守るため、[メモリ保護機能](https://ja.wikipedia.org/wiki/メモリ保護機能 "wikilink")も提供する。

## 実例と呼称

IOMMU の例として、[AGPや](../Page/Accelerated_Graphics_Port.md "wikilink")[PCI Expressのグラフィックスカードで使われる](../Page/PCI_Express.md "wikilink") Graphics Address Remapping Table (GART) がある。

[AMDは](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、HyperTransport アーキテクチャでの IOMMU 技術の仕様を公表している\[1\]。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")は IOMMU の仕様を Virtualization Technology for Directed I/O (VT-d) として公表している\[2\]。[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の IOMMU は Solaris Developer Connection の Device Virtual Memory Access (DVMA) として公表されている\[3\]。[IBM](../Page/IBM.md "wikilink")の IOMMU は Translation Control Entry (TCE) と称している文書がある\[4\]。PCI-SIG では関連する部分を I/O Virtualization (IOV) \[5\]と Address Translation Services (ATS) と呼んでいる。

x86のIOMMUについては、[x86仮想化\#チップセット](https://ja.wikipedia.org/wiki/x86仮想化#チップセット "wikilink")も参照のこと。

## 利点

物理アドレスを直接使う場合と比較した IOMMU の利点は以下の通りである。

  - 大きなバッファを確保する際に、物理的に連続であることを保証する必要がない。IOMMU が連続な仮想アドレスと分断された物理アドレスのマッピングを行う。
  - 主記憶メモリ全体を指定できるほどのアドレス幅を持たない周辺機器（バス）の場合、IOMMU を使えばメモリ上どこにバッファがあってもアクセス可能となる。これにより、周辺機器がアクセスできる範囲にあるバッファと実際のバッファの間でメモリコピーをする必要がなくなる。
      - 例えば、最近のx86系プロセッサは[PAE機能によって](../Page/物理アドレス拡張.md "wikilink") 4GiB 以上のメモリ空間を扱える。しかし、32ビットのPCIデバイスは 4GiB を越えるアドレスにあるメモリには単純にはアクセスできない。IOMMU がない場合、[OS](../Page/オペレーティングシステム.md "wikilink") は double buffering（Windows用語）とか bounce buffers（Linux用語）と呼ばれる時間のかかる処理を必要とする。
  - [メモリ保護機能](https://ja.wikipedia.org/wiki/メモリ保護機能 "wikilink")により、明示的にアクセス権がないとデバイスからメモリにアクセスできない。これによりデバイスの誤動作や悪意あるデバイスからメモリを保護する。IOMMU の設定は CPU 上で動作する OS が行うため、デバイス側から設定することはできない。
      - [仮想化](../Page/仮想化.md "wikilink")では、ゲストOSが IOMMU を直接制御すべきではない。
      - アークテクチャによっては、IOMMU が[割り込みの再マッピングも行う](../Page/割り込み_\(コンピュータ\).md "wikilink")。

IOMMU は CPU がデバイスと（DMAではなく）[ポートマップドI/Oで通信する場合には使われない](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")。

## 欠点

IOMMU を使う場合の欠点として、次の事柄が指摘されている\[6\]。

  - IOMMU による変換と管理による性能低下が見られる。
  - I/O用の[ページテーブル](../Page/ページテーブル.md "wikilink")を作成する必要があるため、物理メモリがそれだけ消費される。[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")機でプロセッサ間でI/O用ページテーブルを共有できれば、問題は若干緩和される。

## IOMMU と仮想化の関係

OS が [Xen](../Page/Xen_\(仮想化ソフトウェア\).md "wikilink") などの[仮想機械](../Page/仮想機械.md "wikilink")上で動作する場合、各OSはアクセスしている物理アドレスを知らない。そのため、周辺機器にDMAを指示しようとしても、直接的に物理アドレスを指定することができない。実際には、仮想機械が I/O 操作に対して変換を施しており、I/O 操作に遅延が生じる原因となっている。

IOMMU は、ゲストOSと周辺機器のアクセスするアドレスのマッピングをそろえることで、これを解決できる\[7\]。

## 脚注

## 参考文献

  -
## 関連項目

  - [仮想記憶](../Page/仮想記憶.md "wikilink")
  - [メモリマップドI/O](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")
  - [Direct Memory Access](../Page/Direct_Memory_Access.md "wikilink")
  - [x86仮想化](https://ja.wikipedia.org/wiki/x86仮想化 "wikilink")

[Category:記憶装置](https://ja.wikipedia.org/wiki/Category:記憶装置 "wikilink")

1.
2.
3.
4.
5.
6.
7.