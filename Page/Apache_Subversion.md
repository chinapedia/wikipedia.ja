> この記事は[Apache Subversion](https://ja.wikipedia.org/wiki/Apache_Subversion)から翻訳されています。


**Apache Subversion**（アパッチ・サブバージョン; SVN）はプログラムのソースコードなどを管理する集中型[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")の一つ。元々は、[CollabNet](https://ja.wikipedia.org/wiki/CollabNet "wikilink")が開発していたが、[2009年](../Page/2009年.md "wikilink")[11月7日](../Page/11月7日.md "wikilink")にApache Incubatorプロジェクトのひとつとなり、[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[2月17日](../Page/2月17日.md "wikilink")より[Apacheのトッププロジェクトとなった](../Page/Apacheソフトウェア財団.md "wikilink")。ライセンスは[Apache Licenseに準じたものとなっている](https://ja.wikipedia.org/wiki/Apache_License "wikilink")。

## 概要

歴史的には広く使われているバージョン管理システムの一つに[CVSがあった](../Page/Concurrent_Versions_System.md "wikilink")。CVSには[ディレクトリ](../Page/ディレクトリ.md "wikilink")の移動の管理やネットワーク対応の点、不可分な更新などの点で難があった。これらCVSの問題点を解決すべく開発されたのがSubversionである。

Subversionは集中型（クライアント・サーバ型）であるが、その後、[Git](../Page/Git.md "wikilink")や[Mercurial](../Page/Mercurial.md "wikilink")や[Bazaar](https://ja.wikipedia.org/wiki/Bazaar "wikilink")などの分散型のバージョン管理システムが登場するようになった。例えば、[Linux](../Page/Linux.md "wikilink")カーネルの管理にはGit、[Mozilla Firefoxの管理にはMercurial](../Page/Mozilla_Firefox.md "wikilink")、[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")の管理にはBazaarが使われている。

## 特徴

Subversionの使い方は[CVSによく似ている](../Page/Concurrent_Versions_System.md "wikilink")。コマンドラインで使用する際の主要なコマンド名はCVSと一致するように作られているため、クライアントはCVSからの移行がきわめて容易である。

1.  ディレクトリの移動や削除をサポートしている。このため、ファイル名やソースツリーの構造がはっきりと決まらないうちからバージョン管理をすることができる。
2.  バージョン番号（リビジョン番号）はソースツリー全体に対して振られるため、原則としては誰かがソースツリーのどこかのファイルを更新する度に番号が増えてゆく。（CVSではファイル毎にリビジョン番号がつけられている。）
3.  作業ディレクトリ内に、最後にソースリポジトリと同期をとったときのファイルのコピーを持っているため、改編中のファイルの変更部の確認などがソースリポジトリにアクセスする事無く高速に実行できる。また、ファイルの差分送信が効率よく行なわれるため、プアなネットワーク環境で利用したときに快適である。
4.  [SSHによるソースリポジトリとの通信を標準でサポートしている](../Page/Secure_Shell.md "wikilink")。インターネット経由で利用してもセキュリティを容易に保つ事ができる。
5.  [WebDAV](../Page/WebDAV.md "wikilink")をバックエンドとして使うことができる。つまり、[Apache HTTP ServerなどのWebDAVをサポートするHTTPサーバを経由して](../Page/Apache_HTTP_Server.md "wikilink")、WebDAVプロトコルを用いてSubversionサーバとSubversionクライアントが通信するという形態が使える。

一方で CVS における module, branch, tag といった概念が Subversion では全てサブディレクトリとして設計されているので、これらの扱いは CVS とはまったく違う考え方を要する。

1.  CVS では <モジュール名>/<サブディレクトリ名>/.../<ファイル名> だが、Subversion では <サブディレクトリ名>/.../<ファイル名> となる。下記の2つのコマンドはほぼ同等の処理を行う。
      - cvs -d:some_repository checkout -d aSubdir aModule/aDir/aSubdir
      - svn co some_repository/aModuleDir/aDir/aSubdir
2.  CVS では tag や branch が各ファイル毎に管理されるが、Subversion では「別ディレクトリ/ファイルへのコピー」で管理される。
      - cvs tag aTagName aSubdir
      - svn copy aSubdir aSubdir_aTagName
3.  CVS の merge はタグ名が使えるのに対し、Subversion の merge はリビジョン番号や日付などで指定する。
4.  Subversion の svn コマンドは同じ表記でリポジトリの直接操作とローカルマシンのワーキングコピーの操作を実現するので注意を要する。
      - svn copy aSubdir anotherDir はワーキングコピーでの操作で, 次に svn commit を実行することでリポジトリに反映される。
      - svn copy some_repository/.../aSubdir some_repository/.../anotherDir では直接リポジトリが変更される。

### 一般的なリポジトリ構成

一般に Subversion ではリポジトリの構成を以下のようにするのがよい、と提案されている。

  - <project>/trunk/<subdir>/...
  - <project>/branches/<branch>/<subdir>/...
  - <project>/tags/<tag>/<subdir>/...

この場合 branch/tag を作成するのは以下のように、コピーするだけでよい。

`svn copy some_repository/aProject/trunk some_repository/aProject/branches/aBranchName`

## クライアント

[クライアントとしては](../Page/クライアント_\(コンピュータ\).md "wikilink")、[コマンドライン](https://ja.wikipedia.org/wiki/コマンドライン "wikilink")ツールの`svn`の他、以下のものがある。

  - [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") - [TortoiseSVN](https://ja.wikipedia.org/wiki/TortoiseSVN "wikilink")(エクスプローラ拡張)
  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") - [SvnX](http://www.lachoseinteractive.net/en/community/subversion/svnx/), [Versions](http://www.versionsapp.com/) なお、LeopardからSubversionは標準インストールされており、Subversionサーバも自動起動している。
  - [Linux](../Page/Linux.md "wikilink") - [RabbitVCS](http://rabbitvcs.org/)
  - [KDE](../Page/KDE.md "wikilink") - [KDESvn](https://ja.wikipedia.org/wiki/KDESvn "wikilink"), [KSvn](http://web.archive.org/web/20070928103218/http://apps.intra-links.com/)
  - [GNOME](../Page/GNOME.md "wikilink")
  - クロスプラットフォーム - [RapidSVN](http://www.rapidsvn.org/), [pysvn WorkBench](http://pysvn.tigris.org/), [eSvn](http://zoneit.free.fr/esvn/), [SmartSVN](http://www.syntevo.com/smartsvn/), [QSvn](http://anrichter.github.io/qsvn/)
  - Webアプリ - [FlexySvn](http://web.archive.org/web/20110101182059/http://www.subversionary.org/node/48), [Trac](../Page/Trac.md "wikilink"), [ViewVC](http://www.viewvc.org/)
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") - [SVNKit](http://svnkit.com/), [NetBeans](../Page/NetBeans.md "wikilink"), [sventon](http://www.sventon.org/)
  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") - [Subclipse](http://subclipse.tigris.org/), [Subversive](http://eclipse.org/subversive/)
  - [Visual Studio](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink") - [AnkhSVN](http://ankhsvn.net/), [VisualSVN](http://www.visualsvn.com/)
  - [IntelliJ IDEA](https://ja.wikipedia.org/wiki/IntelliJ_IDEA "wikilink") - 標準搭載されている。もしくは、[TMate](http://tmatesoft.com/)
  - [Dreamweaver](https://ja.wikipedia.org/wiki/Dreamweaver "wikilink") - 標準搭載されている。もしくは、[SubWeaver](http://sourceforge.net/projects/subweaver/)
  - [Code::Blocks](../Page/Code::Blocks.md "wikilink")
  - [Xcode](../Page/Xcode.md "wikilink") - 2011年3月にリリースされたXcode4より、gitとSubversionが、標準でサポートされた。

## 使用例

コマンドラインから使うクライアント`svn`の使用例

インポート

`$ svn import project_name svn+ssh://dev.example.com/repos/svn/trunk`

チェックアウト

`$ svn checkout http://svn.collab.net/repos/svn/trunk`

作業コピーの更新

`$ svn update`

作業コピーの状態の表示

`$ svn status`

変更点の差分を表示

`$ svn diff`

ファイル README への変更を破棄して元に戻す

`$ svn revert README`

foo を bar に移動

`$ svn move foo bar`

コミット

`$ svn commit`

## 関連項目

  - [CVS](../Page/Concurrent_Versions_System.md "wikilink")
  - [arch](https://ja.wikipedia.org/wiki/arch "wikilink")
  - [バージョン管理システム](../Page/バージョン管理システム.md "wikilink")
  - [TortoiseSVN](https://ja.wikipedia.org/wiki/TortoiseSVN "wikilink")
  - [Subversion クライアントの比較](https://ja.wikipedia.org/wiki/:en:Comparison_of_Subversion_clients "wikilink") (英語版ウィキペディア)

## 外部リンク

  -
  - [Subversionによるバージョン管理](http://svnbook.red-bean.com/) - [O'Reilly Mediaの本](../Page/オライリーメディア.md "wikilink")「Version Control with Subversion（svnbook）」をオンラインで読める公式ウェブサイト

  - [Subversionドキュメントのまとめ](http://jtdan.com/vcs/svn/) - 「Subversionによるバージョン管理」の日本語訳（HTML/PDF/HTML Help形式）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:バージョン管理システム](https://ja.wikipedia.org/wiki/Category:バージョン管理システム "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:協働](https://ja.wikipedia.org/wiki/Category:協働 "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")