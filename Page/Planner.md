> この記事は[Planner](https://ja.wikipedia.org/wiki/Planner)から翻訳されています。


**Planner**（"PLANNER"とも表記される）は、[1969年](https://ja.wikipedia.org/wiki/1969年 "wikilink")に[MITの](../Page/マサチューセッツ工科大学.md "wikilink")[カール・ヒューイット](../Page/カール・ヒューイット.md "wikilink")が設計した[プログラミング言語](../Page/プログラミング言語.md "wikilink")。当初、サブセットの Micro-Planner や Pico-Planner が実装され、後に完全実装として Popler が登場。その後、派生言語として QA-4、Conniver、QLISP、Ether などが実装され、1970年代の[人工知能](../Page/人工知能.md "wikilink")研究の道具として重要な役割を果たし、商用の KEE や ART の開発にも影響を与えた。

当時[マービン・ミンスキー](../Page/マービン・ミンスキー.md "wikilink")、[シーモア・パパート](../Page/シーモア・パパート.md "wikilink")、Mike Peterson の学生だったヒューイットは、「知識の手続き的埋め込み」論者であり、高レベルの手続き的計画によるアプローチを信奉していた。当時、[ジョン・マッカーシー](../Page/ジョン・マッカーシー.md "wikilink")らは[人工知能](../Page/人工知能.md "wikilink")(AI)のための[知識表現](../Page/知識表現.md "wikilink")として[数理論理学](../Page/数理論理学.md "wikilink")を用いた宣言的かつ論理的アプローチを信奉しており、両者は対立関係にあった。このことは次のような基本的な疑問を生み出した。「手続き的アプローチと論理的アプローチの違いは何か?」である。これに答えが出せるようになるまで数年を要した。

## Plannerの初期の歴史

ヒューイット\[2006\]によれば、Planner は「手続き的計画; procedural plan」機能を持つ世界初の言語であり、これを「ゴール」と「[表明](../Page/表明.md "wikilink"); assertion」を使った「パターン管理呼び出し; pattern-directed invocation」と呼ぶ。Planner のサブセット Micro-Planner は Gerry Sussman、Eugene Charniak、[テリー・ウィノグラード](../Page/テリー・ウィノグラード.md "wikilink")らが実装し、ウィノグラードの自然言語理解プログラム [SHRDLU](../Page/SHRDLU.md "wikilink")、Eugene Charniak のストーリー理解のプロジェクトなどに使われた。これらの成果は人工知能分野を活気付かせた。また、当時主流であった論理的アプローチとは異なる手法を提案していたため、論争を呼ぶこととなった。

[エジンバラ大学](https://ja.wikipedia.org/wiki/エジンバラ大学 "wikilink")の Bruce Anderson は Planner のサブセット Pico-Planner を実装し、同じエジンバラ大学の Julian Davies は完全な Planner 言語処理系である Popler を実装した。[SRIでは](../Page/SRIインターナショナル.md "wikilink")、Jeff Rulifson、Jan Derksen、Richard Waldinger らは、Planner の文法をベースにしてデータベースの[モジュール性](https://ja.wikipedia.org/wiki/モジュール性 "wikilink")を提供する機構としてコンテキスト機構を導入した QA4 を開発した。同じ SRI の Earl Sacerdoti と Rene Reboh は QA4 を [InterLisp](https://ja.wikipedia.org/wiki/InterLisp "wikilink") 上に実装した QLISP を開発し、これをいくつかのアプリケーション開発に使用した。論理的アプローチ派の Robert Kowalski は Alain Colmerauer と共同で Micro-Planner によく似た [Prolog](https://ja.wikipedia.org/wiki/Prolog "wikilink") の開発に関わった。実際、ヒューイットは Prolog を Micro-Planner のサブセットの再発明とみなした。というのは、Prolog が単にパターンの一致によってゴールを得るだけなのに対して、Micro-Planner は手続き的計画を呼び出すこともできたからである。しかし、Kowalski 自身は Prolog を人工知能開発へのアプローチのひとつとして論理的パラダイムを保持するものと考えていた。

## 制御構造に関する議論

ヒューイット\[2006\]にもあるように、Planner 開発当時のコンピュータメモリは高価であり容量が小さかった。そこでメモリの使用を節約するため、制御構造として当時一般的だった[バックトラッキング](../Page/バックトラッキング.md "wikilink")を採用した。この手法では、コンピュータはいくつもの可能性のうちひとつだけをメモリに保持しておけばよかったのである。

この実装上の決断により、Micro-Planner は不運な結果を招くこととなった。[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")では `NIL` を空のリストを表すと同時に `false`（メモリ番地 0）を表すようにしている。というのも 0 かどうかのチェックが高速に行えるからである。このため、LISPプログラムでは `NIL`かどうかのチェックは非常に頻繁に行われる。Micro-Planner はこれを拡張して `NIL` をバックトラッキング開始のシグナルとしても扱った。Micro-Planner では、リストの各要素に何らかの処理をループで行うのが一般的だが、このとき先頭の要素をリストから除去した残りのリストを持ってループの先頭に分岐し、リストが空かどうかをチェックする。リストが空だった場合、プログラムは次の別の処理に分岐する。このようなプログラムで最後の要素が処理され、それをリストから取り除いた残りのリストが `NIL` になったとき、それをチェックする部分にはプログラムは到達しない。というのも、Micro-Planner は `NIL` に到達したときにそれをバックトラッキングのシグナルとして扱い、それまでリストの各要素に対して行った処理を取り消してしまうのである。このことに人々は驚かされた。

このことはバックトラッキングの扱いにくさを証明し、制御構造に関する議論が活性化されることとなった。ヒューイットは他の可能な実装方法を調査した。

### 制御構造のクラス分け

ヒューイットは Mike Paterson と共に、[再帰呼び出し](https://ja.wikipedia.org/wiki/再帰呼び出し "wikilink")(recursion)が繰り返し(iteration)よりも強力であること、[並列処理](https://ja.wikipedia.org/wiki/並列処理 "wikilink")が逐次的再帰よりも強力であることを証明した。ヒューイットは同時に[コルーチン](../Page/コルーチン.md "wikilink")が再帰よりも強力であると推測したが、最近の強力な形式手法を使うまでそれを証明できなかった。

### Hairy Control Structure

ヒューイット\[2006\]によれば、Peter Landin は **J** (Jump) 演算子を使って非常に強力な制御構造を導入した。これはプロシージャ呼び出しの途中に飛び込むことが可能なローカルでない goto である。実際、**J** 演算子は既にリターン済みのプロシージャ呼び出しの途中に分岐して戻ることができる。Drew McDermott と Gerald Sussman は、Landin のコンセプトを 「Hairy Control Structure; 複雑な制御構造（Hairy はハッカー用語。本来の意味は"毛深い"）」と呼び、Conniver 言語に実装した。Scott Fahlman はこれをロボット開発に活用した。このコンセプトは現在[再呼び出し可能な継続と呼ばれているものと関連している](../Page/継続.md "wikilink")。

### 制御構造はメッセージパッシングのパターンである

ヒューイットは次のように述べている。「…"Hairy control structure"（例えば CONNIVER のような可能性リスト、ローカルでない goto、他のプロシージャの内部変数への値の代入など）を使わない手法を発見した…通常のメッセージパッシングが問題解決モジュール間の協調動作に関して、より構造化され直観的な通信システムを構築する基礎となる。」すなわち、[アクターモデル](../Page/アクターモデル.md "wikilink")が人工知能の制御構造問題を解決する基礎となるとした。アクターモデルのためのプログラム方法論を開発するにはかなりの時間を要した。しかし、[Scientific Community Metaphorの実装には洗練されたメッセージパッシングを必要とし](https://ja.wikipedia.org/wiki/Scientific_Community_Metaphor "wikilink")、今も研究課題のひとつとなっている。

## 数理論理学の限界

制御構造の議論 はプログラミング言語としての[数理論理学](../Page/数理論理学.md "wikilink")の使用の可能性に関して議論を呼んだ。手続き的アプローチは、数理論理学とは異なる数学的意味論（[表示的意味論](../Page/表示的意味論.md "wikilink")参照）を持つ。数理論理学だけでは、非決定性を持つ並列システムや分散システムを記述できない。

## 参考文献

  - Carl Hewitt. **PLANNER: A Language for Proving Theorems in Robots** IJCAI 1969
  - Gerry Sussman and Terry Winograd. **[Micro-planner Reference Manual](http://hdl.handle.net/1721.1/5833)** AI Memo No, 203, MIT Project MAC, July 1970.
  - Terry Winograd. **[Procedures as a Representation for Data in a Computer Program for Understanding Natural Language](http://hdl.handle.net/1721.1/7095)** MIT AI TR-235. January 1971.
  - Carl Hewitt. **Procedural Embedding of Knowledge In Planner** IJCAI 1971.
  - Gerry Sussman, Terry Winograd and Eugene Charniak. **[Micro-Planner Reference Manual (Update)](http://hdl.handle.net/1721.1/6184)** AI Memo 203A, MIT AI Lab, December 1971
  - Carl Hewitt. **[Description and Theoretical Analysis (Using Schemata) of Planner, A Language for Proving Theorems and Manipulating Models in a Robot](http://hdl.handle.net/1721.1/6916)** AI Memo No. 251, MIT Project MAC, April 1972.
  - Bruce Anderson. **Documentation for LIB PICO-PLANNER** School of Artificial Intelligence, Edinburgh University. 1972
  - Bruce Baumgart. **Micro-Planner Alternate Reference Manual** Stanford AI Lab Operating Note No. 67, April 1972.
  - Eugene Charniak. **[Toward a Model of Children's Story Comprehension](http://hdl.handle.net/1721.1/6892)** MIT AI TR-266. December 1972.
  - Julian Davies. **Popler 1.6 Reference Manual** University of Edinburgh, TPU Report No. 1, May 1973.
  - Jeff Rulifson, Jan Derksen, and Richard Waldinger. **QA4, A Procedural Calculus for Intuitive Reasoning** SRI AI Center Technical Note 73, November 1973.
  - Robert Kowalski **Predicate Logic as Programming Language** Memo 70, Department of Artificial Intelligence, Edinburgh University. 1973
  - Pat Hayes. **Computation and Deduction** Mathematical Foundations of Computer Science: Proceedings of Symposium and Summer School, Štrbské Pleso, High Tatras, Czechoslovakia, September 3-8, 1973.
  - Carl Hewitt, Peter Bishop and Richard Steiger. **A Universal Modular Actor Formalism for Artificial Intelligence** IJCAI 1973.
  - Drew McDermott and Gerry Sussman. **[The Conniver Reference Manual](http://hdl.handle.net/1721.1/6204)** MIT AI Memo 259A. January 1974.
  - Earl Sacerdoti, et. al., **QLISP A Language for the Interactive Development of Complex Systems** AFIPS. 1976
  - William Kornfeld and Carl Hewitt. **[The Scientific Community Metaphor](http://hdl.handle.net/1721.1/5693)** MIT AI Memo 641. January 1981.
  - Carl Hewitt. **The Challenge of Open Systems** Byte Magazine. April 1985
  - Robert Kowalski. **The limitation of logic** Proceedings of the 1986 ACM fourteenth annual conference on Computer science.
  - Robert Kowalski. **The Early Years of Logic Programming** CACM January 1988.
  - Carl Hewitt and Gul Agha. **Guarded Horn clause languages: are they deductive and logical?** in Artificial Intelligence at MIT, Vol. 2. MIT Press 1991.
  - Carl Hewitt. **The repeated demise of logic programming and why it will be reincarnated** What Went Wrong and Why: Lessons from AI Research and Applications. Technical Report SS-06-08. AAAI Press. March 2006.

## 外部リンク

  - [Alain Colmerauer's and Philippe Roussel's 1992 account of the birth of Prolog](http://www.lim.univ-mrs.fr/~colmer/ArchivesPublications/HistoireProlog/19november92.pdf)

[Category:人工知能](https://ja.wikipedia.org/wiki/Category:人工知能 "wikilink") [Category:論理プログラミング言語](https://ja.wikipedia.org/wiki/Category:論理プログラミング言語 "wikilink") [Category:ロボットプログラミング言語](https://ja.wikipedia.org/wiki/Category:ロボットプログラミング言語 "wikilink") [Category:形式手法](https://ja.wikipedia.org/wiki/Category:形式手法 "wikilink") [Category:定理証明ソフトウェア](https://ja.wikipedia.org/wiki/Category:定理証明ソフトウェア "wikilink")