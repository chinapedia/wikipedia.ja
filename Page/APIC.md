> この記事は[APIC](https://ja.wikipedia.org/wiki/APIC)から翻訳されています。


**APIC**（えいぴっく）は**Advanced Programmable Interrupt Controller**の略で、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")により開発された、[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャにおける[割り込みコントローラのことである](../Page/割り込み_\(コンピュータ\).md "wikilink")。

それまでのLegacyの割り込みコントローラとして知られる[PIC](https://ja.wikipedia.org/wiki/Programmable_Interrupt_Controller "wikilink") (Programmable Interrupt Controller) に対し、[マルチプロセッサ](https://ja.wikipedia.org/wiki/マルチプロセッサ "wikilink")対応、プライオリティ制御などの機能が付加されている。APICはインテルアーキテクチャの進歩と共に高機能化しており、いくつかのバージョンが存在する。

## 概要

APICには[CPU](../Page/CPU.md "wikilink")に内蔵される**Local APIC**と、I/Oからの割り込みを管理する**IOAPIC**の2種類が存在する。Local APICとIOAPICは独自のプロトコルで通信を行い、割り込みの通知を行う。[Pentium Pro世代では](../Page/Pentium_Pro.md "wikilink")、APIC Busと呼ばれる割り込み専用の[バスが使用されていたが](../Page/バス_\(コンピュータ\).md "wikilink")、[NetBurst](https://ja.wikipedia.org/wiki/NetBurst "wikilink")世代以降、APIC Busは廃止され、[FSBを介して割り込みの通知が行われる](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")。

### Local APIC

CPU内部に実装され、外部からの割り込みの全てを管理する。I/Oからの割り込み以外にもIPI (Inter-Processor Interrupt) と呼ばれる、マルチプロセッサによる割り込みを使用したCPU間通信にも使用される。

### IOAPIC

IOAPICはI/Oデバイスから受け取った割り込みを、CPUへ通知するためのリダイレクション･テーブルを持つ。

全てのI/O割り込みは一旦IOAPICで受信される。IOAPICは、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) や[BIOSによって適切に設定されたリダイレクション](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")･テーブルを参照し、それに従いCPUに割り込みの通知を行う。 リダイレクション･テーブルには、エッジ/レベル･トリガーの種別、割り込みベクタ（優先度）、割り込み先CPUなどの設定が可能である。

## 特徴

以下に、[PCIをI](../Page/Peripheral_Component_Interconnect.md "wikilink")/Oデバイスに持つ一般的な[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")アーキテクチャにおける、実装、割り込み時の振る舞いを例として解説する。

### 実装

PCIバスにおいては、1本のバスにはINT_A,B,C,Dの、最大4本のI/O割り込み線が存在し、それら割り込み線はIOAPICに接続される。IOAPICには、それぞれの割り込み線に対するリダイレクション･テーブルが割り当てられており、割り込み種別、割り込みベクタなど、CPUのLocal APICと通信を行うための設定がなされる。

I/Oデバイスの数が多い場合、4本の割り込み線では足りずに、1本の割り込み線を複数のI/Oデバイスで共有する場合がある。これらの管理もIOAPICが負っている。なお、IOAPICはシステムで複数存在していてもかまわない。

PCIのI/OデバイスによってはMSI () をサポートするものがあり、これらのデバイスは割り込み線を使用しないが、[チップセット](../Page/チップセット.md "wikilink")によりMSIメッセージは一旦IOAPICにルーティングされ、リダイレクション･テーブル介してからCPUへ割り込み通知される。

### 動作

IOAPICがPCIの割り込み信号の変化を検知すると、リダイレクション･テーブルに従い、CPUに対し割り込みメッセージを発行する。CPUのLocal APICがこれを受信すると、自CPUの割り込み処理の仕掛かり、優先度などをチェックし、[割り込みハンドラ](https://ja.wikipedia.org/wiki/割り込みハンドラ "wikilink")をコールする。 割り込みハンドラは、割り込みを発生させたI/Oデバイスをチェックし、割り込み信号通知を停止させ、それぞれの処理に入る。

一連の割り込み処理が完了すると、CPUはEOI (End of Interrupt)というコマンドをIOAPICに対して発行する。EOIには対応する割り込みベクタ情報が含まれており、IOAPICは、該当するベクタの割り込み処理が完了したことを認識する。 なおこの時、PCIデバイスより依然として当該割り込み信号による通知が行われている場合、即座に再度CPUに対して割り込みを発行する。 これらの一連の動作により、割り込みのロスト防止、割り込み線の共有制御などが行われる。

### プライオリティ制御

高い優先度の割り込み処理を実行しているCPUに対し、低い優先度の割り込みを通知しても、その処理は一旦待たされる。であれば、割り込み処理を行っていない、または低い優先度の割り込み処理を行っているCPUに割り込みを通知すべきである。

NetBurst世代後期のLocal APICには、割り込み処理に出入りするたびに、その割り込み優先度を、FSBを介して定期的にチップセットに通知する機能が実装されており、OSがこの機能を利用して、マルチプロセッサ・システムでの適切な割り込み分散が可能となっている。ただし、本機能に対応したIOAPICおよび、[ノースブリッジ](../Page/ノースブリッジ.md "wikilink")が必要とされる。

[Category:割り込み_(コンピュータ)](https://ja.wikipedia.org/wiki/Category:割り込み_\(コンピュータ\) "wikilink") [Category:マザーボード](https://ja.wikipedia.org/wiki/Category:マザーボード "wikilink") [Category:x86アーキテクチャ](https://ja.wikipedia.org/wiki/Category:x86アーキテクチャ "wikilink")