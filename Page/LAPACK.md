> この記事は[LAPACK](https://ja.wikipedia.org/wiki/LAPACK)から翻訳されています。


**LAPACK** (Linear Algebra PACKage) [数値線形代数](https://ja.wikipedia.org/wiki/数値線形代数 "wikilink")のための[数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")で、[線型方程式や](../Page/線型方程式系.md "wikilink")[線型最小二乗問題](../Page/最小二乗法.md "wikilink")、[固有値](../Page/固有値.md "wikilink")問題、[特異値問題等を数値的に解くために利用される](../Page/特異値分解.md "wikilink")。本ライブラリは[複素数](../Page/複素数.md "wikilink")または[実数](../Page/実数.md "wikilink")を成分とする行列を扱うことが可能であり、[LU分解](../Page/LU分解.md "wikilink")や[コレスキー分解](../Page/コレスキー分解.md "wikilink")、[QR分解](../Page/QR分解.md "wikilink")、[シュア分解](https://ja.wikipedia.org/wiki/シュア分解 "wikilink")等の[行列の分解](https://ja.wikipedia.org/wiki/行列の分解 "wikilink")を行うための[サブルーチン](../Page/サブルーチン.md "wikilink")を含む。サブルーチンは[単精度](https://ja.wikipedia.org/wiki/単精度 "wikilink")版と[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")版が提供される。のLAPACKの初版は[FORTRAN 77](https://ja.wikipedia.org/wiki/FORTRAN#FORTRAN_77 "wikilink") で実装されていたが、現在は[Fortran 90が用いられている](https://ja.wikipedia.org/wiki/FORTRAN#Fortran_90 "wikilink")。LAPACK 3.4.0からはC言語インターフェースであるLAPACKEが統合され、[C言語](../Page/C言語.md "wikilink")や[C++](../Page/C++.md "wikilink")からの利用が容易になった。

LAPACKは[LINPACK](../Page/LINPACK.md "wikilink")および[EISPACK](https://ja.wikipedia.org/wiki/EISPACK "wikilink")の後継と見做されている。ただし、LINPACKの設計が開発当時近代的であった共有メモリ型[ベクトルコンピュータを意識したものであるのに対して](../Page/ベクトル計算機.md "wikilink")、本ライブラリの設計は[キャッシュを用いた](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")[アーキテクチャを有する](../Page/コンピュータ・アーキテクチャ.md "wikilink")、より近代的なコンピュータを意識したものである。LAPACKはLINPACK同様に[BLAS](https://ja.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms "wikilink")（Basic Linear Algebra Subprograms、基本線型代数サブプログラム群）ライブラリ上に構築されている。LAPACKは後に分散メモリ型のコンピュータ向けにやへと拡張された。

LAPACKは[BSDライセンス](../Page/BSDライセンス.md "wikilink")で提供される[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアである。

## サブルーチン

### 構成

LAPACKのサブルーチンは以下の三種類に大別される。

  - ドライバルーチン（driver routines）:LAPACKが扱うことが可能な問題を解くためのルーチン。 問題の例として[線型方程式系](../Page/線型方程式系.md "wikilink")を解く問題や[対称行列](../Page/対称行列.md "wikilink")の[固有値](../Page/固有値.md "wikilink")問題などが挙げられる。利用者の要請に合致する機能のドライバルーチンが存在する場合にはそのルーチンの利用が推奨される。
    計算ルーチン（computational routines）: 問題を解くために必要な計算タスクを実行するためのルーチン。LAPACKのドライバルーチンは計算ルーチンを連続的に呼び出すことで問題を解く。計算タスクの例として行列を[LU分解](../Page/LU分解.md "wikilink")することや[対称行列](../Page/対称行列.md "wikilink")を[三重対角行列](https://ja.wikipedia.org/wiki/三重対角行列 "wikilink")に変換することなどが挙げられる。前者は線型方程式系を解くために、そして後者は対称行列の固有値問題を解くために必要である。利用者の要請に合致するドライバルーチンが存在しない場合は計算ルーチンを組み合わせて問題を解くことになる。
    補助ルーチン（auxiliary routines）: 補助的に利用されるルーチン。ブロックアルゴリズム内部で利用される計算タスクの一部を実行するものや、[BLASの機能をわずかに拡張したものが含まれる](https://ja.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms "wikilink")。

### 命名規則

LAPACKとBLASのサブルーチンの名称は機能の判別が平易である範囲で短くなるような規則で命名されている。 これは初期のFORTRANにおける関数の名称に関する[仕様上の制限を受けたものである](https://ja.wikipedia.org/wiki/FORTRAN#.E5.88.9D.E6.9C.9F_.28FORTRAN_66.29 "wikilink")。

サブルーチンは`pmmaaa`の規則で命名される。 以下、LAPACKの`DGESV`（倍精度一般行列の方程式系の求解）とBLASの`DGEMM`（倍精度行列の積の計算）を例に挙げる。

  - `p`は通常は一文字の英字で数値データの型を表現するために利用される\[1\]。`S`と`D`はそれぞれ単精度と倍精度の実数を意味し、`C`と`Z`はそれぞれ単精度と倍精度の複素数を意味する。なお、一文字目を別の文字に置き換えてサブルーチンの名称を記述することがある\[2\]。ただし、サブルーチンが採用するアルゴリズムによっては例外が存在することに注意が必要である\[3\]。
  - `mm`は二文字の英字でサブルーチンが採用するアルゴリズムが想定する行列の型を意味する。行列の型を現す略号は以下に表で示す。サブルーチンが想定する行列データの格納方法は型ごとに異なる。例えば、[対角行列](../Page/対角行列.md "wikilink")を意味する`DI`が与えられた場合は対角要素が格納された長さの配列を、一般行列を意味する`GE`が与えられた場合は行列の要素が格納されたの配列という具合いである。
  - `aaa`は一文字から三文字の英数字でサブルーチンの処理内容を表現する。例えば`SV`は線型方程式系の求解を意味し、`MM`は行列の積を意味する。

<table>
<caption>LAPACKの命名規則における行列の型</caption>
<thead>
<tr class="header">
<th><p>略号</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BD</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>DI</p></td>
<td><p><a href="../Page/対角行列.md" title="wikilink">対角行列</a></p></td>
</tr>
<tr class="odd">
<td><p>GB</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>GE</p></td>
<td><p>一般行列</p></td>
</tr>
<tr class="odd">
<td><p>GG</p></td>
<td><p>一般行列、一般化された問題（一般行列の対）</p></td>
</tr>
<tr class="even">
<td><p>GT</p></td>
<td><p>一般<a href="https://ja.wikipedia.org/wiki/三重対角行列" title="wikilink">三重対角行列</a></p></td>
</tr>
<tr class="odd">
<td><p>HB</p></td>
<td><p><a href="../Page/エルミート行列.md" title="wikilink">エルミート</a></p></td>
</tr>
<tr class="even">
<td><p>HE</p></td>
<td><p><a href="../Page/エルミート行列.md" title="wikilink">エルミート行列</a></p></td>
</tr>
<tr class="odd">
<td><p>HG</p></td>
<td><p>上、一般化された問題（ヘッセンベルグ行列と<a href="https://ja.wikipedia.org/wiki/三角行列" title="wikilink">三角行列</a>）</p></td>
</tr>
<tr class="even">
<td><p>HP</p></td>
<td><p><a href="../Page/エルミート行列.md" title="wikilink">エルミート行列</a>、</p></td>
</tr>
<tr class="odd">
<td><p>HS</p></td>
<td><p>上</p></td>
</tr>
<tr class="even">
<td><p>OP</p></td>
<td><p><a href="../Page/直交行列.md" title="wikilink">直交行列</a>、</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p><a href="../Page/直交行列.md" title="wikilink">直交行列</a></p></td>
</tr>
<tr class="even">
<td><p>PB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/対称行列#.E6.AD.A3.E5.80.A4.E5.AF.BE.E7.A7.B0.E8.A1.8C.E5.88.97" title="wikilink">正値対称</a> または <a href="https://ja.wikipedia.org/wiki/エルミート行列#.E6.AD.A3.E5.80.A4.E3.82.A8.E3.83.AB.E3.83.9F.E3.83.BC.E3.83.88.E8.A1.8C.E5.88.97" title="wikilink">正値エルミート</a></p></td>
</tr>
<tr class="odd">
<td><p>PO</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/対称行列#.E6.AD.A3.E5.80.A4.E5.AF.BE.E7.A7.B0.E8.A1.8C.E5.88.97" title="wikilink">正値対称行列</a> または <a href="https://ja.wikipedia.org/wiki/エルミート行列#.E6.AD.A3.E5.80.A4.E3.82.A8.E3.83.AB.E3.83.9F.E3.83.BC.E3.83.88.E8.A1.8C.E5.88.97" title="wikilink">正値エルミート行列</a></p></td>
</tr>
<tr class="even">
<td><p>PP</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/対称行列#.E6.AD.A3.E5.80.A4.E5.AF.BE.E7.A7.B0.E8.A1.8C.E5.88.97" title="wikilink">正値対称行列</a> または <a href="https://ja.wikipedia.org/wiki/エルミート行列#.E6.AD.A3.E5.80.A4.E3.82.A8.E3.83.AB.E3.83.9F.E3.83.BC.E3.83.88.E8.A1.8C.E5.88.97" title="wikilink">正値エルミート行列</a>、</p></td>
</tr>
<tr class="odd">
<td><p>PT</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/対称行列#.E6.AD.A3.E5.80.A4.E5.AF.BE.E7.A7.B0.E8.A1.8C.E5.88.97" title="wikilink">正値対称</a><a href="https://ja.wikipedia.org/wiki/三重対角行列" title="wikilink">三重対角行列</a> または <a href="https://ja.wikipedia.org/wiki/エルミート行列#.E6.AD.A3.E5.80.A4.E3.82.A8.E3.83.AB.E3.83.9F.E3.83.BC.E3.83.88.E8.A1.8C.E5.88.97" title="wikilink">正値エルミート</a><a href="https://ja.wikipedia.org/wiki/三重対角行列" title="wikilink">三重対角行列</a></p></td>
</tr>
<tr class="even">
<td><p>SB</p></td>
<td><p><a href="../Page/対称行列.md" title="wikilink">対称</a></p></td>
</tr>
<tr class="odd">
<td><p>SP</p></td>
<td><p><a href="../Page/対称行列.md" title="wikilink">対称行列</a>、</p></td>
</tr>
<tr class="even">
<td><p>ST</p></td>
<td><p><a href="../Page/対称行列.md" title="wikilink">対称</a><a href="https://ja.wikipedia.org/wiki/三重対角行列" title="wikilink">三重対角行列</a></p></td>
</tr>
<tr class="odd">
<td><p>SY</p></td>
<td><p><a href="../Page/対称行列.md" title="wikilink">対称行列</a></p></td>
</tr>
<tr class="even">
<td><p>TB</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/三重対角行列" title="wikilink">三重対角行列</a></p></td>
</tr>
<tr class="odd">
<td><p>TG</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/三角行列" title="wikilink">三角行列</a>、一般化された問題（三角行列の対）</p></td>
</tr>
<tr class="even">
<td><p>TP</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/三角行列" title="wikilink">三角行列</a>、</p></td>
</tr>
<tr class="odd">
<td><p>TR</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/三角行列" title="wikilink">三角行列</a>（または準三角行列）</p></td>
</tr>
<tr class="even">
<td><p>TZ</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>UN</p></td>
<td><p><a href="../Page/ユニタリ行列.md" title="wikilink">ユニタリ行列</a></p></td>
</tr>
<tr class="even">
<td><p>UP</p></td>
<td><p><a href="../Page/ユニタリ行列.md" title="wikilink">ユニタリ行列</a>、</p></td>
</tr>
</tbody>
</table>

命名規則の詳細はLAPACK Users' Guideの当該項目\[4\]を参照。

## 実装

LAPACKにはサブルーチンの機能とインターフェースに互換性のある実装が多く存在する。

以下に例を示す。それぞれの動作環境についてはリンク先を参照。

  - [ACML (AMD Core Math Library)](http://developer.amd.com/acml.aspx): [AMDによる実装](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")。
  - [Accelerateフレームワーク](http://developer.apple.com/jp/documentation/MacOSX/Conceptual/universal_binary/universal_binary_vector/chapter_6_section_2.html): [アップルによる実装](../Page/アップル_\(企業\).md "wikilink")。
  - [HP MLIB](http://h21007.www2.hp.com/portal/site/dspp/menuitem.863c3e4cbcdc3f3515b49c108973a801?ciid=4308852bcbe02110852bcbe02110275d6e10RCRD): [ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")による実装。
  - [ESSL (Engineering and Scientific Subroutine Library)](http://publib.boulder.ibm.com/infocenter/clresctr/index.jsp?topic=/com.ibm.cluster.essl.doc/esslbooks.html): [IBM](../Page/IBM.md "wikilink")による実装。
  - [Intel Math Kernel Library](https://ja.wikipedia.org/wiki/Intel_Math_Kernel_Library "wikilink"): [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")による実装。
  - [MathKeisan](http://www.mathkeisan.com/): [日本電気](../Page/日本電気.md "wikilink")による実装。
  - [SCSL (Scientific Computing Software Library)](http://www.sgi.com/products/software/irix/scsl.html): [SGIによる実装](../Page/シリコングラフィックス.md "wikilink")。
  - [Sun Performance Linaray](http://developers.sun.com/sunstudio/overview/topics/perflib_index.html): [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")による実装。

## LAPACKと言語バインディング

LAPACKはFortran 90以外のプログラミング言語から利用することが可能であり、これを目的とした[言語バインディングのためのライブラリも開発されている](../Page/束縛_\(情報工学\).md "wikilink")。LAPACK 3.4.0よりC言語インターフェースであるLAPACKEが統合された。

以下に例を示す。

  - [LAPACK95](http://www.netlib.org/lapack95/): Fortran 95用。インターフェースが簡略化される。
  - [CLAPACK](http://www.netlib.org/clapack/): [C言語](../Page/C言語.md "wikilink")用。Fortran版をによって変換したもの。
  - [LAPACKE](http://www.netlib.org/lapack/#_standard_c_language_apis_for_lapack): [C言語](../Page/C言語.md "wikilink")用。インテルの[Math Kernel Library互換のC言語インターフェース](https://ja.wikipedia.org/wiki/Math_Kernel_Library "wikilink")。
  - [LAPACK++](http://math.nist.gov/lapack++/): [C++](../Page/C++.md "wikilink")用。
  - [Armadillo](http://arma.sourceforge.net/): [C++](../Page/C++.md "wikilink")用。
  - [CPPLAPACK](http://cpplapack.sourceforge.net/doc/main_page/Japanese.html): [C++](../Page/C++.md "wikilink")用。
  - [Boost Numeric Bindings](http://mathema.tician.de/software/boost-bindings): [C++](../Page/C++.md "wikilink")用。
  - [SciPy](http://www.scipy.org/Installing_SciPy/BuildingGeneral): [Python](../Page/Python.md "wikilink")用。
  - [jlapack](http://www.netlib.org/java/f2j/): [Java](https://ja.wikipedia.org/wiki/Java "wikilink")用。
  - [CSLapack](http://www.dotnumerics.com/NumericalLibraries/LinearAlgebra/CSLapack/): [C\#](https://ja.wikipedia.org/wiki/C# "wikilink")用。
  - [Linalg](http://rubyforge.org/projects/linalg/): [Ruby](../Page/Ruby.md "wikilink")用。
  - [LACAML](http://www.ocaml.info/home/ocaml_sources.html#lacaml): [OCaml](../Page/OCaml.md "wikilink")用。
  - [hmatrix](http://hackage.haskell.org/package/hmatrix): [Haskell](../Page/Haskell.md "wikilink")用。
  - Accelerateフレームワーク: [Objective-C](../Page/Objective-C.md "wikilink")用インターフェースが提供される。

### C言語

多くの処理系ではライブラリのC言語バインディングが可能であるため、いくらかの制約があるにせよLAPACKのサブルーチンをC言語の関数のように利用できる。ただし、Fortranコンパイラが存在しない処理系ではCLAPACKも有効な選択肢となる。なお、が提供するC言語インターフェース\[5\]も存在するが、これはf2cのCLAPACKとは互換性が無い。

C言語では慣用のrow-major orderingな行列を計算させる場合、LAPACKEでは指定オプションが用意されている。その場合、内部で[行列転置が行われオーバヘッドが発生する](../Page/転置行列.md "wikilink")。例えば行列積は、内部の計算は下記のように行われる。ここで「\(\cdot\)」はBLAS/LAPACK本来のcolumn-major orderingな行列積を意味している。

  -
    \(C = \left(  A^\textrm{T} \cdot B^\textrm{T}  \right)^\textrm{T}\)

## 脚注

## 関連文献

  - E. Anderson, Z. Bai, C. Bischof, S. Blackford, J. Demmel, J. Dongarra, J. Du Croz, A. Greenbaum, S. Hammarling, A. McKenney, D. Sorensen：”LAPACK Users' Guide (Software, Environments and Tools)”、SIAM、ISBN 978-0898714470（1987年1月1日）。
  - 村田健郎、J.J.ドンガラ、小国力、三好 俊郎、長谷川 秀彦：「行列計算ソフトウェア―WS、スーパーコン、並列計算機」、丸善、ISBN　978-4621036549（1991年12月）。
  - 小国力：「LAPACK利用の手引―行列計算パッケージ」、丸善、ISBN 978-4621040768（1995年7月）。
  - 幸谷智紀：「LAPACK/BLAS入門」、森北出版、ISBN 978-4627848818（2016年12月16日）。

## 関連項目

  - [BLAS](https://ja.wikipedia.org/wiki/BLAS "wikilink")
  - [数値解析ソフトウェア](https://ja.wikipedia.org/wiki/数値解析ソフトウェア "wikilink")

## 外部リンク

  - [LAPACK Users' Guide](http://www.netlib.org/lapack/lug/) 公式サイトのマニュアル
  - [LAWNs (LAPACK Working Notes)](http://www.netlib.org/lapack/lawns/) LAPACKの実装に関する文献集
  - [LAPACKサンプルプログラム集](http://www.nag-j.co.jp/lapack/) [NAGによるサンプルプログラム集](https://ja.wikipedia.org/wiki/Numerical_Algorithms_Group "wikilink")
  - [PLASMA](http://icl.cs.utk.edu/plasma/) Parallel Linear Algebra for Scalable Multi-core Architectures、BLAS上に構築された[ホモジニアスマルチコア向けの線型計算ライブラリ](https://ja.wikipedia.org/wiki/マルチコア#ホモジニアスとヘテロジニアス "wikilink")
  - [CULA](http://www.culatools.com/) [NVIDIA](../Page/NVIDIA.md "wikilink")の[CUDA](../Page/CUDA.md "wikilink")対応[GPU上で動作する線型計算ライブラリ](../Page/Graphics_Processing_Unit.md "wikilink")
  - [MAGMA](http://icl.cs.utk.edu/magma/) Matrix Algebra on GPU and Multicore Architectures、LAPACKのサブセットで[マルチコア](../Page/マルチコア.md "wikilink")[CPU](../Page/CPU.md "wikilink")と[GPUのハイブリッドアーキテクチャ向け](../Page/Graphics_Processing_Unit.md "wikilink")
  - [The MPACK; Multiple precision arithmetic BLAS and LAPACK](http://mplapack.sourceforge.net/) 多倍長精度版のBLAS/LAPACK
  - 「BLAS，LAPACK チュートリアル」 MPACKの開発者によるチュートリアル
      - [パート1 （簡単な使い方とプログラミング）](http://www.jsces.org/Issue/Journal/pdf/nakata-0411.pdf)
      - [パート2 （GPU編）](http://www.jsces.org/Issue/Journal/pdf/nakata-0711.pdf)

[Category:数値解析ソフトウェア](https://ja.wikipedia.org/wiki/Category:数値解析ソフトウェア "wikilink") [Category:数値線形代数](https://ja.wikipedia.org/wiki/Category:数値線形代数 "wikilink") [Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:1992年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1992年のソフトウェア "wikilink") [Category:FORTRAN](https://ja.wikipedia.org/wiki/Category:FORTRAN "wikilink")

1.  ただし、LAPACK95のサブルーチンはデータの型を自動判別するため`LA_GESV`といった名称を持つ。詳細は\[[http://www.netlib.org/lapack95/DOC/la_gesv.txt\]を参照](http://www.netlib.org/lapack95/DOC/la_gesv.txt%5Dを参照)。
2.  例えば、インテルの[Math Kernel Libraryのリファレンスマニュアル](http://software.intel.com/sites/products/documentation/hpc/mkl/mklman/index.htm)では`DGESV`を`?GESV`と表記している。
3.  LAPACK 3.1.1の`DSGESV`は行列の分解を単精度で実行して得た解を反復改良することで倍精度の解を得るために`DS`で始まる名称を持つ。詳細は\[[http://www.netlib.org/lapack/lapack-3.1.1/html/dsgesv.f.html\]を参照](http://www.netlib.org/lapack/lapack-3.1.1/html/dsgesv.f.html%5Dを参照)。
4.  LAPACK Users' Guide, [Naming scheme](http://www.netlib.org/lapack/lug/node24.html)
5.  [ATLAS ANSI/ISO C LAPACK API REFERENCE](http://math-atlas.sourceforge.net/psdoc/lapackqref.ps)を参照。