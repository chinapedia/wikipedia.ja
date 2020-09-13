> この記事は[SPARC](https://ja.wikipedia.org/wiki/SPARC)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Sun_UltraSPARCII.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:TMX390Z50GF_01.jpg "wikilink") **SPARC**（スパーク、***S**calable **P**rocessor **Arc**hitecture*）は、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が開発・製造した[RISC](../Page/RISC.md "wikilink")ベースの[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")であり、その[命令セット](../Page/命令セット.md "wikilink")アーキテクチャの名称である。

現在は**SPARCインターナショナル**の登録商標であり、複数のメーカーがこのアーキテクチャに基づいたプロセッサを製造している。 オープンソース版がある。

## 歴史の概要

SPARCは[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")により、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に最初に開発された。

SPARCは[RISC](../Page/RISC.md "wikilink")ベースで、特に浮動小数点演算とバイナリレベルの互換性に注意が払われている。サン・マイクロシステムズは当初、自社の[ワークステーション](../Page/ワークステーション.md "wikilink")に、[モトローラ](../Page/モトローラ.md "wikilink")の[68000シリーズの](../Page/MC68000.md "wikilink")[MPUを利用していたが](../Page/CPU.md "wikilink")、後に[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")のRISC Iをモデルに自社開発に着手。Sun4のSPARC搭載モデルを発表した。

SPARCは、[完全ビッグエンディアンの](https://ja.wikipedia.org/wiki/ビッグエンディアン "wikilink")[RISC](../Page/RISC.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")[命令セット](../Page/命令セット.md "wikilink")アーキテクチャで、**SPARCインターナショナル** (*SPARC International, Inc.*) の登録商標である。SPARCインターナショナルはSPARCアーキテクチャの普及と規格検定テストの実施を目的として[1989年](../Page/1989年.md "wikilink")に設立された組織であり、SPARCアーキテクチャをオープンにすることで寿命を延ばすことを目的としている。[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")、[サイプレス・セミコンダクタ](https://ja.wikipedia.org/wiki/サイプレス・セミコンダクタ "wikilink")、[富士通](../Page/富士通.md "wikilink")、サン・マイクロシステムズなどの製造業者がSPARCのライセンス供与を受けている。結果として、SPARCアーキテクチャは完全にオープンとなっており、[GPLの下に](../Page/GNU_General_Public_License.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")として実装されたも存在する。

SPARCアーキテクチャの最初の実装はサン・マイクロシステムズのワークステーションで使われた。その後[富士通](../Page/富士通.md "wikilink")などでも使われ始め、やがてさらに大きな[SMPシステムや](../Page/対称型マルチプロセッシング.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")や制御用としても使われるようになった。SPARCマシンは一般に[Solaris](../Page/Solaris.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")（サンがSPARC用に設計したオペレーティングシステム）と結びつけて考えられているが、[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")などのオペレーティングシステムも使用できる。

アーキテクチャは何回か改訂されていて、最も新しいものがバージョン8と9である。1999年10月、富士通とサン・マイクロシステムズはバージョン9をベースに[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")SPARCプロセッサの共通仕様（コモン プログラマ リファレンスモデル）を共同開発することを発表した。この共通仕様は、SPARC Joint Programming Specification (JPS1) - Commonalityとして公開されている。また2005年12月、サン・マイクロシステムズは[UltraSPARC T1をオープンソース化することを発表した](../Page/UltraSPARC_T1.md "wikilink")。

## 特徴

SPARCアーキテクチャは[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")のRISC I & II（バークレーRISC、[:en:Berkeley RISC](https://ja.wikipedia.org/wiki/:en:Berkeley_RISC "wikilink")）の設計に大きな影響を受けている。本来のRISC設計は必要最小限のものであり、機能や命令の種類を可能な限り切り詰め、クロックサイクル毎に命令を実行することを目指した。このため、乗除算命令が無い、[分岐遅延スロット](https://ja.wikipedia.org/wiki/分岐遅延スロット "wikilink")が存在するなど、[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")と様々な面で類似している。

SPARCプロセッサは通常128本の汎用[レジスタを持つ](../Page/レジスタ_\(コンピュータ\).md "wikilink")。ただし、任意の時点でソフトウェアから見えるのは128本のうちの32本だけである。そのうち8本は汎用レジスタだが、*g0*レジスタは常に内容がゼロであり、実質的な汎用レジスタは7本で、常に同じ内容が見える。他の24本は[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")の一部をレジスタ化したものである。

これら24本のレジスタは、いわゆる[レジスタ・ウィンドウ](../Page/レジスタ・ウィンドウ.md "wikilink")を形成し、関数呼出とリターンの際に、このウィンドウがレジスタスタック上を上下に移動する。各ウィンドウは8本のローカルレジスタを持ち、8本のレジスタを上下の隣接ウィンドウのレジスタと共有する。共有されたレジスタは関数のパラメータ渡しと結果の値を戻すために使われ、ローカルレジスタは、各関数でのローカルな値を保持するために使われる。

SPARCの名称の由来にある「Scalable」とは、組み込み用途からサーバ用途まで同じ仕様を実装し、非特権命令に関しては完全に互換を維持することを意味している。アーキテクチャ上、用途に合わせて規模を変更できる点は、実装するレジスタ・ウィンドウの個数である。仕様では3個から32個までのウィンドウ実装を許可していて、実装者は32個を実装して関数コール性能を向上させるか、3個だけ実装してコンテキスト切り替え性能を向上させるか、あるいはその中間を選択できる。このため、SPARCのアーキテクチャは[C言語](../Page/C言語.md "wikilink")など[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")言語に向けて最適化されているとも言われる。同様なレジスタ・ウィンドウを持つアーキテクチャとして、[Intel i960](../Page/Intel_i960.md "wikilink")、[AMD 29000がある](https://ja.wikipedia.org/wiki/AMD_29000 "wikilink")。

SPARCバージョン8（1987年）では、[浮動小数点](../Page/浮動小数点数.md "wikilink")[レジスタファイル](https://ja.wikipedia.org/wiki/レジスタファイル "wikilink")は16本の[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")レジスタを持つ。各レジスタは2本の[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")レジスタとしても使用でき、全部で32本の単精度レジスタとなる。2本の倍精度レジスタを四倍精度レジスタとして使用することもでき、全体で8本の四倍精度レジスタとなる。SPARCバージョン9（1995年）ではさらに16本の倍精度レジスタを追加したが、これらは単精度レジスタとしては使用できない（四倍精度レジスタ8本としては使用可能）。

タグ付き加減算命令は[LSBの](https://ja.wikipedia.org/wiki/最下位桁ビット "wikilink")2ビットを無視して加減算を行う。これは、[MLや](https://ja.wikipedia.org/wiki/プログラミング言語ML "wikilink")[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")などのタグ付きの整数フォーマットを使うような言語の実装に有効と思われる。

## 仕様の履歴

アーキテクチャは何回か改訂されている。ハードウェアによる乗算と除算がバージョン8で追加されている。バージョン9ではかなり大幅な改訂が加えられ、[64ビット](../Page/64ビット.md "wikilink")化されたSPARC仕様が完成している。

さらにSPARC Joint Programming Specification (JPS1) では、MMU等のバージョン9では未定義とされた部分の仕様が規定されている。

サン・マイクロシステムズ固有のアーキテクチャ仕様であるUltraSPARC Architecture 2005では、命令とレジスタが追加され、超特権 (hyperprivileged) モードも追加された。この仕様は[UltraSPARC T1から始まる新たなUltraSPARCシリーズで実装される](../Page/UltraSPARC_T1.md "wikilink")。T1はCPUコアを8個備え、全体で32[スレッドを実行できる](../Page/スレッド_\(コンピュータ\).md "wikilink")。UltraSPARC Architecture 2005にはサンの標準拡張が含まれるが、それ以外はSPARC V9 Level 1仕様に完全準拠している。このアーキテクチャは1987年のSPARC V7からのアプリケーションのバイナリ互換性を維持している。

2005年12月にサン・マイクロシステムズはUltraSPARC T1の実装をオープンソース化した（[OpenSPARC](../Page/OpenSPARC.md "wikilink")参照）。

SPARCの様々な実装の中で、サン・マイクロシステムズのSuperSPARCとUltraSPARC-1は非常に人気があったことから、[SPEC CPU95と](https://ja.wikipedia.org/wiki/SPEC_CPU95 "wikilink")[CPU2000ベンチマークの基準システムとして使われている](https://ja.wikipedia.org/wiki/SPEC_CPU2000 "wikilink")。

|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |
|  |

SPARCマイクロプロセッサ仕様

### SPARC64

[SPARC64_VIIIfx_2.00GHz.jpg](https://ja.wikipedia.org/wiki/File:SPARC64_VIIIfx_2.00GHz.jpg "fig:SPARC64_VIIIfx_2.00GHz.jpg")）\]\] SPARC64は、[HALコンピュータシステム](https://ja.wikipedia.org/wiki/HALコンピュータシステム "wikilink")ならびに富士通が開発したプロセッサファミリであり、SPARCシリーズのハイエンドのプロセッサとなっている。

SPARC64 Vは富士通の[PRIMEPOWER](https://ja.wikipedia.org/wiki/PRIMEPOWER "wikilink")サーバシリーズで、SPARC64 VIおよびSPARC64 VIIは同社とサン・マイクロシステムズの[SPARC Enterprise](../Page/SPARC_Enterprise.md "wikilink") M3000からM9000に使用された。

富士通の[メインフレーム](../Page/メインフレーム.md "wikilink")用[プロセッサと同じ開発者が設計](../Page/CPU.md "wikilink")・開発しているため、メインフレーム用[プロセッサのRAS](../Page/CPU.md "wikilink")（信頼性、可用性、保守性）技術をすべて継承している。[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")、演算器、[レジスタ等](../Page/レジスタ_\(コンピュータ\).md "wikilink")、どの回路でエラーが発生しても必ず検出できるよう、[ECC](../Page/誤り検出訂正.md "wikilink")、[パリティ](../Page/パリティ.md "wikilink")で保護している。エラーが発生すると、[ECC](../Page/誤り検出訂正.md "wikilink")、ハードウェア命令リトライにより訂正を行う。

万一、訂正不可能なエラーが発生しても、正常なコア、[キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")だけで動作し続けることができる。プロセッサの動作を記録する機能も持ち、エラー発生時の原因特定に役立つ。

また、[スーパースケーラ](https://ja.wikipedia.org/wiki/スーパースケーラ "wikilink")、[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")、[ノンブロッキングキャッシュ制御](https://ja.wikipedia.org/wiki/ノンブロッキングキャッシュ制御 "wikilink")、[ハードウェア・プリフェッチ](https://ja.wikipedia.org/wiki/ハードウェア・プリフェッチ "wikilink")等の高速化技術を採用している。

SPARC64 VIおよびSPARC64 VIIでは、[マルチコア](../Page/マルチコア.md "wikilink")・[マルチスレッド対応がなされている](../Page/ハードウェアマルチスレッディング.md "wikilink")。

[2009年](../Page/2009年.md "wikilink")に発表されたSPARC64 VIIIfxはHPC向け製品である。2-Way SMTからシングルスレッドになったが、コア数は4コアから8コアに増えた。また、メモリーコントローラがプロセッサに統合され、新規に開発されたHPC向け命令拡張「HPC-ACE (High Performance Computing - Arithmetic Computational Extensions)」が実装され、レジスタ本数が増加し、[SIMD](../Page/SIMD.md "wikilink")命令が強化された。

SPARC64 VIIIfxは、[2011年](../Page/2011年.md "wikilink")6月、同年11月と2期連続で[TOP500](https://ja.wikipedia.org/wiki/TOP500 "wikilink")リスト首位を獲得した[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")の「[京](https://ja.wikipedia.org/wiki/京_\(スーパーコンピュータ\) "wikilink")」に採用されている\[1\]。

[2011年](../Page/2011年.md "wikilink")に発表されたSPARC64 IXfxはSPARC64 VIIIfxと同じくHPC向け製品である。クロック周波数が2GHzから1.848GHzに低下したものの、コア数は8コアから16コアに倍増し、メモリ帯域も64GB/sから85GB/sと向上している。

SPARC64 IXfxは、富士通のスーパーコンピュータPRIMEHPC FX10（[2011年](../Page/2011年.md "wikilink")[11月7日](../Page/11月7日.md "wikilink")に販売開始、[2012年](../Page/2012年.md "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")より出荷\[2\]\[3\]）に採用されている。

SPARC64 Xは、UNIXサーバ向けプロセッサとして初めてHPC-ACEを実装し、富士通のUNIXサーバSPARC M10（2013年4月10日提供開始\[4\]）に採用された。

SPARC64 X+は、富士通のUNIXサーバSPARC M10（2014年4月8日提供開始\[5\]）に採用されている。SPARC64 Xのクロック周波数が3.0GHzであるのに対し、SPARC64 X+はそれを3.7GHzに向上させたうえで、暗号処理・十進浮動小数点数（[IEEE 754形式とOracle](https://ja.wikipedia.org/wiki/IEEE_754#十進浮動小数点数 "wikilink") NUMBER形式）・データベース処理をサポートする命令が追加された。また、従来不可能であったcall/returnを跨いだアウトオブオーダー処理を可能としている。

### Rock

Rockはサン・マイクロシステムズがかつて自社開発していた、ハイエンド用のマルチコアSPARCモデルの開発コード名である。次期UltraSPARCとも呼ばれた。2007年1月の発表では、最大で16コアを搭載するとされ、2008年後半に提供予定とされた\[6\]。2008年2月のISSCC 2008では、16コアで最大32スレッドを並行実行し、[アウト・オブ・オーダーを採用し](../Page/アウト・オブ・オーダー実行.md "wikilink")、動作周波数2.3GHzを実現するとされたが、提供時期は最適化のために2009年以降へ延期が発表された\[7\]\[8\]。更に2009年6月には、2008年の提供が延期されたのは社内で欠陥が発見されたためであり、開発中止が決定されたと報道された\[9\]\[10\]。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[1月27日](../Page/1月27日.md "wikilink")、サン・マイクロシステムズは[オラクル](https://ja.wikipedia.org/wiki/オラクル "wikilink")に吸収合併され、独立企業・法人としては消滅したがその後もSPARCの開発は人員を補強して続けられた\[11\]。

## 参照

## 外部リンク

  - [SPARC International, inc.](http://www.sparc.org/)（日本語ページあり）
  - [米国Sun Microsystems](http://sun.com/)（英文であるが一部日本のページもある）
  - [サン・マイクロシステムズ](http://jp.sun.com/)
  - [富士通](http://jp.fujitsu.com/)、（[SPARC64V 仕様書](http://primeserver.fujitsu.com/primepower/catalog/ap/)）、（[ホワイトペーパー](http://primeserver.fujitsu.com/primepower/catalog/data/)）

## 関連項目

  - [CPU](../Page/CPU.md "wikilink")
  - [マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")
  - [RISC](../Page/RISC.md "wikilink")

[Category:コンピュータアーキテクチャ](https://ja.wikipedia.org/wiki/Category:コンピュータアーキテクチャ "wikilink") [Category:SPARC_マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:SPARC_マイクロプロセッサ "wikilink") [Category:サン・マイクロシステムズのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズのマイクロプロセッサ "wikilink") [Category:富士通のマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:富士通のマイクロプロセッサ "wikilink") [Category:命令セットアーキテクチャ](https://ja.wikipedia.org/wiki/Category:命令セットアーキテクチャ "wikilink")

1.  馬場敬信『コンピュータアーキテクチャ 改定4版』、オーム社、平成28年11月15日 改定4版 第1刷 発行、、80ページ
2.  [PRIMEHPC FX10 : 富士通](http://jp.fujitsu.com/solutions/hpc/products/primehpc/)
3.  [【PC Watch】 富士通、最大23.2PFLOPSを実現するスパコンを発売 ～京で用いた技術をさらに発展](http://pc.watch.impress.co.jp/docs/news/20111107_489081.html)
4.
5.
6.  [Sun、「Rock」を2008年にリリース](http://www.itmedia.co.jp/enterprise/articles/0701/19/news047.html)
7.  [Sunがサーバー向けハイエンドプロセッサ「Rock」の概要を公表](http://pc.watch.impress.co.jp/docs/2008/0205/isscc02.htm)
8.  [Sun、Rockのリリースを2009年に延期](http://www.itmedia.co.jp/news/articles/0802/07/news052.html)
9.  [「SunがサーバプロセッサRockの開発打ち切り」の報道](http://www.itmedia.co.jp/news/articles/0906/16/news026.html)
10. [Sun Is Said to Cancel Big Chip Project](http://bits.blogs.nytimes.com/2009/06/15/sun-is-said-to-cancel-big-chip-project/) - The New York Times
11.