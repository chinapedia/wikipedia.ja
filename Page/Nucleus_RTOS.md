> この記事は[Nucleus RTOS](https://ja.wikipedia.org/wiki/Nucleus_RTOS)から翻訳されています。


**Nucleus RTOS**（ニュークリアス アールティーオーエス） は、[米国のソフトウェア企業](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")、[メンター・グラフィックス](https://ja.wikipedia.org/wiki/メンター・グラフィックス "wikilink")の[組み込みシステム](../Page/組み込みシステム.md "wikilink")部門が各種CPUプラットフォーム向けに開発した[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink") (RTOS) とツール群である。組み込み用ミドルウェアを含む組み込みソリューションの一部となっている。

開発は Windows または Linux が動作するホストマシンで行われるのが一般的である。各種対象[CPU](../Page/CPU.md "wikilink")アーキテクチャ上で動作するよう[クロスコンパイルでき](../Page/クロスコンパイラ.md "wikilink")、EDGE SimTest 経由で実際の基板やシミュレータを使ってテストする。

Nucleus RTOS は、家電機器、[セットトップボックス](https://ja.wikipedia.org/wiki/セットトップボックス "wikilink")、[携帯電話](../Page/携帯電話.md "wikilink")、その他の携帯機器などの組み込み向けに設計されている。コードとデータを含めて、最低13KBで動作可能である。このメモリ使用量の少なさが重要な長所となっている。

## コンポーネント

  - カーネル

:\* リアルタイム・カーネル

:\* [C++](../Page/C++.md "wikilink")および[POSIX](../Page/POSIX.md "wikilink")インタフェース

:\* 動的ダウンロード

:\* プロセッサ間通信

:\* クローズドソース（ただし、購入すればソースコードを入手でき、完全にクローズドなOSよりもデバッグが容易である）

:\* ロイヤリティフリー

  - 入出力

:\* [USB 2.0](../Page/ユニバーサル・シリアル・バス.md "wikilink") ホスト

:\* Function スタックおよび [On-The-Go](../Page/USB_On-The-Go.md "wikilink") (OTG) スタック

:\* クラスドライバ

:\* マルチメディア転送（[MTPと](https://ja.wikipedia.org/wiki/Media_Transfer_Protocol "wikilink")[PictBridge](https://ja.wikipedia.org/wiki/PictBridge "wikilink")）

:\* [PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") と [PCI-X](../Page/PCI-X.md "wikilink")

:\* [CAN](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink") と [CANopen](https://ja.wikipedia.org/wiki/CANopen "wikilink")

  - ネットワーク
    60以上のネットワークドライバとプロトコルを用意（[TCP/IP スタック](../Page/インターネット・プロトコル・スイート.md "wikilink")、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")、[IEEE 802.11](https://ja.wikipedia.org/wiki/IEEE_802.11 "wikilink") など）。

  - ファイルシステム

:\* [FAT](../Page/File_Allocation_Table.md "wikilink")

:\* [ISO 9660](../Page/ISO_9660.md "wikilink") [CD-ROM](../Page/CD-ROM.md "wikilink")

:\* [仮想ファイルシステム](https://ja.wikipedia.org/wiki/仮想ファイルシステム "wikilink") [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")

  - グラフィックス

:\* 低レベルレンダリング

:\* 完全なマルチウィンドウシステム

  - セキュリティ
    暗号化、ハッシュ、署名といったアルゴリズム、および鍵交換プロトコル。

## Nucleus RTOS を使っている製品

[メンター・グラフィックス](https://ja.wikipedia.org/wiki/メンター・グラフィックス "wikilink")は、世界中の1000以上の企業にこのソフトウェアを提供している。以下に挙げたものは Nucleus を使った製品のごく一部である。

  - [ハネウェル](https://ja.wikipedia.org/wiki/ハネウェル "wikilink")は航空分野における Critical Terrain Awareness Technology に Nucleus RTOS を使っている。
  - IVL Technologies の On-key Karaoke Handheld Player は Nucleus PLUS カーネルを使っている\[1\]。
  - [Logitech](https://ja.wikipedia.org/wiki/ロジクール "wikilink") Pocket Video（ポータブルデジタルビデオカメラ）
  - [SKテレコム](https://ja.wikipedia.org/wiki/SKテレコム "wikilink")は韓国初の[CDMA技術の商用化にあたって](../Page/符号分割多元接続.md "wikilink") Nucleus RTOS を使用した。
  - [NECアメリカの携帯電話](../Page/日本電気.md "wikilink") 535M
  - ASC の Multi-Service Family \[2\]
  - [テキサス・インスツルメンツ](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink")も組み込み機器の一部に Nucleus を使っている。
  - Telephonics は米空軍の C-130 アビオニクス近代化プログラムで Nucleus を使った。また、767 Tanker プログラムでの航空通信システムにも使っている\[3\]。
  - Garmin の航空用[GPS](../Page/グローバル・ポジショニング・システム.md "wikilink") CNX80\[4\]
  - モトローラ、サムスン、LG、シーメンス、NEC の携帯電話
  - Intellon [HomePlug](https://ja.wikipedia.org/wiki/HomePlug "wikilink") AV
  - Crestron Electronics の制御システムプロセッサ\[5\]
  - BSS Audio の Soundweb London シリーズ\[6\]
  - [Creative Zen](https://ja.wikipedia.org/wiki/Creative_Zen "wikilink") シリーズの後期モデル
  - [アップルの](../Page/アップル_\(企業\).md "wikilink") [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink") で使われている [Infineon](https://ja.wikipedia.org/wiki/インフィニオン・テクノロジーズ "wikilink") S-Gold2 ベースバンドチップ
  - Metrotech i5000 Utility Locating System\[7\]

## 競合オペレーティングシステム

  - [VxWorks](../Page/VxWorks.md "wikilink")
  - [Microsoft Windows CE](https://ja.wikipedia.org/wiki/Microsoft_Windows_CE "wikilink") - Nucleus RTOSと組み合わせて利用されることもある。
  - [QNX](https://ja.wikipedia.org/wiki/QNX "wikilink")
  - [LynxOS](../Page/LynxOS.md "wikilink")
  - [ITRON](../Page/TRONプロジェクト.md "wikilink") - ITRONはあくまでも仕様にすぎず、Nucleus RTOSに[μITRON](https://ja.wikipedia.org/wiki/μITRON "wikilink")仕様準拠のAPIを実装した「Nucleus μiPLUS」が利用されることも多く、両者は単純な競合関係とは言いがたい。
  - [μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")カーネルのOS

## 脚注

## 外部リンク

  - [Nucleus RTOS](http://www.mentor.com/products/embedded_software/nucleus_rtos/kernels/index.cfm)

[Category:リアルタイムオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:リアルタイムオペレーティングシステム "wikilink") [Category:組み込みオペレーティングシステム](https://ja.wikipedia.org/wiki/Category:組み込みオペレーティングシステム "wikilink")

1.  [IVL Technologies](http://www.ivl.com/)
2.  [ASC](http://www.nsgdata.com/asc/index.html)
3.  [Telephonics](http://www.telephonics.com/)
4.  [Garmin CNX 80](https://buy.garmin.com/shop/shop.do?pID=6441)
5.  [www.crestron.com](http://www.crestron.com)
6.  [www.soundweb-london.com](http://www.soundweb-london.com)
7.  [Metrotech](http://www.metrotech.com/)