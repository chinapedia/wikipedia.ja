> この記事は[Jython](https://ja.wikipedia.org/wiki/Jython)から翻訳されています。


**Jython**(旧称JPython)は、プログラミング言語[Python](../Page/Python.md "wikilink")のJavaで書かれた実装である。Jim Huguninによって開発が始められた。

## 概要

Jythonプログラムはあらゆる[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のクラスをシームレスにインポートできる。例えば、Javaの[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")ライブラリである[Swing](../Page/Swing.md "wikilink")、[AWT](../Page/Abstract_Window_Toolkit.md "wikilink")、[SWT](https://ja.wikipedia.org/wiki/SWT "wikilink")などを使って書くことができる。また、逆にPythonでJavaプログラムから使うクラスを実装することも可能である。Jythonは[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")にコンパイルされて作動するが、これは動的にも静的にも可能である。

一部の標準モジュールを除いては、JythonのプログラムはPythonモジュールの代わりにJavaのクラスを使っている。Jythonはほぼ全てのPython標準のライブラリを含んでいるが、C言語で実装された一部ライブラリは除外されている。

## ライセンス

Jythonは、現在は制約の緩いフリーソフトウェアライセンスである[Python Software Foundation Licenseのもとでリリースされている](https://ja.wikipedia.org/wiki/Python_Software_Foundation_License "wikilink")。 Jython2.0,2.1のライセンスは独自だが、制約の緩いフリーソフトウェアライセンスである。 JPython 1.1.xのライセンスも制約の緩いフリーソフトウェアライセンスであると考えられるが、内容が複雑であり、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")や[オープンソース・イニシアティブの査読やコメントも無いため明確ではない](../Page/Open_Source_Initiative.md "wikilink")。

## 歴史

Jim Huguninが開発を1997年に始め、1999年まで開発を続けた。1999年2月に第一開発者がBarry Warsawに変わった。2000年10月にはSourceForge上で開発されるようになった。以来、長年、Samuel PedroniがJythonの保守/開発を担ってきた。2004年末にSamuel Pedroniは[PyPy](https://ja.wikipedia.org/wiki/PyPy "wikilink")に集中するため第一開発者からは退いたのだが、依然彼の発言はJython開発コミュニティにて最も権威あるものと考えられている。2005年1月にはBrian Zimmerが[Pythonソフトウェア財団](https://ja.wikipedia.org/wiki/Pythonソフトウェア財団 "wikilink")から開発続行のための補助金を受けている。2005年12月には第一開発者がFrank WierzbickiからBrian Zimmerに譲られる。2005年頃はJythonの開発は続いたものの、知識とJythonに掛けられる時間のある開発者を確保できなかったため、開発は遅くなってしまった。現在も開発は着実に続けられている。

## 現状とロードマップ

現在のリリースはJython-2.5で、Javaとの統合が更に図られた他、[CPython](https://ja.wikipedia.org/wiki/CPython "wikilink")の2.5相当の機能を実装している。([Jythonロードマップ](http://wiki.python.org/jython/RoadMap)を参照のこと)。

## 用例

  - [WebSphere Application Server](../Page/WebSphere_Application_Server.md "wikilink") - Jaclとともにスクリプト言語として使用されている

## 関連プロジェクト

  - [Groovy](../Page/Groovy.md "wikilink") - [Java仮想マシン](../Page/Java仮想マシン.md "wikilink")での作動を前提とする独自の動的言語
  - [Jacl](https://ja.wikipedia.org/wiki/Jacl "wikilink") - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")による[Tcl](https://ja.wikipedia.org/wiki/Tcl "wikilink")の実装
  - [JRuby](https://ja.wikipedia.org/wiki/JRuby "wikilink") - [Java](https://ja.wikipedia.org/wiki/Java "wikilink")による[Ruby](../Page/Ruby.md "wikilink")の実装
  - [IronPython](../Page/IronPython.md "wikilink") - [.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")/[Mono向けのPython実装](../Page/Mono_\(ソフトウェア\).md "wikilink")。Jythonを作ったJim Huguninによって開発が始められた。

## 外部リンク

  - [Jython ホームページ](http://www.jython.org/)
  - [Jython Sourceforge Page](http://sourceforge.net/projects/jython/)
  - [differences between CPython and Jython](http://jython.sourceforge.net/docs/differences.html)
  - [Charming Jython: Learn how the Java implementation of Python can aid your development efforts](http://www-106.ibm.com/developerworks/java/library/j-jython.html)
  - [Get to know Jython](http://www-106.ibm.com/developerworks/library/j-alj07064/)
  - [Learn how to write DB2 JDBC tools in Jython](http://www-106.ibm.com/developerworks/db2/library/techarticle/dm-0404yang/index.html)
  - [Tips for Scripting Java with Jython](http://www.onjava.com/pub/a/onjava/2002/03/27/jython.html)
  - [Jython tips for Python programmers](http://www.onlamp.com/pub/a/python/2002/04/11/jythontips.html)
  - [Jython license information](http://www.jython.org/Project/license.html)
  - [Scripting on the Java platform](http://www.javaworld.com/javaworld/jw-11-2007/jw-11-jsr223.html)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Pythonの実装](https://ja.wikipedia.org/wiki/Category:Pythonの実装 "wikilink")