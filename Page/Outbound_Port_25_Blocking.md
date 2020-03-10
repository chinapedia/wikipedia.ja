> この記事は[Outbound Port 25 Blocking](https://ja.wikipedia.org/wiki/Outbound_Port_25_Blocking)から翻訳されています。


**Outbound Port 25 Blocking**（アウトバウンドポート25ブロッキング、**OP25B**）は[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")（ISP）の悪意ある顧客が自前の[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")から[スパム](../Page/スパム_\(メール\).md "wikilink")（いわゆる迷惑メール）を送信したり、[SMTP拡大型の](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")[ウイルスに感染したPCからウイルスメールが送信されることなどを防止するために](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")、ISP側で許可した特定のサーバ以外のSMTP（通常使用される[TCP](../Page/Transmission_Control_Protocol.md "wikilink")[ポートの](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")25番）の送信をブロックするという対策方法である。

[ボットネット](https://ja.wikipedia.org/wiki/ボットネット "wikilink")を構成するコンピュータからのスパム送信や、PCから[携帯キャリア宛のスパムの送信を阻止する上で効果を挙げている](../Page/携帯電話.md "wikilink")。一方で予告無く実施されることでISP利用者が設定を変更しなければならない、あるいは利用していた外部のメールサーバがサブミッションポート（[後述](https://ja.wikipedia.org/wiki/#メッセージサブミッションエージェント "wikilink")）に対応しておらず送信できなくなるといった課題もある。

具体的には、ISP・A社に接続してA社以外の他のISPや、学校や勤務先、[ホスティング業者などのメールサーバに](../Page/ホスティングサーバ.md "wikilink")[アカウント](../Page/アカウント.md "wikilink")（[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")）を持っていたとしても、これらのメールサーバからメール送信ができなくなる。逆に、別のISP（ホテルなどでの接続サービス、海外[ローミング](../Page/ローミング.md "wikilink")による接続など）からA社のメールサーバによるメール送信もできなくなる。契約や接続形態によってはA社へ接続した状態でもA社のメールサーバからメールを送信できなくなる場合がある。

## メッセージサブミッションエージェント

2007年現在、OP25Bを実施しているインターネットサービスプロバイダーでは「外部サーバへのメール送信は禁止、もしくはサブミッションポートと呼ばれる**ポート番号587**を利用する」との対応方法が説明されている場合がある。この節では、サブミッションポートに関連しているメッセージサブミッションエージェントについて説明する。

SMTPと呼ばれるプロトコルではメッセージの伝達のみを意図した定義となっており、[MTA](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")（Message Transfer Agent）は、経由情報等の一部のメールヘッダを**追加**すること以外は想定されていないが、インターネットが活用され利便性を求められるようになってからは、MTAが伝達以外の処理を付与されている状態で利用されている。

そこでメールを送り出す[MUA](../Page/電子メールクライアント.md "wikilink")（Message User Agent、メールソフト）と、MTA間のメールの伝達を行うMTA（Message Transfer Agent）の他に、新しくMSA（Message Submission Agent）と呼ばれるMUAからのメール受付窓口（ポート番号587が予約されている）を新しく作ることがRFC2476にて提起された。

つまりMUA（メールソフト）から発信されたメールは、587番ポートを使ってMSAに送られる。MSAはメールを補完したり加工する権限を持ち、配送するかMTAにリレーする。MTAは経由情報等の一部の追加のみ行う権限を持ち、配送するか別のMTAにリレーする。といった処理区分となる。通常、送信時の認証方式の一つである[SMTP-AUTH](https://ja.wikipedia.org/wiki/SMTP-AUTH "wikilink")も併用されている。

要はユーザサイドから見た場合、OP25Bを導入しているISPに接続している場合、外部（アカウントを持つ他のISPやホスティング先、学校、勤務先など）の送信サーバがポート番号587番のアクセスを提供しており、かつMUAの設定を外部利用サーバの提供者が指定するものに変更しないと、メールを送信できないことになる。

また、経由情報等の一部のメールヘッダを追加することのみ行える正常なMTAであること、サーバ自身がMTAであるかMSAであるかを識別できる情報を付与させることを条件にMUAからMTAへ、つまりポート25での通信が認められている。

## 業界での見解

JEAG([Japan Email Anti-Abuse Group](https://ja.wikipedia.org/wiki/Japan_Email_Anti-Abuse_Group "wikilink"))では、OP25Bワーキンググループにて「Source IP Addressが動的IP、かつ、Destination Portが25であるTCPトラフィックを遮断すること」を推奨するRecommendationを取りまとめた。\[1\]

[総務省](../Page/総務省.md "wikilink")は[特定電子メールの送信の適正化等に関する法律](https://ja.wikipedia.org/wiki/特定電子メールの送信の適正化等に関する法律 "wikilink")に基づきスパム防止技術を取りまとめ、その中でOP25Bについて法律上「正当業務行為（違法性阻却事由あり）と解釈できる」との見解を示した。\[2\]

## 参考文献

<references/>

## 関連項目

  - [スパム (メール)](../Page/スパム_\(メール\).md "wikilink")
  - [Inbound Port 25 Blocking](https://ja.wikipedia.org/wiki/Inbound_Port_25_Blocking "wikilink")
  - [Simple Mail Transfer Protocol](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")

## 外部リンク

  -
  - [Inbound / Outbound Port 25 Blocking (IP25B / OP25B) 実施 ISP 一覧](http://seclan.dll.jp/ccblk25.htm)

[Category:電子メール](https://ja.wikipedia.org/wiki/Category:電子メール "wikilink") [Category:コンピュータ・ネットワーク・セキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータ・ネットワーク・セキュリティ "wikilink")

1.  、[過去の資料](https://salt.iajapan.org/wpmu/anti_spam/wp-content/themes/iajapan/docs/op25b.pdf)
2.  [総務省 - 特定電子メール等による電子メールの送受信上の支障の防止に資する技術の研究開発及び電子メールに係る役務を提供する電気通信事業者によるその導入の状況](http://www.soumu.go.jp/menu_news/s-news/090220_3.html)