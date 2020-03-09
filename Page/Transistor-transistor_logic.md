> この記事は[Transistor-transistor logic](https://ja.wikipedia.org/wiki/Transistor-transistor_logic)から翻訳されています。


**Transistor-transistor-logic** (TTL) は[バイポーラトランジスタ](https://ja.wikipedia.org/wiki/バイポーラトランジスタ "wikilink")と[抵抗器](../Page/抵抗器.md "wikilink")で構成される[デジタル回路](https://ja.wikipedia.org/wiki/デジタル回路 "wikilink")の一種。論理ゲート段（例えば[ANDゲート](https://ja.wikipedia.org/wiki/ANDゲート "wikilink")）と増幅段のどちらの機能もトランジスタを使って実装しているので、（[RTLや](https://ja.wikipedia.org/wiki/Resistor-transistor_logic "wikilink")[DTLとの対比で](https://ja.wikipedia.org/wiki/Diode-transistor_logic "wikilink")）このように呼ばれている。

[半導体](../Page/半導体.md "wikilink")を用いた[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")の代表的なもののひとつであり、通常+5V単一電源のモノリシック[集積回路](../Page/集積回路.md "wikilink") (IC) ファミリとして、[コンピュータ](../Page/コンピュータ.md "wikilink")、産業用制御機械、測定機器、家電製品、[シンセサイザー](../Page/シンセサイザー.md "wikilink")など様々な用途で使われている。TTLという略称は、[TTL互換の論理レベルの意味で使われることもあり](https://ja.wikipedia.org/wiki/デジタル信号#ロジック電圧レベル "wikilink")、TTL ICとは直接関係ないところでも使われている。例えば電子機器の入出力のラベルなどに表示することがある\[1\]。

DTLの改良品であり、さまざまなメーカーによってICが製造されているが、1970年代に[テキサス・インスツルメンツ](https://ja.wikipedia.org/wiki/テキサス・インスツルメンツ "wikilink")社（以下 TI, Texas Instruments）の[汎用ロジックIC](https://ja.wikipedia.org/wiki/汎用ロジックIC "wikilink")ファミリ（7400シリーズ）が広く普及して業界標準となった。標準シリーズから、高速版、低消費電力版、高速・低消費電力版などのバリエーションを広げ、初期の[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の応用の広がりとともにさらに普及した。しかし、バイポーラトランジスタを使うため、低消費電力化・高集積化・低電圧化には向かず、[CMOS](https://ja.wikipedia.org/wiki/CMOS "wikilink")技術の発達に伴い[デジタルICの主力の座をCMOSに譲った](https://ja.wikipedia.org/wiki/デジタル回路 "wikilink")。

## 歴史

[right](https://ja.wikipedia.org/wiki/ファイル:TexasInstruments_7400_chip,_view_and_element_placement.jpg "wikilink") 1961年、[TRW](https://ja.wikipedia.org/wiki/TRW "wikilink")の James L. Buie が「新たに開発する集積回路の設計技術に特に適した」ものとして発明。当初は *transistor-coupled transistor logic* (TCTL) と名付けられていた\[2\]。最初に製品化されたTTLのICチップは、1963年にシルバニア ([en](https://ja.wikipedia.org/wiki/:en:Sylvania_Electric_Products "wikilink")) が製造したもので Sylvania Universal High-Level Logic family (SUHL) と名付けられた\[3\]。シルバニア製の電子部品は[フェニックス・ミサイルの制御に使われた](https://ja.wikipedia.org/wiki/フェニックス_\(ミサイル\) "wikilink")\[4\]。TIが軍用規格（動作を保証する温度範囲が広い）の5400シリーズICを1964年に発売し、民生用規格でパッケージもプラスチックにした7400シリーズICを1966年に発売すると、TTLは電子システム設計で広く使われるようになっていった\[5\]。

TIの7400ファミリは業界標準となった。[モトローラ](../Page/モトローラ.md "wikilink")、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、[フェアチャイルド](https://ja.wikipedia.org/wiki/フェアチャイルドセミコンダクター "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[Intersil](https://ja.wikipedia.org/wiki/:en:Intersil "wikilink")、[Signetics](https://ja.wikipedia.org/wiki/:en:Signetics "wikilink")、[Mullard](https://ja.wikipedia.org/wiki/:en:Mullard "wikilink")、[シーメンス](../Page/シーメンス.md "wikilink")、[SGS-Thomson](https://ja.wikipedia.org/wiki/STマイクロエレクトロニクス "wikilink")、[ナショナル セミコンダクター](https://ja.wikipedia.org/wiki/ナショナル_セミコンダクター "wikilink")\[6\]\[7\]といった半導体企業が7400ファミリ互換のICを製造した。単に互換TTL部品を各社が製造しただけではなく、他の回路技術を使った互換部品も製造された。ただし[IBM](../Page/IBM.md "wikilink")は他とは互換性のないTTL部品を製造し、社内で[System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink")、[IBM 4300](https://ja.wikipedia.org/wiki/IBM_4300 "wikilink")、[IBM 3081といった製品に使用していた](https://ja.wikipedia.org/wiki/:en:IBM_3081 "wikilink")\[8\]。なお、54シリーズと74シリーズの中間的な位置付けの製品として、64シリーズも存在し、数年間は製造されたがその後廃止となっている。

"TTL" という略称は[バイポーラ汎用ロジックICのその後の世代にも約](https://ja.wikipedia.org/wiki/バイポーラトランジスタ "wikilink")20年にわたって使われ続け、速度や消費電力が改善されていった。最近のロジックICファミリ である 74AS/ALS（アドバンストショットキー）は1985年に登場した\[9\]。2008年時点でも、TIは様々な古い技術の汎用ロジックICを供給し続けているが、価格は以前より高くなっている。一般にTTLロジックICは数百個以上のトランジスタを集積していない。チップ当たりに搭載される機能は、数個の[論理ゲート](https://ja.wikipedia.org/wiki/論理ゲート "wikilink")から[ビットスライス](https://ja.wikipedia.org/wiki/ビットスライス "wikilink")式のマイクロプロセッサの範囲である。TTLの重要な特徴はその低価格さであり、そのためにそれまでアナログ回路で実現していた機能が次々とデジタル化されていった\[10\]。

[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")の先祖の1つとされる [Kenbak-1](https://ja.wikipedia.org/wiki/Kenbak-1 "wikilink") は[CPU](../Page/CPU.md "wikilink")をTTLで構成したもので、1971年当時[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")はまだ入手できなかった\[11\]。1973年の [Xerox Alto](../Page/Alto.md "wikilink") と1981年の [Star](https://ja.wikipedia.org/wiki/Xerox_Star "wikilink") ワークステーションは[GUIを導入したことで知られているが](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、[ALUやビットスライス単位のTTLチップを使って構成されていた](https://ja.wikipedia.org/wiki/演算論理装置 "wikilink")。1990年代まで、多くのコンピュータはLSIの間をTTL互換ロジックで接続するという形で構成されていた。[プログラマブルロジックデバイス](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス "wikilink")などが登場するまで、TTLに代表されるバイポーラ・ロジックICは開発中の[マイクロアーキテクチャ](https://ja.wikipedia.org/wiki/マイクロアーキテクチャ "wikilink")の[プロトタイピング](https://ja.wikipedia.org/wiki/プロトタイピング "wikilink")とエミュレーションに使われていた。

## 実装

### 基本的なTTLゲート

[thumb](https://ja.wikipedia.org/wiki/ファイル:TTL_npn_nand.svg "wikilink")。出力段は単純化してある。\]\] TTLはDTL ([Diode-transistor logic](https://ja.wikipedia.org/wiki/Diode-transistor_logic "wikilink")) を自然に発展させたもので、基本概念は共通である。DTLで入力ダイオードで構成している論理ゲート部分を[マルチエミッタ・トランジスタ](https://ja.wikipedia.org/wiki/マルチエミッタ・トランジスタ "wikilink")のベース-エミッタ接合を使って実現している。IC上のこの構造は、複数のトランジスタのベースとコレクタをまとめるように接続したのと同等である\[12\]。単純なTTL論理ゲートの出力はDTLと同様に[エミッタ接地回路](https://ja.wikipedia.org/wiki/エミッタ接地回路 "wikilink")で増幅される。

全入力にHI電圧 (1) が印加されると、マルチエミッタ・トランジスタのベース-エミッタ接合部に逆バイアスがかかる。このトランジスタは逆方向アクティブモードにあるため（コレクタとエミッタが逆転した状態）、DTLとは対照的に入力から小さい（約10μA）コレクタ電流が流れる。ベース抵抗と供給電圧の組み合わせは実質的に定電流源として機能する\[13\]。マルチエミッタ・トランジスタのベース-コレクタ接合を通して電流が流れ、出力トランジスタのベース-エミッタ接合がONになる。したがって出力電圧は LO (0) になる。

一方の入力電圧がLO (0) になると、対応するマルチエミッタ・トランジスタのベース-エミッタ接合は2つの直列の接合部（マルチエミッタ・トランジスタのベース-コレクタ接合部と後段のトランジスタのベース-エミッタ接合部）と並列に繋がる。すると入力のベース-エミッタ接合部は出力トランジスタのベース電流を入力ソース（接地）に流れ込ませる\[14\]。出力トランジスタのベース電流が遮断されることでスイッチが切れた状態になり\[15\]、出力電圧はHI (1) になる。遷移の間、入力トランジスタはほぼアクティブ領域にある。そのため出力トランジスタのベース電流の大部分を流れなくし、素早くベースの電位を下げる。TTLがDTLに比べて優れているのは、このようにダイオードを使った入力段よりも高速に遷移する点である\[16\]。

出力段の単純なTTLの短所は、出力がHI (1) のときの出力抵抗が高く、その値が完全に出力トランジスタのコレクタ抵抗で決まる点である。そのために接続可能な入力数（[ファン・アウト](https://ja.wikipedia.org/wiki/デジタル回路#ファン・アウト "wikilink")）が制限される。単純な出力段の長所として、出力に負荷が接続されていないときに出力の "1" に対応する電圧が高い（V<sub>CC</sub> に近い）という点が挙げられる。

この種のロジックは出力トランジスタのコレクタ抵抗を省略し、[オープンコレクタ](https://ja.wikipedia.org/wiki/オープンコレクタ "wikilink")出力とすることが多い。そうすると、いくつかの論理ゲートの出力を接続して外部に1つの[プルアップ抵抗](https://ja.wikipedia.org/wiki/プルアップ抵抗 "wikilink")を用意するという設計が可能となり、ワイヤードANDまたはワイヤードORにすることができる。例えば 7401\[17\] や 7403 がそのような構成である。

### 「トーテムポール」出力段のあるTTL

[thumb](https://ja.wikipedia.org/wiki/ファイル:7400_Circuit.svg "wikilink") 単純な出力段では出力抵抗が高いという問題を解決するには、「トーテムポール」出力（[プッシュプル出力](https://ja.wikipedia.org/wiki/プッシュプル出力 "wikilink")）段を追加する。右図のように2つのNPNトランジスタ V<sub>3</sub> と V<sub>4</sub>、ダイオード V<sub>5</sub>、電流を制限する抵抗器 R<sub>3</sub> で構成される。入力がLOのときの電流の制御の考え方がこの構成でも適用されている\[18\]。

V<sub>2</sub> がオフのとき V<sub>4</sub> もオフとなり、V<sub>3</sub> がアクティブ状態となって[コレクタ接地回路](https://ja.wikipedia.org/wiki/コレクタ接地回路 "wikilink")として働き、HI電圧 (1) が出力される。V<sub>2</sub> がオンのとき V<sub>4</sub> もオンとなり、出力はLO電圧 (0) となる。V<sub>2</sub> と V<sub>4</sub> のコレクタ-エミッタ接合は、直列の V<sub>3</sub> のベース-エミッタ と V<sub>5</sub> のアノード-カソード接合をV<sub>4</sub> のベース-エミッタ接合と並列接続する。すると V<sub>3</sub> のベース電流が流れなくなり、このトランジスタはオフになって出力に影響を与えなくなる。この遷移の際に抵抗器 R<sub>3</sub> が直列接続されているトランジスタ V<sub>3</sub> とダイオード V<sub>5</sub>、さらにトランジスタ V<sub>4</sub> に流れる電流を制限する。また、出力電圧がHI (1) のときの出力電流も制限し、接地との短絡接続のときの出力電流も制限する。プルアップ抵抗とプルダウン抵抗を出力段から排除することで、消費電力を増大させずにゲートを強化できる\[19\]\[20\]。

トーテムポール出力段付きTTLの最大の利点は、HI (1) 出力の際の低出力抵抗である。その値はコレクタ接地回路として動作している上段の出力トランジスタ V<sub>3</sub> によって決まる。抵抗器 R<sub>3</sub> は V<sub>3</sub> のコレクタに接続されており、負帰還によってその影響が補償されるため、出力抵抗にはほとんど影響しない。欠点は出力に負荷が接続されていない場合でも出力のHI電圧が低くなる（3.5V以下）という点である。これは、V<sub>3</sub> のベース-エミッタ間と V<sub>5</sub> のアノード-カソード間で電圧降下があるためである。

## インタフェース

論理レベルを0にするには入力に向かって電流が流れなければいけないため、DTLと同様にTTLは「電流シンク・ロジック」といわれる。入力電圧がLOのとき、TTLの入力ソース電流は前段に流れ込むので、そちらで吸収されなければならない。この電流の最大値は基本的TTLゲートで約1.6mAである\[21\]。入力ソースは、こうして流れ込む電流が無視できるレベル（0.8V未満）の電圧しか発生しないよう抵抗値を小さく（500Ω未満）する必要がある。推奨されない使い方だが、使わない入力を常に論理値 "1" にしておくためにどこにも接続しないままにしておくことがある。

標準TTL回路の電源電圧は5[ボルトである](https://ja.wikipedia.org/wiki/ボルト_\(単位\) "wikilink")。TTLの入力信号は接地に対して0Vから0.8VのときLOと定義され、2.2Vから5VのときHIと定義される\[22\]（正確な電圧はロジックの種類や温度によっても異なる）。TTLの出力の電圧範囲はそれよりも狭く、0Vから0.4VがLO、2.6Vから5VがHIとなっていて、それぞれ0.4Vのノイズのための余裕がある。TTLの電圧レベルの規格化により、回路基板上に様々なメーカーのTTLチップが混在することが当たり前となった。同じ製品でも製造日が違えば異なるメーカーのTTLチップを使うことがあった。製造後何年も経った回路基板の修理に新たに製造された同型のTTLチップを使うことが可能である。電気的特性が広く統一されていたため、相性などを考慮する必要がなく、理想的な論理デバイスとして扱えた。

TTL論理ゲートの出力をCMOSゲートの入力に使用する場合など、トーテムポール出力段の論理レベル "1" の電圧を V<sub>CC</sub> に高めるために、出力ピンと V<sub>CC</sub> の間に外部抵抗器をはさんで接続することがある\[23\]。ただしこのようにするとトーテムポール型の出力を単純な基本的TTL出力に戻していることになり、大きな出力抵抗が生じる。

## パッケージ

1965年から1990年にかけての多くの集積回路と同様にTTLデバイスは[スルーホール実装](https://ja.wikipedia.org/wiki/スルーホール実装 "wikilink")用にパッケージされた14ピンから24ピンの[DIPが一般的だった](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#DIP "wikilink")。エポキシ樹脂製 (PDIP) が一般的だが、セラミック製 (CDIP) もある。大規模なハイブリッドIC向けにパッケージされていないビームリードつきのチップダイスも作られている。軍用や航空宇宙用には表面実装パッケージの一種であるフラットパック ([en](https://ja.wikipedia.org/wiki/:en:Flatpack_\(electronics\) "wikilink")) でパッケージされている。今ではTTL互換デバイスの多くは表面実装型のパッケージであり、様々な種類がある。

TTLは全ての入力が1つのベース領域上に形成されるマルチエミッタ・トランジスタになっているため、構造的に集積回路に向いている。個別部品でTTL回路を構成しようとするとコストが高くつくが、ICで実装すると逆にコストが下がる。

## 他の汎用ロジックICファミリとの比較

TTLデバイスは一般に等価な[CMOS](https://ja.wikipedia.org/wiki/CMOS "wikilink")デバイスに比べて消費電力が大きいが、CMOSデバイスがクロック周波数を上げると消費電力が大きくなるのに対して、TTLではそれほど増加しない\[24\]。[ECLに比べると消費電力が少なく設計も容易だが](https://ja.wikipedia.org/wiki/エミッタ結合論理 "wikilink")、スイッチング性能は低い。性能と経済性を両立させるためにTTLとECLを混在させてシステムを構築することもあったが、両ファミリの間にレベルを変換するデバイスを必要とした。初期のCMOSデバイスは[静電気](https://ja.wikipedia.org/wiki/静電気 "wikilink")の放電に対してTTLより弱かった。

TTLデバイスの出力構造により、出力インピーダンスがHI状態とLO状態で異なるため、伝送線の駆動には不向きである。そのため、ケーブルなどで信号を送る際には伝送線駆動のための専用デバイスで出力をバッファリングするのが一般的である。ECLは出力インピーダンスが対称的であり、このような欠点がない。

トーテムポール構造の出力段の場合、上下のトランジスタが同時にONになる瞬間が存在し、電源からの電流がかなりのパルスとなって流れる。このパルスがIC間で影響を及ぼしあい、結果としてノイズマージンが低下し性能も低下する。TTLシステムでは1つか2つのICパッケージ毎に[バイパスコンデンサ](https://ja.wikipedia.org/wiki/バイパスコンデンサ "wikilink")を配置するのが一般的で、それによって電流パルスが他のチップの電源電圧を瞬間的に低下させないようにしている。

いくつかの製造業者は、TTL互換の入出力レベルのCMOSロジックICを販売しており、ピン配置などもTTLと合わせていることが多い。例えば74HCTシリーズは[CMOS](https://ja.wikipedia.org/wiki/CMOS "wikilink")テクノロジーを使い、バイポーラの74シリーズの部品と置換可能である。

## 派生品

技術の進歩により、互換性を保ちながらスイッチング速度や消費電力を改良した部品が生まれた。各ベンダーはそれらを[ショットキーバリアダイオード](https://ja.wikipedia.org/wiki/ショットキーバリアダイオード "wikilink")付きのTTLとして製品化したが、例えばLSファミリなどの回路構成は実際にはDTLに近い\[25\]。

標準TTLファミリでは、ゲート遅延が10ns、電力消費がゲート当たり10mWで、[電力遅延積](https://ja.wikipedia.org/wiki/電力遅延積 "wikilink")（PD積）またはスイッチングエネルギーが約100[pJである](https://ja.wikipedia.org/wiki/ジュール "wikilink")。その派生および後継のファミリとしては次のものがある。

| シリーズ            | 型名表示  | 特徴                                                                                                                         | 消費電力(mW/Gate) | 遅延 t<sub>pd</sub>(nsec) |
| --------------- | ----- | -------------------------------------------------------------------------------------------------------------------------- | ------------- | ----------------------- |
| 標準TTL           | 74    | [1966年](../Page/1966年.md "wikilink")に商品化された初期の標準品                                                                          | 10            | 10                      |
| ローパワーTTL        | 74L   | 初期の低消費電力品。但しスピードを犠牲にしている。[CMOS](https://ja.wikipedia.org/wiki/CMOS "wikilink")に取って代わられた。                                   | 1             | 33                      |
| ハイスピードTTL       | 74H   | スイッチングが速いが、消費電力が大きい。                                                                                                       | 22            | 6                       |
| ショットキーTTL       | 74S   | 入力部に[ショットキーバリアダイオード](https://ja.wikipedia.org/wiki/ショットキーバリアダイオード "wikilink")を使って電荷蓄積を防ぎ、より高速なスイッチングを可能にした。ただし消費電力がやはり大きい。 | 19            | 3                       |
| ローパワーショットキーTTL  | 74LS  | 1970年代後半～80年代前半の標準TTL。高い抵抗値で消費電力を低減させ、ショットキーダイオードで高速スイッチングを両立させた。PD積は約20pJ。                                                | 2             | 9.5                     |
| FAST            | 74F   | 1980年代中ごろにフェアチャイルドが発売した高速ショットキーTTL。PD積は約10pJ。                                                                              | 4             | 2.5                     |
| アドバンストショットキーTTL | 74AS  | 1980年代中ごろに出たS-TTLの改良品                                                                                                      | 20            | 1.5                     |
| アドバンストLS-TTL    | 74ALS | 1980年代中ごろに出たLS-TTLの改良品。PD積は約4pJと最も小さい。                                                                                     | 1             | 4                       |

多くの製造業者が動作温度範囲が民生用のものとより広範囲な軍事用のものを製品化している。54シリーズは[MIL規格](https://ja.wikipedia.org/wiki/MIL規格 "wikilink")、74シリーズは一般用の品質保証規格で製造販売される[民生用](https://ja.wikipedia.org/wiki/民生用 "wikilink")である。例えば、TIの74シリーズは0℃から75℃までとされているが、54シリーズは-55℃から+125℃までとなっている。軍事用や航空宇宙用に特に品質を高めた高信頼部品もある。放射線耐性を高めたものもある。

### TTL入出力電圧 (V)

基準とされる電圧レベル

  - Hiレベル入力電圧: 2.0[V以上](https://ja.wikipedia.org/wiki/ボルト_\(単位\) "wikilink")
  - Lowレベル入力電圧: 0.8V以下
  - Hiレベル出力電圧: 2.4V以上
  - Lowレベル出力電圧: 0.4V以下

## 用途

[VLSI](https://ja.wikipedia.org/wiki/VLSI "wikilink")が登場するまで、TTLのICチップを使って[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")や[メインフレーム](https://ja.wikipedia.org/wiki/メインフレーム "wikilink")のプロセッサを構築するのが標準的技法だった。例えば、[DECの初期の](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[VAX](https://ja.wikipedia.org/wiki/VAX "wikilink")や[データゼネラル](https://ja.wikipedia.org/wiki/データゼネラル "wikilink")の[Eclipseがそのような構成である](https://ja.wikipedia.org/wiki/Eclipse_\(コンピュータ\) "wikilink")。他にも[数値制御](https://ja.wikipedia.org/wiki/数値制御 "wikilink")の工作機械、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")、ビデオディスプレイ[端末](../Page/端末.md "wikilink")などで使われている。[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")が広まるとTTLは「[グルーロジック](https://ja.wikipedia.org/wiki/グルー・ロジック "wikilink")」として重要になり、マザーボード上でVLSIで実装された機能ブロック間を繋ぐ役割を担うようになった。

### アナログ回路での利用

元々はデジタル信号を扱うよう設計されているが、TTLの[インバータはアナログ増幅器としても使える](https://ja.wikipedia.org/wiki/NOTゲート "wikilink")。出力と入力の間を抵抗器で繋ぐと、負帰還増幅回路として機能する。アナログ信号をデジタルに変換する場合などに使われるが、単にアナログの増幅を行う用途ではTTLインバータを使うことはない\[26\]。TTLインバータは[水晶振動子](https://ja.wikipedia.org/wiki/水晶振動子 "wikilink")の信号増幅にも使われる。

## 脚注・出典

## 参考文献

  - <cite id=CITEAyersn.d.>Ayers, J. [UConn EE 215 notes for lecture 4.](http://people.seas.harvard.edu/~jones/es154/lectures/lecture_7/pdfs/215ln04.pdf) Harvard University faculty web page. Archive of web page from University of Connecticut. n.d. Retrieved 17 September 2008.</cite>
  - <cite id=CITEBuie1966>Buie, J. [*Coupling Transistor Logic and Other Circuits.*](http://www.google.com/patents?id=tZAdAAAAEBAJ&printsec=abstract&zoom=4&dq=3,283,170+%22newly+developing%22) (U.S. Patent 3,283,170). 1 November 1966. United States Patent and Trademark Office. 1 November 1966.</cite>
  - <cite id=CITEComputerHistoryMuseum2007>The Computer History Museum. [*1963 - Standard Logic Families Introduced.*](http://www.computerhistory.org/semiconductor/timeline/1963-TTL.html) 2007. Retrieved 16 April 2008.</cite>
  - <cite id=CITETI1973>Engineering Staff. *The TTL Data Book for Design Engineers.* 1st Ed. Dallas: Texas Instruments. 1973.</cite>
  - <cite id=CITEErin2003>Eren, H. *Electronic Portable Instruments: Design and Applications.* CRC Press. 2003. ISBN 0-8493-1998-6. [Google preview](http://books.google.com/books?id=xwfpvzvNTr4C&pg=PA353&dq=intitle:instruments+intitle:electronic+ttl-outputs&lr=&as_brr=3&ei=Hz6wSKHHDJzOswO6uI3ABA&sig=ACfU3U2jAUGIInuz8NEKLkToZYAqYJTirA#PPT1,M1) available.</cite>
  - <cite id=CITEFairchild>Fairchild Semiconductor. [*An Introduction to and Comparison of 74HCT TTL Compatible CMOS Logic* (Application Note 368).](http://www.fairchildsemi.com/an/AN/AN-368.pdf) 1984. (for relative ESD sensitivity of TTL and CMOS.)</cite>
  - <cite id=CITEHorowitzHill1989>Horowitz, P. and Winfield Hill, W. *The Art of Electronics.* 2nd Ed. Cambridge University Press. 1989. ISBN 0-521-37095-7</cite>
  - <cite id=CITEKlein2008>Klein, E. [*Kenbak-1.*](http://www.vintage-computer.com/kenbak-1.shtml) Vintage-Computer.com. 2008.</cite>
  - <cite id=CITELancaster1975>Lancaster, D. *TTL Cookbook.* Indianapolis: Howard W. Sams and Co. 1975. ISBN 0-672-21035-5.</cite>
  - <cite id=CITEMillman1979>Millman, J. *Microelectronics Digital and Analog Circuits and Systems*. New York:McGraw-Hill Book Company. 1979. ISBN 0-07-042327-X</cite>
  - <cite id=CITEPittler1982>Pittler, M.S., Powers, D.M., and Schnabel, D.L. [System development and technology aspects of the IBM 3081 Processor Complex.](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=5390538) *IBM Journal of Research and Development.* 26 (1982), no. 1:2–11.</cite>
  - <cite id=CITEstandardlogicleveln.d.>[*Standard TTL logic levels.*](http://www.twysted-pair.com/74xx.htm) n.d. Twisted Pair Software.</cite>
  - <cite id=CITETala2006>Tala, D. K. [*Digital Logic Gates Part-V.*](http://www.asic-world.com/digital/gates5.html) asic-world.com. 2006.</cite>
  - <cite id=CITETI1985>Texas Instruments. [*Advanced Schottky Family.*](http://focus.ti.com/lit/an/sdaa010/sdaa010.pdf) 1985. Retrieved 17 September 2008.</cite>
  - <cite id=CITEsiliconfareast2005>[*Transistor-Transistor Logic (TTL).*](http://www.siliconfareast.com/ttl.htm) siliconfareast.com. 2005. Retrieved 17 September 2008.</cite>
  - <cite id=CITEWobschall1987>Wobschall, D. *Circuit Design for Electronic Instrumentation: Analog and Digital Devices from Sensor to Display.* 2d edition. New York: McGraw Hill 1987. ISBN 0-07-071232-8</cite>

## 関連項目

  - [エミッタ結合論理](https://ja.wikipedia.org/wiki/エミッタ結合論理 "wikilink")
  - [デジタル回路](https://ja.wikipedia.org/wiki/デジタル回路 "wikilink")

## 外部リンク

  - [Texas Instruments logic family application notes](http://focus.ti.com/logic/docs/techdocs.tsp?sectionId=452&tabId=1989&techDoc=1&familyId=1&documentCategoryId=1&viewType=1&techFamId=0)
  - [TTL NAND and AND gates](http://ibiblio.org/kuphaldt/electricCircuits/Digital/DIGI_3.html#xtocid653312) from *Lessons In Electric Circuits* by Tony Kuphaldt

[Category:ロジック・ファミリ](https://ja.wikipedia.org/wiki/Category:ロジック・ファミリ "wikilink") [Category:デジタル回路](https://ja.wikipedia.org/wiki/Category:デジタル回路 "wikilink") [Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink")

1.  [Eren, H., 2003.](https://ja.wikipedia.org/wiki/#CITEErin2003 "wikilink")
2.  [Buie, J., 1966.](https://ja.wikipedia.org/wiki/#CITEBuie1966 "wikilink")
3.  [The Computer History Museum, 2007.](https://ja.wikipedia.org/wiki/#CITEComputerHistoryMuseum2007 "wikilink")
4.
5.  Bo Lojek,'' History of semiconductor engineering ''Springer, 2006 ISBN 3540342575,pages 212-215
6.  [Engineering Staff, 1973.](https://ja.wikipedia.org/wiki/#CITETI1973 "wikilink")
7.  L.W. Turner,(ed), Electronics Engineer's Reference Book, 4th ed. Newnes-Butterworth, London 1976 ISBN 0-4-080-0168-2
8.  [Pittler, Powers, and Schnabel 1982, 5](https://ja.wikipedia.org/wiki/#CITEPittler1982 "wikilink")
9.  [Texas Instruments, 1985](https://ja.wikipedia.org/wiki/#CITETI1985 "wikilink")
10. [Lancaster, 1975](https://ja.wikipedia.org/wiki/#CITELancaster1975 "wikilink"), preface.
11. [Klein, 2008.](https://ja.wikipedia.org/wiki/#CITEKlein2008 "wikilink")
12. Electronic Principles Physics, Models, and Circuits, first edition 1969, Gray and Searle, page 870
13.
14. しきい電圧の異なる双安定要素が2つ並列接続されている場合、電流はしきい値の低い方の要素を通して流れる。
15. <cite id=CITEsiliconfareast2005>[*Transistor–Transistor Logic (TTL).*](http://www.siliconfareast.com/ttl2.htm) siliconfareast.com. 2005. Retrieved 17 September 2008.</cite>
16. [Millman 1979 pg. 147.](https://ja.wikipedia.org/wiki/#CITEMillman1979 "wikilink")
17. [SN7401 datasheet](http://www.ti.com/lit/gpn/sn7401) – Texas Instruments
18.
19. [Transistor–Transistor Logic (TTL), 2005](https://ja.wikipedia.org/wiki/#CITEsiliconfareast2005 "wikilink"), p. 1.
20. [Tala, 2006.](https://ja.wikipedia.org/wiki/#CITETala2006 "wikilink")
21. [SN7400 datasheet](http://focus.ti.com/general/docs/lit/getliterature.tsp?genericPartNumber=sn74ls00&fileType=pdf&track=no) - Texas Instruments
22. [TTL standard logic level, n.d.](https://ja.wikipedia.org/wiki/#CITEstandardlogicleveln.d. "wikilink")
23. [TTL-to-CMOS Interfacing Techniques](http://ecelab.com/interfacing-ttl-cmos.htm)
24. [Paul Horowitz](https://ja.wikipedia.org/wiki/:en:Paul_Horowitz "wikilink") and Winfield Hill, ''The Art of Electronics 2nd Ed. '' Cambridge University Press, Cambridge, 1989 ISBN 0-521-37095-7 page 970 *...CMOS devices consume power proportional to ther switching frequency...At their maximum operating frequency they may use more power than equivalent bipolar TTL devices.*
25. [Ayers, n.d.](https://ja.wikipedia.org/wiki/#CITEAyersn.d. "wikilink")
26. [Wobschall, 1987](https://ja.wikipedia.org/wiki/#CITEWobschall1987 "wikilink"), pp. 209-211.