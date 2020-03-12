> この記事は[APRS](https://ja.wikipedia.org/wiki/APRS)から翻訳されています。


**APRS**（）とは、[アマチュア無線](https://ja.wikipedia.org/wiki/アマチュア無線 "wikilink")を用いた位置情報発信システムである\[1\]。

## システム

APRSは、[アマチュア無線](https://ja.wikipedia.org/wiki/アマチュア無線 "wikilink")上での[無線パケット通信](../Page/無線パケット通信.md "wikilink")を応用して[リアルタイム](../Page/リアルタイム.md "wikilink")で生データを配信する通信[プロトコル](../Page/プロトコル.md "wikilink")である\[2\]。アメリカ合衆国のアマチュア無線家ボブ・ブラニンガ（Bob Bruninga、WB4APR）が1992年に提唱・発表した。

APRSは[GPSなどを利用して行われる移動アマチュア無線局の位置](../Page/グローバル・ポジショニング・システム.md "wikilink")[トラッキング](https://ja.wikipedia.org/wiki/トラッキング "wikilink")機能が有名である。GPS信号を一定の時間間隔で送信するとサーバーにデータが蓄積され、[コールサイン](https://ja.wikipedia.org/wiki/コールサイン "wikilink")や日付を入力することで位置情報が赤い点の連続で地図上に表示される（GPS信号の送信が途切れたときは青い線で表示される）\[3\]。

従来の[アマチュアパケット無線に比べ](../Page/パケット通信_\(アマチュア無線\).md "wikilink")、[パケット通信](../Page/パケット通信.md "wikilink")を拡散して使用するため、[ブロードキャスト型](https://ja.wikipedia.org/wiki/ブロードキャスト型 "wikilink")に近い構造となっている。APRSは全世界で運用されており、[インターネット](../Page/インターネット.md "wikilink")[ゲート](../Page/ゲート.md "wikilink")などの[無線通信](../Page/無線通信.md "wikilink")以外の[メディアとも親和性が高く](../Page/メディア_\(媒体\).md "wikilink")、広く利用されている。また、[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")の高い設計となっており、[表示機構を持たず発信のみという小型のものから](../Page/ディスプレイ_\(コンピュータ\).md "wikilink")[アマチュアパケット無線\#ターミナルノードコントローラ](https://ja.wikipedia.org/wiki/アマチュアパケット無線#ターミナルノードコントローラ "wikilink") (TNC) 内蔵で表示機構を持つ[無線機](https://ja.wikipedia.org/wiki/無線機 "wikilink")、そして[PCを接続してフルに運用できるものがある](../Page/パーソナルコンピュータ.md "wikilink")。

APRSを使用するには、専用ソフトウェアの[使用登録](http://www.suny.jp/Ham/APRS.html)をし、固有のナンバーを得なければならない場合がある。これはソフトにより仕様が異なり、APRSサーバに接続し、[ゲート経由](https://ja.wikipedia.org/wiki/ゲート経由 "wikilink")でAPRSに接続する場合のみに必要になる場合や、ナンバーがない起動では、メッセージ(チャット)の送信やI-Gateなど機能制限がつくものがある。

ナンバーには2種類あり、使用に必要なシリアルナンバーの他、APRSサーバに接続する際、無免許者がゲートを通じ、ゲートを通じて発信されないようにするためのナンバーもある。ソフトによっては後者の番号について生成する機能を持ったものも存在する。（Xastirなど）

## 各国での利用

### アメリカ合衆国

位置情報や[ショートメッセージ](https://ja.wikipedia.org/wiki/ショートメッセージサービス "wikilink")、[天気](../Page/天気.md "wikilink")情報などを送受信することができ、またほぼ[リアルタイム](../Page/リアルタイム.md "wikilink")で各局の動きを知ることができるという特性から[アメリカでは](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[パレード](../Page/パレード.md "wikilink")の位置情報や[災害](../Page/災害.md "wikilink")時のコミュニケーション、[捜索](../Page/捜索.md "wikilink")活動などに広く利用されている。

### 日本

[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")では[ケンウッド](../Page/ケンウッド.md "wikilink")社による[ナビトラ](https://ja.wikipedia.org/wiki/ナビトラ "wikilink")という規格も存在するが、これはAPRSとは[互換性](../Page/互換性.md "wikilink")を持たない。しかし、[JAPRSX](https://ja.wikipedia.org/wiki/JAPRSX "wikilink") (Japan APRS Experiment) や[J-net](http://www.suny.jp/Ham/APRS.html)などの[同好会](https://ja.wikipedia.org/wiki/同好会 "wikilink")の活動や、また[インターネット](../Page/インターネット.md "wikilink")経由の[ゲート](../Page/ゲート.md "wikilink")と呼ばれる[ノードにより日本国内においても限定的にAPRSを使用して世界のユーザーと通信することが可能となっている](https://ja.wikipedia.org/wiki/ノード_\(ネットワーク\) "wikilink")。

日本では[アマチュア局](https://ja.wikipedia.org/wiki/アマチュア局 "wikilink")の[無線局免許状](../Page/無線局免許状.md "wikilink")が必要となる。APRS[ソフトウェア](../Page/ソフトウェア.md "wikilink")として、広く利用されているUI-View32の日本での登録業務は、[JA6NKA 池上 いけのうえ](http://www.suny.jp/Ham/reg.html)氏が、認証番号を即日（15分～数時間）発行している。

UI-View32の開発者G4IDE Roger Baker氏の遺言に沿い、任意団体[APRSがん募金](http://www.suny.jp/Ham/GanNcyMapBokin.html)が設立され、[国立がんセンター](https://ja.wikipedia.org/wiki/国立がんセンター "wikilink")へ寄付されている。

また地図作製の必要がなく、設定が容易で[日本語](../Page/日本語.md "wikilink")でも操作できる [AGWTracker](http://www.agwtracker.com/)も利用者が増えている。

## 脚注

<references/>

## 外部リンク

  - [Japan APRS Experiment (JAPRSX)](http://japrsx.com)
  - [UI-View32 認証番号発行（J-net）](http://www.suny.jp/Ham/UI-View32-jareg.html)
  - [AGWTrackerなど番号発行（J-net）](http://www.suny.jp/Ham/AGWT-Password.html)
  - [KENWOOD社の解説集 「APRS と EchoLink を楽しもう」](http://www.kenwood.co.jp/products/amateur/mobile/tm_d710_d710s/tm-d710_s_enjoy_aprs_and_echolink.pdf)

[Category:アマチュア無線](https://ja.wikipedia.org/wiki/Category:アマチュア無線 "wikilink")

1.
2.  What is APRS? [1](ftp://ftp.tapr.org/aprssig/aprsspec/spec/aprs101/APRS101.pdf)
3.