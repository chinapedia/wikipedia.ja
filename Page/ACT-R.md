> この記事は[ACT-R](https://ja.wikipedia.org/wiki/ACT-R)から翻訳されています。


**ACT-R**（Adaptive Control of Thought--Rational、思考の適応制御--理性）とは、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の[ジョン・R・アンダーソン](../Page/ジョン・R・アンダーソン.md "wikilink")を中心として開発された[認知アーキテクチャ](../Page/認知アーキテクチャ.md "wikilink")である。他の認知アーキテクチャと同様、ACT-R は人間の精神を成り立たせる基本的な認識と知覚の操作を定義することを目指している。理論上、人間の行う行為は、そのような個々の操作の連鎖から成っているとされている。

ACT-R の根底にある仮定のほとんどは[認知神経科学](../Page/認知神経科学.md "wikilink")(cognitive neuroscience)の進歩に触発されたものでもあり、実際 ACT-R は脳内の個々の処理モジュールによって認識を生み出す過程を説明するものと言う事もできる。

## 影響を与えたもの

他の多くの認知アーキテクチャと同様、ACT-R は[アレン・ニューウェル](../Page/アレン・ニューウェル.md "wikilink")の業績、特に彼のライフワークである[認知の理論統一に触発されたものである](https://ja.wikipedia.org/wiki/認知の統一理論 "wikilink")\[1\]。実際、[ジョン・R・アンダーソン](../Page/ジョン・R・アンダーソン.md "wikilink")は理論を構築するにあたって最大の影響を受けた人物として[アレン・ニューウェル](../Page/アレン・ニューウェル.md "wikilink")を挙げている。

## ACT-R とは

他の有力な認知アーキテクチャ（[Soar](../Page/Soar_\(認知アーキテクチャ\).md "wikilink")、、など）と同様、ACT-R 理論には専用言語の[インタプリタ](../Page/インタプリタ.md "wikilink")という形態の計算可能な実装がある。インタプリタ自体は[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")言語で書かれており、一般的なLISP言語処理系で実行可能である。

従って、研究者が ACT-R のウェブサイトからコードをダウンロードして LISP 処理系上で実行すれば、ACT-R インタプリタの形式でその理論に触れることが可能である。

また、これによって ACT-R 言語の[スクリプト](../Page/スクリプト.md "wikilink")という形式で人間の認知モデルを指定することも可能である。言語の基本構文とデータ型は認知に関する理論的前提を反映するよう設計されている。それらの前提は、[認知心理学](../Page/認知心理学.md "wikilink")の実験や脳画像処理で得られた多くの知見に基づいている。

一般の[プログラミング言語](../Page/プログラミング言語.md "wikilink")と同様、ACT-R はフレームワークである。タスク（例えば、ハノイの塔、テキストや単語の記憶、言語理解、コミュニケーション、航空機の制御など）毎に ACT-R 上で「モデル」（すなわち、プログラム）を作成する。これらのモデルは、ACT-R の持つ認知についての観点内でのモデル作成者の前提を反映している。作成されたモデルは実行される。

モデルを実行することは、認知の個々の操作（すなわち、記憶の処理と検索、視聴覚の処理、運動制御、精神像操作など）を指定する人間の行為の逐次的シミュレーションを行うことと等しい。各ステップには実行時間と正確度に関する量的予測が関連付けられている。実験で収集されたデータとモデルの実行結果を比較することで、そのモデルを評価することができる。

近年、ACT-R は [fMRI](https://ja.wikipedia.org/wiki/fMRI "wikilink") によって得られるような脳内の活性化パターンの量的予測も行えるよう拡張された。特に ACT-R は、[運動皮質](https://ja.wikipedia.org/wiki/運動皮質 "wikilink")の目と口に関する部分、左[前頭前皮質](https://ja.wikipedia.org/wiki/前頭前皮質 "wikilink")、前[帯状皮質](https://ja.wikipedia.org/wiki/帯状回 "wikilink")、[基底核などの脳内各部の正確な反応形態と反応時間を予測することに注力してきた](../Page/大脳基底核.md "wikilink")。

### 概要

ACT-R の最も重要な前提は、人間の知識が2つの根源的な種類に分けられる、ということである。その2つとは、「[宣言的記憶](https://ja.wikipedia.org/wiki/宣言的記憶 "wikilink")」と「[手続き的記憶](https://ja.wikipedia.org/wiki/手続き的記憶 "wikilink")」である。

ACT-R のコード内で、宣言的知識は「チャンク; chunks」という形態で表現される。これはすなわち、個人の属性のベクトル表現であり、それらに対して個別のラベルを付されたスロットからアクセス可能となっている。

チャンクは「バッファ」を通してアクセス可能である。バッファは「モジュール」のフロントエンドであり、モジュールとは脳内のほぼ独立した機能部分を意味する。

モジュールには、以下の2種類が存在する:

  - **知覚運動モジュール**は、実世界（すなわちシミュレーションされた実世界）とのインターフェイスを受け持つ。ACT-R で最もよく開発された知覚運動モジュールは視覚モジュールと手のモジュールである。
  - **記憶モジュール**。ACT-R には以下の2種類の記憶モジュールがある:
      - **宣言的記憶**は、事実を保持する。例えば、「合衆国の首都はワシントンD.C.」、「フランスはヨーロッパの国家」、「2+3=5」など。
      - **手続き的記憶**は、プロダクションから構成される。プロダクションとは、人間の行為の方法に関する記憶である。例えば、キーボードで "Q" をタイプする方法、車を運転する方法、足し算をする方法などである。

全てのモジュールは対応するバッファを通してのみアクセス可能である。ある時点のバッファの内容は、その時点の ACT-R の状態を表している。手続き的記憶モジュールは例外で、ここには手続き的知識が格納され、それを適用する。従って、アクセス可能なバッファを持たず、他のモジュールの内容にアクセスするのに使われる。

手続き的知識は「プロダクション」の形式で表現される。「プロダクション」という用語は ACT-R が一種の[プロダクションシステム](../Page/プロダクションシステム.md "wikilink")であることにも由来しているが、実際プロダクションは主に皮質（バッファ）から基底核、基底核から皮質という情報の流れを形式的に表現するものと言える。

各瞬間に、バッファの現状と一致するプロダクションを検索するパターン照合器が動作する。ある瞬間には1つだけプロダクションが選択され実行される。プロダクションを実行するとバッファの内容が変更され、システムの状態が変化する。従って ACT-R における認知は、プロダクションの逐次的実行として展開される。

### 記号主義 vs. コネクショニズム の論争

[認知科学](../Page/認知科学.md "wikilink")において、「[記号主義](https://ja.wikipedia.org/wiki/認知主義 "wikilink")」的アプローチと「[コネクショニズム](../Page/コネクショニズム.md "wikilink")」的アプローチがあり、ACT-R は一般に「記号主義」的であると見なされている\[2\]。その実体（チャンクとプロダクション）は離散的で、その操作は統語論的であり、その表現の内容を意味論的に参照せず、計算に必要な属性だけを参照する。そのことは、チャンクのスロットとバッファの属性がプロダクションと一致する際に標準記号変数として機能することからも明らかである。

しかし、ACT-R 開発者を中心とする人々は ACT-R を脳の構成とその上で如何にして精神と呼ばれるものが生み出されるかを示すための汎用フレームワークであるとしている。しかし認知への記号的アプローチは精神を説明することを目標としているので、これはACT-Rを記号システムに分類することへの反論にはなっていない。

ACT-Rは脳の機能を解明しようとしているので記号システムではないという誤解は、2つの点で不正確である。第一に精神は脳の機能であるので、記号的であれそれ以外であれ、認知の計算モデルは全て脳機能を何らかの観点で特徴付けなければならない。第二に重要な一般化を行えるのは認知レベルのみなので、コネクショニズムのアプローチも含めあらゆるそういったアプローチは神経レベルではなく認知レベルで精神を特徴づけようとする\[3\]。

さらなる誤解が生まれる背景には、ACT-Rのある属性の持つ連想的性質があり、例えばチャンクが互いに活性化しあったり、チャンクとプロダクションがそれらの選択に関連する量的属性を持っている点がある。それら属性のユニット選択、さらには計算における役割が何であれ、記号的であることの基本的性質には反しない。

### 理論 vs. 実装、そしてバニラ ACT-R

ACT-R 開発者は、理論と実装を区別する重要性を強調する。

実際、実装のほとんどは理論を反映していない。例えば、実装では計算の都合のためだけに存在するモジュールもあり、それらは脳内の何かを表現しているわけではない（例えば、ある計算モジュールには擬似乱数発生器があって、ノイズ的パラメータを生成するのに使われている。また、別のモジュールにはデータ構造を名前で参照できるように名前をつける機能がある）。

また、実際の実装は研究者が理論を修正できるよう設計されていて、標準パラメータを変更したり、新たなモジュールを追加したり、既存のモジュールの動作を修正したりできる。

アンダーソンの[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")内の研究室が公式の ACT-R のコードをリリースしているが、それ以外の実装も存在する。そのような実装としては、*jACT-R*\[4\]（[ピッツバーグ大学](../Page/ピッツバーグ大学.md "wikilink")の Anthony M. Harrison が[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で作成）や *Python ACT-R*\[5\]（カナダのカールトン大学の Terrence C. Stewart、Robert L. West が[Python](../Page/Python.md "wikilink")で作成）がある。

同様に、1993年版の理論に基づく本格的実装として ACT-RN があった（現在、開発は継続していない）\[6\]。これらはいずれも完全に機能し、モデルをこれらの上で作成して実行できる。

このような実装上の自由度があるため、LISPベースでオリジナルから変更されていない公式バージョンを「バニラ ACT-R; Vanilla ACT-R」と称する。

## 応用

ACT-R モデルは700以上の科学的出版物で扱われ、他の数多くの論文や出版物で引用されてきた。

### 記憶、注意、実行制御

ACT-Rの宣言的記憶システムは、当初から人間の[記憶](../Page/記憶.md "wikilink")のモデル化に使われてきた。長年、数多くの既知の現象をうまくモデル化するために採用されている。例えば、関連情報の干渉によるファン効果\[7\]、リスト形式におけると\[8\]、逐次的想起\[9\]などがある。

ACT-Rはいくつかの認知パラダイムにおける注意と制御のプロセスのモデル化にも使われてきた。例えば、[ストループ課題](../Page/ストループ効果.md "wikilink")\[10\]\[11\]、\[12\]\[13\]、\[14\]、マルチタスキング\[15\]などがある。

### 自然言語

ACT-Rを[自然言語](../Page/自然言語.md "wikilink")の理解と生成のいくつかの観点のモデル化に使っている研究者もいる。例えば、構文解析のモデル\[16\]、言語理解のモデル\[17\]、言語獲得のモデル\[18\]、隠喩理解のモデル\[19\]などがある。

### 複雑な課題

ACT-Rは、[ハノイの塔](../Page/ハノイの塔.md "wikilink")\[20\]や方程式\[21\]のような複雑な課題を人間が解く過程を捕らえることにも使われてきた。また、自動車や航空機の操縦における人間の挙動のモデル化にも使われてきた\[22\]。

知覚運動機能の統合により、ACT-Rは[人間工学](../Page/人間工学.md "wikilink")や[マンマシンインタフェース](../Page/マンマシンインタフェース.md "wikilink")のモデリングツールとしてもよく使われるようになってきた。例えば、様々な状況での自動車運転をモデル化したり\[23\]\[24\]、[コンピュータアプリケーションにおけるメニュー選択や視覚の動きをモデル化したり](../Page/アプリケーションソフトウェア.md "wikilink")\[25\]\[26\]、ウェブページの誘導のモデル化をしたり\[27\]といった使われ方がある。

### 認知神経科学

さらに最近では、イメージを想起したときの脳の活性化パターンの予測にもACT-Rが使われている\[28\]。この分野での成功例としては、記憶検索における[前頭前野と](https://ja.wikipedia.org/wiki/前頭前皮質 "wikilink")[頭頂葉](../Page/頭頂葉.md "wikilink")の活動の予測\[29\]、[前帯状皮質](https://ja.wikipedia.org/wiki/前帯状皮質 "wikilink")の制御活動のモデル化\[30\]、経験に伴う脳活動の変化のモデル化などがある\[31\]。

### 教育

ACT-Rは [cognitive tutor](https://ja.wikipedia.org/wiki/:en:Cognitive_tutor "wikilink") という学習システムの基盤としてもよく採用されてきた\[32\]\[33\]。それらシステムでは、ACT-Rを使って内部に（児童など）学習者個人のモデルを構築し、各課題をその学習者がどの程度難しいと感じるかを推定して課題やカリキュラムをパーソナライズし、適切な助言も提供する。

Cognitive Tutor は Pittsburgh Science of Learning Center での学習および認知のモデリングの研究にも使われている。最も成功した応用として、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")内の数千の学校で利用されている数学用 Cognitive Tutor がある。

## 歴史

### 初期: 1973年-1990年

ACT-Rは[ジョン・R・アンダーソン](../Page/ジョン・R・アンダーソン.md "wikilink")によって開発された人間の認知に関する一連のモデルの最終的な後継である。

その起源は、1973年、[ジョン・R・アンダーソン](../Page/ジョン・R・アンダーソン.md "wikilink")とが共同開発した人間の記憶に関する HAM モデルであり、共同執筆された論文 "Human Associative Memory" で述べられている\[34\]。その後、オリジナルの HAM モデルを拡張した最初の ACT 理論が生まれた\[35\]。その中で初めて、宣言的記憶システムに手続き的記憶が追加され、後に実際の脳にもそれに相当するものがあると証明された\[36\]。その後も理論は ACT\* モデルとして拡張されている\[37\]。

### ACT-Rの誕生: 1990年-1998年

1980年代終盤、アンダーソンは Rational Analysis と名づけた認知に関する数学的アプローチの研究と普及に専念した\[38\]。Rational Analysis の基本となる前提は、認知が最適順応的であることであり、認知機能の正確な推測は環境の統計的属性を反映していることである\[39\]。その後アンダーソンはACT理論の開発に戻り、Rational Analysis を基盤となる計算を統合するのに使った。その重要性を示すため、Rational Analysis から "R" を取って ACT-R と名称が変更された\[40\] 。

1993年、アンダーソンはカスケード相関学習アルゴリズムで有名な[コネクショニズム](../Page/コネクショニズム.md "wikilink")の研究者 Christian Lebiere と出会った。彼らの共同研究は ACT-R 4.0 として結実した\[41\]。[ライス大学](../Page/ライス大学.md "wikilink")の Mike Byrne の尽力により、4.0 にはアーキテクチャに影響された知覚運動機能が追加された。これにより応用の幅が大きく広がった。

### 現在の開発: 1998年以降

ACT-R 4.0 をリリース後、アンダーソンは彼の理論と神経との関連に興味を持つようになり、脳画像処理技術を使って人間の精神の根底にある働きを理解することを目標とするようになった。

脳内の活動の局所性を説明するため、理論は大幅な修正を必要とした。2002年の ACT-R 5.0 ではモジュールの概念が導入され、手続き的表現と宣言的表現の組み合わせによって既知の脳の仕組みをマッピングするようになった\[42\]。さらに手続き的知識と宣言的知識の相互作用は新たに導入されたバッファ（アクティブな情報を一時的に保持する特別な構造）で実現されている。バッファは皮質の活動に対応すると考えられ、その後の研究によって皮質での活動とバッファ上の計算がうまく対応していることがわかった。

その後、理論に重大な変更は加えられていないが、新たな完全に書き換えられたコードが 2005年に ACT-R 6.0 としてリリースされた。ACT-R の言語としての機能が大幅に改善されている。

### スピンオフ

ACT-R 理論の長い開発と並行して、関連プロジェクトがいくつか生まれた。

最も重要なものとして PUPS プロダクションシステムがある。これはアンダーソン理論の初期の実装だが、後に破棄された。また、ニューラルネットワーク的実装の ACT-RN\[43\] は主に Christian Lebiere によって開発された。

[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の Lynne Reder は 1990年代初期に[SACと呼ばれる宣言的記憶のモデルを開発した](https://ja.wikipedia.org/wiki/:en:Source_of_activation_confusion_model "wikilink")。これは ACT-R の宣言的記憶システムと（前提に一部違いはあるが）大部分の機能が同等である。

## 脚注

## 参考文献

  - Anderson, J. R. (2007). *How can the human mind occur in the physical universe?* New York, NY: Oxford University Press. ISBN 0-19-532425-0.
  - Anderson, J. R., Bothell, D., Byrne, M. D., Douglass, S., Lebiere, C., & Qin, Y . (2004). An integrated theory of the mind. *Psychological Review*, 1036–1060

## 外部リンク

  - [Official ACT-R website](http://act-r.psy.cmu.edu/) （数々のオンライン資料、ソースコード、出版物リスト、チュートリアル）
  - [jACT-R](http://jactr.org) Javaで書き直したACT-R
  - [ACT-R: The Java Simulation & Development Environment](http://cog.cs.drexel.edu/act-r/) もう1つのJavaによるオープンソース実装
  - [PythonACT-R](http://sites.google.com/site/pythonactr/) Pythonでの実装

[Category:認知アーキテクチャ](https://ja.wikipedia.org/wiki/Category:認知アーキテクチャ "wikilink")

1.
2.
3.  Pylyshyn, Z. W. (1984). *Computation and Cognition: Toward a Foundation for Cognitive Science*. Cambridge, MA: MIT Press. ISBN 0-262-66058-X
4.  Harrison, A. (2002). jACT-R: Java ACT-R. *Proceedings of the 8th Annual ACT-R Workshop* [Pdf](http://act-r.psy.cmu.edu/workshops/workshop-2002/talks/AnthonyHarrison.pdf)
5.  Stewart, T. C. and West, R. L. (2005) Python ACT-R: A New implementation and a new syntax. *Proceedings of 12th Annual ACT-R Workshop* [Pdf](http://terrystewart.ca/papers/2005-Reimplementing_ACT-R_full.pdf)
6.  Lebiere, C., & Anderson, J. R. (1993). A connectionist Implementation of the ACT-R production system. In *Proceedings of the Fifteenth Annual Conference of the Cognitive Science Society* (pp. 635-640). Mahwah, NJ: Lawrence Erlbaum Associates
7.  Anderson, J. R. & Reder, L. M. (1999). The fan effect: New results and new theories. *Journal of Experimental Psychology: General*, *128*, 186-197.
8.  Anderson, J. R., Bothell, D., Lebiere, C. & Matessa, M. (1998). An integrated theory of list memory. *Journal of Memory and Language*, *38*, 341-380.
9.  Anderson, J. R. & Matessa, M. P. (1997). A production system theory of serial memory. *Psychological Review, 104*, 728-748.
10. Lovett, M. C. (2005) A strategy-based interpretation of Stroop. *Cognitive Science, 29*, 493-524.
11. Juvina, I., & Taatgen, N. A. (2009). A repetition-suppression account of between-trial effects in a modified Stroop paradigm. *Acta Psychologica, 131(1)*, 72-84.
12. Altmann, E. M., & Gray, W. D. (2008). An integrated model of cognitive control in task switching. *Psychological Review, 115*, 602-639.
13. Sohn, M.-H., & Anderson, J. R. (2001). Task preparation and task repetition: Two-component model of task switching. *Journal of Experimental Psychology: General*.
14. Byrne, M. D., & Anderson, J. R. (2001). Serial modules in parallel: The psychological refractory period and perfect time-sharing. *Psychological Review, 108*, 847-869.
15. Salvucci, D. D., & Taatgen, N. A. (2008). Threaded cognition: An integrated theory of concurrent multitasking. ''Psychological Review', 130(1)', 101-130
16. Lewis, R. L. & Vasishth, S. (2005). An activation-based model of sentence processing as skilled memory retrieval. *Cognitive Science, 29*, 375-419
17. Budiu, R. & Anderson, J. R. (2004). Interpretation-Based Processing: A Unified Theory of Semantic Sentence Processing. *Cognitive Science, 28*, 1-44.
18. Taatgen, N.A. & Anderson, J.R. (2002). Why do children learn to say "broke"? A model of learning the past tense without feedback. *Cognition*, *86(2)*, 123-155.
19. Budiu R., & Anderson J. R. (2002). Comprehending anaphoric metaphors. *Memory & Cognition, 30*, 158-165.
20. Altmann, E. M. & Trafton, J. G. (2002). Memory for goals: An activation-based model. *Cognitive Science*, *26*, 39-83.
21. Anderson, J. R. (2005) Human symbol manipulation within an integrated cognitive architecture. *Cognitive Science, 29(3)*, 313-341.
22. Byrne, M. D., & Kirlik, A. (2005). Using computational cognitive modeling to diagnose possible sources of aviation error. *International Journal of Aviation Psychology, 15*, 135-155.
23. Salvucci, D. D. (2006). Modeling driver behavior in a cognitive architecture. *Human Factors*, *48*, 362-380.
24. Salvucci, D. D., & Macuga, K. L. (2001). Predicting the effects of cellular-phone dialing on driver performance. In *Proceedings of the Fourth International Conference on Cognitive Modeling*, pp. 25-32. Mahwah, NJ: Lawrence Erlbaum Associates.
25. Byrne, M. D., (2001). ACT-R/PM and menu selection: Applying a cognitive architecture to HCI. *International Journal of Human-Computer Studies*, *55*, 41-84.
26. Fleetwood, M. D. & Byrne, M. D. (2002) Modeling icon search in ACT-R/PM. *Cognitive Systems Research*, *3*, 25-33.
27.
28. Anderson, J.R., Fincham, J. M., Qin, Y., & Stocco, A. (2008). A central circuit of the mind. *Trends in Cognitive Science*, *12(4)*, 136-143
29. Sohn, M.-H., Goode, A., Stenger, V. A, Carter, C. S., & Anderson, J. R. (2003). Competition and representation during memory retrieval: Roles of the prefrontal cortex and the posterior parietal cortex, *Proceedings of National Academy of Sciences, 100*, 7412-7417.
30. Sohn, M.-H., Albert, M. V., Stenger, V. A, Jung, K.-J., Carter, C. S., & Anderson, J. R. (2007). Anticipation of conflict monitoring in the anterior cingulate cortex and the prefrontal cortex. *Proceedings of National Academy of Science, 104*, 10330-10334.
31. Qin, Y., Sohn, M-H, Anderson, J. R., Stenger, V. A., Fissell, K., Goode, A. Carter, C. S. (2003). Predicting the practice effects on the blood oxygenation level-dependent (BOLD) function of fMRI in a symbolic manipulation task. *Proceedings of the National Academy of Sciences of the United States of America. 100(8)*: 4951-4956.
32. Lewis, M. W., Milson, R., & Anderson, J. R. (1987). The teacher's apprentice: Designing an intelligent authoring system for high school mathematics. In G. P. Kearsley (Ed.), *Artificial Intelligence and Instruction*. Reading, MA: Addison-Wesley. ISBN 0-201-11654-5
33. Anderson, J. R. & Gluck, K. (2001). What role do cognitive architectures play in intelligent tutoring systems? In D. Klahr & S. M. Carver (Eds.) *Cognition & Instruction: Twenty-five years of progress*, 227-262. Lawrence Erlbaum Associates. ISBN 0-8058-3824-4
34. Anderson, J. R., & Bower, G. H. (1973). *Human associative memory*. Washington, DC: Winston and Sons.
35. Anderson, J. R. (1976) *Language, memory, and thought*. Mahwah, NJ: Lawrence Erlbaum Associates. ISBN 0-89859-107-4
36. Cohen, N. J., & Squire, L. R. (1980). Preserved learning and retention of pattern-analyzing skill in amnesia: dissociation of knowing how and knowing that. *Science*, *210(4466)*, 207-210
37. Anderson, J. R. (1983). *The architecture of cognition*. Cambridge, MA: Harvard University Press. ISBN 0-8058-2233-X
38. Anderson, J. R. (1990) *The adaptive character of thought*. Mahwah, NJ: Lawrence Erlbaum Associates. ISBN 0-8058-0419-6
39. Anderson, J. R., & Schooler, L. J. (1991). Reflections of the environment in memory. *Psychological Science*, *2*, 396-408
40. Anderson, J. R. (1993). *Rules of the mind*. Hillsdale, NJ: Lawrence Erlbaum Associates. ISBN 0-8058-1199-0
41. Anderson, J. R., & Lebiere, C. (1998). *The atomic components of thought*. Hillsdale, NJ: Lawrence Erlbaum Associates. ISBN 0-8058-2817-6
42. Anderson, J. R., et al. (2004) An integrated theory of the mind. *Psychological Review*, *111(4)*. 1036-1060
43.