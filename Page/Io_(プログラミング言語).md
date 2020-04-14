> この記事は[Io \(プログラミング言語\)](https://ja.wikipedia.org/wiki/Io_\(プログラミング言語\))から翻訳されています。


**Io**（イオあるいはアイオー\[1\]）は純粋な[オブジェクト指向](../Page/オブジェクト指向プログラミング.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")であり、[Smalltalk](../Page/Smalltalk.md "wikilink")、[Self](../Page/Self.md "wikilink")、[Lua](../Page/Lua.md "wikilink")、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、Act1、の影響を受けている。Self や NewtonScript のような[プロトタイプベース](../Page/プロトタイプベース.md "wikilink")のオブジェクトモデルであり、[オブジェクトと](../Page/オブジェクト_\(プログラミング\).md "wikilink")[クラスを区別しない](../Page/クラス_\(コンピュータ\).md "wikilink")。Smalltalk のようにあらゆるものをオブジェクトとして扱い、[動的型付け](../Page/動的型付け.md "wikilink")を行う。LISPのように文の概念がなく、[制御フロー](https://ja.wikipedia.org/wiki/制御フロー "wikilink")は関数を使って実現される。Io は[アクターによる並行性を実現しており](../Page/アクターモデル.md "wikilink")、のプログラミング言語には珍しい特徴となっている。

Io の特筆すべき特徴は、その効率のよさ、処理系の小ささ、外部リソースを自由に使えるオープン性である。Io は小型で移植性の高い[仮想機械](../Page/仮想機械.md "wikilink")で実行される。

## 歴史

この言語は、[2002年](../Page/2002年.md "wikilink")[3月7日](../Page/3月7日.md "wikilink")ごろ Steve Dekorte が友人の協力を得て作った。彼はプログラミング言語の仕組みをよく知らなかったため、勉強のために小型の言語を実際に作ってみることにした。そして完成したのが Io である。

## 方針

Io の目的は概念的な統一 (conceptual unification) と[動的言語](https://ja.wikipedia.org/wiki/動的言語 "wikilink")の研究にあるので、トレードオフとして性能向上よりも単純さと柔軟性を好む傾向がある。

## 機能/特徴

  - [プロトタイプベース](../Page/プロトタイプベース.md "wikilink")の純粋な[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")
  - [例外処理](../Page/例外処理.md "wikilink")
  - [Perl](../Page/Perl.md "wikilink")風の[正規表現](../Page/正規表現.md "wikilink")
  - [弱い参照](../Page/弱い参照.md "wikilink")をサポートするインクリメンタル[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")
  - 高[移植性](../Page/移植_\(ソフトウェア\).md "wikilink")
  - [DLL](../Page/ダイナミックリンクライブラリ.md "wikilink")/[共有ライブラリの動的ローディング](../Page/ライブラリ.md "wikilink")
  - イントロスペクション、[リフレクション](../Page/リフレクション_\(情報工学\).md "wikilink")、[メタプログラミング](../Page/メタプログラミング.md "wikilink")
  - [アクターモデル](../Page/アクターモデル.md "wikilink")に基づく[並行性](../Page/並行性.md "wikilink")
  - [コルーチン](../Page/コルーチン.md "wikilink")
  - 小規模な[仮想機械](../Page/仮想機械.md "wikilink")
  - [高階関数](../Page/高階関数.md "wikilink")

## 文法

最も単純な形式では、次のような1つの識別子でも Io のプログラムと言える。

``` io
doStuff
```

この doStuff は[メソッドであり](../Page/メソッド_\(計算機科学\).md "wikilink")、引数がないので後ろに括弧をつける必要がない。

doStuff に引数がある場合、次のように記される。

``` io
doStuff(42)
```

Io は[メッセージパッシング言語であり](../Page/メッセージ_\(コンピュータ\).md "wikilink")、Io では[コメント以外はメッセージの集積でプログラムが構成される](../Page/コメント_\(コンピュータ\).md "wikilink")。上掲の例でもそれが現れているがこれが全てではない。メッセージパッシング言語であることを明確に示すため、次の例を示す。

``` io
System version
```

これは、 "version" というメッセージが "System" オブジェクトに送られていることを示している。

[演算子](../Page/演算子.md "wikilink")は特別であり、これまでの例ほど単純ではない。Ioの[構文解析器](../Page/構文解析器.md "wikilink")はインタプリタが定義する演算子をインターセプトし、それをメソッドコールに翻訳する。例えば、次のような記述があったとする。

``` io
1 + 5 * 8 + 1
```

これは次のように翻訳される。

`1 +(5 *(8)) +(1)`

見ての通り、[演算子の優先順位](https://ja.wikipedia.org/wiki/演算子の優先順位 "wikilink")が一応存在しており、[C言語](../Page/C言語.md "wikilink")での優先順位と同じである。

また、演算子がメソッドコールになっていることにも注意されたい。Io の演算子は全てメソッドである（ただし、例外として代入演算子 ":=" と "=" は構文解析器が全く異なるメッセージに翻訳する）。このため、演算順序を制御するための括弧が不要という特徴がある。

### メソッドとブロック

Io には匿名の関数を作る2つの方法がある。メソッドとブロックである。この2つの違いは[スコープ](../Page/スコープ.md "wikilink")である。ブロックは[静的スコープ](../Page/静的スコープ.md "wikilink")であり、メソッドは[動的スコープ](../Page/動的スコープ.md "wikilink")である。

メソッドもブロックも[高階関数](../Page/高階関数.md "wikilink")である。

### 例

[Hello world](../Page/Hello_world.md "wikilink") は次のようになる。

``` io
"Hello, world!" println
```

新たなオブジェクトは[クローニングで生成される](https://ja.wikipedia.org/wiki/クローニング_\(プログラミング\) "wikilink")。Io では新たな空のオブジェクトが作られたとき、その親との違いだけが新しいオブジェクトに格納される。このような方式を[差分継承](https://ja.wikipedia.org/wiki/差分継承 "wikilink")と呼ぶ。以下に例を示す。

``` io
A := Object clone // 新しい空のオブジェクト "A" を作る
```

再帰を使わない階乗プログラムを以下に示す。

``` io
factorial := method(n,
  if(n == 0, return 1)
  res := 1
  n to(1) foreach(i, res = res * i)
  res
)
```

この例では range を使っているが、for ループの方が高速である。もう1つの例を以下に示す。

``` io
// C++ 風のコメントが書ける
# シェル風のコメントでもよい
/* C言語風でもよい */

for(i, 1, 10, i print) // 1 から 10 までの数を表示

x := Object clone // 新たなスロットを作るときは ':=' を使う
x = Map clone // 上書きするときは '=' を使う
x prettyprint := method( // 引数のないメソッドを作る
    foreach(key, value, write(key, ": ", value, "\n")) // マップ上でループする
)
x atPut("hi", 1) // キーと値のペアをマップに置く
x atPut("hello", 2)
x prettyprint
/* 出力は次のようになる:
      hi: 1
      hello: 2
*/
```

## 脚注

## 関連項目

  - [jEdit](https://ja.wikipedia.org/wiki/jEdit "wikilink") - Io のソースファイル向けの強調設定がある

## 外部リンク

  - [io language](http://iolanguage.com/) - Io 公式サイト
  - [IoLanguage/io: Io programming language. Inspired by Self, Smalltalk and LISP.](https://github.com/IoLanguage/io) - [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")リポジトリ
  - [Io Notes](http://iota.flowsnake.org/)
  - [Open Directory: Programming: Languages: Io](http://dmoz.org/Computers/Programming/Languages/Io/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink")

1.  Io言語の名前の由来は2つあり、ひとつは[イタリア語](../Page/イタリア語.md "wikilink")の[一人称代名詞](https://ja.wikipedia.org/wiki/一人称代名詞 "wikilink")  であり、もうひとつは[木星](../Page/木星.md "wikilink")の[第1衛星イオ](../Page/イオ_\(衛星\).md "wikilink") (, ) である。[The Reflective Programming Language Io](http://homes.dico.unimi.it/~cazzola/ps/DISI-TR-04-02.pdf)