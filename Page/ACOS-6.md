> この記事は[ACOS-6](https://ja.wikipedia.org/wiki/ACOS-6)から翻訳されています。


**ACOS-6**（エイコスシックス）は[日本電気](../Page/日本電気.md "wikilink")の[メインフレーム](../Page/メインフレーム.md "wikilink")および[OSである](../Page/オペレーティングシステム.md "wikilink")[ACOSの一系列である](../Page/Advanced_Comprehensive_Operating_System.md "wikilink")。同社のメインフレーム事業草創期に[ハネウェル](../Page/ハネウェル.md "wikilink")社から導入した技術が元となっている。ただし、元にしたハネウェルの技術の内訳には、ハネウェルが[GEから買収したコンピュータ部門の所有していたものが多く含まれている](https://ja.wikipedia.org/wiki/ゼネラルエレクトリック "wikilink")（たとえば、[MITがGEのマシンを使用して開発していた](../Page/マサチューセッツ工科大学.md "wikilink")[Multics](../Page/Multics.md "wikilink")の技術の一部を含む）。

[2003年](../Page/2003年.md "wikilink")現在の名称はACOS-6/NVX PX、対象となるハードウェアはパラレルACOS PX7900である。

## アーキテクチャ

数少ない[ワードマシン](https://ja.wikipedia.org/wiki/ワードマシン "wikilink")である。1[バイト](../Page/バイト_\(情報\).md "wikilink")=9[ビット](../Page/ビット.md "wikilink")で処理をし、1[ワード](../Page/ワード.md "wikilink")=36[ビット](../Page/ビット.md "wikilink")である。

初期のアーキテクチャと後期のアーキテクチャではかなり構造が異なる。

### システム構成

コンピュータの中心にSCU（システム制御ユニット）があり、この配下に演算部(EPU)、メモリ、入出力プロセッサ(IOP)が繋がる。パラレルACOS以前は、初期の機種を除き、1つのSCUに最大2つのEPUを繋げることが出来る。システム2000では、SCPを2つ繋げて、1つのシステムとして4EPUをサポートしている。

### 2つのモード

RモードとVモードという2つのモードがある。

#### Rモード

Rモードは、18ビットのメモリ空間（256Kワード=1Mバイト）の中で処理をする。その範囲でフラットなメモリ空間を提供する。アドレス空間が18ビットしかないので、最大256Kワード（=1Mバイト）しかアクセスできない。しかし、アドレスマッピングのためのレジスタがあり、256Kワード以上のメモリ空間をアクセスできる仕組みが用意されている。 アドレスマッピング機能はVモードでは無効になる。

#### Vモード

Vモードは、セグメントを多用し、各種の保護機能を付加し、さらにメモリ空間を拡張したモードである。[80386](https://ja.wikipedia.org/wiki/80386 "wikilink")のプロテクトモードのようなもの、と思うと理解が早い。アドレスレジスタがセグメントのポインタ+オフセットとなり(名前もデータレジスタと変わる）、セグメント記述子に指定されたメモリ空間、保護機能等が有効に働くようになる。1つのプログラムは、複数のセグメントから構成されるようになる。システム1000以降は、アドレス空間が拡張され、72ビットになる。ただし、Vモードは、ごく初期のマシン（システム600など）では利用できない。また、システム2000以降では、命令空間も拡張される。PentiumプロセッサのEM-64Tモードのようなもの、と思うと理解が早い。

#### 統合アレイプロセッサ

システム1000から取り入れられた機能である。ベクトル演算を実行する命令群である。システム2000からは、マスク制御付きベクトル演算が可能になり、FORTRANで、IF文を含むDOループがベクトル化可能になっている。1つのベクトル命令で処理可能な要素は、S1000では2の18乗個、S2000では2の36乗個である。

#### 拡張仮想計算機システム

システム2000から取り入れられた機能である。ハードウェアが仮想計算機機能をサポートするようになった。このため、同時に複数のOSを動作させることが出来るようになった。

### レジスタ構成

[レジスタが](../Page/レジスタ_\(コンピュータ\).md "wikilink")、他のアーキテクチャに比べて少ないのも特徴である。演算が可能なレジスタは A レジスタ と Q レジスタの2つしかない（それぞれ36ビット）。そのほかにインデックスレジスタ（18ビット）とアドレスレジスタが存在する。インデックスレジスタ、アドレスレジスタともに、実効アドレスを生成する際にアドレスを修飾する際に使われる。Vモードではアドレスレジスタの機能が変わる。

アドレスレジスタを使う場合には、命令語（36ビット）のアドレスレジスタを使用するためのビットをonにする。この時、インデックスフィールド（18ビット）の先頭3ビットがアドレスレジスタのレジスタ番号を指定するようになる。

### 命令体系

命令体系は比較的[COBOL](../Page/COBOL.md "wikilink")向けである。COBOLのMOVE、ADD、SUBTRACT等の演算命令をほぼ機械語レベルで1命令に対応可能である。そのため、データ部分の修飾機能が豊富で、パック/アンパック十進数を直接操作可能である。さらに、COBOLの文字列編集機能（PIC で指定するもの）をそのまま機械語に変換する機能もある。

最近のCPUのような、スタックの概念はRモードにはない。関数コールを行うときには、飛び先で戻りアドレスを保存するような処理が必要である。Vモードではスタックセグメントが存在する。

特権モードがある。特権モードに遷移する命令で特権モードに移行する。特権モードには複数のランク付けがされている。

### サービスプロセッサ

専用のサービスプロセッサがある。メインのOSが稼働するプロセッサとは別に、ファームウェアが動作するプロセッサがある。そのプロセッサに対して操作を行なうことで、メインのOSの起動等を行なえる。

### 文字コード

内部で使うコードは、6ビットの文字コードおよびJISコード([JIS X 0201](https://ja.wikipedia.org/wiki/JIS_X_0201 "wikilink"))である。6ビットの文字コードは、BCDコードと呼ばれ、英数字のみ（かつ、大文字のみ）のコードであり、1ワード中に6文字を詰め込んで処理をしている。内部処理ルーチン等で使われている。JISコードは、通常の（COBOL等の）文字処理を行なうときに利用されている。メインフレームではあるが、EBCDICを使っていない。日本語（漢字）は、[JIPS](../Page/JIPS.md "wikilink")(J)コードと呼ばれるコード体系を使っている。このコードには[ACOS-4](../Page/ACOS-4.md "wikilink")系で使われるJIPS(E)や、[A-VX](../Page/A-VX.md "wikilink")で使われるNEC内部コード(E)への変換手段が用意されている。

## OSの特徴

ACOS-6は[Multics](../Page/Multics.md "wikilink")の流れを汲むOSである。[UNIX](../Page/UNIX.md "wikilink")の遠い親戚とも言える。そのため、UNIXに似た（というようりも、Multics風の、と言うべきだろう）機能がある。

### ファイルシステム

  - FMSというファイルシステムは、UNIXのような階層構造ディレクトリを提供する。ただし、rootディレクトリは1つではなく、複数のトップディレクトリがあり得る。1ファイル名は12文字までである。使用できる文字は、英文字、数字文字と、"-"（ハイフン）などの一部の特殊記号。英文字に大文字と小文字の区別はない（そもそも基本となるキャラクタコードが6ビットのため、小文字用のコードを定義する場所が確保できなかった）。ディレクトリやファイルの間を区切る文字は、[UNIX](../Page/UNIX.md "wikilink")系OSと同じく"/"（スラッシュ文字）である。
  - 入出力が標準化されている。標準形式で書くのであれば、テープだろうがディスク上のファイルだろうが、細かなパラメータを指定しなくても簡単に入出力が行なえる。実デバイス（ファイル）とプログラム上の入出力の切り替え作業は、実行用のJCLを修正するだけで完了する。
  - TSSがUNIXのようなコマンドベース（初期のもの）である。TSS上で簡単にファイルの作成等が行える。UNIX上のedのような行指向エディタが用意されている。

## 歴史

  - ACOS-6
  - ACOS-6/MVX
  - ACOS-6/NVX
  - ACOS-6/NVX PX

## 関連項目

  - [GE-600シリーズ](../Page/GE-600シリーズ.md "wikilink")
  - [GCOS](../Page/GCOS.md "wikilink")
  - [Multics](../Page/Multics.md "wikilink")

## 参考文献

草創期のACOS-6開発の元となったOS技術情報の出自等について：

  -
  -
## 外部リンク

  -
  - \-GEやハネウェル（HIS）のコンピュータ部門を最終的に買収・手中に収めた[Bull](../Page/Bull.md "wikilink")から見たGCOSの歴史

  - [【日本電気】 ACOS-6](http://museum.ipsj.or.jp/computer/os/nec/0014.html) - コンピュータ博物館（[情報処理学会](../Page/情報処理学会.md "wikilink")）

[Category:メインフレームのオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:メインフレームのオペレーティングシステム "wikilink") [Category:日本電気の製品](https://ja.wikipedia.org/wiki/Category:日本電気の製品 "wikilink")