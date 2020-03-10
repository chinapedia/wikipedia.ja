> この記事は[PowerVM](https://ja.wikipedia.org/wiki/PowerVM)から翻訳されています。


**PowerVM**（パワーヴイエム）は、従来は**Advanced Power Virtualization** (APV)と呼ばれていたもので、[IBM](../Page/IBM.md "wikilink") [Power Systemsの](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")[仮想化](../Page/仮想化.md "wikilink")技術の総称であり、[POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink")や[POWER6](https://ja.wikipedia.org/wiki/POWER6 "wikilink")や[POWER7](https://ja.wikipedia.org/wiki/POWER7 "wikilink")のプロセッサを搭載した[サーバ](../Page/サーバ.md "wikilink")ーの仮想化テクノロジーの統合名称で、ハードウェア、ソフトウェアの仮想化に関わる機能全体を包括している。

ハードウェア（ファームウェア）に埋め込まれたPOWERハイパーバイザーによって、高速で信頼性の高い仮想化環境を実現している。稼動[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は、[IBM i](https://ja.wikipedia.org/wiki/IBM_i "wikilink")、[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")に加え、Red HatやNovellから提供されている[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")をサポートしている。

## 概要

PowerVM は以下の機能を含んでいる。

  - [ファームウェア](../Page/ファームウェア.md "wikilink")による[LPAR](../Page/LPAR.md "wikilink")（論理分割）
      - 動的なリソース割当変更が可能な[Dynamic Logical Partitioning](https://ja.wikipedia.org/wiki/Dynamic_Logical_Partitioning "wikilink")
      - 1/100 単位の[CPU](../Page/CPU.md "wikilink")割当が可能な[Micro-Partitioning](https://ja.wikipedia.org/wiki/Micro-Partitioning "wikilink")
      - 稼働中に物理マシン間の移動が可能な[Live Partition Mobility](https://ja.wikipedia.org/wiki/Live_Partition_Mobility "wikilink")
  - I/O仮想化を提供する [Virtual I/O Server](https://ja.wikipedia.org/wiki/Virtual_I/O_Server "wikilink") (VIOS)と仮想[イーサネット](../Page/イーサネット.md "wikilink")
  - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink") [32ビット](../Page/32ビット.md "wikilink") [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")アプリケーションを無修正でPOWER上で実行できる [Lx86](https://ja.wikipedia.org/wiki/Lx86 "wikilink")

PowerVMは以下の3エディションから構成され、含まれる機能が異なる。

  - PowerVM Express
  - PowerVM Standard
  - PowerVM Enterprise

## 外部リンク

  - [Overview of Advanced POWER Virtualization](http://www-03.ibm.com/systems/power/software/virtualization/)
  - [IBM Redbooks | PowerVM Virtualization on IBM System p: Introduction and Configuration](http://www.redbooks.ibm.com/abstracts/sg247940.html?Open)
  - [IBM Redbooks | PowerVM Virtualization on IBM System p: Managing and Monitoring](http://www.redbooks.ibm.com/abstracts/sg247590.html?Open)
  - [Hands-on type article on setting up logical partitions using the Virtual I/O Server](http://www.ibm.com/developerworks/aix/library/au-aix-vioserver-v2/index.html)
  - [Virtual I/O Server Commands Reference](http://publib.boulder.ibm.com/infocenter/eserver/v1r3s/topic/iphcg/iphcg.pdf)

## 関連項目

  - [仮想マシンの比較(英語)](https://ja.wikipedia.org/wiki/:en:Comparison_of_platform_virtual_machines "wikilink")
  - [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")
  - [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") on Power
  - [POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink")
  - [POWER6](https://ja.wikipedia.org/wiki/POWER6 "wikilink")
  - [POWER7](https://ja.wikipedia.org/wiki/POWER7 "wikilink")

## 外部リンク

  - [IBM Website on AIX](http://www.ibm.com/servers/aix/)
  - [IBM Website on System p](http://www.ibm.com/systems/p/)
  - [PowerVM Wiki](http://www.ibm.com/developerworks/wikis/display/virtualization/Home)
  - [AIX 6 Open Beta](http://www.ibm.com/servers/aix/6/beta.html)
  - [PowerVM Editions Formerly Advanced POWER Virtualization (APV)](http://www.ibm.com/systems/power/software/virtualization/)
  - [PowerVM Editions Support](http://www.pseriestech.org/forum/ibm-powervm-editions/)
  - [PowerVM - 日本IBM](http://www-06.ibm.com/systems/jp/power/techinfo/powervm/)

[Category:IBMのソフトウェア](https://ja.wikipedia.org/wiki/Category:IBMのソフトウェア "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")