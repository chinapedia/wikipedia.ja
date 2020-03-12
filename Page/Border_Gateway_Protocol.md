> この記事は[Border Gateway Protocol](https://ja.wikipedia.org/wiki/Border_Gateway_Protocol)から翻訳されています。


**Border Gateway Protocol**（ボーダ・ゲートウェイ・プロトコル、略称 : **BGP**）は[インターネット](../Page/インターネット.md "wikilink")の基幹となる[ルーティングプロトコル](https://ja.wikipedia.org/wiki/ルーティングプロトコル "wikilink")である。インターネットにおける最大の構成要素となる[自律システム(Autonomous System:AS)の管理者のポリシーをAS間の経路制御に反映させる事を目的として設計された](../Page/自律システム_\(インターネット\).md "wikilink")。

## 概要

[自律システム](../Page/自律システム_\(インターネット\).md "wikilink") (AS) 間の[ルーティング](../Page/ルーティング.md "wikilink")を行う[Exterior Gateway Protocol](../Page/Exterior_Gateway_Protocol.md "wikilink")（EGP）の[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

BGPはIPネットワークか[自律システム](../Page/自律システム_\(インターネット\).md "wikilink") (AS) 間の到達性を示すプレフィックス () の[ルーティングテーブル](../Page/ルーティングテーブル.md "wikilink")を維持することでルーティングを行う。 BGPは****に分類され、技術的なメトリックは使用しないが、ネットワークの細かい規則や方針に従って[ルーティング](../Page/ルーティング.md "wikilink")を行う。 BGPはクラスレスドメイン間ルーティング ([CIDR](https://ja.wikipedia.org/wiki/CIDR "wikilink")) をサポートし、経路の集約を行うことでルーティングテーブルのサイズを削減することができる。

BGPを利用するルーター間は[IGP](../Page/Interior_Gateway_Protocol.md "wikilink")[セッション](../Page/セッション.md "wikilink")を張る。 [ルーター](../Page/ルーター.md "wikilink")の数が多いネットワークでBGPを利用する場合、IGPセッションの数が多くなり、[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")の問題が発生する。この問題を解決するために利用している技術を[ルートリフレクション](https://ja.wikipedia.org/wiki/ルートリフレクション "wikilink")と言う。

AS間の経路が変化した場合、変化した差分の情報をやり取りする。

BGPは[NSFNET](https://ja.wikipedia.org/wiki/NSFNET "wikilink")[インターネットバックボーン](https://ja.wikipedia.org/wiki/インターネットバックボーン "wikilink")を廃して、複数のバックボーンネットワークを繋ぐ完全分散ルーティングに移行するため、[EGPに代わるルーティングプロトコルとして生まれた](../Page/Exterior_Gateway_Protocol.md "wikilink")。 こうして生まれたBGPはインターネットを本当の分散システムへと変えた。

BGPの2015年現在のバージョンであるバージョン4は[1994年](../Page/1994年.md "wikilink")に提案され、[2006年](../Page/2006年.md "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")には従来のRFC 1771からRFC 4271に更新された。 その際に以前のバージョンは廃止された。

非常に大きなプライベートIPを利用したネットワークでもBGPを使用することができる。 例えばいくつかの巨大な[OSPFの橋渡しするのに使えるし](https://ja.wikipedia.org/wiki/オープン・ショーテスト・パス・ファースト "wikilink")、BGPの[マルチホーミング](https://ja.wikipedia.org/wiki/マルチホーミング "wikilink")機能を利用してネットワークの冗長性を改善することができる。

大部分のインターネットユーザにはBGPは無縁な存在であるが、大部分の[インターネット・サービス・プロバイダ](https://ja.wikipedia.org/wiki/インターネット・サービス・プロバイダ "wikilink")は他のインターネット・サービス・プロバイダとのルーティングにBGPを利用している。 その重要度はインターネット・サービス・プロバイダを電話回線業者に例えると[公衆交換電話網](../Page/公衆交換電話網.md "wikilink")上における[共通線信号No.7](https://ja.wikipedia.org/wiki/共通線信号No.7 "wikilink")に匹敵する。

## BGPの動作

BGPでの[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")間のネイバー () やピア () は[TCPの](../Page/Transmission_Control_Protocol.md "wikilink")[ポート](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")179番を通じて手動による設定で確立される。 BGPを利用するルータ（スピーカと言う）は接続を維持するために19バイトの[キープアライブ](https://ja.wikipedia.org/wiki/キープアライブ "wikilink") (keepalive) を定期的に送信する（デフォルトは60秒毎）。 トランスポートプロトコルにTCPを使うのは、ルーティングプロトコルの中ではBGPだけである。

BGPが自律システム (AS) 内で動くとき、そのBGPを内部BGP（、以下iBGPと略す）という。 iBGPで広報される経路にはアドミニストレイティブディスタンス値200をとる。 AS間で動くBGPを外部BGP（、以下eBGPと略す）といい、アドミニストレイティブディスタンス値20をとる。 BGPを使用しているルータの中でiBGPのトラフィックにかかわるルータをトランジットルータ () という。 またASの境界に位置し、eBGPを使って他のASと情報をやり取りするルータをボーダルータ () もしくはエッジルータ () という。

同一のAS内に存在し、なおかつBGPのルーティングに参加している全てのルータはフルメッシュで構成されなくてはならない。 つまり各々のルータは自分以外の全てのルータとピアを結ばなくてはならない。 このネットワーク構築方法であると、ネットワーク内のルータが増えるとコネクションの数は二次関数的に増加し、いずれはスケールの問題に直面することになる。 これを回避するには、2つの方法がBGPには組み込まれている。 ひとつはRFC 2796で定められた[ルートリフレクタ](https://ja.wikipedia.org/wiki/ルートリフレクタ "wikilink")、もうひとつはRFC 3065で定められた[コンフェデレーション](https://ja.wikipedia.org/wiki/コンフェデレーション "wikilink")である。

[ルートリフレクタ](https://ja.wikipedia.org/wiki/ルートリフレクタ "wikilink")はAS内で1つ（もしくは冗長性をとって2つ）のルータをルートリフレクタにすることで、他のルータはこのルータとだけピアを結べばいいことになり、AS内で必要なピア接続の数を減らすことができる。

[コンフェデレーション](https://ja.wikipedia.org/wiki/コンフェデレーション "wikilink")はかなり大きなネットワークで使う方法で、いくつかの対処可能なある程度小さなASを大きなASで包み込むような方法である。 コンフェデレーションはルートリフレクタと一緒に使うことができる。

### 有限状態機械

BGPのピアは他のBGPのピアとの動作の決定にシンプルな[有限状態機械](../Page/有限オートマトン.md "wikilink")（、以下FSMと略す）を使用する。 FSMには Idle, Connect, Active, OpenSent, OpenConfirm, Established の6つの状態がある。 BGPのピアはTCP接続がされ次第、ピアのセッションが確立・維持される方向で状態遷移する。

### 経路選択

BGPは経路の選択に上から下の順に以下の基準を用いる。

  - ネクストホップルータへの明示的なルート（[デフォルトルート](https://ja.wikipedia.org/wiki/デフォルトルート "wikilink")ではない）がルーティングテーブルに存在する。
  - より高いWeight属性を持つ経路を選択（[シスコシステムズ](../Page/シスコシステムズ.md "wikilink")社のルータのみ）
  - より高いローカル設定属性を持つ経路を選択
  - この[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")を起源とするBGPを選択
  - ASパスのルートが最も短いものを選択
  - オリジン属性の値がより低いルートを選択 (IGP \< EGP \< Incomplete)
  - MED () 属性の値が一番低い経路を選択
  - 内部経路より外部経路を選択
  - ネクストホップへの経路で最もIGPメトリック値が最も低いものを選択
  - もし全ての経路が外部からのものであれば、一番古いものを選択
  - 最も低いBGP IDを持つネクストホップルータを選択

## BGPにおける問題と緩和策

### ルートフラッピング

**ルートフラップダンピング**は、[ルートフラッピング](https://ja.wikipedia.org/wiki/ルートフラッピング "wikilink")による影響を軽減させるために組み込まれている。 ルータでのフラッピングは[WAN](../Page/Wide_Area_Network.md "wikilink")/WLANのリンクやインターフェースが故障したり自己修復されたりすること、誤設定されること、誤管理されることで発生する。 もしルートフラップダンピングがなかった場合、フラッピングを起こしたルートはただちにルーティングテーブルから削除されるが、その際にルータに高負荷がかかる恐れがあり、それがルーティングの安定性に重大な影響を及ぼす可能性がある。

ダンピングがあることで、ルートのフラッピングは指数減少する。 どういう原因かを問わず、ルートが利用ができなくなったが、すぐさま復活するという事象が起きた場合、初回はBGPの通常の[フェイルオーバー](https://ja.wikipedia.org/wiki/フェイルオーバー "wikilink")する時間を維持するためにダンピングは何も行わない。 2回目に同じことが起きた場合、BGPはこのプリフィックスを通ることを一定時間避ける。 以降、同じことが起きるたびに指数関数的にタイムアウトの時間が減る。 異常な状況が去り、一定時間がたつとプリフィックスは何事もなかったかのように復活する。 ダンピングは[DoS攻撃](../Page/DoS攻撃.md "wikilink")を軽減することも可能である。 またダンピングのタイミングはカスタマイズ可能である。

バックボーンのリンクとルータのプロセッサの速度が速くなりネットワークに変化があった場合、ルータのルーティングテーブルに非常に速く反映できるようになってからは、一部のネットワーク構築にかかわる人からルートフラップダンピングはそれほど重要ではないのではないか、むしろ状況を悪化させてるのではないかという意見が出ている。この意見については今後、研究と議論が必要である。

### ルーティングテーブルの増大

[BGP_Table_growth.svg](https://ja.wikipedia.org/wiki/File:BGP_Table_growth.svg "fig:BGP_Table_growth.svg")のBGPテーブル\]\] [Internet_AS.svg](https://ja.wikipedia.org/wiki/File:Internet_AS.svg "fig:Internet_AS.svg")の数\]\]

BGPとインターネットインフラが直面している最大級の問題のひとつにインターネットルーティングテーブルの増大が挙げられる。 もしインターネットルーティングテーブルが適切な範囲を超えて増大した場合、ルータのルーティングテーブルを維持するための[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")要求や[CPU](../Page/CPU.md "wikilink")の負荷はその能力を超え、[インターネット](../Page/インターネット.md "wikilink")の[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")としての役割を果たせなくなるだろう。 それに加えてルーティングテーブルが巨大化したことによりネットワーク構成に大きな変化があった場合、ネットワークの安定化（上記参照）に相当長い時間かかり、その間ネットワークサービスは全く信頼のできない状態になるか、最悪の場合、全く利用できなくなるだろう。

2001年の後半までグローバルルーティングテーブルは指数関数的に成長しており、それはインターネットへの接続性の維持への脅威となっていた。 それに対してグローバルルーティングテーブルを[CIDRや](https://ja.wikipedia.org/wiki/クラスレスドメイン間ルーティング "wikilink")[ルート集約](https://ja.wikipedia.org/wiki/ルート集約 "wikilink")を用いて、なるべく小さく維持するという各ISPによる協調努力があった。 その努力の甲斐あってその後数年は線形的成長にとどまった。

ただし、[CIDR REPORT](http://www.cidr-report.org/as2.0/)によると、2014年8月にはBGPテーブルのサイズが512Kを突破し、基幹業務向けの標準的なルータの処理能力やリソースでは処理しきれなくなってきている。 CISCO等の機器メーカーは、対応可能な上位機種にルータを変更したり、設定を変更したりすることを勧告している。

2014年8月12日から北米においてフルルートを扱うBGPルータのルーティングテーブルが溢れたことによるISP間の通信障害が発生した。 [自律システムの](../Page/自律システム_\(インターネット\).md "wikilink")1つであるVerizonの経路集約の設定が失敗し、大量の経路情報が外部に流出したことが原因であった。

## 関連項目

  - [EGP](../Page/Exterior_Gateway_Protocol.md "wikilink") - 1984年にRFCとして提案された、BGPの前身となったプロトコルである。

## 外部リンク

  - BGPに関する重要なRFC

      - RFC 4271, （廃止: RFC 1771）
      - RFC 4272, BGPのセキュリティー・脆弱性についての分析
      - RFC 4273, BGP-4のための管理オブジェクトの定義
      - RFC 4274, BGP-4プロトコルの分析
      - RFC 4275,
      - RFC 4276, BGP-4導入レポート
      - RFC 4277, BGP-4プロトコルを使った実験
      - RFC 4278,
      - RFC 3392, BGP-4のアドバタイズ能力
      - RFC 3065, BGPにおける自律システム (AS) のコンフェデレーション
      - RFC 2918, BGP-4のルートリフレッシュ能力
      - RFC 2796, BGPルートリフレクション - IBGPのフルメッシュとの選択
      - RFC 1772,

  - 廃止となったBGPに関するRFC

      - RFC 1965, 廃止 - BGPにおける自律システム（AS）のコンフェデレーション
      - RFC 1771, 廃止 -
      - RFC 1657, 廃止 - BGP-4のための管理オブジェクトの定義
      - RFC 1655, 廃止 - インターネットにおけるBGPアプリケーション
      - RFC 1654, 廃止 -
      - RFC 1105, 廃止 -

  - BGPの導入に関するもの

      - [OpenBGPD](http://www.openbgpd.org/) [OpenBSD](../Page/OpenBSD.md "wikilink")チームによって開発された[BSDライセンス](../Page/BSDライセンス.md "wikilink")のソフト
      - [Quagga](http://www.quagga.net/) [GNU Zebraから分岐したUnix](https://ja.wikipedia.org/wiki/GNU_Zebra "wikilink")-likeな[GPLのルーティングソフトウェア](../Page/GNU_General_Public_License.md "wikilink")
      - [Xorp](http://www.xorp.org/) , BSDライセンスのルーティングソフトウェア
      - [GNU Zebra](http://www.zebra.org/) BGP4をサポートしたGPLのルーティングソフトウェア
      - [BIRD](http://bird.network.cz/) Unix-likeなプラットホームのためのGPLのルーティングパッケージ

  -
  - BGPの通信障害に関する情報

      - [Major outages today, not much info at this time](https://puck.nether.net/pipermail/outages/2014-August/007090.html) 2014年8月12日に米国で発生したISP間の通信障害に関する最初の報告

[Category:ルーティングプロトコル](https://ja.wikipedia.org/wiki/Category:ルーティングプロトコル "wikilink") [Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")