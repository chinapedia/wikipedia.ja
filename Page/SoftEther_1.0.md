> この記事は[SoftEther 1.0](https://ja.wikipedia.org/wiki/SoftEther_1.0)から翻訳されています。


**SoftEther 1.0**（ソフトイーサ いってんぜろ）は[登大遊](../Page/登大遊.md "wikilink")によって開発され、[2003年](../Page/2003年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")に発表された[VPN](../Page/Virtual_Private_Network.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")。

現在は開発・公開は終了している。現役の後継バージョンについては、[PacketiX VPNおよび](../Page/PacketiX_VPN.md "wikilink")[SoftEther VPNを参照のこと](https://ja.wikipedia.org/wiki/SoftEther_VPN "wikilink")。

## 概要

SoftEther 1.0は[LANカード](../Page/Local_Area_Network.md "wikilink")・[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")を忠実にエミュレートしEthernet Over IPを実現。通常の[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")上に仮想[イーサネット](../Page/イーサネット.md "wikilink")を作ることができる。[HTTP Proxy](https://ja.wikipedia.org/wiki/HTTP_Proxy "wikilink")/ [SSH](../Page/Secure_Shell.md "wikilink") / [Socks](https://ja.wikipedia.org/wiki/Socks "wikilink") のいずれかを使って通信するため、通常の[ファイアウォール](../Page/ファイアウォール.md "wikilink")を通過することが可能である。これらの機能のうち一部を搭載したVPNソフトウェアは以前にも存在したが、SoftEther 1.0が反響を呼んだのは、それまで有償製品が主流であったWindows向けのVPNソフトウエアに無償ソフトウエアとして分け入ったこと、従来のVPNソフトウエアの設定がネットワークに関する知識を必要としていたことに対し、SoftEther 1.0ではごく簡単なインストールだけでVPN機能が使えたこと、[PPTP](https://ja.wikipedia.org/wiki/PPTP "wikilink")や[IPsec](../Page/IPsec.md "wikilink")などのレイヤ3を仮想化するVPN技術と比較してレイヤ2（Ethernet）を仮想化することにより柔軟なVPN構築が可能となったことなどが評価されたためである。

SoftEther 1.0は[情報処理振興事業協会](https://ja.wikipedia.org/wiki/情報処理振興事業協会 "wikilink")（IPA）が主催する未踏ソフトウェア創造事業 未踏ユース部門に採択され、支援をうけ開発された。[登大遊](../Page/登大遊.md "wikilink")が個人で運営していた[SoftEther.com Webサイト](http://www.softether.com/)（後に[ソフトイーサ](../Page/ソフトイーサ.md "wikilink")が運営）で配布されていた無料版のほか、法人向けの商用版[SoftEther CAが](https://ja.wikipedia.org/wiki/SoftEther_CA "wikilink")[三菱マテリアル](../Page/三菱マテリアル.md "wikilink")株式会社から発売されている。

未踏ソフトウェア創造事業のプロジェクト期間の終了に伴い、SoftEther 1.0の開発は2004年3月に終了した。その後、開発者の登が中心となって起業した[筑波大学](../Page/筑波大学.md "wikilink")発ベンチャー企業である[ソフトイーサ](../Page/ソフトイーサ.md "wikilink")が後継バージョンである[SoftEther VPN 2.0](https://ja.wikipedia.org/wiki/SoftEther_VPN_2.0 "wikilink")（開発時のソフトウェアの名称）の開発を開始した。

SoftEther VPN 2.0は2005年12月に開発が完了し、[PacketiX VPN 2.0としてリリースされた](../Page/PacketiX_VPN.md "wikilink")。

### 動作環境

  - [Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")
  - [Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")
  - [Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink")
  - [Linux](../Page/Linux.md "wikilink")版（仮想LANカードはサポート対象外）

### 構成

SoftEther 1.0を構成する主なソフトウェアは以下の通りである。

  - [サービス](../Page/サービス.md "wikilink")
      - SoftEther仮想HUBサービス - インストールされたコンピュータを仮想スイッチングハブとして機能させる。仮想ハブの管理は専用の管理[クライアントソフトウェア](../Page/クライアント_\(コンピュータ\).md "wikilink")（後述）または[Telnet](../Page/Telnet.md "wikilink")接続を用いて行う。
      - SoftEther仮想LANカードサービス - 仮想LANカードの制御・仮想ハブとの通信を行う。

※上記2つは独立してインストール可能。

  - [デバイスドライバ](../Page/デバイスドライバ.md "wikilink")
      - SoftEther仮想LANカードアダプタ - 通常のLANカード同様、Windowsのデバイスマネージャに登録され、コントロールパネルの「ネットワーク接続」から設定可能。[MACアドレス](../Page/MACアドレス.md "wikilink")は自動で設定される。
  - 管理用ソフトウェア
      - SoftEtherドライバとサービスの設定 - 上記3つの起動／停止／インストール／アンインストール、仮想LANカードに付けられたMACアドレスの設定変更 をここから行える。
      - SoftEther仮想HUB管理クライアント - 仮想ハブがインストールされたコンピュータに接続し管理コンソールを開く。
      - SoftEther接続マネージャ - 仮想ハブへの接続／切断を行う。HTTP Proxy／SSH／Socks経由での接続が必要な場合はここで設定する。

### 主な機能

  - 仮想LAN上での通信は独自の[通信プロトコル](../Page/通信プロトコル.md "wikilink")（SoftEtherプロトコル）を用いて行われる。[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")（OS）やネットワーク機器はSoftEtherプロトコルを含む[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")[パケット](../Page/パケット.md "wikilink")を通常のTCP/IPパケットと区別できないため、一般的なファイアーウォール等を通り抜けることが可能である。
  - 仮想LANカードをインストールしたコンピュータ上で、WindowsXPまたはWindowsServer2003の機能を用いて仮想LANと物理LANをブリッジ接続することができる。
  - 仮想LAN内で[DHCP](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")・[NATの運用が可能である](https://ja.wikipedia.org/wiki/IPマスカレード "wikilink")。
  - 仮想ハブによる[パケットフィルタリング機能](../Page/ファイアウォール.md "wikilink")、[ログ保存機能](https://ja.wikipedia.org/wiki/サーバログ "wikilink")。
  - 仮想ハブ[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")と仮想LANコンポーネントの両方を1台のコンピュータにインストールすることにより、クライアントとなるコンピュータが仮想ハブの機能を兼ねることができる。

## 危険性と反響

### 公開に伴うセキュリティリスクの懸念にまつわる話

SoftEther 1.0を使用することにより、社内LANと外部のコンピュータをネットワーク管理者の許可なく接続することが可能となる。また、ネットワークに関する十分な知識を持たない者がSoftEther 1.0を使用すると社内LANに重大な悪影響を及ぼしかねない。このため発表直後から「SoftEther 1.0を使用することが[セキュリティホール](../Page/セキュリティホール.md "wikilink")の原因になるのではないか」等の懸念の声がIPA及び[経済産業省](../Page/経済産業省.md "wikilink")に多数寄せられた。IPAはこれを受けて登に公開停止を強く要請、登は2003年12月24日からSoftEther 1.0の公開を一時停止した。その後登とIPAによる協議を経て、同月27日より公開が再開されている。

### 通信遮断ツール

2004年1月、SoftEther 1.0の通信ブロックに機能を絞ったファイアーウォールソフトウェア「One Point Wall SoftEther」がネットエージェント株式会社より発売された。またソフトイーサ社自身もSoftEther 1.0通信の検出・監視用ソフトウェア「SoftEtherAlert」と遮断用ソフトウェア「SoftEther Block」を開発し、同年8月から無料配布している。

### 適切な管理がされていればリスクは少ない

SoftEther 1.0が動作するには仮想ネットワークカードの[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")が必要であり、いずれの版も**インストールするには導入先OSの管理者特権が必要である**。したがって、主なクライアントOSとなるWindows XPをクライアントとする場合、

  - 社内で用いるPCとアカウントはきちんと会社で管理する
  - 一般の社員にはAdministrator権限を与えない
  - 私物のPCを会社のネットワークには接続させない

というNT系Windowsの設計思想を考えれば当然とも言える運用を行っていれば、SoftEther 1.0の導入にまつわるセキュリティリスクは極めて低く抑えられる。

## 関連書籍

  - 公式SoftEther活用ガイド（登大遊／村上和美／池嶋俊、[アスキー](../Page/アスキー_\(企業\).md "wikilink")、2004年） ISBN 4-7561-4483-7
  - 魔法のトンネルSoftEther（ランディス、秀和システム、2004年） ISBN 4-7980-0809-5
  - SoftEther+VPN構築ガイド（塩見 豊久／ケイズプロダクション、アスペクト、2004年） ISBN 4-7572-1066-3
  - ハッカー御用達\!魔法のソフトウェアガイドブックSoftEther入門（IPUSIRON、データハウス、2004年） ISBN 4-88718-759-9
  - 失敗しないVPN構築―VPNベストチョイス/SoftEther自由自在（アスキー、2004年） ISBN 4-7561-4569-8

## 外部リンク

  - [ソフトイーサ公式サイト](http://www.softether.com/jp/)
      - [公開停止の経緯と開発者の見解](http://www.softether.com/jp/news/0312243.aspx)
  - [SoftEther CAサイト](http://www.kisp.jp/SECA/index.html)
  - [ネットエージェント社公式サイト](http://www.netagent.co.jp/)

[Category:VPN](https://ja.wikipedia.org/wiki/Category:VPN "wikilink") [Category:情報処理推進機構](https://ja.wikipedia.org/wiki/Category:情報処理推進機構 "wikilink") [Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink")