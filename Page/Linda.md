> この記事は[Linda](https://ja.wikipedia.org/wiki/Linda)から翻訳されています。


**Linda** は、並列[プログラミング言語](../Page/プログラミング言語.md "wikilink")であり、[Prolog](https://ja.wikipedia.org/wiki/Prolog "wikilink")、[C言語](../Page/C言語.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などの他の（逐次的）言語上に拡張として実装される。

## 概要

[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")と[プログラミング言語](../Page/プログラミング言語.md "wikilink")の関わりを考えたとき、いくつかの手法が考えられる。まず、言語を並列処理向きに一から設計する手法である。例えば、[CSPに基づいた](https://ja.wikipedia.org/wiki/Communicating_Sequential_Process "wikilink") [Occam](https://ja.wikipedia.org/wiki/Occam "wikilink") などがある。第二に既存の言語に並列処理モデルを導入して新たな言語を構築する手法である。例えば、Multilisp、Concurrent Smalltalk などがある。第三に並列化を言語仕様とは別の部分で実現する手法である。例えば、[コンパイラ](../Page/コンパイラ.md "wikilink")によって並列処理を実現する。

Linda はこれらとは異なるアプローチであり、既存の言語仕様に修正を加えずに協調モデル（coordination model）を付加することで並列処理を実現する。このため Linda は「協調言語（coordination language）」とも呼ばれ、並列性のない言語で書かれたアプリケーション間の協調動作にのみ注目している。Linda のモデルでは、タプルスペース（tuplespace）と呼ばれる概念上の共有メモリ上で型つきのデータレコード（[タプル](https://ja.wikipedia.org/wiki/タプル "wikilink")）をそこに格納する。タプルスペースは以下の5つの単純な操作でアクセスされる。

  - out :[プロセス](../Page/プロセス.md "wikilink")からタプルスペースにタプルを出力する。
    in :タプルスペースからタプルを削除し、それをプロセスに返す。必要なタプルが見つからない場合はブロックされ、待つことになる。
    rd :タプルスペースからタプルをコピーし、それをプロセスに返す。必要なタプルが見つからない場合はブロックされ、待たされる。
    inp :in のブロックされない形式。必要なタプルがない場合はエラーを返す。
    rdp :rd のブロックされない形式。

タプルスペースからタプルを取り出す操作は、一種の[連想メモリ](https://ja.wikipedia.org/wiki/連想メモリ "wikilink")のように行う。つまり、タプルの一部のフィールドの値を指定して、それにマッチするタプルを取り出す。これにより、本来関係のないプロセス間でデータをやり取りできる。

## 歴史と実装

[イェール大学](../Page/イェール大学.md "wikilink")の David Gelernter と Nicholas Carriero が1980年代半ばに開発した。協調言語（coordination language）という用語は1992年の彼らの論文で初めて使われた。彼らは並列プログラミングを、計算のアルゴリズムを扱う計算モデルと、プロセス間の通信や同期を扱う協調モデルに分けて考えた。当初、注目を浴びた Linda だが、1990年代半ばには興味が薄れていた。しかし、1990年代後半になって、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") に Linda を実装する例が見られるようになった。

Linda の実装としては、[Prolog](https://ja.wikipedia.org/wiki/Prolog "wikilink")、[Ruby](../Page/Ruby.md "wikilink")（Rinda）、[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink"), Java（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が Java 向けに Linda を規定した [JavaSpaces](http://www.wakhok.ac.jp/~maruyama/summer99/node62.html) 仕様）などがある。[IBM](../Page/IBM.md "wikilink")も似たような仕様として [TSpaces](http://www.almaden.ibm.com/cs/TSpaces/) を持っている。

また、Linda を独立した言語処理系として実装する者も出てきた。例えば、[Ease](https://ja.wikipedia.org/wiki/Ease "wikilink") という言語は Steven Ericsson-Zenith が設計した Linda 風の並列処理言語である。

言語の名称は、[Ada](../Page/Ada.md "wikilink") が[エイダ・ラブレス](../Page/エイダ・ラブレス.md "wikilink")にちなんでいるのにあやかって、ポルノ映画『[ディープ・スロート](https://ja.wikipedia.org/wiki/ディープ・スロート_\(映画\) "wikilink")』の主演女優[リンダ・ラブレースにちなんだものだという](https://ja.wikipedia.org/wiki/リンダ・ラヴレース "wikilink")\[1\]。

## 参考文献

  -
  -
## 脚注

<references />

## 外部リンク

  - [Linda for Prolog](http://www.sics.se/sicstus/docs/3.7.1/html/sicstus_29.html)
  - [Linda for C](http://www.comp.nus.edu.sg/~wongwf/linda.html)
  - [Linda for Java](http://www.cs.bris.ac.uk/Publications/Papers/2000380.pdf)
  - [Rinda (for Ruby)](http://segment7.net/projects/ruby/drb/rinda/)
  - [PyLinda for Python](http://www-users.cs.york.ac.uk/aw/pylinda/)
  - [Linda for C++](https://github.com/aeri/Boreas)

[Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.