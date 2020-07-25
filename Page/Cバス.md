> この記事は[Cバス](https://ja.wikipedia.org/wiki/Cバス)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:c_bus.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:PC-9801DX_expansion_slot.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:NEC_PC-9801-26K_sound_board.jpg "wikilink")）\]\] **Cバス**は[日本電気](../Page/日本電気.md "wikilink")の[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")に搭載されていた[拡張スロット](https://ja.wikipedia.org/wiki/拡張スロット "wikilink")の名称である。

この名称は、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に[NESAを搭載した](../Page/New_Extend_Standard_Architecture.md "wikilink")[PC-H98シリーズが発売された際に](https://ja.wikipedia.org/wiki/PC-9800シリーズ#PC-H98シリーズ "wikilink")32ビット[バスの](../Page/バス_\(コンピュータ\).md "wikilink")[NESAバスをEバス](../Page/New_Extend_Standard_Architecture.md "wikilink")(Extension Bus)、16ビットの従来互換バスをCバス(Compatible Bus)と呼称したことからこれ以降使われるようになった[レトロニム](../Page/レトロニム.md "wikilink")であり、それ以前は単に「汎用拡張スロット」または、98バス等と呼ばれていた。

98シリーズ以外にもCバスの採用機種があった。[PC-88VAシリーズ](https://ja.wikipedia.org/wiki/PC-8800シリーズ "wikilink")、[文豪](../Page/文豪.md "wikilink")シリーズの一部機種、シャープ [MZ-2861](../Page/MZ-2861.md "wikilink")など。

## 規格

  - [Intel 8086のCPUバスに準拠](../Page/Intel_8086.md "wikilink")。
      - ただし、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")発売のPC-98XA以降の機種では、[Intel 80286に対応し](../Page/Intel_80286.md "wikilink")、アドレス線が20bitから24bitに拡大されている。
  - 5MHz、8MHz もしくは 10MHzで駆動され、10Mbytes/secの理論最大転送帯域を有する。
  - 1スロット当り、+5V 0.8A、+12V 0.06A、-12V 0.07A（[EPSON98互換機はそれぞれ](../Page/EPSON_PCシリーズ.md "wikilink")1A、0.125A、0.075A）の電源容量が保証され、他のスロットを使用しない前提でn倍の電力を消費することも許されている。
  - [拡張カード](../Page/拡張カード.md "wikilink")は奥行き17cm、幅15cmの長方形で、部品実装面の厚さは2.5cmまでが許容されている。
  - 100本（片面あたり50本ずつ）の端子を持ち、アドレスバス、データバスの数本おきに1つGNDを配置、クロックや12V等のノイズが発生しやすい端子は端にまとめるなど、電気的によく考えられた構造になっている。
  - 筐体を開けずに抜き差しできるように[エッジ・コネクタ](https://ja.wikipedia.org/wiki/エッジ・コネクタ "wikilink")には引き抜き用のレバーが装着されている。

Cバスは、[サウンドカード](../Page/サウンドカード.md "wikilink")、[ビデオカード](../Page/ビデオカード.md "wikilink")、拡張メモリ、[TVチューナー](../Page/TVチューナー.md "wikilink")カード、[ビデオキャプチャカード](../Page/キャプチャ_\(録画ソフト\).md "wikilink")、[LANカード](../Page/Local_Area_Network.md "wikilink")、[MIDI](../Page/MIDI.md "wikilink")カード、MIDIインターフェースカード、[SCSIカード](../Page/Small_Computer_System_Interface.md "wikilink")、自作基板向けブランクボード、計測器用独自通信拡張カード、[NC加工](../Page/NC加工.md "wikilink")機制御用通信カードなどがあったが、いずれも転送速度の遅さ、さらに98自体の終焉により1990年代後半には減少し消滅した。電力供給には余裕があることから、小型[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")マザーボードなどをはじめ各種専用計算機などをCバスボードに実装した例は多い。

16bitバスであり、PC-9800シリーズで動作させた[Microsoft Windows NT](../Page/Microsoft_Windows_NT.md "wikilink")（[Windows 2000含む](../Page/Microsoft_Windows_2000.md "wikilink")）からは「[ISAバス](../Page/Industry_Standard_Architecture.md "wikilink")」と表示される場合もある。

| ピン  | 信号名      | ピン    | 信号名     |
| --- | -------- | ----- | ------- |
| A1  | GND      | B1    | GND     |
| A2  | V1       | B2    | V1      |
| A3  | V2       | B3    | V2      |
| A4  | AB001    | B4    | DB001   |
| A5  | AB011    | B5    | DB011   |
| A6  | AB021    | B6    | DB021   |
| A7  | AB031    | B7    | DB031   |
| A8  | AB041    | B8    | DB041   |
| A9  | AB051    | B9    | DB051   |
| A10 | AB061    | B10   | DB061   |
| A11 | GND      | B11   | GND     |
| A12 | AB071    | B12   | DB071   |
| A13 | AB081    | B13   | DB081   |
| A14 | AB091    | B14   | DB091   |
| A15 | AB101    | B15   | DB101   |
| A16 | AB111    | B16   | DB111   |
| A17 | AB121    | B17   | DB121   |
| A18 | AB131    | B18   | DB131   |
| A19 | AB141    | B19   | DB141   |
| A20 | AB151    | B20   | DB151   |
| A21 | GND      | B21   | GND     |
| A22 | AB161    | B22   | \+12V   |
| A23 | AB171    | B23   | \+12V   |
| A24 | AB181    | B24   | IR31    |
| A25 | AB191    | B25   | IR51    |
| A26 | AB201    | B26   | IR61    |
| A27 | AB211    | B27   | IR91    |
| A28 | AB221    | B28   | IR101   |
| A29 | AB231    | B29   | IR121   |
| A30 | INT0     | B30   | IR131   |
| A31 | GND      | B31   | GND     |
| A32 | IOCHK0   | B32   | \-12V   |
| A33 | IOR0     | B33   | \-12V   |
| A34 | IOW0     | B34   | RESET0  |
| A35 | MRC0     | B35   | DACK00  |
| A36 | MWC0     | B36   | DACK30  |
| A37 | INTA0    | S00   | B37     |
| A38 | NOWAIT0  | S01   | B38     |
| A39 | SALE1    | S02   | B39     |
| A40 | MACS0    | LOCK0 | B40     |
| A41 | GND      | B41   | GND     |
| A42 | CPUENB10 | B42   | EXHLA10 |
| A43 | RFSH0    | B43   | DMATC0  |
| A44 | BHE0     | B44   | NMI0    |
| A45 | IORDY1   | B45   | MWE0    |
| A46 | SCLK1    | B46   | EXHLA20 |
| A47 | S18CLK1  | B47   | EXHRQ20 |
| A48 | POWER0   | B48   | SBUSRQ1 |
| A49 | \+5V     | B49   | \+5V    |
| A50 | \+5V     | B50   | \+5V    |

PC-98 拡張スロット（Cバス） ピン配列

2項目あるうちの前者は80286以降搭載モデル、後者は8086/[V30](https://ja.wikipedia.org/wiki/V30 "wikilink")搭載モデルの場合。ただし過渡期モデルのPC-9801VX0/2/4（80286/V30切り替え）やVM21（V30搭載）では\#1だけが8086/V30仕様、\#2、\#3、\#4が80286以降仕様と、両方の仕様のCバススロットが搭載されている。それらのマイナーチェンジモデルであるPC-9801VX01/21/41（80286/V30切り替え）では80286以降仕様のCバスしか搭載されていない。例えば[PC-UXボードや](../Page/XENIX.md "wikilink")[68000ボードを使用する場合は](../Page/MC68000.md "wikilink")8086/V30仕様のCバスに装着する必要があり、CPUもV30以下でなければならない。

80286以降搭載モデルでは、AB191ピンは拡張スロット上のスイッチがオン時はバスのAB191信号そのまま、スイッチがオフ時はバスのAB201からAB231までのすべてが0かつAB191=1の場合のみハイになる。つまりこのスイッチ切り替えを含めれば上記8086/V30仕様のCバスと合わせて少なくとも3種類のCバス仕様が確認できることになる。PC-9821時代の後期の機種ではCバスの切り替えスイッチが省略されるケースもあり、該当機種では一番上のスロットでのスイッチが省略されていることが多い。ここには優先的にFDDインターフェースやPCカードスロットを増設するように指定されている。それら以外でスイッチを押す機構のないボードはスイッチ付きのスロットで使用するように指定されている。すなわちスイッチの省略されたスロットはスイッチが押された状態に相当する。

| グラウンド                                      | 電源および信号の0V基準       |
| ------------------------------------------ | ------------------ |
| 電源                                         | 電源ユニットから供給される電源    |
| 出力                                         | 拡張カードからマザーボードへの信号  |
| 入出力                                        | マザーボード・拡張カードの双方向信号 |
| 入力                                         | マザーボードから拡張カードへの信号  |
| [オープンコレクタ](../Page/オープンコレクタ.md "wikilink") | 拡張カード間で共有する信号線     |

色分け凡例

## 他の類似の拡張バス

  - 98NOTE用110ピン拡張バス - Cバスと増設用FDDの信号線が出力されている。[EPSONの98互換機の](../Page/EPSON_PCシリーズ.md "wikilink")[ノートタイプパソコンでも後期のもので採用されている](../Page/ノートパソコン.md "wikilink")（前期のものはEPSON独自のバス）。9821NOTEでは198ピンとなっているがオプションで110ピンに変換可能。
  - Lスロット - EPSON互換機のブック・ノートタイプパソコンに搭載された小型の拡張スロット。

[PCカード](../Page/PCカード.md "wikilink")スロットや[PCIスロットをCバスに変換するアダプタもサードパーティーから発売されていた](../Page/Peripheral_Component_Interconnect.md "wikilink")。

## 参考文献

  - PC-9801VM21ハードウエアマニュアル (NEC)
  - PC-9801VXハードウエアマニュアル (NEC)

## 関連項目

  - [98ローカルバス](../Page/98ローカルバス.md "wikilink") - PC-9821シリーズ(98MATE A)に搭載された32ビットバス。
  - [New Extend Standard Architecture](../Page/New_Extend_Standard_Architecture.md "wikilink") (NESA) - PC-H98シリーズに搭載された32ビットバス。
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI) - 9821シリーズ後期モデルに搭載された32ビットバス。
  - [Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA) - IBM PC/ATに搭載された8ビットまたは16ビットバス。

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink") [Category:日本電気のパーソナルコンピュータ](https://ja.wikipedia.org/wiki/Category:日本電気のパーソナルコンピュータ "wikilink")