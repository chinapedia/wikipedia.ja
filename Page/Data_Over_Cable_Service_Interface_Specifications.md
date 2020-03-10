> この記事は[Data Over Cable Service Interface Specifications](https://ja.wikipedia.org/wiki/Data_Over_Cable_Service_Interface_Specifications)から翻訳されています。


**DOCSIS** (**Data Over Cable Service Interface Specifications**) は、北アメリカのMCNS (Multimedia Cable Network System Partners Limited) が推進し、SCTE（Society of Cable Telecommunications Engineers : CATV通信技術者協会）で承認され、[ITU-T](../Page/ITU-T.md "wikilink")のJ.112 Annex.Bで定められた、[同軸ケーブル](https://ja.wikipedia.org/wiki/同軸ケーブル "wikilink")での通信サービスの国際規格である。Cable Labs (Cable Television Laboratories) が認定・試験を行っている。日本語では通常「ドクシス」と発音される。

[ケーブルモデム](https://ja.wikipedia.org/wiki/ケーブルモデム "wikilink")・STB（[セットトップボックス](https://ja.wikipedia.org/wiki/セットトップボックス "wikilink")）の標準化によるコスト低減、[IP電話](../Page/IP電話.md "wikilink")・双方向[デジタル放送への対応などが行われている](../Page/デジタル放送の一覧.md "wikilink")。

## DOCSIS 1.0

[1996年](../Page/1996年.md "wikilink")に検討開始・[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[3月](https://ja.wikipedia.org/wiki/3月 "wikilink")規格制定・[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")認証試験開始。

以下の帯域共有型の[IP通信が可能である](../Page/Internet_Protocol.md "wikilink")。

  - 下り方向
      - アクセス方式 : [TDM](../Page/時分割多重化.md "wikilink")
      - 変調方式 : 30[Mbps](../Page/ビット毎秒.md "wikilink") (64[QAM](https://ja.wikipedia.org/wiki/QAM "wikilink")) / 42Mbps (256QAM)
      - 帯域幅 : 6MHz（使用周波数 : 88 - 860MHz）
  - 上り方向
      - アクセス方式 : [TDMA](https://ja.wikipedia.org/wiki/時分割多元接続 "wikilink")
      - 変調方式 : 5Mbps ([QPSK](https://ja.wikipedia.org/wiki/QPSK "wikilink")) / 10Mbps (16QAM)
      - 帯域幅 : 3.2MHz（使用周波数 : 200k/400k/800k/1600k/3200kHz）

<!-- end list -->

  - ケーブルモデムごとに1つの[Quality of Service](../Page/Quality_of_Service.md "wikilink") (QoS) の設定が可能。

## DOCSIS 1.1

DOCSIS 1.0のセキュリティ・QoS・[IPマルチキャスト](https://ja.wikipedia.org/wiki/IPマルチキャスト "wikilink")などを強化したものである。

  - Service Flow Control: IP電話・[インターネット](../Page/インターネット.md "wikilink")接続などのサービスタイプ毎に動的なQoSを設定することが可能。
  - リアルタイム通信の遅延を少なくするため、[パケット](../Page/パケット.md "wikilink")を小分けにするFragmentation機能。
  - BPIによる伝送路上の暗号化機能。

[1999年](../Page/1999年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")規格制定。

## DOCSIS 2.0

以下の高速化を行った。[2002年](../Page/2002年.md "wikilink")承認。

  - 下り6MHz帯域幅 : 30Mbps (64QAM) / 42Mbps (256QAM)
  - 上り6.4MHz帯域幅 : 30Mbps
      - A-TDMA 64QAM（Advanced Time Division Multiple Access - 次世代[時分割多元接続](https://ja.wikipedia.org/wiki/時分割多元接続 "wikilink")）
      - S-CDMA 128QAM（TCM : Synchronous Code Division Multiple Access - 同期[符号分割多元接続](../Page/符号分割多元接続.md "wikilink")）

## DOCSIS 3.0

  - [チャネルボンディング](https://ja.wikipedia.org/wiki/チャネルボンディング "wikilink")
      - 帯域を複数束ねて通信することができる。例えば、下り160Mbps（40Mbps 256QAMを4本多重）、上り120Mbps（30Mbps を4本多重）。
  - [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")対応
  - M-CMTS
  - [AES暗号化](../Page/Advanced_Encryption_Standard.md "wikilink")

2010年10月1日、[知多メディアスネットワーク](../Page/知多メディアスネットワーク.md "wikilink")は8波ボンディングにより実測で下り最大270Mbpsのサービスを開始した。この速度は、サービス開始時において、日本のケーブルインターネット最高速である\[1\]。

日本ケーブルラボは、222MHzから450MHzの32波・256QAMを使用し、一本の幹線で下り1.2Gbpsを一検討例として示した\[2\]。

## DOCSIS 3.1

2013年10月に規格化。下り最大10Gbps、上り最大1Gbps。下位の規格に対し、OFDMの採用や使用周波数帯域の拡張といった特徴がある\[3\]\[4\]。

2016年2月には、[Full Duplex](https://ja.wikipedia.org/wiki/複信 "wikilink") DOCSIS 3.1が発表された。Full Duplex DOCSIS 3.1は、下り上りともに最大10Gbps\[5\]。

## Packet Cable

Packet Cableは、[ケーブルテレビ](../Page/ケーブルテレビ.md "wikilink")でのIP電話サービスの標準を定めたものである。[MGCP](https://ja.wikipedia.org/wiki/MGCP "wikilink") (Media Gateway Control Protocol) ・NCS (Network-based Call Signaling protocol) を呼制御の[通信プロトコル](../Page/通信プロトコル.md "wikilink")に使用する。

  - Packet Cable1.0 - [固定電話](https://ja.wikipedia.org/wiki/固定電話 "wikilink")と併用するIP電話。
  - Packet Cable1.1 - 固定電話を置き換え可能なIP電話。
  - Packet Cable1.2 - 事業者間通信の制御。
  - Packet Cable2.0 - [テレビ電話](https://ja.wikipedia.org/wiki/テレビ電話 "wikilink")などのマルチメディア対応。

## 出典

## 関連項目

  - [モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")

  - (CMTS)

  - [High-Definition Multimedia Interface](https://ja.wikipedia.org/wiki/High-Definition_Multimedia_Interface "wikilink")

  - (MoCA)

  - [常時接続](https://ja.wikipedia.org/wiki/常時接続 "wikilink")

  - [HFC](../Page/HFC.md "wikilink")

## 外部リンク

  - [日本ケーブルラボ](http://www.jcl.or.jp/)
  - [社団法人日本ケーブルテレビ連盟](http://www.catv-jcta.jp/)
  - [社団法人日本CATV技術協会](http://www.catv.or.jp/jctea/)
  - [伊藤忠ケーブルシステム DOCSIS 3.0](http://www.itochu-cable.co.jp/products/docsis/)
  - [モトローラ ケーブルモデムシステム](http://www.motorola.jp/broadband/cablemodem.html)
  - [CableLabs](http://www.cablemodem.com/)
  - [docsis.org](http://www.docsis.org/)
  - [Cable Europe](http://www.cableeurope.eu/) (Euro-DOCSIS)

[Category:放送](https://ja.wikipedia.org/wiki/Category:放送 "wikilink") [Category:情報機器](https://ja.wikipedia.org/wiki/Category:情報機器 "wikilink") [Category:アンテナ](https://ja.wikipedia.org/wiki/Category:アンテナ "wikilink") [Category:ケーブルテレビ](https://ja.wikipedia.org/wiki/Category:ケーブルテレビ "wikilink") [Category:有線通信](https://ja.wikipedia.org/wiki/Category:有線通信 "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.
3.
4.
5.