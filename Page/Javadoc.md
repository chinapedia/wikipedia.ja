> この記事は[Javadoc](https://ja.wikipedia.org/wiki/Javadoc)から翻訳されています。


**Javadoc**とは、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が開発したコンピュータソフトで、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のソースコードから[HTML形式の](../Page/HyperText_Markup_Language.md "wikilink")[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[仕様書](https://ja.wikipedia.org/wiki/仕様書 "wikilink")を生成するものである。

JavadocはJavaクラスの仕様書の標準の書式であり、多くの[IDEは自動的にJavadoc](../Page/統合開発環境.md "wikilink") HTMLを生成する機能を備えている。

なお、HTML形式は標準の書式であり、カスタマイズにより変更可能である。

## Javadocのタグ

開発者はソースコードにコメントを記述する時に、ある程度の決まった形式の文章とJavadocタグを使用する。ソースのコメントの内、**/\*\***で始まるものが、生成されたHTMLに含まれることになる。Javadocタグは、頭に"@" 記号が付く。いくつかのタグはテーブル用のものである。

  -
    {| class="wikitable"

\! style="text-align: left;"|タグ \!\!style="text-align: left;"|記述内容 |- |@author || 開発者名を記述する。 |- |@deprecated || 廃止された[クラス](../Page/クラス_\(コンピュータ\).md "wikilink") や[メソッドに付けられる](../Page/メソッド_\(計算機科学\).md "wikilink")。コンパイル時にこれがつけられたメソッドを使用すると警告を発する。[IDEによっては](../Page/統合開発環境.md "wikilink")、このマークがつけられたメソッドを使用したコーディングをした場合、警告を発する。[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5以降からは、[アノテーション](../Page/アノテーション.md "wikilink")を用いて同様のことができるようになっている。 |- |@exception || メソッドが投げる[例外クラスとその説明を記述する](../Page/例外処理.md "wikilink")。— @throwsも参照。 |- |@param || メソッドの引数や[総称型](https://ja.wikipedia.org/wiki/総称型 "wikilink")のパラメータを記述する。引数の数だけ記述する必要がある。引数名と引数の概要を記述する。 |- |@return || メソッドの戻り値を記述する。戻り値がvoidの時は記述しなくて良い。 |- |@returns || @returnと同じ。 |- |@see || 関連する他のメソッドまたはクラスを記述する。このタグの内容は自力で記述するのは大変なので[IDEなどで自動生成すると良い](../Page/統合開発環境.md "wikilink")。 |- |@since || クラスまたはメソッドの導入されたバージョンを記述する。[IDEなどの自動生成ツールでここに日付やバージョン番号などの情報をわりあてることができる](../Page/統合開発環境.md "wikilink")。 |- |@throws || メソッドが投げる例外を記述する。@exceptionと同義。Javadoc 1.2で追加された。 |- |@version || クラスまたはメソッドのバージョンを記述する。[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")を用いてこのバージョン番号割り当てを自動化することができる。 |- |{@link} || 標準テキストのラベルとインラインリンクを挿入する。{パッケージ名.クラス名\#メソッド名 label}という方式で記述。labelの文法は@seeと同じ。 |- |{@docRoot} || 生成されたドキュメントのルートディレクトリを基点とする相対パスを表す。 |- |@serial || デフォルトで[直列化可能](../Page/シリアライズ.md "wikilink")[フィールド](https://ja.wikipedia.org/wiki/フィールド "wikilink")のdocコメントで使用する。このタグの後に説明を入れる。これは直列化形式ページの生成に使われる。 |- |@serialField || クラスのObjectStreamField コンポーネントをドキュメント化する。各 ObjectStreamField コンポーネントに対して @serialField タグを 1 つ使う必要がある。このタグの後に、順番にフィールド名、フィールドの型、フィールドの説明を記述する。 |- |@serialData || データの型と順序を直列化形式でドキュメント化。このデータには、特に writeObject メソッドによって書き込まれる任意指定のデータ、および  メソッドによって書き込まれるすべてのデータが含まれる。@serialData タグは、、、、および の各メソッドの doc コメントで使用できる。 このタグの後に説明を記述する。 |}

## 例

Javadocの使用例。（サンプルには英語が含まれているが、日本語の使用も可能）。

``` java5
 /**
  * クラスの説明.
  * <pre>
  * ピリオド(.)または句点(。)で終わるところまでが、
  * クラス一覧の概要に説明されるところであり、
  * ピリオド以降は説明の概要には含まれず、クラスの説明に含まれる。
  * このように、JavadocにはHTMLタグを使用することができる。
  * </pre>
  * @param <T1> 総称型パラメータの説明
  * @param <T2> 総称型パラメータの説明
  * @author Wikipedian
  * @author Second author
  * @version 1.6
  * @since 1.0
  */
 public class JavadocSample<T1, T2 extends List> {

   /**
    * @serial 直列化可能データの説明
    */
   private int x;

   /**
    * Validates a chess move.
    * @author John Doe
    * @param theFromFile File of piece being moved
    * @param theFromRank Rank of piece being moved
    * @param theToFile   File of destination square
    * @param theToRank   Rank of destination square
    * @return true if a valid chess move or false if invalid
    */
   boolean isValidMove(int theFromFile, int theFromRank, int theToFile, int theToRank)
   {
      //...
   }

   /**
    * 非推奨メソッド。
    * @deprecated このメソッドは非推奨です。
    * @param t 説明
    * @throws SomeException 例外の説明
    */
   String deprecatedMethod() {
     //...
   }

   /**
    * メソッドの説明。
    * @param t 説明
    * @throws SomeException 例外の説明
    * @throws Exception 例外の説明
    * @return String型の値
    * @since 1.5
    * @see "関連"
    * @see <a href="http://www.example.com/">Example</a>
    * @see String#equals(Object) equals
    */
   String add(T1 t) throws SomeException, Exception {

   }
 }
```

## ドキュメント生成

ドキュメント生成には、これらのJavadocコメントのほかに、パッケージやAPI全体の概要を説明するコメントファイルや画像ファイルを参照することができる。

### 概要コメントファイル

ドキュメント全体の概要を示す概要コメントファイル (overview.html) を記述する。これらの文法は以下のような簡単な[HTMLとなる](../Page/HyperText_Markup_Language.md "wikilink")。

``` html4strict
<html>
  <body>
    ここに概要コメントを記述する。
  </body>
</html>
```

概要コメントファイル (overview.html) はJavadocコマンド実行時に-overviewオプションでディレクトリパスを指定するか、または、パッケージを置いているソースツリーのルートにoverview.htmlファイルを置くことでドキュメントに含められる。

### パッケージコメントファイル

package-info.javaというファイルにコメントを記述する。JDK 1.4 までは package.html に記載した。これは以下のように、クラスやメソッドなどに記述するJavadocコメントと同じ要領で済む。ただし、package[キーワードを用いてパッケージ宣言しなければならない](https://ja.wikipedia.org/wiki/予約語_\(Java\) "wikilink")。

``` java5
/**
 * ここにパッケージの概要を記述する。
 * @since 1.5
 */
package com.example.wikipedia;
```

この記法は、Java SE 5から登場した[アノテーション](../Page/アノテーション.md "wikilink")には、パッケージにも指定できるものがあるために用意された。これにより、package-info.javaにはアノテーションも保存でき、たとえばパッケージに対してアノテーションを指定できるようになった。package.htmlではアノテーションが使用できないため、package-info.javaの使用はpackage.htmlよりも推奨されている。

### 未処理ファイル

Javadocで生成するドキュメンテーションには画像やJavaソースコードなどを含めることもできる。画像を置くには 画像を表示したいクラスがあるディレクトリに *doc-files*という名前のディレクトリを作成し、そこに画像をコピーする。そしてこの画像のリンクを実際に張るには以下のようにJavadocコメントに明示的に記述する必要がある。

``` java5
 /**
  * 画像ファイル
  * <img src="doc-files/image.gif" />
  */
```

## Javadoc生成を容易にするツール

Javadocの生成は、そのままでは複雑なコマンドラインを必要とする。とくに設定を細かくすると、[バッチファイル](https://ja.wikipedia.org/wiki/バッチファイル "wikilink")や[シェルスクリプトとして記述するだけでも膨大なものになる](https://ja.wikipedia.org/wiki/シェル#シェルスクリプト "wikilink")。そこで[NetBeans](https://ja.wikipedia.org/wiki/NetBeans "wikilink")や[Eclipseなどの](../Page/Eclipse_\(統合開発環境\).md "wikilink")[IDEや](../Page/統合開発環境.md "wikilink")[Apache Antのようなビルドツールや](https://ja.wikipedia.org/wiki/Apache_Ant "wikilink")[Apache Mavenのようなプロジェクト管理ツールを使うことが薦められている](../Page/Apache_Maven.md "wikilink")。

## Doclet

JavadocにはJavadocのタグを自作できる機能Docletがある。これを用いて、[Apache Tomcatの設定ファイルweb](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink").xmlの内容を[Java ServletソースコードのJavadocコメント上に記述して](../Page/Java_Servlet.md "wikilink")[XDoclet](https://ja.wikipedia.org/wiki/XDoclet "wikilink")を用いてweb.xmlを自動生成するといったことが可能になる。このほかにも、Javadocコメントから他のJavaソースコードやデータベーススキーマや[UMLのクラス図を自動生成するといったことが可能になり](../Page/統一モデリング言語.md "wikilink")、開発効率が飛躍的に向上する。

これは[Enterprise JavaBeansや](../Page/Enterprise_JavaBeans.md "wikilink")[Apache Struts](https://ja.wikipedia.org/wiki/Apache_Struts "wikilink")、[UML](../Page/統一モデリング言語.md "wikilink")、[Hibernate](../Page/Hibernate.md "wikilink")、[JBoss](https://ja.wikipedia.org/wiki/JBoss "wikilink")などにも使われている。ただし現在では、これらの多くがJavadocによる自動生成の代わりに、[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5から登場した[アノテーション](../Page/アノテーション.md "wikilink")で代替することが可能になった。

## 関連項目

  - [文芸的プログラミング](https://ja.wikipedia.org/wiki/文芸的プログラミング "wikilink")
  - [アノテーション](../Page/アノテーション.md "wikilink")
  - [Javaの文法](https://ja.wikipedia.org/wiki/Javaの文法 "wikilink")
  - [ソフトウェアドキュメンテーション](../Page/ソフトウェアドキュメンテーション.md "wikilink")
  - [doxygen](https://ja.wikipedia.org/wiki/doxygen "wikilink")

## 外部リンク

  - [Javadocテクノロジ](http://docs.oracle.com/javase/jp/7/technotes/guides/javadoc/)
  - [ドックレット API](http://docs.oracle.com/javase/jp/7/jdk/api/javadoc/doclet/)
  - [JSR 260: Javadoc<sup>TM</sup> Tag Technology Update](https://www.jcp.org/en/jsr/detail?id=260)

[Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink")