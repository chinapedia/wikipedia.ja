> この記事は[VoIP](https://ja.wikipedia.org/wiki/VoIP)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:1140E.jpg "wikilink")\]\] **Voice over Internet Protocol**（ボイス オーバー インターネット プロトコル）とは、[IPを利用して通話をする技術のことである](../Page/インターネット・プロトコル・スイート.md "wikilink")。**VoIP**（ブイ オー アイピー、ボイップ\[1\]、ボイプ\[2\]）とも呼ばれる。

## 概要および経緯

[Voip-typical.gif](https://ja.wikipedia.org/wiki/File:Voip-typical.gif "fig:Voip-typical.gif")\]\] VoIPにおいては、[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")を各種[符号化方式](../Page/符号化方式.md "wikilink")で[符号化](https://ja.wikipedia.org/wiki/符号化 "wikilink")および[圧縮し](../Page/データ圧縮.md "wikilink")、[パケット](../Page/パケット.md "wikilink")に変換したものを[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")で[リアルタイム](../Page/リアルタイム.md "wikilink")伝送する。VoIPは、 (VoFR) ・ (VoA) などと同じ**Voice over Packet Network (VoPN)** の一種である。

VoPNは、電話網と[データ通信](../Page/データ通信.md "wikilink")網の[伝送路](../Page/伝送路.md "wikilink")や交換設備を共用することを目的として導入が始まった。

VoFRは、[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")よりも遅延が少ない[フレームリレー](../Page/フレームリレー.md "wikilink")を使用するものである。IP加入者網が無かった時代に[内線電話](../Page/内線電話.md "wikilink")として普及したが、[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")の価格の低下と速度の向上、提供地域の拡大により撤去が進んだ。

VoAは、従来の[電話網](../Page/電話網.md "wikilink")で必要となる[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")を[パケット通信](../Page/パケット通信.md "wikilink")とリアルタイム通信とを[多重化](../Page/多重化.md "wikilink")するために開発された[ATM](../Page/Asynchronous_Transfer_Mode.md "wikilink")[交換機](../Page/交換機.md "wikilink")に置き換えるものである。高価で有資格者による保守を必要とするものであり、[電気通信事業者](../Page/電気通信事業者.md "wikilink")の[携帯電話](../Page/携帯電話.md "wikilink")・[固定電話](https://ja.wikipedia.org/wiki/固定電話 "wikilink")などの[公衆交換電話網](../Page/公衆交換電話網.md "wikilink")で使用されているものがほとんどである。

VoIPは、[1990年代](../Page/1990年代.md "wikilink")後半より、[インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink")と呼ばれる、[スピーカー](../Page/スピーカー.md "wikilink")・[マイクロフォン](../Page/マイクロフォン.md "wikilink")または、ヘッドセットを接続した[パソコンに](../Page/パーソナルコンピュータ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")をインストールする方式で利用されていたが、使い勝手が悪く、遅延・エコー・欠落などにより音質も従来の[電話](../Page/電話.md "wikilink")より劣るものであった。

[2000年代](../Page/2000年代.md "wikilink")より、[ADSL](../Page/ADSL.md "wikilink")・[FTTH](../Page/FTTH.md "wikilink")・[広域イーサネット](../Page/広域イーサネット.md "wikilink")といった常時接続・高速・定額制のIP加入者回線が普及し、[Resource Reservation Protocol](../Page/Resource_Reservation_Protocol.md "wikilink") (RSVP) などの[QoS機能で音質が改善された](../Page/Quality_of_Service.md "wikilink")。また、専用機器の開発に伴い一般の電話と同じ操作・機能となり、公衆網への発信が可能になり、[電話番号](../Page/電話番号.md "wikilink")の割り当てにより公衆網などからの着信が可能となった。

今日では、[LINEや](https://ja.wikipedia.org/wiki/LINE_\(アプリケーション\) "wikilink")[Skype](../Page/Skype.md "wikilink")といったVoIP機能を有するアプリをパソコンやスマートフォンで起動することにより、パケット通信を利用して通話することが可能である。ただし、データ通信に用いられる回線は比較的高い[レイテンシ](../Page/レイテンシ.md "wikilink")であるため、応答の遅延が通話に支障をきたす場合もある。

また、[無線LAN](../Page/無線LAN.md "wikilink")上でのVoIPに関する技術を特に**VoWLAN** (Voice over Wireless LAN) と言うこともある。

## 技術

[通信プロトコル](../Page/通信プロトコル.md "wikilink")は呼制御、（電話の呼び出し、切断）と[音](../Page/音.md "wikilink")[声](../Page/声.md "wikilink")の送受信の2つを組み合わせて使用する。

### 呼制御とIP電話網間相互接続

呼制御を行う通信プロトコルとして[Session Initiation Protocol](../Page/Session_Initiation_Protocol.md "wikilink")（SIP）が良く使われる。他にも[H.323](../Page/H.323.md "wikilink")と言う通信プロトコルもある。

開発コスト・検討期間等の問題があるため、IP電話網間は、発着信二者間のSIPサーバ連携となった\[3\]\[4\]。

### 接続方式

[公衆交換電話網](../Page/公衆交換電話網.md "wikilink")を廃止し、相互接続をIP接続に置き換える手法について検討が行われている\[5\]。

1.  イーサネット方式 : 同一イーサネット網に全社接続
2.  個別ルータ方式 : 相互接続の[組み合わせは](../Page/組合せ_\(数学\).md "wikilink")\({}_n{\rm C}_{m}\)となりコスト高となる。
3.  共用ルータ方式 :
4.  個別・共用並存方式

共通のPOIビル（Point Of Interface＝相互接続点、すなわち通信事業者の回線網どうしの接続箇所\[6\]が収容されている建物）で、共用L2スイッチを介した接続とパッチパネルを介した接続が併存する構成が有力となった。 共用L2スイッチの利用を要望する事業者のコンソーシアムが資産保有し、破棄し得ない使用権権（indefeasible right of user）でNTT東日本・NTT西日本に貸し出し、NTT東日本・NTT西日本が設置場所提供・保守・運用を行うことが同意された。

  - POIビルの数は必要最小限とし費用を抑える。
  - トラヒック交流の多い箇所に設置し効率化する。
  - 信頼性確保のため、大規模災害・大規模故障等を想定し、複数を地理的に離れた場所に設置する。

POIは、通信需要の多い東京と大阪に設置することが合理的であると、事業者間の協議において確認された。地域内折り返し用のPOIの設置場所の追加・張り出しPOIの設置ついての協議を行う必要性はある。

POIの設置個所ついては、次の条件で、コスト試算をすることとなった。

[SIPサーバは発着](../Page/Session_Initiation_Protocol.md "wikilink")2者間連携、接続方式は共用ルータ方式、ループ構成の中継伝送路は全国系事業者と地域系事業者の間の通話のみに利用、携帯事業者同士の通話は共用ルータも利用しない、自網からPOIまでの伝送路コストは算入。

1.  東西計2カ所に全事業者がメッシュ状に接続
2.  東西2カ所ずつをループ構成の伝送路で中継・全国系事業者は東西各1カ所に接続・地域系事業者は近傍の2カ所接続
3.  地域ブロックごとに2カ所で各POIをループ構成の伝送路で中継・全国系事業者は、東西各1カ所に接続・地域系事業者は自ブロック内の2カ所に接続

相互接続には、通話料が無料のものと、有料のものがある。

無料相互接続の場合は、ITSP間でVoIP規格や機器[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")などが同一のため、通話の[トラフィック](https://ja.wikipedia.org/wiki/トラフィック "wikilink")をそのままIPレベルで流して、VoIP端末同士で[P2Pの通話を行っている](../Page/Peer_to_Peer.md "wikilink")（もちろん[セッション](../Page/セッション.md "wikilink")管理サーバの仲介はあるが、通話トラフィック自体はP2P）。

有料相互接続の場合は、ITSP間でVoIP規格や機器ベンダーなどが異なるため、通話のトラフィックをVoIPゲートウェイなどを通して相互に変換している。通話中はゲートウェイの資源を消費するなどの理由により、通話料は有料となっている。

### 音声信号

[音](../Page/音.md "wikilink")[声](../Page/声.md "wikilink")信号の[圧縮](../Page/データ圧縮.md "wikilink")[符号化方式](../Page/符号化方式.md "wikilink")には、通常0.3 - 3.4kHz帯域のものが用いられるが、0.05 - 7kHz帯域のものも使用される。狭い帯域で多数チャネルが必要な場合に、音声が一定のレベル以下のときにパケットを送出しない無音圧縮の手法が使われ、頭切れや演算負荷の増加の原因になることもある。

リアルタイム性を重視し再送信を行わない[RTPを使用して音声パケットを送り](../Page/Real-time_Transport_Protocol.md "wikilink")、[パケット通信](../Page/パケット通信.md "wikilink")網の遅延時間のばらつきによるパケットの間隔や順序の乱れを吸収するため、受信側にバッファメモリが使用される。バッファメモリによる遅延時間は、回線の状況が良いときは小さく、悪いときは大きく調整される。途中で破棄されたパケットは、直前のパケットのデータから演算した音声や[ホワイトノイズ](../Page/ホワイトノイズ.md "wikilink")などの挿入で補正される。

バッファ補正の遅延時間の影響で、みなし音声方式の場合[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")などの[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")や[DTMF](../Page/DTMF.md "wikilink")を使用した通信がうまくいかない場合がある。そのため、デジタルデータのパケットとしてファクシミリを送るための専用プロトコルであるT.38対応のゲートウェイを使用することもある。→[InternetFAX](../Page/InternetFAX.md "wikilink")を参照。

## VoIP専用機器

VoIP専用機器には、呼制御を行う[通信プロトコル](../Page/通信プロトコル.md "wikilink")として、SIP ([Session Initiation Protocol](../Page/Session_Initiation_Protocol.md "wikilink")) のものと[H.323](../Page/H.323.md "wikilink")のもの、[IPv4](../Page/IPv4.md "wikilink")のものと[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")のものとがある。網として統一されていないと、多数の[ゲートウェイ](../Page/ゲートウェイ.md "wikilink")が必要となる。

[2016年](../Page/2016年.md "wikilink")現在ではほぼSIPに統一され、H.323を利用することはまれである。

### VoIP網制御装置

VoIP網制御装置とは、[IPアドレス](../Page/IPアドレス.md "wikilink")と[電話番号](../Page/電話番号.md "wikilink")の相互変換・通信帯域管理・[輻輳](../Page/輻輳.md "wikilink")処理・課金・プレゼンス管理などの付加機能などを行う機器。SIPではSIP[サーバ](../Page/サーバ.md "wikilink")、H.323の場合ゲートキーパーと呼ぶ。また、汎用サーバの[ソフトウェア](../Page/ソフトウェア.md "wikilink")として実装されているものを[ソフトスイッチ](https://ja.wikipedia.org/wiki/ソフトスイッチ "wikilink")とも呼ぶ。

電話交換機より安価に導入でき、保守や機能拡張が容易である。

### VoIPゲートウェイ

VoIPゲートウェイとは、IP電話網制御装置の制御により、公衆交換電話網や他のIP電話網などの異なる網間との情報の送受信やプロトコル変換を行う機器。

  - IP構内交換機
    IP[構内交換機](https://ja.wikipedia.org/wiki/構内交換機 "wikilink")（[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")）とは、一般電話網の交換機にIP網への接続機能を追加したもの。事業者用のものと、内線用のIP-PBXと呼ばれるものとがある。VoIP網制御装置と統合されたものもある。
  - IP電話アダプタ
    IP電話アダプタとは、[LANなどを通してVoIPでの通話を可能にするためプロトコルや](../Page/Local_Area_Network.md "wikilink")[インターフェースを変換する機器](../Page/インタフェース_\(情報技術\).md "wikilink")。次の様な機器の接続用がある。
      - アナログ[電話機](https://ja.wikipedia.org/wiki/電話機 "wikilink") ([ATA](../Page/Analog_Telephony_Adapter.md "wikilink")) : 回線数の少ないものが一般的である。家庭向け等の機種では、[ADSL](../Page/ADSL.md "wikilink")モデムや[ルーター](../Page/ルーター.md "wikilink")との[複合機も多い](../Page/オールインワン.md "wikilink")。
      - [PHS](../Page/PHS.md "wikilink") : 構内PHSの[バックボーン](https://ja.wikipedia.org/wiki/バックボーン "wikilink")をLANに統合するために使用する。
      - [ISDN](../Page/ISDN.md "wikilink")対応内線交換機 : ビジネスホンなどをISDNから切り替えるために使用する。S点接続のものが多いがU点のものもある。

### VoWLANコントローラー

[VoWLAN](https://ja.wikipedia.org/wiki/VoWLAN "wikilink")コントローラーとは、[無線LAN](../Page/無線LAN.md "wikilink")[アクセスポイント間で無線IP電話機を](../Page/アクセスポイント_\(無線LAN\).md "wikilink")[ハンドオーバー](../Page/ハンドオーバー.md "wikilink")できるように制御する機器。無線LANのセキュリティ向上機能を持つものも多い。端末とアクセス・ポイント間との認証・ハンドオーバーの時間を短縮する規格として[IEEE](../Page/IEEE.md "wikilink") 802.11iがある。また、[品質確保のための帯域制御](../Page/Quality_of_Service.md "wikilink")・同時通話数制限、待ち受け時間延長のための省電力制御の規格としてIEEE 802.11eがある。

### Wi-Fi電話端末

Wi-Fi電話端末とは、無線LANに直結できる携帯型電話機。[モバイルセントレックス用の端末として](https://ja.wikipedia.org/wiki/IPセントレックス#モバイルセントレックスサービス "wikilink")、期待されている。2007年現在、IEEE 802.11i・IEEE 802.11e対応の連続待ち受け時間などが改善されたものが登場し、また、[携帯電話](../Page/携帯電話.md "wikilink")などとのデュアル機や、通信端末分離型（[CFカード等](../Page/コンパクトフラッシュ.md "wikilink")）の端末も開発されている。

無線LAN内蔵携帯電話は、[2004年](../Page/2004年.md "wikilink")から[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")によって、企業向けに「[PASSAGE DUPLE](https://ja.wikipedia.org/wiki/PASSAGE_DUPLE "wikilink")」というモバイルセントレックスサービスとして展開されている。「[ホームU](https://ja.wikipedia.org/wiki/ホームU "wikilink")」という個人向けサービスも[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")7月より開始されている。

### IP電話機

[IP電話機](https://ja.wikipedia.org/wiki/IP電話機 "wikilink")とは、[イーサネット](../Page/イーサネット.md "wikilink")に直結できる据え置き型電話機。[Power over Ethernet機能のある](../Page/Power_over_Ethernet.md "wikilink")[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")からの給電で動作し、個別の電源アダプタが不要なものも存在する。また、スイッチングハブ機能を持ち[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")との連携機能を持つものもある。

### ソフトフォン

[ソフトフォン](https://ja.wikipedia.org/wiki/ソフトフォン "wikilink")とは、パソコンの[ソフトウェア](../Page/ソフトウェア.md "wikilink")として実現されたIP電話のことである。比較的安価で他ソフトとの連携機能・音声録音などの多くの機能を持ち、[コールセンター](../Page/コールセンター.md "wikilink")などで使用されている。無線IP電話機の携行忘れ時の代替用の導入もある。

また、[USB接続のヘッドセット型で](../Page/ユニバーサル・シリアル・バス.md "wikilink")、内蔵メモリーにソフトウエアが書き込まれており、接続するだけでインストールされるものも販売されている。

### スマートフォン

iPhoneやAndroidなどのスマートフォンに[Skype](../Page/Skype.md "wikilink")や[Viber](https://ja.wikipedia.org/wiki/Viber "wikilink")などのアプリケーションをインストールして、インターネット電話としての利用が可能。

## 端末機器接続方法

[固定電話](https://ja.wikipedia.org/wiki/固定電話 "wikilink")と、セカンダリIP電話とを1台の一般電話機で共用する場合

`一般電話機 - | IP電話 | - 公衆交換電話網`
`             |アダプタ| - IP中継網`

プライマリIP電話と、セカンダリIP電話とを1台の一般電話機で共用する場合

`一般電話機 - |セカンダリ| - 電話ケーブル - |プライマリ| - IP中継網`
`             | アダプタ | - LAN ケーブル - | アダプタ |`

固定電話と、セカンダリIP電話とを2台の一般電話機で別々に使用

`一般電話機 (1)  - 公衆交換電話網`
`一般電話機 (2)  - |IP電話アダプタ| - IP中継網`

プライマリIP電話と、セカンダリIP電話とを2台の一般電話機で別々に使用

`一般電話機 (1)  ----- 電話ケーブル ----- |プライマリ| - IP中継網`
`一般電話機 (2)  - |セカンダリ| -- LAN -- | アダプタ |`
`                  | アダプタ |  ケーブル`

2台対応のプライマリIP電話アダプタで一般電話機を使用

`一般電話機 (1)  - | IP電話 | - IP中継網`
`一般電話機 (2)  - |アダプタ| `

固定電話と、セカンダリIP電話とをn台の一般電話機で共用する場合

`一般電話機 (1)  - |内線電話| - 公衆交換電話網`
`一般電話機 (n)  - | 交換機 | - |IP電話アダプタ| - IP中継網`

プライマリIP電話と、セカンダリIP電話とをn台の一般電話機で共用する場合

`一般電話機 (1)  - |内線電話| ----- 電話ケーブル ----- |プライマリ| - IP中継網`
`一般電話機 (n)  - | 交換機 | - |セカンダリ| -- LAN -- | アダプタ |`
`                               | アダプタ |  ケーブル`

[ISDN](../Page/ISDN.md "wikilink")対応BRIのS点・U点またはPRI接続のIP電話アダプタで一般電話機を使用

`一般電話機 (1)  - |内線電話| - | IP電話 | - IP中継網`
`一般電話機 (n)  - | 交換機 |   |アダプタ|`

ISDN対応BRIのS点・U点またはPRI接続のIP電話アダプタで固定電話を併用して一般電話機を使用

`一般電話機 (1)  - |内線電話| - 公衆交換電話網`
`一般電話機 (n)  - | 交換機 | - |IP電話アダプタ| - IP中継網`

## 網構成方式

中継網のみIP網とするもの。

  - 一般電話機 - 一般[加入者線](https://ja.wikipedia.org/wiki/加入者線 "wikilink") - IP電話交換機 - IP中継網 - 着信先

IP化された加入者線に、IP電話アダプタを介して一般電話機を接続するもの。

  - 一般電話機 - IP電話アダプタ - IP加入者線 - IP中継網 - 着信先

IP電話機をIP化された加入者線に直結するもの。

  - IP電話機 - IP加入者線 - IP中継網 - 着信先

無線IP電話機を無線LAN[アクセスポイントを介してIP化された加入者線に直結するもの](../Page/アクセスポイント_\(無線LAN\).md "wikilink")。[データ通信](../Page/データ通信.md "wikilink")用との併用の場合には、特に通話品質の確保に配慮した基地局やスイッチ網の構成が求められる。2007年現在、[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")を[電気通信事業者](../Page/電気通信事業者.md "wikilink")が設置する移動通信サービスの提供も計画されている。

  - 無線IP電話機 - 無線LAN基地局 - IP加入者線 - IP中継網 - 着信先

## VoIPを活用した電話網

一般的にはIP電話との認知は無いまたは薄いが、中継網にVoIPを活用している電話サービスも以下に述べる。

[2001年](../Page/2001年.md "wikilink")4月から、[フュージョン・コミュニケーションズが日本初の本格的な専用IP網](../Page/楽天コミュニケーションズ.md "wikilink")[中継電話](../Page/中継電話.md "wikilink")を[事業者識別コード番号](../Page/電話番号.md "wikilink")0038の[マイライン](../Page/マイライン.md "wikilink")（優先接続方式）で営業開始した。

[2005年](../Page/2005年.md "wikilink")2月には、[KDDI](../Page/KDDI.md "wikilink")が、内部の中継網（収容局以降）を専用IP網で構成して、メタルプラスサービスを開始した。[直収電話](https://ja.wikipedia.org/wiki/直収電話 "wikilink")の形態を取っている。

PHS事業者の[ウィルコム](../Page/ウィルコム.md "wikilink")では、2005年頃より、トラフィックの多い地域にVoIP対応交換機 (ITX : Ip Transit eXchange) を導入し、VoIP網を構築してきたが、2012年3月には全基地局のITXへの収容を完了した。これにより、[音声通話](https://ja.wikipedia.org/wiki/音声通話 "wikilink")および[データ通信](../Page/データ通信.md "wikilink")のトラフィックについて、内部の中継網（収容局以降）を専用IP網で構成して、従来の電話網から専用IP網（VoIP含む）に流す事で、[NTT東西への接続料が不要となった](../Page/日本電信電話.md "wikilink")。またウィルコム同士の[音声通話定額制](../Page/音声通話定額制.md "wikilink")の導入を可能にできたのも、このITX化による恩恵である。

  - アクセスポイント方式
    通常の[電話](../Page/電話.md "wikilink")から[アクセスポイント](https://ja.wikipedia.org/wiki/アクセスポイント "wikilink")に電話を掛けて、VoIPの中継網を通して他の電話網に着信する、特殊なサービスもある（スーパーテレフォン、JENS ipPhone等）。

## 脚注

## 関連項目

  - [インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink")
  - [Skype](../Page/Skype.md "wikilink")
  - [LINE](https://ja.wikipedia.org/wiki/LINE_\(アプリケーション\) "wikilink")
  - [IP電話](../Page/IP電話.md "wikilink") : 専用の[IP加入者網を利用したもの](../Page/Internet_Protocol.md "wikilink")。IP電話サービスの概要・法的位置付け・[電気通信事業者](../Page/電気通信事業者.md "wikilink")など。
  - [日本のIP電話](https://ja.wikipedia.org/wiki/日本のIP電話 "wikilink")
  - [VoLTE](https://ja.wikipedia.org/wiki/VoLTE "wikilink") ： [第3.9世代移動通信システム](https://ja.wikipedia.org/wiki/第3.9世代移動通信システム "wikilink")のひとつである[Long Term Evolutionにおける音声通話を](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink")、同方式のパケット通信ネットワーク上で実現する技術方式。なお、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")が[2013年](../Page/2013年.md "wikilink")夏モデル時点で発売している、[Xi](https://ja.wikipedia.org/wiki/Xi_\(携帯電話\) "wikilink") (LTE) と[FOMA](../Page/FOMA.md "wikilink") ([W-CDMA](../Page/W-CDMA.md "wikilink")) のデュアルモード[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")端末における音声ネットワークは、[FOMA](../Page/FOMA.md "wikilink")のネットワークで行われており、LTEネットワークによる音声通話は実現されていない。なお、[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")が3G網で手掛けているものは、[HD Voiceとして](https://ja.wikipedia.org/wiki/HD_Voice "wikilink")、VoLTEとは区別されている。
  - [インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink") : [インターネット](../Page/インターネット.md "wikilink")を利用したもの。
  - [IPセントレックス](../Page/IPセントレックス.md "wikilink") : [内線電話](../Page/内線電話.md "wikilink")のVoIP化、モバイルセントレックス・企業内IPセントレックス。
  - [Fixed Mobile Convergence](https://ja.wikipedia.org/wiki/Fixed_Mobile_Convergence "wikilink")
  - [VoWLAN](https://ja.wikipedia.org/wiki/VoWLAN "wikilink") - [Wi-Fi電話端末](https://ja.wikipedia.org/wiki/Wi-Fi電話端末 "wikilink")
  - [InternetFAX](../Page/InternetFAX.md "wikilink") : [IP電話](../Page/IP電話.md "wikilink")や[Internet ProtocolでのFAX通信](../Page/Internet_Protocol.md "wikilink")
  - [プッシュ・ツー・トーク](../Page/プッシュ・ツー・トーク.md "wikilink") : [第3世代移動通信システム](../Page/第3世代移動通信システム.md "wikilink")のVoIPを利用した半二重音声通信サービスなど。
  - [D-STAR](../Page/D-STAR.md "wikilink") : [パケット通信のVoIP](../Page/パケット通信_\(アマチュア無線\).md "wikilink")。
  - [Session Initiation Protocol](../Page/Session_Initiation_Protocol.md "wikilink")
  - [H.323](../Page/H.323.md "wikilink")
  - [MGCP](https://ja.wikipedia.org/wiki/MGCP "wikilink")、[Megaco](https://ja.wikipedia.org/wiki/Megaco "wikilink")、[Media Gateway Control Protocol](https://ja.wikipedia.org/wiki/Media_Gateway_Control_Protocol "wikilink")
  - [パケット通信](../Page/パケット通信.md "wikilink") - [フレームリレー](../Page/フレームリレー.md "wikilink") - [Asynchronous Transfer Mode](../Page/Asynchronous_Transfer_Mode.md "wikilink")
  - [電話網](../Page/電話網.md "wikilink") - [公衆交換電話網](../Page/公衆交換電話網.md "wikilink")
  - [IPマルチメディアサブシステム](https://ja.wikipedia.org/wiki/IPマルチメディアサブシステム "wikilink")

## 外部リンク

  - [Information about VoIP Protocols](http://www.en.voipforo.com)
  - [Topics : VoIP - Computerworld.jp](http://www.computerworld.jp/topics/voip/)

[Category:VoIPのソフトウェア](https://ja.wikipedia.org/wiki/Category:VoIPのソフトウェア "wikilink") [Category:インターネット技術](https://ja.wikipedia.org/wiki/Category:インターネット技術 "wikilink")

1.
2.
3.
4.
5.
6.