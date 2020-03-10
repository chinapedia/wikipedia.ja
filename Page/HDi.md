> この記事は[HDi](https://ja.wikipedia.org/wiki/HDi)から翻訳されています。


**HDi** とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")による [HD DVD](../Page/HD_DVD.md "wikilink") の Advacend Content 層の実装である\[1\]\[2\]。かつては **iHD** と称していた\[3\]\[4\]。[Xbox 360](../Page/Xbox_360.md "wikilink") の HD DVD オプションや HD DVD プレイヤーで使われている\[5\]。

## Advanced Content

Advanced Content は[DVDフォーラム](../Page/DVDフォーラム.md "wikilink")が、メニュー、ブックマーク、ピクチャ・イン・ピクチャ、追加コンテンツやゲームなどの [HD DVD](../Page/HD_DVD.md "wikilink") のインタラクティブ機能のために定義した仕様である。Advanced Content の実装では、タイマ、ユーザー入力（リモコンなど）などの機能が提供される。また、ネットワークにアクセスして追加コンテンツをダウンロードしたり、2次記憶装置上のブックマークなどの情報にアクセスしたりできる。Advanced Content は[HTMLに似た](../Page/HyperText_Markup_Language.md "wikilink")[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")を使って書かれ、アプリケーションのロジックは[ECMAScript](../Page/ECMAScript.md "wikilink")を使って書かれる。Advanced Content が提供する機能は ECMAScript の[APIから利用できる](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。表示スタイルの設定には [XSL-FO](https://ja.wikipedia.org/wiki/XSL_Formatting_Objects "wikilink") をベースとしたXMLマークアップが使われ、タイマの設定には[SMILが使われる](../Page/Synchronized_Multimedia_Integration_Language.md "wikilink")。Advanced Content のアプリケーション作成時には [XPath](https://ja.wikipedia.org/wiki/XML_Path_Language "wikilink") を使うこともできる。

## 概要

HDi は Advanced Content 仕様の実装であり、HDi 向けのアプリケーションはXML派生言語とECMAScriptを使って書かれる。ECMAScript は Microsoft Windows プラットフォーム上で動作する [JScript](https://ja.wikipedia.org/wiki/JScript "wikilink") エンジンで処理される。HDi 実行部は Advanced Content 規格に定義された[APIを提供する](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。シングルスレッドのプログラミングモデルのみに対応しているが、ネットワークアクセスや二次記憶装置アクセスなどの操作は非同期に実行される\[6\]。

[HD DVD](../Page/HD_DVD.md "wikilink") ビデオのインタラクティブ機能は Advanced Content のアプリケーションであり、HDi 実行部により実行され描画される。アプリケーションは、プレイリストファイル (`.xpl`) とサブタイトルファイル (`.xas`) とマークアップファイル (`.xmu`) とスクリプト (`.js`)、さらにビデオ本体から構成され、ディレクトリ構造も定義されている。HDi 実行部はマークアップとスクリプトを解析して実行する。ビデオの再生はナビゲーションシステムの一部として統合されており、スクリプトコードで制御され起動される。

HDi実行部は、ビデオ再生とナビゲーション用アプリケーションの実行と描画を行う。マークアップは構文解析されて [Document Object Model](../Page/Document_Object_Model.md "wikilink") (DOM) に変換され、それによって ECMAScript コードでUIレイアウトを実行時に制御・修正できるようになる。アニメーションとインタラクティブ性は、UIウィジェットのレイアウトを動的に変更することでなされる。DOMと関連APIによって、再生の一時停止、ナビゲーションUIの置換、映画の特定エリアのシーク（手動シークまたはブックマークのシーク）が可能となる。描画面は6層になっている。画面に最終的に現れる画像は、それらの合成されたものである。この合成もHDi実行部が制御する。それぞれの層は背景から前景の順に次のようになっている。

1.  Background plane: アプリケーションの背景色を決定する。
2.  Main video plane: ビデオ本体はこの面で表示される。
3.  Sub video plane: ピクチャ・イン・ピクチャなど2次的ビデオが表示される。
4.  Subtitles graphics plane: サブタイトル（字幕）が表示される。
5.  Application graphics plane: スクリプトとマークアップによるUIはこの面に描画される。
6.  Cursor plane: カーソルを表示する場合に使われる。

マイクロソフトは HDi アプリケーション開発用ツールは提供していないが、サードパーティからそのようなツールが発売されていた。Advanced Content（と HDi）が使っているコンポーネント（[XML](../Page/Extensible_Markup_Language.md "wikilink")、[XSL-FO](https://ja.wikipedia.org/wiki/XSL_Formatting_Objects "wikilink")、[XPath](https://ja.wikipedia.org/wiki/XML_Path_Language "wikilink")、[ECMAScript](../Page/ECMAScript.md "wikilink")）は広く使われているものばかりなので、HDi専用ツールでなくとも流用可能である。しかし、マイクロソフトはHDiシミュレータ（[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") 上で HDi アプリケーションを実行し[デバッグ](../Page/デバッグ.md "wikilink")できる環境）を無料でダウンロード可能にしていた。ただし、これは完全な開発ツールではないし、再生デバイスでもない。

HDi は光ディスクだけでなく、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上のマルチメディアコンテンツなどにも応用できる。実際、2007年10月4日、東芝とマイクロソフトは「光媒体にとどまらないインタラクティブな体験の新たなプラットフォームへの展開を推進するため」 Advanced Interactivity Consortium (AIC) の結成を発表した\[7\]。

## 脚注

## 参考文献

  -
## 外部リンク

  - [HDi trademark press release](http://www.microsoft.com/presspass/press/2007/Sep07/09-20HDiTrademarkPR.mspx)
  - [MSDN HD DVD Authoring Forum](http://forums.microsoft.com/MSDN/ShowForum.aspx?ForumID=527&SiteID=1)
  - [MSFT Peter Torr's HDi Blog](http://blogs.msdn.com/ptorr/)
  - [MSFT Amy Dullard's Application Development for HD DVD Blog](http://blogs.msdn.com/amyd/)
  - [Xbox 360 HD-DVD Developer Interview](http://console.hardocp.com/article.html?art=MTI3MCwxLCxoY29uc29sZQ==)
  - [HP Pressures Blu-Ray Camp](http://www.duplicatorguide.com/index.php?option=com_content&task=view&id=270&Itemid=2)
  - [Microsoft's Amir Majidimehr describes the genesis of HDi (and other things)](http://hddvd.highdefdigest.com/feature_microsofthddvdinterview.html)
  - [Interview: Microsoft’s Kevin Collins on HD DVD](http://www.hometheaterblog.com/hometheater/2006/09/interview_hddvd_1.html)

[Category:マイクロソフト](https://ja.wikipedia.org/wiki/Category:マイクロソフト "wikilink") [Category:DVD](https://ja.wikipedia.org/wiki/Category:DVD "wikilink")

1.
2.
3.  [Engadget:iHD, HDi? Nope it's called Advanced Navigation](http://www.engadgethd.com/2007/01/25/ihd-hdi-nope-its-called-advanced-navigation/)
4.  [iHD changed to HDi](http://www.hdtvinfo.eu/news/hd-video-formats/ihd-changed-to-hdi.html)
5.
6.
7.