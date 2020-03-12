> この記事は[Mesa](https://ja.wikipedia.org/wiki/Mesa)から翻訳されています。


**Mesa**（メサ）は、[Xeroxが](../Page/ゼロックス.md "wikilink")1970年代に開発した[強い型付け](https://ja.wikipedia.org/wiki/強い型付け "wikilink")を持つ汎用の[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。

## 概要

Mesa言語は1974年に基本的な言語仕様が決定され、[Alto](../Page/Alto.md "wikilink")上で処理系が制作された\[1\]。なお、Altoそのもののソフトウェアは主に[BCPL](../Page/BCPL.md "wikilink")で書かれていた\[2\]\[3\]。[Xerox StarワークステーションのOSであるPilotはMesaで書かれた](../Page/Xerox_Star.md "wikilink")\[4\]。

言語の特徴としては[モジュール](../Page/モジュール.md "wikilink")化、[静的な型チェック](https://ja.wikipedia.org/wiki/静的型付け "wikilink")、[並行処理と共有変数のロック](../Page/並行計算.md "wikilink")・アンロック、シグナル（[例外処理](../Page/例外処理.md "wikilink")）などがある\[5\]\[6\]。

[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")は1976年から翌年にかけて[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")で過ごした。ヴィルトの[Lilith](../Page/Lilith.md "wikilink")ワークステーションと[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")言語はそれぞれAltoとMesaの強い影響を受けている\[7\]。

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")言語のモニタを使った並行処理はMesaに由来する\[8\]。

## 文法

### 基本構文

Mesa言語は大文字と小文字を区別し、大文字のみの[識別子](../Page/識別子.md "wikilink")は予約されている。[予約語](../Page/予約語.md "wikilink")や定義ずみの識別子はすべて大文字で書かれる\[9\]。

[コメントは](../Page/コメント_\(コンピュータ\).md "wikilink") -- から行末、または次の -- が現れるまでである。

型宣言はPascalとよく似ており、基本型(INTEGER, CARDINAL, BOOLEAN, CHARACTER, LONG INTEGER, LONG CARDINAL, REAL)、[数え上げ型](../Page/列挙型.md "wikilink")、[サブレンジ型](../Page/派生型.md "wikilink")、[配列](../Page/配列.md "wikilink")型、配列記述子（動的配列）型、レコード型、[ポインタ型](../Page/ポインタ_\(プログラミング\).md "wikilink")、手続き型などがある\[10\]。型宣言をすることもできる。Mesaは静的な型付けの言語であるが、それをすりぬけるためのUNSPECIFIED（1ワードの何でもはいる型）とLOOPHOLE組み込み手続きを使った型変換がサポートされている。定義ずみのSTRING型（レコード型へのポインタ）がある。

Pascalでいう集合型はないが、範囲を指定する演算子があり、範囲チェックやSELECTの選択肢、[FORループの条件などに使うことができる](https://ja.wikipedia.org/wiki/for文 "wikilink")。

代入やIF、SELECTなどは文としても式としても存在する。

[ブロックはBEGINとENDで囲まれ](../Page/ブロック_\(プログラミング\).md "wikilink")、ALGOLと同様に中で変数などを宣言できる。ほかに[ループ用のDO](../Page/ループ_\(プログラミング\).md "wikilink")..ENDLOOPがある。

### モジュール

[モジュール](../Page/モジュール.md "wikilink")は分割コンパイルの単位で、インターフェースモジュールと実装モジュールがあり、これによって異なるモジュールの間で静的な型チェックができるようになった\[11\]。あるプログラムからモジュールを使用する場合、DIRECTORY節によって使用するモジュールを指定する。

実行時には各実装モジュールに対してフレーム（インスタンス）が生成される。NEWを使って実行時にフレームのコピーを生成することもできる\[12\]。

### 並行処理

Mesaは[コルーチン](../Page/コルーチン.md "wikilink")をサポートしている。PORTという型があり、手続きのように呼びだすことである手続きまたはモジュールから制御を移すことができる。

また、FORKを使って手続きを非同期に走らせることもできる。

複数のプロセスの[排他制御](../Page/排他制御.md "wikilink")のためには[モニタというモジュールの一種を作り](../Page/モニタ_\(同期\).md "wikilink")、そこで条件変数を定義することができる。条件変数はNOTIFYすることでロックがかかり、WAITでロックがはずれる。

## 開発環境

Mesaは単なる言語というだけでなく、[デバッガ](../Page/デバッガ.md "wikilink")などを含めたマルチウィンドウの[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")を持っている\[13\]。この統合開発環境は1980年に作られた\[14\]。

## 脚注

## 参考文献

  - (pdf, html 脚注では「Manual」と略記)

  -
  -
[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink")

1.
2.
3.
4.  上谷(1986) p.53
5.  ManualのAbstract
6.  上谷(1986) pp.53-54
7.
8.
9.  Manual p.5
10. 上谷(1986) p.266
11. Sweet (1985) p.217
12. 上谷 (1986) pp.262-265
13. 上谷 (1986) p.270
14. Sweet (1985) p.217