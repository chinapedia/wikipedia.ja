> この記事は[Simula](https://ja.wikipedia.org/wiki/Simula)から翻訳されています。


**SIMULA**（シミュラ ; **SIMU**lation **LA**nguage）は、[オルヨハン・ダール](https://ja.wikipedia.org/wiki/オルヨハン・ダール "wikilink")と[クリステン・ニガード](https://ja.wikipedia.org/wiki/クリステン・ニガード "wikilink")によって[ALGOL60](https://ja.wikipedia.org/wiki/ALGOL60 "wikilink")を拡張する形で1960年代に開発が始められた[シミュレーション](../Page/シミュレーション.md "wikilink")用途の[プログラミング言語](../Page/プログラミング言語.md "wikilink")である\[1\]。

ALGOLの`begin ... end`で囲まれた部分である**ブロック**（block）の概念を実体的な実例（instance）として扱うことを目的として、**クラス**（class）の構文と対象（object、**オブジェクト**）の概念を初めて導入した言語である\[2\]。最初期の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語であるとも言われるが、この言語の設計者はオブジェクト指向を全く意識していなかった。

オブジェクト指向は SIMULA のクラスとオブジェクトの概念を一般化したものであり、SIMULA よりも後に作られた概念である。

## 概要

[オスロ](../Page/オスロ.md "wikilink")のノルウェー計算センターの[クリステン・ニガード](https://ja.wikipedia.org/wiki/クリステン・ニガード "wikilink")と[オルヨハン・ダール](https://ja.wikipedia.org/wiki/オルヨハン・ダール "wikilink")が[1962年](../Page/1962年.md "wikilink")から[1967年](../Page/1967年.md "wikilink")にかけて、 の元となる  と **67** を [{{lang](https://ja.wikipedia.org/wiki/ALGOL60 "wikilink") の拡張として設計/実装した。 は当初シミュレーションに用いられたが、のちに汎用言語となった。名前「」は「シミュレーション言語」を意味する英語「」と「簡潔な汎用言語」を意味する英語「」の二つに由来する。

主に北欧圏で使用されたこと、言語的な未成熟さもあって広く普及することはなかったが、後続言語に与えた影響は大きい。特に は  のオブジェクト概念を一般化したものだと言うことができる。 もまた、当初は[C言語](../Page/C言語.md "wikilink")に  のクラスなどの仕組みを追加したものであった。

開発の動機は、ある制限下におかれたモデル群の全体の挙動をどう記述するか、というものである。気体の分子運動を例にとると、[システム](../Page/システム.md "wikilink")全体を考えてその中の項として分子を扱うよりも、一つの一つの気体分子をモデル化し、それぞれの相互作用の結果をシステムとして捉える方が自然で取り扱いやすい。その為には小さなモデル、関連する法則、それらを一度に複数取り扱う能力が必要となる。こうして[属性](../Page/属性.md "wikilink")を備えた[オブジェクト概念と](../Page/オブジェクト_\(プログラミング\).md "wikilink")、それに従属する[メソッド概念が生まれたのである](../Page/メソッド_\(計算機科学\).md "wikilink")。

67 では[オブジェクト](../Page/オブジェクト_\(プログラミング\).md "wikilink")、 [クラス](../Page/クラス_\(コンピュータ\).md "wikilink")、[サブクラス](../Page/サブクラス_\(計算機科学\).md "wikilink")、[継承](../Page/継承_\(プログラミング\).md "wikilink")、[動的束縛（仮想関数）](../Page/メソッド_\(計算機科学\).md "wikilink")、[コルーチン](../Page/コルーチン.md "wikilink")、 ディスクリートイベントシミュレーション、[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")の機能をもち、オブジェクト指向プログラミングの基本概念はすべてここで発案されているといえる。

は[プログラミングパラダイム](../Page/プログラミングパラダイム.md "wikilink")として最初の[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語であると考えられる。その名前が示すように  はシミュレーションを行うために設計され、その必要性から今日のオブジェクト指向言語で使われる多くの機能のためのフレームワークを提供した。なお、 当時「オブジェクト指向」という言葉はまだない。この用語は[アラン・ケイ](../Page/アラン・ケイ.md "wikilink")が  の概念として70年代ごろに使い出したのが始まりといわれている。従ってその意味では  が世界最初のオブジェクト指向言語であり、 は「オブジェクト指向として再認識が可能な最古の言語」ということができる。

[VLSI](https://ja.wikipedia.org/wiki/VLSI "wikilink")設計、[プロセス](../Page/プロセス.md "wikilink")、[プロトコル](../Page/プロトコル.md "wikilink")、[アルゴリズム](../Page/アルゴリズム.md "wikilink")といったシミュレーションや、[組版](../Page/組版.md "wikilink")、[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")、[教育](../Page/教育.md "wikilink")といったアプリケーションソフトに  は利用された。 形式のオブジェクトは 、、 で再実装されており、 の影響を受けていることが知られている。 の開発者である[ビャーネ・ストロヴストルップ](../Page/ビャーネ・ストロヴストルップ.md "wikilink")は[BCPL](../Page/BCPL.md "wikilink")のような機械語を出力し高速に動作する低レベル言語に  が提供する開発効率を高める機能を導入するため、 開発時に  67 の影響を大きく受けていることを認めている。

## 歴史

クリステン・ニガードは1957年からコンピュータシミュレーションの開発を始めた。ニガードはコンピュータの動作とシミュレーションプログラムに要求されるものの不整合を適切に記述する方法が必要であると考えた。既存の[コンピュータ言語](https://ja.wikipedia.org/wiki/コンピュータ言語 "wikilink")で彼のアイデアを実現するにはプログラミングのスキル以外に何かが必要であると思われた。オルヨハン・ダールは1962年1月にニガードの業務に参加した。1962年3月までにはシミュレーション用プログラミング言語のメインコンセプトは固まっていた。ディクリートイベントシステムを持つシミュレーション専用のプログラミング言語 **** が開発された。

は  1107 を発売するにあたりニガードを1962年3月下旬に招待した。その際にニガードは  の[ボブ・バーマー](../Page/ボブ・バーマー.md "wikilink")システムプログラミング部長に  のアイデアを説明した。バーマーは  の熱烈なファンであり、 プロジェクトに説得力を感じた。IFIP（[情報処理国際連合](https://ja.wikipedia.org/wiki/情報処理国際連合 "wikilink")）が主催する情報処理の第2回国際会議の議長を務めていたバーマーは論文「SIMULA — An Extension of ALGOL to the Description of Discrete-Event Networks」を提出したニガードを会議に招待した。

ノルウェー計算機センターは  との契約に基づいてダールがSIMULA Iを実装するため  1107 を1963年8月に特別価格で譲り受けた。これは  用 [{{langコンパイラを元に実装された](../Page/ALGOL.md "wikilink")。1965年1月には  1107 上で完全な  を利用できた。ダールとニガードはその後の2年間に渡り  を教えることに費やした。 は複数の国に広がり、 は後に [バロース B5000](../Page/バロース_B5000.md "wikilink") やロシアの -16 に移植された。

[アントニー・ホーア](../Page/アントニー・ホーア.md "wikilink")は1966年にレコードクラスのコンストラクタの概念を導入し、ダールとニガードは一般的なプロセス概念という要求を満たすためプリフィックスの概念などを導入してこれを拡張した。ダールとニガードは[クラスと](../Page/クラス_\(コンピュータ\).md "wikilink")[サブクラスの宣言についての論文を](../Page/サブクラス_\(計算機科学\).md "wikilink")1967年3月に[オスロ](../Page/オスロ.md "wikilink")で開催された IFIP のシミュレーション用言語についてのワーキングカンファレンスで発表した。この論文は  67 の最初の正式な定義となった。1967年6月に言語を規格化して複数の実装を始めるためのカンファレンスが開催された。ダールは[データ型](../Page/データ型.md "wikilink")と[クラスの概念の統一化を提案した](../Page/クラス_\(コンピュータ\).md "wikilink")。これは激論を巻き起こし委員会から却下された。 は  標準化グループ (SSG) の最初の会議で1968年2月に正式に標準化された。

は  やその後のオブジェクト指向言語に影響を及ぼした。 だけが[コルーチン](../Page/コルーチン.md "wikilink")をサポートした言語ではないし、真の並列性は持たないが、[アクターモデル](../Page/アクターモデル.md "wikilink")の概念を呼び起こすのに役立った。

60年代後期から70年代前期にかけて  の4つの主要な実装があった。

  - 1100 用。Norwegian Computing Center (NCC) が開発。

  - [{{lang](https://ja.wikipedia.org/wiki/System/360 "wikilink") 用および [{{lang](https://ja.wikipedia.org/wiki/System/370 "wikilink") 用。スウェーデン国立防衛研究所 (FOA) が開発。

  - CDC 3000 用。オスロ市シェラーにある[オスロ大学](../Page/オスロ大学.md "wikilink")の  で開発。

  - 用。 が開発。

これらの実装は様々なプラットフォームに移植された。 用ではメンバ変数とメソッドの `public`、`protected`、`private` が実装され、後に  87 に統合された。 87 は最新の標準規格であり、下記の3つの実装があることが知られている。

  -
  -
  - [](http://www.gnu.org/software/cim/cim.html)

2001年11月に[米国電気電子学会 (IEEE)は](../Page/IEEE.md "wikilink")、「 の設計と実装によりオブジェクト指向の基礎概念を導きだした」ことを讃え[フォン・ノイマンメダル](../Page/フォン・ノイマンメダル.md "wikilink")をダールとニガードに授与した。2002年2月には「プログラミング言語  及び  の実装によりオブジェクト指向を出現させた基礎的アイデア」を表彰して2001年度[チューリング賞](../Page/チューリング賞.md "wikilink")を[ACMより受賞した](../Page/Association_for_Computing_Machinery.md "wikilink")。[両名は6月と8月にそれぞれ死去したため](http://www.acm.org/announcements/turing_obit.html)、シアトルで開催される  カンファレンス2002で行われる予定であった[ACMチューリング賞](http://www.informatik.uni-trier.de/~ley/db/journals/cacm/turing.html)の講演に出席できなかった。

研究所はプログラミング言語  にちなんで名付けられた研究所であり、ニガードはオープン時の2001年から非常勤職員として働いていた。

## サンプルコード

### 最小のプログラム

空のファイルはソースコードのサイズを基準とした場合で最も小さな  のプログラムである。これは1つのダミーのステートメントのみで構成される。

しかしながら合理的に考えれば最小のプログラムは空のブロックとして表現される。

**`Begin`**
**`End`**` ;`

これは起動してすぐに終了するプログラムである。 ではプログラム自身が値を返す [`return`文](../Page/Return文.md "wikilink") を持たない。

### 古典的

Simulaで記述された  の例である。 は大文字と小文字を厳密に区別する。

<code>**`Begin`**
**`OutText`**` ("Hello World!") ;`
**`Outimage`**` ;`
**`End`**` ;`</code>

### 典型的サブクラスと仮想関数

クラス、サブクラス、仮想関数を用いた現実的な例を以下に示す。

<code>**`Begin`**
**`Class`**` Glyph ;`
`   `**`Virtual`**`: `**`Procedure`**` print `**`Is`**` `**`Procedure`**` print ;`
`   `**`Begin`**
`   `**`End`**` ;`

`   Glyph `**`Class`**` Char (c) ;`
`      `**`Character`**` c ;`
`      `**`Begin`**
`      `**`Procedure`**` print ;`
`      OutChar(c) ;`
`      `**`End`**` ;`

`   Glyph `**`Class`**` Line (elements) ;`
`      `**`Ref`**` (Glyph) `**`Array`**` elements ;`
`      `**`Begin`**
`      `**`Procedure`**` print ;`
`         `**`Begin`**
`         `**`Integer`**` i ;`
`         `**`For`**` i:= 1 `**`Step`**` 1 `**`Until`**` UpperBound (elements, 1) `**`Do`**
`            elements (i) .print ;`
`         OutImage ;`
`         `**`End`**` ;`
`      `**`End`**` ;`

`   `**`Ref`**` (Glyph) rg ;`
`   `**`Ref`**` (Glyph) `**`Array`**` rgs (1 : 4) ;`

`   `*`!``   ``Main``   ``program;`*
`   rgs (1):- `**`New`**` Char ('A') ;`
`   rgs (2):- `**`New`**` Char ('b') ;`
`   rgs (3):- `**`New`**` Char ('b') ;`
`   rgs (4):- `**`New`**` Char ('a') ;`
`   rg:- `**`New`**` Line (rgs) ;`
`   rg.print ;`
**`End`**` ;`</code>

上記の例には1つの親クラス（`Glyph`）と2つのサブクラス（`Char`、`Line`）があり、1つの[仮想関数](https://ja.wikipedia.org/wiki/仮想関数 "wikilink")と2つの[実装](../Page/実装.md "wikilink")がある。メインプログラムから実行を開始する。 は純粋仮想関数を持つクラスを[インスタンス化できるため抽象基底クラスの概念が無い](../Page/オブジェクト_\(プログラミング\).md "wikilink")。これは上記の例にある全てのクラスがインスタンス化できるということである。しかしながら純粋仮想関数を呼び出すと[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")[エラー](../Page/エラー.md "wikilink")を引き起こす。

### 名前呼び

は名前呼び（、[評価戦略](https://ja.wikipedia.org/wiki/評価戦略 "wikilink")を参照）をサポートしているため （[:en:Jensen's Device](https://ja.wikipedia.org/wiki/:en:Jensen's_Device "wikilink")）を容易に実装できる。デフォルトはと異なり値呼び（）であるため、を実装する際には、名前呼びであることを明示する必要がある。

単純な例として総和関数\(\sum\)の実装例を以下に示す。

<code>**`Real`**` `**`Procedure`**` Sigma (l, m, n, u) ;`
`   `**`Name`**` l, u ;`
`   `**`Integer`**` l, m, n ;`
`   `**`Real`**` u ;`
`   `**`Begin`**
`   `**`Real`**` s ;`
`   l:= m ;`
`   `**`While`**` l <= n `**`Do`**
`      `**`Begin`**
`      s := s + u ;`
`      l := l + 1 ;`
`      `**`End`**` ;`
`   Sigma := s ;`
`   `**`End`**` ;`</code>

上記のコードは値（`l`）と式（`u`）を制御するために名前呼びを用いている。これにより式で使用する値を制御できる。 の標準規格は `for` 文にある種の制約があるため上記の例では `while` 文を使用している。

以下の式は次のように実装できる。

\(Z = \sum_{i=1}^{100}{1 \over (i + a)^2}\)

`Z:= Sigma (i, 1, 100, 1 / (i + a) ** 2) ;`

### シミュレーション

にはディスクリートイベントシミュレーションを行うための[シミュレーション](../Page/シミュレーション.md "wikilink")パッケージが含まれている。このシミュレーションパッケージはSimulaの[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")と[コルーチン](../Page/コルーチン.md "wikilink")のコンセプトに基づいている。

下記の例で `Sam`、`Sally`、`Andy` は服を買おうとしている。彼らは1つの試着室を共有しなければならない。3人は正規分布によりランダムに約12分間店内を探索し、同様に試着室を約3分間占有する。以下は彼らが試着室をどのように使うのかをシミュレーションするものである。

<code>`Simulation`
`   `**`Begin`**
`   `**`Class`**` FittingRoom ;`
`      `**`Begin`**
`      `**`Ref`**` (Head) door ;`
`      `**`Boolean`**` inUse ;`
`      `**`Procedure`**` request ;`
`         `**`Begin`**
`         `**`If`**` inUse `**`Then`**
`             `**`Begin`**
`             Wait (door) ;`
`             door.First.Out ;`
`             `**`End`**` ;`
`         inUse := `**`True`**` ;`
`         `**`End`**` ;`
`      `**`Procedure`**` leave ;`
`         `**`Begin`**
`         inUse := `**`False`**` ;`
`         `**`Activate`**` door.First ;`
`         `**`End`**` ;`
`      door:- `**`New`**` Head ;`
`      `**`End`**` ;`
`  `
`   `**`Procedure`**` report (message) ;`
`      `**`Text`**` message ;`
`      `**`Begin`**
`      OutFix (Time, 2, 0) ;`
`      OutText (": " & message) ;`
`      OutImage ;`
`      `**`End`**`;`

`   Process `**`Class`**` Person (pname) ;`
`      `**`Text`**` pname ;`
`      `**`Begin`**
`      `**`While`**` `**`True`**` `**`Do`**
`         `**`Begin`**
`         Hold (Normal (12, 4, u)) ;`
`         report  (pname & " is requesting the fitting room") ;`
`         fittingroom1.request ;`
`         report (pname & " has entered the fitting room") ;`
`         Hold (Normal (3, 1, u)) ;`
`         fittingroom1.leave ;`
`         report (pname & " has left the fitting room") ;`
`         `**`End`**` ;`
`      `**`End`**` ;`

`   `**`Integer`**` u ;`
`   `**`Ref`**` (FittingRoom) fittingRoom1 ;`

`   fittingRoom1 :- `**`New`**` FittingRoom ;`
`   `**`Activate`**` `**`New`**` Person ("Sam") ;`
`   `**`Activate`**` `**`New`**` Person ("Sally") ;`
`   `**`Activate`**` `**`New`**` Person ("Andy") ;`
`   Hold (100) ;`
`   `**`End`**`;`</code>

メインブロックが `Simulation` でプレフィックスされることによりシミュレーションを実行できる。シミュレーションパッケージはどこのブロックからでも自由に利用でき、シミュレーションしているものそれ自体をシミュレーションするときにはシミュレーションを再帰的にネストできる。

試着室オブジェクトはキュー（`door`）により試着室にアクセスできる。誰かが使用中の試着室を使おうとしたときはこのキュー（`Wait (door)`）で待たなければならない。誰かが試着室を出るとき、列の先頭にいる者がキューからリリース（**`Activate`**`  door.first `）されてドアキューから削除（`door.First.Out`）される。

`Person` は `Process` のサブクラスでありその動作は `hold`（店内を探索する時間と試着室で過ごす時間）を用いて記述され、試着室に出入りするために試着室オブジェクト内でメソッドを呼び出す。

メインプログラムは全てのオブジェクトを生成し、全ての `Person` オブジェクトをイベントキューに投入するためにアクティベートする。メインプログラムはシミュレーション時間で100分間待ってからプログラムを終了する。

## 脚注

<references />

## 参考文献

  -
  -
  - [IBM System 360/370 Compiler and Historical Documentation](http://www.edelweb.fr/Simula/)

  -

  -
## 関連項目

  - [構造化プログラミング](../Page/構造化プログラミング.md "wikilink")
  - [抽象データ型](../Page/抽象データ型.md "wikilink")
  - [ALGOL](../Page/ALGOL.md "wikilink")
  - [オブジェクト指向](../Page/オブジェクト指向.md "wikilink")

## 外部リンク

  - [](http://staff.um.edu.mt/jskl1/talk.html)
  - [](http://www.ifi.uio.no/~cim/cim_toc.html)
  - [](http://linux.maruhn.com/sec/cim.html) —  の配布ページ
  - [](http://www.volny.cz/petr-novak/cim/) — 上記の  版

[Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink")

1.  [Ole(1966)](https://ja.wikipedia.org/wiki/#Ole\(1966\) "wikilink")
2.  [ダイクストラ(1975)](https://ja.wikipedia.org/wiki/#ダイクストラ\(1975\) "wikilink") p.202