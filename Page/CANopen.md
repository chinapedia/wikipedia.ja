> この記事は[CANopen](https://ja.wikipedia.org/wiki/CANopen)から翻訳されています。


**CANopen**（きゃんおーぷん）とは、オートメーションシステム内の[組み込みシステム](../Page/組み込みシステム.md "wikilink")用の通信プロトコルおよびデバイス[プロファイル仕様である](https://ja.wikipedia.org/wiki/プロファイル_\(工学\) "wikilink")。[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")のネットワーク層から上の層を実装している。CANopenは、アドレッシングスキーム、いくつかの小規模な通信プロトコル、デバイスプロファイルによって定義されたアプリケーション層から構成される。[Controller Area Networkをベースとしており](https://ja.wikipedia.org/wiki/Controller_Area_Network "wikilink")、オープンネットワークのひとつでもある。

## 概要

[組み込みシステム](../Page/組み込みシステム.md "wikilink")のネットワーク技術として、簡易に[マルチマスタのネットワークを構築することができる](https://ja.wikipedia.org/wiki/マルチマスタバス "wikilink")。CANopenは、仕様が一般に公開されている上位[ソフトウエア](https://ja.wikipedia.org/wiki/ソフトウエア "wikilink")である。

[2004年](../Page/2004年.md "wikilink")12月にドイツの非営利団体[:de:CAN in Automationが](https://ja.wikipedia.org/wiki/:de:CAN_in_Automation "wikilink")、最初に通信プロファイルであるDS-301をリリースした。このときのバージョンはv4.02である。

その他に約20の機器（デバイス）の標準仕様が策定されており、モータやリモートI/Oなどの仕様書が作成されている。実際に使われているアプリケーションとして、[新幹線](../Page/新幹線.md "wikilink")などもある。一番大きなCANが使われているシステムとしては、[CERN](https://ja.wikipedia.org/wiki/CERN "wikilink")の実験施設があり、数十万ノードのCANが使われている。

通信速度は、1Mbps。ハードウェアが再送処理を行うので、ノイズが多い環境でもソフトウエアの処理が不要である。推奨されている通信レートと配線長の組合せがある。 一つのネットワークに127個のノードが接続できる。ただし、CAN自体が柔軟なネットワークなので、拡張することが可能である。

通信は、PDOおよびSDOで構成され、NMTによるブートアップが定義されている。

## CANopenのネットワーク構成

CANopenのノードは、コンシューマーとプロデューサーで構成される。

  - コンシューマー
    コンシューマーは、情報を受け取り、利用する側である。

<!-- end list -->

  - プロデューサー
    プロデューサーは、情報を管理し、発信する側である。

## CANopenのレイヤ構造

上記のデータリンク層は、OSIモデルの第2層となる。第1層の物理層は、CANトランシーバーと呼ばれる。

## CANopenのプロファイル

CANopenには、チップの違いを吸収する通信プロファイルDS-301が定義されている。NECエレクトロニクス、ルネサス、富士通デバイスその他、約50の世界中のチップメーカから発売されているCAN内蔵マイコンやCANコントローラの違いを吸収している。

CAN in Automationによれば共通プロファイルが、DS-3xx（ディーエス300番台）で定義されており、通信プロファイルのDS-301だけでなく、コネクタやワイヤを定義したプロファイルも用意されている。

## 接続手順の実際

CANopenのマスターは、CANopenスレーブノードからハートビートまたはガーディングによって基本立ち上げされる。

## CANおよびCANの国際規格

ISOおよびIEC文書で、CANおよびCANopenの規格が定められている。

  - CAN - [国際規格](../Page/国際規格.md "wikilink") ISO 11898, ISO 15765, ISO 11519
  - CANopen - [欧州規格](https://ja.wikipedia.org/wiki/欧州規格 "wikilink") EN 50325-4

## 外部リンク

  - [CAN in Automation](http://www.can-cia.org/)

[Category:インタフェース規格](https://ja.wikipedia.org/wiki/Category:インタフェース規格 "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:自動車電子技術](https://ja.wikipedia.org/wiki/Category:自動車電子技術 "wikilink")