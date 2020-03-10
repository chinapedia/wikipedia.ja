> この記事は[Guarded Command Language](https://ja.wikipedia.org/wiki/Guarded_Command_Language)から翻訳されています。


**Guarded Command Language**（**GCL**）とは、[エドガー・ダイクストラ](../Page/エドガー・ダイクストラ.md "wikilink")が[述語変換意味論](../Page/述語変換意味論.md "wikilink")向けに定義した言語である\[1\]

## ガード付きコマンド

ガード付きコマンドはGCLの最重要要素である。ガード付きコマンドは名前の通り、[ガードが付いている](../Page/ガード_\(プログラミング\).md "wikilink")。ガードは一種の[命題](../Page/命題.md "wikilink")であり、その文を実行する前に真でなければならない。文の実行前に、そのガードは真であると仮定される。また、ガードが偽であった場合、その文は実行されない。ガード付きコマンドを使うことで、[プログラムがその仕様に適合していることを証明することが容易になる](../Page/プログラム_\(コンピュータ\).md "wikilink")。ガード付きコマンドの本体（実行すべき文）がガード付きコマンドになっていることが多い。

### 構文

ガード付きコマンドは、 \(G \rightarrow{S}\) という形式の[文であり](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")、ここで

  - \(G\) は、ガードと呼ばれる[命題](../Page/命題.md "wikilink")である。
  - \(S\) は文である。

\(G \equiv \mbox{True}\) なら、ガード付きコマンドは単に \(S\) と記述される。

### 意味論

計算の流れで \(G\) が出てくると、それを評価する。

  - \(G\) が真なら \(S\) を実行する。
  - \(G\) が偽なら、コンテキストに従って次にすべきことを決定する。

## Skip と Abort

Skip と Abort は非常に単純だがガード付きコマンドと同様に重要な要素である。Abort は未定義命令であり、何もしない。Abort は完了することさえ保証されていない。プログラムが何らかの証明の定式化であるとすれば、Abort は証明の失敗に対応する。Skip は空の命令であり、何もしない。文法上、文が必要とされるが、プログラマが状態を変更したくない場合、プログラム内で使われる。

### 構文

  - Skip
  - Abort

### 意味論

  - Skip: 何もしない
  - Abort: 何もしない

## 代入

代入文は[変数に値を代入する](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")。

### 構文

  - \(v := E\)
  - \(v_{0}, v_{1}, ... , v_{n} := E_{0}, E_{1}, ... , E_{n}\)

ここで

  - v はプログラムの変数（群）
  - E は対応する変数と同じ[データ型](https://ja.wikipedia.org/wiki/データ型 "wikilink")の式

## 連結

代入文はセミコロン(;)を間に書いて、並べて記述される。

## 条件文: *if*

選択（一般に、条件文とかif文と呼ばれる）はガード付きコマンドのリストであり、そのうちの1つの文が選択実行される。複数のガードが真である場合、実行する文は[ランダム](../Page/ランダム.md "wikilink")または非決定的に選択される。どのガードも真でない場合、結果は未定義である。少なくとも1つのガードが真でなければならないので、空文の Skip を使うことが多い。

### 構文

\[\mbox{if}\]

\[G_{0} \rightarrow S_{0}\]

\[[]\ G_{1} \rightarrow S_{1}\]

\[...\]

\[[]\ G_{n} \rightarrow S_{n}\]

\[\mbox{fi}\]

### 意味論

  - どのガードも真でない場合: Abort と同じ
  - 1つの \(G_{x}\) だけが真の場合、\(S_{x}\) を実行
  - \(G_{x_{0}}\ ...\ G_{x_{m}}\) がいずれも真の場合、任意の \(S_{x_{y}}\)（ただし \(0 \leq y \leq m\)）を実行

### 例

#### 単純な例

以下のような[擬似コード](https://ja.wikipedia.org/wiki/擬似コード "wikilink")を考える:

  -
    if a \< b then c := True
    else c := False

GCL ではこれが以下のようになる:

\[\mbox{if}\]

\[a < b \rightarrow c := True\]

\[[]\ a \geq b \rightarrow c := False\]

\[\mbox{fi}\]

#### スキップを使用した例

擬似コード:

  -
    if error = True then x := 0

GCLの場合:

\[\mbox{if}\]

\[error = \mbox{True} \rightarrow x := 0\]

\[[]\ error = \mbox{False} \rightarrow \mbox{skip}\]

\[\mbox{fi}\]

2つ目のガードを省いた場合、error = False なら、結果は Abort となる。

#### 複数のガードが真の場合

\[\mbox{if}\]

\[a \geq b \rightarrow max := a\]

\[[]\ a \leq b \rightarrow max := b\]

\[\mbox{fi}\]

a = b の場合、max の新たな値として a または b が選ばれるが、結果は同じである。しかし、[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")によっては、一方がもう一方より性能的に有利だったり容易だったりする場合もある。プログラマから見れば違いはないので、いかようにも実装してよい。

## 繰り返し: *do*

繰り返しは、全てのガードが真でなくなるまでガード付きコマンド群を繰り返し実行する。通常、ガードはひとつだけである。

### 構文

\[\mbox{do}\]

\[G_{0} \rightarrow S_{0}\]

\[[]\ G_{1} \rightarrow S_{1}\]

\[...\]

\[[]\ G_{n} \rightarrow S_{n}\]

\[\mbox{od}\]

### 意味論

  - 全てのガードが真でない場合: Skip
  - \(G_{x}\) だけが真の場合: \(S_{x}\) を実行し、再度ガード群を評価する
  - \(G_{x_{0}}\ ...\ G_{x_{m}}\) が真の場合: いずれかの \(S_{x_{y}}\) （ただし、\(0 \leq y \leq m\)）を実行し、再度ガード群を評価する

### 例

#### [ユークリッドの互除法](../Page/ユークリッドの互除法.md "wikilink")

\[a, b := A, B;\]

\[\mbox{do}\]

\[a > b \rightarrow a := a - b\]

\[[]\ b > a \rightarrow b := b - a\]

\[\mbox{od}\]

この繰り返しは a = b のとき終了し、その際に a と b には A と B の[最大公約数](../Page/最大公約数.md "wikilink")が格納されている。

#### ユークリッドの互除法の拡張

\[a, b, x, y, u, v := A, B, 1, 0, 0, 1;\]

\[\mbox{do}\]

\[b \neq 0 \rightarrow\]

\[q, r := a\ \mbox{div}\ b, a\ \mbox{mod}\ b;\]

\[a, b, x, y, u, v := b, r, u, v, x - q * u, y - q * v\]

\[\mbox{od}\]

この繰り返しは b = 0 のとき終了し、その際に各変数は xa + yb = gcd(a,b) の解を格納している。

## 応用

### 非同期回路

GCLでは、異なるコマンドの選択による様々な遅延を許容した繰り返しが可能であるため、[QDIモデル](https://ja.wikipedia.org/wiki/QDIモデル "wikilink")（Quasi Delay Insensitive）に基づいた回路設計に適している。この場合、以下のようにノード *y* を駆動する論理ゲートは2つのガード付きコマンドで表現される。

\[PulldownGuard \rightarrow y := 0\]

\[PullupGuard \rightarrow y := 1\] *PulldownGuard* と *PullupGuard* はその論理ゲートの入力の関数であり、それぞれゲートの出力を上げたり下げたりする。古典的な回路評価モデルとは異なり、（非同期回路に対応した）ガード付きコマンド群の繰り返しは、正確にその回路の全ての動的振る舞いを説明できる。モデルによっては、ガード付きコマンドに何らかの制限を加える必要があるだろう。典型的な制限としては、安定性、非干渉、自己無効化コマンドを許さない、などがある\[2\]。

### モデル検査

ガード付きコマンドは [Promela](https://ja.wikipedia.org/wiki/Promela "wikilink") というプログラミング言語で使われている。Promela は[SPINモデルチェッカ](https://ja.wikipedia.org/wiki/SPINモデルチェッカ "wikilink")で使われている。SPINは並行ソフトウェアアプリケーションの[モデル検査](https://ja.wikipedia.org/wiki/モデル検査 "wikilink")用ツールである。

### その他

[Perl](../Page/Perl.md "wikilink")の \[<http://search.cpan.org/perldoc/Commands>::Guarded Commands::Guarded\] モジュールは、ダイクストラのガード付きコマンドを決定論的に修正したバージョンである。

## 参考文献

[Category:形式手法](https://ja.wikipedia.org/wiki/Category:形式手法 "wikilink") [Category:論理プログラミング](https://ja.wikipedia.org/wiki/Category:論理プログラミング "wikilink") [Category:エドガー・ダイクストラ](https://ja.wikipedia.org/wiki/Category:エドガー・ダイクストラ "wikilink")

1.
2.