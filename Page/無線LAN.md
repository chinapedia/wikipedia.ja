> この記事は[LAN](https://ja.wikipedia.org/wiki/LAN)から翻訳されています。


[Wireless_network.jpg](https://ja.wikipedia.org/wiki/File:Wireless_network.jpg "fig:Wireless_network.jpg") **無線LAN**（むせんラン）とは、[無線通信](../Page/無線通信.md "wikilink")を利用して[データ](../Page/データ.md "wikilink")の送受信を行う[LANシステムのことである](../Page/Local_Area_Network.md "wikilink")。**ワイヤレスLAN**（, \[1\]）、もしくはそれを略して****とも呼ばれる。無線LANの通信方式には様々なものがあるが、著名な無線LANの規格として[IEEE 802.11があり](../Page/IEEE_802.11.md "wikilink")、**[Wi-Fi](../Page/Wi-Fi.md "wikilink")**（ワイファイ）は、その規格を使用する無線LANに関する登録商標である。

## 歴史

無線LANが普及する以前は、[IrDA](../Page/IrDA.md "wikilink")規格に準拠した[赤外線通信](https://ja.wikipedia.org/wiki/赤外線通信 "wikilink")がワイヤレス通信の主な手段であり、[ノートパソコン](../Page/ノートパソコン.md "wikilink")や[携帯電話](../Page/携帯電話.md "wikilink")、ICカード式[公衆電話](../Page/公衆電話.md "wikilink")に搭載されていた。その後、IEEE 802.11が標準化され、1998年頃から、メーカーごとに策定中の規格を元に無線LAN機器として製品化されていた。しかし2Mbps程度と低速であり価格が高く、メーカーが異なると相互に接続できない等の問題があり、広く普及することはなかった。

IEEE 802.11bでは通信速度が11Mbpsに改善される予定であったが、当時はIEEE 802.11機器の価格が高いこともあり、Intelが推進していたHomeRF規格が家庭向け無線LANの本命と見られていた\[2\]。しかしIEEE 802.11b正式標準化直前の1999年7月に[アップルコンピュータ](../Page/アップル_\(企業\).md "wikilink")（現：アップル）が[AirPort](../Page/AirMac.md "wikilink")（日本国内での名称はAirMac）を発表。これはアクセスポイントが299ドル、カードが99ドルという低価格で市場にインパクトを与え\[3\]\[4\]、これに日本では[メルコ](../Page/メルコホールディングス.md "wikilink")（現：[バッファロー](../Page/バッファロー_\(パソコン周辺機器\).md "wikilink")）を始め\[5\]各社も追従しIEEE 802.11b規格の機器が一般にも広く普及することとなった。

2009年9月、[IEEE](../Page/IEEE.md "wikilink")（米国電気電子学会）がIEEE 802.11n（11n）を正式に策定した。

## ローミング

無線LANのアクセスポイントが複数設置されている場合に、接続中のアクセスポイントから離れ、別のアクセスポイント付近に移動しても引き続き通信できる機能を「**ローミング**」と言う。 ローミング機能を使用するには、当該アクセスポイントがローミング機能に対応している必要がある。

## 各種方式

### IEEE 802.11シリーズ

### IEEE 802.15シリーズ

  - [Bluetooth](../Page/Bluetooth.md "wikilink")（IEEE 802.15.1） - モバイル機器向け
  - [Ultra Wideband](../Page/超広帯域無線.md "wikilink")（UWB, IEEE 802.15.3a）
  - [ZigBee](../Page/ZigBee.md "wikilink")（IEEE 802.15.4）

なお、[IEEE 802.15シリーズを](../Page/IEEE_802.15.md "wikilink")[無線PAN](https://ja.wikipedia.org/wiki/無線PAN "wikilink")（**WPAN**：Wireless [Personal Area Network](https://ja.wikipedia.org/wiki/Personal_Area_Network "wikilink")）と分類する事もある。

## セキュリティ

無線LANは、電波によって通信が行われるため、第三者によって通信内容を傍受される危険性がある。そのため、無線LANのアクセスポイントと通信を行う機器間とのセキュリティ対策が必要となる。たとえば、ネットワークキーと呼ばれるパスワードを用いて通信できるコンピューターをそのネットワークキーを知るコンピューターのみに限定させる方法がある。

暗号化通信におけるセキュリティ技術としては主にWEPやWPAやWPA2、IEEE 802.11iがある。これらの暗号化通信ではネットワークキーによって通信機器を限定する目的のほか、通信内容を暗号化することで第三者による通信内容の傍受を防ぐ目的もある。

近年は暗号化の解読技術が進み、WEPでは10秒で解読できるという論文がある\[6\]。また、[MACアドレス](../Page/MACアドレス.md "wikilink")によって通信できるコンピューターを限定する手法も、MACアドレスの偽装が技術上可能であることから、強固なセキュリティ対策とは言えない。

[情報処理推進機構](../Page/情報処理推進機構.md "wikilink")によると家庭用であれば認証方式として**WPA2-PSK**、暗号化方式として**AES**（**[CCMP](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink")**）を選択し十分な強度の共有鍵（大文字・小文字・数字・記号を全て含み20文字以上）を使用するべきであるという\[7\]。

なお日本では、[クラッキングなどの手法により](../Page/クラッキング_\(コンピューター用語\).md "wikilink")、パスワードで保護されたネットワークに不正に侵入した場合、もしくは試みた場合は、[不正アクセス行為の禁止等に関する法律](../Page/不正アクセス行為の禁止等に関する法律.md "wikilink")に抵触する可能性がある。

もっとも、パスワード設定されていない無線LANを利用するだけの行為（タダ乗り）については刑事上の問題は生じない。弁護士の[小倉秀夫](../Page/小倉秀夫.md "wikilink")によれば、係るタダ乗りは、不正アクセス行為に該当しないし、窃盗罪に問われることもないが、本来の利用者の使用を妨げるほどの帯域を使うような場合には、民事上の追及を受ける可能性がある\[8\]としている。

## 無線LANの各種機能

  - インフラストラクチャー・モード、アドホック・モード

### セキュリティ

  - [SSID](../Page/サービスセット識別子.md "wikilink")（Service Set ID）・ESSID（Extended SSID）
    無線LAN接続のグループ分けを行うID。認証にも使用される。最大32文字までの英数字が設定できる。通常はアクセスポイントとクライアントの設定を合致させないと接続できない。合致させなくとも接続できるような設定も可能だが、[フリースポット](https://ja.wikipedia.org/wiki/フリースポット "wikilink")等の公衆無料接続サービスを提供する場合以外ではセキュリティ面から推奨されない。

#### 通信プロトコルと暗号化方法

  - WEP（[Wired Equivalent Privacy](../Page/Wired_Equivalent_Privacy.md "wikilink")）
    無線LAN初期の規格。**セキュリティの脆弱性が指摘されており、WEP方式の利用は推奨されない\[9\]。**WEPのパスワードは10秒程度で解読可能であり\[10\]、[AirSnort](https://ja.wikipedia.org/wiki/AirSnort "wikilink")などのクラッキングソフトが出回っているため、容易に乗っ取りが可能である。
  - WPA（[Wi-Fi Protected Access](../Page/Wi-Fi_Protected_Access.md "wikilink")）
    WEPの脆弱性を改良するためIEEE 802.11iの策定に先立ち、[Wi-Fi Allianceによって制定された](../Page/Wi-Fi_Alliance.md "wikilink")。暗号化にはTKIP（[Temporal Key Integrity Protocol](https://ja.wikipedia.org/wiki/Temporal_Key_Integrity_Protocol "wikilink")）というストリーム暗号が用いられているが、これはWEPでの[RC4](../Page/RC4.md "wikilink")方式に、鍵と初期ベクトルをミックスする関数を加えるなどして既知の攻撃を可能な限り避けようとしたものである。しかし実際にはWEPの場合と同様の攻撃の多くが効いてしまう（詳細は[英語版のTKIPの記事を参照](https://ja.wikipedia.org/wiki/:en:Temporal_Key_Integrity_Protocol "wikilink")）。
  - WPA2（Wi-Fi Protected Access 2）
    WPAのセキュリティ強化改良版。IEEE 802.11iの策定に伴い、それを取り込む形で制定された。暗号方式としては[認証暗号の](https://ja.wikipedia.org/wiki/認証付き暗号 "wikilink")[AES](../Page/Advanced_Encryption_Standard.md "wikilink")-[CCMで](https://ja.wikipedia.org/wiki/Counter_with_CBC-MAC "wikilink")[MPDUやそのヘッダを守る](https://ja.wikipedia.org/wiki/:en:Protocol_data_unit "wikilink")[CCMPという方式が採用されている](https://ja.wikipedia.org/wiki/Counter_mode_with_Cipher-block_chaining_Message_authentication_code_Protocol "wikilink")。
  - WPA3（Wi-Fi Protected Access 3）
    WPA2に関する深刻な脆弱性、[KRACK](https://ja.wikipedia.org/wiki/KRACK "wikilink") (Key Re-installation Attack) が2017年10月に報告されたことを受け、2018年6月に策定されたセキュリティ規格。2019年4月にはWPA3にも脆弱性が報告されており\[11\]、いたちごっこの状態が続いている。

#### PSKモードとEAPモード

WPA/WPA2/WPA3にはPSKモードとEAPモードという２つのモードがある。

**PSKモード**(Pre-Shared Key、事前鍵共有)は**パーソナルモード**とも呼ばれ、アクセスポイント側に事前にパスワードを設定しておき、端末側でそのパスワードを打つ事で接続を開始する。通信に使う鍵はパスワードから[PBKDF2というアルゴリズム](https://ja.wikipedia.org/wiki/:en:PBKDF2 "wikilink")（[鍵導出関数](https://ja.wikipedia.org/wiki/鍵導出関数 "wikilink")）を用いて計算する。

一方**EAPモード**は**エンタープライズモード**とも呼ばれ、[RADIUS](../Page/RADIUS.md "wikilink")認証サーバを使って[EAP](../Page/Extensible_Authentication_Protocol.md "wikilink")(Extensible Authentication Protocol)の認証により[PPP接続する](../Page/Point-to-Point_Protocol.md "wikilink")。その詳細はIEEE 802.1xに規格化されている。

### 設定

無線LANでは有線LANに比べ設定が複雑なため、以下のような規格、システムがある。機種によっては手動で設定しなければならない場合もある。

  - WPS（[Wi-Fi Setup](https://ja.wikipedia.org/wiki/Wi-Fi_Protected_Setup "wikilink")）
    WPAを初心者にも簡単に設定できるようにする規格。[Wi-Fiアライアンス](https://ja.wikipedia.org/wiki/Wi-Fiアライアンス "wikilink")によって策定され、メーカーを問わず利用できる。なお規格にはセキュリテイ上問題があり、[PIN認証を用いた場合にはPINが](../Page/暗証番号.md "wikilink")[ブルートフォース攻撃できてしまう](../Page/力まかせ探索.md "wikilink")\[12\]\[13\]\[14\]ため、何度か認証に失敗すると認証をロックするよう設定された機種を使うか、ユーザの側でPIN設定後にWPSを無効化するなどして防御する必要がある\[15\]。
  - [AirStation One-Touch Secure System](../Page/AirStation_One-Touch_Secure_System.md "wikilink")（AOSS）
    [バッファローが発売している](../Page/バッファロー_\(パソコン周辺機器\).md "wikilink")[AirStation](../Page/AirStation.md "wikilink")に導入されている設定システム。
  - [らくらく無線スタート](../Page/らくらく無線スタート.md "wikilink")
    [NECアクセステクニカ](https://ja.wikipedia.org/wiki/NECアクセステクニカ "wikilink")株式会社（現・[NECプラットフォームズ](../Page/NECプラットフォームズ.md "wikilink")）が開発した設定システム。

### 独自拡張

メーカーによっては、IEEE 802.11a/b/gとの接続性を確保したまま独自の改良を加えた技術が存在する。高速化技術（圧縮・プロトコル最適化等）としては「SuperAG」「SuperG」「フレームバースト」「フレームバーストEX」などが、到達エリア拡大技術としては「XR（eXtended Range）」がある（SuperAG、SuperG、XRは[米](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[クアルコム・アセロス](https://ja.wikipedia.org/wiki/クアルコム・アセロス "wikilink")の[商標](../Page/商標.md "wikilink")）。メーカーの独自拡張であるため、親機子機が同じメーカー製であり両方が対応していないと効果はない。これらは最大通信速度は54Mbpsである802.11a、11gが主流の頃に登場したが、通信速度が大幅に向上した802.11nが広まってからはあまり見られなくなった。

## メッシュ型無線LAN

[Wi-Fi_mesh_system_Deco_M9_Plus.jpg](https://ja.wikipedia.org/wiki/File:Wi-Fi_mesh_system_Deco_M9_Plus.jpg "fig:Wi-Fi_mesh_system_Deco_M9_Plus.jpg") メッシュ型無線LANは**[メッシュWi-Fi](https://ja.wikipedia.org/wiki/メッシュWi-Fi "wikilink")**とも呼ばれる\[16\] \[17\]。[メッシュネットワーク](https://ja.wikipedia.org/wiki/メッシュネットワーク "wikilink")を無線LANに応用したもので、複数の[サテライトが相互に接続され](../Page/アクセスポイント_\(無線LAN\).md "wikilink")[ネットワークを構成する](../Page/コンピュータネットワーク.md "wikilink")。

## 公衆無線LAN

アクセスポイントへの接続を公衆に提供しインターネットへの接続手段を提供するサービスを、**[公衆無線LAN](../Page/公衆無線LAN.md "wikilink")**と言う。公衆無線LANにはホットスポットや[FREESPOT](../Page/FREESPOT.md "wikilink")などがある。詳細はこれらの項目を参照。

## 企業などでの利用

無線LANの一般化に伴い、無線LANアクセスポイントの高機能化が進み、様々な場面で利用されることが増えた。しかし無線の特性上、企業向けなどの大規模構成時には機器を多数設置する必要があることから、家庭向けの高機能な単体機器では管理・メンテナンス性や耐障害性等の問題が生じることもある。そのため無線[LANスイッチ](../Page/スイッチングハブ.md "wikilink")（無線LANコントローラ）を使用して集中管理を行い、無線LANアクセスポイントは極力単純な設計のもの（シンアクセスポイント）が選択されることもある。

## 各国の法規制

### 日本

#### 電波法

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")においては、1992年（平成4年）に[電波法](../Page/電波法.md "wikilink")令上のいわゆる[小電力無線局](../Page/小電力無線局.md "wikilink")の[小電力データ通信システム](https://ja.wikipedia.org/wiki/小電力データ通信システム "wikilink")の[無線局](https://ja.wikipedia.org/wiki/無線局 "wikilink")とされ、技術基準が定められた。これにより[免許は不要であるが](../Page/無線局免許状.md "wikilink")[技術基準適合証明](https://ja.wikipedia.org/wiki/技術基準適合証明 "wikilink")を要することとされた。 なお、電気通信回線に接続するものは[電気通信事業法](../Page/電気通信事業法.md "wikilink")令の[技術基準適合認定](https://ja.wikipedia.org/wiki/技術基準適合認定 "wikilink")も要する。

表示を要する事項と無線LANに関する内容は、次のとおりである。 　

<table>
<thead>
<tr class="header">
<th><p>種類</p></th>
<th><p>記号、種別</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/技適マーク.md" title="wikilink">技適マーク</a></p></td>
<td><p><strong>C</strong>の内部に稲妻と<strong><a href="https://ja.wikipedia.org/wiki/〒" title="wikilink">〒</a></strong>を配する。</p></td>
<td><p>技術基準適用時より表示開始<br />
1995年（平成7年）4月にマーク改正<br />
原則として直径5mm以上</p></td>
</tr>
<tr class="even">
<td><p>技術基準適合証明</p></td>
<td><p>2400〜2483.5MHz</p></td>
<td><p>WW</p></td>
</tr>
<tr class="odd">
<td><p>2471〜2497MHz</p></td>
<td><p>GZ</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>5.2、5.3GHz帯</p></td>
<td><p>XW</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.6GHz帯</p></td>
<td><p>YW</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>注：マーク、番号の構成が従前のものであっても証明は有効である。</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

**技適マークがなければ日本国内で使用してはならない**。また、技術基準には[アンテナ](../Page/アンテナ.md "wikilink")系を除き「容易に開けることができないこと」とあり、特殊[ねじ](../Page/ねじ.md "wikilink")などが用いられているので、使用者は改造はもちろん保守・修理のためであっても分解してはならない。 国内向けであっても改造されたものは、技術基準適合証明が無効になるので[不法無線局](https://ja.wikipedia.org/wiki/不法無線局 "wikilink")となる。

[ISMバンド](../Page/ISMバンド.md "wikilink")を用いる[高周波利用設備](https://ja.wikipedia.org/wiki/高周波利用設備 "wikilink")からは、有害な[混信](../Page/混信.md "wikilink")を容認しなければならない\[18\]。最も普及している2.4GHz帯の機器の場合、稼働中の[電子レンジ](../Page/電子レンジ.md "wikilink")の付近では、通信に著しい影響や出たり通信不能に陥る。また、[VICS](https://ja.wikipedia.org/wiki/VICS "wikilink")（[ETC](../Page/ETC.md "wikilink")）、一般用[RFID](../Page/RFID.md "wikilink")、[アマチュア無線局](https://ja.wikipedia.org/wiki/アマチュア無線局 "wikilink")機器など、[無線局免許状](../Page/無線局免許状.md "wikilink")・無線局登録を受けて運用する[無線局](https://ja.wikipedia.org/wiki/無線局 "wikilink")からの有害な混信に対して、**異議・排除を申し立てる権利は一切無く、逆に使用中止を要求されたら、利用者は従わねばならない**。

更に、無線LANと同等の小電力無線局として小電力用RFID、[2.4GHz帯デジタルコードレス電話](https://ja.wikipedia.org/wiki/コードレス電話#2.4GHz帯デジタルコードレス電話 "wikilink")、模型飛行機の[ラジコン](https://ja.wikipedia.org/wiki/ラジコン "wikilink")、[マルチコプター](https://ja.wikipedia.org/wiki/マルチコプター "wikilink")、[Bluetooth](../Page/Bluetooth.md "wikilink")などがあり、これらに対しては先に使用しているものが優先するが、実際には混信を完全に回避できるものではない。別ネットワークの複数機器が[アクセスポイント等でチャネルが重なると](../Page/アクセスポイント_\(無線LAN\).md "wikilink")、[スループット](../Page/スループット.md "wikilink")低下などの影響を受ける。

2010年（平成22年）には、電波法の規定を超えた高出力の無線LAN機器を販売していたとして、[大阪市](../Page/大阪市.md "wikilink")・[日本橋の](../Page/日本橋_\(大阪市\).md "wikilink")[電器店](../Page/電器店.md "wikilink")が摘発され、経営者が逮捕されている\[19\]。

#### アマチュア無線における無線LAN

2009年（平成21年）5月、[アマチュア無線局](https://ja.wikipedia.org/wiki/アマチュア無線局 "wikilink")JF1DQIが5.6GHz帯、10.1GHz帯、24GHz帯においてIEEE 802.11b/g方式の無線LANをアマチュア業務として運用できる[無線局免許状](../Page/無線局免許状.md "wikilink")を与えられた。設備は一般的に市販されているUSB無線LANアダプタで外部アンテナ端子がある機種（2000円以下）を用い、そのアンテナ端子に[トランスバーター](https://ja.wikipedia.org/wiki/トランスバーター "wikilink")（周波数変換を行う機器）を接続し5.6GHz帯、10.1GHz帯、24GHz帯での運用を可能にしている。

[アマチュア無線](https://ja.wikipedia.org/wiki/アマチュア無線 "wikilink")では、[暗語](https://ja.wikipedia.org/wiki/暗語 "wikilink")の使用や秘匿性のある無線設備は認められていない\[20\]\[21\]ため、暗号化技術であるWEP・WPAの設定などをせず、無線局を運用することが条件として求められた。[アマチュア無線で使用できる周波数帯には](../Page/アマチュア無線の周波数帯.md "wikilink")2.4GHz帯もあるが、この周波数帯での運用は、一般的に使用されている「無線LANとの誤接続の可能性がある」として許可されなかった。マイクロ波における遠距離および高速データ通信の実験を目指している。この局以外にも、首都圏で数局が無線局免許状の申請を準備している\[22\]。

### アメリカ

アメリカでは[連邦通信委員会](../Page/連邦通信委員会.md "wikilink")（FCC）が無線LAN網についての管理を行っている\[23\]。

なお、アメリカでは自治体による無線LANを含むブロードバンド網構築について、通信事業者等からは民業圧迫だという主張があり州法で規制する動きもある\[24\]。2014年2月時点で20州がブロードバンド・サービス提供に何からの制限を加えている\[25\]。

## 脚注

## 関連項目

  - [ALOHAnet](../Page/ALOHAnet.md "wikilink") - 無線LANの起源
  - [IEEE 802.11](../Page/IEEE_802.11.md "wikilink")
  - [無線アクセス](../Page/無線アクセス.md "wikilink")
  - [アクセスポイント (無線LAN)](../Page/アクセスポイント_\(無線LAN\).md "wikilink")
  - [無線センサネットワーク](https://ja.wikipedia.org/wiki/無線センサネットワーク "wikilink")
  - [公衆無線LAN](../Page/公衆無線LAN.md "wikilink")
  - [FREESPOT](../Page/FREESPOT.md "wikilink")
  - [ウォードライビング](../Page/ウォードライビング.md "wikilink")
  - [IOT](https://ja.wikipedia.org/wiki/モノのインターネット "wikilink") - モノのインターネット
  - [スマートホーム](https://ja.wikipedia.org/wiki/スマートホーム "wikilink")

## 外部リンク

  - [無線LANの安全な利用](https://www.soumu.go.jp/main_sosiki/joho_tsusin/security/enduser/security01/07.html) 総務省
  - [他人の無線LANアクセスポイントから勝手にインターネットにアクセスすることは問題があるのですか。](https://www.soumu.go.jp/main_sosiki/joho_tsusin/d_faq/5Privacy.htm) 同上

[Category:IEEE_802.11](https://ja.wikipedia.org/wiki/Category:IEEE_802.11 "wikilink") [Category:通信機器](https://ja.wikipedia.org/wiki/Category:通信機器 "wikilink") [Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink")

1.  [WaveLAN](https://ja.wikipedia.org/wiki/:en:WaveLAN "wikilink")
2.
3.  [＜KEY WORD＞ IEEE802.11b 次世代の無線LAN規格](http://www.computernews.com/scripts/bcn/vb_Bridge3.dll?VBPROG=ShowWeeklyArticle&MEM=0&Title=%81%83KEY%20%20WORD%81%84%81%40IEEE8%302%2e11b&File=F:\\inetpub\\wwwroot\\bcn\\Weekly\\BCNarchive1\\200101010194175516.htm) webBCN
4.  [無線LAN〜その栄光への道のり（後編）](http://plusd.itmedia.co.jp/broadband/0109/06/wireless2.html) ITmedia
5.  [11Mビット/秒無線LAN「AirStation」を新発売](http://buffalo.jp/products/new/2000/03_1.html) BUFFALO
6.  [「WEPは10秒で解読可能」、神戸大と広島大のグループが発表](http://internet.watch.impress.co.jp/cda/news/2008/10/14/21162.html) Impress Watch 2008年10月14日
7.  [一般家庭における無線LANのセキュリティに関する注意](http://www.ipa.go.jp/security/ciadr/wirelesslan.html) 情報処理推進機構
8.  隣家の無線LANの電波でネット接続したら違法なの? ITpro 日経NETWORK 2008年8月号 p.15
9.
10.
11.
12.
13.
14.
15.
16.
17.
18. [総務省](../Page/総務省.md "wikilink")[告示](../Page/告示.md "wikilink")[周波数割当計画](https://ja.wikipedia.org/wiki/周波数割当計画 "wikilink")の脚注
19. 『「無料でネット」と違法無線LAN販売 容疑で業者ら逮捕へ』 大阪府警 産経新聞 2010年9月22日
20. 電波法第58条 実験等無線局及びアマチュア無線局の行う通信には、暗語を使用してはならない。
21. [無線設備規則](../Page/無線設備規則.md "wikilink")第18条の2 アマチュア局の送信装置は、通信に秘匿性を与える機能を有してはならない。
22. 「マイクロウェーブワールド」熊野谿寛『[CQ ham radio](https://ja.wikipedia.org/wiki/CQ_ham_radio "wikilink")』2009年7月号、[CQ出版](../Page/CQ出版.md "wikilink")
23. [諸外国における公衆無線LANの整備状況 調査報告書](http://www.soumu.go.jp/main_content/000354253.pdf) 一般財団法人マルチメディア振興センター
24.
25.