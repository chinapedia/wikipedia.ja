> この記事は[Ping](https://ja.wikipedia.org/wiki/Ping)から翻訳されています。


****（ピンまたはピング）は[IPネットワークにおいて](../Page/Internet_Protocol.md "wikilink")、[ノードの到達性を確認するための](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。IPネットワークにおける基本的なツールの一つであり、組み込み[ネットワーク管理](../Page/ネットワーク管理.md "wikilink")ソフトウェアを含む、ネットワーク機能が実装されている[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のほとんどにおいて、何らかの形で用意されている。

pingは、発信元のホストから宛先のコンピュータにメッセージを送信し、宛先がそれに対して返した応答が戻って来るまでの[ラウンドトリップタイム](https://ja.wikipedia.org/wiki/ラウンドトリップタイム "wikilink")（RTT、往復時間）を測定する。この名前は、音波の[パルスを送信して反射音を聴取することで水中の物体を検出する](https://ja.wikipedia.org/wiki/パルス波 "wikilink")[アクティブソナーの用語に由来している](https://ja.wikipedia.org/wiki/ソナー#アクティブソナー "wikilink")\[1\]。

pingは[ICMPの](../Page/Internet_Control_Message_Protocol.md "wikilink")"echo request"[パケット](../Page/パケット.md "wikilink")を対象ホストに送信し、対象ホストから"echo reply"が返って来ることで到達性を確認する。プログラムは、エラー、[パケットロス](https://ja.wikipedia.org/wiki/パケットロス "wikilink")率、結果の統計的要約（通常は最小、最大、[平均](../Page/平均.md "wikilink")のラウンドトリップタイム）を報告する。

これらは対象ノード間の回線状況を知るため重要な情報である。前日までアクセス可能だったサイトがアクセス不能・困難になった時に原因や状況を調べるのに有効なツールである。pingが通るということは、「少なくとも双方向にIPパケットが通り、対象から応答があった」事を示す。[ドメイン名](../Page/ドメイン名.md "wikilink")をノード名としてパケットを投げて正常にリプライされた場合は、[DNS](https://ja.wikipedia.org/wiki/DNS "wikilink")の障害もないことが確認できる。例えばウェブサイトが閲覧できなくなっている場合、ウェブサーバのドメイン名でpingを打ち正常に応答があれば、ネットワークもDNSも正常と判断されるので、より高レベルに位置するソフトウェア側に問題が起きていると推測できる。つまり自身か相手のファイアウォールでhttp通信をブロックされているかもしれないし、相手のWWWサーバソフトウェアに障害が起きている可能性がある。一部の[オンラインソフト](https://ja.wikipedia.org/wiki/オンラインソフト "wikilink")にもping機能を持つものがある。

pingユーティリティのコマンドラインオプションとその出力は、実装によって異なる。ペイロードのサイズ、試行回数、パケットを通過させるネットワークホップ数([TTL](../Page/Time_to_live.md "wikilink"))の制限、試行間隔などをオプションとして指定できる。多くのシステムでは、[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")ネットワークで同様のテストをするための、[ICMPv6](https://ja.wikipedia.org/wiki/ICMPv6 "wikilink")を実装したユーティリティ"ping6"を提供している。

オンラインゲームなどにおいて、サーバーとプレイヤー（クライアント）間の通信タイムラグをpingとして表示するものもある。また、短時間で切断されるような特殊なセッションを定期的なpingによって強制的に保持するという使い方もある。

## 歴史

pingは、[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")12月に、当時[アメリカ陸軍](../Page/アメリカ陸軍.md "wikilink")[弾道研究所](https://ja.wikipedia.org/wiki/弾道研究所 "wikilink")（現 ）に勤務していた[マイク・ムース](https://ja.wikipedia.org/wiki/マイク・ムース "wikilink")が、自身の管理するIPネットワークでのトラブルシュート用に作成した。これは、後に[NTPを開発した](../Page/Network_Time_Protocol.md "wikilink")[デイヴィッド・L・ミルズ](https://ja.wikipedia.org/wiki/デイヴィッド・L・ミルズ "wikilink")の、IPネットワークの診断と測定にICMPエコーパケットを使用することについての発言に触発されたものである\[2\]。ムースは、その挙動が[潜水艦](../Page/潜水艦.md "wikilink")などで使われるアクティブソナーの発する音波（＝ping）の挙動と似ていることから、このプログラムをpingと名づけた\[3\]\[4\]。この事からpingを実行する事を「pingを打つ」と呼ぶ場合が多い。ムースはpingが何かの略語であることを否定しているが、ミルズにより"packet internet groper"、別の人より"packet internet gopher"という[バクロニム](../Page/バクロニム.md "wikilink")を授かっている\[5\]。

最初にリリースされたバージョンは[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")だったが、後に[BSDライセンス](../Page/BSDライセンス.md "wikilink")の下でライセンスされるようになった。pingは[4.3BSD](https://ja.wikipedia.org/wiki/4.3BSD "wikilink")に最初から含まれていた\[6\]。

RFC 1122 では、どのホストもICMP echo requestを処理し、echo replyを返送する必要があると規定している\[7\]。しかし、セキュリティ上の理由から、これはしばしば無効になっている\[8\]。

インターネットの接続性の問題の“診断”にも有用なpingであったが、[2003年](../Page/2003年.md "wikilink")末、[Welchia](https://ja.wikipedia.org/wiki/Welchia "wikilink")のようなpingをネットワークにフラッドし標的を探すタイプの[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")が出現したり、悪意を持ったユーザが攻撃目標の調査やネットワークに負荷をかけるなどの目的でpingの悪用を行ったため、一部の[ISPでICMP](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") Type 8（echo request）パケットが[フィルタリング](https://ja.wikipedia.org/wiki/フィルタリング "wikilink")されるようになった。

## pingの出力例

<u>下線</u>は利用者が入力する部分

### Linux

以下の出力例は[Linux](../Page/Linux.md "wikilink")端末から`www.google.com`へ、iputilsバージョンのpingからpingを打った結果である。

`$ `<u>`ping www.google.com`</u>
`PING www.l.google.com (64.233.183.103) 56(84) bytes of data.`
`64 bytes from 64.233.183.103: icmp_seq=1 ttl=246 time=22.2 ms`
`64 bytes from 64.233.183.103: icmp_seq=2 ttl=245 time=25.3 ms`
`64 bytes from 64.233.183.103: icmp_seq=3 ttl=245 time=22.7 ms`
`64 bytes from 64.233.183.103: icmp_seq=4 ttl=246 time=25.6 ms`
`64 bytes from 64.233.183.103: icmp_seq=5 ttl=246 time=25.3 ms`
`64 bytes from 64.233.183.103: icmp_seq=6 ttl=245 time=25.4 ms`
`64 bytes from 64.233.183.103: icmp_seq=7 ttl=245 time=25.4 ms`
`64 bytes from 64.233.183.103: icmp_seq=8 ttl=245 time=21.8 ms`
`64 bytes from 64.233.183.103: icmp_seq=9 ttl=245 time=25.7 ms`
`64 bytes from 64.233.183.103: icmp_seq=10 ttl=246 time=21.9 ms`

`--- www.l.google.com ping statistics ---`
`10 packets transmitted, 10 received, 0% packet loss, time 9008ms`
`rtt min/avg/max/mdev = 21.896/24.187/25.718/1.619 ms`

出力例からわかることは、まず`www.google.com`というホスト名が[DNSのCNAMEレコードにより](../Page/Domain_Name_System.md "wikilink")`www.l.google.com`へ誘導され、`64.233.183.103`という[IPアドレス](../Page/IPアドレス.md "wikilink")にリゾルブされている。そして`64.233.183.103`に向けて10回pingが打たれており（Linuxの場合はデフォルトでは割込み文字を打って止めるまで、ずっとpingが打たれる設定となっている）、出力の最後にpingの結果が出ている。

結果からわかることは以下の通りである。

  - パケットは10回送信され、10回とも受信された。パケットロスは0%である。
  - ラウンドトリップタイムは最短21.896ミリ秒（1ミリ秒=1/1000秒）、平均24.187ミリ秒、最長25.718ミリ秒、平均偏差は1.619ミリ秒である。

### macOS

以下の出力例は[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")端末から`www.google.com`へ、ターミナルのコマンドpingからpingを打った結果である。 ただし、computernameはコンピューター名、usernameはユーザー名である（Macintosh HD→アプリケーション→ユーティリティ→ターミナル）。

`computername:~ username$ `<u>`ping www.google.com`</u>
`PING www.l.google.com (66.249.89.104): 56 data bytes`
`64 bytes from 66.249.89.104: icmp_seq=1 ttl=238 time=30.556 ms`
`64 bytes from 66.249.89.104: icmp_seq=2 ttl=238 time=30.412 ms`
`64 bytes from 66.249.89.104: icmp_seq=3 ttl=238 time=31.272 ms`
`64 bytes from 66.249.89.104: icmp_seq=4 ttl=238 time=30.121 ms`
`64 bytes from 66.249.89.104: icmp_seq=5 ttl=238 time=30.942 ms`
`64 bytes from 66.249.89.104: icmp_seq=6 ttl=238 time=32.132 ms`
`64 bytes from 66.249.89.104: icmp_seq=7 ttl=238 time=30.680 ms`
`64 bytes from 66.249.89.104: icmp_seq=8 ttl=238 time=32.614 ms`
`64 bytes from 66.249.89.104: icmp_seq=9 ttl=238 time=29.405 ms`
`64 bytes from 66.249.89.104: icmp_seq=10 ttl=238 time=41.360 ms`
`64 bytes from 66.249.89.104: icmp_seq=11 ttl=238 time=32.176 ms`
`64 bytes from 66.249.89.104: icmp_seq=12 ttl=238 time=32.321 ms`
`^C`
`--- www.l.google.com ping statistics ---`
`13 packets transmitted, 12 packets received, 7% packet loss`
`round-trip min/avg/max/stddev = 29.405/31.999/41.360/2.978 ms`

macOSは[UNIX](../Page/UNIX.md "wikilink")であるため、[Linux](../Page/Linux.md "wikilink")とほぼ変わらない表示である。 今回は-cオプションで回数設定していないため、割込み文字（この例ではControl+C）で止めない限り永遠に続く（例では13回pingを送信）。見方はLinuxの出力例を参考。

logから分かる事は、

  - 13回パケットを送信し、12回受信してロスは、7%である。
  - RTT(ラウンドトリップタイム)は最短29.405ミリ秒(ms)、平均31.999ミリ秒、最長41.360ミリ秒、[標準偏差](../Page/標準偏差.md "wikilink")は2.978ミリ秒である。

### Windows

以下の出力例は[Microsoft Windows XP端末から](../Page/Microsoft_Windows_XP.md "wikilink")`www.google.com`へ、コマンドプロンプト標準のpingを使用してpingを打った結果である (95、98、Me、2000も同様)。

`C:\>`<u>`ping www.google.com`</u>

`Pinging www.l.google.com [64.233.183.103] with 32 bytes of data:`

`Reply from 64.233.183.103: bytes=32 time=25ms TTL=245`
`Reply from 64.233.183.103: bytes=32 time=22ms TTL=245`
`Reply from 64.233.183.103: bytes=32 time=25ms TTL=246`
`Reply from 64.233.183.103: bytes=32 time=22ms TTL=246`

`Ping statistics for 64.233.183.103:`
`    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),`
`Approximate round trip times in milli-seconds:`
`    Minimum = 22ms, Maximum = 25ms, Average = 23ms`

出力例からわかることは、まず`www.google.com`というホスト名がDNSのCNAMEレコードにより`www.l.google.com`へ誘導され、`64.233.183.103`というIPアドレスにリゾルブされている。そして`64.233.183.103`に向けて4回pingが打たれており（Windowsの場合はデフォルトではpingは4回ずつ打たれる設定となっている）、出力の最後にpingの結果が出ている。

結果からわかることは以下の通りである。

  - パケットは4回送信され、4回とも受信された。パケットロスは0%である。
  - ラウンドトリップタイムは最短22ミリ秒、最長25ミリ秒、平均23ミリ秒である。

また、次の出力例は日本版[Microsoft Windows 10端末から](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")`www.google.com`へ、018年10月29日にコマンドプロンプト標準のpingを使用してpingを打った結果である。

`C:\Users\（ユーザー名）>ping www.google.com`

`www.google.com [2404:6800:400a:808::2004]に ping を送信しています 32 バイトのデータ:`
`2404:6800:400a:808::2004 からの応答: 時間 =13ms`
`2404:6800:400a:808::2004 からの応答: 時間 =14ms`
`2404:6800:400a:808::2004 からの応答: 時間 =14ms`
`2404:6800:400a:808::2004 からの応答: 時間 =14ms`

`2404:6800:400a:808::2004 の ping 統計:`
`    パケット数: 送信 = 4、受信 = 4、損失 = 0 (0% の損失)、`
`ラウンド トリップの概算時間 (ミリ秒):`
`    最小 = 13ms、最大 = 14ms、平均 = 13ms`

基本的な部分は上の例と同一だが、www.google.comからリゾルブされたIPアドレスが、IPv6の表示となっている。

## エラー表示

宛先のホストからの応答がない場合、ほとんどの実装では単にタイムアウトを表示するだけだが、一部の実装では、タイムアウトに関する以下のようなエラー通知を定期的に出力する。

  - ホストにアクセスできない

  - ネットワークにアクセスできない

  - プロトコルにアクセスできない

  - 送信元ルートが失敗した

  - [フラグメントが必要](https://ja.wikipedia.org/wiki/IPフラグメンテーション "wikilink")

  - 宛先ネットワークが不明

  - 宛先ホストが不明

  - 送信元ホストが孤立している

  - 宛先ネットワークとの通信が管理上禁止されている

  - 宛先ホストとの通信が管理上禁止されている

  - この[ToSでは](https://ja.wikipedia.org/wiki/Type_of_service "wikilink")、宛先ネットワークに到達できない

  - このToSでは、宛先ホストに到達できない

  - 通信が管理上禁止されている

  - ホスト優先順位違反

  - 優先順位カットオフが有効

エラーが発生した場合、宛先ホストや中間ルータは、"host unreachable"や"TTL exceeded in transit"などのICMPエラーメッセージを返信する。このメッセージには、元のメッセージの最初の8バイト（この場合はICMP echo requestのヘッダ）が含まれているため、pingユーティリティは応答を発信元のクエリーと照合できる\[9\]。

## メッセージのフォーマット

### ICMPパケット

<table>
<caption>IPv4データグラム</caption>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p>Bits 0–7</p></th>
<th><p>Bits 8–15</p></th>
<th><p>Bits 16–23</p></th>
<th><p>Bits 24–31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/IPv4ヘッダ" title="wikilink">ヘッダ</a><br />
(20 bytes)</p></td>
<td><p>バージョン/IHL</p></td>
<td><p>サービスの種類</p></td>
<td><p>長さ</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>識別子</p></td>
<td><p>フラグとオフセット</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Time To Live (TTL)</p></td>
<td><p>Protocol</p></td>
<td><p>ヘッダのチェックサム</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>送信元IPアドレス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>宛先IPアドレス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ICMPヘッダ<br />
（8バイト）</p></td>
<td><p>メッセージの種類</p></td>
<td><p>コード</p></td>
<td><p>チェックサム</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ヘッダデータ</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>| ICMPペイロード<br />
（オプション）</p></td>
<td><p>ペイロードデータ</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<table>
<caption>IPv6データグラム</caption>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p>Bits 0–3</p></th>
<th><p>Bits 4–7</p></th>
<th><p>Bits 8–11</p></th>
<th><p>Bits 12–15</p></th>
<th><p>Bits 16–23</p></th>
<th><p>Bits 24–31</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ヘッダ<br />
（40バイト）</p></td>
<td><p>バージョン</p></td>
<td><p>トラフィッククラス</p></td>
<td><p>フローラベル</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ペイロード長</p></td>
<td><p>次のヘッダ</p></td>
<td><p>ホップリミット</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>送信元アドレス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>宛先アドレス</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ICMP6ヘッダ<br />
（8バイト）</p></td>
<td><p>メッセージの種類</p></td>
<td><p>コード</p></td>
<td><p>チェックサム</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ヘッダデータ</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>| ICMP6ペイロード<br />
（オプション）</p></td>
<td><p>ペイロードデータ</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

ICMPパケットの一般的な構成:\[10\]

  - IPv4ヘッダ（青）: プロトコルは1(ICMP)、サービスタイプは0が設定される。
  - IPv6ヘッダ（青）: 次のヘッダは58(ICMP6)が設定される。
  - ICMPヘッダ（赤）:
      - ICMPメッセージの種類（8ビット）
      - コード（8ビット）
      - チェックサム（16ビット）。パケットのICMP部分で計算される（IPヘッダは使用されない）。Typeフィールドで始まるICMPメッセージの1の補数和の16ビットの1の補数である\[11\]。
      - ヘッダデータ（32ビット）。echo request, replyでは、識別子（16ビット）とシーケンス番号（16ビット）で構成される。
  - ICMPペイロード：様々な種類の回答のペイロード。実装の詳細により任意の長さにすることができる。ただし、IPヘッダとICMPヘッダを含むパケットは、ネットワークの[maximum transmission unit](https://ja.wikipedia.org/wiki/maximum_transmission_unit "wikilink")(MTU)より小さくなければならない。MTUより大きくなると、[フラグメントされる危険性がある](https://ja.wikipedia.org/wiki/IPフラグメント "wikilink")。

###  echo request

*echo request*（エコー要求）は、[ICMP](../Page/Internet_Control_Message_Protocol.md "wikilink")/[ICMP6のメッセージである](https://ja.wikipedia.org/wiki/Internet_Control_Message_Protocol_version_6 "wikilink")。

| 00                                   | 01       | 02        | 03 | 04 | 05 | 06 | 07 | 08 | 09 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| ------------------------------------ | -------- | --------- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| Type = 8(IPv4, ICMP) 128(IPv6,ICMP6) | Code = 0 | ヘッダチェックサム |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 識別子                                  | シーケンス番号  |           |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| ペイロード                                |          |           |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

クライアントは、識別子とシーケンス番号を使用して、応答を要求と一致させることができる。実際には、ほとんどのLinuxシステムはpingプロセスごとに異なる識別子を使用しており、シーケンス番号はそのプロセス内で増加する番号である。Windowsは、Windowsのバージョンによって異なる固定識別子と、起動時にのみリセットされるシーケンス番号を使用する。

###  echo reply

*echo reply*（エコー応答）は、echo requestの応答として生成されるICMPメッセージである。規定では、エコー要求を受信した場合は必ずエコー応答を返信しなければならず、エコー応答にはエコー要求に含まれるペイロードをそのまま含まなければならない。

| 00                                  | 01       | 02        | 03 | 04 | 05 | 06 | 07 | 08 | 09 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 |
| ----------------------------------- | -------- | --------- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| Type = 0(IPv4,ICMP) 129(IPv6,ICMP6) | Code = 0 | ヘッダチェックサム |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| 識別子                                 | シーケンス番号  |           |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| ペイロード                               |          |           |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

識別子とシーケンス番号は、エコー要求と応答を関連付けるためにクライアントで使用される。

### ペイロード

パケットのペイロードは一般に[ASCII](../Page/ASCII.md "wikilink")文字で埋められている。以下に、ICMP echo requestの最後の32バイトの[tcpdump](https://ja.wikipedia.org/wiki/tcpdump "wikilink")ユーティリティによる出力の例を示す（echo requestパケットはから始まり、ICMPヘッダの後にペイロードがある）。  ペイロードには、送信の時間を示すタイムスタンプやシーケンス番号（上記の例では含まれていない）を含むことができる。これにより、pingは各パケットの送信時刻を記録することなく、[ステートレスな方法でラウンドトリップタイムを計算できる](https://ja.wikipedia.org/wiki/ステートレス・プロトコル "wikilink")。

## セキュリティ上の考慮事項

多くのpingの実装には"flood"オプションが存在する。これは、高負荷条件下でのネットワークの応答を判断するために、できるだけ速くリクエストを送信するものである。このオプションは管理者特権を持つユーザに制限されているが、標的の元に大量のICM echo requestが届くようにする[DoS攻撃](../Page/DoS攻撃.md "wikilink")の一種のに使用される可能性がある。

pingは、単にホストの存在を知らせることによって潜在的なターゲットとして確認されるため、セキュリティ上のリスクと見なされている。解決策として、多くのシステムにおいて、 RFC 1122 においてホストは常に返信を返さなければならないという規定を無視して、返信を無効にする手段を提供している\[12\]\[13\]。さらに、pingによって計算されたラウンドトリップ時間は、完全性チェックに欠けていることが多く、そのため、過酷な環境では信頼できない。攻撃者は、ほとんどのping実装で計算された遅延を延長または短縮する可能性がある\[14\] 。

## 関連項目

  - [キープアライブ](https://ja.wikipedia.org/wiki/キープアライブ "wikilink")

  - [UNIXユーティリティの一覧](https://ja.wikipedia.org/wiki/UNIXユーティリティの一覧 "wikilink")

  - [Traceroute](../Page/Traceroute.md "wikilink")

  - [Ping of death](../Page/Ping_of_death.md "wikilink")

  -
  -
  - [Smurf攻撃](https://ja.wikipedia.org/wiki/Smurf攻撃 "wikilink")

## 脚注

### 注釈

### 出典

## 外部リンク

  - [The Story of the PING Program](https://ftp.arl.army.mil/~mike/ping.html) pingの作者であるマイク・ムースの解説（英語）

  - [ping(8)](https://linuxjm.osdn.jp/html/netkit/man8/ping.8.html) man page（JM Project）

  - [ping(1M)](https://nixdoc.net/man-pages/HP-UX/man1m/ping.1m.html) man page（HP-UX リファレンス）

  - [ping コマンド Solaris のシステム管理 (IP サービス)](https://docs.oracle.com/cd/E19455-01/806-2719/6jbtsiffe/index.html)

  - [ping.eu](https://ping.eu/) Ping and other online tools and services オンラインネットワークサービス

  - [MTU, RWINなどの簡単調整(EditMTU)](https://hp.vector.co.jp/authors/VA022090/editmtu/)　Windows95・98・Me・2000・XPで利用可能なユーティリティ(フリーソフト)

      - Windows95で使う場合はWinsock2.0とダイヤルアップネットワーク1.3が必要

  - [Online Ping](http://networktools.nl/ping)

[Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:Windowsのコマンド](https://ja.wikipedia.org/wiki/Category:Windowsのコマンド "wikilink") [Category:ネットワーク・アナライザ](https://ja.wikipedia.org/wiki/Category:ネットワーク・アナライザ "wikilink") [Category:1983年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1983年のソフトウェア "wikilink")

1.
2.  ["The Story of the PING Program"](http://ftp.arl.army.mil/~mike/ping.html), Mike Muuss
3.
4.
5.
6.  <http://www.manpagez.com/man/8/ping/>
7.
8.
9.
10.
11.
12.
13.
14.