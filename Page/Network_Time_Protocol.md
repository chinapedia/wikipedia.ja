> この記事は[Network Time Protocol](https://ja.wikipedia.org/wiki/Network_Time_Protocol)から翻訳されています。


**Network Time Protocol**（ネットワーク・タイム・プロトコル、**NTP**）は、[パケット交換による](../Page/パケット通信.md "wikilink")[遅延時間が変動する](../Page/レイテンシ.md "wikilink")[ネットワーク上のコンピュータシステム間で](../Page/コンピュータネットワーク.md "wikilink")[時刻同期](https://ja.wikipedia.org/wiki/時刻同期 "wikilink")させるための[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。1985年以前から運用されており、現在使用されている中で最も古いインターネットプロトコルの1つである。NTPは、の[デイヴィッド・L・ミルズ](https://ja.wikipedia.org/wiki/デイヴィッド・L・ミルズ "wikilink")によって設計された。

## 概要

NTPは、全ての参加コンピュータを[協定世界時](../Page/協定世界時.md "wikilink")(UTC)の数[ミリ秒](https://ja.wikipedia.org/wiki/ミリ秒 "wikilink")以内の時刻に[同期させることを目的としている](../Page/同期_\(計算機科学\).md "wikilink")\[1\]。

ネットワークに接続され、互いにデータの交換を行う機器において、各機器が持つ時計（以下、各機器が持つ時計を「[RTC](../Page/リアルタイムクロック.md "wikilink")」として説明する）の時刻が機器間で異なると、時刻に依存した機器間のデータ交換、例えば[電子メール](../Page/電子メール.md "wikilink")やファイルの送受信、[ログ](https://ja.wikipedia.org/wiki/ログ "wikilink")の配信などに異常をきたすおそれがある。よって、RTCの時刻は機器間で互いに同期していることが望ましい。ネットワークに接続される機器のRTCを正しい時刻に合わせる古典的な方法として[Time Protocolがある](https://ja.wikipedia.org/wiki/Time_Protocol "wikilink")。Time Protocolは正しい時刻を提供する[サーバ](../Page/サーバ.md "wikilink")から各機器が時刻値を取得する方法を定めている。しかし Time Protocol を用いて取得した時刻値にはサーバから機器に時刻値が到達するまでの通信時間が含まれない。よって、取得した時刻値には通信時間に起因する遅れの誤差が含まれてしまいRTCを正しい時刻に同期できない。NTPは通信時間による時刻値の誤差を小さくする工夫がなされた時刻同期のためのプロトコルである。

正確なを選択するために、の修正版であるを使用し、の変化の影響を軽減するように設計されている。NTPは通常、インターネット上で数十ミリ秒以内の時間を維持することができ、理想的な条件の下ではLAN上で1ミリ秒以上の精度を達成することができる。非対称なルートやネットワークの[輻輳](../Page/輻輳.md "wikilink")により、100ミリ秒以上のエラーが発生することがある\[2\]\[3\]。

このプロトコルは通常、[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")で記述されるが、相手側をタイムサーバとみなすことで[ピアツーピアネットワークにおいても使用することができる](../Page/Peer_to_Peer.md "wikilink")\[4\]。実装としては、[UDPの](../Page/User_Datagram_Protocol.md "wikilink")[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")123を使用する\[5\]\[6\]\[7\]。また、[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")や[マルチキャスト](../Page/マルチキャスト.md "wikilink")を使用することもでき、この場合、クライアントは最初に時刻同期のためにサーバと通信した後、時間の更新を受動的に受信することができる\[8\]。NTPは、直近の[閏秒](../Page/閏秒.md "wikilink")の情報は送信するが、[タイムゾーンや](https://ja.wikipedia.org/wiki/時刻帯 "wikilink")[夏時間](../Page/夏時間.md "wikilink")に関する情報は送信しない\[9\]\[10\]。

最新のプロトコルバージョンはバージョン4(NTPv4)で、でproposed standard（標準化への提唱）として文書化されている。これはで規定されているバージョン3との[後方互換性](https://ja.wikipedia.org/wiki/後方互換性 "wikilink")がある。

## 歴史

[DL_Mills-2.jpg](https://ja.wikipedia.org/wiki/File:DL_Mills-2.jpg "fig:DL_Mills-2.jpg")\]\]  1979年、ニューヨークで開催された全米コンピュータ会議において、大西洋横断衛星ネットワーク上で動作する[インターネット](../Page/インターネット.md "wikilink")サービスの最初の公開デモンストレーションが行われ、ここでネットワーク時刻同期技術が使用された。この技術は後に1981年のInternet Engineering Note (IEN) 173\[11\]に記述され、公開プロトコルが開発され、で文書化された。この技術は最初、Helloルーティングプロトコルの一部としてLANに展開され、ネットワークプロトタイピングに使用される実験的なオペレーティングシステムであるに実装され、長年にわたって使用された。

その他の関連するネットワークプロトコルは、現在でも使用可能である。その中には、イベントの時刻を記録するための[DAYTIMEプロトコル](https://ja.wikipedia.org/wiki/DAYTIMEプロトコル "wikilink")と[TIMEプロトコル](https://ja.wikipedia.org/wiki/TIMEプロトコル "wikilink")や、[ICMPの](../Page/Internet_Control_Message_Protocol.md "wikilink")[タイムスタンプ](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol#Timestamp "wikilink")、に規定されるIPタイムスタンプがある。より完全な同期システムとしては、UNIXデーモンのtimedがあり、これは[リーダー選出](https://ja.wikipedia.org/wiki/リーダー選出 "wikilink")アルゴリズムを使って全てのクライアントのためのサーバを指定する\[12\]。デジタル時刻同期サービス(DTSS)は、NTPの階層モデルに似たサーバの階層を使用している。

1985年、NTPバージョン0(NTPv0)がファズボールとUNIXの両方に実装され、NTPパケットヘッダとラウンドトリップ遅延とオフセットの計算がで文書化された。当時は比較的遅いコンピュータとネットワークしか利用できなかったにもかかわらず、大西洋のスパニングリンクでは通常100[ミリ秒](https://ja.wikipedia.org/wiki/ミリ秒 "wikilink")以上、[イーサネット](../Page/イーサネット.md "wikilink")ネットワークでは数十ミリ秒の精度が得られた。

1988年、NTPv1プロトコルのより完全な仕様と関連アルゴリズムがで公開された。この仕様は、実験結果とで文書化されたクロックフィルタアルゴリズムに基づいており、クライアントサーバモードとピアツーピアモードを記述した最初のバージョンだった。1991年、NTPv1のアーキテクチャ、プロトコル、アルゴリズムについての[デイヴィッド・L・ミルズ](https://ja.wikipedia.org/wiki/デイヴィッド・L・ミルズ "wikilink")の論文\[13\]が**に掲載され、エンジニアのコミュニティ内で広く注目を集めた。

1989年にが発行された。このRFCでは、[状態機械](https://ja.wikipedia.org/wiki/状態機械 "wikilink")を用いてNTPv2を定義し、その動作を記述するための[疑似コード](https://ja.wikipedia.org/wiki/疑似コード "wikilink")が含まれている。これは、管理プロトコルと暗号化認証スキームを導入し、アルゴリズムの大部分とともに NTPv4にも引き継がれている。しかし、NTPv2の設計はDTSSのコミュニティから[正当性を欠いていると批判され](https://ja.wikipedia.org/wiki/正当性_\(計算機科学\) "wikilink")、クロック選択手順はNTPv3以降でを組み込むように修正された\[14\]。

1992年にでNTPv3が定義された。このRFCでは、参照クロックから最終的なクライアントに至るまでの全てのエラー発生源の分析が含まれており、これにより、複数の候補の間で一致しないように見える場合に、最適なサーバを選択するのに役立つメトリックの計算が可能になった。また、ブロードキャストモードが導入された。

その後、新しい機能が追加されたり、アルゴリズムが改良されたことにより、新しいプロトコルのバージョンが必要であることが明らかになった\[15\] 。2010年には、でNTPv4の仕様案が提示された。その後、プロトコルは大きく前進しているが、2014年現在、更新されたRFCはまだ公開されていない\[16\]。ミルズが大学教授を引退したのに伴い、Harlan Stennが率いる[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトとしてリファレンス実装が維持されている\[17\]\[18\]。

## 時刻同期の仕組み

### 処理の概略

NTPプロトコル上では[協定世界時](../Page/協定世界時.md "wikilink") (UTC) を使って時刻を送受信する。

NTPサーバプログラムが他のNTPサーバに接続すると、上位NTPサーバとのネットワーク通信の遅延を継続的に計測し、受け取った時刻情報を補正して自動的にミリ秒単位の精度で自機・OSの時計を校正する。このほか後述するように自機・OSの時計の進み遅れ度合いも校正したり、他のNTPサーバからの問い合わせに応えて時刻も提供する機能が実装されることがある。

### クロック階層

[Network_Time_Protocol_servers_and_clients.svg](https://ja.wikipedia.org/wiki/File:Network_Time_Protocol_servers_and_clients.svg "fig:Network_Time_Protocol_servers_and_clients.svg") NTPでは、時間源の階層的システムを使用している。階層の各レベルは*stratum*と呼ばれる。最上位の基準クロックをstratum 0とし、stratum 0に同期しているサーバをstratum 1とする。以降、stratum *n*に同期しているサーバをstratum *n*+1とする。この番号は、基準クロックからの距離を表し、階層内での依存関係のループを防ぐために使用される。stratumの値は必ずしも品質や信頼性を示すものではなく、あるstratum 2サーバとstratum 3サーバを比較して、stratum 3サーバの方が高品質ということもあり得る。

以下に、stratum0、1、2、3について簡単に説明する。

  - stratum 0
    これは一般に[原子時計](../Page/原子時計.md "wikilink")やGPS、[電波時計](../Page/電波時計.md "wikilink")などの高精度の計時装置である。これらのデバイスは、接続されたコンピュータに対し割り込みやタイムスタンプをトリガする非常に正確な毎秒1回のパルスを生成する。stratum 0のデバイスは、リファレンスクロックともいう。
  - Stratum 1
    接続されているstratum 0デバイスの数マイクロ秒以内に[システム時刻](https://ja.wikipedia.org/wiki/システム時刻 "wikilink")が同期されているコンピュータである。stratum 1サーバは、やバックアップのために、他のstratum 1サーバとピアすることができる\[19\]。プライマリ・タイムサーバとも呼ばれる\[20\]\[21\]。
  - Stratum 2
    ネットワークを介してstratum 1サーバに同期しているコンピュータである。多くの場合、stratum 2コンピュータは複数のstratum 1サーバに問い合わせを行う。また、stratum 2コンピュータは、ピアグループ内の他のデバイスに対してより安定した[ロバストな時間を提供するために](https://ja.wikipedia.org/wiki/ロバストネス "wikilink")、他のstratum 2コンピュータとピアすることもある。
  - Stratum 3
    stratum 2のサーバに同期しているコンピュータである。これらのコンピュータは、ピアリングやデータサンプリングにstratum 2と同じアルゴリズムを採用しており、stratum 4のコンピュータのサーバとして機能することができる。

stratumの上限は15で、stratum 16はデバイスが非同期であることを示すために使用される。各コンピュータ上のNTPアルゴリズムは、[ベルマン・フォード最短経路](https://ja.wikipedia.org/wiki/ベルマン–フォード法 "wikilink")[スパニングツリーを構築するために相互に作用し](../Page/全域木.md "wikilink")、全てのクライアントからstratum 1サーバへの累積ラウンドトリップ遅延を最小化する\[22\]。

NTPプロトコルは、stratumのほか、以下に示す参照識別子(refid)を使用して、各サーバの同期化元を特定することができる。

<table>
<caption>共通時間参照識別子(refid)コード</caption>
<thead>
<tr class="header">
<th><p><strong>参照識別子</strong> (refid)[23]</p></th>
<th><p><strong>時間源</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>GOES</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/GOES" title="wikilink">Geosynchronous Orbit Environment Satellite</a>（アメリカの気象衛星）</p></td>
</tr>
<tr class="even">
<td><p>GPS</p></td>
<td><p><a href="../Page/グローバル・ポジショニング・システム.md" title="wikilink">グローバル・ポジショニング・システム</a></p></td>
</tr>
<tr class="odd">
<td><p>GAL</p></td>
<td><p><a href="../Page/ガリレオ_(測位システム).md" title="wikilink">ガリレオ</a>（ヨーロッパの測位システム）</p></td>
</tr>
<tr class="even">
<td><p>PPS</p></td>
<td><p>毎秒1パルス(pps)の時間源を表す汎用コード</p></td>
</tr>
<tr class="odd">
<td><p>IRIG</p></td>
<td><p>(IRIG)</p></td>
</tr>
<tr class="even">
<td><p>WWVB</p></td>
<td><p>長波<a href="../Page/標準電波.md" title="wikilink">標準電波</a> （アメリカ合衆国・<a href="../Page/コロラド州.md" title="wikilink">コロラド州</a><a href="../Page/フォートコリンズ_(コロラド州).md" title="wikilink">フォートコリンズ</a> 60 kHz）</p></td>
</tr>
<tr class="odd">
<td><p>DCF</p></td>
<td><p>長波標準電波 <a href="../Page/DCF77.md" title="wikilink">DCF77</a>（ドイツ・ 77.5 kHz）</p></td>
</tr>
<tr class="even">
<td><p>HBG</p></td>
<td><p>長波標準電波 （スイス・ 75 kHz（運用中止））</p></td>
</tr>
<tr class="odd">
<td><p>MSF</p></td>
<td><p>長波標準電波 <a href="../Page/MSF_(報時).md" title="wikilink">MSF</a>（イギリス・ 60 kHz）</p></td>
</tr>
<tr class="even">
<td><p>JJY</p></td>
<td><p>長波標準電波 <a href="../Page/JJY.md" title="wikilink">JJY</a>（日本・<a href="../Page/福島県.md" title="wikilink">福島県</a><a href="../Page/田村市.md" title="wikilink">田村市</a> 40 kHz、<a href="../Page/佐賀県.md" title="wikilink">佐賀県</a><a href="https://ja.wikipedia.org/wiki/佐賀市" title="wikilink">佐賀市</a> 60 kHz）</p></td>
</tr>
<tr class="odd">
<td><p>LORC</p></td>
<td><p>100 kHz</p></td>
</tr>
<tr class="even">
<td><p>TDF</p></td>
<td><p>中波標準電波 （フランス・ 162 kHz）</p></td>
</tr>
<tr class="odd">
<td><p>CHU</p></td>
<td><p>短波標準電波 （カナダ・<a href="../Page/オンタリオ州.md" title="wikilink">オンタリオ州</a><a href="../Page/オタワ.md" title="wikilink">オタワ</a>）</p></td>
</tr>
<tr class="even">
<td><p>WWV</p></td>
<td><p>短波標準電波 （アメリカ合衆国・コロラド州フォートコリンズ）</p></td>
</tr>
<tr class="odd">
<td><p>WWVH</p></td>
<td><p>短波標準電波 WWVH（アメリカ合衆国・ハワイ州カウアイ）</p></td>
</tr>
<tr class="even">
<td><p>NIST</p></td>
<td><p><a href="../Page/アメリカ国立標準技術研究所.md" title="wikilink">アメリカ国立標準技術研究所</a>(NIST)電話報時サービス</p></td>
</tr>
<tr class="odd">
<td><p>ACTS</p></td>
<td><p>NIST電話報時サービス</p></td>
</tr>
<tr class="even">
<td><p>USNO</p></td>
<td><p><a href="../Page/アメリカ海軍天文台.md" title="wikilink">アメリカ海軍天文台</a>(USNO)電話報時サービス</p></td>
</tr>
<tr class="odd">
<td><p>PTB</p></td>
<td><p>(PTB)電話報時サービス</p></td>
</tr>
<tr class="even">
<td><p>MRS</p></td>
<td><p>複数の参照源</p></td>
</tr>
<tr class="odd">
<td><p>XFAC</p></td>
<td><p>インターフェイス連携の変更（IPアドレスの変更または喪失）</p></td>
</tr>
<tr class="even">
<td><p>STEP</p></td>
<td><p>ステップ時間の変更（オフセットはステップ閾値（125ミリ秒）以上、パニック閾値（1000秒）以下）</p></td>
</tr>
</tbody>
</table>

### タイムスタンプ

NTPで使用される64ビットのタイムスタンプは、秒を表す32ビット部分と、秒未満の時間を表す32ビット部分で構成されている。秒未満の時間は、2<sup>-32</sup>秒（233ピコ秒）の理論的な分解能を持っている。秒を表す部分は32ビット符号なし[整数](../Page/整数.md "wikilink")であり、起点（[エポック](../Page/紀元.md "wikilink")）としている[1900年](../Page/1900年.md "wikilink")[1月1日](../Page/1月1日.md "wikilink") 0時0分0秒([UTC](../Page/協定世界時.md "wikilink"))からの経過秒数を表す。この値は、起点からから2<sup>32</sup>-1秒、すなわち42億9496万7295秒（約136年）で桁あふれする。最初の桁あふれは[2036年](../Page/2036年.md "wikilink")[2月7日](../Page/2月7日.md "wikilink") 6時28分15秒の次の秒に発生し\[24\]\[25\]\[26\]、起点と認識されてNTPが誤動作すると予想されている。これを**2036年問題**という。[UNIX](../Page/UNIX.md "wikilink")にはこの問題が複数の箇所で今後顕在化するとみられるが（例: [2038年問題](../Page/2038年問題.md "wikilink")）、このNTPについても該当する。

には、最上位ビットが0の場合は時刻が2036年から[2104年](https://ja.wikipedia.org/wiki/2104年 "wikilink")の間であるとみなして、2036年2月7日6時28分16秒(UTC)を起点として計算することで2036年問題を回避する方法が書かれている\[27\]。

NTPv4では128ビットのタイムスタンプが導入されており、秒と秒未満にそれぞれ64ビットを割り当てている。秒を表す64ビットのうち、半分の32ビットは現行のNTPと同じであり、残りの32ビットは、桁あふれの回数を表す*Era Number*（時代番号）である\[28\]\[29\]。ミルズによれば、「秒未満の64ビット値は、光子が光速で電子を通過するのにかかる時間を解決するのに十分である。もう1つの64ビットの値は、宇宙が薄暗くなる（[宇宙の終焉](https://ja.wikipedia.org/wiki/宇宙の終焉 "wikilink")）までの時間を明確に表現するのに十分である。」\[30\]

### クロック同期アルゴリズム

[NTP-Algorithm.svg](https://ja.wikipedia.org/wiki/File:NTP-Algorithm.svg "fig:NTP-Algorithm.svg") 一般的なNTPクライアントは、1つ以上のNTPサーバに対して[ポーリングを行う](https://ja.wikipedia.org/wiki/ポーリング_\(情報\) "wikilink")。クライアントは、タイムオフセットと[ラウンドトリップタイム](https://ja.wikipedia.org/wiki/ラウンドトリップタイム "wikilink")を計算する。

タイムオフセット *θ* は、クライアントとサーバのクロック間の絶対時間の差であり、次式で計算される。

\[\theta = {(t_1 - t_0) + (t_2 - t_3 ) \over 2}\]

ラウンドトリップタイム *δ* は、パケットの往復時間からサーバの処理時間を引いたものであり、次式で計算される。

\[\delta = {(t_3 - t_0 ) - ( t_2- t_1 )}\]

ここで、

  -
    *t*<sub>0</sub> は、クライアントがサーバへリクエストを送信した時刻
    *t*<sub>1</sub> は、サーバがクライアントのリクエストを受信した時刻
    *t*<sub>2</sub> は、サーバがクライアントへレスポンスを送信した時刻
    *t*<sub>3</sub> は、クライアントがサーバのレスポンスを受信した時刻

である\[31\]。

*θ*と*δ*の値はフィルタを通過し、統計的分析が行われる。[外れ値](https://ja.wikipedia.org/wiki/外れ値 "wikilink")は破棄され、残りの候補の中で最も優れた3つの候補から時間オフセットの推定値が導出される。その後、オフセットが徐々に減少するようにクロック周波数が調整され、[フィードバック](../Page/フィードバック.md "wikilink")ループを形成する\[32\]。

正確な同期化は、往路と復路の通信時間がほぼ等しい場合に達成される。両者に差がある場合は、その差の2分の1が誤差になる可能性がある\[33\]。極端な例では、通信の往復に合計10秒掛かった場合に最大で約5秒の誤差が発生する。

### 運用

NTPサーバを設定する際は、サーバのIPアドレスを直接指定するのではなく、ホスト名を用いて指定すべき、とされている（RFC4330による）\[34\]。

[LAN内部にクライアント台数がそれなりにある場合には](../Page/Local_Area_Network.md "wikilink")、外部へのトラフィックおよび外部NTPサーバの負荷を最小限にするため、LAN内にNTPサーバとして稼動できる機器\[35\]を用意し、この機器（内部NTPサーバ）をプロバイダなどの外部NTPサーバに接続し、各クライアントはこの内部NTPサーバに接続する設定を行うと良い。

ルーターやクライアントパソコンなどのネットワーク上の各機器では、前述のようなNTPサーバにアクセスして、機器内部の時計の時刻をNTPサーバの時刻に合わせることで内部時計の誤差が少なくなる。

### ドリフトの修正

NTPサーバの実装の多くでは、時刻の校正のみならず、時計の進み遅れの度合いの校正も行う。一般的にコンピュータ内部の時計は、ハードウェアの時計が提供する時刻をそのまま利用する場合と、割り込みなどによりソフトウェア的に時計を進める場合がある。いずれの場合も、設計状態での時計は数ppm以上（1ppmは百万分の一、およそ10日で1秒程度の精度）の狂いがあるため、他のNTPサーバからの時刻と自機の時計を数回比較した後、時計の進み遅れの度合い（ドリフト）も修正する必要がある。さらに気温変動など外乱要因による2次以上のドリフト（上述した進み遅れ度合いの変化）も存在するが、多くのNTPサーバでは一次補正（直線的なドリフトの補正）を行う実装にとどまる。

なおNTPサーバプログラムを用いてコンピュータの時刻の校正を行う場合、突然『もっともらしい時刻』に校正するのは危険である。サーバ機能を提供しているコンピュータでは、時刻が飛ぶことにより、定時に実行されるサービス（UNIXのcron・atなど）が実行されなくなったり（時計を進める場合）同じサービスが2回実行される（時計を遅らせる場合）ことがあるからである。したがって、ドリフトを調整して時刻を目的の時刻に徐々に近づけていく実装が正しい。

### 閏秒の扱い

NTPプロトコルでは、電波時計の時刻送信フォーマットのように[閏秒](../Page/閏秒.md "wikilink")の扱いも規定されている。閏秒の挿入または削除が行われるという通知は、設定ファイル、参照クロック、リモートサーバのいずれかから受け取る。参照クロックやリモートサーバから受け取る場合は、NTPパケット内の閏秒の警告情報のフィールドが使用される。警告情報を受け取った側がどう処理するかは、プログラムの実装に任される。しかし、削除された1秒に自動起動するサービスがあるかもしれなかったり、外部要因で日付が変わると無効になるライセンスがありえたりするため注意が必要である\[36\]。leap smearingと呼ばれる実装では、一秒挿入するのではなく、うるう秒の前後20時間をかけてゆっくり一秒分の時間を伸ばすことで問題を回避している\[37\]。この実装は、Google（内部的にも公開NTPサーバー上でも）とAmazon AWSによって使用されている\[38\]。

## 実装

[Ntpq_-p_query.png](https://ja.wikipedia.org/wiki/File:Ntpq_-p_query.png "fig:Ntpq_-p_query.png")

### 下位プロトコル

通常、NTPは[UDP上で動作する](../Page/User_Datagram_Protocol.md "wikilink")。UDPのポートは123番を使用する。ルータのパケットフィルタの設定でポート123番を通さないようにしている場合は、外部のNTPサーバにアクセスできなくなるので、通すように設定する必要がある

### リファレンス実装

NTPの[リファレンス実装](../Page/リファレンス実装.md "wikilink")は、プロトコルとともに20年以上にわたって継続的に開発されてきた。新しい機能が追加されても、後方互換性が維持されてきた。これには、特にクロックを規律するためのいくつかの繊細なアルゴリズムが含まれており、異なるアルゴリズムを使用しているサーバに同期させると誤動作する可能性がある。このソフトウェアは、パーソナルコンピュータを含むほぼ全てのプラットフォームに移植されている。UNIXではという[デーモンとして](../Page/デーモン_\(ソフトウェア\).md "wikilink")、Windowsでは[サービスとして動作しする](../Page/Windowsサービス.md "wikilink")。基準クロックにも対応しており、そのオフセットはリモートサーバと同じようにフィルタリングされ、分析されるが、通常はより頻繁にポーリングされる\[39\]。この実装は2017年に検査され、多数の潜在的なセキュリティ問題が発見された\[40\]。

### SNTP

[Simple Network Time Protocol](../Page/Simple_Network_Time_Protocol.md "wikilink") (SNTP)は、NTPと同じプロトコルを使用するが、長時間の状態の保存を必要としない、NTPのサブセットの実装である\[41\]。[組み込みシステム](../Page/組み込みシステム.md "wikilink")や、完全なNTP機能が必要とされないアプリケーションで使用される\[42\]。

### Windows

[Windows NTでは](https://ja.wikipedia.org/wiki/Windows_NT "wikilink")[SMBプロトコルを使ったnet](../Page/Server_Message_Block.md "wikilink") timeコマンドによる時刻同期が可能であったが、これはNTPではなかった。またそれ以前のWindowsでは、[サードパーティー](../Page/サードパーティー.md "wikilink")のソフトウェアを使用する必要があり、日本では、Windowsが本格的にインターネット対応を開始した1990年代後半に「[桜時計](https://ja.wikipedia.org/wiki/桜時計 "wikilink")」と呼ばれる、サードパーティーによるNTPの実装が有名になった。

[Windows 2000以降の](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink")[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")には、コンピュータの時計をNTP サーバに同期させる機能を持つWindows Timeサービス (W32Time)が含まれている\[43\]。W32Timeは元々[ケルベロス認証](../Page/ケルベロス認証.md "wikilink")バージョン5のために実装されたものである。ケルベロス認証では、[反射攻撃](https://ja.wikipedia.org/wiki/反射攻撃 "wikilink")への対抗として、タイムスタンプに含まれる時間が正確な時間から5分以内である必要があった。

[Windows 2000と](https://ja.wikipedia.org/wiki/Windows_2000 "wikilink")[Windows XPではSNTPのみを実装しており](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")、NTPバージョン3に対してはいくつかの規約に違反している\[44\]。[Windows Server 2003と](https://ja.wikipedia.org/wiki/Windows_Server_2003 "wikilink")[Windows Vistaからは](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、フルセットのNTPに準拠した実装となり\[45\]、GUIで時刻同期を設定することができるようになった。また、有志によってビルドされたWindows向けのntpd/ntpdateも公開されている\[46\]。

マイクロソフトは、W32Timeは1秒の精度でしか時刻同期を確実に維持できないと声明している\[47\]。より高い精度が必要な場合は、Windowsの新しいバージョンを使用するか、別のNTP実装を使用することを勧めている\[48\]。[Windows 10と](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")[Windows Server 2016では](https://ja.wikipedia.org/wiki/Windows_Server_2016 "wikilink")、特定の動作条件の下で1ミリ秒の時間精度の同期に対応している\[49\]\[50\]。

### UNIXなど

#### OpenNTPD

2004年、Henning Brauerは、セキュリティに焦点を当てて特権分離設計としたNTPの実装である[OpenNTPD](../Page/OpenNTPD.md "wikilink")を発表した。これは、[OpenBSD](../Page/OpenBSD.md "wikilink")ユーザのニーズに密着したものである一方で、 既存のNTPサーバとの互換性を保ちつつ、いくつかのプロトコルセキュリティの改善も含まれている。移植版は、[Linux](../Page/Linux.md "wikilink")のパッケージリポジトリで入手可能である。

#### ntimed

新しいNTPクライアントであるntimedが、によって2014年に開始された\[51\]。この実装は、リファレンス実装の代替として[Linux Foundationがスポンサーとなっている](../Page/Linux_Foundation.md "wikilink")。リファレンス実装を元にするより、新しい実装をゼロから書いた方が簡単であると判断されたためである。公式にはリリースされていないが、ntimedは確実にクロックを同期させることができる\[52\]。

#### NTPsec

NTPsecは、リファレンス実装を[フォークし](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")、体系的に[セキュリティを強化した実装である](https://ja.wikipedia.org/wiki/ハードニング "wikilink")。フォークポイントは2015年6月で、2014年に発生した危殆化した脆弱性への対応が行われた。最初の正式版は2017年10月にリリースされた\[53\]。安全ではない機能の削除、時代遅れのハードウェアやUNIXバリアントへの対応の削除により、元のソースコードのの75%を削除し、残りの部分を検査を受けやすくした\[54\]2017年のコードの検査では、リファレンス実装にはなかった2つを含む8つのセキュリティ問題が検出されたが、元のリファレンス実装に残っていた他の8つの問題の影響を受けることがなかった\[55\]。

#### chrony

[Chronyc.jpg](https://ja.wikipedia.org/wiki/File:Chronyc.jpg "fig:Chronyc.jpg") under [Ubuntu](../Page/Ubuntu.md "wikilink") 16.04.\]\] [chrony](https://ja.wikipedia.org/wiki/chrony "wikilink")は、[Red Hatのディストリビューション](https://ja.wikipedia.org/wiki/Red_Hat "wikilink")\[56\]にデフォルトで搭載されており、[ubuntu](https://ja.wikipedia.org/wiki/ubuntu "wikilink")のリポジトリでも利用可能である\[57\]。chronyは、不安定でスリープモードになったり、インターネットに断続的に接続したりするような一般的なコンピュータを対象としている\[58\]。また、より不安定な環境である[仮想マシン](https://ja.wikipedia.org/wiki/仮想マシン "wikilink")用にも設計されている。リソース消費量（コスト）が少ないのが特徴で、NTPだけでなく、[Precision Time Protocol](https://ja.wikipedia.org/wiki/Precision_Time_Protocol "wikilink")(PTP)にも対応している。主なコンポーネントは、コンピュータの起動時に実行されるデーモンであるchronydと、その設定のためのコマンドラインインターフェースであるchronycの2つである。

chronycは非常に安全で、数件の事故があっただけだが\[59\]、その利点は、不必要な複雑さを避けるためにゼロから書かれたコードの汎用性にある\[60\]。

chronyは[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") version 2で利用可能である。1997年にRichard Curnowによって作成され、現在はMiroslav Lichvarによってメンテナンスされている\[61\]。

### Mac

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") においても、標準でntpd/ntpdateが使用されていて、コマンドを意識せず[GUIから設定できる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。以前の[Mac OS 9でもNTPクライアントは標準で組み込まれていた](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS_9 "wikilink")。

### その他

また、[ルーター](../Page/ルーター.md "wikilink")や[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")などのネットワーク機器にNTPサーバが搭載される場合がある。もともとは高級なネットワーク機器\[62\]に搭載される機能であったが、ネットワーク普及に伴う機器の低価格化により、[2000年代](../Page/2000年代.md "wikilink")後半には民生用のネットワーク機器においてもNTPサーバが搭載されている。

## 運用と諸問題

前述の通りNTPは階層構造を採用しているため、[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")が行えるように工夫されている。しかし、NTPと同じく階層構造を採用する[DNSでは](../Page/Domain_Name_System.md "wikilink")[DHCPや](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")[PPPによるDNSサーバアドレス配信の仕組みが普及しているのに対し](../Page/Point-to-Point_Protocol.md "wikilink")、NTPではNTPサーバアドレス配信の仕組みが存在しない。よって、[エンドユーザー](../Page/エンドユーザー.md "wikilink")は自ネットワーク内のNTPサーバの存在を知ることができず、エンドユーザーが stratum 1 の公開 NTP サーバを使用する傾向がある。結果的に、一つのNTPサーバにアクセスが集中するためサーバの応答性を下げ、配信される時刻の正確性が失われる。

この問題に対する国際的なプロジェクトとして、[NTP pool project](https://www.pool.ntp.org/ja/) が存在する。これは、世界全体、あるいは国単位でまとめられたNTPサーバーのリストを用意し、DNSラウンドロビンによってNTPクライアントからのアクセスを振り分けるようにする公開DNSサーバーであり、サーバー名として 0.pool.ntp.org, 1.pool.ntp.org などのように指定すると全世界にあるNTPサーバーからランダムに選ばれたどれかのIPアドレスが返される。大陸別、あるいは国別の地域割りもなされており、たとえば 0.jp.pool.ntp.org や 1.jp.pool.ntp.org を指定すれば、日本国内にあるNTPサーバーのIPアドレスがランダムに返される。0.asia.pool.ntp.org ならアジア地区のNTPサーバーのどれかがランダムに選ばれる。プールされているサーバーのアドレスは、2017年12月現在、全世界で4146、日本国内については50である。なお、このプロジェクトはエンドユーザーからのアクセスを分散することを主目的としているため、プールされているNTPサーバーには、stratum 3や4も含まれている。

[Windows XPや](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")[Mac OSの初期設定サーバは混雑しているため](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")、[ISP提供のサーバや](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、上記のNTPプール、あるいは後述の[公開NTPサーバ等に変更すると](https://ja.wikipedia.org/wiki/#公開NTPサーバ "wikilink")、より正確な時刻取得が可能になる。

日本では情報通信研究機構 (NICT) が世界最高性能のNTPサーバ (ntp.nict.jp) を2006年6月より一般公開したので、負荷に起因する問題は解決の方向へ向かうと思われる。NICTによれば、世界中のNTPリクエストを合計しても数万リクエスト/秒程度なので、100万リクエスト/秒を扱える新しいシステムでは負荷の問題ではなく知名度の低さが問題としている\[63\]。

### clock.nc.fukuoka-u.ac.jp問題

日本では、[福岡大学](../Page/福岡大学.md "wikilink")が[1993年](../Page/1993年.md "wikilink")（[平成](../Page/平成.md "wikilink")5年）からNTPサーバを公開しているが、ここを参照するように設定された機器や組み込まれたソフトウェアが非常に多いため\[64\]、アクセス集中による過負荷に悩まされていることが、2005年に報告された\[65\]。契約している[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") (ISP) の公開するサーバを利用することで、この問題は解消するので、ISPや研究機関等が加入者向けにサービスするNTPサーバや公開NTPサーバに、今すぐ設定を変更することである。

2017年現在も、福岡大学NTPサーバへのデータトラフィックは過大な状態が続いており、平均180Mbpsに達している\[66\]。アクセス過多の原因の一つとして、一部メーカーのネットワーク機器にNTPサーバのアドレスがハードコーティングされていることが挙げられている。

ネットワーク機器にアドレスがハードコーティングされた一例として、[TP-Link製の無線LAN中継器がある](https://ja.wikipedia.org/wiki/TP-LINK_Technologies "wikilink")。この機器は、本来の時刻同期の目的ではなくインターネット回線の接続状態を確認するため、福岡大学を含む複数のNTPサーバへ数秒間隔でアクセスする仕様になっていた。TP-Linkからは管理画面を開いている間のみNTPサーバへアクセスするよう、仕様を変更したファームウェアが公開されている\[67\]。

2017年、福岡大学は同 NTP サービスの提供を2018年4月以降に停止する事を発表した\[68\]。これは、データトラフィックが多すぎるため、大学ネットワーク運用に無駄な費用がかかっている事や、サービス開始当初の1993年はNTPで時刻同期することが研究対象であったが、現在では様々なアプライアンスが販売されているため、NTPの研究として役目を終えたと理由を挙げている。2019年3月12日に2台あるNTPサーバーのうちの1台を停止した\[69\]。

### ウィスコンシン大学-ネットギアNTP問題

[ネットギア](https://ja.wikipedia.org/wiki/ネットギア "wikilink")製の[ルーター](../Page/ルーター.md "wikilink")が[ウィスコンシン大学](../Page/ウィスコンシン大学.md "wikilink")のNTPサーバを参照するよう[ハードコード](https://ja.wikipedia.org/wiki/ハードコード "wikilink")されていたため、負荷が極度に集中した。以下に問題の経緯を記す。

[2003年](../Page/2003年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")、ウィスコンシン大学に対して平均毎秒4万パケット\[70\]のNTPサービスへの接続が行われた。

これに対し大学側はNTP用に公開していたポートを閉じ、悪意あるアクセスは数時間のうちに収まるであろうと考えていた。しかしながら1ヵ月後の2003年6月の時点において、大学側の予想に反するどころかさらに状況は悪化し平均毎秒25万パケットを記録。さらなる調査によって、多くの接続元が1秒毎に問い合わせを行っている事に不審を抱くこととなる。接続元となっている2つの大学に協力を要請。調査結果の中で双方ともにネットギア製のルーターを使用していた事が判明、型番もMR814であると特定された。

2003年[6月16日](https://ja.wikipedia.org/wiki/6月16日 "wikilink")、大学側はネットギア社のカスタマーサポート宛に電子メールにて状況の報告を行ったが返答がないため直接交渉を行い、2003年6月19日に、ネットギアから「開発者によるデバッグ時の設定値の残骸が引き起こしたもの」との説明が大学側に報告され、協力体制が整備された。

2003年8月の時点において、影響を受けた生産台数70万台から行われる最大毎秒70万パケットに及ぶリスクに対して、大学側はルーター使用者に影響がでないよう配慮し、ネットギアからはファームウェアのバージョンアップが提供された。これによりウィスコンシン大学の転送量の増加傾向は弱くなり、2003年11月からは減少傾向に転じることとなった。

なお、これらの事件の詳細は、2003年[8月21日](../Page/8月21日.md "wikilink")に、ウィスコンシン大学のDave Plonkaによりまとめられている\[71\]。

他に、[FreeBSD](../Page/FreeBSD.md "wikilink")の有力開発者であるPoul-Henning Kamp(phk)が発見した[D-link製ルータの問題や](https://ja.wikipedia.org/wiki/Dリンク "wikilink")、ダブリンのTardis and Trinity Collegeの問題など、同様の問題が発生している。を参照のこと。

## 脚注

### 注釈

### 出典

## 参考文献

  -
  -
## 関連項目

  -
  -
  - [国際原子時](../Page/国際原子時.md "wikilink")

  -
  -
  -
  -
  - [Precision Time Protocol](https://ja.wikipedia.org/wiki/Precision_Time_Protocol "wikilink") (IEEE 1588 PTP)

## 外部リンク

  - [NTP Project](https://www.ntp.org/)
  - [NTP Server Test Online](https://ncomputers.org/ntptest)

### 公開NTPサーバ

  - [Public NTP Time Server Lists](https://support.ntp.org/bin/view/Servers/WebHome) ntp.orgによる公開サーバリスト
      - [Stratum One Time Servers](https://support.ntp.org/bin/view/Servers/StratumOneTimeServers) stratum 1サーバ
      - [Stratum Two Time Servers](https://support.ntp.org/bin/view/Servers/StratumTwoTimeServers) stratum 2サーバ
      - [NTP Pool Time Servers](https://support.ntp.org/bin/view/Servers/NTPPoolServers) ntp.orgによるプールサーバリスト。全世界共通のものの他に、大陸毎、国毎のプールサーバが存在する。

#### 日本国内

  - [時刻情報提供サービス for Public](https://www.mfeed.ad.jp/ntp/) - [インターネットマルチフィード](../Page/インターネットマルチフィード.md "wikilink")(MFEED)による、stratum 2のNTPサービス。国内の多くの[ISPと直接接続されているためネットワーク的に近い](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")。
  - [NICT 公開NTPサービス](https://jjy.nict.go.jp/tsp/PubNtp/) - 日本標準時に直結されたstratum 1のNTPサービス。国内の多くのISPからはホップ数や[ping](https://ja.wikipedia.org/wiki/ping "wikilink")の応答の面で不利。
  - [NTP service : ntp.ring.gr.jp](http://www.ring.gr.jp/ring/ntp.html.ja) - [Ring Server Project参加組織提供によるプールサーバ](https://ja.wikipedia.org/wiki/Ring_Server_Project "wikilink")。stratumは2から4。
  - [NTP - wiki@nothing](http://wiki.nothing.sh/page/NTP) - 日本国内のISPや研究機関等のNTPサーバおよび公開NTPサーバの情報をまとめている。

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:時間に関するネットワークソフト](https://ja.wikipedia.org/wiki/Category:時間に関するネットワークソフト "wikilink")

1.
2.
3.
4.
5.
6.  [Page 16](http://tools.ietf.org/html/rfc5905)
7.  RFC1700のWELL KNOWN PORT NUMBERSではTCPとUDPの2つが指定されているが、NTPの規格を示したRFC1305ではUDPのみとなっている。
8.
9.
10.
11.
12.
13.
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
24. [RFC 4330](https://tools.ietf.org/html/rfc4330) 3. NTP Timestamp Format
25.
26.
27.
28.
29.
30.  Digital Systems Seminar presentation by David Mills, 2006-04-26
31.
32.
33.
34. [日本標準時プロジェクト　公開NTP FAQ ［Q.1-2］ ホスト名ではなく、IPアドレスで設定しても良いですか？](http://www2.nict.go.jp/aeri/sts/tsp/PubNtp/qa.html#q1-2)
35. もし[ルーター](../Page/ルーター.md "wikilink")などで提供できなければ、NTPサービス提供専用の古い[パソコンをセットアップしても良いし](../Page/パーソナルコンピュータ.md "wikilink")、またサーバ的な存在になっている既存のパソコン等にNTPサーバをインストールしても良い
36. [安藤幸央のランダウン44 時を欠ける症状-うるう秒から考えるサステナビリティ](http://www.atmarkit.co.jp/fjava/column/andoh/andoh44.html) アットマーク・アイティ 2011年[10月4日](https://ja.wikipedia.org/wiki/10月4日 "wikilink")閲覧
37. [Making every (leap) second count with our new public NTP servers](https://cloudplatform.googleblog.com/2016/11/making-every-leap-second-count-with-our-new-public-NTP-servers.html)
38.
39.
40.
41.
42.
43.
44.
45.
46. [Meinberg NTP Software Downloads](http://www.meinbergglobal.com/english/sw/ntp.htm)
47.
48.
49.
50.
51.
52.
53.
54.
55.
56.
57.
58.
59.
60.
61.
62. 特にルーターや[ゲートウェイ](../Page/ゲートウェイ.md "wikilink")
63. 日経NETWORK 2006年8月号 「NICTの標準時刻配信サービス」p68
64. 前述の「桜時計」もそのひとつである。
65. [福岡大のNTPサーバがアクセス集中で悲鳴](http://www.itmedia.co.jp/news/articles/0501/21/news059.html) - ITmediaニュース 2005年01月21日（2014年4月20日閲覧）
66. [公開NTPサーバーの運用と課題](http://enog.jp/wp-content/uploads/2017/10/20171027_ENOG47_tanizaki.pdf) 2017/12/27閲覧
67. [＜更新＞TP-Link製無線LAN中継器によるNTPサーバーへのアクセスに関して](http://www.tp-link.jp/news-details-17792.html) 2017/12/27閲覧
68.
69.  福岡大学情報基盤センター|url=[https://www.ipc.fukuoka-u.ac.jp/service/ntp/public_ntp/|website=www.ipc.fukuoka-u.ac.jp|accessdate=2019-03-27](https://www.ipc.fukuoka-u.ac.jp/service/ntp/public_ntp/%7Cwebsite=www.ipc.fukuoka-u.ac.jp%7Caccessdate=2019-03-27)}}
70. 異常値のようなピーク時で毎秒8万パケット
71.