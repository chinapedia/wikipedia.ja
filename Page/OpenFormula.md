> この記事は[OpenFormula](https://ja.wikipedia.org/wiki/OpenFormula)から翻訳されています。


**OpenFormula (OpenDocument formula specification)** は、どの[スプレッドシートのユーザーでも](../Page/表計算ソフト.md "wikilink")、そのアプリケーションに制約されることなく数式を相互に運用することを可能にするために起案された[オープン標準](../Page/オープン標準.md "wikilink")に関する草案の名称である。同様にオープンな文書フォーマットである[OpenDocument](../Page/OpenDocument.md "wikilink") (ISO/IEC 26300) の追加草案。[オープンソース](../Page/オープンソース.md "wikilink")、[フリーウェア](../Page/フリーウェア.md "wikilink")の分野で知られているコンピューター科学者の[デイビット・A・ホイーラー](https://ja.wikipedia.org/wiki/デイビット・A・ホイーラー "wikilink") により提案された。

## 歴史

### OpenFormulaへの要求

OpenDocument 1.0が制定された当時の背景には、どのオフィススイートのユーザーであっても、互換性の問題なく文書ファイルを相互にやり取りすることへの要求があったが、表計算ソフトにおける数式の記述に関しても同様の要求がある。SUM関数のようなごく一般的な数式を除いては、各アプリケーションにより規定されている数式は異なっており、あるアプリケーションで作成されたスプレッドシートを別のアプリケーションで読み込むことは（出来なくないにせよ）、特殊な対応を行うことではじめて可能であった。そうした障害を避けるために構想されたのがOpenFormulaである。

OpenDocumentでは数式を扱う際に、[MathML](https://ja.wikipedia.org/wiki/MathML "wikilink")を利用しており、また、スプレッドシート上のデータ、フォーマット、テーブル等、表計算ソフト上で一般的に利用される情報をやり取りすることも可能である。OpenDocumentでは関数のような（スプレッドシートで計算された）数式は、table:formulaという形式を用いて表示される。

例えばODSファイルに含まれるcontent.xmlは、SUM関数を用いて計算した場合、office:body以下では次のようになる。

    <nowiki>
      <office:body>
       <office:spreadsheet>
        <table:table table:name="Table1" table:style-name="ta1" table:print="false">
         <office:forms form:automatic-focus="false" form:apply-design-mode="false"/>
         <table:table-column table:style-name="co1" table:number-columns-repeated="256" table:default-cell-style-name="ce1"/>
          <table:table-row table:style-name="ro1">
           <table:table-cell office:value-type="float" office:value="1">
            <text:p>1</text:p>
           </table:table-cell>
           <table:table-cell table:number-columns-repeated="255"/>
          </table:table-row>
          <table:table-row table:style-name="ro1">
           <table:table-cell office:value-type="float" office:value="2">
            <text:p>2</text:p>
           </table:table-cell>
           <table:table-cell table:number-columns-repeated="255"/>
          </table:table-row>
           <table:table-row table:style-name="ro1">
            <table:table-cell office:value-type="float" office:value="3">
            <text:p>3</text:p>
           </table:table-cell>
           <table:table-cell table:number-columns-repeated="255"/>
          </table:table-row>
          <table:table-row table:style-name="ro1">
           <table:table-cell office:value-type="float" office:value="3">
            <text:p>4</text:p>
           </table:table-cell>
           <table:table-cell table:number-columns-repeated="255"/>
          </table:table-row>
          <table:table-row table:style-name="ro1">
           <table:table-cell table:formula="oooc:=SUM([.A1:.A4])" office:value-type="float" office:value="10">
            <text:p>10</text:p>
           </table:table-cell>
           <table:table-cell table:number-columns-repeated="255"/>
          </table:table-row>
          <table:table-row table:style-name="ro1" table:number-rows-repeated="65530">
           <table:table-cell table:number-columns-repeated="256"/>
          </table:table-row>
          <table:table-row table:style-name="ro1">
          <table:table-cell table:number-columns-repeated="256"/>
         </table:table-row>
        </table:table>
       </office:spreadsheet>
      </office:body>
    </nowiki>

しかし、この table:formula の構文や意味論は十分に定義されていないとする声もある。OpenDocument 1.0においてスプレッドシートの数式は、例えば値域やSUM関数を指定する方法を表示するような、ごく単純な例のセットによってしか定義されておらず、それらの例について、構文や意味論を含めた上で、より詳細で正確な仕様が求められていると批判された\[1\]\[2\]\[3\]\[4\]。

当時、OpenDocumentの委員会は数式の相互運用性については気にかけておらず、「コメントは、スプレッドシートの、準拠的な実装をサポートするべき数式の文法に関してなされるものであり、確かに相互運用性はユーザーの利益となると思うが、これは目下の仕様の狙うところではないと信じる〔ママ〕。なぜなら、相互運用性は現在その仕様が記述するところのXMLフォーマットとは特に関係がないからである。技術委員会 (Technical Committee) は仕様に定義されている以上の相互運用性の規格の文書化に関して解決法を探ってゆくであろう。」とコメントした\[5\]。

一方では、仕様はそれほど明確でないが（特に数式は数十年の伝統に沿う傾向があるので）、またほとんどのスプレッドシートでは結局のところ普遍的に使われている数式はごくわずかしかない（例えばSUM関数）ため、仕様の意図は十分に明確であるとされることもある。ただ実際には、多くのディベロパーは[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")を「基準となる実装 」と見ている。なぜならOpenOffice.orgのソースコードは公開されていて、またXMLのアウトプットはバイナリデータと異なり、容易に調べることが出来るためである。オープン・スタンダードに沿ったやり方で機能の実装を行うことは、アプリケーションに渡って数式をやり取りする際に生じる多くの問題を解消するといえよう。

### OpenFormula プロジェクト

規格の草案作成はOpenDocumentの外部コメンターである ホイーラーにより始められた。彼の草案は2005年2月に公開され、これを機に表計算ソフトの様々な開発者が議論を始める。

2005年10月、ホイーラーは当初の草案とその後の開発者による議論に基づき、数式の仕様の草案を作成することを目的とし、[OpenDocument Fellowship](https://ja.wikipedia.org/wiki/OpenDocument_Fellowship "wikilink")（オープンドキュメント・フェローシップ）によるサポートの下で非公式プロジェクトを一般に向け開始する。プロジェクトは2006年1月までに膨大な量の仕様を開発し、その後各表計算ソフトウェア開発者は、彼ら独自の仕様を草案のそれに適合させる作業を開始した。

### OASIS Formula 分科委員会

2006年2月、[OASIS](https://ja.wikipedia.org/wiki/OASIS "wikilink")はホイーラーを委員長とする数式分科委員会を公式に設立した。議論の結果、OpenFormulaプロジェクトの文書を基にして作業を進めることとなった。同月、OASISは詳細なフレームワークと100を超える機能が定義された草案を作成した。

### Microsoft の反応

2005年、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が取り扱う[Microsoft Officeの現プログラムマネージャーであるブライアン](../Page/Microsoft_Office.md "wikilink")・ジョーンズは、OpenDocumentはスプレッドシートの数式を詳細に定義していないと述べた\[6\]が、当時競合していたマイクロソフトのプロプライエタリなXMLフォーマットもそのような詳細な仕様は数式に実装していなかったのもまた事実である\[7\]。

マイクロソフトは、OpenDocumentはスプレッドシートの数式のフォーマットを規定していないため、OpenDocumentを使うことは出来ないと繰り返してきたが、 結局OpenFormulaの最初のバージョンに1年3ヶ月遅れ、[OASIS](https://ja.wikipedia.org/wiki/OASIS "wikilink")が最初に提出した仕様の草案に3ヶ月遅れる形で、2006年5月にマイクロソフトもまたXMLフォーマットで数式を定義する作業を開始した。Microsoftはこれを[OpenXML](https://ja.wikipedia.org/wiki/OpenXML "wikilink")と呼んでいる。

## OpenFormula の特性

OpenFormulaの仕様と開発のプロセスを比較すると、OpenDocumentと重複する点があるが、再計算された数式フォーマットのそれと比較して多くの異なる特性がある。例えば、

  - さまざまな表計算ソフトの開発者によって開発されている：OpemFormulaは、[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")や[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[StarOffice](https://ja.wikipedia.org/wiki/StarOffice "wikilink")、[KDE](../Page/KDE.md "wikilink")の[KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink")や[Gnumeric](../Page/Gnumeric.md "wikilink")、[IBM](../Page/IBM.md "wikilink")の[Lotus 1-2-3](../Page/Lotus_1-2-3.md "wikilink")、[wikiCalc](https://ja.wikipedia.org/wiki/wikiCalc "wikilink")等の表計算ソフトウェアの開発者の代表者によって開発されている。
  - 経験豊富なユーザーによって開発されている：多くの経験豊富なユーザーが参加している。またこの開発グループにはユーザー・開発者に加えて数学者も参加している。
  - オープンな開発：グループの議論、そして週ごとのドラフトは誰でも入手可能。
  - 完全なオープン標準：仕様は、[ブルース・ペレンズ](../Page/ブルース・ペレンズ.md "wikilink")と[EUに承認され](https://ja.wikipedia.org/wiki/欧州連合 "wikilink")、最も広く受け入れられている「オープン・スタンダード」の定義に適合している。例えば、定義によるとその仕様は[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")と[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")の両方に実装することが可能であり、作業は単一のソフトウェアベンダーにより支配されるのではなく、合意に基づいて行われる。
  - 既にOpenFormulaの実装が行われ始めている：各アプリケーション開発者は、グループの開発に基づき既に各々のアプリケーションに変更を施している。
  - 集中的な開発：分科委員会はスプレッドシートの数式の標準化のみに集中して作業している。
  - 慌てない：OpenFormulaは2005年2月26日に公開された仕様に基づいており、異なるアプリケーションにおける研究の大部分もまたそうである。
  - 将来性：構文は将来に渡って通用するように構成されている。例えば、列には任意の数を指定することが可能であり、また任意の数を入力できる。
  - テストケースが埋め込まれている：OpenFormulaには、よく忘れられてしまうケースを含む仕様を確認する数多くのテストケースが含まれている。それらのケースには特殊なフォーマットが採用されていて、 ユーザーはテストアプリケーションのスプレッドシートから自動的に取り出したり置換したり出来る。Rob Weirによると「この特性により私たちは、自己テスト機能のある仕様を手に入れられ、労働力の削減とともに、ODF (OpenDocument Format) を用いた革新的機能をもまた手に入れることが出来るのである\[8\]。
  - 厳密な定義：上に挙げたテストケースにより、OpenFormulaはより厳密なものになる。さらに、OpenFormulaはそれぞれの関数を（プロトタイプとして）定義する。関数の定義は深く調べられ、例えば、YEARFRAC()は、注意深く調査され定義された「うるう年」において的確に作動する。
  - 誤りを指令しない：OpenFormulaの仕様は、単に規格にあるバグが含まれているというだけで、そのバグを実装することが求められないように記述されている。例えば、[Excel](https://ja.wikipedia.org/wiki/Excel "wikilink")は誤って1900年をうるう年としているが、少なくともExcelの規格（バージョン1.3）の草稿は、互換性のあるアプリケーションは同じエラーを*含まなければならない*としており、アプリケーションは1900年以前をサポートしてExcelを上回る機能を実装してはならないとされている。他の様々な独立した諸実装を比較することにより、OpenFormulaのグループ機能はアプリケーションに誤りがある場合にはそれを特定し、各ソフトウェアアプリケーションが過度に制限されないようにしている。
  - 様々なソースからの革新：OpenFormulaはExcelとOpenOffice.orgの諸関数、また、それらアプリケーションには含まれていないものの、Gnumericや[KSpread](https://ja.wikipedia.org/wiki/KSpread "wikilink")のような他の表計算ソフトに含まれている重要な関数をカバーしている。例えば、この規格には[DEMICAL](https://ja.wikipedia.org/wiki/DEMICAL "wikilink")や[BASE](https://ja.wikipedia.org/wiki/BASE "wikilink")関数が含まれており、これらの関数は異なるベース を扱う際には[BIN2DEC](https://ja.wikipedia.org/wiki/BIN2DEC "wikilink")等の関数よりも優れている。また、[BITAND](https://ja.wikipedia.org/wiki/BITAND "wikilink")のようなビット処理向けの関数も含まれている。これらのソースはExcel、OpenOffice.orgのCalc、StarOfficeのCalc、KOfficeのKspread、GNOMEのGnumeric、IBMのLotus 1-2-3、CorelのWordPerfect Suite Quattro Pro、wikiCalcやDocumentToGoのSheetToGoが含まれている。分科委員会は、世界中の様々な独立したアプリケーションのイノベーションを取り入れることにより、より包括的で優れた結果を出せるとしている。
  - 誰にでもイノベーションの余地がある：諸関数には、アプリケーションに固有の[名前空間](../Page/名前空間.md "wikilink")が規定されている。これにより、各表計算ソフトは、現在または未来におけるスタンダードな関数、もしくは他のアプリケーションにより定義されている関数に干渉することなく新機能を追加することが出来る。結果的に、他のアプリケーションに干渉することなく、表計算ソフトは各々で新しい関数を追加することが出来る。その新しい関数に関して合意が行われたならば、標準化は可能である。名前空間はインターネットのネームサービスに基づいており、例えば、ORG.OPENOFFICE.STYLEはOpenOffice.orgに固有の関数となる。
  - 国際化：この規格では、あらゆる人々が「.」を小数点に用いるとは見なされず、実際にはインターフェイスは一切強制されない。名付けられた表現は、その名称を各地域の文字セットを用いてもつことができる。
  - 部分集合のサポート：アプリケーションは部分集合もしくは包合集合を実装できる。ユーザーが混乱するのを防ぐため、様々な「グループ」が定義されていて、これによりユーザーは特定の機能セットを要求できる。

## OpenFormula グループ

OpenFormulaの重要な側面に、あらかじめ定義された「グループ」の処理セットを提供することが挙げられる。それらの内で最も重要なのは、小 (small)、中 (medium) そして大 (large) である。

  - 小グループには100強の関数が含まれており、その中には、[三角関数](../Page/三角関数.md "wikilink")、[データベース](../Page/データベース.md "wikilink")、[金融](../Page/金融.md "wikilink")と[統計](../Page/統計.md "wikilink")用の関数が含まれている。大半の表計算ドキュメントは、この小グループを実装しているアプリケーションによって処理することができる。少なくとも1つのPDA用のアプリケーション (SheetToGo) はこのレベルの処理能力を有し、wikiCalcは、特にOpenFormulaにより定義されたセットに適合させるためにこの小グループある関数を実装した。
  - 中グループは小グループで定義された関数に加え、約100以上の関数が加えられた。
  - 大グループは中グループで定義された関数に加え、約130以上の関数が加えられた。また複素数などにも対応している。

他にも、ユーザーが自身の必要性に基づき、特定のグループに適合する実装を要求するであろうと予測されている。

## 予想される完成時期

OpenFormulaは2006年から数回に渡り、公開時期を延期してきていたが、2007年の6月に、[品質保証](../Page/品質保証.md "wikilink") (QA) のレビューに提出する前にすべき4つのタスクが残っているというアナウンスがされた\[9\]。

また、この規格は作業中でありながらも、草稿の規格に従う必要のあるアプリケーションを修正することで既に多くの実装者が規格を実装していることに留意すべきである。草稿の大部分はいくらかに渡って変更されなかったため、多くの表計算ソフト開発者は既に草稿の規格の大部分を実装している。

## 脚注

<references />

## 関連項目

  - [オープンソース](../Page/オープンソース.md "wikilink")
  - [OpenDocument](../Page/OpenDocument.md "wikilink")
  - [スプレッドシート](https://ja.wikipedia.org/wiki/スプレッドシート "wikilink")
  - [OASIS](https://ja.wikipedia.org/wiki/OASIS "wikilink")
  - [OpenOffice.org](../Page/OpenOffice.org.md "wikilink")
  - [Excel](https://ja.wikipedia.org/wiki/Excel "wikilink")

## 外部リンク

  - [About OpenFormula](http://wiki.oasis-open.org/office/About_OpenFormula), OASISのWikiサイトにおけるOpemFormulaの概要
  - [OASIS OpenDocument Formula subcommitee](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office-formula), 規格開発を行っている分科委員会のウェブサイト
  - [OASIS' OpenFormula Wiki](http://wiki.oasis-open.org/office/About_OpenFormula)
  - [OpenDocument - Formula Public Documents](http://www.oasis-open.org/committees/documents.php?wg_abbrev=office-formula)

[Category:OpenDocument](https://ja.wikipedia.org/wiki/Category:OpenDocument "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.  <http://lists.oasis-open.org/archives/office-comment/200411/msg00000.html> - Proposal: More detailed specification for formulas, 2004年11月1日.
2.  <http://software.newsforge.com/software/05/09/09/192250.shtml?tid=93> - OpenDocument office suites lack formula compatibility, 2005年9月20日.
3.  <http://blogs.gnome.org/view/mortenw/2005/06/16/0> - OpenDocument for Spreadsheets, 2005年6月16日.
4.  <http://www.jroller.com/page/erAck?entry=opendocument_for_spreadsheets> - OpenDocument For Spreadsheets, 2005年6月23日.
5.  <http://lists.oasis-open.org/archives/office/200501/msg00004.html> - Open Office XML Format TC Meeting Minutes 10-Jan-05, 2006年1月14日.
6.  <http://blogs.msdn.com/brian_jones/archive/2005/10/04/477127.aspx> - Comments from Tim Bray on OpenDocument, 2005年10月4日.
7.  <http://sourceforge.net/mailarchive/forum.php?thread_name=436F9F71.10506%40dwheeler.com&forum_name=openformula-discuss> - FYI: Formulas not specified by Microsoft XML, either, 2005年11月7日.
8.  <http://www.robweir.com/blog/2006/08/follow-leader.html> - Follow the Leader, 2006年8月3日.
9.  <http://lists.oasis-open.org/archives/office-formula/200706/msg00000.html> - Who is on board?, 2007年6月7日.