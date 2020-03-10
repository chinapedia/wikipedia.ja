> この記事は[Neuroevolution](https://ja.wikipedia.org/wiki/Neuroevolution)から翻訳されています。


**Neuroevolution** または **Neuro-evolution** は人工[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")の学習に[遺伝的アルゴリズム](../Page/遺伝的アルゴリズム.md "wikilink")を用いる[機械学習](https://ja.wikipedia.org/wiki/機械学習 "wikilink")の手法である。ネットワークの性能を測るのが容易であるが、[教師あり学習](https://ja.wikipedia.org/wiki/教師あり学習 "wikilink")を用いて正しい入力と出力の対の概要を作るのが困難または不可能である[ゲームや](../Page/パソコンゲーム.md "wikilink")[ロボット](../Page/ロボット.md "wikilink")のモーター制御するようなアプリケーションに有効である。ニューラルネットワークの学習の分類体系では[強化学習](https://ja.wikipedia.org/wiki/強化学習 "wikilink")に属する。

## 特徴

多くのNeuroevolutionアルゴリズムがある。あらかじめ指定された構造のネットワークで結合重みの値を進化させる手法と重みに加えてネットワークの構造を進化させる手法の違いがある。全体としてこの違いに対して標準化された手法はなく、進化の間ネットワークの結合を加えたり削除することは複雑化や単純化と呼ぶことができる\[1\]。結合重みと構造を進化させるネットワークはTWEANNs (Topology & Weight Evolving Artificial Neural Networks)と呼ばれる。

さらに、パラメータと並行してニューラルネットワークの構造を進化させる手法（例：synaptic weights）とそれらを別々に開発する手法の違いがある。[2つの手法をロボットの制御に適用した比較をこちらで見ることができる。](http://www.ks.informatik.uni-kiel.de/~vision/doc/Publications/nts/SiebelKrauseSommer-DAGM2007.pdf)

## ネットワークの直接コード化と間接コード化

*直接コード化*はネットワークのすべての結合とノードを遺伝子として染色体に記述する。対照的に*間接コード化*はたいていネットワークを構成するルールを記述するのみである\[2\]\[3\]。

## 例

ネットワークの構造とパラメータを進化させるNeuroevolutionの手法の例

  - GNARL by Angeline et al., 1994\[4\]
  - EPNet by Yao and Liu, 1997\[5\]
  - [NeuroEvolution of Augmenting Topologies](https://ja.wikipedia.org/wiki/NeuroEvolution_of_Augmenting_Topologies "wikilink") (NEAT) by Stanley and Miikkulainen, 2005\[6\]\[7\]\[8\]
  - [Evolutionary Acquisition of Neural Topologies](https://ja.wikipedia.org/wiki/Evolutionary_Acquisition_of_Neural_Topologies "wikilink") (EANT/EANT2) by Kassahun and Sommer, 2005\[9\] / Siebel and Sommer, 2007\[10\]

## 関連項目

  - [NeuroEvolution of Augmenting Topologies](https://ja.wikipedia.org/wiki/NeuroEvolution_of_Augmenting_Topologies "wikilink") (NEAT)([:en:NeuroEvolution of Augmenting Topologies](https://ja.wikipedia.org/wiki/:en:NeuroEvolution_of_Augmenting_Topologies "wikilink"))
  - [Evolutionary Acquisition of Neural Topologies](https://ja.wikipedia.org/wiki/Evolutionary_Acquisition_of_Neural_Topologies "wikilink") (EANT/EANT2)

## 参考文献

<div class="references-small">

<references/>

</div>

## 外部リンク

  - [University of Texas neuroevolution page](http://nn.cs.utexas.edu/keyword?neuroevolution) (英語)
  - [ANNEvolve is an Open Source AI Research Project](http://ANNEvolve.sourceforge.net) (英語)
  - [Web page on evolutionary learning with EANT/EANT2](http://www.siebel-research.de/evolutionary_learning/) (英語)

[Category:進化的アルゴリズム](https://ja.wikipedia.org/wiki/Category:進化的アルゴリズム "wikilink") [Category:最適化アルゴリズム](https://ja.wikipedia.org/wiki/Category:最適化アルゴリズム "wikilink")

1.  <http://www.ucs.louisiana.edu/~dxj2534/james_gecco04.pdf>
2.  <http://nn.cs.utexas.edu/downloads/papers/stanley.alife03.pdf>
3.  Yohannes Kassahun, Mark Edgington, Jan Hendrik Metzen, Gerald Sommer and Frank Kirchner. Common Genetic Encoding for Both Direct and Indirect Encodings of Networks. In Proceedings of the Genetic and Evolutionary Computation Conference (GECCO 2007), London, UK, 1029-1036, 2007.
4.  Peter J Angeline, Gregory M Saunders, and Jordan B Pollack. An evolutionary algorithm that constructs recurrent neural networks. IEEE Transactions on Neural Networks, 5:54–65, 1994. [1](http://demo.cs.brandeis.edu/papers/ieeenn.pdf)
5.  Xin Yao and Yong Liu. A new evolutionary system for evolving artiﬁcial neural networks. IEEE Transactions on Neural Networks, 8(3):694–713, May 1997. [2](http://www.cs.bham.ac.uk/~axk/evoNN2.pdf)
6.  <http://nn.cs.utexas.edu/downloads/papers/stanley.ieeetec05.pdf>
7.  <http://nn.cs.utexas.edu/downloads/papers/stanley.ec02.pdf>
8.  <http://nn.cs.utexas.edu/downloads/papers/stanley.ieeetec05.pdf>
9.  Yohannaes Kassahun and Gerald Sommer. Efficient reinforcement learning through evolutionary acquisition of neural topologies. In Proceedings of the 13th European Symposium on Artificial Neural Networks (ESANN 2005), pages 259–266, Bruges, Belgium, April 2005. [3](http://www.ks.informatik.uni-kiel.de/~yk/ESANN2005EANT.pdf)
10. Nils T Siebel and Gerald Sommer. Evolutionary reinforcement learning of artificial neural networks. International Journal of Hybrid Intelligent Systems 4(3): 171-183, October 2007. [4](http://www.ks.informatik.uni-kiel.de/~vision/doc/Publications/nts/SiebelSommer-IJHIS2007.pdf)