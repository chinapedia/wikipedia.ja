> この記事は[ColdFire](https://ja.wikipedia.org/wiki/ColdFire)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Hermstedt_Webshuttle_II_-_board_-_Motorola_Coldfire_MCF5204PU25B-0082.jpg "wikilink") **ColdFire**(コールドファイア)は、[モトローラ](../Page/モトローラ.md "wikilink")が[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けに開発した[68kアーキテクチャの](../Page/MC68000.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")。2004年以降は[フリースケール・セミコンダクタ](../Page/フリースケール・セミコンダクタ.md "wikilink")社の製品である。

## 命令セット

ColdFireの[命令セット](../Page/命令セット.md "wikilink")は[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")のソースレベルで[68000と互換性があり](../Page/MC68000.md "wikilink")(ベンダー提供の翻訳ソフトを使った場合)、オブジェクトコードレベルでは完全な互換ではない。従来の68000系CPUと比較すると、その[命令セット](../Page/命令セット.md "wikilink")の違いは、[BCD演算命令など](../Page/二進化十進表現.md "wikilink")、あまり使われない命令を削除し、他の命令も[アドレッシングモード](../Page/アドレッシングモード.md "wikilink")が削減されている点である。これにより単純で低コストな命令デコーダを実現していると思われる。また、[浮動小数点数](../Page/浮動小数点数.md "wikilink")は[MC68881](../Page/MC68881.md "wikilink")や68882のような80ビットではなく[64ビット](../Page/64ビット.md "wikilink")で表される。命令そのものも[16ビット](../Page/16ビット.md "wikilink")、[32ビット](../Page/32ビット.md "wikilink")、[48ビット](https://ja.wikipedia.org/wiki/48ビット "wikilink")の3種類の長さであり、この点でも68000系より単純化されている。

## 種類

フリースケールから入手可能な ColdFire は次の5つのバージョンである。

  - v1: 8ビットプロセッサからのマイグレーションのために作られた v2 のカットダウン版。2006年リリース。8ビットマイクロプロセッサ [68HC08](https://ja.wikipedia.org/wiki/Freescale_68HC08 "wikilink") から容易に移行可能であり、[ARM系のローエンドチップと競合する](../Page/ARMアーキテクチャ.md "wikilink")。
  - v2: オリジナルのColdFireであり、1994年リリース。[命令パイプライン](https://ja.wikipedia.org/wiki/命令パイプライン "wikilink")は1本で、[MMUも](../Page/メモリ管理ユニット.md "wikilink")[FPU](../Page/FPU.md "wikilink")もない。[積和演算](../Page/積和演算.md "wikilink")命令を持つバージョンもある。
  - v3: MAC（積和演算ユニット）が追加された。
  - v4: 限定的な[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")・コア
  - v4e（または eV4）: v4 の拡張版で、2000年リリース。MMUとFPUを追加し、MAC を改良したバージョン。
  - v5: 完全なスーパースケーラ・コア

[Debian](../Page/Debian.md "wikilink")プロジェクトは m68k ポートでの ColdFire サポートを行おうとしていた（ColdFire なら[MC68060](../Page/MC68060.md "wikilink")以上の性能が期待できるため）\[1\]。ColdFire のクロック周波数は300MHz程度であり、真の68000系CPUで最も高速な 75MHz\[2\] の MC68060 に負けない。ePipe\[3\] や SnapGear\[4\] といったネットワーク・セキュリティ機器でColdFireプロセッサを採用している。[Linux](../Page/Linux.md "wikilink")の動作する[ワンボードマイコン](../Page/ワンボードマイコン.md "wikilink")もあり\[5\]、中には[コンパクトフラッシュ](../Page/コンパクトフラッシュ.md "wikilink")サイズのものもある\[6\]。

2007年、ColdFire クローン Fido 1100 がリリースされた。これは ColdFire をベースにした実行時間の予測可能な[組み込みシステム](../Page/組み込みシステム.md "wikilink")向けの[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")である。ただし、命令セットが68kに準拠しているだけで、アーキテクチャは独自である\[7\]。

2006年11月、フリースケールはColdFireを[IPコア](../Page/IPコア.md "wikilink")として IPextreme Inc. を通してライセンス供与開始することを発表した\[8\]。ColdFire v1 コアは、[アルテラ](../Page/アルテラ.md "wikilink")の[FPGA](../Page/FPGA.md "wikilink") Cyclone-III 上でフリーライセンスで利用できる（ロイヤリティも徴収しない）\[9\]\[10\]。

2007年9月、フリースケールは ColdFire コアを使ったマイクロコントローラ Flexis ファミリをリリースした\[11\]。

2010年6月、フリースケールは Coldfire V1 コアと 90nm TFS（薄膜ストレージ）技術を組合わせた ColdFire+ を発表した\[12\]。

## 脚注・出典

## 関連項目

  - [μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")
  - [eCos](https://ja.wikipedia.org/wiki/eCos "wikilink")
  - [RTEMS](https://ja.wikipedia.org/wiki/RTEMS "wikilink")

## 外部リンク

  - [フリースケールの ColdFire 公式サイト](http://www.freescale.com/webapp/sps/site/homepage.jsp?nodeId=0162468rH3YTLC)
  - [Enter the DRAGON](http://elbox.com/news_04_12_17.html) - ColdFireベースの[Amiga](../Page/Amiga.md "wikilink")クローンの発表とその[FAQ](http://elbox.com/faq_dragon.html) - [ベーパーウェア](https://ja.wikipedia.org/wiki/ベーパーウェア "wikilink")も参照
  - [Debian m68k/ColdFire](http://alioth.debian.org/mail/?group_id=30876) porting project.
  - [Coldfire Background Debugging (BDM)](http://bdm.sourceforge.net/) project for GDB.
  - [Coldfire Emulator](http://www.slicer.ca/coldfire/)
  - [Differences between ColdFire & 68K](http://www.microapl.co.uk/Porting/ColdFire/cf_68k_diffs.html)
  - [uTasker project for V2 MCU, including Kirin3](http://www.utasker.com/kirin3.html) Free for non-commercial work and fully supported
  - [Atari ColdFire Project aka "FireBee"](http://acp.atari.org/) an Atari ST/TT clone based on a ColdFire processor

[Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink")

1.
2.  .
3.  .
4.  .
5.  .
6.  .
7.
8.
9.
10.
11. .
12.