> この記事は[WHOIS](https://ja.wikipedia.org/wiki/WHOIS)から翻訳されています。


**WHOIS**（フーイズ）とは、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上での[ドメイン名](../Page/ドメイン名.md "wikilink")・[IPアドレス](../Page/IPアドレス.md "wikilink")・[Autonomous System (AS) 番号の所有者を検索するための](https://ja.wikipedia.org/wiki/自律システム_\(インターネット\) "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")。[データベース](../Page/データベース.md "wikilink")検索を用い、[TCPベースでクエリ](../Page/Transmission_Control_Protocol.md "wikilink")（質問）・レスポンス（応答）を行う。

## 概要

WHOIS検索は、伝統的には[コマンドラインインタフェースで使用されてきた](../Page/キャラクタユーザインタフェース.md "wikilink")。現在では、異なるデータベースを同時に検索するなど、操作を簡略化したウェブベース ([GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")) で利用できるようになっている。

ウェブベースのWHOIS[クライアントはWHOIS](../Page/クライアント_\(コンピュータ\).md "wikilink")[サーバ](../Page/サーバ.md "wikilink")に接続して検索を実行するために、現在もWHOISプロトコルに頼っている。また、コマンドラインWHOISクライアントも、[システム管理者によって今も幅広く使用されている](https://ja.wikipedia.org/wiki/システムアドミニストレータ "wikilink")。

WHOISシステムは、システム管理者が、自分の管理下にないIPアドレスやドメイン名の管理者と連絡をとるための、いわば電話帳のような役割を果たすことを目的として始まった。クエリに対して返ってきたレスポンスデータの使われ方は、利他的な用途（たとえば[電子商取引](../Page/電子商取引.md "wikilink")用[https](../Page/HTTPS.md "wikilink")[認証局](https://ja.wikipedia.org/wiki/認証局 "wikilink")）や邪悪な用途（たとえば大量かつ勝手に送りつけられてくる[電子メール広告](../Page/スパム_\(メール\).md "wikilink")）に対処するために進化してきた。

WHOISには、RWhois と呼ばれる姉妹プロトコル規格が存在する。

## ThinモデルとThickモデル

WHOIS情報を格納する方法は二種類に分類できる。Thinレジストリ、Thickレジストリと呼ばれるが、ここではThinモデルとThickモデルとして解説する。Thickモデルでは、特定のレジストリ情報を1台のサーバに全て登録しておく（たとえば1台のサーバで、すべての.orgドメイン領域のクエリを実行することができる）。Thinモデルでは1台のWHOISサーバに、検索可能な全ての詳細データが登録してあるWHOISサーバ群の名前を登録しておく（たとえば、.comのドメイン情報が登録された WHOISサーバ群にWHOISのクエリを任せる）。（1台のWHOISサーバのみに接続する必要がある場合には）通常はThickモデルの方が一貫したデータとわずかながら速いクエリを確実にする。

もしWHOISクライアントがクエリに対してレスポンスを返せなかった場合、エンドユーザーに対する結果の表示はわずかなものとなる（WHOISサーバの情報と、おそらくは最低限の情報のみ）。WHOISクライアントがレスポンスできる場合、登録者についての詳細な情報が全て表示される。なお、WHOISプロトコルはThinモデルとThickモデルを区別する方法を規格に含んでいない。

登録情報を正確に格納するためには、ドメイン名を管理する[レジストリ組織での変化を記録する必要がある](https://ja.wikipedia.org/wiki/ネットワークインフォメーションセンター "wikilink")。いくつかの[トップレベルドメイン](../Page/トップレベルドメイン.md "wikilink")（.comや.netを含む）は、ThinモデルでWHOISを提供している。いくつかのレジストリ組織では、顧客に対してデータのメンテナンスを提供している。他のレジストラ（.orgを含む）はThickモデルでWHOISを提供している。

なお、日本においては[JPRSが主なドメイン名に関するレジストリ組織となり](../Page/日本レジストリサービス.md "wikilink")、WHOISも提供している。IPアドレスおよびAS番号に関するWHOISは[JPNICが提供している](../Page/日本ネットワークインフォメーションセンター.md "wikilink")。

## クエリの例

wikipedia.orgのWHOISクエリ結果を下記に示す。

`Domain ID:D51687756-LROR`
`Domain Name:WIKIPEDIA.ORG`
`Created On:13-Jan-2001 00:12:14 UTC`
`Last Updated On:02-Dec-2009 20:57:17 UTC`
`Expiration Date:13-Jan-2015 00:12:14 UTC`
`Sponsoring Registrar:GoDaddy.com, Inc. (R91-LROR)`
`Status:CLIENT DELETE PROHIBITED`
`Status:CLIENT RENEW PROHIBITED`
`Status:CLIENT TRANSFER PROHIBITED`
`Status:CLIENT UPDATE PROHIBITED`
`Registrant ID:CR31094073`
`Registrant Name:DNS Admin`
`Registrant Organization:Wikimedia Foundation, Inc.`
`Registrant Street1:149 New Montgomery Street`
`Registrant Street2:Third Floor`
`Registrant Street3:`
`Registrant City:San Francisco`
`Registrant State/Province:California`
`Registrant Postal Code:94105`
`Registrant Country:US`
`Registrant Phone:+1.4158396885`
`Registrant Phone Ext.:`
`Registrant `<FAX:+1.4158820495>
`Registrant FAX Ext.:`
`Registrant Email:dns-admin@wikimedia.org`
`Admin ID:CR31094075`
`Admin Name:DNS Admin`
`Admin Organization:Wikimedia Foundation, Inc.`
`Admin Street1:149 New Montgomery Street`
`Admin Street2:Third Floor`
`Admin Street3:`
`Admin City:San Francisco`
`Admin State/Province:California`
`Admin Postal Code:94105`
`Admin Country:US`
`Admin Phone:+1.4158396885`
`Admin Phone Ext.:`
`Admin `<FAX:+1.4158820495>
`Admin FAX Ext.:`
`Admin Email:dns-admin@wikimedia.org`
`Tech ID:CR31094074`
`Tech Name:DNS Admin`
`Tech Organization:Wikimedia Foundation, Inc.`
`Tech Street1:149 New Montgomery Street`
`Tech Street2:Third Floor`
`Tech Street3:`
`Tech City:San Francisco`
`Tech State/Province:California`
`Tech Postal Code:94105`
`Tech Country:US`
`Tech Phone:+1.4158396885`
`Tech Phone Ext.:`
`Tech `<FAX:+1.4158820495>
`Tech FAX Ext.:`
`Tech Email:dns-admin@wikimedia.org`
`Name Server:NS0.WIKIMEDIA.ORG`
`Name Server:NS1.WIKIMEDIA.ORG`
`Name Server:NS2.WIKIMEDIA.ORG`
`Name Server: `
`Name Server: `
`Name Server: `
`Name Server: `
`Name Server: `
`Name Server: `
`Name Server: `
`Name Server: `
`Name Server: `
`Name Server: `
`DNSSEC:Unsigned`

## 歴史

インターネットが[ARPANET](../Page/ARPANET.md "wikilink")本体から独立した時、全ての登録情報を取り扱った組織は[アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")の下部組織、[国防高等研究計画局](../Page/国防高等研究計画局.md "wikilink")（DARPA）だけであった。登録手続きはRFC 920で確立された。WHOISは1980年代前半、ドメイン検索用に標準化され、ドメイン名や番号とそれに関する人員の登録を始めた。登録組織は一つしかなかったので、WHOISクエリサーバも1台に集中した。このことは、情報の検索を非常に簡単にした。

初期のWHOISサーバは非常に甘い実装で、ワイルドカード検索が可能であった。人名でWHOIS検索ができ、登録されているすべてのドメイン管理者名を得ることができた。任意のキーワードで検索することもでき、そのキーワードを含むすべての情報を得ることもできた。個々の管理者の連絡先が分かるだけでなく、彼らが関係していた全ての領域を見ることができた。インターネットが商用利用されるようになってからは、複数のレジストラと非倫理的なスパム業者のために、このような甘すぎる検索は利用できなくなった。

1980年代、ARPANETがインターネットに移行しつつ消えゆく間、ドメイン登録についての責任はDARPAに残されていた。UUNetはドメイン登録サービスを提供し始めたが、それは単にDARPAのNICに対する登録の代行業務に過ぎなかった。[米国科学財団](https://ja.wikipedia.org/wiki/アメリカ国立科学財団 "wikilink") (NSF) が[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")として、ドメイン名の登録業務を商用向けに開始した。1993年にはNSFと[Network Solutions](../Page/ネットワーク・ソリューションズ.md "wikilink")、General Atomics、[AT\&T](../Page/AT&T.md "wikilink")の契約のもと、InterNICが作られた。General Atomicsの契約は、パフォーマンス問題のために数年後にキャンセルされた。

1999年12月1日、.com・.net・.org の管理は[ICANN](https://ja.wikipedia.org/wiki/ICANN "wikilink")に引き渡され、これらのポピュラーなトップレベルドメイン（以下、TLD）のWHOISサーバはThinモデルに切り替えられた。従来のWHOISクライアントはその時点で使用できなくなった。翌日には[bw-whois](http://whois.bw.org/)がコマンドライン・クライアントとして公開された。1ヶ月後には同じプログラムをもとに、ウェブベースによるWHOIS検索が可能となり、かつ拡張TLDテーブルを管理できるようにした[CGIとなった](../Page/Common_Gateway_Interface.md "wikilink")。これは結局、最新のWHOISクライアントのモデルになった。

現在は、1980年代初頭にあったよりも多くのTLDが生まれ、さらに多数の国名トップレベルドメイン (ccTLD) が存在する。これらはドメイン管理組織やレジストラの関係を複雑にし、特にインターネットの基盤整備については国際化の必要性が出てきた。こういった事情により、WHOISクエリで正しい結果を得るには、どのWHOISサーバがレジストリを管理しているのかを知っている必要がある。WHOIS検索を横断的に行うツールとして、コマンドラインWHOISクライアント jwhois はドメイン名／ネットワークブロックとレジストリ組織のひも付けを登録・編集できるコンフィギュレーション・ファイルを備えている。

2004年、[IETF委員会は](../Page/Internet_Engineering_Task_Force.md "wikilink")、ドメイン名とネットワーク番号に関する全く新しい検索情報の規格化策定に着手した。提案されたこの新規格の仮称は[CRISP](http://www.ietf.org/html.charters/crisp-charter.html) (Cross Registry Information Service Protocol) という。

## WHOISサーバへのクエリ

### コマンドライン・クライアント

初期のWHOISサーバへのアクセス方法は、コマンドラインのみであった。ほとんどの場合、[UNIX](../Page/UNIX.md "wikilink")またはUNIX系のOS上で動作した。WHOISクライアント・ソフトは、開発当初から現在に至るまで[オープンソース](../Page/オープンソース.md "wikilink")で供給されている。商業ベースのUNIXでは、独自のWHOISクライアントが実装されている（たとえば、[SunのSolaris](../Page/サン・マイクロシステムズ.md "wikilink") には、Sunが開発したWHOISクライアントが含まれている）。

一般的なWHOISコマンドライン・クライアントは、WHOISクエリのため、どのサーバに接続するかをオプションで選ぶことができ、[デフォルトでどのサーバに接続するかを変更するには](../Page/デフォルト_\(コンピュータ\).md "wikilink")、[再コンパイルで対処することになる](../Page/コンパイラ.md "wikilink")。さらに別オプションとして、どの[ポートで接続するか](../Page/ポート_\(コンピュータネットワーク\).md "wikilink")、[デバッグ用データを表示するかどうか](../Page/バグ.md "wikilink")、再帰的照会をするかしないかといったものがある。

大部分の[TCP/IP](../Page/インターネット・プロトコル・スイート.md "wikilink")[クライアント・サーバアプリケーションと同様](../Page/サーバ.md "wikilink")、WHOISクライアントはユーザーの入力を待ち、接続先サーバにIPソケットを開ける。WHOISプロトコルは適当なポートでクエリを送り、応答を待つ。そして、応答をユーザーに表示して終了するか、さらに入力を待つ。WHOISプロトコルに関する詳細な情報は[RFCで見つけることができる](../Page/Request_for_Comments.md "wikilink")。

[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の jwhoisクライアントは、他の多くのWHOISクライアントとは違い、WHOISクエリの照会先を登録できるコンフィギュレーション・ファイルを持っている。この仕組みにより、参照／再帰的照会ロジックをソースコード外に出し、かつインターネット・インフラの変更にも素早く追従できるという特色を持った。

### グラフィカル・クライアント

WHOISサーバから来るデータのすべてがテキストである上に、プロトコルは静的なものであることから、「グラフィカル」という項目は誤解を招くかもしれない。WHOISサーバにはインタラクティブという言葉は当てはまらない。この節において「グラフィカル・クライアント」とは、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) を備えたOS上で動作するWHOISクライアントを指す。

Windowsで動作するポピュラーかつフリーなWHOISクライアントは、[Sam-Spade package](http://www.samspade.org/ssw/)の一部であって、「ホットリンク」が作られるようになっている（たとえば、WHOISクエリの結果の一部をクリックすることで、新しいクエリを実行することができる）。

もう一つのポピュラーなWindows用WHOISクライアントは Active Whois である。このツールはWHOISクエリと、WHOISホスト検索のための[DNS検索ロジックを組み合わせたもので](../Page/Domain_Name_System.md "wikilink")、ThickモデルとThinモデルの両方に対応している。Sam-Spade同様、クエリ結果をホットリンクとして出力する。

### ウェブベース・クライアント

[World Wide Webの急速な発展による](../Page/World_Wide_Web.md "wikilink")、ウェブ上での情報の一般化、特にネットワーク・ソリューション寡占の緩みに伴い、ウェブ経由でのWHOISクエリは一般的になりつつある。もっとも初期のウェブベースWHOISクライアントは、単にインタフェースをウェブとしただけの、コマンドラインWHOISクライアントに対するフロントエンドに過ぎず、必要に応じて出力結果を整形するか消去するのみであった。

現状では、直接WHOISクエリを入力し、表示のために整形された結果が得られるものが一般的である。多くはレジストラによって提供されている。しかし、オープンソース・クライアントも存在する。例えば[GeekTools](http://www.geektools.com/tools.php)、[Whois Proxy](http://wp-whois-proxy.sourceforge.net/)など。

ウェブベース・クライアントの必要性は、コマンドラインWHOISクライアントが当初UNIX（系）と[大型機にしかなく](https://ja.wikipedia.org/wiki/汎用コンピュータ "wikilink")、Windowsや[Macintosh](../Page/Macintosh.md "wikilink")はWHOISクライアントを備えていなかったため、レジストラは潜在的顧客のためにWHOISデータベースへのアクセス手段を見つけなければならなかった。専用アプリケーションとしてのWHOISクライアントツールが各OSに現存する今でも、多くのエンドユーザーはウェブベースのWHOISを利用している。

### Perl モジュール

WHOISサーバとともに、[Perl](../Page/Perl.md "wikilink")で作られた[WHOISクライアント](https://metacpan.org/search?q=whois)が存在する。これらの多くは、現在のWHOISサーバに対する全機能を備えている訳ではない。または、あまり流通していない。しかし、AS番号や登録者情報の検索には大いに役に立つ。

## 問題点

[thumb](https://ja.wikipedia.org/wiki/画像:Captcha.jpg "wikilink")

  - **[プライバシー](../Page/プライバシー.md "wikilink")**

<!-- end list -->

  -
    例示したように、登録者の個人情報が含まれており、大部分のTLDではインターネット上で誰でも簡単にその情報を入手することができる。
    上記のクエリ結果の例でいえば、「Registant」の項目に登録者の住所・氏名・電話番号などの個人情報が含まれており、これが中小企業や大企業であれば問題にならないが、個人が運営するドメインで個人情報が知られるのは問題となる。
    しばしば、一部のレジストラが連絡のための個人情報を提供するが、これはレジストラがそのドメインの合法的な所有者（または借り主）であることを示すためだ。しかし、それらの情報も本来の特定のドメイン所有者が誰であるかの情報を提供するという目的を超えて、誰がどのドメインを持っているかを調べたり、ANSI（合資会社アスカネットワーク）のように氏名で検索した場合に検索エンジンにWHOISの結果が表示されるような仕様にして自社でWHOISサーバを提供しているレジストラまで出現している。
    プライバシーに敏感な利用者は偽の個人情報で登録したり、代理業者の名義で登録するなど本来のWHOISの役割を果たさなくなってきているケースも出てきた。

<!-- end list -->

  - **[スパムメール](../Page/スパム_\(メール\).md "wikilink")**

<!-- end list -->

  -
    しばしばスパム送信者（スパマー）がWHOISクエリから[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")で[電子メール](../Page/電子メール.md "wikilink")情報を収集する。WHOIS検索を提供している[レジストラ](https://ja.wikipedia.org/wiki/レジストラ "wikilink")の一部は、対策として[CAPTCHA](../Page/CAPTCHA.md "wikilink")を利用し、画像に描いてある文字列を入力しないとクエリができないようにしている。

<!-- end list -->

  - **国際化**

<!-- end list -->

  -
    WHOISプロトコルは国際化の方針については規定していなかった。WHOISサーバは、受け入れたテキストの[文字コード](../Page/文字コード.md "wikilink")を判別することができない。そして、WHOISサーバのすべては単に[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")文字のみを使っている。しかし、これは国際的な運用には使うことができない。特に、多言語化されたドメイン名が広く使われ始めており、このことは明らかにWHOISプロトコルのアクセシビリティを英語圏内に限定してしまう。ユーザは（条件付きで）[Punycode](../Page/Punycode.md "wikilink")を使うことができるが、通常のユーザがこれを使いこなすことは簡単ではない。

<!-- end list -->

  - **WHOISサーバリストの不足**

<!-- end list -->

  -
    WHOISには（DNSのような）中央サーバがない。このため、WHOISツールの作成者は、自分自身でWHOISサーバのリストを作らなければならない。そして、異なるサーバリストを書いている他のユーザを見つける可能性がある。数少ないWHOISサーバリストのソースは、[このページ](http://www.dnsstuff.com/tools/whois.ch?domain=list)で見つけることができる。

<!-- end list -->

  - **フォーマットの不徹底**

<!-- end list -->

  -
    レジストラやサーバによって、WHOISクエリに対する応答のフォーマットが異なることがある。このことは、WHOISデータの解析を難しくする。しかし、このことへの対処の自動化は、合法的な用途（ISPによるものなど）もあるが、スパマーへの手助けとなるかもしれない。

## 関連項目

  - [トップレベルドメイン](../Page/トップレベルドメイン.md "wikilink")
  - [:en:Domain name registry](https://ja.wikipedia.org/wiki/:en:Domain_name_registry "wikilink")
  - [:en:RPSL](https://ja.wikipedia.org/wiki/:en:RPSL "wikilink")
  - [IPひろば](https://ja.wikipedia.org/wiki/IPひろば "wikilink")
  - [Asia-Pacific Network Information Centre](https://ja.wikipedia.org/wiki/Asia-Pacific_Network_Information_Centre "wikilink")

## 外部リンク

  - [JPNIC Whois Gateway](https://www.nic.ad.jp/ja/whois/ja-gateway.html)
  - [JP WHOIS -JPRS](https://whois.jprs.jp/)
  - [IP Location Finder](https://tools.keycdn.com/geo)
  - [MxToolbox](https://mxtoolbox.com/ReverseLookup.aspx)
  - [IPひろば](https://www.iphiroba.jp/)
  - [WHOIS Search for Domain Registration Information](https://www.networksolutions.com/whois/)
  - [Go Daddy - Search the WhoIs database](https://jp.godaddy.com/whois)
  - [SRSPlus.com](https://www.srsplus.com/domains/whois.aspx)
  - [WHOIS-IPWHOIS Lookup](https://www.dnsstuff.com/)

### RFC

  - RFC 812 - NICNAME/WHOIS（1982年, 廃止）
  - RFC 954 - NICNAME/WHOIS（1985年, 廃止）
  - RFC 3912 - WHOIS protocol specification（2004年, 現行）

[Category:アプリケーション層プロトコル](https://ja.wikipedia.org/wiki/Category:アプリケーション層プロトコル "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")