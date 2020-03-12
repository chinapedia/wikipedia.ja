> この記事は[OpenID](https://ja.wikipedia.org/wiki/OpenID)から翻訳されています。


（）は分権的な認証プロトコルの[オープンスタンダードで](../Page/オープン標準.md "wikilink")、非営利団体の財団が標準を策定している。名称は同団体の登録商標である\[1\] 。

2016年現在の最新版のOpenIDは2014年2月に発行され\[2\]同年11月にアップデートされた\[3\]**OpenID Connect (OIDC) 1.0**である。

## 財団標準

財団では、誰でも参加可能な手順「」を経て、[デジタルアイデンティティ](../Page/デジタルアイデンティティ.md "wikilink")関連の標準化を行なっている。現在有効、ないしは策定中の仕様には以下のようなものがある。

###

2009年に 2.0の標準化がIETFで始まったことを受けて策定が始まった、次世代の[認証](../Page/認証.md "wikilink")・[連合アイデンティティ](https://ja.wikipedia.org/wiki/連合アイデンティティ "wikilink")システムの[標準](https://ja.wikipedia.org/wiki/標準 "wikilink")。

HTTP上で使う場合には\[\[OAuth| 2.0をベースにしながら、HTTP以外のプロトコル（XMPP他）にも拡張可能になっており、スマートフォン上でのアプリの台頭を意識した作りになっている。

セキュリティ的にも、 2.0がNIST SP800-63ベースでレベル2程度までしかサポートできないのに対して、最高レベルであるレベル4まで対応できるように設計されている。

これに当たって、別規格として\[\[JSON_Web_Token|</ref> |accounts.google.com |- |Amazon |Amazon Cognito User Pools |https://cognito-idp.{region}.amazonaws.com/{userPoolId}\[4\] |}

###

2.0、 のみではなく、SAMLなどでも問題になるユーザーインターフェースの問題（問題、問題）を解決すべく検討されている仕様。

###

携帯電話会社がOpenID ConnectのIdPになるために必要になる追加仕様を規定している。

###

健康情報交換のための仕様。

### （Deprecated） 2.0

注：OpenID Authentication 2.0 は、OpenID Connectによって置換えられた。

2007年12月に制定された、[ウェブサイト](../Page/ウェブサイト.md "wikilink")によらず使用できる[認証](../Page/認証.md "wikilink")・[連合アイデンティティ](https://ja.wikipedia.org/wiki/連合アイデンティティ "wikilink")システムの規格の一つ。ユーザを識別するには、URIベースの**主張識別子**\[5\]を用いる。これは、ユーザが入力したものではなく、認証サーバが割り当てた再利用されないURIである。その為、ユーザ識別子の使い回しによる、旧ユーザのアカウントを新ユーザがのっとってしまう **ユーザー・インパーソネイション**\[6\] と呼ばれる問題が解決されるなどの特徴を持っている。

また、、 などの拡張仕様を利用することによって、ユーザの属性情報を連携することができる他、どのような本人確認や認証手段（パスワード、OTP、ICカードなど）を使ったかなどの**認証コンテキスト**\[7\]も同時に連携可能である。

拡張仕様には、

  -
  -
  -
がある。

プロバイダには、ヤフー、AOL、フランステレコム、ドイチェ・テレコム、NTT、KDDI、ソフトバンクなど多数が対応している。

## Open Process

\[8\]によって規定される標準化プロセス。概ね以下の経緯をとって仕様として標準化される。

1.  ワーキンググループ設置提案（設立趣意書提出）
2.  仕様カウンシルによるレビュー
3.  理事会によるレビュー
4.  ワーキンググループ設置
5.  ワーキンググループメンバーによる\[9\]提出
6.  ワーキング・ドラフト作成
7.  実装者仕様案レビュー（45日間）
8.  実装者仕様案投票（7日間）
9.  実装事例およびフィードバック収集
10. （大幅な変更が会った場合は、実証者仕様案レビューに戻る）
11. 最終仕様案レビュー（60日間）
12. 最終仕様投票（7日間）
13. 最終仕様公開

## 財団

米国オレゴン州で設立された、501(c)(6) 非営利団体である。著作権管理、商標管理、仕様をライセンス費用無しに使うことができるようにする（制限付き特許権非行使ライセンス）ための標準化プロセスの管理、財団の標準化プロセスで標準化された各種規格についての普及啓蒙を行うことを使命としている。

特許権管理は、「制限付き特許権非行使ライセンス」と呼ばれるモデルで、OpenID財団標準仕様の実装に対して、不可逆的特許権非行使宣言を行った主体に対しては特許権を互いに行使しないというものになっている。OpenID財団標準を実装したある企業が、他の企業に対して特許権の主張を行った場合、他の特許権保持者は当該企業に対しては特許権の行使ができるようになる。このため、特許権の行使には抑制的に働き、結果的に通常のロイヤリティ・フリーモデルよりも安全に利用できるようになることを狙っている。

### 役員

役員\[10\]は以下の通り。

| 役職   | 担当者                                                                  |
| ---- | -------------------------------------------------------------------- |
| 理事長  | Nat Sakimura （[崎村夏彦](https://ja.wikipedia.org/wiki/崎村夏彦 "wikilink")) |
| 副理事長 | Adam Dawes（アダム・ドーズ）                                                  |
| 会計担当 | John Bradley（ジョン・ブラッドレイ）                                             |
| 書記   | Mike Jones（マイク・ジョーンズ）                                                |
| 執行役員 | Don Thibeau（ドン・ティボー）                                                 |

### 法人理事

法人理事\[11\]は、各スポンサー企業（年50,000ドル）によって指定された個人であり、所属が変わると他の人に引き継がれる。

| スポンサー企業                                                                 | 担当者                                                   | 備考   |
| ----------------------------------------------------------------------- | ----------------------------------------------------- | ---- |
| [野村総合研究所](../Page/野村総合研究所.md "wikilink")                                | [崎村夏彦](https://ja.wikipedia.org/wiki/崎村夏彦 "wikilink") | 理事長  |
| [グーグル](../Page/Google.md "wikilink")                                    | Adam Dawes                                            | 副理事長 |
| [KDDI](../Page/KDDI.md "wikilink")                                      |                                                       |      |
| [マイクロソフト](../Page/マイクロソフト.md "wikilink")                                | Anthony Nadalin                                       |      |
| [ペイパル](https://ja.wikipedia.org/wiki/Pay_Pal "wikilink")                |                                                       |      |
| [シマンテック](../Page/シマンテック.md "wikilink")                                  | Brian Berliner                                        |      |
| [ピング・アイデンティティー](https://ja.wikipedia.org/wiki/Ping_Identity "wikilink") | Sarah Squire                                          |      |
| [ベライゾン](https://ja.wikipedia.org/wiki/ベライゾン "wikilink")                 | Bjorn Hjelm                                           |      |
| [アメリカ合衆国保健福祉省](https://ja.wikipedia.org/wiki/アメリカ合衆国保健福祉省 "wikilink")   | Debbie Bucchi                                         |      |

### コミュニティ理事

コミュニティ理事 \[12\] は、選挙によって選ばれる。なお、コミュニティ理事は、企業を離れた個人として選ばれており、所属が変わっても継続するので、所属はあくまで参考である。

| 担当者              | 備考           |
| ---------------- | ------------ |
| John Bradley     | Yubico、会計    |
| Michael B. Jones | マイクロソフト所属、書記 |
| George Fletcher  | OATH所属       |

## Openファウンデーション・ジャパン

2008年2月28日ファウンデーション・ジャパンの設立が発表され、2008年10月1日ファウンデーション・ジャパンが有限責任中間法人として設立された、財団の日本支部。発起人企業は、[シックス・アパート](../Page/シックス・アパート.md "wikilink")、[日本ベリサイン](https://ja.wikipedia.org/wiki/日本ベリサイン "wikilink")、[野村総合研究所](../Page/野村総合研究所.md "wikilink")の3社。参加企業は、ウェブ系だけでなく、銀行、保険、運輸など幅広く、2012年7月現在で42社に及ぶ\[13\]。

### 人物

  - [楠正憲](https://ja.wikipedia.org/wiki/楠正憲 "wikilink")（代表理事）
  - [崎村夏彦](https://ja.wikipedia.org/wiki/崎村夏彦 "wikilink")（理事）
  - [米谷修](https://ja.wikipedia.org/wiki/米谷修 "wikilink")（理事）
  - 林達也 (理事)
  - [富士榮 尚寛](https://ja.wikipedia.org/wiki/富士榮_尚寛 "wikilink") (理事)
  - [真武信和](https://ja.wikipedia.org/wiki/真武信和 "wikilink")（事務局長）

## 脚注

## 参考文献

  - [ 2.0時代の幕開け](https://www.atmarkit.co.jp/ait/articles/0802/19/news133.html) (IT)
  - [米国で盛り上がる“”](https://ascii.jp/elem/000/000/020/20628/)（）
  - [が熱狂的に受け入れられる理由](https://www.atmarkit.co.jp/news/analysis/200704/23/openid.html)（IT）
  - [での紹介記事](https://internet.watch.impress.co.jp/cda/news/2007/02/14/14773.html)

## 関連項目

  - [デジタルアイデンティティ](../Page/デジタルアイデンティティ.md "wikilink")

  - [シングルサインオン](../Page/シングルサインオン.md "wikilink")

  -
  - [{{lang](https://ja.wikipedia.org/wiki/i-name "wikilink")

  - [{{lang](https://ja.wikipedia.org/wiki/OAuth "wikilink")

  - [連合アイデンティティ](https://ja.wikipedia.org/wiki/連合アイデンティティ "wikilink")

## 外部リンク

  - <https://openid.net/> —
  - <https://www.openid.or.jp/> — ファウンデーション・ジャパン

[Category:アイデンティティ管理システム](https://ja.wikipedia.org/wiki/Category:アイデンティティ管理システム "wikilink") [Category:ウェブ技術](https://ja.wikipedia.org/wiki/Category:ウェブ技術 "wikilink")

1.  【類似群コード】37D06 42N03 42P02 42P03 42Q02 42Q99 42X11
2.
3.
4.  `iss` クレームの形式は次のとおりです。 [ユーザープールのトークンの使用 - 発行者 (iss)](https://docs.aws.amazon.com/ja_jp/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-with-identity-providers.html)
5.
6.
7.
8.  <http://openid.net/wordpress-content/uploads/2010/01/OpenID_Process_Document_December_2009_Final_Approved.pdf>
9.  <http://openid.net/wordpress-content/uploads/2010/01/paper-contribution-agreement-20100122.doc>
10.
11.
12.
13. [ ファウンデーション・ジャパン - 会員一覧](http://www.openid.or.jp/modules/docs/member/member.html)