> この記事は[Dendral](https://ja.wikipedia.org/wiki/Dendral)から翻訳されています。


**Dendral**は1960年代の[人工知能](../Page/人工知能.md "wikilink")プロジェクトである。未知の[有機化合物](../Page/有機化合物.md "wikilink")を[質量分析法](../Page/質量分析法.md "wikilink")で分析し、[有機化学](../Page/有機化学.md "wikilink")の知識を使って特定する\[1\]。[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")で、[エドワード・ファイゲンバウム](../Page/エドワード・ファイゲンバウム.md "wikilink")、Bruce Buchanan、[ジョシュア・レーダーバーグ](../Page/ジョシュア・レーダーバーグ.md "wikilink")、Carl Djerassi が開発した\[2\]。プロジェクトは1965年に開始された\[3\]。

ソフトウェアとしてのDendralは、化学者が行うような判断と問題解決の過程を自動化したものであるため、世界初の[エキスパートシステム](../Page/エキスパートシステム.md "wikilink")と言われている\[4\]。2つのプログラム **Heuristic Dendral** と **Meta-Dendral** から構成されている\[5\]。[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")で書かれている\[6\]。

Dendral から派生したシステムとして、[Mycin](../Page/Mycin.md "wikilink")、MOLGEN、MACSYMA、PROSPECTOR、XCON、STEAMER などがある。

*Dendral* という名称は "Dendritic Algorithm"（樹枝状アルゴリズム）に由来する[かばん語](../Page/かばん語.md "wikilink")である\[7\]。

## Heuristic Dendral

Heuristic Dendral は、質量分析法などの実験データと化学に関する[知識ベース](../Page/知識ベース.md "wikilink")を使って、データに適合すると考えられる化学構造を割り出す\[8\]。質量分析法は質量分析計で試料を分析するもので、その分子量（原子構成要素の質量の合計）を決定するのに使われる。例えば水（H2O）の場合、水素の質量が 1.01、酸素の質量が 16.00であることから、その分子量は 18 となり、[マススペクトル](../Page/マススペクトル.md "wikilink")は 18 を中心としたピークを形成する。Heuristic Dendral はこの情報を入力とし、各原子の質量に関する知識と分子の結合に関する規則を使って、分子量が 18 となるような分子の構造を決定する\[9\]。分子量が大きくなると、分子構造は複雑化し、考えられる組合せも急激に増大する。従って、仮説形成の過程で考えられる構造の数を減らすプログラムは必須である。

## Meta-Dendral

Meta-Dendral は、知識獲得システムであり、考えられる分子構造とそれに対応したマススペクトルの組合せを入力とし、構造とマススペクトルの相関関係を説明できる[仮説](../Page/仮説.md "wikilink")を提案する\[10\]。これらの仮説は Heuristic Dendral にフィードバックされ、適用可能性が評価される\[11\]。従って、Heuristic Dendral は実行システム、Meta-Dendral は学習システムと言う事ができる。このプログラムの重要な特徴として、計画-生成-評価パラダイムと[知識工学](https://ja.wikipedia.org/wiki/知識工学 "wikilink")がある\[12\]。

### 計画-生成-評価パラダイム

計画-生成-評価[パラダイム](../Page/パラダイム.md "wikilink")（plan-generate-test paradigm）は[問題解決](../Page/問題解決.md "wikilink")手法の基本であり、**Heuristic Dendral** と **Meta-Dendral** に共通するパラダイムである。**generator**（生成器）が問題に対する解の候補を生成する。Dendral では分子のグラフで表現される。ただし、これは解の候補が膨大な個数にならない場合のみに採用できる手法である。解の候補が膨大である場合、Dendral は生成時点でそれを減らすための方法（制約条件）を見つけなければならない。それをするのが Dendral の **planner**（計画器）であり、問題に固有知識を使って generator のための制約条件を探す「仮説生成」プログラムである。**tester**（評価器）は解候補から制約条件に適合しないものを捨てる。この計画-生成-評価パラダイムの機構により Dendral は1つのシステムとして動作する\[13\]。

### 知識工学

知識工学（knowledge engineering）の第一の目的は、[知識ベース](../Page/知識ベース.md "wikilink")と問題解決技法の効率的な相互作用を達成することである。これは、問題固有の情報をヒューリスティックプログラムに符号化した手続きの開発によって可能となる。従って知識工学の第一の基本コンポーネントは巨大な**知識ベース**である。知識ベースには質量分析法に関する固有の知識、[化学](../Page/化学.md "wikilink")と[グラフ理論](../Page/グラフ理論.md "wikilink")に関する基本的な知識、特定の化学構造の解明に役立つ何らかの知識が格納される\[14\]。Dendral は知識工学部分を通して知識ベースを使うことができ、入力データに適合する考えられる化学構造を特定するときと、解候補を削減できる新たな「汎用規則」を知識ベースに追加するときに使われる。以上により、最終的に少数の解候補が得られ、専門家でなくてもそこから正しい解を見つけることが可能となる。

## ヒューリスティクス

[ヒューリスティクス](../Page/ヒューリスティクス.md "wikilink")とは経験則であり、必ずしも唯一の解が得られるとは限らないアルゴリズムである。しかし、ヒューリスティクスに照らして不適切な解を捨てることで、解候補の数を削減できる\[15\]。ヒューリスティクスを使った問題解決法を「ヒューリスティクスプログラミング」と呼び、Dendral では専門家が問題解決で経験則や特定の情報を使って行っていることをマシン上で再現するために使われている。

ヒューリスティクスプログラミングは人工知能に至る大きなステップであった\[16\]。これにより人間の知性の特定の特徴を自動化することが可能となった。1940年代末、George Polya の著書 *How to Solve It: A New Aspect of Mathematical Method* により、この手法が科学界で一般化していった\[17\]。[ハーバート・サイモン](../Page/ハーバート・サイモン.md "wikilink")は *The Sciences of the Artificial* で、「ヒューリスティックを確かな結論と考えるなら、ガッカリさせられるかもしれない。しかし、ヒューリスティックを全く無視しては、何の進歩もないだろう」と述べている。

## 歴史

20世紀中ごろ、「マシンは思考できるか?」という疑問が科学者、特にマシンに人間的性質を付与しようとしていた科学者らの間で興味の的となった。この分野の第一人者であった[ジョン・マッカーシー](../Page/ジョン・マッカーシー.md "wikilink")はこの概念を[ダートマス会議](../Page/ダートマス会議.md "wikilink")（1956年）の際に[人工知能](../Page/人工知能.md "wikilink")(AI)と名づけた。人工知能は一般に、人間の認知機能に由来すると考えられている事を機械が行えるようにすることと定義される\[18\]。

同じころ、科学（特に生物学）は問題を解くのにコンピュータと人間の協調の実現が必要となっていった\[19\]。例えば[ヘモグロビン](../Page/ヘモグロビン.md "wikilink")などの[蛋白質](https://ja.wikipedia.org/wiki/蛋白質 "wikilink")の構造分析は、複雑すぎてコンピュータなしでは困難となっていた。

1960年代初期、[ジョシュア・レーダーバーグ](../Page/ジョシュア・レーダーバーグ.md "wikilink")はコンピュータを使うようになり、[宇宙生物学](../Page/宇宙生物学.md "wikilink")研究の補助となるような対話型コンピュータの開発に多大な興味を抱くようになった。特に未知の有機物の研究に役立つコンピュータシステムの設計に興味を持った。彼は化学もプログラミングも専門ではなかったので、スタンフォードの化学者 Carl Djerassi に化学に関する面で援助を乞い、[エドワード・ファイゲンバウム](../Page/エドワード・ファイゲンバウム.md "wikilink")にはプログラミングを手伝ってもらい、質量分析法のデータから化学構造を特定する過程を自動化するシステムの開発にとりかかった。ファイゲンバウムは[プログラミング言語](../Page/プログラミング言語.md "wikilink")とヒューリスティクスの専門家であり、Carl Djerassi の化学構造特定法をコンピュータ上に再現するシステムの設計をLederberg が行うのを助けた。彼らは、完成したシステムを **Dendritic Algorithm** (Dendral) と名づけた\[20\]。

Dendral は完成当時、[ケトン](../Page/ケトン.md "wikilink")、[アルコール](https://ja.wikipedia.org/wiki/アルコール "wikilink")、[異性体](https://ja.wikipedia.org/wiki/異性体 "wikilink")などを扱ったときに正確な答えを出せなかった。そこで、Djerassi は化学的にあり得ない構造を解候補から除くよう Dendral に教え込んだ。これにより、専門家でないものでも決定できる程度の構造の組合せを生成できるようになった\[21\]。

Dendralチームは、ファイゲンバウムのLISPプログラムを改良するため、Bruce Buchanan を雇った。Buchanan はファイゲンバウムや Lederberg と同様の考え方であったが、彼は特に仮説形成に興味を持っていた。Joseph November は *Digitizing Life: The Introduction of Computers to Biology and Medicine* の中で「（Buchanan）はシステム（Dendral）が単なる人間の補助というだけでなく、単独で唯一の正解を見つけられるようにしたいと考えていた」と書いている。Buchanan は 仮説生成器として Meta-Dendral を設計した。Meta-Dendral と Dendral は 1966年から1967年に結合され、Heuristic Dendral が生まれた。Heuristic Dendral の従来との違いは、それが単に生化学分野だけでなく、他の分野の似たようなシステムのテンプレートとしても使えるようになっていた点である\[22\]。

## 脚注

[Category:エキスパートシステム](https://ja.wikipedia.org/wiki/Category:エキスパートシステム "wikilink") [Category:人工知能の歴史](https://ja.wikipedia.org/wiki/Category:人工知能の歴史 "wikilink")

1.  November, Joseph A. “Digitizing Life: The Introduction of Computers to Biology and Medicine.” Doctoral dissertation, Princeton University, 2006.
2.  Lederberg, Joshua. How Dendral Was Conceived and Born. ACM Symposium on the History of Medical Informatics, 05 Nov. 1987, Rockefeller University. New York: National Library of Medicine, 1987.
3.  Lindsay, Robert K., Bruce G. Buchanan, Edward A. Feigenbaum, and Joshua Lederberg. Applications of Artificial Intelligence for Organic Chemistry: The Dendral Project. McGraw-Hill Book Company, 1980.
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
18. Berk, A A. LISP: the Language of Artificial Intelligence. New York: Van Nostrand Reinhold Company, 1985. 1-25.
19. Lederberg, Joshua. An Instrumentation Crisis in Biology. Stanford University Medical School. Palo Alto, 1963.
20.
21.
22.