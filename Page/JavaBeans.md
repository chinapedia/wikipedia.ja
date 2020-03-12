> この記事は[JavaBeans](https://ja.wikipedia.org/wiki/JavaBeans)から翻訳されています。


**JavaBeans**（ジャバ ビーンズ）とは、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれた再利用可能な[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")またはその技術仕様のこと。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")後半に登場。JDKの`java.beans`パッケージと共に[RAD環境の構築を支援するために作られた](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")。現在では`java.beans`パッケージの技術を活用し、RAD環境の構築に限らずJSP等幅広い用途で利用されている。

## 概要

Java Beansはプログラムの再利用を目的としており、汎用的なロジックで構成されているクラスである。Javaで作成された移植可能なプラットフォームに依存しないコンポーネント・モデルで、JavaBean仕様に従う\[1\]。 サーバーサイド向けのJavaBeansは[Enterprise JavaBeansと呼ばれている](../Page/Enterprise_JavaBeans.md "wikilink")。 `java.beans`パッケージには、Beanの要件に沿ったGUIコンポーネントを編集するためのインターフェースとなるクラスが用意されており\[2\]、それらのクラスを利用することでRAD環境の開発者はGUIコンポーネントのクラスに依存しないRAD環境を構築することができると共に、構築を効率化することができる。

## Beanの必要条件

  - publicで引数なしの[コンストラクタ](../Page/コンストラクタ.md "wikilink")が必要
  - [メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")の命名規則に従わなくてはならない(getter/setterメソッドが必要など)
  - [シリアライズ](../Page/シリアライズ.md "wikilink")可能でなくてはならない

など。

## 役割

`java.util.Observable`や`java.beans.PropertyChangeSupport`と組み合わせることで[Model View Controller](../Page/Model_View_Controller.md "wikilink")（MVC）ではModelに相当する役割をさせることができる。

## 注釈

<references/>

## 関連項目

  - [EJB](../Page/Enterprise_JavaBeans.md "wikilink")

## 外部リンク

  - <https://docs.oracle.com/javase/jp/6/api/java/beans/package-summary.html>
  - [JavaBeans Component API](https://docs.oracle.com/javase/jp/1.5.0/guide/beans/index.html)
  - [Oracle Javaロードマップ:JavaBeans](http://otndnld.oracle.co.jp/tech/java/htdocs/java_roadmap/javabean/listing.htm)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink")

1.  [オラクルの用語集より](http://otndnld.oracle.co.jp/tech/java/htdocs/java_roadmap/glossary.htm#434709)
2.  <https://docs.oracle.com/javase/jp/6/api/java/beans/package-summary.html>