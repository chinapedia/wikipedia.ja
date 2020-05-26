> この記事は[Preboot Execution Environment](https://ja.wikipedia.org/wiki/Preboot_Execution_Environment)から翻訳されています。


**Preboot eXecution Environment**（**PXE**、ピー・エックス・イー、ピクシー）は、コンピュータの[ブート](../Page/ブート.md "wikilink")環境のひとつ。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の策定したネットワーク[ブート](../Page/ブート.md "wikilink")の規格である。ネットワークブートを利用することにより、[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")をもたないクライアントコンピュータや、ストレージに別の[OSが導入されているクライアントコンピュータが](../Page/オペレーティングシステム.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")上のOSイメージを使用して起動できる。

## 概要

PXEによるネットワークブートにはクライアントにPXEに準拠したソフトウェアの入った[ROMを備えた](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")[NIC (Network Interface Card)](../Page/ネットワークカード.md "wikilink") が装備されていること、サーバでは、PXEサーバおよび[DHCPサーバ](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")（または[BOOTPサーバ](../Page/Bootstrap_Protocol.md "wikilink"))が動作している必要がある。

## PC起動時のPXEエラーメッセージ

PXE ROMを搭載したコンピュータの起動時に、ハードディスクなどの起動デバイスからOSを読み込めない場合、PXEという文字列を含む[エラーメッセージ](../Page/エラーメッセージ.md "wikilink")が表示されることがある。 このエラーメッセージは、PXEが起動リソースを検索した結果見つからなかったため、DHCPサーバやLANケーブルをチェックすることを促すものである。すなわち、[BIOSなどにおける起動デバイス設定において](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、ネットワークブートできない環境にもかかわらず、起動デバイスの検索順位にPXEを用いたネットワークブートが含まれていて、通常使用される起動デバイスが障害などにより使用できない場合、PXEを用いたネットワークブートを試み、それも失敗したためチェックせよというメッセージである。

ネットワークブートを利用していない環境において上記のようなメッセージが現れた場合、[BIOSにおける起動デバイス設定に問題があるか](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")、または起動に用いるハードディスクに異常が発生したと考えるのが妥当である。

## 関連項目

  - [DHCP](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")
  - [BOOTP](../Page/Bootstrap_Protocol.md "wikilink")
  - [TFTP](../Page/Trivial_File_Transfer_Protocol.md "wikilink")
  - [WinINSTALL](../Page/WinINSTALL.md "wikilink")(PXEを実装したPC統合管理ツール)
  - [IPXE](https://ja.wikipedia.org/wiki/IPXE "wikilink")
  - [UEFI](https://ja.wikipedia.org/wiki/UEFI "wikilink")
  - [BIOS](https://ja.wikipedia.org/wiki/BIOS "wikilink")

## 参考文献

  - Intel and Systemsoft, *[Preboot Execution Environment (PXE) Specification](http://www.pix.net/software/pxeboot/archive/pxespec.pdf)*, Version 2.1, 1999.

[Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink")