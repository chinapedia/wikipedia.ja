> この記事は[Beowulf](https://ja.wikipedia.org/wiki/Beowulf)から翻訳されています。


**Beowulf**は、[コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")を構成する方式の名前で、[Linux](../Page/Linux.md "wikilink")や[BSD系OS](https://ja.wikipedia.org/wiki/BSD系OS "wikilink")などのフリーな[PC-UNIX](https://ja.wikipedia.org/wiki/PC-UNIX "wikilink")を載せた[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")の[クラスターによる](../Page/コンピュータ・クラスター.md "wikilink")[高性能計算](../Page/高性能計算.md "wikilink")の実現法である。

"Beowulf"とはあくまで方式に付けられた名称である。Beowulfを構成するに当たってそれぞれ使うソフトウェアは異なり特に必要な要素となるソフトウエアの部品はない。

## Beowulfの特徴

  - フリーのUNIXのソースコードの改造により実現される。
  - 一般的に販売されているPCを複数使って作られる。
  - ノードとなるコンピュータクラスターを構成する各コンピュータは、クラスターの処理のためにだけ使われる。
  - ノードは、クラスター専用に使われる高速のネットワークにより接続されている。
  - クラスターとして使われる目的は、あくまで高速な処理をするためで、クラスターとしての別の目的である処理などの信頼性のためではない。

## Beowulfを構成するためのソフトウェア

  - LinuxやBSD系のフリーなUNIXなど。
  - 特に共通して使われる他のソフトウェアはないが、以下のどれかが使われる事が多い。
      - 並列処理ライブラリー：
    <!-- end list -->
      -
        プログラマが計算の単位(タスク)を、分割してネットワーク上のコンピュータに送り、計算の結果を収集する。
          - [MPI](../Page/Message_Passing_Interface.md "wikilink") (Message Passing Interface)
          - [PVM](https://ja.wikipedia.org/wiki/PVM "wikilink") (Parallel Virtual Machine)
    <!-- end list -->
      - その他

## 参照

  - [コンピュータ・クラスター](../Page/コンピュータ・クラスター.md "wikilink")、[並列コンピュータ](https://ja.wikipedia.org/wiki/並列コンピュータ "wikilink")、[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")、[コンピュータ・グリッド](https://ja.wikipedia.org/wiki/コンピュータ・グリッド "wikilink")

他のクラスターコンピュータ：[MOSIX](https://ja.wikipedia.org/wiki/MOSIX "wikilink")。

## 外部リンク

  - [Beowulf.org](http://www.beowulf.org/)
  - [Home build](http://clustercompute.com/)
  - [Cluster Monkey](http://www.clustermonkey.net/) Free On-line Cluster Magazine
  - [LinuxHPC.org](http://www.linuxhpc.org/)
  - [MPI homepage](http://www-unix.mcs.anl.gov/mpi/)
  - [KLAT2](http://aggregate.org/KLAT2/)
  - [Cluster Builder](http://www.clusterbuilder.org)
  - [NPACI Rocks](http://www.rocksclusters.org)
  - [Project Kusu](http://www.osgdc.org) HPC Cluster Toolkit
  - [Engineering a Beowulf-style Compute Cluster](http://www.phy.duke.edu/~rgb/Beowulf/beowulf_book/beowulf_book/index.html)
  - [KASY0 (Kentucky ASYmmetric Zero)](http://aggregate.org/KASY0/)

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:計算科学](https://ja.wikipedia.org/wiki/Category:計算科学 "wikilink")