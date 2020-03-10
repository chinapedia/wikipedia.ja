> この記事は[XULRunner](https://ja.wikipedia.org/wiki/XULRunner)から翻訳されています。


**XULRunner**（ズールランナー）は、[XUL](https://ja.wikipedia.org/wiki/XUL "wikilink")+[XPCOM](https://ja.wikipedia.org/wiki/XPCOM "wikilink")アプリケーションの組み込み、起動を可能にするランタイムパッケージである。XULRunnerはそのバージョン番号と同じ[Firefoxと同じコードベースを使用している](../Page/Mozilla_Firefox.md "wikilink")。XULRunnerは、GRE (Gecko Runtime Environment) の後継技術であり、[Gecko](../Page/Gecko.md "wikilink")レンダリングエンジンの組み込み技術として利用が可能である。このことから、XULRunner を「新GRE」と呼ぶこともある。配布パッケージを利用することで、[C++](../Page/C++.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink") ([XPConnect](https://ja.wikipedia.org/wiki/XPConnect "wikilink"))、[Perl](../Page/Perl.md "wikilink") ([PlXPCOM](https://ja.wikipedia.org/wiki/PlXPCOM "wikilink"))、[Python](../Page/Python.md "wikilink") ([PyXPCOM](https://ja.wikipedia.org/wiki/PyXPCOM "wikilink"))、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") ([JavaXPCOM](https://ja.wikipedia.org/wiki/JavaXPCOM "wikilink"))、[Ruby](../Page/Ruby.md "wikilink") ([RbXPCOM](https://ja.wikipedia.org/wiki/RbXPCOM "wikilink")) などから、提供コンポーネントを呼び出すことが可能である。現在、XULRunnerには 1,000 以上のXPCOMコンポーネントが含まれている。バイナリパッケージは、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") の各[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")用のものが提供されている。また、Firefox 3以降にはプライベートなXULRunnerパッケージが同梱されているため、XULRunnerアプリケーションをFirefoxの環境上で実行することも可能である。

2015年7月にMozillaはXULRunnerの開発を終了することを発表した\[1\]。

## ソフトウェアの構成

XULRunnerは、主に以下の機能を提供している。機能の詳細は、**[What XULRunner Provides](http://developer.mozilla.org/ja/XULRunner/What_XULRunner_Provides)**を参照されたい。

  - Geckoレンダリングエンジン
  - XULアプリケーション実行環境
  - 各言語向け組み込み（埋め込み）API (Java, GTK (Linux), ActiveX (Windows), Cocoa (macOS) )

## システム要件

XULRunnerが要求するシステム要件は、Firefoxと同等である。Firefoxの**[システム要件](http://www.mozilla-japan.org/products/firefox/system-requirements.html)**を参照されたい。

## ライセンス

XULRunnerには、[Mozilla Public License](../Page/Mozilla_Public_License.md "wikilink") (MPL) バージョン2.0が適用されている。

## XULRunnerで動作するアプリケーション

  - [ChatZilla](../Page/ChatZilla.md "wikilink")（[IRCクライアント](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")）
  - [Google Adwords Editor](http://www.google.com/intl/ja/adwordseditor/) ([Google](../Page/Google.md "wikilink"))
  - [SongBird](http://getsongbird.com/) (音楽プレイヤー)
  - [風博士](https://ja.wikipedia.org/wiki/風博士_\(ウェブブラウザ\) "wikilink") (ウェブブラウザ)

## 脚注

## 関連項目

  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")
  - [Mozilla Public License](../Page/Mozilla_Public_License.md "wikilink")
  - [Gecko](../Page/Gecko.md "wikilink")
  - [XUL](https://ja.wikipedia.org/wiki/XUL "wikilink")
  - [XPCOM](https://ja.wikipedia.org/wiki/XPCOM "wikilink")

## 外部リンク

  - [MDC XULRunnerトップページ](http://developer.mozilla.org/ja/XULRunner) (日本語); [XULRunner page on Mozilla Developer Center](http://developer.mozilla.org/en/XULRunner)
  - [What XULRunner Provides](http://developer.mozilla.org/ja/XULRunner/What_XULRunner_Provides)
  - [XULRunner source code](http://ftp.mozilla.org/pub/mozilla.org/xulrunner/)
  - [XULRunner Roadmap](http://wiki.mozilla.org/XULRunner:Roadmap)  (内容は過去のものになっている)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink") [Category:ウィジェット・ツールキット](https://ja.wikipedia.org/wiki/Category:ウィジェット・ツールキット "wikilink")

1.  [XULRunner future and ownership: Announcement to XULRunner dev group](https://groups.google.com/forum/?_escaped_fragment_=msg/mozilla.dev.platform/_rFMunG2Bgw/C-4PcHj9IgAJ#!msg/mozilla.dev.platform/_rFMunG2Bgw/C-4PcHj9IgAJ)