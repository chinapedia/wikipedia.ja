> この記事は[Apache Ant](https://ja.wikipedia.org/wiki/Apache_Ant)から翻訳されています。


**Apache Ant**（アパッチ アント）は、[ビルドツール](https://ja.wikipedia.org/wiki/ビルドツール "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

[GNU](../Page/GNUプロジェクト.md "wikilink") [make](https://ja.wikipedia.org/wiki/make "wikilink") の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")版ともいえるものであり、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) など特定の環境に依存しにくい[ビルドツールである](https://ja.wikipedia.org/wiki/ビルド_\(ソフトウェア\) "wikilink")。[XML文書でビルド](../Page/Extensible_Markup_Language.md "wikilink")（ソフトウェア構築）のルールを記述することが特徴である。[統合開発環境](../Page/統合開発環境.md "wikilink")[EclipseにはAnt](../Page/Eclipse_\(統合開発環境\).md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")が標準で内蔵されている。元々 [Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink") をビルドするために開発されたものである。

Antは[タスク](https://ja.wikipedia.org/wiki/タスク "wikilink")と呼ばれる何種類ものXML要素をビルドファイル (デフォルトではbuild.xml) 上に記述してビルドのルールを作る。このタスクは、Antのプラグインとして提供されているものを外部から採り入れることで、追加することもできる。また、このタスクをAntの[アプリケーションプログラミングインタフェース](../Page/アプリケーションプログラミングインタフェース.md "wikilink") (API) に従ってJavaで記述することにより、自作することもできる。

またでは、Javaのみならず、[IKVM.NET](../Page/IKVM.NET.md "wikilink")プロジェクトにより[Ant task for IKVMCとして](https://ja.wikipedia.org/wiki/Ant_task_for_IKVMC "wikilink")[Mono](../Page/Mono_\(ソフトウェア\).md "wikilink")/[.NET Frameworkでの利用も促進されている](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。

## 主なAntタスク

  - javac : Java[ソースコード](../Page/ソースコード.md "wikilink")を[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")する。
    javadoc : Javaソースコードから[Javadoc](../Page/Javadoc.md "wikilink")ドキュメント（Java APIドキュメント）を生成する。
    java : Javaプログラムを実行する。
    junit : テストフレームワーク[JUnit](../Page/JUnit.md "wikilink")を使ってJavaプログラムを[テストする](../Page/ソフトウェアテスト.md "wikilink")。
    junitreport : junitタスクで出力した結果ファイルを用いて[HTMLフォーマットなどに対応した](../Page/HyperText_Markup_Language.md "wikilink")[レポート](https://ja.wikipedia.org/wiki/レポート "wikilink")を生成する。
    copy : [ファイルをコピーする](../Page/ファイル_\(コンピュータ\).md "wikilink")。
    delete : [ディレクトリ](../Page/ディレクトリ.md "wikilink")やファイルなどを削除する。
    mkdir : ディレクトリを作成する。
    ftp : [FTP接続を開始して](../Page/File_Transfer_Protocol.md "wikilink")、ファイルの[アップロード](../Page/アップロード.md "wikilink")、[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")などを可能にする。
    scp : [SCP](https://ja.wikipedia.org/wiki/secure_copy "wikilink")、[SFTP](https://ja.wikipedia.org/wiki/SFTP "wikilink")接続を開始して、ファイルのアップロード、ダウンロードなどを可能にする。
    cvs : [CVS接続を開始して](../Page/Concurrent_Versions_System.md "wikilink")、CVS[リポジトリ](../Page/リポジトリ.md "wikilink")からの[チェックアウト](https://ja.wikipedia.org/wiki/チェックアウト "wikilink")、[コミット](../Page/コミット.md "wikilink")、[アップデート](https://ja.wikipedia.org/wiki/アップデート "wikilink")を可能にする。
    genkey : [署名つき](../Page/電子署名.md "wikilink")[JARファイルを作成するために必要な](https://ja.wikipedia.org/wiki/Jar "wikilink")[証明書](https://ja.wikipedia.org/wiki/証明書 "wikilink")を生成する。
    signjar : JARファイルに署名する。
    native2ascii : Javaソースコードなどに含まれるマルチバイト文字の文字列部分を[JDKに付属している変換ツールを使って](../Page/Java_Development_Kit.md "wikilink")[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")コードに変換する。
    setproxy : [ネットワークに接続するタスクを実行する際に](../Page/コンピュータネットワーク.md "wikilink")、[プロキシ](../Page/プロキシ.md "wikilink")サーバのアドレスを設定する。
    tstamp : [タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")を更新しAntで使われている変数 DSTAMP、TSTAMP を更新する。
    zip : 指定したディレクトリやファイルを[ZIP形式で](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")[圧縮](../Page/データ圧縮.md "wikilink")・[アーカイブ](../Page/アーカイブ.md "wikilink")する。
    echo : [コンソール](../Page/コンソール.md "wikilink")（コマンドライン環境）に文字列を出力する。
    splash : 実行時に指定した時間だけ[スプラッシュ](../Page/スプラッシュ.md "wikilink")を表示する。画像を指定することもできる。
    buildnumber : ビルドナンバーを更新する。デフォルトでは同じディレクトリにbuild.numerという名前のファイルが自動生成され、そのファイルにビルドナンバーが記録される。
    ant : 別のAntビルドファイルにあるタスクを読み込んで実行する。

## 関連項目

  - [アジャイルソフトウェア開発](../Page/アジャイルソフトウェア開発.md "wikilink")
      - [エクストリーム・プログラミング](../Page/エクストリーム・プログラミング.md "wikilink")
  - [継続的インテグレーション](https://ja.wikipedia.org/wiki/継続的インテグレーション "wikilink")
  - [Apache Maven](../Page/Apache_Maven.md "wikilink")

## 外部リンク

  - [Apache Ant](http://ant.apache.org/)
  - [Apache Ant](http://www.jajakarta.org/ant/)
  - [NAnt](http://nant.sourceforge.net/) - Apache Antの[.NET Frameworkへの移植版](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")