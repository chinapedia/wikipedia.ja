> この記事は[Interlisp](https://ja.wikipedia.org/wiki/Interlisp)から翻訳されています。


**Interlisp**（大文字/小文字の組み合わせは様々見られる）は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の一種を中心としたプログラミング環境。1967年、[Bolt, Beranek and Newman](../Page/BBNテクノロジーズ.md "wikilink") (BBN) で[PDP-10](../Page/PDP-10.md "wikilink")（OSは[TENEX](../Page/TOPS-20.md "wikilink")）上の BBN LISP として開発開始されたものである。[Danny Bobrow](https://ja.wikipedia.org/wiki/:en:Daniel_G_Bobrow "wikilink")、[Warren Teitelman](https://ja.wikipedia.org/wiki/:en:Warren_Teitelman "wikilink")、[Ronald Kaplan](https://ja.wikipedia.org/wiki/:en:Ronald_Kaplan "wikilink") がBBNから[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")に移った際に、それを Interlisp と改称した。Interlispは[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")を中心とする[DARPAコミュニティの](../Page/国防高等研究計画局.md "wikilink")[人工知能](../Page/人工知能.md "wikilink")研究者らに広まっていった。Interlisp で特筆すべきは、プログラミング環境に対話型開発ツールを統合したことであり、[デバッガ](../Page/デバッガ.md "wikilink")、簡単な間違いを自動訂正するツール（\[1\] - "do what I mean"）、解析ツールなどが統合されていた。

## 適応

[パロアルト研究所](../Page/パロアルト研究所.md "wikilink")では移植性を高めるため、"Interlisp virtual machine" と呼ばれる[仮想機械](../Page/仮想機械.md "wikilink")が定義された。しかし、これは移植の基盤としては便利ではなかった。

[Peter Deutsch](https://ja.wikipedia.org/wiki/:en:L._Peter_Deutsch "wikilink") はInterlispのためのバイトコード型命令セットを定義し、[Xerox Alto](../Page/Alto.md "wikilink") にてマイクロプログラム方式のエミュレータとして実装。その後一連のワークステーションに移植され、Xerox 1108 や 1186 といった商用[LISPマシン](../Page/LISPマシン.md "wikilink")に採用されパロアルト研究所内でも使用された。それらの実装はまとめて **Interlisp-D** と呼ばれている。後期の製品は、[ANSI規格の](../Page/米国国家規格協会.md "wikilink") [Common Lisp](../Page/Common_Lisp.md "wikilink") の処理系 Xerox Common Lisp を搭載している。Interlisp-D の[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")機能 LOOPS は、[シンボリックス](https://ja.wikipedia.org/wiki/シンボリックス "wikilink")のと共に [Common Lisp Object System](../Page/Common_Lisp_Object_System.md "wikilink") の元になった。

PDP-10版Interlispは **Interlisp-10** と呼ばれるようになり、BBNではLISPマシン Jerico 向けの **Interlisp-Jericho** も開発された（製品化せず）。[1982年](../Page/1982年.md "wikilink")、[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")の[情報科学研究所](https://ja.wikipedia.org/wiki/情報科学研究所 "wikilink") (ISI) とパロアルト研究所が共同で[VAX](../Page/VAX.md "wikilink")上の[BSD](../Page/BSD.md "wikilink")に移植し、**Interlisp-VAX** と呼んだ\[2\]。

1981年、パロアルト研究所の Warren Teitelman と Larry Masinter が IEEE Computer 誌にInterlispの概要と設計哲学についての記事を発表している\[3\]。

1985年から87年にかけて、[富士ゼロックス](../Page/富士ゼロックス.md "wikilink")がバイトコード・インタプリタのC言語による実装を開発し、[サニーベールの](https://ja.wikipedia.org/wiki/サニーベール_\(カリフォルニア州\) "wikilink") Xerox AI Systems (XAIS) と共同で[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の [SPARC](../Page/SPARC.md "wikilink") 4 アーキテクチャ上にその環境とエミュレータを移植した。同年、ゼロックス社の中でも赤字部門だった XAIS はスピンオフされ Envos 社となったが、すぐに倒産した。

[1992年](../Page/1992年.md "wikilink")、[ACM](../Page/Association_for_Computing_Machinery.md "wikilink") [ソフトウェアシステム賞が](https://ja.wikipedia.org/wiki/ACMソフトウェアシステム賞 "wikilink") Interlisp の先駆的功績に対して与えられた。受賞者は、Daniel G. Bobrow、Richard R. Burton、L. Peter Deutsch、Ronald M. Kaplan、Larry Masinter、Warren Teitelman。

## 脚注

## 関連文献

  - Warren Teitelman *et al.*, *Interlisp Reference Manual* (Xerox tech report, 1974)
  - J Strother Moore, *The Interlisp Virtual Machine Specification* (Xerox tech report, 1976)
  - L Peter Deutsch, *A LISP Machine with Very Compact Programs* (Third Joint Conference on Artificial Intelligence, 1973).
  - Kaisler, S. H. 1986 Interlisp: the Language and its Usage. Wiley-Interscience.

## 外部リンク

  - [Archived Interlisp documentation at bitsavers.org](http://bitsavers.org/pdf/xerox/interlisp/)
  - [LISPF4](http://blake.mcbride.name/software/lispf4/index.html) - Mats Nordstrom が[FORTRAN](../Page/FORTRAN.md "wikilink")で書いた Interlisp のインタプリタ。後に Blake McBride が[C言語](../Page/C言語.md "wikilink")で移植（[Windowsおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[Linux](../Page/Linux.md "wikilink")）
  - [Interlisp documentation at Computer History Museum](http://www.softwarepreservation.org/projects/LISP/interlisp).

[Category:LISP](https://ja.wikipedia.org/wiki/Category:LISP "wikilink")

1.  Teitelman, Warren, "Do What I Mean": the programmer's assistant," Computers and Automation, pp. 8-11, April 1972.
2.
3.  Warren Teitelman, Larry M. Masinter. [The Interlisp Programming Environment](http://larry.masinter.net/interlisp-ieee.pdf). IEEE Computer, April 1981.