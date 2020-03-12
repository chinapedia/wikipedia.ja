> この記事は[Maxima](https://ja.wikipedia.org/wiki/Maxima)から翻訳されています。


**Maxima**（マキシマ）は、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink") で記述された[数式処理システム](../Page/数式処理システム.md "wikilink")である。[GNU GPL](../Page/GNU_General_Public_License.md "wikilink") に基づく[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")であり、現在も活発に開発が続けられている。[Maple](../Page/Maple.md "wikilink") や [Mathematica](../Page/Mathematica.md "wikilink") などの商用の数式処理システムと比べても遜色のない機能を持っている。

## 略史

Maxima の起源は、[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")の [MACプロジェクトによって開発され](https://ja.wikipedia.org/wiki/Project_MAC "wikilink")、[米国エネルギー省](../Page/アメリカ合衆国エネルギー省.md "wikilink")（DOE）によって配布されていたDOE [Macsyma](../Page/Macsyma.md "wikilink") の1982年のバージョンを [GNU Common Lisp](https://ja.wikipedia.org/wiki/Common_Lisp#実装のリスト "wikilink") に移植したものである。

1982年から Macsyma の独自のバージョンを管理・維持していた[ビル・シェルター](https://ja.wikipedia.org/wiki/ビル・シェルター "wikilink") ([en](https://ja.wikipedia.org/wiki/:en:Bill_Schelter "wikilink")) が、1998年にエネルギー省から GPLライセンスを適用することを条件に公開の許可を得た。こうして公開されたプログラムは Maxima と呼ばれることになり、2001年のシェルターの死後も開発者や利用者のグループによって独自に開発が続けられている。

## 実装

上述のように、Maxima は [GNU Common Lisp](https://ja.wikipedia.org/wiki/Common_Lisp#実装のリスト "wikilink") への移植から開発が始まったが、その後 [CLISP](../Page/CLISP.md "wikilink") や[CMU Common Lisp](https://ja.wikipedia.org/wiki/CMU_Common_Lisp "wikilink") (CMUCL) でも動作するように改良されている。V5.9 以降は、CLISP や CMUCL が標準になっている 。

Maxima は、文法的には [ALGOL](../Page/ALGOL.md "wikilink") に、意味的には Lisp にそれぞれ類似のプログラム言語を備えており、プログラミングや計算機代数の教育用としても使えるようになっている。

他の数式処理システムと同様に Maxima も高度な記号処理機能を備えており、有理数や[多倍長整数](https://ja.wikipedia.org/wiki/多倍長整数 "wikilink")、多倍長浮動小数点の演算を可能にしている。浮動小数点数や配列の処理をより効率の良い [FORTRAN](../Page/FORTRAN.md "wikilink") などで処理するためのプログラム書き出しもサポートされている。

Maxima を[グラフィカルユーザーインターフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザーインターフェース "wikilink")から操作するためのフロントエンドとして、[](../Page/TeX.md "wikilink") と [Emacs](../Page/Emacs.md "wikilink") の発想を受け継いだ[GNU <span style="text-transform:uppercase;margin-left:-0.1667em;vertical-align:-0.5ex;line-height:0;margin-right:-0.125em">macs</span>](https://ja.wikipedia.org/wiki/GNU_TeXmacs "wikilink")、[wxWidgets](https://ja.wikipedia.org/wiki/wxWidgets "wikilink") に基づいた wxMaxima、[Emacs](../Page/Emacs.md "wikilink") 用のパッケージ [imaxima](https://ja.wikipedia.org/wiki/imaxima "wikilink") などがある。

## 他のシステムとの比較

  - 結果が[超幾何関数となる](https://ja.wikipedia.org/wiki/超幾何級数#超幾何関数 "wikilink")[積分](https://ja.wikipedia.org/wiki/積分 "wikilink")などの出力は、Mathematica や Maple に比して現在の実装上には限界があることが報告されている\[1\]。

## 使用法

コマンド処理、バッチ処理によるプログラムが可能である。

表記法（入力規則）

`コメント`
` C言語のコメントと同じ`
`  /*コメント行*/`
`実行`
` 結果を表示する場合は式の最後に ; を入れて改行する。`
`  式;`
` 結果を非表示にする場合は$を入れて改行する。`
`  式$`
`代入`
`  変数:代入式;`
`  関数(変数):=代入式;`
`  ev(式,変数=数式);`
`n次解(リストで表示)`
`  [解[1],解[2],...]`

演算（加減乗除, 関数）

`+ 加算`
`- 減算`
`* 乗算`
`/ 除算`
`** べき乗`
`^ べき乗`
`() 括弧内の処理を優先させる。`
`sin()`
`cos()`
`tan()`
`…他にも様々な関数があります。`

抽出

`分数`
` ratsimp(有理式);  通分する`
` num(分子/分母);   分子を取り出す`
` denom(分子/分母); 分母を取り出す`
`右辺、左辺`
` rhs(左辺=右辺);   右辺を取り出す。`
` lhs(左辺=右辺);   左辺を取り出す。`

多項式

`expand(多項式);                     展開`
`factor(多項式);                     因数分解`
`taylor(関数,変数,展開中心,近似次数);  テーラー展開`

解法

`solve([方程式リスト],[変数リスト]);   方程式を解く`
`limit(関数,変数,近づける値);         極限値`
`diff(関数,変数,階数);                微分`
`integrate(関数,変数,開始値,終了値);   積分`
`sum(関数,添え字変数,初期値,終値);     総和を求める ΣAi = A0+A1+...+An`
`product(関数,添え字変数,初期値,終値); 総積を求める ΠAi = A0*A1*...*An`

微分方程式

` atvalue(関数,独立変数=値,関数値);    初期値を代入`
` desolve(微分方程式,求める関数);      微分方程式を解く`

グラフ表示 (2D,　3D)

`plot2d([関数,...]，[変数，始値，終値]);                            /* 2次元グラフ */ `
`plot3d([関数,...]，[変数1，始値1，終値1]，[変数2，始値2，終値2]);    /* 3次元グラフ */`

プログラム

`条件式`
` = 等しい`
` # 等しくない`
` <, >, >=, <= 実数として、大小関係を問う`
` 条件式1 and 条件式2 and ...`
` 条件式1 or 条件式2 or ...`
`分岐`
` if 条件式then 真の場合の処理else 偽の場合の処理;`
`ループ`
` for カウンタ名:初期値step 増分thru 終了値do(反復実行手続き);`
` for カウンタ名:初期値step 増分while 条件式do(反復実行手続き);`
`関数化(リスト化)`
` block([局所変数のリスト], 一連の手続き,return(計算結果));`

ファイル入出力

`ファイルデータをエディタを使って編集することも可能です。`
`書き出し`
` save("ファイル名",all);`
`読み込み`
` loadfile("ファイル名");`
`実行結果表示`
` playback(all);`

## 脚注

## 外部リンク

  - [Maxima, a Computer Algebra System(公式ホームページ)](http://maxima.sourceforge.net/)
  - [Maxima Documentation(英文マニュアル、参考文書等)](http://maxima.sourceforge.net/documentation.html)
  - [日本語マニュアル](http://maxima.osdn.jp/maxima.html)
  - [Maxima 日本語ドキュメント（OSDNプロジェクト）](http://maxima.osdn.jp/) （ダウンロード方式）
  - [Maxima 日本語マニュアル（OSDNプロジェクト）](http://maxima.osdn.jp/maxima.html) (Webブラウジング方式)
  - [Wikibooks "Maxima"](https://ja.wikibooks.org/wiki/Maxima)
  - [Joel Moses: "Macsyma: A Personal History" (2008).](http://esd.mit.edu/Faculty_Pages/moses/Macsyma.pdf)

<!-- end list -->

  - 日本語の解説

<!-- end list -->

  - [Maximaで遊ぼう](http://www.bekkoame.ne.jp/~ponpoko/Math/maxima/MaximaMAIN.html)

  - \- 最新版にも大部分が通用するが、執筆当時の Maxima のバージョンは 5.9.2。

  -
  - [Professional Maxima](http://www.muskmelon.jp/maxima/)

## 解説書類

  - 横田 博史:「はじめてのMaxima」、工学社、ISBN 978-4777512010、 (2006年9月)。
  - 竹内薫：「はじめての数式処理ソフト―Maximaで楽しむ数式計算と物理グラフィック」、講談社(ブルーバックス) 、ISBN 978-4062575607、 (2007年7月20日)。
  - 赤間 世紀：「Maximaで学ぶ微分積分―フリーの「数式処理ソフト」を使って効率的に学習」、工学社(I・O BOOKS) 、ISBN 978-4777515905(2011年4月1日）。
  - 赤間 世紀：「Maximaによる力学入門」、工学社 (I・O BOOKS)、 ISBN 978-4777516216(2011年8月1日)。
  - 赤間 世紀、I・O編集部 (編) ：「Maximaによる電磁気学入門」、工学社、ISBN 978-4777516889（2012年6月1日）。
  - 岩城 秀樹：「Maximaで学ぶ経済・ファイナンス基礎数学」、共立出版、ISBN 978-4320110311（2012年12月8日）。
  - 川谷 亮治：「「Maxima」と「Scilab」で学ぶ古典制御」（改訂版）、工学社 (I・O BOOKS)、ISBN 978-4777518142（2014年2月1日）。
  - 阿部 寛:「古典的数式処理プログラムMACSYMAとその今日への継承」、柏艪舎、ISBN 978-4-434-18980-7、（2014年3月）。
  - 山下 章夫：「Maximaによる経済分析」、晃洋書房、ISBN 978-4771025875（2014/10/1）。
  - 上田 晴彦：「Maximaで学ぶ解析力学」、工学社 (I・O BOOKS)、ISBN 978-4777519460（2016年4月）。
  - 梅野 善雄：「いつでも・どこでも・スマホで数学\! Maxima on Android活用マニュアル」、森北出版、ISBN 978-4627012011 (2017年12月19日)。
  - Dr M Kanagasabapathy: "Introduction to wxMaxima for Scientific Computations", BPB PUBLICATIONS, ISBN 978-9387284425 (June 12, 2018).

[Category:数式処理システム](https://ja.wikipedia.org/wiki/Category:数式処理システム "wikilink") [Category:Linux向け数式処理システム](https://ja.wikipedia.org/wiki/Category:Linux向け数式処理システム "wikilink") [Category:フリー教育ソフトウェア](https://ja.wikipedia.org/wiki/Category:フリー教育ソフトウェア "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  [竹内薫](../Page/竹内薫.md "wikilink")2007『はじめての数式処理ソフト---Maximaで楽しむ数式計算と物理グラフィック』[講談社](../Page/講談社.md "wikilink"):21-2