> この記事は[Javaに対する批判](https://ja.wikipedia.org/wiki/Javaに対する批判)から翻訳されています。


**Javaに対する批判**（ジャバにたいするひはん）では、プログラミング言語[Java](https://ja.wikipedia.org/wiki/Java "wikilink")と、その主たる実装であるJDKやその他の実装に関する批判、およびJavaプラットフォームの性能に対する批判について説明する。Javaプラットフォームの性能に関する、批判以外の内容については「[Javaの性能](https://ja.wikipedia.org/wiki/Javaの性能 "wikilink")」を参照のこと。

Javaは優れた技術だと評価する人々がいる一方で批判も少なくない。Javaは[ソフトウェア](../Page/ソフトウェア.md "wikilink")に関する複雑さを管理する問題に対して革新的な方法を提供するという目標のもとで開発された（ないし、そのように信じられている\[1\]）。多くの人々は、Java技術はこの期待に対して満足できる答えを提供したと評価している。

しかしJavaにも欠点が無いわけではないし、どのようなプログラミング作法にも適応しているというわけでもない。また、どのような環境や要件にも普遍的に適応しているというわけでもない。

ソースコードレベルでのプログラミングパラダイムの追加や記述性の改善を求めて、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM) 上で動作する[Scala](../Page/Scala.md "wikilink")や[Kotlin](https://ja.wikipedia.org/wiki/Kotlin "wikilink")といった後発言語も出現しているが、JVMベースの互換言語であるがゆえに、JVMに存在する制約もまた残されている。

## クラスパス

Java[プログラムを実行する際](../Page/プログラム_\(コンピュータ\).md "wikilink")、すべての[サードパーティー](../Page/サードパーティー.md "wikilink")の[ライブラリ](../Page/ライブラリ.md "wikilink")は[クラスパス](https://ja.wikipedia.org/wiki/クラスパス "wikilink")に存在する必要がある。これは[移植性](../Page/移植性.md "wikilink")の障壁となる。なぜならばクラスパスの文法は[プラットフォームに依存するからである](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。例えば[Windowsベースのシステムはサブディレクトリを区切るために](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[バックスラッシュ](../Page/バックスラッシュ.md "wikilink") "" を使用し、パス区切りに[セミコロン](../Page/セミコロン.md "wikilink") ";" を使用している\[2\]。だが一方、他の多くのプラットフォームではサブディレクトリ区切りに[スラッシュ](../Page/スラッシュ_\(記号\).md "wikilink") "/" を使用し、パス区切りに[コロン](../Page/コロン_\(記号\).md "wikilink") ":" を使用している\[3\]。

各々の[.jarや](../Page/JAR_\(ファイルフォーマット\).md "wikilink")[.zip](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")[アーカイブはクラスパスにおいて明示的に名前がつけられる必要がある](../Page/アーカイブ_\(コンピュータ\).md "wikilink")。この抜け道としてアスタリスク(\*)で終わるクラスパスを指定することで、そのディレクトリにある.jarや.JARで終わるすべてのファイル名にマッチさせることができる。しかしながら、.zipや.classファイルのようなものはマッチしない\[4\]\[5\]。

### 解決策・代替策

これらのクラスパス問題は[環境変数](../Page/環境変数.md "wikilink")CLASSPATHを使用せず、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が推奨する-classpathオプションを使用することで解決する。開発時は、-classpathオプションは[バッチファイル](../Page/バッチファイル.md "wikilink")や[make](https://ja.wikipedia.org/wiki/make "wikilink")や [Apache Ant](../Page/Apache_Ant.md "wikilink") や[統合開発環境](../Page/統合開発環境.md "wikilink")を使うことで便利に指定することができる。[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")を利用する実行エンドユーザに対しては、開発者が[マニフェストファイル](https://ja.wikipedia.org/wiki/マニフェストファイル "wikilink")にクラスパスを記述するか、FatJarやOneJar\[6\]という、複数のjarファイルを一つにまとめるツールを使うことで解決できる。

## ライセンス

[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")（サン）のJavaの財産的価値はフリーソフトウェアコミュニティで議論を呼んだ。なぜならばサンのJavaの実装は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")ではなかったため、フリーソフトウェアや主に[Debian](../Page/Debian.md "wikilink")や[$100ラップトップ](https://ja.wikipedia.org/wiki/The_Children's_Machine "wikilink")、[Fedora Coreのような](https://ja.wikipedia.org/wiki/Fedora_Core "wikilink")[GPL互換](../Page/GNU_General_Public_License.md "wikilink")[ライセンス](../Page/ライセンス.md "wikilink")が要求されるプロジェクトにはサンのJavaを含めることはできなかった\[7\]\[8\]。

サンは [JavaOne](https://ja.wikipedia.org/wiki/JavaOne "wikilink") 2006 で、Javaは[オープンソースソフトウェア](../Page/オープンソースソフトウェア.md "wikilink")になるだろうと公表した。この声明はSun Softwareの上級副社長Rich Greenによって公表された。「オープンソースソフトウェアにするか否かという問題はない。どのような方法でオープンソースにするかが問題である。つまり我々はこれを実行する。」\[9\]\[10\]\[11\]

[2006年](../Page/2006年.md "wikilink")[7月](https://ja.wikipedia.org/wiki/7月 "wikilink")には、サンの[最高技術責任者](../Page/最高技術責任者.md "wikilink")Robert BrewinはJavaは[2007年](../Page/2007年.md "wikilink")[6月](../Page/6月.md "wikilink")に部分的にオープンソースになるが、全体のプラットフォームが完全なオープンソースになるには時間がかかるだろうとコメントしている\[12\]。

[2006年](../Page/2006年.md "wikilink")[11月13日](../Page/11月13日.md "wikilink")、サンは標準版Java実行環境は2007年3月に[GPLの下でリリースされる予定であることを公表した](../Page/GNU_General_Public_License.md "wikilink")\[13\]。Java実行環境のソースコードは[GPLの下で利用可能になる予定である](../Page/GNU_General_Public_License.md "wikilink")。[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")によると、これは[Javaの罠](http://www.gnu.org/philosophy/java-trap.html)の終焉を意味するとのことである。[マーク・シャトルワース](../Page/マーク・シャトルワース.md "wikilink")はJavaのオープンソース化についての最初のSunによる発表を「[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")コミュニティにとっての確かなマイルストーン」と評価した\[14\]\[15\]。

### 解決策・代替案

Javaのライセンスの問題は徐々に解決されつつある。時間が解決していると言える面もあるといえる。今後も新たなライセンスの問題に直面しそうであれば、[Java Community Process](../Page/Java_Community_Process.md "wikilink") に提案するよう働きかけてみるという手段もある。[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")や [Eclipse Foundation](../Page/Eclipse_Foundation.md "wikilink") など他のオープンソースコミュニティの助けを借りることで問題を解決に向けて進めることができる可能性がある。

## リソース管理

Javaはメモリを管理するが、他のリソース（ファイルや[JDBC](../Page/JDBC.md "wikilink")[データベース](../Page/データベース.md "wikilink")接続など）は管理しない。これらは[C言語](../Page/C言語.md "wikilink")および[C++](../Page/C++.md "wikilink")でヒープに動的確保した[メモリを明示的に解放する必要があったのと同様](../Page/記憶装置.md "wikilink")、[プログラマ](../Page/プログラマ.md "wikilink")によって解放されなければならない。

### メモリ管理

Javaは[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")による[メモリ管理](../Page/メモリ管理.md "wikilink")機能を備える。これによって、完全ではないもののプログラマが[メモリリーク](../Page/メモリリーク.md "wikilink")を起こすようなプログラムを作ってしまう危険性を減らした。Javaでは[オブジェクトは常に](../Page/オブジェクト_\(プログラミング\).md "wikilink")[ヒープ領域](../Page/ヒープ領域.md "wikilink")に（[JITコンパイラによって最適化されて](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")[スタックや](https://ja.wikipedia.org/wiki/コールスタック "wikilink")[レジスタに割り当てられない限り](../Page/レジスタ_\(コンピュータ\).md "wikilink")）確保される。[ローカル変数](../Page/ローカル変数.md "wikilink")は[スタックや](https://ja.wikipedia.org/wiki/コールスタック "wikilink")[レジスタに確保される](../Page/レジスタ_\(コンピュータ\).md "wikilink")。C++ではオブジェクトをヒープ領域に割り当てるかスタック領域に割り当てるかをプログラマが選択することができたが、Javaではそれが不可能になっている。

オブジェクトはガベージコレクションによって管理されるが、Javaはプログラマにガベージコレクションがいつ起こるかを保証しない。プログラマはガベージコレクションを阻止することができないし、たとえを用いても任意のオブジェクトを任意のタイミングで解放することはできない\[16\]\[17\]。これはプログラミングを簡易にしメモリリークの可能性を軽減するが、決定論的でより効果的なメモリ処理を行うための柔軟性が犠牲になっている。[C言語](../Page/C言語.md "wikilink")や[アセンブリ言語](../Page/アセンブリ言語.md "wikilink")のような低水準言語はこの柔軟性を提供する。

C++などで書かれた多くのプログラムはメモリリークの犠牲になりがちだが、問題はメモリリークだけではない。[ファイルハンドルやデータベース](../Page/ファイル記述子.md "wikilink")、ネットワーク接続のような他のリソースのリークは特に[例外が投げられたときに常に起こりうる](../Page/例外処理.md "wikilink")。C++では[RAII](../Page/RAII.md "wikilink")と呼ばれる[イディオムによっていずれの問題も克服することができるが](https://ja.wikipedia.org/wiki/イディオム#コンピュータサイエンス "wikilink")、Javaプログラマは忘れずに`finally`節でリソースを解放する必要があり、Javaが何を解放するかということとプログラマは何を解放しなければならないのかということをきちんと理解する必要がある。

### 解決策・代替案

この問題は、メモリを増設する、最大ヒープメモリサイズを拡大するなどで解決できるケースもある。[弱い参照](../Page/弱い参照.md "wikilink") (//) を用いることで多少の解決策になることはある。だが、[JREや](../Page/Java_Runtime_Environment.md "wikilink")[JDKのバージョンが特定の古いものであることが要因となっていることもある](../Page/Java_Development_Kit.md "wikilink") 。最新版のJREやJDKで実行、開発すれば問題発生率を下げることもできる。

`finally`節の問題は、場合によっては、[ライブラリ](../Page/ライブラリ.md "wikilink")や[フレームワークによって解決できることもある](../Page/アプリケーションフレームワーク.md "wikilink")。[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")[入出力](../Page/入出力.md "wikilink")の場合は[Apache Commons](../Page/Apache_Commons.md "wikilink") IOを、[データベース](../Page/データベース.md "wikilink")接続の場合はApache Commons DBUtils、[Hibernate](../Page/Hibernate.md "wikilink")やApache Cayenneなどの[オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")フレームワークを用いることで`finally`節のことをあまり多く気にしなくても良いようにする手段がある。Java 7ではtry-with-resources文でこの問題に対処している（例外安全の確保）。

## 言語選択

### プリミティブ対オブジェクト / オートボクシング

Javaの設計者らは、現在他の言語にあるいくつかの機能（[多重継承](https://ja.wikipedia.org/wiki/多重継承 "wikilink")、[演算子](../Page/演算子.md "wikilink")[多重定義](../Page/多重定義.md "wikilink")、[タプルなど](https://ja.wikipedia.org/wiki/タプル#計算機科学での使用 "wikilink")）を実装しないことを決めた。

[総称型](https://ja.wikipedia.org/wiki/総称型 "wikilink")（[ジェネリクス](../Page/ジェネリックプログラミング.md "wikilink")）がJava 5.0に導入されたとき、すでにJavaには[クラスの大規模な枠組みがあった](../Page/クラス_\(コンピュータ\).md "wikilink")（それらの多くはすでに非推奨となっていた）、そして[後方互換](https://ja.wikipedia.org/wiki/後方互換 "wikilink")性を保つため、総称型の実装方法として既存のクラスを維持することを可能にする（[コンパイル時の](../Page/コンパイラ.md "wikilink")）[型消去](https://ja.wikipedia.org/wiki/型消去 "wikilink")（型削除、type erasure）が選ばれた。これは、他の言語と比べると、総称型の導入によって提供される機能を限定してしまう結果になった\[18\]\[19\]。

Javaの[プリミティブ型](../Page/プリミティブ型.md "wikilink")はオブジェクトではない。プリミティブ型は値への参照ではなく値そのものを[スタック領域に保持している](https://ja.wikipedia.org/wiki/コールスタック "wikilink")。この設計選択はパフォーマンス上の理由により行われた。このためJavaは純粋な[オブジェクト指向言語と見なされていない](../Page/オブジェクト指向プログラミング.md "wikilink")。またこのことにより[リフレクションがより複雑になっている](../Page/リフレクション_\(情報工学\).md "wikilink")。配列を除き、Javaのコレクションクラスは[プリミティブ型](../Page/プリミティブ型.md "wikilink")を直接扱うことができず、[プリミティブラッパークラス](../Page/プリミティブラッパークラス.md "wikilink")への[ボックス化](../Page/ボックス化.md "wikilink")が必要となる。この制約はジェネリクスにおいても変わりない。Javaのジェネリクスは型安全性が担保されるだけであり、ジェネリクスを使わない場合と比べてパフォーマンス上のメリットはない。

また、Java 5.0は、コンパイル中に要求された場合にプリミティブ型を対応する[プリミティブラッパークラス](../Page/プリミティブラッパークラス.md "wikilink")のオブジェクトに自動変換する機能（[オートボクシング](https://ja.wikipedia.org/wiki/オートボクシング "wikilink")）をサポートしているが、オートボクシングでは[NullPointerException](../Page/NullPointerException.md "wikilink")が投げられる可能性がある。オートボクシングは暗黙のうちに起こる（[キャストや](../Page/型変換.md "wikilink")[メソッド呼び出しを伴わない](../Page/メソッド_\(計算機科学\).md "wikilink")）ため、このNullPointerExceptionという非チェック[例外はJavaプログラムのコードに目を通しただけでは明確にはならない恐れがある](../Page/例外処理.md "wikilink")。

### 非virtualメソッド

Javaはメソッドを非virtualにする手段を提供しない（[オーバーライド](../Page/オーバーライド.md "wikilink")を禁止するために`final`修飾子を使用することで封印することはできる）。これは[派生クラスに](../Page/サブクラス_\(計算機科学\).md "wikilink")、同じ名前の関係の無いメソッドを定義させる方法がないことを意味する。これは[基底クラスが別の人間によって設計されるときに問題となることがあり](../Page/スーパークラス_\(計算機科学\).md "wikilink")、また、新しいバージョンが、派生クラスで同じ名前のメソッドがすでに存在するときに、同じ名前とシグネチャのメソッドを導入することで問題となることがある。これは、どちらのクラスの設計者の意図にも反して、派生クラスのメソッドが基底クラスのメソッドを暗黙のうちにオーバーライドするであろうことを意味する。これらのバージョン問題にある程度適合するためにJava 5.0は[アノテーション](../Page/アノテーション.md "wikilink")を導入しているが、後方互換性を保つには、それをデフォルトでは強制できない。

### 単一パラダイム

Javaは主にオブジェクト指向の単一[パラダイム言語である](../Page/プログラミングパラダイム.md "wikilink")。すべてのデータと処理は必ず何らかのクラス内に記述しなければならないため、必要以上にコードが冗長になってしまうことがある。Java 5.0で追加された静的インポート (*static imports*) はこれまでのJavaよりも手続きパラダイムによりよく順応する。

### 例外処理

Javaでは[C++](../Page/C++.md "wikilink")でオプションとされていた[例外処理](../Page/例外処理.md "wikilink")の仕様を取り込んだが、この際チェック対象の例外に対応するthrows文を必須とした。例外のチェックは小規模なシステムにとっては役立つが、大規模なシステムについても有益であるかどうかについては統一的な見解には至っていない。特に上位のコードでは下位のコードから発生するエラーを意識したくない（例としては、[名前解決](https://ja.wikipedia.org/wiki/名前解決 "wikilink")例外である）。名前クラスの作成者は名前解決例外をチェック対象の例外として上位コードに対応を強制するか、コンパイル時のチェックを使わずに下位のコードからの例外を連鎖的に通知するかを選択する必要がある\[20\]。

### クロージャ

Javaでは、内部クラス、ローカルクラス、匿名クラスを使用することで、基本的な[クロージャ](../Page/クロージャ.md "wikilink")に近い記述が実現できる。しかしこれは完全ではなく、ローカルクラス／匿名クラス外の変数に対する参照を、ローカルクラス／匿名クラスのフィールドとして暗黙キャプチャできるように、final修飾子付きで宣言する必要がある。これは、変数のスコープを抜けたときに削除できるような、様々な寿命に対応したスタックモデルをJVM実装者が選択できるようにするためである。Java 8では実質的にfinalとみなせる変数は明示的にfinal修飾する必要がなくなったが、依然として再代入は許可されない。

また匿名クラスの構文も冗長であり、例えば[インタフェースを要求する場面で](../Page/インタフェース_\(情報技術\).md "wikilink")、同インタフェースを実装する匿名クラスを定義する場合、単純なコードブロックとして定義することはできず、`Runnable.run()`メソッドを実装するようなクラスのブロックを定義する必要がある。Java 8では[ラムダ式](https://ja.wikipedia.org/wiki/ラムダ式 "wikilink")と関数型インタフェースによりこの問題を改善している。

### メソッド参照

Java 7以前にはC/C++の[関数ポインタ](https://ja.wikipedia.org/wiki/関数ポインタ "wikilink")や[C\#の](../Page/C_Sharp.md "wikilink")[デリゲートに相当するメソッド参照の機能がなく](../Page/デリゲート_\(プログラミング\).md "wikilink")、[インタフェースで代用するしかなかった](../Page/インタフェース_\(情報技術\).md "wikilink")。Java 8ではメソッド参照が追加された。

## 浮動小数点演算

Javaの[浮動小数点演算は主に](../Page/浮動小数点数.md "wikilink")[IEEE 754](../Page/IEEE_754.md "wikilink")（二進化浮動小数点数演算標準）をベースとしているが、例えばIEEE 754に必須とされる例外フラグや方向指定の丸めなどの、いくつかの機能については"strictfp"修飾子を指定した場合でもサポートされない。Javaの仕様として知られているものはJava自体の問題ではないが、浮動小数点数演算を行う上で避けて通れない問題である\[21\]\[22\]。

## ルックアンドフィール

Java用の[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")な[ウィジェットツールキット](https://ja.wikipedia.org/wiki/ウィジェットツールキット "wikilink")のひとつに[Swing](../Page/Swing.md "wikilink")がある。Swingを使って書かれたアプリケーションの[グラフィカルユーザインタフェース](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink") (GUI) の[ルック・アンド・フィール](../Page/ルック・アンド・フィール.md "wikilink")（look and feel、直訳すると「外観と操作感」）は大抵、各プラットフォームネイティブのアプリケーションのものと異なる。プログラマはネイティブの[ウィジェットを表示する](../Page/ウィジェット_\(GUI\).md "wikilink")[AWT](../Page/Abstract_Window_Toolkit.md "wikilink")（ネイティブであるため[OSのプラットフォームと同じ見た目を提供する](../Page/オペレーティングシステム.md "wikilink")）を使うことを選択することができる。しかしAWTツールキットは、高度なウィジェットのラッピングを必要とし、かつ様々なサポートされたプラットフォームで移植性を犠牲にしない高度なGUIプログラミングには向いていない。そして、SwingとAWTにはとりわけ高水準ウィジェットにおいてAPIが大きく異なる。

Swingツールキットは全てJavaで実装されている。Swingツールキットはネイティブアプリケーションとは異なるルックアンドフィールを持つという問題がある。一方でSwingツールキットのウィジェットはネイティブなツールキットの機能に限定されないという利点がある。この利点は全てのプラットフォームで利用できることが保証される最も基本的な描画機構を使ってウィジェットを再実装していることによる。不幸にも、（2006年8月の時点で）[Java実行環境](../Page/Java_Runtime_Environment.md "wikilink") (JRE) のデフォルトのインストールでは、Swingデフォルトの埋め込みMetal (メタル) ルックアンドフィールの代わりに、システムの「ネイティブ」なルックアンドフィールを使わなかった。プログラマがを使ってシステムネイティブなルックアンドフィールを設定しなかった場合、ユーザーは外観がネイティブアプリケーションのそれとは非常に異なるアプリケーションに遭遇するだろう。 [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")の配布元に限って含まれる[アップル自身のJava実行環境の最適化バージョンは](../Page/アップル_\(企業\).md "wikilink")、デフォルトで「デフォルト」をセットし、"[Aqua](../Page/Aqua_\(コンピュータ\).md "wikilink")" のルックアンドフィールを実装し、[Macintosh](../Page/Macintosh.md "wikilink")上のSwingアプリケーションは、ネイティブなソフトウェアに似た外観を提供している。macOSの環境でさえ、プログラマはそのアプリケーションがAquaのように見えることを確実とするために、若干の余分の作業をまだしなければならない（例えば、メニューバーを[Windowsのように各アプリケーションウィンドウ内部に表示するのではなく](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、macOSのメニューバー内部に表示させるために、システムプロパティをセットする必要がある）。

### 解決策・代替案

この問題は、開発者がJavaのバージョンを [Java SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 6以降にアップグレードすることで解決する。Java SE 6になってからJavaのデスクトップまわり、GUI環境は一新され、開発効率は高まっているため、以前のバージョンよりも開発の手間はかからなくなっている。

## パフォーマンス

### 一般

Javaプログラムのパフォーマンスに関して一般論を述べることは不可能である。なぜなら、実行時の性能は、言語自身が持つ固有の特性よりも、[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")や[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")の品質に非常に大きく影響されるからである。[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")の実行方法は、[仮想マシンによって実行時に翻訳して実行する方法と](../Page/仮想機械.md "wikilink")、ロード時もしくは実行時に機械語にコンパイルしてハードウェアによって直接的に実行する方法がある。前者の翻訳実行する方法は機械語の実行よりも遅く、後者のロード時もしくは実行時にコンパイルして実行する方法は、最初のコンパイル時にパフォーマンスが犠牲になる。これはJavaにかぎらず、[.NET Frameworkなど他の仮想マシンベースのプログラミング環境においても同様である](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。

コンピュータハードウェア性能の向上と、Javaのバージョンアップに伴う最適化技術の進歩によって、Javaプログラムの初回起動時のオーバーヘッドなどは誤差の範囲内になりつつあるが、[ヴィルトの法則](../Page/ヴィルトの法則.md "wikilink")が示すように、総じてソフトウェアの複雑化やシステム要求の上昇にハードウェアの性能向上が追い付いていないのが現状である。C/C++ではJavaよりも細やかな最適化を手動で施すことができるが、プログラマが手作業で施した最適化よりも、JITコンパイルによる自動最適化のほうが性能面で上回るケースもすでに存在する。C/C++でJavaの実行時最適化技術を真似することは困難である。

#### 言語仕様による制約

Javaだけに限ったことではないが、パフォーマンス上の障壁となる言語仕様や言語仕様の欠落がいくつか存在する。それは例えば配列境界チェックや実行時型チェック、非仮想メソッドの欠如などである。ただしコードの安全性と性能はトレードオフの関係にあるため、チェック機構が一概に悪とは言えない。また、コンパイル時の最適化やJVMの実装次第で解消できるものもある。そのほか、Javaは[構造体](../Page/構造体.md "wikilink")（ユーザー定義の値型）および矩形配列（真の多次元配列）を持たず、それぞれクラス（参照型）およびジャグ配列（配列の配列）などで代替する必要がある。また、Javaではメソッドから複数の値を返すためにはクラスや配列といった参照型を使用する以外の方法がない。これらの制約によってJavaのプログラムコードは、他の言語で書かれたコードよりも頻繁にヒープを使用しなければならなくなっている。

### ガベージコレクション

不要オブジェクトの自動回収を行う[ガベージコレクション](../Page/ガベージコレクション.md "wikilink")は明示的なメモリ解放に比べそのオーバーヘッドは大きいが、ガベージコレクタの実装やアプリケーションでのオブジェクトの利用状況によってその影響はまちまちに変化する。多くのJava仮想マシンは[世代別ガベージコレクション](../Page/世代別ガベージコレクション.md "wikilink")の採用によって動的メモリ管理を高速化しているため、多くのアプリケーションでは高い性能を示している。

### バイトコード対ネイティブコンパイル

一般に、プログラミング言語とその実行方法は、直交するのが普通で、コンパイラだったり、インタプリタだったり、バイトコード方式だったりする実装があっても構わないはずである。しかし、Javaには、実装上制限があり、あまりに自由度がない。

[ジャストインタイムコンパイル](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")（JITコンパイル）とネイティブコンパイルの性能差はほとんど無いとされるが、よく議論の種にもなる。JITコンパイルには時間が掛かるため、短時間で起動終了することが求められるアプリケーションや、起動と終了を頻繁に繰り返すアプリケーション、またプログラム内容が巨大なアプリケーションでは問題となる。しかし、一旦[ネイティブコードに変換すれば](../Page/機械語.md "wikilink")[数値計算](https://ja.wikipedia.org/wiki/数値計算 "wikilink")においてもネイティブコンパイルと同等の性能を示す。

Javaはメソッド呼び出しの明示的な[インライン化をサポートしないものの](../Page/インライン関数.md "wikilink")、多くのJITコンパイラではバイトコード読み込み時に[インライン展開](../Page/インライン展開.md "wikilink")を行い、また実行時の[プロファイリングを利用してその効率をより高めている](../Page/性能解析.md "wikilink")。[HotSpot](../Page/HotSpot.md "wikilink")仮想マシンが採用している動的再コンパイルでは、実行時でしか取得できない情報を利用することで、多くのプログラミング言語が採用する静的コンパイル方式を超える性能を得る場合もある。

## ハードウェアインタフェース

Javaはセキュリティと移植性を重視して設計されたので、Javaではマシンアーキテクチャとアドレス空間への直接アクセスをサポートしていない。[スキャナ](../Page/スキャナ.md "wikilink")（[デジタルカメラ](../Page/デジタルカメラ.md "wikilink")、オーディオレコーダ、[ビデオキャプチャ](../Page/キャプチャ_\(録画ソフト\).md "wikilink")）ないし実質的に直接メモリ空間の制御（一般的に、ドライバインストールを必要とするハードウェアやそれらの部品）を必要とする特定の一部のハードウェアを動かすことはJavaでは容易に実現できないことを意味する。この問題の実例はJavaのバージョン1.0で見られた。様々なプリンタドライバへのインタフェースコードがこの初期のJava実行環境に含まれず、[プリンタへのアクセスが可能でなかった](https://ja.wikipedia.org/wiki/プリンター "wikilink")。

### ネイティブコードとインタフェース

ハードウェアに直にアクセスする[クライアントサイド](../Page/クライアントサイド.md "wikilink")または[サーバ](../Page/サーバ.md "wikilink")システムは、ネイティブコードとJavaライブラリを橋渡しする[Java Native Interface](../Page/Java_Native_Interface.md "wikilink") (JNI) を使って、C/C++およびアセンブリ言語とJavaを組み合わせる方法を取る。また、ハードウェアアクセスを担うネイティブコードとJavaとの通信をファイルやデータベース、[共有メモリ](../Page/共有メモリ.md "wikilink")やソケットを介して行う方法もあるが、理想的なやり方ではない。

JNIを使うことで、プラットフォーム依存性、潜在的な[デッドロック](../Page/デッドロック.md "wikilink")、[メモリリーク](../Page/メモリリーク.md "wikilink")、場合によっては性能の著しい劣化などの問題が発生しうる。また、2つの異なるコードベースをメンテナンスするために必要となるコードの[複雑性](https://ja.wikipedia.org/wiki/複雑性 "wikilink")は、言うまでもない。しかし、それは、例えば[.NET Frameworkの](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[共通言語ランタイム](../Page/共通言語ランタイム.md "wikilink")における[P/Invoke](https://ja.wikipedia.org/wiki/P/Invoke "wikilink") のように、他の[仮想マシン環境と共通する事例である](../Page/仮想機械.md "wikilink")。

### 解決策・代替案

現在では今のところ、Javaはまだまだハードウェア開発、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")開発には適していない点が多い。この問題について、Javaで[USBドライバ開発ができる](../Page/ユニバーサル・シリアル・バス.md "wikilink") Java Communication API という技術がすでにある。他にも、[Jini](../Page/Jini.md "wikilink")対応機器を端末に接続すると、サーバから自動的にJava製ドライバを端末にダウンロードしてその機器を使うことができる技術[Jini](../Page/Jini.md "wikilink")というものが考えられている。なおこのJiniは、[Java Native Interfaceを意味するJNIとは別物である](../Page/Java_Native_Interface.md "wikilink")。

## 一貫性のないJava仮想マシン実装

Javaは、[Java仮想マシン](../Page/Java仮想マシン.md "wikilink") (JVM) の上部で動くバイトコード言語である。異なるプラットフォームで実行できる能力と言語の互換性は、最終的にはJVM実装の安定性とJVMのバージョンに依存している。Javaは非常に様々なシステム上で動くとうたわれているが、最新のJVM（と[JRE](../Page/Java_Runtime_Environment.md "wikilink")）はWindows、[Linux](../Page/Linux.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink")対応だけ活発に更新されている状況である。[HP-UX](../Page/HP-UX.md "wikilink")（Java for HP-UXなど）と[IBM](../Page/IBM.md "wikilink") (for MVS、AIX、OS/400) は、それぞれのプラットフォームファミリー独自の実装を提供するが、必ずしも最新のサン・マイクロシステムズのリリースを反映していない。他のプラットフォームにおけるJVM実装も、たいてい今後も続くが、時々一般の実装例よりも何年か何ヶ月か遅れるので、互換性問題が生じる。具体的な例を示すと、Java 2 Platform Standard Edition 1.5 (J2SE 1.5) をサン・マイクロシステムズがリリースしたのは2004年9月30日\[23\]だが、[Mac OS X用J](https://ja.wikipedia.org/wiki/macOS "wikilink")2SE 1.5を[アップルが公開したのは](../Page/アップル_\(企業\).md "wikilink")2005年3月\[24\]であり、5か月余りの差が生じている。

## 移植性・互換性

"[Write once, run anywhere](../Page/Write_once,_run_anywhere.md "wikilink")"（WORA、一度書けばどこでも動く）という言葉があるとおり、Javaの目標の一つに[プラットフォーム非依存があげられる](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。[Javaコンパイラ](../Page/Javaコンパイラ.md "wikilink")は[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")用の[中間言語](../Page/中間言語.md "wikilink")（[Javaバイトコード](https://ja.wikipedia.org/wiki/Javaバイトコード "wikilink")）を生成する。[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")されたJavaのプログラムは、Java仮想マシンを実行環境として動作する。この仮想マシンがハードウェア間の差異を吸収することで、プラットフォーム非依存を実現している。ただし、現時点では一部に[プラットフォーム依存の部分があり](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")、完全な[プラットフォーム非依存ではない](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。

また、マルチプラットフォームにするということは、一部のプラットフォームにしかない独自の機能はJavaから使えないことを意味する。 例えば[Windows用のマルチメディア](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[DirectXや](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、3DグラフィックスAPIである[Direct3D](../Page/Direct3D.md "wikilink")はJavaから直接呼び出すことはできない。そのため、橋渡しをするための拡張APIが提供されている。

またJavaではバージョン間の[前方互換](https://ja.wikipedia.org/wiki/前方互換 "wikilink")性・[後方互換](https://ja.wikipedia.org/wiki/後方互換 "wikilink")性の問題が議論の対象になっている。Javaではバージョン間の互換性をある程度の水準まで達成している。しかし、バージョンの異なる実行環境の取り扱いには課題が残っている。例えば[J2SE](../Page/Java_Platform,_Standard_Edition.md "wikilink") 1.4実行環境用に書かれたプログラムは、実行環境にJ2SE 1.3を想定すると明示的に指定してコンパイルしなければJ2SE 1.3実行環境では動かず、利用する[ライブラリ](../Page/ライブラリ.md "wikilink")がJ2SE 1.4以降から追加されたものである場合にはJ2SE 1.3実行環境での実行を諦めなければならない。J2SE 1.3に対する後方互換性は、2世代先であるJ2SE 5.0まで保証されている。J2SE 1.3以降のJavaプログラムでは前方互換性は保証されないが、Java実行環境 (JRE) の自動アップデート機能によって仮想マシンを最新バージョンにアップデートすれば解決できる。 JDK 1.1、J2SE 1.2 時代のJavaプログラムは、となっては古いため、後方互換性問題に引っかかる可能性がある。例えば、古いプログラムが新しいバージョンのJDK/JREで廃止されたAPIを使用している場合に問題となる。その場合は、そのJavaプログラム開発者に最新版のJavaコンパイラでもコンパイルが通るように修正してもらうしかない。

### 解決策・代替案

この問題も、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")のJavaコーディング規約をJava[プログラマ](../Page/プログラマ.md "wikilink")が守っていればほぼ起きることがなく、Javaソースコード上のimport宣言や新しく加わった[Javaキーワード](https://ja.wikipedia.org/wiki/予約語_\(Java\) "wikilink")（enumやassert）と重複するものが無ければほぼ心配することもなくなる。とくに、多くの場合において、これらの問題はコーディング規約だけでなく、[統合開発環境](../Page/統合開発環境.md "wikilink")や[CheckStyle](https://ja.wikipedia.org/wiki/CheckStyle "wikilink")、[FindBugs](https://ja.wikipedia.org/wiki/FindBugs "wikilink")など各種ツールなどによって解決できるケースがある。Javaプログラマは、日頃からCheckStyleやFindBugsを使って[プログラミングしていれば](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、後方互換性の問題につき当たる可能性は下がる。しかし、[Javaアプレット](../Page/Javaアプレット.md "wikilink")などのように、方針転換による大規模な機能廃止もありうる。JDK/JREにはサポート期間が定められており、古いJDK/JREを永久に使い続けることはできないため、廃止予定となったAPIが完全廃止される前に代替技術に移行するなど、最新のJava技術動向に追随していく必要がある。

## 脚注

## 関連項目

  - [C\#とJavaの比較](../Page/C_SharpとJavaの比較.md "wikilink")
  - [JavaとC++の比較](../Page/JavaとC++の比較.md "wikilink")

## 外部リンク

  - [Free But Shackled - Javaの罠](http://www.gnu.org/philosophy/java-trap.html) - [フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")運動の[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")によるエッセイ (2004年4月12日)

  -
[de:Java (Technik)\#Kritik](https://ja.wikipedia.org/wiki/de:Java_\(Technik\)#Kritik "wikilink")

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:コンピュータ分野における議論と対立](https://ja.wikipedia.org/wiki/Category:コンピュータ分野における議論と対立 "wikilink") [Category:批判](https://ja.wikipedia.org/wiki/Category:批判 "wikilink")

1.  実際にはJavaは、当初は[組み込みシステム](../Page/組み込みシステム.md "wikilink")のための言語と処理系として設計された。
2.  “[Setting the class path](http://java.sun.com/javase/6/docs/technotes/tools/windows/classpath.html)” (Windows). *Java SE 6 Documentation, JDK Development Tools Reference*. Sun Microsystems. Accessed 2007-01-27.
3.  “[Setting the class path](http://java.sun.com/javase/6/docs/technotes/tools/solaris/classpath.html)” (Solaris and Linux). *Java SE 6 Documentation, JDK Development Tools Reference*. Sun Microsystems. Accessed 2007-01-27.
4.
5.
6.  [developerWorks \> Java technology \> One-JARでアプリケーションの配布を単純化するカスタムのクラスローダーによるパワー・プログラミング](http://www-06.ibm.com/jp/developerworks/java/041217/j_j-onejar.html)
7.  さらに、一部の専門家はJava SCSLライセンスは誰もがJavaのフリー[ソフトウェアクリーンルーム](../Page/ソフトウェアクリーンルーム.md "wikilink")実装に貢献するために著作権を放棄するライセンス条項に同意することを要求していると主張している。しかしながらサン・マイクロシステムズの人々は、改訂されたJavaライセンス条項の下ではもはや問題ではなくなったと主張している。
8.  .
9.
10. サンの論点は彼らが非互換分岐なしにオープンソースJavaを欲しがる方法であった
11. これは次の[JavaOne](https://ja.wikipedia.org/wiki/JavaOne "wikilink")でサンの[最高経営責任者](../Page/最高経営責任者.md "wikilink")を務める[ジョナサン・シュワルツ](../Page/ジョナサン・シュワルツ.md "wikilink")のコメントにより説明される可能性がある。彼のブログではこう語っている。「我々はオープンソースJavaの厳粛な前進を行っているが（GPLライセンスが*議論中*であるというは皮肉にもかかわらず）、何が一番大事であるかに議論の焦点をあてている。一番大事なことはソースコードを入手する機会ではない(ソースコードはすでに広く利用可能である)。一番大事なことは互換性を確固たるものとすることである。」
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.