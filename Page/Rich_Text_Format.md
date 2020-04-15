> この記事は[Rich Text Format](https://ja.wikipedia.org/wiki/Rich_Text_Format)から翻訳されています。


**Rich Text Format**（RTF, リッチテキストフォーマット）は、[文書ファイルフォーマット](https://ja.wikipedia.org/wiki/文書ファイルフォーマット "wikilink")の1つ。交換・編集可能な[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")の文書フォーマットとして[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")から[マイクロソフト](../Page/マイクロソフト.md "wikilink")により開発され、仕様の策定が進められた。多くのワープロソフトで読み書き可能。[ファイル拡張子は](../Page/拡張子.md "wikilink")「.rtf」。

[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")に比べて、[フォント](../Page/フォント.md "wikilink")の指定や、文字の色・大きさや太文字などの装飾指定、画像の表示や[中央揃え](https://ja.wikipedia.org/wiki/文字揃え "wikilink")・[箇条書き](../Page/箇条書き.md "wikilink")、[表](https://ja.wikipedia.org/wiki/表 "wikilink")などの簡易レイアウトを行える特徴があり、現在では、比較的簡易な[ワープロソフト](../Page/ワープロソフト.md "wikilink")のデータフォーマットの一つとして位置づけられる。

また、[PDFは主に閲覧](../Page/Portable_Document_Format.md "wikilink")・印刷を目的とした交換フォーマットであるのに対して、RTFは編集可能な交換フォーマットとなっている。

## 仕様

[1992年](../Page/1992年.md "wikilink")にRich Text Formatの仕様であるRTF 1.0が公開され、2007年1月にRTF 1.9となっている。

  - 1992年6月 RTF 1.0
  - 1994年1月 RTF 1.3
  - 1995年9月 RTF 1.4
  - 1997年4月 RTF 1.5
  - 1999年5月 RTF 1.6
  - 2001年8月 RTF 1.7
  - 2004年4月 RTF 1.8
  - 2007年1月 RTF 1.9
  - 2008年3月 RTF 1.91

### バージョンの履歴

  - RTF 1.4の仕様はWord7.0の機能をすべて含んでいる
  - RTF 1.5の仕様はWord 95 Version 7.0とWord 97で追加された命令語に対応、また日本語用の拡張があり、RTF-Jと呼ばれる。
  - RTF 1.6の仕様は 上記のほかWord 2000、Macintosh版Word 98などで追加された命令語をサポートするほか、Pocket Word、Exchange向け仕様（RTF \<-\> HTML変換に使用）を含む。
  - RTF 1.7の仕様は上記のほかWord 2002で追加された命令語をサポートする。
  - RTF 1.8の仕様はWord 2003の新機能をサポートする。
  - RTF 1.91の仕様はWord 2007の新機能をサポートする。ほかPocket Word、RichEdit、Exchange、Outlook 向けの追加機能がある。さらに
      - XMLマークアップ、名前空間のカスタム定義をサポート
      - XMLの利用方法については[Office Open XML仕様](../Page/Office_Open_XML.md "wikilink") (Ecma-376, Part4) 参照
      - カスタムXMLスキーマのバリデーション
      - XML形式に保存する際には[XSLを出力できる](../Page/Extensible_Stylesheet_Language.md "wikilink")（仕様書には記述無し）
      - RTF内に[OMMLを記述できる](https://ja.wikipedia.org/wiki/:en:Office_Open_XML_file_formats#Office_MathML_.28OMML.29 "wikilink")
      - 読み込み専用パスワードでRTFを保護できる

マイクロソフトはRTFの仕様を1.9.1以上には更新しないと言明しているが、ISO/IEC 29500策定の間に小さい修正を加えたい意向である。機能面には影響はないと見られる。

Rich Text Format (RTF) の仕様はMicrosoft WordとOfficeのメジャーバージョンアップの度に改訂されている。

<table>
<caption>RTF仕様とMicrosoft Wordの対応[1][2]</caption>
<thead>
<tr class="header">
<th><p>| RTFバージョン</p></th>
<th><p>| 発行日</p></th>
<th><p>| Microsoft Wordのバージョン</p></th>
<th><p>| Microsoft Wordのリリース日</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>1987</p></td>
<td><p>Microsoft Word 3</p></td>
<td><p>1987</p></td>
<td><p>最終版は 92年6月;[3][4] 1992 版ではMicrosoft の<a href="../Page/Object_Linking_and_Embedding.md" title="wikilink">Object Linking and Embedding</a> (OLE) オブジェクトとMacintosh版でのManager subscriberオブジェクトをサポートした。; また<a href="../Page/Windows_Metafile.md" title="wikilink">WMF</a>、<a href="https://ja.wikipedia.org/wiki/QuickDraw_Picture" title="wikilink">PICT</a>、Windowsの<a href="../Page/Windows_bitmap.md" title="wikilink">DIB</a>、<a href="https://ja.wikipedia.org/wiki/OS/2" title="wikilink">OS/2</a>メタファイル各形式の画像の貼り込みをサポートする。</p></td>
</tr>
<tr class="even">
<td><p>1.1</p></td>
<td></td>
<td><p>Microsoft Word 4</p></td>
<td><p>1989</p></td>
<td><p>フォントの文書ファイル内への埋め込みをサポート</p></td>
</tr>
<tr class="odd">
<td><p>1.2</p></td>
<td><p>1993</p></td>
<td><p>Microsoft Word 5</p></td>
<td><p>1991</p></td>
<td><p>[5][6]</p></td>
</tr>
<tr class="even">
<td><p>1.3</p></td>
<td><p>1994年1月</p></td>
<td><p>Microsoft Word 6</p></td>
<td><p>1993</p></td>
<td><p>GC0165; <a href="../Page/Windows_bitmap.md" title="wikilink">DIBの貼り付けが互換性の問題で非推奨になった</a>。以後は<a href="../Page/Windows_Metafile.md" title="wikilink">WMFの使用が推奨される</a>[7][8]。</p></td>
</tr>
<tr class="odd">
<td><p>1.4</p></td>
<td><p>1995年9月</p></td>
<td><p>Microsoft Word 95/Word 7</p></td>
<td><p>1995</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>1.5</p></td>
<td><p>April 1997</p></td>
<td><p>Microsoft Word 97/Word 8</p></td>
<td><p>1997</p></td>
<td><p>Unicode RTFの導入 - <a href="../Page/16ビット.md" title="wikilink">16ビット</a>Unicode エンコーディングが可能になった。; 画像の添付については<a href="../Page/Portable_Network_Graphics.md" title="wikilink">PNG</a>、<a href="../Page/JPEG.md" title="wikilink">JPEG</a>、<a href="https://ja.wikipedia.org/wiki/拡張メタファイル" title="wikilink">EMF画像形式は</a>16進数のバイナリ形式で貼り付けられる[9]。</p></td>
</tr>
<tr class="odd">
<td><p>1.6</p></td>
<td><p>1999年5月</p></td>
<td><p>Microsoft Word 2000/Word 9</p></td>
<td><p>1999</p></td>
<td><p>Word 2000 RTF仕様 <ref name="rtf16">{{citation | url=<a href="http://msdn.microsoft.com/en-us/library/office/aa140277%28v=office.10%29.aspx">http://msdn.microsoft.com/en-us/library/office/aa140277%28v=office.10%29.aspx</a></p></td>
</tr>
<tr class="even">
<td><p>1.7</p></td>
<td><p>2001年8月</p></td>
<td><p>Microsoft Word 2002/Word 10</p></td>
<td><p>2001</p></td>
<td><p>Word 2002 RTF仕様 [10] [11]<br />
RTF version 1.7はWindows版Word 95/97/2000/2002、Macintosh版Word 98などで追加された命令語をサポートする。</p></td>
</tr>
<tr class="odd">
<td><p>1.8</p></td>
<td><p>2004年4月</p></td>
<td><p>Microsoft Word 2003/Word 11</p></td>
<td><p>2003</p></td>
<td><p>Word 2003 RTF仕様[12] Version 1.8はMicrosoft Word 2003にて追加された拡張機能を備える。</p></td>
</tr>
<tr class="even">
<td><p>1.9.1</p></td>
<td><p>2008年3月19日<br />
(RTF 1.9 - 2007年1月)[13]</p></td>
<td><p>Microsoft Word 2007/Word 12</p></td>
<td><p>2006</p></td>
<td><p>XMLマークアップの導入 - カスタム XML タグ, スマートタグ, RTF内の数学記号のサポート - <a href="../Page/Office_Open_XML.md" title="wikilink">Office Open XML仕様への準拠</a> (Ecma-376, Part 4)[14]</p></td>
</tr>
</tbody>
</table>

### コード例

RTFのデータは[テキスト形式を用いており](../Page/テキストファイル.md "wikilink")、プレーンテキストに装飾やレイアウトのための制御用の文字列を付加した形式となっている。後に現れた[HTMLなどの](../Page/HyperText_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")とは表記方法が異なる。

`RTFの一例`

`{\rtf`
`Hello!\par`
`This is some {\b bold} text.\par`
`}`

上のサンプルは下のように表示される。

> Hello\!
> This is some **bold** text.

## 文字エンコーディング

標準的なRTFファイルは7ビットのASCII文字で記述されているが、[エスケープシーケンス](../Page/エスケープシーケンス.md "wikilink")を使うことでそれ以外の文字を扱える。コードページのエスケープのほか、RTF 1.5では Unicodeのエスケープができる。

RTF 1.5以前は7ビット文字以外は16進数 (\\'xx) で記述された。またUnicodeで32767以降の文字は負の数で表現され、[Unicode planeに収まらない文字は](../Page/基本多言語面.md "wikilink")[サロゲートペア](https://ja.wikipedia.org/wiki/サロゲートペア "wikilink")で表現される。

日本語の文字は[シフトJISコードを](../Page/Shift_JIS.md "wikilink")[ASCII](../Page/ASCII.md "wikilink")形式で表した表記法が用いられる。たとえば、\\'82\\'a0\\'82\\'a2\\'82\\'a4 のように表記され、これは「あいう」を表している。

## 人間にとっての可読性

ワードプロセッサのファイル形式の中では例外的に、RTFはプレーンテキストで記述されるので人間が読むことのできるフォーマットである。しかしながら Microsoft Wordなどが出力するRTFは膨大な命令コードが入るため非常に読みにくくなる。さらに7bit ASCII以外の文字が入ると全部エスケープされるので全く読めない物になる。

RTFは書式付きテキストであるが、本当の意味でのマークアップ言語ではないので人が手で編集するのは考慮されていない。またOLEオブジェクトなどが貼り付けられると、これも人には解読できない。

## 一般的な用途と相互運用性

大半のワードプロセッサではRTFの読み書きができるが、RTFのバージョン次第のところがある。未知の命令語が入っている場合は無視されてしまうことが多い。

### オブジェクト

MicrosoftのOLE またMacintosh版のsubscriber objectsの貼り付けは、元のアプリがないとその部分を編集できないため相互運用性を妨げる。もし開いた文書に自分の持たないアプリで作成されたOLEオブジェクトがある場合、代替ビットマップが表示されるか、全く表示されない。

### 画像

JPEG、PNG, EMF, WMF, PICT, DIBがサポートされる。RTF作成ソフトは、サポート外のファイル形式 (BMP, TIFF, GIF等) を与えられた場合はPNG, WMFなどに変換して貼り付けるか、無視して表示しないようにする。

Microsoft Wordはレジストリに ("ExportPictureWithMetafile=0") の値を設定することで、WMFへの変換を禁止できる。

### フォント

フォントの埋め込みが仕様にあるが、広くサポートされてはいない。

またフォントにファミリー名（セリフ（明朝系）、サンセリフ（ゴシック系））を指定できるが、これも広くサポートされてはいない。

### 注釈

注釈機能があるが、OpenOffice（3.3 当時）、LibreOffice（3.3.2当時）などでは注釈のインポートができないなど、サポートは限定的である。

### 描画オブジェクト

### セキュリティ上の注意

## RTFに対応したソフト

[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")に付属するアクセサリソフトをはじめ、多くの[ワープロソフト](../Page/ワープロソフト.md "wikilink")が RTFの読み書きに対応している。

  - [ワードパッド](../Page/ワードパッド.md "wikilink") - [Windows付属のソフト](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")
  - [テキストエディット](../Page/テキストエディット.md "wikilink") - macOS付属のソフト
  - [Pages](../Page/Pages.md "wikilink") - ワープロ・ページレイアウトソフト
  - [OpenOffice.org](../Page/OpenOffice.org.md "wikilink") - オフィスソフト
  - [iText](https://ja.wikipedia.org/wiki/iText "wikilink") - テキストエディタ
  - [Jedit](https://ja.wikipedia.org/wiki/Jedit "wikilink") - [Mac OS用のソフト](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") - マイクロソフトのソフト開発環境（RichTextBoxオブジェクトがRTF対応のLoadFileメソッド等を実装）

など

## RTFD

[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")、およびNEXTSTEPに由来する機能を持つ[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")・[iOS](https://ja.wikipedia.org/wiki/iOS "wikilink")では、Rich Text Formatを拡張した**RTFD**（Rich Text Format Directory、添付書類付きRTF）というフォーマットも使われている。その実体は、独自拡張したRTFファイルと添付ファイルを、拡張子RTFDの同一フォルダに入れたものである。なおOSからは拡張子RTFDののフォルダは、単一のアーカイブファイルに見えるようになっている。

## 出典

## 関連項目

  - [ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")

## 外部リンク

  - \[<http://msdn2.microsoft.com/en-us/library/aa140277(office.10>).aspx Microsoft RTF1.6仕様 1999年5月\]
  - [Microsoft RTF1.7仕様 2001年8月](http://www.microsoft.com/downloads/details.aspx?FamilyID=e5b8ebc2-6ad6-49f0-8c90-e4f763e3f04f&DisplayLang=en)
  - [Microsoft RTF1.8仕様 2004年4月](http://www.microsoft.com/downloads/details.aspx?FamilyID=ac57de32-17f0-4b46-9e4e-467ef9bc5540&displaylang=en)
  - [Microsoft RTF1.9仕様 2007年1月](http://www.microsoft.com/downloads/details.aspx?familyid=DD422B8D-FF06-4207-B476-6B5396A18A2B&displaylang=en)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.