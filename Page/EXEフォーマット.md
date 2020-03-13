> この記事は[EXE](https://ja.wikipedia.org/wiki/EXE)から翻訳されています。


**EXEフォーマット**（エグゼフォーマット）とは[MS-DOS](../Page/MS-DOS.md "wikilink")およびその互換・後継である[Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[実行ファイル](../Page/実行ファイル.md "wikilink")を格納する[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。EXE は"executable"の省略形であり、Windowsプログラムの標準的な[ファイル拡張子](https://ja.wikipedia.org/wiki/ファイル拡張子 "wikilink")である。多くのWindowsユーザーにとって、EXEファイルはWindowsプログラムと同義で".exe"は最も認知されている拡張子のひとつである\[1\]。

## ファイルフォーマット

ファイルの先頭には0x5A4D（ASCIIコードで'MZ'という文字列）\[2\]の[マジックナンバーが入っている](https://ja.wikipedia.org/wiki/マジックナンバー_\(フォーマット識別子\) "wikilink")。これは、MS-DOS 2.0の開発責任者の一人、Mark Zbikowskiのイニシャルに由来する。

の拡張子を持つファイルのファイルフォーマットにはいくつかの種類が存在する。拡張ヘッダにより、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")の実行ファイルの情報を指定し、これらのOS用に作られたプログラムが本来のアーキテクチャでOSで実行された場合は、その拡張ヘッダを解釈し、MS-DOS上で実行された場合、実行できない事を表示し終了させる等のプログラムを置くことが可能である。このようなフォーマットには[Portable Executable](../Page/Portable_Executable.md "wikilink") (PE) や[New Executable](https://ja.wikipedia.org/wiki/New_Executable "wikilink") (NE), [Linear Executable](https://ja.wikipedia.org/wiki/Linear_Executable "wikilink") (LE, LX) 等が存在する。

### DOS

  - 16ビット DOS MZ executable: 元々の DOS 実行ファイルフォーマットである。ファイルの先頭にはASCIIコードで "MZ" の文字があり、これで識別できる。
    16ビット New Executable: マルチタスクの[MS-DOS 4.0で導入され](https://ja.wikipedia.org/wiki/MS-DOS#バージョン4 "wikilink")、16 ビットの OS/2 と Windows で使われた。[NEはASCIIコードの](https://ja.wikipedia.org/wiki/New_Executable "wikilink")"NE"で識別できる。

### OS/2

  - 32ビット Linear Executable: OS/2 2.0で導入され、ASCIIコードの "LX" で識別できる。OS/2 2.0 と後継でのみ実行可能\[3\]。 また、[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")の一部でも利用された。
    16/32ビット混在 Linear Executable: OS/2 2.0で導入され、ASCIIコードの "LE" で識別できる。このフォーマットは[Windows 3.x](https://ja.wikipedia.org/wiki/Windows_3.1 "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、Windows 9xの[VxD](https://ja.wikipedia.org/wiki/VxD "wikilink")ドライバとして使われた。また、DOSエクステンダの一部でも利用された。

### Windows

16ビットと32ビットのWindows実行ファイルがWindows上で実行されるとき、NEまたはPEから実行が開始され、[DOS](https://ja.wikipedia.org/wiki/DOS "wikilink")[スタブ](https://ja.wikipedia.org/wiki/スタブ "wikilink")と呼ばれるMZコードは無視される\[4\]\[5\]。[DOS](https://ja.wikipedia.org/wiki/DOS "wikilink")ではスタブは"This program cannot be run in DOS mode"、もしくは同様のメッセージを終了前に表示するため[ファットバイナリ](../Page/ファットバイナリ.md "wikilink")の最小フォームを形成している。[レジストリ](../Page/レジストリ.md "wikilink")[エディタ](https://ja.wikipedia.org/wiki/エディタ "wikilink")\[6\]や古い WinZIP 自己解凍形式ファイル等のいくつかのデュアルモード(MZ-NE または MZ-PE)のプログラムにはより多くのDOSプログラムが含まれていた\[7\]。

  - 32ビット [Portable Executable](../Page/Portable_Executable.md "wikilink"): Windows NTで導入され、ASCIIコードの "PE" で特定できる。(ただし、ファイルの先頭はPEではなく"MZ"である)\[8\]
    64ビット Portable Executable (PE32+): 64ビットバージョンのWindowsで導入され、より多くのフィールドを持つPEファイルである。多くの場合、コードは32ビットか64ビットかのいずれかのPEファイルとして動作する\[9\]。

## その他のファイルフォーマット

また、上記のほかにも多くの特殊なEXEフォーマットが存在する。[Microsoft Windows 3.xの](../Page/Microsoft_Windows_3.x.md "wikilink")386エンハンスドモードの[カーネル](../Page/カーネル.md "wikilink")であるWIN386.EXEや、[Microsoft Windows 95等のカーネルであるVMM](../Page/Microsoft_Windows_95.md "wikilink")386.VXDでは特殊な拡張ヘッダで内部に存在する[プロテクトモード](../Page/プロテクトモード.md "wikilink")のカーネルコードや[仮想デバイスドライバ](../Page/仮想デバイスドライバ.md "wikilink")等へのオフセットを保持しており、リアルモードでの初期化を普通のDOSプログラムとして行った上で、そのヘッダにあるプロテクトモードのコードを実行していた。（WIN386.EXEではW3, VMM386.VXDではW4という識別子。*W3* (LEファイルのコレクションでWIN386.EXEのみで利用された)と*W4* (LEファイルの圧縮されたコレクションでVMM32.VXDのみで利用された)のほかにも *DL*、*MP*、*P2*、*P3* (最後の3つは[Phar Lap DOSエクステンダで使われていた](../Page/DOSエクステンダ.md "wikilink"))\[10\]が存在していた。

### COMファイルとの比較

MS-DOSで実行可能なバイナリのフォーマットには他に、[COMフォーマット](https://ja.wikipedia.org/wiki/COMフォーマット "wikilink")と言うファイルフォーマットが存在する。COMフォーマットは、[コード](../Page/プログラム_\(コンピュータ\).md "wikilink")、[データ](../Page/データ.md "wikilink")、[スタック](../Page/スタック.md "wikilink")の全ての[セグメントが同一であるモデルで](../Page/セグメント方式.md "wikilink")、開始番地も固定の0x100であるメモリイメージそのものであり、シンボル再配置も無い。[COMフォーマット](https://ja.wikipedia.org/wiki/COMフォーマット "wikilink")は、ファイルヘッダを持たず拡張性がなかった。これに対し、EXEフォーマットは連続した一つのメモリイメージで、コード、データ、スタックの全てが別々の複数のセグメントを用いてアクセスする必要のある場合に対応し、開始アドレスおよびその時のセグメントレジスタの値をファイル先頭から相対指定することが可能でセグメント指定の再配置エントリが存在する。

### ヘッダー形式の例

C言語による表記は以下の通りである。尚、この定義は[Wine](../Page/Wine.md "wikilink")で使われている[ヘッダファイル](../Page/ヘッダファイル.md "wikilink") (winnt.h) の定義から引用した。WORDは16ビット整数であり、DWORDは32ビット整数である。

`typedef struct _IMAGE_DOS_HEADER {`
`   WORD  e_magic;      /* 00: MZ Header signature */`
`   WORD  e_cblp;       /* 02: Bytes on last page of file */`
`   WORD  e_cp;         /* 04: Pages in file */`
`   WORD  e_crlc;       /* 06: Relocations */`
`   WORD  e_cparhdr;    /* 08: Size of header in paragraphs */`
`   WORD  e_minalloc;   /* 0a: Minimum extra paragraphs needed */`
`   WORD  e_maxalloc;   /* 0c: Maximum extra paragraphs needed */`
`   WORD  e_ss;         /* 0e: Initial (relative) SS value */`
`   WORD  e_sp;         /* 10: Initial SP value */`
`   WORD  e_csum;       /* 12: Checksum */`
`   WORD  e_ip;         /* 14: Initial IP value */`
`   WORD  e_cs;         /* 16: Initial (relative) CS value */`
`   WORD  e_lfarlc;     /* 18: File address of relocation table */`
`   WORD  e_ovno;       /* 1a: Overlay number */`
`   WORD  e_res[4];     /* 1c: Reserved words */`
`   WORD  e_oemid;      /* 24: OEM identifier (for e_oeminfo) */`
`   WORD  e_oeminfo;    /* 26: OEM information; e_oemid specific */`
`   WORD  e_res2[10];   /* 28: Reserved words */`
`   DWORD e_lfanew;     /* 3c: Offset to extended header */`
`} IMAGE_DOS_HEADER, *PIMAGE_DOS_HEADER;`

## 脚注

<references/>

## 関連項目

  - [実行可能ファイルフォーマットの比較](https://ja.wikipedia.org/wiki/実行可能ファイルフォーマットの比較 "wikilink")
  - [実行ファイル圧縮](https://ja.wikipedia.org/wiki/実行ファイル圧縮 "wikilink")
  - [オブジェクトファイル](../Page/オブジェクトファイル.md "wikilink")
  - [実行ファイル](../Page/実行ファイル.md "wikilink")
  - [COMファイル](../Page/COMファイル.md "wikilink")

## 外部リンク

  - [Dependency Walker](http://dependencywalker.com/)
  - [MZ EXE ヘッダーフォーマット](http://www.delorie.com/djgpp/doc/exe/)

[Category:オブジェクトファイルフォーマット](https://ja.wikipedia.org/wiki/Category:オブジェクトファイルフォーマット "wikilink") [Category:MS-DOS](https://ja.wikipedia.org/wiki/Category:MS-DOS "wikilink")

1.
2.  WORD型として読み込む時の[リトルエンディアン](https://ja.wikipedia.org/wiki/リトルエンディアン "wikilink")の場合。バイト並びは低位から0x4D, 0x5Aである。
3.
4.
5.
6.
7.
8.
9.
10.