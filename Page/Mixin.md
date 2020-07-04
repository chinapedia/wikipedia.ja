> この記事は[Mixin](https://ja.wikipedia.org/wiki/Mixin)から翻訳されています。


**mixin** とは[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")において、サブクラスによって[継承されることにより機能を提供し](../Page/継承_\(プログラミング\).md "wikilink")、単体で動作することを意図しない[クラスである](../Page/クラス_\(コンピュータ\).md "wikilink")。言語によっては、その言語でクラスや継承と呼ぶものとは別のシステムとして mixin がある場合もある（[\#バリエーション](https://ja.wikipedia.org/wiki/#バリエーション "wikilink")の節で詳述）。

## 概要

オブジェクト指向プログラミングにおいて、継承は本来は特化を意図したものである。すなわち、継承する側（[派生型](../Page/派生型.md "wikilink")）と継承される側（基底型）の間には[リスコフの置換原則](../Page/リスコフの置換原則.md "wikilink")があることを前提とする。

しかし実際のところは、実装の再利用のための手段として使われることが多い（濫用されがちであるが）。mixin における継承も、前述のような特化のためではなく、複数の機能を集めるための手段である。特にクラスの[多重継承が可能なシステムでは](../Page/継承_\(プログラミング\).md "wikilink")、複数の mixin クラスを多重継承し、「単に複数の機能を持つクラス」を簡単に作る、というような使い方ができる。典型例としては、InputStream と OutputStream という mixin クラスを多重継承して、InputOutputStream という双方向ストリームのクラスとする、といったようなパターンである。

mixin は、そのようなもの自体はそれ以前からも考えられていたが、[シンボリックス](../Page/シンボリックス.md "wikilink")社のオブジェクト指向システム Flavors（[:en:Flavors (programming language)](https://ja.wikipedia.org/wiki/:en:Flavors_\(programming_language\) "wikilink")）でその名が使われ、それが一般化した。Flavorsは、同社の[Lispマシンにおける](../Page/LISPマシン.md "wikilink")、同時期にいくつかあった、Lispでの、あるいはLispによるオブジェクト指向の試みのひとつである。名称の由来は、マサチューセッツ州 Somerville にあったアイスクリーム屋\[1\]からヒントを得て考え出されたものであった\[2\]（シンボリックス社は「MIT発のベンチャー」のひとつである）。このアイスクリーム店の店長は（バニラやチョコレートなどの）基本となる味を混ぜ、追加の具材（ナッツ、クッキー、キャンディなど）と組み合わせたものを提供し、それを Mix-In と呼んで店の登録商標としていた\[3\]。

mixin は[コードの再利用](https://ja.wikipedia.org/wiki/コードの再利用 "wikilink")を促進 する。しかし、mixin にはそれなりの妥協も伴う。

（クラスの多重継承すなわち実装の多重継承ができず、インタフェースの複数実装による型の多重継承のみができる、例えば[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[C\#などの観点からは](../Page/C_Sharp.md "wikilink")）mixin は、「メソッド実装付きの[インタフェース](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink") 」ということもできる。クラスが mixin を含む場合、そのインタフェースを実装したクラスは、mixin の属性と操作を取り込む。継承するというのとは異なっている。取り込んだ要素はコンパイル時にクラスの一部となる。興味深いことに、mixin はインタフェースを実装する必要はない。それでもあえてインタフェースを実装する利点は、そのインタフェースを必要とするメソッドに、引数としてインスタンスを渡せるからである。

## バリエーション

クラスとその継承関係とは別のものとして mixin を活用している言語として[Ruby](../Page/Ruby.md "wikilink")がある。Rubyではクラスの継承は単一継承のみとし、多重継承にまつわる問題（例えば[菱形継承問題](../Page/菱形継承問題.md "wikilink")）を避けた。そして「継承関係の無いクラスのようなもの」としてモジュールと呼ばれる言語機能があり、モジュールは複数個（いくつでも）クラスに「mixinする」ことができる。モジュール自体は何かを継承したりはしていないため、菱形継承問題は起きない。

その他、mixinのようなものがある言語。

  - [D言語](../Page/D言語.md "wikilink") (「テンプレート・ミクスイン」と呼ばれる)

  -
  -
  -
  -
  -
  -
  -
  -
  - （ 向けのオブジェクト指向拡張\]）

  -
  - [Vala](https://ja.wikipedia.org/wiki/Vala "wikilink")

## 例

### Python

Python の、特に Python 2.3 以降および Python 3 では C3 linearization により多重継承した際のメソッド探索順は解決されるので、多重継承は有力な手法であり、実際にいくつか活用例がある。`SocketServer` モジュールは [UDP](../Page/User_Datagram_Protocol.md "wikilink") および [TCP](../Page/Transmission_Control_Protocol.md "wikilink") ソケットサーバとして動作する `UDPServer` と `TCPServer` クラスの両方を備えている。通常、すべてのコネクションは同じプロセス内で処理されるが、`ForkingMixIn` と `ThreadingMixIn` という追加の mixin クラスが存在する。下記のように TCPServer を ThreadingMixIn により拡張すると、

``` python
class ThreadingTCPServer(ThreadingMixIn, TCPServer):
  pass
```

`ThreadingMixIn` が `TCPServer` にコネクションごとに[スレッドを生成する機能を追加する](../Page/スレッド_\(コンピュータ\).md "wikilink")。あるいは、`ForkingMixIn` を用いると各新規のコネクションに対してプロセスが fork される。明らかに、スレッドを生成したりプロセスを fork する機能は単独では大して役に立たない。

この使用例では、mixin はソケットサーバとしての機能に影響することなく、基盤となる機能を選択可能な形で提供している。

### C\#

[C\#では](../Page/C_Sharp.md "wikilink")[インタフェース](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink") と拡張メソッドの組合せによって、Mix-inを再現できる。

``` csharp
using System.Linq;

  System.Collections.Generic.IEnumerable<int> range = Enumerable.Range(1, 10);
  // IEnumerable<T>にはSum()メソッドは定義されない。
  // 実際にはSystem.Linq.Enumerableクラスに実装された拡張メソッドである。
  int sum = range.Sum();

  // 上記は下記の糖衣構文である。
  int sum = Enumerable.Sum(range);
```

## 関連項目

  - [トレイト](https://ja.wikipedia.org/wiki/トレイト "wikilink")
  - [抽象型](https://ja.wikipedia.org/wiki/抽象型 "wikilink")

## 注

<references />

## 外部リンク

  - [Wiki entry](http://c2.com/cgi/wiki?MixIn) at [Cunningham & Cunningham, Inc.](http://c2.com/)
  - [Mixins](http://www.macromedia.com/support/documentation/en/flex/1/mixin/index.html) in [ActionScript](../Page/ActionScript.md "wikilink").
  - [Scala Overview: Mixin Class Composition](http://scala.epfl.ch/intro/mixin.html) - a step-by-step example in [Scala](../Page/Scala.md "wikilink")
  - [The Common Lisp Object System: An Overview](http://www.dreamsongs.com/NewFiles/ECOOP.pdf) by [Richard P. Gabriel](https://ja.wikipedia.org/wiki/:en:Richard_P._Gabriel "wikilink") and Linda DeMichiel provides a good introduction to the motivation for defining classes by means of generic functions.

[Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink")

1.  Steve's Ice Cream Parlor
2.  [Using Mix-ins with Python](http://www.linuxjournal.com/article/4540)
3.  [LISTSERV 14.4](http://listserv.linguistlist.org/cgi-bin/wa?A2=ind0208a&L=ads-l&P=11751)