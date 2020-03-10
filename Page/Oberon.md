> この記事は[Oberon](https://ja.wikipedia.org/wiki/Oberon)から翻訳されています。


**Oberon**（オベロン）は、[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")の[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")率いるチームが設計開発した[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")と[プログラミング言語](../Page/プログラミング言語.md "wikilink")の名称。[天王星](../Page/天王星.md "wikilink")の衛星[オベロンに由来する](https://ja.wikipedia.org/wiki/オベロン_\(衛星\) "wikilink")\[1\]。

## Oberon オペレーティングシステム

[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")としてのOberonは1980年代後半、[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")で同名の言語を使って開発された。独自のテキストベースの[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")でコマンドを起動する。

### 歴史

[NS32032ベースの](https://ja.wikipedia.org/wiki/NS320xx "wikilink")ワークステーションプロジェクトの一部として開発された。同名の[プログラミング言語](../Page/プログラミング言語.md "wikilink")で記述されている\[2\]。基本システムは[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")と Jürg Gutknecht が設計・実装し、その全貌が彼らの著書 "Project Oberon" で詳述されている\[3\]。その後、チューリッヒ工科大学のチームにより他のハードウェアにも移植され、雑誌などにも紹介されている\[4\]\[5\]\[6\]\[7\]\[8\]。

### ユーザインタフェース

Oberonの[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")は[テキストユーザインタフェース](https://ja.wikipedia.org/wiki/テキストユーザインタフェース "wikilink") (TUI) だった。[GUIの便利さと](https://ja.wikipedia.org/wiki/グラフィカルユーザインターフェース "wikilink")[CUIの記述能力を兼ね備えており](../Page/キャラクタユーザインタフェース.md "wikilink")、Oberon 言語の命名規則と密接に関連している。画面に表示されるあらゆるテキストを編集可能で、それをコマンド入力に使うことができる。[コマンドプロンプト](../Page/コマンドプロンプト.md "wikilink")のようなものは必要とされない。一般的なCUIとは大幅に異なるが、そのTUIは非常に効率的で強力である\[9\]。ただし、慣れるまで時間がかかる。その使用法とプログラミングについては Martin Reiser の著書 "The Oberon System" が詳しい\[10\]。この方式は後のオペレーティングシステムに影響を与えたとは言えないが、[ロブ・パイク](../Page/ロブ・パイク.md "wikilink")の[Acme](https://ja.wikipedia.org/wiki/Acme "wikilink") ([Plan 9](../Page/Plan_9_from_Bell_Labs.md "wikilink")) に強い影響を与えた。[Macintosh Programmer's Workshop](https://ja.wikipedia.org/wiki/:en:Macintosh_Programmer's_Workshop "wikilink") のインタフェースと似ているが、Oberonはヴィルトの以前のプロジェクトである[Lilith](../Page/Lilith.md "wikilink")に基づいており、[Macintosh](../Page/Macintosh.md "wikilink")とLilithはどちらも [Alto](../Page/Alto.md "wikilink") に触発されたものだという経緯がある。

### バージョン

Oberon OS は、一般に無料でいくつかのプラットフォーム上で動作する。非常に小型である。Oberon 言語コンパイラ、各種ユーティリティ、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")ネットワーク、GUIなど全てのパッケージを入れても 3.5インチ[フロッピーディスク](../Page/フロッピーディスク.md "wikilink")1枚に納まる。[IBM PC互換機で動作するバージョンを](https://ja.wikipedia.org/wiki/IBM_PC "wikilink") Native Oberon と呼ぶ。

ヴィルトの開発したオリジナルに近いバージョンとして Oberon V4 がある。これもチューリッヒ工科大学で開発されたが、最新版は[リンツ大学](http://www.ssw.uni-linz.ac.at/Oberon.html)にある。ただし、2000年以降開発が停止している。

チューリッヒ工科大学は近年、動的オブジェクトとOSの[並行性](../Page/並行性.md "wikilink")の研究に注力しており、新たな Active Object Oberon という言語とそれを使ったOSをリリースした。そのOSは当初 AOS と呼ばれていたが、現在は A2 または [Bluebottle](https://ja.wikipedia.org/wiki/:en:Bluebottle_OS "wikilink") と呼称されている。チューリッヒ工科大学のサイトでは大部分のソースと共にこれを公開している。現在のバージョンでは[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")のデュアルプロセッサまでと、[StrongARM](https://ja.wikipedia.org/wiki/StrongARM "wikilink")ファミリをサポートしている。

チューリッヒ工科大学の Native Systems Group では、Oberon をベースとした用途限定のOSである stailaOS を開発した\[11\]。これは、リアルタイム解析、高速商取引システム、主記憶のみで動作する[ERPシステムなどが用途とされている](https://ja.wikipedia.org/wiki/企業資源計画 "wikilink")。

### Native Oberon

**Native Oberon** は[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")ベースのPC上で動作するOberonである。ハードウェアに対する要求仕様が小さい（Pentium 133MHz、ハードディスクは100MB、表示は1024×768ピクセル、オプションで[スリーコム](https://ja.wikipedia.org/wiki/スリーコム "wikilink")製ネットワークカード）。フロッピーディスク1枚で基本システムを動作させることが可能で、追加のソフトウェアはネットワーク経由でインストールできる。Native Oberon もシステム全体がOberon言語で書かれている。

## Oberon プログラミング言語

[プログラミング言語](../Page/プログラミング言語.md "wikilink")の**Oberon**は、[Pascal](../Page/Pascal.md "wikilink")や[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")を生み出した[ニクラウス・ヴィルト](../Page/ニクラウス・ヴィルト.md "wikilink")が[チューリッヒ工科大学](../Page/チューリッヒ工科大学.md "wikilink")のチームと共に1986年に開発した。OSのOberonの開発の一環として開発されたもので、Modula-2をシステム実装言語として使用しようとしたとき安全な型拡張機能がないことから新たに設計された。当初から教育目的で言語処理系とOSの詳細を書籍の形で出版する計画だった。そのため新言語は必要な基本機能のみを備えた設計になった。

文法は[Modula-2](https://ja.wikipedia.org/wiki/Modula-2 "wikilink")によく似ているが、かなり小さくなっている\[12\]\[13\]。その単純さから、[コンパイラ](../Page/コンパイラ.md "wikilink")の生成するコードも小さく効率的である。言語仕様は[EBNF](../Page/EBNF.md "wikilink")1ページほどで記述できる。コンパイラも4000行ほどで記述されていた。Modula-2との大きな違いとして[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")を備えている。

Oberonと後継の[Oberon-2](https://ja.wikipedia.org/wiki/Oberon-2 "wikilink")は様々なOS上に移植されており、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")プラットフォーム上でも動作する。OberonのソースコードからJavaのソースコードを生成する方式とJava-VM向け[バイトコード](../Page/バイトコード.md "wikilink")を生成する方式がある。

### 設計目標

Oberon は安全性を指向した言語である。[配列](../Page/配列.md "wikilink")境界チェック、[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")、強い型チェックなどの機能がある。これらはロジックの[バグ](../Page/バグ.md "wikilink")を早期に発見することを目的としており、プログラム実行時に顕在するバグの数を劇的に減少させる。しかし、他の言語がバグ削減を目的として採用している機能が実装されていない（例えば、enum型、プログラマ指定の整数範囲型）。結果として数式的部分に関してはプログラマが注意しなければならない。

### 特徴

Oberon はコードの不透明性をなくし、機能を限定して機能の誤用を防ぐことでミスを減らそうとした。この考え方は [APL](../Page/APL.md "wikilink") と共通するものがあるが、Oberon は簡略化しすぎて可読性を損なうことがないよう意図して設計された。

成功かどうかを定量的に測るのは難しいが、Oberon が当初の目標を達成したかどうかについては異論もある。[Ada](../Page/Ada.md "wikilink") 設計者の1人 Jean Ichbiah は Oberon の簡略化の方針に異議を唱えた。これは、ヴィルトが Ada を「大きすぎる」と非難したことに応えたもので、彼は「ヴィルトは大きな問題への小さな解決策が存在すると考えている。私はそのような奇跡は信じない。大きな問題には大きな解決策しかない\!」と言った。Oberon の開発者たちは、そういう意味では Oberon は行き過ぎていたと考え、Oberon-2 では [FOR文の文法を差し戻した](https://ja.wikipedia.org/wiki/For文 "wikilink")（初期の Oberon には [WHILE文があれば十分と考え削除されていた](https://ja.wikipedia.org/wiki/While文 "wikilink")）。

機能を省くことでプログラマが「[車輪の再発明](../Page/車輪の再発明.md "wikilink")」のように機能を再実装しなければならなくなるという議論もある。[ライブラリ](../Page/ライブラリ.md "wikilink")はそのような問題を多少なりとも和らげる。[Java](https://ja.wikipedia.org/wiki/Java "wikilink")は（Oberonほどではないが）単純な言語と大きな標準ライブラリの実例である（なお、Oberon の標準ライブラリは Java のものより小さい）。ある言語を習得するということは、その言語の標準ライブラリについても学ぶことであり、Ichbiah の上述の反論は、機能を標準ライブラリに移動させることによる単純化戦略にも拡大して当てはめることができる。ヴィルトや Oberon のファンは、Oberon が基本的かつ効果的にこの問題を防いでいるとしている。

  - Pascal風だが、より一貫した文法
  - 強力な型チェックと型拡張
  - 型チェックインタフェース付きモジュールと分割コンパイル
  - 全数値型間での互換性（式内で混用可能）
  - 文字列操作
  - システムプログラミングをサポート

#### Visibility Flag

グローバル変数、型、定数、[プロシージャ](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")はデフォルトでは宣言しているモジュール内でのみ可視である。Visibility Flag をつけることで他のモジュールからも見えるようにできる。Visibility Flag とは例えばリードライト許可の場合アスタリスク(`*`)である。フラグをうっかり忘れた場合の安全を考慮してデフォルトが選ばれている。

ローカル変数、型、定数、プロシージャは常に宣言しているプロシージャ内でのみ可視である。

#### 参照渡しと値渡し

プロシージャの引数に関して2つのモードが可能である。値渡し（Call by value）では引数に式を使用でき、式を評価した結果の値がプロシージャに渡される。参照渡し（Call by reference）では変数を渡すことだけが許されるので、その変数の値はプロシージャ内で変更される可能性がある。参照渡しにする場合、プロシージャの定義で引数に VAR という予約語を付与する。

### 実装と派生

#### Oberon

OberonはOSとともにチューリッヒ工科大学などで公開されている。

#### Oberon-2

[1991年](../Page/1991年.md "wikilink")に一部改訂を行い、オブジェクト指向を取り入れFOR文を復活させたものが**[Oberon-2](https://ja.wikipedia.org/wiki/Oberon-2 "wikilink")**であり、現在最も一般的実装となっている。Native Oberon と呼ばれるOSを含めた実装はPC上で動作する。[.NET向けに若干の拡張を加えたバージョンもチューリッヒ工科大学で開発されている](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。

チューリッヒ工科大学が保守しているOberon-2コンパイラとしては、Windows版、Linux版、OS X 版がある。他にもや[AmigaOS](../Page/AmigaOS.md "wikilink")といった各種OSで動作するバージョンがある。

イギリスのマンチェスター大学の Stephen J Bevan は、[Lex](../Page/Lex.md "wikilink")と[Yacc](../Page/Yacc.md "wikilink")でヴィルトらの仕様に基づいたOberon-2の字句解析器と[構文解析器](../Page/構文解析器.md "wikilink")を作成した。最新バージョンは1.4である。

#### Oberon-07

ヴィルトが2007年に定義したのがOberon-07である。Oberon-2ではなく本来のOberonに基づいており、2011年に仕様が改訂されている。主な変更点は、数値型の明示的変換関数（FLOOR、FLTなど）を必ず使うようにした点、LOOP文とEXIT文を排除した点、WHILE文が拡張された点、RETURN文が関数の最後にのみ存在するようにした点、インポートされた変数や構造のある引数がリードオンリーとなった点、配列をCOPY文を使わずに代入できるようになった点などである\[14\]。

コンパイラの実装としては、32ビットWindows版 [Oberon-07M](http://www.exaprog.com/)\[15\]、32ビット[ARM版](https://ja.wikipedia.org/wiki/ARMアーキテクチャ "wikilink")、Cortex-M3マイクロコントローラ版、ヴィルトが設計したRISCプロセッサを Xilinx FPGA Spartan-3 ボードに実装したもので動作する版がある。

#### Active Oberon

はOberonの別の拡張版で、オブジェクト指向を取り入れ（オブジェクト単位のアクセス制限など）、[表明](https://ja.wikipedia.org/wiki/表明 "wikilink")、プリエンプティブな優先度付きスケジューリング、メソッドの文法の若干の変更などがなされている。オブジェクトはスレッドまたはプロセスとして機能させることもできる。対応するOSはA2またはBluebottleと呼ばれる。

#### 関連言語

Oberon系統の言語開発は継続している。Oberon-2をさらに発展させたのが [Component Pascal](https://ja.wikipedia.org/wiki/Component_Pascal "wikilink") で、チューリッヒ工科大学からスピンオフしたオベロン・マイクロシステムズや[クイーンズランド工科大学](https://ja.wikipedia.org/wiki/クイーンズランド工科大学 "wikilink")がサポートしている。他にも特定分野向けにOberonの精神を受け継いだ言語として、[Lagoonaや](https://ja.wikipedia.org/wiki/:en:Lagoona_\(programming_language\) "wikilink")[Obliqがある](https://ja.wikipedia.org/wiki/:en:Obliq "wikilink")。

チューリッヒ工科大学にて、.NET環境向けに Zonnon という新言語が開発されている。Oberonの特徴を引き継ぎつつ、Pascalから一部機能を復活させたものだが、文法は異なる。動的オブジェクト、演算子オーバーロード、例外処理などの機能が追加されている。.NET向けに [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink") のプラグインとして処理系を使用することができる。

Oberon-Vは[数値解析](https://ja.wikipedia.org/wiki/数値解析 "wikilink")向けにOberonを拡張した言語で、特に[ベクタープロセッサやパイプラインアーキテクチャの](../Page/ベクトル計算機.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")での利用を意図している。元々は[小セネカにちなみ](https://ja.wikipedia.org/wiki/ルキウス・アンナエウス・セネカ "wikilink") Seneca と呼ばれていた\[16\]。

## 脚注

## 外部リンク

### OS

  - [The ETH Oberon Homepage](http://www.oberon.ethz.ch/)
  - [Native Oberon Home Page at ETHZ](http://www.oberon.ethz.ch/archives/systemsarchive/native_new) (Archived page)
  - [Genealogy and History of The Oberon System](http://www.oberon.ethz.ch/archives/systemsarchive/sys_genealogy_new)
  - [Oberon Community Platform - Wiki & Forum](http://www.ocp.inf.ethz.ch/wiki/)
  - [BlueBottle/Aos/A2](http://bluebottle.ethz.ch) An evolution of Native Oberon with support for Multiprocessor systems with Active Objects (kind of threads running on separate processors, if available) and a [Zooming User Interface](https://ja.wikipedia.org/wiki/ズーミングユーザインタフェース "wikilink")
  - [Native Oberon Home Page](http://www.oberon.ethz.ch/archives/systemsarchive/native_new)
  - [Native Oberon Hardware Compatibility](http://www.oberon.ethz.ch/archives/systemsarchive/hw_new)
  - [Notes and bug repairs for ETH Native Oberon](http://carnot.yi.org/OberonPage.html)
  - [Lukas Mathis' Blog about Oberon](http://ignco.de/91) Oberonとユーザインタフェースの歴史

### 言語

  - [Niklaus Wirth's Oberon page at ETH-Zürich](http://www.inf.ethz.ch/personal/wirth/Articles/Oberon.html)
  - [Oberon Language Genealogy](http://www.oberon.ethz.ch/language/genealogy)
  - [Oberon Web Ring](http://v.webring.com/hub?ring=oberon)
  - [Oberon at SSW, Linz](http://www.ssw.uni-linz.ac.at/Research/Projects/Oberon.html)
  - [Linux Native Oberon related section](http://fruttenboel.verhoeven272.nl/Oberon/)
  - [Astrobe - ARM Oberon-07 Development System](http://www.astrobe.com/default.htm)
  - [Oberon System V4 for HP OpenVMS Alpha](http://modulaware.com/mwovms.htm) with source code upward-compatible 64 bit addressing
  - [64 bit Oberon-2 compiler for HP OpenVMS Alpha](http://modulaware.com/mwcvms.htm)

### 言語の変遷

  - "*[The Programming Language Oberon](http://www.inf.ethz.ch/personal/wirth/Articles/Oberon/Oberon.Report.pdf)*" Wirth, (1988/90)
  - "*[The Programming Language Oberon-2](http://www-vs.informatik.uni-ulm.de:81/projekte/Oberon-2.Report/)*" H. Mössenböck, N. Wirth, Institut für Computersysteme, ETH Zürich, January 1992
  - "*[What's New in Component Pascal](http://www.oberon.ch/pdf/CP-New.pdf)*" (Changes from Oberon-2 to CP), Pfister (2001)
  - "*[Differences between Oberon-07 and Oberon](http://www.inf.ethz.ch/personal/wirth/Articles/Oberon/Oberon07.pdf)"* Wirth (2007)
  - "*[The Programming Language Oberon-07 (Revised Oberon)](http://www.inf.ethz.ch/personal/wirth/Articles/Oberon/Oberon07.Report.pdf)*" Wirth, 2007/11 (Most current language report)

[be-x-old:Oberon](https://ja.wikipedia.org/wiki/be-x-old:Oberon "wikilink") [cs:Oberon (programovací jazyk)](https://ja.wikipedia.org/wiki/cs:Oberon_\(programovací_jazyk\) "wikilink") [da:Oberon (programmeringssprog)](https://ja.wikipedia.org/wiki/da:Oberon_\(programmeringssprog\) "wikilink") [de:Oberon (Programmiersprache)](https://ja.wikipedia.org/wiki/de:Oberon_\(Programmiersprache\) "wikilink") [es:Oberon (lenguaje de programación)](https://ja.wikipedia.org/wiki/es:Oberon_\(lenguaje_de_programación\) "wikilink") [fr:Oberon (langage)](https://ja.wikipedia.org/wiki/fr:Oberon_\(langage\) "wikilink") [it:Oberon (linguaggio)](https://ja.wikipedia.org/wiki/it:Oberon_\(linguaggio\) "wikilink") [he:אוברון (שפת תכנות)](https://ja.wikipedia.org/wiki/he:אוברון_\(שפת_תכנות\) "wikilink") [nl:Oberon (programmeertaal)](https://ja.wikipedia.org/wiki/nl:Oberon_\(programmeertaal\) "wikilink") [pl:Oberon (język programowania)](https://ja.wikipedia.org/wiki/pl:Oberon_\(język_programowania\) "wikilink") [pt:Oberon (linguagem de programação)](https://ja.wikipedia.org/wiki/pt:Oberon_\(linguagem_de_programação\) "wikilink") [tg:Оберон (забони барноманависӣ)](https://ja.wikipedia.org/wiki/tg:Оберон_\(забони_барноманависӣ\) "wikilink") [tr:Oberon (programlama dili)](https://ja.wikipedia.org/wiki/tr:Oberon_\(programlama_dili\) "wikilink") [zh:Oberon](https://ja.wikipedia.org/wiki/zh:Oberon "wikilink")

[Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:オブジェクト指向OS](https://ja.wikipedia.org/wiki/Category:オブジェクト指向OS "wikilink") [Category:1985年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1985年のソフトウェア "wikilink")

1.
2.  [M. Reiser and N. Wirth: Programming in Oberon](http://www-old.oberon.ethz.ch/WirthPubl/ProgInOberonWR.pdf) Addison-Wesley/ACM Press (1992) ISBN 0-201-56543-9
3.  [N. Wirth and J. Gutknecht: Project Oberon - The Design of an Operating System and Compiler](http://www-old.oberon.ethz.ch/WirthPubl/ProjectOberon.pdf) Addison-Wesley/ACM Press (1992) ISBN 0-201-54428-8. Out of print.[Electronic Reprint.](http://www.ethoberon.ethz.ch/WirthPubl/ProjectOberon.pdf)
4.  R. Gerike, Wider den Schnickschnack. Oberon System, Teil 1: Anwendersicht. *c't* 1994 (2) p. 180, Teil 2: Technische Einblicke. c't 1994 (3), p. 240 (German language).
5.  Oberon System 3, Dr. Dobb's Journal, October 1994, pages 42-50
6.  D. Pountain, Oberon: A Glimpse at the Future, *BYTE* 15(2), 385-392, Nov. 1990.
7.  D. Pountain, The Oberon/F System, *BYTE* 20(1), Jan. 1995.
8.  T. Börner, Betriebssysteme: Native Oberon für den PC, *CHIP* 1999, March, p. 131ff (German language).
9.
10. Reiser, Martin: "The Oberon System - User Guide and Programmer's Manual" - Out-of-print - Addison-Wesley/ACM Press (1991) ISBN 0-201-54422-9
11. [stailaOS(ETHZ) Project Page](http://nativesystems.inf.ethz.ch/Main/WebHomeResearchStaila)
12. Warren Keuffel, Whither Modula-2?, *Computer Language* 27-33, Dec. 1989
13. Dick Pountain, Modula's Children Part II: Oberon, *BYTE* 135-142, March 1991
14. 詳細については[The Programming Language Oberon-07](http://www.inf.ethz.ch/personal/wirth/Articles/Oberon/Oberon07.Report.pdf) を参照
15. [Oberon-07 language revision 2008](http://exaprog.com/Oberon07.Report.pdf)
16. "Seneca - A Language for Numerical Applications on Vectorcomputers", Proc CONPAR 90 - VAPP IV Conf. R. Griesemer, Diss Nr. 10277, ETH Zurich.