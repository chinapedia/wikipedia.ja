> この記事は[PacketiX VPN](https://ja.wikipedia.org/wiki/PacketiX_VPN)から翻訳されています。


**PacketiX VPN**（パケティックス ブイピーエヌ）は[ソフトイーサ](../Page/ソフトイーサ.md "wikilink")によって開発される、[VPN](../Page/Virtual_Private_Network.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

本項では、派生ソフトウェアである [UT-VPN](https://ja.wikipedia.org/wiki/UT-VPN "wikilink") や [SoftEther VPN](https://ja.wikipedia.org/wiki/SoftEther_VPN "wikilink") と共通する仕様部分も併せて説明する。

## 概要

PacketiX VPN は[仮想LANカード](../Page/仮想LANカード.md "wikilink")および[仮想HUB](https://ja.wikipedia.org/wiki/仮想HUB "wikilink")により[イーサネット](../Page/イーサネット.md "wikilink")を[仮想化](../Page/仮想化.md "wikilink")することで、レイヤ2 VPNを構築できる。また、[レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")を仮想化することにより、レイヤ3 VPNを構築できる。

初版である PacketiX VPN 2.0 は、開発中に **SoftEther VPN 2.0** と呼ばれていた。PacketiX 2.0 は、[SoftEther 1.0](../Page/SoftEther_1.0.md "wikilink") の後継版として [2005年](../Page/2005年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink") に発表され、SoftEther 1.0 の開発者である[登大遊](../Page/登大遊.md "wikilink")が設立した[ソフトイーサ](../Page/ソフトイーサ.md "wikilink")社によって、製品の開発および販売が行われた。

同種のプロトコルを扱うソフトウェアとして、PacketiX VPN 3.0 の機能制限・オープンソース版に当たる[UT-VPN](https://ja.wikipedia.org/wiki/UT-VPN "wikilink")や、同じく PacketiX VPN 4.0 の機能制限・無償版に当たる [SoftEther VPN](https://ja.wikipedia.org/wiki/SoftEther_VPN "wikilink") があり、PacketiX VPN 3.0 以上の版を含めて、これらは PacketiX VPN 2.0 Build 5280 以降のバージョンと相互に接続が可能である\[1\]。

### 更新履歴

  - SoftEther VPN 2.0 (2.0x) \[2\]

<!-- end list -->

  - 2004年12月17日 - 2.0 Beta 1 Ver 2.00.2668
  - 2004年12月24日 - User-mode Router 2.0 Beta 1 <筑波ACルータ> Ver 2.00.2668
  - 2005年2月24日 - Beta 2 Ver 2.01.3600
  - 2005年5月17日 - Beta 3 Ver 2.03.4200
  - 2005年7月4日 - Beta 3.2 Ver 2.03.4340
  - 2005年9月7日 - Beta 4 Ver 2.04.4600
  - 2005年9月30日 - RC1 Ver 2.05.4800
  - 2005年11月7日 - RC2 Ver 2.06.5000

<!-- end list -->

  - PacketiX VPN 2.0 RTM (2.10) \[3\]

<!-- end list -->

  - 2005年12月3日 - RTM Ver 2.20 Build 5060 提供開始。
  - 2005年12月6日 - RTM Ver 2.20 Build 5070 提供開始。
  - 2005年12月25日 - RTM Ver 2.20 Build 5080 提供開始。
  - 2006年2月22日 - RTM Ver 2.20 Build 5090 提供開始。

<!-- end list -->

  - PacketiX VPN 2.0 Option Pack (2.20) \[4\]

<!-- end list -->

  - 2006年8月7日 - Ver 2.20 Build 5210 提供開始。
  - 2006年8月27日 - Ver 2.20 Build 5211 提供開始。
  - 2006年9月11日 - Ver 2.20 Build 5220 提供開始。
  - 2006年12月1日 - Ver 2.20 Build 5280 提供開始。

<!-- end list -->

  - PacketiX VPN 3.0 \[5\]

<!-- end list -->

  - 2010年3月15日 - Ver 3.00 Build 6890 提供開始。
  - 2010年10月10日 - Ver 3.01 Build 7177 提供開始。
  - 2011年2月28日 - Ver 3.02 Build 7392 提供開始。

<!-- end list -->

  - PacketiX VPN 4.0 \[6\]\[7\]

## ソフトウェアの形態

PacketiX VPN は以下のようなソフトウェアによって構成されている。

  - VPN Server (PacketiX VPN / UT-VPN / SoftEther VPN に共通)

VPN Client や VPN Bridge からの接続を受け付けるVPNサーバソフトウェア。VPN Server には複数個の[仮想ハブ](https://ja.wikipedia.org/wiki/仮想ハブ "wikilink")を作成することができ、仮想ハブ内で[イーサネットフレーム](https://ja.wikipedia.org/wiki/イーサネットフレーム "wikilink")を交換することができる。また、VPN Server 内の複数の仮想ハブ間でIPパケットの交換を行うために仮想レイヤ3スイッチを複数個作成することもできる。

  - VPN Client (PacketiX VPN / UT-VPN / SoftEther VPN に共通)

仮想LANカードとしての機能を持ったVPNクライアントソフトウェア。VPN Client をコンピュータにインストールすることで、VPN Server が接続されているLANなどに、インターネット経由でリモートアクセスすることができる。VPN Client を使用する場合は、仮想LANカードを作成し、その仮想LANカードを VPN Server 上で動作している仮想HUBに接続する形式で通信を行う。

  - VPN Bridge (PacketiX VPN / SoftEther VPN のみ)

VPN Server の仮想HUBにカスケード接続する為のVPN接続ソフトウェア。VPN Bridge を動作させているコンピュータ上の物理的なLANカードとの間でローカルブリッジを構成することにより、遠隔地のLAN同士を VPN 接続することが可能である。なお、VPN Bridge の機能は全て VPN Server に内包される。

  - サーバ管理マネージャ (PacketiX VPN / UT-VPN / SoftEther VPN に共通)

VPN Server および VPN Bridge に管理モードで接続して管理を行うための[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")管理ツールである。サーバ管理マネージャは VPN Server や VPN Bridge が動作しているサーバコンピュータ上に必ずしもインストールする必要はなく、別の管理用端末 (ノートパソコンなど) にインストールして使用することもできる。この場合は TCP/IP によって管理用のセッションが確立され遠隔管理が行われる。

  - コマンドライン管理ユーティリティ (PacketiX VPN / UT-VPN / SoftEther VPN に共通)

vpncmd の名称で提供される[CUIの管理ユーティリティ](../Page/キャラクタユーザインタフェース.md "wikilink")。原則としてGUIのサーバ管理マネージャで設定可能なすべての項目をコマンドラインから設定できる。コマンドラインによる通常の管理作業のほか、、自動生成したスクリプトを読み込ませることによって各種の管理操作を自動化することが可能である。また結果をファイルに書き出すこともできる。

### VPN Server

#### 製品版

PacketiX VPN Server は製品版として提供されており、PacketiX VPN 3.0 以降において下記のエディションが用意されている\[8\]。なお、エディションによっては法人向けの一部機能（RASIUD/NTドメイン認証、syslog 転送機能、パケットログ保存機能、クラスタリング機能）が利用できず、利用可能な機能やセッション数も異なる。

  - 法人向け

<!-- end list -->

  - Standard Edition
      - クライアント同時接続数: 30 同時接続
      - 拠点間接続: 2 拠点
      - 法人向けの一部機能が利用できない。
  - Professional Edition
      - クライアント同時接続数: 100 同時接続
      - 拠点間接続: 4 拠点
  - Enterprise Edition
      - クライアント同時接続数: 300 同時接続
      - 拠点間接続: 10 拠点
  - Ultimate Edition
      - クライアント同時接続数: 無制限
      - 拠点間接続: 無制限

<!-- end list -->

  - 個人向け

<!-- end list -->

  - HOME Edition
      - クライアント同時接続数: 2 同時接続
      - 法人向けの一部機能、拠点間接続が利用できない
  - Small Business Edition
      - クライアント同時接続数: 5 同時接続
      - 拠点間接続: 2 拠点
      - 法人向けの一部機能が利用できない。

PacketiX VPN Server を動作させるためには、ソフトイーサ等より提供されるライセンスキーが必要である。PacketiX VPN Server には前述のように多数のエディションがあるが、*シングルバイナリ*によって提供されており、入力するライセンスキーの種類によって動作の内容が異なる。

#### 無償版

PacketiX VPN 2.0 には、かつて一般向けの Free Edition や、学術研究者向けに無償でライセンスされた Academic Edition が提供されていた。

PacketiX VPN 3.0 以降は、製品版に対する実質的な機能制限版である [UT-VPN](https://ja.wikipedia.org/wiki/UT-VPN "wikilink") や、[SoftEther VPN](https://ja.wikipedia.org/wiki/SoftEther_VPN "wikilink") などが、関連プロジェクトより提供されている。これらのソフトウェアでは、組み込まれているソースコードの権利等の問題から、PacketiX VPN において法人向けと位置付けられている一部の機能等が利用できない。但し、これらのソフトウェアにクライアント接続数や拠点接続数の制限はない。

  - UT-VPN

<!-- end list -->

  - SoftEther VPN

SoftEther VPN は、[筑波大学](../Page/筑波大学.md "wikilink")の研究プロジェクトとして開発され、[ソフトイーサ](../Page/ソフトイーサ.md "wikilink")の主力製品である**PacketiX VPN 4.0**をベースに一部機能を制限し\[9\]、2013年7月にフリーウェアとして公開された\[10\]。[UT-VPN](https://ja.wikipedia.org/wiki/UT-VPN "wikilink")の後継プロジェクトとして\[11\]、今後はソースコードの公開が予定されている\[12\]。

### VPN Client/Bridge

PacketiX VPN Client および VPN Bridge は無償提供されており、PacketiX および派生ソフトウェアを含めて VPN Client および VPN Bridge の利用にライセンスキーは不要である。

## ソフトウェアの仕様

### 動作環境

PacketiX VPN 4.0 は、以下のようなオペレーティングシステムおよびCPUの組み合わせで動作する\[13\]。

  - **[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")**
      - 対応バージョン
          - サポート対象は、下記のうちサポートライフサイクル範囲内のバージョンのみ。
        <!-- end list -->
        1.  Windows 98 / 98 SE / ME
        2.  Windows NT 4.0 SP6a
        3.  Windows 2000 SP4
        4.  Windows XP SP2, SP3
        5.  Windows Server 2003 Standard Edition SP2
        6.  Windows Vista SP1, SP2
        7.  Windows Server 2008 SP1, SP2
        8.  Hyper-V Server 2008
        9.  Windows 7 SP1
        10. Windows Server 2008 R2 SP1
        11. Hyper-V Server 2008 R2 SP1
        12. Windows 8
        13. Windows Server 2012
        14. Hyper-V Server 2012
      - CPU アーキテクチャ
        1.  [Intel x86](https://ja.wikipedia.org/wiki/x86 "wikilink") (32bit)
        2.  [Intel x64](https://ja.wikipedia.org/wiki/x64 "wikilink") (64bit)

<!-- end list -->

  - **[Linux](../Page/Linux.md "wikilink")**
      - 対応バージョン
          - サポート対象は、商用サポート期間中の [Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") と、その同等OS（[CentOS](../Page/CentOS.md "wikilink")）のみ。
        <!-- end list -->
        1.  Linux Kernel 2.4
        2.  Linux Kernel 2.6
        3.  Linux Kernel 3.x
      - CPU アーキテクチャ
        1.  Intel x86 (32bit)
        2.  Intel x64 (64bit)
        3.  [PowerPC](../Page/PowerPC.md "wikilink") (32bit)
        4.  [MIPS Little-Endian](https://ja.wikipedia.org/wiki/MIPS "wikilink") (32bit)
        5.  [ARM EABI](../Page/ARMアーキテクチャ.md "wikilink") (32bit)
        6.  ARM legacy ABI (32bit)
        7.  [SH4](../Page/SuperH.md "wikilink") (32bit)

<!-- end list -->

  - **[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")**
      - 対応バージョン
        1.  Mac OS X 10.4 Tiger
        2.  Mac OS X 10.5 Leopard
        3.  Mac OS X 10.6 Snow Leopard
        4.  Mac OS X 10.7 Lion
        5.  Mac OS X 10.8 Mountain Lion
      - CPU アーキテクチャ
        1.  Intel x86 (32bit)
        2.  Intel x64 (64bit)
        3.  PowerPC (32bit)
        4.  PowerPC G5 (64bit)

<!-- end list -->

  - **[FreeBSD](../Page/FreeBSD.md "wikilink")**
      - 対応バージョン
        1.  FreeBSD 5
        2.  FreeBSD 6
        3.  FreeBSD 7
        4.  FreeBSD 8
        5.  FreeBSD 9
      - CPU アーキテクチャ
        1.  Intel x86 (32bit)
        2.  Intel x64 (64bit)

<!-- end list -->

  - **[Solaris](../Page/Solaris.md "wikilink")**
      - 対応バージョン
        1.  Solaris 8
        2.  Solaris 9
        3.  Solaris 10
        4.  Solaris 11
      - CPU アーキテクチャ
        1.  Intel x86 (32bit)
        2.  Intel x64 (64bit)
        3.  [SPARC](../Page/SPARC.md "wikilink") (32bit)
        4.  SPARC (64bit)

一部OSを除いて32ビット版と64ビット版が用意されており、64ビット版ではより多くの仮想 HUB および同時接続 VPN セッションを1台の VPN Server に収納することができる。

### VPN通信プロトコルの仕様

PacketiX VPN でのVPN通信に使用されているプロトコルは以下のような仕様となっている。

  - 通信プロトコル
      - [SSLバージョン](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")3.0およびTCP/IPが使用されている。
      - [SSL](https://ja.wikipedia.org/wiki/SSL "wikilink") / [HTTP over SSL (HTTPS)拡張プロトコル準拠](../Page/HTTPS.md "wikilink")。
  - ポート番号
      - 任意。デフォルトでTCPポート443、992、8888（派生ソフトウェアの一部は5555）が利用可能となっている。
  - 暗号化・電子署名アルゴリズム
      - RC4-MD5 / RC4-SHA / AES128-SHA / AES256-SHA / DES-CBC-SHA / DES-CBC3-SHA
  - データ圧縮
      - ストリーム型データ圧縮
  - 高速通信機能
      - 物理的な1本〜32本のTCPコネクションによる効率的負荷分散およびタイミング制御。
  - 自動再接続
      - 無限回数または指定した回数
  - 接続方法
    1.  直接TCP/IP接続
    2.  HTTP[プロキシ](../Page/プロキシ.md "wikilink")サーバ経由接続
    3.  SOCKSプロキシサーバ経由接続
  - ユーザー認証(クライアント認証)方式
    1.  匿名認証
    2.  標準[パスワード](../Page/パスワード.md "wikilink")認証
    3.  [Radiusサーバを使用した認証](../Page/RADIUS.md "wikilink")
    4.  [NTドメインコントローラまたは](../Page/Microsoft_Windows_NT.md "wikilink")[Active Directoryを使用した認証](../Page/Active_Directory.md "wikilink")
    5.  [X.509](../Page/X.509.md "wikilink")証明書と[RSAを使用した](../Page/RSA暗号.md "wikilink")[PKI認証](https://ja.wikipedia.org/wiki/公開鍵基盤 "wikilink")

### VPN通信が可能なパケットの種類

PacketiX VPN でのVPN通信では、標準的なイーサネットフレーム（MACフレーム、イーサネットパケット）であればどのようなものでも通信を行うことが可能である。したがって、[IPv4](../Page/IPv4.md "wikilink")、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")、[TCP](../Page/Transmission_Control_Protocol.md "wikilink")、[UDPなどの現在インターネットやLANなどで使用されている一般的なプロトコルのほか](../Page/User_Datagram_Protocol.md "wikilink")、[NetBEUI](../Page/NetBEUI.md "wikilink")や[IPX/SPX](https://ja.wikipedia.org/wiki/IPX/SPX "wikilink")などのプロトコルもVPNを通すことができる。

### 多言語対応

2007年11月、ソフトイーサは PacketiX VPN 2.0 の英語版をリリースした\[14\]。日本語版と英語版は、ユーザーインターフェイスやオンラインマニュアルなどの言語が異なるのみであり、機能は同等である。異なる言語のVPNソフトウェア同士でVPN接続を行うこともできる。

2010年3月に発表された PacketiX VPN 3.0 では、中国語簡体字に対応している\[15\]

## 動作原理

PacketiX VPN の VPN 機能の動作は[IPsec](../Page/IPsec.md "wikilink")や[PPTP](https://ja.wikipedia.org/wiki/PPTP "wikilink")などの従来のVPNと比較して異なる点がある。

### 仮想スイッチと仮想LANカード

  - 仮想HUB

PacketiX VPN における**[仮想HUB](https://ja.wikipedia.org/wiki/仮想HUB "wikilink")**は、既存の一般的な[スイッチングHUBと同等の機能をソフトウェアで実現したものである](../Page/ハブ_\(ネットワーク機器\).md "wikilink")。仮想HUBはMACアドレス学習機能や学習に基づくフレームの交換機能を持つ。従来のスイッチングHUBはハードウェアとしてこの処理を行っていたが、PacketiX VPN ではソフトウェアとして同様の処理を行う。VPN Server には複数の仮想HUBを作成できる。それぞれの仮想HUBがVPN経由で流れてきたイーサネットフレームを処理することで、仮想的なレイヤ2のイーサネットセグメントを実現している。

VPN Server 内に複数台の仮想HUBを作成するとき、通常はそれらの仮想HUBは独立して動作し、お互いに干渉せず、別々の仮想HUB間で通信は行われない。また、各仮想HUBの管理権限を別々の管理者に委譲することが可能である。この場合、特定の仮想HUBの管理者は、自分が委任されている仮想HUBのみ管理でき、それ以外の仮想HUBにはアクセスできない。

  - 仮想LANカード

物理的な[LANカード](../Page/ネットワークカード.md "wikilink") (NIC) をソフトウェアによって仮想化することにより**[仮想LANカード](../Page/仮想LANカード.md "wikilink")**が実現される。仮想LANカードはVPNプロトコルを用いて、物理的な TCP/IP ネットワークを経由し、遠隔地にある VPN Server 内の仮想HUBに VPN 接続することができる。VPN Client を用いると、仮想LANカードをクライアントコンピュータのOS内にいくつでも作成することが可能である。仮想LANカードは OS から物理的な LAN カードと同様に認識されるため、原則としてイーサネットでの通信に対応したほぼすべてのプロトコルやアプリケーションが、特に手を加えることなく利用可能である。

  - 仮想レイヤ3スイッチ

**[仮想レイヤ3スイッチ](https://ja.wikipedia.org/wiki/仮想レイヤ3スイッチ "wikilink")** は、IPルーティングを行う[レイヤ3スイッチ](../Page/レイヤ3スイッチ.md "wikilink")をソフトウェア的に仮想化したものである。仮想レイヤ3スイッチにより、別々のIPネットワーク間で、イーサネットのセグメントを分離したまま、ルーティングによりネットワーク同士を接続することが可能である。

仮想HUBと同様に、VPN Server 内には仮想レイヤ3スイッチを複数作成できる。複数の仮想HUB間でIPルーティングを行うことにより、仮想HUB間通信を実現することができる。これを応用すると、遠隔地にある複数のイーサネットセグメント間のレイヤ3でのルーティングが実現される。

### 接続

  - 仮想HUBと仮想LANカードの接続

1台の仮想HUBに複数台のコンピュータの仮想LANカードが接続すると、それぞれのコンピュータ間は自由にイーサネットフレームを送受信することができるようになる。これにより VPN 接続が実現される。

  - 仮想HUB間のカスケード接続

仮想HUB間のカスケード接続を行うことにより、通常の物理的なスイッチングHUB間をクロスケーブルなどでカスケード接続した場合と同じ効果が得られる。すなわち、もともと分離されていた2個のイーサネットセグメントを1つにすることができる。仮想HUB間のカスケード接続は、同一の VPN Server 内の仮想HUB同士だけでなく、物理的に別の VPN Server 内の仮想HUB同士でも、VPNセッションを確立することによって可能である。これにより、遠隔地にある複数のイーサネットセグメント間のレイヤ2での[ブリッジ接続](../Page/ブリッジ接続.md "wikilink")が実現される。

  - 仮想ネットワークと物理ネットワークのブリッジ接続

上記で述べたような仮想HUBや仮想レイヤ3スイッチはあくまでもソフトウェアによってエミュレーションされたネットワーク機器であり、そのままでは仮想的に流れるイーサネットフレームは物理的なネットワーク上に出ることはない。VPN Server および VPN Bridge では、仮想HUBと既存の物理的なイーサネットのセグメントとを、物理的なLANカードを指定することによって[ブリッジ接続](../Page/ブリッジ接続.md "wikilink")することができる。これを**ローカルブリッジ**と呼ぶ。

ローカルブリッジを用いることにより、複数の拠点で、仮想HUBと物理的な既存のLANとの間を接続し、さらに仮想HUB同士を前述したカスケード接続によって VPN 接続することによって、インターネット経由で複数のイーサネットセグメント間のレイヤ2でのブリッジ接続が実現される。

## 機能と特徴

以下、PacketiX VPN に搭載されている VPN 通信機能および特徴について述べる。

### イーサネットの仮想化

[IPsec](../Page/IPsec.md "wikilink")や[PPTP](https://ja.wikipedia.org/wiki/PPTP "wikilink")などの従来のレイヤ3をトンネリング対象としていたVPNプロトコルと異なり、PacketiX VPN ではレイヤ2のイーサネットフレームをVPN通信におけるトンネリング対象とし、トンネルを通してイーサネットフレームを流すことができる。レイヤ2での拠点間接続が可能な為、専用線的サービスにおける[広域イーサネット](../Page/広域イーサネット.md "wikilink")と同様の接続方法を実現できる。これにより、レイヤ3のプロトコルの種類にかかわらず、イーサネット上で利用可能なプロトコルをVPN通信上に流すことができる。

### NAT、プロキシ、ファイアウォールの通過

PacketiX VPN は、物理的な通信のためのプロトコルとして、[GREなどの特別なプロトコルではなく](https://ja.wikipedia.org/wiki/ポイント・ツー・ポイント・トンネリング・プロトコル "wikilink")、標準的なTCP規格を採用している。これにより、すべてのVPN通信をTCP上で実現するため、ほとんどのNAT、プロキシ、ファイアウォールの通過することが可能である。また、デフォルトでTCP443番という[HTTPS](../Page/HTTPS.md "wikilink")通信で一般的に利用されるポートと同一のTCPポートを使用することが可能となっているため、基本的にWebサイトが閲覧できるようなネットワーク環境では PacketiX VPN を用いてVPN通信を行うことが可能である。

### 高速なVPN通信の実現

従来のVPNプロトコルのうち、セキュリティの確保のみに注力しているものについては、VPN処理がボトルネックとなり、実際にVPN通信を行った際のスループットが低くなることがある。PacketiX VPN 2.0は各種の通信回線に合わせて最適化を行う為、通常のPCサーバを用いて**約3.1Gbps**程度の高速なVPN通信を行うことができるとしている。\[16\]

### 移植性の高さ

PacketiX VPN は様々なOSやCPU上で動作するように移植性の高いプログラミングによって開発されており、通常のエディションにおいて、前述のように多くの種類のOSやCPUに対応する。

### セキュリティ機能

PacketiX VPN は以下のようなセキュリティ機能を搭載している。

  - ユーザー認証

許可されていない第三者による不正なVPN接続を禁止するため、以下のようなユーザー認証が可能である。

  - 匿名認証 - : 実質的に認証を必要としないVPN (誰でも接続可能なVPNサーバ) を実現するために使用する認証方法である。[FTPサーバにおけるanonymousアカウントと同様である](../Page/File_Transfer_Protocol.md "wikilink")。
  - 標準パスワード認証 - ユーザー名とパスワードによってユーザー認証を行う。ユーザーアカウントのデータベースは VPN Server が保有する。
  - Radiusサーバ認証 - ユーザー名とパスワードによってユーザー認証を行う。ユーザーアカウントのデータベースは、既存の[Radiusサーバを利用する](../Page/RADIUS.md "wikilink")。
  - NTドメイン / ActiveDirectory 認証 - ユーザー名とパスワードによってユーザー認証を行う。ユーザーアカウントのデータベースは、既存の[NTドメインコントローラまたは](../Page/Microsoft_Windows_NT.md "wikilink")[Active Directoryのサーバを利用する](../Page/Active_Directory.md "wikilink")。
  - 証明書認証 (PKI認証) - クライアント証明書 ([X.509](../Page/X.509.md "wikilink")証明書) と[RSAを使用した](../Page/RSA暗号.md "wikilink")[PKI認証](https://ja.wikipedia.org/wiki/公開鍵基盤 "wikilink")。パスワードなどの固定文字列を用いないせず、よりセキュアな[スマートカードや](../Page/ICカード.md "wikilink")[セキュリティトークン](../Page/セキュリティトークン.md "wikilink")を用いた認証が可能。

<!-- end list -->

  - 暗号化と電子署名

盗聴者が存在する可能性のあるネットワークを経由してVPNを利用する際に、盗聴やデータの改ざんを防止するため、すべてのVPN通信パケットに対して、暗号化と電子署名を行うことが可能である。[SSLのバージョン](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")3で暗号化セッションが確立され、内部では[HTTP over SSL (HTTPS)拡張プロトコルが用いられる](../Page/HTTPS.md "wikilink")。

  - サーバ証明書の検証

PacketiX VPN では、接続先のVPNサーバが提示するX.509証明書とSSLプロトコル内で行われる正当性検証手続きにより、接続先のVPNサーバが本物であるかどうかの検証が可能である。検証に失敗した場合はVPN接続を中止し、[中間者攻撃](https://ja.wikipedia.org/wiki/中間者攻撃 "wikilink")を防止する。

  - スマートカードの利用

VPN Client において、認証方法として証明書認証 (PKI認証) を使用する場合は、セキュアなハードウェアである[スマートカードや](../Page/ICカード.md "wikilink")[セキュリティトークン](../Page/セキュリティトークン.md "wikilink")を用いた認証が可能である。一般的なPKCS\#11規格に対応したデバイスに対応する。

### パケットフィルタリング機能

VPN Server の仮想HUBには、以下の2種類のパケットフィルタリング機能が搭載されている。

  - アクセスリスト

アクセスリストとは、一般的な[ファイアウォール](../Page/ファイアウォール.md "wikilink")機器で実現されるような、IPパケットのヘッダ部をリアルタイムで検査し、あらかじめ設定したルールに基づいて通過/破棄を決定する仕組みである。

  - セキュリティポリシー

セキュリティポリシーとは、ダイナミックなパケットの流れを監視して通過/破棄を決定する仕組みである。セキュリティポリシーを適用するため、仮想HUBは流れるすべての仮想イーサネットフレームについてリアルタイムで高レイヤまでパケットの内容を解釈する。解釈結果を元にして、そのパケットがセキュリティポリシーに適合した通信内容であるかどうかを判別する。セキュリティポリシーに違反したパケットが流れた場合は監査記録を保存することも可能である。

### モニタリング機能

VPN Server の管理者は、仮想HUBに**モニタリングモードセッション**という特別なセッションを作成することにより、その仮想HUB内を流れるすべてのパケットを傍受したり、物理的なLANカードから出力して既存の[IDS製品に入力したりすることができる](../Page/侵入検知システム.md "wikilink")。

### パケットログの保存

仮想HUB内を流れるすべてのパケットをログに保存することが可能である。これにより、管理者は事後にトラブルの追跡や不正アクセスの発見などを行うことができる。パケットログの対象となるパケットは仮想HUBの管理者が細かく設定することができる。この場合、パケットの内容すべてを保存するか、ヘッダ部分のみを保存するかを選択することができる。パケットログの取りこぼしを防ぐため、バッファの空き容量が少なくなると自動的に仮想HUBにおける通信速度を調節し、すべてのパケットログが確実にディスクに書き込まれるような仕組みになっている。

### SecureNAT

仮想HUBには**SecureNAT機能**が搭載されており、仮想NATと仮想DHCPサーバの2つの機能が利用可能である。SecureNAT機能はすべての機能が[ユーザーモードで動作し](../Page/CPUモード.md "wikilink")、一般ユーザー権限で全機能が利用可能である。SecureNAT機能を利用することで、一般的なブロードバンドルータと同等程度の機能を、仮想HUB内で利用することができる。

### クラスタリング

大量のVPNセッションを処理したり、極めて多数の仮想HUBを作成したりするために、クラスタリング機能が提供されている。クラスタリング機能により複数台の VPN Server をまとめて動作させることができ、仮想HUBや仮想HUB内のユーザーデータベースやアクセスリストなどの設定が一元化される。また、[ロードバランシングと](../Page/サーバロードバランス.md "wikilink")[フォールトトレランスが実現される](../Page/フォールトトレラントシステム.md "wikilink")。クラスタリングにより多数の VPN Server が動作している場合であっても、ユーザーや各仮想HUBの管理者から見ると、1つのVPN Serverのシステムとして認識される。したがって、ユーザーや各仮想HUBの管理者は、クラスタリング機能が動作していることに関して意識する必要がない。

## 構築できるネットワークの種類

PacketiX VPN を用いることにより構築することができるネットワークをおおまかに分類すると、以下のようになる。

  - コンピュータ間VPN
    最も単純なVPNの形態である。インターネット上のどこかに設置した仮想HUBに対して、その仮想HUBによって構成される仮想イーサネットセグメントに、複数台のコンピュータのVPN Clientから接続することにより、それらのコンピュータ間でVPN通信が可能になる。
  - リモートアクセスVPN
    コンピュータ間VPNではVPN通信を行いたいコンピュータすべてにVPN Clientをインストールする必要があり手間がかかる。また、既存の物理的なLANに対してVPNを用いてリモートアクセスすることができない。
    そこで、仮想HUBと既存のLANとの間をローカルブリッジによって接続することにより、その仮想HUBにリモートアクセスしたVPN Clientは既存のLANに直接接続しているのと同様な状態になる。これがリモートアクセスVPNである。例えば、社内にリモートアクセスVPNのためのVPN Serverを設置しておけば、社外から社内LANに接続して作業を行うことができる。
  - 拠点間接続VPN
    離れた場所にある物理的なLAN同士を接続する方法である。従来の専用線やフレームリレー、広域イーサネットなどの代替手段として利用できる。
    レイヤ2によって[ブリッジを行う接続方法と](../Page/ブリッジ接続.md "wikilink")、レイヤ3によってルーティングを行う接続方法がある。ネットワークの規模や状況によっていずれか、または両者を組み合わせた方法で接続する。

## 実験サービス

[ソフトイーサ](../Page/ソフトイーサ.md "wikilink")は学術研究目的でPacketiX VPN を用いた以下のサービスを実験的に無償で提供している。

  - [PacketiX.NET](http://www.packetix.net/jp/)
      - [PacketiX.NET ASP型VPN実験サービス](http://www.packetix.net/jp/vpn/) (2006年10月から)
      - [PacketiX.NET セキュアインターネット実験サービス](http://www.packetix.net/jp/secure/) (2004年12月から)
  - <http://www.mobilefree.jp/jp/> MobileFree.jp VPN 実験サービス\] (2007年10月から)
  - [つくばエクスプレス つくば駅前 高画質ライブカメラ ストリーミング配信](http://www.tsukuba-ac.jp/) (2006年4月から)

## 受賞

PacketiX VPN は以下のような賞を受賞している。

  - **MM総研大賞2006「話題賞」** ([MM総研](https://ja.wikipedia.org/wiki/MM総研 "wikilink")、2006年)
  - **ソフトウェア・プロダクト・オブ・ザ・イヤー2006「グランプリ」** ([独立行政法人情報処理推進機構](https://ja.wikipedia.org/wiki/独立行政法人情報処理推進機構 "wikilink")、2006年)
  - **経済産業大臣表彰** ([経済産業省](../Page/経済産業省.md "wikilink")、2007年)

## 関連書籍

  - ソフトイーサ PacketiX VPN入門 (大澤 文孝、工学社、2006年) ISBN 4-7775-1203-7
  - 公式SoftEther活用ガイド (登大遊／村上和美／池嶋俊、[アスキー](../Page/アスキー_\(企業\).md "wikilink")、2004年) ISBN 4-7561-4483-7
  - 魔法のトンネルSoftEther (ランディス、秀和システム、2004年) ISBN 4-7980-0809-5
  - SoftEther+VPN構築ガイド (塩見 豊久／ケイズプロダクション、アスペクト、2004年) ISBN 4-7572-1066-3
  - ハッカー御用達\!魔法のソフトウェアガイドブックSoftEther入門 (IPUSIRON、データハウス、2004年) ISBN 4-88718-759-9
  - 失敗しないVPN構築―VPNベストチョイス/SoftEther自由自在 (アスキー、2004年) ISBN 4-7561-4569-8

## 関連項目

  - 関連ソフトウェア

<!-- end list -->

  - [UT-VPN](https://ja.wikipedia.org/wiki/UT-VPN "wikilink") - PacketiX VPN 3.0 をベースとしたオープンソースのVPNソフトウェア
  - [SoftEther 1.0](../Page/SoftEther_1.0.md "wikilink") - PacketiX VPN 4.0 をベースとした無償のVPNソフトウェア

<!-- end list -->

  - 開発元

<!-- end list -->

  - [ソフトイーサ](../Page/ソフトイーサ.md "wikilink")株式会社
  - [登大遊](../Page/登大遊.md "wikilink")

<!-- end list -->

  - その他の関連項目

<!-- end list -->

  - [VPN](../Page/Virtual_Private_Network.md "wikilink")
  - [TinyVPN](https://ja.wikipedia.org/wiki/TinyVPN "wikilink")

## 外部リンク

  - [ソフトイーサ Web サイト](http://www.softether.jp/)

## 脚注

<references/>

[en:PacketiX VPN](https://ja.wikipedia.org/wiki/en:PacketiX_VPN "wikilink")

[Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink") [Category:情報処理推進機構](https://ja.wikipedia.org/wiki/Category:情報処理推進機構 "wikilink") [Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink")

1.  [UT-VPN よくある質問](http://utvpn.tsukuba.ac.jp/ja/qa/)
2.  [ソフトウェアバージョンアップ履歴 (ChangeLog)](http://www2.softether.jp/jp/vpn2/changelog/)
3.
4.
5.  [PacketiX VPN 3.0 ソフトウェア更新履歴](http://www2.softether.jp/en/vpn3/changelog/)
6.  [ダウンロード・更新履歴](http://www.softether.jp/1-product/11-vpn/81-download)
7.  [バージョン更新履歴](http://ja.softether.org/5-download/history)
8.
9.
10.
11.
12.
13.
14. [PacketiX VPN 2.0 英語版](https://www.softether.co.jp/jp/news/071012.aspx)
15. [PacketiX VPN 3.0 Web サイト](http://www2.softether.jp/jp/vpn3/)
16. [日経ITproによるPacketiX VPNの通信速度に関する記事](http://itpro.nikkeibp.co.jp/article/NEWS/20060608/240438/)