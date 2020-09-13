> この記事は[Preboot Execution Environment](https://ja.wikipedia.org/wiki/Preboot_Execution_Environment)から翻訳されています。


**Preboot eXecution Environment**（**PXE**、ピー・エックス・イー、ピクシー）は、コンピュータの[ブート](../Page/ブート.md "wikilink")環境のひとつ。[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の策定したネットワーク[ブート](../Page/ブート.md "wikilink")の規格である。ネットワークブートを利用することにより、[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")をもたないクライアントコンピュータや、ストレージに別の[OSが導入されているクライアントコンピュータが](../Page/オペレーティングシステム.md "wikilink")[サーバ](../Page/サーバ.md "wikilink")上のOSイメージを使用して起動できる。

## 概要

PXEブート環境を構築することで、[HDD](https://ja.wikipedia.org/wiki/HDD "wikilink")などの[ストレージ](https://ja.wikipedia.org/wiki/ストレージ "wikilink")を持たないコンピューター（[シンクライアント](../Page/シンクライアント.md "wikilink")の類）へ[OS](../Page/OS.md "wikilink")イメージを送り込んで動作させたり、[DVDドライブ](https://ja.wikipedia.org/wiki/DVDドライブ "wikilink")などインストールメディアを持たないコンピューターへインストールイメージを送り込んでインストーラーを起動させたりすることが可能になる。

### 構成

PXEによるネットワークブートには次の構成が必要である。

  - クライアント
      - PXEに準拠したソフトウェアの入った[ROMを備えた](https://ja.wikipedia.org/wiki/Read_Only_Memory "wikilink")[NIC (Network Interface Card)](../Page/ネットワークカード.md "wikilink")
  - ネットワーク上のサーバ
      - [DHCPサーバ](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")（または[BOOTPサーバ](../Page/Bootstrap_Protocol.md "wikilink"))
          - OPTION 60:Client Identifier
          - OPTION 66:TFTP Server Name
          - OPTION 67:Boot File Name
      - [TFTPサーバ](../Page/Trivial_File_Transfer_Protocol.md "wikilink")
          - DHCP OPTION 67 で指定されているファイル名で起動イメージ（[ブート](../Page/ブート.md "wikilink")ローダ）を用意しておく。
      - （オプション）[WWW](https://ja.wikipedia.org/wiki/WWW "wikilink")サーバ、[FTP](https://ja.wikipedia.org/wiki/FTP "wikilink")サーバなど
    <!-- end list -->
      -
        起動イメージ（ブートローダ）が [HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink") や FTP に対応していることを前提に、オペレーティングシステムやインストーラー本体のイメージを WWWサーバや FTPサーバから別途配布させる構成が多い。

#### ProxyDHCPの使用

既存のDHCPサーバーとの通信を仲介（PXEブートのためのオプションを付加して介在）する ProxyDHCP を使用すると、既存のDHCPサーバの設定を変更することなく PXEブート環境を構築することが出来る。[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")向けの[Windows展開サービスも同様の仕組みで機能させている](https://ja.wikipedia.org/wiki/WDS "wikilink")。

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

[Category:ブート](https://ja.wikipedia.org/wiki/Category:ブート "wikilink") [Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink") [Category:BIOS](https://ja.wikipedia.org/wiki/Category:BIOS "wikilink")