> この記事は[Dvips](https://ja.wikipedia.org/wiki/Dvips)から翻訳されています。


**dvips** は [](../Page/TeX.md "wikilink") の **DeVice-Independent**（デバイス非依存）なファイル形式 [DVI](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink") から印刷可能な [PostScript](../Page/PostScript.md "wikilink") 形式に変換するために、今日広く使用されているプログラムである。作者は Tomas Rokicki。

は組版結果を DVI形式で出力する。この DVIファイルを[プリンター](https://ja.wikipedia.org/wiki/プリンター "wikilink")が直接取り扱うことはなく、そしてこのファイルには[フォント](../Page/フォント.md "wikilink")の[グリフ](https://ja.wikipedia.org/wiki/グリフ "wikilink")などの情報は含まれていない。したがって、印刷や画面表示などを行う場合は変換プログラムで DVI形式からプリンター言語やビットマップ画像に変換する必要がある。これらの変換を行うソフトウェアを DVIドライバという。

dvips はプリンタが直接理解できるような PostScript を出力する DVIドライバの中で最も有名なものの1つである。dvips の生成する PostScript はサイズが小さく、プリンタのメモリ消費量も比較的少ない。また、 の`\special`コマンドや仮想フォントなどの拡張を幅広く理解できることも特徴である。 `\special`コマンドは DVIファイルを拡張するために用意されたコマンドであり、このコマンドを用いてPostScriptコードの埋め込みや取り込み、[色](../Page/色.md "wikilink")に関する処理などが行われる。dvips は色などの基本的な`\special`コマンドの他に [MetaPost](../Page/MetaPost.md "wikilink"), emTeX, tpic, [PSTricks](../Page/PSTricks.md "wikilink") といったグラフィックパッケージが生成する拡張された`\special`コマンドにも対応している。

PostScript を生成する同種のDVIドライバとしては、dvi2ps, dvipsone などがあるが、グラフィックパッケージの対応状況や対応フォントの広さから今日では dvips が標準的な地位にある。こういった事情から dvips はほとんどの /  ディストリビューションで標準配布のパッケージ一式の中に含められている。

dvips に[パッチ](../Page/パッチ.md "wikilink")を当てて機能を拡張したものもしばしば配布される。このような機能拡張版はコマンド名やバナーに元の dvips との違いを見てとることができ、たとえば  のフォントサーチ機構 (**k**pathsea) に対応させるパッチを当てた dvips は dvipsk という名前でいくつかの  のディストリビューションの標準配布に含まれている（dvips, dvipsk がともに含まれている配布も少なくない）。他にも[ローカライゼーション](https://ja.wikipedia.org/wiki/ローカライゼーション "wikilink")のための変更を加えることもよくあり、日本では dvips の日本語化パッチを当て [](../Page/Publishing_TeX.md "wikilink") に対応したものが知られるが、コマンド名としては dvips, dvipsk, pdvips など配布元によっていくつか異なるものがある。また、[PDF](../Page/Portable_Document_Format.md "wikilink") 形式へ変換するために、いったん dvips でPostScriptを出力した後に [Distiller](../Page/Adobe_Acrobat.md "wikilink") や [Ghostscript](../Page/Ghostscript.md "wikilink") などで変換して PDF形式を得るという使い方もよくなされている（[dvipdfm](https://ja.wikipedia.org/wiki/dvipdfm "wikilink")(x) というプログラムを用いて DVIファイルから直接 PDF形式を得ることも多い）。

## 外部リンク

  - [dvips 本家](http://www.tug.org/dvips/)（英語版）

[Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:PostScript](https://ja.wikipedia.org/wiki/Category:PostScript "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")