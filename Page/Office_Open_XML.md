> この記事は[Office Open XML](https://ja.wikipedia.org/wiki/Office_Open_XML)から翻訳されています。


とは、[XMLをベースとした](../Page/Extensible_Markup_Language.md "wikilink")[オフィススイート](../Page/オフィススイート.md "wikilink")用の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")である。

2006年12月に  により ECMA-376\[1\]として[標準化](../Page/標準化.md "wikilink")され、2008年4月には[ISOと](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")[IECの合同技術委員会](../Page/国際電気標準会議.md "wikilink") [ISO/IEC JTC 1の副委員会](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")[SC 34において](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1/SC_34 "wikilink")、ISO/IEC 29500として標準化された。競合国際規格として「」がある。

## 概要

はデータを格納するにあたり独自の[バイナリ](../Page/バイナリ.md "wikilink")形式を用いてきたが、バージョン12（ 2007）からは、[XMLで記述された規格を標準ファイル形式として採用した](../Page/Extensible_Markup_Language.md "wikilink")。それが である。

XMLで記述された文書群と画像などの[バイナリ](../Page/バイナリ.md "wikilink")データをオープン・パッケージング・コンベンションズ\[2\]によりひとつのファイルに集成した構造となっている。なお、オープン・パッケージング・コンベンションズは[zipが使用されている](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")。

従来使われている .doc、.xls、.ppt 形式とのバイナリ互換性はない。また[マクロを含む文書は拡張子の末尾は](../Page/マクロ_\(コンピュータ用語\).md "wikilink") .docm、.xlsm、.pptm である。

を標準フォーマットとして採用することで

  - をインストールされていない環境でもファイルの読み書きが可能

  - パーツの再利用が容易になる

  - パーツに分けることによりファイル破損のリスクを限定する事ができる

  - zip圧縮されることでファイルサイズが小さくなる

といったメリットが期待される 。

## 仕様

Office Open XMLに基づいて作られたファイルは複数のXMLファイルから成り立っており、これらをzipで圧縮することにより1つの文書としている。これをOffice Open XMLではパッケージと呼んでいる。

例えば  の .docx ファイルをZIP形式のファイルとして展開すると、以下のようなパーツから成り立っていることが分かる。

  - document.xml
    テキストコンテンツ
  - fontTable.xml
    フォント表
  - settings.xml
    設定情報
  - styles.xml
    テキストのスタイル情報
  - webSettings.xml
    ウェブ用のスタイル情報
  - media
    画像などのメディアファイルを格納するフォルダ
  - _rels
    各パーツの関連性（リレーションシップ）を記述するファイルを格納するフォルダ

個々のXMLファイルやフォルダーをどのように設置するかは[Open Packaging Conventions](https://ja.wikipedia.org/wiki/Open_Packaging_Conventions "wikilink") ([en](https://ja.wikipedia.org/wiki/w:Open_Packaging_Conventions "wikilink"))と呼ばれる方法で定められている\[3\]。また、以下のような専用のマークアップ言語を用いてデータは表現される。

  - PresentationML : PowerPointなどプレゼンテーションのデータを記述するための言語。
    [SpreadsheetML](https://ja.wikipedia.org/wiki/Office_Open_XML_ファイルフォーマット#SpreadsheetML_.28SML.29 "wikilink") : Excelなど表計算のデータを記述するための言語。ワークブックの下に複数のワークシートが連なるという形で構成される。
    [WordprocessingML](https://ja.wikipedia.org/wiki/Office_Open_XML_ファイルフォーマット#WordprocessingML_.28WML.29 "wikilink") : Wordなど文書を記述するための言語。本文を記述するメインドキュメントと、脚注やスタイルデータなどのパーツドキュメントなどから成る。
    [DrawingML](https://ja.wikipedia.org/wiki/Office_Open_XML_ファイルフォーマット#DrawingML "wikilink") : 図形や画像などを記述・格納するための言語。
    [MathML](https://ja.wikipedia.org/wiki/Office_Open_XML_ファイルフォーマット#Office_MathML "wikilink") : 数式を記述するための言語。

### 仕様書

#### ISO/IEC 29500:2008

ISO/IEC 29500の仕様書は以下の4つのパートで構成され、それぞれ独立した規格である。

例として、2008年版の構成は以下の通り。

  - Part 1 (Fundamentals and Markup Language Reference)
    This part has 5560 pages. It contains:
  - Part 2 (Open Packaging Conventions)
    This part has 129 pages. It contains:
  - Part 3 (Markup Compatibility and Extensibility)
    This part has 40 pages. It contains:
  - Part 4 (Transitional Migration Features)
    This part has 1464 pages. It contains:

2012年版は一部がオンラインで閲覧できる\[4\]\[5\]。

  -
    完全版は購入する必要がある。

## 拡張子

| ファイルの種類   | 拡張形式  | MIMEタイプ                                                                   | OOXML仕様 |
| --------- | ----- | ------------------------------------------------------------------------- | ------- |
| ワープロ      | .docx | application/vnd.openxmlformats-officedocument.wordprocessingml.document   |         |
| 表計算       | .xlsx | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet         |         |
| プレゼンテーション | .pptx | application/vnd.openxmlformats-officedocument.presentationml.presentation |         |

## バージョン

は、仕様の厳密さを重視した**ストリクト**\[6\]と過去との互換性を重視した**トランジショナル**\[7\]の2種類を規定したファイルフォーマット仕様である。

  - 第一版
    2006年12月ににより、ECMA-376として発行された初版である。
  - 第二版
    2008年12月にから発行された。
  - 第三版
    2011年6月にから発行された。
  - 第四版
    2012年12月にから発行された。

## アプリケーションの対応

  - マイクロソフト
    マイクロソフトは、 2007 で、ECMA-37 第一版の読み書きに対応し、標準ファイル形式として採用した。 2010 では ECMA-37 第二版の読み書きに対応し標準ファイル形式として採用するとともに、ISO/IEC 29500 のトランジョショナルの読み書き、ISO/IEC 29500のストリクトの読み取りに対応した\[8\]。 付属のワードパッドでも、競合規格である  と共に対応した。また、旧バージョンである  2000、XP、2003 で読み書きをするための互換パックを開発し、無償配布している\[9\]。

  -

    は、 3で読み込みに対応した。

  -

    は、 3.4で OOXML の読み書きに対応した。

  - オフィススイート

    以外の多くの[オフィススイート](../Page/オフィススイート.md "wikilink")は  を開き、加工するまでは可能となっている（保存は  形式などで行う）。ただし2012年現在、日本語パソコン環境で  形式で**保存**まで可能なのは[Kingsoft Office](https://ja.wikipedia.org/wiki/Kingsoft_Office "wikilink")\[[https://www.kingsoft.jp/kingsoft-office/20160218.html\]と](https://www.kingsoft.jp/kingsoft-office/20160218.html%5Dと) のみである（詳しくは「[オフィススイートの比較](../Page/オフィススイートの比較.md "wikilink")」を参照のこと）。

## 昨今の動向

は2006年12月には  の標準規格 ECMA-376 として承認され、ISO の承認へと作業が続けられた。しかし、日本においては政府は[中央省庁](https://ja.wikipedia.org/wiki/中央省庁 "wikilink")で2007年夏より調達するソフトに対しソフトウェアが扱う文書やデータが[国際規格もしくは](https://ja.wikipedia.org/wiki/工業規格#国際規格 "wikilink")[日本工業規格](https://ja.wikipedia.org/wiki/日本工業規格 "wikilink")に準拠していることを調達の原則条件とすることを決定しており\[10\]、Microsoft Office製品は対象外となる可能性があると懸念された。

2007年7月1日にはNHKが上記の考え方に基づき、「国が今後、マイクロソフトの  や  を購入できなくなる」という報道を行った。

これに対して総務省は7月2日の定例会見において資料を配布し、「オープンな標準は、国際規格 (ISO) や日本工業規格 (JIS) だけではなく、その他の公的規格や業界団体による規格も含まれる概念であるため、国際規格 (ISO) や日本工業規格 (JIS) に該当していない製品等がただちに排除されるという理解は誤りです」とNHK報道は誤りであると反論した。この時点で  は、[標準化団体](../Page/標準化団体.md "wikilink")の  によって「ECMA-376」として標準化されており、総務省の言う「その他の公的規格」に該当する。

さらに総務省は、「加えて、政府調達の基本指針では、調達仕様書の要求要件として、 オープンな標準を優先して記載するということのみを定めており、オープンな標準に準拠した製品等を提案として求めるにとどまるものであって、提案された製品等を調達するか否かは、その他の要求要件とも照らし合わせて総合的に評価し決定されるものであることから、そのプロセスを経ずに『原則として、ワードやエクセルを購入できなくなる』ということはありません」と述べた。

アメリカ合衆国[マサチューセッツ州](../Page/マサチューセッツ州.md "wikilink")が州政府の標準文書としてODFを採用するなどの動きに対応するため、マイクロソフトは「」プロジェクトを立ち上げ、2007  用のODF対応[プラグイン](../Page/プラグイン.md "wikilink")モジュール開発を進めた\[11\]。2008年4月には  もISO承認を得て、マイクロソフトは勝利宣言を出した\[12\]\[13\]。その一方で、マイクロソフトは6月にODFフォーマットに対応する意向を示し\[14\]、 文書の相互運用性向上を進めるべくODFを策定する[構造化情報標準促進協会のオフィス文書のためのオープン文書形式技術委員会に参加](../Page/OASIS_\(組織\).md "wikilink")、[2009年](../Page/2009年.md "wikilink")には 2007  で正式にODFフォーマットの読み込みと保存に対応した\[15\]。ただし、ODFの再現性はあまり高くない\[16\]。

## 批判

に類似する規格としてODFが存在する。どちらもXML形式の規格であるが、互換性はない。ODFを推進する[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")をはじめとする諸団体は[マイクロソフト](../Page/マイクロソフト.md "wikilink")による市場の寡占に反対する立場から、「 は[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")ではない」「マイクロソフトの圧倒的なシェアを利用した暴力」だと主張して  に強く反対した。 のISO標準化の際には、両陣営の間で激しい応酬が繰り広げられた\[17\]。

ちなみにクロスプラットフォームについては、2012年2月現在、 を閲覧、編集できるオフィススイートが現れているが、 のまま保存できるオフィススイートは少ない。また、マイクロソフト側は上記の通りODFへの対応を行っている。

## 脚注

## 参考文献

  - Girier陽子/高山佳文/森本孝司 著 大須賀昭彦 監修 『入門 Office Open XML』 ISBN 978-4-7973-3872-0
  - アンテナハウス株式会社 XSL Formatter グループ 著 『Office Open XML Formats 入門』 ISBN 978-4-8399-2582-6
  - [ISO/IEC 29500-3:2012(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:29500:-3:ed-3:v1:en)

## 関連項目

  - [国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")
  - [オフィススイートの比較](../Page/オフィススイートの比較.md "wikilink")
      -
      -
## 外部リンク

  - \[<http://msdn.microsoft.com/ja-jp/library/aa338205(office.12>).aspx  (2007)  ファイル形式の概要\]
  - [](http://www.ecma-international.org/publications/standards/Ecma-376.htm)
  - I[SO/IEC 29500-2:2012(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:29500:-2:ed-3:v1:en)
  - [ISO/IEC 29500-3:2012(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:29500:-3:ed-3:v1:en)

[Category:Ecma](https://ja.wikipedia.org/wiki/Category:Ecma "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:Microsoft_Office](https://ja.wikipedia.org/wiki/Category:Microsoft_Office "wikilink") [Category:オープンコンテントプロジェクト](https://ja.wikipedia.org/wiki/Category:オープンコンテントプロジェクト "wikilink") [Category:オフィスソフト](https://ja.wikipedia.org/wiki/Category:オフィスソフト "wikilink") [Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.  [](http://www.ecma-international.org/publications/standards/Ecma-376.htm)
2.
3.  アンテナP.13
4.  [ISO/IEC 29500-2:2012(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:29500:-2:ed-3:v1:en) Information technology — Document description and processing languages — Office Open XML File Formats — Part 2: Open Packaging Conventions
5.  [ISO/IEC 29500-3:2012(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:29500:-3:ed-3:v1:en) Information technology — Document description and processing languages — Office Open XML File Formats — Part 3: Markup Compatibility and Extensibility
6.
7.
8.  <http://msdn.microsoft.com/ja-jp/library/gg607163.aspx>
9.
10.
11.
12.
13.
14.
15.
16. [1](http://office.microsoft.com/ja-jp/word-help/HA010281619.aspx)
17.