> この記事は[Ghostscript](https://ja.wikipedia.org/wiki/Ghostscript)から翻訳されています。


**Ghostscript**（ゴーストスクリプト）は、[PostScript](../Page/PostScript.md "wikilink") や [Portable Document Format](../Page/Portable_Document_Format.md "wikilink") (PDF) など[アドビシステムズ](../Page/アドビシステムズ.md "wikilink")の[ページ記述言語](../Page/ページ記述言語.md "wikilink")用の[インタプリタ](../Page/インタプリタ.md "wikilink")および、それを基にしたソフトウェアパッケージのことである。[デュアルライセンス](../Page/デュアルライセンス.md "wikilink")で配布されている。

## 特徴

Ghostscript は [ラスターイメージプロセッサ](../Page/ラスターイメージプロセッサ.md "wikilink") (RIP) として、PostScript ファイルを[ビットマップ画像に変換してプリンターに送る](https://ja.wikipedia.org/wiki/ラスター画像 "wikilink")。たとえば、UNIX における line printer daemon (lpd) の入力フィルタとして使われたり、PostScript や PDF ビューアなどに表示するラスター画像を裏で生成する RIP エンジンとしても使われる。

Ghostscript は PostScript → PDF 変換ソフトなどのファイルコンバータとしても使われる。これはよく仮想プリンタなどの PDF 作成ソフト中の PostScript プリンタドライバと組み合わされる。

[TeX](../Page/TeX.md "wikilink")におけるEPS→PDF変換用の画像処理エンジンとしても活用されている。論文執筆者にとっては欠かせないソフトウェアの1つである。

言語インタープリタの形式を採っているため、Ghostscript は一般用途向けプログラミング環境としても使われる。

Ghostscript は [Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")、[OpenVMS](../Page/OpenVMS.md "wikilink")、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink") そして [AmigaOS](../Page/AmigaOS.md "wikilink") など数多くの OS に移植された。Unix系OSではgsというコマンド名で起動するが、利用者が直接このコマンドを起動するよりも、後述のフロントエンドを介して利用される方が一般的である。

## フロントエンド

Ghostscript を使用するための複数の[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) が存在する。これらを使うことで文章の印刷はもちろんのこと、PostScript や PDF ファイルを画面上で見たり、スクロールしたり、前後のページへ移動したり、文章を拡大したりすることができる。

  - Ghostview
    Unix/X11 上で動作する。一般的ではない[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")の特徴を持つ：文章の上で[マウスを](../Page/マウス_\(コンピュータ\).md "wikilink")[ドラッグ](https://ja.wikipedia.org/wiki/ドラッグ "wikilink")すると逆の方向にスクロールする（ドラッグによってイメージそのものではなく、イメージを見る視点を移動させている）。その効果はイメージ全体に見えないスクロールバーがあるのに似ていて、[Google マップやその他のアプリケーションのやり方とはほとんど逆である](../Page/Google_マップ.md "wikilink")。
  - gv
    Unix/X11 上で動作する。Ghostview を視覚的に改良したバージョンで、振る舞いは Ghostview に似ている。
  - mgv
    Unix/X11 上で動作する。[Motif](../Page/Motif_\(GUI\).md "wikilink") を使用した Ghostscript の[フロントエンド](../Page/フロントエンド.md "wikilink")である。その特徴は規則正しいメニューやスクロールバーで実現された、より標準的なユーザーインターフェースにある。
  - Ghostgum GSview
    Microsoft Windows、OS/2 および UNIX 系 OS 上で動作する。Windows and OS/2 向けバージョンが最もよく知られている。UNIX 上では [GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink") toolkit を使用している。Aladdin Free Public License の下で配布されているが、ユーザーに GSview の開発を支援するための登録を促すウィンドウが起動時に表示される。登録料は 40 [AUドル](../Page/オーストラリア・ドル.md "wikilink") である。2013年1月現在、最新版は2012年 1月17日に公開された version 5.0\[1\]である。
  - Artifex GSView
    GSview version 6以降はArtifex Softwareによって開発されたものであり、Ghostgum Software Pty Ltd.のRussell Langによるそれより前のversionと混同してはならない\[2\]。2015年04月22日にversion 6.0 Betaが公開された。商用ライセンスの下でのみ利用可能である。
  - PDF Blender
    クロスプラットフォームなアプリケーションである。文章を PostScript と PDF で変換したり、マージしたりできる。
  - Moonshiner
    Ghostscript を使用して PostScript を PDF に変換するためのグラフィカルなフロントエンドである。Linux 上で [Adobe Acrobat](../Page/Adobe_Acrobat.md "wikilink") のそっくり製品になることを目指している。

## 歴史

Ghostscript は元は [1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")に [GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")のために L. Peter Deutsch によって書かれ、[GPL](../Page/GNU_General_Public_License.md "wikilink") の下でリリースされた。その後 Deutsch は Ghostscript を[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")としてライセンスするために Aladdin Enterprises を設立した。現在 Ghostscript は Artifex Software が所有しており、Artifex Software の従業員と世界中のユーザーコミュニティーが保守・管理している。Ghostscript の現行バージョンは [GPL](../Page/GNU_General_Public_License.md "wikilink") の下で再び利用可能になったが、金銭的利益を得るためのプロプライエタリなプロジェクトでの使用向けライセンスも存在する。

## Ghostscript の実装

  - GPL Ghostscript
    [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")・ライセンス である [GPL](../Page/GNU_General_Public_License.md "wikilink") の下で利用可能であり、公式の実装とされる。2006年6月より以前は、最先端の Ghostscript は **AFPL Ghostscript**（以前の名称は **Aladdin Ghostscript**）として [Aladdin Free Public License](https://ja.wikipedia.org/wiki/Aladdin_Free_Public_License "wikilink") の下で配布されていた。このライセンスは商用利用を制限していた。現在 AFPL Ghostscript は廃れてしまった\[3\]。
  - GNU Ghostscript
    [GNU プロジェクト](../Page/GNU.md "wikilink") の一部であり、現在は GPL Ghostscript から派生している。
  - ESP Ghostscript
    [Easy Software Products](https://ja.wikipedia.org/wiki/Easy_Software_Products "wikilink") によって GPL の下で配布されていた。GPL Ghostscript に基づいており、ESP の [Common Unix Printing System](../Page/Common_Unix_Printing_System.md "wikilink") との互換性を改良するためにいくつかの修正を加えたものである。GPL Ghostscript に統合されたため、[2007年](../Page/2007年.md "wikilink")[3月14日](https://ja.wikipedia.org/wiki/3月14日 "wikilink")にリリースされたバージョン 8.15.4 を最後に開発は終了した\[4\]。
  - Ghostscript
    Artifex Software のプロプライエタリな現行の商用バージョンであり、[クローズド・ソースな製品を含んでいる](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")。

GPL Ghostscript は、[Display PostScript](../Page/Display_PostScript.md "wikilink") を完全にサポートするのに必要な機能を持つ **Display Ghostscript** のバックエンドとしても使われている。

## 関連項目

  - [Common Unix Printing System](../Page/Common_Unix_Printing_System.md "wikilink") (CUPS)
  - [PostScript Printer Description](../Page/PostScript_Printer_Description.md "wikilink") (PPD)
  - [en:Printer driver](https://ja.wikipedia.org/wiki/:en:Printer_driver "wikilink")
  - [en:Foomatic](https://ja.wikipedia.org/wiki/:en:Foomatic "wikilink")
  - [en:Pstoedit](https://ja.wikipedia.org/wiki/:en:Pstoedit "wikilink")

## 脚注

## 外部リンク

  - [Ghostscript コミュニティーサイト、メーリングリスト, Bugzilla, CVS](https://www.ghostscript.com/)
  - [Ghostscript ライセンスと商用サポート](https://www.artifex.com/)
  - [SourceForge の Ghostscript ファイル](https://sourceforge.net/projects/ghostscript/files/)
  - [SourceForge の Ghostscript フォント](https://sourceforge.net/projects/gs-fonts/files/)
  - [GNU Ghostscript](http://www.gnu.org/software/ghostscript/ghostscript.html)
  - [1998 Interview with L. Peter Deutsch on history of Ghostscript project](http://devlinux.org/deutsch-interview.html) - インタビュー記事
  - [Ghostscript, Ghostview と GSview のダウンロード](http://pages.cs.wisc.edu/~ghost/)
  - [GNU gv](http://www.gnu.org/software/gv/)
  - [PDF Blender Home Page](http://www.spaceblue.com/products/pdfblender/)
  - [DOS 向け Ghostscript](http://www.fracassi.net/iw2evk/)
  - [RGhost](http://rghost.rubyforge.org/) - Ruby と Ghostscript を使って文書を生成するプロジェクト。32 種のバーコードをサポートする。
  - [Moonshiner Homepage](http://moonshiner.sourceforge.net/)

[Category:DTP](https://ja.wikipedia.org/wiki/Category:DTP "wikilink") [Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink") [Category:PDFソフト](https://ja.wikipedia.org/wiki/Category:PDFソフト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.  [Ghostscript: GSView](https://www.gsview.com/) - Artifex Software, Inc.
3.  [Advogato: Blog for raph](https://web.archive.org/web/20170629021353/http:/www.advogato.org/person/raph/diary.html?start=411)
4.  [Article \#484: The Grand Unified Ghostscript Officially Released: GPL Ghostscript 8.60 - Common UNIX Printing System](http://www.cups.org/articles.php?L484)