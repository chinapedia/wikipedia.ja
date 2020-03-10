> この記事は[LPAR](https://ja.wikipedia.org/wiki/LPAR)から翻訳されています。


**LPAR** (えるぱー、**L**ogical **PAR**titioning：論理分割、および **Logical PAR**tition：論理区画）は、[コンピュータ](../Page/コンピュータ.md "wikilink")の[仮想化](../Page/仮想化.md "wikilink")技術のひとつで、[仮想機械](../Page/仮想機械.md "wikilink")を実現する技術のひとつであり、またその技術により実現された論理区画である。

## 概要

LPARは、主に[ファームウェア](../Page/ファームウェア.md "wikilink")である[スーパーバイザ](https://ja.wikipedia.org/wiki/スーパーバイザ "wikilink")の機能により実現し、ひとつのコンピュータに、論理的に多数の仮想機械を作成し、それぞれで[OSを起動できる](../Page/オペレーティングシステム.md "wikilink")。

類似の仮想化技術である**[PPAR](https://ja.wikipedia.org/wiki/PPAR "wikilink")**（物理分割、物理区画）と比較すると、PPARはハードウェアの機種（モデル）ごとに予め決められた物理的な構成（ビルディングブロック）でのみ分割できるのに対し、LPARは1つのビルディングブロックのみのマシンでも使用でき、リソース（[CPU](../Page/CPU.md "wikilink")、[メモリ](../Page/主記憶装置.md "wikilink")、I/Oなど）をより細かく柔軟に配分・変更できる。また**仮想化OS**と比較すると、仮想化OSは柔軟性では優れているが、LPARは信頼性や負荷（[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")）の少なさでは優れている。PPAR、LPAR、仮想化OSは組み合わせて使う場合も多い。

## 歴史

  - [1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink") IBM[メインフレーム](../Page/メインフレーム.md "wikilink")用のLPARである[PR/SM](https://ja.wikipedia.org/wiki/PR/SM "wikilink")が登場
  - [2001年](../Page/2001年.md "wikilink") IBM pSeries用のLPARが登場 （[POWER4](https://ja.wikipedia.org/wiki/POWER4 "wikilink")）
  - [2002年](../Page/2002年.md "wikilink") [Dynamic Logical Partitioning](https://ja.wikipedia.org/wiki/Dynamic_Logical_Partitioning "wikilink") ([POWER4](https://ja.wikipedia.org/wiki/POWER4 "wikilink")および[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")5.2)
  - [2004年](../Page/2004年.md "wikilink") [Micro-Partitioning](https://ja.wikipedia.org/wiki/Micro-Partitioning "wikilink") （[POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink")）
  - [2007年](../Page/2007年.md "wikilink") [Live Partition Mobility](https://ja.wikipedia.org/wiki/Live_Partition_Mobility "wikilink") ([POWER6](https://ja.wikipedia.org/wiki/POWER6 "wikilink"))

## メインフレーム

[メインフレーム](../Page/メインフレーム.md "wikilink")のLPARは[IBM](../Page/IBM.md "wikilink")の[PR/SM](https://ja.wikipedia.org/wiki/PR/SM "wikilink")により登場した。個々のLPARでは[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")、[z/VM](https://ja.wikipedia.org/wiki/z/VM "wikilink")、[z/VSE](https://ja.wikipedia.org/wiki/z/VSE "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") on System z などが稼働できる。

## Power Systems

[IBM](../Page/IBM.md "wikilink")の[UNIX](../Page/UNIX.md "wikilink")サーバの[System p](https://ja.wikipedia.org/wiki/System_p "wikilink")（および[日立製作所](../Page/日立製作所.md "wikilink")の EP8000）、ミッドレンジの[System i](https://ja.wikipedia.org/wiki/System_i "wikilink")、両者を統合した[Power Systemsに搭載されている](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")。個々のLPARでは[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[IBM i](https://ja.wikipedia.org/wiki/IBM_i "wikilink")（旧称i5/OS、OS/400）、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") on Power (ただしEP8000ではAIXのみ)などが稼働できる。

Power Systemsでは、LPARは**[PowerVM](https://ja.wikipedia.org/wiki/PowerVM "wikilink")**のひとつの機能と位置づけられている。エディションにより、サーバ当たり3、CPUコア数当たり10などのLPARが作成できる。

[POWER4](https://ja.wikipedia.org/wiki/POWER4 "wikilink")からはOSやアプリケーションの停止を伴わずに動的にリソース割当を変更できる [Dynamic LPAR](https://ja.wikipedia.org/wiki/:en:Dynamic_Logical_Partitioning "wikilink") (D-LPAR)、[POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink")からは 1/100 単位（最低 1/10)でCPUリソースを割当できる[Micro-Partitioning](https://ja.wikipedia.org/wiki/Micro-Partitioning "wikilink")、[POWER6](https://ja.wikipedia.org/wiki/POWER6 "wikilink")からは稼働中に LPAR が物理システム（筐体）間を移動できる [Live Partition Mobility](https://ja.wikipedia.org/wiki/Live_Partition_Mobility "wikilink") が使用可能となった。また[クラスタリング](https://ja.wikipedia.org/wiki/クラスタリング "wikilink")ソフトウェアの [PowerHA](https://ja.wikipedia.org/wiki/PowerHA "wikilink")などと連動して、LPARが移動した先のシステムで自動的にリソースの割当を増やす機能などが追加された。

## 関連項目

  - [仮想化](../Page/仮想化.md "wikilink")
  - [ハイパーバイザ](../Page/ハイパーバイザ.md "wikilink")
  - [PowerVM](https://ja.wikipedia.org/wiki/PowerVM "wikilink")
      - [Dynamic Logical Partitioning](https://ja.wikipedia.org/wiki/Dynamic_Logical_Partitioning "wikilink")
      - [Micro-Partitioning](https://ja.wikipedia.org/wiki/Micro-Partitioning "wikilink")
      - [Live Partition Mobility](https://ja.wikipedia.org/wiki/Live_Partition_Mobility "wikilink")

## 外部リンク

  - [IBM - PowerVM](http://www-06.ibm.com/systems/jp/p/technology/virtualization/editions/)
  - [IBM - Advanced POWER Virtualizationの歴史](http://www-06.ibm.com/systems/jp/p/technology/apv/timeline.html)
  - [IBM RedBook - LPAR Simplification Tools Handbook](http://www.redbooks.ibm.com/abstracts/sg247231.html?Open)

[Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink")