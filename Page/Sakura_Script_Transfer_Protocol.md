> この記事は[Sakura Script Transfer Protocol](https://ja.wikipedia.org/wiki/Sakura_Script_Transfer_Protocol)から翻訳されています。


**Sakura Script Transfer Protocol** (サクラ スクリプト トランスファー プロトコル、**SSTP**) とは、[伺か](../Page/伺か.md "wikilink")、およびその互換環境（以下 SSTP サーバ）の制御に使われる SAKURA [Script](../Page/スクリプト言語.md "wikilink") の転送[プロトコルである](../Page/通信プロトコル.md "wikilink")。 [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") ヘッダに似た構文を持つ。

SSTP を利用することにより、外部から SSTP サーバにイベントを発生させることができる。 SSTP が使用する[ポート番号](https://ja.wikipedia.org/wiki/ポート番号 "wikilink")9801、およびポート番号7743は [IANA](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") が定める予約済みポート番号にも登録されている。 SSTP 自体は単なる転送プロトコルに過ぎず、 SSTP サーバへ実際に与えられる命令は SAKURA Script による。これは HTTP と [HTML](../Page/HyperText_Markup_Language.md "wikilink") の関係に例えると分かりやすい。

ポートを使用する SSTP の他、 [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の COPYDATA メッセージを使用する Direct SSTP がある。 Direct SSTP は SSTP サーバと SSTP クライアントが単一の Windows 上で同時に動く場合に利用される。

SSTP を利用したコミュニケーションツールとして、 SSTP Bottle がある。 SSTP 送信サーバを容易に利用できるように、いもうとネットワークサービス - 毒電波 - ホームページからのメッセージがフリーで利用できる。

## SSTP 使用上の注意

SSTP の通信はサーバから利用者の PC へ接続要求が発生することがあるため、ファイヤーウォールソフトの設定によっては『不正侵入』等の警告メッセージが表示されることが多い。

そのため、 SSTP を不特定多数の利用者がアクセスする可能性のあるホームページ等に設置する場合には、予め『不正侵入』の警告メッセージが表示される旨、記載しておくことが望ましい。

## ポート番号

  - [TCP](../Page/Transmission_Control_Protocol.md "wikilink") 7743：[伺か](../Page/伺か.md "wikilink")（未使用）
  - [UDP](../Page/User_Datagram_Protocol.md "wikilink") 7743：伺か（未使用）
  - TCP 9801：伺か
  - UDP 9801：伺か（未使用）
  - TCP 9821：[SSP](https://ja.wikipedia.org/wiki/SSP_\(曖昧さ回避\) "wikilink")
  - TCP 11000：伺か（廃止）

## 関連項目

  - [伺か](../Page/伺か.md "wikilink")

## 外部リンク

  - [SSTP Bottle](http://bottle.mikage.to/)
  - [いもうとネットワークサービス - 毒電波 - ホームページからのメッセージ](http://imouto.net/)

[Category:インターネットのプロトコル](https://ja.wikipedia.org/wiki/Category:インターネットのプロトコル "wikilink") [Category:伺か](https://ja.wikipedia.org/wiki/Category:伺か "wikilink")