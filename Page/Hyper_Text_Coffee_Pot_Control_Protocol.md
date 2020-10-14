> この記事は[Hyper Text Coffee Pot Control Protocol](https://ja.wikipedia.org/wiki/Hyper_Text_Coffee_Pot_Control_Protocol)から翻訳されています。


[Htcpcp_teapot.jpg](https://ja.wikipedia.org/wiki/File:Htcpcp_teapot.jpg "fig:Htcpcp_teapot.jpg") [HTCPCP_Pot.jpg](https://ja.wikipedia.org/wiki/File:HTCPCP_Pot.jpg "fig:HTCPCP_Pot.jpg")にくっつけた形でのHTCPCP-TEAの実装\]\] **Hyper Text Coffee Pot Control Protocol**（ハイパー・テキスト・コーヒーポット・コントロール・プロトコル、**HTCPCP**、**ハイパーテキスト・コーヒーポット制御プロトコル**）とは[HTTPの拡張で](../Page/Hypertext_Transfer_Protocol.md "wikilink")[コーヒーポットの制御](../Page/コーヒーメーカー.md "wikilink")、監視、診断を行うための[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[4月1日](../Page/4月1日.md "wikilink")に発行された[RFCの](../Page/Request_for_Comments.md "wikilink")で規定されている\[1\]が、これは[エイプリルフール](https://ja.wikipedia.org/wiki/エイプリルフール "wikilink")恒例の[ジョークRFC](https://ja.wikipedia.org/wiki/ジョークRFC "wikilink")として公開されたものである\[2\]。

[2014年](../Page/2014年.md "wikilink")[4月1日](../Page/4月1日.md "wikilink")には、[紅茶](../Page/紅茶.md "wikilink")向けに拡張した**HTCPCP-TEA**(Hyper Text Coffee Pot Control Protocol for Tea Efflux Appliances)がとして公開された\[3\]が、これもエイプリルフールのジョークRFCである。

## 概要

RFC 2324 はが執筆したものである。彼はこれを風刺と表現し、「これは真面目な目的を持っている――それは[HTTPを不適切に拡張する方法を特定することである](../Page/Hypertext_Transfer_Protocol.md "wikilink")。」と書いている\[4\]。プロトコルの文言からして、これが完全に真面目な目的ではないことは明らかである。例えば、"there is a strong, dark, rich requirement for a protocol designed espressoly for the brewing of coffee"（コーヒーを淹れるために[エスプレッソ](../Page/エスプレッソ.md "wikilink")リーに設計したプロトコルには、強く、暗く、豊かな要求がある）と書かれている。

エイプリルフールに発行されたジョークRFCではあるが、プロトコルそのものは実行可能なものである、エディタの[Emacs](../Page/Emacs.md "wikilink")には、完全に機能するHTCPCPクライアントの実装（coffee.el）が存在する\[5\]。[Mozilla](../Page/Mozilla.md "wikilink")のバグレポートには、このプロトコルに対応していないことに対する不満を訴えるものが多数存在する\[6\]。また、大学生の研究対象として、実際にHTCPCPを実装した[コーヒーメーカー](../Page/コーヒーメーカー.md "wikilink")を試作するといったことも行われている\[7\]。

HTCPCPの発表から10年後の2008年4月1日、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink")(W3C)の"HTTP Vocabulary in [RDF](../Page/Resource_Description_Framework.md "wikilink")"\[8\]のパロディとして、Web-Controlled Coffee Consortium(WC3)が"HTCPCP Vocabulary in RDF"の初稿を発表した\[9\]。

HTTPをベースとしたプロトコルであるため、「コーヒーポット側からクライアントに『コーヒーが入った』等の通知を送ることができない」などの問題を抱えており（元々がジョークRFCであるため仕方のないことではあるが）、本プロトコルの代わりに[IRC](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")・[Twitter](../Page/Twitter.md "wikilink")による通知機能を持たせたコーヒーメーカー「萌香」が開発される\[10\]など、本プロトコルの代替となるものも提案されている。

## コマンドと応答

HTCPCPは[HTTPを拡張したものである](../Page/Hypertext_Transfer_Protocol.md "wikilink")。HTCPCPリクエストは、[URIスキーム](../Page/Uniform_Resource_Identifier.md "wikilink") `coffee` （または、29の言語における「コーヒー」を意味する単語。日本語の「コーヒー」も含まれている。）で識別され、HTTPメソッドを以下のように拡張している。

|                   |                                                                                                                                                                                                    |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `BREW` または `POST` | HTCPCPサーバに[コーヒー](https://ja.wikipedia.org/wiki/コーヒー "wikilink")を淹れさせる。この目的で`POST`を使用することは推奨されていない。新しいHTTPリクエストヘッダフィールド"Accept-Additions"が提案されており、クリーム、全乳、バニラ、ラズベリー、ウィスキー、アクアビットなどのオプションの追加に対応している。 |
| `GET`             | HTCPCPサーバからコーヒーを「取得」する。                                                                                                                                                                            |
| `PROPFIND`        | コーヒーに関する[メタデータ](../Page/メタデータ.md "wikilink")を返す。                                                                                                                                                   |
| `WHEN`            | "When"と言うと、HTCPCPサーバがコーヒーにミルクを注ぐのを止める（該当する場合）。                                                                                                                                                     |

以下の2つの[エラー応答が定義されている](https://ja.wikipedia.org/wiki/HTTPステータスコード#4xx_Client_Error_クライアントエラー "wikilink")。

|                      |                                                                                                                                       |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `406 Not Acceptable` | HTCPCPサーバは何らかの理由でAccept-Addition要求を提供できない。応答では、利用可能なオプション機能の一覧を示す必要がある。RFCには次のように書かれている。「実際には、ほとんどの自動化コーヒーポットは、現在のところ追加を提供することはできない。」 |
| `418 I'm a teapot`   | HTCPCPサーバはである。結果として得られるエンティティ本体は「背が低くてがっしりしている」かもしれない（これは『』という子供向けの歌の歌詞の引用である）。この動作のデモンストレーションが存在する\[11\]\[12\]。                      |

## Save 418 movement

2017年8月5日、[IETF](https://ja.wikipedia.org/wiki/IETF "wikilink") HTTPBISワーキンググループの議長であるは、HTCPCPを参照して実装されたステータスコード418 "I'm a teapot "を[Node.js](https://ja.wikipedia.org/wiki/Node.js "wikilink")プラットフォームから削除するよう求めた\[13\]。2017年8月6日、ノッティンガムは、プログラミング言語[Goからの](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")418 "I'm a teapot "への参照の削除を要求し\[14\]、その後[Python](../Page/Python.md "wikilink")のHTTPライブラリ"Requests"\[15\]や[ASP.NET](../Page/ASP.NET.md "wikilink")のHttpAbstractionsライブラリ\[16\]からも削除するよう要求した。

これを受けて、15歳の開発者のシェーン・ブランズウィック(Shane Brunswick)はウェブサイト save418.com を作成し\[17\]、"Save 418 Movement"（418を守れ運動）を立ち上げた。彼は、様々なプロジェクトで 418 "I'm a teapot"が参照されることは、「コンピュータの基礎となるプロセスがまだ人間によって作られていることを思い起こさせる」ことになると主張した。ブランズウィックのサイトは、ソーシャル・プラットフォーム[Reddit](../Page/Reddit.md "wikilink")で数千のアップボイスを集め\[18\]、彼のサイトで紹介されたTwitterの[ハッシュタグ](https://ja.wikipedia.org/wiki/ハッシュタグ "wikilink") "\#save418"を多くの人が使用した。世間の反発を受けて、Node.js、Go、PythonのRequestsライブラリ、ASP.NETのHttpAbstractionsライブラリは、自らのプロジェクトにおいて418 "I'm a teapot" を削除しないことを決定した。

これらのプロジェクトと一般の人々からの満場一致の支持を受けて、ノッティンガムは、418が当面の間、公式のステータスコードに置き換えられないことを保証するために、418 を予約済みのHTTPステータスコードとしてマークするプロセスを開始した\[19\]。

## 脚注

### 注釈

### 出典

## 関連項目

  -
  - [モノのインターネット](https://ja.wikipedia.org/wiki/モノのインターネット "wikilink") (Internet of things)

  - [ジョークRFC](https://ja.wikipedia.org/wiki/Request_for_Comments#一風変わったRFC "wikilink")

  - [ISO 3103](../Page/ISO_3103.md "wikilink") - 紅茶の入れ方の国際標準規格

## 外部リンク

  - ([和訳](http://www.chibutsu.org/iorin/rfc/rfc2324.txt))

  -
  - [Error 418 (I’m a teapot)\!?](https://www.google.com/teapot) - [Google](../Page/Google.md "wikilink")による418エラーのページ。このRFCで定義されているコード418が実際に返されている。

  - [Package teapot HTCPCP-TEA implementation](https://godoc.org/github.com/davsk/teapot) by David Skinner

  - [error418.net](http://www.error418.net/)

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:エイプリルフール](https://ja.wikipedia.org/wiki/Category:エイプリルフール "wikilink") [Category:コーヒー器具](https://ja.wikipedia.org/wiki/Category:コーヒー器具 "wikilink") [Category:茶](https://ja.wikipedia.org/wiki/Category:茶 "wikilink") [Category:Hypertext_Transfer_Protocol](https://ja.wikipedia.org/wiki/Category:Hypertext_Transfer_Protocol "wikilink") [Category:コンピュータ・ユーモア](https://ja.wikipedia.org/wiki/Category:コンピュータ・ユーモア "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.