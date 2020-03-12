> この記事は[Massive Arrays of Inactive Disks](https://ja.wikipedia.org/wiki/Massive_Arrays_of_Inactive_Disks)から翻訳されています。


**MAID** (**M**assive **A**rrays of **I**nactive **D**isks・メイド)とは、コロラド大学のDirk Grunwaldによって提唱された、アクセス局在性に基づく階層化モデルをストレージシステムに適用した大規模ディスクアレイモデルのひとつである。

## アクセス局在性

一般に、メモリにはアクセス局在性に基づく階層化モデルが存在し、それに基づいて実装されている。たとえば、CPUの内部レジスタからキャッシュメモリ・メインメモリ・補助記憶装置と徐々に低速・大容量の記憶装置を階層的に配置する事により、アクセスの集中度合いに応じた適切なメモリデバイスが割り当てられている。ディスクアレイシステムにも、やはりアクセスの集中が存在し、ディスクアレイ全体のうち80%のアクセスは、20%の[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")に集中している事が統計的に明らかにされた。言い換えれば、高性能で常時スタンバイしているハードディスクドライブはディスクアレイ全体の20%だけでよく、残りのハードディスクドライブは低性能で常時モーターを回す必要すら無い。アクセス集中がおきる領域を担う高速なアクセスできる高階層の[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")ハードディスクドライブ等と、その下の階層にあるテープの様な非常に遅い媒体の間に、テープよりは若干高価で高速だが高階層の高性能ハードディスクドライブよりは安価な[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")ハードディスクドライブを大量に挿入する。これらの中階層にあるハードディスクドライブはアクセスが集中しないので通常モーターの回転を止めておく事によりシステム全体の寿命を延長する。そして安価なデバイスを使う事によりストレージシステム全体の性能を向上しながらもシステム全体のコストを削減するものである。

## 参考

  - [Enterprise Watch ディスクとテープのギャップを埋めるMAIDテクノロジ](http://enterprise.watch.impress.co.jp/cda/storage/2005/02/28/4704.html)

## 関連事項

  - [RAID](../Page/RAID.md "wikilink")

[Category:補助記憶装置](https://ja.wikipedia.org/wiki/Category:補助記憶装置 "wikilink") [Category:サーバ](https://ja.wikipedia.org/wiki/Category:サーバ "wikilink") [Category:ハードウェア](https://ja.wikipedia.org/wiki/Category:ハードウェア "wikilink")