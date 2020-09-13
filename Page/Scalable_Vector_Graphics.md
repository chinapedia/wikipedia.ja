> この記事は[Scalable Vector Graphics](https://ja.wikipedia.org/wiki/Scalable_Vector_Graphics)から翻訳されています。


**Scalable Vector Graphics**（スケーラブル・ベクター・グラフィックス、**SVG**、）は、[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")、2次元[ベクターイメージ](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")用の[画像形式の](https://ja.wikipedia.org/wiki/画像フォーマット "wikilink")1つである。アニメーションやユーザインタラクションもサポートしている。SVGの仕様は[W3Cによって開発され](../Page/World_Wide_Web_Consortium.md "wikilink")、[オープン標準](../Page/オープン標準.md "wikilink")として勧告されている。

## 概要

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に[Adobe Systems](../Page/アドビシステムズ.md "wikilink")・[IBM](../Page/IBM.md "wikilink")・[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")の3社によって提案された(Precision Graphics Markup Language)\[1\]と、[Autodesk](../Page/オートデスク.md "wikilink")・[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")・[Macromedia](../Page/マクロメディア.md "wikilink")・[マイクロソフト](../Page/マイクロソフト.md "wikilink")・ の5社によって提案された [VML](../Page/Vector_Markup_Language.md "wikilink") (Vector Markup Language)\[2\]をもとにして、W3C SVG ワーキンググループにより開発された\[3\]。

## 沿革

  - [1999年](../Page/1999年.md "wikilink")2月11日 - SVGのドラフト版を公表\[4\]
  - [2001年](../Page/2001年.md "wikilink")9月4日 - SVG 1.0が[W3C勧告となる](../Page/World_Wide_Web_Consortium.md "wikilink")\[5\]
  - [2003年](../Page/2003年.md "wikilink")1月14日 - SVG 1.1\[6\]と、SVG Tiny・SVG Basic（モバイルSVGプロファイル）\[7\]がW3C勧告となる
  - [2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")12月22日 - SVG Tiny 1.2がW3C勧告となる\[8\]
  - [2011年](../Page/2011年.md "wikilink")8月16日 - 誤記を修正したSVG 1.1 (Second Edition)がW3C勧告となる\[9\]
  - [2018年](../Page/2018年.md "wikilink")10月4日 - SVG 2がW3C勧告候補となる\[10\]

## 特徴

[ベクタ形式](https://ja.wikipedia.org/wiki/ベクタ形式 "wikilink")であるため、拡縮自在である。その他に、XMLベースの為、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")で（画像として、という意味ではなく、HTMLのソースビュー等と同様に、という意味で）閲覧でき、[テキストエディタ](../Page/テキストエディタ.md "wikilink")等で編集できる。また、HTMLとの親和性により、[ハイパーリンク](../Page/ハイパーリンク.md "wikilink")を埋め込んだり、[JavaScript](../Page/JavaScript.md "wikilink") 等と連携させることもできる。 ウィキペディアにおいても、ウィキペディアのロゴやアイコンなどでSVGが使われている。 [代替文=SVG 円](https://ja.wikipedia.org/wiki/ファイル:SVG_Circle.svg "wikilink")

### 編集

SVG は、拡張の自由度が高い [XML](../Page/Extensible_Markup_Language.md "wikilink") () で記述されており、XML ならではの各種機能を定義した要素を持つ。SVG ではそれ自身に回転・拡大・移動などの表現を定義しているため、単体で多様な表現をすることが可能である。

従来のウェブサイトでは、いわゆるインタラクティブな双方性のある画面変化を伴う表示を JavaScript や FLASH を用いてきた。HTML/XHTML に SVG を組み合わせることにより、JavaScript や FLASH を導入せずとも同様の効果が発揮されることが期待される。

XML なので、原理的には専用のアプリケーションを用いることなく通常の[テキストファイル](../Page/テキストファイル.md "wikilink")として作製・編集できる。

### レイヤー

[thumb](https://ja.wikipedia.org/wiki/ファイル:Bitmap_VS_SVG.svg "wikilink") SVG の特筆すべき点としてレイヤー機能がある。SVG では写真や挿絵などのビットマップデータ部分と座標値で指定された円・線分等を組み合わせた図形をベクターデータ部分として個々に指定でき、互いの苦手とする部分を補完しながら共存して画面表示できる。

  - ビットマップデータ: 写真・挿絵・統計グラフ
  - ベクターデータ: 円弧・線分・点・文字・統計グラフ

SVG では文字をベクター情報の領域に有することで拡大縮小した際にはアウトラインフォントで表現する。この機能により、拡大すると[ジャギー](https://ja.wikipedia.org/wiki/ジャギー "wikilink")と呼ばれる文字外延部のギザギザが生じて見にくくなる点が解決されている。具体的には Adobe Acrobat による PDF 形式の文字とほぼ同じ機能を有する。

これらのレイヤー機能により、背景に写真などの画像を置き、ベクターデータによる線画や文字を配置させることが可能である。具体的には等高線を表示した地図画像（ビットマップ）の上に鉄道路線や道路網（ベクターデータ）を重ね、電車や自動車等の移動体を配置して同時表示が可能になる。更に、ベクターデータのみで表現した塗りつぶしでは色の重ね合わせが可能であり、塗りつぶしの透過度の指定により集合論で用いるベン図のような形を必要最低限度の色数で表現できる。

### ファイル形式

基本的に SVG は [MIME 形式指定では](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink") image/svg+xml で指定された画像フォーマットである。ファイルの拡張子は .svg と gzip 圧縮された .svgz がある。拡張子 .svg はテキストファイルであるため、大きなデータではネット間の通信トラフィックにおいてのデメリットが大きいが、圧縮した .svgz では数分の一のファイルサイズになる。展開機能はWebブラウザ側が受け持つ。

### 親和性

SVG は基本的に文章で構成されており、ブラウザの利用者が入力した情報を CGI や JavaScript を介して SVG データに組み入れることが可能である。これにより、ベクターデータを用いた統計グラフでは可変性のある表示が可能になる。

### 長所

文書で制作できるため、独自タグを用いることで高品質な表現が可能である。文字情報は文字データのみを明示的にグループ化しているため、文字のグループのみを抽出することで多言語化が比較的容易にできる。

### 欠点

ビットマップデータの大きさは各形式によってある程度左右されるが、ほぼ面積比によってある程度のサイズに納まることが多い。それに対し、ベクターデータは画面表示サイズに関わらず全ての情報を常に保持し続けるため、表示情報が多い場合はビットマップデータよりもサイズが大きくなる傾向がある（ただし、これはベクターデータ形式全般に言えるものであり、SVG のみの欠点ではない）。

## 規格の概要

  - SVG 1.1
  - SVG Tiny
  - SVG Basic
      - [携帯電話](../Page/携帯電話.md "wikilink")や[携帯情報端末](../Page/携帯情報端末.md "wikilink")等の[携帯情報機器](https://ja.wikipedia.org/wiki/携帯情報機器 "wikilink")を対象にした軽量規格。
  - SVG 2

### 現状

SVG は版を重ねるごとに高度な機能を盛り込んでいる。1.1 版以降から、格納しようとする描画情報に当該情報が使用している[座標](../Page/座標.md "wikilink")参照系を[メタデータ](../Page/メタデータ.md "wikilink")として記述することが可能となった。これにより、SVG を地図として利活用できる道ができ、[国土地理院](../Page/国土地理院.md "wikilink")ではその保有する[電子国土](../Page/電子国土.md "wikilink")基幹情報を SVG で配信し、PC のみならず様々な媒体で活用する方法を提案して広く社会実験に供する試みを実施している。

一方で、SVG の高度な機能を用いるものでは、それに対応した編集ツールや、データを忠実に再現してくれるビューアやブラウザのプラグイン等が必須となる。高度な機能を持ちつつも、それを活かせるインフラが追いついていないのが現状である。

これとは別に、比較的利用頻度の高い重要な機能に絞り込み、小型機器にも搭載可能な軽量な規格も登場している。

### 日本産業規格

**JIS X 4197:2012**「可変ベクタグラフィクス SVG Tiny1.2」としてW3C発行のSVG Tiny 1.2規格を技術的内容を変更することなく邦訳した規格表が発行されている（2012年最終改訂）\[11\]。

## SVG 編集ソフト

SVG は [XML](../Page/Extensible_Markup_Language.md "wikilink") を用いているのでテキストエディタによるデータの作成も一応可能であるが、記述は非常に複雑なため実用的には [GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink") を前提にした編集ソフトが必須となる。

用途により、高度なグラフィクス作成に主眼を置いた[描画ソフトから図](https://ja.wikipedia.org/wiki/グラフィックソフト "wikilink")、表、フローチャートなどの作成に主眼を置いたソフトまで幅がある。

  - SVG を標準データとして扱い、読み書きが可能なもの

:\* SVG Cats

:\* [Inkscape](../Page/Inkscape.md "wikilink")

  - SVG の読み書きが可能なもの

:\*[Adobe Illustrator](../Page/Adobe_Illustrator.md "wikilink")

:\* [Microsoft Office Visio](../Page/Microsoft_Visio.md "wikilink")

:\* [Microsoft Officeのうち](../Page/Microsoft_Office.md "wikilink")、Word、Excel、PowerPoint、Outlook\[12\]\[13\]。

:\* [CorelDRAW](../Page/CorelDRAW.md "wikilink")

:\*[Affinity Designer](https://ja.wikipedia.org/wiki/Affinity_Designer "wikilink")

:\*[Justsystems](https://ja.wikipedia.org/wiki/Justsystems "wikilink") [Xfy](../Page/Xfy.md "wikilink")

:\*[Dia](../Page/Dia_\(ソフトウェア\).md "wikilink")

:\*[Mathematica](../Page/Mathematica.md "wikilink")

:\*[LibreOffice Draw](https://ja.wikipedia.org/wiki/LibreOffice_Draw "wikilink")

:\*[Googleドキュメント](https://ja.wikipedia.org/wiki/Googleドキュメント "wikilink")

  - 一部制限があるもの

:\* [GIMP](../Page/GIMP.md "wikilink") - 読み込みに対応。書き出しはパスの書き出しのみ。

  - SVG の出力が可能なもの

:\*[花子](../Page/花子_\(グラフィックソフト\).md "wikilink")2006は、SVG (Ver.1.0 に準拠) の書き出しに対応。

:\* [OpenOffice](../Page/OpenOffice.org.md "wikilink") Draw - 1.1 までは日本語出力が一部乱れるなど難あり。2.0 から書き出しに対応。[SVG Import Filter](https://web.archive.org/web/20080701061453/http://www.ipd.uka.de/~hauma/svg-import/#download)<small>(アーカイブ)</small>\[14\]を導入すれば読み込みも可能。

:\* Omni Groupの[OmniGraffle](https://ja.wikipedia.org/wiki/OmniGraffle "wikilink") Professional 4 は、SVG 書き出しに対応。

:\* [R](../Page/R言語.md "wikilink") はデータ解析結果のグラフ出力形式として SVG に対応。

:\* [Gnuplot](../Page/Gnuplot.md "wikilink") および GNU [Plotutils](https://ja.wikipedia.org/wiki/Plotutils "wikilink") は、プロットの出力形式として SVG に対応。

:\* [Geometry Expressions](https://ja.wikipedia.org/wiki/Geometry_Expressions "wikilink") は、図形の出力形式として SVG に対応。

この他、[CAD](../Page/CAD.md "wikilink") ソフトウエアには読み書きともに対応しているものが多く存在する。

## ウェブブラウザによる SVG 画像の表示

2011年現在、パソコン用の主要[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")でネイティブサポートされている。しかし、[Internet Explorer 8](https://ja.wikipedia.org/wiki/Internet_Explorer_8 "wikilink") 以前のマイクロソフト製のレンダリングエンジンを用いているブラウザでは対応していない。これに対し、[Internet Explorer 9](https://ja.wikipedia.org/wiki/Internet_Explorer_9 "wikilink") 以上に移行するか、[第三者製の](../Page/サードパーティー.md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")を用いることで、SVG 画像を表示させることができる。

2018年5月時点で\[15\]、HTML標準の仕様ではSVG 2を参照している。さらに、SVGを実装するならそれ以前のバージョンではなくSVG 2を実装しなければならないと規定されている\[16\]。

### ネイティブサポート

  - [Internet Explorer 9](https://ja.wikipedia.org/wiki/Internet_Explorer_9 "wikilink") は、SVG 1.1 に標準対応している\[17\]。
  - [Firefox](../Page/Mozilla_Firefox.md "wikilink") ([Gecko](../Page/Gecko.md "wikilink")) では、Firefox 1.5 から対応している。
  - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") は最初のバージョンから対応。
      - Android ブラウザは Android 3.0 から対応
  - [Safari](../Page/Safari.md "wikilink") は、Safari 3.0 から SVG 1.1 に完全ではないが対応した\[18\]。対応状況は環境毎に異なる。
      - OS X - バージョン 3.1.2 の時点で、[カラープロファイル](https://ja.wikipedia.org/wiki/カラープロファイル "wikilink")など一部機能を未実装。現状の対応状況は、[WebKit SVG Status](http://webkit.org/projects/svg/status.xml)。
      - Mobile - [iPhone OS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") 2.1 の [Mobile Safari](https://ja.wikipedia.org/wiki/Mobile_Safari "wikilink") で SVG に対応した。
      - Windows - Safari 3.1.2 現在、フィルタなど一部の機能を除いて、実装している。
  - [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink") および [Opera Mobile](https://ja.wikipedia.org/wiki/Opera_Mobile "wikilink") は2005年4月に発表された Opera v8.0 で SVG Tiny に、2006年発表の v9.0 で SVG Basic に対応した。
      - [Opera Mini](https://ja.wikipedia.org/wiki/Opera_Mini "wikilink") は 5 から対応。
  - [NetFront Browser](../Page/NetFront_Browser.md "wikilink") - 未対応
  - [KDE](../Page/KDE.md "wikilink") の [Konqueror](../Page/Konqueror.md "wikilink") は [KSVG](https://ja.wikipedia.org/wiki/KSVG "wikilink") を使って表示させることができる。
  - W3C の [Amaya](../Page/Amaya.md "wikilink") が標準対応している。

### プラグインサポート

  - Adobe - [Adobe SVG Viewer](http://www.adobe.com/jp/svg/viewer/install/)。[Internet Explorer](../Page/Internet_Explorer.md "wikilink") や [Netscape](../Page/Netscapeシリーズ.md "wikilink") 向け。
      - Adobe SVG Viewer は2009年1月1日にサポートを終了と発表した。配布の終了は未定である[1](http://www.adobe.com/svg/viewer/install/main.html)。
  - Corel - [Corel SVG Viewer](http://www.corel.com/servlet/Satellite?pagename=Corel2/Products/Content&pid=1047023276653&cid=1047023286996)
  - [GNOME](../Page/GNOME.md "wikilink") - [Mozilla](../Page/Mozilla.md "wikilink") 向けにプラグインの [librsvg](https://ja.wikipedia.org/wiki/librsvg "wikilink")
  - Examotion（開発元が Emia Systems から移った） - [Renesis Player](http://www.examotion.com/index.php?id=product_player)
  - [SVG MAP コンソーシアム](http://blog.svg-map.com/) - 2007年9月6日に地図表示のための拡張機能を備えた SVG Viewer である[SVG Map Toolkit](http://blog.svg-map.com/2007/09/svgmaptoolkit.html)の提供を開始した。

## デスクトップ

[GNU/Linuxなどの](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink") [Unix系](../Page/Unix系.md "wikilink")OSでは、[Freedesktop.org](../Page/Freedesktop.org.md "wikilink") の標準に採用されるなど、様々な利用がされている。[GNOME](../Page/GNOME.md "wikilink") は [librsvg](https://ja.wikipedia.org/wiki/librsvg "wikilink") を使いアイコンや壁紙に SVG を利用でき、また、[KDE](../Page/KDE.md "wikilink") では [KSVG](https://ja.wikipedia.org/wiki/KSVG "wikilink") を利用してアイコンを表示できるほか 3.4 からは SVG を使った壁紙に対応した。

[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 系では2007年現在では特に動きはない。

## 脚注

### 出典

## 参考文献

  - \- SVG 1.0仕様の日本語訳 (TR)

  -
  -
## 関連項目

  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink") (Macromedia Flash)

  - [Apache Batik](../Page/Apache_Batik.md "wikilink")

  -
  - [Commons:SVG変換](https://ja.wikipedia.org/wiki/Commons:Commons:SVG変換 "wikilink")

  -
  - [Computer Graphics Metafile](https://ja.wikipedia.org/wiki/Computer_Graphics_Metafile "wikilink") (CGM)

  - [Direct2D](https://ja.wikipedia.org/wiki/Direct2D "wikilink")

  - [Extensible Markup Language](../Page/Extensible_Markup_Language.md "wikilink") (XML)

  -
  -
  -
  - [PostScript](../Page/PostScript.md "wikilink") (PS)- ベクタ形式の画像フォーマット

      - [Encapsulated PostScript](../Page/Encapsulated_PostScript.md "wikilink") (EPS) - ベクタ形式の画像フォーマット

  -
  -
  -
  -
  -
  - [WYSIWYG](../Page/WYSIWYG.md "wikilink")

  - [Windows Metafile](../Page/Windows_Metafile.md "wikilink") (WMF, EMF) - ベクタ形式の画像フォーマット

  - [ビットマップ画像](../Page/ビットマップ画像.md "wikilink")（ラスターグラフィック）

  - [ベクターイメージ](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")

## 外部リンク

  - [W3C の SVG 公式サイト](https://www.w3.org/Graphics/SVG/)
  - [Scalable Vector Graphics (SVG) 2](https://www.w3.org/TR/SVG2/)  - SVG 2の規格書
  - [SVG: Scalable Vector Graphics](https://developer.mozilla.org/ja/docs/Web/SVG)  - Mozillaによる、ウェブ開発者向けの説明

[Category:W3C勧告](https://ja.wikipedia.org/wiki/Category:W3C勧告 "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:ベクターグラフィックス・マークアップ言語](https://ja.wikipedia.org/wiki/Category:ベクターグラフィックス・マークアップ言語 "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.  “[Precision Graphics Markup Language (PGML)](https://www.w3.org/TR/1998/NOTE-PGML-19980410)”、World Wide Web Consortium、1998年4月10日
2.  “[VML - the Vector Markup Language](https://www.w3.org/TR/1998/NOTE-VML-19980513)”、World Wide Web Consortium、1998年5月13日
3.  「[W3C、Web上でベクターグラフィックを表示する「SVG」のドラフトを公開](https://internet.watch.impress.co.jp/www/article/1999/0212/svg.htm)」『INTERNET Watch』、インプレス、1999年2月12日
4.  “[W3C Working Draft: Scalable Vector Graphics (SVG)](https://www.w3.org/TR/1999/WD-SVG-19990211/)”、World Wide Web Consortium、1999年2月11日
5.  “[Scalable Vector Graphics (SVG) 1.0 Specification](https://www.w3.org/TR/SVG10/)”、World Wide Web Consortium、2001年9月4日
6.  “[Scalable Vector Graphics (SVG) 1.1 (Second Edition)](https://www.w3.org/TR/SVG11/)”、World Wide Web Consortium、2011年8月16日
7.  “[Mobile SVG Profiles: SVG Tiny and SVG Basic](https://www.w3.org/TR/SVGTiny/)”、World Wide Web Consortium、2003年1月14日
8.  “[Scalable Vector Graphics (SVG) Tiny 1.2 Specification](https://www.w3.org/TR/SVGTiny12/)”、World Wide Web Consortium、2008年12月22日
9.
10. “[Scalable Vector Graphics (SVG) 2](https://www.w3.org/TR/SVG2/)”、World Wide Web Consortium、2018年10月4日
11. JIS X 4197
12.
13.
14. SVG Import Filterのアーカイブ版はVersion 1.2.2 (2007-09-02) 以降、アップデートされていない。(アーカイブ版に更新日時：\~\~\~\~\~)
15.
16.
17. [SVG in IE9 Roadmap - Internet Explorer ブログ (日本語版)](http://blogs.msdn.com/b/ie_jp/archive/2010/04/14/svg-in-ie9-roadmap.aspx)
18. [The official WebKit SVG status page](http://webkit.org/projects/svg/status.xml)