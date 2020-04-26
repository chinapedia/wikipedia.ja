> この記事は[BLISS](https://ja.wikipedia.org/wiki/BLISS)から翻訳されています。


**BLISS** は[1970年](../Page/1970年.md "wikilink")ごろ、[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")の W. A. Wolf、D. B. Russel、A. N. Habermann が開発したシステム用[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。数年後に[C言語](../Page/C言語.md "wikilink")が登場するまでは、システム記述に最も適した言語とされていたが、C言語に取って代わられた。C言語が登場した当初、[ベル研究所](../Page/ベル研究所.md "wikilink")では BLISS と C のどちらがよいかという議論が行われた。

BLISS は[データ型](../Page/データ型.md "wikilink")のないブロック構造方式の言語であり、文ではなく式を基本構成要素とし、[例外処理](../Page/例外処理.md "wikilink")構文、[コルーチン](../Page/コルーチン.md "wikilink")構文、[マクロなどを備えている](../Page/マクロ_\(コンピュータ用語\).md "wikilink")。[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")は持たない。

その名称の由来には諸説あり、"Basic Language for Implementation of System Software" の略だとか "System Software Implementation Language, Backwards" の略（書かれている通りに逆転させる）だとか言われている。開発者の Bill Wolf の名前から "Bill's Language for Implementing System Software" とも言われる。

カーネギーメロンで開発された[コンパイラ](../Page/コンパイラ.md "wikilink")は[最適化を多用していることで知られ](../Page/コンパイラ最適化.md "wikilink")、その開発を元に古典的著作 *The Design of an Optimizing Compiler* が生まれた。

[DECは](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")、[PDP-10](../Page/PDP-10.md "wikilink")、[PDP-11](../Page/PDP-11.md "wikilink")、[DEC Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、[Itanium](../Page/Itanium.md "wikilink")、[VAX](../Page/VAX.md "wikilink") 向けにBLISSコンパイラを開発しており、[1980年代](../Page/1980年代.md "wikilink")には社内でも多用していた。[VMS](../Page/OpenVMS.md "wikilink") [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")のユーティリティプログラムの多くは BLISS-32 で書かれていた。

## 概要

以下の記述は、DECが1987年に出版した [Bliss Language Manual](http://63.249.85.132/langs/bliss/bliss.pdf)（注意: PDF形式で968KB）にあるもの（を翻訳したもの）である。

  -
    BLISS には他の高級言語に見られるような様々な機能がある。ブロック構造、自動スタック、再帰ルーチンを定義し呼び出す機構などがある。…事前に定義された様々なデータ構造も提供している… また、評価のためのファシリティ…
    一方、BLISS は他の高級言語が持つある機能を省いている。[システムソフトウェア](../Page/システムソフトウェア.md "wikilink")開発においては入出力機能は自前で開発するのが普通であるため、BLISS は入出力に関する組み込み機能を持たない。また、システムソフトウェアの記述に必要なマシン固有の機能へのアクセスを許している。BLISS は他の高級言語にはない特徴を持っている。名前は…セグメント内の値ではなく、セグメント内のアドレスに変換される。…また、BLISS は "statement language" というよりも " expression language" である。
    すなわち、宣言以外の言語の各構成要素は全て式である。式には値があり、その中でメモリの更新や制御の転送やループ実行といった動作も可能である。例えば、一般的な代入文を BLISS で表した場合も、厳密に言えば値を持つ式になっている。式の値は BLISS では使うこともあるし捨てることもある… 最後に BLISS はマクロアセンブラにあるような機能を提供するマクロファシリティを含んでいる。

定数には必ず、そのマシンのフルワード長が使われる。例えば、[PDP-11](../Page/PDP-11.md "wikilink")のような16ビットマシンなら、定数は16ビットである。[VAX](../Page/VAX.md "wikilink")では、定数は32ビットとなり、[PDP-10](../Page/PDP-10.md "wikilink")では36ビットとなる。

変数の参照は常にその変数のアドレスとなる。例えば、`Z+8` という命令は、Z の「アドレス」に 8 を加えることを意味し、「値」への加算ではない。Z の「値」に 8 を加算したい場合、変数名の前にピリオドを付け、`.Z+8` としなければならない。

代入は = 記号で行われる。例えば `Z=8` と書けば、8 を格納したフルワード定数が生成され、それが Z に対応したアドレス位置に格納される。従って、`Z+12=14`（あるいは `12+Z=14`）と書いた場合、定数 14 を Z のアドレスに12を加えた位置に置くことになる（悪い書き方の例）。

ブロックは [ALGOL](../Page/ALGOL.md "wikilink") のものと似た構文であり、BEGIN と END で囲まれた部分がブロックとなる。文はALGOLと同様、セミコロン ";" で区切られる。文（式）の値が計算されると、それが次の文の終端まで保持される。つまり、計算されたり代入されたりした値は次の文の評価中も保持される。一方、ブロックを括弧で表す場合もある。式の中の括弧は一般的な[計算順序の規則が適用され](https://ja.wikipedia.org/wiki/演算子の優先順位 "wikilink")、括弧内が先に計算される。

`IF` 式によって値のテストが行われる。同値かどうかの比較は EQL を使い（ = 記号はオーバーロードされていない）、GTR は greater than、NEQ は not equal に対応する。例えば、次のコードは Z の値を絶対値を Q で示されるアドレスに代入する。

    Q = (IF .Z GTR 0 THEN .Z ELSE -.Z);

識別子（変数と定数）は使用する前に宣言する必要があり、一般に `OWN` というキーワードを用いる。変数を宣言する部分では、コンパイラはその領域を確保する。場合によっては `BIND` というキーワードを使って固定アドレスに変数を割り当てる。これは、マシンのレジスタや特定のアドレスにアクセスするのに使われる。

サブルーチンは *routines* と呼ばれ、`ROUTINE` というキーワードで宣言される。文字列置換を行うマクロは `MACRO` というキーワードで宣言される。配列は *structures* と呼ばれ、`VECTOR` というキーワードで宣言される。

他にも次のような構成要素がある。

  - `CASE` 式
  - `INCR` 式を使ったループ構造。ALGOL の FOR 文に似ている。
  - 組み込みの文字列関数や自動データ変換（数値から文字列など）

## ソースコードの例

以下のコード例は、上記で引用した *Bliss Language Manual* にあるものである。

    MODULE E1 (MAIN = CTRL) =
    BEGIN
    FORWARD ROUTINE
        CTRL,
        STEP;
    ROUTINE CTRL =
    !+
    ! This routine inputs a value, operates on it, and
    ! then outputs the result.
    !-
        BEGIN
        EXTERNAL ROUTINE
            GETNUM,     ! Input a number from terminal
            PUTNUM;     ! Output a number to terminal
        LOCAL
            X,          ! Storage for input value
            Y;          ! Storage for output value
        GETNUM(X);
        Y = STEP(.X);
        PUTNUM(.Y)
        END;
    ROUTINE STEP(A) =
    !+
    ! This routine adds 1 to the given value.
    !-
        (.A+1);
    END
    ELUDOM

## バージョン

  - BLISS-10
  - BLISS-11 - PDP-11 向け[クロスコンパイラ](../Page/クロスコンパイラ.md "wikilink")
  - BLISS-16
  - BLISS-16C - DEC自身による BLISS-11
  - BLISS-32
  - BLISS-36
  - BLISS-64
  - Common BLISS - 移植性のあるサブセット

## 参考文献

  - Wulf, W. A.; Russell, D. B.; Habermann, A. N. (1971). *BLISS: A Language for Systems Programming*. Communications of the ACM 14(12):780-790, Dec 1971
  - Wulf, W. A.; Johnson, R. K.; Weinstock, C. B.; Hobbs, S. O.; Geschke, C. M. (1975). *The Design of an Optimizing Compiler*. New York: Elsevier, ISBN 0-444-00158-1.

## 外部リンク

  - [Site with PDFs of manuals](http://63.249.85.132/langs)
  - [Alan Lehotsky posting about BLISS at DEC](http://compilers.iecc.com/comparch/article/87-07-029)
  - [Language Reference Manual](http://h71000.www7.hp.com/freeware/freeware80/bliss/documentation/)
  - ["BLISS: A Language for Systems Programming" by W.A. Wulf, D.B. Russell, and A.N. Habermann. (PostScript)](http://vms.process.com/scripts/fileserv/fileserv.com?BLISS-ARTICLE)
  - [Session notes for "Introduction to BLISS" by Matthew D. Madison. (PostScript)](http://vms.process.com/scripts/fileserv/fileserv.com?BLISS-INTRO)

### ダウンロード

  - [BLISS-10](http://pdp-10.trailing-edge.com/bb-m836d-bm/)
  - [Older BLISS-11](ftp://iecc.com/pub/file/bliss.tar.gz)
  - [BLISS-36](http://pdp-10.trailing-edge.com/bls36v42/)
  - [BLISS-11, BLISS-32 and BLISS-64](http://h71000.www7.hp.com/freeware/freeware70/bliss/)
  - [FreeVMS Portable BLISS for GCC](ftp://freevms.nvg.org/pub/vms/freevms/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")