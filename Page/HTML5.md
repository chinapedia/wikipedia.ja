> この記事は[HTML5](https://ja.wikipedia.org/wiki/HTML5)から翻訳されています。


**HTML5**（エイチティーエムエル・ファイブ）は、[HyperText Markup Languageの](../Page/HyperText_Markup_Language.md "wikilink")5回目に当たる大幅な改定版である。

HTML5は[Web Hypertext Application Technology Working Groupによって](../Page/Web_Hypertext_Application_Technology_Working_Group.md "wikilink")[2004年](../Page/2004年.md "wikilink")に定められた[Web Applications 1.0に](https://ja.wikipedia.org/wiki/Web_Applications_1.0 "wikilink")[Web Forms 2.0を取り入れたものが](https://ja.wikipedia.org/wiki/Web_Forms_2.0 "wikilink")[World Wide Web Consortiumの専門委員会に採用され](../Page/World_Wide_Web_Consortium.md "wikilink")、[World Wide Web Consortiumより](../Page/World_Wide_Web_Consortium.md "wikilink")[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[1月22日](../Page/1月22日.md "wikilink")にドラフト（草案）が発表され、[2014年](../Page/2014年.md "wikilink")[10月28日](https://ja.wikipedia.org/wiki/10月28日 "wikilink")に HTML5 が勧告され\[1\]、[2016年](../Page/2016年.md "wikilink")[11月1日](../Page/11月1日.md "wikilink")に HTML 5.1 が勧告され\[2\]、[2017年](../Page/2017年.md "wikilink")[12月14日](../Page/12月14日.md "wikilink")に HTML 5.2 が勧告された\[3\]。

改訂の主要目的のひとつとして、人間にも読解可能で、尚且つ、[コンピュータ](../Page/コンピュータ.md "wikilink")やデバイス（[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")、構文解析器など）にも矛盾せず読解されるとともに最新の[マルチメディア](../Page/マルチメディア.md "wikilink")をサポートする言語に向上することである。HTML5ではHTMLだけでなく[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、[DOMのHTML関係の部分](../Page/Document_Object_Model.md "wikilink")、[ECMAScript](../Page/ECMAScript.md "wikilink")の[APIも追加になっている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

表記は、「**HTML 5.1**」のようにバージョン表記で小数点以下を含める場合はHTMLと5.1の間にスペースを入れ、「**HTML5**」のように小数点以下を含めない場合はHTMLと5の間にスペースを含めない表記法が採用されている\[4\]。過去のバージョンについても、「**HTML4**」や「**HTML 4.0**」という表記法が使われている。[Extensible Markup Languageの文法で記述する場合は](../Page/Extensible_Markup_Language.md "wikilink")、「**XHTML5**」と表記する\[5\]\[6\]。

## 概要

HTML5は、[プロプライエタリな](../Page/プロプライエタリ・ソフトウェア.md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")として提供されている[リッチインターネットアプリケーション](https://ja.wikipedia.org/wiki/リッチインターネットアプリケーション "wikilink")の[プラットフォーム](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")（[JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")、[Adobe Flash](../Page/Adobe_Flash.md "wikilink")、[Microsoft Silverlight](../Page/Microsoft_Silverlight.md "wikilink") 等）を置き換えることを標榜しており、[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")のプラットフォームとしての機能やマルチメディア要素が実装されている。そのためHTML5が普及すればAdobe Flashなどのプラグインは不要になるという意見がある\[7\]\[8\]（後述）。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")以降に発表された[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の多くはHTML5に段階的に対応している。[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") 3.0以降、[Safari](../Page/Safari.md "wikilink") 3.1以降、[Firefox](../Page/Mozilla_Firefox.md "wikilink") 3.5以降、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") 10.5、[Internet Explorer](../Page/Internet_Explorer.md "wikilink") 9などであり主に[audio要素](https://ja.wikipedia.org/wiki/HTML5オーディオ "wikilink")・[video要素](https://ja.wikipedia.org/wiki/video要素 "wikilink")・[canvas要素](https://ja.wikipedia.org/wiki/canvas要素 "wikilink")への対応が進んでいる（2010年3月現在）。また[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")など、当初HTML5の一部とされていたものの切り離され別の規格として策定作業が進められているものがある。

### 広義のHTML5

厳密には別仕様書として分離されているものの、一般的には、[ウェブストレージ](https://ja.wikipedia.org/wiki/ウェブストレージ "wikilink")・[WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")・Geolocation API・[XMLHttpRequest](https://ja.wikipedia.org/wiki/XMLHttpRequest "wikilink") Level 2などもHTML5に含める場合が多い。

W3CのHTML5 Logoでは以下のカテゴリをHTML5に含めている\[9\]。

  - セマンティックス - HTML5の新タグ、RDFa、マイクロデータ、[マイクロフォーマット](../Page/マイクロフォーマット.md "wikilink")
  - オフラインとストレージ - App Cache、Web Storage、[Indexed Database API](https://ja.wikipedia.org/wiki/Indexed_Database_API "wikilink")、File API
  - デバイスアクセス - Geolocation API、マイク・カメラ、アドレス帳・カレンダー、端末の向き
  - 接続性 - [WebSocket](https://ja.wikipedia.org/wiki/WebSocket "wikilink")、Server-Sent Events
  - マルチメディア - [audio要素](https://ja.wikipedia.org/wiki/HTML5オーディオ "wikilink"), [video要素](https://ja.wikipedia.org/wiki/video要素 "wikilink")
  - 3D、グラフィックス、エフェクト - [SVG](../Page/Scalable_Vector_Graphics.md "wikilink")、[canvas要素](https://ja.wikipedia.org/wiki/canvas要素 "wikilink")、[WebGL](https://ja.wikipedia.org/wiki/WebGL "wikilink")、CSS3 3D
  - パフォーマンスと統合 - Web Workers、XMLHttpRequest Level 2
  - [CSS3](https://ja.wikipedia.org/wiki/Cascading_Style_Sheets#Cascading_Style_Sheets,_level_3_\(CSS3\) "wikilink") - [Webフォント](https://ja.wikipedia.org/wiki/Webフォント "wikilink")も含む

### HTML Living Standard

**HTML Living Standard**は、WHATWGが策定しているHTMLの標準仕様である。W3Cの勧告するHTML5およびそれ以降（HTML 5.1など）は、HTML Living Standardを基にしている。ただし、W3C側で変更がなされており、両者には差異が生じている\[10\]\[11\]。ウェブブラウザの開発元では、HTML Living Standardのほうがよく参照されている\[12\]\[13\]。

## 技術仕様

### エンコーディング

文書の文字コードにはUTF-8を推奨している。文書の文字コードの指定は、meta要素におけるcharset属性で指定する。これとHTTPレスポンスヘッダーのcontent-typeでエンコード宣言が省略された場合はUTF-8が既定となる。またcharset属性を含めたmeta要素は**文章先頭から1024バイト以内に記載する必要がある**\[14\]。

### 文書の構造

従来のHTMLやXHTML規格は、仕様に書かれた文書構造のルールだけではなく、妥当性検証のための[DTD](../Page/Document_Type_Definition.md "wikilink")（およびそのほかの[スキーマ](https://ja.wikipedia.org/wiki/スキーマ "wikilink")）を提供していた。一方、HTML5仕様ではスキーマは提供されない。文書構造のために提供されるのはHTML5仕様に列挙されている各種ルールのみである。

### 従来のHTMLとの文法の差異

HTML5仕様は以下のふたつの構文を採用している。

  - HTML5仕様書の中で定義される**HTML構文** → 狭義のHTML5
  - HTML5仕様書からXMLおよびその関連仕様を参照して定めている**XHTML構文** → XHTML5と呼ばれる

一方、従来のHTML仕様は**[SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink")**をその構文に採用している。SGMLおよびその関連仕様を参照しており、規格ごとに以下のような差異もある。

  - SGML規格本体のみを参照しているもの → HTML 4.0以前
  - SGML規格本体および付属書J、付属書Kを参照しているもの → HTML 4.01や、ISO/IEC 15445など

主にこのような違いのために、HTML5と従来のHTMLとの間には基本的な文法の差異が多い。以下にその代表的な例を挙げる。

#### SGML宣言

SGMLを採用していた従来のHTML規格においては、HTML文書は本質的にSGML文書であったため、HTML規格がそれぞれ提供するSGML宣言を文書の先頭に記述することが仕様上許されていた。一方HTML5の仕様では、HTML構文、XHTML構文のいずれを用いた場合でも、文書中にSGML宣言を記述することは許されていない。

#### 文書型宣言およびDTDの扱い

HTML5仕様においては、[文書型宣言](https://ja.wikipedia.org/wiki/文書型宣言 "wikilink")はもはやモード指定以外の意味をなさず、その書式は “`<!DOCTYPE html>`” である。

HTML構文では文書型宣言は必須である。XHTML構文では、HTML5で導入される新しい機能を利用する場合は必須、それ以外の場合は文書型宣言は必須ではない。

従来のHTML規格で提供されていた[DTDがなくなり](../Page/Document_Type_Definition.md "wikilink")、また文書型宣言の書式が決まっているため、HTML5ではDTDが利用できず、DTDに依存する多くの機能のほとんどが扱えなくなる。例としては、HTML4以前に扱えていた[文字実体参照](https://ja.wikipedia.org/wiki/文字実体参照 "wikilink")のほとんどがHTML5では扱えなくなる（XMLは文書内部にDTDを書くこともできるが、上記の文書型宣言の決まりを無視する結果となるため、HTML5の仕様の範疇ではない）。

#### 処理命令

SGMLを採用していた従来のHTML規格では、文書内に処理命令 (Processing instruction) を記述することができた。実際に用いられている例として、DTDを他の処理系で利用するための "architectural support declaration" が存在する (ISO/IEC 15445)。

一方、HTML5仕様におけるHTML構文ではSGMLの処理命令は記述できず、同様の機能も利用できない。XHTML構文であればXMLの処理命令は書ける。

#### マーク区間

SGMLを採用していた従来のHTML規格では、マーク区間 (marked section) と呼ばれる仕組みが利用できた。以下に例を挙げる。

``` html5
<!DOCTYPE HTML PUBLIC "ISO/IEC 15445:2000//DTD HTML//EN">
<html><head><title>...</title></head>
  <body>
    <p><![INCLUDE[ INCLUDE...マーク区間宣言がない場合と同じように解釈される ]]></p>
    <p><![IGNORE[  IGNORE ...マーク区間の中身を無視される ]]></p>
    <p><![RCDATA[  RCDATA ...マーク区間の中身がRCDATAとして処理される ]]></p>
    <p><![CDATA[   CDATA  ...マーク区間の中身がCDATAとして処理される ]]></p>
    <p><![TEMP[    TEMP   ...マーク区間の中身が一時的なものとして扱われる ]]></p>
  </body>
</html>
```

上に挙げた例のうち、HTML5仕様で利用できるのはCDATAセクションのみである。

#### コメントと注釈宣言

SGMLのコメントは "-- コメント文 --" という形を取り、マーク宣言中の空白文字の出現が許されている場所に任意の回数書くことができる。したがって従来のHTMLでは文書型宣言の中などでもコメントを挿入することが可能で、例えばISO/IEC 15445の文書型宣言は

``` html5
<!DOCTYPE HTML PUBLIC "ISO/IEC 15445:2000//DTD HTML//EN" --コメント-->
```

のようにも書ける。一方、HTML5の文書型宣言にはコメントを挿入することはできない。

また、注釈宣言の扱いも従来のHTMLとHTML5では異なる。SGMLを採用していた従来のHTMLでは注釈宣言の中に任意の回数コメントを書くことができるが、HTML5ではHTML構文でもXHTML構文でもこのような書き方は認められていない。また、従来のHTMLでは注釈宣言内の最後のコメントと終了区切り子の間に空白文字を挿入することもできたが、HTML5ではこのような書き方も認められていない。

``` html5
<!--コメント1-- --コメント2-- --HTML5ではこのような注釈宣言は書けない-->
<!-- この注釈宣言の書き方もHTML5では不可能--  >
```

#### 終了区切り子の省略

SGMLをもとにした従来のHTMLでは、タグやマーク宣言の終了区切り子 "`>`" が、文字列　"`<`", "`</`"の直前に存在する場合、その終了区切り子 "`>`" を省略することが仕様の上では許されていた\[15\]。HTML5では終了区切り子の省略はできない。

``` html
<!DOCTYPE HTML PUBLIC "ISO/IEC 15445:2000//DTD HTML//EN">
<html<head<title>Sample</title</head>
<body<p>「閉じないタグ」の例。終了区切り子が省略されている</p</body</html>
```

#### 空タグ

SGMLにおける空タグ (empty tag) とは要素型名などが書かれていない空っぽのタグのことである。従来のHTMLでは空タグの存在を許しており、利用できる場所は限られるが、空開始タグ "`<>`" と空終了タグ "`</>`" が仕様の上では記述できる。一方、HTML5では空タグを利用することはできない。

#### 簡略終了タグ

SGML規格には、NET（Null End Tag、簡略終了タグ）と呼ばれる仕組みが存在する。従来のHTMLでのNETは "/" であり、仕様上では、 "<code>

文章

</code>" という記述を "`<p/文章/`" と書くような記法が許されていた。

一方のHTML5に簡略終了タグという仕組みはない。ただし、後述する空要素の開始タグを "
" などと記述する方法は、（従来のSGMLの立場では）NETを利用したものと解釈することはできる。XMLの空要素タグも、SGMLの立場からはNETおよび付属書KのNESTCを利用した記法であると解釈できる。

#### 空要素のタグ

従来のSGMLおよびHTMLにおける空要素 (empty element) は、DTDで内容モデルを空 (EMPTY) と決められた要素のことである（例：br要素）\[16\]従来のHTMLでは、空要素の終了タグを書くことは許されていない\[17\]。よって例えば、br要素のタグを "
" や "
</br>" のように記述することもできない。

HTML5のHTML構文における空要素 (void elements) は、内容を含むことができない要素のことである\[18\]。空要素はその開始タグを "`>`",　"`/>`" のいずれかで閉じることができる。例を挙げると、br要素のタグは "
" と記述するほかに、XHTML構文のように "
" と記述することもできる。ただし空要素の終了タグを書くことはできない\[19\]。また、このような記法が許されるのは空要素または外部要素 (foreign element) のタグのみで、その他の要素の開始タグは "`>`" で閉じねばならない。例えば、HTML5のHTML構文では内容を含まないp要素を "<code>

</code>" のように書くことはできない。

XML仕様においては、空要素 (empty elements) は内容を含まない要素のことである\[20\]。HTML5のXHTML構文では、空要素は直後に終了タグを伴う開始タグ（例："
</br>"）、あるいは空要素タグ（Empty-Elements。例："
"）のどちらでも表現できる。

### HTML5 の要素と属性

nav要素（ナビゲーションのブロック用）や footer要素（作者や著作権の状態を表すまとまり用）や section要素（節）や progress要素（進捗状況）など、特別な意味を持つ要素が追加される。これらは検索エンジンのインデックス作業を容易にする。また、マルチメディアのための audio要素や video要素や2次元[ビットマップ画像](https://ja.wikipedia.org/wiki/ビットマップ画像 "wikilink")を描画するための canvas要素も追加される。

HTML 4.01で非推奨だった font要素や center要素などの[CSSによって実現されるべきマークアップはすべて廃止されることとしている](../Page/Cascading_Style_Sheets.md "wikilink")。acronym要素も廃止され、abbr要素に一本化される。

lang属性は、XHTML構文における xml:lang属性のように空の文字列をとり得る。

### 新しいAPI

HTML5ではマークアップだけでなく、[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") も新しく追加された。たとえば、以下のようなものである。

  - ビデオやオーディオの再生
  - 保存
  - オフライン
  - 編集
  - ドラッグ&ドロップ
  - 戻るボタン
  - Webページ上のメニュー

### エラーの取り扱い

HTML5 (`text/html`) 対応ブラウザは間違った構文を柔軟に処理できる。HTML5は、古いブラウザが新しいHTML5の構造を安全に無視することが出来るように設計されている。HTML 4.01とは対照的に、HTML5は対応したブラウザであれば間違った構文に対して同じ結果となるように、[字句解析](../Page/字句解析.md "wikilink")と[構文解析](../Page/構文解析.md "wikilink")のための詳細な規則を規定している\[21\]。

## 既存技術との競合

### Adobe Flash

2010年頃までに急速に普及した[アップルの](../Page/アップル_\(企業\).md "wikilink")[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")と[iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")がFlash非対応を貫き、[スティーブ・ジョブズ](../Page/スティーブ・ジョブズ.md "wikilink")CEO（当時）がHTML5を支持しFlashを厳しく批判したことが大きな影響を与えた\[22\]。iPhoneやiPadにFlash対応を求める声は多かったが\[23\]\[24\]、特にスマートフォン向けでは徐々にFlashからHTML5への転換が進んでいる。

Flashの開発元である[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")は、かつて社をあげてFlashを擁護したが\[25\]\[26\]\[27\]、2011年11月には、モバイルブラウザー用のFlash Playerの開発中止を発表した\[28\]。（2013年には担当者でCTOだったケビン・リンチがAppleへ転職\[29\]）2017年現在、アドビはHTML5の推進に積極的であり、FlashからHTML5への変換ツールなどをリリースしている。

### モバイルアプリケーション

スマートフォン向けのアプリの多くは、HTML5で開発された[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")に置き換わるという見方がある。2011年にイギリスの[フィナンシャル・タイムズ](../Page/フィナンシャル・タイムズ.md "wikilink")紙がHTML5による購読アプリを発表し注目を集めた\[30\]\[31\]。アップルの[App Storeには審査や課金に関する制約が大きく](../Page/App_Store.md "wikilink")、[Android](../Page/Android.md "wikilink")では1つのアプリで様々なハードウェア仕様に対応する必要があるが、Webアプリケーションではそれらの制約を受けない。一方で各端末向けの公式アプリストアで配布されるネイティブアプリにもメリットはあるため、2012年時点では置き換えが大きく進んでいるわけではない。ただ、Android端末と[iOS](https://ja.wikipedia.org/wiki/iOS "wikilink")端末ではネイティブアプリの開発に際し全く別個の開発環境を要求されているのに対し、HTML5はほぼ完全に共通の技術を使え、しかもHTML5で開発したアプリをネイティブアプリにすることも可能になっているため、ネイティブアプリ開発でHTML5が利用されることも少なくない。

## video要素

## 脚注

## 外部リンク

  - [HTML5 W3C Recommendation](https://www.w3.org/TR/html5/)
      - [（日本語訳）HTML5](https://momdo.github.io/html5/Overview.html)
  - [HTML 5.1 W3C Recommendation](https://www.w3.org/TR/html51/)
      - [（日本語訳）HTML 5.1](https://momdo.github.io/html51/Overview.html)
  - [HTML 5.2 W3C Recommendation](https://www.w3.org/TR/html52/)
  - [HTML 5.3](https://www.w3.org/TR/html53/)
  - [HTML5 differences from HTML4](https://www.w3.org/TR/html5-diff/)
      - [（日本語訳）HTML4からのHTML5の差分](https://momdo.github.io/html5-diff/)
  - [HTML Living Standard](https://html.spec.whatwg.org/multipage/)
      - [（日本語訳）HTML Living Standard](https://momdo.github.io/html/)

[Category:HTML5](https://ja.wikipedia.org/wiki/Category:HTML5 "wikilink") [Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink") [Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:2014年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2014年のソフトウェア "wikilink")

1.  [HTML5勧告–オープン・ウェブ・プラットフォームの重要なマイルストーンを達成](http://www.w3.org/2014/10/html5-rec.html.ja)
2.  [HTML 5.1 is a W3C Recommendation | W3C News](https://www.w3.org/blog/news/archives/5932)
3.  [HTML 5.2 is done, HTML 5.3 is coming | W3C Blog](https://www.w3.org/blog/2017/12/html-5-2-is-done-html-5-3-is-coming/)
4.  [The WHATWG Blog » Blog Archive » Spelling HTML5](http://blog.whatwg.org/spelling-html5)
5.  [The WHATWG Blog » Blog Archive » XHTML5 in a nutshell](http://blog.whatwg.org/xhtml5-in-a-nutshell)
6.  [HTML 5 + XML = XHTML 5 | HTML5 Doctor](http://html5doctor.com/html-5-xml-xhtml-5/)
7.
8.
9.  [W3C HTML5 Logo](http://www.w3.org/html/logo/)
10.
11.
12.
13.
14. [4.2.5.5. Specifying the document’s character encoding](https://www.w3.org/TR/html/document-metadata.html#specifying-the-documents-character-encoding)
15. 終了区切り子を省略したタグは「閉じないタグ」と呼ばれた。JIS X 4151 "閉じない開始タグ" "閉じない終了タグ"
16. ただし、単に内容がないだけの要素を空要素と呼ぶこともある。このため、単に内容がない要素との区別のために、SGMLの付属書Kなどでは強制空要素 (mandatorily empty element) という用語も使われる。
17. SGML規格に付属書Kが加わる以前には、空要素の終了タグを記述すること自体が禁止されており。また、付属書Kを参照したHTML 4.01やISO/IEC 15445 でも、HTML4以前と同様に空要素の終了タグを記述してはならないこととなった。またいずれのHTML規格でもNETは "/" だった。
18. 原文HTML5仕様 "Void elements can't have any contents (since there's no end tag, no content can be put between the start tag and the end tag)."
19. 原文HTML5仕様 "Void elements only have a start tag; end tags must not be specified for void elements"
20. 原文XML仕様 "An element with no content is said to be empty."
21.
22.
23.
24.
25. [AdobeのCTOがFlash擁護 「HTML5があればFlashは不要」論に反論](http://www.itmedia.co.jp/news/articles/1002/03/news057.html)、ITmedia、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[2月2日](../Page/2月2日.md "wikilink")
26. [アドビがFlash Catalystで考えていること HTML5はFlashの脅威か?エバンジェリストに聞いた](http://ascii.jp/elem/000/000/459/459590/)
27. [Flashは比べようもないほどHTML5より優れている](http://itpro.nikkeibp.co.jp/article/Interview/20091105/340042/)
28.
29. [Adobe CTO Kevin Lynch Headed to Apple](http://allthingsd.com/20130319/adobe-cto-kevin-lynch-headed-to-apple/)
30.
31.