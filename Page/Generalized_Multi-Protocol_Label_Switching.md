> この記事は[Generalized Multi-Protocol Label Switching](https://ja.wikipedia.org/wiki/Generalized_Multi-Protocol_Label_Switching)から翻訳されています。


**Generalized Multi-protocol label switching** (**GMPLS**) は、[光通信](../Page/光通信.md "wikilink")ネットワーク上で多様な[通信プロトコル](../Page/通信プロトコル.md "wikilink")を統合して経路制御する技術である。[MPLSを](../Page/Multi-Protocol_Label_Switching.md "wikilink")[IP以外にも適応可能なように拡張するもので](../Page/Internet_Protocol.md "wikilink")[IETFで標準化がすすめられている](../Page/Internet_Engineering_Task_Force.md "wikilink")。また、日本国内においては[PILを中心として](https://ja.wikipedia.org/wiki/Photonic_Internet_Lab. "wikilink")、米国においては[ISOCORE](https://ja.wikipedia.org/wiki/ISOCORE "wikilink")を中心として相互接続性検証や標準化への貢献が進められてきている。

## GMPLSの仕組み

光波長、タイムスロット、装置のポート番号等をラベルとして定義し、ラベルスイッチの交換操作を行うための経路設定を共通的な設定プロトコルで行う。

歴史的には、光波長に対する検討 Multi-Protocol Lambda Switching から開始された。 光信号を光のまま波長を元に経路設定し、光スイッチによる交換操作をし、[波長分割多重伝送を行う](../Page/光波長多重通信.md "wikilink")。

そのことにより、以下のことが可能になる。

  - 交換処理を単純化して高速化する。
  - 障害発生時に瞬時に代替経路への切り替えを行う。
  - 多様な通信プロトコルを波長ごとに割り当てて多重化する。

## 関連項目

  - [Multi-Protocol Label Switching](../Page/Multi-Protocol_Label_Switching.md "wikilink")

## 外部リンク

  - RFC 3473: Generalized Multi-Protocol Label Switching (GMPLS) Signaling Resource ReserVation Protocol-Traffic Engineering (RSVP-TE) Extensions
  - RFC 3945: Generalized Multi-Protocol Label Switching (GMPLS) Architecture

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")