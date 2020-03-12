> この記事は[FASTA](https://ja.wikipedia.org/wiki/FASTA)から翻訳されています。


**FASTA** は、[DNA](../Page/デオキシリボ核酸.md "wikilink") の[塩基配列](../Page/塩基配列.md "wikilink")と[タンパク質の](https://ja.wikipedia.org/wiki/蛋白質 "wikilink")[アミノ酸](https://ja.wikipedia.org/wiki/アミノ酸 "wikilink")配列の[シーケンスアラインメント](../Page/シーケンスアラインメント.md "wikilink")を行うための、[バイオインフォマティクス](../Page/バイオインフォマティクス.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")パッケージである。

FASTA と同様に[シーケンス](https://ja.wikipedia.org/wiki/シーケンス "wikilink")アライメントを行うためのソフトウェアとして、[BLAST](../Page/BLAST.md "wikilink") なども知られる。

最初のバージョンは FASTP という名前であり、デヴィッド・J・リップマンとウィリアム・R・ピアスンが、1985年に開発して論文を発表した\[1\]。

当初はタンパク質のアミノ酸配列の[シーケンスデータベース](https://ja.wikipedia.org/wiki/シーケンスデータベース "wikilink")に対して、アミノ酸配列の類似性 (similarity) の検索を行うように設計された。FASTA の1988年のバージョンでは、DNAの塩基配列の類似性を検索する機能が加えられた\[2\]。FASTA は FASTP よりも精巧なアルゴリズムで処理を行い、統計上の有意性を評価する。FASTA ソフトウェアパッケージには、タンパク質のアミノ酸配列やDNAの塩基配列のアライメントを行うための、いくつかの[プログラムが含まれている](../Page/プログラム_\(コンピュータ\).md "wikilink")。

FASTA は、"FAST-Aye"（ファストエー）と発音する。FASTA は、"FAST-P"（**P**rotein; タンパク質）アライメント と "FAST-N"（**N**ucleotide; [ヌクレオチド](https://ja.wikipedia.org/wiki/ヌクレオチド "wikilink")）アライメント の総称である、"FAST-All" を意味している。

FASTA ソフトウェアパッケージの現在のバージョンでは、次のようなことができる。なお、シーケンス[データベース](../Page/データベース.md "wikilink")に与える検索のシーケンスをクエリーという。

  - 塩基配列クエリーで塩基配列データベースを検索
  - 塩基配列クエリーをアミノ酸配列に翻訳してアミノ酸配列データベースを検索
  - アミノ酸配列クエリーでアミノ酸配列データベースを検索
  - アミノ酸配列クエリーで塩基配列データベース（アミノ酸配列に翻訳）を検索
  - 複数の[ペプチド](https://ja.wikipedia.org/wiki/ペプチド "wikilink")（短いペプチド鎖）をクエリーとしてアミノ酸配列データベースを検索

フレームシフト[突然変異](../Page/突然変異.md "wikilink")を考慮した検索も可能である。Smith-Watermanアルゴリズムを実装した SSEARCH でのシーケンスデータベースの検索・比較をすることもできる（処理速度は遅くなる）。

FASTA ソフトウェアパッケージの主な用途は、類似性の精密な統計値を計算することである。類似性の統計値を計算することにより、生物学者は、どのアライメントが妥当性が高いかを判断することや、[相同](../Page/相同.md "wikilink")性 (homology) を推測することができる。

FASTA ソフトウェアパッケージは、[ヴァージニア大学のFTPサーバから提供されている](../Page/バージニア大学.md "wikilink")。

## FASTAフォーマット

FASTA では、[シーケンス](https://ja.wikipedia.org/wiki/シーケンス "wikilink")データの記述形式として FASTAフォーマットという形式を使う。FASTAフォーマットは[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")である。1つのシーケンスのデータは、"\>" で始まる1行のヘッダ行と、2行目以降の実際のシーケンス文字列で構成される。ヘッダ行では、"\>" の次にシーケンスデータを識別するための文字列を記述し、続けてそのシーケンスデータを説明する文字列を記述する（両方とも省略してよい）。ヘッダ行の "\>" と識別文字列の間にスペースを入れてはいけない。FASTAフォーマットの全ての行は、80文字未満とすることが推奨される。"\>" で始まる別の行が出現すると、そこでシーケンスデータが区切られ、別のシーケンスデータが始まる。

FASTA ファイルフォーマットの例を示す。

`>gi|5524211|gb|AAD44166.1| cytochrome b [Elephas maximus maximus]`
`LCLYTHIGRNIYYGSYLYSETWNTGIMLLLITMATAFMGYVLPWGQMSFWGATVITNLFSAIPYIGTNLV`
`EWIWGGFSVDKATLNRFFAFHFILPFTMVALAGVHLTFLHETGSNNPLGLTSDSDKIPFHPYYTIKDFLG`
`LLILILLLLLLALLSPDMLGDPDNHMPADPLNTPLHIKPEWYFLFAYAILRSVPNKLGGVLALFLSIVIL`
`GLMPFLHTSKHRSMMLRPLSQALFWTLTMDLLTLTWIGSQPVEYPYTIIGQMASILYFSIILAFLPIAGX`
`IENY`

FASTAフォーマットでは、IUB/[IUPAC](../Page/国際純正・応用化学連合.md "wikilink") で規定されている[アミノ酸](https://ja.wikipedia.org/wiki/アミノ酸 "wikilink")コードもしくは[核酸](../Page/核酸.md "wikilink")コードで、シーケンス文字列を記述する。ただし、小文字で記述した場合は FASTA内部で自動的に大文字に変換される。また、"-"（ハイフン）でギャップを、"U" で[セレノシステイン](../Page/セレノシステイン.md "wikilink")を、"\*" で翻訳終止を記述する。FASTAでは、クエリーのシーケンスに数字が含まれていると正しく処理をすることができない。FASTAで処理を行う前に、数字は、除去しておくか、適切な文字列（"N" は不明な核酸塩基、"X" は不明なアミノ酸 を意味する）に置き換えておく必要がある。

| 核酸のコード | 意味                                                                   |
| ------ | -------------------------------------------------------------------- |
| A      | **A**denosine （[アデニン](../Page/アデニン.md "wikilink")）                   |
| C      | **C**ytidine （[シトシン](https://ja.wikipedia.org/wiki/シトシン "wikilink")） |
| G      | **G**uanine （[グアニン](../Page/グアニン.md "wikilink")）                     |
| T      | **T**hymidine （[チミン](../Page/チミン.md "wikilink")）                     |
| U      | **U**racil （[ウラシル](../Page/ウラシル.md "wikilink")）                      |
| R      | G A （pu**R**ine, [プリン](../Page/プリン_\(化学\).md "wikilink")）            |
| Y      | T C （p**Y**rimidine, [ピリミジン](../Page/ピリミジン.md "wikilink")）           |
| K      | G T （**K**etone, [ケトン](../Page/ケトン.md "wikilink")）                   |
| M      | A C （a**M**ino group, [アミノ基](../Page/アミン.md "wikilink")）             |
| S      | G C （**S**trong interaction, 強い[結合](../Page/水素結合.md "wikilink")）     |
| W      | A T （**W**eak interaction, 弱い結合）                                     |
| B      | G T C (not A) （**B**, A の次の文字）                                       |
| D      | G A T (not C) （**D**, C の次の文字）                                       |
| H      | A C T (not G) （**H**, G の次の文字）                                       |
| V      | G C A (not T, not U) （**V**, U の次の文字）                                |
| N      | A G C T （a**N**y, 不明）                                                |
| \-     | ギャップ                                                                 |

FASTA で使える核酸のコード

| アミノ酸コード | 意味                                                                                   |
| ------- | ------------------------------------------------------------------------------------ |
| A       | [アラニン](../Page/アラニン.md "wikilink")                                                   |
| B       | [アスパラギン酸](../Page/アスパラギン酸.md "wikilink") もしくは [アスパラギン](../Page/アスパラギン.md "wikilink") |
| C       | [システイン](../Page/システイン.md "wikilink")                                                 |
| D       | [アスパラギン酸](../Page/アスパラギン酸.md "wikilink")                                             |
| E       | [グルタミン酸](../Page/グルタミン酸.md "wikilink")                                               |
| F       | [フェニルアラニン](../Page/フェニルアラニン.md "wikilink")                                           |
| G       | [グリシン](../Page/グリシン.md "wikilink")                                                   |
| H       | [ヒスチジン](../Page/ヒスチジン.md "wikilink")                                                 |
| I       | [イソロイシン](https://ja.wikipedia.org/wiki/イソロイシン "wikilink")                            |
| K       | [リシン](../Page/リシン.md "wikilink")                                                     |
| L       | [ロイシン](../Page/ロイシン.md "wikilink")                                                   |
| M       | [メチオニン](https://ja.wikipedia.org/wiki/メチオニン "wikilink")                              |
| N       | [アスパラギン](../Page/アスパラギン.md "wikilink")                                               |
| P       | [プロリン](../Page/プロリン.md "wikilink")                                                   |
| Q       | [グルタミン](../Page/グルタミン.md "wikilink")                                                 |
| R       | [アルギニン](../Page/アルギニン.md "wikilink")                                                 |
| S       | [セリン](../Page/セリン.md "wikilink")                                                     |
| T       | [スレオニン](https://ja.wikipedia.org/wiki/トレオニン "wikilink")                              |
| U       | [セレノシステイン](../Page/セレノシステイン.md "wikilink")                                           |
| V       | [バリン](../Page/バリン.md "wikilink")                                                     |
| W       | [トリプトファン](../Page/トリプトファン.md "wikilink")                                             |
| Y       | [チロシン](../Page/チロシン.md "wikilink")                                                   |
| Z       | [グルタミン酸](../Page/グルタミン酸.md "wikilink") もしくは [グルタミン](../Page/グルタミン.md "wikilink")     |
| X       | 不明 (any)                                                                             |
| \*      | 翻訳終止                                                                                 |
| \-      | ギャップ                                                                                 |

FASTA で使えるアミノ酸コード

## 参考文献

<references />

## 外部リンク

  - [FASTAフォーマットの説明（英語）](http://www.ncbi.nlm.nih.gov/BLAST/fasta.shtml)
  - [ヴァージニア大学のFASTAサーバ](http://fasta.bioch.virginia.edu/fasta_www2/fasta_down.shtml) - FASTAソフトウェアパッケージを配布している
  - [GenBank to Fasta conventer](http://gp2fasta.ovh.org/)

[Category:バイオインフォマティクス](https://ja.wikipedia.org/wiki/Category:バイオインフォマティクス "wikilink")

1.  Lipman, D. J.; Pearson, W.R. (1985). "Rapid and sensitive protein similarity searches." *Science* **227** (4693): 1435–1441. PMID 2983426.
2.  Pearson, W.R.; Lipman, D. J. (1988). "Improved tools for biological sequence comparison." *Proc. Natl. Acad. Sci. USA* **85** (8): 2444–2448. PMID 3162770