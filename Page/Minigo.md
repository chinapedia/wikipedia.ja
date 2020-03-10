> この記事は[Minigo](https://ja.wikipedia.org/wiki/Minigo)から翻訳されています。


**Minigo**(ミニ碁)は[オープンソース](../Page/オープンソース.md "wikilink")の[コンピュータ囲碁](../Page/コンピュータ囲碁.md "wikilink")ソフトウェア([囲碁](../Page/囲碁.md "wikilink")思考エンジン)。

## 概要

Minigoは[DeepMind](https://ja.wikipedia.org/wiki/DeepMind "wikilink")が学術誌*[Nature](https://ja.wikipedia.org/wiki/Nature "wikilink")*ので[AlphaGo Zeroについて発表した論文](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")『\[1\]』をもとに実装された[オープンソース](../Page/オープンソース.md "wikilink")の[囲碁](../Page/囲碁.md "wikilink")思考エンジン(囲碁[AI](../Page/人工知能.md "wikilink"))\[2\]で、[定石](../Page/定石.md "wikilink")や[手筋などの](../Page/手筋_\(囲碁\).md "wikilink")[ヒューリスティクス](../Page/ヒューリスティクス.md "wikilink")(経験則)はプログラムに書き込まれず、囲碁の基本的なルールのみがプログラムされている。また、一種類の[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")のみを持ち、自己対戦の対局で学習が行われる（[AlphaGo](https://ja.wikipedia.org/wiki/AlphaGo "wikilink")はポリシーネットワークとバリューネットワークの2種類で設計されている）。

ソフトウェア本体は[Python](../Page/Python.md "wikilink")で記述されており\[3\]、[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")の[ライブラリ](../Page/ライブラリ.md "wikilink")には[TensorFlow](https://ja.wikipedia.org/wiki/TensorFlow "wikilink")が使用されている\[4\]。[ソースコード](../Page/ソースコード.md "wikilink")は[Apache License 2.0で公開され](https://ja.wikipedia.org/wiki/Apache_License_2.0 "wikilink")\[5\]、[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")のトレーニングデータは[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")でリリースされている\[6\]。

プロジェクトの目標は以下としている\[7\]：

  - [TensorFlow](https://ja.wikipedia.org/wiki/TensorFlow "wikilink")、[Kubernetes](https://ja.wikipedia.org/wiki/Kubernetes "wikilink")、[Google Cloud Platformを使用した](https://ja.wikipedia.org/wiki/Google_Cloud_Platform "wikilink")[強化学習](../Page/強化学習.md "wikilink")を実装の例を提供。
  - [AlphaGo Zeroの論文の実証と](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")、オープンソースのツールとして提供。
  - 囲碁界、[機械学習](../Page/機械学習.md "wikilink")コミュニティ以及Kubernetesコミュニティへの情報提供。

これ以外にも[Leela ZeroについてMinigoの作者が感じた疑問を明らかにする目的もある](https://ja.wikipedia.org/wiki/Leela_Zero "wikilink")\[8\]。

### GoogleおよびDeepMindとの関連

Minigoの[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")でのプロジェクトは[TensorFlow](https://ja.wikipedia.org/wiki/TensorFlow "wikilink")の公式アカウント直下に置かれており（TensowFlowはGoogleが開発したソフトウェア），プロジェクトのメインの開発者であるAndrew Jackson\[9\]は[Google](../Page/Google.md "wikilink")社員だが\[10\]、MinigoはTensorFlowのプロジェクトとは無関係で\[11\]，[DeepMind](https://ja.wikipedia.org/wiki/DeepMind "wikilink")が開発した[AlphaGo](https://ja.wikipedia.org/wiki/AlphaGo "wikilink")の公式の実装でもなく\[12\]、[AlphaGo Zeroの論文をもとに独自に開発したとしている](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")\[13\]\[14\]。

### 開発段階

[Google](../Page/Google.md "wikilink")と[DeepMind](https://ja.wikipedia.org/wiki/DeepMind "wikilink")はMinigoプロジェクトに企業としては公式にプロジェクトへの参加しませんでしたが、開発者のAndrew JacksonはGoogleが提供している勤務時間の20%(「[20 percent time](https://ja.wikipedia.org/wiki/Google#社風 "wikilink")」)を使い\[15\]、Googleからハードウェアリソース([計算資源](../Page/計算資源.md "wikilink"))の支援を受けました\[16\]\[17\]：

  - 第一段階（First run、2017年11月）
    約1000のCPUコア（[GPU](https://ja.wikipedia.org/wiki/GPU "wikilink")なし）を使用して2週間実行し、主にプログラム実装の正確さを確認するために[九路盤](https://ja.wikipedia.org/wiki/九路盤 "wikilink")でのトレーニング。

  - 第二段階（Second run、2017年12から2018年1月）
    約1000のGPUで約4週間実行し、19路盤を使用し訓練、20 ブロック x 128種類のフィルターのCNN([畳み込みニューラルネットワーク](https://ja.wikipedia.org/wiki/畳み込みニューラルネットワーク "wikilink"))が使われ、大規模な[バグ](../Page/バグ.md "wikilink")を修正し、プログラムにさまざまな改善を加え論文に記載されていない詳細を実装する方法を模索した。バージョン160あたりで、[KGS](https://ja.wikipedia.org/wiki/KGS "wikilink")と[CGOS](https://ja.wikipedia.org/wiki/CGOS "wikilink")に`somebot`のニックネームで登録した。

  - 第三段階（Third run、2018年1月20日から2018年2月1日）
    [AlphaGo Zeroの論文の中で使用が不明瞭な部分を確認し](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")、試行錯誤し適切な結果を採用した。

  - 第四段階（2018年2月7日から2018年3月）

## 他の囲碁AIとの協業

[Leela ZeroもMinigoと同樣に](https://ja.wikipedia.org/wiki/Leela_Zero "wikilink")[AlphaGo Zeroの論文をもとに作られたソフトウェアであり](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")\[18\]、[Google](../Page/Google.md "wikilink")の援助により[計算資源](../Page/計算資源.md "wikilink")を得て、それをもとに多くの学習結果を得た。こうしたことから、Leela ZeroとMinigoのそれぞれの開発チームは学習結果や学習によるパラメータなどのノウハウの共有についての議論を行った\[19\]。

## 成績

Minigoの第二段階から[CGOS](https://ja.wikipedia.org/wiki/CGOS "wikilink")の19路盤に登録を行い(登録名`somebot)` \[20\]、最高点は `somebot-199b`\[21\]のアカウントで[イロレーティング](../Page/イロレーティング.md "wikilink")約2600点に到達した\[22\]。

## 市販ソフトでの採用

2019年11月29日に発売された『[入神の囲碁](https://ja.wikipedia.org/wiki/入神の囲碁 "wikilink")』にMinigoが搭載されている\[23\]。入神の囲碁ではMinigoを含め5種類の囲碁思考エンジン(囲碁AI)が搭載されている。

## 関連項目

  - [AlphaGo](https://ja.wikipedia.org/wiki/AlphaGo "wikilink")
  - [AlphaGo Zero](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")
  - [Leela Zero](https://ja.wikipedia.org/wiki/Leela_Zero "wikilink") －Minigoと同樣に[AlphaGo Zeroの論文をもとに作られたソフトウェア](https://ja.wikipedia.org/wiki/AlphaGo_Zero "wikilink")。
  - [TensorFlow](https://ja.wikipedia.org/wiki/TensorFlow "wikilink") - Minigoが使用しているされる[機械学習](../Page/機械学習.md "wikilink")の[ソフトウェアライブラリ](../Page/ライブラリ.md "wikilink")。
  - [コンピュータ囲碁](../Page/コンピュータ囲碁.md "wikilink")

## 脚注

### 注釈

<references group="注"/>

### 出典

## 外部リンク

  -

[Category:コンピュータ囲碁](https://ja.wikipedia.org/wiki/Category:コンピュータ囲碁 "wikilink") [Category:人工ニューラルネットワーク](https://ja.wikipedia.org/wiki/Category:人工ニューラルネットワーク "wikilink") [Category:機械学習](https://ja.wikipedia.org/wiki/Category:機械学習 "wikilink") [Category:2018年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2018年のソフトウェア "wikilink")

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
20.
21.
22.
23.