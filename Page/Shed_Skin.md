> この記事は[Shed Skin](https://ja.wikipedia.org/wiki/Shed_Skin)から翻訳されています。


**Shed Skin** は、暗黙的に[静的に型付けされた](https://ja.wikipedia.org/wiki/型システム "wikilink")[Python](../Page/Python.md "wikilink")プログラムを最適化された[C++](../Page/C++.md "wikilink")プログラムに変換する実験的な[コンパイラ](../Page/コンパイラ.md "wikilink")である。型についての制約条件を満たすため、プログラムは多くの場合変更する必要があるが、変更した後でも、Python プログラムとしての正しさは保つことができる。Shed Skin は現在のところ Python の標準ライブラリをそれほど使用していない小さなプログラムに限定されている。現在までに変換できた最大のプログラムは 1,600 行である。

Shed Skin では、[変数は単一の型のみ持つことができる](https://ja.wikipedia.org/wiki/変数_\(プログラミング\) "wikilink")。すなわち、たとえば `a=1; a='1'` といったコードは許容されない。単一の型であれば、[抽象型](https://ja.wikipedia.org/wiki/抽象型 "wikilink")や汎用型 (C++におけるテンプレート)でよく、クラス A とクラス B が共通の基底クラスをもてば `a=A(); a=B()` というコードは許容される。

ShedSkin の開発者によって作成されたテストケースでは、Shed Skin は [Psyco](https://ja.wikipedia.org/wiki/Psyco "wikilink") の `psyco.full()` による方法を使って最適化した同一のコードに対して 2-40 倍高速に動作する。しかし、ShedSkin はコンパイル可能ないくつかのプログラムで、[CPython](https://ja.wikipedia.org/wiki/CPython "wikilink") よりも著しく低速に動作する(たとえば、CPython でよく最適化されている *set* や *str* 型に大きく依存したプログラム)。\[1\].

Shed Skin によって生成されたコードは Python のランタイムにまったく依存しておらず、ハードウェアの制約がある組み込みシステムでも利用可能である。また Shed Skin は[コードの難読化に用いることもできる](https://ja.wikipedia.org/wiki/難読化コード "wikilink")。C++ コンパイラで生成した機械語はPython の[バイトコード](../Page/バイトコード.md "wikilink")よりリバースエンジニアリングが難しいためである。

C++ の型宣言(たとえば`int`など)を生成するための型を推測するため、Shed Skin は型推論の技法を用いている。Shed Skin の型推論は Ole Agesen の Cartesian Product Algorithm と John Plevyak の Iterative Class Splitting の技法を組み合わせて用いている。こうした技法はプログラムサイズの増加に対して、これまでのテストで見られた以上に対応することはできない可能性がある。

Shed Skin は Python の一部の機能のみをサポートした組み込みライブラリの C++ 実装を除くと 6,500 行のコードで記述されている。 Shed Skin は [Pyrex](https://ja.wikipedia.org/wiki/Pyrex "wikilink"), [Boo](https://ja.wikipedia.org/wiki/:en:Boo_\(programming_language\) "wikilink"), [RPython](https://ja.wikipedia.org/wiki/PyPy "wikilink") などのプロジェクトに類似した試みである。

## Shed Skin の制限

  - プログラムは Python の標準ライブラリを自由に使うことができない。一部の共通のインポートは可能である(lib/\*.py を参照)
  - 現在のところ、型の解析は数百行以上のコードではうまく動作しない。
  - バージョン 0.0.22 の時点で、簡単な拡張モジュールを生成することができるが、カスタムのクラスや、戻り値・引数の再帰的なコピーがサポートされていない。
  - 生成されたC++ プログラムはlibstdc++ のほか、libgc (BoehmGC) 、libgcc (GCC)、libpcre (PCRE) 等に依存する。

## 関連項目

  - [PyPy](https://ja.wikipedia.org/wiki/PyPy "wikilink")
  - [Psyco](https://ja.wikipedia.org/wiki/Psyco "wikilink")
  - [RPython](https://ja.wikipedia.org/wiki/PyPy "wikilink")

## 参考文献

<references/>

## 外部リンク

  - <http://sourceforge.net/projects/shedskin/>
  - <http://code.google.com/p/shedskin/>

[Category:Python](https://ja.wikipedia.org/wiki/Category:Python "wikilink")

1.