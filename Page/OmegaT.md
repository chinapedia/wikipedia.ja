> この記事は[OmegaT](https://ja.wikipedia.org/wiki/OmegaT)から翻訳されています。


**OmegaT**は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で記述された[コンピュータ](../Page/コンピュータ.md "wikilink")[翻訳支援ツール](../Page/翻訳支援ツール.md "wikilink")である。2000年にKeith Godfreyにより開発され、現在はDidier Brielらにより開発が進められている、[自由に使える、改変できるソフトウェアである](../Page/フリーソフトウェア.md "wikilink")。

OmegaTはプロの翻訳者向けに開発されている。主な機能の特徴として、[正規表現](../Page/正規表現.md "wikilink")を用いたカスタマイズ可能な分節化、参考訳文としての参照や訳文の蓄積が可能な[翻訳メモリ](../Page/翻訳メモリ.md "wikilink")、用語集や辞書ファイルの参照、[Hunspellスペルチェック辞書を用いたインラインでの綴り確認機能などがある](https://ja.wikipedia.org/wiki/:en:Hunspell "wikilink")。

OmegaTは[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（98 SE以降）上で動作し\[1\]、Java 1.5を必要とする（3.0以降はJava 1.6）。27の言語環境で使用可能である。2010年の調査によると\[2\]、プロの翻訳家458人のうち、[Wordfast](https://ja.wikipedia.org/wiki/Wordfast "wikilink")、Deja Vu、MemoQユーザー数の1/3、また最も利用されている[Tradosユーザー数の](../Page/TRADOS.md "wikilink")1/8がOmegaTを使用している。

## 歴史

OmegaTは2000年にKeith Godfreyにより開発された。

当初はC++で記述されていたが、2001年2月\[3\]の最初のリリース版以降は、Javaで記述されている。この版では翻訳メモリに[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")な翻訳メモリ形式を用いており、整形されていない[テキストファイルとHTMLファイルの翻訳と](../Page/プレーンテキスト.md "wikilink")、ブロック単位の（つまり文単位でなく、段落単位の）分節化だけが可能であった。

## 開発とリリース

OmegaTソースコードの開発情報は[SourceForge.net](../Page/SourceForge.net.md "wikilink")上に公開されており、現在のプロジェクトマネージャーはDidier Brielである。他の多くの[オープンソース](../Page/オープンソース.md "wikilink")プロジェクトと同様、OmegaTの新バージョンは高い頻度でリリースされ、その都度いくつかのバグ修正や機能改善がなされている。完成した取扱説明書（ユーザーマニュアル）が含まれる通常版（Standard）と、説明書に未記載の新しい機能を含む開発版（latest）が存在する。\[4\]最新のソースコードはSourceForgeのコードレポジトリで入手可能である。\[5\]

## OmegaTのしくみ

OmegaTは、1つの翻訳作業ごとに、使用するファイル一式を含めたプロジェクトフォルダーを生成する。ユーザーは、未翻訳の原文文書をsourceフォルダーにコピーしておく。翻訳作業の最後には、翻訳されたファイルがtargetフォルダーに格納される。OmegaTは、原文文書にある翻訳可能な部分を、分節化した状態で、ユーザーが翻訳を入力する編集ウィンドウに表示する。

翻訳を開始する前に、既存の翻訳内容をtmフォルダーに、用語集をglossaryフォルダーに、StarDict形式の辞書をdictionaryフォルダーに置いておくこともできる。翻訳作業時に、OmegaTはこれらを自動的に参照する。

OmegaTは、いま翻訳している文章と、これまでの翻訳内容を自動的にチェックし、類似したものがあればそれを参考訳文ウィンドウに表示する。翻訳者はキーボードショートカットを使ってその内容を編集中の分節に挿入できる。あらかじめプロジェクトフォルダーに用語集と辞書ファイルを追加しておくと、OmegaTはその内容も参照する。Google Translateなどの機械翻訳の機能を有効にしておくと、随時、機械翻訳ウィンドウにその翻訳内容を表示する。

翻訳が終了すると、OmegaTがファイル一式の翻訳版を生成し、プロジェクト全体の現在の翻訳内容を[TMX](https://ja.wikipedia.org/wiki/TMX "wikilink")ファイルに出力する。このファイルは今後の翻訳に流用が可能であり、また必要であればOmegaTや他の翻訳支援ツールを使用している他の翻訳者と交換できる。

## OmegaTの機能

OmegaTは、他の主要な翻訳支援ツールと同等の機能を多く持っている。翻訳メモリの生成、その追加や出力、翻訳メモリに存在する参考訳文の参照、用語集の参照、参照ファイル中の一致検索機能などである。

OmegaTには、他の翻訳支援ツールが必ずしも持っていない機能もある。例えば：

  - 異なる形式を持った複数のファイルを同時に翻訳したり、複数の翻訳メモリの参照や、用語集や辞書の参照が可能（コンピューターのメモリ容量が許す限り）

<!-- end list -->

  - 対応するファイル形式について、拡張子やファイルのエンコーディングのカスタマイズが可能。多種類に対応した文書の形式ごとに、どの要素を翻訳するかどうかをユーザーが選択可能。（例えば、OpenOffice.org Writerファイルの場合、ブックマークを翻訳対象とするかどうか。またMicrosoft Office 2007/2010ファイルの場合、脚注を翻訳するかどうか。HTMLファイルの場合、imgタグのALT属性の代替文字列を翻訳するかどうかなど）サードパーティの翻訳メモリで使用される標準でない要素を、どのように扱うかも選択が可能

<!-- end list -->

  - OmegaTの分節化規則は正規表現に基づいている。分節化の設定は言語またはファイル形式ごとに行うことができ、逐次作成する分節化の設定の間で、設定内容を継承できる

<!-- end list -->

  - 編集ウィンドウでは、次の未翻訳の分節に直接移動できる。また、移動した分節履歴をさかのぼったり、くだったりすることができる。高機能なテキストエディタと同様、操作の取り消し、やり直し、文字列のコピーや貼り付け、大文字⇔小文字の変換も行える。すでに翻訳された分節について、原文をあわせて表示したままにしておくようにもできる。編集ウィンドウでは、Hunspellスペルチェック辞書によるインラインで綴り確認機能を使用したり、マウス操作によりその都度綴り確認を行うこともできる

<!-- end list -->

  - キーボードショートカットまたはマウス操作により、編集中の分節に参考訳文を挿入できる。参考訳文との一致率を色づけ表示ができ、それぞれの分節を翻訳した日時とユーザー名を表示できる。用語集ウィンドウに表示された内容は、マウス操作で編集ウィンドウに挿入できる。訳文入力行には、原文をコピーして入力するか、最も一致率の高い参考訳文を自動で挿入するかを選択できる

<!-- end list -->

  - 検索ウィンドウでは、検索対象として、現在のプロジェクトの原文、訳文に加え、他の翻訳メモリやファイルを選択できる。大文字と小文字の区別や、正規表現の使用も可能である。検索結果をダブルクリックするだけで、編集ウィンドウに直接その分節を表示できる

<!-- end list -->

  - 翻訳作業終了後に、ここには不用意なタグ編集の間違いを防ぐなどのため、タグ検証を実施できる。OmegaTは、翻訳開始前、または翻訳状況の確認用に、プロジェクトのファイルと翻訳メモリについての統計情報（翻訳済みまたは未翻訳の分節数、単語数など）を表示できる

<!-- end list -->

  - OmegaTは[Apertium](https://ja.wikipedia.org/wiki/Apertium "wikilink")、[Belazar](https://ja.wikipedia.org/wiki/Belazar "wikilink")、[Google Translate](https://ja.wikipedia.org/wiki/Google_Translate "wikilink")、Microsoft Translatorの機械翻訳結果を取得し、独立したウィンドウに表示できる

<!-- end list -->

  - OmegaTのユーザーインターフェースは、ウィンドウ構成をさまざまに設定できる。位置を動かしたり、各ウィンドウの最大化や最小化、タイル表示（重ならないよう並べて表示）、タブ表示が行える。OmegaTが起動すると「お手軽スタートガイド」と呼ばれる簡単なチュートリアルが表示される

## 対応する文書形式

いくつかのファイル形式であれば、OmegaTが直接翻訳できる。OmegaTはその拡張子でファイル形式を判断する。ファイルの拡張子と対応するエンコーディングは、デフォルトの設定に追記する形でカスタマイズが可能である。

整形された文書については、OmegaTは市販の他の翻訳支援ツールと同様、その整形情報をタグに変換することで処理できる。

### 翻訳が直接可能なファイル形式

OmegaTで直接翻訳することができるのは、以下の形式である：

| ファイル形式                                                                                                                                                                                                                                                               | ファイルの拡張子                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| 文書形式                                                                                                                                                                                                                                                                 |                           |
| [Unicode](../Page/Unicode.md "wikilink")を含むさまざまなエンコーディングでエンコードされたプレーンテキスト（Javaで扱える任意のテキスト形式）                                                                                                                                                                         | .txt, .txt1, .txt2, .utf8 |
| [HTML](https://ja.wikipedia.org/wiki/HTML "wikilink")または[XHTML](https://ja.wikipedia.org/wiki/XHTML "wikilink")                                                                                                                                                      | .html, .htm, .xhtml, .xht |
| [OpenDocument](../Page/OpenDocument.md "wikilink") (ODF)\[6\]、代表的な使用アプリは[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")、[StarOffice](https://ja.wikipedia.org/wiki/StarOffice "wikilink")、[OpenOffice.org](../Page/OpenOffice.org.md "wikilink") | .sx?, .st?, .od?, .ot?    |
| Microsoft [Office Open XML](../Page/Office_Open_XML.md "wikilink")                                                                                                                                                                                                   | .doc?, .xls?, .ppt?       |
| ヘルプとマニュアル                                                                                                                                                                                                                                                            | .xml, .hmxp               |
| HTMLヘルプコンパイラ                                                                                                                                                                                                                                                         | .hhc, .hhk                |
| [LaTeX](../Page/LaTeX.md "wikilink")                                                                                                                                                                                                                                 | .tex, .latex              |
| DokuWiki                                                                                                                                                                                                                                                             | .txt                      |
| [QuarkXPress](../Page/QuarkXPress.md "wikilink") 用 CopyFlow Gold                                                                                                                                                                                                     | .tag, .xtg                |
| [DocBook](../Page/DocBook.md "wikilink")                                                                                                                                                                                                                             | .xml, .dbk                |
| ローカリゼーションリソース形式                                                                                                                                                                                                                                                      |                           |
| Androidリソース                                                                                                                                                                                                                                                          | .xml                      |
| Java properties                                                                                                                                                                                                                                                      | .properties               |
| [TYPO3](../Page/TYPO3.md "wikilink") LocManager                                                                                                                                                                                                                      | .xml                      |
| Mozilla [DTD](../Page/Document_Type_Definition.md "wikilink")                                                                                                                                                                                                        | .dtd                      |
| Windowsリソース                                                                                                                                                                                                                                                          | .rc                       |
| [WiX](../Page/WiX.md "wikilink")ローカリゼーション                                                                                                                                                                                                                            | .wxl                      |
| ResX                                                                                                                                                                                                                                                                 | .resx                     |
| “キー=値” 形式で記述されたファイル                                                                                                                                                                                                                                                  | .ini, .lng                |
| 多言語ローカリゼーション形式                                                                                                                                                                                                                                                       |                           |
| [XLIFF](https://ja.wikipedia.org/wiki/XLIFF "wikilink")                                                                                                                                                                                                              | .xlf, .sdlxliff           |
| [Portable Object](../Page/Gettext.md "wikilink") (PO)                                                                                                                                                                                                                | .po, .pot                 |
| その他の形式                                                                                                                                                                                                                                                               |                           |
| SubRip字幕                                                                                                                                                                                                                                                             | .srt                      |
| SVG画像                                                                                                                                                                                                                                                                | .svg                      |
|                                                                                                                                                                                                                                                                      |                           |

### 間接的に翻訳可能なファイル形式

OmegaTが対応していない形式のファイルを扱うには、以下の2つの方法がある：

  - そのファイル拡張子を、適したファイルフィルター（通常はプレーンテキスト形式に準じたもの）に登録する
  - そのファイルを、OmegaTが直接翻訳が可能な形式に変換する

#### XLIFFによる対応

[Okapi FrameworkのRainbowを用いると](https://ja.wikipedia.org/wiki/Okapi_Framework "wikilink")、いくつかのファイル形式を、OmegaTが取り扱える[XLIFF](https://ja.wikipedia.org/wiki/XLIFF "wikilink")形式に変換できる。Rainbowであれば、そのような文書からOmegaTプロジェクトフォルダーを生成でき、OmegaT上でより取り扱いやすくなる。\[7\]

#### Gettext POによる対応

多くのファイル形式はGettext Portable Object (PO) ファイルに変換できる。POファイルはOmegaTで翻訳可能である。Debian Linux上で使用可能なpo4aは、[LaTeX](../Page/LaTeX.md "wikilink")や[TeX](../Page/TeX.md "wikilink")、[POD形式のファイルをGettext](../Page/Plain_Old_Documentation.md "wikilink") PO形式へ変換できるプログラムである。\[8\] [Translate Toolkitは](https://ja.wikipedia.org/wiki/Translate_Toolkit "wikilink")、Mozilla .propertiesやdtdファイル、CSVファイル、特定のQuickTime .tsファイルやXLIFFファイルを、Gettext PO形式に変換できる。

#### Office Open XMLまたはODFによる対応

バージョン97から2003までのMicrosoft Word、Excel,、PowerPoint文書ファイルは、Office Open XML形式（Microsoft Office 2007/2010）、またはODF（OpenOffice.org）形式に変換できる。完全に可逆な変換ではないため、形式情報が失われる可能性がある。

## 取り扱える翻訳メモリと用語集の形式

### TMX形式の翻訳メモリ

OmegaTが内部で保持する翻訳メモリは、ユーザーは確認できないようになっている。しかし翻訳プロジェクトが自動保存されるたびに、新規の、または更新された翻訳内容が自動的に出力され、3つのTMX形式の翻訳メモリファイル（OmegaTネイティヴのTMX、レベル1 TMX、レベル2 TMX）が生成される。

  - ネイティヴTMXファイルは、OmegaTのプロジェクト専用の形式である。
  - レベル1 TMXファイルは、文字情報を保持しており、TMXレベル1とレベル2に対応した他の翻訳支援ツールで使用可能である。
  - レベル2 TMXファイルは、文字情報と内部タグの情報を保持しており、TMXレベル2に対応した翻訳支援ツールで使用可能である。

生成されたレベル2 TMXファイルには、OmegaTの内部タグがTMXタグに挟まれた形で含まれ、このTMXタグによって、TMXレベル2に対応した他の翻訳支援ツールで参考訳文として使用できる。

バージョン1.4b以降のOmegaTであれば、レベル1とレベル2のTMXファイルをインポートできる。OmegaTへインポートされたレベル2 TMXファイルは、そこに含まれるレベル2タグをOmegaT自身が変換するため、ネイティヴTMXファイルと同じように扱える。

### 用語集

OmegaTが使用できる用語集ファイルは、UTF-8エンコーディングで記述され、拡張子が.txtや.utf8である、タブ区切りで記述されたプレーンテキストファイルである（3.1.7よりUTF-16LEにも対応）。用語集ファイルの構造はきわめて単純である。最初の列に原文の用語、2番目の列に対応する訳文の用語、そして3番目の列に（任意で）内容に関するコメントを加えることができる。このような形であるため、テキストエディターなどで簡単に作成できる。

用語データ交換の標準フォーマットであるTBXファイルや、標準的なCSVフォーマットで記述された構造化されたテキストにも、同様に対応している。

## ユーザーのコミュニティによる貢献

### OmegaTプロジェクト

OmegaTプロジェクトは、翻訳者たちの要望に着目する、コンピューターに詳しいメンバーのグループと言える。OmegaTのユーザーは、翻訳者からのニーズのうち、OmegaTプログラム本体ではまだ実現されていないものについては、対応が可能なツールをユーザー自身で開発し、公開することを推奨されている。\[9\]

### OmegaTのローカリゼーション

OmegaTのユーザーインターフェースとドキュメントは、約30の言語に翻訳されている。興味があるボランティア翻訳者は、ユーザーインターフェース、「お手軽スタートガイド」− OmegaT起動時に表示される短いチュートリアル、および取扱説明書の全体（もしくは上記3つすべて）の翻訳に携わることができる。すべての言語ファイルと、取扱説明書の翻訳内容は、OmegaTの標準パッケージに含まれている。

### ユーザーが作成したプログラム

OmegaTのユーザーコミュニティの特徴として、OmegaT本体に機能が不足していると、その役割を果たすマクロやスクリプト、プログラムを作成しようという機運がユーザー間に生まれる、という点がある。（時にはそれがきっかけで、後にOmegaT本体の機能として実装されることもある。）OmegaTが段落単位の分節化だけに対応していたときは、あるユーザーが文章単位で分節化できるOpenOffice.orgマクロを作成した。OmegaTで翻訳メモリを自動的に活用する場合、翻訳メモリを結合する必要性が生まれたが、あるユーザーがTMX結合スクリプトを作成した。OmegaTに綴り確認（スペルチェック）機能が存在しなかった頃、複数のユーザーがスクリプトを作成し、OmegaTを用いた翻訳作業の流れに綴り確認を加えることに成功した。\[10\]

現在、OmegaTにはない機能を提供するツール群には、Trados TagEditorファイル用の変換ユーティリティや、2種類の単純な整列ツール、その場で用語を追加できるツール、そしてタグを自分で配置可能にするツールが含まれる。\[11\]

## OmegaTに関連したその他のソフトウェア

### Autshumato translation suite

Autshumatoには、コンピューター翻訳支援ツール、整列ツール、PDF抽出ツール、TMX編集ツール、収集データを基準にしたパブリック翻訳メモリなどが含まれる。The finished version will include a terminology manager and a machine translator. コンピューター翻訳支援ツールの部分はOmegaTが元になっており、実行にはOpenOffice.orgが必要である。その開発は、南アフリカ共和国の芸術文化科学技術省による支援を受けている。\[12\]

### Benten

Bentenは、[EclipseをベースにしたXLIFF編集ツールである](../Page/Eclipse_\(統合開発環境\).md "wikilink")。翻訳メモリを参照するプロセスで、OmegaTのソースコードを使用している。 \[13\]

### Boltran

Boltranは、スタンドアロン、Webベースで動作する、OmegaTプロジェクトの仕組みを模擬したコンピューター翻訳支援ツールである。OmegaTのソースコードを元にしている。従って、OmegaTが翻訳可能なあらゆる文書を、同じく翻訳可能である。また、OmegaTとほぼ同等の用語集と参考訳文の機能も持っている。現在、公開されているBoltranのサーバーは開発者のWebサイトのみである。しかし、誰であってもそこへ公開または非公開のBoltranサーバーをセットアップできる。\[14\]

### OmegaT+

OmegaT+は、OmegaT 1.4.5を元にしたコンピューター翻訳支援ツールである。OmegaT+はOmegaTと同じ仕組みで動作する。しかし、プロジェクトファイル群に互換性はない。\[15\]

## 関連項目

  - [Translation Memory eXchange](https://ja.wikipedia.org/wiki/Translation_Memory_eXchange "wikilink") (TMX、翻訳メモリのためのデータ形式)
  - [オープンソース](../Page/オープンソース.md "wikilink")
  - [翻訳メモリ](../Page/翻訳メモリ.md "wikilink")
  - [翻訳支援ツール](../Page/翻訳支援ツール.md "wikilink")
  - [Office Open XML](../Page/Office_Open_XML.md "wikilink")
  - [OpenDocument](../Page/OpenDocument.md "wikilink")

## 脚注

## 外部リンク

  - [OmegaT公式Webサイト（英語版）](http://omegat.org/)

  - [OmegaT公式Webサイト（日本語版）](http://www.omegat.org/ja/omegat.html)

  -
  - [OmegaT 日本語マニュアル](http://www.bi-japan.co.jp/manual/OmegaT_01contents.html)

### ユーザーグループ

  - [omegat@yahoogroups.com](http://groups.yahoo.com/group/omegat) – メーリングリスト（多言語対応、未購読でも検索可能）

  - OmegaT日本語化、日本語による情報提供サイト（ファイルのリポジトリ登録やWikiページ）

  - [Googleグループ：OmegaT-doc-ja](https://groups.google.com/group/omegat-doc-ja?hl=ja) – OmegaT日本語化メンバーのディスカッション（メーリングリスト）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Javaプラットフォームソフトウェア](https://ja.wikipedia.org/wiki/Category:Javaプラットフォームソフトウェア "wikilink") [Category:翻訳ソフトウェア](https://ja.wikipedia.org/wiki/Category:翻訳ソフトウェア "wikilink")

1.  <http://www.java.com/ja/download/help/5000011000.xml>
2.  <http://www.translationtribulations.com/2010/07/results-of-june-translation-tools.html>
3.  <http://accurapid.com/journal/23linux.htm>
4.  [1](https://sourceforge.net/projects/omegat/files/) OmegaTの通常版、開発版の公開ページ
5.  [2](http://sourceforge.net/p/omegat/svn/HEAD/tree/trunk/) 最新のソースファイルはSourceForgeのコードレポジトリで入手可能
6.  [Officeアプリケーション向けOpen Document形式](http://www.iso.org/iso/en/CatalogueDetailPage.CatalogueDetail?CSNUMBER=43485&scopelist=PROGRAMME) – ISO/IEC 26300:2006 規格
7.  [Okapi Framework](http://okapi.sourceforge.net/Release/Shared/Help/tutorial_02.htm) – テキスト抽出ユーティリティ。中のフォルダー階層を含めた、OmegaTプロジェクトフォルダーを生成できる
8.  [po4a](http://po4a.alioth.debian.org/) – [Portable Object](../Page/Gettext.md "wikilink") 形式へ、または同形式からの変換が可能なユーティリティ。Debianパッケージに含まれるPerlアプリケーション
9.  [OmegaT Getting Involved](http://www.omegat.org/ja/involved.html) – 翻訳者が、OmegaT本体の機能を拡張するツールを開発することを推奨されている
10. <http://tech.groups.yahoo.com/group/OmegaT/files/>
11. <http://www.omegat.org/ja/resources.html>
12. [Autshumato](http://autshumato.sourceforge.net/)
13. [Benten](http://sourceforge.jp/projects/benten/)
14. [Boltran](http://www.boltran.com/home.seam)
15. [OmegaT+](http://omegatplus.sourceforge.net/)