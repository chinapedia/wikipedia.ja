> この記事は[Adapter パターン](https://ja.wikipedia.org/wiki/Adapter_パターン)から翻訳されています。


**Adapter パターン**（アダプター・パターン）とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink") (Gang of Four; 4人のギャングたち) によって定義された[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。Adapter パターンを用いると、既存の[クラスに対して修正を加えることなく](../Page/クラス_\(コンピュータ\).md "wikilink")、[インタフェースを変更することができる](../Page/インタフェース_\(情報技術\).md "wikilink")。Adapter パターンを実現するための手法として[継承を利用した手法と](../Page/継承_\(プログラミング\).md "wikilink")[委譲](../Page/委譲.md "wikilink")を利用した手法が存在する。それぞれについて以下の節で説明する。

## 継承を利用したAdapter

[継承を利用したAdapterは](../Page/継承_\(プログラミング\).md "wikilink")、利用したいクラスの[サブクラスを作成し](../Page/サブクラス_\(計算機科学\).md "wikilink")、そのサブクラスに対して必要な[インタフェースを実装することで実現される](../Page/インタフェース_\(情報技術\).md "wikilink")。

### サンプルプログラム

下記の例において、Product[クラスは既存のクラスであり修正できないものとする](../Page/クラス_\(コンピュータ\).md "wikilink")。 ここで、Productクラスを利用したい開発者がいて、 その開発者はgetPriceという[メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")でProductの値段を取得したいとする。 この場合、ProductAdapterというAdapterを作成することで、既存クラス(Product)クラスを修正することなく、 異なる[インタフェースを持たせることができる](../Page/インタフェース_\(情報技術\).md "wikilink")。 このように、既存クラスを修正することなく、異なるインタフェースを持たせるということが、**Adapter パターン**の役割である。

``` java
interface ProductPrice{
  public int getPrice();
}

class Product{
  private int cost;
  public int getCost(){
    return cost;
  }
}

class ProductAdapter extends Product implements ProductPrice{
  public int getPrice(){
    return this.getCost();
  }
}
```

### クラス図

継承を利用したAdapterの[クラス図](../Page/クラス図.md "wikilink")は以下のようになる。

[center](https://ja.wikipedia.org/wiki/ファイル:Adapter_using_inheritance_UML_class_diagram.svg "wikilink")

参考までに、上のサンプルコードとこのクラス図との対応を示す。

  - Target:[ProductPrice](https://ja.wikipedia.org/wiki/#ProductPrice "wikilink")
    Target\#requiredMethod:[ProductPrice\#getPrice()](https://ja.wikipedia.org/wiki/#ProductPrice-getPrice "wikilink")
    Adapter:[ProductAdapter](https://ja.wikipedia.org/wiki/#ProductAdapter "wikilink")
    Adapter\#requiredMethod:[ProductAdapter\#getPrice()](https://ja.wikipedia.org/wiki/#ProductAdapter-getPrice "wikilink")
    Adaptee:[Product](https://ja.wikipedia.org/wiki/#Product "wikilink")
    Adaptee\#oldMethod:[Product\#getCost()](https://ja.wikipedia.org/wiki/#Product-getCost "wikilink")

## 委譲を利用したAdapter

委譲を利用したAdapterは、利用したいクラスの[インスタンス](../Page/インスタンス.md "wikilink")を生成し、そのインスタンスを他クラスから利用することで実現される。

### サンプルプログラム

``` java
interface ProductPrice{
  public int getPrice();
}

class Product{
  private int cost;
  public int getCost(){
    return cost;
  }
}

class ProductAdapter implements ProductPrice{
  private Product product = new Product();
  public int getPrice(){
    return product.getCost();
  }
}
```

### クラス図

委譲を利用したAdapterの[クラス図](../Page/クラス図.md "wikilink")は以下のようになる。

[center](https://ja.wikipedia.org/wiki/ファイル:Adapter_using_delegation_UML_class_diagram.svg "wikilink") ※上図において、extendsはimplementsでも良い。

こちらのほうも、参考までにサンプルコードの対応を示す。

  - Target:[ProductPrice](https://ja.wikipedia.org/wiki/#ProductPrice2 "wikilink")
    Target\#requiredMethod():[ProductPrice\#getPrice()](https://ja.wikipedia.org/wiki/#ProductPrice-getPrice2 "wikilink")
    Adapter:[ProductAdapter](https://ja.wikipedia.org/wiki/#ProductAdapter2 "wikilink")
    Adapter\#requiredMethod():[ProductAdapter\#getPrice()](https://ja.wikipedia.org/wiki/#ProductAdapter-getPrice2 "wikilink")
    Adaptee:[Product](https://ja.wikipedia.org/wiki/#Product2 "wikilink")
    Adaptee\#oldMethod():[Product\#getCost()](https://ja.wikipedia.org/wiki/#Product-getCost2 "wikilink")

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")