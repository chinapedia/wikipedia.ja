> この記事は[Challenge-Handshake Authentication Protocol](https://ja.wikipedia.org/wiki/Challenge-Handshake_Authentication_Protocol)から翻訳されています。


[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")において、**Challenge-Handshake Authentication Protocol** (チャレンジ・ハンドシェイク・オーセンティケーション・プロトコル、**CHAP**) は、ユーザやネットワークホストに対する[認証](../Page/認証.md "wikilink")プロトコルである。例えば、この認証は[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")によって行われる。

[RFC](../Page/Request_for_Comments.md "wikilink") 1994: PPP Challenge Handshake Authentication Protocol (CHAP) がこのプロトコルを定義している。

CHAP は [Point-to-Point Protocol (PPP)](../Page/Point-to-Point_Protocol.md "wikilink") が、リモートクライアントの正当性を確認するための認証方法として使用される。CHAP は[3ウェイ・ハンドシェイク](../Page/3ウェイ・ハンドシェイク.md "wikilink")によって、定期的に[クライアントの正当性を確認する](../Page/クライアント_\(コンピュータ\).md "wikilink")。これは、最初の[データ通信](../Page/データ通信.md "wikilink")リンクを確立するときに行われ、その後はいつでも行われる可能性がある。この確認は、 (例えばクライアントユーザのパスワード) に基づいている。

1.  データリンク確立フェーズの後、認証者は "チャレンジ" メッセージを被認証者に送る。
2.  被認証者は、[MD5](../Page/MD5.md "wikilink") [チェックサム](../Page/チェックサム.md "wikilink")の[ハッシュ関数](../Page/ハッシュ関数.md "wikilink")のような、[一方向性関数](../Page/一方向性関数.md "wikilink")を使って計算した値のレスポンス返送する。
3.  認証者は、期待すべきハッシュ値の計算を自分で行い、レスポンス内容を確認する。もし、値が一致するならば、認証者は被認証者を正当な相手として承認する。
4.  ランダムな間隔で、認証者は新しい "チャレンジ" を送り、ステップ 1 から 3 を繰り返す。

CHAP は、増加していく識別子と、可変の "チャレンジ" 値を用いることにより、相手からの[反射攻撃](https://ja.wikipedia.org/wiki/反射攻撃 "wikilink")に対する防御を提供する。 CHAP は、クライアントとサーバが秘密鍵の平文を知っていることを必要とするが、これがネットワークに対して送られることはない。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は、 と呼ばれる CHAP のバリエーションを実装した。これは相手が秘密鍵の平文を知ることさえ要求しない。

## 動作

  - チャレンジ (Challenge) パケット (システムからユーザ)
  - 応答 (Response) パケット (ユーザからシステム)
  - 成功 (Success) ／失敗 (Failure) パケット (システムからユーザ)

## CHAP パケット

| 説明        | 1 バイト    | 1 バイト | 2 バイト | 1 バイト       | 可変長        | 可変長 |
| --------- | -------- | ----- | ----- | ----------- | ---------- | --- |
| Challenge | Code = 1 | ID    | 長さ    | "チャレンジ" の長さ | "チャレンジ" の値 | 名前  |
| Response  | Code = 2 | ID    | 長さ    | 応答の長さ       | 応答の値       | 名前  |
| Success   | Code = 3 | ID    | 長さ    |             | メッセージ      |     |
| Failure   | Code = 4 | ID    | 長さ    |             | メッセージ      |     |

CHAP パケットは PPPフレームに埋め込まれる。プロトコルフィールドの値は C223(16進数) である。

| フラグ | アドレス | コントロール | プロトコル (C223(16進数)) | Payload (上記の表) | FCS | フラグ |
| --- | ---- | ------ | ------------------ | -------------- | --- | --- |

## 関連項目

  - [Point-to-Point Protocol](../Page/Point-to-Point_Protocol.md "wikilink")

  - [Password Authentication Protocol](https://ja.wikipedia.org/wiki/Password_Authentication_Protocol "wikilink")

  -
  - [暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数 "wikilink")

## 外部リンク

  - RFC 1994
  - [Divide and Conquer: Cracking MS-CHAPv2 with a 100% success rate](https://www.cloudcracker.com/blog/2012/07/29/cracking-ms-chap-v2/)
  - [カプセル化されていない MS-CHAP v2 認証により、情報漏えいが起こる](https://technet.microsoft.com/library/security/2743314)
  - [MS-CHAP v2 の認証情報漏えいの問題に関する注意喚起](https://www.jpcert.or.jp/at/2012/at120027.html)

[Category:認証プロトコル](https://ja.wikipedia.org/wiki/Category:認証プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")