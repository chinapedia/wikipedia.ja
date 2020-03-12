> この記事は[Apache Maven](https://ja.wikipedia.org/wiki/Apache_Maven)から翻訳されています。


**Apache Maven**（アパッチ メイヴン／メイヴェン）は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")用プロジェクト管理ツールである。[Apache Antに代わるものとして作られた](../Page/Apache_Ant.md "wikilink")。[Apacheライセンスにて配布されている](https://ja.wikipedia.org/wiki/Apache_License "wikilink")[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")である。

## 特徴

このツールの大きな特徴は[プラグイン](../Page/プラグイン.md "wikilink")拡張により様々な使い方ができることである。[ソースコード](../Page/ソースコード.md "wikilink")の[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")、[テスト](../Page/ソフトウェアテスト.md "wikilink")、[Javadoc](../Page/Javadoc.md "wikilink")生成、テストレポート生成、[プロジェクト](../Page/プロジェクト.md "wikilink")[サイト](../Page/サイト.md "wikilink")生成、[JAR生成](../Page/JAR_\(ファイルフォーマット\).md "wikilink")、[サーバ](../Page/サーバ.md "wikilink")への[デプロイ](https://ja.wikipedia.org/wiki/デプロイ "wikilink")、[WAR](https://ja.wikipedia.org/wiki/WAR_\(アーカイバ\) "wikilink"), [EAR](https://ja.wikipedia.org/wiki/EAR "wikilink")ファイル生成など様々な機能が用意されており、Antの場合にはbuild.xmlという設定ファイルに細かい指示を記述して行っていた各処理を、Mavenでは大まかな指示をpom.xmlに記述して処理する形となっている。

Mavenの大きな特徴は、pom.xmlの<dependency>[タグ](../Page/タグ.md "wikilink")にプロジェクトで使用したいJARライブラリ名及びバージョンを指定することで、外部サイトで集中管理されているJARを自動ダウンロードし、ローカルでビルドに使用することができる。JARを手動でひとつずつ[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")して設定する旧来の手法と比較して、この[Perl](../Page/Perl.md "wikilink")の[CPAN](../Page/CPAN.md "wikilink")や[PHPの](../Page/PHP_\(プログラミング言語\).md "wikilink")[PEAR](../Page/PEAR.md "wikilink")に似た技術により、[WindowsUpdate](https://ja.wikipedia.org/wiki/WindowsUpdate "wikilink")などののように容易に[ライブラリ](../Page/ライブラリ.md "wikilink")を管理・アップデートできる。そのほか[Git](../Page/Git.md "wikilink")、[CVSや](../Page/Concurrent_Versions_System.md "wikilink")[Subversionなどの](../Page/Apache_Subversion.md "wikilink")[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")にも対応している。

例えば、開発チームでプロジェクトを共有したいとき、JARファイルをわざわざ他者に手動でダウンロード、インストール、アップデートさせる手間も省くことができ、pom.xmlファイルと必要なソースコード、[リポジトリ](../Page/リポジトリ.md "wikilink")に登録されていないJARファイルを配布するだけで済むようになる。なお、リポジトリに登録されていないJARファイルについては自身でリポジトリを作成し、集中管理・配布することも可能となっている。

Mavenはプラグインによって拡張することも可能である。

## Maven 2

Maven 2はJavaで書き直されて多くの点で改良されているため、Maven 1と互換性がかなり低いものの、Maven 1とMaven 2で使われるMavenのファイル名が異なることから、ひとつのMavenプロジェクトディレクトリでMaven 1とMaven 2の設定ファイル（project.xml,pom.xmlなど）を共有し、併用することができる。及びAntに対する依存性はなくなっている。また、[スクリプト言語](../Page/スクリプト言語.md "wikilink")である[Groovy](../Page/Groovy.md "wikilink")に対応している。Maven 2ではproject.xmlがpom.xmlになり文法が変わっている。project.propertiesはsettings.xmlに変わった。Maven 1で使用していたmaven.xmlはpom.xmlに統合されている。

## Maven 3

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")にはMaven 3がリリースされた。3においては2との後方互換性の確保が図られている一方、各種内部構造の大幅な更新がなされている。\[1\]

## 外部ツール

Javaの主要IDEである[Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink")、[NetBeans](../Page/NetBeans.md "wikilink")、[IntelliJはネイティブにMavenに対応しており](https://ja.wikipedia.org/wiki/IntelliJ_IDEA "wikilink")、pom.xmlをIDEのプロジェクトとして取り込んで作業することが可能となっている。

## 脚注

## 外部リンク

  - [Maven ホームページ](http://maven.apache.org/)

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.