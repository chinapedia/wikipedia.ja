> この記事は[JUnit](https://ja.wikipedia.org/wiki/JUnit)から翻訳されています。


**JUnit**とは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で開発された[プログラムにおいてユニットテスト](../Page/プログラム_\(コンピュータ\).md "wikilink")（[単体テスト](../Page/単体テスト.md "wikilink")）の自動化を行うためのフレームワークである。

## 概要

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に、[Smalltalk](../Page/Smalltalk.md "wikilink") のためのユニットテストのフレームワークである[SUnit](https://ja.wikipedia.org/wiki/SUnit "wikilink")をもとにして、[エーリヒ・ガンマ](../Page/エーリヒ・ガンマ.md "wikilink")と、SUnitの開発者の[ケント・ベック](../Page/ケント・ベック.md "wikilink")が中心となって開発された。

単体でも動作可能だが、[Apache Antや](../Page/Apache_Ant.md "wikilink")[Eclipseのプラグインからも利用可能である](https://ja.wikipedia.org/wiki/統合開発環境Eclipse "wikilink")。[エクストリーム・プログラミング](../Page/エクストリーム・プログラミング.md "wikilink")などの、[アジャイルソフトウェア開発](../Page/アジャイルソフトウェア開発.md "wikilink")のいくつかの開発手法では、テスト重視が推奨されており紹介されることが多い。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の黎明期からテスト実行環境を提供し続けており、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")を用いるシステム開発では必要不可欠になっている。

Java以外の言語向けには[xUnit](https://ja.wikipedia.org/wiki/xUnit "wikilink")が存在する。

## JUnitが推奨される理由

  - 一度作成すればすばやくテスト可能である。
  - その後はテストコードを標本とすることでバグ訂正が容易となる。
  - テストコードを見れば仕様が一目瞭然となる。
  - 誰でも同じテストを行えるようになる。
  - 独自のテストコードによるテスト作成の手間を省ける。

## JUnitの問題点

  - 仕様変更ごとにテストコードを作り直さなければならない。
      - [Eclipseなどの](../Page/Eclipse_\(統合開発環境\).md "wikilink")[IDEを使うことで](../Page/統合開発環境.md "wikilink")、テストコードの再作成によって生じる手間を軽減することもできる。
      - [エクストリーム・プログラミング](../Page/エクストリーム・プログラミング.md "wikilink")(XP)などのテスト駆動開発の開発形態の場合、問題が解消される場合がある。なぜなら、[テスト駆動開発](../Page/テスト駆動開発.md "wikilink")では、テストコード自体が仕様であるという考え方に立つからである。
  - テストコードの作成に時間がかかる。
      - EclipseなどのIDEを使うことでテストコードの作成を高速化することもできる。
      - 「テストは機能テストであり、内部ロジックの確認ではない」という考え方に立つと問題が解消される場合がある。

## JUnit4の新機能

JUnit4は、[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5から[アノテーション](../Page/アノテーション.md "wikilink")が利用可能になったため、従来の命名規則に縛られることがなくなり、さらに使いやすくなった。 従来は、テストクラス名は`Test`で終わる必要があった。テストしたい[メソッドをテストするメソッド名には](../Page/メソッド_\(計算機科学\).md "wikilink")、`test`の接頭辞を付ける必要があった。JUnit4からは、`TestCase#setUp()`, `TestCase#tearDown()`メソッドをオーバーライドする必要は無くなり、かわりに、`setUp()`に相当するメソッドには`@Before`アノテーションをつけ、`tearDown()`に相当するメソッドには`@After`アノテーションをつけるだけで済むようになった。さらに、メソッドに`@BeforeClass`、`@AfterClass`アノテーションをつけることで、テストクラス実行前と実行後に実行したいメソッドを作ることも可能になった。

### JUnit4から利用可能になったアノテーション

  - @Test – そのメソッドがテストメソッドであることを示す。このメソッドにテストを記述する。従来のJUnitでメソッド名が`test`で始まるメソッドと同じ。
  - @Before – このアノテーションが付加されたメソッドは、@Testアノテーションが付いたメソッドを実行するたびに事前に実行されることを意味する。JUnit4以前の`setup()`メソッドと同じ。
  - @After – このアノテーションが付加されたメソッドは、@Testアノテーションが付いたメソッドを実行するたびに、必ず後から実行されることを意味する。JUnit4以前の`tearDown()`メソッドと同じ。
  - @BeforeClass – このアノテーションが付加されたメソッドは、そのテストクラスを呼び出す前に実行される。
  - @AfterClass – このアノテーションが付加されたメソッドは、そのテストクラスを呼び出した後に実行される。

## JUnitから派生したツール/関連ツール

JUnitから派生したツールを下記に示す。

  - [TestNG](../Page/TestNG.md "wikilink") - 'Test the NextGeneration'の略とされている。Java SE 5から追加された[アノテーション](../Page/アノテーション.md "wikilink")を利用して、[クラスや](../Page/クラス_\(コンピュータ\).md "wikilink")[メソッドにTest](../Page/メソッド_\(計算機科学\).md "wikilink")/testと命名する必要がなくなった。JUnit4では、同様に命名規則が緩くなった。他にもJUnit4では使用できない機能が追加されている\[1\]。
  - JxUnit - JUnitはprivateなメソッドをテストできないが、JxUnitはテスト可能。内部で[リフレクション](https://ja.wikipedia.org/wiki/リフレクション "wikilink")を利用している。
  - [Jakarta Cactus](https://ja.wikipedia.org/wiki/Jakarta_Cactus "wikilink") - [Servlet](https://ja.wikipedia.org/wiki/Servlet "wikilink")の単体テストだけでなく、統合テストを実行できる。
  - [MockObject](https://ja.wikipedia.org/wiki/MockObject "wikilink") - テスト用にオブジェクトを偽装する。
  - [djUnit](https://ja.wikipedia.org/wiki/djUnit "wikilink") - JUnitのテストをそのまま実行でき、カバレッジレポートの出力などができる。

## 脚注

## 関連項目

  - [アジャイルソフトウェア開発](../Page/アジャイルソフトウェア開発.md "wikilink")
      - [エクストリーム・プログラミング](../Page/エクストリーム・プログラミング.md "wikilink")
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [xUnit](https://ja.wikipedia.org/wiki/xUnit "wikilink")
  - [ソフトウェアテスト](../Page/ソフトウェアテスト.md "wikilink")
  - [TestNG](../Page/TestNG.md "wikilink")

## 外部リンク

  - [JUnit](http://www.junit.org/)（英語）

[Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:ソフトウェアテスティング](https://ja.wikipedia.org/wiki/Category:ソフトウェアテスティング "wikilink") [Category:エクストリーム・プログラミング](https://ja.wikipedia.org/wiki/Category:エクストリーム・プログラミング "wikilink") [Category:ユニットテスト・フレームワーク](https://ja.wikipedia.org/wiki/Category:ユニットテスト・フレームワーク "wikilink")

1.  参考 [コード品質を追求する: JUnit 4 対 TestNG 大規模なテストでは TestNG のほうが優れたフレームワークになる理由](http://www.ibm.com/developerworks/jp/java/library/j-cq08296/)