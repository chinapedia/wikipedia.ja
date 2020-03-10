> この記事は[Enterprise Objects Framework](https://ja.wikipedia.org/wiki/Enterprise_Objects_Framework)から翻訳されています。


{this.\>\\\~'+'(("function, set_margin")file\\\\\\. {default} (MB) | || . **Enterprise Objects Framework**（**EOF**）とは、1994年に[NeXT](../Page/NeXT.md "wikilink")の[NeXTSTEPおよび](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")[OpenStep向けに導入された初期の](https://ja.wikipedia.org/wiki/OPENSTEP "wikilink")[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")製品である。EOFは[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")とのやり取りの過程を抽象化し、データベース内の行を[Java](https://ja.wikipedia.org/wiki/Java "wikilink")や[Objective-C](../Page/Objective-C.md "wikilink")の[オブジェクトにマッピングする](../Page/オブジェクト_\(プログラミング\).md "wikilink")。これにより、開発者は低レベルな[SQL](../Page/SQL.md "wikilink")コードを書く作業からほぼ解放される。EOFは1990年代中盤に金融関係でそれなりの成功を収めた。1996年にNeXTが[アップルコンピュータに吸収合併されると](../Page/アップル_\(企業\).md "wikilink")、EOFはアップルの[アプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink") [WebObjects](https://ja.wikipedia.org/wiki/WebObjects "wikilink") の一部として統合され、同製品の特徴とされるようになった。

## 歴史

1990年代初期[NeXT](../Page/NeXT.md "wikilink")は、データベース利用が多くのビジネスにとって基本であり、かつそれがかなり複雑であることを認識していた。データのソースが違えばアクセス言語（あるいは[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")）も違うため、学習に要するコストや各社製品を使うことによるコストが問題となっていた。NeXT の技術者は[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")の利点を生かし、オブジェクトに関係データベースと対話させようと考えた。オブジェクト指向と関係データベースは全く異なる技術であるため、何らかの抽象化層を作る必要があると考えられた。それによって、開発者が低レベルで各データソースに固有な手続き的コード ([SQL](../Page/SQL.md "wikilink")) を書くことから解放されるのである。

最初の試みは[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")にリリースされた Database Kit (DBKit) であった。これはオブジェクト指向フレームワークで任意のデータベースを覆ってしまおうというものである。しかし、当時の[NEXTSTEP](https://ja.wikipedia.org/wiki/NEXTSTEP "wikilink")の性能が足りず、DBKitの設計は実用には向いていなかった。

[1994年](../Page/1994年.md "wikilink")にNeXTはEnterprise Objects Framework (EOF) バージョン 1をリリースした。DBKitよりさらに強力だが、基本的な考え方は変わっていない。

その後根本的に書き換えを行って、[モジュール性](https://ja.wikipedia.org/wiki/モジュール性 "wikilink")を強化しつつ[OpenStepにも対応させ](https://ja.wikipedia.org/wiki/OPENSTEP "wikilink")、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")後半にEOF 2.0がリリースされた。EOF 2.0は[NeXT](../Page/NeXT.md "wikilink")がFoundation Kitを使った初の製品であった。開発チームはたった3人で構成されていた ([Craig Federighi](https://ja.wikipedia.org/wiki/クレイグ・フェデリギ "wikilink"), Eric Noyau、Dan Willhite\[1\])。

EOFは1990年代中盤に金融業系のプログラミングである程度の人気を得たが、やがて[World Wide Webの成長と](../Page/World_Wide_Web.md "wikilink")[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")の概念が生まれたことで本領を発揮することになった。EOFを使えば、古いデータベースを全くいじらずに、そのデータをWebに利用できることは明らかだった。EOFを核とし、状態管理、負荷分散、動的HTML生成などのフレームワークを追加して、NeXTは[1996年](../Page/1996年.md "wikilink")に世界初のオブジェクト指向アプリケーションサーバ[WebObjects](https://ja.wikipedia.org/wiki/WebObjects "wikilink")をリリースした。

[2000年](../Page/2000年.md "wikilink")、[アップルコンピュータはEOFを独立した製品とし](../Page/アップル_\(企業\).md "wikilink")、[Mac OS Xでのデスクトップアプリケーション開発に利用できるようにした](https://ja.wikipedia.org/wiki/macOS "wikilink")。ただし、同時にWebObjectsの主要コンポーネントとしても使われ続けている。2001年にリリースされたWebObjects 5では、そのフレームワークを[Objective-C](../Page/Objective-C.md "wikilink")から[Java](https://ja.wikipedia.org/wiki/Java "wikilink")へ移植した。この変更に批判的な人は、EOFの能力の大半がObjective-Cと深く結びついており、Javaへの移植によってEOFが持っていた美しさと単純さが失われたと指摘している。[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")のツール（EOGeneratorなど）は、Objective-CとJavaの差異を埋める助けとなる（主な問題は、[カテゴリ機能が無くなったことに起因する](https://ja.wikipedia.org/wiki/Objective-C#カテゴリ "wikilink")）。

## 動作原理

EOFは[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")のためのツールとフレームワークを提供する。この技術は、[JDBC](../Page/JDBC.md "wikilink")経由の[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")や[JNDIディレクトリといった各種データソースからデータを検索する機構と](../Page/Java_Naming_and_Directory_Interface.md "wikilink")、それらデータソースにデータを書き戻す機構を提供することに特化したものである。その機構は階層化・抽象化されており、開発者は特定のデータソースやそのベンダーを意識することなく、高い抽象レベルでデータの読み書きを考えることができる。

その中心となるのはモデルファイル ("EOModel") であり、視覚化ツールEOModelerか[Xcode](https://ja.wikipedia.org/wiki/Xcode "wikilink")のEOModelerプラグインを使って構築する。そのマッピングは以下のように行われる。

  - データベースの表をクラスにマッピングする。EOF
  - データベースの列（カラム）をクラスの属性にマッピングする。EOF
  - データベースの行（ロウ）をオブジェクト（クラスの[インスタンス](../Page/インスタンス.md "wikilink")）にマッピングする。EOF

既存のデータソースに基づいてデータモデルを構築することもできるし、一から構築することもできる（その場合、データベースも一から構築される）。結果として、データベースのレコードがJavaのオブジェクトに変換される。

データモデルを使う利点は、固有な性質を持つデータソースとアプリケーションを分離できる点にある。アプリケーションの[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")をデータベースから分離することで、アプリケーションに変更を加えることなくデータベースを置き換えることが可能となる。

EOFは他のツールには見られないレベルでデータベース透過性を提供しており、同じモデルを使って異なるデータベースにアクセスでき、さらには複数の異なるデータベースを同時に扱うことも可能である。

### 継承の利用

EOFでは、オブジェクト指向の特徴である[継承を活用している](https://ja.wikipedia.org/wiki/継承_\(プログラミング\) "wikilink")。オブジェクトは、より汎用的な上位のオブジェクトを「継承」し、それに何らかの特殊化を施す。オブジェクト指向プログラミングでは、全てのオブジェクトがこのような継承関係の階層に位置づけられる。しかし、関係データベースはこのような階層は持たない。EOFを使ってデータモデルを構築すると、そこにはオブジェクトの階層が反映される。すなわち、Enterprise Objectsが複数の表にマップされるか[ビューにマップされるように設計することで](https://ja.wikipedia.org/wiki/ビュー_\(データベース\) "wikilink")、データベースの表群が継承をサポートするかのように設計することが可能である。

## Enterprise Objectとは何か

Enterprise Object（直訳すれば「企業オブジェクト」）は、オブジェクト指向プログラミングで[ビジネスオブジェクト](https://ja.wikipedia.org/wiki/ビジネスオブジェクト "wikilink")と呼ばれるものに似ている。ビジネスオブジェクトとは、ビジネス領域での具体的あるいは概念的オブジェクト（例えば、顧客、注文、商品など）をモデル化したクラスである。EO (Enterprise Objects) が他のオブジェクトと異なるのは、そのインスタンスが何らかのデータソースとマッピングされている点である。典型的なEnterprise Objectは、キーと値のペアを含み、関係データベースの行を表している。キーは列（カラム）の名前であり、その値はデータベース内のその行のそのカラムに格納されている値に他ならない。従って、EOの属性は[永続性があると言える](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink")。

より正確に言えば、Enterprise Objectとは、com.webobjects.eocontrol.EOEnterpriseObjectインタフェースを実装したクラスのインスタンスである。

Enterprise Objectには対応するモデル (EOModel) があり、そのクラスのオブジェクトモデルとデータベースの[スキーマとのマッピングが定義されている](../Page/スキーマ_\(データベース\).md "wikilink")。しかし、Enterprise Object自体にはそのモデルに関する知識は存在しない。このような抽象化によって、データベース製品を切り換えても、コードを修正せずに済むのである。そのため、Enterprise Objectsは高度な再利用性を有する。

## EOFとCore Data

EOF の概念の多くは、2005年4月にリリースされた[Mac OS X Tigerにおいてデスクトップアプリケーション向けに導入された](../Page/Mac_OS_X_v10.4.md "wikilink")。[Core Dataは](https://ja.wikipedia.org/wiki/Core_Data "wikilink")、[Cocoa](../Page/Cocoa.md "wikilink") APIを使った開発者向けのオブジェクト-グラフ管理と永続性フレームワークである。つまり、Core Dataはアプリケーションのモデル層をメモリ上に定義されたデータオブジェクト群に編成する。Core Dataはそれらオブジェクトの変化を監視し、必要に応じてその変化を取り消すことができる（ユーザーがundoコマンドを実行したような場合）。そして、アプリケーションのデータの変更点をセーブする際、Core Dataがオブジェクトを永続性のある記憶装置に格納する作業を行う。

このように2つの技術はよく似ているが、目的は異なる。EOFは、クライアントをデータベースサーバに接続するための[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ベースのフレームワークである。Core Dataは、デスクトップアプリケーション開発をサポートするよう設計された[Objective-C](../Page/Objective-C.md "wikilink")ベースのフレームワークである。Core DataとEOFには、それぞれもう一方にはない固有の機能がある。

## 脚注

## 外部リンク

  - [Apple documentation: *Enterprise Objects*](http://developer.apple.com/documentation/WebObjects/Enterprise_Objects/)
  - [Apple WebObjects product page](http://www.apple.com/webobjects)
  - [article in linuxjournal about GDL2](http://www.linuxjournal.com/article.php?sid=7101&mode=thread&order=0&thold=0)

[Category:オブジェクト関係マッピング](https://ja.wikipedia.org/wiki/Category:オブジェクト関係マッピング "wikilink") [Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:NeXT](https://ja.wikipedia.org/wiki/Category:NeXT "wikilink")

1.  [Object graph editing context and methods of use](https://www.google.com/patents/US5956728) US 5956728 A