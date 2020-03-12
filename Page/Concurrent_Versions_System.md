> この記事は[Concurrent Versions System](https://ja.wikipedia.org/wiki/Concurrent_Versions_System)から翻訳されています。


**Concurrent Versions System**（コンカレント・バージョンズ・システム、並行バージョンシステム）は、通常**CVS**（シーブイエス）と略される、[テキストファイル](../Page/テキストファイル.md "wikilink")の変更を記録し管理する[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。

## 概要

主に[ソフトウェア](../Page/ソフトウェア.md "wikilink")の開発における[ソースコード](../Page/ソースコード.md "wikilink")を始めとしたテキストファイルの共有（保存、取出し）に使われる。テキストファイルの枝分かれした版を管理することができる。

枝分かれ（並行ヴァージョン）の機能を使わなくても、ファイルの直線的な追加改変を追いかけるのに使うことができる。特にダウンロードをする場合、サーバ上のファイルと自分の持っているファイルの差分を転送するだけで最新版を手にいれることができるので、開発途中のプログラムの配布にも使われる。

通常、CVSサーバを用意してファイルの共有をする。CVSサーバにアクセスするCVSクライアント・プログラムは、コマンドラインの`cvs`を始め、[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")によるラッパーや、[統合開発環境](../Page/統合開発環境.md "wikilink")向けの[プラグイン](../Page/プラグイン.md "wikilink")が多数作られている。

CVSは、ネットワークでの使用を考慮した最初のソースコード管理システムであって、[フリーウェア](../Page/フリーウェア.md "wikilink")だったので、1990年代を通じて広く利用された。しかし、後述するような欠陥が明らかになるにつれ、これらの問題を改善した、[Subversion](../Page/Apache_Subversion.md "wikilink")、[Perforce](../Page/Perforce.md "wikilink")、[Git](../Page/Git.md "wikilink") などの新しいツールに取って代わられた。

## RCSとの比較

CVSは元々、単一のファイルを対象としたバージョン管理ツールである[RCSの上に作られていたが](../Page/Revision_Control_System.md "wikilink")、現在は依存はなくなった（リポジトリ内のデータ保持は依然として RCSのそれである）。$Id:$などのキーワードは、その名残である。更にRCSは、diffなどのUNIX系のテキスト処理プログラムの上に作られている。

RCSは、マルチユーザーシステム（1台のコンピュータに、複数のダム端末が接続され、[CPU](../Page/CPU.md "wikilink")や[ファイルシステム](../Page/ファイルシステム.md "wikilink")が共有されている）の上で、同じファイル/フォルダを共有した状態で使われたのに比べ、CVSではCVSサーバとして別のコンピュータ上に用意することもできる。

同一ファイルを複数人で同時編集した場合のコンフリクトに対するアプローチも異なる。RCSはファイルをロックする事で同時編集を禁止する。対するCVSでは、RCSのような強固なロックメカニズムは、もたない。すなわち、同時編集を許可する代りにコンフリクトが生じた場合、コミット時にマージ操作が必要とされる。

## 欠点

  - ファイル名の変更削除、ディレクトリ名の変更削除をうまく扱えない。
  - 異なる文字コード（JIS/SJIS/EUC）に対するサポートがない。
  - 基本的に個々のファイルの履歴はわかるが、リポジトリの履歴は簡単には知ることができない。
  - バイナリーファイルの扱いが下手で、リポジトリサイズの増大につながる。
  - 分散リポジトリをサポートしない。
  - アトミック・コミットをサポートしない。複数のファイルを同時にコミットした場合、CVSではそれぞれのファイルを（ごく短時間の間に）一つずつコミットしたものとして扱うため、[アトミック性を満たすことができない](../Page/不可分操作.md "wikilink")。

等の点が挙げられる。

## クライアント

  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") - [WinCvs](http://cvsgui.sourceforge.net/), [TortoiseCVS](https://ja.wikipedia.org/wiki/TortoiseCVS "wikilink")（エクスプローラ拡張）
  - [Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink"), [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") - [MacCvs](http://cvsgui.sourceforge.net/)
  - [GNOME](../Page/GNOME.md "wikilink") - [gCvs](http://cvsgui.sourceforge.net/)
  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") - クライアント機能が内蔵されている。
  - [KDE](../Page/KDE.md "wikilink") - GUI[フロントエンド](../Page/フロントエンド.md "wikilink")として[Cervisia](https://ja.wikipedia.org/wiki/Cervisia "wikilink")が公開されている。

## その他のツール

  - [ViewVC（ViewCVS）](http://www.viewvc.org/) - CVSおよびSubversionリポジトリをブラウザ上で閲覧するためのツール。[SourceForge.net](../Page/SourceForge.net.md "wikilink")によって採用される。
  - [Bonsai](http://www.mozilla-japan.org/projects/bonsai/) - [Mozilla](../Page/Mozilla.md "wikilink")によって開発されたCVSリポジトリをブラウザ上で管理するためのツール。
  - [OpenGrok](http://opengrok.github.io/OpenGrok/) - ソースコードをブラウザ上で検索・参照するためのツール。CVSやSubversion, Git, Mercurial, Bazaarなど多数のバージョン管理システムをサポート。Javaで書かれている。
  - [StatCVS](http://statcvs.sourceforge.net/) - CVSリポジトリから情報を取得して、表やグラフを用いたグラフィカルなレポートを作成するJavaで書かれたツール。

## 関連項目

  - [バージョン管理システム](../Page/バージョン管理システム.md "wikilink")
  - [Git](../Page/Git.md "wikilink")
  - [Apache Subversion](../Page/Apache_Subversion.md "wikilink")（SVN）
  - [patch](https://ja.wikipedia.org/wiki/patch "wikilink")
  - [UNIX](../Page/UNIX.md "wikilink")、[Linux](../Page/Linux.md "wikilink")

## 外部リンク

  -
  - [CVS manual の日本語訳](http://www.sodan.org/~penny/vc/)

  - [The CVS Book 日本語訳](http://jtdan.com/vcs/kahori.com/j-cvsbook/)

  - [バージョン管理システム CVS を使う](https://vox.nishimotz.com/cvs/cvs.html)

  - [バージョン管理システム CVS](http://oku.edu.mie-u.ac.jp/~okumura/networking/cvs.html)

[Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1990年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1990年のソフトウェア "wikilink")