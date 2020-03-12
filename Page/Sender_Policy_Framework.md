> この記事は[Sender Policy Framework](https://ja.wikipedia.org/wiki/Sender_Policy_Framework)から翻訳されています。


**Sender Policy Framework**（センダー・ポリシー・フレームワーク）とは、[電子メール](../Page/電子メール.md "wikilink")における**[送信ドメイン認証](https://ja.wikipedia.org/wiki/送信ドメイン認証 "wikilink")**のひとつ。差出人の[メールアドレス](../Page/メールアドレス.md "wikilink")が他の[ドメイン名](../Page/ドメイン名.md "wikilink")に[なりすまし](https://ja.wikipedia.org/wiki/なりすまし "wikilink")していないか検出する技術である。 **SPF** もしくは **SPF認証** とも呼ばれる。

## 概要

[インターネット](../Page/インターネット.md "wikilink")上の[電子メール](../Page/電子メール.md "wikilink")に用いられる「[SMTP](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")」は、差出人のメールアドレスを誰でも自由に名乗ることができる。これが[事実上の標準として普及したため](../Page/デファクトスタンダード.md "wikilink")、セキュリティ上の欠陥として表面化することになった。これにより、[迷惑メール送信者](../Page/スパム_\(メール\).md "wikilink")、いわゆる「スパマー」による差出人アドレスの詐称が世界各地で行われ、利用者を悩ませてきた。

そのため、議論は次第に本格化し、対策のひとつとして、SPFが登場した。これは、[IPアドレス](../Page/IPアドレス.md "wikilink")の詐称は難しいという前提のもとに策定されており、原則として、[DNSサーバ](../Page/DNSサーバ.md "wikilink")上に記載される情報を取得するだけで、認証を完了できる。SPF対応したドメインにするには、そのドメインが属するDNSサーバ内の[ゾーンファイル](https://ja.wikipedia.org/wiki/ゾーンファイル "wikilink")に対して、 **SPFレコード** と呼ばれる構文を追記することで容易に実装できる。

SPFは、全ての迷惑メールを防御できるわけではない。SPFが行うのは、あくまで「差出人アドレスに記載された[ドメイン名](../Page/ドメイン名.md "wikilink")を読みとり、正しいメールサーバから送信されているかどうかを検出すること」である。そのため、例えば大企業や政府などのドメインになりすました電子メールを経由した[フィッシング詐欺](https://ja.wikipedia.org/wiki/フィッシング詐欺 "wikilink")などには効果があるものの、**差出人アドレスを詐称していない迷惑メールは検出できない**。また、同一ドメイン内で、アカウント部分のみを詐称してメール送信ができる場合、SPFでは検出ができない。

しかし、SPFは、ドメイン所有者側での対応が比較的容易であることもあり、普及は進んでいると言える。日本においては、[携帯電話](../Page/携帯電話.md "wikilink")事業者を中心に、電子メールで用いられる[フィルタリング](https://ja.wikipedia.org/wiki/フィルタリング "wikilink")サービスのひとつとして提供されており、「ドメイン認証」のほか「**なりすましメール対策**」などと称されて急速に普及している。

### SPFレコード

SPFは、RFC 7208 で定められており、その仕様が公開されている。

SPFレコードの一般的な内容を示す。以下の内容が指定されたドメインは、「指定したIPアドレス帯域から送信された電子メールなら信頼して欲しいが、それ以外のIPアドレスからの電子メールは拒否して欲しい」と宣言することになる。

``` text
v=spf1 +ip4:203.0.113.0/24 +ip4:198.51.100.0/24 -all
```

実際にSPFレコードを反映したゾーンファイルの、一般的な内容を示す。以下の内容が指定されたドメインは、「 203.0.113.1 または 203.0.113.2 から送信された電子メールは信頼して欲しいが、それ以外のIPアドレスからの電子メールは拒否して欲しい」と宣言することになる。

``` text
  :
  :
      IN  MX  10 mail
      IN  TXT "v=spf1 +ip4:203.0.113.1 +ip4:203.0.113.2 -all"
      IN  A   203.0.113.1
mail  IN  A   203.0.113.2
  :
  :
```

古いDNSサーバとの互換性を維持するため、SPFレコードは450文字以内に収めることが推奨される。しかし、DNSサーバのTXTレコードは、1行につき255文字しか記入できないことに注意を要する。例として、電子メールを送信する[IPアドレス](../Page/IPアドレス.md "wikilink")帯域が非常に多くあり255文字を超える場合には、以下のようにレコードの途中でダブルクウォートを閉じ、区切りながら記述する必要がある。区切られた部分は、DNSサーバによってそのまま結合され解釈される。

``` text
  :
  :
      IN  MX  10 mail
      IN  TXT "v=spf1 "
              "+ip4:203.0.113.0/28 +ip4:198.51.100.64/28 +ip4:192.0.2.16/28 "
              "+ip4:203.0.113.128/28 +ip4:198.51.100.96/28 +ip4:192.0.2.48/28 "
              "+ip4:203.0.113.144/28 +ip4:198.51.100.128/28 +ip4:192.0.2.160/28 "
              "+ip4:203.0.113.160/28 +ip4:198.51.100.160/28 +ip4:192.0.2.176/28 "
              "+ip4:203.0.113.192/28 +ip4:198.51.100.192/28 +ip4:192.0.2.240/28 "
              "-all"
      IN  A   203.0.113.1
mail  IN  A   203.0.113.2
  :
  :
```

以下の内容が指定されたドメインは、「 sp.example.jp や sp.example.com で指定されている SPF レコードの記述に準じる」と宣言することになる。後述するが、ip4 ip6 all 以外の項目が1レコード内に10個を超えてはならない。

``` text
  :
  :
      IN  MX  10 mail
      IN  TXT "v=spf1 +ip4:203.0.113.2 include:sp.example.jp include:sp.example.com -all"
      IN  A   203.0.113.1
mail  IN  A   203.0.113.2
  :
  :
```

## 動作原理

SPFは、あるドメインのための電子メールを送信することが正式に認められているマシンはどれかという事（以下送信者[ポリシー](https://ja.wikipedia.org/wiki/ポリシー "wikilink")）を、ドメイン所有者が専用の書式を使って[DNSのTXTレコードに明示することを可能にする](../Page/Domain_Name_System.md "wikilink")。例えば、送信者アドレスが「〜@example.jp」で終わっている電子メールを送信することを、正式に認めていないマシンはどれかということを、「example.jp」所有者が指定できる。SPFを検証する配送先メールサーバは、電子メールの通信文を受け取る前に、権限がないマシンから届いた電子メールを拒否することができる。したがって動作原理は、SPFが本当の[Domain Name Systemの権威委任を利用することを除いて](../Page/Domain_Name_System.md "wikilink")、[DNSブラックリスト](https://ja.wikipedia.org/wiki/DNSブラックリスト "wikilink")（DNSBL: DNS-based Blackhole List）による物と全く同様である。

SPFは、[エラーメール](https://ja.wikipedia.org/wiki/エラーメール "wikilink")の通知先である Return-Path のメールアドレスを保護する。 送信者アドレスは[SMTPによる通信を開始する最初に伝えられる](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")。もし送信先メールサーバがその送信者アドレスを拒否する場合は、権限のない送信元メールサーバはエラーメールをそのメールアドレスに送信するべきである。もし送信先メールサーバがその送信者アドレスを受け入れ、また続けて宛先メールアドレスと通信文も受け入れる場合は、送信者アドレスを保持するためにReturn-Pathヘッダを挿入するべきである。Return-Path のメールアドレスは、「From:」や「Sender:」のようなメールヘッダの発信者メールアドレスと一致することが多いが、必ずしもそういう訳ではない。またSPFはこれらのメールアドレス詐称を防止するものではない。

スパマーは、送信者ポリシーが記載されているドメインのアカウントを持っていたり、そのドメイン下の危殆化したシステムを不正利用することで、SPFの検証に合格（Pass）する電子メールを送信できる。また、登録ユーザーに対して任意の送信者アドレスからのSPF認証を合格させるようなサービスを提供する不正な認証サーバーを経由することでも、SPFの検証に合格する電子メールを送信できる。しかしながら、そうして作られた迷惑メールは、送信元メールサーバを容易に特定できる。

SPF の主な利点は、Return-Path の詐称にメールアドレスが使われる人々にもたらされる。彼らは頼んでもいない膨大なエラーメールやその他の自動返信メールが送りつけられ、それが電子メールを普通に使うことを難しくしている。もしそのような人々が、正規の送信IPアドレスと同時に、検証に不合格（Fail）するそれ以外の全IPアドレスをSPFレコードに明示すれば、SPFを検証する配送先メールサーバが詐称メールを拒否できるようになり、後方散乱メールの総量が減少する。

SPFは、迷惑メールの身元確認の助けとなる域を越えて、利益をもたらす可能性がある。特に送信者がSPF情報を提供する場合は、配送先メールサーバはSPFの検証に合格した結果を、既知の信頼できる送信者を識別するためのホワイトリストに結合して使うことができる。しかし、危殆化したシステムや共有メール送信システムのようなものは、この使い方を制限するだろう。

## 検証不合格とメール転送

あるドメインが検証に不合格となるSPFレコードを宣言した場合、そのドメインから送信され、配送先メールサーバから第三者へ転送された正当な電子メールは、以下の条件で配送が拒否され、エラーレスポンスが返されることがあり得る。 (1)メーリングリストと異なり、転送元メールサーバがReturn-Pathを書き換えない (2)転送先メールサーバのホワイトリストに転送元メールサーバが存在しない (3)転送先メールサーバがSPFを検証する これは必要にして明確なSPFの特徴である。配送先の「境界」メールサーバ（メールエクスチェンジャ〈MX 〉）の背後では、SPFを直接検証することはできない。

SPFの検証に不合格となる宣言をする者は、潜在的な問題を受け入れなければならない。彼らは全ての配送先メールサーバが転送処理を変更することを要求することはできない。つまり少なくともここに挙げた三つの重大な条件の内一つは明白である。

[センダー・リライティング・スキーム](../Page/センダー・リライティング・スキーム.md "wikilink") (SRS) と呼ばれる手法は、メール転送サービスがこの問題を回避するための方法である。

### HELO試験

エラーメールやその他の自動返信メールで用いられる空（から）のReturn-Pathのため、HELOアイデンティティによるSPF検証はほぼ義務と言える。「HELO `mail.example.jp`」や「EHLO `mail.example.jp`」では、実際には人為的に「`postmaster@mail.example.jp`」を検証する。

偽のHELOアイデンティティではSPF無し（None）結果は役に立たないが、有効なホスト名のために、SPFはHELOアイデンティティを保護する。このSPFの特徴は配送先メールサーバのための選択肢として常に対応され、また後のSPF草案では常にHELOを検証することが推奨される最終仕様が含まれた。

これはHELOに合格することに基づいた送信元メールサーバのホワイトリストや、またHELOに不合格となる全てのメールサーバを拒否することを可能とする。格付け（レピュテーション）システムに使われることもできる。（ホワイトリストやブラックリストは格付けシステムの単純な事例である）

## 実装

SPFの実装は2つの部分から成る。

ドメインが彼らを代表して電子メールを送信するために正式に認めたメールサーバを特定する。ドメインは彼らの既存のDNS情報へこの付加情報を追加する。 配送先メールサーバはSPF情報を要求しそれを用いることができる。メールサーバは普段どおりのDNS問合せを使い、一般的にはDNSの性能向上のためにキャッシュされる。配送先メールサーバはSPFに記載された情報を解釈し、その結果に従い行動する。

このように、ドメインが設定し配送先メールサーバが用いる、新しいDNS情報の仕様がSPFの核心である。SPFレコードは下記のように標準的なDNS構文で設定される。 example.jp. IN TXT "v=spf1 a mx -all"

「v=」は使用されたSPFのバージョンを定義する。以下の語は、あるドメインが電子メールを送信する資格があるかどうかを、決定するために用いる機構（Mechanism）を規定する。「a」および「mx」は、所定のドメインのために電子メールを送信することが許可されたコンピュータシステムを示す。SPFレコードの最後にある「-all」は、もしそれまでの機構が一致しなければ、メッセージは拒否されるべきということを示す。

### 機構

8つの機構が定義されている。

|         |                                                                                                                                                                                                      |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| all     | 常に真である。優先する機構に一致しない全てのIPアドレスのために、「`-all`」のように既定の結果として用いられる。                                                                                                                                          |
| a       | ドメイン名が、送信元メールサーバのIPアドレスに一致するAレコード（または[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")のためのAAAAレコード）を持っている場合に真となる（つまり電子メールは直接ドメイン名から届く）。                                                          |
| ip4     | 送信元メールサーバが所定の[IPv4](../Page/IPv4.md "wikilink")アドレス範囲にある場合に真となる。                                                                                                                                     |
| ip6     | 送信元メールサーバが所定の[IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink")アドレス範囲にある場合に真となる。                                                                                                                  |
| mx      | 所定のドメイン名が、送信元メールサーバのIPアドレスに結び付けられるMXレコードを持っている場合に真となる（つまり電子メールはドメインのメールサーバの内のひとつから届く）。                                                                                                               |
| ptr     | 送信元メールサーバのIPアドレスに対する逆引きドメインを正引きした結果に（[Forward Confirmed reverse DNS](https://ja.wikipedia.org/wiki/Forward_Confirmed_reverse_DNS "wikilink")）、送信元メールサーバのIPアドレスが含まれること、及び逆引きドメインが所定のドメイン名で終わる場合に真となる。 |
| exists  | 所定のドメイン名で正引きを行い、Aレコードが存在する場合に（そのIPアドレスに関係なく）真となる。 これは、[DNSBLのようにさらに複雑な照合に用いるSPFマクロ言語と一緒にしか](https://ja.wikipedia.org/wiki/スパム_\(メール\)#ブラックリスト "wikilink")、ほとんど使われない。                                 |
| include | 所定の方針を取り込み、それがSPFの検証に合格する場合に真となる。これは複数の[ISPの方針を取り込むために標準的に使われる](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")。                                                                          |

### 限定子

各々の*機構*は4つの*限定子*の内1つと結合させることができる。

  - 「**`+`**」は検証の合格（Pass）を意味する。限定子を省略した場合の既定値として用いられ、「`mx`」は「`+mx`」と同等である。
  - 「**`?`**」は検証の中立（Neutral）を意味する。方針が指定されていない場合（NONE）のように解釈される。
  - 「**`~`**」は弱い失敗（SoftFail）を意味する。中立（Neutral）と失敗（Fail）の間をデバッグする助けとなる。
  - 「**`-`**」は失敗（Fail）を意味する。電子メールは拒否されるべきである（下記参照）。

### 変更子

*変更子*はSPFの将来の拡張を考慮する。これまでのところ、RFC 7208で定められた2つの*変更子*については、広く展開された。

「`exp=some.example.jp`」は、[DNSのTXTレコードにドメイン名を挙げる](../Page/Domain_Name_System.md "wikilink")。それはSMTPエラーコードに加え失敗（Fail）の説明（一般的には[URL](../Page/Uniform_Resource_Locator.md "wikilink")）を得るためにSPFのマクロ言語を用いて解釈される。この過度に装飾的な機能はほとんど使われない。

「`redirect=some.example.jp`」は、他ドメインのSPFレコードに「all」を結び付ける代わりに使うことができる。この*変更子*は幾らか類似した*機構*である「include」を理解するより簡単である。

### エラー処理

SPF実装がSPFレコードの文法エラーを検出すると、直ちに恒久的エラー（PermError）として評価を中断し**なければならない**。誤っている*機構*を読み飛ばして続けると、その結果は予想できない。したがって「`include:bad.example`」や「`redirect=bad.example`」もまた「PermError」となる。

その他の安全策としては、DNSへ問合せる機構、すなわち「ip4」「ip6」「all」以外のあらゆる*機構*が、SPFレコード当たり最大**10**までに制限されている。SPF実装では、評価が長時間に渡る場合やDNSの問合せがタイムアウトとなった際に、一時的エラー（TempError）として評価の中断ができる。もしSPFが直接または間接的に10を超える問合せを必要とした場合は恒久的エラー（PermError）を返さ**なければならない**。「`redirect=`」もまたこの*処理制限*に数えられる。

標準的なSPF宣言である「`v=spf1 a -all`」は、(1)TXTレコード、(2)SPFレコード、(3)AまたはAAAAレコードのように、DNS問合せが3回必要である。この最後のDNS問合せの数は、最初の*機構*から制限（10）に向かって合計された物であり、今回の例では「all」がDNS問合せを必要としないため、最初の機構が最後でもある。

## 注意

SPFは通常は送信者アドレス（Return-Pathに表示されるenvelope sender）のドメインが正当であると確認するだけである。送信メールサーバを共有するドメイン（例えば[仮想ホスティング](https://ja.wikipedia.org/wiki/ホスティングサービス "wikilink")）は、それぞれ別々のドメイン名を名乗ることができる。SPFはネットワーク層で機能するため、送信者と称された人から所定の電子メールが実際に届くのかどうか確認しない。

### 検証不合格による拒否

検証に不合格となる宣言は、効果的な物となり得るが危険な手段でもある。そこで危険を回避するため、Failの代わりに（限られた試験期間のために作られた）SoftFailが宣言されることがある。しかしFailとなった電子メールを配送先メールサーバが拒否し、SoftFailとなった電子メールは迷惑メールの可能性がある物として受け入れることで、SoftFailはFailより以上に危険な物となり得る。

転送メールを拒否した時の挙動は明白である。その場合は、転送元のメールサーバはReturn-Pathで示されたメールアドレスにエラーメールを送信する。一般的なエラーメール（レスポンス）には、SMTPエラーの説明と配送に失敗した（転送先の）アドレスが含まれる。通常のSMTPエラーコードである「` 551 User not local; please try  `<転送先アドレス>」を模倣して、元の送信者は転送元のメールサーバを迂回し、転送先アドレスへ直接電子メールを再送することができる。

しかしながら、*迷惑メールの可能性がある物*として受け入れたSoftFailの電子メールは、最終的な受信者によって削除されることもある。SPFを考慮しない転送設定の経験がある利用者は、*迷惑メールの可能性がある物*とされた電子メールを、注意深く確認せずに簡単に削除することもある。

同じ論法は、本当の検証不合格メールを拒否するために配送先メールサーバはSPF提案を受けるべきということも示唆する。迷惑メールの可能性がある物として検証不合格メールを受け入れることは、検証不合格メールを簡単に拒否する事よりさらに危険となり得る。送信者ドメインにおいて検証に不合格となる宣言がされていて、それが何を意味するか知った上で宣言されていると期待できる場合は、検証不合格となったとしても、それは明らかにSPFを考慮しない転送設定により転送された物ではない。

### 検証地点

「境界」メールサーバ（メールエクスチェンジャ〈MX 〉）の背後でSPFを検証することは不可能ではない。通常、検証に関係する情報は、配送された電子メールにメールエクスチェンジャが追加した、`Received`ヘッダ行に記される。しかしこの場合、検証不合格メールを拒否するのは非常に時間が掛かり、検証地点においては原則として検証不合格メールを削除することだけ可能である。

専門家はこの権利を得られるべきだが、*プラグ・アンド・プレイ*ができる状況ではない。したがってSPF仕様では、メールエクスチェンジャの後ではなく、SMTPセッション中のメールエクスチェンジャだけが、SPFの検証をすることが推奨されている。もしSPFレコードの宣言者が彼らの方針の改善を計画する時に、一緒に[DNSキャッシュの満了を考慮して慎重に計画しないと](../Page/Domain_Name_System.md "wikilink")、メールエクスチェンジャの後でSPFを検証することは予想外の結果を得ることもある。

### [DoS攻撃](../Page/DoS攻撃.md "wikilink")

[2006年](../Page/2006年.md "wikilink")のIETF Internet-Draft（[SPFがDoSを引き起こす危険性〈SPF DoS Exploitation 〉](https://tools.ietf.org/html/draft-otis-spf-dos-exploit-01)）では、SPFに関するDNS回答の規模によっては、SPFをDNSへ打撃を与える手段とする[ネットワーク攻撃に繋がるという懸念について議論された](../Page/DoS攻撃.md "wikilink")。この問題は、SPFに関するRFCの「セキュリティに関する考察」（Security Considerations）でも取り上げられている。SPFプロジェクトはこの草案の詳細な[分析](http://www.open-spf.org/draft-otis-spf-dos-exploit_Analysis/)を行い、SPFはDNSサービス拒否攻撃の原因とならないという結論を下した。

この結論で見落とされていることは、SPFの機構は10個までに制限されているが、それぞれの機構が名前解決をするごとに10個のDNS問合せが行われ、攻撃対象に対して合計100個の問合せを一度に引き起こすかもしれないということである。その上、送信者アドレスのlocal-part（@の左側部分）に展開されるマクロ文字は、それ以降の問合せを無作為化するために用いることができるため、スパマーの資源は何も消耗されない。そのようなネットワーク通信は、DNSは問合せより回答の方がデータ量が多い（つまりデータ量を増幅させる）という特性を悪用したDNSアンプ攻撃を無限に引き起こすことを意味する。この起こり得る弱点の重大性は他の通信規約（ネットワーク・プロトコル）ではみられない物である。

## 歴史

[2003年](../Page/2003年.md "wikilink")に開催された[YAPC](https://ja.wikipedia.org/wiki/YAPC "wikilink")（Yet Another Perl Conference）と[OSCON](https://ja.wikipedia.org/wiki/OSCON "wikilink")（O'Reilly Open Source Convention）において、SPFの概念が紹介された。[2002年](../Page/2002年.md "wikilink")に[ポール・ヴィクシー](../Page/ポール・ヴィクシー.md "wikilink")（Paul Vixie）により著された"Repudiating Mail-From"（『Mail-Fromの否認』）という短い論説である。その前身は、Hadmut Danischによる"Reverse MX"（RMX）と、Gordon Fecykによる"Designated Mailer Protocol" （DMP）であった。

2003年6月、[メン・ウェン・ウォン](https://ja.wikipedia.org/wiki/メン・ウェン・ウォン "wikilink")（Meng Weng Wong）はRMXとDMP仕様を融合し、他のプログラマからの提案を求めた。その後6ヶ月以上に渡り多くの改良が為され、コミュニティはSPFの取り組みを始めた。

当初、SPFは"**Sender Permitted From**"の略であり、時には"SMTP+SPF"とも呼ばれた。その後[2004年](../Page/2004年.md "wikilink")2月には、SPFの正式名称が"Sender Policy Framework"に変更された。

2004年前半には、[IETFは](../Page/Internet_Engineering_Task_Force.md "wikilink")[MARID](https://ja.wikipedia.org/wiki/MARID "wikilink")（MTA Authorization Records in DNS）ワーキンググループを組織し、SPFとマイクロソフトのCallerID提案を基にして、現在[Sender IDとして知られていることの制定を試みた](https://ja.wikipedia.org/wiki/Sender_ID "wikilink")。

しかしMARIDによる検討が失敗に終わり、SPFコミュニティは元の"Classic"バージョンのSPFに立ち返り、RFC化を目指すことを決定した。[2005年](../Page/2005年.md "wikilink")7月にはClassicバージョンの仕様がIETF experimentとして[IESGにより承認](../Page/Internet_Engineering_Steering_Group.md "wikilink")、そして[2006年](../Page/2006年.md "wikilink")[4月28日](../Page/4月28日.md "wikilink")、SPFはとしてRFC化された。

### 論争

[2004年](../Page/2004年.md "wikilink")[1月5日](../Page/1月5日.md "wikilink")、[スティーヴン M. ベロヴィン](https://ja.wikipedia.org/wiki/スティーヴン_M._ベロヴィン "wikilink")（Steven M. Bellovin）は[長い電子メール](http://permalink.gmane.org/gmane.culture.people.interesting-people/3797)を書き、SPFに関する幾つかの懸念について議論した。それは次のような内容だった。

  - SPFはDNSのTXTレコードを使うが、TXTレコードは特別な意味を持たない自由形式の文章であることが想定されている。SPFの支持者は、SPF用に明確に指定されたレコードを持つ方が良いと直ちに肯定するが、その選択はSPFの迅速な実装を可能にした。[2005年](../Page/2005年.md "wikilink")7月、[IANAはSPFにtype](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") 99の資源レコードを割り当てた。SPFを宣言する者は両方のレコード型で宣言する可能性があり、SPFの検証ソフトはそれぞれの型を検証する可能性がある。全てのDNSソフトがこの新しいレコードに完全に対応するまで、何年も掛かることが予想される。

彼がこの声明文を書いた時は、これが正しい方法であるという合意はなかった。幾つかの主要なメールサービス業者はこの理論に同意しなかった。多くの利用者を抱える主要なメールサービス業者が対応するまで、それらのメールサービスを直接利用する者や、それらのメールサービスのドメインを詐称した電子メールを受け取る者に対して、SPFはあまり効果を上げることができない。SPFに対する関心が高まった時から、特にAOLが[SPFを採用した](http://postmaster.aol.com/spf/)点に注目する価値がある。

  - ベロヴィンの最も強い懸念は、SPFの根底にある前提（SPFの「意味論モデル」）に関連する物であった。SPFを使う時、どのように電子メールが送信されることが許されるのかということを、SPFのDNSレコードは決定する。つまり電子メールの送信方法についてドメインの所有者が制御することになる。（例えば、医師や弁護士などの専門家に対して作られたメールアドレスなど）個人が移動する先々で使える「携帯型」のメールアドレスを使う人は、メール送信に用いるメールサーバのドメインを送信者アドレスとして使うことが必須となっている。しかしその送信者アドレスはすでに存在しないかも知れない。それらの「携帯型」メールアドレスを提供している組織は、その組織が自ら**Mail Submission Agent（MSA）**（RFC 4409）や[Virtual Private Network](../Page/Virtual_Private_Network.md "wikilink")（VPN）を用意するということもあり得る。またSPFはメール送信を許されたMSAに[SMTPのReturn](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")-Pathを関係付けるだけであり、利用者が別の場所で発行された自分のメールアドレス（RFC 2822）\[1\]を使うことは自由なままである。

Jonathan de Boyne Pollardは、SPFが電子メールに関するRFCと矛盾するという議論において、SPFに反対して[別の痛烈な非難](http://homepages.tesco.net/J.deBoynePollard/FGA/smtp-spf-is-harmful.html)を書いた。ISPの顧客に特定の方法で電子メールを使用させることをISPに押し付けることと、[転送時の問題がSPFの能力である](https://ja.wikipedia.org/wiki/#検証不合格とメール転送 "wikilink")。

### 配備

その限界にもかかわらず、多くの人はSPFの利点がその欠点に勝ることを確信し、SPFの実装を始めた。[SpamAssassin](https://ja.wikipedia.org/wiki/SpamAssassin "wikilink") version 3.0.0や[Anti-Spam SMTP Proxy](https://ja.wikipedia.org/wiki/Anti-Spam_SMTP_Proxy "wikilink")（ASSP）といった迷惑メール対策ソフトウェアがSPFに対応した。多くのメールサーバ（MTA: [Message Transfer Agent](https://ja.wikipedia.org/wiki/Message_Transfer_Agent "wikilink")）は、[CommuniGate Pro](https://ja.wikipedia.org/wiki/CommuniGate_Pro "wikilink")、[Wildcat](https://ja.wikipedia.org/wiki/Wildcat!_BBS "wikilink")、[Microsoft Exchange](https://ja.wikipedia.org/wiki/Microsoft_Exchange "wikilink")、[SmarterMail](http://www.smartertools.com)のように直接SPFに対応したり、また[Postfix](../Page/Postfix.md "wikilink")、Sendmail、[Exim](https://ja.wikipedia.org/wiki/Exim "wikilink")、[qmail](https://ja.wikipedia.org/wiki/qmail "wikilink")のように修正パッチやプラグインの形でSPFに対応した。[Amazon](../Page/Amazon.com.md "wikilink")、[AOL](../Page/AOL.md "wikilink")、[EBay](../Page/EBay.md "wikilink")、[Google](../Page/Google.md "wikilink")、[GMX](https://ja.wikipedia.org/wiki/w:de:United_Internet "wikilink")、[Hotmail](../Page/Hotmail.md "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")、[W3Cといった多くの有名なドメインは](../Page/World_Wide_Web_Consortium.md "wikilink")、2004年中頃にはSPFデータを宣言することを決めた。

[2007年](../Page/2007年.md "wikilink")に発表された調査によると、`.com`ドメインおよび`.net`ドメインの5%が、何らかの送信者ポリシーが宣言されていた。ただしこれには「`v=spf1 ?all`」のように全く役に立たない宣言も含まれている可能性がある。[1](http://www.onlamp.com/pub/a/onlamp/2007/01/11/dns-extensions.html)

### 日本における普及

現在、日本の下記携帯電話会社においてSPF認証が導入または導入予定である。ただし、その実装は標準とは一部異なり、検証の対象や条件は各社で異なる。

  - [au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink") - 「メールフィルター」サービスにおいて「ドメイン認証規制」\[2\]を選択可能。エンベロープFrom、それが存在しなければHELOドメインが検証の対象\[3\]となる。
  - [DoCoMo](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink") - 「なりすましメール対策」を導入（[2007年](../Page/2007年.md "wikilink")[11月](../Page/11月.md "wikilink")）。メールヘッダのFromフィールド、それが存在しなければエンベロープFromが検証の対象\[4\]となる。
  - [SoftBank](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink") - 「なりすましメール拒否設定」が導入の予定\[5\]。

## 実効性

前述の通り、SPFは部分的にではあるものの、迷惑メールの防御に役立つと言われている。しかし、実効性には疑問の声がある。

  - 2005年には、SPFを逆手に取ったスパムが増加したことが報じられている\[6\]。これによると、スパムの9%はSPF認証に合格しているメールであり、そのうちの84%はスパム送信用に設けられたドメインであるという。つまり、登録ユーザーに対して任意の送信者アドレスからのSPF認証を合格させるようなスパム送信者用のドメインが横行しているということである。
  - 前述の通り、日本の一部の携帯電話会社ではSPF認証を導入している。しかし、2011年時点で設けられている仕組みは、SPF認証に合格したメールを許可し、合格しなかったものについて成りすまし判定を行うというものである。この仕組みでは、前項のように、スパム送信者用のドメイン経由で配信された、適当な送信者メールアドレスが付けられたSPF認証に合格したメールを許可することになってしまう。パソコンのメールにおいては過去より強固なフィルタリングルールが指定できるものが多く登場しており、そのようなものを使用すれば排除可能であるが、携帯メールについては左記の理由から、そうは言えない側面がある。
  - 前述の通り、SPFによって迷惑メールに対する追跡や法的な請求が容易になると言われている。しかし、SPFによって得られる情報は、送信者メールアドレスに対してSPF認証に合格したというお墨付きをあるメールサーバーが与えるだけのものである。そのメールサーバーを経由したというところまでの追跡は容易になるが、前述のような「登録ユーザーに対して任意の送信者アドレスからのSPF認証を合格させるようなスパム送信者用のドメイン」を経由した迷惑メールに対して、送信者を追跡できるだけの情報が得られるとは言えない。また、法的な請求については法的整備の範疇であり、SPFの守備範囲からは外れる。実際、日本においては[特定電子メールの送信の適正化等に関する法律](../Page/特定電子メールの送信の適正化等に関する法律.md "wikilink")のような法的整備が行われているが、依然として迷惑メールの量は増加傾向にある\[7\]といった報告がある。

## 脚注

<references />

## 参考

  - [送信ドメイン認証](https://ja.wikipedia.org/wiki/送信ドメイン認証 "wikilink")
      - [ドメインキー](../Page/ドメインキー.md "wikilink")（DomainKeys）
      - [Sender ID](https://ja.wikipedia.org/wiki/Sender_ID "wikilink")
      - [センダー・リライティング・スキーム](../Page/センダー・リライティング・スキーム.md "wikilink")
      - [Sender Signing Policy](https://ja.wikipedia.org/wiki/Sender_Signing_Policy "wikilink")
      - [ドメインキー・アイデンティファイド・メール](../Page/ドメインキー・アイデンティファイド・メール.md "wikilink")（DKIM）
  - [MARID](https://ja.wikipedia.org/wiki/MARID "wikilink")

## 外部リンク

  - RFC 7208: Sender Policy Framework (SPF) for Authorizing Use of Domains in Email, Version 1
  - [SPF homepage](http://www.openspf.org) and [news](http://www.openspf.org/News)
  - [Mailing list archives](http://dir.gmane.org/index.php?prefix=gmane.mail.spam.spf)
  - [SPF Testing site](http://www.dnsstuff.com/pages/spf.htm)
  - [ONLamp report about DNS extensions](http://www.onlamp.com/pub/a/onlamp/2007/01/11/dns-extensions.html)（2007年1月）
  - [*emailbattles*: SPF Claws Sender-ID](http://www.emailbattles.com/archive/battles/spam_aabeeighag_ef/)（2005年8月）
  - [Canadian recommendation for ISPs](http://e-com.ic.gc.ca/epic/internet/inecic-ceac.nsf/en/gv00329e.html)（2005年5月）
  - [Interview with co-author W. Schlitt](http://www.cbronline.com/article_news.asp?guid=44D2955C-3C04-4BA1-AC45-AF8277B8B455)（2005年3月）
  - [David Woodhouse discusses flaws in SPF](http://david.woodhou.se/why-not-spf.html)（2005年1月）
  - [SpamCop FAQ entry about bogus bounces](http://www.spamcop.net/fom-serve/cache/329.html) discusses also SPF（2005年）
  - [M. Wong's Deployment White Paper](http://www.openspf.org/whitepaper.pdf)（PDF、2004年11月）
  - [The Register: Spammers embrace email authentication](http://www.theregister.co.uk/2004/09/03/email_authentication_spam/)（2004年9月）
  - [CircleID interview with co-author M. Wong](http://www.circleid.com/posts/an_interview_with_the_lead_developer_of_spf_part_i/)（2004年6月）
  - [Brad Knowles considers SPF as harmful](http://bradknowles.typepad.com./considered_harmful/2004/05/spf.html)（2004年5月）
  - [Jonathan de Boyne Pollard's list of the flaws in SPF](http://homepages.tesco.net./~J.deBoynePollard/FGA/smtp-spf-is-harmful.html)（2004年）
  - [Diagram of e-mail flow and SPF's impact](http://www.openspf.org/mailflows.pdf)（PDF、[PNG](http://www.openspf.org/mailflows-l.png)）
  - [MIT Spam Conference Handout on SPF](http://www.openspf.org/for-mit-spam-conference.html)（2004年1月）
  - [Steve Bellovin expresses doubts](http://www.interesting-people.org/archives/interesting-people/200401/msg00037.html)（2004年1月）

[Category:電子メールのプロトコル](https://ja.wikipedia.org/wiki/Category:電子メールのプロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.  [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")10月、RFC 2822は、RFC 5322で置き換えられた。
2.
3.
4.
5.
6.
7.