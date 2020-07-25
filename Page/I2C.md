> この記事は[I2C](https://ja.wikipedia.org/wiki/I2C)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:I2C.svg "wikilink") **I<sup>2</sup>C**（アイ・スクエアド・シー、アイ・アイ・シー）は[フィリップス](../Page/フィリップス.md "wikilink")社で開発された[シリアルバス](https://ja.wikipedia.org/wiki/シリアルバス "wikilink")である。低速な周辺機器を[マザーボード](../Page/マザーボード.md "wikilink")へ接続したり、[組み込みシステム](../Page/組み込みシステム.md "wikilink")、[携帯電話](../Page/携帯電話.md "wikilink")などで使われている。

*Inter-Integrated Circuit* の略で、*I-squared-C*（アイ・スクエアド・シー）が正式な[読みとされている](https://ja.wikipedia.org/wiki/発音 "wikilink")。ただし、一般的な[文字コード](../Page/文字コード.md "wikilink")環境の[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")上では上付き文字が使えないため、**I2C**あるいは**IIC**と表記されることも多く、これをもって「アイ・ツー・シー」と発声されたりカタカナ表記される\[1\]ことがある。

## 設計

I<sup>2</sup>C で使われているのは、[抵抗で](../Page/抵抗器.md "wikilink")[プルアップ](https://ja.wikipedia.org/wiki/プルアップ "wikilink")された双方向の[オープンコレクタ](../Page/オープンコレクタ.md "wikilink")信号線が**2本**だけである。2本の信号線は、**シリアルデータ** (SDA) と**シリアルクロック** (SCL) からなる。 電圧は最高で +5V までで、よく使われるのは +3.3V だが、他の電圧でも構わない。

I<sup>2</sup>C の参照設計では、7[bit](../Page/ビット.md "wikilink") の[アドレス空間](../Page/アドレス空間.md "wikilink")のうち 16 の予約アドレスを除いた最大 112 個の[ノード](https://ja.wikipedia.org/wiki/ノード "wikilink")が、同じバス上で通信できる。 もっとも一般的な I<sup>2</sup>C バスのモードは、100[kbit/s](https://ja.wikipedia.org/wiki/キロビット毎秒 "wikilink") の標準モード () と 10kbit/s の低速モード () だが、クロック周波数はゼロまで下げても構わない。 ノード数の拡大と高速動作が可能な 400kbit/s のファーストモード () や 3.4Mbit/s の高速モード () の追加と、10bit アドレス空間などの機能拡張が行なわれている。

特定のI<sup>2</sup>Cバス上に存在できるノードの数は、アドレス空間とバスの静電容量によって制限され、実際の通信距離は数メートルに制限される。比較的高いインピーダンスと低い雑音耐性は共通の接地電位を必要とし、実用的にはPC基板や小さな基板同士の通信に制限される。\[2\]

## 改訂

元々の I<sup>2</sup>C システムは、フィリップスの各種チップを使った電子機器制御用のシンプルな内部[バスシステムとして](../Page/バス_\(コンピュータ\).md "wikilink")[1980年代](../Page/1980年代.md "wikilink")初期に開発されたものである。

  - [1992年](../Page/1992年.md "wikilink")バージョン 1.0 - 最初の標準化が行なわれ、400kbit/s のファーストモード (fast mode) と、1008ノードまでの 10bit アドレッシングモードが追加された。

<!-- end list -->

  - [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")バージョン 2.0 - 3.4Mbit/s の高速モード (high-speed mode) と、低消費電力を目的とした低電圧・低電流条件が追加された。

<!-- end list -->

  - [2001年](../Page/2001年.md "wikilink")バージョン 2.1 - 2.0 からの小修正である。

<!-- end list -->

  - [2007年](../Page/2007年.md "wikilink")バージョン 3 - Fast mode plus (Fm+) を追加、通信速度を従来の Fast mode (Fm) 0～400kbit/s から 0～1000Kb/s に向上させるための条件を規格化。

<!-- end list -->

  - [2012年](../Page/2012年.md "wikilink")バージョン 4 - Ultra fast mode (UFm) を追加、通信速度を 0～5000Kb/s に高速化させるため物理層をオープンコレクタ出力からCMOS出力に変更。予約アドレスから不要な CBUS address / Hs-mode master code が reserved に変更され general call address / START byte / 10-bit slave addressing のみ対応。

<!-- end list -->

  - [2012年](../Page/2012年.md "wikilink")バージョン 5 - 誤記修正

<!-- end list -->

  - [2014年](../Page/2014年.md "wikilink")バージョン 6 - 2つの図を修正。最新版。\[3\]

最新の仕様書は、フィリップスが設立した[NXPセミコンダクターズ](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")社のサイトにて配布されている。また、2004年8月に特許が失効しており、現在は[ロイヤリティフリー](https://ja.wikipedia.org/wiki/ロイヤリティフリー "wikilink")である。

## 応用

I<sup>2</sup>C が適しているのは、シンプルで製造コストを抑えることが速度よりも重要とされるような周辺機器である。 I<sup>2</sup>C バスの代表的な用途としては、次の通り。

  - [DRAMのバスタイミングの設定記憶](../Page/Dynamic_Random_Access_Memory.md "wikilink")()
  - ユーザの設定を記憶しているシリアル[不揮発性メモリ](../Page/不揮発性メモリ.md "wikilink")(24C01/24C02/24C04など)へのアクセス。
  - 低速な [D/Aコンバータへのアクセス](../Page/デジタル-アナログ変換回路.md "wikilink")。
  - 低速な [A/Dコンバータへのアクセス](../Page/アナログ-デジタル変換回路.md "wikilink")。
  - モニターのコントラスト、色調、色バランスの変更。
  - インテリジェント・スピーカの音量変更。
  - 携帯電話などの [LED](../Page/発光ダイオード.md "wikilink") 表示の制御。
  - [リアルタイムクロック](../Page/リアルタイムクロック.md "wikilink")の読み出し。
  - CPU の温度やファンの回転速度など、ハードウェアの監視や診断用センサーの読み取り。(パーソナルコンピュータにおける[ACPI](https://ja.wikipedia.org/wiki/ACPI "wikilink")制御下の[SMBus](https://ja.wikipedia.org/wiki/SMBus "wikilink")など)
  - システムの電源オン・オフ制御。
  - 2次電池の充放電状態コントローラの通信インタフェース。(スマートバッテリシステム)

わずか2本の汎用I/Oピンとソフトウェアだけで、[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")からデバイス・チップのネットワークを制御できることが、I<sup>2</sup>C の最大の利点である。

I<sup>2</sup>C バスでは、システムが動作中であっても周辺機器の取り付け・取り外しが可能なので、[ホットスワップ](../Page/ホットスワップ.md "wikilink")が必要とされる用途には特に向いている。

I<sup>2</sup>C のようなバスが広まったのは、パッケージのサイズとピン数が、生産コストや集積回路設計に大きな影響を与えていることにコンピュータ技術者が気付いたからである。 パッケージが小さければ軽量化・低消費電力化が可能で、これは携帯電話やポータブル・コンピューティングでは特に重要なことである。

## OSでのサポート

[Linux](../Page/Linux.md "wikilink") では、I<sup>2</sup>C は特定のデバイス（ADM1026やLM92など）用に特定のカーネルモジュールで扱われている。Linux 2.6ではカーネルコンフィグレーションのでサポートするシステムハードウェアモニタを選択できる。I<sup>2</sup>Cドライバのソースコードは drivers/hwmon 配下にある。I<sup>2</sup>Cドライバは大きく分けて core と algorithm, adapter の3種類のモジュールに分割されている。 I<sup>2</sup>C クライアントの書き方の詳細は、カーネル関連のドキュメントや `/usr/include/linux/i2c.h` [ヘッダファイル](../Page/ヘッダファイル.md "wikilink")にある。 [OpenBSD](../Page/OpenBSD.md "wikilink") には最近、いくつかの共通マスター・コントローラとセンサのサポートで I<sup>2</sup>C フレームワークが加えられた。

[シンクレア](https://ja.wikipedia.org/wiki/シンクレア・リサーチ "wikilink") QDOS とミネルヴァ（ QDOS の再実装） QL オペレーティング・システムでは、TF サービスから提供されている拡張セットで I<sup>2</sup>C がサポートされている。

[AmigaOS](../Page/AmigaOS.md "wikilink") では、 Wilhelm Noeker の *i2c.library* 共有ライブラリで I<sup>2</sup>C アクセスできる。

[eCos](https://ja.wikipedia.org/wiki/eCos "wikilink") は、いくつかのハードウェア・アーキテクチャで I<sup>2</sup>C に対応している。

EPIA-M マザーボードは、[Mini-ITX](../Page/Mini-ITX.md "wikilink") で I<sup>2</sup>C に対応している。

## 派生技術

I<sup>2</sup>C が元になっているものには、 ACCESS.bus 、 [VESA](../Page/VESA.md "wikilink") の [Display Data Channel](https://ja.wikipedia.org/wiki/VESA_Display_Data_Channel "wikilink") (DDC) インターフェイス、 SMBus 、 IPMI などがある。 これらの実装では、電圧やクロック周波数に違いがあり、また[割り込み信号があることもある](../Page/割り込み_\(コンピュータ\).md "wikilink")。

## 関連項目

  - [バス (コンピュータ)](../Page/バス_\(コンピュータ\).md "wikilink")
  - [SPI](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink")
  - [CCI](https://ja.wikipedia.org/wiki/カメラ制御インターフェース "wikilink") (カメラ制御インターフェース) - I2C互換
  - [1-Wire](https://ja.wikipedia.org/wiki/1-Wire "wikilink")
  - [Wiiリモコン](../Page/Wiiリモコン.md "wikilink") - ヌンチャク等との通信に使用

## 参考文献

## 外部リンク

  - [MCC I2C Bus Technical Overview](http://www.mcc-us.com/I2CBusTechnicalOverview.pdf)
  - [I2C-bus specification and user manual Rev.6](http://www.nxp.com/docs/en/user-guide/UM10204.pdf)
  - [I2Cバス仕様およびユーザーマニュアル Rev.5](http://www.nxp.com/docs/ja/user-guide/UM10204.pdf)
  - [Detailed introduction, Primer](http://www.i2c-bus.org/)
  - [Introduction to I2C](http://embedded.com/story/OEG20010718S0073)
  - [I<sup>2</sup>C Bus / Access Bus](http://www.interfacebus.com/Design_Connector_I2C.html)
  - [Using the I2C Bus with Linux](http://www.linuxjournal.com/article/1342)
  - [OpenBSD iic(4) manual page](http://www.openbsd.org/cgi-bin/man.cgi?query=iic&sektion=4)
  - Linux package [lm-sensors](http://secure.netroedge.com/~lm78/) support I2C bus among others.
  - [massmind i2c page](http://techref.massmind.org/i2cs.htm) Source code, samples and technical information for using i2c with PC, PIC and SX microcontrollers.
  - [I<sup>2</sup>C bus](http://tmd.havit.cz/Papers/I2C.pdf)
  - [Serial buses information page](http://www.epanorama.net/links/serialbus.html)
  - [I2C Bus Technical Overview and Frequently Asked Questions](http://www.esacademy.com/faq/i2c/)
  - [The I2C Faq Version 2.0](http://www.kar.elf.stuba.sk/predmety/mmp/i2c/i2cindex.htm)
  - [The Bus Buffer Resource. For 2-wire buses such as I2C, SMBus, PMBus, IPMB & IPMI](http://www.bus-buffer.com)
  - [SMBus (System Management Bus)](http://www.smbus.org/)
  - [SBS-IF Smart Battery System Implementers Forum](http://www.sbs-forum.org/)

[カテゴリ:インタフェース規格](https://ja.wikipedia.org/wiki/カテゴリ:インタフェース規格 "wikilink")

1.
2.
3.