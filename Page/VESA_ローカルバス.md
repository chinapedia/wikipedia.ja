> この記事は[VESA ローカルバス](https://ja.wikipedia.org/wiki/VESA_ローカルバス)から翻訳されています。


**VESA ローカルバス**は、**VLバス**とも呼ばれ、当時乱立していた[グラフィックアクセラレータ](../Page/グラフィックアクセラレータ.md "wikilink")接続用[ローカルバス](https://ja.wikipedia.org/wiki/ローカルバス "wikilink")を統一すべく、[パソコン向けグラフィックス機器メーカーの業界団体](../Page/パーソナルコンピュータ.md "wikilink")[VESA](../Page/VESA.md "wikilink")によって[1992年](../Page/1992年.md "wikilink")[8月](../Page/8月.md "wikilink")に策定されたローカルバス規格である。

## 概要

[ISAコネクタの先に](../Page/Industry_Standard_Architecture.md "wikilink")[MCAコネクタを設置し](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")、そこに[i486のメモリバスを直結する構造で](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")、ISA部分が通常の[I/O](../Page/入出力.md "wikilink")（[ポートマップドI/O](https://ja.wikipedia.org/wiki/ポートマップドI/O "wikilink")）と[割り込みを](../Page/割り込み_\(コンピュータ\).md "wikilink")、MCAコネクタ部分が[メモリマップドI/O](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")と[DMAを担当する](../Page/Direct_Memory_Access.md "wikilink")。

[VGAカード](../Page/Video_Graphics_Array.md "wikilink")、[SCSIカード](../Page/Small_Computer_System_Interface.md "wikilink")、[マルチ](../Page/マルチ.md "wikilink")I/Oカード等が商品化されていた。

VLバスは、ISAの後継たる汎用高速バス出現までの**つなぎ**として設計されたもので、i486に強く依存した構造であるため以下の制限を持っており、[PCIバス登場後はその普及と共に姿を消していった](../Page/Peripheral_Component_Interconnect.md "wikilink")。

<File:I486> ISA- VL-Bus-Mainboard.jpg <File:Motherboard> Baby AT.jpg <File:KL> Trident TGUI9440 VLB.jpg

## 欠点

  - i486依存
    前述の通り、i486のメモリバスをそのまま利用しているため、他の[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")に直接実装することは殆ど不可能である。下記のように一部の[Pentium機にも搭載されているが](../Page/Intel_Pentium_\(1993年\).md "wikilink")、間に[バス変換](../Page/バス_\(コンピュータ\).md "wikilink")[ブリッジ](../Page/ブリッジ.md "wikilink")が入っているため本来の性能は発揮できない。
    当時の日本では世界と比べてPCが低性能で割高な傾向があり、PCIの登場まで486機が多く使われた結果、VLバスを備えたPentium機はごく一部の高級機に限られた。しかしPentiumが早期から普及していたアメリカにおいてはその間もVLバスを使わざるをえなかったため、PCIが充分に普及するまでの一時期は、意外にもVLバスを備えたPentium機が主流を担う事態となっていた。

<!-- end list -->

  - 利用可能なスロット数が少ない
    i486のメモリバスそのものであるため、あまり配線を伸ばすことができない。そのため、ベースクロックが25[MHz](https://ja.wikipedia.org/wiki/MHz "wikilink")の場合は3本、33MHzの場合2本、50MHzの場合は1本の使用が可能とされている。

<!-- end list -->

  - 信頼性が低い
    本来、短距離であるが故に信頼性の高い[伝送路](../Page/伝送路.md "wikilink")として想定されているメモリバスをそのまま引き出した構造であるため、エラー検出機能、エラー訂正機能や再送機能などが存在しない。そのため、[ノイズ](../Page/ノイズ.md "wikilink")対策などが充分行われていない安価な[マザーボード](../Page/マザーボード.md "wikilink")のVLバスに[ハードディスクコントローラ等を接続した場合](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、大規模なデータ化けが発生する可能性がある。
    またコネクタそのものが長く、カードの装着が困難で基板を物理的に破壊してしまうことがある。一部で『**Very Long Bus**の略』と揶揄されるのは、このコネクタの長さからである。

## 類似バスについて

[PC-9821A-Mateの](../Page/PC-9821シリーズ.md "wikilink")[98ローカルバス](../Page/98ローカルバス.md "wikilink")もこれに準ずるものとして扱われることが多いが、こちらは[NESAバスのサブセットに近い構造で](../Page/New_Extend_Standard_Architecture.md "wikilink")、元のNESA同様、電源や信号特性はVLバスと比較にならないほど良好である。ただしi486に依存し、Pentium機では性能を充分に発揮できない点は同じである。

## 関連項目

  - [98ローカルバス](../Page/98ローカルバス.md "wikilink")
  - [New Extend Standard Architecture](../Page/New_Extend_Standard_Architecture.md "wikilink") (NESA)
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI)
  - [Extended Industry Standard Architecture](../Page/Extended_Industry_Standard_Architecture.md "wikilink") (EISA)
  - [Micro Channel Architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") (MCA)
  - [Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA)
  - [XTバス](../Page/XTバス.md "wikilink")
  - [VESA](../Page/VESA.md "wikilink")

## 外部リンク

  - [VESA](http://www.vesa.org/)

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")