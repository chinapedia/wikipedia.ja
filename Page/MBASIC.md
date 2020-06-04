> この記事は[MBASIC](https://ja.wikipedia.org/wiki/MBASIC)から翻訳されています。


**MBASIC**（エムベーシック）は、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")向けの[Microsoft BASICである](../Page/Microsoft_BASIC.md "wikilink")。MBASICは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の最初の製品である[Altair BASICインタプリタの子孫である](../Page/Altair_BASIC.md "wikilink")。MBASICは、[Osborne 1に同梱されていた](../Page/Osborne_1.md "wikilink")2つのバージョンのBASICのうちの1つである。「MBASIC」という名前は、BASICインタプリタのディスクファイル名 MBASIC.COM に由来する。

## 動作環境

[MBasic_5.21.jpg](https://ja.wikipedia.org/wiki/File:MBasic_5.21.jpg "fig:MBasic_5.21.jpg")

MBASIC バージョン5では、最低28 kB の[RAMと最低](../Page/Random_Access_Memory.md "wikilink")1台のディスクドライブを備えたCP/Mシステムが必要だった。

[ホームコンピュータ](https://ja.wikipedia.org/wiki/ホームコンピュータ "wikilink")メーカーがそのコンピュータ固有のハードウェア機能を使用するためにカスタマイズしたMicrosoft BASIC-80とは異なり、MBASICは全ての入出力をCP/Mの[システムコール](../Page/システムコール.md "wikilink")のみに依存していた。使用可能なのはCP/Mのコンソール（スクリーンとキーボード）、ラインプリンタ、ディスクデバイスのみだった。

カスタマイズされていない状態のMBASICには、[グラフィックス](../Page/コンピュータグラフィックス.md "wikilink")、カラー、ジョイスティック、マウス、[シリアル通信](../Page/シリアルポート.md "wikilink")、[ネットワーク](../Page/イーサネット.md "wikilink")、サウンド、リアルタイムクロックなどの機能はなかった。MBASICはホストのCP/Mの機能に完全には対応していなかった。例えば、フロッピーディスク上のファイルを整理するためのCP/Mのユーザ領域に対応していなかった。CP/Mシステムは一般的にシングルユーザでスタンドアローンであったため、ファイルやレコードのロックや、いかなる形態の[マルチタスク](../Page/マルチタスク.md "wikilink")にも対応していなかった。これらの制限を除けば、MBASICは、当時、BASICの強力で有用な実装であると考えられていた。

## 機能

### 言語システム

MBASICは[インタプリタ](../Page/インタプリタ.md "wikilink")である。プログラムのソースは[トークン化された形でメモリに格納され](../Page/バイトコード.md "wikilink")、BASICのキーワードを1バイトのトークンに置き換えることで、メモリ容量を節約し、実行を高速化した。[行番号](../Page/行番号.md "wikilink")を先頭に書いた行はプログラムテキストとして保存され、行番号を先頭に書かないBASIC文はコマンドとして直ちに実行される。プログラムは編集のために画面に表示したり、圧縮されたバイナリ形式またはプレーンなASCIIテキストとしてディスクに保存したりすることができた。ソースの各行は行番号で識別され、[GOTOや](https://ja.wikipedia.org/wiki/goto文 "wikilink")[GOSUBの転送先として使用することができる](../Page/サブルーチン.md "wikilink")。ソースの編集には行編集コマンドのみが提供されていた\[1\]。プログラムをプレーンテキストとして保存し、フル機能の[テキストエディタ](../Page/テキストエディタ.md "wikilink")で編集することがしばしば行われた。

プログラムテキスト、変数、ディスクバッファ、そしてオペレーティングシステム(CP/M)自体も、全て[Intel 8080プロセッサの](../Page/Intel_8080.md "wikilink")64キロバイトのアドレス空間を共有しなければならなかった。通常、MBASICを最初に起動したときには、64キロバイトのRAMを搭載したマシンであっても、プログラムやデータに使用できるメモリは32キロバイト以下になる。`REM`キーワードや[アポストロフィ](https://ja.wikipedia.org/wiki/アポストロフィ "wikilink")を先頭にした[コメント行をプログラムのテキストに配置することがはできたが](../Page/コメント_\(コンピュータ\).md "wikilink")、貴重なメモリスペースを占有してしまうため、ユーザがコメントをあまり残さないようになった。より大きく複雑なプログラムを実行できるようにするために、MBASICの後のバージョンでは、プログラムテキストの一部を読み込んでプログラム制御下で実行できるようにする関数が追加された（や`MERGE`文）。"shell"コマンドの実行には対応していなかったが、この機能はプログラマによって複製することができた。

MBASICの特に優れた点は、シンタックスエラーやランタイムエラーのようなエラーメッセージが全文表示されることだった。MBASICには、実行時に行番号を表示する"trace"機能もあった。これは通常のプログラム出力と同じ画面スペースを占有するが、[無限ループ](../Page/無限ループ.md "wikilink")のような状態を検出するのに役立った。

### ファイルと入出力

データは、シーケンシャルファイル（CP/Mの規約により、各行の最後がCRLFで区切られている）として、または固定レコード長のランダムアクセスファイルとして、ディスクへの読み取り・保存ができ、十分な能力を持ったプログラマであれば、データベースタイプのレコード操作に使用することができる。

[浮動小数点数](../Page/浮動小数点数.md "wikilink")のためのは、その実装が[プロプライエタリなものであった](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。すなわち、浮動小数点数のデータを他のプログラムとの間で交換する場合は、ASCIIテキスト表現を使用するか、バイナリフォーマットを変換するための大規模なプログラミングが必要であった。

### 変数とデータ型

MBASICには以下のデータ型があった。

  - 8ビット 文字列データ。文字列長は0から255文字。
  - 16ビット [整数](../Page/整数型.md "wikilink")
  - 32ビット [浮動小数点数](../Page/浮動小数点数.md "wikilink")（[単精度](../Page/単精度浮動小数点数.md "wikilink")）
  - 64ビット 浮動小数点数（[倍精度](../Page/倍精度浮動小数点数.md "wikilink")）

文字列演算子には、部分文字列の選択、連結、代入、文字列が等しいかどうかのテストなどがある。

上記のデータ型の[配列](../Page/配列.md "wikilink")は7次元まで使用できる。関数や演算子は配列では動作しない。例えば、配列の代入はできない。当時の他のBASICの実装とは異なり、MBASICは[行列](https://ja.wikipedia.org/wiki/行列 "wikilink")演算、[複素数](../Page/複素数.md "wikilink")、金融計算用の[十進数(BCD)データ型に対応していない](../Page/二進化十進表現.md "wikilink")。典型的なCP/Mシステムには[浮動小数点演算ハードウェアがなかったため](../Page/FPU.md "wikilink")、浮動小数点演算は全てソフトウェアで行われた。内蔵の数学関数（[三角関数](../Page/三角関数.md "wikilink")、[対数](../Page/対数.md "wikilink")、[指数](https://ja.wikipedia.org/wiki/指数 "wikilink")、[平方根](../Page/平方根.md "wikilink")）は単精度の結果しか得られなかった。ソフトウェアによる[疑似乱数発生器が提供されていた](../Page/擬似乱数.md "wikilink")。これは、ユーザが入力したシード値から、ゲームやシミュレーションに有用な数列を得るものである。MBASICには代入文のための`LET`キーワードがあったが、なくても代入できた。

マイクロコンピュータにおけるのBASICの初期のバージョンでは、1文字または2文字の変数名しか使用できず、複雑なプログラムでは変数の意味を思い出すのが困難となった。MBASICバージョン5では、40文字までの識別子を使用できるようになり、プログラマは変数に読みやすい名前を付けることができるようになった。

### 制御構造

MBASICの[制御構造](../Page/制御構造.md "wikilink")には、条件判定の[`IF...THEN...ELSE...`](https://ja.wikipedia.org/wiki/if文 "wikilink")、[`WHILE...WEND`](https://ja.wikipedia.org/wiki/while文 "wikilink")ループ、[`GOTO`](https://ja.wikipedia.org/wiki/goto文 "wikilink")、`GOSUB`があった。[`CASE`](https://ja.wikipedia.org/wiki/switch文 "wikilink")はなかったが、`ON...GOTO...`による多方向分岐があった。[サブルーチン](../Page/サブルーチン.md "wikilink")には引数がなく、全ての変数はグローバル変数だった。MBASICは[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")を必須としていなかったので、容易に[スパゲッティコード](https://ja.wikipedia.org/wiki/スパゲッティコード "wikilink")となってしまった。

## PEEK、POKE、ユーザ関数

1970年代後半から1980年代前半の8ビットコンピュータのBASICについての議論は、メモリへの直接読み書きのためのの重要性への言及が不可欠である。これらのシステムには通常、[メモリ保護](../Page/メモリ保護.md "wikilink")機能がなかったため、プログラマはOSの一部の通常の方法では利用できない機能にアクセスすることができた。これにより、ユーザプログラムによってシステムがハングアップする可能性も高くなった。例えば、CP/Mプログラマは、（システムBIOSが対応していれば）BASIC がコンソールデバイスをシリアルポートに切り替えるために`POKE`関数を使用した。[リアルタイムクロック](../Page/リアルタイムクロック.md "wikilink")を持つマシンでは、時刻を取得するために`PEEK`命令を使用していた。

より複雑な操作のために、MBASICはBASICプログラムから呼び出すことができるユーザ定義の関数を仕様できるようにした。これは通常メモリの予約領域に配置されたり、一連の[機械語](../Page/機械語.md "wikilink")コード（オペコード）として文字列定数にPOKEされたりする。また、MBASICには、8080のハードウェア入出力ポートに直接読み書きする`INP`命令と`OUT`命令もある。少なくとも[Osborne 1では](../Page/Osborne_1.md "wikilink")、全てのI/O命令はシステムで使用するために[プリエンプション](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")されていたが、この命令は周辺機器を制御するために使用することができる。

`PEEK`や`POKE`、機械語のユーザ関数を利用したMBASICプログラムは、そのままでは異なる機種間の移植性がなかった。

## MBASICの後継

CP/M用のMicrosof BASIC-80の他に、用のMBASICもあった。

[MSX-BASIC](../Page/MSX-BASIC.md "wikilink")もまたMBASICの後継として知られており、[MSX](https://ja.wikipedia.org/wiki/MSX "wikilink")に特化したいくつかの拡張機能を備えている。

CP/M用MBASIC の全ての機能は、[IBM PCの](../Page/IBM_PC.md "wikilink")やで利用可能であり、CP/Mシステムから[IBM PC互換機へのプログラムの移行が可能だった](https://ja.wikipedia.org/wiki/IBM_PC互換機 "wikilink")。キーワードを表すために使用されるトークンが異なるため、移植のためにはCP/MプログラムはASCIIソース形式で保存されなければならなかった。

## BASCOM

マイクロソフトは、MBASICと同様のソース言語を使用するCP/M BASIC[コンパイラ](../Page/コンパイラ.md "wikilink")・**BASCOM**を販売した。MBASICで[デバッグ](../Page/デバッグ.md "wikilink")されたプログラムはBASCOMでコンパイルすることができた。プログラムのテキストがメモリに残らず、コンパイラのランタイム要素がインタプリタよりも小さかったため、ユーザデータに使用できるメモリが増えた。また、実際のプログラム実行速度は約3倍に向上した。

開発者たちは、人気はあったが遅くてぎこちないの代替としてBASCOMを歓迎した。CBASICとは異なり、BASCOMはMBASICソースコードのための[プリプロセッサ](../Page/プリプロセッサ.md "wikilink")を必要としなかったので、対話的にデバッグすることができた\[2\]。ただし、マイクロソフトは、BASCOMでコンパイルしたプログラムのコピーを1つ配布するごとに9%の[ロイヤルティー](../Page/ロイヤルティー.md "wikilink")を要求し\[3\]、ハードウェアとソフトウェアの組み合わせには40ドルを要求した。また、マイクロソフトは開発者の財務記録を監査する権利を持っていた。ソフトウェアの著作者のロイヤルティー率は一般的には10-25%だったので、『』誌は1980年に、BASCOMを使用することによる9%のロイヤルティーの上乗せは「ソフトウェア開発を収益性の低いものにする可能性がある」と述べ、「マイクロソフトには（CBASICに対抗する）技術的な解決策はあるが、経済的な解決策はない」と結論づけた\[4\]。

## MBASICの重要性

MBASICは8ビットのCP/Mコンピュータの時代には重要なツールだった。熟練したユーザは、現代のシステムならば強力なアプリケーションプログラムのコマンドやスクリプト言語によって実行されるであろうタスクを自動化するために、MBASICでルーチンを書くことができた。便利なMBASICプログラムの交換は、コンピュータの[ユーザーグループ](https://ja.wikipedia.org/wiki/ユーザーグループ "wikilink")の機能の1つだった。雑誌の記事に掲載された長いBASICのプログラムリストをキー入力することは、新しいCP/Mシステムにソフトウェアを「ブートストラップ」（インストール）"する一つの方法だった。大規模な高レベル言語用のコンパイラがMBASICで書かれ、数行から数千行のコードまでの小さなゲームやユーティリティプログラムが数多く書かれていた。

## その他

Basic Micro, Inc.が開発した[マイクロチップ・テクノロジー](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink")の[PICファミリー用の商用BASICコンパイラの名称もMBASICであるが](../Page/PIC_\(コントローラ\).md "wikilink")、本項目で説明したCP/M用BASICインタプリタとは無関係である。

## 脚注

  - Thom Hogan and Mike Iannamico, *Osborne 1 User's Reference Guide*,(1982) Osborne Computer Corporation
  - David A. Lien, *The BASIC Handbook*, 2nd Edition Encyclopedia of the BASIC Computer Language",(1981), Compusoft Publishing
  - *BASIC 80 Reference Manual*, Microsoft Corporation, no date

[Category:CP/M](https://ja.wikipedia.org/wiki/Category:CP/M "wikilink") [Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.  フルスクリーン編集を行えるCP/M製品は、システムコンソールとして使用される特定の[端末](../Page/端末.md "wikilink")用にソフトウェアをカスタマイズするために、独自のインストールルーチンを必要としていた。CP/M内では、端末の機能を標準化する機能は提供されていなかった。
2.
3.
4.