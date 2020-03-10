> この記事は[INTERCAL](https://ja.wikipedia.org/wiki/INTERCAL)から翻訳されています。


**INTERCAL**はプログラム言語。それ自身が[プログラミング言語](../Page/プログラミング言語.md "wikilink")の[パロディ](../Page/パロディ.md "wikilink")にもなっており、実用言語ではない。いわゆる[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")の典型例として知られている。

INTERCALは、[FORTRAN](../Page/FORTRAN.md "wikilink")や[COBOL](../Page/COBOL.md "wikilink")はもちろん、[1960年代](../Page/1960年代.md "wikilink")に提案された数々のプログラミング言語の構造や表記法も皮肉の対象としている。そのため、[Cや](../Page/C言語.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")に慣れ親しんだ今日の観点からすると、そのユーモアは少々時代遅れに感じられる部分もある。

## 概要

INTERCALは[1972年](../Page/1972年.md "wikilink")、[プリンストン大学](https://ja.wikipedia.org/wiki/プリンストン大学 "wikilink")の学生であった[ドン・ウッズ](https://ja.wikipedia.org/wiki/ドン・ウッズ "wikilink")と[ジェイムズ・リヨン](https://ja.wikipedia.org/wiki/ジェイムズ・リヨン "wikilink")によって作成された\[1\]。現行バージョンであるC-INTERCALは、[エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink")によって保守されている\[2\]。INTERCALという名前は、製作者らによれば "Compiler Language With No Pronounceable Acronym" （発音できる[頭字語](../Page/頭字語.md "wikilink")のないコンパイラ言語）からつけられたものだという。

INTERCALは意図的に、他のあらゆる主だったコンピュータ言語とは異なるように設計されている\[3\]。他のプログラム言語におけるごく普通の処理も、INTERCALでは不可解で無駄の多い文法で表現される。例として、INTERCALのリファレンスマニュアルの一部を以下に示す。

INTERCALのマニュアルにはこの他にも、逆説的で馬鹿げた、あるいはユーモラスな説明が数多く書かれている。

INTERCALにはこの他にも、プログラマ的美的感覚とは決して相容れない数々の特徴がある。例えば、ステートメントに"READ OUT"、"IGNORE"、"FORGET"、"PLEASE"といったキーワードが用いられている。マニュアルでは、アルファベット以外の[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")文字が独特の名称で呼ばれている。例えば、シングルクォート(')とダブルクォート(")はそれぞれ「火花(sparks)」「ウサギの耳(rabbit ears)」、等価記号(=)は「半メッシュ(half mesh)」といった具合である。他のプログラム言語では代入に等価記号が使用されるが、INTERCALでは"\<-"を用いる。この記号はそれぞれ「アングル(angle)」と「ワーム(worm)」と呼ばれている。

オリジナルのプリンストン大学版では[パンチカード](../Page/パンチカード.md "wikilink")と[EBCDIC](https://ja.wikipedia.org/wiki/EBCDIC "wikilink")の文字セットが使用されていた。そのため、ASCIIのコード体系を採用しているコンピュータ上でINTERCALを実行する場合、2種類の文字を別の文字に置き換える必要がある。ミングル演算子は"ハードウェアに対応して増加するソフトウェアのコストを表現する"「¢」の代わりに「$」を、単項排他的論理和演算子として"[排他的論理和](../Page/排他的論理和.md "wikilink")(XOR)を初めて目にした人々の平均的反応を正確に表現した"「∀」の代わりに「?」を用いる。

[Usenetのニューズグループ](../Page/ネットニュース.md "wikilink") alt.lang.intercal は、INTERCALやその他の難解プログラム言語の研究と鑑賞のために作られたものである。

意図的に鈍重かつ冗漫な言語であるべく作成されたにもかかわらず、INTERCALは[チューリング完全](../Page/チューリング完全.md "wikilink")である。つまり、十分なメモリさえあれば、万能[チューリングマシン](../Page/チューリングマシン.md "wikilink")が計算可能なあらゆる問題を処理することができる。ただし、実行速度はきわめて遅い。ベンチマークとして[SUN](../Page/サン・マイクロシステムズ.md "wikilink") SPARCStation-1上で[エラトステネスの篩](../Page/エラトステネスの篩.md "wikilink")を実行したところ、65536以下の素数を全て計算するのにかかった時間は、Cでは0.5秒以下であるが、INTERCALでは17時間以上であった\[4\]。

[International Obfuscated C Code Contest](https://ja.wikipedia.org/wiki/IOCCC "wikilink")（国際醜いCプログラムコンテストの意）のようなコンテストを見てもわかるとおり、INTERCAL以外の言語であってもINTERCALと同等あるいはそれ以上の理解しづらいプログラムを書くことは可能である。しかし、これらの読みにくいコードは、通常なんらかの意図を持って記述されたものである。これに対して、INTERCALの読みにくさは言語仕様によるものである。

INTERCALのマニュアルには「INTERCALの設計上の目標は、前例のないものを作ることだ」と記載されている。これはおそらく制御構造とデータの操作演算子の両方を対象にしていると思われるが、確かに設計者は部分的にこの試みに成功している。唯一知られている例外は[1967年](../Page/1967年.md "wikilink")にリリースされたソビエトのメインフレーム[BESM-6](https://ja.wikipedia.org/wiki/BESM-6 "wikilink")のある命令で、これは事実上INTERCALのセレクト演算子とほぼ同様である。

後発の言語には一部にINTERCALと同様の設計が見られるものもある。たとえば代入記号では、[1988年](../Page/1988年.md "wikilink")に誕生した[S言語](../Page/S言語.md "wikilink")でも \<- を用いている。（[論理学](../Page/論理学.md "wikilink")で代入や定義を表す記号 ← を模したものであるので、代入に等号を用いるより自然と考える立場もある。）なお、代入に = を使うことには問題がある、という意見はFORTRANの昔からあり := などを使う言語も少なくない（C言語では、設計者らの簡単な調査によればコード中には代入のほうが比較より多く現れるので、代入のほうを短い = にしたという話がある）。一部の言語では ∈ の代用として \<- を使う。

## バリエーション

ウッズとリヨンによる最初のINTERCALは、[入出力](../Page/入出力.md "wikilink")の能力が極めて制限されていた。入力できるデータは桁が指定された数字のみ、出力は拡張された[ローマ数字](../Page/ローマ数字.md "wikilink")のみであった。

インターネット上で利用可能な再実装版のC-INTERCALは、より一般的な仕様となっている。これは難解プログラミング言語の愛好家達によるものである。C-INTERCALにはオリジナル版からの何点かの変更と、新しく導入されたいくつかの機能が存在する。[COME FROMステートメント](https://ja.wikipedia.org/wiki/COME_FROM "wikilink")\[5\]やチューリング・テキスト・モデルによるテキストの入出力機能がその例である。

C-INTERCALの作者はまた、TriINTERCALというバリアントも作成した\[6\]。これは[3進数によるシステムで](https://ja.wikipedia.org/wiki/3進記数法 "wikilink")、演算子が一般化されている。 更に新しいバリアントとしてThreaded Intercalがある\[7\]。このバリアントでは[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")をサポートするために、"COME FROM"ステートメントの機能が拡張されている。

## Hello, world

伝統的な[Hello worldプログラムを使い](../Page/Hello_world.md "wikilink")、INTERCALが通常の言語とどれだけ異なっているかを示す。Cでは、以下のように記述される。

``` c

        #include <stdio.h>
        int main(void) {
          printf("hello, world\n");
          return 0;
        }
```

C-INTERCALでは以下のようになる。コードはより長く、かつ読みにくいものになっている。

```
        DO ,1 <- #13
        PLEASE DO ,1 SUB #1 <- #234
        DO ,1 SUB #2 <- #112
        DO ,1 SUB #3 <- #112
        DO ,1 SUB #4 <- #0
        DO ,1 SUB #5 <- #64
        DO ,1 SUB #6 <- #194
        DO ,1 SUB #7 <- #48
        PLEASE DO ,1 SUB #8 <- #22
        DO ,1 SUB #9 <- #248
        DO ,1 SUB #10 <- #168
        DO ,1 SUB #11 <- #24
        DO ,1 SUB #12 <- #16
        DO ,1 SUB #13 <- #214
        PLEASE READ OUT ,1
        PLEASE GIVE UP
```

## 脚注

<references />

## 外部リンク

  - [The INTERCAL Resources Page](http://www.catb.org/~esr/intercal/).
  - [INTERCAL Resources on the Web](http://www.muppetlabs.com/~breadbox/intercal/) - いくつかの実装も紹介されている。
  - [INTERCAL reference manual](http://www.progsoc.uts.edu.au/~sbg/intercal/intercal.html)
  - [C-INTERCAL supplemental reference manual](http://www.progsoc.uts.edu.au/~sbg/intercal/ick.html)
  - [Threaded Intercal](http://www.cse.unsw.edu.au/~malcolmr/intercal/threaded.html)
  - [alt.lang.intercal](http://groups.google.com/group/alt.lang.intercal/)

-----

本記事の英語版の初期のバージョンには、[The Jargon File 4.2.3 Mar 2001](http://www.catb.org/~esr/jargon/)([ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink"))の文章が含まれている。

[Category:難解プログラミング言語](https://ja.wikipedia.org/wiki/Category:難解プログラミング言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")

1.  [The Original INTERCAL Manual](http://www.muppetlabs.com/~breadbox/intercal/intercal.txt)
2.  [INTERCAL Resources on the Web](http://www.muppetlabs.com/~breadbox/intercal/)
3.
4.  [INTERCAL — the Language from Hell](http://www.catb.org/~esr/intercal/stross.html) （チャールズ・ストロス、*Computer Shopper* \[UK\], 1992年9月）
5.  発想の元はの提案（このdoiは再録版のもので、初出はデータメーション誌（[:en:Datamation](https://ja.wikipedia.org/wiki/:en:Datamation "wikilink")）1973年12月号）である。
6.  [Wimps don't read this message (long) -- alt.lang.intercal](http://groups.google.co.uk/group/alt.lang.intercal/msg/a1b9db14c09bdbdf)
7.  [Threaded Intercal](http://www.cse.unsw.edu.au/~malcolmr/intercal/threaded.html)