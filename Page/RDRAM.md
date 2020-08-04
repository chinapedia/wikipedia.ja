> この記事は[RDRAM](https://ja.wikipedia.org/wiki/RDRAM)から翻訳されています。


**RDRAM**は『Rambus DRAM』の略で、[Rambus社による基本設計で同社がライセンスする](https://ja.wikipedia.org/wiki/ラムバス "wikilink")、[SDRAM](../Page/SDRAM.md "wikilink")モジュールの方式の一種である。バスのビット幅を制限する代わりに、一筆書き状の配線によって実現される高速性などを特長とする。

## 概要

設計の発展により、Base Rambus DRAM、Concurrent Rambus DRAM、Direct Rambus DRAM（DRDRAM）などがある。総称して、あるいは単に、**Rambus DRAM**とも呼ぶ。特徴に、バスのビット幅を制限する代わりに、一筆書き状の配線によって実現される高速性などがあったが、メモリモジュールを取り付けない空きメモリスロットに配線のみのダミーのモジュールを付け、配線のターミネートを管理しなければならないなどの利便上の欠点などから、パーソナルコンピュータ用としては広く普及するには至らなかった。

## 実装

### パーソナルコンピュータ

RDRAMをサポートする最初のPC用[マザーボード](../Page/マザーボード.md "wikilink")は[1999年](../Page/1999年.md "wikilink")に登場した。これらの製品はPC-800 RDRAMに対応しており、400[メガヘルツ](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")動作で1600[MB](../Page/メガバイト.md "wikilink")/sの転送速度を、184ピンのRIMMフォームファクタを用いて提供した。

[クロック](../Page/クロック.md "wikilink")信号の立ち上がりと立ち下がりで転送する[ダブルデータレート](https://ja.wikipedia.org/wiki/ダブルデータレート "wikilink")方式であることもあり、400MHzのラムバス規格は（主としてマーケティング上の理由から）PC800という名前となった。これは、以前の規格PC-133 [SDRAM](../Page/SDRAM.md "wikilink")より大幅に高速であった。PC-133は133MHzで動作し、64bitの168ピン[DIMM](../Page/DIMM.md "wikilink")の[フォームファクタ](https://ja.wikipedia.org/wiki/フォームファクタ "wikilink")で1066MB/sの転送速度を提供した。

[thumb](https://ja.wikipedia.org/wiki/ファイル:RAMBUS-Memory.jpg "wikilink")

さらに、マザーボードが[デュアルあるいは](../Page/デュアルチャネル.md "wikilink")[クアッドチャネル](https://ja.wikipedia.org/wiki/クアッドチャネル "wikilink")のメモリサブシステムを備えている場合、すべてのメモリのチャンネルは同時にアップグレードする必要があった。16[ビット](../Page/ビット.md "wikilink")のモジュールが1チャンネルのメモリを提供し、32ビットのものが2チャンネルを提供した。このため、16ビットのモジュールを受け付けるデュアルチャンネルのマザーボードは、RIMMをペアで着脱する必要があった。32ビットのモジュールに対応したデュアルチャンネルのマザーボードは、一枚ずつRIMMを着脱することができた。

#### モジュール仕様

| 規格名                | バス幅   | チャンネル数         | 仕様上のクロック速度 | 転送速度      |
| ------------------ | ----- | -------------- | ---------- | --------- |
| PC600              | 16ビット | シングルチャンネル RIMM | 300 MHz    | 1200 MB/s |
| PC700              | 16ビット | シングルチャンネル RIMM | 355 MHz    | 1420 MB/s |
| PC800              | 16ビット | シングルチャンネル RIMM | 400 MHz    | 1600 MB/s |
| PC1066 (RIMM 2100) | 16ビット | シングルチャンネル RIMM | 533 MHz    | 2133 MB/s |
| PC1200 (RIMM 2400) | 16ビット | シングルチャンネル RIMM | 600 MHz    | 2400 MB/s |
| RIMM 3200          | 32ビット | デュアルチャンネル RIMM | 400 MHz    | 3200 MB/s |
| RIMM 4200          | 32ビット | デュアルチャンネル RIMM | 533 MHz    | 4200 MB/s |
| RIMM 4800          | 32ビット | デュアルチャンネル RIMM | 600 MHz    | 4800 MB/s |
| RIMM 6400          | 32ビット | デュアルチャンネル RIMM | 800 MHz    | 6400 MB/s |

### ビデオゲーム機

[thumb](https://ja.wikipedia.org/wiki/ファイル:RDRAM18-NUS_01.jpg "wikilink") Concurrent Rambus DRAMは、[1996年](../Page/1996年.md "wikilink")の[NINTENDO64](../Page/NINTENDO64.md "wikilink") (N64) をはじめとしていくつかの[ビデオゲーム機で使用された](../Page/ゲーム機.md "wikilink")。[任天堂](../Page/任天堂.md "wikilink")のゲーム機は4.5[MiBの](https://ja.wikipedia.org/wiki/メビバイト "wikilink")9ビット[バス](../Page/バス_\(コンピュータ\).md "wikilink")、266MHzダブルデータレート動作のRDRAMを使用し、500MB/sの転送速度を提供した。RDRAMの簡素な設計のおかげで、N64は広いメモリ転送速度を確保することができた。またRDRAMの狭いバス幅のおかげで、ボードの回路設計者は単純な設計手法を使用しコストを最小限にすることができた。しかしながら、高いアクセス[レイテンシ](../Page/レイテンシ.md "wikilink")のため、RDRAMのメモリは好まれなかった。N64では、RDRAMモジュールはパッシブの[ヒートスプレッダ](https://ja.wikipedia.org/wiki/ヒートスプレッダ "wikilink")部品により冷却されていた[1](http://n64.icequake.net/)。また36Pinメモリー拡張コネクタを持ち、ターミネータパックを取り外して代わりに[メモリー拡張パック](https://ja.wikipedia.org/wiki/メモリー拡張パック "wikilink")を挿入することで合計9MiBに増設できた。

[thumb](https://ja.wikipedia.org/wiki/ファイル:DRDRAM_01A.jpg "wikilink") [ソニー](../Page/ソニー.md "wikilink")は[PlayStation 2でDRDRAMを使用した](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")。PS2は32MiBのメモリを備え、デュアルチャンネルの構成を実現したため3200MB/sの転送速度が利用可能であった。PlayStation 2発売時のパーソナルコンピューターで主流であったPC100 SDRAMが800MB/s程度であった事を考えると相当に高速であった。

[PlayStation 3はRDRAMの後継と考えられるRambus社の](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")[XDR DRAMを](../Page/XDR_DRAM.md "wikilink")256MiB使用し、8倍速転送\[1\]（ダブルデータレートと比較）の400MHz 64ビットバスにより、3.2GHzの速度で、204.8Gbit/s (25.6GiB/s) という高いデータレートを実現した\[2\]。

## ビデオカード

[シーラス・ロジック](../Page/シーラス・ロジック.md "wikilink")は、*Laguna*グラフィックチップファミリの三つの製品でConcurrent Rambus DRAMのサポートを実現した。2DのみのCL-GD5462と、3Dアクセラレーションも可能な2DチップのCL-GD5464、さらにAGP接続に対応したCL-GD5465である。

RDRAMは、その高い転送速度により潜在的に高速であるうえ、コスト面での利点を提供した。このチップは[CreativeのGraphics](../Page/クリエイティブテクノロジー.md "wikilink") Blaster MA3xxシリーズなどに用いられた。

他には東芝、[クロマティックリサーチ](https://ja.wikipedia.org/wiki/クロマティックリサーチ "wikilink")([英](https://ja.wikipedia.org/wiki/:en:Chromatic_Research "wikilink")) などが開発したMPACTメディアプロセッサがある。最初のMPACTはDVDデコードを担当する単なるコプロセッサであったが、後継のMPACT2ではVGA機能を有し、名目上のビデオカードとなった。MPACTでは9ビット幅で4.5MiBのRambus DRAMが接続されたが、MPACT2では18ビット幅で4.5MiBないし9MiBのRambus DRAMが接続された。

## 性能

現代の他のメモリ規格と比較して、ラムバスには若干のレイテンシの増加と、発熱、製造上の複雑さとコストの高さがある。RDRAMの大きなダイサイズを批判する者もおり、16Mビットで10-20パーセント、64Mで約5パーセントのインターフェイスのためのペナルティが必要である[2](http://findarticles.com/p/articles/mi_m0EKF/is_n2161_v43/ai_19288320)。

PC-800 RDRAMは45[ナノ秒](../Page/ナノ秒.md "wikilink")のレイテンシで動作するが、これはその時点での対抗する他のDRAM技術より高いレイテンシであった。RDRAMのメモリチップはSDRAMのチップよりかなり大きな熱を排出し、すべてのRIMMにヒートスプレッダを必要とした。RDRAMはそれぞれのメモリチップにコントローラーを内蔵しており、[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")上に配置された単一のメモリコントローラを使用するSDRAMに対して製造上大幅に複雑であった。RDRAMは、高い製造コストとライセンス料のためPC-133 SDRAMと比べ2-3倍の価格であった。[2000年](../Page/2000年.md "wikilink")に登場したPC-2100 [DDR SDRAMはクロック速度](../Page/DDR_SDRAM.md "wikilink")133MHzで動作し、184ピンのDIMMフォームファクタを用いた64ビットバスで2100MB/sの性能を提供した。

複数のRIMMを一つのメモリチャンネルに装着する場合、パフォーマンス上の影響はSDRAMの設計より大きく、SDRAMのマザーモードでは経路が1〜2チップであるのに対して、RDRAMでは遠いメモリモジュール上のチップはメモリコントローラの近くに物理的に配置されたすべてのメモリチップ上を通らなければならない。 [thumb](https://ja.wikipedia.org/wiki/IMAGE:RDRAM-und-sein-CRIMM.jpg "wikilink") ごく一般的なラムバスメモリコントローラの設計では、メモリモジュールを2本をセットとして装着することが前提となる。残った未使用のメモリスロットは、[CRIMM](https://ja.wikipedia.org/wiki/CRIMM "wikilink")を装着しなければならない。

CRIMMモジュールはメモリの容量を増やすものではなく、マザーボード上で信号が反射する終端が生じないよう、終端抵抗に対する信号を伝達するためだけに働く。

(SCSIのターミネーターに相当するものである。)右の画像はCRIMMモジュールを示す。

[Intel 840](https://ja.wikipedia.org/wiki/インテル_チップセット#840_チップセット_ファミリ "wikilink") ([Pentium III](../Page/Pentium_III.md "wikilink"))、[Intel 850](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_850_チップセット_ファミリ "wikilink") ([Pentium 4](../Page/Pentium_4.md "wikilink"))、[Intel 860](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_860_チップセット_ファミリ "wikilink") ([Pentium 4 Xeon](https://ja.wikipedia.org/wiki/Xeon#Xeon_（NetBurstマイクロアーキテクチャ世代） "wikilink")) [チップセット](../Page/チップセット.md "wikilink")の登場に伴い、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")はバス幅を32ビットに増やすことで転送速度を2倍にしたデュアルチャンネルのPC-800 RDRAMのサポートを追加した。その後、[i850E](https://ja.wikipedia.org/wiki/i850E "wikilink")チップセットでは PC-1066 RDRAMが導入され、デュアルチャンネル時の合計転送速度を4200MB/sに拡大した。[2002年](../Page/2002年.md "wikilink")に、インテルは[E7205](https://ja.wikipedia.org/wiki/E7205 "wikilink") Granitebayチップセットを発表した。デュアルチャンネルのDDRを導入し、対抗するRDRAMより若干低いレイテンシで4200MB/sの合計転送速度で提供している。

RDRAMで800MHzの速度を達成するためには、64ビットのバス幅を持つ現代のSDRAM DIMMとは異なり、メモリモジュールは16ビットバスでしか動作できない。さらに、インテル820の登場した当時のRDRAMモジュールは、すべての製品が800MHzでは動作できず、遅いクロックでしか動作しないものもあった。

### ベンチマーク

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に実施された[ベンチマークテスト](https://ja.wikipedia.org/wiki/ベンチマークテスト "wikilink")では、大半の[アプリケーションがRDRAMでは低速に動作した](../Page/アプリケーションソフトウェア.md "wikilink")。RDRAMは[UMAではSDRAM製品よりわずかに高速であったものの](../Page/ユニファイドメモリアーキテクチャ.md "wikilink")、Intel 820はローエンドの製品ではなく、またRIMMを使用するローエンド製品は開発されなかった。このため、この利点はエンドユーザーにとっては無意味だった[3](http://www.tomshardware.com/1998/08/14/performance_impact_of_rambus/)。

[1999年](../Page/1999年.md "wikilink")、Intel 840・Intel 820・[Intel 440BXを使ったベンチマークでは](../Page/Intel_440BX.md "wikilink")、ラムバスチップセットを用いたことにより得られる性能の向上（もしあればだが）は、[ワークステーション](../Page/ワークステーション.md "wikilink")の用途を除き、440BXチップセットとPC-133 SDRAMに対して大幅に高い値段を正当化できるものではなかった[4](http://www.tomshardware.com/1999/12/15/the_rdram_avenger_/)。

後に[2002年](../Page/2002年.md "wikilink")、シングルチャンネルのDDR SDRAMモジュールが[SiS](../Page/Silicon_Integrated_Systems.md "wikilink")648と組み合わせた場合、実際のアプリケーションではデュアルチャンネルの1066MHz RDRAM構成のIntel 850Eと拮抗することが示された[5](http://www.tomshardware.com/2002/07/20/ddr400_kills_rambus/)。 さらに、デュアルチャンネルDDR400 SDRAMモジュールを使用可能なチップセットが登場しようとしていた。

## PC市場での RDRAM のマーケティング

1996年11月、ラムバスは[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")との開発およびライセンス契約を結んだ\[3\]。 DDR SDRAMと比較した場合のRDRAMの優位性を認識し、インテルはWintelの開発コミュニティに対し、自社の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")にラムバスメモリインターフェイスのみサポートする声明を発表し\[4\]、インテルはラムバス株を100万株、一株10ドルで購入する権利を与えられた。

1998年、インテルはDirect RDRAMの導入を加速させるため、5億ドルの資本投資を[マイクロン・テクノロジ](../Page/マイクロン・テクノロジ.md "wikilink")に対して行うことを計画した\[5\]。そのほかの投資として、1999年の[サムスン電子](../Page/サムスン電子.md "wikilink")への1億ドルの支払いなどがある。

移行の戦略として、インテルは将来的にIntel 82xチップセットで[Memory Transfer Hub](https://ja.wikipedia.org/wiki/Intel_820#MTH "wikilink") (MTH) を用いPC-133 SDRAM DIMMをサポートすることを計画した\[6\]。2000年、インテルはMTHの搭載されたIntel 820マザーボードをリコールした。MTHは同時にスイッチングを行う際、不明の理由で停止したり、突発的に再起動させる電気的なノイズを発生させたためである\[7\]。これ以降、Intel 820のマザーボードがMTHを搭載することはなかった。

2000年、インテルはリテールのPentium 4 CPUに2枚のRIMMをセットにして販売し、RDRAMを援助した\[8\]。しかし、インテルはその翌年の[2001年](../Page/2001年.md "wikilink")から徐々にラムバスへの支援を打ち切り始めた\[9\]。

[2003年](../Page/2003年.md "wikilink")、インテルはIntel 865および[Intel 875チップセットを発表し](https://ja.wikipedia.org/wiki/インテル_チップセット#Intel_875_チップセット_ファミリ "wikilink")、ハイエンドチップセットとしてIntel 850を置き換える製品として位置づけた。さらに、将来のメモリのロードマップにはラムバスは含まれていなかった\[10\]。

RDRAMを生産するライセンスを取得したDRAM製造会社はほとんどなく、技術ライセンスを取得した会社もPCマーケットの需要を満たすだけのRIMMを生産することに失敗し、メモリが高騰した2002年ですらRIMMがSDRAM DIMMより高い価格設定となった\[11\]。RDRAMが下降線をたどる中、DDRはスピードの面で発展し続け、しかも、RDRAMより安価であった。当時、DDR SDRAMで繰り広げられた大規模な価格競争により、DDR SDRAMは製造原価かそれ以下で販売された。RDRAMのサプライヤが一枚一枚のモジュールごとに良い利益を出す一方、DDR SDRAMのメーカーは大規模な損失を出した。現在でも生産されてはいるが、RDRAMをサポートするマザーボードはほとんどない。2002年から[2005年](../Page/2005年.md "wikilink")の間、RDRAMの市場シェアが5%を超えることは一度もなかった\[12\]。

[2004年](../Page/2004年.md "wikilink")には、[インフィニオン](../Page/インフィニオン・テクノロジーズ.md "wikilink")、[ハイニックス](https://ja.wikipedia.org/wiki/ハイニックス半導体 "wikilink")、サムスン、[マイクロン](../Page/マイクロン・テクノロジ.md "wikilink")、[エルピーダが](https://ja.wikipedia.org/wiki/エルピーダメモリ "wikilink")2001年に固定価格への操作を行ったことが明らかになった\[13\]。問題の企業は犯行を認め、後に罰金を科された。価格操作の目標は、不公平な市場戦略によりRDRAMを市場から抹殺するためであった。複数のメモリ製造企業が罪状を認め、ラムバスに数100万ドルの支払いを行った。

## 出典

## 外部リンク

  - [Rumbus 社ウェブサイト上の RDRAM](http://www.rambus.com/jp/technology/solutions/rdram/index.html)
  - [PS2のデュアルチャンネルRDRAMについての情報があるサイト](http://archives.cnn.com/2001/TECH/fun.games/10/24/linux.ps2.idg/index.html)
  - [RAMBUS メモリーの装着方法](http://www.memorystock.com/how_to_install_rambus_rimm.htm)
  - [RDRAM 装着の図解ガイド](http://www.cheapestrdram.com/rdram_install.php)
  - [『Direct RDRAMはなぜPC分野では失敗したのか？』、ASCII MEDIA WORKS、2011年05月09日](http://ascii.jp/elem/000/000/604/604231/)

[it:DRAM\#Direct Rambus DRAM (DRDRAM)](https://ja.wikipedia.org/wiki/it:DRAM#Direct_Rambus_DRAM_\(DRDRAM\) "wikilink")

[Category:SDRAM](https://ja.wikipedia.org/wiki/Category:SDRAM "wikilink")

1.  [Rambus.com 8倍速](http://www.rambus.com/jp/technology/innovations/detail/odr.html)
2.  [Rambus.com XDR](http://www.rambus.com/us/products/xdr_xdr2/index.html)
3.  <http://www10.edacafe.com/nbc/articles/view_weekly.php?articleid=209198&page_no=3>
4.  <http://www.webopedia.com/TERM/R/RDRAM.html>
5.  <http://www.hpcwire.com/hpc-bin/artread.pl?direction=Current&articlenumber=14137>
6.  <http://www.tomshardware.com/1999/10/05/intel_i820_chipset_review/>
7.  <http://www.computerwriter.com/Star/2000/jun/cw062100_intel_i820_mth_recall.htm>
8.  <http://news.zdnet.com/2100-9595_22-523724.html>
9.  <http://archive.is/20120711022039/http://news.com.com/Intel+drops+Rambus+subsidies/2100-1001_3-270561.html>
10. <http://www.tomshardware.com/2003/04/01/ram_wars/page9.html>
11. <http://www.geek.com/news/geeknews/2002mar/mac20020306010604.htm>
12. <http://www.tomshardware.com/2003/04/01/ram_wars/>
13. <http://archive.is/20120712124210/http://news.com.com/Government+finds+witness+in+RAM+price-fixing+probe/2100-1004_3-5347423.html>