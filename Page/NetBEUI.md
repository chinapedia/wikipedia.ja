> この記事は[NetBEUI](https://ja.wikipedia.org/wiki/NetBEUI)から翻訳されています。


**NetBEUI** （NetBIOS Extended User Interface、ネットブーイ、ネットビューイ） は、**NetBIOS**を改良した[プロトコルである](../Page/通信プロトコル.md "wikilink")。

NetBEUIは[LAN Manager](https://ja.wikipedia.org/wiki/LAN_Manager "wikilink")、[LAN Server](https://ja.wikipedia.org/wiki/LAN_Server "wikilink")、[Windows for Workgroups](https://ja.wikipedia.org/wiki/Microsoft_Windows_3.x#ネットワーク／インターネット "wikilink")（Windows 3.x系）、[Windows 9x系](../Page/Windows_9x系.md "wikilink")、[Microsoft Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、[Microsoft Windows Vistaまでの](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[Windows NT系の各](../Page/Windows_NT系.md "wikilink")[ネットワーク](../Page/コンピュータネットワーク.md "wikilink")[OSにおいて利用される](../Page/オペレーティングシステム.md "wikilink")。

## 概要

Systek社が[IBM PC用のネットワーク用に](https://ja.wikipedia.org/wiki/PC/AT "wikilink")**NetBIOS**を開発した。NetBIOSの名称は「[BIOS呼び出しの仕組みを利用したネットワーク](https://ja.wikipedia.org/wiki/Basic_Input/Output_System "wikilink")[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")」に由来する。

**NetBEUI**は米[IBM](../Page/IBM.md "wikilink")社により同社の「PC LAN Program」と米[マイクロソフト](../Page/マイクロソフト.md "wikilink")社の「MS-NET」（Microsoft Networks）のために[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に拡張された。[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")にはマイクロソフトと米[ノベル社がそれぞれ](../Page/ノベル_\(企業\).md "wikilink")[LAN Managerと](https://ja.wikipedia.org/wiki/LAN_Manager "wikilink")[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")のためにさらに拡張した。

以前はプロトコルとAPI（Application programming interface）を総称してNetBIOSと呼んでいたが、その後プロトコルをNetBEUI、APIをNetBIOSと呼ぶようになった。ただし、NetBEUI は「拡張NetBIOS」の名前から分かるように、本来はAPIである。プロトコルを指す場合、正確にはNBF(NetBEUI Frame Protocol) と呼ぶべきである。実際、Windowsに実装されたNetBEUIプロトコルドライバのファイル名はNBF.SYSであるし、レジストリキーもNBFである。

今日では、NetBEUI（NBF:NetBIOS Frames protocol or NetBIOS over [IEEE 802.2](https://ja.wikipedia.org/wiki/IEEE_802.2 "wikilink")）は[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")(**NBT**:NetBIOS over TCP/IP)へほとんど置き換えられている。

マルチキャストを多用すること、ルーティング機能が実装されていないことから、プロトコルとしては小規模な[LAN向けである](../Page/Local_Area_Network.md "wikilink")。セキュリティ上の観点から、NBTをオフにしてNetBEUIを使う場合もある。

## 終焉

前述のとおりインターネットの一般化とTCP/IP（NBT）が主流になったため、Windows XPでは、標準のビルトイン・プロトコルからは外され（付属のCDからインストール可）、Windows XPとではNetBIOS[名前解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")（NBNS）を使ってコンピュータ名をネットワーク上に登録・取得していた\[1\]程度となり、NetBEUIのみでネットワークを構築することは現実的ではなくなった。このためかNetBEUI自体が廃止された。

## 関連項目

  - [IPX/SPX](https://ja.wikipedia.org/wiki/IPX/SPX "wikilink")
  - [Server Message Block](../Page/Server_Message_Block.md "wikilink")
  - [Common Internet File System](https://ja.wikipedia.org/wiki/Common_Internet_File_System "wikilink")

## 出典

<references/>

[Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")

1.  日経NETWORKTOW 2007年11月号「Vistaネットワーク大解剖 第2回 Windowsネットワークへの参加」