> この記事は[System p](https://ja.wikipedia.org/wiki/System_p)から翻訳されています。


**System p**は、[IBM](../Page/IBM.md "wikilink")の[UNIX](../Page/UNIX.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")および[ワークステーション](../Page/ワークステーション.md "wikilink")のシリーズである。[プロセッサ](../Page/プロセッサ.md "wikilink")は[POWER](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")、稼働可能な[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) は[AIX](../Page/AIX.md "wikilink")および[Linux](../Page/Linux.md "wikilink")である。

従来の**RS/6000**([RISC](../Page/RISC.md "wikilink") System/6000)、**pSeries**の後継である。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")4月に後継の [Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink") が発表された。

## 名称

正式名称は「IBM eServer pSeries」である。IBMのサーバ全体のブランド名「[IBM Systems](https://ja.wikipedia.org/wiki/IBM_Systems "wikilink")」を構成するシリーズ（[System z](../Page/System_z.md "wikilink")、[System i](https://ja.wikipedia.org/wiki/System_i "wikilink")、System p、[System x](../Page/System_x.md "wikilink")、[System Storage](https://ja.wikipedia.org/wiki/System_Storage "wikilink")）の1つである。「p」は「performance（パフォーマンス）」を意味する。また[POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink")ベースのものを **p5** とも称する。

## 歴史

  - [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink") [RT-PCの後継として](../Page/IBM_RT-PC.md "wikilink") RS/6000 が発表された。この製品ファミリは何回か名称が変更されてきた。当初、サーバもワークステーションも RS/6000 と呼ばれていた。
  - [1990年代](../Page/1990年代.md "wikilink") 従来の[MCAモデルから](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")、[PReP](https://ja.wikipedia.org/wiki/PReP "wikilink")/[CHRP](https://ja.wikipedia.org/wiki/CHRP "wikilink")ベースの[PCIモデルに](../Page/Peripheral_Component_Interconnect.md "wikilink")、43P(7043)などから順次移行された。
  - 2000年 e-Server ブランド戦略により、サーバだけを ***e*Server pSeries** とした。
  - 2004年 [POWER5](https://ja.wikipedia.org/wiki/POWER5 "wikilink") プロセッサの導入に際して、該当モデルを ***e*Server p5** と呼んだ。
  - 2005年 ブランド名戦略の変更により、このファミリは再び **System** を頭に置くブランド名とされ、**System p** となった。また、新たに IBM [OpenPower](https://ja.wikipedia.org/wiki/OpenPower "wikilink") 製品ラインが登場した。
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")4月2日 後継の **[Power Systems](https://ja.wikipedia.org/wiki/Power_Systems "wikilink")** が発表された。

広い範囲をカバーしているが、ワークステーションは徐々に品揃えを減らしつつある。

## プロセッサ

初期の RS/6000 では、[POWER](../Page/POWER_\(マイクロプロセッサ\).md "wikilink") および POWER2 プロセッサが使われていた。[PowerPC](../Page/PowerPC.md "wikilink") [ISA](../Page/命令セット.md "wikilink") が開発されると、下位機種は PowerPC 604e などを使うようになった。上位機種やクラスターでは、[浮動小数点演算性能の高い](../Page/浮動小数点数.md "wikilink") POWER が引き続き使われた。整数演算性能が重視される商用向け機種では PowerPC から派生した RS64 が使われた。

POWER4 が開発されると RS64 は使われなくなった。このためビジネス向けと科学技術計算向けの区別がなくなった。その後、System p は主に POWER5+ を使用し、一部の下位機種やブレードサーバでは [PowerPC 970](../Page/PowerPC_970.md "wikilink") も使用された。現在の最新は、ブレードを含めPOWER8である。

## 機能

IBM System p5 と IBM *e*Server p5 以降は、仮想化機能として以下を備えている。

  - [動的論理パーティショニング](https://ja.wikipedia.org/wiki/動的論理パーティショニング "wikilink")（[Dynamic LPAR](https://ja.wikipedia.org/wiki/Dynamic_Logical_Partitioning "wikilink")、D-LPAR）
  - マイクロパーティショニング
  - 仮想I/Oサーバ（VIOS）

[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")は[AIX](../Page/AIX.md "wikilink")およびPOWER版の[Linux](../Page/Linux.md "wikilink")（Linux on POWER）が使用できる。2008年4月現在、AIXはV6.1が最新である。

## ディープ・ブルー

[ディープ・ブルーはRS](../Page/ディープ・ブルー_\(コンピュータ\).md "wikilink")/6000をベースに作られた[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")であり、正式な時間制限でチェスの世界チャンピオン（[ガルリ・カスパロフ](../Page/ガルリ・カスパロフ.md "wikilink")）に初めて勝利したコンピュータとなった。30台のRS/6000で構成されたマシンに、480台の特殊なチェス専用VLSIを接続していた。[チェス](../Page/チェス.md "wikilink")プログラムは[C言語](../Page/C言語.md "wikilink")で書かれ、AIX 上で動作した。ディープ・ブルーは1秒間に20億箇所の位置を評価する能力を有していた。

## 関連項目

  - [IBM Systems](https://ja.wikipedia.org/wiki/IBM_Systems "wikilink")
      - [System z](../Page/System_z.md "wikilink")
      - [System i](https://ja.wikipedia.org/wiki/System_i "wikilink")
      - [System x](../Page/System_x.md "wikilink")

## 参考文献

## 外部リンク

  - [IBM Power Systems](https://www.ibm.com/jp-ja/it-infrastructure/power)
  - [IBM Systems](https://www.ibm.com/jp-ja/it-infrastructure)
  - [IBM マーケットプレイス](https://www.ibm.com/jp-ja/products)
  - [IBM ソフトウェア](https://www.ibm.com/software/jp/)
  - [IBM RS/6000 PowerPC/AIX Notebook](http://www.thinkwiki.org/wiki/Category:860)
  - [RS/6000 Machine Timeline](http://archive.rootvg.net/RStimeline.htm)
  - [RS/6000 Machine Type Models](http://archive.rootvg.net/RSmodels.htm)

[Category:IBMのワークステーション](https://ja.wikipedia.org/wiki/Category:IBMのワークステーション "wikilink") [Category:コンピュータ史](https://ja.wikipedia.org/wiki/Category:コンピュータ史 "wikilink") [Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:サーバ_(ハードウェア)](https://ja.wikipedia.org/wiki/Category:サーバ_\(ハードウェア\) "wikilink")