> この記事は[OpenMP](https://ja.wikipedia.org/wiki/OpenMP)から翻訳されています。


**OpenMP**（オープンエムピー）は、[並列計算](../Page/並列計算.md "wikilink")機環境において共有メモリ・[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")型の並列[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")開発をサポートするために標準化されたAPIである\[1\]。「OpenMP」は「open multiprocessing」の略である\[2\]。

同様に並列コンピューティングに利用される[MPIでは](../Page/Message_Passing_Interface.md "wikilink")、メッセージの交換を[プログラム中に明示的に記述しなければならないが](../Page/プログラム_\(コンピュータ\).md "wikilink")、OpenMPでは[ディレクティブ](../Page/ディレクティブ.md "wikilink")を挿入することによって並列化を行う。OpenMPが使用できない環境では、このディレクティブは無視されるため、並列環境と非並列環境でほぼ同一の[ソースコード](../Page/ソースコード.md "wikilink")を使用できるという利点がある。また、プラットフォーム固有の[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink")[APIを使わず](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")、[コンパイラ](../Page/コンパイラ.md "wikilink")によって暗黙的に生成されたスレッドプールを利用してタスクを振り分けることになるため、並列プログラムを簡潔に記述できるだけでなく、複数の環境に移植しやすくなる。

MPIとの比較では、OpenMPは異なる[スレッドが同一のデータを同じアドレスで参照できるのに対して](../Page/スレッド_\(コンピュータ\).md "wikilink")、MPIでは明示的にメッセージ交換を行わなければならない。そのため、OpenMPは、[SMP環境においては大きなデータの移動を行なわずにすむので高い効率が期待できる](../Page/対称型マルチプロセッシング.md "wikilink")。ただし並列化の効率は[コンパイラ](../Page/コンパイラ.md "wikilink")に依存するので、チューニングによる性能改善がMPIほど高くならないという問題がある。また、。

OpenMPは、並列プログラミングにおいて最も広く利用されているAPIであるが、共有メモリに対してに近いアクセスができるハードウェアシステムアーキテクチャでは、スケーラビリティに限界がある\[3\]。そのため、現在のほとんどのスーパーコンピューターでは、OpenMP単独ではなく、分散メモリ環境で高いスケーラビリティを発揮するMPIと組み合わせた、ハイブリッドMPI+OpenMPが利用されている\[4\]\[5\]。

現在[FORTRAN](../Page/FORTRAN.md "wikilink")と[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")について標準化が行われている。

## OpenMPを用いたコード例

以下は[C言語](../Page/C言語.md "wikilink")における for ループを並列処理させる例である。

``` c
int main(int argc, char *argv[])
{
    int i;
#pragma omp parallel for
    for (i = 0; i < 10000; ++i)
    {
        /* (並列処理させたいプログラム) */
    }
    return 0;
}
```

OpenMPはループの反復処理を自動的に複数のスレッドに分割して並行処理できるようにする。例えば4つのスレッドを用いて処理を分割する場合、上記例ではインデックス\[0, 2499\], \[2500, 4999\], \[5000, 7499\], \[7500, 9999\]の各範囲をそれぞれのスレッドに分担させる、といった具合である。実際にいくつのスレッドを起動するのか、また各スレッドに対してどのように処理を振り分けるのかはOpenMP処理系およびプログラム実行環境などの条件に依存する\[6\]。

以下は[区分求積法](https://ja.wikipedia.org/wiki/区分求積法 "wikilink")を用いた[円周率](https://ja.wikipedia.org/wiki/円周率 "wikilink")πの数値計算を、OpenMP並列リダクションによって行なうC++のコード例である。

``` cpp
#include <iostream>
#include <chrono>
#include <cmath>
#include <iomanip>
#include <omp.h>

const double D_PI = 3.1415926535897932384626433832795;

// 区分求積法で π の近似値を求める。
// 1 / (x^2 + 1) を区間 [0, 1] で積分すると π/4 になるという定積分を利用する。

int main()
{
  const int DivNum = 1000 * 1000 * 1000;
  const double delta = 1.0 / DivNum;

  std::cout << "OpenMP max threads count = " << omp_get_max_threads() << std::endl;

  const auto startTime = std::chrono::system_clock::now();
  double sum = 0;
#pragma omp parallel for reduction(+ : sum)
  for (int i = 0; i < DivNum; ++i)
  {
    const double x = (delta * i);
    const double area = delta *  1.0 / (x * x + 1.0);
    sum += area;
  }
  const double pi = sum * 4.0;
  const auto endTime = std::chrono::system_clock::now();
  std::cout << std::setprecision(15) << "PI ~= " << pi << std::endl;
  std::cout << "Error [%] = " << (100.0 * std::fabs(D_PI - pi) / D_PI) << std::endl;
  std::cout << "Elapsed time [ms] = " << std::chrono::duration_cast<std::chrono::milliseconds>(endTime - startTime).count() << std::endl;
  return 0;
}
```

OpenMPコンパイルオプションの有無を切り替えるか、OpenMPディレクティブをコメントアウト／コメント解除してからコンパイル・実行することで、マルチスレッド版およびシングルスレッド版の速度性能比較を簡単に行なうことができるのがOpenMPプログラムの特徴である。

## 対応コンパイラ

  - [GCC](../Page/GNUコンパイラコレクション.md "wikilink")：バージョン4.9時点でOpenMP 4.0をサポートしている\[7\]。GCC 5ではオフロード機能のサポートが追加された。

  - [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")：3.7でOpenMP 3.1に対応した\[8\]。Clang 3.7以前は派生プロジェクトが存在した\[9\]。

  - [Microsoft Visual C++](../Page/Microsoft_Visual_C++.md "wikilink")：Visual C++ 2017時点でOpenMP 2.0をサポートしている\[10\]。Visual C++ 2019では[SIMD](../Page/SIMD.md "wikilink")並列化機能を実験的にサポートする\[11\]。

  - [Intel C++ Compiler](../Page/Intel_C++_Compiler.md "wikilink")：バージョン12.1においてOpenMP 3.1をサポートしている。また、バージョン14.0においてOpenMP 4.0の機能を一部サポートしている\[12\]。

  -
## 脚注

## 関連項目

  - [オープン標準](../Page/オープン標準.md "wikilink")
  - [OpenCL](../Page/OpenCL.md "wikilink")
  - [OpenACC](https://ja.wikipedia.org/wiki/OpenACC "wikilink")
  - [スレッド (コンピュータ)](../Page/スレッド_\(コンピュータ\).md "wikilink")

## 参考文献(学習用)

  - Rohit Chandra, Ramesh Menon, Leo Dagum, David Kohr, Dror Maydan and Jeff McDonald:　"Parallel Programming in OpenMP" , Morgan Kaufmann, ISBN 978-1558606715,(2000年10月).
  - Barbara Chapman，Gabriele Jost and　Ruud Van der Pas: "Using OpenMP: Portable Shared Memory Parallel Programming", ISBN 978-0-262-53302-7, MIT Press, (2007年10月）.
  - Ruud van der Pas, Eric Stotzer and Christian Terboven: "Using OpenMP -- The Next Step: Affinity, Accelerators, Tasking, and SIMD", ISBN 978-0262344005, MIT Press, (2017年10月27日）．※ OpenMP 4.5 の仕様を記述。
  - [OpenMP Architecture Review Board："OpenMP Application Programming Interface Specification Version 5.0",　ISBN 978-1-7311996-0-7 (2018年12月）](https://www.openmp.org/wp-content/uploads/OpenMP-API-Specification-5.0.pdf)。※ OpenMP 5.0 の仕様を記述。
  - Timothy G. Mattson, Yun (Helen) He, and Alice Konigs: "The OpenMP Common Core: Making OpenMP Simple Again", MIT Press, ISBN 978-0262538862 (2019年11月19日)。

<!-- end list -->

  - 牛島 省:「OpenMPによる並列プログラミングと数値計算法」，丸善、ISBN 978-4621077177（2006年5月）。
  - [黒田久泰：「C言語によるOpenMP入門」、東京大学情報基盤センター スーパーコンピューティングニュース、Vol.9, No. Special Issue 1(2008), pp.149-168](https://www.cc.u-tokyo.ac.jp/public/VOL9/special/9.pdf).
  - [佐藤三久：「OpenMP並列プログラミング入門」、筑波大学計算科学センター（2010）](https://www2.ccs.tsukuba.ac.jp/workshop/HPCseminar/2010/material/2010-03openmp.pdf)。
  - 菅原 清文：「C/C++ プログラマーのための OpenMP 並列プログラミング」、第2版、カットシステム、ISBN 978-4-87783-223-0 (2012年6月)。
  - 片桐孝洋：「並列プログラミング入門:サンプルプログラムで学ぶOpenMPとOpenACC」、東京大学出版会、ISBN 978-4130624565　(2015年5月29日)。
  - [片桐孝洋：「OpenMPの基礎」、名古屋大学情報基盤センター、計算科学技術特論A第3回（2017年度）](https://www.r-ccs.riken.jp/r-ccssite/wp-content/uploads/2017/04/tokuronA_17_3_katagiri_r1.pdf)。
  - [一般財団法人高度情報科学技術研究機構（著）：「並列プログラミング入門（OpenMP編）」（2018年10月）](https://www.hpci-office.jp/invite2/documents2/openmp_20200203.pdf)
  - 北山洋幸：「OpenMP基本と実践―メニ―コアCPU時代の並列プログラミング手法」、カットシステム、ISBN 978-4877834494 (2018年10月1日)。

## 外部リンク

  - [OpenMP](http://www.openmp.org/)
  - [OpenMP入門 - Fortran利用者向け (NAG社)](http://www.nag-j.co.jp/openMP/index.htm)

[Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink")

1.
2.
3.
4.
5.
6.  [OpenMP\* 入門 | iSUS](http://www.isus.jp/article/openmp-special/getting-started-with-openmp/)
7.  [openmp - GCC Wiki](https://gcc.gnu.org/wiki/openmp)
8.
9.  [OpenMP®/Clang](http://clang-omp.github.io/)
10. [OpenMP in Visual C++ | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/parallel/openmp/openmp-in-visual-cpp)
11. [/openmp (Enable OpenMP Support) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/reference/openmp-enable-openmp-2-0-support?view=vs-2019)
12. [OpenMP\* 4.0 Features in Intel C++ Composer XE 2013 | Intel® Developer Zone](https://software.intel.com/en-us/articles/openmp-40-features-in-intel-c-composer-xe-2013)