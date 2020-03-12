> この記事は[FPU](https://ja.wikipedia.org/wiki/FPU)から翻訳されています。


**FPU**（**Floating Point Unit**、**浮動小数点（演算処理）装置**）とは、[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")演算を専門に行う処理装置のこと。コンピュータの周辺機器のような[アーキテクチャのものもあれば](../Page/コンピュータ・アーキテクチャ.md "wikilink")、主[プロセッサ](../Page/プロセッサ.md "wikilink")と一体化した[コプロセッサ](../Page/コプロセッサ.md "wikilink")のようなアーキテクチャのものもある。

[AMDではAm](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")9511をAPU (Arithmetic Processing Unit) と呼んでおり（2011年以降はAPUを[Accelerated Processing Unitの略称として使用](https://ja.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit "wikilink")）、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")では[x87](https://ja.wikipedia.org/wiki/x87 "wikilink")を**NDP**（**Numeric data processor**, **数値演算コプロセッサ**）、またその命令について**NPX**（**Numeric Processor eXtension**）とも呼んでいる。

[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")においては、[Apple IIの頃は完全に周辺機器のようなアーキテクチャだったが](../Page/Apple_II.md "wikilink")、[8087の頃には命令の一体化など](../Page/Intel_8087.md "wikilink")、CPUの拡張装置のようなアーキテクチャになった。

1990年代中盤以降の高性能プロセッサではFPUはプロセッサ内部のサブユニットとなっている。インテルの[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系CPUでは独立ユニットのFPUは[387](https://ja.wikipedia.org/wiki/Intel_80387 "wikilink")（[386用](../Page/Intel_80386.md "wikilink")）が最後となり、[486からは同一のチップ内に内蔵された](../Page/Intel486.md "wikilink")（486の初期には、FPUを内蔵しない廉価版と、事実上は[オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")であった[487もあった](https://ja.wikipedia.org/wiki/Intel487 "wikilink")）。同様に、モトローラの[68000系でも](../Page/MC68000.md "wikilink")[MC68040](../Page/MC68040.md "wikilink")以降はチップ内に内蔵している。プロセッサに内蔵されたFPUは[スーパースカラー](../Page/スーパースカラー.md "wikilink")で他ユニットと並列動作させることができるなど様々なメリットがあるため、現在ではFPUを単体で用いることは珍しくなっている。

## 接続の形式

### I/Oプロセッサ形式

FPUを[I/Oポートに接続して](https://ja.wikipedia.org/wiki/Input/Outputポート "wikilink")、通常の周辺機器と同様にI/Oポートを介してデータのやり取りを行なう形式。たとえばAm9511はこの形式で設計されている。FPUは周辺機器として扱われるので、CPUと同じメーカのFPUを使わなくてもよく、8ビットCPUの時代には、コストのかかるAm9511などの代わりに別メーカの電卓用CPUをI/Oポートに接続して使うことがホビイストの間で実験的に行なわれた。

また、対応機種として設計されていない組み合わせ、たとえば[モトローラ](../Page/モトローラ.md "wikilink")の[MC68881](../Page/MC68881.md "wikilink")（[MC68020](../Page/MC68020.md "wikilink")/[MC68030](../Page/MC68030.md "wikilink")用FPU）や、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[287](https://ja.wikipedia.org/wiki/Intel_80287 "wikilink")（[286用FPU](../Page/Intel_80286.md "wikilink")）を、[MC68000](../Page/MC68000.md "wikilink")や[MC68010](../Page/MC68010.md "wikilink")に接続する場合は、データの入出力をプログラム上で明示的に行わなくてはならない。そのマシンに対応した数値演算ライブラリを使用すれば、アプリケーションソフトウェアのプログラミングにおいては、FPUを使用することを意識する必要は無いが、[I/Oポートを介してデータをやり取りするため直接接続されている場合に比べて](https://ja.wikipedia.org/wiki/Input/Outputポート "wikilink")、大きなオーバヘッドが生ずる。逆に利点としては、主プロセッサと、副プロセッサの動作速度を個別に設定できるなど、自由度が高い点がある。

2018年現在では、[Graphics Processing Unit及びそれをベースにしたプロセッサを用い](../Page/Graphics_Processing_Unit.md "wikilink")、[暗号通貨](https://ja.wikipedia.org/wiki/暗号通貨 "wikilink")や各種演算処理に用いられる事が増え、グラフィックボードが品薄になる程の需要が生じている。

### コプロセッサ方式

CPUとFPUがアドレスバスとデータバスを共有し、協調して動作する方式。ユーザから見るとCPUの命令が拡張されたように見える。 [8087ではデコーダを独立して内蔵しており](../Page/Intel_8087.md "wikilink")、真の意味でコプロセッサだったが、[287以降はCPUのデコード結果を専用I](https://ja.wikipedia.org/wiki/Intel_80287 "wikilink")/Oポートを介し引き渡す方式を採った。 8086/87では次の浮動小数点命令を実行する前に、前の命令が終わるまで待つための wait 命令が必要だったが、286/287からは必要なくなっている。

[モトローラ](../Page/モトローラ.md "wikilink")の[MC68881](../Page/MC68881.md "wikilink")や[MC68882を同社](https://ja.wikipedia.org/wiki/MC68881#MC68882 "wikilink")[MC68020](../Page/MC68020.md "wikilink")または[MC68030](../Page/MC68030.md "wikilink")と組み合わせる場合、専用に用意された制御線を使用して接続すれば、ソフトウェアの変更は必要なく、[プログラマ](../Page/プログラマ.md "wikilink")からは単純にCPUの機能が拡張されたように扱える。MC68020の場合、厳密にはコプロセッサの存在を示す[フラグが立つ](../Page/フラグ_\(コンピュータ\).md "wikilink")。

### 乗っ取り形

コプロセッサ方式の発展形。コプロセッサが実際にはCPUとしての全機能を持っており、制御は完全にコプロセッサ側に渡してしまい、既存のCPUは停止させてしまう。

[487がこれで](https://ja.wikipedia.org/wiki/Intel487 "wikilink")、要するにFPUというのは名前だけで、実態は[オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")である。

## 関連項目

  - [CPU](../Page/CPU.md "wikilink")
  - [マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")
  - [オーバードライブプロセッサ](../Page/オーバードライブプロセッサ.md "wikilink")
  - [ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:コンピュータの算術](https://ja.wikipedia.org/wiki/Category:コンピュータの算術 "wikilink")