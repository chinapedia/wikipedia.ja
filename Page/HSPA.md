> この記事は[HSPA](https://ja.wikipedia.org/wiki/HSPA)から翻訳されています。


**HSPA** (High Speed Packet Access) は、[W-CDMA](../Page/W-CDMA.md "wikilink")を拡張した高速[パケット通信](../Page/パケット通信.md "wikilink")規格である。[第3世代移動通信システム](../Page/第3世代移動通信システム.md "wikilink") (3G) に対して、[第3.5世代移動通信システム](../Page/第3.5世代移動通信システム.md "wikilink") (3.5G) と位置づけられている\[1\]。

下りの高速化を[HSDPA](https://ja.wikipedia.org/wiki/HSDPA "wikilink") (High-Speed Downlink Packet Access)、上りの高速化は[HSUPA](https://ja.wikipedia.org/wiki/HSUPA "wikilink") (High-Speed Uplink Packet Access) または EUL と呼ぶ。また、[3GPP](../Page/3GPP.md "wikilink") (Third Generation Partnership Project) Release 7にて、HSPA Evolution としてさらなる高度化が行われた。

## HSDPA

**[HSDPA](https://ja.wikipedia.org/wiki/HSDPA "wikilink")**は、3GPP Release 5にて規定されている。物理チャネル速度としてセル当たり下り方向最大14.4M[bpsのパケット通信が可能である](../Page/ビット毎秒.md "wikilink")\[2\]。

[3GPP](../Page/3GPP.md "wikilink") [FDDの](https://ja.wikipedia.org/wiki/周波数分割複信 "wikilink")[Release '99規格に対して](https://ja.wikipedia.org/wiki/Universal_Mobile_Telecommunications_System#Release_'99 "wikilink")、物理レイヤでは以下のチャネルが追加された。

  - 下り方向
      - HS-PDSCH (High Speed Pysical Downlink Shared Channel)
      - HS-SCCH (Shared Control Channel)
  - 上り方向
      - HS-DPCCH (Dedicated Physical Control Channel(uplink) for HS-DSCH）

また、MACレイヤでは以下の機能を有する**MAC-hs**が物理レイヤと隣接する形で新設された。

  - 基地局側
      - フロー制御 - 上位レイヤに対して、無線側の通信速度に応じた適切なデータ送出速度を指示する機能。ただし、3GPP上では本機能を実現するアルゴリズムは規定されず、実装依存となっている。
      - スケジューリングおよび優先制御 - 上位ノードから通知された優先度情報を考慮しつつ、システム全体の総合的な通信効率を向上させることを目的として、端末にタイムスロットを配分する機能。ただし、3GPPにおいては本機能を実現するアルゴリズムは規定されず、実装依存となっている。
      - [パケット合成型HARQ](https://ja.wikipedia.org/wiki/パケット合成型HARQ "wikilink") - Hybrid Automatic Repeat Requestの略。受信側で復号失敗データが破棄されずに再送データと組み合わせて復号されることを考慮した上で、再送パターンを決定する。複数のHARQプロセスが独立に動作する。
      - TFRIの選択 - TFRI (Transport Format Resource Index) はタイムスロットに割りあてたコード数、変調方式、データサイズを表しており、HS-SCCHを用いて端末に送信される。端末から送信された品質情報を用いて適切なTFRIを選択することで[適応変調](https://ja.wikipedia.org/wiki/適応変調 "wikilink")・[符号化](https://ja.wikipedia.org/wiki/誤り訂正符号 "wikilink") ([AMC](https://ja.wikipedia.org/wiki/:en:Link_adaptation "wikilink"): Adaptive Modulation and Coding）を実現する。ただし、3GPP上では本機能を実現するアルゴリズムは規定されず、実装依存となっている。
  - 端末側
      - [パケット合成型HARQ](https://ja.wikipedia.org/wiki/パケット合成型HARQ "wikilink") - 受信失敗データを廃棄せずに再送データと組み合わせて復号を行う。複数のHARQプロセスが独立に動作する。復号成功時にはACK、復号失敗時にはNACKをHS-DPCCH上で伝送する。
      - 順序制御 - 送信側のHARQがプロセスごとに独立に動作するため、初回送信時の時系列順に受信成功するとは限らない。本機能では、初回送信時の順序性を保持した上でデータを上位レイヤへ受け渡す。復号失敗の確認応答が基地局側で復号成功と誤判定してしまうなどの理由で、あるHARQプロセスについて[デッドロック](../Page/デッドロック.md "wikilink")が発生することがある。本機能ではこのようなデッドロックを回避するために、受信されるべきデータの待ち時間（*Timer T1*）が設定されている。待ち時間が満了すると、端末で受信されたデータは強制的に上位レイヤに受け渡される。

以上のように、HSDPAでは基地局と端末にMAC-hsを追加することで機能を実現しているが、逆に言えば、その他のレイヤには大きな変更が加えられていない。この点から、既にR99通信網を整備している事業者にとっては設備の大幅な入れ替え無しにHSDPAが導入可能であると言える。

HSDPAの要素技術（基地局スケジューラ、HARQ, AMC等）は、[auなどが既に商用展開している](../Page/Au_\(携帯電話\).md "wikilink")[EV-DOと本質的には同一である](../Page/CDMA2000_1x.md "wikilink")。しかし、EV-DOでは占有帯域が1.25MHz ([Rel. 0](../Page/CDMA2000_1x.md "wikilink")、[Rev. Aの場合](../Page/CDMA2000_1x.md "wikilink")。[Rev. Bでは](../Page/CDMA2000_1x.md "wikilink")20MHzにまで拡大予定) であるのに対し、HSDPAでは5MHzと広帯域であるため、HSDPAシステムのみで帯域を占有してしまうことは好ましくない。よって、HSDPAではEV-DOと異なり、端末からは受信品質に対応したインデックスであるCQI（Channel Quality Indicator）をHS-DPCCH上で送信するのみに止まり、実際にタイムスロット単位で送信されるデータサイズは、送信時に使用可能な基地局送信リソースに基づいて基地局で決定する方式が採用された。これにより、音声ユーザやR99パケットユーザが存在することで基地局送信リソースが変動したとしても、問題なく通信を行うことが可能となっている。対してEV-DOでは、ある帯域をEV-DOのみで占有可能なため基地局送信リソースが変動せず、端末側において、所要の誤り率で受信可能なデータレートと受信品質が常に対応することになる。このため、端末から所望のデータレートを直接的に基地局に通知することで[AMC](https://ja.wikipedia.org/wiki/AMC "wikilink")を実現している。

### 端末カテゴリ

HSDPAでは受信能力のカテゴリ分けを行うことで、目的にあわせた[端末](../Page/端末.md "wikilink")の製造を可能としている。

HSDPAにおける初回送信データの符号化手順では、まず[符号化前のデータビットを仮想的なIRバッファサイズに合わせて](https://ja.wikipedia.org/wiki/誤り訂正符号 "wikilink")[符号化した](https://ja.wikipedia.org/wiki/誤り訂正符号 "wikilink") (First [Rate Matching](https://ja.wikipedia.org/wiki/Rate_Matching "wikilink"))。 後に、再度、物理チャネルのサイズに応じたビット系列の間引き（puncturing）を実施する (Second [Rate Matching](https://ja.wikipedia.org/wiki/Rate_Matching "wikilink")) 。このような2段階の符号化（正確には[Rate Matching](https://ja.wikipedia.org/wiki/Rate_Matching "wikilink")）を行うことで、再送データの[符号化率を柔軟に設定することが可能となっている](https://ja.wikipedia.org/wiki/誤り訂正符号 "wikilink")。その反面、受信能力的に上位カテゴリに属する端末だとしても初回の[符号化率が異なるため](https://ja.wikipedia.org/wiki/誤り訂正符号 "wikilink")、必ずしも下位互換性を有しないことになる。

HSDPAのタイムスロットは2msであるため、下表の**タイムスロット当たりに受信可能なビット数の最大値**を**連続受信可能なタイムスロット間隔の最小値**で除算し、更に、2000で除算すると通信速度の最大値（Mbps）が得られる。ただし、本通信速度は上記で述べたMAC-hsレイヤでの通信速度であり、実際にユーザ側で体感可能な通信速度とは異なることに注意すべきである。例えば、[3GPP](../Page/3GPP.md "wikilink")で規定された[Common test environments for User Equipment (UE) conformance testing](http://www.3gpp.org/ftp/Specs/html-info/34108.htm)の6.10.2.4.5.1.2.1.1.1節に記載されたパラメータを参照すると、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")において[2006年](../Page/2006年.md "wikilink")にサービスが開始されたカテゴリ6の最高速度は3.65Mbpsとなる。

<table>
<caption>受信能力のカテゴリ</caption>
<thead>
<tr class="header">
<th><p>カテゴリ</p></th>
<th><p>同時受信可能な<br />
コード数の最大値</p></th>
<th><p>連続受信可能な<br />
タイムスロット間隔の最小値</p></th>
<th><p><a href="../Page/変調方式.md" title="wikilink">変調方式</a></p></th>
<th><p>タイムスロット当たりに受信可能な<br />
ビット数の最大値 (bit)</p></th>
<th><p>IRバッファサイズ(kbit)</p></th>
<th><p>通信速度(M<a href="../Page/ビット毎秒.md" title="wikilink">bps</a>)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>5</p></td>
<td><p>3</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>7298</p></td>
<td><p>19.2</p></td>
<td><p>1.22</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>5</p></td>
<td><p>3</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>7298</p></td>
<td><p>28.8</p></td>
<td><p>1.22</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>5</p></td>
<td><p>2</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>7298</p></td>
<td><p>28.8</p></td>
<td><p>1.82</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>5</p></td>
<td><p>2</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>7298</p></td>
<td><p>38.4</p></td>
<td><p>1.82</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>5</p></td>
<td><p>1</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>7298</p></td>
<td><p>57.6</p></td>
<td><p>3.65</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>5</p></td>
<td><p>1</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>7298</p></td>
<td><p>67.2</p></td>
<td><p>3.65</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>10</p></td>
<td><p>1</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>14411</p></td>
<td><p>115.2</p></td>
<td><p>7.21</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>10</p></td>
<td><p>1</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>14411</p></td>
<td><p>134.4</p></td>
<td><p>7.21</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>15</p></td>
<td><p>1</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>20251</p></td>
<td><p>172.8</p></td>
<td><p>10.13</p></td>
</tr>
<tr class="even">
<td><p>10</p></td>
<td><p>15</p></td>
<td><p>1</p></td>
<td><p>QPSK/16QAM</p></td>
<td><p>27952</p></td>
<td><p>172.8</p></td>
<td><p>13.98</p></td>
</tr>
<tr class="odd">
<td><p>11</p></td>
<td><p>5</p></td>
<td><p>2</p></td>
<td><p>QPSK</p></td>
<td><p>3630</p></td>
<td><p>14.4</p></td>
<td><p>0.91</p></td>
</tr>
<tr class="even">
<td><p>12</p></td>
<td><p>5</p></td>
<td><p>1</p></td>
<td><p>QPSK</p></td>
<td><p>3630</p></td>
<td><p>28.8</p></td>
<td><p>1.82</p></td>
</tr>
</tbody>
</table>

## HSUPA

**[HSUPA](https://ja.wikipedia.org/wiki/HSUPA "wikilink")** (High Speed Uplink Packet Access) は、3GPP Release 6で[2006年](../Page/2006年.md "wikilink")に規定された上り方向の高速化を行うパケット通信規格である。3GPPではHSDPAとの混乱を避けるため、**EUL** (Enhanced UpLink) と呼ばれており、新規に追加された物理チャネルやMACについても**E-DPDCH**や**MAC-e**といったように"e"が修辞語として用いられている。端末あたり最高速度が0.7～5.7Mbpsに向上するが、最高速度に幅があるのはHSDPAと同様に送信能力に応じて端末が[カテゴリ分けされているためである](https://ja.wikipedia.org/wiki/#端末カテゴリ "wikilink")。HSDPAとは異なり、カテゴリ毎に使用可能なタイムスロット長が異なる。奇数カテゴリはタイムスロット長として10msのみ使用可能であり、偶数カテゴリでは10msの他に2msも使用可能である。最高速度5.7Mbpsは、カテゴリ6をタイムスロット長2msで運用した場合にのみ達成される。タイムスロット長10msの最高速度は2Mbpsであり、カテゴリ4～6でサポートされている。

また、HSDPAのような2段階の符号化を行っていないため、タイムスロット長を除けば上位カテゴリが下位カテゴリを包含することになる。

| カテゴリ          | 最大送信速度       |
| ------------- | ------------ |
| 1             | 0.73 Mbit/s  |
| 2             | 1.46 Mbit/s  |
| 3             | 1.46 Mbit/s  |
| 4             | 2.93 Mbit/s  |
| 5             | 2.00 Mbit/s  |
| 6             | 5.742 Mbit/s |
| 7 (3GPP Rel7) | 11.5 Mbit/s  |
|               |              |

  - [外部リンク FDD enhanced uplink; Overall description; Stage 2](http://www.3gpp.org/ftp/Specs/html-info/25309.htm)

## HSPA Evolution / HSPA+

**HSPA Evolution**は、HSPAを高速化したもの。**[HSPA+](https://ja.wikipedia.org/wiki/w:HSPA+ "wikilink")**、**[Enhanced HSPA](https://ja.wikipedia.org/wiki/w:Ehspa "wikilink")（[eHSPA](https://ja.wikipedia.org/wiki/w:Ehspa "wikilink")）**、**[Evolved HSPA](https://ja.wikipedia.org/wiki/w:Evolved_HSPA "wikilink")**とも呼ばれる。下り最大21Mbps、上り最大11.5Mbpsを実現する。

日本では、[2009年](../Page/2009年.md "wikilink")[7月24日](../Page/7月24日.md "wikilink")より、[イーアクセス](https://ja.wikipedia.org/wiki/イーアクセス "wikilink")(当時)が、下り最大21Mbps・上り最大5.8Mbpsによる、HSPA+サービスを提供開始している。[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[9月](../Page/9月.md "wikilink")現在、対応端末は、データ端末([D31HW](https://ja.wikipedia.org/wiki/D31HW "wikilink")・[D32HW](https://ja.wikipedia.org/wiki/D32HW "wikilink")等)のみで、音声端末でのデータ通信では提供されていなかった(後に、音声端末として、[GS03](https://ja.wikipedia.org/wiki/GS03 "wikilink")が投入された)。

音声端末では、[2011年](../Page/2011年.md "wikilink")冬モデルより、[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")モバイル(当時)が[ULTRA PHONEとして](https://ja.wikipedia.org/wiki/ULTRA_PHONE "wikilink")、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")4機種を投入し参入している（ドコモの[XiあるいはKDDIの](https://ja.wikipedia.org/wiki/Xi_\(携帯電話\) "wikilink")[+WiMAX](https://ja.wikipedia.org/wiki/+WiMAX "wikilink")によるデュアル端末に対抗したもの）。

また、[2012年](../Page/2012年.md "wikilink")[7月25日](../Page/7月25日.md "wikilink")から、[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")モバイルは(当時)、[900MHz帯](https://ja.wikipedia.org/wiki/900MHz帯 "wikilink")の[プラチナバンド](https://ja.wikipedia.org/wiki/プラチナバンド_\(ソフトバンク\) "wikilink")5MHz×2を使ってHSPA+を始めた。同時期に既存の[2GHz帯](../Page/2GHz帯.md "wikilink")W-CDMA局の一部をHSPA+対応に更新中でもある。

3.5Gに相当する HSPA+ などもマーケティング的に「4G」と呼称されることがある。そのため ITU は市場の混乱を避けることを名目に[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[12月6日](../Page/12月6日.md "wikilink")に LTE や WiMAX 、さらには HSPA+ などの3Gを発展させた規格も「4Gと呼称してよい」とする声明を発表した\[3\]。

## DC-HSDPA

**DC-HSDPA** (Dual Cell High Speed Downlink Packet Access) とは、複数の周波数帯（日本では、主に5MHz幅×2）の利用により、2倍以上の速度を実現する高速化規格の一つ。下り最大42Mbps。

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[12月3日](../Page/12月3日.md "wikilink")より、[イー・モバイル](../Page/イー・モバイル.md "wikilink")が、周波数帯域を5MHz×2幅（既存の5MHz幅と新規獲得の10MHz幅のうち5MHz幅によって実現としている）を利用し、下り最大21Mbps（HSPA+）を2つ束ねる形での最大42Mbps(誤り訂正符号を除外すると35Mbps\[4\])のサービスを開始している。サービスブランドは、[EMOBILE G4](https://ja.wikipedia.org/wiki/EMOBILE_G4 "wikilink")。同ブランドは、DC-HSDPA開始と同時に、HSPA+が包括された。対応端末は、サービス開始時点で[D41HW](https://ja.wikipedia.org/wiki/D41HW "wikilink")のみとなっていたが、[GP02](https://ja.wikipedia.org/wiki/GP02 "wikilink")と[GD01](https://ja.wikipedia.org/wiki/GD01 "wikilink")が後に追加されている。2011年11月時点で、音声端末でHSPA+以上の高速通信に対応した端末は無かった(後に[GS03](https://ja.wikipedia.org/wiki/GS03 "wikilink")がHSPA+対応で発売)。2012年3月に予定される、[LTE](https://ja.wikipedia.org/wiki/LTE "wikilink")サービス開始に伴い、DC-HSDPAに対応していない基地局の運用については、当初からの5MHz幅分をHSPA+用途として、残り10MHz幅分をLTE用途に運用する方針のため、当該エリアでのDC-HSDPAサービスは受けられない可能性がある。なお、すでにDC-HSDPA運用を行っている基地局は、LTEは5MHz幅分のみ提供を行うため、下り最大37.5Mbpsサービスとなるとしている。ただし、2013年8月中旬以降、順次、DC-HSDPAのエリアを削減し、当該エリアを[EMOBILE LTEの](https://ja.wikipedia.org/wiki/EMOBILE_LTE "wikilink")75Mbps対応エリアに転換する方針を明らかにしており、その後は、[HSPA+](https://ja.wikipedia.org/wiki/HSPA+ "wikilink")のエリアとしてのみ利用可能な状態となる。なお、[2018年](../Page/2018年.md "wikilink")3月末を以て、同帯域での3Gネットワークが完全に停波された為、旧イー・アクセス契約の音声通話利用者は強制解約となった(旧イー・アクセス契約のデータサービスで、LTEが使用できないユーザーで、アップグレードを希望する利用者へ無償で607HWに交換された)。

[2011年](../Page/2011年.md "wikilink")2月25日より、ソフトバンクモバイル(現・[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")の[SoftBankブランド](../Page/SoftBank_\(携帯電話\).md "wikilink"))が開始したサービスは、[ULTRA SPEEDというブランドでなされ](https://ja.wikipedia.org/wiki/ULTRA_SPEED "wikilink")、2010年4月に再獲得した1.5GHz帯の10MHz幅すべてを用いて実現される。当初はデータ通信端末のみの提供であったが、後にスマートフォンでも対応機種が出た。また、[MVNO](https://ja.wikipedia.org/wiki/MVNO "wikilink")として[ウィルコム](../Page/ウィルコム.md "wikilink")の[WILLCOM CORE 3Gへも法人向けおよび](https://ja.wikipedia.org/wiki/WILLCOM_CORE_3G "wikilink")、条件を満たした個人向けに、[HX008ZT](https://ja.wikipedia.org/wiki/HX008ZT "wikilink")等を提供している。しかし、[2015年](../Page/2015年.md "wikilink")[11月3日](https://ja.wikipedia.org/wiki/11月3日 "wikilink")に新規受け付けが終了され、[2017年](../Page/2017年.md "wikilink")3月31日午前２時で、[1.5GHz帯](https://ja.wikipedia.org/wiki/1.5GHz帯 "wikilink")での3Gネットワークが停波した為、日本国内でのDC-HSDPAサービスは終了した\[5\]。

## DC-HSPA

**DC-HSPA** (Dual Cell High Speed Packet Access) とは、複数の基地局や周波数帯の帯域幅を広く利用することにより、上り下りともにDC-HSDPA以上の速度を実現する高速化規格の一つ。現時点では、下り最大84Mbps・168Mbpsが規格化されている。

日本国内での商用サービスの提供は、DC-HSDPAの展開終了やLTEサービスへの帯域使用などの理由により、事実上不可となっている。

## 次世代通信技術への移行

HSPAを標準技術とする[第3.5世代移動通信システム](../Page/第3.5世代移動通信システム.md "wikilink")とLTE（[Long Term Evolution](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink")）を標準技術とする[第3.9世代移動通信システム](https://ja.wikipedia.org/wiki/第3.9世代移動通信システム "wikilink")は[第3世代移動通信システム](../Page/第3世代移動通信システム.md "wikilink")から[第4世代移動通信システム](../Page/第4世代移動通信システム.md "wikilink")への過渡的な技術と位置づけられる\[6\]。

### 日本の状況

  - [NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")
    [2006年](../Page/2006年.md "wikilink")[8月31日](../Page/8月31日.md "wikilink")、サービス名称「[FOMAハイスピード](../Page/FOMAハイスピード.md "wikilink")」で[HSDPA規格に対応](https://ja.wikipedia.org/wiki/#HSDPA "wikilink")。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[4月1日](../Page/4月1日.md "wikilink")、最大受信通信速度7.2Mbps(カテゴリ8)のHSDPA通信サービス開始。[2009年](../Page/2009年.md "wikilink")1月、[人口カバー率](../Page/人口カバー率.md "wikilink")100%を達成\[7\]。2009年6月、[HSUPA規格に対応](https://ja.wikipedia.org/wiki/#HSUPA "wikilink")\[8\]。[2011年](../Page/2011年.md "wikilink")[6月13日](../Page/6月13日.md "wikilink")にHSDPAの14Mbpsサービスを開始した。HSPA+、DC-HSDPAの展開について言及はないが、代わりに[LTEサービスの](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink")[Xi(クロッシィ)を提供している](https://ja.wikipedia.org/wiki/Xi_\(携帯電話\) "wikilink")。
  - [ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")（旧・ボーダフォン日本法人）
    [2006年](../Page/2006年.md "wikilink")[10月1日](../Page/10月1日.md "wikilink")、サービス名称「[3G ハイスピード](../Page/3G_ハイスピード.md "wikilink")」で[HSDPA対応開始](https://ja.wikipedia.org/wiki/#HSDPA "wikilink")。[SoftBank 6-2停波後再獲得した](../Page/SoftBank_6-2.md "wikilink")[1.5GHz帯](https://ja.wikipedia.org/wiki/1.5GHz帯 "wikilink")を用い、2011年2月25日より、[ULTRA SPEEDのブランド名にてHSPA](https://ja.wikipedia.org/wiki/ULTRA_SPEED "wikilink")+、DC-HSDPAサービス開始した。同周波数帯を利用した音声端末は先行して2009年冬～[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")春モデルよりハイスペックモデル一部で順次発表されているが、ULTRA SPEEDには対応せずHSPAまでであった。2011年冬モデルでは1.5GHz帯のHSPA+に対応したスマートフォンを[ULTRA PHONEとして用意され](https://ja.wikipedia.org/wiki/ULTRA_PHONE "wikilink")、[2012年](../Page/2012年.md "wikilink")[5月29日](../Page/5月29日.md "wikilink")にはDC-HSDPAに対応する[106SHと](https://ja.wikipedia.org/wiki/SoftBank_106SH "wikilink")[101Fの発売が発表された](https://ja.wikipedia.org/wiki/SoftBank_101F "wikilink")。[2012年](../Page/2012年.md "wikilink")7月に900MHz帯でのHSPA+サービスが開始されるがULTRA SPEEDとしては扱われず、[3Gハイスピード](https://ja.wikipedia.org/wiki/3Gハイスピード "wikilink")(HSPA+対応)という扱いになる。なお、[2017年](../Page/2017年.md "wikilink")3月31日午前2時をもって、1.5GHz帯における3Gネットワークが停波され、DC-HSDPAのサービスは終了となり、以降の3Gサービスは、[2GHz帯](../Page/2GHz帯.md "wikilink")と[900MHz帯](https://ja.wikipedia.org/wiki/900MHz帯 "wikilink")による、HSPA+のサービスとなる。
  - [イー・アクセス](https://ja.wikipedia.org/wiki/イー・アクセス "wikilink")→[ソフトバンク](https://ja.wikipedia.org/wiki/ソフトバンク "wikilink")の[Y\!mobile](https://ja.wikipedia.org/wiki/Y!mobile "wikilink")部門
    [2007年](../Page/2007年.md "wikilink")[3月31日](../Page/3月31日.md "wikilink")、サービス名称「[EMモバイルブロードバンド](https://ja.wikipedia.org/wiki/EMモバイルブロードバンド "wikilink")」でHSDPA規格によるデータ通信サービス開始。2007年[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")、日本の携帯電話業界初最大受信通信速度7.2MbpsのHSDPAデータ通信サービス、2008年[11月20日](../Page/11月20日.md "wikilink")、日本の携帯電話業界初最大送信通信速度1.4MbpsのHSUPA通信サービスを開始。 [2009年](../Page/2009年.md "wikilink")[4月17日](../Page/4月17日.md "wikilink")、東名阪の主要ターミナル駅、空港等で、最大送信通信速度5.8Mbpsのサービスを開始。[2009年](../Page/2009年.md "wikilink")[7月24日](../Page/7月24日.md "wikilink")、HSPA+サービスを開始。[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[12月3日](../Page/12月3日.md "wikilink")より、DC-HSDPAサービスである[EMOBILE G4を開始](https://ja.wikipedia.org/wiki/EMOBILE_G4 "wikilink")（同時に、[EMOBILE G4ブランドにHSPA](https://ja.wikipedia.org/wiki/EMOBILE_G4 "wikilink")+方式も包括された）。音声端末は2009年末時点で、HSUPA対応端末はなかった（[S22HT](https://ja.wikipedia.org/wiki/S22HT "wikilink")のみHSDPA7.2Mbps対応）が、2010年2月、HSUPA(MAX1.4Mbps)対応端末として[H31IA](https://ja.wikipedia.org/wiki/H31IA "wikilink")発売。同年12月には同社[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")としては初のHSUPA(MAX5.8Mbps)対応端末として、[S31HT](https://ja.wikipedia.org/wiki/S31HT "wikilink")を発売。[2011年](../Page/2011年.md "wikilink")[12月1日](../Page/12月1日.md "wikilink")には、スマートフォンとしては初となるHSDPA最大14Mbps対応の[GS02](https://ja.wikipedia.org/wiki/GS02 "wikilink")を発売。そして2012年[6月14日](../Page/6月14日.md "wikilink")に初のHSPA+対応スマートフォンである[GS03](https://ja.wikipedia.org/wiki/GS03 "wikilink")を発売した。DC-HSDPA対応のスマートフォンについては、発売されないまま、DC-HSDPAに利用されている帯域の半分を2013年8月中旬以降順次LTEネットワークの帯域に転換するため、以降はDC-HSDPAの利用はできなくなるため、初のLTEスマートフォンとなった[GL07S](https://ja.wikipedia.org/wiki/GL07S "wikilink")にも、UMTS系統では、速度がHSPA+までの対応にとどまっている。LTE非対応のDC-HSDPAに対応するデータ端末についても、巻き取りを順次実施する計画を予定。さらに、[2018年](../Page/2018年.md "wikilink")[1月31日](../Page/1月31日.md "wikilink")を以て、3Gネットワークが停波された為、イー・モバイル及びイー・アクセス由来の3Gネットワークが終了され、旧イー・アクセス契約の音声端末やLTE非対応のデータ端末及び[Y\!mobile](https://ja.wikipedia.org/wiki/Y!mobile "wikilink")ブランドのタイプ2契約のスマートフォンは使用不可になった。

## 脚注

## 関連項目

  - [無線アクセス](../Page/無線アクセス.md "wikilink") - 無線[データ通信](../Page/データ通信.md "wikilink")の比較
  - [CDMA2000 1x](../Page/CDMA2000_1x.md "wikilink") - [CDMA2000](../Page/CDMA2000.md "wikilink")の高速データ通信拡張
  - [Long Term Evolution](https://ja.wikipedia.org/wiki/Long_Term_Evolution "wikilink")

[Category:携帯電話の通信規格](https://ja.wikipedia.org/wiki/Category:携帯電話の通信規格 "wikilink")

1.  谷口功『これだけ\!通信』2015年、秀和システム、95頁
2.  [外部リンク High Speed Downlink Packet Access (HSDPA); Overall description; Stage 2](http://www.3gpp.org/ftp/Specs/html-info/25308.htm)
3.
4.
5.   スマートフォン・携帯電話|url=[https://www.softbank.jp/mobile/network/1500-1700mhz/|website=ソフトバンク|accessdate=2020-10-04|language=ja](https://www.softbank.jp/mobile/network/1500-1700mhz/%7Cwebsite=ソフトバンク%7Caccessdate=2020-10-04%7Clanguage=ja)}}
6.  谷口功『これだけ\!通信』2015年、秀和システム、96頁
7.  [FOMAハイスピードエリアの人口カバー率100％を達成](http://www.nttdocomo.co.jp/info/news_release/page/090106_00.html) NTTドコモ
8.  [2009年度のお客様満足度の向上やCSRなどの取組みについて](http://www.nttdocomo.co.jp/info/news_release/page/090428_00.html) NTTドコモ