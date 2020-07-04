> この記事は[Link Control Protocol](https://ja.wikipedia.org/wiki/Link_Control_Protocol)から翻訳されています。


**Link Control Protocol** (リンク・コントロール・プロトコル、**LCP**) は、[Point-to-Point Protocol](../Page/Point-to-Point_Protocol.md "wikilink") の一部を構成する[プロトコルである](../Page/通信プロトコル.md "wikilink")。

## 概要

PPP通信を開始するとき、送信側・受信側の両側の装置は、これから行う[データ転送](https://ja.wikipedia.org/wiki/データ転送 "wikilink")で必要となる特定の条件を決定するために、LCPパケットを送信する。

LCP [プロトコル](../Page/プロトコル.md "wikilink")は以下の動作を行う。

  - リンクした相手を識別し、[ピア](../Page/ピア.md "wikilink")デバイスを受け入れるか拒絶するかを決める
  - データ転送で許容されるパケットサイズを決定する
  - 構成におけるエラーを検出する
  - 要求条件が受け入れられないならば、リンクを切断する

LCPパケットによりリンクが許容されるまで、デバイスは PPP でデータをネットワークに送信することができない。しかし、LCP パケットは PPP パケットに埋め込まれるので、LCP が再設定を行う前に、基本的な PPP 接続は確立されていなければならない。 PPP パケット上の LCP は、コントロールコード 0xC021 であり、 INFO フィールドに LCP パケットを含んでいる。LCPパケットには 4 つのフィールドがある。(Code, Id, Length, Data)

  - Code: 要求するオペレーション: Configure Link, Terminate Link, ... および [肯定応答](https://ja.wikipedia.org/wiki/肯定応答 "wikilink")、否定コード
  - Data: オペーレーションのパラメータ

## 関連項目

  - [コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")

## 外部リンク

  - [RFC1570](http://tools.ietf.org/html/rfc1570.html): PPP LCP Extensions
  - [RFC1661](http://tools.ietf.org/html/rfc1661.html): The Point-to-Point Protocol (PPP)
  - [RFC1663](http://tools.ietf.org/html/rfc1663.html): PPP Reliable Transmission

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")