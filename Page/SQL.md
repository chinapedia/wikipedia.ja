> この記事は[SQL](https://ja.wikipedia.org/wiki/SQL)から翻訳されています。


**SQL**（エスキューエル\[1\]、シークェル\[2\]、シーケル\[3\]）は、[関係データベース管理システム](https://ja.wikipedia.org/wiki/関係データベース管理システム "wikilink") (RDBMS) において、データの操作や定義を行うための[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")（[問い合わせ言語](https://ja.wikipedia.org/wiki/問い合わせ言語 "wikilink")）、[ドメイン固有言語](https://ja.wikipedia.org/wiki/ドメイン固有言語 "wikilink")である。プログラミングにおいてデータベースへのアクセスのために、[プログラミング言語](../Page/プログラミング言語.md "wikilink")と併用されるが、**SQLそのものはプログラミング言語ではない。**理論上は[チューリング完全](https://ja.wikipedia.org/wiki/チューリング完全 "wikilink")ではないため、ユーザーが通常の方法で行える事は読み書きしたいデータの条件を宣言するのみである。

SQLが使われるRDBは非常に良く「[エドガー・F・コッド](../Page/エドガー・F・コッド.md "wikilink")によって考案された[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")の[関係モデル](https://ja.wikipedia.org/wiki/関係モデル "wikilink")における演算体系である、[関係代数と](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\) "wikilink")[関係論理](https://ja.wikipedia.org/wiki/関係論理 "wikilink")（関係計算）に基づいている」と宣伝されている。しかし、SQLについては、そのコッド自身をはじめ他からも、関係代数と関係論理にきちんと準拠していないとして批判されてはいる（[The Third Manifesto](https://ja.wikipedia.org/wiki/The_Third_Manifesto "wikilink") - [クリス・デイト](https://ja.wikipedia.org/wiki/クリス・デイト "wikilink")、[ヒュー・ダーウェン](https://ja.wikipedia.org/wiki/ヒュー・ダーウェン "wikilink")）。

[国際標準](https://ja.wikipedia.org/wiki/国際標準 "wikilink")の規格票内では「**SQL**は何かの略語ではない」と言明がある。また、発音としては *シークェル*  と読まれることもある。これは、SQLの元となったデータベース言語が、IBMが開発したRDBMSの実験[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")である[System Rの操作言語](https://ja.wikipedia.org/wiki/System_R "wikilink")「」\[4\]であったことにもちなんでいる。

## 標準SQL規格

SQL規格は1986年に統一標準規格が発表されるまでは、その統一標準規格が存在しない状況であった。そのため、各[関係データベース管理システム](https://ja.wikipedia.org/wiki/関係データベース管理システム "wikilink") (RDBMS) ベンダーごとにさまざまな拡張がなされてきた。

近年になって[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")、後に[ISOで言語仕様の標準化が行われており](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、制定された年ごとにSQL86、SQL89、SQL92、[SQL:1999](https://ja.wikipedia.org/wiki/SQL:1999 "wikilink")、[SQL:2003](https://ja.wikipedia.org/wiki/SQL:2003 "wikilink")、SQL:2006、[SQL:2008](https://ja.wikipedia.org/wiki/SQL:2008 "wikilink")、SQL:2011などの規格があるが、対応の程度はベンダーごとにバラバラである。これは標準SQL策定に時間がかかりすぎたことにより、ビジネスの現状から早期の機能拡張が迫られたベンダーの都合と、独自構文を頻繁に利用していた利用者およびプログラマーに対し、互換性保持を保証する必要もあったためである。

そして1986年に統一標準規格が発表されて以来非常に多くの改正が行われた。制定年度順に代表的な規格を以下に挙げる。

<table>
<thead>
<tr class="header">
<th><p>年</p></th>
<th><p>規格名称</p></th>
<th><p>別称</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1986年</p></td>
<td><p>SQL86</p></td>
<td><p>SQL87</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/ANSI" title="wikilink">ANSI</a>によって発表された最初の規約。1987年に<a href="https://ja.wikipedia.org/wiki/国際標準化機構" title="wikilink">ISOによって批准された</a>。</p>
<ul>
<li><a href="https://ja.wikipedia.org/wiki/データ操作言語" title="wikilink">データ操作言語</a> (DML) 仕様策定: <a href="https://ja.wikipedia.org/wiki/COBOL" title="wikilink">COBOL</a>、<a href="../Page/FORTRAN.md" title="wikilink">FORTRAN</a>、<a href="https://ja.wikipedia.org/wiki/PL/I" title="wikilink">PL/I</a>など、親言語（母言語、ホスト言語とも言う）への<a href="https://ja.wikipedia.org/wiki/埋め込みSQL" title="wikilink">埋込みSQL文仕様策定</a></li>
</ul></td>
</tr>
<tr class="even">
<td><p>1989年</p></td>
<td><p>SQL89</p></td>
<td><p> </p></td>
<td><p>マイナーバージョン。</p>
<ul>
<li><a href="https://ja.wikipedia.org/wiki/データ定義言語" title="wikilink">データ定義言語</a> (DDL) 仕様策定 （<a href="https://ja.wikipedia.org/wiki/CREATE_(SQL)" title="wikilink">CREATE</a> TABLE文、CREATE <a href="https://ja.wikipedia.org/wiki/ビュー_(データベース)" title="wikilink">VIEW文</a>、GRANT文。ただし、<a href="https://ja.wikipedia.org/wiki/DROP_(SQL)" title="wikilink">DROP文</a>、<a href="https://ja.wikipedia.org/wiki/ALTER_(SQL)" title="wikilink">ALTER文</a>、REVOKE文はなし）</li>
<li>制約および整合性機能を追加 （DEFAULT、<a href="https://ja.wikipedia.org/wiki/一意性制約" title="wikilink">UNIQUE制約</a>、<a href="https://ja.wikipedia.org/wiki/NOT_NULL制約" title="wikilink">NOT NULL制約</a>、<a href="https://ja.wikipedia.org/wiki/主キー" title="wikilink">PRIMARY KEY制約</a>、<a href="https://ja.wikipedia.org/wiki/CHECK制約" title="wikilink">CHECK制約</a>、<a href="https://ja.wikipedia.org/wiki/参照整合性" title="wikilink">参照整合性</a>制約）</li>
<li><a href="../Page/C言語.md" title="wikilink">C言語</a>への埋込みSQL文仕様の追加</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>1992</p></td>
<td></td>
<td><p>SQL2</p></td>
<td><p>メジャーバージョン</p>
<ul>
<li><a href="https://ja.wikipedia.org/wiki/直交性_(情報科学)" title="wikilink">直交性の改善</a> （表式）</li>
<li><a href="https://ja.wikipedia.org/wiki/データ型" title="wikilink">データ型</a>の拡張 （可変長文字列、ビット、<a href="https://ja.wikipedia.org/wiki/文字集合" title="wikilink">文字集合</a>、日付・時刻・時間間隔 (DATE、TIME、TIMESTAMP、INTERVAL)）</li>
<li><a href="https://ja.wikipedia.org/wiki/関係代数_(関係モデル)#外結合" title="wikilink">外部結合</a> (OUTER JOIN)</li>
<li><a href="https://ja.wikipedia.org/wiki/定義域_(データベース)" title="wikilink">定義域</a> (DOMAIN)</li>
<li><a href="https://ja.wikipedia.org/wiki/表明" title="wikilink">表明</a> (ASSERTION)</li>
<li>一時表 （TEMPORARY TABLE: <a href="https://ja.wikipedia.org/wiki/永続化" title="wikilink">永続化</a>しないデータを格納）</li>
<li>DDL仕様追加 （<a href="https://ja.wikipedia.org/wiki/DROP_(SQL)" title="wikilink">DROP文</a>、<a href="https://ja.wikipedia.org/wiki/ALTER_(SQL)" title="wikilink">ALTER文</a>）</li>
<li>動的SQL仕様</li>
<li>前方・後方スクロール可能な<a href="https://ja.wikipedia.org/wiki/カーソル_(データベース)" title="wikilink">カーソルサポート</a></li>
<li><a href="https://ja.wikipedia.org/wiki/クライアントサーバモデル" title="wikilink">クライアント/サーバシステムのためのCONNECT</a>/DISCONNECT文</li>
</ul></td>
</tr>
<tr class="even">
<td><p>1995年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/SQL/CLI" title="wikilink">SQL/CLI</a></p></td>
<td><p> </p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Call_Level_Interface" title="wikilink">コールレベルインターフェース</a> (Call Level Interface)<br />
業界標準になった <a href="https://ja.wikipedia.org/wiki/Open_Database_Connectivity" title="wikilink">ODBC</a> <a href="../Page/アプリケーションプログラミングインタフェース.md" title="wikilink">API</a> のインタフェースに相当する機能を国際標準化した規格</p></td>
</tr>
<tr class="odd">
<td><p>1996年</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/SQL/PSM" title="wikilink">SQL/PSM</a></p></td>
<td><p> </p></td>
<td><p>永続格納モジュール (Persistent Storage Module)<br />
一般的に<a href="https://ja.wikipedia.org/wiki/ストアドプロシージャ" title="wikilink">ストアドプロシージャ</a>と呼ばれる機能を国際標準化した規格</p></td>
</tr>
<tr class="even">
<td><p>1999年</p></td>
<td><p><br />
(SQL99)</p></td>
<td><p>SQL3</p></td>
<td><p>RDBMSのための完全な言語になることを目指した仕様。</p>
<ul>
<li><a href="../Page/正規表現.md" title="wikilink">正規表現</a>による値照合</li>
<li>共通表式(WITH句)</li>
<li><a href="https://ja.wikipedia.org/wiki/再帰クエリ" title="wikilink">再帰クエリ</a></li>
<li><a href="https://ja.wikipedia.org/wiki/OLAP" title="wikilink">OLAP</a> (ROLLUP、CUBE、GROUPING SETS)</li>
<li><a href="https://ja.wikipedia.org/wiki/関係代数_(関係モデル)#和" title="wikilink">ユニオン (UNION)</a>・結合経由の更新</li>
<li>カーソル操作の機能強化 （トランザクション完了後のオープン状態保持）・ユーザ定義権限 (ROLE)・トランザクション管理の新機能 (<a href="https://ja.wikipedia.org/wiki/SAVEPOINT_(SQL)" title="wikilink">SAVEPOINT</a>)</li>
<li>SQL/<a href="https://ja.wikipedia.org/wiki/ストアドプロシージャ" title="wikilink">PSM強化</a> （<a href="https://ja.wikipedia.org/wiki/制御構造" title="wikilink">制御構文</a> （<a href="https://ja.wikipedia.org/wiki/if文" title="wikilink">IF</a> 、<a href="https://ja.wikipedia.org/wiki/while文" title="wikilink">WHILEなど</a>） サポートなど）</li>
<li><a href="https://ja.wikipedia.org/wiki/SQLJ" title="wikilink">SQLJ</a> （<a href="https://ja.wikipedia.org/wiki/Java" title="wikilink">Java</a>を親言語とする埋め込みSQL規格）</li>
<li><a href="https://ja.wikipedia.org/wiki/データベーストリガ" title="wikilink">データベーストリガ</a></li>
<li>ユーザ定義関数 （ストアドファンクション）</li>
<li>非スカラー型の新しい<a href="https://ja.wikipedia.org/wiki/データ型" title="wikilink">データ型</a>: <a href="https://ja.wikipedia.org/wiki/真理値" title="wikilink">真理値</a> (BOOLEAN) 型と<a href="https://ja.wikipedia.org/wiki/配列" title="wikilink">配列</a> (ARRAY) 型、LOB (Large Object)、ユーザ定義型、構造型</li>
<li>上位表と下位表 （スーパーテーブルとサブテーブル）</li>
<li><a href="../Page/オブジェクト指向.md" title="wikilink">オブジェクト指向</a>の考え方を取り入れた<a href="https://ja.wikipedia.org/wiki/オブジェクト関係データベース" title="wikilink">オブジェクト関係データベース</a>技術 (ORDB)。配列型やユーザ定義型、ユーザ定義関数と上位表/下位表仕様により実現されている。</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2003年</p></td>
<td></td>
<td><p> </p></td>
<td><ul>
<li><strong>SQL/MM</strong> （マルチメディア: フレームワーク、<a href="../Page/全文検索.md" title="wikilink">全文検索</a>、空間データ (Spatial)、静止画像）</li>
<li><strong>SQL/MED</strong> （外部データ管理: 非関係データ （<a href="https://ja.wikipedia.org/wiki/順編成ファイル" title="wikilink">順編成ファイル</a>や<a href="https://ja.wikipedia.org/wiki/階層型データベース" title="wikilink">階層型データベース</a>など） や他社の関係データをSQLでアクセスするための規格）</li>
<li><strong>SQL/OLB</strong> （オブジェクト<a href="https://ja.wikipedia.org/wiki/言語バインディング" title="wikilink">言語バインディング</a>: <a href="https://ja.wikipedia.org/wiki/SQLJ" title="wikilink">SQLJ</a>を標準化する。<a href="https://ja.wikipedia.org/wiki/Java" title="wikilink">Java</a>プログラムに埋め込むSQL文）</li>
<li><a href="../Page/Extensible_Markup_Language.md" title="wikilink">XML関連の機能</a></li>
<li><a href="https://ja.wikipedia.org/wiki/ウィンドウ関数" title="wikilink">ウィンドウ関数</a></li>
<li>順序（シーケンス）の標準化と識別キー列に対する値の自動生成を行う列仕様の導入 （ID型）</li>
</ul>
<p>(See <a href="https://sigmodrecord.org/publications/sigmodRecord/0403/E.JimAndrew-standard.pdf">Eisenberg et al.: <em>SQL:2003 Has Been Published</em></a>.)</p></td>
</tr>
<tr class="even">
<td><p>2008年</p></td>
<td></td>
<td><p> </p></td>
<td><ul>
<li>INSTEAD OF <a href="https://ja.wikipedia.org/wiki/データベーストリガ" title="wikilink">トリガ</a></li>
<li><a href="https://ja.wikipedia.org/wiki/TRUNCATE_(SQL)" title="wikilink">TRUNCATE TABLE</a> ステートメント</li>
<li><a href="https://ja.wikipedia.org/wiki/配列" title="wikilink">配列</a>型の集約と展開 (array_agg, unnest) [5]</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>2011年</p></td>
<td></td>
<td><p> </p></td>
<td></td>
</tr>
<tr class="even">
<td><p>2016年</p></td>
<td></td>
<td><p> </p></td>
<td></td>
</tr>
</tbody>
</table>

## SQLとオンライン処理

SQLはその性質上、「宣言型」の言語である。**[プログラミング言語](../Page/プログラミング言語.md "wikilink")ではない。**

### SQLとプログラミング言語

SQL自体はプログラミング言語ではない。プログラミング言語から関係データベースを操作するための方法として、SQLが関係するものや関係しないものがあり、以下にそれらを述べる。

手続き型プログラミング言語、あるいは手続き型ではないプログラミング言語から[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")を操作するため、[ソースコード](../Page/ソースコード.md "wikilink")中にSQLを埋め込み、[プリプロセッサ](https://ja.wikipedia.org/wiki/プリプロセッサ "wikilink")によってSQL部分を変換してデータベースアプリケーションを開発する方式がある。これを「埋め込みSQL」(Embedded SQL/ESQL) と呼び、後に[ANSI](https://ja.wikipedia.org/wiki/ANSI "wikilink")により仕様が標準化された。

[マイクロソフト](../Page/マイクロソフト.md "wikilink")は、C言語から[APIレベルで統一したソースコードを記述し](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、[クライアント・サーバ](https://ja.wikipedia.org/wiki/クライアント・サーバ "wikilink")型アプリケーションシステムの構築に有用である仕組み「[Open Database Connectivity](https://ja.wikipedia.org/wiki/Open_Database_Connectivity "wikilink")」(ODBC) を発表し、その有用性からANSIではODBC仕様を参考に「[SQL/CLI](https://ja.wikipedia.org/wiki/Call_Level_Interface "wikilink")」という仕様を標準化した。

[LINQ](https://ja.wikipedia.org/wiki/LINQ "wikilink")では、プログラミング言語[C♯内において](../Page/C_Sharp.md "wikilink")、文脈によって何らかの綴りを[キーワードとして扱うという](../Page/予約語.md "wikilink") contextual keyword を活用し、言語内に言語の拡張のようにしてSQLライクな記述ができる。文字列ベースの埋め込みで発生するインジェクションに関係する問題や、プレースホルダの利用のようなわずらわしさが無いのが利点である。

## SQLとバッチ処理

埋め込みSQLや[ODBCの普及により](https://ja.wikipedia.org/wiki/Open_Database_Connectivity "wikilink")、[オンライントランザクション処理](https://ja.wikipedia.org/wiki/オンライントランザクション処理 "wikilink")向きのSQLアクセス方法は確立されたが、[バッチ処理](https://ja.wikipedia.org/wiki/バッチ処理 "wikilink")性能向上の必要性が求められるようになった。

ある[表 (テーブル)の内容を編集して別の表に格納する大量データの更新処理などをデータベースエンジン内部で処理プログラムを実行し](https://ja.wikipedia.org/wiki/表_\(データベース\) "wikilink")、[入出力](https://ja.wikipedia.org/wiki/入出力 "wikilink") (I/O) のほとんどをデータベース内部で完結することにより、クライアント側とのデータ通信によるオーバヘッドを削減することでバッチ処理性能を向上させる**「[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")」**が考え出された。

[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")は、同じくデータベース内部に定義し、データベースに発生したイベントの内容に応じて任意の処理を実行する機能である「[データベーストリガ](https://ja.wikipedia.org/wiki/データベーストリガ "wikilink")」とともに、標準SQL仕様に採用され、SQL:1999 (SQL99) 規格の永続格納モジュール ([SQL/PSM](https://ja.wikipedia.org/wiki/SQL/PSM "wikilink")) として標準化された。

しかし、標準化される以前から各関係データベース管理システム (RDBMS) ベンダーがデータベースエンジン内部で制御文法を記述し実行できるように独自の拡張が行われていたため、ストアドプロシージャの処理ロジック記述文法はそれ以前に標準化されたSQL文法と比較して著しい非互換が認められるため、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")の[移植性](https://ja.wikipedia.org/wiki/移植性 "wikilink")・開発生産性・保守性を損なう場合がある。

標準SQLのSQL/PSMを採用したRDBMSを以下に挙げる。これらは概ね仕様に準拠しているが、仕様に定められていない部分や実装上の理由により細部には違いがある。

  - SQL/PSM ([DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink"), [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink"))

各RDBMSベンダーによる標準以外の独自のプロシージャには以下のようなものがある。これらには、独自追加された制御構文だけでなく、命令やデータ型の非互換も含むため注意が必要である。

  - [PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink") ([Oracle](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink"), [DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink"))
  - [Transact-SQL](https://ja.wikipedia.org/wiki/Transact-SQL "wikilink") ([Adaptive Server Enterprise](https://ja.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink"), [Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink"))
  - [PL/pgSQL](https://ja.wikipedia.org/wiki/PL/pgSQL "wikilink") ([PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink"))
  - [PSQL](https://ja.wikipedia.org/wiki/PSQL "wikilink") ([Firebird](../Page/Firebird.md "wikilink"), [InterBase](https://ja.wikipedia.org/wiki/InterBase "wikilink"))

## SQLの対話的実行

SQLを対話的に実行する場合、[関係データベース管理システム](https://ja.wikipedia.org/wiki/関係データベース管理システム "wikilink") (RDBMS) に付属する[コマンドラインタイプのアクセスユーティリティを利用するのが一般的である](https://ja.wikipedia.org/wiki/コマンドラインインタフェース "wikilink")。SQL文を記述した[テキストファイル](https://ja.wikipedia.org/wiki/テキストファイル "wikilink")をスクリプトとして実行し、バッチ的に実行することが可能なものもあり、広く利用されている。RDBMSごとに、そのユーティリティ固有の命令を備えているものもあるため、データベースを扱う[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")開発の初心者はその命令もデータベースエンジンが解釈するSQL文法のひとつであると間違って覚えてしまい、[ODBCや](https://ja.wikipedia.org/wiki/Open_Database_Connectivity "wikilink")[JDBC](../Page/JDBC.md "wikilink")など[APIからSQLを実行したときのエラーの原因が理解できずに混乱することもある](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

ユーティリティ固有の文法で誤解しやすいものには、データベースでSQL文の文末に指定する文字である。全データベース共通では「;」、[Oracle Database](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink") の ユーティリティであるSQL\*Plusで、ストアドプロシージャの定義や無名[PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")ブロックを発行するときに文末行に指定する「/」 や、[Sybase](https://ja.wikipedia.org/wiki/Sybase "wikilink")/SQL Serverのisql/osqlではすべてのSQL文の文末行に指定する「GO」などがある。このなかでもっとも間違えやすいのが「;」である。これは、一般的なSQL教科書でも構文の終端文字として例が記載されているが、標準SQLの構文の終端文字ではない。

## SQL文法

### コマンド種別

[データベース言語](https://ja.wikipedia.org/wiki/データベース言語 "wikilink")SQLの文法の種別は、以下の3つに大別される。

  - [データ定義言語](https://ja.wikipedia.org/wiki/データ定義言語 "wikilink") (DDL: data definition language)
  - [データ操作言語](https://ja.wikipedia.org/wiki/データ操作言語 "wikilink") (DML: data manipulation language)
  - [データ制御言語](https://ja.wikipedia.org/wiki/データ制御言語 "wikilink") (DCL: data control language)

その他に、これらの命令の適用範囲を補完するための機能として、SQL文を実行時に解釈する「動的SQL」や、[埋め込みSQL](https://ja.wikipedia.org/wiki/埋め込みSQL "wikilink")のための命令などが用意されている。 [関係データベース管理システム](https://ja.wikipedia.org/wiki/関係データベース管理システム "wikilink") (RDBMS) 以前の[データベース管理システム](../Page/データベース管理システム.md "wikilink") (DBMS) では、これらは必ずしも同一の言語ではなかった。データ定義言語は存在せずにすべて専用のコマンドにパラメタを指定して実行する[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")も存在した。

### コマンド文法

#### データ定義言語

  - [CREATE](https://ja.wikipedia.org/wiki/CREATE_\(SQL\) "wikilink") （データベースオブジェクト（表、インデックス、制約など）の定義）
  - [DROP](https://ja.wikipedia.org/wiki/DROP_\(SQL\) "wikilink") （データベースオブジェクトの削除）
  - [ALTER](https://ja.wikipedia.org/wiki/ALTER_\(SQL\) "wikilink") （データベースオブジェクトの定義変更）

#### データ操作言語

  - [INSERT](https://ja.wikipedia.org/wiki/INSERT_\(SQL\) "wikilink") INTO （行データもしくは表データの挿入）
  - [UPDATE](https://ja.wikipedia.org/wiki/UPDATE_\(SQL\) "wikilink") 〜 SET （表を更新）
  - [DELETE](https://ja.wikipedia.org/wiki/DELETE_\(SQL\) "wikilink") FROM （表から特定行の削除）
  - [SELECT](https://ja.wikipedia.org/wiki/SELECT_\(SQL\) "wikilink") 〜 FROM 〜 WHERE （表データの検索、結果集合の取り出し）
      - 後述する「動的SQL」でのSELECT文には、一度の実行で1行の結果を取得する「単一行SELECT文」と、[カーソルにより複数行の結果を取得する](https://ja.wikipedia.org/wiki/カーソル_\(データベース\) "wikilink")「カーソルSELECT文」がある。

列名と値を、対で指定

``` sql
INSERT INTO 表名(列名1,列名2) VALUES(値1,値2)
```

[表を構成するすべての列に値を格納する場合は](https://ja.wikipedia.org/wiki/表_\(データベース\) "wikilink")、列名の記述を省略可能

``` sql
INSERT INTO 表名 VALUES (値1, 値2)
```

他表のデータを検索して格納

``` sql
INSERT INTO 表名1 SELECT 列名1, 列名2 FROM 表名2 〜
```

更新

``` sql
UPDATE 表名
 SET 列名2=値2, 列名3=値3
 WHERE 列名1=値1
```

削除

``` sql
DELETE FROM 表名
 WHERE 列名1=値1
```

1行以上の検索

``` sql
SELECT *
 FROM 表名
 WHERE 列名1 BETWEEN 値1 AND 値2
 ORDER BY 列名1
```

1行だけの検索

``` sql
SELECT *
 INTO 受け取り変数
 FROM 表名
 WHERE 列名1=値1
```

#### データ制御言語

  - GRANT （特定のデータベース利用者に特定の作業を行う権限を与える）
  - REVOKE （特定のデータベース利用者からすでに与えた権限を剥奪する）
  - SET TRANSACTION （[トランザクション](https://ja.wikipedia.org/wiki/トランザクション "wikilink")モードの設定（並行トランザクションの[分離レベル](https://ja.wikipedia.org/wiki/トランザクション分離レベル "wikilink") (ISOLATION MODE) など））
  - BEGIN （トランザクションの開始）
  - [COMMIT](https://ja.wikipedia.org/wiki/コミット "wikilink") （[トランザクション](https://ja.wikipedia.org/wiki/トランザクション "wikilink")の確定）
  - [ROLLBACK](https://ja.wikipedia.org/wiki/ロールバック "wikilink") （トランザクションの取り消し）
  - [SAVEPOINT](https://ja.wikipedia.org/wiki/SAVEPOINT_\(SQL\) "wikilink") （任意にロールバック地点を設定する）
  - LOCK （表などの資源を占有する）

#### カーソル定義・操作

「[カーソル](https://ja.wikipedia.org/wiki/カーソル_\(データベース\) "wikilink")」とは、[SELECT文などによるデータベース検索による検索実行の結果を](https://ja.wikipedia.org/wiki/SELECT_\(SQL\) "wikilink")1行ずつ取得して処理するために、データベースサーバ側にある結果集合と行取得位置を示す概念をいう。 カーソルの定義とその操作は、主に[アプリケーションプログラム](https://ja.wikipedia.org/wiki/アプリケーションプログラム "wikilink")などの手続き型言語からのSQL実行において利用する。

  - DECLARE CURSOR （カーソル定義）
  - OPEN （カーソルのオープン）
  - FETCH （カーソルのポインタが指し示す位置の行データを取得し、ポインタを一行分進める。）
  - UPDATE （カーソルのポインタが指し示す位置の行データを更新する）
  - DELETE （カーソルのポインタが指し示す位置の行データを削除する）
  - CLOSE （カーソルのクローズ）

##### カーソル宣言例

``` sql
DECLARE CR1 CURSOR FOR
 SELECT CLMA, CLMB, CLMC
  FROM TBL1
  WHERE CLMA BETWEEN :V開始値 AND :V終了値
```

※V開始値、V終了値は、埋め込み変数あるいはホスト変数と呼ばれ、埋め込みSQLの場合は、プログラム中の**BEGIN DECLARE SECTION**〜**END DECLARE SECTION**の間で宣言する。

##### カーソルのオープン例

``` sql
OPEN CR1
```

※カーソルのオープン前に、V開始値、V終了値には値を設定しておく。

##### 行の取り出し例

``` sql
FETCH CR1 INTO :V列A, :V列B, :V列C
```

検索条件に合致した行をすべて取り出すには、「データなし」になるまでFETCHを繰り返す。

※V列A, :V列B, :V列C は、埋め込み変数あるいはホスト変数と呼ばれ、埋め込みSQLの場合は、プログラム中の**BEGIN DECLARE SECTION**〜**END DECLARE SECTION**の間で宣言する。

**取り出した行の更新例**

``` sql
UPDATE TBL1
 SET CLMB=CLMB+1, CLMC=:V列C更新値
 WHERE CURRENT OF CR1
```

FETCHで位置付けた行を更新するには、UPDATE文で**WHERE CURRENT OF カーソル名**を指定する。

※V列C更新値は、埋め込み変数あるいはホスト変数と呼ばれ、埋め込みSQLの場合は、プログラム中の**BEGIN DECLARE SECTION**〜**END DECLARE SECTION**の間で宣言する。

**取り出した行の削除例**

``` sql
DELETE FROM TBL1
 WHERE CURRENT OF CR1
```

FETCHで位置付けた行を削除するには、DELETE文で**WHERE CURRENT OF カーソル名**を指定する。

**カーソルのクローズ例**

``` sql
CLOSE CR1
```

#### 動的SQL

動的SQLは、通常SQL文をRDBMSに対して送信の度にデータベースエンジンで実行可能な内部中間コードに翻訳する作業を事前に行うことによって、 翻訳済みSQLコードを再度利用してSQL解析のオーバーヘッドを削減することと、SQL文をソースコードで固定せずにデータベースへのアクセス毎に構文を書き換えたい場合に、有用である。[データ操作言語](https://ja.wikipedia.org/wiki/データ操作言語 "wikilink") (DML) ももちろん実行できるが、[データ定義言語](https://ja.wikipedia.org/wiki/データ定義言語 "wikilink") (DDL) のようにデータベース製品の機能アップによって新しい命令が追加されるものは、[プリプロセッサ](https://ja.wikipedia.org/wiki/プリプロセッサ "wikilink")の対応作業が重荷になるため、ほとんどのデータベース製品ではDDL文は動的SQLにて実行することが一般的となっている。

  - PREPARE （文字列で与えたSQL文を解析・翻訳する）
  - EXECUTE （PREPAREで翻訳したSQL文を実行する）

<!-- end list -->

    パラメタなし
    PREPARE PRESQL FROM 'DELETE FROM TBL1 WHERE CLMA=1'
      ↓
    EXECUTE PRESQL

    パラメタあり（1回のPREPAREで、EXECUTEの繰り返し実行が可能）
    PREPARE PRESQL FROM 'DELETE FROM TBL1 WHERE CLMA=? AND CLMB=?'
    　↓
    EXECUTE PRESQL USING :XCLMA,:XCLMB

#### 埋め込みSQL

もともとカーソルは、埋め込みSQLでホスト言語（母言語）から結果集合を取得するために、都合のよい方法として考えられたものである。データベースと通信するためのリソースの割り当て確保や開放、1行ごとにホスト言語のループ処理で取得するための命令 (FETCH) などがある。

  - ALLOCATE (DEALLOCATE) DESCRIPTOR　（データベースとホスト言語（母言語）間での通信領域の確保と開放。）
  - WHENEVER （エラー発生時の振る舞いを定義）
  - SQLSTATE （SQL文実行後の状態が保存される領域）

<!-- end list -->

``` sql
EXEC SQL INCLUDE SQLCA         END-EXEC.
EXEC SQL BEGIN DECLARE SECTION END-EXEC.
77  XPARM              PIC X(3).
01  XTBL1.
  03  XCLMA            PIC X(3).
  03  XCLMB            PIC X(10).
01  XTBL2.
  03  XCLM1            PIC S9(5) COMP-3.
  03  XCLM2            PIC S9(9) COMP.
EXEC SQL END   DECLARE SECTION END-EXEC.

    EXEC SQL
     DECLARE CR1 CURSOR FOR
      SELECT CLMA, CLMB FROM TBL1
       WHERE CLMA>=:XPARM
       ORDER BY CLMA
    END-EXEC.

    EXEC SQL WHENEVER SQLERROR GO TO ERR--PROC END-EXEC.

*   SQLの静的実行（カーソル操作例）
    MOVE  'ABC'    TO  XPARM.
    EXEC SQL OPEN CR1          END-EXEC.
    PERFORM TEST BEFORE
     UNTIL SQLCODE NOT = ZERO
      EXEC SQL
       FETCH CR1 INTO :XCLMA, :XCLMB
      END-EXEC
      IF SQLCODE = ZERO
       データ検索時の処理
       END-IF
    END-PERFORM.
    IF SQLCODE = 100
     EXEC SQL CLOSE CR1          END-EXEC
    END-EXEC.
*   SQLの動的実行（？パラメタ使用）
    EXEC SQL
     PREPARE PRESQL FROM
      'INSERT INTO TBL2 (CLM1, CLM2) VALUES(?, ?)'
    END-EXEC.
    MOVE ZERO       TO  XCLM2.
    PERFORM TEST AFTER
     VARYING XCLM1 FROM 1 BY 1
     UNTIL XCLM1 >= 10
      EXEC SQL
       EXECUTE PRESQL USING :XCLM1, :XCLM2
      END-EXEC
    END-PERFORM.
    GOBACK.
ERR--PROC.
    例外処理
```

#### 3値論理

SQLで用いられる論理値は、コンピュータの世界でもっとも広く利用されている[2値論理](https://ja.wikipedia.org/wiki/2値論理 "wikilink") (TRUE, FALSE) ではなく、[3値論理](https://ja.wikipedia.org/wiki/3値論理 "wikilink") (TRUE, FALSE, UNKNOWN) となっている（[クリーネや](https://ja.wikipedia.org/wiki/スティーヴン・コール・クリーネ "wikilink")[ウカシェヴィチによるような](https://ja.wikipedia.org/wiki/ヤン・ウカシェヴィチ "wikilink")3値の論理体系を持っている、という意味で「3値論理となっている」というわけではない（少なくとも、はっきりと標準化され、ほぼ全ての実装でそれが満たされているような唯一の体系となっているわけではない。詳細は [:en:Three-valued_logic\#SQL](https://ja.wikipedia.org/wiki/:en:Three-valued_logic#SQL "wikilink") を参照）。現実的には単に通常の2値論理の[真理値](https://ja.wikipedia.org/wiki/真理値 "wikilink")の他に例外的な値としてのUNKNOWNがあるということであって、このような言い方をするならば、「[null](https://ja.wikipedia.org/wiki/null "wikilink")」の類が真理値の文脈にあらわれるような、広く利用されている多くのプログラミング言語も同様に「3値論理となっている」）。

## 主な SQL DBMS 実装

  - [Ingres](https://ja.wikipedia.org/wiki/Ingres "wikilink")（[オープンソース](../Page/オープンソース.md "wikilink")、[UNIX](../Page/UNIX.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[Mac OS対応](https://ja.wikipedia.org/wiki/Mac_OS "wikilink")）
  - [Oracle Database](https://ja.wikipedia.org/wiki/Oracle_Database "wikilink")（[プロプライエタリ](https://ja.wikipedia.org/wiki/プロプライエタリ "wikilink")、UNIX、Linux、Windows対応）
  - [SQL/DS](https://ja.wikipedia.org/wiki/SQL/DS "wikilink") ([VSE](https://ja.wikipedia.org/wiki/VSE "wikilink"), VM/CMS)
  - [IBM DB2](https://ja.wikipedia.org/wiki/DB2 "wikilink") (プロプライエタリ、[AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")、[z/OS](https://ja.wikipedia.org/wiki/z/OS "wikilink")、UNIX、Linux、Windows対応）
  - [IBM Informix Dynamic Server](https://ja.wikipedia.org/wiki/Informix_Dynamic_Server "wikilink")（プロプライエタリ、UNIX、Linux、Windows対応）
  - [Sybase Adaptive Server Enterprise](https://ja.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink")（プロプライエタリ、UNIX、Linux、Windows対応）
  - [Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")（プロプライエタリ、Windows対応）
  - [PostgreSQL](https://ja.wikipedia.org/wiki/PostgreSQL "wikilink")（オープンソース、UNIX、Linux、Windows対応）
  - [MySQL](https://ja.wikipedia.org/wiki/MySQL "wikilink")（オープンソース、UNIX、Linux、Windows対応）
  - [InterBase](https://ja.wikipedia.org/wiki/InterBase "wikilink")（プロプライエタリ、Linux、Windows、[Solaris](../Page/Solaris.md "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") 対応）
  - [Firebird](../Page/Firebird.md "wikilink")（オープンソース、Linux、Windows、macOS 、Solaris、[HP-UX](https://ja.wikipedia.org/wiki/HP-UX "wikilink")対応）
  - [SQLite](https://ja.wikipedia.org/wiki/SQLite "wikilink")（オープンソース(パブリックドメイン)、標準のC言語で実装されており再コンパイルであらゆる環境に対応）

## 脚注

### 注釈

### 出典

## 関連項目

  - [関係モデル](https://ja.wikipedia.org/wiki/関係モデル "wikilink")
      - [関係代数 (関係モデル)](https://ja.wikipedia.org/wiki/関係代数_\(関係モデル\) "wikilink")
      - [関係論理](https://ja.wikipedia.org/wiki/関係論理 "wikilink")
  - [SQLインジェクション](https://ja.wikipedia.org/wiki/SQLインジェクション "wikilink")
  - [ドメイン固有言語](https://ja.wikipedia.org/wiki/ドメイン固有言語 "wikilink")
  - 整列法
      - クイックソート
      - バブルソート
  - 並列演算処理

[Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink") [Category:問い合わせ言語](https://ja.wikipedia.org/wiki/Category:問い合わせ言語 "wikilink")

1.  よりデジタル大辞泉、IT用語がわかる辞典を参照
2.
3.  よりDBM用語辞典を参照
4.
5.  [SQL:2008 now an approved ISO International Standard](https://web.archive.org/web/20110628130925/http://iablog.sybase.com/paulley/2008/07/sql2008-now-an-approved-iso-international-standard/) - Sybase Blog - Glenn Paulley - Id Rather Play Golf