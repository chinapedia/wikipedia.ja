> この記事は[IP](https://ja.wikipedia.org/wiki/IP)から翻訳されています。


[Avaya_9640_IP_Deskphone.jpg](https://ja.wikipedia.org/wiki/File:Avaya_9640_IP_Deskphone.jpg "fig:Avaya_9640_IP_Deskphone.jpg") IP電話 9640\]\] **IP電話**（アイピーでんわ）は、広い意味では[電話網](https://ja.wikipedia.org/wiki/電話網 "wikilink")の一部もしくは全てに[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")技術を利用する[電話](../Page/電話.md "wikilink")サービスである。[音](../Page/音.md "wikilink")声のみのものが多いが、[動画](../Page/動画.md "wikilink")も利用できる[テレビ電話](https://ja.wikipedia.org/wiki/テレビ電話 "wikilink")サービスなども可能である。

狭い意味では、VoIP技術を加入者回線に利用するもののうち[電気通信役務](https://ja.wikipedia.org/wiki/電気通信役務 "wikilink")として規制されるものをさす。多くの国では、[公衆交換電話網](https://ja.wikipedia.org/wiki/公衆交換電話網 "wikilink")と相互接続されるものが該当する。[電気通信事業者](https://ja.wikipedia.org/wiki/電気通信事業者 "wikilink")のIP加入者線を利用した[電話番号](https://ja.wikipedia.org/wiki/電話番号 "wikilink")の割り当てられるもの、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")をアクセス回線として利用した電話番号の割り当てられるもの、インターネットを利用した電話番号が割り当てられず発信のみのものに大別される。

また、一般的にはIP電話との認知は無いまたは薄いが、中継網にVoIPを活用している[中継電話](https://ja.wikipedia.org/wiki/中継電話 "wikilink")もある。IP電話とVoIPを区別せずに記述することもある。また、[IPセントレックス](https://ja.wikipedia.org/wiki/IPセントレックス "wikilink")など[内線電話](https://ja.wikipedia.org/wiki/内線電話 "wikilink")のVoIP化として利用も増えている。

この項では、狭い意味でのIP電話サービスに関して述べる。その他については[関連項目を参照](https://ja.wikipedia.org/wiki/#関連項目 "wikilink")。

なお正式名称は、「インターネットプロトコル ([Internet Protocol](../Page/Internet_Protocol.md "wikilink")) 電話」だが、本項では一般的な呼称である「IP電話」で記述する。

## 固定電話との比較

[固定電話](https://ja.wikipedia.org/wiki/固定電話 "wikilink")と比較して、以下のような特徴がある。

  - 家庭用のものではアクセス回線には[FTTH](https://ja.wikipedia.org/wiki/FTTH "wikilink")や[ADSL](../Page/ADSL.md "wikilink")などといった、いわゆる[ブロードバンド回線を利用する](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")。音声を[データ圧縮](../Page/データ圧縮.md "wikilink")・[符号化](https://ja.wikipedia.org/wiki/符号化 "wikilink")して[IP](../Page/Internet_Protocol.md "wikilink")[パケット](https://ja.wikipedia.org/wiki/パケット "wikilink")に分割し、比較的安価な[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")により[リアルタイム](../Page/リアルタイム.md "wikilink")伝送する（この技術は一般的に[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")と呼ばれる）。
  - [電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")（高価で有資格者による工事や煩雑な保守を必要とする）の代わりにIP電話サーバを使用する（以下は[SIPの場合](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")）。
      - IP電話加入者データを元に通信を制御する「加入者系呼制御サーバ」（SIPサーバ）、IP電話と他のIPネットワークとの通信を制御する「中継系呼処理サーバ」（CA（Call Agent）サーバ）、これらを連携させる「呼処理サーバ」（SIP連携サーバ）の他、従来の電話網側には「相互接続用関門交換機」が設置されている。
  - プレゼンス管理・ボイスメール・電話会議・テレビ電話サービスなどその他の付加価値をつけたものも存在する。
  - ネットワーク構成の自由度を生かして、電話の音声帯域を拡張し ( - 7kHz、G722) 高音質化を図ったものも一部にある。

注意点として以下の点があげられる。

  - 停電時に局給電による電話が使えない（停電を補償するには[UPSが必要](https://ja.wikipedia.org/wiki/無停電電源装置 "wikilink")）。
      - 対照的に、[ISDN](../Page/ISDN.md "wikilink")では[TA](https://ja.wikipedia.org/wiki/ターミナルアダプタ "wikilink") (Terminal Adapter) に[乾電池](https://ja.wikipedia.org/wiki/乾電池 "wikilink")を装備したり、局給電に対応したTAを使用することにより、停電時でも電話は使用可能。また、基本的にIP電話回線は特定の物理的回線には依存しない（ADSL/CATV/FTTH/FTTx/専用線と多様）ため、停電時の問題解決も一様ではない。
      - ただし、近年は広く普及した[携帯電話](../Page/携帯電話.md "wikilink")・[PHS](../Page/PHS.md "wikilink")により代替すれば良く、災害時の長期・大規模停電を除いては、重要な問題とは言えなくなっている。
  - 発展途上の技術であるので、標準化が完全でない部分がある。
  - 障害発生時の原因の特定・回復に時間がかかる場合がある。
  - [緊急通報や特殊通話が出来ない場合や](https://ja.wikipedia.org/wiki/緊急通報用電話番号 "wikilink")、通信できない電話番号がある。
  - 電話の付加サービスが無いか仕様が異なる場合がある。

、日本でもNTTが[PSTNのNGNへのマイグレーション（移行）を実施しつつあり](https://ja.wikipedia.org/wiki/公衆交換電話網#PSTNのマイグレーション "wikilink")、携帯電話で欠点を補完しつつ、2025年までにIP電話にすべて切り替わる見込みである。

## 法的位置付け

2007年現在、各国で法的位置付けが異なる。

1.  基本的に情報サービスの位置付け
      - [ペルー](https://ja.wikipedia.org/wiki/ペルー "wikilink")・[スイス](../Page/スイス.md "wikilink")
2.  [電気通信役務](https://ja.wikipedia.org/wiki/電気通信役務 "wikilink")として規制するかどうか議論中
      - [アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")・[アルジェリア](../Page/アルジェリア.md "wikilink")
3.  特定の機能を持つものを電気通信役務として規制、その他は情報サービスの位置付け
      - [欧州連合](https://ja.wikipedia.org/wiki/欧州連合 "wikilink")・[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")・[大韓民国](https://ja.wikipedia.org/wiki/大韓民国 "wikilink")
4.  基本的に電気通信役務として規制
      - [日本](https://ja.wikipedia.org/wiki/日本 "wikilink")・[インドネシア](../Page/インドネシア.md "wikilink")・[タイ王国](https://ja.wikipedia.org/wiki/タイ王国 "wikilink")・[エジプト](../Page/エジプト.md "wikilink")
5.  固定電話 - 固定電話間のサービスを禁止。その他を部分解禁
      - [ハンガリー](../Page/ハンガリー.md "wikilink")・[インド](../Page/インド.md "wikilink")・[ベトナム](https://ja.wikipedia.org/wiki/ベトナム "wikilink")・[モーリシャス](../Page/モーリシャス.md "wikilink")

また、[公衆交換電話網](https://ja.wikipedia.org/wiki/公衆交換電話網 "wikilink") (PSTN) と同様に[基礎的電気通信役務](https://ja.wikipedia.org/wiki/基礎的電気通信役務 "wikilink")として位置付けるかについても差異がある。

[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")で国際的に接続している限り、政府による規制は難しい面がある。しかし、一部の[発展途上国では](../Page/開発途上国.md "wikilink")、VoIPパケットを国際関門[ルーター](https://ja.wikipedia.org/wiki/ルーター "wikilink")でブロックしたり、[インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink")のアカウントの取得を制限していることもある。[Skype\#その他の国々](https://ja.wikipedia.org/wiki/Skype#その他の国々 "wikilink")も参照。

### アメリカ合衆国

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[5月19日](../Page/5月19日.md "wikilink")、[連邦通信委員会](https://ja.wikipedia.org/wiki/連邦通信委員会 "wikilink")が公衆交換電話網と相互接続を行うIP電話サービスの提供プロバイダに対して、緊急通報911をダイヤルした場合に地元の緊急対応機関に接続し、所在地情報を緊急オペレーターに提供するように義務付けた。[11月28日](../Page/11月28日.md "wikilink")以降は条件を満たさないIP電話の新規加入の受付を停止することとなった。非対応のサービスを継続して提供する場合は、利用者に緊急通報が不可能であることをわかりやすく説明して同意を得ることとなっている。

法執行機関による通信傍受、[障害者](../Page/障害者.md "wikilink")の利用を可能とする、消費者保護などの社会的規制、[アクセスチャージ](https://ja.wikipedia.org/wiki/アクセスチャージ "wikilink")・ユニバーサルサービス基金など経済的な分担については、2007年現在引き続き議論が行われている。

### カナダ

公衆交換電話網と相互接続されるものは、電気通信役務として規制される。

ユニバーサルサービス基金の分担もある。

### 欧州連合

欧州連合では、枠組み指令により次の3種類に分けられる。

  - 電子通信サービス: 通常は有償で提供されるサービスであって、もっぱらまたは主として電子通信ネットワーク上の信号を伝送すること。企業の[内線電話](https://ja.wikipedia.org/wiki/内線電話 "wikilink")など。
    公衆電子通信サービス: 一般消費者に直接提供される電気通信サービス。消費者保護などの一般的な規制が適用される。
    公衆に利用可能な電話サービス: [公衆交換電話網](https://ja.wikipedia.org/wiki/公衆交換電話網 "wikilink")と相互接続される音声通信サービス。[緊急通報](https://ja.wikipedia.org/wiki/緊急通報用電話番号 "wikilink")・国際[電話番号計画](https://ja.wikipedia.org/wiki/電話番号計画 "wikilink")への対応が求められる。

また、無料で提供される場合は他の電気通信サービスを妨害しないこと、消費者に不利益を与えないための最低限の条件のみを定めることとなっている。

### 南アフリカ

公衆交換電話網が整備されていない地域で、部分的な自由化を行う。

### 大韓民国

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")から固定電話の番号がそのままIP電話で使えるようになる。

### 日本

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")の[電気通信事業法](https://ja.wikipedia.org/wiki/電気通信事業法 "wikilink")の[電気通信役務](https://ja.wikipedia.org/wiki/電気通信役務 "wikilink")の届出区分では、インターネットを使用した電話番号の割り当てられないものも含め、電気通信役務として規制される。また、提供サービス・通話品質等を利用者に分かり易く広告などで契約前に提示し、苦情受付を誠実に行うこととなっている。

[電気通信役務\#日本の電気通信事業法における利用者保護](https://ja.wikipedia.org/wiki/電気通信役務#日本の電気通信事業法における利用者保護 "wikilink")を参照のこと。

ユニバーサルサービス基金の分担もある。

## 関連項目

  - [日本のIP電話](https://ja.wikipedia.org/wiki/日本のIP電話 "wikilink")
  - [Next Generation Network](https://ja.wikipedia.org/wiki/Next_Generation_Network "wikilink") - IP技術を利用するFMC ([Fixed Mobile Convergence](https://ja.wikipedia.org/wiki/Fixed_Mobile_Convergence "wikilink")) と呼ばれる固定・移動体通信を統合した[マルチメディア](../Page/マルチメディア.md "wikilink")[サービス](../Page/サービス.md "wikilink")を実現する、次世代電話網
  - [VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink") - 技術・機器の分類、網構成・中継網のみのサービス等。[中継電話](https://ja.wikipedia.org/wiki/中継電話 "wikilink")方式やアクセスポイント方式のIP電話などもこちら
      - [VoLTE](https://ja.wikipedia.org/wiki/VoLTE "wikilink") - [VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")の携帯電話版ともいわれる規格。[3.9G](https://ja.wikipedia.org/wiki/3.9G "wikilink")規格の一つである[Long Term Evolution方式自体は](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink")、[パケット通信](https://ja.wikipedia.org/wiki/パケット通信 "wikilink")回線であり、[音声通話](https://ja.wikipedia.org/wiki/音声通話 "wikilink")の回線ではないため、パケット通信網に音声通話のデータを流す形で通話する方式。ちなみに、VoLTEに対応していないLTE端末の音声通信は、[3G](https://ja.wikipedia.org/wiki/3G "wikilink")網を利用して行う。
  - [インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink") - [インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")を利用したサービス、[プロバイダフリーのIP電話も含む](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")
  - [IPセントレックス](https://ja.wikipedia.org/wiki/IPセントレックス "wikilink") - [内線電話](https://ja.wikipedia.org/wiki/内線電話 "wikilink")のVoIP化、モバイルセントレックス、企業内IPセントレックスなど
  - [パケット通信](https://ja.wikipedia.org/wiki/パケット通信 "wikilink")
  - [Session Initiation Protocol](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink")
  - [電話](../Page/電話.md "wikilink") - [電話網](https://ja.wikipedia.org/wiki/電話網 "wikilink")
  - [音声通話定額制](https://ja.wikipedia.org/wiki/音声通話定額制 "wikilink")
  - [テレビ電話](https://ja.wikipedia.org/wiki/テレビ電話 "wikilink")
  - [IPマルチメディアサブシステム](https://ja.wikipedia.org/wiki/IPマルチメディアサブシステム "wikilink")
  - [LINE (アプリケーション)](https://ja.wikipedia.org/wiki/LINE_\(アプリケーション\) "wikilink")
  - [インターフォン](https://ja.wikipedia.org/wiki/インターフォン "wikilink")

## 外部リンク

  - [IP電話普及推進センタ](http://www.iptpc.com/index.html)

[Category:IP電話](https://ja.wikipedia.org/wiki/Category:IP電話 "wikilink")