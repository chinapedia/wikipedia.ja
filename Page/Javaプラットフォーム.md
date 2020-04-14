> この記事は[Javaプラットフォーム](https://ja.wikipedia.org/wiki/Javaプラットフォーム)から翻訳されています。


**Javaプラットフォーム**（ジャバプラットフォーム、[英](../Page/英語.md "wikilink"): ）は、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で記述されたプログラムの開発および実行を行うことのできるソフトウェア群の総称である。

## 概要

Javaのプログラムは、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) や[ハードウェア](../Page/ハードウェア.md "wikilink")に依存しない[バイトコード](../Page/バイトコード.md "wikilink")（中間言語）と呼ばれる抽象的なコードで表現されている。そのため、Javaプログラムの実行に必要な[仮想マシン](../Page/仮想機械.md "wikilink") () や、開発に必要な標準ライブラリセットおよびコンパイラを個々の環境にあわせて作りさえすれば、Javaプログラムはそれら全ての環境で同一に動く。Javaプラットフォームとはこうした実行環境および開発環境のことである。

Javaプラットフォームは、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Javaアプレット](../Page/Javaアプレット.md "wikilink")、[Java Runtime Environment](../Page/Java_Runtime_Environment.md "wikilink")、[JVM](../Page/Java仮想マシン.md "wikilink")、[携帯電話](../Page/携帯電話.md "wikilink")や[組み込み機器対応Java](../Page/組み込みシステム.md "wikilink") ([Java ME](../Page/Java_Platform,_Micro_Edition.md "wikilink"))、[Java Web Start](../Page/Java_Web_Start.md "wikilink")、Java製[アプリケーションなども含めてまとめて単純に](../Page/アプリケーションソフトウェア.md "wikilink")「**Java**」と呼ばれることがある。

