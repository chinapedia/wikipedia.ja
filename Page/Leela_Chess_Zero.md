> この記事は[Leela Chess Zero](https://ja.wikipedia.org/wiki/Leela_Chess_Zero)から翻訳されています。


**Leela Chess Zero**（リーラ・チェス・ゼロ、略称: **LCZero**、**lc0**）は、[フリーでオープンソースの](../Page/FLOSS.md "wikilink")[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")に基づく[チェスエンジン](https://ja.wikipedia.org/wiki/チェスエンジン "wikilink")ならびに[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")プロジェクトである。開発の陣頭指揮を執るのはプログラマーのGary Linscott。Linscottは[Stockfish](https://ja.wikipedia.org/wiki/Stockfish "wikilink")チェスエンジンの開発者でもある。Lella Chess Zeroは[囲碁](../Page/囲碁.md "wikilink")エンジン[Leela Zeroのチェス版である](https://ja.wikipedia.org/wiki/Leela_Zero "wikilink")\[1\]。そしてLeela Zeroは[Google](../Page/Google.md "wikilink")の[AlphaGo Zeroプロジェクトを基礎としており](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")\[2\]、[AlphaZero](https://ja.wikipedia.org/wiki/AlphaZero "wikilink")の論文の手法をチェスに適用することで検証することも目的としている。

Leela ZeroおよびAlphaGo Zeroと同様に、Leela Chess Zeroはチェスの基本ルール以外のチェス特異的な固有知識を与えずに始められた\[3\]。Leela Chess Zeroは次に繰り返し行う自己対戦からの[強化学習](../Page/強化学習.md "wikilink")によってチェスをどうのように指すかを学習する。自己対戦にはLeela Chess Zeroウェブサイトで連係される分散コンピューティングネットワークを用いて行われた。

2020年現在、Leela Chess Zeroは3億局以上の自己対戦を行っており\[4\]、従来のトップチェスプログラムである[Stockfish](https://ja.wikipedia.org/wiki/Stockfish "wikilink")と比肩する水準で指す能力がある\[5\]\[6\]。

## 歴史

Leela Chess Zeroプロジェクトは2018年1月9日にTalkChess.comで初めて公表された\[7\]\[8\]。ここで、Leela Chess Zeroがオープンソースの自己学習チェスエンジンで、目標は強いチェスエンジンを作ることであることが明らかにされた\[9\]。訓練を開始して最初の数か月のうちに、Leela Chess Zeroは既に[グランドマスター](../Page/グランドマスター.md "wikilink")の水準に達し、[モンテカルロ木探索](https://ja.wikipedia.org/wiki/モンテカルロ木探索 "wikilink")を使うため評価する局面が数桁少ないにもかかわらず、、Stockfish、の初期リリースの強さを超えた。

2018年12月、[AlphaZero](https://ja.wikipedia.org/wiki/AlphaZero "wikilink")チームは[サイエンス](../Page/サイエンス.md "wikilink")誌に新たな論文を発表し、未発表であったAlphaZeroのために使われたアーキテクチャの詳細と訓練パラメータを明らかにした\[10\]。これらの変更点はすぐにLeela Chess Zeroに取り込まれ、強さと訓練効率の両方が上昇した\[11\]。

Leela Chess Zeroについての作業は[将棋](../Page/将棋.md "wikilink")に関する類似プロジェクトAobaZeroに知識を与えている\[12\]。

本エンジンはその発端以来書き直され、注意深く反復されており、現在は複数の[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")上で動作する。これによって、CPUとGPUの両方のハードウェアを効率的に使用することが可能になった\[13\] 。

[変則チェス](../Page/変則チェス.md "wikilink")の一種である[フィッシャーランダムチェス](../Page/チェス960.md "wikilink")（チェス960）をサポートしており、2020年5月現在こういったネットワークの実行可能性を試験するためにネットワークが訓練されている\[14\]。

## プログラムと使用

Leela Chess Zeroを自己学習させ、人間の水準以上でチェスを指させるために設計者らによって使われた手法が[強化学習](../Page/強化学習.md "wikilink")である。これは[機械学習](../Page/機械学習.md "wikilink")アルゴリズムの1つで、自己対局を通して報酬を最大化するよう訓練される\[15\]\[16\]。オープンソース分散コンピューティングプロジェクトとして、ボランティアユーザはLeela Chess Zeroを実行し、強化学習アルゴリズムに与えるための自己対局を何億局も行わせる\[17\]。Leela Chess Zeroエンジンの進歩に貢献するために、本エンジンとクラインアントの最新非リリース候補版（non-rc）をダウンロードしなければならない。クラインアントはLeela Chess Zeroの現在のサーバに接続し（サーバには自己対局からの全ての情報が貯えられる）、最新のネットワークを入手し、自己対局を生成し、訓練データをサーバにアップロードするために必要である\[18\]。

マシン上でLeela Chess Zeroエンジンと対局するためには、エンジンバイナリとネットワークの2つの構成要素が必要である（エンジンバイナリは、クライアントがエンジンのための訓練プラットフォームとして使われるという点で、クライアントとは異なる）。ネットワークは、局面を評価するために必要なLeela Chess Zeroの評価関数を含む\[19\]。より古いネットワークもダウンロード可能であり、それらのネットワークをlc0バイナリがあるフォルに置くことで使うことができる。

## 出典

## 外部リンク

  -
  - [Leela Chess Zero](https://github.com/LeelaChessZero/lc0) on [GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")

  - [Neural network training client](https://github.com/LeelaChessZero/lczero-client/releases)

  - [Engine](https://github.com/LeelaChessZero/lc0/releases)

  - [Neural nets](https://training.lczero.org/networks/?show_all=0)

  - [Chessprogramming wiki on Leela Chess Zero](https://www.chessprogramming.org/Leela_Chess_Zero)

[Category:コンピュータチェス](https://ja.wikipedia.org/wiki/Category:コンピュータチェス "wikilink") [Category:フリーソフトウェアとオープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアとオープンソースソフトウェア "wikilink") [Category:分散コンピューティングプロジェクト](https://ja.wikipedia.org/wiki/Category:分散コンピューティングプロジェクト "wikilink") [Category:2018年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2018年のソフトウェア "wikilink") [Category:応用機械学習](https://ja.wikipedia.org/wiki/Category:応用機械学習 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.