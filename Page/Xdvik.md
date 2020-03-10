> この記事は[Xdvik](https://ja.wikipedia.org/wiki/Xdvik)から翻訳されています。


**xdvik** は、[X Window System用の](../Page/X_Window_System.md "wikilink")[オープンソース](../Page/オープンソース.md "wikilink")の[DVIファイルビューアーである](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink")。[xdvi](https://ja.wikipedia.org/wiki/xdvi "wikilink")を基に作られているが、[xdvi](https://ja.wikipedia.org/wiki/xdvi "wikilink")とは異なり[kpathsea](https://ja.wikipedia.org/wiki/kpathsea "wikilink")が含まれる。xdvikのバージョン番号は対応する[xdvi](https://ja.wikipedia.org/wiki/xdvi "wikilink")に追従し、その後ろにパッチレベルの番号が付加される。たとえば、xdvikのバージョン 22.84.10は[xdvi](https://ja.wikipedia.org/wiki/xdvi "wikilink")のバージョン 22.84に対応し、パッチレベルが10であることを示す。

## 特徴

xdvik-22.84には以下のような特徴がある。

  - 全機能についてキーボードによる操作をサポートする
  - [ghostscript](https://ja.wikipedia.org/wiki/ghostscript "wikilink")により、[PostScript](../Page/PostScript.md "wikilink")画像ファイルのレンダリングを行う
  - インバース検索 - xdvi のウィンドウをクリックすることにより、対応する [](../Page/TeX.md "wikilink") ソースをエディタでオープンできる（その逆も可能）
  - カラースペシャルをサポート
  - DVIファイルのPostScript版の印刷・保存が可能

また、22.84で新たに加わった機能は以下の通り。

  - hyperrefパッケージによるDVIファイルのハイパーリンクに対応
  - DVIファイルの文字列検索ができる
  - DVIファイルを自動的にリロードするためのオプション
  - ファイルが壊れているときはDVIファイルのバックアップコピーを使用する。それにより、(La) の実行中も旧バージョンのドキュメントを見ることができる。
  - t1libによりPostScriptフォントのレンダリングが可能
  - GUIの向上 : ナビゲーション用のページリスト、ステータスライン、ツールバー、選好ウィンドウ（Motif 版）
  - DVIファイルを以下のフォーマットにして保存できる : PS、PDF、DVI、プレーンテキスト
  - DVIファイル内のテキストを検索できる。
  - Kpathseaライブラリにより、ファイルの配置・生成を行う
  - Omegaをサポート

## 関連項目

  - [xdvi](https://ja.wikipedia.org/wiki/xdvi "wikilink")
  - [](../Page/TeX.md "wikilink")

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink")