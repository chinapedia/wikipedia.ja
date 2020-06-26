> この記事は[Apache Harmony](https://ja.wikipedia.org/wiki/Apache_Harmony)から翻訳されています。


**Apache Harmony**（アパッチ・ハーモニー）は、[オープンソース](../Page/オープンソース.md "wikilink")かつフリーな[Java](https://ja.wikipedia.org/wiki/Java "wikilink")実装である。[Java SE](https://ja.wikipedia.org/wiki/Java_SE "wikilink") 5, 6を元にしており、[Apache License](../Page/Apache_License.md "wikilink") Version 2 にて提供されていた。開発は[2005年](../Page/2005年.md "wikilink")5月に開始され、[2006年](../Page/2006年.md "wikilink")10月にはApache財団のトップレベルプロジェクトとなった。しかし別のオープンソース実装である[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")に集約される形となり、[2011年](../Page/2011年.md "wikilink")11月3日に開発終了した\[1\]\[2\]。

SDKやJREも配布されており、仮想機械にはDRLVMを、コンパイラにはEclipse Java Compilerを使用していた。

## 歴史

### 立ち上げ

HarmonyプロジェクトはフリーなJava実装の開発者たちを統括する動きと捉えられていた。多くの開発者はこの動きがApache, GNU等のプロジェクトとして纏まると期待していた。まずGNU開発者がプロジェクトの立ち上げ準備に関わったが、後にHarmonyでは[GNU Classpathのコードは利用しないと決定した](../Page/GNU_Classpath.md "wikilink")。ライセンス互換上の問題で、Harmonyと他プロジェクト間でのコードの共有が難しくなるという問題があったためである。Apache開発者たちは必要なクラスをスクラッチから書き始め、またソフトウエア会社からコードの寄贈を募集した。

### スクラッチから書き直す意味

GNU ClasspathとApacheプロジェクトが袂を分かったのは、[GPLと](../Page/GNU_General_Public_License.md "wikilink")[Apacheライセンス](https://ja.wikipedia.org/wiki/Apacheライセンス "wikilink")の違いにある。多くの組織や個人がこの相違点を取り上げ、派生物には公開義務が無いApacheライセンスの適用を望むとの意見が寄せられた。GNU Classpathは独占的ソフトウエアとのリンクは可能だが、GNU Classpath自身の非公開派生物を作成するのは法的に困難なためである。

しかし、いくらかのフリーソフトウエア開発者は、これらのライセンスやコミュニティ哲学の違いは別個に実装を行うまでは違わず、妥協点を探せなくはないと頻繁に否定的な意見を述べている。だが、時折現れるこういったプロジェクトへの反対的な提案は幅広い支持を得ていない。フリーソフトウエア支持者は以下の単純な言葉でこれを切って捨てている。"*more free software is not a problem*（フリーソフトウエアが多いことは問題ではない）".

### サンのTCKライセンスを巡る問題

2007年4月10日、Apache財団 (ASF) は[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")（サン）のCEO、[ジョナサン・シュワルツ](../Page/ジョナサン・シュワルツ.md "wikilink")宛にJava SE 5 テクノロジ互換キット (TCK) についての[公開書簡](https://ja.wikipedia.org/wiki/公開書簡 "wikilink")を送った\[3\]。TCKのライセンスはHarmonyユーザに利用範囲の制限を課すもので[JCPのルールに反しているから](../Page/Java_Community_Process.md "wikilink")、ASFにとって承諾しがたいものであると主張している。

  - テクノロジ互換キット (Technology Compatibility Kit) は、Java SE5仕様に実装が準拠しているかを確認するためのテストキットで、SunがJavaの仕様ライセンス内で規定している。

サンは企業のブログ上で回答し、TCKを含めJavaのオープンソース実装プラットフォームをGPLで提供したいが、まずはGNU/Linuxコミュニティに対してJavaプラットフォームのGPL提供を優先するとした。 このやりとりは一部からオープンなやり方ではないとサンやASFは批評を受けたが、結果的にはクラスライブラリ開示のスケジュールを考えると、より多くの提供をサンから受けることを目的にASFは強気に振舞ったのだと考える人もいた。

## 開発チーム

立ち上がるとすぐに、プロジェクトは既に開発に着手していたいくつかの会社から大きなコード寄贈を受けて動き出した。しかしながらメーリングリスト上での全般的な議論は常に開かれていた。

その後、プロジェクトにはASF管理者により\[4\]アパッチ流の開発方式\[5\]を取り入れたことにより、大きく成功したといえるだろう。2006年11月時点で、プロジェクトチームのコミッターは16人の開発者及び、[IBM](../Page/IBM.md "wikilink")と[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")に属する16の開発チームで構成されていた\[6\]。

## 開発終了前の状況

[2006年](../Page/2006年.md "wikilink")10月、Apache HarmonyプロジェクトはApache財団の公式プロジェクト (Top level Projects) に昇格された。

### ライブラリ実装

当初期待したソフトウエア会社からのコード寄贈は現実のものとなっていた。Apache Harmonyの作業コードにはIntelより寄贈された [Swing](../Page/Swing.md "wikilink"), [AWT](https://ja.wikipedia.org/wiki/Abstract_Windowing_Toolkit "wikilink"), [Java 2D](../Page/Java_2D.md "wikilink") のコードが加えられた。

クラスの実装については、2010年9月20日時点で (5.0M15, 6.0M3)、Java SE 5の99.00%、Java SE 6の97.54%が実装（クラス・メソッド・フィールドとして存在）されていた\[7\]。

また、HarmonyのテストスィートはGNU Classpathと比べてより厳密なものとなっていた。（2006年10月の時点で、GNU Classpathは20000 tests [1](http://wiki.apache.org/harmony/Unit_Tests_Pass_on_DRLVM)、Harmonyは 50000 [2](http://www.object-refinery.com/classpath/mauve/report/) である）

Harmonyプロジェクトの進捗は J2SE 1.4\[8\] と Java SE 5.0.\[9\]を追っている状態であり、Harmony v6.0 は java SE 6.0[3](http://harmony.apache.org/downloads.html#Harmony6_Snapshot) の別ブランチと見なす事ができるほどであった。

### 文書化

文書化については、Harmony は他のフリーの Java 実装より整備が進んでいない状態にあった。 たとえば、GNU Classpath では中心的な [CORBA](https://ja.wikipedia.org/wiki/CORBA "wikilink") のクラス (ORB) の各メソッドに関して、 抽象 API クラス [4](http://cvs.savannah.gnu.org/viewcvs/*checkout*/classpath/org/omg/CORBA/ORB.java?rev=1.2.2.12&root=classpath) と実装クラス [5](http://cvs.savannah.gnu.org/viewcvs/*checkout*/classpath/gnu/CORBA/OrbFunctional.java?rev=1.6&root=classpath) について説明のコメントが付いている。Harmony で使用されている [6](http://www.mail-archive.com/yoko-dev@incubator.apache.org/msg01428.html) [Yoko](http://incubator.apache.org/yoko/) プロジェクトでは、大半のメソッドについて 標準の宣言[7](http://svn.apache.org/repos/asf/incubator/yoko/trunk/yoko-spec-corba/src/main/java/org/omg/CORBA/ORB.java) および実装クラス [8](http://svn.apache.org/repos/asf/incubator/yoko/trunk/core/src/main/java/org/apache/yoko/orb/OBCORBA/ORB_impl.java) のドキュメント化がされていなかった（2006年10月時点）。また、GNU Classpath は、（Sunの実装同様）CORBA の機能について古いものと現在のものの両方をサポートしている。Harmony では、古い規格に基づく代表的なメソッド (ORB.connect(Object)) が全く実装されていないままであった。

### ツール

Javaプラットフォームの完全な実装には、たとえば Java ソースコードを[バイトコード](../Page/バイトコード.md "wikilink")に変換する[コンパイラ](../Page/コンパイラ.md "wikilink")、[Jar](https://ja.wikipedia.org/wiki/Jar "wikilink")ファイルを管理するプログラム、[デバッガ](../Page/デバッガ.md "wikilink")、[アプレット](https://ja.wikipedia.org/wiki/アプレット "wikilink")ビューアー、[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")などが必要である。Harmony ではコンパイラのみが実現されていた[9](http://incubator.apache.org/harmony/roadmap.html#General)。

### 仮想マシンのサポート

Harmony は、いずれも外部からの寄付による4種類の [Java VM](../Page/仮想機械.md "wikilink") 実装をサポートしていた。

  - JC Harmony Edition VM, "JCHEVM," [JCVM's](https://ja.wikipedia.org/wiki/:en:JC_virtual_machine "wikilink") [インタプリタ](../Page/インタプリタ.md "wikilink") に基づいており、[Archie Cobbs](https://ja.wikipedia.org/wiki/Archie_Cobbs "wikilink") によって寄贈された。
  - BootJVM, シンプルな[ブートストラップ可能な仮想マシンで](https://ja.wikipedia.org/wiki/:en:Bootstrapping_\(computing\) "wikilink")、[Daniel Lydick](https://ja.wikipedia.org/wiki/Daniel_Lydick "wikilink") によって寄贈された。
  - [SableVM](../Page/SableVM.md "wikilink") は先進的でポータブルなインタプリタで、[Sable Research Group](https://ja.wikipedia.org/wiki/:en:Sable_Research_Group "wikilink") および Dynamic Runtime Layer Virtual Machine の作者達によって寄贈された。
  - BEA は Apache Harmony クラスライブラリが動作する JRockit VM の評価版が利用できることを発表していた\[10\]。

2006 年 11 月の時点でこれらの仮想マシンによる言語のサポートは完全ではなかったため、クラスライブラリのテスト\[[http://incubator.apache.org/harmony/quickhelp_contributors.html\]を実行するためのビルドの手順として](http://incubator.apache.org/harmony/quickhelp_contributors.html%5Dを実行するためのビルドの手順として) [IBM](../Page/IBM.md "wikilink") の [プロプライエタリ](../Page/プロプライエタリ・ソフトウェア.md "wikilink") の VM である J9 を使うよう推奨されていたが、2007年7月時点では J9 は不要となっていた。

DRLVM [仮想マシンの開発が積極的に進んでおり](../Page/仮想機械.md "wikilink")（2006年7月時点）、進展が期待できる状態にあった。

## 実行可能なアプリケーションの状況

構想の時点から、Harmony は重要な Java アプリケーション（[リンク参照](http://wiki.apache.org/harmony/Application_Status)）を実行する能力を着実に向上させてきた。2007年7月の時でたとえば下記のアプリケーションがサポートされていた。

  - [Eclipse](../Page/Eclipse_\(統合開発環境\).md "wikilink") : 36,000 件の[リファレンス実装](../Page/リファレンス実装.md "wikilink")テストのうち 99.3% が Harmony の DRLVM とクラスライブラリで合格[11](http://wiki.apache.org/harmony/Eclipse_Unit_Tests_Pass_on_DRLVM#PassRate_2007)。
  - [Apache Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink") : [リファレンス実装](../Page/リファレンス実装.md "wikilink") テストが 100% 合格[12](http://wiki.apache.org/harmony/Apache_Tomcat)。
  - [JUnit](../Page/JUnit.md "wikilink") : [リファレンス実装](../Page/リファレンス実装.md "wikilink") テストが 100% 合格[13](http://wiki.apache.org/harmony/JUnit)。
  - [Apache Ant](../Page/Apache_Ant.md "wikilink") : [リファレンス実装](../Page/リファレンス実装.md "wikilink") テストが 97% 合格[14](http://wiki.apache.org/harmony/Apache_Ant).
  - [Apache Derby](../Page/Apache_Derby.md "wikilink")、[Apache Axis](../Page/Apache_Axis.md "wikilink")、[Log4j](../Page/Log4j.md "wikilink")、[Apache Velocity](../Page/Apache_Velocity.md "wikilink")、[Apache Cocoon](../Page/Apache_Cocoon.md "wikilink")、[jEdit](https://ja.wikipedia.org/wiki/jEdit "wikilink")、[Apache Commons](../Page/Apache_Commons.md "wikilink") などのアプリケーションも高い合格率を示す。

しかし、Harmony のライブラリ実装が不完全であるため、実行できないアプリケーションもあった。

  - [ArgoUML](https://ja.wikipedia.org/wiki/:en:ArgoUML "wikilink"): Harmony では利用できない [Javaアプレット](../Page/Javaアプレット.md "wikilink") の実装を必要とする。
  - [Apache Geronimo](../Page/Apache_Geronimo.md "wikilink") は、若干の修正により（問題もあるが）Apache Harmony 上で動作する\[11\]。
  - [Azureus](https://ja.wikipedia.org/wiki/Azureus "wikilink") セキュリティのクラスが未実装である。

## 関連項目

  - [GNU Classpath](../Page/GNU_Classpath.md "wikilink")
  - [OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")
  - [Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")
  - [Dalvik仮想マシン](../Page/Dalvik仮想マシン.md "wikilink")

## 参照

## 外部リンク

  - [Apache Harmony Web Page](http://harmony.apache.org/)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:Java仮想マシン](https://ja.wikipedia.org/wiki/Category:Java仮想マシン "wikilink") [Category:Javaプラットフォームソフトウェア](https://ja.wikipedia.org/wiki/Category:Javaプラットフォームソフトウェア "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.  [Result - Move Apache Harmony to the Attic (updated) - Tim Ellison - org.apache.harmony.dev - MarkMail](http://markmail.org/message/sxjtefpayanbqfe5)
2.
3.  [Open Letter to Sun Microsystems](http://www.apache.org/jcp/sunopenletter.html)
4.
5.
6.
7.  [Class Library Component Status](http://harmony.apache.org/subcomponents/classlibrary/status.html)
8.  [Apache Harmony Library Coverage against J2SE 1.4](http://www.kaffe.org/~stuart/japi/htmlout/h-jdk14-harmony)
9.  [Apache Harmony Library Coverage against Java SE 5.0](http://www.kaffe.org/~stuart/japi/htmlout/h-jdk15-harmony)
10. BEA JRockit VM under a binary, evaluation-only license[10](http://dev2dev.bea.com/jrockit/jrockitVM/)
11. [Running Geronimo on Harmony](http://cwiki.apache.org/confluence/display/GMOxDOC20/Apache+Harmony)