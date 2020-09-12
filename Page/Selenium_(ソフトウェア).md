> この記事は[Selenium \(ソフトウェア\)](https://ja.wikipedia.org/wiki/Selenium_\(ソフトウェア\))から翻訳されています。



 **Selenium** は、 [Webアプリケーションを](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")[テストするためのポータブル](../Page/ソフトウェアテスト.md "wikilink")[フレームワークである](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")。 Selenium は、テスト[スクリプト言語](../Page/スクリプト言語.md "wikilink")(Selenium IDE)を学ぶ必要なしに、機能テストを作成するための再生ツールを提供する。また、[C＃](../Page/C_Sharp.md "wikilink")、[Groovy](../Page/Groovy.md "wikilink")、[Java](../Page/Javaプラットフォーム.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Scala](../Page/Scala.md "wikilink") 等の一般的な[プログラミング言語](../Page/プログラミング言語.md "wikilink")でテストを作成するためのテスト[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")(Selenese)も提供する。その後、テストはほとんどの最新の[Webブラウザに対して実行できる](../Page/ウェブブラウザ.md "wikilink")。Selenium は、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")、および[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で動作する。これは、[Apache License 2.0](../Page/Apache_License.md "wikilink") の下でリリースされた[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")である。

## 歴史

Selenium は、2004年にJason Huggins によってThoughtWorks の内部ツールとして開発された。 Huggins は後に、ThoughtWorks の他の[プログラマ](../Page/プログラマ.md "wikilink")や[テスタが参加し](https://ja.wikipedia.org/wiki/テスター "wikilink")、Paul Hammant がチームに加わり、後に「Selenium Remote Control」(RC)となる2番目の操作モードの開発を進めた。ツールはその年[オープンソース](../Page/オープンソース.md "wikilink")化された。

2005年、Dan Fabulich とNelson Sproul は、(Pat Lightbodyの助力を得て)Selenium-RC を最も有名なものに変える一連のパッチを受け入れることを申し出た。同じ会議で、プロジェクトとしてのSelenium の運営は委員会として継続され、Huggins とHammant がThoughtWorks の代表となった。

2007年、Huggins は[Google](../Page/Google.md "wikilink") に加わった。Jennifer Bevan のような他の人と共に、彼はSelenium RC の開発と安定化を続けた。同時に、ThoughtWorks のSimon Stewart は、**WebDriver** と呼ばれる優れたブラウザ自動化ツールを開発した。2009年、Google Test Automation Conference での開発者間の会議の後、2つのプロジェクトをマージし、新しいプロジェクトをSelenium WebDriver またはSelenium 2.0 と呼ぶことが決定した\[1\]。

2008年、Philippe Hanrigou(当時はThoughtWorks)は「Selenium Grid」を作成した。これは、複数のローカルまたはリモートシステムで複数のSelenium テストを同時に実行できるハブを提供し、テストの実行時間を最小限に抑える。 グリッドは、[オープンソース](../Page/オープンソース.md "wikilink")として、Selenium RC の内部/プライベートGoogle クラウドと同様の機能を提供した。Pat Lightbody はすでに「HostedQA」のプライベートクラウドを作成しており、これをGomez、Inc. に販売した。

Selenium の名前は、メールでHuggins が作ったジョークに由来し、[マーキュリー](../Page/マーキュリー.md "wikilink")という競合他社をあざけって、Selenium のサプリメントを摂取することで水銀中毒を治すことができると述べている。メールを受け取った他の人は名前を取り、それを採用した\[2\]。

## [コンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")

Selenium はいくつかの[コンポーネントで構成され](../Page/ソフトウェアコンポーネント.md "wikilink")、それぞれが[Web アプリケーションの](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")[テスト自動化](https://ja.wikipedia.org/wiki/テスト自動化 "wikilink")の開発を支援する特定の役割を果たす\[3\]。

### Selenium IDE

Selenium IDE は、Selenium テスト用の完全な[統合開発環境](../Page/統合開発環境.md "wikilink")(IDE)である。これは、 Firefoxアドオンおよび[Chrome 拡張機能として実装される](../Page/Chromeウェブストア.md "wikilink")。機能テストの記録、編集、デバッグが可能である。 以前はSelenium Recorder として知られていた。Selenium IDE は、もともと笠谷真也によって作成され、2006年にSelenium プロジェクトに寄付された。Selenium IDE は以前はほとんどメンテナンスされていなかった\[4\]。Selenium IDE は2018年に積極的にメンテナンスされ始めた\[5\]\[6\]\[7\]\[8\]。

スクリプトは自動的に記録され、手動で編集されて、[自動補完](https://ja.wikipedia.org/wiki/自動補完 "wikilink")サポートとコマンドをすばやく移動する機能を提供する。スクリプトは、Selenium 用の特別なテストスクリプト言語である*Selenese* で記録される。Selenese には、[ブラウザでアクションを実行](../Page/ウェブブラウザ.md "wikilink")(リンクをクリックしてオプションを選択)するコマンド、および結果のページからデータを取得するコマンドが用意されている。

[Firefox](../Page/Mozilla_Firefox.md "wikilink") 用のSelenium IDE の2.xバージョンは、Firefox 55 のアップグレード後に機能しなくなり\[9\]、Selenium IDE 3.x に置き換えられた\[10\]。

公式のSelenium IDE プロジェクトに加えて、2つの代替Selenium IDE [ブラウザ拡張機能が積極的に維持されている](../Page/ウェブブラウザ.md "wikilink")\[11\]: Kantu([オープンソース](../Page/オープンソース.md "wikilink")[GPLライセンス](../Page/GNU_General_Public_License.md "wikilink"))とKatalon Recorder([クローズドソース](../Page/プロプライエタリ・ソフトウェア.md "wikilink")）。

### Selenium クライアントAPI

Selenese でテストを作成する代わりに、テストをさまざまな[プログラミング言語](../Page/プログラミング言語.md "wikilink")で作成することもできる。これらのテストは、Selenium クライアントAPIのメソッドを呼び出すことによってSelenium と通信する。Selenium は現在、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C＃](../Page/C_Sharp.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[R](../Page/R言語.md "wikilink")、[Python](../Page/Python.md "wikilink") 用のクライアントAPIを提供している。

Selenium 2では、*WebDriver* を中心コンポーネントとして使用する新しいクライアントAPIが導入された。ただし、古いクラス(*Selenium* クラスを使用)は引き続きサポートされる。

### Selenium WebDriver

Selenium WebDriver は、Selenium RC の後継である。Selenium WebDriver は(Selenese で、またはクライアントAPIを介して送信される)コマンドを受け入れ、それらを[ブラウザに送信する](../Page/ウェブブラウザ.md "wikilink")。これは、[ブラウザにコマンドを送信して結果を取得する](../Page/ウェブブラウザ.md "wikilink")[ブラウザ固有のブラウザ](../Page/ウェブブラウザ.md "wikilink")・ドライバを介して実装される。ほとんどのブラウザ・ドライバは、実際に[ブラウザアプリケーション](../Page/ウェブブラウザ.md "wikilink")([Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、[Internet Explorer](../Page/Internet_Explorer.md "wikilink")、[Safari](../Page/Safari.md "wikilink")、[Microsoft Edge](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink") 等)を起動してアクセスする。ヘッドレスブラウザーHtmlUnitを使用してブラウザーをシミュレートするHtmlUnit ブラウザ・ドライバもある。

テストを実行するためにSelenium サーバが必要であったSelenium 1とは異なり、Selenium WebDriver はテストを実行するために特別なサーバを必要としない。代わりに、WebDriver は直接[ブラウザインスタンスを起動して制御する](../Page/ウェブブラウザ.md "wikilink")。ただし、Selenium Grid をWebDriver と共に使用して、リモートシステムでテストを実行できる(以下参照)。可能な場合、WebDriver は[ブラウザベースの](../Page/ウェブブラウザ.md "wikilink")[JavaScript](../Page/JavaScript.md "wikilink") コマンドではなく、ネイティブの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")レベルの機能を使用して[ブラウザを駆動する](../Page/ウェブブラウザ.md "wikilink")。これにより、セキュリティ制限等、ネイティブコマンドと[JavaScript](../Page/JavaScript.md "wikilink") コマンドの微妙な違いに関する問題が回避される\[12\]。

実際には、これはSelenium 2.0 API の呼び出しがSelenium 1.0 API の呼び出しよりも大幅に少ないことを意味する。Selenium 1.0は、さまざまな[ブラウザ操作に豊富なインターフェースを提供しようとしたが](../Page/ウェブブラウザ.md "wikilink")、Selenium 2.0は、開発者が独自の[ドメイン固有言語](../Page/ドメイン固有言語.md "wikilink")を作成できる基本的なビルディングブロックのセットを提供することを目的としている。そのような[DSL](../Page/ドメイン固有言語.md "wikilink") の1つは既に存在する。[Ruby](../Page/Ruby.md "wikilink") 言語のWatir プロジェクトには、優れた設計の豊富な歴史がある。 Watir-webdriver は、[Ruby](../Page/Ruby.md "wikilink") のSelenium-Webdriver のラッパーとしてWatir API を実装している。 Watir-Webdriverは、WebDriver 仕様と[HTML](../Page/HyperText_Markup_Language.md "wikilink") 仕様に基づいて、完全に自動的に作成される。

2012年の初めに、当時[Google](../Page/Google.md "wikilink") に、現在は[Facebook](../Page/Facebook.md "wikilink") にいたSimon Stewart(WebDriver の発明者)と[Mozilla](../Page/Mozilla.md "wikilink") のDavid Burns は、WebDriver をインターネット標準にするために[W3Cと交渉している](../Page/World_Wide_Web_Consortium.md "wikilink")。2012年7月にワーキングドラフトがリリースされ、2018年6月に勧告が行われた\[13\]。Selenium-Webdriver(Selenium 2.0)は、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、および[C＃で完全に実装およびサポートされている](../Page/C_Sharp.md "wikilink")。

### Selenium リモートコントロール

Selenium Remote Control(RC)は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") で記述されたサーバであり、[HTTP経由で](../Page/Hypertext_Transfer_Protocol.md "wikilink")[ブラウザのコマンドを受け入れる](../Page/ウェブブラウザ.md "wikilink")。 RCを使用すると、任意の[プログラミング言語](../Page/プログラミング言語.md "wikilink")で[Web アプリケーションの自動テストを作成できる](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")。これにより、Selenium を既存の単体テストフレームワークに適切に統合できる。テストの記述を簡単にするために、Selenium プロジェクトは現在、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[Perl](../Page/Perl.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink") 等のクライアント・ドライバを提供している。 [Java](https://ja.wikipedia.org/wiki/Java "wikilink") ドライバは[Rhino](../Page/Rhino.md "wikilink") エンジン経由で[JavaScript](../Page/JavaScript.md "wikilink") でも使用できる。[HTML](../Page/HyperText_Markup_Language.md "wikilink") テストケースを起動するには、Selenium RC サーバのインスタンスが必要である。つまり、並列実行ごとにポートが異なる必要がある。ただし、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")/[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink") テストケースでは、1つのSelenium RC インスタンスのみを継続的に実行する必要がある\[14\]。

Selenium Remote Controlは、Paul Hammant によって設計されたDriven Selenium またはSelenium B のリファクタリングであり、Selenium の共同作成者としてJason 氏と称された。 元のバージョンは、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[.NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[Python](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") または[Ruby](../Page/Ruby.md "wikilink") のテスト言語から、問題の[ブラウザのプロセスを直接起動した](../Page/ウェブブラウザ.md "wikilink")。[Wire protocol](https://ja.wikipedia.org/wiki/Wire_protocol "wikilink")(当時は「Selenese」と呼ばれていた)は、各言語ポートで再実装された。 Dan Fabulich とNelson Sproul による[リファクタリングの後](../Page/リファクタリング_\(プログラミング\).md "wikilink")(Pat Lightbody の助力を得て)、ドライビング・テスト・スクリプトと[ブラウザの間に中間](../Page/ウェブブラウザ.md "wikilink")[デーモンプロセスがあった](../Page/デーモン_\(ソフトウェア\).md "wikilink")。利点には、リモート[ブラウザを駆動する機能と](../Page/ウェブブラウザ.md "wikilink")、コードのすべての行をますます成長する言語のセットに移植する必要性の減少が含まれる。*Selenium Remote Control* は、2006年にDriven Selenium コードラインから完全に引き継がれた。'Driven' / 'B' および 'RC' の[ブラウザパターンは応答](../Page/ウェブブラウザ.md "wikilink")/要求だったが、後に[Comet](../Page/Comet.md "wikilink")と呼ばれるようになった。

Selenium 2 のリリースに伴い、Selenium RC はSelenium WebDriver を支持して正式に非推奨になった。

### Selenium Grid

Selenium Grid は、リモートマシンで実行されている[Web ブラウザインスタンスをテストで使用できるようにするサーバである](../Page/ウェブブラウザ.md "wikilink")。Selenium Grid では、1つのサーバがハブとして機能する。 テストはハブに接続して、[ブラウザインスタンスへのアクセスを取得する](../Page/ウェブブラウザ.md "wikilink")。ハブには、[ブラウザインスタンス](../Page/ウェブブラウザ.md "wikilink")(WebDriver ノード)へのアクセスを提供するサーバのリストがあり、テストでこれらのインスタンスを使用できる。Selenium Grid を使用すると、複数のマシンで並行してテストを実行し、さまざまな[ブラウザのバージョンと](../Page/ウェブブラウザ.md "wikilink")[ブラウザの構成を](../Page/ウェブブラウザ.md "wikilink")、個別のテストではなく、集中管理できる。

リモート[ブラウザインスタンスでテストを実行する機能は](../Page/ウェブブラウザ.md "wikilink")、テストの負荷を複数のマシンに分散し、異なる[プラットフォームまたは](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")で実行されている[ブラウザでテストを実行するのに役立つ](../Page/ウェブブラウザ.md "wikilink")。後者は、テストに使用されるすべての[ブラウザが同じ](../Page/ウェブブラウザ.md "wikilink")[プラットフォームで実行できない場合に特に役立つ](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。

## 参考

  - 受け入れ試験
  - カピバラ（ソフトウェア）
  - Given-When-Then
  - Webテストツールのリスト
  - [MediaWiki Selenium拡張](https://ja.wikipedia.org/wiki/mw:Extension:Selenium "wikilink")
  - [MediaWiki Selenium Framework拡張](https://ja.wikipedia.org/wiki/mw:Selenium_Framework "wikilink")
  - 回帰試験
  - ロボットフレームワーク

## 脚注

## 外部リンク

  - [公式Webサイト](https://www.selenium.dev/)
  - [Selenium with Python — Selenium Python Bindings 2 documentation](https://selenium-python.readthedocs.io/)

[Category:Webオーサリングソフト](https://ja.wikipedia.org/wiki/Category:Webオーサリングソフト "wikilink") [Category:ユニットテスト・フレームワーク](https://ja.wikipedia.org/wiki/Category:ユニットテスト・フレームワーク "wikilink") [Category:未査読の翻訳があるページ](https://ja.wikipedia.org/wiki/Category:未査読の翻訳があるページ "wikilink")

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