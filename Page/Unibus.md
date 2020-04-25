> この記事は[Unibus](https://ja.wikipedia.org/wiki/Unibus)から翻訳されています。


[Unibus.jpg](https://ja.wikipedia.org/wiki/File:Unibus.jpg "fig:Unibus.jpg")（左）とUnibus対応基板\]\] **Unibus**(ユニバス)は、[ディジタル・イクイップメント・コーポレーション](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")が製造した[PDP-11](../Page/PDP-11.md "wikilink")や初期の[VAX](../Page/VAX.md "wikilink")で使用された初期の[バス技術の一種](../Page/バス_\(コンピュータ\).md "wikilink")。

Unibusは72本の信号線から構成される(36本×2コネクタ)。電力供給線と接地線を除くと、56本の信号線から構成されている。[バックプレーン](../Page/バックプレーン.md "wikilink")やケーブルの形で存在する。ひとつのUnibusセグメントには最大20ノードのデバイスが接続可能で、セグメントとセグメントをバスリピーターで接続することもできる。

このバスは完全な非同期で、高速なデバイスと低速なデバイスの混在が可能である。バス調停(arbitration; 次のバスマスターを選択する動作)のオーバーラップが可能であり、現在のバスマスターが[データ転送](https://ja.wikipedia.org/wiki/データ転送 "wikilink")をしている間に調停を行うことができる。アドレス信号線は18本であり、[アドレス空間](../Page/アドレス空間.md "wikilink")は最大256Kバイトとなる。PDP-11アーキテクチャでは、先頭8Kバイトが[メモリマップされたI/Oデバイスのレジスタ用に予約されていた](https://ja.wikipedia.org/wiki/メモリマップドI/O "wikilink")。

システムが必要とする冗長な論理回路を最小限にするよう意図的に設計されている。例えば、スレーブデバイスはマスターデバイスよりも多いのが通例である。従って非同期データ転送を行うためのロジックは少数のマスターデバイスだけが持つようになっていた。[割り込みに関しては](../Page/割り込み_\(コンピュータ\).md "wikilink")、*Interrupt-fielding Processor*だけが複雑なタイミング回路を装備した。結果として多くのI/Oコントローラの回路は非常に単純化され、重要な回路はカスタム[集積回路](../Page/集積回路.md "wikilink")化された。

`18 A00-A17 - アドレス`
`16 D00-D15 - データ`
` 4 BR4-BR7 - バス(割り込み)要求、優先度 4(低)～7(高)`
` 4 BG4-BG7 - バス(割り込み)応答、優先度 4(低)～7(高)`
` 1 NPR     - 非プロセッサ要求(DMA)`
` 1 NPG     - 非プロセッサ応答(DMA)`
` 1 ACLO    - AC Low`
` 1 DCLO    - DC Low`
` 1 MSYNC   - Master Sync`
` 1 SSYNC   - Slave Sync`
` 1 BBSY    - Bus Busy`
` 1 SACK    - Selection Acknowledge`
` 1 INIT    - Bus Init`
` 1 INTR    - 割り込み要求`
` 1 PA      - パリティ制御`
` 1 PB      - パリティ制御`
` 2 C0-C1   - Cyce Control Lines:`
` 2 +5v     - 電源(56本の信号線には含まれない)`
`14 Gnd     - 接地(56本の信号線には含まれない)`

2本の制御線(C0とC1)は以下のような4種類のデータ転送サイクルを選択可能とした:

  - DATI (Data In、リード)
  - DATIP (Data In/Pause、リード-モディファイ-ライト操作([アトミック操作](https://ja.wikipedia.org/wiki/アトミック操作 "wikilink"))の開始、DATO か DATOB で完了させる)
  - DATO (Data Out、ワードライト)
  - DATOB (Data Out/Byte、バイトライト)
  - 割込みサイクルの間に、5番目の転送種別として、割り込み元デバイスから「割り込みベクター」を *Interrupt-fielding Processor* に伝える転送サイクルが自動的に実行される。

[Category:コンピュータバス](https://ja.wikipedia.org/wiki/Category:コンピュータバス "wikilink") [Category:ディジタル・イクイップメント・コーポレーション](https://ja.wikipedia.org/wiki/Category:ディジタル・イクイップメント・コーポレーション "wikilink")