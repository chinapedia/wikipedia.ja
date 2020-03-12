> この記事は[Hyper Estraier](https://ja.wikipedia.org/wiki/Hyper_Estraier)から翻訳されています。


**Hyper Estraier**（はいぱー・えすとれいや）は、[日本](https://ja.wikipedia.org/wiki/日本 "wikilink")で開発された[全文検索エンジン](https://ja.wikipedia.org/wiki/全文検索エンジン "wikilink")の[ライブラリ](../Page/ライブラリ.md "wikilink")である。ライセンスは[LGPL](https://ja.wikipedia.org/wiki/LGPL "wikilink")で提供されている。

## 概要

[N-gram法を拡張したインデックス方式である](https://ja.wikipedia.org/wiki/全文検索#N-Gram "wikilink")[N.M-gram](https://ja.wikipedia.org/wiki/N.M-gram "wikilink")法を採用し、どの言語でも洩れの無い[検索](../Page/検索.md "wikilink")が可能になっている。また、[MeCab](../Page/MeCab.md "wikilink")を用いて[形態素解析](../Page/形態素解析.md "wikilink")の結果を用いた処理を行うことが出来る。作者は[平林幹雄](https://ja.wikipedia.org/wiki/平林幹雄 "wikilink")。

バックエンドには、同じ作者による[QDBM](https://ja.wikipedia.org/wiki/QDBM "wikilink")を採用、データベースに対するgathererとsearcher、独自のテキスト分析システムで構成される。

文書が持つ複数の属性をインデックスに保存することができる。属性を用いた検索と、全文検索を併用することができる、実用的な全文検索エンジンである。類似文章検索の機能もある。

  - Hyper EstraierのAPIを利用したコマンド群
  - Webブラウザを通じて検索を行うためのCGI
  - 複数台のサーバーのP2Pによる分散処理機能。これにより1000万件以上の超大規模インデックスに対応。
  - ウェブクローラー。類似度優先による巡回機能がある。

などが同梱されている。

同作者による[Estraier](https://ja.wikipedia.org/wiki/Estraier "wikilink")という全文検索エンジンが存在する。Estraierは形態素解析（[わかち書き](../Page/わかち書き.md "wikilink")）に基づいたインデックスを採用している。Hyper EstraierはEstraierを開発した経験に基づいて、新しく開発された全文検索エンジンである。また、Estraierの前は、Snatcherという名称で作成していた。

## N.M-gram法

[N.M-gram](https://ja.wikipedia.org/wiki/N.M-gram "wikilink")法とは、[N-gram法を拡張したインデックスのデータ構造である](https://ja.wikipedia.org/wiki/全文検索#N-Gram "wikilink")。長さNの文字列と、それに後続する長さMの文字列をキーとしたハッシュ値とがペアとして[転置インデックス](../Page/転置インデックス.md "wikilink")に保存される。

[N.M-gram](https://ja.wikipedia.org/wiki/N.M-gram "wikilink")法を採用することにより、トークンの出現位置情報を持つことなしに、N文字を超える長さの文字列を検索することができる。

Hyper Estraierでは、N=2, M=2でインデックスが作成される。これを2.2-gram法と呼ぶ。

## コマンドツール

estcmdというコマンドラインツールが付属する。estcmdにサブコマンドをあたえることで、インデックスの作成・更新・検索などの操作を行うことができる。主なコマンドを挙げる。

  - create
    インデックスを作成する。その際に新しい属性などを付加することができる。
  - edit
    属性の更新を行う。
  - list
    インデックスにある文書のリストを作成する。
  - gather
    既にあるインデックスに新しいデータを追加する。
  - search
    指定されたインデックスから、検索をおこなう。この際、出力形式などを指定することができる。

### フィルタ

フィルタと呼ばれるテキスト抽出プログラムを利用することにより、プレインテキスト以外のフォーマットで記録されたファイルをインデックスすることができる。現在、公式では[MS Officeや](https://ja.wikipedia.org/wiki/MS_Office "wikilink")[PDFなどのフィルタを配布している](../Page/Portable_Document_Format.md "wikilink")。

## P2P機能

インデックスを分散して配置することによって、大規模な検索システムを構築することが可能になる。

[P2P](https://ja.wikipedia.org/wiki/P2P "wikilink")の機能を利用する際には、ノードマスタと呼ばれる統括的なプロセスを利用し、そのプロセスが個別のノードサーバーを管理する。アプリケーションは、ノードサーバーと連携し、そのノードサーバーが個別に個々のサーバーと連携することによって、それほど難易度の無いP2P方式での検索が可能になっている。また、このノードサーバーの連携の際に「信頼度」を設定することが出来、これにより、より精度の高い検索が可能になっている。

ノード間の通信プロトコルは[HTTPである](../Page/Hypertext_Transfer_Protocol.md "wikilink")。

## クローラ

Hyper Estraierには、各コマンドのほかに、estwaverと呼ばれるウェブのクローラが付属している。このクローラを使うことで、他サーバーで公開されている情報に対するインデックスを作成することができる。

## プログラミングとバインディング

Hyper Estraierには、CによるAPIを経由して操作することができる。主として、文書の属性を扱うもの、検索条件を扱うもの、データベースを扱うもの、という三つで構成されている。

また、Java、Perl、Ruby、Pythonといった各言語のバインディングも付属し、好きな言語でHyper Estraierを利用できる。

## Hyper Estraierを利用したアプリケーション

  - [mod_estraier](http://modestraier.sourceforge.net/index.ja.html) : リバースプロクシ方式のApacheモジュール
  - [pgestraier](http://pgestraier.projects.postgresql.org/) : PostgreSQLからノードサーバを操作するためのインターフェイス
  - [acts_as_searchable](http://rubyforge.org/projects/ar-searchable) : [Ruby on Railsから操作するためのインターフェイス](../Page/Ruby_on_Rails.md "wikilink")
  - [Strigi](http://www.vandenoever.info/software/strigi/) : デーモン型デスクトップ検索ツール
  - [gdestraier](http://sourceforge.jp/projects/gdestraier/) : GNOME環境でのデスクトップ検索ツール
  - [DesktopHE](http://freemind.s57.xrea.com/desktophe/) : Javaで作成された、Windows上で使うデスクトップ検索ツール
  - [Hyper Estraier Mode on xyzzy](http://august.oor.jp/logs/estraier/)

ほかにも、[Slashdot](https://ja.wikipedia.org/wiki/Slashdot "wikilink")日本語版や商品検索[SURE-SHOT](https://ja.wikipedia.org/wiki/SURE-SHOT "wikilink")などが検索エンジンとして採用するなど、いくつかのサイトで検索エンジンとして利用されている。

## 外部リンク

  - [公式サイト](http://fallabs.com/hyperestraier/)
  - [オープンソースの全文検索システムの速度性能比較](http://www.seman.cs.uec.ac.jp/paper/oss_fulltext_search.pdf)(PDF) - 巨大な文書群のインデックス作成において、Hyper Estraierが最速であるとの結果
  - [N.M-gram : ハッシュ値付き N-gram 法による転置インデックスの実現](http://ci.nii.ac.jp/naid/110004849355) [情報処理学会](../Page/情報処理学会.md "wikilink")研究報告. DBS,データベースシステム研究会報告 140(2), 215-222, 2006-07-14 一般社団法人情報処理学会

[Category:全文検索](https://ja.wikipedia.org/wiki/Category:全文検索 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")