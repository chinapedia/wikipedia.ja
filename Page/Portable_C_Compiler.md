> この記事は[Portable C Compiler](https://ja.wikipedia.org/wiki/Portable_C_Compiler)から翻訳されています。


**Portable C Compiler** (略して **pcc**) は[ベル研究所](../Page/ベル研究所.md "wikilink")の[スティーヴン・カーティス・ジョンソン](https://ja.wikipedia.org/wiki/スティーヴン・カーティス・ジョンソン "wikilink")が1970年代に書いた[C言語](../Page/C言語.md "wikilink")コンパイラである\[1\]。異なるアーキテクチャ用のコードを出力することが容易な[コンパイラ](../Page/コンパイラ.md "wikilink")の先駆けであり、1980年代初期には多くのCコンパイラが**pcc**をもとにしていた\[2\]。[Version 7 Unixで](../Page/Version_7_Unix.md "wikilink")[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")のコンパイラに代わって採用されたあとは、1990年の[4.3BSD](https://ja.wikipedia.org/wiki/4.3BSD "wikilink")-Renoに含まれるなど、[4.4BSD](https://ja.wikipedia.org/wiki/4.4BSD "wikilink")で[GNU Cコンパイラに取って代わられるまで](../Page/GNUコンパイラコレクション.md "wikilink")、長く標準コンパイラとして君臨していた。

**pcc**の成功の鍵は移植性と診断能力にある。

  - ソースファイルの大部分がマシン非依存である。
  - 文法違反に強く、不正なプログラムを受け付けない。[lint](https://ja.wikipedia.org/wiki/lint "wikilink")はもともと**pcc**の一部だった。
  - pass1の時点でも最適化する。

こうした特徴を持つコンパイラは当時としては斬新で、たとえば[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")による最初のCコンパイラは[PDP-11](../Page/PDP-11.md "wikilink")に強く依存していた。

なお、**pcc**は[Alan Snyderによる別のportable](https://ja.wikipedia.org/wiki/Alan_Snyder "wikilink") C compilerからアイディアを取り入れているが、Snyderのものは遅く複雑で、実装上の問題もあった。

## 現在(2014年12月10日)

近年では[Anders MagnussonがC](https://ja.wikipedia.org/wiki/Anders_Magnusson "wikilink")99対応を目指して開発を続けており、2007年9月には[NetBSD](../Page/NetBSD.md "wikilink")の[pkgsrc](https://ja.wikipedia.org/wiki/pkgsrc "wikilink")と[OpenBSD](../Page/OpenBSD.md "wikilink")のソースツリーに導入された\[3\]。どちらもまだ標準コンパイラとして利用しているわけではないが、[GCCより軽量でメンテナンスしやすく](../Page/GNUコンパイラコレクション.md "wikilink")、BSDライセンスであることから、関心が高まっている\[4\]。

利用者の観点からGCCと比較すると、以下の大きな違いがある。これは両者の目標とするものが異なるためである。

  - **pcc**自体が小さく、ビルドしやすい。移植も容易である。
  - **pcc**自体の動作が高速である。
  - 出力されるコードが大きく、遅い。GCCは各種最適化に優れている。

2011年4月1日、PCC version 1.0がついにリリースされた。BSD FundのプログラムマネジャーであるMichael Dexterは、プロジェクトへの寄付者に向けて、こう語っている。

2014年12月10日、PCC version 1.1がリリースされた。

## 関連項目

  - [clang](https://ja.wikipedia.org/wiki/clang "wikilink")

## 参考文献

  - [Johnson, S.C.](https://ja.wikipedia.org/wiki/スティーヴン・カーティス・ジョンソン "wikilink") (1978). "A portable compiler: theory and practice". Proceedings of the 5th ACM SIGACT-SIGPLAN symposium on Principles of programming languages. Tucson, Arizona. pp. 97-104. [Online reprint at ACM.](http://doi.acm.org/10.1145/512760.512771)
  - [Ritchie, Dennis M.](../Page/デニス・リッチー.md "wikilink") (1993). "The development of the C language". The second ACM SIGPLAN conference on History of programming languages. Cambridge, Massachusetts. pp. 201-208. [Online reprint.](https://www.bell-labs.com/usr/dmr/www/chist.html)
  - [Snyder, A.](https://ja.wikipedia.org/wiki/Alan_Snyder "wikilink") (1975). "A Portable Compiler for the Language C". Master’s Thesis. M.I.T., Cambridge, Mass. [Online reprint.](http://www.lcs.mit.edu/publications/specpub.php?id=717)
  - [Johnson, S.C.](https://ja.wikipedia.org/wiki/スティーヴン・カーティス・ジョンソン "wikilink") (1981). "A Tour Through the Portable C Compiler". Unix Programmer's Manual, 7th edition, Volume 2, ISBN 0-03-061743-X. [Online version.](http://citeseer.ist.psu.edu/johnson81tour.html) ([mirror](ftp://226.net120.skekraft.net/pcc/porttour.ps))

## 脚注

<references/>

## 外部リンク

  - [初期のソースコード](http://minnie.tuhs.org/cgi-bin/utree.pl?file=V7/usr/src/cmd/pcc)
  - [Anders Magnusson 版の PCC サイト](http://pcc.ludd.ltu.se/)
  - [BSD Licensed PCC Compiler Imported, OpenBSD Journal](http://undeadly.org/cgi?action=article&sid=20070915195203&mode=flat&count=0)
  - [スラッシュドット ジャパン | OpenBSD が PCC をソースツリーに投入](http://slashdot.jp/bsd/article.pl?sid=07/09/17/0920228)

[Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink")

1.  [A portable compiler: theory and practice](http://doi.acm.org/10.1145/512760.512771)
2.  [The Development of the C Language](http://cm.bell-labs.com/cm/cs/who/dmr/chist.html)
3.  ['CVS: cvs.openbsd.org: src' - MARC](http://marc.info/?l=openbsd-cvs&m=118988004013923&w=2)
4.  [Slashdot | GCC Compiler Finally Supplanted by PCC?](http://developers.slashdot.org/article.pl?sid=07/09/17/1451239)