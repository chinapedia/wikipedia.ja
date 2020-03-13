> この記事は[NeoOffice](https://ja.wikipedia.org/wiki/NeoOffice)から翻訳されています。


**NeoOffice**（ネオオフィス）は、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")用の[ソフトウェア](../Page/ソフトウェア.md "wikilink")。[オープンソース](../Page/オープンソース.md "wikilink")の[オフィススイート](../Page/オフィススイート.md "wikilink")である[OpenOffice.org](../Page/OpenOffice.org.md "wikilink")（以下、OOo）から分岐して開発されていたもので、同バージョンのOOoとほぼ同等の機能を備えていた。2018年6月現在は、[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink") 4.4ベースとなっている。[ワープロ](../Page/ワードプロセッサ.md "wikilink")、[表計算](../Page/表計算ソフト.md "wikilink")、[プレゼンテーション](../Page/プレゼンテーション.md "wikilink")、[ドローソフト](../Page/ドローソフト.md "wikilink")の機能がある。

開発元は[NeoOffice.org](http://www.neooffice.org/)で、主な開発者は Patrick Luby と Edward Peterlin。[Solaris](../Page/Solaris.md "wikilink")と[Linux](../Page/Linux.md "wikilink")用に開発されたOOoと、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の[Aqua](../Page/Aqua_\(コンピュータ\).md "wikilink")[インタフェースを統合するために](../Page/インタフェース_\(情報技術\).md "wikilink")、過去には[Java](https://ja.wikipedia.org/wiki/Java "wikilink")テクノロジーが使われていた。LibreOfficeベースの2018年現在はDBなどの一部機能を除いてJavaは使われていない\[1\]。

## 概要

OpenOffice.org3.0より以前、OpenOffice.orgにはすでに[X11版があったが](../Page/X_Window_System.md "wikilink")、Aquaネイティヴで動くOpenOffice.orgの開発は長年停滞していた。そのためMac上でネイティヴに動くOpenOffice.orgを開発することを目的に開発が始まった。

## 特徴

[X11には問題があり](../Page/X_Window_System.md "wikilink")、macOSで利用できるが、X11版OOoの使用には[Apple X11か](https://ja.wikipedia.org/wiki/XQuartz "wikilink")[XDarwin](https://ja.wikipedia.org/wiki/XDarwin "wikilink")をインストールする必要があり、また日本語入力などいくつかの問題がある。そのため、Mac上ではOOoでなくNeoOfficeの利用が推奨されていた\[2\]。

NeoOfficeのほうがインストールが簡単で、Aqua版OpenOffice.orgより概ねAquaライクなインタフェース（デスクトップ上部のメニューバーや親切なキーボードショートカットなど）を備え、macOSの[フォント](../Page/フォント.md "wikilink")や印刷サービス、[クリップボード](../Page/クリップボード.md "wikilink")、[ドラッグ・アンド・ドロップ](../Page/ドラッグ・アンド・ドロップ.md "wikilink")機能などが利用でき、OOoよりMacとの親和性が高い。

ただし、NeoOfficeをストレス無く動かすにはX11版より多くの[メモリが必要であり](../Page/主記憶装置.md "wikilink")、いくつかの機能の処理速度がやや遅いことが指摘されている。また追加されたコードはOOoほどテストを受けているとはいえない。

2018年時点のNeoOfficeは、[Microsoft Officeとの](../Page/Microsoft_Office.md "wikilink")[互換性](../Page/互換性.md "wikilink")のある、LibreOffice 4.4ベースである。

## 開発

NeoOffice/Jは[GPLライセンスを採用しており](../Page/GNU_General_Public_License.md "wikilink")、その[ソースコード](../Page/ソースコード.md "wikilink")を改変して作成したソフトウェアを配布する場合、[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")として提供されなければならないと定めている。対してOOoは以前[LGPLライセンスと](../Page/GNU_Lesser_General_Public_License.md "wikilink")[SISSL](https://ja.wikipedia.org/wiki/SISSL "wikilink")を使用していたが、SISSLの廃止によりLGPLに一本化された。なおOpenOffice.orgの商業版として、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が[StarOfficeを販売していた](../Page/StarSuite.md "wikilink")。

関連プロジェクトにNeoOffice/Cがある。これは、ネイティブなmacOS版OOo 2.0を作るためのプロトタイプとして、[アップルの](../Page/アップル_\(企業\).md "wikilink")[Cocoa](../Page/Cocoa.md "wikilink") [APIを使ってmacOS用OOo](../Page/アプリケーションプログラミングインタフェース.md "wikilink") 1.xを開発するプロジェクトである。しかし、NeoOffice/Cは実装が非常に難しいことが判明した。アプリケーションは非常に不安定である。そのため、もっと見込みのあるNeoOffice/Jが支持され、NeoOffice/Cは棚上げにされた。

NeoOffice 1.2 のリリース時に、これまでのアプリケーション名から/Jが削られることが発表され NeoOffice に変更された。

\#2008年10月に[Mac OS X v10.4以降にネイティブ対応した本家OOo](../Page/Mac_OS_X_v10.4.md "wikilink") 3.0が公開された。

2012年リリースされたNeoOffice 3.3以降のバージョンは、 JavaベースではなくCocoaベースになっている\[3\]\[4\]。

2017年に、古いOOo 3.1.1コードベースから、LibreOffice 4.4コードベースに移行が完了した\[5\]。

2018年現在、最新バージョンは、[Mac App Storeにて販売されている](https://ja.wikipedia.org/wiki/Mac_App_Store "wikilink")\[6\]。

## 関連項目

  - [オフィススイートの比較](../Page/オフィススイートの比較.md "wikilink")
  - **[Apache OpenOffice](https://ja.wikipedia.org/wiki/Apache_OpenOffice "wikilink")**
  - **[LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink")**

## 脚注

<references />

## 外部リンク

  - [NeoOffice](http://www.neooffice.org)開発本家
  - [NeoOfficeホーム](http://download.neooffice.org/neojava/ja/index.php) 日本語ページ

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:オフィスソフト](https://ja.wikipedia.org/wiki/Category:オフィスソフト "wikilink") [Category:MacOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:MacOSのソフトウェア "wikilink") [Category:OpenDocument](https://ja.wikipedia.org/wiki/Category:OpenDocument "wikilink")

1.
2.  [OOoの日本語プロジェクト](http://wiki.services.openoffice.org/wiki/Ja.start_mac)。
3.
4.
5.
6.  [NeoOffice](https://itunes.apple.com/jp/app/neooffice/id639210716?mt=12) Mac App Store