> この記事は[TWiki](https://ja.wikipedia.org/wiki/TWiki)から翻訳されています。


**TWiki** は[構造化ウィキ](https://ja.wikipedia.org/wiki/構造化ウィキ "wikilink")の一種であり、連携基盤、[ナレッジマネジメント](../Page/ナレッジマネジメント.md "wikilink")システム、[文書管理システム](https://ja.wikipedia.org/wiki/文書管理システム "wikilink")、[知識ベース](https://ja.wikipedia.org/wiki/知識ベース "wikilink")その他の共有アプリケーションとして使われる。[ブログ](../Page/ブログ.md "wikilink")にも使うことができる。ウェブコンテンツは[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")や[イントラネット](../Page/イントラネット.md "wikilink")を通してブラウザだけで共同で作成することができる。TWiki は、プログラミング経験のないユーザーでもウィキアプリケーションを作成でき、[プラグイン](../Page/プラグイン.md "wikilink")を使って機能を拡張できる。

## 概要

TWiki は他のウィキと同様、共有ホワイトボードとして使うことができる。TWiki はまた単純な（プログラミング不要な）フォームベースのウェブアプリケーション作成にも利用できる。その他にも[バージョン管理](../Page/バージョン管理システム.md "wikilink")、細かい[アクセス制御](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")（全くアクセス制御しない使い方も可能）、構成変数、可変テキスト、[トランスクルージョン](https://ja.wikipedia.org/wiki/トランスクルージョン "wikilink")、電子メール通知、[RSS](../Page/RSS.md "wikilink")/Atom、埋め込み型検索、[Server Side Includes](https://ja.wikipedia.org/wiki/Server_Side_Includes "wikilink")、ファイルアタッチメントといった機能がある。

TWiki にはプラグインAPIがあり、260ものプラグインがある。[データベース](../Page/データベース.md "wikilink")とのリンク、グラフ作成、[タギング](https://ja.wikipedia.org/wiki/タギング_\(コンピュータ\) "wikilink")、表のソート、[スプレッドシート作成](../Page/表計算ソフト.md "wikilink")、画像ギャラリー/[スライドショー](../Page/スライドショー.md "wikilink")の作成、[イラストレーション](../Page/イラストレーション.md "wikilink")、[ブログ](../Page/ブログ.md "wikilink")、各種[認証](../Page/認証.md "wikilink")スキーマとのインタフェース、[エクストリーム・プログラミング](../Page/エクストリーム・プログラミング.md "wikilink")プロジェクト管理向け機能などのプラグインがある。

TWiki はテンプレートやテーマ、ユーザー毎の[CSS設定によって見た目を変更できる](../Page/Cascading_Style_Sheets.md "wikilink")。[国際化と地域化](../Page/国際化と地域化.md "wikilink")（I18N）もよくサポートしており、各種文字セットや UTF-8 URL をサポートし、中国語、チェコ語、オランダ語、フランス語、ドイツ語、イタリア語、日本語、ポーランド語、ポルトガル語、ロシア語、スペイン語、スウェーデン語といった言語でのユーザーインタフェースをサポートしている。

[バージョン管理と](../Page/バージョン管理システム.md "wikilink")[アクセス制御リスト](https://ja.wikipedia.org/wiki/アクセス制御リスト "wikilink")を備えているため、TWiki は特に企業などのサイト（[企業向けwiki](https://ja.wikipedia.org/wiki/企業向けwiki "wikilink")）に適している（公式サイトによれば、2007年3月現在で約4万のサイトが利用している）。一方、他の機能により、インターネット上のウィキサイトにも使われている（同様に、約2万サイトで使われている）。TWiki は[Perl](../Page/Perl.md "wikilink")で実装されており、[GPL](../Page/GNU_General_Public_License.md "wikilink") によりフリーかつオープンソースなソフトウェアとしてリリースされている。また、[仮想アプライアンス](https://ja.wikipedia.org/wiki/仮想アプライアンス "wikilink")としても利用可能である。

## 主な機能

  - バージョン管理 - アクセス制御設定などのメタデータも含めた完全な履歴
  - ユーザーグループ単位の細かいアクセス制御
  - 判り易い包括的[マークアップ言語](../Page/マークアップ言語.md "wikilink")
  - WYSIWIGエディタ
  - TWiki 変数による動的コンテンツ生成
  - データベースは不要（テキストファイルとして格納）
  - 構造化情報をフォームを使って入力可能
  - プログラミング経験がなくてもウィキアプリケーションを作成可能
  - 各種プラグインあり
  - カスタマイズ可能なサイドバー、トップバー、ボトムバー

## リリース

TWikiを使うには、Perl、GNU diff、GNU grep が必要である。[RCS](../Page/Revision_Control_System.md "wikilink") は、Perl による代替品があるので、必須ではない。

括弧内は開発時のコード名を示している。

  - [最新版ダウンロード](http://twiki.org/cgi-bin/view/Codev/DownloadTWiki)、[VMダウンロード](http://twiki.org/cgi-bin/view/Codev/TWikiVMDebianStable)、[TWiki for Windows Personal ダウンロード](http://twiki.org/cgi-bin/view/Codev/TWikiForWindowsPersonal)
  - TWiki-5.0.1 Release (10-Oct-2010)
  - TWiki-5.0.0 Release (29-May-2010)
  - TWiki-4.1.2 Release (03-Mar-2007) (Edinburgh)
  - TWiki-4.0.5 Release (24-Oct-2006) (Dakar)
  - TWiki Release 04-Sep-2004 (Cairo)
  - TWiki Release 01-Feb-2003 (Beijing)
  - TWiki Release 01-Dec-2001 (Athens)
  - TWiki Release 01-Sep-2001
  - TWiki Release 01-Dec-2000
  - TWiki Release 01-May-2000

詳しくは公式サイト（外部リンク）参照。

## TWiki.org コミュニティウィキ

twiki.org のコミュニティウィキには TWiki とウィキ全般に関する約5万のページがある。

  - [Codev web](http://twiki.org/cgi-bin/view/Codev/WebHome): ウィキ技術とTWikiエンジン開発
  - [TWiki web](http://twiki.org/cgi-bin/view/TWiki/WebHome): TWikiソフトウェアに関する文書
  - [Plugins web](http://twiki.org/cgi-bin/view/Plugins/WebHome): TWiki拡張（プラグイン、アドオン、スキン、コード寄贈）のリストとパッケージ
  - [Support web](http://twiki.org/cgi-bin/view/Support/WebHome): TWikiユーザーやアドミニストレータのためのサポート

## TWiki を使っている主な公共サイト

  - [CERN Webs](https://twiki.cern.ch/twiki/bin/view/DefaultWeb/WebHome) - CERN研究所
  - [Java.net](http://wiki.java.net/bin/view/Main/WebHome) - Java開発者向けオンライン百科事典
  - [Biowiki](http://biowiki.org/) - カリフォルニア大学バークレー校での計算生物学プロジェクト
  - [IntelliJ Community Wiki](http://www.intellij.org/twiki/bin/view/Main/WebHome) - 開発者向けウィキ
  - [BEAs dev2dev wiki](http://dev2dev.bea.com/wiki/bin/view/Main/WebHome) - 開発者向けウィキ

## 外部リンク

  - [twiki.org](http://twiki.org/) - 公式サイト
  - [TWIKI.NET](http://twiki.net/) - 商用インストールと保守を行っている企業
  - [List of TWiki installations](http://twiki.org/cgi-bin/view/Main/TWikiInstallation)
  - [User submitted stories of some companies using TWiki](http://twiki.org/cgi-bin/view/Main/TWikiSuccessStories)

[Category:ウィキ](https://ja.wikipedia.org/wiki/Category:ウィキ "wikilink") [Category:ウィキクローン](https://ja.wikipedia.org/wiki/Category:ウィキクローン "wikilink") [Category:グループウェア](https://ja.wikipedia.org/wiki/Category:グループウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink")