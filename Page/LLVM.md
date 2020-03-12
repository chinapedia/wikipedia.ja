> この記事は[LLVM](https://ja.wikipedia.org/wiki/LLVM)から翻訳されています。


**LLVM**とは、コンパイル時、[リンク時](../Page/リンケージエディタ.md "wikilink")、実行時などあらゆる時点でプログラムを最適化するよう設計された、任意の[プログラミング言語](../Page/プログラミング言語.md "wikilink")に対応可能な[コンパイラ](../Page/コンパイラ.md "wikilink")基盤である。当初は、LLVMの名称の由来は、Low Level Virtual Machine (低水準[仮想機械](../Page/仮想機械.md "wikilink")) の[略であるとしていたが](../Page/頭字語.md "wikilink")\[1\]、現在は、何の頭文字でもないとしている\[2\]。

## 概要

LLVMは、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")と[Java VMの関係のように](../Page/Java仮想マシン.md "wikilink")、まず[仮想機械](../Page/仮想機械.md "wikilink")をターゲットとした中間コード（ビットコード）を生成し、その仮想機械向けコードを特定のマシンの[機械語](../Page/機械語.md "wikilink")に変換する。この時言語や[プラットフォームとは独立した](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[最適化を行う](../Page/コンパイラ最適化.md "wikilink")。この方法によってLLVMは言語からもアーキテクチャからも独立しており、それぞれに特化した、プログラミング言語固有のモジュールと、マシン向け[コード生成](https://ja.wikipedia.org/wiki/コード生成 "wikilink")部を用意することにより様々な言語アーキテクチャーに対応する。LLVMは積極的にプロシージャ間最適化を行うとともに、静的コンパイラとしても[JITコンパイラとしても使え](../Page/実行時コンパイラ.md "wikilink")、開発の様々な段階で使える多数の部品を持っている（[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")と[CILフロントエンド](../Page/共通中間言語.md "wikilink")、[Python](../Page/Python.md "wikilink")フロントエンド、[グラフ彩色](https://ja.wikipedia.org/wiki/グラフ彩色 "wikilink")式の[レジスタ割り付け](../Page/レジスタ割り付け.md "wikilink")モジュール、など）。JITコンパイラの場合、実行時に不要な静的分岐を最適化する機能があり、これはプログラムが様々な実行時オプションを持っている場合、強力な最適化手法（[部分評価](../Page/部分評価.md "wikilink")）となる。このため、[Mac OS X v10.5ではこれを使ってハードウェア機能がない場合に](../Page/Mac_OS_X_v10.5.md "wikilink")[OpenGL](../Page/OpenGL.md "wikilink")パイプラインを実現している。

LLVM自体はC++で書かれており、[イリノイ大学](../Page/イリノイ大学.md "wikilink")で[2000年](../Page/2000年.md "wikilink")に開発が開始されたものである。ライセンス条件は[イリノイ大学/NCSAオープンソースライセンス](https://ja.wikipedia.org/wiki/イリノイ大学/NCSAオープンソースライセンス "wikilink")\[3\]であり、これは[BSDライセンス](../Page/BSDライセンス.md "wikilink")によく似た[OSI認証ライセンスである](../Page/Open_Source_Initiative.md "wikilink")。バージョン9.0.0からはライセンスがLLVM例外付き[Apache License 2.0に変更された](https://ja.wikipedia.org/wiki/Apache_License_2.0 "wikilink")\[4\]。

## ビットコード

LLVMは言語から独立した[命令セット](../Page/命令セット.md "wikilink")と[型システム](../Page/型システム.md "wikilink")を持つ。命令の多くは[3番地コード](https://ja.wikipedia.org/wiki/3番地コード "wikilink")形式に似ている。各命令はまた[静的単一代入](https://ja.wikipedia.org/wiki/静的単一代入 "wikilink")形でもあり、[変数](../Page/変数_\(プログラミング\).md "wikilink")（型付きレジスタ）は一回代入されるとその後は変更されない。このため、変数間の依存関係の解析が単純化される。

[型変換](../Page/型変換.md "wikilink")は、どういう形式であっても明示的に `cast` 命令を使って行われる。LLVMの持つ基本型はいくつかの固定長の整数型であり、[派生型](../Page/派生型.md "wikilink")として[ポインタ](../Page/ポインタ_\(プログラミング\).md "wikilink")、[配列](../Page/配列.md "wikilink")（任意のデータ型を格納可能な配列）、ベクトル（[整数](../Page/整数.md "wikilink")、[浮動小数](https://ja.wikipedia.org/wiki/浮動小数 "wikilink")、ポインタのみ格納可能な配列）、[構造体](../Page/構造体.md "wikilink")、[関数の](../Page/サブルーチン.md "wikilink")5つがある。具体的な言語で構築される型は、LLVM上ではこれらの型を組み合わせて表現される。例えば、C++における[クラスは](../Page/クラス_\(コンピュータ\).md "wikilink")、構造体と関数と[関数へのポインタ](../Page/関数へのポインタ.md "wikilink")の配列を組み合わせて表現される。

## フロントエンド

### dragonegg

LLVMは、もともと既存の[GCCスタック用のものより積極的な最適化を行う高性能のシステムとして開発され](../Page/GNUコンパイラコレクション.md "wikilink")、GCCフロントエンドがLLVMと動作するように修正された。現在では、GCC 4.6から派生した[フロントエンド](../Page/フロントエンド.md "wikilink")（dragonegg）を用いて[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[FORTRAN](../Page/FORTRAN.md "wikilink")、[Ada](../Page/Ada.md "wikilink")をサポートし、[Objective-C](../Page/Objective-C.md "wikilink")、Objective-C++、[Goがおおむね動くとしている](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")。

### Clang

しかし、LLVMへの興味が広がるにつれ、まったく新しいフロントエンドを多数のプログラミング言語向けに開発しようという動きが出てきた。もっとも注目されているのはC、C++、Objective-C、Objective-C++をサポートする新しいコンパイラ[Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")である。主にアップルのサポートを受け、ClangはGCCシステムのC/C++/Objective-C/Objective-C++コンパイラを[統合開発環境](../Page/統合開発環境.md "wikilink")と統合でき[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")をサポートした現代的なシステムで置き換えることを目指している\[5\]。GCCでのObjective-C/Objective-C++の開発は衰退気味で、アップルが施した変更は別個にメンテナンスされている。アップルにとっては、自社でコンパイラを開発することにより、第一のObjective-C/Objective-C++実装であり続けながら、LLVMがすでに達成している統合開発環境への統合やその他の現代的な機能への対応といった問題を解決することができる。

## 標準C++ライブラリ

GNUは[libstdc++](https://ja.wikipedia.org/wiki/libstdc++ "wikilink")という[標準C++ライブラリ](../Page/標準C++ライブラリ.md "wikilink")を開発しているが、LLVMも独自の[libc++](https://ja.wikipedia.org/wiki/libc++ "wikilink")という標準C++ライブラリを開発している。

## 参照

## 関連項目

  - [Clang](https://ja.wikipedia.org/wiki/Clang "wikilink")
  - [C--](https://ja.wikipedia.org/wiki/C-- "wikilink")

## 外部リンク

  -
  - [LLVM: A Compilation Framework for Lifelong Program Analysis & Transformation](http://llvm.org/pubs/2004-01-30-CGO-LLVM.pdf) — by Chris Lattner and Vikram Adve.

  - [LLVM Language Reference Manual](http://llvm.org/docs/LangRef.html) — LLVMの[中間表現](../Page/中間表現.md "wikilink")の解説

  - [LLVM/GCC Integration Proposal](http://gcc.gnu.org/ml/gcc/2005-11/msg00888.html) — LLVMをGCCに導入することについての議論

[Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:C言語](https://ja.wikipedia.org/wiki/Category:C言語 "wikilink") [Category:C++](https://ja.wikipedia.org/wiki/Category:C++ "wikilink") [Category:仮想機械](https://ja.wikipedia.org/wiki/Category:仮想機械 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.  [The University of Illinois/NCSA Open Source License (NCSA) - Open Source Initiative](http://www.opensource.org/licenses/UoI-NCSA.php)
4.
5.  [New LLVM C Front-end (Steve Naroff)](http://llvm.org/devmtg/2007-05/09-Naroff-CFE.pdf)