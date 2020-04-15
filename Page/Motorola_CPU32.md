> この記事は[Motorola CPU32](https://ja.wikipedia.org/wiki/Motorola_CPU32)から翻訳されています。


**Motorola CPU32**(**683xx**)は、[フリースケール・セミコンダクタ](../Page/フリースケール・セミコンダクタ.md "wikilink")によって製造された[68000ベースの](../Page/MC68000.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")コアを使った[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")の製品群である。

## 特徴

[命令セット](../Page/命令セット.md "wikilink")は[68020から](../Page/MC68020.md "wikilink")[ビットフィールド](https://ja.wikipedia.org/wiki/ビットフィールド "wikilink")命令を削除し、テーブル参照更新命令や低電力停止モードなどいくつかの命令を追加したものである。このファミリは[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")を使い[コンピュータ](../Page/コンピュータ.md "wikilink")上で[コンパイルして設計された](../Page/コンパイラ.md "wikilink")。これにより、回路を追加しやすくなり、最新の製造工程にもマッチし、[ダイ](../Page/ダイ.md "wikilink")サイズも小さくなった。

マイクロコントローラのモジュール群は個別に設計され、新しい[CPU](../Page/CPU.md "wikilink")のテストに使われた。この方式をとることにより設計者はデザイン優先で進めることができ、後に半導体技術が進歩したときに[モトローラ](../Page/モトローラ.md "wikilink")はそれらをワンチップに搭載して市場に出すことができた。これらのサブモジュールの設計は[ColdFire](../Page/ColdFire.md "wikilink")の系統に生かされている。

## 内蔵モジュール

これらのモジュールが内部[バスで接続されている](../Page/バス_\(コンピュータ\).md "wikilink")。

  - 停止状態から最高速 (25[MHz](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")/33MHz) まで動作中に[クロック](../Page/クロック.md "wikilink")周波数を変更できるCPUコア。
  - CPUコアは[トランジスタ](../Page/トランジスタ.md "wikilink")数を減らしつつ性能を向上させるよう設計された。
  - "background debug mode" (BDM) と呼ばれる高速クロック同期式シリアル[デバッガ](../Page/デバッガ.md "wikilink")用[インタフェースを備えている](../Page/インタフェース_\(情報技術\).md "wikilink")。この機能を初めて組み込んだのが683xxシリーズである。
  - SIM（システム・インタフェース・モジュール）。[アドレスを制御信号に変換することにより周辺回路を大幅に減らすことのできる](../Page/メモリアドレス.md "wikilink")[モジュール](../Page/モジュール.md "wikilink")。クロック・ジェネレータ、各種操作に使える[ウォッチドッグタイマー](../Page/ウォッチドッグタイマー.md "wikilink")、プロセッサのピン構成変更機能、[周期タイマ](https://ja.wikipedia.org/wiki/インターバルタイマ "wikilink")、[割り込みコントローラも装備](../Page/Programmable_Interrupt_Controller.md "wikilink")。

## オプション装備

以下のものがオプションとして一部のモデルに採用されている。

  - タイミング処理ユニット (TPU)：ほとんど全てのタイミング関連の処理を行う。タイマ、カウンタ、制御用パルス発生、計測用パルス発生、[ステッピングモーター](../Page/ステッピングモーター.md "wikilink")制御、直角[位相](../Page/位相.md "wikilink")検出など。フリースケール・セミコンダクタは開発システムと[ソースコード](../Page/ソースコード.md "wikilink")を無償で提供している。
  - 補助用[RAM](../Page/Random_Access_Memory.md "wikilink")：TPU用プログラム記憶領域を倍にする。
  - 初期モデルでは2つのカウンタータイマーを装備。
  - いくつかのモデルでは[ネットワーク・インターフェイス・プロセッサを装備](../Page/ネットワークカード.md "wikilink")。
  - 汎用タイマー (GPT) モジュール：パルス計数器、CCP(capture/compare/PWM)機能。
  - いくつかのモデルは通信処理モジュール (CPM) や[シリアル通信](https://ja.wikipedia.org/wiki/シリアル通信 "wikilink")コントローラー (SCC) を装備し、[イーサネット](../Page/イーサネット.md "wikilink")や[HDLC](https://ja.wikipedia.org/wiki/HDLC "wikilink")をサポートしている。
  - 多くのモデルはキュー付シリアルモジュール (QSM) を装備。クロック同期式[SPIバス](https://ja.wikipedia.org/wiki/SPIバス "wikilink")とロジックレベルの[RS-232](../Page/RS-232.md "wikilink")C・[UART](../Page/UART.md "wikilink")機能をサポートしている。

[Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink")