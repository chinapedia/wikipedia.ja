> この記事は[H](https://ja.wikipedia.org/wiki/H)から翻訳されています。


**\(H^\infty\)制御理論**（エイチインフィニティせいぎょりろん、[英語](../Page/英語.md "wikilink")：H-infinity control theory）は、外乱信号の影響を抑制する[制御系](https://ja.wikipedia.org/wiki/制御系 "wikilink")を構築するための[制御理論](../Page/制御理論.md "wikilink")である。この制御理論は、1980年代に研究が進み、1989年頃に完成した。**\(H^\infty\)ノルム**と呼ばれる[ノルム](../Page/ノルム.md "wikilink")によって[伝達関数](https://ja.wikipedia.org/wiki/伝達関数 "wikilink")を評価し、それが所望の値より小さくなるようにすることにより、目的の性能を達成させる。具体的には、一般化プラントと呼ばれる*制御入力*、*外乱入力*、*制御出力*、*評価出力*の 4 つの入出力を持つ汎用的な制御モデルを対象に、制御出力から制御入力に適切なフィードバックを施すことで外乱入力から評価出力までの伝達関数の **H<sup>∞</sup>ノルム**を小さくするという制御系設計手順を取る。制御対象の不確定な部分を外乱信号として扱うことで、モデルの不確かさの影響を抑制する制御系となる。このように、想定していたモデル（ノミナルモデルと呼ぶ）からの誤差に対しても有効な（安定性を失わない） 性質を[ロバスト性](https://ja.wikipedia.org/wiki/ロバストネス "wikilink")（堅牢性、安定性）と呼ぶ。

それまでの現代制御論はモデルが正確であることを前提としていたため、モデル化誤差のあるシステムに対して性能を保証しなかったが、H<sup>∞</sup>制御はロバスト性により多少いいかげんな同定でも許されるようになったこと、周波数領域での設計ができるようになったために古典制御に慣れた技術者が容易に設計できることなどから、産業界で積極的に採り入れられ、理論と現場の距離を縮めたと言われている。

## 主な概念

### モデル表現

  - \(H^\infty\)ノルム (H-infinity norm)
    伝達関数の評価指標であり、入力が出力におよぼす**最大**の（入力が外乱であれば最悪の）影響を見積もることができる。\(H^\infty\)は、伝達関数の Hardy 空間\(H^\infty\)におけるノルムを評価規範としていることに由来する。伝達関数\(G\in H^\infty\)の\(H^\infty\)ノルムは、全周波数領域における最大特異値と定義される。
    <math style="margin-left:2em;">

\\|G\\|_\\infty = \\sup_{\\omega} \\sigma (G(j\\omega)). </math>

  -
    ただし\(\sigma(\cdot)\) は最大特異値である。特に伝達関数が[スカラー](https://ja.wikipedia.org/wiki/スカラー "wikilink")である場合は全周波数領域におけるゲインの上界となる。
    <math style="margin-left:2em;">

\\|G\\|_\\infty = \\sup_{\\omega} |G(j\\omega)|. </math>

  - 一般化プラント (generalized plant)
    **制御入力** \(u\), **外乱入力** \(w\), **制御出力** \(y\), **評価出力** \(z\) の 4 つの入出力を持つ、汎用的な制御モデルである。
    [Generalized_Plant.png](https://ja.wikipedia.org/wiki/File:Generalized_Plant.png "fig:Generalized_Plant.png")
    この系は、下図のようなフィードバック則 \(u = Ky\) を適用することを前提としている。
    [Generalized_Feedback.png](https://ja.wikipedia.org/wiki/File:Generalized_Feedback.png "fig:Generalized_Feedback.png")
    補償器 \(K\) を適当に選ぶことで外乱入力 \(w\) から評価出力 \(z\) までの伝達関数の H<sup>∞</sup>ノルム \(\|G_{zw}\|_{\infty}\) を望みの値より小さくすることができれば、**最悪外乱**に対して所望の外乱抑制効果を保証することができる。
    状態空間表現では
    <math style="margin-left:2em;">\\begin{matrix}

\\dot{x} & = \&Ax + B_1 w + B_2 u\\\\ z & = & C_1 x + D_{11} w + D_{12} u\\\\ y & = & C_2 x + D_{21} w + D_{22} u \\end{matrix} </math>

  -
    のように表される。

### 解析手法

  - 小ゲイン定理 (small gain theorem)
    閉ループ系の構成要素となる各ブロックの積の H<sup>∞</sup>ノルムが 1 未満であれば、閉ループ系は安定であるという定理。

  - 混合感度問題 (mixed sensitivity problem)

  - 正規化既約分解 (normalized coprime factorization)

### 制御系設計

  - 標準問題 (standard problem)
    プロパーな制御器 \(u = K(s)y\) によって、与えられた \(\gamma\) について、*ノルム条件*
    <math style="margin-left:2em;">

\\|G\\|_{\\infty} \< \\gamma </math>

  -
    を満たす \(K(s)\) を見出す問題。\(\gamma\) が小さければ小さいほど外乱抑制性能が優れていることになる。2 次の[リッカチ方程式](https://ja.wikipedia.org/wiki/リッカチ方程式 "wikilink")を解く問題に帰着されるが、一般に解析的な解が得られないため、与えられた \(\gamma\) について可解であるかどうかは、リッカチ方程式を解いてみるまで分からない。
  - ガンマイタレーション (Gamma Iteration)
    繰り返し標準問題を解くことによって、ノルム条件を満たす最小の \(\gamma\) を極値探索法で見つけること。これにより制御器を得ることを H<sup>∞</sup>最適制御問題と呼ぶ。

## 関連項目

  - [制御理論](../Page/制御理論.md "wikilink")
      - [線形システム論](../Page/線形システム論.md "wikilink")
      - [最適制御理論](https://ja.wikipedia.org/wiki/制御理論#最適制御理論 "wikilink")

[Category:制御理論](https://ja.wikipedia.org/wiki/Category:制御理論 "wikilink")