> この記事は[C++](https://ja.wikipedia.org/wiki/C++)から翻訳されています。


**標準C++ライブラリ**は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[C++](../Page/C++.md "wikilink")の標準規格で定められた[ライブラリ](../Page/ライブラリ.md "wikilink")である。これは[クラスと](../Page/クラス_\(コンピュータ\).md "wikilink")[関数などの集合であり](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")、汎用的な[コンテナとそれを操作する関数](../Page/コンテナ_\(データ型\).md "wikilink")、[関数オブジェクト](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")、汎用的な[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")と[ストリーム](https://ja.wikipedia.org/wiki/ストリーム_\(プログラミング\) "wikilink")（コンソールや[ファイルとの](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[入出力](../Page/入出力.md "wikilink")）、言語機能サポート、数学関数ライブラリ（[超越関数](../Page/超越関数.md "wikilink")の近似を含む）などといった一般的かつ汎用的な関数などから構成される。また、ISO C90規格の[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")も含んでいる（[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")で[C99](../Page/C99.md "wikilink")互換のライブラリも追加された）。標準C++ライブラリはそのほとんどが[名前空間](../Page/名前空間.md "wikilink")**`std`**内にある。[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")規格以降では標準ライブラリに大幅な拡張や機能追加が行なわれた。

[Standard Template Library](https://ja.wikipedia.org/wiki/Standard_Template_Library "wikilink") (STL) は標準C++ライブラリの一部分で、[コンテナ](../Page/コンテナ_\(データ型\).md "wikilink")、[アルゴリズム](../Page/アルゴリズム.md "wikilink")、[イテレータ](../Page/イテレータ.md "wikilink")、[関数オブジェクト](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")などを含むものである。

C言語と異なり、標準C++ライブラリの[ヘッダには末尾に](https://ja.wikipedia.org/wiki/ヘッダファイル "wikilink")[拡張子](../Page/拡張子.md "wikilink") (`.h`) が付かない。

## ヘッダ

次に挙げるヘッダが存在する。

### コンテナ

  - <array> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[deque](https://ja.wikipedia.org/wiki/両端キュー "wikilink")\>
  - <forward_list> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[list](../Page/リスト_\(抽象データ型\).md "wikilink")\>
  - \<[map](../Page/連想配列.md "wikilink")\>
  - \<[queue](../Page/キュー_\(コンピュータ\).md "wikilink")\>
  - \<[set](https://ja.wikipedia.org/wiki/集合_\(プログラミング\) "wikilink")\>
  - \<[stack](../Page/スタック.md "wikilink")\>
  - <unordered_set> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <unordered_map> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[vector](../Page/配列.md "wikilink")\>

### 一般

  - \<[algorithm](../Page/アルゴリズム.md "wikilink")\>
  - <any> ([C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink"))
  - \<[bitset](https://ja.wikipedia.org/wiki/ビット配列 "wikilink")\>
  - <chrono> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <codecvt> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[functional](https://ja.wikipedia.org/wiki/関数オブジェクト "wikilink")\>
  - \<[iterator](../Page/イテレータ.md "wikilink")\>
  - \<[locale](https://ja.wikipedia.org/wiki/ロケール "wikilink")\>
  - \<[memory](../Page/メモリ管理.md "wikilink")\>
  - <memory_resource> ([C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink"))
  - <optional> ([C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink"))
  - \<[ratio](../Page/分数.md "wikilink")\> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <scoped_allocator> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[tuple](https://ja.wikipedia.org/wiki/タプル "wikilink")\> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <typeindex> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <type_traits> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <utility>
  - <variant> ([C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink"))

### 文字列

  - \<[regex](../Page/正規表現.md "wikilink")\> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[string](https://ja.wikipedia.org/wiki/文字列 "wikilink")\>
  - <string_view> ([C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink"))

### ストリームと入出力

  - <filesystem> ([C++17](https://ja.wikipedia.org/wiki/C++17 "wikilink"))
  - \<[fstream](https://ja.wikipedia.org/wiki/fstream "wikilink")\>
  - \<[ios](https://ja.wikipedia.org/wiki/Ios_\(C++\) "wikilink")\>
  - \<[iostream](https://ja.wikipedia.org/wiki/ストリーム_\(プログラミング\) "wikilink")\>
  - \<[iosfwd](https://ja.wikipedia.org/wiki/前方参照 "wikilink")\>
  - \<[iomanip](https://ja.wikipedia.org/wiki/iomanip "wikilink")\>
  - <istream>
  - <ostream>
  - \<[sstream](https://ja.wikipedia.org/wiki/sstream "wikilink")\>
  - <strstream> - deprecated、sstream 推奨
  - \<[streambuf](https://ja.wikipedia.org/wiki/streambuf "wikilink")\>

### 数値処理

  - \<[complex](../Page/複素数.md "wikilink")\>
  - <numeric>
  - <random>
  - \<[valarray](../Page/配列.md "wikilink")\>

### 言語支援

  - \<[exception](../Page/例外処理.md "wikilink")\>
  - <initializer_list> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <limits>
  - \<[new](../Page/メモリ管理.md "wikilink")\>
  - \<[typeinfo](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink")\>

### 診断

  - \<[stdexcept](https://ja.wikipedia.org/wiki/stdexcept "wikilink")\>
  - <system_error>

### スレッド

  - \<[atomic](https://ja.wikipedia.org/wiki/不可分操作 "wikilink")\> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <condition_variable> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[future](../Page/Future_パターン.md "wikilink")\> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[mutex](https://ja.wikipedia.org/wiki/ミューテックス "wikilink")\> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - <shared_mutex> ([C++14](https://ja.wikipedia.org/wiki/C++14 "wikilink"))
  - \<[thread](../Page/スレッド_\(コンピュータ\).md "wikilink")\> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))

### 標準Cライブラリ

C++において[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")のヘッダは、Cと異なった名前になる。ヘッダ名の末尾から拡張子 `.h` を取り除き、先頭に `c` を加える。例えば `time.h` は `ctime` という具合である。そしてヘッダ内の宣言は名前空間`std`の中に置かれるため、（名前空間の影響を受けないマクロを除いて）関数や型名には`std::`を付けて完全修飾することで区別する。なお、ISO Cでは関数をマクロとして実装することも認めていたが、ISO C++では認められていない。

  - \<[cassert](https://ja.wikipedia.org/wiki/標準Cライブラリ#診断機能_\<assert.h\> "wikilink")\>
  - \<[cctype](https://ja.wikipedia.org/wiki/標準Cライブラリ#文字操作_\<ctype.h\> "wikilink")\>
  - \<[cerrno](https://ja.wikipedia.org/wiki/標準Cライブラリ#エラー_\<errno.h\> "wikilink")\>
  - <cfenv> ([C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink"))
  - \<[cfloat](https://ja.wikipedia.org/wiki/標準Cライブラリ#浮動小数点型の特性_\<float.h\> "wikilink")\>
  - \<[climits](https://ja.wikipedia.org/wiki/標準Cライブラリ#整数型の大きさ_\<limits.h\> "wikilink")\>
  - \<[cmath](https://ja.wikipedia.org/wiki/標準Cライブラリ#数学_\<math.h\> "wikilink")\>
  - \<[csetjmp](https://ja.wikipedia.org/wiki/標準Cライブラリ#非局所分岐_\<setjmp.h\> "wikilink")\>
  - \<[csignal](https://ja.wikipedia.org/wiki/標準Cライブラリ#シグナル操作_\<signal.h\> "wikilink")\>
  - \<[cstdlib](https://ja.wikipedia.org/wiki/標準Cライブラリ#一般ユーティリティ_\<stdlib.h\> "wikilink")\>
  - \<[cstddef](https://ja.wikipedia.org/wiki/stddef.h "wikilink")\>
  - \<[cstdarg](https://ja.wikipedia.org/wiki/stdarg.h "wikilink")\>
  - <cuchar>
  - \<[ctime](https://ja.wikipedia.org/wiki/標準Cライブラリ#日付及び時間_\<time.h\> "wikilink")\>
  - \<[cstdio](https://ja.wikipedia.org/wiki/stdio.h "wikilink")\>
  - \<[cstring](https://ja.wikipedia.org/wiki/標準Cライブラリ#文字列操作_\<string.h\> "wikilink")\>
  - \<[cwchar](https://ja.wikipedia.org/wiki/wchar.h "wikilink")\>
  - \<[cwctype](https://ja.wikipedia.org/wiki/wctype.h "wikilink")\>

## 外部リンク

  - [Rogue Wave 標準 C++ ライブラリ・ユーザーズガイド](http://docs.sun.com/source/820-2985/)
  - \[<http://msdn2.microsoft.com/en-us/library/cscc687y(VS.80>).aspx Microsoft MSDN Library - Standard C++ Library Reference\]
  - [C++ Standard Library reference](http://cs.stmarys.ca/~porter/csc/ref/cpp_standlib.html)

## 参考文献

  - 『プログラミング言語C++第3版』(1998) [ビャーネ・ストロヴストルップ](../Page/ビャーネ・ストロヴストルップ.md "wikilink")著 長尾高弘訳 アジソンウェスレイパブリッシャーズジャパン ISBN 978-4756118950

[Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink")