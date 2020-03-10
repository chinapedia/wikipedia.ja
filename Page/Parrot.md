> この記事は[Parrot](https://ja.wikipedia.org/wiki/Parrot)から翻訳されています。


**Parrot** は[レジスタベースの](../Page/レジスタマシン.md "wikilink")[仮想機械](../Page/仮想機械.md "wikilink")（仮想マシン）で、[動的プログラミング言語](../Page/動的プログラミング言語.md "wikilink")を効率的に動作させるために開発された、[C言語](../Page/C言語.md "wikilink")で書かれたソフトウェアである。Parrotは他の多くの仮想マシンと異なり、[型情報を扱うことができる](https://ja.wikipedia.org/wiki/データ型 "wikilink")。[Parrot アセンブリ言語と](https://ja.wikipedia.org/wiki/:en:Parrot_assembly_language "wikilink")[PIR](https://ja.wikipedia.org/wiki/:en:Parrot_intermediate_representation "wikilink")（Parrot[中間言語](../Page/中間言語.md "wikilink")）をParrotの[バイトコード](../Page/バイトコード.md "wikilink")に変換し、実行することができる。

Parrotプロジェクトは[Perl](../Page/Perl.md "wikilink")のコミュニティにより開始され、Parrotは[オープンソース](../Page/オープンソース.md "wikilink")と[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")のコミュニティの協力により開発されている。結果として、Parrotは[ライセンス](../Page/ライセンス.md "wikilink")の互換性 ([Artistic License 2.0](https://ja.wikipedia.org/wiki/Artistic_License "wikilink"))、非常に広い範囲の[プラットフォーム](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")、現代的なほとんどの[プロセッサ](../Page/プロセッサ.md "wikilink")[アーキテクチャに対する互換性](../Page/コンピュータ・アーキテクチャ.md "wikilink")、実行速度、サイズ（プラットフォームによるが 700K 程度）、Perlおよび全てではないがほとんどの現代的な[動的プログラミング言語](../Page/動的プログラミング言語.md "wikilink")の様々な要求に対して柔軟に対応できること、に焦点を置いている。また、[イントロスペクション](https://ja.wikipedia.org/wiki/リフレクション_\(情報工学\) "wikilink")、[デバッガ](../Page/デバッガ.md "wikilink")の機能、コンパイル時のセマンティックの調節 (semantic modulation) にも焦点を置いている。

## 歴史

プロジェクトは[Raku](https://ja.wikipedia.org/wiki/Raku "wikilink")を実装するために始まり、非常に長い時間、「Raku を動作させるために開発中のソフトウェア」であった。*Parrot*という名前は、「新しい想像上の言語 *Parrot* が[Python](../Page/Python.md "wikilink")と[Perl](../Page/Perl.md "wikilink")を統一するとアナウンスされた」という、[エイプリルフール](https://ja.wikipedia.org/wiki/エイプリルフール "wikilink")のジョークに由来している[1](http://www.oreilly.com/news/parrotstory_0401.html)。後に、PerlとPythonをサポートすることが目的で、プロジェクトはこの名前を採用した。

Parrot仮想マシンで動作するよう、複数の言語がParrotとともに開発されている。

[2009年](../Page/2009年.md "wikilink")[3月17日](../Page/3月17日.md "wikilink")にバージョン1.0がリリースされた。"Haru Tatsu" という[コードネーム](../Page/コードネーム.md "wikilink")がついている。

過去のバージョンのリリースの日付は、Parrot のウェブサイト\[[http://www.parrotcode.org/docs/parrothist.html\]に記載されている](http://www.parrotcode.org/docs/parrothist.html%5Dに記載されている)。

## 対応言語

Parrot仮想マシンの目標は[クライアントの言語をホストし](../Page/クライアント_\(コンピュータ\).md "wikilink")、それらの相互運用を可能にすることである。目標を実現するには多数のハードルが存在する。

### 静的な言語と動的な言語

[静的な型付けと動的な型付け言語の異なる性質がParrotの開発の動機となっている](https://ja.wikipedia.org/wiki/型システム#静的型付けと動的型付け "wikilink")。 現在の[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")や[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink") (CLR) などの人気のある仮想マシンは、静的に型付けされた言語のために開発されているが、Parrotが対象としている言語は動的な型付けのものである。

また、Java仮想マシンや現行のPerl 5 仮想マシンは[スタックマシン](https://ja.wikipedia.org/wiki/スタックマシン "wikilink")である。Parrotの開発者達は、Parrotがレジスタを備えているため実際の[ハードウェア](../Page/ハードウェア.md "wikilink")の設計に近く、バイトコードを[機械語](../Page/機械語.md "wikilink")に近い速度で動作させるためにこれまでの膨大な[コンパイラ最適化](../Page/コンパイラ最適化.md "wikilink")の学術的な資産をParrot仮想マシン用のコード生成に利用できる利点があると考えている。

### 関数言語的な概念

Parrotは、[クロージャ](https://ja.wikipedia.org/wiki/クロージャ "wikilink")や[継続](https://ja.wikipedia.org/wiki/継続 "wikilink")などの、いずれも[例外処理](../Page/例外処理.md "wikilink")や[マルチスレッドと組み合わせた場合には](../Page/スレッド_\(コンピュータ\).md "wikilink")、正しくかつ移植性を保って実現するのが特に難しいような[関数型プログラミングの機能を数多くサポートしている](../Page/関数型言語.md "wikilink")。こうした問題を仮想マシンのレベルで解決することにより、Parrotのクライアント言語で実現する労力を著しく軽減することができる。

### コンパイラツール

Parrotは[コンパイラ作成ツールセットを提供している](https://ja.wikipedia.org/wiki/:en:Parrot_compiler_toolchain "wikilink")。[再帰下降構文解析](../Page/再帰下降構文解析.md "wikilink")や[演算子順位パーサーを表現できる](https://ja.wikipedia.org/wiki/:en:operator-precedence_parser "wikilink")[ハイブリッド](https://ja.wikipedia.org/wiki/ハイブリッド "wikilink")の[Parser Grammar Engine](https://ja.wikipedia.org/wiki/:en:Parser_Grammar_Engine "wikilink") (PGE) を備えており、この2つを同じ文法で自由に遷移できる。

PGEは[Tree Grammar Engine](https://ja.wikipedia.org/wiki/Tree_Grammar_Engine "wikilink") (TGE) に解析結果を与え、TGE は最適化のため、究極的にはコード生成のために、PGE が作成した解析構文木を変換する。

### クライアントの言語

予定されている[Raku](https://ja.wikipedia.org/wiki/Raku "wikilink")のサブセットに加えて、多数のプログラム言語が[Parrot assembly languageにコンパイルできるようにすることが次々に計画されている](https://ja.wikipedia.org/wiki/:en:Parrot_assembly_language "wikilink")。 [APL](../Page/APL.md "wikilink")、[BASIC](../Page/BASIC.md "wikilink")、[Befunge](../Page/Befunge.md "wikilink")、[Brainfuck](../Page/Brainfuck.md "wikilink")、[Cola](https://ja.wikipedia.org/wiki/:en:Cola_programming_language "wikilink")、[Forth](../Page/Forth.md "wikilink")、[Jako](https://ja.wikipedia.org/wiki/:en:Jako_\(programming\) "wikilink")、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[m4](../Page/M4_\(プログラミング言語\).md "wikilink")、[Miniperl](https://ja.wikipedia.org/wiki/Miniperl "wikilink")、[Parakeet](https://ja.wikipedia.org/wiki/:en:Parakeet_programming_language "wikilink")、[OpenComal](https://ja.wikipedia.org/wiki/:en:OpenComal "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Plot](https://ja.wikipedia.org/wiki/Plot_programming_language "wikilink")、Pheme、[Punie](https://ja.wikipedia.org/wiki/:en:Punie "wikilink")、 [Python](../Page/Python.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Scheme](../Page/Scheme.md "wikilink")、[Span](https://ja.wikipedia.org/wiki/:en:Span_programming_language "wikilink")、[Tcl](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink")（別名partcl）、[URM](https://ja.wikipedia.org/wiki/URM_programming_language "wikilink")、[YAL](https://ja.wikipedia.org/wiki/:en:YAL "wikilink")、[Zork](../Page/ゾーク.md "wikilink") [Z-codeなどである](https://ja.wikipedia.org/wiki/Z-machine "wikilink")。しかし、これらの言語の実装のほとんどは、まだ不完全であったり、実験的であったり、さらに放棄されてしまったりしている。

### 将来可能性のある言語やプロジェクト

Rubyコミュニティの一部にParrotに対する強い興味がある。すでにPythonからマシンコードへの[JITコンパイラ](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")[Psyco](https://ja.wikipedia.org/wiki/Psyco "wikilink")や、Python からバイドコードへのコンパイラ[Jython](https://ja.wikipedia.org/wiki/Jython "wikilink")、[.NETプラットフォームへのコンパイラ](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") [IronPython](https://ja.wikipedia.org/wiki/IronPython "wikilink")、現在開発中の高レベルの最適化や静的なコード生成を目的とした[PyPy](https://ja.wikipedia.org/wiki/PyPy "wikilink")などがあるため、Pythonコミュニティは見守る様子を見せている。

## Parrot の内部

### バイトコード

Parrot のコードには3つの形態がある。[バイトコード](../Page/バイトコード.md "wikilink")(**Parrot Bytecode**, **PBC**)はネイティブでParrotに解釈される[機械語](../Page/機械語.md "wikilink")であり、ほかの2つのコードは**IMCC**(旧バージョン)または**PIRC**(新バージョン)によってバイトコードにコンパイルされる[中間言語](../Page/中間言語.md "wikilink")である。

[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")(**[Parrot Assembly Language](https://ja.wikipedia.org/wiki/:en:Parrot_Assembly_Language "wikilink")**, **PASM**) は、バイトコードにほぼ1対1で対応する低レベルの言語である。

**[Parrot intermediate representation](https://ja.wikipedia.org/wiki/:en:Parrot_intermediate_representation "wikilink")** (**PIR**) はPASMより若干高レベルの言語であるが、直接バイトコードにコンパイルすることができる。Parrot上で動作させる言語処理系は、普通はPASMより扱いやすいPIRへのコンパイラを実装する。

PIRを使うと、Parrotのルーチン間の[呼び出し規約](https://ja.wikipedia.org/wiki/呼び出し規約 "wikilink")の違いを管理・吸収し、またより実効効率のよい命令への変換([命令選択](https://ja.wikipedia.org/wiki/命令選択 "wikilink"), [instruction selection](https://ja.wikipedia.org/wiki/:en:instruction_selection "wikilink"))\[1\]や、変数の[レジスタ割り付け](../Page/レジスタ割り付け.md "wikilink")やメモリ退避（レジスタスピル) などの最適化を個別に実装することなくParrot (IMCCやPIRC) に任せることができる。

### ネイティブコードへの変換

もともとは独自のJITコンパイラを開発していたが、2009年のバージョン1.7.0で放棄された。将来的には、[LLVM](../Page/LLVM.md "wikilink")や[nanojit](https://ja.wikipedia.org/wiki/nanojit "wikilink")などの既存のJITライブラリを利用して新しいコンパイラを用意するとしている。\[2\]

### PMC

**Polymorphic Container**(**PMC**, 以前はParrot Magic Cookieの略とされていた)は、クライアント言語が扱う型を拡張するための仕組みである。

## 例

### レジスタ

Parrotは大半のハードウェアの[CPU](../Page/CPU.md "wikilink")と同様レジスタベースであり、大半の仮想マシンがスタックマシンであるのとは異なる。Parrotは4種類のレジスタを提供する。

  - I: ネイティブの[整数](../Page/整数.md "wikilink")型
  - N: [浮動小数点数](../Page/浮動小数点数.md "wikilink")
  - S: [Unicode](../Page/Unicode.md "wikilink")をサポートする先進的な[文字列](https://ja.wikipedia.org/wiki/文字列 "wikilink")レジスタ
  - P: Parrotのオブジェクト型であるPMC（あるいは *Parrot Magic Cookie*）

Parrot は任意の数のレジスタを提供する。レジスタの数は、コンパイル時に[サブルーチン](https://ja.wikipedia.org/wiki/サブルーチン "wikilink")ごとに決定される。

### 数値演算

PASMコード

`   set I1, 4`
`   inc I1        # I1 は 5`
`   add I1, 2     # I1 は 7`
`   set N1, 42.0`
`   dec N1        # N1 は 41.0`
`   sub N1, 2.0   # N1 は 39.0`
`   print I1`
`   print ', '`
`   print N1`
`   print "\n"`
`   end`

PIR コード

`.sub 'main' :main`
`   $I1 = 4`
`   inc $I1     # $I1 は 5`
`   $I1 += 2    # $I1 は 7`
`   $N1 = 42.0`
`   dec $N1     # $N1 は 41.0`
`   $N1 -= 2.0  # $N1 は 39.0`
`   print $I1`
`   print ', '`
`   print $N1`
`   print "\n"`
`.end`

## Parrot の文化

Parrot の[キャッチフレーズは](../Page/キャッチコピー.md "wikilink")「1つのバイトコードは全てを統べる」である。これは[J・R・R・トールキン](https://ja.wikipedia.org/wiki/J・R・R・トールキン "wikilink")の『[ホビットの冒険](../Page/ホビットの冒険.md "wikilink")』『[指輪物語](../Page/指輪物語.md "wikilink")』のキーアイテム「[一つの指輪](../Page/一つの指輪.md "wikilink")」に刻まれた銘に由来する。

[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")後半まで、Dan SugalskiがParrotの設計者のリードでありチーフアーキテクトであった。

長年のPerl、[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")、[C++](../Page/C++.md "wikilink")のハッカーであるが[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")半ば開発者のリードとなったときにこれを引き継いだ。の先導開発者（リード・デヴェロッパー）であり、Parrotのコンパイラツールのチーフアーキテクトでもある[アリソン・ランダル](https://ja.wikipedia.org/wiki/アリソン・ランダル "wikilink")が現在のチーフアーキテクトである。

開発に関する議論は主に[IRC上で行われており](https://ja.wikipedia.org/wiki/インターネット・リレー・チャット "wikilink")、普段はirc.perl.orgの\#parrotチャンネルが使われる。また、\#parrotsketchチャンネルで毎週Parrotおよび言語開発者のためのミーティングが開かれている。加えて、parrot.orgでホストされているparrot-dev[メーリングリスト](../Page/メーリングリスト.md "wikilink")上でも更なる議論がなされている。

Parrotの設計上の議論はParrotのリポジトリ\[[http://www.parrotcode.org/docs/pdd/\]に](http://www.parrotcode.org/docs/pdd/%5Dに) Parrot設計文書、PDDの形で存在している。チーフアーキテクトや指名された設計者が、ある機能についての考えや、[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink")、設計メモを説明するためにこれらのドキュメントを記述している。Parrotハッカーは、これらの文書を実行可能なテストに変換し、次に実在する機能に変えて行く。

Parrotの安定版は毎月第3火曜日にリリースされる。リリース作業は中心的な開発者が交代で担当し、同じ開発者が連続してリリース担当になることがないよう配慮されている。この慣習はプロジェクトの進行速度と安定性を高めるのに一役買っている。

## ライセンス

Parrot は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")プロジェクトであり、[Artistic License](https://ja.wikipedia.org/wiki/Artistic_License "wikilink") Version 2.0 の元配布されている。

## 脚注

## 関連項目

  - [共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink")
  - [Java仮想マシン](../Page/Java仮想マシン.md "wikilink")
  - [mod_parrot](https://ja.wikipedia.org/wiki/:en:mod_parrot "wikilink")

## 外部リンク

  - [Parrot homepage](http://www.parrot.org/)
  - [Perl 6 and Parrot links](http://perl6.cz/wiki/Perl_6_and_Parrot_links)

[Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink") [Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.