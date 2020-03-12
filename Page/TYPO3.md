> この記事は[TYPO3](https://ja.wikipedia.org/wiki/TYPO3)から翻訳されています。


**TYPO3**は、フリーのオープンソース[コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink")である。[PHPで書かれたモデル](../Page/PHP_\(プログラミング言語\).md "wikilink") - ビュー - コントローラー (MVC) のウェブアプリケーション開発フレームワークであり、[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) の下で開発されている。[Linux](../Page/Linux.md "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")および[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")上の[Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink") (Apache) または[Internet Information Services](../Page/Internet_Information_Services.md "wikilink") (IIS) で動作する。

## 歴史

TYPO3は、最初に[Kasper Skårhøj](http://typo3.org/community/people/kaspers-korner/)によって作成された。

TYPO3に接続可能なエクステンションの多くは[サードパーティー](../Page/サードパーティー.md "wikilink")の開発者によって書かれている。

## 特徴

既存の[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")、機能およびモジュールに加え、TYPO3に柔軟性と拡張性を追加するエクステンションが公開されている巨大なリポジトリがある。10,000個以上のエクステンションが、[GNU General Public Licenseの下で](../Page/GNU_General_Public_License.md "wikilink")[TYPO3エクステンションリポジトリ (TER)](https://extensions.typo3.org/) と呼ばれるリポジトリからダウンロード可能である。

TYPO3は、ユーザ向けに提供されるウェブサイトとなるウェブフロントエンドと、ウェブサイトのコンテントを管理するために編集者およびサイト管理者によって利用されるウェブベースのバックエンドから構成される。TYPO3は、Linux、WindowsおよびmacOS上の ApacheまたはIISで動作する。PHPと [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[Oracle](../Page/Oracle_Database.md "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")などの [TYPO3 DBAL](http://typo3.org/documentation/document-library/extension-manuals/dbal/1.0.0/view/) によってサポートされるリレーショナルデータベースシステムを使う。ハードウェア要件としては、最近のCPUと256MBのRAMを搭載するサーバで動作し、フロントエンドは、[JavaScript](../Page/JavaScript.md "wikilink")が動作する、あらゆるOSの[Mozilla Firefoxのようなブラウザで表示可能である](../Page/Mozilla_Firefox.md "wikilink")。

### 設計

システムはテンプレートを基本としている。既存のテンプレートを選択して、ロゴ、色およびフォントなどの特徴を変更することができる。または、TypoScriptという設定言語を使って独自のテンプレートを作成することもできる。この単純な記法を用いて、データベースのデータと置き換えられるプレースホルダーとなる情報を大きなオブジェクトツリーへと構成することができる。値や機能を変更または追加することでプログラム済みのオブジェクトが設定される。このオブジェクトツリー構造はテキストファイルに保存される。さまざまなエディタがコンテントの変更に利用可能である。コンテントの生成にはこのデータ構造を使う。TypoScriptは、条件以外の制御構造を持たない; 実際の処理が実行されるときには、PHP関数に渡される。トップレベルオブジェクトはPAGEオブジェクトである。MENUオブジェクトにはさまざまなタイプがある。

### TypoScriptの文法

基本的な文法は:

`   [オブジェクトパス].[属性]  [演算子]  [値]`

演算子は

`   * = 値の割り当て`
`   * < オブジェクト全体のコピー`
`   * =< 参照の挿入`
`   * > オブジェクトの削除`

例題:

`   myObject.attribute1=Hello`

コンテントは主に、2つのテーブルに格納される: 1つは、「pages」というテーブル、もう1つは、「tt_content」である。これらは、ページに含まれる要素を保持する。各ページオブジェクトには固有の識別キー(uid)があり、現在のページにリンクしている。そのため、ページはツリー状に構成され、システムが簡単にメニューとサイトマップを生成できるようになっている。

TYPO3を特徴づける1つの鍵は、開発者がそれぞれに追加機能を提供することを可能にする柔軟なアプリケーションプログラミングインタフェースを持つことである。このAPIを使っているモジュールのことを「エクステンション」といい、多くの開発者がTYPO3の開発者ポータルの公開リポジトリにエクステンションを提供している。

### TemplaVoila

TemplaVoilaは、TYPO3のもう1つのテンプレートエンジンエクステンションである。テンプレートを作成するグラフィカルなマッピングツールが含まれ、別のページモジュール、フレキシブルコンテントエレメントを作成する機能と開発者向けのAPIがある。新しいコンテントエレメントタイプをプログラムすることなく作成できる。

TemplaVoilaは、完全に統合されたデザインにそって編集者がより直観的にコンテントを扱うことができ、TYPO3標準のテンプレーティングよりもウェブページの保守を柔軟にする。その一方で、標準テンプレートよりも若干遅くなる。

## 関連項目

  - [コンテンツ管理システム](../Page/コンテンツ管理システム.md "wikilink") (CMS)

## 外部リンク

  - [公式サイト](https://typo3.org/)
  - [TYPO3 GmbH](https://typo3.com/)
  - [TYPO3 UsersGroup Japan](https://typo3.jp/)
  - [スタイルチューン株式会社](https://www.stune.co.jp/)

[Category:コンテンツ管理システム](https://ja.wikipedia.org/wiki/Category:コンテンツ管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")