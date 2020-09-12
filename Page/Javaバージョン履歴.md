> この記事は[Javaバージョン履歴](https://ja.wikipedia.org/wiki/Javaバージョン履歴)から翻訳されています。


本稿では**[Java](https://ja.wikipedia.org/wiki/Java "wikilink")**[プラットフォームの基準である](../Page/Javaプラットフォーム.md "wikilink")[スタンダード版のメジャーバージョン履歴を説明する](../Page/Java_Platform,_Standard_Edition.md "wikilink")。その他にも[エンタープライズ版](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")、[マイクロ版](../Page/Java_Platform,_Micro_Edition.md "wikilink")、[カード版といった周辺エディションが存在し](../Page/Java_Card.md "wikilink")、それぞれが個別にメジャーバージョン改訂を行っているが、いずれもスタンダード版改訂を基準にしそれに後発する時系列でリリースされている。

## バージョン一覧

### JDK 1.0 (1996年1月23日)

Javaプラットフォームの初回バージョンは、ブランド名「Java」プロダクト名「Development Kit」から「Java Development Kit」とネーミングされ通称は「JDK」とされた。当初のメジャーバージョン値は小数点第一位にされた。通称にバージョン値を付けたものがリリース名になった。まだ国際化対応はされず英語版のみだった\[1\]。

  - ファイル入出力
  - ネットワーク接続（TCPソケットとUDPソケット）
  - データコレクション（Array、Vector、List、Set、Map）
  - 数学演算
  - アプレットとセキュリティ
  - [Abstract Window Toolkit](../Page/Abstract_Window_Toolkit.md "wikilink")（グラフィカルユーザーインターフェースサポート）

### JDK 1.1 (1997年2月19日)

[国際化対応され日本語版も追加された](../Page/国際化と地域化.md "wikilink")\[2\]。

  - 内部クラス（言語仕様）
  - [JavaBeans](../Page/JavaBeans.md "wikilink")（[ソフトウェアコンポート用API](../Page/ソフトウェアコンポーネント.md "wikilink")）
  - [データベース接続](../Page/JDBC.md "wikilink")
  - 印刷サービス
  - [Java RMI](../Page/Java_Remote_Method_Invocation.md "wikilink")（分散オブジェクトAPI）
  - [リフレクション](../Page/リフレクション_\(情報工学\).md "wikilink")（クラスメタデータ操作API）
  - Java Text（文章、暦、日付、数値などの国別書式）
  - Input Method Framework（文章入力の国別書式）
  - Java 2D（グラフィックサポート）

### J2SE 1.2 (1998年12月8日)「Playground」

大幅な技術刷新によりブランド名が「Java 2」に改められた。統合仕様の確立でプロダクト名が「Platform」に改められた。エディションの分化で「Standard」が付加された。こうして「Java 2 Platform, Standard Edition」通称「J2SE」になった。ここからコードネームが付けられるようになった\[3\]。翌年にエンタープライズ版「J2EE 1.2」とマイクロ版「J2ME 1.2」もリリースされた。

  - `strictfp`キーワード（言語仕様、浮動小数点計算）
  - 仮想マシンに実行時コンパイラ（*Just-In-Time Compiler*）
  - Javaプラグイン（WEBブラウザへのアプレット実行環境挿入）
  - [Swing](../Page/Swing.md "wikilink")（グラフィックユーザーインターフェース）
  - Collection Framework（コレクションAPI）
  - Security Framework（セキュリティAPI）
  - Java Internet Description Language（[IDLからJava](https://ja.wikipedia.org/wiki/IDL_\(プログラミング言語\) "wikilink") CORBA用スタブ＆スケルトンを生成）
  - Java Accessibility API（画面Reader、音声認識、点字端末などのユーザー補助機能）

### J2SE 1.3 (2000年5月8日)「Kestrel」

ここからメジャーバージョンのコードネームは鳥獣名、マイナーバージョンは昆虫名にするのが慣例になった\[4\]\[5\]。

  - 仮想マシンに[HotSpot](../Page/HotSpot.md "wikilink")エンジン（動的再コンパイル技術と[世代別ガベージコレクション](../Page/世代別ガベージコレクション.md "wikilink")）
  - Java Platform Debugger Architecture（デバッガ・アーキテクチャ）
  - [Java Name and Directory Interface](../Page/Java_Naming_and_Directory_Interface.md "wikilink")（ネーミング＆ディレクトリサービスAPI）
  - [RMI over IIOP](../Page/RMI-IIOP.md "wikilink")（RMIをIIOPプロトコル上でも使える仕様）
  - Java Sound（サウンドAPI）

### J2SE 1.4 (2002年2月6日)「Merlin」

このバージョンからJavaコミュニティプロセス（[Java Community Process](../Page/Java_Community_Process.md "wikilink")）による仕様策定が開始された\[6\]\[7\]\[8\]。

  - `assert` キーワード（言語仕様、デバッグ用ディレクティブ、任意条件でプログラム中断）
  - [Java Web Start](../Page/Java_Web_Start.md "wikilink")
  - [正規表現](../Page/正規表現.md "wikilink")用API
  - ロギング用API
  - New I/O（非遮断ストリーム入出力、バッファストリームAPI）
  - Image I/O（[JPEG](../Page/JPEG.md "wikilink")と[PNGを使えるAPI](../Page/Portable_Network_Graphics.md "wikilink")）
  - Preferences（ツリー型のJava式セーブデータ収納庫API）
  - [Java API for XML Processing](../Page/Java_API_for_XML_Processing.md "wikilink")（[XMLパーサ](../Page/Extensible_Markup_Language.md "wikilink")＆マニュピレータAPI、[XSLTフォーマットAPI](../Page/XSL_Transformations.md "wikilink")）
  - Java Cryptography Extension（暗号化API）
  - Java Secure Socket Extension（[TLS / SSL用API](../Page/Transport_Layer_Security.md "wikilink")）
  - Java Authentication and Authorization Service（認証＆権限サービスAPI）

### J2SE 5.0 (2004年9月30日)「Tiger」

メジャーバージョン値が整数部分に変更された。言語仕様に大幅な拡張が加えられた\[9\]\[10\]。メモリモデル改善でマルチスレッドも軽量化した。他エディションは「J2EE 1.4」「J2ME 1.4」のままだった。この頃に「Java Card Platform」がエディション昇格し、バージョンは独自式のまま「Java Card 2.2」でリリースされた。

  - [ジェネリクス](https://ja.wikipedia.org/wiki/ジェネリクス "wikilink")（[パラメトリック多相を適用したデータコンテナクラス](https://ja.wikipedia.org/wiki/多態性 "wikilink")→ `List`<T>）
  - [オートボクシング](https://ja.wikipedia.org/wiki/オートボクシング "wikilink")（[ボックス化](../Page/ボックス化.md "wikilink")、プリミティブ値とラッパーインスタンスの自動変換）
  - [列挙型](../Page/列挙型.md "wikilink")（`enum`キーワードで定数クラスを定義）
  - 可変長引数（引数欄の型名に3連ドットで配列渡しと解釈される→ `void drawText(String... lines)`）
  - [アノテーション](../Page/アノテーション.md "wikilink")（`@`キーワードでクラスメタデータに注釈タグと注釈コメントを埋め込むアドホック多相）
  - 拡張`for`文（対象リストの[イテレータ](../Page/イテレータ.md "wikilink")表現式になるfor文）
  - 静的インポート文（クラス静的メンバのフルパスを`import`で指定できる）
  - [Java Management Extensions](../Page/Java_Management_Extensions.md "wikilink")（MBeanを用いた[依存性の注入](../Page/依存性の注入.md "wikilink")による実行プログラムの動的再構成の最適化）

### Java SE 6 (2006年12月11日)「Mustang」

ブランド名が「Java 2」から「Java」に戻されて通称が「J2SE」から「Java SE」になった。バージョン値から小数点以下が外された。なおマイナーバージョン更新では再び小数点以下が付けられた。他エディションも「Java EE 5」「Java ME 5」になった。仮想マシンを含めた既存機能の改善と洗練に力が注がれた。

  - Scripting for the Java Platform（スクリプト言語との連携サポート）
  - Java Architecture for XML Binding（Java XMLアーキテクチャ）
  - Java API for XML Web Services（WEB向けのXML）
  - Java Compiler API（Javaコンパイラへのディレクティブに特化したAPI）
  - [Unicode正規化](../Page/Unicode正規化.md "wikilink") API
  - 差し込みアノテーション（インスタンス別、クラス派生別にアノテーションを埋め込めるアドホック多相）
  - [Swing](../Page/Swing.md "wikilink")の高速化、[Windows用ルック](../Page/Windows_Aero.md "wikilink")＆フィールの追加、Windows[タスクトレイ](../Page/タスクトレイ.md "wikilink")表示
  - Update10で、Java Quick Starter（アプリ起動高速化）Java Kernel（Java環境インストール高速化）を搭載\[11\]

### Java SE 7 (2011年7月28日)「Dolphin」

サン社を買収したオラクル社による初のメジャーバージョンリリースである。

  - invoke_dynamic API（クラスインスタンスとメソッドシグネチャの組み換えによる動的ディスパッチ）
  - New File I/O Library（新しいファイル入出力ライブラリ）
  - Concurrency Library（並行処理API）
  - 暗号化APIに[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")を導入
  - ネットワークAPIに[Stream Control TransmissionプロトコルとSockets](../Page/Stream_Control_Transmission_Protocol.md "wikilink") Directプロトコルを導入
  - グラフィック関連の強化。Update2で[JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")の導入

### Java SE 8 (2014年3月18日)

ここでコードネームが廃止された\[12\]。長期サポート（LTS）リリース制度下の最終版である。

  - 言語仕様に[ラムダ式の導入](https://ja.wikipedia.org/wiki/無名関数 "wikilink")（引数 -\> 関数式）
  - 関数型インターフェース（引数と返値をテンプレート化できるパラメトリック多相）
  - Stream API（コレクションコンテナ各要素への連続的なラムダ式適用）
  - JavaScriptのコードを埋め込めるNashorn Javaスクリプトエンジンの搭載（Project Nashorn）
  - 型アノテーション（`@interface`で構造体化したアノテーションを定義、複数の注釈フィールドを持つ）
  - 反復アノテーション（バックグラウンドタスクのクラスをアドホック多相で任意日時稼働にスケジュールする）
  - Date and Time API（日付時刻）
  - 静的結合 [Java Native Interface](../Page/Java_Native_Interface.md "wikilink") ライブラリ

### Java SE 9 (2017年9月21日)

ここからメジャーバージョンは一定の新機能蓄積を待たずに公開する毎年3月と9月の年2回定期リリース制に変更された\[13\]。従来の長期サポート（LTS）が無くなり、原則的に半年間サポートになった。

  - *従来のパッケージ（*package*）の上にモジュール（*module*）を追加（*Project Jigsaw）
  - 言語仕様の細かな拡張（Project Coin）
  - 並行処理ライブラリの拡張
  - Compact Stringの追加
  - 「JShell」の搭載。コンソール形式でJavaコードを入力し実行結果を確認できる
  - 「The Java Linker」の搭載。ユーザー環境に最適なモジュールと仮想マシンモードを自動選択実行する
  - 仮想マシンに前方コンパイル（*Ahead-Of-Time Compilation*）の導入
  - XML catalogs（永続的URLへのマッピング）
  - [HiDPI](https://ja.wikipedia.org/wiki/HiDPI "wikilink") Graphicsの導入（画像拡大縮小の改善）

### Java SE 10 (2018年3月20日)

JSR 383にて仕様規定\[14\]。ここから追加機能の大半は規範テクノロジ相当のJSR（仕様要求）ではなく、拡張テクノロジ相当のJEP（改良提案）になった。JEPは導入宣言バージョンでのみその安定性が保証される。

  - ローカル変数の[型推論](../Page/型推論.md "wikilink")
  - [ルート証明書](../Page/ルート証明書.md "wikilink")
  - Unicode language-tag extensions（Unicode言語タグの操作）
  - Zガベージコレクタ（ZGC）第1版

### Java SE 11 (2018年9月25日)

JSR 384にて仕様規定\[15\]。Java開発環境として「Oracle JDK」と「[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")」の二つが提供されるようになり、前者の商用利用は有償長期サポート（LTS）契約を結んだ顧客のみになった。Java EEのアップグレードがエクリプス財団による「Jakarta EE」に移譲されたので、JDKにEnterprise版連携モジュールが含まれなくなった。CORBAモジュールも外された。[Java FXも取り除かれた](https://ja.wikipedia.org/wiki/JavaFX "wikilink")。このバージョンは長期サポート（LTS）対象にされているが、上述の通り有償LTSである。

  - Dynamic class-file constants（拡張invoke_dynamic、クラスローディングによるクラス静的メンバの動的バインディング）
  - [ラムダ式の引数の型推論](https://ja.wikipedia.org/wiki/無名関数 "wikilink")
  - HTTPクライアント実装用API
  - Flight recorder（Javaプログラム実行トレース用の軽快な各種データ収集フレームワーク）
  - Unicode 10.0.0のサポート
  - Zガベージコレクタ（ZGC）第2版

### Java SE 12 (2019年3月19日)

JSR 386にて仕様規定。アップデートで令和改元に向けたセキュリティ対策が施された。

  - switch文を[パターンマッチング](../Page/パターンマッチング.md "wikilink")式スタイルに拡張・第1版
  - JVM Constants API（クラスローディングに関連した仮想マシン内のクラス定数プールの操作）
  - Zガベージコレクタ（ZGC）第3版

### Java SE 13（2019年9月17日)

JSR 388にて仕様規定。「数百の小粒改良、数千のバグ修正」と宣伝された。

  - ソケットAPIの改良実装
  - switch文を[パターンマッチング](../Page/パターンマッチング.md "wikilink")式スタイルに拡張・第2版
  - Text Blocks（[文字列](../Page/文字列.md "wikilink")リテラルの複数行記述可能）第1版

### Java SE 14（2020年3月17日)

JSR 389にて仕様規定。

  - Recordクラス（不変フィールド、標準アクセッサ、標準構築子を持つイミュータブルオブジェクト）第1版
  - instanceofパターンマッチング（if文のinstanceof判定で代入変数も同時定義できる糖衣構文）第1版
  - switch文を[パターンマッチング](../Page/パターンマッチング.md "wikilink")式スタイルに拡張・第3版
  - Text Blocks（[文字列](../Page/文字列.md "wikilink")リテラルの複数行記述可能）第2版
  - Foreign-Memory Access API （仮想マシンの外部メモリにも安全にアクセスできる）第1版
  - Zガベージコレクタ（ZGC）第4版

### Java SE 15（2020年9月15日予定)

以下のJEP（改善提案）が導入予定である。

  - JEP-339：[Edwards-Curve デジタル署名アルゴリズム](https://openjdk.java.net/jeps/339)
  - JEP-360：[Sealedクラス・第1版](https://openjdk.java.net/jeps/360)（サブクラスを事前定義で固定化したクラス。オブジェクトの[非交和](https://ja.wikipedia.org/wiki/非交和 "wikilink")＝直和構造を表わす）
  - [JEP-371：Hiddenクラス](https://openjdk.java.net/jeps/371)（通常使用できないフレームワーク内限定クラス。[モンキーパッチ](https://ja.wikipedia.org/wiki/モンキーパッチ "wikilink")などに応用できる。）
  - JEP-373：[データグラム・ソケットAPIの改良実装](https://openjdk.java.net/jeps/373)
  - JEP-375：[instanceofパターンマッチング・第2版](https://openjdk.java.net/jeps/375)
  - [JEP-377：ZGC：応答時間短縮化ガーベジコレクタ・第5版](https://openjdk.java.net/jeps/377)
  - [JEP-378：Text Blocks・第3版](https://openjdk.java.net/jeps/378)
  - [JEP-379：Shenandoah：休止時間短縮化ガベージコレクタ](https://openjdk.java.net/jeps/379)
  - JEP-383：[Foreign-Memory Access API・第2版](https://openjdk.java.net/jeps/383)
  - JEP-384：[Recordクラス・第2版](https://openjdk.java.net/jeps/384)（フィールドを不変にしたクラス。オブジェクトの[直積構造を表わす](../Page/直積集合.md "wikilink")）

## 概要

[Java](https://ja.wikipedia.org/wiki/Java "wikilink")言語では、[JDK](../Page/Java_Development_Kit.md "wikilink")1.0以降、標準[ライブラリ](../Page/ライブラリ.md "wikilink")に[クラスやパッケージが多数追加されただけでなく](../Page/クラス_\(コンピュータ\).md "wikilink")、いくつかの変更が行われてきた。J2SE 1.4以降、Java言語の進化は、[Java Community Process](../Page/Java_Community_Process.md "wikilink") (JCP)によって管理されてきた。このプロセスでは、Java Specification Requests（JSR）を使用してJavaプラットフォームへの追加や変更を提案・指定している。言語はJava言語仕様書（JLS）によって規定されており、JLSへの変更は[JSR 901](http://www.jcp.org/en/jsr/detail?id=901)によって管理されている。

言語の変更に加えて、[Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")にも長年にわたって変更が加えられ、JDK 1.0の数百クラスからJ2SE 5では3,000クラスを超えるまでに成長した。 [Swing](../Page/Swing.md "wikilink")や[Java2Dなどの全く新しい](../Page/Java_2D.md "wikilink")[APIが導入され](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、オリジナルのJDK 1.0のクラスやメソッドの多くが非推奨となっている。いくつかのプログラムでは、Javaプログラムを[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")のあるバージョンから古いバージョンに変換することができる（例えば、Java 5.0を1.4にバックポートするなど）。

Java 11は、現在サポートされている長期サポート（LTS）バージョン（「オラクルの顧客は、Oracle Premier Supportを提供される」）である。オラクルは、「[レガシー](https://ja.wikipedia.org/wiki/レガシーシステム "wikilink")」Java 8 LTSについて、商用利用向けには2019年1月に最後の無料の「パブリック・アップデート」をリリースしたが、それ以外の場合は、少なくとも2020年12月までは、個人利用向けのパブリック・アップデートでJava 8をサポートする\[16\]。Java 10は以前サポートされていたラピッドリリース版である。Java 10のサポートは、Java 11のサポートが開始されたのと同じ日、2018年9月に終了した。Java 7はパブリックサポートが終了し、Java 9はJava 10と現在のJava 11に取って代わられた短期のラピッドリリース版であったため、アップデートの受信が停止している。Java 11については、長期的なサポートはオラクルが一般向けに提供するものではなく、AdoptOpenJDKなどとして、より広範な[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")コミュニティが作業を行うことが期待されている\[17\]。

Java 14の一般提供は2020年3月17日に行われ\[18\] 、Java 15にはアーリーアクセスビルドが含まれている。 \[19\]

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>無料公開アップデート期限[20][21]</p></th>
<th><p>延長サポート期限</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>1995</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>1996年1月</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>1997年2月</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>1998年12月</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2000年5月</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>2002年2月</p></td>
<td><p>2008年10月</p></td>
<td><p>2013年2月</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2004年9月</p></td>
<td><p>2009年11月</p></td>
<td><p>2015年4月</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>2013年4月</p></td>
<td><p>2018年12月</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2011年7月</p></td>
<td></td>
<td><p>2022年7月</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>2014年3月</p></td>
<td><p>Oracle（商用）　　 2019年1月まで Oracle（個人用）　 2020年12月まで</p>
<p>AdoptOpenJDK　　2026年5月以降も予定</p>
<p>Amazon Corretto　2023年6月までは保証<ref name="Corretto2018">{{cite web</p></td>
<td><p>title = Introducing Amazon Corretto, a No-Cost Distribution of OpenJDK with Long-Term Support</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2017年9月</p></td>
<td><p>OpenJDK 2018年3月</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>2018年3月</p></td>
<td><p>OpenJDK 2018年9月</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2018年9月</p></td>
<td><p>Amazon Corretto　2024年8月以降も予定[22] AdoptOpenJDK　　2024年10月まで</p></td>
<td><p>2026年9月</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>2019年3月</p></td>
<td><p>OpenJDK 2019年9月</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2019年9月</p></td>
<td><p>OpenJDK 2020年3月</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>2020年3月</p></td>
<td><p>OpenJDK 2020年9月</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2020年9月</p></td>
<td><p>OpenJDK 2021年3月</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>2021年3月</p></td>
<td><p>OpenJDK 2021年9月</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>2021年9月</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><small></small></p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 参考文献

## 外部リンク

  - [公式Java SEダウンロード](https://www.oracle.com/technetwork/java/javase/downloads/index.html)
  - [Javaの初期の歴史](http://www.agocg.ac.uk/brief/java.htm)
  - [J2SE 1.3の変更点の完全なリスト](https://web.archive.org/web/20110318063805/http://download.oracle.com/javase/1.3/docs/relnotes/features.html)
  - [J2SE 1.4の変更点の完全なリスト](https://web.archive.org/web/20110317073530/http://download.oracle.com/javase/1.4.2/docs/relnotes/features.html)
  - [J2SE 5.0の変更点の完全なリスト](http://download.oracle.com/javase/1.5.0/docs/relnotes/features.html)
  - [Java SE 6の変更点の完全なリスト](https://web.archive.org/web/20061208161637/https://java.sun.com/javase/6/features.jsp)
  - [Java SE 6のMustang開発サイト](https://web.archive.org/web/20070618133610/https://jdk6.dev.java.net/)
  - [Java SE 7リリースノート](https://www.oracle.com/technetwork/java/javase/jdk7-relnotes-429209.html)
  - [Sun JavaがサポートするバージョンとEOL](https://www.oracle.com/technetwork/java/eol-135779.html)
  - [古いバージョンのJavaのダウンロードアーカイブ](https://www.oracle.com/technetwork/java/archive-139210.html)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:ソフトウェアの歴史](https://ja.wikipedia.org/wiki/Category:ソフトウェアの歴史 "wikilink")

1.
2.
3.
4.
5.
6.  [JSR 59](http://www.jcp.org/en/jsr/detail?id=59)
7.
8.
9.
10.
11.
12. [JSR 337: Java SE 8 Release Contents](http://jcp.org/en/jsr/detail?id=337)
13.
14. [JSR 383: Java™ SE 10 (18.3)](http://jcp.org/en/jsr/detail?id=383)
15. [JSR 384: JavaTM SE 11 (18.9)](http://jcp.org/en/jsr/detail?id=384)
16.
17.
18.
19.
20.
21.
22.