> この記事は[CPL \(プログラミング言語\)](https://ja.wikipedia.org/wiki/CPL_\(プログラミング言語\))から翻訳されています。


**CPL**（Combined Programming Language、「統合プログラミング言語」の意）は、[C言語](../Page/C言語.md "wikilink")の遠い祖先となった古いプログラミング言語である。

たとえば、C言語でブロックを表す{・・・}の表記は、ブロックの区切りを単語ではなく記号で表すという点でCPLの影響を受けており、ブロックの区切り記号は以下のような変遷を経ている。

CPL(1963年): § → BCPL初版(1967年): $(・・・$) → BCPL TX-2版(1967年?): {・・・} → B言語(1969年): {・・・} → C言語(1972年): {・・・}

## 概要

CPL\[1\]は[ケンブリッジ大学](../Page/ケンブリッジ大学.md "wikilink")の数学研究所と[ロンドン大学](../Page/ロンドン大学.md "wikilink")コンピュータ部の共同プロジェクトとして[1960年代](../Page/1960年代.md "wikilink")に開発された。言語の名前にある「統合」は共同開発であることを表している（当初はケンブリッジプログラミング言語(Cambridge Programming Language)という名前であった）。[クリストファー・ストレイチー](https://ja.wikipedia.org/wiki/クリストファー・ストレイチー "wikilink")が関与していた（その他の人は論文を参照のこと）。論文が出版された[1963年](../Page/1963年.md "wikilink")の時点でケンブリッジの[タイタンコンピュータとロンドンの](https://ja.wikipedia.org/wiki/:en:Titan_\(computer\) "wikilink")[アトラスコンピュータに実装されていた](https://ja.wikipedia.org/wiki/:en:Atlas_Computer_\(Manchester\) "wikilink")。

[ALGOL](../Page/ALGOL.md "wikilink") 60の影響を強く受けていたが、ALGOLがコンパクトでエレガントでシンプルであったのに対し、CPLは巨大で、それなりにエレガントで、複雑だった。CPLは（[FORTRAN](../Page/FORTRAN.md "wikilink")やALGOL方式の）科学的プログラミングと、([COBOL](../Page/COBOL.md "wikilink")方式の）商用プログラミングの両方で優れていることを目指していた。同様の努力は[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")でも見られた。

CPLは当時のコンピュータが非力で[コンパイラ](../Page/コンパイラ.md "wikilink")技術も未熟であったことを明白にした。実用的なCPLコンパイラは恐らく1970年頃に作られた\[2\]が、全く普及することなく、[1970年代](../Page/1970年代.md "wikilink")に自然消滅した。

CPLをベースにした[BCPL](../Page/BCPL.md "wikilink")（Basic CPL、元々はBootstrap CPL）という後発の言語は特にコンパイラを記述することを目的とした比較的シンプルな[システム記述用言語](https://ja.wikipedia.org/wiki/システム記述用言語 "wikilink")であった。後にBCPLは[B言語](../Page/B言語.md "wikilink")となり、今日最も重要な[プログラミング言語](../Page/プログラミング言語.md "wikilink")の1つである[C言語](../Page/C言語.md "wikilink")の元になった。

## コードの例

ピーター・ノーヴィグが記述したMAX関数:\[3\]

    Max(Items, ValueFunction) = value of
    § (Best, BestVal) = (NIL, -∞)
    while Items do §
    (Item, Val) = (Head(Items), ValueFunction(Head(Items)))
    if Val > BestVal then (Best, BestVal) := (Item, Val)
    Items := Rest(Items) §⃒
    result is Best §⃒

(開始シンボル"§"に対応した終了シンボル"§⃒"は縦線が含まれたものである。このシンボルはUnicodeでは"§⃒"となるが、これは§(U+00A7, SECTION SIGN) と ⃒ (U+20D2, 縦棒の重ね合わせ)であり、ブラウザ上では正しく表示されないものと思われる。)

## 脚注

## 関連項目

  - [BCPL](../Page/BCPL.md "wikilink") - [B言語](../Page/B言語.md "wikilink") - [C言語](../Page/C言語.md "wikilink")

## 参考文献

"The main features of CPL" by D.W. Barron, J.N. Buxton, D.F. Hartley, E. Nixon, and C. Strachey. The Computer Journal, volume 6, issue 2, pp.134-143 (1963).

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.
2.
3.