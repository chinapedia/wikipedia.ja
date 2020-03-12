> この記事は[Transmission Control Protocol](https://ja.wikipedia.org/wiki/Transmission_Control_Protocol)から翻訳されています。


**Transmission Control Protocol**（トランスミッション コントロール プロトコル、**TCP**）は、伝送制御プロトコルといわれ、[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")の中核[プロトコルのひとつ](../Page/通信プロトコル.md "wikilink")。

## 概要

TCPはインターネット・プロトコル・スイートの初期からある2つのコンポーネントの1つで、もう1つは [Internet Protocol](../Page/Internet_Protocol.md "wikilink") (IP) である。そのため、スイート全体を一般に「TCP/IP」と呼ぶ。

TCPは、送信元のコンピュータ上のプログラムから別のコンピュータ上の別のプログラムへと信頼できる順序通りの[オクテット列の転送を行う](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")。 [World Wide Web](../Page/World_Wide_Web.md "wikilink")、[電子メール](../Page/電子メール.md "wikilink")、、[File Transfer Protocol](../Page/File_Transfer_Protocol.md "wikilink") (FTP) などの主要な[インターネット](../Page/インターネット.md "wikilink")・アプリケーションはTCPを利用している。

高信頼のデータストリーム・サービスを必要としないアプリケーションでは [User Datagram Protocol](../Page/User_Datagram_Protocol.md "wikilink") (UDP) を使うこともある。 UDPは信頼性よりも[レイテンシ](../Page/レイテンシ.md "wikilink")低減を重視した[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")サービスを提供する。

[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の[トランスポート層にあたる](https://ja.wikipedia.org/wiki/OSI参照モデル#トランスポート層 "wikilink")。 [ネットワーク層のプロトコルである](https://ja.wikipedia.org/wiki/OSI参照モデル#ネットワーク層 "wikilink")[IPの上位プロトコルとして使われる](../Page/Internet_Protocol.md "wikilink")。 IPヘッダでの[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")は6である。

TCPは、[セッション](../Page/セッション.md "wikilink")という形で1対1の通信を実現し、パケットシーケンスチェックによる欠損パケット[再送](https://ja.wikipedia.org/wiki/再送 "wikilink")などのエラー訂正機能などを持ち、[データ転送](https://ja.wikipedia.org/wiki/データ転送 "wikilink")などの信頼性の必要な場面でよく使用される。 一方他の[トランスポート層](../Page/トランスポート層.md "wikilink")プロトコルに比べ、[プロトコル](../Page/プロトコル.md "wikilink")上のオーバヘッドが大きい為、比較的低速となる。

[IETFが](../Page/Internet_Engineering_Task_Force.md "wikilink")、[RFC](../Page/Request_for_Comments.md "wikilink") 793 (STD 7) に技術仕様を規定している。

上位プロトコルとして、[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")、[FTP](../Page/File_Transfer_Protocol.md "wikilink")、[Telnet](../Page/Telnet.md "wikilink")、[SSHなどがある](../Page/Secure_Shell.md "wikilink")。

## 起源

[1974年](../Page/1974年.md "wikilink")5月、Institute of Electrical and Electronic Engineers ([IEEE](../Page/IEEE.md "wikilink")) が "*A Protocol for Packet Network Interconnection*" と題した論文を出版\[1\]。著者は[ヴィントン・サーフ](../Page/ヴィントン・サーフ.md "wikilink")と[ロバート・カーン](../Page/ロバート・カーン.md "wikilink")で、ノード間で[パケット通信](../Page/パケット通信.md "wikilink")を使い資源を共有する[インターネットワーキング](https://ja.wikipedia.org/wiki/インターネットワーキング "wikilink")のプロトコルを記述したものである。このモデルでの中核制御コンポーネントが *Transmission Control Program* で、ホスト間のコネクション指向のリンクと[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")サービスの両方を含んでいた。当初一体だった Transmission Control Program は後に[モジュール化](https://ja.wikipedia.org/wiki/モジュール化 "wikilink")されたアーキテクチャに分割され、コネクション指向部分の *Transmission Control Protocol* とデータグラムサービス部分の *Internet Protocol* に分けられた。このモデルを一般に TCP/IP と呼ぶが、公式には[インターネット・プロトコル・スイート](../Page/インターネット・プロトコル・スイート.md "wikilink")と呼ぶようになった。

## ネットワーク機能

TCPは、アプリケーションプログラムと [Internet Protocol](../Page/Internet_Protocol.md "wikilink") (IP) の中間の層で通信サービスを提供する。すなわち、[アプリケーションプログラムがIPを使って大きなデータの塊を送信したいという場合](../Page/アプリケーションソフトウェア.md "wikilink")、直接そのデータをIPのサイズで分割して一連のIP要求を発行するのではなく、TCPに1度要求を発行するだけで、TCPにIPの詳細を任せることができる。

IPは[パケット](../Page/パケット.md "wikilink")と呼ばれる情報の断片をやり取りする形で機能する。パケットは、ヘッダ部に本体が続く形で構成される[オクテット列である](https://ja.wikipedia.org/wiki/オクテット_\(コンピュータ\) "wikilink")。ヘッダ部には、そのパケットの宛先があり、その宛先に到達するために中継で使用すべき[ルーター](../Page/ルーター.md "wikilink")を指定することもある。本体にはIPが転送すべきデータが格納される。

ネットワークが混雑（[輻輳](../Page/輻輳.md "wikilink")）したり、トラフィックを負荷分散させようとしたり、その他ネットワークの予測できない振る舞いにより、IPパケットは喪失したり、重複したり、順序がばらばらで届いたりする。TCPはそれらの問題を検出し、喪失データの再送を要求し、データの順序を正しく並べ替え、さらにネットワークの混雑が起きにくくなるよう制御して他の問題が発生する可能性を低くする。TCPの受信側は、オクテット列の順序を元通りに再現すると、それをアプリケーションプログラムに渡す。したがってTCPは、アプリケーションに対してネットワークの詳細を隠蔽して抽象化しているといえる。

TCPはインターネットの様々な主要アプリケーションで広く使われている。例えば、[World Wide Web (WWW)](../Page/World_Wide_Web.md "wikilink")、[電子メール](../Page/電子メール.md "wikilink")、[File Transfer Protocol](../Page/File_Transfer_Protocol.md "wikilink")、[Secure Shell](../Page/Secure_Shell.md "wikilink")、[ファイル共有](https://ja.wikipedia.org/wiki/ファイル共有ソフト "wikilink")、一部の[ストリーミング](../Page/ストリーミング.md "wikilink")などがある。

TCPは高速さよりも正確さに最適化されており、そのためメッセージの順序がばらばらだったり、喪失したメッセージの再送を待ったりすることがあると、秒のオーダーの比較的長い遅延が生じることがある。これはリアルタイム性を求められる[VoIP](../Page/VoIP.md "wikilink")などのアプリケーションには向いていない。そのような用途には一般に [User Datagram Protocol](../Page/User_Datagram_Protocol.md "wikilink") (UDP) 上の [Real-time Transport Protocol](../Page/Real-time_Transport_Protocol.md "wikilink") (RTP) などのプロトコルが推奨される\[2\]。

TCPは高信頼ストリーム配送サービスであり、重複したり喪失したりすることなく、あるホストから別のホストにデータを配送することを保証する。パケット転送は信頼できないので、確認応答と再送という技法でパケット転送の信頼性を保証している。この基本的技法では、受信側がデータを受信するたびに確認応答メッセージを送り返す必要がある。送信側は送信した各パケットの記録を保持しておき、次のパケットを送信する前に確認応答を待つ。送信側はまたパケット送信時からのタイマーを保持しており、規定時間以内に確認応答がなければ再送を行う。これは、パケットが喪失した場合や内容が壊れていて確認応答もできない場合に必要とされる\[3\]。

TCPには一連の規則がある。Internet Protocol と組合わせて使う際の規則、インターネット上のホスト間で「メッセージ単位の形式で」データを送信するためのIPの規則である。IPがデータの実際の配送を扱う一方、TCPは「セグメント (segment)」と呼ばれるデータ単位の転送を扱う。セグメントはネットワーク内での効率的ルーティングのためにメッセージを分割したものである。例えばWebサーバがHTMLファイルを送信する場合、そのサーバのTCP層（[トランスポート層](../Page/トランスポート層.md "wikilink")）でそのファイルのオクテット列を一連のセグメントに分割し、セグメント毎にIP層（[ネットワーク層](../Page/ネットワーク層.md "wikilink")）に渡す。IP層はTCPセグメントに宛先[IPアドレス](../Page/IPアドレス.md "wikilink")などを含むIPヘッダを付与して、IPパケットに[カプセル化する](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。各パケットは同じ宛先アドレスを付与されているが、ネットワーク内の転送経路はパケット毎に異なる可能性がある。宛先のコンピュータ上のクライアントプログラムがそれらを受信すると、TCP層はセグメント群に誤りがないことを確認し、それらを正しい順序で再結合し、アプリケーションに渡す。

## TCPセグメント構造

TCPは上位から受け取ったデータを分割し、それにTCPヘッダを付与してTCPセグメントを作成する。TCPセグメントはさらに [Internet Protocol](../Page/Internet_Protocol.md "wikilink") (IP) データグラムに[カプセル化される](https://ja.wikipedia.org/wiki/カプセル化_\(通信\) "wikilink")。TCPセグメントは「データを相手と交換するためにTCPが使う情報の束」である\[4\]。

なお、非公式に「TCPパケット」という用語が使われることがあるが、最近の用法では TCP PDU ([Protocol Data Unit](../Page/Protocol_Data_Unit.md "wikilink")) は「セグメント」、IP PDU は「[データグラム](https://ja.wikipedia.org/wiki/データグラム "wikilink")」\[5\]、[データリンク層](../Page/データリンク層.md "wikilink")のPDUは「フレーム」と呼ぶのが一般的である。

> プロセスはTCPを呼び出し、データを格納したバッファを引数で渡すことでデータを送信する。TCPはそれらのバッファ内のデータをセグメント群にパッケージし、インターネット・モジュール（例えばIP）を呼び出すことで宛先のTCPへ各セグメントを送信する。\[6\]

TCPセグメントは、セグメント・ヘッダとデータ部分から成る。TCPヘッダは10の必須フィールドとオプションの拡張フィールドを含む（テーブルではオプション部分をオレンジで示している）。

データ部はヘッダ部の後に続いている。その内容はアプリケーションに渡すべきデータである。データ部の長さはTCPセグメントのヘッダには記されておらず、IPヘッダにあるIPデータグラム長からIPヘッダとTCPヘッダの長さを差し引いて計算できる。

<table>
<caption>TCPヘッダ</caption>
<thead>
<tr class="header">
<th><p><em>オフセット</em></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/オクテット_(コンピュータ)" title="wikilink">オクテット</a></p></th>
<th><p>0</p></th>
<th><p>1</p></th>
<th><p>2</p></th>
<th><p>3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>オクテット</p></td>
<td><p><a href="../Page/ビット.md" title="wikilink"><code>ビット</code></a></p></td>
<td><p><code> 0</code></p></td>
<td><p><code> 1</code></p></td>
<td><p><code> 2</code></p></td>
<td><p><code> 3</code></p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td><p><code>  0</code></p></td>
<td><p>送信元ポート</p></td>
<td><p>送信先ポート</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p><code> 32</code></p></td>
<td><p>シーケンス番号</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p><code> 64</code></p></td>
<td><p>確認応答番号（<code>ACK</code> がセットされている場合）</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>12</p></td>
<td><p><code> 96</code></p></td>
<td><p>ヘッダ長</p></td>
<td><p>予約<br />
<strong><code>0</code><code> </code><code>0</code><code> </code><code>0</code></strong></p></td>
<td><p><code>N</code><br />
<code>S</code></p></td>
<td><p><code>C</code><br />
<code>W</code><br />
<code>R</code></p></td>
</tr>
<tr class="even">
<td><p>16</p></td>
<td><p><code>128</code></p></td>
<td><p>検査合計</p></td>
<td><p>緊急ポインタ（<code>URG</code>がセットされている場合）</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>20<br />
...</p></td>
<td><p><code>160</code><br />
<code>...</code></p></td>
<td><p>オプション（ヘッダ長が5より大きければ、必要に応じて最後まで0でパディングする）<br />
...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - 送信元[ポート](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")（16ビット） – 送信側のポート番号
  - 送信先ポート（16ビット） – 受信側のポート番号
  - シーケンス番号（32ビット） – 2つの役割がある。
      - `SYN`フラグがセットされている場合 (1)、初期シーケンス番号である。実際の先頭データバイトのシーケンス番号と対応する確認応答の確認応答番号は、このシーケンス番号に1を加えた値になる。
      - `SYN`フラグがセットされていない場合 (0)、このセッションにおけるこのパケットの先頭データバイトの累積シーケンス番号である。
  - 確認応答番号（32ビット） – `ACK`フラグがセットされている場合、受信側が期待する次のシーケンス番号を格納している。（もしあれば）それまでの全バイト列の受信を確認済みであることを示す。最初に互いに`ACK`を送る際は、相手側の初期シーケンス番号を確認するだけで、データは含めない。
  - ヘッダ長（4ビット） – TCPヘッダのサイズを32ビットワード単位で表す。ヘッダの最小サイズは5ワードで、最大サイズは15ワードである。すなわち、ヘッダ部は20バイトから60バイトまでの大きさであり、21バイトめからの40バイトはオプションとなる。TCPセグメント内の実際にデータが始まる位置を示すことにもなるため、データオフセットとも呼ぶ。
  - 予約（3ビット） – 将来の利用のために予約されたビット列であり、常に 0 をセットする。
  - フラグあるいは制御ビット列（9ビット） – 9個の1ビットのフラグがある。
      - `NS`（1ビット） – ECN-nonce 輻輳保護（RFC 3540 でヘッダに追加）
      - `CWR`（1ビット） – 輻輳制御ウィンドウ縮小 (Congestion Window Reduced)。`ECE`フラグがセットされたTCPセグメントを受信した際、輻輳制御機構で応答するときにセットする。（RFC 3168 でヘッダに追加）
      - `ECE`（1ビット） – ECN-Echo を示す。
          - `SYN`フラグがセットされている場合 (1)、を利用可能であることを示す。
          - `SYN`フラグがセットされていない場合 (0)、通常送受信時にIPヘッダに Congestion Experienced フラグがセットされたパケットを受信したことを示す。（RFC 3168 でヘッダに追加）
      - `URG`（1ビット） – 緊急ポインタ・フィールドが有効であることを示す。
      - `ACK`（1ビット） – 確認応答番号フィールドが有効であることを示す。最初の`SYN`パケットを除く以降の全パケットでこのフラグをセットする。
      - `PSH`（1ビット） – プッシュ機能。バッファに蓄えたデータをアプリケーションにプッシュする（押しやる）ことを依頼する。
      - `RST`（1ビット） – コネクションをリセットする。
      - `SYN`（1ビット） – シーケンス番号の同期。通信する両方で最初のパケットだけ、このフラグをセットする。他のフラグはこのフラグの値によって意味が変化したり、このフラグの値によって有効/無効が決まる。
      - `FIN`（1ビット） – 送信終了を示す。
  - ウィンドウサイズ（16ビット） – 受信ウィンドウの大きさ。このセグメントの送信側がその時点（確認応答番号フィールドにあるシーケンス番号以降）で受信可能なバイト数を指定する。詳しくは[フロー制御の節と](https://ja.wikipedia.org/wiki/#フロー制御 "wikilink")[ウィンドウスケーリングの節を参照](https://ja.wikipedia.org/wiki/#ウィンドウスケーリング "wikilink")。
  - 検査合計（16ビット） – ヘッダおよびデータの誤り検出用の16ビット[検査合計](https://ja.wikipedia.org/wiki/検査合計 "wikilink")。後述の[\#誤り検出](https://ja.wikipedia.org/wiki/#誤り検出 "wikilink")と[\#検査合計の計算](https://ja.wikipedia.org/wiki/#検査合計の計算 "wikilink")も参照。
  - 緊急ポインタ（16ビット） – `URG`フラグがセットされている場合、最新の緊急データバイトのシーケンス番号からのオフセットを示す。
  - オプション（0から320ビットまで可変で、32ビット単位で変化する） – ヘッダ長フィールドによって、このフィールドの長さが決まる。個々のオプションは、オプション種別（1バイト）、オプション長（1バイト）、オプションデータ（可変）から成る。オプション種別フィールドはオプションの種類を示し、オプションとしては必ず存在するフィールドである。オプションの種類によって扱い方が違い、後続の2つのフィールドの有無も異なる。存在する場合、オプション長フィールドはそのオプションの全長が格納されており、オプションデータ・フィールドにはオプションに関わる値が格納されている。例えば、オプション種別が 0x01 の場合、No-Op オプションであることを意味し、オプション長やオプションデータは存在しない。オプション種別が0の場合、End Of Options オプションであることを意味し、この場合も1バイトだけである。オプション種別が 0x02 の場合、[最大セグメントサイズ](https://ja.wikipedia.org/wiki/最大セグメントサイズ "wikilink") (MSS) オプションであることを意味し、その後ろに1バイトのMSSフィールド長を指定するフィールドがある（値は 0x04）。この長さはオプションの全長であるため、オプション種別フィールドとオプション長フィールドのぶんも含んでいる。従って、MSS値は通常2バイトで表され、オプション長は4（バイト）となる。例えば、MSS値が 0x05B4 なら、MSSオプション全体の値は (0x02 0x04 0x05B4) となる。
  - パディング – TCPヘッダが32ビット境界で終わるようにするために使われる。パディングは常に0である\[7\]。

一部のオプションは`SYN`がセットされているときだけ送信される。それらは以下で <sup>`[SYN]`</sup> で示している。各行の先頭は「オプション種別\[, オプション長, オプション値\]（全ビット数）」の形式で示す。

  -   - 0（8ビット） - オプションリストの終了
      - 1（8ビット） - 何もしない（NOP、パディング）。オプション・フィールドを32ビット境界に揃えるのに使う。
      - 2,4,*SS*（32ビット） - 最大セグメント長（[最大セグメントサイズ](https://ja.wikipedia.org/wiki/最大セグメントサイズ "wikilink") を参照） <sup>`[SYN]`</sup>
      - 3,3,*S*（24ビット） - ウィンドウスケール（詳しくは[ウィンドウスケーリング参照](https://ja.wikipedia.org/wiki/#ウィンドウスケーリング "wikilink")）<sup>`[SYN]`</sup>\[8\]
      - 4,2（16ビット） - 選択確認応答が可能。<sup>`[SYN]`</sup> （[選択確認応答を参照](https://ja.wikipedia.org/wiki/#選択確認応答 "wikilink")）\[9\]
      - 5,*N,BBBB,EEEE,...*（可変長、*N* は 10, 18, 26, 34 のいずれか） - 選択確認応答 (SACK)\[10\]。最初の2バイトの後に選択確認応答される1から4ブロックのリストを32ビットの開始/終了ポインタで示す。
      - 8,10,*TTTT,EEEE*（80ビット） - タイムスタンプと前のタイムスタンプのエコー（[TCPタイムスタンプを参照](https://ja.wikipedia.org/wiki/#TCPタイムスタンプ "wikilink")）\[11\]
      - 14,3,*S*（24ビット） - 検査合計方式変更要求。<sup>`[SYN]`</sup>\[12\]
      - 15,*N,...*（可変長） - 検査合計方式が変更されて、その検査合計が16ビットより長い場合にこれで検査合計値を示す。

他のオプションは既に使われていないもの、実験的なもの、標準になっていないものなどである。

## プロトコル操作

[Tcp_start.svg](https://ja.wikipedia.org/wiki/File:Tcp_start.svg "fig:Tcp_start.svg")呼び出しを付記した。\]\] [Tcp_end.svg](https://ja.wikipedia.org/wiki/File:Tcp_end.svg "fig:Tcp_end.svg") TCPプロトコル操作は3つのフェーズに分けられる。コネクションは多段階のハンドシェイクプロセスで正しく確立する必要があり（コネクション確立フェーズ）、その後「データ転送フェーズ」に入る。データ転送が完了したら「コネクション終了フェーズ」で仮想回線を閉じ、確保していたリソースを解放する。

TCPコネクションは[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")が[ソケットというプログラミングインタフェースを通して管理する](../Page/ソケット_\(BSD\).md "wikilink")。TCPコネクションが存在する間、以下のような状態間で遷移する\[13\]。

1.  LISTENING : サーバの場合、任意のリモートクライアントからのコネクション要求を待ち受ける。
2.  SYN-SENT : SYNフラグとACKフラグをセットしたTCPセグメントを相手側が送ってくるのを待つ状態（通常、クライアント側）。
3.  SYN-RECEIVED : コネクション確立要求に対して確認応答を返した後、相手側が確認応答を返してくるのを待つ状態（通常、サーバ側）。
4.  ESTABLISHED : 相手側とコネクションが確立し、指定ポートでのデータの送受信が可能な状態。
5.  FIN-WAIT-1 : FINフラグをセットしたTCPセグメントを先に相手に送り、確認応答が返ってくるのを待つ状態。
6.  FIN-WAIT-2 : FINに対する確認応答を受け取り、相手からのFINを待つ状態。
7.  CLOSE-WAIT : 相手から先にFINを受け取り、アプリケーションがクローズ可能となるのを待つ状態。クローズ可能になったら相手にFINに対する確認応答を送る。
8.  LAST-ACK : FINセグメントを送って、その確認応答を待っている状態。
9.  TIME-WAIT : 「FIN-WAIT2」でFINセグメントを受信し、確認応答を返した状態。相手が確認応答を受信完了することを保証するため、十分な時間待つ。RFC 793 では最大4分間この状態でコネクションを保つことができるとされており、これをMSL (maximum segment lifetime) と呼ぶ。
10. CLOSED : コネクションがクローズした状態。

### コネクション確立

コネクションを確立する際、TCPでは[3ウェイ・ハンドシェイク](../Page/3ウェイ・ハンドシェイク.md "wikilink")を行う。

クライアントがサーバと接続する前、サーバはコネクション可能なようにポートをバインドしておかなければならない。これをパッシブ・オープンと呼ぶ。サーバ側がパッシブ・オープンになっていれば、クライアントはアクティブ・オープンを開始できる。コネクションを確立するための3ウェイ・ハンドシェイクは次のようになる。

1.  **SYN**: クライアントはサーバにSYNを送り、アクティブ・オープンを行う。クライアントはこの際に無作為な値Aを選び、SYNセグメントのシーケンス番号とする。
2.  **SYN-ACK**: それに対してサーバはSYN+ACKを返す。確認応答番号は受信したSYNセグメントのシーケンス番号に1を加えたもの (A + 1) とし、SYN+ACK のシーケンス番号は別の無作為な値 B とする。
3.  **ACK**: クライアントがサーバからの SYN+ACK に対して ACK を返す。その際のシーケンス番号は受信した SYN+ACK の確認応答番号 (A + 1) とし、確認応答番号は SYN+ACK のシーケンス番号に1を加えた値 (B + 1) とする。

この時点でクライアントとサーバ双方がコネクション確立の確認応答を受け取ったことになる。

### リソースの使い方

多くの実装では、テーブルの1エントリを動作中のOSプロセスとのセッションにマッピングする。TCPセグメントにはセッション識別子がないため、通信している双方でクライアントのアドレスとポートでセッションを識別する。パケットを受信すると、TCPソフトウェアはそのテーブルを参照して、対応するプロセスを見つける。

サーバ側でのセッション数はメモリ容量にのみ制限され、コネクション確立要求がくるたびに増えていく。しかし、クライアントはサーバに最初のSYNセグメントを送る前に無作為にポートを選んで確保しなければならない。このポートはコネクションをクローズするまで確保され続け、実質的にクライアントの持つIPアドレス毎の外に出て行くコネクション数を制限している。アプリケーションが不要になったコネクションをクローズしそこねると、空いているポートが足りなくなり、新たなTCPコネクションを確立できなくなる。

また、通信する双方で確認応答を受け取っていない送信済みデータとアプリケーションに渡す前の受信データを格納しておく領域を確保する必要がある。

### データ転送

TCP には以下のように [User Datagram Protocol](../Page/User_Datagram_Protocol.md "wikilink") とは異なる重要な特徴がある。

  - データ転送時の順序を保証 - 受信側でシーケンス番号を使って並べ替えを行う\[14\]。
  - 喪失パケットの再送 - 確認応答のないセグメントは再送する\[15\]。
  - 誤りのないデータ転送\[16\]
  - フロー制御 - 高信頼配送を保証するため、送信側が送出するレートを制限する。受信側は常にどのくらいのデータを受け取れるかを知らせている（スライディングウィンドウで制御している）。受信側のバッファが一杯になると、次の確認応答ではウィンドウサイズを0とするので送信が停止し、バッファ内のデータを処理する余裕ができる\[17\]。
  - 輻輳制御\[18\]

#### 高信頼転送

TCPは「シーケンス番号」を使ってデータの各バイトを識別する。シーケンス番号は双方のホストが送信するバイト列に先頭から振られる番号であり、それによってデータがどう分割されても、順番が入れ替わっても、転送中に失われても、元のデータを復元できる。ペイロードの各バイトを送るたびにシーケンス番号をインクリメントしなければならない。3ウェイ・ハンドシェイクの最初の2ステップで、双方のホストは初期シーケンス番号 (ISN) をやりとりする。この番号は任意であり、[TCPシーケンス番号予測攻撃](https://ja.wikipedia.org/wiki/TCPシーケンス番号予測攻撃 "wikilink")への防御のために予測不可能な値とすべきである。

TCPは「累積確認応答」方式を採用しており、受信側が確認応答を返すとき、そのセグメントで示されている確認応答番号は、対応するシーケンス番号未満のデータを全て受信済みであることを示している。送信側はペイロードの先頭バイトのシーケンス番号をそのセグメントのシーケンス番号として設定する。受信側は次に受信することを期待しているバイトのシーケンス番号を確認応答番号に設定して確認応答を返す。例えば、送信側が4バイトのペイロードをシーケンス番号 100 で送信する場合、そのペイロードの4バイトのシーケンス番号は順に 100、101、102、103 である。受信側がこのセグメントを受信すると、その確認応答での確認応答番号は 104 となり、次のパケットで送られてくるペイロードの先頭バイトのシーケンス番号となっている。

累積確認応答に加えて、受信側は[選択確認応答でさらなる情報を送ることができる](https://ja.wikipedia.org/wiki/#選択確認応答 "wikilink")。

送信側がネットワーク内でデータが失われたと判断した場合、データの再送を行う。

#### 誤り検出

後述の[\#検査合計の計算](https://ja.wikipedia.org/wiki/#検査合計の計算 "wikilink")も参照。 シーケンス番号と確認応答は、パケットの重複、喪失パケットの再送、データの順序通りの並べ替えなどを扱っている。受信したパケットの内容が正しいことを確認するため、TCPには[検査合計](https://ja.wikipedia.org/wiki/検査合計 "wikilink")フィールドがある。検査合計フィールドは設定必須の項目であり省略できない。

TCP検査合計は、現在の標準から見れば弱い。データリンク層のビット誤り率が高ければ、TCP検査合計とは別の[誤り検出訂正](../Page/誤り検出訂正.md "wikilink")機能が必要である。TCP/IPの下層である[データリンク層](../Page/データリンク層.md "wikilink")には一般に[CRCなどのもっと強力な検査機構があり](../Page/巡回冗長検査.md "wikilink")、TCP検査合計の弱さを一部補っている（例えば、[PPPや](../Page/Point-to-Point_Protocol.md "wikilink")[イーサネット](../Page/イーサネット.md "wikilink")）。しかし、だからといって16ビットのTCP検査合計が無駄というわけではない。実際、CRCで保護された通信路でパケットに誤りが残ることはよくあるが、[エンドツーエンドの](../Page/エンドツーエンド原理.md "wikilink")16ビットTCP検査合計がそういった単純な誤りを捉えている\[19\]。これは[エンドツーエンド原理](../Page/エンドツーエンド原理.md "wikilink")が機能している例である。

#### フロー制御

TCPはエンドツーエンドの[フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")プロトコルを使い、送信ペースが受信側にとって速すぎる状態になるのを防いでいる。様々な性能の機器が接続されたネットワークでは、フロー制御は欠かせない機構である。例えば、PCから性能の劣るPDAにデータを送る場合、PDAの性能に合わせて送信ペースを調整する必要がある\[20\]。

TCPは[スライディングウィンドウ](https://ja.wikipedia.org/wiki/スライディングウィンドウ "wikilink")によるフロー制御を採用している。各TCPセグメントについて、受信側は「ウィンドウサイズ」フィールドで、そのコネクション用のバッファの空き容量に相当する今後受信可能なデータの量（バイト単位）を示す。送信側は確認応答を待ち合わせるまでに、そのフィールドで指定された量までのデータを送り、新たな確認応答でウィンドウサイズ・フィールドを確認してさらに送信できるデータ量を更新する。

[Tcp.svg](https://ja.wikipedia.org/wiki/File:Tcp.svg "fig:Tcp.svg")

受信側がウィンドウサイズを0としたとき、送信側は送信を停止してタイマ (persist timer) を起動する。このタイマは受信側のウィンドウサイズの更新セグメントが喪失して[デッドロック](../Page/デッドロック.md "wikilink")状態になるのを防ぐためのものである（受信側がウィンドウサイズを更新しないと送信を再開できないため）。タイマがタイムアウトすると、送信側は小さなパケットを送り、その確認応答で受信側のウィンドウサイズが回復したかを調べる。

受信側での受信データの処理が遅いと、ウィンドウサイズの指定は小さいままとなる。これを (SWS)と呼び、送信側は1度に数バイトのデータしか送れなくなり、TCPヘッダの方が大きな割合を占めるため転送効率が極端に低下する。そのような状況に陥らないようにするためのウィンドウ・アルゴリズムが RFC 813 (Window and acknowledgement strategy in TCP) に記載されている。

#### 輻輳制御

TCPは高性能を達成し[輻輳](../Page/輻輳.md "wikilink")崩壊（ネットワーク性能が数桁のオーダーで低下する現象）を防ぐため、[輻輳制御](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")機構をいくつか備えている。ネットワークに流入させるデータレートを制御し、崩壊のきっかけとなるようなレート未満でデータを送るよう保つ。また、おおまかになフロー割り当てを目指す。

送信データへの ACK (確認応答)の有無は、送信側でネットワークの状態を推測する材料となる。これをタイマと組み合わせ、データのフローの振る舞いを変化させることができる。これを一般に輻輳制御またはネットワーク輻輳回避などと呼ぶ。

最近のTCP実装では、、、、ファストリカバリ([en](https://ja.wikipedia.org/wiki/:en:Slow-start#Fast_recovery "wikilink"), RFC 5681) という4つの相互にからみあったアルゴリズムを使用している。

スループットをあげるため輻輳しない限界まで送信側はスライディングウィンドウを大きくする必要があるが、ウィンドウサイズを調整する輻輳回避アルゴリズムは長年研究されている。一覧は [:w:TCP congestion avoidance algorithm](https://ja.wikipedia.org/wiki/:w:TCP_congestion_avoidance_algorithm "wikilink") を参照。かつては、輻輳するとパケットロスが発生することを利用し、パケットロスをベースにした [TCP Reno](https://ja.wikipedia.org/wiki/TCP_Reno "wikilink") およびそれを改良した [TCP NewReno](https://ja.wikipedia.org/wiki/TCP_NewReno "wikilink") (RFC 3782) がよく使われていたが、現在では、送信側のスライディングウィンドウにどれだけの時間とどまっていたかを元にしたアルゴリズム (Delay-based Congestion Avoidance) が中心になっており、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") では、[Windows Vista](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink") 以降は、 が採用され、[Linux](../Page/Linux.md "wikilink") では 2.6.8〜2.6.18 は  が、2.6.19 以降は  が使われている。

さらに送信側には「再送タイムアウト (RTO)」があり、送信してから確認応答が戻るまでの時間である[ラウンドトリップタイム](https://ja.wikipedia.org/wiki/ラウンドトリップタイム "wikilink") (RTT) を推算し、ばらつきも考慮して設定する。このタイマの動作は RFC 2988 で規定されている。RTTの推算には微妙な点がある。例えば、再送パケットのRTTを計算する場合は注意しなければならず、一般にやTCPタイムスタンプ（RFC 1323 参照）を使う。個々のRTTの標本から時系列で平均をとり、[ジェイコブソンのアルゴリズムを使って](https://ja.wikipedia.org/wiki/バン・ジェイコブソン "wikilink") Smoothed Round Trip Time (SRTT) を生成する。最終的にSRTT値がRTTの推算に使われる。

TCPを拡張して、喪失を高信頼に扱ったり、誤りを最小化したり、輻輳を制御してより高速化しようという試みが今も行われている。

#### 遅延送信

[最大セグメントサイズ](https://ja.wikipedia.org/wiki/最大セグメントサイズ "wikilink")以下の小さなパケットをばらばらと送るのは非効率なので、送信を遅延し、それらを1つのTCPパケットにまとめるのが、[Nagleアルゴリズム](https://ja.wikipedia.org/wiki/Nagleアルゴリズム "wikilink")である。同様に、複数のACKを1つにまとめるのが、[TCP遅延ACK](https://ja.wikipedia.org/wiki/TCP遅延ACK "wikilink")である。どちらも、送信を遅延させるという点においては同じだが、相互に影響し合い、遅延が増大するという問題があり、詳細は[Nagleアルゴリズム](https://ja.wikipedia.org/wiki/Nagleアルゴリズム "wikilink")を参照。

### 最大セグメントサイズ

[最大セグメントサイズ](https://ja.wikipedia.org/wiki/最大セグメントサイズ "wikilink") (MSS) はバイト単位で指定され、単一のセグメントとして受信可能な最大データ量を示す。性能を最大限発揮するには[IPフラグメンテーション](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")を十分防げる程度に小さくする必要がある。IPフラグメンテーションが行われると、パケット喪失時の再送に時間がかかることになる。一般にコネクション確立時にMSSオプションを使って双方のMSSを通知するので、適切なMSSを決めるには[データリンク層](../Page/データリンク層.md "wikilink")の [Maximum Transmission Unit](../Page/Maximum_Transmission_Unit.md "wikilink") (MTU) から導出したMSSを通知すればよい。さらに送信側は[経路MTU探索](https://ja.wikipedia.org/wiki/経路MTU探索 "wikilink")を使うことができ、通信相手との間にある経路でMTUが最小の部分を推定し、それを使ってMSSを動的に調整しIPフラグメンテーションを防ぐことができる。

MSS通知は「MSSネゴシエーション」とも呼ばれる。ネゴシエーションというと送信側と受信側が交渉して合意に達するかのように思われるが、実際には異なり、送信する方向によってそれぞれ異なるMSSが設定可能である\[21\]。これは例えば一方がメモリ容量が小さいため、バッファ領域を大きくとれない場合などに起きる（発見したパスMTUより小さいこともありうる）。

### 選択確認応答

もともとのTCPプロトコルで採用されている累積確認応答方式を使うと、パケットを喪失したときに非効率になる可能性がある。例えば、10,000バイトのデータを10個のTCPセグメントで送信し、その最初のパケットが喪失したとする。もともとの累積確認応答プロトコルでは、受信側は1,000から9,999までのバイトは受信成功、ただし0から999までのバイトを含む先頭パケットの受信に失敗したという風に伝えることができないので、送信側は10,000バイト全体を再送しなければならない。

このため RFC 2018 で「選択確認応答 (SACK)」オプションが追加された。これは、通常の累積確認応答とは別に、受信側が不連続なブロックを正しく受信したという確認応答を返せるようにしたものである。選択確認応答にはオプション部分にいくつかのSACKブロックを指定し、SACKブロックには正しく受信できた連続な範囲のシーケンス番号の開始点と終了点を指定する。例えば、先ほどの例では 1000 と 9999 のシーケンス番号をSACKオプションで示せばよい。すると送信側は 0 から 999 までのバイトを含む最初のパケットだけを再送する。

SACKオプションの拡張として RFC 2883 で定義されたデュプリケートSACK (D-SACK) オプションがある。パケットの順序がばらばらになると、送信側への確認応答も順序どおりにならないため送信側でパケット喪失と勘違いし、喪失したと思われるパケットを再送することがあり、同時にネットワーク輻輳を防ぐため送信ペースを落とす。このとき、受信側が D-SACK オプションで再送パケットが重複していることを通知すれば、遅くなっていた送信ペースを元に戻すことができる。

SACKオプションは必須ではなく、両者がサポートしている場合だけ使われる。これはコネクション確立時に調整される。SACKオプションは主なTCPスタックでサポートされており、広く使われている。選択確認応答は [Stream Control Transmission Protocol](../Page/Stream_Control_Transmission_Protocol.md "wikilink") (SCTP) でも使われている。

### ウィンドウスケーリング

広帯域ネットワークをより効率的に使うには、TCPウィンドウのサイズを大きくする必要がある。TCPヘッダのウィンドウサイズのフィールドは16ビットで、2バイトから65,535バイトまでしか設定できない。

ウィンドウサイズ・フィールドは拡張できないので、が導入されている。RFC 7323 で定義されているウィンドウスケール・オプションを使えば、最大ウィンドウサイズを 65,535 バイトから 1 ギガバイトに拡張できる。ウィンドウサイズのスケールアップはTCPのチューニング ([en](https://ja.wikipedia.org/wiki/:en:TCP_Tuning "wikilink")) に必須の要素である。

ウィンドウスケール・オプションは3ウェイ・ハンドシェイクの際にしか使われない。ウィンドウスケール・オプションのオプション値は、16ビットのウィンドウサイズ・フィールドの値を左にシフトするビット数を表している。ウィンドウスケールの値は0（シフトしない）から14まで指定でき、通信の双方向で別々に設定できる。どちらの方向もSYNセグメントのオプションとして通知する。

一部の[ルーター](../Page/ルーター.md "wikilink")や[ファイアウォール](../Page/ファイアウォール.md "wikilink")は、このスケールファクタを転送時に書き換えることがある。すると送信側と受信側でウィンドウサイズの認識が異なることになり、トラフィックが不安定になって、非常に低速になることがある\[22\]。

### TCPタイムスタンプ

TCPタイムスタンプは RFC 1323 で定義されており、パケット送出の順序をTCPレベルで知ることが出来る。TCPタイムスタンプはシステムクロックに合わせているわけではなく、無作為な値から開始する。多くのOSはこのタイムスタンプ値をミリ秒単位でインクリメントする。ただし、RFCは単に時間経過に比例して増加すべきだとしているだけである。

タイムスタンプのフィールドは2つある。

  - 4バイトの送信側タイムスタンプ値（自分のタイムスタンプ）
  - 4バイトの応答タイムスタンプ値（相手から直近に受け取ったタイムスタンプ値）

TCPタイムスタンプは PAWS (Protection Against Wrapped Sequences) と呼ばれるアルゴリズム（RFC 1323 参照）で利用する。PAWSは、2の32乗まであるシーケンス番号が一周してしまう場合に使われる。シーケンス番号はデータバイト毎に振られるので、最大4ギガバイトしか表せないが、最近の高速ネットワークでは1分以内に一周する可能性があり、再送が必要になったとき、現在の周回なのか前の周回なのかを識別するのにタイムスタンプを使う。

RFC 1323 の2.2節では、ウィンドウサイズは1ギガバイトまでとされているため、多くの実装でスケールオプションの最大値を14までとしている。

また、Eifel detection アルゴリズム (RFC 3522) でもTCPタイムスタンプを使っており、再送の原因がパケット喪失なのか順序がばらばらになったせいなのかを判断する。

### 帯域外データ

ストリームが完了するのを待たずに、キューイングされたストリームに割り込むことができる。この場合、緊急 (urgent) と指定したデータを使う。それによって受信側プログラムが緊急データをすぐさま処理すべきであることを知らせる。その処理が終了すると、もとのストリーム・キューの処理を再開する。例えば、リモートログインのセッションにTCPを使っているとき、ユーザーが実行中のプログラムをアボートさせるキーシーケンスを送るときなどに使われる。プログラムが暴走したときなど、そのプログラムの出力を待っているのではなく、強引にアボートさせたいときに必須となる\[23\]。

帯域外データの概念は現在のインターネット向けの設計ではない。緊急ポインタは相手ホストでの処理を変えるものであって、ネットワーク上の処理は何も変わらない。緊急ポインタのあるセグメントがリモートホストに到着したとき、若干異なる2つのプロトコルの解釈があり、単一バイトの帯域外データしか信頼できないという状況になっている。そのため滅多に使われず、実装も貧弱になる傾向がある \[24\]\[25\]。

### 強制的データ送出

通常、TCPは送信すべきデータが[最大セグメントサイズ](https://ja.wikipedia.org/wiki/最大セグメントサイズ "wikilink") (MSS) まで溜まるか、200ミリ秒経過するまで待つ（[Nagleアルゴリズム](https://ja.wikipedia.org/wiki/Nagleアルゴリズム "wikilink")で小さいメッセージを単一パケットにまとめようとするため）。これは例えばファイル転送のような一定の送信が要求される場合に問題となることがある。例えば、送信ブロックが一般的な4KBで、MSSも一般的な1460バイトだとする。すると1ブロックが3セグメントで送信され、最後の1セグメントはMSSに満たないことになる。すると、2パケットまでは約1.2ミリ秒で送信され、1176バイトの3パケット目は197ミリ秒待ってから送信ということになる。

[Telnet](../Page/Telnet.md "wikilink")の場合、ユーザーがキーを押下するたびに通信先からエコーバックされて画面に文字が表示される。すると、1文字押下するたびに200ミリ秒待たされることになり、非常にストレスになる。

この場合、[ソケットのオプション](../Page/ソケット_\(BSD\).md "wikilink") `TCP_NODELAY` を使ってデフォルトの200ミリ秒の送信遅延を変更することができる。

RFCには `PSH` フラグを使って「受信側TCPスタックでそのデータを即座にアプリケーションに送る」という機能が定義されている\[26\]。しかし[ソケットにはこれを制御するインタフェースがなく](../Page/ソケット_\(BSD\).md "wikilink")、[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")の実装に任されている\[27\]。

### コネクション終了

コネクション終了フェーズは多くの場合「4ウェイ・[ハンドシェイク](https://ja.wikipedia.org/wiki/ハンドシェイク "wikilink")」を使い、コネクションの双方がそれぞれ独立に終了できる。一方がコネクションを終了したい場合、FINセグメントを送信し、相手がそのACKを返す。相手も同様にFINを送ってACKを受信することでコネクションを終了する。両方のFIN/ACK交換が済むと、最後にACKを送った側（先にFINを送った側）がタイマを設定してタイムアウトするまで当該ポートを別のコネクションに再利用できないようにする。これによって配送が遅れていたパケットが新たなコネクションで受信されて混乱するのを防ぐ。

コネクションは「ハーフオープン」という状態にもでき、一方だけ終了していても、もう一方はデータを送り続けることができる。終了した側はもう一方が終了するまで受信可能の状態を継続する。

コネクション終了を3ウェイ・ハンドシェイクで行うこともでき、ホストAのFIN送信に対してホストBが FIN+ACK で応答し、ホストAがACK応答する\[28\]。実際にはこれが最も一般的である。

両方から同時にFINセグメントを送りあい、双方がACKを返すということもありうる。FIN/ACKシーケンスが並行して行われるため、2ウェイ・ハンドシェイクと呼ぶこともできる。

## 脆弱性

TCPは様々な方法で攻撃される可能性がある。TCPの完全なセキュリティアセスメントの結果は、認識されていた問題の考えうる対策と共に2009年に公表され\[29\]、その後も[IETF内で進められている](../Page/Internet_Engineering_Task_Force.md "wikilink")\[30\]。

### DoS攻撃

[IPスプーフィング](https://ja.wikipedia.org/wiki/IPスプーフィング "wikilink")を使い、悪意を持って作ったSYNパケットを繰り返し送信することで、偽の接続に対処するために対象サーバの多大な量のリソースを消費させることができる。これを [SYN flood](../Page/SYN_flood.md "wikilink") 攻撃と呼ぶ。この問題への対策として提案された方法として、[SYN cookies](../Page/SYN_cookies.md "wikilink") や暗号的パズルがある。[Sockstress](https://ja.wikipedia.org/wiki/:en:Sockstress "wikilink") も類似の攻撃法だが、システムのリソース管理によって効果を和らげることができる\[31\]。オンラインマガジン [Phrack](https://ja.wikipedia.org/wiki/Phrack "wikilink") 66号では、TCPの Persist Timer に存在する脆弱性を利用した改良型[DoS攻撃](../Page/DoS攻撃.md "wikilink")の分析を行っている\[32\]。

### コネクション乗っ取り

TCPセッションを盗聴できパケットをリダイレクトできる攻撃者は、TCPコネクションを乗っ取ることができる。その場合、攻撃者は進行中の通信からシーケンス番号を読み取り、ストリームにおける次のセグメントを装った偽のセグメントを作る。そのような簡単な乗っ取りで、通信中の一方に1つのパケットを誤って受け取らせることができる。受け取ったホストが余分なセグメントへの確認応答をコネクションのもう一方に返すと、同期が失われる。ARPまたはルーティング攻撃を組合わせることで、乗っ取ったTCPコネクションの制御を完全に奪うことができる\[33\]。

RFC 1948 が登場する以前は異なるIPアドレスを真似ることは難しくなく、初期シーケンス番号は容易に推測可能だった。そのため攻撃者はARP/ルーティング攻撃を併用することなく、適当な一連のパケットを受信者に送信し、異なるIPアドレスからのものだと信じさせることができた。その際、偽装したIPアドレスの本来のホストがダウンしていれば十分であり、Dos攻撃でそのホストをダウンさせればよかった。以上のような理由から、初期シーケンス番号のランダムな選択が行われるようになった。

## TCPポート

TCPはポート番号をホスト上の送受信アプリケーションの識別に使う。TCPコネクションの両端に16ビット符号なしのポート番号 (0-65535) が対応付けられており、一部のポート番号は送受信アプリケーションによって予約されている。受信したTCPセグメントは、送信元IPアドレスと送信元ポートと宛先IPアドレスと送信先ポートの組み合わせによって特定のTCPコネクションに属すると識別される。異なる送信元ポートから同じ送信先ポートへのコネクションを複数同時に確立できるので、サーバは複数のクライアントに対して同時にサービスを提供できる。

ポート番号は大きく3つに分類されており、ウェルノウン (well-known)、レジスタード (registered)、ダイナミック/プライベート (dynamic/private) がある。ウェルノウンポート番号は [Internet Assigned Numbers Authority](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") (IANA) が割り当てを行っており、主にシステムレベルや重要なプロセスで使われている。サーバとして動作する有名なアプリケーションは、それらのポートを使いコネクション確立要求を待ち受けているのが一般的である。例えば、[FTP](../Page/File_Transfer_Protocol.md "wikilink") (20, 21)、[SSH](../Page/Secure_Shell.md "wikilink") (22)、[TELNET](../Page/Telnet.md "wikilink") (23)、[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink") (25)、[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") (80) などがある。レジスタードポート番号は一般にエンドユーザー用アプリケーションが送信元の[エフェメラルポート](https://ja.wikipedia.org/wiki/エフェメラルポート "wikilink")としてサーバに接続するのに使うが、サードパーティが登録した名前を持ったサービスの識別にも使われている。ダイナミック/プライベートポート番号もエンドユーザーのアプリケーションで使えるが、一般にそのような使い方は少ない。ダイナミック/プライベートポート番号は、それを使っている特定のTCPコネクションでしか意味を持たない。

## 発展

TCPは複雑なプロトコルである。長年重大な改良が実施されたり提案されたりしてきたが、1974年に RFC 675 で最初の仕様が登場し、1981年9月に RFC 793 でバージョン4が登場して以来、基本的動作はほとんど変わっていない。RFC 1122 (Host Requirements for Internet Hosts) はTCPプロトコルの実装時の要求仕様を何点か明確にし、近年最も重要なTCP関連のRFCの1つである RFC 2581 (TCP Congestion Control) は輻輳を防ぐための新たなアルゴリズムを提示している。2001年、RFC 3168 で (ECN) が提示された。

当初のは "TCP Tahoe" と呼ばれているが、代替アルゴリズムも多数提案されている（[TCP Reno](https://ja.wikipedia.org/wiki/:en:TCP_Reno "wikilink")、[TCP Vegas](https://ja.wikipedia.org/wiki/:en:TCP_Vegas "wikilink")、[FAST TCP](https://ja.wikipedia.org/wiki/:en:FAST_TCP "wikilink")、[TCP New Reno](https://ja.wikipedia.org/wiki/:en:TCP_New_Reno "wikilink")、[TCP Hybla](https://ja.wikipedia.org/wiki/:en:TCP_Hybla "wikilink") など）。

Multipath TCP (MPTCP)\[34\]\[35\]は[IETFで近年進行中の改良で](../Page/Internet_Engineering_Task_Force.md "wikilink")、リソース利用効率と冗長性を高めるためにTCPコネクションを複数経路にする試みである。Multipath TCP による冗長性は、無線ネットワークでリソースの[統計多重化](https://ja.wikipedia.org/wiki/統計多重化 "wikilink")を可能にし、TCPのスループットを劇的に高める\[36\]。Multipath TCP はデータセンター環境にも性能面の利点をもたらす\[37\]。Multipath TCP の[リファレンス実装](../Page/リファレンス実装.md "wikilink")\[38\]が[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")向けに開発されている\[39\]。

[TCP Cookie Transactions](https://ja.wikipedia.org/wiki/:en:TCP_Cookie_Transactions "wikilink") (TCPCT) は2009年12月に提案された拡張で、サーバをDoS攻撃から守ることを意図している。[SYN cookies](../Page/SYN_cookies.md "wikilink") とは異なり、TCPCTはウィンドウスケーリングなどの他のTCP拡張と共存できる。TCPCTは、短命なTCPコネクションをサーバが多数処理しなければならない[DNSSECでの必要から設計された](https://ja.wikipedia.org/wiki/DNS_Security_Extensions "wikilink")。

[tcpcrypt](https://ja.wikipedia.org/wiki/:en:tcpcrypt "wikilink") は2010年7月に提案された拡張で、TCP自身で直接暗号化するものである。透過的に動作可能なように設計されており、設定変更は不要である。[TLS](../Page/Transport_Layer_Security.md "wikilink") (SSL) とは異なり、tcpcrypt 自体は認証機構を持たないが、そのための簡単なプリミティブをアプリケーションに提供する。2010年現在、[IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") による最初のドラフトが公表されており、いくつかの主要プラットフォームでの実装が存在する。

## 無線ネットワークでのTCP

TCPは有線ネットワーク向けに最適化されてきた。一般にパケット喪失は[ネットワーク輻輳の結果と判断され](https://ja.wikipedia.org/wiki/輻輳制御 "wikilink")、予防のために輻輳ウィンドウサイズが大幅に縮小される。しかし無線の場合、減衰、影に入る、[ハンドオーバー](../Page/ハンドオーバー.md "wikilink")などの無線特有の原因でパケットを喪失することがあり、輻輳が原因とは限らない。無線パケット喪失による（誤った）輻輳ウィンドウサイズ縮小後、輻輳回避のための保守的なウィンドウサイズの縮小も行われる可能性がある。これにより無線リンクの効率が低下する。このような問題への対策が広く研究されている。提案されている対策としては、エンドツーエンド型の対策（クライアントとサーバの修正が必要）\[40\]と[リンク層](../Page/リンク層.md "wikilink")の対策（[RLPなど](https://ja.wikipedia.org/wiki/:en:Radio_Link_Protocol "wikilink")）とプロキシを使った対策（端点以外のネットワークの何らかの変更が必要）\[41\]\[42\]がある。

## デバッグ

[LANアナライザ](../Page/LANアナライザ.md "wikilink")はネットワークリンク上のTCPトラフィックをインターセプトできる機器で、リンク上を通るパケットの内容を表示でき、ネットワーク、プロトコルスタック、TCPを使っているアプリケーションの[デバッグ](../Page/デバッグ.md "wikilink")に有効である。一部の実装ではソケットの `setsockopt()` で `SO_DEBUG` オプションを指定でき、全パケット、TCPのステータス、ソケット上のイベントなどを出力でき、デバッグに有効である。他に、[netstat](https://ja.wikipedia.org/wiki/netstat "wikilink")もデバッグに使われる。

## 代替となる選択肢

TCPの多くの用途は適切とはいえない。（少なくとも通常の実装での）最大の問題は、喪失パケットの再送を受信してからでないと受信済みの後続のパケットをアプリケーションで利用できない点である。特に[ストリーミング](../Page/ストリーミング.md "wikilink")、オンラインゲーム、[VoIP](../Page/VoIP.md "wikilink")などのリアルタイム型アプリケーションで重要な問題であり、データの順序性よりも適時性が重要である。

歴史的・性能的理由により、[ストレージエリアネットワーク](../Page/ストレージエリアネットワーク.md "wikilink") (SAN) はTCP/IPよりも[ファイバーチャネル](../Page/ファイバーチャネル.md "wikilink")プロトコルを採用することが多い。

[組み込みシステム](../Page/組み込みシステム.md "wikilink")でも、[ネットワークブート](https://ja.wikipedia.org/wiki/ネットワークブート "wikilink")や多数のクライアントからの簡単な要求を受け付けるサーバ（例えば[DNSサーバ](../Page/Domain_Name_System.md "wikilink")）でTCPの複雑さが問題となる可能性がある。さらには、[STUN](https://ja.wikipedia.org/wiki/STUN "wikilink")などの [NAT traversal](../Page/NAT_traversal.md "wikilink") 技法では相対的に複雑なTCPを使わずに、遥かに単純な方法で実現している。

一般にTCPが適さない場合は [User Datagram Protocol](../Page/User_Datagram_Protocol.md "wikilink") (UDP) を使用する。UDPはTCPと同様にアプリケーション[多重化](../Page/多重化.md "wikilink")と検査合計機構を提供するが、ストリームの構築や再送を行わず、アプリケーションにそういった機能の実装を任せている。

[SCTPは](../Page/Stream_Control_Transmission_Protocol.md "wikilink")、TCPとよく似たストリーム指向のサービスを提供するプロトコルである。TCPより新しくさらに複雑であり、広く普及したとは言い難い。しかし、信頼性とリアルタイム性を同時に必要とする用途を意図して設計されている。

TCPは広帯域環境でも問題を抱えている。は、送信者が事前にわからない場当たり的な環境ではうまく機能するが、通信パターンが予測可能な環境では [Asynchronous Transfer Mode](../Page/Asynchronous_Transfer_Mode.md "wikilink") (ATM) のようなタイミングに基づくプロトコルの方がオーバーヘッドが小さく、うまく機能する。

## 検査合計の計算

### IPv4でのTCP検査合計

[IPv4](../Page/IPv4.md "wikilink")上のTCPの場合、検査合計計算法は RFC 793 で定義されている。

> 検査合計・フィールドは、ヘッダおよびテキストの全16ビットワードの1の補数の総和の1の補数の下位16ビットである。オクテット数が奇数の場合、最後のオクテットの右にゼロの列をパディングして16ビットワードにしてから検査合計を計算する。このパディングはセグメントの一部として送信することはない。検査合計計算時、検査合計・フィールド自体はゼロとして計算する。

言い換えれば、正しくパディングした後、全16ビットワードを[1の補数表現で加算していく](https://ja.wikipedia.org/wiki/符号付数値表現#1の補数 "wikilink")。そして総和をビット毎に反転して検査合計・フィールドに挿入する。検査合計計算時には、IPv4パケットヘッダを真似た擬似ヘッダも含めて行うことになっている。擬似ヘッダを含めた検査合計計算範囲を以下に示す。

<table>
<caption>検査合計計算用TCP擬似ヘッダ (IPv4)</caption>
<colgroup>
<col style="width: 12%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 22%" />
<col style="width: 44%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ビットオフセット</p></th>
<th><p>0–3</p></th>
<th><p>4–7</p></th>
<th><p>8–15</p></th>
<th><p>16–31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>送信元<a href="../Page/IPアドレス.md" title="wikilink">IPアドレス</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>32</p></td>
<td><p>あて先<a href="../Page/IPアドレス.md" title="wikilink">IPアドレス</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>64</p></td>
<td><p>ゼロ</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/プロトコル番号" title="wikilink">プロトコル番号</a> (6)</p></td>
<td><p>パケット長</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>96</p></td>
<td><p>送信元ポート</p></td>
<td><p>送信先ポート</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>128</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/シーケンス番号" title="wikilink">シーケンス番号</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>160</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/確認応答番号" title="wikilink">確認応答番号</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>192</p></td>
<td><p>ヘッダ長</p></td>
<td><p>予約</p></td>
<td><p>フラグ群</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ウィンドウサイズ" title="wikilink">ウィンドウサイズ</a></p></td>
</tr>
<tr class="even">
<td><p>224</p></td>
<td><p>検査合計</p></td>
<td><p>緊急ポインタ</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>256</p></td>
<td><p>オプション（あれば）</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>256/288+</p></td>
<td><p> <br />
データ<br />
 </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

上のピンクの部分はIPv4ヘッダの一部である。[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")はTCPでは 6 である。パケット長はTCPヘッダとデータの合計の長さである。

### IPv6でのTCP検査合計

[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")上のTCPの場合、検査合計計算法は RFC 2460 で示すように変更されている。

> 検査合計計算にIPヘッダのアドレスを含める上位層のプロトコルでは、IPv4の32ビットアドレスの代わりにIPv6の128ビットのアドレスを使うよう変更しなければならない。

検査合計計算で使うIPv6ヘッダを真似た擬似ヘッダは次のようになる。

<table style="width:100%;">
<caption>検査合計計算用TCP擬似ヘッダ (IPv6)</caption>
<colgroup>
<col style="width: 12%" />
<col style="width: 22%" />
<col style="width: 22%" />
<col style="width: 22%" />
<col style="width: 22%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bit offset</p></th>
<th><p>0 - 7</p></th>
<th><p>8–15</p></th>
<th><p>16–23</p></th>
<th><p>24–31</p></th>
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
<td><p>パケット長</p></td>
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
<td><p>送信元ポート</p></td>
<td><p>送信先ポート</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>352</p></td>
<td><p>シーケンス番号</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>384</p></td>
<td><p>確認応答番号</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>416</p></td>
<td><p>ヘッダ長</p></td>
<td><p>予約</p></td>
<td><p>フラグ</p></td>
<td><p>ウィンドウサイズ</p></td>
</tr>
<tr class="odd">
<td><p>448</p></td>
<td><p>検査合計</p></td>
<td><p>緊急ポインタ</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>480</p></td>
<td><p>オプション（あれば）</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>480/512+</p></td>
<td><p> <br />
データ<br />
 </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - 送信元IPアドレス - IPv6ヘッダにあるもの
  - あて先IPアドレス - 最終送信先。ルーティングヘッダがある場合、TCPは最終のあて先アドレスを使用する。発信元ノードでは、そのアドレスはルーティングヘッダの最後の要素にあり、受信側ではIPv6ヘッダの着信アドレスフィールドにある。
  - パケット長 - TCPのヘッダとデータをあわせた全長
  - 次のヘッダ - TCPの[プロトコル番号](https://ja.wikipedia.org/wiki/プロトコル番号 "wikilink")

### 検査合計・オフロード

多くのTCP/IPスタック実装では、[ネットワークカード](../Page/ネットワークカード.md "wikilink")による自動検査合計計算を補助的に使うオプションを用意している。これによりCPUサイクルを検査合計計算に費やすコストを低減でき、ネットワーク性能を向上させることができる。

なお、送信時に検査合計計算をネットワークカードに任せていると、[LANアナライザ](../Page/LANアナライザ.md "wikilink")が検査合計エラーを検出することがある。

## 脚注・出典

## 参考文献

  - [W. Richard Stevens](../Page/W・リチャード・スティーヴンス.md "wikilink"). TCP/IP Illustrated, Volume 1: The Protocols. ISBN 0-201-63346-9
  - [W. Richard Stevens](../Page/W・リチャード・スティーヴンス.md "wikilink") and Gary R. Wright. TCP/IP Illustrated, Volume 2: The Implementation. ISBN 0-201-63354-X
  - [W. Richard Stevens](../Page/W・リチャード・スティーヴンス.md "wikilink"). TCP/IP Illustrated, Volume 3: [TCP for Transactions](https://ja.wikipedia.org/wiki/:en:T/TCP "wikilink"), [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink"), [NNTP](../Page/Network_News_Transfer_Protocol.md "wikilink"), and the [UNIX Domain](https://ja.wikipedia.org/wiki/:en:unix_domain_sockets "wikilink") Protocols. ISBN 0-201-63495-3

## 関連項目

  - [ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")
  - [TCPやUDPにおけるポート番号の一覧](https://ja.wikipedia.org/wiki/TCPやUDPにおけるポート番号の一覧 "wikilink")
  - [Maximum Transmission Unit](../Page/Maximum_Transmission_Unit.md "wikilink") (MTU)
  - [最大セグメントサイズ](https://ja.wikipedia.org/wiki/最大セグメントサイズ "wikilink") (MSS)
  - [SYN flood](../Page/SYN_flood.md "wikilink")
  - [SYN cookies](../Page/SYN_cookies.md "wikilink")
  - [Stream Control Transmission Protocol](../Page/Stream_Control_Transmission_Protocol.md "wikilink") (SCTP)
  - [トランスポート層](../Page/トランスポート層.md "wikilink")
  - [エンドツーエンド原理](../Page/エンドツーエンド原理.md "wikilink")
  - [二人の将軍問題](https://ja.wikipedia.org/wiki/二人の将軍問題 "wikilink")
  - [ウィンドウサイズ](https://ja.wikipedia.org/wiki/ウィンドウサイズ "wikilink") - [スライディングウィンドウ](https://ja.wikipedia.org/wiki/スライディングウィンドウ "wikilink") - [フロー制御](https://ja.wikipedia.org/wiki/フロー制御 "wikilink")
  - [Bufferbloat](https://ja.wikipedia.org/wiki/Bufferbloat "wikilink")

## 外部リンク

### RFC

  - RFC 675 - Specification of Internet Transmission Control Program 1974年12月版
  - RFC 793 - Transmission Control Protocol (TCP v4)
  - RFC 813 - Window and Acknowledgement Strategy in TCP
  - RFC 1122 - Requirements for Internet Hosts -- Communication Layers (TCP に関する細かい修正が含まれている)
  - RFC 1323 - TCP Extensions for High Performance
  - RFC 1379 - Extending TCP for Transactions—Concepts
  - RFC 1948 - Defending Against Sequence Number Attacks
  - RFC 2018 - TCP Selective Acknowledgment Options
  - RFC 2988 - Computing TCP's Retransmission Timer
  - RFC 3390 - Increasing TCP's Initial Window
  - RFC 3782 - The NewReno Modification to TCP's Fast Recovery Algorithm
  - RFC 4614 - A Roadmap for TCP Specification Documents
  - RFC 5681 - TCP Congestion Control

### その他

  - [Oral history interview with Robert E. Kahn](https://conservancy.umn.edu/handle/11299/107387), [Charles Babbage Institute](https://ja.wikipedia.org/wiki/チャールズ・バベッジ研究所 "wikilink"), University of Minnesota, Minneapolis.
  - [John Kristoff's Overview of TCP](https://condor.depaul.edu/~jkristof/technotes/tcp.html) - TCPの基本概念とデータ転送動作について
  - [TCP, Transmission Control Protocol](http://www.networksorcery.com/enp/protocol/tcp.htm)
  - [Compute 16-bit One's Complement Sum](http://mathforum.org/library/drmath/view/54379.html) - 検査合計の例
  - [TCP tutorial](http://www.ssfnet.org/Exchange/tcp/tcpTutorialNotes.html)
  - [Linktionary on TCP segments](https://www.linktionary.com/s/segment_tcp.html)

[Category:Transmission_Control_Protocol](https://ja.wikipedia.org/wiki/Category:Transmission_Control_Protocol "wikilink") [Category:トランスポート層プロトコル](https://ja.wikipedia.org/wiki/Category:トランスポート層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.
2.
3.
4.  [TCP (Linktionary term)](http://www.linktionary.com/t/tcp.html)
5.  [RFC 791 - section 2.1](http://tools.ietf.org/html/rfc791#section-2.1)
6.  [RFC 793](http://tools.ietf.org/html/rfc793)
7.  RFC 793 section 3.1
8.  [RFC 1323, TCP Extensions for High Performance, Section 2.2](http://tools.ietf.org/html/rfc1323#page-9)
9.  [RFC 2018, TCP Selective Acknowledgement Options, Section 2](http://tools.ietf.org/html/rfc2018#section-2)
10. [RFC 2018, TCP Selective Acknowledgement Options, Section 3](http://tools.ietf.org/html/rfc2018#section-3)
11. [RFC 1323, TCP Extensions for High Performance, Section 3.2](http://tools.ietf.org/html/rfc1323#page-11)
12. [RFC 1146, TCP Alternate Checksum Options](http://tools.ietf.org/html/rfc1146#page-2)
13. RFC 793 Section 3.2
14.
15.
16.
17.
18.
19.
20.
21. [RFC 879](http://www.faqs.org/rfcs/rfc879.html)
22. [TCP window scaling and broken routers](http://lwn.net/Articles/92727/) lwn.net
23.
24.
25.
26.
27.
28.
29. [Security Assessment of the Transmission Control Protocol (TCP)](http://www.cgisecurity.com/2009/02/security-assessment-of-the-transmission-control-protocol-tcp.html)
30. [Security Assessment of the Transmission Control Protocol (TCP)](http://tools.ietf.org/html/draft-ietf-tcpm-tcp-security)
31. <http://www.gont.com.ar/talks/hacklu2009/fgont-hacklu2009-tcp-security.pdf> Some insights about the recent TCP DoS (Denial of Service) vulnerabilities
32. [Exploiting TCP and the Persist Timer Infiniteness](http://phrack.org/issues.html?issue=66&id=9#article)
33. [Laurent Joncheray, *Simple Active Attack Against TCP*, 1995](http://www.usenix.org/publications/library/proceedings/security95/joncheray.html)
34. [Architectural Guidelines for Multipath TCP Development draft-ietf-mptcp-architecture](http://tools.ietf.org/html/draft-ietf-mptcp-architecture-03)
35. [TCP Extensions for Multipath Operation with Multiple Addresses draft-ietf-mptcp-multiaddressed-03](http://tools.ietf.org/html/draft-ietf-mptcp-multiaddressed-03)
36. [TCP with feed-forward source coding for wireless downlink networks](http://portal.acm.org/citation.cfm?id=1794199)
37.
38. [MultiPath TCP - Linux Kernel implementation](http://mptcp.info.ucl.ac.be)
39.
40.
41.
42.