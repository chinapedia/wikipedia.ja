> この記事は[Tor](https://ja.wikipedia.org/wiki/Tor)から翻訳されています。


**Tor**（トーア、）とは、[TCP/IPにおける接続経路の](../Page/インターネット・プロトコル・スイート.md "wikilink")[匿名](../Page/匿名.md "wikilink")化を実現するための[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")、及びその[リファレンス実装](../Page/リファレンス実装.md "wikilink")である[ソフトウェア](../Page/ソフトウェア.md "wikilink")の名称である。通常、ユーザはローカルに[SOCKS](https://ja.wikipedia.org/wiki/SOCKS "wikilink")[プロキシ](../Page/プロキシ.md "wikilink")（オニオンプロキシ）を立て、そのプロキシ経由で通信を行うことになる。Torという名称はオリジナルのソフトウェア開発プロジェクトの名称である「The Onion Router」の頭文字を取ったものである。

当初は[オニオンルーティング](https://ja.wikipedia.org/wiki/オニオンルーティング "wikilink")の開発元でもある、[アメリカ海軍調査研究所](../Page/アメリカ海軍調査研究所.md "wikilink") によって支援されていたが\[1\]、[2004年](../Page/2004年.md "wikilink")以降は[電子フロンティア財団](../Page/電子フロンティア財団.md "wikilink") (Electronic Frontier Foundation) により支援されるプロジェクトとなった。[2005年](../Page/2005年.md "wikilink")11月以降\[2\]はEFFによる金銭の支援は終了した。ウェブホスティングは継続されている。

## 概要

Torは主として接続経路を匿名化するものであり、通信内容の秘匿を保証するものではない。Torでは経路の中間に限り[暗号](../Page/暗号.md "wikilink")化を行っているが、経路の末端では暗号化が行われていない。通信内容の秘匿まで行いたい場合は、[TLSなど](../Page/Transport_Layer_Security.md "wikilink")（[HTTPS](../Page/HTTPS.md "wikilink")や[SMTP over SSLなど](https://ja.wikipedia.org/wiki/SMTPS "wikilink")）を用いて、別途暗号化を行う必要がある。しかし、Torの隠し機能として後述の [Hidden Service](https://ja.wikipedia.org/wiki/#ランデブーポイントと秘匿サービス（Hidden_Service） "wikilink") というTorサーキット上でサービスをホストする機能があり、これを用いれば末端の通信も暗号化される。

Torのリファレンス実装は、[Microsoft Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](../Page/Linux.md "wikilink")等の各種[Unix系](../Page/Unix系.md "wikilink")[OSで動作する](../Page/オペレーティングシステム.md "wikilink")。「オニオンルーティング」と呼ばれる[多重化](../Page/多重化.md "wikilink")接続により、通信を複数の[ノードを経由させることにより](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")、匿名性を高めている。暗号化が、「あたかも[タマネギ](../Page/タマネギ.md "wikilink")の皮のように、1ホップごとに積み重ねられること」が名前の由来である。現実装では[TCPで通信が可能だが](../Page/Transmission_Control_Protocol.md "wikilink")、[UDPや](../Page/User_Datagram_Protocol.md "wikilink")[ICMP](https://ja.wikipedia.org/wiki/ICMP "wikilink")などの[プロトコル](../Page/プロトコル.md "wikilink")は使用することができない。

通信を秘匿するにあたって、まずTorは各ノード間に回線を構築する。このとき、ユーザは各ノードと共通鍵を共有する。この鍵はユーザと1つ1つのノードのみが共有している。回線構築後は、この回線を使って通信を行う。データは先述の共通鍵を使って暗号化されるが、このとき、データは終端ノードから順番に暗号化される。ユーザはこのデータを構築した回線に渡し、各ノードは共通鍵を用いて、1枚ずつ暗号化の層を剥いでいく。こうすることで、終端ノード以外はデータの内容を読み取ることができなくなる。

## Torのデザイン

接続元がオニオンプロキシ (OP) を立て、オニオンルータ（OR、ノード）経由で本来の宛先へ接続する\[3\]。OPはユーザの複数のTCPストリームを受け取り、それらを多重化、ORがそれらを宛先までリレーする。

それぞれのORは、長期のidキーと、短期のオニオンキーを維持している。前者はルータディスクリプタに署名するのに、後者は回線を構築する際や、別の短期のキーを作るときのリクエストを復号するのに使われる。短期のキーは漏洩したときの影響を小さくするため、一定期間ごとに交換されている。関連項目の[オニオンルーティング](https://ja.wikipedia.org/wiki/オニオンルーティング "wikilink")も参照。

### セル

セルとは、TLS 接続を流れるデータの単位で、512バイト\[4\]。ヘッダとペイロードを持ち、ヘッダに回線id (circID) が含まれる。これは、単一の TLS 接続で、複数の回線を多重化できるため、回線を特定するための識別子である。

セルはコントロールセルとリレーセルの2種類があり、前者は受け取ったノードによって処理されるコマンドを伝達し、後者は接続元から宛先へのデータの受け渡しに使われる。リレーセルは、circID の他に、streamID、チェックサム、リレーコマンド等を持つ。リレーセルのヘッダとペイロードの全ては、暗号化されて送信される。

### 回線の構築

以下は、TorクライアントAlice（発信元）から、オニオンルータBob、Carolまでの回線を構築する際の説明である\[5\]。

  - Aliceは、あらかじめ得ているディレクトリリストの中から、無作為的にBobとCarolを選択する（[実際は最初のノードは2、3ヶ月同じ](https://support.torproject.org/en-US/tbb/tbb-2/)）。
  - Alice→Bob: Alice は create cell（セルに回線構築要求コマンドを乗せたもの）を送信し、回線構築の要求を行う
      - このとき、Alice は今までに使われていない circID \(C_{AB}\) を発行する
      - ペイロードは **Bob のオニオンキーで**暗号化された、DH ハーフハンドシェイクを含んでいる (\(g^x\))
  - Bob→Alice: Bob は created cell（セルに構築完了を通知するためのコマンドを乗せたもの）の中に \(g^y\) と共通鍵 \(K = g^{xy}\) のハッシュを積んで送る
      - AliceとBobは共通鍵 \(K_1 = g^{x1y1}\) を共有できた
      - 以降、Alice-Bob間の通信はこの共通鍵で暗号化されて行われる

<!-- end list -->

  - Alice→Bob: Alice は relay extend cell（セルにサーキットを延長する要求を乗せたもの）を送信する
      - この中に次の OR (Carol) のアドレスが含まれており、**Carol のオニオンキーで**暗号化された \(g^{x2}\) も含まれる
  - Bob→Carol: Bob はハーフハンドシェイクを create cell に入れ、Carolに送信する
      - このとき、Bob は今までに使われていない circID \(C_{BC}\) を発行する
  - Carol→Bob: created cell に共通鍵のハッシュを積んで送る
      - **Bob は \(C_{AB}\) と \(C_{BC}\) を対応付けている**
  - Bob→Alice: Carol が created cell を返した場合、ペイロードを relay extended cell に入れて Alice に返す
      - Alice と Carol は共通鍵 \(K_2 = g^{x2y2}\) を共有できた

以上の手続きは一方向エンティティ認証、すなわち、Alice は Bob を知っているが、Alice は公開鍵を使っていないので、Bob は Alice が誰なのか知らないということを達成している。一方向鍵認証も達成しており、Alice と Bob は鍵について合意しており、Alice は Bob のみがその鍵を知っていることを知っていることを意味している。前方秘匿性とキーの新鮮さの保持にも成功していて、これにより、鍵共有プロトコルでセッションキーを生成した際に、のちに秘密鍵の安全性が破れたとしてもセッションキーの安全性が保たれることが保証される。

Alice-Bob間、Bob-Carol間の共通鍵はそれぞれAliceとBob、BobとCarolしか知らないので、データを盗聴されることなく、中継により匿名性を得ることができる。

セッション鍵交換のために[Diffie-Hellman鍵交換方式が用いられ](../Page/ディフィー・ヘルマン鍵共有.md "wikilink")、通信の暗号化としては[AESが使用される](../Page/Advanced_Encryption_Standard.md "wikilink")。オニオンサーキット構築を含めたTorノード間の全通信は、外部からの盗聴や改竄を防ぐために、[TLSによる通信の上で行われる](../Page/Transport_Layer_Security.md "wikilink")。

### データの送受信

先述の、リレーセルや回線を用いて行われる。以下は、Alice のデータが Bob、Carol を経由して、Dave まで届く様子を説明したものである\[6\]。

[Alice から Bob から Carol から Dave へ](https://ja.wikipedia.org/wiki/File:A2b2c2d.png "fig:Alice から Bob から Carol から Dave へ")

  - Alice はペイロードやペイロードのダイジェストをリレーセルに入れ、circID 以外の全てを終端ノードから順番に、共通鍵を用いて暗号化して送信する
  - Bob は1つ復号し、ダイジェストが一致**しない**場合、Bob は circID を置き換えて、Carol へセルを送信する
  - Carol も同じように1つ復号し、ダイジェストが一致**した**場合、かつ relay cell の内容を認識可能なら、Dave へ送信する (送信完了)
      - Carol に到着したペイロードとそのダイジェストが一致しなかった場合、回線そのものを切断する

[Tor_A2b.png](https://ja.wikipedia.org/wiki/File:Tor_A2b.png "fig:Tor_A2b.png") [Tor_B2c.png](https://ja.wikipedia.org/wiki/File:Tor_B2c.png "fig:Tor_B2c.png")

逆に Dave が送信し、Alice が受信する場合、各ノードは自分にセルが回ってきたときに、ペイロードを暗号化していく。

### ランデブーポイントと秘匿サービス（Hidden Service）

Torの特徴として、身元を明かさずに各種 TCP のサービス（[Webサーバ](../Page/Webサーバ.md "wikilink")、[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")、[IRCサーバなど](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")）を運用することが可能である。 これは、.onionの識別子を持つ、特殊な疑似アドレスを持たせることにより、特定の[IPアドレス](../Page/IPアドレス.md "wikilink")と結びつけることなく、Torを実行させているノード同士が接続することができる。一般のWebサイト等にTor経由で接続するのとは異なり、Hidden Serviceは[深層Web](https://ja.wikipedia.org/wiki/深層Web "wikilink")の一角を成す[ダークネット](https://ja.wikipedia.org/wiki/ダークネット "wikilink")に含まれ**出口ノードは存在しない**し、**中継ノードが通信の内容を見ることは不可能**である。

Alice を接続元、Bob を宛先とすると、このサービスを用いることで、Bob は自身のIPアドレスをさらすことなくサービスを提供でき、アプリケーションもTorの存在を透過的に扱うことができる。

サーバのBobはまず、複数のORを introduction point として指名し、ルックアップサービスへ広告する\[7\]。このとき、Bobは長期の公開鍵暗号のペアを持っており、これでサービスを証明する。先ほどの広告も、Bobの公開鍵で署名されている。Bobは introduction points までの回線を開き、リクエストを待つように伝える。

[Hs1.png](https://ja.wikipedia.org/wiki/File:Hs1.png "fig:Hs1.png")

AliceはBobのサービスを知ると（ネットや直接Bobに聞いて）、ルックアップサービスから情報を得る。Alice はある OR を rendezvous point (RP) として指名し、回線を構築する。この際、Bob を識別するためにランダムな rendezvous cookie も渡す。

[Hs2.png](https://ja.wikipedia.org/wiki/File:Hs2.png "fig:Hs2.png")

次に、Alice は Bob の introduction points の1つに匿名でストリームを開く。このとき、AliceはBob の公開鍵で暗号化した RP の情報と rendezvous cookie を渡し、DH 鍵共有を始める。introduction point は Bob へそのメッセージを送る。

[Hs3.png](https://ja.wikipedia.org/wiki/File:Hs3.png "fig:Hs3.png")

Bob は了承すると Alice の RP への回線を構築し、rendezvous cookie、DH 鍵共有の返答、セッション鍵のハッシュを送る。Alice のRP は Alice の回線を Bob の回線に接続する。

[Hs4.png](https://ja.wikipedia.org/wiki/File:Hs4.png "fig:Hs4.png")

以上の手続きにおいて、RP は Alice も Bob も知らないし、データの内容も知ることはない。両端は双方のOPになっているので、AliceとBob以外の中継ノードがデータの内容を復号することもできない。

Bobのintroduction pointは複数存在しているので、DoS対策にもなっている。さらに、Alice が introduction point へメッセージを送信するとき、end-to-end の認証トークンも乗せることができる。秘匿サービスの仮想ドメイン、x.y.onion は、xが認証トークン、yがBobの公開鍵のハッシュになっている\[8\]。

## エントリーガード

現在、Torの回線は3つのノードを経由しているが、悪意のある攻撃者が両端のノードをコントロールできた場合、匿名性が破られてしまう\[9\]。そのため、Torは2、3ヶ月の間最初のノードを使い続けることで、攻撃のコストを上げており、このノードはエントリーガードと呼ばれる\[10\]。

## Torの応用

[政府機関](../Page/政府機関.md "wikilink")や[軍隊](../Page/軍隊.md "wikilink")が[安全な通信を行うため](../Page/セキュア通信.md "wikilink")、あるいは[通信の秘密](../Page/通信の秘密.md "wikilink")や[プライバシー](../Page/プライバシー.md "wikilink")を重視する個人や活動家などが[ネット検閲](../Page/ネット検閲.md "wikilink")回避のため使用する。使用例については、[ダークネット\#使用](https://ja.wikipedia.org/wiki/ダークネット#使用 "wikilink")の項が詳しい。下記は、公式サイトから入手する必要あり。ただし、[国際的監視網](https://ja.wikipedia.org/wiki/国際的監視網 "wikilink")の形成や[PRISMの導入が行われ](https://ja.wikipedia.org/wiki/PRISM_\(監視プログラム\) "wikilink")、[情報機関](../Page/情報機関.md "wikilink")や[治安当局に](../Page/公安警察.md "wikilink")[把握される可能性があり](https://ja.wikipedia.org/wiki/#サイト管理者へのTor規制要請 "wikilink")、公式サイトの閲覧やブラウザ等の入手・使用は[自己責任](https://ja.wikipedia.org/wiki/自己責任 "wikilink")かつ工夫の上行うこと。また、個人サイトや[アップローダー](../Page/アップローダー.md "wikilink")など第三者によって公開されているものは、[改竄や](https://ja.wikipedia.org/wiki/改竄#ITと改竄 "wikilink")[マルウェア](../Page/マルウェア.md "wikilink")などの混入の可能性がある。

### Torブラウザ

[Tor-9.png](https://ja.wikipedia.org/wiki/File:Tor-9.png "fig:Tor-9.png")（[Linux](../Page/Linux.md "wikilink")）上で動作するTor Browser 9.0。about:torページが表示された起動時の状態。|200px\]\]

\[11\]\[12\]は、[盗聴](../Page/盗聴.md "wikilink")防止や[プライバシー](../Page/プライバシー.md "wikilink")保護を目的に開発された[WEBブラウザである](../Page/ウェブブラウザ.md "wikilink")。設定済みのTorと[Mozilla Firefox ESR（延長サポート版）を組み合わせ](https://ja.wikipedia.org/wiki/Mozilla_Firefox#リリースサイクル "wikilink")、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](../Page/Linux.md "wikilink")の各環境で動作するものがあり、ver 4.5までは[Startpage.com](https://ja.wikipedia.org/wiki/Startpage.com "wikilink")、現在は[DuckDuckGo](https://ja.wikipedia.org/wiki/DuckDuckGo "wikilink")が標準[検索エンジン](../Page/検索エンジン.md "wikilink")に採用されている。さらにいくつかの[拡張機能](../Page/拡張機能_\(Mozilla\).md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")を制御でき[XSSにも対応可能な](../Page/クロスサイトスクリプティング.md "wikilink")[NoScript](../Page/NoScript.md "wikilink")のほか、[Hidden Service（.onionドメイン）以外の](https://ja.wikipedia.org/wiki/#ランデブーポイントと秘匿サービス（Hidden_Service） "wikilink")[HTTP](https://ja.wikipedia.org/wiki/HTTP "wikilink")通信で出口[ノードからの末端部を](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")[暗号化する](../Page/HTTPS.md "wikilink")[HTTPS Everywhere](../Page/HTTPS_Everywhere.md "wikilink")\[13\]\[14\]などが標準で組み込まれている。[Tailsに搭載されるものには](https://ja.wikipedia.org/wiki/Tails_\(オペレーティングシステム\) "wikilink")、[インターネット広告](https://ja.wikipedia.org/wiki/インターネット広告 "wikilink")の[遮断などに用いられる](https://ja.wikipedia.org/wiki/アドブロック "wikilink")[uBlock Originも含む](https://ja.wikipedia.org/wiki/uBlock_Origin "wikilink")。Torブラウザは常時[プライベートブラウシングモードで動作し](https://ja.wikipedia.org/wiki/プライバシーモード "wikilink")、終了時に[履歴や](../Page/データログ.md "wikilink")[キャッシュおよび](../Page/キャッシュ_\(コンピュータシステム\).md "wikilink")[cookie等も残さない](../Page/HTTP_cookie.md "wikilink")。いまのところ、やなどの[対策にも有効である](https://ja.wikipedia.org/wiki/#匿名性を低下、又はユーザーを危険に晒す迂回サービスの存在 "wikilink")\[15\]。また、[Android端末向けや](../Page/Android_\(オペレーティングシステム\).md "wikilink")、[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")に入れての利用を想定したゼロインストールパッケージも用意されている。

### TorBirdy

\[16\]\[17\]\[18\]は、Microsoft Windows、macOS、Linuxの各環境で動作する[インターネット統合ソフト](../Page/インターネットスイート.md "wikilink")・[SeaMonkey](../Page/SeaMonkey.md "wikilink")および[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")・[Mozilla Thunderbird用の](../Page/Mozilla_Thunderbird.md "wikilink")[拡張機能](../Page/拡張機能_\(Mozilla\).md "wikilink")。[電子メール](../Page/電子メール.md "wikilink")の盗聴や[傍受](https://ja.wikipedia.org/wiki/傍受 "wikilink")の防止を目的に開発されており、メールの[送信経路の秘匿化を行う](https://ja.wikipedia.org/wiki/セキュア通信#匿名ネットワーク "wikilink")。[Torネットワークに接続した状態で動作するため](https://ja.wikipedia.org/wiki/#Torのデザイン "wikilink")、公式には、Torブラウザを起動した状態での使用を推奨している。Tailsでは、メールそのものを[公開鍵で暗号化する](../Page/公開鍵暗号.md "wikilink")[GnuPGや](../Page/GNU_Privacy_Guard.md "wikilink")[Enigmail](https://ja.wikipedia.org/wiki/Enigmail "wikilink")とともに組み込まれている。

### Tails

[Tails](https://ja.wikipedia.org/wiki/Tails_\(オペレーティングシステム\) "wikilink")\[19\]\[20\]はプライバシー保護を重視した[Linux](../Page/Linux.md "wikilink")系[OSで](../Page/オペレーティングシステム.md "wikilink")、TorブラウザやTorBirdyなども標準搭載し、通信はすべてTorネットワーク経由となる。[Live DVDや](../Page/Live_CD.md "wikilink")[Live USBから起動し](https://ja.wikipedia.org/wiki/Live_USB "wikilink")、さらに[PCに](../Page/パーソナルコンピュータ.md "wikilink")[履歴を一切残さない](../Page/データログ.md "wikilink")。匿名性・秘匿性が高く、[人権活動家](https://ja.wikipedia.org/wiki/人権活動家 "wikilink")や[弁護士](../Page/弁護士.md "wikilink")、[ジャーナリスト](../Page/ジャーナリスト.md "wikilink")および[各国の工作員なども使用する](../Page/スパイ.md "wikilink")。公式サイトやTails公式アーカイブで[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")が無償配布されており手軽に入手可能である。

### Orbot

[Orbot](https://ja.wikipedia.org/wiki/Orbot "wikilink")\[21\]\[22\]は[Androidユーザー向け](../Page/Android_\(オペレーティングシステム\).md "wikilink")[匿名](../Page/匿名.md "wikilink")ネットワーククライアント。

## 問題点

### 通信傍受

[2007年](../Page/2007年.md "wikilink")8月30日、スウェーデンのセキュリティー研究者、ダン・エガースタッド (Dan Egerstad) は、「世界中の大使館や人権擁護団体の電子メールを傍受することに成功した」と発表した\[23\]。

Torノード間の通信は暗号化されているものの、末端（出口）となるTorノードと通常のTCP通信先との間では、その暗号化が解除されるという点を利用したもので、[LANアナライザ](../Page/LANアナライザ.md "wikilink")を搭載したTorノードを設置することで、そこからTorネットワークを抜けようとする通信を監視するだけで、簡単に傍受できてしまうというものである。

この問題はTorネットワークに対して送信するデータ自体を、たとえば[HTTPS](../Page/HTTPS.md "wikilink")や[SMTP over SSLなどを用いて別途暗号化することで](https://ja.wikipedia.org/wiki/SMTPS "wikilink")、防ぐことができる。Torブラウザには、標準で[HTTPS Everywhereが添付される](../Page/HTTPS_Everywhere.md "wikilink")。

### DNS漏洩

ほとんどのソフトウェアは、[UDPを用いて](../Page/User_Datagram_Protocol.md "wikilink")[DNSを参照するため](../Page/Domain_Name_System.md "wikilink")、TCP専用であるTorネットワークを経由せず直接参照してしまい、匿名性が不完全になる可能性がある。

DNS規格自体はUDPとTCPの両方をサポート (RFC 2136) しており、多くのDNSサーバー実装も両対応となっているが、DNSを参照する多くのソフトウェアではUDPを用いるのが一般的であるという事が問題の根底にある。TCPを用いたDNS参照をサポートしているソフトウェアであれば、この問題の影響を受けることはない。

以上のことより、古いバージョンのTorでは、HTTP通信を行う場合に、TCPを用いたDNS参照をサポートしている[Privoxy](https://ja.wikipedia.org/wiki/Privoxy "wikilink")をWebブラウザとTorの間に設置し、併用することが推奨されていた。

バージョン0.2.0.1-alpha以降のTorは、DNS参照をTorネットワーク経由で行うDNSリゾルバが搭載された。これを使用するには、ユーザはシステム上の任意のDNSリクエストを、指定したポートで動作するTorのDNSリゾルバ経由で処理させるよう、リダイレクトする必要がある (iptables 等を用いて)。こうすることでDNS漏洩問題は解決され、SOCKSに非対応のアプリケーションでも安全にTor経由の通信を行うことができるようになるが、少々設定が複雑で、パケットがリークする可能性があるため、**安易に使うべきではない**\[24\]。

代替案として、公式のFAQでは、以下のSOCKSベースの解決策が挙げられている\[25\]:

  - SOCKS 4a （ホスト名を使う）を用いる
  - SOCKS ベースのポートフォワーダ（socat 等）を用いて、SOCKS 経由で通信させる
  - tor-resolve を用いて、Tor経由でホスト名を解決。その後、アプリケーションに解決されたIPアドレスを渡す

### トラフィック分析

[2005年](../Page/2005年.md "wikilink")5月8日から11日にかけて米国カリフォルニア州オークランドで開催された2005 IEEE Symposium on Security and Privacy で、ケンブリッジ大学の Steven J. MurdochとGeorge Danezis は論文「Low-Cost Traffic Analysis of Tor」を提示した。この論文によると、Torの匿名性を大幅に低下させる手法が存在する。当該論文はDanezis自身のページ\[26\]ないし IEEE Computer Society digital library などで閲覧可能である。

### 匿名性を低下、又はユーザーを危険に晒す迂回サービスの存在

本来、[Hidden Service（.onionドメイン）は自身もTorネットワークに接続することでしか閲覧できず](https://ja.wikipedia.org/wiki/tor#ランデブーポイントと秘匿サービス（Hidden_Service） "wikilink")、技術/知識を持ち意識をしてアクセスを行うべきサイト群である。前述の通り、.onionドメインは一般的に[アングラに属する情報が多く集まるが](https://ja.wikipedia.org/wiki/アンダーグラウンド_\(文化\)#インターネット "wikilink")、これらのサイトに対し、迂回サービスを利用することによって誰もが場所を問わず通常のブラウザ経由でそのまま気軽に検索、閲覧することが可能な状況が発生している。

この状況を逆手に取り、悪意のある[JavaScript](../Page/JavaScript.md "wikilink")を仕込むサイトなどの登場が危惧される。また、目立たない画像を仕込まれされる場合もある。関連する項目の、[ウェブビーコン](../Page/ウェブビーコン.md "wikilink")や[HTTP cookie\#トラッキング・クッキーも参照](https://ja.wikipedia.org/wiki/HTTP_cookie#トラッキング・クッキー "wikilink")。.onionドメインのサイト群の中には、[悪意ある者や犯罪者およびテロリストなどが関わるサイトも存在するため](https://ja.wikipedia.org/wiki/#秘匿サービスの問題点 "wikilink")、常に[情報機関](../Page/情報機関.md "wikilink")や[治安当局の](../Page/公安警察.md "wikilink")[工作員も](../Page/スパイ.md "wikilink")[監視しており](../Page/ネット検閲.md "wikilink")、興味本位で安易に接続するのは非常に高い危険性をともなう。

通常、[Mozilla Firefoxから派生したTorブラウザは](../Page/Mozilla_Firefox.md "wikilink")[XSSなどに対応する](../Page/クロスサイトスクリプティング.md "wikilink")[NoScript](../Page/NoScript.md "wikilink")が標準でインストールされており、JavaScriptがOFF、もしくはOFFにするべき状況のため影響を受ける可能性は低く、逆に知識のない一般人が通常のブラウザで安易に接続し被害に遭う可能性がある。[Google Chrome系ブラウザで接続する場合](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、JavaScriptを制御できる[ScriptSafe](https://ja.wikipedia.org/wiki/ScriptSafe "wikilink")\[27\]のほかトラッキングや対策の[拡張機能も必要である](https://ja.wikipedia.org/wiki/ブラウザ拡張機能 "wikilink")。

### 秘匿サービスの問題点

[2000年](../Page/2000年.md "wikilink")代後半より、ブラックビジネスの基盤としても利用され始め、Tor経由でしかアクセス出来ない秘匿された違法サービスが多数運営されていることが確認されている。[ダークネット・マーケット](https://ja.wikipedia.org/wiki/ダークネット・マーケット "wikilink")で取り扱うサービスは武器・麻薬・ギャンブル・偽造通貨などである。サーバの存在が秘匿された違法サイトが運営されているウェブの領域は、[ダークウェブ](https://ja.wikipedia.org/wiki/ダークウェブ "wikilink")と呼ばれており、特定の違法サイトの摘発と新たな違法サイトの展開といういたちごっこが続いている。

攻撃者がTorを使って攻撃を仕掛けた場合、被害者側のログに出口ノードを運営するボランティアとの通信が記録される。そのため、運営するだけで逮捕されかねないようなリスクを負うことになる。公式もこのことを問題視しており、ボランティアはExit Policyを設定することで、出口ノードになるかどうか、出口ノードとしてどのサービスを許可するか、等を制限することができる\[28\]。

## サイト管理者へのTor規制要請

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")で[2012年](../Page/2012年.md "wikilink")に[パソコン遠隔操作事件](https://ja.wikipedia.org/wiki/パソコン遠隔操作事件 "wikilink")が発生してTorの存在がマスコミにより連日報道された。近年はTorを悪用した犯罪行為が発生しており、[殺人予告や](https://ja.wikipedia.org/wiki/犯罪予告 "wikilink")[オンラインバンキング](https://ja.wikipedia.org/wiki/オンラインバンキング "wikilink")等への[不正アクセス](https://ja.wikipedia.org/wiki/不正アクセス "wikilink")、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")の[警視庁国際テロ捜査情報流出事件](https://ja.wikipedia.org/wiki/警視庁国際テロ捜査情報流出事件 "wikilink")でも使用が確認されている\[29\]。

[警察庁](https://ja.wikipedia.org/wiki/警察庁 "wikilink")の有識者会議は、[2013年](../Page/2013年.md "wikilink")4月18日の報告書で「国内外で犯罪に使われている状況に鑑みると対策が必要」として、末端となるTorノードの[IPアドレス](../Page/IPアドレス.md "wikilink")からアクセスがあった場合は通信を遮断するよう、国内の[ウェブサイト管理者に自主的な取り組みを要請する構えを見せている](https://ja.wikipedia.org/wiki/ウェブマスター "wikilink")\[30\]\[31\]\[32\]。

2014年7月に「Tor」を管理する非営利団体は、Torのネットワーク上で5か月間にわたり密かにトラフィックに変更を加え、「[秘匿サービス](https://ja.wikipedia.org/wiki/tor#ランデブーポイントと秘匿サービス（Hidden_Service） "wikilink")」と呼ばれるサイトにアクセスしているTorユーザーの身元を探ろうとしていたコンピュータの存在が確認されたとして、秘匿サイトを利用しているTorユーザーの多くが政府が支援する研究者によって身元を特定された可能性があると発表した\[33\]。

国際[ハッカー集団](https://ja.wikipedia.org/wiki/ハッカーグループ "wikilink")「[アノニマス](https://ja.wikipedia.org/wiki/アノニマス_\(集団\) "wikilink")」は、Torの検閲への動きを撤廃することを望む動画を、[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")にアップロードした\[34\]。

## 中国とTorプロジェクトの攻防

[中華人民共和国](../Page/中華人民共和国.md "wikilink")（中国）は、[2009年](../Page/2009年.md "wikilink")9月30日の建国60周年記念式典に併せるかたちで[インターネット検閲](https://ja.wikipedia.org/wiki/インターネット検閲 "wikilink")を強化し、Torを始めとする類似技術を用いた[グレート・ファイアウォール](https://ja.wikipedia.org/wiki/グレート・ファイアウォール "wikilink")（中国の検閲システム）回避を行う者の摘発、Tor公式サイトへのアクセス遮断、Torリレーノードへのアクセス遮断などを強化した\[35\]。

これに対抗するようにTorプロジェクトでは、Torリレーノードとなってくれるボランティアの増強を呼びかけている。たとえ[ISPに規制されても](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、[IPアドレス](../Page/IPアドレス.md "wikilink")が公開されていないTor Brigdeを利用すればこれらの規制を回避することが可能であり、Torへのアクセスが禁止されている[非民主主義的な国内も利用可能である](../Page/独裁政治.md "wikilink")。

## 注・出典

<references />

## 関連項目

  - [Orbot](https://ja.wikipedia.org/wiki/Orbot "wikilink") - [AndroidユーザーがTorに接続することを目指すプロジェクト](../Page/Android_\(オペレーティングシステム\).md "wikilink")
  - [Bitmessage](https://ja.wikipedia.org/wiki/Bitmessage "wikilink")
  - [Tails](https://ja.wikipedia.org/wiki/Tails_\(オペレーティングシステム\) "wikilink")
  - [深層Web](https://ja.wikipedia.org/wiki/深層Web "wikilink") - 通常の[検索エンジン](../Page/検索エンジン.md "wikilink")が収集することができない情報。
      - [ダークネット](https://ja.wikipedia.org/wiki/ダークネット "wikilink") - 深層Webの一部。特殊な環境で接続できる暗号化されたネットワーク。
          - [ダークウェブ](https://ja.wikipedia.org/wiki/ダークウェブ "wikilink") - ダークネットの一部で、[ダークネット・マーケット](https://ja.wikipedia.org/wiki/ダークネット・マーケット "wikilink")をはじめとする[アングラ系](https://ja.wikipedia.org/wiki/アンダーグラウンド_\(文化\)#インターネット "wikilink")。
  - [Ahmia](../Page/Ahmia.md "wikilink") - Torの隠し機能。クリアネット用検索エンジン

## 外部リンク

### 公式

  - [Tor公式サイト](https://www.torproject.org/)
  - [Tor: The Second-Generation Onion Router - Tor のデザイン](https://svn.torproject.org/svn/projects/design-paper/tor-design.pdf)
  - [仕様書](https://gitweb.torproject.org/torspec.git/tree/tor-spec.txt)

### Hidden Serviceの例

Hidden Service（onionドメイン）の接続はTor本体及びSOCKS4aもしくはSOCKS5に対応した[ローカル](../Page/Local_Area_Network.md "wikilink")[プロキシ](../Page/プロキシ.md "wikilink")が必要。

  - [Tor公式サイト群](https://onion.torproject.org)（onionドメイン一覧）
  - [ダークウェブ地図～torの歩き方2020年　リンク集](https://w.atwiki.jp/internetkyogakusys/pages/70.html)（onionドメイン一覧）
  - [DuckDuckGo](http://3g2upl4pq6kufc4m.onion/)
  - [ProtonMail](https://protonirockerxow.onion/)
  - [Facebook](https://www.facebookcorewwwi.onion/)

[Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:ファイル共有ソフト](https://ja.wikipedia.org/wiki/Category:ファイル共有ソフト "wikilink") [Category:匿名ネットワーク](https://ja.wikipedia.org/wiki/Category:匿名ネットワーク "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ダークウェブ](https://ja.wikipedia.org/wiki/Category:ダークウェブ "wikilink")

1.  [米海軍が産み、オープンソース陣営が育てる匿名ネット技術『トーア』](http://wired.jp/wv/archives/2004/08/06/%E7%B1%B3%E6%B5%B7%E8%BB%8D%E3%81%8C%E7%94%A3%E3%81%BF%E3%80%81%E3%82%AA%E3%83%BC%E3%83%97%E3%83%B3%E3%82%BD%E3%83%BC%E3%82%B9%E9%99%A3%E5%96%B6%E3%81%8C%E8%82%B2%E3%81%A6%E3%82%8B%E5%8C%BF%E5%90%8D/)
2.  [Tor: People](http://tor.eff.org/people.html)
3.  <https://svn.torproject.org/svn/projects/design-paper/tor-design.html#tth_sEc4>
4.  <https://svn.torproject.org/svn/projects/design-paper/tor-design.html#tth_sEc4.1>
5.  <https://svn.torproject.org/svn/projects/design-paper/tor-design.html#tth_sEc4.2>
6.  <https://svn.torproject.org/svn/projects/design-paper/tor-design.html#tth_sEc4.2>
7.  <https://svn.torproject.org/svn/projects/design-paper/tor-design.html#tth_sEc5>
8.  <https://svn.torproject.org/svn/projects/design-paper/tor-design.html#tth_sEc5.2>
9.  <https://gnunet.org/sites/default/files/Wright-2004.pdf>
10. <https://support.torproject.org/en-US/tbb/tbb-2/>
11. [Tor Project | Anonymity Online](https://www.torproject.org/)
12. [tor-package-archive torbrowser](https://archive.torproject.org/tor-package-archive/torbrowser/)
13. [HTTPS Everywhere – 🦊 Firefox (ja) 向け拡張機能を入手](https://addons.mozilla.org/ja/firefox/addon/https-everywhere/)
14. [HTTPS Everywhere Electronic Frontier Foundation](https://www.eff.org/https-everywhere)
15. [Fingerprint解説サイト - 明治大学 情報セキュリティ研究室](https://www.saitolab.org/fp_site/)
16. [TorBirdy :: Thunderbird向けアドオン - Thunderbird Add-ons](https://addons.thunderbird.net/ja/thunderbird/addon/torbirdy/)
17. [torbirdy – Tor Bug Tracker & Wiki](https://trac.torproject.org/projects/tor/wiki/torbirdy)
18. [tor-package-archive torbirdy](https://archive.torproject.org/tor-package-archive/torbirdy/)
19. [Tails - Privacy for anyone anywhere](https://tails.boum.org/)
20. [amnesia.boum.org/tails](https://archive.torproject.org/amnesia.boum.org/tails/stable/)
21. [Orbot: Tor for Android](https://guardianproject.info/apps/orbot/)
22. [tor-package-archive android](https://archive.torproject.org/tor-package-archive/android/)
23. [Rogue Nodes Turn Tor Anonymizer Into Eavesdropper's Paradise](http://www.wired.com/politics/security/news/2007/09/embassy_hacks)
24. <https://trac.torproject.org/projects/tor/wiki/doc/TransparentProxy>
25. <https://www.torproject.org/docs/faq.html.en#WarningsAboutSOCKSandDNSInformationLeaks>
26. [Low-cost Traffic Analysis of Tor.](http://www0.cs.ucl.ac.uk/staff/G.Danezis/papers/TorTA.pdf)（pdf）
27. [ScriptSafe - Google Chrome](https://chrome.google.com/webstore/detail/scriptsafe/oiigbmnaadbkfbmpbfijlflahbdbdgdf?hl=ja)
28. <https://svn.torproject.org/svn/projects/design-paper/tor-design.html#tth_sEc6.2>
29.
30.
31.
32.
33. 匿名化ツール「Tor」ユーザーの身元が特定された可能性 ソフト更新を呼びかけ IT MECIA 2014年8月4日
34. [1](https://www.youtube.com/watch?v=ccK4Xa32bQs)
35. [【Bloomberg Businessweek特約】【BusinessWeek特約】中国、建国60周年でネット検閲をさらに強化| nikkei BPnet 〈日経BPネット〉](http://www.nikkeibp.co.jp/article/news/20091007/186877/)