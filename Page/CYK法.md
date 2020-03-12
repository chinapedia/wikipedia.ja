> この記事は[CYK](https://ja.wikipedia.org/wiki/CYK)から翻訳されています。


**CYK法**（）は、ある[文字列](../Page/文字列.md "wikilink")が与えられた[文脈自由文法](../Page/文脈自由文法.md "wikilink")で生成できるかを決め、生成できる場合の生成方法を求める[アルゴリズム](../Page/アルゴリズム.md "wikilink")である。CYK は **Cocke-Younger-Kasami** の略（それぞれ、RISCの先駆と言われる[801などでも知られる](../Page/IBM_801.md "wikilink")[ジョン・コック](../Page/ジョン・コック.md "wikilink")、Daniel Younger、[嵩忠雄](https://ja.wikipedia.org/wiki/嵩忠雄 "wikilink")である）。文脈自由文法の[構文解析](../Page/構文解析.md "wikilink")手法と捉えることもできる。このアルゴリズムは一種の[動的計画法](../Page/動的計画法.md "wikilink")である。

標準的なCYK法は、[チョムスキー標準形](../Page/チョムスキー標準形.md "wikilink")で書かれた文脈自由文法で定義される言語を認識する。任意の文脈自由文法をチョムスキー標準形に書き換えるのはそれほど困難ではないので、CYK法は任意の文脈自由文法の認識に使うことができる。CYK法を拡張してチョムスキー標準形で書かれていない文脈自由文法を扱うようにすることも可能である。これにより性能は向上するが、アルゴリズムを理解することは難しくなる。

CYK法の最悪時間計算量は [Θ](../Page/ランダウの記号.md "wikilink")(n<sup>3</sup>) であり、*n* は解析対象の文字列の長さである。従って、CYK法は任意の文脈自由言語を認識できる最も効率的なアルゴリズムの1つである。ただし、文脈自由言語の特定のサブセットについて、より効率の良いアルゴリズムが他に存在する。

## アルゴリズム

CYK法は[ボトムアップ構文解析](../Page/ボトムアップ構文解析.md "wikilink")アルゴリズムであり、文脈自由言語のメンバシップ問題が[決定可能であることを構成的に証明できることから](https://ja.wikipedia.org/wiki/決定問題 "wikilink")、理論的にも重要である。

メンバシップ問題についてのCYK法は次の通り。

**`Let`**` `*`n`*` 文字 `*`a`*<sub>`1`</sub>` ... `*`a`*<sub>*`n`*</sub>` からなる文字列を入力する。`
**`Let`**` 文法は `*`r`*` 個の非終端記号 `*`R`*<sub>`1`</sub>` ... `*`R`*<sub>*`r`*</sub>` からなる。`
`この文法には開始記号を含む部分集合 R`<sub>`s`</sub>` が含まれる。`
**`Let`**` P[n,n,r] をブーリアン型の配列とする。P の全要素を false で初期化する。`
**`For``   ``each`**` i = 1 to n`
`  `**`For``   ``each`**` 生成規則 R`<sub>`j`</sub>` → a`<sub>`i`</sub>` があるなら、`**`set`**` P[i,1,j] = true.`
**`For``   ``each`**` i = 2 to n -- 範囲の長さ`
`  `**`For``   ``each`**` j = 1 to n-i+1 -- 範囲の開始位置`
`    `**`For``   ``each`**` k = 1 to i-1 -- 範囲の区分`
`      `**`For``   ``each`**` 生成規則 R`<sub>`A`</sub>` -> R`<sub>`B`</sub>` R`<sub>`C`</sub>
`        `**`If`**` P[j,k,B] and P[j+k,i-k,C] `**`then`**` set P[j,i,A] = true`
**`If`**` P[1,n,x] のいずれかが true （x は集合 s について反復される。s は R`<sub>`s`</sub>` の全てのインデックスの集合）`
`  `**`Then`**` 文字列は言語のメンバーである。`
`  `**`Else`**` 文字列は言語のメンバーではない。`

### 解説

形式的でない説明をするなら、このアルゴリズムは単語の並びについて、考えられるあらゆる組合せを考慮し、与えられた文字列の i 番目から長さ j の並びが R<sub>k</sub> から生成される場合に P\[i,j,k\] を true にセットする。長さ 1 の並びを検討したら、次に長さ 2 の並びというように検討していく。長さ 2 以上の並びの場合、その並びを2つに分け（分け方を様々に変えて）、P → Q R という生成規則で Q と R がその並びの前半部分と後半部分にマッチするかどうかを調べる。マッチする場合、P をその並び全体にマッチするものとして記録する。この一連の処理が完了すると、入力文字列全体を含む記号の並びが開始記号から生成されるかどうかが判定できる。

|       |
| ----- |
| **S** |
|       |
|       |
| **S** |
|       |
| **S** |
| NP    |
| she   |

CYK テーブル

### 拡張

このアルゴリズムを、文が言語に含まれるかどうかを決定するだけでなく、[構文木](https://ja.wikipedia.org/wiki/構文木 "wikilink")を構築するよう拡張するには、構文木のノードをブーリアンの代わりに配列の要素として格納すればよい。認識しようとする文法は曖昧な場合があるので、ノードのリストを格納する必要がある（可能な解釈からひとつだけ選べばよい場合はその限りではない）。従って、結果として複数の構文木が得られる。別の方式としては、*backpointers* と呼ばれる第二のテーブル B\[n,n,r\] を使う方式もある。

[加重文脈自由文法](https://ja.wikipedia.org/wiki/加重文脈自由文法 "wikilink")や[確率文脈自由文法](../Page/確率文脈自由文法.md "wikilink")を使って文字列の構文解析をするよう拡張することも可能である。この場合、加重や確率はテーブル P にブーリアンの代わりに格納される。すなわち、P\[i,j,A\] は i から長さ j の並びが A から生成される最小加重（または最大確率）を格納する。さらにアルゴリズムを拡張すれば、あらゆる加重（確率）の構文木を列挙できる。

## 関連項目

  - [チャートパーサ](https://ja.wikipedia.org/wiki/チャートパーサ "wikilink") - [アーリー法](../Page/アーリー法.md "wikilink")
  - [GLR法](../Page/GLR法.md "wikilink")
  - [パックラット構文解析](https://ja.wikipedia.org/wiki/パックラット構文解析 "wikilink")

## 参考文献

  - [John Cocke](../Page/ジョン・コック.md "wikilink") and Jacob T. Schwartz (1970). Programming languages and their compilers: Preliminary notes. Technical report, Courant Institute of Mathematical Sciences, New York University.
  - T. Kasami (1965). An efficient recognition and syntax-analysis algorithm for context-free languages. Scientific report AFCRL-65-758, Air Force Cambridge Research Lab, Bedford, MA.
  - Daniel H. Younger (1967). Recognition and parsing of context-free languages in time *n*<sup>3</sup>. *Information and Control* 10(2): 189–208.

[Category:構文解析アルゴリズム](https://ja.wikipedia.org/wiki/Category:構文解析アルゴリズム "wikilink")