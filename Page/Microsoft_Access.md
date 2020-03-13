> この記事は[Microsoft Access](https://ja.wikipedia.org/wiki/Microsoft_Access)から翻訳されています。


**Microsoft Office Access**（マイクロソフト・オフィス・アクセス）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 向けに[販売](../Page/販売.md "wikilink")している、[データベース管理システム](../Page/データベース管理システム.md "wikilink")の[ソフトウェア](../Page/ソフトウェア.md "wikilink")である。

[Microsoft Officeの上位版に同梱され](../Page/Microsoft_Office.md "wikilink")、同社の[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink")である[Microsoft SQL Serverに似たソフトウェアである](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")。

Accessは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")によるRDBMSであり、（Microsoft Access 2007以降はACE＝Access Connectivity Engine）と[GUI開発環境を組み合わせてMicrosoft](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") Office Professionalへの同梱形態や、単体で販売されている。

Accessは、Access/Jet、Microsoft SQL Server、[Oracleや](../Page/Oracle_Database.md "wikilink")[ODBC準拠のデータを取り扱うことができる](../Page/Open_Database_Connectivity.md "wikilink")。データベースに精通した技術者であれば、比較的高度なアプリケーションが開発できるが、そうではない人でも各種の[ウィザード機能](../Page/ウィザード_\(ソフトウェア\).md "wikilink")\[1\]を使用することにより小規模で簡単なアプリケーションの構築が可能であるとしている。データベース入門者に対して敷居が低いように見えるが、効率のよい実用的なシステムを構築するには、それなりの技術が必要である。現在Accessは[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")に基づいたアプリケーション作成が可能であるが、完全なオブジェクト指向開発ツールには至っていない。

「Microsoft Access」は、以前マイクロソフトが販売していた通信ソフトウェアの名前でもあった。これは[ProComm](https://ja.wikipedia.org/wiki/ProComm "wikilink")などといったソフトと競合していたが、販売不振のため製品ラインナップから消滅していた。それから数年後、現在知られているデータベース・ソフトウェアの名前として再登場した。

## 歴史

Microsoft Accessのバージョン1.0は、1992年12月にリリースされた。

Access 2007では新しいファイル形式を採用により拡張子.accdbを使用。添付ファイルデータ型や[Windows SharePoint Servicesへの対応等が行われる](https://ja.wikipedia.org/wiki/Windows_SharePoint_Services "wikilink")\[2\]。

## 用途

Accessは、規模としては中小企業や大企業の事業部といった場面から、データの作成や操作をするプログラムを作りたい趣味レベルのプログラマまで広く使われている。Accessの使いやすく強力な設計ツールは、データベースをよく知らない人間であっても、非常に効率的に開発を進められる。このため、Accessとは素人向けの開発環境であって、専門家にはあまり用いられていないかのように思われがちである。

Accessはデータアクセスがネットワーク経由の場合には力不足であるため、数名以上に利用されるようなアプリケーションが必要な場合、Oracle、[DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink")、[Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、MaxDB、またはFileMaker Proのような[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")のソリューションに頼りがちである。しかしAccessの「[フロントエンド](../Page/フロントエンド.md "wikilink")」（フォーム、レポート、クエリ、およびVBコード）は、Access自身、Microsoft SQL Server、Oracle、その他のODBC──適合する製品を含むデータベース・バックエンドのホストに対して使える。

Accessを使う利用者の多くが[Leszynski命名規則](https://ja.wikipedia.org/wiki/Leszynski命名規則 "wikilink")を使用するが、これは万人共通ではない。これは[DBMSが強制する規則ではなく](../Page/データベース管理システム.md "wikilink")、プログラミングの規則である。

## 特徴

プログラマから見たAccessの利点の1つは、そのSQLとの相対的な互換性である。──クエリは[SQL](../Page/SQL.md "wikilink")文として表示や編集ができる。そしてSQL文はAccessのテーブルを操作するためにマクロや[VBAモジュールの中で直接使用できる](../Page/Visual_Basic_for_Applications.md "wikilink")。ユーザーはプログラムの形式と論理、そして[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")の可能性の提示のために、VBAと「マクロ」の両方を結合して使える。SQL文の中ではVBAと同じ[演算子](../Page/演算子.md "wikilink")や[関数を用いることができ](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")、モジュール内で定義された利用者独自の関数さえも使用できる。

Accessのレポート作成機能は、有能で洗練された報告書作成の仕事に適していたとしても、他の有名なデータベースレポート作成機能──[Crystal Reportsほどには十分に特色があり力強いとは言えない](../Page/Crystal_Reports.md "wikilink")。MSDE (Microsoft SQL Server Desktop Engine) 2000はMicrosoft SQL Server 2000のミニ・バージョンだが、[Office XP](../Page/Microsoft_Office.md "wikilink") Developer Editionに含まれており、Jet Database Engineの代わりにAccessと共に使われるかもしれない（MSDEとMicrosoft Exchange Serverの初期バージョンはデータの膨大な量を取り扱うのに実際にJet Engineを使用しており、その上にそれらのアプリケーション用に「偽の」アプリケーション層を置いた。この事実に関する知識不足は、特に「大規模な」プロジェクトについては、ソフトウェア製品Access/Jetファミリーに対する不当な軽視の一因となった）。

Accessのカット・アンド・ペースト機能は、他のデータベース間（例えばデータやデータベースを通じてOracleとMicrosoft SQL Serverと）を接続する便利なツールである。Accessにはテキスト形式やExcel形式を含め、Windowsと他のプラットフォーム・アプリケーションとの統合を許す様々なインポート・エクスポート機能（又はリンク機能）が付属しており、それらのいくつかはアプリケーション内部からの要求、又はユーザーが手動によって実行できる。例えば、完全実装されたAccessソフトウェアを持たない人たちと完全に書式化されたレポートを共有するための非常にコンパクトなAccessのスナップショット形式がある。Accessはまた、Microsoft SQL Serverにアップグレード（アップサイジングという）することができる。

Excelに慣れているユーザーから見れば、クリップボードを経由してAccessとデータを簡単にやりとりできる機能は大いに魅力的であろう。小さなデータベースなら、わずかな操作で全体をExcelに貼り付けることが可能なので、便利なだけセキュリティが甘くなることには注意が必要だ。

完全なRDBMSと異なり、Accessの[データベースエンジン](https://ja.wikipedia.org/wiki/データベースエンジン "wikilink")JETには[データベーストリガ](https://ja.wikipedia.org/wiki/データベーストリガ "wikilink")および[ストアドプロシージャ](../Page/ストアドプロシージャ.md "wikilink")が存在しない。Accessは基礎となるテーブルに対する変更を引き起こすようなコードをフォームに含めることを認めており、また、Accessに含まれるパススルー・クエリや他の技術を用いて、外部のRDBMSがサポートしているストアドプロシージャを実行することも一般的である。

Access内の各オブジェクト（テーブル、クエリ、フォーム、レポート、マクロ、モジュール等）は、拡張子がaccdbおよびmdbのデータベースファイルに保存されている。 運用上の注意点としては、Accessデータベースファイルはレコードの追加削除を繰り返すと、ファイルの容量が膨らみ大きくなってしまうので、適宜「最適化」を行う必要がある。 また、「最適化」後においてもAccessの特性上、必要以上に容量を確保するため、保存する場合はZipファイルなどに圧縮しておくと容量を削減できる場合が多い。

## 開発

Accessで利用できるプログラミング言語は、他のMicrosoft Officeスイートの製品同様、[Visual Basic for Applicationsである](../Page/Visual_Basic_for_Applications.md "wikilink")。COMコンポーネントの2つのデータベース・アクセス・ライブラリが提供されている。すなわち、Accessのみで利用可能な従来の[Data Access Objects](https://ja.wikipedia.org/wiki/Data_Access_Objects "wikilink") (DAO) と、新しい[ActiveX Data Objects](https://ja.wikipedia.org/wiki/ActiveX_Data_Objects "wikilink") (ADO) である。

Microsoft Accessは小さなプロジェクトには容易に使えるが、アプリケーションの設計が貧弱な場合、大規模なプロジェクトに対しては非効率的に働く。

また、ADOやODBC経由でWebサーバとの連携も可能であり、Webアプリケーションのデータベースとしても利用可能ではあるが、Access自体がWebDBとしての利用を想定した設計がされていないものであるため、WebDBとして利用した場合、予期せぬ、かつ解決困難な不具合が生ずる可能性がある。

すべてのデータベースのクエリ、フォーム、及びレポートはデータベースの中に格納され、リレーショナル・モデルの理想と一致するように、それらを物理的に構造化した階層は作れない。

1つの設計技術はAccessのアプリケーションをデータとプログラムに分割することである。1つのデータベースはテーブルとリレーションシップのみを含むべきであり、一方他のデータベースはすべてのプログラム、フォーム、レポート、及びクエリを含み、最初のデータベースのテーブルにリンクする。なお、Accessはリンクする場合に相対パスを許可しないため、開発環境は製品環境と同じパスを持たなければならない（ただし、Accessがカレント・パスにバックエンド・ファイルを見つけられない時、[ディレクトリ](../Page/ディレクトリ.md "wikilink")・ツリー内を検索して、あるバックエンド・ファイルを捜し出せる独自の「動的リンカ」をVBA内に記述できる）。

この技術はまた、開発者がアプリケーションを周囲の異なるファイルに分割することを可能にするため、ある種の構造は可能となる。Accessではデータベース・ファイルが大きくなり過ぎたり、ネットワーク上で多人数が同時にデータベースにアクセスした場合などで、データベースが損傷を受ける可能性が高まることが指摘されており、[分割は有効な対応策と考えられている](https://ja.wikipedia.org/wiki/分割_\(データベース\) "wikilink")。

Accessはもともとスタンドアローンで使われることを想定されている製品なので、入門書で紹介されているような、スタンドアローンで開発したデータベースを複数のユーザーが共有するような使い方では、しばしばパフォーマンスが極端に低下する。このようなケースでは、後述のようにテーブル本体をサーバのMicrosoft SQL Serverなどの中におき、ODBCでリンクする方法がある。ODBCリンクは遅いという偏見があるが、データ検索をテーブル直接でなく、インデックスから行うようにすると、ネットワークトラフィックを大幅に軽減でき、実用的なパフォーマンスが得られるようになる。Access 2000以降には[MSDE](https://ja.wikipedia.org/wiki/MSDE "wikilink")というMicrosoft SQL Serverのサブセット版が付属しているので、小規模C/Sデータベースの開発も可能となっているが、ODBCリンクを活用すればOracleや[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")などのフロントエンド開発ツールとしてAccessを利用する道も開けている。

システムの中核にAccessを据えた場合、競争が熾烈なオフィススイート製品ゆえの頻繁なプログラムの更新には注意が必要である。たとえば、Access 2003ではSP2にアップデートをするとデータベースファイルにリンクしているExcelワークシートのデータは参照のみが可能であり、リンク先ワークシート上のデータを直接更新できないようにその機能に制約が設けられた。Accessを使ったシステム開発においても、このように業務アプリケーションの機能に影響を及ぼすことが起こり得るため、システム運用中のツール（Accessのバージョン（リビジョン））自体の管理にも注意を払う必要がある。

## 仕様制限

最も大きい制限がファイルサイズで、Accessのファイルサイズ制限は2GB（リンクファイルを除く）となっている。\[3\]。

## アップサイジング

Access2000以降、スタンドアローンのデータベース（accdbファイルと[mdb](https://ja.wikipedia.org/wiki/mdb "wikilink")ファイル形式）に加えて、別のMicrosoft SQL Server（またはMSDE）内にテーブルをおき、ビューやストアドプロシージャ、トリガーを定義するプロジェクトと呼ばれる開発手法（[adp](https://ja.wikipedia.org/wiki/adp "wikilink")ファイル形式）が備わった。accdbやmdbからadpへの移行を[アップサイジング](https://ja.wikipedia.org/wiki/アップサイジング "wikilink")と呼んでいる。Accessのデータベースユーティリテイとしてアップサイジングウイザードが用意されているが、システム全体の移行にはクエリの手直しなどが必要で、決して容易な作業ではない。困難を回避するには、accdbやmdbシステムが肥大化する前にアップサイジングを行い、固有のノウハウを早く蓄積すべきである。なおアップサイジングウイザードは2013から廃止された。

mdbファイルの中のテーブルやクエリの実体はローカルにそのまま存在するが、adpファイルの中のテーブルやクエリ（ビュー、ストアドプロシージャなど）の実体はMicrosoft SQL Server内に存在する。そのためadpファイルはMicrosoft SQL Serverの管理ツールとしても機能する。ただしダイレクトにテーブルなどの定義・編集が可能となるのは、Access2000ではMicrosoft SQL Server7.0（またはMSDE）、Access2003ではMicrosoft SQL Server 2000（またはMSDE2000）である。いずれもMicrosoft SQL Server 2005（Expressを含む）と接続はできるが、テーブルなどの編集・改変はできない。Microsoft SQL Server 2005のテーブルの編集などはAccess2007およびSQL Server Management Studio（無償のExpressもある）で行える。

adpにおけるMicrosoft SQL Serverとの接続についてはODBCリンクより効率がよく有益な手法だが、プロジェクト開発に関する参考書籍など必要な情報が極端に少ないのが現状である。なおテーブルとリレーションシップの定義、ビューの作成など基本的なデータベース設計をadpで行い、入力フォームと出力レポートの設計をaccdbやmdbで行い、データをODBCリンクで結ぶという、併用的折衷的な開発スタイルもある。この場合、accdbやmdbにおいて各種外部ファイルのリンクテーブルとローカルテーブルを使い分けるといった、柔軟なシステム設計が可能となる。

ともあれ、データベース本体とフロントエンドを分離するアップサイジング開発においては、常にネットワークトラフィックの軽減を意識しなければならず、1台のPC内で完結でき、それだけわがままが許されるスタンドアローン開発とは発想の転換が必要となり、必然的にVBAコーディングが増加して、Access本来の魅力である手軽さが失われることになる。

## 主な機能

  - [テーブル](https://ja.wikipedia.org/wiki/表_\(データベース\) "wikilink")
      - リレーションシップ (関連)
  - [クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")
  - [フォーム](https://ja.wikipedia.org/wiki/フォーム "wikilink")
  - [レポート](https://ja.wikipedia.org/wiki/レポート "wikilink")
  - ページ ([HTML](../Page/HyperText_Markup_Language.md "wikilink"))
  - [マクロ](../Page/マクロ言語.md "wikilink")
  - モジュール ([VBA](../Page/Visual_Basic_for_Applications.md "wikilink"))

## Microsoft Access Runtime

Accessで開発されたアプリケーションを他のコンピュータで実行させたい場合、Accessが必要となる。しかし開発せずに実行のみの場合においてはAccessライセンスを購入せずとも、適切なMicrosoft Access Runtimeをインストールすることで開発されたアプリケーションを実行できる\[4\]。ランタイムであるため開発に必要な機能は使用できない。

## バージョン

  - Access 1.0
      - 1992年11月米国リリース
  - Access 1.1
      - 1993年5月米国リリース
      - マイクロソフト社の他製品との互換性を改善
      - Access Basicを搭載
      - 日本語版が登場
  - Access 2.0
      - ビルダ、ウィザードの導入
      - イベントプロシージャが利用可能に
  - Access 95
      - Access BasicからVBAへ移行
      - ActiveXコントロール (DAO) の導入
      - [レプリケーション](../Page/レプリケーション.md "wikilink")の導入
  - Access 97
      - ハイパーリンクなど、HTML連携の強化
      - タブコントロールの導入
  - Access 2000
      - データアクセスページの導入（データの表示・更新を[WEBページで行うことが可能](../Page/World_Wide_Web.md "wikilink")）
      - サブデータシートの導入
      - JET以外のデータベースとの連携強化、ADOの導入
      - [文字コード](../Page/文字コード.md "wikilink")を[シフトJISから](../Page/Shift_JIS.md "wikilink")[Unicode](../Page/Unicode.md "wikilink")へ変更
      - MSDE 付属
  - Access 2002 (XP)
      - MSDE 2000 付属
  - Access 2003
      - [セキュリティの強化](../Page/コンピュータセキュリティ.md "wikilink")
      - MSDE 2000 リリースA 付属
  - Access 2007
      - 他の[Office製品と同様なインターフェイスとして](../Page/Microsoft_Office.md "wikilink")、リボンインターフェイスとセキュリティセンターの導入
      - 新しいファイル形式として.accdbファイルの導入
  - Access 2010
  - Access 2013
  - Access 2016
  - Access 2019

## 脚注

## 関連項目

  - [Microsoft Office](../Page/Microsoft_Office.md "wikilink")
  - [マイクロソフト](../Page/マイクロソフト.md "wikilink")
  - [オフィススイートの比較](../Page/オフィススイートの比較.md "wikilink")
  - [Open Database Connectivity (ODBC)](../Page/Open_Database_Connectivity.md "wikilink")
  - [FileMaker](../Page/FileMaker.md "wikilink")

### 競合製品

  - [LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink") Base ([The Document Foundation](https://ja.wikipedia.org/wiki/The_Document_Foundation "wikilink"))

## 外部リンク

  - [Microsoft Office マイクロソフト 公式技術情報](http://technet.microsoft.com/ja-jp/office/default.aspx)
  - [Microsoft Office Access ホーム](http://office.microsoft.com/ja-jp/access)

[Category:データベース管理システム](https://ja.wikipedia.org/wiki/Category:データベース管理システム "wikilink") [Category:デスクトップデータベースアプリケーション開発ツール](https://ja.wikipedia.org/wiki/Category:デスクトップデータベースアプリケーション開発ツール "wikilink") [Category:Microsoft_Office](https://ja.wikipedia.org/wiki/Category:Microsoft_Office "wikilink") [Category:1992年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1992年のソフトウェア "wikilink")

1.  [Access ウィザード](https://msdn.microsoft.com/ja-jp/library/cc376162.aspx)
2.  [ACCDB ファイル形式と MDB ファイル形式の相違点](https://support.office.com/ja-jp/article/ACCDB-%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E5%BD%A2%E5%BC%8F%E3%81%A8-MDB-%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E5%BD%A2%E5%BC%8F%E3%81%AE%E7%9B%B8%E9%81%95%E7%82%B9-8cf93630-0b68-4a40-a13c-7528b9f074b6)
3.  [Access の仕様](https://support.office.com/ja-jp/article/access-%E3%81%AE%E4%BB%95%E6%A7%98-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
4.  [Download Microsoft Access 2016 Runtime from Official Microsoft Download Center](https://www.microsoft.com/ja-jp/download/details.aspx?id=50040)