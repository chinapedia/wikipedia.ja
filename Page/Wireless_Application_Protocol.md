> この記事は[Wireless Application Protocol](https://ja.wikipedia.org/wiki/Wireless_Application_Protocol)から翻訳されています。


**Wireless Application Protocol**（ワイヤレス アプリケーション プロトコル、略称: **WAP**）は [携帯電話](../Page/携帯電話.md "wikilink")などのデバイスで[インターネット](../Page/インターネット.md "wikilink")閲覧などのサービスが行えるようにする為の技術仕様である。

## 概要

それまで業界標準規格がなかった携帯電話インターネットの技術仕様として、WAPは誕生した。

WAP 1.xで使われるコンテンツ記述言語は[Wireless Markup Language](../Page/Wireless_Markup_Language.md "wikilink") (WML) であった。しかし、インターネット標準の[HTMLとは互換性が無く](../Page/HyperText_Markup_Language.md "wikilink")、コンテンツ作成にはWML用のオーサリングツールが必要であり、不便であった。また、当時の利用可能な携帯電話による通信環境は9.6kbpsのCSD接続があるばかりでパケットは無いというような時代であり、コンテンツも主にテキスト、[液晶](../Page/液晶.md "wikilink")はモノクロという時代であった。そのためコンテンツがそろわず、更にオペレータによる閲覧可能なサイトの制限もあり、全世界的にあまり良い評判を得ることは出来なかった。

日本ではIDO/DDIセルラーフォングループ（のちの[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")）は[PDC](../Page/PDC.md "wikilink")を打ち切って[CDMAを選んだのと同じ理由でWAPを採用した](../Page/符号分割多元接続.md "wikilink")。一方で[NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")はWAPを採用せずに、主要機種においては[Compact HTMLを元にした独自の](../Page/Compact_HTML.md "wikilink")[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")を採用した（ただし特定用途に限定された端末についてはその限りではなく、例えば[JRAの](../Page/日本中央競馬会.md "wikilink")[電話投票](../Page/電話投票.md "wikilink")用端末である「モバイルゲット」（1999年11月発売）などではWAPを搭載している\[1\]）。

WAP技術の標準化・推進組織は[WAP Forumであったが](https://ja.wikipedia.org/wiki/WAP_Forum "wikilink")、発展的解消という形で他の標準化団体とならんで、2002年6月に[オープン・モバイル・アライアンス](https://ja.wikipedia.org/wiki/オープン・モバイル・アライアンス "wikilink") (OMA) に統合された。

## WAP 2.0

その後の携帯電話は、[GPRS](https://ja.wikipedia.org/wiki/GSM#GPRS "wikilink")、[EDGEおよび](../Page/Enhanced_Data_Rates_for_GSM_Evolution.md "wikilink")[第三世代携帯電話](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")などのパケットベースでの通信が比較的安価に利用できるようになり、また、液晶のカラー化、カメラ搭載なども進んで、携帯電話インターネットサービスを広く利用する環境は整いつつあった。

WAP 2.0では、WAP 1.xの失敗を踏まえ、インターネットで標準的に使われている技術が大幅に採用された。コンテンツ記述言語としては従来までのWMLとならんで[XHTML MPと](../Page/XHTML_Mobile_Profile.md "wikilink")[cHTML](https://ja.wikipedia.org/wiki/cHTML "wikilink")が妥協の産物として併記され、トランスポートプロトコルとしては従来までのWTP/WSPとならんで[TCP/IPを採用した](../Page/インターネット・プロトコル・スイート.md "wikilink")。これにより一層のコンテンツ利用の拡大をはかることになった。現在、WAP1.x時代からの標準であった、WML、WTP、WSPはcHTMLとともに消えゆく存在となりつつある。

過去、携帯電話によるブラウジングとメッセージングは、WAP Forumの後継団体であるOMAが制定したものが業界標準であり、それはWAP1.x/2.0をもとにしたものであった。国際的には、圧倒的多数の携帯電話はOMAの仕様をもとにした実装をしていた。しかしながら、通信速度の更なる向上と[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")や[Androidといったオープンプラットホームの存在は](../Page/Android_\(オペレーティングシステム\).md "wikilink")、OMA仕様自体の意味を完全に減殺し、WAPは過去のものとなった。

[写メール](../Page/写メール.md "wikilink")や[iショット](https://ja.wikipedia.org/wiki/iショット "wikilink")などの日本発のピクチャーメール規格は、国際標準となることは出来なかった。業界標準のマルチメディア携帯メール規格はWAP Forumが採用した[マルチメディアメッセージングサービス](../Page/マルチメディアメッセージングサービス.md "wikilink") (MMS) である。

## WAPプッシュ

WAPプッシュはWAP 1.2から導入されたWAPにおけるプッシュ技術であり、サービスプロバイダーによる配信サービスが受けられるようにするものである。WAPプッシュのメッセージのタイプにより、SL (Service Loading)、SI (Service Indication) とCO (Cache Operation) の3つがある。規格策定時の想定用途としては、ネットワーク閑散時間帯にデイリーの配信などを行なったり、天気予報表示の更新などに使えるものであったが、通信費用に対する消費者側の懸念などもあって、広くは普及していない。

## プロトコル設計での教訓

WAPプロトコル設計の妥当性に対しては、その発足時から論争の元になっていた。すなわち、WAP 1.xのプロトコルは、より低速で遅延性の高い携帯電話ネットワークに最適化するという意図のもと、WTP（ワイヤレストランスポートプロトコル）、WSP（ワイヤレスセッションプロトコル）、WTLS（ワイヤレストランスポートレイヤーセキュリティ）などがIP層の上位にのせられることになった。これらのプロトコルは携帯電話の世界でしか使われず、また、TCP/IPの対応するプロトコルと比べるとかなり複雑なものであって、その効果と存在理由について主にインターネット側から多くの批判がなされてきた。

WAP 2.0でWAP自体がトランスポートプロトコルとしてTCPを併記する形で採用し、最終的にこの論争には終止符が打たれた。WAP 2.0でのTCP採用時には、有線と無線を[プロキシ](../Page/プロキシ.md "wikilink")サーバで分けるという考えの元、Wireless Profiled TCPという概念もあわせて採用された。 　 品質の異なるネットワーク間（例：無線と有線）を中継する場合に再送セグメントの分割を行い効率化を図ることもある（具体例：w-TCP/WAP2.0 [1](http://www.atmarkit.co.jp/fmobile/rensai/wap02/wap02.html)、split-TCP \[RFC 2757\]）。

## 関連項目

  - [モバイルブラウザ](../Page/モバイルブラウザ.md "wikilink")
  - [iモード](https://ja.wikipedia.org/wiki/iモード "wikilink") - NTTドコモが開発した、WAP、MMSの対抗規格

## 脚注

[Category:GSM](https://ja.wikipedia.org/wiki/Category:GSM "wikilink") [Category:携帯電話](https://ja.wikipedia.org/wiki/Category:携帯電話 "wikilink")

1.  [馬券が購入できるケータイ](http://www.watch.impress.co.jp/mobile/news/1999/11/15/jrapat.htm) - Mobile Central・1999年11月15日