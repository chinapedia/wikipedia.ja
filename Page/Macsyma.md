> この記事は[Macsyma](https://ja.wikipedia.org/wiki/Macsyma)から翻訳されています。


**Macsyma** (Project MAC’s SYmbolic MAnipulator\[1\]) は、1968年から1982年まで[MITの](../Page/マサチューセッツ工科大学.md "wikilink") [Project MAC](https://ja.wikipedia.org/wiki/Project_MAC "wikilink") の一環として開発された[数式処理システム](../Page/数式処理システム.md "wikilink")であり、その後商用化された。世界初の数式処理システムで、初期の[エキスパートシステム](../Page/エキスパートシステム.md "wikilink")の1つであり、その様々なアイデアが後の [Mathematica](../Page/Mathematica.md "wikilink") や [Maple](../Page/Maple.md "wikilink") といったシステムに影響を与えた。

## 開発

1968年7月、カール・エンゲルマン\[2\]、（フロントエンド、数式表示、多項式算術）、[ジョエル・モーゼス](../Page/ジョエル・モーゼス.md "wikilink")（簡約化、不定積分、ヒューリスティックス）によりプロジェクトが始まった。1971年までのプロジェクト責任者はマーティンで、モーゼスがその後10年間責任者を務めた。エンゲルマンと彼のスタッフは1969年に [MITRE Corporation](https://ja.wikipedia.org/wiki/:en:Mitre_Corporation "wikilink") に戻っている\[3\]。その後、様々な人々が開発に関与した。

使用言語は [Maclisp](../Page/Maclisp.md "wikilink") で、Maclisp を数値計算向きに改良する主な動機となった。Maclisp は[PDP-6](../Page/PDP-6.md "wikilink")および[PDP-10](../Page/PDP-10.md "wikilink")が主なプラットフォームだったが、[Multics](../Page/Multics.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")や[LISPマシン](../Page/LISPマシン.md "wikilink")アーキテクチャでも動作した。Macsyma は当時としては大規模な[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")プログラムの1つだった。

### 商用化

1979年、当時[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink") (UCB) の教授だったリチャード・フェイトマンの要望で、MITは Macsyma のコードの一時的ライセンスを提供した。これを使い、フェイトマンの研究室で Maclisp から派生させた  を使い、 上にすぐさま移植した。MITは、適切なライセンス条件の交渉が完了した際には現状の一時的ライセンスは破棄されるという条件で、UCBが VAX 版 Macsyma を[カリフォルニア工科大学](../Page/カリフォルニア工科大学.md "wikilink")など約50の大学に配布することをしぶしぶ許可した。実際、後述するシンボリックスとの契約が成立した際に従来のライセンスは破棄された。するとシンボリックスは[VAX](../Page/VAX.md "wikilink")製品が同社の[LISPマシン](../Page/LISPマシン.md "wikilink")と性能的に競合することからVAX版Macsymaのライセンス提供を渋り、結局5年間VAX版のライセンスを提供しなかった。UCBはさらに[サンのワークステーションなど](../Page/サン・マイクロシステムズ.md "wikilink")[MC68000](../Page/MC68000.md "wikilink")を使ったシステムにもMacsymaを移植した。同じころフェイトマンは、破棄された当初のライセンスを恒久化すべく働きかけていた。

最終的に1982年、[アメリカ合衆国エネルギー省](../Page/アメリカ合衆国エネルギー省.md "wikilink") (DoE) はMITに対して National Energy Software Center (NESC) ライブラリにコピーをリリースさせるという条件と引き換えに、高い価格設定と再配布禁止というライセンス条件をMITが設定することを許可した。これはシンボリックスへの技術移転を保護することを意図したものだった（そのような制限は2002年ごろ撤廃された）。このいわゆる DOE Macsyma はMITが [Common Lisp](../Page/Common_Lisp.md "wikilink") の前身である [NIL](https://ja.wikipedia.org/wiki/NIL_\(プログラミング言語\) "wikilink") で書き直したもので、当時学界で主流だった [Berkeley VAX Unix](../Page/BSD.md "wikilink") ではなく、人気のない [VAX/VMS](../Page/OpenVMS.md "wikilink") で動作した。DOE Macsyma は後のオープンソースの Maxima の基礎となった。

1981年、モーゼスとリチャード・パヴェル（MIT職員で、Macsymaを工学や科学に適用することを提案した）は Macsyma を商用化するための会社を創業しようとした。パヴェルは Macsyma を使った科学的論文を多数書いていた。そうした論文を手に、パヴェルとモーゼスは出資に興味を示したいくつかのベンチャーキャピタルを訪れた。契約が成立しそうになったころ、MITはMITの人間がMITでの開発で直接利益を得るべきではないと決定した。1982年初め、MIT は Macsyma を[アーサー・D・リトル](../Page/アーサー・D・リトル.md "wikilink") (ADL) にライセンス供与し、同社が Macsyma の仲買人となり、1982年後半には Macsyma を[シンボリックス](../Page/シンボリックス.md "wikilink")にライセンス供与した。この間にADLによってモーゼスが締め出され、パヴェルがシンボリックスのMacsyma部門のトップに就任することになった。シンボリックスはMacsymaを独占することにはそれほど興味がなく、競合する[LISPマシン](../Page/LISPマシン.md "wikilink")企業  もライセンス供与を受けている。シンボリックスとADLの契約では、Macsymaの売り上げの15%をロイヤリティとしてADLに支払うことになっていた。この法外なロイヤリティは、Macsyma が絶対に売れるとMITとADLが考えていたことの表れである。シンボリックスでは[LISPマシン](../Page/LISPマシン.md "wikilink")を売るのが本業と考えていたが、Macsyma の開発も継続していた。Macsyma およびそれを搭載したLISPマシンの売り上げは2年以内にシンボリックスの売り上げ全体の10%を占めるようになっていった。シンボリックス社内からは多くの抵抗があったが、1980年代初めから中ごろに Macsyma をバークレーの Franz Lisp で書いたものが[DECの](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")[VAX](../Page/VAX.md "wikilink")やサンのワークステーション向けにリリースされた。

他社のコンピュータ向けにも Macsyma が販売されるようになると、Macsyma を搭載したシンボリックスのLISPマシンの売り上げが低下していった。市場自体は成長しているにも関わらず、1986年上半期の Macsyma の売り上げは、1985年上半期の売り上げより低下した。数式処理という点では明らかに Macsyma の方が優れていたが、そのころ[スティーブン・ウルフラム](../Page/スティーブン・ウルフラム.md "wikilink")の[SMPや](https://ja.wikipedia.org/wiki/:en:Symbolic_Manipulation_Program "wikilink")[ウォータールー大学](../Page/ウォータールー大学.md "wikilink")の[Maple](../Page/Maple.md "wikilink")が売り上げを伸ばしていた。

パヴェルはシンボリックスの Macsyma 部門を1986年初めごろまで指揮していた。1986年後半にはリチャード・ペッティに引き継がせ、シンボリックス社内の衝突を避けるため、経営陣は Macsyma の販売を減らす方針を採用した。Macsyma部門の従業員数は削減されたが、営業部門は強化し、顧客が求める機能を開発することに集中するようにした。例えば、[グレブナー基底](https://ja.wikipedia.org/wiki/グレブナー基底 "wikilink")を求めるアルゴリズムは1970年代にMITで発展したが、1987年まで製品版 Macsyma にそれが搭載されることはなかった。1987年、Macsyma の年間売り上げはほぼ倍増した。マニュアルやオンラインヘルプが改良され、コマンド名をさらに覚えやすくし、Macsyma は格段に使いやすくなっていった。ペッティはシンボリックス経営陣に対して、Macsyma はハードウェア部門の戦略とは切り離して出資されるべき戦略事業単位だと主張した。しかし、シンボリックスはその後も Macsyma 部門の人員を削減している。シンボリックスは多大な赤字を出しているハードウェア部門の赤字補填のドル箱として Macsyma を使おうとした。

Macsyma の最大の弱点は[数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")能力の低さだった。数式処理は難しいタスクだが、数値解析はより大きな科学技術計算市場に参入する際に重要となる。MIT版 Macsyma は数値計算ライブラリ [IMSL](../Page/IMSL.md "wikilink") とリンクしていたが、シンボリックス版 Macsyma ではこのリンクは難しかった（LISPマシン向けのIMSLがない）。シンボリックスのLISP開発者は数値解析を古い技術だと信じていて、LISPの用途としては重要でないと考えていたため、その方面の強化を怠っていた。[PC版](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink") Macsyma の[倍精度](https://ja.wikipedia.org/wiki/倍精度 "wikilink")演算は、[FORTRAN](../Page/FORTRAN.md "wikilink")の6倍の時間がかかった。また行列をリストのリストとして実装していたため、重要なアルゴリズムの性能低下の要因となっていた。Macsyma には[LU分解](../Page/LU分解.md "wikilink")のような数値線形代数の基本アルゴリズムも備わっていなかった。

1987年から1988年にかけて、Gold Hill Lisp を使ったPC版 Macsyma をリリースしようとした。一般的なコンピュータ向けにLISPコンパイラを開発することはシンボリックスにとって本業であるLISPマシンと競合する相手を作るようなもので、シンボリックス経営陣はそのプロジェクトをやめさせた。しかし、プロジェクトは経営陣には無断で続行された。ところがこの Gold Hill Lisp は非常に不安定で、アーキテクチャに問題があるためバグ修正も難しかった。これが Macsyma にとっては致命傷となった。1988年中ごろに[Mathematica](../Page/Mathematica.md "wikilink")の[Macintosh](../Page/Macintosh.md "wikilink")版が登場したとき、PC版Macsymaを対抗してリリースすることができなかった。[Windows版Macsymaは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、シンボリックスが開発した CLOE Lisp を使って1989年8月にリリースされた。しかしそのころ Macsyma 部門の人員はあまりに少なく、[Mathematica](../Page/Mathematica.md "wikilink")が備えていたグラフィックス描画機能、ノートブック・インタフェース、数値演算機能などに対抗できるものを実装できなかった。

1989年、シンボリックスは製品戦略の失敗から事業を整理統合する必要に迫られた。ペッティは Macsyma 部門を独立させようとしたがMITから資金協力を得られなかった。1988年末、ペッティは経営陣にソフトウェア専業への移行を進言したが、受け入れられなかった。そこで新たな企業を創業するためペッティはシンボリックスを退社した。

### Macsyma, Inc.

1992年、[シンボリックス](../Page/シンボリックス.md "wikilink")の創業者の1人（会長）とリチャード・ペッティ（社長）が Macsyma, Inc. を創業。シンボリックスから Macsyma の権利を買い取った。市場は急激に成長していたが、Macsyma の売り上げは1991年から1992年初めにかけても急激に落ち込んでいた。数式処理ソフトウェアにおけるMacsymaのシェアは、1987年には70%だったものが、1992年には1%となっている。1993年に市場の成長がおさまったころには、Mathematica と Maple がほとんどを占めるようになっていた。1990年代を通して、Macsyma, Inc. の開発要員は競合他社の4分の1から8分の1だった。

1995年初め、様々な改良を施した Macsyma 2.0.5 をリリース。Wester による数式処理システムの大規模な評価によると、Macsyma 2.0.5 は Maple より10%、Mathematica より15%性能がよいとされている\[4\]。Macsyma 2.0.5 の数値演算性能は相変わらず低かったが、数値解析および線形代数のルーチンは大幅に強化されていた。1996年には [LAPACK](../Page/LAPACK.md "wikilink") を採用し、数値線形代数の性能も強化された。

しかし開発チームの人員の少なさから、性能上の優位を継続的に維持することはできなかった。市場シェアは2%を越えることはなかった。1999年、Macsyma, Inc. はシンボリックスも買収した企業 Tenedos LLC に買収された。この企業が Macsyma を販売することはなかったが、シンボリックスがMacsymaの販売を継続している。

## 入手可能なバージョン

[Maxima](../Page/Maxima.md "wikilink") は1982年版の DOE Macsyma をベースとした[GPLライセンス版であり](../Page/GNU_General_Public_License.md "wikilink")、後に [William Schelter](https://ja.wikipedia.org/wiki/:en:William_Schelter "wikilink") が [Common Lisp](../Page/Common_Lisp.md "wikilink") で書き直し強化を施していった。今も盛んに開発が続いている。[GNU/Linux](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") などのシステム向けの[GUIも備えた実行ファイル版がダウンロード可能である](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。1982年以降の商用版 Macsyma での強化をほとんど含んでいないが、オープンソースであるため様々な機能が追加されてきた。そのため Macsyma と Maxima には非互換があるが、Macsymaの代数言語で書かれたものはほぼ変更なく両方のシステムで実行可能である。

## 脚注

## 外部リンク

  - [Richard Petti's summary of the history of commercial Macsyma](http://www.math.utexas.edu/pipermail/maxima/2003/005861.html) 30 October 2003
  - [The Macsyma Saga](http://www.math.utexas.edu/pipermail/maxima/2003/005884.html) Richard Petti, 2 November 2003
  - [Symbolics Macsyma](http://www.symbolics-dks.com/Macsyma-1.htm)

[Category:数式処理システム](https://ja.wikipedia.org/wiki/Category:数式処理システム "wikilink") [Category:Linux向け数式処理システム](https://ja.wikipedia.org/wiki/Category:Linux向け数式処理システム "wikilink") [Category:1968年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1968年のソフトウェア "wikilink")

1.
2.
3.  . See also
4.   Wester's 1995 review and 1999 review