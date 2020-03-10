> この記事は[WebKit](https://ja.wikipedia.org/wiki/WebKit)から翻訳されています。


**WebKit**（ウェブキット）は、[アップルが中心となって開発されている](../Page/アップル_\(企業\).md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[HTMLレンダリングエンジン](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink")群の総称である。[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[CSS](../Page/Cascading_Style_Sheets.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[SVG](../Page/Scalable_Vector_Graphics.md "wikilink")、[MathMLなどを解釈する](https://ja.wikipedia.org/wiki/Mathematical_Markup_Language "wikilink")。

WebKitは、元々アップルの[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に搭載される[Safari](../Page/Safari.md "wikilink")の[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")として、[Linux](../Page/Linux.md "wikilink")や[BSD](../Page/BSD.md "wikilink")といった、[Unix系](../Page/Unix系.md "wikilink")用の[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")である[KHTML](../Page/KHTML.md "wikilink")を[フォークして開発された](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。現在はその他の多くのプラットフォームに移植されている。

## ライセンス

WebKitのWebCoreおよびJavaScriptCoreライブラリは[GNU Lesser General Public License](../Page/GNU_Lesser_General_Public_License.md "wikilink") (LGPL) 、その他の部分は修正[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")で利用可能である\[1\]。

## 歴史

WebKitは元々、macOSの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink") "Safari" のレンダリングエンジンとして使用するため、LinuxやBSDといったUnix系用のブラウザ "[Konqueror](../Page/Konqueror.md "wikilink")" のKHTMLソフトウェア・ライブラリを基にアップルによって作成され、現在までに、アップル、KDE、ノキア、Google、Torch Mobileなどによって改良が加えられた。

### 起源

LinuxやBSDなどのUnix系用ブラウザとして、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に [KDE](../Page/KDE.md "wikilink")プロジェクト の [HTMLレンダリングエンジン](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink") "[KHTML](../Page/KHTML.md "wikilink")" と KDE の[JavaScriptエンジン](https://ja.wikipedia.org/wiki/JavaScriptエンジン "wikilink") ([KJS](https://ja.wikipedia.org/wiki/KJS "wikilink")) が開発された。その後、アップルが[2002年](../Page/2002年.md "wikilink")にそれらを[フォークしてWebKitを開発した](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。

WebKitは[KHTML](../Page/KHTML.md "wikilink")を基にした[HTMLパーザかつレンダラであるWebCoreと](../Page/HyperText_Markup_Language.md "wikilink")、[KJS](https://ja.wikipedia.org/wiki/KJS "wikilink")を基にした[JavaScript](../Page/JavaScript.md "wikilink")エンジンであるJavaScriptCoreを下位[ライブラリ](../Page/ライブラリ.md "wikilink")として含む。

当初、KHTMLとKJSは、[Mozilla](../Page/Mozilla.md "wikilink")プロジェクトによって同じくオープンソースで開発が進められていた[Gecko](../Page/Gecko.md "wikilink")エンジンの基本方針である高いWeb標準への準拠と競合しないよう、[Internet Explorerとの高い互換を目指し開発が行われていた](../Page/Internet_Explorer.md "wikilink")。

その後、WebKitでは両ライブラリともパフォーマンス向上やWebサイトの表示の改善、Web標準へのさらなる準拠のために、基となった[KDE](../Page/KDE.md "wikilink")の実装からかなりの修正が加えられている。

### 開発・オープンソース化

[Mac OS X v10.3以降に搭載されているmacOS標準のウェブブラウザ](../Page/Mac_OS_X_v10.3.md "wikilink")、Safariの基礎を成している。[プログラマ](../Page/プログラマ.md "wikilink")はわずかな作業でその機能を外部アプリケーションから利用できる。[Objective-C](../Page/Objective-C.md "wikilink")からWebKitの[APIにアクセスすることで](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")との通信、[Webページの取得および表示](../Page/ウェブページ.md "wikilink")、外部[プラグイン](../Page/プラグイン.md "wikilink")の利用などを扱うことができる。

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[6月7日](../Page/6月7日.md "wikilink")、Safariの開発者[Dave Hyattは自身のブログ上でアップルがWebKitを](https://ja.wikipedia.org/wiki/:en:Dave_Hyatt "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")化し（それまではWebCoreとJavaScriptCoreのみがオープンソースであった）、[CVSと](../Page/Concurrent_Versions_System.md "wikilink")[Bugzilla](../Page/Bugzilla.md "wikilink")へのアクセスを公開することを発表した\[2\]。これに関しては[Bertrand SerletがAppleの](https://ja.wikipedia.org/wiki/w:Bertrand_Serlet "wikilink")[WWDC](https://ja.wikipedia.org/wiki/WWDC "wikilink") 2005にて初めて公式発表を行っている。また、[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[1月10日](../Page/1月10日.md "wikilink")にCVSから[Subversionに移行した](../Page/Apache_Subversion.md "wikilink")。

[2007年](../Page/2007年.md "wikilink")初めにはアニメーションなどを含む新たな[CSS](../Page/CSS.md "wikilink")拡張の実装に着手した\[3\]。これらの拡張は標準化のため2009年にW3Cにワーキングドラフトとして提出された\[4\]。

2007年11月には、[HTML5](../Page/HTML5.md "wikilink")のメディア機能のサポートを達成したことが発表された\[5\]。このHTML5に部分対応したWebKitでは、組み込み動画のネイティブ描画とスクリプトコントロールが可能である。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[3月26日](https://ja.wikipedia.org/wiki/3月26日 "wikilink")、WebKit r31356（最初のスコア100はr31342）が、世界で最初に公開された[Acid3](https://ja.wikipedia.org/wiki/Acid3 "wikilink")（[ウェブ標準](../Page/ウェブ標準.md "wikilink")準拠の指標の一つ）に合格したレンダリングエンジンとなった\[6\]。2008年[9月25日](../Page/9月25日.md "wikilink")、スムーズなアニメーションを含め、Acid3を完全にパスしたと発表された\[7\]。

### WebKit2

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[4月8日](https://ja.wikipedia.org/wiki/4月8日 "wikilink")、分離プロセスモデルを採用した**WebKit2**\[8\]の開発が発表された\[9\]。WebKit2の採用例としては、Appleや[Tizen](https://ja.wikipedia.org/wiki/Tizen "wikilink")などがある。WebKit2ではWebKitから大幅にAPIの仕様が変更されており、互換性が失われている。そのため「WebKit2」という新たな名称を採用し、従来のWebKitとは区別できるようにしている。

[2011年](../Page/2011年.md "wikilink")[7月21日](../Page/7月21日.md "wikilink")にアップルがWebKit2エンジンであるSafari5.1を公開した\[10\]。[iOS向けのSafariでは](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、iOS 8よりWebKit2が採用された\[11\]。

### Blinkとの分裂

[2013年](../Page/2013年.md "wikilink")[4月3日](../Page/4月3日.md "wikilink")、アップルとGoogleが開発方針をめぐって対立したことや、WebKitエンジン自体が複雑化したことによる開発の遅滞が問題視されたことにより、GoogleはWebKitを[Blinkにフォークさせる事を発表した](https://ja.wikipedia.org/wiki/Blink_\(レンダリングエンジン\) "wikilink")。同日、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")もWebKitではなく、Blinkを採用することを表明した。翌日の[4月4日](../Page/4月4日.md "wikilink")、Appleは[V8の排除](https://ja.wikipedia.org/wiki/V8_\(JavaScriptエンジン\) "wikilink")、JavaScriptCore以外の使用の排除、[Skia](https://ja.wikipedia.org/wiki/Skia "wikilink")の排除、Googleのビルドシステム[GYPの排除などの計画を表明し](https://ja.wikipedia.org/wiki/GYP_\(ソフトウェア\) "wikilink")\[12\]、WebKitはSafari用のエンジンとなった。

### 移植

当初macOSのために開発されたため、WebKitを使用したウェブブラウザはmacOS専用のものが多かったが、[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink") (同系統のChromiumも同様。ただしそれらは2013年4月以降はWebKitから分岐されたBlinkを使用) など、LinuxやWindows向けウェブブラウザにもWebKitを採用したものが出てきている。アップル自身もWindows版のSafariの開発にも用いている。最近ではWebKitはデスクトップにとどまらず、[モバイルプラットフォーム](https://ja.wikipedia.org/wiki/モバイルプラットフォーム "wikilink")でも活用され始めている。

  - [ノキア](https://ja.wikipedia.org/wiki/ノキア "wikilink")は、自社の[Symbian OS上のインターフェース環境](https://ja.wikipedia.org/wiki/Symbian_OS "wikilink")[S60](https://ja.wikipedia.org/wiki/Series_60 "wikilink") 3rd Editionのブラウザ用に、WebKitをS60に移植した (S60 WebKit)\[13\]。
  - [アドビシステムズ](../Page/アドビシステムズ.md "wikilink")は、[Flash](../Page/Adobe_Flash.md "wikilink")、[Flex](https://ja.wikipedia.org/wiki/Adobe_Flex "wikilink")、HTML、JavaScript、[Ajax](https://ja.wikipedia.org/wiki/Ajax "wikilink")の技術を用いて、高度なインターネットアプリケーションを構築する[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な[ランタイムである](../Page/ランタイムライブラリ.md "wikilink")[AIR](https://ja.wikipedia.org/wiki/Adobe_Integrated_Runtime "wikilink")（コードネームApollo）において、HTMLやJavaScriptを処理するエンジンとしてWebKitを採用している\[14\]。また、Adobe Dreamweaver CS4での採用が発表された\[15\]。
  - [Google](../Page/Google.md "wikilink")は、[Google Chromeや](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")[Android標準ブラウザ(4.3以前)](https://ja.wikipedia.org/wiki/Androidブラウザ "wikilink")、携帯電話プラットフォーム[Android](../Page/Android.md "wikilink")で採用している\[16\]。
  - WebKit/GTK+は、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")向けのポート。様々なWebブラウザやメールクライアント等で利用されている\[17\]。
  - Windows向けの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")である[Lunascape](https://ja.wikipedia.org/wiki/Lunascape "wikilink")は、バージョン5.0αから、WebKitを選択可能なエンジンの一つとして搭載。
  - Iris Browserは、Torch MobileによるWebKitをベースにした、QTとQtopia、Windows Mobile向けブラウザ。1.0.5PreviewよりWindows Mobile 5もサポートされた\[18\]。
  - [Opera Softwareは](https://ja.wikipedia.org/wiki/Opera_Software "wikilink")、自社の独自路線を変更し、Webkitの採用を決めたことを発表していた\[19\]。ただし、前述の通りその後Blinkへ移行している。

## コンポーネント

### WebCore

WebCoreは、WebKitプロジェクトにより開発された、HTMLおよびSVGのレイアウト、レンダリング、[Document Object Model](../Page/Document_Object_Model.md "wikilink") (DOM) [ライブラリ](../Page/ライブラリ.md "wikilink")である。WebCoreの完全な[ソースコード](../Page/ソースコード.md "wikilink")は[LGPLで公開されている](../Page/GNU_Lesser_General_Public_License.md "wikilink")。WebKit[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")はWebCoreおよびJavaScriptCoreをラップし、[C++](../Page/C++.md "wikilink")ベースのWebCoreレンダリングエンジンおよびJavaScriptCoreスクリプトエンジンにObjective-C application programming interface (API) を提供することにより、[Cocoa](../Page/Cocoa.md "wikilink") APIベースのアプリケーションから容易に参照することを可能にしている。より最近のバージョンはクロスプラットフォームのC++プラットフォーム抽象化を含んでおり、また様々なportは追加APIを提供している。

### JavaScriptCore

JavaScriptCoreは、WebKitの実装に[JavaScriptエンジン](https://ja.wikipedia.org/wiki/JavaScriptエンジン "wikilink")を提供するフレームワークであり、またmacOSのその他の場面で使用される同様のスクリプティングを提供する\[20\]\[21\]。JavaScriptCoreはKDE's JavaScript engine ([KJS](https://ja.wikipedia.org/wiki/KJS "wikilink")) ライブラリおよび[Perl Compatible Regular Expressions](https://ja.wikipedia.org/wiki/Perl_Compatible_Regular_Expressions "wikilink") (PCRE) [正規表現](../Page/正規表現.md "wikilink")ライブラリに由来している。KJSおよびPCREからフォークされてから、JavaScriptCoreは多くの新機能について改良がなされ、パフォーマンスも大幅に向上している\[22\]。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[6月2日](https://ja.wikipedia.org/wiki/6月2日 "wikilink")、発表時点で従来より1.6倍の高速化を果たした、新たなJavaScriptCoreとして[バイトコードインタプリタ](https://ja.wikipedia.org/wiki/インタプリタ#バイトコードインタプリタ "wikilink")[VM](../Page/仮想機械.md "wikilink")\[23\]のSquirrelFishが発表された\[24\]。また、[9月18日](../Page/9月18日.md "wikilink")には、SquirrelFishよりおよそ2倍の高速化を果たしたSquirrelFish Extreme (SFX) が発表された\[25\]。

### Drosera

DroseraはWebKitのナイトリービルドに含まれていたJavaScript[デバッガーである](../Page/デバッグ.md "wikilink")\[26\]\[27\]。Droseraの名は[食虫植物](https://ja.wikipedia.org/wiki/食虫植物 "wikilink")（つまりバグを食べる）の[モウセンゴケ属](../Page/モウセンゴケ属.md "wikilink")の学名から付けられた。DroseraはWeb Inspectorに含まれるデバッギング機能によって置き換えられている\[28\]。

### SunSpider

SunSpiderは、現在および近い将来に想定されるJavaScriptの使用（画面描画、暗号化、テキスト操作など）に関連するタスクのJavaScriptパフォーマンスを測定する目的で作られたベンチマークスイートである\[29\] The suite further attempts to be balanced and statistically sound.\[30\]。

SunSpiderはアップルのWebKitチームによって2007年12月にリリースされた\[31\]。SunSpiderは広く受け入れられ\[32\]、他のブラウザーの開発者もブラウザー間のJavaScriptパフォーマンスを比較するため使用している\[33\]。

## WebKitを使用するソフトウェア

### ウェブブラウザ

  - クロスプラットフォーム
      - [Arora](https://ja.wikipedia.org/wiki/Arora "wikilink") (Qt Webkit Integration)
      - [Midori](https://ja.wikipedia.org/wiki/Midori_\(ウェブブラウザ\) "wikilink")（Webkit/GTK+、[Xfce](../Page/Xfce.md "wikilink")プロジェクトの一部）
      - [QtWeb](https://ja.wikipedia.org/wiki/QtWeb "wikilink")
      - [NetFront Browser NX](https://ja.wikipedia.org/wiki/NetFront_Browser_NX "wikilink") \[34\]
  - macOS向け
      - [OmniWeb](https://ja.wikipedia.org/wiki/OmniWeb "wikilink")
      - [Sunrise](https://ja.wikipedia.org/wiki/Sunrise_\(ウェブブラウザ\) "wikilink")
      - [Stainless](https://ja.wikipedia.org/wiki/Stainless "wikilink")
      - [iCab](https://ja.wikipedia.org/wiki/iCab "wikilink")
      - [Shiira](../Page/シイラ_\(ウェブブラウザ\).md "wikilink")
  - Windows向け
      - [Lunascape](https://ja.wikipedia.org/wiki/Lunascape "wikilink")（5.0α以降・[Trident](../Page/Trident.md "wikilink")及びGeckoも使用可能）
      - [Sleipnir](../Page/Sleipnir.md "wikilink")（3.5.0.4000以降4.1.4.4000まで、4.3.0.4000以降は[Blink採用](https://ja.wikipedia.org/wiki/Blink_\(レンダリングエンジン\) "wikilink")）
  - Unix系OS向け
      - [rekonq](https://ja.wikipedia.org/wiki/rekonq "wikilink")
      - [Web](https://ja.wikipedia.org/wiki/Web_\(ウェブブラウザ\) "wikilink")（2.28以降）
  - [Haiku](../Page/Haiku_\(オペレーティングシステム\).md "wikilink") 向け
      - [WebPositive](https://ja.wikipedia.org/wiki/WebPositive "wikilink")
  - モバイル向け
      - [BlackBerry Browser](../Page/BlackBerry.md "wikilink")（6.0以降）
      - [Iris Browser](https://ja.wikipedia.org/wiki/Iris_Browser "wikilink") (for Windows Mobile 5/6)
      - [NetFront Life Browser](https://ja.wikipedia.org/wiki/NetFront_Life_Browser "wikilink")\[35\]
  - ゲーム機向け
      - [ニンテンドー3DS インターネットブラウザー](https://ja.wikipedia.org/wiki/ニンテンドー3DS "wikilink")（システムバージョン2.0.0-2J以降）
          - [NetFront Browser NX](https://ja.wikipedia.org/wiki/NetFront_Browser_NX "wikilink") が搭載されている\[36\]\[37\]。ただし、任天堂の仕様では[NetFront Browserになっている](../Page/NetFront_Browser.md "wikilink")\[38\]。
      - [Wii U インターネットブラウザー](https://ja.wikipedia.org/wiki/Wii_U "wikilink")（システムバージョン2.1.0J以降）
          - [NetFront Browser NX](https://ja.wikipedia.org/wiki/NetFront_Browser_NX "wikilink") が搭載されている\[39\]\[40\]
      - [PlayStation Vita Browser](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink")
      - [PlayStation 3 Internet browser](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")(システムソフトウェア4.10以降)
      - [PlayStation 4 インターネットブラウザー](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")

#### Chromiumベース

  - Windows、macOSおよびLinux向け
      - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")
      - [SRWare Iron](https://ja.wikipedia.org/wiki/SRWare_Iron "wikilink")
      - [CoolNovo](https://ja.wikipedia.org/wiki/CoolNovo "wikilink")
  - Windows向け
      - [AnciaChrome](https://ja.wikipedia.org/wiki/AnciaChrome "wikilink")

#### WebKit2

  - macOSおよびiOS向け
      - [Safari](../Page/Safari.md "wikilink")

#### 開発終了

  - [Flock](../Page/Flock.md "wikilink")（3.0以降）
  - [Swift](https://ja.wikipedia.org/wiki/Swift_\(ウェブブラウザ\) "wikilink") (for Windows)
  - [RockMelt](https://ja.wikipedia.org/wiki/RockMelt "wikilink")（WindowsおよびmacOS）

### その他のソフトウェア

  - macOSおよびWindows向け
      - [iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")
      - [AIR](https://ja.wikipedia.org/wiki/Adobe_Integrated_Runtime "wikilink")
      - [Dreamweaver CS4, CS5](https://ja.wikipedia.org/wiki/Adobe_Dreamweaver "wikilink") - Webオーサリングソフト
      - [Steam](../Page/Steam.md "wikilink") - ゲーミングプラットフォーム
  - macOS向け
      - [メール](../Page/メール_\(アップル\).md "wikilink") - macOS付属のソフトウェア
      - [Dashboard](../Page/Dashboard.md "wikilink") - macOS付属のソフトウェア環境
  - モバイル向け
      - [Android](../Page/Android.md "wikilink") - Googleの提唱する携帯電話用プラットフォーム
      - [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") - 内包され、SafariやMail等で利用されている
      - [HP webOS](https://ja.wikipedia.org/wiki/HP_webOS "wikilink") - HPの[Access Linux Platform](../Page/Access_Linux_Platform.md "wikilink") (ALP) をベースとした携帯電話用プラットフォーム
  - [Google Chrome OS](https://ja.wikipedia.org/wiki/Google_Chrome_OS "wikilink")

## バージョンの対応関係

Google Chrome は 28以降 [Blink](https://ja.wikipedia.org/wiki/Blink_\(レンダリングエンジン\) "wikilink") に移行したが、下記表は Blink を含まず、WebKit の対応表。

<table>
<thead>
<tr class="header">
<th><p>WebKit</p></th>
<th><p><a href="../Page/Safari.md" title="wikilink">Safari</a></p></th>
<th><p>Mobile Safari</p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Google_Chrome" title="wikilink">Google Chrome</a></p></th>
<th><p><a href="https://ja.wikipedia.org/wiki/Androidブラウザ" title="wikilink">Android<br />
Browser</a></p></th>
<th><p>Chrome for<br />
Android</p></th>
<th><p>3DS</p></th>
<th><p>New 3DS</p></th>
<th><p>Wii U</p></th>
<th><p>PS3</p></th>
<th><p>PS4</p></th>
<th><p>Vita</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>525</p></td>
<td><p>3.1, 3.2</p></td>
<td><p>3.1</p></td>
<td><p>0.4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>528</p></td>
<td></td>
<td><p>4.0</p></td>
<td><p>1</p></td>
<td><p>1.5, 1.6</p></td>
<td></td>
<td></td>
<td></td>
<td><p>　</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>530</p></td>
<td><p>4.0 - 4.0.2</p></td>
<td></td>
<td><p>2</p></td>
<td><p>2.0, 2.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>531</p></td>
<td><p>4.0.3 - 4.0.5</p></td>
<td><p>4.0.4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>4.10 -</p></td>
<td></td>
<td><p>1.00 - 1.81</p></td>
</tr>
<tr class="odd">
<td><p>532</p></td>
<td></td>
<td><p>4.0.5</p></td>
<td><p>3, 4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>533</p></td>
<td><p>4.1, 5.0</p></td>
<td><p>5.0.2</p></td>
<td><p>5</p></td>
<td><p>2.2, 2.3</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>534</p></td>
<td><p>5.1</p></td>
<td><p>5.1</p></td>
<td><p>6 - 12</p></td>
<td><p>3.0 - 4.2</p></td>
<td></td>
<td><p>2.0.0-2J - 9.5.0-22J</p></td>
<td></td>
<td><p>2.1.0J - 3.1.0J</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>535</p></td>
<td></td>
<td></td>
<td><p>13 - 18</p></td>
<td></td>
<td><p>16 - 18</p></td>
<td><p>9.5.0-23J -</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>536</p></td>
<td><p>6.0</p></td>
<td><p>6.0</p></td>
<td><p>19, 20</p></td>
<td></td>
<td></td>
<td></td>
<td><p>8.1.0-0J -</p></td>
<td><p>4.0.0J -</p></td>
<td></td>
<td><p>1.00 - 1.76</p></td>
<td><p>2.00 - 3.20</p></td>
</tr>
<tr class="even">
<td><p>537</p></td>
<td><p>7.0</p></td>
<td><p>7.0</p></td>
<td><p>21 - 27</p></td>
<td><p>4.3</p></td>
<td><p>25 - 27</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><p>2.00 -</p></td>
<td><p>3.30 -</p></td>
</tr>
</tbody>
</table>

## 脚注

### 出典

## 関連項目

  - [Android](../Page/Android.md "wikilink")
  - [iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")
  - [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")
  - [iPod touch](https://ja.wikipedia.org/wiki/iPod_touch "wikilink")
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - [ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")
  - [HTMLレンダリングエンジン](https://ja.wikipedia.org/wiki/HTMLレンダリングエンジン "wikilink")

## 外部リンク

  - [webkit.org: WebKit Open Source Project](http://webkit.org/)
  - [developer.apple.com: Open Source - Internet & Web - WebKit](http://developer.apple.com/opensource/internet/webkit.html)

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink")

1.
2.  <http://weblogs.mozillazine.org/hyatt/archives/2005_06.html#008281>
3.  [*CSS Transforms*](http://webkit.org/blog/130/css-transforms/)
4.  [*CSS3 Animations*](http://dev.w3.org/csswg/css3-animations/)
5.  [*HTML5 Media Support*](http://webkit.org/blog/140/html5-media-support/) by Antti Koivisto, *Surfin' Safari* blog, November 12th, 2007
6.  [WebKit achieves Acid3 100/100 in public build](http://webkit.org/blog/173/webkit-achieves-acid3-100100-in-public-build/)
7.  [Full Pass of Acid3](http://webkit.org/blog/280/full-pass-of-acid-3/)
8.  [WebKit2](http://trac.webkit.org/wiki/WebKit2)
9.  [\[webkit-dev](https://lists.webkit.org/pipermail/webkit-dev/2010-April/012235.html) Announcing WebKit2\]
10.
11.
12. [webkit-dev Cleaning House](https://lists.webkit.org/pipermail/webkit-dev/2013-April/024388.html)
13.
14. [Adobe Integrated Runtime (AIR)](http://www.adobe.com/jp/aboutadobe/pressroom/pressreleases/200706/20070612apollo.html)
15. [Adobe Dreamweaver CS3 10 周年記念イベント レポート](http://www.tcp-net.ad.jp/danbo/DreamweaverCS3_10/index.html)
16. [What is Android?](http://code.google.com/android/what-is-android.html)
17. [WebKitGtk - GNOME Live\!](http://live.gnome.org/WebKitGtk)
18. [Torch Mobile](http://www.torchmobile.com/)
19.
20. [The WebKit Open Source Project – JavaScript](http://webkit.org/projects/javascript/index.html)
21. KDE-Darwin mailing list, "[JavaScriptCore, Apple’s JavaScript framework based on KJS](http://web.archive.org/web/20070310215550/www.opendarwin.org/pipermail/kde-darwin/2002-June/000034.html)", 13 June 2002.
22.
23. [SquirrelFish – WebKit – Trac](http://trac.webkit.org/wiki/SquirrelFish)
24. [Surfin’ Safari - Blog Archive » Announcing SquirrelFish](http://webkit.org/blog/189/announcing-squirrelfish/)
25. [Introducing SquirrelFish Extreme](http://trac.webkit.org/wiki/Introducing%20SquirrelFish%20Extreme.ja)
26. WebKit.org [Drosera](http://trac.webkit.org/projects/webkit/wiki/Drosera) wiki article
27.
28.
29.
30.
31.
32.
33.
34. [HTML5対応のWebKit版ブラウザ | 株式会社ACCESS](http://jp.access-company.com/products/browser/nx/)
35.
36. [ニンテンドー3DS用インターネットブラウザーLGPL適用オープンソースについて](http://www.nintendo.co.jp/3ds/hardware/features/sourcecode.html) アーカイブの中に**WebKit**のソースコードが入っている
37. [ACCESS、情報家電向けブラウザの新製品「NetFront® Browser NX」を発表](http://jp.access-company.com/news_event/archives/2011/110607/)
38. [インターネットブラウザーの主な仕様](http://www.nintendo.co.jp/3ds/hardware/features/browser.html)
39. [Wii U インターネットブラウザーの主な仕様](http://www.nintendo.co.jp/wiiu/hardware/features/internetbrowser/browser/)
40. [任天堂の新ゲーム機「Wii U」に ACCESSの「NetFront® Browser NX」をブラウザエンジンとして提供 | 株式会社ACCESS](http://jp.access-company.com/news_event/archives/2012/121210/)