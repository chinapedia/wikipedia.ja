> この記事は[Eclipse \(統合開発環境\)](https://ja.wikipedia.org/wiki/Eclipse_\(統合開発環境\))から翻訳されています。


**Eclipse**（、イクリプス）は[コンピュータプログラミングにおいて使用される統合開発環境](../Page/プログラミング.md "wikilink")（IDE）である\[1\]。ベースとなるワークスペースと、環境をカスタマイズするための拡張可能なプラグインシステムが含まれている。Eclipseは主に[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で書かれており、主にJavaアプリケーションの開発に使用されるが、[Ada](../Page/Ada.md "wikilink") 、[ABAP](../Page/ABAP.md "wikilink")、[C](../Page/C言語.md "wikilink") 、[C ++](../Page/C++.md "wikilink") 、[C＃](../Page/C_Sharp.md "wikilink") 、[Clojure](https://ja.wikipedia.org/wiki/Clojure "wikilink") 、[COBOL](../Page/COBOL.md "wikilink") 、[D](../Page/D言語.md "wikilink")、[Erlang](../Page/Erlang.md "wikilink")、[Fortran](../Page/FORTRAN.md "wikilink") 、[Groovy](../Page/Groovy.md "wikilink") 、[Haskell](../Page/Haskell.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[Julia](https://ja.wikipedia.org/wiki/Julia_\(プログラミング言語\) "wikilink")、\[2\] [Lasso](https://ja.wikipedia.org/wiki/投げ縄（プログラミング言語） "wikilink")、[Lua](../Page/Lua.md "wikilink")、[NATURAL](https://ja.wikipedia.org/wiki/ソフトウェアAG "wikilink")、[Perl](../Page/Perl.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Prolog](https://ja.wikipedia.org/wiki/Prolog "wikilink")、[Python](../Page/Python.md "wikilink")、[R](../Page/R言語.md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")（[Ruby on Railsフレームワークを含む](../Page/Ruby_on_Rails.md "wikilink")）、[Rust](https://ja.wikipedia.org/wiki/Rust_\(プログラミング言語\) "wikilink")、[Scala](../Page/Scala.md "wikilink")、[Scheme](../Page/Scheme.md "wikilink")などのプラグインを介して他のプログラミング言語のアプリケーションを開発するために使用することもできる。また，[LaTeX](../Page/LaTeX.md "wikilink")(TeXlipseプラグイン経由)やソフトウェア[Mathematica](../Page/Mathematica.md "wikilink")のパッケージを使ったドキュメントの開発にも利用できる。開発環境としては，JavaやScala用のEclipse Java開発ツール(JDT)，C/C++用のEclipse CDT，PHP用のEclipse PDTなどを含んでいる。

初期のコードベースはIBM [VisualAge](https://ja.wikipedia.org/wiki/VisualAge "wikilink")に由来している。Java開発ツールを含むEclipse[ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink")（SDK）は、Java開発者向けのものである。ユーザーは、他のプログラミング言語の開発ツールキットなど、Eclipseプラットフォーム用に書かれたプラグインをインストールすることで、その機能を拡張することができ、独自のプラグインモジュールを書いてコントリビュートすることができる。Eclipseのバージョン3で[OSGi](../Page/OSGi.md "wikilink")実装(Equinox)が導入されて以来、プラグインは動的に停止することができ、(OSGI)バンドルと呼ばれている。

Eclipse [ソフトウェア開発キット](../Page/ソフトウェア開発キット.md "wikilink") （SDK）は[フリーでオープンソースのソフトウェアであり](https://ja.wikipedia.org/wiki/FLOSS "wikilink")、 [Eclipse Public Licenseの条件に基づいてリリースされているが](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink")、 [GNU General Public Licenseとは互換性がない](../Page/GNU_General_Public_License.md "wikilink")。 \[3\] これは、[GNU Classpathで実行される最初のIDEの](../Page/GNU_Classpath.md "wikilink")1つであり、[IcedTea](https://ja.wikipedia.org/wiki/IcedTea "wikilink")で問題なく実行される。

## 歴史

Eclipseの歴史は1990年代後半から始まる。当時の状況は、[JBuilder](../Page/JBuilder.md "wikilink")、、そして[IBM](../Page/IBM.md "wikilink")の[VisualAge](https://ja.wikipedia.org/wiki/VisualAge "wikilink")、[PFU](../Page/PFU.md "wikilink")のteikadeなど第1世代のJava開発ツールが存在している。IBMは様々なプラットフォームの製品を抱えていることから、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")のマルチプラットフォームの可能性に注目していた。単なるVisualAgeの代替ではなく、IBMや他社のツールを統合するための共通プラットフォームの開発という基本構想の下、1998年11月にIBMカナダでプロジェクトが開始された。開発に携わったのは、VisualAgeの開発を行ったObject Technology International (OTI) 研究所である。

その後、IBMはこのプラットフォームに搭載するツールの開発のために組織の編成を行い、さらにオープンソース化することで新しい開発者の引き込みを図った。2001年11月、IBMはEclipseをオープンソース化するとともに、他の組織 ([ボーランド](../Page/ボーランド.md "wikilink")、[MERANT](https://ja.wikipedia.org/wiki/マイクロフォーカス "wikilink")、[QNX Software Systems](../Page/ブラックベリー_\(企業\).md "wikilink")、[ラショナル](../Page/ラショナル.md "wikilink")ソフトウェア、[レッドハット](../Page/レッドハット.md "wikilink")、[SuSE](../Page/SUSE.md "wikilink")、、) と共同で初期のEclipse.orgであるEclipse Board of Stewardsを設立する。公開されたEclipseはたちまちのうちに多くの開発者の興味を惹くこととなった。同年IBMはVisualAgeの後継製品として、EclipseをベースにWebSphere Studioを開発、リリースした。 また、2003年の終わりには、Eclipse Board of Stewardsの参加メンバーも80を越えている。

しかし爆発的人気の陰で、Eclipseは、IBM以外の他団体から新たなツールが提供されないという問題を抱えていた。それは、IBMがEclipseの制御権を握っているという認識によるものであった。IBM側にも「EclipseはWebSphere Studioの共通基盤であるWebSphere Studio Workbenchの一部を公開した物である」という認識が存在した。\[4\]Eclipseの勢いを止めないために、IBMとEclipseを切り離すことが必要とされた。2004年2月2日、Eclipse Board of Stewardsは、Eclipse組織の再構築を発表した。非営利組織[Eclipse Foundationの結成と](../Page/Eclipse_Foundation.md "wikilink")、Eclipseの全てをEclipse Foundationに移管することで、全ての団体や開発者を対等に扱うこととなった。このEclipse Foundationから、Eclipse 3.0、3.1、3.2がリリースされている。現在Eclipse Foundationは、115以上のメンバー企業、50以上のサブプロジェクトを抱えるオープンソース組織に成長している。

2006年、Eclipse Foundationは、Eclipse 3.2に10のオープンソースプロジェクトを合わせたリリースを行った。この製品は、Eclipse Callistoと呼ばれている。現在では毎年6月に同時リリース (Simultaneous Release)、その後9月と2月にそれぞれSR1とSR2 (Service Release) が行われている。同時リリースにはコードネームが付与されており、3.4までは[ガリレオ衛星](../Page/ガリレオ衛星.md "wikilink")に因んだ名が付けられていたが、3.5で予定されていた[Ioは](../Page/イオ_\(衛星\).md "wikilink")[I/Oと誤認されるおそれがあるため](../Page/入出力.md "wikilink")、ガリレオ衛星発見者の[ガリレオ・ガリレイ](../Page/ガリレオ・ガリレイ.md "wikilink")よりとった名称であるGalileoへと変更された。また、2010年リリースの3.6はHelios（ギリシア神話の太陽神である[ヘーリオス](../Page/ヘーリオス.md "wikilink")）と名付けられている。なお、Galileoからは頭文字がアルファベット順となるような名称が投票で選ばれている。

Eclipse 3.8は存在するが、3.7のバグフィクス版であること、すでに4.2のリリースが決まっていたことなどからWeb上では公表されていない。

Eclipse 4.9以降はコードネームが廃止になり、3か月ごとのリリースになった。

| バージョン | リリース日      | コードネーム   | 由来                                                                                                                                                                   |
| ----- | ---------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.0   | 2001/11/29 |          |                                                                                                                                                                      |
| 2.0   | 2002/06    |          |                                                                                                                                                                      |
| 2.1   | 2003/03    |          |                                                                                                                                                                      |
| 3.0   | 2004/06    |          |                                                                                                                                                                      |
| 3.1   | 2005/06    |          |                                                                                                                                                                      |
| 3.2   | 2006/06/30 | Callisto | 木星の第4衛星[カリスト](../Page/カリスト_\(衛星\).md "wikilink")。ガリレオ衛星の1つ。                                                                                                          |
| 3.3   | 2007/06/29 | Europa   | 木星の第2衛星[エウロパ](../Page/エウロパ_\(衛星\).md "wikilink")。ガリレオ衛星の1つ。                                                                                                          |
| 3.4   | 2008/06/25 | Ganymede | 木星の第3衛星[ガニメデ](../Page/ガニメデ_\(衛星\).md "wikilink")。ガリレオ衛星の1つ。                                                                                                          |
| 3.5   | 2009/06/24 | Galileo  | ガリレオ衛星の発見者[ガリレオ・ガリレイ](../Page/ガリレオ・ガリレイ.md "wikilink")。                                                                                                              |
| 3.6   | 2010/06/23 | Helios   | ギリシア神話の太陽神ヘーリオス。                                                                                                                                                     |
| 3.7   | 2011/06/22 | Indigo   | [ニュートンが](https://ja.wikipedia.org/wiki/アイザック・ニュートン "wikilink")[プリズム](../Page/プリズム.md "wikilink")によって光を7色に分解できることを発見したときに紫の内側の色に付けた名前。[藍色](../Page/藍色.md "wikilink")。 |
| 4.2   | 2012/06/27 | Juno     | ローマ神話に出てくる、女性と結婚を守護する女神[ユーノー](../Page/ユーノー.md "wikilink")。[ユーピテル](../Page/ユーピテル.md "wikilink") (Jupiter) の妻であり、6月を意味する"June"の由来。                                     |
| 4.3   | 2013/06/26 | Kepler   | 「[ケプラーの法則](../Page/ケプラーの法則.md "wikilink")」で有名なドイツの天文学者[ヨハネス・ケプラー](../Page/ヨハネス・ケプラー.md "wikilink")。                                                                  |
| 4.4   | 2014/06/25 | Luna     | [月](https://ja.wikipedia.org/wiki/月 "wikilink")を意味する。                                                                                                                |
| 4.5   | 2015/06/24 | Mars     | [火星](../Page/火星.md "wikilink")を意味する。                                                                                                                                 |
| 4.6   | 2016/06/22 | Neon     | 元素の一つ、[ネオン](../Page/ネオン.md "wikilink")を意味する。                                                                                                                         |
| 4.7   | 2017/06/28 | Oxygen   | 元素の一つ、[酸素](../Page/酸素.md "wikilink")を意味する。                                                                                                                           |
| 4.8   | 2018/06/27 | Photon   | [光子](../Page/光子.md "wikilink")を意味する。                                                                                                                                 |
| 4.9   | 2018/09/19 | 2018-09  | (コードネーム廃止)                                                                                                                                                           |
| 4.10  | 2018/12/19 | 2018-12  |                                                                                                                                                                      |
| 4.11  | 2019/03/20 | 2019-03  |                                                                                                                                                                      |
| 4.12  | 2019/06/19 | 2019-06  |                                                                                                                                                                      |
| 4.13  | 2019/09/18 | 2019-09  |                                                                                                                                                                      |
| 4.14  | 2019/12/18 | 2019-12  |                                                                                                                                                                      |
| 4.15  | 2020/03/18 | 2020-03  |                                                                                                                                                                      |

## Eclipseの機能

Eclipseの主な機能は以下のとおり。

### プラグイン

機能統合環境に[プラグイン](../Page/プラグイン.md "wikilink")としてさまざまな機能を組み込むことができるよう設計されている。その拡張性は非常に高く、Java開発環境自体が標準添付のプラグインとして実装されているほどであり、プラグイン次第で[C++](../Page/C++.md "wikilink")や[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[C\#](../Page/C_Sharp.md "wikilink")、[D言語](../Page/D言語.md "wikilink")、[TeX](../Page/TeX.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Ruby](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[COBOL](../Page/COBOL.md "wikilink")、[AspectJ](https://ja.wikipedia.org/wiki/AspectJ "wikilink")、[Mathematica](../Page/Mathematica.md "wikilink") など多様な言語への対応が可能となっている。

プラグインはJavaで記述され、プラグイン開発環境自体もEclipseに標準で付属している。これは、[Emacs](../Page/Emacs.md "wikilink")がその主要機能を搭載した[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")言語で記述できることと対比できる。LISPの代わりにJavaを用いるEmacsのようなものなのだと例えられることもある。

Eclipse 3.0より、プラグインの機構には[OSGi](../Page/OSGi.md "wikilink")フレームワークの実装であるEquinoxを採用している（Equinox自身もEclipse Foundationの傘下にあるサブプロジェクトである）。このため、EclipseプラグインはOSGiフレームワークに規定されているbundle形式で配布される。この機構はEclipse RCP (Rich Client Platform) においても同様である。

主なプラグインは後述する。

### デバッグ・ステップ実行

EclipseにはJava Debug Interface (JDI) を用いたグラフィカルデバッガが含まれている。

### バージョン管理システム連携

[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")の[CVSや](../Page/Concurrent_Versions_System.md "wikilink")[Subversion](../Page/Apache_Subversion.md "wikilink")、[Git](../Page/Git.md "wikilink")等を使ってソースコード管理を行うことができる。EclipseのCVS機能はコマンドラインのCVSコマンドを呼び出すフロントエンドとして動作するのではなく、自前のコードで直接CVSサーバと通信する（ssh、pserverの両方が利用可能）。

### JUnit連携

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")ソースコードから、[JUnit](../Page/JUnit.md "wikilink")テストコードの自動生成、テスト実行を行うことができる。Eclipse 3.2からは、[Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 5の[アノテーション](../Page/アノテーション.md "wikilink")に対応した[JUnit](../Page/JUnit.md "wikilink") 4を使うことが可能になった。

### Ant連携

ビルドシステム[Antと連携できる](../Page/Apache_Ant.md "wikilink")。Antは、[Unix系](../Page/Unix系.md "wikilink")のコマンド[make](https://ja.wikipedia.org/wiki/make "wikilink")を置き換えるプログラムで、[Makefile](https://ja.wikipedia.org/wiki/Makefile "wikilink")に相当する各ソースコードの依存関係を[XMLにより記述する](../Page/Extensible_Markup_Language.md "wikilink")。Antは、Javaで書かれており、ウェブサーバで知られる[Apache Software Foundationプロジェクトで開発されている](https://ja.wikipedia.org/wiki/Apache_Software_Foundation "wikilink")。EclipseはAntをデフォルトで同梱している。

### リファクタリング

getter, setterメソッドの自動生成や、try-catchの自動追加、による文字列の外部化、[クラス名](../Page/クラス_\(コンピュータ\).md "wikilink")・[メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")名・変数名の変更（それを参照している部分も自動的に書き換わる）、メソッドの移動や抽出などをウィザード形式で行ってくれる。

### コード編集支援

クラス名・メソッド名・変数名の補完や、自動整形、import文の整理・自動生成、必要なthrows節の自動追加、必要なメソッドスケルトンの自動生成などさまざまな編集支援機能を持つ。

### Eclipse Compiler for Java (ECJ)

JavaDevelopmentToolsに使用されているEclipse独自の[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")。 この為EclipseはJDKが無くてもJavaファイルのコンパイルが可能である。

## SWT

Eclipseは他のJavaで記述されたIDE（[JBuilder](../Page/JBuilder.md "wikilink")や[Sun ONE Studioなど](https://ja.wikipedia.org/wiki/Sun_ONE_Studio "wikilink")）と比べて動作があきらかに軽快である。この軽快さはGUIツールキットにJava標準の[Swing](../Page/Swing.md "wikilink")やAWT ([Abstract Window Toolkit](../Page/Abstract_Window_Toolkit.md "wikilink")) を使用せず、Eclipse独自のGUIツールキットであるSWT ([Standard Widget Toolkit](../Page/Standard_Widget_Toolkit.md "wikilink")) を採用していることで得られている。

SWTの位置づけはSwingではなくAWTに対応するが、AWTとSWTの違いは、AWTが[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) あるいはウィンドウシステムレベルの描画操作をネイティブメソッド群というレイヤ（つまり[Cあるいは](../Page/C言語.md "wikilink")[C++](../Page/C++.md "wikilink")で書かれた[JNIメソッドのDLL](../Page/Java_Native_Interface.md "wikilink")・共有ライブラリエントリ）で抽象化し、それをさらにJavaの[APIで覆い](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[インタフェースが二重に重ねられているのに比べ](../Page/インタフェース_\(情報技術\).md "wikilink")、SWTではネイティブのウィンドウシステムのAPIとJNIメソッドがほぼ一対一に対応するように定義されており、JNIの層が量的・質的に非常に薄い、ということである。

言い換えると、ネイティブのウィンドウシステムのAPIレイヤと、JavaのGUIツールキットクラスライブラリとしてのレイヤの間のセマンティックギャップを埋めるのに、AWTではCコードとJavaコードの両方を使用するのに対して、SWTではCの部分が僅少でありJavaコードが実質的に主体である。

AWTにおいて、下位層の[ウィンドウシステム](../Page/ウィンドウシステム.md "wikilink")のAPIをOSを越えて共通のものにみせかけるための、DLLのエントリとして定義されるインターフェース層は、積極的な存在意義が無く、見通しを悪くしており、2回の[セマンティクス](https://ja.wikipedia.org/wiki/セマンティクス "wikilink")変換が効率を悪くする可能性があり、柔軟性にかけ、拡張性に劣る。またJNIを使ったCコードというのは単なるCコードよりもはるかに可読性が悪く、[デバッグ](../Page/デバッグ.md "wikilink")も難しく、開発効率は極めて低い。

SWTではこのセマンティックギャップ吸収、つまりネイティブレベルの機能とJava APIの間の機能マッピングロジックが見通しよくJavaのみで記述されている。またSWTでは問題の切り分けも容易である（AWTではソースの無いDLL中のエラーは基本的にデバッグ不能。SWTでは生じた問題をネイティブAPIを呼び出す等価なCコードに書き換えることができ、問題の切り分けが容易）。

AWTとSWTのどちらが速いのかは実は良くわからないが、見た目や機能上の制約から現時点でAWTでアプリケーションを書くことはほぼありえない。したがって実用的な意味でSWTと速度比較すべきなのは[Swing](../Page/Swing.md "wikilink")であり、その比較においては明らかにSWTの方が軽快であるし、アプリケーションがそれを実証している。

''※注 [J2SE1.4登場前の話](../Page/Java_Platform,_Standard_Edition.md "wikilink")。ハードウェアアクセラレーションが施されるようになった1.4.1以降はVMの高速化とJNIが相対的にネックになってきたSWTより快適な場合もわりと多くなってきた。 ''

SWTはEclipseとは独立して、単独でJavaアプリケーションから利用することもできる。

### JFace

SWTの利用時において、生産性を上げるために、JFaceというクラスライブラリがある。[Model View Controllerのプログラミングスタイルを支援する](../Page/Model_View_Controller.md "wikilink")。SWTよりも、より抽象化されたデータの取り扱いを可能にする。JFace自体はPure Javaである。

誤解されやすいが、SWTに対するJFaceは、AWTに対するSwingとは大きく異なる。

## 主なプラグイン

  - WTP (Web Tools Platform)
    [Tomcat](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")、[Java EEなどのウェブ系開発に必要なものが一通りそろっているEclipse](../Page/Java_Platform,_Enterprise_Edition.md "wikilink").orgで開発されているプラグイン。
    [JavaScript](../Page/JavaScript.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[CSS](../Page/Cascading_Style_Sheets.md "wikilink")、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[JSPのエディタ](../Page/JavaServer_Pages.md "wikilink")、[データベース](../Page/データベース.md "wikilink")エクスプローラー、サーバエクスプローラーも内蔵。
    将来、Ajax開発環境も取り込まれる予定。Lombozプラグインが原型。
  - VE (Visual Editor)
    Eclipseで[AWT](../Page/Abstract_Window_Toolkit.md "wikilink")/[Swing](../Page/Swing.md "wikilink")/[SWT](https://ja.wikipedia.org/wiki/SWT "wikilink")のGUI開発ができるEclipse.orgから出ているプラグイン。開発は止まっている。
  - Tomcatプラグイン
    [Java Servlet](../Page/Java_Servlet.md "wikilink")・[JSPコンテナである](../Page/JavaServer_Pages.md "wikilink")[Tomcatと連携できる](https://ja.wikipedia.org/wiki/Apache_Tomcat "wikilink")。Sysdeoプラグイン、LombozプラグインなどによってもTomcatと連携することができる。
  - JBoss IDE
    Java J2EEアプリケーションサーバの[JBoss](../Page/JBoss.md "wikilink")との連携ができる。
  - UMLプラグイン
    [UMLの](../Page/統一モデリング言語.md "wikilink")[ユースケース図](https://ja.wikipedia.org/wiki/ユースケース図 "wikilink")、[クラス図](../Page/クラス図.md "wikilink")、[シーケンス図](https://ja.wikipedia.org/wiki/シーケンス図 "wikilink")、[コラボレーション図](https://ja.wikipedia.org/wiki/コラボレーション図 "wikilink")、[配置図](https://ja.wikipedia.org/wiki/配置図 "wikilink")などを編集、およびクラス図などからJavaコードの生成・双方向編集 ([MDA](../Page/MDA.md "wikilink"))、[リバースエンジニアリング](../Page/リバースエンジニアリング.md "wikilink")などを行うことができる。
    プラグインとしてはOmondo (EclipseUML) プラグインなどがある。
  - DoJaプラグイン
    [iアプリ](https://ja.wikipedia.org/wiki/iアプリ "wikilink")のプロジェクトの作成、ビルド、[エミュレータの起動を行うことができる](../Page/エミュレータ_\(コンピュータ\).md "wikilink")。
  - AJDT (AspectJ Development Tools) プラグイン
    [Java](https://ja.wikipedia.org/wiki/Java "wikilink")を[アスペクト指向プログラミング](../Page/アスペクト指向プログラミング.md "wikilink")言語として拡張した[AspectJ](https://ja.wikipedia.org/wiki/AspectJ "wikilink")によるプログラミングを行うことができる。
  - CDT (C/C++ Development Tooling)
    [C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")の開発をできるようにするプラグイン。
  - [DTP](../Page/DTP.md "wikilink") (Data Tools Platform)
    [関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) などによるデータ中心のアプリケーション開発をサポートするプラグイン。
  - TPTP (Test & Performance Tools Platform)
    テスト、モニタリング、トレーシング、プロファイリングなどを可能にするプラグイン。
  - [BIRT](https://ja.wikipedia.org/wiki/BIRT "wikilink") (Business Intelligence and Reporting Tools)
    レポート、帳票作成をサポートするプラグイン。
  - DSDP (Device Software Development Platform)
    [組み込み](https://ja.wikipedia.org/wiki/組み込み "wikilink")[デバイスソフトウェア](https://ja.wikipedia.org/wiki/デバイスソフトウェア "wikilink")開発を支援するプラグイン。
  - STP (SOA Tools Platform)
    [サービス指向アーキテクチャ](../Page/サービス指向アーキテクチャ.md "wikilink") (Service Oriented Architecture, SOA) 開発を支援するプラグイン。
  - [Checkstyleプラグイン](https://checkstyle.org/eclipse-cs/#!/)
    [コーディングスタイル](https://ja.wikipedia.org/wiki/コーディングスタイル "wikilink")をチェックする[Checkstyle](https://checkstyle.org/eclipse-cs/#!/)をEclipseで使うことができる。
  - FindBugsプラグイン
    [Java](https://ja.wikipedia.org/wiki/Java "wikilink")[ソースコード](../Page/ソースコード.md "wikilink")からバグパターンを検出するプラグイン。
  - [Papilioプラグイン](http://www.valtech.jp/papilio.htm)
    Eclipse上で[バグ管理システム](../Page/バグ管理システム.md "wikilink") (BTS) を実現したプラグイン。従来の代表的なBTS（BugzillaやScarabなど）と違い、WebサーバやDBサーバを構築する必要がない。
  - ByteCode Outline プラグイン
    [Java](https://ja.wikipedia.org/wiki/Java "wikilink")ソースコードを編集中にリアルタイムで、そのソースコードの[バイトコードを表示するプラグイン](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")。
  - m2eclipse
    Eclipseプロジェクトを[Maven 2のプロジェクトとしても使うことができ](../Page/Apache_Maven.md "wikilink")、マウスによるMavenの実行、Maven[リポジトリ](../Page/リポジトリ.md "wikilink")からライブラリの自動ダウンロード、自動インストールを可能にするプラグイン。
  - Maven Repo Search プラグイン
    Mavenのリポジトリを検索し、検索結果から表示されたライブラリリストからライブラリに合わせた<dependency>タグを生成し、[クリップボード](../Page/クリップボード.md "wikilink")に貼り付ける[プラグイン](../Page/プラグイン.md "wikilink")。
  - EPIC Perlプラグイン
    [Perl](../Page/Perl.md "wikilink")開発を可能にするプラグイン。
  - PHPプラグイン
    [PHP開発を可能にするプラグイン](../Page/PHP_\(プログラミング言語\).md "wikilink")。主なプラグインとしては、PDT (PHP Development Tools)、PHPEclipse、PHP-IDE、TruStudioなどがある。
  - RDT (Ruby Development Tools)
    [Ruby開発を可能にするプラグイン](https://ja.wikipedia.org/wiki/Ruby_\(代表的なトピック\) "wikilink")。
  - RadRails プラグイン
    [Ruby on Rails開発環境を提供するプラグイン](../Page/Ruby_on_Rails.md "wikilink")。
  - [PyDev](http://pydev.org/)
    [Python](../Page/Python.md "wikilink")開発を可能にするプラグイン。
  - Monalipse
    Eclipseで[2ちゃんねる](../Page/2ちゃんねる.md "wikilink")を閲覧できる[2ちゃんねるブラウザ](../Page/2ちゃんねるブラウザ.md "wikilink")プラグイン。
  - [EclipseFP](http://eclipsefp.sourceforge.net/)
    [Haskell](../Page/Haskell.md "wikilink")、[Objective Caml開発を可能にするプラグイン](https://ja.wikipedia.org/wiki/Objective_Caml "wikilink")。Objective Caml関連は、OCaml Development Toolsに引き継がれた（後述）。
  - [OCaml Development Tools (ODT)](http://ocamldt.free.fr/)
    Objective Caml開発を可能にするプラグイン。
  - ADT (Android Development Tools) プラグイン
    [Google](../Page/Google.md "wikilink")が開発した携帯電話用プラットフォームである[Android](../Page/Android.md "wikilink")用のプロジェクトの作成、ビルド、エミュレータの起動を行うためのプラグインであり、[Google](../Page/Google.md "wikilink")から公式IDEとして認定されていたが、2015年6月に、同年末で開発・サポートを終了することが発表され\[5\]、実際に開発・サポートが終了した。
  - Google Plugin for Eclipse
    [Google](../Page/Google.md "wikilink")が開発した[Google Web Toolkitと](https://ja.wikipedia.org/wiki/Google_Web_Toolkit "wikilink")[Google App Engineによるウェブアプリケーションのプロジェクト作成](https://ja.wikipedia.org/wiki/Google_App_Engine "wikilink")、ローカルサーバーでの実行、Googleのインフラストラクチャへのデプロイ、などを行う。
  - [Force.com IDE](https://developer.salesforce.com/page/JP_Force.com_IDE?useskin=dfcjskin)
    [セールスフォース・ドットコム](https://ja.wikipedia.org/wiki/セールスフォース・ドットコム "wikilink")の提供するクラウドプラットフォームのForce.com上で動作するForce.comアプリケーションの開発を可能にするプラグイン。2019年10月12日に廃止され、[Visual Studio Code用プラグイン](https://ja.wikipedia.org/wiki/Visual_Studio_Code "wikilink")[Salesforce Extensions for Visual Studio Code](https://developer.salesforce.com/tools/vscode/)へ置き換えられた。\[6\]
  - [Wolfram Workbench](https://www.wolfram.com/workbench/)
    [ウルフラム・リサーチ](../Page/ウルフラム・リサーチ.md "wikilink")社の提供する、[Mathematica](../Page/Mathematica.md "wikilink")開発環境を提供するプラグイン。有償。

<!-- end list -->

  - [GoClipse](http://goclipse.github.io/)
    [Go言語用のプラグイン](https://ja.wikipedia.org/wiki/Go_\(プログラミング言語\) "wikilink")。

## 日本語化

  - [Babel](http://www.eclipse.org/babel/)
    多言語化のためのEclipseのIncubationプロジェクト。

  - [Pleiades（Eclipse プラグイン日本語化プラグイン）](http://mergedoc.sourceforge.jp/)
    AOP により動的に日本語化するプラグイン。プラグイン単体の他、複数の有用なプラグインとEclipse本体を含めた「Pleiades All in One」も配布されている。

  - [Eclipse 日本語化言語パック（サードパーティ版）](http://sourceforge.jp/projects/blancofw/wiki/nlpack):以前は、IBMが無償で日本語パックを提供していたが、提供されなくなったためBlancoプロジェクトにより作成されている。翻訳内容は、Pleiadesの内容と同じ。

## Eclipseベースの製品

プラグインによる高い拡張性と、後述する[Eclipse Public License](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink") (EPL) が完全な[コピーレフト](../Page/コピーレフト.md "wikilink")ではなく再配布も認めている事から、生みの親であるIBMに限らず様々な企業、団体からEclipseをベースとした有償、無償の製品が公開されている。また、それらは[IDE](https://ja.wikipedia.org/wiki/IDE "wikilink")に限らない。

  - WebSphere Studio
    VisualAge の後継製品となるIBM [WebSphere](../Page/WebSphere.md "wikilink")ブランドの[統合開発環境](../Page/統合開発環境.md "wikilink")。Eclipseに有料プラグイン製品を組み合わせた製品であり、そういった観点では上記の有償プラグイン各種と変わらない。\[7\]Eclipse相当の共通基盤はWebSphere Studio Workbenchと呼ぶ。現在は営業活動が終了し、Rational Application Developerに置換されている。

  -
    WebSphere Studioの後継製品。IBM [Rational](https://ja.wikipedia.org/wiki/Rational "wikilink")ブランドの[統合開発環境](../Page/統合開発環境.md "wikilink")。

  - [HCL Notes](../Page/IBM_Notes.md "wikilink")
    [ロータス](../Page/ロータス.md "wikilink")→[IBM](../Page/IBM.md "wikilink")→へと事業売却された[グループウェア](../Page/グループウェア.md "wikilink")用[ミドルウェア](../Page/ミドルウェア.md "wikilink")製品。旧称 IBM Lotus Notes。IBM Lotus Notes/Domino 8以降、従来のWindowsアプリケーションであるNotes Basicと、Eclipse RCP ベースのLotus Expeditor 上に構築するNotes Standard Editionの2種が同梱されるようになった。

  -

    製の[統合開発環境](../Page/統合開発環境.md "wikilink")。

  - [JBuilder](../Page/JBuilder.md "wikilink")
    [ボーランド](../Page/ボーランド.md "wikilink")→[エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")製の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")。IBMのVisualAgeと競合していたが、JBuilder 2007 以降は、Eclipseベースになっている。

  - [Adobe Flash Builder](https://ja.wikipedia.org/wiki/Adobe_Flash_Builder "wikilink")
    Adobe製の[Apache Flex用](../Page/Apache_Flex.md "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")。

  - e² studio
    [ルネサスエレクトロニクス](../Page/ルネサスエレクトロニクス.md "wikilink")製のルネサスマイコン用[統合開発環境](../Page/統合開発環境.md "wikilink")。

  - [Aptana](../Page/Aptana.md "wikilink")
    EclipseベースのWebオーサリングツール。

## ライセンス

[Eclipse Public License](https://ja.wikipedia.org/wiki/Eclipse_Public_License "wikilink") (EPL) が適用される[1](http://www.eclipse.org/org/documents/epl-v10.php)。EPLは、OSIオープンソース・コンソーシアムからオープンソースの認定を受けている。EPLは[Common Public License](../Page/Common_Public_License.md "wikilink") (CPL) から派生したライセンスである。

## 出典

## 外部リンク

  - [Eclipse公式サイト](https://www.eclipse.org/)

[Category:Eclipse](https://ja.wikipedia.org/wiki/Category:Eclipse "wikilink") [Category:Java開発ツール](https://ja.wikipedia.org/wiki/Category:Java開発ツール "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Eclipse_Foundation](https://ja.wikipedia.org/wiki/Category:Eclipse_Foundation "wikilink") [Category:フリーUMLツール](https://ja.wikipedia.org/wiki/Category:フリーUMLツール "wikilink")

1.
2.
3.
4.
5.
6.   Force.com IDE Developer Guide (Retired) {{\!}} Salesforce Developers|accessdate=2019-11-17|publisher=Salesforce|website=Salesforce Developers}}
7.   日経 xTECH（クロステック）|accessdate=2019-11-17|publisher=Nikkei Business Publications, Inc.|author=星 暁雄＝日経BP Javaプロジェクト|website=日経 xTECH（クロステック）|date=2003-10-31}}