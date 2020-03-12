> この記事は[GNU Classpath](https://ja.wikipedia.org/wiki/GNU_Classpath)から翻訳されています。


**GNU Classpath** は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[標準クラスライブラリの](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")[フリーな実装を作るプロジェクトである](../Page/フリーソフトウェア.md "wikilink")。[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")の[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部である。作成すべきライブラリは膨大だが、そのほとんどは完了しており、[Swing](../Page/Swing.md "wikilink")、[CORBAなども含まれる](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")。ClasspathではJ2SE 1.4および5.0の全クラスをほとんど実装してきた。従ってClasspathを[Vuze](../Page/Vuze.md "wikilink")や[Eclipseといった一般的なJavaベースのソフトウェアで使うことができる](../Page/Eclipse_\(統合開発環境\).md "wikilink")。

GNU Classpathはライセンス条件の違いがあるため、[libgcjと並行して開発された](../Page/GNU_Compiler_for_Java.md "wikilink")。現在ではGPLを採用することで合意がなされ、両プロジェクトは統合された。

## ライセンス

GNU Classpathは、[リンクに関する例外付きの](https://ja.wikipedia.org/wiki/GPLリンク例外 "wikilink")[GPLの条件下でライセンス提供される](../Page/GNU_General_Public_License.md "wikilink")。すなわち、[オープンソース](../Page/オープンソース.md "wikilink")の[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。全コードは形式上[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")の所有となっており、その所有権は開発者たちとの契約上の義務によって束縛されている。

## Uses

GNU Classpathは多くのフリーなJava実装（[Kaffe](https://ja.wikipedia.org/wiki/Kaffe "wikilink")、[SableVM](https://ja.wikipedia.org/wiki/SableVM "wikilink")、[JamVM](http://jamvm.sourceforge.net/)、[CACAO](http://www.cacaojvm.org/)、[Jikes RVM](http://jikesrvm.org/)など）で採用されている。というのも、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")を実装した際に標準クラスライブラリが必須であり、GPLライセンスとするには選択肢はあまりないためである。

他に以下のもので使われている。

  - [GNU Compiler for Java](../Page/GNU_Compiler_for_Java.md "wikilink") (GCJ) はJavaのコードをネイティブな独立した（Java VMを必要としない）実行ファイルにコンパイルする機能を持つ。
  - [IKVM.NET](../Page/IKVM.NET.md "wikilink")はJavaと[.NET Frameworkを結びつけるものである](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。
  - [JNode](https://ja.wikipedia.org/wiki/JNode "wikilink")はJavaアプリケーションが動作する[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")であり、Javaと[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")だけで書かれている。
  - [Jaos](http://www.oberon.ethz.ch/jaos/overview.html)は[Oberon-2](https://ja.wikipedia.org/wiki/Oberon-2 "wikilink")言語と結びついた特殊なJava VMである。
  - [Jupiter Project](http://www.eecg.toronto.edu/jupiter/)はクラスタ上の分散コンピューティング向け仮想機械。[Myrinet](https://ja.wikipedia.org/wiki/Myrinet "wikilink")で128プロセッサを結合したマシンで動作。

## 歴史

GNU Classpathの開発は5人の開発者が1998年に開始した。その後、他のプロジェクトとの合併を何回か経験している ([Kaffe](https://ja.wikipedia.org/wiki/Kaffe "wikilink"), libgcj)。かつて、GNU Classpathは独自の仮想マシン (Japher) を提供していた。Classpathが標準ライブラリとして充実するにつれて他のプロジェクトで利用されることが多くなり、仮想マシンが使われなくなったため、Japherの開発は中止された。公式のJava 1.4 APIのほとんどを実装した後、プロジェクトはバグ修正を主に行うようになった。2006年10月24日、1.4で最後まで実装されていなかったクラスHTMLWriterの実装が完了した。開発速度（一日平均の追加[コード行数](https://ja.wikipedia.org/wiki/コード行数 "wikilink")で計算）は2006年になって最高潮に達した。

GNU Classpathという名称はBradley M. Kuhnが初期の開発者Paul Fisherに示唆したものである。当時、Javaのフリーな実装に[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の商標を付与することを強いることについて、コミュニティには大きな懸念があった。KuhnはJavaのライブラリの場所を指す[`$CLASSPATH`という](https://ja.wikipedia.org/wiki/クラスパス "wikilink")[環境変数](../Page/環境変数.md "wikilink")を名称に使ってはどうかと示唆したのである。`$CLASSPATH`は実際に使われる際に*java*（例えば`/usr/lib/java`）という文字列を含むディレクトリのパス名に展開される。従って具体的に*Java*という単語を使わずにそれを連想させることができるのである。Fisherらは*$*や全部大文字の名前を好まなかったため、*Classpath*に落ち着いた。

## 開発チーム

プロジェクトチームには70名の開発者がおり（うち、約20名が常時活動している）、管理者が1名活動している。管理者は法律面の対応をし、定期的なリリースの実行と品質管理にも関与する。管理者は[CVSへのアクセス許可も行う](../Page/Concurrent_Versions_System.md "wikilink")。

他のプロジェクトとは異なり、GNU Classpathには正式な階層構造がない。技術的に可能な者が可能なことをしており、明確な分担は存在しない。コード修正はまずディスカッションリストにパッチとして投稿され、問題があればそこで議論される。毎日、5件から8件のパッチ投稿がある。

プロジェクトは独自のテストスイート (Mauve) を使っている。175,000項目のテストが毎日実行され、公式のAPIと互換が保たれていることが確認されている。

## 仮想マシンとの繋がり

GNU Classpathには、公式なJava APIネームスペースにあるクラス群がある。これらクラス内でネイティブコードにアクセスする必要が生じた場合、少数の "VM" クラス群が使われる。VMクラス群は本来のクラス名の前に**VM**と付けたものである（VMObject、VMStringなど）。VMクラス群は他のコードとは分離して格納され、private属性と final属性を付与される。これらのクラスのメソッドには*native*というキーワードが含まれ、サポートライブラリが必要であることを示している。このようなライブラリはJava仮想マシンの側で用意する。GNU Classpathが接続できるJava仮想マシンは、そのソースコードにアクセス可能で修正可能な場合である。例えば、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の仮想マシンはこの条件を満たしていないので、使えない。

## Java 1.5の新言語機能サポート

バージョン 0.95以前、GNU Classpathリリースでは 2つのtarballがリリースされていた。一方はメインの開発ブランチであり、もう一方はより実験的なブランチである。後者では[総称型](https://ja.wikipedia.org/wiki/総称型 "wikilink")、[列挙型](../Page/列挙型.md "wikilink")、[アノテーション](../Page/アノテーション.md "wikilink")といったJava 1.5の新機能が追加されている。

バージョン 0.95からはJava 1.5の総称型のような追加機能はメインブランチに完全に統合されている。Eclipseのコンパイラ (ecj) でJava 1.5のソースコードをバイトコードにコンパイルし、それをGCJでネイティブコードに変換できる[1](http://www.gnu.org/software/classpath/announce/20070423.html)。

## サンのオープンソースコンパイラとのインタフェース

バージョン 0.95 から、[GPLのオープンソースの](../Page/GNU_General_Public_License.md "wikilink")[javac](https://ja.wikipedia.org/wiki/javac "wikilink")でGNU Classpathのランタイム ([GIJ](https://ja.wikipedia.org/wiki/GNU_Interpreter_for_Java "wikilink")) とコンパイラ ([GCJ](../Page/GNU_Compiler_for_Java.md "wikilink")) が利用可能となり、また、GNU Classpathのクラスライブラリやツールや例をjavac自身でコンパイル可能となっている。

## omg.org ドメインに由来するクラス

GNU Classpathは、フリーでないライセンスのコードやフリーでないライセンスのコードから自動的に生成されたコードを受理しない。標準Java APIにはomg.orgドメインのクラスが多数含まれており、これらは[Object Management Groupがリリースした](../Page/Object_Management_Group.md "wikilink")[IDLファイルから生成されたものである](../Page/インタフェース記述言語.md "wikilink")。これらのファイルは改変が許されていないためフリーではない。そのため、GNU Classpathでは、OMGの公式仕様書を参照して、対応するクラスを一から手で書いた。従って、GNU Classpathのそれらのコードも他の部分と同様に、フリーソフトウェアとして利用可能である。

## 関連項目

  - [Apache Harmony](../Page/Apache_Harmony.md "wikilink")
  - [GNU Compiler for Java](../Page/GNU_Compiler_for_Java.md "wikilink")
  - [Kaffe](https://ja.wikipedia.org/wiki/Kaffe "wikilink")
  - [IcedTea](https://ja.wikipedia.org/wiki/IcedTea "wikilink")

## 外部リンク

  - [GNU Classpath homepage](http://www.gnu.org/software/classpath/)
  - [Automatically generated documentation, including source code](http://developer.classpath.org/doc/)
  - [Test runs and binary compatibility tests](http://builder.classpath.org)
  - [May 2006 article by a GNU Classpath developer](http://lwn.net/Articles/184967/) フリーJavaプロジェクトの状況について
  - [Permeable Development](http://public.smi.ethz.ch/blog/2006/01/25/permeable-development/)

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Javaプラットフォームソフトウェア](https://ja.wikipedia.org/wiki/Category:Javaプラットフォームソフトウェア "wikilink")