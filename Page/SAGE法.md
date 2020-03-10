> この記事は[SAGE](https://ja.wikipedia.org/wiki/SAGE)から翻訳されています。


**SAGE法** (Serial Analysis of Gene Expression) とは、対象とする[細胞](../Page/細胞.md "wikilink")や[組織における](../Page/組織_\(生物学\).md "wikilink") [mRNA](../Page/伝令RNA.md "wikilink") の発現状況を把握する、いわゆる遺伝子発現プロファイリングのための[分子生物学](../Page/分子生物学.md "wikilink")的手法である。

この技術は[ジョンズ・ホプキンス大学](https://ja.wikipedia.org/wiki/ジョンズ・ホプキンス大学 "wikilink")の[がんセンターに勤務していた](../Page/悪性腫瘍.md "wikilink") [Victor Velculescu](https://ja.wikipedia.org/wiki/:en:Victor_Velculescu "wikilink") 博士によって開発され、1995年に[サイエンス](https://ja.wikipedia.org/wiki/サイエンス "wikilink")誌に掲載された\[1\]。それ以降幾つかの派生的手法が報告されているが、有名な改良版としては LongSAGE\[2\] や [SuperSAGE](https://ja.wikipedia.org/wiki/:en:SuperSAGE "wikilink")\[3\] などが挙げられる。特に後者は 25-27 [塩基対の長いタグを用いることで](../Page/核酸.md "wikilink")、[遺伝子](https://ja.wikipedia.org/wiki/遺伝子 "wikilink")の正確な[アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")や[ゲノム](../Page/ゲノム.md "wikilink")からの新規遺伝子のより確実な発見を可能にする技術である。

## 手順の概要

SAGE法の流れは以下の通り。

1.  [腫瘍](https://ja.wikipedia.org/wiki/腫瘍 "wikilink")などの試料から mRNA を単離する。
2.  単離した mRNA の特定の位置から十～数十塩基対の配列（SAGEタグ）を分離する。
3.  SAGEタグ連結してある程度の長さの配列（コンカテマー）を作成する。
4.  コンカテマーを[ベクターに挿入し](../Page/ベクター_\(遺伝子工学\).md "wikilink")、[バクテリア](https://ja.wikipedia.org/wiki/バクテリア "wikilink")に導入して[クローニング](../Page/クローニング.md "wikilink")する。
5.  [DNAシークエンシング](https://ja.wikipedia.org/wiki/DNAシークエンシング "wikilink")を行って配列を決定する。
6.  読まれた配列からそれぞれのSAGEタグを計数し、データを分析して発現状況を調べる。

より詳細な説明は[欧州分子生物学研究所](https://ja.wikipedia.org/wiki/欧州分子生物学研究所 "wikilink")（EMBL）のサイト\[4\]を参照。 また、[CDNA](https://ja.wikipedia.org/wiki/CDNA "wikilink")の項に、類似手法が列記されている。

## 分析

SAGE法によって得られるデータは、短いSAGEタグの配列とそのカウント数の対応表である。タグの配列は[BLAST](https://ja.wikipedia.org/wiki/BLAST "wikilink")などの[データベース](../Page/データベース.md "wikilink")検索によって、出所となった mRNA （にコードされている遺伝子）と対応付けられる。

| SAGEタグ     | カウント数 | 対応する遺伝子                                    |
| ---------- | ----- | ------------------------------------------ |
| ATATTGTCAA | 5     | translation elongation factor 1 gamma      |
| AAATCGGAAT | 2     | T-complex protein 1, z-subunit             |
| ACCGCCTTCG | 1     | no match                                   |
| GCCTTGTTTA | 81    | rpa1 mRNA fragment for r ribosomal protein |
| GTTAACCATC | 45    | ubiquitin 52-AA extension protein          |
| CCGCCGTGGG | 9     | SF1 protein (SF1 gene)                     |
| TTTTTGTTAA | 99    | NADH dehydrogenase 3 (ND3) gene            |
| GCAAAACCGG | 63    | rpL21                                      |
| GGAGCCCGCC | 45    | ribosomal protein L18a                     |
| GCCCGCAACA | 34    | ribosomal protein S31                      |
| GCCGAAGTTG | 50    | ribosomal protein S5 homolog (M(1)15D)     |
| TAACGACCGC | 4     | BcDNA.GM12270                              |

SAGE法によるデータの例（EMBL\[5\]より引用・一部翻訳）

このようなデータに対してさらに[統計学](../Page/統計学.md "wikilink")的な手法が用いられ、異なる試料間での遺伝子発現状況の比較が行われる。例えば病理組織と正常な組織を比較して、患部で多く発現する遺伝子を把握するなどの用途に利用される。SAGE法は元々がんの研究のためのものだったが、現在では他の病気や様々な生物・組織の[トランスクリプトーム](https://ja.wikipedia.org/wiki/トランスクリプトーム "wikilink")解析に利用されている。

## DNAマイクロアレイとの比較

SAGE法と同様に遺伝子発現プロファイリングに用いられる技術としては[DNAマイクロアレイ](https://ja.wikipedia.org/wiki/DNAマイクロアレイ "wikilink")がある。しかしSAGE法はDNAシークエンシングに基づく技術であり、[蛍光](https://ja.wikipedia.org/wiki/蛍光 "wikilink")強度という[アナログ](../Page/アナログ.md "wikilink")で定性的なデータを生む[ハイブリダイゼーションとは異なる](https://ja.wikipedia.org/wiki/DNA_-_DNA分子交雑法 "wikilink")。またDNAマイクロアレイではアレイに用いる遺伝子の配列を解読しておかねばならないが、SAGE法では実験者が前もって mRNA の配列を知っておく必要は無い。そのためSAGE法は探索的であり、新奇の遺伝子が発見される可能性がある。コストの面ではDNAマイクロアレイの方がずっと有利であるが、一般にSAGE法ではそれほど大規模な解析は行われない。

## 出典

<div class="references-small" lang="en" xml:lang="en">

<references />

</div>

## 参考文献

  - [Oncology Centre at Johns Hopkins University](http://www.hopkinsmedicine.org/academics/oncology.html)

## 外部リンク

  - [標準技術集（核酸の増幅および検出）データベース:発現する遺伝子の同定](http://www.jpo.go.jp/shiryou/s_sonota/hyoujun_gijutsu/kakusan/0030.html) （[特許庁](../Page/特許庁.md "wikilink")）
  - [SAGEnet](http://www.sagenet.org) （英語）
  - [A review of the SAGE technique at the Science Creative Quarterly](http://www.scq.ubc.ca/?p=294) （英語）

[Category:分子生物学](https://ja.wikipedia.org/wiki/Category:分子生物学 "wikilink") [Category:分子生物学的技法](https://ja.wikipedia.org/wiki/Category:分子生物学的技法 "wikilink")

1.   PMID 7570003
2.   PMID 11981567
3.   15617519
4.  [SAGE for Beginners](http://www.embl-heidelberg.de/info/sage/)
5.