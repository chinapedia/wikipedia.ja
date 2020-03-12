> この記事は[DoS](https://ja.wikipedia.org/wiki/DoS)から翻訳されています。


**DoS攻撃**（ドスこうげき）（英：Denial of Service attack）は、[情報セキュリティ](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")における[可用性](../Page/可用性.md "wikilink")を侵害する攻撃手法のひとつ。

ウェブサービスを稼働している[サーバ](../Page/サーバ.md "wikilink")や[ネットワーク](../Page/ネットワーク.md "wikilink")などのリソース（資源）に意図的に過剰な負荷をかけたり脆弱性をついたりする事でサービスを妨害する。

## 概要

DoS攻撃には２種類の類型があり、第一の類型はウェブサービスに大量のリクエストや巨大なデータを送りつけるなどしてサービスを利用不能にする**フラッド攻撃**（Flood＝「洪水」）であり、第二の類型はサービスの脆弱性を利用する事でサービスに例外処理をさせるなどしてサービスを利用不能にする攻撃である\[1\]\[2\]。

### 攻撃の目的

DoS攻撃の主な目的はサービスの[可用性](../Page/可用性.md "wikilink")を侵害する事にあり、具体的な被害としては、[トラフィックの増大によるネットワークの遅延](../Page/トラヒック理論.md "wikilink")、サーバやサイトへのアクセス不能といったものがあげられる\[3\]。

しかしDoS攻撃は被害者に経済的ダメージを負わせる事を目的として行われる場合もあり、**EDoS攻撃**(Economic DoS Attack)と呼ばれる。たとえばクラウド上で従量課金されているサービスにDoS攻撃をしかければサービスの運営者に高額な課金を発生させることができる\[4\]。

### DDoS攻撃

[Stachledraht_DDos_Attack.svg](https://ja.wikipedia.org/wiki/File:Stachledraht_DDos_Attack.svg "fig:Stachledraht_DDos_Attack.svg")によるDDoS攻撃\]\] フラッド型のDoS攻撃には、大量のマシンから1つのサービスに、一斉にDoS攻撃を仕掛ける**DDoS攻撃**（ディードスこうげき、**分散型サービス妨害攻撃**、）という類型がある。

DDoS攻撃の類型は2つあり、第一のものは攻撃者が大量のマシン(**踏み台**)を不正に乗っ取った上で、それらのマシンから一斉にDoS攻撃をしかける**協調分散型DoS攻撃**である。

第二の類型は、**DRDoS攻撃**（。**DoSリフレクション攻撃**、**分散反射型DoS攻撃**）\[5\]\[6\]と呼ばれる。DRDoS攻撃では、攻撃者が攻撃対象のマシンになりすまして大量のマシンに何らかのリクエストを一斉に送信する。するとリクエストを受け取ったマシン達は攻撃対象のマシンに向かって一斉に返答を返すことになるので、攻撃対象のマシンには大量の返答が集中し、高負荷がかかることになる\[7\]。DRDoS攻撃は協調分散型DDoS攻撃と異なり[マルウェア](../Page/マルウェア.md "wikilink")などで踏み台を乗っ取らなくても実行可能なため攻撃が発覚しづらい。

主なDRDoS攻撃として、[Domain Name Systemを利用した](../Page/Domain_Name_System.md "wikilink")**DNSアンプ攻撃**(。DNS amp攻撃、DNSリフレクター攻撃、DNSリフレクション攻撃とも)\[8\]や  を利用した**[Smurf攻撃](https://ja.wikipedia.org/wiki/Smurf攻撃 "wikilink")**などがある。

DRDoS攻撃に使える主なプロトコルとして、 がある\[9\]。

NetBIOSネームサーバやRPCポートマップなどへのリクエストを利用する攻撃も観測されてる\[10\]。 協調分散型DDoS攻撃とDRDoS攻撃が組み合わされることもある\[11\]。

## 攻撃手法

フラッド型のDoS攻撃は、ウェブ上に公開されている様々なサービスに対して行うことができるので、攻撃対象となるサービスごとにフラッド攻撃が存在する。

### SYNフラッド攻撃

TCPの[3ウェイ・ハンドシェイク](../Page/3ウェイ・ハンドシェイク.md "wikilink")では２つのマシンA,BがTCP接続をする際、Aが通信要求SYNパケットを送信し、BがSYN/ACKパケットを送信し、最後にAがACKパケットを送るという手順をたどる。 SYNフラッド攻撃では攻撃者が攻撃対象のマシンに対し、SYNパケットを攻撃対象に大量に送りつけ、それらすべてに対するSYN/ACKパケットを攻撃対象に発行させる。しかし攻撃者はそれらのSYN/ACKパケットに対しACKパケットを返信しない。 これにより攻撃対象はタイムアウトになるまでいつまでもACKパケットを待ち続けることとなり、リソースを食いつぶされてしまう。 対策としてはRFC 4987に[ファイアーウォール](https://ja.wikipedia.org/wiki/ファイアーウォール "wikilink")や[プロキシ](../Page/プロキシ.md "wikilink")の利用といった一般的手法の他、[SYN cookies](../Page/SYN_cookies.md "wikilink")、、SYN Cacheといった手法が記載されている。

### ICMPとUDP

**[ICMP](https://ja.wikipedia.org/wiki/ICMP "wikilink")や[UDP](https://ja.wikipedia.org/wiki/UDP "wikilink")のようなコネクションレスのサービスでは発信元の偽装が容易**なので、DoS攻撃を行う攻撃者にとって身元がわかりにくいという利点がある。

ICMPを利用したものにはICMP echo request (を利用した[ping](https://ja.wikipedia.org/wiki/ping "wikilink"))を攻撃対象に大量に送り続ける****（pingフラッド攻撃）や、踏み台にICMP echo requestをブロードキャストする事でICMP echo replyを攻撃対象に集めるDRDDoS攻撃である**[Smurf攻撃](https://ja.wikipedia.org/wiki/Smurf攻撃 "wikilink")**がある。

他にも規格外の大きなサイズのICMPパケットを送りつける事で攻撃対象をクラッシュさせる**[ping of death](https://ja.wikipedia.org/wiki/ping_of_death "wikilink")**という攻撃がかつてあったが、1996年に発見されて以降この脆弱性は防がれているため、この手法はほぼ通用しなくなっている。

UDPに対してもUDPポートに対して大量のトラフィックを送信する****があり、UDPを利用したDRDDoS攻撃を**UDPベース増幅攻撃**（UDP-Based Amplification Attack）と呼ぶ。

UDPベース増幅攻撃の中でも[NTP](https://ja.wikipedia.org/wiki/NTP "wikilink")の実装であるntpdの**monlist**コマンドを使った攻撃は増幅率が高く、19倍から206倍の増幅率に達する\[12\]。このコマンドはNTPサーバが過去にやり取りしたアドレスを最大で600件返すものであり、ntpdにおけるコマンドを利用した攻撃が2013年に観測されている\[13\]\[14\]。なおntpdのバージョン4.2.7p26以降はこのコマンドを悪用できないよう修正されている\[15\]。

この他にも[SSDPや](https://ja.wikipedia.org/wiki/:en:Simple_Service_Discovery_Protocol "wikilink")[RIPv](../Page/Routing_Information_Protocol.md "wikilink")1を利用したUDPベース増幅攻撃がある\[16\]\[17\]。

### ブラウザの再読み込み

[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")に備わっているページの再読み込み機能を使用し、[Webサーバ](../Page/Webサーバ.md "wikilink")に大量にリクエストを送りつける攻撃は**F5アタック**（**F5攻撃**）と呼ばれることがある。この名称は、「[F5キーを連打する攻撃](../Page/ファンクションキー.md "wikilink")」であることに由来する。

[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")上で動作するウェブブラウザでは、F5キーが更新機能に割り当てられていることが多いため、F5キーを押下するたびにWebサーバにリクエストが送られることになる。

### その他

  - スローなHTTP系：長時間にわたってWebサーバがコネクションを維持してくれることを悪用して能力を浪費する\[18\]。次の攻撃がある\[19\]。

      - Slow HTTP Headers（[Slowloris](https://ja.wikipedia.org/wiki/:en:Slowloris_\(software\) "wikilink")）
      - Slow HTTP POST（RUDY：R-U-Dead-Yet?）
      - Slow Read DoS

  - メールボム：サイズの大きいメールや大量のメールを送り付ける手法。

  - HTTP GET/POSTフラッド：HTTPの規格には準拠しているが負荷のかかるリクエストを大量にWebサーバ宛てに送る。

  - Teardropおよび[Land攻撃](https://ja.wikipedia.org/wiki/Land攻撃 "wikilink")：かつてTCP/IP実装にあった脆弱性\[20\]を利用した攻撃。前者は分割されたIPパケットを再統合する際パケットの重複をうまく扱えない実装上の問題を利用した攻撃、後者は攻撃者が送り主と送信先を一致させたパケットを送りつけると無限ループにはまるなどの脆弱性を利用した攻撃\[21\]。

  - かつて[Microsoft Windowsの](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")「NetBIOS over TCP/IP」に在った脆弱性が攻略された。

## 攻撃ツール

  - 荒らしプログラムとは、主に[Web](../Page/World_Wide_Web.md "wikilink")[掲示板を荒らすために作られたプログラムを指すが](../Page/電子掲示板.md "wikilink")、内容としては[HTMLの解析やHTMLFORMの送信機能を備え](../Page/HyperText_Markup_Language.md "wikilink")、連続投稿を可能とした[HTTPクライアントで](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[DoS](https://ja.wikipedia.org/wiki/DoS "wikilink")攻撃プログラムに準じている。**F5アタック**が[WebブラウザからのGETメソッドによるhttpアクセスしか出来ないのに対し荒らしプログラムは様々なメソッドにおいてのアクセスを可能としている](../Page/ウェブブラウザ.md "wikilink")。また前述した**DDoS**に準じ、**踏み台**となったサーバからの一斉攻撃を行うものもある。少しHTMLの知識があれば使える物や、アドレスを入力するだけで使えるようになる(自動解析)ツールも存在する。主に[Perl](../Page/Perl.md "wikilink")によって記述されるが、これも**踏み台**とされたサーバでの利便性を考えたものである。
  - [LOIC](https://ja.wikipedia.org/wiki/LOIC "wikilink")は、[アノニマスの常とう手段となっていた](https://ja.wikipedia.org/wiki/アノニマス_\(集団\) "wikilink")。例えば[2010年ペイバック作戦](https://ja.wikipedia.org/wiki/2010年ペイバック作戦 "wikilink")においても使われた。
  - HOIC（[High Orbit IonCanon](https://ja.wikipedia.org/wiki/:en:High_Orbit_Ion_Cannon "wikilink")）は、[LOIC](https://ja.wikipedia.org/wiki/LOIC "wikilink")の後継として[2010年ペイバック作戦](https://ja.wikipedia.org/wiki/2010年ペイバック作戦 "wikilink")の時期に開発された。
  - [Slowlorisは](https://ja.wikipedia.org/wiki/:en:Slowloris_\(software\) "wikilink")、Slow HTTP Headers攻撃を再現する。
  - [Stacheldraht](https://ja.wikipedia.org/wiki/:en:Stacheldraht "wikilink")（独：「有刺鉄線」の意）は図に示すように、踏み台側のエージェントと、エージェントを操るハンドラーと、攻撃者がハンドラーを操るクライアントから成るDDoS攻撃ツールである。
  - イギリスの[GCHQ](https://ja.wikipedia.org/wiki/GCHQ "wikilink")は、\`PREDATORS FACE'と\`ROLLING THUNDER'というDDoS攻撃ツールをもっている\[22\]といわれている。
  - [田代砲](https://ja.wikipedia.org/wiki/田代砲 "wikilink")はhttpリクエストを連続送信するスクリプトを組み込んだ極めて単純な攻撃ツールの一例である。メガ粒子田代砲や連装田代砲などのより攻撃的な亜種も多数開発された。

## 防御技法

### 各サイトにおける防御技法

  - [侵入防止システム](https://ja.wikipedia.org/wiki/侵入防止システム "wikilink")（IPS： Intrusion Prevention System）には、シグニチャに基づく防御機能と閾値に基づく防御機能が実装されている。シグネチャに基づく防御機能は、Smurf攻撃やLand攻撃のように特徴あるパケットに対して有効であったが、プロトコル実装側の脆弱性もすでに解消されている。
  - [SYNクッキーは](../Page/SYN_cookies.md "wikilink")、SYNフラッド等への対策として各OSごとに開発され、それぞれのプロトコルスタックに実装されている。
  - WAF（Web Application Firewall）には、スローなHTTP系の攻撃に対する設定を行える。Webサーバについては[QoS](https://ja.wikipedia.org/wiki/QoS "wikilink")や[タイムアウトについての設定も見直す価値がある](https://ja.wikipedia.org/wiki/タイムアウト_\(コンピュータ\) "wikilink")。

### インターネットサービスプロバイダにおける防御技法

  - イングレスフィルタリング：送信元IPアドレスを偽ったパケットをフィルタリングすることによって攻撃元とならないようにする。\[23\]
  - 代理応答\[24\]
  - [帯域制御](../Page/帯域制御.md "wikilink")
  - [ブラックホール](https://ja.wikipedia.org/wiki/:en:Black_hole_\(networking\) "wikilink")
  - [OpenFlow](https://ja.wikipedia.org/wiki/OpenFlow "wikilink")

## 事件

  - MafiaBoy

    2000年2月に[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")人の15歳の少年が6日間にわたって[ボットネット](../Page/ボットネット.md "wikilink")で[Yahoo\!](../Page/Yahoo!.md "wikilink")や[CNN](https://ja.wikipedia.org/wiki/CNN "wikilink")や[Amazon.com](../Page/Amazon.com.md "wikilink")などの人気が非常に高いサイトに対してDDoS攻撃を行い、ターゲットにしたサイトをサービス不能状態に陥らせ、自身の行動をインターネット上の[IRCチャットルームで吹聴し](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")、逮捕された。この事件は国際的に大きく取り上げられた。

  - 米国 Yahoo\!
    パソコンを利用した踏み台は、一台当たりの計算・通信能力は低いが、膨大な数が利用される事から、従来のサーバを利用したDDoS攻撃よりも甚大な被害を発生させやすい。有名なものとして2002年2月に[米国の](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[Yahoo\!](../Page/Yahoo!.md "wikilink")がこの攻撃を受け、アクセス不能になるという被害を受けている。また特に大規模な感染事件を引き起こすコンピュータウイルスのなかには、当初よりDDoS攻撃を意図して設計されたと推察されるものも見られ、2002年頃から活動が確認されているコンピュータウイルスによって形成された攻撃用パソコンネットワークにより、企業脅迫事件の発生が危惧されている。

  - コスタリカ ブックメーカー等
    2004年前後には、[ブックメーカー](../Page/ブックメーカー.md "wikilink")（公的な賭けを取りまとめている企業・団体等）のサイトが攻撃をうけ業務を妨害され、脅迫された事件<ref>

</ref>や、英国の大学生が学費の捻出に一案を講じて莫大な利益を生んだ[Million Dollar Home Pageが](https://ja.wikipedia.org/wiki/Million_Dollar_Home_Page "wikilink")[脅迫を受けたケースも報じられている](https://ja.wikipedia.org/wiki/Million_Dollar_Home_Page#DDoS攻撃 "wikilink")。

  - ニコニコ動画(β)
    2007年2月20日にDDoSによる攻撃を受け、正常に運営できる状態でなくなってしまい、同年2月24日に一時的にサービスを停止する事態となった\[25\]。

  - 2ちゃんねる（現・[5ちゃんねる](https://ja.wikipedia.org/wiki/5ちゃんねる "wikilink")）

    同掲示板サイトは度々DoS攻撃の標的にされており、中でも大規模なものが2010年3月、[バンクーバーオリンピック](https://ja.wikipedia.org/wiki/バンクーバーオリンピック "wikilink")の時期に起きている。韓国語ネットコミュニティ「ネイバー」や「ダウム」上から2ちゃんねるに対して攻撃が呼びかけられ、これにより一部のサーバーがダウンの後故障し、データが失われ、多大なる損害を出し、FBIが最終的に動く結果となった。

  - 岡崎市立中央図書館事件

    DoS攻撃とは到底呼べないような通常の「常識的」で「礼儀正しい」設計の[クローラ](../Page/クローラ.md "wikilink")が原因であっても、極端に脆弱なシステムにおいては問題を引き起こす場合がある。2010年5月のこの事件はその代表的な例であり、[三菱電機インフォメーションシステムズ](https://ja.wikipedia.org/wiki/三菱電機インフォメーションシステムズ "wikilink")の致命的な不具合をもつシステム、その不具合を認めない[岡崎市立中央図書館](https://ja.wikipedia.org/wiki/岡崎市立中央図書館 "wikilink")、警察担当者の無知および自白の強要が重なり、逮捕勾留に至る\[26\]結果となった。この事例の法的な見解については、2010年7月時点では未だ議論の対象\[27\]となっている。

  - アノニマスによるペイバック作戦

    2010年9月に[アノニマスによって](https://ja.wikipedia.org/wiki/アノニマス_\(集団\) "wikilink")、インターネット上の不正コピー行為に対応する団体等に対してDDoS攻撃が行われた。引き続いて2010年12月、アノニマスは、[ウィキリークス](https://ja.wikipedia.org/wiki/ウィキリークス "wikilink")への寄付受付を停止した銀行やクレジットカード決済会社のWebサイトに対してDDoS攻撃を実行した（作戦名：アサンジの復讐作戦）\[28\]。

  - ソニーのプレイステーションネットワーク
    2011年4月、アノニマスはソニーのインターネット配信サービス「[プレイステーションネットワーク](https://ja.wikipedia.org/wiki/プレイステーションネットワーク "wikilink")」のサーバに対してもDDoS攻撃を放った\[29\]。

  - Dynサイバーアタック

    2016年10月21日、大手ウェブサイトなどのドメイン管理システムを運営しているインターネット管理企業に対して、断続的なDDoS攻撃が行われた。結果、[Amazon.com](../Page/Amazon.com.md "wikilink")、[Paypal](https://ja.wikipedia.org/wiki/Paypal "wikilink")、[Netflix](../Page/Netflix.md "wikilink")や[Twitter](../Page/Twitter.md "wikilink")、[Reddit](../Page/Reddit.md "wikilink")、[Spotify](https://ja.wikipedia.org/wiki/Spotify "wikilink")、Gov.UK（英国政府ウェブサイト）、[ニューヨーク・タイムズ](../Page/ニューヨーク・タイムズ.md "wikilink")、[ウォール・ストリート・ジャーナル](../Page/ウォール・ストリート・ジャーナル.md "wikilink")など多くのウェブサイトサービスがオフラインになるなどの支障が出ていた\[30\]\[31\]。セキュリティー企業などによると、今回の攻撃はセキュリティの弱い[監視カメラ](../Page/監視カメラ.md "wikilink")、[ルーター](../Page/ルーター.md "wikilink")、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")などの[IoT機器を乗っ取る](https://ja.wikipedia.org/wiki/モノのインターネット "wikilink")[マルウェア](../Page/マルウェア.md "wikilink")[Miraiによって引き起こされ](https://ja.wikipedia.org/wiki/Mirai_\(マルウェア\) "wikilink")、1.2テラ[ビット毎秒](../Page/ビット毎秒.md "wikilink")の通信負荷がかけられたものとみている\[32\]\[33\]。

  - github
    2018年3月1日、[Github](https://ja.wikipedia.org/wiki/Github "wikilink")に対して、最高1.35テラ[ビット毎秒](../Page/ビット毎秒.md "wikilink")の断続的な攻撃が行われたが、[Akamai](https://ja.wikipedia.org/wiki/Akamai "wikilink")のDDoS軽減サービスを使用することによって、無効化することに成功した。\[34\]

## 関連項目

  -
  - [LOIC](https://ja.wikipedia.org/wiki/LOIC "wikilink")

  - [ボットネット](../Page/ボットネット.md "wikilink")

  - [通信妨害](../Page/通信妨害.md "wikilink")

## 脚注

## 外部リンク

  -
[Category:DoS攻撃](https://ja.wikipedia.org/wiki/Category:DoS攻撃 "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12. ＠IT「[DNSよりも高い増幅率の「理想的なDDoSツール」：NTP増幅攻撃で“史上最大規模”を上回るDDoS攻撃発生](http://www.atmarkit.co.jp/ait/articles/1402/12/news140.html)」　2016年9月28日閲覧。
13. ＠IT「[悪用した攻撃も2013年12月に観測：増幅攻撃はDNSだけではない――NTPサーバーの脆弱性に注意喚起](http://www.atmarkit.co.jp/ait/articles/1401/15/news126.html)」2016年9月28日閲覧。
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26. [岡崎図書館事件まとめ](http://librahack.jp/)
27. [情報ネットワーク法学会 - 第1回「技術屋と法律屋の座談会」](http://in-law.jp/bn/2010/index-20100716.html)
28.
29.
30. [米で大規模サイバー攻撃　ツイッターやアマゾン被害 ネット基盤サービス狙う](http://www.nikkei.com/article/DGXLASGM22H1P_S6A021C1MM0000/)（[日本経済新聞](../Page/日本経済新聞.md "wikilink")）
31. [米国で「大規模DDoS攻撃」発生：Netflix、Twitter、Spotifyがダウン](http://wired.jp/2016/10/24/internet-down-dyn-october-2016/)（[WIRED (雑誌)](../Page/WIRED_\(雑誌\).md "wikilink")）
32.
33.
34. <https://japanese.engadget.com/2018/03/01/github-1-35tbps-ddos/> 、2018年9月24日閲覧。