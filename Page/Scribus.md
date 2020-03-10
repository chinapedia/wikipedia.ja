> この記事は[Scribus](https://ja.wikipedia.org/wiki/Scribus)から翻訳されています。


**Scribus**（すくらいばす（英語読み））は、[オープンソース](../Page/オープンソース.md "wikilink")な[DTP](../Page/DTP.md "wikilink")（デスクトップパブリッシング）[ソフトウェア](../Page/ソフトウェア.md "wikilink")。動作[OSは](../Page/オペレーティングシステム.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[UNIX](../Page/UNIX.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")および[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")（[NT系](../Page/Windows_NT系.md "wikilink")）。 [Adobe PageMakerや](../Page/Adobe_PageMaker.md "wikilink")[QuarkXPress](../Page/QuarkXPress.md "wikilink")、[Adobe InDesignの様に高度なページレイアウト機能を持つ](../Page/Adobe_InDesign.md "wikilink")。

## 解説

Scribus は、柔軟なレイアウト構成、植字およびプロ品質のイメージセッティング装置のためのファイル調整や、動的・対話的な[PDFのプレゼンテーションや組み版の作製を目的として設計されており](../Page/Portable_Document_Format.md "wikilink")、使用目的としては新聞、[パンフレット](../Page/小冊子.md "wikilink")、会報、ポスターや冊子などがある。

Scribus は、[SVG](https://ja.wikipedia.org/wiki/SVG "wikilink")を含み広範な画像形式ファイルの利用が可能となっており、[CMYK](../Page/CMYK.md "wikilink")やICC プロファイルによる[カラーマネージメント機能が](https://ja.wikipedia.org/wiki/カラーマネージメントシステム "wikilink")[Python](../Page/Python.md "wikilink")による[スクリプト](../Page/スクリプト.md "wikilink")として組み込まれており、24以上の言語で利用可能である。

印刷は、組み込みのレベル3 [PostScript](../Page/PostScript.md "wikilink")ドライバによって行われ、[TrueType](../Page/TrueType.md "wikilink")や[Type 1](https://ja.wikipedia.org/wiki/PostScriptフォント#Type_1 "wikilink")、[OpenType](../Page/OpenType.md "wikilink")等のフォント埋め込みもサポートされている。また、このドライバはレベル2 PostScriptを完全にサポートしている。

PDFへの対応は透過、暗号化および入力可能なフォーム、注釈、ブックマークを含む。PDF のエクスポートは問題無いが、インポートと編集は出来ない。またScribusがエクスポートしたPDFファイルは、[プロポーショナルフォント](../Page/プロポーショナルフォント.md "wikilink")を含む場合Acrobat Readerで検索することが出来ない \[1\]\[2\]。

ファイルフォーマットはSLAと呼ばれ、[XMLで記述されている](../Page/Extensible_Markup_Language.md "wikilink")。[OpenDocument](../Page/OpenDocument.md "wikilink")のテキスト形式ファイルや[リッチテキスト](https://ja.wikipedia.org/wiki/リッチテキスト "wikilink")、[マイクロソフト](../Page/マイクロソフト.md "wikilink")[ワード形式および](../Page/Microsoft_Word.md "wikilink")[HTML形式のファイルが](../Page/HyperText_Markup_Language.md "wikilink")（制限はあるものの）インポートが可能である。

Scribusは [QuarkXPress](../Page/QuarkXPress.md "wikilink")や[Microsoft Publisher](https://ja.wikipedia.org/wiki/Microsoft_Publisher "wikilink")、[InDesign](https://ja.wikipedia.org/wiki/InDesign "wikilink")などの商用ソフトウェアのネイティブフォーマットを読み込んだり書き込んだりすることは出来ない。開発者はこれらファイルフォーマットの[リバースエンジニアリング](https://ja.wikipedia.org/wiki/リバースエンジニアリング "wikilink")は非常に複雑であり、またこれらのソフトウェアの開発元から法に訴えられる恐れがあると考えている \[3\]。

## 改良の歴史

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>特徴</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.4.0</p></td>
<td><p>アプリケーションフレームワークがQt3→Qt4, レンダーフレーム追加, インポートファイルフィルター強化等。<br />
</p></td>
</tr>
<tr class="even">
<td><p>1.4.1</p></td>
<td><p>1.4.0安定版のバグ修正と強化部分を含む最初のポイントリリース。<br />
</p></td>
</tr>
<tr class="odd">
<td><p>1.4.2</p></td>
<td><p>Microsoft Windows 64ビット版に対応。LinuxとUNIXだけで動作したスペルチェッカーがクロスプラットフォームになった。<br />
</p></td>
</tr>
<tr class="even">
<td><p>1.4.3</p></td>
<td><p>Haiku OSポート追加, 職業的需要に応えるカラーツール群強化, QRコードに対応, 政府機関(加, 独, 蘭, 英)のカラーパレット追加。<br />
</p></td>
</tr>
<tr class="odd">
<td><p>1.4.4</p></td>
<td><p>Software Consulting Services(LLC)およびアメリカ新聞協会と提携し新聞出版の領域に進出した。<br />
</p></td>
</tr>
<tr class="even">
<td><p>1.4.5</p></td>
<td><p>Barcode Writer in Pure PostScript の最新版を含む。Scripter の更新により PDF への出力調整の自由度向上。Scripter に 新コマンド applyMasterPage() が加わり既存のマスターページを適用できるようになった。</p></td>
</tr>
<tr class="odd">
<td><p>1.4.6</p></td>
<td><p>1.5シリーズで実装された機能を追加したバグ修正版。SVGブレンドモード、CIE LAB と CIE HLCを含む４つのカラーパレットへの対応等。</p></td>
</tr>
<tr class="even">
<td><p>1.4.7</p></td>
<td><p>2018-04-27発行。1.4シリーズの最終版になると想定されていた。ほぼバグ修正のみ。</p></td>
</tr>
<tr class="odd">
<td><p>1.4.8</p></td>
<td><p>2019-03-05発行。1.4シリーズの最終版になる予定。ほぼバグ修正とアップデートのみ。</p></td>
</tr>
<tr class="even">
<td><p>1.5.0</p></td>
<td><p>1.5.x は次期安定版である 1.6.0 の見本版。特長的機能が 1.4 シリーズと比較してほぼ倍増した。 PDF/X-4 と Microsoft の XPS への出力に対応した。</p></td>
</tr>
<tr class="odd">
<td><p>1.5.1</p></td>
<td><p>アイコン一新。RTF と DOCX の読込に対応。CIE L*a*b* および CIE HLC カラーモデルに対応。</p></td>
</tr>
<tr class="even">
<td><p>1.5.2</p></td>
<td><p>アラビア語, ヘブライ語, 中国語, ヒンディー語等への対応に備えてテキスト・レイアウト・エンジンが初めから書き直された。</p></td>
</tr>
<tr class="odd">
<td><p>1.5.3</p></td>
<td><p>キャンバス上の文字入力とテキスト描画高速化。フォント選択時のフォントプレビュー実装等。</p></td>
</tr>
<tr class="even">
<td><p>1.5.4</p></td>
<td><p>カラーパレットがISO規格CxF3に対応。実験段階であるもののZonerDraw文書(バージョン4,5)とQuarkXPress文書(バージョン3,4) の読込に対応等。</p></td>
</tr>
<tr class="odd">
<td><p>1.6.x</p></td>
<td><p>PDF/X-1a, PDF/X-4, PDF/E, 脚注, 傍注, ePub出力を実現する予定。</p></td>
</tr>
</tbody>
</table>

## 関連項目

  - [DTP](../Page/DTP.md "wikilink")
  - [OpenDocumentをサポートするアプリケーションの一覧](https://ja.wikipedia.org/wiki/OpenDocumentをサポートするアプリケーションの一覧 "wikilink")
  - [オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")

## 脚注

<references/>

## 外部リンク

  -
[Category:DTPソフト](https://ja.wikipedia.org/wiki/Category:DTPソフト "wikilink") [Category:OpenDocument](https://ja.wikipedia.org/wiki/Category:OpenDocument "wikilink") [Category:Qtを使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:Qtを使用するソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:フリー教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:フリー教育ソフトウェア "wikilink")

1.  [Scribus Developer Blog PDF Surgery](http://rants.scribus.net/2006/12/10/pdf-surgery/)
2.  [:Scribus:. GPL Desktop Publishing and More](http://docs.scribus.net/index.php?lang=en&page=importhints2)
3.  [Scribus FAQ "Why are there no import filters for Quark, Indesign or other commerical \[sic\] DTP applications?"](http://docs.scribus.net/index.php?lang=en&page=faq2#19), scribus.net