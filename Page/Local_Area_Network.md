> この記事は[Local Area Network](https://ja.wikipedia.org/wiki/Local_Area_Network)から翻訳されています。


[Local_Area_Network_Topology_Image.png](https://ja.wikipedia.org/wiki/File:Local_Area_Network_Topology_Image.png "fig:Local_Area_Network_Topology_Image.png") **Local Area Network**（ローカル・エリア・ネットワーク。**LAN**）とは、企業、官庁のオフィスや工場などの事業所、学校、家庭などで使用される[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")である。 狭義にはイーサネットに代表される通信ケーブルとデータリンク層の技術方式、規格を指し、広義には事業所内、家庭内で使用される[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")と情報処理システムを指す場合がある。 本項では狭義の技術方式、規格について解説する。

歴史的経緯から初期の技術規格として可能な配線長が数百ｍ程度であったことから、室内、建物内を主な対象とする意味でLocal Area Networkという名称であるが、現在では数十kmの延長が可能な規格も存在する。

## 概説

LANの標準化組織である[米国電気電子技術者協会](../Page/IEEE.md "wikilink")（IEEE）や[国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")（ISO）での定義によると

1.  限定された広がりをもつ地域で、コンピュータをはじめとする様々な機器の間で自由に情報交換ができる。
2.  導入したユーザーが主体となって管理・運営する（[電気通信事業者](../Page/電気通信事業者.md "wikilink")資格が不要）。
3.  異なる[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")で作成された機器をLANに接続でき、相互に通信可能（マルチベンダ接続）。

といった特徴をもっている。

本項では狭義の技術方式、規格の種類と歴史を概観する。個別の方式の構成や動作についてはそれぞれの見出し項目を参照されたい。 また本項で解説する単独のLANを複数組み合わせた広義のLANである事業所内LAN、企業内LANなどについては、該当の節を参照されたい。

## LANの種類

LANが商用化される初期の時期に規格化されたLANの種類には次のものが存在する。

  - **[イーサネット](../Page/イーサネット.md "wikilink")** (**Ethernet**、DIX規格、[Ethernet II](https://ja.wikipedia.org/wiki/Ethernet_II "wikilink")、[IEEE](../Page/IEEE.md "wikilink") 802.3)
  - **[トークンバス](https://ja.wikipedia.org/wiki/トークンバス "wikilink")** (**Token Bus**、IEEE 802.4)
  - **[トークンリング](../Page/トークンリング.md "wikilink")** (**Token Ring**、IEEE 802.5)
  - **[FDDI](https://ja.wikipedia.org/wiki/FDDI "wikilink")**(**Fiber-distributed data interface**、ANSI X3T9.5など)

この内イーサネットが商業的な普及を広め、以後それを高速化した後継規格がデファクト・スタンダードとなっている。

近年は無線方式による、[無線LAN](../Page/無線LAN.md "wikilink")（[IEEE 802.11シリーズ](../Page/IEEE_802.11.md "wikilink")）も普及している。

[HomePNA](../Page/HomePNA.md "wikilink")は家庭内の既設[電話線を利用するLANである](../Page/ツイストペアケーブル.md "wikilink")。

既設の電灯線・配電線を利用する[PLCも家庭内LANの新技術として注目されている](../Page/電力線搬送通信.md "wikilink")。

## LANの歴史

LANの発祥の一つである[イーサネット](../Page/イーサネット.md "wikilink")は1973年に米[Xerox](https://ja.wikipedia.org/wiki/Xerox "wikilink")[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")で[ロバート・メトカーフ](../Page/ロバート・メトカーフ.md "wikilink")を中心に開発された。 これに先立つ基となる研究として1960年代中頃の[ポール・バラン](../Page/ポール・バラン.md "wikilink")(アメリカ)または[ドナルド・デービス](https://ja.wikipedia.org/wiki/ドナルド・デービス "wikilink")(イギリス)による[パケット通信](../Page/パケット通信.md "wikilink")、1970年頃のハワイ大学における[ALOHAプロジェクトによる](../Page/ALOHAnet.md "wikilink")[多重ランダムアクセス通信方式の研究がある](../Page/ALOHA.md "wikilink")。

1980年2月に[IEEE 802委員会が発足する](https://ja.wikipedia.org/wiki/IEEE_802委員会 "wikilink")。これは可変サイズのパケットを伝送するネットワークに関する検討を目的としたものであった。 この年DIX規格のEthernet Iが発表される。

1982年、DIX規格のEthernet IIが発表される。

1983年、IEEE 802.3 10Base5が標準化される。

1984年、IEEE 802.3a 10Base2が標準化される。米IBMがトークンリングを開発する。

1987年、[アメリカ国家規格協会(ANSI)でFDDIが標準化される](https://ja.wikipedia.org/wiki/ANSI "wikilink")。

1990年、IEEE 802.3i 10Base-Tが標準化される。

1995年、IEEE 802.3u 100Base-TXが標準化される。

1998年、IEEE 802.3z 1000Base-SX、LXが標準化される。

1999年、IEEE 802.3ab 1000Base-Tが標準化される。

2006年、IEEE 802.3an 10GBase-Tが標準化される。

その後40GigabitEthernet、100GigabitEthernetの開発が続いている。

## LANの分類

レイヤについては**[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")を参照のこと。**

### トポロジーによる分類（レイヤ1）

トポロジー（形状）による分類では、**スター型**、**バス型**、**リング型**の3つに分類される。これらは各規格における伝送媒体と接続機器の実装により形成されるものである。

  - **スター型LAN**は、中央に集線装置である[ハブを置き](../Page/ハブ_\(ネットワーク機器\).md "wikilink")、すべての端末を接続する形である。配置の変更が柔軟に行え、故障箇所の特定もしやすいことから、広く普及している。ただし、ハブ部分で故障が起きた場合には全端末で相互通信が不可能になるため、信頼性が必要な場合はハブを二重化するなどの対策をとることが多い。例として[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")(撚り対線)を利用した[イーサネット](../Page/イーサネット.md "wikilink")([10Base-T](https://ja.wikipedia.org/wiki/10Base-T "wikilink")、100Base-TX、1000Base-T等)、トークンリング\[1\]がある。
  - **バス型LAN**は、バスと呼ばれる伝送路に接続する形であり、基幹ケーブルに短冊状に端末がぶら下がるような形となる。バス上の一部で故障が発生した場合、故障点を超える通信は不可能になる。構成上バスを増やす以外に信頼性向上の手段がないため、信頼性向上は難しい。例として同軸ケーブルを用いるイーサネット(10Base5、10Base2)、[トークンバス](https://ja.wikipedia.org/wiki/トークンバス "wikilink")がある。
  - **リング型LAN**は、端末を順次伝送路につないでいく形であり、伝送路が数珠つなぎの円形となる。伝送路及び伝送路機器に障害が発生するとLANが停止するため、伝送路を2重にする場合が多い。また2重化することにより、途中、伝送路機器の故障、伝送路の切断などの各種障害に対し非常に強くなるため、基幹用に用いられることが多い。例として[FDDI](https://ja.wikipedia.org/wiki/FDDI "wikilink")がある。

Image:Topoloxía en estrela.png|スター型 Image:Topoloxía en bus.png|バス型 Image:Topoloxía en anel.png|リング型

LANのトポロジーに関する議論は、伝送媒体(ケーブル、光ケーブル)とデータリンク層を接続する機器間で共有するイーサネット(10Base5、10Base2)、[FDDI](https://ja.wikipedia.org/wiki/FDDI "wikilink")が現役であった1990年代までは意義のあるところだったが、その後のLANスイッチの普及拡大により、近年ではほぼすべてがスター型配線になっている。

### 伝送媒体による分類

各規格において使用する伝送媒体が定められている。主な例として[同軸ケーブル](../Page/同軸ケーブル.md "wikilink")、[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")(撚り対線)、[光ファイバー](../Page/光ファイバー.md "wikilink")、[無線](../Page/無線.md "wikilink")(大気の電波伝播)が利用される。

| 標準名称         | 規格名称       | 伝送媒体                                   |
| ------------ | ---------- | -------------------------------------- |
| IEEE 802.3   | 10Base5    | 外径9.5mm、特性インピーダンス50Ωの同軸ケーブル(Thickケーブル) |
| IEEE 802.3a  | 10Base2    | 外径5mm、特性インピーダンス50Ωの同軸ケーブル(Thinケーブル)    |
| IEEE 802.3i  | 10BASE-T   | カテゴリ3以上のツイステッド・ペア・ケーブル                 |
| IEEE 802.3u  | 100Base-TX | カテゴリ5以上のツイステッド・ペア・ケーブル                 |
| IEEE 802.3ab | 1000Base-T | カテゴリ5e以上のツイステッド・ペア・ケーブル                |

### 変調方式による分類（レイヤ1）

変調方式による分類では、[ベースバンド](https://ja.wikipedia.org/wiki/ベースバンド "wikilink")方式と[ブロードバンド](https://ja.wikipedia.org/wiki/ブロードバンド "wikilink")方式に分けられる。

  - **ベースバンド方式**は、コンピュータで扱われるディジタルデータを符号化し、変調せずに電気パルスとして伝送路に送信する方式である。イーサネットや[FDDI](https://ja.wikipedia.org/wiki/FDDI "wikilink") (TP-PMD, CDDI) がこの方式である。
  - **ブロードバンド方式**は、コンピュータで扱われるディジタルデータを符号化し、変調して搬送波としてアナログ伝送路に送信する方式である。IEEE 802.4（[トークン・バス](https://ja.wikipedia.org/wiki/トークン・バス "wikilink")）がこの方式である。

## 広義のLAN(大規模LAN)

LANの最も基本的な構成はケーブルとデータリンク層を共有する単独のLANである。それについては本項で種類を解説した。 企業などの事業所内で利用するコンピューターネットワークとしてのLANでは、複数のLANを[ブリッジ](../Page/ブリッジ_\(ネットワーク機器\).md "wikilink")、[ルーター](../Page/ルーター.md "wikilink")、[LANスイッチ](../Page/LANスイッチ.md "wikilink")を用いて接続し、ネットワークを拡張する。 ネットワークの拡張に当たってはLAN技術以外にシリアル回線、ATM、[WDM伝送装置などが利用される場合がある](../Page/光波長多重通信.md "wikilink")。 広義のLAN(大規模LAN)の構成や方式については先に述べたものの他に[IP(Internet Protocol)や関係する技術](../Page/Internet_Protocol.md "wikilink")、さらに上位レイヤも含めた技術の複合体として成り立っている。 これらの話題についてはネットワーク構築、(情報)システム構築の分野の技術として、関係する書籍などの情報を参照されたい。

## 脚注

## 関連項目

  - [Wide Area Network](../Page/Wide_Area_Network.md "wikilink")
  - [イーサネット](../Page/イーサネット.md "wikilink")（Ethernet）
  - [イントラネット](../Page/イントラネット.md "wikilink")
  - [トークンリング](../Page/トークンリング.md "wikilink")（Token Ring）
  - [IEEE 802.11](../Page/IEEE_802.11.md "wikilink")
  - [LANパーティー](../Page/LANパーティー.md "wikilink")

[Category:コンピュータネットワーク](https://ja.wikipedia.org/wiki/Category:コンピュータネットワーク "wikilink")

1.  トークンリングという名称であるが、配線、機器の実装はツイストペアケーブルによるスター型トポロジーである。