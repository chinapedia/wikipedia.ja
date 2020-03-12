> この記事は[LaTeX](https://ja.wikipedia.org/wiki/LaTeX)から翻訳されています。


****（ラテック、ラテフ）とは、[レスリー・ランポート](../Page/レスリー・ランポート.md "wikilink")によって開発されたテキストベースの[組版](../Page/組版.md "wikilink")処理システムである。電子組版ソフトウェア [](../Page/TeX.md "wikilink") にマクロパッケージを組み込むことによって構築されており、単体の  に比べて、より手軽に組版を行うことができるようになっている。[middle](https://ja.wikipedia.org/wiki/画像:LaTeX_logo.svg "wikilink") と表記できない場合は“LaTeX”と表記する。

なお、 を基に[アスキーが](../Page/アスキー_\(企業\).md "wikilink")[日本語](../Page/日本語.md "wikilink")処理に対応させたものとして**日本語 ** が、さらに[縦組み](https://ja.wikipedia.org/wiki/縦組み "wikilink")処理にも対応させたものとして **[](../Page/Publishing_TeX.md "wikilink")** がある。

専門分野にもよるが、学術機関においては標準的な論文執筆ツールとして扱われている。 [LaTeX_diagram.svg](https://ja.wikipedia.org/wiki/File:LaTeX_diagram.svg "fig:LaTeX_diagram.svg")

## 読み方

の生みの親[レスリー・ランポート](../Page/レスリー・ランポート.md "wikilink")は、“”の発音について自著の中で、

と述べている\[1\]。日本語では「ラテック」あるいは「ラテフ」と呼ばれることが多い。

## 成立の背景と開発者

以前に、“[](../Page/TeX.md "wikilink")”という名の数式の処理に優れる組版ソフトウェアがあり、その  を使ってもっと簡単に論文やレポートを作成したいという要望があった。 はその要望に応えて開発されたものであり、レスリー・ランポートが  の上にマクロパッケージを組み込むことで構築したものである。さらに  では、 の煩雑な部分の修正も行っている（たとえば、[累乗根](https://ja.wikipedia.org/wiki/累乗根 "wikilink")や[分数](../Page/分数.md "wikilink")の設定方法など）。また  やそれを基にした  は主に[米国での表記法を基に作られたもので](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")、日本の[初等教育](../Page/初等教育.md "wikilink")・[中等教育](../Page/中等教育.md "wikilink")での数式の書き方とは一部異なる\[2\]\[3\]。例を挙げれば、日本の初等教育・中等教育では[等号附き不等号として](../Page/不等号.md "wikilink")、「≦」と「≧」が、近似記号として「≒」が、[相似記号](https://ja.wikipedia.org/wiki/相似記号 "wikilink")として「」が用いられる。一方で  や  の標準では、等号附き不等号として「\(\le\)」（`\leq` または `\le`）と「\(\ge\)」（`\geq` または `\ge`）が、近似記号として「\(\approx\)」(`\approx`) や「\(\sim\)」(`\sim`)が、相似記号として「\(\sim\)」(`\sim`) が用いられる。日本で使われる記号を使う必要がある場合は、amssymb パッケージを用いることで「\(\leqq\)」(`\leqq`)、「\(\geqq\)」(`\geqq`)、「\(\fallingdotseq\)」(`\fallingdotseq`) が使用できる。

## 動作環境と各種バージョン

ソフトウェアは、 (LPPL)\[4\]に規定された[ライセンス](../Page/ライセンス.md "wikilink")で提供された[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。現在、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") や [Solaris](../Page/Solaris.md "wikilink") などの [UNIX](../Page/UNIX.md "wikilink")、[Linux OS](../Page/Linux.md "wikilink") や [BSD 系 OS](../Page/BSDの子孫.md "wikilink") や [OpenSolaris](../Page/OpenSolaris.md "wikilink") などの [UNIX 互換](../Page/Unix系.md "wikilink") OS、そして [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") など、多くの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")上で利用できる。

現在使われているバージョンは （ラテック・トゥー・イー） である。組版処理による表記ができない[プレーンテキスト](../Page/プレーンテキスト.md "wikilink")や[電子メール](../Page/電子メール.md "wikilink")などの場合には“LaTeX2e”と表記する。古い  2.09 を利用している場合には、 への更新が推奨されている。

  - [1993年](../Page/1993年.md "wikilink")、 の新版である  がリリースされた。
  - [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、日本語  (p) がリリースされた。

なお、「p」は[株式会社アスキーの](../Page/アスキー_\(企業\).md "wikilink")[登録商標](https://ja.wikipedia.org/wiki/登録商標 "wikilink")であり、「ピーラテックツーイー」と読むのが正しいとされている。

## 特徴

での文書作成と一般的な[ワープロソフト](../Page/ワープロソフト.md "wikilink")での文書作成を比べると以下のような特徴が見られる。

  - ファイル作成時に記述するファイル形式と閲覧ファイル形式が異なる。
      - [ソースコード](../Page/ソースコード.md "wikilink")を作成して[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")\[5\]を行うことで、初めて [DVI](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink")\[6\] や [PDF](../Page/Portable_Document_Format.md "wikilink")\[7\] のような閲覧用のファイルを得ることができる。
      - 一度コンパイルを行わないとどういった出力が得られるかがわかりにくい。
      - ソースコードをインクルード\[8\]することで、過去の文章を簡単に再利用できる。また、大規模な文書の場合に作業を分割して並行作業することが容易である。
      - 一般的な[プログラミング言語](../Page/プログラミング言語.md "wikilink")における[ライブラリ](../Page/ライブラリ.md "wikilink")に当たる、スタイルファイルを用いることで文書の表現力を拡張しやすい。
      - [Perl](../Page/Perl.md "wikilink") や [Lua](../Page/Lua.md "wikilink") などのプログラミング言語と連携させることがワープロソフトで作成されたファイルと比べて容易である。
  - 組版性能が高い。[DTP](../Page/DTP.md "wikilink") システムとして使用するものもいる。
      - 一般向けの[出版](../Page/出版.md "wikilink")物の作成にも充分に耐えられるものであり、実際の出版例もある\[9\]。
      - 数式の入力のためのコマンドが豊富に組み込まれており行いやすい。更に数式組版の性能は特に高い。
  - [GUIベースのワープロソフトと比べると](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、CUIの操作やソースコード作成に関する知識が必要となる点で、コンピュータ初心者はハードルが高いと感じることが多い。
  - しかし、文書のページ数が増えてくると、画面出力の全てを自動化した[ソースコード](../Page/ソースコード.md "wikilink")作成による組版と比較して、[GUI経由で文書のページを](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")1枚毎に手作業で調整する組版は飛躍的に非効率になる。[ソースコード](../Page/ソースコード.md "wikilink")作成方式では、文書のページ数が幾ら膨大であっても、事前に文書スタイルさえ定義されていれば、[CUI上のコマンド入力で一括して全てを組版することが可能である](../Page/キャラクタユーザインタフェース.md "wikilink")。従って、コンピュータ上の作業自動化のメリットを知っている[研究者](https://ja.wikipedia.org/wiki/学者 "wikilink")・[技術者](../Page/技術者.md "wikilink")からの受けは良い。

数式組版性能が非常に高いという特徴から、自然科学・応用科学系の中でも数学を多用する分野では学会提出の資料の標準形式として広く用いられている。雑誌に掲載するための体裁を整えた[テンプレート](../Page/テンプレート.md "wikilink")の配布を行っている学会もある\[10\]。一方で化学式を多用する分野では [Word](../Page/Microsoft_Word.md "wikilink") 形式を奨励し、 の使用は一般的でないことがある\[11\]。

## 入力と出力の具体例

以下は  用の入力の例\[12\]。

``` latex
\documentclass[12pt]{article}
\title{\LaTeX}
\date{}
\begin{document}
\maketitle \LaTeX{} is a document preparation system for the \TeX{}
typesetting program. It offers programmable desktop publishing
features and extensive facilities for automating most aspects of
typesetting and desktop publishing, including numbering and
cross-referencing, tables and figures, page layout, bibliographies,
and much more. \LaTeX{} was originally written in 1984 by Leslie
Lamport and has become the dominant method for using \TeX; few
people write in plain \TeX{} anymore. The current version is
\LaTeXe.
\newline
% This is a comment, it is not shown in the final output.
% The following shows a little of the typesetting power of LaTeX
\begin{eqnarray}
E &=& mc^2                              \\
m &=& \frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}}
\end{eqnarray}
\end{document}
```

上記の[ソースコード](../Page/ソースコード.md "wikilink")を  で処理することで、以下のような出力が得られる。

[LaTeX_Output.svg](https://ja.wikipedia.org/wiki/File:LaTeX_Output.svg "fig:LaTeX_Output.svg")

## 脚注

### 補足

### 出典

## 参考文献

  -
## 関連項目

  - [数式エディタ](https://ja.wikipedia.org/wiki/数式エディタ "wikilink")
  - [MathJax](https://ja.wikipedia.org/wiki/MathJax "wikilink")

## 外部リンク

  - [CTAN: Comprehensive  Archive Network](http://www.ctan.org/)

  -

  - [ Wiki](https://texwiki.texjp.org/)  ・ に関する Wiki

  - [MyTeXpert](http://mytexpert.sourceforge.jp/index.php?FrontPage)

      - [myTeXpert プロジェクト日本語トップページ](http://sourceforge.jp/projects/mytexpert/)

  - [T. Yoshinaga's LaTeX page](http://www.h4.dion.ne.jp/~latexcat/index.html)

      -

  - [LaTeXの家](http://www.okomeda.net/?LaTeX%E3%81%AE%E5%AE%B6)

  - [pLaTeX for Windows](http://www9.oninet.ne.jp/ohishi/tex/index.html)

  - Web 上で  を用いて数式の画像を生成できる

  - [らすてすでいこう](http://www.geocities.co.jp/HeartLand-Poplar/1240/)

      - [てふますたーへの道](http://www.geocities.co.jp/HeartLand-Poplar/1240/latex/menu.html)

  - [Cloud LaTeX](https://cloudlatex.io)[株式会社アカリクが運営する](../Page/アカリク.md "wikilink")、Web 上で  をコンパイルできるサービス

  - [MOEDITOR](https://moeditor.js.org/) とMarkdown(簡単に見出しなどのレイアウトを変えられる機能)を融合したエディタ

  - [Google Colaboratory](https://colab.research.google.com/notebooks/welcome.ipynb) とPythonをWeb上で使えるサービス

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink") [Category:1984年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1984年のソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  Leslie Lamport『文書処理システム 』・倉沢良一 監訳、大野俊治・小暮博道・藤浦はる美 訳、アスキー、1990年、5頁、ISBN 978-4-7561-0784-8.
2.  日本の初等教育・中等教育での数式表記は [JIS Z 8201](https://ja.wikipedia.org/wiki/JIS_Z_8201 "wikilink") を基準にしている。[2006年](../Page/2006年.md "wikilink")[1月20日](../Page/1月20日.md "wikilink")に確認が行われている JIS Z 8201-1981 (JIS Z 8201:1981) と国際標準である [ISO 31-11](https://ja.wikipedia.org/wiki/ISO_31-11 "wikilink"):1992 とでは、表記が一部異なっている。
3.  日本の初等教育・中等教育での数式用に記号の形を調整するマクロとして、初等数学プリント作成マクロ [emath](https://ja.wikipedia.org/wiki/emath "wikilink") がある。
4.  [](http://www.latex-project.org/lppl/)
5.  ソースコードを DVI などの文書ファイル形式に変換すること。
6.  [Microsoft Word](../Page/Microsoft_Word.md "wikilink") でしか開くことができなかった doc ファイルなどとは異なり、処理系に依存しないとされるファイル形式。
7.  処理系に依存しない標準規格。
8.  他のソースコードの記述を自動的に読み込む仕組み。
9.  [ で作られた本 — ](https://texwiki.texjp.org/?TeXで作られた本)
10. 例えば[日本数学会](http://mathsoc.jp/meeting/texstyle/)や[電子情報通信学会](http://www.ieice.org/ftp/)
11. [](https://ja.wikipedia.org/wiki/XyMTeX "wikilink") や [mhchem](https://ja.wikipedia.org/wiki/mhchem "wikilink") といったパッケージを利用すれば書ける。
12. [ScienceSoft — LaTeX](http://sciencesoft.at/latex/index?lang=en)