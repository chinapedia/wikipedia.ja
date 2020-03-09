> この記事は[Peripheral Component Interconnect](https://ja.wikipedia.org/wiki/Peripheral_Component_Interconnect)から翻訳されています。


[200pxにある](https://ja.wikipedia.org/wiki/ファイル:pci-slots.jpg "wikilink")32[ビット](https://ja.wikipedia.org/wiki/ビット "wikilink")PCIバススロット\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:64bitpci.jpg "wikilink")

**Peripheral Component Interconnect**（ペリフェラル コンポーネント インターコネクト）、略して**PCI**とは[コンピュータ](../Page/コンピュータ.md "wikilink")の[プロセッサ](https://ja.wikipedia.org/wiki/プロセッサ "wikilink")と[周辺機器](https://ja.wikipedia.org/wiki/周辺機器 "wikilink")との間の[通信](https://ja.wikipedia.org/wiki/通信 "wikilink")を行うための[バス](https://ja.wikipedia.org/wiki/バス_\(コンピュータ\) "wikilink")[アーキテクチャ](https://ja.wikipedia.org/wiki/アーキテクチャ "wikilink")の一つ。

おおむね2000年代初頭を中心とした前後数年間において、**PCIバス**は[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")（パソコン）または[ワークステーション](https://ja.wikipedia.org/wiki/ワークステーション "wikilink")、[サーバ](https://ja.wikipedia.org/wiki/サーバ "wikilink")、[オフィスコンピュータ](https://ja.wikipedia.org/wiki/オフィスコンピュータ "wikilink")用の[拡張カード](https://ja.wikipedia.org/wiki/拡張カード "wikilink")を増設するための業界標準のバスとして広く採用されていたが、2004年に登場した後継規格の[PCI Expressがまず](https://ja.wikipedia.org/wiki/PCI_Express "wikilink")[グラフィックカードの分野で急速に普及し](https://ja.wikipedia.org/wiki/ビデオカード "wikilink")、その他の拡張カードも2010年代中盤頃にかけて次第に代替されていった。

## 規格

  - [2003年](../Page/2003年.md "wikilink")現在、最新のバージョンはPCI 3.0である。
  - 一般のパソコンではPCI 2.3準拠の 32ビットの33MHz、5VのPCIバスが採用されている。
  - 動作[クロック](https://ja.wikipedia.org/wiki/クロック "wikilink")は最大33MHzまたは最大66MHzで下限クロック数は規定されていない。
      - これはPCIの動作単位がクロックではなく実時間（例:Output Delayはクロック立ち上がりより12ns後）で規定されている為である。
  - [バス幅](https://ja.wikipedia.org/wiki/バス幅 "wikilink")は32ビットまたは64ビットで、1バスセグメント内で10デバイスをサポートする。それ以上の数のデバイスを接続する場合は、PCIバス-PCIバスブリッジを使用しバスセグメントを拡張するか、バスコントローラそのものを増設しセグメント数を増やす。
      - 拡張スロットは33MHzの場合2デバイス、66MHzの場合4デバイス扱いで、チップセットなどのバスコントローラも1デバイスないしは2デバイスとして扱われるため、1バスセグメントで最大4スロットまでの実装が可能となる\[1\]。
      - また、32ビットスロットに64ビットの拡張カードを挿入して使用することやその逆も可能であるように設計されている。ただしこれはバス設計に於いてであって、挿入するカードがその互換性を持っているか否かは別問題であり、特に64ビットカードを32ビットスロットに装着した場合、宙に浮いた32ビット分の処理はカード側の処理（すなわち設計）に依る。
  - 動作[電圧](https://ja.wikipedia.org/wiki/電圧 "wikilink")は5Vまたは3.3Vであり、カードの切り欠き、スロット突起の有無により誤挿入を防止している。
      - PCIカードの表を正面に見て右にだけ切り欠きがあるものが5V専用、左にのみ切り欠きがあるものは3.3V専用、左右に切り欠きが有るものは両方対応している。
  - PCIデバイスは、各々のベンダが固有の[PCI IDを持つ](https://ja.wikipedia.org/wiki/PCI_ID "wikilink")。
  - マザーボードや相性にもよるが、[AGPコネクタの隣に位置するPCIコネクタはリソース等の競合が起こる事があり](https://ja.wikipedia.org/wiki/Accelerated_Graphics_Port "wikilink")、正常に動作しない場合は、別のPCIスロットを使用して再確認する事が推奨されている。大型のクーラーを装備するビデオカードの場合、隣のPCIスロットが物理的に使えないこともしばしばである。
  - 特に規定があるわけではないが、スロットのコネクタ色は白色が多い。
  - [ISAバスとは](https://ja.wikipedia.org/wiki/Industry_Standard_Architecture "wikilink")、部品を実装する面が向きが逆であり、ATXの縦型ケースでは、部品面が下になる。これはAGP、PCI-EXpressにも引き継がれた。
  - ISAバスとPCIバスが混在した時期においては、隣接するISAバスとPCIバスは、PCケースの細長い穴を共用するために、同時には使えないことが多かった。このためPCI,ISA3本ずつでも、PCI2,ISA2,PCI/ISA1と表記される事もあった。

## 歴史

[thumb](https://ja.wikipedia.org/wiki/ファイル:Scsiboard01.jpg "wikilink")

**PCIバス**は、当初[CPU](../Page/CPU.md "wikilink")アーキテクチャに全く依存しないデバイス間を結ぶ内部高速バス**Local Glueless Bus**として、[1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink")に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")から提案された。

その当時、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")においては、標準の拡張バスである[ISAバス](https://ja.wikipedia.org/wiki/Industry_Standard_Architecture "wikilink")（いわゆるATバス）が低速、かつ[バス調停](https://ja.wikipedia.org/wiki/バス調停 "wikilink")機能が存在しなかったため、高速なデバイス（[VGAや](https://ja.wikipedia.org/wiki/Video_Graphics_Array "wikilink")[LAN](../Page/Local_Area_Network.md "wikilink")、[SCSI等](https://ja.wikipedia.org/wiki/Small_Computer_System_Interface "wikilink")）の接続、[マルチタスク](../Page/マルチタスク.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の運用などの際ボトルネックになっていた。

そのため、全く新しい設計の16/32ビットバスである[MCAバス](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")、ISAバスを拡張しそれに対する上位互換機能を備えた32ビットバスである[EISAバス](https://ja.wikipedia.org/wiki/Extended_Industry_Standard_Architecture "wikilink")、[i486の](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")バスをそのまま引き出した[VLバスなどが登場したが](https://ja.wikipedia.org/wiki/VESA_ローカルバス "wikilink")、MCAバスは高度なバス調停機能を持つがISAバスとの互換性が無く、また特許権の問題から[IBM](../Page/IBM.md "wikilink")以外にはほとんど普及せず、EISAバスは高度なバス調停機能による高価格化とISA互換によるデータ[転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")の不足、VLバスは転送速度は充分（50MHz駆動時200MB/秒）だがi486アーキテクチャに強く依存し互換性・安定性が不十分でバス調停機能は存在しない、などの理由で、それぞれ限定的にしか普及しなかった。

このため、インテルの提案を受けた各社から、ISAを代替する高速な標準汎用バスとしてLocal Glueless Busを外部バス化する要求が多く寄せられた。

この要求に対し、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")や[PC-9821シリーズ](https://ja.wikipedia.org/wiki/PC-9821シリーズ "wikilink")への実装を目的とした機種依存仕様の追加、64ビットバスへの拡張対応、拡張スロット形状を含めた最終の形に近いPCIバスの仕様が、インテルを中心として策定された。

PCIバスは、策定当初からアーキテクチャに依存しない汎用高速バスとして設計されていたが、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")における標準バスとしての地位が約束されていた訳ではなかった。このため、PCIバスを搭載した初期の[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")にはEISAバスとVLバスも搭載するという変則的な製品やVLバス上にPCIブリッジを実装する製品も存在した。

また、PCIバスはワークステーションやサーバ、オフィスコンピュータなどの方面にも同時に取り入れられていった。この方面ではEISAバス、[APバス](https://ja.wikipedia.org/wiki/APバス "wikilink")、[VMEバス](https://ja.wikipedia.org/wiki/VMEバス "wikilink")などを使用していたが、特にコンピュータグラフィックや衛星画像処理などで大規模な画像データを表示する必要に迫られたり、大規模なデータを取り扱うSCSI等にいちはやく取り入れられていった。同時に、i486系のCPUを持つワークステーションのみならず、[R4400](https://ja.wikipedia.org/wiki/R4000 "wikilink")、[R10000](https://ja.wikipedia.org/wiki/R10000 "wikilink")等、[MIPS系の](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")[RISC](https://ja.wikipedia.org/wiki/RISC "wikilink")型CPUを持つワークステーションやサーバ等でも利用できるよう、PCIコントローラーが開発され実装されていった。また、サーバなどのボードの拡張を容易にするため、PCIブリッジと呼ばれる外部筐体にPCIバスを拡張するコントローラーも開発され、i486系、[MIPS系のサーバに使用されている](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")。

2002年には、PCIと[AGPの後継規格である](https://ja.wikipedia.org/wiki/Accelerated_Graphics_Port "wikilink")[PCI Expressが発表される](https://ja.wikipedia.org/wiki/PCI_Express "wikilink")。 [thumb](https://ja.wikipedia.org/wiki/ファイル:Minipci.jpg "wikilink")

  - [1991年](https://ja.wikipedia.org/wiki/1991年 "wikilink") 原案である「Local Glueless Bus」が発表。
    「PCI Local Bus」として規格化すべく PCI SIG が設立された。

  - [1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink") PCI 1.0策定。
    内部接続バスとしての仕様のみ規定され、見切り発車などとも言われた。

  - [1993年](../Page/1993年.md "wikilink") PCI 2.0策定。
    64bit規格、コネクタ仕様等が制定され、製品への本格的な実装が開始された。

  - [1994年](../Page/1994年.md "wikilink") PCI 2.1へ改訂。
    Delayed Transactionの明文化、PCIバスブリッジや66MHzの仕様が盛り込まれる。

  - [1999年](../Page/1999年.md "wikilink") PCI 2.2へ改訂。
    MSI (Message Signaled Interrupt) と言うサイドバンド信号線無しで割り込み通知等の機能が追加され、これに準拠した別ケーブル無しでの[WOL対応](https://ja.wikipedia.org/wiki/Wake-on-LAN "wikilink")[イーサネット](https://ja.wikipedia.org/wiki/イーサネット "wikilink")カードや[PCMCIAインタフェースが販売された](https://ja.wikipedia.org/wiki/PCカード "wikilink")。

  - [2000年](../Page/2000年.md "wikilink") PCI 2.3へ改訂。
    5Vのみで動作する拡張カードの廃止。マザーボード側スロットへの5V給電（配電）は引き続き許される。

  - [2002年](../Page/2002年.md "wikilink") PCI 3.0制定。
    マザーボード側スロットへの5V給電（配電）を廃止。

  - [2002年](../Page/2002年.md "wikilink") 派生規格 [PCI-X](https://ja.wikipedia.org/wiki/PCI-X "wikilink") 1.0b 及び PCI-X 2.0制定。

[thumb](https://ja.wikipedia.org/wiki/ファイル:PCI-X_Ethernet.jpg "wikilink")

  -
    64bitPCIの後継規格で、1バスセグメント内で66MHzなら4本、100MHzなら2本、133MHz動作なら1本のスロットが使用可能などの機能拡張が行われている。

    PCI-X 2.0では、信号電圧の1.5Vへの動的変更を行うことで、DDR (Double Data Rate:倍速)やQDR（Quad Data Rate : 4倍速）でのデータ転送をサポートする。

  - [2002年](../Page/2002年.md "wikilink") 後継規格 [PCI Express](https://ja.wikipedia.org/wiki/PCI_Express "wikilink") 1.0制定。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Gigabyte_GV-NX62TC256D8_Rev_1.0.jpg "wikilink")

  -
    プロトコルと信号が混在していたPCIを見直し、各層を完全に分割し、スケーラビリティを確保した規格。これ以降のPCの標準汎用拡張バスとなった。[PCカード](https://ja.wikipedia.org/wiki/PCカード "wikilink")においてもPCI Express派生規格の[ExpressCard](https://ja.wikipedia.org/wiki/ExpressCard "wikilink")による置き換えが進んだ。

## 脚注

## 関連項目

  - [PCI Express](https://ja.wikipedia.org/wiki/PCI_Express "wikilink") - 後継規格

  -
  - [Accelerated Graphics Port](https://ja.wikipedia.org/wiki/Accelerated_Graphics_Port "wikilink") (AGP)

  - [Extended Industry Standard Architecture](https://ja.wikipedia.org/wiki/Extended_Industry_Standard_Architecture "wikilink") (EISA)

  - [Industry Standard Architecture](https://ja.wikipedia.org/wiki/Industry_Standard_Architecture "wikilink") (ISA)

  - [Micro Channel Architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") (MCA)

  - [VESA ローカルバス](https://ja.wikipedia.org/wiki/VESA_ローカルバス "wikilink")（VLバス）

  - [APバス](https://ja.wikipedia.org/wiki/APバス "wikilink")

  - [XTバス](https://ja.wikipedia.org/wiki/XTバス "wikilink")

  - [ロープロファイルPCI](https://ja.wikipedia.org/wiki/ロープロファイルPCI "wikilink")

  - [コンパクトPCI](https://ja.wikipedia.org/wiki/コンパクトPCI "wikilink")

## 外部リンク

  - [PCI-SIG](http://www.pcisig.com/)
  - [PCI ID](http://pciids.sourceforge.net)
  - [PCI Rev間差異の比較](http://dualsocketworld.blog134.fc2.com/blog-entry-42.html)
  - [Linux with miniPCI cards](http://tuxmobil.org/minipci_linux.html)
  - [PCIの5Vと3.3Vに付いて](http://dualsocketworld.blog134.fc2.com/blog-entry-267.html)

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  ただし、これはPCI規格を提唱したIntelのガイドラインで示された、拡張スロットの電気的負荷を考慮し一定の余裕を確保した値である。そのため、PCIバス全盛期のPC/AT互換機用マザーボードでは基板の回路設計を工夫してバスの負荷を軽減し、4スロット前提のIRQルーティングを拡張・整合させる回路を付加することで、最大6スロットの32ビット33MHz PCIバススロットを1バスセグメント接続で実装する製品が多数存在した。