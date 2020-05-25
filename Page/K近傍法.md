> この記事は[K近傍法](https://ja.wikipedia.org/wiki/K近傍法)から翻訳されています。


***k*近傍法**（ケイきんぼうほう、）は、[特徴空間](https://ja.wikipedia.org/wiki/特徴空間 "wikilink")における最も近い訓練例に基づいた[分類の手法であり](../Page/分類_\(統計学\).md "wikilink")、[パターン認識](../Page/パターン認識.md "wikilink")でよく使われる。[最近傍探索](../Page/最近傍探索.md "wikilink")問題の一つ。k近傍法は、インスタンスに基づく学習の一種であり、 の一種である。その関数は局所的な近似に過ぎず、全ての計算は分類時まで後回しにされる。また、[回帰分析](../Page/回帰分析.md "wikilink")にも使われる。

## 概要

*k*近傍法は、ほぼあらゆる[機械学習](../Page/機械学習.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")の中で最も単純である。あるオブジェクトの分類は、その近傍のオブジェクト群の投票によって決定される（すなわち、*k* 個の最近傍のオブジェクト群で最も一般的なクラスをそのオブジェクトに割り当てる）。*k* は正の[整数](../Page/整数.md "wikilink")で、一般に小さい。*k* = 1 なら、最近傍のオブジェクトと同じクラスに分類されるだけである。[二項分類](../Page/二項分類.md "wikilink")の場合、*k* を奇数にすると同票数で分類できなくなる問題を避けることができる。

同じ手法は[回帰分析](../Page/回帰分析.md "wikilink")に使われる。この場合、オブジェクトの属性値を *k* 個の最近傍のオブジェクト群の属性値の平均値とする。より近いオブジェクトに大きく重み付けすることもできる。

近傍のオブジェクトは、正しい分類が判っているもの（あるいは回帰分析の場合、属性値が判っているもの）から選ばれる。これをアルゴリズムの訓練例と考えることもできるが、明確な訓練段階は不要である。近傍を選ぶにあたって、各オブジェクトは多次元の特徴空間における位置ベクトルで表される。通常、[ユークリッド距離](https://ja.wikipedia.org/wiki/ユークリッド距離 "wikilink")を使うが、[マンハッタン距離](../Page/マンハッタン距離.md "wikilink")などの他の距離も原理的には使うことができる。*k*近傍法は、データの局所的構造に左右されやすい。

## アルゴリズム

[thumb](https://ja.wikipedia.org/wiki/ファイル:KnnClassification.svg "wikilink")

訓練例は、多次元の特徴空間におけるベクトルである。空間は、訓練例のラベルと位置によって領域に分割されている。空間内のある点には、その *k* 個の最近傍の訓練例に最も多く付けられているクラスラベル *c* が割り当てられる。このとき、一般に[ユークリッド距離](https://ja.wikipedia.org/wiki/ユークリッド距離 "wikilink")が使われる。

アルゴリズムの訓練段階では、訓練例の特徴ベクトルとクラスラベルだけを保持している。実際の分類段階では、クラスが未知である標本の特徴空間におけるベクトルが与えられる。この新たなベクトルと既存のベクトル群との距離を計算し、*k* 個の最近傍の標本が選択される。新たなベクトルを特定のクラスに分類する方法はいくつかある。最も一般的な手法は、*k* 個の最近傍のオブジェクトの中で最も一般的なクラスに分類する方法である。この技法による分類の問題点は、全訓練例で個体数が最も多いクラスに分類される可能性が高くなる点である。この対策として、*k* 個の最近傍のオブジェクトの間で、新たなベクトルとの距離の大小を考慮して（重み付けして）クラスを決定する方法がある。

## パラメータ選択

*k* をどのように決定するかは、データに依存する。一般に *k* が大きければ、分類にあたってのノイズの影響を低減できるが、クラス間の境界が明確にならない傾向がある。*k* の選択には様々な[ヒューリスティックス](https://ja.wikipedia.org/wiki/ヒューリスティックス "wikilink")が用いられる（例えば、[交差検証](../Page/交差検証.md "wikilink")）。*k* = 1 のときの *k*近傍法を、最近傍法と呼び、最も近傍にある訓練例のクラスを採用する。

*k*近傍法の正確さは、ノイズ的な特徴や不適切な特徴によって著しく損なわれることがある。あるいは、特徴尺度がその重要性と対応していない場合も、同様である。このあたりに関しては、[特徴選択](https://ja.wikipedia.org/wiki/特徴選択 "wikilink")（feature selection）として研究されている。特徴尺度を最適化するための特によく使われる手法として、[進化的アルゴリズム](../Page/進化的アルゴリズム.md "wikilink")の利用がある。また、訓練データと訓練クラスとの[相互情報量](../Page/相互情報量.md "wikilink")によって特徴の尺度を決定する方法もよく使われる。

## 特徴

このアルゴリズムの単純なバージョンは、単に標本と既存のベクトルとの距離を計算すればよいが、データが増えれば計算量も膨大となる。様々な[最近傍探索](../Page/最近傍探索.md "wikilink")アルゴリズムが提案されており、一般に実際に距離を計算する回数を削減する。特徴空間のパーティショニングによる最適化や、特定の値が近いものだけ距離を計算する最適化などがある。その他の最近傍探索アルゴリズムとしては、次のようなものがある。

  - [kd木](https://ja.wikipedia.org/wiki/kd木 "wikilink")
  - [Metric tree](https://ja.wikipedia.org/wiki/:en:Metric_tree "wikilink")
  - [Locality sensitive hashing](https://ja.wikipedia.org/wiki/局所性鋭敏型ハッシュ "wikilink") (LSH)

最近傍法は、強い[一致性を示す](../Page/推定量.md "wikilink")。データ量が無限に近づくにつれて、このアルゴリズムの誤り率はベイズ誤り率（達成可能な最小誤り率）の2倍以下となる。*k*近傍法は *k*（近傍とするデータ個数）を増やすことでベイズ誤り率に近づく。

*k*近傍法は、連続値をとる変数についても適用可能である。そのような実装の例として、距離の逆数で重み付けした *k*近傍法がある。このアルゴリズムは次のように動作する。

1.  対象データと他のデータのユークリッド距離か[マハラノビス距離](../Page/マハラノビス距離.md "wikilink")を計算する。
2.  計算された距離の順にデータを[ソート](../Page/ソート.md "wikilink")する。
3.  ヒューリスティックによって決めた最適な *k* 個の近傍を選ぶ（[根二乗平均誤差](https://ja.wikipedia.org/wiki/根二乗平均誤差 "wikilink")など）
4.  それらについて、距離の逆数で重み付けした平均を求める。

## 関連項目

  - [サポートベクターマシン](../Page/サポートベクターマシン.md "wikilink")
  - [データマイニング](../Page/データマイニング.md "wikilink")
  - [パターン認識](../Page/パターン認識.md "wikilink")
  - [カーネル密度推定](../Page/カーネル密度推定.md "wikilink")
  - [機械学習](../Page/機械学習.md "wikilink")
  - [最近傍探索](../Page/最近傍探索.md "wikilink")
  - [人工知能](../Page/人工知能.md "wikilink")
  - [統計学](../Page/統計学.md "wikilink")
  - [K平均法](../Page/K平均法.md "wikilink")
  - [予測分析](https://ja.wikipedia.org/wiki/予測分析 "wikilink")

## 参考文献

  - Belur V. Dasarathy, editor (1991) *Nearest Neighbor (NN) Norms: NN Pattern Classification Techniques*, ISBN 0-8186-8930-7
  - *Nearest-Neighbor Methods in Learning and Vision*, edited by Shakhnarovish, Darrell, and Indyk, The MIT Press, 2005, ISBN 0-262-19547-X
  - Estimation of forest stand volumes by Landsat TM imagery and stand-level field-inventory data. Forest Ecology and Management, Volume 196, Issues 2-3, 26 July 2004, Pages 245-255. Helena Mäkelä and Anssi Pekkarinen
  - Estimation and mapping of forest stand density, volume, and cover type using the *k*-nearest neighbors method. Remote Sensing of Environment, Volume 77, Issue 3, September 2001, Pages 251-274. Hector Franco-Lopez, Alan R. Ek and Marvin E. Bauer

## 外部リンク

  - [*k*-nearest neighbor algorithm in Visual Basic](http://paul.luminos.nl/documents/show_document.php?d=197) （ソースコードと実行ファイルあり）

  - [*k*-nearest neighbor tutorial using MS Excel](http://people.revoledu.com/kardi/tutorial/KNN/index.html)

  - [Agglomerative-Nearest-Neighbor Algorithm, by Michael J. Radwin](http://www.radwin.org/michael/projects/learning/)

  - [Weighted distance learning for nearest neighbor error minimization by R. Paredes and E. Vidal](http://www.dsic.upv.es/~rparedes/english/research/CPW/index.html)

  -
[Category:検索アルゴリズム](https://ja.wikipedia.org/wiki/Category:検索アルゴリズム "wikilink") [Category:分類アルゴリズム](https://ja.wikipedia.org/wiki/Category:分類アルゴリズム "wikilink") [Category:機械学習アルゴリズム](https://ja.wikipedia.org/wiki/Category:機械学習アルゴリズム "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")