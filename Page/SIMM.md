> この記事は[SIMM](https://ja.wikipedia.org/wiki/SIMM)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:SIMM-muistikampoja.jpg "wikilink") **SIMM**（しむ、*' Single In-line Memory Module*' ）とは、[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")で [RAM](../Page/Random_Access_Memory.md "wikilink") として使われるメモリモジュールの一種である。現在主流である [DIMM](https://ja.wikipedia.org/wiki/DIMM "wikilink") とは異なり、SIMM の接点はモジュールの両面で[冗長化](../Page/冗長化.md "wikilink")されている。

最も初期の PC マザーボード（[8088](../Page/Intel_8088.md "wikilink") ベースの PC や [XT](https://ja.wikipedia.org/wiki/PC/AT#PC_XT "wikilink") など）では、[DIP](https://ja.wikipedia.org/wiki/DIP "wikilink") チップをソケットに嵌め込むようになっていた。[80286](../Page/Intel_80286.md "wikilink") ベースの [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink") では記憶量が大幅に増え、[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")のスペースを節約したり簡単にメモリ増設できるように、メモリモジュールが使われるようになった。メモリを増やすには、それまでは 8個か9個の [DRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink") チップを挿し込まねばならなかったのが、メモリモジュールを1枚追加するだけで済むようになった。80286 ベースのコンピュータの中には（非標準の）SIPP (single in-line pin package) メモリモジュールを使うものもあったが、SIPP の 30本のピンが挿入時に折れたり壊れたりすることが多かったため、ピンではなく接点プレートを採用している SIMM への置き換えが急速に進んだ。

SIMM を考案したのは [IBM](../Page/IBM.md "wikilink") に在籍していた Skip Coppola で、[1980年代](../Page/1980年代.md "wikilink")中頃の [PS/2](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink") で初めて採用された。これにより、いくつかの問題が解決された。例えば、マザーボードの面積の問題（チップをソケットに取り付けるよりも、占有面積が遥かに少なくて済む）や、メモリ容量の急激な進化の問題（特定の RAM チップに対応するソケットを備えたマザーボードは、すぐに時代遅れとなる）である。また、メーカー（この場合は IBM）が RAM チップを調達するのに、そのベンダーが変わったり、チップのパッケージが変わったりしても、中間基板である SIMM で互換性を保つことができる。 SIMM基板の製造は、IBMの他に[キングストンテクノロジー](https://ja.wikipedia.org/wiki/キングストンテクノロジー "wikilink")などがいち早く参入した。

初期の SIMM は、30ピンの8[ビット](../Page/ビット.md "wikilink") データ（[パリティ付きでは](https://ja.wikipedia.org/wiki/パリティビット "wikilink") 9ビット）だった。[MC68040](https://ja.wikipedia.org/wiki/MC68040 "wikilink") や [80486](../Page/Intel486.md "wikilink") のようなプロセッサでは[32ビット](https://ja.wikipedia.org/wiki/32ビット "wikilink")データバスのため、30ピンの SIMM を使うマザーボードであれば 4枚セットでインストールする必要があった。

二世代目の SIMM は、72ピンの 32ビットデータ（パリティ付きでは36ビット）で、[1990年代](../Page/1990年代.md "wikilink")の前半頃に 30ピン SIMM から 72ピン SIMM へ移行した。

[Macintosh IIfx](https://ja.wikipedia.org/wiki/Macintosh_IIfx "wikilink") では、非標準の 64ピン SIMM が使われていた。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Atari_STE_256kB_RAM_2.jpg "wikilink") 前述のようにデータバス幅がメモリモジュールとプロセッサで異なっている場合には、同じペアもしくは4枚のモジュールでメモリバンクを埋めなければならないことがある。例えば、データバス幅が32ビットの [80386](../Page/Intel_80386.md "wikilink") や [80486](../Page/Intel486.md "wikilink") のシステムでは、1つのメモリバンクに対して 30ピン SIMM を4枚か、72ピン SIMM を1枚が必要となる。データバス幅が[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")の [Pentium](../Page/Intel_Pentium_\(1993年\).md "wikilink") システムや [PowerPC](../Page/PowerPC.md "wikilink") システムでは、72ピン SIMM が2枚必要である。これは[メモリコントローラ](https://ja.wikipedia.org/wiki/メモリコントローラ "wikilink")の仕様に依存するため、製品によっては例外もある。

初期の SIMM ソケットは、従来からあった挿し込み型のソケットだった。しかし、すぐに、挿し込んでから回転させてロックする ZIF ソケット ([Zero insertion force](https://ja.wikipedia.org/wiki/:en:Zero_insertion_force "wikilink")) が使われるようになった。SIMM を取り付ける場合、ある角度でソケットに置いて、所定の位置まで回転させる。取り外す場合は、両端にある金属またはプラスチック製のクリップを横に動かしてロックを外し、SIMM を傾けて引っ張り出す。初期のソケットではプラスチック製のクリップが使われていたが、これは壊れやすかったため、金属製クリップも使われるようになった。しかし安価なプラスチック製クリップのソケットも製品によっては使われ続けた。

SIMM 上の [DRAM](../Page/Dynamic_Random_Access_Memory.md "wikilink") には、[EDO](https://ja.wikipedia.org/wiki/Dynamic_Random_Access_Memory#EDO_DRAM "wikilink") (Extended Data Out) や [FPM](https://ja.wikipedia.org/wiki/Dynamic_Random_Access_Memory#高速ページモード付きDRAM "wikilink") (Fast Page Mode) が使われている。

SIMM は、[JEDEC](https://ja.wikipedia.org/wiki/JEDEC "wikilink") の JESD-21C で標準化されている。

## 代表的なメモリサイズ

  - 30ピン SIMM : 256KB, 1MB, 4MB, 16MB
    72ピン SIMM : 1MB, 2MB, 4MB, 8MB, 16MB, 32MB, 64MB, 128MB

## ピン配列

| ピン番号 | 名称             | 信号                     |
| ---- | -------------- | ---------------------- |
| 1    | V<sub>CC</sub> | \+5VDC                 |
| 2    | CAS            | Column Address Strobe  |
| 3    | DQ1            | Data 0                 |
| 4    | A0             | Address 0              |
| 5    | A1             | Address 1              |
| 6    | DQ2            | Data 1                 |
| 7    | A2             | Address 2              |
| 8    | A3             | Address 3              |
| 9    | V<sub>SS</sub> | Ground                 |
| 10   | DQ3            | Data 2                 |
| 11   | A4             | Address 4              |
| 12   | A5             | Address 5              |
| 13   | DQ4            | Data 3                 |
| 14   | A6             | Address 6              |
| 15   | A7             | Address 7              |
| 16   | DQ5            | Data 4                 |
| 17   | A8             | Address 8              |
| 18   | A9             | Address 9              |
| 19   | A10            | Address 10             |
| 20   | DQ6            | Data 5                 |
| 21   | W              | Write Enable           |
| 22   | V<sub>SS</sub> | Ground                 |
| 23   | DQ7            | Data 6                 |
| 24   | NC             | No Internal Connection |
| 25   | DQ8            | Data 7                 |
| 26   | NC             | No Internal Connection |
| 27   | RAS            | Row Address Strobe     |
| 28   | NC             | No Internal Connection |
| 29   | NC             | No Internal Connection |
| 30   | V<sub>CC</sub> | \+5VDC                 |

30ピン SIMM メモリモジュール

| ピン番号 | パリティ無し         | パリティ付き         | 信号                      |
| ---- | -------------- | -------------- | ----------------------- |
| 1    | V<sub>SS</sub> | V<sub>SS</sub> | Ground                  |
| 2    | DQ0            | DQ0            | Data 0                  |
| 3    | DQ1            | DQ1            | Data 1                  |
| 4    | DQ2            | DQ2            | Data 2                  |
| 5    | DQ3            | DQ3            | Data 3                  |
| 6    | DQ4            | DQ4            | Data 4                  |
| 7    | DQ5            | DQ5            | Data 5                  |
| 8    | DQ6            | DQ6            | Data 6                  |
| 9    | DQ7            | DQ7            | Data 7                  |
| 10   | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                 |
| 11   | PD1            | PD1            | Presence Detect 1       |
| 12   | A0             | A0             | Address 0               |
| 13   | A1             | A1             | Address 1               |
| 14   | A2             | A2             | Address 2               |
| 15   | A3             | A3             | Address 3               |
| 16   | A4             | A4             | Address 4               |
| 17   | A5             | A5             | Address 5               |
| 18   | A6             | A6             | Address 6               |
| 19   | A10            | A10            | Address 10              |
| 20   | n/c            | PQ8            | Data 8 (Parity 1)       |
| 21   | DQ9            | DQ9            | Data 9                  |
| 22   | DQ10           | DQ10           | Data 10                 |
| 23   | DQ11           | DQ11           | Data 11                 |
| 24   | DQ12           | DQ12           | Data 12                 |
| 25   | DQ13           | DQ13           | Data 13                 |
| 26   | DQ14           | DQ14           | Data 14                 |
| 27   | DQ15           | DQ15           | Data 15                 |
| 28   | A7             | A7             | Address 7               |
| 29   | A11            | A11            | Address 11              |
| 30   | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                 |
| 31   | A8             | A8             | Address 8               |
| 32   | A9             | A9             | Address 9               |
| 33   | /RAS3          | RAS3           | Row Address Strobe 3    |
| 34   | /RAS2          | RAS2           | Row Address Strobe 2    |
| 35   | DQ16           | DQ16           | Data 16                 |
| 36   | n/c            | PQ17           | Data 17 (Parity 2)      |
| 37   | DQ18           | DQ18           | Data 18                 |
| 38   | DQ19           | DQ19           | Data 19                 |
| 39   | V<sub>SS</sub> | V<sub>SS</sub> | Ground                  |
| 40   | /CAS0          | CAS0           | Column Address Strobe 0 |
| 41   | /CAS2          | CAS2           | Column Address Strobe 2 |
| 42   | /CAS3          | CAS3           | Column Address Strobe 3 |
| 43   | /CAS1          | CAS1           | Column Address Strobe 1 |
| 44   | /RAS0          | RAS0           | Row Address Strobe 0    |
| 45   | /RAS1          | RAS1           | Row Address Strobe 1    |
| 46   | A12            | A12            | Address 12              |
| 47   | /WE            | WE             | Read/Write              |
| 48   | A13            | A13            | Address 13              |
| 49   | DQ20           | DQ20           | Data 20                 |
| 50   | DQ21           | DQ21           | Data 21                 |
| 51   | DQ22           | DQ22           | Data 22                 |
| 52   | DQ23           | DQ23           | Data 23                 |
| 53   | DQ24           | DQ24           | Data 24                 |
| 54   | DQ25           | DQ25           | Data 25                 |
| 55   | n/c            | PQ26           | Data 26 (Parity 3)      |
| 56   | DQ27           | DQ27           | Data 27                 |
| 57   | DQ28           | DQ28           | Data 28                 |
| 58   | DQ29           | DQ29           | Data 29                 |
| 59   | DQ31           | DQ31           | Data 31                 |
| 60   | DQ30           | DQ30           | Data 30                 |
| 61   | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                 |
| 62   | DQ32           | DQ32           | Data 32                 |
| 63   | DQ33           | DQ33           | Data 33                 |
| 64   | DQ34           | DQ34           | Data 34                 |
| 65   | n/c            | PQ35           | Data 35 (Parity 4)      |
| 66   | PD2            | PD2            | Presence Detect 2       |
| 67   | PD3            | PD3            | Presence Detect 3       |
| 68   | PD4            | PD4            | Presence Detect 4       |
| 69   | PD5            | PD5            | Presence Detect 1       |
| 70   | PD6            | PD6            | Presence Detect 6       |
| 71   | PD7            | PD7            | Presence Detect 7       |
| 72   | V<sub>SS</sub> | V<sub>SS</sub> | Ground                  |

72ピン ECC SIMM メモリモジュール

| ピン番号 | パリティ無し         | パリティ付き         | 信号                       |
| ---- | -------------- | -------------- | ------------------------ |
| 1    | V<sub>SS</sub> | V<sub>SS</sub> | Ground                   |
| 2    | DQ0            | DQ0            | Data 0                   |
| 3    | DQ16           | DQ18           | Data 16 / Data 18        |
| 4    | DQ1            | DQ1            | Data 1                   |
| 5    | DQ17           | DQ19           | Data 17 / Data 19        |
| 6    | DQ2            | DQ2            | Data 2                   |
| 7    | DQ18           | DQ20           | Data 18 / Data 20        |
| 8    | DQ3            | DQ3            | Data 3                   |
| 9    | DQ19           | DQ21           | Data 19 / Data 21        |
| 10   | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                  |
| 11   | n/c            | n/c            |                          |
| 12   | A0             | A0             | Address 0                |
| 13   | A1             | A1             | Address 1                |
| 14   | A2             | A2             | Address 2                |
| 15   | A3             | A3             | Address 3                |
| 16   | A4             | A4             | Address 4                |
| 17   | A5             | A5             | Address 5                |
| 18   | A6             | A6             | Address 6                |
| 19   | A10            | A10            | Address 10               |
| 20   | DQ4            | DQ4            | Data 4                   |
| 21   | DQ20           | DQ22           | Data 20 /Data 22         |
| 22   | DQ5            | DQ5            | Data 5                   |
| 23   | DQ21           | DQ23           | Data 21 / Data 23        |
| 24   | DQ6            | DQ6            | Data 6                   |
| 25   | DQ22           | DQ24           | Data 22 / Data 24        |
| 26   | DQ7            | DQ7            | Data 7                   |
| 27   | DQ23           | DQ25           | Data 23 / Data 25        |
| 28   | A7             | A7             | Address 7                |
| 29   | A11            | A11            | Address 11               |
| 30   | V<sub>CC</sub> | V<sub>CC</sub> | \+5 VDC                  |
| 31   | A8             | A8             | Address 8                |
| 32   | A9             | A9             | Address 9                |
| 33   | /RAS3          | /RAS3          | Row Address Strobe 3     |
| 34   | /RAS2          | /RAS2          | Row Address Strobe 2     |
| 35   | n/c            | DQ26           | n/c / Data 26 (Parity 3) |
| 36   | n/c            | DQ8            | n/c / Data 8 (Parity 1)  |
| 37   | n/c            | DQ17           | n/c / Data 17 (Parity 2) |
| 38   | n/c            | DQ35           | n/c / Data 35 (Parity 4) |
| 39   | V<sub>SS</sub> | V<sub>SS</sub> | Ground                   |
| 40   | /CAS0          | /CAS0          | Column Address Strobe 0  |
| 41   | /CAS2          | /CAS2          | Column Address Strobe 2  |
| 42   | /CAS3          | /CAS3          | Column Address Strobe 3  |
| 43   | /CAS1          | /CAS1          | Column Address Strobe 1  |
| 44   | /RAS0          | /RAS0          | Row Address Strobe 0     |
| 45   | /RAS1          | /RAS1          | Row Address Strobe 1     |
| 46   | A12            | A12            | Address 12               |
| 47   | /WE            | /WE            | Read/Write               |
| 48   | A13            | A13            | Address 13               |
| 49   | DQ8            | DQ9            | Data 8 / Data 9          |
| 50   | DQ24           | DQ27           | Data 24 / Data 27        |
| 51   | DQ9            | DQ10           | Data 9 / Data 10         |
| 52   | DQ25           | DQ28           | Data 25 / Data 28        |
| 53   | DQ10           | DQ11           | Data 10 / Data 11        |
| 54   | DQ26           | DQ29           | Data 26 / Data 29        |
| 55   | DQ11           | DQ12           | Data 11 / Data 12        |
| 56   | DQ27           | DQ30           | Data 27 / Data30         |
| 57   | DQ12           | DQ13           | Data 12 / Data 13        |
| 58   | DQ28           | DQ31           | Data 28 / Data 31        |
| 59   | V<sub>CC</sub> | V<sub>CC</sub> |                          |
| 60   | DQ29           | DQ32           | Data 29 / Data 32        |
| 61   | DQ13           | DQ14           | Data 13 / Data 14        |
| 62   | DQ30           | DQ33           | Data 30 / Data 33        |
| 63   | DQ14           | DQ15           | Data 14 / Data 15        |
| 64   | DQ31           | DQ34           | Data 31 / Data 34        |
| 65   | DQ15           | DQ16           | Data 15 / Data 16        |
| 66   | n/c            | n/c            |                          |
| 67   | PD0            | PD0            | Presence Detect 0        |
| 68   | PD1            | PD1            | Presence Detect 1        |
| 69   | PD2            | PD2            | Presence Detect 2        |
| 70   | PD3            | PD3            | Presence Detect 3        |
| 71   | n/c            | n/c            |                          |
| 72   | V<sub>SS</sub> | V<sub>SS</sub> | Ground                   |

72ピン ECC無し SIMM メモリモジュール

## 関連項目

  - [コンピュータ略語一覧](../Page/コンピュータ略語一覧.md "wikilink")
  - [転送速度](https://ja.wikipedia.org/wiki/転送速度 "wikilink")

### 類似の他種

  - [DIMM](https://ja.wikipedia.org/wiki/DIMM "wikilink") (Dual in-line memory module)
  - [RDRAM](https://ja.wikipedia.org/wiki/RDRAM "wikilink") (Rambus Dynamic Random Access Memory)

## 外部リンク

  - [General SIMM Installation Guide](http://www.edgetechcorp.com/support/installation-manuals/1000%20General%20SIMM%20Ver2\(09-04\).pdf)

[Category:半導体メモリ](https://ja.wikipedia.org/wiki/Category:半導体メモリ "wikilink")