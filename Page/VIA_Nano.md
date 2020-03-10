> この記事は[VIA Nano](https://ja.wikipedia.org/wiki/VIA_Nano)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/画像:VIA_Nano_Chip_Image_\(perspective\).jpg "wikilink") **VIA Nano**(ヴィア ナノ)は、[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")[VIA Technologiesが販売するCPUの名称である](../Page/VIA_Technologies.md "wikilink")。

## 概要

**VIA Nano**はVIAが2008年5月に発表したCPU製品である。従来の同社CPU製品同様にVIA傘下の[セントールテクノロジー](https://ja.wikipedia.org/wiki/セントールテクノロジー "wikilink")により設計された。開発コードネームはIsaiah (VIA) またはCNA/CNB/CNC/CNQ (Centaur)。

[VIA C7の後継製品とされ](../Page/VIA_C7.md "wikilink")、VIA製x86互換CPUとして初めて[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")および[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")を搭載する他、拡張命令として[SSE3命令](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE3 "wikilink")・[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")互換命令などがフルサポートがされた。これにより前モデルであるC7から大幅に性能の向上がされているが、CNA/CNB/CNCにおいては[ハードウェアマルチスレッディング](../Page/ハードウェアマルチスレッディング.md "wikilink")や[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")といった並列化技術は搭載していない。

[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")は後にCNQコアにおいて搭載された、これはVIAのCPUが[マルチコア](https://ja.wikipedia.org/wiki/マルチコア "wikilink")化された初めての例である。

また[AES](../Page/Advanced_Encryption_Standard.md "wikilink")[暗号化](https://ja.wikipedia.org/wiki/暗号化 "wikilink")エンジン[PadLock](https://ja.wikipedia.org/wiki/PadLock "wikilink")によるハードウェア暗号化アクセラレーションをサポートする。

省電力技術**Adaptive PowerSaver**による高度な省電力制御が可能であり、アイドル時の消費電力は100～200mWとなっている。(最上位のL2100のみ500mW)

[富士通](../Page/富士通.md "wikilink")の65nmプロセスルール(Nano 1000～3000シリーズ)と[TSMC](https://ja.wikipedia.org/wiki/TSMC "wikilink")の40nmプロセスルール (Nano X2/VIA QuadCore) により製造がされ、パッケージングはオンボード用の**NanoBGA2**のみで提供される。VIA NanoのパッケージはVIA C7とピン互換性があり、C7対応にデザインされたシステムであれば容易に置換えが可能となっている。

2009年11月、VIAはマイナーチェンジとなる**VIA Nano 3000 (CNC)** シリーズを発表した。これは従来のNanoプロセッサーに対し、20%低い消費電力で20%高い性能を実現したとされている。またCPU仮想化および**SSE4**命令への対応といった新機能も搭載している。Nano 3000シリーズの発表に伴い、従来モデルはNano 1000 (CNA)/2000シリーズ (CNB) と表記されている。

2011年1月、VIA Nano 3000をベースとしたデュアルコアCPU**VIA Nano X2 (CNQ)** シリーズを発表した。

CentaurのコードネームがCNDではなくCNQになっているのはもともとQuadCore化を前提に設計されたためである\[1\]

同年5月にはNano X2をベースにしたクアッドコアCPUである**VIA QuadCore**シリーズを発表した。

これは同じダイ (CNQ) を基板上に2つ搭載する手法 ([Multi-Chip Module](https://ja.wikipedia.org/wiki/Multi-Chip_Module "wikilink")) でクアッドコアを実現したCPUであり同じ手法を利用したCPUとしては[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[Pentium Dや](https://ja.wikipedia.org/wiki/Pentium_D "wikilink")[Core2](https://ja.wikipedia.org/wiki/Core2 "wikilink") Quadなどが知られている。

また、VIA Nanoプロセッサーには消費電力や発熱に応じてクロックを引き上げる自動オーバークロック機能を備えており、シングルスレッド時の性能を引き上げることが可能となっている。

## 主な仕様

  - パッケージサイズ：21mm x 21mm
  - ダイサイズ：7.650mm x 8.275mm（63.3平方mm）
  - プロセスルール：65nm（Nano 1000～3000シリーズ）/40nm（Nano X2シリーズ及びNano QuadCoreシリーズ）
  - パッケージ形式：NanoBGA2
  - 動作クロック：0.8～2.0GHz
  - FSB：VIA V4 1333/1066/800MHz/533MHz

<!-- end list -->

  - L2キャッシュ：4/2/1MB (16-way set associative)
  - 対応チップセット:CN896+VT8237S/VX900/VX900H/VN1000/VX11

## 主なラインナップ

VIA Nanoの製品ラインナップは メインストリーム[デスクトップ](https://ja.wikipedia.org/wiki/デスクトップ "wikilink")/[ノートPC](https://ja.wikipedia.org/wiki/ノートPC "wikilink")向けの**Lシリーズ**と、 SFFデスクトップ/[UMPC](https://ja.wikipedia.org/wiki/UMPC "wikilink")向けの**Uシリーズ**及び組み込み向けの**Eシリーズ**に大別される。

また、ファンレス駆動が可能なCPUはEDENシリーズとしてモデルナンバーが付されているがここではIsaiahコアのEDENも合わせて表記する。

### デスクトップ・ノートPC向け

VIA Nano 2000 シリーズ

  - サポート命令セット: [MMX](https://ja.wikipedia.org/wiki/MMX "wikilink")、[SSE](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令 "wikilink")、[SSE2](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE2 "wikilink")、[SSE3](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE3 "wikilink")、[SSSE3](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSSE3 "wikilink")、[x86-64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")、[VIA VT virtualization](https://ja.wikipedia.org/wiki/VIA_VT_virtualization "wikilink") (stepping 3 and higher)、[VIA PadLock](https://ja.wikipedia.org/wiki/VIA_PadLock "wikilink") (SHA, AES, RNG)、[VIA PowerSaver](https://ja.wikipedia.org/wiki/PowerSaver "wikilink")
  - プロセスルール:65nm

| モデルナンバー    | クロックスピード | L1キャッシュ  | L2キャッシュ | FSBスピード | Clock Multiplier | TDP  | アイドル時の消費電力 | Socket   | Core数 | 発表日時         | Part Number(s) |
| ---------- | -------- | -------- | ------- | ------- | ---------------- | ---- | ---------- | -------- | ----- | ------------ | -------------- |
| Nano L2200 | 1.6 GHz  | 16+16 KB | 1024 KB | 800 MHz | 8×               | 17 W | 200 mW     | NanoBGA2 | 1     | May 29, 2008 |                |
| Nano L2207 | 1.6 GHz  | 16+16 KB | 1024 KB | 800 MHz | 8×               | 17 W | 200 mW     | NanoBGA2 | 1     | \-           |                |
| Nano L2007 | 1.6 GHz  | 16+16 KB | 1024 KB | 800 MHz | 8×               | 25 W | 500 mW     | NanoBGA2 | 1     | \-           |                |
| Nano L2100 | 1.8 GHz  | 16+16 KB | 1024 KB | 800 MHz | 9×               | 25 W | 500 mW     | NanoBGA2 | 1     | May 29, 2008 |                |
| Nano L2107 | 1.8 GHz  | 16+16 KB | 1024 KB | 800 MHz | 9×               | 25 W | 500 mW     | NanoBGA2 | 1     | \-           |                |

VIA Nano 3000 シリーズ

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、[SSE4.1](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#SSE4.1 "wikilink")、x86-64、NXビット、VIA VT virtualization、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver
  - プロセスルール:65nm

| モデルナンバー    | クロックスピード | L1キャッシュ  | L2キャッシュ | FSBスピード | Clock Multiplier | TDP | アイドル時の消費電力 | Socket   | Core数 | 発表日時             | Part Number(s) |
| ---------- | -------- | -------- | ------- | ------- | ---------------- | --- | ---------- | -------- | ----- | ---------------- | -------------- |
| Nano L3600 | 2 GHz    | 16+16 KB | 512 KB  | 800 MHz | 10×              | \-  | 500 mW     | NanoBGA2 | 1     | November 3, 2009 |                |
| Nano L3100 | 2 GHz    | 16+16 KB | 512 KB  | 800 MHz | 10×              | 25W | 500 mW     | NanoBGA2 | 1     | November 3, 2009 |                |
| Nano L3050 | 1.8 GHz  | 16+16 KB | 512 KB  | 800 MHz | 9×               | 25W | 500 mW     | NanoBGA2 | 1     | November 3, 2009 |                |
| Nano L3025 | 1.6 GHz  | 16+16 KB | 512 KB  | 800 MHz | 8×               | \-  | 500 mW     | NanoBGA2 | 1     | November 3, 2009 |                |
|            |          |          |         |         |                  |     |            |          |       |                  |                |

VIA Nano Dual Coreシリーズ \[2\]\[3\]

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、SSE4.1、x86-64、NXビット、VIA VT virtualization、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver
  - プロセスルール:40nm

| モデルナンバー | クロックスピード | ターボ時クロック | L1キャッシュ  | L2キャッシュ | FSBスピード  | TDP    | Socket   | Core数 | 発表日時        | Part Number(s) |
| ------- | -------- | -------- | -------- | ------- | -------- | ------ | -------- | ----- | ----------- | -------------- |
| L4350   | 1.6 GHz  | 1.73Ghz  | 64+64 KB | 1 MB    | 1066 MHz | 27.5 W | NanoBGA2 | 2     | May 5, 2011 |                |
| L4050   | 1.4 GHz  | \-       | 64+64 KB | 1 MB    | 1066 MHz | 19 W   | NanoBGA2 | 2     | May 5, 2011 |                |

### 超低電圧CPU(SFFデスクトップ/UMPC向け)

VIA Nano 1000/2000 シリーズ

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、x86-64、NXビット、VIA VT virtualization (stepping 3 and higher)、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver

| モデルナンバー    | クロックスピード | ターボ時クロック | L1キャッシュ  | L2キャッシュ | FSBスピード | Clock Multiplier | TDP   | アイドル時の消費電力 | Socket   | Core数 | 発表日時         | Part Number(s) |
| ---------- | -------- | -------- | -------- | ------- | ------- | ---------------- | ----- | ---------- | -------- | ----- | ------------ | -------------- |
| Nano U1700 | 1.0 GHz  | 1.3 GHz  | 16+16 KB | 256 KB  | 800 MHz | 10\~13×          | 5 W   | 200 mW     | NanoBGA2 | 1     | May 29, 2008 |                |
| Nano U2300 | 1.0 GHz  |          | 16+16 KB | 256 KB  | 533 MHz | 7.5×             | 5 W   | 100 mW     | NanoBGA2 | 1     | May 29, 2008 |                |
| Nano U2225 | 1.3 GHz  |          | 16+16 KB | 256 KB  | 800 MHz | 13×              | 8 W   | 200 mW     | NanoBGA2 | 1     | May 29, 2008 |                |
| Nano U2250 | 1.3 GHz  | 1.6 GHz  | 16+16 KB | 256 KB  | 800 MHz | 13\~16×          | 8 W   | 200 mW     | NanoBGA2 | 1     | May 29, 2008 |                |
| Nano U2500 | 1.2 GHz  |          | 16+16 KB | 256 KB  | 800 MHz | 12×              | 6.8 W | 100 mW     | NanoBGA2 | 1     | May 29, 2008 |                |

VIA Nano 3000シリーズ \[4\]\[5\]

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、x86-64、NXビット、VIA VT virtualization、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver
  - プロセスルール：65nm

| モデルナンバー    | クロックスピード | ターボ時クロック | L1キャッシュ  | L2キャッシュ | FSBスピード | Clock Multiplier | TDP   | アイドル時の消費電力 | Socket   | Core数 | 発表日時           | Part Number(s) |
| ---------- | -------- | -------- | -------- | ------- | ------- | ---------------- | ----- | ---------- | -------- | ----- | -------------- | -------------- |
| Nano U3100 | 1.3 GHz  | 1.6 GHz  | 64+64 KB | 1 MB    | 800 MHz | 13\~16x          | 9 W   | 100 mW     | NanoBGA2 | 1     | April 22, 2010 |                |
| Nano U3300 | 1.2 GHz  |          | 64+64 KB | 1 MB    | 800 MHz | 12×              | 6.8 W | 100 mW     | NanoBGA2 | 1     | April 22, 2010 |                |
| Nano U3500 | 1.0 GHz  |          | 64+64 KB | 1 MB    | 800 MHz | 10×              | 5 W   | 100 mW     | NanoBGA2 | 1     | April 22, 2010 |                |
| Nano U3400 | 0.8 GHz  |          | 64+64 KB | 1 MB    | 800 MHz | 8x               | 3.5 W | 100 mW     | NanoBGA2 | 1     | April 22, 2010 |                |

VIA Nano DualCoreシリーズ \[6\]\[7\]

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、SSE4.1、x86-64、NXビット、VIA VT virtualization、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver
  - プロセスルール:40nm

| モデルナンバー | クロックスピード | ターボ時クロック | L1キャッシュ  | L2キャッシュ | FSBスピード | TDP  | Socket   | Core数 | 発表日時        |
| ------- | -------- | -------- | -------- | ------- | ------- | ---- | -------- | ----- | ----------- |
| U4300   | 1.2+ GHz | 1.46 GHz | 64+64 KB | 2 MB    | 1066MHz | 13 W | NanoBGA2 | 2     | May 5, 2011 |
| U4025   | 1.2 GHz  | \-       | 64+64 KB | 4 MB    | 1066MHz | 18 W | NanoBGA2 | 2     | May 5, 2011 |

VIA QuadCoreシリーズ \[8\]\[9\]\[10\]

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、SSE4.1、x86-64\]、NXビット、VIA VT virtualization、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver
  - プロセスルール:40nm
  - [Multi-chip module](https://ja.wikipedia.org/wiki/Multi-chip_module "wikilink")

| モデルナンバー | クロックスピード | ターボ時クロック | L1キャッシュ     | L2キャッシュ | FSBスピード  | TDP  | Socket   | Core数 | 発表日時        |
| ------- | -------- | -------- | ----------- | ------- | -------- | ---- | -------- | ----- | ----------- |
| L4650   | 1.0+ GHz | 1.2 GHz  | 64 KB /core | 4 MB    | 1333 MHz | 18 W | NanoBGA2 | 4     | May 5, 2011 |

### 組み込み向け

VIA Nano DualCoreシリーズ \[11\]\[12\]

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、SSE4.1、x86-64、NXビット、VIA VT virtualization、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver
  - プロセスルール:40nm

| シリーズネーム   | モデルナンバー | クロックスピード | ターボ時クロック | L1キャッシュ  | L2キャッシュ | FSBスピード  | TDP    | Socket   | Core数 | 発表日時        |
| --------- | ------- | -------- | -------- | -------- | ------- | -------- | ------ | -------- | ----- | ----------- |
| Nano X2 E | L4350E  | 1.6 GHz  | 1.73Ghz  | 64+64 KB | 1 MB    | 1066 MHz | 27.5 W | NanoBGA2 | 2     | May 5, 2011 |
| Nano X2 E | L4300E  | 1.2 GHz  | \-       | 64+64 KB | 1 MB    | 1066 MHz | 13 W   | NanoBGA2 | 2     | May 5, 2011 |
| Eden X2   | L4200E  | 1.0 GHz  | \-       | 64+64 KB | 1 MB    | 800 MHz  | 9 W    | NanoBGA2 | 2     | May 5, 2011 |
| Eden X2   | L4100E  | 0.8 GHz  | \-       | 64+64 KB | 1 MB    | 533 MHz  | 6 W    | NanoBGA2 | 2     | May 5, 2011 |

VIA QuadCore Processor \[13\]\[14\]\[15\]

  - サポート命令セット: MMX、SSE、SSE2、SSE3、SSSE3、SSE4.1、x86-64、NXビット、VIA VT virtualization、VIA PadLock (SHA, AES, RNG)、VIA PowerSaver
  - プロセスルール:40nm
  - [Multi-chip module](https://ja.wikipedia.org/wiki/Multi-chip_module "wikilink")

| モデルナンバー | クロックスピード      | ターボ時クロック | L1キャッシュ      | L2キャッシュ | FSBスピード  | TDP    | Socket   | Core数 | 発表日時        |
| ------- | ------------- | -------- | ------------ | ------- | -------- | ------ | -------- | ----- | ----------- |
| L4700E  | 1.2+ GHz      | 1.46 GHz | 64 KB / core | 4 MB    | 1333 MHz | 27.5 W | NanoBGA2 | 4     | May 5, 2011 |
| L4650E  | 1.0+ GHz(ULV) | 1.2 GHz  | 64 KB /core  | 4 MB    | 1333 MHz | 18 W   | NanoBGA2 | 4     | May 5, 2011 |

VIAの公式ウェブサイトにおいて、VIA Nano L2200 (1.6GHz) と[Intel Atom](https://ja.wikipedia.org/wiki/Intel_Atom "wikilink") N270 (1.6GHz) と比較したベンチマークにおいて、PCMark 05で20％、3DMark2006で29％上回っていることが示されている。\[16\]

またVIAの公式ウェブサイトにおいて、VIA Nano X2 U4300(1.2GHz+)と[Intel Atom](https://ja.wikipedia.org/wiki/Intel_Atom "wikilink") D525(1.8GHz)と比較したベンチマークにおいて、50%高いベースクロックによって駆動するAtom Dシリーズに対し、VIA Nano X2が40%～35％程高いスコアを出していると公開し\[17\]、共に1ワット当たりの性能がAtomより高いことを主張している。

VIA QuadCoreの発表会場で公開されたベンチマーク結果によると[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink")E-350に比べ高い性能を発揮するとされている\[18\]。

## ロードマップ

2014年7月にVIAグループのCPU開発会社であるCentaurTechnologyからVIA Nanoの後継CPUであるIsaiah IIのベンチマークが発表された。

## 主な採用例

VIA NanoはVIA C7同様にコンシューマ向けの単体販売はされておらず、主にVIA社製の産業向けシステムボードに搭載される形で販売されている。

[Intel Atom同様に](https://ja.wikipedia.org/wiki/Intel_Atom "wikilink")[ネットブック](https://ja.wikipedia.org/wiki/ネットブック "wikilink")用CPUとも目されており、[韓国](https://ja.wikipedia.org/wiki/韓国 "wikilink")[サムスン](https://ja.wikipedia.org/wiki/サムスン "wikilink")および[中国](../Page/中華人民共和国.md "wikilink")[レノボ](https://ja.wikipedia.org/wiki/レノボ "wikilink")がそれぞれNano U2250を搭載したNC20、Idea Pad S12を発売している他、[台湾および](https://ja.wikipedia.org/wiki/中華民国 "wikilink")[中国の小規模メーカーに採用されている](../Page/中華人民共和国.md "wikilink")。また[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")のメジャーメーカーでは、[日立製作所](../Page/日立製作所.md "wikilink")のシンクライアントに採用された例がある\[19\]。

[デル](../Page/デル.md "wikilink")はVIA Nanoを採用したサーバ製品**XS11-VX8**を発表した。これはVIA社製CPUがデルに採用された初の例であると同時に、VIA社製CPUが大手サーバベンダーのサーバ製品に採用された初の例でもある。

[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")はThinclientにVIA製CPUを多く採用しておりNano搭載Thinclientとしてt5570 Thin Clientを発売している。

[ZOTAC](https://ja.wikipedia.org/wiki/ZOTAC "wikilink")はVIA Nano X2を採用したベアボーンキットZBOXNANO- VD01を発売している。これは日本において一般向けに販売されているPCに初めてNano X2を搭載した例である。

## 参考文献

  - [VIA Nano ホワイトペーパー](http://www.viatech.co.jp/jp/downloads/whitepapers/processors/WP080529VIA_Nano.pdf)

## 脚注

<div class="references-small">

<references/>

</div>

## 外部リンク

  - [VIA Nano](http://www.viatech.co.jp/jp/products/processors/nano/)
  - [VIA Global Mobility Bazaar Alliance](http://gmb.viatech.com/resource/jsp/AboutGMB/GMB-aboutVIA.jsp)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")

1.
2.  <http://www.via.com.tw/en/resources/pressroom/pressrelease.jsp?press_release_no=5467>
3.  <http://www.viaembedded.com/servlet/downloadSvl?id=1373&download_file_id=13043>
4.  <http://www.via.com.tw/en/resources/pressroom/pressrelease.jsp?press_release_no=4767>
5.  <http://www.viaembedded.com/servlet/downloadSvl?id=1370&download_file_id=13044>
6.  <http://www.via.com.tw/en/resources/pressroom/pressrelease.jsp?press_release_no=5467>
7.  <http://www.viaembedded.com/servlet/downloadSvl?id=1373&download_file_id=13043>
8.  <http://www.via.com.tw/en/resources/pressroom/pressrelease.jsp?press_release_no=6127>
9.  <http://www.via.com.tw/en/products/processors/quadcore/index.jsp>
10. <http://www.viaembedded.com/en/products/processors/1830/1/VIA_QuadCore_E-Series.html>
11. <http://www.via.com.tw/en/resources/pressroom/pressrelease.jsp?press_release_no=5467>
12. <http://www.viaembedded.com/servlet/downloadSvl?id=1373&download_file_id=13043>
13. <http://www.via.com.tw/en/resources/pressroom/pressrelease.jsp?press_release_no=6127>
14. <http://www.via.com.tw/en/products/processors/quadcore/index.jsp>
15. <http://www.viaembedded.com/en/products/processors/1830/1/VIA_QuadCore_E-Series.html>
16.
17.
18.
19.