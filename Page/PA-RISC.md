> この記事は[PA-RISC](https://ja.wikipedia.org/wiki/PA-RISC)から翻訳されています。


**PA-RISC**（**ぴーえーりすく**）は、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")社 (HP) の*Systems & VLSI Technology Operation*が開発した[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink") [アーキテクチャである](../Page/コンピュータ・アーキテクチャ.md "wikilink")。

その名前にも含まれているように[RISC](../Page/RISC.md "wikilink")アーキテクチャの実装であり、PAは*Precision Architecture*（精密なアーキテクチャ）の略である。また、**HP/PA**つまり***H**ewlett **P**ackard **P**recision **A**rchitecture*と呼ばれることもある。

1986年2月26日、PA-RISCの最初の実装であるTS1を採用した [HP 3000 Series 930](https://ja.wikipedia.org/wiki/HP_3000 "wikilink") と [HP 9000 Model 840](https://ja.wikipedia.org/wiki/HP_9000 "wikilink") が発表された\[1\]\[2\]。

HPと[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")は [Itanium](../Page/Itanium.md "wikilink")（[IA-64](../Page/IA-64.md "wikilink") ISA）を共同開発し、PA-RISCはItaniumに取って代わられた\[3\]。2008年末にはPA-RISCベースの HP 9000 システムの販売を終了したが、サポートは2013年まで継続予定である\[4\]。

## 背景

1980年代後半、HPは[CISC](../Page/CISC.md "wikilink")のCPUを使った4つのコンピュータシリーズを製造していた。1つは[80286ベースの](../Page/Intel_80286.md "wikilink")[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink") Vectra シリーズだが、残る3つは[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")ベースではない。1つは[アポロコンピュータ](../Page/アポロコンピュータ.md "wikilink")社を買収した際に得た[モトローラ](../Page/モトローラ.md "wikilink")の[68000ファミリを使ったUNIXワークステーション](../Page/MC68000.md "wikilink") HP Series 300 で、残る2つは Silicon-on-sapphire (SOS) 技術を使ったHP独自設計の [16ビット](../Page/16ビット.md "wikilink")[CPU](../Page/CPU.md "wikilink")の[HP3000](https://ja.wikipedia.org/wiki/HP3000 "wikilink")シリーズと、独自設計のマイクロプロセッサを使った[UNIX](../Page/UNIX.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")の [HP 9000](https://ja.wikipedia.org/wiki/HP_9000 "wikilink") シリーズ（16ビットおよび32ビット）である。HPはこれらPC互換機以外のマシンをPA-RISCを用いてひとつの RISC CPU ファミリに統合しようとしていた。

Precision Architecture は1986年に登場した。当初、32ビットの整数レジスタを32本と64ビットの浮動小数点レジスタを16本持っていた。浮動小数点レジスタが16本では性能に悪影響があることがわかり、バージョン1.1で倍の32本にしている。設計を行ったアーキテクトは、Allen Baum、Hans Jeans、Michael J. Mahon、Ruby Bei-Loh Lee、Russel Kao、Steve Muchnick、Terrence C. Miller、David Fotland、William S. Worley らである\[5\]。

## PA-7000シリーズ

[thumb](https://ja.wikipedia.org/wiki/ファイル:HP_PA-RISC_7300LC.jpg "wikilink") 初期のPA-RISCチップは[32ビット](../Page/32ビット.md "wikilink")であった。最初の実装TS1は、[TTL](../Page/Transistor-transistor_logic.md "wikilink") (74F) チップを組合わせてCPUを構成したものである。その後、VLSIを使ったマルチチップ方式となり、NMOSプロセス（NS1とNS2）とCMOSプロセスのもの（CS1とPCX）が作られた。1980年代終盤、そういった初期のPA-RISCチップが[HP3000](https://ja.wikipedia.org/wiki/HP3000 "wikilink")シリーズの新しいマシン930と950に使われた。これらのマシンは当時、開発した研究所の名前をとって**Spectrum**と呼ばれた。OSは[MPE](https://ja.wikipedia.org/wiki/MPE "wikilink")/iXが動作した。[HP 9000シリーズもすぐにPA](https://ja.wikipedia.org/wiki/HP_9000 "wikilink")-RISCプロセッサを導入し、OSはHP製[UNIX](../Page/UNIX.md "wikilink")の[HP-UX](../Page/HP-UX.md "wikilink")であった。

PA-RISCプロセッサ上に移植された他のオペレーティング・システムとしては、[Mach](../Page/Mach.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[NEXTSTEP](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")、そしてリリースされなかった[Windows NTがある](../Page/Microsoft_Windows_NT.md "wikilink")。

PA-RISCの興味深い点は、そのシリーズのほとんどが[L2キャッシュ](../Page/L2キャッシュ.md "wikilink")を持たなかったことである。その代わり大きな一次キャッシュを使っているが、以前は別チップをバスで接続していたが、現在は内蔵している。PA-7100LCとPA-7300LCだけがL2キャッシュを持つ。もうひとつPA-RISC独自と言えるのは7100LCで初めて導入された"Multimedia Acceleration eXtensions (MAX)"形式のマルチメディア命令 ([SIMD](../Page/SIMD.md "wikilink")) である。

## PA-8000シリーズ

1996年、[ISAが](https://ja.wikipedia.org/wiki/命令セット "wikilink")[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")に拡張され、PA-RISC 2.0 と名付けられた。[積和演算](../Page/積和演算.md "wikilink")も追加されており、浮動小数点を多用するアルゴリズムで役立つ。MAX SIMD 拡張も備えており、マルチメディア・アプリケーションで役立つ命令を提供している。最初の PA-RISC 2.0 の実装は1996年1月、 としてリリースされた。PA-8000は10個の機能ユニットを持ち、先進的な[パイプラインシステムを搭載していた](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")。また、命令キャッシュをふたつに分け、長期保持のキャッシュと短期保持のキャッシュを設けた。1997年にリリースされたPA-8200はPA-8000とほぼ同じであるが、[分岐予測](../Page/分岐予測.md "wikilink")機能が改善され、[TLBミス率が低減され](https://ja.wikipedia.org/wiki/トランスレーション・ルックアサイド・バッファ "wikilink")、大容量高速キャッシュを持っていた。

PA-8500では1.5Mバイトの一次キャッシュをチップ上に組み込み、大きな性能向上を実現した。また、同時に[DDRバスを導入し](../Page/DDR_SDRAM.md "wikilink")、最大2GB/sのメモリ転送速度を実現した。分岐予測のための履歴テーブルは2倍の2048エントリとなり、[TLBは](https://ja.wikipedia.org/wiki/トランスレーション・ルックアサイド・バッファ "wikilink")120エントリから160エントリに拡張された。

8600は8500の高クロック版であり、"quasi-LRU instruction cache eviction policy"（擬似LRU命令キャッシュ入れ替えポリシー）を採用している。8700は8600をさらに高クロックにして、2.25MBの一次キャッシュを持っている。また、擬似[LRU命令キャッシュ入れ替えポリシー](../Page/Least_Recently_Used.md "wikilink")（命令キャッシュの中で最も使われていないエントリを見つけて入れ替える方式。本当に使用頻度を記録するのは至難なので「擬似」的に使用頻度を決める）とデータ[プリフェッチ](../Page/プリフェッチ.md "wikilink")機能（ロード命令を実行する前に、メモリから読み込んでくる）を備えている。一次キャッシュは大容量であるもののあまり速くなく、性能の足かせとなった。しかし、プロセスのサイズを考慮するとHPが内蔵したキャッシュのサイズは印象的である。

PA-8800（コードネームMako）は2つの独立したマクロプロセッサをひとつのダイに組み込んでいる。そして、ひとつのチップで2ウェイの[SMPを構成する](../Page/対称型マルチプロセッシング.md "wikilink")。8800内の各プロセッサは1.5Mバイトの一次キャッシュを持つが、HPは一次キャッシュのみというポリシーをやめて32MBの外部L2キャッシュをサポートした。外部バスは6.4GB/sのItanium2のバスを採用し、PA-RISCと[Itanium](../Page/Itanium.md "wikilink")に共通のサーバデザインを採用した。

PA-8900は8800によく似ているが、L2キャッシュを64MBまで拡張し、キャッシュエラー検出や訂正などの機能を強化した。噂されていたような8800のダイ縮小版ではない。これがPA-RISCシリーズの最後のマイクロプロセッサである。

HP社の方針と思われるが、PA-RISCは高性能であるものの周辺を含めたシステムとしての販売のみを行ってきたため、[MIPSのように広く使われることはなかった](../Page/MIPSアーキテクチャ.md "wikilink")。PA-RISCは既にその役目を終え、MIPSのように組み込みプロセッサとして残ることはない。

## モデルの変遷

<table>
<thead>
<tr class="header">
<th><p>モデル</p></th>
<th><p>別名</p></th>
<th><p>登場年</p></th>
<th><p>周波数[MHz]</p></th>
<th><p>メモリバス[MB/s]</p></th>
<th><p>プロセス[μm]</p></th>
<th><p>トランジスタ[百万個]</p></th>
<th><p>ダイサイズ[mm2]</p></th>
<th><p>電力[W]</p></th>
<th><p>Dキャッシュ[kB]</p></th>
<th><p>Iキャッシュ[kB]</p></th>
<th><p>L2キャッシュ[MB]</p></th>
<th><p>ISA</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TS-1</p></td>
<td><p>?</p></td>
<td><p>1986</p></td>
<td><p>8</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>—</p></td>
<td><p>—</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>—</p></td>
<td><p>1.0</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>CS-1</p></td>
<td><p>?</p></td>
<td><p>1987</p></td>
<td><p>8</p></td>
<td><p>?</p></td>
<td><p>1.6</p></td>
<td><p>0.164</p></td>
<td><p>72.93</p></td>
<td><p>1</p></td>
<td><p>—</p></td>
<td><p>0.25</p></td>
<td><p>—</p></td>
<td><p>1.0</p></td>
<td><p>[6]</p></td>
</tr>
<tr class="odd">
<td><p>NS-1</p></td>
<td><p>?</p></td>
<td><p>1987</p></td>
<td><p>25/30</p></td>
<td><p>?</p></td>
<td><p>1.5</p></td>
<td><p>0.144</p></td>
<td><p>70.56</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>—</p></td>
<td><p>1.0</p></td>
<td><p>[7]</p></td>
</tr>
<tr class="even">
<td><p>NS-2</p></td>
<td><p>?</p></td>
<td><p>1989</p></td>
<td><p>27.5/30</p></td>
<td><p>?</p></td>
<td><p>1.5</p></td>
<td><p>0.183</p></td>
<td><p>196</p></td>
<td><p>27</p></td>
<td><p>512</p></td>
<td><p>512</p></td>
<td><p>—</p></td>
<td><p>1.0</p></td>
<td><p>[8]</p></td>
</tr>
<tr class="odd">
<td><p>PCX</p></td>
<td><p>?</p></td>
<td><p>1990</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>1.0</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PCX-S</p></td>
<td><p>PA-7000</p></td>
<td><p>1991</p></td>
<td><p>66</p></td>
<td><p>?</p></td>
<td><p>1.0</p></td>
<td><p>0.58</p></td>
<td><p>201.6</p></td>
<td><p>?</p></td>
<td><p>256</p></td>
<td><p>256</p></td>
<td><p>—</p></td>
<td><p>1.1a</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PCX-T</p></td>
<td></td>
<td><p>1992</p></td>
<td><p>33–100</p></td>
<td><p>?</p></td>
<td><p>0.8</p></td>
<td><p>0.85</p></td>
<td><p>196</p></td>
<td><p>?</p></td>
<td><p>2048</p></td>
<td><p>1024</p></td>
<td><p>—</p></td>
<td><p>1.1b</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PCX-T</p></td>
<td><p>PA-7150</p></td>
<td><p>1994</p></td>
<td><p>125</p></td>
<td><p>?</p></td>
<td><p>0.8</p></td>
<td><p>0.85</p></td>
<td><p>196</p></td>
<td><p>?</p></td>
<td><p>2048</p></td>
<td><p>1024</p></td>
<td><p>—</p></td>
<td><p>1.1b</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PCX-T'</p></td>
<td></td>
<td><p>1994</p></td>
<td><p>120</p></td>
<td><p>960</p></td>
<td><p>0.55</p></td>
<td><p>1.26</p></td>
<td><p>210</p></td>
<td><p>30</p></td>
<td><p>1024</p></td>
<td><p>2048</p></td>
<td><p>—</p></td>
<td><p>1.1c</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PCX-L</p></td>
<td></td>
<td><p>1994</p></td>
<td><p>60–100</p></td>
<td><p>?</p></td>
<td><p>0.75</p></td>
<td><p>0.9</p></td>
<td><p>201.6</p></td>
<td><p>7–11</p></td>
<td><p>—</p></td>
<td><p>1</p></td>
<td><p>2</p></td>
<td><p>1.1d</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PCX-L2</p></td>
<td><p>PA-7300LC</p></td>
<td><p>1996</p></td>
<td><p>132–180</p></td>
<td><p>?</p></td>
<td><p>0.5</p></td>
<td><p>9.2</p></td>
<td><p>260.1</p></td>
<td><p>?</p></td>
<td><p>64</p></td>
<td><p>64</p></td>
<td><p>0–8</p></td>
<td><p>1.1e</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PCX-U</p></td>
<td></td>
<td><p>1996</p></td>
<td><p>160–180</p></td>
<td><p>960</p></td>
<td><p>0.5</p></td>
<td><p>3.8</p></td>
<td><p>337.68</p></td>
<td><p>?</p></td>
<td><p>1024</p></td>
<td><p>1024</p></td>
<td><p>—</p></td>
<td><p>2.0</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PCX-U+</p></td>
<td><p>PA-8200</p></td>
<td><p>1997</p></td>
<td><p>200–240</p></td>
<td><p>960</p></td>
<td><p>0.5</p></td>
<td><p>3.8</p></td>
<td><p>337.68</p></td>
<td><p>?</p></td>
<td><p>2048</p></td>
<td><p>2048</p></td>
<td><p>—</p></td>
<td><p>2.0</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PCX-W</p></td>
<td><p>PA-8500</p></td>
<td><p>1998</p></td>
<td><p>300–440</p></td>
<td><p>1920</p></td>
<td><p>0.25</p></td>
<td><p>140</p></td>
<td><p>467</p></td>
<td><p>?</p></td>
<td><p>1024</p></td>
<td><p>512</p></td>
<td><p>—</p></td>
<td><p>2.0</p></td>
<td><p>[9]</p></td>
</tr>
<tr class="odd">
<td><p>PCX-W+</p></td>
<td><p>PA-8600</p></td>
<td><p>2000</p></td>
<td><p>360–550</p></td>
<td><p>1920</p></td>
<td><p>0.25</p></td>
<td><p>140</p></td>
<td><p>467</p></td>
<td><p>?</p></td>
<td><p>1024</p></td>
<td><p>512</p></td>
<td><p>—</p></td>
<td><p>2.0</p></td>
<td><p>[10]</p></td>
</tr>
<tr class="even">
<td><p>PCX-W2</p></td>
<td><p>PA-8700(+)</p></td>
<td><p>2001</p></td>
<td><p>625–875</p></td>
<td><p>1920</p></td>
<td><p>0.18</p></td>
<td><p>186</p></td>
<td><p>304</p></td>
<td><p>&lt;7.1@1.5 V</p></td>
<td><p>1536</p></td>
<td><p>768</p></td>
<td><p>—</p></td>
<td><p>2.0</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Mako</p></td>
<td><p>PA-8800</p></td>
<td><p>2003</p></td>
<td><p>800–1000</p></td>
<td><p>6400</p></td>
<td><p>0.13</p></td>
<td><p>300</p></td>
<td><p>361</p></td>
<td><p>?</p></td>
<td><p>768/core</p></td>
<td><p>768/core</p></td>
<td><p>32</p></td>
<td><p>2.0</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Shortfin</p></td>
<td><p>PA-8900</p></td>
<td><p>2005</p></td>
<td><p>800–1100</p></td>
<td><p>6400</p></td>
<td><p>0.13</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>?</p></td>
<td><p>768/core</p></td>
<td><p>768/core</p></td>
<td><p>64</p></td>
<td><p>2.0</p></td>
<td></td>
</tr>
</tbody>
</table>

## 脚注・出典

## 外部リンク

  - [OpenPA.net](http://www.openpa.net/) 分かりやすいPA-RISCチップとコンパイラに関する情報
  - [PA-RISC Linux](http://www.parisc-linux.org/) PA-RISC向けLinux移植に関するサイト
  - [PA8800 Risc Processor の概要](http://www.lostcircuits.com/mambo//index.php?option=com_content&task=view&id=42&Itemid=42) LostCircuits
  - [各種PA-RISCプロセッサの画像](http://www.chipdb.org/cat-pa-risc-592.htm) chipdb.org

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:ヒューレット・パッカードの製品](https://ja.wikipedia.org/wiki/Category:ヒューレット・パッカードの製品 "wikilink")

1.  "One Year Ago". (26 February 1987). *Computer Business Review*.
2.  Hewlett-Packard Company (September 1987). *Hewlett-Packard Journal* **38** (9): p. 3.
3.  [PA-RISCの歴史に幕、HPが最後の製品リリースでItaniumへの移行を完了](http://news.mynavi.jp/news/2005/06/01/103.html) マイナビ、2005年6月1日
4.  [How long will HP continue to support HP 9000 systems?](http://www.hp.com/products1/evolution/9000/faqs.html#2)
5.  Smotherman, Mark (2 July 2009). [*Recent Processor Architects*](http://www.cs.clemson.edu/~mark/architects.html).
6.  Marston, A. et al. (1987). "A 32b CMOS single-chip RISC type processor". *ISSCC Digest of Technical Papers*. pp. 28–29.
7.  Yetter, J. et al. (1987). "A 15 MIPS 32b Microprocessor". *ISSCC Digest of Technical Papers*.
8.  Boschma, Brian D. et al. (1989). "A 30 MIPS VLSI CPU". *ISSCC Digest of Technical Papers*. pp. 82–83, 299
9.  [HP L1000 & L2000 (rp5400/5450) Servers](http://www.openpa.net/systems/hp_l1000_l2000-rp5400_rp5450.html) OpenPA.net
10.