Javaプラットフォームにはいくつかのエディションがあり、PCの[スタンドアロン](https://ja.wikipedia.org/wiki/スタンドアロン "wikilink")アプリケーションや他のエディションの基礎となるJava Standard Edition ([Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink"))、[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")や[Webサービス](../Page/Webサービス.md "wikilink")など、サーバーサイド用のJava Enterprise Edition ([Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink"))\[1\]、[スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink")のような携帯端末向けJava Micro Edition ([Java ME](../Page/Java_Platform,_Micro_Edition.md "wikilink")) が存在する。

2019年5月時点で、Javaプラットフォームの現在のメジャーバージョンは12である。なおJavaプラットフォームには、バージョン番号とは別の概念としてバージョン文字列というものがあり、現時点では1.8.0である。\[2\]

Javaプラットフォームは様々なプログラムから成り立っており、各々はそれ全体の能力から全く異なる一部品を提供する。例えば、Java[ソースコード](../Page/ソースコード.md "wikilink")を[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")に変換する[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")があり、それは[Java Development Kit](../Page/Java_Development_Kit.md "wikilink") (JDK) の一部として提供されている。実行環境である[Java Runtime Environment](../Page/Java_Runtime_Environment.md "wikilink") (JRE) は通常、オンザフライでバイトコードを[ネイティブマシンコードに変換する](../Page/機械語.md "wikilink")[JITコンパイラとして実装されている](../Page/実行時コンパイラ.md "wikilink")。また、[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")にプリコンパイルされた大規模なライブラリが存在する。アプリケーションが配置される手段も、[アプレットとしてウェブページに埋め込むなど多岐にわたる](../Page/Javaアプレット.md "wikilink")。他にも、[Java Platform Standard Edition 8 Documentation](https://docs.oracle.com/javase/8/docs/)にあるように様々なコンポーネントが存在する。

プラットフォームにある極めて重要なコンポーネントはJavaコンパイラ、ライブラリ、そして仮想マシン仕様で設計されたルールによってJava中間バイトコードを「実行」する実行環境である。

## Java仮想マシン

Javaプラットフォームの本質はJavaバイトコードを実行する「[仮想機械](../Page/仮想機械.md "wikilink") (**)」の発想である。Javaバイトコードは実行プログラムの下にどんなハードウェアやOSがあろうと全く同じである。JITコンパイラはJava仮想マシン (<em lang="en">Java virtual machine</em>) で動く。JITコンパイラは実行時にJavaバイトコードをネイティブなプロセッサ命令に翻訳し、プログラム実行中にメモリ上にネィティブコードをキャッシュする。

中間言語としてのバイトコードの使用は、バーチャルマシンが存在する様々なプラットフォーム上でJavaプログラムが走ることを可能にする。JITコンパイラの使用はローディングによる僅かな遅延と、それらが一度にほとんどまたは全てJITコンパイルされ、一度「ウォームアップ」した後で、Javaアプリケーションがネイティブなプログラムと同じくらいの速さで走る傾向があることを意味する。

[JREバージョン](../Page/Java_Runtime_Environment.md "wikilink")1.1以来、サンのJava VM実装は[インタプリタ](../Page/インタプリタ.md "wikilink")だけでなく、[JITコンパイラ](https://ja.wikipedia.org/wiki/JITコンパイラ "wikilink")も含んでいる。

## クラスライブラリ

最も現代的なOSでは、再利用可能なコードの大きな集まりがプログラマの仕事を容易にした。 このコードは一般的にアプリケーションが実行時に呼び出せる[動的読込ライブラリのセットとして提供される](https://ja.wikipedia.org/wiki/ライブラリ#動的リンク "wikilink")。Javaプラットフォームは特定のOSに依存しないため、アプリケーションは既存のライブラリのいくつかに頼ることはできない。それどころか、Javaプラットフォームは多くのものを含む標準クラスライブラリの集合を提供し、多くの現代のOSで一般に見つかる同じく再利用可能な機能の多くを含んでいる。

[Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")はJavaプラットフォームで三つの意図を役立てる。標準コードライブラリのように、それらはプログラマに、よく知られた、品目リストを保持する、複雑な文字列解析を行うというような共通のタスクを成し遂げる機能セットを提供する。その上、クラスライブラリはハードウェアやOSへの強い依存が普通である仕事を果たす抽象インタフェースを提供する。ネットワーク接続とファイルアクセスのようなタスクはよくプラットフォーム特有の能力に強く依存する。Javaのとライブラリは、時には内部に必要不可欠なネイティブコードを実装しており、時にはそれらのタスクを機能するJavaアプリケーションの標準インタフェースを提供する。最終的に、 いくらかの基礎を成すプラットフォームはJavaアプリケーションが期待する特色の全てをサポートするかもしれない。これらの件についていえば、クラスライブラリはどんなに役立つものも使うそれらの特色をエミュレートするか、特別な特色の存在をチェックする一貫した方法提供するかのどちらかを行使できる。

、[JREに含まれているクラスライブラリは依然として私有のソフトウェアである](../Page/Java_Runtime_Environment.md "wikilink")。互換性のあるフリーライブラリの集合で記述されている[Free Software Foundationの進行プロジェクトがある](https://ja.wikipedia.org/wiki/Free_Software_Foundation "wikilink")。それは[GNU Classpathと呼ばれている](../Page/GNU_Classpath.md "wikilink")。2006年11月13日に、サンはJavaソースコード全てが2007年3月に[GNU General Public Licenseのもとでリリースされると発表した](../Page/GNU_General_Public_License.md "wikilink")。\[3\]

## 言語

Javaという言葉そのものは、通常、Javaプラットフォームで設計されたJavaプログラミング言語を指す。プログラミング言語は一般的に「プラットフォーム」というフレーズの範囲外にあるにもかかわらず、Javaプログラミング言語はJavaプラットフォームの中心部品であると考えられている。Javaの言語と実行はそれゆえ、通例一単位と考えられている。

それでもやはり、[サードパーティー](../Page/サードパーティー.md "wikilink")はJavaプラットフォームを対象にしたかなり多くの[コンパイラ](../Page/コンパイラ.md "wikilink")や[インタプリタ](../Page/インタプリタ.md "wikilink")を生み出している。それらのうちいくつかは既存の言語として、他は一方はJava言語自身の拡張として存在する。これらは以下を含む:

### 拡張

  - [AspectJ](https://ja.wikipedia.org/wiki/AspectJ "wikilink") - [アスペクト指向プログラミング](../Page/アスペクト指向プログラミング.md "wikilink")を実現できるJava

  - (GJ) - これはJava SE 5.0で正式にJavaに取り込まれた。

### 言語

  - [Ceylon](https://ja.wikipedia.org/wiki/Ceylon "wikilink")
  - [Clojure](https://ja.wikipedia.org/wiki/Clojure "wikilink") - [LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")方言の一つ
  - [Fortress](https://ja.wikipedia.org/wiki/Fortress "wikilink")
  - [Groovy](../Page/Groovy.md "wikilink")
  - [JRuby](https://ja.wikipedia.org/wiki/JRuby "wikilink") - [Ruby](../Page/Ruby.md "wikilink")インタプリタ
  - [Jython](../Page/Jython.md "wikilink") - Python-Javaバイトコードコンパイラ jythonc を含む[Python](../Page/Python.md "wikilink")インタプリタ
  - [Kawa](https://ja.wikipedia.org/wiki/Kawa "wikilink") - LISP方言の一つである[Scheme](../Page/Scheme.md "wikilink")のインタプリタ
  - [Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")
  - [Processing](../Page/Processing.md "wikilink")
  - [Rhino](../Page/Rhino.md "wikilink") - [JavaScript](../Page/JavaScript.md "wikilink") インタプリタ
  - [Scala](../Page/Scala.md "wikilink")

## 類似プラットフォーム

Javaの成功とそのコンセプト[write once, run anywhereは](https://ja.wikipedia.org/wiki/write_once,_run_anywhere "wikilink")、2002年に現れて以来、[.NET Frameworkプラットフォームなど他の類似する取り組みを導き](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、それらはJavaの成功側面の多くを受けいれた。しかしながら、.NETの完全な実装は[Microsoft Windowsのみに向けたものしか存在しない](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。一方、Javaは多くのプラットフォームで完全にサポートされている。しかし.NETは、多くの異なるプログラミング言語を[共通中間言語](../Page/共通中間言語.md "wikilink")へとコンパイルする言語非依存ライブラリのユーザビリティに強い主眼点を置いている。.NETは言語非依存互換性の面ではJavaよりも成功している。しかし、Javaにも[Scala](../Page/Scala.md "wikilink")、[Jython](../Page/Jython.md "wikilink")、[Groovy](../Page/Groovy.md "wikilink")、[JRubyなどJavaVMを実行プラットフォームとする言語処理系が複数存在する](https://ja.wikipedia.org/wiki/Ruby#JRuby "wikilink")。

.NETにも[Visual J\#というJavaの実装が存在するが](../Page/J_Sharp.md "wikilink")、これは本家のJavaとは非互換で、関連するクラスライブラリは殆ど言語バージョンが古い**JDK 1.1**に基づいている。これらは、Visual J\#が.NETにおける主要な言語として設計されたのではなく、Javaから.NETプラットフォームへ移行するために用意された言語であることに起因する。

その一方で、近年ではオープンソースコミュニティによって[IKVM.NET](../Page/IKVM.NET.md "wikilink")という[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink")上で動作するJava仮想マシンが登場し、一方的ではあるが、互換性及び相互利用性は急激に向上している。

## 脚注

<references />

## 関連項目

  - [共通言語基盤](../Page/共通言語基盤.md "wikilink") (CLI)
  - [Dalvik仮想マシン](../Page/Dalvik仮想マシン.md "wikilink")

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink")

1.
2.
3.