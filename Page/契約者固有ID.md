> この記事は[契約者固有ID](https://ja.wikipedia.org/wiki/契約者固有ID)から翻訳されています。


**契約者固有ID**（けいやくしゃこゆうアイディー）とは、[携帯電話](../Page/携帯電話.md "wikilink")などで[ウェブサイト](../Page/ウェブサイト.md "wikilink")を閲覧したときにサーバに送信される識別子であり、狭義には携帯電話の契約者ごとに固有のID（機種変更を行っても契約者が同一である限りは変更されないID）を指し、広義には端末ごとに固有のID（機種を変更すると変更されるID）を含む。[キャリアによってその呼び方は異なる](../Page/電気通信事業者.md "wikilink")。

これらのIDは各事業者が独自に付与するもので、[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")/[W-CDMA](../Page/W-CDMA.md "wikilink")方式の携帯電話全般で加入者識別に使用される[International Mobile Subscriber Identity](https://ja.wikipedia.org/wiki/International_Mobile_Subscriber_Identity "wikilink")（IMSI）や、同じく端末識別に使用される[International Mobile Equipment Identity](https://ja.wikipedia.org/wiki/International_Mobile_Equipment_Identity "wikilink")（IMEI）との関係はない。またIDの形式や文字数・使用される文字種別などは事業者によって異なっている。

## 用途

日本では、[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")において「かんたんログイン」機能を実装するためにしばしば用いられている。ログイン中に「かんたんログイン」機能を有効にする設定をすると、ウェブアプリケーションがそのユーザの契約者固有IDをユーザIDとひも付けて記憶し、それ以降は、その契約者固有IDの端末でアクセスされたならば、ログインの際にユーザIDの入力を省略することができる。ウェブサイトによっては、パスワードの入力まで省略するところもある。

また、[行動ターゲティング](https://ja.wikipedia.org/wiki/行動ターゲティング "wikilink")広告において、人々のアクセス履歴を収集するための一意なIDとしても使われる。これについては、ユーザの[プライバシー](../Page/プライバシー.md "wikilink")保護との関係で問題も指摘されている（詳細は[行動ターゲティング\#プライバシーの問題](https://ja.wikipedia.org/wiki/行動ターゲティング#プライバシーの問題 "wikilink")を参照）。

## 各キャリアにおける取り扱い

携帯電話（クライアント）のキャリアによって定義、機能およびサーバでの取得方法は異なる\[1\]。

### NTTドコモ

  - 呼称：「端末製造番号」「個体識別情報」「ユーザID」「iモードID」

[iモード](https://ja.wikipedia.org/wiki/iモード "wikilink")では、契約者固有IDが3種類存在する。ユーザIDとiモードIDは[SSL環境下では取得できない](https://ja.wikipedia.org/wiki/Secure_Sockets_Layer "wikilink")。

  - iモードの公式サイトでは、URLの引数に「uid=NULLGWDOCOMO」の文字列を付加しておく（POSTメソッドの場合は、フォームのhidden属性として持たせておく）と、そのURLにアクセスされたとき、ドコモのiモードゲートウェイが「NULLGWDOCOMO」の部分を契約者ID(「ユーザID」)に置換する\[2\]。これは契約者が機種変更を行った場合でも変更されない。
  - [HTMLのいくつかの要素に](../Page/HyperText_Markup_Language.md "wikilink")「utn」属性を付加しておくと、そこにアクセスすると、画面上に端末製造番号を送信するかどうかの確認を求めるダイアログが表示され、ユーザが送信することを選択した場合には、HTTPリクエストの[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")ヘッダに端末製造番号が付加される\[3\]。この番号は端末に固有なものであるので、契約者が機種変更を行うと変更される。
  - 2008年4月より、URLの引数に「guid=ON」という文字列を付加しておく（「uid=NULLGWDOCOMO」とは異なり、POSTメソッドの時もFORMタグのACTIONの中に記述する）と、そのURLにアクセスされたとき、HTTPリクエストの「X-DCMGUID」ヘッダに、英数字7桁の契約者ID(iモードID、ユーザIDとは別の番号)が付加される\[4\]。このIDは契約者の機種変更では変更されないが、名義変更・改番・iモード契約の解約によって変更される\[5\]。

### au

  - 呼称：「サブスクライバID」「EZ番号」

[EZweb](../Page/EZweb.md "wikilink")では、ユーザが送信を止める設定をしていない限り、すべてのウェブサイトへのアクセスにおいて、HTTPリクエストの「X-UP-SUBNO」ヘッダに契約者IDが付加される\[6\]。この契約者IDはSSL環境下でも取得できる。

### ソフトバンクモバイル

  - 呼称：「端末シリアル番号」

[Yahoo\!ケータイ](../Page/Yahoo!ケータイ.md "wikilink")では、ユーザが送信を止める設定をしていない限り、すべてのウェブサイトへのアクセスにおいて、HTTPリクエストの[ユーザーエージェント](../Page/ユーザーエージェント.md "wikilink")ヘッダに端末IDが付加され\[7\]、また、HTTPリクエストの「X-JPHONE-UID」ヘッダに契約者IDが付加される。

SSL環境では、ソフトバンクモバイルが提供するSSLゲートウェイ（secure.softbank.ne.jp）を通して通信する場合に限り端末ID・契約者IDを取得可能である。「https://〜」で始まるURLを直接指定してアクセスした場合など、同ゲートウェイを通さずに通信を行う場合はIDを取得できない。

なおソフトバンクモバイルでは、[2011年](../Page/2011年.md "wikilink")6月末でSSLゲートウェイを原則廃止しており\[8\]、同年7月以降はSSL環境での端末ID・契約者IDの取得ができなくなった。

### イー・モバイル

  - 呼称：「ユーザID」

イー・モバイルでは、[EMnet](https://ja.wikipedia.org/wiki/EMnet "wikilink")で接続して、ウェブブラウザの設定で wm.internal.emnet.ne.jp:8080 をProxyサーバに指定すると、HTTPリクエストの「X-EM-UID」ヘッダに端末IDが付加される。この端末IDはSSL環境下では取得できない。\[9\]

### ウィルコム

  - 呼称：「個体識別情報（UID）」

ウィルコム公式サイト向けに個体識別情報を送出する仕組みがある\[10\]。

## プライバシー上の問題点

契約者固有IDはサイト側で簡単に取得できる。このため、個人情報とひも付けされた契約者固有IDがサイトから流出してしまうと、契約者固有IDを手がかりに個人情報が特定できることとなり、悪意のある者により犯罪利用される可能性が指摘されている\[11\]\[12\]。

また現在のところ、契約者固有IDはサーバによらず端末（契約者）が同じであれば同じIDが使用されるため、Web上の複数のサービスの利用状況をマッチングさせることでも個人情報を収集できる可能性がある。

しかも、契約者の都合で契約者固有IDを任意に変更する機能は、現在のところ提供されていない。従って、何らかの形で契約者固有IDが悪用された場合には、契約者は契約の解約・機種変更等で対抗することを迫られ、無駄な労力・出費を強いられることになる。

## セキュリティ上の問題点

契約者固有IDは、単にHTTPリクエストのヘッダに付与されるものなので、任意のHTTPリクエストの送信が可能なクライアントからは任意の契約者固有IDの送信が可能であり、ウェブマスターはHTTPリクエストヘッダを参照することでウェブサーバにリクエストを送ったユーザの契約者固有IDを取得することが可能である。この性質から、他人の契約者固有IDを入手した者は、容易にその契約者固有IDが送信可能である。携帯電話のHTTPクライアントは悪意のあるHTTPリクエストを送信できないという前提とすれば、アクセス元のIPアドレスがその[キャリアのものであることを確認することで](../Page/電気通信事業者.md "wikilink")、悪意のあるアクセスを回避する事ができる。

どのIPアドレスの範囲がどの携帯電話のキャリアのものであるか、その範囲は定常的に決まっておらず、各会社の管理とともに変化している。そのため、信頼できる最新の情報に基づいてIPアドレスのチェックを行わないと、「かんたんログイン」機能を提供する各ウェブサイトは、任意の契約者になりすました悪意のあるユーザからアクセスされてしまう危険がある。各キャリアは「IPアドレス帯域」として技術情報のウェブページに掲載しており、この情報は各キャリアが随時更新している。

しかし、一部のキャリア\[13\]の「IPアドレス帯域」情報が掲載されているウェブページはSSLを使わずに提供されており、その情報の発信元が信頼できる状態ではなく、また、掲載されている情報には 携帯電話以外からのアクセスがないことを保証しない、と掲載されている\[14\]ため、それらのウェブページの情報を元にIPアドレスを判断して「かんたんログイン」機能を提供する場合、なりすましアクセスを排除することができない。

## 脚注

## 外部リンク

  - [契約者固有IDとは](http://itpro.nikkeibp.co.jp/article/Keyword/20081007/316269/) - ITpro
  - [支払督促等を用いた請求、携帯電話の「個体識別番号」による脅し](http://www.kokusen.go.jp/news/data/n-20041105_3.html) - 国民生活センター

[Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:携帯電話](https://ja.wikipedia.org/wiki/Category:携帯電話 "wikilink")

1.  [携帯各キャリアの固有IDについて (全キャリア対応)](http://parame.mwj.jp/blog/0273) - ぱらめでぃうす
2.  [「UID」とは](http://itpro.nikkeibp.co.jp/word/page/10008450/) - ITpro
3.  [iモード対応HTMLタグ一覧 : utn属性](http://www.nttdocomo.co.jp/service/imode/make/content/browser/html/tag/utn.html)
4.  [重要なお知らせ : 『iモードID』の提供開始について | お知らせ | NTTドコモ](http://www.nttdocomo.co.jp/info/notice/page/080228_00.html) (2008.02.28)
5.  [iモードIDについて](http://www.nttdocomo.co.jp/service/imode/make/content/ip/index.html#imodeid)
6.  [ユーザエージェント](http://www.au.kddi.com/ezfactory/tec/spec/4_4.html) - EZfactory
7.  [WEB & NETWORK ユーザーエージェント](http://creation.mb.softbank.jp/web/web_ua_about.html) - MOBILE CREATION
8.  [Yahoo\!ケータイ仕様変更、従来の携帯サイトに接続できない場合も](http://k-tai.impress.co.jp/docs/news/20101015_400282.html) - ケータイWatch・2010年10月15日
9.  [ユーザエージェント](http://developer.emnet.ne.jp/useragent.html) - イー・モバイル 技術情報
10. [個体識別情報（UID）](http://www.willcom-inc.com/ja/service/contents_service/create/uid/index.html)
11. [携帯ＩＤ開放の危うさ・事件が起きる前に対策を](https://web.archive.org/web/20090309003921/http://it.nikkei.co.jp/internet/news/index.aspx?n=MMITbf000029092008) (楠正憲 日本経済新聞社IT+PLUS 2008.9.30 ウェブアーカイブ)
12. [日本のインターネットが終了する日](http://takagi-hiromitsu.jp/diary/20080710.html) - [高木浩光](../Page/高木浩光.md "wikilink")＠自宅の日記 2008.7.10
13. 2010年8月現在：DoCoMoとau
14. 2011年7月現在：ドコモとauとソフトバンクとイー・モバイルとウィルコムのIPアドレス帯域情報ページにその旨脚注が書いてある。
    ・[作ろうiモードコンテンツ：iモードセンタの各種情報 | サービス・機能 | NTTドコモ](http://www.nttdocomo.co.jp/service/imode/make/content/ip/#ip)
    ・[KDDI au: 技術情報 \> IPアドレス帯域](http://www.au.kddi.com/ezfactory/tec/spec/ezsava_ip.html)
    ・[WEB & NETWORK　IPアドレス](http://creation.mb.softbank.jp/web/web_ip.html) (ソフトバンク)
    ・[技術情報 | イー・モバイル](http://developer.emnet.ne.jp/ipaddress.html)
    ・[WILLCOM｜ウィルコムのセンター情報](http://www.willcom-inc.com/ja/service/contents_service/create/center_info/#01)