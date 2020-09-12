> この記事は[CANape](https://ja.wikipedia.org/wiki/CANape)から翻訳されています。


**CANape**は[ベクター・インフォマティック](https://ja.wikipedia.org/wiki/ベクター・インフォマティック "wikilink")のソフトウェアツール。この開発ソフトウェアは、自動車業界のOEMおよびECUサプライヤーによって広く使用されており\[1\]\[2\]\[3\]\[4\]\[5\]\[6\]\[7\]、動作中に[ECUの](https://ja.wikipedia.org/wiki/エレクトロニックコントロールユニット "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")を調整するために使用される。

## 説明

ECUのキャリブレーションでは、さまざまな車両モデルやバリエーションの制御動作が変更される。プログラムコードを変更することなく、ECUの[パラメータ](https://ja.wikipedia.org/wiki/パラメータ "wikilink")設定を変更することによってこれを行う。このために、実験室、テストベンチ、または車両でのテスト試行でCANapeなどの測定・キャリブレーションシステムを利用することがある。パラメーターの変更の影響を評価するために、開発エンジニアは[センサ](../Page/センサ.md "wikilink")と[アクチュエータ](../Page/アクチュエータ.md "wikilink")で従来の測定技術を使用して関連するプロセス変数にアクセスし、ECUからデータを読み取る。ECU内部の測定データ（例：計算関数の中間結果）は、ASAM標準プロトコルまたはCCPおよびECUの標準インターフェース（([CAN](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink")、[FlexRay](https://ja.wikipedia.org/wiki/FlexRay "wikilink")、、[Ethernet](../Page/イーサネット.md "wikilink") / ）を介してアクセスできる。 For a high-performance ECU access, data from microcontroller-specific interfaces (for example JTAG, DAP, AURORA) can be converted via an external hardware (like Vector’s VX1000 system) in XCP on Ethernet. A typical use case for calibration with CANape is online calibration. This involves modifying parameters directly in the ECU. The resulting control characteristic can be measured and checked directly. Using this approach, measured data from the ECU or physical measurement variables on or in the vehicle can be precisely analyzed to determine the effects of each individual change.

## 特徴

Functions required to modify parameter values are implemented as standard features in CANape: Measuring, analyzing (manually or automated),\[8\] calibrating, calibration data management, and flashing. CANape also enables symbolic access to data and functions accessible via the diagnostic protocol, and it supports calibration over  on FlexRay.\[9\] Options extend the functional features of CANape\[10\] by enabling access to models at runtime in [Simulink](../Page/Simulink.md "wikilink"), functional bypassing, optical verification of object detection algorithms in developing driver assistance systems ([ADAS](https://ja.wikipedia.org/wiki/先進運転支援システム "wikilink")), and an ASAM MCD3 interface.

CANape uses its own scripting language, hereinafter referred to as CASL (Calculation and Scripting Language).\[11\] CASL, is a signal-oriented language. CANape contains a function editor for writing cross-device functions and scripts. The CASL scripting language used for this is similar to the C programming language. For easier use, CANape provides an IntelliSense input, code blocks, and various built-in function groups. Functions and scripts can be used to solve a variety of different tasks from simple calculations, e.g., adding signals, to automation of CANape.

## バージョン

Version 1.0 was released in 1996.\[12\] Up to Version 6.0 the product was known as CANape Graph. In January 2017, CANape version 15.0\[13\] was current. In October 2019, the current version was 17.0\[14\].

## サポートする標準

Internal ECU parameters are accessed via standardized measurement and calibration protocols such as CCP (CAN Calibration Protocol) and XCP (Universal Measurement and Calibration Protocol). CANape was the first measurement and calibration tool to enable access over XCP on CAN\[15\] and XCP on FlexRay.\[16\]

Supported ASAM standards,\[17\] status as of June 2015:

  - AE MCD-1 XCP
  - XCP on CAN Interface Reference
  - XCP on Ethernet Interface Reference
  - XCP on FlexRay Interface Reference
  - XCP on SxI Interface Reference
  - XCP on [USB](../Page/ユニバーサル・シリアル・バス.md "wikilink") Interface Reference
  - AE MCD-1 CCP
  - AE MCD-2MC ASAP2/A2L
  - AE MCD-2D ODX
  - AE MCD-2
  - AE MCD-3
  - COM/DCOM Interface Reference
  - ASAP3 (Automation/Optimization Interface)
  - MDF

Other supported standards:

  - CAN with DBC description format, CAN FD, Ethernet, BroadR-Reach, SOME/IP, FlexRay, LIN, SAE J1939, GMLAN, and MOST
  - [KWP2000](https://ja.wikipedia.org/wiki/KWP2000 "wikilink") on K-Line
  - ISO 14230 (KWP2000 on CAN) and ISO 14229 (UDS)
  - Transport protocols ISO/TF2 and VW-TP2.0
  - Integration of measuring devices and hardware interfaces of third-party manufacturers
  - iLinkRT

If a development task requires a high measurement data throughput of up to 30 MByte/s, Vector’s VX1000 System\[18\] can be used to access data over microcontroller-specific data trace and debug interfaces like JTAG, DAP, LFAST, RTP/DMM, Nexus AUX or AURORA.

## 関連項目

  - [CANalyzer](../Page/CANalyzer.md "wikilink")
  - [CANoe](../Page/CANoe.md "wikilink")

## 参照

## 外部リンク

  - [CANape on the web site of Vector](https://www.vector.com/jp/ja/products/products-a-z/software/canape/)
  - [ASAM (Association for Standardisation of Automation and Measuring Systems)](https://web.archive.org/web/20111121132716/http://www.asam.net/nc/home/products-services.html) – CCP and XCP at standard category "ASAM AE (Automotive Electronics) – Software Development, Connection and Use of Controllers"

[Category:CAE](https://ja.wikipedia.org/wiki/Category:CAE "wikilink") [Category:ネットワーク・アナライザ](https://ja.wikipedia.org/wiki/Category:ネットワーク・アナライザ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. [Options for CANape](http://www.vector.com/vi_canape_en.html)
11.
12.
13. [Version History CANape](http://vector.com/vi_canape_versionhistory_en.html)
14. [1](https://www.vector.com/us/en-us/products/products-a-z/software/canape/)
15.
16.
17.
18.