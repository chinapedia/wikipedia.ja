> この記事は[XOOPS Cube](https://ja.wikipedia.org/wiki/XOOPS_Cube)から翻訳されています。


**XOOPS Cube**（ズープス キューブ）および**XOOPS Cube Project**は[XOOPS](../Page/XOOPS.md "wikilink")から派生した[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink") (CMS) を作成するプロジェクト。また、そのプロジェクトが作成されたCMSを指す。CMSは**XOOPS Cube Legacy**（ズープス キューブ レガシィ）を作成・管理する。

## 概要

**Simple、Secure、Scalable** の「3S」コンセプトのもと、日本語を含むマルチバイト環境に対応した柔軟性およびカスタマイズ性の高いシステムの提供を目指している。

XOOPS Cubeの「Cube」には以下の意味がある。

  - これまでのXOOPS（XOOPS 2.0系）の発展系のイメージ（XOOPS 3 ⇒ Cubeを連想できる）
  - Cube（＝立方体）を組合すことで、オブジェクト指向のシステムとして様々な形で活用できる
  - Cubeの単語が持つ「真面目な・堅い」という意味が、セキュアなシステムのイメージにつながる
  - XOOPSの後継であることを示しつつも、XOOPSとの識別が容易な名称である\[1\]

なお、派生プロジェクトのため名称は変えているが、使用しているロゴはベースとなるフォントに関してXOOPS 2.0までのXOOPSロゴを継承している。（一方XOOPSはロゴを一新させている。）

## 歴史

  - [2005年](../Page/2005年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")〜[5月](https://ja.wikipedia.org/wiki/5月 "wikilink") - XOOPS日本サポートチームは、XOOPSをサポートせず、日本独自のバージョンを提供することを発表。XOOPS Cubeという名前に決定する。
  - [2005年](../Page/2005年.md "wikilink")[6月](../Page/6月.md "wikilink") - 日本独自のバージョンXOOPS 2.0.xJPを発表・公開する。
  - [2005年](../Page/2005年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink") - 日本初のXOOPS新名称をXOOPS Cubeと発表。
  - [2005年](../Page/2005年.md "wikilink")[9月](../Page/9月.md "wikilink") - XOOPS Cubeの新公式サイトへ移行、XOOPS Cubeのロゴを公開。
  - [2007年](../Page/2007年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink") - XOOPS 2.0.xJP系の上位互換であるXOOPS Cube Legacy 2.1.0を発表。日本公式サイトが[SourceForge.net](../Page/SourceForge.net.md "wikilink")へ移される\[2\]。
  - [2011年](../Page/2011年.md "wikilink")[4月26日](../Page/4月26日.md "wikilink") - XOOPS Cube Legacy 2.2.0を発表\[3\]。
  - [2012年](../Page/2012年.md "wikilink")[7月9日](../Page/7月9日.md "wikilink") - XOOPS Cube日本サイトを日本公式サイトに改める\[4\]。
  - [2012年](../Page/2012年.md "wikilink")[7月22日](../Page/7月22日.md "wikilink") - [ソースコード](../Page/ソースコード.md "wikilink")[リポジトリ](../Page/リポジトリ.md "wikilink")をSourceforge.netから[GitHub](https://github.com/xoopscube/legacy)に移行\[5\]。

[XOOPS-JP-history.png](https://ja.wikipedia.org/wiki/File:XOOPS-JP-history.png "fig:XOOPS-JP-history.png")

## 特徴

  - インターネットの初期から存在したBBS（[電子掲示板](../Page/電子掲示板.md "wikilink")システム）の発展形と考えるとイメージがつかみやすい。ユーザーの登録制度、投稿記事のチェック、プライベートフォーラム、サイト内検索、禁止用語設定など管理機能が強化され、いわゆる**[荒らし](https://ja.wikipedia.org/wiki/荒らし "wikilink")**に耐えうる安全なサイト運営が可能となった。
  - インストール、初期構築は簡単だが、動作や画面表示細部に関わる改造には、HTML、CSS、PHP、MySQLなどの知識が不可欠。
  - フリーで配布されている「テーマ」と呼ばれるファイルセットを切り替えることによってデザインの変更が可能。HTML、CSSの知識があれば自作テーマも可能。
  - 「モジュール」と呼ばれるプラグイン型プログラムを組み込むことにより、機能を自由に追加できる。モジュールはニュースやフォーラムに加えてスケジュール管理、ダウンロード、リンク集、フォトアルバムなど数多くの種類がモジュール作者たちのサイトからダウンロード可能。PHPやデータベースに関する知識があれば自作モジュールも可能。
  - 他のオープンソースCMSに比べて日本語、中国語などマルチバイト言語への対応度が高い。
  - 日本国内の携帯3キャリア向け表示変換classファイルやモジュールが配布されていることから、ブログ系を除く汎用CMSの中では、唯一、各キャリア携帯電話ブラウザでの表示を完全実現できるCMSと言える。
  - 企業向けXOOPS構築サービスも展開されており、企業の[サイトなどへの利用も注目されている](../Page/ウェブサイト.md "wikilink")。

統合型CMSとしては草分け的な存在で導入実績が多く、参考となる出版物も豊富にあるが、モジュールごとに微妙に[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")が異なる、アップデートが遅れがちで、[W3Cのバリデーションチェックをパスできていない](../Page/World_Wide_Web_Consortium.md "wikilink")（2009年5月現在）などの問題がある。

## 動作環境

XOOPS Cube Legacy 2.2 では下記の動作環境になっている\[6\]。

  - 推奨[Webサーバ](../Page/Webサーバ.md "wikilink")：[Apache](../Page/Apache_HTTP_Server.md "wikilink")
  - [データベース](../Page/データベース.md "wikilink")：**[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") 5.0 以上**
  - PHP：**[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink") 5.2 推奨。**5.1以下は動作しなくなる可能性あり、また5.3は[サードパーティー](../Page/サードパーティー.md "wikilink")製作のモジュールで対応していない場合あり。

XOOPS Cube Legacy 2.1 までは下記の動作環境である。

  - 推奨[Webサーバ](../Page/Webサーバ.md "wikilink")：[Apache](../Page/Apache_HTTP_Server.md "wikilink") (1.3.xx)（Apache 2.0.xxや[IISなどでの動作報告あり](../Page/Internet_Information_Services.md "wikilink")）
  - [データベース](../Page/データベース.md "wikilink")：[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink") (MySQL4.0.xx以降)
  - PHP：[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")4.3.3〜5.2.12

## インストール

先にサーバー側のMySQLに受け皿となるデータベースを用意しておく。日本語文字コードは従来[EUC-JP](../Page/EUC-JP.md "wikilink")が標準であったが、[UTF-8](../Page/UTF-8.md "wikilink")の標準化も進んでいる。なおUTF-8化するにはPHP5+MySQL5の環境が望ましい。

レンタルサーバーにアップロードするとき、全てのファイルは約14MBと大きく時間がかかるが、不要なドキュメント、言語フォルダと古いXOOPSテーマフォルダを削除すれば6MB程度の軽量となる。なお現在配布されているCube Legacyパッケージには基本的な管理モジュールしかバンドルされておらず、フォーラムなどを開始するには対応モジュールを追加インストールする必要がある\[7\]。

## 脚注

<references />

## 外部リンク

  - [XOOPS Cube日本サイト（XOOPS Cube Legacy 公式サイト：日本語）](http://xoopscube.jp/)
  - [XOOPS Cube国際サイト（XOOPS Cube Legacy 関連サイト：英語）](http://xoopscube.org/)

<!-- end list -->

  - [日本XOOPSユーザーズグループ（日本語）](http://www.xugj.org/)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  ここまで [XOOPS Cube とは - XOOPS Cube 日本サイト](http://xoopscube.jp/modules/doc/?XOOPS%20Cube%E3%81%A8%E3%81%AF) より
2.  ここまで [XOOPS年票 XUGJ](http://www.xugj.org/modules/documents/index.php?content_id=2)
3.  [XOOPS Cube Legacy 2.2.0 リリース](http://xoopscube.jp/news/829)。ただしSourceForce.netでの公開は2011年4月23日 [Xoops Cube Project - Browse /legacy at SourceForge.net](http://sourceforge.net/projects/xoopscube/files/legacy/)、英語サイトxoopscube.orgでの公開は5月4日になっている[XOOPS Cube Legacy 2.2.0 Released\!](http://xoopscube.org/modules/xhnewbb/viewtopic.php?topic_id=1025)
4.  [サイトリニューアルのお知らせ](http://xoopscube.jp/news/886)
5.  [Initial commit · 24e35b8 · xoopscube/legacy](https://github.com/xoopscube/legacy/commit/24e35b84b320be53cd3d9a65934e1668d9724555)
6.
7.  フォーラム・ブログなどのモジュールがバンドルされている独自版も存在する。