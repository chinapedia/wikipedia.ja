> この記事は[Oberon-2](https://ja.wikipedia.org/wiki/Oberon-2)から翻訳されています。


**Oberon-2** とは、[プログラミング言語](../Page/プログラミング言語.md "wikilink") [Oberon](../Page/Oberon.md "wikilink") を拡張し、[オブジェクト指向的なコンセプトを取り入れた言語である](../Page/オブジェクト指向プログラミング.md "wikilink")。

1991年、[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")の[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")と （現システムソフトウェア研究所）が開発した。Oberon-2 は [Oberon](../Page/Oberon.md "wikilink") の上位互換である。Oberon-2 は Object Oberon（Oberon にオブジェクト指向のコンセプトを導入した最初の試み）の再設計でもあった。

Oberon-2 は Oberon から限定された[リフレクションとインタフェースなどを持たない](../Page/リフレクション_\(情報工学\).md "wikilink")[単一継承](https://ja.wikipedia.org/wiki/継承_\(プログラミング\)#派生型による共用と置換 "wikilink")（[型拡張](../Page/派生型.md "wikilink")）を受け継いでいるが、効果的な仮想メソッド（型束縛プロシージャ）を追加している。メソッド呼び出しは、[C++](../Page/C++.md "wikilink")のような[仮想メソッドテーブルを使って実行時に確定する](https://ja.wikipedia.org/wiki/仮想関数テーブル "wikilink")。

[Smalltalk](../Page/Smalltalk.md "wikilink") などの完全なオブジェクト指向言語に比べると、Oberon-2 の基本データ型はオブジェクトになっておらず、クラスもオブジェクトではなく、多くの操作がメソッドではないし、[メッセージパッシング](https://ja.wikipedia.org/wiki/メッセージパッシング "wikilink")の概念もなく、[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")も限定的である（[Smalltalk](../Page/Smalltalk.md "wikilink")や[Ruby](../Page/Ruby.md "wikilink")のような[ダックタイピング](https://ja.wikipedia.org/wiki/ダックタイピング "wikilink")がなく、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のような[インタフェースも定義できない](https://ja.wikipedia.org/wiki/インタフェース_\(情報技術\)#ソフトウェアインタフェース "wikilink")）。オブジェクト/クラスレベルでの[カプセル化](../Page/カプセル化.md "wikilink")もサポートしていないが、モジュールをその目的で使用することができる。

Oberon-2 のリフレクションはを使わず、実行ファイル内に含まれる型記述子を単に読み、それが型やプロシージャを定義しているモジュールに渡される。その構造体の形式が言語レベルで渡されるなら（例えば Oberon System 3 がそうである）、ライブラリレベルでのリフレクションの実装が可能である。従って、言語コードを全く変えずにライブラリレベルでほとんど全てを実行することも可能である。実際、Oberon System 3 は言語レベルとライブラリレベルのリフレクションを多用している。

## コード例

以下の Oberon-2 のコードは、単純な[リストクラスを実装したものである](../Page/連結リスト.md "wikilink")。

``` oberon2
MODULE ListClass;

  TYPE List*    = POINTER TO ListNode;
       ListNode = RECORD
            value : INTEGER;
             next : List;
       END;

  PROCEDURE ( l : List ) Add*    ( v : INTEGER );
  BEGIN
       (* ... *)
  END Add;
  PROCEDURE ( l : List ) AddLast*( v : INTEGER );
  BEGIN
       (* ... *)
  END AddLast;
  PROCEDURE ( l : List ) AddAt*  ( i : INTEGER; v : INTEGER );
  BEGIN
       (* ... *)
  END AddAt;

  PROCEDURE ( l : List ) Remove*;
  BEGIN
       (* ... *)
  END Remove;
  PROCEDURE ( l : List ) RemoveLast*;
  BEGIN
       (* ... *)
  END RemoveLast;
  PROCEDURE ( l : List ) RemoveAt* ( i : INTEGER );
  BEGIN
       (* ... *)
  END RemoveAt;

END ListClass.
```

## Oberon からの拡張

  - 型束縛プロシージャ
    [プロシージャ](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")は、レコード型（あるいはポインタ型）に[束縛することができる](../Page/束縛_\(情報工学\).md "wikilink")。オブジェクト指向的用語で言えば、[インスタンスメソッドと等価である](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\)#インスタンスメソッドとクラスメソッド "wikilink")。
  - リードオンリーのエクスポート
    エクスポートされた変数やレコードのフィールドについて、参照だけにアクセスを制限することもできる。これは、visibility flag に "-" を付与することで示される。
  - Open arrays
    Oberon では正式なパラメータ型としてのみ宣言可能だったが、Oberon-2 ではポインタベースの型として宣言できる。
  - FOR 文
    Pascal や Modula-2 にあった FOR 文は、Oberon では実装されなかった。それが、Oberon-2 で復活している。

### 実行時型チェック

Oberon-2 はオブジェクトの型について、動的なチェックを行う機構がいくつか用意されている。例えば、Bird オブジェクトのインスタンスとして Duck や Cuckoo があったとき、Oberon-2 では実行時にオブジェクトの実際の型に応じた処理が可能である。

従来的な方法としては、「型束縛システム」を使った方法がある。第二の方法として、`WITH` 文を使った方法がある。これは、変数の動的な[派生型](../Page/派生型.md "wikilink")を直接チェックするものである。どちらの場合も、派生型を特定したら、プログラマはその派生型に適切な型束縛プロシージャや型束縛変数を使うことができる。以下に具体例を示す。

なお、Oberon-2 の `WITH` 文と Pascal や Modula-2 の WITH 文は無関係である。以下のメソッドではレコードのフィールドへのアクセスを略記しているが、Oberon や Oberon-2 では実際にはこのような記法は使わない。

**型束縛**

``` oberon2
MODULE Birds;

    TYPE Bird* = RECORD
                     sound* : ARRAY 10 OF CHAR;
                 END;
END Birds.
(*-------------------------------------*)
MODULE Ducks;
    IMPORT Birds;

    TYPE Duck* = RECORD(Birds.Bird) END;

    PROCEDURE makeSound*( VAR bird: Duck );
    BEGIN COPY("Quack!", bird.sound); END makeSound;

END Ducks.
(*-------------------------------------*)
MODULE Cuckoos;
    IMPORT Birds;

    TYPE Cuckoo* = RECORD(Birds.Bird) END;

    PROCEDURE makeSound*( VAR bird: Cuckoo );
    BEGIN COPY("Cuckoo!", bird.sound); END makeSound;

END Cuckoos.
```

**`WITH` 文**

``` oberon2
MODULE Test;
  IMPORT Out, Birds, Cuckooo, Ducks;

    TYPE SomeBird* = RECORD ( Birds.Bird ) END;

    VAR sb : SomeBird;
    VAR c  : Cuckoos.Cuckoo;
    VAR d  : Ducks.Duck;

    PROCEDURE setSound*( VAR bird : Birds.Bird );
    BEGIN
        WITH bird : Cuckoos.Cuckoo DO
                    bird.sound := "Cuckoo!";
           | bird : Ducks.Duck DO
                    bird.sound := "Quack!";
        ELSE
                    bird.sound := "Tweet!";
        END;
    END setSound;

    PROCEDURE MakeSound* ( VAR b : Birds.Bird );
    BEGIN
    Out.Ln;
    Out.String( b.sound );
    Out.Ln;
    END MakeSound;

BEGIN

    setSound(c);
    setSound(d);
    setSound(sb);

    MakeSound(c);
    MakeSound(d);
    MakeSound(sb);

END Test.
```

**`POINTER`**

``` oberon2
MODULE PointerBirds;
   IMPORT Out;

   TYPE BirdRec*   = RECORD sound* : ARRAY 10 OF CHAR; END;
        DuckRec*   = RECORD(BirdRec) END;
        CuckooRec* = RECORD(BirdRec) END;

   TYPE Bird   = POINTER TO BirdRec;
        Cuckoo = POINTER TO CuckooRec;
        Duck   = POINTER TO DuckRec;

    VAR pb : Bird;
        pc : Cuckoo;
        pd : Duck;

    PROCEDURE makeDuckSound*( bird : Duck );
    BEGIN COPY("Quack!", bird.sound) END makeDuckSound;

    PROCEDURE makeCuckooSound*( bird : Cuckoo );
    BEGIN COPY("Cuckoo!", bird.sound) END makeCuckooSound;

    PROCEDURE makeSound*( bird : Bird );
    BEGIN
        WITH bird : Cuckoo DO makeCuckooSound(bird);
           | bird : Duck   DO makeDuckSound(bird)
          ELSE
            COPY("Tweet!", bird.sound);
        END;
    END makeSound;

BEGIN
   NEW(pc);
   NEW(pd);

   makeCuckooSound( pc );
   makeDuckSound( pd );

   Out.Ln;Out.String( pc^.sound );Out.Ln;
   Out.Ln;Out.String( pd^.sound );Out.Ln;

   makeSound( pc );
   makeSound( pd );

   Out.Ln;Out.String( pc^.sound );Out.Ln;
   Out.Ln;Out.String( pd^.sound );Out.Ln;
(* -------------------------------------- *)
(* Pass dynamic type to procedure         *)

   pb := pd;

   makeDuckSound( pb(Duck) );
   Out.Ln;Out.String( pb^.sound );Out.Ln;

   pb := pc;

   makeCuckooSound( pb(Cuckoo) );
   Out.Ln;Out.String( pb^.sound );Out.Ln;
(* -------------------------------------- *)

   makeSound(pb);
   Out.Ln;Out.String( pb^.sound );Out.Ln;

   pb := pd;

   makeSound(pb);
   Out.Ln;Out.String( pb^.sound );Out.Ln;
(* -------------------------------------- *)
   NEW(pb);

   makeSound(pb);
   Out.Ln;Out.String( pb^.sound );Out.Ln;

END PointerBirds.
```

第三の方法として、`IS` 演算子を使った方法もある。これは、等号（`=`）や不等号（`>`）などと同じ優先順位の関係演算子であるが、動的な型の検査を行う。しかし、上述の2つの方法とは異なり、検出した派生型によって処理を振り分けることはできない。

## 文法

[ALGOL](../Page/ALGOL.md "wikilink") - [Pascal](../Page/Pascal.md "wikilink") - [Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink") - [Oberon](../Page/Oberon.md "wikilink") - [Component Pascal](https://ja.wikipedia.org/wiki/Component_Pascal "wikilink") の系列の言語は文法を単純化させてきたと言える。Oberon-2 は[EBNF](../Page/EBNF.md "wikilink")を使って下記のように33の構文生成規則で表せる（*Mössenböck & Wirth, 1993*）。

``` ebnf
Module        = MODULE ident ";" [ImportList] DeclSeq [BEGIN StatementSeq] END ident ".".
ImportList    = IMPORT [ident ":="] ident {"," [ident ":="] ident} ";".
DeclSeq       = { CONST {ConstDecl ";" } | TYPE {TypeDecl ";"} | VAR {VarDecl ";"}} {ProcDecl ";" | ForwardDecl ";"}.
ConstDecl = IdentDef "=" ConstExpr.
TypeDecl = IdentDef "=" Type.
VarDecl = IdentList ":" Type.
ProcDecl = PROCEDURE [Receiver] IdentDef [FormalPars] ";" DeclSeq [BEGIN StatementSeq] END ident.
ForwardDecl = PROCEDURE "^" [Receiver] IdentDef [FormalPars].
FormalPars = "(" [FPSection {";" FPSection}] ")" [":" Qualident].
FPSection = [VAR] ident {"," ident} ":" Type.
Receiver = "(" [VAR] ident ":" ident ")".
Type = Qualident
              | ARRAY [ConstExpr {"," ConstExpr}] OF Type
              | RECORD ["("Qualident")"] FieldList {";" FieldList} END
              | POINTER TO Type
              | PROCEDURE [FormalPars].
FieldList = [IdentList ":" Type].
StatementSeq = Statement {";" Statement}.
Statement = [ Designator ":=" Expr
              | Designator ["(" [ExprList] ")"]
              | IF Expr THEN StatementSeq {ELSIF Expr THEN StatementSeq} [ELSE StatementSeq] END
              | CASE Expr OF Case {"|" Case} [ELSE StatementSeq] END
              | WHILE Expr DO StatementSeq END
              | REPEAT StatementSeq UNTIL Expr
              | FOR ident ":=" Expr TO Expr [BY ConstExpr] DO StatementSeq END
              | LOOP StatementSeq END
              | WITH Guard DO StatementSeq {"|" Guard DO StatementSeq} [ELSE StatementSeq] END
              | EXIT
              | RETURN [Expr]
      ].
Case = [CaseLabels {"," CaseLabels} ":" StatementSeq].
CaseLabels = ConstExpr [".." ConstExpr].
Guard = Qualident ":" Qualident.
ConstExpr = Expr.
Expr = SimpleExpr [Relation SimpleExpr].
SimpleExpr = ["+" | "-"] Term {AddOp Term}.
Term = Factor {MulOp Factor}.
Factor = Designator ["(" [ExprList] ")"] | number | character | string | NIL | Set | "(" Expr ")" | " ~ " Factor.
Set = "{" [Element {"," Element}] "}".
Element = Expr [".." Expr].
Relation = "=" | "#" | "<" | "<=" | ">" | ">=" | IN | IS.
AddOp = "+" | "-" | OR.
MulOp = " * " | "/" | DIV | MOD | "&".
Designator = Qualident {"." ident | "[" ExprList "]" | " ^ " | "(" Qualident ")"}.
ExprList = Expr {"," Expr}.
IdentList = IdentDef {"," IdentDef}.
Qualident = [ident "."] ident.
IdentDef = ident [" * " | "-"].
```

## 実装

  - [チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")では、Windows、Linux、Solaris、Mac OS X向けのOberon-2コンパイラを実装・保守している。
  - マンチェスター大学のStephen J. BevanによるOberon-2対応の[Lex](../Page/Lex.md "wikilink")（を使った）[字句解析器](https://ja.wikipedia.org/wiki/字句解析器 "wikilink")と[Yacc](../Page/Yacc.md "wikilink")（を使った）[構文解析器](../Page/構文解析器.md "wikilink")がある。現在のバージョンは1.4である。
  - [Programmer's Open Workbench](http://www.fim.uni-linz.ac.at/pow/Pow.htm) (POW\!) は、エディタ、リンカ、Oneron-2コンパイラを備えた単純な[統合開発環境](../Page/統合開発環境.md "wikilink")である。[Windows上の実行ファイルを生成する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。全ソースコードも提供されており、コンパイラ自体が Oberon-2 で書かれている。
  - [Java to Oberon Compiler](http://www.uni-vologda.ac.ru/JOB/) (JOB) は、ロシアの University of Vologda で書かれた Oberon-2 コンパイラである。生成するコードは[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")（[バイトコード](../Page/バイトコード.md "wikilink")）である。Java互換の専用クラスが提供されているが、全体としての階層構造はOberonのものである。
  - [Optimizing Oberon-2 Compiler](http://sourceforge.net/projects/ooc)は、一旦Cに変換し、gccを使ってオブジェクトを生成する。

## 参考文献

  - "Second International Modula-2 Conference", 1991年9月

## Oberon と Oberon-2 の変遷

  - "*[From Modula-2 to Oberon](ftp://ftp.inf.ethz.ch/pub/software/Oberon/OberonV4/Docu/ModToOberon.ps.gz)"* Wirth (1988)（PostScript形式を圧縮してある）
  - "*[The Programming Language Oberon](ftp://ftp.inf.ethz.ch/pub/software/Oberon/OberonV4/Docu/OberonReport.ps.gz)"* Wirth (1988)（PostScript形式を圧縮してある）
  - "*[Differences between Oberon and Oberon-2](ftp://ftp.inf.ethz.ch/pub/software/Oberon/OberonV4/Docu/Oberon2.Differences.ps.gz)"* Mössenböck and Wirth (1991)（PostScript形式を圧縮してある）
  - "*[The Programming Language Oberon-2](http://www-vs.informatik.uni-ulm.de:81/projekte/Oberon-2.Report/)*" H. Mössenböck, N. Wirth, Institut für Computersysteme, ETH Zürich ([ETHZ](../Page/チューリッヒ工科大学.md "wikilink")), January 1992
  - "*[Oberon Language Genealogy Tree](http://www.oberon.ethz.ch/genealogy.html)*" maintained at [ETHZ](../Page/チューリッヒ工科大学.md "wikilink")
  - "*[What's New in Component Pascal](http://www.oberon.ch/pdf/CP-New.pdf)*" (Changes from Oberon-2 to CP), Pfister (2001)

## 外部リンク

  - [Oberon Reference page at ETH-Zürich](http://www.oberon.ethz.ch/)
  - [Oberon at SSW, Linz](http://www.ssw.uni-linz.ac.at/Research/Projects/Oberon.html)
  - [The Oberon-2 Reflection Model and its Applications](http://www.ssw.uni-linz.ac.at/Research/Projects/Reflection/Reflection99/paper.ps)（PostScript形式）

[en:Oberon-2](https://ja.wikipedia.org/wiki/en:Oberon-2 "wikilink")

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink")