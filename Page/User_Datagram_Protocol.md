> この記事は[User Datagram Protocol](https://ja.wikipedia.org/wiki/User_Datagram_Protocol)から翻訳されています。


**User Datagram Protocol**（ユーザ データグラム プロトコル、**UDP**（ユーディーピー））は、主に[インターネット](../Page/インターネット.md "wikilink")で使用される[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")の中核[プロトコル](../Page/プロトコル.md "wikilink")の一つ。

## 概要

アプリケーションから [Internet Protocol](../Page/Internet_Protocol.md "wikilink") (IP) ネットワーク上の他のホストへ「[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")」と呼ばれるメッセージを送るのに使われ、事前に転送チャネルやデータ経路といった特別な設定をする必要がない。が1980年に設計し、RFC 768 で定義した（[STD番号](../Page/インターネット標準.md "wikilink"): 6）。非常にシンプルに設計されており公式仕様のRFC 768はわずか3ページである。

主に[IPプロトコル上に実装されており](../Page/Internet_Protocol.md "wikilink")[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の[トランスポート層](../Page/トランスポート層.md "wikilink")にあたる。明確な[ハンドシェイク](https://ja.wikipedia.org/wiki/ハンドシェイク "wikilink")を省いた[コネクションレスであり](https://ja.wikipedia.org/wiki/コネクションレス型通信 "wikilink")、送達確認などを行わない言わば無手順方式のデータ転送で、信頼性・順序性・[データ完全性](../Page/データ完全性.md "wikilink")を保証しない。通信中のパケット紛失や重複、改竄の検出やそのための対応が必要な場合はアプリケーションで行う。それによって[トランスポート層](../Page/トランスポート層.md "wikilink")でのそのような処理のオーバーヘッドを削減している。リアルタイム・システムでは遅れているパケットを待つよりもそういうパケットはないものとして処理する方が好ましいため、適時性を重視するアプリケーションでよく使われている\[1\]。トランスポート層での誤り検出機能が必須なら、その用途に設計された [Transmission Control Protocol](../Page/Transmission_Control_Protocol.md "wikilink") (TCP) または [Stream Control Transmission Protocol](../Page/Stream_Control_Transmission_Protocol.md "wikilink") (SCTP) を使えばよい。

UDPは内部状態を持たない「[ステートレス](https://ja.wikipedia.org/wiki/ステートレス・プロトコル "wikilink")」であり、多数のクライアントからの簡単な問い合わせに応えるサーバなどの用途に有効である。[TCPとは異なり](../Page/Transmission_Control_Protocol.md "wikilink")、[ブロードキャスト](../Page/ブロードキャスト.md "wikilink")（ローカル・ネットワーク上の全ホストへの送信）と[マルチキャスト](../Page/マルチキャスト.md "wikilink")（購読者全員への送信）をサポートしている\[2\]。

UDPを使っている主なネットワーク・アプリケーションとしては、途中でデータが抜け落ちても問題が少ない音声や画像の[ストリーム](https://ja.wikipedia.org/wiki/ストリーム "wikilink")形式での配信（[VoIP](../Page/VoIP.md "wikilink")、[MPEG-TS](../Page/MPEG-2システム.md "wikilink")、[Realストリーミング](https://ja.wikipedia.org/wiki/Realストリーミング "wikilink")、[QuickTime](../Page/QuickTime.md "wikilink")ストリーミング、[IP放送](../Page/IP放送.md "wikilink")など）、小さなデータをリアルタイムで大量に転送する[オンラインゲーム](../Page/オンラインゲーム.md "wikilink")などがある。

その他、[SNMP](../Page/Simple_Network_Management_Protocol.md "wikilink")、[TFTP](../Page/Trivial_File_Transfer_Protocol.md "wikilink")、[DNS](../Page/Domain_Name_System.md "wikilink")、[DHCPなどの各種上位プロトコルがある](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink")。

IPヘッダにおける[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")は17である。

## ポート

UDPアプリケーションは[データグラム・ソケットを使ってホスト間の通信を行う](../Page/ソケット_\(BSD\).md "wikilink")。アプリケーションでソケットとデータ転送のエンドポイントを結びつけるのだが、そのエンドポイントは[IPアドレス](../Page/IPアドレス.md "wikilink")とサービスポートの組み合わせで表される。[ポートとはポート番号で識別されるソフトウェア構造であり](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")、ポート番号は16ビット整数値で0から65,535まである。ポート番号0は予約されているが、送信側プロセスが応答を期待していない場合は使うことも許されている。

[Internet Assigned Numbers Authority](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") (IANA) はポート番号を3つの範囲に分割した\[3\]。0から1023まではウェルノウンポートであり、よく知られている一般的サービスが使用する。[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")では、そのうちの一部の使用には[スーパーユーザー](../Page/スーパーユーザー.md "wikilink")の権限を必要とする。1024から49,151まではレジスタードポートであり、IANAが登録したサービスが使用する。49,152から65,535まではダイナミックポートであり、公式には特定サービスに割り当てられておらず、任意の用途で使用可能である。[エフェメラルポート](https://ja.wikipedia.org/wiki/エフェメラルポート "wikilink")としても使用でき、ソフトウェアがランダムに選んで使うことができる\[4\]。一般に、[クライアントが何らかの](../Page/クライアント_\(コンピュータ\).md "wikilink")[サーバ](../Page/サーバ.md "wikilink")と通信する際に一時的ポートとして使用する。

## パケット構造

UDPは最小メッセージ指向の[トランスポート層](../Page/トランスポート層.md "wikilink")プロトコルで、仕様は [IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") RFC 768 にある。

[上位層プロトコル](https://ja.wikipedia.org/wiki/上位層プロトコル "wikilink")へのメッセージ配送を全く保証せず、送信済みのUDPメッセージについて何の状態も保持しない。このため、UDPを *Unreliable Datagram Protocol*（信頼できないデータグラム・プロトコル）と呼ぶこともある\[5\]。

UDPは（ポート番号による）アプリケーション[多重化](../Page/多重化.md "wikilink")と、（[検査合計](https://ja.wikipedia.org/wiki/検査合計 "wikilink")による）ヘッダおよびペイロードの完全性検証を提供する\[6\]。高信頼転送が必要なら、上位アプリケーションが実装しなければならない。

<table>
<thead>
<tr class="header">
<th><p>オフセット（ビット）</p></th>
<th><p>0 – 15</p></th>
<th><p>16 – 31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>送信元ポート番号</p></td>
<td><p>宛先ポート番号</p></td>
</tr>
<tr class="even">
<td><p>32</p></td>
<td><p>データ長</p></td>
<td><p>検査合計</p></td>
</tr>
<tr class="odd">
<td><p>64+</p></td>
<td><p> <br />
データ<br />
 </p></td>
<td></td>
</tr>
</tbody>
</table>

UDPヘッダには4つのフィールドがあり、それぞれ2バイト（16ビット）である\[7\]。そのうち2つ（ピンク色の部分）はIPv4ではオプションである。IPv6では送信元ポート番号だけがオプションである（後述）。

  - 送信元ポート番号
    送信元のポート番号で、相手からの応答が不要の場合はゼロ。それ以外の値の場合、必要なら相手からの応答を受け付けるポート番号を示す。送信元がクライアントの場合、[エフェメラルポート](https://ja.wikipedia.org/wiki/エフェメラルポート "wikilink")番号ということが多い。送信元がサーバの場合、ウェルノウンポート番号ということが多い\[8\]。
  - 宛先ポート番号
    宛先のポート番号であり、必須である。送信元ポート番号と同様、宛先がクライアントならエフェメラルポート、サーバならウェルノウンポートということが多い\[9\]。
  - データ長
    ヘッダとデータを含むデータグラム全体のバイト数を指定する。ヘッダが8バイトなので、それが最小値となる。理論上の上限は65,535バイト（ヘッダ8バイト + データ65,527バイト）である。下位層が[IPv4](../Page/IPv4.md "wikilink")の場合、実際の上限は65,507バイト（IPヘッダ20バイトとUDPヘッダ8バイトを差し引いた値）となる\[10\]。
    [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")のジャンボグラム機能では、65,535バイトを越えるサイズのUDPパケットを扱える\[11\]。この場合、IPv6のオプションヘッダでサイズを指定し、最大4,294,967,295バイト（2<sup>32</sup> - 1）を指定できるので、ヘッダ部の8バイトを差し引くと最大4,294,967,287バイトのデータを扱える。
  - 検査合計
    ヘッダとデータの誤り検出に使用。送信元が検査合計を生成しない場合、このフィールドの値はゼロとする\[12\]。IPv6ではオプションではないので、ゼロにはできない\[13\]。

\[14\]

## 検査合計の計算

検査合計の計算法は RFC 768 で以下のように定義されている。

> IPヘッダからの情報で作られる擬似ヘッダとUDPヘッダとデータを長さが2オクテットの倍数になるように（必要なら）値がゼロのオクテットでパディングし、各2オクテットの1の補数の総和の1の補数の下位16ビットを検査合計とする\[15\]。

つまり、全16ビットワードを1の補数演算で足しあわせる。その合計を1の補数化すればUDPの検査合計・フィールドの値になる。

検査合計計算の結果がゼロになる場合（16ビット全部が0）、検査合計を省略する場合と区別するため、その1の補数（全ビットが1）を設定する。

[IPv4](../Page/IPv4.md "wikilink")と[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")では検査合計計算に使うデータに差異がある。

### IPv4 擬似ヘッダ

IPv4上のUDPでは、実際のIPv4ヘッダからの情報から作った擬似ヘッダを検査合計計算に使用する。擬似ヘッダは実際のIPv4ヘッダそのものではない。以下に検査合計計算にのみ使用する擬似ヘッダを示す。

<table>
<thead>
<tr class="header">
<th><p>bits</p></th>
<th><p>0 – 7</p></th>
<th><p>8 – 15</p></th>
<th><p>16 – 23</p></th>
<th><p>24 – 31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>送信元IPアドレス</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>32</p></td>
<td><p>あて先IPアドレス</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>64</p></td>
<td><p>ゼロ</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/プロトコル番号" title="wikilink">プロトコル番号</a></p></td>
<td><p>UDP長</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>96</p></td>
<td><p>送信元ポート番号</p></td>
<td><p>宛先ポート番号</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>128</p></td>
<td><p>データ長</p></td>
<td><p>検査合計</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>160+</p></td>
<td><p> <br />
データ<br />
 </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

送信元IPアドレスとあて先IPアドレスはIPv4ヘッダにある値である。[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")はUDPを表すので17 (0x11) である。UDP長フィールドはUDPのヘッダとデータの全長である。

UDP検査合計計算はIPv4ではオプションである。検査合計を使わない場合はゼロを設定する。

### IPv6 擬似ヘッダ

IPv6上のUDPでは、検査合計は基本的に必須である。ただしUDP上でトンネリングプロトコルを利用する場合は例外的に計算を省略しゼロに設定して良い\[16\]。検査合計の計算法は RFC 2460 で次のように文書化されている。

> トランスポート層かそれより上位のプロトコルで、IPヘッダ内のアドレスを検査合計計算に使う場合、IPv6では128ビットのIPv6のアドレスを使用する\[17\]。

検査合計計算では、実際のIPv6ヘッダを真似た次のような擬似ヘッダを用いる。

<table>
<thead>
<tr class="header">
<th><p>bits</p></th>
<th><p>0 – 7</p></th>
<th><p>8 – 15</p></th>
<th><p>16 – 23</p></th>
<th><p>24 – 31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>送信元IPアドレス</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>32</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>64</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>96</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>128</p></td>
<td><p>あて先IPアドレス</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>160</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>192</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>224</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>256</p></td>
<td><p>UDP長</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>288</p></td>
<td><p>ゼロ</p></td>
<td><p>次のヘッダ</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>320</p></td>
<td><p>送信元ポート番号</p></td>
<td><p>宛先ポート番号</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>352</p></td>
<td><p>データ長</p></td>
<td><p>検査合計</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>384+</p></td>
<td><p> <br />
データ<br />
 </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

送信元IPアドレスはIPv6ヘッダにある値を使う。あて先IPアドレスは最終的なあて先であり、IPv6パケットにルーティングヘッダがなければIPv6ヘッダ内のあて先IPアドレスを使い、さもなくば送信側ではルーティングヘッダの最後の要素を、受信側ではIPv6ヘッダのあて先IPアドレスを使う。次のヘッダというフィールドは[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")を意味し、UDPなので17を指定する。UDP長フィールドはUDPのヘッダとデータを合わせた長さである。

## 信頼性と輻輳制御の実現

UDPアプリケーションはパケットの喪失、誤りが起こることを想定しなければならない。[TFTPなどのアプリケーションでは](../Page/Trivial_File_Transfer_Protocol.md "wikilink")、アプリケーション層で必要に応じて基本的な信頼性機構を付与している\[18\]。

多くの場合、UDPアプリケーションは信頼性機構を持たず、むしろそのオーバーヘッドを嫌っている。[ストリーミング](../Page/ストリーミング.md "wikilink")、リアルタイムのオンラインゲーム、[VoIP](../Page/VoIP.md "wikilink")といった用途ではUDPを使うことが多く、パケット喪失は大きな問題とはならない。高信頼性が求められる用途では、[Transmission Control Protocol](../Page/Transmission_Control_Protocol.md "wikilink") などのプロトコルやを代わりに使う。

より深刻なのは、TCPとは異なり、UDPアプリケーションでは[輻輳を回避](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")・制御する機構を持たないことがある点である。帯域の大きな部分を消費して輻輳を起こしやすいUDPアプリケーションは、インターネットの安定性を危険にさらす可能性があり、実際に帯域を大幅に占める事態が発生している。制御できないUDPトラフィックによって輻輳崩壊になる可能性を低減するためのネットワーク機構が提案されてきた。現状では、[ルーター](../Page/ルーター.md "wikilink")などのネットワーク機器でのパケット・キューイングやパケット・ドロッピングが過度なUDPトラフィックをスローダウンさせる唯一の手段となっている。[Datagram Congestion Control Protocol](../Page/Datagram_Congestion_Control_Protocol.md "wikilink") (DCCP) はこの問題を部分的に解決すべく設計されたプロトコルで、ストリーミングなどの高転送レートのUDPストリームに対してTCPのような輻輳制御を追加するものである。

## 用途

UDPを利用するインターネットの重要なアプリケーションはいくつもある。例えば [Domain Name System](../Page/Domain_Name_System.md "wikilink") (DNS) は、1つのクエリに素早く1つの応答パケットを返すだけなのでUDPを使用している。他にも [Simple Network Management Protocol](../Page/Simple_Network_Management_Protocol.md "wikilink") (SNMP)、[Routing Information Protocol](../Page/Routing_Information_Protocol.md "wikilink") (RIP)\[19\]、[Dynamic Host Configuration Protocol](https://ja.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "wikilink") (DHCP)、[Network Time Protocol](../Page/Network_Time_Protocol.md "wikilink") (NTP) などがある。

音声や動画のトラフィックも一般にUDPを使用している。リアルタイムの動画・音声ストリーミングのプロトコルはパケット喪失が発生しても画質・音質が若干低下するだけで済むよう設計されており、喪失パケットの[再送](https://ja.wikipedia.org/wiki/再送 "wikilink")を待って止まってしまう方が不都合である。TCPとUDPは同じネットワーク上で使われており、ストリーミングなどの用途が増えているため、UDPトラフィックの割合も増えている。そのため、[POS](../Page/販売時点情報管理.md "wikilink")、[会計](https://ja.wikipedia.org/wiki/会計ソフトウェア "wikilink")、[データベースなどのTCPを使っているシステムはUDPトラフィックに圧迫されつつある](../Page/データベース管理システム.md "wikilink")。TCPでパケットを喪失すると、輻輳制御が働いて転送レートを抑えるというのも一因である。リアルタイム・アプリケーションもビジネス・アプリケーションもビジネスには重要なので、[Quality of Service](../Page/Quality_of_Service.md "wikilink") のソリューション開発が大切だとする者もいる\[20\]。

## UDPとTCPの比較

[TCPはコネクション指向のプロトコルであり](../Page/Transmission_Control_Protocol.md "wikilink")、エンドツーエンドの通信を設定するための[ハンドシェイク](https://ja.wikipedia.org/wiki/ハンドシェイク "wikilink")を必要とする。コネクションが設定されると、そのコネクション上で双方向のデータ転送が行われる。

  - 信頼性
    TCPではメッセージに対する確認応答があり、再送やタイムアウトを管理している。そして、何とかしてメッセージを確実に届けようとする。パケットが喪失した場合、相手側から再送を要求する。TCPでは全くデータが失われないか、あるいは複数のタイムアウトが発生してコネクションが維持できなくなるかのどちらかである。
  - 順序性
    2つのメッセージが順番に送り出されると、受信側アプリケーションには順番どおりにメッセージが届く。セグメントがばらばらな順番で届いた場合、TCPがそれらを蓄積し、正しい順番に並べ替えてアプリケーションに渡す。
  - オーバーヘッド
    TCPでは、ユーザーのデータを送信する前に必ず3つのパケットをやり取りしてコネクションを確立する必要がある。また、信頼性と[輻輳制御](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")のためのオーバーヘッドもある。
  - ストリーミング
    アプリケーションから見ればデータは[バイトストリームであり](../Page/バイト_\(情報\).md "wikilink")、個々のメッセージ（セグメント）の境界を示す印はない。

UDPはより単純なメッセージベースのコネクションレス・プロトコルである。コネクションレス・プロトコルはエンドツーエンドのコネクション確立を行わない。通信は送信側から受信側へ、特に相手の状態を確認することなく一方的に行われる。UDPがTCPに対して優れているのはリアルタイム性であり、[VoIP](../Page/VoIP.md "wikilink")などの用途で重視される。

  - 信頼性
    メッセージを送ったとき、それが相手に届いたかどうかを確認できず、喪失したらそのままである。検査合計で誤りを検出したメッセージも廃棄され、廃棄したことはどちらのアプリケーションにも通知されない。確認応答、再送、タイムアウトといった概念がない。
  - 順序性
    2つのメッセージを相手に送ったとき、どちらが先に届くかは予測できない。
  - オーバーヘッド
    メッセージの順序を保証せず、コネクションも保持しないなど、[トランスポート層](../Page/トランスポート層.md "wikilink")プロトコルとしてはオーバーヘッドが小さい。
  - データグラム
    パケットは個別に送信され、受信されたときだけ完全性をチェックする。メッセージ単位の送受信であり、送信元のアプリケーションが1つのメッセージとして送ったものが、そのまま相手側アプリケーションに1つのメッセージとして届く。
  - 輻輳
    UDP自身は輻輳を防げない。広帯域アプリケーションでは輻輳が発生する可能性があり、必要ならば上位層で[輻輳制御](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")を実装しなければならない。

## RFC

  - RFC 768 – User Datagram Protocol
  - RFC 2460 – Internet Protocol, Version 6 (IPv6) Specification
  - RFC 2675 - IPv6 Jumbograms
  - RFC 4113 – Management Information Base for the UDP
  - RFC 4347 - [Datagram Transport Layer Security](https://ja.wikipedia.org/wiki/Datagram_Transport_Layer_Security "wikilink")
  - RFC 5405 – Unicast UDP Usage Guidelines for Application Designers

## 注釈・出典

## 関連項目

  - [UDP-Lite](../Page/UDP-Lite.md "wikilink")
  - [TCPやUDPにおけるポート番号の一覧](https://ja.wikipedia.org/wiki/TCPやUDPにおけるポート番号の一覧 "wikilink")
  - [UDPヘルパーアドレス](../Page/UDPヘルパーアドレス.md "wikilink")
  - [SCTP](../Page/Stream_Control_Transmission_Protocol.md "wikilink")
  - [Reliable User Datagram Protocol](https://ja.wikipedia.org/wiki/Reliable_User_Datagram_Protocol "wikilink") (RUDP)

## 外部リンク

  - [The Trouble with UDP Scanning (PDF)](https://condor.depaul.edu/~jkristof/papers/udpscanning.pdf)
  - [Breakdown of UDP frame](http://www.networksorcery.com/enp/protocol/udp.htm)
  - [UDP connections](http://www.faqs.org/docs/iptables/udpconnections.html)

[Category:トランスポート層プロトコル](https://ja.wikipedia.org/wiki/Category:トランスポート層プロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.
2.
3.  Forouzan, B.A. (2000). *TCP/IP: Protocol Suite, 1st ed*. New Delhi, India: Tata McGraw-Hill Publishing Company Limited.
4.
5.
6.  Clark, M.P. (2003). *Data Networks IP and the Internet, 1st ed*. West Sussex, England: John Wiley & Sons Ltd.
7.
8.
9.
10.
11. RFC 2675
12.
13.
14.
15. Postel, J. (August 1980). RFC 768: User Datagram Protocol. *Internet Engineering Task Force*. Retrieved from //tools.ietf.org/html/rfc768
16. Eubanks, M., Chimento, P., and M. Westerlund, "IPv6 and UDP Checksums for Tunneled Packets", RFC 6935, April 2013.
17. Deering S. & Hinden R. (December 1998). RFC 2460: Internet Protocol, Version 6 (IPv6) Specification. *Internet Engineering Task Force*. Retrieved from //tools.ietf.org/html/rfc2460
18.
19.
20.