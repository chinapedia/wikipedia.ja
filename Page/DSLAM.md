> この記事は[DSLAM](https://ja.wikipedia.org/wiki/DSLAM)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Outdoor_DSLAM.JPG "wikilink") **DSLAM**（**Digital Subscriber Line Access Multiplexer**）は、[デジタル加入者線](../Page/デジタル加入者線.md "wikilink") (DSL) で使われるネットワーク機器である。電話局側にあり、複数の加入者線を[多重化](https://ja.wikipedia.org/wiki/多重化 "wikilink")して、高速な[インターネットバックボーン](https://ja.wikipedia.org/wiki/インターネットバックボーン "wikilink")に接続する\[1\]。電話会社の[電話交換機](https://ja.wikipedia.org/wiki/電話交換機 "wikilink")とは遠隔にDSLAMを配置することで、DSLサービスの提供可能な距離を伸ばすことができる。

## DSLAM までのデータ経路

[XDSL_Connectivity_Diagram_en.svg](https://ja.wikipedia.org/wiki/File:XDSL_Connectivity_Diagram_en.svg "fig:XDSL_Connectivity_Diagram_en.svg")

1.  住宅/商業施設などの発信源: 加入者のコンピュータがDSLモデムに接続される。
2.  [ローカルループ](https://ja.wikipedia.org/wiki/ローカルループ "wikilink"): 加入者宅から最寄りの電話局までの（電話会社が所有する）電話回線。[ラストワンマイル](https://ja.wikipedia.org/wiki/ラストワンマイル "wikilink")とも呼ばれる。
3.  [中央集配線盤](https://ja.wikipedia.org/wiki/主配線盤 "wikilink") (MDF): 加入者向けの配線と内部の配線を相互接続するための集線盤。デジタル加入者線では、スプリッタで配線を分岐しDSLAMに接続する。
4.  DSLAM: [DSLサービスのための機器](../Page/デジタル加入者線.md "wikilink")。

## DSLAM の役割

DSLAMには多数のDSLモデムポートがあり、そこから入ってきた[デジタル信号](../Page/デジタル信号.md "wikilink")を集め、[多重化](https://ja.wikipedia.org/wiki/多重化 "wikilink")してひとつの信号にする。DSLAMの機種によっては、DSL以外にも [Asynchronous Transfer Mode](../Page/Asynchronous_Transfer_Mode.md "wikilink") (ATM)、[フレームリレー](https://ja.wikipedia.org/wiki/フレームリレー "wikilink")、[IPネットワーク](../Page/Internet_Protocol.md "wikilink")（後述するIP-DSLAM）なども多重化する。

多重化された信号は局内の基幹交換機を通して最大10Gbit/sの[アクセスネットワーク](https://ja.wikipedia.org/wiki/アクセスネットワーク "wikilink")に接続され、[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")に送られる。

[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")でいえば、DSLAMは純粋な[データリンク層](https://ja.wikipedia.org/wiki/データリンク層 "wikilink")の装置であり、巨大な[スイッチングハブ](../Page/スイッチングハブ.md "wikilink")のような働きをする。

DSLAMは必ずしも電話局に設置されるとは限らず、より加入者に近い局外設置もある（これをSAI、Serving Area Interface という）。これと[FTTx](https://ja.wikipedia.org/wiki/FTTx "wikilink")を組み合わせることもある。

DSLAMは[マルチプレクサ](https://ja.wikipedia.org/wiki/マルチプレクサ "wikilink")というだけでなく、DSLモデムの集合体でもある。各モデムは加入者側のDSLモデムと通信する。モデム群はDSLAMとして一体化しており、個別の[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")がハードウェアとして独立して内蔵されているわけではない。従来のモデムと同様、このDSLモデムは回線を調べ、最大データ転送速度を出せるように適応する能力がある。物理的には同じ[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")を使っていても、[イーサネット](../Page/イーサネット.md "wikilink")よりもDSLサービスの方が長距離の通信が可能なのは、このためでもある。

## 速度と距離

[VDSLAM_in_Aachen.jpg](https://ja.wikipedia.org/wiki/File:VDSLAM_in_Aachen.jpg "fig:VDSLAM_in_Aachen.jpg") ツイストペアケーブルでは、周波数が高いほど減衰が激しい。従って、DSLAMと加入者の距離が長いほど、データ転送レートは低くなる。以下に距離とデータ転送レートの大まかな関係を示す。実際の条件によっても大きく変化するが、2kmを超える場合は、より近い場所にDSLAMを設置しないとそれなりの転送速度は得られない。

  - 25 Mbit/s - 約300m
  - 24 Mbit/s - 約600m
  - 23 Mbit/s - 約900m
  - 22 Mbit/s - 約1.2km
  - 21 Mbit/s - 約1.5km
  - 19 Mbit/s - 約1.8km
  - 16 Mbit/s - 約2.1km
  - 1.5 Mbit/s - 約2.8km
  - 800 kbit/s - 約5.2km

（0.40mm銅線の場合）

## 追加機能

DSLAMは、加入者から上流の[ルーター](../Page/ルーター.md "wikilink")に渡す際に[VLANトラフィックにタグ付けする機能を持っていることがある](https://ja.wikipedia.org/wiki/Virtual_Local_Area_Network "wikilink")。完全な[ファイアウォール](../Page/ファイアウォール.md "wikilink")というわけではないが、パケットフィルタリングを行うDSLAMもあり、ポート間トラフィックを排除したり、特定の[通信プロトコル](../Page/通信プロトコル.md "wikilink")のパケットを排除する。

DSLAMはまた、[DiffServ](../Page/DiffServ.md "wikilink") や[優先度付きキュー](https://ja.wikipedia.org/wiki/優先度付きキュー "wikilink")などの [Quality of Service](https://ja.wikipedia.org/wiki/Quality_of_Service "wikilink") (QoS) をサポートしている。

## ハードウェアの詳細

加入者のコンピュータは[ADSL](../Page/ADSL.md "wikilink")モデムやDSL[ルーター](../Page/ルーター.md "wikilink")経由で普通の[ツイストペアケーブル](../Page/ツイストペアケーブル.md "wikilink")の電話線で[公衆交換電話網](https://ja.wikipedia.org/wiki/公衆交換電話網 "wikilink")と接続され、DSLAMに接続される。DSLAMには複数の集合カードがあり、各カードには複数の[入出力ポート](../Page/入出力ポート.md "wikilink")があって、それぞれが加入者の線と接続される。典型的な集合カードには24個程度のポートがあるが、個数は機種によって異なる。DSLAMを格納する筐体には48[ボルトの](../Page/ボルト_\(単位\).md "wikilink")[直流](../Page/直流.md "wikilink")電源が供給される。典型的なDSLAMには、電源装置、DSLAM筐体、集合カード、ケーブル、上流リンクが含まれる。上流リンクとしては、[ギガビット・イーサネット](https://ja.wikipedia.org/wiki/ギガビット・イーサネット "wikilink")や数ギガビットの[光ファイバー](https://ja.wikipedia.org/wiki/光ファイバー "wikilink")リンクが使われることが多い。

## IP-DSLAM

[IP](../Page/Internet_Protocol.md "wikilink")-DSLAM (*Internet Protocol Digital Subscriber Line Access Multiplexer*) は、トラフィックのほとんどをIPベースで行うものである。

従来のDSLAMは、上流に[ATMルーター](../Page/Asynchronous_Transfer_Mode.md "wikilink")/スイッチがあって、ATM回線で接続されていた。そして、ATMルーター/スイッチでIPトラフィックを抽出して、IPネットワークに渡していた。IP-DSLAM では、DSLAM自身がIPトラフィックを抽出する。従って、高価なATM機器が不要となり、同時に機能的にも向上する。

## 脚注

## 関連項目

  - [ADSL](../Page/ADSL.md "wikilink")
  - [ブロードバンドインターネット接続](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")

## 外部リンク

  - [Google Directory](../Page/Googleのサービス.md "wikilink"): [DSL Vendors](http://www.google.com/Top/Computers/Data_Communications/DSL/Vendors/)
  - [Technical whitepaper on merging fiber with DSLAM](http://www.convergedigest.com/blueprints/ttp03/z2critical1.asp?ID=38&ctgy=Loop)

[Category:通信機器](https://ja.wikipedia.org/wiki/Category:通信機器 "wikilink") [Category:インターネット接続](https://ja.wikipedia.org/wiki/Category:インターネット接続 "wikilink")

1.