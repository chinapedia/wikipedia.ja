> この記事は[Mercurial](https://ja.wikipedia.org/wiki/Mercurial)から翻訳されています。


**Mercurial** (マーキュリアル) は、ソフトウェア開発者向けの分散型[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")である。[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[FreeBSD](../Page/FreeBSD.md "wikilink")、[MacOS](../Page/MacOS.md "wikilink")、[Linux](../Page/Linux.md "wikilink")等の [Unix 系システムでサポートされている](../Page/Unix系.md "wikilink")。GPL v2+ \[1\] の条件の下で[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")としてリリースされている。

Mercurial はシンプルな概念の下、次のものを主要な設計目標としている。

1.  分散型 VCS
2.  完全分散型の共同開発
3.  高いパフォーマンス
4.  [スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")
5.  [プレーンテキスト](../Page/プレーンテキスト.md "wikilink")ファイルと[バイナリ](../Page/バイナリ.md "wikilink")ファイル両方に対する堅牢な処理
6.  高度な分岐
7.  マージ機能

Mercurial は主としてコマンドライン駆動のプログラムである。Mercurial のすべての操作は、そのドライバープログラム hg への引数として呼び出される。(hg というプログラム名は、 が[水銀](../Page/水銀.md "wikilink")を意味しその[元素記号](../Page/元素記号.md "wikilink")が  であることに由来する。)

その一方で、Mercurial には、統合された Web インターフェイスが含まれており、[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")の拡張機能が利用できる。 [TortoiseHg](../Page/TortoiseHg.md "wikilink") およびいくつかの [IDE](https://ja.wikipedia.org/wiki/IDE "wikilink") では、Mercurial によるバージョン管理のサポートを提供する。また他のバージョン管理システム、特に [Apache Subversion](../Page/Apache_Subversion.md "wikilink") のユーザの移行を容易にする手段も講じている。

Mercurial は主に [Python](../Page/Python.md "wikilink") で実装されている。[バイナリ](../Page/バイナリ.md "wikilink") [Diff](../Page/Diff.md "wikilink") 実装は [C 言語で記述されていた](../Page/C言語.md "wikilink")。現在は[Rustを用いた](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink") chg (差分取得。[C言語](../Page/C言語.md "wikilink") からの置換え)、hgcli (クライアント用コマンドツール)、hg-core (コアモジュール) の実装が進められている。\[2\]\[3\]

Matt Mackall は、Mercurial の創始者であり、2016年後半までリード開発者を務めた。

## 歴史

[2005年](../Page/2005年.md "wikilink")[4月](https://ja.wikipedia.org/wiki/4月 "wikilink")上旬、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")の開発に利用されていた[BitKeeper](../Page/BitKeeper.md "wikilink")のフリー版の配布停止が発表された（詳細については[BitKeeper\#価格変更](https://ja.wikipedia.org/wiki/BitKeeper#価格変更 "wikilink")参照）。Linuxカーネル開発者の一人でもあったMatt Mackall は[BitKeeper](../Page/BitKeeper.md "wikilink")に代わる分散型[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")の開発に乗り出し、[4月19日](../Page/4月19日.md "wikilink")に0.1をリリースした。\[4\] 既に[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")の原著作者である[Linus Torvaldsも同様の目的で](../Page/リーナス・トーバルズ.md "wikilink")[Git](../Page/Git.md "wikilink")の開発を開始していたが、Mackall はLinux kernel Mailing List上でMercurial の優位性(データを差分の形式で保持することにより、リポジトリのサイズを節約している等)を訴え、Torvalds と論争を繰り広げたこともあった。[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")プロジェクトはMercurial ではなくGitを使用することを決定したが、現在、Mercurial は他の多くのプロジェクトで使用されている。「Git vs. Mercurial」は[ハッカー文化](../Page/ハッカー文化.md "wikilink")の聖戦の1つになった。

Mercurial メーリングリストの回答で、Mackall は「Mercurial」という名前がどのように選ばれたか説明した。

> 最初のリリースの少し前に、Larry McVoy を(「気まぐれ」の意味で)水銀性であると説明しています。進行中の[BitKeeper](../Page/BitKeeper.md "wikilink")の失敗に関する記事を読みました。複数の意味、便利な略語、および既存の命名スキーム(私の電子メールアドレスを参照)との適合性を考えると、すぐにクリックしました。したがって、Mercurial はLarry の名誉にちなんで名付けられました。同じことが[Git](../Page/Git.md "wikilink")にも当てはまるかどうかはわかりません\[5\]\[6\]。

## 設計

設計目標は、

  - 高い性能と[スケーラビリティ](https://ja.wikipedia.org/wiki/スケーラビリティ "wikilink")
  - サーバが不要な、完全に分散した共同開発環境
  - [テキストファイル](../Page/テキストファイル.md "wikilink")と[バイナリファイル](https://ja.wikipedia.org/wiki/バイナリファイル "wikilink")の両方を効率よく扱うこと
  - 概念上はシンプルなままで、高度なブランチ機能とマージ機能を持つこと

である。またMercurialは完全なWebインターフェースを含んでいる。 原著作者はMatt Mackall で、現在も主要開発者である。

Mercurial は[SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink")ハッシュを使用してリビジョンを識別する。ネットワークを介した[リポジトリ](../Page/リポジトリ.md "wikilink")へのアクセスでは、Mercurial は[Hypertext Transfer Protocolベースの](../Page/Hypertext_Transfer_Protocol.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")を使用して、往復要求、新しい接続、および転送されるデータを削減しようとします。 Mercurial は、プロトコルが[Hypertext Transfer Protocolベースの](../Page/Hypertext_Transfer_Protocol.md "wikilink")[プロトコル](../Page/プロトコル.md "wikilink")に非常に似ている[SSH](https://ja.wikipedia.org/wiki/SSH "wikilink")でも機能する。デフォルトでは、外部マージツールを呼び出す前に[マージ (バージョン管理システム)を使用する](https://ja.wikipedia.org/wiki/マージ_\(バージョン管理システム\)#3ウェイマージ "wikilink")。

## 主な機能

0.9.5版から、他の[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")で管理された[ソースコード](../Page/ソースコード.md "wikilink")を、取り込む機能がサポートされている。\[7\]

## 採用事例

Mercurial は[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")ソースの管理に選択されていないが、[Facebook](../Page/Facebook.md "wikilink")\[8\]、[World Wide Web Consortium](../Page/World_Wide_Web_Consortium.md "wikilink")、[Mozilla](../Page/Mozilla.md "wikilink")を含むいくつかの組織に採用されている。[Facebook](../Page/Facebook.md "wikilink")は[Rustを使用してMononoke](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")\[9\]\[10\]を作成している。これは、大規模なマルチプロジェクト[リポジトリ](../Page/リポジトリ.md "wikilink")をサポートするために特別に設計されたMercurial サーバである。

[2013年](../Page/2013年.md "wikilink")、[Facebook](../Page/Facebook.md "wikilink")はMercurial を採用し、大規模な統合コード[リポジトリ](../Page/リポジトリ.md "wikilink")を処理するためのスケーリングに取り組み始めた\[11\]。

[Bitbucket](https://ja.wikipedia.org/wiki/Bitbucket "wikilink")は、Webベースのバージョン管理サービスが[2020年](../Page/2020年.md "wikilink")6月にMercurial のサポートを終了すると発表し、新しいプロジェクトの1％のみがそれを使用していると説明した\[12\]。

## Mercurial サーバと[リポジトリ](../Page/リポジトリ.md "wikilink")管理

  - RhodeCode Inc. によるRhodeCode
  - Kallithea(RhodeCodeの[GPLv3](https://ja.wikipedia.org/wiki/GPLv3 "wikilink")[フォーク](../Page/フォーク.md "wikilink"))
  - Fog Creek Software によるKiln
  - Phacility による[Phabricator](https://ja.wikipedia.org/wiki/Phabricator "wikilink")

### [ソースコードホスティング](https://ja.wikipedia.org/wiki/ソースコードホスティング "wikilink")

参照: [OSSホスティングサービスの比較](https://ja.wikipedia.org/wiki/OSSホスティングサービスの比較 "wikilink")、[分散バージョン管理Git/Mercurial/Bazaar徹底比較](https://www.atmarkit.co.jp/ait/articles/0901/14/news133.html)

以下の[ウェブサイト](../Page/ウェブサイト.md "wikilink")は、Mercurial [リポジトリ](../Page/リポジトリ.md "wikilink")の無料の[ソースコードホスティング](https://ja.wikipedia.org/wiki/ソースコードホスティング "wikilink")を提供している。

  - [アトラシアン](https://ja.wikipedia.org/wiki/アトラシアン "wikilink")による[Bitbucket](https://ja.wikipedia.org/wiki/Bitbucket "wikilink")(2020年2月から非推奨、2020年6月1日から廃止されるMercurial [リポジトリ](../Page/リポジトリ.md "wikilink")のサポート)
  - [SourceForge.net](../Page/SourceForge.net.md "wikilink")
  - [フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")による[Savannah](https://ja.wikipedia.org/wiki/Savannah "wikilink")
  - Puszcza\[13\]([Savannah](https://ja.wikipedia.org/wiki/Savannah "wikilink")姉妹サイト、ウクライナでホスト)
  - [OSDN](../Page/OSDN.md "wikilink")\[14\]
  - Perforce\[15\]
  - Mozdev
  - TuxFamily\[16\]
  - FusionForge
  - その他\[17\]

### Mercurial を使用した[オープンソース](../Page/オープンソース.md "wikilink")プロジェクト

Mercurial 分散RCSを使用するいくつかのプロジェクト\[18\]

  - [Adium](https://ja.wikipedia.org/wiki/Adium "wikilink")
  - [GNU Health](https://ja.wikipedia.org/wiki/GNU_Health "wikilink")
  - [GNU Multi-Precision Library](https://ja.wikipedia.org/wiki/GNU_Multi-Precision_Library "wikilink")
  - [GNU Octave](../Page/GNU_Octave.md "wikilink")
  - [IcedTea](https://ja.wikipedia.org/wiki/IcedTea "wikilink")
  - [LEMON](https://ja.wikipedia.org/wiki/LEMON_\(C++_library\) "wikilink")
  - [LiquidFeedback](https://ja.wikipedia.org/wiki/LiquidFeedback "wikilink")
  - [Mozilla](../Page/Mozilla.md "wikilink")\[19\]
  - [Nginx](https://ja.wikipedia.org/wiki/Nginx "wikilink")
  - [OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")\[20\]
  - [Orthanc](https://ja.wikipedia.org/wiki/Orthanc_\(software\) "wikilink")
  - [Pidgin](https://ja.wikipedia.org/wiki/Pidgin_\(software\) "wikilink")
  - [RhodeCode](https://ja.wikipedia.org/wiki/RhodeCode "wikilink")
  - [Roundup](https://ja.wikipedia.org/wiki/Roundup_\(issue_tracker\) "wikilink")
  - [SDL](https://ja.wikipedia.org/wiki/Simple_DirectMedia_Layer "wikilink")
  - [Tryton](https://ja.wikipedia.org/wiki/Tryton "wikilink")
  - [WinDirStat](https://ja.wikipedia.org/wiki/WinDirStat "wikilink")
  - [wmii](https://ja.wikipedia.org/wiki/wmii "wikilink")
  - [XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")
  - [Xine](../Page/Xine.md "wikilink")

## 脚注

## 外部リンク

  -
  - [Official Mercurial Project Wiki](https://www.mercurial-scm.org/wiki/)

  - [Mercurial 日本語チュートリアル](https://www.mercurial-scm.org/wiki/JapaneseTutorial)

  - [分散バージョン管理Git/Mercurial/Bazaar徹底比較](https://www.atmarkit.co.jp/ait/articles/0901/14/news133.html)

  - [Mercurialではじめる分散構成管理](https://gihyo.jp/dev/feature/01/mercurial)

  - [Mercurial の利用](http://www.lares.dti.ne.jp/~foozy/fujiguruma/scm/mercurial.html)

  - [Mercurialでバージョン管理](http://www.02.246.ne.jp/~torutk/mercurial/intro.html)

[Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink") [Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:2005年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2005年のソフトウェア "wikilink")

1.  .
2.
3.
4.
5.
6.  Torvalds has said: *"I'm an egotistical bastard, so I name all my projects after myself. First Linux, now git."*
7.  <http://www.selenic.com/mercurial/wiki/index.cgi/ConvertExtension>
8.
9.
10.
11.
12.
13.
14.
15.
16.
17. .
18. .
19.
20.