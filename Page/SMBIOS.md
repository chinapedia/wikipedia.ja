> この記事は[SMBIOS](https://ja.wikipedia.org/wiki/SMBIOS)から翻訳されています。


**SMBIOS**（System Management BIOS）とは、[BIOS内のデータ構造の配置](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")（およびそのアクセスメソッド）に関する仕様である。SMBIOSにより、その[PCに固有の情報をユーザやアプリケーションが格納したり使用したりすることができる](../Page/パーソナルコンピュータ.md "wikilink")。1999年ごろ、[Distributed Management Task Force](../Page/Distributed_Management_Task_Force.md "wikilink")（DMTF）がSMBIOSを扱うようになった。それ以前は、SMBIOSは[Desktop Management Interface](../Page/Desktop_Management_Interface.md "wikilink")（DMI）の一部として知られていた。ほぼ同じ時期に[マイクロソフト](../Page/マイクロソフト.md "wikilink")社は[OEM](../Page/OEM.md "wikilink")各社とBIOSベンダー各社に対して認定を受ける際にSMBIOS情報（インタフェースとデータ）を提供するよう要求している。

2019年現在、DMTFがリリースしている最新の仕様は2019年8月22日のバージョン3.3である。

## Structure Type

バージョン2.7.1のSMBIOS仕様では、以下のStructure Typeを定義している。

| Type    | 説明                                     |
| ------- | -------------------------------------- |
| 0       | BIOS情報                                 |
| 1       | システム情報                                 |
| 2       | 基板（またはモジュール）情報                         |
| 3       | 筐体                                     |
| 4       | プロセッサ情報                                |
| 5       | メモリコントローラ情報 (Obsolete)                 |
| 6       | メモリモジュール情報 (Obsolete)                  |
| 7       | キャッシュ情報                                |
| 8       | ポートコネクタ情報                              |
| 9       | システムスロット                               |
| 10      | オンボード・デバイス情報                           |
| 11      | OEM文字列                                 |
| 12      | システム構成オプション                            |
| 13      | BIOS言語情報                               |
| 14      | structureのグループ化                        |
| 15      | システムイベントログ                             |
| 16      | 物理メモリアレイ                               |
| 17      | メモリデバイス                                |
| 18      | 32ビット・メモリエラー情報                         |
| 19      | メモリアレイの配置アドレス                          |
| 20      | メモリデバイスの配置アドレス                         |
| 21      | 組み込みポインティングデバイス                        |
| 22      | 可搬バッテリ                                 |
| 23      | システムリセット                               |
| 24      | ハードウェアセキュリティ                           |
| 25      | システム電源制御                               |
| 26      | 電圧プローブ                                 |
| 27      | 冷却デバイス                                 |
| 28      | 温度プローブ                                 |
| 29      | 電流プローブ                                 |
| 30      | 帯域外遠隔アクセス                              |
| 31      | Boot Integrity Services (BIS) エントリポイント |
| 32      | システムブート情報                              |
| 33      | 64ビット・メモリエラー情報                         |
| 34      | 管理デバイス                                 |
| 35      | 管理デバイス装置                               |
| 36      | 管理デバイスしきい値データ                          |
| 37      | メモリチャネル                                |
| 38      | IPMI デバイス情報                            |
| 39      | システム電源                                 |
| 40      | 追加情報                                   |
| 41      | オンボードデバイス拡張情報                          |
| 42      | 管理コントローラ・ホストインタフェース                    |
| 126     | 不活性                                    |
| 127     | テーブル終端                                 |
| 128-255 | システム固有またはOEM固有の情報を追加可能                 |

## SMBIOSデータへのアクセス

### Linux

[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")にはSMBIOSデコーダがあり、SMBIOS情報に基づいてシステム管理者が特定のワークアラウンドの有効/無効を設定できる。ユーザ空間のコマンド行ユーティリティ \[1\] を使えばSMBIOSデータを見ることができる。

### Windows

[WMIを使えば](../Page/Windows_Management_Instrumentation.md "wikilink")、Windows上でSMBIOS情報にアクセスできる\[2\]。XPおよびそれ以降でサポートしている。一部のSMBIOS情報はコマンドプロンプトでWMICコマンドを使って表示することができ、[レジストリ](../Page/レジストリ.md "wikilink")にも同様の情報がある。

SMBIOSデータをそのまま取得するユーティリティも各種あり、例えば "smbiosw"\[3\] や "SMBIOS Peek"\[4\] がある。

### UEFI

[UEFIでは](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")、"SmbiosView" というシェルアプリケーションでSMBIOSデータを見ることができる。

## 脚注・出典

## 関連項目

  - [Web-Based Enterprise Management](../Page/Web-Based_Enterprise_Management.md "wikilink") (WBEM)

## 外部リンク

  - [WinDMI Utility](http://aopen.jp/tech/techinside/WinDMI.html) AOpen社のWebサイトにあるSMBIOSに関する説明
  - [System Management BIOS (SMBIOS) Specification](http://www.dmtf.org/standards/smbios/) Distributed Management Task Force, Inc.

[Category:BIOS](https://ja.wikipedia.org/wiki/Category:BIOS "wikilink")

1.  [dmidecode](http://www.nongnu.org/dmidecode/) - DMIテーブルをLinux/BSD/Solaris上でデコードするツール。同サイトには他のシステム情報関連ツールへのリンクもある。
2.  [SMBIOS Support in Windows](http://msdn.microsoft.com/en-us/windows/hardware/gg463136), Microsoft paper, updated April 25, 2005
3.  [FREE:SMBIOS Utilities for Windows and Command Line](http://desktopengineer.com/story_20050215082742328)
4.  [SMBIOS Peek](http://www.codeproject.com/Articles/24730/SMBIOS-PeekM)