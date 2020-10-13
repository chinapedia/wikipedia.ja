> この記事は[Peripheral Component Interconnect](https://ja.wikipedia.org/wiki/Peripheral_Component_Interconnect)から翻訳されています。


[thumbにある](https://ja.wikipedia.org/wiki/ファイル:pci-slots.jpg "wikilink")32[ビット](../Page/ビット.md "wikilink")PCIバススロット\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:64bitpci.jpg "wikilink")

**Peripheral Component Interconnect**（ペリフェラル コンポーネント インターコネクト、**PCI**）は、[コンピュータ](../Page/コンピュータ.md "wikilink")の[プロセッサ](../Page/プロセッサ.md "wikilink")と[周辺機器](../Page/周辺機器.md "wikilink")との間の[通信](../Page/通信.md "wikilink")を行うための[バス](../Page/バス_\(コンピュータ\).md "wikilink")[アーキテクチャ](../Page/アーキテクチャ.md "wikilink")の一つ。

## 概要

おおむね2000年代初頭を中心とした前後数年間において、**PCIバス**は[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")（パソコン）または[ワークステーション](../Page/ワークステーション.md "wikilink")、[サーバ](../Page/サーバ.md "wikilink")、[オフィスコンピュータ](../Page/オフィスコンピュータ.md "wikilink")用の[拡張カード](../Page/拡張カード.md "wikilink")を増設するための業界標準のバスとして広く採用されていたが、2004年に登場した後継規格の[PCI Expressが](../Page/PCI_Express.md "wikilink")、まず[グラフィックカードの分野で急速に普及し](../Page/ビデオカード.md "wikilink")、その他の拡張カードも2010年代中盤頃にかけて次第に代替されていった。

## 規格

  - [2003年](../Page/2003年.md "wikilink")現在、最新のバージョンはPCI 3.0である。
  - 一般のパソコンではPCI 2.3準拠の 32ビットの33 [MHz](https://ja.wikipedia.org/wiki/MHz "wikilink")、帯域幅132 [MB/s](https://ja.wikipedia.org/wiki/ビット毎秒#バイト毎秒 "wikilink")、5 [V信号のPCIバスが採用されていた](../Page/ボルト.md "wikilink")。64ビット/66 MHz PCIやさらに高速な[PCI-X](../Page/PCI-X.md "wikilink")は高価で、一部の[Power Macなどに搭載された以外は](../Page/Power_Mac.md "wikilink")、[シリアルATA](https://ja.wikipedia.org/wiki/シリアルATA "wikilink")や[1000BASE-Tの登場で](../Page/ギガビット・イーサネット.md "wikilink")32ビット/33 MHz PCI帯域幅の限界が目立つようになって[PCI Expressへの移行に至るまで](../Page/PCI_Express.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")、[ワークステーション](../Page/ワークステーション.md "wikilink")などでの採用にとどまった。
  - 動作[クロック](../Page/クロック.md "wikilink")は最大33 MHzまたは最大66 MHzで下限クロック数は規定されていない。
      - これはPCIの動作単位がクロックではなく実時間（例:Output Delayはクロック立ち上がりより12[ナノ秒](../Page/ナノ秒.md "wikilink")後）で規定されている為である。
  - [バス幅](https://ja.wikipedia.org/wiki/バス幅 "wikilink")は32ビットまたは64ビットで、1バスセグメント内で32デバイスをサポートする。それよりも多くのデバイスを接続する場合は、PCIバス-PCIバスブリッジを使用しバスセグメントを拡張するか、バスコントローラそのものを増設しセグメント数を増やす。
      - 拡張スロットの電気的負荷を考慮した値は、1バスセグメント内で10デバイスまで。ただし、拡張スロットは33 MHzの場合2デバイス、66 MHzの場合4デバイス扱いで、チップセットなどのバスコントローラも1デバイスないしは2デバイスとして扱われるため、1バスセグメントで最大4スロットまでの実装が可能となる。\[1\]。

      - 32ビットスロットに64ビットの拡張カードを挿入して使用することやその逆も可能であるように設計されている。ただしこれはバス設計に於いてであって、挿入するカードがその互換性を持っているか否かは別問題であり、特に64ビットカードを32ビットスロットに装着した場合、宙に浮いた32ビット分の処理はカード側の処理（すなわち設計）に依る。
  - 信号[電圧](../Page/電圧.md "wikilink")は5 Vまたは3.3 Vであり、カードの切り欠き、スロット突起の有無により誤挿入を防止している。
      - PCIカードの表を正面に見て右にだけ切り欠きがあるものが5 V信号専用、左にのみ切り欠きがあるものは3.3 V信号専用、左右に切り欠きが有るものは5 V信号と3.3 V信号の両方に対応している。
  - PCIデバイスは、各々のベンダが固有の[PCI IDを持つ](https://ja.wikipedia.org/wiki/PCI_ID "wikilink")。
  - マザーボードや相性にもよるが、[AGPコネクタの隣に位置するPCIコネクタはリソース等の競合が起こる事があり](../Page/Accelerated_Graphics_Port.md "wikilink")、正常に動作しない場合は、別のPCIスロットを使用して再確認する事が推奨されている。大型のクーラーを装備するビデオカードの場合、隣のPCIスロットが物理的に使えないこともしばしばである。
  - 特に規定があるわけではないが、スロットのコネクタ色は白色が多い。
  - [ISAバスとは](../Page/Industry_Standard_Architecture.md "wikilink")、部品を実装する面が向きが逆であり、ATXの縦型ケースでは、部品面が下になる。これはAGP、PCI-EXpressにも引き継がれた。
  - ISAバスとPCIバスが混在した時期においては、隣接するISAバスとPCIバスは、PCケースの細長い穴を共用するために、同時には使えないことが多かった。このためPCI, ISA3本ずつでも、PCI2, ISA2, PCI/ISA1と表記される事もあった。

## 歴史

[thumb](https://ja.wikipedia.org/wiki/ファイル:Scsiboard01.jpg "wikilink")

**PCIバス**は、当初[CPU](../Page/CPU.md "wikilink")アーキテクチャに全く依存しないデバイス間を結ぶ内部高速バスとして、[1991年](../Page/1991年.md "wikilink")に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")から提案された。

その当時、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")においては、標準の拡張バスである[ISAバス](../Page/Industry_Standard_Architecture.md "wikilink")（いわゆるATバス）が低速、かつ[バス調停](https://ja.wikipedia.org/wiki/バス調停 "wikilink")機能が存在しなかったため、高速なデバイス（[VGAや](../Page/Video_Graphics_Array.md "wikilink")[LAN](../Page/Local_Area_Network.md "wikilink")、[SCSI等](../Page/Small_Computer_System_Interface.md "wikilink")）の接続、[マルチタスク](../Page/マルチタスク.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の運用などの際ボトルネックになっていた。

そのため、全く新しい設計の16/32ビットバスである[MCAバス](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")、ISAバスを拡張しそれに対する上位互換機能を備えた32ビットバスである[EISAバス](../Page/Extended_Industry_Standard_Architecture.md "wikilink")、[i486の](https://ja.wikipedia.org/wiki/Intel_486 "wikilink")[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")バスをそのまま引き出した[VLバスなどが登場したが](../Page/VESA_ローカルバス.md "wikilink")、MCAバスは高度なバス調停機能を持つがISAバスとの互換性が無く、また特許権の問題から[IBM](../Page/IBM.md "wikilink")以外にはほとんど普及せず、EISAバスは高度なバス調停機能による高価格化とISA互換によるデータ[転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")の不足、VLバスは転送速度は充分（50 MHz駆動時200 MB/s）だがi486アーキテクチャに強く依存し互換性・安定性が不十分でバス調停機能は存在しなかった。

このため、インテルの提案を受けた各社から、ISAを代替する高速な標準汎用バスとしてを外部バス化する要求が多く寄せられた。

この要求に対し、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")や[PC-9821シリーズ](../Page/PC-9821シリーズ.md "wikilink")への実装を目的とした機種依存仕様の追加、64ビットバスへの拡張対応、拡張スロット形状を含めた最終の形に近いPCIバスの仕様が、インテルを中心として策定された。

PCIバスは、策定当初からアーキテクチャに依存しない汎用高速バスとして設計されていたが、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")における標準バスとしての地位が約束されていた訳ではなかった。このため、PCIバスを搭載した初期の[マザーボード](../Page/マザーボード.md "wikilink")にはEISAバスとVLバスも搭載するという変則的な製品やVLバス上にPCIブリッジを実装する製品も存在した。

PCIバスはワークステーションやサーバ、オフィスコンピュータなどの方面にも同時に取り入れられていった。この方面ではEISAバス、[APバス](../Page/APバス.md "wikilink")、[VMEバス](../Page/VMEバス.md "wikilink")などを使用していたが、特にコンピュータグラフィックや衛星画像処理などで大規模な画像データを表示する必要に迫られたり、大規模なデータを取り扱うSCSI等にいちはやく取り入れられていった。同時に、i486系のCPUを持つワークステーションのみならず、[R4400](https://ja.wikipedia.org/wiki/R4000 "wikilink")、[R10000](https://ja.wikipedia.org/wiki/R10000 "wikilink")等、[MIPS系の](../Page/MIPSアーキテクチャ.md "wikilink")[RISC](../Page/RISC.md "wikilink")型CPUを持つワークステーションやサーバ等でも利用できるよう、PCIコントローラーが開発され実装されていった。サーバなどのボードの拡張を容易にするため、PCIブリッジと呼ばれる外部筐体にPCIバスを拡張するコントローラーも開発され、i486系、[MIPS系のサーバに使用されている](../Page/MIPSアーキテクチャ.md "wikilink")。

2002年には、PCIと[AGPの後継規格である](../Page/Accelerated_Graphics_Port.md "wikilink")[PCI Expressが発表される](../Page/PCI_Express.md "wikilink")。 [thumb](https://ja.wikipedia.org/wiki/ファイル:Minipci.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:PCI-X_Ethernet.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Gigabyte_GV-NX62TC256D8_Rev_1.0.jpg "wikilink")

  - [1991年](../Page/1991年.md "wikilink") 原案である「」が発表。
    「」として規格化すべく PCI SIG が設立された。

  - [1992年](../Page/1992年.md "wikilink") PCI 1.0策定。
    内部接続バスとしての仕様のみ規定され、見切り発車などとも言われた。

  - [1993年](../Page/1993年.md "wikilink") PCI 2.0策定。
    64bit規格、コネクタ仕様等が制定され、製品への本格的な実装が開始された。

  - [1994年](../Page/1994年.md "wikilink") PCI 2.1へ改訂。
    Delayed Transactionの明文化、PCIバスブリッジや66 MHzの仕様が盛り込まれる。

  - [1999年](../Page/1999年.md "wikilink") PCI 2.2へ改訂。

    と言うサイドバンド信号線無しで割り込み通知等の機能が追加され、これに準拠した別ケーブル無しでの[WOL対応](../Page/Wake-on-LAN.md "wikilink")[イーサネット](../Page/イーサネット.md "wikilink")カードや[PCMCIAインタフェースが販売された](../Page/PCカード.md "wikilink")。

  - [2000年](../Page/2000年.md "wikilink") PCI 2.3へ改訂。
    5 V信号のみで動作する拡張カードの廃止。5 V信号で動作するマザーボード側スロットは引き続き仕様に含まれる。

  - [2002年](../Page/2002年.md "wikilink") PCI 3.0制定。
    5 V信号で動作するマザーボード側スロットの廃止。5 V信号と3.3 V信号の双方に対応する拡張カードは引き続き仕様に含まれる。

  - [2002年](../Page/2002年.md "wikilink") 派生規格 [PCI-X](../Page/PCI-X.md "wikilink") 1.0b 及び PCI-X 2.0制定。
    64bit PCIの後継規格で、1バスセグメント内で66 MHzなら4本、100 MHzなら2本、133 MHz動作なら1本のスロットが使用可能などの機能拡張が行われている。

    PCI-X 2.0では、信号電圧の1.5 Vへの動的変更を行うことで、DDR (:倍速)やQDR（ : 4倍速）でのデータ転送をサポートする。

  - [2002年](../Page/2002年.md "wikilink") 後継規格 [PCI Express](../Page/PCI_Express.md "wikilink") 1.0制定。
    プロトコルと信号が混在していたPCIを見直し、各層を完全に分割し、スケーラビリティを確保した規格。これ以降のPCの標準汎用拡張バスとなった。

  - [2003年](../Page/2003年.md "wikilink") [ExpressCard](../Page/ExpressCard.md "wikilink")策定。
    [PCカード](../Page/PCカード.md "wikilink")におけるPCI Express派生規格としてExpressCardが策定され、一時期はPCカードスロットの置き換えが進められた。しかしビジネス向けノートでは旧来のPCカードの需要が根強かったことや、急速に小型化が進んだ[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")ではUSBやメモリーカード用スロットで済まされるケースが目立ったこともあり、結果的にPCカードほどは普及せずに衰退した。

## 脚注

### 注釈・出典

## 参考 

  -
  -
## 関連項目

  - [PCI Express](../Page/PCI_Express.md "wikilink") - 後継規格

  -
  - [Accelerated Graphics Port](../Page/Accelerated_Graphics_Port.md "wikilink") (AGP)

  - [Extended Industry Standard Architecture](../Page/Extended_Industry_Standard_Architecture.md "wikilink") (EISA)

  - [Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA)

  - [Micro Channel Architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") (MCA)

  - [VESA ローカルバス](../Page/VESA_ローカルバス.md "wikilink")（VLバス）

  - [APバス](../Page/APバス.md "wikilink")

  - [XTバス](../Page/XTバス.md "wikilink")

  - [ロープロファイルPCI](../Page/ロープロファイルPCI.md "wikilink")

  - [コンパクトPCI](https://ja.wikipedia.org/wiki/コンパクトPCI "wikilink")

  - [ペリフェラル](../Page/周辺機器.md "wikilink")

  - [コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")

  -
## 外部リンク

  - [PCI-SIG](https://pcisig.com/)

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.  ただし、これは一定の余裕を確保した値である。そのため、PCIバス全盛期のPC/AT互換機用マザーボードでは基板の回路設計を工夫してバスの負荷を軽減し、最大6スロットの32ビット33 MHz PCIバススロットを1バスセグメント接続で実装する製品が多数存在した。