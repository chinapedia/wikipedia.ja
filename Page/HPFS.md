> この記事は[HPFS](https://ja.wikipedia.org/wiki/HPFS)から翻訳されています。


**HPFS**（High Performance Filesystem、エイチ・ピー・エフ・エス）は、[1989年](../Page/1989年.md "wikilink")に発売された[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")のバージョン1.2以降で導入された[ファイルシステム](../Page/ファイルシステム.md "wikilink")。従来の[FATファイルシステムの欠点を補うため](../Page/File_Allocation_Table.md "wikilink")、最大ファイル名長の拡張（255[バイトまで](../Page/バイト_\(情報\).md "wikilink")）、最大ボリュームサイズの拡張、ファイル属性の付加（[拡張属性](https://ja.wikipedia.org/wiki/拡張ファイル属性 "wikilink"): EA）、[フラグメンテーション](../Page/フラグメンテーション.md "wikilink")の最小化、ファイルパフォーマンスの高速化などの改良が行われた。

## 概要

[Windows NT系では](../Page/Windows_NT系.md "wikilink")、初期のWindows NTでOS/2との互換の為に採用されていたが、よりパフォーマンスのよい[NTFSがメインに使われているため](../Page/NT_File_System.md "wikilink")[Windows 2000でサポートが打ち切られた](../Page/Microsoft_Windows_2000.md "wikilink")。そのため、OS/2での互換目的以外はほとんど使われていないファイルシステムである。

なお、Windows NT登場後もOS/2においてはHPFSが利用され続けた。同程度の資源ではNTは重く、FAT (VFAT) しか利用できない[Windows 95が信用できないとして](../Page/Microsoft_Windows_95.md "wikilink")、一部の個人と企業においてOS/2がHPFSで利用された。OS/2においても、大量のメモリーを[ディスクキャッシュ](https://ja.wikipedia.org/wiki/ディスクキャッシュ "wikilink")に活用できるHPFS386が高価なオプションであったため、速度面の優位性は失われていったが、フラグメンテーションが発生しにくい利点は高い成果を発揮した。

また、1990年代後半は[Linux](../Page/Linux.md "wikilink")でもHPFSが書き込み可能なかたちでリリースされることが多かった。そのため、Windows NT 4.0で、NT 3.51のHPFS.DLLを流用し、LinuxとNTとの間をHPFSでやりとりする場合もあった。現在ではWindows、LinuxともにHPFS対応は現実的ではなく、ファイルのやりとりには、別途ファイルサーバを用意したり、FAT32領域を用意する方法が一般的となっている。

## 特徴

  - ブロックサイズは512バイト固定である。ボリュームサイズによってサイズが大きくなるFATに比べると無駄になるディスク領域が少ない。
  - フラグメンテーションの最小化。ファイルを拡張したときのブロックの割り当てを工夫する事で、ボリュームサイズが小さくてもフラグメンテーションが少なくなるように設計されている。
  - 最大ボリュームサイズは2TiB。16GiB未満が推奨されている。ただしOS/2の実装上64GB以上はHPFSでフォーマットできずHPFS386を含む他のファイルシステムを用いる必要がある
  - 最大ファイル名長は255バイト。後に拡張された[VFAT](https://ja.wikipedia.org/wiki/VFAT "wikilink")と同じである。
  - VFATが長いファイル名だけを重視したFATの拡張に過ぎないのに対して、HPFSはフラグメンテーションの回避や対障害性を重視する。

## 関連項目

  - [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")
  - [Windows NT](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")
  - [NTFS](../Page/NT_File_System.md "wikilink")
  - [FAT](../Page/File_Allocation_Table.md "wikilink")

[Category:OS/2](https://ja.wikipedia.org/wiki/Category:OS/2 "wikilink") [Category:Windows_NT系](https://ja.wikipedia.org/wiki/Category:Windows_NT系 "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink")