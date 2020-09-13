> この記事は[Advanced SCSI Programming Interface](https://ja.wikipedia.org/wiki/Advanced_SCSI_Programming_Interface)から翻訳されています。


**ASPI** (Advanced SCSI Programming Interface) とは、[アダプテック](../Page/アダプテック.md "wikilink")が提唱した以下の仕様の総称である。

  - [SCSI](../Page/Small_Computer_System_Interface.md "wikilink") [ホストアダプタ](https://ja.wikipedia.org/wiki/ホストアダプタ "wikilink")の[ドライバと](../Page/デバイスドライバ.md "wikilink")、SCSI 装置（[HDD](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink") や [CD-ROM](../Page/CD-ROM.md "wikilink") ドライブなど）のドライバを分離するドライバモデル
  - ホストアダプタのドライバにアクセスするためのソフトウェアインターフェイス

ホストアダプタのドライバを **ASPI マネージャ**といい、ASPI 仕様のソフトウェアインターフェイスを提供する。 このソフトウェアインターフェイスを利用して SCSI 装置を制御するドライバを **ASPI ドライバ**という。 また、アプリケーションからも API を利用して ASPI マネージャ経由で SCSI 装置を制御することが可能である。

なお、[ATAPI](../Page/Advanced_Technology_Attachment.md "wikilink") のコマンドは SCSI と似たようなものであるため、ATAPI デバイスが一般的になると、ATAPI 用の ASPI マネージャ (**ATASPI**) も提供されるようになり、ATAPI と SCSI を統一的に扱えるようになった。

[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")を対象としているが、[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")にも実装された。

類似の仕様に、CAM (Common Access Method) がある。

## 経緯

もともと ASPI は [MS-DOS](../Page/MS-DOS.md "wikilink") および [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") 向けに提唱された。 当時これらの OS ではドライバモデルが未成熟で、SCSI アダプタのドライバと SCSI 装置のドライバが一体化している（モノリシック）のが一般的であった。 すなわち、SCSI アダプタのメーカーや製品と、SCSI 装置のデバイスクラスや製品の組み合わせごとに個別にドライバが必要であり、開発者にとっては開発の負担、利用者にとってはドライバの入手困難を招いていた。また、複数のドライバをインストールして利用する場合に、各ドライバがそれぞれに SCSI アダプタや SCSI 装置を制御している点でも好ましくなかった。

そこでアダプテックは、SCSI アダプタのドライバ（ASPI マネージャ）と SCSI 装置のドライバ（ASPI ドライバ）を分離するデバイスモデル、およびその間を結ぶ共通の API の仕様を提唱した。これが ASPI である。 これにより、SCSI アダプタのメーカーは自社製品の ASPI マネージャだけを、SCSI 装置のメーカーは自社製品の ASPI ドライバだけを開発すればよく、開発の負担が大きく軽減された。 利用者にとっても、自分の利用している SCSI アダプタと SCSI 装置の組み合わせを気にすることなく、ASPI マネージャと ASPI ドライバをインストールすれば事足りるようになった。 とくに、HDD や CD-ROM ドライブのような標準化されたデバイスクラスの ASPI ドライバは、ASPI マネージャと共に SCSI アダプタに添付されるのが通例であり、そのような装置を使う限りは ASPI ドライバの存在もほとんど意識する必要がなかった。 PC/AT 互換機では、SCSI アダプタのメーカーや製品が多様であったため、ASPI の提唱したデバイスモデルの利点は大きく、広く受け入れられるところとなった。

ただ、当時日本で支配的であった PC-9800 シリーズの MS-DOS 環境の場合は事情が異なり、SCSI アダプタは純正の PC-9801-55 （いわゆる55ボード）とハードウェアレベルで互換性のあるものがほとんどであったため、モノリシックな構造のドライバでも比較的問題が少なかったことから、ASPI はそれほど浸透していなかった。しかし一方で、ASPI を導入することにより、PC/AT 互換機向けの各種の ASPI ドライバが PC-9800 シリーズでも利用可能となる（ASPI マネージャが機種依存性を隠蔽する）という側面があったことから、55ボード用の[フリーウェア](../Page/フリーウェア.md "wikilink")の ASPI マネージャも存在し、一部のユーザに使われていた。 後に、PC-9821 シリーズの [PCI](../Page/Peripheral_Component_Interconnect.md "wikilink") 採用機種向けに、アダプテックの SCSI アダプタが NEC 純正品として提供されるに至り、同製品用の ASPI マネージャも純正品として提供された。

## Windows 時代の ASPI

このように、ASPI の本質はドライバモデルにあるということができる。 しかし、このようなドライバモデルはまともな OS なら本来当然備えているべきものであり、PC 用の OS でも [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[Windows 95](../Page/Microsoft_Windows_95.md "wikilink")、[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") などではもともと備えていた。 そのため、これらの OS にも ASPI は提供されたものの、その役割は「SCSI アダプタのドライバ」ではなく「DOS の ASPI と似たソフトウェアインターフェイスを提供するラッパー」に過ぎないもの、すなわち**ASPI レイヤー**となり、[CD-R](../Page/CD-R.md "wikilink") や[イメージスキャナ](../Page/イメージスキャナ.md "wikilink")を制御するアプリケーションなど一部で利用されるにとどまった。

それでも、Windows 95 系列では ASPI レイヤーが OS 標準で付属していたため、それなりに使われてもいたが、Windows NT系列においては、ASPIレイヤーが OS に標準で付属しておらず、SCSI を制御する標準ソフトウェアインターフェイスとして**SPTI** (SCSI Pass-Through Interface) が新たに定義されたことにより、ASPI の存在意義は限りなく薄いものになってしまった。 にもかかわらず、Windows 95 系列での流れから、Windows NT 系列でも SPTI に対応せず ASPI を必要とする CD-R ライティングソフトなどが多数あり、利用者を悩ませていた。 ただし、一部の CD-R ライティングソフトなどには、Windows NT 系列にもインストール可能な ASPI レイヤーが付属しているものがあった。 また、アダプテックも Windows NT 向けに ASPI レイヤーを別途提供していたものの、そのインストールにはアダプテックの SCSI アダプタを装着している必要があり、他社製品の利用者には役に立たないものであった。

近年では Windows NT 系列が主流となったことから、ASPI はほとんど使われなくなってきている。

## ASPI が提供されたプラットフォーム

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [Windows 3.1](../Page/Microsoft_Windows_3.x.md "wikilink")
  - [Windows 9x系](../Page/Windows_9x系.md "wikilink")
  - [Windows NT系](../Page/Windows_NT系.md "wikilink")
  - [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")
  - [OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")

## 外部リンク

### Adaptec 社の ASPI driver

  - [Windows ASPI Package](http://www.adaptec.com/en-US/speed/software_pc/aspi/aspi_471a2_exe.htm)

### Adaptec 社以外の実装

  - [Pinnacle Systems's ASAPI driver](ftp://ftp.pinnaclesys.de/driver/pc/InstantCDDVD/ASAPI.exe)
  - [Nero's ASPI driver](ftp://ftp6.nero.com/NeroASPIdt.exe)

### 技術情報

  - [Technical reference (ASPI for Win32)](http://www.zianet.com/jgray/dat/files/ASPI32.pdf)
  - [ASPI Layer setup](http://www.doom9.org/aspi.htm)

[Category:パーソナルコンピュータ](https://ja.wikipedia.org/wiki/Category:パーソナルコンピュータ "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:デバイスドライバ](https://ja.wikipedia.org/wiki/Category:デバイスドライバ "wikilink") [Category:SCSI](https://ja.wikipedia.org/wiki/Category:SCSI "wikilink")