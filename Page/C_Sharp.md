> この記事は[C Sharp](https://ja.wikipedia.org/wiki/C_Sharp)から翻訳されています。


**C\#**（シーシャープ）は、[アンダース・ヘルスバーグ](../Page/アンダース・ヘルスバーグ.md "wikilink")が設計した[プログラミング言語](../Page/プログラミング言語.md "wikilink")であり、構文はその名前にもある通りC系言語（[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")など）の影響があるが、構文以外の言語機能などについてはヘルスバーグが以前の所属である[ボーランド](../Page/ボーランド.md "wikilink")で設計した[Delphi](../Page/Delphi.md "wikilink")からの影響がある。

マイクロソフトによる謳い文句としては、[マルチパラダイムプログラミング言語](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")、強い[型付け](../Page/型システム.md "wikilink")、[命令型](../Page/命令型プログラミング.md "wikilink")、[宣言型](../Page/宣言型プログラミング.md "wikilink")、[手続き型](../Page/手続き型プログラミング.md "wikilink")、[関数型](../Page/関数型言語.md "wikilink")、[ジェネリック](../Page/ジェネリックプログラミング.md "wikilink")、[オブジェクト指向の要素を持つ](../Page/オブジェクト指向プログラミング.md "wikilink")、などといった点が強調されている。

[共通言語基盤](../Page/共通言語基盤.md "wikilink") (CLI) といった周辺技術も含め、マイクロソフトのフレームワーク「[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")」の一部である他、[Visual J++で](https://ja.wikipedia.org/wiki/Microsoft_Visual_J++ "wikilink")「非互換なJava」をJavaに持ち込もうとしたような以前のマイクロソフトとは異なり、その多くの仕様を積極的に公開し標準化機構に託して自由な利用を許す (ECMA-334, ISO/IEC 23270:2003, JIS X 3015) など、同社の姿勢の変化があらわれている。

## 概要

開発にはボーランドの[Turbo PascalやDelphiを開発したアンダース](../Page/Turbo_Pascal.md "wikilink")・ヘルスバーグを筆頭に多数のDelphi開発陣が参加している。

C\#は[共通言語基盤](../Page/共通言語基盤.md "wikilink")（[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink")など）が解釈する[共通中間言語](../Page/共通中間言語.md "wikilink")に[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")されて実行される。

[自動ボックス化](../Page/ボックス化.md "wikilink")、[デリゲート](../Page/デリゲート_\(プログラミング\).md "wikilink")、 [プロパティ](https://ja.wikipedia.org/wiki/プロパティ_\(プログラミング\) "wikilink")、[インデクサ](../Page/インデクサ.md "wikilink")、[カスタム属性](../Page/メタデータ_\(共通言語基盤\).md "wikilink")、[ポインタ演算操作](../Page/ポインタ_\(プログラミング\).md "wikilink")、[構造体](../Page/構造体.md "wikilink")（値型オブジェクト）、[多次元配列](../Page/配列.md "wikilink")、[可変長引数](../Page/引数.md "wikilink")、などの機能を持つ。また、Javaと同様に大規模[ライブラリ](../Page/ライブラリ.md "wikilink")、[プロセッサ・アーキテクチャ](https://ja.wikipedia.org/wiki/プロセッサ・アーキテクチャ "wikilink")に依存しない実行形態、[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")、[JITコンパイルによる実行の高速化](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")、などが実現されている（もっともこれらはC\#の機能というより.NET Frameworkによるものである）。

.NET構想における中心的な開発言語であり、[XML](../Page/Extensible_Markup_Language.md "wikilink") [Webサービス](../Page/Webサービス.md "wikilink")や[ASP.NET](../Page/ASP.NET.md "wikilink")の記述にも使用される。他の.NET系の言語でも記述可能だが、。マイクロソフトの[統合開発環境](../Page/統合開発環境.md "wikilink")では、[Microsoft Visual C\#がC](../Page/Microsoft_Visual_C_Sharp.md "wikilink")\#に対応している。

共通言語仕様のCLSによって、他のCLS準拠の言語（[Visual Basic .NETや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")[Visual C++](../Page/Microsoft_Visual_C++.md "wikilink") ([C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")) など）と相互に連携することができる。

## バージョンおよびリリース時期

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>言語仕様</p></th>
<th><p>リリース時期</p></th>
<th><p>実装</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Visual_Studio" title="wikilink">Visual Studio</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Ecma_International" title="wikilink">ECMA</a>[1][2]</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ISO/IEC" title="wikilink">ISO/IEC</a></p></td>
<td><p><a href="../Page/マイクロソフト.md" title="wikilink">マイクロソフト</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.0</p></td>
<td><p><a href="http://www.ecma-international.org/publications/files/ECMA-ST-WITHDRAWN/ECMA-334,%202nd%20edition,%20December%202002.pdf">ECMA-334:2003</a>(2002年12月)</p></td>
<td><p><a href="https://www.iso.org/standard/36768.html">ISO/IEC 23270:2003</a>(2003年4月)</p></td>
<td><p><a href="http://download.microsoft.com/download/a/9/e/a9e229b9-fee5-4c3e-8476-917dee385062/CSharp%20Language%20Specification%20v1.0.doc">2002年1月</a></p></td>
<td><p>2002年1月</p></td>
</tr>
<tr class="odd">
<td><p>1.1<br />
1.2</p></td>
<td><p><a href="http://download.microsoft.com/download/5/e/5/5e58be0a-b02b-41ac-a4a3-7a22286214ff/csharp%20language%20specification%20v1.2.doc">2003年10月</a></p></td>
<td><p>2003年4月</p></td>
<td></td>
<td><p>.NET 2003</p></td>
</tr>
<tr class="even">
<td><p>2.0</p></td>
<td><p><a href="http://www.ecma-international.org/publications/files/ECMA-ST-ARCH/Ecma-334%204th%20edition%20June%202006.pdf">ECMA-334:2006</a>(2006年6月)</p></td>
<td><p><a href="https://www.iso.org/standard/42926.html">ISO/IEC 23270:2006</a>(2006年9月)</p></td>
<td><p><a href="http://download.microsoft.com/download/9/8/f/98fdf0c7-2bbd-40d3-9fd1-5a4159fa8044/csharp%202.0%20specification_sept_2005.doc">2005年9月</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td></td>
<td></td>
<td><p><a href="http://download.microsoft.com/download/3/8/8/388e7205-bc10-4226-b2a8-75351c669b09/CSharp%20Language%20Specification.doc">2007年8月</a></p></td>
<td><p>2007年11月</p></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td></td>
<td></td>
<td><p>2010年4月</p></td>
<td><p>2010年4月</p></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p><a href="https://www.ecma-international.org/publications/files/ECMA-ST/ECMA-334.pdf">ECMA-334:2017</a>(2017年12月)</p></td>
<td><p><a href="https://www.iso.org/standard/75178.html">ISO/IEC 23270:2018</a>(2018年12月)</p></td>
<td><p><a href="https://www.microsoft.com/en-us/download/details.aspx?id=7029">2013年6月</a></p></td>
<td><p>2012年8月</p></td>
</tr>
<tr class="even">
<td><p>6.0</p></td>
<td></td>
<td></td>
<td><p><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/">Draft</a></p></td>
<td><p>2015年7月</p></td>
</tr>
<tr class="odd">
<td><p>7.0</p></td>
<td></td>
<td></td>
<td></td>
<td><p>2017年3月</p></td>
</tr>
<tr class="even">
<td><p>7.1</p></td>
<td></td>
<td></td>
<td></td>
<td><p>2017年8月</p></td>
</tr>
<tr class="odd">
<td><p>7.2</p></td>
<td></td>
<td></td>
<td></td>
<td><p>2017年11月</p></td>
</tr>
<tr class="even">
<td><p>7.3</p></td>
<td></td>
<td></td>
<td></td>
<td><p>2018年5月</p></td>
</tr>
<tr class="odd">
<td><p>8.0</p></td>
<td></td>
<td></td>
<td></td>
<td><p>2019年9月</p></td>
</tr>
</tbody>
</table>

## 言語仕様

さまざまな意味において、基盤である[CLIの機能をもっとも反映している言語であるといえる](../Page/共通言語基盤.md "wikilink")。C\#にある組み込み型のほとんどは、CLIフレームワークに実装されている値型と対応している。しかし、C\#の言語仕様はコンパイラのコード生成については何も言及していない。つまり、[CLRに対応しなければならないとか](../Page/共通言語ランタイム.md "wikilink")、[共通中間言語](../Page/共通中間言語.md "wikilink") (CIL) などの特定のフォーマットのコードを生成しなければならないとかいうことは述べられていない。そのため、理論的には[C++](../Page/C++.md "wikilink")や[FORTRAN](../Page/FORTRAN.md "wikilink")のように環境依存のマシン語を生成することも可能である。しかし、現在存在するすべてのC\#コンパイラはCLIをターゲットにしている。

### CやC++からの改良点

C\#では、CやC++と比較してさまざまな制限や改良が加えられている。また、仕様の多くはC\#言語というよりは、基盤である.NET Frameworkそのものに依拠している。Javaで導入された制限および改良をC\#でも同様に採用しているものが多いが、C\#で新たに導入された改良がのちにJavaにも同様に採用されたものもある。その例を次に挙げる。

#### 構文や構文以外の改良点

  - 外のブロックで宣言した変数と同じ名前の変数を、内のブロックで再宣言（シャドウ）してはいけない。再宣言は便利なこともあれば、混乱や曖昧のもとと主張されることもあるが、C\#では禁止されている。
  - C\#には[ブール型](../Page/ブーリアン型.md "wikilink")`bool`が存在し、[`while`](https://ja.wikipedia.org/wiki/while文 "wikilink")文や[`if`](https://ja.wikipedia.org/wiki/if文 "wikilink")文のように条件をとるステートメントには、`bool`型の式を与えなければならない。C言語では、ブール型が無く`int`型（0を偽とし、非0を真とする）に兼用させた上、（[ヌルポインタ](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")を偽とみなすこととするといろいろと便利だった、ということもあり）ポインタでも`while`文や`if`文に与える式にできる、という仕様としていた。これは便利なこともあったが、本来比較式を記述すべきところで誤って代入式を記述してもコンパイル適合となってしまうなど、ミスが見逃されることもあった。C\#ではに、そのような仕様ではなくブール型を独立させ、またブール型を厳密に要求する場所を多くしている。
  - [`switch`](https://ja.wikipedia.org/wiki/switch文 "wikilink")文に整数型あるいは整数型に準ずる型のみならず、文字列型`string`を使用できる。`case`ラベルには、整数型あるいは整数型に準ずる型の定数のみならず、文字列リテラル（文字列定数）を使用できる。
  - 組み込み型のサイズおよび内部表現が仕様で定められており、プラットフォームや処理系に依存しない。[浮動小数点数](../Page/浮動小数点数.md "wikilink")は[IEEE 754に準拠する](../Page/IEEE_754.md "wikilink")\[3\]。文字および文字列は[UTF-16](../Page/UTF-16.md "wikilink")エンコーディングを採用する\[4\]。

#### ポインタとメモリ管理

  - ポインタをサポートする。ポインタは`unsafe`スコープ内のみで使用することができ、適切な権限をもつプログラムのみが`unsafe`とマークされたコードを実行することができる。オブジェクトへのアクセスの大部分は管理された安全な参照によってなされ、大部分の算術演算はオーバフローのチェックがなされる。`unsafe`ポインタは値型や文字列を指すことができる。セーフコードでは、必ずしもそうする必要はないものの、`IntPtr`型を通してポインタをやりとりすることができる。
  - マネージドなメモリを明示的に解放する方法は存在せず、参照されなくなったメモリは[ガベージコレクタによって自動的に解放される](../Page/ガベージコレクション.md "wikilink")。ガベージコレクタは、メモリの解放忘れによって起こるメモリリークを解消する。C\#は、データベース接続のようなアンマネージドなリソースに対しても明示的に制御する方法を提供している。これは`IDisposable`インターフェイスと`using`ステートメントによってなされる。

#### 名前空間とオブジェクト指向な型システム

  - [グローバル変数](../Page/グローバル変数.md "wikilink")やグローバルメソッドは存在しない。すべての[フィールドと](../Page/フィールド_\(計算機科学\).md "wikilink")[メソッドはクラスあるいは構造体の一部として宣言されなければならない](../Page/メソッド_\(計算機科学\).md "wikilink")。

<!-- end list -->

  -
    例えばC/C++の[`printf`](https://ja.wikipedia.org/wiki/printf "wikilink")`()`関数のように[名前空間](../Page/名前空間.md "wikilink")レベルに存在するフリー関数を定義することはできない。ほとんどの場合クラスおよび構造体は名前の衝突を避けるために[名前空間](../Page/名前空間.md "wikilink")に所属する。

<!-- end list -->

  - 名前空間は階層構造をもつ。つまり、名前空間は他の名前空間の中に宣言することができる。
  - 組み込みの値型を含めたすべての型は、`object`クラス (`System.Object`) の派生型である。つまり`object`クラスのもつすべてのプロパティやメソッドを継承する。例えば、すべての型は`ToString()`メソッドをもつ。
  - クラス (`class`) は参照型であり、構造体 (`struct`) および列挙型 (`enum`) は値型である。構造体はクラスよりも軽量で、C/C++との相互運用性に優れるが、派生型を定義することができない。
  - クラスおよび構造体は複数の[インターフェイスを実装することができるが](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")、[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")はサポートされない。
  - C\#はC++に比べて型安全である。既定の暗黙変換は、整数の範囲を広げる変換や、派生クラスから基底クラスへの変換といった、安全な変換のみに限定される。これは、コンパイル時、[JITコンパイル時](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")、そして一部の動的なケースでは実行時に強制される。ブール型と整数型、列挙型と整数型、の間は暗黙変換はできない。暗黙変換をユーザー定義する際は、明示的にそのように指定しなければならない。これはC++のコンストラクタとは違った仕様である。
  - 列挙型のメンバーは、列挙型のスコープの中に置かれる。また、列挙型の定数名を取得することができる。さらに、列挙型の定数名から動的に定数値を得ることができる。
  - [アクセサ](https://ja.wikipedia.org/wiki/アクセサ "wikilink")の定義と利用を簡略化するために[プロパティ構文を利用できる](https://ja.wikipedia.org/wiki/プロパティ_\(プログラミング\) "wikilink")。C++およびJavaにおける[カプセル化](../Page/カプセル化.md "wikilink")では、通例getter/setterアクセサとなるメンバー関数あるいはメソッドを定義して利用するが、C\#ではプロパティ機能により、[カプセル化](../Page/カプセル化.md "wikilink")を維持しつつ、あたかも[フィールドを直接読み書きするような直感的な構文でオブジェクトの状態にアクセスすることができる](../Page/フィールド_\(計算機科学\).md "wikilink")。プロパティによってメンバーのアクセス制御やデータの正当性チェックを実行することができる。なお、[イベントハンドラー](https://ja.wikipedia.org/wiki/イベントハンドラー "wikilink")に利用するデリゲートのカプセル化にはイベント構文 (`event`) が用意されている。

### C\# 2.0からの仕様

#### 部分型

部分型 () が導入された\[5\]。以下のようにクラスや構造体の宣言に`partial`修飾子をつけることで、その宣言を分割することができる。

``` csharp
partial class MyClass { int a; }
partial class MyClass { int b; }
```

これは以下と同義である:

``` csharp
class MyClass { int a; int b; }
```

これによって、巨大なクラスを分割したり、自動生成されたコードを分離したりすることができる。`partial` 修飾子はすべての宣言につける必要がある。

#### ジェネリクス

[ジェネリクスが導入された](https://ja.wikipedia.org/wiki/総称型 "wikilink")。これは.NET Framework 2.0の機能である。クラス、構造体、インターフェイス、デリゲート、メソッドに対して適用することができる。.NETのGenericsはC++の[テンプレート](../Page/テンプレート_\(プログラミング\).md "wikilink")、あるいは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")におけるそれとも異なるもので、コンパイルによってではなく実行時にランタイムによって特殊化される。これによって異なる言語間の運用を可能にし、リフレクションによって型パラメーターに関する情報を取得することができる。また、`where`節によって型パラメーターに制約を与えることができる。一方、C++のように型パラメーターとして[式を指定することはできない](../Page/式_\(プログラミング\).md "wikilink")。なお、ジェネリックメソッドの呼び出し時に引数によって型パラメーターが推論できる場合、型パラメーターの指定は省略できる。

#### 静的クラス

静的クラスが導入された。`static`属性をクラスの宣言につけることで、クラスは[インスタンス](../Page/インスタンス.md "wikilink")化できなくなり、静的なメンバーしか持つことができなくなる。

#### yieldキーワード

`yield`キーワードによる[コルーチン](../Page/コルーチン.md "wikilink")を使うことで、[イテレータの生成を楽に実装できるようになった](https://ja.wikipedia.org/wiki/ジェネレータ_\(プログラミング\) "wikilink")。

#### 匿名デリゲート

[クロージャ](../Page/クロージャ.md "wikilink")の機能を提供する匿名[デリゲートが導入された](../Page/デリゲート_\(プログラミング\).md "wikilink")。

#### プロパティに対する個別のアクセス制御

プロパティの`get` もしくは `set`アクセサのどちらかにアクセス修飾子を指定することでアクセス制御が別個にできるようになった。次の例では、`get`アクセサは`public`、`set`アクセサは`private`である。

``` csharp
public class MyClass
{
  private string status = string.Empty;
  public string Status
  {
    get { return status; }
    private set { status = value; }
  }
}
```

#### Null許容型とnull結合演算子

nullを保持できる値型、`Nullable`が導入された。

``` csharp
int? i = 512;
i = null;

int? j = i + 500; //jはnullとなる。nullとの演算の結果はnullになる。
```

`int?`は`Nullable`<int>の[糖衣構文](../Page/糖衣構文.md "wikilink")である。また、nullを保持しているNull許容型のインスタンスを[ボックス化](../Page/ボックス化.md "wikilink")しようとすると、単に空参照 (null) に変換される\[6\]。

``` csharp
int? x = null;
object o = x;
System.Console.WriteLine(o == null); //Trueが出力される
```

また、[null結合演算子](https://ja.wikipedia.org/wiki/null合体演算子 "wikilink") (`??`)が導入された。これは、`null`でない最初の値を返す。

``` csharp
object obj1 = null;
object obj2 = new object();
object obj3 = new object();
return obj1 ?? obj2 ?? obj3; // obj2 を返す
```

この演算子は主に`Nullable`型を非`Nullable`型に代入するときに使われる。

``` csharp
int? i = null;
int j = i ?? -1; // nullをint型に代入することはできない
```

### C\# 3.0からの仕様

#### varキーワード

`var` キーワードが導入され、[型推論](../Page/型推論.md "wikilink")を利用したローカル変数の宣言ができるようになった。

``` csharp
var s = "foo";
// 上の文は右辺が string 型であるため、次のように解釈される:
string s = "foo";
// 以下に挙げる文は誤りである（コンパイルエラーとなる）:
var v; // 初期化式を欠いている (型を推論する対象が存在しない)
var v = null; // 型が推論できない (曖昧である)
```

#### 拡張メソッド

拡張メソッド (extension method) が導入された。既存のクラスを継承して新たなクラスを定義することなく、新たなインスタンスメソッドを疑似的に追加定義することができる。具体的には、入れ子になっていない、非ジェネリックの静的クラス内に、`this` 修飾子をつけた、拡張メソッドを追加する対象の型の引数を最初に持つメソッドをまず定義する。これによって、通常の静的メソッドとしての呼び出しの他に、指定した型のインスタンスメソッドとしての呼び出しを行うことができるメソッドを作ることができる。以下に例を挙げる:

``` csharp
public static class StringUtil
{
  public static string Repeat(this string str, int count)
  {
    var array = new string[count];
    for (var i = 0; i < count; ++i) array[i] = str;
    return string.Concat(array);
  }
}
```

この例は、文字列（`string` 型のインスタンス）を指定した回数繰り返し連結したものを返すメソッド `Repeat` を、既存の `string` 型に追加している。このメソッドは、以下のように呼び出すことができる:

``` csharp
// 静的メソッドとしての呼び出し
StringUtil.Repeat("foo", 4);
// 拡張メソッドとしての呼び出し
"foo".Repeat(4);
// (どちらの例も "foofoofoofoo" を返す)
```

また、列挙型やインターフェイスなど本来メソッドの実装を持ち得ない型に、見かけ上インスタンスメソッドを追加することも可能である。以下に例を挙げる:

``` csharp
public enum Way
{
  None, Left, Right, Up, Down
}

public static class EnumUtil
{
  public static Way Reverse(this Way src)
  {
    switch (src)
    {
      case Way.Left:  return Way.Right;
      case Way.Right: return Way.Left;
      case Way.Up:    return Way.Down;
      case Way.Down:  return Way.Up;
      default: return Way.None;
    }
  }
}
```

このメソッドは以下のように呼び出すことができる:

``` csharp
Way l = Way.Left;
Way r = l.Reverse(); // Way.Right
```

拡張メソッドは[糖衣構文](../Page/糖衣構文.md "wikilink")の一種であり、[カプセル化](../Page/カプセル化.md "wikilink")の原則に違反するものではないが、必要な場合に限り注意して実装することがガイドラインとして推奨されている\[7\]。

#### 部分メソッド

部分メソッドが導入された。部分型（`partial` 型）内で定義された `private` で、かつ戻り値が `void` のメソッドに `partial` 修飾子をつけることでメソッドの宣言と定義を分離させることができる。定義されていない部分メソッドは何も行わず、何らエラーを発生させることもない。例えば:

``` csharp
partial class Class
{
  partial void DebugOutput(string message);

  void Method()
  {
    DebugOutput("Some message");
    Console.WriteLine("Did something.");
  }
}
```

上のコードにおいて `Method()` を呼び出すと、`Did something.` と表示されるだけだが、ここで以下のコード:

``` csharp
partial class Class
{
  partial void DebugOutput(string message)
  {
    Console.Write("[DEBUG: {0}] ", message);
  }
}
```

を追加した上で `Method()` を呼び出すと、`[DEBUG: Some message] Did something.` と表示される。

#### ラムダ式

ラムダ式が導入された。この名前は[ラムダ計算](../Page/ラムダ計算.md "wikilink")に由来する。

以下の匿名メソッド

``` csharp
// iを変数としてi+1を返すメソッド
delegate (int i) { return i + 1; }
```

は、ラムダ式を使って次のように記述できる:

``` csharp
(int i) => i + 1; /* 式形式のラムダ */
//或いは:
(int i) => { return i + 1; }; /* ステートメント形式のラムダ */
```

ラムダ式は匿名メソッドと同様に扱えるが、式形式のラムダが`Expression`<TDelegate>型として扱われた場合のみ匿名メソッドとして扱われず、コンパイラによって式木を構築するコードに変換される。匿名デリゲートが実行前にコンパイルされた[CILを保持するのに対し](../Page/共通中間言語.md "wikilink")、式木はCILに実行時コンパイル可能である[DOMのような式の](../Page/Document_Object_Model.md "wikilink")[木構造そのものを保持する](../Page/木構造_\(データ構造\).md "wikilink")。これはLINQクエリをSQLクエリなどに変換する際に役立つ。

以下は、3つの任意の名前の変数、整数、括弧、及び四則演算子のみで構成された式を[逆ポーランド記法](../Page/逆ポーランド記法.md "wikilink")に変換する汎用的なコードである:

``` csharp
public static string ToRPN(Expression<Func<int, int, int, int>> expression)
{
  return Parse((BinaryExpression) expression.Body).TrimEnd(' ');
}

private static string Parse(BinaryExpression expr)
{
  string str = "";

  if (expr.Left is BinaryExpression)
  {
    str += Parse((BinaryExpression) expr.Left);
  }
  else if (expr.Left is ParameterExpression)
  {
    str += ((ParameterExpression) expr.Left).Name + " ";
  }
  else if (expr.Left is ConstantExpression)
  {
    str += ((ConstantExpression) expr.Left).Value + " ";
  }

  if (expr.Right is BinaryExpression)
  {
    str += Parse((BinaryExpression) expr.Right);
  }
  else if (expr.Right is ParameterExpression)
  {
    str += ((ParameterExpression) expr.Right).Name + " ";
  }
  else if (expr.Right is ConstantExpression)
  {
    str += ((ConstantExpression) expr.Right).Value + " ";
  }

  return str + expr.NodeType.ToString()
    .Replace("Add", "+")
    .Replace("Subtract", "-")
    .Replace("Multiply", "*")
    .Replace("Divide", "/")
    + " ";
}

// 呼び出し例:
ToRPN((x, y, z) => (x + 1) * ((y - 2) / z)); // "x 1 + y 2 - z / *" を返す
```

#### オブジェクト初期化の簡略化

オブジェクトの初期化が式として簡潔に記述できるようになった。

``` csharp
var p = new Point { X = 640, Y = 480 };
// 上の文は次のように解釈される:
Point __p = new Point();
__p.X = 640;
__p.Y = 480;
Point p = __p;
```

また、コレクションの初期化も同様に簡潔に記述できるようになった。

``` csharp
var l = new List<int> {1, 2, 3};
var d = new Dictionary<string, int> {{"a", 1}, {"b", 2}, {"c", 3}};
// 上の文は次のように解釈される:
List<int> __l = new List<int>();
__l.Add(1);
__l.Add(2);
__l.Add(3);
List<int> l = __l;
Dictionary<string, int> __d = new Dictionary<string, int>();
__d.Add("a", 1);
__d.Add("b", 2);
__d.Add("c", 3);
Dictionary<string, int> d = __d;
```

但し、上のコードでは匿名の変数に便宜的に __p、__l、__d と命名している。実際はプログラマはこの変数にアクセスすることはできない。

#### 自動実装プロパティ

プロパティをより簡潔に記述するための自動実装プロパティが導入された。プロパティの定義に `get; set;` と記述することで、プロパティの値を保持するための匿名のフィールド（プログラマは直接参照することはできない）と、そのフィールドにアクセスするためのアクセサが暗黙に定義される。また、C\# 5.0 までは `get;`と`set;`のどちらか片方だけを記述することは出来なかったが、C\# 6.0 からは `get;` のみが可能。以下のコード:

``` csharp
public int Value { get; set; }
```

は、以下のようなコードに相当する動作をする:

``` csharp
private int __value;
public int Value
{
  get { return __value; }
  set { __value = value; }
}
```

但し、上のコードでは匿名のフィールドに便宜的に `__value` と命名している。実際はプログラマはこのフィールドにアクセスすることはできない。

#### 匿名型

一時的に使用される型を簡単に定義するための匿名型が導入された。以下に例を挙げる:

``` csharp
new { Name = "John Doe", Age = 20 }
```

上の式は、以下の内容のクラスを暗黙に定義する。定義されたクラスは匿名であるが故にプログラマは参照できない。

``` csharp
public string Name { get; }
public int Age { get; }
```

同じ型、同じ名前のプロパティを同じ順序で並べた匿名型は同じであることが保証されている。即ち、以下のコード:

``` csharp
var her = new { Name = "Jane Doe", Age = 20 }
var him = new { Name = "John Doe", Age = 20 }
```

において、`her.GetType() == him.GetType()` は `true` である。

#### 配列宣言の型省略

`new` キーワードを用いた配列の宣言の際、型を省略できるようになった。匿名型の配列を宣言する際に威力を発揮する。

``` csharp
var a = new[] {"foo", "bar", null};
// 上の文は次のように解釈される:
string[] a = new string[] {"foo", "bar", null};
// 以下の文:
var a = new[] {"foo", "bar", 123};
// は次のように解釈されることなく、誤りとなる:
object[] a = new object[] {"foo", "bar", 123};
```

#### クエリ式

[LINQ](https://ja.wikipedia.org/wiki/Language_Integrated_Query "wikilink") をサポートするために、クエリ式が導入された。これは [SQL](../Page/SQL.md "wikilink") の構文に類似しており、最終的に通常のメソッド呼び出しに変換されるものである。以下に例を示す:

``` csharp
var passedStudents =
  from s in students
  where s.MathScore + s.MusicScore + s.EnglishScore > 200
  select s.Name;
```

上のコードは以下のように変換される:

``` csharp
var passedStudents = students
  .Where(s => s.MathScore + s.MusicScore + s.EnglishScore > 200)
  .Select(s => s.Name);
```

C\# 3.0で追加された構文の多くは式であるため、より巨大な式（当然クエリ式も含まれる）の一部として組み込むことができる。旧来複数の文に分けたり、作業用の変数を用意して記述していたコードを単独の式としてより簡潔に記述できる可能性がある。

出井秀行著の『実戦で役立つ C\#プログラミングのイディオム/定石&パターン』（技術評論社、2017年）という書籍ではクエリ構文よりメソッド構文を推奨しており、クエリ構文ではLINQの全ての機能を使用できるわけではないこと、メソッド呼び出しは処理を連続して読める可読性があること、メソッド呼び出しであれば[Microsoft Visual Studioの強力な](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")[インテリセンス](../Page/インテリセンス.md "wikilink")が利用できることを理由に、著者はクエリ構文をほとんど使用していないと記している。

### C\# 4.0からの仕様

#### dynamicキーワード

dynamicキーワードが導入され、[動的型付け](../Page/動的型付け.md "wikilink")変数を定義できるようになった。dynamic型として宣言されたオブジェクトに対する操作のバインドは実行時まで遅延される。

``` csharp
// xはint型と推論される:
var x = 1;
// yはdynamic型として扱われる:
dynamic y = 2;

public dynamic GetValue(dynamic obj)
{
  // objにValueが定義されていなくとも、コンパイルエラーとはならない:
  return obj.Value;
}
```

#### オプション引数・名前付き引数

[VBや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[C++](../Page/C++.md "wikilink")に実装されているオプション引数・名前付き引数が、C\#でも利用できるようになった。

``` csharp
public void MethodA()
{
  // 第1引数と第2引数を指定、第3引数は未指定:
  Console.WriteLine("Ans: " + MethodB(1, 2));  // Ans: 3 … 1 + 2 + 0となっている

  // 第1引数と第3引数を指定、第2引数は未指定:
  Console.WriteLine("Ans: " + MethodB(A: 1, C: 3));  // Ans: 4 … 1 + 0 + 3となっている
}

// 引数が指定されなかった場合のデフォルト値を等号で結ぶ:
public int MethodB(int A = 0, int B = 0, int C = 0)
{
  return A + B + C;
}
```

#### ジェネリクスの共変性・反変性

ジェネリクスの型引数に対してin、out修飾子を指定することにより、ジェネリクスの共変性・反変性を指定できるようになった。

``` csharp
IEnumerable<string> x = new List<string> { "a", "b", "c" };
// IEnumerable<T>インターフェイスは型引数にout修飾子が指定されているため、共変である。
// したがって、C# 4.0では次の行はコンパイルエラーにならない
IEnumerable<object> y = x;
```

### C\# 5.0からの仕様

  - 非同期処理 (await, async)
  - 呼び出し元情報属性
  - foreach の仕様変更

### C\# 6.0からの仕様

  - 自動実装プロパティの初期化子\[8\]
  - get のみの自動実装プロパティおよびコンストラクタ代入

<!-- end list -->

  - 静的 using ディレクティブ
  - インデックス初期化子
  - catch/finally での await
  - 例外フィルタ
  - 式形式のメンバー (expression-bodied members)
  - [null条件演算子](https://ja.wikipedia.org/wiki/null条件演算子 "wikilink")
  - [文字列補間](https://ja.wikipedia.org/wiki/文字列補間 "wikilink")（テンプレート文字列）
  - nameof 演算子
  - \#pragma
  - コレクションの初期化子での拡張メソッド
  - オーバーロード解決の改善

#### 静的 using ディレクティブ

静的 using ディレクティブを利用することで、型名の指定無しに他クラスの静的メンバーの呼び出しを行えるようになった。利用するには`using static`の後に完全修飾なクラス名を指定する。

``` csharp
using static System.Math;
// ↑ソースコードの上部で宣言
class Hogehoge {
    // System.Math.Pow() , System.Math.PI を修飾無しで呼び出す
    double area = Pow(radius, 2) * PI;
}
```

#### 例外フィルタ

`catch`の後に`when`キーワードを使用することで、処理する例外を限定することができるようになった。

``` csharp
try {
    // ...
}
catch (AggregateException ex) when (ex.InnerException is ArgumentException) {
    // ...
}
```

### C\# 7.0からの仕様

  - 出力変数宣言
  - パターンマッチング (is 式/switch 文)
  - タプル (タプル記法/分解/値の破棄)
  - ローカル関数
  - 数値リテラルの改善(桁セパレータ/バイナリリテラル)
  - ref戻り値、ref変数
  - 非同期戻り値型の汎用化
  - Expression-bodied 機能の拡充(コンストラクタ/デストラクタ/get/set/add/remove)
  - Throw 式

#### 出力変数宣言

`out`引数で値を受け取る場合、その場所で変数宣言可能となった\[9\]。

``` csharp
total += int.TryParse("123", out var num) ? num : 0;
```

#### パターンマッチング

##### is 式の拡張

`is`式の構文が拡張され、型の後ろに変数名を宣言できるようになった。 拡張された`is`式はマッチした場合に宣言した変数にキャストした値を代入し、さらに**true**と評価される。 マッチしなかった場合は**false**と評価され、宣言した変数は未初期化状態となる。

``` csharp
void CheckAndSquare(object obj) {
    // objの型チェックと同時にnumに値を代入する。
    if (obj is int num && num >= 0) {
        num = num * num;
    }
    else {
        num = 0;
    }
    // if文の条件セクションは、ifの外側と同じスコープ
    Console.WriteLine(num);
}
```

##### switch 文の拡張

`switch`文のマッチ方法が拡張され、`case`ラベルに従来の「定数パターン」に加え、新たに「型パターン」を指定できるようになった。 また、「型パターン」の`case`ラベルでは、`when`句に条件を指定することができる。 「型パターン」を含む`switch`文では、必ずしも条件が排他的でなくなったため、最初にマッチした`case`ラベルの処理が実行される。\[10\]

``` csharp
void Decide(object obj) {
    switch (obj) {
        case int num when num < 0:
            Console.WriteLine($"{num}は負の数です。");
            break;
        case int num:
            Console.WriteLine($"{num}を二乗すると{num * num}です。");
            break;
        case "B":
            Console.WriteLine($"これはBです。");
            break;
        case string str when str.StartsWith("H"):
            Console.WriteLine($"{str}はHから始まる文字列です。");
            break;
        case string str:
            Console.WriteLine($"{str}は文字列です。");
            break;
        case null:
            Console.WriteLine($"nullです");
            break;
        default:
            Console.WriteLine("判別できませんでした");
            break;
    }
}
```

#### タプル

[タプル](../Page/タプル.md "wikilink")のための軽量な構文が導入された。 従来の`System.Tuple`クラスとは別に、`System.ValueTuple`構造体が新しく追加された。

##### タプル記法

2個以上の要素を持つタプルのための記法が導入された。 引数リストと同様の形式で、タプルを記述できる。

``` csharp
// タプル記法
(int, string) tuple = (123, "Apple");
Console.WriteLine($"{tuple.Item1}個の{tuple.Item2}");
```

##### 分解

多値戻り値を簡単に扱えるように、分解がサポートされた。

``` csharp
var tuple = (123, "Apple");
// 分解
(int quantity, string name) = tuple;
Console.WriteLine($"{quantity}個の{name}");
```

分解はタプルに限らない。`Deconstruct()`メソッドが定義されたクラスでも、分解を利用できる。

以下に、`DateTime`型に分解を導入する例を示す。

``` csharp
static class DateExt {
    public static void Deconstruct(this DateTime dateTime, out int year, out int month, out int day) {
        year = dateTime.Year;
        month = dateTime.Month;
        day = dateTime.Day;
    }
}
```

上記のコードで`DateTime`型に`Deconstruct()`拡張メソッドを定義し、

``` csharp
// 分解
(int year, int month, int day) = DateTime.Now;
```

のように左辺で3つの変数に値を受け取ることができる。

#### 値の破棄

分解、out引数、パターンマッチングで、値の破棄を明示するために`_`が利用できるようになった。 破棄された値は、後で参照することはできない。

``` csharp
// 年と日は使わない
(_, int month, _) = DateTime.Now;

// 解析結果だけ取得し、変換された値は使わない
bool isNumeric = int.TryParse(str, out _);

switch (obj) {
    // string型で分岐するが、値は使わない
    case string _:
        // Do something.
        break;
}
```

#### ref戻り値、ref変数

`ref`キーワードの使用方法が拡張された。これによって、安全な参照の使い道が広がった。

##### ref戻り値

戻り値の型を`ref`で修飾することで、オブジェクトの参照を戻り値とすることができる。

``` csharp
// 二つの参照引数の内、値の大きいものの参照戻り値を返す
static ref int Max(ref int left, ref int right) {
    if (left >= right) {
        return ref left;
    }
    else {
        return ref right;
    }
}
```

変数の寿命は変わらないため、メソッド終了時に破棄されるローカル変数をref戻り値とすることはできない。

``` csharp
static int s_count = 1;

// メンバーの参照はref戻り値になる。
static ref int ReturnMember() {
    return ref s_count;
}
// ref引数はもちろんref戻り値になる。
static ref int ReturnRefParam(ref int something) {
    return ref something;
}
// ローカル変数をref戻り値とすることはできない。
// static ref int ReturnLocal() {
//     int x = 1;
//     return ref x;
// }
```

##### ref変数

ローカル変数の型を`ref`で修飾することで、参照を代入することができる。

``` csharp
// 参照戻り値を参照変数で受け取る
ref int max = ref Max(ref x, ref y);
// limitとmaxは同じ値を参照する
ref int limit = ref max;
```

### C\# 7.1からの仕様

#### 非同期なMainメソッド

Mainメソッドの戻り値として、`Task`型、`Task(int)`型が認められた\[11\]。

``` csharp
static Task Main()
```

``` csharp
static Task<int> Main()
```

#### default式

型推論可能な場面では、`default`の型指定は省略可能となった。

``` csharp
int number = default;
string name = default;
```

### C\# 7.2からの仕様

C\#7.2で追加された仕様は以下の通り。\[12\]\[13\]

#### 値型の参照セマンティクス

値型におけるパフォーマンス向上を意図した複数の機能が追加された。

##### in参照渡し、ref readonly参照戻り値

引数に`in`を指定することで、読み取り専用参照渡しを指定できる。 また、戻り値に`ref readonly`を指定することで、読み取り専用参照戻り値を指定できる。

これにより、構造体のコピーを避けると共に、意図しない値の変更を抑止できる。

##### readonly構造体

構造体宣言時に`readonly`を指定することで、真の読み取り専用構造体を定義できる。 readonly構造体の全てのフィールドは`readonly`でなければならず、`this`ポインタも読み取り専用となる。

これにより、メンバーアクセス時の意図しない防御的コピーを抑止できる。

##### ref構造体

構造体宣言時に`ref`を指定することで、ヒープ領域へのコピーを防ぐ構造体がサポートされる。 ref構造体では、box化できない、配列を作成できない、型引数になることができない、など、ヒープ領域へのコピーを防ぐための厳しい制限がかかる。

この機能は、`Span`<T>のような構造体をサポートするために利用され、unsafe文脈以外での`stackalloc`の利用をも可能とする。

#### 末尾以外の場所での名前付き引数

C\#4.0で追加された[名前付き引数が末尾以外でも利用できるようになった](https://ja.wikipedia.org/wiki/#オプション引数・名前付き引数 "wikilink")。

``` csharp
Hogehoge(name: "John", 17);
```

#### private protected アクセス修飾子

同一アセンブリ内、かつ、継承先からのアクセス許可を表す`private protected`アクセス修飾子が追加された。

#### 数値リテラルの改善

十六進リテラルの`0x`、二進リテラルの`0b`の直後のアンダースコアが認められた。

``` csharp
int bin = 0b_01_01;
int hex = 0x_AB_CD;
```

### C\# 7.3からの仕様

C\#7.3では以下の仕様が追加された。\[14\]

  - ジェネリック型制約の種類の追加
      - `System.Enum`, `System.Delegate`
      - `unmanaged` (文脈キーワード)

<!-- end list -->

``` csharp
unsafe class MyGenericsClass<T1,T2,T3>
    where T1 : System.Enum
    where T2 : System.Delegate
    where T3 : unmanaged {

    public MyGenericsClass(T1 enum1, T1 enum2, T2 func, T3 unmanagedValue) {
        if (enum1.HasFlag(enum2)) {
            func.DynamicInvoke();
        }
        else {
            T3* ptr = &unmanagedValue;
        }
    }
}
```

  - `ref`ローカル変数の再割り当て
  - `stackalloc`初期化子
  - Indexing movable fixed buffers
  - カスタム`fixed`ステートメント
  - オーバーロード解決ルールの改善
  - 出力変数宣言の利用箇所の追加

<!-- end list -->

``` csharp
class MyOutVar {
    // メンバー変数初期化子やコンストラクタ初期化子で出力変数宣言が可能
    readonly int x = int.TryParse("123", out var number) ? number : -1;
}
```

  - タプル同士の比較

<!-- end list -->

``` csharp
(long, long) tuple = (1L, 2L);
// タプルのすべての要素間で == が比較可能
if (tuple == (1, 2)) { }
// 要素数が異なるタプル同士は比較できない。
//if (tuple == (1, 2, 3)) { }
```

  - バッキングフィールドに対するAttribute指定

<!-- end list -->

``` csharp
// C#7.2までは無効な指定(コンパイル自体は可能。無視される)
// C#7.3からはバッキングフィールドに対するAttribute指定と見なされる
[field: NonSerialized]
public int MyProperty { get; set; }
```

### C\# 8.0からの仕様

C\# 8.0で追加された仕様は以下の通り。\[15\]\[16\]

#### null許容参照型

参照型にnull許容性を指定できるようになった。参照型の型名に`?`を付加した場合にnull許容参照型となる。

参照型の型名に`?`を付加しない場合、null非許容参照型となる。

フロー解析レベルでのnull許容性チェックが行われる。null許容値型の`Nullable`<T>のような新しい型は導入されない。

##### null許容コンテキスト

参照型のnull許容性は、null許容コンテキストによって有効、無効の切り替えが可能である。 C\#7.3以前の互換性のために、既定では無効となっている。

  - Nullable コンパイルオプション： プロジェクト全体でのnull許容コンテキストを指定する
  - `#nullable` ディレクティブ： ソースコードの部分ごとにnull許容コンテキストを指定する
      - `annotations` オプション、`warnings`オプションにより、適用範囲を限定できる

##### null免除演算子

null許容参照型の変数名の後に `!`を使用することで、フロー解析時の警告が免除される。

#### インターフェイスの既定メンバー

インターフェイスのメンバーに既定の実装を指定できるようになった。また、インターフェイスに静的メンバーを持つことができるようになった。

さらに、インターフェイスのメンバーにアクセシビリティを指定できるようになった。

  - 既定のアクセシビリティは、従来通り `public` となる。
  - 実装があるインスタンスメンバーは、既定で `virtual` となり `override`可能である。
  - 実装を`override`させないために`sealed`を指定することができる。

#### パターンマッチングの拡張

`switch`式が追加された。 プロパティパターン、タプルパターン、位置指定パターンの追加により、再帰的なパターンマッチングが可能になった。

  - switch式
  - 再帰パターン
      - プロパティパターン
      - タプルパターン
      - 位置指定パターン

#### 非同期ストリーム

`IAsyncEnumerable`<T> インターフェイスを返すことで、イテレータ構文と非同期構文の共存が可能になった。

``` csharp
async IAsyncEnumerable<int> EnumerateAsync() {
    await Task.Delay(100);
    yield return 1;
    await Task.Delay(100);
    yield return 2;
}
```

`await foreach`によって非同期ストリームを列挙する。

``` csharp
async void SpendAsync() {
    await foreach (var item in EnumerateAsync()) {
        Console.WriteLine(item);
    }
}
```

#### 範囲指定

`Index`と`Range`を指定できる専用構文が追加された。

``` csharp
  Index a = 1; // new Index(1, fromEnd: false)
  Index b = ^1; // new Index(1, fromEnd: true)
  Range range = a..b; // new Range(start: a, end: b)
```

#### その他の仕様

  - 静的ローカル関数
  - null結合代入演算子
  - 構造体の読み取り専用メンバー
  - using 宣言
  - ref構造体のDispose
  - ジェネリクスを含むアンマネージ型
  - 式中の`stackalloc`
  - 文字列補間のトークン順序の緩和

## 実装

C\#の言語仕様は標準化団体[Ecma Internationalを通じて公開](https://ja.wikipedia.org/wiki/Ecma_International "wikilink")・標準化されており、第三者がマイクロソフトとは無関係にコンパイラや実行環境を実装することができる\[17\]。 現段階で、C\#コンパイラの実装は次の5つが知られている。

  - マイクロソフト製
      - Visual Studio 2015 以降で使用されている、 (コードネームRoslyn)。[Apacheライセンス](https://ja.wikipedia.org/wiki/Apacheライセンス "wikilink")の[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトで[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")で公開されている\[18\]。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](../Page/Linux.md "wikilink")で動作する。C\#のコンパイラはC\#、VB.NETのコンパイラはVB.NETで実装されている。以前のコンパイラと比べて、リファクタリングやIDE、スクリプティングなどへの利用が可能なAPIが公開されており、コンパイラ以外への様々な応用が可能。
      - Visual Studio 2013 まで使われていた、マイクロソフトによるVisual C\# コンパイラ。
      - 2006年のC\# 2.0当時の、マイクロソフトによる[Shared Source Common Language Infrastructure](http://www.microsoft.com/downloads/details.aspx?FamilyId=8C09FD61-3F26-4555-AE17-3121B4F51D4D&displaylang=en)。共通言語基盤 (CLI) とC\#コンパイラがソースコードで公開されている。
  - [Mono Project](http://www.mono-project.com/)による[Mono内の](../Page/Mono_\(ソフトウェア\).md "wikilink") Mono Compiler Suite (mcs)。
  - 2012年まで開発されていた、[DotGNU Project](http://dotgnu.org/)による[Portable.NET](https://ja.wikipedia.org/wiki/Portable.NET "wikilink")内の the C-Sharp code compiler (cscc)。

## 名称

  - ECMA-334 3rd/4th/5th edition によると、**C\#** は「**C Sharp**」（シーシャープ）と発音し、**LATIN CAPITAL LETTER C (U+0043)** の後に **NUMBER SIGN \# (U+0023)** と書く\[19\]。 音楽の[シャープ](../Page/変化記号.md "wikilink") (♯, MUSIC SHARP SIGN (U+266F)) ではなく[ナンバーサイン](../Page/番号記号.md "wikilink") (\#) を採用したのは、[フォント](../Page/フォント.md "wikilink")や[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")などの技術的な制約に加え、[ASCII](../Page/ASCII.md "wikilink")コードおよび標準的キーボードには前者の記号が存在しないためである。
  - "\#"接尾辞は、他の.NET言語にも使用されており、[J\#](../Page/J_Sharp.md "wikilink")（Javaのマイクロソフトによる実装）、[A\#](https://ja.wikipedia.org/wiki/A_Sharp "wikilink")（[Ada](../Page/Ada.md "wikilink")から）、[F\#](../Page/F_Sharp.md "wikilink")（[System Fなどから](https://ja.wikipedia.org/wiki/System_F "wikilink")\[20\]）が含まれる。また"\#"接尾辞は[Gtk\#](https://ja.wikipedia.org/wiki/Gtk_Sharp "wikilink")（[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")などの[GNOME](../Page/GNOME.md "wikilink")ライブラリの.NETラッパ）、[Cocoa\#](https://ja.wikipedia.org/wiki/Cocoa_Sharp "wikilink")（[Cocoa](../Page/Cocoa.md "wikilink")のラッパ）などのライブラリにも使用されている。そのほか、[SharpDevelop](../Page/SharpDevelop.md "wikilink")などの"Sharp"を冠する関連ソフトウェアも存在する。
  - C\#という名称の解釈として、「（A-Gで表された）直前の音を半音上げる」という音楽記号の役割に着目し、「C言語を改良したもの」を意味したのではないか、。これは、[C++](../Page/C++.md "wikilink")の名称が「C言語を1つ進めたもの」という意味でつけられたことにも似ている。
  - [アンダース・ヘルスバーグ](../Page/アンダース・ヘルスバーグ.md "wikilink")は、「C\#」が「C++++」（すなわち「C++をさらに進めたもの」）にみえるのが由来である、と語っている\[21\]\[22\]。

## 脚注

### 注釈

### 出典

## 関連項目

  - 言語仕様
      -
      - [C\#のデータ型](https://ja.wikipedia.org/wiki/C_Sharpのデータ型 "wikilink")

      - [キーワード (C\#)](https://ja.wikipedia.org/wiki/キーワード_\(C_Sharp\) "wikilink")
  - 実行環境
      - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
      - [.NET Core](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")
      - [Mono](../Page/Mono_\(ソフトウェア\).md "wikilink")
      - [Xamarin](https://ja.wikipedia.org/wiki/Xamarin "wikilink")
  - 開発環境
      - [Visual C\#](../Page/Microsoft_Visual_C_Sharp.md "wikilink")
      - [Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
      - [SharpDevelop](../Page/SharpDevelop.md "wikilink") - フリーの統合開発環境
  - 比較
      - [C♯とJavaの比較](../Page/C_SharpとJavaの比較.md "wikilink")

## 外部リンク

  - [C\#](https://docs.microsoft.com/ja-jp/dotnet/csharp/csharp) - Microsoft Docs
  - 言語仕様
      - [C\# 言語仕様](https://docs.microsoft.com/ja-jp/dotnet/csharp/language-reference/language-specification) - Microsoft Docs

      - [ECMA-334 C\# 言語仕様](https://www.ecma-international.org/publications/standards/Ecma-334.htm)

      -
  - [Mono C\# コンパイラ](https://www.mono-project.com/docs/about-mono/languages/csharp/)

{{.NET}}

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink") [Category:C_Sharp](https://ja.wikipedia.org/wiki/Category:C_Sharp "wikilink")

1.
2.  [Standard ECMA-334-archive](http://www.ecma-international.org/flat/publications/standards/Ecma-334-arch.htm)
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18. [dotnet/roslyn - GitHub](https://github.com/dotnet/roslyn)
19. [Standard ECMA-334 C\# Language Specification](http://www.ecma-international.org/publications/standards/Ecma-334.htm)
20. [The A-Z of programming languages: F\# | Network World](https://www.networkworld.com/article/2271225/software/the-a-z-of-programming-languages--f-.html)
21. [レポート：コミュニティスペシャルセッション with Anders Hejlsberg in Microsoft Developers Conference 2006](http://www.atmarkit.co.jp/fdotnet/insiderseye/20060215cscommunity/cscommunity_01.html)
22. [C\#への期待。アンダースからの返答](http://www.microsoft.com/japan/msdn/community/person/andershejlsberg/communityreport.aspx)