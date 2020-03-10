> この記事は[LOGO](https://ja.wikipedia.org/wiki/LOGO)から翻訳されています。


**LOGO**（ロゴ）は、教育向けとして設計された[マルチパラダイムの](../Page/プログラミングパラダイム.md "wikilink")[コンピュータ](../Page/コンピュータ.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。しばしば簡易言語だと誤解されていることもあるが、[再帰](../Page/再帰.md "wikilink")なども扱える言語としての機能、リストなどのデータ構造や、I/O・ファイルなどの一般的な機能を持ったライブラリなど、簡易言語ではなく、十分な能力を持ったプログラミング言語である。特徴的な機能としては「タートルグラフィック」がある。

[1967年](../Page/1967年.md "wikilink")、[教育](../Page/教育.md "wikilink")（特に[構成主義](../Page/構成主義_\(教育\).md "wikilink")[教育](../Page/教育.md "wikilink")）のために、、[Wally Feurzeig](https://ja.wikipedia.org/wiki/:en:Wally_Feurzeig "wikilink")、[シーモア・パパート](https://ja.wikipedia.org/wiki/シーモア・パパート "wikilink")、シンシア・ソロモンによって開発された。名称はギリシャ語の *logos* （言葉）に由来する。（現代ではいささか想像しにくくなったことであるが）当時代表的な既存言語であった[FORTRAN](../Page/FORTRAN.md "wikilink")や、その影響を受けた言語がもっぱら数値計算を指向したものであったのに対し、「言葉」で操作する言語であるといったようなことを強調したものである。多くの計算機科学の概念を教えるのに使うことができ、例えば[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")の講師は3巻の著書 *Computer Science Logo Style* にまとめている\[1\]。

[コンピュータ](../Page/コンピュータ.md "wikilink")の使用を通じた[児童](../Page/児童.md "wikilink")の思考能力の訓練を目的としており、主に8歳から12歳の児童にも扱い易いよう配慮された豊富なグラフィック関連のコマンドが特徴である。主な使用者は学生、教師が想定された。

## 歴史

1967年、[マサチューセッツ州](../Page/マサチューセッツ州.md "wikilink")[ケンブリッジにある研究機関](../Page/ケンブリッジ_\(マサチューセッツ州\).md "wikilink") [Bolt, Beranek and Newman](../Page/BBNテクノロジーズ.md "wikilink") (BBN) にて、Wally Feurzeig と[シーモア・パパート](https://ja.wikipedia.org/wiki/シーモア・パパート "wikilink")が開発した\[2\]。[人工知能](../Page/人工知能.md "wikilink")、[数理論理学](../Page/数理論理学.md "wikilink")、[発達心理学](../Page/発達心理学.md "wikilink")の成果を基盤としている。最初の4年間は、BBNにてLOGO開発とLOGOによる教育の研究が行われた。LOGOの最初の実装は、「Ghost」という名前で、[PDP-1](../Page/PDP-1.md "wikilink")の[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")で書かれた。その目標は子どもが単語や文で遊べる数学の遊び場を作ることだった\[3\]。LOGOの設計では、しきいが低く使いやすいことと、エラーの原因がわかりやすいことが重視されている。[タートル](../Page/ウォルターの亀.md "wikilink")（亀）を採用したのは、視覚的フィードバックが即座に得られ、デバッグを即座に行えるからだった。

LOGOで操縦可能な[亀のロボットが](../Page/ウォルターの亀.md "wikilink")[MITで作られたのは](../Page/マサチューセッツ工科大学.md "wikilink")1969年のことであり、それ以前から画面上で動作する仮想的なタートルが存在していた。現代のLOGOも、その最初のタートルの基本コンセプトからそれほど変わっていない。最初の亀ロボットは有線式であり、[ラジコン](https://ja.wikipedia.org/wiki/ラジコン "wikilink")あるいは[無線操縦ではなかった](../Page/無線通信.md "wikilink")。後にBBNはIrvingという亀ロボットを開発しており、それは触角センサを持ち、前進、後退、回転といった動きができ、ベルを鳴らす機能も備えていた。1968年から69年にかけて、マサチューセッツ州[レキシントンの中学校で](https://ja.wikipedia.org/wiki/レキシントン_\(マサチューセッツ州\) "wikilink")1年間かけたLOGO教育が実施されている。仮想的なタートルや亀ロボットを最初に教育に取り入れたのは同じレキシントンの小学校（5年生）で、1970年から71年にかけてのことである。

## タートルグラフィックス

[Turtle_draw.jpg](https://ja.wikipedia.org/wiki/File:Turtle_draw.jpg "fig:Turtle_draw.jpg") LOGO最大の特徴はタートルであり\[4\]、画面上の[カーソル](../Page/カーソル.md "wikilink")で表され（タートルと呼ばれるようになったのは、先述の亀のロボットから）、それに動きと線描を命令することができ、プログラムに基づいて線で描かれたグラフィックスを生成できる。三角形または亀の形で表されることが多い（実際にはどんなアイコンでもよい）。シーモア・パパートがLOGOにタートルグラフィックスを追加したのは1960年代末ごろで、パパート自身が開発した亀ロボットに上げ下げ可能なペンを装着させて描画できるようにしたことからである。

やはり現代からは想像が難しいことであるが、1960年代にはCRTによるラスタースキャンディスプレイ自体は存在していたものの、コンピュータグラフィックスの出力先としてはあまり一般的で実用的なものではなかった（たとえば、フレームバッファに必要なメモリの容量と帯域幅は当時のコンピュータの性能では非現実的であった）。当時、グラフィックの一般的な出力方式としては、[プロッター](https://ja.wikipedia.org/wiki/プロッター "wikilink")や[ベクタースキャン](../Page/ベクタースキャン.md "wikilink")ディスプレイであり、いずれも「デカルト座標」的に (x, y) の絶対値ないし相対値で指定するものであった。

そのような描画方式のほうが便利なこともあるが、正多角形や渦巻きなど、自然に再帰的あるいは繰返しになっているものを、そのまま自然に再帰あるいは繰返しによって描く、という操作にはあまり向いていない。

それに対しタートルでは、命令は常にその時点での状態から、相対的に作用する。すなわち、タートルは命令を受けるとその時点の位置と向きを起点として動作し、例えば *LEFT 90* と命令すれば左に90度回転する。子供は、自己と一体化しやすいタートルを操作してその軌跡を図形として描いたり色を塗ったりして楽しむ事が簡単に出来る。パパートはこれを body-syntonic reasoning（身体同調性推論）と呼んだ。特に複数のタートルを同時に操作可能なLOGO実装では、タートル（カーソル）の見た目の再定義や、タートル同士の[当たり判定](https://ja.wikipedia.org/wiki/当たり判定 "wikilink")ができるようになっていて、ビデオゲーム用語でいういわゆる「[スプライト](../Page/スプライト_\(映像技術\).md "wikilink")」のように使うことができるものもある。

「最終参照座標」といったようなものがある、タートル的な描画システムはごくありふれたものだが（例えばSVGのpath要素による描画など）、一例としては、[L-system](../Page/L-system.md "wikilink")の図形を描画するFractintというプログラムは、内部でタートルへのコマンドという形で描画を表現している。

## 言語

大文字と小文字は区別しないが、出力では大文字/小文字を保持する。標準規格は存在しないが、**UCBLogo**が高く評価されている。教育用言語ではあるが、リスト処理能力の高さから実用的なスクリプトが非常に書きやすくなっている\[5\]。

### データ

UCBLogoには次の3種類の[データ型](../Page/データ型.md "wikilink")がある。

  - ワード（[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")のatomに相当）
  - [リスト](../Page/リスト_\(抽象データ型\).md "wikilink")（LISPのconsに相当）
  - [配列](../Page/配列.md "wikilink")

数はワードの特殊ケースと解釈される。

[静的型付け](https://ja.wikipedia.org/wiki/静的型付け "wikilink")ではなく、データ型は実行によってチェックされる。

次の2つの記号は重要な意味を持つ。

  - コロン (`:`) は「-の中身（値）」を意味する。これは変数が実際にはメモリの特定の位置を示していると児童に意識させるのに役立つ。
  - ダブルクオート (`"`) は「そのワードをそれ自身として評価する」あるいは「それを評価した後の値はそれ以前と同じである」を意味する。他のプログラミング言語ではダブルクオートは引用符として2つを組みにして使うが、LOGOではそのような対応付けがない。

数はその点で特別であり、本当はダブルクオート付きで書く必要があるが、**2** も **"2** も同じに扱われる。

変数への代入（例えば、`x := y + 3`）は、LOGOでは`make`コマンドで行う。例えば、以下の2つの文は等価である。

`make "x sum :y 3`
`make "x sum :y "3`

`make`は2つのパラメータをとり、この例での2つ目のパラメータは `sum :y "3` である。`sum` は2つのパラメータをとる演算 (operation) であり、2つのパラメータの和を計算する。`"3` を評価すると `3` となり、`:y` は `y` と呼ばれるものの中身をとる。その結果、両者を加算した和が数として得られる。

`make` は第二パラメータを評価した結果を第一パラメータに格納する。プログラミングの観点から言えば、`make`の第一パラメータは参照渡しで、第二パラメータは値渡しである。

#### スコープ

通常は変数を使用前に宣言せず、変数[スコープ](https://ja.wikipedia.org/wiki/スコープ "wikilink")は大域的である。

`local` と宣言した変数のスコープは、宣言した[プロシージャ](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")およびそのプロシージャを呼び出す任意のプロシージャに限定される（[動的スコープ](../Page/動的スコープ.md "wikilink")の一種）。入力（引数）のあるプロシージャでは、実引数（アーギュメント）の値を保持するローカル変数が生成される（仮引数（パラメータ））。

#### リスト

[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")と同様のリストがあり、主要なデータ構造として頻用される。配列も用意している。

  - ワード列をリストに変換する演算、リスト群を配列に変換する演算、および逆の演算が存在する。
  - リストは配列とは異なり無限に拡張可能という利点がある。first, butfirst, last, butlast, butmember, member, item といった演算でリストからデータを取り出すことができる。データ要素をリストに追加する場合は、fput または lput という文を使う。
  - リストは[キューとして扱うこともでき](../Page/キュー_\(コンピュータ\).md "wikilink")、そのための queue と dequeue という演算がある。また、[スタック](../Page/スタック.md "wikilink")として扱うための push と pop という演算もある。
  - リストを処理する際はループではなく再帰を使うのが自然である。

#### 制御構造コマンド

LOGOには、[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")、[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")、[do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")、回数指定の[ループといった](../Page/ループ_\(プログラミング\).md "wikilink")、いくつかの一般的[制御構造](../Page/制御構造.md "wikilink")を備えている。一般にLOGOではループよりも再帰を好んで使用する。

また、リストベースの制御構造もある。基本的な考え方は次のように2つのリストを使う。

`OPERATION [ コマンドのリスト ] [ データのリスト ]`

そうすると、コマンド群がリストの個々のアイテムに適用される。MAP, APPLY, FILTER, FOREACH, REDUCE, CASCADE といったテンプレートコマンドがある。テンプレート反復は、explicit-slot、named-procedure、named-slot（またはLambda）、procedure-text の4種類に分類される。

#### 属性リスト

属性リストは特殊なリストで、奇数番目のアイテムは属性名、偶数番目のアイテムは属性値となっている。属性リストを操作するコマンドとして以下の3つがある。

  - `pprop :listname :name :value` - 新たなペアをリストに追加する。
  - `remprop :listname :name :value` - リストから指定したペアを削除する。
  - `show gprop :listname :name` - 指定した属性名に対応する属性値を取得する。

### I/O

コマンドウィンドウ（出力ストリーム）にテキストを書き込むには `print` コマンドを使い、グラフィックスウィンドウにテキストを出力するには `label` コマンドを使用する。

キーボードからの通常の入力ストリームから入力を受け付けるコマンドとして、`readlist`、`readword`、`readchar` がある。入力ストリームはディスク上のファイルなどから入力するよう切り換えることができる。同様に出力もリダイレクト可能である。

### 構文

コマンドは1行または複数行で書かれる。多くのコマンドには短縮形があり、例えば `FORWARD` は `FD`、`RIGHT` は `RT` と短縮できる。これは児童のタイピングの手間を省くという意味がある。セミコロンから行末まではコメントとして無視される。

`; 辺の長さが100の正方形を描画`
`FORWARD 100`
`LEFT 90`
`FORWARD 100`
`LEFT 90`
`FORWARD 100`
`LEFT 90`
`FORWARD 100`
`LEFT 90`

`FD 100 RT 120 FD 100 RT 120 ; 三角形の描画`
`FD 100 RT 120`

LOGOでの [Hello world](../Page/Hello_world.md "wikilink") プログラムは次のようになる。

`print [Hello World]`

### ループ

ループ用コマンドは3種類ある。その1つが `REPEAT` で、次の例は正方形を描画する。

`REPEAT 4 [FD 100 LEFT 90]`

この場合、`FD 100 LEFT 90` というコマンドを4回実行する。近似的に円を描くには、`REPEAT 360 [FD 1 RIGHT 1]` のように1度ずつ回転して1単位だけ描画するコマンドを360回反復すればよい。ループは入れ子可能であり、次のようなちょっとしたコードで面白い図形を描画できる。

`REPEAT 36 [RT 10 REPEAT 360 [FD 1 RT 1]]`
`FD 25`
`RT 90`

次もループの入れ子の例である。

`REPEAT 36 [REPEAT 4 [FD 100 RT 90] RT 10]`

### ペン

[right](https://ja.wikipedia.org/wiki/ファイル:Ubclogo_drawing_dash.png "wikilink") タートルは、その尻尾にペンをつけた形のアナロジーで使われることが多い。タートルのペンは上げ下げでき、次のように破線を描くことができる。

`FD 20 ; 直線を描きつつタートルが移動する`
`PENUP ; ペンを持ち上げる。そのため描画されなくなる`
`FD 20 ; 移動するが、線は描かれない`
`PENDOWN ; ペンを下ろすので、再び描画されるようになる`
`FD 20 ; 直線を描きつつタートルが移動する`
`PENUP ; ペンを持ち上げる。そのため描画されなくなる`
`FD 40 ; 移動するが、線は描かれない`
`PENDOWN ; ペンを下ろすので、再び描画されるようになる`
`RT 20 ; 右（時計回り）に20度回転`

LOGOの設計は「しきいは低く、天井はない」(low threshold and no ceiling) という精神で貫かれており、初心者にとってはとっつきやすいが熟練したユーザーが使えば高度なこともできる。アニメーションを行うには図形を描画し、それを消去する機能を必要とする。タートルのアナロジーでは、タートルが描画だけでなく消去もできなければならない。UCBLogoでは PENERASE (PE) というコマンドで既に描かれているものをタートルが消去することができる。その状態でFDコマンドを使えば、タートルが通った跡に沿って既に描画されていたものが消去される。再び描画状態にするには PENPAINT (PPT) コマンドを使用する。

### 手続き

  - command - 何らかの副作用があるが、値は返さない。例えば `print`
  - operation - 値を返す。例えば、`sum`、`first`、`readlist` など。

commandは[Pascal](../Page/Pascal.md "wikilink")において値を返さない「プロシージャ」に似ており、operationはPascalにおいて値を返す「関数」に似ている。 (CQS) で言えば、LOGOのoperationはクエリに相当する。LISPに似た慣習として、返す値が`true`または`false`に限定されているoperationを述語 (predicate) と呼び、慣習として名前の最後に`p`をつける。例えば、`emptyp`、`wordp`、`listp` などがある。

#### プロシージャ

[thumb](https://ja.wikipedia.org/wiki/ファイル:Ucblogo.png "wikilink") プロシージャは、`TO`と`END`で囲まれたコードで次のように定義できる。

`TO CHAIR  REPEAT 4 [FD 100 RT 90]  FD 200  END`

LOGOでは<cite>EDALL</cite>などのコマンドでエディタを呼び出すことができる。エディタではプロシージャを複数行で記述でき、完了の後に解釈される。

`EDALL`

`TO CHAIR`
`REPEAT 4 [FD 100 RT 90]  FD 200`
`END`

新たに定義したプロシージャは名前に対応するワード（上記の例ではCHAIR）としてセーブされるが、LOGOのセッションが終了すると忘れられてしまう。上の例の場合、プロシージャを定義した後は `CHAIR` と入力すれば `REPEAT 4 [FD 100 LEFT 90] FD 200` というコードが実行される。つまり `CHAIR` というワードはコマンドのように使うことができ、例えば `REPEAT 4 [CHAIR]` とすれば `CHAIR` の操作が4回反復される。

`EDALL ; エディタモードに入り、その後実際のプロシージャを記述する`

`TO ERASECHAIR`
`PE`
`BK 200 REPEAT 5 [FD 50 RT 144]`
`PPT`
`END`

`CS CHAIR WAIT 200 ERASECHAIR`

`CS`はグラフィックスウィンドウをクリアするコマンド、`WAIT`は指定した時間だけ待つコマンドである。次のようにすればアニメーションが可能となる。

`CS REPEAT 20 [CHAIR WAIT 200 ERASECHAIR FD 20]`

### プロシージャ呼出

[thumb](https://ja.wikipedia.org/wiki/ファイル:Ubclogo_function_call.png "wikilink") LOGOではプロシージャに追加情報を渡し、プロシージャが情報を返すことができる。追加情報を使用するプロシージャは、定義の際にそれらに名前をつける。その場合、名前の前のコロンをつける。情報は値渡しであり、コロンは「-の値」を意味する。次の例のように CHAIR 200 という形でプロシージャを呼び出せば、:thesize に200という値がセットされ、FD :thesize とすることで、FDに対して200という値を指定して実行することになる。

`EDALL ;`
`TO CHAIR :thesize`
`REPEAT 4 [FD :thesize RT 90]`
`FD :thesize`
`END`
`CS`
`REPEAT 9 [CHAIR 50 RT 20 CHAIR 100 WAIT 50 RT 20]`

### その他

数式は[前置記法](https://ja.wikipedia.org/wiki/前置記法 "wikilink")が基本であり、`sum :x :y, product :x :y, difference :x :y, quotient :x :y` のように記述する。[中置記法](../Page/中置記法.md "wikilink")も可能である。

キーワードについての説明は`help`コマンドで表示できる。その際キーワードの前にダブルクオートが必要である。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Ubclogo_spiral.png "wikilink")

LOGOは[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")が可能であり、プロシージャの定義内でそのプロシージャ自身を呼び出せる。

`to spiral :size`
`   if  :size > 30 [stop] ; 脱出条件`
`   fd :size rt 15        ; 本体処理`
`   spiral :size *1.02    ; 再帰呼び出し（引数は中置記法の数式）`
`end`

`spiral 10`

[再帰](../Page/再帰.md "wikilink")と描画機能によって、[コッホ曲線](../Page/コッホ曲線.md "wikilink")や[ヒルベルト曲線](https://ja.wikipedia.org/wiki/ヒルベルト曲線 "wikilink")、[二分木](../Page/二分木.md "wikilink")などといった再帰的な図形を自然に描くことができるのもLOGOの大きな特徴である。教育としては、子供に思い思いの図形を定義させ、図形に潜んでいる規則性に気づかせるというような指導が行われている。

原設計者たちが英語話者であったため、英語ベースで設計されたが、他言語をベースとしたコマンドへの置き換えがさかんに行われている言語でもある。例えば日本語化されたコマンドを持つLOGOでは、`FORWARD`を「まえへ」、`RIGHT`を「みぎへ」などとしているものがある。

## 実装

2012年11月時点で、261の実装や方言があり、それぞれに特徴がある\[6\]。その多くは歴史的なもので既に使われていないが、今も活発に開発されているものもある。

標準規格がないが、言語の中核的部分については大まかな合意が形成されている。それでも様々な方言があり、相互に完全な互換性がない。単にの描画プログラムをLOGOと呼んでいる場合があり、状況を混乱させている。

1980年代初頭から中ごろにかけて、[Apple II用の](../Page/Apple_II.md "wikilink") **Apple Logo** や[TI-99/4A](https://ja.wikipedia.org/wiki/TI-99/4A "wikilink")用の **TI Logo** が発売され、初心者のプログラミング入門に最適と宣伝された。このころ欧米の小学校での教育によく使われ、LOGOの最盛期だったといえる。Apple Logo を開発したのはLCSI\[7\]で、これ (LCSI Logo) が初期のLOGO実装として広く普及した。

今日ほぼデファクトスタンダードとされているのがブライアン・ハーヴェイの開発した**UCBLogo** (Berkeley Logo) である\[8\]。フリーかつクロスプラットフォームの実装だが、[GUIは初歩的なものしかなく](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、そのインタフェースを改良するプロジェクトがいくつかある。[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 向けに拡張した**[MSWLogo](https://ja.wikipedia.org/wiki/:en:MSWLogo "wikilink")**\[9\]とその後継である**[FMSLogo](https://ja.wikipedia.org/wiki/:en:FMSLogo "wikilink")**\[10\]は、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")、[オーストラリア](../Page/オーストラリア.md "wikilink")、[ギリシャ](../Page/ギリシャ.md "wikilink")の学校でよく使われている。製品として販売されているLOGOも学校でよく使われており、**[MicroWorlds](https://ja.wikipedia.org/wiki/:en:MicroWorlds "wikilink")**や**Imagine Logo**などがある。

MSWLogoは複数のタートルを扱え、3Dグラフィックスを描画できる。またウィンドウインタフェースもサポートしており、GUIを通したI/Oも可能で、キーボードやマウスからのイベントを扱える。MSWLogo 6.5 では gifsave コマンドで簡単な[GIFアニメーション](../Page/GIFアニメーション.md "wikilink")も生成できる。

最近の実装では、数千ものタートルを同時に扱える。代表的な実装として、[MITの](../Page/マサチューセッツ工科大学.md "wikilink")**[StarLogo](https://ja.wikipedia.org/wiki/StarLogo "wikilink")**\[11\]\[12\]とCCL (Center for Connected Learning) の**[NetLogo](https://ja.wikipedia.org/wiki/NetLogo "wikilink")**\[13\]がある。これを使って[創発](../Page/創発.md "wikilink")現象など、社会学、生物学、物理学などの分野の研究も行われている。

多くのLOGO実装は2Dグラフィックスしか扱えないが、**Elica**などは3Dグラフィックスをサポートしている\[14\]。多くの実装はインタプリタだが、Elicaの作者は**Lhogho**というコンパイラも開発している\[15\]。元々タートルは単純な[ロボット](../Page/ロボット.md "wikilink")に対する操作をコンピュータ上で再現した物であるため、ロボット操作との親和性が非常に高い。そのためロボット制御ができる実装もある。例えば、[レゴ](../Page/レゴ.md "wikilink")で作ったものをLOGOで操作するということも行われていたが、後に[MINDSTORMS](../Page/MINDSTORMS.md "wikilink")として発展させた際に別の言語を採用した。その元になった Crikets はレゴとMITが共同開発したもので\[16\]、そのための **Criket Logo** が開発された\[17\]。

オブジェクト指向的拡張を施した実装として**[ObjectLOGO](https://ja.wikipedia.org/wiki/:en:ObjectLOGO "wikilink")**\[18\]などがある。

LOGOを3次元グラフィックスに拡張した実装として**Logo3D**もある\[19\]。

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装されたオープンソースのLOGOとして Daniel Azuma の開発した**TurtleTracks**がある。これは BSD Logo に拡張を施したもので、後に George Birbilis が [.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") / [J♯](../Page/J_Sharp.md "wikilink") で動かしたものもある。

**E-Slate Logo** はTurtleTracksに[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")的プリミティブ (TELL, ASK, EACH, TELLALL) を追加して拡張したもので、こちらも開発は George Birbilis である\[20\]。

日本で開発された、あるいは日本語版が発売されたLOGOとして以下の例がある。

  - [ドリトル](../Page/ドリトル_\(プログラミング言語\).md "wikilink") (Dolittle) - ロゴ言語実行環境「ロゴ坊」を拡張したもの。厳密にはLogo言語から派生したオリジナル言語を用いる。
  - FindOut - 旧[福武書店が](https://ja.wikipedia.org/wiki/ベネッセコーポレーション "wikilink")、[ACCESSと共同で開発した教育用環境](../Page/ACCESS_\(企業\).md "wikilink")。
  - [GLOGO](http://www.osakac.ac.jp/ecip/cybercampus/glogo.html) - 大阪電気通信大学が開発した3次元対応LOGO
  - LogoWriter - LCSI Logoの日本語版。[PC-9801](https://ja.wikipedia.org/wiki/PC-9801 "wikilink")シリーズをはじめ多くの機種に対応した、日本におけるLogoブームの火付け役となった実行環境。現行バージョンは「ロゴライターWin 4」。のちに[レゴ・マインドストームのロボット制御用Logoとして](../Page/MINDSTORMS.md "wikilink")「Lego Logo」も開発された（日本では「レゴロゴコントロール Lego TC Logo」として、Logo Writer 2とテクニカルレゴがセットでパッケージ販売された。
  - Microworlds - LCSI Logoの日本語版。現行バージョンは「マイクロワールドEx」、派生バージョンとしてEx Roboticsがある。他にMicroworlds Jr、Microworlds Pro。

## 影響

LOGOはプログラミング言語[Smalltalk](../Page/Smalltalk.md "wikilink")に大きな影響を与えた。オブジェクト指向がタートル・グラフィックスに起源を持つことはよく知られている\[21\]\[22\]。[Smalltalk](../Page/Smalltalk.md "wikilink")から派生した[Squeak](../Page/Squeak.md "wikilink")で書かれたプログラミング教育環境[Etoys](https://ja.wikipedia.org/wiki/Etoys "wikilink")もLOGOの影響を強く受けている。

学習者の学習環境として思考の表現方法としては、そのEtoys、同じくSqueakで書かれたMITの[Scratch](https://ja.wikipedia.org/wiki/Scratch_\(プログラミング言語\) "wikilink")\[23\]、カーネギーメロン大学の\[24\]、Elicaがその可能性を競い合っている。

LOGOはまた、Boxerの基盤言語でもある。Boxerは[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")と[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")の共同開発プロジェクトで、「[リテラシー](../Page/リテラシー.md "wikilink")モデル」に基づくマイクロワールドの一種である\[25\]。

は、緩やかにLOGOに基づいた子供向けプログラミング環境であり、[KDE](../Page/KDE.md "wikilink")上で動作する[KDE Education Projectに含まれる](https://ja.wikipedia.org/wiki/KDE_Education_Project "wikilink")\[26\]\[27\]。

## 脚注

## 参考文献

  -
  -
  -
  - *How to Think Like a Computer Scientist: Logo Version (Paperback)*, Allen Downey & Guido Gay, Lulu .

  - *The Great Logo Adventure*, Jim Muller, Doone Publications ISBN 0-9651934-6-2 - 絶版だが、[MSWLogo](http://www.softronix.com/logo.html)のサイトからPDFファイルを圧縮したものをダウンロード可能

  - [*To Artificial Intelligence* (1976)](http://history.dcs.ed.ac.uk/archive/docs/ArtificialIntelligence/art0084.html) - LOGOを多く使っている初期のAIの教科書（[エディンバラ大学](../Page/エディンバラ大学.md "wikilink")の方言 AI2LOGO を使用）

  - [Turtle Geometry](http://www.amazon.com/gp/product/0262510375) Abelson and diSessa

  - *Children Designers*, Idit Harel Caperton, Ablex Publishing Corporation ISBN 0893917885.

  - *Learning With Logo*, Daniel Watt, McGraw Hill, ISBN 0-07-068570-3.

  - Teaching With Logo: Building Blocks For Learning, Molly Watt and Daniel Watt, Addison Wesley (now Pearson) 1986, ISBN 0-201-08112-1

## 関連項目

  - [SMC-777](../Page/SMC-777.md "wikilink") - 同言語環境（DR LOGO）が標準でサポートされていた。
  - [N88-BASIC](../Page/N88-BASIC.md "wikilink") - NECの初期のパソコンにはタートルグラフィック機能を実装したBASICがついていた。
  - [UCSD Pascal](../Page/UCSD_Pascal.md "wikilink") - LOGOと同様に教育用として開発された言語で、タートルグラフィック機能が実装されていた。
  - [知育玩具](../Page/知育玩具.md "wikilink") - 遊びを通して教育ないし知能をトレーニングする[玩具](../Page/玩具.md "wikilink")。LOGOも広義の知育玩具である。
  - [Processing](../Page/Processing.md "wikilink")

## 外部リンク

  - [Logo Foundation](http://el.media.mit.edu/logo-foundation/) - ロゴ情報の基本である。英語
  - [株式会社ロゴコミュニティ](http://www.logocom.jp/) - 旧株式会社ロゴジャパンが2003年に改組。ロゴライターWinの発売元。
  - [ロゴ情報室](http://dolittle.eplang.jp/index.php?Logo%BE%F0%CA%F3%BC%BC) - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[環境で動作するLOGOプラットフォーム](../Page/オペレーティングシステム.md "wikilink")「ロゴ坊」が[フリーウェア](../Page/フリーウェア.md "wikilink")で提供されている。
  - [MSWLogo, An Educational programming language](http://www.softronix.com/logo.html) - MSWLogo配布ページ
  - [ドリトル](http://dolittle.eplang.jp/index.php) - 学習環境ドリトルの情報サイト
  - [マイクロワールド](http://microworlds.jp/) - LCSI Logoの日本語版、現行製品、FCマネージメントのサイト
  - [NetLogo](http://ccl.sesp.northwestern.edu/netlogo/) - ノースウェスタン大学NetLogoのサイト。教育用、シミュレーションモデリング用
  - [PLOGO](http://olivier.sc.free.fr/logosc/plogosc/telechar.htm) - フランス製のLogo配布ページ
  - [rLogo](http://www.embry.com/rLogo/) - rLogo配布ページ
  - [StarLogo](http://education.mit.edu/starlogo/) - MITのStarLogo配布ページ、教育用、シミュレーションモデリング用
  - [TerrapinLogo](http://www.terrapinlogo.com/) - TerrapinLogoのサイト
  - [TinyLogo](http://www.palmspot.com/software/detail/ps3104a_98232.html) - Palm用Logo
  - [Win-Logo](http://www.win-logo.de/eng/e_index.htm) - Win-Logo配布ページ。英語・独語
  - [xLogo](http://xlogo.sourceforge.net/) - xLogo配布ページ
  - [Logo Interpreter](http://www.calormen.com/logo/) - オンラインで利用可能
  - [Learn Logo for free](http://turtleacademy.com/)

[Category:ロボットプログラミング言語](https://ja.wikipedia.org/wiki/Category:ロボットプログラミング言語 "wikilink") [Category:教育用プログラミング言語](https://ja.wikipedia.org/wiki/Category:教育用プログラミング言語 "wikilink") [Category:フリー教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:フリー教育ソフトウェア "wikilink")

1.  、、
2.  [Logo Foundation](http://el.media.mit.edu/logo-foundation/logo/index.html)
3.  [Cynthia Solomon](https://logothings.wikispaces.com/)
4.  [Logo Foundation](http://el.media.mit.edu/logo-foundation/index.html)
5.  [Logo Programming Language at the Logo Foundation website](http://el.media.mit.edu/logo-foundation/logo/programming.html)
6.  [The Logo Tree Project](http://elica.net/download/papers/LogoTreeProject.pdf)
7.  <http://www.microworlds.com/>
8.  [Berkeley Logo (UCBLogo)](http://www.cs.berkeley.edu/~bh/logo.html)
9.  [MSWLogo](http://www.softronix.com/logo.html)
10. [FMSLogo](http://fmslogo.sourceforge.net/)
11. [StarLogo](http://education.mit.edu/starlogo/)
12. [StarLogo](http://mas.kke.co.jp/modules/tinyd4/index.php?id=5)
13. [NetLogo](http://ccl.northwestern.edu/netlogo/)
14. [Elica](http://www.elica.net/site/index.html)
15. [Lhogho](http://lhogho.sourceforge.net/)
16. [Crikets](http://llk.media.mit.edu/projects.php?id=1942)
17. [Criket Logo](http://llk.media.mit.edu/projects/cricket/doc/help/cricketlogo/cricketlogo.html)
18. [Object Logo](http://www.digitool.com/ol-specs.html)
19.
20. [E-Slate](http://e-slate.cti.gr/)
21. <http://jibun.atmarkit.co.jp/ljibun01/rensai/gyoukai/042/01.html>
22. <http://www.h6.dion.ne.jp/~origami/LOGO.html>
23. [Scratch](http://scratch.mit.edu/)
24. [Alice](http://www.alice.org/)
25. [Boxer](http://www.soe.berkeley.edu/boxer/)
26. [*The programming language used in KTurtle is loosely based on Logo.*](http://edu.kde.org/kturtle/)
27. [KTurtle](http://www.kde.gr.jp/applications/education/kturtle/)