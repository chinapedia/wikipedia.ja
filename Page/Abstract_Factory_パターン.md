> この記事は[Abstract Factory ](https://ja.wikipedia.org/wiki/Abstract_Factory_)から翻訳されています。


**Abstract Factory パターン**（アブストラクト・ファクトリ・パターン）\[1\]とは、[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")（Gang of Four; 4人のギャングたち）によって定義された[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。 関連するインスタンス群を生成するための [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") を集約することによって、複数のモジュール群の再利用を効率化することを目的とする。日本語では「抽象的な工場」と翻訳される事が多い。

Kit パターンとも呼ばれる\[2\]。

## クラス図

Abstract Factory パターンの[クラス図](../Page/クラス図.md "wikilink")を以下に挙げる。 [center](https://ja.wikipedia.org/wiki/ファイル:Abstract_Factory_UML_class_diagram.svg "wikilink")

## 利用例

## 応用例

[DOM](../Page/Document_Object_Model.md "wikilink") は Abstract Factory パターンを応用した API の一つである。参考までに、クラス図との対応関係を示す。

  - AbstractFactory:[org.w3c.dom.Document](http://download.java.net/jdk/jdk-api-localizations/jdk-api-ja/builds/latest/html/ja/api/org/w3c/dom/Document.html)
    AbstractFactory\#createProduct():\[<http://download.java.net/jdk/jdk-api-localizations/jdk-api-ja/builds/latest/html/ja/api/org/w3c/dom/Document.html#createElement(java.lang.String>) org.w3c.dom.Document\#createElement(String)\], \[<http://download.java.net/jdk/jdk-api-localizations/jdk-api-ja/builds/latest/html/ja/api/org/w3c/dom/Document.html#createTextNode(java.lang.String>) org.w3c.dom.Document\#createTextNode(String)\] など
    Product:[org.w3c.dom.Element](http://download.java.net/jdk/jdk-api-localizations/jdk-api-ja/builds/latest/html/ja/api/org/w3c/dom/Element.html), [org.w3c.dom.Text](http://download.java.net/jdk/jdk-api-localizations/jdk-api-ja/builds/latest/html/ja/api/org/w3c/dom/Text.html) など

## 関連するパターン

生成するProductを変更する手法としては、AbstractFactoryクラスがfactory method（[Factory Method パターンを参照](../Page/Factory_Method_パターン.md "wikilink")）を持ち、それを個々のConcreteFactoryが上書きする手法が一般的である。しかし、[Prototype パターンを使い](https://ja.wikipedia.org/wiki/Prototype_パターン "wikilink")、prototypeとなるオブジェクトの変更により生成するProductを変える手法もある\[3\]。

ConcreteFactoryは、singletonオブジェクト（[Singleton パターンを参照](../Page/Singleton_パターン.md "wikilink")）であることもある。

## Factory Method パターンとの違い

『オブジェクト指向における再利用のためのデザインパターン』においてはFactory Method パターンは「クラスパターン」に分類されている。一方Abstract Factory パターンは「オブジェクトパターン」に分類されている。

Factory Method パターンは親クラスであるCreatorクラスが子クラスであるConcreteCreatorクラスにオブジェクトの生成を委ねるという、CreatorクラスとConcreteCreatorクラスとの関連である。一方でAbstract Factory パターンは、ClientのインスタンスがConcreteFactoryのインスタンスにオブジェクトの生成を委ねるという、オブジェクト同士の関連である。

## 関連項目

  - [Factory Method パターン](../Page/Factory_Method_パターン.md "wikilink")
  - [Prototype パターン](https://ja.wikipedia.org/wiki/Prototype_パターン "wikilink")
  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - [Document Object Model](../Page/Document_Object_Model.md "wikilink")

## 参考文献

<references/>

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink") [Category:抽象](https://ja.wikipedia.org/wiki/Category:抽象 "wikilink")

1.  [エリック・ガンマ](../Page/エーリヒ・ガンマ.md "wikilink")、[ラルフ・ジョンソン](https://ja.wikipedia.org/wiki/ラルフ・ジョンソン "wikilink")、[リチャード・ヘルム](https://ja.wikipedia.org/wiki/リチャード・ヘルム "wikilink")、[ジョン・ブリシディース](../Page/ジョン・ブリシディース.md "wikilink")（著）、[グラディ・ブーチ](../Page/グラディ・ブーチ.md "wikilink")（まえがき）、本位田真一、吉田和樹（監訳）、『オブジェクト指向における再利用のためのデザインパターン』、[ソフトバンクパブリッシング](https://ja.wikipedia.org/wiki/ソフトバンクパブリッシング "wikilink")、1995。ISBN 978-4-7973-1112-9.
2.
3.