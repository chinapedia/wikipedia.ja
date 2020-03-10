> この記事は[CPLD](https://ja.wikipedia.org/wiki/CPLD)から翻訳されています。


[Altera_MAX_7128_2500_gate_CPLD.jpg](https://ja.wikipedia.org/wiki/File:Altera_MAX_7128_2500_gate_CPLD.jpg "fig:Altera_MAX_7128_2500_gate_CPLD.jpg")製の2500ゲートを持つMAX 7000シリーズのCPLD\]\]

**CPLD (Complex Programmable Logic Device)**とは、[プログラマブルロジックデバイス](../Page/プログラマブルロジックデバイス.md "wikilink")の一種で、[PALと](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス#PLD "wikilink")[FPGA](../Page/FPGA.md "wikilink")の中間の集積度を持ち、これら両方のアーキテクチャの特徴を持っている。CPLD で作られるブロックは[マクロセル](https://ja.wikipedia.org/wiki/マクロセル "wikilink")であり、これには[加法標準形](https://ja.wikipedia.org/wiki/加法標準形 "wikilink")での表現とより特殊な論理的操作が実装されている。

PALと共通する特徴は以下のようである。

  - 不揮発性であるコンフィギュレーションメモリである。多くの[FPGA](../Page/FPGA.md "wikilink")と違い、コンフィギュレーション[ROM](https://ja.wikipedia.org/wiki/ROM "wikilink")は必要ない。CPLDはシステムが立ち上がるとすぐに機能する。
  - 多くの古いCPLDデバイスでは、ほとんどの論理ブロックは外部ピンに接続され信号を入力あるいは出力しており、内部情報の記憶や深くレイヤ化された論理に使用されることは少なくなっていた。
  - これは、一般には、より大きなCPLDやより新しいCPLD製品ファミリーには当てはまらない。

FPGAと共通する特徴は以下のようである。

  - 多数のゲートが利用可能である。CPLDは典型的には数千から数万の[論理ゲートに相当するものを持ち](https://ja.wikipedia.org/wiki/論理回路#.E7.B5.84.E3.81.BF.E5.90.88.E3.82.8F.E3.81.9B.E5.9B.9E.E8.B7.AF "wikilink")、中程度に複雑なデータ処理デバイスを実装することができる。PALは典型的には数百の論理ゲートに相当するものを持ち、FPGAは典型的には数万から数百万の範囲の論理ゲートを持つ。
  - 提供されている論理は、[論理和または論理積よりフレキシブルで](https://ja.wikipedia.org/wiki/加法標準形 "wikilink")、マクロセル間での複雑なフィードバックパスや多くのよく使われる機能 (例えば、[整数](../Page/整数.md "wikilink")[演算](https://ja.wikipedia.org/wiki/演算 "wikilink")など)を実装するための特別な論理が含まれている。

CPLDとFPGAのアプリケーション上重要な違いのひとつに、CPLDはチップ上の不揮発性のメモリでコンフィギュレーションされている、ということがある。この特徴のために、CPLDは電源投入時の[ブート](../Page/ブート.md "wikilink")ローダのためのデバイスとして使われている。典型的な例として、不揮発性メモリからFPGAへコンフィギュレーションデータをロードするのにCPLDを使う、というものがある。しかし、最新FPGA製品にはコンフィギュレーションメモリを組み込んだモデルも存在する。

CPLDは、それ以前に普及していたより小さな規模の[PLA](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス#PLD "wikilink")(これは最初に[シグネティックス](https://ja.wikipedia.org/wiki/シグネティックス "wikilink")によって出荷された)や[PALといったデバイスから進歩してきたものであり](https://ja.wikipedia.org/wiki/プログラマブルロジックデバイス#PLD "wikilink")、PLAやPALは、プログラム機能を提供せずいくつかの[汎用ロジックIC](../Page/汎用ロジックIC.md "wikilink")をワイヤで接続することによってプログラムする方法から進歩してきた。

FPGAとCPLDのデバイスアーキテクチャ上の主な違いは、FPGAが内部的には[ルックアップテーブル](https://ja.wikipedia.org/wiki/ルックアップテーブル "wikilink")(LUT)をベースにしているのに対し、CPLDはチャネルレス型ゲートアレイ(SOG)による論理機能によっていることである。

## 関連項目

  - [ASIC](../Page/ASIC.md "wikilink")
  - [:en:Erasable programmable logic device](https://ja.wikipedia.org/wiki/:en:Erasable_programmable_logic_device "wikilink") (EPLD) 英語
  - [:en:Simple programmable logic device](https://ja.wikipedia.org/wiki/:en:Simple_programmable_logic_device "wikilink") (SPLD) 英語
  - [:en:Macrocell array](https://ja.wikipedia.org/wiki/:en:Macrocell_array "wikilink") 英語
  - [:en:Programmable array logic](https://ja.wikipedia.org/wiki/:en:Programmable_array_logic "wikilink") (PAL) 英語
  - [プログラマブルロジックデバイス](../Page/プログラマブルロジックデバイス.md "wikilink") (PLD)
  - [:en:Field-programmable gate array](https://ja.wikipedia.org/wiki/:en:Field-programmable_gate_array "wikilink") (FPGA) 英語
  - [VHDL](https://ja.wikipedia.org/wiki/VHDL "wikilink")
  - [Verilog](https://ja.wikipedia.org/wiki/Verilog "wikilink")

## 著名なCPLDメーカー

  - [アルテラ](../Page/アルテラ.md "wikilink")
  - [アトメル](https://ja.wikipedia.org/wiki/アトメル "wikilink")
  - [サイプレス・セミコンダクタ](https://ja.wikipedia.org/wiki/サイプレス・セミコンダクタ "wikilink")
  - [ラティスセミコンダクター](https://ja.wikipedia.org/wiki/ラティスセミコンダクター "wikilink")
  - [ザイリンクス](https://ja.wikipedia.org/wiki/ザイリンクス "wikilink")

[fr:Circuit logique programmable\#CPLD](https://ja.wikipedia.org/wiki/fr:Circuit_logique_programmable#CPLD "wikilink")

[Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink") [Category:デジタル回路](https://ja.wikipedia.org/wiki/Category:デジタル回路 "wikilink")