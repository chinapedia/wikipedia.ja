> この記事は[SBus](https://ja.wikipedia.org/wiki/SBus)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Sbus_cards.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Sbus_slots.jpg "wikilink")

**SBus**とは、1990年代に[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")から販売された[SPARC](../Page/SPARC.md "wikilink")をベースとしたたいていのコンピュータで使われた[コンピュータバスである](../Page/バス_\(コンピュータ\).md "wikilink")。[1989年](../Page/1989年.md "wikilink")に、高速なSPARCプロセッサに対する高速なバスとして導入された。より古い[モトローラ](../Page/モトローラ.md "wikilink")[68030ベースのシステムや初期のSPARCベースのシステムに採用されており](../Page/MC68030.md "wikilink")、当時既に時代遅れになりつつあった[VMEバス](../Page/VMEバス.md "wikilink")からの移行であった。1990年代初頭、サンはSPARCを「オープン」にしようと試みたので、SBusは標準バスのようになり、[IEEE1496](https://ja.wikipedia.org/wiki/IEEE1496 "wikilink")として標準化された。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、サンはSBusから[PCIへの移行をはじめ](../Page/Peripheral_Component_Interconnect.md "wikilink")、今日ではSBusはもはや使われていない。

## 概要

SBusはさまざまな点で「きれいな」デザインをしている。なぜなら、SPARCシステムだけをターゲットとしているので、[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")を実現するために発生する多くの問題を考慮する必要はなかったからである。SBusは[ビッグエンディアン](https://ja.wikipedia.org/wiki/ビッグエンディアン "wikilink")であり、32bitの[アドレスバス](https://ja.wikipedia.org/wiki/アドレスバス "wikilink")と[データバス](https://ja.wikipedia.org/wiki/データバス "wikilink")を持つ。クロックは16.6MHzから25MHzで動作し、100MB/sまでのデータ転送速度を誇る。各デバイスは、それぞれ28bitアドレス空間(256MB)にマッピングされる。SBusはマスターを8つまでサポートするが、スレーブの数には制限はない。

64bitの[UltraSPARC](https://ja.wikipedia.org/wiki/UltraSPARC "wikilink")が導入されたとき、SBusは、動作クロックを倍にして、1クロックあたり32bitデータを2つ転送することによって、64bitバスで200MB/sの転送速度を達成した。これに対して、2006年現在使用されている、66MHz/64bit PCI転送速度は528MB/sである。このSBusアーキテクチャの変種は、PCIの様々なバージョンの場合とは違って、以前と同じ96ピンコネクタを用いた。

SBusはPCIのように周辺機器内部接続用であった。サンのシステムは、CPUとメモリ間のバスには別の標準化された、[MBus](../Page/MBus.md "wikilink")と呼ばれるバスを使用した。

## 外部リンク

  - [PCI:SBus Comparison](http://www.sun.com/products-n-solutions/hardware/docs/pdf/805-7410-10.pdf) (PDF)
  - [PCIとSBusの機能比較](http://docs.sun.com/app/docs/doc/806-3917?l=ja)

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")