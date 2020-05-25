> この記事は[OpenBSD](https://ja.wikipedia.org/wiki/OpenBSD)から翻訳されています。


**OpenBSD**（オープンビーエスディー）は、[オープンソース](../Page/オープンソース.md "wikilink")の[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")。[NetBSD](../Page/NetBSD.md "wikilink") や [FreeBSD](../Page/FreeBSD.md "wikilink") と同じく、[BSDの子孫](../Page/BSDの子孫.md "wikilink")である。[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink") の主要開発者だった[テオ・デ・ラート](../Page/テオ・デ・ラート.md "wikilink") (Theo de Raadt) により 、NetBSD から[分岐する形で開発が始まった](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。

[OpenBSD_hackers_at_c2k++_at_MIT.jpg](https://ja.wikipedia.org/wiki/File:OpenBSD_hackers_at_c2k++_at_MIT.jpg "fig:OpenBSD_hackers_at_c2k++_at_MIT.jpg")で開催されたc2k1の[ハッカソン](https://ja.wikipedia.org/wiki/ハッカソン "wikilink")イベントに参加するOpenBSDの開発者たち\]\]

## 特徴

目標としているのは*正しい思想* (correctness) と*先制的なセキュリティ* (proactive security) である。[オープンソース](../Page/オープンソース.md "wikilink")および[ドキュメンテーション](https://ja.wikipedia.org/wiki/ドキュメンテーション "wikilink")の重視、[ソフトウェアライセンス](../Page/ソフトウェアライセンス.md "wikilink")に妥協しない姿勢でも知られている。テオ・デ・ラートの自宅が[アルバータ州](../Page/アルバータ州.md "wikilink")[カルガリー](../Page/カルガリー.md "wikilink")ということで、[暗号](../Page/暗号.md "wikilink")の輸出制限がない[カナダ](https://ja.wikipedia.org/wiki/カナダ "wikilink")を開発の本拠地としている。ロゴおよびマスコットは[フグ](../Page/フグ.md "wikilink")のPuffy。

OpenBSD の目指す*正しい思想*には、[GPLより制限の少ない](../Page/GNU_General_Public_License.md "wikilink")[BSDライセンス](../Page/BSDライセンス.md "wikilink")こそ真にフリーであるという意見や、正しく設計されたOSは移植が容易であるはずだという理念などが含まれる。もともと NetBSD から派生したため移植性は高いレベルにあったが、新しいプラットフォームへの移植のたびにコードが洗練されセキュリティの向上につながってきたとして、NetBSD とは別の観点から移植の意義を強調している。

また*先制的なセキュリティ*とは、[脆弱性が発見されてから問題を修正するのではなく](https://ja.wikipedia.org/wiki/セキュリティホール#脆弱性 "wikilink")、問題の起こりにくい設計や徹底したコード監査によって、事前にあらゆる危険性を排除しようとすることを意味する。

そのため、通常のインストールではほとんどのサービスが起動しないようになっており、これまでに「デフォルトインストールでのリモート[セキュリティホール](../Page/セキュリティホール.md "wikilink")が2つしか発見されていない」\[1\]ことを売り文句にしている。 その2つとは、[2002年](../Page/2002年.md "wikilink")に発見された [OpenSSH](../Page/OpenSSH.md "wikilink") の桁あふれ問題 \[[http://www.iss.net/threats/advise123.html\]と](http://www.iss.net/threats/advise123.html%5Dと)、[2007年](../Page/2007年.md "wikilink")に発見された [IPv6](https://ja.wikipedia.org/wiki/IPv6 "wikilink") スタックのバッファオーバーフロー\[[http://www.coresecurity.com/?action=item\&id=1703\]である](http://www.coresecurity.com/?action=item&id=1703%5Dである)。

設計や仕様は文書化され、コーディングと同時に[マニュアル](https://ja.wikipedia.org/wiki/UNIXマニュアル "wikilink") (man) が更新されている。実態に即したマニュアルを保証することにより、管理者や開発者の無知・不注意に起因するセキュリティ問題を防止している。

## 成果

他のOSでも標準的に使われている[SSHの代表的実装](../Page/Secure_Shell.md "wikilink")[OpenSSH](../Page/OpenSSH.md "wikilink")の他、[C言語](../Page/C言語.md "wikilink")で文字列を安全に扱うための[strlcpy](https://ja.wikipedia.org/wiki/strlcpy "wikilink")と[strlcat](https://ja.wikipedia.org/wiki/strlcat "wikilink")、IPパケットをフィルタリングする[PF](../Page/PF_\(ファイアウォール\).md "wikilink")（パケットフィルタ）、BSD系OSで暗号化ハードウェアサポートを可能にする[OCF](https://ja.wikipedia.org/wiki/OCF "wikilink") (OpenBSD Cryptographic Framework) などは他の[BSDの子孫](../Page/BSDの子孫.md "wikilink")達にも取り込まれている。

CVS リポジトリを外部に公開したのは OpenBSD が最初だが、その後 anonymous cvs は subversion や git などの普及前の時期においてオープンソースプロジェクトの標準的な開発基盤となっていた。

## 歴史

1994年12月、NetBSD の立ち上げ時のメンバーでもあった[テオ・デ・ラート](../Page/テオ・デ・ラート.md "wikilink")は、上級開発者の地位とNetBSD中核チームメンバーという立場から退くよう要求され、ソースコードへのアクセスもできないようにされた。そうなった経緯は明らかではないが、NetBSDプロジェクトおよび[メーリングリスト](../Page/メーリングリスト.md "wikilink")での性格の不一致が原因と言われている\[2\]。テオはそれまでも周囲と衝突の絶えない性格を批判されていた。Peter Wayner は自著 *Free For All* の中でテオがNetBSDを離脱する直前「何人かの人々の気持ちを逆なでしはじめた」と書いている\[3\]。[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")はテオを「気難しい」と評している\[4\]。あるインタビュアーは彼と会う前に「不安だ」ともらしている\[5\]。しかし、そのように思わない人も多い。件のインタビュアーはテオがOpenBSDを立ち上げる際に「変化」し「チームの面倒を見ることを望んでいる」と述べた。彼が有能な[プログラマ](../Page/プログラマ.md "wikilink")であり\[6\]、セキュリティに関する第一人者の1人\[7\]であることを否定する者はほとんどいない。

[right](https://ja.wikipedia.org/wiki/ファイル:Bsd_distributions_usage.svg "wikilink")。複数回答あり。2005 BSD usage survey\[8\]\]\] 1995年10月、テオは NetBSD 1.0 からのフォークとしてOpenBSDプロジェクトを立ち上げた。最初のリリースは1996年7月の OpenBSD 1.2 であり、同年10月には OpenBSD 2.0 をリリース\[9\]。約半年ごとに新リリースが公開され、各リリースについて1年間サポートと保守を行う。ただし、開発者はシステム全体の整合性を保つ範囲でのみコードに変更を加えなくてはならないため、常時更新されているスナップショット版も安定して動作することが期待されている。[2007年](../Page/2007年.md "wikilink")[11月1日](../Page/11月1日.md "wikilink")に公開された OpenBSD 4.2 は直前に急逝した[萩野純一郎](../Page/萩野純一郎.md "wikilink")に捧げられている[1](ftp://ftp.openbsd.org/pub/OpenBSD/4.2/ANNOUNCEMENT)。

2007年7月25日、OpenBSD開発者 Bob Beck は [OpenBSD Foundation](https://ja.wikipedia.org/wiki/OpenBSD_Foundation "wikilink") の創設を発表した\[10\]。これはカナダの[非営利団体](../Page/非営利団体.md "wikilink")で「個人や法人がOpenBSDをサポートしたい場合に対応する窓口として働く」ものである\[11\]。

OpenBSDがどれほど使われているかは確認が難しい。開発者側でも把握していないし統計も公表していないが、他の情報源が若干存在する。2005年9月、創設間もない BSD Certification Group が利用状況の調査を行い、BSD系OS利用者の32.8%（4330件の回答のうち1420件）がOpenBSDを使っているという結果が得られた\[12\]。同調査では[FreeBSD](../Page/FreeBSD.md "wikilink")は77%、NetBSDは16.3%であり、OpenBSDは2位だった\[13\]。[DistroWatch](https://ja.wikipedia.org/wiki/DistroWatch "wikilink")という[ウェブサイト](../Page/ウェブサイト.md "wikilink")は[Linux](../Page/Linux.md "wikilink")コミュニティではよく知られているが、各[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")と他のOSのサイトのヒット数を公表している。それによると2018年7月22日現在、OpenBSDのサイトには1日146ヒットがあり、79位となっている。ちなみにFreeBSDは1日295ヒットで33位、NetBSDは1日101ヒットで107位である。

2016年9月1日の6.0のリリースに伴い[EFIブートローダーを追加し](../Page/Unified_Extensible_Firmware_Interface.md "wikilink")、[FATまたは](../Page/File_Allocation_Table.md "wikilink")[ext](https://ja.wikipedia.org/wiki/ext "wikilink")ファイルシステムに代わって、[FFSから](../Page/Unix_File_System.md "wikilink")[U-Bootヘッダなしにカーネルを読み込めるようになった](../Page/Das_U-Boot.md "wikilink")\[14\]。

## 「オープン」という姿勢

OpenBSD プロジェクトが生まれた当時は、オープンソースプロジェクトであっても、ソースのリポジトリにアクセスできるのは選ばれた少人数の開発者チームだけというのが普通だった。この方式では、外部のコントリビュータは最新の開発状況を直接知ることができないため、貢献しようとしても作業がダブってしまい無駄になることが多かった。テオ・デ・ラートはソースを誰でもいつでも読めるようにすべきだと考え、Chuck Cranor の支援を求めた\[15\]。Cranor は公開の匿名[CVSサーバを立ち上げた](../Page/Concurrent_Versions_System.md "wikilink")。これはソフトウェア開発の世界で初の試みであり、この決断により *OpenBSD* という名称が生まれ、ソースコードと文書へのアクセスをオープンにするという姿勢を表すようになった。

OpenBSD のオープン性についての方針は、ハードウェアに関しても適用される。テオは2006年12月のプレゼンテーション用スライドで、ハードウェア仕様の詳細を示す文書が公開されていなければ「開発者がドライバを書く際に間違うことが多い」とし、「（やった、動いたぞ、という）快感を味わうことは難しく、開発者によってはあきらめてしまう」と説明している\[16\]。更に、OpenBSD プロジェクトにとってベンダーの提供するバイナリドライバは信用できないし、「問題が生じても…修正する方法がない」ため、許容できないとした。また、ベンダーによるソースは「若干受け入れ可能」だが、依然として問題発生時に修正が困難だとしている。

このような方針を示す出来事として、2005年3月、テオが *openbsd-misc* というメーリングリストにポストしたメッセージ\[17\]を端緒とする議論がある。メッセージの中でテオは、[アダプテック](../Page/アダプテック.md "wikilink")の AAC [RAID](../Page/RAID.md "wikilink") コントローラ用の[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")を改良するために、同社に必要な文書を開示してくれるよう4カ月に渡って交渉してきたが、開示されなかったことを明らかにし、OpenBSD コミュニティ全体に対して、アダプテックに彼らの意見を表明することを奨励した（このような行動はこれ以前にも行われている）。その直後、アダプテック元従業員で FreeBSD 版 AAC RAID サポートの作者でもある FreeBSD の[コミッター](https://ja.wikipedia.org/wiki/コミッター "wikilink") Scott Long\[18\] が、テオがアダプテックとのこの問題について彼に直接コンタクトを取らなかったとして、テオを酷評する文章を [OSNews](https://ja.wikipedia.org/wiki/:en:OSNews "wikilink") というサイトで発表した\[19\]。この件で *freebsd-questions* メーリングリストは議論が紛糾し、そこで OpenBSD プロジェクトのリーダーは Scott Long から支援の申し出は全くなかったし、アダプテックからも Long を紹介されなかったと反論した\[20\]。議論は、[バイナリ・ブロブ](https://ja.wikipedia.org/wiki/バイナリ・ブロブ "wikilink")と[秘密保持契約](https://ja.wikipedia.org/wiki/秘密保持契約 "wikilink") (NDA) の使用を許容するかしないかという2派に分かれての激論に発展した\[21\]。OpenBSD の開発者らは、ソースツリー内に[プロプライエタリなバイナリドライバの存在を許さない立場で](../Page/プロプライエタリ・ソフトウェア.md "wikilink")、NDAにも消極的である。これに対してFreeBSDプロジェクトの方針は異なり、Scott Long がOpenBSDへの支援として提案したアダプテックの RAID 用コードの多くは、クローズドソースか NDA 契約に基づいて書かれている。結局 OpenBSD 3.7 の締め切りまでの文書は提供されず、アダプテックの AAC RAID コントローラサポートは、標準の OpenBSD カーネルからは削除された。

## ライセンス

[thumb](https://ja.wikipedia.org/wiki/ファイル:Openbsd37withjwm.png "wikilink")。[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")は[JWM](https://ja.wikipedia.org/wiki/Jwm "wikilink")\]\] OpenBSDプロジェクトの目標のひとつとして、「元々のバークレー版Unixの[著作権](../Page/著作権.md "wikilink")の精神を保ち」、それによって「相対的に邪魔されることのないUnixソースのディストリビューション」を可能にすることを掲げている\[22\]。このため、[ベルヌ条約によって不要となる言い回しをBSDライセンスから削除して単純化した](../Page/文学的及び美術的著作物の保護に関するベルヌ条約.md "wikilink")[ISCライセンス](https://ja.wikipedia.org/wiki/ISCライセンス "wikilink")を新規コードに適用することを基本としているが、[MITおよび](../Page/MIT_License.md "wikilink")[BSDライセンス](../Page/BSDライセンス.md "wikilink")も許容している。広く使われている [GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") は、それらに比べると制限が厳しすぎると見なされている\[23\]。不適切と見なされたライセンスで提供されているコードは、現在では基本システムには追加しない方針となっている。既存コードでそのようなライセンスで提供されているものは、可能な限り置換したりライセンスを変更しているが、適当な代替物がない場合や新たな開発に時間がかかる場合はそのままとなっている。ライセンス問題から開発したものとして[OpenSSH](../Page/OpenSSH.md "wikilink")がある。元々の [SSHスイートをベースとしてOpenBSDチームが開発したもので](../Page/Secure_Shell.md "wikilink")、、OpenBSD 2.6 で最初に登場し、今では最も広く使われているSSHの実装になっており、様々なOS上で利用可能である。同様なライセンス問題は[IPFilter](https://ja.wikipedia.org/wiki/IPFilter "wikilink")にもあり、その代替物として[PF](../Page/PF_\(ファイアウォール\).md "wikilink")[パケットフィルタを開発した](../Page/ファイアウォール.md "wikilink")\[24\]。OpenBSD 3.0 で最初に登場し、現在では [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")、NetBSD、FreeBSD でも使える。最近ではGPLでライセンスされた [diff](https://ja.wikipedia.org/wiki/diff "wikilink")、[grep](https://ja.wikipedia.org/wiki/grep "wikilink")、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")、[pkg-config](https://ja.wikipedia.org/wiki/pkg-config "wikilink") などのツールをBSDライセンスの代替物で置き換えている。また、新プロジェクトとして[OpenBGPD](https://ja.wikipedia.org/wiki/OpenBGPD "wikilink")、[OpenNTPD](../Page/OpenNTPD.md "wikilink")、OpenOSPFD、OpenSMTPDなども立ち上げている。2007年9月、OpenBSDチームは[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink") (GCC) を置き換える作業に乗りだし、手始めに Anders Magnusson によるBSDライセンスの [Portable C Compiler](../Page/Portable_C_Compiler.md "wikilink") (PCC) を導入した\[25\]。

2001年6月、Darren Reed がライセンスの文言を変えたことで懸念が生じ、OpenBSDの全portsとソースツリーについての体系的なライセンスの監査が行われた\[26\]。システム全体で100以上のファイルのコードについて、ライセンスが不明であるか、ライセンスに反した使い方をしていることが判明した。全てのライセンスを適切に遵守することを保証するため、それぞれの著作権者に連絡をとろうと試みた。結果として一部のコードは削除され、多くは置き換えられた。他に、[ゼロックス](../Page/ゼロックス.md "wikilink")が研究用途にのみライセンスしていた[マルチキャスト](../Page/マルチキャスト.md "wikilink")[ルーティング](../Page/ルーティング.md "wikilink")ツール mrinfo と map-mbone\[27\] などがあったが、ライセンスの変更を著作権者が受け入れたため、そのままOpenBSDで使うことができるようになった。この監査作業で削除されたソフトウェアとして、[ダニエル・バーンスタイン](../Page/ダニエル・バーンスタイン.md "wikilink")の作った全ソフトウェアがある。このときバーンスタインは、彼のコードの修正版を再配布する前に彼の承認を得ることを要求していたが、OpenBSDチームはそのための時間がないとしてその要求を退けたためである\[28\]。これに対して、バーンスタインはいわれなく削除されたとして憤慨した。彼はもっとフリーでないライセンスで提供されている[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")[Netscapeを引き合いに出し](../Page/Netscapeシリーズ.md "wikilink")、彼のソフトウェアを削除しておいてNetscapeをそのままにしておくのは偽善だとOpenBSD開発者らを非難した\[29\]。OpenBSDプロジェクトのスタンスは、Netscapeはオープンソースではないが、そのライセンス条件はプロジェクトの方針に適合しているというものだった\[30\]。彼らは、派生物を制御しようとするバーンスタインの要求を受け入れると多大な労力が付随して必要になるため、削除が最も適切な対応だったとしている。

## セキュリティとコード監査

OpenBSDを始めた直後、テオ・デ・ラートは Secure Networks, Inc. (SNI) というソフトウェア企業からの接触を受けた\[31\]\[32\]。SNIは「ネットワークセキュリティ監査ツール」Ballista（SNIが[マカフィー](../Page/マカフィー.md "wikilink")に買収された後には Cybercop Scanner と改称）を開発しており、それはソフトウェアのセキュリティ上の欠陥を見つけ出し[利用できるか確認するというものだった](https://ja.wikipedia.org/wiki/エクスプロイト "wikilink")。これはテオ自身のセキュリティへの関心と共通していたので、両者は協力することに合意し、その関係は OpenBSD 2.3 のリリースまで続き\[33\]、プロジェクトの方向性に影響を与えた。OpenBSDの開発者は、容易さや性能や機能を犠牲にしてでも、正しく適切でセキュアな方法を選択しようとする。OpenBSDの中のバグは見つかったとしてもセキュリティホールとして利用しづらいものになっていき、SNIはOpenBSDを使った確認が困難になってきた。数年の協力の後、両者は目標としていたレベルに到達したと判断し、協力関係を解消した。

2002年6月まで、OpenBSDは次のようなスローガンをウェブサイトに掲げていた。

2002年6月、[Internet Security Systems](https://ja.wikipedia.org/wiki/:en:IBM_Internet_Security_Systems "wikilink") の Mark Dowd は[チャレンジ-レスポンス型](https://ja.wikipedia.org/wiki/チャレンジ-レスポンス型認証 "wikilink")[認証](../Page/認証.md "wikilink")を実装した[OpenSSH](../Page/OpenSSH.md "wikilink")のコードにバグを見つけた\[34\]。この[セキュリティホール](../Page/セキュリティホール.md "wikilink")は、OpenBSDのデフォルトのインストールでも[利用でき](https://ja.wikipedia.org/wiki/エクスプロイト "wikilink")、攻撃者がリモートからのアクセスで[root特権を得ることができる](../Page/スーパーユーザー.md "wikilink")。これはOpenBSDだけの問題ではなく、当時OpenSSHを利用していた他のOSにとっても大きな問題だった\[35\]。このため、OpenBSDのウェブサイトでもスローガンを次のように変更せざるを得なくなった。

しばらくはこのスローガンで推移したが、2007年3月13日、Core Security Technologies\[36\] の Alfredo Ortega ネットワーク関連の脆弱性を発見した\[37\]。スローガンは次のように変更された。

このスローガンについては、OpenBSDのデフォルトのインストールではほとんど何もできないし、リリースに含まれているソフトウェアには他にもセキュリティホールが見つかったものがあると批判されている。しかしプロジェクト側は、デフォルトのインストールであることを強調しているのだから間違いではないとしている。OpenBSDの基本的考え方として、システムをシンプルでクリーンで [secure by default](https://ja.wikipedia.org/wiki/:en:secure_by_default "wikilink") に保つという方向性がある。例えばOpenBSDの最小のデフォルト構成では、ごく一部のサービスしか有効にしない。このプロジェクトはまた、セキュリティシステムの重要な要素とされているオープンソースとコード監査手法を使っている\[38\]。

[thumb画面](https://ja.wikipedia.org/wiki/ファイル:Openbsd38boot.png "wikilink")。3.8 では *[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")* [関数にセキュリティ上の変更が加えられている](../Page/サブルーチン.md "wikilink")。\]\]

OpenBSDにはセキュリティ強化のための設計変更がいくつも加えられている。例えば、[APIと](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[ツールチェーン](https://ja.wikipedia.org/wiki/ツールチェーン "wikilink")の変更としては、*arc4random*、*issetugid*、*strlcat*、*strlcpy*、*strtonum* といった[関数の修正がある](../Page/サブルーチン.md "wikilink")。他にも[静的境界チェック機構](../Page/静的コード解析.md "wikilink")、不正アクセスからの保護のためのメモリ保護技法として、ProPolice、StackGhost、[W^Xによる](https://ja.wikipedia.org/wiki/NXビット#W^X "wikilink")[ページ保護機能](../Page/ページング方式.md "wikilink")、*[malloc](https://ja.wikipedia.org/wiki/malloc "wikilink")* の修正などがある。また、[暗号](../Page/暗号.md "wikilink")およびランダム化機能として、[プロトコルスタック](../Page/プロトコルスタック.md "wikilink")の強化や[パスワード](../Page/パスワード.md "wikilink")暗号化への[Blowfish](../Page/Blowfish.md "wikilink")暗号の追加などがある。

[特権昇格](https://ja.wikipedia.org/wiki/特権昇格 "wikilink")を可能にするような設定ミスや脆弱性の危険を低減させるため、一部のプログラムでは[特権分離](https://ja.wikipedia.org/wiki/特権分離 "wikilink")、[特権放棄](https://ja.wikipedia.org/wiki/特権放棄 "wikilink")、[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink")の使用といった手法を採用している。このうち特権分離はOpenBSDでいち早く採用した技法で、[最小特権の原則](https://ja.wikipedia.org/wiki/最小特権の原則 "wikilink")に基づいてプログラムを複数の部分に分け、一部にだけ特権の必要な操作を受け持たせて、他の大部分は特権なしで実行するという技法である\[39\]。特権放棄も同様の技法で、必要なときだけ特権を得て操作を行い、その操作が終わったら特権を放棄するという技法である。chrootを使った技法は、アプリケーションが[ファイルシステム](../Page/ファイルシステム.md "wikilink")の一部だけを使って動作するようにし、個人的なファイルやシステムファイルのある部分にアクセスできないようにする。開発者らは一般的なアプリケーションのOpenBSD版にこのような技法を適用しており、例えば [tcpdump](https://ja.wikipedia.org/wiki/tcpdump "wikilink") や [Apache](../Page/Apache_HTTP_Server.md "wikilink") [Webサーバ](../Page/Webサーバ.md "wikilink") などがそうなっている（Apache についてはバージョン2.xではライセンス問題があるため、1.3.29 に巨大な[パッチ](../Page/パッチ.md "wikilink")をあてている）。なお、OpenBSD6.0ではhttpdとしてApacheは実装されなくなり、[nginx](https://ja.wikipedia.org/wiki/nginx "wikilink")が採用された。

プロジェクトは問題に対して継続的にコード監査する方針を採用しており、開発者 Marc Epsie はこの作業を「特定のバグを見つけ出すというよりもプロセス自体への問いかけともいうべきもので…決して終わらない」と評した\[40\]。彼はバグが見つかったときのいくつかの典型的工程を示しているが、その中には、同じまたは類似の問題がないかソースツリー全体を調査すること、「ドキュメンテーションを改正すべきかどうかを見つけ出すこと」、「この問題について警告を表示するよう[コンパイラ](../Page/コンパイラ.md "wikilink")を強化できないか」を調査すること、などが含まれる。標準の[字下げスタイル](../Page/字下げスタイル.md "wikilink")は [Kernel Normal Form](https://ja.wikipedia.org/wiki/字下げスタイル#BSD/KNFスタイル "wikilink") だが、これはコードの保守を容易にするための規定である。そのためコードをOSのベースに組み込む際には必ず守る必要がある。既存のコードもスタイルの要求仕様に合うように適宜書き換えられている。

[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")の創始者である[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")はこれについて、開発というものは大きな問題に対処することに注力すべきで、バグはセキュリティ関連以外にも山ほどあるのだから、セキュリティ問題だけに注力すべきでないと述べている（「全ての平凡なバグは、単にそれらが数が多いというだけでも、より重要である」\[41\]）。2008年7月15日、彼はOpenBSDの方針を批判し「彼らはセキュリティに専念することを大々的に宣言することで、他のことは彼らにとって重要でないと認めているようなものだ」と述べた\[42\]。これに対してOpenBSDの開発者 Marc Espie は「これは全くの誤解だ…（通常のバグ修正は）OpenBSDプロジェクトで人々が常にやっていることそのものだ」と応答した\[43\]。開発者 Artur Grabowski も驚きを表明し「この中で最もおかしな部分は…（トーバルズが）言っていることが我々の言っていることと同じだという点だ」と述べた\[44\]。

## 利用

暗号を組み込み[ファイアウォール](../Page/ファイアウォール.md "wikilink")スイート[PFを備えるといったOpenBSDのセキュリティ強化により](../Page/PF_\(ファイアウォール\).md "wikilink")、セキュリティ関連での利用に適しており、ファイアウォール、[侵入検知システム](../Page/侵入検知システム.md "wikilink")、[VPN](../Page/Virtual_Private_Network.md "wikilink")[ゲートウェイ](https://ja.wikipedia.org/wiki/ゲートウェイ "wikilink")などで特に利用されている。また、[DoS攻撃](../Page/DoS攻撃.md "wikilink")や[クラッキングへの耐性が必要なサーバでもよく使われており](../Page/クラッキング_\(コンピューター用語\).md "wikilink")、[spamd](https://ja.wikipedia.org/wiki/:en:spamd "wikilink")[デーモンが含まれていることから](../Page/デーモン_\(ソフトウェア\).md "wikilink")[電子メールフィルタリング](../Page/電子メールフィルタリング.md "wikilink")用途にも使われることがある。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Openbsd38defaultwm.png "wikilink")。デフォルトの [FVWM](../Page/FVWM.md "wikilink") 2.2.5 [ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")が動作中\]\] [thumb](https://ja.wikipedia.org/wiki/ファイル:Xfce-openbsd.png "wikilink")\]\]

OpenBSDに基づいた[プロプライエタリシステムもいくつかの業者が製品化している](../Page/プロプライエタリ・ソフトウェア.md "wikilink")。例えば、Calyptix Security\[45\]、GeNUA mbH\[46\]、RTMX Inc\[47\]、.vantronix GmbH\[48\]などがある。GeNUAは、i386プラットフォームでの[SMP機能の開発に寄与し](../Page/対称型マルチプロセッシング.md "wikilink")、RTMXはシステムを[POSIX](../Page/POSIX.md "wikilink")準拠に近づけるためのパッチを送り、.vantronix はネットワークや[負荷分散機能の追加に寄与した](../Page/サーバロードバランス.md "wikilink")。OpenBSDのシステムツールのコードの多くは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の [Services for UNIX](../Page/Microsoft_Windows_Services_for_UNIX.md "wikilink") にも使われている（元々は[4.4BSD-LiteをベースとしたUnix系機能を](../Page/BSD.md "wikilink")[Windowsに提供する拡張](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")）。[Core Force](https://ja.wikipedia.org/wiki/:en:Core_Force "wikilink") はWindows向けのセキュリティ製品だが、OpenBSDのPFファイアウォールをベースにしている。[組み込みシステム](../Page/組み込みシステム.md "wikilink")関係でOpenBSDを一部に利用しているプロジェクトとして、OpenSoekris、flashdist、flashrd などがある。

OpenBSDには [X Window System](../Page/X_Window_System.md "wikilink") が含まれている。そのためデスクトップあるいはワークステーションとしても利用でき、様々な[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")や[ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")を利用できる。portsツリーにはデスクトップ用の各種ツールが含まれており、デスクトップ環境としては[GNOME](../Page/GNOME.md "wikilink")、[KDE](../Page/KDE.md "wikilink")、[Xfce](../Page/Xfce.md "wikilink")、ウェブブラウザとしては[Konqueror](../Page/Konqueror.md "wikilink")、[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")、[マルチメディア](../Page/マルチメディア.md "wikilink")関連では[MPlayer](../Page/MPlayer.md "wikilink")、[VLCメディアプレーヤー](../Page/VLCメディアプレーヤー.md "wikilink")、[xine](https://ja.wikipedia.org/wiki/xine "wikilink")などがある。[互換レイヤー](../Page/互換レイヤー.md "wikilink")も利用可能で、Linux、FreeBSD、[SunOS](../Page/SunOS.md "wikilink")、[HP-UX](../Page/HP-UX.md "wikilink") などの他のOS向けにコンパイルされたバイナリを実行できる。

OpenBSDは性能やユーザビリティの面で批判されることがある。Felix von Leitner の性能/[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")のテスト\[49\]によれば、他のOSに比べて性能が低い。これに対してOpenBSD関係者は von Leitner の客観性と技法を批判しつつ、性能は確かに考慮に値するが、セキュリティの良さと正しい設計によって正当化されるとし、開発者 Nick Holland は「それは結局のところ、何を重要と考えるかに帰着する」とコメントした\[50\]。また、OpenBSDはFreeBSDやLinuxに比べるとプロジェクトの規模が小さく、開発者の時間は性能の最適化よりもセキュリティ強化に費やされているように見える。ユーザビリティの批判としては、OpenBSDにはユーザーフレンドリーな設定ツールがない点、デフォルトのインストールがほぼ裸状態である点\[51\]、インストーラが「簡素」で「威嚇的」な点\[52\]を挙げることがある。これに対する反論も性能の場合とほぼ同じで、簡潔性、信頼性、セキュリティを重視した結果だという。あるレビューでは「極めてセキュアなOSを動作させることは、ちょっとした仕事と言えるかもしれない」と評している\[53\]。

## ディストリビューションとマーケティング

OpenBSDは様々な方法で無料で入手可能である。ソースは匿名CVSまたは[CVSup](https://ja.wikipedia.org/wiki/CVSup "wikilink")で入手でき、バイナリ版リリースや開発スナップショットは[FTPまたは](../Page/File_Transfer_Protocol.md "wikilink")[HTTPでダウンロード可能である](../Page/Hypertext_Transfer_Protocol.md "wikilink")。[CD-ROM](../Page/CD-ROM.md "wikilink")のパッケージ版はわずかな代金でオンラインで注文でき、おまけとしてステッカーやリリースのテーマ曲が付いてくる。その収入やアート作品の代価や寄付金でプロジェクトが運営されており、ハードウェアなどのサイト運営費用を賄っている。OpenBSD 4.2 までは、完全版のCD-ROMセットの売り上げを確保するため、小さなインストール用[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")しかダウンロードできないようにしていた。OpenBSD 4.2 から、完全版のISOイメージがダウンロードできるようになった。

他のいくつかのオペレーティングシステムと同様、OpenBSDではプログラムのインストールと管理を容易にするためにportsとパッケージシステムを使っており、それらはOS本体の一部ではない。元々はFreeBSDのportsツリーに基づいていたが、現在のシステムは全く異なる。さらに3.6のリリースで大きな変更が加えられ、特にパッケージツールを Marc Espie が[Perl](../Page/Perl.md "wikilink")で書いた高機能なツールに置き換えた。FreeBSDとは対照的に、OpenBSDのportsシステムは製品版のパッケージを生成することを意図している。portをインストールするとパッケージが生成され、パッケージツールを使ってそれをインストールすることになる。リリースの度にOpenBSDチームがまとめてパッケージを作り、ダウンロード用に提供している。他のBSDの子孫と比較してユニークな点として、portsとOS本体が各バージョンで共に開発されている点が挙げられる。すなわち、例えば3.7でリリースされたportsやパッケージは3.6で使うのには適していない（逆も同様）。このポリシーによって開発プロセスの安定性が確保されているが、OpenBSDの最新リリースのportsにあるソフトウェアは、そのソフトウェアの原作者の最新バージョンより若干遅れることがある。

[thumb](https://ja.wikipedia.org/wiki/ファイル:Puffy.png "wikilink")

OpenBSD 2.7 がリリースされたころ、それまでの[BSDデーモン](../Page/BSDデーモン.md "wikilink")に代わってオリジナルのマスコット Puffy を登場させた。これは[フグ](../Page/フグ.md "wikilink") (pufferfish) とされている。実際のフグの多くはトゲがなく、Puffyの絵はどちらかといえば[ハリセンボン](../Page/ハリセンボン.md "wikilink")に近い。これは、OpenSSHが[Blowfish](../Page/Blowfish.md "wikilink")（フグの意）暗号を使っていることと、ハリセンボンのトゲが外敵を防ぐイメージを表しているという。Puffyは OpenBSD 2.6 で最初に登場し、その後[Tシャツ](../Page/Tシャツ.md "wikilink")や[ポスター](../Page/ポスター.md "wikilink")に様々な姿で登場した。例えば、*Puffiana Jones* は[ハッカー](../Page/ハッカー.md "wikilink")学者にして冒険家であり、Lost RAID を追い求めている。*Puffathy* はアルバータの少女で、[Taiwanと共に冒険する](https://ja.wikipedia.org/wiki/台湾 "wikilink")。*Puff Daddy* は有名なラッパーであり、政治的偶像である。

OpenBSDは、リリースごとに覚えやすいテーマ曲やコミカルなアート作品を生み出してきたことでも有名になった。初期のOpenBSDのリリースには統一感のあるプロモーション用素材はなかったが、OpenBSD 3.0 のCD-ROM版以降、テーマ曲、ポスター、Tシャツなどをリリースごとに統一的に生み出しており、時にはカナダの音楽グループ Plaid Tongued Devils の Ty Semaka が協力している。元々は単にユーモアを加えるだけの軽い意図だったが、コンセプトが成長するに従いそれらがOpenBSDの一部となり、[パロディ](../Page/パロディ.md "wikilink")の形でプロジェクトの理念を表すようになっていった。例えば、OpenBSD 3.8 のテーマは *Hackers of the Lost RAID*、すなわち[インディアナ・ジョーンズ](../Page/インディアナ・ジョーンズ.md "wikilink")のパロディであり、新RAIDツールがリリースに加わったことと連携している。OpenBSD 3.7 のテーマは *The Wizard of OS* で、[ピンク・フロイド](../Page/ピンク・フロイド.md "wikilink")の作品や『[オズの魔法使](https://ja.wikipedia.org/wiki/オズの魔法使 "wikilink")』のパロディであり、[無線通信](../Page/無線通信.md "wikilink")関連のプロジェクトと連携している。OpenBSD 3.3 のテーマ *Puff the Barbarian* は80年代のロックや[英雄コナン](../Page/英雄コナン.md "wikilink")のパロディを含み、オープンドキュメンテーションを示唆している。

リリースごとのTシャツやポスターに書かれたスローガンに加え、プロジェクトは、"Sending [script kiddies](../Page/スクリプトキディ.md "wikilink") to [OpenBSD//dev/null](https://ja.wikipedia.org/wiki/OpenBSD/dev/null "wikilink") since 1995"、"Functional, secure, free  choose 3"、"Secure by default" といった様々な[キャッチフレーズ](https://ja.wikipedia.org/wiki/キャッチフレーズ "wikilink")も生み出し、開発者のみの会合で配布されるTシャツに書かれた内部スローガンとして "World class security for much less than the price of a [cruise missile](../Page/巡航ミサイル.md "wikilink")" とか、"Shut up and hack\!" といった言葉も生み出している。

## 対応プラットフォーム

順番は公式サイトに従う\[54\]。

### 開発中

  - [DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")
  - [amd64](https://ja.wikipedia.org/wiki/x64 "wikilink")
  - [armv7](../Page/ARMアーキテクチャ.md "wikilink")
  - [HPPA](https://ja.wikipedia.org/wiki/HPPA "wikilink")
  - [i386](../Page/Intel_80386.md "wikilink")
  - landisk\[55\]
  - [Loongson](https://ja.wikipedia.org/wiki/Loongson "wikilink")
  - [luna88k](../Page/Luna_\(ワークステーション\).md "wikilink")
  - macppc\[56\]
  - octeon
  - sgi
  - socppc
  - [sparc64](../Page/SPARC.md "wikilink")

### 開発終了

  - [Amiga](../Page/Amiga.md "wikilink")

  - [ARC](https://ja.wikipedia.org/wiki/Advanced_RISC_Computing "wikilink")

  - armish

  -
  - cats

  - [HP300](../Page/HP_9000.md "wikilink")

  - HPPA64

  - mac68k\[57\]

  - [mvme68k](../Page/MC68000.md "wikilink")

  - [mvme88k](../Page/MC88000.md "wikilink")

  - [Palm](../Page/Palm.md "wikilink")

  -
  - pmax

  -
  - [SPARC](../Page/SPARC.md "wikilink")

  - [Sun-3](../Page/Sun-3.md "wikilink")

  - [VAX](../Page/VAX.md "wikilink")

  - [ザウルス](../Page/ザウルス.md "wikilink")

## 脚注

### 注釈

### 出典

## 関連項目

  - [フリーソフトウェアライセンス](https://ja.wikipedia.org/wiki/フリーソフトウェアライセンス "wikilink")
  - [BSDの子孫](../Page/BSDの子孫.md "wikilink")
  - [KAMEプロジェクト](../Page/KAMEプロジェクト.md "wikilink")
  - [LibreSSL](https://ja.wikipedia.org/wiki/LibreSSL "wikilink")
  - [河豚板](https://ja.wikipedia.org/wiki/河豚板 "wikilink")
  - [Bitrig](https://ja.wikipedia.org/wiki/Bitrig "wikilink")

## 参考文献

  - *[The OpenBSD Command-Line Companion, 1st ed.](http://www.devguide.net/books/obclc1)* by Jacek Artymiak. ISBN 83-916651-8-6.
  - *[Building Firewalls with OpenBSD and PF: Second Edition](http://www.devguide.net/books/bfwoap2)* by Jacek Artymiak. ISBN 83-916651-1-9.
  - *[Mastering FreeBSD and OpenBSD Security](http://www.oreilly.com/catalog/mfreeopenbsd/)* by Yanek Korff, Paco Hope and Bruce Potter. ISBN 0-596-00626-8.
  - *[Absolute OpenBSD, Unix for the Practical Paranoid](http://www.nostarch.com/frameset.php?startat=openbsd)* by Michael W. Lucas. ISBN 1-886411-99-9.
  - *[Secure Architectures with OpenBSD](http://cseng.aw.com/catalog/academic/product/0,1144,0321193660,00.html)* by Brandon Palmer and Jose Nazario. ISBN 0-321-19366-0.
  - *[The OpenBSD PF Packet Filter Book: PF for NetBSD, FreeBSD, DragonFly and OpenBSD](http://www.reedmedia.net/books/pf-book/)* published by Reed Media Services. ISBN 0-9790342-0-5.
  - *[Building Linux and OpenBSD Firewalls](http://www.wiley.com/legacy/compbooks/catalog/35366-3.htm)* by Wes Sonnenreich and Tom Yates. ISBN 0-471-35366-3.
  - *[The OpenBSD 4.0 Crash Course](http://www.oreilly.com/catalog/openbsd4/)* by Jem Matzan. ISBN 0-596-51015-2.
  - *[The Book of PF A No-Nonsense Guide to the OpenBSD Firewall](http://nostarch.com/pf.htm)* by Peter N.M. Hansteen ISBN 978-1-59327-165-7.

## 外部リンク

  -
  - [スラッシュドット・ジャパンでの Theo de Raadt へのインタビューの翻訳](https://srad.jp/story/04/01/02/1655202/)

  - [スラッシュドット・ジャパン OpenBSD 10周年 の記事](https://srad.jp/story/05/10/19/1254231/)

  - [OpenBSD journal](http://www.undeadly.org/)

  - [OpenBSD ports](http://ports.openbsd.nu/)

  - [One Floppy OpenBSD MP3 Player and One Floppy Router](http://www.freebsd.nfo.sk/)

[Category:OpenBSD](https://ja.wikipedia.org/wiki/Category:OpenBSD "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")

1.  この数には、[DoS攻撃](../Page/DoS攻撃.md "wikilink")やデフォルトで起動しないデーモンの脆弱性は含まれていない。
2.  Glass, Adam. Message to netbsd-users: *[Theo De Raadt(sic)](http://mail-index.netbsd.org/netbsd-users/1994/12/23/0000.html),* December 23, 1994. Visited January 8, 2006.
3.  Wayner, Peter. *Free For All: How Linux and the Free Software Movement Undercut the High Tech Titans,* [18.3 Flames, Fights, and the Birth of OpenBSD](http://www.jus.uio.no/sisu/free_for_all.peter_wayner/18.html#987), 2000. Visited January 6, 2006.
4.  Forbes. *[Is Linux For Losers?](http://www.forbes.com/intelligentinfrastructure/2005/06/16/linux-bsd-unix-cz_dl_0616theo.html)* June 16, 2005. Visited January 8, 2006.
5.  NewsForge. *[Theo de Raadt gives it all to OpenBSD](http://www.linux.com/archive/articles/7543),* January 30, 2001. Visited January 8, 2006.
6.  In [このメール](http://mail-index.netbsd.org/netbsd-users/1994/12/23/0000.html) でNetBSD中核チームは、テオ自身がどうであれ、彼が多大な貢献をしたことを認めている。
7.  Tux Journal. *[A good morning with: Theo de Raadt（日本語訳）](http://www.unixuser.org/~euske/doc/openssh/theointerview2005.html),* June 2, 2005.（原文） 2009年11月13日閲覧
8.
9.  de Raadt, Theo. Mail to openbsd-announce: *[The OpenBSD 2.0 release](http://www.monkey.org/openbsd/archive2/announce/199610/msg00001.html),* October 18, 1996. Visited December 10, 2005.
10. [Official OpenBSD Foundation site.](http://www.openbsdfoundation.org)
11. Beck, Bob. Mail to openbsd-misc: *[Announcing: The OpenBSD Foundation](http://www.nabble.com/Announcing%3A-The-OpenBSD-Foundation-p11801927.html),* July 25, 2007. Visited July 26, 2007.
12. [The BSD Certification Group.](http://www.bsdcertification.org/); [PDF](../Page/Portable_Document_Format.md "wikilink") of [usage survey results](http://www.bsdcertification.org/downloads/pr_20051031_usage_survey_en_en.pdf).
13. 複数回答が可能なため、複数種類のBSD系OSを使っているユーザーもいる。
14.
15. [Chuck Cranor's site](http://chuck.cranor.org/).
16. de Raadt, Theo. *[Presentation at OpenCON](http://www.openbsd.org/papers/opencon06-docs/index.html),* December 2006. Visited December 7, 2006.
17. de Raadt, Theo. Mail to openbsd-misc: *[Adaptec AAC raid support](http://marc.theaimsgroup.com/?l=openbsd-misc&m=111118558813932),* March 18, 2005. Visited December 9, 2005.
18. [Scott Long's site](http://people.freebsd.org/~scottl/).
19. Long, Scott. Post to OSNews: *[From a BSD and former Adaptec person...](http://osnews.com/comment.php?news_id=10032&offset=15&rows=28#350222),* March 19, 2005. Visited December 9, 2005.
20. de Raadt, Theo. Mail to freebsd-questions: *[aac support](http://lists.freebsd.org/pipermail/freebsd-questions/2005-March/081294.html),* March 19, 2005. Visited December 9, 2005.
21. de Raadt, Theo. Mail to freebsd-questions: *[aac support](http://lists.freebsd.org/pipermail/freebsd-questions/2005-March/081313.html),* March 19, 2005. Visited December 9, 2005.
22. OpenBSD.org. *[Copyright Policy](http://www.openbsd.org/policy.html).* Visited January 7, 2006.
23. Linux.com. *[BSD cognoscenti on Linux](http://www.linux.com/archive/feature/45572),* June 15, 2005. Visited January 7, 2006.
24. Hartmeier, Daniel. [Design and Performance of the OpenBSD Stateful Packet Filter (pf)](http://www.benzedrine.cx/pf-paper.html). Visited December 9, 2005.
25. CVS [log message](http://marc.info/?l=openbsd-cvs&m=118988004013923&w=2) of the import. Visited September 21, 2007.
26. Linux.com. *[OpenBSD and ipfilter still fighting over license disagreement](http://www.linux.com/feature/12774),* June 06, 2001. Visited May 4, 2009.
27. Man pages: [mrinfo](http://www.openbsd.org/cgi-bin/man.cgi?query=mrinfo) and [map-mbone](http://www.openbsd.org/cgi-bin/man.cgi?query=map-mbone).
28. de Raadt, Theo. Mail to openbsd-misc: *[Re: Why were all DJB's ports removed? No more qmail?](http://archives.neohapsis.com/archives/openbsd/2001-08/2544.html),* August 24, 2001. Visited December 9, 2005.
29. Bernstein, DJ. Mail to openbsd-misc: *[Re: Why were all DJB's ports removed? No more qmail?](http://archives.neohapsis.com/archives/openbsd/2001-08/2812.html),* August 27, 2001. Visited December 9, 2005.
30. Espie, Marc. Mail to openbsd-misc: *[Re: Why were all DJB's ports removed? No more qmail?](http://archives.neohapsis.com/archives/openbsd/2001-08/2864.html),* August 28, 2001. Visited December 9, 2005.
31. The Age. *[Staying on the cutting edge](http://www.theage.com.au/articles/2004/10/07/1097089476287.html),* October 8, 2004. Visited January 8, 2006.
32. ONLamp.com. Interview with OpenBSD developers: *[The Essence of OpenBSD](http://www.onlamp.com/pub/a/bsd/2003/07/17/openbsd_core_team.html),* July 17, 2003. Visited December 18, 2005.
33. Theo de Raadt on SNI: "Without their support at the right time, this release probably would not have happened." From the [2.3 release announcement](http://www.monkey.org/openbsd/archive/misc/9805/msg00308.html). Visited December 19, 2005.
34. Internet Security Systems. [OpenSSH Remote Challenge Vulnerability](http://www.iss.net/threats/advise123.html), June 26, 2002. Visited December 17, 2005.
35. [A partial list of affected operating systems](http://xforce.iss.net/xforce/xfdb/9169).
36. [Core Security Technologies' homepage](http://www.coresecurity.com).
37. Core Security Technologies. *[OpenBSD's IPv6 mbufs remote kernel buffer overflow.](http://www.coresecurity.com/content/open-bsd-advisorie)* March 13, 2007. Visited March 13, 2007.
38. Wheeler, David A. Secure Programming for Linux and Unix HOWTO, [2.4. Is Open Source Good for Security?](http://www.dwheeler.com/secure-programs/Secure-Programs-HOWTO/open-source-security.html), March 3, 2003. Visited December 10, 2005.
39. Provos, Niels. [Privilege Separated OpenSSH](http://www.citi.umich.edu/u/provos/ssh/privsep.html). Visited January 30, 2006.
40. O'Reilly Network. *[An Interview with OpenBSD's Marc Espie](http://www.onlamp.com/pub/a/bsd/2004/03/18/marc_espie.html),* March 18, 2004. Visited January 24, 2006.
41. Torvalds, Linus. Mail to linux-kernel: *[Re: \[stable\] Linux 2.6.25.10](http://thread.gmane.org/gmane.linux.kernel/701694/focus=706950)*, July 15, 2008. Visited July 20, 2008.
42.
43. Espie, Marc. Mail to openbsd-misc: *[Re: This is what Linus Torvalds calls openBSD crowd](http://archive.is/20120529013443/kerneltrap.org/mailarchive/openbsd-misc/2008/7/16/2536484)*, July 16, 2008. Visited July 20, 2008.
44. Grabowski, Artur. Mail to openbsd-misc: *[Re: This is what Linus Torvalds calls openBSD crowd](http://archive.is/20120529013443/kerneltrap.org/mailarchive/openbsd-misc/2008/7/17/2545214)*, July 16, 2008. Visited July 20, 2008.
45. [Calyptix Security's website](http://www.calyptix.com/).
46. [GeNUA mbH's homepage](http://www.genua.de/).
47. [RTMX Inc homepage](http://www.rtmx.com/).
48. [.vantronix GmbH's homepage](http://www.vantronix.com/).
49. [Scalability test results and conclusions](http://bulk.fefe.de/scalability/).
50. Holland, Nick. Mail to openbsd-misc: *[Re: OpenBSD Benchmarked... results: poor\!](http://groups.google.co.uk/group/lucky.openbsd.misc/msg/2b6f9d5bf42b712a),* October 19, 2003. Visited January 8, 2006.
51. Linux.com. *[Trying out the new OpenBSD 3.8](http://www.linux.com/archive/feature/49451),* November 2, 2005. Visited January 8, 2006.
52. Linux.com. *[Review: OpenBSD 3.5](http://www.linux.com/archive/feature/37599),* July 22, 2004. Visited January 8, 2006.
53. DistroWatch. *[OpenBSD - For Your Eyes Only](http://distrowatch.com/dwres.php?resource=review-openbsd),* 2004. Visited January 8, 2006.
54. [OpenBSD のサポートするプラットフォーム一覧](http://www.openbsd.org/plat.html)
55. [SH-4を搭載した](../Page/SuperH.md "wikilink")[IO-DATA](https://ja.wikipedia.org/wiki/IO-DATA "wikilink")製NAS
56. [PowerPC](../Page/PowerPC.md "wikilink")を搭載した[Macintosh](../Page/Macintosh.md "wikilink")
57. [MC68000](../Page/MC68000.md "wikilink")を搭載した[Macintosh](../Page/Macintosh.md "wikilink")