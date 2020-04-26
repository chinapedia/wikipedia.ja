> この記事は[Javaバージョン履歴](https://ja.wikipedia.org/wiki/Javaバージョン履歴)から翻訳されています。


[Java](https://ja.wikipedia.org/wiki/Java "wikilink")言語では、[JDK](../Page/Java_Development_Kit.md "wikilink")1.0以降、標準[ライブラリ](../Page/ライブラリ.md "wikilink")に[クラスやパッケージが多数追加されただけでなく](../Page/クラス_\(コンピュータ\).md "wikilink")、いくつかの変更が行われてきた。J2SE 1.4以降、Java言語の進化は、[Java Community Process](../Page/Java_Community_Process.md "wikilink") (JCP)によって管理されてきた。このプロセスでは、Java Specification Requests（JSR）を使用してJavaプラットフォームへの追加や変更を提案・指定している。言語はJava言語仕様書（JLS）によって規定されており、JLSへの変更は[JSR 901](http://www.jcp.org/en/jsr/detail?id=901)によって管理されている。

言語の変更に加えて、[Javaクラスライブラリ](https://ja.wikipedia.org/wiki/Javaクラスライブラリ "wikilink")にも長年にわたって変更が加えられ、JDK 1.0の数百クラスからJ2SE 5では3,000クラスを超えるまでに成長した。 [Swing](../Page/Swing.md "wikilink")や[Java2Dなどの全く新しい](../Page/Java_2D.md "wikilink")[APIが導入され](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、オリジナルのJDK 1.0のクラスやメソッドの多くが非推奨となっている。いくつかのプログラムでは、Javaプログラムを[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")のあるバージョンから古いバージョンに変換することができる（例えば、Java 5.0を1.4にバックポートするなど）。

Java 11は、現在サポートされている長期サポート（LTS）バージョン（「オラクルの顧客は、Oracle Premier Supportを提供される」）である。オラクルは、「[レガシー](https://ja.wikipedia.org/wiki/レガシーシステム "wikilink")」Java 8 LTSについて、商用利用向けには2019年1月に最後の無料の「パブリック・アップデート」をリリースしたが、それ以外の場合は、少なくとも2020年12月までは、個人利用向けのパブリック・アップデートでJava 8をサポートする\[1\]。Java 10は以前サポートされていたラピッドリリース版である。Java 10のサポートは、Java 11のサポートが開始されたのと同じ日、2018年9月に終了した。Java 7はパブリックサポートが終了し、Java 9はJava 10と現在のJava 11に取って代わられた短期のラピッドリリース版であったため、アップデートの受信が停止している。Java 11については、長期的なサポートはオラクルが一般向けに提供するものではなく、AdoptOpenJDKなどとして、より広範な[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")コミュニティが作業を行うことが期待されている\[2\]。

Java 14の一般提供は2020年3月17日に行われ\[3\] 、Java 15にはアーリーアクセスビルドが含まれている。 \[4\]

Java開発チームは、2020年9月15日までにJDK 15を発表する予定である。 しかし、彼らはすでに次のバージョンのいくつかのアップデートを明らかにしている。 これまでのJDK 15を対象としたJEPは以下である。

  - [JEP-371：非表示のクラス](https://openjdk.java.net/jeps/371)
  - [JEP-372：Nashorn JavaScriptエンジンを削除](https://openjdk.java.net/jeps/372)
  - [JEP-377：ZGC：スケーラブルな低レイテンシガベージコレクター（プロダクション）](https://openjdk.java.net/jeps/377)
  - [JEP-378：テキストブロック](https://openjdk.java.net/jeps/378)
  - [JEP-379：Shenandoah：少ない休止時間のガベージコレクター（プロダクション）](https://openjdk.java.net/jeps/379)

<table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>リリース日</p></th>
<th><p>無料公開アップデート期限[5][6]</p></th>
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
<td><p><strong>Oracle（商用）の場合は2019年1月</strong> Oracle（個人使用）の場合は2020年12月</p>
<p>AdoptOpenJDKの場合は2026年5月以上</p>
<p>Amazon Correttoの場合は少なくとも2023年6月<ref name="Corretto2018">{{cite web</p></td>
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
<td><p>Amazon Correttoは2024年8月以降[7] AdoptOpenJDKは2024年10月</p></td>
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

## バージョン履歴

1996年の第一回公開のJavaプラットフォームは「*Java Development Kit*」通称「*JDK*」と呼ばれており、最初のバージョン数値は「1.0」に定められた。通称とバージョン値を合わせたものが製品名とされて「JDK 1.0」で市場導入されている。当初は開発チームの控えめにしたい意向で小数点第一位がメジャーバージョン値にされたが、これは不必要な謙遜という声もあった。

1998年の第三回メジャーバージョン公開である「1.2」では大幅な技術刷新をアピールするべく「*Java 2*」と次世代呼称にした。これは経営側の判断だったので開発側は小数点第一位の数値改訂を譲らなかった。製品仕様の確立で「*Development Kit*」は「*Platform*」に置き換えられた。マーケットの分化を示唆する「Standard」のエディション名も付けられた。こうして「*Java 2 Platform, Standard Edition*」の通称「*J2SE*」とバージョン値「1.2」を合わせた製品名「J2SE 1.2」で市場導入された。この次世代呼称と小数点第一位の混在名は意味が不明瞭で製品バージョンへの理解を妨げかねないと不評を買っている。この時はまだStandard版だけであったが、翌1999年にEnterprise版の「J2EE 1.2」とMicro版の「J2ME 1.2」が市場導入されて３エデイションになった。

2005年の第六回メジャーバージョン公開である「1.5」から整数部分がメジャーバージョン値にされて「5.0」になり、通称と合わせた製品名は「J2SE 5.0」になった。他のエディションは後発なので「J2EE 1.4」「J2ME 1.4」のままだった。この頃に「*Java Card Platform*」が正規のエディション認定されているが、バージョン体系は独自のままの「Java Card 2.2」であり、これは以降も継続された。

2006年の第七回メジャーバージョン公開で「*Java 2*」の次世代呼称が外されて「*Java*」になり、バージョン値からも小数点以下が外された。「*Java Platform, Standard Edition*」「*Java Platform, Enterprise Edition*」「*Java Platform, Mirco Edition*」の各通称と各バージョン値を合わせた製品名は「Java SE 6」「Java EE 5」「Java ME 5」になった。なお、マイナーバージョンアップの際には再び小数点以下が付けられた。この命名方式は現在まで続いている。

## JDK 1.0 (1996年1月23日)

最初のバージョン\[8\]。まだ国際化対応はされず英語版のみだった。

## JDK 1.1 (1997年2月19日)

[国際化対応され日本語版も追加された](../Page/国際化と地域化.md "wikilink")\[9\]。

  - 内部クラス（言語仕様）
  - [JavaBeans](../Page/JavaBeans.md "wikilink")（[ソフトウェアコンポート仕様とAPI](../Page/ソフトウェアコンポーネント.md "wikilink")）
  - [Java Database Connectivity](../Page/JDBC.md "wikilink")（データベースAPI）
  - [RMI](../Page/Java_Remote_Method_Invocation.md "wikilink")（分散オブジェクトAPI）
  - [Java Reflection](../Page/リフレクション_\(情報工学\).md "wikilink")（クラスメタデータ操作API）
  - [AWTのイベントモデル拡張](../Page/Abstract_Window_Toolkit.md "wikilink")

## J2SE 1.2 (1998年12月8日)「Playground」

ここからコードネームが付けられるようになった\[10\]。

  - `strictfp`キーワード（言語仕様、浮動小数点計算）
  - 仮想マシンに実行時コンパイラ（*Just-In-Time Compiler*）
  - Javaプラグイン（WEBブラウザへのアプレット実行環境挿入）
  - Java Internet Description Language（[IDLからJava](https://ja.wikipedia.org/wiki/IDL_\(プログラミング言語\) "wikilink") CORBA用スタブ＆スケルトンを生成）
  - [Swing](../Page/Swing.md "wikilink")（グラフィカルAPI）
  - Collection Framework（コレクションAPI）

## J2SE 1.3 (2000年5月8日)「Kestrel」

ここからメジャーバージョンのコードネームは鳥獣名、マイナーバージョンは昆虫名にするのが慣例になった\[11\]\[12\]。

  - 仮想マシンに[HotSpot](../Page/HotSpot.md "wikilink")エンジン（動的再コンパイル技術と[世代別ガベージコレクション](../Page/世代別ガベージコレクション.md "wikilink")）
  - Java Platform Debugger Architecture（デバッガ・アーキテクチャ）
  - [Java Name and Directory Interface](../Page/Java_Naming_and_Directory_Interface.md "wikilink")（ネーミング＆ディレクトリサービスAPI）
  - JavaSound（サウンドAPI）
  - [RMI over IIOP](../Page/RMI-IIOP.md "wikilink")（RMIをIIOPプロトコル上でも使える仕様）

## J2SE 1.4 (2002年2月6日)「Merlin」

このバージョンからJavaコミュニティプロセス（[Java Community Process](../Page/Java_Community_Process.md "wikilink")）による仕様策定が開始された\[13\]\[14\]\[15\]。

  - `assert` キーワード（言語仕様、例外発生ディレクティブ）
  - 例外処理の連鎖格納（言語仕様）
  - [Java Web Start](../Page/Java_Web_Start.md "wikilink")
  - Regular Expression（[正規表現](../Page/正規表現.md "wikilink")API）
  - Non-blocking I/O API（非遮断ストリーム入出力API）
  - [Logging](https://ja.wikipedia.org/wiki/ログ "wikilink")（ログ取りAPI）
  - Image I/O（[JPEG](../Page/JPEG.md "wikilink")と[PNGを使えるAPI](../Page/Portable_Network_Graphics.md "wikilink")）
  - Preferences（ツリー型のJava式セーブデータ収納庫API）
  - [Java API for XML Processing](../Page/Java_API_for_XML_Processing.md "wikilink")（[XMLパーサ](../Page/Extensible_Markup_Language.md "wikilink")＆マニュピレータAPI、[XSLTフォーマットAPI](../Page/XSL_Transformations.md "wikilink")）
  - Java Cryptography Extension（暗号化API）
  - Java Secure Socket Extension（[TLS / SSL用API](../Page/Transport_Layer_Security.md "wikilink")）
  - Java Authentication and Authorization Service（認証＆権限サービスAPI）

## J2SE 5.0 (2004年9月30日)「Tiger」

言語仕様に大幅な拡張が加えられた\[16\]\[17\]。

  - [ジェネリクス](https://ja.wikipedia.org/wiki/ジェネリクス "wikilink")（コレクションコンテナに収納要素の型指定が可能 `List`<T>）
  - [オートボクシング](https://ja.wikipedia.org/wiki/オートボクシング "wikilink")（[プリミティブと](../Page/プリミティブ型.md "wikilink")[ラッパークラスの自動変換による相互代入](../Page/プリミティブラッパークラス.md "wikilink")）
  - [列挙型](../Page/列挙型.md "wikilink")（`enum`キーワードで定数列挙の型を定義）
  - 可変引数（最終引数の型名＋3個のドットで自動配列化 `void drawText(String... lines)`）
  - [アノテーション](../Page/アノテーション.md "wikilink")（`@`キーワードで、クラスメタデータの各要素に任意のタグワードと注釈を埋め込む）
  - 拡張`for`文（コレクションコンテナから各要素を順々に取り出すのが便利になるループ文）
  - 静的インポート文（他クラスの定数のフルパスを`import`で指定可能）
  - [Java Management Extensions](../Page/Java_Management_Extensions.md "wikilink")（MBeanを用いた[依存性の注入](../Page/依存性の注入.md "wikilink")による実行プログラム動的再構成の最適化）
  - メモリモデルの改善によるスレッド処理高速化

## Java SE 6 (2006年12月11日)「Mustang」

仮想マシンを含めた既存機能の改善と洗練に力が注がれた。

  - Scripting for the Java Platform（スクリプト言語との連携サポート）
  - Java Architecture for XML Binding（Java XMLアーキテクチャ）
  - Java API for XML Web Services
  - Java Compiler API（Javaコンパイラへのディレクティブ的なAPI）
  - [Unicode正規化](../Page/Unicode正規化.md "wikilink") API
  - Plugging annotation（コンパイル解析用途のアノテーション）
  - [Swing](../Page/Swing.md "wikilink")の高速化、[Windows用ルック](../Page/Windows_Aero.md "wikilink")＆フィールの追加、Windows[タスクトレイ](../Page/タスクトレイ.md "wikilink")表示
  - Update10で、Java Quick Starter（アプリ起動高速化）Java Kernel（Java環境インストール高速化）を搭載\[18\]

## Java SE 7 (2011年7月28日)「Dolphin」

サン社を買収したオラクル社による初のメジャーバージョンリリースである。

  - 言語仕様の細かな拡張
  - invoke_dynamic API（実装クラスとメソッドシグネチャの組み換えによる動的メソッド呼び出し）
  - New File I/O Library（新しいファイル入出力ライブラリ）
  - Concurrency Library（並列処理系ライブラリ）
  - コレクションフレームワークへのティムソートの採用
  - 暗号化APIに[楕円曲線暗号](../Page/楕円曲線暗号.md "wikilink")を導入
  - ネットワークAPIに[Stream Control TransmissionプロトコルとSockets](../Page/Stream_Control_Transmission_Protocol.md "wikilink") Directプロトコルを導入
  - グラフィック関連の強化
  - Update2で、[JavaFX](https://ja.wikipedia.org/wiki/JavaFX "wikilink")の導入

## Java SE 8 (2014年3月18日)

ここでコードネームが廃止された\[19\]。

  - 言語仕様に[ラムダ式の導入](https://ja.wikipedia.org/wiki/無名関数 "wikilink")（引数 -\> 関数式）
  - 関数型インターフェース
  - Stream API（コレクションコンテナ各要素への連続的なラムダ式適用）
  - JavaScriptのコードを埋め込めるNashorn Javaスクリプトエンジンの搭載（Project Nashorn）
  - Annotation on Java types（型アノテーション）
  - Repeating annotations（反復アノテーション）
  - Date and Time API（日付時刻）
  - 静的結合 [Java Native Interface](../Page/Java_Native_Interface.md "wikilink") ライブラリ

## Java SE 9 (2017年9月21日)

ここからメジャーバージョンは一定の新機能蓄積を待たずに公開する毎年3月と9月の年2回定期リリース制に変更された\[20\]。従来の長期サポート（LTS）が無くなり半年間限定になった。

  - 言語仕様に*package*を統合分類する「*module*」の導入（Project Jigsaw）
  - 言語仕様の細かな拡張（Project Coin）
  - 並列処理APIのアップデート、Flowクラスの追加など
  - Compact Stringの追加
  - 「JShell」の搭載。コンソール形式でJavaコードを入力し実行結果を確認できる
  - 「The Java Linker」の搭載。ユーザー環境に最適なモジュールと仮想マシンモードを自動選択実行する
  - 仮想マシンに前方コンパイル（*Ahead-Of-Time Compilation*）の導入
  - XML catalogs（永続的URLへのマッピング）
  - [HiDPI](https://ja.wikipedia.org/wiki/HiDPI "wikilink") Graphicsの導入（画像拡大縮小の改善）

## Java SE 10 (2018年3月20日)

JSR 383にて仕様規定\[21\]。ここから追加機能の大半は規範テクノロジ相当のJSR（仕様要求）ではなく、拡張テクノロジ相当のJEP（改良提案）になった。

  - ローカル変数の[型推論](../Page/型推論.md "wikilink")
  - ガーベジコレクタ関連
  - [ルート証明書](../Page/ルート証明書.md "wikilink")
  - Unicode language-tag extensions（Unicode言語タグの取り扱い）

## Java SE 11 (2018年9月25日)

JSR 384にて仕様規定\[22\]。Java開発環境として「Oracle JDK」と「[OpenJDK](https://ja.wikipedia.org/wiki/OpenJDK "wikilink")」の二つが提供されるようになり、前者の商用利用は有償長期サポート（LTS）契約を結んだ顧客のみになった。Java EEのアップグレードがエクリプス財団による「Jakarta EE」に移譲されたので、JDKにEnterprise版連携モジュールが含まれなくなった。CORBAモジュールも外された。[Java FXも取り除かれた](https://ja.wikipedia.org/wiki/JavaFX "wikilink")。

  - Dynamic class-file constants（invoke_dynamic拡張、動的ロードされたクラスへの定数ブートストラップ呼出）
  - [ラムダ式への型推論](https://ja.wikipedia.org/wiki/無名関数 "wikilink")
  - HTTPクライアント実装へのAPI
  - Flight recorder（Javaプログラム実行トレース用の軽快な各種データ収集フレームワーク）
  - Unicode 10.0.0のサポート
  - ガーベジコレクタ関連

## Java SE 12 (2019年3月19日)

JSR 386にて仕様規定。アップデートで令和改元に向けたセキュリティ対策が施された。

  - ガーベジコレクタ関連
  - switch文の拡張
  - JVM Constants API（主にクラスの動的ロードに関連した仮想マシン内の定数プールの操作）

## Java SE 13（2019年9月17日)

JSR 388にて仕様規定。「数百の小粒改良、数千のバグ修正」と宣伝された。

  - ソケットAPIの再実装
  - switch文の拡張
  - Text Blocks（文字列定義の複数行化）

## Java SE 14（2020年3月17日)

JSR 389にて仕様規定。

  - Recordクラス（メンバ変数不変でコンストラクタと標準メソッドが自動定義されるイミュータブルオブジェクト）
  - パターンマッチングinstanceof構文（if文のinstanceof判定で変数も同時定義できる糖衣構文）
  - switch文のcase結果値を代入式に組み込める糖衣構文
  - Text Blocks（文字列定義の複数行化）
  - Foreign-Memory Access API （仮想マシンヒープの外部メモリにも安全にアクセスできる）
  - Zガベージコレクタ

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
6.
7.
8.
9.
10.
11.
12.
13. [JSR 59](http://www.jcp.org/en/jsr/detail?id=59)
14.
15.
16.
17.
18.
19. [JSR 337: Java SE 8 Release Contents](http://jcp.org/en/jsr/detail?id=337)
20.
21. [JSR 383: Java™ SE 10 (18.3)](http://jcp.org/en/jsr/detail?id=383)
22. [JSR 384: JavaTM SE 11 (18.9)](http://jcp.org/en/jsr/detail?id=384)