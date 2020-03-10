> この記事は[XScale](https://ja.wikipedia.org/wiki/XScale)から翻訳されています。


**XScale**（エックススケール）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が実装した第五世代[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")の[RISC](../Page/RISC.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")であり、v5TE [ISAに基づいている](../Page/命令セット.md "wikilink")。

これは、[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[StrongARM](../Page/StrongARM.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")および[マイクロコントローラ](https://ja.wikipedia.org/wiki/マイクロコントローラ "wikilink")の後継であり、StrongARMはDECとの訴訟問題の和解案としてDECの半導体部門から購入した経緯がある。インテルはStrongARMを同社の古くなった[RISC](../Page/RISC.md "wikilink")プロセッサ([i860](../Page/Intel_i860.md "wikilink")、[i960](../Page/Intel_i960.md "wikilink"))の後継として使用した。

[2006年](../Page/2006年.md "wikilink")[6月27日](../Page/6月27日.md "wikilink")の[プレスリリース](../Page/プレスリリース.md "wikilink")でインテルは[マーベル・テクノロジー・グループ](https://ja.wikipedia.org/wiki/マーベル・テクノロジー・グループ "wikilink")（マーベル）にXScaleおよびその周辺チップ事業を6億ドルで譲渡する事を発表した。

## アーキテクチャ

全てのXScaleプロセッサは、32ビットARM v5TEアーキテクチャであり、32Kバイトのデータ[キャッシュと](../Page/キャッシュメモリ.md "wikilink")32Kバイトの命令キャッシュを装備している。これ以外に2Kバイトのミニデータキャッシュも装備している。第1世代、第2世代のプロセッサ・コアまでは0.18μmプロセスで製造され、第3世代のプロセッサ・コアは90nmプロセスに変更された。

2006年11月にインテルはすべてのPXAプロセッサ事業をマーベルへ譲渡した。しかし、IXPネットワークプロセッサ事業やIOPストレージプロセッサ事業はそのまま保有しているため、XScaleプロセッサ・コア技術を有する製品がマーベルとインテル両方から販売されているという変則的な状況が続いている。

## ファミリ

### インテル製

[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Typhoon_MyGuide_3500_mobile_-_controller_-_Intel_PXA255A0C300-1180.jpg "wikilink") XScaleプロセッサにはいくつかのファミリが存在する。アプリケーションプロセッサ (PXA) と3G携帯電話向けベースバンドプロセッサ (PXA)、I/Oプロセッサ (IOP)、ネットワークプロセッサ (IXP)、コントロール・プレーン・プロセッサ (IXC) である。 その他にスタンドアロンプロセッサとして80200と80219（PCIデバイス向け）がある。 2006年11月にPXAプロセッサ事業がマーベルへ譲渡された後は、マーベルからの販売サポートが継続されている。

以下はXScaleアプリケーションプロセッサを列挙したものである。

  - PXA210 (2002年2月)：エントリレベル向け、携帯電話などをターゲットとしている。動作周波数は133MHzと200MHz。
  - PXA250 (2002年2月)：動作周波数は 200MHz, 300MHz, 400MHz。
  - PXA255 (2003年3月)：バスクロックを倍に強化(100MHz→200MHz)。低電圧化(400MHzで1.3V)。
  - PXA260 (2003年3月)：パッケージを53%小型化。
  - PXA261 (2003年3月)：16ビット StrataFlashメモリ 16Mバイト内蔵
  - PXA262 (2003年3月)：16ビット StrataFlashメモリ 32Mバイト内蔵
  - PXA263 (2003年3月)：32ビット StrataFlashメモリ 32Mバイト内蔵
  - PXA270 (2004年4月)：動作周波数は 312MHz, 416MHz, 520MHz, 624MHz
  - PXA271 (2004年4月)：動作周波数は 312MHz, 416MHz。16ビット StrataFlashメモリ 32MB、16ビットSDRAM 32MB内蔵
  - PXA272 (2004年4月)：動作周波数は 312MHz, 416MHz, 520MHz。 32ビット StrataFlashメモリ 64MB内蔵

インテルはPXA27xファミリにいくつかの新技術を導入している。

  - ワイヤレス・スピードステップ：負荷に応じて自動的にクロックを落として電力消費を抑える。
  - ワイヤレス[MMX](../Page/MMX.md "wikilink")：43種の新しい[SIMD](../Page/SIMD.md "wikilink")命令([MMX](../Page/MMX.md "wikilink")[命令セット](../Page/命令セット.md "wikilink")とSSE命令とXScale独自命令)を追加。マルチメディアコンテンツのデコード、エンコードおよびゲームで使用。
  - 組み込み用グラフィックスコプロセッサ 2700G も同時にリリース。

以下はXScaleI/Oプロセッサを列挙したものである。

  - IOP321：PCI-X (64bit/133MHx)インターフェイス。最大で1GBのDDR200をサポート。動作周波数は400と600MHz。
  - IOP310：PCI (64bit/66MHz)インターフェイス。最大で512MBのPC100をサポート。動作周波数は 400MHzと600MHz。
  - IOP332：PCI-E to PCI-Xブリッジインターフェイス。最大で2GBのDDR333又は1GBまでのDDR400をサポート。動作周波数は500MHzと667MHzと800MHz。
  - IOP331：PCI-X (64bit/133MHz)ブリッジインターフェイス。最大で2GBのDDR333又は1GBまでのDDR400をサポート。動作周波数は500MHzと667MHzと800MHz。
  - IOP333：PCI-E to Dual PCI-Xブリッジインターフェイス。最大で2GBのDual-Ported DDR333又は1GBまでのDual-Ported DDR400をサポート。動作周波数は500MHzと667MHzと800MHz。
  - IOC340：PCI-E to PCI-Xインターフェイス。最大で4GBのDDR2 400/533をサポート。動作周波数は800MHzと1200MHz。
  - IOP341：PCI-E & PCI-Xインターフェイス。最大で4GBのDDR2 400/533をサポート。動作周波数は800MHzと1200MHz。
  - IOP342：PCI-E & PCI-Xインターフェイス。最大で4GBのDDR2 400/533をサポート。動作周波数は800MHzと1200MHz。
  - IOP348：PCI-E & PCI-Xインターフェイス。最大で4GBのDDR2 400/533をサポート。動作周波数は667MHzと800MHzと1200MHz。

### マーベル製

#### PXA3xxシリーズ

[Toradex_Colibri_XScale_Monahans_PXA290.jpg](https://ja.wikipedia.org/wiki/File:Toradex_Colibri_XScale_Monahans_PXA290.jpg "fig:Toradex_Colibri_XScale_Monahans_PXA290.jpg") 2005年8月、インテルは後継となるMonahans（コード名）を発表した。新開発の第三世代XScaleプロセッサ・コアを開発し、その上でSoCとしての周辺機能やデータ・スループットを大幅に改善した。当初はPXA29xシリーズとなる予定だったが、XScaleがマーベルに移った後、仕様変更を経て2006年11月にPXA3xx (PXA300/PXA310/PXA320) シリーズとして改めて製品発表が行われた。動作周波数は最大806MHz。性能向上は例えば624MHz同士で比較した場合、PXA270に比較して約25%だという。2005年8月時点では、2700Gの後継となる組み込み用グラフィックスコプロセッサ（コード名Stanwood）も発表しているが、2006年11月のPXA300シリーズ発表時点で発表はされなかった。 （写真はインテル時代のPXA290試作品の物であり、PXA3xxシリーズとは異なる。）

PXA300シリーズに採用された第三世代XScaleコアは、それまでのXScaleコアと同様ARM V5TE互換であることに変化はない。しかし、性能向上のための根本的な改良が加えられている。

  - PXA320では256KBのL2キャッシュが追加された。
  - 内部のローカルバスの本数を増やし、バススイッチという機能でデータ転送の多重化を行った。
  - ワイヤレスMMX系の命令セットを追加した。（ワイヤレスMMX2）
  - PXA320では最高806MHz、PXA310/300でも最高624MHzを仕様とした。
  - DRAMとして、DDR-SDRAMを標準対応とした。
  - NANDコントローラを内蔵し、システムブートをNANDからできるようにして、NORフラッシュメモリが不要になった。（NORメモリ対応品とNANDメモリ対応品の2種類が存在する。）

加えて、周辺機能としては、次のような特長がある。

  - PXA320ではVGA16ビットカラー対応のオンチップ・フレームメモリ(RAM)を内蔵 （LCDコントローラとしてはSVGA解像度までを標準でサポート）
  - 省電力機能を強化、ワイヤレス・スピードステップ2となった。
  - LCDコントローラに2Dグラフィック・アクセラレーション機能が追加された。
  - USB機能が強化。デバイス機能（クライアント）ではUSB2.0ハイスピード対応になった。（ホスト機能・OTGは1.1フルスピードのまま）
  - クイックカメラ・キャプチャ機能では、PXA310の場合最大500万画素まで対応する
  - PXA310では、MPEG2/4,H.264,JPEGなどのコーデック機能をハードウェアで内蔵することで、消費電力のピークを抑えるように考慮されている。

製品は以下の通り。

  - PXA300（2006年11月）:エントリレベル向けまたは低消費電力用途向け。16ビット外部バス。208MHz/624MHz。
    PXA310（2006年11月）:携帯電話や情報端末向け。16ビット外部バス。マルチメディア拡張機能内蔵。セキュリティ機能搭載。624MHzのみ。
    PXA320（2006年11月）:ハイエンド機器向け。32ビット外部バス。L2キャッシュ搭載、624MHz/806MHz。

#### PXA1xxシリーズ

  - PXA168（2009年 1月）:1GHzプロセッサ

## 使用例

**PXA2xxシリーズ：** IT通信機器関連では、国内外の携帯電話やスマートホン、携帯情報端末PDAなどで数多く使われている。有名なところではウィルコム[W-ZERO3](../Page/W-ZERO3.md "wikilink")シリーズ・[Windows Mobile機が知られている](../Page/Windows_Mobile.md "wikilink")。マルチメディア機器としては、ポータブル・ビデオ・プレイヤーに使われている。組み込み機器関連では、プロセッサ名が公表されないため情報が少ないが、マーベルのデモ展示などを参考にすると、ポータブル・ナビゲーション (PND) や、電子POP、ハンディ端末（ハンディPOSなど）を始め産業用組み込みプロセッサとしても使用されているようである。変わったところでは、近畿日本鉄道の運転支援装置として電車の運転台に設置された機器に搭載され、列車の運行を運転士に知らせる機器として使用されている。

  - PXA3xxシリーズ:IT通信機器関連では、発表後1年を経て国内外のスマートホンや[携帯情報端末](../Page/携帯情報端末.md "wikilink") (PDA) への搭載が確認されている。組み込み機器についてはプロセッサ名が公表されないため情報が少ないが、産業用組み込みプロセッサとしても既に使用されているようである。
    IXP4xxシリーズ:プロセッサ名が公表されることが少ないため情報が少ないが、国内外のブロードバンドルータに搭載されている。

また、IyonixというデスクトップコンピュータのCPUとしても使用されている。XScale IOP33xストレージI/Oプロセッサは[Xeon](../Page/Xeon.md "wikilink")ベースのサーバで使われている。

## 関連項目

  - [ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")
  - [Pocket PC](../Page/Pocket_PC.md "wikilink")
  - [アップル・ニュートン](../Page/アップル・ニュートン.md "wikilink")
  - [携帯情報端末](../Page/携帯情報端末.md "wikilink")
  - [スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")
  - [W-ZERO3](../Page/W-ZERO3.md "wikilink")
  - [ザウルス](../Page/ザウルス.md "wikilink")

## 外部リンク

  - [TRITON 270](http://www.karo-electronics.de/index.php?id=30&L=1)
  - [TRITON 320](http://www.karo-electronics.de/index.php?id=204&L=1)
  - [Colibri モジュール](http://www.toradex.com/Ja/Products/Colibri_XScale_Computer_Modules_Overview_PXA255_PXA270_PXA270M_PXA300_PXA310_PXA320_ARM)

[Category:ARMアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ARMアーキテクチャ "wikilink") [Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")