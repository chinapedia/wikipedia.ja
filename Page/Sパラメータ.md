> この記事は[Sパラメータ](https://ja.wikipedia.org/wiki/Sパラメータ)から翻訳されています。


**Sパラメータ**([Scattering parameters](https://ja.wikipedia.org/wiki/:en:Scattering_parameters "wikilink"))とは、[高周波](../Page/高周波.md "wikilink")[電子回路](../Page/電子回路.md "wikilink")や高周波[電子部品](../Page/電子部品.md "wikilink")の特性を表すために使用される[回路網パラメータのひとつ](../Page/二端子対回路.md "wikilink")。**散乱行列**（**S行列**）または**散乱パラメータ**とも呼ばれる。回路網の通過・反射電力特性を表現する。

## 定義

### n端子対回路網の定義

n対の端子を持つ電気回路において、入力方向に進む波の振幅を*a<sub>1</sub>・・・a<sub>n</sub>* 、出力方向に進む波の振幅を*b<sub>1</sub>・・・b<sub>n</sub>*としたとき、次のように記述する。

  -
    *b<sub>1</sub> = S<sub>11</sub>a<sub>1</sub> + S<sub>12</sub>a<sub>2</sub> + ・・・ + S<sub>1n</sub>a<sub>n</sub>*
    *b<sub>2</sub> = S<sub>21</sub>a<sub>1</sub> + S<sub>22</sub>a<sub>2</sub> + ・・・ + S<sub>2n</sub>a<sub>n</sub>*
      -
        *・・・*
    *b<sub>n</sub> = S<sub>n1</sub>a<sub>1</sub> + S<sub>n2</sub>a<sub>2</sub> + ・・・ + S<sub>nn</sub>a<sub>n</sub>*

これらの式を[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")を用いて次のように表現する。

\[\begin{pmatrix} b_1 \\ \vdots \\ b_n \end{pmatrix}=\begin{pmatrix} S_{11} & \cdots & S_{1n} \\ \vdots & \ddots & \vdots \\ S_{n1} & \cdots & S_{nn}\end{pmatrix}\begin{pmatrix} a_1 \\ \vdots \\ a_n \end{pmatrix}\] この*S<sub>11</sub>*・・・*S<sub>nn</sub>*を要素とする行列が散乱行列であり、行列の要素がSパラメータである。Sパラメータの各要素は[複素数](../Page/複素数.md "wikilink")表現であり、回路の[振幅](../Page/振幅.md "wikilink")に対する影響に加えて[位相](../Page/位相.md "wikilink")に対する影響も内包する。

進行波の振幅 \(a_i\)， \(b_i\) は、電力の平方根の次元を持つように定義されることが多い．しかし，\(|a_i|^2\)，\(|b_i|^2\) が実際に電力になるとは限らない\[1\]．また，\(a_i\)， \(b_i\) を電圧進行波や電流進行波とする流儀もある\[2\]．

### 2端子対回路網の定義

2対の端子を持つ回路網（[二端子対回路](https://ja.wikipedia.org/wiki/2端子対回路網 "wikilink")、すなわち**4端子回路網**）にて使われることが多く、入力側の端子対を**端子対1**、出力側の端子対を**端子対2**とした場合には次のように定義される。

\[\begin{pmatrix}b_1 \\ b_2 \end{pmatrix} = \begin{pmatrix} S_{11} & S_{12} \\ S_{21} & S_{22} \end{pmatrix}\begin{pmatrix} a_1 \\ a_2 \end{pmatrix}\,\]

ここで、

  - \(a_1\) は **端子1**から入力される電力の平方根。
  - \(a_2\) は **端子2**から入力される電力の平方根。
  - \(b_1\) は **端子1**から出力される電力の平方根。
  - \(b_2\) は **端子2**から出力される電力の平方根。
  - *S<sub>11</sub>* は **端子1**から信号を入力したときに、**端子1**に反射する信号。絶対値の[デシベル](../Page/デシベル.md "wikilink")表示は、**端子1**の[反射損失](https://ja.wikipedia.org/wiki/反射損失 "wikilink") (リターンロス) を示す。
  - *S<sub>21</sub>* は **端子1**から信号を入力したときに、**端子2**に通過する信号。絶対値の[デシベル](../Page/デシベル.md "wikilink")表示は、**端子1**から**端子2**の[挿入損失](https://ja.wikipedia.org/wiki/挿入損失 "wikilink") (インサーションロス) を示す。
  - *S<sub>12</sub>* は **端子2**から信号を入力したときに、**端子1**に通過する信号。絶対値の[デシベル](../Page/デシベル.md "wikilink")表示は、**端子2**から**端子1**の[挿入損失](https://ja.wikipedia.org/wiki/挿入損失 "wikilink") (インサーションロス) を示す。
  - *S<sub>22</sub>* は **端子2**から信号を入力したときに、**端子2**に反射する信号。絶対値の[デシベル](../Page/デシベル.md "wikilink")表示は、**端子2**の[反射損失](https://ja.wikipedia.org/wiki/反射損失 "wikilink") (リターンロス) を示す。

## 測定方法・表示方法

Sパラメータの測定にはしばしば[ネットワークアナライザが利用される](../Page/ネットワーク・アナライザ_\(高周波回路\).md "wikilink")。

S<sub>11</sub>とS<sub>22</sub>の[利得が](../Page/利得_\(電気工学\).md "wikilink")[定在波比](../Page/定在波比.md "wikilink") (VSWR) を示すため、Sパラメータの[利得の](../Page/利得_\(電気工学\).md "wikilink")[デシベル](../Page/デシベル.md "wikilink")表示は、

  -
    <math>

20 \\log _{10} \\left| S_{ji} \\right| </math> \[dB\] と表示される。

## 脚注

## 参考文献

  -
  -
  -
## 関連項目

  - [二端子対回路](../Page/二端子対回路.md "wikilink")
  - [高周波回路](../Page/高周波回路.md "wikilink")
  - [S行列](https://ja.wikipedia.org/wiki/S行列 "wikilink")
  - [黒川兼行](https://ja.wikipedia.org/wiki/黒川兼行 "wikilink") - 一般化散乱パラメータの提唱者

[Category:無線工学](https://ja.wikipedia.org/wiki/Category:無線工学 "wikilink") [Category:電気回路](https://ja.wikipedia.org/wiki/Category:電気回路 "wikilink") [Category:電磁気学](https://ja.wikipedia.org/wiki/Category:電磁気学 "wikilink")

1.
2.  ，