> この記事は[Micro Channel architecture](https://ja.wikipedia.org/wiki/Micro_Channel_architecture)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:MCA_IBM_XGA-2.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:MCA_NIC_IBM_83X9648.jpg "wikilink") **Micro Channel architecture** （マイクロチャネルアーキテクチャ、**MCA**、エムシーエー） または**Micro Channel**は[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")に[IBM](../Page/IBM.md "wikilink")が開発した、[CPU](../Page/CPU.md "wikilink")の[アーキテクチャに依存しない](../Page/コンピュータ・アーキテクチャ.md "wikilink")[16ビット](../Page/16ビット.md "wikilink")/[32ビット](../Page/32ビット.md "wikilink")の高速[バスアーキテクチャである](../Page/バス_\(コンピュータ\).md "wikilink")。

Micro Channelは[ISAの問題点を全て解決する為に設計されたバスアーキテクチャで](../Page/Industry_Standard_Architecture.md "wikilink")、[IBM PS/2](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")、[AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")、[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")、[System/370](https://ja.wikipedia.org/wiki/System/370 "wikilink")などの一部のモデルで採用された。

## 開発の経緯

### ISAの問題点

ISAは、遅いバススピード、[割り込み数の不足](../Page/割り込み_\(コンピュータ\).md "wikilink")、[バスマスタリング](https://ja.wikipedia.org/wiki/バスマスタリング "wikilink")機能の欠如、貧弱なグランドによる信号保護の不足、[XTバス](../Page/XTバス.md "wikilink")を拡張したが故の無秩序で非合理的な信号線の配列等、多数の問題点を抱えていた。これらの問題の大部分は、初期の[MS-DOS](../Page/MS-DOS.md "wikilink")を使用する限りにおいては問題とならなかったが、[周辺機器](../Page/周辺機器.md "wikilink")の性能向上や、[マルチタスク](../Page/マルチタスク.md "wikilink")への欲求とともに問題点が浮上してきた。

もう一つの問題は、ISAが [8088に強く依存した構造を持つことであった](../Page/Intel_8088.md "wikilink")。ISAカードは他のアーキテクチャではそのままではまともに動作しないであろう。

最後の問題は、IBMが[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")（パソコン）の[ハードウェア](../Page/ハードウェア.md "wikilink")市場の主導権を失っていたことである。誰でもISAカードを作って、誰でも[コンピュータ](../Page/コンピュータ.md "wikilink")の中にそれを導入することが出来たが、誰もISAカードの[互換性](../Page/互換性.md "wikilink")に関して保証を行っていなかった。

### 主導権の奪還

IBMは既に[デスクトップパソコン](../Page/デスクトップパソコン.md "wikilink")での[RISC](../Page/RISC.md "wikilink") [CPU](../Page/CPU.md "wikilink")採用を検討しており、全てのラインナップで同一のバスアーキテクチャが使用できれば大幅なコストの削減が可能であると判断していた。そこで、新しい標準を作り、仕様の使用に[ライセンス](../Page/ライセンス.md "wikilink")契約を必要とする事で、IBMはハードウェア市場の主導権を取り戻すことが出来ると考えた。これが、彼らが当時存在した高速バスアーキテクチャであった[NuBus](../Page/NuBus.md "wikilink")を採用せずに大金をかけてMicro Channelを作成した理由であった。

## 仕様

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:MCA_Slot_32_16_AVE.jpg "wikilink") Micro Channelは本来32ビットのバスであるが、PS/2のような[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")16ビットCPUベースのマシン等での使用の際のコネクタとロジックの価格を下げるため、16ビット版もサポートした。16ビット版のMicro Channelカード(Micro Channelではアダプターと呼ぶ)は、16ビットのMicro Channelスロットまたは32ビットのMicro Channelスロットに、32ビット版のMicro Channelカードは32ビットのMicro Channelスロットのみに、挿入し使用することができた。Micro Channelは信号の干渉を最小限に抑えるため、ピン配置を最適化し、信号線の周囲には必ず[アースと電源供給線が配置された](../Page/接地.md "wikilink")。

### バス転送速度

バスクロックはISAの8.33MHzから10MHzへとほんの少しだけ増やされただけだが、バスサイクルの見直しによるタイミングの切り詰め、データ幅の拡大、[DDR化](../Page/DDR_SDRAM.md "wikilink")、アドレスバスとデータバスを併用した64bit転送を行っているため、データ転送[スループット](../Page/スループット.md "wikilink")は理論最大40Mbytes/sec～160Mbytes/secと帯域幅はISAの実に5倍～20倍に増大している。

後の32bit 33MHzの[PCIでは理論最大データ転送速度が](../Page/Peripheral_Component_Interconnect.md "wikilink")133Mbytes/secであることから、Micro Channelは非常に効率のよいバスプロトコル設計が為されていたと言えよう。

### バスマスタと高度なバス調停機能

カード、メモリ間のみならず、カード、カード間のバスマスタ転送にも対応し、当然ながらCPUは一切それに関与しない。これは、バスマスタ要求の競合と言う事態を発生させ得るが、Micro Channelでは12ms単位でバス調停を行い、最も優先順位の高い処理にバスマスタを許すことで解決している。

この調停機構の存在により、非常にスループットの高いバス使用が可能となり、Micro Channelは他のシステムの介入無しにシステムCPUのスピードより高速にデータを転送することが出来た。

### POS(Programmable Option Select)

Micro Channel最大の特徴は**POS** (Programmable Option Select) と呼ばれる[ソフトウェア](../Page/ソフトウェア.md "wikilink")により[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")を自動設定できることである。おかげで、ISAでのディップスイッチなどを使用した地獄のような設定作業から逃れることが出来た。今日の [Plug and Playの始祖ともいえる](../Page/プラグアンドプレイ.md "wikilink")。

### 割り込みの共有

Micro Channelの割り込みはISAのエッジトリガ割り込みではなくレベルトリガ割り込みを採用しており、1本の割り込み線で複数の割り込みを処理することが可能である。これは、後のPCIに似た仕組みで、割り込みレベルがHIになったとき、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")が各Micro Channelデバイスが[ファームウェア](../Page/ファームウェア.md "wikilink")に持つ固有の[ID](../Page/ID.md "wikilink")を順に調べて行き、割り込みを要求しているデバイスの処理を行うことで実現している。

## 採用

Micro Channelは以下のコンピュータで採用された。

  - [IBM](../Page/IBM.md "wikilink")
      - [IBM PS/2の上位](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")・中位モデル (下位モデルや後の[PS/1](https://ja.wikipedia.org/wiki/PS/1 "wikilink")ではXTバスやATバスを継続した）
      - [PS/55](https://ja.wikipedia.org/wiki/PS/55 "wikilink")（[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")のS/T/Vモデル以降。PS/55noteは内部ATバス。）
      - [UNIX](../Page/UNIX.md "wikilink")サーバの[RS/6000](https://ja.wikipedia.org/wiki/RS/6000 "wikilink")
      - 小型[メインフレーム](../Page/メインフレーム.md "wikilink")の一部モデル([:en:PC-based IBM-compatible mainframes](https://ja.wikipedia.org/wiki/:en:PC-based_IBM-compatible_mainframes "wikilink"))
  - IBM以外
      - [タンディの一部のサーバー](../Page/ラジオシャック.md "wikilink")
      - ALRの一部のサーバー
      - [三菱電機](../Page/三菱電機.md "wikilink")のApricotシリーズ

## 衰退

Micro ChannelはISAの欠点を無くすために徹底的に改良を加えたものであったが、IBMが販売するハードウェアにのみ搭載された。そして、[EISAやXTバスアーキテクチャと同時に使用できないように](../Page/Extended_Industry_Standard_Architecture.md "wikilink")、全く互換性の無いものであった。

IBMはライセンス料金を下げるなどの対策を取らなかったため、Tandy・ALR・[三菱電機](../Page/三菱電機.md "wikilink")など[サーバ](../Page/サーバ.md "wikilink")専門の一部の[互換機](../Page/互換機.md "wikilink")メーカーのみにしか採用されず、Micro Channelは非常に小さなマーケットのまま高価格の製品に搭載されるのみとなった。

IBMの[PS/2](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")（日本では[PS/55](https://ja.wikipedia.org/wiki/PS/55 "wikilink")）は主に企業向けの上位・中位機種ではMicro Channelを採用し続けたが、低価格シリーズでは[PS/1](https://ja.wikipedia.org/wiki/PS/1 "wikilink")と[PS/ValuePoint](https://ja.wikipedia.org/wiki/PS/ValuePoint "wikilink")(日本では[PS/V](https://ja.wikipedia.org/wiki/PS/V "wikilink"))にてATバスに回帰し、上位・中位機種もIBM PC 700/300シリーズの中でMicro ChannelからPCIに移行した。その後、RS/6000もMicro ChannelからPCIに移行し、Micro Channelは市場から姿を消した。

## 参考文献

  - IBM PS/55・ハードウェア ハードウェア・インターフェース技術解説書、日本アイ・ビー・エム、オーム社、1990年、ISBN 9784274076268

## 関連項目

  - [Extended Industry Standard Architecture](../Page/Extended_Industry_Standard_Architecture.md "wikilink") (EISA)
  - [Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA)
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI)
  - [XTバス](../Page/XTバス.md "wikilink")
  - [VESA ローカルバス](../Page/VESA_ローカルバス.md "wikilink")
  - [98ローカルバス](../Page/98ローカルバス.md "wikilink")
  - [New Extend Standard Architecture](../Page/New_Extend_Standard_Architecture.md "wikilink") (NESA)
  - [Accelerated Graphics Port](../Page/Accelerated_Graphics_Port.md "wikilink") (AGP)
  - [PCI Express](../Page/PCI_Express.md "wikilink")

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink")