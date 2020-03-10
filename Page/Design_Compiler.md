> この記事は[Design Compiler](https://ja.wikipedia.org/wiki/Design_Compiler)から翻訳されています。


**Design Compiler**（デザインコンパイラ）は、米[シノプシス](https://ja.wikipedia.org/wiki/シノプシス "wikilink")社が開発した[論理合成](../Page/論理合成.md "wikilink")ソフトウェアである。あるいはそれを中核とした、ソフトウェア群の総称である。

## 概要

[ハードウェア記述言語](https://ja.wikipedia.org/wiki/ハードウェア記述言語 "wikilink")(HDL)や真理値表で書かれた論理回路定義を[論理ゲート](https://ja.wikipedia.org/wiki/論理ゲート "wikilink")レベル回路に変換するための[論理合成](../Page/論理合成.md "wikilink")ツールの一つである。使用できるHDLとしては[Verilog HDL](https://ja.wikipedia.org/wiki/Verilog "wikilink") 、[VHDL](https://ja.wikipedia.org/wiki/VHDL "wikilink")などのほか [SystemVerilog](../Page/SystemVerilog.md "wikilink")や[SystemC](https://ja.wikipedia.org/wiki/SystemC "wikilink")へも対応している。合成された結果は同社標準の論理回路[ライブラリ](../Page/ライブラリ.md "wikilink")のほか [半導体](../Page/半導体.md "wikilink")ベンダーが作成したライブラリを使って、ネットリスト（配線情報）化される。

米[シノプシス](https://ja.wikipedia.org/wiki/シノプシス "wikilink")社が開発・販売しており、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")現在、[集積回路](../Page/集積回路.md "wikilink")、特に[ASIC](../Page/ASIC.md "wikilink")製造に用いる論理合成ツールの[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となっている。

## Design Compiler を用いた論理合成の流れ

### ハードウェアの設計

作成したいハードウェアを設計し、それをVerilog HDL 、VHDLなどのハードウェア記述言語や[真理値表](https://ja.wikipedia.org/wiki/真理値表 "wikilink")を用いて論理を記述する。 ただし記述は[レジスタ転送レベル](../Page/レジスタ転送レベル.md "wikilink")でなければならない。

### デザインのリード

論理合成を行うために、デザインをリードする。 デザインをリードするには、readコマンドを実行する。

  - Verilogの場合

`>  read -f verilog filename.v`

### 制約条件の選定

論理合成を行うにあたり、そのハードウェアの仕様が要求する制約条件を指定する。 制約条件には例えば以下のようなものがある。

#### 配線負荷

設計するハードウェアの配線負荷のことである。 設計するハードウェアによって、シリコン上に配線される配線長が変わってくる。 Design Compilerでは、モジュール同士(設定により異なる)の配線長をどの位に想定するかを設定することができる。 set_wire_load_modeコマンドでは、どのレベル(モジュール単位、チップ単位他)を負荷計算に考慮するのかを設定できる。 set_wire_loade_modeコマンドでは、ベンダーがおのおの提供している値。 そのライブラリを用いたときの負荷の特性が、ライブラリに設定されている。

#### 入力遅延

LSIや、ASICなどのハードウェアは、単体で動作させることはない。 つまり、基板に実装し、CPUでASICを制御したりする。 そのため、自分が設計したLSIへの入力信号が、水晶振動子が出しているタイミングと同時に来るとは分からない。 そのため、Design Compilerには次のコマンドが用意されている。

`>  set_input_delay x[ライブラリの単位時間] -clock CLK[定義したクロック名] -all_inputs()[全ての入力ピンに適用]`

同様に、出力に対しての遅延時間も設定することができる。

### コンパイル

適切な制約条件が決定したら、論理記述をコンパイルする。コンパイルには `compile` コマンドを用いる。

`> compile `

コンパイル時には選定した制約条件を指定する。

### report_timing

論理変換したデザイン内の遅延パスを表示させるコマンド。単純に`report_timing`と入力すると、そのデザイン内の最大遅延パスを表示する。以下に、一例を示す。

  - **[クロック](../Page/クロック.md "wikilink")[スキュー](https://ja.wikipedia.org/wiki/スキュー "wikilink")のレポートの取り方**

`> report_timing -delay min_rise -from CTS/Z to [all_registers -clock CTS/Z -clock_pins]`

CTS/Zから出力されている[クロック](../Page/クロック.md "wikilink")を用いている全ての[レジスタで](../Page/レジスタ_\(コンピュータ\).md "wikilink")、そのクロックの立ち上がりでの最小遅延パスを求めている。

`> report_timing -delay max_rise -from CTS/Z to [all_registers -clock CTS/Z -clock_pins]`

同様に、最大遅延パスを求めている。

この差を用いれば、そのデザイン内の最大[クロック](../Page/クロック.md "wikilink")[スキュー](https://ja.wikipedia.org/wiki/スキュー "wikilink")が求められる。

## 関連項目

  - [論理合成](../Page/論理合成.md "wikilink")
  - [Verilog](https://ja.wikipedia.org/wiki/Verilog "wikilink")

## 外部リンク

  - [Design Compiler製品概要](http://www.synopsys.co.jp/products/designcompilerfamily/) — 日本シノプシス

[Category:EDAソフト](https://ja.wikipedia.org/wiki/Category:EDAソフト "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink")