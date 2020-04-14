> この記事は[Comefrom文](https://ja.wikipedia.org/wiki/Comefrom文)から翻訳されています。


[プログラミング言語](../Page/プログラミング言語.md "wikilink")における**comefrom文**（カムフロム文、）とは、コード内の任意のポイント（専ら[ラベルで指定される](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink")）から、その`comefrom`文の場所へ制御がジャンプ（移動）するという[制御構造](../Page/制御構造.md "wikilink")のひとつである「[文](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")」である。[goto文](https://ja.wikipedia.org/wiki/goto文 "wikilink")とほぼ反対の働きをするものであり、元々は冗談として提唱されたものだったが、一部のプログラミング言語で実際に実装されている。`goto`が`go to`とも書かれるように、`comefrom`も`come from`とも書かれる。

## 概要

コード内の移動元のポイントは、通常`comefrom`の[引数](../Page/引数.md "wikilink")として指定される。指定されたポイントで移動が発生するかどうかは、使用される言語によって異なる。同じ移動元を指定するcomefrom文が複数ある場合、言語によって、そのような`comefrom`は無効となるもの、非決定的となるもの、定義済みの優先順位で実行されるものや、[INTERCAL](../Page/INTERCAL.md "wikilink")のような[並列計算](../Page/並列計算.md "wikilink")もしくは[並行計算](../Page/並行計算.md "wikilink")が行われるものがある。

comefrom文の簡単な例"`comefrom x`"で説明する。この文は、トラップドアとして機能する[ラベル](https://ja.wikipedia.org/wiki/ラベル_\(プログラミング\) "wikilink") `x` と対になって使用される。このラベルは、対応するcomefrom文の近くに物理的に配置する必要はない。コードの実行がラベルに達すると、対応するcomefrom文に制御が移動する。[if文](https://ja.wikipedia.org/wiki/if文 "wikilink")の中にラベルがある場合は、goto文の場合と同様に、if文の条件が満たされた場合のみ移動が行われる。goto文がコードのローカル構造のみに依存するのに対し、comefrom文はグローバル構造に依存する。goto文の場合はgoto文のある行に到達すると無条件に制御が移動するが、comefrom文は、ラベルのあるスコープ内にcomefrom文があるか確認し、条件がヒットしたかどうかを確認するために、プログラムまたはスコープ全体をスキャンする必要がある。これにより、デバッグ（およびプログラムの制御フローの理解）が非常に困難になる。これは、問題の行やラベルの近くに制御のジャンプ先を示すものがなく、その行またはラベルを参照しているcomefrom文をプログラム全体から探す必要があるためである。

Python gotoモジュールでは、デバッガフックを使用してcomefrom文を実装できる\[1\]（[後述](https://ja.wikipedia.org/wiki/#PythonGoto "wikilink")）。また、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")の構成オプション CONFIG_JUMP_LABEL で使用されるgcc機能"asm goto"でも実装できる。 no-opの場所は保存されており、no-opの後に命令に戻る実行可能フラグメントへのジャンプに置き換えられる。

## 歴史

`comefrom`は、冗談の[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")の命令'CMFRM'として現れたのが最初である。これは、1973年に『』誌に掲載された、R・ローレンス・クラークによる[エドガー・ダイクストラ](../Page/エドガー・ダイクストラ.md "wikilink")の文書「（Go to 文は有害と考えられる）」に反応した記事にて詳しく説明されていたものである\[2\] 。

comefrom文は最終的に、[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")の1つである[INTERCAL](../Page/INTERCAL.md "wikilink")の変種であるC-INTERCALに、さらに曖昧な'computed `comefrom`'（計算されたcomefrom）とともに実装された。また、[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")に、既存のdo文を補完するための'assigned `COME FROM`'と'`DONT`'を追加する提案もあった\[3\]。

2004年4月1日、Richie Hindleが、[Python](../Page/Python.md "wikilink")用の`GOTO`と`COMEFROM`の実装を公開した\[4\]。[エイプリルフール](https://ja.wikipedia.org/wiki/エイプリルフール "wikilink")に公開されたものであり、真面目に使用することを意図したものではないが、構文は正当であり、実装は完全に機能する。

## 実用的な用途

### BASIC

以下は、"`GOTO`"の代わりに"`COMEFROM`"を使用した架空の[BASIC](../Page/BASIC.md "wikilink")方言のプログラムの例である。

``` qbasic
10 COMEFROM 40
20 INPUT "WHAT IS YOUR NAME? "; A$
30 PRINT "HELLO, "; A$
40 REM
```

このプログラムは、ユーザに名前を質問し、入力された名前に対し挨拶をするという動作を繰り返す。行40の命令"`REM`"は、単なる[NOP](../Page/NOP.md "wikilink")（この場合は[コメント](../Page/コメント_\(コンピュータ\).md "wikilink")）である。行10の"`COMEFROM`"文は、その内容に関係なく、実行が行40に達するとこの行に戻る。

### Python

以下に、joke gotoモジュールがインストールされた[Python](../Page/Python.md "wikilink")での完全に実行可能な例（デバッガフックを使用してプログラムの実行を制御する）を示す。

``` python
from goto import comefrom, label

comefrom .repeat
name = raw_input('What is your name? ')
if name:
    print("Hello", name)
    label .repeat
print("Goodbye!")
```

### Ruby

以下に、Intercal comefrom文の[Ruby](../Page/Ruby.md "wikilink")での実装を示す。

``` ruby
$come_from_labels = {}

def label(l)
  if $come_from_labels[l]
    $come_from_labels[l].call
  end
end

def come_from(l)
  callcc do |block|
    $come_from_labels[l] = block
  end
end
```

### OS/360 Fortran G

[OS/360](https://ja.wikipedia.org/wiki/OS/360 "wikilink")のFortran Gコンパイラには、デバッグパケット機能がある。その"AT"文は、制御フローをデバッグブロックに渡すという点でcomefrom文に似ている。[ブレークポイント](https://ja.wikipedia.org/wiki/ブレークポイント "wikilink")は一般的に似ている\[5\]。

  - 例1：SOLON、GFAR、EWELLの値は、文10の完了時に検査される。AT文は文11を示す。

<!-- end list -->

``` fortranfixed
      INTEGER SOLON, GFAR, EWELL
         .
         .
         .
10    SOLON = GFAR * SQRT(FLOAT(EWELL))
11    IF (SOLON) 40, 50, 60
         .
         .
         .
      DEBUG UNIT(3)
      AT 11
      DISPLAY GFAR, SOLON, EWELL
      END
```

  - 例2：文35が検出されると、STOCKの全ての値が表示される。

<!-- end list -->

``` fortranfixed
      DIMENSION STOCK(1000),OUT(1000)
         .
         .
         .
      DO 30 I=1, 1000
25    STOCK(I)=STOCK(I) - OUT(I)
30    CONTINUE
35    A = B + C
         .
         .
         .
      DEBUG UNIT(3)
      AT 35
      DISPLAY STOCK
      END
```

  - 例3：トレースは文10で始まり、ループの実行中に文20でトレースが停止し、ループの後に再開する。文30が実行される直前にトレースが停止する。

<!-- end list -->

``` fortranfixed
10    A = 1.5
12    L = 1
15    B = A + 1.5
20    DO 22 I = 1,5
         .
         .
         .
22    CONTINUE
25    C = B + 3.16
30    D = C/2
      STOP
         .
         .
         .
      DEBUG UNIT(3), TRACE
C     DEBUG PACKET NUMBER 1
      AT 10
      TRACE ON
C     DEBUG PACKET NUMBER 2
      AT 20
      TRACE OFF
      DO 35 I = 1,3
         .
         .
         .
35    CONTINUE
      TRACE ON
C     DEBUG PACKET NUMBER 3
      AT 30
      TRACE OFF
      END
```

## 関連項目

  - (F. X. Reid) - comefrom文の意味論の専門家\[6\]

  -
  - [INTERCAL](../Page/INTERCAL.md "wikilink")

comefrom文に類似した概念

  - [アスペクト指向プログラミング](../Page/アスペクト指向プログラミング.md "wikilink")における
  - [継続](../Page/継続.md "wikilink")
  - [MATLAB](../Page/MATLAB.md "wikilink") SimulinkにおけるGoto/From signal routing block

## 脚注

## 外部リンク

  - [COMEFROM Information Page](http://c2.com/cgi/wiki?ComeFrom)
  - [Datamation Article](https://web.archive.org/web/20180716171336/http://www.fortran.com/fortran/come_from.html)
  - [Joke Assembler Instruction List Including CMFRM](https://web.archive.org/web/20121022080527/http://homepage.ntlworld.com/brook.street/funny/pdp11.htm)
  - \[<https://metacpan.org/module/Acme>::ComeFrom comefrom support for Perl\]

[Category:コンピュータ・ユーモア](https://ja.wikipedia.org/wiki/Category:コンピュータ・ユーモア "wikilink") [Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")

1.
2.
3.
4.  .
5.  IBM System/360 and System/370 Fortran IV Language, GC28-6515-10, May 1974
6.  F. X. Reid, On the Formal Semantics of the COMEFROM Statement. [*FACS FACTS*, Issue 2006-1](http://www.bcs.org/upload/pdf/facts200603.pdf), pages 18–20, March 2006.