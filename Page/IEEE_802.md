> この記事は[IEEE 802](https://ja.wikipedia.org/wiki/IEEE_802)から翻訳されています。


**IEEE 802** とは、[IEEE](../Page/IEEE.md "wikilink")標準規格のうち、[ローカル・エリア・ネットワークなどの規格を定めたものである](../Page/Local_Area_Network.md "wikilink")。1980年2月に活動が開始されたことにより、802委員会と呼ばれるようになった。

より詳細には、IEEE 802標準が扱う範囲は、可変サイズのパケットを伝送するネットワークに限定される（対照的に、セルベース・ネットワークでは、セルと呼ばれる固定長で一様に伝送される。アイソクロナス（等時性）ネットワークは、オクテットやオクテット群を時刻基準通りに伝送する。これらは、IEEE 802規格の範囲にはない）。

IEEE 802のマップでは、[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")における7層のうち、データリンク層と物理層の二つの下位レイヤに位置するサービス及び[プロトコル](../Page/プロトコル.md "wikilink")が指定されている。そして、IEEE 802はOSIのデータリンク層を、二つのサブレイヤ（副層）、LLC (Logical link control)とMACに分割する。このため、構成は次のようになる。

  - データリンク層
      - LLC
      - MAC
  - 物理層

IEEE 802標準ファミリは、IEEE 802委員会、略称LMSC (LAN/MAN Standards Committee) の標準化委員会により整備される。最も広範に使用されているのは、[イーサネット](../Page/イーサネット.md "wikilink")、[トークン・リング](../Page/トークンリング.md "wikilink")、[無線LAN](../Page/無線LAN.md "wikilink")、ブリッジまたは仮想ブリッジLANである。それぞれの標準ごとに、独立した委員会（WG：ワーキンググループ）が存在している。

委員会の一覧：

  -
    {|class="wikitable"

\!WG \!WG名 \!英語名称 \!日本語名称(\*) |- |[IEEE 802.1](../Page/IEEE_802.1.md "wikilink") |HILI |Higher layer LAN protocols |高位レベル・レイヤ・インタフェース |- |[IEEE 802.2](https://ja.wikipedia.org/wiki/IEEE_802.2 "wikilink") |LLC（休会中） |Logical link control |論理リンク制御| |- |[IEEE 802.3](https://ja.wikipedia.org/wiki/IEEE_802.3 "wikilink") |CSMA/CD(Ethernet) |Ethernet (Formerly : Carrier Sense Multiple Access with Collision Detection) |[イーサネット](../Page/イーサネット.md "wikilink")（旧：衝突検出機能付き搬送波感知多重アクセス方式） |- |[IEEE 802.4](https://ja.wikipedia.org/wiki/IEEE_802.4 "wikilink") |Token bus（解散） |Token bus |[トークン・バス](https://ja.wikipedia.org/wiki/トークン・バス "wikilink") |- |[IEEE 802.5](https://ja.wikipedia.org/wiki/IEEE_802.5 "wikilink") |Token Ring（休会中） |Token Ring |[トークン・リング](../Page/トークンリング.md "wikilink") |- |[IEEE 802.6](https://ja.wikipedia.org/wiki/IEEE_802.6 "wikilink") |MAN（解散） |Metropolitan Area Network |都市域ネットワーク |- |[IEEE 802.7](https://ja.wikipedia.org/wiki/IEEE_802.7 "wikilink") |Broadband TAG（解散） |Broadband Techniacal Advisary Group |ブロードバンドLAN技術アドバイザリー・グループ |- |[IEEE 802.8](https://ja.wikipedia.org/wiki/IEEE_802.8 "wikilink") |Fiber Optic TAG（解散） |Fiber Optic Technical Advisary Group |光ファイバ技術アドバイザリー・グループ |- |[IEEE 802.9](https://ja.wikipedia.org/wiki/IEEE_802.9 "wikilink") |IS LAN（解散） |Integrated Services LAN |サービス統合型LAN |- |[IEEE 802.10](https://ja.wikipedia.org/wiki/IEEE_802.10 "wikilink") |SILS（解散） |Standard for Interoperable LAN/MAN Security |LAN/MANセキュリティ |- |[IEEE 802.11](../Page/IEEE_802.11.md "wikilink") |WLAN |Wireless LAN |[無線LAN](../Page/無線LAN.md "wikilink") |- |[IEEE 802.12](https://ja.wikipedia.org/wiki/IEEE_802.12 "wikilink") |Demand Priority（休会中） |Demand Priority |デマンド優先方式 |- |[IEEE 802.13](https://ja.wikipedia.org/wiki/IEEE_802.13 "wikilink") |Used for 100BASE-X Ethernet |unlucky number |未使用番号 |- |[IEEE 802.14](https://ja.wikipedia.org/wiki/IEEE_802.14 "wikilink") |Cable Modem（解散） |Cable Modem |ケーブル・モデム |- |[IEEE 802.15](../Page/IEEE_802.15.md "wikilink") |WPAN |Wireless PAN |[無線個人用ネットワーク](https://ja.wikipedia.org/wiki/無線センサネットワーク "wikilink") |- |[IEEE 802.15.1](../Page/Bluetooth.md "wikilink") |[Bluetooth](../Page/Bluetooth.md "wikilink") certification | |ブルートゥース |- |[IEEE 802.15.2](https://ja.wikipedia.org/wiki/IEEE_802.15.2 "wikilink") | |[IEEE 802.15](../Page/IEEE_802.15.md "wikilink") and [IEEE 802.11](../Page/IEEE_802.11.md "wikilink") coexistence |無線LAN（[IEEE 802.11b](https://ja.wikipedia.org/wiki/IEEE_802.11b "wikilink")）と無線PANの互換性を保つため |- |[IEEE 802.16](https://ja.wikipedia.org/wiki/IEEE_802.16 "wikilink") |BWA |Broadband wireless access ([WiMAX](https://ja.wikipedia.org/wiki/WiMAX "wikilink") |広帯域無線アクセス |- |[IEEE 802.17](https://ja.wikipedia.org/wiki/IEEE_802.17 "wikilink") |RPR |Resilient packet ring |（リング型転送方式） |- |[IEEE 802.18](https://ja.wikipedia.org/wiki/IEEE_802.18 "wikilink") |Radio Regulatory TAG |Radio Regulatory TAG |（無線規制に関する技術アドバイザリー・グループ） |- |[IEEE 802.19](https://ja.wikipedia.org/wiki/IEEE_802.19 "wikilink") |Coexistence TAG |Coexistence TAG |（他の標準規格との共存に関する技術アドバイザリー・グループ） |- |[IEEE 802.20](../Page/IEEE_802.20.md "wikilink") |Mobile Broadband Wireless Access |Mobile Broadband Wireless Access |（移動体広帯域無線アクセス） |- |[IEEE 802.21](https://ja.wikipedia.org/wiki/IEEE_802.21 "wikilink") |Media Independent Handoff |Media Independent Handoff |（無線システム間ハンドオーバー） |- |<span style="white-space: nowrap;">[IEEE 802.22](https://ja.wikipedia.org/wiki/IEEE_802.22 "wikilink")</span> |Wireless Regional Area Network |Wireless Regional Area Network |（地域無線ネットワーク） |- |} **注意**　(\*)日本語名称のうち、括弧内は正確なものではない。

## 関連項目

  - [コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")

## 外部リンク

  - [802 Committee website](http://www.ieee802.org/) (英語)
  - [各WGの一覧](http://grouper.ieee.org/groups/802/dots.html) （英語）

[Category:IEEE_802](https://ja.wikipedia.org/wiki/Category:IEEE_802 "wikilink") [Category:IEEE標準](https://ja.wikipedia.org/wiki/Category:IEEE標準 "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")