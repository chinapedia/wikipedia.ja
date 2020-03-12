> この記事は[RAII](https://ja.wikipedia.org/wiki/RAII)から翻訳されています。


**RAII**（）は、日本語では「**リソース取得は初期化である**」「**リソースの確保は初期化時に**」「**リソースの取得と初期化**」などの意味を持ち、資源（[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")）の確保と解放を、[クラス型の変数の初期化と破棄処理に結び付けるというプログラミングのテクニックである](../Page/クラス_\(コンピュータ\).md "wikilink")。特に[C++](../Page/C++.md "wikilink")と[D言語](../Page/D言語.md "wikilink")で一般的であり、[デストラクタ](../Page/デストラクタ.md "wikilink")をサポートしない[C言語](../Page/C言語.md "wikilink")などに対する優位性や利便性のうちのひとつとなっている。

RAIIでは、資源の取得をクラス型変数の構築（初期化）時に、また返却を破壊時に行う。特にプログラムの制御フローが自動変数の属する[ブロックを抜けるとき](../Page/ブロック_\(プログラミング\).md "wikilink")、その変数の[デストラクタ](../Page/デストラクタ.md "wikilink")が自動的に呼ばれるため、デストラクタを適切に記述したクラス型変数の寿命が終わるとすぐに資源が返却されることが保証できるようになる。これは[例外が発生したときでも同様であるため](../Page/例外処理.md "wikilink")、RAIIは[例外安全](https://ja.wikipedia.org/wiki/例外安全 "wikilink")なコードを書くための鍵となる概念となった (Sutter 1999)。

## 典型的な用法

RAIIの最も基本的な活用例は、[動的確保されたメモリを自動解放するスマートポインタ](../Page/動的メモリ確保.md "wikilink") (smart pointer) である。C++において[new演算子](https://ja.wikipedia.org/wiki/new演算子 "wikilink")（またはnew\[\]演算子）で動的に確保されたメモリは、不要になったときにその領域を指すポインタを経由してdelete演算子（またはdelete\[\]演算子）で明示的に解放しなければならない。もし解放忘れがあると[メモリリーク](../Page/メモリリーク.md "wikilink")につながるが、解放忘れがないように細心の注意を払って、コードパスに手動でひとつひとつ削除処理を記述していくことは非常に手間がかかる。一方、C++ではオブジェクトを[スタック](../Page/スタック.md "wikilink")に割り当てることも可能であり、動的確保されたメモリを指すポインタをラップするスマートポインタクラスのオブジェクトをスタックに割り当て、ラッパーオブジェクトの寿命が尽きた時点で自動的に呼び出されるデストラクタを利用することにより、動的確保されたメモリの解放を明示的に逐一記述することなく、暗黙的かつ確実に実行させることができる。[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")における動的[配列](../Page/配列.md "wikilink")クラステンプレートの`std::vector`なども、プログラマが明示的にnew\[\]およびdelete\[\]を呼び出す必要のないRAIIクラスの一種である。

RAIIはファイル操作にも用いられる。C言語ではファイルアクセスの際、`fopen()`関数により取得した`FILE`オブジェクトを明示的に`fclose()`関数で解放することでファイルを閉じる必要があったが、[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")の[ファイルストリームでは](../Page/ストリーム_\(プログラミング\).md "wikilink")、オブジェクトの[コンストラクタ](../Page/コンストラクタ.md "wikilink")でファイルストリームを開き、[デストラクタ](../Page/デストラクタ.md "wikilink")で閉じることで、ファイルハンドルの管理を自動化し、リソースリークを防ぐことができる。このようなファイルアクセスの管理に限らず、C++のデストラクタ機構はあらゆるリソースの寿命管理に活用できる。ほかには、[マルチスレッドアプリケーションにおいて](../Page/スレッド_\(コンピュータ\).md "wikilink")[クリティカルセクション](../Page/クリティカルセクション.md "wikilink")の[ロックの管理にもよく用いられる](../Page/ロック_\(情報工学\).md "wikilink")。C++03規格以前においても、[Boost C++ライブラリや](../Page/Boost_C++ライブラリ.md "wikilink")[Microsoft Foundation Classライブラリなどにクリティカルセクション管理用のRAIIクラスが用意されていたが](../Page/Microsoft_Foundation_Class.md "wikilink")、[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")規格でスレッドおよび同期オブジェクトが標準化された際に、類似のRAIIクラスが`std::lock_guard`および`std::unique_lock`として導入された。

また、動的に確保されたメモリの[所有権](../Page/所有権.md "wikilink")もRAIIで管理できる。所有権が唯一となるスマートポインタクラステンプレートとして、C++03までの[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")では`std::auto_ptr`が用意されていたが、C++11以降では非推奨となり、代替の`std::unique_ptr`が用意されている。[Boost C++ライブラリには類似のクラステンプレートとして](../Page/Boost_C++ライブラリ.md "wikilink")`boost::scoped_ptr`や`boost::interprocess::unique_ptr`が実装されている。また、[参照カウント](../Page/参照カウント.md "wikilink")方式で所有権を共有するオブジェクトのスマートポインタクラステンプレートとして、[Boost C++ライブラリの](../Page/Boost_C++ライブラリ.md "wikilink")`boost::shared_ptr`がある。これは[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")にて`std::shared_ptr`として標準化された。`shared_ptr`とともに利用する[弱参照](https://ja.wikipedia.org/wiki/弱参照 "wikilink")スマートポインタとして、それぞれ`boost::weak_ptr`および`std::weak_ptr`が存在する。そのほか、侵入型参照カウント方式の`boost::intrusive_ptr`、の[ポリシー](https://ja.wikipedia.org/wiki/ポリシー "wikilink")ベースの`Loki::SmartPtr` 、[COMインターフェイスオブジェクト](../Page/Component_Object_Model.md "wikilink") ([`IUnknown`](https://ja.wikipedia.org/wiki/IUnknown "wikilink")) の参照カウント管理に特化した[ATLの](../Page/Active_Template_Library.md "wikilink")`ATL::CComPtr`などがある。

後の例のようにRAIIは[例外安全](https://ja.wikipedia.org/wiki/例外安全 "wikilink")の達成にも活用される。RAIIを使えばあちこちに`try`-`catch`ブロックを記述することなく[メモリリーク](../Page/メモリリーク.md "wikilink")やリソースリークを防げる。

## C++での例

以下、特に断りがない限り、C++03以前でもC++11以降でもコンパイルできるコードで例示する。

### 動的確保されたメモリの管理

単純な例として、[関数内で一時的な作業領域として](../Page/サブルーチン.md "wikilink")[配列](../Page/配列.md "wikilink")を動的確保することを考える\[1\]。単純な方法では、以下のようにnew\[\]演算子を使用する。

``` cpp
void function1A(size_t count) {
    double* array1 = NULL;
    double* array2 = NULL;
    try {
        // 配列を動的に確保する。メモリ確保失敗により std::bad_alloc 例外がスローされる可能性がある。
        array1 = new double[count]();
        array2 = new double[count]();

        // 動的に確保した配列をここで作業領域として使用する。
        for (size_t i = 0; i < count; ++i) {
            array1[i] = i * 0.1;
            array2[i] = i * 0.1;
        }
        // ...

        // 配列を使わなくなったので削除する。
        delete[] array2;
        delete[] array1;
    }
    catch (...) {
        // 例外がスローされる場合に備える。
        delete[] array2;
        delete[] array1;
        throw; // 例外の再送出。
    }
}
```

これはC言語の[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")およびfree関数による原始的な寿命管理手法に近い。もし動的に確保したメモリを削除する前に関数を抜けると[メモリリーク](../Page/メモリリーク.md "wikilink")してしまうため、慎重に削除処理をひとつひとつ記述していく必要がある。動的にメモリ管理するオブジェクトの数が増えるにつれ、ソースコードのメンテナンスコストは増大していく。

一方、RAIIを利用した場合は以下のようになる。

``` cpp
// RAII を実現する配列ラッパークラス。
template<typename T> class ArrayWrapper {
    size_t m_count;
    T* m_data;
public:
    ArrayWrapper() : m_count(), m_data() {}
    explicit ArrayWrapper(size_t count) : m_count(count), m_data(new T[count]()) {}
    ~ArrayWrapper() { delete[] m_data; }
    size_t count() const { return m_count; }
    T* data() { return m_data; }
    const T* data() const { return m_data; }
    T& operator[](size_t index) { return m_data[index]; }
    const T& operator[](size_t index) const { return m_data[index]; }
    // コピーは禁止とする。所有権の移動もサポートしない。
private:
    ArrayWrapper(const ArrayWrapper&);
    ArrayWrapper& operator=(const ArrayWrapper&);
};

void function1B(size_t count) {
    ArrayWrapper<double> array1(count);
    ArrayWrapper<double> array2(count);

    // 動的に確保した配列をここで作業領域として使用する。
    for (size_t i = 0; i < count; ++i) {
        array1[i] = i * 0.1;
        array2[i] = i * 0.1;
    }
    // ...

} // RAII 変数 array1, array2 の属するブロックを抜ける。このとき array2, array1 の各デストラクタが順に呼ばれ、それぞれが内部で管理する配列メモリ領域は自動的に破棄される。
```

[Boost C++ライブラリの](../Page/Boost_C++ライブラリ.md "wikilink")`boost::scoped_array`を使う場合は以下のように書ける。

``` cpp
#include <boost/scoped_array.hpp>

void function1C(size_t count) {
    boost::scoped_array<double> array1(new double[count]());
    boost::scoped_array<double> array2(new double[count]());

    for (size_t i = 0; i < count; ++i) {
        array1[i] = i * 0.1;
        array2[i] = i * 0.1;
    }
}
```

[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")以降の`std::unique_ptr`を使う場合は以下のように書ける。

``` cpp
#include <memory>

void function1D(size_t count) {
    std::unique_ptr<double[]> array1(new double[count]());
    std::unique_ptr<double[]> array2(new double[count]());

    for (size_t i = 0; i < count; ++i) {
        array1[i] = i * 0.1;
        array2[i] = i * 0.1;
    }
}
```

RAIIを使ってメモリ管理する場合、明示的な削除処理の記述が必要なくなり、コードの見通しやメンテナンス性が向上する。関数の途中でreturnしたり、例外がスローされたりする場合でも、後始末を自動的に実行してくれる。また、C++のテンプレートを利用することで、任意の型に対するRAIIを実現するラッパークラスを定義することができる。C++の標準テンプレートライブラリ ([STL](../Page/Standard_Template_Library.md "wikilink")) には、RAIIの概念をもとに実装された汎用的な動的配列のクラステンプレートとして、`std::vector`が用意されている。

### ファイルハンドルの管理

別の例として、ファイルのオープンとクローズを挙げる。従来の[標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")を使って、直接リソースを管理する書き方だと以下のようになる。

``` cpp
#include <cstdio>
#include <cassert>
#include <stdexcept>

FILE* openFile(const char* fileName, const char* mode) {
    FILE* fp = std::fopen(fileName, mode);
    if (!fp) {
        throw std::runtime_error("Failed to open file!");
    }
    return fp;
}

void writeLine(FILE* fp, const char* strLine) {
    assert(fp);
    const int ret = std::fprintf(fp, "%s\n", strLine);
    if (ret < 0) {
        throw std::runtime_error("Failed to write data on file!");
    }
}

void function2A() {
    FILE* fp1 = NULL;
    FILE* fp2 = NULL;
    try {
        fp1 = openFile("test1.txt", "a");
        fp2 = openFile("test2.txt", "a");
        // ファイルの書き込みを行なう。
        writeLine(fp1, "Test line for file#1.");
        writeLine(fp2, "Test line for file#2.");
        // ファイルを使い続ける。
        // 何か問題が起こって関数を抜ける場合、return の前に fclose() を忘れずに呼ばなければならない。

        // 明示的にファイルを閉じる必要がある。
        std::fclose(fp1);
        std::fclose(fp2);
    }
    catch (...) {
        // 獲得したリソースがあれば返却する。
        if (fp1) {
            std::fclose(fp1);
        }
        if (fp2) {
            std::fclose(fp2);
        }
        throw; // 例外の再送出。
    }
}
```

一方、RAIIを利用した場合は以下のようになる。

``` cpp
class FileWrapper {
    FILE* m_fp;
public:
    FileWrapper(const char* fileName, const char* mode)
        : m_fp(std::fopen(fileName, mode)) { // ファイルハンドルでデータメンバーを初期化。
        if (!m_fp) {
            throw std::runtime_error("Failed to open file!");
        }
    }
    ~FileWrapper() {
        assert(m_fp);
        std::fclose(m_fp);
    }
    void writeLine(const char* strLine) {
        assert(m_fp);
        const int ret = std::fprintf(m_fp, "%s\n", strLine);
        if (ret < 0) {
            throw std::runtime_error("Failed to write data on file!");
        }
    }
    // コピーは禁止とする。所有権の移動もサポートしない。
private:
    FileWrapper(const FileWrapper&);
    FileWrapper& operator=(const FileWrapper&);
};

void function2B() {
    FileWrapper file1("test1.txt", "a");
    file1.writeLine("Test line for file#1.");
    FileWrapper file2("test2.txt", "a");
    file2.writeLine("Test line for file#2.");
} // 関数の途中で return したり、例外がスローされたりしても、RAII 変数の属するブロックを抜けた時点で確実にファイルハンドルは閉じられる。
```

標準C++ライブラリでは、抽象化されたファイルストリーム管理用のRAIIクラスとして、`std::basic_fstream`が用意されている。

`FileWrapper`クラスでは`FILE*`をカプセル化したが、RAIIの真髄は有限の資源ならば何でも同様に管理できることにある。そしてRAIIでは、関数（やその他ブロック）を抜けるときに適切に資源が破棄されることが保証される。なお、`FileWrapper`クラスのコンストラクタはファイルが開けなければ例外を投げるため、インスタンスが生成されていれば内包するファイルハンドルは常に利用可能であると仮定してよい。

RAIIを使わない場合、例外が発生するとある問題が生じる。複数の資源を確保する際、それぞれの確保の間に例外が投げられたら、`catch`ブロックではどれを解放すべきか分からなくなってしまう（通常、確保されていない資源を解放することはできない）。`function1A`や`function2A`のように、初期値を無効と見なすことにして二段階初期化したり、`try`-`catch`ブロックを重ねていったりするなど、状況に応じてコードを適切に書いていかなければ安全性は得られない。`function1B`や`function2B`のようなRAIIならばこれにも対処できる。変数（メンバ変数も含む）が構築されたときとは逆順で破棄され、また完全に構築された（内部で例外が投げられずにコンストラクタが実行された）オブジェクトのみが破棄されるので問題は起こらない。これはプログラムが資源（またはそれに類するもの）の管理から逃れることができるようになったということである。RAIIクラスを定義する手間はかかるが、いくつもの関数でRAIIクラスを使っていれば、[コードの再利用](https://ja.wikipedia.org/wiki/コードの再利用 "wikilink")により全体的にはコードが単純化し、良いプログラムにする手助けとなる。また、副次効果としてビジネスロジックの記述に集中することができるようになる。

なお、`function1A`や`function2A`は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のようなRAIIでない言語での資源管理に使われるイディオムに似ている。Javaの`try`-`finally`ブロックは資源の確実な返却を実行するポイントを提供するが、都度`try`-`finally`ブロックで適切に破棄処理を書かなければならず、プログラマに負担がかかる。

## 広義のスマートポインタの活用

スマートポインタと呼ばれる類のクラスを使い、RAIIを任意のリソース管理APIへ適用することも可能である。

なお、この節では広い意味でスマートポインタという言葉を使っている。一般的にはメモリに特化したものをスマートポインタと言う。

例えば、`stlsoft::scoped_handle`\[2\]は、（`void`を含む）任意の型の解放関数を受け付け、また`0`でない広義の「[ヌル](https://ja.wikipedia.org/wiki/Null "wikilink")」値（無効値）も受け付ける（[Windowsのように複数の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[呼出規約](https://ja.wikipedia.org/wiki/呼出規約 "wikilink")が用いられる環境では、どんなものでも受け付ける）。

以下は[Windows APIのファイル入出力関数および](../Page/Windows_API.md "wikilink")[Winsock](../Page/Winsock.md "wikilink") API関数のリソースをRAIIでラップした例である。`CreateFile()`関数\[3\]が返す無効値`INVALID_HANDLE_VALUE`および`WSASocket()`関数\[4\]が返す無効値`INVALID_SOCKET`は、[Windows SDK](https://ja.wikipedia.org/wiki/Windows_SDK "wikilink") 8.1ではそれぞれ以下のように定義されている。

``` c
#define INVALID_HANDLE_VALUE  ((HANDLE)((LONG_PTR)-1))
```

``` c
#define INVALID_SOCKET  (SOCKET)(~0)
```

RAIIは特に複数のリソースを同時に管理する場合に効果を発揮する。少なくとも`try-catch`節がいくつも現れて混乱する事態からは逃れられる。

``` cpp
#include <WinSock2.h>
#include <cstdlib>
#include <cassert>
#include <cstring>
#include <stdexcept>
#include <iostream>
#include <stlsoft/smartptr/scoped_handle.hpp>

// 3つの資源を同時に使う。
void testScopedHandle() {
    // ファイルを開く。
    // CreateFile() は失敗した場合 INVALID_HANDLE_VALUE を返す。ただし NULL もまた HANDLE としては一般的に無効値。
    HANDLE hFile = ::CreateFileW(L"test.txt", GENERIC_WRITE, FILE_SHARE_READ, NULL, OPEN_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);
    if (hFile == NULL || hFile == INVALID_HANDLE_VALUE) {
        throw std::runtime_error("Failed to create file handle!");
    }
    else {
        stlsoft::scoped_handle<HANDLE> cleanupFile(hFile, ::CloseHandle, INVALID_HANDLE_VALUE); // ファイルが確実に閉じられるようにする。

        // TCP ソケットを作成。
        // BSD ソケット API における socket() 関数の戻り値は int で、異常値は負数 (-1) となっており、0 は正常値のひとつ。
        // Winsock もそれを踏襲している。
        SOCKET socketDesc = ::WSASocketW(AF_INET, SOCK_STREAM, IPPROTO_TCP, NULL, 0, 0);
        if (socketDesc == INVALID_SOCKET) {
            throw std::runtime_error("Failed to create socket descriptor!");
        }
        else {
            stlsoft::scoped_handle<SOCKET> cleanupSocket(socketDesc, ::closesocket, INVALID_SOCKET); // ソケットが確実に閉じられるようにする。

            void *mem = std::malloc(10000);
            if (!mem) {
                throw std::bad_alloc();
            }
            else {
                stlsoft::scoped_handle<void*> cleanupMem(mem, std::free); // メモリが確実に解放されるようにする。

                // ここでメモリとソケットとファイルを使う。

                const LARGE_INTEGER dummy = {};
                if (!SetFilePointerEx(cleanupFile.get(), dummy, NULL, FILE_END)) {
                    throw std::runtime_error("Failed to set file pointer to end!");
                }

                const char* text = "Test line.\r\n";
                const DWORD numOfBytesToWrite = static_cast<DWORD>(std::strlen(text));
                DWORD numOfBytesWritten = 0;
                if (!::WriteFile(cleanupFile.get(), text, numOfBytesToWrite, &numOfBytesWritten, NULL) || numOfBytesWritten != numOfBytesToWrite) {
                    throw std::runtime_error("Failed to write data on file!");
                }

                // ...

            } // mem はここで解放される。
            mem = NULL;

            // ソケットを自動的な管理から切り離す。
            //SOCKET detachedVal = cleanupSocket.detach();
            //assert(detachedVal == socketDesc);

        } // socketDesc を RAII から切り離した場合、ここでは閉じられない。

        //const int ecode = ::closesocket(socketDesc);
        socketDesc = INVALID_SOCKET;

        // 早期に hFile の資源を返却することもできる。
        //cleanupFile.close();

    } // hFile の資源を早期に返却した場合、ここでは返却されない。
    hFile = INVALID_HANDLE_VALUE;
}

int main() {
    WSADATA wsaData = {};
    const int ecode = ::WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (ecode == 0) {
        try {
            testScopedHandle();
        }
        catch (const std::exception& ex) {
            std::cout << ex.what() << std::endl;
        }
        ::WSACleanup();
    }
}
```

### 制約

RAIIクラスでは解放関数が失敗すると問題になる。C++では言語の制約上デストラクタから例外を投げるのは良い考えではないため、デストラクタではすべての例外を握りつぶす必要がある。エラーコードによる通知も難しくなるため、結果として解放失敗の原因を上位層に通知することが難しくなる。そのため`stlsoft::scoped_handle`のようなクラスは、次のどちらかに当てはまるときには使うべきではない。

1.  解放関数が失敗する可能性のある場合
2.  利用者がその失敗を知るべき場合

## クロージャとRAII

[Ruby](../Page/Ruby.md "wikilink")と[Smalltalk](../Page/Smalltalk.md "wikilink")は特別なスコープに関連付けられた変数の中にある[クロージャ](../Page/クロージャ.md "wikilink")ブロックという形でRAIIに対応している。以下はRubyの例である。

``` ruby
File.open("data.txt") { |file|
    # ファイルの内容を標準出力へ
    print file.read
}
# 変数'file'はもう存在しない。ファイルハンドルは閉じられた。
```

## RAIIに類似した制御構造

[C\#と](../Page/C_Sharp.md "wikilink")[VB .NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink") 2005はC++デストラクタに代わる`System.IDisposable`インターフェイスを実装するクラスと`using`文を使ってRAIIに似た機能を実現している。

[Python](../Page/Python.md "wikilink") 2.5に追加された`with`ステートメントでは、同様の目的に`__entry__`と`__exit__`のメソッドを使う。

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")はバージョン7で導入されたtry-with-resources文により、C\#のusing文に近い機能を提供する。

## 脚注

## 参考文献

  - Sutter, Herb (1999). Exceptional C++. Addison-Wesley. ISBN 978-0-201-61562-3.
      - 日本語訳 ハーブ・サッター　『Exceptional C++』　浜田真理、ピアソンエデュケーション、2000年、249頁。ISBN 978-4-89471-270-6

## 外部リンク

  - Article "[The RAII Programming Idiom](http://www.hackcraft.net/raii/)" by [Wikipedia editor](https://ja.wikipedia.org/wiki/Wikipedia_editor "wikilink") Jon Hanna (Talliesin)
  - Wiki ["Resource Acquisition Is Initialization" from the Portland Pattern Repository](http://c2.com/cgi/wiki?ResourceAcquisitionIsInitialization)
  - Sample Chapter "[Gotcha \#67: Failure to Employ Resource Acquisition Is Initialization](http://awprofessional.com/articles/article.asp?p=30642&seqNum=8)" by Stephen Dewhurst
  - Article "[A Conversation with Bjarne Stroustrup](http://artima.com/intv/modern3.html)" by Bill Venners
  - Article "[The Law of The Big Two](http://artima.com/cppsource/bigtwo3.html)" by Bjorn Karlsson and [Matthew Wilson](https://ja.wikipedia.org/wiki/Matthew_Wilson "wikilink")
  - [RAII in C++](http://jrdodds.blogs.com/blog/2004/08/raii_in_c.html) by Jonathan Dodds
  - Article "[Implementing the 'Resource Acquisition is Initialization' Idiom](http://gethelp.devx.com/techtips/cpp_pro/10min/2001/november/10min1101.asp)" by Danny Kalev
  - Article "[RAII](http://sourceforge.net/docman/display_doc.php?docid=8673&group_id=9028)" by Mike Nordell
  - Article "[RAII, Dynamic Objects, and Factories in C++](http://www.codeproject.com/cpp/RAIIFactory.asp)" by Roland Pibinger
  - Wikibooks [RAII in VB6](http://en.wikibooks.org/wiki/Programming:Visual_Basic_Classic/Idioms#Resource_Acquisition_Is_Initialization_-_RAII)

[Category:オブジェクト指向](https://ja.wikipedia.org/wiki/Category:オブジェクト指向 "wikilink") [Category:イディオム_(プログラミング言語)](https://ja.wikipedia.org/wiki/Category:イディオム_\(プログラミング言語\) "wikilink") [Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink")

1.  [gcc拡張および](../Page/GNUコンパイラコレクション.md "wikilink")[C99](../Page/C99.md "wikilink")標準規格では、関数を抜けた際に自動的に破棄される[可変長配列](../Page/可変長配列.md "wikilink")をサポートするが、[スタックオーバーフロー](../Page/スタックオーバーフロー.md "wikilink")の危険性がある。必要な長さが事前に明らかでない場合は、mallocやnewによるヒープへの動的確保を利用する。
2.  [STLSoft: scoped_handle Class Template Reference](http://www.stlsoft.org/doc-1.9/classstlsoft_1_1scoped__handle.html)
3.  [CreateFileW function | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/fileapi/nf-fileapi-createfilew)
4.  [WSASocketW function | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)