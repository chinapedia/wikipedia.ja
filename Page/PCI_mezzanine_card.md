> この記事は[PCI mezzanine card](https://ja.wikipedia.org/wiki/PCI_mezzanine_card)から翻訳されています。


**PCI mezzanine card**(PMC)はIEEE P1386.1規格にのっとって製造されるプリント基板のこと。[PCIの電気的仕様とCommon](../Page/Peripheral_Component_Interconnect.md "wikilink") mezzanine card(CMC;IEEE P1386規格)を組み合わせている。

PMCには32bitPCIをサポートする2つのコネクタ(P1とP2)を持つもの、64bitPCIをサポートする3つのコネクタを持つもの(P1,P2,P3)、規格化されていない入出力信号をサポートするためのP4コネクタを持つものがある。さらに、任意のコネクタが前面パネルかベゼルに配置される。

PMC規格はコネクタ中のどのピンがどのPCI信号に割り当てられるか定義している。さらに任意の入出力信号に使用されるオプションのP4コネクタについても定義している。

PMCは実績のあるPCIバス互換ではあるが、標準のPCIカードを使うよりも小さくより頑丈な製品をつくることを可能にした。mezzanineという単語は建物の2つの階の間に挿入された段（[中二階](https://ja.wikipedia.org/wiki/中二階 "wikilink")）を意味し、コネクタと支柱で基板のうちの一つに取り付けられて、標準カードラックで隣接した基板の間に設置される状態を形容している。Single PMCは74mm x 149mmの寸法である。規格には2倍のサイズの基板も定義されているがほとんど使用されない。

PMCが取り付けられる基板は通常[Eurocard](https://ja.wikipedia.org/wiki/Eurocard "wikilink")サイズで作られた、Single height,Double height,Triple heightのVMEバス基板や[CompactPCI](https://ja.wikipedia.org/wiki/CompactPCI "wikilink")基板などである。

PMC規格によってシリアル通信、[SCSI](../Page/Small_Computer_System_Interface.md "wikilink")、グラフィックコントローラ、[FireWireなど様々なI](https://ja.wikipedia.org/wiki/IEEE1394 "wikilink")/Oカードが使用できるようになっている。

## 関連規格

次のようなPMCの関連規格が存在する。

  - PMC-X ([PCI-X](../Page/PCI-X.md "wikilink") PMC) VITA 39規格
  - PPMC (processor PMC) VITA 32規格
  - CCPMC (conduction-cooled PMC) VITA 20規格
  - XMC (PMC with high-speed serial fabric interconnect) VITA 42規格。XMCは[PCI Express](../Page/PCI_Express.md "wikilink")(VITA 42.3規格)かSerial RapidIO(VITA 42.2規格)とParallel RapdIO(VITA 42.1規格)のような他の高速シリアル通信をサポートする5番目のコネクタ(P5)を規定している。

## 外部リンク

  - [What is PMC? (with schematic drawings)](http://www.gocct.com/sheets/pmc.htm)
  - [VME board with a PMC slot](http://www.extensionmedia.com/interconnect/datasheet.php?ds=27)
  - [Picture of an PMC graphics card (with ATI Radeon chip)](http://www.gocct.com/sheets/picture/iopmcdg1.htm)

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")