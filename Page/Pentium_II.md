> この記事は[Pentium II](https://ja.wikipedia.org/wiki/Pentium_II)から翻訳されています。


**Pentium II**（ペンティアム ツー）は、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")が[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")2月に発売した[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[アーキテクチャの](../Page/コンピュータ・アーキテクチャ.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")([CPU](../Page/CPU.md "wikilink"))である。

## 概要

Pentium IIという名称が付けられているが、内部構造は[Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")ではなく[Pentium Proがベースである](../Page/Pentium_Pro.md "wikilink")。Pentium Proで初めて採用された[P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")を引き続き採用したが、L1[キャッシュを倍増](../Page/キャッシュメモリ.md "wikilink")（L1命令キャッシュ8 KB→16 KB、L1データキャッシュ8 KB→16 KB）し、Pentium Proの弱点であった[16ビット](../Page/16ビット.md "wikilink")コードの処理速度を改善し、さらにPentiumでは拡張されたがPentium Proには無かった[MMX](../Page/MMX.md "wikilink")演算器を追加したものである。

Pentium ProではCPUパッケージ内にCPUコアと2次[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")がそれぞれ1枚ずつ封入されていた。この2次キャッシュに用いられていた[SRAMは](https://ja.wikipedia.org/wiki/スタティックランダムアクセスメモリ "wikilink")、[リフレッシュが不要](https://ja.wikipedia.org/wiki/Dynamic_Random_Access_Memory#リフレッシュ "wikilink")、且つ[DRAMのような高速動作が可能であったが](https://ja.wikipedia.org/wiki/ダイナミックランダムアクセスメモリ "wikilink")、高[クロック](../Page/クロック.md "wikilink")対応品は主に[汎用機や](../Page/メインフレーム.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")でのキャッシュメモリとしての使用を前提として開発、販売されていたため、[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")、価格共々非常に高く、また、[歩留まり](../Page/歩留まり.md "wikilink")も非常に悪かったため、常識的な価格帯においてPentium Proのクロックを向上させる事は困難とされた。

そこでこのPentium IIからはCPU基板の上にCPUコアチップとコアチップの1/2の速度で動作する[2次キャッシュメモリチップが](../Page/L2キャッシュ.md "wikilink")[実装](../Page/実装.md "wikilink")され、**[S.E.C.C.](../Page/Slot_1.md "wikilink")** (Single Edge Contact Cartridge) ならびに**[S.E.C.C.2](../Page/Slot_1.md "wikilink")** (Single Edge Contact Cartridge 2) と呼ばれる[ファミコンなどに代表される](https://ja.wikipedia.org/wiki/ファミリーコンピュータ "wikilink")[家庭用ビデオゲーム用の](https://ja.wikipedia.org/wiki/テレビゲーム "wikilink")[ROMカートリッジ風のパッケージに封入した](../Page/ロムカセット.md "wikilink")。これにより2次キャッシュ性能の大幅低下と引き替えに製造不良率が低下、[製造原価](../Page/製造原価.md "wikilink")、販売価格の低下に寄与し、また後のコアクロック向上による性能向上を容易にした。 低価格PC向けとしてPentium IIの外付け2次キャッシュメモリを削減（あるいは削除）した製品が[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")として投入され、[サーバ](../Page/サーバ.md "wikilink")用途にはキャッシュメモリを増量したPentium II [Xeon](../Page/Xeon.md "wikilink")が発売された。詳細は各プロセッサの項目を参照。 後継プロセッサは[Pentium IIIである](../Page/Pentium_III.md "wikilink")。

## 第一世代"クラマス" (Klamath)

[right](https://ja.wikipedia.org/wiki/ファイル:Pentium_II_inside_front.jpg "wikilink") 0.35μmプロセスで製造され、[バス速度は](../Page/フロントサイドバス.md "wikilink")66 MHzであった。これはP6アークテクチャの本領を発揮するには不十分な速度であり、またこのチップは非常に消費電力が大きく高熱を発した。特に300 MHz動作品は最大44.4 Wの電力を消費し、Xeonを除いてはP6系プロセッサ第一位の消費電力となっている 。ちなみに、第二位は[Pentium III](../Page/Pentium_III.md "wikilink") 1.13 GHz (S.E.C.C.2 / Coppermine) で41.4 W、第三位がPentium III 600 MHz (Katmai) で41.3 Wである。

なお、この世代のカートリッジは4枚のSRAMチップがCPU基板に実装されており、2枚1組で[インターリーブ](../Page/インターリーブ.md "wikilink")動作することで2次キャッシュ速度の低下を極力隠蔽する設計となっていた。

## 第二世代 "デシューツ" (Deschutes)

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に登場し、0.25μmプロセスで製造された。課題であった発熱は抑えられ、処理速度は大幅に向上した。333 MHz版まではFSB66 MHzのままだったが、350 MHz版以降でFSB速度が100 MHzへ高められた。なおFSB100 MHz版は、初期の一部ロット（および[ES版](https://ja.wikipedia.org/wiki/:en:Engineering_sample "wikilink")）を除き、CPU倍率が固定されるようになった。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Intel_Celeron_300A_MHz.jpg "wikilink")
Pentium IIをベースにL2キャッシュを縮小した製品\]\] また、この世代以降のP6系コンシューマー向けCPUではPentium Proと同様に2次キャッシュの有効レンジが従来の512 MBから4 GBに拡大されたため、大量にメモリを搭載したワークステーションやPCで512 MB以上の実メモリ空間へアクセスした際にメモリアクセスに巨大なペナルティが発生することが無くなったのも、重要な改良点であった。

## モバイル版 第一世代 "トンガ" (Tonga)

1998年登場。0.25μmプロセスで製造され、コア電圧を1.6 Vに抑えたもの。L2キャッシュは512 KBで、コアに統合されていないため動作速度はコアクロックの2分の1である。

ミニカートリッジ、モバイルモジュール（MMC1及びMMC2）といった小型の外付けパッケージで提供されるため、交換が容易であった。

## モバイル版 第二世代 "ディクソン" (Dixon)

1999年に登場。0.25μmプロセスで製造されL2キャッシュはコアに統合された。この為キャッシュ容量は256 KBと半減したものの、動作スピードはCPUコアの等速と2倍になり、結果処理速度が向上している。FSB100 MHz版が出たDeschutesと異なり、最後までFSB66 MHz据え置きとなった。

ミニカートリッジやモバイルモジュールタイプの他、コアの微細化により従来の8分の1サイズの[BGAタイプのものが用意された](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#BGA_\(Ball_grid_array\) "wikilink")。

なお、L2キャッシュをさらに半分の128 KBとしたものが[モバイルCeleron（Dixon-128K）として製造された](https://ja.wikipedia.org/wiki/Intel_Celeron#Dixon-128K "wikilink")。

## 関連項目

  - [P6マイクロアーキテクチャ](../Page/P6マイクロアーキテクチャ.md "wikilink")
  - [AMD K6](../Page/AMD_K6.md "wikilink") / [K6-2](../Page/AMD_K6-2.md "wikilink")

[Category:インテルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:インテルのマイクロプロセッサ "wikilink")