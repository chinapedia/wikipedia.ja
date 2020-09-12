> この記事は[USB Attached SCSI](https://ja.wikipedia.org/wiki/USB_Attached_SCSI)から翻訳されています。


**USB Attached SCSI** (**UAS**) ないし**USB Attached SCSI プロトコル** (**UASP**) は、 [ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") (HDD)、[ソリッドステートドライブ](../Page/ソリッドステートドライブ.md "wikilink") (SSD)、[USBメモリなどの](../Page/USBフラッシュドライブ.md "wikilink")[USBストレージデバイスを用いてデータ転送を行うために使用される](../Page/ユニバーサル・シリアル・バス.md "wikilink")[コンピュータープロトコル](../Page/通信プロトコル.md "wikilink")。UASはUSBプロトコルに依存し、標準の[SCSIコマンドセットを使用する](../Page/Small_Computer_System_Interface.md "wikilink")。 UASを使用すると、従来のバルク転送 (BOT) ドライバーと比較して、一般的に高速にデータ転送が行える。

UASはUSB 3.0の一部として導入されたが、従来のUSBに準拠するデバイスでも対応していれば使用可能である。

## 概要

UASは、「UAS」仕様と呼ばれるT10「USB Attached SCSI」（T10 / 2095-D）と、USB「Universal Serial Bus Mass Storage Class - USB Attached SCSI Protocol (UASP)」仕様の2つの規格にわたって定義されている。UASの仕様は、 [国際情報技術標準委員会](https://ja.wikipedia.org/wiki/情報技術規格国際委員会 "wikilink") (INCITS) のT10技術委員会が開発・保守している。 また、SCSI Trade Association (SCSITA) が、UAS技術を推進している。[USBマスストレージデバイスクラス](https://ja.wikipedia.org/wiki/USB大容量記憶装置クラス "wikilink") (MSC) ワーキンググループは、UASPの仕様を開発・保守している。 [USB Implementers Forum](https://ja.wikipedia.org/wiki/USBインプリメンターズ・フォーラム "wikilink") (USB-IF) はUASP技術を推進している。

UASドライバーは通常、従来のバルク転送 (BOT) ドライバーと比較して、一般的に高速にデータ転送が行える\[1\]\[2\]\[3\]。また、UASは[USB 3.0標準として追加されたが](../Page/ユニバーサル・シリアル・バス.md "wikilink")、互換性のあるハードウェアであれば、USB 2.0環境においても使用できる\[4\]。

[SSDで使用する場合](../Page/ソリッドステートドライブ.md "wikilink")、UASはランダムな読み取り・書き込みにおいてはBOTよりもかなり高速だが、ネイティブ[SATA 3インターフェースの速度](https://ja.wikipedia.org/wiki/シリアルATA "wikilink") (6 Gbps) を大きく下回っている\[5\]。

## ハードウェアサポート

SemiAccurateによる2010年7月の簡単なハードウェアラウンドアップでは、 [Gigabyte Technologyが](../Page/GIGABYTE.md "wikilink")[NEC](../Page/日本電気.md "wikilink")/[Renesasチップを使用しているボード用のUASドライバーを導入しており](../Page/ルネサスエレクトロニクス.md "wikilink")、少なくともハードウェアレベルでは、LucidPort USB 300およびUSB302、 [Symwave](https://ja.wikipedia.org/wiki/マイクロチップ・テクノロジー "wikilink") SW6315、 [Texas Instruments](../Page/テキサス・インスツルメンツ.md "wikilink") TUSB9260と[VLI](../Page/VIA_Technologies.md "wikilink") VL700コントローラーは完全にUASPをサポートしているが、ASMedia ASM1051とASM1051E、およびFujitsu MB86C30Aはサポートしていない\[6\]。

2011年8月のVR-Zoneによる比較パフォーマンスレビューでは、NEC/RenesasチップのみがUASドライバーを備えていると結論付けられている\[7\]。同じルネサスのUASドライバー（Windows用）は、AMDのA70MおよびA75フュージョンコントローラーハブ\[8\]でも動作する\[9\]。2011年10月には、ASMediaチップもドライバーのサポートを受けている（以前はハードウェア側でサポートしていた）\[10\]。富士通は、UASをサポートするMB86C311Aのようなハイエンドチップをいくつかリストアップしている\[11\]。

インテル[プラットフォームコントローラーハブ](https://ja.wikipedia.org/wiki/プラットフォーム・コントローラー・ハブ "wikilink") (PCH) によるサポートについては、MyCEの記事で「ネイティブのIntel USB3 UASPソリューションはWindows 8でのみサポートされている」「すべてのZ77マザーボードでサポートされているわけではない」「UASPの実装にはライセンスが必要であり、全マザーボードメーカーがコストを製品に転嫁している状況ではない」と書かれている\[12\]。

## オペレーティングシステムのサポート

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は、UASのネイティブサポートを[Windows 8以降に追加した](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")\[13\]。UASをサポートするドライブは、従来のUsbstor.sysではなくUaspstor.sysをロードする\[14\]。Windows 8以降は、USB 2.0を介してのUASもデフォルトでサポートしている\[15\]。UASのドライバーと製品は、 Windowsハードウェア認定キットを使用してマイクロソフトによって認定されている\[16\]。

Appleは[OS X 10.8 Mountain LionにUASのネイティブサポートを追加した](https://ja.wikipedia.org/wiki/OS_X_Mountain_Lion "wikilink")。UASを使用するドライブがシステム情報内に表示される\[17\]。対応しているのに未ロードとして表示されているドライブは、従来のバルク転送 (BOT) モードで機能している。これは、ドライブのUSBコントローラ、MacのUSBポート、または接続されているUSBハブがUASPモードをサポートしていない場合に発生することがある。

[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")では、バージョン3.15がリリースされた2014年6月8日以降、UASをサポートしている\[18\] 。ただし、[Ubuntu](../Page/Ubuntu.md "wikilink")（v11.xx以降）などの一部の[Linux](../Page/Linux.md "wikilink")ディストリビューションでは、UASプロトコルの実装に関する問題が発生している。一部のUAS非対応USB HDDドライブでは、ドライブがオペレーティングシステムからマウントできない。回避策として modprobeのUASモジュールをブラックリストに登録する必要があるとされている\[19\]。

## 達成された事項

  - USBマスストレージデバイスクラスのバルク転送 (BOT) の障害に直接対処するように設計
      - USBマスストレージデバイスのコマンドキューイングと順不同の完了を有効化
      - SCSIコマンドフェーズのソフトウェアオーバーヘッドを排除
      - SSDの[TRIM](../Page/TRIM.md "wikilink") (SCSIではUNMAP) 操作を有効化\[20\]
  - 最大64 Kのコマンドをキューに入れることが可能
  - SCSI SAM-4に準拠
  - USB 3.0 SuperSpeedおよびUSB 2.0 High-Speedバージョンでの定義
      - USB 3.0 SuperSpeed –ホストコントローラー (xHCI) ハードウェアサポート、アウトオブオーダーコマンドのソフトウェアオーバーヘッド排除
      - USB 2.0 High-speed– USB 2.0ドライブでのコマンドキューイングを大幅に有効化
  - UASの順不同の完了をサポートするために、ストリームをUSB 3.0 SuperSpeedプロトコルに追加
      - USB 3ホストコントローラー (xHCI) でストリームのハードウェアサポートを提供

## 参考文献

## 外部リンク

  - [USB Attached SCSI Protocol (UASP) v1.0 and Adopters Agreement](https://web.archive.org/web/20120119200525/http://www.usb.org/developers/devclass_docs/uasp_1_0.zip), 2009-06-24

  - , 2013-03-04

  - [USB Attached SCSI (UAS)](http://www.t10.org/members/w_uas-.htm) (data on t10.org)

  - [USB Attached SCSI Protocol (UASP)](https://web.archive.org/web/20140729191729/http://www.usb.org/developers/presentations/pres0410/2-4_SSUSB_DevCon_UASP_Stevens.pdf) (PDF)

[Category:USB](https://ja.wikipedia.org/wiki/Category:USB "wikilink") [Category:SCSI](https://ja.wikipedia.org/wiki/Category:SCSI "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15. [USB Attached SCSI (UAS) Best Practices for Windows 8](http://msdn.microsoft.com/en-us/library/windows/hardware/jj248714.aspx), page 6
16.
17.
18.
19.
20. [New API allows apps to send "TRIM and Unmap" hints to storage media](https://msdn.microsoft.com/en-us/windows/compatibility/new-api-allows-apps-to-send-trim-and-unmap-hints)