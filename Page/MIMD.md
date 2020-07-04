> この記事は[MIMD](https://ja.wikipedia.org/wiki/MIMD)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:MIMD.svg "wikilink") **MIMD**(**M**ultiple **I**nstruction stream, **M**ultiple **D**ata stream)とは、[コンピューティング](../Page/コンピューティング.md "wikilink")において並列性を達成するのに使われる技法の一種。MIMD型のマシンは、独立して機能する複数の[プロセッサを持つ](../Page/CPU.md "wikilink")。任意の時点で、異なるプロセッサは異なる命令を使って異なるデータを処理している。MIMDアーキテクチャは様々な分野で応用されており、[CAD](../Page/CAD.md "wikilink")/[CAM](../Page/CAM.md "wikilink")、[シミュレーション](../Page/シミュレーション.md "wikilink")、[モデリング](../Page/モデル_\(自然科学\).md "wikilink")、通信スイッチなどに使われている。MIMD型マシンは、[共有メモリ](../Page/共有メモリ.md "wikilink")型と[分散メモリ](https://ja.wikipedia.org/wiki/分散メモリ "wikilink")型に分類される。この分類は、MIMD型マシンのプロセッサがどのようにメモリにアクセスするかに着目したものである。共有メモリ型マシンは、単純な[バスを使ったものや](../Page/バス_\(コンピュータ\).md "wikilink")、階層型のバスを使ったものがある。分散メモリ型マシンは、[ハイパーキューブ型やメッシュ型の相互接続ネットワークを使うことが多い](../Page/超立方体.md "wikilink")。

## 共有メモリ型

### バス方式

メモリとプロセッサ群が[バスに接続されたMIMDマシン](../Page/バス_\(コンピュータ\).md "wikilink")。最も単純な形態では、単一のバスに全てが接続される。バスが[ボトルネック](../Page/ボトルネック.md "wikilink")となりやすいため、小規模なマシンでよく使われている。[対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")の多くはこの方式である。

### 階層型バス方式

バス方式のMIMDマシンを上位のバスで相互接続したMIMDマシン。下位のバス内でのメモリアクセスと、上位のバスを経由したメモリアクセスで、アクセスコストが異なる[NUMA](../Page/NUMA.md "wikilink")型である。NUMAの中でも比較的小規模なマシンに多い。

## 分散メモリ型

各プロセッサにローカルなメモリが個別に配置されたMIMDマシン。データを共有するには、[メッセージとしてプロセッサ間でやりとりする必要がある](../Page/メッセージ_\(コンピュータ\).md "wikilink")。共有メモリがないため、メモリアクセスの衝突は問題とはならない。多数のプロセッサを1対1に接続するのはコストがかかりすぎるため、直接接続するプロセッサ数を制限するのが一般的である。しかし、その場合に直接接続していないプロセッサ間で通信をするとき、間にあってメッセージを転送するプロセッサ数が多いほど転送に時間がかかることになる。そのため、最大転送時間を考慮したネットワーク設計が重要となる。また、バス方式の共有メモリ型MIMDマシンを最小単位としてネットワークを形成する場合もある。

### [ハイパーキューブ型ネットワーク](../Page/超立方体.md "wikilink")

[超立方体](../Page/超立方体.md "wikilink")の各頂点にプロセッサとメモリを配置する形態。2<sup>n</sup>個のプロセッサ（ノード）があるとき、最も遠いプロセッサまでに経由する辺の数は n 本となる。また、2<sup>n</sup>個のノードがあるとき、直接接続するノード数も n 個となる。例えば、16ノードであれば1つのノードから4本の通信路が出ていて、最も遠いノードまで3個のノードを経由する。具体例としては[nCUBE](https://ja.wikipedia.org/wiki/nCUBE "wikilink")のマシンなどがある。ハイパーキューブの欠点としては、ノード数が常に 2<sup>n</sup> 個でなければならない点である（そうでないと転送できない経路が出てくる）。従って、アプリケーションが実際に必要とするノード数より多めにノードを用意しなければならない。

### メッシュ型ネットワーク

2次元の格子状にプロセッサとメモリを配置する形態。各プロセッサは常に4つの近傍のプロセッサと相互接続される。格子の端は相互に接続され、全体として[トーラス](../Page/トーラス.md "wikilink")型とされることが多い。ハイパーキューブに比較すると、プロセッサ数が任意である点が優れているが、最も遠いプロセッサとの距離はハイパーキューブよりも大きい。

## 関連項目

  - [対称型マルチプロセッシング](../Page/対称型マルチプロセッシング.md "wikilink")
  - [NUMA](../Page/NUMA.md "wikilink")
  - [フリンの分類](../Page/フリンの分類.md "wikilink")
  - [SPMD](https://ja.wikipedia.org/wiki/SPMD "wikilink")
  - [マルチコア](../Page/マルチコア.md "wikilink")

[de:Flynnsche Klassifikation\#MIMD (Multiple Instruction, Multiple Data)](https://ja.wikipedia.org/wiki/de:Flynnsche_Klassifikation#MIMD_\(Multiple_Instruction,_Multiple_Data\) "wikilink")

[Category:フリンの分類](https://ja.wikipedia.org/wiki/Category:フリンの分類 "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink")