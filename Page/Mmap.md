> この記事は[Mmap](https://ja.wikipedia.org/wiki/Mmap)から翻訳されています。


**mmap**() は、[UNIX](../Page/UNIX.md "wikilink")の[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")のひとつで、[ファイルや](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[デバイスなどの](../Page/ハードウェア.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 上の[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")の一部または全部を連続した[仮想アドレス空間にマッピングする関数である](../Page/仮想記憶.md "wikilink")。

[ファイルシステム](../Page/ファイルシステム.md "wikilink")上の[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")に対するアクセス方法として、[ストリームI](https://ja.wikipedia.org/wiki/ストリーム_\(プログラミング\) "wikilink")/Oを行う[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")との比較で、[ユーザ空間と](https://ja.wikipedia.org/wiki/アドレス空間#ユーザ空間 "wikilink")[カーネル空間の間で読み書きされるデータの](https://ja.wikipedia.org/wiki/アドレス空間#カーネル空間 "wikilink")[ブロック転送](https://ja.wikipedia.org/wiki/ブロック転送 "wikilink")が多くの[アーキテクチャ上では発生しないことから](../Page/コンピュータ・アーキテクチャ.md "wikilink")、好まれる場合がある。

[デバイスでは](../Page/ハードウェア.md "wikilink")、[ioctl](https://ja.wikipedia.org/wiki/ioctl "wikilink")()とともに[メモリマップドI/O](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")や[DMAなどの操作を抽象化するものとして](../Page/Direct_Memory_Access.md "wikilink")[ドライバからファイルI](../Page/デバイスドライバ.md "wikilink")/Oサービスの一部として提供されることがある。

## 規格

mmap()は[POSIX](../Page/POSIX.md "wikilink")により定義されており、POSIX準拠のOSで利用することができる。POSIXで定められた動作のほかに、各OS毎に独自の拡張が施されていることがよくあり、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")でも、mmap() はいくつかのOS固有のマッピングを生成可能である。

Win32 API の場合、対応する関数は、ファイルマッピングは CreateFileMapping()\[1\] と MapViewOfFile()\[2\]、無名マッピングは VirtualAlloc()\[3\]。

## ファイルマッピングと無名マッピング

### ファイルマッピング

ファイルを[仮想アドレス空間へマッピングした場合](../Page/仮想記憶.md "wikilink")、OSはファイル上の対象となる領域のデータを、[ビュー](../Page/ビュー.md "wikilink")として、mmap()を呼び出した[プロセス](../Page/プロセス.md "wikilink")がアクセスできる仮想アドレス空間に割り当てる。そして、プロセスがマッピングされた領域へ書き込みを行った場合、MAP_SHARED を指定した場合は、OSはその変更を同期的あるいは非同期的にファイルへと反映する。MAP_SHARED と排他的な MAP_PRIVATE を指定した場合は、変更はファイルには反映されない。

### 無名マッピング

ファイルの裏付けがないものを、無名 (Anonymous) マッピングと呼ぶ。無名マッピングを使用するには引数flags に MAP_ANONYMOUS を指定し、ファイルディスクリプタに -1 を指定する。無名マッピングを使うと利用可能なメモリ領域を[仮想アドレス空間から確保できる](../Page/仮想記憶.md "wikilink")。この機能は、[アプリケーションの実行中にOSから追加のメモリ](../Page/アプリケーションソフトウェア.md "wikilink")[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")を獲得する方法として利用される。多くの[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")の[Cライブラリ](https://ja.wikipedia.org/wiki/Cライブラリ "wikilink")の[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")()の実装は、小さなメモリ領域の確保はデータセグメントを拡張してそこから小分けに切り分け、大きなメモリ領域の確保のケースには mmap() を内部的に使っている。例えば、Doug Lea の実装した dlmalloc の場合、デフォルト値は256KB以上のメモリ確保に mmap() を使用する\[4\]。

## 複数プロセス間におけるmmap

複数のプロセスで、同じリソースの同じ領域をマッピングした場合の動作は、mmap()呼び出し時のパラメータや、OSの提供するマッピングの[セマンティクス](https://ja.wikipedia.org/wiki/セマンティクス "wikilink")によって異なる。なお、MAP_SHARED, MAP_PRIVATE などのメモリの属性は、[fork](https://ja.wikipedia.org/wiki/fork "wikilink")() により生じた[子プロセス](https://ja.wikipedia.org/wiki/子プロセス "wikilink")においても保持される。

### MAP_SHARED

MAP_SHARED を指定すると、マッピングされたメモリ領域が複数のプロセスで共有される。あるプロセスがマッピングされた領域に書き込んだ内容を、他のプロセスが（同期的あるいは非同期的に）即座に読むことができるようになる。この性質は、[プロセス間通信](../Page/プロセス間通信.md "wikilink")の手法の1つとして（[UNIX System Vの](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")[共有メモリ](../Page/共有メモリ.md "wikilink")機構の代替として）使われることがある。

### MAP_PRIVATE

MAP_PRIVATE を指定すると、マッピングが[コピーオンライト](https://ja.wikipedia.org/wiki/コピーオンライト "wikilink")になる。そこでは、マッピングされたメモリ領域からの読み取りしか行われていない状況が続く限りプロセス間でマッピングが共有されるが、あるプロセスがメモリ領域に何かを書き込もうとした瞬間に[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")がマッピングを複製し、メモリ領域のコピーを生成したのち、その領域をプロセス固有のものとして位置づける。つまり、事実上、プロセス間ではマッピングが共有されていないということになり、この状況では、マッピングによるリソースへのアクセスは一貫性がないということになる。

## アドレス指定

通常は利用する[仮想アドレス空間のアドレスは](../Page/仮想記憶.md "wikilink")、mmap() 側が勝手に割り振るが、MAP_FIXED を指定した場合、もし、そこが空き領域であれば、好きなアドレスを利用できる。ただし、アドレス 0 だけは使用できない。また、アドレスはページサイズ（多くのケースで4KB）の倍数でないといけない。

## 関連項目

  - [メモリマップトファイル](https://ja.wikipedia.org/wiki/メモリマップトファイル "wikilink")
  - [共有メモリ](../Page/共有メモリ.md "wikilink")

## 参照

## 外部リンク

  -
  -
[Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:UNIXのシステムコール](https://ja.wikipedia.org/wiki/Category:UNIXのシステムコール "wikilink") [Category:プロセス間通信](https://ja.wikipedia.org/wiki/Category:プロセス間通信 "wikilink")

1.  [CreateFileMapping](http://msdn.microsoft.com/ja-jp/library/cc430039.aspx)
2.  [MapViewOfFile](http://msdn.microsoft.com/ja-jp/library/cc430198.aspx)
3.  [VirtualAlloc](http://msdn.microsoft.com/ja-jp/library/cc430204.aspx)
4.  [dlmalloc](ftp://g.oswego.edu/pub/misc/malloc.c)