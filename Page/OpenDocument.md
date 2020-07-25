> この記事は[OpenDocument](https://ja.wikipedia.org/wiki/OpenDocument)から翻訳されています。


（オープンドキュメント、）とは、[XMLをベースとした](../Page/Extensible_Markup_Language.md "wikilink")[オフィススイート](../Page/オフィススイート.md "wikilink")用の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。

構造化情報標準促進協会 ([OASIS](../Page/OASIS_\(組織\).md "wikilink"))\[1\]、[国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") (ISO) / [国際電気標準会議](../Page/国際電気標準会議.md "wikilink") (IEC)\[2\]および[日本産業規格](../Page/日本産業規格.md "wikilink") (**JIS X 4401**:2014)\[3\]、[韓国工業規格](../Page/大韓民国.md "wikilink")\[4\]、[ブラジル](https://ja.wikipedia.org/wiki/ブラジル "wikilink")\[5\]、[南アフリカ](https://ja.wikipedia.org/wiki/南アフリカ共和国 "wikilink")\[6\]の標準規格に認定されている。 競合国際規格として、「[ISO/IEC 29500:Office Open XML(OpenXML, OOXML)](../Page/Office_Open_XML.md "wikilink") 」がある。

## 仕様

ODFは、複数のXMLファイルを[ZIP形式で](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")[データ圧縮](../Page/データ圧縮.md "wikilink")したファイルである。一つの規格でありながら、[テキスト](https://ja.wikipedia.org/wiki/ワープロ "wikilink")、[表計算](../Page/表計算ソフト.md "wikilink")（スプレッドシート）、[プレゼンテーション](../Page/プレゼンテーション.md "wikilink")の他、[数式](../Page/数式.md "wikilink")、[グラフィックドキュメント](../Page/画像.md "wikilink")、[データベース](../Page/データベース.md "wikilink")の各形式をサポートしている。

[多言語](../Page/多言語.md "wikilink")対応となっており、仕様上は、文章・段落・文字列について、各々「[言語](../Page/言語.md "wikilink")」及び「[国](../Page/国.md "wikilink")又は地域」を指定できるようになっている。

データの記述方法とその（画面上および紙上での）表現方法については一定の規格があるが、詳細な表現方法については各アプリケーションに依存している。そのため、閲覧する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")やアプリケーションによって、表示される結果が異なることがある。しかし最近ではソフト間の対応によって、これらの問題は改善されつつある。

ODFファイルの中身となっているXMLファイルはそれぞれ次のような内容となっている。

  -  : テキストコンテンツ
     : メタ情報。
     : 設定情報
     : テキストのスタイル情報
     : XMLファイルの構造
     : サムネイル画像（必須ではない）

## ファイルの種類

| ファイルの種類    | 拡張形式                                             | MIMEタイプ                                                                                     | ODF仕様     |
| ---------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------- | --------- |
| ワープロ       | <span style="font-family:monospace;">.odt</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.text</span>         | 1.0-      |
| 表計算        | <span style="font-family:monospace;">.ods</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.spreadsheet</span>  | 1.0-      |
| プレゼンテーション  | <span style="font-family:monospace;">.odp</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.presentation</span> | 1.0-      |
| 図形         | <span style="font-family:monospace;">.odg</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.graphics</span>     | 1.0-      |
| グラフ        | <span style="font-family:monospace;">.odc</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.chart</span>        | 1.0-      |
| 数式         | <span style="font-family:monospace;">.odf</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.formula</span>      | 1.0-      |
| イメージ       | <span style="font-family:monospace;">.odi</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.image</span>        | 1.0-      |
| マスタードキュメント | <span style="font-family:monospace;">.odm</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.text-master</span>  | 1.0-      |
| データベース     | <span style="font-family:monospace;">.odb</span> | <span style="font-family:monospace;">application/vnd.oasis.opendocument.base</span>         | 1.2-\[7\] |

## バージョン

  - [OpenDocument 1.0](http://docs.oasis-open.org/office/v1.0/OpenDocument-v1.0-os.pdf)
      - OpenDocument 1.0 は[2005年](../Page/2005年.md "wikilink")5月1日にOASIS標準規格として承認された規格である。
  - [OpenDocument 1.0 (second edition)](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43485)
      - OpenDocument 1.0 (Second edition)は、2006年5月1日にISO/IEC 26300:2006 として公開された規格である。これは[OASISによる](../Page/OASIS_\(組織\).md "wikilink") Committee Specification を含み、JTC1 ballot のコメントを検討した上で、編集上の修正がなされたものである。国際規格化されたことに伴い、2007年に韓国工業規格 KS X ISO IEC 26300、2008年にブラジルABNT NBR ISO/IEC 26300、南アフリカSANS 26300 の各国で相次いで規格化された。日本に於いては、2010年にとして規格化された。
  - [OpenDocument 1.1](http://docs.oasis-open.org/office/v1.1/OS/OpenDocument-v1.1.pdf)
      - OpenDocument 1.1 は[2006年](../Page/2006年.md "wikilink")10月19日にOASISにより策定された規格である。アクセシビリティの観点から諸機能が追加された\[8\]。また、"The Open Document Format for Office Applications (OpenDocument) Specification"の バージョン1.1が、[2007年](../Page/2007年.md "wikilink")1月16日に行われた投票の結果、OASIS標準規格として2月1日に承認された\[9\]\[10\]。このことは2007年2月13日に公式に発表された\[11\]。この規格は、2012年3月8日に ISO/IEC 26300:2006/Amd 1:2012 - Open Document Format for Office Applications (OpenDocument) v1.1として公開された。\[12\]\[13\]
  - OpenDocument 1.2
      - OpenDocument 1.2 は2011年10月5日にOASIS標準規格として承認された規格である。[RDFベースの](../Page/Resource_Description_Framework.md "wikilink")[メタデータ](../Page/メタデータ.md "wikilink")、[OpenFormula](../Page/OpenFormula.md "wikilink")に基づく[スプレッドシートの計算式等の標準化などが行われた](../Page/表計算ソフト.md "wikilink")\[14\]。この規格は2015年6月17日に ISO/IEC 26300:2015として公開された。\[15\]\[16\]\[17\]

## 経緯

一般にプロプライエタリなフォーマットでは、そのプロプライエタリさを支えている「ライセンス」の文言上の禁止事項により以下のような問題点があることが極めて多い（著作権法上、そのような禁止事項にどのような法理があるのかはともかく）。

  - 互換性が無い
    複数のデータ形式は互換性がない。特定の製品で作成したデータは、基本的に他社の製品では使用することができない。
  - 仕様が非公開
    データ形式は公開されていないため、第三者が相互変換のためのツールを作成するなどの対策を行うことや対応するシステムを開発することは困難である。

このことは、既に広く使われている製品を選択せざるを得ない状況を生み、特定製品に依存するシステムを生むため、営業戦略において効果的であった。実際、[MS-DOS](../Page/MS-DOS.md "wikilink")全盛時代において表計算ソフト[Lotus 1-2-3](../Page/Lotus_1-2-3.md "wikilink")、日本国内でワープロソフト[一太郎](../Page/一太郎.md "wikilink")を普及させ、[Windows全盛期においてはオフィススイート製品の分野において](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Microsoft Officeの独占に近い状態をもたらした一因ともなっている](../Page/Microsoft_Office.md "wikilink")。

このように、特定ベンダによって独占されたファイル形式に依存すること（[ベンダロックイン](https://ja.wikipedia.org/wiki/ベンダロックイン "wikilink")）は、コンピュータの環境が変わると過去のドキュメントの参照や編集ができなくなるなど、知的資産としてのドキュメントの存在意義を低下させる上に、電子文書の活用を妨げるものでもあった。

また、Microsoft Officeが提供されていない[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")（[Linux](../Page/Linux.md "wikilink")など）の普及に伴い、Microsoft Officeとデータを交換できるオフィススイート向けファイル形式も必要とされていた。

要するに情報化社会において、（法学的にはともかく）コンプライアンスを遵守しライセンスに従わなければならないならば、プロプライエタリなフォーマットで作られたデータは、サポートの終了などによりゴミになってしまうか、ライセンス違反を犯すか、という多大なリスクとなっていた。

よって、特定ベンダに独占されないオープンなファイル形式（[オープンフォーマット](../Page/オープンフォーマット.md "wikilink")）の要求、オフィススイート共通のドキュメントファイル形式を策定する動きが起こり、特定のベンダーに依存しないオフィススイートのためのファイル形式として、[OASISのオフィス文書のためのオープン文書形式技術委員会によって策定された](../Page/OASIS_\(組織\).md "wikilink")。なお、策定開始時の仕様は、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が「OpenOffice.org」のファイル形式をもとに作成したものである。

## 反応

### 支持団体

OpenDocumentは、一部の公共団体、企業とソフトウェア製品から支持されている。

  - [OpenDocument Format Alliance](../Page/OpenDocument_Format_Alliance.md "wikilink")
      - [IBM](../Page/IBM.md "wikilink")、[Google](../Page/Google.md "wikilink")、[コーレル](../Page/コーレル.md "wikilink")、[アメリカ図書館協会](https://ja.wikipedia.org/wiki/アメリカ図書館協会 "wikilink")、[ジャストシステム](../Page/ジャストシステム.md "wikilink")など、600以上の企業・団体が普及促進\[18\]
  - OASIS ODF Adoption Committee
      - インド政府の国立情報センター、オランダの税関管理局ほか
  - 日本Open Source Office Suites & OpenDocument Format利用推進グループ（ODPG）\[19\]\[20\]
      - [アイコクアルファ](https://ja.wikipedia.org/wiki/アイコクアルファ "wikilink")株式会社、[会津若松市](https://ja.wikipedia.org/wiki/会津若松市 "wikilink")、株式会社[アシスト](../Page/アシスト_\(ソフトウェア会社\).md "wikilink")、[エヌ・ティ・ティ・コムウェア株式会社](../Page/NTTコムウェア.md "wikilink")、クリオン株式会社、株式会社コミューチュア情報システム、三洋機工株式会社、[住友電気工業](../Page/住友電気工業.md "wikilink")株式会社、[住友電工情報システム](../Page/住友電工情報システム.md "wikilink")株式会社ほか
  - [アップル](../Page/アップル_\(企業\).md "wikilink")、 [アドビシステムズ](../Page/アドビシステムズ.md "wikilink")、 [Google](../Page/Google.md "wikilink")、 [IBM](../Page/IBM.md "wikilink")、 [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")、 [マイクロソフト](../Page/マイクロソフト.md "wikilink")、 [ノキア](../Page/ノキア.md "wikilink")、 [ノベル](../Page/ノベル_\(企業\).md "wikilink")、 [レッドハット](../Page/レッドハット.md "wikilink")、 [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink") 、[カノニカル](https://ja.wikipedia.org/wiki/カノニカル "wikilink")などのIT企業
  - オープンソースオフィスソフト [LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")、 [Apache OpenOffice](https://ja.wikipedia.org/wiki/Apache_OpenOffice "wikilink") 、 [KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink") などが標準ファイル形式として採用、普及促進をしている。
  - OpenDoc Society

### 採用

| 組織                | 採用時期       | unsortable|備考                                                                                                                                                                        |
| ----------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 国土交通省（日本）         | 2007年      | 2007年頃から申請書などでODF形式を採用\[21\]                                                                                                                                                         |
| マサチューセッツ州政府（アメリカ） | 2007年1月1日  | 2005年9月2日に米国[マサチューセッツ州](../Page/マサチューセッツ州.md "wikilink")が2007年1月1日以降の同州の公文書のフォーマットをODFとする方針を発表した。その後、担当者の辞任等が相次ぎ、2007年8月1日、マサチューセッツ州は、ODFに加えOOXMLを同州の公文書フォーマットの一つとして追加採用する方針を発表している。 |
| マレーシア政府           | 2007年8月    | 2007年8月、ODF形式をマレーシアの公共機関で採用する計画を発表\[22\]                                                                                                                                             |
| ベルギー政府            | 2007年9月    | ベルギー政府は、2007年9月から連邦政府全省庁でODFの可読を義務化、2008年9月からODF を文書交換用ファイル形式として採用した\[23\]。                                                                                                          |
| 会津若松市役所（日本）       | 2008年8月    | 2008年8月より[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")を標準ソフトとして840台に導入し、ODF形式を標準フォーマットとして採用した\[24\]。                                                                        |
| 交野市役所（日本）         | 2010年7月    | Microsoft Office 2007ならびに2010年7月から[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")を標準ソフトとして導入し、ODF形式を標準フォーマットとして採用した\[25\]。                                                    |
| 経済産業省（日本）         | 2011年      | 2011年ごろから一部調達仕様により、ISO 26300(ODF)形式により保存したファイルの納品を要求\[26\]。                                                                                                                          |
| 徳島県庁（日本）          | 2011年7月1日  | 2011年7月1日から[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")を標準ソフトと位置付け約4,000台に導入し、ODF形式を標準フォーマットとして採用した\[27\]。                                                                 |
| JA福岡              | 2011年12月6日 | 2011年12月6日から[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")を標準ソフトとして約400台に導入、ODFを標準フォーマットとして採用した\[28\]。                                                          |
| 甲賀市役所（日本）         | 2012年4月    | 2012年4月ごろより[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")を導入。ODFを標準フォーマットとして採用 \[29\]                                                                           |
| ポルトガル政府           | 2012年11月   | ポルトガル政府は、2012年11月、ODF形式を採用\[30\]                                                                                                                                                     |
| イギリス政府            | 2014年6月    | イギリス政府は、2014年6月、政府が利用する外部交換用文書形式としてODF採用を発表 \[31\]                                                                                                                                   |
| 台湾中央政府            | 2015年6月    | 2015年6月、台湾中央政府は政府の利用する文書形式としてODFの利用を発表。自治体や企業にODFの利用を呼びかける。\[32\]\[33\]\[34\]                                                                                                        |
| イタリア国防省           | 2015年9月    | イタリア国防省は使用するオフィスソフトをLibreOfficeに移行し、省内で利用する文書形式にODFを採用。\[35\]                                                                                                                        |
| フランス政府            | 2015年7月    | 2015年7月、フランス政府は政府内で利用する文書形式としてODFの利用を確認。[OOXMLの利用は却下された](../Page/Office_Open_XML.md "wikilink")。\[36\]                                                                               |
| 北大西洋条約機構          |            | 義務的な利用\[37\]                                                                                                                                                                         |

### アプリケーションソフトウェアの対応

  - [The Document Foundation](https://ja.wikipedia.org/wiki/The_Document_Foundation "wikilink")
    [LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink") は、ODFを標準ファイル形式として採用している。
  - [Apacheソフトウェア財団](../Page/Apacheソフトウェア財団.md "wikilink")
    [Apache OpenOfficeは](https://ja.wikipedia.org/wiki/Apache_OpenOffice "wikilink")、 ODFを標準ファイル形式として採用している。
  - [ジャストシステム](../Page/ジャストシステム.md "wikilink")
    [一太郎](../Page/一太郎.md "wikilink") 2006、[花子](../Page/花子_\(グラフィックソフト\).md "wikilink") 2007も追加モジュール（一太郎は2006年[9月](../Page/9月.md "wikilink")、花子は2007年[2月](https://ja.wikipedia.org/wiki/2月 "wikilink")リリース）によってODFの入出力に対応した。また、[三四郎](../Page/三四郎_\(表計算ソフト\).md "wikilink") 2008、[Agree](https://ja.wikipedia.org/wiki/Agree "wikilink") 2008では2008年10月リリースの修正プログラムを適用することで対応する。4製品ともその後のバージョンでは標準で対応している。
  - マイクロソフト
    [2009年](../Page/2009年.md "wikilink")に「2007 Office system Service Pack 2 (SP2)」をリリースし、[Word](../Page/Microsoft_Word.md "wikilink")、[Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[PowerPointでODFの読み込み](../Page/Microsoft_PowerPoint.md "wikilink")、保存に対応した\[38\]。また、Windows 7付属の[ワードパッド](../Page/ワードパッド.md "wikilink")でも対応した\[39\]。

### 批判

  - OASIS ODF 1.0、1.1、ISO/IEC 26300:2006 では、表計算の数式言語、構文、関数が明確に定義されていない\[40\]\[41\]。
  - OASIS ODF 1.0、1.1、ISO/IEC 26300:2006 では、電子署名が定義されていない\[42\]。

## 脚注

## 参考文献

  -
## 関連項目

  - [オープンフォーマット](../Page/オープンフォーマット.md "wikilink")
  - [OpenDocument Format Alliance](../Page/OpenDocument_Format_Alliance.md "wikilink")
  - [国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")
  - [OASIS](../Page/OASIS_\(組織\).md "wikilink")（構造化情報標準促進協会）
  - [Office Open XML (OpenXML, OOXML)](../Page/Office_Open_XML.md "wikilink")
  - [Compound Document Format (CDF)](../Page/Compound_Document_Format.md "wikilink")
  - [オフィススイートの比較](../Page/オフィススイートの比較.md "wikilink")
  - [Uniform Office Format](../Page/Uniform_Office_Format.md "wikilink")

## 外部リンク

  -
  - [OASIS OpenDocument](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)

  -
  -
[Category:OpenDocument](https://ja.wikipedia.org/wiki/Category:OpenDocument "wikilink") [Category:オフィスソフト](https://ja.wikipedia.org/wiki/Category:オフィスソフト "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.  [OpenDocument Format for Office Applications (OpenDocument) v1.0](http://www.oasis-open.org/specs/index.php#opendocumentv1.0)
2.  [ISO/IEC 26300:2006 Information technology -- Open Document Format for Office Applications (OpenDocument) v1.0](http://www.iso.org/iso/en/CatalogueDetailPage.CatalogueDetail?CSNUMBER=43485&ICS1=35&ICS2=240&ICS3=30)
3.
4.  <http://www.standard.go.kr/CODE02/USER/0B/03/SerKS_View.asp?ks_no=KSXISOIEC26300&OlapCode=STAU020201> KSXISOIEC26300:Information technology - Open Document Format for Office Applications:(OpenDocument) v1.0
5.  [ABNT Catalogo](https://www.abntcatalogo.com.br/norma.aspx?ID=1549)：ABNT NBR ISO/IEC 26300:2008:Information technology - Open document format for office aplications (OpenDocument) v1.0
6.  <https://www.sabs.co.za/content/uploads/files/SANS26300%28colour%29.pdf> SANS 26300 Information technology - Open technology - Open Document Format for Office Applications (OpenDocument) v1.0
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19. [ODPG](http://odpg.org/) 2014年4月1日閲覧。
20. [c71210710583b702b0a4c4e8d49fe578.pdf](http://prtimes.jp/data/corp/666/c71210710583b702b0a4c4e8d49fe578.pdf)：日本 OpenOffice.org & OpenDocument Format 利用推進グループを設立 ～　企業・団体での利用促進を目指すとともに、国内のコミュニティ活動を支援　～
21. [建設産業・不動産業：関連書類ダウンロード](http://www.mlit.go.jp/totikensangyo/const/1_6_bt_000233.html) - 国土交通省
22. <http://www.zdnetasia.com/malaysia-formally-embraces-open-document-format-62030781.htm>
23. [Belgium adopts OpenDocument | Apps & wearables | Techworld](https://www.techworld.com/news/apps-wearables/belgium-adopts-opendocument-6335/)
24. <http://www.e-aizu.jp/ja/shisei/torikumi/ooo/>
25. <http://www.city.katano.osaka.jp/docs/2011082200248/>
26. <http://www.meti.go.jp/information_2/downloadfiles/2012032113420107.pdf>
27. <http://www.pref.tokushima.jp/docs/2011080900034/files/siryou1.pdf>
28.
29. <https://web.archive.org/web/20170420111412/http://www.city.koka.lg.jp/item/10035.htm>
30. [0646006465.pdf](https://dre.pt/application/dir/pdf1sdip/2012/11/21600/0646006465.pdf)
31. [Open document formats selected to meet user needs - GOV.UK](https://www.gov.uk/government/news/open-document-formats-selected-to-meet-user-needs)
32. [國家發展委員會-推動ODF-CNS15251為政府文件標準格式](https://www.ndc.gov.tw/cp.aspx?n=D6D0A9E658098CA2&s=CDA642B408087E65)
33. [台湾で進行するLibreOffice導入、「完全移行を強いないのがコツ」 | 日経 xTECH（クロステック）](http://itpro.nikkeibp.co.jp/atcl/column/14/090100053/122200217/)
34. [簡報_slat](https://wiki.documentfoundation.org/images/d/d9/LibreOffice_ODF_Migration_in_Taiwan.Japanese.pdf)：台湾における LibreOffice/ODF への移行
35. [Italian military to switch to… | Joinup](https://joinup.ec.europa.eu/news/italian-military-switch)
36. [French Government IT Directorate Stands Its Ground : ODF Supported, OOXML Rejected | April](https://www.april.org/en/french-government-it-directorate-stands-its-ground-odf-supported-ooxml-rejected)
37. <http://nhqc3s.nato.int/architecture/_docs/NISPv2/volume2/ch03s04.html>
38.
39. <http://windows.microsoft.com/ja-JP/windows7/Using-WordPad>
40.
41.
42.