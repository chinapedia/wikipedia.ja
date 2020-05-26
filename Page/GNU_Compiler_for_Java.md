> この記事は[GNU Compiler for Java](https://ja.wikipedia.org/wiki/GNU_Compiler_for_Java)から翻訳されています。


**GNU Compiler for Java**（グニュー・コンパイラ・フォー・ジャバ、**GCJ**、ジーシージェー）は[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のためのフリーな[コンパイラ](../Page/コンパイラ.md "wikilink")で、[GCCの一部である](../Page/GNUコンパイラコレクション.md "wikilink")。Java[ソースコード](../Page/ソースコード.md "wikilink")をコンパイルし、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")の[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")または[機械語](../Page/機械語.md "wikilink")を出力する。また、バイトコードを格納した[Javaクラスファイル](https://ja.wikipedia.org/wiki/Javaクラスファイル "wikilink")や、それらを格納した[JAR](https://ja.wikipedia.org/wiki/JAR "wikilink")全体をマシン語にコンパイルすることも出来る。GCJで使用されるほとんど全ての[ランタイムライブラリ](../Page/ランタイムライブラリ.md "wikilink")は[GNU Classpathプロジェクトに由来する](../Page/GNU_Classpath.md "wikilink")。

[AWTと](../Page/Abstract_Window_Toolkit.md "wikilink")[Swing](../Page/Swing.md "wikilink")の2つのグラフィカル[APIをGNU](../Page/アプリケーションプログラミングインタフェース.md "wikilink") Classpathにサポートさせることに現在多くの労力が投入されている。AWTとSwingの両方のフルサポートは間近であり、AWT/Swingアプリケーションを実行するために[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")から提供されたランタイムを使用する必要性は遠からずなくなる見通しである。

2015年より、新しい開発のアナウンスはなく、製品はメンテナンスモードとなった\[1\]。2016年9月30日、GCJはGCCのtrunkから削除された\[2\]\[3\]。削除のアナウンスは、GCJを含まないGCC 7.1のリリースとともに行われた\[4\]。GCJはGCC 6の一部として残されている。

## CNI (Compiled Native Interface)

CNI (Compiled Native Interface)は、ネイティブアプリケーションや[C++](../Page/C++.md "wikilink")で記述されたライブラリを、Javaコードとの間で相互に呼び出せるようにするためのGCJのための[ソフトウェアフレームワーク](https://ja.wikipedia.org/wiki/ソフトウェアフレームワーク "wikilink")である。

これは多くのJava仮想マシンで標準とされている[JNI](https://ja.wikipedia.org/wiki/JNI "wikilink")(Java Native Interface)フレームワークに似ているが、CNIの作成者はJNIに対して幾つもの優位性を主張している。

> *我々はCNIをより良い手段だと考えて採用している。特に、Javaは標準的なコンパイル技術を使って実装されるもう一つのプログラミング言語に過ぎない、とする発想に基づいたJava実装において、より良いと考える。それゆえ、そしてGCCを用いた言語実装は出来るだけ互換であるべきなので、Javaの呼び出し規約は、他の言語、特にC++で使用される規約に対して、実用性を損なわない範囲で極力似ていなければならない。なぜなら我々は、JavaをC++のサブセットと考えることもできるためである。CNIは、単にC++とJavaは同じ呼び出し規約とオブジェクト配置を持ち、バイナリ互換である、という発想によるヘルパー関数と規約のセットである。(この説明は単純化されているが、十分に正確である）*\[5\]

## 脚注

## 関連項目

  - [GNU Interpreter for Java](https://ja.wikipedia.org/wiki/GNU_Interpreter_for_Java "wikilink")
  - [GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")
  - [Kaffe](../Page/Kaffe.md "wikilink")

## 外部リンク

  - [GCJ Homepage](http://gcc.gnu.org/java/)
  - [GCJ Manual](http://gcc.gnu.org/onlinedocs/gcj/)
  - [About CNI section of GCJ Manual](http://gcc.gnu.org/onlinedocs/gcj/About-CNI.html)
  - [GCJ Frequently Asked Questions](http://gcc.gnu.org/java/faq.html)
  - [GCC/GCJ for MinGW](http://www.thisiscool.com/gcc_mingw.htm)

[Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [GCC Looks To Turn Off Java, Replace With Go Or ADA](https://www.phoronix.com/scan.php?page=news_item&px=MTUwOTA)
2.
3.
4.
5.  The GCJ FAQ 2.3 Why does GCJ use CNI?[1](http://gcc.gnu.org/java/faq.html#2_3) より