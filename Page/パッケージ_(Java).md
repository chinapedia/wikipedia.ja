> この記事は[パッケージ \(Java\)](https://ja.wikipedia.org/wiki/パッケージ_\(Java\))から翻訳されています。


**Javaパッケージ**(<em lang="en">**Java package**</em>)は[名前空間](../Page/名前空間.md "wikilink")の中にある[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[クラスをまとめるメカニズムである](../Page/クラス_\(コンピュータ\).md "wikilink")。Javaパッケージは、[JARファイルと呼ばれる圧縮ファイルの中に保存することができ](https://ja.wikipedia.org/wiki/Jar "wikilink")、クラス群を一つのグループとしてまとめた方が1つずつダウンロードするよりも高速化される。プログラマも一般に同じカテゴリに属しているクラスや類似した機能を提供するクラスをまとめたパッケージを使う。

Java[ソースファイル](https://ja.wikipedia.org/wiki/ソースファイル "wikilink")はファイルの先頭にソースファイルが定義したクラスのパッケージを明示する**`package`**構文を含むことができる。

  - パッケージはそれが含むタイプに関してユニークな名前空間を提供する。
  - 同じパッケージにあるクラス群はお互いに保護された(`protected`)メンバにアクセスできる。
  - パッケージは次に述べる種類の[型を含むことができる](../Page/データ型.md "wikilink")。
      - [クラス](../Page/クラス_\(コンピュータ\).md "wikilink")
      - [インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")
      - [列挙型](../Page/列挙型.md "wikilink")
      - [アノテーション](../Page/アノテーション.md "wikilink")

[C++](../Page/C++.md "wikilink")などの言語に使われている[namespace (名前空間)に似ているが](../Page/名前空間.md "wikilink")、その名前空間よりも機能は限定的であり、階層構造を持たず、[クラス名の衝突を避けるために存在する](../Page/クラス_\(コンピュータ\).md "wikilink")。またその**パッケージ**内にあるクラスに対しては、**package private**といった設定が可能であり、**package private**な[クラスは](../Page/クラス_\(コンピュータ\).md "wikilink")**パッケージ**外部の[クラスからのアクセスが禁止され](../Page/クラス_\(コンピュータ\).md "wikilink")、[カプセル化](../Page/カプセル化.md "wikilink")による情報隠蔽を実現できる。これにより[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink")[デザインパターンの一つ](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")、[Facade パターンをより忠実に実現することができる](../Page/Facade_パターン.md "wikilink")。

## パッケージ使用

Javaソースファイルでは、ファイルが属しているパッケージには`package` [キーワードが明示されている](https://ja.wikipedia.org/wiki/予約語_\(Java\) "wikilink")。

``` java
package java.awt.event;
```

Javaソースファイル内でパッケージを使うことで、`import`文でパッケージからクラスをインポートすることは便利なものとなる。この構文

``` java
 import java.awt.event.*;
```

は `java.awt.event` からすべてのクラスをインポートする。一方、

``` java
 import java.awt.event.ActionEvent;
```

はパッケージから`ActionEvent`クラスだけをインポートする。これらの`import`文どちらも、以下のように単純クラス名で`ActionEvent` クラスを参照利用することができる:

``` java
 ActionEvent myEvent = new ActionEvent();
```

クラスはクラス完全修飾名を使うことで`import`文無しで直接使うことができる。例えば、

``` java
 java.awt.event.ActionEvent myEvent = new java.awt.event.ActionEvent();
```

は前述の`import`文を要求しない。

## パッケージアクセス保護

パッケージ宣言付きクラスは*デフォルトアクセス(<em lang="en">default access</em>)*宣言(修飾子無指定)したクラスや[メンバ](https://ja.wikipedia.org/wiki/メンバー "wikilink")、*`protected`*アクセス[修飾子](https://ja.wikipedia.org/wiki/修飾子 "wikilink")宣言されたクラスメンバにアクセスできる。デフォルトアクセスは`public`、`protected`、`private`アクセス修飾子が宣言に指定されていないときに強要される。それとは対照的に、他のパッケージ内にあるクラスはデフォルトアクセス宣言されたクラスやメンバにアクセスできない。`protected`宣言されたクラスメンバはそのクラスのサブクラスである他のパッケージ内クラスからのみアクセスすることができる。

## JARファイル生成

[JARファイルはjar](https://ja.wikipedia.org/wiki/Jar "wikilink")[コマンドラインユーティリティによって生成される](../Page/コマンドラインインタプリタ.md "wikilink")。そのコマンド

``` java
 jar cf myPackage.jar *.class
```

はすべての拡張子.classファイルをJARファイル*myPackage.jar*に圧縮する。コマンドラインオプション'c'はjarコマンドに「新しいアーカイブを作れ」と指示する。'f'オプションはJARファイルが生成されるファイル名の直前に置く必要がある。

## パッケージ命名規約

パッケージは通常、ピリオド(`.`) （「ドット」と発音）によって分割された階層レベルで[階層](https://ja.wikipedia.org/wiki/階層 "wikilink")命名[パターン](https://ja.wikipedia.org/wiki/パターン "wikilink")を使用する。名前階層が下位であるパッケージはしばしば上位層に相当するパッケージの「サブパッケージ」と呼ばれるが、パッケージ間には意味的な関係は無い。[Java Language Specification](https://web.archive.org/web/20141031140825/http://docs.oracle.com/javase/specs/jls/se5.0/html/j3TOC.html) は二つの公開されたパッケージが同じ名前を持つことを避けるためにパッケージ命名規約を設けている。命名規約がユニークなパッケージ名を作成する方法を説明するように、広く配布されたパッケージはユニークな名前空間を持つだろう。これはパッケージ群が簡単で無意識的にインストールされカタログ化されるようにしている。

パッケージ名は組織の[トップレベルドメイン](../Page/トップレベルドメイン.md "wikilink")名と、そのときの組織のドメインといくつかのサブドメインリストが逆順になったもので始まることが推奨されている。組織はそれらの名前にそのときに特定の名前を選ぶ。パッケージ名は可能ならばすべて小文字にすべきである。

例えば、もしカナダにMySoftと呼ばれる組織がfraction(小数、分数)を扱うパッケージを作るとすると、パッケージを`ca.mysoft.fractions`とネーミングすることは、他社によって開発された類似するもうひとつのパッケージからfractionパッケージを見分ける。もしMySoftと呼ばれるアメリカの企業もまたfractionパッケージを作るとするが、名前は`com.mysoft.fractions`であり、そのとき、それら二つのパッケージにあるクラスはユニークに定義され、名前空間は分割される。

曖昧でないパッケージ名に関して完全な規約と、パッケージ名に直接使うことができないインターネットドメイン名をパッケージに命名するルールは、Java言語仕様の[Chapter 6.1](https://docs.oracle.com/javase/specs/jls/se8/html/jls-6.html#jls-6.1)で説明されている。

[ハイフン](../Page/ハイフン.md "wikilink")(-)が使われている[ドメイン名](../Page/ドメイン名.md "wikilink")をそのまま[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")で使用すると[コンパイルエラーを引き起こす](../Page/コンパイラ.md "wikilink")。そのためハイフンが使われているドメイン名には、ハイフンの代わりに[アンダースコア](../Page/アンダースコア.md "wikilink") (_)を使用する。

## Java SE 5 から追加されたアノテーション

Java SE 5から追加された[アノテーション](../Page/アノテーション.md "wikilink")は、パッケージも対象にすることができる。 パッケージにアノテーションを保存するには、該当するパッケージディレクトリにpackage-info.javaというファイルを作り、以下のように記述する。

``` java
 /**
  * パッケージの説明。
  * パッケージのコメントにはJavadocのタグがそのまま使える。
  */
 @Deprecated package com.example.wikipedia;
```

この例は、パッケージcom.example.wikipediaを非推奨にしていることを意味する。このpackage-info.javaは[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")に警告を表示させる以外に、[Javadoc](../Page/Javadoc.md "wikilink")にパッケージの説明を表示するドキュメントを生成させるためにも利用される。package-info.javaは、パッケージにアノテーションを付加するために作られ、従来のpackage.htmlの代替となるものである。

## Java SE 6のコアパッケージ

<table>
<tbody>
<tr class="odd">
<td></td>
<td><p>— 基本言語機能性と基本型basic language functionality and fundamental types</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>— コレクション<a href="../Page/データ構造.md" title="wikilink">データ構造</a>クラス</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>— 入出力操作</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>— 多倍長演算</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>— Javaによる<a href="https://ja.wikipedia.org/wiki/New_I/O" title="wikilink">New I/Oフレームワーク</a></p></td>
</tr>
<tr class="even">
<td></td>
<td><p>— ネットワーク命令、ソケット、<a href="https://ja.wikipedia.org/wiki/DNSルックアップ" title="wikilink">DNSルックアップ</a>...</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>— 暗号鍵生成、暗号化、復号</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>— データベースにアクセスするための<a href="../Page/JDBC.md" title="wikilink">Java Database Connectivity</a> (<a href="../Page/JDBC.md" title="wikilink">JDBC</a>)</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>— <a href="https://ja.wikipedia.org/wiki/ネイティブ" title="wikilink">ネイティブ</a><a href="https://ja.wikipedia.org/wiki/GUI" title="wikilink">GUI</a><a href="https://ja.wikipedia.org/wiki/コンポーネント" title="wikilink">コンポーネント</a>のパッケージの基本階層</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>— プラットフォーム非依存リッチ<a href="https://ja.wikipedia.org/wiki/GUI" title="wikilink">GUI</a>コンポーネントのパッケージ階層</p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [JAR（ファイルフォーマット）](https://ja.wikipedia.org/wiki/Jar "wikilink")
  - [クラスパス](https://ja.wikipedia.org/wiki/クラスパス "wikilink")
  - [Apache Harmony](../Page/Apache_Harmony.md "wikilink")

## 外部リンク

  -
  - [Java Language Specification, 3rd edition: Unique Package Names](http://docs.oracle.com/javase/specs/jls/se5.0/html/packages.html#7.7)

  - [Java Package Naming Conventions](http://java.sun.com/docs/codeconv/html/CodeConventions.doc8.html)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")