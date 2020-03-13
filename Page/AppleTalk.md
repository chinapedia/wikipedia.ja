> この記事は[AppleTalk](https://ja.wikipedia.org/wiki/AppleTalk)から翻訳されています。


**AppleTalk**（アップルトーク）は、主に[アップル製パソコンの](../Page/アップル_\(企業\).md "wikilink")[Macintosh](../Page/Macintosh.md "wikilink") (Mac) で利用された[通信プロトコル](../Page/通信プロトコル.md "wikilink")群の総称。 AARP、DDP、RTMP、AEP、NBP、ZIP、ATP、PAP、ASP、ADSP、[AFPといった複数のプロトコルを組み合わせて利用する技術だった](../Page/Apple_Filing_Protocol.md "wikilink")。

## 概説

AppleTalkは[TCP/IPとは全く別のものである](../Page/インターネット・プロトコル・スイート.md "wikilink")。初期のTCP/IPはユーザや管理者による複雑な設定を必要としたのに対し、AppleTalkは「ケーブルを繋げばすぐ使える」ネットワークであった。ただし、基本的なフレームワークが全く異なり、相互互換性がない。TCP/IP ([IPv4](../Page/IPv4.md "wikilink")) が[32ビット](../Page/32ビット.md "wikilink")の[IPアドレス](../Page/IPアドレス.md "wikilink")で個体の識別を行なうのに対し、AppleTalkでは[24ビット](https://ja.wikipedia.org/wiki/24ビット "wikilink")（[16ビット](../Page/16ビット.md "wikilink")のネットワーク部と[8ビット](../Page/8ビット.md "wikilink")のノードアドレス）を用いた。

AppleTalk対応機器は、電源投入時あるいは[ネットワーク接続時に](../Page/コンピュータネットワーク.md "wikilink")[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")信号を流し、自動的にアドレスとマシン名を割り当てる。また、ネットワーク上の[ファイルサーバ](../Page/ファイルサーバ.md "wikilink")や[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")を発見することができる。すなわち、AppleTalkのみのネットワークでは、ユーザは何の設定も行なわず、繋いだ途端に[ファイル共有](../Page/ファイル共有.md "wikilink")や印刷が行なえるようになっていた。こうしたユーザの手を煩わせない自動設定の仕組みはTCP/IPよりも先行していた。ただし、この機能の実現のためネットワークに大きな負荷をかけた。

やがて[インターネット](../Page/インターネット.md "wikilink")が普及して接続にはTCP/IPを用いるのが主流となると、AppleTalkとTCP/IPを共存させる必要性が出てきた。結果的にユーザと管理者は両立のための複雑な設定を余儀なくされた。また、TCP/IPとはプロトコルの構造が異なるため、一般的な[ルーター](../Page/ルーター.md "wikilink")では他のネットワークに接続できず、AppleTalk対応ルーターを用意する必要があった。

一方で、TCP/IPも時代とともに技術が進み、自動設定のプロトコルが登場するようになった。[DHCPプロトコルは](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")、AppleTalkのAARPやNBPをヒントに開発されたといわれている。

現在のアップルの製品は[Bonjour](../Page/Bonjour.md "wikilink")を実装している。これはAppleTalkにおける自動設定と同様の機能をTCP/IP上で実現し、更にネットワーク負荷を小さくするものである。

## 終焉

[Mac OS X v10.2からBonjour](../Page/Mac_OS_X_v10.2.md "wikilink")（当時Rendezvous）の登場により現在主流のプロトコルである前述のTCP/IP上で同等あるいはそれ以上の機能を実現しているため、AppleTalkの機能は徐々に縮小され、[Mac OS X v10.5では](../Page/Mac_OS_X_v10.5.md "wikilink")[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")が使用可能となる程度となり、[Mac OS X v10.6にて完全になくなった](../Page/Mac_OS_X_v10.6.md "wikilink")。

## 登場背景

Macintosh登場当初は[WYSIWYG](../Page/WYSIWYG.md "wikilink")を実現するため1[ポイント](../Page/ポイント.md "wikilink")=1[ピクセル](../Page/ピクセル.md "wikilink")となる72dpiを画面表示の[解像度](../Page/解像度.md "wikilink")としており、スケーラブルなイメージを表現するために[QuickDraw](../Page/QuickDraw.md "wikilink")を利用していた。 このため画面表示用の演算は初期のMacintoshでも本体のMPU ([68000](../Page/MC68000.md "wikilink")) と[メモリで実現可能であった](../Page/記憶装置.md "wikilink")（Macintosh自体がある時期までモノクロ表示だったことも影響する）。 しかし、印刷用となると72dpiでというわけにはいかず、プリンター内に本体と同等以上の[MPUとメモリを必要とした](../Page/マイクロプロセッサ.md "wikilink")（特に高解像度のデータを展開するには大量のメモリを必要とした）。 このため、プリンターの価格が高くなりワークグループでプリンターを共有するために、早急にネットワーク環境を構築する必要があった。 そこでMacintoshに標準搭載されていた[シリアルポート](../Page/シリアルポート.md "wikilink")の[RS-422](https://ja.wikipedia.org/wiki/RS-422 "wikilink")を物理媒体にした[LANのプロトコルとして登場することとなった](../Page/Local_Area_Network.md "wikilink")。 なお、[Apple IIGSにもLocalTalkは搭載されている](../Page/Apple_II.md "wikilink")。

## 歴史

最初のAppleTalkは1984年に開発された。

次のAppleTalk Phase 2は1989年に公開された。これは規模の大きいネットワーク環境のための拡張であった。

これ以降はTCP/IPが主流になってきたため、AppleTalk自体には大きな進化は見られず、TCP/IPとAppleTalkを共存させる手法が一般的になる。

IPをAppleTalkでカプセル化する[MacIP](https://ja.wikipedia.org/wiki/MacIP "wikilink")や、これとは逆にAppleTalkをIPでカプセル化する[IPTalkもあったが](https://ja.wikipedia.org/wiki/IPTalk_\(通信\) "wikilink")、現在は使われていない。

[サーバ](../Page/サーバ.md "wikilink")のブラウジングはAppleTalkのNBPが使われていたが、Mac OS 8.5からTCP/IPベースの[SLPも採用され](../Page/サービス・ロケーション・プロトコル.md "wikilink")、更に[Mac OS X v10.2から](../Page/Mac_OS_X_v10.2.md "wikilink")[Bonjour](../Page/Bonjour.md "wikilink")へと移行した。

プリンター共有はAppleTalkのPAPが使われていたが、Mac OS XからはLPR、[IPP](../Page/Internet_Printing_Protocol.md "wikilink")、[SMB (CIFS)](https://ja.wikipedia.org/wiki/Common_Internet_File_System "wikilink") 等も利用できるようになった。[AirMacベースステーションや](https://ja.wikipedia.org/wiki/AirMac#ベースステーション "wikilink")[Time CapsuleではUSB接続したプリンタに対してネットワーク越しに印刷できる機能があるが](../Page/Time_Capsule.md "wikilink")、これはIPベースの印刷でありAppleTalkは使われない。

ファイル共有はAFP over TCPへと移行した。[漢字Talk](../Page/漢字Talk.md "wikilink")7.5.5に[Open Transport](../Page/Open_Transport.md "wikilink") J-1.1.2以降をインストールすればAFP over TCPが利用できる。

[Mac OS X v10.4ではNBPによるAFPサーバのブラウジングは可能であったが](../Page/Mac_OS_X_v10.4.md "wikilink")、ファイルサーバへの接続はAppleTalkではなくAFP over TCPのみになった。

[Mac OS X v10.5ではAppleTalkプリンターの使用が可能であるだけで](../Page/Mac_OS_X_v10.5.md "wikilink")、それ以外の機能はほとんど残っていない。

[Mac OS X v10.6でついにAppleTalkの対応がなくなった](../Page/Mac_OS_X_v10.6.md "wikilink")。

## 物理層およびデータリンク層

初期は物理層のRS-422をも含めてAppleTalkと称したが、後に別の物理媒体も使えるようになったため、AppleTalkは主にプロトコルを示すものとし、物理層と分けて考えるようになった。物理層とAppleTalkパケットの間に位置するデータリンク層のプロトコルを**LAP** (Link-Access Protocol) と呼ぶ。

それまでの[RS-422を用いたものをLocalTalkと呼び](../Page/EIA-422.md "wikilink")、新たに使えるようになったものをEtherTalk、TokenTalk、FDDITalk等と呼んで区別する。

LocalTalkより後のものは、[IEEE 802.2による](https://ja.wikipedia.org/wiki/IEEE_802.2 "wikilink")[LLC](https://ja.wikipedia.org/wiki/論理リンク制御 "wikilink") (Logical Link Control) を用いてAppleTalkのパケットをカプセル化する方法をとったため、LLCさえサポート出来ればさまざまな物理媒体が使えることとなった。結果、ずっと後に登場した[IEEE 802.11による](../Page/IEEE_802.11.md "wikilink")[無線LAN](../Page/無線LAN.md "wikilink")上でもAppleTalkが利用できる。

また、これらとは別に、AppleはARA (Apple Remote Access) や[Open Transportと呼ばれるソフトウェアを開発し](../Page/Open_Transport.md "wikilink")、これらを使えば電話回線を通じて遠隔地のMacとAppleTalkで接続できるようにした。

### LocalTalk

初期の頃に使われた。物理層はMacなどのプリンターポートのRS-422を想定している。 プリンターや[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")用のRS-422ケーブルを双方に直に挿すだけでOS標準の機能だけで2台のMacでファイル交換ができたりもした。3台以上の場合はMac本体やプリンタのRS-422の先に二股のRS-422のつく接続キットを用いる。 米Farallon Computingが、両端がRS-422で中間に[RJ-11コネクタの](../Page/Registered_jack.md "wikilink")6線式電話線を2口備え、電話線が使えるようにした「[PhoneNet](https://ja.wikipedia.org/wiki/フォーンネット "wikilink")」を開発した。このFarallon Computing式の電話モジュラーケーブルによる接続がEtherTalkが一般的になるまでは実質LocalTalkの物理層の3台以上の小規模接続の主流となった。作りが簡単なため多くの互換品が市場にでまわり、ついにアップル自身もPhoneNet互換の電話線用[モジュラーケーブルを利用するLocalTalk接続キットを発売していた](../Page/Registered_jack.md "wikilink")。PhoneNetは登録商標であるため、互換品では**PhoneTalk**と称する場合がある。 またLoaclTalkの物理層としてRS-422の先に取り付ける赤外線が使える製品なども[サードパーティー](../Page/サードパーティー.md "wikilink")から出ていた。 RS-422上でAppleTalkを使うプロトコルを**LLAP** (LocalTalk Link-Access Protocol) と呼ぶ。

### EtherTalk

[イーサネット](../Page/イーサネット.md "wikilink")を用いたものをEtherTalkと称する。LLCによってAppleTalkのパケットをカプセル化するデータリンク層のプロトコルを**ELAP** (EtherTalk Link-Access Protocol) と呼ぶ。 現在AppleTalkが使われるとすれば、このEtherTalkが多いであろう。

### TokenTalk

[トークンリング](../Page/トークンリング.md "wikilink")を用いたものをTokenTalkと称する。LLCによってAppleTalkのパケットをカプセル化するデータリンク層のプロトコルを**TLAP** (TokenTalk Link-Access Protocol) と呼ぶ。

### FDDITalk

[FDDIを用いたものをFDDITalkと称する](../Page/Fiber_distributed_data_interface.md "wikilink")。FDDIはIEEE 802によって定められたものではないが、LLCを使えるためAppleTalkを利用することができる。LLCによってAppleTalkのパケットをカプセル化するデータリンク層のプロトコルを**FLAP** (FDDITalk Link-Access Protocol) と呼ぶ。

### IRTalk

赤外線ポートを用いたものをIRTalkと称する。これはアップル独自の赤外線ポートであり、以下のIrDAとは別である。

### IrDA

最初にMacに搭載された赤外線通信であるIRTalkは独自の規格であったが、後により一般的な[IrDA](../Page/IrDA.md "wikilink")を用いてAppleTalkやTCP/IPを利用できるようになった。

### IPTalk

IPTalkは特定の物理層を用いるものではない。[IP上でAppleTalkのパケットをカプセル化するプロトコルである](../Page/Internet_Protocol.md "wikilink")。すなわちAppleTalk over IPである。詳しくは[IPTalkを参照](https://ja.wikipedia.org/wiki/IPTalk_\(通信\) "wikilink")。

### 無線LAN

IEEE 802.11による無線LANを用いたAppleTalkに関しては特に固有の名称はない。IEEE 802.11はEthernetによく似た規格でありLLCを使えるため、基本的にEtherTalkと同一と考えてよい。したがって、アップル製、他社製を問わず一般的な無線LAN製品で何ら問題なくAppleTalkパケットを扱うことができる。Ethernetと並んで現在多く用いられているであろう。

### 電話回線

ARA (Apple Remote Access) や[Open Transportのためのソフトウェアをインストールすると](../Page/Open_Transport.md "wikilink")、[アナログ回線](https://ja.wikipedia.org/wiki/アナログ回線 "wikilink")、[ISDN](../Page/ISDN.md "wikilink")等を問わず[電話回線経由](https://ja.wikipedia.org/wiki/電話回線経由 "wikilink")で遠隔地のMacとAppleTalkで接続することができた。このためのプロトコルとしては、**ARAP** (Apple Remote Access Protocol) と[PPPの二種類がある](../Page/Point-to-Point_Protocol.md "wikilink")。ARAPはApple独自のプロトコルである。PPPは元々[NCP](https://ja.wikipedia.org/wiki/Network_Control_Protocol "wikilink") (Network Control Protocol) によってAppleTalkも使えるように設計されたプロトコルである。

## 各プロトコル

ユーザサイドから考えれば、ファイル共有のためのAFPと印刷のためのPAPが有名であるが、実際にはもっと多くのプロトコルの組み合わせで動作している。ネットワーク層（第3層）のDDPとAARPが動作すればAppleTalkの最低条件が整い、他のプロトコルはこれらの上で動作することになる。

### AppleTalk Address Resolution Protocol

**AARP**はAppleTalkのノードアドレスと物理アドレスのマッピングを行なうネットワーク層（第3層）のプロトコルである。TCP/IPにおける[ARPと同等である](../Page/Address_Resolution_Protocol.md "wikilink")。

### Datagram Delivery Protocol

**DDP**は最下位でデータグラムを配送するネットワーク層（第3層）のプロトコルである。TCP/IPにおける[IPに相当する](../Page/Internet_Protocol.md "wikilink")。

### Routing Table Maintenance Protocol

**RTMP**はDDPパケットのルーティングに用いられるトランスポート層（第4層）のプロトコルである。

### AppleTalk Echo Protocol

**AEP**はDDP上でEchoを送受信するトランスポート層（第4層）のプロトコルである。TCP/IPでは[ping](https://ja.wikipedia.org/wiki/ping "wikilink")を用いた[ICMPのechoに近い](../Page/Internet_Control_Message_Protocol.md "wikilink")。

### Name Binding Protocol

**NBP**はAppleTalkの[名前解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")、すなわちノード名とアドレス名の解決やlookupを行なうトランスポート層（第4層）のプロトコルである。

### Zone Information Protocol

**ZIP**はネットワークとAppleTalk Zoneのマッピング等を行なうセッション層（第5層）のプロトコルである。

### AppleTalk Transaction Protocol

**ATP**はAppleTalkのトランザクションを実現するトランスポート層（第4層）プロトコルであり、DDP上に実装される。

### Printer Access Protocol

**PAP**はプリンタ共有のためのセッション層（第5層）プロトコルであり、ATP上に実装される。AppleTalkプリンタは、すなわちPAPサーバとして動作している。

### AppleTalk Session Protocol

**ASP**は高位のネットワークサービスを行なうセッション層（第5層）のプロトコルであり、ATP上に実装される。

### AppleTalk Data Stream Protocol

**ADSP**はAppleTalkで全二重通信を実現するためのセッション層（第5層）のプロトコルである。

### AppleTalk Filing Protocol

**AFP**はファイル共有のためのプレゼンテーション層（第6層）とアプリケーション層（第7層）にまたがるプロトコルであり、ASP上に実装される。数あるAppleTalkのプロトコルのうち、このAFPだけがTCP/IPに移植されている。AFP Version 2.1迄がAppleTalkベースであり、2.2からはTCP/IPベースである (AFP over TCP)。AppleTalkを使用しなくなったことから、名称が**Apple Filing Protocol**に変更された。 詳しくは[Apple Filing Protocolを参照](../Page/Apple_Filing_Protocol.md "wikilink")。AFPによるファイル共有のことを[AppleShare](https://ja.wikipedia.org/wiki/AppleShare "wikilink")と呼ぶ場合がある。

### Appletalk Update-Based Routing Protocol

**AURP**はRFC1504で公開されたAppleTalkのルーティングをWANに拡張するためのトランスポート層（第4層）のプロトコルである。

### MacIP Protocol

**MacIP**はAppleTalk上で[IPのパケットをカプセル化するプロトコルである](../Page/Internet_Protocol.md "wikilink")。すなわちIP over AppleTalkである。詳しくは[MacIP](https://ja.wikipedia.org/wiki/MacIP "wikilink")を参照。

### Timelord Protocol

**Timelord Protocol**は時刻合わせのプロトコルである。[メルボルン大学](../Page/メルボルン大学.md "wikilink")で開発されたものであり、サーバソフトウェア「Timeload」にはMac OS用と[CAP用がある](https://ja.wikipedia.org/wiki/Columbia_AppleTalk_Package "wikilink")。[クライアントソフトウェアは](../Page/クライアント_\(コンピュータ\).md "wikilink")「tardis」という。 仕様書は特に存在しないため、[netatalk](https://ja.wikipedia.org/wiki/netatalk "wikilink")はCAP用Timeloadのソースをリバースエンジニアリングして実装を行なっている。 Mac OS 8.5以降はTCP/IPの時刻プロトコルである[NTPクライアント機能を実装しているため](../Page/Network_Time_Protocol.md "wikilink")、Timelordの必要性は薄まっている。

## OSI参照モデル

ゾーン情報を取得するには、ZIP over DDPが用いられる。

Macから他のノードを発見するには、NBP over DDPが用いられる。

プリンタへの印刷は、PAP over ATP over DDPが用いられる。

ファイル共有には、AFP over ASP over ATP over DDPが用いられる（AFP over TCPに関しては[Apple Filing Protocolを参照](../Page/Apple_Filing_Protocol.md "wikilink")）。

## セレクタ

[Mac OS 9までの](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS_9 "wikilink")[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")「Chooser」、「セレクタ」やMac OS X v10.4までの「ネットワーク」では、他のノードを発見し選択することができるが、 これらが起動している間は常にネットワークへNBPによるブロードキャスト信号を流す。このため、開いたままにしておくとネットワークトラフィックの増加を招くので使用後はすぐに終了させたほうがよいとされた。

また、ネットワーク上の他のマシン（接続先のプラットフォームは問わない）を接続し、その内容を表示していると、「常にウィンドウ内容の変化を監視する」動作を行うMac OSの仕組みにより、ローカルディスクのみならずネットワーク上デバイスのウィンドウも逐一内容更新を行うため、やはりネットワークに負荷がかかった。

現在のBonjourでは、なるべくトラフィックを少なくする工夫がされている。

## ルーター

TCP/IPとはプロトコルの構造が異なるため、遠隔地へ接続するためには専用の[ルーター](../Page/ルーター.md "wikilink")が必要になる。ルーターを接続した際には「ゾーン名」の設定が必要になる（AppleTalkルーターが存在する環境で「セレクタ」を開くと、画面左下に選択肢が現れる）。

## 他のオペレーティングシステムでの利用

[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") ([BSD](../Page/BSD.md "wikilink"), [Linux](../Page/Linux.md "wikilink"), [Solaris](../Page/Solaris.md "wikilink")) には、Macintoshのファイルサーバ/プリントサーバとして利用するために[netatalk](https://ja.wikipedia.org/wiki/netatalk "wikilink")というパッケージが存在する。kernelがDDPとAARPを実装し、それ以外のプロトコルをnetatalkが受け持つ仕様である。

かつては[コロンビア大学](https://ja.wikipedia.org/wiki/コロンビア大学 "wikilink")にて開発された[Columbia AppleTalk Package](https://ja.wikipedia.org/wiki/Columbia_AppleTalk_Package "wikilink") (CAP) というパッケージが存在したが、現在はサポートを停止している。

また、[Windows NT以前に一世を風靡したサーバソフトの](../Page/Microsoft_Windows_NT.md "wikilink")[NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink")や、[Windowsサーバ製品でもAppleTalkのファイルサーバ](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")/プリントサーバ/ルーティング機能を実装している（Windows NT 3.1 Advanced Server以降。2000 Professional以降ではプリンターのみのサポート）。

## 外部リンク

  - [Inside Macintosh:Networking](http://developer.apple.com/documentation/mac/Networking/Networking-2.html)
  - [Inside AppleTalk Second Edition (pdf)](http://developer.apple.com/MacOs/opentransport/docs/dev/Inside_AppleTalk.pdf)
  - [AppleTalk Filing Protocol Version 2.1 and 2.2 (pdf)](http://developer.apple.com/MacOs/opentransport/docs/dev/AFP_21_22.pdf)
  - RFC 1243 - AppleTalk Management Information Base
  - RFC 1742 - AppleTalk Management Information Base II
  - RFC 1378 - The PPP AppleTalk Control Protocol (ATCP)
  - RFC 1504 - Appletalk Update-Based Routing Protocol: Enhanced Appletalk Routing
  - [System 7.x.x: AppleTalk and ADSP Versions](http://docs.info.apple.com/article.html?artnum=10151&coll=ap)
  - [株式会社インテリジェントワークス/技術情報 - Apple Talkのプロトコル](http://www.intelligentworks.co.jp/support/skill/appletalk.html)
  - [Internetworking Technology Handbook - Apple Talk - Cisco Systems](http://www.cisco.com/en/US/docs/internetworking/technology/handbook/AppleTalk.html)
  - [Apple Talk Protocol suite](http://www.protocols.com/pbook/appletalk.htm)
  - [CITES UIUCnet documentation: AppleTalk on the Urbana-Champaign Campus](http://www.cites.uiuc.edu/guidelines/network/appletalk/)
  - [AppleTalk Directory & Informational Resource](http://softtechinfo.com/network/apt.html)

## 関連項目

  - [Apple Filing Protocol](../Page/Apple_Filing_Protocol.md "wikilink")
  - [Bonjour](../Page/Bonjour.md "wikilink")
  - [TCP/IP](../Page/インターネット・プロトコル・スイート.md "wikilink")
  - [MacTCP](https://ja.wikipedia.org/wiki/MacTCP "wikilink")
  - [Open Transport](../Page/Open_Transport.md "wikilink")
  - [AppleShare](https://ja.wikipedia.org/wiki/AppleShare "wikilink")
  - [MacIP](https://ja.wikipedia.org/wiki/MacIP "wikilink")
  - [IPTalk (通信)](https://ja.wikipedia.org/wiki/IPTalk_\(通信\) "wikilink")
  - [CAP](https://ja.wikipedia.org/wiki/Columbia_AppleTalk_Package "wikilink")
  - [netatalk](https://ja.wikipedia.org/wiki/netatalk "wikilink")

[Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:Mac_OS](https://ja.wikipedia.org/wiki/Category:Mac_OS "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")