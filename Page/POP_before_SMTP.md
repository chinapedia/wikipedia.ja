> この記事は[POP before SMTP](https://ja.wikipedia.org/wiki/POP_before_SMTP)から翻訳されています。


**POP before SMTP**（POP ビフォー SMTP、ポップビフォーエスエムティーピー）とは、[SMTPに利用者](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")[認証](../Page/認証.md "wikilink")を付加するための機構。利用者が[電子メール](../Page/電子メール.md "wikilink")をSMTPで送信する前 (before) に、[POP](../Page/Post_Office_Protocol.md "wikilink") (POP3) の認証を通過させておくことによって送信を許可することから、この名称があった。

この方法は SMTP の認証機構が普及する前\[1\]、RFC 2476\[2\] - Message Submission の 3.3章 "Authorized Submission" においてクライアント制限方法の一つとして記述されていたもので、その詳細を規定したRFC文書は存在しない。SMTP のみで認証を完結させた[SMTP-AUTHの普及に伴い](https://ja.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol#SMTP-AUTH "wikilink")、現在は使われなくなってきている。

## 背景

[インターネット](../Page/インターネット.md "wikilink")の利用者が電子メールを送信する場合、[ISPなどがその網内に用意したメール送信](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")（中継）用[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")へ[SMTPを用いて電子メールを提出し](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")、送信（中継）を要求する形式が一般的である。しかし、SMTPはもともと配送経路上のメールサーバがバケツリレー式にメールを転送することを想定していたため、利用者認証の機構を持たなかった。したがって、そのままではISP利用者だけでなく、インターネット上のあらゆる利用者に、送信用[メールサーバ](https://ja.wikipedia.org/wiki/メールサーバ "wikilink")を使用されてしまう状態になってしまう。インターネットの利用が学術・研究目的に限られ利用者の善意を期待できた時代には、このようなメールサーバの運用も一般的であったが、利用者の増大に伴い、これらの利用者制限が全くないメールサーバが[スパムの中継のために悪用されるケースが頻発し](../Page/スパム_\(メール\).md "wikilink")、メールサーバの運用者は何らかの利用者制限を施す必要に迫られた。

最も単純な利用者制限は、そのメールサーバを運用するISPが保持している[IPアドレス](../Page/IPアドレス.md "wikilink")以外からのメール中継要求を常に拒否するようにサーバを設定することであった。こうすることで、そのISPに現在接続している利用者以外からの中継要求を防ぐことができる。しかし、[モバイル](https://ja.wikipedia.org/wiki/モバイル "wikilink")環境が普及し複数の異なるISPからインターネットに接続することが一般的になり、接続するISPが変わるたびに電子メールソフトの設定を変更（メールの送信に使用するサーバを、現在接続しているISPが運用するものに変更）する必要が生じ、利便性が低下した。また一方、[ブロードバンド接続の普及により](https://ja.wikipedia.org/wiki/ブロードバンドインターネット接続 "wikilink")、従来[ダイヤルアップ接続](../Page/ダイヤルアップ接続.md "wikilink")で利用していたISPを[メールアドレス](../Page/メールアドレス.md "wikilink")維持のためだけに残し、アクセス回線は別のブロードバンド対応ISPに乗り換えるということもしばしばあり、その場合旧ISPのメールサーバが上記のような運用をされているとメールを送信することができなくなってしまう。このように、固定されたIPアドレスによる送信者制限はいろいろと問題があった。これらの対策として生まれたのがPOP before SMTPであった。

## 概要

利用者がメールを受信する場合は、POP3等を用いてISPの受信用メールサーバから（利用者の端末へ）メールを転送する（取り出す）、という形式が一般的である。POP3等のメール取得用プロトコルは、利用者の認証（利用者名とパスワードによる）が必須となっているため、一旦その認証を通過した利用者端末のIPアドレスを、当面の間は正規利用者であると推定することができる。

この事を利用して、POP before SMTPでは、中継用（送信用）メールサーバは、自ISP内部からの中継要求を受理する一方、外部ISPからの接続に関しては、既にPOP3による認証を通過している端末のIPアドレスからのメール中継要求のみを「一時的に」（通常は数分程度）受け付けるようにする。このようにすることで、全く関係がない（POP3の認証を通過できない）利用者からのメール中継要求を拒否しつつ、正規利用者からのメール中継については受け付けることができる。

DRAC (Dynamic Relay Authorization Control)と呼ばれる[RPCを利用した機構をPOP](https://ja.wikipedia.org/wiki/Remote_Procedure_Call "wikilink")3、SMTPサーバー双方にパッチ等をあてることにより実装し、機能を実現することが多かった。

## 議論

POP before SMTPの利点として、SMTPとPOP3という既存の方式により実現しているため、一般的な利用者が環境を変更する必要がない、ということがあった。しかし、利用者がメールを送信する前に、POP3による「受信」動作を利用者が行わなければならない、という操作手順の制約も発生し、このことを知らない利用者からは「メールが受信できるが送信できない」という質問・苦情もしばしば見られた。これらは、[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")がSMTPの前にPOP を行うという実装を行ったことで次第に解消していった。また、ISPにとっては、本来は全く独立に運用していた送信用（SMTP）メールサーバと、受信用（POP3）メールサーバの間の連携が必要となり、運用がやや煩雑になる、という問題点もあった。

POP before SMTP の前提となっている仮定が必ずしも成り立たないケースも存在した。すなわち、POP3認証を通過した正規利用者と同じ[IPアドレス](../Page/IPアドレス.md "wikilink")で接続してきた利用者が、正規とは限らないケースである。一例として、多数の利用者を[NAT環境下に収容しているISPから接続した場合が相当する](https://ja.wikipedia.org/wiki/IPマスカレード "wikilink")(NAT環境下では、多数の利用者が単一もしくは少数のグローバルアドレスを共有するため)。また、個人向けインターネット接続サービスでは、同じISP内部の利用者間で[IPアドレス](../Page/IPアドレス.md "wikilink")を使いまわしている場合がほとんどである。しかし、POP before SMTP は厳密な利用者認証が目的ではなく、ISP外部からの中継(送信)用メールサーバの意図的な不正利用を十分に困難にすることができればよいとされ（実際、同じNAT環境下の他の利用者が、どのISPのメールサーバに対してPOP認証を最近完了したかを知ることや、POP認証を実行した利用者のIPアドレスと同じアドレスを限られた時間内で取得することは、一般利用者の立場では困難であった）、ネットワーク資源が現在ほど潤沢でなかった2000年代には、POP before SMTP は多くの [ISP](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink") で採用されていた。

POP before SMTPは、上記のようなやや不完全な面もあるため、あくまでも本来の利用者認証の目的で設計された[SMTP-AUTH等が普及するまでの](https://ja.wikipedia.org/wiki/SMTP#SMTP-AUTH "wikilink")「つなぎ」とするべきという考え方もあった。RFC 2476においてもSMTP-AUTHの利用を先ず挙げている。

## 現在

上記議論にある中で、[IPアドレスの枯渇やセキュリティの面などから](../Page/IPアドレス枯渇問題.md "wikilink")、NAT環境はさらに普及していき、企業などではひとつのIPアドレスを複数のクライアントを使いまわすことが一般的になってきた。現在では個人のブロードバンド接続においてもNATが一般的であり、IPアドレスによる許可自体が難しくなってきた。また、[ボットや](../Page/ボットネット.md "wikilink")[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")等に感染したクライアントなど悪意を持った送信者にも対応することが難しく、メールサーバーの管理者は根本的な対策を求められることになった。

より本質的な解決策として、SMTP自体を拡張して利用者認証を行うSMTP-AUTHが広く提供されるようになり、多くの電子メールクライアントにも実装されるようになったことから、ISPでも廃止されることが多くなり\[3\]\[4\]\[5\]、現在では提供されることが少なくなってきている。

## 脚注

## 関連項目

  - [Outbound Port 25 Blocking](../Page/Outbound_Port_25_Blocking.md "wikilink")
  - [Simple Mail Transfer Protocol](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")（SMTP）
  - [スパム (メール)](../Page/スパム_\(メール\).md "wikilink")（いわゆる迷惑メール）

[Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink") [Category:認証プロトコル](https://ja.wikipedia.org/wiki/Category:認証プロトコル "wikilink")

1.  SMTP-AUTHの提案文書は RFC 2554であり、RFC 2476と同時の1998年12月の発行。
2.  現在の最新文書はRFC 6409。
3.  [「POP Before SMTP」廃止のお知らせ](http://www2.7-dj.com/support/info/popbefore.html)- [7-dj.com](../Page/7-dj.com.md "wikilink")
4.  [メール送信時のユーザー認証　「POP before SMTP」の終了のお知らせ](http://www.tiki.ne.jp/announce/160303.html)- [TikiTikiインターネット](https://ja.wikipedia.org/wiki/TikiTikiインターネット "wikilink")
5.  [「POP Before SMTP」とは何ですか。なぜ廃止するのですか。](https://support.ntt.com/mw-business/faq/detail/pid2300000h3o) - [NTT Communications](../Page/NTTコミュニケーションズ.md "wikilink")