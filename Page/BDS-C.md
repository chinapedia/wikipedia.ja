> この記事は[BDS-C](https://ja.wikipedia.org/wiki/BDS-C)から翻訳されています。


**BDS-C**は、BD Software製の[8080](../Page/Intel_8080.md "wikilink")/[Z80](../Page/Z80.md "wikilink")用の[C言語](../Page/C言語.md "wikilink")処理系（[コンパイラ](../Page/コンパイラ.md "wikilink")）である。同社を設立したレオ・ゾルマン（Leor Zolman）が[1979年](../Page/1979年.md "wikilink")に開発した。

## 概要

[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")-80上で稼動し、[K\&R時代のC言語仕様のやや方言を伴うサブセットとして実装されている](https://ja.wikipedia.org/wiki/プログラミング言語C "wikilink")。米国ライフボート社から世界的に販売されたが、日本では初期のバージョンおよび完成度を高めたVer.1.5が一部の愛好家に知られたものの、一般的には[サブセット](https://ja.wikipedia.org/wiki/サブセット "wikilink")としてライフボート社（日本法人）から発売されたα-Cの方がメジャーだった（BDS社によれば、BDS-Cは世界で約25,000セット、α-Cは日本で約50,000セットが出荷された）。BD Software社の販売価格は$110、日本での販売価格は6万円と、当時の同クラスのコンパイラに比して非常に安価であったのも成功の理由である。なお、BDはレオのMIT時代のニックネーム"Brain Damaged"(脳障害）から付けたというが、現在は名前の由来に関しての説明は、BD Software側で回避している。

## 特徴

2.5～4MHzのZ80が主流であった1980年代初期の8ビット[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")の乏しいハードウェア資源を考慮し、少ない[メインメモリと](https://ja.wikipedia.org/wiki/主記憶 "wikilink")[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")で稼動した。コンパイラは前半・後半に分かれて実行されたが、それらの間の受け渡しは一般的な手法であるFD上に中間ファイルを生成することを避け、メモリ上に中間コードを置いて直接渡すなどの工夫により、高速なコンパイル・リンクが可能だった。その代償として余り大きなモジュールをコンパイルすることは不可能だったが、実用上は支障はそれほど見られなかった。

当初は標準ヘッダやライブラリが非互換で、とくにファイルディスクリプタが独特のため、K\&Rのサンプルプログラムもそのままでは実行できないものであったが、Ver. 1.5以降は標準的な入出力関数（fputc、fprintfなど）が、一般的な引数を用いて利用できるようになった。

実行速度は当時最速といわれたLSI-C80はもちろん、最適化を効かせたWhitesmith Cなどには及ばなかったものの、プログラム入門から小規模なツール開発などには充分な効率と実行速度が得られ、コンパイル・リンクに要する時間の短さとあいまって、C言語の入門用として評価が高かった。

BDS-C/α-Cはfloat型やdouble型に対応していなかったため、実用的なアプリケーションの作成には向いていないという弱点があった。そのため、関数呼び出しの形で実行する[浮動小数点](https://ja.wikipedia.org/wiki/浮動小数点 "wikilink")演算[ライブラリ](../Page/ライブラリ.md "wikilink")が多数開発・配布されていた。BDS-C/α-Cに対応した解説書も多数出版されており、[CP/M](https://ja.wikipedia.org/wiki/CP/M "wikilink")におけるC言語の草分け的存在といえる。

BDS-Cは現在、BD Software社のサイトからパブリックドメインで提供されている。

## αシリーズについて

ライフボート社はαシリーズとして多数のプログラミング言語パッケージを販売しており、[ライブラリ](../Page/ライブラリ.md "wikilink")レベルで相互に互換性を持たせていた。例えばα-[FORTRAN](../Page/FORTRAN.md "wikilink")（FORTRAN 66相当）で浮動小数点を含む数値計算を行い、α-Cで作成した実行制御およびハードウェア制御ルーチンをライブラリとしてリンクするといった、マルチ言語プログラミングを可能としていた。この機能を実現する上で、マクロアセンブラM80およびリンカL80の働きは大きい。

αシリーズの言語としては、α-C、α-FORTRAN、α-[PASCAL](../Page/Pascal.md "wikilink")、α-[COBOL](../Page/COBOL.md "wikilink")、α-[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、α-[FORTH](../Page/Forth.md "wikilink")、α-[APL](../Page/APL.md "wikilink")、α-[PROLOGがシリーズ展開されていた](https://ja.wikipedia.org/wiki/Prolog "wikilink")。

## 外部リンク

  - [BD Software](http://www.bdsoft.com/index.html)
  - [BDS-Cダウンロード](http://www.bdsoft.com/resources/bdsc.html)

[Category:フリーコンパイラとフリーインタプリタ](https://ja.wikipedia.org/wiki/Category:フリーコンパイラとフリーインタプリタ "wikilink") [Category:Cコンパイラ](https://ja.wikipedia.org/wiki/Category:Cコンパイラ "wikilink")