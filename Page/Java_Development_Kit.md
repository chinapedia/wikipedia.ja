> この記事は[Java Development Kit](https://ja.wikipedia.org/wiki/Java_Development_Kit)から翻訳されています。


**Java Development Kit** (**JDK**) は[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")（旧[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）により提供されている、プログラミング言語[Java](https://ja.wikipedia.org/wiki/Java "wikilink")を使って[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")およびその他の[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")を構築するための[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") (SDK) および開発環境である\[1\]。[Linux](../Page/Linux.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")または[Windows向けのパッケージがそれぞれ用意されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。JDK 11までは[Solaris](../Page/Solaris.md "wikilink")向けのパッケージも用意されていた\[2\]\[3\]。Javaの[APIセットおよび実行環境](../Page/アプリケーションプログラミングインタフェース.md "wikilink") ([Java Runtime Environment](../Page/Java_Runtime_Environment.md "wikilink"), JRE) はその用途ごとに、[Java Platform, Standard Edition](../Page/Java_Platform,_Standard_Edition.md "wikilink") (Java SE)、[Java Platform, Enterprise Edition](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") (Java EE)、[Java Platform, Micro Edition](../Page/Java_Platform,_Micro_Edition.md "wikilink") (Java ME) などのエディション（プロファイル）が用意されているが、JDKはJava SE向けの開発に対応する。Java EE向けの開発にはJava EE SDKが\[4\]、Java ME向けの開発にはJava ME SDKが\[5\]それぞれ用意されている。

[2006年](../Page/2006年.md "wikilink")11月17日に、サンはJDKを[GNU General Public License](../Page/GNU_General_Public_License.md "wikilink") (GPL) に基づきリリースすると発表した。サンは実際に[2007年](../Page/2007年.md "wikilink")5月8日にJDKのソースコードを[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")に寄付した\[6\]。従ってJDKは[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")である。OpenJDKなどの他の実装と区別するため、従来のJDKはSun JDKあるいはOracle JDKとも呼ばれる。

## JDKの内容

JDKには主要なコンポーネントとして以下のようなプログラミングツールが含まれる :

  - appletviewer – このツールは[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")なしで[Javaアプレット](../Page/Javaアプレット.md "wikilink")を起動しデバッグするために使用される。
  - apt – アノテーション処理ツール\[7\]
  - extcheck – JARファイル衝突を検出可能なユーティリティ
  - idlj – IDL-to-Javaコンパイラ。このユーティリティは指定されたJava IDLファイルからJava[バインディングを生成する](https://ja.wikipedia.org/wiki/束縛_\(情報工学\) "wikilink")。
  - java – Javaアプリケーション用の[ローダ](../Page/ローダ.md "wikilink")。このツールはインタプリタで、[javac](https://ja.wikipedia.org/wiki/javac "wikilink")コンパイラにより生成されたクラスファイルを解釈できる。現在では1つのランチャーが開発と配備の両方で使用される。古い配備ランチャーであるjreはもう付属せず、代わりに新しいjavaローダに置き換えられた。
  - [javac](https://ja.wikipedia.org/wiki/javac "wikilink") – [Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")で、ソースコードを[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")に変換する。
  - [javadoc](https://ja.wikipedia.org/wiki/javadoc "wikilink") – ドキュメンテーション生成器で、ソースコードのコメントから自動的にドキュメンテーションを生成する。
  - jar – アーカイバで、関連するクラス[ライブラリ](../Page/ライブラリ.md "wikilink")を単一の[JARファイルにパッケージする](../Page/JAR_\(ファイルフォーマット\).md "wikilink")。このツールはJARファイルを管理するのにも役に立つ。
  - javah – Cヘッダとスタブ生成器で、ネイティブメソッドを書くのに使われる。
  - javap – クラスファイル[逆アセンブラ](../Page/逆アセンブラ.md "wikilink")
  - javaws – JNLPアプリケーション用の[Java Web Startランチャー](../Page/Java_Web_Start.md "wikilink")
  - JConsole – Javaモニタリングおよび管理コンソール
  - jdb – [デバッガ](../Page/デバッガ.md "wikilink")
  - jhat – Javaヒープ分析ツール（実験用）
  - jinfo – このユーティリティにより起動中のJavaプロセスやクラッシュダンプから設定情報を得る（実験用）
  - jmap – このユーティリティはJava用のメモリマップを出力し、指定のプロセスやコアダンプの共有オブジェクトメモリマップやヒープメモリの詳細を表示できる（実験用）
  - jps – Java仮想マシンプロセスステータスツールはターゲットとなるシステム上に取り付けられたHotSpot Java仮想マシンを一覧にする（実験用）
  - jrunscript – Javaコマンドライン[スクリプト](../Page/シェルスクリプト.md "wikilink")[シェル](../Page/シェル.md "wikilink")
  - jstack – JavaスレッドのJava[スタックトレース](../Page/スタックトレース.md "wikilink")を表示するユーティリティ
  - jstat – [Java仮想マシン](../Page/Java仮想マシン.md "wikilink")静的モニタリングツール（実験用）
  - jstatd – jstatデーモン（実験用）
  - keytool – キーストアを操作するためのツール
  - pack200 – JAR圧縮ツール
  - policytool – ポリシー作成および管理ツールで、様々なソースからコード用に利用可能であるかどうかのパーミッションを指定することで、Javaランタイム用のポリシーを決定できる。
  - VisualVM – いくつかの[コマンドラインJDKツールを統合するビジュアルツールで](../Page/キャラクタユーザインタフェース.md "wikilink")、軽快なパフォーマンスでメモリ[プロファイリングが可能である](../Page/性能解析.md "wikilink")。
  - wsimport – Webサービス呼び出し用のポータブルなJAX-WSアーティファクトを生成する。
  - xjc – Java API for XML Binding (JAXB) APIの一部。XMLスキーマを受けてJavaクラスを生成する。

実験用ツールはJDKの将来のバージョンで利用不可能になるかもしれない。

JDKには、通常**プライベートランタイム**と呼ばれる完全な[Java Runtime Environment](../Page/Java_Runtime_Environment.md "wikilink") (JRE) も付属する。JDKが「レギュラー」なJREから分離され余分な内容が含まれているためである。それは[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")および、[国際化と地域化](../Page/国際化と地域化.md "wikilink")ライブラリや[IDLライブラリのような](../Page/インタフェース記述言語.md "wikilink")、開発者にのみ役に立つ追加ライブラリと同様に、生産環境として提供されるクラスライブラリの全てから構成される。

JDKのコピーは、Java APIのほとんど全ての部分の利用を説明する広範囲なプログラム例の抜粋も含んでいる。

## JDKとSDKの曖昧さ

JDKは[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") (SDK) の拡張されたサブセットになる。Java SE、EE、そしてMEを実装するに付属している説明書によると、サンはその専門用語に基づいてJDKを認め、JDKはJavaプログラムを書くことと起動することに対して責任があるSDKのサブセットとなる。SDKの残りは、アプリケーションサーバ、デバッガ、そしてドキュメンテーションといった余分なソフトウェアを含む。

## 他のJDK

本記事で論じられ最も広範囲に利用されるJDKに加えて、Sun JDKソースやそうではない物である、様々なプラットフォームで一般的に利用可能な他のJDKもある。それら全ては基本的なJava仕様に基づいているが、ガベージコレクション、コンパイル方法、そして最適化技術といった明確に指定されていない部分はしばしば異なる。それらを以下に示す。

開発中やメンテナンスモードの状態であるもの:

  - [OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink") / [IcedTea](https://ja.wikipedia.org/wiki/IcedTea "wikilink")

  - [GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の[GNU Classpath](../Page/GNU_Classpath.md "wikilink")、[GNU Interpreter for Java](https://ja.wikipedia.org/wiki/GNU_Interpreter_for_Java "wikilink") (GIJ) および[GNU Compiler for Java](../Page/GNU_Compiler_for_Java.md "wikilink") (GCJ)

  -

  - [IBM J9](https://ja.wikipedia.org/wiki/IBM_J9 "wikilink") JDK – AIX、Linux、Windows、MVS、OS/400、Pocket PC、z/OS用\[8\]

  - [オラクルの](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink") JDK – Windows、Linux、Solaris用\[9\]

メンテナンスが終了したもの:

  - [Apache Harmony](../Page/Apache_Harmony.md "wikilink")

  - [アップルの](../Page/アップル_\(企業\).md "wikilink")[Classic Mac OS用の](../Page/Classic_Mac_OS.md "wikilink") JVM / JDK\[10\]

  - – Linux用のSun JDKの[移植](../Page/移植_\(ソフトウェア\).md "wikilink")\[11\]\[12\]

## 関連項目

  - [Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")
  - [クラスパス](https://ja.wikipedia.org/wiki/クラスパス "wikilink")

## 脚注

## 外部リンク

  - [Oracle - Java SE](http://www.oracle.com/technetwork/jp/java/javase/overview/)
  - [IBM Java technology JDK](http://www.ibm.com/developerworks/java/jdk/)
  - [OpenJDK](http://openjdk.java.net/)
  - [GCJ](http://gcc.gnu.org/java/)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:ソフトウェア開発キット](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発キット "wikilink")

1.  [Java SE Development Kit 13- - Downloads](https://www.oracle.com/technetwork/java/javase/downloads/jdk13-downloads-5672538.html)
2.  [Java SE Development Kit 11- - Downloads](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html)
3.  Java 12以降をSolaris上で利用したい場合、OpenJDKを使用することが推奨されている。[Update on Oracle Java on Oracle Solaris | Oracle Solaris Blog](https://blogs.oracle.com/solaris/update-on-oracle-java-on-oracle-solaris)
4.  [Java EE - Downloads: GlassFish and Java EE 8 | Oracle Technology Network | Oracle](https://www.oracle.com/technetwork/java/javaee/downloads/index.html)
5.  [Java ME SDK](https://www.oracle.com/technetwork/java/embedded/javame/javame-sdk/overview/index.html)
6.
7.
8.
9.
10.
11.
12.