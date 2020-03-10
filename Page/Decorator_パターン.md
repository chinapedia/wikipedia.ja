> この記事は[Decorator ](https://ja.wikipedia.org/wiki/Decorator_)から翻訳されています。


**Decorator パターン**（デコレータ・パターン）とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")（Gang of Four; 4人のギャングたち）によって定義された[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。 このパターンは、既存の[オブジェクトに新しい機能や振る舞いを動的に追加することを可能にする](../Page/オブジェクト_\(プログラミング\).md "wikilink")。

## クラス図

Decorator パターンの[クラス図](https://ja.wikipedia.org/wiki/クラス図 "wikilink")を以下に挙げる。

[center](https://ja.wikipedia.org/wiki/ファイル:Decorator_UML_class_diagram.svg "wikilink")

## 概要

Decorator パターンの方針は、既存のオブジェクトを新しい `Decorator` オブジェクトでラップすることである。 その方法として、`Decorator` のコンストラクタの引数でラップ対象の `Component` オブジェクトを読み込み、コンストラクタの内部でそのオブジェクトをメンバに設定することが一般的である。

Decorator パターンは、既存のクラスを拡張する際に[クラスの継承の代替手段として用いられる](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")。継承がコンパイル時に機能を拡張するのに対し、Decorator パターンはプログラムの実行時に機能追加をする点が異なる。

## 利用例

[Java](https://ja.wikipedia.org/wiki/Java "wikilink") による利用例を以下に挙げる。

``` java
/** 価格をあらわすインタフェース */
interface Price{
    int getValue();
}

/** 原価を表すクラス */
class PrimePrice implements Price{
    private int value;
    PrimePrice(int value){
        this.value = value;
    }
    public int getValue(){
        return this.value;
    }
}

/** マージンを介する価格 */
abstract class MarginPrice implements Price{
    protected Price originalPrice;
    MarginPrice(Price price){
        this.originalPrice = price;
    }
}

/** 設定された利益を仕入れ価格に上乗せする Price */
class WholesalePrice extends MarginPrice{
    private int advantage;
    WholesalePrice(Price price, int advantage){
        super(price);
        this.advantage = advantage;
    }
    public int getValue(){
        return this.originalPrice.getValue() + advantage;
    }
}

/** 仕入れ価格の 2 倍の値段を提示する Price */
class DoublePrice extends MarginPrice{
    DoublePrice(Price price){
        super(price);
    }
    public int getValue(){
        return this.originalPrice.getValue() * 2;
    }
}

public class DecoratorTest{
    public static void main(String[] argv){
        System.out.println(
            new WholesalePrice(
                new DoublePrice(
                    new WholesalePrice(
                        new DoublePrice(
                            new PrimePrice(120)
                            )
                        ,80
                        )
                    )
                ,200
                )
            .getValue()
            );
    }
}
```

クラス図との関連は以下の通りである。

  - Component:`Price`
    ConcreteComponent:`PrimePrice`
    Decorator:`MarginPrice`
    ConcreteDecorator:`WholesalePrice`, `DoublePrice`

## 関連項目

  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - [Adapter パターン](https://ja.wikipedia.org/wiki/Adapter_パターン "wikilink")
  - [Abstract Factory パターン](../Page/Abstract_Factory_パターン.md "wikilink")
  - [Composite パターン](https://ja.wikipedia.org/wiki/Composite_パターン "wikilink")
  - [イミュータブル](../Page/イミュータブル.md "wikilink")

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")