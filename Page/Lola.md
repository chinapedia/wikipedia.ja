> この記事は[Lola](https://ja.wikipedia.org/wiki/Lola)から翻訳されています。


**Lola** は、[同期式](https://ja.wikipedia.org/wiki/同期_\(計算機科学\)#ハードウェアにおける同期 "wikilink")[デジタル回路](../Page/デジタル回路.md "wikilink")を記述するよう設計された単純な[ハードウェア記述言語](../Page/ハードウェア記述言語.md "wikilink")。[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")が開発した言語で、[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")の教授時代に[計算機科学](../Page/計算機科学.md "wikilink")の学生に[FPGA](../Page/FPGA.md "wikilink")上のデジタル設計について教える道具として作ったものである。

Lola ではハードウェア部品の構造と機能を静的に記述し、部品間の接続を記述する。Lola のテキストは宣言と文から構成される。信号設定の形で[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")レベルでハードウェアを記述する。信号は演算器を使って統合され別の信号となる。信号とその割り当ては型としてグループ化される。型のインスタンスがハードウェア部品となる。[型を他の型の組み合わせで構成することもでき](../Page/データ型.md "wikilink")、それによって階層的設計が可能で、[ジェネリックプログラミング](../Page/ジェネリックプログラミング.md "wikilink")の一種ということもできる（例えば、ワード幅の回路をパラメータ化するなど）。

以上のような概念は下記の例（二進加算器回路）に示されている。まず基本構成要素（`TYPE Cell`）が定義され、次にその `Cell` を使ってワード幅 8 ビットのカスケードを宣言し、最後に複数の `Cell` を相互接続する。ここで定義されている `MODULE Adder` はより高次の設計の構成要素として使用可能である。

    MODULE Adder;

    TYPE Cell; (* Composite Type *)
      IN x,y,ci:BIT; (* input signals *)
      OUT z,co:BIT; (* output signals *)
      BEGIN
      z:=x-y-ci;
      co:=x*y+x*ci+y*ci;
    END Cell;

    CONST N:=8;
    IN X,Y:[N]BIT; ci:BIT; (* input signals *)
    OUT Z:[N]BIT; co:BIT; (* output signals *)
    VAR S:[N]Cell; (* composite type instances *)
    BEGIN
      S.0(X.0, Y.0, ci); (* inputs in cell 0*)
      FOR i:=1..N-1 DO
        S.i(X.i,Y.i,S[i-1].co); (* inputs in cell i *)
      END;
      FOR i:=0..N-1 DO
        Z.i:=S.i.z;
    END;
      co:=S.7.co;
    END Adder.

ヴィルトは、自著 [*Digital Circuit Design*](http://www.cs.inf.ethz.ch/~wirth/books/DigitalDesign/) で Lola のユーザーから見た説明を行っている。Lola コンパイラの中身の詳細はヴィルトの技術レポート [*Lola System Notes*](ftp://ftp.inf.ethz.ch/pub/publications/tech-reports/2xx/236.ps.gz) にある。デジタル設計に関するツール全体の概要は技術レポート [*Tools for Digital Circuit Design using FPGAs*](ftp://ftp.inf.ethz.ch/pub/publications/tech-reports/2xx/215.ps.gz) にある（Lola に関するレポート *Lola: An Object-Oriented Logic Description Language* も含まれている）。

## 外部リンク

  - [Lola language page](http://www.cs.inf.ethz.ch/projects/lola/lola_lang/)（[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")）

[Category:ハードウェア記述言語](https://ja.wikipedia.org/wiki/Category:ハードウェア記述言語 "wikilink")