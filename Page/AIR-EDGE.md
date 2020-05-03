> この記事は[AIR-EDGE](https://ja.wikipedia.org/wiki/AIR-EDGE)から翻訳されています。


**AIR-EDGE**（エアーエッジ、旧表記**AirH"**） は、ソフトバンク（旧各社名、DDIポケット、[ウィルコム](../Page/ウィルコム.md "wikilink")、[ワイモバイル](../Page/ワイモバイル.md "wikilink")）がDDIポケット時代の[2001年](../Page/2001年.md "wikilink")[6月1日](../Page/6月1日.md "wikilink")より提供している、[PHS](../Page/PHS.md "wikilink")回線を利用した[パケット通信](../Page/パケット通信.md "wikilink")による、定額制または準定額制のIPデータ通信サービスである。多くの場合は[インターネット・サービス・プロバイダ](https://ja.wikipedia.org/wiki/インターネット・サービス・プロバイダ "wikilink") (ISP) への[無線アクセス](../Page/無線アクセス.md "wikilink")として利用されるほか、法人向けに企業LANへのインターネットを介さない閉域サービスを提供することもできる。常時接続ではなく、従来のダイアルアップ同様、オンデマンド接続である。

2018年3月末を以てソフトバンクは[PHS](../Page/PHS.md "wikilink")の新規契約受付を終了しており、本サービスも新規契約は出来ない。

## 概説

このサービスを開始するにあたり、当時PHSサービスを提供していた他の事業者（[ドコモPHS](../Page/ドコモPHS.md "wikilink")、[アステル](../Page/アステル.md "wikilink")）とは異なり、基地局にオンラインで小規模な改良を加えるだけで済んだため、サービス開始当初から、現ワイモバイルのPHS (H") が利用できるほぼ全国のエリアで利用できた。移動体通信での定額データ通信サービスに先鞭をつけ、2004年に当時のウィルコムが世界に先駆けて導入した[音声通話](https://ja.wikipedia.org/wiki/音声通話 "wikilink")用端末でのフルブラウザ定額制も本サービス無くしては実現し得なかったものであり、[2005年](../Page/2005年.md "wikilink")の[音声通話定額制](../Page/音声通話定額制.md "wikilink")の導入と共に音声端末での契約が激減していた同社が復権する原動力となった。他方、基地局への新プログラムを追加していく過程で、メモリ容量を確保するため、需要のなくなった古いサービスのプログラムは一部、削除された。

エアーエッジが利用できる端末には、[PCカード](../Page/PCカード.md "wikilink")や[CFカードなどの形状をしたデータ通信専用の端末と](../Page/コンパクトフラッシュ.md "wikilink")、音声通話用の端末でエアーエッジに対応したものがある。前者には、[PC](../Page/パーソナルコンピュータ.md "wikilink")・[PDAによる音声通話可能なものもある](../Page/携帯情報端末.md "wikilink")。後者は、当初の機種は専用ケーブルでPC等と接続した場合にしかエアーエッジは利用できなかったが、[2003年](../Page/2003年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")に端末でのメールやネット閲覧による通信もエアーエッジで行うようにした「AIR-EDGE PHONE（エアーエッジフォン）」が登場した。また、エアーエッジをモジュールとして[PCなどに内蔵した](../Page/パーソナルコンピュータ.md "wikilink")「AIR-EDGE IN（エアーエッジイン）」というものも存在するほか、法人向けのテレメトリングにも用いられている。

基本的なターゲットは屋外で[ノートパソコン](../Page/ノートパソコン.md "wikilink")やPDAなどを用いた[モバイル](https://ja.wikipedia.org/wiki/モバイル "wikilink")通信を行なうユーザーで、人口カバー率99%以上というウィルコムの完成されたエリアを重視する層である。他方、エリアの面展開は出来ないがより高速な通信が必要で、スポット的に喫茶店などで使えればよいというユーザーには無線LAN(WiFi)という別の選択肢があり、ウィルコム自身が無線LANサービスのオプションを提供している。また、本サービスは無線LANと比べ、最高速度は遅いがエラー率は低く、セキュリティ上の懸念ははるかに低い。

[2005年](../Page/2005年.md "wikilink")[2月2日](../Page/2月2日.md "wikilink")の、DDIポケットがウィルコムへ社名変更した際、エアーエッジの表記も「**AirH"**」から「**AIR-EDGE**」へ変更された。

## 通信方式

エアーエッジは、従来PHSで利用されていたデータ通信方式の[PIAFS](https://ja.wikipedia.org/wiki/PIAFS "wikilink")等と異なり、[パケット通信](../Page/パケット通信.md "wikilink")を行っている。このパケット通信のみを利用する通信方式（パケット方式）と、従来型のPIAFS通信（PHS[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")方式）を併用（自動切替）する通信方式（フレックスチェンジ方式）がある。

なお、通信端末によって、下記の各通信方式に対応・非対応が異なる。

### パケット方式

パケット通信のみ利用する通信方式（「パケット方式」と呼ぶ）では、通信速度（理論値）が下り最大で32kbps・64kbps・128kbps・256kbps（※[W-OAM通信の場合は後述](https://ja.wikipedia.org/wiki/#W-OAM "wikilink")）の4種類があり、それぞれ「1xパケット方式」・「2xパケット方式」・「4xパケット方式」・「8xパケット方式」と呼ぶ。なお「\(n\)x」と言うのは、束ねるチャネルのリンク数の最大値の事である。いずれの方式によるパケット通信も、回線状態により、リンク数を含めて通信速度が変化する「ベストエフォート方式」である。

料金コース「つなぎ放題」では最大2xまで、「新つなぎ放題」では最大8xまでのパケット方式が、それぞれ利用できる。いずれも定額制となる。なお、通信端末についても、最大1x、4x、または8x方式までに対応の別があるため、端末が対応する最大の（「\(n\)xパケット方式」）までしか通信できない。以下同。

一方、料金コース「ネット25」では、準定額制（前述参照）のもとで、1x・4xパケット方式および後述の「フレックスチェンジ方式」を利用できる。「パケコミネット」では、1x・4xパケット方式が利用できるが、「フレックスチェンジ方式」は利用できない。ネット25は法人契約の場合、全社員の利用分を合計して後の課金となるため、ごく一部のユーザが1月に25時間以上つないでも、全体としては準定額制のうちに収まることが多い。ウィルコムは、エアーエッジが簡単には切断されない一方で、強制切断や切断認識のサイクルが複雑化していることから、端末側での体感と課金システム上の接続時間は精密には一致しないことを注意喚起している。

#### W-OAM

なお、[高度化PHS](../Page/高度化PHS.md "wikilink")である「**[W-OAM](../Page/W-OAM.md "wikilink")**」の方式により通信する場合、「1xパケット方式」・「2xパケット方式」・「4xパケット方式」・「8xパケット方式」による速度は、上下とも最大で51kbps・102kbps・204kbps・408kbpsとなる。また、「**W-OAM typeG**」方式では最大で64kbps・128kbps・256kbps・512kbps、[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")回線の[光](../Page/光通信.md "wikilink")[IP化後は最大で](../Page/Internet_Protocol.md "wikilink")100kbps・200kbps・400kbps・800kbpsとなる。

W-OAM / typeG 対応の通信端末および[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")が必要。詳細は[W-OAM](../Page/W-OAM.md "wikilink")の項目を参照。

### フレックスチェンジ方式

パケット通信とPIAFS通信を自動切替する通信方式は「フレックスチェンジ方式」と呼ばれる。これは「ネット25」でのみ利用できる。この方式では、通信負荷に応じて、4xパケット通信と、最大64kbpsのPIAFS通信を自動的に切り替えるというものである。なお、PIAFS通信もベストエフォート（PIAFS2.1および2.2規格）なので、回線状態によっては32kbps (PIAFS) で通信している場合もある。フレックスチェンジ方式対応の通信端末が必要。

### 各通信方式の切替え

各通信方式の間の切替は、[PPP](../Page/Point-to-Point_Protocol.md "wikilink")[ダイヤルアップ](https://ja.wikipedia.org/wiki/ダイヤルアップ "wikilink")先の手動切替による。[プロバイダのアクセスポイント電話番号の最後に](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")、下記の記述子をつけて電話機より発呼する。\#\#で始まる番号を含めてアクセスポイント番号だと思っているユーザが多いが、実は\#\#以降は電話番号の一部ではなく、電話機に対して通信方式を指定する[ATコマンド](https://ja.wikipedia.org/wiki/ATコマンド "wikilink")である。通信方式については、次のような規則により切替えられる。なお、実際の電話番号やダイヤルアップ記述子については、ウィルコムや接続先[プロバイダの](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")[ウェブサイト](../Page/ウェブサイト.md "wikilink")等を参照のこと。

  - 1xパケット方式（通常は\#\#61）
  - フレックスチェンジ方式（通常は\#\#7）
  - 2x、4xまたは8xパケット方式（通常は\#\#64）

なお、多くの機種はPIAFS通信にも対応しており、\#\#4でコールするが、エアーエッジサービスの定額料金制の範疇外となってしまうため、パケット・オンリーの設定を依頼すると、PIAFSではつながらなくなり、誤用を防止できる。エアーエッジがIPにしか対応していないのと異なり、PIAFSであれば[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")を含む、その他のデータ通信形式も利用できる。

## 特長

エアーエッジはパケット通信を行っており、データ通信中にエリア外（圏外）になり物理的なPHS無線回線が切断されても、[ダイヤルアップ](https://ja.wikipedia.org/wiki/ダイヤルアップ "wikilink")[PPPは仮想的に接続状態が保持](../Page/Point-to-Point_Protocol.md "wikilink")（[ドーマント](https://ja.wikipedia.org/wiki/ドーマント "wikilink")状態 ）される。これにより、一定時間後にエリア内（圏内）に戻れば、ユーザから見てダイヤルアップPPPが切断されることなく、データ通信を継続することができるという特徴がある。これにより、通信中のセッションが切断されにくいという意味で安定したデータ通信が可能である。

### 料金（税込）

  - 2010年12月時点

（通則）

  - 「新つなぎ放題」、「つなぎ放題\[PRO\]」、「つなぎ放題\[4x\]」および「つなぎ放題」は、パケット方式の通信が定額制となる。
  - 「ネット25\[PRO\]」ではパケット方式 (1x～8x) の通信が月に25時間まで定額利用できる準定額制となる。なお、25時間の超過分は10.5円/60秒の従量制となる。ただし超過分20,100円以上は課金されない。なお、ネット25でAIR-EDGE PHONEセンター（[AIR-EDGE PHONE端末単体接続専用](https://ja.wikipedia.org/wiki/#AIR-EDGE_PHONE "wikilink")）に接続した場合、月25時間分定額の対象とはならず、別途パケット料金が従量制で掛かる。
  - 「ネット25」ではパケット方式 (1x～4x) およびフレックスチェンジ方式の通信が月に25時間まで定額利用できる準定額制となる。超過分やAIR-EDGE PHONEセンター接続の場合の扱いは「ネット25\[PRO\]」と同様。
  - 「パケコミネット」ではパケット方式の通信が、月200,000パケット（1[パケット](../Page/パケット.md "wikilink")=128[バイトで計算](../Page/バイト_\(情報\).md "wikilink")）まで定額利用でき、超過分は1パケット0.0315円の従量制となる。ただし超過分20,100円以上は課金されない。PDA向けのコースである。
  - なお、いずれの場合も[プロバイダ接続料が別途必要となる](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")。*後述の[\#プロバイダ](https://ja.wikipedia.org/wiki/#プロバイダ "wikilink")参照*。
  - 下記の[W-OAM](../Page/W-OAM.md "wikilink")またはW-OAM typeG通信でも別途の通信料金はかからない。
  - 料金コースの集約化に伴い、今後、データ通信端末でのAIR-EDGE向けの料金コースはパケット方式を問わない「新つなぎ放題」のみとなり、これ以外の料金コースは2011年2月28日（店頭での受付は2010年12月31日）に新規受付を終了する。

各コースで利用できる最大通信速度および料金は、それぞれ次の表のとおりである。

<table>
<thead>
<tr class="header">
<th><p>料金コース</p></th>
<th><p>最大通信速度（上下各、理論値）</p></th>
<th><p>月額料金</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>標準</p></td>
<td><p><a href="../Page/W-OAM.md" title="wikilink">W-OAM</a>時[1]</p></td>
<td><p>W-OAM typeG時[2]</p></td>
<td><p>通常</p></td>
</tr>
<tr class="even">
<td><p>新つなぎ放題</p></td>
<td><p>256k<a href="../Page/ビット毎秒.md" title="wikilink">bps</a> (8x)</p></td>
<td><p>408kbps (8x)</p></td>
<td><p>512～800kbps[3] (8x)</p></td>
</tr>
<tr class="odd">
<td><p>つなぎ放題[PRO]</p></td>
<td><p>256kbps (8x)</p></td>
<td><p>408kbps (8x)</p></td>
<td><p>512～800kbps[4] (8x)</p></td>
</tr>
<tr class="even">
<td><p>つなぎ放題[4x]</p></td>
<td><p>128kbps (4x)</p></td>
<td><p>204kbps (4x)</p></td>
<td><p>256〜400kbps[5] (4x)</p></td>
</tr>
<tr class="odd">
<td><p>つなぎ放題</p></td>
<td><p>64kbps (2x)</p></td>
<td><p>102kbps (2x)</p></td>
<td><p>128〜200kbps[6] (2x)</p></td>
</tr>
<tr class="even">
<td><p>ネット25[PRO]</p></td>
<td><p>256kbps (8x)</p></td>
<td><p>408kbps (8x)</p></td>
<td><p>512～800kbps[7] (8x)</p></td>
</tr>
<tr class="odd">
<td><p>ネット25</p></td>
<td><p>128kbps (4x)<br />
64kbps（フレックスチェンジ方式）</p></td>
<td><p>204kbps (4x)</p></td>
<td><p>256～400kbps[8] (4x)</p></td>
</tr>
<tr class="even">
<td><p>パケコミネット</p></td>
<td><p>128kbps (4x)</p></td>
<td><p>204kbps (4x)</p></td>
<td><p>256～400kbps[9] (4x)</p></td>
</tr>
</tbody>
</table>

（表注）

  - (\(n\)x) ＝ \(n\)xパケット方式。束ねるマルチリンクの数。
    料金コースでの上限リンク数に関わらず、端末が対応する最大のリンク数に制限される。現在、音声端末（[W-SIM](../Page/W-SIM.md "wikilink")端末含む）では最大4xまで。
  - 最大割引時の金額は、年間契約割引＋長期割引＋「A\&B割」で、4割引（契約後3年を越えた場合）が適用された場合の金額。なお「A\&B割」（エービーワリ）とは、既にウィルコム指定プロバイダ（[OCN](../Page/OCN.md "wikilink")や[au one net](https://ja.wikipedia.org/wiki/au_one_net "wikilink")、[Yahoo\!BB](https://ja.wikipedia.org/wiki/Yahoo!BB "wikilink")など、[CATV以外の主要プロバイダはほとんど対象](../Page/ケーブルテレビ.md "wikilink")）の[ADSL](../Page/ADSL.md "wikilink")や[FTTH](../Page/FTTH.md "wikilink")といった、いわゆる[ブロードバンドインターネット接続](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")コースに契約している場合、AIR-EDGEの契約の際にその旨を書き込むと、料金が約15%割引になる制度である。割引は他に「[マルチパック](https://ja.wikipedia.org/wiki/マルチパック "wikilink")」などがある。なお、\[PRO\]の付くコースは長期割引は適用対象外。なお、料金コースを「新つなぎ放題」に絞り込むため、年間契約割引、「A\&B割」、マルチパックは2011年2月28日（店頭での受け付けは2010年12月31日）をもって新規受付を終了する。
  - 音声通話に対応する端末 で通話した場合、標準コース等の音声通話向け料金コースと違い通話1回当りの接続料はかからない\[10\]。

（料金コース）

  - [新ウィルコム定額プラン](https://ja.wikipedia.org/wiki/新ウィルコム定額プラン "wikilink")
      -
        ウィルコムの電話同士の通話が[定額制となる基本料金プラン](../Page/音声通話定額制.md "wikilink")。そのため、基本的には音声端末向けの料金コースである。標準コース等と違い通話1回当りの接続料はかからない\[11\]。なお、willcomドメインのメール送受信についても[定額制が適用される](../Page/メール定額制.md "wikilink")。
        基本料金は月額2,900円。年間契約割引、長期割引、「A\&B割」、データセット割引、複数回線割引などの割引サービスは適用されない。[ファミリーパック](https://ja.wikipedia.org/wiki/ファミリーパック "wikilink")や[マルチパック](https://ja.wikipedia.org/wiki/マルチパック "wikilink")などは適用される。データ通信については定額ではなくパケット料金（0.084円/パケット）が発生するが上限は2800円。

\*\*[新通話パック](https://ja.wikipedia.org/wiki/新通話パック "wikilink")

\*:新ウィルコム定額プラン向けのオプション。1050円で携帯電話や一般加入電話へ2倍の2100円分無料通話ができる。

### プロバイダ

基本的にAIR-EDGEの使用時（後述のAIR-EDGE PHONE等については別途後述する）は、AIR-EDGEの回線契約（および通信料）とは別に、[ISPとの契約](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")（および接続料）が必要である。

このISPについては、WILLCOMの公式ISPサービスであるPRINや、それ以外のISPも別途プロバイダ契約が必要となるが利用可能である。なお、既に自宅などで固定回線にISPを利用している場合には、当該ISPが提供するAIR-EDGE接続サービスを利用すると、場合によっては割安または無料となる場合がある。

### MEGA PLUS（高速化サービス）

エアーエッジでは、高速化サービス「MEGA PLUS」を利用することで、専用サーバを介し、画像を含むデータを圧縮し通信容量を低減した形で通信が可能になる。パソコンに専用クライアントソフトをインストールする必要がある。対応OSは[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")/[Mac](../Page/Macintosh.md "wikilink")。圧縮対応[プロトコル](../Page/プロトコル.md "wikilink")は[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink")/[HTTPS](../Page/HTTPS.md "wikilink")/[POP3](../Page/Post_Office_Protocol.md "wikilink")/[IMAP](../Page/Internet_Message_Access_Protocol.md "wikilink")/[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")/[FTP](../Page/File_Transfer_Protocol.md "wikilink")/[RTSP](../Page/Real_Time_Streaming_Protocol.md "wikilink")（一部OSでは非対応プロトコルあり）。月額利用料は500円・税込で、\[PRO\]の付く料金コースは無料となる。

なお以前は「トルネードweb」(Venturi Client for AirH") として無料提供されており、その改良版として有料提供されたもの。また、2005年1月当初、つなぎ放題/\[4x\]での月額利用料は1050円・税込に設定されていたが、ユーザからの不評などにより、同年9月に500円・税込に統一されたうえ、開始当初から価格改定の間まで無料キャンペーンが継続されたため、幻の料金となった。

このサービスは利用者数の減少により、2010年12月31日をもってサービスを終了することが発表されている。現在利用中のユーザーには他社の類似サービスへの案内を行っている。

## その他

### 通信速度

2006年2月23日、高度化PHS規格「[W-OAM](../Page/W-OAM.md "wikilink")」の導入により、W-OAM対応通信時に最大408kbpsを、また、2007年4月5日の「W-OAM typeG」の導入により、最大512～800kps\[12\]を実現している。通信速度に係るその他の詳細は前述を参照。

よって[W-CDMA](../Page/W-CDMA.md "wikilink")方式による[第3世代移動通信システム](../Page/第3世代移動通信システム.md "wikilink")の標準的な1ユーザ当たり速度（ユーザレート）384kbpsを上回る数値を、理論値ではあるが達成している事になる。

AIR-EDGEは一時期、理論値と比べ遅いという評判が立ったが、これは主として、通信パイプの太さの示す「帯域」が足りないことではなく、一瞬、体感できるほどの反応の遅れ（遅延）があることが理由だった。遅延は現在、網内のアルゴリズムの改善で、大幅に解消されている。また、Venturiを用いた高速化サービスは、PCにプロキシ設定を施すものであるため[IPsec](../Page/IPsec.md "wikilink")クライアントソフトとの相性が悪く、最悪のケースでは社外からLANへの接続ができなくなるため、企業ユーザでは必ずしも好評ではない。

一方、第3世代移動通信システムでも、[第3.5世代移動通信システム](../Page/第3.5世代移動通信システム.md "wikilink")と称する2Mbpsや、それ以上の下り通信速度となるものが、一部でサービス提供中である。これらは、1つの[携帯電話](../Page/携帯電話.md "wikilink")基地局にアクセスが集中すると速度が落ちるという欠点がある。というのも、この「2Mbpsやそれ以上の通信速度」というのは、通常、「1つの基地局が通信できる最高速度」（セルスループット）または、「基地局のセル中の一定角度方向のセル内の部分である1セクタ内で通信できる最高速度」（セクタスループット）であり、それをこの基地局を利用するユーザーで共用するためである。また、携帯電話では、通常、1基地局あたりのカバーエリア（セル半径）が広く（マクロセル）、結果的に収容ユーザ数が多くなるため、セル半径の小さい（マイクロセル）PHSによるエアーエッジと比較して、混雑時のユーザレートの速度低下が顕著になりうる、と言う事をウィルコムでは広告のアピールポイントとして謳っていた。

対して、PHSは通信チャネルが[FDMとされ](https://ja.wikipedia.org/wiki/周波数分割多重化 "wikilink")、日本ではPHS用の帯域内で数10チャンネル（公衆用）の割り当てが可能である。基地局はDCA (Dynamic Cell Assign) により自律分散型で通信チャネルの周波数割り当てを行う。よって通信チャネルの周波数が異なれば、基地局のセルを干渉を起こさずにオーバーラップさせる事は容易である。以上から、単位面積当たりの総スループットについては、マイクロセルによるPHSと、典型的なマクロセルによる[3G](../Page/第3世代移動通信システム.md "wikilink")・[3.5G携帯電話とを比較すると](../Page/第3.5世代移動通信システム.md "wikilink")、理論上は最大で2桁程度、前者が高くする事が可能である。（実際に、高トラフィックな大都市中心部では、それに近いようなレベルで高密度な基地局設置がなされている\[13\]。

これに対して、携帯電話事業者では[3.5G等のさらなる高速化や](../Page/第3.5世代移動通信システム.md "wikilink")、周波数利用効率の向上を目指して開発を続けている。また、[定額制サービスの提供にあたっては](../Page/モバイルデータ通信定額制.md "wikilink")、輻輳対策として、一部のネットワークアプリケーションの制限や、転送量により速度制御を掛けるなどの対策を取る事業者もある。

### PC定額制

通信端末を[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink") (PC) に接続または内蔵して利用したような場合には、音声端末などによる場合と比較して、通信する総データ量が著しく大きくなる（1桁以上）ことが知られている。

2009年1月時点の日本国内で、PCに接続した場合にも料金定額制となるのは、以下のサービスのみである。

  - PHSであるエアーエッジと、[電力系通信事業者](../Page/電力系通信事業者.md "wikilink")の一部PHSサービス（[ケイ・オプティコム](https://ja.wikipedia.org/wiki/ケイ・オプティコム "wikilink")の[eo64エア](https://ja.wikipedia.org/wiki/アステル関西#eo64エア "wikilink")）
  - [イー・モバイル](../Page/イー・モバイル.md "wikilink")による定額制サービス。
  - NTTドコモ（[FOMA](../Page/FOMA.md "wikilink")）- 定額データプランHIGH-SPEED・定額データプラン64K
  - [KDDI](../Page/KDDI.md "wikilink")（[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")） - 「Packet WINシングルサービス」（「WINシングル定額」）

ただし、[2005年](../Page/2005年.md "wikilink")[7月25日](../Page/7月25日.md "wikilink")より、[MVNOによる法人向け](https://ja.wikipedia.org/wiki/仮想移動体通信事業者 "wikilink")[VPNアクセス回線限定ながら](../Page/Virtual_Private_Network.md "wikilink")、ボーダフォン（現[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")）の第3世代携帯電話 (3G) 回線でのPC等外部接続の定額制が[日本通信](https://ja.wikipedia.org/wiki/日本通信 "wikilink")より提供開始された\[14\]。

典型的な第3世代携帯電話やその事業者（NTTドコモ・au・ソフトバンクモバイル）では、1000万人単位の端末単体通信ユーザを抱えているため、混雑時の速度低下や電波帯域の不足、投下設備資本の回収上など問題から、PC定額制の導入が大幅に遅れたと見られている。各社とも、2007年春前後、PDA限定の定額制を一部導入し、（[Biz・ホーダイ](../Page/Biz・ホーダイ.md "wikilink")、[PCサイトダイレクト](https://ja.wikipedia.org/wiki/PCサイトダイレクト "wikilink")等）、さらに3.5Gインフラの拡大や、プロトコル制限・転送量制御などの適用により、導入に踏み切っている。

PHSが早期にPC定額制を実現できているのは、設備投資の点でも携帯電話より安価な上、マイクロセル方式によりトラフィックを分散できるためである。

2007年末までに、[イー・モバイル](../Page/イー・モバイル.md "wikilink")、NTTドコモに続いてKDDIが、PC接続での定額制データ通信サービスへ参入し、この分野での競争激化の本格化が予想されている。他方で、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")のデータ通信量の負担に耐えかね、定額料金制を本音ではやめたがっている携帯電話事業者は少なくないと見られる（実際に、各社のLTEサービスでは、一定のパケット容量を超えた場合は、速度制限がかけられるケースがほとんど）。

*なお料金制度に関しての詳細は[パケット定額制](../Page/パケット定額制.md "wikilink")、[モバイルデータ通信定額制](../Page/モバイルデータ通信定額制.md "wikilink")の各項目も参照のこと。*

### その後

2005年より、主要電話局にITX（IP Transit Exchange、IP中継交換機。[NTT東西回線をバイパスする装置](../Page/NTTグループ.md "wikilink")。[4](http://www.toshiba.co.jp/tech/review/2005/02/60_02pdf/b05.pdf)）の導入が進められており、高トラフィックの都市部に概ね導入されていると言う。ITXにより、バックボーン回線をウィルコムが構築した[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")に切り替えた上で、将来的に各[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")に[光ファイバー](../Page/光ファイバー.md "wikilink")を接続。現在は1チャンネルあたり51kbpsの通信が可能で、[変調方式の高度化](../Page/デジタル変調.md "wikilink") (QAM) により、これを最大96～100kbpsまでに高速化。これを最大16本束ねることで1.5Mbpsのサービスを提供する計画とされている。*（[W-OAM](../Page/W-OAM.md "wikilink")の項目も参照）*

参考：[ウィルコムインタビュー「2つのアプローチで体感数Mbpsを目指す」](http://bb.watch.impress.co.jp/cda/special/8841.html)

### ウィルコム経営再建以降

2007年以降、次世代PHS等の試験や免許取得に向かうが、モバイルブロードバンドである[イー・モバイル](../Page/イー・モバイル.md "wikilink")や[UQコミュニケーションズ](https://ja.wikipedia.org/wiki/UQコミュニケーションズ "wikilink")の参入が相次ぎ、また2009年には経営破綻、経営再建となり、以降は急速に競争力を喪失した。

## AIR-EDGE PHONE（エアーエッジフォン）

[thumb搭載のエアーエッジフォン](https://ja.wikipedia.org/wiki/ファイル:Kyocera_PHS_AH-K3001V.jpg "wikilink")・[AH-K3001V](../Page/AH-K3001V.md "wikilink")\]\] エアーエッジサービスの一つとして、また音声端末の一種別として、[2003年](../Page/2003年.md "wikilink")[4月1日](../Page/4月1日.md "wikilink")からウィルコム（旧DDIポケット）が開始したもの。旧表記：AirH"PHONE。

  -
    なお、2005年～2006年冬モデル以降の、WXシリーズ端末は、「AIR-EDGE PHONE」を名乗っておらず、音声端末によるウェブブラウズサービスについても**「公式サイト」**（WXシリーズや、[WS009KE](../Page/WS009KE.md "wikilink"),[WS018KE](../Page/WS018KE.md "wikilink"),[WS023T](https://ja.wikipedia.org/wiki/WS023T "wikilink")など）ないしは**「ウィルコム公式サイト」**（主に、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")）と名乗っているが、その直接のかつ事実上の後継機種である。よって、*本項目では便宜上、AIR-EDGE PHONEに含めて取り扱う。*

従来の端末は[PCカード](../Page/PCカード.md "wikilink")や[CFカードタイプのものか](../Page/コンパクトフラッシュ.md "wikilink")、対応音声端末に[PCやPDAなどをケーブルで接続した場合のみ通信回線としてエアーエッジが利用できるというもので](../Page/パーソナルコンピュータ.md "wikilink")、これをエアーエッジ端末単体で音声通話・[Eメール](../Page/電子メール.md "wikilink")・[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")が利用できるようにしたものである。

端末単体で通信（ウェブ・メール等）する場合も、「つなぎ放題コース」の契約でPCとケーブル ([USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")) で接続し、エアーエッジ対応ISPに接続して通信した場合も、いずれも同じく完全[定額制となる](../Page/パケット定額制.md "wikilink")。このような利用方法が可能な端末は現在のところエアーエッジフォンと[イー・モバイル](../Page/イー・モバイル.md "wikilink")の電話端末のみである。[携帯電話](../Page/携帯電話.md "wikilink")の[パケット定額制](../Page/パケット定額制.md "wikilink")は前述のサービスを除き、端末単体でのみ有効で、PC等と接続した場合は、通常は従量課金対象となる。

AIR-EDGE PHONEによる通信は、（リンク数が）最大4xパケット方式となり、最大通信速度は標準で128kbps、[W-OAM](../Page/W-OAM.md "wikilink")時\[15\]は204kbpsとなる。1xパケット方式のみ対応の端末では32kbpsまで。対応端末ではフレックスチェンジ方式による通信も可能。2007年現在、8xパケット方式による通信は利用できない。

なおAIR-EDGE PHONEの基本仕様としては次のものがあり、全てのAIR-EDGE PHONE（および後継機種）に共通して搭載されている。

  - USBケーブルによる外部接続（コネクタ形状はメーカーにより異なる）
  - ブラウザ搭載
  - POP3/SMTP対応のEメール送受信機能
      -
        端末専用メールだけでなく、他プロバイダのメールアカウントに直接アクセス可能。ただしウィルコムのメールと違い自動受信は原則、出来ない。
  - 他のAIR-EDGE対応プロバイダのアクセスポイントへの[PPP接続](../Page/Point-to-Point_Protocol.md "wikilink")
      -
        端末専用のもの（AIR-EDGE PHONEセンター）以外のアクセスポイントにも直接接続可能。

### 略歴

サービス開始時に発売されたのは、[日本無線](../Page/日本無線.md "wikilink")の端末「[AH-J3001V](https://ja.wikipedia.org/wiki/AH-J3001V "wikilink")」「[AH-J3002V](https://ja.wikipedia.org/wiki/AH-J3002V "wikilink")」の2機種である。この端末では、一部の[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")用[ウェブサイト](../Page/ウェブサイト.md "wikilink")の閲覧も可能な「[cHTML](https://ja.wikipedia.org/wiki/compact_HTML "wikilink")」に対応したブラウザ (Compact NetFront) や、POP3/SMTP対応のEメール送受信機能等を搭載する。端末単体およびPC接続等のいずれのデータ通信についても「完全定額制」の選択が可能なことから、発売開始から一部では高い人気を博した。

[2004年](../Page/2004年.md "wikilink")[5月14日](../Page/5月14日.md "wikilink")には[京セラ](../Page/京セラ.md "wikilink")の端末「[AH-K3001V](../Page/AH-K3001V.md "wikilink")」がラインナップに追加された。この端末では[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")や、PC向けの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")「[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")（オペラ）」を携帯電話・PHS用にチューニングした物が搭載された。5月の発売後は3日間で2万台以上を販売し、その後数ヶ月にわたって品不足が続くなどPHSでは近年まれに見るヒット商品となった。日本無線製端末と同様、内蔵ソフトウェアをユーザーがアップデートすることも可能となっている。

[2005年](../Page/2005年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")、[AH-K3002V](https://ja.wikipedia.org/wiki/AH-K3002V "wikilink")が発売された。これはAH-K3001Vのカメラ機能を省き、代わりにセキュリティ対策として、リモートロック機能を搭載したものである。

AH-K3002Vまでの機種は、1xパケット方式のみ対応（最大32kbps）。[AH-J3003S](https://ja.wikipedia.org/wiki/AH-J3003S "wikilink")では2005年2月以降の[ファームウェア](../Page/ファームウェア.md "wikilink")の更新により、PC/PDAへの外部接続時 の4xパケット方式通信（最大128kbps）に対応した。

2005年～2006年冬モデルとして[WX310K](../Page/WX310K.md "wikilink")、[WX300K](https://ja.wikipedia.org/wiki/WX300K "wikilink")、[WX310SA](../Page/WX310SA.md "wikilink")、[WX310J](../Page/WX310J.md "wikilink")、2006年～2007年冬モデルでは[WX220J](https://ja.wikipedia.org/wiki/WX220J "wikilink")、[WX320K](../Page/WX320K.md "wikilink")、[WX321J](../Page/WX321J.md "wikilink")が発売。これらの機種は「AIR-EDGE PHONE」を名乗っていないが、事実上の後継シリーズである。

WX300Kは2006年6月以降の[ファームウェア](../Page/ファームウェア.md "wikilink")の更新により、4xパケット方式通信（最大128kbps）に対応している(それまでは1xパケット方式のみ対応)。WX310シリーズでは、当初から4xパケット方式通信（最大128kbps）に標準で対応している。

WX220J/WX320K/WX321Jでは、4xパケット方式通信の他、[W-OAM](../Page/W-OAM.md "wikilink")による通信に標準で対応し、最大通信速度は標準で128kbps、[W-OAM](../Page/W-OAM.md "wikilink")時\[16\]は204kbpsとなる。

その他、2006年以降、*WILLCOM SIM STYLE*という[W-SIM](../Page/W-SIM.md "wikilink")対応の各種端末もリリースされた。機種によって仕様は大きく異なるものの、AIR-EDGE PHONEの基本的な機能仕様については、各端末に概ね踏襲されている。

*[ウィルコム\#通信端末](https://ja.wikipedia.org/wiki/ウィルコム#通信端末 "wikilink")の項目も参照。*

### AIR-EDGE PHONEセンター

基本的に、AIR-EDGE PHONEの端末単体の通信（ウェブ・メール等）をする場合には、ウィルコムが用意する端末単体専用の[アクセスポイントを利用する](https://ja.wikipedia.org/wiki/アクセスポイント_\(ISP\) "wikilink")。このセンターは、AIR-EDGE PHONEの名称使用時期には「AIR-EDGE PHONEセンター」と呼ばれていたが、AIR-EDGE PHONE名称使用が控えられるとともに、単に「ウィルコム経由のパケット通信時」などと表現され、正式な名称は付かなくなった。なお、AIR-EDGE PHONE等で接続時に「CLUB AIR-EDGE」等と表示されるが、CLUB AIR-EDGEは正式には端末単体アクセス専用のポータルサイトの名称である。[\#CLUB AIR-EDGE参照](https://ja.wikipedia.org/wiki/#CLUB_AIR-EDGE "wikilink")。

*本項目では便宜上、この端末単体アクセス専用のアクセスポイントを「AIR-EDGE PHONEセンター」と呼ぶ。*

AIR-EDGE PHONEの端末単体の通信（ウェブ・メール等）をする場合に、公式のAIR-EDGE PHONEセンターだけでなく、前述のAIR-EDGEで使用されるような一般の[ISPと接続して使用することも可能である](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")（別途、契約および接続料等が必要となる。例えば、Java VM搭載の機種では、公式以外のJavaアプリがAIR-EDGE PHONEセンター経由での通信を利用する事ができず、一般のAIR-EDGE接続用ISPとの接続・通信が必要となる。さらには、AIR-EDGEの範疇からは外れるが、PIAFS方式による回線交換接続すら可能である。ISPのAPや、PIAFS対応の任意のAPに接続し、ウェブ・メール等のIP通信が可能。

さらに、AIR-EDGE PHONEを外部のPC/PDA等に接続して通信する場合には、前述のAIR-EDGEと同様の使用方法で、AIR-EDGE接続ISP等が必要となる。

これらの端末単体・外部接続の別や、アクセスポイントの別により、通信料等の課金体系が異なる場合があり、複雑である。もっとも、AIR-EDGE PHONEの端末単体の通信（ウェブ・メール等）のみを利用するユーザは、何ら設定をしなくとも、ウィルコムが用意する「AIR-EDGE PHONEセンター」に接続するものであるから、その限りではない。

### 高速化サービス

端末上でAIR-EDGE PHONEセンターに接続して使う場合、「高速化サービス」を利用することで専用サーバを介し、画像データ等を圧縮し通信容量を低減した形で通信が可能になるため、Webやメールでの体感速度が速くなる（月額利用料315円・税込）。なお、AIR-EDGE PHONEの名称を使用していた時期にはこのサービスの呼称も「AIR-EDGE PHONE高速化サービス」としていたが、その後、AIR-EDGE PHONE名称使用が控えられるとともに、この呼称も単に「高速化サービス」となった。

  - [W-ZERO3](../Page/W-ZERO3.md "wikilink")向け高速化サービス
    W-ZERO3 / W-ZERO3\[es\] 向けに専用クライアントソフトをインストールする事により、体感速度がより向上するとしている。2007年4月23日開始予定\[17\]。

### 愛称

  - 「AIR-EDGE PHONE（エアエッジフォン）」が極端に訛った「**味ぽん**」の愛称がつけられるようになった。出自は[2ちゃんねる](../Page/2ちゃんねる.md "wikilink")だと考えられている。
  - 本来「味ぽん」とはAIR-EDGE PHONE全てを指すものだが、1年以上他の機種が発売されなかったこともあり、日本無線製のエアーエッジフォン[AH-J3001V/J3002Vのみを指して](https://ja.wikipedia.org/wiki/AH-J3002V "wikilink")「味ぽん」と呼ぶケースもある。
  - 「[AH-K3001V](../Page/AH-K3001V.md "wikilink")」は京セラ製の味ぽん、ということから「**京ぽん**」の愛称で呼ばれている。京セラは2005年4月4日付けで、「京ぽん」を[商標](../Page/商標.md "wikilink")登録出願した\[18\]\[19\]。これは悪意を持った第三者による濫用を牽制するのが目的であり、言葉自体を独占するつもりは、全くないとコメントしている。
  - 同様に「[WX310SA](../Page/WX310SA.md "wikilink")」は三洋製の味ぽん、ということから「**洋ぽん**」の愛称で呼ばれている。

## CLUB AIR-EDGE

**CLUB AIR-EDGE**（くらぶえあえっじ）は、AIR-EDGEおよびAIR-EDGE PHONE利用者向けの、ウィルコムの公式[ポータルサイト](../Page/ポータルサイト.md "wikilink")である。

概略

  - AirH" (AIR-EDGE) の開始時から、「Club AirH"」の名称で、AIR-EDGE接続のPC向けのポータルサイトとして開始。
  - その後、PDAにAirH" (AIR-EDGE) を接続して利用する形態が普及し、「Club AirH" for PDA」の名称で、AIR-EDGE接続のPDA向けのポータルサイトとして開始。
  - その後、AirH" PHONE (AIR-EDGE PHONE) のサービスインしAIR-EDGE PHONE端末向けのポータルサイトの開始とともに、上記のポータルサイトも含めて名称変更され、「Club AirH" for PC」「Club AirH" for PDA」「Club AirH" for AirH" PHONE」の三本立てとなった。
  - その後、AIR-EDGEおよびAIR-EDGE PHONEへの名称変更と共に、「CLUB AIR-EDGE for PC」「CLUB AIR-EDGE for PDA」「CLUB AIR-EDGE for AIR-EDGE PHONE」に改称。
  - その後、AIR-EDGE PHONEの名称使用が控えられるとともに、AIR-EDGE PHONE端末向けのポータルサイトが単に「CLUB AIR-EDGE」となった。

なお、AIR-EDGE PHONE等では、アクセスポイントへの接続時に「CLUB AIR-EDGE」等と表示されることがあるため、CLUB AIR-EDGEが公式アクセスポイント（[\#AIR-EDGE PHONEセンターのように解釈されることも](https://ja.wikipedia.org/wiki/#AIR-EDGE_PHONEセンター "wikilink")、公式・一般と問わず見られる。

## AIR-EDGE対応端末

※**強調**は、現行機

### データ通信専用端末

  - [MC-P300](https://ja.wikipedia.org/wiki/MC-P300 "wikilink")（[SII](../Page/セイコーインスツル.md "wikilink")、[PCMCIA](../Page/PCカード.md "wikilink")）
  - [RH2000P](https://ja.wikipedia.org/wiki/RH2000P "wikilink")（[TDK](../Page/TDK.md "wikilink")、[CF](../Page/コンパクトフラッシュ.md "wikilink") typeI）
  - [CFE-02](https://ja.wikipedia.org/wiki/CFE-02 "wikilink")（[NECインフロンティア](https://ja.wikipedia.org/wiki/NECインフロンティア "wikilink")）、CF typeII）
  - [AH-G10](../Page/AH-G10.md "wikilink")（本多エレクトロン（現[ネットインデックス](https://ja.wikipedia.org/wiki/ネットインデックス "wikilink")））、PCMCIA）
  - [AH-N401C](https://ja.wikipedia.org/wiki/AH-N401C "wikilink")（[NECインフロンティア](https://ja.wikipedia.org/wiki/NECインフロンティア "wikilink")、CF typeII）
  - [AH-H401C](../Page/AH-H401C.md "wikilink")（本多エレクトロン、CF typeII）
  - [AH-H403C](../Page/AH-H403C.md "wikilink")（本多エレクトロン、CF typeII）
  - **[AH-F401U](https://ja.wikipedia.org/wiki/AH-F401U "wikilink")**（[富士通](../Page/富士通.md "wikilink")、[USB](../Page/ユニバーサル・シリアル・バス.md "wikilink")）
  - **[AH-S101S](https://ja.wikipedia.org/wiki/AH-S101S "wikilink")**（SII、[SD](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink")）
  - **[AH-S405C](https://ja.wikipedia.org/wiki/AH-S405C "wikilink")**（SII、CF typeI）
  - **[AH-H407P](../Page/AH-H407P.md "wikilink")**（本多エレクトロン、PCMCIA）
  - **[AX510N](https://ja.wikipedia.org/wiki/AX510N "wikilink")**（NECインフロンティア、PCMCIA、AIR-EDGE\[PRO\]対応）
  - **[WS002IN](../Page/WS002IN.md "wikilink") ("DD")**（ネットインデックス、USB、W-SIM端末、[RX420AL](https://ja.wikipedia.org/wiki/RX420AL "wikilink")利用時に限りW-OAM対応）
  - **[WS008HA](https://ja.wikipedia.org/wiki/WS008HA "wikilink")**（[ハギワラシスコム](https://ja.wikipedia.org/wiki/ハギワラシスコム "wikilink")、[ExpressCard](../Page/ExpressCard.md "wikilink")/34、W-SIM端末、RX420AL利用時に限りW-OAM対応）
  - **[AX420S](../Page/AX420S.md "wikilink")**（SII、CF typeI、[W-OAM](../Page/W-OAM.md "wikilink")対応）
  - **[AX420N](https://ja.wikipedia.org/wiki/AX420N "wikilink")**（NECインフロンティア、CF typeI、W-OAM対応）
  - **[AX520N](https://ja.wikipedia.org/wiki/AX520N "wikilink")**（NECインフロンティア、PCMCIA、W-OAM及びAIR-EDGE\[PRO\]対応）
  - **[AX530IN](https://ja.wikipedia.org/wiki/AX530IN "wikilink")**（ネットインデックス、PCMCIA、W-OAM typeG及びAIR-EDGE\[PRO\]対応）
  - **[AX530S](https://ja.wikipedia.org/wiki/AX530S "wikilink")**（SII、PCMCIA（アダプタ装着によりUSB接続可能）、W-OAM typeG及びAIR-EDGE\[PRO\]対応）

### intelligent H"

intelligent H"とは、AIR-EDGE対応（PC等に接続しAIR-EDGEとして使用可能）のfeelH"端末を、一時期そう呼称したもの。

  - KX-HV50（九州松下電器\<現:[パナソニック コミュニケーションズ](https://ja.wikipedia.org/wiki/パナソニック_コミュニケーションズ "wikilink")\>製）
  - KX-HV200（同）
  - KX-HV210（同）
  - RZ-J700（三洋電機製）
  - [H-SA3001V](../Page/H-SA3001V.md "wikilink")（同）

### AIR-EDGE PHONE

[thumb](https://ja.wikipedia.org/wiki/ファイル:DDI-Pocket_JRC_AH-J3002V_2.jpg "wikilink")

  - [AH-J3001V](https://ja.wikipedia.org/wiki/AH-J3001V "wikilink")（[日本無線](../Page/日本無線.md "wikilink")）
  - [AH-J3002V](https://ja.wikipedia.org/wiki/AH-J3002V "wikilink")（日本無線）
  - AH-J3003S（日本無線）
  - [AH-K3001V](../Page/AH-K3001V.md "wikilink")（[京セラ](../Page/京セラ.md "wikilink")）
  - AH-K3002V（京セラ）

#### WX220/300/310/320シリーズ

なお、公式にはWXシリーズであり、AIR-EDGE PHONEのブランドは伴わない。

  - **WX300K** （京セラ）
  - **[WX310K](../Page/WX310K.md "wikilink")** （京セラ）
  - **[WX310SA](../Page/WX310SA.md "wikilink")** （[三洋電機](../Page/三洋電機.md "wikilink")）
  - **[WX310J](../Page/WX310J.md "wikilink")** （日本無線）
  - **[WX220J](https://ja.wikipedia.org/wiki/WX220J "wikilink")** （日本無線）
  - **[WX321J](../Page/WX321J.md "wikilink")** （日本無線）
  - **[WX320K](../Page/WX320K.md "wikilink")** （京セラ）
  - **[WX320T](../Page/WX320T.md "wikilink")** （東芝）

### W-SIMモジュール

AIR-EDGEの通信機能も網羅する。

  - **[RX410IN](https://ja.wikipedia.org/wiki/W-SIM#RX410IN "wikilink")**（[ネットインデックス](https://ja.wikipedia.org/wiki/ネットインデックス "wikilink")）…[2005年](../Page/2005年.md "wikilink")[11月25日](../Page/11月25日.md "wikilink")発売。 単体ではなく、WILLCOM SIM-STYLEの機器に挿入して音声通話・データ通信を行うための通信モジュール。[WS001IN](../Page/WS001IN.md "wikilink")、[WS002IN](../Page/WS002IN.md "wikilink")、[WS003SH](https://ja.wikipedia.org/wiki/WS003SH "wikilink")、[WS004SH](https://ja.wikipedia.org/wiki/WS004SH "wikilink")、[WS005IN](../Page/WS005IN.md "wikilink")、[WS007SH](../Page/WS007SH.md "wikilink")、[WS008HA](https://ja.wikipedia.org/wiki/WS008HA "wikilink")には標準添付（後に、WS008HAはRX420ALに、それ以外はRX420INに差し替えられている）。
  - **[RX420AL](https://ja.wikipedia.org/wiki/W-SIM#RX420AL "wikilink")**（[アルテル](../Page/アルテル.md "wikilink")）…[2006年](../Page/2006年.md "wikilink")[12月19日](https://ja.wikipedia.org/wiki/12月19日 "wikilink")発売。この端末から単体購入が可能になった。新規契約の[WS009KE](../Page/WS009KE.md "wikilink")、[WS018KE](../Page/WS018KE.md "wikilink")、[WS023T](https://ja.wikipedia.org/wiki/WS023T "wikilink")、[WS024BF](https://ja.wikipedia.org/wiki/WS024BF "wikilink")、[WS026T](https://ja.wikipedia.org/wiki/WS026T "wikilink")には標準装備され、[WS009KE](../Page/WS009KE.md "wikilink")とのセットは[2006年](../Page/2006年.md "wikilink")[12月14日](../Page/12月14日.md "wikilink")に先行発売。
  - **[RX420IN](https://ja.wikipedia.org/wiki/W-SIM#RX420IN "wikilink")**（[ネットインデックス](https://ja.wikipedia.org/wiki/ネットインデックス "wikilink")）…[2007年](../Page/2007年.md "wikilink")[4月10日](../Page/4月10日.md "wikilink")発売。\[\[WS011SH|WS011SH (Advanced/W-ZERO3 \[es\])\]\]、[WS014IN](https://ja.wikipedia.org/wiki/WS014IN "wikilink")、[WS016SH](../Page/WS016SH.md "wikilink")、[WS020SH](../Page/WS020SH.md "wikilink")に標準装備されている。
  - **[RX430AL](https://ja.wikipedia.org/wiki/W-SIM#RX430AL "wikilink")**（[アルテル](../Page/アルテル.md "wikilink")→[エイビット](https://ja.wikipedia.org/wiki/エイビット "wikilink")）…[2009年](../Page/2009年.md "wikilink")[12月17日](../Page/12月17日.md "wikilink")発売。[WS027SH](https://ja.wikipedia.org/wiki/WS027SH "wikilink")に標準装備される。

*WILLCOM SIM STYLE端末については、[W-SIM](../Page/W-SIM.md "wikilink")の項目を参照のこと。*

### AIR-EDGE IN対応端末

  - FMV-BIBLO LOOX T50G/W（[富士通](../Page/富士通.md "wikilink")）
  - FMV-BIBLO LOOX T50E/W（富士通）
  - FMV-BIBLO LOOX S80C/W（富士通）
  - FMV-BIBLO LOOX T60D/W（富士通）
  - FMV-BIBLO LOOX T93C/W（富士通）
  - FMV-BIBLO LOOX S80B/W（富士通）
  - FMV-BIBLO LOOX T93B/W（富士通）
  - FMV-BIBLO LOOX S73AW（富士通）
  - FMV-BIBLO LOOX T86AW（富士通）
  - FMV-BIBLO LOOX S9/70W（富士通）
  - FMV-BIBLO LOOX S8/70W（富士通）
  - FMV-BIBLO LOOX T8/80W（富士通）

## 対応プロバイダ

プロバイダには、ADSLや光回線に加入しているとPHSの通信料金だけで使えるところと、ADSLや光回線の利用料金とは別にプロバイダ指定のAIR-EDGEコース等に加入してオプション料金を払わないと使えないところの2種類がある。

  - ふれあいインターネット 法人マックス・月コース 付加的サービス 3,240円/月
  - [BEKKOAME INTERNET](https://ja.wikipedia.org/wiki/ベッコアメ "wikilink") ベッコアメ・ライト 2,160円/月 福祉割引あり12,960円（年会費制）
  - Canonet ダイヤルアップ（モバイル対応）2,160円/月 サービス抱き合わせなどの諸条件あり
  - E-JAN ダイヤルアップ接続 2,160円/月
  - 群馬インターネット 固定制（電話料金別プラン）2,160円/月 20,000円（1,333円/月換算）/年払+３ヶ月分サービス
  - インフォスフィア AIR-EDGEコース 2,160円/月
  - JENS SpinNet 基本料金内での付加的サービス 2,160円/月
  - Webしずおか マルチコース（付加的サービス）1,998円/月
  - OKBNET モバイルプラン 1,944円/月 19,440円（1,620円/月換算）/年払
  - 3WEB 各種プラン付加的サービス 1,922円/月 21,600円（1,800円/月換算）/年払
  - いわみインターネット 基本料金内での付加的サービス 1,728円/月
  - サンフィールド・インターネット アクセスフリーコース 1,620円/月
  - [PRIN](../Page/PRIN.md "wikilink") 1,575円/月
  - ニルスインターネット AirH"プラン 1,575円/月
  - かなざわネット AirH"プラン 1,575円/月
  - アイコムティ MnetIPコネクト・モバイル 1,490円/月
  - marimo internet ダイヤルアップ接続コース オプションサービス 1,223円/月
  - アーバンインターネット（do\!up）オプションサービス 1,080円/月
  - U-netSURF ダイヤルアップ接続サービスの付加的サービス 1,080円/月
  - 株式会社大塚商会 αWeb エアエッジコース 1,080円/月
  - サザンクロス エアエッジプラン 1,080円/月
  - えるねっと迫 AirH"(エアーエッジ)コース 1,080円/月
  - リムネット オプションサービス 1,058円/月
  - アレスネット エアエッジコース 1,058円/月 口座振替も対応
  - まねきねこ エアエッジコース 1,058円/月
  - JASNET21 モバイルコース 1,026円/月
  - ACROSS ダイヤルアップコース 1,026円/月 9,500円（791円/月換算）/年払
  - インターネットMAGMA AIR-EDGE対応プラン 1,026円/月
  - A-Net エアエッジプラン 980円/月
  - NMTnet My-Web\&Mailセット 付加的サービス 972円/月
  - オープンサーキット エアエッジコース 972円/月
  - AIRnet AirH”コース 972円/月
  - アイネットコミュニケーションズ エアエッジサービス 972円/月 11,016円（918円/月換算）/年払
  - エディオンネット モバイルプランST 918円/月
  - interQ MEMBERS オプションサービス 864円/月
  - @T COM エアエッジコース 864円/月 口座振替も対応
  - イオン・ネット どこでもアクセスコース 864円/月
  - INTERLINK 864円/月
  - コスモスネットコミュニケーションズ モバイル定額接続サービス 864円/月
  - KIWI internet エアエッジコース 861円/月
  - [OCN](../Page/OCN.md "wikilink") 840円/月
  - KISweb ダイヤルアップデイタイム 付加的サービス 799円/月 口座振替も対応
  - JOMON Internet エアエッジプラン 756円/月 7,560円（630円/月換算）/年払
  - WAKWAK 756円/月
  - リンククラブインターネット[5](http://www.linkclub.jp/) オプションサービス 720円/月
  - ZERO エアエッジ接続サービス 648円/月
  - SANNET 648円/月
  - [7-dj.com](../Page/7-dj.com.md "wikilink") AIR-EDGEコース 648円/月
  - HITWave モバイル接続（法人専用プロバイダ）630円/月
  - [BIGLOBE](../Page/BIGLOBE.md "wikilink") オプションサービス 無料〜600円/月
  - 117net オプションサービス 540円/月
  - ASAHIネット オプションサービス 540円/月
  - SYNAPSE シナプス・チョイス オプションサービス 540円/月
  - info Pepperインターネット オプションサービス 540円/月
  - 四国インターネット AIR-EDGEオプション 540円/月
  - ミンク・インターネット エアエッジオプション 540円/月
  - ケイ・オプティコム（旧DS Networks）オプションサービス 540円/月
  - mitene internet service AIR-EDGEサービス 540円/月
  - CORALNET エアエッジサービス 540円/月
  - Mirai NET ダイヤルアップ接続プラン 540円/月 学校・福祉割引制度あり
  - kyotoInet BB 基本料金内での付加的サービス 540円/月
  - MicNet オプションサービス 343円/月
  - [ぷらら](https://ja.wikipedia.org/wiki/ぷららネットワークス "wikilink") オプションサービス 324円/月
  - [Tigers-net.com](https://ja.wikipedia.org/wiki/アイテック阪急阪神 "wikilink") ダイヤルアップ 324円/月
  - @NetHome. オプションサービス 210円/月
  - [au one net](https://ja.wikipedia.org/wiki/au_one_net "wikilink") オプションサービス

<!-- end list -->

  - [IIJ](https://ja.wikipedia.org/wiki/インターネットイニシアティブ "wikilink") モバイルアクセス 324円/月 (2016年3月31日をもってサービス終了)
  - hi-ho オプションサービス (2016年3月31日をもってサービス終了)
  - [TOKAI](../Page/TOKAI.md "wikilink")ネットワーククラブ 付加的サービス (2015年11月30日をもってY\!mobile端末での接続サービス終了)
  - [So-net](https://ja.wikipedia.org/wiki/So-net "wikilink") (2015年5月31日をもってサービス終了)
  - [AT\&T](../Page/AT&T.md "wikilink")ビジネス・インターネットサービス (2015年3月31日をもってサービス終了)
  - [TikiTikiインターネット](https://ja.wikipedia.org/wiki/TikiTikiインターネット "wikilink") 定額モバイルコース 972円/月（2015年1月27日をもって新規申込終了）
  - はまっこ (2014年5月31日をもってサービス終了)
  - ホッカイ・ネット (2014年5月31日をもってサービス終了)
  - コガネット エアエッジ接続 1,050円/月 (2014年3月31日をもって新規申込終了)
  - 生協インターネット (2013年9月30日をもってサービス終了)
  - アルファインターネット (2013年1月1日をもってユビキタスプロバイダDTIへ統合によりサービス終了）
  - [@nifty](https://ja.wikipedia.org/wiki/@nifty "wikilink") (2012年6月30日をもってサービス終了)
  - [DTI](../Page/ドリーム・トレイン・インターネット.md "wikilink") エアエッジプラン 950円/月 (2009年5月31日をもって新規申込終了)
  - [KCOM](https://ja.wikipedia.org/wiki/KDDIネットワーク&ソリューション "wikilink") (2005年3月31日をもってDIONへの集約移行に伴い接続サービス終了）
  - [ODN](../Page/ODN.md "wikilink") オプションモバイルプラン 842円/月（2004年5月31日をもって新規申込終了）
  - ネットウェーブ四国 ダイヤルアップサービス 1,944円/月 (現在新規受付はおこなっていない)
  - ejnet おもいっきりコース(ダイヤルアップ) 1,260円/月 (現在新規受付はおこなっていない)
  - BBplus 840円/月 (現在新規受付はおこなっていない)
  - ツインインターネット モバイル専用コース 486円/月 (現在新規受付はおこなっていない)
  - ReSET.JP オプションサービス モバイルオプション 324円/月 (現在新規受付はおこなっていない)
  - [コジマ](../Page/コジマ.md "wikilink")ネット (現在はサービスをおこなっていない)
  - 天糸瓜ネット (現在はサービスをおこなっていない)

など

## 脚注

## 関連項目

  - [ウィルコム](../Page/ウィルコム.md "wikilink")
  - [PHS](../Page/PHS.md "wikilink")
  - [W-OAM](../Page/W-OAM.md "wikilink")
  - [@FreeD](https://ja.wikipedia.org/wiki/@FreeD "wikilink")

## 外部リンク

  - [AirH"](https://web.archive.org/web/20030401213439/http://www.ddipocket.co.jp/data/i_air.html) - 閉鎖（2003年4月1日時点の[アーカイブ](../Page/インターネットアーカイブ.md "wikilink")）

[Category:PHS_(ウィルコム)](https://ja.wikipedia.org/wiki/Category:PHS_\(ウィルコム\) "wikilink") [Category:インターネット接続](https://ja.wikipedia.org/wiki/Category:インターネット接続 "wikilink")

1.  「W-OAM時」とは、W-OAM対応端末によりW-OAM対応[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")と通信した場合を示す。
2.  「W-OAM typeG時」とは、W-OAM typeG対応端末によりW-OAM対応[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")と通信した場合を示す。
3.  高い方の速度は[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")回線の[光](../Page/光通信.md "wikilink")[IP化後のもの](../Page/Internet_Protocol.md "wikilink")。
4.
5.
6.
7.
8.
9.
10. [つなぎ放題コースでの音声通話料金](http://www.willcom-inc.com/ja/plan/data/whole/charge/index.html)
11. [新ウィルコム定額プラン](http://www.willcom-inc.com/ja/plan/phone/new_fixed_rate/index.html)
12.
13. [1](http://www.willcom-inc.com/cgi-bin/Map4_txt.cgi?Mcod=13&Meki=&Mlat=35.677788&Mlon=139.769965&Mzom=6&Mpag=9&Mtyp=4&Msvg=0&Mcrc=0)
14. [2](http://www.itmedia.co.jp/enterprise/mobile/articles/0507/25/news020.html) [3](http://www.j-com.co.jp/news/release/0503.html)
15.
16.
17. <http://www.willcom-inc.com/ja/corporate/press/2007/04/11/index_01.html>
18.
19.