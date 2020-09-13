> この記事は[IEEE 802.1X](https://ja.wikipedia.org/wiki/IEEE_802.1X)から翻訳されています。


**IEEE 802.1X**とは、[LAN接続時に使用する](../Page/Local_Area_Network.md "wikilink")[認証](../Page/認証.md "wikilink")規格（認証[VLAN](https://ja.wikipedia.org/wiki/VLAN "wikilink")）である。接続を認めた端末機器以外が[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")に参加しないように認証によって接続を規制する。有線と無線の接続に使用できる検疫ネットワークのデータリンク層の技術である。

この標準はIEEE Standard for Local and metropolitan area networks--Port-Based Network Access Controlで規定されており、初版が2001年に、改定版が2004年に、最新版が2010年に発行されている。2014年に802.1Xbx、2018年に802.1Xckという追補（ammendment）を発行している。

IEEE 802.1Xを使った認証システムは、以下のものから構成される。

  - **サプリカント**（Supplicant） - [認証](../Page/認証.md "wikilink")[クライアント](../Page/クライアント_\(コンピュータ\).md "wikilink")・ソフトウェア。接続しようとする[パソコン上で必要である](../Page/パーソナルコンピュータ.md "wikilink")。
  - **オーセンティケータ**と呼ばれる802.1Xに対応した**[LANスイッチ](../Page/ハブ_\(ネットワーク機器\).md "wikilink")**
  - 認証サーバ - [認証](../Page/認証.md "wikilink")を判断するサーバ。**[RADIUS](../Page/RADIUS.md "wikilink")または[DIAMETER](https://ja.wikipedia.org/wiki/DIAMETER "wikilink")認証サーバ**でもよい。

本項目ではレベル2スイッチやインテリジェント・ハブ、LANスイッチと呼ばれているネットワーク機器を「LANスイッチ」と呼ぶ。また、802.1Xに対応したLANスイッチを「認証LANスイッチ」と、サプリカント・ソフトウェアを備えたクライアントPCを「サプリカントPC」と呼ぶ。 [thumb](https://ja.wikipedia.org/wiki/ファイル:IEEE_802.1Xの認証方法.PNG "wikilink") IEEE 802.1XはEthernetの認証であるのに対して、RADIUSはIP以上での認証であり、直接対応させて理解しない。

## 動作

[802.1X_wired_protocols.png](https://ja.wikipedia.org/wiki/File:802.1X_wired_protocols.png "fig:802.1X_wired_protocols.png") IEEE 802.1Xを使った認証動作は以下の3段階からなる。

  - 接続
  - [EAP（Extended authentication protocol）による認証](../Page/Extensible_Authentication_Protocol.md "wikilink")
  - 認証完了

### 接続

  - 有線LAN
    有線接続のLANでは、802.1Xに対応したLANスイッチに端末であるパソコンが接続された時点で認証動作を行い、その端末にLANへの接続を許可するかどうかを決める。
  - 無線LAN
    [無線LAN](../Page/無線LAN.md "wikilink")ではアソシエーション後に認証動作を行い、その端末にLANへの接続を許可するかどうかを決める。

### EAPによる認証

[EAPメッセージを認証](../Page/Extensible_Authentication_Protocol.md "wikilink")[LANスイッチ](../Page/LANスイッチ.md "wikilink")を経由して認証サーバと何度かやりとりを交わすことで、認証を受ける。サプリカントのMAC[フレームは認証LANスイッチによって](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")[RADIUS](../Page/RADIUS.md "wikilink")フレームに変換されて認証サーバへ送られ、逆に認証サーバから返信されるRADIUSフレームは認証LANスイッチによってMACフレームへ変換されてサプリカントへ送られる。認証LANスイッチはサプリカントPCからの通信は認証サーバへのもの以外は受け付けない。

### 認証完了

認証が完了して、初めてサプリカントはネットワークに自由に接続できるようになる。認証の種類によっては認証完了時に認証サーバから認証LANスイッチに暗号鍵の材料や所属LANの情報などが通知され、認証LANスイッチからサプリカントに[暗号鍵](https://ja.wikipedia.org/wiki/暗号鍵 "wikilink")が通知されることがある。

## EAP

802.1Xに使用できるEAPはいくつかあるが、サプリカントと認証サーバの両方が対応している必要がある。

  - EAP-MD5
    EAP-MD5（EAP-Message digest algorithm 5）はIDとパスワードで認証する方式。パスワードはチャレンジ＆レスポンス方式で暗号化されて送信される。無線LANでは安全ではない。
  - EAP-TLS
    EAP-TLS（EAP-Transport layer security）はデジタル電子証明書を使って認証する方式。IDやパスワードは使用されない。[スマートカードやUSBキー](../Page/ICカード.md "wikilink")（[ドングル](../Page/ドングル.md "wikilink")）と組み合わせて使用されることが多い。無線LANでもほぼ安全。
  - PEAP
    PEAP（Protected EAP）は米[マイクロソフト](../Page/マイクロソフト.md "wikilink")社が開発したEAP規格でIDとパスワードで認証する方式。[SSL](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")（Secure Sockets Layer）と同じ暗号化技術によって認証通信全体が暗号化されている。暗号化のために認証サーバにデジタル電子証明書が必要。無線LANでもほぼ安全。
  - LEAP
    LEAP（Lightweight EAP）は米[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")社が開発したEAP製品。
  - EAP-TTLS
    EAP-TTLS（EAP-Tunneled transport layer security）は米ファンク・ソフトウェア社（Funk Software）が開発したEAP製品。

## LANスイッチの接続環境

サプリカントPCと認証LANスイッチは直接接続されることが必要であるが、仮に両者の間に別のネットワーク機器が存在した場合の動作を以下に示す。

  - 通常のLANスイッチ
    サプリカントが送信するEAPメッセージを含んだMACフレームは、[マルチキャスト](../Page/マルチキャスト.md "wikilink")・アドレスで送信されているために、通常のLANスイッチでは[セグメント](../Page/セグメント.md "wikilink")外部にある認証LANスイッチへ転送しない。このため、認証動作が行われず、サプリカントPCであるクライアントPCはネットワークに接続されない。
  - リピータ・ハブ
    サプリカントが送信するEAPメッセージを含んだMACフレームは、[リピータ](https://ja.wikipedia.org/wiki/リピータ "wikilink")・[ハブによって認証LANスイッチへ転送される](../Page/ハブ_\(ネットワーク機器\).md "wikilink")。認証LANスイッチは送り手側にリピータ・ハブが介在していることが判らないため、認証要求を受付けて、認証接続の動作を開始する。サプリカントPCが認証を完了してネットワークに接続された場合に問題となるのは、リピータ・ハブに接続された他のPCは、認証を受けずにそのままネットワークに接続が可能となることである。認証LANスイッチの認証は[ポート単位で行われているため](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")、その1つの認証済みポートに接続されたリピーター・ハブの配下の全てのPCがネットワークへの接続を許されてしまう。ここまでがIEEE 802.1Xで規定された動作であるが、これではセキュリティが確保できないため、実際の認証LANスイッチ製品の多くでは、[MACアドレス](../Page/MACアドレス.md "wikilink")・フィルタ機能と連動させて、たとえリピーター・ハブを使われても認証されたPCをMACアドレスで認識して、他のPCをネットワークに接続することはない。

## ネットワーク・プリンタとIP電話

多くのネットワーク・プリンタと少し旧型の[IP電話](../Page/IP電話.md "wikilink")はIEEE 802.1Xに非対応のため、そのままではこれらの機器がネットワークに接続できなくなる。対症療法的にLANスイッチのMACアドレス・フィルタ機能を使ってこれらの機器をネットワークに参加させることができるが、LANスイッチのポートが固定となるため設定の手間がかかるだけでなく、MACアドレスを偽装した不正接続に対して大きな[セキュリティホール](../Page/セキュリティホール.md "wikilink")となり推奨できない。[ネットワーク・プリンタ](https://ja.wikipedia.org/wiki/ネットワーク・プリンタ "wikilink")等のセキュリティの確保できない端末機器だけのネットワークを[VLAN](https://ja.wikipedia.org/wiki/VLAN "wikilink")によって分割するなどの工夫が求められる。

## WindowsとMacでの対応

[Windows 2000](../Page/Microsoft_Windows_2000.md "wikilink") SP4以降、EAP-TLSとPEAPに対応しており、[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") 以降、EAP-MD5、EAP-TLS、PEAPにも対応している。

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")はサプリカント機能を標準で内蔵している。

## 出典

  - 「IEEE 802.1Xの全貌」日経NETWORK 2004年12月号 p.82〜p.95

## 関連項目

  - [RADIUS](../Page/RADIUS.md "wikilink") - 認証サーバ
  - [ハッシュ関数](../Page/ハッシュ関数.md "wikilink")
  - [暗号](../Page/暗号.md "wikilink")
  - [電子署名](../Page/電子署名.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [Wi-Fi Protected Access](../Page/Wi-Fi_Protected_Access.md "wikilink") (WPA)

[Category:認証プロトコル](https://ja.wikipedia.org/wiki/Category:認証プロトコル "wikilink") [Category:IEEE_802](https://ja.wikipedia.org/wiki/Category:IEEE_802 "wikilink")