> この記事は[SystemC](https://ja.wikipedia.org/wiki/SystemC)から翻訳されています。


**SystemC**（システムシー）は、[電子回路](../Page/電子回路.md "wikilink")機器の[機能設計への使用を目的とした](https://ja.wikipedia.org/wiki/回路設計#ディジタル集積回路の設計 "wikilink")[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink") (HDL) の一種である。SystemC登場以前より存在し、純然たるHDLである[Verilog](../Page/Verilog.md "wikilink")や[VHDL](../Page/VHDL.md "wikilink")に比べ、動作レベルモデリングなど、よりシステム寄りの記述言語である。

## 仕様

SystemCは、[プログラム言語](https://ja.wikipedia.org/wiki/プログラム言語 "wikilink")である[C++](../Page/C++.md "wikilink")のクラスライブラリを提供している。独立した文法ではない。ライブラリにはハードウェア記述の為の機能、並列実行の概念やデータ型を扱う各種関数を定義している。プログラムはC++コンパイラで[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")することができる。生成したオブジェクトはハードウェアの[シミュレータ](https://ja.wikipedia.org/wiki/シミュレータ "wikilink")として動作する。

言語としては、VerilogやVHDLと類似点も持つ。C++に由来する[抽象データ型](../Page/抽象データ型.md "wikilink")や[テンプレート](../Page/テンプレート_\(プログラミング\).md "wikilink")、動的なメモリ割り当てなどを使った自由度が大きく、抽象度の高い記述が可能である。自由に、抽象的に記述したものを実際のハードウェア化するのは困難なことである。論理合成ツールの能力に依存する。VerilogやVHDLで論理合成可能な具体化は人手による介在が必要な場合がある。仕様あるいは、あるアルゴリズムを最初は純然たるソフトウェアとして記述、デバッグ、その後順次ハードウェアに変換していくということがC++という同じ枠内でできるということに意味があるということである。

SystemCは複数の[EDA](https://ja.wikipedia.org/wiki/EDA "wikilink")ベンダーや大学などの研究機関により提案され仕様が策定されてきた。2005年時点でのバージョンは2.1、さらに2007年3月には、バージョン2.2を公開した。トランザクションレベル・モデルライブラリを検討した。 2011年、IEEE 1666 IEEE Standard for Standard SystemC Language Reference Manualとして規格になっている。

## 言語要素

### モジュール

モジュールはSystemCによる設計の階層中で基本となるブロックである。SystemCのモデルでは、ポート（次項）を通じて通信する複数のモジュールから構成される。

### ポート

ポートは、モジュール内部と外部とを接続する端子である。通常は別のモジュールのポートに接続される。

### プロセス

プロセスは、メインとなる処理要素である。個々のプロセスは同時、並列に実行される。

### チャネル

チャネルは通信の要素であり、単純な配線のこともあれば、FIFOのような複雑なメカニズムのこともある。

基本チャネル:

  - 信号
  - バッファ
  - FIFO
  - [ミューテックス](../Page/ミューテックス.md "wikilink")
  - [セマフォ](../Page/セマフォ.md "wikilink")

### インターフェイス

ポートはチャネルとの通信にインターフェイスを使用する。

### イベント

プロセス間の同期を取るために用いる。

### データタイプ（型）

SystemCはモデリングを支援するいくつかのデータタイプを用意している。

C++標準の型を拡張したもの:

  - sc_int\<\> 64-bitまでの符号付整数
  - sc_uint\<\> 64-bitまでの符号無整数
  - sc_bigint\<\> 可変精度符号付整数 (※1)
  - sc_biguint\<\> 可変精度符号無整数 (※1)

論理型:

  - sc_bit 2-値シングルビット (※2)
  - sc_logic 4-値シングルビット
  - sc_bv\<\> sc_bitのベクター（可変配列）
  - sc_lv\<\> sc_logicのベクター

固定小数点型:

  - sc_fixed\<\> 符号付固定小数点テンプレート
  - sc_ufixed\<\> 符号無固定小数点テンプレート
  - sc_fix 符号付固定小数点
  - sc_ufix 符号無固定小数点

※1 sc_bigint\<\>, sc_biguintは、sc_int\<\>, sc_uint\<\>に比べ著しくシミュレーションスピードが遅い

※2 sc_bitは、IEEE1666ではdeprecated featuresであり、代わりにboolの使用が薦められている

## 例

[加算器](../Page/加算器.md "wikilink")の記述例:

``` c
# include "systemc.h"

SC_MODULE(adder)          // モジュール (クラス) 宣言
{
  sc_in<int> a, b;        // ポート
  sc_out<int> sum;

  void do_add()           // プロセス
  {
    sum = a + b;
  }

  SC_CTOR(adder)          // コンストラクタ
  {
    SC_METHOD(do_add);    // カーネルへのdo_addの登録
    sensitive << a << b;  // do_addのセンシティビティリスト
  }
};
```

## 参考文献

  - Grötker, Thorsten 『SystemCによるシステム設計』柿本勝、河原林政道、長谷川隆（監訳）、[丸善](https://ja.wikipedia.org/wiki/丸善 "wikilink")、2003年 ISBN 4-621-07144-0 C3055
  - 1666-2011 - IEEE Standard for Standard SystemC Language Reference Manual

## 関連項目

  - [SpecC](https://ja.wikipedia.org/wiki/SpecC "wikilink")
  - [SystemVerilog](../Page/SystemVerilog.md "wikilink")

## 外部リンク

  - [SystemC ホームページ（英語）](http://www.systemc.org)

[Category:EDAソフト](https://ja.wikipedia.org/wiki/Category:EDAソフト "wikilink") [Category:ハードウェア記述言語](https://ja.wikipedia.org/wiki/Category:ハードウェア記述言語 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink")