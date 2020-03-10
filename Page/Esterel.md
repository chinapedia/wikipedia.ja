> この記事は[Esterel](https://ja.wikipedia.org/wiki/Esterel)から翻訳されています。


**Esterel** は、複雑な[リアルタイムシステム](https://ja.wikipedia.org/wiki/リアルタイムシステム "wikilink")向けの同期型[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。[命令型プログラミング](../Page/命令型プログラミング.md "wikilink")のスタイルで、[並列性と](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")[プリエンプション](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")を単純に表せる。従って、制御系の設計に非常に適している。

開発は、Gérard Berry に率いられた[パリ国立高等鉱業学校](https://ja.wikipedia.org/wiki/パリ国立高等鉱業学校 "wikilink")と [INRIA](https://ja.wikipedia.org/wiki/INRIA "wikilink") のチームにより、[1980年代](../Page/1980年代.md "wikilink")初めに開始された。現在のコンパイラは、Esterel のソースコードから[C言語](../Page/C言語.md "wikilink")のコードか[レジスタ転送レベル](../Page/レジスタ転送レベル.md "wikilink")のハードウェア記述（[VHDL](https://ja.wikipedia.org/wiki/VHDL "wikilink")か[Verilog](https://ja.wikipedia.org/wiki/Verilog "wikilink")）を生成する。

開発は今も継続している。商用版には統合開発環境 Esterel Studio がある。その開発会社 Esterel Technologies は [IEEE](../Page/IEEE.md "wikilink") での標準化を開始している。現在、[Esterel v7 Reference Manual Version v7 30 – initial IEEE standardization proposal](http://www.esterel-technologies.com/files/Esterel-Language-v7-Ref-Man.pdf) が一般に公開されている。

## 時間の多形記法

Esterel での時間に記法は、非同期言語のそれとは異なる。具体的な時間は順序記述に置き換えられる。そのとき、事象の有無と同時性のみが考慮される。つまり、具体的な時間は特別な役割を持たないことを意味する。これを時間の多形記法（multiform notion of time）と呼ぶ。Esterel は、論理実体を完全に順序付けて並べて記述する。各実体では（0個を含む）任意個数の事象が発生する。同じ論理実体で発生した事象は同時に発生したと見なされる。それ以外の事象は発生した実体によって順序が決定される。文には、時間を消費しない文（実行と完了が同じ実体にあるもの）と、ある一定サイクル数の遅延がある文がある。

## シグナル

シグナルは唯一の通信手段である。シグナルには値付きのものと値無しのものがある。さらに、入力となるシグナル、出力となるシグナル、ローカルなシグナルに分類される。1つのシグナルは、1つの実体において存在するかしないかという属性を持つ。値付きシグナルはさらに値を属性として持つ。シグナルはプログラム全体にブロードキャストされ、任意のプロセスがシグナルを読み書きできる。値付きシグナルの値は、そのシグナルが存在しない場合でも任意の実体が決定できる。シグナルはデフォルト状態では存在せず、明示的に emit 文で存在するようにしない限り、存在しないままである。通信は即時に行われ、あるサイクルで放出されたシグナルは即座に（そのサイクル内で）各プロセスで観測できる。

### シグナル一貫性規則

  - 各シグナルは、1つのサイクルでは存在するかしないかのどちらかであり、両方ということはない。
  - ライターはリーダーが動作する前に動作する。

従って

`present A else`
`    emit A`
`end`

は間違ったプログラムである（シグナル A が存在しない場合、それをブロードキャストする）。

## 言語構文

### 基本的な Estrel の文

:\# `emit S` -- 現在の実体上でシグナル *S* を存在させる。シグナルは emit されるまで存在しない。

:\# `pause` -- 一旦停止し、pause の次のサイクルで実行再開する。

:\# `present S then stmt1 else stmt2 end` -- 現在の実体でシグナル *S* が存在するなら、即座に stmt1 を実行し、さもなくば stmt2 を実行する。

:\# `await S` -- *S* が存在するようになるまで待つ。`await` は通常、サイクルの開始時に *S* の存在をチェックしない（1サイクルは必ず待つ）。 `await immediately` はサイクル開始時にチェックする。

:\# `loop p end` -- *p* を無限に繰り返す。ループ本体の中に `pause` や `await` などがない限り、ループは停止しない。

:\# `p||q` -- *p* と *q* を並行して実行する。全グループが完了したときに完了となる。

### 例 (ABRO)

次のプログラムは、A と B を受信すると同時に O を出力する。R を受信すると振る舞いがリセットされる。

`module ABRO:`
`input A, B, R;`
`output O;`

`loop`
`  [ await A || await B ];`
`  emit O`
`each R`

`end module`

## 利点

  - 時間モデルにより、プログラマは正確な制御が可能
  - 並行性により、制御システムを記述しやすい
  - 完全に決定的な動作
  - 有限状態言語
      - 実行時間が予測可能（[最悪実行時間](../Page/最悪実行時間.md "wikilink")）
      - 形式的な検証が容易（[形式的検証](https://ja.wikipedia.org/wiki/形式的検証 "wikilink")）
  - ソフトウェアとしてもハードウェアとしても実装可能

## 欠点

  - 有限状態性により、言語としての柔軟性が低い（ただし、適用分野における表現能力としては問題ない）
  - 意味論的問題
      - 因果律違反を防ぐのが難しい
      - 一般にコンパイルが困難だが、単純な[正当性検証手法が存在する](https://ja.wikipedia.org/wiki/正当性_\(計算機科学\) "wikilink")

## 外部リンク

  - [Synfora, Inc.](http://www.synfora.com/products/esterelStudio.html)
  - [Esterel Web](http://www-sop.inria.fr/esterel.org/)
  - [The Esterel Language](http://www-sop.inria.fr/meije/esterel/esterel-eng.html)
  - [The Columbia Esterel Compiler: An open-source Esterel compiler](http://www1.cs.columbia.edu/~sedwards/cec/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:組み込みシステム](https://ja.wikipedia.org/wiki/Category:組み込みシステム "wikilink") [Category:ハードウェア記述言語](https://ja.wikipedia.org/wiki/Category:ハードウェア記述言語 "wikilink")