> この記事は[Template Method ](https://ja.wikipedia.org/wiki/Template_Method_)から翻訳されています。


**Template Method パターン**（テンプレート・メソッド・パターン）とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")(Gang of Four; 4人のギャングたち)によって定義された[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。「振る舞いに関するパターン」に属する。Template Method パターンの目的は、ある処理のおおまかなアルゴリズムをあらかじめ決めておいて、そのアルゴリズムの具体的な設計をサブクラスに任せることである。そのため、システムの[フレームワークを構築するための手段としてよく活用される](https://ja.wikipedia.org/wiki/アプリケーションフレームワーク "wikilink")。

## クラス図

以下に Template Method パターンの[クラス図](https://ja.wikipedia.org/wiki/クラス図 "wikilink")を挙げる。

[center](https://ja.wikipedia.org/wiki/画像:Template_Method_UML_class_diagram.svg "wikilink")

`AbstractClass` で定義されている抽象メソッドの可視性が protected なのは、このメソッドが `AbstractClass#templateMethod()` 内でのみ使用されることを想定しているからである。

## 利用例

以下に**Template Method パターン**を使って文字列型配列をリストアップする[Java](https://ja.wikipedia.org/wiki/Java "wikilink")プログラムの例を示す。 なお、このソースコードは可読性のために [Java SE 5](../Page/Java_Platform,_Standard_Edition.md "wikilink") 以降で採用された「[拡張for文](https://ja.wikipedia.org/wiki/Foreach文#Java_5.0以降 "wikilink")」という構文が使用されているため \[1\] J2SE 1.4 以前のバージョンでは動作しない。

``` java
abstract class StringLister {
    abstract String formatHeader();
    abstract String formatItem(String item);
    abstract String formatFooter();
    final String display(String[] items) {
        StringBuilder result = new StringBuilder(this.formatHeader());
        for(String item : items) result.append(this.formatItem(item));
        result.append(this.formatFooter());
        return result.toString();
    }
}

class PlainTextStringLister extends StringLister{
    String formatHeader(){
        return "";
    }
    String formatItem(String item){
        return " - " + item + "\r\n";
    }
    String formatFooter(){
        return "";
    }
}

class HtmlStringLister extends StringLister{
    String formatHeader(){
        return "<ul>\r\n";
    }
    String formatItem(String item){
        return "  <li>" + item + "</li>\r\n";
    }
    String formatFooter(){
        return "</ul>\r\n";
    }
}

public class TemplateMethodTest{
    public static void main(String[] argv){
        String[] items = {"First", "Second", "Third"};
        StringLister l1 = new PlainTextStringLister();
        StringLister l2 = new HtmlStringLister();
        System.out.println(l1.display(items));
        System.out.println(l2.display(items));
    }
}
```

このサンプルを実行すると、次の実行結果が得られる。最初の3行が `PlainTextStringLister#display()` の返り値で、空行を挟んでその後にある出力が `HtmlStringLister#display()` の返り値である。

` - First`
` - Second`
` - Third`


  - First
  - Second
  - Third

参考までに、クラス図との対応関係を示す。

  - AbstractClass:[StringLister](https://ja.wikipedia.org/wiki/#StringLister "wikilink")
    AbstractClass\#templateMethod():[StringLister\#display()](https://ja.wikipedia.org/wiki/#StringLister-display "wikilink")
    ConcreteClass:[PlainTextStringLister](https://ja.wikipedia.org/wiki/#PlainTextStringLister "wikilink"),[HtmlStringLister](https://ja.wikipedia.org/wiki/#HtmlStringLister "wikilink")

## 関係するパターン

[Factory Method パターンは](https://ja.wikipedia.org/wiki/Factory_Method_パターン "wikilink")、内部に Template Method パターンを包含することが多い。

## 関連項目

  - [Factory Method パターン](https://ja.wikipedia.org/wiki/Factory_Method_パターン "wikilink")
  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")

## 脚注

<references/>

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")

1.  拡張for文を使わなくても同等のプログラムを書くことは出来る。