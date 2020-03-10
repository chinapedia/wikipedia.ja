> この記事は[BugBrowser](https://ja.wikipedia.org/wiki/BugBrowser)から翻訳されています。


**BugBrowser**（バグブラウザ）は[IEコンポーネントを用いた](https://ja.wikipedia.org/wiki/IEコンポーネントブラウザ#特徴 "wikilink")[タブブラウザ](https://ja.wikipedia.org/wiki/タブブラウザ "wikilink")である。

## 概要

ユーザーの多いタブブラウザーの1つで、頻繁にバージョンアップも続けられていたが、2007年12月現在は作者の元に開発環境がないとのことで、バージョンアップは停まっている。

[Windows XP](../Page/Microsoft_Windows_XP.md "wikilink") [x64](https://ja.wikipedia.org/wiki/x64 "wikilink") Editionにおいては、[WOW64](../Page/WOW64.md "wikilink")経由で動作した例があるとの話が、作者以外からの動作報告情報として公式サイトに記載されている。（2007年2月5日現在）

## 特徴

### タブブラウズ機能

Webページ表示部分の上部から左側にかけて、横倒しL字型のタブ表示域を持つ。

上部のタブは、閲覧している複数のWebページや自マシン上のファイル等を切り換え表示するために用いられ、左側の4つのタブには、**ドキュメント**、**お気に入り**、**ごみ箱**、**履歴**という名称がそれぞれ与えられている。 左側にあるタブの上に[マウスカーソルを重ねると](https://ja.wikipedia.org/wiki/カーソル "wikilink")、**フローティングツリー**と呼ばれるツリー管理機能が作動し、以下の内容が表示される。

  - ドキュメント
    現在閲覧している、Webページや自マシン上のファイル等の全一覧
  - お気に入り
    [ブックマーク](https://ja.wikipedia.org/wiki/ブックマーク "wikilink")されているwebページ等の一覧
  - ごみ箱
    削除操作によりごみ箱入りしたファイル等の一覧
  - 履歴
    過去に閲覧したwebページや自マシン上のファイル等の一覧。設定を変更する事により、タブのクリックによる表示などに変更する事も可能。

### 検索機能

初期状態で[検索エンジン](../Page/検索エンジン.md "wikilink")を用いた検索機能（**検索バー**）が装備されている。使用可能な検索エンジンは、[Google](https://ja.wikipedia.org/wiki/Google "wikilink")、[Yahoo\!](https://ja.wikipedia.org/wiki/Yahoo! "wikilink")（[地図](https://ja.wikipedia.org/wiki/地図 "wikilink")検索を含む）、[infoseek](https://ja.wikipedia.org/wiki/infoseek "wikilink")、[goo](https://ja.wikipedia.org/wiki/goo "wikilink")（[国語辞典](../Page/国語辞典.md "wikilink")、[英和辞典](https://ja.wikipedia.org/wiki/英和辞典 "wikilink")、[和英辞典](https://ja.wikipedia.org/wiki/和英辞典 "wikilink")を含む）、[Excite](https://ja.wikipedia.org/wiki/Excite "wikilink")、[Amazon](../Page/Amazon.co.jp.md "wikilink")（全検索）である。

表示されているWebページ上の文字列をマウスで範囲指定した上で、画面上部にある**検索**と掻かれている場所をクリックして検索することも可能。検索結果は新たなタブが開いて表示される。

### リンク先URLの抽出・送出機能

1.  クリップボードにWebページの[URL](https://ja.wikipedia.org/wiki/URL "wikilink")が保存されると、当該URLで示されたリンク先ページを自動的に開くことができる。
2.  閲覧中のWebページからリンク先URLを抽出し、クリップボードにコピーしたりファイルに出力する事ができる。出力する際に拡張子によるフィルタを掛け、特定の拡張子を持つURL（例えば、jpeg画像）のみを抽出出力する事が可能（メールアドレスは除く）。抽出したURLを[ダウンロードマネージャ](https://ja.wikipedia.org/wiki/ダウンロードマネージャ "wikilink")（Iria、FlashGet、DCさくら）に直接引き渡すこともできる。

上記2つの機能は、閲覧中のWebページ等から興味のあるリンク先ページを、短時間、かつ、簡便な操作で巡回・情報収集する為に存在しているものと思われる。ただし、メールアドレスの収集活動には使えない。

### 起動時OpenURL機能

本ブラウザを起動したときに自動的に開かれる閲覧ページを、URL指定で登録する機能である。特定の閲覧ページ（掲示板等を含む）を巡回する常用ブラウザとして使う目的などに用いると便利である。ただし、あまりにもたくさんの閲覧ページを登録すると、全ての表示が完了するまでの時間が掛かるようになるので、注意が必要である。

### オートメーションサーバ機能

Webページに組み込んだスクリプトや他のアプリケーションから、本ブラウザの動作を制御できる機能を搭載している。制御に用いる事ができるスクリプトやアプリケーションのプログラミング言語は、[VBScript](../Page/VBScript.md "wikilink"),[JScript](https://ja.wikipedia.org/wiki/JScript "wikilink"),[VB](https://ja.wikipedia.org/wiki/VisualBasic "wikilink"),[Delphi](../Page/Delphi.md "wikilink"),[C++](../Page/C++.md "wikilink")など、Windowsの[Component Object Model](../Page/Component_Object_Model.md "wikilink")(COM)[インターフェースを操作可能なもの](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\) "wikilink")。

本ブラウザには、制御を行なう為の専用のメソッドやプロパティが定義されている。起動時の初期設定を始めとするページ閲覧作業の自動化などに、用いる事ができるものと思われる。

5.20の版からは、.NETスクリプトも使用できるようになった（[.NET Frameworkの全ての機能が使用できる](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")）

なお、オートメーションサーバ機能のスクリプトエンジンには、前述のIriaにも使用されているDMonkeyを用いている。

本ブラウザのオートメーションサーバ機能は管理者権限下で実行する時しか使用できない為、オートメーションサーバ機能を搭載していない派生版も配布されている。

### 使用プロキシサーバの複数設定機能

Webページを閲覧する際に使用する[プロキシ](https://ja.wikipedia.org/wiki/プロキシ "wikilink")サーバの設定を、複数登録する事ができる。

登録した複数のプロキシサーバをランダムに選択してwebページの閲覧を行なう機能も搭載している。指定した時間（分単位）が経過するごとに、使用するプロキシサーバが切り替わる。この機能を用いると、立場上身元を明かせない立場の閲覧者が、閲覧経路の[IPアドレス](../Page/IPアドレス.md "wikilink")から身元を特定され難くする効果がある。ただし、悪意のある目的（[誹謗中傷](../Page/誹謗中傷.md "wikilink")目的の[掲示板等への書き込みなど](https://ja.wikipedia.org/wiki/電子掲示板 "wikilink")）にこの機能を利用する事例が多発した場合は、本ソフトウェア自体が[マルウェア](https://ja.wikipedia.org/wiki/マルウェア "wikilink")の扱いを受ける可能性もある。

## セキュリティ

### 表示したくないWebページの排除

閲覧者にとって表示したくないWebページについては、当該WebページのURLやページタイトルを用いて強制的にページを閉じる機能が備わっている（**強制CloseURL**、**強制Closeタイトル**設定）。広告目的等のページやポップアップウィンドウを排除する目的にも使用できるものと思われる。強制CloseURL設定については、0.83の版より[ワイルドカード指定](https://ja.wikipedia.org/wiki/ワイルドカード_\(情報処理\) "wikilink")（'\*'で指定）のURLも記述できる。

### オートメーションサーバ機能の問題点

オートメーションサーバ機能は、起動時の動作設定操作の自動化やWebページ閲覧時の省力化などに役立つが、思わぬ[セキュリティホール](../Page/セキュリティホール.md "wikilink")を生じさせる場合もありうる。**悪意のあるサイトには、HTMLにBugBrowserを操作するスクリプトが記述されているかもしれません**との注意書きも添付されているので、信頼できるサイト以外を閲覧する場合はオートメーションサーバ機能によるスクリプト実行を行なわないように設定（もしくは機能非搭載版を使用）するのが望ましいと考えられる。

## B6X

BugBrowserの作者は、2009年2月1日、新たなウェブブラウザ「B6X」製作について、自身のブログで発表した。 その時点では名称は決まっていなかったが、後に開発コードは「B6X」となることを発表、そのまま正式名称となることも公表されている。

## 参考文献

  - BugBrowser（5.30.2の版および5.5.2の版）の添付文書

## 外部リンク

  - [EG6+ EXPRESS](http://eg6p.smallnews.net/)

[Category:フリーウェア](https://ja.wikipedia.org/wiki/Category:フリーウェア "wikilink") [Category:IEコンポーネントブラウザ](https://ja.wikipedia.org/wiki/Category:IEコンポーネントブラウザ "wikilink")