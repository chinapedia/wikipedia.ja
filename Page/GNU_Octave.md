> この記事は[GNU Octave](https://ja.wikipedia.org/wiki/GNU_Octave)から翻訳されています。


**GNU Octave** は、主に[数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")を目的とした高レベル[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。Octaveは線形ならびに非線形問題を数値的に解くためのコマンドライン·インタフェースを提供する。また、 [MATLAB](../Page/MATLAB.md "wikilink")とほぼ互換性のある、数値実験を行うためのプログラミング言語として使用することができる。 Octaveは、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一つで[GNU General Public Licenseの条件の下の](https://ja.wikipedia.org/wiki/GPL "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。 GNU Octaveと[Scilab](../Page/Scilab.md "wikilink")は、MATLABのオープンソース代替品の一つである。 ただし、Octaveは、ScilabよりもMATLABとの互換性維持に重点を置いている\[1\] \[2\] \[3\] \[4\] \[5\] \[6\]。

## 開発の経緯

開発が始まったのは1988年ごろである。当初は化学反応器設計の授業で使うために作られたが、その後1992年から、ジョン・イートン ([John W. Eaton](https://ja.wikipedia.org/wiki/:en:John_W._Eaton "wikilink")) が開発を始めた。彼による最初のアルファ版のリリースは1993年1月4日で、正式版 (ver. 1.0) は翌年、1994年2月17日にリリースされた。2007年12月21日にバージョン3.0が、2015年5月29日にはバージョン4.0がリリースされた。

**Octave**という名前は、イートンの指導教官であり、裏紙にでも軽く書いてやるような概算の計算 ([back-of-the-envelope calculation](https://ja.wikipedia.org/wiki/:en:back-of-the-envelope_calculation "wikilink")) が速かった元[オレゴン州立大学](../Page/オレゴン州立大学.md "wikilink")教授のオクターブ・レヴェンシュピール（[Octave Levenspiel](https://ja.wikipedia.org/wiki/:en:Octave_Levenspiel "wikilink")、[反応工学](https://ja.wikipedia.org/wiki/反応工学 "wikilink")）にちなむ\[7\]。

当初の目的である個人的な計算機としての利用に加え、Octaveは学術的及び工業的な用途にも使われている。例えば米国ピッツバーグ・スーパーコンピューティング・センター (Pittsburgh supercomputing center) では大規模[並列計算](../Page/並列計算.md "wikilink")による[社会保障番号](../Page/社会保障番号.md "wikilink")の攻撃に対する脆弱性検証に、Octaveを使っている\[8\]。

[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")は永らく[CUIのみであったが](../Page/キャラクタユーザインタフェース.md "wikilink")、3.8.0からは[GUIが搭載された](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")\[9\]。

## 特徴

  - MATLAB 互換のプログラミング言語の[インタプリタ](../Page/インタプリタ.md "wikilink")を実装しており、また[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")の開発環境がそろっている。
  - [C++](../Page/C++.md "wikilink")と[STLを用いている](../Page/Standard_Template_Library.md "wikilink")。
  - Mex-fileならびにOct-fileとよばれる仕組みを用いて、C/C++言語で記述された自作関数によりOctaveを拡張可能である。
  - Octave 4.0からグラフィックは[gnuplot](https://ja.wikipedia.org/wiki/gnuplot "wikilink") から[OpenGL](../Page/OpenGL.md "wikilink") graphics with [Qt](../Page/Qt.md "wikilink") widgetsへ変更された。
  - Octaveは行列計算で[BLAS](https://ja.wikipedia.org/wiki/BLAS "wikilink")を呼び出しているため高速かつ信頼性が高い。
  - Octave 4.0から[OpenMP](../Page/OpenMP.md "wikilink")がデフォルトで有効になっており、システムにOpenMPが実装されている場合、計算の高速化が期待できる。

### 計算機言語としての Octave

Octaveを操作するための命令系統は、[計算機言語でもある](../Page/プログラミング言語.md "wikilink")。Octaveは[C言語](../Page/C言語.md "wikilink")のような構造化言語であり、C言語の[標準ライブラリ](https://ja.wikipedia.org/wiki/標準ライブラリ "wikilink")に含まれる多くの関数がOctaveでも実装されている。また[UNIXの](../Page/POSIX.md "wikilink")[システムコール](../Page/システムコール.md "wikilink")もいくつか利用できる\[10\]。しかし関数呼び出しの際の、引き数値の参照渡しはサポートされていない \[11\]。

Octave言語で書かれたプログラムは、関数呼び出しの並びで構成されるスクリプトである。その文法は行列計算が基本であり、スクリプトにおいては行列計算の演算子が多数利用できる。多種多様な[データ構造](../Page/データ構造.md "wikilink")を利用できる他，3.2以降のバージョンでは，[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")プログラミング機能が付加された。

Octaveの文法はMATLABのものと非常によく似ており、少し注意してプログラミングすることでOctaveとMATLABの両方で実行できるスクリプトを書くことができる\[12\]。

Octaveは[GNU General Public Licenseによって公開されているため](../Page/GNU_General_Public_License.md "wikilink")、その改変、複製、利用は自由である\[13\]。Octaveは多くの [UNIX](../Page/UNIX.md "wikilink")や[Unix系](../Page/Unix系.md "wikilink")の[プラットフォーム](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") で実行できる\[14\]。

### 関数名、変数名の補完

対話的に実行中のOctaveのコマンドラインでタブを入力すると、関数名、変数名、ファイル名の入力を補完する（[Bash](../Page/Bash.md "wikilink")の[タブ補完](https://ja.wikipedia.org/wiki/タブ補完 "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Command-line_completion "wikilink")) と同様の機能）。その時点でカーソルの直前に入力されているテキストを補完する。

### ヒストリ機能

対話的に実行中のOctaveでは、それまでに入力されたコマンドラインが保存されており、必要に応じて修正して再実行できる。

### データ構造

Octaveではユーザーがデータ構造をある程度定義できる。たとえばスカラー、行列、文字列の変数を持つ構造体を以下のようにして定義できる。

    octave:1> x.a = 1; x.b = [1, 2; 3, 4]; x.c = "string";
    octave:2> x.a
    ans =  1
    octave:3> x.b
    ans =

       1   2
       3   4

    octave:4> x.c
    ans = string
    octave:5> x
    x =
    {
      a =  1
      b =

         1   2
         3   4

      c = string
    }

### 条件判定のショートカット

Octaveで条件判定に使われる論理演算の二項[演算子](../Page/演算子.md "wikilink")、'`&&`' および '`||`' が評価されるときには、[短絡評価](../Page/短絡評価.md "wikilink")が行われる（C言語の場合と同様）。一方、条件判定に '`&`' および '`|`' 演算子を使った場合は短絡評価は行われない。

### インクリメントおよびデクリメント演算子

OctaveにはC言語と同様の '`++`' および '`--`' 演算子があり、やはりC言語と同様に変数の前及び後ろに置くことができる。変数値の増減後に代入を行う '`+=`' および '`-=`' 演算子もある。

### Unwind-protect

Octaveでは[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の '`unwind_protect`'\[15\]を実装しており、それによる[例外処理](../Page/例外処理.md "wikilink")を記述することができる。unwind_protectブロックはOctaveでは以下のように書かれる。

``` octave
unwind_protect
   body
unwind_protect_cleanup
   cleanup
end_unwind_protect
```

Octaveでは一般的に、ブロックの終端は '`end`' キーワードで示される（MATLAB と互換である）が、'`end_`*`block`*' でも示すことができる。'`unwind_protect`' ブロックでも '`end`' に加えて '`end_unwind_protect`' を使うことができる。

unwind_protectの*cleanup*部は、常に実行される。*body*部で例外が発生した場合は、その時点で*cleanup*が実行され、 '`unwind_protect`' ブロックの残りの部分が評価されることはない。

Octaveでは他の例外処理も使える（MATLAB との互換性を持たせるため）。

``` octave
try
   body
catch
   exception_handling
end
```

この '`try`' と '`catch`' を使う例では '`unwind_protect`' ブロックと違い、例外が*body*部で発生したときにのみ*exception_handling*が実行される。また*exception_handling*の実行後は、 '`rethrow( lasterror )`' 文が*exception_handling*部に記述されていない限りは、'`try`' ブロックの例外発生場所以降の部分が評価されることはない。

### 個数が可変の引数

Octaveでは関数の引数について、その個数の上限を指定することなく可変としておくことができる。引数が0個以上であることを指定するには、`varargin`を引数として指定する。`varargin`は、引数リストの最後に置くか、または唯一の引数として指定する。

``` octave
function s = plus (varargin)
   if (nargin==0)
      s = 0;
   else
      s = varargin{1} + plus (varargin{2:nargin});
   end
end
```

### 個数が可変の返り値

Octaveの関数は、`varargout`を使うことで返り値の数が実行時に決まるように記述できる。

``` octave
function varargout = multiassign (data)
   for k=1:nargout
      varargout{k} = data(:,k);
   end
end
```

### C++との統合

C++ソースプログラムの中から直接、Octave の関数を呼ぶことができる。以下の例では、`rand([10,1])`というOctaveの関数呼び出しをC++のプログラムの中から行っている。

``` cpp
#include <octave/oct.h>
...
ColumnVector NumRands(2);
NumRands(0) = 10;
NumRands(1) = 1;
octave_value_list f_arg, f_ret;
f_arg(0) = octave_value(NumRands);
f_ret = feval("rand",f_arg,1);
Matrix unis(f_ret(0).matrix_value());
```

## MATLAB との互換性

Octaveは、MATLABとの互換性を主に目指しており、MATLABの機能の多くをOctaveも持っている。またMATLABのために書かれたプログラムも修正せずに動作するものが多い。

1.  行列を基本のデータ形式にしている
2.  複素数に対応
3.  強力なbuild-in関数と、ライブラリを持つ
4.  ユーザ定義関数によって拡張可能

MATLABとOctaveの相異点については、オフィシャル・サイトのFAQにまとめられている\[16\]が、以下のようなものがある。

1.  行頭に % の他に \# を置いても、その行をコメントとすることができる
2.  \++, --, +=, \*=, /= などの[C言語](../Page/C言語.md "wikilink")の演算子が使える
3.  \[1:10\](3) などのように、変数 (インスタンス) を生成しなくても、配列の要素を参照できる
4.  ' の他に、" を使っても文字列を定義できる

## 関連項目

  - [数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")
  - 類似のソフトウェア
      - [FreeMat](https://ja.wikipedia.org/wiki/FreeMat "wikilink")
      - [MATLAB](../Page/MATLAB.md "wikilink")
      - [Scilab](../Page/Scilab.md "wikilink")

## 脚注

<references/>

## 参考文献

  - Hansen, Jesper (June 2011). [GNU Octave Beginner's Guide](http://www.packtpub.com/gnu-octave-beginners-guide/book). [Packt Publishing](https://ja.wikipedia.org/wiki/:en:Packt "wikilink").

## 外部リンク

一部を除いて、全て英語のサイトである。

  - [Octave.org Home Page](http://www.octave.org/)
  - [オンライン・マニュアル（英語）](http://www.gnu.org/software/octave/doc/interpreter/index.html) ([旧版2.1.xの日本語訳](http://www.obihiro.ac.jp/~suzukim/masuda/octave/html/))
  - [コミュニティによる開発サイト Octave-forge](http://octave.sourceforge.net/)
  - [Octave wiki](http://wiki.octave.org/) （ブラウザによってはリダイレクトがタイムアウトを生じるので，2回クリックするとよい）
  - [Online access to Octave](http://www.online-utility.org/math/math_calculator.jsp) オンラインでOctaveによる計算を試せる。
  - [Octave - AIMSWiki](http://www.aims.ac.za/wiki/index.php/Octave)
  - [QtOctave un Front-End para Octave](http://web.archive.org/20070427014315/qtoctave.wordpress.com/) - インターフェイスをグライフィカルに拡張したQtOctaveを開発している。
  - [DomainMath IDE](https://sites.google.com/site/domainmathide/home) - GUIフロントエンドを開発している。オープンソース。
  - [MATLAB Central](http://www.mathworks.com/matlabcentral/) MATLABのユーザーコミュニティのサイト。多くの科学技術計算スクリプトが投稿され、ユーザーにより評価されている。MATLABの別売りToolboxを使わないスクリプトは、GNU Octaveでそのまま利用できるものも多い。
  - [Octave Programming Tutorial](http://en.wikibooks.org/wiki/Octave_Programming_Tutorial) WikiBooks プロジェクト内のドキュメント集。

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:Linux向け数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:Linux向け数値解析ソフトウェア "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:Qtを使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:Qtを使用するソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [Social Security Number Vulnerability Findings Relied on Supercomputing](http://www.hpcwire.com/industry/government/Social-Security-Number-Vulnerability-Findings-Relied-on-Supercomputing-50292227.html) HPCwire, July 8, 2009.
9.
10.
11.
12.
13.
14.
15. [CLHS: Special Operator UNWIND-PROTECT](http://www.lispworks.com/documentation/HyperSpec/Body/s_unwind.htm) Common Lisp Hyper Specのサイトでの解説（英語）
16. [How is Octave different from Matlab? 互換性に関するFAQ](http://www.octave.org/wiki/index.php?title=FAQ#How_is_Octave_different_from_Matlab.3F)