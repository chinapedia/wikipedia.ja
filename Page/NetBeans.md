> この記事は[NetBeans](https://ja.wikipedia.org/wiki/NetBeans)から翻訳されています。


**NetBeans**（**ネットビーンズ**）とは、[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")（買収以前は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")、以下同）を中心としたコミュニティにより開発されている、[オープンソース](../Page/オープンソース.md "wikilink")の[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")/[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")/[C言語](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")/[JavaScript](../Page/JavaScript.md "wikilink")/[Groovy](../Page/Groovy.md "wikilink")等のいくつかの[プログラミング言語](../Page/プログラミング言語.md "wikilink")に対応している。NetBeans Platformを利用して開発されており、様々な[モジュール](../Page/モジュール.md "wikilink")を組み込むことが可能である。NetBeansの特徴の一つである[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[エディタ](https://ja.wikipedia.org/wiki/エディタ "wikilink") (Project Matisse) もその一つである。

## 概要

ほぼ100%Javaで書かれている統合開発環境である。バージョン4.0以降は、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")自体の大幅な高速化もあって、ネイティブな環境との速度差は感じないとされる。

この[ソフトウェア](../Page/ソフトウェア.md "wikilink")はJavaを開発しているオラクルが開発していることから、最新版のJavaにいち早く対応できるという利点がある。[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5.0が登場した際には他のIDEに先んじて、新機能である[ジェネリックや](../Page/ジェネリックプログラミング.md "wikilink")[アノテーション](../Page/アノテーション.md "wikilink")に対応した。またGUI開発はNetBeansがJava IDEの中で秀でており、「フリーデザイン」によるコンポーネントの配置などの優れた機能を持つ。

NetBeansは始めから[多言語](../Page/多言語.md "wikilink")に対応しており[日本語](../Page/日本語.md "wikilink")などの多くの言語をインストール直後から利用可能である。

パッケージによって異なるが開発できる言語として、Java・[JavaScript](../Page/JavaScript.md "wikilink")・[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")・[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")・[Groovy](../Page/Groovy.md "wikilink")がある。また[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")を動作させるのに必要な[Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")・[GlassFish](https://ja.wikipedia.org/wiki/GlassFish "wikilink")といった[アプリケーションサーバ](../Page/アプリケーションサーバ.md "wikilink")が同封されているパッケージもあるため、別途インストールすることなく利用できる。

Java IDEとして既に広く使われている[Eclipseと比較されることが多い](../Page/Eclipse_\(統合開発環境\).md "wikilink")。現状、シェア、多機能性、[プラグイン](../Page/プラグイン.md "wikilink")の豊富さは、Eclipseに一日の長がある。NetBeansは3.51までJava [Look\&Feelを使用していたため](https://ja.wikipedia.org/wiki/Look_and_feel "wikilink")、特にWindowsユーザーに受け入れられにくかったようである。3.6でLook\&FeelをSystemLook\&Feelに変更したことにより、ユーザーが増加しはじめた。

## 沿革

4.0から[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") / [EEのリファレンス的な開発環境としての側面が強まっている](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。5.5からは、[Webサービス](../Page/Webサービス.md "wikilink")や[パーシスタンスAPI等に対するスムーズな開発を可能にしており](../Page/Java_Persistence_API.md "wikilink")、[UMLや](../Page/統一モデリング言語.md "wikilink")[JSFのビジュアル開発なども取り込まれた](https://ja.wikipedia.org/wiki/JavaServer_Faces "wikilink")。

6.0では[Ruby](../Page/Ruby.md "wikilink")や[JavaScript](../Page/JavaScript.md "wikilink")のサポート、[プロファイラ](https://ja.wikipedia.org/wiki/プロファイラ "wikilink")の統合、ビジュアルWebJSFと通常のWEBプロジェクトの統合、[Swing](../Page/Swing.md "wikilink")アプリケーションフレームワーク、そして大幅なエディタの見直しやレスポンスの改善などがあげられる。Java言語以外のサポート、複数バージョンの[Tomcatサーブレットコンテナや各種アプリケーションサーバの対応など標準機能でカバーする範囲が広がったのが特徴である](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")。また、使用者の利用するパッケージを選択できるインストーラもいままでになかったものである。

6.1では新たに暫定版ではあるものの[PHP対応がされた](../Page/PHP_\(プログラミング言語\).md "wikilink")。また、Rubyの更なるサポート、JavaScriptの本格サポートなどJava以外の言語の対応が充実したのも特徴である。また、標準API以外のサポートは珍しいのだが、[Spring](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")2.5がWebプロジェクトのフレームワークとしてサポートされた。JSR311 としてRESTful Web サービスもサポートされ、Javaの最新技術も引き続き先行搭載されていくようである。バージョン管理システムとして[Mercurial](../Page/Mercurial.md "wikilink")が標準サポートされたが、これはNetBeans自体のバージョン管理にMercurialを使うようになったためだろう。

6.5では新たに暫定版ではあるものの[Python](../Page/Python.md "wikilink")に対応した。またPHPが正式に標準対応した\[1\]。そのほかJavaScriptのフレームワークにも対応し、prototype.js、[jQuery](https://ja.wikipedia.org/wiki/jQuery "wikilink")などをすぐに設定し使用することが可能になり\[2\]、それぞれのフレームワークに合わせた補完も効くように強化された。NetBeansのJavaは標準API以外のサポートが比較的珍しいのだが[Hibernate](../Page/Hibernate.md "wikilink")がサポートされ\[3\]、HQLを即座に試せるようになっている。データベースの扱いが強化され、データの編集に[SQL](../Page/SQL.md "wikilink")をうたなくても容易に行えるようになった。

6.4以前は英語版から一ヶ月程度遅れてML(多言語)版が登場するのが普通であったが、6.5以降では同時リリースされている。

6.7では[JIRA](https://ja.wikipedia.org/wiki/JIRA_\(ソフトウェア\) "wikilink") と [Bugzilla](../Page/Bugzilla.md "wikilink")といった課題追跡に対応した\[4\]。また、継続的インテグレーションツールである[Hudson](https://ja.wikipedia.org/wiki/Hudson "wikilink")との統合機能も追加された\[5\]。プロジェクトの形式として従来の[Antベースのもののほかに](../Page/Apache_Ant.md "wikilink")[Maven2が標準でサポートされた](https://ja.wikipedia.org/wiki/Apache_Maven#Maven_2 "wikilink")\[6\]。あわせてPHPUnit\[7\]、Selenium\[8\]、Ruby のリモートデバッグ\[9\]、[C](../Page/C言語.md "wikilink") / [C++](../Page/C++.md "wikilink")でのプロファイリングなどがサポートされたこともあり、品質向上のための機能が大幅に強化されたのが本バージョンでの最大の特徴である。

その後7.0でPythonとRuby\[10\]のサポートが外され、7.1で[JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")と[CSS3のサポートが追加された](../Page/Cascading_Style_Sheets.md "wikilink")\[11\]。7.2ではパフォーマンスチューニングが中心であったが、Amazon Elastic Beanstalk等クラウドリソースへの対応（7.2.1でOracle Cloudの対応も追加された）や[Subversionがリリースに組み込まれる等の新機軸もある](../Page/Apache_Subversion.md "wikilink")\[12\]。

7.3では新しい[JavaScriptエンジン](https://ja.wikipedia.org/wiki/JavaScriptエンジン "wikilink")、組み込み[Webkit](https://ja.wikipedia.org/wiki/Webkit "wikilink")ブラウザ、[Firefox](https://ja.wikipedia.org/wiki/Firefox "wikilink")や[Chrome](https://ja.wikipedia.org/wiki/Chrome "wikilink")との連携、そして[HTML5](../Page/HTML5.md "wikilink")やCSS3への対応強化等、Webアプリケーション開発を中心とした大型の変更が予定されている。

なお、オラクルがサポートしているわけではないが、[Scala](../Page/Scala.md "wikilink")も動作する。こちらはScala開発チームが公式のプラグインをリリースしている。

## 歴史

NetBeansは、1996年に始まったチェコの学生によるプロジェクトであるXelfiにその源流を持つ。XelfiはJavaで書かれた最初のIDEであり、1997年に最初のプレリリースが行われている。やがてXelfiは、チェコの実業家Roman Stanekの支援を得て、ネットワーク環境を前提としたJava Beansコンポーネント開発用のIDEとして開発が進められることになった。この基本構想が、NetBeansの名前の由来となっている。NetBeansの名を冠した最初のリリースは、1999年である。

この1999年は、NetBeansにとって重要な年であった。より良いJava開発環境を求めていたサンが、NetBeansと契約。サンは、その後別のツールであるForteを獲得したが、ForteではなくNetBeansをForte for Javaの名の下にリリースを行った。これは当時の知名度を優先したビジネス判断であった。しかし、ほどなくNetBeansの名は復活し、現在に至っている。なお、Xelfiに関わったメンバーの多くは、現在もNetBeansコミュニティで活躍している。

### サン・マイクロシステムズの買収

2010年の1月にオラクルがサン・マイクロシステムズを買収した。元々オラクルはJavaの統合開発環境[JDeveloper](../Page/JDeveloper.md "wikilink")を開発しており、サン・マイクロシステムズのNetBeansとはライバル製品のため、経営戦略により消えるのではないかと危惧された。しかしオラクルはJDeveloperを置き換える計画はないとしている。また、NetBeansをJavaエコシステムの重要要素と見なしており、Java開発に使用するIDEの選択肢を開発者が持ち続けることは重要であると考えているとし、開発を継続するとしている \[13\]。

2010年1月27日のOracle + Sun Strategy Update Webcastにおいて、OracleがNetBeans IDEを今度の計画のなかでどう位置づけているかが発表された\[14\]。発表されたスライドショーから関係する部分を抜き出すと

  - NetBeans IDEはJava開発向けの軽量IDEとしての位置づけを継続していく
  - Java EE6、Java ME、スクリプト言語へ注力
  - モバイル開発環境やスクリプト言語へのフォーカスを強める

となっており、従来の方針をそのまま継続する形となっている。

オラクルはまたEclipseへの投資を継続する方針も表明している。IDEにはそれぞれ一長一短があり、多様であるべきとの考えからである。

### Apacheソフトウェア財団への寄贈

2016年、オラクルはNetBeansのApacheソフトウェア財団への寄贈を提案し\[15\]、プロジェクトは[Apache Incubatorに登録された](https://ja.wikipedia.org/wiki/Apache_Incubator "wikilink")\[16\]。2019年にはApache Incubatorを脱し、トップレベルプロジェクトに昇格した\[17\]。

## NetBeansの機能

NetBeansの主要な機能は以下の通りである。

### プラグイン

標準で必要な機能が多く提供されているが、プラグインにより追加機能を使用できる。NetBeansコミュニティーや多くのベンダーから提供されている。

### ビルドツール

Javaの[ビルドに](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")[Apache Antが標準となっており](../Page/Apache_Ant.md "wikilink")、コンパイル作業が楽に行える。

### コード支援

クラス・変数・関数等のコード支援があり、開発者の手助けをしてくれる。また、[Javadoc](../Page/Javadoc.md "wikilink")にJava SEの[API日本語ドキュメントを指定すればクラスやメソッドのコード補完中に小窓が現れて日本語の説明文を読める](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

### リファクタリング

[リファクタリングにより安全にクラス名](../Page/リファクタリング_\(プログラミング\).md "wikilink")・メソッド名・変数名の変更等が行える。

### データベース管理

[JDBC](../Page/JDBC.md "wikilink")ドライバーを使うことで、[データベース管理システム](../Page/データベース管理システム.md "wikilink")に接続でき、データ操作が行える。

### バージョン管理システム

[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")として、[CVS](../Page/Concurrent_Versions_System.md "wikilink")・[Mercurial](../Page/Mercurial.md "wikilink")・[Subversionの](../Page/Apache_Subversion.md "wikilink")3つが利用できる。

### xUnit

[ユニットテストに](https://ja.wikipedia.org/wiki/ユニットテスト#.E5.8D.98.E4.BD.93.E3.83.86.E3.82.B9.E3.83.88.EF.BC.88Unit_Testing.EF.BC.89 "wikilink")[xUnit](https://ja.wikipedia.org/wiki/xUnit "wikilink")であるJUnitやPHPUnitが使用できる。

## 対応オペレーティングシステム

IDE自体がJavaで書かれていることから、[Java VMを搭載した](../Page/Java仮想マシン.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上で動作が可能である。

なお公式にサポートしているオペレーティングシステムは、以下のものである\[18\]。

  - [Microsoft Windows 7](../Page/Microsoft_Windows_7.md "wikilink") Professional
  - [Microsoft Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") SP1
  - [Microsoft Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") Professional SP3
  - [Ubuntu](../Page/Ubuntu.md "wikilink") 9.10（12.04推奨）
  - [Solaris](../Page/Solaris.md "wikilink") 11 Express
  - [Mac OS X v10.6](../Page/Mac_OS_X_v10.6.md "wikilink") Intel（[Mac OS X Lion推奨](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink")）

その他、[Oracle Enterprise Linux](https://ja.wikipedia.org/wiki/Oracle_Enterprise_Linux "wikilink") 5、Ubuntu 8.x および 10.04、[Red Hat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") など、ほかのさまざまな[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で動作することも確認されている。また[FreeBSD](../Page/FreeBSD.md "wikilink")のportsコレクションにも組み込まれている。

## ライセンス

NetBeansのコードの大部分は、[Common Development and Distribution License](https://ja.wikipedia.org/wiki/Common_Development_and_Distribution_License "wikilink") (CDDL) とGNU General Public License v2 (GPLV2) のデュアルライセンスの下でソースコードを公開している。CDDLは、Mozilla Public License (MPL) をベースとしたOSI承認ライセンスの一つである。

Apacheソフトウェア財団への寄贈後はApache License 2.0に一本化された。

## 関連製品

  - [Java Studio Creator](https://ja.wikipedia.org/wiki/Java_Studio_Creator "wikilink") - サンが開発したNetBeansベースの無償の統合開発環境。[VBに慣れたプログラマでも取り込めるようウェブ](../Page/Visual_Basic.md "wikilink")[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")開発を[Dreamweaver](https://ja.wikipedia.org/wiki/Dreamweaver "wikilink")を使うような感覚で容易に行うことができる。
  - [JDeveloper](../Page/JDeveloper.md "wikilink") - オラクルが開発したJavaの統合開発環境。

## ねこび〜ん

[ねこび〜ん.gif](https://ja.wikipedia.org/wiki/File:ねこび〜ん.gif "fig:ねこび〜ん.gif")

**ねこび〜ん** は NetBeans の[キャラクター](../Page/キャラクター.md "wikilink")。

[カネウチカズコ](https://ja.wikipedia.org/wiki/カネウチカズコ "wikilink")により作成され、日本コミュニティを介して提唱されたマスコットキャラ。[猫](https://ja.wikipedia.org/wiki/猫 "wikilink")とNetBeansをかけあわせたもの。[Creative Commons](https://ja.wikipedia.org/wiki/Creative_Commons "wikilink") 表示-継承 2.1 日本ライセンスされている\[19\]。

2008年2月27日、仙台のグループ「東北デベロッパーズコミュニティ」の設立総会後に行われた懇親会・二次会で、カネウチカズコが見せたキャラクター画像を見て、「NetBeansのキャラクターが欲しい」という話となり、ここからねこび〜んが誕生するきっかけとなった\[20\]\[21\]\[22\]。

イベントでの利用やグッズ制作にも多数使われるようになっている\[23\]。

## 注釈

## 出典

## 外部リンク

  - NetBeans

<!-- end list -->

  -
  - [NetBeans 日本語サイト](https://ja.netbeans.org/)

  - [NetBeans.jp NetBeans 日本コミュニティー](http://www.netbeans.jp/)

  - [PlanetNetBeans.org プラネットNetBeans](http://planetnetbeans.org/ja/)

<!-- end list -->

  - ねこび〜ん

<!-- end list -->

  - [ja:NetBeans ねこび〜ん](http://ja.netbeans.org/nekobean/)
  - [ねこび〜んファンサイト](http://nekobean.net/)

[Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2000年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2000年のソフトウェア "wikilink") [Category:フリーUMLツール](https://ja.wikipedia.org/wiki/Category:フリーUMLツール "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink") [Category:サン・マイクロシステムズ](https://ja.wikipedia.org/wiki/Category:サン・マイクロシステムズ "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13. [FAQ - OracleのJava開発ツール（最終更新日2010年1月27日）](http://www.oracle.com/technology/global/jp/tech/java/htdocs/javatoolsfaq.html)
14. [NetBeansはJava開発のままいく - Oracle](https://news.mynavi.jp/news/2010/02/01/015/index.html)
15.
16.
17.
18. <http://netbeans.org/community/releases/73/relnotes_ja.html#system_requirements>
19. *[NetBeans ねこび〜ん](http://ja.netbeans.org/nekobean/)*
20. *[設立総会レポート](http://tohoku-dev.jp/modules/unopen/)* 東北デベロッパーズコミュニティ, 2012年7月27日閲覧
21. *[「ねこび〜ん」を応援しましょう！](http://tohoku-dev.jp/modules/news/article.php?storyid=4)* 東北デベロッパーズコミュニティ, 2012年7月27日閲覧
22. *[グッズ売上げを義援金として寄付させていただきました](http://nekobean.net/2011/03/post-21.html)* ねこび〜ん, 2012年7月27日閲覧
23. [NekoBean](http://wiki.netbeans.org/NekoBean) NetBeans Wiki