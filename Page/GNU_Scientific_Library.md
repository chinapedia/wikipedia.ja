> この記事は[GNU Scientific Library](https://ja.wikipedia.org/wiki/GNU_Scientific_Library)から翻訳されています。


**GNU Scientific Library** (**GSL**) は、C言語で記述された[科学技術計算](https://ja.wikipedia.org/wiki/科学技術計算 "wikilink")関数の[ライブラリ](../Page/ライブラリ.md "wikilink")である。[オープンソース](../Page/オープンソース.md "wikilink")であり、[GNU General Public Licenseのもとで配布されている](../Page/GNU_General_Public_License.md "wikilink")。

このプロジェクトは1996年に[ロスアラモス国立研究所](https://ja.wikipedia.org/wiki/ロスアラモス国立研究所 "wikilink")のDr. M. GalassiとDr. J. Theilerの着想に始まり、[計算物理の専門家集団](../Page/計算物理学.md "wikilink")（Dr G. Jungman、Dr B. Gough、Dr J. Davies、R. Priedhorsky、Dr M. Booth、Dr F. Rossi、Dr D. Eddelbuettelら）を中心に作成された。

線形計算については[BLAS](https://ja.wikipedia.org/wiki/BLAS "wikilink")をサポートしており、CBLAS インターフェイスを実装している。

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")をはじめ、[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")OSを中心にサポートしている。[Microsoft Visual Studio用のバイナリもある](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。

参考論文のレファレンス、文献等も充実している (リファレンス・マニュアルには日本語訳がある)。リファレンス・マニュアルにはサンプル・コードも多数収録されている。[PSPP](https://ja.wikipedia.org/wiki/PSPP "wikilink")、[Perl Data Language](https://ja.wikipedia.org/wiki/Perl_Data_Language "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Perl_Data_Language "wikilink"))、O2scl\[1\] などのフリーウェア・プロジェクトでも利用されている。

複素数型やベクトル／行列型などは [ANSI C](../Page/C言語.md "wikilink") で規定されている構造体で実装されており、C++ のクラスではない。そのためたとえば、複素数オブジェクト同士の加算が + 演算子で行えるようになっている訳ではなく、加算のための関数 (この場合 gsl_complex_add) を、二つの複素数オブジェクトを引数として呼ばねばならない。

拡張倍精度以上の精度における計算は、変数の内部表現が言語仕様で標準化されておらず、さらに環境に依存して精度が大きく変化するために対応していない。

## 開発

GSL の開発チームは、GSL が [GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")のパッケージであることを明示しており、GSL のコードはすべて誰もが自由に、どんな用途にでも使えることを保証している。そのために、プロプライエタリなコードや (たとえば 書籍 Numerical Recipes ISBN 4874085601 などの) GNU の定義するフリーソフトウェアに該当しないコードとは対立した開発姿勢をとっている。

2011年現在、年に1〜2回のメンテナンスリリースによるバグ修正対応が基本になっている。一方で[ブロックやスライスといったデータ構造の有用性や](https://ja.wikipedia.org/wiki/ブロック_\(データ\) "wikilink") C++ 対応の是非についての議論も ML 上で行われており、もし議論が収束して開発陣での合意が形成されれば将来のバージョンで反映される可能性があるが、具体的なスケジュールを考慮するような段階ではない。

### C++ サポート

GSL は C 言語ライブラリであるため、[C++](../Page/C++.md "wikilink")のクラスから利用できる。しかしメンバー関数へのポインタは、その型が関数へのポインタとは異なる\[2\]ため、利用できない。関数へのポインタは、静的に定義された関数 (C言語における一般的な関数定義によるもの) に対して利用する必要がある。

C++から GSL を利用するためのラッパーも複数あるが、いずれも不完全であり、どの開発もあまり活発ではないか、停止している。GSL のヘルプ・メイリング・リストの議論\[3\]では、ラッパーを使わなくても普通に関数を呼ぶのに支障はない、ベクトル用にラッパーを作って使っている、線形代数が目的ならEigen\[4\]がある、などの情報が寄せられている。

なお、[Microsoft Visual Studio 2008用にまとめられたパッケージが公開されている](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")\[5\]。

### 他の言語とのバインディング

[FORTRAN](../Page/FORTRAN.md "wikilink") から GSL の各関数を利用するためのインターフェイスが開発中であり、β版がリリースされている\[6\]。またラッパーを自作したい場合の情報も公開されている\[7\]。

[GNU Octave](../Page/GNU_Octave.md "wikilink") から GSL の特殊関数を利用できるパッケージがリリースされている\[8\]。

GSL のホームページ\[9\] に紹介されているもののうち、現在も開発が続いている主な言語バインディングを以下に挙げる。

  - [Java](https://github.com/bytedeco/javacpp-presets/tree/master/gsl)
  - [Perl](http://search.cpan.org/dist/Math-GSL/)
  - [Perl Data Language](http://pdl.perl.org/)
  - [Common LISP](http://common-lisp.net/project/gsll/)
  - [Python](http://pygsl.sourceforge.net/README.html)
  - [Ruby](http://rubyforge.org/projects/rb-gsl/)
  - [GNU R](http://cran.r-project.org/web/packages/gsl/index.html)
  - [OCaml](http://oandrieu.nerim.net/ocaml/)

## プログラム例

[ベッセル関数](https://ja.wikipedia.org/wiki/ベッセル関数 "wikilink")の値を計算する C プログラムの例を以下に示す\[10\]。

``` c
#include <stdio.h>
#include <gsl/gsl_sf_bessel.h>

int main(void)
{
  double x = 5.0;
  double y = gsl_sf_bessel_J0(x);
  printf("J0(%g) = %.18e\n", x, y);
  return 0;
}
```

[GNU Make](https://ja.wikipedia.org/wiki/GNU_Make "wikilink") を使って上のプログラムをコンパイルし、GSL とリンクしようとする場合、そのコマンドは Makefile ファイル中では以下のようになる。

    gcc $(gsl-config --cflags) example.c $(gsl-config --libs)

上のコマンドで生成された実行ファイルを実行すると、以下のように出力する。計算値の精度は倍精度実数である。

    J0(5) = -1.775967713143382920e-01

## 提供する機能

  - [複素数](../Page/複素数.md "wikilink") (Complex Numbers)
  - [多項式の求根](https://ja.wikipedia.org/wiki/零点 "wikilink") (Roots of Polynomials)
  - [特殊関数](https://ja.wikipedia.org/wiki/特殊関数 "wikilink") (Special Functions)
  - [ベクトル](https://ja.wikipedia.org/wiki/ベクトル "wikilink")・[行列](https://ja.wikipedia.org/wiki/行列_\(数学\) "wikilink") (Vectors and Matrices)
  - [置換](../Page/対称群.md "wikilink") (Permutations)
  - [組み合わせ](../Page/組合せ_\(数学\).md "wikilink") (Combinations)
  - [多重集合](../Page/多重集合.md "wikilink") (Multisets)
  - [整列](https://ja.wikipedia.org/wiki/整列 "wikilink")（Sorting)
  - [BLAS](https://ja.wikipedia.org/wiki/BLAS "wikilink")サポート (BLAS Support)
  - [線形代数](https://ja.wikipedia.org/wiki/線形代数 "wikilink") (Linear Algebra)
  - [固有値問題](https://ja.wikipedia.org/wiki/固有値問題 "wikilink") (Eigensystems)
  - [高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink") (Fast Fourier Transforms)
  - [数値積分](https://ja.wikipedia.org/wiki/数値解析#積分 "wikilink") (Quadrature)
  - [乱数](https://ja.wikipedia.org/wiki/乱数 "wikilink") (Random Numbers)
  - [準乱数列](https://ja.wikipedia.org/wiki/準乱数列 "wikilink") (Quasi-Random Sequences、[超一様分布列](https://ja.wikipedia.org/wiki/超一様分布列 "wikilink")の事)
  - [乱数分布](../Page/確率分布.md "wikilink") (Random Distributions)
  - [統計計算](https://ja.wikipedia.org/wiki/統計量 "wikilink") (Statistics)
  - [ヒストグラム](../Page/ヒストグラム.md "wikilink") (Histograms)
  - [N-Tuples](https://ja.wikipedia.org/wiki/タプル "wikilink")
  - [モンテカルロ積分](../Page/モンテカルロ法.md "wikilink") (Monte Carlo Integration)
  - [焼きなまし法](https://ja.wikipedia.org/wiki/焼きなまし法 "wikilink") (Simulated Annealing)
  - [微分方程式](https://ja.wikipedia.org/wiki/数値解析#微分方程式 "wikilink") (Differential Equations)
  - [補間](https://ja.wikipedia.org/wiki/補間 "wikilink") (Interpolation)
  - [数値微分](https://ja.wikipedia.org/wiki/数値解析#微分 "wikilink") (Numerical Differentiation)
  - [チェビシェフ近似](https://ja.wikipedia.org/wiki/チェビシェフ多項式 "wikilink") (Chebyshev Approximation)
  - 数列収束の加速 (Series Acceleration)
  - 離散[ハンケル変換](https://ja.wikipedia.org/wiki/ハンケル変換 "wikilink") (Discrete Hankel Transforms)
  - [一元および多次元の方程式の求根](https://ja.wikipedia.org/wiki/数値解析#方程式、方程式系の解 "wikilink") (Root-Finding)
  - [一次元及び多次元空間での非線形最小化問題](../Page/最適化問題.md "wikilink") (Minimization)
  - [最小二乗フィッティング](../Page/最小二乗法.md "wikilink") (Least-Squares Fitting)
  - [物理定数](../Page/物理定数.md "wikilink") (Physical Constants)
  - [IEEE浮動小数点の操作](https://ja.wikipedia.org/wiki/IEEE_754 "wikilink") (IEEE Floating-Point)
  - [離散ウェーブレット変換](../Page/離散ウェーブレット変換.md "wikilink") (Discrete Wavelet Transforms)
  - [B-スプライン曲線](https://ja.wikipedia.org/wiki/B-スプライン曲線 "wikilink") (Basis Splines)
  - [疎行列](../Page/疎行列.md "wikilink")およびその線形代数 (Sparse Matrices and Linear Algebra)

## 関連項目

  - [数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")
  - [アルゴリズム](../Page/アルゴリズム.md "wikilink")
  - [計算科学](https://ja.wikipedia.org/wiki/計算科学 "wikilink")
  - [シミュレーション](../Page/シミュレーション.md "wikilink")
  - [数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")
  - [Netlib](https://ja.wikipedia.org/wiki/Netlib "wikilink") (数値計算ソフトウェアのリポジトリ、有益なプログラムが多数公開されている一方で、ライセンスが明確でないものが多く含まれている)
  - [FFTW](https://ja.wikipedia.org/wiki/FFTW "wikilink") ([FFTライブラリ](../Page/高速フーリエ変換.md "wikilink")、より高速なライブラリとして紹介されている)
  - [ATLAS](https://ja.wikipedia.org/wiki/ATLAS_\(数値演算ライブラリ\) "wikilink") (行列計算ライブラリ、同上)
  - [GLPK](https://ja.wikipedia.org/wiki/GNU_Linear_Programming_Kit "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:GNU_Linear_Programming_Kit "wikilink")、線形プログラミングのパッケージ、同上)
  - NLopt (非線形数値最適化パッケージ、同上)
  - [GNU plotutils](https://ja.wikipedia.org/wiki/GNU_plotutils "wikilink") (GSL のマニュアル中で、[gnuplot](https://ja.wikipedia.org/wiki/gnuplot "wikilink") の代わりに利用が推奨されている)

## 脚注

<references/>

## 関連書籍

  - Mark Galassi, Jim Davies, James Theiler, Brian Gough, Gerard Jungman, Michael Booth, Fabrice Rossi (2001). *Gnu Scientific Library Reference Manual*, (English), Network Theory Ltd. ISBN 978-0-9541617-0-5 .

## 外部リンク

  - [GSL - GNU Scientific Library](http://www.gnu.org/software/gsl/) GNU Project - Free Software Foundation (FSF) (英語)
  - [オンライン・マニュアル](http://www.gnu.org/software/gsl/manual/html_node/) (英語)
  - [GSL リファレンス・マニュアル](http://cbrc3.cbrc.jp/~tominaga/translations/gsl/) (日本語訳、PDF、LaTeX ソース)
  - [gsl-discuss](http://sourceware.org/ml/gsl-discuss/) 開発者用メイリング・リスト

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:数学ライブラリー](https://ja.wikipedia.org/wiki/Category:数学ライブラリー "wikilink") [Category:数値計算ライブラリー](https://ja.wikipedia.org/wiki/Category:数値計算ライブラリー "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [1](http://o2scl.sourceforge.net/)
2.  [pointer to member function (英語)](http://www.parashift.com/c++-faq-lite/pointers-to-members.html#faq-33.1)
3.  [C++ラッパーの有無に関する質問と返答 (英語)](http://lists.gnu.org/archive/html/help-gsl/2010-04/msg00048.html)
4.  [Eigen ホームページ (英語)](http://eigen.tuxfamily.org/index.php?title=Main_Page)
5.  [GSL Visual Studio 移植版](http://david.geldreich.free.fr/dev.html)
6.  <http://www.lrz-muenchen.de/services/software/mathematik/gsl/fortran/index.html> FGSL: A Fortran interface to the GNU Scientific Library (英語)\][FGSL 原著論文 (英語)](http://delivery.acm.org/10.1145/1280000/1279942/p4-bader.pdf?key1=1279942&key2=1922105721&coll=GUIDE&dl=GUIDE&CFID=89882829&CFTOKEN=27952890)
7.  [Fortranでgsl (日本語)](http://ckpmac7.yz.yamagata-u.ac.jp/user/murasima/pukiwiki/index.php?Fortran%A4%C7gsl)
8.  [GNU Octave の \`gsl' パッケージ](http://octave.sourceforge.net/gsl/index.html)
9.  [GSL のホームページ (英語)](http://www.gnu.org/software/gsl/)
10. [オンライン・マニュアル中のサンプル・プログラム](http://www.gnu.org/software/gsl/manual/html_node/An-Example-Program.html)