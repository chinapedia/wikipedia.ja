> この記事は[XUnit](https://ja.wikipedia.org/wiki/XUnit)から翻訳されています。


**xUnit**とは、[コンピュータ](../Page/コンピュータ.md "wikilink")[プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[単体テスト](https://ja.wikipedia.org/wiki/ソフトウェアテスト#単体テスト（Unit_Testing） "wikilink")（ユニットテスト）を行うためのテスティング[フレームワークの総称である](https://ja.wikipedia.org/wiki/アプリケーションフレームワーク "wikilink")。これらのフレームワークでは、関数やクラスなど、ソフトウェアの様々な要素（ユニット）をテストすることができる。xUnitフレームワークの主な利点は、テストを自動化できること、同じテストを何度も書かずに済むこと、個々のテストの結果がどうあるべきかを覚えておかなくても良いことである。

このようなフレームワークの最初の実装は、[ケント・ベック](../Page/ケント・ベック.md "wikilink")が開発した[Smalltalk](../Page/Smalltalk.md "wikilink")用のテスティングフレームワーク**[SUnit](https://ja.wikipedia.org/wiki/SUnit "wikilink")**である。その後、各コンピュータ[プログラム言語](https://ja.wikipedia.org/wiki/プログラム言語 "wikilink")や開発環境毎に、同様の設計を持つフレームワークが多数作成されている。xUnitそれ自体は非常に単純なプログラムであるが、近年のソフトウェア開発で採用されつつある。[JUnit](https://ja.wikipedia.org/wiki/JUnit "wikilink")（[Java](https://ja.wikipedia.org/wiki/Java "wikilink")用のxUnit）の項目も参照。

[アジャイルソフトウェア開発](https://ja.wikipedia.org/wiki/アジャイルソフトウェア開発 "wikilink")（[エクストリーム・プログラミング](../Page/エクストリーム・プログラミング.md "wikilink")など）においては、[リファクタリング](../Page/リファクタリング_\(プログラミング\).md "wikilink")・[テストファースト](https://ja.wikipedia.org/wiki/テストファースト "wikilink")等の前提となる重要な要素である。

## xUnitの設計

xUnitフレームワークの設計上の特徴は、いくつかの部分に分けられる。言い換えると、以下の特徴をすべて持つテストフレームワークはxUnitフレームワークの一種であるといえる。

### テストフィクスチャ

テストを実行、成功させるために必要な状態や[前提条件](https://ja.wikipedia.org/wiki/前提条件 "wikilink")の集合を、[フィクスチャ](https://ja.wikipedia.org/wiki/フィクスチャ "wikilink")と呼ぶ。これらはテストコンテキストとも呼ばれる。開発者はテストの実行前にテストに適した状態を整え、テスト実行後に元の状態を復元することが望ましい。

### テストスイート

同じフィクスチャを共有するテストの集合を、テストスイートと呼ぶ。テストスイート内のそれぞれのテストの実行順序は保証されない。

### テストの実行

個々のユニットテストは以下のような流れで実行される。

``` c
setup(); /* 最初に、テストのためのクリーンな
            環境（設定など）を用意する。 */
...
/* テストの本体。ここですべてのテストを行う。 */
...
teardown(); /* 最後は、テストが成功したか失敗したかに関わらず、
               他のテストやプログラムに影響を与えないよう、
               初めに用意したテスト用の環境を元に戻す。 */
```

setup() と teardown() の各メソッドは、テストフィクスチャの初期化とクリーンアップを行うためのものである。

### アサーション（表明、検証）

テスト対象の関数やクラスなどについて、振る舞いや状態を確認するための関数やマクロを、[アサーションと呼ぶ](https://ja.wikipedia.org/wiki/表明 "wikilink")。アサーションが失敗した時（実際の実行結果が期待される結果と異なっていた場合）は、一般的には、例外が投げられ現在のテストの実行は中断される。

## xUnitの一覧

  - [JUnit](https://ja.wikipedia.org/wiki/JUnit "wikilink"), [TestNG](../Page/TestNG.md "wikilink")（[Java](https://ja.wikipedia.org/wiki/Java "wikilink")用）
  - [SUnit](http://sunit.sourceforge.net/)（[Smalltalk](../Page/Smalltalk.md "wikilink")用）
  - [CUnit](http://cunit.sourceforge.net/), [Cutter](http://cutter.sourceforge.net/index.html.ja)（[C言語](../Page/C言語.md "wikilink")用）
  - [CppUnit](http://sourceforge.net/projects/cppunit/), [Cutter](http://cutter.sourceforge.net/index.html.ja)（[C++](../Page/C++.md "wikilink")用）
  - VBUnit（[Visual Basic用](../Page/Visual_Basic.md "wikilink")）
  - [DUnit](http://dunit.sourceforge.net/)（[Delphi](../Page/Delphi.md "wikilink")用）
  - PBUnit（[PowerBuilder](https://ja.wikipedia.org/wiki/PowerBuilder "wikilink")用）
  - [PerlUnit](http://dunit.sourceforge.net/)（[Perl](../Page/Perl.md "wikilink")用）
  - [PyUnit](http://pyunit.sourceforge.net/), [nose](http://code.google.com/p/python-nose/) ([Python](../Page/Python.md "wikilink")用)
  - [RubyUnit](http://homepage1.nifty.com/markey/ruby/rubyunit/index.html)\[1\], [Test::Unit](http://test-unit.rubyforge.org/)（[Ruby](../Page/Ruby.md "wikilink")用）
  - [NUnit](http://www.nunit.org/), [xUnit.net](https://xunit.github.io/)（[.NET Framework用](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")）
  - [tclUnit](http://tclunit.sourceforge.net/)（[Tcl/Tk](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")用）
  - [HUnit](http://hunit.sourceforge.net/)（[Haskell](../Page/Haskell.md "wikilink")用）
  - [OUnit](http://ounit.forge.ocamlcore.org/)（[Objective Caml用](https://ja.wikipedia.org/wiki/Objective_Caml "wikilink")）
  - [PHPUnit](http://phpunit.de/)（[PHP用](../Page/PHP_\(プログラミング言語\).md "wikilink")）
  - [JsUnit](http://www.jsunit.net/), [MochiKit](https://ja.wikipedia.org/wiki/MochiKit "wikilink")（[MochiKit](https://ja.wikipedia.org/wiki/:en:MochiKit "wikilink") 英語版Wikipedia）[本家](http://mochikit.com/)（[JavaScript](../Page/JavaScript.md "wikilink")用）
  - [HttpUnit](http://httpunit.sourceforge.net/)（[HTTPによる通信を擬似的に行う](../Page/Hypertext_Transfer_Protocol.md "wikilink")）
  - [HtmlUnit](http://htmlunit.sourceforge.net/)（Webベースのアプリケーション用。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の[エミュレータ](../Page/エミュレータ_\(コンピュータ\).md "wikilink")）

## 関連項目

  - [ユニットテスト・フレームワーク一覧](https://ja.wikipedia.org/wiki/ユニットテスト・フレームワーク一覧 "wikilink")

## 脚注

[Category:ソフトウェアテスティング](https://ja.wikipedia.org/wiki/Category:ソフトウェアテスティング "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:ユニットテスト・フレームワーク](https://ja.wikipedia.org/wiki/Category:ユニットテスト・フレームワーク "wikilink")

1.  Test::UnitとしてRuby1.8の標準添付ライブラリに統廃合された。