> この記事は[HyperText Markup Language](https://ja.wikipedia.org/wiki/HyperText_Markup_Language)から翻訳されています。


（ハイパーテキスト マークアップ ランゲージ、**HTML**（エイチティーエムエル））は、[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")を記述するための[マークアップ言語](../Page/マークアップ言語.md "wikilink")の1つである。[World Wide Web](../Page/World_Wide_Web.md "wikilink") (WWW)において、[ウェブページ](../Page/ウェブページ.md "wikilink")（1990年代後半頃からは[コンテンツ](../Page/コンテンツ.md "wikilink")という語も利用されている。「中身」という意味の語であり、大層な意味は無い）を表現するために用いられる。[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")や画像等の[マルチメディア](../Page/マルチメディア.md "wikilink")を埋め込むハイパーテキストとしての機能、[見出し](../Page/見出し.md "wikilink")や[段落](../Page/段落.md "wikilink")といったドキュメントの抽象構造、[フォント](../Page/フォント.md "wikilink")や文字色の指定などの見た目の指定、などといった機能がある。

2019年6月以降\[1\]、[WHATWG](../Page/Web_Hypertext_Application_Technology_Working_Group.md "wikilink") により仕様が作られ、それが[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")となる流れになっている（ただし、この体制になってから[W3C勧告](https://ja.wikipedia.org/wiki/W3C勧告 "wikilink")に至った仕様はまだ存在しない）。W3C は、[XML](../Page/Extensible_Markup_Language.md "wikilink") ベースの規格である [XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") の勧告も行っている。

## 特徴

HTMLは[木構造](../Page/木構造_\(データ構造\).md "wikilink")（[入子構造](../Page/ネスティング.md "wikilink")）の[マークアップ言語](../Page/マークアップ言語.md "wikilink")であり、[形式言語](../Page/形式言語.md "wikilink")である。「プレーンテキストの文書を要素で括って意味付け」という一般的な説明\[2\]は間違いである。「『タグ』と『タグ』で括られたもの全体」が「要素」（element）であり、タグすなわち要素ではない。マークアップ言語としての特徴は、先祖である[SGMLや](../Page/Standard_Generalized_Markup_Language.md "wikilink")、兄弟の[XMLと共通しているため](../Page/Extensible_Markup_Language.md "wikilink")、以下ではWWWという[システム](../Page/システム.md "wikilink")における「[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")記述言語」としての側面についてのみ記述する。

HTMLの要素には、文書を表現するものとしてごく一般的なものである見出し（ヘッドライン、h1〜 ）、段落（パラグラフ、p ）、ハイパーテキストとして特徴的な「アンカー」（ a ）に関係するもの、画像など（ img など）の電子メディア的なもの、などがある。また文字色の指定などといった、意味ではなく直接見た目のみを指定するようなものは、近年ではスタイルシートなどに分離するべきとされているが、歴史的事情、及び、スタイルシートよりもこの、HTMLでの記述が簡便になる場合が度々あること\[3\]<sub>等</sub>から現在でもしばしば使われている。その他主要な要素は、[HTMLの要素の記事で解説している](../Page/HTML要素.md "wikilink")。

形式言語として見た場合「構文規則」（あるいは文法）に相当する「スキーマ」は、HTML4までは[DTDとして公開され要素ごとに記載することの出来る属性](../Page/Document_Type_Definition.md "wikilink")、内容に含むことの出来る要素などが定められていた。HTML 4.01 では厳密なもの\[4\]、HTML 3.2 からの移行過渡期のためのもの\[5\]、フレームを用いた文書のためのもの\[6\]といった3つのDTDが定義されていた。

HTML 3.2 では見た目を左右する要素や属性が追加されたがHTMLは本来文書構造を示すためだけにその存在意義があり、それらの要素は目的に反するものとされた。そのため視覚的・感覚的効果を定義する手段として[スタイルシート](../Page/スタイルシート.md "wikilink")（一般にはその中の[CSS](../Page/Cascading_Style_Sheets.md "wikilink")）が考案された。見た目を左右する要素や属性の一部は HTML4 以降では非推奨とされており、HTML 4.01  では定義されていないので使用できない。ただし HTML 4.01  で定義され、非推奨とされない要素や属性の一部にも見た目を左右するものがある。装飾的な視覚表現のためにそれらの要素や属性を用いているのであればその内容に適する要素を用いた上で、スタイルシートで表現を指定するのが望ましい。

## HTML文書

HTML で書かれた文書をHTML文書と言い、HTML では、まず[文書型宣言](https://ja.wikipedia.org/wiki/文書型宣言 "wikilink")を書く。文書型宣言が無いものは、HTML の規格に従っているとはいえない。HTML5 の文書型宣言は以下のようなものである。HTML4 までは [Document Type Definition](../Page/Document_Type_Definition.md "wikilink") (DTD) によって定義される書式に沿って記述しなければならなく、DTD は文書型宣言（ 宣言）で宣言したバージョンのものが選択された。

``` html5
<!DOCTYPE html>
```

次にHTML文書の例を挙げる。

``` html5
<!DOCTYPE html>
<html lang="ja">
 <head>
  <meta charset="UTF-8">
  <link rel="author" href="mailto:mail@example.com">
  <title lang="en">HyperText Markup Language - Wikipedia</title>
 </head>
 <body>
  <article>
   <h1 lang="en">HyperText Markup Language</h1>
   <p>HTMLは、<a href="http://ja.wikipedia.org/wiki/SGML">SGML</a>
      アプリケーションの一つで、ハイパーテキストを利用してワールド
      ワイドウェブ上で情報を発信するために作られ、
      ワールドワイドウェブの<strong>基幹的役割</strong>をなしている。
      情報を発信するための文書構造を定義するために使われ、
      ある程度機械が理解可能な言語で、
      写真の埋め込みや、フォームの作成、
      ハイパーテキストによるHTML間の連携が可能である。</p>
  </article>
 </body>
</html>
```

このHTML文書は次のような構造を示している。

  - `<!DOCTYPE html>`:文書型宣言
    このテキストが**HTML5**であることを示す。
  - `<html lang="ja">`:html 要素。また、`lang="ja"`で、言語コード `ja` の言語が使われていることの明示。
      - `<head>`:head 要素（この文書のヘッダ情報の明示）
          - `<meta`:meta要素（文書のメタ情報）。ここでは、`charset="UTF-8"`で、文字コードが、「**[UTF-8](../Page/UTF-8.md "wikilink")**」であることを示す。
          - `link` 要素（他のリソースとの関連を明示。この場合、作者の明示）
          - `<title lang="en">`:title 要素（この文書のタイトル)の明示。また、この部分は `en` の言語が使われていることの明示。
      - `<body>`:body要素（この文書の内容の明示）
          - `<article>`:article 要素（この要素が、記事であることを明示）
              - `<h1 lang="en">`:h1要素（第一レベル)の見出しを明示。また、`lang="en">`で、この部分の見出しは `en` の言語が使われていることを明示。
              - `<p>`:p(段落)要素の明示。
                  - `<a href="http://ja.wikipedia.org/wiki/SGML/">SGML</a>`:a(アンカー)要素（他のリソースへのアンカー)であることの明示。`href`で、「`""`」内にリンク先の[URL](https://ja.wikipedia.org/wiki/URL "wikilink")を記述する。ちなみに、この[URL](https://ja.wikipedia.org/wiki/URL "wikilink")の場合は、WIKIPEDIA 日本語版の[SGML](https://ja.wikipedia.org/wiki/SGML "wikilink")の記事。
                  - `<strong>`:strong 要素（強い強調であることの明示）

タグによって文字列を括ることによりその文字列の意味付けがなされる。ユーザエージェントはそれを解釈して、例えば GUI によるウェブブラウザであれば `strong` 要素で括られたテキストを太字として表示するなどする。また、スタイルシートを用いることで見た目などを指定することができるようになっている。 尚、テキストエディターで改行をしても、ウェブブラウザ上では `br` 要素がなければ改行はされない。

### 要素

[W3C勧告の](../Page/World_Wide_Web_Consortium.md "wikilink") HTML4.01 仕様書で、要素はタグではない\[7\]としている\[8\]。「タグ」とは、文字「`<`」で始まり、文字「`>`」で終わっている部分（マークアップ）のみを指し、「要素」（エレメント）は開始タグ～終了タグに囲まれた全体を指す概念である。
のように、開始タグと終了タグを兼ねる一つのタグのみで一つの要素を構成する場合もあるが、あくまでタグと要素の概念は別物である。

### 属性

要素にid、class、styleなどの属性を付与することができる。

## 歴史

[1989年](../Page/1989年.md "wikilink")、[CERN](https://ja.wikipedia.org/wiki/CERN "wikilink")の[ティム・バーナーズ＝リー](../Page/ティム・バーナーズ＝リー.md "wikilink")は、オリジナルのHTML（および多くの関連したプロトコル、[HTTPなど](../Page/Hypertext_Transfer_Protocol.md "wikilink")）のメモを提案し、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")5月にコード化した\[9\]。[NEXTSTEP](../Page/NEXTSTEP.md "wikilink")の動作する[NeXTcube](../Page/NeXTcube.md "wikilink")ワークステーション上で開発された。当時のHTMLは仕様ではなく、直面していた問題を解決するためのツール群であった。直面していた問題とは、ティム・バーナーズ＝リーやその同僚たちがどのように情報や進行中の研究を共有するかということである。彼の成果は後に国際的かつ公開のネットワークの出現として結実し、世界的な注目を集めることになった。

HTML の初期のバージョンはゆるい文法規則によって定義されており、ウェブ技術になじみのない層に受け入れられる助けとなった。[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")はウェブページの意図を推測し、レンダリングを実行するのが一般的であった。やがて公式規格においては厳格な言語構文を作ることを志向するようになっていったが、それに加え、ウェブブラウザの挙動を元に構文エラーの取り扱いも規格に含めることで、既存のウェブページに対する互換性の維持が図られている\[10\]。

HTML が公式な仕様として定義されたのは[1990年代](../Page/1990年代.md "wikilink")からである。それは従来のマークアップ言語である[SGMLに](../Page/Standard_Generalized_Markup_Language.md "wikilink")、[インターネット](../Page/インターネット.md "wikilink")のための[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")の機能を取り入れるというティム・バーナーズ＝リーの提案に大きく影響を受けたものだった。

[1993年](../Page/1993年.md "wikilink")には[IETFからHTML仕様書バージョン](../Page/Internet_Engineering_Task_Force.md "wikilink") 1.0が公開され、SGMLからの拡張として文法定義の[DTDを持つようになった](../Page/Document_Type_Definition.md "wikilink")。また[1994年](../Page/1994年.md "wikilink")にIETFのHTMLワーキンググループが発足した。しかし、2.0以降のIETFの元での開発は他の開発との競合から停滞した。[1996年](../Page/1996年.md "wikilink")からは[W3Cによって商用ソフトウェア](../Page/World_Wide_Web_Consortium.md "wikilink")・ベンダーからの支援も受け、HTMLの仕様が標準化されている\[11\]。また[2000年](../Page/2000年.md "wikilink")からは国際標準ともなった（[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](../Page/国際電気標準会議.md "wikilink") 15445:2000）。W3Cから勧告された最新のHTML仕様はHTML 5.2である。

### HTML 1.0、HTML+

[1993年](../Page/1993年.md "wikilink")6月に、IETFのIIIR Workingグループより提出された[HTML仕様書](https://www.w3.org/MarkUp/draft-ietf-iiir-html-01.txt)がインターネット・ドラフトとして発表された。本来はバージョン番号が付いていないが通常HTML 1.0と呼ぶ。このドラフトはティム・バーナーズ＝リーおよびダニエル・コノリーによって、ティム・バーナーズ＝リーの出した [HTML Design Constraints](https://www.w3.org/MarkUp/HTMLConstraints.html) に極力従うように書かれた。

1993年11月に、HTML の上位互換な HTML+ が発表された。テーブルなどが追加になっている。[HTML+仕様書](https://www.w3.org/MarkUp/HTMLPlus/htmlplus_1.html)。

### HTML 2.0

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")11月に、IETFのHTMLワーキンググループによって RFC 1866 （[日本語訳](https://web.archive.org/web/20010815115248/http://www.asahi-net.or.jp/~bd9y-ktu/W3C20/html-spec_toc.html)） として仕様が発表された。下記の補助的な RFC もリリースされた。HTML 2.0 は RFC 2854 によって廃止され HTML は IETF ではなく W3C が管理することとなった。

  - 1995年11月：フォームベースのファイルアップロード。RFC 1867
  - 1996年5月：テーブル。RFC 1942
  - 1996年8月：クライアントサイドイメージマップ。RFC 1980
  - 1997年1月：HTMLの国際化。RFC 2070（[非公式な日本語訳](https://hp.vector.co.jp/authors/VA014833/rfc2070J.html)）。「HTML i18n」とも呼ばれる。日本語を扱えるHTMLのバージョンとしては、最も古い。

### HTML 3.0、HTML 3.2

HTML 3.0は策定作業が行われたが、ドラフトの段階で策定途中に破棄された。[HTML 3.0仕様書](https://www.w3.org/MarkUp/html3/)。

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[1月14日](../Page/1月14日.md "wikilink")に、HTML 3.2 がW3C勧告として仕様が発表された。[HTML 3.2 Reference Specification](https://www.w3.org/TR/2018/SPSD-html32-20180315/)（[非公式な日本語訳](http://www.doraneko.org/webauth/html32/html32.html)）。

### HTML 4.0、HTML 4.01

1997年[12月18日](../Page/12月18日.md "wikilink")に、W3C勧告としてHTML 4.0の仕様が発表された。HTML 4.0は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")[4月24日](../Page/4月24日.md "wikilink")に仕様が改訂\[12\]された。この仕様にいくらかのマイナーな修正が加えられたHTML 4.01は[1999年](../Page/1999年.md "wikilink")[12月24日](../Page/12月24日.md "wikilink")にW3C勧告となった。 の他にHTML 3.2からの移行過渡期のための  とフレームを使うことのできる  の3つのスキーマを持つ。

この後、HTML 4.01をベースとして[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink") 1.0が策定されることになる。

[2018年](../Page/2018年.md "wikilink")[3月28日](../Page/3月28日.md "wikilink")に代替された勧告に指定され、最新の勧告を参照することを推奨されている。

  - [](https://www.w3.org/TR/REC-html40-971218/)
  - [](https://www.w3.org/TR/1998/REC-html40-19980424/)
      - [日本規格協会による和訳を原案とする経済産業省の標準情報 TR X 0033:2002](http://www.y-adagio.com/public/standards/tr_html4_rev/toc.html)
  - [](https://www.w3.org/TR/html401/)
      - [内田明らによる和訳](http://www.asahi-net.or.jp/~sd5a-ucd/rec-html401j/cover.html)

### ISO/IEC 15445:2000

[ISO/IEC JTC 1による規格](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")。HTML 4.01を参考にし、より厳密に規格化された。これは[2000年](../Page/2000年.md "wikilink")に翻訳され JIS X 4156:2000 という[JIS規格になった](../Page/日本産業規格.md "wikilink")。

ISO/IEC 15445:2000は[2003年](../Page/2003年.md "wikilink")に訂正版\[13\]が発行された（ただし訂正なので、その後も名称はISO/IEC 15445:2000のまま）。JIS X 4156は[2005年](../Page/2005年.md "wikilink")に改正され、となっている。

### HTML5、HTML 5.1、HTML 5.2

その後、HTMLの改良にW3Cが興味を示さなかったことから、2004年に[WHATWG](https://ja.wikipedia.org/wiki/WHATWG "wikilink")が開発を開始した\[14\]。2007年には、W3Cもワーキンググループを設立し\[15\]、WHATWGと共同での開発が始まった。しかし、2012年7月、両者は別個に作業する体制となった\[16\]。WHATWGの仕様策定はHTML Living Standardとして継続している。

[2014年](../Page/2014年.md "wikilink")[10月28日](https://ja.wikipedia.org/wiki/10月28日 "wikilink")に HTML5 が W3C より勧告された\[17\]。ブログや記事向けの「article」要素やマルチメディアのための「audio」および「video」要素などをはじめとした新要素・属性が追加され、以前は見た目を規定していた要素の殆どは変更または削除された。[2016年](../Page/2016年.md "wikilink")[11月1日](../Page/11月1日.md "wikilink")に HTML 5.1 が勧告され\[18\]、[2017年](../Page/2017年.md "wikilink")[12月14日](../Page/12月14日.md "wikilink")に HTML 5.2 が勧告された\[19\]。

  - [HTML5関連仕様のメモ](https://github.com/momdo/momdo.github.io/wiki/html5)
  - [HTML5.JP](http://html5.jp/)

W3CによるHTML5～HTML 5.2は、WHATWGのHTML Living Standardを元に編集が加えられたものであり、HTML Living Standardとの差異が発生している状態となっていた。これについてWHATWGのがW3C側を強く非難する事態となっている\[20\]。W3CはHTML 5.3への作業を進められていたものの、2019年のWHATWGとの合意により、取りやめている\[21\]。

### HTML Living Standard

HTML Living Standard\[22\] は [WHATWG](../Page/Web_Hypertext_Application_Technology_Working_Group.md "wikilink") が更新し続けている HTML の最新仕様。2019年まではW3CのHTML5～HTML 5.2と並行して仕様策定が進められている状態だった。これを元にして W3C の勧告が作られている。

## HTML形式の電子メール

## 脚注

## 関連項目

  - \- SGML。汎用マークアップ言語。

  - \- XHTML。XMLで作ったHTML。

  - \- HDML。携帯端末用のHTML。

  - \- AMP。Googleらによる、モバイル（携帯）端末でのウェブページの表示の高速化を目指すプロジェクト。HTMLのサブセットとなるAMP HTMLを規定している。

  - \- CSS。表示方法・音声化方法を定義する設定ファイル。

  - [ダイナミックHTML](../Page/ダイナミックHTML.md "wikilink") - ユーザの操作で内容が変化するHTML文書。

  - [ユーザビリティ](../Page/ユーザビリティ.md "wikilink") - 利便性。

  - [アクセシビリティ](../Page/アクセシビリティ.md "wikilink") - 環境に依存しないアクセス容易性。

  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink") - HTML文書を表示するシステム。

  - [HTMLレンダリングエンジン](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink") - HTML文書を表示・音声化・点字化するシステムの核。

  - [文字参照](../Page/文字参照.md "wikilink") - 特殊な文字を表現する符号。

  - \- 通信規約。

  - [{{lang](../Page/Webオーサリングツール.md "wikilink") - ウェブ文書を視覚的に作成するシステム。

  - \- HTML文書を検証するソフトウェア。

## 外部リンク

  - [W3Cの最新のHTML仕様](https://www.w3.org/TR/html/)

  - [WHATWGの最新のHTML仕様](https://html.spec.whatwg.org/multipage/)

  - [W3C Markup Validation Service](https://validator.w3.org/index.html) - [W3C](https://ja.wikipedia.org/wiki/W3C "wikilink")による構文チェック

  - [ごく簡単なHTMLの説明](https://www.kanzaki.com/docs/htminfo.html)

[Category:マークアップ言語](https://ja.wikipedia.org/wiki/Category:マークアップ言語 "wikilink") [Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink") [Category:World_Wide_Web](https://ja.wikipedia.org/wiki/Category:World_Wide_Web "wikilink") [Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.
2.
3.  例えば、太字指定の「**\<b\>\</b\>**」<sub>等</sub>
4.
5.
6.
7.
8.  [](http://www.w3.org/TR/1999/REC-html401-19991224/intro/sgmltut.html#h-3.2.1)、1999年12月24日
9.
10.
11.
12.
13.
14.
15.
16.
17. [HTML5勧告–オープン・ウェブ・プラットフォームの重要なマイルストーンを達成](http://www.w3.org/2014/10/html5-rec.html.ja)
18. [HTML 5.1 is a W3C Recommendation | W3C News](https://www.w3.org/blog/news/archives/5932)
19. [HTML 5.2 is done, HTML 5.3 is coming | W3C Blog](https://www.w3.org/blog/2017/12/html-5-2-is-done-html-5-3-is-coming/)
20.
21.
22. [HTML Living Standard](https://whatwg.org/html)