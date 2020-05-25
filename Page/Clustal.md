> この記事は[Clustal](https://ja.wikipedia.org/wiki/Clustal)から翻訳されています。


**Clustal**は広く用いられている[多重整列](../Page/多重整列.md "wikilink")プログラムである。現在はコマンドライン版の**Clustal W**とグラフィカルインターフェース（[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")）版の**Clustal X**とがある。[欧州バイオインフォマティクス研究所](https://ja.wikipedia.org/wiki/欧州バイオインフォマティクス研究所 "wikilink")の[FTPサーバ](ftp://ftp.ebi.ac.uk/pub/software/clustalw2/)から入手できる。

## アルゴリズム

以下の3つの段階を踏む。

1.  1対1の整列（ペアワイズアラインメント）を行う
      -
        1対1の整列を総当たりで行い、配列一致度の行列を作成する。
2.  配列一致度に基づいて樹形図（Guide Tree）を得る
      -
        配列一致度を距離尺度に用いて階層型[クラスタリングを行う](https://ja.wikipedia.org/wiki/データ・クラスタリング "wikilink")。この際のアルゴリズムは[近隣結合法](../Page/近隣結合法.md "wikilink")（または[非加重結合法](https://ja.wikipedia.org/wiki/非加重結合法 "wikilink")）が用いられている。
3.  樹形図に沿って配列を追加しながら整列を行う
      -
        最も一致度の高い配列ペアからはじめて、樹形図に沿って1つずつ配列を追加しながら整列させていくことで効率的に多重整列を得る。

これらは自動的に行われるが、ガイドツリーのみを計算させたり、ガイドツリーを指定して多重整列のみを行わせることもできる。

## 入出力

入力ファイルとしてはNBRF/PIR, [FASTA](../Page/FASTA.md "wikilink"), EMBL/Swissprot, Clustal, GCC/MSF, GCG9 RSF , GDEの形式を受け付け、Clustal, NBRF/PIR, GCG/MSF, [PHYLIP](https://ja.wikipedia.org/wiki/PHYLIP "wikilink"), GDE, NEXUSの形式で出力することができる。

## 系統解析

多重整列を行う目的の1つに分子系統解析があるが、Clustalで系統解析を行うことも可能である。ただし近隣結合法を用いたきわめてシンプルな解析に限られる。多重整列の際に作成される樹形図 (.dnd) は系統樹ではないことに注意が必要である。

## 履歴

  - 1988年、Higginsにより最初のバージョンが公表される\[1\]。これは上記アルゴリズムの3段階に対応する3つのプログラム (Clustal1, Clustal2, Clustal3) からなるパッケージであり、すべてIBM AT機用のMicrosoft [Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")で書かれていた。ペアワイズアラインメントと多重整列はWilbur and Lipmanのアルゴリズム、クラスタリングは[非加重結合法](https://ja.wikipedia.org/wiki/非加重結合法 "wikilink")を使用していた。
  - 1989年、HigginsによりClustal3の改良版Clustal4が公表される\[2\]。これは多重整列のアルゴリズムにMyers and Millerの変法を採用することで、少ないメモリでも類縁性の低い配列を整列できるようにしたものである。
  - 1992年、Higginsにより**Clustal V**が公表される\[3\]。これは[C言語](../Page/C言語.md "wikilink") (C89) で書き直された単一のプログラムであり、[VAX](../Page/VAX.md "wikilink")/[VMS](../Page/OpenVMS.md "wikilink")・[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")・[Macintosh](../Page/Macintosh.md "wikilink")・[MS-DOS](../Page/MS-DOS.md "wikilink")で利用可能だった。入出力のファイル形式が多様になり、整列済みファイルの再整列や[近隣結合法](../Page/近隣結合法.md "wikilink")による系統樹の作成ができるようになった。
  - 1994年、Thompsonによって**Clustal W**が公表される\[4\]。クラスタリングが近隣結合法に変更され、多重整列にも配列ごとに重み付けを行うなど様々な改良が施されている。以後継続的にチューニングが施され続けている。
  - 1997年、Thompsonによって[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")版の**Clustal X**が公表される\[5\]。[GUIツールキット](https://ja.wikipedia.org/wiki/GUIツールキット "wikilink")として[NCBI](https://ja.wikipedia.org/wiki/NCBI "wikilink")のvibrant toolboxを使用しており、[X Window System](../Page/X_Window_System.md "wikilink")・Macintosh・Microsoft Windowsで利用できる。多重整列された配列をウィンドウシステムによってスクロールしながら調べることができ、低クオリティ領域をマークしてそこだけ整列し直すようなことが可能になった。
  - 2007年、Larkinによって**Clustal W**および**Clustal X**のバージョン2.0が公表される\[6\]。これは[C++](../Page/C++.md "wikilink")によって書き直されており、これによりClustal Xはツールキットとして[Qt](../Page/Qt.md "wikilink")を利用するように変更された。機能面での進歩は大きくなく、クラスタリングのアルゴリズムとして非加重結合法を選べるようになったことと、配列を一旦取り除いてから再度整列し直すことで結果を改善する機能が追加されたのみである。

## その他

[SGIによるものをはじめとして](../Page/シリコングラフィックス.md "wikilink")、いくつかの並列化バージョンが開発されている。Clustal Wを高速に実行するための[FPGA](../Page/FPGA.md "wikilink")による専用ハードウェアが[Progeniq](http://www.progeniq.com)社によって開発されている。

## 参考文献

[Category:バイオインフォマティクス](https://ja.wikipedia.org/wiki/Category:バイオインフォマティクス "wikilink")

1.
2.
3.
4.
5.
6.