> この記事は[Microsoft ](https://ja.wikipedia.org/wiki/Microsoft_)から翻訳されています。


**Microsoft アカウント**（マイクロソフトアカウント、以前は **Microsoft Wallet**\[1\]、**Microsoft Passport**\[2\]、**.NET Passport**、**Microsoft Passport Network**、**Windows Live ID**）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発し提供する[シングルサインオン](../Page/シングルサインオン.md "wikilink")Webサービスである。Microsoft アカウントにより、ユーザーは1つのアカウントで複数の[ウェブサイト](../Page/ウェブサイト.md "wikilink")へログインすることが可能となる。

## 概要

Microsoft アカウントによりユーザーは、複数の証明書を一まとまりとしたものを利用するサービスをサポートするウェブサイトにサインインすることが可能となる。ユーザーの証明書をチェックするのはMicrosoft アカウントが利用可能なウェブサイトではなく、Microsoft アカウント認証サーバである。Microsoft アカウントが利用可能なウェブサイトにサインインする新規ユーザーは、まず最初に最も近くにある認証サーバにリダイレクトされ、認証サーバはユーザー名とパスワードを[SSLを通じて尋ねる](../Page/Transport_Layer_Security.md "wikilink")。ユーザーは自身のコンピュータに自分のログイン情報を覚えさせるよう選択することも可能である。新たにサインインしたユーザーは、自身のコンピュータ内に保存される暗号化された制限時間付きの[cookieを持ち](../Page/HTTP_cookie.md "wikilink")、認証サーバとMicrosoft アカウントが利用可能なウェブサイト間で承認済みの、[トリプルDES](../Page/トリプルDES.md "wikilink")で暗号化されたIDタグを受け取る。それからこのIDタグは、ユーザーのコンピュータに別の暗号化されたcookieをもたらすウェブサイトへと送られる。またこのIDタグも制限時間付である。これらのcookieが有効である限り、ユーザーはユーザ―名とパスワードを要求されない。ユーザーが自発的にMicrosoft アカウントからログアウトした場合、これらのcookieは削除される。

Microsoft アカウントは、ユーザーに2つの異なるアカウント作成方法を示す：

1.  **電子メールアドレスを利用する方法 :** ユーザーはMicrosoft アカウントと契約するために自身が持つ正規の電子[メールアドレス](https://ja.wikipedia.org/wiki/メールアドレス "wikilink")を使うことができる。そのサービスにより要求するユーザーの電子メールアドレスをMicrosoft アカウントにする。ユーザーは自身で選択したパスワードを選ぶことができる。
2.  **マイクロソフト電子メールアドレスと契約する方法 :** ユーザーは、他のMicrosoft アカウントが利用可能なウェブサイトにサインインするために、Microsoft アカウントとして利用可能なドメイン（すなわち@hotmail.com、@live.com、@msn.com、@passport.comそして@outlook.comあるいは国ごとにそれらを変更したもの）で指定されたマイクロソフトの[Webメール](https://ja.wikipedia.org/wiki/Webメール "wikilink")（[Outlook.com](https://ja.wikipedia.org/wiki/Outlook.com "wikilink")や[Hotmail](https://ja.wikipedia.org/wiki/Hotmail "wikilink")など）サービスを用いた電子メールアカウントで契約することもできる。

[Windows Live](https://ja.wikipedia.org/wiki/Windows_Live "wikilink")、[MSN](../Page/MSN.md "wikilink")、[Xbox Live](https://ja.wikipedia.org/wiki/Xbox_Live "wikilink")、[Zune](https://ja.wikipedia.org/wiki/Zune "wikilink")、[Windows Phone](https://ja.wikipedia.org/wiki/Windows_Phone "wikilink")、そして[Windows 8といったマイクロソフトのサイト](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、サービス、そしてプロパティは、ユーザー確認のためにMicrosoft アカウントを使用する。NineMSNがホストするHoytsウェブサイトのように、それを使用する他の会社もある。

[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink")、および[Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、[Windows 7では](../Page/Microsoft_Windows_7.md "wikilink")、Windows ユーザーアカウントとMicrosoft アカウントとを結びつけるためのオプションがある。そうするとユーザーがサービスにアクセスする度に自動的にMicrosoft アカウントでログインする。一方、[Windows 8](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")、および[Windows 8.1](https://ja.wikipedia.org/wiki/Microsoft_Windows_8.1 "wikilink")、[Windows 10では](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")、ローカルやドメインユーザーよりもむしろMicrosoft アカウントを利用することで、ユーザーが自身のPCに直接認証することが可能となる。

### Web認証

[2007年](../Page/2007年.md "wikilink")[8月15日](../Page/8月15日.md "wikilink")、マイクロソフトは、Webデベロッパーが、Windows Live IDと、[ASP.NET](https://ja.wikipedia.org/wiki/ASP.NET "wikilink") ([C\#](../Page/C_Sharp.md "wikilink"))、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Perl](../Page/Perl.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Python](../Page/Python.md "wikilink")そして[Ruby](../Page/Ruby.md "wikilink")が含まれたWebサーバプラットフォームの幅広い範囲で起動しているWebデベロッパーのウェブサイトとを統合することを可能とするための**Windows Live ID Web Authentication SDK**をリリースした。\[3\]\[4\]

### Windows CardSpaceのサポート

Windows Live ID ログインページは、ユーザー名とパスワードの組み合わせの代わりに[Windows CardSpaceを使用したサインインを提出する](https://ja.wikipedia.org/wiki/Windows_CardSpace "wikilink")。Windows Live ID アカウントの所有者は、自身のWindows Live IDとリンクするために、Windows CardSpaceセレクタUIからインフォメーション カードを選択することで、（[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 3.0および3.5のコンポーネントである）Windows CardSpaceに集約することが可能である。\[5\]

### OpenIDのサポート

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[10月27日](../Page/10月27日.md "wikilink")、マイクロソフトは、Windows Live IDが[OpenID](../Page/OpenID.md "wikilink")プロバイダになることで、OpenIDフレームワークをサポートすることを公に委託されたことを公表した。\[6\][2009年](../Page/2009年.md "wikilink")[8月](../Page/8月.md "wikilink")以降、マイクロソフトのOpenIDの実装のアップデートはなくなった。\[7\]

## 特徴

Microsoft アカウントは、ユーザーが自身のアイデンティティを管理するためのウェブサイトである。Microsoft アカウントの特徴を以下に示す:

  - 苗字、名前、住所といったユーザーの情報をアップデートし、アカウントに関連付けられる。
  - お好みの言語やお好みの電子メールコミュニケーションのような、ユーザー設定をアップデートできる。
  - パスワードを変更したり再設定したりできる。
  - アカウントを停止できる。
  - アカウントに関連付けられた請求書の詳細を見ることができる。
  - 複数のMicrosoft アカウントを同時にリンクできる。

## セキュリティ脆弱性

[2007年](../Page/2007年.md "wikilink")[6月17日](../Page/6月17日.md "wikilink")、[オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")のウェブ開発者であるErik Duindamが、「マイクロソフトのプログラマーが任意の電子メールアドレス用のIDの作成を許可することにより、致命的なエラーが発生する」と発言し、プライバシーおよびアイデンティティリスクを報告した\[8\]。その後、不正な、または既に存在する電子メールアドレスを登録することを許してしまう不具合が発見された。マイクロソフトでは、電子メールアドレスを登録する際、正当なアドレスであるかを確認するための電子メールをユーザーに送信している。ユーザーは、その電子メールに記載されたリンクをクリックして正当な電子メールアドレスの所有者であることを証明する。しかしながら、それを利用する前に、ユーザーが自分に割り当てられた電子メールアドレスを存在しない電子メールアドレスや他人の電子メールアドレスに変更することを許してしまっていた。この問題は、2日後の2007年[6月19日](../Page/6月19日.md "wikilink")に修正された。\[9\]

[2012年](../Page/2012年.md "wikilink")[4月20日](https://ja.wikipedia.org/wiki/4月20日 "wikilink")、マイクロソフトは、Hotmailアカウントをリセットすることを許可するシステムの問題点を修正した。同日、マイクロソフトにはVulnerability Labの研究員よりこの問題が知らされており\[10\]、この問題は数時間で修正された。しかし、その問題が修正されたころにはこの脆弱性を用いた大規模な攻撃が行われていた\[11\]\[12\]。

## 歴史

Windows Live IDの前身であるMicrosoft Passportは元々、全てのWebコマース用のシングルサインオンサービスとして位置付けられた。Microsoft Passportは多数の批判を受けた。Laws of Identityの著者である批評家のKim Cameronは、Microsoft Passportが法律違反ではないかと疑問を持った。彼はそれ以降マイクロソフトのチーフアイデンティティアーキテクトとなり、Windows Live IDアイデンティティメタシステムの設計の違反に対処した。その結果として、Windows Live IDは全てのWebコマース用のシングルサインオンサービスとしてではなく、多くのアイデンティティシステムの中の一つとして位置付けられた。

[1999年](../Page/1999年.md "wikilink")[12月](https://ja.wikipedia.org/wiki/12月 "wikilink")、マイクロソフトは「passport.com」の年次のドメイン登録料35ドルを[ネットワーク・ソリューションズ](../Page/ネットワーク・ソリューションズ.md "wikilink")に支払うことを怠った。その怠りにより、passport.comを認証用サイトとして利用している[Hotmail](https://ja.wikipedia.org/wiki/Hotmail "wikilink")は同年[12月24日](../Page/12月24日.md "wikilink")に利用不可能となった。[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")コンサルタントのMichael Chaneyが、ダウンしたサイトのこの問題を解決することを望んだため、翌日にそれを支払った。その支払により、翌朝そのサイトを利用できるようになった\[13\]。[2003年](../Page/2003年.md "wikilink")の[秋](../Page/秋.md "wikilink")、マイクロソフトが "hotmail.co.uk" の支払いをミスした際、ダウンした時間が生じなかったものの、類似の[善きサマリア人のたとえ](https://ja.wikipedia.org/wiki/善きサマリア人のたとえ "wikilink")によりマイクロソフトは助かった\[14\]。

[2001年](../Page/2001年.md "wikilink")に、[電子フロンティア財団](https://ja.wikipedia.org/wiki/電子フロンティア財団 "wikilink")のスタッフ代理人であるDeborah Pierceが、Microsoft Passportによりマイクロソフトが顧客情報の完全なアクセスおよび利用を行えることを暴露した後で、Microsoft Passportが潜在的脅威であるとして批難した\[15\]。顧客の不安を和らげるため、プライバシーの規約はすぐにマイクロソフトにより更新された。

[2001年](../Page/2001年.md "wikilink")の[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")、[電子プライバシー情報センター](https://ja.wikipedia.org/wiki/電子プライバシー情報センター "wikilink")と14の大手消費者集団が、Microsoft Passportシステムは、商取引において不公平または欺瞞的な実行を禁ずる[Federal Trade Commission Act (FTCA)の](https://ja.wikipedia.org/wiki/:en:Federal_Trade_Commission_Act "wikilink")5章に違反していると断言している[:en:Federal Trade Commissionと共に](https://ja.wikipedia.org/wiki/:en:Federal_Trade_Commission "wikilink")[抗議](http://www.epic.org/privacy/consumer/MS_complaint.pdf)を提出した。 [2003年](../Page/2003年.md "wikilink")、イギリスのITセキュリティエキスパートであるFaisal Danka\[16\]は、Microsoft PassportまたはHotmailにリンクしたアカウントが一般的なブラウザを使うことで容易に行えるクラックを通して、Microsoft Passportに欠点がいくつかあることを明らかにした。

マイクロソフトはマイクロソフトではないエンティティがインターネットワイドな統一ログインを作成することを推し進めてきた。Microsoft Passportを使用したサイトの例としては、[eBay](https://ja.wikipedia.org/wiki/eBay "wikilink")や[:en:Monster.com](https://ja.wikipedia.org/wiki/:en:Monster.com "wikilink")がある。しかし[2004年](../Page/2004年.md "wikilink")にそれらの協約はキャンセルされた\[17\]。[2009年](../Page/2009年.md "wikilink")[8月](../Page/8月.md "wikilink")、ExpediaはもうMicrosoft Passport / Windows Live IDをサポートしないことを公表した。

[2012年](../Page/2012年.md "wikilink")、Windows Live IDはその名をMicrosoft アカウントへと変更された\[18\]\[19\]。

## 関連項目

  - [アイデンティティ管理](../Page/アイデンティティ管理.md "wikilink")
  - [:en:Identity management system](https://ja.wikipedia.org/wiki/:en:Identity_management_system "wikilink")
  - [シングルサインオン](../Page/シングルサインオン.md "wikilink")
  - [:en:List of single sign-on implementations](https://ja.wikipedia.org/wiki/:en:List_of_single_sign-on_implementations "wikilink")

<!-- end list -->

  - 他のアイデンティティサービス

<!-- end list -->

  - [:en:Active Directory Federation Services](https://ja.wikipedia.org/wiki/:en:Active_Directory_Federation_Services "wikilink")
  - [OpenID](../Page/OpenID.md "wikilink")
  - [:en:Light-Weight Identity](https://ja.wikipedia.org/wiki/:en:Light-Weight_Identity "wikilink")
  - [:en:Yadis](https://ja.wikipedia.org/wiki/:en:Yadis "wikilink")
  - [Windows CardSpace](https://ja.wikipedia.org/wiki/Windows_CardSpace "wikilink")

<!-- end list -->

  - アイデンティティ管理

<!-- end list -->

  - [:en:Liberty Alliance](https://ja.wikipedia.org/wiki/:en:Liberty_Alliance "wikilink")
  - [OASIS](https://ja.wikipedia.org/wiki/OASIS_\(組織\) "wikilink")

## 脚注

## 参考文献

  - [Microsoft アカウントに新規登録するにはどうすればよいですか?](http://www.microsoft.com/ja-jp/msaccount/signup/default.aspx)
  - [Introduction to Windows Live ID whitepaper](http://msdn2.microsoft.com/en-us/library/bb288408.aspx) ? Provides a brief overview of the Windows Live ID service in the context of Microsoft's overall identity strategy.
  - [Understanding Windows Live Delegated Authentication whitepaper](http://msdn2.microsoft.com/en-us/library/cc287613.aspx) ? Describes how a Web site can use the Windows Live ID Delegated Authentication system to get permission to access users' information on Windows Live services.
  - [Windows Live ID Federation whitepaper](http://msdn2.microsoft.com/en-us/library/cc287610.aspx) ? Describes the concept of identity federation and offers considerable detail about how the Windows Live ID service supports it.

## 外部リンク

  - [Microsoft アカウント](https://account.microsoft.com/)

[Category:Windows_Live](https://ja.wikipedia.org/wiki/Category:Windows_Live "wikilink")

1.
2.  [Microsoft Passport: Streamlining Commerce and Communication on the Web](http://www.microsoft.com/presspass/features/1999/10-11passport.mspx)
3.  LiveSide.net: [Windows Live ID Web Authentication Is Final](http://www.liveside.net/developer/archive/2007/08/16/windows-live-id-web-authentication-is-final.aspx) 2007-07-16
4.  Live ID Team blog announcement: [Windows Live ID Web Authentication SDK for Developers Is Released](http://winliveid.spaces.live.com/blog/cns!AEE1BB0D86E23AAC!908.entry) 2007-07-15
5.  LiveSide.net: [CardSpace (InfoCard) and Live ID](http://www.liveside.net/blogs/main/archive/2007/07/02/cardspace-infocard-and-live-id.aspx) 2007-07-02
6.  [Windows Live ID Becomes an OpenID Provider](http://dev.live.com/blogs/devlive/archive/2008/10/27/421.aspx)
7.  [Windows Live ID OpenID Status Update](http://blogs.technet.com/b/privacyimperative/archive/2009/08/28/windows-live-id-openid-status-update.aspx)
8.  ["Windows Live ID security breached" on erikduindam.com](http://www.erikduindam.com/windowslive.pdf)
9.  [Microsoft Windows Live Flaw Opened Door to Scammers](http://pcworld.about.com/od/instantmessaging1/Microsoft-Windows-Live-Flaw-Op.htm)
10. [Microsoft MSN Hotmail - Password Reset & Setup Vulnerability](http://www.vulnerability-lab.com/get_content.php?id=529)
11. [Twitter / @msftsecresponse: On Friday we addressed a reset function incident to help protect Hotmail customers, no action needed](https://twitter.com/msftsecresponse/status/195568235654021121)
12.
13.
14.
15. [Privacy terms revised for Microsoft Passport](http://archive.is/20120629091209/http://news.com.com/Privacy+terms+revised+for+Microsoft+Passport/2100-1023_3-255310.html?tag=bplst)
16. [Faisal Danka](http://faisaldanka.wordpress.com)
17. [Microsoft Passport Dumped By Ebay](http://www.searchenginejournal.com/microsoft-passport-dumped-by-ebay/1203/)
18. [Windows 8 Consumer Preview - FAQ](http://windows.microsoft.com/en-US/windows-8/faq)
19.