> この記事は[CLU](https://ja.wikipedia.org/wiki/CLU)から翻訳されています。


**CLU** は、[1974年](../Page/1974年.md "wikilink")から[1975年](../Page/1975年.md "wikilink")にかけて[MITの](../Page/マサチューセッツ工科大学.md "wikilink")[バーバラ・リスコフ](../Page/バーバラ・リスコフ.md "wikilink")が学生らと共に開発した[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。[抽象データ型](https://ja.wikipedia.org/wiki/抽象データ型 "wikilink")のコンストラクタ（操作コードを含む）を備えており、[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")への重要なステップとなった。しかし、それ以外のオブジェクト指向の機能は欠けているか不完全であり、継承もなく、文法が扱いにくいことが欠点であった。CLU と Alphard はどちらも完全なオブジェクト指向言語となる可能性を秘めていたが、実際にはそうならなかった。

## クラスター

CLU の文法は他の多くの言語と同様 [ALGOL](../Page/ALGOL.md "wikilink") に基づいていた。重要な追加点として「クラスター; cluster」がある。クラスターとは、CLU の型拡張システムであり、言語名の由来でもある（CLUster）。クラスターは現在のオブジェクト指向言語で言えば「オブジェクト」にほぼ相当し、似たような文法（構文）であった。以下に[複素数](../Page/複素数.md "wikilink")を実装した CLU のクラスターの例を示す:

``` text
     complex_number = cluster is add, subtract, multiply, ....
          rep = record [ real_part: real, imag_part: real ]
          add = proc ... end add;
          subtract = proc ... end subtract;
          multiply = proc ... end multiply;
          ...
     end complex_number;
```

クラスターは当時としては最新の構造化プログラミングを実現していたが、CLU はクラスター自体には全く構造を提供していない。クラスター名はグローバルであり、クラスターをグループ化するための[名前空間](../Page/名前空間.md "wikilink")機構も無く、クラスター内にクラスターをローカルに作ることもできない。このような問題は CLU に限ったことではない。ALGOLでの変数のスコープを何故クラスターやオブジェクトにも拡張しなかったのかは定かではない。

CLU は暗黙の型変換をしない。クラスターでは、明示的型変換 'up' と 'down' で抽象データ型とその実体との変換をする。汎用型 'any' が用意されていて、プロシージャ force\[\] でオブジェクトが所定の型であるかチェックする。オブジェクトは可変（mutable）と不変（immutable）があり、整数などの基本型は後者に含まれる。

## その他の特徴

もう1つの CLU の型システムでの重要な機能は「[イテレータ](../Page/イテレータ.md "wikilink"); iterators」である。これは、集合からオブジェクトを順次取り出すものである。イテレータは[ブラックボックス](https://ja.wikipedia.org/wiki/ブラックボックス "wikilink")であり、集合内のオブジェクトが何であるかを気にしない[APIを提供する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。つまり、複素数の集合のイテレータと整数の集合のイテレータには区別がない。イテレータは最近の言語では一般的機能となっている。

CLU は他の言語での様々な試みに基づいた[例外処理](../Page/例外処理.md "wikilink")も備えている。例外は `signal` を使って発生させられ、`except` で処理される。型の設計が重視されているにも関わらず、CLU には[列挙型](../Page/列挙型.md "wikilink")がなく、列挙型を作る方法もなかった。

CLU の特殊な機能として、多重代入がある。代入記号の左辺に複数の変数を書くことができる。例えば、`x,y = y,x` というコードで `x` と `y` の値を入れ替えることができる。同様に関数は複数の値を返すことができ、`x,y,z = f(t)` などと記される。

CLU プログラム内のオブジェクトは全てヒープにあり、メモリ管理は自動的に行われる。

## その他

  - 1982年の映画『[トロン](https://ja.wikipedia.org/wiki/トロン_\(映画\) "wikilink")』で、[ジェフ・ブリッジス](../Page/ジェフ・ブリッジス.md "wikilink")演じる Kevin Flynn のプログラムアバターの名前が Clu であった。

## 他のプログラミング言語への影響

  - [Python](../Page/Python.md "wikilink") と [Ruby](../Page/Ruby.md "wikilink") は CLU の影響を受けている（例えば、*yield* 文や多重代入）。
  - CLU は [Ada](../Page/Ada.md "wikilink") と共に C++ のテンプレートに影響を与えた。
  - CLU の例外処理機構は Java や C++ などの新しい言語に影響を与えた。
  - CLU プログラム内の全オブジェクトはヒープ内にあり、メモリ管理は自動的に行われる。Java に直接的な影響を与えた。
  - [Python](../Page/Python.md "wikilink") の generator や [C\#](../Page/C_Sharp.md "wikilink") の iterator の起源は CLU の *iterators* である。

## 文献

  - ビューティフルコード Brian Kernighanほか オライリージャパン ISBN 9784873113630

## 外部リンク

  - [CLU Home Page](http://www.pmg.lcs.mit.edu/CLU.html)
  - [A History of CLU](http://www.lcs.mit.edu/publications/pubs/pdf/MIT-LCS-TR-561.pdf) (pdf)
  - [Dictionary of Programming Languages](http://cgibin.erols.com/ziring/cgi-bin/cep/cep.pl?_key=CLU)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")