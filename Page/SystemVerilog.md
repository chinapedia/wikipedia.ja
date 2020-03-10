> この記事は[SystemVerilog](https://ja.wikipedia.org/wiki/SystemVerilog)から翻訳されています。


**SystemVerilog** は、[ハードウェア記述言語](https://ja.wikipedia.org/wiki/ハードウェア記述言語 "wikilink")の[Verilog](https://ja.wikipedia.org/wiki/Verilog "wikilink") HDLを拡張した言語で、主に検証に関する機能が拡張・統合されている。2002年に[Accellera](http://www.accellera.org)に対して Superlog 言語を寄付したことで生まれた\[1\]。検証機能の部分は[シノプシス](https://ja.wikipedia.org/wiki/シノプシス "wikilink")が提供した OpenVera に基づいている。2005年、SystemVerilog は [IEEE](../Page/IEEE.md "wikilink") Standard 1800-2005 として標準化された\[2\]。

## 全体構成

SystemVerilog は Verilog-2005 の拡張であり、機能的に上位互換となっている。以下では、Verilog-2001 から SystemVerilog で拡張した部分について解説する。Verilog-2001 との共通部分は [Verilog](https://ja.wikipedia.org/wiki/Verilog "wikilink") を参照。

Verilog HDLと同様、その機能は、

  - 設計機能 - [電子回路](../Page/電子回路.md "wikilink")およびシミュレータで利用可能
  - 検証機能 - シミュレータで、テストやデバッグ時に利用

に大別できる。

## 論理合成

Verilog HDL同様、どの機能が[合成可能で](https://ja.wikipedia.org/wiki/論理合成 "wikilink")、どの機能が不可能かは実装次第であり言語マターではない。例えば Altera の Quartus II 11.0 では、共用体はできないが、構造体は論理合成可能である\[3\]。

## 設計機能

ここでは、主に、[論理合成](https://ja.wikipedia.org/wiki/論理合成 "wikilink")可能である可能性が高いと思われる物を述べる（前述のように実装次第であり言語マターではないため）。

### 新たなデータ型

**多次元詰め込み配列**により、Verilog の "registers" と "memories" を統合拡張した:

``` systemverilog
reg [1:0][2:0] my_var[32];
```

本来の Verilog では変数名の左には一次元の宣言しかできなかった。SystemVerilog は任意の詰め込み次元を指定可能である。詰め込み配列型の変数には整数算術実体を 1:1 でマップする。上記の例では、`my_var` の各要素は6ビットの整数を表す。名前の右側にある次元（例では32）は詰め込み型でない次元である。Verilog-2001 と同様、詰め込み型でない次元は任意の次元の指定が可能である。

**列挙データ型**により、数値実体に意味のある名前をつけることが可能となった。列挙型で宣言された変数は、他の列挙型とは cast なしで代入できない。これはパラメータには当てはまらない。Verilog-2005 での列挙型の実装に合わせたためである。

``` systemverilog
typedef enum reg [2:0] {
   RED, GREEN, BLUE, CYAN, MAGENTA, YELLOW
} color_t;

color_t   my_color = GREEN;
```

このように、設計者は基となる算術型（この場合 `reg [2:0]`）を指定し、その値に名前を付ける。メタ値 X と Z を使うこともでき、不正状態を表すのに使う。

**新しい整数型**: SystemVerilog では `byte`、`shortint`、`int`、`longint` という二値統合型を定義しており、それぞれ8ビット/16ビット/32ビット/64ビットである。`bit` 型は不定長の二値型であり、`reg` と似たような働きをする。二値型では reg では使えるメタ値 X と Z が使えない。このため、シミュレーションの高速化を期待する。Verilog-2001 にもある integer と time はそのまま四値が使える。

**浮動小数点型**: real (64ビット)に加えて、shortreal (32ビット)を追加。

**構造体**と**共用体**は[C言語](../Page/C言語.md "wikilink")と同様の働きをする。SystemVerilog ではこれらに**詰め込み型**属性を導入し、詰め込み型配列のビット列に構造体や共用体を 1:1 で対応させることができる:

``` systemverilog
typedef struct packed {
    bit [10:0]  expo;
    bit         sign;
    bit [51:0]  mant;
} FP;

FP     zero = 64'b0;
```

### Unique/priority if/case

入れ子になった `if` や `case` 文において、**unique**属性を指定することで必ず1つの分岐（case）だけが実行されることを指示できる（どれも実行できない場合はエラーとなる）。つまり、各ケースは並行して実行可能である。`if` や `case` 文での **priority**属性は条件を順次評価していくことを示す。これまで[アノテーション](https://ja.wikipedia.org/wiki/アノテーション "wikilink")で `synopsys full_case parallel_case` を使って指示していたことを正式にキーワードとして指示できるようになったのである。

### 手続き的ブロック

Verilog の `always` ブロックに加え、SystemVerilog では設計構造をより意識した手続きブロックを新たに提供している。これによってEDAツールはどういう動作が求められているのかを正確に把握できるようになる。

`always_comb` ブロックは組合せ論理を生成する。シミュレータはブロック内の文からセンシティビティ・リストを推定する:

``` systemverilog
always_comb begin
    tmp = b * b - 4 * a * c;
    no_root = (tmp < 0);
end
```

`always_ff` ブロックは順序論理（FF回路）を推定する:

``` systemverilog
always_ff @(posedge clk)
    count <= count + 1;
```

`always_latch` ブロックはラッチを推定する。この場合もセンシティビティ・リストはコードから推定できる:

``` systemverilog
always_latch
    if (en) q <= d;
```

## 検証機能

以下の検証機能は[論理合成](https://ja.wikipedia.org/wiki/論理合成 "wikilink")不可能であることが多いと思われる。目的としては、[シミュレーター](https://ja.wikipedia.org/wiki/シミュレーター "wikilink")用に拡張可能で柔軟なテストベンチの生成を支援するためのものである。

### 新たなデータ型

`string` データ型は任意長のテキスト文字列を表す。

設計で使われる静的配列に加え、SystemVerilog は動的配列、連想配列、キューを提供する:

``` systemverilog
int da[];       // 動的配列
int da[string]; // 文字列をインデックスとする連想配列
int da[$];      // キュー

initial begin
    da = new[16]; // 16要素を生成
end
```

動的配列は非詰め込み型の配列のように働くが、上で示したように動的に生成されなければならない。この配列は必要に応じてサイズを変更できる。連想配列はユーザー指定のキーの型とデータ型による[二分探索木](https://ja.wikipedia.org/wiki/二分探索木 "wikilink")のようなものである。キーによる暗黙の順序付けがあり、辞書式順序で読み出すことができる。キューは [C++](../Page/C++.md "wikilink") の [STL](https://ja.wikipedia.org/wiki/Standard_Template_Library "wikilink") にある [deque](https://ja.wikipedia.org/wiki/deque "wikilink") 型の機能とほぼ同等のものを提供する。要素の追加や削除がキューの両端から可能である。これらのデータ型は大規模設計で必要となる複雑なデータ型の生成を可能とする。

### クラス

SystemVerilog は[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")モデルも提供する。

SystemVerilog クラスは、単一インタフェースモデルである。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の `interface` のように複数のインタフェースを使用することはできない。SystemVerilog のクラスは型をパラメータ化でき、C++ の[テンプレートのような機能を提供する](../Page/テンプレート_\(プログラミング\).md "wikilink")。しかし、関数テンプレートやテンプレートの特殊化は対応していない。

[ポリモーフィズム](https://ja.wikipedia.org/wiki/ポリモーフィズム "wikilink")機能はC++と似ている。`virtual` 指定で関数を書くことで、派生型がその関数の制御を奪うことができる。

[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")とデータ隠蔽は `local` および `protected` というキーワードで実現され、任意のアイテムに指定して隠蔽できる。デフォルトでは、全てのクラス属性が public である。

SystemVerilog のクラスのインスタンスは `new` キーワードで生成する。`function new` でコンストラクタを定義できる。SystemVerilog は[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")もサポートしており、インスタンスを明示的に解放・消去する機能はない。

例:

``` systemverilog
virtual class Memory;
    virtual function bit [31:0] read(bit [31:0] addr); endfunction
    virtual function void write(bit [31:0] addr, bit [31:0] data); endfunction
endclass

class SRAM #(parameter AWIDTH=10) extends Memory;
    bit [31:0] mem [1<<AWIDTH];

    virtual function bit [31:0] read(bit [31:0] addr);
        return mem[addr];
    endfunction

    virtual function void write(bit [31:0] addr, bit [31:0] data);
        mem[addr] = data;
    endfunction
endclass
```

### 制約乱数生成

整数実体はクラス定義内であれ、何らかのスコープ内の独立した変数であれ、ある制約に基づいた乱数を設定可能である。これは検証のためにランダムなシナリオを生成する際に便利である。

クラス定義内で、修飾子 `rand` や `randc` を指定することで変数に乱数を設定する。`randc` は順列型の乱数を生成する。つまり、同じ値を生成する前に可能な範囲の全ての値を一通り必ず生成する。修飾子のない変数を乱数化しない。

``` systemverilog
class eth_frame;
    rand bit [47:0] dest;
    rand bit [47:0] src;
    rand bit [15:0] type;
    rand byte       payload[];
    bit [31:0]      fcs;
    rand bit [31:0] fcs_corrupt;

    constraint basic {
        payload.size inside {[46:1500]};
    }

    constraint good_fr {
        fcs_corrupt == 0;
    }
endclass
```

この例では、`fcs` というフィールドを乱数化していない。実際、これは[CRC生成の計算に関するコードであり](../Page/巡回冗長検査.md "wikilink")、`fcs_corrupt` フィールドは[FCSエラーを発生するのに使う](https://ja.wikipedia.org/wiki/Frame_Check_Sequence "wikilink")。2つの制約により、[イーサネット](../Page/イーサネット.md "wikilink")のフレームの検査をしようとしていることがわかる。制約は選択的に適用可能で、上の例では壊れたフレームを生成するのに制約選択機能を用いる。制約には複雑なものも指定でき、変数間の関係や含意や繰り返しを指定できる。SystemVerilog の制約解読機能は解があれば必ずそれを見つけることを求められるが、解の探索にかかる時間を保証しない。

### 表明

SystemVerilog は[表明](https://ja.wikipedia.org/wiki/表明 "wikilink")記述言語を内包しており、[Property Specification Language](https://ja.wikipedia.org/wiki/Property_Specification_Language "wikilink") に似ている。表明は、各時点での設計上の特性を照合するのに使う。

SystemVerilog の表明は **sequence**（シーケンス）と **property**（属性）から構成される。属性はシーケンスの上位概念であり、シーケンスは属性としても扱うことが可能である。ただし、それが必ずしも有益というわけではない。

シーケンスには、時相演算子を使ったブーリアンの式を指定する。最も単純な時相演算子 `##` は連結を意味する:

``` systemverilog
sequence S1;
@(posedge clk)
req ##1 gnt;
endsequence
```

このシーケンスでは、`gnt` 信号が `req` 信号が High となった1クロック後に High となることを表明している。このようにシーケンス型の表明は常にクロックと同期している。

これ以外にも様々な時相演算子がある。これらを使うとコンポーネント間の設計上の複雑な関係を表現することができる。

1つの表明は、あるシーケンスや属性の状態を連続的に監視し、表明に記述したことに反する動作をするとエラーとなる。上記のシーケンスは `req` が Low であった場合に失敗する。`gnt` に続いて `req` が High になるということを正確に表現するには属性表明が必要となる:

``` systemverilog
property req_gnt;
@(posedge clk)
req |=> gnt;
endproperty

assert_req_gnt: assert property (req_gnt) else $error("req not followed by gnt.");
```

この例では**含意**演算子 `|=>` を使っている。含意の左辺は **antecedent**（先行事項）と呼ばれ、右辺は **consequent**（結果事項）と呼ぶ。含意の評価は、まず先行事項を繰り返し評価することから開始する。先行事項が成功すると、結果事項を評価する。表明全体として成功するかどうかは結果事項の評価結果に依存する。この例では結果事項は `req` が High になるまで評価せず、`gnt` がその1クロック後にHighにならない場合にこの属性表明に失敗する。

表明のほかに、SystemVerilog は属性の「仮定; assumptions」と「カバレッジ; coverage」に対応している。仮定とは、形式論理証明ツールで必ず真となる条件を記述するものである。表明は真であることが証明されなければならない属性を指定する。シミュレーションでは、表明と仮定は並行して検査する。属性のカバレッジは、表明が正確に設計を監視しているかどうかを検証するためのものである。

### カバレッジ

ハードウェア検証言語における**カバレッジ**とは、シミュレーション時のイベントをサンプリングした統計情報群を意味する。カバレッジを利用して評価対象デバイス(DUT)が正しく機能しているかどうかをある程度正確に判定できる。これは、[ソフトウェアテスト](https://ja.wikipedia.org/wiki/ソフトウェアテスト "wikilink")でコードが実行された割合の尺度である[コード網羅率](https://ja.wikipedia.org/wiki/コード網羅率 "wikilink")（code coverage）とは異なる概念であることに注意されたい。機能カバレッジでは、必要とする設計上の隅々まで検証していることを保証する。

SystemVerilog のカバレッジグループは関連する変数の値の[度数分布](../Page/度数分布.md "wikilink")のデータベースを生成する。クロスカバレッジを定義することもでき、複数の変数の値の組合せ（[直積集合](../Page/直積集合.md "wikilink")）の度数分布を生成する。

サンプリングイベントはサンプルを採取するタイミングを制御する。サンプリングイベントは Verilog のイベントでもよいし、ブロックの出入り口でも、カバレッジグループの `sample` メソッド呼び出しでもよい。ただし、意味があるデータだけをサンプル採取するよう注意しなければならない。

例:

``` systemverilog
class eth_frame;
   covergroup cov;
      coverpoint dest {
          bins bcast[1] = {48'hFFFFFFFFFFFF};
          bins ucast[1] = default;
      }
      coverpoint type {
          bins length[16] = { [0:1535] ];
          bins typed[16] = { [1536:32767] };
          bins other[1] = default;
      }
      psize: coverpoint payload.size {
          bins size[] = { 46, [47:63], 64, [65:511], [512:1023], [1024:1499], 1500 };
      }

      sz_x_t: cross type, psize;
   endgroup
endclass
```

この例では、検証者はブロードキャストのフレームとユニキャストのフレームに注目し、特に size/type フィールドとペイロードサイズに注目している。ペイロードサイズの coverpoint には注目している限界値群を反映していて、最大フレームと最小フレームを含んでいる。

### 同期

複雑なテスト環境では、再利用可能な検証コンポーネント群が相互に通信しながら動作する。SystemVerilog は通信と同期のための2つのプリミティブを用意している。**mailbox** と **mutex** である。mutex は計数型[セマフォ](https://ja.wikipedia.org/wiki/セマフォ "wikilink")のようなものである。mailbox は[FIFO](https://ja.wikipedia.org/wiki/FIFO "wikilink")の一種である。mailbox は型をパラメータ化でき、指定された型のみ通すようにできる。これらのオブジェクトは **transactions** のクラスインスタンスであり、検証コンポーネントが実行する基本操作群（例えば、フレームを送信するなど）である。

## 参考文献

<references />

## 外部リンク

  - [SystemVerilog.org](http://www.systemverilog.org/) - IEEE 標準化前のホームページ
  - ワーキンググループ
      - [IEEE P1800 SystemVerilog Working Group](http://www.eda.org/sv-ieee1800/)
      - [SystemVerilog Technical Committees](http://www.vhdl.org/sv/) - IEEE 標準化前の委員会
  - 仕様書
      - [1800-2012 IEEE Standard for SystemVerilog--Unified Hardware Design, Specification, and Verification Language](http://ieeexplore.ieee.org/document/6469140/)
      - [SystemVerilog 3.1a 言語リファレンスマニュアル](http://www.vhdl.org/sv/SystemVerilog_3.1a.pdf) - IEEE 1800の仕様となる前の2004年の物。

[Category:ハードウェア記述言語](https://ja.wikipedia.org/wiki/Category:ハードウェア記述言語 "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink")

1.  Rich, D. “The evolution of SystemVerilog” IEEE Design and Test of Computers, July/August 2003
2.  \[<http://www.eetimes.com/news/design/showArticle.jhtml>;?articleID=173601060 IEEE approves SystemVerilog, revision of Verilog\]
3.  [Quartus II Support for SystemVerilog](http://quartushelp.altera.com/11.0/mergedProjects/hdl/hdl.htm#vlog/vlog_list_sys_vlog.htm)