> この記事は[Dcgan](https://ja.wikipedia.org/wiki/Dcgan)から翻訳されています。


**DCDAN**（Deep Convolutional GAN)は、2015年にA.Radfordらによって発表された[敵対的生成ネットワーク](https://ja.wikipedia.org/wiki/敵対的生成ネットワーク "wikilink")の一種であり、[生成ネットワーク](https://ja.wikipedia.org/wiki/生成ネットワーク "wikilink")（generator）と[識別ネットワーク](https://ja.wikipedia.org/wiki/識別ネットワーク "wikilink")（discriminator）の2つのネットワークに[畳み込みニューラルネットワーク](https://ja.wikipedia.org/wiki/畳み込みニューラルネットワーク "wikilink")([CNN](https://ja.wikipedia.org/wiki/CNN "wikilink"))を用いたモデルのことである。

## 概要

DCGANにおける[生成モデル](https://ja.wikipedia.org/wiki/生成モデル "wikilink")は100次元の一様分布Zを入力とし、転置畳み込みによって徐々に画像空間へ投影していく仕組みである。また識別モデルは同じく[プーリング層](https://ja.wikipedia.org/wiki/プーリング層 "wikilink")を使わずに畳み込みによってダウンサンプリングしていき、[活性化関数](https://ja.wikipedia.org/wiki/活性化関数 "wikilink")には[ReLU](https://ja.wikipedia.org/wiki/ReLU "wikilink")の代わりに[Leaky ReLUを使用する](https://ja.wikipedia.org/wiki/Leaky_ReLU "wikilink")。

プーリング層や[全結合層](https://ja.wikipedia.org/wiki/全結合層 "wikilink")を使わずにCNNによって学習を進めることで、通常の[GANよりも鮮明な画像の生成が可能になった](https://ja.wikipedia.org/wiki/敵対的生成ネットワーク "wikilink")。

さらにDCGANによる生成は、その入力の[ベクトル空間](https://ja.wikipedia.org/wiki/ベクトル空間 "wikilink")的な性質が極めて良いことが明らかになり、値の近い入力同士なら似たような画像を生成し、二つの入力の間の値によって生成される画像は二つの画像の意味的な中間となる。これにより、入力を適切に調整することでより高次な特徴レベルの画像をコントロールすることができる。\[1\]

## 脚注

<references group="">

</references>

1.
## 参考文献

  - 原論文
      - Alec Radford, Luke Metz, Soumith Chintala (2015年11月19日) <https://arxiv.org/abs/1511.06434>.[arXiv](https://ja.wikipedia.org/wiki/arXiv "wikilink"). 2020年7月5日閲覧。
  - Antonio Gulli, Sujit Pal (2018) 『直感DeepLearning』オライリー・ジャパン
  - 浅川 伸一 , 江間 有沙 , 工藤 郁子 , 巣籠 悠輔  , 瀬谷 啓介  , 松井 孝之 , 松尾 豊　著（2018)『ディープラーニングG検定公式テキスト』翔泳社

[Category:人工ニューラルネットワーク](https://ja.wikipedia.org/wiki/Category:人工ニューラルネットワーク "wikilink") [Category:教師なし学習](https://ja.wikipedia.org/wiki/Category:教師なし学習 "wikilink") [Category:認知科学](https://ja.wikipedia.org/wiki/Category:認知科学 "wikilink") [Category:モデル](https://ja.wikipedia.org/wiki/Category:モデル "wikilink")

1.