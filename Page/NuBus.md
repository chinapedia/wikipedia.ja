> この記事は[NuBus](https://ja.wikipedia.org/wiki/NuBus)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:Macintosh_II_motherboard.jpg "wikilink") IIのマザーボード。左に6個のNuBusスロットが見える。\]\] [right](https://ja.wikipedia.org/wiki/ファイル:Nubus_graphics_card.jpg "wikilink")

**NuBus**（ニューバス）は[32ビット](../Page/32ビット.md "wikilink")の[パラレルバスである](../Page/バス_\(コンピュータ\).md "wikilink")。当初は[MITでNuMachineワークステーションの一部として開発されたが](../Page/マサチューセッツ工科大学.md "wikilink")、ついには、[アップルコンピュータや](../Page/アップル_\(企業\).md "wikilink")[NeXT](../Page/NeXT.md "wikilink")コンピュータにも採用された。だが[21世紀](../Page/21世紀.md "wikilink")に入る頃には、もはや広く使われることのない規格となった。[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")の登録商標（日本における商標登録番号は第2315207号）である。

## アーキテクチャ

NuBusは、開発された当時のその他の[インタフェースと比較して](../Page/インタフェース_\(情報技術\).md "wikilink")、かなり先進的な設計だった。当時のたいていのコンピュータシステムのバスは[8ビット](../Page/8ビット.md "wikilink")で、その8ビットのバスで他のコンピュータと接続されていた。しかしながら、市場はより高速なバスを求めていることは明らかであったので、NuBusは32ビットインタフェースの採用を決めた。

加えて、NuBusはプロセッサ非依存であった。たいていのバスは基本的には、[CPU](../Page/CPU.md "wikilink")上のピンをそのまま基板上に出しているだけであった。つまり、[拡張カード](../Page/拡張カード.md "wikilink")は接続先のマシンのデータ構造(たとえばリトルエンディアン)や信号規格を満たしていなければならなかった。NuBusはこのような仮定を取り除き、適切な[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")が用意されるならば、NuBusカードはどのNuBusマシンにも接続できるようにした。

適切なデバイスドライバを選択するために、NuBusには、NuBusカードが起動時にホストコンピュータを識別できる仕組みがある。バスにカードを接続する際の面倒なシステム設定を行う必要がなかった。たとえば、[Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA) では、カードの設定だけでなく、カードが使用するメモリ空間や[割り込みなども設定しなければならない](../Page/割り込み_\(コンピュータ\).md "wikilink")。NuBusはこのような設定は必要とせず、[プラグアンドプレイ](../Page/プラグアンドプレイ.md "wikilink")をサポートするアーキテクチャの最初の一例となった。

この柔軟性のために、NuBusはユーザーとデバイスドライバ作成者にとっては非常に単純なものになったが、代わりにカードの設計者にとってはより難しくなった。たいていの「単純」なバスシステムは、ターゲットCPU用に設計された少ない入出力チップを使えば簡単にサポートできたのに対して、NuBusは、すべてのNuBusカードとコンピュータを、プラットフォーム非依存な「NuBusワールド」に変えなければならなかった。一般的に、このことは、カード上のバスと[I/Oチップとの間にNuBusコントローラチップを加え](../Page/入出力.md "wikilink")、カードのコストが増えることを意味した。この対策は今日では取るに足らないものであり、すべての新しいバスには必要なものであるのに対して、[1980年](https://ja.wikipedia.org/wiki/1980年 "wikilink")当時は、NuBusは複雑で高価なものであると思われた。

## 実装

NuMachineはリリースされることがなかったが、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")は1980年にNuBusを採用し、[IEEE](../Page/IEEE.md "wikilink")1196として標準化した。このバージョンは[VMEバス](../Page/VMEバス.md "wikilink") や他のバスで見られる標準の96ピンの3列コネクタを使っていて、10MHzのクロックで最大バースト転送速度40MB/sと10MB/sから20MB/sの平均転送速度を出すことができた。後に追加されたNuBus90は、転送速度を上げるためにクロックは20MHzに引き上げられ、バースト転送速度は70MB/s、平均転送速度は約30MB/sにまで増加した。

NuBusは、よくデザインされたMITのNuMachineの派生品である、テキサス・インスツルメンツが開発したTI Explorerという[LISPマシン](../Page/LISPマシン.md "wikilink")に最初に用いられた。その後まもなく、[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")にテキサス・インスツルメンツはS1500マルチプロセッサUNIXシステムに採用した。

NuBusは、アップルコンピュータによって[Macintosh IIプロジェクトに採用された](../Page/Macintosh.md "wikilink")。そのプラグアンドプレイで使える特徴は、簡単に使えるというMacの哲学にぴったり一致していた。NuBusは[1980年代](../Page/1980年代.md "wikilink")後半から[1990年代](../Page/1990年代.md "wikilink")を通してMacintoshの大部分の製品ラインアップに使われた。そして、Macintosh Quadra以降からNuBus90にアップグレードされた。ただ、ロジックボード上のコントローラがアップグレードされなかったので、初期のQuadraは2枚のカードが互いに通信する場合、20MHzのクロックしかサポートしていなかった。この仕様は後に660AVと840AVにも搭載され、初期の[Power Macintoshにも使われた](../Page/Power_Macintosh.md "wikilink")。また、アップルコンピュータの実装は、コンピュータの電源をオフにする間、電話線を監視するタスク([Wake-on-Ring](https://ja.wikipedia.org/wiki/Wake-on-Ring "wikilink"))を動かすために、トリッキーな5V電源の常時供給も行った。これは明らかにNuBus標準として認められていないものであった。

NuBusはNeXT BUSとしてNeXTコンピュータ([NeXTcube](../Page/NeXTcube.md "wikilink")および[NeXTstation](https://ja.wikipedia.org/wiki/NeXTstation "wikilink"))にも採用されたが、物理的な配線は異なっていた。NuBusはこれら以外のコンピュータにはほとんど使用されていなかった。そして、アップルコンピュータが[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に[PCIに切り替えると](../Page/Peripheral_Component_Interconnect.md "wikilink")、NuBusはすぐに消えた。

## 関連項目

  - [Apple Desktop Bus](../Page/Apple_Desktop_Bus.md "wikilink") (ADB)
  - [Cバス](../Page/Cバス.md "wikilink")
  - [Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA)
  - [Extended Industry Standard Architecture](../Page/Extended_Industry_Standard_Architecture.md "wikilink") (EISA)
  - [Micro Channel architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") (MCA)
  - [VESA ローカルバス](../Page/VESA_ローカルバス.md "wikilink") (VESA)
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI)
  - [Accelerated Graphics Port](../Page/Accelerated_Graphics_Port.md "wikilink") (AGP)
  - [PCI Express](../Page/PCI_Express.md "wikilink") (PCIe)

## 外部リンク

  - [NuBus specs](http://www.bitsavers.org/pdf/ti/2242825-0001_NuBus_Spec1983.pdf)

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink")