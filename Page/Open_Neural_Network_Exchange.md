> この記事は[Open Neural Network Exchange](https://ja.wikipedia.org/wiki/Open_Neural_Network_Exchange)から翻訳されています。


**Open Neural Network Exchange (ONNX)**は、 [オープンソースで開発されており](../Page/オープンソースソフトウェア.md "wikilink")、[機械学習](../Page/機械学習.md "wikilink")や[人工知能](../Page/人工知能.md "wikilink")のモデルを表現する為の代表的なフォーマットである。 \[1\] ONNXは[GitHub](https://ja.wikipedia.org/wiki/GitHub "wikilink")で入手できる。

## 歴史

2017年9月に、[Facebook](../Page/Facebook.md "wikilink")と[Microsoftは](../Page/マイクロソフト.md "wikilink")、PyTorchや[Caffe](../Page/Caffe.md "wikilink")2などの[機械学習](../Page/機械学習.md "wikilink")フレームワーク間において相互運用を可能にする為の取り組みとして、このプロジェクトを始動した。その後、[IBM](../Page/IBM.md "wikilink")、[Huawei](../Page/ファーウェイ.md "wikilink")、[Intel](https://ja.wikipedia.org/wiki/インテル "wikilink")、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、[ARM](https://ja.wikipedia.org/wiki/ARMホールディングス "wikilink")、[Qualcommがこの取り組みに対して積極的な支援を表明した](../Page/クアルコム.md "wikilink")。 \[2\]

2017年10月に、Microsoftは[Cognitive ToolkitおよびProject](https://ja.wikipedia.org/wiki/Microsoft_Cognitive_Toolkit "wikilink") Brainwaveプラットフォームにおいて、ONNXのサポートを発表した。 \[3\]

2019年11月、ONNXはLinux Foundation AIの卒業生プロジェクトとして承認された。

## 開発背景

以下の特性を補完する意図にて開発が進められた。

### フレームワークの相互運用性

開発工程や機械学習の高速処理、ネットワークの基本設計における柔軟性やモバイルデバイスでの推論などの特定の段階において、開発者が複数のフレームワークでのデータのやり取りを簡単に行えるようにする。 \[4\]

### 最適化の共有

ハードウェアベンダーなどは、ONNXを対象に調整を行うことで、複数のフレームワークにおける[ニューラルネットワーク](../Page/ニューラルネットワーク.md "wikilink")のパフォーマンスを一度に改善することができる。\[5\]

## 内容

ONNXは、推論（評価）に焦点を当て、拡張可能な計算グラフモデル、組み込み演算子、および標準[データ型](../Page/データ型.md "wikilink")の定義を提供する。 \[6\]

それぞれの[データフロー](../Page/データフロー.md "wikilink")グラフは、[非循環グラフを形成するノードのリストになっている](../Page/木_\(数学\).md "wikilink")。 ノードには入力と出力があり、各ノードが処理を呼び出すようになっている。メタデータはグラフを文書化する。組み込み演算子は、ONNXをサポートする各フレームワークで利用可能である。 \[7\]

## その他のパートナーシップ

MicrosoftとFacebookは、[Apple](../Page/アップル_\(企業\).md "wikilink")、[Amazon](../Page/Amazon.com.md "wikilink")、[Google](../Page/Google.md "wikilink")、[IBM](../Page/IBM.md "wikilink")とともにAIのパートナーシップに参加しており、広く一般に認知度を高め、研究を促進する活動を行っている。 \[8\]

## 関連項目

  - [Neural Network Exchange Format](https://ja.wikipedia.org/wiki/:en:Neural_Network_Exchange_Format "wikilink")
  - [Comparison of deep learning software](https://ja.wikipedia.org/wiki/:en:Comparison_of_deep_learning_software "wikilink")

## 参照資料

## 外部リンク

  -
  -
[Category:人工知能](https://ja.wikipedia.org/wiki/Category:人工知能 "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:応用機械学習](https://ja.wikipedia.org/wiki/Category:応用機械学習 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.