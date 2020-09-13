> この記事は[GNUコンパイラコレクション](https://ja.wikipedia.org/wiki/GNUコンパイラコレクション)から翻訳されています。


**GNU Compiler Collection**（グニューコンパイラコレクション）は、[GNU](../Page/GNU.md "wikilink")の[コンパイラ](../Page/コンパイラ.md "wikilink")群である。略称は「**GCC**（ジーシーシー）」。[GNUツールチェーン](https://ja.wikipedia.org/wiki/GNUツールチェーン "wikilink")の中核コンポーネント。

## 概説

最新標準パッケージには [C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Objective-C](../Page/Objective-C.md "wikilink")、[Objective-C++](https://ja.wikipedia.org/wiki/Objective-C++ "wikilink")、[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")、[Ada](../Page/Ada.md "wikilink")、[Go](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")、[Dのコンパイラ並びにこれらの](../Page/D言語.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")が含まれている。\[1\] バージョン7以前では、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")もサポートされていた。\[2\]

当初はCコンパイラとして開発し、GCCは **GNU C Compiler** を意味していた。しかし、もともと[多言語](../Page/多言語.md "wikilink")を想定して設計しており、 GNU C Compiler と呼ばれていたときでも多くの言語に対応していた。現在でも GNU C Compiler の意味で「GCC」と呼ぶことも多い。ちなみに GNU C Compiler の実行ファイルの名称も**`gcc`**である。なお、GNU C++コンパイラを**G++**、GNU Javaコンパイラを**[GCJ](../Page/GNU_Compiler_for_Java.md "wikilink")**、GNU Adaコンパイラを**[GNAT](https://ja.wikipedia.org/wiki/GNAT "wikilink")**と呼ぶ。

CコンパイラとしてのGCCは、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")規格 (ANSI X3.159-1989) にほぼ適合するC言語コンパイラ処理系であった。登場当初の時点では、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) 標準に付属するCコンパイラがANSI規格に適合していない部分が多いものがあった。そのため、GCCはANSI規格を広める役割を果たした。GCC自身は[K\&Rの範囲内のC言語で記述していたので](https://ja.wikipedia.org/wiki/C言語#K&R "wikilink")、OS付属のコンパイラでコンパイルできた。ただし、GNU拡張という独自の仕様もあり、GCCでコンパイルできるものがANSI適合コンパイラでコンパイルできるとは限らない。

## 歴史

1985年、当時[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink") (MIT) の研究者であった[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")によって、既成のコンパイラを拡張する形で開発が始められた。当初コンパイラはという[Pascal](../Page/Pascal.md "wikilink")の方言によって書かれていた。その後ストールマンとLeonard H. Tower, Jr.によってC言語で書き直され、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一つとして1987年に公開された。さらに2012年にはLawrence CrowlとDiego NovilloによってC++で書き直された。

### EGCS

[EGCS](https://ja.wikipedia.org/wiki/EGCS "wikilink") (エッグズ\[3\]、Experimental/Enhanced GNU Compiler System) は、1997年に当時開発中のGCC 2.8をベースとしてCygnus社の[EGCS Steering Committee](https://ja.wikipedia.org/wiki/EGCS_Steering_Committee "wikilink")（後のGCC Steering Committee）により開発された拡張版GCCである。1999年4月、GCCと再統合されてEGCSがGCCの公式バージョンとなり、GCCの開発主力はGCC Steering Committeeに委ねられた。また、この時点でGCCはGNU Compiler Collectionの意味となった\[4\]。統合後初めてリリースされたバージョンは、1999年7月のGCC 2.95である。

## 構成

GCCは通常のコンパイラと同様に[フロントエンド](../Page/フロントエンド.md "wikilink")部、最適化部、[バックエンド](https://ja.wikipedia.org/wiki/バックエンド "wikilink")部から構成される。

フロントエンド部は[字句解析](../Page/字句解析.md "wikilink")、[構文解析](../Page/構文解析.md "wikilink")などを行い、対応言語ごとに用意されている。たとえばC++フロントエンド、Javaフロントエンドなどがある。

バックエンド部の[コード生成](https://ja.wikipedia.org/wiki/コード生成 "wikilink")部（コードジェネレータ）、および[最適化部](../Page/コンパイラ最適化.md "wikilink")（オプティマイザ）は全言語で共通である。したがってGCCの対応の言語同士の間では、生成コードの質や対応するCPUの種類は原理的に同じになる。なお、フロントエンドおよびバックエンドの間でやりとりされる中間形式としてRTL () が使用される。

CコンパイラとしてのGCCの開発のために開発された構文解析部生成系[bison](https://ja.wikipedia.org/wiki/bison "wikilink")やフリーな字句解析部生成系[flexといったプログラムを使用してGNU](../Page/Lex.md "wikilink") Cコンパイラその他の各種フロントエンドは構築されている。これらは単独のフリーソフトウェアとしても有用なものである。

GCCはバージョン4から中間形式が2つ追加された。まず、各言語は通常フロントエンド言語の[木構造を保持した共通中間形式の](../Page/木構造_\(データ構造\).md "wikilink")[GENERIC](https://ja.wikipedia.org/wiki/GENERIC "wikilink")に変換されその後[GIMPLE](https://ja.wikipedia.org/wiki/GIMPLE "wikilink")という中間形式で木の最適化[SSAをおこなってからRTLの最適化がおこなわれる](https://ja.wikipedia.org/wiki/静的単一代入 "wikilink")。また、CやC++のコンパイル時にフロントエンドの構文解析、字句解析においてbisonやflexを使用しなくなった。

## 影響と評価

### 貢献

GCCはそれ自身が有用な[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")だが、OSや[DOSエクステンダ](../Page/DOSエクステンダ.md "wikilink")（[DJGPP](https://ja.wikipedia.org/wiki/DJGPP "wikilink")、[EMX](https://ja.wikipedia.org/wiki/EMX "wikilink")など）を構築するための基盤ツールとしても非常に有用であり、商用・非商用を問わず多くの環境で標準的なCコンパイラとして採用されている。特に[Linux](../Page/Linux.md "wikilink")や[FreeBSD](../Page/FreeBSD.md "wikilink")など、フリーソフトウェアとしてのOSは、もしGCCが存在しなかったならば大きく違ったものになっていたであろうと言われている。実際Linuxの生みの親である[リーナス・トーバルズ](../Page/リーナス・トーバルズ.md "wikilink")はGCCをGNUプロジェクトの中で最も重要なものとして挙げている\[5\]。

また、多くの[組み込みOS](../Page/組み込みオペレーティングシステム.md "wikilink") や、ゲームの開発環境でもGCCを採用している場合も多い。これは、クロス開発を容易なものとするGCCの広範なプロセッサへの対応が評価されていることによる。

その一方で、現状では生成コードの最適化において、特定のプロセッサへの最適化を図る商用コンパイラに水をあけられているのが実情である。特に科学技術演算で多用されるベクトル演算機構への対応や、特定のベンチマークなどでは顕著であった。これは多様な環境に対応することを第一とし、個別のプロセッサ向けの最適化を追求してこなかったことも大きな要因であったが、最近ではこれを改善するための試みも始められている。（最適化を参照）

### 批判

## GNU Cコンパイラ拡張

GNU C コンパイラの特徴のひとつは、前述のようにANSIあるいはISO等の標準への準拠である。もうひとつの特徴は独自の拡張機能である。このような拡張を「GCC拡張機能」とよぶ。GCC拡張機能は数多いが、多引数[マクロ](../Page/マクロ_\(コンピュータ用語\).md "wikilink")、基本型としての[複素数](../Page/複素数.md "wikilink")型、式の演算結果としての左辺値、初期化式の拡張、Cでのインライン関数定義、[ネストした関数定義](../Page/ネスティング.md "wikilink")、ラベルに対する&[演算子](../Page/演算子.md "wikilink")の適用などがある。

このような拡張は、[C99](../Page/C99.md "wikilink")における標準Cの拡張として逆に取り込まれたものも多い。

言語機能の拡張のほかに、標準外機能としてasm文による[インラインアセンブラ](https://ja.wikipedia.org/wiki/インラインアセンブラ "wikilink")の機能はユニークである。ただし、GCCにおいてはこのインラインアセンブラ機能を利用して記述したコードに対しても最適化が行われる（プログラマが意図して[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")を用いて書いたとしても、その通りのコードが出力されない可能性がある）点に注意が必要である。

その他、研究論文の発表における実装例のベースとして、あるいは実験的機能実装のベースとしてGCC (G++)が使われることも多い。そのような拡張の最近の例としては、[スタックバッファオーバーフローに関する脆弱性の回避のためのGCC拡張ProPoliceなどがある](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")。[1](http://www.trl.ibm.com/projects/security/ssp/)

## 最適化

GCCは高度な最適化を行うが、CPUベンダやRISCワークステーションメーカが提供するコンパイラと比べると見劣りする場合もある。マルチアーキテクチャゆえに、機種依存しない最適化が中心となるため、特定の CPU に特化した専用コンパイラと比べてやや不利な立場といえる。

2005年4月にリリースされたGCC4.0は[ループ最適化の改善や自動](../Page/ループ_\(プログラミング\).md "wikilink")[ベクトル化](../Page/ベクトル化.md "wikilink")など最適化機構が大幅に見直されている反面、GCC3.x で書かれたコードがコンパイルエラーになることがあり、[互換性](../Page/互換性.md "wikilink")において若干の問題点がある。GCC4.2ではバグ修正、最適化の改善に加え、新機能として[C](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Fortran](https://ja.wikipedia.org/wiki/Fortran "wikilink")で[OpenMP](../Page/OpenMP.md "wikilink")に対応し、さらにGCC4.3ではループの自動[並列化](../Page/並列化.md "wikilink")による[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")処理が可能となるなど、マルチプロセッサ環境では大幅にアプリケーションの性能を引き上げることが可能になった。ただし、マルチスレッドやベクトルプロセッサを使用しないことを前提としたシングルスレッドアプリケーションにおける最適化においては3.x系よりも一部のプログラムにおいて劣る場合もある。

[PGCC](https://ja.wikipedia.org/wiki/PGCC "wikilink")は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink") [Pentium](https://ja.wikipedia.org/wiki/Pentium "wikilink")専用の最適化を行うGCCの派生であり、通常版と比べてPentium CPU上でより効率良く動作するコードを生成する。

登場当初は、特にMC680x0系に対して商用コンパイラを凌駕する最適化品質を誇っていたとされる。ただし、これは同時代の68k系商用コンパイラとの相対的な比較・評価であり、絶対的な指標によるものではない。単に、当時の68k系用商用コンパイラに生成コードの最適化でgccよりも優れた製品がなかっただけである。gccは、他のプロセッサ環境においてもその生成コードの品質ではなく、移植性の高さ、クロスプラットフォーム開発における作業の手間を省くことに注力している。68kプロセッサを特別優遇しているわけではない。

## サポートするアーキテクチャ

## 脚注

## 関連項目

## 外部リンク

  -

  - [本の虫: OpenBSDのコンパイラー](https://cpplover.blogspot.com/2013/08/openbsd.html) GCC 2.5からEGCSまでの記載もある

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:1987年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1987年のソフトウェア "wikilink")

1.
2.
3.  <https://gcc.gnu.org/news/announcement.html>
4.  <https://gcc.gnu.org/wiki/History>
5.  Linuxの強味 <https://www.oreilly.co.jp/BOOK/osp/OpenSource_Web_Version/chapter08/chapter08.html>