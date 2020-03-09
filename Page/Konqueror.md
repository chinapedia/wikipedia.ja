> この記事は[Konqueror](https://ja.wikipedia.org/wiki/Konqueror)から翻訳されています。


**Konqueror** （コンカラー、コンケラー、コンキュラー）は、[KDE](../Page/KDE.md "wikilink")[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")の中核として設計された[ファイルビューア](https://ja.wikipedia.org/wiki/ファイルビューア "wikilink")としての機能を提供する[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")および[ファイルマネージャ](https://ja.wikipedia.org/wiki/ファイルマネージャ "wikilink")である。元々はボランティアによって開発されたもので、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")などの [Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のほか、[Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")上でも動作する。Konquerorは[KDEBase](https://ja.wikipedia.org/wiki/KDEBase "wikilink")パッケージ内の他のコンポーネントと同様に[GNU General Public Licenseの下で配布されている](../Page/GNU_General_Public_License.md "wikilink")。

## ユーザインタフェース

Konquerorは「ナビゲーションパネル」とともに縦横に動作し、表示するパネルは再配置したり追加したりできる。例えば、ユーザはブラウザ[ウィンドウ](../Page/ウィンドウ.md "wikilink")の左側に[ブックマーク](https://ja.wikipedia.org/wiki/ブックマーク "wikilink")パネルを配置し、ブックマークをクリックすることで、それぞれの[ウェブページ](../Page/ウェブページ.md "wikilink")を右のより大きなパネル内に表示させることができる。また、ユーザはひとつのパネル内に[フォルダ](https://ja.wikipedia.org/wiki/フォルダ "wikilink")の階層リストを表示させ、選択されたフォルダの中身をもう一つのパネル内に表示させることもできる。パネルはかなり柔軟性がありコンソールウィンドウを含めることさえできる。パネルの設定は保存でき、いくつかの標準設定がある（例えば、"[Midnight Commander](https://ja.wikipedia.org/wiki/Midnight_Commander "wikilink")" は二つのパネルに分割されたスクリーンを表示し、それぞれがフォルダ、ウェブサイトまたはファイルビューを含む）。

ナビゲーション機能（戻る、進む、履歴など）はすべての操作中で利用できる。ほとんどのキーボードショートカットはグラフィカルな設定を使って再配置でき、ナビゲーションはコントロールキーを押すことでアクティブなファイル上のノードに文字を割り当てることを通して行なうことができる。アドレスバーはローカルディレクトリ、過去の[URLや過去の検索項目に対する豊富な自動補完をサポートしている](../Page/Uniform_Resource_Locator.md "wikilink")。

このアプリケーションは[Tabbed Document Interfaceを使っており](https://ja.wikipedia.org/wiki/タブ_\(GUI\) "wikilink")、ウィンドウはタブで複数のドキュメントを含めることができる。[Multiple Document Interfaceはサポートされていないが](https://ja.wikipedia.org/wiki/Multiple_Document_Interface "wikilink")、同時に複数のドキュメントを見るのにウィンドウを再帰的に分割したり、単にもう一つのウィンドウを開いたりできる。

## ウェブブラウザ

[thumb](https://ja.wikipedia.org/wiki/ファイル:Wikipedia_main_page_in_Konqueror_3.5.8.png "wikilink") Konquerorは独立した[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")プロジェクトとして開発されてきた。[レンダリングエンジン](https://ja.wikipedia.org/wiki/レンダリングエンジン "wikilink")として通常[KHTML](../Page/KHTML.md "wikilink")を利用しており、[KHTML](../Page/KHTML.md "wikilink")は[HTMLに準拠し](../Page/HyperText_Markup_Language.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")アプレット、[Cascading Style Sheets](../Page/Cascading_Style_Sheets.md "wikilink")、[SSLや他の関連する](../Page/Transport_Layer_Security.md "wikilink")[オープン標準](https://ja.wikipedia.org/wiki/オープン標準 "wikilink")をサポートする。

Konquerorはいくつかのカスタマイズ可能な[検索サービスを統合しており](../Page/検索エンジン.md "wikilink")、サービスの略号（例えば、[Google](https://ja.wikipedia.org/wiki/Google "wikilink")については`gg:`）に続けて検索語を入力することでサービスにアクセスできる。ユーザは独自の検索サービスを追加することもできる。例えば、日本語版[ウィキペディア](https://ja.wikipedia.org/wiki/ウィキペディア "wikilink")の記事を取得するには、`http://ja.wikipedia.org/wiki/Special:Search?search=\{@}&go=Go` という URL を使い、[文字コード](../Page/文字コード.md "wikilink")セットを[utf-8にして](../Page/UTF-8.md "wikilink")`wp:`というウェブショートカットを追加する。

Konquerorのレンダリングスピードは競合ブラウザと同程度であるが、他のブラウザに比べて不正な形式のHTMLで書かれたサイトをあまり寛大にレンダリングしない。Konquerorの動作する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の下で動作しないウェブサイト上の[プラグイン](../Page/プラグイン.md "wikilink")の使用も問題の原因になりうる。[QuickTime](../Page/QuickTime.md "wikilink")[動画](../Page/動画.md "wikilink")や[Shockwave](https://ja.wikipedia.org/wiki/Adobe_Shockwave "wikilink")[アニメーション](../Page/アニメーション.md "wikilink")はそのような問題をもたらす。しかし、[SWF](https://ja.wikipedia.org/wiki/SWF "wikilink") (Flash)、[PDF](../Page/Portable_Document_Format.md "wikilink")、Javaアプレットやその他プラグインは、それぞれのソフトウェアがインストールされていれば、サポートされる。

## ファイルマネージャ

[thumb](https://ja.wikipedia.org/wiki/ファイル:Konqueror_large.png "wikilink") アドレスバー内に場所を入れるか、ファイルブラウザウィンドウ内の項目を選択することにより、Konquerorでローカルやリモート（[Samba](https://ja.wikipedia.org/wiki/Samba "wikilink")や[FTPなど](../Page/File_Transfer_Protocol.md "wikilink")）のディレクトリ階層をブラウズすることができる。異なるビューでブラウズすることができ、ビュー間では[アイコン](../Page/アイコン.md "wikilink")やレイアウトの使用法が異なる。ファイルを[実行したり](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")、表示したり、コピーしたり、移動したり、リンクしたり、削除することもできる。

ユーザは組み込まれた[Konsole](https://ja.wikipedia.org/wiki/Konsole "wikilink")を開くこともでき、その中でシェルコマンドを直接実行できる。

この機能はKonquerorから削除されていないが、KDE 4のKonquerorは標準のファイルマネージャとしての[Dolphinによって置き換えられた](https://ja.wikipedia.org/wiki/Dolphin_\(ファイルマネージャ\) "wikilink")。

## ファイルビュアー

[KPart](https://ja.wikipedia.org/wiki/KPart "wikilink")s[オブジェクトモデル](https://ja.wikipedia.org/wiki/オブジェクトモデル "wikilink")を使って、Konquerorは特定の[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")を表示（し、場合によっては編集）できるコンポーネントを実行し、それぞれのファイルが開かれているKonquerorのパネルに直接クライアント領域を組み込む。これにより、例えば、[PDFドキュメントや](../Page/Portable_Document_Format.md "wikilink")（[KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink")を通して）[OpenDocument](https://ja.wikipedia.org/wiki/OpenDocument "wikilink")をKonqueror内で直接見ることができるようになる。[KPart](https://ja.wikipedia.org/wiki/KPart "wikilink")sモデルを正しく実装している、どのアプリケーションもこのような方法で組み込むことができる。

KPartsはHTMLページにある種のマルチメディアコンテンツを組み込むのにも使われる。例えば[KMPlayer](https://ja.wikipedia.org/wiki/KMPlayer "wikilink")のKPartによって、ウェブページ上に組み込まれたビデオをKonquerorが表示できるようになる。

## KIO

[thumb](https://ja.wikipedia.org/wiki/ファイル:Konqi-audiocd.png "wikilink")  ファイルやウェブサイトをブラウズするのに加え、Konquerorは機能を拡張するのに他のブラウザやファイルマネージャよりはるかに優れたKIOプラグインを利用している。[HTTPや](../Page/Hypertext_Transfer_Protocol.md "wikilink")[FTP](../Page/File_Transfer_Protocol.md "wikilink")（これらに対するサポートは組込みである）のような異なるプロトコルにアクセスするのに、KIOというKonqueror I/O プラグインシステムのコンポーネントを使っている。

同様に、[ZIPファイル](../Page/ZIP_\(ファイルフォーマット\).md "wikilink") などのアーカイブファイル、smb (Windows) 共有にアクセスしたり、ed2kリンク (edonkey/emule) を処理したり、[オーディオCD](../Page/コンパクトディスク.md "wikilink") をブラウズしたり ("audiocd:/")、[ドラッグ・アンド・ドロップ](https://ja.wikipedia.org/wiki/ドラッグ・アンド・ドロップ "wikilink")を通して[リッピング](https://ja.wikipedia.org/wiki/リッピング "wikilink")したりするのに、KonquerorはIOslavesと呼ばれるKIOプラグインを使うことができる。FISH ("<fish://user@host>") IOslaveによってKonquerorでリモートの[Secure Shellサービス上のファイルを管理することができるようになり](../Page/Secure_Shell.md "wikilink")、"man:" と "info:" IOslaves はフォーマット通りのドキュメントを取得するのに役立つ。

完全なリストは[KDE 情報センターのプロトコルセクション内で得られる](https://ja.wikipedia.org/wiki/KInfoCenter "wikilink")。

## 動向

最近ではKHTMLをベースに開発された[WebKit](https://ja.wikipedia.org/wiki/WebKit "wikilink")が[アップルの](../Page/アップル_\(企業\).md "wikilink")[Safari](../Page/Safari.md "wikilink")に採用されるなど、KDE以外のブラウザとしても活発に開発が行われている。一方、[Mozilla](https://ja.wikipedia.org/wiki/Mozilla "wikilink")の[Gecko](../Page/Gecko.md "wikilink")がKDEに移植され、Konquerorでも利用できるようになったほか、[KDE](../Page/KDE.md "wikilink")のファイルマネージャ[Dolphinとの統合が進むなど](https://ja.wikipedia.org/wiki/Dolphin_\(ファイルマネージャ\) "wikilink")、他のプロジェクトとの融合も進んでいる。

## 関連項目

  - [ファイル (GNOME)](https://ja.wikipedia.org/wiki/ファイル_\(GNOME\) "wikilink")

## 外部リンク

  - [KDE 公式サイト](http://www.kde.org/)
  - [Konqueror 公式サイト](http://www.konqueror.org/)
  - [Konqueror ハンドブック](http://docs.kde.org/stable/en/kdebase-apps/konqueror/index.html)

[Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink") [Category:KHTMLを用いたウェブブラウザ](https://ja.wikipedia.org/wiki/Category:KHTMLを用いたウェブブラウザ "wikilink") [Category:ファイルマネージャ](https://ja.wikipedia.org/wiki/Category:ファイルマネージャ "wikilink") [Category:1996年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1996年のソフトウェア "wikilink")