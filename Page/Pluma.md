> この記事は[Pluma](https://ja.wikipedia.org/wiki/Pluma)から翻訳されています。


**pluma**は、[gedit](https://ja.wikipedia.org/wiki/gedit "wikilink") 2をフォークして作られた[テキストエディタ](../Page/テキストエディタ.md "wikilink")である。[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で使用される[MATEのデフォルトのテキストエディタである](https://ja.wikipedia.org/wiki/MATE_\(デスクトップ環境\) "wikilink")。plumaは、基本的な機能のほか、追加の[プラグイン](../Page/プラグイン.md "wikilink")で機能を拡張することができる。

plumaは、複数のファイルを一度に編集することができる（[タブ](../Page/タブ.md "wikilink")または[MDI](https://ja.wikipedia.org/wiki/MDI "wikilink")をサポート）グラフィカルなアプリケーションである。また、国際化されており、[Unicode](../Page/Unicode.md "wikilink") [UTF-8](../Page/UTF-8.md "wikilink")を用いている。plumaは一般的なテキストエディタとしては標準的な機能をサポートしており、簡潔さと使いやすさを強調している。plumaの核となる機能は、ソースコードのシンタックスハイライティング、オートインデント、プレビュー機能付きの[印刷](../Page/印刷.md "wikilink")のサポートなどである。

plumaは、MATEプロジェクトの思想に従って、クリーンでシンプルな[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")にデザインされており、MATEのデフォルトのテキストエディタとなっている。また、plumaは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")、[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアであり、[GNU GPLバージョン](https://ja.wikipedia.org/wiki/GNU_GPL "wikilink") 2以降に従う。

## 機能

plumaは完全にMATEに統合されており、Caja（MATEの[ファイルマネージャ](../Page/ファイルマネージャ.md "wikilink")）からのドロップが可能で、MATE Virtual File System、MATEのプリントフレームワーク、MATEのヘルプシステムを使っている\[1\]。

plumaは、[MDI](https://ja.wikipedia.org/wiki/MDI "wikilink")の機能や、GUIによるタブ機能を持っており、複数のファイルを編集することができる。タブは、複数のウィンドウの間をユーザーの手で自由に移動することができる。また、[GVfs](https://ja.wikipedia.org/wiki/GVfs "wikilink")を使ってリモートのファイルを編集することも可能である。他のコード指向の機能としては、行番号の表示、ブラケットのマッチング、テキスト折り返し、現在の行のハイライト、オートインデントや自動的なファイルのバックアップなどがある。

plumaは[印刷](../Page/印刷.md "wikilink")機能をサポートしており、これには印刷プレビューや[PostScript](../Page/PostScript.md "wikilink")や[PDF](https://ja.wikipedia.org/wiki/PDF "wikilink")への印刷のサポートが含まれている。印刷オプションは、テキストの[フォント](../Page/フォント.md "wikilink")や、ページサイズ、向き、余白、オプションのページヘッダーや行番号、シンタックスハイライティングが含まれている\[2\]。

加えて、plumaはGtkSourceView\[3\]経由で、様々なプログラムコードやマークアップのフォーマットに対応したシンタックスハイライティングを提供する。

### 機能のリスト

  - シンタックスハイライティング
  - 印刷と印刷プレビューのサポート
  - ファイルのリバート
  - UTF-8テキストの完全なサポート
  - リモートファイルの編集のサポート
  - 検索と置換
  - 設定可能なプラグインシステム（[Python](../Page/Python.md "wikilink")のサポートを含む）
  - 完全な設定のインターフェース

### プラグインのリスト

いくつかのプラグインは、plumaに予めパッケージングされ、インストールされている（外部プラグインも利用可能である）。

  - ファイルブラウザー
  - タグリスト
  - 文字数カウント
  - スペルチェッカー
  - 日付/時刻の挿入
  - ソート
  - 選択されたテキストのケースの変更
  - 自動的なスニペットの拡張
  - 外部ツール群
  - SyncTeX

## アーキテクチャ

MATE Core Applicationsの一部として、plumaは、最新の[GTK](https://ja.wikipedia.org/wiki/GTK "wikilink")とMATEのライブラリを使っている。また、plumaのソースコードは[Git](../Page/Git.md "wikilink")により管理されている\[4\]。

## 関連項目

  - [テキストエディタの一覧](https://ja.wikipedia.org/wiki/テキストエディタの一覧 "wikilink")

## 脚注

## 外部リンク

  -
[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink")

1.  [pluma: General Information](https://github.com/mate-desktop/pluma/blob/master/README) 15 February 2008
2.
3.  [GtkSourceView home page](https://wiki.gnome.org/Projects/GtkSourceView)
4.  [pluma @ GitHub](https://github.com/mate-desktop/pluma)