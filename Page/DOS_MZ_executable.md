> この記事は[DOS MZ executable](https://ja.wikipedia.org/wiki/DOS_MZ_executable)から翻訳されています。


**DOS MZ実行可能**形式は、[DOSの](../Page/DOS_\(OS\).md "wikilink")[EXEファイルに使用される](../Page/EXEフォーマット.md "wikilink")[実行可能形式](../Page/実行ファイル.md "wikilink")[ファイルである](../Page/ファイルフォーマット.md "wikilink")。

この形式は、ファイルの先頭にある[ASCII](../Page/ASCII.md "wikilink")文字列「MZ」（[16進数](../Page/十六進法.md "wikilink") ：4D 5A）（「 [マジックナンバー](../Page/マジックナンバー_\(プログラム\).md "wikilink")」）で識別できる。「MZ」は、[MS-DOS](../Page/MS-DOS.md "wikilink")の主要な開発者の1人であるMark Zbikowskiの頭文字である\[1\]。

MZ DOS実行可能ファイルは、 [COM実行可能形式よりも新しく形式が異なる](../Page/COMファイル.md "wikilink")。 DOS実行可能[ヘッダーには](https://ja.wikipedia.org/wiki/ヘッダ_\(コンピュータ\) "wikilink")、複数のセグメントを任意のメモリアドレスにロードできる[リロケーション情報が含まれ](../Page/リロケータブルバイナリ.md "wikilink")、64キロバイトを超える実行可能ファイルをサポートする。ただし、この形式では依然として使用可能メモリ量が制限される。 この制限は、後に[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")で回避されることになる。

DOSで実行されるEXEプログラムの環境に関する情報は、プログラムセグメントプレフィクス (PSP) に格納されている。

EXEファイルには、通常、コード、データ、およびスタック用の個別のセグメントがある。 プログラムの実行はコードセグメントのアドレス0から始まり、スタックポインターレジスタはヘッダー情報に含まれる値に設定される（したがって、ヘッダーが512バイトスタックを指定している場合、スタックポインターは200hに設定される）。 個別のスタックセグメントを使用せずに、必要に応じて単純にスタックのコードセグメントを使用することもできる。

DS（データセグメント）レジスタには通常、CS（コードセグメント）レジスタと同じ値が含まれており、EXEファイルが初期化されると、データセグメントの実際のセグメントアドレスはロードされない。プログラマーが自分で設定する必要があり、通常は次の手順で行う。

``` nasm
  MOV AX, @DATA
  MOV DS, AX
```

元のDOS 1.x APIでは、プログラム終了時にPSPのあるセグメントを指すDSレジスタも必要であった。これは、次の手順で実行された。

``` nasm
  PUSH DS
  XOR AX, AX
  PUSH AX
```

その後、プログラムの終了はRETF命令によって実行され、スタックからPSPを使用して元のセグメントアドレスを取得し、INT 20h命令を含むアドレス0にジャンプする。

DOS 2.x APIでは、プログラムの開始時にPSPセグメントアドレスを保存する必要のないINT 21h Function 4Chという新しいプログラム終了関数を導入し、マイクロソフトは古いDOS 1.x方式は使用しないよう推奨した。

## 互換性

MZ DOS実行ファイルは、DOSおよび[Windows 9xベースのオペレーティングシステムから実行できる](../Page/Windows_9x系.md "wikilink")。 32ビット[Windows NTベースのオペレーティングシステムでは](../Page/Microsoft_Windows_NT.md "wikilink")、組み込みの[仮想DOSマシン](../Page/仮想DOSマシン.md "wikilink")で実行できる（ただし、一部のグラフィックモードはサポートされていない）。 64ビットバージョンのWindowsでは実行できない。 これらの実行可能ファイルは、 [DOSBox](https://ja.wikipedia.org/wiki/DOSBox "wikilink") 、 DOSEMU、[Wine](../Page/Wine.md "wikilink")、[Cygwin](../Page/Cygwin.md "wikilink") を使っても実行できる。

MZ DOS実行ファイルは、 Digital Mars Optlink、MSリンカー、VALXまたはOpen WatcomのWLINK、FASMなどの[リンカ](https://ja.wikipedia.org/wiki/リンカ "wikilink")を使って作成できる。

## 関連項目

  - [DOS](../Page/DOS_\(OS\).md "wikilink")
  - [DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")
  - [実行可能ファイルフォーマットの比較](https://ja.wikipedia.org/wiki/実行可能ファイルフォーマットの比較 "wikilink")
  - [DOS API](https://ja.wikipedia.org/wiki/DOS_API "wikilink")
  - [実行ファイル圧縮](https://ja.wikipedia.org/wiki/実行ファイル圧縮 "wikilink")

## 脚注

## 外部リンク

  - [MZ DOS EXEファイル形式](http://www.delorie.com/djgpp/doc/exe/)
  - [EXE DOSスタブの詳細](https://marcin-chwedczuk.github.io/a-closer-look-at-portable-executable-msdos-stub)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:プログラミング言語の実装](https://ja.wikipedia.org/wiki/Category:プログラミング言語の実装 "wikilink")

1.  [Inside Windows: An In-Depth Look into the Win32 Portable Executable File Format - MSDN Magazine, February 2002](https://msdn.microsoft.com/en-us/magazine/bb985992.aspx). "Every PE file begins with a small MS-DOS executable. ... The first bytes of a PE file begin with the traditional MS-DOS header, called an IMAGE_DOS_HEADER. The only two values of any importance are e_magic and e_lfanew. ... The e_magic field (a WORD) needs to be set to the value 0x5A4D. ... In ASCII representation, 0x5A4D is MZ, the initials of Mark Zbikowski, one of the original architects of MS-DOS."