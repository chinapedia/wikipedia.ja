> この記事は[Network Driver Interface Specification](https://ja.wikipedia.org/wiki/Network_Driver_Interface_Specification)から翻訳されています。


**Network Driver Interface Specification** (**NDIS**) は、[ネットワークカード](https://ja.wikipedia.org/wiki/ネットワークカード "wikilink")のための[APIの一種である](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[スリーコム](https://ja.wikipedia.org/wiki/スリーコム "wikilink")が共同で開発し、主に [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") で使われているが、[オープンソース](../Page/オープンソース.md "wikilink")の [NdisWrapper](https://ja.wikipedia.org/wiki/NdisWrapper "wikilink") や Project Evil のドライバラッパーにより、NDIS準拠のネットワークカードの多くが [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") や [FreeBSD](../Page/FreeBSD.md "wikilink") で利用可能となっている。[BeOS](../Page/BeOS.md "wikilink") から派生した [ZETA](https://ja.wikipedia.org/wiki/ZETA "wikilink") はいくつかの NDIS ドライバをサポートしている。

NDIS は[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")におけるデータリンク層（7層のうちの第2層）の上側のサブレイヤーである[論理リンク制御](https://ja.wikipedia.org/wiki/論理リンク制御 "wikilink") (LLC) に相当し、第2層と第3層（ネットワーク層）の間のインタフェースとして機能する。下側のサブレイヤーは [媒体アクセス制御](https://ja.wikipedia.org/wiki/媒体アクセス制御 "wikilink") (MAC) [デバイスドライバ](../Page/デバイスドライバ.md "wikilink")である。

NDIS はラッパー (wrapper) と呼ばれる機能群のライブラリであり、下位のハードウェアの複雑さを隠蔽し、第3層のネットワークプロトコルドライバとハードウェアレベルのMACドライバに標準化されたインタフェースを提供する。同様な LLC 機能を提供するものとして [Open Data-Link Interface](https://ja.wikipedia.org/wiki/Open_Data-Link_Interface "wikilink") (ODI) がある。

[Wireless Zero Configuration](https://ja.wikipedia.org/wiki/Wireless_Zero_Configuration "wikilink") (WZC) のコンポーネントとして、 NDIS User Mode I/O (NDISUIO) プロトコルドライバがある。これはマイクロソフト製のドライバで Windows XP に含まれている。通常、[IEEE 802.3ドライバ](../Page/イーサネット.md "wikilink")（ミニポート）と共にインストールされる。

各 Windows のバージョンでサポートされている NDIS バージョンは以下の通り。

  - NDIS 2.0: MS-DOS, Windows for Workgroups 3.1
  - NDIS 3.0: Windows for Workgroups 3.11, NT 3.5
  - NDIS 3.1: Windows 95
  - NDIS 4.0: Windows 95 OSR2, NT 4.0
  - NDIS 4.1: Windows 98, NT 4.0 SP3
  - NDIS 5.0: Windows 98 SE, Me, 2000
  - NDIS 5.1: Windows XP
  - NDIS 5.2: Windows Server 2003
  - NDIS 6.0: Windows Vista
  - NDIS 6.1: Windows Vista SP1, Server 2008
  - NDIS 6.2: Windows 7, Server 2008 R2
  - NDIS 6.3: Windows 8, Server 2012
  - NDIS 6.4: Windows 8.1, Server 2012 R2
  - NDIS 6.50: Windows 10 1507
  - NDIS 6.51: Windows 10 1511
  - NDIS 6.60: Windows 10 1607, Windows Server 2016
  - NDIS 6.70: Windows 10 1703
  - NDIS 6.80: Windows 10 1709
  - NDIS 6.81: Windows 10 1803
  - NDIS 6.82: Windows 10 1809, Windows Server 2019
  - NDIS 6.83: Windows 10 1903

## 関連項目

  - [NdisWrapper](https://ja.wikipedia.org/wiki/NdisWrapper "wikilink")
  - [Open Data-Link Interface](https://ja.wikipedia.org/wiki/Open_Data-Link_Interface "wikilink") (ODI)
  - [Uniform Driver Interface](https://ja.wikipedia.org/wiki/Uniform_Driver_Interface "wikilink") (UDI)

## 外部リンク

  - [Network Driver Design Guide | Microsoft Docs](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/)

[Category:デバイスドライバ](https://ja.wikipedia.org/wiki/Category:デバイスドライバ "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")