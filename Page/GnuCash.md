> この記事は[GnuCash](https://ja.wikipedia.org/wiki/GnuCash)から翻訳されています。


[C++](../Page/C++.md "wikilink"){{・}}[Guile](https://ja.wikipedia.org/wiki/GNU_Guile "wikilink") |対応言語=[英語](../Page/英語.md "wikilink"){{・}}[中国語](https://ja.wikipedia.org/wiki/中国語 "wikilink"){{・}}[フランス語](https://ja.wikipedia.org/wiki/フランス語 "wikilink"){{・}}[ドイツ語](../Page/ドイツ語.md "wikilink")など21ヶ国語 |対応プラットフォーム=[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink") | operating_system = [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink"){{・}}[BSD](../Page/BSD.md "wikilink")などの[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink"){{・}}[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink"){{・}}[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | genre = [財務](../Page/財務.md "wikilink")管理{{・}}[会計ソフトウェア](https://ja.wikipedia.org/wiki/会計ソフトウェア "wikilink") | license = [GPL](../Page/GNU_General_Public_License.md "wikilink") | website =  }}

**GnuCash**（グニュー・キャッシュ）とは、[財務](../Page/財務.md "wikilink")管理（金銭管理）を行うための[会計ソフトウェア](https://ja.wikipedia.org/wiki/会計ソフトウェア "wikilink")の1つ。

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")や[Unix系](https://ja.wikipedia.org/wiki/Unix系 "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上の [GNOME](../Page/GNOME.md "wikilink")環境で動作し、[GPLライセンスのもとで配布されている](../Page/GNU_General_Public_License.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。[BSD](../Page/BSD.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")でも動作する。バージョン2.2.0 以降では [Microsoft Windowsもサポートされるようになった](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")\[1\]。

## 特徴

個人の金銭管理、とりわけ[家計簿](https://ja.wikipedia.org/wiki/家計簿 "wikilink")として利用できる他、比較的[小規模企業の財務管理に役立つように作られており](../Page/中小企業.md "wikilink")、[複式簿記](../Page/複式簿記.md "wikilink")の仕組みを採り入れた財務管理を行う。直感的な操作が可能なインターフェースが採用されている。バージョン 2.2.xにおいてはアプリケーション・メニューの一部が完全に日本語化されていないが、通常の利用には差し支えが無い。バージョン 2.2.3に至って、ほぼ全ての日本語化が完了した\[2\]。

GnuCashは、取引月日の表示や利用通貨の国際化に対応している。アプリケーション・メニューの表示は、中国語や[デンマーク語](../Page/デンマーク語.md "wikilink")、フランス語、ドイツ語を始めとして、21ヶ国語に対応している。また、ドキュメント類については、英語やフランス語、[ポルトガル語](https://ja.wikipedia.org/wiki/ポルトガル語 "wikilink")、[スペイン語](https://ja.wikipedia.org/wiki/スペイン語 "wikilink")で利用できる\[3\]。

GnuCash は、[GPLのもとで配布される](../Page/GNU_General_Public_License.md "wikilink")[自由なソフトウェアであり](../Page/フリーソフトウェア.md "wikilink")、[GNOME](../Page/GNOME.md "wikilink")アプリケーションの1つに含められる。

## 機能

[right](https://ja.wikipedia.org/wiki/ファイル:Gnucash-currency-transfer.png "wikilink") 多数の編集機能が備わっているが、その一部を以下列挙する。

  - [勘定科目](https://ja.wikipedia.org/wiki/勘定科目 "wikilink")は、[階層構造](../Page/階層構造.md "wikilink")に編集し管理することができる。

  - 資金の流れは、[円グラフ](https://ja.wikipedia.org/wiki/円グラフ "wikilink")や[棒グラフ](https://ja.wikipedia.org/wiki/棒グラフ "wikilink")で把握できる。

  - 複数の異なる[通貨](../Page/通貨.md "wikilink")を一元的に管理できる。

  - および、、[OFX形式のファイルをインポートすることが可能である](https://ja.wikipedia.org/wiki/Open_Financial_Exchange "wikilink")。

  - データの保存には[XML形式が使われるが](../Page/Extensible_Markup_Language.md "wikilink")、バージョン 2.4.0 から[SQLite](https://ja.wikipedia.org/wiki/SQLite "wikilink")3や[MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")、[PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")といった[RDBMSも利用可能になった](../Page/関係データベース管理システム.md "wikilink")。

  - [貸借対照表](../Page/貸借対照表.md "wikilink")や[損益計算書](../Page/損益計算書.md "wikilink")などの帳票を生成可能。これらの帳票は[HTMLとして生成され](../Page/HyperText_Markup_Language.md "wikilink")、あるいは[WebKit](https://ja.wikipedia.org/wiki/WebKit "wikilink")により表示される。

  - [為替レート](../Page/為替レート.md "wikilink")や[株価](../Page/株価.md "wikilink")などは[Perl](../Page/Perl.md "wikilink")の[Finance::Quote](http://finance-quote.sourceforge.net/)モジュールで対応している情報サービスであれば自動的に最新の情報を取得し、反映することができる。

## リリース

それぞれのリリースには、一般ユーザー向けに配布される「安定版」と、開発者向けに用意された「開発版」の2種類が存在する。リリース番号の第2番目の数字が偶数であれば安定版、奇数であれば開発版という扱いとなっている\[4\]。

| リリース日       | バージョン       |
| ----------- | ----------- |
| 2013年12月30日 | 2.6.0\[5\]  |
| 2010年12月21日 | 2.4.0\[6\]  |
| 2009年 5月15日 | 2.3.0\[7\]  |
| 2009年 2月23日 | 2.2.9\[8\]  |
| 2008年12月14日 | 2.2.8\[9\]  |
| 2008年 9月27日 | 2.2.7\[10\] |
| 2008年 7月31日 | 2.2.6\[11\] |
| 2008年 4月28日 | 2.2.5\[12\] |
| 2008年 3月 4日 | 2.2.4\[13\] |
| 2008年 1月 8日 | 2.2.3\[14\] |
| 2007年 7月15日 | 2.2.0\[15\] |
| 2006年 7月 9日 | 2.0.0\[16\] |
| 2003年 2月 3日 | 1.8.0\[17\] |

## 出典

<references />

## 外部リンク

  -
  - [GnuCash Wiki](https://wiki.gnucash.org/wiki/GnuCash)

  - [SourceForge プロジェクト・ホームページ](https://sourceforge.net/projects/gnucash/)

  - [GnuCash 利用ガイド](https://code.gnucash.org/docs/ja/gnucash-guide/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:GNOME](https://ja.wikipedia.org/wiki/Category:GNOME "wikilink") [Category:会計ソフトウェア](https://ja.wikipedia.org/wiki/Category:会計ソフトウェア "wikilink")

1.
2.  gnucash-2.2.3.tar.gzをインストールしたときは、初期設定画面が英語で表示されるため、未だ完全に日本語化されていない。日本語ドキュメントも未整備である。
3.
4.  例えば、2.*2*.0は安定版、2.*1*.0は開発版。
5.  <http://lists.gnucash.org/pipermail/gnucash-announce/2013-December/000188.html>
6.  <http://lists.gnucash.org/pipermail/gnucash-announce/2010-December/000128.html>
7.  <https://lists.gnucash.org/pipermail/gnucash-devel/2009-May/025405.html>
8.  <http://lists.gnucash.org/pipermail/gnucash-announce/2009-February/000098.html>
9.  <http://lists.gnucash.org/pipermail/gnucash-announce/2008-December/000097.html>
10. <http://lists.gnucash.org/pipermail/gnucash-announce/2008-September/000096.html>
11. <http://lists.gnucash.org/pipermail/gnucash-announce/2008-July/000095.html>
12. <http://lists.gnucash.org/pipermail/gnucash-announce/2008-April/000094.html>
13. <http://lists.gnucash.org/pipermail/gnucash-announce/2008-March/000093.html>
14. <http://lists.gnucash.org/pipermail/gnucash-announce/2008-January/000092.html>
15. <http://lists.gnucash.org/pipermail/gnucash-announce/2007-July/000089.html>
16. <http://lists.gnucash.org/pipermail/gnucash-announce/2006-July/000069.html>
17. <http://www.gnucash.org/oldnews.phtml>