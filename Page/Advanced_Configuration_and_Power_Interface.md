> この記事は[Advanced Configuration and Power Interface](https://ja.wikipedia.org/wiki/Advanced_Configuration_and_Power_Interface)から翻訳されています。


**Advanced Configuration and Power Interface**（アドバンスド・コンフィグレーション・アンド・パワー・インターフェイス、**ACPI**）は、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[東芝](../Page/東芝.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が共同で作り上げた、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")等の[電源](../Page/電源.md "wikilink")[制御](https://ja.wikipedia.org/wiki/制御 "wikilink")と構成要素に関する公開された統一規格である。ACPI2.0（[2000年](../Page/2000年.md "wikilink")8月に公開）からはさらに[コンパック](../Page/コンパック.md "wikilink")（現[ヒューレットパッカード](https://ja.wikipedia.org/wiki/ヒューレットパッカード "wikilink")）、[フェニックステクノロジーズ](https://ja.wikipedia.org/wiki/フェニックステクノロジーズ "wikilink")が主な開発団体として参加している。

## 概要

ACPIは電源管理のための枠組であるだけではなく、[プラットフォームの構成要素を列挙し管理する統一された枠組でもあり](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、プラットフォームの電源管理を行う[APMのみならず](../Page/Advanced_Power_Management.md "wikilink")、[マザーボード](../Page/マザーボード.md "wikilink")上の[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")を列挙する[PnPBIOS](https://ja.wikipedia.org/wiki/PnPBIOS "wikilink"),[マルチプロセッサの列挙を行う](../Page/マルチプロセッシング.md "wikilink")[MPTable](https://ja.wikipedia.org/wiki/MPTable "wikilink")等をも統一した形で置き換えるものである。これらは[BIOS主導の管理方式だったが](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、ACPIは[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")主導の管理を実現し、システム全体の電源管理だけでなく緻密な[デバイス](https://ja.wikipedia.org/wiki/デバイス "wikilink")の電源をも含めた管理に加え、温度管理や[スタンバイ](https://ja.wikipedia.org/wiki/スタンバイ "wikilink")（サスペンド）、[冷却ファン制御など](../Page/CPUの冷却装置.md "wikilink")、さまざまな機能を提供する。また、マルチプロセッサや[16ビット](../Page/16ビット.md "wikilink")コードの呼び出しにくい[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")のプロセッサ、[CPU](../Page/CPU.md "wikilink")の速度制御も可能になり、最近では[ノートパソコン](../Page/ノートパソコン.md "wikilink")だけでなく[デスクトップや](../Page/デスクトップパソコン.md "wikilink")[ワークステーション](../Page/ワークステーション.md "wikilink")、[サーバ](../Page/サーバ.md "wikilink")に関しても使用される局面が多くなった。

必要の無いデバイスへの電源供給を停止したり、使用しないときは自動的にスタンバイ（サスペンド）したりすることにより[消費電力](https://ja.wikipedia.org/wiki/消費電力 "wikilink")を抑えられる。これによりノートパソコンでは[バッテリーの持続時間が飛躍的に長くなった](../Page/電池.md "wikilink")。

実装の複雑さ、およびオペレーティングシステムとの[競合で問題が出やすいため](../Page/競合状態.md "wikilink")、最近では[APMをサポートせずACPIのみのBIOSが増えてきている](../Page/Advanced_Power_Management.md "wikilink")。

## 構成要素

ACPIは**ACPI ハードウエアレジスタ**・**ACPI BIOS**・**ACPI テーブル**および**ACPI Machine Language** (**AML**) の構成要素を持つ。

  - ACPI BIOS
    ACPI テーブルを初期化し、OS起動後は必要とされる機会は少ないが（[IA-32](../Page/IA-32.md "wikilink")の場合は[システムマネジメントモード](../Page/システムマネジメントモード.md "wikilink")を通すことにより）必要に応じて動作する。APMとは違い、電源イベントは主にオペレーティングシステム側に見える割り込みとして伝わって来る。メモリマップ取得BIOSコールInt 15H AX=E820HはOSが後述のACPIテーブルを意識せずに書き潰さないようにするために、ACPIのテーブル等を含むメモリをOSに通知する必要がある。
  - ACPI テーブル
    メモリ ([RAM](../Page/Random_Access_Memory.md "wikilink")) 上に置かれたデータ構造で、システムの初期化に必要なデータが拡張性の高い形で並べられている。 大きな構造は、下位1MBの16ビットモードからもアクセス可能ないわゆるBIOSエリア等の何処かに16バイト整列されたRSDP (Root System Description Pointer) と呼ばれる構造体がある。RSDPは、RSDT (Root System Description Table) もしくはXSDT (eXtended System Description Table) と呼ばれるメモリ構造を指す。RSDTは様々なテーブルへのポインタを含み、XSDTはその64ビットメモリ空間対応版である。それに含まれているテーブルで最も重要なものはFixed ACPI Control Pointer (FACP) またはFixed ACPI Description Table (FADT)と呼ばれるポインタで、ここにACPIハードウエアレジスタの位置や、FACS (Firmware ACPI Control Structure) と呼ばれるBIOSとの排他制御やサスペンドリジューム時にBIOSとのやりとりに使うメモリの位置、そしてDifferentiated System Description Table (DSDT) と呼ばれる後述のAML (ACPI Machine Language) で記述されたシステム上のデバイス等の情報の入ったメモリブロックの位置を指し示す。非常に柔軟なので基本的には以上に挙げたもので必要な情報はほぼ記述可能であるが、DSDTの解釈は[オーバーヘッド](https://ja.wikipedia.org/wiki/オーバーヘッド "wikilink")が大きく、[ブート](../Page/ブート.md "wikilink")の初期に必要なもの等に関してはRSDTもしくはXSDTの他のエントリを使って特別に記述されているものがある。RSDP以外のメモリブロックは、（PCの場合のBIOS呼出Int15H AX=E820Hのような）システムのメモリマップ取得で予約される領域に置かれ、英文字4文字の[シグネチャ](https://ja.wikipedia.org/wiki/シグネチャ "wikilink")を持つ。

<!-- end list -->

  -
    XSDTに置かれることのある他のテーブルをシグネチャとともにACPI spec 4.0bから列挙する 。
      - SSDT (SSDT : Secondary System Description Table)
        DSDTの補足として使われるAMLで記述されたデバイスなどの情報。
      - APIC (MADT : Multiple Apic Description Table)
        システムにある[APIC](../Page/APIC.md "wikilink")の情報を記述したテーブル。MPTablesと同等の情報を提供するが、より高機能で[ハイパースレッディング](https://ja.wikipedia.org/wiki/ハイパースレッディング "wikilink")対応した機械の場合必ず存在する。
      - ECDT (ECDT : Embedded Controller Description Table)
        エンベデッドコントローラデバイスの（使用I/Oポート等の）情報を記述したテーブル。DSDT内でもデバイスとして定義されており、ACPI1.0の頃はこのテーブルは定義されていなかったが、他のACPIのデバイス記述がこれによってアクセス可能なリソースを使用するため初期化順の解決が困難であった。
      - TCPA (Trusted Computing Platform Alliance Capability Table)
        [トラステッド・コンピューティング・グループ](https://ja.wikipedia.org/wiki/トラステッド・コンピューティング・グループ "wikilink")によって定義されたメモリテーブルで、ブートシーケンスの妥当性を検証するためのデータへのポインタを含むテーブル。
      - MCFG (PCI Express memory mapped configuration space base address Description Table)
        [PCI Expressのアクセスメモリ空間の場所](../Page/PCI_Express.md "wikilink")、バス番号の範囲などを示すテーブル。
    等のようなものがある。
  - AML
    プラットホームから独立した[中間言語](../Page/中間言語.md "wikilink")列で**ACPI Source Language** (**ASL**) から生成され、これをオペレーティングシステムが解釈することで、高度な機能を実現する。[木構造の](../Page/木構造_\(データ構造\).md "wikilink")[名前空間](../Page/名前空間.md "wikilink")や[サブルーチン](../Page/サブルーチン.md "wikilink")呼出や繰り返しなどの[制御構造](../Page/制御構造.md "wikilink")を持ち、デバイスはその木構造の名前空間の中にある[オブジェクトとして表現され](../Page/オブジェクト_\(プログラミング\).md "wikilink")、その識別の枠組に関しては、使用される識別用IDや、使用リソースの記述に使われるデータ構造等の点でPnPBIOSの特徴を受け継いでいる。
    このように、[高級言語](https://ja.wikipedia.org/wiki/高級言語 "wikilink")により、OSの[ブート](../Page/ブート.md "wikilink")に使われる構成情報を記述するものに[Open Firmwareがあるが](../Page/Open_Firmware.md "wikilink")、Open Firmwareと違い、解釈を行うのはOSのコンテクストであり[インタプリタ](../Page/インタプリタ.md "wikilink")をOSに内蔵する必要がある。

## システムスリープ状態

システム[スリープ状態はS](https://ja.wikipedia.org/wiki/スリープ_\(コンピュータ\) "wikilink")0・S0ix・S1・S2・S3・S4・S5の7状態が定義されており、深いスリープ状態ほど復帰への時間がかかるが、待機時の電力消費は少ない（なお、直接の関係は無いが、アイドル時のプロセッサのスリープ状態Cxやデバイスのスリープ状態Dxというものも別に定義されている）。

  - S0
    通常の運用状態。
  - S0ix
    Modern Standby\[1\]。
  - S1
    スタンバイとよばれるメモリ、デバイス、レジスタコンテクストおよびキャッシュコンテクストをCPUが保持したまま割り込み等を止め、低消費電力状態に移行する状態である。タイマの復帰などを電源管理イベントとして扱い処理する程度で矛盾無く復帰可能である。
  - S2
    デバイスなどのコンテクストが保存されているのはS1と同様であるが、レジスタコンテクストとキャッシュコンテクストが失われているためS3と同様の方式で復帰する必要がある（ほとんど実装されている事例を見ない）。
  - S3
    Suspend to RAMまたは[スリープと呼ばれる状態で](https://ja.wikipedia.org/wiki/スリープ_\(コンピュータ\) "wikilink")、メモリは保持されているが、チップセットの情報やレジスタコンテクストが失われる。サスペンドに入る前にOSはレジスタコンテクストをメモリに書き出し、16ビットコードの復帰ベクタをFACSの然るべき場所に書いておく。復帰はリセット状態から復帰し、BIOSがサスペンド状態であったことを検知して初期化を行った後復帰ベクタへ移行する。その後復帰ベクタから[プロテクトモード](../Page/プロテクトモード.md "wikilink")への復帰などを行って最終的にレジスタを書き戻して運用状態に復帰する。
  - S4
    Suspend to Diskまたは[ハイバネーション](https://ja.wikipedia.org/wiki/ハイバネーション "wikilink")と呼ばれる状態で、メモリ内容も失われる。メモリをディスクに書き出し、電源断状態にするのと同じである。初期は書き出し復帰はBIOSが行う事もあり、その場合の処理はS1やS3等と同等だったが、OSが行う場合は復帰時はブートローダやOSがハイバネーション内容が存在することを検出してメモリ内容を書き戻すことになる。
  - S5
    完全なる電源断である。[商用電源](https://ja.wikipedia.org/wiki/商用電源 "wikilink")あるいは[無停電電源装置](../Page/無停電電源装置.md "wikilink")から電力を全く消費しない状態。

## サポートされるプラットフォーム

いわゆる[AT互換機](https://ja.wikipedia.org/wiki/AT互換機 "wikilink")[アーキテクチャの他に](../Page/コンピュータ・アーキテクチャ.md "wikilink")[AMD64や](https://ja.wikipedia.org/wiki/x64 "wikilink")[IA-64](../Page/IA-64.md "wikilink")を使用したシステムで使用されている。特にIA-64上のOSではACPIサポートは必須の要件となっている。その上で動くOSでは[Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Windows 98から](../Page/Microsoft_Windows_98.md "wikilink")、[Linux](../Page/Linux.md "wikilink")では（開発バージョンの）2.3.19から[FreeBSD](../Page/FreeBSD.md "wikilink")では5-CURRENTからACPIが利用できるようになったが、管理対象となるデバイス全てがACPIをサポートしていないと不具合が出ることがある。ACPI 3.0の規格書の\\_OSIオブジェクトの記述から読み取れる通りこの他にIA-64上の[HP-UX](../Page/HP-UX.md "wikilink")、[OpenVMS](../Page/OpenVMS.md "wikilink")でもサポートされている。

LinuxやFreeBSDや[NetBSD](../Page/NetBSD.md "wikilink")ではインテルによって開発及び保守されている**ACPI Component Architecture**(**ACPI-CA**) と呼ばれるカーネル内コンテキストで動作するライブラリを使用して実装されている。

## 歴史

1997年に初めて仕様が公開された\[2\]。ACPI 2.0は2000年にリリースされ、ACPI 3.0は2004年にリリースされ、ACPI 4.0は2009年にリリースされ、ACPI 5.0は2011年にリリースされた。2013年10月、ACPIは[Unified EFI Forumの下に置かれ](https://ja.wikipedia.org/wiki/Unified_EFI_Forum "wikilink")、新しいACPI仕様はUEFI Forumによって開発される。

## 脚注

## 関連項目

  - [Advanced Power Management](../Page/Advanced_Power_Management.md "wikilink") (APM)
  - [System Management BIOS](../Page/SMBIOS.md "wikilink")（SMBIOS）
  - [Basic Input/Output System](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")（BIOS）
  - [Unified Extensible Firmware Interface](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")（UEFI）
  - [Hardware Abstraction Layer](../Page/Hardware_Abstraction_Layer.md "wikilink")
  - [ハイバネーション](https://ja.wikipedia.org/wiki/ハイバネーション "wikilink")
  - [スリープ (コンピュータ)](https://ja.wikipedia.org/wiki/スリープ_\(コンピュータ\) "wikilink")

## 外部リンク

  - [公式Webページ](http://www.acpi.info/)
  - [ACPI-CA](http://www.acpica.org/)

[Category:ファームウェア](https://ja.wikipedia.org/wiki/Category:ファームウェア "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:システム管理](https://ja.wikipedia.org/wiki/Category:システム管理 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.