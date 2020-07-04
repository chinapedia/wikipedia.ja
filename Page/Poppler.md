> この記事は[Poppler](https://ja.wikipedia.org/wiki/Poppler)から翻訳されています。


**Poppler**とは、[PDF](../Page/Portable_Document_Format.md "wikilink") ドキュメントの閲覧に用いられる[フリーのプログラミング](../Page/フリーソフトウェア.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")である。[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") によって管理されている。Poppler は [Xpdf](https://ja.wikipedia.org/wiki/Xpdf "wikilink") をベースとし、レンダリングエンジンの扱い方を変えファイルの表示を効率化し、また（Xpdf は独立したソフトウェアであるが） [OS](../Page/オペレーティングシステム.md "wikilink") の機能性を統合しそれを利用するという、Xpdf の目的それ以上のものを達成するために作成された。

Poppler はいくつかの PDF ビューアに用いられており、Xpdf に対するバックエンドとして用いることも出来る。また、[KOffice](https://ja.wikipedia.org/wiki/KOffice "wikilink") のような他のアプリケーションにも用いられている。

Poppler という名前は、テレビアニメーションシリーズである“[フューチュラマ](../Page/フューチュラマ_\(アニメ\).md "wikilink")”のシーズン2、第15話に付けられたタイトル“The Problem with Popplers”に由来する。

## Poppler を用いた PDF リーダー

いくつかのフリーソフトウェアは、PDF ドキュメントの描写に Poppler を利用する。\[1\]

| 名前                                                                                        | フロントエンド                                                                       | URL                                                                     |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [Evince](../Page/Evince.md "wikilink")                                                    | [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")                         | <http://www.gnome.org/projects/evince/>                                 |
| [Okular](../Page/Okular.md "wikilink")                                                    | [Qt](../Page/Qt.md "wikilink")4                                               | <http://okular.kde.org/>                                                |
| [KDE 3 PDF kfile plugin](https://ja.wikipedia.org/wiki/KDE_3_PDF_kfile_plugin "wikilink") | [Qt](../Page/Qt.md "wikilink")                                                | <http://websvn.kde.org/branches/KDE/3.5/kdegraphics/kfile-plugins/pdf/> |
| [PopplerKit](https://ja.wikipedia.org/wiki/PopplerKit "wikilink")                         | [GNUstep](../Page/GNUstep.md "wikilink")/[Cocoa](../Page/Cocoa.md "wikilink") | <http://svn.gna.org/viewcvs/gsimageapps/trunk/Frameworks/PopplerKit/>   |
| [Vindaloo](https://ja.wikipedia.org/wiki/Vindaloo "wikilink")                             | PopplerKit                                                                    | <http://svn.gna.org/viewcvs/gsimageapps/trunk/Applications/Vindaloo/>   |
| [ePDFView](https://ja.wikipedia.org/wiki/ePDFView "wikilink")                             | [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")                         | <http://trac.emma-soft.com/epdfview/>                                   |
| [TeXworks](https://ja.wikipedia.org/wiki/TeXworks "wikilink")                             | [Qt](../Page/Qt.md "wikilink")4                                               | <http://code.google.com/p/texworks/>                                    |
| [LocoPDF](https://ja.wikipedia.org/wiki/LocoPDF "wikilink")                               | none                                                                          | <https://github.com/quickhand/locopdf/>                                 |
| [DiffPDF(オープンソース版)](https://ja.wikipedia.org/wiki/DiffPDF\(オープンソース版\) "wikilink")         | [Qt](../Page/Qt.md "wikilink")4                                               | <http://www.qtrac.eu/diffpdf-foss.html>                                 |

## [Xpdf](https://ja.wikipedia.org/wiki/Xpdf "wikilink") を拡張した機能

  - [Cairo](../Page/Cairo.md "wikilink")を描画バックエンドに用いているため、[アンチエイリアス](../Page/アンチエイリアス.md "wikilink")処理がなされた[ベクターイメージ](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")と透過オブジェクトを使用することが出来る。Cairoは[X Window Systemを必要としないので](../Page/X_Window_System.md "wikilink")、Popplerは[Microsoft Windowsや](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Mac OSのような](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")、[X.Org Serverがプレインストールされていないプラットフォーム上でも動かすことが出来る](../Page/X.Org_Server.md "wikilink")。
  - 注釈のサポート（予定）。PDFドキュメントに保存された注釈を扱うことが出来る。[live.gnome.org](http://live.gnome.org/Evince/Annotations)を参考のこと。
  - フォームの編集機能（プレビューリリースにて）。PDFのフォームに記入された情報をファイルに保存可能。

## 関連項目

  - [freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink")
  - [PDFソフトウェアの一覧](../Page/PDFソフトウェアの一覧.md "wikilink")
  - [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")

## 脚注

<references/>

## 外部リンク

  - [Popplerホームページ](http://poppler.freedesktop.org/)
  - [How to install Poppler on Windows](http://stackoverflow.com/questions/18381713/how-to-install-poppler-on-windows/) Windows版Popplerの入手方法- Stack Overflow
  - [Poppler --- PDF ビューア・操作ツール](http://texwiki.texjp.org/?Poppler) 日本語の情報 - TeX Wiki

[Category:PDFソフト](https://ja.wikipedia.org/wiki/Category:PDFソフト "wikilink") [Category:Freedesktop.org](https://ja.wikipedia.org/wiki/Category:Freedesktop.org "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.