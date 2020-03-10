> この記事は[New](https://ja.wikipedia.org/wiki/New)から翻訳されています。


**new**または**New**は、[C++](../Page/C++.md "wikilink")を始めとしたオブジェクト指向プログラミング言語において、[インスタンス](../Page/インスタンス.md "wikilink")を作成する[演算子](../Page/演算子.md "wikilink")である。多くの場合、[ヒープ領域](https://ja.wikipedia.org/wiki/ヒープ領域 "wikilink")からの[動的メモリ確保](https://ja.wikipedia.org/wiki/動的メモリ確保 "wikilink")（動的記憶域確保）を伴う。

new演算子によるインスタンスの作成は、大きく分けて、記憶域を確保することと初期化を行うことに分けられる。記憶域を確保する処理は、多くの場合言語の[処理系](https://ja.wikipedia.org/wiki/処理系 "wikilink")が用意するが、後述するC++のようにプログラム内で独自に定義できるものもある。初期化は、[コンストラクタ](https://ja.wikipedia.org/wiki/コンストラクタ "wikilink")を呼ぶことで行われ、プログラム内で自由に定義できることが一般的である。

## 概要

C++やC++の影響を受けた言語では、概ね次のような構文となっている。

``` cpp
var = new T
```

`var`は、作成されたインスタンスへの参照を保持する[ポインタ型もしくは](../Page/ポインタ_\(プログラミング\).md "wikilink")[参照型の変数である](https://ja.wikipedia.org/wiki/参照_\(情報工学\) "wikilink")。`T`は、作成されるインスタンスの[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")を指定する。`T`がクラス型の場合、`T`のインスタンスを生成するために[デフォルトコンストラクタ](https://ja.wikipedia.org/wiki/デフォルトコンストラクタ "wikilink")が呼ばれる。クラス以外の型を指定可能かどうかは言語による。

次のように、newでインスタンスを生成する際には、初期化子 (initializer) を指定できる。

``` cpp
var = new T(init);
```

`init`は初期化に用いる値を表す。`T`がクラス型の場合、これを引数にしてコンストラクタが呼ばれる。

また、[配列](../Page/配列.md "wikilink")を作成することも可能である。なお、C++では、これを**new\[\]演算子**として、new演算子と区別している。一方、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[C\#では](../Page/C_Sharp.md "wikilink")、new演算子の構文の一種として扱っている。

``` cpp
var = new T[size];
```

`size`は、作成する要素数を指定する。なお、C++やC\#では、次のようにnewした配列に初期化子を与えられる。

``` cpp
var = new T[size] {init1, init2, init3};
```

  - C++では、初期化子リストの要素数よりも`size`が大きい場合、残りの要素はゼロもしくはデフォルトコンストラクタで初期化される。
  - C\#では、初期化子リストの要素数と`size`は同じでなければならないが、初期化子を指定すれば`size`は省略可能である。
  - Javaでは、初期化子を指定する場合は`size`を指定できない。

<!-- end list -->

``` java
var = new T[] {init1, init2, init3};
```

また、JavaやC\#の配列は、常にnew演算子でヒープに作られる存在であり、(2)のような配列変数の初期化は、(1)に対する[糖衣構文](../Page/糖衣構文.md "wikilink")となっている。

``` csharp
T[] var1 = new T[size] {init1, init2, init3}; // (1) new演算子を使用
T[] var2 = {init1, init2, init3}; // (2) 配列初期化の構文を使用、(1)と同じ意味
```

### エラー処理

C++の場合、new演算子で記憶域確保に失敗すると、多くの場合、[例外が投げられる](../Page/例外処理.md "wikilink")。そのため、[C言語](../Page/C言語.md "wikilink")関数の[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")などと違い、newの結果は常に正当なオブジェクトを指し示しているものとして扱うことが可能である。ただし、古いコンパイラでは確保失敗時に[NULLを返すものがあるので注意が必要である](https://ja.wikipedia.org/wiki/null "wikilink")。また、組み込み用途など、コンパイラの設定で例外の使用を不可能にした場合も、確保に失敗したときはNULLが返却される。

C\#およびJavaの場合、new演算子がnullを返すことはなく、必ず例外がスローされる。

## 言語ごとの詳細

### C++

C++のnew演算子とnew\[\]演算子は、まず、同名の演算子関数（[後述](https://ja.wikipedia.org/wiki/#new演算子関数 "wikilink")）で記憶域を確保し、次にコンストラクタを呼んでインスタンスの初期化を行う。C++のnew演算子という名称は、[Simula](../Page/Simula.md "wikilink")の同名の演算子に由来する。

#### deleteとdelete\[\]演算子

C++では、newあるいはnew\[\]で記憶域を動的に確保して生成したインスタンスは、不要になったときにそれぞれdeleteあるいはdelete\[\]演算子で破棄されなければならない。これはC言語においてmalloc関数で確保した領域をfree関数で解放することに相当するが、deleteあるいはdelete\[\]演算子の場合はメモリ解放の前にデストラクタが呼ばれる点が異なる。ヒープ領域に動的に確保されたメモリは自動的に破棄されることはなく、破棄し忘れたままプログラムを続行すると[メモリリーク](../Page/メモリリーク.md "wikilink")となる。多くの場合、明示的な破棄を毎回記述することはプログラマの負担となるため、破棄を[デストラクタ](../Page/デストラクタ.md "wikilink")に任せる[RAII](../Page/RAII.md "wikilink")パターンが利用される。デストラクタを利用することで例外が発生しても確実に破棄することが可能となる（例外安全）。

従来のC++標準ライブラリにはスマートポインタのクラステンプレートとして`std::auto_ptr`が定義されていたが、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")では廃止予定となり、代わって`std::unique_ptr`や`std::shared_ptr`などが定義された。

``` cpp
#include <memory>

class Bar { /* ... */ };

void f()
{
    auto b = std::make_unique<Bar>();
    // make_unique<Bar>は、newとunique_ptrに関する補助的な関数テンプレートである。new Barを行い、結果のポインタをunique_ptr<Bar>に格納して返す。
    // すなわち、上記はstd::unique_ptr<Bar> b(new Bar);に相当する。

    //...

} // 有効範囲（スコープ）から外れるこの位置でbのデストラクタが実行される。unique_ptr<Bar>のデストラクタが、内包するBarオブジェクトのdeleteを行う。
```

動的配列のRAIIとしては、`std::vector`クラステンプレートがよく利用される。

#### new演算子関数

new演算子とnew\[\]演算子での記憶域の確保を制御するために、これらの演算子は[多重定義](https://ja.wikipedia.org/wiki/多重定義 "wikilink")が可能である。そうして定義されたnewおよびnew\[\]演算子関数は、newおよびnew\[\]演算子での記憶域確保に使用される。そして、deleteおよびdelete\[\]演算子の記憶域の解放には、deleteおよびdelete\[\]演算子関数が使用される。

クラス内に設置した場合、そのクラスと派生クラスをnew演算子で作成する際の記憶域の確保に使用される。なおクラス内に置いた場合、staticを指定しなくても、自動的に静的メンバ関数として扱われる (X3014 12.5)。

``` cpp
class hoge
{
public:
    static void* operator new(std::size_t);
    static void* operator new[](std::size_t);
    static void operator delete(void*);
    static void operator delete[](void*);
};
```

`new hoge`という式は次のように実行される。

1.  まず、new演算子関数の[名前探索](https://ja.wikipedia.org/wiki/名前探索 "wikilink")を行う（この例では、`hoge::operator new`が見つかる）。
2.  sizeof (hoge) の値を引数にしてnew演算子関数を呼び、記憶域確保を行う。
3.  new演算子関数が返したポインタの指す位置を[thisポインタとして](https://ja.wikipedia.org/wiki/this_\(プログラミング\) "wikilink")、コンストラクタを呼び、インスタンスを生成する。

new\[\]演算子関数がnew演算子関数と分かれている理由は、『C++の設計と進化』によれば、型Tの配列はTのオブジェクトではないという方針により、Tの配列を確保するためにTのnew演算子関数を使うわけには行かないと考えられたためである。そこで別途new\[\]演算子関数を設けることにしたのである (§10.3)。

なお、new T\[n\]としたとき、new\[\]演算子関数にはsizeof (T) \* nよりも大きい値が引数に渡される可能性がある。これは、主にdelete\[\]で解放するときにデストラクタを呼ぶ回数（配列の要素数）を記録するためなどといった理由によるものである。

また、newとnew\[\]演算子関数は、クラスの外、[名前空間](../Page/名前空間.md "wikilink")内にも定義でき、new及びnew\[\]演算子関数が定義されていないクラスとその他の型では、[名前探索](https://ja.wikipedia.org/wiki/名前探索 "wikilink")を行って記憶域の確保に用いるnewないしnew\[\]演算子関数を決定する。このため、大域名前空間にはデフォルトのnewとnew\[\]演算子関数が定義されており、[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")の中で唯一の大域名前空間で定義された関数となっており、ヘッダ<new>に宣言が置かれている。一方で、この大域名前空間のnew、new\[\]演算子関数はプログラム内で定義を与えることも可能で、そうした場合、処理系の用意した定義に代わってプログラム内の定義が用いられる (X3014 17.4.3.4)。

::new Tのように、new、new\[\]に::を前置すると、大域名前空間のnew、new\[\]演算子関数で記憶域の確保することを強制できる (X3014 5.3.4 9)。この場合、解放には::delete、::delete\[\]を使用する必要がある。

ちなみに、初期のC++では記憶域の確保と初期化が分離しておらず、クラス型に対するnewで独自の記憶域の確保方法を用いるには、コンストラクタ内で、thisへ代入を行うという構文を用いていた (D\&E 3.9)。

##### 既定のnew演算子関数

大域名前空間のnew及びnew\[\]演算子関数がプログラムによって定義されなかった場合に用いられる既定の実装は、次のような動作を行う (X3014 18.4.1.1)。

  - 次の内容のループを行う。
    1.  何らかの方法で記憶域確保を試みる。
          - 成功すればそれを返すことで関数を抜ける。
    2.  失敗した場合、newハンドラが登録されているか確認する。
          - 登録されていたら、そのnewハンドラを呼び出す。
          - newハンドラが登録されていなければ、`std::bad_alloc`型のインスタンスが例外として投げられる。

#### 配置new

配置new (プレースメントnew, placement new) は、new演算子からnew演算子関数へ引数を与えられる機能である。当初、インスタンスを特定の[メモリアドレス](https://ja.wikipedia.org/wiki/メモリアドレス "wikilink")に「配置」するための機能ということで配置newと命名された。後に配置に限らず様々な使い道に応用できることが明らかとなったものの、今でも慣習的に配置newと呼ばれる。

例えばヘッダ<new>には、通常のnew、new\[\]演算子関数のほか、次のようなnew、new\[\]演算子関数が定義されている (X3014 18.4)。

``` cpp
void* operator new(std::size_t, void*) throw();
void* operator new[](std::size_t, void*) throw();
void* operator new(std::size_t, std::nothrow_t) throw();
void* operator new[](std::size_t, std::nothrow_t) throw();
```

上の2つは引数に与えられたポインタをそのままnew演算子関数の戻り値とするもので、当初の配置newの目論見どおり指定したメモリアドレスにオブジェクトを配置するために使用できる。

``` cpp
class Hoge {/* ... */};

void *p = std::malloc(sizeof (Hoge)); // new演算子を使わず、mallocでメモリ領域を確保する
Hoge *obj = new(p) Hoge;

//objを使う

obj->~Hoge();
std::free(p);
```

下の2つは記憶域が確保できなかったときに、例外を投げない代わりに[ヌルポインタ](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")を返すnewである（なお、newハンドラは呼ばれる）。std::nothrow_t型のインスタンスとしてstd::nothrowが定義されており、次のように使用する。

``` cpp
int* p = new(std::nothrow) int;
delete p;
```

deleteおよびdelete\[\]演算子は、std::nothrow_tを引数に取るnewが返す記憶域も解放できると定められている。また、std::nothrow_tを引数に取るものも、そうでない（nothrow_tを引数に取らない配置newでないnew演算子関数）もの同様にプログラム内で定義可能とされている (X3014 18.4.1.1 6)。

newおよびnew\[\]演算子を使用した際、コンストラクタが例外を投げると、コンパイラは引数の対応するdeleteないしdelete\[\]演算子関数で記憶域を解放しようとする。そのため、newおよびnew\[\]演算子で独自の記憶域確保を行う場合、対応するdelete、delete\[\]演算子を用意すべきであるとされる\[1\]。

``` cpp
class MyAllocator;

class Foo
{
    static void* operator new(std::size_t, MyAllocator);
    static void* operator new[](std::size_t, MyAllocator);
    static void operator delete(void*, MyAllocator);
    static void operator delete[](void*, MyAllocator);
};
```

#### エラー処理

newやnew\[\]が記憶域を確保できなかった場合、既定では例外クラス型`std::bad_alloc`（またはその派生クラス）のインスタンスが投げられるが、カスタマイズすることも可能である。

##### newハンドラ

newハンドラは、既定のnewおよびnew\[\]演算子関数で記憶域確保に失敗した場合に呼ばれる[コールバック関数](https://ja.wikipedia.org/wiki/コールバック関数 "wikilink")であり、`std::set_new_handler`関数で登録できる。当時まだ[例外処理](../Page/例外処理.md "wikilink")がなかったC++で、記憶域確保の失敗をまとめて取り扱うために導入された。

newハンドラでは、例外を投げたり、プログラムを終了させたりするなどのほか、何らかの方法で記憶域に空きを作ることで、newおよびnew\[\]演算子関数の記憶域確保を成功へ導かせることも可能である。

### C++/CLI

[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")では、C++のnew演算子のほかに、マネージヒープから記憶域を確保する**gcnew演算子**が存在する。

``` cpp
System::Object^ o = gcnew System::Object;
```

gcnewには、配置構文は存在しない。

また、gcnewにはnew\[\]演算子に相当する配列構文も存在しない。CLI配列（マネージ配列）の作成には、arrayキーワード (cli::array型) を用いる\[2\]\[3\]。

``` cpp
array<int>^ a1 = gcnew array<int>(10); //要素数10の1次元配列
array<int, 2>^ a2 = gcnew array<int, 2>(3, 4); //3×4の2次元配列
```

ただし、gcnewには配列初期化の構文が存在する。

``` cpp
array<int>^ a1 = gcnew array<int>(4) {0, 1, 2, 3};
array<int>^ a2 = gcnew array<int> {0, 1, 2, 3}; //上と同じ。初期化子から要素数が算出される。

array<int, 2>^ a3 = gcnew array<int, 2> {{0, 1}, {2, 3}}; //多次元配列の例
```

### C\#

[C\#のnew演算子は](../Page/C_Sharp.md "wikilink")、インスタンスを生成・初期化するという意味を持っており、参照型を対象とする場合はヒープから記憶域を確保するが、値型（[構造体](../Page/構造体.md "wikilink")や[列挙型](../Page/列挙型.md "wikilink")）を対象とする場合は単に一時的なインスタンス（これはヒープ上に生成されるのではない）を初期化するだけである。

下のコードの場合、少なくとも概念上は、一時的な`int`型のインスタンスが生成され、それが`x`へコピーされているという扱いである。

``` csharp
// intは値型なので、xはスタック上に存在する。
int x = new int();
```

上記は以下と等価である。

``` csharp
int x = 0;
```

### Java

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のnew演算子もC\#と同じくオブジェクトの生成と初期化に利用される。ただしC\#と違ってプリミティブ型の初期化にnew演算子は使えない。

``` java
class Point { int x, y; }
Point pt = new Point();
//int x = new int(); // コンパイル不可。
```

### Visual Basic

[Visual Basicには](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、キーワードNewが存在し、COMのクラスのインスタンス作成に用いる。

``` vb
'MSXML2が参照設定されてあるものとする。
Dim xd As MSXML2.DOMDocument
Set xd = New MSXML2.DOMDocument
```

また、次のように変数の宣言と同時にインスタンスを作成し変数を初期化させることも可能である。

``` vb
Dim xd As New MSXML2.DOMDocument
```

ただし、この2つのコード例は必ずしも同じ意味を持つとは限らない。

### Visual Basic .NET

[Visual Basic .NETのNewは](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")、概ねVisual Basicの構文を踏襲している。しかし、CLIクラスを対象にする点が異なる。

``` vbnet
Dim o1 As System.Object
o1 = New System.Object()

Dim o2 As New System.Object()
```

また、配列の初期化も可能となった。

``` vbnet
Dim a As Integer()
a = New Integer() {0, 1, 2}
```

## 他の手法

オブジェクト指向の言語では、何かしらの方法によりオブジェクトを生成できるようにする必要があるが、その手段が演算子である必然性はない。例えば、C++では、参照やポインタとしてでなく宣言されたオブジェクト型の変数は、暗黙のうちにオブジェクトを生成し、自動的に初期化される。また、[Objective-C](../Page/Objective-C.md "wikilink")や[Ruby](../Page/Ruby.md "wikilink")\[4\]のように、オブジェクトの生成をクラスメソッドにより行う言語もあるほか、オブジェクトの生成を[ファクトリメソッドに落としこんで](../Page/Factory_Method_パターン.md "wikilink")、[継承により上書き可能な形とすることも行われる](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")。

## 参考文献

  - JIS X3014:2003 『プログラム言語C++』
  - (D\&E) 『C++の設計と進化』(2005) [ビャーネ・ストロヴストルップ](../Page/ビャーネ・ストロヴストルップ.md "wikilink")著 επιστημη監修 岩谷宏訳 ソフトバンククリエイティブ ISBN 978-4-7973-2854-7

## 関連項目

  - [delete演算子](https://ja.wikipedia.org/wiki/delete演算子 "wikilink")
  - [malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")
  - [ポインタ](../Page/ポインタ_\(プログラミング\).md "wikilink")
  - [スマートポインタ](https://ja.wikipedia.org/wiki/スマートポインタ "wikilink")
  - [例外処理](../Page/例外処理.md "wikilink")

## 脚注

<references/>

[Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:プログラミング言語の演算子](https://ja.wikipedia.org/wiki/Category:プログラミング言語の演算子 "wikilink")

1.  Effective C++ 原著第3版 52項
2.  [Arrays (C++ Component Extensions)](https://msdn.microsoft.com/en-us/library/ts4c4dw6.aspx)
3.  [Platform, default, and cli Namespaces (C++ Component Extensions)](https://msdn.microsoft.com/en-us/library/d87eee3k.aspx)
4.  [instance method Class\#new](http://docs.ruby-lang.org/ja/1.9.2/method/Class/i/new.html) Ruby 1.9.2 リファレンスマニュアル、2013年11月22日閲覧。