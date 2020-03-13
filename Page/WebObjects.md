> この記事は[WebObjects](https://ja.wikipedia.org/wiki/WebObjects)から翻訳されています。


**WebObjects**（ウェブオブジェクツ）は、[Mac OS Xの開発環境に含まれていた](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")による[Webアプリケーションサーバである](../Page/アプリケーションサーバ.md "wikilink")。[アップルが開発していた](../Page/アップル_\(企業\).md "wikilink")。

Webアプリケーション・[Webサービス](../Page/Webサービス.md "wikilink")を開発・運用するための[開発ツール](https://ja.wikipedia.org/wiki/プログラミングツール "wikilink")・[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")を持ち、徹底した[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")、強力なデータベース接続機能、[ラピッドプロトタイピング](../Page/ラピッドプロトタイピング.md "wikilink")が可能なツールが特徴である。WebObjectsでは、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")から使用できる[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")、Webサービスを提供する[アプリケーションを開発することができる](../Page/アプリケーションソフトウェア.md "wikilink")。

WebObjectsのサポートするプラットフォームは開発・運用環境共にMac OS Xのみだが、運用環境はJavaのみで開発されており、Javaをサポートしている[プラットフォームであればWebObjectsアプリケーションを運用できる](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")（バージョンによっては[Mac OS X Serverを購入して運用ライセンスを得ることが必要](https://ja.wikipedia.org/wiki/macOS_Server "wikilink")）。また、[JBoss](../Page/JBoss.md "wikilink")、[Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")、BEA WebLogic、IBM WebSphereといった[サードパーティー](../Page/サードパーティー.md "wikilink")の[Java EEアプリケーションサーバでも運用できる](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。

現在アップルは[Apple Online Store](../Page/Apple_Online_Store.md "wikilink")、[App Storeをはじめとした自社オンラインサービスをWebObjectsで構築している](../Page/App_Store.md "wikilink")。中でも[iTunes Storeは最も利用者の多いWebObjectsアプリケーションであった](https://ja.wikipedia.org/wiki/iTunes_Store "wikilink")。

## 特徴

  - コストが不要
    WebObjectsはMac OS Xの開発環境に付属するので、Mac以外のコストはかからない。
  - 強力なフレームワーク
    Webアプリケーションの開発・運用に必要な機能を提供する各種フレームワークを持つ。
  - Webアプリケーションサーバ
    WebObjectsアプリケーションは[Java SEベースのWebアプリケーションサーバとしてスタンドアロンで動作する](../Page/Java_Platform,_Standard_Edition.md "wikilink")。アプリケーションの管理にはJavaMonitorというアプリケーションを使い、Webブラウザから操作する。[サーブレット](https://ja.wikipedia.org/wiki/サーブレット "wikilink")として[Java EEサーバで運用することも可能](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。
  - データベースアクセス
    [関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")のテーブルをクラスにマッピングするデータベースフレームワークにより、SQL文を記述することなくデータベースにアクセスすることができる。（[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")）
  - プレゼンテーション、ロジック、データの分離
    プレゼンテーション (HTML)、ロジック (Java)、データ (SQL) を明確に分離し、再利用可能なWebページを構成する。
  - ステート管理
    セッションを用いてあらゆるオブジェクトを長期間保持することができる。
  - スケーラビリティとパフォーマンス
    複数のアプリケーションインスタンス、複数のアプリケーションサーバを管理できる。[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")のアルゴリズムは3種類用意されている。
  - ルールベースの高速アプリケーション開発
    プロジェクト作成時にデータモデルを与えるだけで、カスタマイズが可能なWebアプリケーションを生成することができる。

## 歴史

WebObjectsは[1996年](../Page/1996年.md "wikilink")3月に[NeXT Software Inc.から世界初のWebアプリケーションサーバとしてリリースされた](../Page/NeXT.md "wikilink")。以降他製品との競争により開発が進み、[ウォルト・ディズニー・カンパニー](../Page/ウォルト・ディズニー・カンパニー.md "wikilink")、[デル](../Page/デル.md "wikilink")コンピュータ、[英国放送協会](../Page/英国放送協会.md "wikilink")、[日産自動車](../Page/日産自動車.md "wikilink")などの大企業でも使われるようになった。

その後NeXTは[アップルコンピュータに買収され](../Page/アップル_\(企業\).md "wikilink")、アップルコンピュータはWebObjectsを手に入れてからソフトウェアをハードウェアの販売につなげる戦略を展開している。[2000年](../Page/2000年.md "wikilink")には無制限の運用ライセンスを含めたWebObjectsの価格を、5万ドルから699ドルに大幅に値下げした（当時の日本円で約692万円の値下げ）。[2001年](../Page/2001年.md "wikilink")5月にはWebObjectsの運用環境を含めたMac OS X Serverの販売を開始した。Mac OS X ServerにはWebObjectsの無制限の運用ライセンスも含まれているので、WebObjectsは実質的に無料である。

なお、現在もアップルはバージョン5.2の販売を継続している。WebObjects 5.2は[Windows 2000 Serverと](../Page/Microsoft_Windows_2000.md "wikilink")[Solaris 8での運用を公式にサポートしており](../Page/Solaris.md "wikilink")、[Windows 2000 Professional用の開発ツールが付属している](../Page/Microsoft_Windows_2000.md "wikilink")。

[2005年](../Page/2005年.md "wikilink")6月にはバージョン5.3がリリースされ、WebObjectsは単体の製品からMac OS Xの一部として移行した。699ドルで販売されていた開発ツールとフレームワークは[Xcode](../Page/Xcode.md "wikilink")に付属するようになり、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Solaris](../Page/Solaris.md "wikilink")など他プラットフォームのサポートを打ち切った。一部の開発ツールの[インタフェースが一新されたが](../Page/インタフェース_\(情報技術\).md "wikilink")、主な機能にほとんど変更はなかった。アップルはこのままWebObjectsをXcodeに統合する方針だったが、この方針はすぐに変更されることとなった。

[2006年](../Page/2006年.md "wikilink")8月、アップルはWWDCでCocoa-Javaブリッジの廃止を告げた。WebObjectsの開発ツールはすべてCocoa-Javaブリッジを利用して実装されていたが、アップルは再実装を行わないことに決めた。これにより、WebObjectsの開発ツールもすべて廃止されることとなった。

アップルはWebObjectsのランタイムのみ開発を継続することにし、開発ツールの開発をオープンソースコミュニティに任せることにした。オープンソースのツールの中でも代替可能なものは、[EclipseのプラグインであるWOLipsである](../Page/Eclipse_\(統合開発環境\).md "wikilink")。WOLipsは、すでに何年も重要な更新のないアップルのツールに匹敵する機能を持っていた。ただしEOModelerに相当する機能だけ欠けていたが、アップルの方針が定まったことで、急ピッチで開発が進められた。

[2007年](../Page/2007年.md "wikilink")10月、Mac OS X Leopardの開発ツールに含まれる形でWebObjects 5.4がリリースされた。ライセンスキーが不要になり、プラットフォームと開発・運用の区分に関係なく使えるようになった。Mac OS X Leopardの開発ツールからWebObjectsの開発ツールが廃止され、XcodeでもWebObjectsプロジェクトを開発できなくなり、事実上WOLipsが唯一の開発ツールとなった。

## フレームワーク

WebObjectsで使われる主なフレームワークは次の3つに分けられる。

### WebObjects フレームワーク (WOF)

WebObjects（ウェブオブジェクツ）フレームワークは、Webインタフェースとステート管理の機能を提供する。Webページを「テンプレート（HTMLファイル）、ロジック（Javaクラス）、両者間の設定ファイル（バインディングと呼ぶ）」の3つの要素で構成し、コンポーネントと呼ばれる単位で管理する。Webページ表示時には、テンプレート内の<WEBOBJECT>タグが設定に応じてHTMLに変換される。

このフレームワークはハイパーリンクやフォームコントロールも管理する。フォームの入力値は適切なオブジェクトに変換され、コンポーネントオブジェクトに代入される。ハイパーリンクや送信ボタンをクリックすると、コンポーネントオブジェクトのメソッドが呼び出されるようになっている。

また、ステート管理によりコンポーネントオブジェクトはHTTPトランザクションを越えて保持される。そのためオブジェクトの状態をHTMLとして表示したものがWebページとなる。WebObjectsアプリケーションでは、ユーザはブラウザを通してオブジェクトを操作していると言える。

### [Enterprise Objects フレームワーク](../Page/Enterprise_Objects_Framework.md "wikilink") (EOF)

Enterprise Objects（エンタープライズオブジェクツ）フレームワークは、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")とオブジェクト（Enterprise Object、エンタープライズオブジェクト、略してEOと呼ばれることが多い）をマッピングする。必要に応じてSQL文を生成するため、データベースの問い合わせから保存までオブジェクトを通して操作することができる。

EOFの大きな特徴はデータ構造としての[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")をマッピングするだけでなく、[DBMSとしての機能](../Page/データベース管理システム.md "wikilink")（トランザクション管理、同時実行制御、整合性など）を備えている点にある。特にトランザクション管理を行うオブジェクト (EOEditingContext)が中心となり、多くのデータベース操作はこのオブジェクトを通して行われる。データベース操作後はオブジェクトとデータベースが同期され、SQL文も随時生成されるので、データベースを特別に意識しなくてもプログラミングすることができる。

### Foundation フレームワーク

Foundation（ファウンデーション）フレームワークは、基本的なデータ構造やWebObjectsに必要な機能を提供する。前述したフレームワークはこのフレームワークに依存している。

このフレームワークは配列や辞書などの基本的なコレクションクラスも持ち、一部機能がJava標準ライブラリと重複する。バージョン5以前のWebObjectsは[Objective-C](../Page/Objective-C.md "wikilink")で開発されており、[NeXTSTEP](https://ja.wikipedia.org/wiki/NeXTSTEP "wikilink") / [OPENSTEP](../Page/OPENSTEP.md "wikilink")の同名フレームワークに大きく依存していた。そのため[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に移行する際に同名フレームワークがほぼそのまま移植された。ただし、多くのクラスでJava標準ライブラリと同じインタフェースが実装されている。

## ルールベースのアプリケーション開発

WebObjectsにはEOFの設定ファイルを与えるだけで各種データベース操作（検索、追加、更新、削除）を行うアプリケーションを作成する機能があり、プロトタイプを素早く作成することができる。このアプリケーションは起動時に設定ファイルからデータベースの情報を取得し、動的にWebインタフェースを生成する。アプリケーションをカスタマイズするには主にルールを用い、ルールの変更は再コンパイルをしなくともアプリケーションに反映される。

ルールベースのアプリケーションは次の3種類。

  - Direct To Web (D2W)
    HTMLベースのWebアプリケーション。
  - Direct To Web Services
    [Webサービス](../Page/Webサービス.md "wikilink")アプリケーション。

## Javaとの互換性

WebObjectsは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装されている。

  - 運用
    Java 1.3以降をインストールしたOSで動作する。サポート外ではあるが、[Windowsや各](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")ディストリビューションでの動作が確認されている。また[Java EEサーバでも運用することができる](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")。
  - [Java EEとの統合](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")
    WebObjectsアプリケーションを.warファイルなどにまとめ、[Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")[サーブレット](https://ja.wikipedia.org/wiki/サーブレット "wikilink")として運用できる。
  - [JDBC](../Page/JDBC.md "wikilink")
    WebObjectsは[JDBC](../Page/JDBC.md "wikilink")ドライバを使ってデータベースと通信する。

## バージョン履歴

  - 1.0 — [1996年](../Page/1996年.md "wikilink")[5月28日](../Page/5月28日.md "wikilink")
      - デビューリリース。
  - 2.0 — [1996年](../Page/1996年.md "wikilink")[6月25日](../Page/6月25日.md "wikilink")
      - WebObjects Builderのプレリリース。
  - 3.0 — [1996年](../Page/1996年.md "wikilink")11月
  - 3.1
      - Java APIの一部をサポート。
  - 3.5 — [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")12月
      - Javaのサポートを強化。すべてのコンポーネントとオブジェクトがJDK 1.1.3で動作するようになった。
  - 4.0 — [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")9月
      - [OPENSTEP](../Page/OPENSTEP.md "wikilink") 4.2 OSのサポートが中止され、YelloBoxと呼ばれる[OPENSTEP](../Page/OPENSTEP.md "wikilink")のライブラリが[Windows NTに移植された](../Page/Microsoft_Windows_NT.md "wikilink")。
      - 静的なURLから特定のメソッドを呼び出せる、ダイレクトアクションと呼ばれる機能が追加された。
      - Direct to Webアプリケーションが開発できるようになった。
      - WebObjectsとEOFが[スレッドセーフ](../Page/スレッドセーフ.md "wikilink")になり、マルチスレッドで動作するアプリケーションを開発できるようになった。
      - 1999年3月
          - [Mac OS X Serverに対応](https://ja.wikipedia.org/wiki/Mac_OS_X_Server_1.0 "wikilink")。このMac OS X Serverは「Rhapsody」のコードネームで開発されていたもの。
  - 4.5 — [2000年](../Page/2000年.md "wikilink")5月
      - [Objective-C](../Page/Objective-C.md "wikilink")で開発できる最後のバージョン。
  - 5.0 — [2001年](../Page/2001年.md "wikilink")5月
      - [Objective-C](../Page/Objective-C.md "wikilink")から[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に全面的に書き直された。
  - 5.1 — [2002年](../Page/2002年.md "wikilink")[1月10日](../Page/1月10日.md "wikilink")
      - Enterprise JavaBeansをサポート。
      - アプリケーションをサーブレットとして運用できるようになった。
  - 5.2 — [2002年](../Page/2002年.md "wikilink")11月
      - [Webサービス](../Page/Webサービス.md "wikilink")をサポート。
  - 5.2.1 — [2002年](../Page/2002年.md "wikilink")11月
  - 5.2.2 — [2003年](../Page/2003年.md "wikilink")8月
  - 5.2.3 — [2004年](../Page/2004年.md "wikilink")2月
  - 5.2.4 — [2005年](../Page/2005年.md "wikilink")[5月2日](../Page/5月2日.md "wikilink")
  - 5.3 — [2005年](../Page/2005年.md "wikilink")[6月6日](../Page/6月6日.md "wikilink")
      - 開発ツールが[Xcode](../Page/Xcode.md "wikilink")に統合された。
      - 開発・運用環境がMac OS Xのみのサポートになった。
  - 5.3.1 — [2005年](../Page/2005年.md "wikilink")[11月10日](../Page/11月10日.md "wikilink")
  - 5.3.2 — [2006年](../Page/2006年.md "wikilink")[8月7日](../Page/8月7日.md "wikilink")
  - 5.3.3 — [2007年](../Page/2007年.md "wikilink")[2月15日](../Page/2月15日.md "wikilink")
  - 5.4 — [2007年](../Page/2007年.md "wikilink")10月 (Mac OS X 10.5)
      - 開発ツールの廃止 (EOModeler, WebObjects Builder、Rule Editor)。
      - [Xcode](../Page/Xcode.md "wikilink")から開発環境が外された。以降の開発はWOLipsを使う必要がある。

## オープンソースの代替ソフトウェア

[OPENSTEP](../Page/OPENSTEP.md "wikilink")と同様、WebObjectsが周囲に与えた影響は小さくない。 WebObjectsが[Objective-C](../Page/Objective-C.md "wikilink")から[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に書き直されてから、[オープンソース](../Page/オープンソース.md "wikilink")の代替ソフトウェアが数多く作られてきた。 Objective-CやJavaを含め、様々な言語で影響を受けたフレームワークが開発されている。

  - Objective-C
      - [SOPE](https://ja.wikipedia.org/wiki/SOPE "wikilink")
      - [GNUstepWeb](https://ja.wikipedia.org/wiki/GNUstepWeb "wikilink")
  - Java
      - [Tapestry](../Page/Apache_Tapestry.md "wikilink")
      - [Cayenne](https://ja.wikipedia.org/wiki/Cayenne "wikilink")
      - [wotonomy](https://ja.wikipedia.org/wiki/wotonomy "wikilink")
  - [Ruby](../Page/Ruby.md "wikilink")
      - [IOWA](https://ja.wikipedia.org/wiki/IOWA "wikilink")
      - [Borges](https://ja.wikipedia.org/wiki/Borges "wikilink")
      - [SWS](../Page/SWS.md "wikilink")
      - [SDS](../Page/SDS.md "wikilink")
      - [CGIKit](https://ja.wikipedia.org/wiki/CGIKit "wikilink")
      - [TapKit](https://ja.wikipedia.org/wiki/TapKit "wikilink")
  - [Python](../Page/Python.md "wikilink")
      - [Modeling Framework](https://ja.wikipedia.org/wiki/Modeling_Framework "wikilink")
  - [Smalltalk](../Page/Smalltalk.md "wikilink")
      - [Seaside](https://ja.wikipedia.org/wiki/Seaside "wikilink")
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
      - [PHOCOA](https://ja.wikipedia.org/wiki/PHOCOA "wikilink")

## 外部リンク

### 情報及びサンプルコード

  - [Apple WebObjects product page（英語版）](http://www.apple.com/webobjects/)
  - [Apple WebObjects developer page（英語版）](http://developer.apple.com/tools/webobjects/)
  - [Apple WebObjects Reference Library（英語版）](http://developer.apple.com/referencelibrary/DeveloperTools/idxWebObjects-date.html)

### オープンソースの代替ソフトウェア

  - [Objective-C](../Page/Objective-C.md "wikilink")
      - [SOPE](http://sope.opengroupware.org)
      - [GNUstepWeb](http://www.gnustepweb.org/)
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
      - [Tapestry](http://jakarta.apache.org/tapestry/)
      - [Cayenne](http://www.objectstyle.org/cayenne/)
      - [wotonomy](http://wotonomy.sourceforge.net/)
  - [Ruby](../Page/Ruby.md "wikilink")
      - [IOWA](http://enigo.com/projects/iowa)
      - [Borges](http://borges.rubyforge.org/)
      - [SWS](http://www.starware.one.pl/software/sws/index.html)
      - [SDS](http://www.starware.one.pl/software/sds/index.html)
      - [CGIKit](http://cgikit.sourceforge.jp/)
      - [TapKit](http://www.spice-of-life.net/tapkit/index_ja.html)
  - [Python](../Page/Python.md "wikilink")
      - [Modeling Framework](http://modeling.sourceforge.net/)
  - [Smalltalk](../Page/Smalltalk.md "wikilink")
      - [Seaside](http://seaside.st/)
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
      - [PHOCOA](http://phocoa.com/)
  - [Haskell](../Page/Haskell.md "wikilink")
      - [WebFunctions](http://www.cs.uu.nl/wiki/WebFunctions/)

[Category:Webサーバ](https://ja.wikipedia.org/wiki/Category:Webサーバ "wikilink") [Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:ウェブアプリケーション](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーション "wikilink")