> この記事は[Inkscape](https://ja.wikipedia.org/wiki/Inkscape)から翻訳されています。


**Inkscape**（インクスケープ）は[オープンソース](../Page/オープンソース.md "wikilink")で開発されている[ベクトル画像編集](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")（[ドローソフト](../Page/ドローソフト.md "wikilink")）。Inkscape は[XML](../Page/Extensible_Markup_Language.md "wikilink")、[SVG](../Page/Scalable_Vector_Graphics.md "wikilink")、[CSS](../Page/Cascading_Style_Sheets.md "wikilink") などの標準に完全に準拠したグラフィックツールとなることを目標としている。[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")なソフトウェアであり、[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS)、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") などで動作する。開発の主体は[Linux](../Page/Linux.md "wikilink")で行われている。

Inkscapeは[2003年](../Page/2003年.md "wikilink")にベクトル画像編集ソフト[Sodipodi](https://ja.wikipedia.org/wiki/Sodipodi "wikilink")からの[フォークとしてスタートした](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。Inkscape は現状でも幅広く利用されているが、今後さらに SVG、CSSの標準への準拠を完全にしていくことが可能で、それにはSVGアニメーションの対応も含まれる。現在も活発に開発中であり、新しい機能が定期的に加えられている。

## 歴史

Inkscapeは、[2003年](../Page/2003年.md "wikilink")にSodipodiの[フォークとしてスタートした](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。元となったSodipodiは2004年2月のバージョン 0.34 より事実上開発が停止している\[1\]。さらにそのSodipodiはGill (**G**nome **Ill**ustration app.\[2\]、Raph Levienによって書かれたドローソフト）のフォークとして[1999年](../Page/1999年.md "wikilink")にスタートした。

Sodipodiの開発者であったTed Gould、Bryce Harrington、MenTaLguYが、プロジェクトの目的の差異、外部からのコントリビューションに積極的でないこと、技術的な意見の差異などから、2003年にSodipodiから分かれてInkscapeプロジェクトを立ち上げた。彼らは[SVGの完全準拠を目的にすることにした](../Page/Scalable_Vector_Graphics.md "wikilink")。

開発はトップダウン方式ではなく、多くの開発者が平等かつ活発に参加する方式を取っている。このような方式であるために多くの新規開発者が加わった。Sodipodiは[GIMP](../Page/GIMP.md "wikilink")に似たControlled Single Document Interface (CSDI) を採用していたが、開発者の一人のBulia Byakは、現在のInkscapeの[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")のアーキテクチャを作成した。

Inkscapeは元のSodipodiの[コードに対して数多くの変更が加えられている](../Page/ソースコード.md "wikilink")。例えば、開発言語を[Cから](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")に変えたこと、[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")ベースからそのC++[バインディングである](https://ja.wikipedia.org/wiki/言語バインディング "wikilink")[gtkmm](https://ja.wikipedia.org/wiki/gtkmm "wikilink")ベースに変えたこと、ユーザインタフェースをデザインしなおして改善したこと、そのほか数多くの新機能を追加したことなどである。

### リリース履歴

Sodipodiのリリースについては示さず、[フォーク後のInkscapeのみ以下に示す](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")。

| リリース日                                                                      | バージョン  | 備考                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [2003年](../Page/2003年.md "wikilink")[10月14日](../Page/10月14日.md "wikilink") | 0.35   | Inkscapeの最初のリリース。この時点ではSodipodiからのフォーク直後であり、非常に類似したソフトであった。                                                                                                                                                                                                                                                                           |
| 2004年                                                                      | 0.36   | メニューバーやツールバーをドキュメントウィンドウごとにあるユーザインタフェースに変更した。                                                                                                                                                                                                                                                                                         |
| 2004年2月10日                                                                 | 0.37   | パスのインセットやアウトセット、論理演算 (boolean operator) を追加した。                                                                                                                                                                                                                                                                                        |
| 2004年4月8日                                                                  | 0.38.1 | バグフィックスの他、テキストの[カーニング](https://ja.wikipedia.org/wiki/カーニング "wikilink")や[トラッキング](https://ja.wikipedia.org/wiki/トラッキング "wikilink")や多段グラデーションのサポートの他、使い勝手を向上させた。                                                                                                                                                                         |
| 2004年7月15日                                                                 | 0.39   | [Pango](../Page/Pango.md "wikilink") を使った最初のリリースで他言語の取り扱いがよくなった。また、マーカーやクローンやパターンをサポートした。                                                                                                                                                                                                                                             |
| 2004年11月28日                                                                | 0.40   | レイヤーや[ビットマップ画像](../Page/ビットマップ画像.md "wikilink")のトレース機能やテキストをパスに乗せる機能を追加。                                                                                                                                                                                                                                                              |
| 2005年2月10日                                                                 | 0.41   | グリッド配置やカラートレースを追加。                                                                                                                                                                                                                                                                                                                    |
| 2005年7月24日                                                                 | 0.42   | テキストのフロー配置（テキストをフレームに挿入）を追加。テキストスパンのサポート。グラデーションツールを新しくした。                                                                                                                                                                                                                                                                            |
| 2005年11月19日                                                                | 0.43   | コネクターツール、ホワイトボード機能の追加。タブレットのサポート、ノードツールの使い勝手を向上した。                                                                                                                                                                                                                                                                                    |
| 2006年6月22日                                                                 | 0.44   | レイヤダイアログ、クリッピング、マスキングのサポート、透過 [PDF](../Page/Portable_Document_Format.md "wikilink") 出力の改善。[OpenDocument](../Page/OpenDocument.md "wikilink")フォーマットのエクスポートに対応。                                                                                                                                                                         |
| 2007年2月5日                                                                  | 0.45   | ガウスぼかしのサポート。                                                                                                                                                                                                                                                                                                                          |
| 2007年3月23日                                                                 | 0.45.1 | バグフィックスとユーザーインターフェースの翻訳の改善。                                                                                                                                                                                                                                                                                                           |
| 2008年3月24日                                                                 | 0.46   |                                                                                                                                                                                                                                                                                                                                       |
| 2009年11月24日                                                                | 0.47   | 自動保存、スペルチェッカー機能の追加。フィルタの追加。PS、EPS出力の改善。                                                                                                                                                                                                                                                                                               |
| 2010年8月23日                                                                 | 0.48   | スプレーツール、マルチパス編集、上付き・下付きなどのテキスト関連の強化。                                                                                                                                                                                                                                                                                                  |
| 2015年1月30日                                                                 | 0.91   | レンダリングエンジン[cairo](https://ja.wikipedia.org/wiki/cairo "wikilink")の採用、[OpenMP](../Page/OpenMP.md "wikilink")によるマルチスレッド処理への対応、テキストツールの改良、ものさしツール、タイプデザイン機能、シンボルライブラリとVisioステンシルのサポート、[WMF/EMFのインポートおよびエクスポート](../Page/Windows_Metafile.md "wikilink")、実世界での単位（[ミリメートル](../Page/ミリメートル.md "wikilink")など）のサポート、メモリ消費量の大幅な減少、反応性の向上、他\[3\] |
| 2017年1月4日                                                                  | 0.92   | [SVG2](../Page/Scalable_Vector_Graphics.md "wikilink")、[CSS3への対応の改善](../Page/Cascading_Style_Sheets.md "wikilink")\[4\]。 Inkscapeのデフォルト解像度を90dpiから96dpiに変更\[5\]。                                                                                                                                                                      |
| 2018年3月22日                                                                 | 0.92.3 | [双方向テキスト](https://ja.wikipedia.org/wiki/双方向テキスト "wikilink")に対応\[6\]。 windowsユーザーに対する起動パフォーマンスの改善\[7\]。                                                                                                                                                                                                                                |

[USBメモリ](https://ja.wikipedia.org/wiki/USBメモリ "wikilink")などの上で動作可能な[ポータブルアプリケーション](../Page/ポータブルアプリケーション.md "wikilink")として**Inkscape Portable**も開発されている。

## 関連項目

  - [Adobe Illustrator](../Page/Adobe_Illustrator.md "wikilink")
  - [CorelDRAW](../Page/CorelDRAW.md "wikilink")
  - [OpenDocumentをサポートするアプリケーションの一覧](https://ja.wikipedia.org/wiki/OpenDocumentをサポートするアプリケーションの一覧 "wikilink")
  - [Scalable Vector Graphics](../Page/Scalable_Vector_Graphics.md "wikilink") (SVG)
  - [Open Clip Art Library](../Page/Open_Clip_Art_Library.md "wikilink") - Sodipodiは世界の国旗などのSVG[クリップアート](../Page/クリップアート.md "wikilink")コレクションを開始した。その作業がOpen Clip Art Libraryの発祥の一因となった。
  - [GIMP](../Page/GIMP.md "wikilink") - オープンソースで開発されている[ペイントソフト](../Page/ペイントソフト.md "wikilink")
  - [LibreOffice](https://ja.wikipedia.org/wiki/LibreOffice "wikilink") - オープンソースで開発されている[オフィスソフト](https://ja.wikipedia.org/wiki/オフィスソフト "wikilink")

## 参考文献

## 外部リンク

  -   - [チュートリアル - 基本](http://www.inkscape.org/doc/basic/tutorial-basic.ja.html)

  -
  -
[Category:画像処理ソフト](https://ja.wikipedia.org/wiki/Category:画像処理ソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:GTK+を使用するソフトウェア](https://ja.wikipedia.org/wiki/Category:GTK+を使用するソフトウェア "wikilink") [Category:OpenDocument](https://ja.wikipedia.org/wiki/Category:OpenDocument "wikilink") [Category:ドローソフト](https://ja.wikipedia.org/wiki/Category:ドローソフト "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.  [Sodipodiのメーリングリストの過去ログ](http://sourceforge.net/mailarchive/message.php?msg_id=loom.20050120T134439-394%40post.gmane.org)
2.  <http://www.levien.com/svg/>
3.  [Release notes/0.91/ja](http://wiki.inkscape.org/wiki/index.php/Release_notes/0.91/ja)、2015年2月2日版
4.  [公式サイト - Inkscape Version 0.92 is Released\!](https://inkscape.org/en/news/2017/01/04/inkscape-version-092-released)
5.
6.  [公式サイト - Announcing the 0.92.3 Release of Inkscape](https://inkscape.org/en/news/2018/03/22/announcing-0923-release-inkscape/)
7.