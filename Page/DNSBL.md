> この記事は[DNSBL](https://ja.wikipedia.org/wiki/DNSBL)から翻訳されています。


**DNSBL**とは、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上で（一部の人々が）防ぎたい[IPアドレス](../Page/IPアドレス.md "wikilink")の一覧を[ソフトウェア](../Page/ソフトウェア.md "wikilink")が扱いやすい形式で公表したもの。**DNSブラックリスト**とも。[Domain Name System](../Page/Domain_Name_System.md "wikilink") (DNS) 上に構築された技術であり、DNSBLは主に[スパムに関係するアドレスの一覧を公表するのに使われている](../Page/スパム_\(メール\).md "wikilink")。たいていの[メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")（メールサーバ）は、この一覧上にあるサイトから送られてきた電子メールを拒否したりフラグを付けたりするよう設定することができる。

DNSBLは特定の一覧や[ポリシー](https://ja.wikipedia.org/wiki/ポリシー "wikilink")の名称ではなく、そのような一覧の総称である。[MAPS](https://ja.wikipedia.org/wiki/:en:Mail_Abuse_Prevention_System "wikilink") RBL や [SPEWS](https://ja.wikipedia.org/wiki/:en:Spam_Prevention_Early_Warning_System "wikilink") といった特定の一覧に関しては、運営方針をめぐって多くの議論がなされてきた。

## 用語

以下はそれぞれ相互に密接に関連した用語である。

  - RBL (Real-time Blackhole List)
    この種の技術を使った最初のシステムの名称。プロプライエタリな MAPS DNSBL と "RBL" は登録商標である\[1\]。一部のメールソフトでは設定パラメータ名を "RBLs" あるいは "RBL domains" としているが、MAPS RBL だけでなく任意の DNSBL を指定可能である。
  - DNSBL (DNS Blacklist)
    ブラックリスト (Blacklist) という言葉の使用は若干語弊があると考える人もいる（[ジョセフ・マッカーシー](https://ja.wikipedia.org/wiki/ジョセフ・マッカーシー "wikilink")を思い起こさせるため）\[2\]。そこで DNSBL を "DNS blocklist" の略ということにしようと言う人もいる（ただし、DNSBL が常にブロックに直接使われるわけではない）。また、RBL からの連想で "DNS blackhole list" を提案する人もいるが、DNSBL によって[ブラックホールが生成されるわけではない](https://ja.wikipedia.org/wiki/ブラックホール_\(ネットワーク\) "wikilink")。当たり障りのない用語として "DNS-Based List" も提案されている\[3\]\[4\]\[5\]。
  - DNSWL (DNS Whitelist)
    その一覧を作った人々が、もっと好意的に扱ってほしいと考えているIPアドレスの一覧。
  - RHSBL (Right Hand Side Blacklist)
    DNSBL に似ているが、IPアドレスではなく[ドメイン名](../Page/ドメイン名.md "wikilink")の一覧である。名称の "right-hand side" とはメールアドレスの *@* 記号の右側を意味し、その部分をRHSBLで参照する。
  - URIBL ([Uniform Resource Identifier](../Page/Uniform_Resource_Identifier.md "wikilink") Blacklist)
    メールの本文で言及されているウェブサイトのURIの中に出現するドメイン名とIPアドレスの一覧である。RHSBLがメールアドレスで使われているドメイン名の一覧であるのとは対照的である\[6\]。

## 歴史

最初のDNSBLは Real-time Blackhole List (RBL) で、1997年に[ポール・ヴィクシー](https://ja.wikipedia.org/wiki/ポール・ヴィクシー "wikilink")が自身の開発した [Mail Abuse Prevention System (MAPS)](https://ja.wikipedia.org/wiki/:en:Mail_Abuse_Prevention_System "wikilink") の一部として作った。最初の加入者は Adovenet の Dave Rand であった\[7\]。当初、RBLはDNSBLではなく、むしろ加入者が所有する[ルーター](../Page/ルーター.md "wikilink")に[BGP経由で転送されるネットワークの一覧であり](https://ja.wikipedia.org/wiki/ボーダ・ゲートウェイ・プロトコル "wikilink")、スパムを送るのに使われたマシンやウェブサイトのようなスパムを可能にするサービスを行っているホストについて、全ての[TCP/IPトラフィックをブラックホール化させることが可能であった](../Page/インターネット・プロトコル・スイート.md "wikilink")（ブラックホール化とは、トラフィックを全く通知することなく捨てること）。

RBLの目的は単にスパムをブロックするだけではなく、[インターネットサービスプロバイダ](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")や他のサイトをスパムや関連する問題（[第三者中継](https://ja.wikipedia.org/wiki/第三者中継 "wikilink")、スパム的広告など）について教育することにあった。RBLにアドレスが掲載される前に、ボランティアやMAPSスタッフがそのアドレスの責任者に何度もコンタクトをとり、問題を修正してもらう。このような作業は全トラフィックをブラックホール化する前に是非とも実施しておく必要があったが、同時にスパマーやスパムをサポートしているISPはそのような議論が続いている間はRBLに掲載されることを遅らせることができ、それは時には非常に時間がかかった。

その後RBLはDNSBL形式でもリリースされ、ポール・ヴィクシーは [sendmail](https://ja.wikipedia.org/wiki/sendmail "wikilink") や他のメールソフトウェアの作者にRBLクライアントの実装を奨励した。これによりメールソフトはRBLに問合せることができ、その一覧に掲載されているサイトからの電子メールを排除できるようになった。そのため、全トラフィックをブラックホール化しなくともメールサーバ単位に実施できるようになった。

RBLの登場後まもなく、他にもそれぞれ独自のポリシーで一覧を作る人々が登場した。そのうちの1つが Alan Brown の [Open Relay Behavior-modification System (ORBS)](https://ja.wikipedia.org/wiki/:en:ORBS "wikilink") である。これは[第三者中継](https://ja.wikipedia.org/wiki/第三者中継 "wikilink")に利用可能な状態（スパマーがスパム転送に利用可能な状態）のメールサーバを自動的に見つけ出し、一覧に加える。当時は多くの人が第三者中継は許容されると考えていたため、それを探索するORBSに対しては多くの批判が寄せられた。

[2003年](../Page/2003年.md "wikilink")、いくつかのDNSBLは[DoS攻撃](https://ja.wikipedia.org/wiki/DoS攻撃 "wikilink")にさらされた。攻撃者は不明であるため、その目的は憶測するしかない。しかし、スパマーがDNSBLの運用を妨害し閉鎖に追い込むことを目的として攻撃したと信じられている。2003年8月、[SPEWSデータセットに基づいたいくつかのDNSBLを運用していた](https://ja.wikipedia.org/wiki/:en:Spam_Prevention_Early_Warning_System "wikilink") *Osirusoft* は、数週間におよぶ攻撃を受け閉鎖を余儀なくされた。

### URI DNSBL

[URI](../Page/Uniform_Resource_Identifier.md "wikilink") DNSBL は、スパムの本文に含まれるクリック可能なリンクにある（ただしスパムでないものには出現しない）ドメイン名とIPアドレスを一覧にしたDNSBLである。

URI DNSBL はスパマーがIPアドレスを頻繁に変えてスパムメールを送信することで従来のDNSBLを出し抜くようになったために生まれた。スパムは受信者を特定のサイトに誘導するためのURIを本文に含んでいることが多く、送信元が変わっても内容は変わらないためである。そこで、スパムフィルタはメール本文から全URIを抜き出し、それを URI DNSBL と比較し、一致すれば送信元がDNSBLになくともスパムと判断してブロックできる。

主な URI DNSBL としては以下のものがある。

  - [SURBL](http://www.surbl.org/) - 最も古く有名。Jeff Chan が運営している。
  - [URIBL](http://www.uribl.com/) - SURBL 関係者によるフォーク。
  - [ivmURI](http://dnsbl.invaluement.com/ivmuri/) - SURBL にも関わっていた [Rob McEwen](http://www.linkedin.com/in/invaluement) によるもの。

URI DNSBL は RHSBL と混同されやすいが、両者は異なる。URI DNSBL はメール本文にあるドメイン名やIPアドレスを一覧にしている。RHSBL は "from" または "reply-to" にあるメールアドレスのドメイン名を一覧にしたものである。スパムの "from" アドレスは捏造されていたり、フリーメールのドメイン名（@gmail.com, @yahoo.com, @hotmail.com など）だったりするため、RHSBL はあまり有効とは言えない。あまり効果の無かった RHSBL に比べると URI DNSBL は非常に効果的で、大半のスパムフィルタが使っている。

## DNSBL の運用

DNSBL を運用するには、ホスティングのためのドメイン、そのドメインのネームサーバ、公表すべきアドレスの一覧が必要となる。

任意の汎用DNSサーバソフトウェアで DNSBL を運用することができる。しかし[CIDRネットブロック全体を一覧するようなDNSBLは効率的ではない](https://ja.wikipedia.org/wiki/Classless_Inter-Domain_Routing "wikilink")。DNSBL専用ソフトウェアがいくつかあり、より高速かつ効率的に運用でき、設定も容易である。

  - [rbldnsd](http://www.corpit.ru/mjt/rbldnsd.html) by Michael J. Tokarev
  - [rbldns](http://cr.yp.to/djbdns.html) [ダニエル・バーンスタイン](../Page/ダニエル・バーンスタイン.md "wikilink")
  - [DNS Blacklist Plug-In](http://www.simpledns.com/kb.aspx?kbid=1241) for [Simple DNS Plus](https://ja.wikipedia.org/wiki/:en:Simple_DNS_Plus "wikilink")

DNSBL 運用の難しい部分は、一覧の保守である。一般向けのDNSBLは、一覧が何を意味するかについて特定のポリシーを公表して運用されており、それが利用者の信頼を得なければならない。

### DNSBL クエリ

メールサーバがクライアントからコネクションを受け付けたとき、クライアントをDNSBL（ここでは *dnsbl.example.net*）に照らしてチェックするには、以下のようなことをする。

1.  クライアントのIPアドレス（ここでは *192.168.42.23*）のバイト順を逆転させ *23.42.168.192* とする。
2.  これにDNSBLのドメイン名を連結し *23.42.168.192.dnsbl.example.net* とする。
3.  これをドメイン名（"A"レコード）としてDNSで参照する。クライアントが一覧にあればアドレスが返ってくる。そうでなければ "NXDOMAIN" ("No such domain") というコードが返ってくる。
4.  クライアントが一覧にある場合、その名前をテキストレコード（"TXT"レコード）として参照することができる。多くのDNSBLはTXTレコードで何故そのクライアントが一覧に加えられたかという情報を公表している。

以上のようにDNSBLでのアドレス参照は、リバースDNSの参照に似ている。違いはDNSBLでは "PTR" ではなく "A" を使う点と、特殊リバースドメイン *in-addr.arpa* ではなくフォワードドメイン（上の例では *dnsbl.example.net*）を使う点である。

DNSBLクエリで一致したときに返すアドレスは非公式なプロトコルに従う。多くのDNSBLは 127.0.0.0/8 のループバックにあるアドレスを返す。127.0.0.2 が通常返され、他のアドレスを返す場合は、第三者中継、プロキシ、スパマーの所有ホストなどの種別を表す。詳細については [Anti-Spam Research Group](https://ja.wikipedia.org/wiki/:en:Anti-Spam_Research_Group "wikilink") の [Internet draft](http://tools.ietf.org/html/draft-irtf-asrg-dnsbl) を参照のこと。

### URI DNSBL

URI DNSBL クエリ（および RHSBL クエリ）はもっと直接的である。次のようにドメイン名をDNSリストホストの前に付加する。

`example.net.dnslist.example.com`

一般に"A"レコードが返ってくれば一覧にあったことになる。

### DNSBL ポリシー

DNSBL はそれぞれ固有のポリシーで運用されている。その差異は以下の3点である。

  - 目標
    そのDNSBLで探せる（一覧に掲載されている）ものは何か? それは、第三者中継に使われるメールサーバやプロキシサーバの一覧、スパム送信に使われているIPアドレス、スパマーを野放しにしているISPに属するIPアドレスなどである。
  - 候補選択
    そのDNSBLはどうやって一覧に掲載すべきアドレスを探すか? ユーザーからの情報を利用するか? スパムトラップや[ハニーポット](https://ja.wikipedia.org/wiki/ハニーポット "wikilink")を利用するか?
  - 有効期限
    一覧はどれだけの期間、有効か? 自動的に無効化されるのか、それとも手動で削除されるのか? 一覧に掲載されたホストのオペレータが削除してもらうにはどうすればよいか?

## 批判

DNSBLによって自身の電子メールがブロックされたユーザーは、大抵の場合大いに怒り、一覧の存在そのものを攻撃することもある。以下のような論争がある。

  - 動的/ダイヤルアップIPアドレスを一覧に含めること。これには静的な[ADSL](../Page/ADSL.md "wikilink")アドレスも含まれるので、「エンドユーザーIPアドレス」が適切な表現かもしれない。一部のメールサイトはそのようなアドレスからの電子メールを受け付けない。というのも、スパマーウイルスに侵された家庭内のコンピュータであることが多いためである。しかし、[SOHOユーザーが自前のメールサーバを運用する場合やノートPC上で](https://ja.wikipedia.org/wiki/Small_Office/Home_Office "wikilink")[メール転送エージェント](https://ja.wikipedia.org/wiki/メール転送エージェント "wikilink")を動作させる場合に困ったことになる。これに対処するには、多くのメールサーバに組み込まれている[スマートホスト](https://ja.wikipedia.org/wiki/スマートホスト "wikilink")機能を使って、自身のメールサーバからISPのメールサーバへ中継する必要がある。
  - [MAPS RBL](http://www.mail-abuse.com/) など、"spam-support operations" を含めている一覧。"spam-support operations" とは、それ自体はスパムを送ってはいないが、スパマーに何らかのサービスを提供しているサイトを指す（スパムに掲載されているウェブサイトをホスティングしているなど）。そのようなサイトからの電子メールを拒否するのは、スパマー相手のビジネスをやめさせようとする一種の[ボイコット](../Page/ボイコット.md "wikilink")であり、そのサイトを利用するスパマーでない一般利用者に不便を強いることになる。
  - [SPEWS](https://ja.wikipedia.org/wiki/:en:Spam_Prevention_Early_Warning_System "wikilink") など、予言的（早期警告的）一覧。SPEWS は "spam-support operations" に属するアドレスを一覧に含めている。これは、それらのアドレスが将来スパム送信に使われる可能性が高いという仮説に基づいている。SPEWS はスパムをサポートし続けるサイトのネットブロック範囲を増大させている。
  - 一部の一覧はポリシーが不明確で、削除も即座に行われない。DNSBL によっては削除にあたって料金を徴収したり（例えば uceprotect.net\[8\]）、寄付を求めたりする（例えば [SORBS](https://ja.wikipedia.org/wiki/:en:Spam_and_Open_Relay_Blocking_System "wikilink")）。

個々のDNSBLへの反対意見は多いが、中には自動的にメールを排除するシステムそのものに反対する人もいる。[ジョン・ギルモア](../Page/ジョン・ギルモア.md "wikilink")はそのような考え方から、意図的に[第三者中継](https://ja.wikipedia.org/wiki/第三者中継 "wikilink")サイトを運用している。ギルモアは、DNSBL運用者は[独占禁止法](../Page/独占禁止法.md "wikilink")を犯していると非難している。

  -
    「普通の人が電子メールを拒否するのは正当だ（ただし、それは「メッセンジャーを撃つ」ようなもので、よい方針とは言えない）。しかし、百万人が徒党を組んでブラックリストを作るなら、それは不当な独占力の行使だ」\[9\]

[電子フロンティア財団](https://ja.wikipedia.org/wiki/電子フロンティア財団 "wikilink")やといった団体は、[ISPによるDNSBLの利用に懸念を表明している](https://ja.wikipedia.org/wiki/インターネットサービスプロバイダ "wikilink")。彼らを含むグループによる共同声明では、ISPが顧客に通知せずにDNSBLなどのスパム[ブロッキングを行うことを](https://ja.wikipedia.org/wiki/ブロッキング_\(インターネット\) "wikilink")「ステルスブロッキング」と呼んでいる\[10\]。

スパマーがDNSBL運用者を訴えた事例もある。

  - [2003年](../Page/2003年.md "wikilink")、新たに設立された企業 "EmarketersAmerica" が[フロリダ州](https://ja.wikipedia.org/wiki/フロリダ州 "wikilink")でいくつかのDNSBL運用者を訴えた。スパマー Eddy Marin が背後にいたが、同社は電子メールによるマーケティングを行う企業の組合だと主張し、[Spamhaus](https://ja.wikipedia.org/wiki/:en:The_Spamhaus_Project "wikilink") と [SPEWS](https://ja.wikipedia.org/wiki/:en:Spam_Prevention_Early_Warning_System "wikilink") というDNSBL運用者が取引を不当に制限していると主張した。この訴えは原告適格でないとされ、退けられた\[11\]。
  - [2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")、アメリカの法廷で Spamhaus はスパマー "e360 Insight LLC" に損害賠償として 1171万5千ドルの支払いを命じられた。これは欠席裁判によるもので、Smanhaus はその法廷の司法権の及ばないイギリスで運営されている。

## 脚注

## 外部リンク

  - [DNSBL Lookup](http://dnsbllookup.com) - DNSBLデータベース内のブラックリストにIPアドレスをルックアップします。
  - [DNS Blacklist/Whitelist Checker](http://multirbl.valli.org/) - IP/ホスト名を入力すると即座に DNS Blacklist/Whitelist をチェックする。
  - [Blacklists Compared](http://www.sdsc.edu/~jeff/spam/Blacklists_Compared.html) - 2001年以降現在までの比較リスト
  - [Blacklist Monitor](http://www.intra2net.com/en/support/antispam/) - ブラックリストの成功率と失敗率の週間統計
  - [Howto Create a DNSBL](http://www.zytrax.com/books/dns/ch9/dnsbl.html) - DNSBL の作成方法チュートリアル

[Category:スパム](https://ja.wikipedia.org/wiki/Category:スパム "wikilink") [Category:Domain_Name_System](https://ja.wikipedia.org/wiki/Category:Domain_Name_System "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [uceprotect.net](http://www.uceprotect.net/en/index.php?m=2&s=0)
9.  [Verio censored John Gilmore's email under pressure from anti-spammers.](http://www.toad.com/gnu/verio-censorship.html)
10. [Coalition Statement against "stealth blocking"](http://www.peacefire.org/stealth/group-statement.5-17-2001.html) 2001年5月17日
11. [EMarketersAmerica.org sues anti-spam groups](http://www.linxnet.com/misc/spam/slapp.php) 2003年5月7日