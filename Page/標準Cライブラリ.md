> この記事は[C](https://ja.wikipedia.org/wiki/C)から翻訳されています。


**標準Cライブラリ**（ひょうじゅんシーライブラリ）は、[C言語](../Page/C言語.md "wikilink")の標準規格で定められた、[型](../Page/データ型.md "wikilink")・[マクロ](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")・[関数の集合からなる](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")である。

## 歴史

C言語は、[Pascal](../Page/Pascal.md "wikilink")や[PL/1](https://ja.wikipedia.org/wiki/PL/1 "wikilink")等の従来の[プログラミング言語](../Page/プログラミング言語.md "wikilink")とは異なり、文字列操作や入出力等の基本的な機能を内蔵していなかった。やがてC言語の利用者は、現在の標準Cライブラリの原型となる概念や実装を共有するようになった。

C言語の普及に伴い、言語仕様がそうであったように、ライブラリもまた多くの方言が生まれたが、[1989年](../Page/1989年.md "wikilink")（ISO/IEC 9899:1990）に[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")によるC言語の標準規格が制定されることで統一化が図られ、更にはいくつかの新たな概念が導入され、これが標準Cライブラリとなった。

その後に行われた標準規格の改定は、標準Cライブラリへの機能追加が主であった。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")（ISO/IEC 9899/AMD1:1995）には、主として[ワイド文字](../Page/ワイド文字.md "wikilink")操作に関する関数群が大幅に追加された。また、[1999年](../Page/1999年.md "wikilink")（ISO/IEC 9899:1999、[C99](../Page/C99.md "wikilink")）には、主として[複素数](../Page/複素数.md "wikilink")や数学上の演算に関する関数群が大幅に追加された。[2011年](../Page/2011年.md "wikilink")（ISO/IEC 9899:2011、[C11](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink")）には、[アライメント](https://ja.wikipedia.org/wiki/データ構造アライメント "wikilink")・[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")・[Unicode](../Page/Unicode.md "wikilink")・メモリ境界チェック付き関数などが追加になった。

## 主な機能

### 標準ヘッダ

[C11](https://ja.wikipedia.org/wiki/C11_\(C言語\) "wikilink") (ISO/IEC 9899:2011) では、標準ヘッダとして以下のものを定めている。

| ヘッダーファイル        | 概要                                                            |
| --------------- | ------------------------------------------------------------- |
| `assert.h`      | 診断機能                                                          |
| `complex.h`     | 複素数計算 (C99より追加)                                               |
| `ctype.h`       | 文字操作                                                          |
| `errno.h`       | エラー                                                           |
| `fenv.h`        | 浮動小数点環境 (C99より追加)                                             |
| `float.h`       | 浮動小数点型の特性                                                     |
| `inttypes.h`    | 整数型の書式の変換 (C99より追加)                                           |
| `iso646.h`      | 代替つづり(Alternate spellings) (ISO/IEC 9899/AMD1:1995 より追加)      |
| `limits.h`      | 整数型の大きさ                                                       |
| `locale.h`      | 文化圏固有操作                                                       |
| `math.h`        | 数学                                                            |
| `setjmp.h`      | 非局所分岐                                                         |
| `signal.h`      | シグナル操作                                                        |
| `stdalign.h`    | アライメント (C11より追加)                                              |
| `stdarg.h`      | 可変個数の実引数                                                      |
| `stdatomic.h`   | アトミック操作 (C11より追加)                                             |
| `stdbool.h`     | 論理型および論理値 (C99より追加)                                           |
| `stddef.h`      | 共通の定義                                                         |
| `stdint.h`      | 整数型 (C99より追加)                                                 |
| `stdio.h`       | 入出力                                                           |
| `stdlib.h`      | 一般ユーティリティ                                                     |
| `stdnoreturn.h` | `_Noreturn` (C11より追加)                                         |
| `string.h`      | 文字列操作                                                         |
| `tgmath.h`      | 型総称数学関数(Type-generic math) (C99より追加)                          |
| `threads.h`     | マルチスレッド (C11より追加)                                             |
| `time.h`        | 日付及び時間                                                        |
| `uchar.h`       | Unicodeユーティリティ (C11より追加)                                      |
| `wchar.h`       | 多バイトおよびワイド文字拡張ユーティリティ (ISO/IEC 9899/AMD1:1995 より追加)           |
| `wctype.h`      | ワイド文字種分類およびワイド文字大文字小文字変換ユーティリティ (ISO/IEC 9899/AMD1:1995 より追加) |

### 診断機能 `assert.h`

ヘッダ `assert.h` が[インクルード](https://ja.wikipedia.org/wiki/インクルード "wikilink")される時点における `NDEBUG` マクロの定義状態により、実行時診断機能の有効・無効を切り替えることができる。

  - `assert` — `NDEBUG` マクロが定義されていない場合に実行時診断を行う。

### 複素数 `complex.h`

複素数の演算、虚数単位の定義、実部と虚部の分離機能などが含まれている。

  - `complex` — 複素数型
  - `I` — [虚数単位](../Page/虚数単位.md "wikilink")
  - `cabs` — [絶対値](https://ja.wikipedia.org/wiki/絶対値#複素数の絶対値 "wikilink")
  - `carg` — [偏角](https://ja.wikipedia.org/wiki/複素数#極形式 "wikilink")
  - `cacos` — [逆余弦](https://ja.wikipedia.org/wiki/三角関数#逆三角関数 "wikilink")
  - `cacosh` — [逆双曲線余弦](https://ja.wikipedia.org/wiki/双曲線関数#逆双曲線関数 "wikilink")
  - `casin` — [逆正弦](https://ja.wikipedia.org/wiki/三角関数#逆三角関数 "wikilink")
  - `casinh` — [逆双曲線正弦](https://ja.wikipedia.org/wiki/双曲線関数#逆双曲線関数 "wikilink")
  - `catan` — [逆正接](https://ja.wikipedia.org/wiki/三角関数#逆三角関数 "wikilink")
  - `catanh` — [逆双曲線正接](https://ja.wikipedia.org/wiki/双曲線関数#逆双曲線関数 "wikilink")
  - `ccos` — [余弦](../Page/三角関数.md "wikilink")
  - `ccosh` — [双曲線余弦](../Page/双曲線関数.md "wikilink")
  - `cexp` — [指数関数](../Page/指数関数.md "wikilink")
  - `cfabs` — 浮動小数点数の[絶対値](https://ja.wikipedia.org/wiki/絶対値 "wikilink")
  - `cimag` — 複素数の虚部
  - `clog` — [自然対数](../Page/自然対数.md "wikilink")
  - `clog10` — [常用対数](https://ja.wikipedia.org/wiki/常用対数 "wikilink")
  - `conj` — 共役複素数
  - `cpow` — [冪乗](https://ja.wikipedia.org/wiki/冪乗 "wikilink")（べき乗、累乗）
  - `cproj` — リーマン球への射影
  - `creal` — 複素数の実部
  - `csin` — [正弦](../Page/三角関数.md "wikilink")
  - `csinh` — [双曲線正弦](../Page/双曲線関数.md "wikilink")
  - `csqrt` — 平方根
  - `ctan` — [正接](../Page/三角関数.md "wikilink")
  - `ctanh` — [双曲線正接](../Page/双曲線関数.md "wikilink")

### 文字操作 `ctype.h`

文字種別の分類、および大文字・小文字の変換を行う関数を提供する。 `ctype.h` ヘッダが提供する文字操作関数は、設定されているロケールに応じて動作が変わる。

  - `isalnum` — 英数字かどうかの判別
  - `isalpha` — 英字かどうかの判別
  - `iscntrl` — 制御文字かどうかの判別
  - `isdigit` — 数字かどうかの判別
  - `isgraph` — 空白（' '）を除く表示文字かどうかの判別
  - `islower` — 小文字かどうかの判別
  - `isprint` — 表示文字かどうかの判別
  - `ispunct` — 区切り文字かどうかの判別
  - `isspace` — 空白類文字かどうかの判別
  - `isupper` — 大文字かどうかの判別
  - `isxdigit` — 16進数字かどうかの判別
  - `tolower` — 小文字への変換
  - `toupper` — 大文字への変換

### エラー `errno.h`

ライブラリ関数内でエラーが発生した場合、そのエラーの内容を報告するために使用するいくつかのマクロ定義。

  - `errno` — エラー番号を格納する`int`型の変数を参照するマクロ。マクロであるが、見かけ上は`int`型の外部変数のように振舞う。
  - `EDOM` — 定義域エラー
  - `ERANGE` — 範囲エラー
  - `EILSEQ` — [多バイト文字の不正な並び](../Page/マルチバイト文字.md "wikilink")

### 浮動小数点型の特性 `float.h`

[浮動小数点型](https://ja.wikipedia.org/wiki/浮動小数点型 "wikilink")の大きさや様々な特性を表すマクロの定義。

  - `FLT_RADIX` — 浮動小数点型の内部表現に使用される基数
  - `FLT_ROUNDS` — 浮動小数点型の丸め方向
  - `FLT_MANT_DIG` — `float`型の`FLT_RADIX`を基数とした仮数部の桁数
  - `FLT_MAX_EXP` — `float` 型における`FLT_RADIX`を基数とした指数部の最大値
  - `FLT_MIN_EXP` — `float` 型における`FLT_RADIX`を基数とした指数部の最小値
  - `FLT_MAX_10_EXP` — `float` 型における`10`を基数とした指数部の最大値
  - `FLT_MIN_10_EXP` — `float` 型における`10`を基数とした指数部の最小値
  - `FLT_MAX` — `float` 型の最大値
  - `FLT_MIN` — `float` 型の正の値の最小値（整数型とは違い`float`型の実数の最小値は`-FLT_MAX`である）
  - `FLT_EPSILON` — `float`型で表現可能な1より大きい最小値と`1`との差（[計算機イプシロン](https://ja.wikipedia.org/wiki/計算機イプシロン "wikilink")）
  - `DBL_MANT_DIG` — `double` 型の`FLT_RADIX`を基数とした仮数部の桁数
  - `DBL_MAX_EXP` — `double` 型における`FLT_RADIX`を基数とした指数部の最大値
  - `DBL_MIN_EXP` — `double`型における`FLT_RADIX`を基数とした指数部の最小値
  - `DBL_MAX_10_EXP` — `double`型における`10`を基数とした指数部の最大値
  - `DBL_MIN_10_EXP` — `double` 型における`10`を基数とした指数部の最小値
  - `DBL_MAX` — `double`型の最大値
  - `DBL_MIN` — `double`型の正の値の最小値（整数型とは違い`double`型の実数の最小値は`-DBL_MAX`である）
  - `DBL_EPSILON` — `double` 型で表現可能な1より大きい最小値と`1`との差
  - `LDBL_MANT_DIG` — `long double` 型の `FLT_RADIX` を基数とした仮数部の桁数
  - `LDBL_MAX_EXP` — `long double` 型における `FLT_RADIX` を基数とした指数部の最大値
  - `LDBL_MIN_EXP` — `long double` 型における `FLT_RADIX` を基数とした指数部の最小値
  - `LDBL_MAX_10_EXP` — `long double` 型における`10`を基数とした指数部の最大値
  - `LDBL_MIN_10_EXP` — `long double` 型における`10`を基数とした指数部の最小値
  - `LDBL_MAX` — `long double` 型の最大値
  - `LDBL_MIN` — `long double` 型の最小値
  - `LDBL_EPSILON` — `long double` 型で表現可能な1より大きい最小値と`1`との差

### 整数型の大きさ `limits.h`

整数型の大きさを表すマクロの定義。

  - `CHAR_BIT` — `char`型を構成する[ビット](../Page/ビット.md "wikilink")数（`>=8`）
  - `MB_LEN_MAX` — 処理系がサポートする[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")の最大バイト数
  - `CHAR_MAX` — `char`型の最大値。`SCHAR_MAX` または `UCHAR_MAX` と同じ
  - `CHAR_MIN` — `char`型の最小値。`SCHAR_MIN` または `0` と同じ
  - `SCHAR_MAX` — `signed char` 型の最大値（`>=127`）
  - `SCHAR_MIN` — `signed char` 型の最小値（`<=-127`）
  - `UCHAR_MAX` — `unsigned char` 型の最大値（`>=255`）
  - `SHRT_MAX` — `short`型の最大値（`>=32767`）
  - `SHRT_MIN` — `short`型の最小値（`<=-32767`）
  - `USHRT_MAX` — `unsigned short`型の最大値（`>=65535`）
  - `INT_MAX` — `int`型の最大値（`>=32767`）
  - `INT_MIN` — `int`型の最小値（`<=-32767`）
  - `UINT_MAX` — `unsigned int`型の最大値（`>=65535`）
  - `LONG_MAX` — `long`型の最大値（`>=2147483647`）
  - `LONG_MIN` — `long`型の最小値（`<=-2147483647`）
  - `ULONG_MAX` — `unsigned long`型の最大値（`>=4294967295`）

### 文化圏固有操作 `locale.h`

[ロケール](https://ja.wikipedia.org/wiki/ロケール "wikilink")ごとに異なる、[文字コード](../Page/文字コード.md "wikilink")、数値を記述する場合の書式等の操作を行う型・マクロ・関数の宣言定義。

  - `struct lconv` — 数値を記述する場合の書式に関する情報を格納する構造体
  - `localeconv` — 設定されているロケールに応じた値を格納した `struct lconv`を参照
  - `setlocale` — 現在のロケールを設定

### 数学 `math.h`

数学的な演算を行うための関数、および関連するマクロの宣言定義。

  - `HUGE_VAL` — `float`型で表現できるとは限らない正の`double`型の式。無限大またはそれに類する大きな値
  - `acos` — [逆余弦](https://ja.wikipedia.org/wiki/三角関数#逆三角関数 "wikilink")
  - `asin` — [逆正弦](https://ja.wikipedia.org/wiki/三角関数#逆三角関数 "wikilink")
  - `atan` — [逆正接](https://ja.wikipedia.org/wiki/三角関数#逆三角関数 "wikilink")
  - `atan2` — 底辺と高さを指定した直角三角形の逆正接
  - `ceil` — [天井関数](https://ja.wikipedia.org/wiki/床関数 "wikilink")
  - `cos` — [余弦](../Page/三角関数.md "wikilink")
  - `cosh` — [双曲線余弦](../Page/双曲線関数.md "wikilink")
  - `exp` — [指数関数](../Page/指数関数.md "wikilink")
  - `fabs` — 浮動小数点数の[絶対値](https://ja.wikipedia.org/wiki/絶対値 "wikilink")
  - `floor` — [床関数](https://ja.wikipedia.org/wiki/床関数 "wikilink")
  - `fmod` — 浮動小数点どうしの商と剰余
  - `frexp` — 「正規化された[仮数](https://ja.wikipedia.org/wiki/仮数 "wikilink")部」と「`2`の累乗」への分解
  - `ldexp` — 浮動小数点数と2の累乗との乗算
  - `log` — [自然対数](../Page/自然対数.md "wikilink")
  - `log10` — [常用対数](https://ja.wikipedia.org/wiki/常用対数 "wikilink")
  - `modf` — 整数部と小数部の分解
  - `pow` — [冪乗](https://ja.wikipedia.org/wiki/冪乗 "wikilink")（べき乗、累乗）
  - `sin` — [正弦](../Page/三角関数.md "wikilink")
  - `sinh` — [双曲線正弦](../Page/双曲線関数.md "wikilink")
  - `sqrt` — 平方根
  - `tan` — 三角関数|正接
  - `tanh` — 双曲線関数|双曲線正接

### 非局所分岐 `setjmp.h`

関数の枠組みを越えた分岐（ジャンプ）を制御するための型・マクロ・関数の宣言定義。

  - `jmp_buf` — `setjmp` マクロが実行環境を保存するための型
  - `setjmp` — `longjmp` 関数による復帰を可能にするために実行環境を保存するためのマクロ（しばしば直接、関数で実装されているが、標準ではマクロとされている。POSIXではマクロか関数かは指定されない、としている）
  - `longjmp` — `setjmp` マクロで保存された環境への復帰

### シグナル操作 `signal.h`

[シグナル処理関数の登録およびシグナルの送信に関するマクロ](../Page/シグナル_\(Unix\).md "wikilink")・型・関数の宣言定義。

  - `sig_atomic_t` — 代入および参照が不分割に実行される（アトミックオペレーションとなる）整数型
  - `raise` — シグナルの送信
  - `signal` — シグナル処理関数の登録

### 可変個数の引数 `stdarg.h`

printf 関数のような[可変長引数](https://ja.wikipedia.org/wiki/可変長引数 "wikilink")の関数における実引数の操作に関する型とマクロの定義。

  - `va_list` — 可変個の実引数にアクセスするための情報を格納する型
  - `va_arg` — 可変個の実引数の取り出し
  - `va_start` — 可変個の実引数操作の開始
  - `va_end` — 可変個の実引数操作の終了

### 共通の定義 `stddef.h`

処理系に依存する型とマクロの定義。

  - `ptrdiff_t` — ポインタ減算の結果の型。符号付き整数型。
  - `size_t` — [sizeof](https://ja.wikipedia.org/wiki/sizeof "wikilink") 演算子の結果の型。符号無し整数型。Unix 系など、POSIX 1003.1-1996 API に準拠している場合、`ssize_t`が符号付きの`size_t`。
  - `wchar_t` — ワイド文字型。8ビット以上の整数だが、コンパイラやプラットフォームにより大きさは様々。[Microsoft Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")16ビット、Unix系では32ビットであることが多い。
  - [`NULL`](https://ja.wikipedia.org/wiki/Null "wikilink") — 空ポインタ定数マクロ
  - `offsetof` — 構造体メンバの先頭からのオフセットを得る

### 入出力 `stdio.h`

[ストリームおよび](../Page/ストリーム_\(プログラミング\).md "wikilink")[ファイルの操作に関する型](../Page/ファイル_\(コンピュータ\).md "wikilink")・マクロ・関数の宣言定義。

  - `FILE` — ストリームを制御するためのオブジェクト型（構造体とは限らない）
  - `fpos_t` — ファイルのシーク位置を格納するための型
  - `clearerr` — ファイル終端表示子およびエラー表示子のクリア
  - `fclose` — ファイルのクローズ
  - `feof` — ファイル終端表示子の判定
  - `ferror` — エラー表示子の判定
  - [`fgetc`](https://ja.wikipedia.org/wiki/fgetc "wikilink") — ストリームからの1文字入力
  - `fgetpos` — ストリームのファイル位置表示子の参照
  - [`fgets`](https://ja.wikipedia.org/wiki/fgets "wikilink") — ストリームからの1行入力
  - `fopen` — ファイルのオープン
  - `fprintf` — ストリームへの書式付き出力
  - [`fputc`](https://ja.wikipedia.org/wiki/fputc "wikilink") — ストリームへの1文字出力
  - `fputs` — ストリームへの1行出力
  - [`fread`](https://ja.wikipedia.org/wiki/fread "wikilink") — ストリームからの読み込み
  - `fscanf` — ストリームからの書式付き入力
  - `fseek` — ストリームのファイル位置表示子の変更
  - `fsetpos` — ストリームのファイル位置表示子の設定
  - `ftell` — ストリームのファイル位置表示子の参照
  - [`fwrite`](https://ja.wikipedia.org/wiki/fwrite "wikilink") — ストリームへの書き込み
  - [`getc`](https://ja.wikipedia.org/wiki/getc "wikilink") — ストリームからの1文字入力
  - `getchar` — 標準入力からの1文字入力
  - [`gets`](https://ja.wikipedia.org/wiki/gets "wikilink") — 標準入力からの1行入力（ただし、C11で削除された）
  - `perror` — 標準エラー出力への[エラーメッセージ](https://ja.wikipedia.org/wiki/エラーメッセージ "wikilink")の出力
  - [`printf`](https://ja.wikipedia.org/wiki/printf "wikilink") — 標準出力への書式付き出力
  - [`putc`](https://ja.wikipedia.org/wiki/putc "wikilink") — ストリームへの1文字出力
  - `putchar` — 標準出力への1文字出力
  - `puts` — 標準出力への1行出力
  - `remove` — ファイルの削除
  - `rename` — ファイル名の変更
  - `rewind` — ストリームの巻き戻し
  - [`scanf`](https://ja.wikipedia.org/wiki/scanf "wikilink") — 標準入力からの書式付き入力
  - `setbuf` — ストリームのバッファ設定
  - `setvbuf` — ストリームの詳細なバッファ設定
  - `sprintf` — 文字配列への書式付き出力
  - `sscanf` — 文字列からの書式付き入力
  - `tmpfile` — テンポラリファイルをバイナリモードでオープン
  - `tmpnam` — テンポラリファイル名の生成
  - `vprintf` — 標準出力への書式付き出力（`va_list`版）
  - `vscanf` — 標準入力からの書式付き入力（`va_list`版）

### 一般ユーティリティ `stdlib.h`

一般[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティ "wikilink")に関する型・マクロ・関数の宣言定義。

  - `div_t` — `int`型の商と剰余を格納する構造体
  - `ldiv_t` — `long`型の商と剰余を格納する構造体
  - `MB_CUR_MAX` — 設定されているロケールにおける[マルチバイト文字](../Page/マルチバイト文字.md "wikilink")の最大バイト数を表すマクロ
  - `RAND_MAX` — `rand`関数が返す擬似乱数の最大値
  - `abort` — プログラムの異常終了
  - [`abs`](https://ja.wikipedia.org/wiki/abs "wikilink") — `int`型の絶対値
  - `atexit` — 終了時関数の登録
  - [`atof`](https://ja.wikipedia.org/wiki/atof "wikilink") — 文字列から`double`型への変換
  - [`atoi`](https://ja.wikipedia.org/wiki/atoi "wikilink") — 文字列から`int`型への変換
  - [`atol`](https://ja.wikipedia.org/wiki/atol "wikilink") — 文字列から`long`型への変換
  - `bsearch` — [バイナリサーチ](https://ja.wikipedia.org/wiki/バイナリサーチ "wikilink")
  - [`calloc`](https://ja.wikipedia.org/wiki/calloc "wikilink") — [メモリブロック](https://ja.wikipedia.org/wiki/メモリブロック "wikilink")の割り付けとクリア
  - [`div`](https://ja.wikipedia.org/wiki/div "wikilink") — `int`型どうしの商と剰余
  - [`exit`](https://ja.wikipedia.org/wiki/exit "wikilink") — プログラムの終了
  - `free` — メモリブロックの解放
  - `getenv` — 環境変数の参照
  - `labs` — `long`型の絶対値
  - `ldiv` — `long`型どうしの商と剰余
  - [`malloc`](https://ja.wikipedia.org/wiki/malloc "wikilink") — メモリブロックの割り付け
  - `mblen` — マルチバイト文字の構成バイト数
  - `mbstowcs` — マルチバイト文字列からワイド文字列への変換
  - `mbtowc` — マルチバイト文字からワイド文字への変換
  - `qsort` — [クイックソート](../Page/クイックソート.md "wikilink") (ただし、仕様上はソートを行うとあるだけで「クイックソートによる」とは書かれていない)
  - [`rand`](https://ja.wikipedia.org/wiki/rand "wikilink") — 擬似乱数
  - `realloc` — メモリブロックの再割り付け
  - [`srand`](https://ja.wikipedia.org/wiki/srand "wikilink") — 乱数種の設定
  - `strtod` — 文字列から`double`型への変換
  - `strtol` — 文字列から`long`型への変換（基数指定可）
  - `strtoul` — 文字列から`unsigned long`型への変換（基数指定可）
  - [`system`](https://ja.wikipedia.org/wiki/system "wikilink") — コマンドプロセッサの呼び出し
  - `wcstombs` — ワイド文字列からマルチバイト文字列への変換
  - `wctomb` — ワイド文字列からマルチバイト文字列への変換

### 文字列操作 `string.h`

文字列操作に関する型・マクロ・関数の宣言定義。

  - `memchr` — メモリブロック中の文字検索
  - `memcmp` — メモリブロックの比較
  - `memcpy` — メモリブロックのコピー
  - `memmove` — メモリブロックの転送
  - [`memset`](https://ja.wikipedia.org/wiki/memset "wikilink") — メモリブロックを指定文字で埋める
  - `strchr` — 文字列内の文字探索
  - [`strcat`](https://ja.wikipedia.org/wiki/strcat "wikilink") — 文字列の連結
  - [`strcmp`](https://ja.wikipedia.org/wiki/strcmp "wikilink") — 文字列の比較
  - [`strcpy`](https://ja.wikipedia.org/wiki/strcpy "wikilink") — 文字列のコピー
  - `strcspn` — 文字列中の指定文字群を含まない先頭部分の長さ
  - `strerror` — エラー番号に対応したエラーメッセージ文字列の取得
  - `strcoll` — ロケールに応じた順序付けによる文字列の比較
  - [`strlen`](https://ja.wikipedia.org/wiki/strlen "wikilink") — 文字列の長さ
  - `strncat` — 字数制限付きで文字列の連結
  - `strncmp` — 字数制限付きで文字列の比較
  - `strncpy` — 字数制限付きで文字列のコピー
  - `strpbrk` — 文字列中の文字群探索
  - `strrchr` — 文字列内の逆方向文字探索
  - `strspn` — 文字列中の指定文字群を含む先頭部分の長さ
  - `strstr` — 文字列中の文字列探索
  - `strtok` — 文字列からの字句切り出し
  - `strxfrm` — ロケールに応じた順序付けになるように文字列を変換

### 日付及び時間 `time.h`

[グレゴリオ暦](../Page/グレゴリオ暦.md "wikilink")に基づく日付等を扱うための型・マクロ・関数の宣言定義。

  - `clock_t` — clock 関数が返す値の型
  - [`time_t`](https://ja.wikipedia.org/wiki/time_t "wikilink") — 時刻を表す型
  - `struct tm` — 暦時刻の各要素（年月日時分秒等）を格納する構造体
  - `CLOCKS_PER_SEC` — `clock`関数が返す値を秒単位に変換するための[除数](https://ja.wikipedia.org/wiki/除数 "wikilink")を表すマクロ定数
  - `asctime` — `tm`構造体から文字列への変換
  - `clock` — 処理系定義の開始点（通例プログラム実行開始）からの経過時間（プロセッサ時間、[CPU](../Page/CPU.md "wikilink")使用時間）の取得
  - `ctime` — `time_t`型から文字列への変換
  - `difftime` — `time_t`型どうしの秒単位での差
  - `gmtime` — [協定世界時](../Page/協定世界時.md "wikilink") (UTC) の取得
  - `localtime` — 地方時刻の取得
  - `mktime` — `tm`構造体から `time_t`型への変換
  - `strftime` — `tm`構造体から文字列への書式付き変換
  - `time` — 現在の[暦時刻](https://ja.wikipedia.org/wiki/暦時刻 "wikilink") (calendar time) の取得

time_tは、特に[UNIX](../Page/UNIX.md "wikilink")用の実装を初めとした多くの実装において、協定世界時 (UTC) 1970年1月1日0時0分0秒からの経過秒数を符号付32ビット整数型で表すようになっている。そのような実装では[2001年9月9日問題](../Page/2001年9月9日問題.md "wikilink")、[2038年問題](../Page/2038年問題.md "wikilink")のような問題が生じる。詳しくは各問題の記事を参照されたい。

## フリースタンディング環境

[フリースタンディング環境](../Page/フリースタンディング環境.md "wikilink")では、C89 では標準Cライブラリのうち `float.h`、`limits.h`、`stdarg.h`、`stddef.h` に対応している。ISO/IEC 9899/AMD1:1995 では加えて `iso646.h` が、C99 では更に `stdbool.h` および `stdint.h` に対応している。

## Unix系の標準Cライブラリ

[Unix系](../Page/Unix系.md "wikilink")に関係する[POSIX](../Page/POSIX.md "wikilink")、[SUS](../Page/Single_UNIX_Specification.md "wikilink")、[Linux Standard Baseなどの標準仕様では](../Page/Linux_Standard_Base.md "wikilink")、標準Cライブラリを包含し、さらに追加の関数やマクロ、型などが規定されている。

[GNU/Linuxシステム](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")（多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")）では、一般的に[GNU Cライブラリ](https://ja.wikipedia.org/wiki/GNU_Cライブラリ "wikilink") (glibc) が標準Cライブラリの実装として用いられている。[BSD](../Page/BSD.md "wikilink")系列での実装は、[BSD libcと呼称される](https://ja.wikipedia.org/wiki/BSD_libc "wikilink")。

## C++における標準Cライブラリ

C++03の[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")では、C95相当の標準Cライブラリを包含している。更には、C95では任意実装であった`float`型や`double`型の数学関数も常にサポートされる。[C++11](https://ja.wikipedia.org/wiki/C++11 "wikilink")ではC99相当の標準Cライブラリと `uchar.h` を包含している。

標準Cライブラリにおけるヘッダ <var>`xxx`</var>`.h` は、[C++](../Page/C++.md "wikilink")では `c`<var>`xxx`</var> というヘッダにマッピングされる。各識別子は `std` [名前空間](../Page/名前空間.md "wikilink")内で宣言される。また、標準Cライブラリとの互換性を持たせるため、<var>`xxx`</var>`.h` 形式のヘッダも使用することができ、`std` 名前空間内で宣言された識別子は`using`指令によってグローバル名前空間に引き出される。

C++固有の事情から、一部の関数についてはC言語との互換性が低下している。具体的には`memchr`関数や`strstr`関数等がそれにあたる。すなわち、引数として渡されるポインタが指す型が`const`修飾されているか否かにより、返却値の型もそれに合わせて変更されるように[多重定義](../Page/多重定義.md "wikilink")されている。

Cの場合

``` c
char *strchr(const char*, int);
```

C++の場合

``` cpp
const char *strchr(const char*, int);
char *strchr(char*, int);
```

## 外部リンク

[Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:標準Cライブラリ](https://ja.wikipedia.org/wiki/Category:標準Cライブラリ "wikilink")