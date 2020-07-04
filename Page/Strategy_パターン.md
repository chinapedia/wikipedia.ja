> この記事は[Strategy パターン](https://ja.wikipedia.org/wiki/Strategy_パターン)から翻訳されています。


**Strategy パターン**は、[コンピュータープログラミングの領域において](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、[アルゴリズム](../Page/アルゴリズム.md "wikilink")を実行時に選択することができる[デザインパターンである](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。

Strategyパターンはアルゴリズムを記述する[サブルーチン](../Page/サブルーチン.md "wikilink")への参照をデータ構造の内部に保持する。このパターンの実現には、[関数ポインタ](https://ja.wikipedia.org/wiki/関数ポインタ "wikilink")や[関数オブジェクト](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")、[デリゲートのほか](../Page/デリゲート_\(プログラミング\).md "wikilink")、オーソドックスな[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")における[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")と[委譲](../Page/委譲.md "wikilink")、あるいは[リフレクションによる動的](../Page/リフレクション_\(情報工学\).md "wikilink")[ダック・タイピング](../Page/ダック・タイピング.md "wikilink")などが利用される。

このパターンは、関数が[第一級オブジェクト](../Page/第一級オブジェクト.md "wikilink")である言語では暗黙のうちに使用されている。例として後述の[Pythonコード例を参照のこと](https://ja.wikipedia.org/wiki/#Python "wikilink")。

Strategy パターンは、アプリケーションで使用されるアルゴリズムを動的に切り替える必要がある際に有用である。Strategy パターンはアルゴリズムのセットを定義する方法を提供し、これらを交換可能にすることを目的としている。Strategy パターンにより、アルゴリズムを使用者から独立したまま様々に変化させることができるようになる。

## Strategy パターンを示す図

[500px](https://ja.wikipedia.org/wiki/ファイル:StrategyPatternClassDiagram.svg "wikilink") で表した Strategy パターン\]\]

## サンプルコード

### Java

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")では[クラスの](../Page/クラス_\(コンピュータ\).md "wikilink")[メソッド](../Page/メソッド_\(計算機科学\).md "wikilink")[オーバーライド](../Page/オーバーライド.md "wikilink")によるポリモーフィズムを使ってStrategyパターンを実現することができる。[インターフェイスを用いた例を示す](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。

``` java
package org.wikipedia.patterns.strategy;

// MainApp test application
class MainApp {
    public static void main(String[] args) {
        Context context;

        // 異なるアルゴリズムに従う3つのコンテキスト。
        context = new Context(new ConcreteStrategyA());
        context.execute();

        context = new Context(new ConcreteStrategyB());
        context.execute();

        context = new Context(new ConcreteStrategyC());
        context.execute();
    }
}

// 具体的な戦略を実装するクラスは、このインターフェイスを実装する。
// コンテキストクラスは、具体的な戦略を呼び出すためにこのインターフェイスを使用する。
interface Strategy {
    void execute();
}

// Strategy インターフェイスを用いたアルゴリズムの実装。
class ConcreteStrategyA implements Strategy {
    public void execute() {
        System.out.println("Called ConcreteStrategyA.execute()");
    }
}

class ConcreteStrategyB implements Strategy  {
    public void execute() {
        System.out.println("Called ConcreteStrategyB.execute()");
    }
}

class ConcreteStrategyC implements Strategy {
    public void execute() {
        System.out.println("Called ConcreteStrategyC.execute()");
    }
}

// ConcreteStrategy を指定して作成され、Strategy オブジェクトへの参照を保持する。
class Context {
    Strategy strategy;

    // Constructor
    public Context(Strategy strategy) {
        this.strategy = strategy;
    }

    public void execute() {
        this.strategy.execute();
    }
}
```

### Python

[Python](../Page/Python.md "wikilink") では関数が[第一級オブジェクト](../Page/第一級オブジェクト.md "wikilink")であり、このパターンを明示的に定義する必要はない。下記は[コールバック関数](https://ja.wikipedia.org/wiki/コールバック関数 "wikilink")を用いる [GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") プログラミングで見られる例である。

``` python
class Button:
    """A very basic button widget."""
    def __init__(self, submit_func, label):
        self.on_submit = submit_func   # strategy 関数を直接生成
        self.label = label

# 異なる戦略を持つ2つのインスタンスを作成
button1 = Button(sum, "Add 'em")
button2 = Button(lambda nums: " ".join(map(str, nums)), "Join 'em")

# ボタンをテストする
numbers = range(1, 10) # A list of numbers 1 through 9
print button1.on_submit(numbers) # displays "45"
print button2.on_submit(numbers) # displays "1 2 3 4 5 6 7 8 9"
```

### C\#

[C\#はJava同様にクラスやインターフェイスによるポリモーフィズムを用いることもできるが](../Page/C_Sharp.md "wikilink")、カスタマイズポイントがひとつのメソッドしかない場合（オブジェクトの他のプロパティやメソッドにアクセスしない場合）は、継承関係を必要としないデリゲートを使うほうが好まれる\[1\]。

``` csharp
using System;

// MainApp テストアプリケーション。
public class MainApp
{
    public static void Main()
    {
        Context context;

        // 異なるアルゴリズムに従う3つのコンテキスト。
        context = new Context(new ConcreteStrategyA().Execute);
        context.Execute();

        context = new Context(new ConcreteStrategyB().Execute);
        context.Execute();

        context = new Context(new ConcreteStrategyC().Execute);
        context.Execute();
    }
}

// 具体的な戦略を実装するクラスは、このデリゲートに適合するメソッドを実装する。
// コンテキストクラスは、具体的な戦略を呼び出すためにこのデリゲートを使用する。
public delegate void ExecuteStrategyDelegate();

class ConcreteStrategyA
{
    public void Execute()
    {
        Console.WriteLine("Called ConcreteStrategyA.Execute()");
    }
}

class ConcreteStrategyB
{
    public void Execute()
    {
        Console.WriteLine("Called ConcreteStrategyB.Execute()");
    }
}

class ConcreteStrategyC
{
    public void Execute()
    {
        Console.WriteLine("Called ConcreteStrategyC.Execute()");
    }
}

// ExecuteStrategyDelegate オブジェクトへの参照を保持する。
class Context
{
    ExecuteStrategyDelegate executeStrategy;

    // Constructor
    public Context(ExecuteStrategyDelegate executeStrategy)
    {
        this.executeStrategy = executeStrategy;
    }

    public void Execute()
    {
        this.executeStrategy();
    }
}
```

なお、Javaもバージョン8以降であれば、メソッド参照と関数型インターフェイス (functional interface) を用いることで、C\#と類似の実装が可能となる。

## Strategy パターンと Bridge パターン

Strategy パターンの [UML](../Page/統一モデリング言語.md "wikilink") クラス図は [Bridge パターンのものと同じである](../Page/Bridge_パターン.md "wikilink")。しかし、これら二つのデザインパターンはその**意図**が同じではない。Strategy パターンは**振る舞い**に対するパターンであるが、Bridge パターンは**構造**に対するパターンである。

一般にコンテキストと戦略との結合は、Bridge パターンにおける抽象化と実装の結合より強固である。

## Strategy パターンと開放/閉鎖原則

Strategy パターンに従うと、クラスの振る舞いは継承されるべきではなく、インターフェイスを用いてカプセル化するべきである。例として Car クラスを考えると、Car の振る舞いにはブレーキとアクセルがある。

アクセルとブレーキの振る舞いはモデルにより大きく異なるため、良くあるアプローチはこれらの振る舞いをサブクラスとして実装することであるが、このアプローチには大きな問題点がある。すなわち、アクセルとブレーキの振る舞いは、新たな Car モデルごとに宣言されなければならない。これはモデルが少ないときには問題にならないが、モデルの数が増えるにつれ、それらの振る舞いを管理する作業が大幅に増加し、またコードがモデル間で重複することになる。さらに、各コードを詳しく分析しなければそれぞれのモデル用の振る舞いの性質を知ることができない。

これに対して Strategy パターンでは、継承ではなく合成 (composition) を用いる。Strategy パターンにおける振る舞いは別々のインターフェイスと、これらのインターフェイスを実装した[抽象クラス](https://ja.wikipedia.org/wiki/抽象クラス "wikilink")として定義される。具体的なクラスは、これらのインターフェイスをカプセル化する。これにより、振る舞いと、それを用いるクラスがうまく分離できる。振る舞いは、それを用いるクラスに変更を加えずに変更することができ、クラスは大きなコード変更を必要とすることなく、使用する実装を切り替えることで振る舞いを切り替えることができる。振る舞いは設計時にも実行時にも変更することができる。例として、Car オブジェクトのブレーキの振る舞いを、メンバー brakeBehavior を BrakeWithABS から Brake に変えることで変更できる：

`brakeBehavior = new Brake(); `

[ファイル:Strategy.JPG](https://ja.wikipedia.org/wiki/ファイル:Strategy.JPG "wikilink")

これにより設計に優れた柔軟性をもたせることができ、かつ拡張に対して開放的であり変更に対して閉鎖的であるべきとする[開放/閉鎖原則](https://ja.wikipedia.org/wiki/開放/閉鎖原則 "wikilink") (Open/Closed Principle, OCP) とも調和を保つことができる。

## 脚注

## 関連項目

  - [ミックスイン](https://ja.wikipedia.org/wiki/ミックスイン "wikilink")
  - [:en:Policy-based design](https://ja.wikipedia.org/wiki/:en:Policy-based_design "wikilink")
  - [:en:First-class function](https://ja.wikipedia.org/wiki/:en:First-class_function "wikilink")
  - [Template Method パターン](../Page/Template_Method_パターン.md "wikilink")
  - [Bridge パターン](../Page/Bridge_パターン.md "wikilink")
  - [開放/閉鎖原則](https://ja.wikipedia.org/wiki/開放/閉鎖原則 "wikilink")
  - [Factory パターン](https://ja.wikipedia.org/wiki/Factory_パターン "wikilink")
  - [:en:List of object-oriented programming terms](https://ja.wikipedia.org/wiki/:en:List_of_object-oriented_programming_terms "wikilink") (オブジェクト指向の用語一覧)

## 外部リンク

  - [Strategy Pattern for Java article](http://www.javaworld.com/javaworld/jw-04-2002/jw-0426-designpatterns.html)
  - [Data & object factory](http://www.dofactory.com/Patterns/PatternStrategy.aspx)
  - [Refactoring: Replace Type Code with State/Strategy](http://www.refactoring.com/catalog/replaceTypeCodeWithStateStrategy.html)
  - [Jt](http://www.fsw.com/Jt/Jt.htm) J2EE Pattern Oriented Framework
  - [Strategy Pattern with a twist\!](http://anirudhvyas.com/root/2008/04/02/a-much-better-strategy-pattern/)

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")

1.  \[<https://docs.microsoft.com/en-us/previous-versions/ms173173(v=vs.140>) When to Use Delegates Instead of Interfaces (C\# Programming Guide) | Microsoft Docs\]