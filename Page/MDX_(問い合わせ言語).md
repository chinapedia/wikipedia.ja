> この記事は[MDX \(問い合わせ言語\)](https://ja.wikipedia.org/wiki/MDX_\(問い合わせ言語\))から翻訳されています。


**MDX**（[英](../Page/英語.md "wikilink"): **MultiDimensional eXpressions**）は、[データベース管理システム](../Page/データベース管理システム.md "wikilink")を使用した[オンライン分析処理](../Page/OLAP.md "wikilink")（OLAP）の[問い合わせ言語](https://ja.wikipedia.org/wiki/問い合わせ言語 "wikilink")である。[SQL](../Page/SQL.md "wikilink")と共通点が多い、[OLAPキューブ](https://ja.wikipedia.org/wiki/OLAPキューブ "wikilink")用の問い合わせ言語である\[1\]。また、[スプレッドシートの数式に似た構文を持つ計算言語でもある](../Page/表計算ソフト.md "wikilink")。

## 背景

MultiDimensional eXpressions（MDX）言語は、OLAPキューブに格納されている多次元データを照会および操作するための特殊な構文を提供する\[2\]。 これらの一部を従来のSQLに変換することも可能だが、その場合は非常に単純なMDX文の場合でも不格好なSQL文の合成が必要になることが多い。MDXは多くのOLAPベンダーに採用されており、事実上、OLAPシステムの[業界標準ともいえる](../Page/デファクトスタンダード.md "wikilink")。

## 歴史

MDXは、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に[MicrosoftからOLE](../Page/マイクロソフト.md "wikilink") DB for OLAP仕様の一部として初めて紹介された。これはMosha Pasumanskyを含む[SQL Serverエンジニアのグループによって発明されたもの](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")。 これに続いて[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にMicrosoft OLAP Services 7.0が商用リリースされ、その後、Microsoft Analysis Servicesがリリースされた。OLE DB for OLAP仕様の最新バージョンは、[1999年](../Page/1999年.md "wikilink")にMicrosoftから発表されている。

これはオープンな仕様ではなく、Microsoftが所有する仕様であったものの、さまざまなOLAPベンダーによって採用された。

XML for Analysis仕様ではMDX問い合わせ言語の詳細については、OLE DB for OLAP仕様を参照していた。Analysis Services 2005では、Microsoftは副問い合わせのようなMDX問い合わせ言語拡張をいくつか追加した。 Microsoft Excel 2007などの製品は、これらの新しいMDX問い合わせ言語拡張機能を使用し始めた。 MDXのこの新しいものをMDX 2005と呼ぶ人もいる。

### mdXML

[2001年](../Page/2001年.md "wikilink")、XMLA評議会（[英](../Page/英語.md "wikilink"): XMLA Council）は問い合わせ言語としてmdXMLを含むXML for Analysis（XMLA）標準をリリースした。 XMLA 1.1仕様では、mdXMLは基本的に[XML](../Page/Extensible_Markup_Language.md "wikilink") <Statement>タグでラップされたMDXである。

## MDX データ型

MDXには主に6つの[データ型](../Page/データ型.md "wikilink")がある。

  - **スカラー** - スカラーは数値または文字列。リテラルとして指定できる。例として数値5や文字列"OLAP"のようなリテラル、あるいは `Aggregate` (数値)、 `UniqueName` （文字列）、 `.Value` （数値または文字列）のようなMDX関数の戻り値など。
  - **ディメンション**/**階層** - OLAPキューブのディメンション。ディメンションは、キューブ内のメジャーや属性情報を構成するもの。MDXはディメンション間の依存関係を認識、想定せず、それらが相互に独立しているとみなす。ディメンションには、レベルを含むいくつかの階層または階層に編成されたいくつかのメンバー（以下を参照）が含まれ、一意の名前で指定できる。例として `[Time]` あるいは `.Dimension` のようなMDX関数の戻り値。階層はOLAPキューブのディメンション階層であり、一意の名前で指定できる。例として `[Time].[Fiscal]` あるいは `.Hierarchy` のようなMDX関数の戻り値。階層はディメンション内に含まれる。（OLEDB for OLAP MDX仕様では、ディメンションと階層のデータ型が区別されない。MicrosoftAnalysis Servicesなどの一部の実装では、それらの扱いが異なる。）
  - **レベル** - レベルはディメンション階層のレベルであり、一意の名前で指定できる。例として `[Time].[Fiscal].[Month]` のような一意な値、あるいは `.Level` のような関数の戻り値。
  - **メンバー** - メンバーはディメンション階層のメンバーであり、一意の名前で指定できる。例として `[Time].[Fiscal].[Month].[August 2006]` 、 `[Time].[Fiscal].[2006].[Q3].[August 2006]` のような修飾名、あるいは `.PrevMember`, `.Parent`, `.FirstChild` のようなMDX関数の戻り値。すべてのメンバーは階層ごとに固有のものでであることに注意。同一のものが2つの異なる階層（`[Product].[ByManufacturer]` and `[Product].[ByCategory]`）のメンバーである場合、セットとタプルで調整する必要のある2つの異なるメンバーが表示される可能性がある（以下を参照）。
  - **タプル** - タプルは、異なるディメンションの1つ以上のメンバーの順序付けられた集まりである。タプルはメンバーを列挙することで指定できる。例として `([Time].[Fiscal].[Month].[August], [Customer].[By Geography].[All Customers].[USA], [Measures].[Sales])` あるいは `.Item` のようなMDX関数の戻り値。
  - **セット** - セットは、同じディメンション、またはMicrosoftの実装の場合は階層のタプルの順序付けられた集まりである。タプルを列挙して指定できる。例として `{([Measures].[Sales], [Time].[Fiscal].[2006]), ([Measures].[Sales], [Time].[Fiscal].[2007])}` あるいは `Crossjoin` 、 `Filter` 、 `Order` 、 `Descendants` のようなMDX関数の戻り値など。
  - その他のデータ型 - メンバープロパティは、データウェアハウスの意味での「属性」に相当する。これらは、クエリ（問い合わせ）の軸のPROPERTIES句を使用して、クエリの文内の名前で取得できる。一部のメンバーのメンバープロパティのスカラーデータ値は、プロパティに名前を付ける（例として `[Product].CurrentMember.[Sales Price]` ）か、または特別なアクセス関数（例として `[Product].CurrentMember.Properties("Sales Price")` ）を使用することでMDXからアクセスできる。状況によっては、MDXは他のデータ型も許可する。例として[配列](../Page/配列.md "wikilink")を `SetToArray` 関数内で使用して、MDXによって処理されずにActiveXライブラリ内のユーザー定義関数へ渡される配列を指定できる。その他、Microsoftの `MeasureGroupMeasures` 関数のメジャーグループ名やMicrosoftの `KPIValue` や `KPIGoal` 関数といったデータ型もある。

## 例文

次の例は、SQL Server 2000 Books Onlineを応用したもので、SELECTステートメントを使用する基本的なMDXクエリ。このクエリは、カリフォルニア州の店舗の2002年および2003年の店舗売上を含む結果セットを返す。

``` tsql numberLines
SELECT
   { [Measures].[Store Sales] } ON COLUMNS,
   { [Date].[2002], [Date].[2003] } ON ROWS
FROM Sales
WHERE ( [Store].[USA].[CA] )
```

この例では、クエリは次の結果セット情報を定義する。

  - SELECT句は、クエリの軸をメジャーディメンションのStore Sales（店舗売上）メンバー、および日付ディメンションの2002年、2003年メンバーとして設定する。
  - FROM句は、データソースがSales（売上）キューブであることを示す。
  - WHERE句は、「スライサー軸」をStore（店舗）ディメンションのカリフォルニア州メンバーとして定義する。

注意：MDXクエリでは、最大128のクエリの軸を指定できる。

2つの軸を作成する場合、1つは列軸で、もう1つは行軸である必要があるが、クエリ内での表示順序は関係ない。軸が1つだけのクエリを作成する場合、それは列軸でなければならない。特定のオブジェクト識別子を囲む角括弧は、識別子が予約語でなく、文字、数字、またはアンダースコア以外の文字を含まない限り、オプションである。

``` tsql numberLines
SELECT
    [Measures].[Store Sales] ON COLUMNS,
    [Date].Members ON ROWS
FROM Sales
WHERE ( [Store].[USA].[CA] )
```

## 脚注

## 参考文献

  - George Spofford, Sivakumar Harinath, Chris Webb, Dylan Hai Huang, Francesco Civardi: *MDX-Solutions: With Microsoft SQL Server Analysis Services 2005 and Hyperion Essbase*. Wiley, 2006,
  - Mosha Pasumansky, Mark Whitehorn, Rob Zare: *Fast Track to MDX*.
  - Larry Sackett: *MDX Reporting and Analytics with SAP NetWeaver BW*. SAP Press, 2008, 978-1-59229-249-3

## 外部リンク

  - [多次元式 (MDX) リファレンス](https://docs.microsoft.com/ja-jp/sql/mdx/multidimensional-expressions-mdx-reference?view=sql-server-ver15), [Microsoft](https://ja.wikipedia.org/wiki/Microsoft "wikilink") Docs より

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink")

1.
2.