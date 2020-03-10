> この記事は[Netwide Assembler](https://ja.wikipedia.org/wiki/Netwide_Assembler)から翻訳されています。


**Netwide Assembler** (**NASM**) は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")を対象とした[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")の[アセンブラであり](../Page/アセンブリ言語.md "wikilink")、[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink")、[32ビット](https://ja.wikipedia.org/wiki/32ビット "wikilink") ([IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink"))、[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")すべてのコード生成に対応している。

NASMは当初、Julian HallとSimon Tathamが作成していたが、現在はH. Peter Anvinを中心とした少人数のチームによって開発されている。また、当初は独自の[ライセンス](../Page/ライセンス.md "wikilink")によって公開されていたが、後に[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")に変更している。

NASMは[COFF](https://ja.wikipedia.org/wiki/COFF "wikilink")、[a.out形式](https://ja.wikipedia.org/wiki/a.outフォーマット "wikilink")、[ELF](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")、ネイティブ[MINIX](https://ja.wikipedia.org/wiki/MINIX "wikilink")形式など様々な種類の形式の出力に対応している。フラットな単なる[機械語](../Page/機械語.md "wikilink")のファイルも出力でき、[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")ローダや[ROMイメージ](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")開発などに用いることもできる。またNASMは独自の形式として[RDOFF](https://ja.wikipedia.org/wiki/RDOFF "wikilink")を定めている。これは単純かつ実用的であるよう設計され、クロスアセンブルにも適するという特徴を持っている。なお、[SPARC](../Page/SPARC.md "wikilink")や[PowerPC](../Page/PowerPC.md "wikilink")などx86以外でNASMを実行することもできる。その場合、当然そのコンピュータではNASMの出力したプログラムを実行できない。

NASMの哲学は、[プログラマ](../Page/プログラマ.md "wikilink")が簡単に理解できるインテル[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")として親しまれるようにするということである。そのため従来のインテル構文を採用し（[GNUアセンブラ](https://ja.wikipedia.org/wiki/GNUアセンブラ "wikilink") (GAS)ではAT\&T構文を採用）、[MASMやその互換アセンブラに存在するセグメントオーバーライドプレフィックスの自動生成](https://ja.wikipedia.org/wiki/Microsoft_Macro_Assembler "wikilink")（ASSUME擬似命令など）は搭載していない。

## 関連項目

  - [アセンブリ言語](../Page/アセンブリ言語.md "wikilink")
  - [YASM](https://ja.wikipedia.org/wiki/YASM "wikilink")（NASMを基に64ビット対応したもの）
  - [NASK](https://ja.wikipedia.org/wiki/NASK "wikilink")（NASM互換のアセンブラ、[OSASK](../Page/OSASK.md "wikilink")の開発に使用された）
  - [RDOFF](https://ja.wikipedia.org/wiki/RDOFF "wikilink")

## 外部リンク

  - [NASM](http://www.nasm.us/)

[Category:アセンブラ](https://ja.wikipedia.org/wiki/Category:アセンブラ "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:リバースエンジニアリング](https://ja.wikipedia.org/wiki/Category:リバースエンジニアリング "wikilink")