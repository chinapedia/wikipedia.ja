> この記事は[Singleton パターン](https://ja.wikipedia.org/wiki/Singleton_パターン)から翻訳されています。


**Singleton パターン**（シングルトン・パターン）とは、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の[コンピュータプログラムにおける](../Page/プログラム_\(コンピュータ\).md "wikilink")、[デザインパターンの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")1つである。[GoF](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink") (Gang of Four; 4人のギャングたち) によって定義された。Singleton パターンとは、その[クラスの](../Page/クラス_\(コンピュータ\).md "wikilink")[インスタンス](../Page/インスタンス.md "wikilink")が1つしか生成されないことを保証するデザインパターンのことである。[ロケール](https://ja.wikipedia.org/wiki/ロケール "wikilink")や[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")など、絶対にアプリケーション全体で統一しなければならない仕組みの実装に使用される\[1\]。

## クラス図

Singleton パターンの一般的な[クラス図](../Page/クラス図.md "wikilink")を示す。

[center](https://ja.wikipedia.org/wiki/ファイル:Singleton_UML_class_diagram.svg "wikilink")

このクラス図で注目すべきことは以下の3点である。

  - 同じ型のインスタンスが private な[クラス変数](../Page/クラス変数.md "wikilink")として定義されている。
  - [コンストラクタ](../Page/コンストラクタ.md "wikilink")の可視性が private である。
  - 同じ型のインスタンスを返す `getInstance()` が[クラス関数として定義されている](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\)#静的メソッド "wikilink")。

クラス図内にあるアンダーラインは、その項目がクラス変数あるいはクラス関数であることを意味している。

## Javaでの実装例

以下にSingleton パターンを用いた[クラスの](../Page/クラス_\(コンピュータ\).md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")による例を示す。

``` java
final class Singleton {
  private static Singleton instance;
  private Singleton() {}
  public static synchronized Singleton getInstance() {
    if (instance == null) {
      instance = new Singleton();
    }
    return instance;
  }
}
```

この[クラスにおいて](../Page/クラス_\(コンピュータ\).md "wikilink")、[コンストラクタ](../Page/コンストラクタ.md "wikilink")は`private`で定義されているため、他のクラスによって、`Singleton`クラスの[インスタンス](../Page/インスタンス.md "wikilink")を生成することはできない。このクラスのインスタンスを生成したいときは、`getInstance()`[メソッドを利用することになるが](../Page/メソッド_\(計算機科学\).md "wikilink")、このメソッドは最初に呼び出されたときにだけインスタンスを生成し、2回目以降に呼び出されたときは最初に生成したインスタンスを返すように作られている。そのため、プログラム中に`Singleton`クラスのインスタンスが1つしか存在しないことが保証される。

`getInstance()`メソッドが`synchronized`に指定されているのは、複数のスレッドからほぼ同時に呼び出された際に複数のインスタンスが生成されてしまう危険性をなくすためである。

### 問題点および改善策

[Java](https://ja.wikipedia.org/wiki/Java "wikilink") における一般的な Singleton パターンの記述は上述した通りであるが、この方法は同期化コストが高い。そこで*double-checked locking*という[イディオム](https://ja.wikipedia.org/wiki/イディオム "wikilink")\[2\]が考えられたが、「[アウトオブオーダー書き込み](../Page/アウト・オブ・オーダー実行.md "wikilink")」を許す[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")のメモリーモデルが原因で、同期化に失敗する（言うまでもないが、この最適化による副作用は Java だけのものではない）。この問題を克服しようとするとコードが肥大化しコストがかかる。そこで現在では以下のように static フィールドを用いることが推奨されている。

``` java
final class Singleton {
  private static final Singleton instance = new Singleton();
  private Singleton() {}
  public static Singleton getInstance() {
    return Singleton.instance;
  }
}
```

これによりコストは改善される。同期化は行われないが、static フィールドの初期化はそのクラスが呼び出される最初の一回しか行われないため、何回`getInstance()`メソッドを呼んでもスレッドアンセーフを心配する必要はなくなるだけでなく、コストパフォーマンスも非常に高い。

ただしこの場合、Singletonクラスがロードされたときに初期化されるのであって、`getInstance()`が初めて呼ばれたときではない。このことはプログラマーの意図しないタイミングで初期化が始まってしまい混乱の元となる場合がある。 そこで [:en:Initialization-on-demand holder idiom](https://ja.wikipedia.org/wiki/:en:Initialization-on-demand_holder_idiom "wikilink") と呼ばれる手法、すなわちinstanceフィールドのみを別のホルダークラスに隔離して、そのホルダークラスがロードされたときにSingletonの初期化が行なわれるよう改善したものが下記である。

``` java
final class Singleton {
  private Singleton() {}
  private static class SingletonHolder {
    private static final Singleton instance = new Singleton();
  }
  public static Singleton getInstance() {
    return SingletonHolder.instance;
  }
}
```

これでSingletonクラスがロードされたときではなく、`getInstance()`呼び出しによりSingletonHolderクラスがロードされたときにSingletonクラスが初期化される。

### 環境ごとの注意点

上記のSingletonは、Javaクラスのアンロードを考慮していない。Javaでは、参照されなくなったクラスは[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")により回収され、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM) からアンロードされることがありえる。クラスのアンロードにより、そのクラスのstaticフィールドもまた無効となる。つまり、staticフィールドの寿命はアプリケーションの寿命と同一ではなくなる。アンロードされたクラスは再度必要になったときにリロードされ、クラスのstaticイニシャライザも再度呼び出される。こうした一連の動作によりstaticフィールド上のインスタンスは再生成されてしまう。また、各staticフィールドはJVMごとにひとつ存在するのではなく、ロードされたクラスごとにひとつ存在するため、Singletonが破たんするケースもありえる\[3\]。

[Android](../Page/Android.md "wikilink")の[Dalvik](../Page/Dalvik仮想マシン.md "wikilink")/[ART環境上では](https://ja.wikipedia.org/wiki/Android_Runtime "wikilink")、サスペンドされたアプリケーションのActivityは、メモリが足らなくなったときや長時間放置されたときなどに破棄されることがあるが、その際、Activityコンテキストに属するすべての[android.view.View](https://developer.android.com/reference/android/view/View)が無効となり、これらは通例アプリケーション再開時に呼ばれるandroid.app.Activity.onCreate()で再初期化することになる。しかし、クラス自体がアンロードされることも起こりうる\[4\]。アンロードされたクラスはアプリケーションの再開時に必要に応じてリロードされる。

Android環境下でアプリケーションの寿命と同等のstaticフィールドを使用したい場合、独自の[android.app.Application](https://developer.android.com/reference/android/app/Application)派生クラスを定義してAndroidManifest.xmlに記述する。通常はApplicationのサブクラス化は必要なく、たいていのケースでは、（クラスの再初期化が起こりうることに注意してさえいれば）staticシングルトンで同等機能を提供できるとされている\[5\]。

Androidは通例リソースに制限のあるモバイル環境であることもあいまって、オブジェクトのライフサイクルは比較的短く、アプリケーションのサスペンドによりクラスのアンロードが発生しやすくなる。そもそもAndroidの仮想マシンは正式な[Java SE](https://ja.wikipedia.org/wiki/Java_SE "wikilink")/[Java ME仕様に則っていない](https://ja.wikipedia.org/wiki/Java_ME "wikilink")。しかし、たとえ正式な[Java SE](https://ja.wikipedia.org/wiki/Java_SE "wikilink")/[Java EE仕様に則ったデスクトップ環境やサーバー環境であっても](https://ja.wikipedia.org/wiki/Java_EE "wikilink")、クラスのアンロードは起こりうる\[6\]。

このように、SingletonパターンはJavaという言語だけで考えてはならず、実行環境によってもあり方が変わってくるので注意が必要である。Androidのようにフレームワーク内でSingletonを行いたい場合はフレームワーク提供の機構を使うことを検討しなくてはならない。[Java EE](https://ja.wikipedia.org/wiki/Java_EE "wikilink") 6ではアノテーションが導入されている。

## PHP 5.x以降での実装例

バージョン5.0以降の[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink") では、可視性、クラス関数、クラス変数などの機能を備えてより Java に近い仕様となったため、[Javaの例と同じ原理で](https://ja.wikipedia.org/wiki/#例\(Java\) "wikilink") Singleton パターンを実現できる。ソースコードも Java のサンプルコードとほとんど同じものになるため、ここでは省略する。

## C++での実装例

[C++](../Page/C++.md "wikilink")ではクラスのコンストラクタ、コピーコンストラクタとコピー代入演算子を private にすることで唯一となる。さらにデストラクタを private にすることで派生クラスのスタック上への作成を禁止できる。

静的ローカル変数を利用した実装例を示す。

``` cpp
class Singleton {
private:
  Singleton() {} // コンストラクタを private に置く。
  Singleton(const Singleton&); // コピーコンストラクタも private に置き、定義しない。
  Singleton& operator=(const Singleton&); // コピー代入演算子も private に置き、定義しない。
  ~Singleton() {} // デストラクタを private に置く。
public:
  static Singleton& getInstance() {
    static Singleton inst; // private なコンストラクタを呼び出す。
    return inst;
  }

  const char* getString() const {
    return "Hello world!";
  }
};

// 利用例。
int main() {
  std::cout << Singleton::getInstance().getString() << std::endl;
  return 0;
}
```

静的ローカル変数を利用して実装した場合、シングルトンインスタンスを削除するタイミングを明示的に制御できないことに注意が必要となる。また、インスタンスが生成されるのは最初にgetInstance()関数を呼び出したタイミングとなるが、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")よりも前の規格では静的ローカル変数の初期化はスレッドセーフ性が保証されないため、複数のスレッドから同時に初回アクセスが発生した場合、未定義動作を引き起こす。静的ローカル変数ではなく、ポインタ型の静的メンバー変数を利用して実装する場合でも、*double-checked locking*などの技法によるスレッドセーフ化が必要となる。

なお、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")規格では、[コンパイラが生成する関数へのdefault/delete指定により](https://ja.wikipedia.org/wiki/C++11#コンパイラが生成する関数へのdefault/delete指定 "wikilink")、コンストラクタ/デストラクタ以外はprivateに置かなくてもよくなった。また、finalキーワードでクラスを修飾することで、派生クラスの定義を禁止することができる。さらに、静的ローカル変数の初期化は自動的に排他制御され、スレッドセーフとなる\[7\]。

``` cpp
class Singleton final {
private:
  Singleton() = default; // コンストラクタを private に置く。
  ~Singleton() = default; // デストラクタを private に置く。
public:
  Singleton(const Singleton&) = delete; // コピーコンストラクタを delete 指定。
  Singleton& operator=(const Singleton&) = delete; // コピー代入演算子も delete 指定。
  Singleton(Singleton&&) = delete; // ムーブコンストラクタを delete 指定。
  Singleton& operator=(Singleton&&) = delete; // ムーブ代入演算子も delete 指定。

...

};
```

## 特徴

扱い次第では、[グローバル変数](../Page/グローバル変数.md "wikilink")のように機能させることもできる。例えば Java にグローバル変数はないと言われているが、この Singleton パターンで Singleton クラスを作成することで、コード中のどこからでも同一のインスタンスにアクセスすることができる。これはグローバル変数そのものであり、ゆえに Singleton パターンはグローバル変数と同様の問題を引き起こす危険性をはらんでいる。ただし、[パッケージ](../Page/パッケージ_\(Java\).md "wikilink")（[名前空間](../Page/名前空間.md "wikilink")）を指定することにより、インスタンスにアクセス可能なコード範囲を制限し、この問題を回避ないしは軽減することはできる。

また、コードを工夫すればインスタンスの個数制限を設けることもできる。たとえば、上記のサンプルコード中の getInstance() を複数回呼び出したとき、10回目までは毎回新しいインスタンスを生成するが、11回目以降は以前のインスタンスを再利用する、といったような機構である。これは単なるグローバル変数で実現することはできない利点である。

## Multiton パターン

[Multiton.svg](https://ja.wikipedia.org/wiki/File:Multiton.svg "fig:Multiton.svg") Singletonパターンを拡張したデザインパターンとして[{{langと呼ばれるものがある](https://ja.wikipedia.org/wiki/:en:Multiton_pattern "wikilink")。これはSingletonで生成されるインスタンスを[連想配列](../Page/連想配列.md "wikilink")で複数保持する。ただしMultiton パターンは[ユニットテスト](https://ja.wikipedia.org/wiki/ユニットテスト "wikilink")を難しくし\[8\]、ガーベジコレクションのある言語ではオブジェクトへの強い参照によりメモリリークを起こす恐れがあることも念頭に置く必要がある。

### Javaでの例

``` Java
public class FooMultiton {
    private static final Map<Object, FooMultiton> instances = new HashMap<Object, FooMultiton>();

    private FooMultiton() {
        // no explicit implementation
    }

    public static synchronized FooMultiton getInstance(Object key) {

        // Our "per key" singleton
        FooMultiton instance = instances.get(key);

        if (instance == null) {
            // Lazily create instance
            instance = new FooMultiton();

            // Add it to map
            instances.put(key, instance);
        }

        return instance;
    }

    // other fields and methods ...
}
```

## 脚注

<references/>

## 関連項目

  - [デザインパターン](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - [クリティカルセクション](../Page/クリティカルセクション.md "wikilink")
  - [排他制御](../Page/排他制御.md "wikilink")
  - [マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")
  - [グローバル変数](../Page/グローバル変数.md "wikilink")

[Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")

1.  [エリック・ガンマ](../Page/エーリヒ・ガンマ.md "wikilink")、[ラルフ・ジョンソン](https://ja.wikipedia.org/wiki/ラルフ・ジョンソン "wikilink")、[リチャード・ヘルム](https://ja.wikipedia.org/wiki/リチャード・ヘルム "wikilink")、[ジョン・ブリシディース](../Page/ジョン・ブリシディース.md "wikilink")（著）、[グラディ・ブーチ](../Page/グラディ・ブーチ.md "wikilink")（まえがき）、本位田真一、吉田和樹（監訳）、『オブジェクト指向における再利用のためのデザインパターン』、[ソフトバンクパブリッシング](https://ja.wikipedia.org/wiki/ソフトバンクパブリッシング "wikilink")、1995。ISBN 978-4-7973-1112-9.
2.  [double-checked lockingとSingletonパターン この破綻したプログラミング・イディオムを多角的に検討する](http://www.ibm.com/developerworks/jp/java/library/j-dcl/)
3.  [クラスローダーとJ2EEパッケージング戦略を理解する: 第2回「クラスローダーを理解する - シングルトンがシングルトンでなくなる日」](https://www.ibm.com/developerworks/jp/websphere/library/java/j2ee_classloader/2.html)
4.  [JNI tips | Android NDK | Android Developers](https://developer.android.com/training/articles/perf-jni)*"Classes are only unloaded if all classes associated with a ClassLoader can be garbage collected, which is rare but will not be impossible in Android."*
5.  [Application | Android Developers](https://developer.android.com/reference/android/app/Application)*"There is normally no need to subclass Application. In most situations, static singletons can provide the same functionality in a more modular way."*
6.  [Java のクラスアンロード (Class Unloading)](http://www.nminoru.jp/~nminoru/java/class_unloading.html)
7.  [ブロックスコープを持つstatic変数初期化のスレッドセーフ化 - cpprefjp C++日本語リファレンス](https://cpprefjp.github.io/lang/cpp11/static_initialization_thread_safely.html)
8.  [Google Testing Blog: Clean Code Talks - Global State and Singletons](https://testing.googleblog.com/2008/11/clean-code-talks-global-state-and.html)