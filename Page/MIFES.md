> この記事は[MIFES](https://ja.wikipedia.org/wiki/MIFES)から翻訳されています。


**MIFES**（**マイフェス**）は、[メガソフト](https://ja.wikipedia.org/wiki/メガソフト "wikilink")株式会社が販売している[テキストエディタ](../Page/テキストエディタ.md "wikilink")である。[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")[MS-DOS](../Page/MS-DOS.md "wikilink")用 (MIFES-98) として初めて販売され、[2015年](../Page/2015年.md "wikilink")5月現在、[Windows版](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Linux](../Page/Linux.md "wikilink")版\[1\]（最終更新は2005年のVer.1.03）、[MS-DOS](../Page/MS-DOS.md "wikilink")版\[2\]（[DOS/V](https://ja.wikipedia.org/wiki/DOS/V "wikilink")版および[PC-9800](https://ja.wikipedia.org/wiki/PC-9800 "wikilink")版、最終更新は1994年のVer.5.5）が販売されているが、開発が継続されているのはWindows版のみである。MIL/W言語と呼ばれる組込の[マクロ言語](../Page/マクロ言語.md "wikilink")を実装しており、柔軟な[カスタマイズ](https://ja.wikipedia.org/wiki/カスタマイズ "wikilink")が可能である。MS-DOSが主体の頃には高速かつ高性能なスクリーンエディタとして。

発売当初はソフトウェア開発を目的としたエディタであったが、バージョンアップによって文書作成機能が強化され、バージョン9でCSV編集モード\[3\]、バージョン10でXML編集モード\[4\]が追加された。また[バイナリ](../Page/バイナリ.md "wikilink")編集モード、2GBまでのファイル編集、100個までの同時オープン、それに様々な[文字コード](../Page/文字コード.md "wikilink")に対応している。Windows版のバージョン8ではオンライン[ライセンス認証](https://ja.wikipedia.org/wiki/ライセンス認証 "wikilink")が必要になった。バージョン9ではライセンス条件が変わり、1ライセンスで2台のコンピューターとUSBメモリにインストールできるようになり、ライセンス認証は採用されていない。

## 関連機能

### 自動コード判定

ファイルを開くとき、内容を調べて文字コードを判別し、[Shift_JIS](../Page/Shift_JIS.md "wikilink")に変換して表示する機能。バージョン7までは、ファイルを閉じるときには、本来の文字コードに変換して保存できた。ただしShift_JISに変換して処理を行うためShift_JISで扱えない文字を編集できないという制限が存在したが、Windows版のバージョン8より内部処理がUnicodeに変更されShift_JISで扱えない文字も扱えるようになった。

なお、拡張子に応じてあらかじめ既定の文字コードを指定しておくことも可能である。

### 検索と置換

現在編集中のファイルの中から、指定した文字列を検索あるいは置換する。検索文字列にはメタ文字（[ワイルドカードおよび](../Page/ワイルドカード_\(情報処理\).md "wikilink")[正規表現](../Page/正規表現.md "wikilink")）の指定が可能。検索文字列を一括ハイライト表示することもできる。なお、正規表現の入力を支援するための[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")も備わっている。MIFES独自の**正規表現の方言**はやや強く、[Perl](../Page/Perl.md "wikilink")や[ECMAScript](../Page/ECMAScript.md "wikilink")など他のプログラム言語やエディタの正規表現に慣れているユーザーはこの支援機能を用いると正規表現を完成させるのが楽になる。

なお、MIFES 9からはこれまでのMIFES独自の正規表現に加えて、Perl形式の正規表現もサポートするようになった。以前のバージョンの独自正規表現では不可能だった、直前のパターンの指定回数繰り返し、および先読み／後読みの肯定／否定といった柔軟かつ強力な正規表現を使うことができるようになる。

また、複数の文字列の組を一度にそれぞれ置換する「複数置換」機能も備えている。

### グローバル検索

ディスク内の指定フォルダ以下に存在するファイルの中から、指定した文字列を検索して一覧表示する。検索文字列にはメタ文字の指定が可能。検索結果一覧表示において各行をダブルクリックすると、該当のファイルを開いて該当の行に移動するリンク機能が備わっている。検索するファイルの[拡張子](../Page/拡張子.md "wikilink")および[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")の範囲指定も可能。

### グローバル置換

ディスク内の指定フォルダ以下に存在するファイルの中から、指定した文字列を検索して置換する。

### 文書整形

半角文字と全角文字の相互変換、センタリング、引用符挿入などの整形機能。バージョン9では、行のソート、行の単一化といった機能も追加されている。

### ファイラ

ファイル管理ツールとしての[ファイラ](https://ja.wikipedia.org/wiki/ファイラ "wikilink")では、MS-DOS上でのファイル一覧に似た画面上でファイル操作ができる。

### マクロ

ユーザーの一連のコマンド操作を記録して、[マクロとして登録しておくことができるキーボードマクロ機能を備える](../Page/マクロ_\(コンピュータ用語\).md "wikilink")。マクロは独自の[コンパイル言語MIL](../Page/コンパイラ.md "wikilink")/Wで実装されており、マクロプログラム（マクロソース）はMIFESアプリケーション自体によって自動生成されるほか、ユーザーがマクロソースを記述してライブラリとして登録することもできる。

### バージョン管理ツールとの連携

MIFESバージョン9では、バージョン管理ツールである[Subversionおよび](../Page/Apache_Subversion.md "wikilink")[Microsoft Visual SourceSafe](https://ja.wikipedia.org/wiki/Microsoft_Visual_SourceSafe "wikilink") (VSS) との連携が可能となっている。MIFESのGUI上から、SubversionあるいはVSSのチェックアウト・チェックイン（コミット）、比較や履歴表示といった機能にアクセスできる。なお、Microsoft [Team Foundation Server](https://ja.wikipedia.org/wiki/Team_Foundation_Server "wikilink")（TFS）には対応していない。

### GUIのカスタマイズ

MIFESは標準でタブ[MDI動作をするが](../Page/Multiple_Document_Interface.md "wikilink")、オプションで[SDI動作に切り替えることも可能である](https://ja.wikipedia.org/wiki/Single_Document_Interface "wikilink")。

[メニューバー](https://ja.wikipedia.org/wiki/メニューバー "wikilink")、[ツールバー](https://ja.wikipedia.org/wiki/ツールバー "wikilink")、[コンテキストメニュー](../Page/コンテキストメニュー.md "wikilink")のカスタマイズはもちろん、画面各部の色やツールバーで使用される[アイコン](../Page/アイコン.md "wikilink")イメージさえもカスタマイズ可能となっている。またユーザーが自由にコマンドを割り当てて使用することができる「ユーザー定義バー」を作成することもできる。

カスタマイズ情報は項目ごとにファイルでインポート／エクスポートが可能となっており、以前のバージョンで作成したカスタマイズファイルを読み込むこともできる。

## 関連項目

  - [メガソフト](https://ja.wikipedia.org/wiki/メガソフト "wikilink")
  - [テキストエディタの一覧](https://ja.wikipedia.org/wiki/テキストエディタの一覧 "wikilink")

## 脚注

## 外部リンク

  - [MEGASOFT](http://www.megasoft.co.jp/mifes/)
  - [MIFESの歴史](http://www.megasoft.co.jp/mifes/history/index.html)

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink") [Category:DOSのソフトウェア](https://ja.wikipedia.org/wiki/Category:DOSのソフトウェア "wikilink") [Category:Windowsのソフトウェア](https://ja.wikipedia.org/wiki/Category:Windowsのソフトウェア "wikilink") [Category:Linuxのソフトウェア](https://ja.wikipedia.org/wiki/Category:Linuxのソフトウェア "wikilink") [Category:1985年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1985年のソフトウェア "wikilink")

1.  [テキストエディタ MIFES for Linux-メガソフト](http://www.megasoft.co.jp/milinux/)
2.  [テキストエディタ MIFES Ver.5.5-メガソフト](http://www.megasoft.co.jp/products/mifes55/)
3.  [CSV編集-テキストエディタ MIFES 9-メガソフト](http://www.megasoft.co.jp/mifes9/product/csv.html)
4.  [新機能-Windows版 テキストエディタ MIFES 10](http://www.megasoft.co.jp/mifes10/function/newfunction.php)