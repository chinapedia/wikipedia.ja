> この記事は[Java Native Interface](https://ja.wikipedia.org/wiki/Java_Native_Interface)から翻訳されています。


**Java Native Interface** (JNI) は、[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")において、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で記述された[プログラムと](../Page/プログラム_\(コンピュータ\).md "wikilink")、他のプログラミング言語（たとえば[Cや](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")など）で書かれた、実際の[CPU](../Page/CPU.md "wikilink")上で動作するコード（[ネイティブコード](../Page/機械語.md "wikilink")）とを連携するための[インタフェース仕様である](../Page/インタフェース_\(情報技術\).md "wikilink")。Java言語からネイティブコードを利用するための[ABIと](../Page/Application_Binary_Interface.md "wikilink")、逆にネイティブコードから[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")を動作させるために[バーチャルマシン](../Page/仮想機械.md "wikilink") (VM) を利用するための[APIの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")2つから成る。

JNIを使うことで、Java言語のVMで動作させるには処理速度の面で不利とされる計算量の多いプログラムを部分的にネイティブコードに置き換えて高速化したり、標準[Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")からはアクセスできない[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")あるいはハードウェアの機能を利用するプログラムを、あたかも通常のJavaクラスのメソッドのように呼び出したりできるようになる。逆に、Javaクラスライブラリによって実装されている高水準の機能を、C/C++などで書かれた下位層から利用することもできるようになる。JNIはJava言語以外の[Java VM上で動作する言語](https://ja.wikipedia.org/wiki/Java_VM "wikilink") (AltJava) からも利用可能である。

JNIによる、Java VMからのネイティブコードの呼び出しは、VMの実行環境の一貫性を保つために、通常のJavaプログラムの実行時とは異なる例外的な[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")管理や[排他制御](../Page/排他制御.md "wikilink")を必要とする場合があり、しばしばプログラムの実行速度の低下を招くことがある。そのため、単純にJNIを利用することで必ずしも[アプリケーション性能を改善できるというわけではない](../Page/アプリケーションソフトウェア.md "wikilink")。また、ネイティブコードを含むバイナリはプロセッサアーキテクチャやオペレーティングシステムに依存してしまうことになるため、Javaのみで記述されたプログラムと比べて再利用や再配布の面で難がある。

## Javaからのネイティブコード呼び出し

以下ではC/C++言語によるネイティブコードの記述例を用いて説明する。なおJNI関連のシンボル定義や関数宣言を含む[ヘッダーファイル](https://ja.wikipedia.org/wiki/ヘッダーファイル "wikilink")は、[Java Development Kit](../Page/Java_Development_Kit.md "wikilink") (JDK) に付属している。

JNIフレームワークでは、ネイティブ関数はC/C++のソースファイル ([拡張子](../Page/拡張子.md "wikilink")は.cもしくは.cppなど) に分離して実装する。Java VMは、`JNIEnv`へのポインタ、コンテキストとしてJavaクラスもしくはクラスインスタンスを間接参照するポインタである`jobject`、そしてJavaメソッドで定義されたすべてのJava引数を通して、ネイティブな関数を起動する。JNI関数は以下のようなC言語形式関数となる。C++のシグネチャは使えない。

``` c
JNIEXPORT void JNICALL
Java_PackageName_ClassName_MethodName
  (JNIEnv *env, jobject obj)
{
    /* ネイティブコードをここに記述する */
}
```

`JNIEnv`はJava VMへのインタフェースを含む構造体`JNINativeInterface`へのポインタである\[1\]。これはJava VMとの相互作用および、Javaオブジェクトとの連携に必要な全ての関数ポインタを含んでいる。JNI関数の例としては、ネイティブ配列とJava配列の相互変換、ネイティブ文字列とJava文字列の相互変換、オブジェクトのインスタンス化、例外の送出などが挙げられる。基本的には、Javaコードでできることは全て`JNIEnv`を用いて行うことができる。

以下の例ではJava文字列をネイティブな文字列に変換し、C/C++の標準ライブラリを利用して[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")に出力する。

``` c
/* C code */
JNIEXPORT void JNICALL
Java_com_example_TestClass_printString
  (JNIEnv *env, jobject obj, jstring javaString)
{
    /* Java 文字列より Modified UTF-8 形式のネイティブ文字列を取得する。 */
    const char *nativeString = (*env)->GetStringUTFChars(env, javaString, NULL);

    printf("%s\n", nativeString);

    /* ネイティブ文字列を解放する。 */
    (*env)->ReleaseStringUTFChars(env, javaString, nativeString);
}
```

``` cpp
// C++ code
extern "C" {
JNIEXPORT void JNICALL
Java_com_example_TestClass_printString
  (JNIEnv *env, jobject obj, jstring javaString)
{
    const char *nativeString = env->GetStringUTFChars(javaString, NULL);

    std::cout << nativeString << std::endl;

    env->ReleaseStringUTFChars(javaString, nativeString);
}
}
```

上記のようにしてCまたはC++で記述した関数が *myjni* ライブラリモジュール\[2\]に実装されていると仮定し、Javaプログラムから呼び出す例を示す。C/C++側の実装関数とJava側のメソッドバインディングは実行時に動的に解決される。

``` java
package com.example;
public class TestClass {
    static {
        System.loadLibrary("myjni");
    }
    public static native printString(String s);
    public static void main(String[] args) {
        printString("Hello, JNI.");
    }
}
```

[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")であるC++に対しては、Cよりも多少洗練されたJNI APIが提供される。C++ではJavaのように、オブジェクトのメソッド（メンバー関数）という概念を持つため、C++のJNIコードはCのそれに比べて文法的に多少簡潔である。

Cでは`env`パラメータは`(*env)->`で被参照され、さらに`env`パラメータはオブジェクトメソッド起動[セマンティクス](https://ja.wikipedia.org/wiki/セマンティクス "wikilink")の一部として、明示的に`JNIEnv`メソッドに渡されなければならない。

C++では`env`パラメータは`env->`で被参照されるが、`env`パラメータはオブジェクトメソッド起動セマンティクスの一部として暗黙的に渡される。

以降のコード例では、断りがない限りC++を前提とするものとする。

## データ型のマッピング

一部のネイティブデータ型とJavaデータ型はそれぞれ相互変換をすることができる。オブジェクトや配列、文字列などの合成型のために、ネイティブコードは`JNIEnv`のメソッド呼び出しにおいて、明示的なデータの変換を行う必要がある。

以下の表ではJavaとネイティブ間のデータ型のマッピングを示す。C/C++の型は\<jni.h\>ヘッダーにて[typedef](https://ja.wikipedia.org/wiki/typedef "wikilink")により定義されたエイリアスであり、実装は処理系依存である\[3\]。

<table>
<thead>
<tr class="header">
<th><p>C/C++データ型</p></th>
<th><p>Javaデータ型</p></th>
<th><p>説明</p></th>
<th><p>型シグネチャ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>jboolean</p></td>
<td><p>boolean</p></td>
<td><p>符号無し8ビット整数型（論理型）</p></td>
<td><p>Z</p></td>
</tr>
<tr class="even">
<td><p>jbyte</p></td>
<td><p>byte</p></td>
<td><p>符号付き8ビット整数型</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>jchar</p></td>
<td><p>char</p></td>
<td><p>符号無し16ビット整数型（文字型）</p></td>
<td><p>C</p></td>
</tr>
<tr class="even">
<td><p>jshort</p></td>
<td><p>short</p></td>
<td><p>符号付き16ビット整数型</p></td>
<td><p>S</p></td>
</tr>
<tr class="odd">
<td><p>jint</p></td>
<td><p>int</p></td>
<td><p>符号付き32ビット整数型</p></td>
<td><p>I</p></td>
</tr>
<tr class="even">
<td><p>jlong</p></td>
<td><p>long</p></td>
<td><p>符号付き64ビット整数型</p></td>
<td><p>J</p></td>
</tr>
<tr class="odd">
<td><p>jfloat</p></td>
<td><p>float</p></td>
<td><p>32ビット<a href="../Page/単精度浮動小数点数.md" title="wikilink">単精度浮動小数点数</a></p></td>
<td><p>F</p></td>
</tr>
<tr class="even">
<td><p>jdouble</p></td>
<td><p>double</p></td>
<td><p>64ビット<a href="../Page/倍精度浮動小数点数.md" title="wikilink">倍精度浮動小数点数</a></p></td>
<td><p>D</p></td>
</tr>
<tr class="odd">
<td><p>void</p></td>
<td><p>void</p></td>
<td></td>
<td><p>V</p></td>
</tr>
<tr class="even">
<td><p>jobject</p></td>
<td><p>Object</p></td>
<td><p>インスタンス</p></td>
<td><p>Ljava/lang/Object;</p></td>
</tr>
<tr class="odd">
<td><p>jstring</p></td>
<td><p>String</p></td>
<td><p>インスタンス</p></td>
<td><p>Ljava/lang/String;</p></td>
</tr>
<tr class="even">
<td><p>jthrowable</p></td>
<td><p>Throwable</p></td>
<td><p>インスタンス</p></td>
<td><p>Ljava/lang/Throwable;</p></td>
</tr>
<tr class="odd">
<td><p>jclass</p></td>
<td><p>Class</p></td>
<td><p>インスタンス</p></td>
<td><p>Ljava/lang/Class;</p></td>
</tr>
</tbody>
</table>

JNIでJavaの型を識別する概念として、「**型シグネチャ**」が定義されている。

"L *fully-qualified-class* ;"というシグネチャは名前によって一意に識別されるJavaクラスを意味する。 例えば文字列`"Ljava/lang/String;"`はクラスを意味する。また、接頭辞`[`はその型の配列を意味する。例えば、`[I`はJavaにおける`int`型の配列すなわち`int[]`に相当する。

表中の対応する型同士は暗黙的に相互変換可能である。実際の変換はJNIレイヤーが担う。プログラマーは型キャスト無しで、Javaの`int`型と同様に`jint`を使用することができる。`jint`型からJavaの`int`型への変換も同様である。

なお、`jstring`はJavaの`String`型への間接参照であり、C/C++のポインタ型`char*`とは無関係である。

``` cpp
// !!! 誤ったコード !!! //
JNIEXPORT void JNICALL
Java_com_example_TestClass_printString
  (JNIEnv *env, jobject obj, jstring javaString)
{
    // 未定義動作を引き起こす。
    printf("%s", javaString);
}
```

``` cpp
// 正しいコード //
JNIEXPORT void JNICALL
Java_com_example_TestClass_printString
  (JNIEnv *env, jobject obj, jstring javaString)
{
    const char *nativeString = env->GetStringUTFChars(javaString, NULL);
    printf("%s", nativeString);
    env->ReleaseStringUTFChars(javaString, nativeString);
}
```

このことはJava配列についても同様である。例えば`jintArray`はJavaの`int[]`型への間接参照であり、C/C++のポインタ型`int*`とは無関係である。

配列の全ての要素の合計を得る例を用いて以下に示す。

``` cpp
// !!! 誤ったコード !!! //
JNIEXPORT jint JNICALL
Java_TestClass_sumIntArray
  (JNIEnv *env, jobject obj, jintArray arr)
{
    int sum = 0;
    const jsize len = env->GetArrayLength(arr);
    for (jsize i = 0; i < len; i++) {
        sum += arr[i];
    }
    return sum;
 }
```

``` cpp
// 正しいコード //
JNIEXPORT jint JNICALL
Java_TestClass_sumIntArray
  (JNIEnv *env, jobject obj, jintArray arr)
{
    jint sum = 0;
    const jsize len = env->GetArrayLength(arr);
    jint *buf = env->GetIntArrayElements(arr, NULL);
    // コピーする場合は GetIntArrayRegion() を用いる方法もある。
    for (jsize i = 0; i < len; i++) {
        sum += buf[i];
    }
    env->ReleaseIntArrayElements(arr, buf, JNI_ABORT);
    return sum;
}
```

Javaの`null`はC/C++の`NULL`ポインタにマッピングされる。

`String`型インスタンスや`Class`型インスタンスなどのJavaオブジェクト参照を`Object`型変数に代入可能であるように、`jstring`や`jclass`などの「JNIオブジェクト参照」もまた`jobject`型変数に代入可能である。

なお、Javaの文字型および文字列型の内部表現は[UTF-16](../Page/UTF-16.md "wikilink")であり、`jstring`に対してGetStringChars()関数を使用することで、UTF-16形式の文字列バッファへのポインタ`jchar*`を得ることができる（ただし[ゼロ終端ではなく](https://ja.wikipedia.org/wiki/ヌル終端文字列 "wikilink")、文字列の長さは別途GetStringLength()関数で取得する）。バッファへのポインタが不要になった場合はReleaseStringChars()関数で解放する必要がある。また、NewString()関数を用いることで、UTF-16バッファから`jstring`を生成することができる。`jchar`はUTF-16を表現できるデータ型であることが保証されるため、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")で追加された`char16_t`など、UTF-16用データ型との相互変換が可能である。

## JNIEnv

JNIのAPI関数の多くはJava VM環境変数として、JNIEnvへのポインタを受け取る。

しかしながら、Javaからnativeメソッドを呼び出す際に、C/C++実装側の関数に引数として渡ってくるJNIEnvは、JNI呼び出しの間のみ有効となる。つまりスタックフレームの[制御フロー](https://ja.wikipedia.org/wiki/制御フロー "wikilink")がJava側に戻ると無効になる。

またJNIEnvは[スレッド間で共有できない](../Page/スレッド_\(コンピュータ\).md "wikilink")。そのため、Java VMに関連付けられていないC/C++スレッド上でJNIEnvを取得するためには、以下のようにAttachCurrentThread()関数を使用してスレッドをVMにアタッチする必要がある。スレッドでJNIEnvが必要なくなったとき、あるいはスレッドを終了する際にDetachCurrentThread()関数を使用してスレッドをVMからデタッチする。

``` cpp
JavaVM *g_vm; // JNI_GetCreatedJavaVMs() を使って取得済みとする。
JNIEnv *env = NULL;
// 現在のスレッドを VM にアタッチする。
g_vm->AttachCurrentThread((void **)&env, NULL);
// 取得した JNIEnv を使って JNI 関数を実行する。
...
// 現在のスレッドを VM からデタッチする。
g_vm->DetachCurrentThread();
```

すでにJava VMに関連付けられているC/C++スレッド上でJNIEnvを取得するためには、GetEnv()関数を呼び出すだけでよい。

``` cpp
JNIEnv *env = NULL;
g_vm->GetEnv((void **)&env, JNI_VERSION_1_6);
```

## Javaクラスへのアクセス

JNIを経由することで、C/C++からJavaの[クラスを利用することもできる](../Page/クラス_\(コンピュータ\).md "wikilink")。

C/C++からJNI関数を用いてJavaクラスをインスタンス化したり、[メソッドを呼び出したり](../Page/メソッド_\(計算機科学\).md "wikilink")、[フィールドを読み書きしたりするためには](../Page/フィールド_\(計算機科学\).md "wikilink")、まずJavaクラス (`jclass`) およびメソッドID (`jmethodID`) あるいはフィールドID (`jfieldID`) を探索・取得する必要があるが、その際に前述の「型シグネチャ」の文字列が識別子として使用される。

以下はクラスの静的フィールドを取得し、静的メソッドを呼び出す例である。

``` cpp
void DoJniTest(JNIEnv *env) {
    jclass jcMath = env->FindClass("java/lang/Math");
    jfieldID jfMathPi = env->GetStaticFieldID(jcMath, "PI", "D"); // static double PI
    jmethodID jmMathMinI = env->GetStaticMethodID(jcMath, "min", "(II)I"); // static int min(int a, int b)
    jmethodID jmMathMaxI = env->GetStaticMethodID(jcMath, "max", "(II)I"); // static int max(int a, int b)
    const jdouble pi = env->GetStaticDoubleField(jcMath, jfMathPi);
    const jint arg1 = 10, arg2 = -7;
    const jint minVal = env->CallStaticIntMethod(jcMath, jmMathMinI, arg1, arg2);
    const jint maxVal = env->CallStaticIntMethod(jcMath, jmMathMaxI, arg1, arg2);
    printf("%f, %d, %d\n", pi, static_cast<int>(minVal), static_cast<int>(maxVal));
    env->DeleteLocalRef(jcMath);
}
```

FindClass()関数で取得した`jclass`はJavaクラスへのJNIオブジェクト参照である。クラス、フィールド、メソッドの型シグネチャをもとに、[リフレクションの要領でC](../Page/リフレクション_\(情報工学\).md "wikilink")/C++からアクセスすることができる。クラス、フィールド、メソッドを繰り返し利用する場合は、探索にかかる時間を節約するためにキャッシュしておく。

## ローカル参照とグローバル参照

特に断りがない限り、JNIのAPI関数が返却するJNIオブジェクト参照は、Javaオブジェクトへの「**ローカル参照**」を表すポインタである。これはJavaの参照型[ローカル変数](../Page/ローカル変数.md "wikilink")に相当する。ローカル参照はスタックフレームの制御フローがJava側に返る際に[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")によって自動的に破棄されるが、DeleteLocalRef()関数を使って手動で削除することもできる\[4\]。

JNIオブジェクト参照を長期間保持する場合は、「**グローバル参照**」を使わなければならない\[5\]\[6\]。

具体的には、C/C++側の静的変数（グローバル変数）などのヒープ領域に`jobject`を格納する場合や、スレッド間で`jobject`を共有する場合に、ローカル参照ではなくグローバル参照を用いる\[7\]。

Javaのスレッドから呼ばれたC関数内でローカル参照を作成した場合、スタックフレームの制御フローがJava側に戻った時点でローカル参照は自動解放される。また、C/C++のスレッド上でローカル参照を作成した場合、スレッドがJVMからデタッチされた時点でローカル参照は自動解放される\[8\]。一方、グローバル参照は自動解放されず、DeleteGlobalRef()関数で明示的に削除する必要がある。

NewGlobalRef()関数を呼び出すことで、ローカル参照からグローバル参照を生成することができる。

グローバル参照はヒープメモリが許す限り自由に作成可能だが、ローカル参照の同時利用可能個数には上限がある。JNI仕様で保証されているのは少なくとも16個ということだけであり、JVMのスタック容量に依存する\[9\]。

JNI参照はJavaのヒープに対する直接のポインタではなく、[メモリコンパクション](https://ja.wikipedia.org/wiki/メモリコンパクション "wikilink")によるJavaオブジェクトのアドレス移動の影響を受けない\[10\]。2つのJNI参照が同じJavaオブジェクトを参照しているかどうかを調べるには、IsSameObject()関数を使用する。

JNIのローカル参照またはグローバル参照が残っている間は、参照先のJavaオブジェクトはGCルートから到達可能であり、ガベージコレクションの対象とはならないため、これらを削除し忘れるとメモリリークしてしまう。

## 脚注

## 関連項目

  - [Foreign function interface](https://ja.wikipedia.org/wiki/Foreign_function_interface "wikilink")
  - [Java Native Access](https://ja.wikipedia.org/wiki/Java_Native_Access "wikilink"): JNI を用いずにネイティブコードを呼び出すためのライブラリ
  - [P/Invoke](https://ja.wikipedia.org/wiki/P/Invoke "wikilink"), [C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink"): [.NET Frameworkにおける](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") JNI と類似の仕組み
  - [SWIG](https://ja.wikipedia.org/wiki/SWIG "wikilink"): 多言語に対応したインターフェイス生成ツールで、C/C++のライブラリ用の JNI コードを生成する

## 外部リンク

  - [Java SE 7 Java Native Interface 関連 API および 開発者ガイド -- Oracle](http://docs.oracle.com/javase/jp/7/technotes/guides/jni/)
  - [Java SE 7 Java Native Interface-related API's and Developer Guides -- Oracle](http://docs.oracle.com/javase/7/docs/technotes/guides/jni/index.html)
  - [Best practices for using the Java Native Interface](http://www.ibm.com/developerworks/java/library/j-jni/index.html)
  - [GNU CNI Tutorial](http://gcc.gnu.org/onlinedocs/gcj/About-CNI.html)
  - [A JNI Tutorial at CodeProject.com (Microsoft specific)](http://www.codeproject.com/java/jnibasics1.asp)
  - [JNI Tutorial at CodeToad.com](http://www.codetoad.com/java_simpleJNI.asp)
  - [JNI in XCode from Apple](http://developer.apple.com/java/jniuniversal.html)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink")

1.  [JNI 関数 - Oracle Java SE Documentation 7](https://docs.oracle.com/javase/jp/7/technotes/guides/jni/spec/functions.html)
2.  [Microsoft Windowsの場合は](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")**\*.dll**ファイル。[UNIX](../Page/UNIX.md "wikilink")/[Linux](../Page/Linux.md "wikilink")の場合は**lib\*.so**ファイル。[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の場合は**lib\*.jnilib**ファイル。
3.  C/C++ではプラットフォームや言語処理系によって組み込み型のサイズが異なる。JNIインターフェイスでは移植性の観点から型エイリアスを使用することが求められる。
4.  [Local and Global References | The Open Journal Project](http://journals.ecs.soton.ac.uk/java/tutorial/native1.1/implementing/refs.html)
5.  [JNI tips | Android NDK | Android Developers](https://developer.android.com/training/articles/perf-jni)*If you want to hold on to a reference for a longer period, you must use a "global" reference.*
6.  [JNI に関するヒント | Android NDK | Android Developers](https://developer.android.com/training/articles/perf-jni?hl=ja)“参照期間を延ばしたい場合は、「グローバル」参照を使用する必要があります。”
7.  [Sun Developer Connection - JDC テクニカル・ティップ 2000年8月1日号](http://otn.oracle.co.jp/technology/global/jp/sdn/java/private/techtips/2000/tt0801.html)
8.  [IBM Knowledge Center - JNI オブジェクト参照の概要](https://www.ibm.com/support/knowledgecenter/ja/SSYKE2_8.0.0/com.ibm.java.vm.80.doc/docs/jni_refs.html)
9.  [Java Native Interface を使用する上でのベスト・プラクティス](https://www.ibm.com/developerworks/jp/java/library/j-jni/index.html)
10. [IBM Knowledge Center - Java Native Interface (JNI)](https://www.ibm.com/support/knowledgecenter/ja/SSYKE2_8.0.0/com.ibm.java.vm.80.doc/docs/jni.html)