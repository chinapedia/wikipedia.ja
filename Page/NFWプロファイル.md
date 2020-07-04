> この記事は[NFWプロファイル](https://ja.wikipedia.org/wiki/NFWプロファイル)から翻訳されています。


**NFWプロファイル** () は[ダークマターハロー](https://ja.wikipedia.org/wiki/ダークマターハロー "wikilink")の密度プロファイルのモデル。[N体シミュレーション](../Page/N体シミュレーション.md "wikilink")で得られるハローは普遍的にNFWプロファイルを持つ。このプロファイルを最初に提案した [Julio Navarro](https://ja.wikipedia.org/wiki/:en:Julio_Navarro_\(astrophysicist\) "wikilink")、[Carlos Frenk](https://ja.wikipedia.org/wiki/:en:Carlos_Frenk "wikilink")、[サイモン・ホワイト](../Page/サイモン・ホワイト.md "wikilink")にちなんで命名された\[1\]\[2\]\[3\]。

## 概要

[NFW_vs_Einasto_profile.svg](https://ja.wikipedia.org/wiki/File:NFW_vs_Einasto_profile.svg "fig:NFW_vs_Einasto_profile.svg")

NFWプロファイルは \(r\) を動径座標として次式で定義される球対称密度プロファイル \(\rho ( r )\) のことをいう。

\[\rho ( r ) = \frac{ \rho_s }{ \frac{ r }{ r_s } \left( 1 + \frac{ r }{ r_s } \right)^2 }\] ここに \(\rho_s\), \(r_s\) はパラメータで、\(r_s\) をスケール半径と呼ぶ。\(r \ll r_s\) で \(\rho \propto r^{-1}\)、\(r \gg r_s\) で \(\rho \propto r^{-3}\) というべき関数へと漸近する。ハローの[ビリアル半径](https://ja.wikipedia.org/wiki/ビリアル半径 "wikilink") \(R_{200m}\) とスケール半径 \(r_s\) の比 \(c_{200m} := \frac{ R_{200m} }{ r_s }\) を concentration parameter と呼ぶ。

NFWプロファイルでは動径 \(r\) 以内の質量 \(M ( r )\) および重力ポテンシャル \(\Phi ( r )\) が解析的に求まり

\[M ( r ) = 4 \pi \rho_s r_s^3 \left[ \ln \left( 1 + \frac{ r }{ r_s } \right) - \frac{ r / r_s }{ 1 + r / r_s } \right] ,\]

\[\Phi ( r ) = - 4 \pi G \rho_s r_s^2 \frac{ \ln \left( 1 + r / r_s \right) }{ r / r_s }\] となる。このようにNFWプロファイルは解析的な取り扱いが容易であるため、ハローの理論モデルとして広く採用されている\[4\]。ただし質量 \(M ( r )\) は極限 \(r \to \infty\) で対数発散する。

## 歴史

[1996年](../Page/1996年.md "wikilink")に Navarro, Frenk, White はN体シミュレーションの中で[矮小銀河](../Page/矮小銀河.md "wikilink")から[銀河団](../Page/銀河団.md "wikilink")までの異なる質量スケールのダークマターハローを選び出し、その密度プロファイルを比較したところ、ハロー質量によらず普遍的に同じプロファイルを与えることに気付いた\[5\]。彼らはさらに研究を進め、ハロー密度プロファイルが初期密度ゆらぎのパワースペクトルや[宇宙論パラメータ](../Page/宇宙論パラメータ.md "wikilink")にさえ依存しないと結論した\[6\]。[無衝突重力多体系](https://ja.wikipedia.org/wiki/無衝突重力多体系 "wikilink")でこのような普遍的な構造が得られたことは驚きを持って受け止められ、この普遍性がシミュレーションの解像度のためなのではないか、あるいは重力の近距離発散を除去するε-処方の効果なのではないか、という疑問を引き起こした。

[福重俊幸](https://ja.wikipedia.org/wiki/福重俊幸 "wikilink")と[牧野淳一郎](../Page/牧野淳一郎.md "wikilink")は1997年に[GRAPE](../Page/GRAPE.md "wikilink")を用いたより高解像度のシミュレーションに基づいてハロー中心部での密度スロープはより急な \(-1.5\) 程度であると主張し\[7\]、この結果は [Ben Moore](https://ja.wikipedia.org/wiki/:en:Ben_Moore_\(astrophysicist\) "wikilink") ら\[8\]らによって支持された。福重、牧野による[2001年](../Page/2001年.md "wikilink")のシミュレーション\[9\]も同じ結果を示している。この場合、密度プロファイルとしてはNFWプロファイルを一般化した

\[\rho ( r ) = \frac{ \rho_s }{ \left( \frac{ r }{ r_s } \right)^\gamma \left( 1 + \frac{ r }{ r_s } \right)^{3-\gamma} }\] という形のプロファイルになる。一方で Y. P. Jing は2001年に密度プロファイルが普遍的なのはサンプルセレクションのためであり、実際にはハローは多様なプロファイルを持つと主張した\[10\]。

[2004年](../Page/2004年.md "wikilink")になって Navarro らは [Jaan Einasto](https://ja.wikipedia.org/wiki/:en:Jaan_Einasto "wikilink") が[1965年](../Page/1965年.md "wikilink")に[銀河](../Page/銀河.md "wikilink")モデルの文脈で提案した[アイナストプロファイル](https://ja.wikipedia.org/wiki/アイナストプロファイル "wikilink")

\[\rho ( r ) = \rho_{-2} \exp \left[ - \frac{ 2 }{ \alpha } \left\{ \left( \frac{ r }{ r_{-2} } \right)^\alpha - 1 \right\} \right]\] がダークマターハローの密度プロファイルとしてより適切であると主張した。このプロファイルは

\[\frac{ d \ln \rho }{ d \ln r } = - 2 \left( \frac{ r }{ r_{-2} } \right)^\alpha\] からわかるように、密度スロープが動径 \(r\) のべき関数という形で変化する。Hayashi & White による Millennium Simulation の解析\[11\]、および [Volker Springel](https://ja.wikipedia.org/wiki/:de:Volker_Springel "wikilink") らによる Aquarius Project の成果\[12\]などのより新しいシミュレーションもまたアイナストプロファイルを支持している。

2010年現在でもN体シミュレーションにおいてダークマターハローの密度プロファイルとしてNFWプロファイル（またはアイナストプロファイル）がなぜ普遍的に現れるのかという疑問に対するコンセンサスの得られた解答は提出されていない\[13\]。

## 観測との比較

NFWプロファイルは暗黒物質のみを含むシミュレーションから得られたものであり、現実的には[バリオン](https://ja.wikipedia.org/wiki/バリオン "wikilink")の効果によりハロー中心部の密度プロファイルはNFWプロファイルの予言から逸脱すると予想されている\[14\]。しかしながら、バリオンの効果が効かないと考えられている[低表面輝度銀河](https://ja.wikipedia.org/wiki/低表面輝度銀河 "wikilink")や[矮小銀河](../Page/矮小銀河.md "wikilink")の[Hα線](https://ja.wikipedia.org/wiki/Hα線 "wikilink")を用いた観測が[2001年](../Page/2001年.md "wikilink")頃から進展し、その結果[銀河の回転曲線に基づいて得られた密度プロファイルはハロー中心部でNFWプロファイルとは一致せず](https://ja.wikipedia.org/wiki/銀河の回転曲線問題 "wikilink")、スロープは \(\gamma \sim 0\) 程度（コア型のプロファイル）であることが示唆された\[15\]\[16\]。このシミュレーションと観測の不一致は「[コア-カスプ問題](https://ja.wikipedia.org/wiki/コア-カスプ問題 "wikilink")」と呼ばれ、[コールドダークマター](https://ja.wikipedia.org/wiki/コールドダークマター "wikilink")モデルの小スケールでの破綻を示している可能性が議論されている\[17\]。

## 脚注

## 関連項目

  - [暗黒物質](../Page/暗黒物質.md "wikilink")
  - [銀河](../Page/銀河.md "wikilink")
  - [銀河団](../Page/銀河団.md "wikilink")

[Category:宇宙の大規模構造](https://ja.wikipedia.org/wiki/Category:宇宙の大規模構造 "wikilink") [Category:暗黒物質](https://ja.wikipedia.org/wiki/Category:暗黒物質 "wikilink") [Category:エポニム](https://ja.wikipedia.org/wiki/Category:エポニム "wikilink") [Category:天文学に関する記事](https://ja.wikipedia.org/wiki/Category:天文学に関する記事 "wikilink")

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