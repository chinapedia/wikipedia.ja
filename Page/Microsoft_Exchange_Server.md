> この記事は[Microsoft Exchange Server](https://ja.wikipedia.org/wiki/Microsoft_Exchange_Server)から翻訳されています。


**Microsoft Exchange Server （マイクロソフト エクスチェンジ サーバー）** は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の開発した[グループウェア](../Page/グループウェア.md "wikilink") / [電子メール](../Page/電子メール.md "wikilink")製品。[Microsoft Serversの一部であり](../Page/Microsoft_Servers.md "wikilink")、マイクロソフト製品を採用している企業で広く使われている。Exchangeの主な機能は、電子メール / 予定表 / 連絡先などの共有と携帯機器やウェブからの情報アクセスサポート、さらにデータ格納サポートである。

## 歴史

マイクロソフトが従来の[XENIX](../Page/XENIX.md "wikilink")ベースのメッセージングシステムからExchange Serverへの移行を開始したのは[1993年](../Page/1993年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")であり\[1\]、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")[1月](https://ja.wikipedia.org/wiki/1月 "wikilink")には約500ユーザーが **Exchange Server Beta 1** を使用していた。[1996年](../Page/1996年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")までに 32,000 ユーザーが移行した。

1996年[6月11日](../Page/6月11日.md "wikilink")にリリースされた**Exchange Server 4.0**が社外に販売するようになった最初のバージョンであり、**Microsoft Mail 3.5**の後継とされた。ただし、Exchange Serverは全く新しい[X.400](../Page/X.400.md "wikilink")ベースの[クライアントサーバ型メールシステムであり](../Page/クライアントサーバモデル.md "wikilink")、単一の[データベース](../Page/データベース.md "wikilink")と[X.500](../Page/X.500.md "wikilink")ディレクトリサービスをサポートしていた。Exchange Serverで使われていたディレクトリは後に[Active Directoryという](../Page/Active_Directory.md "wikilink")[LDAP準拠ディレクトリサーバとなった](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")。Active Directoryは[Windows 2000に導入された](../Page/Microsoft_Windows_2000.md "wikilink")。

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[5月23日](../Page/5月23日.md "wikilink")、**Exchange Server 5.0**がリリースされた。Exchange Administrator コンソールが新たに導入され、[SMTPベースのネットワークとの連携を初めて実現した](../Page/Simple_Mail_Transfer_Protocol.md "wikilink")。SMTPリレーが別途必要だったMicrosoft Mailとは異なり、Exchange Server 5.0はInternet Mail Connectorというアドインを使って、直接SMTPベースのサーバと通信可能であった。また、Exchange Web Accessという[Webメール](../Page/Webメール.md "wikilink")インタフェースも新たに導入された。ただし、これは後にOutlook Web Accessと改称し、サービスパックに入れられた。5.0に対応して、その新機能をサポートした[Microsoft Outlook](../Page/Microsoft_Outlook.md "wikilink") 8.01、Microsoft Exchange Client 5.0、Microsoft Schedule+ 7.5がリリースされた。

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[11月](../Page/11月.md "wikilink")、**Exchange Server 5.5**がリリースされた。スタンダード・エディションとエンタープライズ・エディションがある。これらは、データベースの大きさ、メール転送機能、クラスタリング機能などで差がある。スタンダード・エディションは従来版と同じ16GBというデータベースの制限があるが、エンタープライズ・エディションではこれが8TBに拡張されていた（ただし、マイクロソフトは100GBを越えた構成を推奨していない）。スタンダード・エディションには、Site Connector、MS Mail Connector、Internet Mail Service（Internet Mail Connector から改称）、Internet News Service（Internet News Connector から改称）、[cc:Mail](https://ja.wikipedia.org/wiki/cc:Mail "wikilink") / [Lotus Notes](https://ja.wikipedia.org/wiki/Lotus_Notes "wikilink") / [Novell GroupWiseといったソフトウェアとの連携機能がある](../Page/Novell_GroupWise.md "wikilink")。エンタープライズ・エディションにはさらに、[X.400](../Page/X.400.md "wikilink") Connector、[IBM](../Page/IBM.md "wikilink")のSNADSやPROFSとの連携機能がある。エンタープライズ・エディションには2ノードの[クラスタリング機能が導入された](../Page/コンピュータ・クラスター.md "wikilink")。その他の新機能として、予定表をサポートした[Outlook Web Access](../Page/Outlook_Web_Access.md "wikilink")、[IMAP4と](../Page/Internet_Message_Access_Protocol.md "wikilink")[LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink") v3クライアントのサポート、削除されたアイテムの復旧機能がある。このバージョンまで、Exchange Serverには内蔵のディレクトリとSMTP / NNTPサービスが含まれていた。Outlook 8.03が対応するクライアントとしてリリースされたが、Exchange ClientとSchedule+は対応バージョンがリリースされなかった。

[2000年](../Page/2000年.md "wikilink")[11月29日](../Page/11月29日.md "wikilink")にリリースされた**Exchange Server 2000**（開発コード名 Platinum）では、様々な制限が解除された。例えば、データベースのサイズ制限が緩和され、クラスタは2ノードから4ノードに拡張された。しかし、Active Directoryが必須となったためにアップグレードできない顧客が続出した。つまり、以前はディレクトリサービスを内蔵していたのだが、2000 ではActive Directoryなしでは機能しなくなったのである。Exchange Server 5.5から移行する場合、5.5の動作するシステムと2000をインストールするサーバは別に必要であり、そうしないとディレクトリの内容を変換できない。[インスタントメッセージ](../Page/インスタントメッセージ.md "wikilink")のサポートも追加されたが、後に[Microsoft Office Live Communications Serverとして分離されている](https://ja.wikipedia.org/wiki/Microsoft_Office_Live_Communications_Server "wikilink")。**Exchange Server 2003**（開発コード名 Titanium）で従来版からの移行がかなり容易になった。このため、Exchange Server 5.5のユーザーは2003のリリースを待ったところが多い。また、アップグレードするには、サーバのOSを[Windows 2000にする必要があった](../Page/Microsoft_Windows_2000.md "wikilink")。顧客によっては、マイクロソフトのサポートが得られないExchange Server 5.5と[Windows NT 4.0の組合せに留まる選択をしたところもある](../Page/Microsoft_Windows_NT.md "wikilink")。この製品発表会では、アクティブ/アクティブ型のクラスタ対応を宣伝するため、黒山羊と白山羊を模した自動メール発信を動作させておき、障害が発生しても問題が発生しないことをアピールしようとした。このパフォーマンス中、サーバの電源を引き抜き、障害を発生させたが、送信メール数と受信メール数が合わず、エラーにもならず、メールをロストしてしまったという、失態を演じた。\[2\]

## Exchange Server 2003

[2003年](../Page/2003年.md "wikilink")[9月28日](../Page/9月28日.md "wikilink")リリース。Windows 2000 Server（ただし、SP4）と、32ビットの[Windows Server 2003で動作するが](../Page/Microsoft_Windows_Server_2003.md "wikilink")、前者では新機能の一部が機能しない。各種[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")を備えており、ユーザーが徐々に移行できるようにしている。これは、多数のExchange Serverを稼動させていて、移行のためにサービスを停止できない企業などで重宝された。

Exchange Server 2003の新機能の一つとして、ダウン時の復旧を高速化した点が挙げられる。これは、メッセージストアがバックアップから復旧される前から新規メールのやり取りを可能としたものである。Mobile Information Server 2001 / 2002の機能の一部もExchange Serverに取り入れられた。例えば、Outlook Mobile Accessや[ActiveSyncのサーバ側などである](../Page/Microsoft_ActiveSync.md "wikilink")（Mobile Information Server はその後開発中止となった）。ウイルスおよびスパム対策も強化され\[3\]、フィルタリングソフト向けのAPIの追加、[SPFおよび](https://ja.wikipedia.org/wiki/センダー・ポリシー・フレームワーク "wikilink")[DNSBL](../Page/DNSBL.md "wikilink")\[4\]フィルタリングの基本部分の組み込みがなされている。メッセージ / メールボックス管理ツールも強化され、管理者の作業時間短縮に寄与している。[インスタントメッセージ](../Page/インスタントメッセージ.md "wikilink")と Exchange Conferencing Serverは[Live Communication Server](https://ja.wikipedia.org/wiki/Live_Communication_Server "wikilink")（現在は[Microsoft Office Communications Serverに改名](https://ja.wikipedia.org/wiki/Microsoft_Office_Communications_Server "wikilink")）に分離され別製品となったため、完全に除かれた。マイクロソフトはグループウェアとしての機能を、[Microsoft Office](../Page/Microsoft_Office.md "wikilink")、[Microsoft Office Live Communications Server](https://ja.wikipedia.org/wiki/Microsoft_Office_Live_Communications_Server "wikilink")、[Microsoft Live Meeting](https://ja.wikipedia.org/wiki/Microsoft_Live_Meeting "wikilink")、[Microsoft Office SharePoint Server](https://ja.wikipedia.org/wiki/Microsoft_Office_SharePoint_Server "wikilink") の組合せで実現するという方向となっている。このため、Exchange Serverは、電子メールと予定表だけを分担するようになっている。

Exchange Server 2003には、スタンダード・エディションとエンタープライズ・エディションがある。スタンダード・エディションはサーバ毎に1つのメッセージ・データベースをサポートし、データベースは最大16GBである。SP2では最大75GBに拡張されたが、デフォルトは18GBとなっており、それ以上に設定するには[レジストリ](../Page/レジストリ.md "wikilink")を編集する必要がある\[5\]。エンタープライズ・エディションでは最大 16TB であり、最大5つのデータベースからなるストレージグループをサーバ内に最大4つ持つことができる（合計で20個のデータベース）\[6\]。

Windows Small Business Server 2003にはExchange Server 2003も含まれるが、32ビット版だけであり、64ビット版では動作しない。

Exchange Serverの使う[RPCプロトコルは独自のもので](../Page/遠隔手続き呼出し.md "wikilink")、[APIしか公開されていない](../Page/アプリケーションプログラミングインタフェース.md "wikilink") ([MAPI](../Page/Messaging_Application_Programming_Interface.md "wikilink"))。これは、[Microsoft Outlookクライアントで使うべく設計された](../Page/Microsoft_Outlook.md "wikilink")。Exchange Server上の電子メールは[POP3と](../Page/Post_Office_Protocol.md "wikilink")[IMAP4でアクセスでき](../Page/Internet_Message_Access_Protocol.md "wikilink")、[Mozilla Thunderbirdや](../Page/Mozilla_Thunderbird.md "wikilink")[Lotus Notesといったクライアントでも使える](https://ja.wikipedia.org/wiki/Lotus_Notes "wikilink")。Outlookと[EvolutionはExchange](../Page/Evolution_\(ソフトウェア\).md "wikilink") Server特有の機能にも対応したクライアントである。[Macintosh](../Page/Macintosh.md "wikilink")用の[Microsoft Entourageも最新版ではExchange](https://ja.wikipedia.org/wiki/Microsoft_Entourage "wikilink") Server特有の機能の大部分をサポートしている。ウェブブラウザからメールボックスにアクセスすることもでき、これを[Outlook Web Access](../Page/Outlook_Web_Access.md "wikilink") (OWA) と呼ぶ。また、Exchange Server 2003はモバイル版OWA (Outlook Mobile Access, OMA) もサポートしている。

[Windows Mobile](../Page/Windows_Mobile.md "wikilink") 5.0 AKU2以降では、Exchange Server 2003 SP2と組み合わせて、[プッシュ型電子メール](../Page/プッシュ型電子メール.md "wikilink")をサポートしている\[7\]\[8\]。

## Exchange Server 2007

[2006年](../Page/2006年.md "wikilink")[12月7日](../Page/12月7日.md "wikilink")リリース。Exchange Server 2003以降、マイクロソフトの方向性は不明だった。[2005年](../Page/2005年.md "wikilink")に何らかの改良がリリースされる予定が立てられたが、中止されている。Exchange Server 2007がリリースされたのは2006年末であった。ボイスメールとの連携、ウェブサービス検索強化、フィルタリング強化、新たな[Outlook Web Accessインタフェースなどが含まれる](../Page/Outlook_Web_Access.md "wikilink")。

64ビットの[x64](https://ja.wikipedia.org/wiki/x64 "wikilink")版のWindows Serverでのみ動作する。サポートは得られないが、32ビットの試用版がダウンロード可能となっている。32ビットのハードウェアでExchange Serverを使っている顧客は、ハードウェアの置換が必要となるし、64ビットのハードウェアを使っている顧客でも、OSを64ビット版にしないと移行できない。

ベータ版は2005年12月にリリースされたが、ベータテストを行ったサイトはごく少ない。広範囲に配布されるベータ版は（開発チームのブログによれば）2006年3月に公開された。2006年4月25日、マイクロソフトはExchange Serverの次期バージョンが**Exchange Server 2007**となることを発表した。

[2009年](../Page/2009年.md "wikilink")1月、Exchange Server 2007 のセキュリティソリューションとしてマイクロソフトが起案・監修した[メール情報セキュリティ強化パック](https://ja.wikipedia.org/wiki/メール情報セキュリティ強化パック "wikilink")がリリースされ、開発した[ソフトバンク・テクノロジー](https://ja.wikipedia.org/wiki/ソフトバンク・テクノロジー "wikilink")のWebサイトから無償提供される。

### 主な強化点

マイクロソフトによれば、強化点は以下の通り\[9\]。

  - 保護機能: アンチスパム、アンチウイルス、法令順守、クラスタリングによるデータ複製、セキュリティと暗号の強化
  - アクセスの強化: 予定表強化、統合メッセージング、モバイル対応強化、ウェブアクセス強化
  - IT効率強化: 64ビット化によるスケーラビリティと性能、コマンドシェルと単純な[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、展開強化、役割分離、ルーティングの単純化
  - Exchange Management Shell: 管理者向けの新たな[コマンド行](../Page/キャラクタユーザインタフェース.md "wikilink")[シェル](../Page/シェル.md "wikilink")と[スクリプト言語](../Page/スクリプト言語.md "wikilink")（[Windows PowerShellベース](https://ja.wikipedia.org/wiki/Windows_PowerShell "wikilink")）。GUIでできることは全て実行可能であり、日々の作業でよく実施するものをスクリプト化することが可能。375種のコマンドを備えている\[10\]。
  - 統合メッセージング: ボイスメール、電子メール、ファックスを統合的に利用可能。また、メールボックスに携帯機器や電話からアクセス可能。
  - データベースサイズの制限を解除。ハードウェアおよびOSの限界までの大きさのデータベースを利用可能。
  - サーバ毎のストレージグループ数とデータベース数を拡大。スタンダード・エディションでは5個まで、エンタープライズ・エディションでは50個まで。
  - Outlook 2007との組み合わせにより階層型アドレス帳機能をサポート。

## Exchange Server 2010

2009年[11月2日](../Page/11月2日.md "wikilink")リリース。ベータ版は2009年4月にリリースされた。マイクロソフトが推進する[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")である、[ソフトウェア プラス サービス](https://ja.wikipedia.org/wiki/ソフトウェア_プラス_サービス "wikilink") (S+S) に対応した最初のリリース。マルチテナント型で提供される[クラウドコンピューティング](https://ja.wikipedia.org/wiki/クラウドコンピューティング "wikilink")サービスである[Microsoft Exchange Onlineを意識したつくりになっている](https://ja.wikipedia.org/wiki/Microsoft_Exchange_Online "wikilink")。

### 主な強化点

  - [Outlook Web Appの機能向上](https://ja.wikipedia.org/wiki/Outlook_Web_App "wikilink"): リッチクライアントであるOutlookとの使い勝手の差がより小さくなった。複数の人の予定を一画面で表示させることも可能になった。
  - トランスポート保護ルール: メール送信時に、特定の条件に当たる場合は、自動的に[Information Rights Management](https://ja.wikipedia.org/wiki/Information_Rights_Management "wikilink") (IRM) 保護を適用することが可能。
  - 個人用アーカイブ機能: 従来はPSTファイルとしてローカルに保存していた過去のメールをサーバー上に保存する機能が実装された。
  - マルチメールボックス検索: 管理者が複数のメールボックスを検索することが可能。
  - メールヒント: [Outlook Web AppやOutlook](https://ja.wikipedia.org/wiki/Outlook_Web_App "wikilink") 2010でメールを編集している場合、メールの送信時に、組織外部のメールアドレスが含まれていたり、配布リストに多人数のメールアドレスが含まれていたり、という特定の条件に当たる場合は、警告メッセージを表示する。

## クラスタリングと高可用性

エンタープライズ・エディションは、Windows 2000 Serverでは4ノードまでのクラスタ、Windows Server 2003では8ノードまでのクラスタをサポートしている。Exchange Server 2003はアクティブ/アクティブ型クラスタも導入しているが、その場合は2ノードクラスタのみである。アクティブ / アクティブ型では、同時に両方のサーバが利用できる。より一般的なアクティブ/パッシブ型は、クラスタ内に現用系の[フェイルオーバー](https://ja.wikipedia.org/wiki/フェイルオーバー "wikilink")のための待機系が存在する。待機系は現用系で障害が発生するときのために待機状態にある。アクティブ / アクティブ型については性能問題があることがわかり、マイクロソフトも現在では利用を推奨していない\[11\]。実際、Exchange Server 2007 では、アクティブ / アクティブ型クラスタはサポートされていない。

Exchangeのクラスタリングは、同じ物理データのノード間での共有方法が問題視されてきた。クラスタリングによってExchange Serverは「アプリケーション」として多重化されるが、「データ」は多重化されない\[12\]。この場合、データが「[単一故障点](https://ja.wikipedia.org/wiki/単一故障点 "wikilink")」となるが、マイクロソフトはこれを "Shared Nothing" と説明している\[13\]。ただし、この隙間をISVやストレージ企業が様々な手法で埋めてきた\[14\]。Exchange Server 2007 では、新たなクラスタリング構成を導入し、従来の "shared data model" の問題点に対処している\[15\]。

Exchange Server 2007では、[SQL Serverの](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")"Log Shipping"\[16\]に基づいた非同期[レプリケーション](../Page/レプリケーション.md "wikilink")を、CCR（クラスタ連続レプリケーション）\[17\]として組み込みでサポートしている。これは、MSCS MNS(Microsoft Cluster Service - Major Node Set) を使ったもので、共有ストレージを必要としない。このようなクラスタは安価に構成でき、遠隔のデータセンタ間でクラスタを構成可能で、サイト全体の災害などにも対応できる。CCRクラスタは、2ノードでのみ構成可能で、追加のファイル共有証人としての "voter node" が第三のノードとして追加可能である\[18\]。voter nodeは[スプリットブレインシンドローム](../Page/スプリットブレインシンドローム.md "wikilink")を防ぐもので、一般にHub Transport Server上でファイル共有する\[19\]。

第二のクラスタ形態は、以前のバージョンから可能だったもので、現在はSCC（シングルコピークラスタ）と呼ばれている。Exchange Server 2007では、CCRもSCCも展開が簡略化され、Exchange Serverのインストール時にクラスタとしての構成が可能である。LCR（ローカル連続レプリケーション）\[20\] は "poor man's cluster"（貧者のクラスタ）とも呼ばれる。これは、データのレプリケーションを同じサーバ上の別の装置に行うもので、ストレージの故障に対応できる。しかし、サーバそのものが故障した場合には対応できない。

2007年11月、マイクロソフトはExchange Server 2007のSP1をリリースした。このサービスパックには新たな高可用機能 SCR（スタンバイ連続レプリケーション）が含まれている。CCRでは両サーバがWindowsクラスタに属していなければならなかったが、SCRではクラスタ化されていないサーバにレプリケーション可能であり、遠隔地のデータセンタへのレプリケーションが容易である。

## 関連項目

  - [Microsoft Servers](../Page/Microsoft_Servers.md "wikilink")
  - [Microsoft Office Communications Server](https://ja.wikipedia.org/wiki/Microsoft_Office_Communications_Server "wikilink")
  - [Microsoft Exchange Online](https://ja.wikipedia.org/wiki/Microsoft_Exchange_Online "wikilink")

## 脚注

## 参考文献

  - ["Active Directory LDAP Compliance"](http://www.microsoft.com/windowsserver2003/techinfo/overview/ldapcomp.mspx) Microsoft Corporation, 2003年12月2日。2005年11月2日閲覧。

  -
  -
  -
## 外部リンク

  - [Exchange Server マイクロソフト 公式技術情報](http://technet.microsoft.com/ja-jp/exchange)
  - [Exchange ブログ JAPAN](http://blogs.technet.com/exchangeteamjp/)

[Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink") [Category:グループウェア](https://ja.wikipedia.org/wiki/Category:グループウェア "wikilink") [Category:メール転送エージェント](https://ja.wikipedia.org/wiki/Category:メール転送エージェント "wikilink") [Category:1993年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1993年のソフトウェア "wikilink")

1.
2.  2000年9月8日 東京国際フォーラム Bホール Microsoft Exchange 2000 Server Airlift において
3.
4.
5.
6.
7.
8.
9.  [Microsoft Exchange Server Website](http://www.microsoft.com/exchange/)
10. [Exchange 2007 Cmdlet List](http://technet.microsoft.com/en-us/library/bb123703.aspx)
11.  （ログインが必要）
12.
13.
14.
15.
16.
17.
18.
19.
20.