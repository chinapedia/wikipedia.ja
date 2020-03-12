> この記事は[SPICE \(\)](https://ja.wikipedia.org/wiki/SPICE_\(\))から翻訳されています。


**SPICE** (Simulation Program with Integrated Circuit Emphasis, スパイス) は[電子回路](../Page/電子回路.md "wikilink")シミュレータである。[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")で1970年代前半頃に開発が始まり、以後何回かバージョンアップされた。[集積回路](../Page/集積回路.md "wikilink")の設計に利用可能なように開発されたため、長さや幅などといったパラメータによりトランジスタであれば特性や駆動能力を、配線であればインピーダンスと過渡特性といったものまでシミュレーションする能力まで持つが、単純にディスクリートの素子を定義し、配線は全て等電位とするといったようにして簡単に電子工作のシミュレーションを行う、といった用途にも問題なく使える。

シミュレーション対象となる回路は一般的な[受動素子](../Page/受動素子.md "wikilink")（[抵抗](../Page/抵抗器.md "wikilink")、[コンデンサー](https://ja.wikipedia.org/wiki/コンデンサー "wikilink")など）と[能動素子](https://ja.wikipedia.org/wiki/能動素子 "wikilink")（[ダイオード](../Page/ダイオード.md "wikilink")、[トランジスタ](../Page/トランジスタ.md "wikilink")など）と伝送線路、各種電源を組み合わせたものである。解析手法としては過渡解析、直流解析、小信号交流解析、雑音解析などが可能である。

現在使われている、名称にSPICEの語を含むシミュレータは、このバークレー校のものを元に改良、機能付加したものである。それらを含めた総称としてSPICEと呼ばれることもある。

## 回路、動作記述

### 概略

シミュレータへの入力となる回路や動作、制御文などは[テキスト](../Page/テキスト.md "wikilink")で記述する。各項目の基本は行単位であるが複数行にまたがる記述も可能であり、その場合には次の行の先頭に`+`を付ける。 コマンドの記述はドット (`.`) から始まる。

最初の行は表題となり、次の行以降に回路や制御文を記述する。 回路網はSPICE書式の[ネットリスト](https://ja.wikipedia.org/wiki/ネットリスト "wikilink") にて表現する。 最後の行は`.END`で終了する。 `.END`と記述した次の行は新たな回路記述として認識され、複数回路のシミュレーションが可能。

回路記述は１行１素子で記述する。 各行の行頭は素子のインスタンス名（固有の名前）を示し最初の一文字が素子種別を表す。抵抗ならRxxx、[インダクタンス](../Page/インダクタンス.md "wikilink")ならLyyyといった名前となる。 続けて、素子の各端子が接続されるノード名を記述し、最後に素子の特性値などを記述する。インスタンス名、ノード名などの区切りには空白文字を使用する。

行頭に `*` のある行はコメントである。

簡単な例1：CR回路

    CR circuit
    * 0---R1---1---C1---2
    R1 0 1 10
    C1 1 2 20
    .END

ここでR1の行の最後は10Ω、C1の行の最後は20Fを示す。0,1 あるいは 1,2 はそれぞれの端子のノードを示す。 結果として 0---R1---1---C1---2 と抵抗とキャパシタが直列につながった回路となる。

これだけでは回路記述のみであり電気回路として動作しない。 回路として動作させるためには、例えば次のように電圧源（Vで始まる素子）を付加する。

簡単な例2：CR回路 + 直流電源

    CR circuit+power
    * 0---R1---1---C1---2---V1---0
    R1 0 1 10
    C1 1 2 20
    V1 2 0 5
    .END

この例では前述の回路の両端（+側がノード 2 で-側がノード 0 ）に 5V の電圧を加えたことになる。 電源には直流のほか[正弦波](../Page/正弦波.md "wikilink")やパルス波形、[定電流源](https://ja.wikipedia.org/wiki/定電流源 "wikilink")なども指定できる。 電源も形式的には素子との位置づけであり他の素子同様、回路記述内に含める。 ノード 0 （グランド）は、必ず含まれていなくてはならない。 各部の電圧とは、指定した場所の電位とノード 0 との電位差として定義されている。

これを実際に動作させるには解析内容を指定する。

簡単な例3：CR回路 + 直流電源 + 過渡解析

    CR circuit+power+transient
    .TRAN 1 10
    * 0---R1---1---C1---2---V1---0
    R1 0 1 10
    C1 1 2 20
    V1 2 0 5
    .END

.TRAN文は1秒きざみで10秒まで経過させることを意味する（過渡解析）。 なおピリオドに始まる語は各種制御文を意味する。

シミュレータとしては動作した結果の観測も可能でなければならない。 次の指定で表示ができる。

簡単な例4：CR回路 + 直流電源 + 過渡解析 + 表示

    CR circuit+power+transient+print
    .TRAN 1 10
    .PRINT TRAN V(1) I(V1)
    * 0---R1---1---C1---2---V1---0
    R1 0 1 10
    C1 1 2 20
    V1 2 0 5
    .END

.PRINT文でノード1の電圧と電源V1の電流を一覧として出力する。 ほかに.PLOT文もありグラフ化することができる。

期待するような、コンデンサに充電されていくようなシミュレーション結果はこのままだと出てこない。これはSPICEは過渡解析を行う前に自動的にDC解析により初期条件の電位を決定し、この際コンデンサはショート状態として扱われるため、コンデンサに充電された状態でシミュレーションが開始してしまうためである。充電されていない状態でシミュレーションを開始するためには、.IC文を使用して初期条件における電位を明示的に指定する。

簡単な例5：CR回路 + 直流電源 + 過渡解析 + 初期条件 + 表示

    CR circuit+power+transient+ic+print
    .TRAN 1 10
    .PRINT TRAN V(1) I(V1)
    * 0---R1---1---C1---2---V1---0
    R1 0 1 10
    C1 1 2 20
    V1 2 0 5
    .IC V(1) = 2
    .END

この例では、コンデンサC1の抵抗R1側のノードの初期電位を2Vに設定する。これはV1の電圧と等しいため、コンデンサが充電されていない状態からシミュレーションが行われる。

なお先頭行と.ENDの間の記述順序は任意である。

### 素子詳細

素子の記述は一般に頭が種別を示すインスタンス名、それに続くノード名の列挙、必要に応じてパラメータなどの値の列挙が続く形式となっている。ノード名は初期は数値が基本であるがSPICEの種類、バージョンにより英数字での単語も可能となっている。 以下に主要な素子を列挙する。（細かいオプションは略）

  - 抵抗(R)

<!-- end list -->

    　  Rxxx N1 N2 value

  -
    N1、N2はノード名、valueは抵抗値で単位は[オーム](https://ja.wikipedia.org/wiki/オーム "wikilink")
    なお、単位接頭辞としてm（ミリ）、u（マイクロ、μの代用）、n（ナノ）、p（ピコ）、k（キロ）などが使用できる。SPICEでは大文字と小文字は区別されないため、メガはMではなくmegと表記する。すなわち1メガは「1meg」1ミリは「1m」と表す。また、単位（Ω）は通常省略する。（以下すべてに共通）

<!-- end list -->

  - キャパシタ(C)

<!-- end list -->

    　  Cxxx N+ N- value

  -
    N+、N-は正負のノード、valueは容量値で単位は[ファラド](../Page/ファラド.md "wikilink")

<!-- end list -->

  - インダクタ(L)

<!-- end list -->

    　  Lxxx N+ N- value

  -
    N+、N-は正負のノード、valueはインダクタンスで単位は[ヘンリー](../Page/ヘンリー.md "wikilink")

<!-- end list -->

  - 相互インダクタ(K)

<!-- end list -->

    　  Kxxx Lyyy Lzzz value

  -
    Lyyy、Lzzzは結合したインダクタの名前でvalueは結合係数である。

<!-- end list -->

  - 独立電圧源(V)

<!-- end list -->

    　  Vxxx N+ N- <option>

  -
    N+、N-は正負のノード、optionに交流(AC)、直流(DC)の区分、形式、電圧値などを記述する。

<!-- end list -->

  - 独立電流源(I)

<!-- end list -->

    　  Ixxx N+ N- <option>

  -
    N+、N-は正負のノード、optionに交流(AC)、直流(DC)の区分、形式、電圧値などを記述する。

<!-- end list -->

  - 電圧制御電流源(G)

<!-- end list -->

    　  Gxxx N+ N- NC+ NC- value

  -
    N+、N-は正負のノード、NC+、NC-は正負の制御ノード、valueは相互コンダクタンス。

<!-- end list -->

  - 電圧制御電圧源(E)

<!-- end list -->

    　  Exxx N+ N- NC+ NC- value

  -
    N+、N-は正負のノード、NC+、NC-は正負の制御ノード、valueは電圧増幅率。

<!-- end list -->

  - 電流制御電流源(F)

<!-- end list -->

    　  Fxxx N+ N- vname value

  -
    N+、N-は正負のノード、vnameは制御電流が流れている電圧源N、valueは電流増幅率。

<!-- end list -->

  - 電流制御電圧源(H)

<!-- end list -->

    　  Hxxx N+ N- vname value

  -
    N+、N-は正負のノード、vnameは制御電流が流れている電圧源N、valueは相互抵抗。

<!-- end list -->

  - ダイオード(D)

<!-- end list -->

    　  Dxxx N+ N- model <option>

  -
    N+、N-は正負のノード、modelにモデルを指定する。

<!-- end list -->

  - バイポーラトランジスタ(Q)

<!-- end list -->

    　  Qxxx NC NB NE model <option>

  -
    NCはコレクタ、NBはベース、NEはエミッタの各ノード、modelにモデルを指定する。

<!-- end list -->

  - 接合形電界効果トランジスタ(J)

<!-- end list -->

    　  Jxxx ND NG NS <NB> model <option>

  -
    NDはドレイン、NGはゲート、NSはソース（NBはバルクでオプションの一部）の各ノード、modelにモデルを指定する。

<!-- end list -->

  - MOS形電界効果トランジスタ(M)

<!-- end list -->

    　  Mxxx ND NG NS <NB> model <option>

  -
    NDはドレイン、NGはゲート、NSはソース（NBはバルクでオプションの一部）の各ノード、modelにモデルを指定する。

<!-- end list -->

  - 無損失伝送線路(T)

<!-- end list -->

    　  Txxx N1 N2 N3 N4 Z0=value

  -
    N1、N2はポート1のノード、N3、N4はポート2のノード、Z0は特性インピーダンス。

<!-- end list -->

  - 有損失伝送線路(O)

<!-- end list -->

    　  Oxxx N1 N2 N3 N4 model

  -
    N1、N2はポート1のノード、N3、N4はポート2のノード、MODELはモデル。

<!-- end list -->

  - 一様分布RC線路(U)

<!-- end list -->

    　  Uxxx N1 N2 N3 model L=LEN <option>

  -
    N1、N2はRC伝送線路が結ぶノード、N3はキャパシタがつながるノード、MODELはモデル、LENはRC伝送線路の長さ。

<!-- end list -->

  - サブサーキット

<!-- end list -->

```
    .SUBCKT name N1 <N2 ...>
    　回路記述
　　.ENDS
```

  -
    素子ではないが同一の回路ブロックを複数使用する場合、それを階層化するために用いる。nameがサブサーキット名、N1、N2..は端子名。呼び出し時は素子Xとして呼び出す。

### 制御文詳細

  - 過渡解析初期設定(.IC)

<!-- end list -->

```
   .IC V(ノード1)=value1 <V(ノード2)=value1 ... >
```

  -
    ノード1にvalue1を与える。以降必要数繰り返す。

<!-- end list -->

  - 過渡解析指定(.TRAN)

<!-- end list -->

```
   .TRAN step stop <option>
```

  -
    stepはPRINTまたはPLOTの時間の区切り。stopは最終時間。

<!-- end list -->

  - 直流解析指定(.DC)

<!-- end list -->

```
   .DC src start stop step <option>
```

  -
    srcは独立電圧源または電流源、startは開始値、stopは終了値、stepは増分値。

<!-- end list -->

  - 温度指定(.TEMP)

<!-- end list -->

```
   .TEMP temp
```

  -
    tempで温度を指定する。

<!-- end list -->

  - オプション(.OPTIONS)

<!-- end list -->

```
   .OPTIONS opt1 <opt2 ...>
```

  -
    各種オプション指定。

以上のとおり見てきたように、SPICEはテキストによる記述を基本としているが、商用版ソフトウェアなどでは回路図CADと統合化してグラフィカルな記述も可能となり、より使いやすくなっている。

## 歴史

初期のバージョンは[FORTRAN](../Page/FORTRAN.md "wikilink")で書かれており[フリーウェア](../Page/フリーウェア.md "wikilink")として公開されている。後には[C言語](../Page/C言語.md "wikilink")に移植された（バージョン3）。

  - [1973年](../Page/1973年.md "wikilink") SPICE
  - [1975年](../Page/1975年.md "wikilink") SPICE2
  - [1981年](../Page/1981年.md "wikilink") SPICE2G.6　主要商用版の元
  - [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink") SPICE3 この版よりC言語化

1980年代　商用版各種登場(HSPICE、PSPICEなど)

## 派生したSPICEソフトウェア

  - spice3f (バークレイによる最終版)
  - ngspice (オープンソース版SPICEのひとつ)
  - Qucs (オープンソース版SPICEのひとつ[入手ページ](http://qucs.sourceforge.net/))
  - HSPICE (meta software社開発、現[シノプシス](../Page/シノプシス.md "wikilink"))
  - PSpice (MicroSim社開発、現[ケイデンス・デザイン・システムズ](../Page/ケイデンス・デザイン・システムズ.md "wikilink"))
  - SmartSpice ([シルバコ](../Page/シルバコ.md "wikilink")社 [入手ページ](https://www.silvaco.co.jp/products/analog_mixed_signal/smartspice.html))
  - LTSpice (リニアテクノロジ社配布 [入手ページ](http://www.linear-tech.co.jp/designtools/software/))
  - TINA-TI (テキサス・インスツルメンツ社配布 [入手ページ](http://www.tij.co.jp/tool/jp/tina-ti#descriptionArea))

## 外部リンク

  - [カリフォルニア大学バークレー校によるSPICE解説](http://bwrc.eecs.berkeley.edu/Classes/IcBook/SPICE/)
  - [A BRIEF HISTORY OF SPICE](http://www.ecircuitcenter.com/SpiceTopics/History.htm)
  - [Spice 3f5マニュアル 日本語訳 (HTML版)](http://ayumi.cava.jp/audio/spiceman/spiceman.html) | [(PDF版)](http://ayumi.cava.jp/audio/spiceman.pdf)

[Category:EDAソフト](https://ja.wikipedia.org/wiki/Category:EDAソフト "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink") [Category:1973年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1973年のソフトウェア "wikilink")