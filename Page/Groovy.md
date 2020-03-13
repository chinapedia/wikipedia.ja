> この記事は[Groovy](https://ja.wikipedia.org/wiki/Groovy)から翻訳されています。


（グルービー）は、[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")上で動作する[動的プログラミング言語](../Page/動的プログラミング言語.md "wikilink")である。

の処理系は[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアであり、 と  らを中心に、オープンソース開発サイトであるコードハウス上で、2003年8月27日に開発が開始された（[CVSへの最初のコミットがなされた](../Page/Concurrent_Versions_System.md "wikilink")）。その後、開発の主体は  と  らに移り開発が続けられている。[2015年](../Page/2015年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink")までは Pivotal がスポンサー企業となり、開発者をフルタイム雇用していたが、3月末を持って終了し、[Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")の管理に移行した\[1\]。

## 概要

GroovyはJVM上で動作する言語処理系および言語の名称であり、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")との直接的な連携を特徴とする。例えばGroovyからすべての[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") [APIや](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、Javaで書かれた任意のサードパーティ製のコンパイル済みのライブラリなどを呼び出すことができる。言語の記述能力としては、Javaで記述できることは、無名内部クラスの定義など一部の例外を除き基本的にGroovyでも記述することができる。逆に言うとJavaで記述できない機能は記述できないが、Javaと同様に[C言語](../Page/C言語.md "wikilink")などで書かれたネイティブメソッドなどは呼び出すことができる。

Groovyは動的な言語であり、直接スクリプトを実行することができる。Groovyコード断片をコマンドラインに与え[ワンライナー](https://ja.wikipedia.org/wiki/ワンライナー "wikilink")として実行することも可能である。なおこの時、中間的にJavaソースコードが生成されることはなく、[バイトコード](../Page/バイトコード.md "wikilink")がメモリ上に生成されて直接実行される。また、groovycコマンド（groovyコンパイラ）を使ってクラスファイルをあらかじめ生成しておくこともできる。いずれにせよGroovyコードは内部的には[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")に変換されてJVM上で実行される。

このとき、GroovyコードもJavaコードも、JVMからみると両方ともJavaバイトコードとして解釈実行されるという意味で区別がない。Groovyのこのような仕組みから、GroovyはJavaと極めて親和性が高く、Java技術で培われてきた開発インフラやライブラリ、ノウハウ、ツール、JVM最適化技術などの多くをそのまま流用することができる。Groovyから生成したクラスファイルは通常のクラスファイルであるので、[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")を要求するプラグインなどをGroovyで記述することも容易である。

Groovyは、同じ実行時システムを共有する、Javaコードの別の表記法だと考えることもできる。

## 言語仕様

Groovyの言語仕様はJavaのそれをベースとしており、基本的にJavaプログラマにとって慣れ親しみやすいものである。Groovyはスクリプト言語として大幅に簡易化された記述を許している。以下に簡略な記述を可能とするGroovy言語の特徴を示す。

  - 変数の型宣言は不要である。

      - 通常の場合 - 宣言をしなかった場合型として扱われ、メソッド呼び出しは[動的ディスパッチ](https://ja.wikipedia.org/wiki/動的ディスパッチ "wikilink")によって解決される（変数の型の宣言をすることも可能であり、静的なスタイルと動的なスタイルの場合に応じた使い分けることができる）。メソッドの引数や返り値の型宣言も同様である。
      - `@TypeChecked` を使用した場合 - 変数の型を指定しなかった場合は[型推論](../Page/型推論.md "wikilink")され、型が正しいかどうかチェックされる。メソッド呼び出しは動的ディスパッチのまま。
      - `@CompileStatic` を使用した場合 - 上記に加えて、メソッド呼び出しは静的に解決される。`@ToString` のようなコンパイル時のメソッド生成は通常通り使える。この3種の中では最速。

  - メソッド呼び出しの括弧は省略できる。

  - 行末のセミコロンは省略できる。

  - [リストや](../Page/リスト_\(抽象データ型\).md "wikilink")[マップの初期化を記述する組み込み構文を持つ](../Page/連想配列.md "wikilink")。

  - 演算子のオーバーロード定義（ユーザ定義演算子）が可能である。

      - 組み込み型としてリストやマップを扱うことができ、それらのリテラル表記や、それらを処理する演算子が定義されている。

      - 、型などについては四則演算がオーバーロード定義されている。

  - 検査例外をthrowsするメソッドを呼び出す際にもtry/catchで囲んだり呼び出し側メソッドをthrows宣言する必要はない。

  - プリミティブ型はリファレンス型と同様に扱うことができる（明示的な変換を行う必要はない）。

  - if文やwhile文、3項演算子('?～:～')の条件節では0やnullの値は偽として扱われる(boolean型の値である必要がない)。

  - J2SEの正規表現クラスを扱うための組み込みの演算子（=\~や==\~など）が用意されている。また構文上も特別扱いされておりPerlやRubyと似た使用ができる。

  - 文字列定数中に任意のGroovyの式を埋め込むことができる（${}の記法を用いる。GStringと呼ぶ。なお変数名の場合は中括弧も不要であり、"$変数名"の形式で変数の値を文字列に埋め込むことができる。）。

  - 名前つき引数でのメソッド呼び出し。

  - アクセス修飾子のデフォルトはpublicである。

  - 、、、、、groovy.lang、groovy.utilは明示的に指定しなくても、暗黙的にインポートされている。

  - groovyファイルで定義したクラスはGroovyObjectインターフェースを暗黙で実装し、クラスの外で定義したフィールドやメソッドはScript[抽象クラス](https://ja.wikipedia.org/wiki/抽象クラス "wikilink")の実装クラスのフィールドやメソッドとして定義されたと見なされる。

### クラス定義

Groovyコードはクラス定義中にある必要はなく、クラス定義の外側でのメソッドの定義や実行文の記述が可能である。

以下、ファイル名が HelloTest.groovy とする

``` groovy
println "Hello, World!"
```

すると、

``` groovy
class HelloTest {
    public HelloTest() {
        println "Hello, World!"
    }
    public static void main(String[] args) {
        new HelloTest()
    }
}
```

と同じ意味を持つ。

### switch, case

switch/case文は任意の型に対して分岐することができるように拡張されている。

``` groovy
switch (value) {
case "Hello":
   println "value == 'Hello'"
   break
case String:
   println "valueはString型"
   break
case 1..12:
   println "valueは1～12の間"
   break
default:
   println "それ以外"
}
```

### for

通常の for と [for in](https://ja.wikipedia.org/wiki/foreach文 "wikilink") がある。for を使うと、break や continue が使える。@CompileStatic を付けた状態では、C言語スタイルの for ループかつループ変数に型を付けた状態が最速であり、Java言語と同等の速度で動く。each や times はクロージャ呼び出し分の時間がかかる。

``` groovy
for (int i = 0; i < 3; i++) { println "$i: Hello" }
for (i in 1..3) { println "$i: Hello" }
(1..3).each { println "$it: Hello" }
3.times { println "$it: Hello" }
```

### Getter, Setter

Getter、Setterメソッドは自動生成される。フィールドアクセスの記法でGetter、Setterメソッドを呼び出すことができる。

``` groovy
class Pojo {
    def name
}
def pojo = new Pojo(name:"名前")
println pojo.getName() // getName()が生成されている
println pojo.name // getName()が呼ばれる
```

### デフォルト引数

デフォルト引数（メソッド・コンストラクタ呼び出しチェインの自動生成）。

``` groovy
def greet(mess = "Hello World") {
    println mess
}
greet()
greet("foo")
```

は

`Hello World`
`foo`

と出力される。

### ExpandoMetaClass

``` groovy
def obj = "foo"
obj.metaClass.greet = { println "Hello World" }
obj.greet()
```

### Expando

Groovyは未実装のフィールドの参照と代入、未実装のメソッドの起動をキャッチしGroovyObjectのメソッドを起動する。

``` groovy
GroovyObject#getProperty(String name)
GroovyObject#setProperty(String name, Object value)
GroovyObject#invokeMethod(String name, Object arguments)
```

以下、Expando を使用した例である。

``` groovy
def obj = new Expando()
obj.greetingMessage = "Hello World"
obj.greet = { println greetingMessage }
obj.greet()
obj.message = "foo"
println obj.message
```

また、連想配列を使用しても、似た構文が可能である。`this`の意味が変わる。

``` groovy
def obj = [:]
obj.greetingMessage = "Hello World"
obj.greet = { println obj.greetingMessage }
obj.greet()
obj.message = "foo"
println obj.message
```

### MOP(Meta Object Protocol)

``` groovy
GroovyObject#setMetaClass(MetaClass)
```

``` groovy
class Main {
  static void main(String[] array) {
    GroovyObject groovyObject = new Main()
    Interceptor interceptor = new GreetingInterceptor()
    InterceptorUtils.setInterceptor(groovyObject, interceptor)
    groovyObject.greet()
  }
}

class InterceptorUtils {
  static void setInterceptor(GroovyObject groovyObject, Interceptor interceptor) {
    ProxyMetaClass proxyMetaClass = ProxyMetaClass.getInstance(groovyObject.getClass())
    proxyMetaClass.setInterceptor(interceptor)
    groovyObject.setMetaClass(proxyMetaClass)
  }
}

class InterceptorImpl implements Interceptor {
  Object beforeInvoke(Object groovyExtensionObject, String name, Object[] arguments) {
    return null
  }
  Object afterInvoke(Object groovyExtensionObject, String name, Object[] arguments, Object beforeInvokeReturnObject) {
    Object object = invokeMethod(name, arguments)
    return object
  }
  boolean doInvoke() {
    return false
  }
}

class GreetingInterceptor extends InterceptorImpl {
  void greet() {
    println "Hello World"
  }
}
```

### use

未実装のメソッドをuseブロック内で起動すると、ブロックで指定したクラスのクラスメソッドに処理をディスパッチする。

``` groovy
import groovy.inspect.Inspector

use (Category.class) {
    def obj = "Hoge"
    println obj.getShortClassName()
    println obj.toString()
}

//名前は自由
class Category {
    //最初の引数は、メソッドが起動されたインスタンスの参照コピー
    static getShortClassName(obj) {
        Inspector.shortName(obj.getClass())
    }
    //実装メソッドと重複する場合、Groovyはカテゴリーより実装メソッドを優先
    static String toString(Object obj) {
        "Hello World"
    }
}
```

は

`String`
`Hoge`

と出力される。

### GroovyMarkup

Groovyコードの表記を使い、Groovyの機能（クロージャやダイナミックなメソッド追加）を駆使してツリーデータ構造の組み上げを行う。具体的には、新規ノードの追加をメソッド呼び出しとして、その新規ノードの子ノード群の記述をメソッドに渡すクロージャとして定義する。そのクロージャにはさらにその子ノードのための一連のノード追加メソッド呼び出しを含めることができ…… というように再帰的に記述していく。このときGroovyのループ文やif文などの制御構造を含むすべてのGroovyの言語機能を使うことができる。

GroovyMarkupは直感的には、[XMLほど静的ではないが](../Page/Extensible_Markup_Language.md "wikilink")、純粋なプログラムコード列よりは宣言的な、「やや宣言的なデータ記述」であるといえるかもしれない。

GroovyMarkupは基本的な機能であり、GroovyMarkupを使った具体的なライブラリとしては、[Swing](../Page/Swing.md "wikilink")の[GUIコンポーネントの組み立てを行うSwingBuilder](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、DOMのようなXMLデータ構造を組み立てるMarkupBuilderなどがある。

``` groovy
import groovy.xml.MarkupBuilder

class Main {

  static void main(array) {

    Writer writer = new StringWriter()

    writer.println("<?xml version='1.0' ?>")
    writer.println()

    def builder = new MarkupBuilder(writer)

    /*
     名前がルートのタグ名であるメソッド

      引数がマップである場合はタグの属性
      引数が文字列である場合はテキストノードの内容でHTMLエスケープされます。

      未実装メソッドをハンドルするGroovyObject#invokeMethod(String methodName, Object methodParameter)を利用

      メソッドの括弧が省略されています。
    */
    builder.html(xmlns:"http://www.w3.org/1999/xhtml", "xml:lang":"ja") { //以降は名前がタグ名であるクロージャ

      /*
       引数がクロージャである場合は名前がタグ名
        引数がマップである場合はタグの属性
        引数が文字列である場合はテキストノードの内容でHTMLエスケープされます。
      */

      head() {
      }

      body() {

        div("1行目");
        div("2行目");

        //ヒア・ドキュメント構文

        String string = """
      <div id='3'>3行目</div>
      <div id='4'>4行目</div>
    """

        pre(string) {
        }
      }
    }

    println writer.toString()

    /*
      標準出力結果
<?xml version='1.0' ?>

<html ns='http://www.w3.org/1999/xhtml' xml:lang='ja'>
  <head />
  <body>
    <div>1行目</div>
    <div>2行目</div>
    <pre>
      <div id='3'>3行目</div>
      <div id='4'>4行目</div>
    </pre>
  </body>
</html>
    */
  }
}
```

### クロージャ

Groovyでは[コードブロック](https://ja.wikipedia.org/wiki/コードブロック "wikilink")をファーストクラス（第一級）オブジェクトとして生成し、変数に格納したりメソッド引数や戻り値として受け渡したりすることができる。Groovyのライブラリは繰り返し処理や入出力処理などを中心に[クロージャ](../Page/クロージャ.md "wikilink")が駆使されており、簡潔な表記を行うことができる。

クロージャは構築されたスコープ内の変数を読み書きできる。

``` groovy
def str = "Hello World"
def readerClosure = { println str }
readerClosure()
def writerClosure = { str = "foo" }
writerClosure()
println str
```

このコードを実行すると

`Hello World`
`foo`

と出力される。

### Groovy JDK

GroovyからJava SEの標準APIをすべて呼び出すことができるが、この際にGroovyから使うと便利なメソッドが[リフレクションを用いてJava](../Page/リフレクション_\(情報工学\).md "wikilink") SEクラスに擬似的に多数追加されている。例えば、クロージャをとるFile\#eachLine()といったメソッドを使用することができ、以下の様な記述が可能となっている。

``` groovy
new File("test.txt").eachLine { println it }
```

File\#eachLine(Closure)はそれぞれの行の値を変数itに代入してクロージャを呼び出す、という繰り返し処理を行うだけでなく、処理の終了時もしくは例外の発生時に、ファイルのクローズ処理を行う。つまりJavaの場合必要なfinally節におけるclose処理を必要とせず簡潔に記述できる。他に同様に、Reader\#eachLine(Closure)メソッドなども追加されている。また、File\#getText(String characterCodeSetName)、Reader\#getText()、Reader\#readLines()というファイルの全ての内容を一括で読み込むメソッドが追加されており、入出力処理を簡潔に記述することができる。

## 他の言語からの影響

James StrachanはGroovyはオブジェクト指向スクリプト言語[Ruby](../Page/Ruby.md "wikilink")から大きな影響を受けていることを何度か公言している。実際、クロージャの仕様や表記、その他予約語の選択などにおいてRubyからの影響を色濃く見ることができる。その他、[Python](../Page/Python.md "wikilink")、[Dylan](../Page/Dylan.md "wikilink")、[Smalltalk](../Page/Smalltalk.md "wikilink")などからも言語機能が取り込まれている。

## 適用分野

Groovyは本格的なアプリケーション構築にも使えるし、 また、Javaシステム開発におけるテストコードの記述を上げることにも使える。（Groovyには標準でJUnit機能が組み込まれている）。さらに、スクリプト言語として、フィルタ的なツールやプロトタイプを書き下すことも容易である。

アプリケーションの複雑なコンフィグレーションやカスタマイズ用の言語として用いるということも注目されている。[Antの設定ファイル](../Page/Apache_Ant.md "wikilink") (build.xml) をGroovyで記述する機能は標準で組み込まれているし、いくつかの[DIコンテナ](https://ja.wikipedia.org/wiki/DIコンテナ "wikilink")（依存性注入コンテナ、[IoCコンテナ](https://ja.wikipedia.org/wiki/IoCコンテナ "wikilink")）と呼ばれる[アプリケーションフレームワーク](../Page/アプリケーションフレームワーク.md "wikilink")における起動時設定ファイルの記述言語として採用されるなど、XMLの代用として採用されはじめている。

将来的には、既存Javaシステムを連携させるグルー言語として、[Microsoft Windowsの世界における](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Visual Basicや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[VBAの役割をJavaシステム全般において果たせる可能性がある](../Page/Visual_Basic_for_Applications.md "wikilink")。

Groovyの応用として注目すべき事例として、[Grails](https://ja.wikipedia.org/wiki/Grails "wikilink")をあげることができる。[Grails](https://ja.wikipedia.org/wiki/Grails "wikilink")はGroovyを使用したWebアプリケーションフレームワークであり、Webアプリ開発において[Ruby on Railsが実現しているような高い生産性をもたらす](../Page/Ruby_on_Rails.md "wikilink")。

## 標準化

Groovyは[2004年](../Page/2004年.md "wikilink")[3月29日](../Page/3月29日.md "wikilink")にJava技術の標準化プロセスJCPにおいてJSR 241として受理され仕様の標準化がすすめられたが、その後 dormant (休止)扱いとなった\[2\]。

## サンプルコード

### クロージャとループ

``` groovy
def forLoop() {
    def map = [name: "James", location: "London"]
    for(e in map) { println "entry $e.key is $e.value" }
}
def closureExample(list) {
    list.each { println "value $it" }
}
def values = [1, 2, 3, "abc"]
closureExample(values)
forLoop()
```

### メモ帳

``` groovy
import groovy.swing.SwingBuilder
import javax.swing.*

def notepad
new SwingBuilder().frame(title: "メモ帳", defaultCloseOperation: JFrame.EXIT_ON_CLOSE,
    size: [800, 600], show: true, locationRelativeTo: null) {
  menuBar() {
    menu(text: "ファイル(F)", mnemonic: 'F') {
      menuItem(text: "名前をつけて保存(A)...", mnemonic: 'A', actionPerformed: {
        fc = new JFileChooser()
        if (fc.showSaveDialog(null) == JFileChooser.APPROVE_OPTION) {
          fc.selectedFile.text = notepad.text
        }
      })
      menuItem(text: "終了(X)", mnemonic: 'X', actionPerformed: { System.exit(0) })
    }
  }
  scrollPane() { notepad = textArea() }
}
```

## 統合開発環境

多くの[統合開発環境](../Page/統合開発環境.md "wikilink")（IDE）がGroovyに対応している。

### [NetBeans](../Page/NetBeans.md "wikilink")

  - 標準でサポートされている。
  - 構文の強調表示、コード折り畳み、およびコード補完をサポート。

### [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink")

  - 変数の型を指定した物は、メソッドの補完が可能。
  - リファクタリング。メソッドの抽出、名前の変更など。
  - デバッガ
  - ソースコードの整形。
  - <http://groovy.codehaus.org/Eclipse+Plugin> にて配布している。

### [IntelliJ IDEA](https://ja.wikipedia.org/wiki/IntelliJ_IDEA "wikilink")

IntelliJ IDEA では Groovy や Grails や Gant などが標準でサポートされている\[3\]。

  - 補完ができる。
      - JavaとGroovyが相互に補完ができ、JavaのクラスをGroovyで補完できるだけでなく、リアルタイムでGroovyのクラスをJavaで補完が可能。JavaとGroovyをプロジェクト内に混在させることができる。
  - Ctrl + クリックによる、定義した場所への移動。
      - 補完同様、JavaとGroovy相互の移動が可能。
  - Dynamic properties により、動的に追加されるメンバ変数を管理することができる。これにより、動的に追加されるメンバ変数に対しても補完やスペルミスのチェックが可能になる。
  - デバッガ
  - コーディング上のエラーに対して、リアルタイムで表示し、Quick-fix ができる。
  - GroovyDoc に対しても補完が使える。
  - 名前の変更やメソッドの抽出や変数の導入などのリファクタリング機能がある。
      - Groovyでの名前の変更は、同時にJavaのソースコードに対しても修正（リファクタリング）がかかる。
  - Grails や Groovy Server Pages (GSP) をサポートしている。
  - Gant や Apache Ivy をサポートしていて、Gant に対して補完やデバッガによるデバッグができる。
  - [Gradle](https://ja.wikipedia.org/wiki/Gradle "wikilink") を Gradle GUI Plugin でサポート。

## 参照

<references />

## 関連項目

  - [Grails](https://ja.wikipedia.org/wiki/Grails "wikilink")
  - [Gradle](https://ja.wikipedia.org/wiki/Gradle "wikilink")
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")
  - [Scala](../Page/Scala.md "wikilink")

## 外部リンク

  - [Groovyホームページ](http://groovy-lang.org/)
  - [Groovy - Documentation](http://groovy-lang.org/documentation.html)
      - [Groovy JDK](http://groovy-lang.org/gdk.html)
      - [Groovy API](http://groovy-lang.org/api.html)
  - [JSR 241](http://jcp.org/en/jsr/detail?id=241)
  - [PLEAC-Groovy](http://pleac.sourceforge.net/pleac_groovy/index.html)
  - [Apache Groovy日本語チュートリアル](https://koji-k.github.io/groovy-tutorial/)

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink")

1.  [Groovy Projects intends to join the Apache Software Foundation -- Guillaume Laforge's Blog](http://glaforge.appspot.com/article/groovy-projects-intends-to-join-the-apache-software-foundation)
2.  [JSR 241: The Groovy Programming Language](http://jcp.org/en/jsr/detail?id=241)
3.  [IntelliJ IDEA :: Smart Groovy IDE with Groovy-Java compiler for Groovy scripts, Groovy Swingbuilder, Groovy server pages with ER diagram for productive Groovy programming, plus Groovy on Grails, available via Groovy plugin](http://www.jetbrains.com/idea/features/groovy_grails.html)