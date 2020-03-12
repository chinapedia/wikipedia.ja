> この記事は[BibTeX](https://ja.wikipedia.org/wiki/BibTeX)から翻訳されています。


[BibTeX_logo.svg](https://ja.wikipedia.org/wiki/File:BibTeX_logo.svg "fig:BibTeX_logo.svg")\]\]

****\[1\]とは[参考文献](../Page/参考文献.md "wikilink")の一覧の整形に使われるツールである。

## 概要

は[オーレン・パタシュニク](../Page/オーレン・パタシュニク.md "wikilink") (Oren Patashnik) と[レスリー・ランポート](../Page/レスリー・ランポート.md "wikilink") (Leslie Lamport) が[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に開発した。 では文献書誌情報とその情報の表記方法とを分離して記述できるため、文献の参照形式を一貫した形式で書くことが可能である。コンテンツと表記・スタイルの[分離という同様の方式は](../Page/関心の分離.md "wikilink")、[](../Page/LaTeX.md "wikilink") や [XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink") と [CSS](../Page/Cascading_Style_Sheets.md "wikilink") といった[マークアップ言語](../Page/マークアップ言語.md "wikilink")にも見てとることができる。

なお、 を基にして日本語処理に対応させたものが **** である。そのため、日本語文字を含む `.bib` ファイルを処理する場合には、 ではなく  を使用する必要がある。

## 書誌情報ファイル

は参考文献の一覧用に、出力形式とは独立したテキストベースのファイル形式を用いる。各書誌情報は論文・書籍・学位論文といった書誌項目の種別を持つ。 書誌情報ファイルは通常 「`.bib`」 の拡張子を持つ。

書誌情報には以下のような標準的なデータ項目がある。

| データ項目          | 説明                                                                                                                                                                  |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `address`      | 出版社の住所。出版地として通常は都市名が記載されるが、あまり知られていない出版社等については正式な住所が記載される。                                                                                                          |
| `annote`       | 注釈附きの書誌スタイル用の注釈（あまり使われない）。                                                                                                                                          |
| `author`       | 著者名。著者が複数である場合には、「`and`」 でつなげる。                                                                                                                                     |
| `booktitle`    | （書籍中の一部のみを参照している場合に）書籍タイトル。                                                                                                                                         |
| `crossref`     | 相互参照用のキー。                                                                                                                                                           |
| `chapter`      | 章番号。                                                                                                                                                                |
| `edition`      | 書籍の版（「第一版」・「改訂版」などの形式で表記される）。                                                                                                                                       |
| `editor`       | 編著者名。                                                                                                                                                               |
| `eprint`       | 電子出版時の指定。プレプリントもしくはテクニカルレポート。                                                                                                                                       |
| `howpublished` | 出版形態（出版形態が特殊な場合）。                                                                                                                                                   |
| `institution`  | 出版社とは別に出版に関わった機関。                                                                                                                                                   |
| `journal`      | 雑誌名。                                                                                                                                                                |
| `key`          | エントリのアルファベット順での並びを指定する際に使われる隠れ項目。引用参照や相互参照時に使われるキーとは異なる。                                                                                                            |
| `month`        | 出版月。出版されていない場合は制作月。                                                                                                                                                 |
| `note`         | 注記。                                                                                                                                                                 |
| `number`       | 雑誌・テクニカルレポートの号数。大半の雑誌には 「」（巻数）が付与されているが、「」（号数）は付与されていない場合がある。                                                                                                       |
| `organization` | 会議の主催者。                                                                                                                                                             |
| `pages`        | ページ数。                                                                                                                                                               |
| `publisher`    | 出版社名。                                                                                                                                                               |
| `school`       | 学位論文の場合に、学位の提出大学名。                                                                                                                                                  |
| `series`       | 書籍のシリーズ名。                                                                                                                                                           |
| `title`        | タイトル。                                                                                                                                                               |
| `type`         | 報告種別。(例：「」)                                                                                                                                                         |
| `url`          | [WWW](../Page/World_Wide_Web.md "wikilink") 上の [URI](../Page/Uniform_Resource_Identifier.md "wikilink")（[URL](../Page/Uniform_Resource_Locator.md "wikilink") を含む）。 |
| `volume`       | 雑誌または書籍の巻数。                                                                                                                                                         |
| `year`         | 出版年（出版されていない場合は制作年）。                                                                                                                                                |

さらに各書誌項目には、その書誌を引用参照もしくは相互参照する際に用いられるキーが付与される。このキーは各書誌項目の先頭で与えられ、データ項目の一部とはならない。

### エントリ種別

書誌情報ファイルに含まれる各エントリは、いくつかの種類に分けられる。以下の種類は全て  スタイルが解釈する。

  - `article`: 雑誌に掲載された論文。
    必須項目：`author`, `title`, `journal`, `year`
    オプション項目：`volume`, `number`, `pages`, `month`, `note`, `key`
    `book`: 出版社が刊行した書籍。
    必須項目：`author`/`editor`, `title`, `publisher`, `year`
    オプション項目：`volume`, `series`, `address`, `edition`, `month`, `note`, `key`
    `booklet`: 出版社や機関名が明示的されていない印刷物や製本済の作品。
    必須項目：`title`
    オプション項目：`author`, `howpublished`, `address`, `month`, `year`, `note`, `key`
    `conference`: `inproceedings` と同一。[Scribe](https://ja.wikipedia.org/wiki/Scribe "wikilink") との互換性のために残されている。
    必須項目：`author`, `title`, `booktitle`, `year`
    オプション項目：`editor`, `pages`, `organization`, `publisher`, `address`, `month`, `note`, `key`
    `inbook`: 書籍中の一部。一章もしくは一節など。範囲ページの指定による。
    必須項目：`author`/`editor`, `title`, `chapter`/`pages`, `publisher`, `year`
    オプション項目：`volume`, `series`, `address`, `edition`, `month`, `note`, `key`
    `incollection`: それ自体がタイトルを持っている書籍中の一部。
    必須項目：`author`, `title`, `booktitle`, `year`
    オプション項目：`editor`, `pages`, `organization`, `publisher`, `address`, `month`, `note`, `key`
    `inproceedings`: 会議論文集中の一論文。
    必須項目：`author`, `title`, `booktitle`, `year`
    オプション項目：`editor`, `pages`, `organization`, `publisher`, `address`, `month`, `note`, `key`
    `manual`: マニュアル。技術文書。
    必須項目：`title`
    オプション項目：`author`, `organization`, `address`, `edition`, `month`, `year`, `note`, `key`
    `mastersthesis`: [修士](../Page/修士.md "wikilink")学位論文。
    必須項目：`author`, `title`, `school`, `year`
    オプション項目：`address`, `month`, `note`, `key`
    `misc`: その他該当種別が無いもの。
    必須項目：無し
    オプション項目：`author`, `title`, `howpublished`, `month`, `year`, `note`, `key`
    `phdthesis`: [博士](../Page/博士.md "wikilink")学位論文。
    必須項目：`author`, `title`, `school`, `year`
    オプション項目：`address`, `month`, `note`, `key`
    `proceedings`: 会議論文集。
    必須項目：`title`, `year`
    オプション項目：`editor`, `publisher`, `organization`, `address`, `month`, `note`, `key`
    `techreport`: 大学、研究機関などから出版された報告書。通常シリーズ化され、番号付けされる。
    必須項目：`author`, `title`, `institution`, `year`
    オプション項目：`type`, `number`, `address`, `month`, `note`, `key`
    `unpublished`: 著者とタイトルがある文書であるが、公式に刊行されていないもの。
    必須項目：`author`, `title`, `note`
    オプション項目：`month`, `year`, `key`

## 書誌スタイルファイル

文書中では `\bibliographystyle` コマンドにより書誌スタイルを指定する必要がある。一般的な指定値として、「`\bibliographystyle{plain}`」や 「`\bibliographystyle{abbrv}`」 といった指定がある。

の書誌スタイルファイルは 「`.bst`」という拡張子を持ち、書誌項目をどのように整形するかを記述するのに、単純なスタックベースのプログラミング言語を用いる。 プログラム `bibtex` はこのスタイルファイルに従って書誌事項を整形し、[](../Page/TeX.md "wikilink") または  の整形コマンドに変換する。なお、[HTML](../Page/HyperText_Markup_Language.md "wikilink") を出力するようなスタイルファイルも存在する。固有の  スタイルファイルは `latex makebst` コマンドにより生成することができる。

##  コマンドの動作

参考文献一覧の情報を出力するには  ツールを動作させる必要がある。

1.  まず `latex` コマンドを起動し、元の論文ファイルを整形し、参照情報を取り出す。この時点では、 ツールからは参考文献情報が未定義であるとの警告メッセージが出力される。

2.  ツールを動作させる。

3.  再度  ツールを動作させる。この時点でも再び参考文献情報が未定義であるとの警告メッセージが出力される。

4.  3回目の  ツールの動作。参考文献情報が整形され、出力される。

参照情報を加えるもしくは削除するたびに、上記手順を繰り返す。

## 例

`.bib` ファイルに以下のような数学ハンドブックのエントリが含まれているとする。

``` bibtex
 @Book{abramowitz+stegun,
 author = "Milton Abramowitz and Irene A. Stegun",
 title = "Handbook of Mathematical Functions with
 Formulas, Graphs, and Mathematical Tables",
 publisher = "Dover",
 year = 1964,
 address = "New York",
 edition = "ninth Dover printing, tenth GPO printing"
 }
```

本文中でこのハンドブックを参照する場合に、書誌情報は参照スタイル（[APA](https://ja.wikipedia.org/wiki/APAスタイル "wikilink")、MLA、[Chicago](https://ja.wikipedia.org/wiki/シカゴ・マニュアル・オブ・スタイル "wikilink") など）に応じて様々な形式で表記される。 は `\cite` コマンドおよび書誌参照スタイルの指定に従って、これを扱う。 文書中に `\cite{abramowitz+stegun}` というコマンドが現れた場合に、`bibtex` プログラムはこれを参考文献リストに追加し、 の整形用コードを出力する。 文書を組版した結果としては、以下のような見栄えになることが多い。

スタイルファイルに応じて  は著者名の姓名の順を入れ替えたり、タイトルの大文字・小文字を変えたり、`.bib` ファイルにある情報のうちいくつかの項目については省略したり、テキストの一部を斜体に変更したり、[約物](../Page/約物.md "wikilink")を加えたりなどの整形を行う。参考文献一覧の情報全体を同一のスタイルファイルで整形することによって、最小限の労力で全体の出力の一貫性を保ち、一定の整形結果を得ることができる。

### 著者名の整形

「von」、「van」、「der」のような姓に付与される[接頭辞](../Page/接頭辞.md "wikilink")は自動的に処理され、ミドルネームと区別するために小文字で整形される。複数語からなる姓を名・ミドルネームと区別する場合には、姓を先に書き、カンマを間に加えてから、名・ミドルネームを書く。「Jr.」、「Sr.」や 「III」などの、名に付与される[接尾辞](../Page/接尾辞.md "wikilink")は通常2つのカンマを間に加えることで自動的に処理できる。

``` bibtex
 @Book{hicks2001,
 author = "von Hicks, III, Michael",
 title = "Design of a Carbon Fiber Composite Grid Structure for the GLAST
 Spacecraft Using a Novel Manufacturing Technique",
 publisher = "Stanford Press",
 year = 2001,
 address = "Palo Alto",
 edition = "1st,",
 isbn = "0-69-697269-4"
 }
```

姓接頭辞を認識させるのにカンマを使わない場合、代わりに中括弧を用いる書き方（「`{Hicks III}`」）もある。

### 相互参照

では `crossref` フィールドを用いて、他の書誌情報を参照することができる。以下の例では、文献「`author:06`」 から文献 「`conference:06`」を参照している。

``` bibtex
 @INPROCEEDINGS {author:06,
 title = {Some publication title},
 author = {First Author and Second Author},
 crossref = {conference:06},
 pages = {330--331},
 }
 @PROCEEDINGS {conference:06,
 editor = {First Editor and Second Editor},
 booktitle = {Proceedings of the Xth Conference on XYZ},
 year = {2006},
 month = {October},
 }
```

上記入力を  にかけると、以下のような出力が得られる。

## 用途別スタイルファイル

学術雑誌毎に多くの異なるスタイルファイルがいわば「お手製」で作られてきた。引用スタイルをカスタマイズする必要がある場合は、`natbib` や `jurabib` といった  マクロパッケージを使うか、`makebst` といったツールを使える。

### フリーソフトウェア

大半の[参考文献管理ソフトウェアが](../Page/引用管理ソフトウェア.md "wikilink")  形式の入出力に対応している。以下のパッケージは を内部形式として用いている。

<table>
<thead>
<tr class="header">
<th><p>ソフトウェア名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Bib-it[2]</p></td>
<td><p>形式による書誌情報の管理用フロントエンドの <a href="https://ja.wikipedia.org/wiki/Java" title="wikilink">Java</a> 実装。スタイルファイル (<code>.bst</code>) の生成機能もある。(<a href="../Page/GNU_General_Public_License.md" title="wikilink">GPL</a>)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/bib2xhtml" title="wikilink">bib2xhtml</a> <a href="http://www.spinellis.gr/sw/textproc/bib2xhtml/">1</a></p></td>
<td><p>ファイルを <a href="../Page/Extensible_HyperText_Markup_Language.md" title="wikilink">XHTML</a> による一覧に変換。(GPL)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/BibDesk" title="wikilink">BibDesk</a> <a href="http://bibdesk.sourceforge.net">2</a></p></td>
<td><p>形式による書誌情報管理用の <a href="https://ja.wikipedia.org/wiki/macOS" title="wikilink">macOS</a> アプリケーション。(GPL)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/BibTex2Word2007" title="wikilink">BibTex2Word2007</a> <a href="http://sdudah.googlepages.com/bibtex2word2007bibliographyconverter">3</a></p></td>
<td><p>形式を <a href="../Page/Office_Open_XML.md" title="wikilink">Office Open XML</a> Document 形式に変換する簡易 <a href="../Page/AWK.md" title="wikilink">AWK</a> スクリプト。(GPL)</p></td>
</tr>
<tr class="odd">
<td><p>Bibtex4Word <a href="http://www.ee.ic.ac.uk/hp/staff/dmb/perl/bibtex4word.doc">4</a></p></td>
<td><p>データベースから指定の書式で文献参照するための <a href="../Page/Microsoft_Word.md" title="wikilink">Microsoft Word</a> マクロ。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/bibutils" title="wikilink">bibutils</a> <a href="http://www.scripps.edu/~cdputnam/software/bibutils/">5</a></p></td>
<td><p>XML ベースの米国議会図書館による Metadata Object Description Schema (MODS) 形式を中間形式として、いくつかの書誌形式間の変換を行う。クロスプラットフォーム。(GPL)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Bibwiki" title="wikilink">Bibwiki</a> <a href="http://www.plaschg.net/bibwiki/">6</a></p></td>
<td><p>参照情報を管理する Mediawiki 用拡張。いくつかの情報源（Aleph、<a href="../Page/Amazon.com.md" title="wikilink">Amazon</a> など）からの入力に対応し、 形式での一覧作成を行える。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Jabref" title="wikilink">Jabref</a></p></td>
<td><p>形式による書誌情報の管理用フロントエンドの Java 実装。<a href="../Page/PubMed.md" title="wikilink">PubMed</a> や <a href="https://ja.wikipedia.org/wiki/CiteSeer" title="wikilink">CiteSeer</a> への検索機能もある。(GPL)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/KBibTeX" title="wikilink">KBibTeX</a> <a href="http://www.unix-ag.uni-kl.de/~fischer/kbibtex/index.html">7</a></p></td>
<td><p>形式で参考文献情報を管理する <a href="../Page/KDE.md" title="wikilink">KDE</a> アプリケーション。Web 検索機能（<a href="../Page/Google.md" title="wikilink">Google</a>、PubMed など）や RTF、<a href="../Page/Extensible_Markup_Language.md" title="wikilink">XML</a>、HTML への出力機能など。(GPL)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Pybliographer" title="wikilink">Pybliographer</a></p></td>
<td><p>形式による書誌情報の管理用フロントエンドの <a href="../Page/Python.md" title="wikilink">Python</a> 実装。(GPL)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Referencer" title="wikilink">Referencer</a> <a href="http://icculus.org/referencer/index.html">8</a></p></td>
<td><p>形式で参考文献情報を管理する <a href="../Page/GNOME.md" title="wikilink">GNOME</a> アプリケーション。自動メタデータ取得機能（DOI、Arxiv ID など）や、<a href="../Page/Portable_Document_Format.md" title="wikilink">PDF</a> プレビュー機能、タグ付け機能など。(GPL)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/RefTeX" title="wikilink">RefTeX</a></p></td>
<td><p>形式に対応した <a href="../Page/Emacs.md" title="wikilink">Emacs</a> 上の<a href="https://ja.wikipedia.org/wiki/引用情報管理ソフトウェア" title="wikilink">引用情報管理ソフトウェア</a>。<a href="https://ja.wikipedia.org/wiki/AUCTeX" title="wikilink">AUCTeX</a> パッケージに対応。(GPL)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/Rtfbtx" title="wikilink">Rtfbtx</a> <a href="http://www.spinellis.gr/sw/ports/rtfbtx/">9</a></p></td>
<td><p>スタイルファイルから（ 出力ではなく、）<a href="../Page/Rich_Text_Format.md" title="wikilink">RTF</a> 出力を行う。(Pre-<a href="https://ja.wikipedia.org/wiki/LaTeX_Project_Public_License" title="wikilink">{{lang</a>)</p></td>
</tr>
</tbody>
</table>

## 書誌情報データベース

<table>
<thead>
<tr class="header">
<th><p>データベース名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Association_for_Computing_Machinery.md" title="wikilink">ACM</a> ポータル <a href="http://portal.acm.org">10</a></p></td>
<td><p>リンクをクリックすると、エントリを取得可能。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Amatex" title="wikilink">Amatex</a> <a href="http://www.2ndminute.org:8080/amatex">11</a></p></td>
<td><p>amazon.com の情報から  エントリを自動生成。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/BibSonomy" title="wikilink">BibSonomy</a> <a href="http://www.bibsonomy.org/">12</a></p></td>
<td><p>ベースのソーシャルブックマーク・論文情報管理ソフトウェア。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/CiteSeer" title="wikilink">CiteSeer</a></p></td>
<td><p>オンラインの研究論文データベース。 形式の引用情報を生成している。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/CiteULike" title="wikilink">CiteULike</a></p></td>
<td><p>コミュニティベースの論文情報データベース。入出力に  形式を使用。</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/Google_Scholar.md" title="wikilink">Google Scholar</a></p></td>
<td><p><a href="../Page/Google.md" title="wikilink">Google</a> の学術論文検索システム。「Scholar Preferences」 のオプションを有効にすると、 形式での参考文献情報が入手できる。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/HubMed" title="wikilink">HubMed</a> <a href="http://www.hubmed.org/">13</a></p></td>
<td><p>カスタマイズ可能な <a href="../Page/PubMed.md" title="wikilink">PubMed</a> インタフェース。 出力機能附き。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/Lead2Amazon" title="wikilink">Lead2Amazon</a> <a href="http://lead.to/amazon/jp/">14</a></p></td>
<td><p><a href="../Page/Amazon.com.md" title="wikilink">Amazon.com</a>[3]から  エントリを自動生成する。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/MathSciNet" title="wikilink">MathSciNet</a></p></td>
<td><p>米国数学会によるデータベース（登録者オプション）。 「Select alternative format」 オプションの選択で  形式を取得可能。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ja.wikipedia.org/wiki/TeXMed" title="wikilink">TeXMed</a> <a href="http://www.sbg.bio.ic.ac.uk/~mueller/TeXMed/">15</a></p></td>
<td><p><a href="../Page/PubMed.md" title="wikilink">PubMed</a> 用の  インタフェース。</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ja.wikipedia.org/wiki/The_Collection_of_Computer_Science_Bibliographies" title="wikilink">The Collection of Computer Science Bibliographies</a></p></td>
<td><p>形式を内部形式として使用。検索結果や新規情報の追加も  形式で行われる。</p></td>
</tr>
</tbody>
</table>

## 脚注

<references />

## 外部リンク

  - [the Comprehensive  Archive Network](http://www.ctan.org/) ([CTAN](https://ja.wikipedia.org/wiki/CTAN "wikilink"))
      - [The  Catalogue OnLine, Entry for , Ctan Edition](http://www.ctan.org/get/help/Catalogue/entries/bibtex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/bibtex.html)）
  - [てんびんの経済学](http://www.okomeda.net/)
      - [ の家](http://www.okomeda.net/?LaTeX%E3%81%AE%E5%AE%B6)
          - [BibTeX 活用術](http://www.okomeda.net/?BibTeX%E6%B4%BB%E7%94%A8%E8%A1%93)
  - [私的文書置場 — 新堂 安孝](http://quruli.ivory.ne.jp/document/)
      - [BibTeX と bibtex-mode，reftex-mode の使い方](http://quruli.ivory.ne.jp/document/bibtex.html)
  - [齋藤経史 (Keiji <span style="font-variant: small-caps">Saito</span>) のホームページ](http://keijisaito.info/)
      - [齋藤経史（Keiji <span style="font-variant: small-caps">Saito</span>）の Web 倉庫 \#BibTeX と文献管理](http://keijisaito.info/archive.htm#tex_bibtex)
  - [LaTeX handbook — 萩平 哲 (<span style="font-variant: small-caps">Hagihira</span>, Satoshi)](http://www.med.osaka-u.ac.jp/pub/anes/www/html/manual/latex.html)
      - [II. レファレンスの書式設定について](http://www.med.osaka-u.ac.jp/pub/anes/www/html/manual/latex3.html)
  - [BibTeX.org](http://www.bibtex.org/)
  - [Managing Citations and Your Bibliography with BibTeX](http://www.tug.org/pracjourn/2006-4/fenn/) by Jürgen <span style="font-variant: small-caps">Fenn</span> ( 2006, number 4)
  - [Getting to Grips with  — Bibliography Management](http://www.andy-roberts.net/misc/latex/latextutorial3.html)
  - [ Bibliography Style Database](http://jo.irisson.free.fr/bstdatabase/)……各種論文誌用の  スタイルファイルのデータベース
  - [BibTeX in WinEdit](http://www.math.jhu.edu/~jkramer/bibtex/)
  - [BibTeX Style Examples](http://www.cs.stir.ac.uk/~kjt/software/latex/showbst.html)……50以上のパブリックドメインの  スタイルファイルの例
  - [Bibliography Styles](http://amath.colorado.edu/documentation/LaTeX/reference/faq/bibstyles.pdf) ([PDF](../Page/Portable_Document_Format.md "wikilink")) ……参考文献スタイルの種類別に引用スタイルと書誌項目の整形例を例示

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink")

1.  本来はこのように大文字を並べて表記すべきであるが、組版処理による表記ができない[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")や[電子メール](../Page/電子メール.md "wikilink")などでは、大文字と小文字を組み合わせて「BibTeX」と表記する。通常 [](../Page/LaTeX.md "wikilink") 文書とともに用いられる。
2.  <http://bib-it.sourceforge.net/>
3.  amazon.ca、amazon.co.jp、amazon.co.uk、amazon.com、amazon.de、amazon.fr