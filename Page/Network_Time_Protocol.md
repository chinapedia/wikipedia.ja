> この記事は[Network Time Protocol](https://ja.wikipedia.org/wiki/Network_Time_Protocol)から翻訳されています。


**Network Time Protocol**（ネットワーク・タイム・プロトコル、略称**NTP**（エヌティーピー））は、[ネットワークに接続される機器において](../Page/コンピュータネットワーク.md "wikilink")、機器が持つ[時計](../Page/時計.md "wikilink")を正しい[時刻](../Page/時刻.md "wikilink")へ[同期するための](../Page/同期_\(計算機科学\).md "wikilink")[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。

[OSI基本参照モデル](https://ja.wikipedia.org/wiki/OSI基本参照モデル "wikilink")の第7層（[アプリケーション層](../Page/アプリケーション層.md "wikilink")）に位置し、[UDPポート](../Page/User_Datagram_Protocol.md "wikilink")\[1\]の123番を使用する。

## 概要

ネットワークに接続され、互いにデータの交換を行う機器において、各機器が持つ時計（以下、各機器が持つ時計を「[RTC](../Page/リアルタイムクロック.md "wikilink")」として説明する）の時刻が機器間で異なると、時刻に依存した機器間のデータ交換、例えば[電子メール](../Page/電子メール.md "wikilink")やファイルの送受信、[ログ](https://ja.wikipedia.org/wiki/ログ "wikilink")の配信などに異常をきたすおそれがある。よって、RTCの時刻は機器間で互いに同期していることが望ましい。

ネットワークに接続される機器のRTCを正しい時刻に合わせる古典的な方法として[Time Protocolがある](https://ja.wikipedia.org/wiki/Time_Protocol "wikilink")。Time Protocolは正しい時刻を提供する[サーバ](../Page/サーバ.md "wikilink")から各機器が時刻値を取得する方法を定めている。しかし Time Protocol を用いて取得した時刻値にはサーバから機器に時刻値が到達するまでの通信時間が含まれない。よって、取得した時刻値には通信時間に起因する遅れの誤差が含まれてしまいRTCを正しい時刻に同期できない。

NTPは通信時間による時刻値の誤差を小さくする工夫がなされた時刻同期のためのプロトコルである。

2010年6月、最新バージョンのNTP4が[RFCのProposed](../Page/Request_for_Comments.md "wikilink") Standardとなった\[2\]。

## 時刻同期の仕組み

### 処理の概略

NTPプロトコル上では[協定世界時](../Page/協定世界時.md "wikilink") (UTC) を使って時刻を送受信する。

NTPサーバプログラムが他のNTPサーバに接続すると、上位NTPサーバとのネットワーク通信の遅延を継続的に計測し、受け取った時刻情報を補正して自動的にミリ秒単位の精度で自機・OSの時計を校正する。このほか後述するように自機・OSの時計の進み遅れ度合いも校正したり、他のNTPサーバからの問い合わせに応えて時刻も提供する機能が実装されることがある。

### 階層構造

[thumb](https://ja.wikipedia.org/wiki/ファイル:Architecture_NTP_labels_ja.svg "wikilink") NTPはstratumと呼ばれる階層構造を持ち、最上位のサーバが正確な時計から標準時を取得し、下位のホストはそれを参照する事で時刻を合わせる。最上位のNTPサーバはstratum 1であり、階層を下りるごとに数字が一つずつ大きくなる。stratum 16が最下位で、stratum 16に同期することは出来ない。NTPでは複数のサーバへ時刻を問い合わせることが可能で、これにより可用性と精度の向上が期待できる。通常サーバは複数の上位サーバを利用して時刻を取得する。一般にstratumの大きさよりも、サーバとのネットワーク的な近さのほうが時刻精度に大きく影響する。

[GPSや](../Page/グローバル・ポジショニング・システム.md "wikilink")[標準電波](../Page/JJY.md "wikilink")、[原子時計](../Page/原子時計.md "wikilink")などの正確な時刻源 (stratum 0) に直結されたNTPサーバはstratum 1となる。これらの時刻源は誤差±1μ秒未満（100万分の1秒未満）の非常に正確な時刻を刻んでいる\[3\]。また現実には、電波時計やGPSの受信機自体の信号遅延、受信機とstratum 1となる機器の間の遅延が無視できない\[4\]。GPS衛星には原子時計が搭載されており、その電波にはGPSタイムと呼ばれる時刻情報が含まれている。標準電波は地域の標準時を保持する組織が時刻情報を電波で送出するものであり、日本の場合は[独立行政法人](../Page/独立行政法人.md "wikilink")[情報通信研究機構](../Page/情報通信研究機構.md "wikilink")（NICT、旧・通信総合研究所 (CRL)）が行っている。

代表的なNTPの実装であるntpdでは、上位stratumだけではなく、複数の同位・下位stratumのNTPサーバとも接続できる\[5\]。ピアとよばれる他のサーバをどれにするかの設定は設定ファイルなどにより行う。より多くの複数のサーバと時刻の比較・ネットワークの遅延、および遅延のばらつきの計測を行ない、重み付けを行なって最ももっともらしい時刻を現在時刻とする。

### 通信遅延時間の計測

NTPでは、往復の通信時間を計測することで遅延時間の補正を行っている。具体的には、クライアントがリクエストを送信した時刻を \(t_s\)、サーバがクライアントのリクエストを受信した時刻を \(T_r\)、サーバがレスポンスを送信した時刻を \(T_s\)、クライアントがサーバのレスポンスを受信した時刻を \(t_r\) とすると、通信遅延時間 \(\delta\) は、

\(\delta = (t_r - t_s) - (T_s - T_r)\)

で表される。これは、パケットの往復時間からサーバの処理時間を引いたものである。一方、往路と復路の通信時間に差がないと仮定すれば、クライアントの時計の遅延時間 \(\theta\) は、

\(\theta = \frac{T_s + T_r}{2} - \frac{t_s + t_r}{2}\)

で表される。これは、サーバ、クライアントの、[パケット通信](../Page/パケット通信.md "wikilink")の送信時刻、受信時刻の平均の差である。

往路と復路の通信時間は等しい物として計算しているため、両者に差がある場合は、その差の2分の1が誤差になる可能性がある。極端な例では、通信の往復に合計10秒掛かった場合に最大で約5秒の誤差が発生する。

### 運用

NTPサーバを設定する際は、サーバのIPアドレスを直接指定するのではなく、ホスト名を用いて指定すべき、とされている（RFC4330による）\[6\]。

[LAN内部にクライアント台数がそれなりにある場合には](../Page/Local_Area_Network.md "wikilink")、外部へのトラフィックおよび外部NTPサーバの負荷を最小限にするため、LAN内にNTPサーバとして稼動できる機器\[7\]を用意し、この機器（内部NTPサーバ）をプロバイダなどの外部NTPサーバに接続し、各クライアントはこの内部NTPサーバに接続する設定を行うと良い。

ルーターやクライアントパソコンなどのネットワーク上の各機器では、前述のようなNTPサーバにアクセスして、機器内部の時計の時刻をNTPサーバの時刻に合わせることで内部時計の誤差が少なくなる。

### ドリフトの修正

NTPサーバの実装の多くでは、時刻の校正のみならず、時計の進み遅れの度合いの校正も行う。一般的にコンピュータ内部の時計は、ハードウェアの時計が提供する時刻をそのまま利用する場合と、割り込みなどによりソフトウェア的に時計を進める場合がある。いずれの場合も、設計状態での時計は数ppm以上（1ppmは百万分の一、およそ10日で1秒程度の精度）の狂いがあるため、他のNTPサーバからの時刻と自機の時計を数回比較した後、時計の進み遅れの度合い（ドリフト）も修正する必要がある。さらに気温変動など外乱要因による2次以上のドリフト（上述した進み遅れ度合いの変化）も存在するが、多くのNTPサーバでは一次補正（直線的なドリフトの補正）を行う実装にとどまる。

なおNTPサーバプログラムを用いてコンピュータの時刻の校正を行う場合、突然『もっともらしい時刻』に校正するのは危険である。サーバ機能を提供しているコンピュータでは、時刻が飛ぶことにより、定時に実行されるサービス（UNIXのcron・atなど）が実行されなくなったり（時計を進める場合）同じサービスが2回実行される（時計を遅らせる場合）ことがあるからである。したがって、ドリフトを調整して時刻を目的の時刻に徐々に近づけていく実装が正しい。

### 閏秒の扱い

NTPプロトコルでは、電波時計の時刻送信フォーマットのように[閏秒](../Page/閏秒.md "wikilink")の扱いも規定されている。閏秒は、原子時 (TAI) と同期して進むUTCが、地球の自転速度の変化によって[世界時](../Page/世界時.md "wikilink") (UT1) から長年の間に大きく狂わないように、世界的な協定に基づいてUTCに挿入または削除される1秒である。これは本質的にコンピュータの時計の進み遅れとは異なり、必ず±1秒の差となる。したがって、問合せ先のNTPサーバからうるう秒挿入または削除を警告するパケットが送られてきたときは、自機の時計を1秒ずらす（ドリフトは調整しない）ことになる。

## 2036年問題

NTPでは、時刻の表現に**[1900年](../Page/1900年.md "wikilink")[1月1日](../Page/1月1日.md "wikilink") 0時0分0秒** ([UTC](../Page/協定世界時.md "wikilink"))（この時間を以下では「起点」とする）**からの積算[秒](../Page/秒.md "wikilink")数**を使用している。この値は32ビット符号なし[整数](../Page/整数.md "wikilink")で表現されるため、起点から (2<sup>32</sup>-1) 秒、すなわち42億9496万7295秒までしか表現できない。

その結果、起点から42億9496万7295秒経過した**[2036年](../Page/2036年.md "wikilink")[2月7日](../Page/2月7日.md "wikilink") 6時28分15秒** (UTC) の次の秒（16秒）\[8\]が桁あふれによって起点と認識されてしまい、NTPが誤動作すると予想されている。

これが**2036年問題**である。[UNIX](../Page/UNIX.md "wikilink")\[9\]にはこの問題が複数の箇所で今後顕在化するとみられるが（例: [2038年問題](../Page/2038年問題.md "wikilink")）、このNTPについても該当する。

なお、RFC 4330には、最上位ビットが0の場合は時刻が2036年から[2104年](https://ja.wikipedia.org/wiki/2104年 "wikilink")の間であるとみなして、2036年2月7日6時28分16秒(UTC)を起点として計算することで2036年問題を回避する方法が書かれている\[10\]。

## 実装

### 下位プロトコル

通常、NTPは[UDP上で動作する](../Page/User_Datagram_Protocol.md "wikilink")。UDPのポートは123番を使用する。ルータのパケットフィルタの設定でポート123番を通さないようにしている場合は、外部のNTPサーバにアクセスできなくなるので、通すように設定する必要がある

### リファレンス実装

代表的なNTPの実装として、[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")用のNTPサーバである[ntpd](https://ja.wikipedia.org/wiki/ntpd "wikilink")（旧xntpd）、およびNTPクライアントの[ntpdate](https://ja.wikipedia.org/wiki/ntpdate "wikilink")がある。ntpd/ntpdateは多くのオペレーティングシステムで標準的に組み込まれている。

### SNTP

[Simple Network Time Protocol](../Page/Simple_Network_Time_Protocol.md "wikilink") (SNTP) はNTPのサブセット版である。

### UNIXなど

[OpenBSD](../Page/OpenBSD.md "wikilink")では、ntpd/ntpdateの代替となる[OpenNTPD](../Page/OpenNTPD.md "wikilink")がサブプロジェクトの一つとして提供されている。

[X Window Systemの](../Page/X_Window_System.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")でもntpd/ntpdateをGUIより設定するユーティリティが付属するものがある。

スクラッチから書かれた実装として[chrony](https://ja.wikipedia.org/wiki/chrony "wikilink")がある。[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") 8と[SUSE Linux Enterprise Server](https://ja.wikipedia.org/wiki/SUSE_Linux_Enterprise_Server "wikilink") 15ではデフォルトのNTP[クライアント及び](../Page/クライアント_\(コンピュータ\).md "wikilink")[サーバ](../Page/サーバ.md "wikilink")ーとしてchronyを採用している\[11\]\[12\]。また、多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")でも利用可能である。

### Mac

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") においても、標準でntpd/ntpdateが使用されていて、コマンドを意識せず[GUIから設定できる](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。以前の[Mac OS 9でもNTPクライアントは標準で組み込まれていた](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS_9 "wikilink")。

### Windows

[Microsoft Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Active Directoryにおいて時刻同期が必須となったため](../Page/Active_Directory.md "wikilink")、Windows TimeサービスとしてNTPの機能が組み込まれている\[13\]。Windows NTでは[SMBプロトコルを使ったnet](../Page/Server_Message_Block.md "wikilink") timeコマンドによる時刻同期が可能であったが、これはNTPではなかった。またそれ以前のWindowsでは、[サードパーティー](../Page/サードパーティー.md "wikilink")のソフトウェアを使用する必要があり、日本では、Windowsが本格的にインターネット対応を開始した1990年代後半に「[桜時計](https://ja.wikipedia.org/wiki/桜時計 "wikilink")」と呼ばれる、サードパーティーによるNTPの実装が有名になった。

[Active Directoryが実装された](../Page/Active_Directory.md "wikilink")[Windows 2000では](../Page/Microsoft_Windows_2000.md "wikilink")、NTPのサブセット版である[Simple Network Time Protocol](../Page/Simple_Network_Time_Protocol.md "wikilink") (SNTP) が採用された。[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") / Server 2003からはフルセット版であるNTPが用いられ、GUIで時刻同期を設定することができるようになった。また、有志によってビルドされたWindows向けのntpd/ntpdateも公開されている\[14\]。

### その他

また、[ルーター](../Page/ルーター.md "wikilink")や[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")などのネットワーク機器にNTPサーバが搭載される場合がある。もともとは高級なネットワーク機器\[15\]に搭載される機能であったが、ネットワーク普及に伴う機器の低価格化により、[2000年代](../Page/2000年代.md "wikilink")後半には民生用のネットワーク機器においてもNTPサーバが搭載されている。

## 運用と諸問題

前述の通りNTPは階層構造を採用しているため、[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")が行えるように工夫されている。しかし、NTPと同じく階層構造を採用する[DNSでは](../Page/Domain_Name_System.md "wikilink")[DHCPや](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")[PPPによるDNSサーバアドレス配信の仕組みが普及しているのに対し](../Page/Point-to-Point_Protocol.md "wikilink")、NTPではNTPサーバアドレス配信の仕組みが存在しない。よって、[エンドユーザー](../Page/エンドユーザー.md "wikilink")は自ネットワーク内のNTPサーバの存在を知ることができず、エンドユーザーが stratum 1 の公開 NTP サーバを使用する傾向がある。結果的に、一つのNTPサーバにアクセスが集中するためサーバの応答性を下げ、配信される時刻の正確性が失われる。

この問題に対する国際的なプロジェクトとして、[NTP pool project](https://www.pool.ntp.org/ja/) が存在する。これは、世界全体、あるいは国単位でまとめられたNTPサーバーのリストを用意し、DNSラウンドロビンによってNTPクライアントからのアクセスを振り分けるようにする公開DNSサーバーであり、サーバー名として 0.pool.ntp.org, 1.pool.ntp.org などのように指定すると全世界にあるNTPサーバーからランダムに選ばれたどれかのIPアドレスが返される。大陸別、あるいは国別の地域割りもなされており、たとえば 0.jp.pool.ntp.org や 1.jp.pool.ntp.org を指定すれば、日本国内にあるNTPサーバーのIPアドレスがランダムに返される。0.asia.pool.ntp.org ならアジア地区のNTPサーバーのどれかがランダムに選ばれる。プールされているサーバーのアドレスは、2017年12月現在、全世界で4146、日本国内については50である。なお、このプロジェクトはエンドユーザーからのアクセスを分散することを主目的としているため、プールされているNTPサーバーには、stratum 3や4も含まれている。

[Windows XPや](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")[Mac OSの初期設定サーバは混雑しているため](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")、[ISP提供のサーバや](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、上記のNTPプール、あるいは後述の[公開NTPサーバ等に変更すると](https://ja.wikipedia.org/wiki/#公開NTPサーバ "wikilink")、より正確な時刻取得が可能になる。

日本では情報通信研究機構 (NICT) が世界最高性能のNTPサーバ (ntp.nict.jp) を2006年6月より一般公開したので、負荷に起因する問題は解決の方向へ向かうと思われる。NICTによれば、世界中のNTPリクエストを合計しても数万リクエスト/秒程度なので、100万リクエスト/秒を扱える新しいシステムでは負荷の問題ではなく知名度の低さが問題としている\[16\]。

### clock.nc.fukuoka-u.ac.jp問題

日本では、[福岡大学](../Page/福岡大学.md "wikilink")が[1993年](../Page/1993年.md "wikilink")（[平成](../Page/平成.md "wikilink")5年）からNTPサーバを公開しているが、ここを参照するように設定された機器や組み込まれたソフトウェアが非常に多いため\[17\]、アクセス集中による過負荷に悩まされていることが、2005年に報告された\[18\]。契約している[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") (ISP) の公開するサーバを利用することで、この問題は解消するので、ISPや研究機関等が加入者向けにサービスするNTPサーバや公開NTPサーバに、今すぐ設定を変更することである。

2017年現在も、福岡大学NTPサーバへのデータトラフィックは過大な状態が続いており、平均180Mbpsに達している\[19\]。アクセス過多の原因の一つとして、一部メーカーのネットワーク機器にNTPサーバのアドレスがハードコーティングされていることが挙げられている。

ネットワーク機器にアドレスがハードコーティングされた一例として、[TP-Link製の無線LAN中継器がある](https://ja.wikipedia.org/wiki/TP-LINK_Technologies "wikilink")。この機器は、本来の時刻同期の目的ではなくインターネット回線の接続状態を確認するため、福岡大学を含む複数のNTPサーバへ数秒間隔でアクセスする仕様になっていた。TP-Linkからは管理画面を開いている間のみNTPサーバへアクセスするよう、仕様を変更したファームウェアが公開されている\[20\]。

2017年、福岡大学は同 NTP サービスの提供を2018年4月以降に停止する事を発表した\[21\]。これは、データトラフィックが多すぎるため、大学ネットワーク運用に無駄な費用がかかっている事や、サービス開始当初の1993年はNTPで時刻同期することが研究対象であったが、現在では様々なアプライアンスが販売されているため、NTPの研究として役目を終えたと理由を挙げている。2019年3月12日に2台あるNTPサーバーのうちの1台を停止した\[22\]。

### ウィスコンシン大学-ネットギアNTP問題

[ネットギア](https://ja.wikipedia.org/wiki/ネットギア "wikilink")製の[ルーター](../Page/ルーター.md "wikilink")が[ウィスコンシン大学](../Page/ウィスコンシン大学.md "wikilink")のNTPサーバを参照するよう[ハードコード](https://ja.wikipedia.org/wiki/ハードコード "wikilink")されていたため、負荷が極度に集中した。以下に問題の経緯を記す。

[2003年](../Page/2003年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")、ウィスコンシン大学に対して平均毎秒4万パケット\[23\]のNTPサービスへの接続が行われた。

これに対し大学側はNTP用に公開していたポートを閉じ、悪意あるアクセスは数時間のうちに収まるであろうと考えていた。しかしながら1ヵ月後の2003年6月の時点において、大学側の予想に反するどころかさらに状況は悪化し平均毎秒25万パケットを記録。さらなる調査によって、多くの接続元が1秒毎に問い合わせを行っている事に不審を抱くこととなる。接続元となっている2つの大学に協力を要請。調査結果の中で双方ともにネットギア製のルーターを使用していた事が判明、型番もMR814であると特定された。

2003年[6月16日](https://ja.wikipedia.org/wiki/6月16日 "wikilink")、大学側はネットギア社のカスタマーサポート宛に電子メールにて状況の報告を行ったが返答がないため直接交渉を行い、2003年6月19日に、ネットギアから「開発者によるデバッグ時の設定値の残骸が引き起こしたもの」との説明が大学側に報告され、協力体制が整備された。

2003年8月の時点において、影響を受けた生産台数70万台から行われる最大毎秒70万パケットに及ぶリスクに対して、大学側はルーター使用者に影響がでないよう配慮し、ネットギアからはファームウェアのバージョンアップが提供された。これによりウィスコンシン大学の転送量の増加傾向は弱くなり、2003年11月からは減少傾向に転じることとなった。

なお、これらの事件の詳細は、2003年[8月21日](../Page/8月21日.md "wikilink")に、ウィスコンシン大学のDave Plonkaによりまとめられている\[24\]。

他に、[FreeBSD](../Page/FreeBSD.md "wikilink")の有力開発者であるPoul-Henning Kamp(phk)が発見した[D-link製ルータの問題や](https://ja.wikipedia.org/wiki/Dリンク "wikilink")、ダブリンのTardis and Trinity Collegeの問題など、同様の問題が発生している。を参照のこと。

## 参考

<div class="references-small">

<references />

</div>

## 注釈

<div class="references-small">

<references group="注釈" />

</div>

## 関連RFC

  - RFC 1128
  - RFC 1129
  - RFC 1305
  - RFC 2030
  - RFC 4330
  - RFC 5905
  - RFC 5906
  - RFC 5907
  - RFC 5908
  - RFC 8633
  - RFC 868 - Time Protocol （NTPが登場する前の古典的な時刻同期プロトコル）

## 関連項目

  - [:en:NTP server misuse and abuse](https://ja.wikipedia.org/wiki/:en:NTP_server_misuse_and_abuse "wikilink")
  - [ntpd](https://ja.wikipedia.org/wiki/Nptd "wikilink")
  - [OpenNTPD](../Page/OpenNTPD.md "wikilink")
  - [Precision Time Protocol](https://ja.wikipedia.org/wiki/Precision_Time_Protocol "wikilink")

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

1.  RFC1700のWELL KNOWN PORT NUMBERSではTCPとUDPの2つが指定されているが、NTPの規格を示したRFC1305ではUDPのみとなっている。
2.  [NTP.ORG - What is NTP (Network Time Protocol) ?](http://support.ntp.org/bin/view/Main/WebHome#What_is_NTP_Network_Time_Protoco)
3.  ただし、不正確・不安定な信頼性の低い時刻源と直結していても、stratum 1を名乗ることはできる。
4.  定量ではあるが計測が難しい
5.  したがってこの項でNTPサーバとよんでいるプログラムは、サービスを提供しているという意味であり、通常のネットワークのサーバ・クライアントモデルからいうとNTPクライアントにあたる場合もある。
6.  [日本標準時プロジェクト　公開NTP FAQ ［Q.1-2］ ホスト名ではなく、IPアドレスで設定しても良いですか？](http://www2.nict.go.jp/aeri/sts/tsp/PubNtp/qa.html#q1-2)
7.  もし[ルーター](../Page/ルーター.md "wikilink")などで提供できなければ、NTPサービス提供専用の古い[パソコンをセットアップしても良いし](../Page/パーソナルコンピュータ.md "wikilink")、またサーバ的な存在になっている既存のパソコン等にNTPサーバをインストールしても良い
8.  [RFC 4330](https://tools.ietf.org/html/rfc4330) 3. NTP Timestamp Format
9.  [Linux](../Page/Linux.md "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink")等UNIXライクなOSも含む
10.
11.
12.
13. [NTPとWindows時刻同期サービス － ＠IT](http://www.atmarkit.co.jp/fwin2k/operation/winntp201/winntp201_02.html)
14. [Meinberg NTP Software Downloads](http://www.meinbergglobal.com/english/sw/ntp.htm)
15. 特にルーターや[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")
16. 日経NETWORK 2006年8月号 「NICTの標準時刻配信サービス」p68
17. 前述の「桜時計」もそのひとつである。
18. [福岡大のNTPサーバがアクセス集中で悲鳴](http://www.itmedia.co.jp/news/articles/0501/21/news059.html) - ITmediaニュース 2005年01月21日（2014年4月20日閲覧）
19. [公開NTPサーバーの運用と課題](http://enog.jp/wp-content/uploads/2017/10/20171027_ENOG47_tanizaki.pdf) 2017/12/27閲覧
20. [＜更新＞TP-Link製無線LAN中継器によるNTPサーバーへのアクセスに関して](http://www.tp-link.jp/news-details-17792.html) 2017/12/27閲覧
21.
22.  福岡大学情報基盤センター|url=[https://www.ipc.fukuoka-u.ac.jp/service/ntp/public_ntp/|website=www.ipc.fukuoka-u.ac.jp|accessdate=2019-03-27](https://www.ipc.fukuoka-u.ac.jp/service/ntp/public_ntp/%7Cwebsite=www.ipc.fukuoka-u.ac.jp%7Caccessdate=2019-03-27)}}
23. 異常値のようなピーク時で毎秒8万パケット
24.