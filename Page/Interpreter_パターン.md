> この記事は[Interpreter パターン](https://ja.wikipedia.org/wiki/Interpreter_パターン)から翻訳されています。


**Interpreter パターン**は、[コンピュータプログラミングにおける](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")[デザインパターンの一つである](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。**Interpreter パターン**の基本的な考えは、定義された種類の問題を素早く解くために、[ドメインに特化した言語を実装することである](../Page/ドメイン固有言語.md "wikilink")。特化言語は汎用の言語よりも数倍から数百倍高速に問題を解ける場合が多い。

## Interpreter パターンの使用例

  - データベースに特化した問い合わせ言語（[SQL](../Page/SQL.md "wikilink")など）
  - 通信プロトコルを記述するために良く用いられる特化したコンピュータ言語
  - 特化言語を導入した汎用のコンピュータ言語

## 例

### Java

以下の Java の例は、汎用のプログラミング言語がより特化した言語を解釈する例を、ここでは [逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink") を用いて示す。

出力：

`'42 4 2 - +' equals 44`

``` java
import java.util.*;

interface Expression {
    public void interpret(Stack<Integer> s);
}

class TerminalExpression_Number implements Expression {
    private int number;
    public TerminalExpression_Number(int number)       { this.number = number; }
    public void interpret(Stack<Integer> s)  { s.push(number); }
}

class TerminalExpression_Plus implements Expression {
    public void interpret(Stack<Integer> s)  { s.push( s.pop() + s.pop() ); }
}

class TerminalExpression_Minus implements Expression {
    public void interpret(Stack<Integer> s)  { s.push( - s.pop() + s.pop() ); }
}

class Parser {
    private ArrayList<Expression> parseTree = new ArrayList<Expression>(); // only one NonTerminal Expression here

    public Parser(String s) {
        for (String token : s.split(" ")) {
            if      (token.equals("+")) parseTree.add( new TerminalExpression_Plus() );
            else if (token.equals("-")) parseTree.add( new TerminalExpression_Minus() );
            // ...
            else                        parseTree.add( new TerminalExpression_Number(Integer.valueOf(token)) );
        }
    }

    public int evaluate() {
        Stack<Integer> context = new Stack<Integer>();
        for (Expression e : parseTree) e.interpret(context);
        return context.pop();
    }
}

class InterpreterExample {
    public static void main(String[] args) {
        String expression = "42 4 2 - +";
        Parser p = new Parser(expression);
        System.out.println("'" + expression +"' equals " + p.evaluate());
    }
}
```

## 関連項目

  - [バッカス・ナウア記法](../Page/バッカス・ナウア記法.md "wikilink")
  - [ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")
  - *[Design Patterns](https://ja.wikipedia.org/wiki/:en:Design_Patterns "wikilink")* p. 243

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")