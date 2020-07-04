> この記事は[Password Authentication Protocol](https://ja.wikipedia.org/wiki/Password_Authentication_Protocol)から翻訳されています。


**Password Authentication Protocol** (パスワード・オーセンティケーション・プロトコル、**PAP**) は、[ネットワークアクセスサーバ](https://ja.wikipedia.org/wiki/ネットワークアクセスサーバ "wikilink")がユーザを[PPPで認証する時に用いる](../Page/Point-to-Point_Protocol.md "wikilink")、単純な認証プロトコルである。 例えば[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")がこれを利用している。

この認証は、資源にアクセスする前にユーザの正当性を確認するプロセスである。 PAP は暗号化されていない [ASCII](../Page/ASCII.md "wikilink") コードのパスワードをネットワーク上で送信するため、[CHAPや](../Page/Challenge-Handshake_Authentication_Protocol.md "wikilink")[EAPに比較した場合](../Page/Extensible_Authentication_Protocol.md "wikilink")、安全性に欠ける場合がある。

## 動作

  - クライアントはユーザ名とパスワードを送信する
  - サーバは Authentication-ack (認証に成功した場合) または Authentication-nak (それ以外) を送信する

## PAP パケット

| 説明                     | 1 バイト    | 1 バイト | 2 バイト | 1 バイト    | 可変長  | 1 バイト    | 可変長   |
| ---------------------- | -------- | ----- | ----- | -------- | ---- | -------- | ----- |
| Authentication-request | Code = 1 | ID    | 長さ    | ユーザ名の長さ  | ユーザ名 | パスワードの長さ | パスワード |
| Authentication-ack     | Code = 2 | ID    | 長さ    | メッセージの長さ | ユーザ名 |          |       |
| Authentication-nak     | Code = 3 | ID    | 長さ    | メッセージの長さ | ユーザ名 |          |       |

PAPパケットは、PPPフレームに埋め込まれる。プロトコルフィールドの値は C023 (16進数) である。

| フラグ | アドレス | コントロール | プロトコル (C023 (16進数)) | ペイロード(上記の表) | FCS | フラグ |
| --- | ---- | ------ | ------------------- | ----------- | --- | --- |

## 参考文献

  -
## 関連項目

  - CHAP - [Challenge-Handshake Authentication Protocol](../Page/Challenge-Handshake_Authentication_Protocol.md "wikilink")
  - EAP - [Extensible Authentication Protocol](../Page/Extensible_Authentication_Protocol.md "wikilink")

## 外部リンク

  - RFC 1334: PPP Authentication Protocols

[Category:認証プロトコル](https://ja.wikipedia.org/wiki/Category:認証プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")