> この記事は[Clipper \(プログラミング言語\)](https://ja.wikipedia.org/wiki/Clipper_\(プログラミング言語\))から翻訳されています。


**Clipper** は、[xBase](https://ja.wikipedia.org/wiki/xBase "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")のひとつで、[コンパイラ](../Page/コンパイラ.md "wikilink")の形で提供された。汎用プログラミング言語だが、xBase言語として主に[データベース](../Page/データベース.md "wikilink")やビジネス用プログラムの作成に使われた。

## 歴史

Clipper は1985年、[xBase](https://ja.wikipedia.org/wiki/xBase "wikilink")言語として（[dBASE III向け](../Page/DBASE.md "wikilink")）[コンパイラ](../Page/コンパイラ.md "wikilink")として登場した。それまでの dBASE の[pコードマシン](https://ja.wikipedia.org/wiki/pコードマシン "wikilink")ベースの[インタプリタ](../Page/インタプリタ.md "wikilink")に対し、コンパイルによる高速化などが意図され期待されたものであった。Clipper は Nantucket Corporation が開発し、後に[コンピュータ・アソシエイツ](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink")（後のCA）に売却された。2002年4月22日、CAと GrafX Software は CA-Clipper と類似の言語である Visual Objects（CA-Visual Objects）の開発・ライセンス・販売に関する提携に合意したと発表した（Visual Objects は Nantucket が Clipper を [Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 対応させようとして生み出した言語）。

Clipper は長年にわたってDOS用ツールとして生き残りつつ、[C言語](../Page/C言語.md "wikilink")や[Pascal](../Page/Pascal.md "wikilink")の要素を取り入れ、[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")の要素やコードブロック[データ型](../Page/データ型.md "wikilink")の概念（dBASE[マクロ言語や](../Page/マクロ_\(コンピュータ用語\).md "wikilink")[文字列](../Page/文字列.md "wikilink")評価と[関数ポインタの概念を融合させたもの](../Page/関数へのポインタ.md "wikilink")）を導入し、当初よりもずっと強力な言語となってきた。

2006年現在、Clipper 言語の実装や拡張が複数の組織やベンダーで活発に行われている。[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")（[GPLライセンス](../Page/GNU_General_Public_License.md "wikilink")）では、Clip、Harbour、xHarbour などがある。商用製品としては、XBase++、FlagShip などがある。最近の実装の多くは各種プラットフォーム（DOS、Windows、[Linux](../Page/Linux.md "wikilink")、[UNIX](../Page/UNIX.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")など）で動作し、様々な拡張をサポートし[1](http://www.xharbour.org/index.asp?page=product/extensions)、[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")も豊富で、各種データベース形式（[DBF](https://ja.wikipedia.org/wiki/dBASE "wikilink")、DBTNTX、DBFCDX、MachSix、[SQL](../Page/SQL.md "wikilink") など）をサポートする Replaceable Database Drivers (RDD) がある。これらの実装は標準の dBase/[xBase](https://ja.wikipedia.org/wiki/xBase "wikilink") 文法に準拠していると同時に、オブジェクト指向的構文や `SQLExecute()` のようなターゲットデータベース対応の機能も備えている。

2007年12月現在、[ネットニュース](../Page/ネットニュース.md "wikilink")の[ニュースグループ](../Page/ニュースグループ.md "wikilink") [`comp.lang.clipper`](http://groups.google.com/group/comp.lang.clipper) と [`comp.lang.clipper.visual-objects`](http://groups.google.com/group/comp.lang.clipper.visual-objects) が今でも活動している。

## コーディング例

単純な [Hello world](../Page/Hello_world.md "wikilink") のコード例。

<code>

`? "Hello World!"`

</code>

簡単なデータベース入力のコード例。 <code>

`USE Customer SHARED NEW`
`cls`
`@  1, 0 SAY "CustNum" GET Customer->CustNum PICT "999999" VALID Customer->CustNum > 0`
`@  3, 0 SAY "Contact" GET Customer->Contact VALID !empty(Customer->Contact)`
`@  4, 0 SAY "Address" GET Customer->Address`
`READ`

</code>

## バージョン履歴

Clipper にはいくつかのバージョンがある。

Nantucket Corporation による "seasonal versions"。"[dBase](../Page/DBASE.md "wikilink") [コンパイラ](../Page/コンパイラ.md "wikilink")"として使われた。

  - Nantucket Clipper Winter'84 - [1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")5月25日
  - Nantucket Clipper Summer'85 - 1985年
  - Nantucket Clipper Winter'85 - [1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")1月29日
  - Nantucket Clipper Autumn'86 - 1986年10月31日
  - Nantucket Clipper Summer'87 - [1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")12月21日
  - Namtucket Clipper 4.5 [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink") 日本語バージョン

Nantucket Corporation による Clipper 5

  - Nantucket Clipper 5.00 - [1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")
  - Nantucket Clipper 5.01 - [1991年](../Page/1991年.md "wikilink")4月15日
  - Nantucket Clipper 5.01 Rev.129 - [1992年](../Page/1992年.md "wikilink")3月31日

[CAによる](https://ja.wikipedia.org/wiki/CA_\(企業\) "wikilink") CA-Clipper-5

  - CA Clipper 5.01a -
  - CA Clipper 5.20 - [1993年](../Page/1993年.md "wikilink")2月15日
  - CA-Clipper 5.2a - 1993年3月15日
  - CA Clipper 5.2b - 1993年6月25日
  - CA-Clipper 5.2c - 1993年8月6日
  - CA Clipper 5.2d - [1994年](../Page/1994年.md "wikilink")3月25日
  - CA-Clipper 5.2e - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")2月7日
  - CA Clipper 5.30 - 1995年6月26日
  - CA Clipper 5.3a - [1996年](../Page/1996年.md "wikilink")5月20日
  - CA Clipper 5.3b - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")5月20日

## 外部リンク

  - [mini Clipper FAQ](http://www.davep.org/clipper/)
  - [The Oasis](http://www.the-oasis.net/) CA-Clipper と xBase に関する最大のファイルアーカイブ
  - [Harbour](http://www.harbour-project.org) Open Source alternative

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:1985年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1985年のソフトウェア "wikilink")