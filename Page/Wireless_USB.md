> この記事は[Wireless USB](https://ja.wikipedia.org/wiki/Wireless_USB)から翻訳されています。


**Wireless USB**（ワイヤレスUSB、**WUSB**）とは、コンピュータ用の無線接続の通信技術のひとつで、短い距離を結ぶ有線通信である[USBを拡張して](../Page/ユニバーサル・シリアル・バス.md "wikilink")、[有線通信](https://ja.wikipedia.org/wiki/有線通信 "wikilink")の安全性と速度を確保しながら、[無線通信](../Page/無線通信.md "wikilink")の使いやすさを持つ技術規格である。

[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")、[ビデオカメラ](../Page/ビデオカメラ.md "wikilink")、[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")、[DVD](../Page/DVD.md "wikilink")機器等の大容量データ転送用途を想定している。

## 規格

[2004年](../Page/2004年.md "wikilink")[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")に、WUSBの規格を策定するための推進団体としてWireless USB Promoter Groupが発足した。同グループには、Agere Systems（現[LSIコーポレーション](../Page/LSIコーポレーション.md "wikilink")）、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink") (HP)、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[日本電気](../Page/日本電気.md "wikilink") (NEC)、[フィリップス](../Page/フィリップス.md "wikilink")、[サムスン電子](../Page/サムスン電子.md "wikilink")が参加している。

[2005年](../Page/2005年.md "wikilink")[5月](https://ja.wikipedia.org/wiki/5月 "wikilink")にはWireless USB Specification 1.0の仕様が完成したことがアナウンスされたが、ホストとデバイス間の初回の接続手順を定めたAssociation Model部分の標準化が難航し、結局同モデルの標準は[2006年](../Page/2006年.md "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")に公開された。そのためWUSBを搭載した最終製品の出荷は2006年後半までずれ込んだ。またマイクロソフトも、[Windows Vistaのリリース版にはWUSB用の](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")は収録されないことを明らかにしている。

[2017年](../Page/2017年.md "wikilink")現在、WUSBに対応した[パソコンや](../Page/パーソナルコンピュータ.md "wikilink")[周辺機器](../Page/周辺機器.md "wikilink")はほとんど市場に出てきておらず、日本国内では、Y-E DATAから発売されたワイヤレスUSB対応レシーバーとワイヤレスUSB対応USBハブのセット品と、[Lavie](https://ja.wikipedia.org/wiki/Lavie "wikilink") Jシリーズの最上位機種でワイヤレスUSB対応PCとワイヤレスUSB対応USBハブのセットが発売されたのみにとどまっている。

## 技術

### PHY

WUSBは、数[GHzもの超広帯域を用いる無線技術である](../Page/ギガヘルツ.md "wikilink")[UWB](../Page/超広帯域無線.md "wikilink") (Ultra wideband) をベースに[スペクトラム拡散](../Page/スペクトラム拡散.md "wikilink") (Spread spectrum) 技術を使用している。アメリカ連邦通信委員会 (FCC) ではUWBを『最高輻射の中心周波数に対して輻射電力が10[dB下がる周波数帯域幅が](../Page/デシベル.md "wikilink")500[MHz以上](https://ja.wikipedia.org/wiki/メガヘルツ "wikilink")、または中心周波数の20%以上の無線通信』と定義している。

物理層・MAC層の規格としては[WiMedia Allianceが推進するMB](https://ja.wikipedia.org/wiki/WiMedia_Alliance "wikilink")-OFDM方式を採用している。米国では軍事技術として開発されたUWBであったが、2002年2月に民生機器での利用が認められた。

通信速度はホスト・デバイス間の距離等により変化することがあり物理層で53.3-480Mbpsをサポートする。ホスト・デバイス間距離3メートルで480Mbps、10メートルで110Mbpsの性能を目標として設計されている。

### MAC以上

データ転送は128ビットAESで暗号化される。1つのホストが同時にすべてのデバイスと通信できるため、有線のUSBと異なり、ハブは仕様上存在しない。ただし有線のUSBデバイスをWireless USBにつなぐための有線USBデバイスからみるとハブ的な動作をするデバイスクラスは定義されており、"Device Wire Adapter" (DWA) と呼ばれる。現在市販されている有線USBの先につなぐことのできるWireless USBの親機はWireless USBの仕様上の「ホスト」である。

1つのバス上のデバイスは127個で有線と同じ。論理層では有線USBとほとんど同様の仕様になっているが、無線の性質を反映してアイソクロナス転送の仕様は異なっており、一定数の再送などを行う（有線USBでは再送は行わない）、40Mbpsまでに制限されるなどの差異がある。

WUSBはスタートポロジを使用し、1台のホストで最大127台のデバイスに対応する。いわゆるDual-role Device（ホストとデバイス両方の機能を持つ機器）にも対応しており、例えば[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")が[コンピュータ](../Page/コンピュータ.md "wikilink")に接続されているときはクライアントとして動作し、[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")に直接画像を送るときにはホストとして動作する。

## 他の無線方式との比較

<table>
<caption><u>Wireless USBと主な無線機器の通信方法の比較</u>[1]</caption>
<thead>
<tr class="header">
<th><p>規格名</p></th>
<th><p>Wireless USB<br />
Specification Rev. 1.0</p></th>
<th><p><a href="../Page/IEEE_802.11.md" title="wikilink">IEEE 802.11</a> a/b/g/n/ac</p></th>
<th><p><a href="../Page/Bluetooth.md" title="wikilink">Bluetooth</a> 5.0(HS)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>周波数帯域</p></td>
<td><p>3.1GHz～10.6GHz</p></td>
<td><p>2.4GHz/5.0GHz〜5-1GHz</p></td>
<td><p>2.4GHz</p></td>
</tr>
<tr class="even">
<td><p>伝送速度<br />
（通信距離）</p></td>
<td><p>最大60Mbps (3m) ,<br />
14Mbps (10m)</p></td>
<td><p>最大6933Mbps<br />
(100m)</p></td>
<td><p>最大4Mbps<br />
（1m～100m 出力に依存）</p></td>
</tr>
<tr class="odd">
<td><p>変調方式</p></td>
<td><p>MB-OFDM</p></td>
<td><p>DSSS、DBPSK、DQPSK、<br />
CCK、OFDMなど</p></td>
<td><p>GFSK</p></td>
</tr>
</tbody>
</table>

|        |                                            |                                            |                                            |
| ------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| CCK:   | Complementary code keying                  | EDR:                                       | Enhanced data rate                         |
| DBPSK: | Differential binary phase shift keying     | GFSK:                                      | Gaussian frequency shift keying            |
| DQPSK: | Differential quadrature phase shift keying | MB-OFDM:                                   | Multiband-OFDM                             |
| DSSS:  | Direct sequence spread spectrum            | [OFDM](../Page/直交周波数分割多重方式.md "wikilink"): | Orthogonal frequency division multiplexing |

## 各国の無線周波数比較

[Wireless_USB_frequency_band_assignment.PNG](https://ja.wikipedia.org/wiki/File:Wireless_USB_frequency_band_assignment.PNG "fig:Wireless_USB_frequency_band_assignment.PNG")

## CWUSB (Certified WirelessUSB™)

Cypress Semiconductor社は "WirelessUSB™" という2.4 GHzの[ISMバンド](../Page/ISMバンド.md "wikilink")を使用したプロトコルを発表しているが、これは上述の "Wireless USB" とは関係ない。WirelessUSBの通信範囲は10～50メートルで、入力デバイス向けに設計されている。現在、[ベルキン](https://ja.wikipedia.org/wiki/ベルキン "wikilink")、[ロジテック](../Page/ロジテック.md "wikilink")、[バーチャルインク](https://ja.wikipedia.org/wiki/バーチャルインク "wikilink")より製品が提供されている。

**CWUSB** (Certified WirelessUSB™) のロゴ使用及びCWUSBの製品発売（市場投入）は、USB-IF (USB Forum, Inc.) の試験、認可が必要で、認可されたCWUSB製品は、USB-IFの公式サイトで確認することができる。 Certified WirelessUSBリスティング製品（認可承認された製品）は、下記USB-IFのURLに掲載公開されている。

<http://www.usb.org/kcompliance/view/catalog_search/sselect_item/process/refresh?dev_categories=All%20Categories&retail_categories=All%20Categories&hispeed=wireless&referring_url=http%3A//www.usb.org/about&step%3Aint=2&sitemlist_orderby=profile&sitemlist_dir=0&&batch_size=10&sitemlist_start=31>

## 現状

一時期は「Bluetoothを統合してワイヤレスUSBが標準規格となる」という市場予測もあったが、Windows標準でサポートされない事（ハブに対し、別途ドライバやユーティリティのインストールが必要）や、Wireless USBと競合関係にあるWireless USBより長距離の通信に対応した無線LAN対応USBデバイスサーバーやUSBデバイスサーバー搭載無線LANルーターの存在などにより、[2017年](../Page/2017年.md "wikilink")現在、ワイヤレスUSB対応PCも、ワイヤレスUSB対応USBハブも発売されることはなくなっている。

現在では、メーカー独自規格のワイヤレスUSBレシーバーと、ワイヤレス対応周辺機器をワイヤレスで直接接続する事が主流になっており、マウスやキーボードなどで多数製品が発売されている。

## 脚注

<references/>

## 関連項目

  - [超広帯域無線](../Page/超広帯域無線.md "wikilink")(UWB)
  - [ユニバーサル・シリアル・バス](../Page/ユニバーサル・シリアル・バス.md "wikilink") (USB)
  - [Bluetooth](../Page/Bluetooth.md "wikilink")
  - [無線LAN](../Page/無線LAN.md "wikilink")
  - [Personal Area Network](https://ja.wikipedia.org/wiki/Personal_Area_Network "wikilink")

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink") [Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink")

1.  日経エレクトロニクス 2007/10/8