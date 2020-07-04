> この記事は[PIC \(コントローラ\)](https://ja.wikipedia.org/wiki/PIC_\(コントローラ\))から翻訳されています。


**PIC**（ピック、Peripheral Interface Controller）とは、[マイクロチップ・テクノロジー](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink")社 (Microchip Technology Inc.) が製造している[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")（制御用IC）製品群の総称である。

## 概要

[コンピュータ](../Page/コンピュータ.md "wikilink")の周辺機器接続の制御用として[1975年](../Page/1975年.md "wikilink")に[ジェネラル・インストゥルメント](https://ja.wikipedia.org/wiki/ジェネラル・インストゥルメント "wikilink") (General Instrument Corporation) 社により開発された。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")にPICの事業部門が独立してマイクロチップ社となり現在に至る。

PICには[CPU](../Page/CPU.md "wikilink")、[メモリ](../Page/記憶装置.md "wikilink") ([RAM](../Page/Random_Access_Memory.md "wikilink"), [ROM](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink"))、[I/Oなどが](../Page/入出力.md "wikilink")1[チップ](../Page/チップ.md "wikilink")に収められており、ROMに書き込まれた[プログラムにより](../Page/プログラム_\(コンピュータ\).md "wikilink")[制御](https://ja.wikipedia.org/wiki/制御 "wikilink")される。[回路](https://ja.wikipedia.org/wiki/回路 "wikilink")構成が容易かつ安価で、他のマイクロコントローラと比べて圧倒的に[インターネット](../Page/インターネット.md "wikilink")上で情報を得やすく、関連書籍も豊富で、PICそのものの入手性も良いため[電子工作](../Page/電子工作.md "wikilink")愛好家の間で人気がある。 [Pic32mz2048ecm100-ipt.jpg](https://ja.wikipedia.org/wiki/File:Pic32mz2048ecm100-ipt.jpg "fig:Pic32mz2048ecm100-ipt.jpg") [Pic24fj64gb002-isp.JPG](https://ja.wikipedia.org/wiki/File:Pic24fj64gb002-isp.JPG "fig:Pic24fj64gb002-isp.JPG")

## 特徴

命令語長を揃え命令数を抑えた[RISC](../Page/RISC.md "wikilink")ライクな[構造になっているほか](../Page/コンピュータ・アーキテクチャ.md "wikilink")、コードエリアとデータエリアが分離された[ハーバード・アーキテクチャ](../Page/ハーバード・アーキテクチャ.md "wikilink")をとり、コードエリアとデータエリアとでバス幅をそれぞれ最適化しているのが特徴である。「ビットコア」とはコードメモリの1命令の[ビット](../Page/ビット.md "wikilink")数を指す。たとえば命令長12ビットコアの場合はコードエリアのバス幅は12ビット・データエリアのバス幅は[8ビット](../Page/8ビット.md "wikilink")となっている。またコード・データそれぞれのアドレス空間も必要十分なサイズに抑えられている。

大半の命令が1サイクルで実行されるが、シリーズにより1サイクルあたりの[クロック](../Page/クロック.md "wikilink")は異なる。8ビット系PIC (PIC10/12/16/18系) は4クロックが1サイクル、PIC24/dsPIC系は2クロックが1サイクル、[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")コアのPIC32系は1クロックが1サイクルである。

大多数の品種で、動作用のクロック発振回路を内蔵しており単独で動作することが可能だが、高精度を要する場合のために外付けの水晶等を使用する発振回路も内蔵し、また外部オシレータからのクロック入力による動作も可能になっている。

プログラムコード用の内蔵メモリとしては、古くはワンタイムROM、[EPROM](../Page/EPROM.md "wikilink")（紫外線消去）品があったが、現在では大多数が[フラッシュROM品となっている](../Page/フラッシュメモリ.md "wikilink")。 多くの品種で、不揮発性のデータ保存用としてEEPROMが内蔵されている。

[バスは多くの品種で外部に出力されていないが](../Page/バス_\(コンピュータ\).md "wikilink")、PIC18シリーズの多ピン（100ピン等）の品種などでは外部バスが用意されているものもある。

パッケージは長方形の[DIPタイプから小型の](https://ja.wikipedia.org/wiki/パッケージ_\(電子部品\)#DIP_\(Dual_Inline_Package\) "wikilink")[表面実装](https://ja.wikipedia.org/wiki/表面実装 "wikilink")タイプのものまでさまざま豊富な形態で供給されている。ピン数のバリエーションも豊富で、下は6ピンのもの（俗に米粒PICと呼ばれる）から存在する。[GPIO](https://ja.wikipedia.org/wiki/GPIO "wikilink")ポートのほか、[タイマや](../Page/タイマー.md "wikilink")[A/Dコンバータなどを内蔵するもの](../Page/アナログ-デジタル変換回路.md "wikilink")、シリアルコントローラ ([USART](../Page/UART.md "wikilink"), [IIC](https://ja.wikipedia.org/wiki/I²C "wikilink")) や[USBコントローラを内蔵している製品もある](../Page/ユニバーサル・シリアル・バス.md "wikilink")。

多くの品種で[GPIO](https://ja.wikipedia.org/wiki/GPIO "wikilink")ポートには1ピンあたり25mAまで流せる出力回路が採用されており、LED等を直接駆動することができる。ただし1ポート及び1素子当たりの合計の出力電流には制限がある。

なおPICの開発元であるMicrochip社は、ディスコン（廃盤、生産停止）にしない事を会社の方針としており、古いチップも入手可能である。 そのため、設計の古いものや機能の劣るものも存在し、そのことが他社との比較において誤解され、性能的に不利であるという誤った解釈をされる理由ともなっている。 一方で、存在する過去の使用例や作例の蓄積が時間を経た現在でも有効に活用できるというメリットは大きく、チップが入手できないために見つけた作例が実際には生かせないというケースはまれである。

開発環境は、Microchipからは、古くは[アセンブラ](https://ja.wikipedia.org/wiki/アセンブラ "wikilink")のみが無償で提供されていたが、現在ではMPLAB Xという[統合開発環境](../Page/統合開発環境.md "wikilink")とCコンパイラ (XC) が無償で配布されている（無償版では最適化などに機能制限があるもののコードサイズ制限などはない）。MPLAB X は NetBeans IDEをベースにしている。 もちろん現在でもアセンブラも利用可能であり、[サードパーティー](../Page/サードパーティー.md "wikilink")製の開発環境も古くから何種類か発売されている。

PIC内蔵のプログラムメモリに書き込みを行うためのライタは、初期のものはDIPのゼロプレッシャソケットを備え、PICチップをライタに装着して書き込むものが一般的であったが、現在ではMicrochipから廉価な純正ライタのPICKitシリーズが発売されているのでこちらを用いるのが一般的となっている。PICKitを使用した書き込みは、回路上に用意した5ピンのICSP (In-Cirtuit-Serial-Programming) コネクタ経由で行うため、いちいち基板からPICを着脱する必要がない（ということはソケットを使わない表面実装タイプのPICの場合でも使用できる）。またPICKitは書き込みのみならずICD (In-Circuit-Debug) 対応の品種であればデバッガとしても使用できる（ただし小ピン品種でICDをサポートしているPICはあまり無い）。

日本では、電子工作雑誌で紹介されたり、[秋葉原](https://ja.wikipedia.org/wiki/秋葉原 "wikilink")などにある電子パーツ店では独自に企画したライタなどのキットが販売され、PICチップやライタ、開発環境が入手しやすいため普及した。また1995年ごろから、ソニー [PlayStationのCD](../Page/PlayStation_\(ゲーム機\).md "wikilink")-ROMコピープロテクトを、ハードウェアに細工して回避する手段が流行した。このための追加部品を通称[MODチップ](https://ja.wikipedia.org/wiki/MODチップ "wikilink")というが、これにはPIC12C508等がよく使用された。アンダーグラウンドでは数千円で売られていたMODチップが、自分でPICにプログラムを書き込めば数百円で作れるため、これを糸口として普及が進んだ側面もある。

PICマイクロコンピュータの入手性は他のマイクロコンピュータと比べて格段に良く、特にDIPパッケージと呼ばれる扱いやすいパッケージの豊富さから、日本でのアマチュア電子工作においてはゆるぎない人気を維持している。PICは電子部品を扱う複数の会社がキットで提供しているため、電子工作でよく使われている。今まで専用のLSIやICなどで構成されていた回路をPICに置き換えている電子工作キットなどもある。

近年では後発の[Atmel AVRマイコンとそれを利用した](../Page/Atmel_AVR.md "wikilink")[Arduino](https://ja.wikipedia.org/wiki/Arduino "wikilink")や、[ARMアーキテクチャ](../Page/ARMアーキテクチャ.md "wikilink")を採用した[32ビット](../Page/32ビット.md "wikilink")級マイクロコントローラが台頭しているなど、ライバルも多い。（なお[Atmel](https://ja.wikipedia.org/wiki/Atmel "wikilink")社は2016年1月、Microchip社に買収された）。

PICは（特に初期の12ビットコア・14ビットコアは）制限が多くプログラミングしにくいアーキテクチャであったが、その後、高級言語（[C言語](../Page/C言語.md "wikilink")）でも扱いやすくなるような機能拡張が行われたシリーズも増えている。

## 機能

すべてのPICに搭載されている機能（\*の付いた副機能のみ非搭載機種もある）

  - [発振回路](../Page/発振回路.md "wikilink")
      - 外部発振回路
          - [水晶振動子](../Page/水晶振動子.md "wikilink")発振
          - 外部からクロックを供給
          - RC発振\*
      - 内部発振回路\*（[RC発振回路](https://ja.wikipedia.org/wiki/RC回路 "wikilink")・4-16MHz程度）
      - 高精度（誤差±1-5%程度）内部発振回路\* （品種によっては工場出荷時に校正値がプログラムフラッシュの特定アドレスに書き込まれているため、これを消去してしまわないよう注意が必要）
      - PLL回路（クロックソースを3逓倍あるいは4逓倍できる）\*
  - [リセット](../Page/リセット.md "wikilink")（プログラムの先頭に戻る）
      - RESET端子によるもの
      - [ウォッチドッグタイマ(WDT)](../Page/ウォッチドッグタイマー.md "wikilink")\*によるもの
  - [割り込み](../Page/割り込み_\(コンピュータ\).md "wikilink")
      - 外部割込み
          - ピン変化\*
          - INTピン
      - 内部割込み
          - AD変換完了\*
          - [EEPROM](../Page/EEPROM.md "wikilink")にライト完了\*
          - タイマのオーバーフロー（桁あふれ）
  - [スリープ](https://ja.wikipedia.org/wiki/スリープ_\(コンピュータ\) "wikilink")（動作を停止し低消費電力となる）

一部品種に搭載されている機能

  - CCP機能（キャプチャ、コンペア、PWMの頭文字）
      - キャプチャ
      - コンペア
      - [PWM](../Page/パルス幅変調.md "wikilink")（オンとオフの割合でモーターの速度制御やLEDの明るさ制御ができる）
  - [タイマー](../Page/タイマー.md "wikilink")（カウントアップ）
  - [AD変換](https://ja.wikipedia.org/wiki/AD変換 "wikilink")（アナログ→デジタル変換）
  - [DA変換](https://ja.wikipedia.org/wiki/DA変換 "wikilink")（デジタル→アナログ変換）
  - [コンパレータ](../Page/コンパレータ.md "wikilink")（比較）
  - [シリアル通信](../Page/シリアル通信.md "wikilink")
      - [USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")（18Fシリーズ以上の一部）
      - [SPI](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink")
      - [I2C](../Page/I2C.md "wikilink")
      - [USART](https://ja.wikipedia.org/wiki/USART "wikilink")
      - [CAN](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink")
  - [パラレル通信](https://ja.wikipedia.org/wiki/パラレル通信 "wikilink")
  - ウォッチドッグタイマ (WDT) フリーズ・暴走を回避する為の監視タイマ
  - [JTAG](../Page/JTAG.md "wikilink")プログラミング（24FとdsPIC33Fシリーズのみ）
  - [USB On-The-Go機能](../Page/USB_On-The-Go.md "wikilink")

## PICの種類

### 8bit PICシリーズ（データメモリが8ビット幅）

  - 命令長12、14ビットコアシリーズの特徴

:\* CPUの内蔵[レジスタはWレジスタ](../Page/レジスタ_\(コンピュータ\).md "wikilink")（[アキュムレータ](../Page/アキュムレータ_\(コンピュータ\).md "wikilink")）一つしかない。データメモリ空間にはSFR (Special Function Register) とGPR（General Purpose Register。いわゆるRAM）が混在している。一般的にはマイクロコントローラの周辺機能のレジスタをSFRと呼ぶが、PICにおいてはプログラムカウンタやステータスレジスタ、インデックスレジスタなど、一般的にはCPU内蔵レジスタとなっているものまでがSFRとしてデータメモリ空間上に存在している。

  - \* データメモリ空間は「レジスタファイル」と呼ばれ、アドレス0x00-0x7F（命令長12ビットコアの場合0x00-0x1F）をレジスタのような感覚で高速にアクセスできるようになっているが、この範囲を超えるアドレスはバンク切り替えでアクセスする必要があり、リニアなメモリアクセスに難がある。

:\* GOTO、CALL命令のアドレス指定部が限られているため、一定サイズ以上のプログラムはページ切り替えを必要とする。

:\* 定数テーブルは作れないので（コード空間とデータ空間が分離されているハーバードアーキテクチャであり、ROMはすべてコード空間に存在するため）、[リテラルをWレジスタに返すリターン命令](https://ja.wikipedia.org/wiki/リテラル#コンピュータプログラミング "wikilink") (RETLW) を並べて代用する。

:\* 一般的なCPUのようなジャンプ先を指定できる条件ジャンプ命令を持っておらず、あるのは「ビットテスト結果で次の命令をスキップ」するBTFSC, BTFSS命令だけである。これらとGOTO命令等を組み合わせて条件分岐せざるを得ないため、直感的でないコーディングを強要される。

:\* 命令長12ビットコアは割り込み機構を持っていない。割り込み機構がある14ビットコアでも、割り込み時の自動コンテキスト保存は一切行われないためプログラムで対応する必要がある。

:\* [スタック](../Page/スタック.md "wikilink")は一般的なCPUのようにデータメモリ空間を使用するのではなく、RETURN系命令の戻り先を積むための専用メモリが用意されている（ハードウェアスタック）。段数は命令長12ビットコアでは2レベル・命令長14ビットコアでは8レベルと限られているのであまり深いネストはできない。

:\* 古い品種ではGPIO出力・入力共にPORTnレジスタを使用する。PORTnレジスタは読み込むとポートの入出力設定に関わらず常にピンの状態が読み込まれる。このためリードモディファイライトには注意が必要であったが、比較的新しい品種ではGPIO出力ラッチレジスタLATnが新設され、この問題に対応している。

  - Enhancedミッドレンジコア(命令長14ビット)シリーズの特徴

:\* 後述の命令長16ビットコアの登場後、その機能を一部取り込んで新たに投入された拡張版の命令長14ビットコアアーキテクチャ。命令数の増加・コードメモリ／データメモリのリニア化・スタックの倍増（16レベル）・割り込み時のハードウェアによるコンテキスト保存などが強化されている。

  - 命令長16ビットコアシリーズの特徴

:\* 命令長12, 14ビットシリーズをベースに、アーキテクチャを[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")向きに改良するなど、より汎用マイコンらしく拡張されている。

:\* コードメモリのページ切り替えは必要なくなった。

:\* データメモリもバンクを意識することなくリニアにアクセスできる命令が拡張された。

:\* コードメモリ空間をデータとして読み出すための命令が追加された。

:\* ハードウェア[スタック](../Page/スタック.md "wikilink")は32レベルに拡張された。

:\* 最大CPUクロックは品種によるが40-64MHz（1命令実行サイクルに4クロックを要する点は命令長12, 14ビットコアシリーズと同様）

:\* 命令長12ビット、14ビットコアの品種ではプログラムメモリ容量を**ワード(命令長)単位**で表記していたが、命令長16ビットコアの品種では基本的に**バイト（8ビット）単位**で表記し、ワード単位表記も併記される形になったので注意が必要である。すなわちプログラムメモリ32KBの品種では、16384命令までのプログラムが格納可能となる。

  - ベースラインシリーズ（命令12ビット長コア）

:; PIC10系

::このシリーズは全て6ピンである（表面実装パッケージの場合。[DIPの場合はNC](../Page/パッケージ_\(電子部品\).md "wikilink")2ピンを加えて8ピンとしている）

::;10F200

::;10F202 等

:;PIC12系

  -

      -
        PIC12は初期からある8ピンのシリーズである。初期の品種は12ビットコアだが、その後14ビットコア・Enhancedミッドレンジ（拡張版命令14ビット長コア）の品種も加わっている。
          - 12C508,509
            初期の、プログラムメモリにワンタイムPROM（1回のみ書き込み可能）を使用した品種。開発用の紫外線消去窓付きの品種(CE)もあった。
          - 12F508,509
            12C508,509のフラッシュ版

  - ミッドレンジシリーズ（命令14ビット長コア）

:; PIC12系

::; 12F629

  -

      -
        発振回路 (4MHz) を内蔵し単独動作可能な8PinのPIC

:; 12F675

:::12F629にA/Dコンバータを追加

::; 12F683

  -

      -
        CCPを搭載・内部クロック8MHz

:; PIC16系

::; 16F84A

:::多数のPIC入門書で取り上げられた定番機種（だが、周辺機能はGPIOとタイマしかない）。

::; 16F648A

:::16F84Aに多彩な機能を追加搭載、発振回路(4MHz)内蔵したため単独動作で実験できるため扱いやすい、CCP・USARTを搭載

::; 16F88

:::18PinのPICでは最も多機能な機種、A/Dコンバータ搭載、内蔵クロック8MHz搭載

::; 16F877A

:::40pinとI/Oの数も多く機能も16F88以上、プログラムメモリも8Kワードで大容量

::; 16F887

:::16F877Aの改良版。発振回路を内蔵し、A/Dコンバータのピン数が増えている。

::; 16F876A

:::16F877Aの28pin版

::; 16F886

  -

      -
        16F887の28pin版

  - Enhancedミッドレンジシリーズ（拡張版命令14ビット長コア）

:; PIC12系

::; 12F1571 等

:; PIC16系

::; 16F19xx 等

::; 16F1455

  -

      -
        14ピンながら[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")（デバイス）モジュールを備える。

  - [ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")シリーズ（命令16ビット長コア）
    2016年6月現在、このシリーズに属する物はPIC18シリーズのみである

      - PIC18系, PIC18 Kシリーズ, PIC18 Jシリーズ

    :\* PIC18 Kシリーズは低消費電力・高パフォーマンスアプリケーションに対応したシリーズと位置づけられている（反面、チップトータルでのポート駆動能力は他品種に比べて低い場合がある）。

    :\* PIC18 Jシリーズは高機能シリーズとなっており、最大のものは100ピンパッケージで外部メモリバスインタフェイスを備える。

    :;18F4520

    ::40Pin。プログラムメモリは32KB(16Kワード)、RAMは約1.5KB

    :;18F2550

    ::28Pin。USB（デバイス）モジュールを内蔵

    :;18F4550

    ::18F2550の40Pin版

    :; 18F2620

    ::28Pin。8722と同じRAM容量をもつ

    :; 18F4620

    ::18F2620の40Pin版

    :; 18F8722

    ::80Pin [TQFPパッケージ](https://ja.wikipedia.org/wiki/QFP "wikilink")、プログラムメモリは128KB、RAMも約4KBと大容量

    :; 18F14K50

    ::20Pin。USB（デバイス）モジュールを内蔵。手頃なピン数で手軽に扱えるUSBマイコンとして近年よく利用されている。

    :; 18F2480

      -

          -
            28Pin。自動車の車載ECU間及び診断用コネクタなどとの通信に使用される[CANインタフェイスを実装したECANモジュールを備える](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink")。
            ELM Electronics社のという[OBD2](https://ja.wikipedia.org/wiki/OBD2 "wikilink")（標準化された診断用コネクタ）-非同期シリアル変換チップは、18F2480にファームウェアを書き込んだ製品である（低消費電力版ELM327Lは18F25K80を使用）。ELM327と[Bluetooth](../Page/Bluetooth.md "wikilink") (SPP) モジュールを組み合わせドングル状にしたOBD2-Bluetoothアダプタもまた通称ELM327と呼ばれている。ELM Electronics社は当初コードプロテクトをかけずにチップを出荷してしまったため、デッドコピー品が大量に出回ってしまっている。

### PIC24とdsPIC

2001年にマイクロチップ社はdsPICシリーズを発表し\[1\]、2004年後半に出荷を開始した。

マイクロチップ社による本格的な16ビットのマイクロコントローラである。 PIC24は一般的な目的用であり、dsPICは[DSPの能力を追加したものである](../Page/デジタルシグナルプロセッサ.md "wikilink")。

1.  PIC24　　　このシリーズにはプログラムメモリ256KB、RAM32KBといった大容量なものもある
      - PIC24F系　　　最大16[MIPS](https://ja.wikipedia.org/wiki/MIPS "wikilink")
      - PIC24H系　　　最大40MIPS
      - PIC24E系　　　最大70MIPS
2.  dsPIC　　　命令[24ビット](https://ja.wikipedia.org/wiki/24ビット "wikilink")長・データ長16ビットのCPUコアと、DSPを内蔵
      - dsPIC30F系　　　最大30MIPS
      - dsPIC33F系　　　最大40MIPS
      - dsPIC33E系　　　最大70MIPS

それでいてそれ以前のPICアーキテクチャに類似しているにもかかわらず、飛躍的に拡張されている:\[2\]

  - すべてのレジスタは16ビット幅
  - 命令実行サイクルがこれまでのPICアーキテクチャの4クロックサイクルから、2クロックサイクルに短縮された
  - データアドレス空間は64KBに拡張される
  - 最初の2KBは周辺機器コントロールレジスタとして予約される
  - データバンク切り替えはRAMが62KBを超えるまで必要ない
  - 「fオペランド」による直接的なアドレス指定は13ビットに拡張される (8KB)
  - 16W レジスタが、レジスタ間命令用に利用できる（ただしfオペランドとは常にW0が参照される）
  - プログラムカウンタは22ビット（ビット22:1が有効で、bit0は常に0）
  - 命令は24ビット幅
  - 命令はバイト (B=1) および16ビット形態 (B=0) をとる
  - スタックはRAMの中にとられる（W15がスタックポインタ）; ハードウェアスタックは存在しない
  - W14はフレームポインタ
  - ROMに格納されたデータは直接参照できる（プログラム空間が読める）
  - 異なる割り込みソースからの割り込みベクタがサポートされる

いくつかの特長:

  - ハードウェア[積和演算](../Page/積和演算.md "wikilink")
  - [バレルシフタ](../Page/バレルシフタ.md "wikilink")
  - ビット反転
  - 16x16ビットの1サイクルでの積算およびその他のDSP命令
  - ハードウェア除算支援（16/32ビット除算で19サイクル）
  - ループ処理に対するハードウェア支援(ゼロオーバーヘッドループ)
  - [ダイレクトメモリアクセス](https://ja.wikipedia.org/wiki/ダイレクトメモリアクセス "wikilink")

dsPICではマイクロチップXC16コンパイラ（C30と呼ばれる）を使用することでC言語でプログラミングできる。これはGCCの一種である。

プログラム用ROMは24ビット幅である。ソフトウェアは16ビット幅でこのROMにアクセスできる。16ビット2ワードとして読み込むと、1ワード目は16ビット、2ワード目は8ビットであり、上位8ビットは0が設定される。プログラムカウンタは23ビット幅であるが、最下位ビットは常に0であり、実質的には22ビットである。

命令は大きく2種類ある。 一つはクラシックなPIC命令であり、W0および指定されたfレジスタ（例えば最初の8KBのRAM）の間の処理である。出力先はビット設定により選択され、処理結果として書き換えられる。Wレジスタはメモリマップである。つまりfオペランドはあらゆるWレジスタであるといえるだろう。

### PIC32MX

2007年11月、マイクロチップ社は新しい32ビットマイクロコントローラである[PIC32MX](https://ja.wikipedia.org/wiki/PIC32MX "wikilink")ファミリーを発表した。 最初のラインナップは業界標準である[MIPSアーキテクチャ](../Page/MIPSアーキテクチャ.md "wikilink")を採用している\[3\]。 この製品は[Microchip MPLAB C Compiler for PIC32 MCUs](http://microchip.com/c32)によってプログラムを作成できる。このコンパイラは[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")の派生である。 最初の18モデル（PIC32MX3xxおよびPIC32MX4xx）は既存の16ビット製品であるPIC24FxxGA0xxファミリーとピン配置および周辺サポートに互換性があり、同じソフトウェアライブラリやハードウェアの装置が使用できる 今日では28ピンのより小さなQFNパッケージが出荷されており、ハイパフォーマンス向けに[イーサネット](../Page/イーサネット.md "wikilink")、CAN、[USB On-The-Goのサポートが含まれる製品もある](../Page/USB_On-The-Go.md "wikilink")。ミッドレンジの32ビットマイクロコントローラのすべてのファミリーが利用可能である。

PIC32アーキテクチャはマイクロチップ社のポートフォリオにいくつかの新しい特長をもたらしている:

  - 最大512KBの[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")
  - 1つのインストラクションは1クロックで実行される
  - キャッシュメモリのある初めてのプロセッサ
  - RAMから実行可能になった
  - フルスピード対応のUSBデバイスまたはOTGホストとなれる二役のサポート
  - [JTAG](../Page/JTAG.md "wikilink")にフル対応および2ワイヤーによるROM書き換えおよびデバッグ
  - リアルタイムトレース

### PIC32MZ

2013年11月、マイクロチップ社はMIPS M14KコアをベースとしたPIC32MZシリーズのマイクロプロセッサを発表した。

PIC32MZシリーズの特長:\[4\]

  - 200 MHz動作、および330 DMIPS、3.28 CoreMark/MHzのパフォーマンス
  - 2MBのフラッシュメモリおよび512KBのRAM
  - 新しい周辺サポート。ハイスピードUSBおよび暗号化エンジン、SQI

## PIC互換

1.  SCENIX SXシリーズ - [SCENIX](https://ja.wikipedia.org/wiki/SCENIX "wikilink")（現在は[Ubicom](https://ja.wikipedia.org/wiki/Ubicom "wikilink")）のCPUで、[ミップス・テクノロジーズ](../Page/ミップス・テクノロジーズ.md "wikilink")を[スピンオフ](../Page/スピンオフ.md "wikilink")したチームが開発した。PICとバイナリ互換で命令を4倍速にし、さらに50MHzや75MHzと高クロック化されている。PIC12相当のものとPIC16相当のものがある。

## クローン製品

### ELAN Microelectronics

[ELAN Microelectronics Corp.](https://ja.wikipedia.org/wiki/:en:List_of_common_microcontrollers#ELAN_Microelectronics_Corp. "wikilink") ELAN社は13ビット命令長のPICライクなマイクロコントローラーを発表している。\[5\] この命令セットは14ビット命令セットのミッドレンジにもっとも互換性があるが、レジスターアドレスが6ビットであり（16個の専用目的のレジスタおよび48バイトのRAM）10ビット(1024ワード)のプログラム空間である。10ビットのプログラムカウンターはR2としてアクセスできる。

下位のビットのみが読み込み可能であり、上位のビットが書き込みやクリアができる。 TBL命令の例外によって、あらかじめ保存された下位バイト8-9が書き換えられる。(原文:which modifies the low byte while preserving bits 8 and 9.) 7つの即時積算命令が14ビットのPICの同等命令に対応する。オペコードを示すビットが3ではなく4ビットあるが、それらはそこだけではなく、追加されるソフトウェア割り込みに割り当てられている。

いくつかの雑多な命令が追加されており、述語の変更であるが、(PICオプションレジスタはコントロールレジスタと呼ばれる; PIC 1-3はTRISレジスター、5-7はI/Oコントロールレジスタ)明らかに同等である。

いくつかのモデルはほかのPICにあるような複数のROMやRAMバンクを持つ。

### Holtek

[Holtek](https://ja.wikipedia.org/wiki/Holtek "wikilink")は多種のPICライクなマイクロコントローラーを発表しており\[6\]、HT37、HT4x、HT56、HT6x、HT82、HT95ファミリーなどである。 14ビットのミッドレンジのPICマイクロコントローラーに似ているが、正確なクローンではない。 ステータスレジスタは算術的なオーバーフローフラグを持ち、いくつかの追加命令を含み、2ポインタを使用する非直接的なレジスタを含む。

3種類の命令幅がある:

  - 14ビット命令セット、11ビットROMアドレス(2Kx14ビット)および7ビットRAMアドレス
  - 15ビット命令セット、12ビットROMアドレス(4Kx15ビット)および8ビットRAMアドレス
  - 16ビット命令セット、13ビットROMアドレス(8Kx16ビット)および8ビットRAMアドレス。いくつかの拡張ROMおよびRAMをバンクとして利用できる

[基本的な14-bit PIC命令セットにない命令は](https://ja.wikipedia.org/wiki/PIC_instruction_listings#Mid-range_core_devices_\(14_bit\) "wikilink"):

  - キャリーを足したり引いたりする命令
  - キャリーを無視して右や左にビットローテート
  - 0かどうかテストしてスキップする(インクリメントやデクリメントを伴わない)
  - すべてのビットを1にする(CLR命令が全てを0にするように)
  - ROMからテーブル読み込み
  - CLRWDT1およびCLRWDT2命令はウォッチドッグタイマーをリセットするために使われる。

オリジナルのPICとの特筆すべき差異:

  - 引き算は[アキュムレータ](https://ja.wikipedia.org/wiki/アキュムレータ "wikilink")から引かれる
  - TRIS/OPTION命令がない。全てのレジスタはアドレスを持つ
  - ソフトウェアはすべてのサブルーチンスタックを利用できる。スタックがいっぱいのときに割り込みはマスクされ、その関数が抜けるときに初めて実行される

## 使用可能なC言語コンパイラ

  - [MPLAB XC Compiler](http://www.microchip.com/pagehandler/ja-jp/devtools/mplabxc/)
    Windows版 (x86/x64)、Linux版 32-Bit and Linux 64-Bit (Requires 32-Bit Compatibility Libraries)、Mac版 (10.X) のコンパイラが無料で提供されており、それぞれ、MPLAB XC8 Compiler、MPLAB XC16 Compiler、MPLAB XC32 Compilerの3種のコンパイラで、発売中のすべてのPICマイクロコンピュータに対応している。統合開発環境である[MPLAB X](http://www.microchip.com/pagehandler/ja-jp/family/mplabx/)に統合して使用される。マイクロチップ・テクノロジー社が公開しているライブラリやサンプルコードをそのまま利用できる利点がある。最適化機能に制限のないPRO版と、最適化機能が制限されたFree版、Standard版があるが、個人レベルでの使用ではFree版で必要・十分な機能を得られる。Free版は、PRO版と全く同じデバイスとコマンドをサポートし、使用時間とメモリ使用量にも制限はない。ほとんどの用途で十分なコード最適化機能を備えた、機能に制限のないライセンスで使うことができる。
  - CCS PIC C Compiler
    対象となるPICの種類（ビット数）および開発環境の[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")により製品が分かれている。初期のバージョンは専用のIDEが付属していたが、最近のバージョンでは[MPLAB](https://ja.wikipedia.org/wiki/MPLAB "wikilink")に統合して使用するようになっている。
  - HI-TECH PIC C Compiler
    [MPLAB](https://ja.wikipedia.org/wiki/MPLAB "wikilink")に統合するほか[Eclipseをベースとした独自のIDEで使用できる](../Page/Eclipse_\(統合開発環境\).md "wikilink")。出力可能な容量が制限された PICC Lite は無償で使用できる。
  - mikroElektronika mikroC for PIC
    [SDカードやキャラクタLCDを含む多くのライブラリが標準でついている](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")。独自のIDEになっている。対応するシリーズは12, 16, 18シリーズのほぼ全て。PIC24やdsPICシリーズは別製品になっている。無償バージョンでは出力が2Kワードに制限されるが、その範囲内であれば有償版と同じライブラリがつかえる。また、Basic版とPascal版も販売されている。HI-TECHのコンパイラと違い、include文が不要だったり、大文字と小文字は区別しないなどの違いがある。
  - [SDCC](http://sdcc.sourceforge.net/) (Small Device C Compiler)
    小型デバイス向けのフリーのCコンパイラ。PICを含む複数のデバイスに対応しており、マルチプラットフォームで動作する。

## 脚注

## 関連項目

  - [Atmel AVR](../Page/Atmel_AVR.md "wikilink") - PICと競合する製品
  - [組み込みシステム](../Page/組み込みシステム.md "wikilink")
  - [シーケンス制御](../Page/シーケンス制御.md "wikilink")

## 外部リンク

  - [マイクロチップ・テクノロジー・ジャパン株式会社](http://www.microchip.co.jp/)
  - [Microchip MPLAB XC Compilers 無料のコンパイラー](http://www.microchip.com/pagehandler/en_us/devtools/mplabxc/)
  - [Microchip MPLAB X IDE 無料の統合開発環境](http://www.microchip.com/pagehandler/en-us/family/mplabx/)
  - [Microchip Advanced Part Selector 機能からPICを絞り込めるセレクター](http://www.microchip.com/maps/microcontroller.aspx)
  - [MPLAB XC8 入門ガイド](http://www.microchip.co.jp/download/dl_download.php/ID=1b8e81fa1e7dceaecc44ec989309ba036f5eac33/)
  - [MPLAB X IDE ユーザガイド](http://www.microchip.co.jp/download/dl_download.php/ID=eaac03ddd8ed9ab33f11001444215401dcf2fa97/)
  - [PICkit 3 プログラマ/ デバッガ ユーザガイド](http://www.microchip.co.jp/download/dl_download.php/ID=251116475b138428d44de24d7e58263ce64d5b7e/)
  - [電子工作の実験室](http://www.picfun.com/)

[Category:制御工学](https://ja.wikipedia.org/wiki/Category:制御工学 "wikilink") [Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink") [Category:ロボット工学](https://ja.wikipedia.org/wiki/Category:ロボット工学 "wikilink") [Category:命令セットアーキテクチャ](https://ja.wikipedia.org/wiki/Category:命令セットアーキテクチャ "wikilink")

1.  [1](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=2018&mcparam=en013529)
2.
3.  <http://www.mips.com/products/processors/32-64-bit-cores/mips32-m4k/>
4.  <http://www.microchip.com/pagehandler/en-us/press-release/microchips-pic32mz-32-bit-mcus.html>
5.  <http://www.emc.com.tw/eng/products.asp>
6.  [Holtek products, by part number](http://www.holtek.com/english/products/numindex.htm)