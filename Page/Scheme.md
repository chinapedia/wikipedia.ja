> この記事は[Scheme](https://ja.wikipedia.org/wiki/Scheme)から翻訳されています。


**Scheme**（スキーム）はコンピュータ・[プログラミング言語](../Page/プログラミング言語.md "wikilink") [Lisp](https://ja.wikipedia.org/wiki/Lisp "wikilink")の[方言のひとつで](../Page/方言_\(プログラミング言語\).md "wikilink")、[静的スコープ](../Page/静的スコープ.md "wikilink")などが特徴である。仕様（2017年現在、改7版まで存在する）を指すこともあれば、実装を指すこともある。Schemeにより、Lisp方言に静的スコープが広められた。

## 概要

Schemeは、[MIT AIラボにて](../Page/MIT人工知能研究所.md "wikilink")、[ジェラルド・ジェイ・サスマン](https://ja.wikipedia.org/wiki/ジェラルド・ジェイ・サスマン "wikilink")と[ガイ・スティール・ジュニア](../Page/ガイ・スティール・ジュニア.md "wikilink")によって1975年頃に基本的な設計がなされた。動機は、[カール・ヒューイット](../Page/カール・ヒューイット.md "wikilink")の提案によるエレガントな並行計算モデル「[アクター](../Page/アクターモデル.md "wikilink")」と、同じくその言語のPLASMA（Planner-73）を理解するためであった。

[静的スコープ](../Page/静的スコープ.md "wikilink")（[ALGOL](../Page/ALGOL.md "wikilink")由来とされる\[1\]）は、状態を持つデータであるアクタ（[クロージャ](../Page/クロージャ.md "wikilink")\[2\]）の実現以外にも、`lambda` 構文を用いた**[λ計算](https://ja.wikipedia.org/wiki/λ計算 "wikilink")**\[3\]や**[末尾再帰](../Page/末尾再帰.md "wikilink")**\[4\]の最適化に不可欠な機構であった。

また、プログラムの制御理論から当時出てきた**[継続](../Page/継続.md "wikilink")**\[5\]及びアクタ理論におけるアクタへの**メッセージ渡し**\[6\]の概念から触発された**[継続渡し形式](https://ja.wikipedia.org/wiki/継続渡しスタイル "wikilink")**\[7\]\[8\]と呼ばれるプログラミング手法は以後の継続の研究に大きな影響を与えた。

## 歴史

[MIT人工知能研究所](../Page/MIT人工知能研究所.md "wikilink")においては以下のとおりLISPに始まるいくつかの言語が作られた。

<table>
<thead>
<tr class="header">
<th><p>年</p></th>
<th><p>言語</p></th>
<th><p>作者</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1958年</p></td>
<td></td>
<td><p>マッカーシー、他</p></td>
</tr>
<tr class="even">
<td><p>1964年</p></td>
<td></td>
<td><p>ボブロウ</p></td>
</tr>
<tr class="odd">
<td><p>1969年</p></td>
<td></td>
<td><p>ガズマン</p></td>
</tr>
<tr class="even">
<td><p>1969年</p></td>
<td></td>
<td><p>ヒューイット</p></td>
</tr>
<tr class="odd">
<td><p>1970年</p></td>
<td></td>
<td><p>サスマン、ヒューイット、他</p></td>
</tr>
<tr class="even">
<td><p>1971年</p></td>
<td></td>
<td><p>サスマン、他</p></td>
</tr>
<tr class="odd">
<td><p>1972年</p></td>
<td></td>
<td><p>サスマン、他</p></td>
</tr>
<tr class="even">
<td><p>1973年</p></td>
<td></td>
<td><p>ヒューイット、他</p></td>
</tr>
<tr class="odd">
<td><p>1975年</p></td>
<td></td>
<td><p>サスマン、スティール</p></td>
</tr>
</tbody>
</table>

この中でカール・ヒューイットが設計した規則ベースの言語 [Planner](../Page/Planner.md "wikilink") はあまりに複雑な機構を持っていたため当初設計された全機能の実装は困難であり\[9\]、サスマン等はそれをサブセット言語の  として実現し、さらには、 Planner の流れを汲んだ独自言語として  を作成した。

同じくカール・ヒューイットが設計したアクタ言語  (-73) も複雑な機構を持っていたため、 による実装が存在したものの、その動作の仕組みを理解するのは困難であった。サスマン及びガイ・スティール・ジュニアは  を理解するために、不要な機能を省いた  構文を持つ小さな  を設計した。

上記の  からその小さな  の設計に至る過程は  から  及び  へ至る過程を彷彿とさせるものであったため、その言語は （計画する者）及び （策略を巡らす者）の次という意味で当初 （陰謀を企てる者）と名付けられた。しかし、当時のオペレーティングシステムのファイルシステムの制限からファイル名が6文字に切られたことから  という名前が使われるようになった。

## 機能

### 静的スコープ

マッカーシーが後に回顧で、初期のLisp（LISP 1 および LISP 1.5）に関して「In modern terminology, lexical scoping was wanted, and dynamic scoping was obtained.」と書いているように\[10\]、計算理論的にも[静的スコープ](../Page/静的スコープ.md "wikilink")が本来は「正当」であり、[動的スコープ](../Page/動的スコープ.md "wikilink")は、言ってしまえばある種の安易なインタプリタの実装手法が招く「バグ」である（有用なことも多いが）。

ガイ・スティールは、LISP 1.5 からの変更点として最初に静的スコープの採用と実装を挙げており、サスマンが[Algol](https://ja.wikipedia.org/wiki/Algol "wikilink")に関して持っていた興味からによるもので、Algolの直接の影響だと述べている。\[11\]

「FUNARG問題」（[:en:Funarg problem](https://ja.wikipedia.org/wiki/:en:Funarg_problem "wikilink")）としてLISPの初期から既に認識され議論されていたことでもあり、必ずしもSchemeから始まったとは言えないが、Scheme以後のLisp方言に静的スコープが広まったのはSchemeからの影響と言ってよく、殊に[Common Lispは特筆される](../Page/Common_Lisp.md "wikilink")。

### 継続

#### `call-with-current-continuation`

は（略称：`call/cc`）と呼ばれる\[12\]ピーター・ランディンやジョン・レイノルズに始まる脱出オペレータ\[13\]の命令を提供する。

## 言語仕様

の言語仕様は[IEEE](../Page/IEEE.md "wikilink")によって公式に定められ\[14\]、その仕様は「」と呼ばれている。2016年現在広く実装されているものは改訂第五版に当たるR5RS（1998年）である。

なお、2007年9月に「」\[15\]が成立した。4部構成となり、R5RSに比べおよそ3倍の文章量となった。R5RSまでは小さな言語仕様に対してのこだわりが見られたが、 サポート等の実用的な言語として必要な要素が盛り込まれている点が特徴的である。しかし、多くの機能が盛り込まれたにもかかわらず細部の練りこみが不十分であるといった批判もあり、非公式にR5RSを拡張する形でERR5RS () という規格を検討する党派も現れている。

2009年8月、 言語運営委員会は、 を大規模バージョンと、大規模バージョンのサブセットとなる小さな言語仕様のふたつの言語に分割することを推奨する意向を発表した\[16\]。

2013年7月、「」\[17\] () が成立した。

### 仕様の決定

## 実装

の仕様書はR5RSだと50ページにも満たないため、かなりの数の実装が存在する。

  - [](http://www-sop.inria.fr/mimosa/fp/Bigloo/) - 高速な実行ファイルを作るコンパイラ。

  - [](http://www.biwascheme.org/) -  による実装。ブラウザ上で動作する。

  - [](http://www.scheme.com/) - もと商用だったが、現在はオープンソースの高速な実装。

  - [{{lang](https://ja.wikipedia.org/wiki/Chicken_\(Scheme\) "wikilink") - 可搬性の高い実用的コンパイラ。

  - \- インタプリタ。多言語への対応、 を発展させた（メタ）オブジェクトシステムを持つ。

  - \-  の公式な拡張用言語。 を元にしている。

  - [](http://hscheme.sourceforge.net/)

  - [](http://www.codeplex.com/IronScheme)

  - [](http://www.norvig.com/jscheme.html)

  - [](http://www.yuasa.kuis.kyoto-u.ac.jp/~yuasa/jakld/index-j.html) -  アプリケーション組み込み用のドライバ

  - [](http://www.gnu.org/software/kawa/) - [{{langのひとつ](../Page/GNUプロジェクト.md "wikilink")。 プログラムを  仮想機械用にコンパイル可能。

  - [](http://www.larcenists.org/) - [IA-32](../Page/IA-32.md "wikilink")、 の機械語を出力。IEEE/ANSI、R5RS、ERR5RS, R6RS準拠。

  - [](http://www.lispme.de/) -  用の実装。無料。

  - [](http://www.swiss.ai.mit.edu/projects/scheme/) - [x86](https://ja.wikipedia.org/wiki/x86 "wikilink")アーキテクチャ用の  実装。無料。

  - [](http://code.google.com/p/mosh-scheme/) - R6RS準拠の高速なインタプリタFFI、ソケットなどの拡張も。

  - [](http://will.iki.fi/software/ocs/)

  - [](http://www.mazama.net/scheme/pscheme.htm) -  用の実装。

  - \- 旧称 。教育用の豪華な開発環境、柔軟なシステムで広く使われる。

  - [](http://www.sof.ch/dan/qscheme/index-e.html)

  - [](http://www.kt.rim.or.jp/~qfwfq/rhiz-pi/index.html)

  - [](http://s48.org/)

  - [](http://www.maroon.dti.ne.jp/nagar17/mulasame/) -  拡張による（並列）。

  - [](http://code.google.com/p/sigscheme/) - アプリケーション組み込みを目的としたR5RS準拠の実装。[uim](https://ja.wikipedia.org/wiki/uim "wikilink")で使用されている。

  - [](http://sisc-scheme.org/) - 。 仮想機械上で動作するR5RS準拠の実装。 オブジェクトを  上から利用することが可能。

  - [](http://tinyscheme.sourceforge.net/) - 非常に小さい実装。[{{langなどでも走る](../Page/ザウルス.md "wikilink")。正規表現やソケット通信もサポート。

  - [](http://code.google.com/p/vx-scheme/) -  用の実装。

  - [](http://code.google.com/p/ypsilon/) - R6RSに準拠するリアルタイムアプリケーション向けの実装。

### SRFI（サーフィ）

は言語機能を必要十分の最低限まで単純化することを目指した言語である。そのため仕様書が簡素な反面、実用に際して各種のライブラリが乱立し、移植性が問題になっていた。そこで実装間の統一をとるため、コミュニティ内の議論を集約しているのが「」である。 ではライブラリ仕様、言語拡張仕様などがインデックス化されており、 準拠の実装系は「◯◯に準拠」といった形で利用者の便宜を図ることができる。

なお、 では言語機能とライブラリ機能は分けて考えられているため、 と  言語仕様のコミュニティは原則分離している。

## 応用

はしばしば他のアプリケーションの拡張用言語として使われる。代表的なアプリケーションには以下のようなものがある。

  - の

  - [uim](https://ja.wikipedia.org/wiki/uim "wikilink")

  - [{{lang](../Page/GNU_LilyPond.md "wikilink")

より専門的な応用としては、映画[ファイナルファンタジーのために](../Page/ファイナルファンタジー_\(映画\).md "wikilink")3Dレンダリングエンジンに  インタプリタを組み込んだ例\[18\]や、[リトルウイング](../Page/リトルウイング.md "wikilink")のピンボールコンストラクションシステムの記述に  を使った例\[19\]がある。

用の  では、 コンパイラである  を使って[{{lang用のバイトコードを生成している](../Page/Java仮想マシン.md "wikilink")。

## 出典

### ラムダ論文一覧

が発表された一連の論文は、ラムダ論文と呼ばれている\[20\]。

<table>
<thead>
<tr class="header">
<th><p>年</p></th>
<th><p>題名</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>nowrap|1975年</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>nowrap|1976年</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>nowrap|1976年</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>nowrap|1977年</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>nowrap|1978年</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>nowrap|1978年</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>nowrap|1979年</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>nowrap|1980年</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>nowrap|1980年</p></td>
<td></td>
</tr>
</tbody>
</table>

### 参考文献

  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
  - [和訳](http://kreisel.fam.cx/webmaster/clog/img/www.ice.nuie.nagoya-u.ac.jp/~h003149b/lang/p/funarg/funarg.html)

## 脚注

## 関連項目

  - [アクターモデル](../Page/アクターモデル.md "wikilink")

  - [継続](../Page/継続.md "wikilink")

  - [末尾再帰](../Page/末尾再帰.md "wikilink")

  -
  - [計算機プログラムの構造と解釈](../Page/計算機プログラムの構造と解釈.md "wikilink") -  を用いた計算機科学分野の古典的な教科書。

## 外部リンク

  - [`schemers.org`](http://schemers.org/)
  - [`R6RS.org`](http://www.r6rs.org/)
  - [](http://srfi.schemers.org/)
  - [プログラミング言語 ](http://www.sci.u-toyama.ac.jp/~iwao/Scheme/scheme.html)
  - [R5RS](http://www.swiss.ai.mit.edu/~jaffer/r5rs_toc.html)
  - [R5RS日本語版](http://www.swiss.ai.mit.edu/~jaffer/r5rsj_toc.html)
  - [](http://scheme-punks.cyber-rush.org/wiki/index.php?title=Main_Page)
  - [独習  三週間](http://www.sampou.org/scheme/t-y-scheme/t-y-scheme.html)
  - [](http://practical-scheme.net/)
  - [もうひとつの Scheme 入門](http://www.shido.info/lisp/idx_scm.html)

[Category:Scheme](https://ja.wikipedia.org/wiki/Category:Scheme "wikilink") [Category:LISP](https://ja.wikipedia.org/wiki/Category:LISP "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink")

1.  元々のALGOLには関数引数等が無いためFUNARG問題なども無く、静的スコープの歴史としてALGOLをあまり強調する意味は無い。
2.
3.
4.
5.
6.
7.  、CPS
8.  継続渡し形式は一連のλ論文において導入された。ただし、体系として確立されてはいないものの、同様の手法は「」にもみられる。
9.  後の完全な Planner の実装として、エジンバラ大学の Julian Davies が POP-2 で実装した Popler がある
10. <http://www-formal.stanford.edu/jmc/history/lisp/node4.html>
11. 「Scheme 過去◇現在◇未来 前編」『bit』（共立出版）Vol. 28, No.4（1996年4月号） pp. 4～9
12. 当初は `CATCH` という名称であった。
13.
14.
15.
16.
17.
18.
19.
20.