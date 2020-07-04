> この記事は[BladeCenter](https://ja.wikipedia.org/wiki/BladeCenter)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:IBM_bladecenter_\(front\).jpg "wikilink") [IBM_HS20_blade_server.jpg](https://ja.wikipedia.org/wiki/File:IBM_HS20_blade_server.jpg "fig:IBM_HS20_blade_server.jpg") [UPM-CeSViMa-SupercomputadorMagerit.jpg](https://ja.wikipedia.org/wiki/File:UPM-CeSViMa-SupercomputadorMagerit.jpg "fig:UPM-CeSViMa-SupercomputadorMagerit.jpg") supercomputer ([:en:CeSViMa](https://ja.wikipedia.org/wiki/:en:CeSViMa "wikilink")) has 86 Blade Centers (6 Blade Center E on each computing rack)\]\] **BladeCenter**（ブレードセンタ）は、[IBM](../Page/IBM.md "wikilink")が[2002年](../Page/2002年.md "wikilink")から発売していた[ブレードサーバ](../Page/ブレードサーバ.md "wikilink")のシリーズである。2014年以降は[レノボ社から販売とサポートが継続されていた](https://ja.wikipedia.org/wiki/Lenovo "wikilink")。2016年6月30日に営業活動終了している。

## 概要

BladeCenterは、米国IBMと[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")により[1999年](../Page/1999年.md "wikilink")から共同開発され、日本市場では2002年の第３四半期に[日本IBMから発表された](../Page/日本アイ・ビー・エム.md "wikilink")。開発はシャーシ部分をインテル社が担当し、ブレード部分をIBMが担当している。発表時点で、主要なサーバメーカーはブレードサーバを既に発表しており、市場では後発の製品であった。しかしインテル[CPU](../Page/CPU.md "wikilink")の消費電力の上昇や[InfiniBandなどの高性能I](https://ja.wikipedia.org/wiki/インフィニバンド "wikilink")/Oのサポート、シャーシ内の各部品の徹底した二重化による高信頼性、SANブートなどに対応している点など、先発のブレードサーバ製品との差別化要素となり、ブレードサーバ市場において発売以来一貫して高いシェアを有していた。[2005年](../Page/2005年.md "wikilink")には[直流](../Page/直流.md "wikilink")電源をサポートするBladeCenter Tが発表され、[2006年](../Page/2006年.md "wikilink")には[10ギガビット・イーサネット](../Page/10ギガビット・イーサネット.md "wikilink")などI/Oと電源を強化したBladeCenter H、[2007年](../Page/2007年.md "wikilink")にはAC100Vのサポートと筐体ストレージを組み込む機能が追加されたBladeCenter Sが発表された。BladeCenterの規格は、オープンコミュニティであるBlade Open Specification ([BOS](http://www-03.ibm.com/systems/bladecenter/resources/signin.html))で公開されており、サードパーティは技術情報を入手及び、BladeCenterに対応した製品を開発することが可能である。[2012年](../Page/2012年.md "wikilink")に後継製品となるFlex Systemが発表されたが、BladeCenterも2016年まで引き続き販売されていた。2014年のIBMのx86サーバ事業の事業売却により、以後は[Lenovo](https://ja.wikipedia.org/wiki/Lenovo "wikilink")社が、製品の販売とサポートを行っていた。2016年6月30日に営業活動終了している。

## シャーシ

### IBM BladeCenter (E)

[thumb](https://ja.wikipedia.org/wiki/ファイル:Bladecenter-front.jpg "wikilink") 最初のバージョンのBladeCenterの[シャーシ](../Page/シャーシ.md "wikilink")であり、現在の製品名は"BladeCenter E"である。"E"の意味は公表されていないが、"Enterprise"の略でないかと推測される。7Uのシャーシに14枚のブレードサーバを収納できる。2002年の発表時は1200W電源が搭載されていたが、モジュール交換により1400W,1800W,2000W,2320Wまでアップグレード可能である。2014年に営業活動終了。

  - 仕様
      - 14 ブレードスロット (7U)
      - メディアトレイ（標準）には各ブレードで共有可能な[光学ドライブ](../Page/光学ドライブ.md "wikilink")（当初[CD-ROM](../Page/CD-ROM.md "wikilink")、後にCD-ROM/[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink"))、[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") 1.1（後に2.0）ポートを備える。
      - 管理モジュール（Management ModuleもしくはAdvanced Management Module）は標準で1基、拡張で2基（1基は故障時の予備）まで追加可能
      - 電源モジュールは標準で2基、拡張で4基（2基は故障時の予備）まで追加可能
      - 冷却用ブロワーは標準で2基（1基は故障時の予備）
      - スイッチ用スロット1,2には[ギガビットイーサネット](https://ja.wikipedia.org/wiki/ギガビットイーサネット "wikilink")用スイッチ、もしくはパススルーモジュールを実装可能
      - スイッチ用スロット3,4には各種スイッチ（ギガビットイーサネット、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")、インフィニバンド、もしくはパススルーモジュールを実装可能

[File:Bladecenter-front.jpg|BladeCenter](File:Bladecenter-front.jpg%7CBladeCenter) E 前面 [File:Bladecenter-back.jpg|BladeCenter](File:Bladecenter-back.jpg%7CBladeCenter) E 背面

### IBM BladeCenter T

[NEBS](https://ja.wikipedia.org/wiki/:en:Network_Equipment-Building_System "wikilink") Level3の規格を満たした、主に通信業者向けのブレードシャーシである。 [DC](../Page/直流.md "wikilink") (48V) モデルと[AC](../Page/交流.md "wikilink") (200V) モデルを選択することができ、直流データセンターにおいても利用可能である。ブレードサーバ及びスイッチについてはBladeCenter Eと互換性が提供されている。この"T"の意味は公表されていないが、"[Telco](https://ja.wikipedia.org/wiki/:en:Telephone_company "wikilink")" の略でないかと推測される。2009年営業活動終了。

  - 仕様
      - 8ブレードスロット (8U)

### IBM BladeCenter H

[thumb](https://ja.wikipedia.org/wiki/ファイル:BladecenterH.jpg "wikilink") IBM BladeCenter Eの上位シャーシとして2006年に発売された。高速な光ファイバー通信に対応しているのが特徴である。BladeCenter Eとの間でスイッチやブレードについて互換性が保たれている。この"H"の意味については、公表されていないが、"High-speed"あるいは"High-end"の略でないかと推測される。2006年の発表時は2900W電源が搭載されていたが、モジュール交換により2980Wまでアップグレード可能。2016年に営業活動終了

  - 仕様
      - 14 ブレードスロット (9U)
      - メディアトレイ（標準）には各ブレードで共有可能な[光学ドライブ](../Page/光学ドライブ.md "wikilink")CD-ROM/[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink")（標準もしくはオプション）、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") 2.0ポートを備える。
      - 管理モジュール (Advanced Management Module) は標準で1基、拡張で2基（1基は故障時の予備）まで追加可能
      - 電源モジュールは標準で2基、拡張で4基（2基は故障時の予備）まで追加可能
      - 冷却用ブロワーは標準で2基（1基は故障時の予備）一部のシャーシは130W以上のCPUを搭載したブレードを装着する場合に拡張冷却モジュールに交換が必要
      - スイッチ用スロット1,2には[ギガビットイーサネット](https://ja.wikipedia.org/wiki/ギガビットイーサネット "wikilink")用スイッチ、もしくはパススルーモジュールを実装可能
      - スイッチ用スロット3,4には各種スイッチ（ギガビットイーサネット、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")、インフィニバンド）、もしくはパススルーモジュールを実装可能である。
      - スイッチ用スロット5,6はシャーシ側に高速スイッチ用として備えており、2010年現在はFCoE構成時のFibre Channel Gatewayスイッチを実装可能
      - スイッチ用スロット7,8,9,10は高速スイッチとして[10GbEスイッチ](../Page/10ギガビット・イーサネット.md "wikilink")、もしくはインフィニバンドスイッチを搭載可能である他、マルチスイッチインターコネクトモジュールを利用することで、スイッチ用スロット1,2,3,4用のオプションであるギガビットイーサネットスイッチ、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")スイッチ、パススルーモジュールを実装可能

[File:BladecenterH.jpg|BladeCenter](File:BladecenterH.jpg%7CBladeCenter) H 前面 [File:BladecenterHback.jpg|BladeCenter](File:BladecenterHback.jpg%7CBladeCenter) H 背面

### IBM BladeCenter HT

[NEBS](https://ja.wikipedia.org/wiki/:en:Network_Equipment-Building_System "wikilink") Level3の規格を満たした、主に通信業者向けのブレードシャーシであり、IBM BladeCenter Tの上位シャーシとして2007年に発売された。 [DC](../Page/直流.md "wikilink") (48V) モデルと[AC](../Page/交流.md "wikilink") (200V) モデルを選択することができ、直流データセンターにおいても利用可能である。ブレードサーバ及びスイッチについてはBladeCenter Hと互換性が提供されている。この"HT"の意味は公表されていないが、"High-Speed [Telco](https://ja.wikipedia.org/wiki/:en:Telephone_company "wikilink")"の略でないかと推測される。 2016年に営業活動終了

  - 仕様
      - 12 ブレードスロット (12U)

### IBM BladeCenter S

小規模なシステム構築のためのシャーシとして2007年に発売された。シャーシ内にブレード間で共有可能なストレージ（ハードディスク装置）を内蔵可能である他、100V (110V) 電源でも稼動可能であることなど、データセンターだけでなく、オフィスでも利用を可能とする仕様となっているのが大きな特徴である。この"S"の意味については、公表されていないが、"Small business"あるいは"Storage"の略でないかと推測される。

  - 仕様
      - 6ブレードスロット (7U)
      - メディアトレイ（標準）には各ブレードで共有可能な[光学ドライブ](../Page/光学ドライブ.md "wikilink")（CD-ROM/[DVD-ROM](https://ja.wikipedia.org/wiki/DVD-ROM "wikilink"))、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") 2.0ポートを備える。
      - 管理モジュール (Advanced Management Module) は標準で1基
      - 電源モジュールは100V/200V対応電源を標準で2基、拡張で4基まで追加可能である。
          - 100V利用時には2基/4基搭載時共に、電源1基の障害時にも残りの電源装置で連続稼動が可能
          - 200V利用時には2基搭載時共には電源1基、4基搭載時には電源2基の障害時にも残りの電源装置で連続稼動が可
      - 冷却用ブロワーは標準で4基（2基は故障時の予備）
      - スイッチ用スロット1,2には[ギガビットイーサネット](https://ja.wikipedia.org/wiki/ギガビットイーサネット "wikilink")用スイッチ、もしくはパススルーモジュールを実装可能
      - スイッチ用スロット3,4には各種スイッチ（ギガビットイーサネット、[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")、[SAS](../Page/SAS.md "wikilink")スイッチ）、もしくはパススルーモジュールを実装可能
      - シリアル・モジュール・ベイにはシリアルパススルーモジュールを実装可能
      - 最大12個の3.5inch HDD (SAS/SATA) を内蔵可能であり、SAS RAIDコントローラの機能でRAID0,1,0+1,5を構成可能
      - IBM BladeCenter Sの出荷開始当初はSAS RAIDコントローラ機能は組み込まれておらず、後日ファームウェアのアップデートで機能追加された。

## ブレードサーバ

### x86（インテル）ブレードサーバ

| 名称                    | 型番                 | プラットフォーム           | CPU                           | CPU Socket/Core             | Chipset                                                          | FSB                                                                | HDD                                                                                    | 管理(\*)        | 発売年                                                      | 営業活動                                                                  | リンク                                                                     |
| --------------------- | ------------------ | ------------------ | ----------------------------- | --------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------ | -------------------------------------------------------------------------------------- | ------------- | -------------------------------------------------------- | --------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| HS20                  |                    |                    |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 8678                  | x86(x32)           | Xeon DP(Prestonia) | 2/2                           | ServerWorks ServerSet GC-LE | 400Mhz                                                           | [ATA100](https://ja.wikipedia.org/wiki/AT_Attachment "wikilink")   | 4.0                                                                                    | 2002          | 終了                                                       | [1](http://www-06.ibm.com/systems/jp/x/pdf/bladecenter0307.pdf)       |                                                                         |
| 8832                  | x86(x32)           | Xeon DP(Prestonia) | 2/2                           | 533Mhz                      | [ATA100](https://ja.wikipedia.org/wiki/AT_Attachment "wikilink") | 4.11                                                               | 2003                                                                                   | 終了            | [2](http://www-06.ibm.com/systems/jp/x/pdf/hs200408.pdf) |                                                                       |                                                                         |
| Xeon DP(Nocona)       | 4.11               | 2003               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 8843                  | x86(x32/x64)       | Xeon DP(Nocona)    | 2/2                           | Intel E7520                 | 800Mhz                                                           | [SCSI U320](../Page/Small_Computer_System_Interface.md "wikilink") | 4.21                                                                                   | 2004          | 終了                                                       | [3](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_bladecenter.pdf) |                                                                         |
| x86(x32/x64)          | Xeon DP(Irwindale) | 4.21               | 2004                          | 終了                          |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 7981                  | x86(x32)           | Xeon DP(Sossaman)  | 2/2                           | |667Mhz                     | [SAS](../Page/SAS.md "wikilink")                                 | 5.10.2                                                             | 2006                                                                                   | 終了            |                                                          |                                                                       |                                                                         |
| HS40                  | 8839               | x86(x32)           | Xeon MP(Foster)               | 4/4                         | ServerWorks ServerSet GC-LE                                      | 400Mhz                                                             | [ATA100](https://ja.wikipedia.org/wiki/AT_Attachment "wikilink")                       | 4.20.2        | 2004                                                     | 終了                                                                    | [4](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_bladecenter67.pdf) |
| HS21                  | 8853               | x86(x32/x64)       | Xeon DP (Woodcrest)           | 2/4                         | Intel 5000P                                                      | 1066/1333Mhz                                                       | [SAS](../Page/SAS.md "wikilink")                                                       | 5.10.2        | 2006                                                     | 終了                                                                    | [5](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_hs21_8853.pdf)     |
| Xeon DP (Wolfdale-DP) | 2006               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| Xeon DP (Clovertown)  | 2/8                | 2007               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| Xeon DP (Harpertown)  | 2007               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HS21 XM               | 7995               | x86(x32/x64)       | Xeon DP (Woodcrest)           | 2/4                         | Intel 5000P                                                      | 1066/1333Mhz                                                       | [SAS](../Page/SAS.md "wikilink")                                                       | 5.20          | 2006                                                     | 終了                                                                    | [6](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_hs21xm_7995.pdf)   |
| Xeon DP (Wolfdale-DP) | 2006               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| Xeon DP(Clovertown)   | 2/8                | 2007               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| Xeon DP (Harpertown)  | 2007               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HS12                  | 8028               | x86(x32/x64)       | Core 2 Duo (Conroe-CL)        | 1/2                         | Intel 5100                                                       | 1066Mhz                                                            | [SAS](../Page/SAS.md "wikilink") [SATA](https://ja.wikipedia.org/wiki/SATA "wikilink") | 5.20.2/5.20.3 | 2008                                                     | 終了                                                                    | [7](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_hs12_8028.pdf)     |
| Xeon (Yorkfield-CL)   | 1/4                | 2008               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| Xeon (Conroe-CL)      | 1/2                | 2008               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| Xeon (Harpertown)     | 1/4                | 2008               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HS22                  | 7870               | x86(x32/x64)       | Xeon (Nehalem-EP/Westmere)    | 2/8                         | Intel 5520                                                       | 800/1066/1333Mhz (メモリ同期クロック）                                       | [SAS](../Page/SAS.md "wikilink") [SATA](https://ja.wikipedia.org/wiki/SATA "wikilink") | 6.1           | 2009                                                     | 終了                                                                    | [8](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_hs22_7870.pdf)     |
| 2/4                   | 6.1                | 2009               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/12                  | 6.1                | 2010               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HS22V                 | 7871               | x86(x32/x64)       | Xeon (Nehalem-EP/Westmere)    | 2/4                         | Intel 5520                                                       | 1066/1333Mhz (メモリ同期クロック）                                           | 1.8inch SSD                                                                            | 6.1           | 2010                                                     | 終了                                                                    | [9](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_hs22v_7871.pdf)    |
| 2/8                   | 2010               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/12                  | 2010               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HX5                   | 7872 (１ブレード構成）     | x86(x32/x64)       | Xeon (Nehalem-EX/Westmere-EX) | 2/8                         | Intel 7500                                                       | 978/1066Mhz (メモリ同期クロック）                                            | 1.8inch SSD                                                                            | 6.12/6.2      | 2010                                                     | 終了                                                                    | [10](http://www-06.ibm.com/systems/jp/x/system/pdf/sg_hx5_7872.pdf)     |
| 2/12                  | 2010               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/16                  | 2010               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/20                  | 2011               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 7872 (2ブレード構成）        | 4/16               | 2010               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 4/24                  | 2010               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 4/32                  | 2010               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 4/40                  | 2011               | 終了                 |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HS23                  |                    | x86(x32/x64)       | Xeon (Sandy Bridge-EP)        | 2/8                         | Intel C600                                                       | 1600Mhz (メモリ同期クロック）                                                | [SAS](../Page/SAS.md "wikilink") [SATA](https://ja.wikipedia.org/wiki/SATA "wikilink") |               | 2012                                                     | 終了                                                                    | [11](http://www.redbooks.ibm.com/abstracts/tips0843.html)               |
| 2/12                  |                    | 2012               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/16                  |                    | 2012               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HS23E                 |                    | x86(x32/x64)       | Xeon (Sandy Bridge-EP)        | 1/2                         | Intel C600                                                       | 1600Mhz (メモリ同期クロック）                                                | [SAS](../Page/SAS.md "wikilink") [SATA](https://ja.wikipedia.org/wiki/SATA "wikilink") |               | 2012                                                     | 終了                                                                    | [12](http://www.redbooks.ibm.com/abstracts/tips0887.html)               |
| 2/8                   |                    | 2012               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/12                  |                    | 2012               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/16                  |                    | 2012               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| HS23 V2               |                    | x86(x32/x64)       | Xeon (Ivy Bridge-EP)          | 2/8                         | Intel C600                                                       | 1600Mhz (メモリ同期クロック）                                                | [SAS](../Page/SAS.md "wikilink") [SATA](https://ja.wikipedia.org/wiki/SATA "wikilink") |               | 2013                                                     | 終了                                                                    | [13](http://www.redbooks.ibm.com/abstracts/tips0887.html)               |
| 2/12                  |                    | 2013               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/16                  |                    | 2013               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/20                  |                    | 2013               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
| 2/24                  |                    | 2013               | 終了                            |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |
|                       |                    |                    |                               |                             |                                                                  |                                                                    |                                                                                        |               |                                                          |                                                                       |                                                                         |

(\*)サポートするIBM管理ソフトウェア(IBM Systems Director)の最低バージョン（記述のバージョン以降をサポート）

#### HS12

[IBM_BLADECENTER_HS12_8028_JPN_JPY.jpg](https://ja.wikipedia.org/wiki/File:IBM_BLADECENTER_HS12_8028_JPN_JPY.jpg "fig:IBM_BLADECENTER_HS12_8028_JPN_JPY.jpg") 低価格・省電力ブレードサーバ　/旧機種

  - 仕様
      - サポートOS :Windows Server2003/2008,Linux,VMware
      - Quad-Core Xeon 1ソケット
      - 6 DIMM スロット（最大24 GB）
      - SAS/SATA 2.5inch Hotswap HDD（最大2個）
      - GbE 標準 2port
      - 拡張スロット 1slot（ファイバーチャネル、イーサネット、ミリネット、インフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot（10GbE,インフィニバンド(4X)などの拡張カード追加可能）

#### HS20

[IBM_BladeCenter_HS20_8678_JPN_JPY.jpg](https://ja.wikipedia.org/wiki/File:IBM_BladeCenter_HS20_8678_JPN_JPY.jpg "fig:IBM_BladeCenter_HS20_8678_JPN_JPY.jpg") 最初にリリースされたブレードサーバ /旧機種

  - 仕様
      - サポートOS :Windows Server2000/2003,Linux,VMware
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):4.0以降
      - Single もしくは Dual-Core Xeon 2ソケット
      - 4 DIMM スロット
      - ATA100/SAS 2.5inch HDD（最大2個）
      - GbE 標準 2port
      - 拡張スロット 標準1slot（ファイバーチャネル、イーサネット、ミリネット、インフィニバンドなどの拡張カード追加可能）

<File:IBM> BladeCenter HS20 8678 JPN JPY.jpg|HS20(8678)写真 <File:IBM> BLADECENTER HS20 7981 JPN JPY.jpg|HS20(7981)写真 <File:IBM> BLADECENTER HS20 8832 JPN JPY.jpg|HS20(8832)写真 <File:IBM> BLADECENTER HS20 8843 JPN JPY.jpg|HS20(8843)写真

#### HS21

[IBM_BladeCenter_HS21_8853_JPN_JPY.jpg](https://ja.wikipedia.org/wiki/File:IBM_BladeCenter_HS21_8853_JPN_JPY.jpg "fig:IBM_BladeCenter_HS21_8853_JPN_JPY.jpg") HS20の後継機　High-Speed I/Oへの対応などが強化された　/旧機種

  - 仕様
      - サポートOS :Windows Server2003/2008,Linux,VMware,Solaris
      - Dual-Core　もしくは Quad-Core Xeon 2ソケット
      - 4 DIMM スロット
      - SAS 2.5inch HDD（最大2個）
      - GbE 標準 2port
      - 拡張スロット 1slot（ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### HS21 XM

[IBM_BLADECENTER_HS21XM_7995_JPN_JPY.jpg](https://ja.wikipedia.org/wiki/File:IBM_BLADECENTER_HS21XM_7995_JPN_JPY.jpg "fig:IBM_BLADECENTER_HS21XM_7995_JPN_JPY.jpg") HS20の後継機　High-Speed I/Oへの対応などが強化された点などはHS21と同等だが、メモリ拡張機能をさらに強化したブレードサーバ /旧機種

  - 仕様
      - サポートOS :Windows Server2003/2008,Linux,VMware,Solaris
      - Dual-Core　もしくは Quad-Core Xeon 2ソケット
      - 8 DIMM スロット
      - SAS 2.5inch HDD（最大1個）もしくは 2.5inch SSD（最大2個）
      - GbE 標準 2port
      - 拡張スロット 1slot（ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot（10GbE,イニフィニバンド (4X) などの拡張カード追加可能）

#### HS22

[IBM_BLADECENTER_HS22_7870_JPN_JPY.jpg](https://ja.wikipedia.org/wiki/File:IBM_BLADECENTER_HS22_7870_JPN_JPY.jpg "fig:IBM_BLADECENTER_HS22_7870_JPN_JPY.jpg") HS21,HS21 XMの後継機　新CPU(Nehalem)対応 /旧機種

  - 仕様
      - サポートOS :Windows Server2003/2008,Linux,VMware,Solaris
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):6.1以降
      - Xeon 5500/5600 2ソケット
      - 12 DIMM スロット
      - SAS/SATA 2.5inch ホットスワップHDDもしくは 2.5inch SSD(最大2個）
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、SASなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）
      - VMware ESXi用 USBスロット 1ソケット

#### HS22V

[HS22v.JPG](https://ja.wikipedia.org/wiki/File:HS22v.JPG "fig:HS22v.JPG") HS22のメモリ搭載容量拡張モデル /旧機種

  - 仕様
      - サポートOS :Windows Server2003/2008,Linux,VMware,Solaris
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):6.1以降
      - Xeon 5500/5600 2ソケット
      - 18 DIMM スロット
      - 1.8inch SSD(最大2個）
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、SASなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）
      - VMware ESXi用 USBスロット 1ソケット

#### HS40

[IBM_BLADECENTER_HS40_8839_1_JPN_JPY.jpg](https://ja.wikipedia.org/wiki/File:IBM_BLADECENTER_HS40_8839_1_JPN_JPY.jpg "fig:IBM_BLADECENTER_HS40_8839_1_JPN_JPY.jpg") HS20の拡張版としての4ソケットサーバ /旧機種

  - 仕様
      - サポートOS :Windows Server2000/2003,Linux,VMware
      - 1台あたり2ブレードスロットが必要（通常ブレードの2倍の厚さ）
      - Xeon MP 4ソケット
      - 4 DIMM スロット
      - ATA100/SAS 2.5inch HDD (最大2個)
      - GbE 標準 4port
      - 拡張スロット 標準2slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）

<File:IBM> BLADECENTER HS40 8839 1 JPN JPY.jpg|HS40(8839)1段目写真 <File:IBM> BLADECENTER HS40 8839 2 JPN JPY.jpg|HS40(8839)2段目写真

#### HX5 (1ブレード構成)

[HX5.JPG](https://ja.wikipedia.org/wiki/File:HX5.JPG "fig:HX5.JPG") EX5アーキテクチャー採用 2ソケットモデル HX5は、１台で利用する場合は２ソケットサーバ、２台を連結すれば４ソケットサーバになるという特徴を有しており、スケールアップとスケールアウトの両方に対応可能である。 /旧機種

  - 仕様
      - サポートOS :Windows Server2003/2008,Linux,VMware
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):6.12以降
      - Xeon 7500 2ソケット
      - 16 DIMM スロット
      - 1.8inch SSD(最大2個）
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、SASなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### HX5 (2ブレード構成)

EX5アーキテクチャー採用 4ソケットモデル /旧機種

  - 仕様
      - サポートOS :Windows Server2003/2008,Linux,VMware
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):6.12以降
      - Xeon 7500 4ソケット
      - 32スロット
      - 1.8inch SSD(最大4個）
      - GbE 標準 4port
      - CIOv拡張スロット 2slot (ファイバーチャネル、イーサネット、SASなどの拡張カード追加可能）
      - CFFh高速拡張スロット 2slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### HS23

HS22の後継機　新CPU(Sandy Bridge-EP)対応 /旧機種

  - 仕様
      - サポートOS :
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):
      - Xeon E5-2600 2ソケット
      - 16 DIMM スロット
      - SAS/SATA 2.5inch ホットスワップHDDもしくは 2.5inch SSD(最大2個）
      - GbE 標準 2port
      - CIOv拡張スロット
      - CFFh高速拡張スロット
      - VMware ESXi用 USBスロット

#### HS23E

HS22の後継機　新CPU(Sandy Bridge-EP)対応 /旧機種

  - 仕様
      - サポートOS :
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):
      - Xeon E5-2400 2ソケット, Pentium 140X
      - 12 DIMM スロット
      - SAS/SATA 2.5inch ホットスワップHDDもしくは 2.5inch SSD(最大2個）
      - GbE 標準 2port
      - CIOv拡張スロット
      - CFFh高速拡張スロット
      - VMware ESXi用 USBスロット

#### HS23 V2

HS23の後継機　新CPU(Ivy Bridge-EP)対応 /旧機種

  - 仕様
      - サポートOS :
      - サポート[IBM Systems Director](https://ja.wikipedia.org/wiki/IBM_Systems_Director "wikilink"):
      - Xeon E5-2600 V2 2ソケット
      - 16 DIMM スロット
      - SAS/SATA 2.5inch ホットスワップHDDもしくは 2.5inch SSD(最大2個）
      - GbE 標準 2port
      - CIOv拡張スロット
      - CFFh高速拡張スロット
      - VMware ESXi用 USBスロット

### x86(AMD) ブレードサーバ

| 名称                | 型番   | プラットフォーム       | CPU                 | CPU Socket/Core | Chipset                   | Hyper Transport | HDD                                                                | 管理S/W       | 発売年  | 営業活動 |
| ----------------- | ---- | -------------- | ------------------- | --------------- | ------------------------- | --------------- | ------------------------------------------------------------------ | ----------- | ---- | ---- |
|                   |      |                |                     |                 |                           |                 |                                                                    |             |      |      |
| LS20              | 8850 | x86(x32/AMD64) | Opteron(Italy)      | 2/2             | AMD 8131&8111             | 1Ghz            | [SCSI U320](../Page/Small_Computer_System_Interface.md "wikilink") | 4.22        | 2005 | 終了   |
| 2/4               | 終了   |                |                     |                 |                           |                 |                                                                    |             |      |      |
| LS21              | 7971 | x86(x32/AMD64) | Opteron(Santa Rosa) | 2/4             | ServerWorks HT2000/HT1000 | 1Ghz            | [SAS](../Page/SAS.md "wikilink")                                   | 5.20        | 2006 | 終了   |
| LS41              | 7972 | x86(x32/AMD64) | Opteron(Santa Rosa) | 2/4             | ServerWorks HT2000/HT1000 | 1Ghz            | [SAS](../Page/SAS.md "wikilink")                                   | 5.20        | 2006 | 終了   |
| 4/8               | 2006 | 終了             |                     |                 |                           |                 |                                                                    |             |      |      |
| LS22              | 7901 | x86(x32/AMD64) | Opteron(Barcelona)  | 2/8             | ServerWorks HT2100/HT1000 | 1Ghz            | [SAS](../Page/SAS.md "wikilink")                                   | 5.20.2/6.10 | 2008 | 終了   |
| Opteron(Istanbul) | 2/12 | 2009           | 終了                  |                 |                           |                 |                                                                    |             |      |      |
| LS42              | 7902 | x86(x32/AMD64) | Opteron(Barcelona)  | 4/16            | ServerWorks HT2100/HT1000 | 1Ghz            | [SAS](../Page/SAS.md "wikilink")                                   | 5.20.2/6.10 | 2008 | 終了   |
| Opteron(Istanbul) | 4/24 | 2009           | 終了                  |                 |                           |                 |                                                                    |             |      |      |

#### LS20

[LS20_8850.jpg](https://ja.wikipedia.org/wiki/File:LS20_8850.jpg "fig:LS20_8850.jpg") 最初にリリースされたx86(AMD)ブレードサーバ

  - 主な特徴
      - Single もしくは Dual-Core AMD Opteron CPU 2ソケット
      - 4 DIMM スロット
      - SCSI U320 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - 拡張スロット 標準1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）

#### LS21

[LS21_7971.jpg](https://ja.wikipedia.org/wiki/File:LS21_7971.jpg "fig:LS21_7971.jpg") LS20の後継機　High-Speed I/Oへの対応などが強化された

  - 主な特徴
      - Dual-Core AMD Opteron CPU 2ソケット
      - 8 DIMM スロット
      - SAS 2.5inch HDD (最大1個)
      - GbE 標準 2port
      - 拡張スロット 標準1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### LS22

LS21の後継機　新型CPU(Quad-Core/Hex-Core)への対応などが強化されたブレードサーバ

  - 主な特徴
      - Quad-Core/Hex-Core AMD Opteron CPU 2ソケット
      - 8 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - 拡張スロット 標準1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### LS41

LS21をCPU4ソケットまで拡張可能に強化されたブレードサーバ

  - 主な特徴
      - 1台あたり2ブレードスロットが必要（通常ブレードの2倍の厚さ）
      - Dual-core AMD Opteron CPU 4ソケット
      - 16 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 4port
      - 拡張スロット 標準2slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### LS42

[LS42_7902.jpg](https://ja.wikipedia.org/wiki/File:LS42_7902.jpg "fig:LS42_7902.jpg") LS41の後継機　新型CPU(Quad-Core/Hex-Core)への対応などが強化された

  - 主な特徴
      - 1台あたり2ブレードスロットが必要（通常ブレードの2倍の厚さ）
      - Dual-core AMD Opteron CPU 4ソケット
      - 16 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 4port
      - 拡張スロット 標準2slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

### POWERブレードサーバ

| 名称                | 型番                | プラットフォーム     | CPU               | CPU Socket/Core | Chipset                                                                                                                                                                         | Hyper Transport                  | HDD                                                              | FC Port (最大) | NIC Port (最大) | 発売年  | 営業活動 |
| ----------------- | ----------------- | ------------ | ----------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | ---------------------------------------------------------------- | ------------ | ------------- | ---- | ---- |
|                   |                   |              |                   |                 |                                                                                                                                                                                 |                                  |                                                                  |              |               |      |      |
| JS20              | 8842              | POWER(PPC64) | PowerPC(PPC970)   | 2/2             | AMD 8131&8111                                                                                                                                                                   | 800MHz                           | [ATA100](https://ja.wikipedia.org/wiki/AT_Attachment "wikilink") | 4            | 4             | 2004 | 終了   |
| PowerPC(PPC970FX) | 1.1GHz            |              |                   |                 |                                                                                                                                                                                 |                                  |                                                                  |              |               |      |      |
| JS21              | 7988              | POWER(PPC64) | PowerPC(PPC970FX) | 2/2             | [CPC945](https://ja.wikipedia.org/wiki/PowerPC_970#.E3.82.B7.E3.82.B9.E3.83.86.E3.83.A0.E3.82.B3.E3.83.B3.E3.83.88.E3.83.AD.E3.83.BC.E3.83.A9 "wikilink") & BCM 5780 & AMD 8111 | 1.35GHz                          | [SAS](../Page/SAS.md "wikilink")                                 | 4            | 6             | 2006 | 終了   |
| 8844              | PowerPC(PPC970MP) | 2/2          | 1.35GHz           |                 |                                                                                                                                                                                 |                                  |                                                                  |              |               |      |      |
| PowerPC(PPC970MP) | 2/4               | 1.25GHz      |                   |                 |                                                                                                                                                                                 |                                  |                                                                  |              |               |      |      |
| JS22              | 7998              | POWER(64)    | POWER6            | 2/4             |                                                                                                                                                                                 |                                  | [SAS](../Page/SAS.md "wikilink")                                 | 4            | 6             | 2007 | 終了   |
| JS12              | POWER(64)         | POWER6+      | 1/2               |                 |                                                                                                                                                                                 | [SAS](../Page/SAS.md "wikilink") | 4                                                                | 6            | 2007          | 終了   |      |
| JS23              | 7778              | POWER(64)    | POWER6+           | 2/4             |                                                                                                                                                                                 |                                  | [SAS](../Page/SAS.md "wikilink")                                 | 4            | 6             | 2009 | 終了   |
| JS43              | POWER(64)         | POWER6+      | 4/8               |                 |                                                                                                                                                                                 | [SAS](../Page/SAS.md "wikilink") | 8                                                                | 12           | 2009          | 終了   |      |
| PS700 Express     | 8402              | POWER(64)    | POWER7            | 1/4             |                                                                                                                                                                                 |                                  | [SAS](../Page/SAS.md "wikilink")                                 | 4            | 6             | 2010 | 終了   |
| PS701 Express     | POWER(64)         | POWER7       | 2/8               |                 |                                                                                                                                                                                 | [SAS](../Page/SAS.md "wikilink") | 4                                                                | 6            | 2010          | 終了   |      |
| PS702 Express     | POWER(64)         | POWER7       | 4/16              |                 |                                                                                                                                                                                 | [SAS](../Page/SAS.md "wikilink") | 8                                                                | 12           | 2010          | 終了   |      |
| PS703 Express     | 7891              | POWER(64)    | POWER7            | 2/16            |                                                                                                                                                                                 |                                  | [SAS](../Page/SAS.md "wikilink")                                 | 4            | 6             | 2011 | 終了   |
| PS704 Express     | POWER(64)         | POWER7       | 4/32              |                 |                                                                                                                                                                                 | [SAS](../Page/SAS.md "wikilink") | 8                                                                | 12           | 2011          | 終了   |      |
|                   |                   |              |                   |                 |                                                                                                                                                                                 |                                  |                                                                  |              |               |      |      |

#### JS12 Express

JS22の1ソケット版

  - 主な特徴
      - サポートOS:Linux/AIX/iOS
      - DLPAR(Dynamic Logical Partitioning)/Integrated Virtualization Manager(IVM) サポート
      - POWER6+(Dual-Core) 1ソケット
      - 8 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - 拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### JS20

最初にリリースされたPowerブレードサーバ

  - 主な特徴
      - サポートOS:Linux/AIX
      - PowerPC 970 2ソケット
      - 4 DIMM スロット
      - ATA100 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - 拡張スロット 標準1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）

#### JS21

[JS21_7988.jpg](https://ja.wikipedia.org/wiki/File:JS21_7988.jpg "fig:JS21_7988.jpg") JS20の後継機　High-Speed I/Oへの対応などが強化された

  - 主な特徴
      - サポートOS:Linux/AIX
      - DLPAR(Dynamic Logical Partitioning)サポート
      - PowerPC 970FX(Single-Core)/970MP(Dual-Core) 2ソケット
      - 4 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### JS22

[JS22_7998.jpg](https://ja.wikipedia.org/wiki/File:JS22_7998.jpg "fig:JS22_7998.jpg") JS21の後継機 新CPU(POWER6)のサポート及び、i/OSサポートが追加された

  - 主な特徴
      - サポートOS:Linux/AIX/iOS
      - DLPAR(Dynamic Logical Partitioning)/Integrated Virtualization Manager(IVM) サポート
      - POWER6(Dual-Core) 2ソケット
      - 4 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### JS23 Express

JS22の後継機 新CPU(POWER6+)のサポート

  - 主な特徴
      - サポートOS:Linux/AIX/iOS
      - DLPAR(Dynamic Logical Partitioning)/Integrated Virtualization Manager(IVM) サポート
      - POWER6+(Dual-Core) 2ソケット
      - 4 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### JS43 Express

JS23の4ソケット(8コア）版

  - 主な特徴
      - 1台あたり2ブレードスロットが必要（通常ブレードの2倍の厚さ）
      - サポートOS:Linux/AIX/iOS
      - DLPAR(Dynamic Logical Partitioning)/Integrated Virtualization Manager(IVM) サポート
      - POWER6+(Dual-Core) 4ソケット
      - 8 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### PS700 Express

JS23の後継機 新CPU(POWER7)のサポート

  - 主な特徴
      - サポートOS:Linux/AIX/iOS
      - DLPAR(Dynamic Logical Partitioning)/Integrated Virtualization Manager(IVM) サポート
      - POWER7(Quad-Core) 1ソケット
      - 8 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### PS701 Express

JS23の後継機 新CPU(POWER7)のサポート

  - 主な特徴
      - サポートOS:Linux/AIX/iOS
      - DLPAR(Dynamic Logical Partitioning)/Integrated Virtualization Manager(IVM) サポート
      - POWER7(Quad-Core) 2ソケット
      - 16 DIMM スロット
      - SAS 2.5inch HDD (最大1個)
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### PS702 Express

JS43の後継機 新CPU(POWER7)のサポート

  - 主な特徴
      - 1台あたり2ブレードスロットが必要（通常ブレードの2倍の厚さ）
      - サポートOS:Linux/AIX/iOS
      - DLPAR(Dynamic Logical Partitioning)/Integrated Virtualization Manager(IVM) サポート
      - POWER7(Quad-Core) 4ソケット
      - 16 DIMM スロット
      - SAS 2.5inch HDD (最大2個)
      - GbE 標準 2port
      - CIOv拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、イニフィニバンドなどの拡張カード追加可能）
      - CFFh高速拡張スロット 1slot (10GbE,イニフィニバンド(4X)などの拡張カード追加可能）

#### PS703 Express

JS23の後継機 新POWER7(オクトコア）のサポート

  - 主な特徴
      - サポートOS:Linux/AIX/iOS

#### PS704 Express

JS43の後継機 新POWER7(オクトコア）のサポート

  - 主な特徴
      - 1台あたり2ブレードスロットが必要（通常ブレードの2倍の厚さ）
      - サポートOS:Linux/AIX/iOS

### Cellブレードサーバ

| 名称   | 型番 | プラットフォーム | CPU               | CPU Socket/Core | Chipset | Hyper Transport | HDD                                                              | 発売年  | 営業活動 |
| ---- | -- | -------- | ----------------- | --------------- | ------- | --------------- | ---------------------------------------------------------------- | ---- | ---- |
|      |    |          |                   |                 |         |                 |                                                                  |      |      |
| QS20 |    | Cell(64) | Cell B.E.         | 2/2PPE,16SPE    |         |                 | [ATA100](https://ja.wikipedia.org/wiki/AT_Attachment "wikilink") | 2006 | 終了   |
| QS21 |    | Cell(64) | Cell B.E.         | 2/2PPE,16SPE    |         |                 | N/A                                                              | 2007 | 終了   |
| QS22 |    | Cell(64) | IBM PowerXCell 8i | 2/2PPE,16SPE    |         |                 | 専用SSD                                                            | 2008 | 終了   |
|      |    |          |                   |                 |         |                 |                                                                  |      |      |

#### QS20

最初のCellブレードサーバ

  - 主な特徴
      - 1台あたり2ブレードスロットが必要（通常ブレードの2倍の厚さ）
      - サポートOS:Linux
      - Cell B.E 2ソケット
      - 4 DIMM スロット
      - ATA100 2.5inch HDD (最大1個)
      - GbE 標準 2port
      - インフィニバンド(4X)追加可能

#### QS21

QS20の後継機　High-Speed I/Oへの対応などが強化された

  - 主な特徴
      - サポートOS:Linux
      - Cell B.E 2ソケット
      - 4 DIMM スロット
      - 内蔵ストレージなし
      - GbE 標準 2port
      - 拡張スロット 1slot (SASなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (インフィニバンド(4X)などの拡張カード追加可能）

#### QS22

QS21の後継機　新CPU(PowerXCell 8i)への対応などが強化された

  - 主な特徴
      - サポートOS:Linux
      - PowerXCell 8i 2ソケット
      - 8 DIMM スロット
      - 8GB uFDM Flash Drive 1個
      - GbE 標準 2port
      - 拡張スロット 1slot (SASなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (インフィニバンド(4X)などの拡張カード追加可能）

### ブレード・ワークステーション

| 名称                     | 型番   | プラットフォーム     | CPU                 | CPU Socket/Core | Chipset            | Hyper Transport | HDD                                                   | 発売年  | 営業活動 |
| ---------------------- | ---- | ------------ | ------------------- | --------------- | ------------------ | --------------- | ----------------------------------------------------- | ---- | ---- |
|                        |      |              |                     |                 |                    |                 |                                                       |      |      |
| HC10                   | 7996 | x86(x32/x64) | Core 2 Duo (Conroe) | 1/2             | Intel Q965 Express | 1066Mhz         | [SATA](https://ja.wikipedia.org/wiki/SATA "wikilink") | 2007 | 終了   |
| Core 2 Duo (Allendale) | 2007 | 終了           |                     |                 |                    |                 |                                                       |      |      |
|                        |      |              |                     |                 |                    |                 |                                                       |      |      |

#### HC10

ブレード型ワークステーション。 今日のVMwareが標準採用しているPCoIPプロトコルを、世界で初めて採用した製品であり、PCoIPプロトコルをハードウェア処理できるコントローラー(IGTA)を搭載している。これはTeradici社のTera1200シリーズ登載により実現されている。 ユーザーは遠隔地でIBM CP20ポータルを用い、HC10上で実行されている CAD/CAM/CAEの画面をあたかも手元にワークステーションがあるかの如く快適に利用できる。 尚、ネットワーク上を流れるデータは暗号化されており、Dassault CATIA/Solid Works, UGS NX, PTC Wildfire など主要CADの認証を取得している。2009年に営業活動終了。

  - 主な特徴
      - サポートOS:Windows XP,Windows Vista
      - Core 2 Duo 1ソケット
      - 4 DIMM スロット
      - 2.5inch SATA HDD (最大1個）
      - GbE 標準 1port
      - NVIDIA Quadro 1600M 3Dグラフィックス・アダプター
      - NVIDIA Quadro 120M 2Dグラフィックス・アダプター
      - I/O&グラフィックス送信アダプター標準(IGTA)

### ディープ・パケット・インスペクション専用ブレードサーバ

| 名称   | 型番   | プラットフォーム | CPU                             | CPU Socket/Core | Chipset | FSB | HDD   | 発売年 | 営業活動 |
| ---- | ---- | -------- | ------------------------------- | --------------- | ------- | --- | ----- | --- | ---- |
|      |      |          |                                 |                 |         |     |       |     |      |
| PN41 | 3020 |          | Intel IXP2805 network processor |                 |         |     | |2008 | 終了  |      |
|      |      |          |                                 |                 |         |     |       |     |      |

#### PN41

米国CloudShield Technologies社の[DPIアプリケーション専用ブレードサーバ](https://ja.wikipedia.org/wiki/ディープ・パケット・インスペクション "wikilink")

  - 主な特徴
      - Intel IXP2805 network processor
      - GbE 標準 2port　/10GbE 標準 4port /10GbE+1GbE(前面）標準 各1Port

### SPARCブレードサーバ

| 名称   | 型番 | プラットフォーム  | CPU           | CPU Socket/Core | Chipset   | FSB | HDD | 発売年   | 営業活動 |
| ---- | -- | --------- | ------------- | --------------- | --------- | --- | --- | ----- | ---- |
| T2BC |    | SPARC(64) | UltraSPARC T2 | 1/8             | |SATA/SAS |     |     | |2008 | 終了   |
|      |    |           |               |                 |           |     |     |       |      |

#### T2BC

Themis Computer社からリリースされた最初のSPARCブレードサーバ

  - 主な特徴
      - サポートOS:Solaris
      - Ultra SPARC T2 1ソケット
      - 8 DIMM スロット
      - SAS/SATA 2.5inch HDD (最大1個)
      - GbE 標準 2port
      - 拡張スロット 1slot (ファイバーチャネル、イーサネット、ミリネット、インフィニバンドなどの拡張カード追加可能）
      - 高速拡張スロット 1slot (10GbE,インフィニバンド(4X)などの拡張カード追加可能）

### zEnterprise BladeCenter Extension（zBX）

IBM System z と高速ネットワークで連結され、zEnterprise Unified Resource Manager（zManager）による統合管理下におかれるブレードサーバである。ハードウェアとしてはIBM BladeCenter PS701 ExpressおよびIBM BladeCenter HX5と同等である。HX5にはKVMをベースとしたハイパーバイザーが組み込まれており、WindowsやLinuxなどの汎用OSを利用可能である。x86事業のLenovo社への移管後もIBMから販売が継続されていたが、2014年12月に営業活動終了。

## スイッチモジュール

### Layer2 GbEスイッチ

#### 4-port GbEスイッチ・モジュール(13N0568)

[D-Link](https://ja.wikipedia.org/wiki/D-Link "wikilink") Layer 2 スイッチング/フィルタリング

  - （内部/外部）10/100/1000Base-T
  - 営業活動終了

#### BladeCenter Cisco Intelligent Gigabit Ethernet Switch Module(13N2281)

[Cisco](https://ja.wikipedia.org/wiki/Cisco "wikilink") Catalyst 29XX Layer 2 スイッチング/フィルタリング

  - （内部/外部）10/100/1000Base-T
  - 営業活動終了

#### Server Connectivity Module (39Y9324)

簡易版[BNT](https://ja.wikipedia.org/wiki/:en:BLADE_Network_Technologies "wikilink") Layer 2 スイッチング/フィルタリング

  - （内部/外部）10/100/1000Base-T

<File:IBM> BLADECENTER JPN JPY CIGESM.jpg|BladeCenter Cisco Intelligent Gigabit Ethernet Switch Module <File:IBM> BLADECENTER JPN JPY D-link.jpg|4-port GbEスイッチ・モジュール

### Layer2/3 GbEスイッチ

#### BNT Layer 2-3 カッパーGbEスイッチ・モジュール(32R1860)

[Nortel](../Page/ノーテルネットワークス.md "wikilink") Networks Layer 2-3 カッパーGbEスイッチ・モジュールから名称変更

BNT Layer 2/3 スイッチング/フィルタリング

  - （内部/外部）10/100/1000Base-T

#### BNT Layer 2-3 ファイバーGbEスイッチăモジュール(32R1861)

[BNT](https://ja.wikipedia.org/wiki/:en:BLADE_Network_Technologies "wikilink") Layer 2/3 スイッチング/フィルタリング

  - （内部/外部）10/100/1000Base-SX

#### Cisco Catalyst スイッチモジュール 3110X(41Y8522)

[Cisco](https://ja.wikipedia.org/wiki/Cisco "wikilink") Catalyst Layer 2/3 スイッチング/フィルタリング

  - （内部）10/100/1000Base-T
  - （外部）10GB-SR 1Port
  - Virtual Blade Switch機能

#### Cisco Catalyst スイッチモジュール 3110G(41Y8523)

[Cisco](https://ja.wikipedia.org/wiki/Cisco "wikilink") Catalyst Layer 2/3 スイッチング/フィルタリング

  - （内部/外部）10/100/1000Base-T
  - Virtual Blade Switch機能

#### Cisco Catalyst スイッチモジュール 3012(43W4395)

[Cisco](https://ja.wikipedia.org/wiki/Cisco "wikilink") Catalyst Layer 2/3 スイッチング/フィルタリング

  - （内部/外部）10/100/1000Base-T

#### Nortel 10Gb Uplink イーサースイッチ･モジュール（32R1783）

BNT Layer 2/3 スイッチング/フィルタリング

  - （内部）1000Base-SX
  - （外部）10Gb CX4 2Port、10Gb XFP Port(SR or LR)、1Gb RJ-45 1Port
  - 営業活動終了

#### BNT 1/10 Gb Uplink イーサネットスイッチモジュール(43W4395)

[BNT](https://ja.wikipedia.org/wiki/:en:BLADE_Network_Technologies "wikilink") Layer 2/3 スイッチング/フィルタリング

  - （内部）1000Base-SX
  - （外部）10GB-SR 3Port,10/100 1000Base-T 6port

### Layer2/3 10GbEスイッチ

#### BNT 10ポート 10Gb イーサネットスイッチモジュール(46C7191)

[BNT](https://ja.wikipedia.org/wiki/:en:BLADE_Network_Technologies "wikilink") Layer 2/3 スイッチング/フィルタリング

  - （内部/外部）10BASE-SR
  - CEEサポート・FCoEE対応

#### Cisco Nexus 4001I スイッチモジュール(46M6071)

Cisco Layer 2/3 スイッチング/フィルタリング

  - （内部/外部）10BASE-SR
  - FCoEサポート

#### Nortel 10Gb イーサーネット･スイッチ･モジュール(39Y9267)

BNT Layer 2/3 スイッチング/フィルタリング

  - （内部）10000Base-SX
  - （外部）10Gb XFP 6Port、1Gb RJ-45 1Port（管理用）
  - 営業活動終了

### 負荷分散スイッチ

#### BNT Layer 2-7 GbE スイッチ・モジュール(32R1859)

[Nortel](../Page/ノーテルネットワークス.md "wikilink") Networks Layer 2-7 GbE スイッチ・モジュールから名称変更 [BNT](https://ja.wikipedia.org/wiki/:en:BLADE_Network_Technologies "wikilink") Layer 2-7 スイッチング

  - （内部/外部）10/100/1000Base-T L2-7スイッチ

### SASスイッチ

#### SAS 接続モジュール(39Y9195)

ブレードと外部のSASストレージを接続するためのスイッチ

#### IBM BladeCenter S SAS RAIDコントローラー(43W3584)

BladeCenter S 専用　RAIDコントローラ付きスイッチ

### 2Gb SANスイッチ

#### 2ポートファイバーチャネル・スイッチモジュール (FCSM) (48P7062)

Qlogic 16port(内部14/外部2) 2Gb FC Switch

  - 営業活動終了

#### 6ポートファイバーチャネル・スイッチモジュール (FCSM) (26K6477)

Qlogic 20port(内部14/外部6) 2Gb FC Switch

  - 営業活動終了

#### Brocade Entry SAN スイッチモジュール (26K5601)

Brocade 16port(内部14/外部2) 2Gb FC Switch

  - カスケード上限 2
  - 営業活動終了

#### Brocade Enterprise SAN スイッチモジュール (90P0165)

Brocade 16port(内部14/外部2) 2Gb FC Switch

  - カスケード上限 239
  - 営業活動終了

### 4Gb SANスイッチ

#### Brocade 10/20ポート 4Gb スイッチモジュール(32R1812/32R1813)

#### QLogic 10/20ポート 4Gb SAN スイッチ モジュール(43W6724/43W6725)

#### Cisco 4Gb 10/20ポート ファイバーチャネルăスイッチăモジュール(39Y9284/39Y9280)

### 8Gb SANスイッチ

#### Qlogic 20ポート 8Gb SANスイッチモジュール(44X1905)

#### Brocade 10/20ポート 8Gb SANスイッチモジュール(44X1921/44X1920)

#### Qlogic バーチャルファブリック拡張モジュール（46M6172）

BNT 10ポート 10Gb イーサネットスイッチモジュール(46C7191) と組み合わせ、Qlogic コンバージドネットワークアダプタ（CNA)から8Gb ファイバーチャネル接続を可能にするゲートウェイモジュール

### インフィニバンドスイッチ

#### InfiniBandスイッチ・モジュール

  - Topspin Infiniband スイッチ・モジュール
  - 営業活動終了

#### Voltaire 40Gb InfiniBand スイッチ・モジュール(46M6005)

  - Voltaire Infiniband スイッチ・モジュール

### パススルーモジュール

#### オプティカル・パススルー・モジュール (39Y9316)

各ブレードサーバから光ファイバー接続（GbE(1000Base-SX) または 2Gb FC SAN）をスイッチを介さずに外部と接続する (4Gb,8Gb FC SAN接続は不可）

#### カッパー・パススルー・モジュール (39Y9316)

各ブレードサーバからGbE(1000Base-T) をスイッチを介さずに外部と接続する(10/100Base-T接続は不可)

#### インテリジェントカッパーパススルーモジュール(44W4483)

各ブレードサーバからGbEインターフェースをスイッチを介さずに外部と接続する (100Base-Tもしくは1000Base-T)

#### Qlogic 8Gb インテリジェント・パススルー・モジュール(44X1907)

各ブレードサーバから光ファイバー接続（8Gb FC SAN）をスイッチを介さずに外部と接続する 接続先スイッチは[NPIV機能を有する必要がある](https://ja.wikipedia.org/wiki/:en:NPIV "wikilink")

#### Qlogic 4Gb インテリジェント・パススルー・モジュール(43W6723)

各ブレードサーバから光ファイバー接続（4Gb FC SAN）をスイッチを介さずに外部と接続する　接続先スイッチはNPIV機能を有する必要がある

#### 10Gb イーサネットパススルーモジュール for IBM BladeCenter (46M6181)

各ブレードサーバから光ファイバー接続（10GB-SR/LR), または10GBASE-Tをスイッチを介さずに外部と接続する

### Converged スイッチ･モジュール

#### Brocade コンバージド 10GbE スイッチモジュール(69Y1909))

  - （内部）（1Gbps/10Gbps)
  - （外部）10G Converged Enhanced Ethernet(CEE) 8port、FCポート(2G/4G/8Gbps)8port
  - 出荷時16ポート利用可。全30ポートを利用時は、Brocade コンバージド 10GbE スイッチ 14ポート アップグレードを追加

## BladeCenter関連 Systems Software

### BOFM (BladeCenter Open Fabric Manager)

ブレードサーバーの MAC アドレスや WWN などを仮想化することで、接続に関する管理を容易化する機能。オプション機能となる。

#### BOFM Basic

ブレードサーバーの MAC アドレスや WWN などを仮想化し、同一ブレードベイに装着するブレード間で引き継ぐことができる

#### BOFM Advance

ブレードサーバーの MAC アドレスや WWN などを仮想化し、物理的なブレードサーバ故障時に他のブレードベイに装着された ブレードにMAC アドレスや WWN などを引き継ぐことが可能である。なおv3.0まではSystems Directorからの設定/操作が必要だったが、v4.0からは専用ソフトウェア単体で実現する仕様に変更された。

## 外部リンク

  - [IBM・BladeCenter](http://www-06.ibm.com/systems/jp/bladecenter/)
  - [IBMプレスリリース・Solaris 10 サポート開始](http://www-06.ibm.com/jp/press/20060712002.html)
  - [会社引っ越し ブレードで仮想化大作戦](http://ascii.jp/elem/000/000/169/169566/)

[Category:IBMのコンピュータ](https://ja.wikipedia.org/wiki/Category:IBMのコンピュータ "wikilink") [Category:サーバ_(ハードウェア)](https://ja.wikipedia.org/wiki/Category:サーバ_\(ハードウェア\) "wikilink") [Category:Cell_BEアーキテクチャ](https://ja.wikipedia.org/wiki/Category:Cell_BEアーキテクチャ "wikilink")