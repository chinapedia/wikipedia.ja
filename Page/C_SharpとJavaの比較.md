> この記事は[C SharpとJavaの比較](https://ja.wikipedia.org/wiki/C_SharpとJavaの比較)から翻訳されています。


**C\#とJavaの比較**（シーシャープとジャバのひかく）の記事では、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[C\#と](../Page/C_Sharp.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の比較について説明する。

## 言語

### オブジェクトの扱い

いずれの言語も[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")であり、その文法は[C++](../Page/C++.md "wikilink")に類似しているが、C++との互換性はない。メモリ再利用の手段として、従来の手動で解放する方法ではなく[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を使用する。また、[スレッド同期の手段を言語構文に組み込んでいる](../Page/スレッド_\(コンピュータ\).md "wikilink")。

いずれの言語も[強い参照と](../Page/参照_\(情報工学\).md "wikilink")[弱い参照](../Page/弱い参照.md "wikilink")の両方をもつ。Javaでは参照がガベージコレクタによって回収された時に通知を受けるリスナーを登録することができる。これはの[性能](https://ja.wikipedia.org/wiki/性能 "wikilink")を考慮したものである。C\#にはこれに相当する機能はなく、[ファイナライザ](https://ja.wikipedia.org/wiki/ファイナライザ "wikilink")（Javaにも存在する）を使用する方法しかない。その一方、C\#は指定した[オブジェクトのファイナライザ呼び出しをプログラマが抑止することができる](../Page/オブジェクト_\(プログラミング\).md "wikilink")。「世代」の概念をもつガベージコレクション（Javaと[.NETいずれにも当てはまる](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")）においてファイナライザの呼び出しは性能に大きな影響を与えるため、またファイナライザはプログラマがオブジェクトを破棄しなかった場合の[フェイルセーフ](../Page/フェイルセーフ.md "wikilink")であるため、これは非常に有効である。ファイナライザをもつオブジェクトは通常余分な世代が与えられ、回収されるまでに長くかかる。

C\#は、一部の言語設計者から危険であると指摘される[ポインタを使用した演算が制限つきながら利用できる](../Page/ポインタ_\(プログラミング\).md "wikilink")。C\#はポインタを使用するコードブロックあるいは[メソッドを](../Page/メソッド_\(計算機科学\).md "wikilink")`unsafe`キーワードで修飾することでこの懸念に対応している。これにより、このコードを利用する者はそれが他の部分に比べて危険であるということを知ることができる。また、このようなコードをコンパイルする際には[コンパイラ](../Page/コンパイラ.md "wikilink")に対して`/unsafe`スイッチを指定する必要がある。一般に、`unsafe`コードが使われるのは[アンマネージな](../Page/マネージコード.md "wikilink")[APIや](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[システムコール](../Page/システムコール.md "wikilink")との相互運用が必要な時、あるいは性能の向上が必要な時のみである。

### 型システムとデータ型

Javaには大別して参照型（クラス型）と[プリミティブ型](../Page/プリミティブ型.md "wikilink")（基本型）が存在する。参照型はクラスから派生するが、プリミティブ型はスーパークラスを持たない。

一方、C\#には大別して参照型、値型、ポインタ型が存在する\[1\]。このうちポインタ型を除き、あらゆる型はすべて`System.Object`クラスから派生する。クラス (`class`) は参照型であり、数値型や論理型を含む[構造体](../Page/構造体.md "wikilink") (`struct`) および[列挙型](../Page/列挙型.md "wikilink") (`enum`) は抽象クラス`System.ValueType`から暗黙的に派生する値型である\[2\]。

Javaの組み込み型 (built-in type) は[プリミティブ型](../Page/プリミティブ型.md "wikilink")と呼ばれる。C\#は組み込み型をJavaよりも多く持ち、すべての組み込み型は`System`名前空間に存在する型へのエイリアスである\[3\]\[4\]。組み込み型には以下のようなものがある。

  - [整数型](../Page/整数型.md "wikilink"): Javaには符号付き整数のみをサポートし、符号なし整数が存在しない。C\#では符号付き整数と符号なし整数の両方をサポートする。
  - [浮動小数点数](../Page/浮動小数点数.md "wikilink")型: いずれの言語も[IEEE 754準拠の](../Page/IEEE_754.md "wikilink")32bit[単精度浮動小数点数](../Page/単精度浮動小数点数.md "wikilink")と64bit[倍精度浮動小数点数](../Page/倍精度浮動小数点数.md "wikilink")を持つ。

<!-- end list -->

  -
    C\#ではさらに、10の累乗の形で指数部を表す[浮動小数点数](../Page/浮動小数点数.md "wikilink")である`decimal`型をサポートする。`decimal`型は値型かつ組み込み型であるが、CLRのプリミティブではない。

<!-- end list -->

  - [文字型](../Page/キャラクタ_\(コンピュータ\).md "wikilink"): いずれの言語も[UTF-16](../Page/UTF-16.md "wikilink")ベースの文字型を持つ。
  - [ブーリアン型](../Page/ブーリアン型.md "wikilink"): いずれの言語も`true`/`false`のいずれかを表すブーリアン型を持つ。
  - [オブジェクト型](../Page/オブジェクト型.md "wikilink"): C\#では組み込み型として`object`型を持つ。Javaのオブジェクト型は組み込み型ではない。
  - [文字列](../Page/文字列.md "wikilink")型: C\#では組み込み型として`string`型を持つ。Javaの文字列型は組み込み型ではない。

<!-- end list -->

  -
    文字列はいずれの言語においても[不変](../Page/イミュータブル.md "wikilink") () なオブジェクトとして扱われるが、特殊な構築方法として文字列[リテラル](../Page/リテラル.md "wikilink")を利用することができる。C\#では[エスケープ文字](../Page/エスケープ文字.md "wikilink")を処理しないような逐語的文字列リテラル（文字列: [ヒアドキュメント](https://ja.wikipedia.org/wiki/ヒアドキュメント "wikilink")を参照）をサポートする。

C\#言語自体にはプリミティブ型という用語は存在しないが、[.NET Frameworkの](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink") (CLR) では、`System.Type.IsPrimitive`プロパティによって、型がCLRプリミティブ型であるかどうかを判定できる\[5\]。.NET言語組み込みの値型は必ずしもCLRプリミティブ型ではないが、CLRプリミティブ型はすべて値型である。

いずれの言語もプリミティブ型（もしくは値型）と参照型との間で変換するために[ボックス化](../Page/ボックス化.md "wikilink") (boxing) とボックス化解除 (unboxing) が可能である。これによってプリミティブ型（もしくは値型）は参照型のサブセットとみなすことができる。値型は[仮想メソッドテーブルを持たず](https://ja.wikipedia.org/wiki/仮想関数テーブル "wikilink")、したがってそのままでは多態性を利用できないが、C\#においては、ボックス化によって値型で多態性を利用することが可能である（例えば`object`型の`ToString()`メソッドを[オーバーライド](../Page/オーバーライド.md "wikilink")することができる）。C\#では数値リテラルもオブジェクトであり、たとえば`42.ToString()`のように`int`型のリテラルからメソッドを呼び出すことも可能である。Javaではこのような用途のために[プリミティブ型をラップするクラスが別に定義される](../Page/プリミティブラッパークラス.md "wikilink")。すなわち、`42.toString()`のような[インスタンス](../Page/インスタンス.md "wikilink")メソッド呼び出しでなくのような静的メソッド呼び出しが必要になる。もう一つの相違点として、Javaでは[ジェネリクスにおいてこのような型を多用するため](https://ja.wikipedia.org/wiki/総称型 "wikilink")、暗黙的なボックス化解除が可能になっている（C\#ではボックス化せずにジェネリクスを利用できる）。このような変換は[nullポインタ例外を発生する可能性があるが](../Page/NullPointerException.md "wikilink")、Javaではそれがコード上で明白ではない。

C\#では、`struct`[キーワードによって構造体を定義することができる](../Page/予約語.md "wikilink")。構造体にはフィールドやメソッド、プロパティなどの任意のメンバーを定義できる。引数を持たないデフォルト[コンストラクタ](../Page/コンストラクタ.md "wikilink")をプログラマが定義することはできないが、一つ以上の引数をもつパラメータ化されたコンストラクタを定義することはできる。デフォルトコンストラクタはすべてのメンバーを各々の既定値（通例ゼロ相当の値）で初期化する。また構造体を定義する際、メンバーのメモリレイアウトを属性によって細かく制御することができるため、[P/Invoke](https://ja.wikipedia.org/wiki/P/Invoke "wikilink")などによるネイティブコードとの相互運用にも便利である。また、構造体は[継承元となる基底型を指定することはできず](../Page/継承_\(プログラミング\).md "wikilink")、派生型を定義することもできない。ただし任意の[インターフェイスの実装は可能である](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。Javaには構造体が存在せず、ユーザー定義の値型を作成することはできない。

C\#の[列挙型](../Page/列挙型.md "wikilink")は抽象クラス`System.Enum`から暗黙的に派生する値型の一種であり、組み込みの[整数型](../Page/整数型.md "wikilink")をベースとしている。ベースとなる整数型のどの値も列挙型の値として有効になる（明示的なキャストは必要であるが）。このため、[ビットフラグにおいて](../Page/フラグ_\(コンピュータ\).md "wikilink")[ビットごとのOR演算で列挙型の値を組み合わせることが可能である](../Page/ビット演算.md "wikilink")。ただし構造体と違って任意のインターフェイスを実装することはできない。一方、Javaの列挙型は抽象クラスから暗黙的に派生する参照型である。Javaの列挙型として有効な値は定義においてリストされたものだけである。列挙型の値を組み合わせるためには列挙セットクラスを使用する必要がある。Javaの列挙型では、値によって異なるメソッドの実装が可能である。JavaとC\#はいずれも列挙型を文字列に変換することができるが、Javaにおいてはこの変換をカスタマイズすることができる。また、Javaの列挙型は任意のインターフェイスを実装することができる。

プリミティブ型（あるいは値型）は参照型（クラス）とは異なり、インスタンスは[ヒープ領域](../Page/ヒープ領域.md "wikilink")ではなく[スタック](../Page/スタック.md "wikilink")に置かれる。また、（[フィールドとして](../Page/フィールド_\(計算機科学\).md "wikilink")、あるいはボックス化された状態で）クラスの一部になることも、配列の要素になることも可能である。クラスのインスタンスはメモリ上で間接的に参照される必要があるが、プリミティブ型（あるいは値型）はその必要がない。[プログラマ](../Page/プログラマ.md "wikilink")の視点からは、C\#の値型は軽量なクラスとみなせる。しかし、プリミティブ型（あるいは値型）には前述のように多数の制限がある。値型は通常[null](https://ja.wikipedia.org/wiki/null "wikilink")の値をとることができないが、.NET Framework 2.0でnull許容型 (`System.Nullable`) が導入され、C\#でも擬似的にnull値を取り得る値型が利用可能となった。

### 配列

C\#およびJavaの[配列](../Page/配列.md "wikilink")は参照型であり、[第一級オブジェクト](../Page/第一級オブジェクト.md "wikilink")である。C\#の配列は共通の基本クラス`System.Array`から派生するが、Javaの配列はから派生する。代わりに、配列のユーティリティクラスとしてが用意されている。

いずれの言語も配列は共変性 (covariance) を持つ。

``` csharp
System.Console.WriteLine(typeof(int[]).BaseType); // System.Array
object[] objs = new string[3]; // 代入可能。
objs[0] = "test";
objs[0] = 10; // System.ArrayTypeMismatchException
```

``` java
System.out.println(int[].class.getSuperclass()); // java.lang.Object
Object[] objs = new String[3]; // 代入可能。
objs[0] = "test";
objs[0] = 10; // java.lang.ArrayStoreException
```

なお、Java 1.5で拡張for文がサポートされた。これはC\#の[`foreach`](https://ja.wikipedia.org/wiki/foreach文 "wikilink")文に相当する。[配列](../Page/配列.md "wikilink")を始めとする[コレクション型を](../Page/コンテナ_\(データ型\).md "wikilink")、[イテレータ](../Page/イテレータ.md "wikilink")により走査することができる。

C\#は真の多次元配列（矩形配列）をサポートするが、Javaはサポートしない。C\#およびJavaはともに「配列の配列」をサポートする（C\#ではジャグ配列と呼ばれる）。

### 内部クラス

いずれの言語もネストされた型（入れ子にされた型：クラスや構造体のブロックの中で定義されたクラス・構造体・列挙型・インターフェイス）をサポートする。Javaではインターフェイス内部にクラスや列挙型を定義することもできる。C\#ではインターフェイス内部にクラス・構造体・列挙型・インターフェイスを定義することはできない。

Javaでは、ネストされたクラス (nested class) は既定で内部クラス (inner class) となる。内部クラスは外側のクラスのインスタンスを暗黙的にキャプチャすることで、静的メンバ、非静的メンバいずれにもアクセスすることができる。ネストされたクラスが`static`修飾されていた場合は静的メンバのみにアクセスできる。メソッドの内部にクラスを定義することもでき、これはローカルクラス (local class) と呼ばれる。ローカルクラスでは、外側のローカル変数には読み取りアクセスのみできる。また、型の名前を持たないローカルクラス（匿名クラス: anonymous class）を定義し、同時にインスタンス生成をすることもできる。

C\#では、ネストされたクラス／構造体から外側のクラス／構造体の非静的メンバにアクセスするためには外側のクラス／構造体のインスタンスへの明示的な参照が必要になる。Javaの内部クラスやローカルクラスに相当する機能は存在しない。代わりに、C\# 2.0以降では匿名メソッド (anonymous method) が、C\# 3.0以降では[ラムダ式](https://ja.wikipedia.org/wiki/ラムダ式 "wikilink")が、そしてC\# 7.0以降ではローカル関数がサポートされ、外側の変数をキャプチャする[クロージャ](../Page/クロージャ.md "wikilink")として利用できる。なお、C\# 3.0では限定的なローカルクラスとして、匿名型（読み取り専用プロパティのみを持つ、匿名のクラス型）がサポートされる。

### ジェネリクス

Javaでは[ジェネリクスは型消去](../Page/ジェネリックプログラミング.md "wikilink") () によって実装されている。これによってジェネリック型についての情報は実行時には失われ、[リフレクションを通してのみ取得できるようになる](../Page/リフレクション_\(情報工学\).md "wikilink")。.NET 2.0では、[ジェネリック型についての情報は完全に保存される](https://ja.wikipedia.org/wiki/総称型 "wikilink")。Javaはプリミティブ型に対するジェネリック型は定義できないが、C\#では参照型・値型（プリミティブ型を含む）いずれに対してもジェネリック型を定義できる。Javaはその代わりにボックス化した型を使用することができる（`List`<int>の代わりに`List`<Integer>など）が、全ての値をヒープに確保し直す必要があるため、パフォーマンスコストが高い。JavaとC\#はいずれも、参照型に特殊化されたジェネリック型は、型によらず共通のコードが実行される。しかし、C\#において値型に特殊化された場合、CLRは型に最適化されたコードを動的に生成する。[.NETにおいては](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、ジェネリック型に対する型安全性はコンパイル時にチェックされ、[CLRにロードされる時に強制される](../Page/共通言語ランタイム.md "wikilink")。Javaにおいてはコンパイル時に部分的にチェックされるのみであり、[Java VMは実行時にジェネリック型に関する情報を持たないため](../Page/Java仮想マシン.md "wikilink")、キャスト操作を行う必要がある。

#### ジェネリクスの型制約

C\#、Java共に、ジェネリクスの型制約を持つ。C\#では基底型指定以外に、`class`(参照型)、`struct`(値型)、`new()`(デフォルトコンストラクタ有)の各制約を指定できる。

``` csharp
// C#
class ConstraintClass { }
class SomeGenericsClass<T> where T : ConstraintClass { }
class OtherGenericsClass<T> where T : new() { }
```

``` java
// Java
class ConstraintClass { }
class SomeGenericsClass<T extends ConstraintClass> { }
```

#### ジェネリクスの共変性と反変性

C\#、Java共に、ジェネリクスの[共変性と反変性](https://ja.wikipedia.org/wiki/共変性と反変性_\(計算機科学\) "wikilink") (covariance and contravariance) を持つ。ただしC\#における共変性・反変性のサポートはバージョン4.0以降である。

C\#では、型定義側で共変性`out`あるいは反変性`in`を指定し、利用側では変性の指定を行わない。なお、C\#の値型は不変 (invariant) であり、共変性・反変性は適用されない。

``` csharp
// C#
// System.Func<T, TResult> と同様のデリゲートを定義。
// 型定義側で変性の指定を行う。
public delegate TOut MyFunc<in TIn, out TOut>(TIn arg);

public class GenericsTest {
    public static void Main() {
        // 利用側では変性の指定を行わない。
        MyFunc<object, string> func1 = x => "<" + x + ">";
        MyFunc<string, object> func2 = func1;
        object ret = func2("test");
        System.Console.WriteLine(ret);
        System.Console.WriteLine(ret.GetType()); // System.String
    }
}
```

Javaでは、型定義側では変性の指定を行わず、利用側で共変性`extends`あるいは反変性`super`を指定する。 Javaではさらに、上限と下限のいずれも指定しないワイルドカード`?`による型引数の指定が可能である。以下にJava 8の例を示す。

``` java
// Java
// java.util.function.Function<T, R> と同様のインターフェイスを定義。
// 型定義側では変性の指定を行わない。
@FunctionalInterface
interface MyFunc<TIn, TOut> {
    TOut apply(TIn arg);
}

public class GenericsTest {
    public static void main(String[] args) {
        // 利用側で変性の指定を行う。
        MyFunc<? super Object, ? extends String> func1 = x -> "<" + x + ">";
        MyFunc<? super String, ? extends Object> func2 = func1;
        Object ret = func2.apply("test");
        System.out.println(ret);
        System.out.println(ret.getClass().getName()); // java.lang.String

        // 変性の上下限いずれも指定しないこともできる。
        java.util.List<?> list;
    }
}
```

### 型推論

C\# 3.0でコンテキストキーワード`var`による限定された[型推論](../Page/型推論.md "wikilink")が導入された。ローカル変数の宣言時に、型を右辺から推論できる。メソッド引数やフィールドには使えない。また、[ラムダ式](https://ja.wikipedia.org/wiki/ラムダ式 "wikilink")の戻り値および仮引数は型推論により決定される。ラムダ式の仮引数は型を省略することで型推論されるが、型推論が困難な場合には明示的に型を指定する。

Java 7で導入されたダイヤモンド演算子`<>`は宣言文の右辺ジェネリクスの型を省略できる程度のものでしかなかったが、Java 10ではC\#同様に予約型名`var`によるローカル変数の型推論が導入された。Java 8で導入されたラムダ式では、仮引数の型を省略することで型推論されるが、さらにJava 11ではラムダ式の仮引数の型に`var`を使用して型推論できるようになった。

### 表記法と特殊な仕様

Java 1.5で、あるクラスの[静的メソッド](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\)#静的メソッド "wikilink")・[静的フィールドを短い名前で使用するために](../Page/クラス変数.md "wikilink")`static import`構文が導入された。これにより、例えば`ClassA`クラスの`foo()`メソッドを静的インポートして、無関係の`ClassB`クラスにて`ClassA.foo()`のように型名で修飾することなく、`foo()`を直接使用できる。C\# 6.0でも同様の機能として`static using`ディレクティブがサポートされた。

C\#は静的クラス（Javaの静的内部クラスとは異なる）の構文をもち、これによってクラスは静的メソッドのみを持つことができるようになる。C\# 3.0から、型に静的にメソッドを追加するための拡張メソッドが導入されている（`Foo`型のインスタンス`foo`についての処理を行う`Bar()`拡張メソッドを定義することで、あたかも`Foo`にインスタンスメソッドが追加されたかのように、`foo.Bar()`と記述できる）。この機能は、が、ターゲットとなるクラスのプライベートメンバにアクセスすることはできないため、そのような事は無い。

#### キーワード

<table>
<thead>
<tr class="header">
<th><p>キーワード</p></th>
<th><p>仕様・使用例</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>get, set</p></td>
<td><p>C#では、Javaにおける<a href="https://ja.wikipedia.org/wiki/メソッド_(計算機科学)#アクセサ" title="wikilink">アクセサメソッドへの代替として</a><a href="https://ja.wikipedia.org/wiki/プロパティ_(プログラミング)" title="wikilink">プロパティを言語構文としてサポートする</a>。</p></td>
</tr>
<tr class="even">
<td><p>out, ref</p></td>
<td><p>C#ではメソッド引数を<code>out</code>または<code>ref</code>で修飾することで、引数への出力あるいは参照をサポートする。これによって複数の戻り値を得たり、参照渡ししたりといったことが可能になる。 C# 7.0ではさらにメソッドの戻り値を<code>ref</code>修飾して参照とすることができ、<code>ref</code>修飾されたローカル変数でその参照を受け取ることができる[6]。</p></td>
</tr>
<tr class="odd">
<td><p>switch</p></td>
<td><p>C#では<a href="https://ja.wikipedia.org/wiki/switch文" title="wikilink">switch文</a>で整数型、<code>char</code>型、<code>bool</code>型、列挙型、それらの型の<code>Nullable</code>、および<code>string</code>型を使うことができる。C#では<a href="https://ja.wikipedia.org/wiki/フォールスルー" title="wikilink">フォールスルー</a>を許可しない（<code>case</code>ラベルが連続している場合のみ許可される）。C# 7.0ではさらに「型パターン」により型ベースの分岐が可能である。</p>
<p>Javaでは<code>int</code>/<code>short</code>/<code>byte</code>/<code>char</code>型およびそれらのプリミティブラッパークラスを使うことができるが、<code>long</code>/<code>boolean</code>型を使うことはできない。Java 1.5では列挙型を、Java 7では<code>String</code>型を使えるようになったが、C#と違って<code>case</code>ラベルに<code>null</code>を使うことはできない。Javaではフォールスルーを許可する。</p></td>
</tr>
<tr class="even">
<td><p>strictfp</p></td>
<td><p>Javaでは、異なるプラットフォーム間で実数演算結果が同じになるよう保証する<a href="https://ja.wikipedia.org/wiki/strictfp" title="wikilink">strictfp</a>キーワードを利用できる。</p></td>
</tr>
<tr class="odd">
<td><p>checked, unchecked</p></td>
<td><p>C#では、<code>checked</code>ブロック内（あるいは式単体）では実行時に数値<a href="https://ja.wikipedia.org/wiki/算術オーバーフロー" title="wikilink">オーバーフローがチェックされる</a>。</p></td>
</tr>
<tr class="even">
<td><p>using, try</p></td>
<td><p>C#では、<code>using</code>ステートメントによって、作成されたオブジェクトがブロックを抜ける際に確実に破棄されるよう強制することができる。</p>
<div class="sourceCode" id="cb1"><pre class="sourceCode csharp"><code class="sourceCode cs"><span id="cb1-1"><a href="#cb1-1"></a><span class="co">// &quot;test.txt&quot;というファイルを作成し、文字列を書き込み、（例え例外が発生しても）確実に閉じる。</span></span>
<span id="cb1-2"><a href="#cb1-2"></a><span class="kw">using</span> (StreamWriter file = <span class="kw">new</span> <span class="fu">StreamWriter</span>(<span class="st">&quot;test.txt&quot;</span>))</span>
<span id="cb1-3"><a href="#cb1-3"></a>{</span>
<span id="cb1-4"><a href="#cb1-4"></a>   file.<span class="fu">Write</span>(<span class="st">&quot;test&quot;</span>);</span>
<span id="cb1-5"><a href="#cb1-5"></a>}</span></code></pre></div>
<p>Java 7では、try-with-resources構文で同様のリソース解放に対応している。</p></td>
</tr>
<tr class="odd">
<td><p>goto</p></td>
<td><p>C#では<a href="https://ja.wikipedia.org/wiki/goto文" title="wikilink">goto文</a>がサポートされる。これは便利な場面もあるが、通常はより構造化されたフロー制御方法が推奨される。C#では<code>switch</code>ステートメントにおいて<code>goto</code>キーワードを使うことで、異なる<code>case</code>ラベルに移ることができる。</p>
<div class="sourceCode" id="cb2"><pre class="sourceCode csharp"><code class="sourceCode cs"><span id="cb2-1"><a href="#cb2-1"></a><span class="kw">switch</span> (color)</span>
<span id="cb2-2"><a href="#cb2-2"></a>{</span>
<span id="cb2-3"><a href="#cb2-3"></a>   <span class="kw">case</span> Color.<span class="fu">Blue</span>: Console.<span class="fu">WriteLine</span>(<span class="st">&quot;Color is blue&quot;</span>); <span class="kw">break</span>;</span>
<span id="cb2-4"><a href="#cb2-4"></a>   <span class="kw">case</span> Color.<span class="fu">DarkBlue</span>: Console.<span class="fu">WriteLine</span>(<span class="st">&quot;Color is dark&quot;</span>); <span class="kw">goto</span> <span class="kw">case</span> Color.<span class="fu">Blue</span>;</span>
<span id="cb2-5"><a href="#cb2-5"></a>   <span class="co">// ...</span></span>
<span id="cb2-6"><a href="#cb2-6"></a>}</span></code></pre></div>
<p>Javaではgoto文はサポートされない。ただし<code>goto</code>は予約されており、識別子として利用できない。代わりに制限されたgotoとして、ラベル付き<a href="https://ja.wikipedia.org/wiki/break文" title="wikilink">break文</a>/<a href="https://ja.wikipedia.org/wiki/continue文" title="wikilink">continue文</a>を使うことができる。これにより多重ループの脱出などを簡潔に記述できる。</p></td>
</tr>
<tr class="even">
<td><p>yield</p></td>
<td><p>C#ではコンテキストキーワード<code>yield</code>が用意されており、<code>yield return</code>文と<code>yield break</code>文を使用して<a href="../Page/イテレータ.md" title="wikilink">イテレータ</a>（コルーチン）を記述できる。これらの文を含むメソッド（イテレータ）の戻り値はIEnumerableインターフェイス、またはIEnumeratorインターフェイスでなければならない。 また、イテレータは、内部的に状態を持つ<a href="https://ja.wikipedia.org/wiki/ステートマシン" title="wikilink">ステートマシン</a>としてコンパイルされ、値を部分的に返却する列挙子を提供するように振る舞う。</p>
<div class="sourceCode" id="cb3"><pre class="sourceCode csharp"><code class="sourceCode cs"><span id="cb3-1"><a href="#cb3-1"></a><span class="co">// 指定された個数の乱数を生成する</span></span>
<span id="cb3-2"><a href="#cb3-2"></a><span class="kw">public</span> IEnumerable&lt;<span class="dt">int</span>&gt; <span class="fu">RandomValueGenerator</span>(<span class="dt">int</span> count)</span>
<span id="cb3-3"><a href="#cb3-3"></a>{</span>
<span id="cb3-4"><a href="#cb3-4"></a>    <span class="dt">var</span> r = <span class="kw">new</span> <span class="fu">Random</span>();</span>
<span id="cb3-5"><a href="#cb3-5"></a>    <span class="kw">for</span> (<span class="dt">var</span> index = <span class="dv">0</span>; index &lt; count; index++)</span>
<span id="cb3-6"><a href="#cb3-6"></a>    {</span>
<span id="cb3-7"><a href="#cb3-7"></a>        <span class="kw">yield</span> <span class="kw">return</span> r.<span class="fu">Next</span>();</span>
<span id="cb3-8"><a href="#cb3-8"></a>    }</span>
<span id="cb3-9"><a href="#cb3-9"></a>}</span></code></pre></div></td>
</tr>
</tbody>
</table>

#### イベント処理

Javaでは、[Observer パターンの記述を容易にするために匿名クラスという](../Page/Observer_パターン.md "wikilink")[糖衣構文](../Page/糖衣構文.md "wikilink")が用意されている。匿名クラス構文により、クラス本体の定義とインスタンスの生成を同時に行なうことができ、また定義と生成がひとつの式として扱えるため、インターフェイス実装クラスのインスタンスを一度限りしか生成しない場面、例えば特定のインターフェイス実装（あるいは特定のスーパークラスのメソッドの[オーバーライド](../Page/オーバーライド.md "wikilink")）を要求するイベントハンドラーの設定時などによく用いられる。Java 8ではラムダ式がサポートされ、匿名クラスの代わりに使うこともできる。Java 7まではC\#の[デリゲートに相当するものは存在しなかったが](../Page/デリゲート_\(プログラミング\).md "wikilink")、Java 8では類似機能としてメソッド参照がサポートされるようになった。

C\#では[デリゲート](../Page/デリゲート_\(プログラミング\).md "wikilink") (`delegate`) 型をはじめ、[イベント処理をサポートするための機能が広範囲に渡って言語レベルでサポートされている](../Page/イベント_\(プログラミング\).md "wikilink")。デリゲート型はメソッドへの型安全な参照であり、複数のデリゲートを結合して[マルチキャスティングすることもできる](../Page/マルチキャスト.md "wikilink")。デリゲートを結合／分離するための`+`, `-`演算子、イベントハンドラーをカプセル化するためのイベント構文 (`event`, `add`/`remove`) や、イベントハンドラーを登録／削除するための`+=`, `-=`演算子が用意されている。デリゲートは[共変性と反変性](https://ja.wikipedia.org/wiki/共変性と反変性_\(計算機科学\) "wikilink") () をサポートし、完全な[クロージャ](../Page/クロージャ.md "wikilink")としての性質をもつ匿名関数（匿名メソッドおよびラムダ式）を作成することができる。

#### 非同期処理

JavaおよびC\#はともに標準ライブラリでスレッドをサポートしている。OSのスレッドに対する薄い抽象化を提供するクラスとして、Javaには、C\# (.NET) には`System.Threading.Thread`が用意されている。そのほか、セマフォなどの同期オブジェクトやアトミック演算なども標準ライブラリでサポートされている。

言語組み込みの同期構文として、Javaには`syncronized`ブロックおよび`syncronized`メソッドが用意されている。C\#には`lock`ステートメントが用意されている。

C\# 5.0以降は`async`/`await`コンテキストキーワードによる非同期メソッド構文がサポートされた。async/awaitは[イテレータ](../Page/イテレータ.md "wikilink")および.NET 4以降で追加されたタスク並列ライブラリ (Task Parallel Library; TPL) を実行基盤とする糖衣構文であり、非同期タスクの完了待機と実行結果の取得をあたかも同期メソッドのように記述することができる。

### 数値処理

[数学](../Page/数学.md "wikilink")・科学計算・[金融](../Page/金融.md "wikilink")分野のアプリケーション開発に十分対応するための言語仕様が、それぞれに存在する。Javaでは厳密な[浮動小数点計算を強制するために](../Page/浮動小数点数.md "wikilink")`strictfp`キーワードが存在する。これによってあらゆるプラットフォームで必ず同じ値が結果として得られることを保証することができる。C\#にはこれに相当する機能はないが、厳密な浮動小数点計算のために`decimal`型が存在する。これによって二進浮動小数点表現（`float`、`double`）に存在する問題が解決される（[二進表現の浮動小数点数は](https://ja.wikipedia.org/wiki/二進記数法 "wikilink")[十進数を正確に表現することができないため](https://ja.wikipedia.org/wiki/十進記数法 "wikilink")、丸め誤差が生じてしまう）。金融分野の[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")では厳密な十進表現は必須である。Javaでは、このような用途のためにが導入されている。また、Java 1.1では巨大な整数を扱うためのクラス型としてが導入されている。`BigDecimal`と`BigInteger`は最大で約21億桁程度までの[数](../Page/数.md "wikilink")を任意精度で表現できる。C\#においては、.NET Framework 4より`System.Numerics.BigInteger`型が導入されている。

Javaでは、`BigDecimal`や複素数型といったライブラリ定義の型をプリミティブ型と同じレベルで使用することは不可能である。また、Javaではユーザー定義型はすべて参照型扱いとなり、メモリブロックの実体はヒープに確保される。一方、C\#は次のような機能をサポートする。

  - 演算子[多重定義](../Page/多重定義.md "wikilink")やインデクサ。
  - 暗黙的または明示的な型変換。C++のキャスト演算子オーバーロードに似た、ユーザー定義の型変換を定義できる。これにより、例えばプリミティブ数値型同士の変換と類似の機能を提供できる。
  - 値型と値型に対するジェネリック型。値型はスタックに確保される。これは実行時の性能面に影響を及ぼす。

これらに加え、C\#では数値処理アプリケーションのために、コード中の特定領域の数値オーバーフローの実行時チェックの有効・無効を制御することができる`checked`/`unchecked`キーワードを使用できる。

#### 演算子多重定義

Javaは言語仕様をシンプルに保つため、また乱用による難読化を防ぐため、ユーザー定義の演算子オーバーロードをサポートしていない。一方でコードの書きやすさおよび直感性は犠牲になっている。

``` java
var myList = new java.util.ArrayList<Integer>(java.util.Collections.nCopies(10, 0));
myList.set(4, -100);
var gravityTable = new java.util.HashMap<String, Double>();
gravityTable.put("Mercury", 0.377);
gravityTable.put("Venus", 0.9);
gravityTable.put("Earth", 1.0);
double gravityOnVenus = gravityTable.get("Venus");
```

``` java
var b1 = new java.math.BigInteger(Long.toString(Long.MAX_VALUE));
var b2 = new java.math.BigInteger(Integer.toString(1));
var b3 = b1.add(b2);
```

C\#は表記法の多くの点でJavaよりも多機能である。演算子多重定義やユーザー定義キャストなど、それらの多くはC++プログラマによって既に親しまれているものである。

C\#は[インデクサ](../Page/インデクサ.md "wikilink")（C++の`operator[]`に相当）をサポートする。インデクサの定義構文はプロパティと似ているが、`this[]`という名前をもち、一つ以上の引数（インデックス）を持つ点が異なる。インデクサを定義する際、インデックスには任意の型を使用することができる。

``` csharp
var myList = new System.Collections.Generic.List<int>(new int[10]);
myList[4] = -100;
var gravityTable = new System.Collections.Generic.Dictionary<string, double>();
gravityTable["Mercury"] = 0.377;
gravityTable["Venus"] = 0.9;
gravityTable["Earth"] = 1.0;
double gravityOnVenus = gravityTable["Venus"];
```

C\#は（論理的一貫性を保つための制限はあるものの）ユーザー定義の演算子オーバーロードをサポートしており、注意深く使用すれば簡潔で可読性の高いコードを記述することができる。

``` csharp
var b1 = new System.Numerics.BigInteger(long.MaxValue);
var b2 = new System.Numerics.BigInteger(1);
var b3 = b1 + b2;
```

また、C\#では明示的メンバ実装 (Explicit Member Implementation) が可能である。これによって、インターフェイスメソッドの実装とクラス自身のメソッドの実装とを分離することができ、また同じ[シグネチャ](https://ja.wikipedia.org/wiki/シグネチャ "wikilink")（名前および引数の数と型の順序）を持つメソッドが異なるインターフェイスにそれぞれ存在した場合に、インターフェイス名を指定して区別することでそれらの実装を別々に行うことができる。

### メソッド

C\#の[メソッドはデフォルトで非仮想](../Page/メソッド_\(計算機科学\).md "wikilink")（非）であり、仮想メソッドにする必要がある場合は明示的に`virtual`と宣言しなければならない。Javaのメソッドは常に仮想 (C\#でvirtual指定された状態) であり、非仮想にすることはできないが、`final`修飾子を指定することでオーバーライドを禁止することはできる。

Javaでは、メソッドを非仮想的にする方法はない。これは、派生クラスが同名の無関係なメソッドを再定義することが不可能であることを意味する。これは[基底クラスが別のプログラマによって書かれており](../Page/スーパークラス_\(計算機科学\).md "wikilink")、バージョン更新の際に、派生クラスに既に存在していたものと同じシグネチャのメソッドが追加されてしまった場合に問題になる。Javaでは、この場合どちらのプログラマの意図とも異なり、[派生クラスのメソッドは暗黙的に基底クラスのオーバーライドになってしまう](../Page/サブクラス_\(計算機科学\).md "wikilink")（基底クラスでfinal宣言されていた場合はコンパイルエラーになってしまう）。

これらのバージョン更新の問題を部分的に解決するため、[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5.0では[アノテーション](../Page/アノテーション.md "wikilink")が導入された。これにより、基底クラスが同一シグネチャのメソッドを持ち、それが派生クラスで正しくオーバーライドされていることを保証することはできる。しかし[後方互換性](https://ja.wikipedia.org/wiki/後方互換性 "wikilink")維持のため、この指定は必須ではない。従って[IDEやツールなしに上記のように思いがけずオーバーライドしてしまうような問題を防ぐことはできない](../Page/統合開発環境.md "wikilink")。

C\#では、派生クラスで仮想メソッドをオーバーライドする際には、明示的にその旨を宣言する必要がある。メソッドが基底クラスのオーバーライドである場合、`override`修飾子が指定されていなければならない。また、オーバーライドではなく同名の無関係なメソッドを派生クラスで再定義することができるが、コンパイラが警告を発する。コンパイラ警告を抑制したい場合、`new`修飾子を指定しなければならない。

<table>
<thead>
<tr class="header">
<th><p>メソッド種別</p></th>
<th><p>C#</p></th>
<th><p>Java</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>非仮想</p></td>
<td><p>(指定なし)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>仮想</p></td>
<td><p><code>virtual</code></p></td>
<td><p>(指定なし)</p></td>
</tr>
<tr class="odd">
<td><p>抽象</p></td>
<td><p><code>abstract</code></p></td>
<td><p><code>abstract</code></p></td>
</tr>
<tr class="even">
<td><p>オーバーライド</p></td>
<td><p><code>override</code></p></td>
<td><p><code>@Override</code></p></td>
</tr>
<tr class="odd">
<td><p>継承先でのオーバーライド禁止</p></td>
<td><p>(指定なし：非仮想)</p></td>
<td><p><code>final</code></p></td>
</tr>
<tr class="even">
<td><p>オーバーライド かつ 継承先でのオーバーライド禁止</p></td>
<td><p><code>sealed override</code></p></td>
<td><p><code>@Override</code> <code>final</code></p></td>
</tr>
<tr class="odd">
<td><p>隠蔽</p></td>
<td><p><code>new</code></p></td>
<td></td>
</tr>
</tbody>
</table>

### プリプロセッサ

JavaはC/C++でしばしば問題を引き起こしていた[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")を採用しなかった。一方でC\#は限定的にプリプロセッサ[ディレクティブ](../Page/ディレクティブ.md "wikilink")を使用可能である。

#### 条件付きコンパイル

Javaではプリプロセッサがサポートされないため、コンパイル時の分岐は不可能となっている。

一方、C\#ではプリプロセッサディレクティブを用いた条件付きコンパイル (条件コンパイル、) が実装されている。また、指定されたコンパイル定数が定義されている時のみ呼び出されるよう`Conditional`属性をメソッドに指定することができる。この方法によって、`DEBUG`定数が定義されている時のみ評価される[表明](../Page/表明.md "wikilink")（アサート）機能 (`System.Diagnostics.Debug.Assert()`メソッド) が提供されている。Java 1.4からは実行時に有効・無効を切り替えられる`assert`文が言語仕様として導入されている。

### 名前空間とソースファイル

C\#の[名前空間](../Page/名前空間.md "wikilink")はC++のそれと類似している。[Javaのパッケージとは異なり](../Page/パッケージ_\(Java\).md "wikilink")、名前空間はソースファイルの物理的位置とは無関係である。Javaではパッケージ構造と[ソースファイル](https://ja.wikipedia.org/wiki/ソースファイル "wikilink")の位置が必ずしも一致している必要はないものの、デフォルトではそのような振る舞いをする。

Javaではアクセスレベルが`public`のクラス名はソースファイル名 (\*.java) と一致していなければならない。つまり1つのソースファイルに`public`クラスは1つだけしか定義できない。デフォルトのアクセスレベルのクラスであれば、1つのソースファイルに複数のクラスをまとめて記述することができる。

C\#ではそのような制約はなく、クラス名と無関係の1つのソースファイル (\*.cs) に任意のクラスを複数記述することができる。C\# 2.0からは`partial`キーワードによってクラスの定義を複数のファイルに分けて記述することが可能になった。

### 例外処理

Javaは非チェック[例外](../Page/例外処理.md "wikilink") () に加えてチェック済み例外 () をサポートする。C\#では非チェック例外のみである。チェック済み例外は、プログラマがメソッドから発生し得るものを全て宣言し、捕捉する必要がある。

全てのエラーが処理されることを保証できるため、チェック済み例外は非常に便利だとする者もいる。一方、C\#の設計者である[アンダース・ヘルスバーグ](../Page/アンダース・ヘルスバーグ.md "wikilink")のように、Javaのチェック済み例外はある程度実験的な仕様であり、小さなプログラムでの例を除いては実装する価値を見出せなかった、とする者もいる\[7\]\[8\]。一つの批判として、チェック済み例外はプログラマが空のcatchブロックを記述するのを促進し、`catch (``  e) {} `のような危険なコードを増やす結果になってしまったというものがある。また別の批判として、[メソッドの実装に変更を加えた結果新しいチェック済み例外が発生するようになる可能性があり](../Page/メソッド_\(計算機科学\).md "wikilink")、これによって契約が破壊されてしまう、というものがある。これは限られた例外のみが宣言された[インタフェースを実装するメソッドや](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")、メソッドの内部実装が変更された場合に起こり得る。中には、このような予期しない例外が発生することを見越し、あらゆる型の例外が発生し得る、と宣言 (`throws Exception`) するプログラマもいる。これはチェック済み例外の利点を無にしている。しかしながら、いくつかの場面では例外連鎖 ()、すなわち捕捉した例外を別の例外でラップして投げ直す、という手法が適用できる。例えば、ファイルにアクセスするコードが[データベース](../Page/データベース.md "wikilink")にアクセスするよう変更された場合、呼び出し側は内部で何が行われているかを知る必要がないため、が捕捉された場合でもとして投げ直すことが可能である。

`try-finally`ステートメントにおいても両者は異なる。`finally`は例え`try`ブロック内で`throw`や`return`が実行された場合でも必ず実行される。これは、`try`内と`finally`内で異なる値が`return`された場合に予期しない振る舞いを生じることがある。C\#では`finally`ブロック内では`return`や`break`といった文の実行を禁止している。

### 低レベルコード

C/C++などで書かれたネイティブコード資産の再利用や、オペレーティングシステムあるいはハードウェアへのローレベルなアクセスを可能とするため、JavaおよびC\#はともにネイティブ相互運用のための機能を提供している。

[Java Native Interface](../Page/Java_Native_Interface.md "wikilink") (JNI) ではJavaコード内で非Javaコードをnativeメソッドとして呼び出すことができる。しかしながら、JNIは呼び出されるコードのインターフェイス（シグネチャ）に制限がある。このため、Javaと既存のネイティブコード資産との間に余分なレイヤーが必要になることがよくある。このレイヤーはJavaではない言語で書かれる必要があり、CやC++がよく用いられる。JNIを利用することで、逆にC/C++側からJavaのクラスライブラリにアクセスすることも可能である。

.NETのプラットフォーム呼び出し（、[P/Invoke](https://ja.wikipedia.org/wiki/P/Invoke "wikilink")）はC\#からアンマネージコードの呼び出しを可能にする。プログラマは[メタデータを通して](../Page/メタデータ_\(共通言語基盤\).md "wikilink")、メソッドの引数や戻り値がどのように橋渡し（マーシャリング）されるかを完全に制御することができる。このため、既存コードのインターフェイスがC言語形式関数でありさえすれば、余分なレイヤーは必要にならない。P/Invokeは（Win32やPOSIXなどの）手続き型APIにはほぼ完全にアクセスすることができるが、C++クラスライブラリへの直接的なアクセスはきわめて困難である。そのほか、[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")言語を介することで、C\#とC/C++間の相互運用を行なうことも可能である。また[COM相互運用により](../Page/Component_Object_Model.md "wikilink")、コード資産を相互に利用することも可能である。

C\#は通常の型チェックなどのCLRの安全のための機能を無効にし、ポインタ変数を利用することができる。この時、プログラマはコードを`unsafe`キーワードでマークする必要がある。JNI、P/Invoke、`unsafe`コードはどれも同様に「危険な」機能であり、セキュリティホールやアプリケーションの不安定性につながる恐れがある。`unsafe`コードがP/InvokeやJNIに対して優れている点は、アンマネージコードを呼び出すことなくC\#の機能内でタスクを完結できる点である。`unsafe`コードを含む[アセンブリはコンパイル時にそのように明示的に指定する必要がある](../Page/アセンブリ_\(共通言語基盤\).md "wikilink")。これにより、実行環境は危険な可能性があるコードであるということを実行する前に知ることができる。

### 統合言語クエリ

C\#には、[統合言語クエリ](../Page/統合言語クエリ.md "wikilink")の為の拡張されたキーワード群が存在し、ソースコード上でSQL構文に似たクエリを直接記述することができる。このキーワード群は構文糖として機能し、決められた拡張メソッド呼び出しに展開される。

``` csharp
// 数列から偶数を抜き出して表示する
var inputs = new[] { 1, 5, 2, 3, 4, 7, 11, 10, 6 };
#if true
// LINQクエリ構文
var results =
    from inputValue in inputs
    where (inputValue % 2) == 0
    select inputValue;
#else
// LINQメソッド構文
var results = inputs.
        Where(inputValue => (inputValue % 2) == 0).
        Select(inputValue => inputValue);
#endif
foreach (var resultValue in results)
{
    Console.WriteLine(resultValue);
}
```

統合言語クエリの拡張メソッド群は、コレクションに対するさまざまな集合演算が実装されており、このような演算をロジックで記述することなく、簡単に操作することができる。 また、ラムダ式から式ツリー（Expressionクラス）のインスタンスを生成することが出来るため、この機能を使用してデータベースへのクエリ発行・収集を、タイプセーフ性を失うことなく直接的に行うことができる（LINQ to SQL、LINQ to Entitiesなど）。 Javaでは、このようなクエリ構文を直接サポートしない。Java8ではC\#のLINQメソッド構文に近い記述が可能となるStream APIとラムダ式がサポートされた。

## 実装

### JVMとCLR

Javaはまったく異なる多くの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")間で実行できる。またパーソナル・コンピュータに限らず、高度な計算処理や制御を必要とする家電製品や、[Blu-ray Discのインタラクティブ技術にも](../Page/Blu-ray_Disc.md "wikilink")[BD-J](../Page/BD-J.md "wikilink")として使用されている。このように数多くの[Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (Java VM, JVM) 実装が存在する。

C\#および.NETテクノロジーもやはり[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")である。[.NET Frameworkは](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")による.NETの実装であり、[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink") (CLR) はマイクロソフトによる[共通言語基盤](../Page/共通言語基盤.md "wikilink") (CLI) の実装である。主なプラットフォームは[Windowsだが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、他のプラットフォームにも実装が存在する。有名なものに[Monoがある](../Page/Mono_\(ソフトウェア\).md "wikilink")。ただし、マイクロソフトによる実装と比較して未実装部分が多く、利用できるライブラリに大きく制限がある。マイクロソフトによるモバイル／組み込み環境向け実装としては[.NET Compact Frameworkがある](../Page/.NET_Compact_Framework.md "wikilink")。

2017年現在、[.NET Frameworkの他に](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[.NET Core](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")\[9\]やMono/[Xamarin](https://ja.wikipedia.org/wiki/Xamarin "wikilink")などの実装が存在し、多くの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")向けの開発が可能となっている。

### 標準

両言語の構文（文法）、プログラミングインタフェース、バイナリ形式（[実行ファイル](../Page/実行ファイル.md "wikilink")形式）、実行環境などは様々な機関によって管理されている。

C\#は[Ecmaと](https://ja.wikipedia.org/wiki/Ecma_International "wikilink")[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、[JISによって定義されている](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")。標準化の対象は言語構文、[基本クラスライブラリ](https://ja.wikipedia.org/wiki/基本クラスライブラリ "wikilink")、[アセンブリ形式](../Page/アセンブリ_\(共通言語基盤\).md "wikilink")、実行環境（[共通言語基盤](../Page/共通言語基盤.md "wikilink"): CLI）など多岐に渡る。下位層フレームワークの上に新しく実装された上位層ライブラリの多くはこの標準には含まれない（[Windows Forms](../Page/Windows_Forms.md "wikilink")、[ASP.NET](../Page/ASP.NET.md "wikilink")、[ADO.NET](../Page/ADO.NET.md "wikilink")など）。

現在のところ、Javaのどの部分も第三者の[標準化団体によって標準化されていない](../Page/標準化団体_\(コンピュータと通信\).md "wikilink")。Javaの[商標](../Page/商標.md "wikilink")、[ソースコード](../Page/ソースコード.md "wikilink")やその他の素材に関しては[オラクル](../Page/オラクル_\(企業\).md "wikilink")（旧[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）が無制限の独占的な権利を保持しているが、オラクル（[サン](../Page/サン・マイクロシステムズ.md "wikilink")）は[Java Community Process](../Page/Java_Community_Process.md "wikilink")\[10\] (JCP) と呼ばれるプロセスに参加し、当事者たちがJavaに関連する技術（[言語](../Page/プログラミング言語.md "wikilink")、[SDKから](../Page/ソフトウェア開発キット.md "wikilink")[APIに至るまで](../Page/アプリケーションプログラミングインタフェース.md "wikilink")）に対する変更を専門家団体や諮問会議を通して提案することを許可している。JCP内の規定では、Javaに対する新しい仕様や変更はオラクル（サン）による承認が必要であるとされている。JCPは営利寄与者に対しては会費が必要としているが、非営利寄与者や個人は無料で参加できる。JavaのAPIセットにはいくつかのエディションがあり、標準エディションの[Java SE](https://ja.wikipedia.org/wiki/Java_SE "wikilink")、エンタープライズ向けエディションの[Java EE](https://ja.wikipedia.org/wiki/Java_EE "wikilink")、モバイル／組み込み環境向けエディションの[Java MEが存在する](https://ja.wikipedia.org/wiki/Java_ME "wikilink")。

## 姉妹言語

C\#およびJavaには、それぞれの実行環境を用いて動作する姉妹言語が存在し、それぞれ.NET言語およびJVM言語と呼ばれている。姉妹言語は他の既存言語からの移行のしやすさや、記述能力および生産性の向上、あるいは新たな[プログラミングパラダイム](../Page/プログラミングパラダイム.md "wikilink")を導入するなどの目的で開発されたものであり、異なる言語間でユーザー定義のクラス型などを再利用する相互運用も可能である。

各々の代表的な姉妹言語を列挙する。

  - .NET言語

<!-- end list -->

  - [Visual Basic .NET](../Page/Visual_Basic_.NET.md "wikilink")
  - [F\#](../Page/F_Sharp.md "wikilink")
  - [IronPython](../Page/IronPython.md "wikilink")

<!-- end list -->

  - JVM言語

<!-- end list -->

  - [Scala](../Page/Scala.md "wikilink")
  - [Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")
  - [Groovy](../Page/Groovy.md "wikilink")

## 参照

## 関連項目

  - [JavaとC++の比較](../Page/JavaとC++の比較.md "wikilink")

[Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:C_Sharp](https://ja.wikipedia.org/wiki/Category:C_Sharp "wikilink") [Category:ソフトウェアの比較](https://ja.wikipedia.org/wiki/Category:ソフトウェアの比較 "wikilink")

1.  [型 (C\# リファレンス) | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/csharp/language-reference/keywords/types)
2.  [値型 (C\# リファレンス) | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/csharp/language-reference/keywords/value-types)
3.  \[<https://docs.microsoft.com/ja-jp/previous-versions/visualstudio/visual-studio-2008/ms228360(v=vs.90>) データ型 (C\# と Java の比較) | Microsoft Docs\]
4.  [Built-in types table (C\# Reference) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/built-in-types-table)
5.  [Type.IsPrimitive Property (System) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.type.isprimitive)
6.  [C\# 7.0 の新機能 - C\# ガイド | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/csharp/whats-new/csharp-7#ref-locals-and-returns)
7.  [The Trouble with Checked Exceptions](http://www.artima.com/intv/handcuffs.html)
8.  [Why doesn't C\# have exception specifications?](http://msdn2.microsoft.com/en-us/vcsharp/aa336812.aspx)
9.  [.NET Core とオープン ソース | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/framework/get-started/net-core-and-open-source)
10. [「Javaはオラクルのもの？」、「いいえ、これからもJavaコミュニティのものです！」――Javaエバンジェリスト 寺田佳央氏が、Javaの現在、未来を語る](https://www.oracle.com/technetwork/jp/database/articles/pickup/index-1838236-ja.html)