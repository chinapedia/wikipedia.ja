> この記事は[NaN](https://ja.wikipedia.org/wiki/NaN)から翻訳されています。


**NaN**（**N**ot **a** **N**umber、非数、ナン）は、[コンピュータ](../Page/コンピュータ.md "wikilink")において、主に[浮動小数点演算の結果として](../Page/浮動小数点数.md "wikilink")、不正なオペランドを与えられたために生じた結果を表す値またはシンボルである。NaNの体系的仕様は、[無限](../Page/無限.md "wikilink")大の表現などと共に1985年の [IEEE 754](../Page/IEEE_754.md "wikilink") 浮動小数点規格で標準が与えられている。

NaNには quiet NaN と signaling NaN の2種類がある。quiet NaN は不正な操作や不正な値で生じる誤りを伝播させるのに使用され、signaling NaN は数値計算との混合や基本的な浮動小数点演算への他の拡張といった高度な機能のサポートに使える。例えば結果が実数の範囲内でない[ゼロ除算](../Page/ゼロ除算.md "wikilink")において、ゼロ以外のゼロ除算は[無限](../Page/無限.md "wikilink")大だが、ゼロのゼロ除算は NaN である。負数の[平方根](../Page/平方根.md "wikilink")は[虚数](../Page/虚数.md "wikilink")となるため、浮動小数点数としては表現できず、NaN で表現される。他に、正負の無限大の両方が絡んだために、どちらの無限大ともできないような計算の結果も NaN である。また、NaN は計算上必要な値が得られていない場合にも使われることがある\[1\]\[2\]。

類似用語として**NA**（Not Available）や [n/a](https://ja.wikipedia.org/wiki/n/a "wikilink") があるが、異なる概念なので注意を要する。（後述[NA参照](https://ja.wikipedia.org/wiki/#NA "wikilink")）

## 浮動小数点数の NaN

浮動小数点演算においては、NaNと無限大は別の概念であるが、どちらも浮動小数点数としての表現も特殊であり、それを使った演算も特殊である（文献によっては、それら両方を含む広義の「非数」という表現が見られることもあるが、混同のおそれが無い場合以外は避けたほうがよい）。不正な演算という概念と、[算術オーバーフロー](https://ja.wikipedia.org/wiki/算術オーバーフロー "wikilink")（無限大を結果とする場合もある）や算術アンダーフロー（[非正規化数](../Page/非正規化数.md "wikilink")か、ゼロとなる）は異なる。

[IEEE 754では](../Page/IEEE_754.md "wikilink")、NaNの表現について、指数部は全て1とし（これは無限大と同じ）、無限大の場合は[仮数](https://ja.wikipedia.org/wiki/仮数 "wikilink")部の全てを0とするのに対し、NaNは全0以外の任意のビット列としている。他に、先頭の符号ビットで正負の区別がある。また、NaNの種別として**quiet NaN** (*qNaN*) と**signaling NaN**（*sNaN*）があり、例外を投げる場合について違いがある。

仮数部のビット列について任意としているため複数の表現があり得るが、それらが必ずしも区別して扱われるとは限らない。qNaNとsNaNの表現について規格の以前の版では具体的に決まっていなかったなど煩雑なため、詳細は[\#エンコード](https://ja.wikipedia.org/wiki/#エンコード "wikilink")の節を参照。

IEEE 754 の[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")（32ビット）での NaN をビット列として表現すると <span style="white-space:nowrap;">s111 1111 1xxx xxxx xxxx xxxx xxxx xxxx</span> となり、ここで *s* は正負の符号（多くのアプリケーションでは無視する）、*x* は特殊ペイロード（多くのアプリケーションでは無視する）である。

大小比較以外の浮動小数点数操作は一般に quiet NaN をそのまま伝播する。signaling NaN に対する浮動小数点数操作は不正例外を発生し、デフォルトの例外処理ではqNaNをオペランドとしたときと同様に演算結果としてqNaNを生成するだけである。

NaNとの大小比較では、自分自身と比較した場合でも「大小不明な結果」を返す。比較には signaling と non-signaling があり、signaling 版では NaN との比較を行うと不正例外を発生する。等号および不等号で比較する場合は常に non-signaling であり、*x* が quiet NaN なら *x* = *x* は偽 (false) を返す。他の一般的な大小比較は全て signaling であり、オペランドとして NaN を渡されると不正例外を発生するが、規格ではそれらの non-signaling 版も提供することになっている。*isNaN(x)* は渡された値がNaNかどうかを判定する関数であり、*x* が signaling NaN であっても例外を発生しない。

quiet NaN が演算を通して伝播していくため、計算途中で何度もチェックを入れる必要はなく、最終的に得られた値を調べればよい。ただし、言語や関数によっては NaN を渡されてもそれが計算結果に影響しない場合に黙って普通の浮動小数点数値を返すことがある。例えばどんな数でも0乗すれば1になるので、NaN^0 は 1 と定義することもできる。そのため一般に最終的な値を得るまでの過程で NaN が入り込んでいたかを示す INVALID フラグを調べる必要がある\[3\]（詳しくは後述の[関数定義における NaN節を参照](https://ja.wikipedia.org/wiki/#関数定義における_NaN "wikilink")）。

標準の最新版である [IEEE 754-2008](../Page/IEEE_754.md "wikilink") の6.2節に、引数のうち大きい方あるいは小さい方を返す **maxnum** と **minnum** という関数があるが、これらは引数の一方が NaN の場合は常にもう一方の引数を返す。

同様のコンセプトは [GNU Octave](../Page/GNU_Octave.md "wikilink") と [MATLAB](../Page/MATLAB.md "wikilink") のNaNツールボックスに実装されている\[4\]。NaNツールボックスに含まれる統計関数群（平均、標準偏差などの関数）は、NaNを統計データがないことを示すものとみなし、単に NaN を無視して伝播させない。

### NaN を返す演算

以下の処理で NaN が生成される可能性がある\[5\]。

  - 唯一の引数に NaN を指定された数学関数

  -   - 次のような除算: 0/0、±∞/±∞
      - 次のような乗算: 0×±∞、±∞×0
      - 次のような加算（および等価な減算）: ∞ + (−∞)、(−∞) + ∞
      - 標準には[冪乗](https://ja.wikipedia.org/wiki/冪乗 "wikilink")が2種類定義されている。
          - `pow` 関数と冪指数が整数である `pown` 関数は、0<sup>0</sup>、1<sup>∞</sup>、∞<sup>0</sup> を 1 と定義している。
          - `powr` 関数は上記3つの不定形を不正演算と定義しており、NaN を返す。

  - 結果が[虚数](../Page/虚数.md "wikilink")となるような演算（以下は一部）

      - 負数の平方根
      - 負数の対数
      - \-1未満の値や+1より大きい値の逆三角関数

必要な値がないとき、明示的に変数に NaN を代入しておくことがある。IEEE 754 制定以前、未定義値を表すのに特別な値（例えば −99999999）を使うことが多かったが、そういった値が常に想定通りに扱われるとは限らなかった\[6\]。

上記の全ケースで常に NaN が生成されるとは限らない。マスクされていない例外やトラップを発生できる場合、NaNを生成する代わりにトラップを発生させることもある\[7\]。引数が quiet NaN で signaling NaN ではない場合、例外の発生する条件が成立しておらず quiet NaN を結果として返す。明示的に代入する場合は signaling NaN であっても例外は発生しない。

### quiet NaN

quiet NaN あるいは qNaN は演算過程で伝播していく以外に何も例外などを発生させない。ただし、NaNを出力できない処理の場合は別である。たとえば、フォーマットの変換やある種の比較操作である(NaNが入力されることを想定していない操作)。

### signaling NaN

signaling NaN あるいは sNaN は特殊なNaNであり、多くの操作に入力として用いられたときに不正例外を発生する（通常、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[例外処理](../Page/例外処理.md "wikilink")が呼び出される）。その後、sNaN は qNaN に変化し、伝播していく。これは [IEEE 754](../Page/IEEE_754.md "wikilink") で導入された。この機能の使い方はいくつかある。

  - 未使用メモリに signaling NaN の値を入れておくと、初期化前にそのデータが使われたときに不正例外が発生するようにできる。
  - sNaN をもっと複雑な[オブジェクトのプレースホルダーとして使うこともできる](../Page/オブジェクト_\(プログラミング\).md "wikilink")。
      - 算術アンダーフローとなった数を表現する。
      - [算術オーバーフロー](https://ja.wikipedia.org/wiki/算術オーバーフロー "wikilink")となった数を表現する。
      - より高い精度フォーマットの数
      - [複素数](../Page/複素数.md "wikilink")

これらに遭遇するとトラップハンドラは sNaN をデコードして計算結果へのインデックスを返すこともできる。実際にはこの手法は非常に複雑である。NaN の正負の符号ビットの単純な操作（たとえば絶対値を返す操作）における扱いは通常の算術操作とは異なる。トラップ処理は規格上は要求されていない。このような問題を扱う他の移植性の高い方法がいくつか存在する。

## 関数定義における NaN

数値関数が入力として NaN を受け取ったとき、どう処理すべきかについては様々な意見がある。1つの見方は、NaN はエラーを示すものとして常に出力に伝播させなければならないというものである。別の見方として、その関数に複数の引数があり、NaN でない引数だけで出力値が決定される場合、その値を返すべきだという考え方もある。IEEE 754 は主に後者の立場で策定されている。例えば、hypot(±∞, qNaN) と hypot(qNaN, ±∞) は +∞ を返す。

例えば[冪乗](https://ja.wikipedia.org/wiki/冪乗 "wikilink")関数 `pow(x,y) = x ** y` という関数を考えてみよう。0<sup>0</sup>、∞<sup>0</sup>、1<sup>∞</sup> といった式は極限を考えると（∞ × 0 などと同様）だが、[0の0乗](../Page/0の0乗.md "wikilink")は1と定義すべきだという意見もある。

引数が未定義なら結果も未定義とする場合、`pow(1,qNaN)` は qNaN を出力すべきである。しかし、一般的な数学ライブラリでは `pow(1,y)` は任意の[実数](../Page/実数.md "wikilink") y について常に 1 を返す。これは y が無限大であっても同様である。同様に `pow(x,0)` は x が 0 や無限大であっても 1 を返す。本来不定形であるはずなのに 1 を返す論理的根拠は、[ロピタルの定理](../Page/ロピタルの定理.md "wikilink")である。IEEE 754-2008 では、`pow(1,qNaN)` と `pow(qNaN,0)` はどちらも 1 を返すべきだとされている。

冪乗関数がより厳密な解釈に従うべきだという立場を考慮し、IEEE 754-2008 では他に2つの冪乗関数を定義している。`pown(x, n)` は冪指数として整数しか指定できない。`powr(x, y)` は引数のいずれかが NaN の場合や計算結果が不定形になる場合、常に NaN を返す。

## 整数の NaN

固定ビット幅の[整数](../Page/整数.md "wikilink")フォーマットは明確に不正データを示す方法がない。

[Perl](../Page/Perl.md "wikilink") の BigInt パッケージは正常な整数でないものを表す文字列として "NaN" を使用する。

`>perl -mMath::BigInt -e "print Math::BigInt->new('foo')"`
`NaN`

## テキスト表現

各種プログラミング言語やライブラリの入出力における、[リテラル](../Page/リテラル.md "wikilink")などにおけるNaNのテキスト表現はまちまちである。以下に例を挙げる。

` nan`
` NaN`
` NaN%`
` NAN`
` NaNQ`
` NaNS`
` qNaN`
` sNaN`
` 1.#SNAN`
` 1.#QNAN`
` +nan.0`
` -nan.0`
` -1.#IND`

符号と診断用の情報（ペイロード）を含む場合の例。

` -NaN`
`  NaN12345`
` -sNaN12300`
` -NaN(s1234)`

これら以外の場合もある。

## エンコード

[IEEE 754](../Page/IEEE_754.md "wikilink") の浮動小数点数フォーマットにおけるNaNの表現（エンコード）の詳細について説明する。符号ビットはどちらでもよい。指数部は全て1であり（無限大と同じ）、仮数部はゼロでない値（無限大ではゼロ）である。IEEE 754-1985 では signaling NaN と quiet NaN を区別する方法は標準化されていなかった。一般に仮数部の最上位ビットで signaling か quiet かを判定する実装が多かったが、その具体的な 1 と 0 の意味付けは逆の場合があった。

  - 多くのプロセッサ（[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")/[AMDの](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")[x86-32](../Page/IA-32.md "wikilink")/[x86-64ファミリ](../Page/X64.md "wikilink")、モトローラ[MC68000](../Page/MC68000.md "wikilink")ファミリ、[AIM](https://ja.wikipedia.org/wiki/AIM連合 "wikilink") [PowerPC](../Page/PowerPC.md "wikilink")ファミリ、[Sun](../Page/サン・マイクロシステムズ.md "wikilink") [SPARC](../Page/SPARC.md "wikilink")ファミリ）では、0でないとき quiet、0のとき signaling と解釈される。したがって、そのビットは 'is_quiet' フラグと言える。
  - [PA-RISC](../Page/PA-RISC.md "wikilink")と[MIPSの場合](../Page/MIPSアーキテクチャ.md "wikilink")、0のとき quiet、0でないとき signaling と解釈される。したがって、そのビットは 'is_signaling' フラグと言える。

IEEE 754-2008 では、このビットを仮数部の最上位ビットとし解釈についても標準化するよう、正式な勧告を追加している。

  - 二進フォーマットの場合、'is_quiet' フラグとすることを標準とする。すなわち、0でないとき quiet、0のとき signaling である。
  - IEEE 754-2008では十進フォーマットも定めたため、その場合のNaNについても定められた。符号ビットに続く5ビットのフィールドを全て1にセットすることでNaNを表す。そして、その直後に 'is_signaling' フラグとなるビットがある。当該ビットが0のとき quiet、1のとき signaling である。

ビットを 0 にして quiet と signaling を逆にしようとした場合、無限大にならないよう別のビットも操作する必要があるかもしれないことに注意が必要である。

（qNaN/sNaNであることを示すための以上のビットを除くと）残りのビットについては標準は特に無い（無限大を表す仮数部が全て0の場合を除く）。これをNaNの「ペイロード」と呼び、[デバッグ](../Page/デバッグ.md "wikilink")のために、出力がqNaNとなった操作で1つ目のqNaNの引数のペイロードをそのまま伝播させることを推奨している。

## NA

紛らわしい言葉として、[NA](https://ja.wikipedia.org/wiki/n/a#NA "wikilink")(Not Availableの略、N/Aとも表記される)がある。「数表のコラムにデータが存在しない場合」に使われ『欠損値』（missing value）と訳される。 殊に統計計算の分野、[R言語](../Page/R言語.md "wikilink")など統計解析ソフトウェアで用いられる。R言語では、NaN==NaNの結果が偽なのに対し、NA==NAの結果はNAである。

## 脚注

## 外部リンク

  - [Not-a-Number](http://foldoc.org/?Not-a-Number) FOLDOC
  - [IEEE 754-2008 Standard for Floating-Point Arithmetic](http://ieeexplore.ieee.org/servlet/opac?punumber=4610933) （ログインが必要、有償）

[Category:コンピュータの算術](https://ja.wikipedia.org/wiki/Category:コンピュータの算術 "wikilink") [Category:プログラミング言語の構文](https://ja.wikipedia.org/wiki/Category:プログラミング言語の構文 "wikilink") [Category:コンピュータのエラー](https://ja.wikipedia.org/wiki/Category:コンピュータのエラー "wikilink")

1.  Bowman, Kenneth (2006) An introduction to programming with IDL: Interactive Data Language. Academic Press. p. 26 ISBN 0-12-088559-X
2.  William H. Press, Saul A. Teukolsky, William T. Vetterling (2007) Numerical recipes: the art of scientific computing.p. 34 Cambridge University Press, ISBN 0-521-88068-8
3.
4.  [NaN 'toolbox'](http://pub.ist.ac.at/~schloegl/matlab/NaN/)
5.
6.
7.