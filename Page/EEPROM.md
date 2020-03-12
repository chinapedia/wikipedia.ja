> この記事は[EEPROM](https://ja.wikipedia.org/wiki/EEPROM)から翻訳されています。


**EEPROM**（Electrically Erasable Programmable Read-Only Memory）は[不揮発性メモリ](../Page/不揮発性メモリ.md "wikilink")の一種。**E<sup>2</sup>PROM**とも表記される。コンピュータなどの電子機器において、設定情報など、電源を切っても保持すべきデータの記憶に用いられる。

[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")のように大量のデータを格納する用途では、従来型のEEPROMよりもその一種である[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")などの方が経済的である。EEPROMは[フローティングゲートMOSFET](https://ja.wikipedia.org/wiki/フローティングゲートMOSFET "wikilink")の配列でできている。

## 概要

EEPROMは利用者が内容を書き換え可能な[ROMであり](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")、印加する電圧を読み取りのときよりも高くすることで何回も記憶内容の消去・再書き込みが可能である。高い電圧は最近のEEPROMではチップ内部で発生させるようになっている。[EPROM](../Page/EPROM.md "wikilink")の記憶内容を消去・再書き込みするには、機器の構造にもよるが、通常は一旦取り外す必要がある。EEPROMの場合は回路設計により、機器に取り付けたまま消去・再書き込みが可能である。初期のEEPROMは1バイト単位でしか操作できず非常に遅かったが、今では多バイトページ操作が可能である。また初期のEEPROMは書き換え可能回数が限られていたが、数十回、数百回、数千回と徐々にそれが延びていった。今では百万回の書き込みも可能となっている。機器に内蔵するEEPROMが頻繁に書き換えられるような場合、このEEPROMの寿命は設計時に考慮すべき重要な問題となる。EEPROMが記憶内容の書き換えができ、電源を切っても内容が失われないという理想的なメモリのように見えるにもかかわらず、[主記憶装置](../Page/主記憶装置.md "wikilink")に使われずに主に設定情報の格納などに使われているのは、速度と寿命のためである\[1\]。

## 歴史

[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")社の George Perlegos は初期の[EPROM](../Page/EPROM.md "wikilink")技術に基づいて Intel 2816 を開発したが、酸化膜の層を使い[紫外線](../Page/紫外線.md "wikilink")を使わなくともチップ自身がビットを消去できるようにした。Perlegos らは後にインテル社を退職して Seeq Technology\[2\] を創業し、[チャージポンプ](https://ja.wikipedia.org/wiki/チャージポンプ "wikilink")回路を組み込んでEEPROMの書き換えに必要な高電圧をチップ内で発生できるEEPROMを開発した\[3\]。

## 種類

EEPROMチップの外部インタフェースにはシリアルバス型とパラレルバス型がある。EEPROMの操作方法はこのインタフェースによって大きく異なる。

### シリアルバス型

シリアルバス型のEEPROMでよく採用している[バス規格としては](../Page/バス_\(コンピュータ\).md "wikilink")、[SPI](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink")、[I²C](https://ja.wikipedia.org/wiki/I²C "wikilink")、[マイクロワイヤ](https://ja.wikipedia.org/wiki/マイクロワイヤ "wikilink")、[UNI/O](https://ja.wikipedia.org/wiki/UNI/O "wikilink")、[1-Wire](https://ja.wikipedia.org/wiki/1-Wire "wikilink") がある。これらのバスの信号線は1本から4本であり、結果としてEEPROMチップも8端子程度で済む。

シリアルEEPROMは一般に、オペコード・フェーズ、アドレス・フェーズ、データ・フェーズの3フェーズで操作される。[オペコード](../Page/オペコード.md "wikilink")はEEPROMチップの入力ピンに最初に入力される（通常）8ビットの信号であり、それに続いて8ビットから24ビット（チップの記憶容量に依存する）のアドレス指定信号、その後に（読み取った、あるいは書き込むべき）データ信号がバス上を流れる。

オペコードはEEPROMチップ毎に決まっており、それによって操作の種類を指定する。[SPIの場合](../Page/シリアル・ペリフェラル・インタフェース.md "wikilink")、次のような命令が一般に存在する。

  - 書き込みイネーブル (Write Enable, WREN)
  - 書き込みディセーブル (Write Disable, WRDI)
  - ステータスレジスタ読み取り (Read Status Register, RDSR)
  - ステータスレジスタ書き込み (Write Status Register, WRSR)
  - データ読み取り (Read Data, READ)
  - データ書き込み (Write Data, WRITE)

一部のEEPROMでは他に次のような命令をサポートしている。

  - プログラム (Program)
  - セクタ消去 (Sector Erase)
  - 全消去 (Chip Erase)

### パラレルバス型

パラレルEEPROMチップは一般に8個（8ビット）のデータ端子と記憶容量に対応したぶんのアドレス端子を持つ。チップセレクト端子と書き込み保護端子も持っていることがほとんどである。一部の[マイクロコントローラ](../Page/マイクロコントローラ.md "wikilink")はパラレルEEPROMを内蔵している。

パラレルEEPROMの操作はシリアルに比べれは単純で高速だが、端子数が多いので（24かそれ以上）チップの占める面積も大きくなる。このためシリアル型やフラッシュメモリに比べて敬遠される傾向にある。

### その他

EEPROMは厳密にはメモリチップでないチップに必要に迫られて組み込まれることがある。例えば[リアルタイムクロック](../Page/リアルタイムクロック.md "wikilink")、デジタル・[ポテンショメータ](../Page/ポテンショメータ.md "wikilink")、デジタル[温度センサなどでは](https://ja.wikipedia.org/wiki/シリコン温度センサ "wikilink")、校正情報などの電源を切った際に保持する必要があるデータをチップ内蔵のEEPROMに格納している。

## 限界

EEPROMに記憶させた情報について、書き換え回数の限界と情報を保持できる期間の限界が存在する。

書き換えの際、[フローティングゲートMOSFET](https://ja.wikipedia.org/wiki/フローティングゲートMOSFET "wikilink")のゲート酸化膜は徐々に捉えた電子を蓄えていく。捉えられた電子が電界を発生することでそれがフローティングゲートに印加され、0と1を表す電圧の差が徐々に縮まっていく。ある十分な回数書き換えを行うとその差が判別できなくなり、そのセルの内容が0なのか1なのかわからなくなる。一般にメーカーはこのような問題が発生する書き換え回数を 10<sup>6</sup> かそれ以上としている\[4\]。

フローティングゲートに注入された電子は、特に温度が上がると不導体を通り抜けて漂うようになり、蓄えた電荷が徐々に失われ、最終的にはセルの記憶が消去された状態になる。メーカーによれば、記憶したデータが保持される期間は10年かそれ以上だという\[5\]。

## 関連する種類のメモリ

[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")はEEPROMの一種で比較的新しい。業界ではバイト単位の消去を行うデバイスをEEPROMと呼び、ブロック単位で消去を行うデバイスをフラッシュメモリと呼ぶことが多い。EEPROMはセル（1ビットを記憶する回路）毎に読み取りと書き込みと消去のための[トランジスタ](../Page/トランジスタ.md "wikilink")を必要とするが、フラッシュメモリではブロック（通常512×8セル）単位で消去用回路を共有しているため、単位記憶容量あたりのチップ面積が小さくなる。

[FeRAMや](../Page/強誘電体メモリ.md "wikilink")[MRAMといったさらに新しい不揮発性メモリ技術がEEPROMを徐々に置き換えつつある](https://ja.wikipedia.org/wiki/磁気抵抗メモリ "wikilink")。

### EPROMとEEPROM/フラッシュメモリとの比較

[EPROM](../Page/EPROM.md "wikilink")とEEPROMの違いは書き込みと消去の方式の違いである。EEPROMは[電界電子放出](https://ja.wikipedia.org/wiki/電界電子放出 "wikilink")（FNトンネリング）を利用して電気だけで書き込みと消去が可能である。

EPROMは電気だけでは消去できず、フローティングゲートへの[ホットキャリア注入](https://ja.wikipedia.org/wiki/ホットキャリア注入 "wikilink")で再書き込みを行う。消去には[紫外線](../Page/紫外線.md "wikilink")光源を使う。内部は同じ半導体を使いながらも、安価なプラスチックパッケージ（窓なし）を使って最初の1回しか書き込めないものを「PROM」と言う。

多くの[NOR型フラッシュメモリ](../Page/NOR型フラッシュメモリ.md "wikilink")はハイブリッドな方式を採用しており、書き込みはホットキャリア注入で行い、消去は電界電子放出で行う。

## EEPROMメーカー

  - [インフィニオン・テクノロジーズ](../Page/インフィニオン・テクノロジーズ.md "wikilink")
  - [三菱電機](../Page/三菱電機.md "wikilink")
  - [NXPセミコンダクターズ](https://ja.wikipedia.org/wiki/NXPセミコンダクターズ "wikilink")
  - [オン・セミコンダクター](https://ja.wikipedia.org/wiki/オン・セミコンダクター "wikilink")
  - [ルネサス エレクトロニクス](https://ja.wikipedia.org/wiki/ルネサス_エレクトロニクス "wikilink")
  - [ローム](../Page/ローム.md "wikilink")
  - [サムスン電子](../Page/サムスン電子.md "wikilink")
  - [STマイクロエレクトロニクス](../Page/STマイクロエレクトロニクス.md "wikilink")
  - [セイコーインスツル](../Page/セイコーインスツル.md "wikilink")
  - [Atmel](https://ja.wikipedia.org/wiki/Atmel "wikilink")

## 脚注・出典

## 関連項目

  - [フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")

[Category:不揮発性メモリ](https://ja.wikipedia.org/wiki/Category:不揮発性メモリ "wikilink") [Category:集積回路](https://ja.wikipedia.org/wiki/Category:集積回路 "wikilink") [Category:記憶装置](https://ja.wikipedia.org/wiki/Category:記憶装置 "wikilink")

1.  [EEPROM](http://www.tech-faq.com/eeprom.html) TopBits.com
2.  [Seeq Technology](http://www.antiquetech.com/companies/seeq_technology.htm) The Antique Chip Collector's Page
3.
4.  [FAQ EEPROMとは？](http://www.rohm.co.jp/products/lsi/eeprom/faq.html) ROHM
5.  System Integration - From Transistor Design to Large Scale Integrated Circuits