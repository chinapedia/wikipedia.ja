> この記事は[Verilog](https://ja.wikipedia.org/wiki/Verilog)から翻訳されています。


**Verilog**（ヴェリログ）は、**IEEE 1364**として標準化されている[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")（Hardware Description Language; HDL）である。最も重要な用途は、[デジタル回路](../Page/デジタル回路.md "wikilink")を[レジスタ転送レベル](../Page/レジスタ転送レベル.md "wikilink")で設計・検証することである。また、[アナログ回路](../Page/アナログ回路.md "wikilink")やの検証や、の設計にも使用されている\[1\]。

もともとVerilogは[電子回路シミュレーション](https://ja.wikipedia.org/wiki/電子回路シミュレーション "wikilink")を行うシミュレータであり、それに使用する言語であった。文法は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")の[C言語](../Page/C言語.md "wikilink")や[Pascal](../Page/Pascal.md "wikilink")に似ている。

後継言語は[SystemVerilog](../Page/SystemVerilog.md "wikilink")で、おおむねVerilogのスーパーセットである。System Verilogの規格と統合して、「IEEE/IEC 62530:2011 SystemVerilog - Unified Hardware Design, Specification, and Verification Language」と呼ばれる標準になっている。

## 概要

Verilogのようなハードウェア記述言語は、[ソフトウェアプログラミング言語に似ている](../Page/プログラミング言語.md "wikilink")。これは、信号の伝達時間や信号強度を記述するコードから作られているからである。Verilogには、ブロッキング代入とノン・ブロッキング代入という2種類の代入演算子がある。ノン・ブロッキング代入文のおかげで、設計者はステートマシンの更新をを宣言せずに書くことができるようになった。これらの概念はVerilog言語のセマンティックの一部となっているため、設計者は大規模な回路の記述を比較的にコンパクトで簡潔な形式ですばやく書くことができる。Verilogが開発された当初（1984年）、回路設計者はグラフィカルなソフトウェアや、ドキュメントと[電子回路シミュレータ](https://ja.wikipedia.org/wiki/電子回路シミュレータ "wikilink")のためだけに書かれた特殊なソフトウェアを使っていたため、複雑な回路を簡潔に記述できるVerilogは、極めて大きな生産性の向上をもたらした。

Verilogの設計者は、言語の構文を、工学分野の[ソフトウェア開発](../Page/ソフトウェア開発.md "wikilink")で当時すでに広く普及していた[C言語](../Page/C言語.md "wikilink")と似たものにしたいと考えた。そのため、C言語のように、Verilogの識別子は [ケース・センシティブ](https://ja.wikipedia.org/wiki/ケース・センシティブ "wikilink")であり、基本的な[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")ーを持っている（ただし、ANSI C/C++のものほどは洗練されていない）。制御フローの[キーワード](../Page/予約語.md "wikilink")（if/else、for、while、caseなど）はC言語と同一であり、[演算子の優先順位](https://ja.wikipedia.org/wiki/演算子の優先順位 "wikilink")もC言語と互換性がある。構文の違いとしては、変数宣言にビット幅が必要であることや、手続きブロックの宣言の相違（カーリー・ブレイス{}の代わりにbegin/endを使用する）があり、その他多数の細かな違いがある。Verilogは変数に固定サイズを与えなければならないが、C言語の場合はサイズは変数の「型」から推定される（たとえば、integer型は8ビットであると）。

Verilogのコードはから構成する。モジュールは設計の階層をカプセル化し、他のモジュールとは、宣言された入力、出力、必要に応じて双方向ポートを使用して通信する。モジュールの内部では、net/変数の宣言（wire、reg、integerなど）、[並行または逐次の](../Page/並行性.md "wikilink")[ステートメントブロック](../Page/ブロック_\(プログラミング\).md "wikilink")、他のモジュールのインスタンス（サブ階層）などの、あらゆる組み合わせが記述できる。逐次的な文は、begin/endブロック内に配置し、ブロック内では逐次的に実行される。しかし、ブロック自体は並列に実行されるため、この特徴によりVerilogは[データフロー言語](https://ja.wikipedia.org/wiki/データフロー言語 "wikilink")となっている。

次に、配線を示すwire、記憶素子を示すregとサブモジュールのリストなどを定義する。さらに、続いてその動作を規定するステートメントやステートメントをグループにしたブロック群を定義する。ブロックはbeginキーワードで始まり、endキーワードで終わる範囲で定義し、ブロック内はステートメントが並列に実行される。逐次実行したい場合は、ブロッキング代入を使うか、クロックのタイミングを待つ書き方をする。各ブロックは並列に実行される。Verilogの'wire'の概念は信号の値 (4状態："1、0、floating、undefined") と信号の強度（強い、弱いなど）からなる。このシステムのおかげで、共有信号線の抽象的なモデリングが可能になり、複数のソースで共通の回路網を駆動することが可能になった。wireが複数のドライバーを持つ時、wireの（読み取り可能な）値はソースドライバーの関数と強度で解決される。

Verilog言語の文のサブセットは、[合成可能である](../Page/論理合成.md "wikilink")。RTL（register-transfer level; レジスタ転送レベル）として知られる合成可能なコーディングスタイルを使用して書かれたVerilogのモジュールは、合成ソフトウェアを使用することで物理的に実装することができる。合成ソフトウェアは、アルゴリズムを用いて、（抽象的な）Verilogのソースをネットリストに変換する。とは、特定の[FPGA](../Page/FPGA.md "wikilink")や[VLSI](https://ja.wikipedia.org/wiki/VLSI "wikilink")技術で利用可能な基本ゲート（AND、OR、NOT、フリップフロップなど）のみからなるソースコードと論理的に等価な記述である。さらにネットリストに修正を加えることで、究極的には（[ASIC](../Page/ASIC.md "wikilink")の[フォトマスク](../Page/フォトマスク.md "wikilink")のセットやFPGAの[ビットストリーム](https://ja.wikipedia.org/wiki/ビットストリーム "wikilink")などの）電子回路製造の設計図を生成することが可能である。

「Verilog-HDL」という表記が用いることがあるが、IEEEなどの文書では「Verilog」と「HDL」との間にハイフンが入らない「Verilog HDL」のように表記されている。

## 歴史

### 始まり

Verilogは、社の[フィル・ムーアビー](../Page/フィル・ムーアビー.md "wikilink")が、ハードウェア・モデリング言語とそのためのシミュレータとして[1984年](../Page/1984年.md "wikilink")頃開発した。その後、同社は[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に[ケイデンス・デザイン・システムズ](../Page/ケイデンス・デザイン・システムズ.md "wikilink")が買収した。ケイデンスは、現在も大元のゲートウェイVerilogおよびVerilog-XL論理シミュレータの版権を持っている。

### 標準化

同種のハードウェア記述言語である[VHDL](../Page/VHDL.md "wikilink")の台頭に対し、ケイデンスはVerilogの規格を公開し標準化する道をとり、OVI（Open Verilog International）と呼ばれる組織へ版権の一部を移譲した。その後、Verilogの規格が[IEEE](../Page/IEEE.md "wikilink")に提出され、IEEE 1364-1995\[2\]として標準化された。この標準は、Verilog-1995と呼ばれる。なお、OVIはその後Accelleraという組織になっている。

標準化にともない、ケイデンス社以外の会社やフリーソフトのVerilogシミュレータが登場するようになった。

### Verilog 2001

オリジナルのVerilog標準に対する不満を解消するために、Verilog-95に対する拡張がなされた。この拡張はVerilog 2001といいIEEE 1364-2001\[3\]になった。VHDLにあったgenerate文に対応し、大規模設計が容易になった。

### Superlog/System Verilog

やがてOpenVeraやVerisityのE言語のようなハイ・レベルの検証言語が登場する。このことはその種の機能を盛り込んだVerilog、すなわちコデザイン・オートメーション社によるSuperlogの開発を促すこととなった。コデザイン・オートメーション社は、[シノプシス](../Page/シノプシス.md "wikilink")によってその後買収された。SuperlogとVeraの基本部分はAccelleraに寄贈され、次のIEEE標準として[SystemVerilog](../Page/SystemVerilog.md "wikilink")とVerilogとに分かれた。

### Verilog-AMS

言語の最新のバージョンは、アナログ素子および回路の機能記述を行うための言語である[Verilog-A](https://ja.wikipedia.org/wiki/Verilog-A "wikilink")を包含し、さらにアナログ／デジタルのミックス・シグナル・モデルへの対応もなされており、Verilog-AMSという。

### Verilog 2005

IEEE 1364-2005\[4\] として規格化。その際、上位互換の SystemVerilog IEEE 1800-2005 も作った。

### System Verilog 2011

IEEE/IEC 62530-2011 - SystemVerilog – Unified Hardware Design, Specification, and Verification Language \[5\]として、Verilog HDLとSystem Verilogの文書を一本化した。

## 例

簡単な2フリップフロップの例を以下に示す。

``` verilog
module toplevel(clock,reset);
  input clock;
  input reset;

  reg flop1;
  reg flop2;

  always @ (posedge reset or posedge clock)
    if (reset)
      begin
        flop1 <= 0;
        flop2 <= 1;
      end
    else
      begin
        flop1 <= flop2;
        flop2 <= flop1;
      end
endmodule
```

Verilogにおける"\<="演算子は、普通の手続き型言語とは異なる、ハードウェア記述言語としてのもう1つの側面である。この演算子は「ノンブロッキング」代入文として知られ、alwaysブロックが実行されるまでアクションは登録されない。つまり、代入文を書いた順序は無関係であり、必ず同じ結果が生じる。そのため、flop1とflop2はクロックごとに値がスワップされることになる。

もう1つの代入演算子である"="は、ブロッキング代入文と呼ばれる。"="による代入が行われると、代入先の値は即座に更新される。もし上の例で"\<="の代わりにブロッキング演算子の"="を使用したとすると、flop1とflop2の値はスワップされず、手続き型プログラミング言語のように、コンパイラはflop1の値をflop2の値にセットするのだと解釈する（その結果、flop2とflop1の値にセットするという冗長な論理は無視されることになる）。

モジュールはキーワードmoduleで始まる。その後のDiv20xが名前を示し、続く括弧内は端子リストである。6個の端子があり、それぞれの端子の入出力方向はモジュール中のポート宣言（inputとoutput）で指定される。最後のendmoduleでモジュールの終了である。モジュール内には、パラメータ宣言、ポート宣言、レジスタ宣言、イベント宣言、ネット宣言、ステートメントなどを記述する。

``` verilog
//
// 表題 イネーブル付20段カウンター
//
module Div20x (
    // ポート宣言（外部から本モジュールへの接続を定義する）
    input clock,  // クロック
    input reset,  // リセット（正論理, ハイアクティブ）
    input cet,    // カウンターとTC出力のイネーブル
    input cep,    // カウンターのみのイネーブル
    output reg [size - 1:0] count,   // 束線を示す。この場合5bit幅
                                     // alwaysまたはinitialブロックでドライブする信号は
                                     // reg型でなければならない
    output tc);                      // regと明記していない、他の信号はwire型。
                                     // ポート宣言したwire型信号のネット宣言は省略可能であり、省略することも多い。

    // パラメータ宣言
    parameter length = 20; // カウント段数
    parameter count_zero = 5'b00000; // 5bit幅,2進数の0を表す
    parameter count_one  = 5'b00001; // 5bit幅,2進数の1を表す
    parameter size = 5;   // bit幅,基数の指定を省略すると32bit,10進数になる。

    // always文。resetやclock信号の変化に同期し並列に実行される
    always @ (posedge clock or posedge reset) begin
        if (reset) begin // 非同期リセット
            count <= count_zero;
        end else begin
            if (cet || cep) begin // イネーブル
                if (count == length - 1) begin
                    count <= count_zero;
                end else begin
                    count <= count + count_one;
                end
            end
        end
    end

    // assign文。tcの値は実行中、継続的に値が与る
    assign tc = (cet && (count == length - 1));
endmodule
```

ポート宣言やレジスタ宣言での\[a:b\]のような形式は、束線（多くはバス）を示す。例えば\[3:0\]であれば配線が4本あることになる。always節は、括弧内の信号を指定した条件に変化があったときに実行される。posedgeは信号が0から1に変化した場合を指定する。orは括弧内の信号のどれか1つでも変化した場合を指定する。上記のように、resetに合わせてreg型を初期化するのが基本的な[デザインパターンである](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。

ディレイの例は以下の通りである。

``` verilog
...
reg a, b, c, d;
wire e;
...
always @(b or e)
  begin
    a = b & e;
    b = a | b;
    #5 c = b;
    d = #6 c ^ e;
  end
```

上記の**always**節は、もう1つの使い方を示している。たとえば、上の例では、リストに含まれる要素（**b**または**e**）が変化したタイミングでいつでもalways節が実行される。いずれかの変数が変化すると、即座に新しい値が**a**に代入される。ブロッキング代入文を使用しているため、**b**にはその代入後に（**a**の新しい値を用いて）新しい値が代入される。5単位時間のディレイの後、**c**に**b**の値が代入されると同時に、**c ^ e**の値が計算され、見えない保管場所に一時的に保存される。6単位時間後、保管されていた値が**d**に代入される。

プロセス内（initialまたはalwaysブロック内）で操作される信号は、**reg**型を持つ必要がある。また、プロセスの外で操作される信号は**wire**型を持たなければならない。この時使われる**reg**という名前は、必ずしもハードウェアのレジスタを意味するわけではない。

## 定数の定義

Verilogにおける定数の定義では、追加のビット幅パラメータがサポートされている。基本的な構文は次のとおりである。

<ビット幅>'<基数を表す文字><数字>

例:

  - 12'h123 — 16進数（hexadecimal）の123（12ビットを使用）
  - 20'd44 — 10進数（decimal）44 (20ビットを使用。未使用桁への0の付加は自動で行われる）
  - 4'b1010 — 2進数（Binary）1010（4ビットを使用）
  - 6'o77 — 8進数（octal）の77（6ビットを使用）

## 回路として合成可能な構成

Verilogのいくつかの文は、たとえば$display文など、現実のハードウェアでは物理的に実装できないものもある。そのため、言語の多くの機能はハードウェアを記述するためには使用できない。以下に示す例では、直接物理的なゲートに対応する、合成可能な言語の典型的なサブセットを使用している。

``` verilog
// Mux の例 — 同じ動作をする例を3種類の方法で示す。

// 1番目の例は連続束縛を使用している。
wire out;
assign out = sel ? a : b;

// 2番目の例は同じことを行うために手続き的な表現を使用している。

reg out;
always @(a or b or sel)
  begin
    case(sel)
      1'b0: out = b;
      1'b1: out = a;
    endcase
  end

// 3番目の例: 手続き構造の中で if/else 文を使用することもできる。
reg out;
always @(a or b or sel)
  if (sel)
    out = a;
  else
    out = b;
```

次の非常によく使われる例は、[フリップフロップ](../Page/フリップフロップ.md "wikilink")である。Verilogでは、D-フリップフロップが最も簡単に記述でき、以下のようにモデリングできる。

``` verilog
reg q;
always @(posedge clk)
  q <= d;
```

例の中で注目すべき重要な点は、ノンブロッキング代入を使用していることである。基本的な経験則（）として、always節の中で**posedge**または**negedge**文を使用する場合には、**`<=`**を使用するとよい。

Dフリップフロップの変種として、非同期リセット機能を付加したものがある。慣習として、以下のようにリセット状態をチェックするコードを文内の最初のif節とすることが多い。

``` verilog
reg q;
always @(posedge clk or posedge reset)
  if(reset)
    q <= 0;
  else
    q <= d;
```

## initialとalwaysキーワード

Varilogの処理を宣言する方法には、**always**キーワードと**initial**キーワードという異なる2つの方法がある。**always**キーワードは、自由に実行される処理を表す。**initial**キーワードは、ちょうど1回だけ実行される処理を表す。2つの処理はともに、シミュレーター時刻0に実行が開始され、ともにブロックの終わりまで実行される。**always**ブロックの場合、処理がブロックの最後に到達すると、実行が再度スケジュールされる。よくある間違いは、initialブロックは常にalwaysブロックの前に最初に実行されるというものである。実際には、**initial**ブロックは、1回目の実行時に終了する特殊な**always**-ブロックであると考えるとよい。

``` verilog
// 例:
initial
  begin
    a = 1; // reg a の値を 0 に束縛する
    #1; // 1 単位時間待つ
    b = a; // reg a の値を reg b の値に束縛する
  end

always @(a or b) // a または b が *変更された* タイミングで処理が行われる
begin
  if (a)
    c = b;
  else
    d = ~b;
end // このブロックが終了すると、先頭から処理が再開される (例: @ event-control)

always @(posedge a) // reg a が low から high に変更されるたびに実行される
  a <= b;
```

上記2つは、これら2つのキーワードの典型的な使用例であるが、更に2つの特徴的な使用例がある。最もよく使うのが、信号強度を書いたリスト**@(...)**なしで**always**キーワード使用する方法である。alwaysは以下のように使用することもできる。

``` verilog
always
 begin // always は時刻0に実行が始まり、*決して* 終了しない
   clk = 0; // clk を 0 にセットする
   #1; // 1 単位時間待つ
   clk = 1; // clk を 1 にセットする
   #1; // 1 単位時間待つ
 end // 実行を続ける — したがって、begin から実行が再開する
```

**always**キーワードは、C言語の**while(1) {..}**構造と同じように無限ループとして振る舞う。

もう1つの特徴的な使用例は、**initial**キーワードに**forever**キーワードを追加するというものである。

次の例は、上の**always**の例と同等である。

``` verilog
initial forever // 時刻 0 で実行が開始され、begin/end の間の処理を永遠に (forever) 繰り替える
 begin
   clk = 0; // clk を 0 にセットする
   #1; // 1 単位時間待つ
   clk = 1; // clk を 1 にセットする
   #1; // 1 単位時間待つ
 end
```

## Fork/join

**fork/join**のペアは、Verilog内で並列処理を作るために使われる。fork/joinのペアの間にある文（またはブロック）は、実行フローで**fork**に到達したタイミングで同時に実行が開始され、**fork**と**join**の間で最も長い時間実行される文またはブロックの終了後、残りのコードの実行が再開する。

``` verilog
initial
 fork
   $write("A"); // 文字 A を出力する
   $write("B"); // 文字 B を出力する
   begin
     #1; // 1 単位時間待つ
     $write("C");// 文字 C を出力する
   end
 join
```

上のように書いた場合、出力は"ABC"または"BAC"のいずれにもなる可能性がある。最初の$writeと2番目の$writeのシミュレーションの実行順序は、シミュレータの実装に依存するためである。シミュレータによっては、意図的に順序をランダム化していることもある。そのため、偶然競合状態が起きたり、意図的な非決定的な振る舞いをする場合がある。

VHDLは、Verilogとは違い、複数のプロセスを動的に生成することはできない\[6\]。

## 競合状態

Verilogでは、実行の順序は常に保証されるわけではない。これは、典型的な例で最もよく示すことができる。次のコードスニペットについて考えてみる。

``` verilog
initial
  a = 0;

initial
  b = a;

initial
  begin
    #1;
    $display("Value a=%d Value of b=%d",a,b);
  end
```

aおよびbの値として出力されるのはどんな値だろうか？initialブロックの実行順序によって、それぞれ0と0になる場合と、0と何らかの初期化されていない値となる場合の2パターンがありえる。ただし、$display文は\#1ディレイを挟んでいるため、2つの代入ブロックより後に実行されることが常に保証されている。

## 演算子

注意：これらの演算子は優先度の順に並んでいるわけでは*ない*。

| 演算の種類       | 演算子記号                          | 実行する演算                                                   |
| ----------- | ------------------------------ | -------------------------------------------------------- |
| ビット操作       | \~                             | ビット単位NOT（1ビットの否定）                                        |
| &           | ビット単位AND                       |                                                          |
| |           | ビット単位OR                        |                                                          |
| ^           | ビット単位XOR                       |                                                          |
| \~^ または ^\~ | ビット単位XNOR                      |                                                          |
| 論理演算        | \!                             | NOT                                                      |
| &&          | AND                            |                                                          |
| <nowiki>    | </nowiki>                      | OR                                                       |
| リダクション      | &                              | Reduction AND                                            |
| \~&         | Reduction NAND                 |                                                          |
| |           | Reduction OR                   |                                                          |
| \~|         | Reduction NOR                  |                                                          |
| ^           | Reduction XOR                  |                                                          |
| \~^ または ^\~ | Reduction XNOR                 |                                                          |
| 数値演算        | \+                             | 加算                                                       |
| \-          | 減算                             |                                                          |
| \-          | 次の値の否定                         |                                                          |
| \*          | 乗算                             |                                                          |
| /           | 除算                             |                                                          |
| \*\*        | べき乗（\*Verilog-2001）            |                                                          |
| 関係演算        | \>                             | 大なり                                                      |
| \<          | 小なり                            |                                                          |
| \>=         | 以上                             |                                                          |
| \<=         | 以下                             |                                                          |
| \==         | 論理的に等しい（1'bXのビット値は比較対象から除外される） |                                                          |
| \!=         | 論理的に異なる（1'bXのビット値は比較対象から除外される） |                                                          |
| \===        | 4値理論で等しい（1'bXのビット値はリテラルとみなされる） |                                                          |
| \!==        | 4値理論で異なる（1'bXのビット値はリテラルとみなされる） |                                                          |
| シフト操作       | \>\>                           | [論理右シフト](https://ja.wikipedia.org/wiki/シフト演算 "wikilink") |
| \<\<        | 論理左シフト                         |                                                          |
| \>\>\>      | 算術右シフト（\*Verilog-2001）         |                                                          |
| \<\<\<      | 算術左シフト（\*Verilog-2001）         |                                                          |
| 連結          | { および }                        | 連結                                                       |
| 複製          | {n{m}}                         | 値mをn回複製する                                                |
| 条件分岐        | ? :                            | 条件分岐                                                     |

## 4値理論

IEEE 1364標準では、0、1、Z（[ハイ・インピーダンス](https://ja.wikipedia.org/wiki/ハイ・インピーダンス "wikilink")）、X（論理値が未知）の4つの状態を使用するが定義されている。一方、Verilogの競合であるVHDLの標準では、9つのレベルを持つ多値理論が定義されている。

## システムタスク

システムタスクは、シミュレーション中に単純なI/Oや設計測定関数を操作するために利用できる。すべてのシステムタスクは、**$**が接頭辞になっており、ユーザー定義のタスクや関数と区別される。このセクションでは、最もよく使用されるタスクの一覧を紹介する。完全なリストではないことに注意。

  - $display — 1行を画面に表示する。自動で改行文字を付加する。
  - $write — 1行を画面に表示する。改行文字は加えない。
  - $swrite — 改行文字無しで変数を1行で出力する。
  - $sscanf — 変数から書式指定で文字列を読み込む。 (\*Verilog-2001)
  - $fopen — ファイルハンドルを開く。読み込みまたは書き込みのために使用する。
  - $fdisplay — ファイルに1行を書き込む。自動で改行文字を付加する。
  - $fwrite — ファイルに1行を書き込む。改行文字は加えない。
  - $fscanf — ファイルから書式指定で文字列を読み込む。（\*Verilog-2001）
  - $fclose — オープンしたファイルハンドルを閉じて開放する。
  - $readmemh — 16進数ファイルの内容をメモリ配列に読み込む。
  - $readmemb — バイナリファイルの内容をメモリ配列に読み込む。
  - $monitor — 何らかの変更が発生した時に、すべての変数リストを出力する。
  - $time — 現在のシミュレーション時刻の値。
  - $dumpfile — VCD（[Value Change Dump](https://ja.wikipedia.org/wiki/:en:Value_change_dump "wikilink")）フォーマットでの出力ファイル名を宣言する。
  - $dumpvars — 変数を有効にしてダンプする。
  - $dumpports — 変数を有効にしてExtended-VCDフォーマットでダンプする。
  - $random — ランダムな値を返す。

## プログラム言語インターフェイス

PLI（Program Language Interface）は、プログラマーに対して、VerilogからC言語で書かれたプログラムに制御を移すことを可能にするメカニズムを提供する。IEEE Std 1364-2005において、PLIは新しいに完全に置き換えられて公式に[非推奨](https://ja.wikipedia.org/wiki/非推奨 "wikilink")となった。

PLI（現在はVPI）を利用することで、Verilogは、たとえば、[テストハーネス](https://ja.wikipedia.org/wiki/テストハーネス "wikilink")、[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")の[命令セットシミュレータ](https://ja.wikipedia.org/wiki/命令セットシミュレータ "wikilink")、[デバッガ](../Page/デバッガ.md "wikilink")など、C言語で書かれた他のプログラムと連携することができる。たとえば、PLIはC言語の関数`tf_putlongp()`および`tf_getlongp()`を提供しており、この関数を利用すると、現在のVerilogタスクや関数の引数の値を読み書きすることができる。具体的には、`tf_putlongp(pin, lower_32, higher_32)`は、C言語側の `higher_32` と `lower_32` を、Verilog側の64幅のpin信号にセットすることができ, `lower_32 = tf_getlongp(higher_32, pin)`は、Verilog側の64幅のpin信号を読み出し、その上位と下位をC言語側の変数 `higher_32` と `lower_32` にそれぞれセットする。

## 主要ソフトウェア

### シミュレータ

  - 有償
      - Incisive Enterprise Simulator (Verilog-XL、NC-Verilog) ケイデンス社 [1](http://www.cadence.co.jp/products/sd/index.html)
      - VCS シノプシス社[2](http://www.synopsys.com/JP2/Tools/Verification/FunctionalVerification/Pages/VCS.aspx)
      - [ModelSim](https://ja.wikipedia.org/wiki/ModelSim "wikilink") [メンター・グラフィックス](../Page/メンター・グラフィックス.md "wikilink")社
      - VeriLogger Extreme シナプチキャド社 [3](http://www.syncad.com/verilogger_verilog_simulator.htm)
      - Veritak [4](http://japanese.sugawara-systems.com/)
      - FinSim [5](http://www.fintronic.com/)
      - Aldec Active-HDL [6](http://www.aldec.com/Products/Product.aspx?productid=f8ee0c96-cd00-4b24-812c-c2935fe143ae)
      - Dolphine SMASH [7](http://www.dolphin.fr/medal/smash/smash_overview.php)
      - Axiom MPSim [8](http://www.axiom-da.com/mpsim.html)
      - ISim [9](http://japan.xilinx.com/tools/isim.htm) [Xilinx](https://ja.wikipedia.org/wiki/Xilinx "wikilink")社 (制限付き版は無償)
  - 無償
      - [Icarus Verilog](https://ja.wikipedia.org/wiki/Icarus_Verilog "wikilink") [10](http://iverilog.icarus.com/)
      - GPL Cver [11](http://sourceforge.net/projects/gplcver/)
      - Verilator [12](http://www.veripool.org/wiki/verilator)
      - VeriWell Verilog Simulator [13](http://sourceforge.net/projects/veriwell/)

### 論理合成

  - Design Compiler シノプシス社
  - Encounter RTL Compiler ケイデンス社

### lint チェックツール

  - SpyGlass (Synopsys)
  - Leda (Synopsys)　
  - ALINT (Aldec)　
  - Accent lint (Real Intent)

## 文献

  -
  -
## 関連項目

  - [EDA (半導体)](../Page/EDA_\(半導体\).md "wikilink")
  - [ASIC](../Page/ASIC.md "wikilink")
  - [FPGA](../Page/FPGA.md "wikilink")
  - [Property Specification Language](https://ja.wikipedia.org/wiki/Property_Specification_Language "wikilink")

## 出典

<references />

[Category:ハードウェア記述言語](https://ja.wikipedia.org/wiki/Category:ハードウェア記述言語 "wikilink")

[Category:EDAソフト](https://ja.wikipedia.org/wiki/Category:EDAソフト "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink")

1.
2.  [1364-1995 IEEE Standard Hardware Description Language Based on the Verilog(R) Hardware Description Language](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=803556)
3.  [1364-2001 IEEE Standard Verilog Hardware Description Language](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=954909)
4.  [1364-2005 IEEE Standard for Verilog Hardware Description Language](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=1620780)
5.  <http://standards.ieee.org/findstds/standard/62530-2011.html>
6.