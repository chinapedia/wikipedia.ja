> この記事は[OSDN](https://ja.wikipedia.org/wiki/OSDN)から翻訳されています。


**OSDN**（オーエスディーエヌ）は、日本の[オープンソース](../Page/オープンソース.md "wikilink")ソフトウェアプロジェクト向けのホスティングサイト。[SourceForge.net](../Page/SourceForge.net.md "wikilink")の姉妹サイトで、[OSDN社が運営している](https://ja.wikipedia.org/wiki/Open_Source_Development_Network "wikilink")。2015年5月11日にサイト名称が**SourceForge.JP**から変更された。\[1\]。 [Sfjp-char-lang-h250.png](https://ja.wikipedia.org/wiki/File:Sfjp-char-lang-h250.png "fig:Sfjp-char-lang-h250.png")

## 概要

[SourceForge.net](../Page/SourceForge.net.md "wikilink")の日本語版サイトとして、[VA Linux Systems JapanのOSDN事業部によって](https://ja.wikipedia.org/wiki/VA_Linux "wikilink")2002年に設立（2002年3月ベータ公開、2002年4月正式運用開始）。現在は2007年9月にVA LinuxからスピンオフしたOSDN株式会社によって運営されている。提供されているサービスはSourceForge.netとかぶる部分が多いが、コンパイルファームのようにOSDNにしかないサービスもある（詳細は[サービスの節を参照](https://ja.wikipedia.org/wiki/#サービス "wikilink")）。

OSDNではホスティング費用は発生しないが、オープンソースプロジェクトホスティングサイトなので、開発成果はオープンソースとして公開する必要がある。ライセンスは[OSIにオープンソースライセンスとして承認されているものが利用可能](../Page/Open_Source_Initiative.md "wikilink")。

企業によるオープンソース活動の拠点としても利用されており、登録開発者には個人のほか、それらの企業に所属する開発者も多い。

2016年10月3日からサイトドメインがosdn.jpからosdn.netへと変更された。他サイトの不祥事(SourceForge.net)が要因で海外オープンソースプロジェクトの登録が増加し、ダウンロードミラーサーバーが海外に設置されるなどしてjpドメインの実態がそぐわなくなってきたため\[2\]。

2017年4月現在の登録プロジェクト数は6,174、登録ユーザ数は53,997。

## サービス

OSDNで提供されている主なサービスは以下のとおり。

### CVS/SVN/Git/Mercurial/Bazaarリポジトリ

ソースコードをバージョン管理するためのリポジトリ。従来はバージョン管理システムとして[CVSだけが利用可能だったが](../Page/Concurrent_Versions_System.md "wikilink")、2007年3月から[Subversion](../Page/Apache_Subversion.md "wikilink") (SVN)、2008年11月から[Git](https://ja.wikipedia.org/wiki/Git "wikilink")、2009年10月から[Mercurial](../Page/Mercurial.md "wikilink")、2009年11月から[Bazaar](https://ja.wikipedia.org/wiki/Bazaar "wikilink")も利用可能になった。

### プロジェクトWiki

2007年に追加された[Wiki](https://ja.wikipedia.org/wiki/Wiki "wikilink")ツール。Trac、MoinMoin風の文法が使えるが、実装はOSDN独自のもの。ファイルリリースやトラッカーなどOSDNの他のツールの情報を埋め込むためのプラグインを備えている。

### プロジェクトWeb

ホスティングされているプロジェクトが自由に使えるWebスペース。CGI等も自由に設置できる。基本的にサイト名は「プロジェクト名.osdn.jp」となるが、独自ドメインを所持している場合はそれを割り当てることもできる。

### コンパイルファーム

ソフトウェアをビルドするためのサーバ群。SSHで接続して利用する。ちなみにSourceForge.netではコンパイルファームは提供されていない。2010年11月末でサービス終了。\[3\]以下のプラットフォームが利用可能。

| アーキテクチャ | OS                                                         |
| ------- | ---------------------------------------------------------- |
| x86     | [Debian GNU/Linux](../Page/Debian.md "wikilink")           |
| x86-64  | Debian GNU/Linux                                           |
| x86     | [NetBSD](../Page/NetBSD.md "wikilink")                     |
| PPC     | [Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") |

### シェルサーバ

[シェル](../Page/シェル.md "wikilink")の機能を利用するためのサーバ。主にプロジェクトWebのコンテンツ管理に用いる。

### トラッカー

バグ報告や機能の追加要望等を管理するためのツール。

### ML/フォーラム

開発者間、開発者/利用者間でコミュニケーションを取るためのメーリングリストとディスカッションフォーラム。

### ファイルリリース/ダウンロードミラー

ソフトウェアのパッケージ（バイナリパッケージやソースパッケージなど）を配布するためのツール。ファイルリリースに登録したパッケージは、ミラーサーバ群にもコピーされる。

## ホスティングされている主なプロジェクト

  - [akj eclipse rcp](https://osdn.net/projects/akjrcp/)：Eclipse RCPを利用したマルチメディアツール群
  - [All-In-One Project](https://osdn.net/projects/aioec/)：開発に便利なツールをまとめたインストーラ（All-In-One Eclipse、All-In-One Trac）
  - [Amateras](https://osdn.net/projects/amateras/)：Javaベースの開発ツール/ドキュメント
  - [Anthy](https://ja.wikipedia.org/wiki/Anthy "wikilink")：かな漢字変換エンジン
  - [BathyScaphe](https://ja.wikipedia.org/wiki/BathyScaphe "wikilink")：Mac OS X用の２ちゃんねるブラウザ
  - [Berry Linux](https://ja.wikipedia.org/wiki/Berry_Linux "wikilink")：マルチメディアに強いライブCD Linux
  - [blanco Framework](https://osdn.net/projects/blancofw/)：Excelブックの仕様書からソースを自動生成するツール
  - [Cabos](https://ja.wikipedia.org/wiki/Cabos "wikilink")：Javaで書かれたクロスプラットフォームのP2Pツール
  - [FFFTP](https://ja.wikipedia.org/wiki/FFFTP "wikilink")：Windows用2ペイン型FTPクライアントソフト
  - [GLOBALBASE PROJECT](https://osdn.net/projects/globalbase/)：完全自律分散型のGIS
  - [CotEditor](https://osdn.net/projects/coteditor/)：Mac OS X用のテキストエディタ
  - [Hinemos](https://ja.wikipedia.org/wiki/Hinemos "wikilink")：複数のコンピュータを単一のシステムイメージで運用管理
  - [M+ FONTS](https://ja.wikipedia.org/wiki/M+_FONTS "wikilink")：フリーな日本語フォント
  - [MergeDoc](https://osdn.net/projects/mergedoc/)：Eclipse用の日本語化関連ツール、プラグイン
  - [Mysaifu JVM](https://osdn.net/projects/mysaifujvm/)：Windows Mobileで動作するJVM（Java Virtual Machine）
  - [Network Kanji Filter](https://ja.wikipedia.org/wiki/Network_Kanji_Filter "wikilink") (nkf)：歴史の長い文字コード変換ツール
  - [NNsi](https://osdn.net/projects/nnsi/)：PalmOS用のWebクライアント集
  - [PukiWiki](https://ja.wikipedia.org/wiki/PukiWiki "wikilink")：PHPで動作するWikiツール
  - [Tera Term](https://ja.wikipedia.org/wiki/Tera_Term "wikilink")：Windows用の端末エミュレータ/SSHクライアント
  - [TOMOYO Linux](https://ja.wikipedia.org/wiki/TOMOYO_Linux "wikilink")：LinuxをセキュアOS化するソフトウェア
  - [ギコナビ](https://ja.wikipedia.org/wiki/ギコナビ "wikilink")：老舗のWindows用２ちゃんねるブラウザ
  - [さきゅばす](https://osdn.net/projects/saccubus/)：ニコニコ動画の動画をコメント付きで保存するツール
  - [シイラ](https://ja.wikipedia.org/wiki/シイラ_\(ウェブブラウザ\) "wikilink")：WebKitベースのMac OS X用Webブラウザ
  - [プロパティエディタ開発プロジェクト](https://osdn.net/projects/propedit/)：Unicode参照文字で書かれたプロパティファイルを直接編集
  - [風博士](https://ja.wikipedia.org/wiki/風博士_\(ウェブブラウザ\) "wikilink")：[肉の日](https://ja.wikipedia.org/wiki/肉の日 "wikilink")（毎月29日）リリースで有名なGeckoエンジンベースのWebブラウザ

## 注釈

<references/>

## 関連項目

  - [OSSホスティングサービスの比較](https://ja.wikipedia.org/wiki/OSSホスティングサービスの比較 "wikilink")

## 外部リンク

  -

  -

  - [OSDN株式会社](https://osdn.co.jp/)

[Category:技術のウェブサイト](https://ja.wikipedia.org/wiki/Category:技術のウェブサイト "wikilink") [Category:オープンソース文化・運動](https://ja.wikipedia.org/wiki/Category:オープンソース文化・運動 "wikilink") [Category:フリーソフトウェアのプロジェクト](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアのプロジェクト "wikilink") [Category:日本のLinux開発](https://ja.wikipedia.org/wiki/Category:日本のLinux開発 "wikilink") [Category:OSSホスティングサービス](https://ja.wikipedia.org/wiki/Category:OSSホスティングサービス "wikilink")

1.
2.  [OSDN、サイトドメイン変更のお知らせ](http://osdn.co.jp/press/2016/08/osdn.net)
3.