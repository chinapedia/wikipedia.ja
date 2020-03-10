> この記事は[Factory Method ](https://ja.wikipedia.org/wiki/Factory_Method_)から翻訳されています。


**Factory Method パターン**（ファクトリメソッド・パターン）\[1\]とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink") (Gang of Four; 四人組)によって定義された[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。 Factory Method パターンは、他のクラスのコンストラクタをサブクラスで上書き可能な自分のメソッドに置き換えることで、 アプリケーションに特化したオブジェクトの生成をサブクラスに追い出し、クラスの再利用性を高めることを目的とする。

Virtual Constructor パターンとも呼ばれる\[2\]。

## クラス図

Factory Method パターンの[クラス図](https://ja.wikipedia.org/wiki/クラス図 "wikilink")は以下の通りである。

[center|500px|抽象クラス Creator は 抽象クラス Product を生成するメソッドを持つ。 クラス ConcreteCreator は Creator の具象クラスであり、ConcreteProduct を生成するメソッドを持つ。 ConcreteProduct は Product の具象クラスである。](https://ja.wikipedia.org/wiki/画像:Factory_Method_UML_class_diagram.svg "wikilink")

ここで、anOperationはfactoryMethodを呼び出し、Productのサブクラスのインスタンスを得て、利用する。factoryMethodのようなメソッドはfactory methodと呼ばれる。

factoryMethodは、デフォルトの動作を含んだ具象メソッドである場合もある。パラメータを取り、それによって生成するクラスを変えることもある。ConcreteCreatorごとの操作手段を Productとして他のクラスに提供するようなケースでは、factoryMethodをpublicとして公開する。\[3\]。しかし、factoryMethodは上書きされることが前提であるため、privateにはしない。

## 利用例

例として、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") でリストの要素をさまざまな順で表示するプログラムを考える。このソースコードは J2SE 1.5 以降のバージョンで動作する。

``` java
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collections;
import java.util.Comparator;
import java.util.List;

// Creatorに相当する
abstract class ListPrinter {
    // anOperationに相当する
    public void printList(List<String> list) {
        Comparator<String> comparator = createComparator();
        list = new ArrayList<String>(list);

        Collections.sort(list, comparator);

        for (String item : list) {
            System.out.println(item);
        }
    }

    // factoryMethodに相当する
    protected abstract Comparator<String> createComparator();
}

// ConcreteCreatorに相当する
class DictionaryOrderListPrinter extends ListPrinter {
    @Override
    protected Comparator<String> createComparator() {
        return new DictionaryOrderComparator();
    }
}

// java.util.ComparatorがProductに相当する

// ConcreteProductに相当する
class DictionaryOrderComparator implements Comparator<String> {
    @Override
    public int compare(String str1, String str2) {
        return str1.compareTo(str2);
    }
}

// ConcreteCreatorに相当する
class LengthOrderListPrinter extends ListPrinter {
    @Override
    protected Comparator<String> createComparator() {
        return new LengthOrderComparator();
    }
}

// ConcreteProductに相当する
class LengthOrderComparator implements Comparator<String> {
    public int compare(String str1, String str2) {
        return str1.length() - str2.length();
    }
}

// メインクラス
public class FactoryMethodSample {
    public static void main(String args[]) {
        List<String> list = Arrays.asList("いちご", "もも", "いちじく");

        System.out.println("五十音順で表示:");
        new DictionaryOrderListPrinter().printList(list);

        System.out.println();

        System.out.println("長さ順で表示:");
        new LengthOrderListPrinter().printList(list);
    }
}
```

このプログラムは、以下の結果を出力する。

`五十音順で表示:`
`いちご`
`いちじく`
`もも`

`長さ順で表示:`
`もも`
`いちご`
`いちじく`

前半ではリストを五十音順で表示し、後半ではリストを文字列の長さ順に表示している。 リストを並び変えて表示する[ListPrinter\#printListメソッドでは](https://ja.wikipedia.org/wiki/#ListPrinter-printList "wikilink")、並び変えに使うComparatorを生成する際にnew演算子を使って直接生成するのではなく、抽象メソッドcreateComparatorを使ってサブクラスに生成を委ねる。

## 関係するパターン

factory methodは普通template method ([Template Method パターンを参照](../Page/Template_Method_パターン.md "wikilink"))であるanOperationから呼ばれる。ただし、factory methodをpublicにして他のクラスからも呼ぶ場合もある\[4\]。

[Abstract Factory パターンのAbstractFactoryクラスはfactory](https://ja.wikipedia.org/wiki/Abstract_Factory_パターン "wikilink") methodを持ち、それを個々のサブクラスが上書きして生成するProductを変える手法が一般的である。しかし、[Prototype パターンを使い](https://ja.wikipedia.org/wiki/Prototype_パターン "wikilink")、prototypeとなるオブジェクトの変更により生成するProductを変える手法もある\[5\]。

## Abstract Factory パターンとの違い

『オブジェクト指向における再利用のためのデザインパターン』においてはFactory Method パターンは「クラスパターン」に分類されている。一方Abstract Factory パターンは「オブジェクトパターン」に分類されている。

Factory Method パターンは親クラスであるCreatorクラスが子クラスであるConcreteCreatorクラスにオブジェクトの生成を委ねるという、CreatorクラスとConcreteCreatorクラスとの関連である。一方でAbstract Factory パターンは、ClientのインスタンスがConcreteFactoryのインスタンスにオブジェクトの生成を委ねるという、オブジェクト同士の関連である。

## 関連項目

  - [Template Method パターン](../Page/Template_Method_パターン.md "wikilink")
  - [Abstract Factory パターン](https://ja.wikipedia.org/wiki/Abstract_Factory_パターン "wikilink")
  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")

## 参考文献

<references/>

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")

1.  [エリック・ガンマ](https://ja.wikipedia.org/wiki/エーリヒ・ガンマ "wikilink")、[ラルフ・ジョンソン](https://ja.wikipedia.org/wiki/ラルフ・ジョンソン "wikilink")、[リチャード・ヘルム](https://ja.wikipedia.org/wiki/リチャード・ヘルム "wikilink")、[ジョン・ブリシディース](https://ja.wikipedia.org/wiki/ジョン・ブリシディース "wikilink")（著）、[グラディ・ブーチ](https://ja.wikipedia.org/wiki/グラディ・ブーチ "wikilink")（まえがき）、本位田真一、吉田和樹（監訳）、『オブジェクト指向における再利用のためのデザインパターン』、[ソフトバンクパブリッシング](https://ja.wikipedia.org/wiki/ソフトバンクパブリッシング "wikilink")、1995。ISBN 978-4-7973-1112-9.
2.
3.
4.
5.