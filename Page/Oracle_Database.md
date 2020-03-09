> この記事は[Oracle Database](https://ja.wikipedia.org/wiki/Oracle_Database)から翻訳されています。


**Oracle Database**（オラクル データベース）とは、[米国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink") (Oracle) が開発・販売している、[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS) のことである。Oracle Databaseは世界初の商用RDBMSであり、[メインフレーム](../Page/メインフレーム.md "wikilink")から[パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")まで、幅広い[プラットフォームをサポートしている](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。

## 以前のバージョン (Oracle Database 12c) における特徴

  - 行レベルロック
    ページ単位ではなく処理対象の行のみにロックをかけることにより、待ち時間の発生確率を低減している。また、ロックされた行に対する参照は可能であるため処理待ちが発生しない。
  - 読み取り一貫性
    [SELECTを発行した時点のデータが読み取れることを保障する機能](https://ja.wikipedia.org/wiki/SELECT_\(SQL\) "wikilink")。更新前のデータが格納されているUNDOセグメント（Oracle8iまではロールバックセグメント：一般的には[トランザクションログ](https://ja.wikipedia.org/wiki/トランザクションログ "wikilink")、更新前イメージともいう）を参照することで、排他ロックによるブロックを受けずにデータを読み取ることができる。
  - 堅牢性
    REDOログ（更新ログ・[ジャーナル](https://ja.wikipedia.org/wiki/ジャーナル "wikilink")ログ）のアーカイブとその冗長化、Real Application Clusters (RAC) に代表されるノード分散による運用構成の冗長化や、災害対策のためのデータベース遠隔複製機能（スタンバイデータベース・DataGuard）をもち、ダウンタイムの削減やデータ資産消失を防ぐことが可能である。
  - 移植性
    データベースエンジン・コア[API周りはすべて](../Page/アプリケーションプログラミングインタフェース.md "wikilink")[C言語](../Page/C言語.md "wikilink")、各種ツール類はほとんどがC言語または[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で記述されており、広い[プラットフォームでの移植性を誇る](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。ユーザの開発する[応用プログラムも](../Page/アプリケーションソフトウェア.md "wikilink")、C言語、[C++](../Page/C++.md "wikilink")、[COBOL](https://ja.wikipedia.org/wiki/COBOL "wikilink")、JavaまたWindowsでは[ODBC等の規格に対応し移植性は良い](https://ja.wikipedia.org/wiki/Open_Database_Connectivity "wikilink")。

## 他RDBMSとの互換性

[RDBMSのデファクトスタンダードとも位置づけられる製品であるが](../Page/関係データベース管理システム.md "wikilink")、古くからの仕様を引きずるあまり、標準SQL規格に準拠していない点が多く、他RDBMSとの移行性は良くない場合がある。他RDBMSとの移行の際に問題となりうる主な点には以下のようなものがある。

  - 可変長文字列において空文字列とNULLを区別しない。(正確には空文字列がNULLとして扱われる。例えば、以下の条件式は偽となる。)

<!-- end list -->

    ''=''

  - 比較演算子が通常の演算子としては認識されず、WHERE句の中でしか利用できない。
  - 表を必要としないSELECT文でも、必ず何らかの表（通常[DUAL表](https://ja.wikipedia.org/wiki/DUAL表 "wikilink")が用いられる）を参照するFROM句を書かなければならない。
  - テーブル名や列名、またその別名等に日本語などのマルチバイト文字を使用した場合必ず""で囲む必要があり、そうしないとSQLの動作が保障されず実際に異常な動作をすることが多い。プログラム言語内でSQL文字列を[ハードコーディング](https://ja.wikipedia.org/wiki/ハードコーディング "wikilink")する際に、""で囲むルールを徹底することは非常に困難である。そのためテーブル名、列名、別名等には英数字および一部の記号（_、$、\#）のみを使用することが推奨される。

## 歴史

[1977年](../Page/1977年.md "wikilink")、[ラリー・エリソン](https://ja.wikipedia.org/wiki/ラリー・エリソン "wikilink")、ボブ・マイナー、エド・オーツの3名により、Software Development Laboratories (SDL) が設立された。[1979年](../Page/1979年.md "wikilink")にSDLは、社名を Relational Software, Inc (RSI) に変更し、その際に初期の商用[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")として、Oracle V2を発表した。Oracle V2には、[トランザクション](https://ja.wikipedia.org/wiki/トランザクション "wikilink")の概念はなかったが、基本的な[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")である[SQL](../Page/SQL.md "wikilink")を使用することができた。

なお、OracleにVersion 1が存在しないのは、購買層に洗練されたデータベースであることを印象付けるための営業戦略であったといわれている。

[1983年](https://ja.wikipedia.org/wiki/1983年 "wikilink")、RSIが社名を変更し、Oracle Corporationになる。同年、Oracle version 3がリリースされるが、それは、旧バージョンをC言語により再プログラミングしたものであり、[コミット](https://ja.wikipedia.org/wiki/コミット "wikilink")や[ロールバック](https://ja.wikipedia.org/wiki/ロールバック "wikilink")といったトランザクションの概念をサポートしたものであった。このバージョンでは、使用可能な[プラットフォームを](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")[UNIX](../Page/UNIX.md "wikilink")まで拡張している。

[1984年](../Page/1984年.md "wikilink")にリリースされた Oracle 4は読み取り一貫性をサポートした。

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")、徐々に[ネットワークが進化していく中で](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")、[クライアントサーバモデル](https://ja.wikipedia.org/wiki/クライアントサーバモデル "wikilink")をサポートする。また、Oracle 5.0は、分散クエリーを搭載した。

[1988年](../Page/1988年.md "wikilink")、Oracleは[ERPの市場へ参加する](https://ja.wikipedia.org/wiki/企業資源計画 "wikilink")。[Oracle Financialsと呼ばれた製品は](https://ja.wikipedia.org/wiki/Oracle_Financials "wikilink")、これまでのOracle Databaseをもとに開発された。また、Oracle 6.0がリリースされ、[PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")や行レベルロックなどをサポートした。また、RACの前身であるシェアードエブリシング型のクラスタリングであるパラレルサーバがサポートされた。

[1992年](https://ja.wikipedia.org/wiki/1992年 "wikilink")、Oracle7 7.0がリリースされる。このバージョンにおいて、パラレルクエリー、完全制約性、[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")、[データベーストリガ](https://ja.wikipedia.org/wiki/データベーストリガ "wikilink")、データベースリンク、[レプリケーション](https://ja.wikipedia.org/wiki/レプリケーション "wikilink")などがサポートされた。最終バージョンは7.3.4である。

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")や[マルチメディア](../Page/マルチメディア.md "wikilink")に対応したOracle8 8.0がリリースされる。このバージョンにおいて、パーティショニング機能と新しいカラム型LOB (BLOB型,CLOB型) がサポートされた。またROWIDの仕様変更により大容量のデータをサポートするようになった。

[1999年](../Page/1999年.md "wikilink")には、[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")上での使用が高まる中、Oracle8i (R8.1.5 ～) をリリースした。このバージョンには、UNIX/[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")プラットフォームでも[インストーラの](https://ja.wikipedia.org/wiki/インストール#インストーラ "wikilink")[GUI化や](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、データベースエンジンに[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")を組み込んだ。データベースロケール（*i* は *Internet* の略とされている。）。最終バージョンは8.1.7である。

[2001年](../Page/2001年.md "wikilink")、[XMLの入出力など](../Page/Extensible_Markup_Language.md "wikilink")、400もの新しい特徴を有したOracle9i Databaseをリリースする。運用機能の最大の目玉は、パラレルサーバの後継機能として性能と安定性向上を実現したRAC (Real Application Clusters) である。最終バージョンは9.2.0.8となる。

[2003年](../Page/2003年.md "wikilink")、[グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink")を目指し、グリッド技術を応用したOracle Database 10gがリリースされた。（*g* は *Grid* の略とされている。）

[2007年](https://ja.wikipedia.org/wiki/2007年 "wikilink") Oracle Database 11gがリリースされた。

[2012年](../Page/2012年.md "wikilink") 10月1日、サンフランシスコで開催された「Oracle OpenWorld 2012」にて、米Oracleは2013年にマルチテナントデータベース製品「Oracle Database 12c」をリリース予定と発表した。（*c* は *Cloud（クラウド）* の略とされている。）

[2013年](../Page/2013年.md "wikilink") Oracle Database 12cがリリースされた

## 製品群

2015年1月時点では、国内最新リリースとして Oracle Database 12c Release 1(12.1.0.2)が提供されている。

  - Oracle RDBMS V6
      - 主要な機能拡張：行レベル・ロック、オンラインバックアップ（アーカイブログ機構）、[PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")（無名ブロックのみ）
  - Oracle7 Server (7.0.x, 7.1.x, 7.2.x)
      - 主要な機能拡張：[クライアント・サーバ](https://ja.wikipedia.org/wiki/クライアント・サーバ "wikilink")対応 (SQL\*Net)、[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")・[トリガー](https://ja.wikipedia.org/wiki/トリガー "wikilink")の実装、[参照整合性](https://ja.wikipedia.org/wiki/参照整合性 "wikilink")制約の実装
  - Oracle7 Server (7.3.1 - 7.3.4.5)
      - 主要な機能拡張：[データウェアハウス](../Page/データウェアハウス.md "wikilink")向け機能の実装（ハッシュ結合、ビットマップ索引）、パラレルクエリーによる大規模テーブル検索の高速化、レプリケーション、スタンバイデータベース
  - Oracle8 Server (8.0.3 - 8.0.6.3)
      - 主要な機能拡張：パーティショニングテーブル、Parallel Server（シェアードディスク型のハイパフォーマンス型クラスタリング）、[マルチメディア](../Page/マルチメディア.md "wikilink")対応（ビデオ・空間データ）、全文検索機能 (Oracle\*Context)、LOB型カラムの追加、[オブジェクト関係データベース](https://ja.wikipedia.org/wiki/オブジェクト関係データベース "wikilink")機能（オブジェクト型）の導入
  - Oracle8i Database (8.1.5 - 8.1.7.4)
      - 主要な機能拡張：JServer/OracleJVM（DBサーバプロセス内で稼動する[Java仮想マシン](../Page/Java仮想マシン.md "wikilink")環境）、[マテリアライズドビュー](https://ja.wikipedia.org/wiki/マテリアライズドビュー "wikilink")、各種グラフィカルユーザインタフェースツール（GUIツール）・インストーラの[Javaアプリケーション](https://ja.wikipedia.org/wiki/Javaアプリケーション "wikilink")化、[XML対応](../Page/Extensible_Markup_Language.md "wikilink") (Oracle XDK)
  - Oracle9i Database (9.0.1.1 - 9.0.1.4, 9.2.0.1 - 9.2.0.8)
      - 主要な機能拡張：領域管理の自動化、[XMLデータベース](https://ja.wikipedia.org/wiki/XMLデータベース "wikilink")機能（XMLType型カラム、DBUri）、[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")/[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") [SQL](../Page/SQL.md "wikilink"):1999 準拠構文サポート、[クラスタの機能強化](../Page/コンピュータ・クラスター.md "wikilink")　(Parallel Server → Real Application Clusters「RAC」)、DataGuard、削除したデータの[リカバリ](https://ja.wikipedia.org/wiki/リカバリ "wikilink")ができるフラッシュバッククエリー機能
  - Oracle Database 10g (10.1.0.2 - 10.1.0.5, 10.2.0.1 - 10.2.0.5)
      - 主要な機能拡張：RAC構成ノード間での動的負荷分散運用の実現（RACへのGrid技術導入）、ストレージ管理の自動化 (ASM)、情報統合 ([EII](https://ja.wikipedia.org/wiki/EII "wikilink")) 機能の強化 (OTG、OGC)、削除した表の[リカバリ](https://ja.wikipedia.org/wiki/リカバリ "wikilink")ができるフラッシュバック機能
  - Oracle Database 11g (11.1.0.6 - 11.1.0.7, 11.2.0.1 -)
      - 性能チューニングやバックアップ・リカバリなどの運用管理の自動化、災害対策機能の強化、非構造化データの処理性能向上、グリッド機能の向上
  - Oracle Database 12c （12.1.0.1 - ）
      - クラウドで有効な「マルチテナント」機能の搭載。

### リリースとバージョン

Oracleデータベース製品名は、リリース番号および接尾辞による命名規則に従って命名される。現在の最新リリースのOracle Database 18cの 「c」 は、「Cloud」を表わす。 以前のリリース（Oracle Database 10gおよびOracle9i Databaseなど）では、それぞれ「Grid」および「Internet」のを表す「g」および「i」の接尾辞を使用していた。 接尾辞の採用はOracle8i Database以降で、それより前のOracle Databaseの命名規則に接尾辞は存在しない。 オラクル創業者[ラリー・エリソン](https://ja.wikipedia.org/wiki/ラリー・エリソン "wikilink")が「バージョン1を購入したい者はいない」と考えたため、Oracle Databaseのv1は存在しない。 \[1\] Oracleの[RDBMSリリース番号は](../Page/関係データベース管理システム.md "wikilink")、下記のコードを使用している。

<table>
<thead>
<tr class="header">
<th><p>Oracle<br />
Database<br />
バージョン</p></th>
<th><p>初版</p></th>
<th><p>初版<br />
リリース</p></th>
<th><p>最終PSR</p></th>
<th><p>最終<br />
PSR<br />
リリース</p></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>2.3</p></td>
<td><p>1979年</p></td>
<td></td>
<td></td>
<td><p>最初の市販のSQLベースのRDBMS</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>3.1.3</p></td>
<td><p>1983年</p></td>
<td></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/並行性制御" title="wikilink">同時実行制御</a>、データ分散、および<a href="https://ja.wikipedia.org/wiki/スケーラビリティ" title="wikilink">スケーラビリティ</a></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>4.1.4.0</p></td>
<td><p>1984年</p></td>
<td><p>4.1.4.4</p></td>
<td></td>
<td><p>マルチバージョン読み取り一貫性</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>5.0.22 (5.1.17)</p></td>
<td><p>1985年</p></td>
<td><p>5.1.22</p></td>
<td></td>
<td><p><a href="https://ja.wikipedia.org/wiki/クライアントサーバモデル" title="wikilink">クライアントサーバモデル</a>と<a href="https://ja.wikipedia.org/wiki/分散データベース" title="wikilink">分散データベース</a>のサポート</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>6.0.17</p></td>
<td><p>1988年</p></td>
<td><p>6.0.37</p></td>
<td></td>
<td><p>行レベルのロック、スケーラビリティ、オンラインバックアップリカバリ、<a href="https://ja.wikipedia.org/wiki/PL/SQL" title="wikilink">PL/SQL</a></p></td>
</tr>
<tr class="even">
<td></td>
<td><p>6.2.0</p></td>
<td></td>
<td></td>
<td></td>
<td><p>Oracle Parallel Server</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>7.0.12</p></td>
<td><p>1992年6月</p></td>
<td></td>
<td></td>
<td><p>PL/SQLストアドプロシージャ、トリガ、分散2フェーズコミット、共有カーソル、コストベース最適化</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>7.1.0</p></td>
<td><p>1994年5月</p></td>
<td></td>
<td></td>
<td><p>SQL並列実行</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>7.2.0</p></td>
<td><p>1995年5月</p></td>
<td></td>
<td></td>
<td><p>共有サーバー、XAトランザクション、透過的アプリケーションフェイルオーバー</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>7.3.0</p></td>
<td><p>1996年2月</p></td>
<td><p>7.3.4</p></td>
<td></td>
<td><p>オブジェクトリレーショナルデータベース</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>8.0.3</p></td>
<td><p>1997年6月</p></td>
<td><p>8.0.6</p></td>
<td></td>
<td><p>リカバリマネージャ、パーティショニング</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>8.1.5.0</p></td>
<td><p>1998年</p></td>
<td><p>8.1.7.4</p></td>
<td><p>2000年8月</p></td>
<td><p>ネイティブインターネットプロトコルとJava、Virtual Private Database（VPD）</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>9.0.1.0</p></td>
<td><p>2001年</p></td>
<td><p>9.0.1.5</p></td>
<td><p>2003年12月</p></td>
<td><p>、Oracle XML DB</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>9.2.0.1</p></td>
<td></td>
<td><p>9.2.0.8</p></td>
<td><p>2007年4月</p></td>
<td><p>、、ストリーム、ロジカル・スタンバイ</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>10.1.0.2</p></td>
<td><p>2003年</p></td>
<td><p>10.1.0.5</p></td>
<td><p>2006年2月</p></td>
<td><p>自動データベース管理、自動データベース診断モニター、グリッド・インフラストラクチャ、Oracle ASM、フラッシュバック・データベース</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>10.2.0.1</p></td>
<td><p>2005年7月 [2]</p></td>
<td><p>10.2.0.5</p></td>
<td><p>2010年4月</p></td>
<td><p>Real Application Testing、Database Vault、インデックスのオンライン作成、高度な圧縮、Data Guardファスト・スタート・フェイルオーバー、透過的データベース暗号化（TDE）</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>11.1.0.6</p></td>
<td><p>2007年9月</p></td>
<td><p>11.1.0.7</p></td>
<td><p>2008年9月</p></td>
<td><p>、SecureFiles、Exadata、</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>11.2.0.1</p></td>
<td><p>2009年9月 [3]</p></td>
<td><p>11.2.0.4</p></td>
<td><p>2013年8月</p></td>
<td><p>エディションベースの再定義、データ修正、ハイブリッド列圧縮、クラスタファイルシステム、GoldenGateレプリケーション、</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>12.1.0.1</p></td>
<td><p>2013年7月 [4]</p></td>
<td><p>12.1.0.2</p></td>
<td><p>2014年7月</p></td>
<td><p>マルチテナント・アーキテクチャ、インメモリ列ストア、<a href="https://ja.wikipedia.org/wiki/JavaScript_Object_Notation" title="wikilink">JSONのネイティブサポート</a>、SQLパターン・マッチング、データベースクラウドサービス</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>12.2.0.1</p></td>
<td><p>2016年9月 (クラウド版) 2017年3月 (オンプレミス版)</p></td>
<td></td>
<td></td>
<td><p>シャーディングのネイティブサポート、ゼロ・データロス・リカバリ・アプライアンス、Exadata Cloud Service、Cloud at Customer</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>18.1.0</p></td>
<td><p>2018年2月 (クラウド版: 18.1.0) 2018年7月 (オンプレミス版: 18.3.0)</p></td>
<td></td>
<td></td>
<td><p>Polymorphic Table Function、Active Directoryとの統合</p></td>
</tr>
<tr class="even">
<td><p><small></small></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

[Oracle Database Administrators Guide](https://docs.oracle.com/en/database/oracle/oracle-database/12.2/cncpt/introduction-to-oracle-database.html#GUID-43F9DD5C-8D8C-4E61-A2B4-5C05907D3CEC)には、Oracle Databaseの各メジャーリリースで導入されたいくつかの主要な革新的技術の簡単な歴史が記載されています。

## 関連製品

  - Oracle Database Lite ： [PDA等の極小リソースでも稼動するモバイルデータベース](../Page/携帯情報端末.md "wikilink")。実際のデータはOracle Databaseに格納されている。
  - [Oracle Application Server](https://ja.wikipedia.org/wiki/Oracle_Application_Server "wikilink") ： [Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") に準拠した[ウェブアプリケーションサーバ](https://ja.wikipedia.org/wiki/アプリケーションサーバ "wikilink")。Webサーバについては[Apache](https://ja.wikipedia.org/wiki/Apache "wikilink")をOracleが改良したものである。
      - 中核となる Java EE コンテナのOC4J(Oracle Containers for Java)は、[Orion Application Serverをベースとしている](https://ja.wikipedia.org/wiki/Orion_Application_Server "wikilink")。
  - Oracle Developer ： ウェブに対応したOracle独自の[4GL](https://ja.wikipedia.org/wiki/4GL "wikilink")アプリケーション開発・実行環境 (Forms/Reports)
  - Oracle Designer ： [リポジトリ](https://ja.wikipedia.org/wiki/リポジトリ "wikilink")ベースの統合[CASE環境](https://ja.wikipedia.org/wiki/Computer_Aided_Software_Engineering "wikilink")
  - Oracle [E-Business Suite](https://ja.wikipedia.org/wiki/E-Business_Suite "wikilink") (旧名:Oracle Applications) ： Oracle Database実行環境とForms/Reports環境をベースとした、ウェブ対応の[ERP製品群](https://ja.wikipedia.org/wiki/企業資源計画 "wikilink")
  - [Oracle JDeveloper](https://ja.wikipedia.org/wiki/Oracle_JDeveloper "wikilink") ： [Java](https://ja.wikipedia.org/wiki/Java "wikilink")/[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")開発のための[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE)
  - [Oracle Application Express](https://ja.wikipedia.org/wiki/Oracle_Application_Express "wikilink") ： ブラウザで作るブラウザウェブアプリケーション開発ツール
  - [Oracle Collaboration Suite](https://ja.wikipedia.org/wiki/Oracle_Collaboration_Suite "wikilink") ： [グループウェア](../Page/グループウェア.md "wikilink")、ファイルサーバ
  - Oracle Content Management SDK
  - [Oracle Identity Management](https://ja.wikipedia.org/wiki/Oracle_Identity_Management "wikilink")
  - [Oracle OLAP Server](https://ja.wikipedia.org/wiki/Oracle_OLAP_Server "wikilink") ： H-OLAP (R-OLAPとM-OLAPのハイブリッド型[OLAP](https://ja.wikipedia.org/wiki/OLAP "wikilink")) サーバ。
  - [Oracle BPEL Process Manager](https://ja.wikipedia.org/wiki/Oracle_BPEL_Process_Manager "wikilink")　ビジネスプロセスモデリング製品
  - [Oracle Secure Enterprise Search](https://ja.wikipedia.org/wiki/Oracle_Secure_Enterprise_Search "wikilink") ： 企業内コンテンツを検索する製品。ユーザアクセス権限を制御しながらgoogleのようなことができる。
  - [Oracle TimesTen In-Memory Database](https://ja.wikipedia.org/wiki/Oracle_TimesTen_In-Memory_Database "wikilink") インメモリデータベース

## 他の管理ツール

  - [Navicat for Oracle](https://jp.navicat.com/products/navicat-for-oracle)

## 競合製品

Oracle Databaseは大企業向けの市場で高いシェアを誇っているが、近年は他ベンダーが提供するRDB製品も多機能化、高速化が進んでおり、競争が激化している。Oracle Databaseの主要な競合製品には以下の製品がある。

  - [Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") : 米マイクロソフトのRDB製品。価格がOracle Databaseより比較的安価であるため、主に中小企業向けに出荷されてきたが、他のマイクロソフト製品との連動を武器に大手企業での実績も増えている。
  - [SAP HANA](https://ja.wikipedia.org/wiki/SAP_HANA "wikilink") : ヨーロッパ最大級のソフトウェア企業SAPのデータベース製品。高速なインメモリーデータベースに分類されるが、基幹系システムや情報系システムのプラットフォームとして、Oracle Databaseをはじめとした従来のRDB製品からSAP HANAにリプレースする企業が急速に増えている。
  - [SAP Sybase Adaptive Server Enterprise](https://ja.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink") : 証券や銀行で多く採用されているRDB製品。Sybase社が提供していたが、SAPがSybaseを買収したことでSAPの製品ラインナップに加わり、金融機関向けでOracle Databaseと熾烈な競争を繰り広げている。
  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink") : 競合ベンダーの製品ではなく、[オープンソースデータベースであるが](https://ja.wikipedia.org/wiki/オープンソースソフトウェア "wikilink")、近年機能が大幅に拡充され、Oracle Databaseの主要な競合製品として台頭している。

## 「SCOTT/TIGER」の由来

**Oracle Database**に付属するdemobld.sql（Oracle Database 10g以降ではutlsampl.sql）を実行すると「EMP」「DEPT」というふたつのテーブルと「SCOTT/TIGER」という[スキーマ](https://ja.wikipedia.org/wiki/スキーマ "wikilink")よりなる伝統的なデモ環境が構築される。「SCOTT」とはオラクルの前身であるSDLに在籍していたBruce Scottを指し、「Tiger」は彼の愛猫の名前に由来する。Scottは優秀な開発者であり最初期の[SQL\*Plus](https://ja.wikipedia.org/wiki/SQL*Plus "wikilink")も彼の手によるものとされている。Scottはすでにオラクルを後にしているが、この伝統は変わる様子がない。

## Oracleは「高価」で「難しい」

Oracleは高機能である反面、システムや操作方法を理解するのが非常に困難であり、[ユーザビリティ](https://ja.wikipedia.org/wiki/ユーザビリティ "wikilink")も低い（[CUIによる操作がメインである](../Page/キャラクタユーザインタフェース.md "wikilink")。Oracle Enterprise Managerで[GUIの操作も可能となっているが](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")、CUIによる操作と比較すると限定される）ため、開発・運用がとても難しいと思われている。また、大規模のシステムを構築するには必要不可欠となるOracle Database Enterprise Editionの価格は1プロセッサ（CPU）当たり570万円とかなり高額である。さらに、大規模システムでは各オプション機能(パーティショニング、DataGuard、RAC等)も高価で他社DBの製品自体のライセンス価格に匹敵するものも多い。\[5\] こうしたことから、Oracleは「高飛車である」「高くて難しい」というイメージを持たれていると、日本オラクルのクロスインダストリー統括本部長が明かしている。特にその導入コストを嫌って、こと中小企業での導入率が芳しくないという。\[6\]

過去には日本オラクルは、こうしたイメージを払拭し、中小企業にもOracleを売り込むために、「高くて難しい」といったイメージを[都市伝説](https://ja.wikipedia.org/wiki/都市伝説 "wikilink")と定義して中小企業向けのアピールを強化していた。\[7\]

しかし、2016年2月29日にOracle standard Edition One / 696,000円 最大CPU:2ソケット、Oracle standard Edition / 2,100,000円 最大CPU:4ソケット の販売が終わり、翌3月1日から Oracle standard Edition 2 / 2,100,000円 最大CPU:2ソケット に統一されたため、Oracleを使う中小企業は少なくなるものと想像される。\[8\]

## サポート契約

サポート契約を結んだユーザー以外に対しては、製品にどれだけ重大な[バグ](https://ja.wikipedia.org/wiki/バグ "wikilink")や[セキュリティホール](../Page/セキュリティホール.md "wikilink")などの不具合があろうとも、[修正パッチの提供はもちろんのことバグ情報の公開も行わない](https://ja.wikipedia.org/wiki/パッチ "wikilink")。

また、オラクル社とのサポート契約は基本的に製品購入当時より締結し続けなければならないものとされており、サポート契約を一旦[解約した後に再契約しようとする場合は](https://ja.wikipedia.org/wiki/解除 "wikilink")、前回解約時点にまで遡及する形になる。つまり、解約時点までに遡り（解約後から再契約までの間に）サポート契約を締結していた場合に発生していたはずの金額に加えて、プレミアムを加えた額を全額オラクル社に納めなければ再契約できない。そのため場合によっては新規に製品を買い直す方が安価になることが多い。サポートサービス費用が年々値上がりしていくようになっている。

こうしたことから、サポート契約は必須である（解約そのものは可能であるが、解約による弊害が非常に大きく、製品を使い続けるためには解約が不可能に近い）と言える。またサポート契約の締結の有無が原則としてシステム単位でなく企業単位に変更されており、一部のシステムだけ契約を締結することができなくなった。\[9\]

## 脚注

## 関連項目

  - [PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")
      -
        オラクルが**Oracle Database**の為に開発した[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")。「[SQL](../Page/SQL.md "wikilink")を[手続き型に拡張したもの](https://ja.wikipedia.org/wiki/手続き型言語 "wikilink")」とされている。処理を[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")の[プログラムとして](../Page/プログラム_\(コンピュータ\).md "wikilink")、データベースに格納できる点も特徴のひとつである。
  - [オラクルマスター](https://ja.wikipedia.org/wiki/オラクルマスター "wikilink")
      -
        **Oracle Database**技術者の認定資格。Oracle社が主催する[オラクル認定試験](https://ja.wikipedia.org/wiki/オラクル認定試験 "wikilink")により取得することができる。
  - [オラクル (企業)](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")
      -
        **Oracle Database**の開発、販売を行う企業。米国[カリフォルニア州](../Page/カリフォルニア州.md "wikilink")に本拠を置く。
  - [日本オラクル](https://ja.wikipedia.org/wiki/日本オラクル "wikilink")
      -
        オラクルの日本法人。製品の販売やサポート、コンサルティングを行う。
  - 内部構造
      - [システムグローバル領域](https://ja.wikipedia.org/wiki/システムグローバル領域 "wikilink")
      - [バックグラウンドプロセス (Oracle Database)](https://ja.wikipedia.org/wiki/バックグラウンドプロセス_\(Oracle_Database\) "wikilink")
      - [ファイル (Oracle Database)](https://ja.wikipedia.org/wiki/ファイル_\(Oracle_Database\) "wikilink")

## 外部リンク

  - [Oracle Technology Network (OTN) Japan](http://www.oracle.com/technetwork/jp/index.html)
  - [Oracle Corporation](http://www.oracle.com/jp/index.html)
  - [shift the oracle](http://www.shift-the-oracle.com/)

[Category:関係データベース管理システム](https://ja.wikipedia.org/wiki/Category:関係データベース管理システム "wikilink") [Category:オラクル](https://ja.wikipedia.org/wiki/Category:オラクル "wikilink") [Category:1979年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1979年のソフトウェア "wikilink")

1.
2.  <http://www.oracle.com/us/corporate/press/017324_EN>
3.  <http://www.oracle.com/us/corporate/press/032365>
4.  <http://www.oracle.com/us/corporate/press/1967380>
5.  [Oracle 価格表 - 日本オラクル](http://www.oracle.com/jp/corporate/pricing/price/index.html)
6.  [「高い、難しい」イメージの転換を図るオラクル](http://enterprise.watch.impress.co.jp/cda/topic/2004/09/17/3405.html) - Enterprise Watch
7.
8.
9.