> この記事は[Javac](https://ja.wikipedia.org/wiki/Javac)から翻訳されています。


**javac**（「ジャバシー」や「ジャバック」と発音される）は最も基本的な[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")で、[オラクルの](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")[Java Development Kit](../Page/Java_Development_Kit.md "wikilink") (JDK) に含まれる。

javacコンパイラは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")言語仕様 (JLS) に準拠する[ソースコード](../Page/ソースコード.md "wikilink")を入力として、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")仕様 (JVMS) に準拠する[バイトコードを生成する](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")。

javac自体が[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれており（[セルフホスティング](../Page/セルフホスティング.md "wikilink")）、さらにjavacをプログラムから呼び出すこともできる\[1\]。

## 歴史

[2006年](../Page/2006年.md "wikilink")[10月13日](../Page/10月13日.md "wikilink")より、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のJava仮想マシン (JVM) と[Java Development Kit](../Page/Java_Development_Kit.md "wikilink") (JDK) が[GPLに基づき利用できるようになった](../Page/GNU_General_Public_License.md "wikilink")\[2\]（[Sun's OpenJDK Hotspot page](https://openjdk.dev.java.net/hotspot/)も参照）。

[Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")の[フリーな実装である](../Page/フリーソフトウェア.md "wikilink")[GNU Classpathは](../Page/GNU_Classpath.md "wikilink")、バージョン0.95からClasspathランタイム ([GIJ](../Page/GNU_Compiler_for_Java.md "wikilink")) とコンパイラ ([GCJ](../Page/GNU_Compiler_for_Java.md "wikilink")) を用いたjavacのコンパイルと起動をサポートしており、GNU Classpath自身でGNU Classpathのクラスライブラリ、ツールおよびサンプルをコンパイルすることもできる\[3\]。

## 関連項目

  - [Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink") - Javaコンパイラ全般の紹介と、既存のjavac代替コンパイラのリストが書かれた記事。
  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")
  - [Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")
  - [OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")

## 脚注

## 外部リンク

  - [The Compiler Group](http://openjdk.java.net/groups/compiler/) - OpenJDKのjavacページ。
  - [The Java Virtual Machine Specification](http://java.sun.com/docs/books/vmspec/)
  - [JSR 199](http://www.jcp.org/en/jsr/detail?id=199) - JavaプログラムからJavaコンパイラを呼び出すためのJava Compiler API [Java Specification Request](../Page/Java_Community_Process.md "wikilink")

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")

1.  "\[...\]an application can access javac programmatically."
2.  [Sun opens Java (feature story)](http://www.sun.com/2006-1113/feature/story.jsp)
3.  "This release supports compiling and running the GPL OpenJDK javac compiler\[...\]"