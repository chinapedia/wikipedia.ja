> この記事は[ExpressCard](https://ja.wikipedia.org/wiki/ExpressCard)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:PCCard-ExpressCard.png "wikilink")\]\] [Logitec_LPM-ECSA32.jpg](https://ja.wikipedia.org/wiki/File:Logitec_LPM-ECSA32.jpg "fig:Logitec_LPM-ECSA32.jpg") [Expresscard_34.jpg](https://ja.wikipedia.org/wiki/File:Expresscard_34.jpg "fig:Expresscard_34.jpg") **Express Card**（エクスプレスカード）は、[PCカード](../Page/PCカード.md "wikilink")に代わる[パソコン](../Page/パーソナルコンピュータ.md "wikilink")（[ノートパソコン](../Page/ノートパソコン.md "wikilink")）用小型カード型[インターフェース](../Page/インタフェース_\(情報技術\).md "wikilink")、およびその規格による[拡張カード](../Page/拡張カード.md "wikilink")。[IBM](../Page/IBM.md "wikilink")、[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、[テキサス・インスツルメンツ](../Page/テキサス・インスツルメンツ.md "wikilink")、[デル](../Page/デル.md "wikilink")、[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[レキサー・メディア](../Page/レキサー・メディア.md "wikilink")、SCM Microsystemsといった各社の協業で、規格策定団体[PCMCIA](https://ja.wikipedia.org/wiki/PCMCIA "wikilink")において[2003年](../Page/2003年.md "wikilink")に策定された。

## 概要

PCカードの後継として開発されたものである。PCカードがデスクトップPC用の拡張バス規格[ISAを](../Page/Industry_Standard_Architecture.md "wikilink")、CardBusでは[PCIバスを基にモバイル向けに規格化されて来ているように](../Page/Peripheral_Component_Interconnect.md "wikilink")、ExpressCardではPCI ExpressバスとUSB2.0を基に設計・規格化されている。バスの性能・能力的には、現在PCカードで使われている機能は、再設計によってすべてExpressCardに置き換えることも可能である。ただし、PCカードとの物理的な[互換性](../Page/互換性.md "wikilink")はない。

接続インタフェースにはPCI Express x1とUSB2.0が用いられ、通常はそのうちのどちらか一方を使用する。サイズは幅が34mmのExpressCard/34と54mm のExpressCard/54があり、どちらも長さ75mm、厚み5mmである。製品にExpressCard[スロット](https://ja.wikipedia.org/wiki/スロット "wikilink")を搭載する際、「ExpressCard/34カード」又は「ExpressCard/34及びExpressCard/54」に対応し利用出来る事が条件となっている。

各社のノートPCがPCI Expressに対応した[チップセット](../Page/チップセット.md "wikilink")を採用するに連れてExpressCardの採用例も一定数存在していた。

PC Card/CardBusからExpressCardへの移行は[2005年](../Page/2005年.md "wikilink")頃から本格的に始まった。傾向としてはコンシューマ向けノートPCの対応が早く、一方の法人向け製品ではCardBusの採用や併設が長く続いており、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")頃まではCardBusスロットを持つ製品の提供されていた。 移行の特に初期では、[筐体](../Page/筐体.md "wikilink")寸法に余裕のある大型の機種でPCカードとExpressCardの両スロット併設とした例や、本体・ドッキングステーションのいずれか片方にExpressCardスロット、もう一方にCardBusスロットを配置する製品なども提供された。

[2018年](../Page/2018年.md "wikilink")現在、ExpressCardを搭載するノートPCはほとんど存在しない。理由はいくつか考えられ、後発となる[USB3.0](https://ja.wikipedia.org/wiki/USB3.0 "wikilink")や[Thunderbolt](https://ja.wikipedia.org/wiki/Thunderbolt "wikilink")などの利便性に優れた規格に代替されていったことや、[Ultrabook](https://ja.wikipedia.org/wiki/Ultrabook "wikilink")に代表される小型薄型化により物理的なスペース確保が難しくなったこと、ノートPCのコストダウンが一段と進んだ影響によりコネクタの実装すら省かれつつあることなどが挙げられる。

## ピン配列

| ピン | 信号               |
| -- | ---------------- |
| 1  | GROUND           |
| 2  | USB データ-         |
| 3  | USB データ+         |
| 4  | CP USB \#        |
| 5  | 予備               |
| 6  | 予備               |
| 7  | 予備               |
| 8  | SMBus CLK        |
| 9  | SMBus データ        |
| 10 | \+1.6V           |
| 11 | WAKE \#          |
| 12 | \+3.3V AUX       |
| 13 | Power Switch \#  |
| 14 | \+3.3V           |
| 15 | \+3.3V           |
| 16 | Clock Request \# |
| 17 | CPPE \#          |
| 18 | Ref CLK-         |
| 19 | Ref CLK+         |
| 20 | GROUND           |
| 21 | PERn0            |
| 22 | PERp0            |
| 23 | GROUND           |
| 24 | PETn0            |
| 25 | PETp0            |
| 26 | GROUND           |

  - 1 - 5ピンがUSB2.0端子、10 - 26ピンがPCI Express端子。

## データ通信カード

現在、[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")や[イー・モバイル](../Page/イー・モバイル.md "wikilink")などからExpressCard型のデータ通信カードが発売されている。

  - NTTドコモ向け
      - ~~[OP2502 HIGH-SPEED](../Page/OP2502_HIGH-SPEED.md "wikilink")~~発売されなかった。
      - [L-07A](https://ja.wikipedia.org/wiki/L-07A "wikilink")
      - [F-06C](https://ja.wikipedia.org/wiki/F-06C "wikilink")…Xi対応。
  - [イー・モバイル](../Page/イー・モバイル.md "wikilink")向け
      - ~~[D02OP](https://ja.wikipedia.org/wiki/D02OP "wikilink")~~販売開始後に自主回収となった。
      - [D03HW](https://ja.wikipedia.org/wiki/D03HW "wikilink")
      - [D24HW](https://ja.wikipedia.org/wiki/D24HW "wikilink")
  - [WILLCOM](https://ja.wikipedia.org/wiki/WILLCOM "wikilink")向け
      - [WS008HA](https://ja.wikipedia.org/wiki/WS008HA "wikilink")
  - au（KDDI・沖縄セルラー電話連合）向け
      - [W06K](https://ja.wikipedia.org/wiki/W06K "wikilink")
      - [W07K](https://ja.wikipedia.org/wiki/W07K "wikilink")
      - [HID02](https://ja.wikipedia.org/wiki/HID02 "wikilink")･･･[UQコミュニケーションズ](https://ja.wikipedia.org/wiki/UQコミュニケーションズ "wikilink")の[MVNO](https://ja.wikipedia.org/wiki/MVNO "wikilink")による[モバイルWiMAX](https://ja.wikipedia.org/wiki/モバイルWiMAX "wikilink")（[+WiMAX](https://ja.wikipedia.org/wiki/+WiMAX "wikilink")ブランド）とのデュアル契約用端末（定額料金対応）
      - [HID04](https://ja.wikipedia.org/wiki/HID04 "wikilink")･･･同上（従量制料金対応）
  - [WILLCOM CORE 3G向け](https://ja.wikipedia.org/wiki/WILLCOM_CORE_3G "wikilink")
      - [HX007ZT](https://ja.wikipedia.org/wiki/HX007ZT "wikilink")

## 関連項目

  - [拡張カード](../Page/拡張カード.md "wikilink")
  - [PCI Express](../Page/PCI_Express.md "wikilink")
  - [PCカード](../Page/PCカード.md "wikilink")

## 外部リンク

  - [About ExpressCard Technology](http://www.usb.org/developers/expresscard) ([USB-IF](https://ja.wikipedia.org/wiki/:en:USB_Implementers_Forum "wikilink"))

  -
  - [allpinouts.org - PCI Express Card and PCI Express Mini Card Connector Pinout](http://www.allpinouts.org/index.php/PCI_Express_Card_and_PCI_Express_Mini_Card)

  - <http://www.itproportal.com/2011/04/01/expresscard-format-be-discontinued/>

[Category:拡張カード](https://ja.wikipedia.org/wiki/Category:拡張カード "wikilink") [Category:PCI_Express](https://ja.wikipedia.org/wiki/Category:PCI_Express "wikilink") [Category:USB](https://ja.wikipedia.org/wiki/Category:USB "wikilink")