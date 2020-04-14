> この記事は[Oz \(プログラミング言語\)](https://ja.wikipedia.org/wiki/Oz_\(プログラミング言語\))から翻訳されています。


**Oz** は、[ザールラント大学](https://ja.wikipedia.org/wiki/ザールラント大学 "wikilink") Programming Systems Lab で開発された[マルチパラダイム型プログラミング言語である](https://ja.wikipedia.org/wiki/マルチパラダイムプログラミング言語 "wikilink")。

## 歴史

[1991年](../Page/1991年.md "wikilink")、Gert Smolka が学生らと共に設計したのが最初である。[1996年](../Page/1996年.md "wikilink")、Oz の開発はスウェーデン計算機科学研究所の Seif Haridi の研究グループの協力で続けられた。[1999年](../Page/1999年.md "wikilink")以降、Oz の開発は *Mozart Consortium* という国際的グループによって続けられている。*Mozart Consotium* には、ザールラント大学とスウェーデン計算機科学研究所のほかに、[ルーヴァン・カトリック大学](../Page/ルーヴァン・カトリック大学.md "wikilink")も当初から参加している。[2005年](../Page/2005年.md "wikilink")、Oz 処理系である [Mozartプログラミングシステム](https://ja.wikipedia.org/wiki/Mozartプログラミングシステム "wikilink") の開発を管理する Mozart Board が設けられ、Mozart の開発をより大きなコミュニティで行う用意が整った。

## 処理系

Oz の高品質な実装として [Mozartプログラミングシステム](https://ja.wikipedia.org/wiki/Mozartプログラミングシステム "wikilink") がある。これは[オープンソース](../Page/オープンソース.md "wikilink")で Mozart Consortium からリリースされている。Mozart は、[Unix系](../Page/Unix系.md "wikilink")オペレーティングシステム、[FreeBSD](../Page/FreeBSD.md "wikilink")、[Linux](../Page/Linux.md "wikilink")、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") などに移植されている。

## 言語の特徴

Oz は主要な[プログラミングパラダイム](../Page/プログラミングパラダイム.md "wikilink")の概念を単純かつ巧妙に取り入れており、論理型の拡張である[並行制約プログラミング](https://ja.wikipedia.org/wiki/並行制約プログラミング "wikilink")をベースに、[関数型](https://ja.wikipedia.org/wiki/関数型プログラミング言語 "wikilink")（[遅延評価](../Page/遅延評価.md "wikilink")も、[先行評価](https://ja.wikipedia.org/wiki/先行評価 "wikilink")も）、命令型、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")、分散といった要素が含まれている。Oz の[形式意味論は単純で](../Page/プログラム意味論.md "wikilink")、実装（[Mozartプログラミングシステム](https://ja.wikipedia.org/wiki/Mozartプログラミングシステム "wikilink")）は効率が良い。Oz は[並行性](../Page/並行性.md "wikilink")指向言語とも呼ばれる（この名付け親は[Erlang](../Page/Erlang.md "wikilink")の主要設計者 Joe Armstrong）。並行性指向言語は並行性を容易かつ効率的に実現できる。

単なるマルチパラダイム言語というだけでなく、Oz の利点は[制約プログラミング](../Page/制約プログラミング.md "wikilink")と[分散プログラミングにある](../Page/分散コンピューティング.md "wikilink")。Oz はネットワーク[透過な分散プログラミングモデルを実装できる](../Page/透過性_\(情報工学\).md "wikilink")。このモデルにより、[フォールトトレラントアプリケーションを容易に書ける](../Page/フォールトトレラント設計.md "wikilink")。制約プログラミングのために Oz は 「計算空間; computation space」という考え方を導入している。これにより、制約領域に対して直交するユーザー定義の検索・分散戦略を実施できる。

## 参考文献

  - Peter Van Roy and Seif Haridi (2004). *Concepts, Techniques, and Models of Computer Programming*. MIT Press. 同書の [オンライン関連資料](http://www.info.ucl.ac.be/~pvr/book.html)。Oz を例として、プログラミング言語の基本原則を解説した教科書的書籍
  - ピーター・ヴァン・ロイ、セイフ・ハリディ、羽永洋(訳) 、『[コンピュータプログラミングの概念・技法・モデル](../Page/コンピュータプログラミングの概念・技法・モデル.md "wikilink")』、[翔泳社](../Page/翔泳社.md "wikilink")、2007年、ISBN 978-4-7981-1346-3 上記書の日本語訳

## 関連項目

  - [Mozartプログラミングシステム](https://ja.wikipedia.org/wiki/Mozartプログラミングシステム "wikilink")
  - 『[コンピュータプログラミングの概念・技法・モデル](../Page/コンピュータプログラミングの概念・技法・モデル.md "wikilink")』
  - [Alice](https://ja.wikipedia.org/wiki/:en:Alice_\(programming_language\) "wikilink") - 並行/関数/制約プログラミング言語（ザールラント大学）。当初 Mozart/Oz の VM 上で動作した。

## 外部リンク

  - [The Mozart Programming System](http://mozart.github.io/)
  - [Tutorial of Oz](http://www.mozart-oz.org/documentation/tutorial/) [和訳](http://e-p-i.github.com/tutorial_of_oz/)
  - [Open Directory: Oz](http://dmoz.org/Computers/Programming/Languages/Oz/)
  - [Programming Language Research at UCL](http://www.info.ucl.ac.be/people/PVR/distribution.html) Mozart/Oz の主要な開発元の1つ
  - [*Multiparadigm Programming in Mozart/Oz: Proceedings of MOZ 2004*](http://www.informatik.uni-trier.de/~ley/db/conf/moz/moz2004.html) Mozart/OZ に関する国際会議

[Category:論理プログラミング言語](https://ja.wikipedia.org/wiki/Category:論理プログラミング言語 "wikilink") [Category:関数型言語](https://ja.wikipedia.org/wiki/Category:関数型言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")