> この記事は[P](https://ja.wikipedia.org/wiki/P)から翻訳されています。


**pコードマシン**とは、[プロセッサ](../Page/プロセッサ.md "wikilink")の一種であるが、ハードウェアではなくソフトウェアで、すなわち[エミュレータや](../Page/エミュレータ_\(コンピュータ\).md "wikilink")[仮想機械](../Page/仮想機械.md "wikilink")のような[インタプリタ](../Page/インタプリタ.md "wikilink")型の[プログラムで実装されることを目的としたものであり](../Page/プログラム_\(コンピュータ\).md "wikilink")、p-code と呼ばれる[中間コード](https://ja.wikipedia.org/wiki/中間コード "wikilink")を解釈実行する。この用語は、そのような仕様一般を指すこともあるが、多くの仕様はそれぞれ個々の名称を持っている。特に[UCSD Pascalの](../Page/UCSD_Pascal.md "wikilink") p-Machine を指すことが多い。「p」の意味については、[Pascal](../Page/Pascal.md "wikilink")処理系の場合はPascalの頭文字ともされるが、他言語の場合はpseudo（[マイクロソフトのサポート情報](http://support.microsoft.com/kb/229415/en-us)を参照）やportable\[1\]などとされる。

このコンセプトは1966年ごろ、[BCPL](https://ja.wikipedia.org/wiki/BCPL "wikilink")のや[ニクラウス・ヴィルト](https://ja.wikipedia.org/wiki/ニクラウス・ヴィルト "wikilink")ののPとして実装されたのが最初であるが、pコード (p-code) と呼ばれるようになったのは1970年代初期であった。pコードを生成する初期の[コンパイラ](../Page/コンパイラ.md "wikilink")としては、1973年、Nori、Ammann、Jensen、Hageli、Jacobi が開発した Pascal-P コンパイラと\[2\]、ヴィルトが1975年に開発した Pascal-S コンパイラがある。

ソースコードからコンパイラの[コード生成](https://ja.wikipedia.org/wiki/コード生成 "wikilink")によってpコードが生成され、そのpコードはpコードマシンのエミュレータ、言い換えればインタプリタによって解釈実行される。商業的に十分意味があるとみて、pコードを直接実行するハードウェアが実装された例もある（例えば、[Pascal MicroEngine](https://ja.wikipedia.org/wiki/:en:Pascal_MicroEngine "wikilink")）。

## pコードによる実装の利点と欠点

### 利点

（実機の）機械語コードに直接変換するのに比べ、途中でpコードを経由してインタプリタや[実行時コンパイラ](../Page/実行時コンパイラ.md "wikilink")でpコードを実行する方式にはいくつかの利点がある。

  - 移植性が高い。コンパイラを他のプラットフォームに移植する際、小さなpコードインタプリタを移植するほうが簡単である。そうすれば、コンパイラ本体は修正なしで移行できる（再コンパイルは必要）。
  - 実装が単純化される。コンパイラ作成にあたっては、機械語生成部分は最も複雑な部分の1つである。その点で、pコードを生成する方が簡単である。それによりコンパイラ開発が早くなる。
  - コードのサイズが小さくなる。pコードは理想的な[仮想機械](../Page/仮想機械.md "wikilink")に基づいているため、多くの場合、生成されたpコードは実機の機械語コードよりも小さくなる。
  - デバッグしやすい。pコードは[インタプリタ](../Page/インタプリタ.md "wikilink")で実行されるため、インタプリタに各種実行時チェックを入れることで本来の機械語では困難なデバッグが可能となる。

[Pascal](../Page/Pascal.md "wikilink")のいくつかの実装では、pコードの解釈実行に[ジャストインタイムコンパイル方式](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")を利用している。ニクラウス・ヴィルトは Pascal の後継である [Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink") 向けの m-code について言及している[1](http://www.swissdelphicenter.ch/en/niklauswirth.php) 。1980年代、イギリスでpコードのプログラムを実行するクロスプラットフォームの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") Business Operating System (BOS) が開発された。[UCSD p-System](https://ja.wikipedia.org/wiki/UCSD_p-System "wikilink") はpコードを使ったマシン非依存の移植性の高いオペレーティングシステムであった。

### 欠点

pコードの最大の欠点は実行速度が遅い点だが、[実行時コンパイラ](../Page/実行時コンパイラ.md "wikilink")を使えばある程度おぎなえることもある。

## UCSD p-Machine

### アーキテクチャ

pコードマシンは[スタックマシン](https://ja.wikipedia.org/wiki/スタックマシン "wikilink")であり、ほとんどの命令がスタックからオペランドを持ってきて、結果をスタックに戻す。例えば、add 命令はスタックの先頭2要素を取り出し、加算結果をスタックに戻す。一部の命令は即値オペランドを持つ。Pascalと同様、pコードも型があり、ブーリアン(b)、文字(c)、整数(i)、実数(r)、集合(s)、ポインタ(a)が最初から用意されている。

以下に簡単な命令を示す。命令名、実行前のスタック状態、実行後のスタック状態、解説の順に並んでいる。

  -
    adi: (i1 i2) ⇒ (i1+i2) - 2つの整数の加算
    adr: (r1 r2) ⇒ (r1+r2) - 2つの実数の加算
    dvi: (i1 i2) ⇒ (i1/i2) - 整数の除算
    inn: (i1 s1) ⇒ (b1) - メンバーシップを設定。b1 には i1 が s1 のメンバーかどうかが設定される（true/false）。
    idci i1: () ⇒ (i1) - 整数定数をスタック上にロードする。
    mov: (a1 a2) ⇒ () - メモリ間のコピー
    not: (b1) ⇒ (\~b1) - ブーリアンの否定

### 環境

[FORTHや](../Page/Forth.md "wikilink")[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")のような他のスタックベースの環境とは異なり、pコードマシンは[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")としても使われる1つのスタックしか持たない。マシンの持つ3つの[レジスタは](../Page/レジスタ_\(コンピュータ\).md "wikilink")、それぞれスタック内の位置を指している。スタックはアドレスの大きくなる方向に成長する。

  - SP (stack pointer) はスタックのトップを指す。
  - MP (mark pointer) は現在のスタックフレームの開始位置を指す。
  - EP (extreme pointer) は現在のプロシージャが使っているトップの位置を指す。

他に定数域があり、その下に[動的メモリアロケーション](https://ja.wikipedia.org/wiki/動的メモリアロケーション "wikilink")域がある。NPレジスタ (new pointer) はヒープの先頭（最低位アドレス）を指す。EPがNPより大きくなった場合、マシンのメモリが使い尽くされたことを示す。

PCレジスタはコード領域で現在実行中の命令を指している。

### 呼出規約

スタックフレームは以下のようになっている:

`EP ->`
`      ローカルスタック`
`SP -> ...`
`      ローカル変数`
`      ...`
`      引数`
`      ...`
`      リターンアドレス（前のPC）`
`      前のEP`
`      動的リンク（前のMP）`
`      静的リンク（外側のプロシージャのMP）`
`MP -> 関数のリターン値`

プロシージャ呼び出しは次のようになる。まず呼び出しは次の命令で開始される。

` mst n`

ここで、*n* は入れ子レベルを指定する（Pascalではプロシージャが入れ子になりうることに注意）。この命令はスタックに印をつける。すなわち現在のスタックフレームの上の5要素ぶんを予約し、以前のEP、動的リンク、静的リンクなどを設定する。呼び出し側は必要な引数を計算してプッシュし、次の命令を実行する。

` cup n, p`

これでユーザープロシージャが呼び出される（*n* は引数の個数、*p* はプロシージャのアドレス）。この命令はPCをリターンアドレスとしてスタック上にセーブし、そのプロシージャのアドレスを新たなPCとしてセットする。

ユーザープロシージャは次の2つの命令から開始される。

` ent 1, i`
` ent 2, j`

1番目の命令はSPを MP + *i* にする。2番目の命令は EP を SP + *j* にする。従って、*i* にはローカル変数用の領域サイズを指定し（引数および余分に5要素分も予約する）、*j* には命令実行でローカルに必要なスタック領域が指定される。メモリ不足が発生していないかはこの時点でチェックされる。

呼び出し側への復帰は次の命令で行われる。

` retC`

*C*にはリターン型（上述の基本型 i, r, c, b, a と何も返さない場合の p）が指定される。リターン値は適切なセルに格納される。p 以外の各型のリターンでは、その値がスタックに置かれたまま呼び出し側に復帰する。

ユーザープロシージャの呼び出し(cup)ではなく、標準プロシージャ *q* を呼び出す場合は次の命令を使用する。

` csp q`

標準プロシージャとは、Pascalの標準ライブラリのようなもので、例えば *readln()*（"csp rln"）、*sin()*（"csp sin"）などがある。ただし、*eof()* はpコードでは1つの命令となっている。

## 例

[1976年](https://ja.wikipedia.org/wiki/1976年 "wikilink")、[ニクラウス・ヴィルト](https://ja.wikipedia.org/wiki/ニクラウス・ヴィルト "wikilink")は単純なpコードマシンを自著 *Algorithms + Data Structures = Programs* で定義した。このマシンには3つのレジスタがある。プログラムカウンタ(p)、[スタックベースレジスタ](https://ja.wikipedia.org/wiki/コールスタック "wikilink")(b)、[スタック](../Page/スタック.md "wikilink")ポインタ(t) である。8種類の命令があり、うち1種 (opr) は複数の形式がある。

このマシンのコードは以下のようになる (Pascal):

``` pascal
const
    levmax=3;
    amax=2047;
type
    fct=(lit,opr,lod,sto,cal,int,jmp,jpc);
    instruction=packed record
        f:fct;
        l:0..levmax;
        a:0..amax;
    end;

procedure interpret;

  const stacksize = 500;

  var
    p, b, t: integer; {program-, base-, topstack-registers}
    i: instruction; {instruction register}
    s: array [1..stacksize] of integer; {datastore}

  function base(l: integer): integer;
    var b1: integer;
  begin
    b1 := b; {find base l levels down}
    while l > 0 do begin
      b1 := s[b1];
      l := l - 1
    end;
    base := b1
  end {base};

begin
  writeln(' start pl/0');
  t := 0; b := 1; p := 0;
  s[1] := 0; s[2] := 0; s[3] := 0;
  repeat
    i := code[p]; p := p + 1;
    with i do
      case f of
        lit: begin t := t + 1; s[t] := a end;
        opr:
          case a of {operator}
            0:
              begin {return}
                t := b - 1; p := s[t + 3]; b := s[t + 2];
              end;
            1: s[t] := -s[t];
            2: begin t := t - 1; s[t] := s[t] + s[t + 1] end;
            3: begin t := t - 1; s[t] := s[t] - s[t + 1] end;
            4: begin t := t - 1; s[t] := s[t] * s[t + 1] end;
            5: begin t := t - 1; s[t] := s[t] div s[t + 1] end;
            6: s[t] := ord(odd(s[t]));
            8: begin t := t - 1; s[t] := ord(s[t] = s[t + 1]) end;
            9: begin t := t - 1; s[t] := ord(s[t] <> s[t + 1]) end;
            10: begin t := t - 1; s[t] := ord(s[t] < s[t + 1]) end;
            11: begin t := t - 1; s[t] := ord(s[t] >= s[t + 1]) end;
            12: begin t := t - 1; s[t] := ord(s[t] > s[t + 1]) end;
            13: begin t := t - 1; s[t] := ord(s[t] <= s[t + 1]) end;
          end;
        lod: begin t := t + 1; s[t] := s[base(l) + a] end;
        sto: begin s[base(l)+a] := s[t]; writeln(s[t]); t := t - 1 end;
        cal:
          begin {generate new block mark}
            s[t + 1] := base(l); s[t + 2] := b; s[t + 3] := p;
            b := t + 1; p := a
          end;
        int: t := t + a;
        jmp: p := a;
        jpc: begin if s[t] = 0 then p := a; t := t - 1 end
      end {with, case}
  until p = 1;
  writeln(' end pl/0');
end {interpret};
```

このマシンはヴィルトの[PL/0](https://ja.wikipedia.org/wiki/PL/0 "wikilink")の実行に使われた。PL/0 はコンパイラ開発の教育用に使われたPascalのサブセットである。

## 脚注

## 参考文献

  - Steven Pemberton and Martin Daniels: [Pascal Implementation: The P4 Compiler and Interpreter](http://www.cwi.nl/~steven/pascal/book/). ISBN 0-85312-358-6; ISBN 0-13-653031-1
  - [Steven Pemberton's page on Pascal](http://homepages.cwi.nl/~steven/pascal/) P4 コンパイラとインタプリタのPascalによるソースコード、使用方法
  - [The Jefferson Computer Museum's page on the UCSD P-System](http://www.threedee.com/jcm/psystem/)
  - [Open Source implementation](http://ucsd-psystem-vm.sourceforge.net/)
      - [Klebsch implementation](http://www.klebsch.de) - そのフォーク
  - *Compiling with C\# and Java*, Pat Terry, 2005, ISBN 0-321-26360-X, 624
  - *Algorithms + Data Structures = Programs*, Niklaus Wirth, 1975, ISBN 0-13-022418-9
  - *Compiler Construction*, Niklaus Wirth, 1996, ISBN 0-201-40353-6
  - *The Byte Book of Pascal*, Blaise W. Liffick, Editor, 1979, ISBN 0-07-037823-1
  - *PASCAL - The Language and its Implementation*, Edited by D.W. Barron, 1981, ISBN 0-471-27835-1. Especially see the articles *Pascal-P Implementaion Notes* and *Pascal-S: A Subset and its Implementation*.

## 関連項目

  - [バイトコード](../Page/バイトコード.md "wikilink")
  - [Pascal](../Page/Pascal.md "wikilink") - [UCSD Pascal](../Page/UCSD_Pascal.md "wikilink") - [UCSD p-System](https://ja.wikipedia.org/wiki/UCSD_p-System "wikilink")
  - [コンパイラ](../Page/コンパイラ.md "wikilink")
  - [インタプリタ](../Page/インタプリタ.md "wikilink")
  - [スレッデッドコード](https://ja.wikipedia.org/wiki/スレッデッドコード "wikilink")
  - [Sweet16](https://ja.wikipedia.org/wiki/Sweet16 "wikilink")

[Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:インタプリタ](https://ja.wikipedia.org/wiki/Category:インタプリタ "wikilink") [Category:プログラミング言語の実装](https://ja.wikipedia.org/wiki/Category:プログラミング言語の実装 "wikilink")

1.  この記事の英語版で現在要出典となっているが、参考のために挙げる
2.