> この記事は[TestNG](https://ja.wikipedia.org/wiki/TestNG)から翻訳されています。


**TestNG**（テスティング\[1\]）は、[JUnit](https://ja.wikipedia.org/wiki/JUnit "wikilink")と[NUnit](https://ja.wikipedia.org/wiki/NUnit "wikilink")に触発された[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のための[テスティング](https://ja.wikipedia.org/wiki/ソフトウェアテスト "wikilink")[フレームワークである](https://ja.wikipedia.org/wiki/アプリケーションフレームワーク "wikilink")。TestNGは**Testing, the Next Generation**の略である。

TestNGは以下のような、使用をよりパワフルで容易にするいくつかの新機能を導入している。

  - [Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink")5の[アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")（JDK 1.4 では[JavaDocによってアノテーション同等の機能をサポート](https://ja.wikipedia.org/wiki/Javadoc "wikilink")。しかし、JUnit4でもアノテーションをサポートした）
  - 柔軟なテスト設定。
  - [データ駆動型テスト](https://ja.wikipedia.org/wiki/データ駆動型テスト "wikilink")をサポート(@DataProvider)。
  - テスト[メソッドにアノテーションで指定した値を代入できる引数をサポート](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\) "wikilink")。
  - スレーブマシンでテストの分散を可能に。
  - パワフルな実行モデル（これ以上のTestSuiteが無い）。
  - 豊富なツールとプラグインによるサポート（[Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink"), [IDEA](https://ja.wikipedia.org/wiki/International_Data_Encryption_Algorithm "wikilink"), [Mavenなど](https://ja.wikipedia.org/wiki/Apache_Maven "wikilink")）。
  - さらなる柔軟性を兼ねたBeansShell拡張。
  - 実行と[ロギング](https://ja.wikipedia.org/wiki/ロギング "wikilink")は[JDKの機能がデフォルト](../Page/Java_Development_Kit.md "wikilink")（JDK以外の環境には非依存）。
  - [アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")テストのための依存メソッド。

TestNGはすべてのテストカテゴリをカバーするよう設計されている: ユニットテスト、機能テスト、エンドトゥーエンドテスト、[結合テスト](https://ja.wikipedia.org/wiki/結合テスト "wikilink")、[統合テスト](https://ja.wikipedia.org/wiki/統合テスト "wikilink")その他。

現状では、JUnit4よりも非常に優位な点がいくつか存在する。JUnitは単体テストを重視しているのに対して、TestNGは高レベルなテストや統合テストもできるようになっている。\[2\]

## 外部リンク

  - [TestNG](http://testng.org/)
  - [TestNG javadocs](http://testng.org/javadocs/index-all.html)
  - [jyperion.org TestNG](http://jyperion.org/articles/testng/testng.htm)
  - [TestNG makes Java unit testing a breeze](http://www-128.ibm.com/developerworks/java/library/j-testng/)（注意: 例は非推奨コードを含んでいる可能性がある）

## 脚注

<div class="references-small">

<references/>

</div>

## 関連項目

  - [ソフトウェアテスト](https://ja.wikipedia.org/wiki/ソフトウェアテスト "wikilink")
  - [JUnit](https://ja.wikipedia.org/wiki/JUnit "wikilink")
  - [xUnit](https://ja.wikipedia.org/wiki/xUnit "wikilink")
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [Java Platform, Standard Edition](../Page/Java_Platform,_Standard_Edition.md "wikilink")

[Category:ソフトウェアテスティング](https://ja.wikipedia.org/wiki/Category:ソフトウェアテスティング "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:ユニットテスト・フレームワーク](https://ja.wikipedia.org/wiki/Category:ユニットテスト・フレームワーク "wikilink")

1.  [Next Generation Java Testing](http://www.javalobby.org/articles/testng-david/)
2.  [コード品質を追求する: JUnit 4 対 TestNG 大規模なテストでは TestNG のほうが優れたフレームワークになる理由](http://www.ibm.com/developerworks/jp/java/library/j-cq08296/)