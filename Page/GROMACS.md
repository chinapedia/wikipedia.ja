> この記事は[GROMACS](https://ja.wikipedia.org/wiki/GROMACS)から翻訳されています。


**GROMACS**（グローマックス、**Groningen Machine for Chemical Simulations**、グローニンゲン・マシン・フォー・ケミカル・シミュレーションズ）は、[フローニンゲン大学](https://ja.wikipedia.org/wiki/フローニンゲン大学 "wikilink")で開発された[分子動力学](https://ja.wikipedia.org/wiki/分子動力学 "wikilink")[シミュレーション](../Page/シミュレーション.md "wikilink")のソフトウェアパッケージである。現在は世界中の大学と研究所の貢献者によって維持管理されている\[1\]\[2\]\[3\]。[フリー](../Page/フリーソフトウェア.md "wikilink")、[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")であり、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink")（GPL）と、バージョン4.6からは[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (LGPL) の下で公表されている。

GROMACSは現在利用可能な最速かつ最も人気のあるソフトウェアパッケージの一つであり\[4\]\[5\]、[中央処理装置](https://ja.wikipedia.org/wiki/中央処理装置 "wikilink")（CPU）および[Graphics Processing Unit](../Page/Graphics_Processing_Unit.md "wikilink")（GPU）上で動作する\[6\]。

GROMACSは並列計算を前提としたプログラミングがなされている。プログラムの大部分は[C言語](../Page/C言語.md "wikilink")で記述されており、同じグループが以前に開発した[GROMOS](https://ja.wikipedia.org/wiki/GROMOS "wikilink")（[FORTRAN](../Page/FORTRAN.md "wikilink") 77ベース）が参考にされている。バージョン4.6時点において、[SSEや](../Page/ストリーミングSIMD拡張命令.md "wikilink")[AVX](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令#Intel_AVX "wikilink")、[HPC-ACE](https://ja.wikipedia.org/wiki/HPC-ACE "wikilink")などの拡張命令を用いたアセンブリ言語のルーチンが実装されており、高速な計算が可能となっている。

[力場はGROMACS](https://ja.wikipedia.org/wiki/力場_\(化学\) "wikilink")、[GROMOS](https://ja.wikipedia.org/wiki/GROMOS "wikilink")、[OPLS](https://ja.wikipedia.org/wiki/OPLS "wikilink")-AA、[AMBER](https://ja.wikipedia.org/wiki/AMBER "wikilink")、[CHARMM](https://ja.wikipedia.org/wiki/CHARMM "wikilink")が標準で使用可能である\[7\]。

## 歴史

GROMACSプロジェクトは1991年に[オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")、[フローニンゲン大学](https://ja.wikipedia.org/wiki/フローニンゲン大学 "wikilink")生物物理化学科で始まった（1991年-2000年）。2001年からは、[スウェーデン](https://ja.wikipedia.org/wiki/スウェーデン "wikilink")の[王立工科大学と](https://ja.wikipedia.org/wiki/スウェーデン王立工科大学 "wikilink")[ウプサラ大学](../Page/ウプサラ大学.md "wikilink")のGROMACS開発チームによって開発されている。

## 機能

GROMACSはアルゴリズム的ならびにプロセッサ特異的最適化によって極めて速く、CPUを使用した計算において大抵は多くのシミュレーションプログラムよりも3から10倍高速に動作する\[8\]。GROMACSは[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")を通じて操作され、インプットおよびアウトプットにファイルを用いることができる。GROMACSは計算の進行度合いと[完了予定時刻のフィードバック](https://ja.wikipedia.org/wiki/到着予定時刻 "wikilink")、トラクジェクトリビュアー、トラクジェクトリ解析のための豊富なライブラリを備える\[9\]。加えて、異なる[力場のサポートによってGROMACSは非常に柔軟性が高い](https://ja.wikipedia.org/wiki/力場_\(化学\) "wikilink")。[MPIあるいは](../Page/Message_Passing_Interface.md "wikilink")[スレッドを用いて並列計算が可能である](../Page/スレッド_\(コンピュータ\).md "wikilink")。

### シミュレーション

  - シミュレーション（分子動力学、[ランジュバン動力学](https://ja.wikipedia.org/wiki/ランジュバン動力学 "wikilink")）
  - エネルギー最小化（共役勾配法、最急降下法）
  - 基準振動解析
  - 相関関数

### アンサンブル

  - Weak Coupling法（温度・圧力制御）
  - [Nose-Hoover法](https://ja.wikipedia.org/wiki/能勢＝フーバー・サーモスタット "wikilink")（温度制御）
  - Parrinello-Rahman法（圧力制御）
  - Martyna-Tobias-Tuckerman-Klein法（温度・圧力制御）

### 長距離相互作用の取り扱い

  - カットオフ近似（Group based、twin-range、スイッチング関数、シフト関数）
  - [PME](https://ja.wikipedia.org/wiki/エバルトの方法#粒子・メッシュ・エバルト_\(PME\)_法 "wikilink") (particle mesh Ewald)
  - PPPM (particle-particle particle mesh Ewald)
  - Reaction Field
  - ユーザ定義テーブル関数

### 自由エネルギー計算

  - [熱力学的積分法](../Page/熱力学的積分法.md "wikilink") (thermodynamic integration)
  - [自由エネルギー摂動法](https://ja.wikipedia.org/wiki/自由エネルギー摂動法 "wikilink") (free energy perturbation)
  - 試験粒子挿入法 (test particle insertion)
  - [レプリカ交換法](https://ja.wikipedia.org/wiki/レプリカ交換法 "wikilink") (replica exchange)

## 脚注

<references />

## 参考文献

  -
  -
  -
  -
## 外部リンク

  - [GROMACS Webページ](http://www.gromacs.org/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:分子動力学ソフトウェア](https://ja.wikipedia.org/wiki/Category:分子動力学ソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.