> この記事は[Drupal](https://ja.wikipedia.org/wiki/Drupal)から翻訳されています。


**Drupal**（ドルーパル、）は、[プログラム言語](https://ja.wikipedia.org/wiki/プログラム言語 "wikilink")[PHPで記述された](../Page/PHP_\(プログラミング言語\).md "wikilink")[フリーでオープンソースのモジュラー式](https://ja.wikipedia.org/wiki/FLOSS "wikilink")[フレームワークであり](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")、[コンテンツ管理システム](https://ja.wikipedia.org/wiki/コンテンツ管理システム "wikilink") (CMS) である。昨今の多くのCMSと同様に、Drupalは[システム管理者](https://ja.wikipedia.org/wiki/システム管理者 "wikilink")に[コンテンツ](../Page/コンテンツ.md "wikilink")の作成と整理、提示方法のカスタマイズ、管理作業の自動化、[ウェブサイト](../Page/ウェブサイト.md "wikilink")への訪問者や寄稿者の管理を可能にする。

その性能がコンテンツ管理から、幅広い[サービス](../Page/サービス.md "wikilink")や商取引を可能にするにまで及ぶことから、Drupalは時々「[ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/ウェブアプリケーションフレームワーク "wikilink")」であると評される。Drupalは洗練された[プログラミングインタフェースを提供するものの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、基本的なウェブサイトの設置と管理は[プログラミング](../Page/プログラミング.md "wikilink")なしに成し遂げることができる。Drupalは一般に、最も優れたWeb 2.0フレームワークの一つであると考えられている\[1\]。

Drupalは[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink") 10、 [OpenSolaris](https://ja.wikipedia.org/wiki/OpenSolaris "wikilink")を始め、[Webサーバ](../Page/Webサーバ.md "wikilink")[Apache](../Page/Apache_HTTP_Server.md "wikilink")（1.3以上）または[IIS](../Page/Internet_Information_Services.md "wikilink")（IIS5以上）、及びPHP（4.3.3以上）をサポートするあらゆる環境で動作する。Drupalはコンテンツや設定を格納するために、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、[SQLite](https://ja.wikipedia.org/wiki/SQLite "wikilink")、[MongoDB](https://ja.wikipedia.org/wiki/MongoDB "wikilink")のような[データベース管理システム](../Page/データベース管理システム.md "wikilink")を必要とする。

## 歴史

DrupalはもともとDries Buytaertが[BBSシステムとして書いたもので](../Page/電子掲示板.md "wikilink")、[2001年](../Page/2001年.md "wikilink")に[オープンソース](../Page/オープンソース.md "wikilink")・プロジェクトとなった。*Drupal*の綴りは、"drop" [滴](https://ja.wikipedia.org/wiki/滴 "wikilink")）を意味する[オランダ語](../Page/オランダ語.md "wikilink")の単語 "Druppel" を、英語に[翻字](https://ja.wikipedia.org/wiki/翻字 "wikilink")したものである。この名称は、現在は閉鎖されたウェブサイトDrop.orgから取られたもので、ここで使われていたコードがゆっくりとDrupalに発展した。Buytaertはこのサイトを "dorp"（そのコミュニティの様相を指す「村」のオランダ語）と呼びたかったが、ドメイン名をチェックするときにタイプミスをし、それがより良いと考え "drop" を採用した\[2\]。

2006年5月から2007年4月まで、Drupalは公式サイトから600,000回以上ダウンロードされた\[3\]。現在では大きなコミュニティがDrupalの開発を支えている\[4\]。

[2020年](../Page/2020年.md "wikilink")2月時点ではDrupal 8.8.2が最新のリリース版である\[5\]。

## Drupalコア

"Drupal core" として知られるDrupalの公式リリースは、ほとんどのCMSに共通する基本的な機能を備えている。これらには個々のユーザ・アカウントの登録と維持、管理メニュー、[RSS](../Page/RSS.md "wikilink")フィード、カスタマイズ可能なレイアウト、柔軟なアカウント権限、ログ機能、[ブログ](../Page/ブログ.md "wikilink")作成システム、フォーラムなどを含み、典型的な企業サイト（*[brochureware](https://ja.wikipedia.org/wiki/:en:Brochureware "wikilink")*）でも、インタラクティブなコミュニティサイトでも構築することができる。

ウェブサイトのコンテンツは、管理者の裁量で登録・匿名ユーザが寄稿することができ、様々な基準（日付、カテゴリー、検索など）で訪問者に対してアクセスさせることができる。Drupalコアはさらに、[コンテンツ](../Page/コンテンツ.md "wikilink")の分類や、アクセスしやすいキーワードで「タグ付け」することができる、階層的なタクソノミー ([taxonomy](https://ja.wikipedia.org/wiki/:en:Taxonomy "wikilink")) システムを備えている。

Drupalはバージョン単位のコア機能のアップデートについて、詳細なチェンジログを保持している\[6\]。

### コア・モジュール

Drupalコアはさらに、コアのみで作成したウェブサイトの標準の機能性を、管理者が拡張することのできる「コア・モジュール」を備えている。

コアのDrupalディストリビューションは、以下を含む多くの機能を提供している。

  - 複数ユーザによるコンテンツの作成・編集
  - 高度な検索機能
  - コメント、フォーラム、投票
  - ユーザ・プロフィール
  - 多層式のメニュー・システム
  - RSSフィードとフィード・アグリゲーター
  - 様々なアクセス・コントロール制限（ユーザロール、IPアドレス、電子メール）
  - アクセス統計とログ記録
  - 高負荷状態でのパフォーマンスを向上させるキャッシュと機能調整機能（スロットル）
  - 説明的なURL（例えば "www.example.com/?q=node/432" ではなく "www.example.com/products" のようなもの）
  - ワークフロー・ツール（「トリガ」と「アクション」）
  - セキュリティ・リリースや新機能リリースのアップデート通知
  - [OpenID](../Page/OpenID.md "wikilink")のサポート

### コア・テーマ

[thumb](https://ja.wikipedia.org/wiki/ファイル:Drupal.jpg "wikilink") Drupalコアは審美的な[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")をカスタマイズできる、いくつかの「コア・テーマ」を備え、管理者はこれらの[テーマを専用メニューから選ぶことができる](https://ja.wikipedia.org/wiki/スキン_\(GUI\) "wikilink")。

Drupalコア5.0から導入された "Color" モジュールは、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の[インタフェースを通じて特定テーマの配色を変更できるようにする](../Page/インタフェース_\(情報技術\).md "wikilink")。この機能は[プログラミングの知識を持たない普通のユーザでも](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、より高度なカスタマイズができるように追加された。

### 翻訳

2008年2月の時点で、Drupalインタフェース用の[翻訳](../Page/翻訳.md "wikilink")はデフォルトの[英語](../Page/英語.md "wikilink")に加え、44カ国語が利用可能となっている\[7\]。いくつかの言語は右から左へと読まれる（例えばアラビア語やヘブライ語）。Drupal 6は多言語におけるコンテンツおよびコンテンツ管理に対し、より一層のサポートを提供する。

### 自動アップデート通知

バージョン6.0から、寄贈されたモジュールやテーマ、あるいはDrupalコア自体の新しいバージョンが利用可能になるとき、Drupalは自動的に管理者へ通知できるようになった。これはインストール済みのDrupalを、最新の機能やセキュリティ修正で最新式の状態に保つのを補助する機能である。

コア・リリースには含まれていないが、バージョン5.x用にも同等の機能を提供するモジュールがある。

## Drupalコアの拡張

Drupalコアは、[APIを通じて内部的にアクセスされる](../Page/アプリケーションプログラミングインタフェース.md "wikilink")「[フック](https://ja.wikipedia.org/wiki/フック "wikilink")」と「[コールバック](https://ja.wikipedia.org/wiki/コールバック "wikilink")」システムを備えた、モジュール式であるように設計されている。\[8\]。この設計は、[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")による「寄贈された」（しばしば "contrib" と省略される）[モジュール](https://ja.wikipedia.org/wiki/モジュール "wikilink")やテーマが、Drupalコアのコードを変更せずにDrupalのデフォルト動作を拡張したり、置き換えられるようにする。

コントリビュート・モジュールやテーマからDrupalコアのファイルを隔離するDrupalのモジュラー式設計は、柔軟性と安全性を増大し、Drupalの管理者がサイトのカスタマイズを上書きすることなく、Drupalコアの新しいリリースにきれいにアップグレードできるようにする。この分離を維持するため、Drupalの管理者はDrupalコアのソフトウェアを変更することは避けるよう指示されている。

### コントリビュート・モジュール

Drupalのコントリビュート・モジュールは、イメージ・ギャラリー、カスタムのコンテンツ・タイプやコンテンツ・リスト、[WYSIWYG](../Page/WYSIWYG.md "wikilink")エディタ、[プライベート・メッセージング](https://ja.wikipedia.org/wiki/プライベート・メッセージング "wikilink")、サードパーティー統合ツール等々、様々な機能を提供する。Drupalウェブサイトには、Drupalのコミュニティによって開発・寄贈された2147\[9\]（2008年6月1日現在）のフリーなモジュールがリストされている。

典型的なDrupalの設置では、以下の2つのモジュールが特に重要となる：。

  - **Content Construction Kit (CCK)**\[10\] は、サイト管理者が動的にコンテンツ・タイプを作成することを可能にする。コンテンツ・タイプは、ウェブサイトのデータベースに格納されるあらゆる種類の情報を表現する。これらにはイベント、招待状、レビュー、記事、製品などが挙げられるが、これらに限定されるものではない。
  - **Views**\[11\] は、サイト訪問者へのコンテンツの検索と提示を容易にする。

CCK [APIはDrupal](../Page/アプリケーションプログラミングインタフェース.md "wikilink") 7からコア・モジュールとしてDrupalへの統合が予定されており、Views（[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")以外の部分）もその後のある時点で統合されようとしている。\[12\]

### コントリビュート・テーマ

コントリビュート・テーマは、Drupalで構築されたサイトのデフォルトの[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")の適応や交換を行う。

Drupalのテーマは、一般的なサードパーティー製テーマデザイン・エンジンによってもたらされる、標準フォーマットを使用する。多くのDrupal用テーマは、[PHPTemplate](https://ja.wikipedia.org/wiki/PHPTemplate "wikilink")エンジン\[13\]や、それほどでもないが[XTemplate](https://ja.wikipedia.org/wiki/XTemplate "wikilink")エンジン\[14\]で書かれている。いくつかのテンプレートではハードコードされたPHPを使用する。

Drupalのテーマ・システムの初期バージョンは、[Mambo](https://ja.wikipedia.org/wiki/Mambo "wikilink")や[Joomla\!](https://ja.wikipedia.org/wiki/Joomla! "wikilink")、あるいは[Plone](https://ja.wikipedia.org/wiki/Plone "wikilink")のテーマ・システムより設計指向型でなく、より複雑であるために批判\[15\]されたが、PHPTemplateとXTemplateエンジンのDrupalへの統合ではこれらの懸案事項のいくつかに取り組まれた。新しいDrupal 6のテーマ・システムは、PHPから[HTML](../Page/HyperText_Markup_Language.md "wikilink") / [CSSをさらに分離しようとする試みで](../Page/Cascading_Style_Sheets.md "wikilink")[テンプレートエンジン](../Page/テンプレートエンジン.md "wikilink")を活用する。新しいDrupal開発モジュール "Devel" は、Drupal 6を使用するテーマ作成者へ支援を提供する。

## 批評

### オブジェクト指向の欠如

Drupalはもっぱら、[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink") (OOP) ではなく、[手続き型プログラミング](../Page/手続き型プログラミング.md "wikilink")が用いられる。DrupalはいくつかのOOPの特徴に近づけてはいるが\[16\]、OOP自体の欠如は以下のことをもたらす。

  - 基礎をなすプログラミング言語システムによって強化された[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")がない。これはプライベート・データの使用を排除し、[名前空間](../Page/名前空間.md "wikilink")分離の存在しない実施をもたらす。名前空間の分離がないため、インストールされたモジュールやテーマでのあらゆる[関数や変数が](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")、その他のインストールされたモジュール、インストールされたテーマ、あるいはDrupalコアにおけるその他の関数や変数の名前と同じ場合、「死の白画面」（[:en:white screen of death](https://ja.wikipedia.org/wiki/:en:white_screen_of_death "wikilink")）を含む重大なエラーを起こす可能性がある\[17\]。
  - オブジェクトの継承が「弱い」ためコードの再利用があまり効率的ではなく、[多態性](https://ja.wikipedia.org/wiki/多態性 "wikilink")はレンダリング層でのみ近づけられる\[18\]。

Drupalの擁護論者は、PHPのOOP言語機能は直接実装されていない（PHPバージョン4.xとの互換性を保証するため）にもかかわらず、OOPと[アスペクト指向プログラミング](../Page/アスペクト指向プログラミング.md "wikilink")（AOP）の原則がDrupalの設計には存在すると反証する\[19\]。これはDrupalコアの将来のバージョンに移行するのに役立つが、それはバージョン7を皮切りに、PHP5によって提供されるOOPを活用し始めるであろう。Drupal 7は以前のPHPリリースと後方互換ではなくなるであろう。\[20\]

## セキュリティ対策の記録

2008年1月から5月まで、Drupalコアで5つのセキュリティ脆弱性が報告され、修正された\[21\]。また、ユーザから寄贈された2147のモジュールのうち、25のモジュールでセキュリティホールが発見され、修正された\[22\]。

セキュリティホールが発見されるとともに、Drupalコアは規則的に新しいバージョンへと更新される。Drupalサイトの管理者は、“Update Status”モジュールによってこれらの新しいリリースを自動的に通知される\[23\]。さらに、Drupal.orgは、セキュリティ告知メーリングリスト、全セキュリティ勧告の履歴\[24\]、セキュリティ・マニュアル\[25\]、最新のセキュリティ勧告のRSSフィード\[26\]を保持する。

## ディストリビューション（配布パッケージ）

カスタマイズされたDrupalのディストリビューションには、いくつかの再パッケージ化されたサードパーティー製モジュールが含まれ、Drupalと[vBulletinが統合された](https://ja.wikipedia.org/wiki/:en:VBulletin "wikilink")[vbDrupal](https://ja.wikipedia.org/wiki/vbDrupal "wikilink")を含むいくつかのディストリビューションでは、徹底的な変更が加えられている。

[ハワード・ディーン](https://ja.wikipedia.org/wiki/ハワード・ディーン "wikilink")の2004年のアメリカ大統領選挙戦を支援する、多くの独立したウェブサイトのホストとして機能した[DeanSpaceには](https://ja.wikipedia.org/wiki/:en:DeanSpace "wikilink")、Drupal 4.2\[27\]が使用された。ディーンの選挙運動終了後、DeanSpaceは成長して[CivicSpace](https://ja.wikipedia.org/wiki/:en:CivicSpace "wikilink")（コミュニティの内部で集団行動をできるようにし、結束的に遠隔地の後援者グループを結ぶ、Drupalに基づく草の根組織化プラットフォーム）となった。このようにCivicSpaceは、もとはDrupal 4.2に基づいた派生ディストリビューションである。

CivicSpaceにおける多くの新機軸が、逆にDrupalプロジェクト自体に組み込まれた\[28\]。非営利団体や政治運動に特に有用な機能は、Drupal 5.0以上で動作する[CiviCRMモジュールで提供されている](https://ja.wikipedia.org/wiki/:en:CiviCRM "wikilink")。

ディストリビューションは、サードパーティー製モジュールであらかじめカスタマイズされ、特定タイプのウェブサイト（例えば、オンライン・ストア、音楽レビューサイト、ブログサイトなど）向けに設定済みの、「あらかじめ作られた」Drupalインストレーションを頒布するために提案された。Drupal 5.xでは、特定の目的に合わせてある「インストール・プロフィール」のセットを提供し、この方向を目指している\[29\]。

## コミュニティ

Drupalはユーザと開発者の大規模なコミュニティを所有する。Drupal.orgでは300,000を超えるユーザ・アカウントが作成され、2000人以上が開発者アカウントに登録した。\[30\]。最近の大きなカンファレンスDrupalcon Boston 2008では800人以上を集めた\[31\]。

多くの活動的な[フォーラム](https://ja.wikipedia.org/wiki/フォーラム "wikilink")\[32\]、[メーリングリスト](../Page/メーリングリスト.md "wikilink")\[33\]、ディスカッション・グループ\[34\]があり、さらに、[Freenode](https://ja.wikipedia.org/wiki/Freenode "wikilink")ネットワーク上でいくつかの[IRCチャネルを運営している](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")\[35\]。

## 関連項目

  - [コンテンツ管理システム](https://ja.wikipedia.org/wiki/コンテンツ管理システム "wikilink")
  - [オープンソース](../Page/オープンソース.md "wikilink")
  - [ポータルサイト](../Page/ポータルサイト.md "wikilink")
  - [ブログ](../Page/ブログ.md "wikilink")

## 脚注

## より詳しい文献

  - Douglass, Robert T., Mike Little, and Jared W. Smith. *Building Online Communities With Drupal, phpBB, and WordPress*. New York: Springer Verlag/Apress, 2005. ISBN 1-59059-562-9.
  - Gillmor, Dan. *We the Media|We the Media: Grassroots Journalism by the People for the People*. Sebastopol, Calif.: O’Reilly, 2004. ISBN 0-596-00733-7.
  - Graf, Hagen. *Drupal. Community-Websites entwickeln und verwalten mit dem Open Source-CMS.* Munich: Addison-Wesley, 2006. ISBN 3-8273-2321-5.
  - Mercer, David. *Drupal: Creating Blogs, Forums, Portals, and Community Websites*. Birmingham, England: Packt Publishing, 2006. ISBN 1-904811-80-9.
  - Peacock, Michael. *Selling Online with Drupal e-Commerce*. Birmingham, England: Packt Publishing, 2008. ISBN 978-1-84719-406-0
  - Shreves, Ric. *Drupal 5 Themes*. Birmingham, England: Packt Publishing, 2007. ISBN 1-84719-182-7.
  - Trippi, Joe. *The Revolution Will Not Be Televised: Democracy, the Internet, and the Overthrow of Everything*. New York: ReganBooks, 2004. ISBN 0-06-076155-5.
  - VanDyk, John K., and Matt Westgate. *Pro Drupal Development*. New York: Springer Verlag/Apress, 2007. ISBN 1-59059-755-9.

## 外部リンク

  - [公式サイト（英語）drupal.org](https://drupal.org/)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:Webオーサリングソフト](https://ja.wikipedia.org/wiki/Category:Webオーサリングソフト "wikilink") [Category:ブログソフト](https://ja.wikipedia.org/wiki/Category:ブログソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  Web 2.0 <https://drupal.org/node/101689>
2.  History <https://drupal.org/node/769>
3.  "Drupal Download Statistics," <https://dri.es/drupal-download-statistics-2007>
4.  "Growth Graphs," <http://groups.drupal.org/node/1980>
5.  <https://drupal.org/download>
6.  [Drupal changelog](https://cgit.drupalcode.org/drupal/plain/core/CHANGELOG.txt)
7.  ["Translations," Drupal (February 18, 2008)](https://drupal.org/project/Translations)
8.  [Drupal's API page](https://api.drupal.org)
9.  [Drupal modules](https://drupal.org/project/Modules/name)
10. [Content Construction Kit](https://drupal.org/project/CCK)
11. [Views](https://drupal.org/project/views)
12. [My Drupal predictions for 2008 | Dries Buytaert](https://dri.es/drupal-predictions-for-2008)
13. "[PHPTemplate theme engine](https://drupal.org/phptemplate)", Drupal.org.
14. "[XTemplate theme engine](https://drupal.org/node/6493)", Drupal.org.
15. "[How does Drupal compare to Mambo?](https://drupal.org/node/15689#comment-25704)" discussion thread, Drupal.org. - Old, but still interesting
16.
17.
18.
19.
20. [Drupal 7 and PHP 5.2](http://drupal.org/gophp5)
21. [Security announcements | drupal.org](https://drupal.org/security)
22.
23. [Update Status module](https://drupal.org/project/update_status)
24. [Security advisories](https://drupal.org/security)
25. [Drupal security manual](https://drupal.org/node/32750)
26. [Security RSS feed](https://drupal.org/security/rss.xml)
27. [Predictions for 2004 | drupal.org](https://drupal.org/node/4877#comment-7552)
28. [CivicSpace](http://civicspacelabs.com)
29. See <https://drupal.org/project/Installation+profiles>
30. [Drupal.org stats](http://cvs.drupal.org/viewvc.py/drupal/contributions/tricks/drupal_org_stats/output-2008-05-18.html?revision=1.1&content-type=text%2Fhtml)
31. [Drupalcon Boston 2008](http://boston2008.drupalcon.org/)
32. [Drupal forums](https://drupal.org/forum/)
33. [Drupal mailing lists](https://drupal.org/mailing-lists)
34. [Drupal groups](https://groups.drupal.org/)
35. [Drupal IRC channels](https://drupal.org/node/108355)