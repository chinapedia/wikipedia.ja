> この記事は[Power On Self Test](https://ja.wikipedia.org/wiki/Power_On_Self_Test)から翻訳されています。


**Power On Self Test**（**POST**）とは、[コンピュータ](../Page/コンピュータ.md "wikilink")や[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")、[ルーター](../Page/ルーター.md "wikilink")などの電源を入れたとき[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")の前に行われる処理を指す。用語は違っても、同様のシーケンスは全てのコンピュータアーキテクチャに存在する。IPL（Initial Program Load）、[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")、ブートストラップなどと呼ばれる処理の前に行われる。POST という用語は[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")で使われ、一般化した。ブート前の処理を行うコードを指すこともあるし、処理そのものを指すこともある。

## 一般的な処理の流れ

電源を入れると、POST は [BIOS](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink") によって制御され、さらにビデオや[SCSIなどの](../Page/Small_Computer_System_Interface.md "wikilink")[周辺機器](../Page/周辺機器.md "wikilink")の初期化はそれ専用のプログラムが分担する。そのような特定機能を分担するプログラムは、ビデオBIOS、SCSI BIOS などと呼ばれ、全体として[オプションROMなどと呼ばれる](https://ja.wikipedia.org/wiki/:en:Option_ROM "wikilink")。

BIOS が POST 実行中に行う処理は次のようになる。

1.  BIOSコード自体が問題ないかチェックする。
2.  POST を実行する契機が何なのかを特定する。
3.  システムの[メインメモリを探し](../Page/主記憶装置.md "wikilink")、大きさを調べ、問題ないか検証する。
4.  全ての[フロントサイドバス](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")とデバイスを検出し、初期化し、登録する。
5.  必要ならば、個別のBIOS群に制御を渡す。
6.  システム設定のための[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を提供する。
7.  ブート可能なデバイスを特定し、選択する。
8.  対象[OSが必要とするシステム環境があれば](../Page/オペレーティングシステム.md "wikilink")、それを構築する。

BIOS は、[CPU](../Page/CPU.md "wikilink")がリセットされたときにPOSTを起動する。CPUがリセット後に最初に実行しようとするメモリ位置をリセットベクタと呼ぶ。[ハードリブートの場合](https://ja.wikipedia.org/wiki/ブート "wikilink")、[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")がそのコードフェッチ要求をBIOSのあるシステム[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")に向けさせる。[ウォームブートでは](https://ja.wikipedia.org/wiki/ブート "wikilink")、BIOSは[RAM内の適切な位置に置かれているので](https://ja.wikipedia.org/wiki/ランダムアクセスメモリ "wikilink")、ノースブリッジはそのRAM上の位置にリセットベクターを向けさせる。

最近のBIOSでは、POST実行で最初に何故起動されたのかを特定しなければならない。例えばコールドブートなら、全機能を実施しなければならないだろう。しかし、システムが電力節約モードやクイックブートといったものをサポートしている場合、BIOS は標準の POST におけるデバイス検出工程をしなくて済み、既にあるシステムデバイステーブルを使ってデバイスを設定できる。

POST の処理は本来は非常に単純だったが、PCの発展と共に複雑化してきた。POST 実施中、BIOS はハードウェアやOSがサポートすることを期待されている様々な（そして時に相互に排他的な）各種標準規格を考慮しなければならない。しかし、ユーザーから見える POST と BIOS は、従来とほとんど変わらないメモリテスト画面と設定画面でしかない。

## 基本構造

[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")の場合、主BIOSは二つの部分に分けられる。POST部分（POSTコード）は上述の処理を行い、POSTがOSのために構築する環境がいわゆるランタイムBIOS（ランタイムコード）である。基本的にPOSTコードは役目が終わると、OSに制御が渡される前にメインメモリ上から消されるが、ランタイムコードはメモリに常駐する。このような分け方は単純化しすぎかもしれないが、もちろんPOST処理中にもランタイムコードが使われる。

## エラー通知法

[thumb](https://ja.wikipedia.org/wiki/ファイル:BIOS_POST_card.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:POST_card_3usd.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:POST_card_98usd.jpg "wikilink") 本来の IBM BIOS は POST 処理中にエラーを検出すると、固定の[I/Oポートアドレス](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink") 80 にエラーを示す番号を出力する。[ロジックアナライザ](../Page/ロジックアナライザ.md "wikilink")を使うか、専用の POST カード（ポート 80 の内容を表示するためのカード）を使うと、問題がどこにあるのかが分かる。表示器を搭載したマザーボードもある。なお、OSが動作している間は、そのI/Oポートを監視しても無意味である。例えば [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") はポート80をI/Oタイミングの調整に使用する。その後、BIOS ベンダー各社はマザーボード上にあるスピーカーを使って、一連の[ビープ音](https://ja.wikipedia.org/wiki/ビープ音 "wikilink")でエラーを通知するようになった。

### 本来の IBM POST エラーコード

  - 短いビープ音1回 - Normal POST - システムは正常
  - 短いビープ音2回 - POST error - エラーコードは画面表示される
  - ビープ音なし - [電源](../Page/電源回路.md "wikilink")、[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")の問題。あるいは、スピーカーが故障している。
  - 連続的なビープ音 - 電源、マザーボード、[キーボードの問題](https://ja.wikipedia.org/wiki/キーボード_\(コンピュータ\) "wikilink")
  - 短いビープ音の繰り返し - 電源、マザーボード、キーボードのいずれかの問題
  - 長いビープ音1回と短いビープ音1回 - マザーボードの問題
  - 長いビープ音1回と短いビープ音2回 - [ビデオカード](../Page/ビデオカード.md "wikilink")（MDA、CGA）の問題
  - 長いビープ音1回と短いビープ音3回 - [EGA](../Page/Enhanced_Graphics_Adapter.md "wikilink") の問題
  - 長いビープ音3回 - 3270 キーボード・カードの問題

### POST AMI BIOS ビープコード

  - 1回 - メモリリフレッシュ・タイマのエラー
  - 2回 - ベースメモリ（先頭の64KB）での[パリティエラー](https://ja.wikipedia.org/wiki/パリティビット "wikilink")
  - 3回 - ベースメモリのリード/ライト・テストでのエラー
  - 4回 - [マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")のタイマが操作不能
  - 5回 - プロセッサのエラー
  - 6回 - 8042 ゲートの A20 テスト・エラー（プロテクトモードに移行できない）
  - 7回 - 一般例外エラー（プロセッサ例外割り込みエラー）
  - 8回 - 表示用メモリのエラー（システムのビデオアダプタ）
  - 9回 - AMI BIOS ROM [チェックサム](../Page/チェックサム.md "wikilink")エラー
  - 10回 - CMOS シャットダウンレジスタの読み書きエラー
  - 11回 - [キャッシュメモリ](../Page/キャッシュメモリ.md "wikilink")テストでのエラー

出典: [AMIBIOS8 Check Point and Beep Code List](http://www.ami.com/support/doc/AMIBIOS8_Checkpoint_and_Beep_Code_List_PUB.pdf), version 1.9, [2007年](../Page/2007年.md "wikilink")[10月11日](../Page/10月11日.md "wikilink")更新

### コンプティア A+ Core Hardware 試験での POST ビープコード

[コンプティア](https://ja.wikipedia.org/wiki/コンプティア "wikilink")の実施する A+ Core Hardware 試験で特に出てくる POST ビープコードは以下の通り。

| ビープ音              | 意味                                          |
| ----------------- | ------------------------------------------- |
| 一定の短いビープ音         | 電源が故障していると思われる                              |
| 長い連続したビープ音        | 電源故障か電源とマザーボードのコネクタがしっかりはまっていない。            |
| 一定の長いビープ音         | 電源故障                                        |
| ビープ音なし            | 電源故障、あるいは電源が入っていない。                         |
| ビープ音なし            | どこにも問題がないようなら、ビープ音を発生する機構（スピーカー周辺）自体に問題がある。 |
| 長いビープ音1回と短いビープ音2回 | ビデオカード故障                                    |

### IBM POST 診断コード

  - 100 から 199 まで - マザーボード
  - 200 から 299 まで - メモリ
  - 300 から 399 まで - キーボード
  - 400 から 499 まで - モノクロ・ディスプレイ
  - 500 から 599 まで - カラー/グラフィックス・ディスプレイ
  - 600 から 699 まで - フロッピーディスクドライブかそのアダプタ
  - 700 から 799 まで - [FPU](../Page/FPU.md "wikilink")
  - 900 から 999 まで - パラレル・プリンタポート
  - 1000 から 1099 まで - 追加プリンタポート
  - 1100 から 1299 まで - 非同期通信デバイス、アダプタ、ポート
  - 1300 から 1399 まで - ゲームポート
  - 1400 から 1499 まで - カラー/グラフィックス・プリンター
  - 1500 から 1599 まで - 同期通信デバイス、アダプタ、ポート
  - 1700 から 1799 まで - ハードディスクドライブ、アダプタ
  - 1800 から 1899 まで - 拡張装置 (XT)
  - 2000 から 2199 まで - BSC 通信アダプタ
  - 2400 から 2599 まで - EGA ビデオ (MCA)
  - 3000 から 3199 まで - LANアダプタ
  - 4800 から 4999 まで - 内蔵モデム
  - 7000 から 7099 まで - Phoenix BIOS チップ
  - 7300 から 7399 まで - 3.5インチ・フロッピーディスクドライブ
  - 8900 から 8999 まで - MIDIアダプタ
  - 11200 から 11299 まで - SCSIアダプタ
  - 21000 から 21099 まで - SCSI固定ディスクとコントローラ
  - 21500 から 21599 まで - SCSI CD-ROM ドライブ

## Macintosh の POST

[アップルの](../Page/アップル_\(企業\).md "wikilink") [Macintosh](../Page/Macintosh.md "wikilink") にもコールドブート時のPOST処理がある。致命的なエラーが発生すると、Macintosh ではチャイム音が鳴らない。

### 1998年まで

1998年までに製造された Macintosh では、POST 処理が失敗すると「死のチャイム」と呼ばれる音とともに停止する（音そのものは機種によって異なり、ビープ音だったり、車が衝突する音だったり、ガラスが割れる音だったり、音楽だったりする）。画面には泣き顔の Macintosh のアイコンが表示され、16進の文字列が2行表示され、それが問題特定の手掛かりとなる。

### 1998年から1999年

1998年に登場した [iMac](https://ja.wikipedia.org/wiki/iMac "wikilink") では、それまでとは大幅な変更が加えられた。初期化時に致命的なエラーが発生すると、以下のようなビープ音が発せられる[1](http://docs.info.apple.com/article.html?artnum=58183)。

  -
    ビープ音1回 - RAMを検出できない
    ビープ音2回 - RAMの種類が非互換（例えば EDORAM）
    ビープ音3回 - RAMのメモリテストが全て失敗
    ビープ音4回 - ブートROMの残りの部分のチェックサムエラー
    ビープ音5回 - ブートROMのブート機能部分のチェックサムエラー

### 1999年以降

上記ビープコードは、1999年10月に変更された[2](http://docs.info.apple.com/article.html?artnum=58442)。さらに、機種によっては同時に電源LEDが点滅する。

  -
    ビープ音1回 - RAMが検出できない
    ビープ音2回 - RAMの種類が非互換
    ビープ音3回 - RAMのメモリテストが全て失敗
    ビープ音4回 - ブートROMのブートイメージが不正（あるいは sys config ブロックが不正）
    ビープ音5回 - プロセッサ故障

## 関連項目

  - [ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")

## 外部リンク

  - [AwardBios Version 4.51PG - POST Codes and Error Messages](http://www.phoenix.com/NR/rdonlyres/320A0046-F6B2-41F8-8DEE-1CD7D4B78F12/0/biosawardpostcode.pdf)
  - [PhoenixBIOS 4.0 - Revision 6.0 POST Tasks and Beep Codes](http://www.phoenix.com/NR/rdonlyres/81E6C43C-93BD-4097-A9C4-62F05AAD6025/0/biospostcode.pdf)
  - [Power On Self Test Beep Codes for AMI and Phoenix BIOS](http://www.pchell.com/hardware/beepcodes.shtml) - from PC Hell.
  - [Computer Hardware - Additional information on computer POST / Beep Codes](http://www.computerhope.com/beep.htm) - from Computer Hope.
  - [Hardware Diagnostics](http://www.eventhelix.com/RealtimeMantra/FaultHandling/hardware_diagnostics.htm)
  - [BIOS Beep codes and their meaning](http://www.pctechbytes.com/bios.htm) - from PCTechBytes.
  - [basicinputoutputsystem.com](http://www.basicinputoutputsystem.com/) - BIOSについて

[Category:ファームウェア](https://ja.wikipedia.org/wiki/Category:ファームウェア "wikilink") [Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink") [Category:コンピュータの仕組み](https://ja.wikipedia.org/wiki/Category:コンピュータの仕組み "wikilink") [Category:BIOS](https://ja.wikipedia.org/wiki/Category:BIOS "wikilink")