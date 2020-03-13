> この記事は[Nemerle](https://ja.wikipedia.org/wiki/Nemerle)から翻訳されています。


**Nemerle**（**ネマール**）は[.NETプラットフォーム上で動作する](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[静的型付け](https://ja.wikipedia.org/wiki/静的型付け "wikilink")の[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")である。

手続き型、オブジェクト指向、関数型言語の機能を取り込んだハイブリッド言語であり、[C\#によく似た構文構造と強力なメタプログラミング機能が特徴となっている](../Page/C_Sharp.md "wikilink")。

Wrocław University（[ポーランド](../Page/ポーランド.md "wikilink")）のKamil Skalski、Michał Moskal、Prof. Leszek Pacholski、Paweł Olsztaらによって開発された。

現在ではロシアの開発コミュニティである[RSDNによって開発](https://ja.wikipedia.org/wiki/:ru:RSDN "wikilink")・保守がされているが、2012年より[JetBrainsがコア開発者を雇用して](https://ja.wikipedia.org/wiki/ジェットブレインズ "wikilink")、"N2" と呼ばれる新規・既存言語を実装するためのフレームワークの開発に注力している。\[1\]\[2\]\[3\]

## 特徴

おそらくNemerleの最も重要な特徴は、オブジェクト指向プログラミングと関数型プログラミングの両方を混在可能であるということであろう。プログラムのトップレベルではオブジェクト指向の構造を用いるが、メソッド本体には関数型のスタイルを用いることもできる。これは幾つかのプログラムにおいて非常に便利に機能する。以下に特徴的な機能を示す。

  - 強い[型推論](../Page/型推論.md "wikilink")
  - [マクロによる柔軟なメタプログラミング](../Page/マクロ_\(コンピュータ用語\).md "wikilink")
  - (C\#やJava、C++のような文法の)[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミング
  - (ML、OCaml、Haskellのような文法の)[関数型プログラミングの諸機能](../Page/関数型言語.md "wikilink")：
      - [高階関数](../Page/高階関数.md "wikilink")
      - [パターンマッチング](../Page/パターンマッチング.md "wikilink")
      - [代数的データ型](../Page/代数的データ型.md "wikilink")
      - ローカル関数
      - [タプル](../Page/タプル.md "wikilink")と[匿名型](https://ja.wikipedia.org/wiki/匿名型 "wikilink")
      - 関数の[部分適用](https://ja.wikipedia.org/wiki/部分適用 "wikilink")

メタプログラミング機能はコンパイラの高度な拡張を可能としており、プログラマの負担を可能な限り軽減しつつ、[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")の組み込み、[部分評価](../Page/部分評価.md "wikilink")、[アスペクト指向プログラミング](../Page/アスペクト指向プログラミング.md "wikilink")などを可能にしている。

また、[ジェネリックプログラミング](../Page/ジェネリックプログラミング.md "wikilink")や[ラムダや](https://ja.wikipedia.org/wiki/無名関数 "wikilink")[拡張メソッド](https://ja.wikipedia.org/wiki/拡張メソッド "wikilink")などといった[CLIの全ての機能を利用することができ](../Page/共通言語基盤.md "wikilink")、.NETのライブラリを[C\#と同じくらい](../Page/C_Sharp.md "wikilink")（あるいはそれ以上に）簡単に扱うことも可能である。

以下では、これらの機能をNemerle中でどのように利用できるかをいくつかの例を挙げて説明する。

### 型推論

``` nemerle
def x = 1;           // int
def myList = List(); // ジェネリック型 List[T] として宣言され、その後の使われ方から推論される
myList.Add(x);       // コンパイラにより myList は List[int] と推論される
```

### 全ては式である

``` nemerle
def x =
  { // x = 3 と等しい
    def y = 1;
    def z = 2;
    y + z   // 最後に評価された値が返される
  };

def x =
  if (DateTime.Now.DayOfWeek == DayOfWeek.Monday)  // if、using、try なども全て式である
    "Monday"
  else
    "other day";

def x = try int.Parse(someString)
        catch { | FormatException() => 0 };

def x = returnBlock :
  {
    foreach (i in [1, 2, 3])
      when (i > 2)
        returnBlock(true); // ブロックを抜ける ( x = true となる )

    false // x = false
  };
```

### タプル

``` nemerle
def k = (1, "one"); // k : (int * string)
def (a, b) = k; // a = 1, b = "one"
```

### パターンマッチ

``` nemerle
def result = match (number)
{
  | 0            => "zero"
  | 1            => "one"
  | x when x < 0 => "negative"
  | _            => "more than one"
}
```

### 関数型とローカル関数

``` nemerle
using System.Console; // クラスとモジュール(静的クラス)を名前空間として使用できる
def next(x) { x + 1 }; // 引数 x の型は使われ方から推論される

def mult(x, y) { x * y };

def fibonacci(i)
{
  | 0     => 0
  | 1     => 1
  | other => fibonacci(i - 1) + fibonacci(i - 2)
};

WriteLine(next(9));        // 10  "Console.WriteLine(next(9));" と等しい
WriteLine(mult(2, 2));     // 4
WriteLine(fibonacci(10)); // 55
```

### バリアント

[バリアント](../Page/代数的データ型.md "wikilink") (代数的データ型とも) は複数の種類の値を表現できる:

``` csharp
 variant RgbColor{
   | Red
   | Yellow
   | Green
   | Different {
       red : float;
       green : float;
       blue : float;
     }
 }
```

### メタプログラミング

Nemerle のマクロ機能は、コンパイル中にプログラム中のコードの生成・解析・編集を可能にする。マクロは通常のメソッド呼び出しとして使えるほか、構文を定義して用いることもできる。Nemerleの多くの構文(if、for、foreach、while、usingなど)はマクロによって定義されている。

"**if**" マクロの例:

``` nemerle
macro @if (cond, e1, e2)
syntax ("if", "(", cond, ")", e1, Optional (";"), "else", e2)
{
  /*
    <[ ]> はコードクォートであり、Nemerleコンパイラは中身を構文木に変換して提供する。
    C# における式木に似ているところがある。
  */
  <[
    match ($cond : bool)
    {
      | true => $e1
      | _ => $e2
    }
  ]>
}

// コード中でマクロを使う:
def max = if (a > b) a else b;
// コンパイル中に上のコードは下のように展開される:
def max = match (a > b)
{
  | true => a
  | _    => b
}
```

## 統合開発環境

Nemerleは[Visual Studio 2008に統合することができる](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。[Visual Studio 2008 Shellをベースとした無料のIDEも存在する](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。\[4\]

また、[SharpDevelop](../Page/SharpDevelop.md "wikilink")用のプラグインも用意されている([プラグインのページ](http://code.google.com/p/nemerle/source/browse/#svn%2Fnemerle%2Ftrunk%2Fsnippets%2Fsharpdevelop))。

[アドイン](http://visualstudiogallery.msdn.microsoft.com/5d93dc0a-0ce9-4b97-970c-ab1993eb934a)によりVisual Studio 2010にも統合が可能で、[Visual Studio 2013版](http://visualstudiogallery.msdn.microsoft.com/fb29c7b2-d1e5-42e4-8a56-9b9c022c22a9)も存在している。

## 例

### Hello, World\!

伝統的な[Hello worldは](../Page/Hello_world.md "wikilink")、次のようにC\#ライクなスタイルで書くことができる。

``` csharp
 class Hello {
   static Main () : void {
     System.Console.WriteLine ("Hello, world!");
   }
 }
```

あるいは、よりシンプルに

``` csharp
 System.Console.WriteLine("Hello, world!");
```

とも書ける。

### マクロの例

#### 文字列フォーマット

$ 記号により文字列中に値を展開することができる:

``` php
def s = $"The number is $i"; // $i を変数 i の値で置き換える
def s = $"$x + $y = $(x+y)"; // $(...) を使うことで複雑な式も展開できる
```

#### コード生成

*StructuralEquality*、*Memoize*、*json*、*with*などはコンパイル時にコードを生成するマクロである。 いくつかのマクロ(*StructuralEquality*, *Memoize*)はC\#における属性のように見えるが、コンパイル時に適切なコードへの変換を行う。

``` csharp
[StructuralEquality] // IEquatable[Sample] インターフェースを自動で実装するマクロ
class Sample
{
   [Memoize]  // 最初の計算結果を保持する
   public static SomeLongEvaluations() : int
   {
       MathLib.CalculateNthPrime(10000000)
   }

   [DependencyProperty] // WPF 依存関係プロパティ
   public DependencyPropertySample { get; set; }

   public static Main() : void
   {
/* 構文マクロ "json" は次のようなコードを生成する:
JObject.Object([("a", JValue.Number(SomeLongEvaluations())), ("b", JValue.Number(SomeLongEvaluations() + 1))])
*/
       def jObject = json { a: SomeLongEvaluations(); b: (SomeLongEvaluations() + 1)}
// オブジェクト初期化マクロ "<-" はC#のオブジェクト初期化子と同じ機能を提供する
       def k = Diagnostics.Process() <-
       {
          StartInfo <- // コンストラクタ呼び出しなしに内部のプロパティの初期化を行える
          {
              FileName = "calc.exe";
              UseShellExecute = true;
          }
          Exited += () => WriteLine("Calc done"); // イベントとデリゲート
       }

       ReadLine();
   }
}
```

#### データベースへのアクセス

例えば、Nemerleのマクロを用いて[SQL](../Page/SQL.md "wikilink")文を発行するコードは以下のように書くことができる。

``` csharp
 ExecuteReaderLoop ("SELECT firstname, lastname FROM employee WHERE firstname = $myparm", dbcon,
 {
   System.Console.WriteLine ("Name: {0} {1}", firstname, lastname)
 });
```

これは、次の文の代わりに用いられる。

``` csharp
 string sql = "SELECT firstname, lastname FROM employee WHERE firstname = :a";
 NpgsqlCommand dbcmd = new NpgsqlCommand (sql, dbcon, dbtran);
 dbcmd.Parameters.Add("a", myparm);

 NpgsqlReader reader = dbcmd.ExecuteReader();

 while(reader.Read()) {
   string firstname = reader.GetString (0);
   string lastname = reader.GetString (1);
   System.Console.WriteLine ("Name: {0} {1}", firstname, lastname)
 }
 reader.Close();
 dbcmd.Dispose();
```

これは、ライブラリ中の幾つかの動作を隠すだけでなく、クエリ文字列や変数、データベースから返されたコラムがコンパイラによって理解され実行されるということを表している。`ExecuteReaderLoop`マクロは、プログラマが記述しなければならないコードと同等のコードを生成させることができる。またSQL文が正しいかどうかをコンパイル時に検査することも可能である。

#### 新しい言語の実装

Nemerleのマクロを用いると、言語に新しい構文を導入することも可能である。

``` nemerle
 macro ReverseFor (i, begin, body)
 syntax ("ford", "(", i, ";", begin, ")", body)
 {
   <[ for ($i = $begin; $i >= 0; $i--) $body ]>
 }
```

この例では`ford ( EXPR ; EXPR ) EXPR`構文を定義していて、この構文は次のように用いることができる。

``` nemerle
 ford (i ; n) print (i);
```

### NemerleとASP.NET

Nemerleは[ASP.NET](../Page/ASP.NET.md "wikilink")上に直接組み込むことが可能である。

`<%@ Page Language="Nemerle" %>`
` <script runat="server">`
` `
`     Page_Load(_ : object, _ : EventArgs) : void {`
`         Message.Text = $"You last accessed this page at: $(DateTime.Now)";`
`     }`
` `
`     EnterBtn_Click(_ : object, _ : EventArgs) : void {`
`         Message.Text = $"Hi $(Name.Text), welcome to ASP.NET!";`
`     }`
` `
` </script>`
` `
` <html>`
`     <body>`
`         <form runat="server">`
`             Please enter your name: <asp:TextBox ID="Name" runat="server" />`
`             <asp:Button OnClick="EnterBtn_Click" Text="Enter" runat="server" />`
` `
`             <p><asp:Label ID="Message" runat="server" /></p>`
`         </form>`
`     </body>`
` </html>`

また、別ファイルにコードを記載し、それを呼び出すことも可能である。

`<%@ Page Language="Nemerle" Src="test.n" Inherits="Test" %>`

### P/Invoke

Nemerleはネイティブのプラットフォームライブラリを呼び出すことができる。その構文はC\#やその他の.NET言語に非常に似ている。

``` csharp
 using System;
 using System.Runtime.InteropServices;

 class PlatformInvokeTest
 {
     [DllImport("msvcrt.dll")]
     public extern static puts(c : string) : int;

     [DllImport("msvcrt.dll")]
     internal extern static _flushall() : int;

     public static Main() : void
     {
         _ = puts("Test");
         _ = _flushall();
     }
 }
```

## 参照

## 参考

  - [Publications about Nemerle in RSDN Magazine, Russian official science magazine](http://rsdn.ru/summary/3766.xml)

  -
  - [Presentation "Nemerle is notable" by Denis Rystsov](http://www.slideshare.net/rystsov/nemerle-is-notable)

  - [Article "Unconventional languages for unconventional supercomputers" by Andrey Adinetz](http://www.osp.ru/os/2011/05/13009416/)

## 外部リンク

  - [Nemerle Homepage](http://nemerle.org/)
  - [GitHub上のリポジトリ(RSDN管理下の新しいバージョン)](https://github.com/rsdn/nemerle)
  - [Google Code上のプロジェクトとリポジトリ(古いバージョン)](https://code.google.com/archive/p/nemerle/)
  - [Nemerle Forum](https://groups.google.com/forum/#!forum/nemerle-en)

{{.NET}}

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink")

1.
2.
3.
4.  [Nemerle Studio Microsoft Setup Installer](http://code.google.com/p/nemerle/downloads/list) can be installed after installation of [Visual Studio Shell 2008 Isolated](http://www.microsoft.com/downloads/en/details.aspx?FamilyID=aca38719-f449-4937-9bac-45a9f8a73822&displaylang=en)