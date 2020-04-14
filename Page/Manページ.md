> この記事は[Manページ](https://ja.wikipedia.org/wiki/Manページ)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Unix_manual.png "wikilink") **manページ**（マンページ）とは、[UNIX](../Page/UNIX.md "wikilink")および[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の man システムのコンテンツであり、電子化された[ドキュメントのこと](../Page/ソフトウェアドキュメンテーション.md "wikilink")。各ページは独立した文書として構成されている。ライブラリやシステムコールなどの[コンピュータプログラム](../Page/プログラム_\(コンピュータ\).md "wikilink")、標準や慣例、抽象的概念などに関するページがある。`man` [コマンドを実行することでmanページを閲覧することができる](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。

## 使い方

マニュアル内のあるページを閲覧するには、以下のようなコマンドを使用する。

    % man [<章番号>] <ページ名>
    % man [-s <章番号>] <ページ名>

シェルのプロンプトで、たとえば "`man ftp`" と入力する（章番号は通常省略可能）。見やすくするため、[ページャ](https://ja.wikipedia.org/wiki/ページャ "wikilink")として一般に[less](https://ja.wikipedia.org/wiki/less "wikilink")をman内部で用いている。

ページを文章内で指す場合 "ページ名（章番号）" という書き方をする（たとえば、）。章番号は、同じ名前のページが複数の章に存在する場合、特定のページを指定するために使う。これはたとえば、[システムコール](../Page/システムコール.md "wikilink")の名前と[コマンドの名前などが衝突する場合に必要となる](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。たとえば、 と 、 と  などがある。

多くの **`man`** のバージョンでは最近閲覧した数ページのフォーマットされた内容をキャッシュとして保存している。マニュアルファイルのパス設定は環境変数MANPATHにて定義・指定する。このパスの通っていない場所にあるマニュアルは表示されない。また、言語設定が “ja” または “japanese” になっていない場合に、日本語と英語両方のマニュアルが存在する場合は、日本語で表示されない可能性があるので注意が必要。

**`man`**コマンドのその他のオプションを知るには、

    % man man
    % man 5 man

というコマンドラインを入力・実行する。

## 歴史

*[UNIX Programmer's Manual](http://man.cat-v.org/unix-1st/)* は[1971年](https://ja.wikipedia.org/wiki/1971年 "wikilink")11月3日に最初に出版された。オンラインのmanページは1971年、[ダグ・マキルロイの命令で](https://ja.wikipedia.org/wiki/ダグラス・マキルロイ "wikilink")[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")と[ケン・トンプソン](../Page/ケン・トンプソン.md "wikilink")が書いた。後に[UNIX System IIIのマニュアルの主執筆者となったTed](../Page/UNIX_System_III.md "wikilink") Dolottaが汎用的な[troff](https://ja.wikipedia.org/wiki/troff "wikilink")<small>([:en:troff](https://ja.wikipedia.org/wiki/:en:troff "wikilink"))</small>マクロを書き、それをマニュアル向けに修正したものを使っている。当時、マニュアルページシステムによる文書のオンライン化は大きな特長と考えられていた。今日では、UNIX上のコマンドライン・アプリケーションには必ずそのmanページが付属しており、逆にmanページがないアプリケーションは品質が悪いと思われるようになった。実際、[Debian](../Page/Debian.md "wikilink")プロジェクトなどでは、未だ書かれていないプログラムのmanページまで作っていた。

しかし、各アプリケーションについてひとつのページという形態は複雑で大きなアプリケーションやユーザとやりとりを行うアプリケーションには合わず、グラフィックスなども使えないフォーマット機能も時代遅れになりつつある。アプリケーションが複雑化し、ユーザーが文書がないことに文句を言わないことから、manページシステムは廃れつつあり、後継のシステムが開発されつつある。

基本的には全てのUnix系システムはmanページをサポートし続けているが、多くの場合それ以外のオンライン文書やヘルプを提供している。初期の後継システムのプロジェクトとしては、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の "[info](../Page/Texinfo.md "wikilink")" システムがあり、これは素朴な[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")システムであった。多くのUNIXの[GUIアプリケーション](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")（特に[GNOME](../Page/GNOME.md "wikilink")や[KDE](../Page/KDE.md "wikilink")の開発環境を使って作られたもの）は、ユーザー向け文書として[HTMLを採用し](../Page/HyperText_Markup_Language.md "wikilink")、`yelp`などのHTMLビューアーをアプリケーションに内蔵することが多い。

manページのデフォルトのフォーマットは[troff](https://ja.wikipedia.org/wiki/troff "wikilink") <small>([:en:troff](https://ja.wikipedia.org/wiki/:en:troff "wikilink"))</small>で あり、troffマクロのman（見た目重視）またはシステムによってはmdoc（意味論重視）を使っている。これによりmanページは[PostScript](../Page/PostScript.md "wikilink")や[PDFに変換でき](../Page/Portable_Document_Format.md "wikilink")、様々なフォーマットで表示・印刷可能となっている。

最近の[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")のmanパッケージには man2html というコマンドがあり、manページをHTMLブラウザで閲覧することも可能である。

2010年、[OpenBSD](../Page/OpenBSD.md "wikilink")はtroffの代わりにをmanページのフォーマットに採用した。mandocはmanページ専用のコンパイラ/フォーマッタで、[PostScript](../Page/PostScript.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[XHTML](../Page/Extensible_HyperText_Markup_Language.md "wikilink")、端末向けの出力を自前で行える。

## マニュアルの章立て

マニュアルは一般に8つの章に分かれており、以下のように構成されている（[BSD](../Page/BSD.md "wikilink")系と[Linux](../Page/Linux.md "wikilink")での章立て）。

| 章 | 内容                                                                                    |
| - | ------------------------------------------------------------------------------------- |
| 1 | 汎用[コマンド](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")                    |
| 2 | [システムコール](../Page/システムコール.md "wikilink")                                              |
| 3 | [ライブラリ](../Page/ライブラリ.md "wikilink")関数、特に[標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")関数 |
| 4 | 特殊なファイル（主に/devにあるデバイス）と[ドライバ](../Page/デバイスドライバ.md "wikilink")                         |
| 5 | [ファイル形式とその使用法](../Page/ファイルフォーマット.md "wikilink")                                      |
| 6 | [ゲームと](../Page/コンピュータゲーム.md "wikilink")[スクリーンセーバー](../Page/スクリーンセーバー.md "wikilink")   |
| 7 | その他                                                                                   |
| 8 | システム管理コマンドと[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")                              |

[UNIX System Vでは章立てが少し異なっている](../Page/UNIX_System_V.md "wikilink")。

| 章  | 内容                                                                                  |
| -- | ----------------------------------------------------------------------------------- |
| 1  | 汎用[コマンド](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")                  |
| 1M | システム管理コマンドと[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")                            |
| 2  | [システムコール](../Page/システムコール.md "wikilink")                                            |
| 3  | [標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")関数                                        |
| 4  | [ファイル形式とその使用法](../Page/ファイルフォーマット.md "wikilink")                                    |
| 5  | その他                                                                                 |
| 6  | [ゲームと](../Page/コンピュータゲーム.md "wikilink")[スクリーンセーバー](../Page/スクリーンセーバー.md "wikilink") |
| 7  | 特殊なファイル（主に/devにあるデバイス）と[ドライバ](../Page/デバイスドライバ.md "wikilink")                       |

いくつかのシステムではマニュアルに以下のような章もある。

| 章 | 内容                                                                                                          |
| - | ----------------------------------------------------------------------------------------------------------- |
| 0 | [標準Cライブラリ](../Page/標準Cライブラリ.md "wikilink")の[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")                         |
| 9 | [カーネル](../Page/カーネル.md "wikilink") ルーチン                                                                     |
| n | [Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")/[Tk](https://ja.wikipedia.org/wiki/Tk "wikilink") キーワード |
| x | [X Window System](../Page/X_Window_System.md "wikilink")                                                    |

章は後ろに文字を付与することでさらに分割されている。例えば、3CはCライブラリ、3Mは数学ライブラリなどといった具合である。これに関連して、8章のシステム管理コマンドを 1章の一部として1Mで表すこともある。以下のような文字は章を横断して同じ意味で使われる。

| 付与文字 | 説明                                                         |
| ---- | ---------------------------------------------------------- |
| p    | [POSIX](../Page/POSIX.md "wikilink")仕様                     |
| x    | [X Window System文書](../Page/X_Window_System.md "wikilink") |

## レイアウト

manページのレイアウトは、単純なテキストとして表示するのに最適化され、何らかの強調やフォント制御も可能ならば行われる。1つのmanページ内の節構成は以下の通りで、常に以下の順序で配置される。

  - NAME（名前） - コマンドや関数の名前とその機能を一行で説明する文。
  - SYNOPSIS（書式） - コマンドの場合、コマンド行のオプションを含めた形式定義。関数の場合、定義のあるヘッダファイルの指定とプロトタイプ宣言形式の定義。
  - DESCRIPTION（説明） - コマンドや関数についての具体的な説明。
  - EXAMPLES（例） - 使用法の具体例。
  - SEE ALSO（関連項目） - 関連するコマンドや関数のリスト。

他にも節はあるが、あらゆるマニュアルで共通化されているわけではない。例えば、OPTIONS、EXIT STATUS、ENVIRONMENT、KNOWN BUGS、FILES、AUTHOR、REPORTING BUGS、HISTORY、COPYRIGHTなどがある。

## manページの書き方

[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")や[Linux](../Page/Linux.md "wikilink")では、*man*と*mdoc*という2つの[groff](https://ja.wikipedia.org/wiki/groff "wikilink")マクロのパッケージがmanページ執筆に使える。*man*の方が古く、UNIXの従来からのフォーマットのmanページを書くことができる。一方*mdoc*は新しく、文書の意味論的構造をよくサポートしている。macOSおよびLinuxでこれらの使い方を知るには、`man groff_man`および`man groff_mdoc`というコマンドを実行すればよい。

あるいは、システム内にある個々のmanページの[ソースコード](../Page/ソースコード.md "wikilink")を見て真似をすればmanページを書ける。macOSとLinuxの場合、通常`/usr/share/man`にmanページのソースファイルがある。ソースファイルの場所は、例えばコマンド名が`command`ならば`man -w command`を実行することで得られる。

manページは[DocBook](../Page/DocBook.md "wikilink")やフォーマットで書くこともでき、それをgroffにより変換すればよい。

## manページの変換

オンラインで（`man`コマンドを使って）manページを見る以外に、manページを[PDFに変換して印刷することもできる](../Page/Portable_Document_Format.md "wikilink")。macOSとLinuxでは次のように入力する（`command`を適当なコマンド名に置き換えること）。

``` bash
 groff -mandoc command.1 >command.ps
 gs -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -sOutputFile=command.pdf command.ps
```

1行目でmanページを[PostScript](../Page/PostScript.md "wikilink")フォーマットでエクスポートし、2行目でPDFに変換している。これは*man*フォーマットでも*mdoc*フォーマットでも機能する。場合によっては、[等幅フォント](../Page/等幅フォント.md "wikilink")を使って印刷した方が読みやすい場合もある。その場合は上記の`groff`コマンドの`-mandoc`オプションの次に`-f C`オプションを追加すればよい。

フォーマッタは各種ファイルフォーマットで出力でき、PDFフォーマットも直接サポートしている。

``` bash
 mandoc -Tpdf command.1 >command.1.pdf
 mandoc -Tps command.1 >command.1.ps
 mandoc -Txhtml command.1 >command.1.xhtml
```

## 外部リンク

  - [*Unix Programmer's Manual* of November 3, 1971](http://man.cat-v.org/unix-1st/) （[原本をスキャンし PSおよびPDFフォーマットにしたもの](http://cm.bell-labs.com/cm/cs/who/dmr/1stEdman.html) も参照）

  - [History of UNIX Manpages](https://manpages.bsd.lv/history.html) - UNIX manページの歴史に関する文献

  - [Online man pages](https://www.freebsd.org/cgi/man.cgi) 各種Unix、Linux、DarwinなどのOSの各バージョンのmanページを閲覧可能

  - [man](http://primates.ximian.com/~flucifredi/man/) - オープンソース版manコマンドの実装; Red Hat, Fedora, Gentoo, Slackware, Mac OS-X などで採用している。

  - [man-db](http://man-db.nongnu.org/) - 別のmanコマンド実装; Debian/Ubuntu、SUSEなどで採用している。

  - [Practical UNIX Manuals: mdoc](https://manpages.bsd.lv/) - *mdoc*でmanページを書くためのチュートリアル

  -
  - [Manpage of man](https://linuxjm.osdn.jp/html/man/man1/man.1.html) - [JM Project](https://ja.wikipedia.org/wiki/JM_Project "wikilink")

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")