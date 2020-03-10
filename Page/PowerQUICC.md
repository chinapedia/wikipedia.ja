> この記事は[PowerQUICC](https://ja.wikipedia.org/wiki/PowerQUICC)から翻訳されています。


**PowerQUICC**（パワー クイック）は、[フリースケール・セミコンダクタ](https://ja.wikipedia.org/wiki/フリースケール・セミコンダクタ "wikilink")が製造している[POWERアーキテクチャに基づいた](../Page/PowerPC.md "wikilink")[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")の名称である。PowerQUICCは、一つまたは複数の[PowerPC](../Page/PowerPC.md "wikilink")コアと、**QUICC Engine**と呼ばれる、別の[RISC](../Page/RISC.md "wikilink")コアで構成される。QUICC Engineは、[I/O](../Page/入出力.md "wikilink")、通信、[ATM](../Page/Asynchronous_Transfer_Mode.md "wikilink")、セキュリティアクセラレータ、[ネットワーキング](https://ja.wikipedia.org/wiki/ネットワーキング "wikilink")、[USBのようなタスクに特化している](../Page/ユニバーサル・シリアル・バス.md "wikilink")。多くの製品は、[組み込みアプリケーション向けの](../Page/組み込みシステム.md "wikilink")、個別に設計された[SoCである](https://ja.wikipedia.org/wiki/System-on-a-chip "wikilink")。

PowerQUICCプロセッサーは、ネットワーク、自動車、産業用、ストレージデバイス、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")、コンシューマ製品で利用されている。フリースケールは、[mobileGT](https://ja.wikipedia.org/wiki/mobileGT "wikilink")プラットフォームの一部として、PowerQUICCプロセッサを使用している。

フリースケールは、古い[68kの技術に基づいた](../Page/MC68000.md "wikilink")、[QUICC](https://ja.wikipedia.org/wiki/QUICC "wikilink")マイクロコントローラも製造している。

## PowerQUICCシリーズ

PowerQUICCには、主に処理能力で分けられた4つのシリーズがある。

### PowerQUICC I

[thumbの](https://ja.wikipedia.org/wiki/ファイル:XPC855TZP66D4_3K20A.jpg "wikilink")[Fire V20zに搭載されたフリースケールXPC](https://ja.wikipedia.org/wiki/Sun_Fire "wikilink")855Tサービスプロセッサ\]\] **MPC8xx**シリーズは、[モトローラ](../Page/モトローラ.md "wikilink")製の最初の[PowerPC](../Page/PowerPC.md "wikilink")ベースの組み込みプロセッサであり、[ネットワークプロセッサ](https://ja.wikipedia.org/wiki/ネットワークプロセッサ "wikilink")と[SoCデバイスに適していた](https://ja.wikipedia.org/wiki/System-on-a-chip "wikilink")。コアはPowerPC仕様の最初の実装の一つであった。MPC8xxは一つの4ステージパイプライン、MMU、分岐予測ユニットを搭載したコアであり、最大133 MHzで動作した。MPC821は、完全なQUICC Engineを搭載したMPC860と共に、1995年に発売された。キャッシュとIOポートを減らし、スリム化したバージョンのMPC850は1997年に発売された。QUICC通信プロセッサモジュール (Communications Processor Module, CPM) は、CPUからネットワークタスクの負荷を低減した。こうして、このシリーズにはPowerQUICCという商標が与えられた。このシリーズのプロセッサは、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")、シリアル、PCMCIA、ATM、イーサーネットコントローラのようなオンチップデバイスの搭載や、 1[KiBから](https://ja.wikipedia.org/wiki/キビバイト "wikilink")16KiBの範囲に渡るL1キャッシュサイズのバリエーションがある。

**MPC8xx** - 全てのPowerQUICCプロセッサは、この形式の名前を持っている。

  - MPC821 - 組み込み用として最初のPowerPCプロセッサであり、CPMを搭載していたが、FPUは搭載していなかった。最大50 MHzで動作した。
  - MPC860 - 完全なQUICC Engineを統合した最初のPowerPCであり、最大80 MHzで動作した。
  - MPC850 - MCP860からUSBと[イーサーネット](https://ja.wikipedia.org/wiki/イーサーネット "wikilink")を削除した低価格販。最大50 MHzで動作した。

### PowerQUICC II

[thumb](https://ja.wikipedia.org/wiki/ファイル:MPC8245.jpg "wikilink") SANbox 5200 [ファイバーチャネル](https://ja.wikipedia.org/wiki/ファイバーチャネル "wikilink")スイッチに搭載されたMPC8245\]\] **PowerQUICC II**は、[PowerPC 603eの直接の後継機であり](../Page/PowerPC_603.md "wikilink")、1998年に発売された。同じコアが**603e**や**G2**という名前でも使用された。PowerQUICC IIは16/16 KiBのL1インストラクション／データキャッシュを持ち、動作周波数は450MHzに達した。これらの通信プロセッサは、[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")システム、[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")、[フェムトセル](../Page/フェムトセル.md "wikilink")、[DSLAM](../Page/DSLAM.md "wikilink")、のようなアプリケーションで利用された。PowerQUICC II シリーズは、より強力なPowerQUICC II Proシリーズが導入されたため、徐々に縮小している。このコアに関する今後の開発は計画されていない。

**MPC82xx** - 全てのPowerQUICC IIプロセッサは、この形式の名前を持っている。

### PowerQUICC II Pro

2004年に[PowerPC 603eコアを](../Page/PowerPC_603.md "wikilink")32/32 KiBのL1インストラクション／データキャッシュで強化した[e300コアに基づいた](https://ja.wikipedia.org/wiki/PowerPC_e300 "wikilink")、**PowerQUICC II Pro**が発表された。PowerQUICC II Proは、[ルーター](../Page/ルーター.md "wikilink")、[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")、プリンター、[ネットワークアタッチトストレージ](../Page/ネットワークアタッチトストレージ.md "wikilink")、[無線LANアクセスポイント](../Page/アクセスポイント_\(無線LAN\).md "wikilink")、[DSLAM](../Page/DSLAM.md "wikilink")向けの[ネットワーキング・プロセッサ](https://ja.wikipedia.org/wiki/ネットワーキング・プロセッサ "wikilink")として使用された。PowerQUICC II Proは最大677MHzで動作し、USB、[PCI](../Page/Peripheral_Component_Interconnect.md "wikilink")、イーサネット、セキュリティ機能など、多数の組み込みシステム向けの機能を内蔵することができた。PowerQUICC II Proは、オリジナルのPowerQUICC IやPowerQUICC IIシリーズでに搭載されたCPMとは異なる、新しいネットワーク負荷軽減エンジンのQUICC Engineを内蔵した。

**MPC83xx** - 全てのPowerQUICC II Proプロセッサは、この形式の名前を持っている。名前の末尾の"E"は、プロッセッサが暗号化モジュールを内蔵していることを示す。834xの名前を持つプロセッサは、QUICC Engineを内蔵していないが、836xの名前を持つものは内蔵している。

  - MPC8321E - MPC8xxファミリからの移行を容易にするローエンド
  - MPC8343E - "[Killer NIC](https://ja.wikipedia.org/wiki/Killer_NIC "wikilink")" [ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")で使用された。
  - MPC8347E
  - MPC8349E - ACK Systemsが製造した[Amiga](../Page/Amiga.md "wikilink")クローンで使用された。[1](http://www.extremetech.com/article2/0,1558,2124107,00.asp)
  - MPC8358E
  - MPC8360E

### PowerQUICC III

**PowerQUICC III**プロセッサは、32ビットの[Power命令セットv.2.03](https://ja.wikipedia.org/wiki/Power命令セットv.2.03 "wikilink")に対応した[e500と呼ばれるコアに基づき](https://ja.wikipedia.org/wiki/PowerPC_e500 "wikilink")、2003年に発表された。PowerQUICC IIIは、2並列の7ステージパイプライン、倍精度のFPU、32/32 KiB のL1インストラクション／データキャッシュを持ち、複数の[ギガビット・イーサネット](https://ja.wikipedia.org/wiki/ギガビット・イーサネット "wikilink")、PCIと[PCIe](https://ja.wikipedia.org/wiki/PCI_Express "wikilink")、[RapidIO](https://ja.wikipedia.org/wiki/RapidIO "wikilink")、DDR/DDR2メモリコントローラ、セキュリティアクセラレータを持っていた。動作周波数は533 MHzから1.5 GHzまでの範囲であった。PowerQUICC IIIは、企業向けのネットワーキングと通信アプリケーション、ハイエンドのストレージ・プリンター・イメージングをターゲットにしていた。一部のプロセッサは、ネットワーク処理の負荷軽減のために古いCPMモジュールを内蔵していた。新しいQUICC Engine（PowerQUICC II Proと同じもの）を内蔵したものも、CPMやQUICC Engineを全く内蔵しないものもあった。しかし、フリースケールのマーケティング部門は、85xxシリーズの全てのプロセッサに"PowerQUICC III"のブランド名をつけた。

**MPC85xx** - 全てのPowerQUICC IIIプロセッサは、この形式の名前を持っている。名前の末尾の"E"は、プロッセッサが暗号化モジュールを内蔵していることを示す。

  - MPC8540 - 世界初の[RapidIO](https://ja.wikipedia.org/wiki/RapidIO "wikilink")対応ホストプロセッサ。2つのギガビット・イーサネットコントローラを内蔵し、ルータの用途に適している。動作周波数は600 MHzから1 GHzである。
  - MPC8548/47/43/41(E) - 1つのe500コアとPCI Express、RapidIOを統合したプロセッサのシリーズ。数字が小さいものは、数字が大きいものよりも低い能力である。
  - MPC8544 - コストを抑えるために90 nmプロセスで作られたが、8548と同等の機能を持つ。
  - MPC8560 - 8540と同時に出荷された、最初のPowerQUICC IIIプロセッサである。e500コアとCPMを内蔵していた。
  - MPC8568/68E/67/67E - CPMの代わりにQUICC Engineを内蔵。8567は周辺ユニットの一部が削除されている。
  - MPC8572E - 最大1.5 GHzのe500コアを2個内蔵。[ファイアウォール](../Page/ファイアウォール.md "wikilink")や[アンチウイルスソフトウェア](https://ja.wikipedia.org/wiki/アンチウイルスソフトウェア "wikilink")（[カスペルスキー・ラボ](https://ja.wikipedia.org/wiki/カスペルスキー・ラボ "wikilink")による）のようなハイエンドアプリケーションのネットワーク装置で使われた。
  - MPC8574 and MPC8578 - [3G](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")、[WiMAX](https://ja.wikipedia.org/wiki/WiMAX "wikilink")基地局向けの、4コアまたは8コアのプロセッサである。2008年に[SOI](https://ja.wikipedia.org/wiki/SOI "wikilink")プロセスで製造された。[2](http://www.electronicsweekly.com/Articles/2007/10/17/42400/freescale+jumps+to+45nm+with+embedded+powerpc.htm)

## 将来

シングルコアから32コアまでのマルチコアの[PowerPC e500ベースのプロセッサの全ての特徴を持ち](https://ja.wikipedia.org/wiki/PowerPC_e500 "wikilink")、ソフトウェア互換の[QorIQ](https://ja.wikipedia.org/wiki/QorIQ "wikilink")プラットフォームに移行し、PowerQUICCの開発は終了する。フリースケールは、既存の顧客向けにPowerQUICCプロセッサの製造を継続するが、QorIQへの移行を容易にする手助けをしている。

## 関連項目

  - [PowerPC](../Page/PowerPC.md "wikilink")
  - [PowerPC 603](../Page/PowerPC_603.md "wikilink")
  - [PowerPC e300](https://ja.wikipedia.org/wiki/PowerPC_e300 "wikilink")
  - [PowerPC e500](https://ja.wikipedia.org/wiki/PowerPC_e500 "wikilink")
  - [QorIQ](https://ja.wikipedia.org/wiki/QorIQ "wikilink")

## 参照

  - [フリースケールのPowerアーキテクチャ ポートフォリオ](http://www.freescale.com/files/32bit/doc/brochure/BRPOWERPCQUKRG.pdf)
  - [フリースケールのPowerアーキテクチャ ホワイトペーパー - "From Somerset to SoC"](http://www.freescale.com/files/32bit/doc/white_paper/PPCCORESWP.pdf)

## 外部リンク

  - [フリースケールのPowerQUICCサイト](http://www.freescale.com/powerquicc)

[Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink")