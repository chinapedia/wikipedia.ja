> この記事は[キーワード \(Java\)](https://ja.wikipedia.org/wiki/キーワード_\(Java\))から翻訳されています。


この項目では[Java](https://ja.wikipedia.org/wiki/Java "wikilink")におけるキーワード（[予約語](../Page/予約語.md "wikilink")の記事を参照）\[1\]に関して説明する。全部で50個ある。

この項目は、プログラムの細かい説明には立ち入らず、他の言語と比較できるような説明を目的としている。

## 特徴

  - [プリミティブ型](../Page/プリミティブ型.md "wikilink")名や分岐処理 ([if](../Page/If文.md "wikilink"), [switch](../Page/Switch文.md "wikilink"))、反復処理 ([for](../Page/For文.md "wikilink"), [while](../Page/While文.md "wikilink")) などの基本的な構文とキーワードは[C言語](../Page/C言語.md "wikilink")および[C++](../Page/C++.md "wikilink")と共通するものが多い。[クラスや](../Page/クラス_\(コンピュータ\).md "wikilink")[例外処理](../Page/例外処理.md "wikilink")に関しては[C++](../Page/C++.md "wikilink")類似の構文とキーワードが多い。

## プリミティブ型

### 型名

[プリミティブ型](../Page/プリミティブ型.md "wikilink")の名前である。C言語およびC++と共通するものが多い。

  - **byte**, **char**, **short**, **int**, **long**, **float**, **double**
      -
        [整数型](../Page/整数型.md "wikilink")・[浮動小数点型](https://ja.wikipedia.org/wiki/浮動小数点型 "wikilink")。Javaには符号なしの整数型がなく、C/C++で使われる `unsigned` はない。
  - **boolean**
      -
        [論理型](../Page/ブーリアン型.md "wikilink")。`boolean`はC言語（[C99](../Page/C99.md "wikilink")）における`_Bool`、C++における`bool`に相当する。
  - **void**
      -
        これはプリミティブ型ではないが、型と同じ文脈で使うキーワードなのでここに分類する。[メソッドに戻り値がないことを宣言する](../Page/メソッド_\(計算機科学\).md "wikilink")。[void (コンピュータ)も参照のこと](https://ja.wikipedia.org/wiki/void_\(コンピュータ\) "wikilink")。

### 値

以下はキーワードと同様に扱われるが、定義では論理値リテラル、またはnullリテラルという[リテラル](../Page/リテラル.md "wikilink")である。

  - **true**, **false**
      -
        [論理値を表すリテラル](https://ja.wikipedia.org/wiki/真理値 "wikilink")。
  - **null**
      -
        null型という特殊な型のリテラル。[Null](https://ja.wikipedia.org/wiki/Null "wikilink")も参照。

## 制御構造

C言語およびC++と共通のキーワードを使用している。

  - 分岐
      - **if**, **else**
      - **switch**, **case**, **default**
  - 繰り返し
      - **for**, **while**, **do**
  - ジャンプ
      - **continue** - ループの先頭に戻る
      - **break** - ループのブロックから抜け出す
      - **return** - [メソッドから抜け出す](../Page/メソッド_\(計算機科学\).md "wikilink")。戻り値のあるものは値やオブジェクトの参照を返す。

## クラス、パッケージ

  - **package**
      -
        自[クラスのパッケージを宣言する](../Page/クラス_\(コンピュータ\).md "wikilink")。Javaではパッケージと呼ばれるツリー構造でクラス群を分類している。クラスやメンバに (後述する **public**, **protected**, **private**) を付けることにより、パッケージ内外でクラスやクラスのメンバにアクセス可能な範囲が変わってくる。
  - **import**
      -
        自クラスの所属するパッケージとは異なるパッケージにあるクラスを使用するときにこの宣言でインポートする。
  - **class**
      -
        クラスの定義。例えば、以下のように宣言する。それぞれについてはこの後、説明する。

`例1 public class クラス名 { ... }`
`例2 public class クラス名 extends 親クラス名 { ... }`
`例3 public class クラス名 implements インタフェース名1, インタフェース名2, ... { ... }`
`例4 public class クラス名 extends 親クラス名 implements インタフェース名1, ... { ... }`

  - **interface**
      -
        [インタフェースの定義](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。Javaのインタフェースとは、定義のみで実装をもたない[抽象型](https://ja.wikipedia.org/wiki/抽象型 "wikilink")であり、型の[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")に使用される。インタフェースの[インスタンス](../Page/インスタンス.md "wikilink")を直接生成することはできない。サブクラスでインタフェースを実装して使用する。実装するインタフェースはカンマ区切りで複数並べることができる。

`例1 public interface インタフェース名 { ... }`
`例2 public interface インタフェース名 extends 上位インタフェース名1, 上位インタフェース名2, ... { ... }`

  - **extends**
      -
        **class** の宣言で他のクラスを継承するときに使用する。Javaのクラスは1つのスーパークラスのみ継承可能で、[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")（実装の多重継承）はできない (参考: [菱形継承問題](../Page/菱形継承問題.md "wikilink"))。**interface**の宣言では一つ以上のインタフェースを継承するときに使用する。インタフェースがインタフェースを継承するだけなので、こちらの場合は多重継承が可能。
  - **implements**
      -
        **class** の宣言で、インタフェースを実装するときに使用する。カンマ区切りで並べた複数のインタフェースを実装することができる。
  - **[this](https://ja.wikipedia.org/wiki/this_\(プログラミング\) "wikilink")**
      -
        自クラスを明示するときに使用する。[コンストラクタ](../Page/コンストラクタ.md "wikilink")内から他の引数のコンストラクタを呼ぶときに使用するのが一般的である。また、例えば、コンストラクタの場合は**this(引数)**、メソッドの場合は**this.メソッド名(引数)** などのように使い、親クラスに同一名・同一引数の[メソッドがあるときに明示的に区別できるようにする](../Page/メソッド_\(計算機科学\).md "wikilink")。こちらは、[ローカル変数](../Page/ローカル変数.md "wikilink")や同じクラス内メソッドや[上位クラスに同名のメソッドが存在しない場合は](../Page/スーパークラス_\(計算機科学\).md "wikilink")**this**を省略できる。内部クラスのコード領域で外部クラスのインスタンスへの参照を得るときの構文（*`OuterClass`*`.`**`this`**）でも使用される。
  - **super**
      -
        [上位クラスの](../Page/スーパークラス_\(計算機科学\).md "wikilink")[コンストラクタ](../Page/コンストラクタ.md "wikilink")、[フィールド](../Page/フィールド.md "wikilink")、[メソッドにアクセスするときに使用する](../Page/メソッド_\(計算機科学\).md "wikilink")。上位クラスのコンストラクタを呼び出すときは単に**super(引数)**と書き、メソッドを呼び出すときは**super.メソッド名(引数)** などのように使う。フィールドやメソッドの場合は、自クラスに同一のものがない場合は **super** の記述を省略できる。
  - **new**
      -
        [コンストラクタ](../Page/コンストラクタ.md "wikilink")の呼び出し。インスタンスを生成するときに使用する。

例:

``` java
SampleClass s = new SampleClass();
```

  - **instanceof**
      -
        指定された[クラスのオブジェクトかどうか](../Page/クラス_\(コンピュータ\).md "wikilink")、あるいは指定されたインタフェースを実装しているオブジェクトかどうかを判定する。*`a`*`   `**`instanceof`**`   `*`ClassName`* とした場合、*`a`* が *`ClassName`* のオブジェクトか、その派生クラスのオブジェクトであれば true になる。*`ClassName`* の箇所にオブジェクトの変数名を記述することはできない。

## 修飾子

クラス、メンバの宣言に付けられる修飾子である。

  - **public**, **protected**, **private**
      -
        クラス、メンバのアクセス制御を指示する修飾子（）である。外部からアクセス可能な範囲を決める。Javaでは4つの段階が設けられ、以下の番号が大きくなるほど外部からのアクセスが制約される。
        1.  **public**では、すべてのクラスからアクセスでき。
        2.  **protected**では、同一パッケージにあるクラスかサブクラスからのみアクセスできる。異なるパッケージでサブクラスでないクラスからはアクセスできない。クラスを修飾することはできない ([内部クラスは例外](https://ja.wikipedia.org/wiki/#内部クラス "wikilink"))。
        3.  アクセス修飾子がない場合は、同一のパッケージ内のクラスからのみアクセスできる。サブクラスであってもパッケージが異なる場合はアクセスできない。
        4.  **private**では、他のクラスからはアクセスできず、自クラスからのみアクセスできる。クラスに修飾することはできない (内部クラスは例外)。
        5.  [Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 1.0では**private protected**という組み合わせを使用して、自分自身とサブクラスからのアクセスができるが同じパッケージ内の他のクラスからはアクセスできないというアクセス権を使用することができたが、これはJava SE 1.1以降から廃止され利用することができなくなった。
  - **final**
      -
        フィールドに付けられた場合は再代入を禁止する。メソッド宣言に付けられた場合は、下位クラスで[上書きできないことを表す](../Page/オーバーライド.md "wikilink")。クラス宣言に付けられた場合は、継承できないことを表す。なお、Javaでは、**final**宣言されたフィールドで、宣言部では初期化せずコンストラクタ内で1回だけ代入できる記述も行える。**abstract**との併用はできない。メソッドの引数や[ローカル変数](../Page/ローカル変数.md "wikilink")に使用すればその引数やローカル変数に対して再代入を許さないため、堅牢性の高いメソッドを作ることができる。**final**修飾子は「[イミュータブル](../Page/イミュータブル.md "wikilink") (不変)」なクラスを実装するときに役立つ。

例1:

``` java
public class SampleClass {
    final int constantValue = 5;
}
```

例2:

``` java
public class SampleClass {
    final int constantValue; // 初期化なし

    // コンストラクタ
    public SampleClass() {
        constantValue = 5;  // 1回だけ代入できる。
    }
}
```

  - **static**
      -
        フィールドに付けられた場合は、クラスに属する変数（クラス変数、静的フィールド、クラスフィールド）が確保されることを表す。この修飾子のついたフィールドは、インスタンスがいくつ生成されてもフィールドの実体は1つで、すべてのインスタンスの間で共有される。

記述例:

``` java
class SampleClass {
    static String shared = "shared";
    static final String STR = "constant";
}
```

  -

      -
        [メソッドに付けられた場合は](../Page/メソッド_\(計算機科学\).md "wikilink")、オブジェクトを生成しなくても直接呼び出せるメソッド（静的メソッド、クラスメソッド）であることを表す。[手続き型言語](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")の[関数と同じ扱いになる](../Page/サブルーチン.md "wikilink")。

例:

``` java
class Sample1 {
    // static なメソッド
    public static void method() { ... }
}

class Sample2 {
    void proc() {
        ...
        Sample1.method(); // インスタンスを生成せず直接実行できる。
        ...
    }
}
```

  -

      -
        クラス内に**static {...}**というブロックが現れた場合は、そのクラスが最初に参照されたときにそのブロック内のコードを実行する。これを静的初期化子と呼び、主にstatic finalな[配列](../Page/配列.md "wikilink")やオブジェクトの初期化などに利用される。[データベース](../Page/データベース.md "wikilink")にアクセスするために[JDBC](../Page/JDBC.md "wikilink")ドライバを呼び出すもこの静的初期化子を呼び出している。

例:

``` java
class StaticInitSampleClass {
    private static final List<String> list;

    static {
        final List<String> tempList = new ArrayList<>();
        tempList.add("Hello,");
        tempList.add("World.");
        StaticInitSampleClass.list = Collections.unmodifiableList(tempList);
    }
}
```

  -

      -
        入れ子にされたクラス（ネストされたクラス: nested class）のうち、`static`修飾されていないものは内部クラス (inner class) と呼ばれ、暗黙的に外側のクラスのインスタンスをキャプチャして参照することができるが、このネストクラスを`static`修飾すると静的ネストクラス (static nested class) となり、暗黙的に外側のクラスのインスタンスを参照できなくなる\[2\]。

例:

``` java
class OuterClass {
    static int outerStaticField = 0;
    int outerField = 0;

    class InnerClass {
        void setOuterField(int value) {
            outerField = value; // 暗黙参照可能。
            outerStaticField = value; // OK。
        }
    }

    static class StaticClass {
        void setOuterField(int value) {
            //outerField = value; // コンパイルエラー。
            outerStaticField = value; // OK。
        }
    }

    public OuterClass() {
        new InnerClass().setOuterField(100);
        new StaticClass().setOuterField(-100);
    }

    public static void test() {
        final OuterClass outer = new OuterClass();
        System.out.println("OuterField = " + outer.outerField);
        System.out.println("OuterStaticField = " + outerStaticField);
    }
}
```

  - **abstract**

クラスまたはメソッドに付けられる修飾子である。**final**と併用することはできない。Javaでは、実装されないメソッドがあるクラスを作成することができる。抽象クラス自身のインスタンスを作成することはできない。似たものとしてインタフェースがあるが、**abstract class** は以下の点においてインタフェースと異なる。

  - [コンストラクタ](../Page/コンストラクタ.md "wikilink")を持つことができる
  - メソッドなどの実装を記述できる
  - インスタンス変数を持つことができる

**abstract class** はそのままではインスタンス化できず、不足しているメソッドを実装した派生クラスを用意して使用する。

記述例:

``` java
public abstract class Sample {
    // 実装があるメソッド
    public void method1() {
        ...
    }
    // 実装がないメソッド
    public abstract void method2();
}
```

  - **native**
      -
        メソッドがJava言語以外で実装されていることを宣言する（[Java Native Interfaceを参照](../Page/Java_Native_Interface.md "wikilink")）。
  - **synchronized**
      -
        メソッドの宣言や特定のブロックに付けられ、[排他制御](../Page/排他制御.md "wikilink")を指示する。同一オブジェクトが複数のオブジェクトから参照され、異なる[スレッドで同時に処理を行っている場合でも](../Page/スレッド_\(コンピュータ\).md "wikilink")、この修飾子があるブロックでは処理を行えるスレッドはただ1つしか存在しない。

記述例1:

``` java
public synchronized void method() { ... }
```

記述例2:

``` java
public void method() {
    ...
    synchronized(this) { // 自クラスのインスタンスに対して排他制御
        // 排他制御されるブロック
    }
    ...
}
```

記述例3:

``` java
public void method(Object obj) {
    ...
    synchronized(obj) { // Object obj に対して排他制御
        // 排他制御されるブロック
    }
    ...
}
```

  - **volatile**
      -
        フィールドの宣言に付けられ、キャッシュを見に行かずに常に最新の値を見に行くようになる。マルチスレッド下における軽量かつ限定的な同期処理に使われる\[3\]。

例:

``` java
public class SampleClass {
    volatile int syncSample;
    ...
}
```

  - **transient**
      -
        フィールドの宣言につけられる。Javaにはオブジェクトをそのまま[ネットワークに送信したり](../Page/コンピュータネットワーク.md "wikilink")[ファイルなどに保存したりするための](../Page/ファイル_\(コンピュータ\).md "wikilink")[シリアライズ](../Page/シリアライズ.md "wikilink")と呼ばれる機能があり、**transient** は対象フィールドがシリアライズの対象にならないことを指示する。スレッドオブジェクトなど、保存できないフィールドや保存されると不都合なフィールドに対して使用される。

## 例外処理

[例外処理](../Page/例外処理.md "wikilink")はC言語にはない。Javaでは、[C++](../Page/C++.md "wikilink")および[C\#とほぼ共通の構文およびキーワードが使用されている](../Page/C_Sharp.md "wikilink")。ただしfinallyはC++には存在せず、throwsはC\#には存在しない。

  - **try**, **catch**, **finally**
      -
        例外が発生しうる箇所で使用する。tryブロック (`try{`と`}`との間) で例外が発生しうるコードを囲み、catchブロック (`catch(`の派生クラス例外オブジェクト`){`と`}`との間) に例外発生後の処理を書く。finallyブロック (`finally{`と`}`との間) には、ファイルのクローズ、データベースセッションの切断、ログアウトなど、例外発生の有無にかかわらずtry/catchブロック内の処理を終了する前に必ず実行しておきたいコードを書く。catchを記述した場合finallyは省略可能であり、finallyを記述した場合catchは省略可能である。try/catchブロックとfinallyブロックの両方にreturn文がある場合、後者が優先される。catchブロックにはif-else-if文のように連続して捕捉したい例外を記述することができる。
  - **throw**
      -
        例外を発生させる。
  - **throws**
      -
        メソッドの宣言で使用される。そのメソッドがどのような例外をスローするかを列挙する。Javaにおける例外の種類には大きく分けて **throws** の明示が必要な例外と必要でない例外がある。前者は主にファイルエラーなどプログラムの動作中にその都度対応すべき例外で、後者は主に開発・デバッグの段階で対処すべき例外あるいは深刻なエラーである。

以下はを使った記述例である。

``` java
public void method() throws Exception { // メソッドが例外をスローすることを宣言
    try {
        ...
        if (エラー条件)
            throw new IOException(); // 例外を発生させる。
        // (1) 正常終了
        // このtryブロックにはreturn文を記述することもできる。
        // ただし、finallyブロックにすでにreturn文があるときは、ここにreturn文を書いてもfinallyブロックのreturnが優先される。
    }
    catch (IOException e) { // IOException は Java の例外クラスの1つ
        // (2) 例外処理
        // このcatchブロックにはreturn文を記述することもできる。
        // ただし、finallyブロックにすでにreturn文があるときは、ここにreturn文を書いてもfinallyブロックのreturnが優先される。
    }
    catch (Exception e) { // IOException よりも上位（親）の例外クラス
        // (3) 例外をさらに外のブロックにスローする。
        throw e;
    }
    finally {
        // (1), (2), (3) どの場合でもこのブロックは必ず実行される。
        // ここにreturn文があるときはtry/catchブロックにreturn文があろうともこちらのreturn文が優先される。
        ...
    }
}
```

## 追加されたキーワード

J2SE 1.4で**assert**が追加され、J2SE 5.0で**enum**が追加された。Java 9では制限されたキーワード (restricted keyword) として、`open`, `module`, `requires`, `transitive`, `exports`, `opens`, `to`, `uses`, `provides`, `with`が追加された\[4\]。また、Java 9では単一の[アンダースコア](../Page/アンダースコア.md "wikilink")`_`が予約済みのキーワードとなり、識別子として使用できなくなった。

Java 10では`var`による[型推論](../Page/型推論.md "wikilink")が追加されたが、これはキーワードではなく、予約された型名 (reserved type name) によって実現されている\[5\]。

## その他

### 浮動小数点演算

その他のキーワードとして、浮動小数点演算の移植性を高める**strictfp**がある。浮動小数点の演算では一般に全く同じ結果は期待できないものではあるが、[x87などハードウェアによっては](../Page/Intel_8087.md "wikilink")、途中の値においてより高い精度や、より広い値の範囲で演算が行われるために、最終結果が他のプラットフォームと一致しない場合があり、特に[IEEE 754を前提として予想される結果から外れることが問題である](../Page/IEEE_754.md "wikilink")。

strictfpを指定すると、途中結果についても全てIEEE 754の倍精度を強制し、相異なるプラットフォーム同士の間でも演算結果が一致することを保証するとされている（仕様では FP-strict という用語を使っている\[6\]）。[Java VMの実装で](https://ja.wikipedia.org/wiki/Java_VM "wikilink")、これを正しく実現するには、x86系CPUを使った計算機の場合、x87を避けてSSE2で計算するか、それができない場合は特殊なテクニック\[7\]が必要である。

なお、同様に移植性のある結果を保証するというクラスがあるが、そちらはFDLIBMというSun製のライブラリと同じ結果を保証するとされている。

### 未使用

**const**、**goto**がキーワードとして予約されているが、Javaでは使用できない。使用すると[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")時に構文エラーになる。

## 注

<references/>

## 参考文献

  -
  -
[Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")

1.  仕様においてreserved wordではなくkeywordと呼んでいる。\[[http://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html\#jls-3.9\]を参照](http://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html#jls-3.9%5Dを参照)。
2.  [Nested Classes (The Java™ Tutorials \> Learning the Java Language \> Classes and Objects)](https://docs.oracle.com/javase/tutorial/java/javaOO/nested.html)
3.  [Javaの理論と実践: volatile を扱う](https://www.ibm.com/developerworks/jp/java/library/j-jtp06197.html)
4.  [The Java Language Specification, Java SE 9 Edition](http://cr.openjdk.java.net/~mr/jigsaw/spec/java-se-9-jls-diffs.pdf)
5.  [Java 10リリース | InfoQ](https://www.infoq.com/jp/news/2018/03/Java10GAReleased)
6.  <http://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.4>
7.  オライリー『Binary Hacks』Hack \#98 を参照。