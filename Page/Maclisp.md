> この記事は[Maclisp](https://ja.wikipedia.org/wiki/Maclisp)から翻訳されています。


**MacLISP**（または **MACLISP**）は、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")の一種。初期の[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")に基づき、[1960年代](../Page/1960年代.md "wikilink")後半、[MITの](../Page/マサチューセッツ工科大学.md "wikilink") [Project MAC](https://ja.wikipedia.org/wiki/Project_MAC "wikilink") で開発された。[リチャード・グリーンブラット](https://ja.wikipedia.org/wiki/リチャード・グリーンブラット "wikilink")がメインプログラマとして [PDP-6](../Page/PDP-6.md "wikilink") 向けのコードベースを書き、その後の保守や開発は Jon L. White が担当した。'MacLISP' と呼ばれるようになったのは[1970年代](../Page/1970年代.md "wikilink")に入ってからで、PDP-6 上に他の LISP 処理系も登場したためである（BBN Lisp）。

MacLISP は [DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") [PDP-6/10](../Page/PDP-10.md "wikilink") 上で動作した。当初[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")としては [ITS](../Page/Incompatible_Timesharing_System.md "wikilink") だけだったが、後には PDP-10 上の他のOSでも動作するようになった。当初の実装は PDP-10 の[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")で書かれていたが、後に [Multics](../Page/Multics.md "wikilink") 上に [PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink") を使って移植されている。MacLISP では、他の言語処理系ならバージョン番号がどんどん大きくなるような大幅な機能追加が継続的に行われた。

MacLISP は[数式処理システム](../Page/数式処理システム.md "wikilink") [Macsyma](../Page/Macsyma.md "wikilink") の実装に使われ、逆に Macsyma の一部機能が MacLISP に導入された。[SHRDLU](../Page/SHRDLU.md "wikilink") の実装にも使われ、[1980年代](../Page/1980年代.md "wikilink")初期まで[人工知能](../Page/人工知能.md "wikilink")研究でよく使われた。[Planner](../Page/Planner.md "wikilink") や [Scheme](../Page/Scheme.md "wikilink") など他のプログラミング言語の実装ベースとしても使われた。また、Multics 上の MacLISP は、LISPベースの[Emacs](../Page/Emacs.md "wikilink")の実装に使われた。

MacLISP は様々な影響を及ぼしたが、現在ではほとんど保守されていない。しかし、PDP-10 [エミュレータ](../Page/エミュレータ.md "wikilink")上では動作するので、古いAIプログラムを実行してみることはできる。

MacLISP には当初、少数の決まったデータ型しかなかった。CONSセル、アトム（当時はシンボルと呼ばれた）、[整数](../Page/整数.md "wikilink")、[浮動小数点数](../Page/浮動小数点数.md "wikilink")だけである。その後、[配列](../Page/配列.md "wikilink")、[多倍長整数](https://ja.wikipedia.org/wiki/多倍長整数 "wikilink")、[文字列](../Page/文字列.md "wikilink")、[タプル](../Page/タプル.md "wikilink")が追加された。整数以外のオブジェクトはポインタとして実装されており、そのデータ型はポインタが指したアドレスの範囲で判断されていた。

プログラムは[インタプリタ](../Page/インタプリタ.md "wikilink")でも[コンパイラ](../Page/コンパイラ.md "wikilink")でも実行可能である。コンパイラは変数スコープが制限される点と、[CAR や CDRといったインライン処理でエラーチェックをしない以外はインタプリタと変わらない](https://ja.wikipedia.org/wiki/CARとCDR "wikilink")。1970年代中ごろ、数値演算性能を強化したコンパイラが登場した。これにより、整数演算では[FORTRAN](../Page/FORTRAN.md "wikilink")と同程度の性能が実現された（ただし、配列やループの実装はFORTRANの方が高速だった）。

初期のバージョンは PDP-10 のアドレス範囲である 18ビットで制限されており、様々な実装上の制限があった。Multics では、より大きな[アドレス空間](../Page/アドレス空間.md "wikilink")が使えたが、Multics システム自体が数少なかった。人工知能で必要とするメモリ量と性能が PDP-10 の限界を超えたころ、[LISPマシン](../Page/LISPマシン.md "wikilink")が開発された。このため、LISPマシン上のLISPは MacLISP の後継に当たる。その他のLISP処理系も様々なコミュニティで作られ、最終的にこれらを統合した [Common Lisp](../Page/Common_Lisp.md "wikilink") が生まれることとなった。

MacLISP という名称は Project MAC に由来しており、アップルの [Macintosh](../Page/Macintosh.md "wikilink") とは無関係である。Macintosh 用のLISP処理系としては MCL (Macintosh Common Lisp） があるが、MacLISP とは関係ない。

## 参考文献

  - スティーブン・レビー（著）、古橋芳恵・松田信子（訳）、『ハッカーズ』、1987年、工学社、ISBN 978-4-87593-100-3

## 外部リンク

  - [MACLISP.info: The Pitmanual](http://maclisp.info/)
  - [MacLisp manual](http://zane.brouhaha.com/~healyzh/doc/lisp.doc.txt)
  - [The Multics Maclisp compiler](http://www.multicians.org/lcp.html)

[Category:LISP](https://ja.wikipedia.org/wiki/Category:LISP "wikilink")