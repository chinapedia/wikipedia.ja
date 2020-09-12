> この記事は[IBM標準モジュラーシステム](https://ja.wikipedia.org/wiki/IBM標準モジュラーシステム)から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:SMScard.jpg "wikilink") [サムネイル中型コンピュータのSMSカード](https://ja.wikipedia.org/wiki/ファイル:IBM_1401_card_cage.agr.jpg "wikilink") \]\]

**標準モジュラーシステム (ひょうじゅんモジュラーシステム、Standard Modular System = SMS)**とは、1950年代後半に[IBM](../Page/IBM.md "wikilink")が開発した標準的な[トランジスタ](../Page/トランジスタ.md "wikilink")化された回路基板とマウントラックのシステムで、当初は[IBM 7030 Stretchのために開発された](../Page/IBM_7030.md "wikilink")\[1\]。 これらは、IBMの第2世代コンピュータ、周辺機器、 [7000シリーズ](https://ja.wikipedia.org/wiki/IBM_700/7000_series "wikilink") 、 [1400シリーズ](https://ja.wikipedia.org/wiki/IBM_1400 "wikilink") 、および[1620の全てに使用されていた](../Page/IBM_1620.md "wikilink")。 SMSは、1964年に[System/360](https://ja.wikipedia.org/wiki/System/360 "wikilink")で導入された[ソリッド・ロジック・テクノロジー](../Page/IBMソリッド・ロジック・テクノロジ.md "wikilink") (Solid Logic Technology = SLT)に取って代わられたが、1970年代までレガシーシステムで使用されていた。

System/360の一部でありながら、第2世代の設計から採用された多くのIBM周辺機器は、新しいSLTの代わりにSMS回路を使用し続けている。 これらには、[240xシリーズテープドライブ](https://ja.wikipedia.org/wiki/9トラックテープ "wikilink")とコントローラ、 [2540カードリーダー/パンチと](https://ja.wikipedia.org/wiki/IBM_2540 "wikilink")[1403N1プリンタ](https://ja.wikipedia.org/wiki/IBM_1403 "wikilink") 、1403と2540用の[2821統合コントロールユニット](https://ja.wikipedia.org/wiki/IBM_2821コントロールユニット "wikilink")が含まれていた。 System/360周辺機器で使用されているSMSカードの中には、SLTタイプのハイブリッドICが搭載されているものもある\[2\]。

SMSカードは、片面紙エポキシ[プリント回路基板に実装された](../Page/プリント基板.md "wikilink")[個別のコンポーネントで構成されている](../Page/電子部品.md "wikilink")。 シングル幅のカードは、16ピンの金メッキ [エッジコネクタを備えた](https://ja.wikipedia.org/wiki/エッジ・コネクタ "wikilink")2.5インチ幅、4.5インチ高、0.056インチ厚である。 倍幅のカードは5.375インチ幅、4.5インチ高で、2つの16ピン金メッキエッジコネクタを備えている。 接点は、最初のエッジコネクタには*A–R* (*I*と*Oを*スキップ)、2番目のエッジコネクタには*S–Z、1–8の*ラベルが付けられている。

カードは、カードケージのバックプレーンに接続され、エッジコネクタの接点は[ワイヤーラップピンに接続されている](../Page/ワイヤラッピング.md "wikilink")。 電源バスラインを除いて、すべての相互接続はワイヤーラップ接続で行われる。 バックプレーンのワイヤーラップ接続は、ほとんどが工場で自動化された装置で行われていたが、ワイヤーラップ技術により、カスタマーエンジニアによる技術的変更の現場設置が容易になった。

一部のカードタイプは、回路構成を変更するために切断することができる「プログラムキャップ」（15個の接続を持つダブルレールの金属ジャンパーバー）を介してカスタマイズすることができる。 「プログラムキャップ」付きのカードタイプは、標準構成用にあらかじめカットされてたものが付属しており、カスタマーエンジニアが現場で異なる構成を必要とする場合は、必要に応じて追加のカットを行うことができる。 この機能は、カスタマーエンジニアが顧客サイトに持ち運ばなければならない異なるカードタイプの数を減らすことを目的としていた。

カードタイプは、カードにエンボス加工された2〜4文字のコードである(例: *MX、ALQなど* )。 カードに「プログラムキャップ」が付いている場合、コードは2文字のカードタイプコードと2文字の「キャップ接続」コード(例: *AK ZZ* )に分類される。

SMSが最初に開発された当初、IBMは、数百種類の標準カードタイプのセットがあれば、必要なものはすべてそろい、設計、製造、保守がより簡単になると予測していた。 しかし残念ながら、それは楽観的過ぎることが判明し、SMSカードの種類はすぐに2500種類以上に増えてしまった。 成長の理由の一部は、カードが使用される多くの異なるシステムの要件を満たすために、[アナログ回路](../Page/アナログ回路.md "wikilink")だけでなく、複数の[デジタル](../Page/デジタル.md "wikilink") [ロジック・ファミリー](../Page/汎用ロジックIC.md "wikilink")(ECL、RTL、DTLなど)が実装されていたことである。

ファイル:IBM SMS card component side.agr.jpg.jpg|IBM 1401のSMSカード ファイル:IBM SMS card circuit side.agr.jpg.jpg|同じSMSカードの回路側 ファイル:SMS card with power transistors.agr.jpg|IBM 1401のSMSカード ファイル:IBM 1401 card cage 2.agr.jpg|IBM 1401カードケージ ファイル:IBM 1401 backplane.agr.jpg|同じ1401カードケージの[ワイヤラップ](../Page/ワイヤラッピング.md "wikilink")・[バックプレーン](../Page/バックプレーン.md "wikilink") ファイル:IBM 7070.jpg|[IBM 7070カードケージ](https://ja.wikipedia.org/wiki/IBM_7070 "wikilink")

## 脚注

## 外部リンク

  - [カスタマーエンジニアリングインストラクションリファレンス、標準モジュラーシステム](http://www.piercefuller.com/scan/ibm-223-6900-2.pdf?id=ibm-223-6900-2) PDF
  - [IBMの標準モジュラーシステム（SMS）カード](http://members.optushome.com.au/intaretro/SMSCards.htm)
  - <http://ibm-1401.info/index.html>
      - <http://ibm-1401.info/IBM-StandardModularSystem-Neff7.pdf>
  - [IBM SMSカードデータベース](http://files.righto.com/sms/)

[Category:IBMのメインフレーム](https://ja.wikipedia.org/wiki/Category:IBMのメインフレーム "wikilink") [Category:初期のコンピュータ](https://ja.wikipedia.org/wiki/Category:初期のコンピュータ "wikilink") [Category:IBMの製品](https://ja.wikipedia.org/wiki/Category:IBMの製品 "wikilink")

1.
2.