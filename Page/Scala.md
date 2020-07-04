> この記事は[Scala](https://ja.wikipedia.org/wiki/Scala)から翻訳されています。


**Scala**（スカラ、\[1\]）は[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")と[関数型言語](../Page/関数型言語.md "wikilink")の特徴を統合したマルチパラダイムの[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。名前の「」は英語の「」に由来するものである。

## プラットフォーム

主に[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")（[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")）上で動作し、既存の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のプログラムと容易に連携させることができる。2.13.0時点ではほかに[JavaScript](../Page/JavaScript.md "wikilink")への[トランスパイル](https://ja.wikipedia.org/wiki/トランスパイル "wikilink")や[LLVM](../Page/LLVM.md "wikilink")もサポートする\[2\]。 また、過去には下記のプラットフォームもサポートしていたが、現在は開発が中断している。

  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")\[3\]
  - [Java Platform, Micro Edition](../Page/Java_Platform,_Micro_Edition.md "wikilink") [CLDC](../Page/Connected_Limited_Device_Configuration.md "wikilink")

## 歴史

Scalaは2001年にスイス・ローザンヌにあるスイス連邦工科大学 (EPFL) の教授によって設計された。マーティン・オーダスキー教授はFunnelという関数型言語の[ペトリネット](../Page/ペトリネット.md "wikilink")を合わせた言語の開発に携わっていた。オーダスキーは過去にGeneral Javaと[javac](https://ja.wikipedia.org/wiki/javac "wikilink")の開発に携わった事があった。

Scalaは2003年の暮れに内部で公開された後、2004年の始めにJavaのプラットフォームにリリースされ、2004年の6月に.NETのプラットフォームに公開された。Ver2.0は2006年3月にリリースされたが、.NETのサポートは2012年に中止になった。

## 特徴

主に以下のような特徴がある。

  - 開発生産性を高める簡潔な表記が可能である。
  - Javaの豊富なライブラリが使える（.NET Framework上で実行する場合、.NETのライブラリが使える）。
  - 全てがオブジェクトとして扱われるオブジェクト指向言語である。
  - [静的型付け](https://ja.wikipedia.org/wiki/静的型付け "wikilink")を行う関数型言語である。静的型付けのため、コンパイル時点でのエラー（特に型関連の）検出が得意である。
  - 型（クラス）をJavaなどと比べてより容易に作ることができ、また、型を使った条件分岐をはじめとして、型に関する機能が豊富なため、メソッドやフィールドを束ねるだけのクラスではなく、型に積極的な意味を持たせてのプログラミングが可能である。
  - [型推論](../Page/型推論.md "wikilink")をサポートし、多くの場面で型を自動的に補ってくれる。
  - 純粋関数型言語的な、val（定数）と不変List, Set, Mapという組み合わせでもプログラミングできるし、より手続き型的なvar（変数）と可変List, Set, Mapという組み合わせでもプログラミングができる。
  - 関数もオブジェクトとして利用可能であり、[カリー化](../Page/カリー化.md "wikilink")が可能。
  - パターンマッチを利用可能であり、任意のクラスをグループ化してパターンマッチで判定させることが可能（CASEクラス）。
  - implicit def と言う宣言を用いて、既存の[クラスを拡張したような記述が可能](../Page/クラス_\(コンピュータ\).md "wikilink")。
  - traitクラスを用いた、Mix-in機能を持つ。
  - [クロージャ](../Page/クロージャ.md "wikilink")をサポートする。
  - [XMLを直接プログラム内部に記述可能](../Page/Extensible_Markup_Language.md "wikilink")。
  - [遅延評価](../Page/遅延評価.md "wikilink")のある関数型言語であるため、無限リストを扱え、標準ライブラリにそのためのクラスが提供されている。
  - [構文解析](../Page/構文解析.md "wikilink")のための、が標準ライブラリに入っている。

## 例

「文字列の中に'a'という文字が存在するか判定する」という例を挙げる。

手続き型言語的なコードを書くと以下のようになる。

``` scala
def hasLowerCaseA(s: String): Boolean = {
  for (i <- 0 until s.length) {
    if (s(i) == 'a') return true
  }
  return false
}
```

上のコードは、添え字を使わずに、次のように書くことができる。

``` scala
def hasLowerCaseA(s: String): Boolean = {
  for (c <- s) {
    if (c == 'a') return true
  }
  return false
}
```

上のコードは、[トレイト](https://ja.wikipedia.org/wiki/トレイト "wikilink")`scala.collection.Traversable`を使って、次のように書くことができる。

``` scala
def hasLowerCaseA(s: String) = s.exists(_ == 'a')
```

典型的な関数型言語では再帰をよく使う。再帰に置き換えると以下のようになる。

``` scala
def hasLowerCaseA(s: String, i: Int = 0): Boolean = {
  if (i == s.length) return false
  if (s(i) == 'a') return true
  return hasLowerCaseA(s, i + 1)
}
```

### 部分関数

Scalaの[部分関数](https://ja.wikipedia.org/wiki/部分関数 "wikilink") (partial function) は数学における同名の概念をもとにして生まれた機能である。具体的には、[定義域](../Page/定義域.md "wikilink")が制限された関数に相当する。以下は \[-1, +1\] の範囲で2乗を計算する部分関数の例である。

``` scala
val myPartialSquare: PartialFunction[Double, Double] = {
  case x if -1 <= x && x <= 1 => x * x
}

println(myPartialSquare(-0.5)) // 0.25
println(myPartialSquare(0.9)) // 0.81
println(myPartialSquare.isDefinedAt(1)) // true
println(myPartialSquare.isDefinedAt(-10)) // false
println(myPartialSquare(1.1)) // MatchError
```

## Scala開発の動機

Martin Oderskyによると、Scala開発の動機は2つの仮説による。

1.  汎用言語は**スケーラブル**でなくてはならない。同じ概念で、小さいプログラムも大きなプログラムも記述できるべきである。
2.  [スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")は[関数型言語](../Page/関数型言語.md "wikilink")と[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語の2つのプログラミングの概念を統合し、一般化することにより実現できる。

## 利用例

[Twitter](../Page/Twitter.md "wikilink")がバックエンドを[Ruby](../Page/Ruby.md "wikilink")からScalaに[2009年](../Page/2009年.md "wikilink")に移行した\[4\]のを初め、大型のソフトウェアでの利用例がいくつか存在する。

  - [Foursquare](https://ja.wikipedia.org/wiki/Foursquare "wikilink")はScalaと[Lift](https://ja.wikipedia.org/wiki/Lift "wikilink")[フレームワークを利用している](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")\[5\]。（Liftは[Ruby on Rails類似の機能を持つScala上のフレームワーク](../Page/Ruby_on_Rails.md "wikilink")）
  - [イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の大手[新聞](../Page/新聞.md "wikilink")[ガーディアン](../Page/ガーディアン.md "wikilink")は[2011年](../Page/2011年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")ウェブサイトの運用を[Java](https://ja.wikipedia.org/wiki/Java "wikilink")からScalaに移行すると発表した。
  - [LinkedIn](https://ja.wikipedia.org/wiki/LinkedIn "wikilink")
  - [スイス銀行](../Page/スイス銀行.md "wikilink")
  - [ニコニコ生放送](https://ja.wikipedia.org/wiki/ニコニコ生放送 "wikilink")
  - [Apache Spark](https://ja.wikipedia.org/wiki/Apache_Spark "wikilink")
  - [スタディサプリ](https://ja.wikipedia.org/wiki/スタディサプリ "wikilink")

## 脚注

## 関連項目

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM)
  - [Groovy](../Page/Groovy.md "wikilink")
  - [Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")
  - [Kojo](https://ja.wikipedia.org/wiki/Kojo "wikilink")

## 外部リンク

  - [Scala website](http://www.scala-lang.org/)
  - [Scala Documentation 日本語版](https://docs.scala-lang.org/ja/)
  - [A Scala Tutorial for Java Programmer の和訳](http://www29.atwiki.jp/tmiya/pages/11.html) - オフィシャルチュートリアルの和訳
  - [ScalaによるWebアプリケーションフレームワークLiftの公式サイト](http://www.liftweb.net/)
      - [日本語訳](http://oss.infoscience.co.jp/scala/liftweb.net/)（あしたのオープンソース研究所）
  - [日本Scalaユーザーズグループ (ScalaJP)](http://jp.scala-users.org/)
  - [sbt — sbt Documentation](http://www.scala-sbt.org/) - ScalaおよびJava向けのビルドツール

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Java仮想マシンで動作するプログラミング言語](https://ja.wikipedia.org/wiki/Category:Java仮想マシンで動作するプログラミング言語 "wikilink")

1.  [Scala: Martin Odersky, Scala -- the Simple Parts](https://www.youtube.com/watch?v=ecekSCX3B4Q:SF)
2.  [The Scala Programming Language](https://www.scala-lang.org/)内Scara runs on...セクション
3.  [A Brief History of Scala](http://www.artima.com/weblogs/viewpost.jsp?thread=163733)
4.  [The Secret Behind Twitter's Growth](http://www.technologyreview.com/blog/editors/23282/?nlid=1908)
5.  [Scala, Lift, and the Future](http://grenadesandwich.com/blog/steven/2009/11/27/scala-lift-and-future/)