> この記事は[PdfTeX](https://ja.wikipedia.org/wiki/PdfTeX)から翻訳されています。


**pdf** (**pdfTeX**) は、[](../Page/TeX.md "wikilink") から派生した[組版](../Page/組版.md "wikilink")処理ソフトウェアである。<span style="font-variant: small-caps">Hàn</span> Thế Thành が開発した。 と pdf の一番の違いは、 が [DVI](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink") ファイルを出力するのに対して、pdf が [PDF](../Page/Portable_Document_Format.md "wikilink") ファイルを直接出力する点である。PDF と密に連携できるため、[ハイパーテキスト](../Page/ハイパーテキスト.md "wikilink")リンクや目次といった機能が使用でき、[hyperref](https://ja.wikipedia.org/wiki/hyperref "wikilink") のようなパッケージを使える。一方で DVI から [PostScript](../Page/PostScript.md "wikilink") への変換過程で使える [PSTricks](https://ja.wikipedia.org/wiki/PSTricks "wikilink") のようなパッケージとは連携できないが、同様の機能を持つ [pdftricks](https://ja.wikipedia.org/wiki/pdftricks "wikilink") が作られている。

pdf から DVI 出力を得ることも可能である。この DVI 出力は  と基本的には同じだが、pdf 独自のマイクロ組版機能が有効になっていると異なった出力となる。さらに、[](../Page/LaTeX.md "wikilink") や [](https://ja.wikipedia.org/wiki/ConTeXt "wikilink") などといったソフトウェアは  のための単純な[マクロパッケージであるため](https://ja.wikipedia.org/wiki/マクロ_\(コンピュータ用語\) "wikilink")、pdf とも連携可能である。`pdflatex` では、標準的な  マクロを使った文書について pdf プログラムが呼び出されて組版処理が行われる。

## 機能

pdf には以下のような標準の  には無い機能がある。なお、[日本語](../Page/日本語.md "wikilink")は正式にはサポートされていないため、日本語を扱うには工夫が必要となる。

  - ネイティブ [TrueType](../Page/TrueType.md "wikilink") と Type 1 フォントの埋め込み
  - フォントの幅を調整することによる字間調整などの微細な組版処理
  - ハイパーリンク・目次・文書情報といった PDF 固有機能への直接アクセス

## 外部リンク

  - [pdf —  Users Group](http://www.pdftex.org/)
  - [PRAGMA ADE web page: text](http://www.pragma-ade.nl/)
      - [Micro-typographic extensions to the  typesetting system](http://www.pragma-ade.nl/pdftex/thesis.pdf) ([PDF](../Page/Portable_Document_Format.md "wikilink")) ……<span style="font-variant: small-caps">Hàn</span> Thế Thành による学位論文
  - [the Comprehensive  Archive Network](http://www.ctan.org/) ([CTAN](https://ja.wikipedia.org/wiki/CTAN "wikilink"))
      - [The  Catalogue OnLine, Entry for pdf, Ctan Edition](http://www.ctan.org/get/help/Catalogue/entries/pdftex.html)（[Ring Server によるミラーリング](http://www.ring.gr.jp/pub/text/CTAN/help/Catalogue/entries/pdftex.html)）
  - [Sarovar.org](http://sarovar.org/)
      - [Sarovar.org: pdf: Project Info](http://sarovar.org/projects/pdftex/)

[Category:PDFソフト](https://ja.wikipedia.org/wiki/Category:PDFソフト "wikilink") [Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")