> この記事は[HomePNA](https://ja.wikipedia.org/wiki/HomePNA)から翻訳されています。


**HomePNA**とは、現存する家庭内の電話線を用い、インターネット接続を行うための規格である。規格を推進する団体名、**Home Phoneline Networking Alliance**の略でもあり、*HPNA*、*Home PNA*、*Home Phoneline Networking*、*Homepna*とも書かれる。

## 概要

Home Phoneline Networking Allianceは非営利団体であり、Epigram・[3Com](https://ja.wikipedia.org/wiki/3Com "wikilink")・[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")・[AT\&T](../Page/AT&T.md "wikilink")・[コンパック](../Page/コンパック.md "wikilink")・[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")・[IBM](../Page/IBM.md "wikilink")・[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")・[ルーセント・テクノロジー](https://ja.wikipedia.org/wiki/ルーセント・テクノロジー "wikilink")・[ロックウェル](https://ja.wikipedia.org/wiki/ロックウェル "wikilink")・Tut Systemsなど、150を超える会社が参加している。この団体は、HomePNAに関する通信・コンピュータ関連技術・ネットワーク製品の互換性を確立することを目的としている。団体自身は標準を推し進めないものの、[国際電気通信連合](../Page/国際電気通信連合.md "wikilink")（ITU）に標準化についての助言を行っている。

この団体のメンバーは企画に沿った製造を行うものの、この団体自体は何らかの製造を行うことはない。しかしながら、規格に適合した製品には「Home Phoneline Network Certified™」として認証を行っている。現在の認証規格は「Specifications 3.0」であり、これは2003年からHomePNA 3.0と呼ばれている。 [HomePNAのロゴ](http://upload.wikimedia.org/wikipedia/en/1/1b/HomePNA.jpg)

## 歴史

バージョン1.0の技術はTut Systems社が開発し、バージョン2.0の技術は、より発展的な役割を果たしたEpigram社が開発した。バージョン3.0の技術は、[Broadcom](https://ja.wikipedia.org/wiki/Broadcom "wikilink")社とイスラエルのCoppergate solutions社により開発された。この発展の歴史については、Epigram社のジャック・ハロウェイとエド・フランクによって書かれた文書がある[1](http://www.homepna.org/docs/paper500.pdf)（英語、PDF）。

バージョン2.0は国際電気通信連合により承認を受け、ITU G.989.1として世界標準になり、続いてG989.2およびG989.3（Phoneline Networking Transceivers）が承認された。

なお、この団体のマーケティング担当責任者であるデイビッド・トマソンは、「私たちはリダイアルして出直し、この技術規格の改名を行いたいと望んでいる。しかし、私たちはそのことで困っている」（"I wish we could redial and go back and rename this whole technology, but we're stuck with it,"[2](http://www.nwfusion.com/net.worker/columnists/2001/0903kistner.html)）と言っている。無視された初期バージョンのHomePNAに関して、この混乱を非難する人もいる。

## HomePNA 3.0規格

HomePNA 3.0はこれらに継続した新しい技術であり、家庭内の電話回線を利用して[LANのような使い方ができる](../Page/Local_Area_Network.md "wikilink")。単体のPCで受信されたデータは、[ルータ](https://ja.wikipedia.org/wiki/ルータ "wikilink")を介さずに他のPCと共有することができる。PCはHomePNA 3.0を通して、他のPCの周辺機器など、たとえば[プリンタや](https://ja.wikipedia.org/wiki/プリンター "wikilink")[ファイルストレージにアクセスでき](../Page/補助記憶装置.md "wikilink")、また[オンラインゲーム](../Page/オンラインゲーム.md "wikilink")で遊ぶこともできる。

HomePNA 3.0は、電話としての通話通信と、データアクセスのための通信のために、異なる周波数帯域を使用する。電話とファックスの通信は、全てのデータ通信より優先される。V92モデムは、すでにこのコンセプトを実装している。

なお、ネットワーク能力の拡大と、電話線のジャックの位置による制限を克服するために、HomePNA標準に同軸ケーブルを含める提案がなされている。

## 必要条件

HomePNA 3.0を利用するための必要条件は次の通り。

1.  電話線のジャックは単一の電話線から分岐したものであること（電話線が活線（電話局と繋がっている）である必要はない。たとえば北米の99%の電話線ではHomePNA 3.0がそのまま使用可能である。
2.  ハードウェアは認証を受けたものを使用する必要がある。一般に、最も必要なことは、アナログ信号とデジタル信号の変換を行うHomePNAカードのようなハードウェアである。しかし、逆にリストはブランド、ルータ、ソフトウェア、プロバイダ、イーサネット・ブリッジ、USBアダプターなどが次々に発売されることにより、かなり大きなものとなっている。いくつかのPCには、認証を受けたアダプターを標準装備している。平均的なユーザーは、通常HomePNAカードだけを必要とする。

## 利点

  - 電話、ファックス、DSLモデムによる通信は、HomePNAによるネットワーク通信とは別の帯域であるため、干渉は原理的に発生しない。このため、電話、HomePNAアダプタ、アナログモデム、DSLモデムなどが、1本の電話線で共存可能である。
  - 特別な、または新しい配線を家庭内に引き回す必要がない。
  - 別の階に電話回線がすでに敷設されていれば、LANと違ってすぐにそれを使い通信を始めることができる。
  - HomePNA 1.0の通信速度は1.0Mbpsに制限されていたが、HomePNA 3.0では128Mbpsの通信を行うことができる。これは、たいていのユーザーの要求を満たすのに十分な値である。さらに、大量のデータ転送を行いたい場合には、最大240Mbpsにまで拡張することができる。
  - 50台までの接続であれば、最大10Mbpsの通信を維持することができる。なお、これ以上台数を増やした場合には、通信速度が悪化する可能性が高い。
  - 装置間の距離は300mまで許容され、面積的には900平方メートルまで網展開することができる。
  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、Apple [Macintosh](../Page/Macintosh.md "wikilink")、[Linux](../Page/Linux.md "wikilink")での互換性を持っている。
  - 電話線は活線（電話局と繋がっている）である必要がない。
  - 必要となるハードウェアはそれほど高価ではない。
  - たとえば、居間のテレビで見ている放送を、HomePNA 3.0経由で寝室のテレビに転送できる可能性を持っている。[Wi-Fiや](../Page/無線LAN.md "wikilink")[Bluetooth](../Page/Bluetooth.md "wikilink")は、容易に動画を転送できるような帯域または安定性が無いことが多い。
  - HomePNA 3.0は将来、機器相互間の（異種ベンダ間の）互換性を持つ予定である。（たとえば、Wi-Fi無線LANや、ユニバーサルxDSL、電力線インターネット（HomePlug powerline alliance）のように）
  - HomePNA 3.0は、HomePNA 1.0規格およびHomePNA 2.0規格と下位互換性を持っている。
  - ブロードバンド・コンテンツ提供各社とサードパーティー各社は、認証を受けることで、単一のシンプルなパッケージで電話通信・インターネット通信・動画通信を提供することができる。
  - よく比較される電力線インターネット（PLC:[電力線搬送波通信](https://ja.wikipedia.org/wiki/電力線搬送波通信 "wikilink")）は、漏洩電波の問題が残っている（ただし日本では規則上解決はされ、2006年に製品化の目途が立っている）。
  - ひきかえ、HomePNA 2.0は国際電気通信連合に承認を受けた標準規格であり、Home Phoneline Network Certified™の承認を受けた製品は、（特に現地の行政庁の許可等が必要な場合を除いて）世界中で共通使用できる。
  - ホテル産業にとって、HomePNAはもっともコストパフォーマンスの高いサービス提供手段である。[3](http://www.nwfusion.com/net.worker/columnists/2001/0903kistner.html)（英語）

## 欠点

  - 代替手段である電力線インターネット（PLC:[電力線搬送波通信](https://ja.wikipedia.org/wiki/電力線搬送波通信 "wikilink")）も、多くの会社が互換性を目指して開発を続けている。日本ではパナソニック コミュニケーションズ株式会社(現パナソニック システムネットワークス)から2006年12月9日より国内発売が開始されており、以後各社から販売されている。そのため、HomePNAとの市場の競合が予想される。
  - 不適切な位置に設置された電話用ジャックは障害となりうる。
  - HomePNA 3.0を使用する多くの製品は、実際の転送速度がまだ確定していない。
  - 日本国内の場合、[VDSL](https://ja.wikipedia.org/wiki/VDSL "wikilink")との互換性の問題がある等その他諸事情により、一般にはあまり普及していない。（一部、[FTTx](../Page/FTTx.md "wikilink")の末端として10MbpsのHomePNAが導入された。一部の[CATVシステムなど](../Page/ケーブルテレビ.md "wikilink")、建物固有のFTTBシステム等での導入も見られる。）

## 外部リンク

  - [HomePNA公式サイト](http://www.homepna.org)（英語）
  - [簡潔な解説](http://www.homepna.org/connected/HomePNAindex.html)（英語）

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:有線通信](https://ja.wikipedia.org/wiki/Category:有線通信 "wikilink")