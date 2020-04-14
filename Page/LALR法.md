> この記事は[LALR法](https://ja.wikipedia.org/wiki/LALR法)から翻訳されています。


**LALR法**（）は、[構文解析](../Page/構文解析.md "wikilink")手法の一種であり、Lookahead（先読み）[LR法](../Page/LR法.md "wikilink")の略である。[単純LR法](../Page/単純LR法.md "wikilink")（SLR法）の[構文解析器](../Page/構文解析器.md "wikilink")よりも多くの[文脈自由文法](../Page/文脈自由文法.md "wikilink")を扱うことができる。[構文解析表](https://ja.wikipedia.org/wiki/構文解析表 "wikilink")の大きさがあまり大きくなく、多くの文法を扱えることから、最も一般的な構文解析器となっている。[yacc](https://ja.wikipedia.org/wiki/yacc "wikilink") や [GNU bison](../Page/Bison.md "wikilink") といった[パーサジェネレータ](../Page/パーサジェネレータ.md "wikilink")の多くもこの種の構文解析器を生成する。

SLR法と同様、LALR法では LR(0) の構文解析表を必要とする。SLR 法では Follow-set を使って reduce アクションを構築するのに対して、LALR法では [Lookahead-set](../Page/先読み.md "wikilink") を使う。Lookahead-set は構文解析により特化している。Follow-set は関連する記号の集合だが、Lookahead-set は[LR(0)アイテムと構文解析状態に特化した集合である](https://ja.wikipedia.org/wiki/LR法#アイテム "wikilink")。

ある LR(0) 文法での状態 `S` におけるアイテム `I` の Follow-set は、文法上 `I` の左辺の非終端記号の後に出現可能な全記号を含む。一方、状態 `S` におけるアイテム `I` の Lookahead-set は、状態 `S` で構文解析を開始したときの `I` の右辺に出現可能な記号のみを含む。*follow*(`I`) は左辺が同じ `I` である全 LR(0)アイテムの Lookahead-set の和集合と等価であり、状態やアイテムの右辺は考慮されていない。従って、Follow-set からは文脈情報が失われている。Lookahead-set は特定の構文解析向けであるため、さらに選別が可能で、Follow-set よりも詳細な識別が可能となる。

## 参考文献

  - Alfred V. Aho, Ravi Sethi, and Jeffrey D. Ullman. *Compilers: Principles, Techniques, and Tools.* Addison--Wesley, 1986. （LALR(1)構文解析器の構築に関する従来からの技法の解説）
  - Frank DeRemer and Thomas Pennello. Efficient Computation of LALR(1) Look-Ahead Sets. *ACM Transactions on Programming Languages and Systems (TOPLAS)* 4:4, pp. 615–649. 1982. （より効率的な LALR(1)構文解析器構築技法の説明）
  - Richard Bornat *Understanding and Writing Compilers*, Macmillan, 1979. （構文解析と構文解析表などの基本原理を解説）

[Category:構文解析アルゴリズム](https://ja.wikipedia.org/wiki/Category:構文解析アルゴリズム "wikilink")