> この記事は[LFM](https://ja.wikipedia.org/wiki/LFM)から翻訳されています。


**LFM(Leniar Filtering Method)**とは、[データ](../Page/データ.md "wikilink")の[成分分解法](https://ja.wikipedia.org/wiki/成分分解法 "wikilink")を採用した[データ](../Page/データ.md "wikilink")構造である FAST構造を処理する[アルゴリズム](../Page/アルゴリズム.md "wikilink")群（特許取得済み）の総称。

従来のレコード単位処理に対し、全く新たな概念「ファイル単位一括オン[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")ー処理」を実現し、 64ビット、[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")ー大容量化、[マルチコア](../Page/マルチコア.md "wikilink")、超並列時代に適合した[データ](../Page/データ.md "wikilink")超高速並列処理技術である。

## 特徴

  - PC（[マルチコア](../Page/マルチコア.md "wikilink")）から[サーバ](../Page/サーバ.md "wikilink")（[SMP](../Page/対称型マルチプロセッシング.md "wikilink")、[マルチコア](../Page/マルチコア.md "wikilink")）[CELL](../Page/Cell_Broadband_Engine.md "wikilink")・[パラレル](../Page/パラレル.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")に適用可能
  - 数百行小規模[データ](../Page/データ.md "wikilink")から大規模約21億行（32ビット行カウンタ）まで、普遍的、統一的に処理
  - 世界で初めて、[プログラミングインデペンデントで](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")[データ](../Page/データ.md "wikilink")処理の並列化を実現
  - 大規模テーブル（表）[データ](../Page/データ.md "wikilink")を、ビジュアル、インタラクティブに高速に処理
  - [ソート](../Page/ソート.md "wikilink")、ジョイン、検索、抽出、集計、計算、等々各種[データ](../Page/データ.md "wikilink")加工処理を関数化して一括処理
  - 中間[ファイル用Disc不要](../Page/ファイル_\(コンピュータ\).md "wikilink")；高コストのDiscドライブを大幅に削減（1/20～1/100）
  - [バッチ処理](../Page/バッチ処理.md "wikilink")時間の大幅短縮により[CPU](../Page/CPU.md "wikilink")数、システム運用コストの大幅削減実現

## 性能値

6種のFASTがあると公表されている。

| 種別                                                  | モデル   | プリセッサコア数([SPU](../Page/SPU.md "wikilink")数) | テーブル最大行数 | 性能指標        |
| --------------------------------------------------- | ----- | ------------------------------------------- | -------- | ----------- |
| [SMP](../Page/対称型マルチプロセッシング.md "wikilink")&マルチコア    | 1/3MS | 2,8,64                                      | 21億      | 2-40        |
| Parallel                                            | 3/5   | 64、2の20乗                                    | 21億      | 1200-400000 |
| [CELL](../Page/Cell_Broadband_Engine.md "wikilink") | 3/5MS | 64、72                                       | 21億      | 100-300     |

FASTモデル(表形式)

  - 1億行のテーブル(値は1億通り)をソートするのに40秒掛かる時に‘1’となる
  - FASTモデル(ツリー系)の 2/4MS,4/6,4/6MSに関しては、性能値未発表

## 参考文献

  - [汎用超高速データベース処理技術](http://www.creage.ne.jp/app/BookDetail?isbn=4902721015)
  - [超高速DBアルゴリズムの超並列環境下のシミュレータ開発](https://www.ipa.go.jp/SPC/report/02fy-pro/report/818/paper.pdf)

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink")