> この記事は[Transact-SQL](https://ja.wikipedia.org/wiki/Transact-SQL)から翻訳されています。


**Transact-SQL** (T-SQL) は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")と[Sybase](../Page/Sybase.md "wikilink")が独自に拡張した[SQL](../Page/SQL.md "wikilink")言語である。マイクロソフトによる実装は [Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") として出荷されている。Sybase ではこの言語を Sybase SQL Server の後継である [Adaptive Server Enterprise](https://ja.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink") で使っている。

SQL を強化するため、次のような機能が追加されている。

  - 制御フロー言語
  - 局所変数
  - グローバル変数
  - 文字列処理、データ処理、数値処理のための各種関数。
  - DELETE文とUPDATE文の強化

## 制御フロー言語

Transact-SQL の制御フローのためのキーワードとしては、`BEGIN` と `END`、`BREAK`、`CONTINUE`、`GOTO`、`IF` と `ELSE`、`RETURN`、`WAITFOR`、`WHILE` がある。

`IF` と `ELSE` によって条件付実行が可能となる。例えば、日付が週末であれば "weekend" と表示し、そうでなければ "weekday" と表示するといった処理が可能である。

``` tsql
IF DATEPART(dw, GETDATE()) = 7 OR DATEPART(dw, GETDATE()) = 1
   PRINT 'It is the weekend.'
ELSE
   PRINT 'It is a weekday.'
```

`BEGIN` と `END` は文のブロック化を可能とする。例えば、上記のコードで複数の文を条件付で実行する場合、BEGIN と END を使って次のように書く。

``` tsql
IF DATEPART(dw, GETDATE()) = 7 OR DATEPART(dw, GETDATE()) = 1
BEGIN
   PRINT 'It is the weekend.'
   PRINT 'Get some rest!'
END
ELSE
BEGIN
   PRINT 'It is a weekday.'
   PRINT 'Get to work!'
END
```

`WAITFOR` は、指定された時間だけ待つか、指定された時刻まで待つ。遅延制御に使ったり、指定時刻まで実行をブロックするのに使われる。

`RETURN` は、[ストアドプロシージャ](https://ja.wikipedia.org/wiki/ストアドプロシージャ "wikilink")や関数から即座に戻るときに使う。

`BREAK` は `WHILE` ループからの脱出、`CONTINUE` はループの次の繰り返しへの飛び越しである。`WHILE` ループの例は下記にある。

## 局所変数

局所変数は実行中のスクリプト内でのみ使われる。Transact-SQL はユーザー定義の広域変数をサポートしていない。

`DECLARE` によって変数名と型を指定して変数を宣言する。SET 文で値を代入し、その後の文で変数名を使うことでその値を参照できる。

次のスクリプトは整数の変数を宣言し、値を初期化し、`WHILE` ループで処理を実行している。

``` tsql
DECLARE @Counter INT
SET @Counter = 10
WHILE @Counter > 0
BEGIN
   PRINT 'The count is ' + CONVERT(VARCHAR(10), @Counter)
   SET @Counter = @Counter - 1
END
```

このループ本体は、変数の値を含むメッセージを表示し、その値をデクリメントするものである。

変数の初期化は次のようにもできる。

``` tsql
DECLARE @ArticleCount INT
SELECT @ArticleCount = COUNT(*) FROM Articles

INSERT INTO SizeLog (SampleTime, ArticleCount) VALUES (GETDATE(), @ArticleCount)
```

これは、Articles 表の行数を取得し、その値と現在時刻を SizeLog 表の行として挿入するものである。

## グローバル変数

グローバル変数は実行中のスクリプト内での様々なステータスを監視・取得ができる。 Transact-SQLではグローバル変数は主として@@で書き始める。

良く使われるグローバル変数としては以下のものがある。

`@@ERROR` 直前に実行したクエリのエラー状態を保持

`@@ROWCOUNT` 直前に実行したクエリの処理数を保持

`@@FETCH_STATUS` 現在実行中のカーソルのFETCH状態を保持(`@@FETCH_STATUS = 0`の場合、正常終了)

下記にグローバル変数を利用したエラー処理の例を示す

  - クエリ実行時のエラーハンドリング

<!-- end list -->

``` tsql
DECLARE @ERROR_STATUS INT
SET @ERROR_STATUS = 0

SELECT DATE
FROM CALENDAR WITH (NOLOCK)
WHERE YEAR = '2007' AND MONTH = '01'

-- グローバル変数@@ERRORにて直前のクエリのエラー状況を取得
-- 0 の場合はエラーなし
SET @ERROR_STATUS = @@ERROR

IF @ERROR_STATUS <> 0
BEGIN
    PRINT 'ERROR OCCURD'
    RETURN
END
```

  - UPDATE実行時の該当件数が無かった場合のエラーハンドリング

<!-- end list -->

``` tsql
DECLARE @ROW_COUNT INT
SET @ROW_COUNT = 0

UPDATE CALENDAR
SET DATE = GETDATE()
WHERE YEAR = '2007' AND MONTH = '01'

-- グローバル変数@@ROWCOUNTにて直前のクエリの結果件数を取得
SET @ROW_COUNT = @@ROWCOUNT

IF @ROW_COUNT = 0
BEGIN
    PRINT 'NO RECORD UPDATED'
    RETURN
END
```

## DELETE文とUPDATE文の変更

Transact-SQL では、DELETE文とUPDATE文にFROM節を指定可能となっている。

次の例では、'Idle' フラグの立っている全ての `users` を削除する。

``` tsql
DELETE FROM users as u
    JOIN user_flags as f
        ON u.id=f.id
    WHERE f.name = 'Idle'
```

## カーソルの実装

Transact-SQL では、`CURSOR`を使用することで、テーブルを逐次処理することが可能である。

次の例では、`CURSOR`を利用し、`CALENDAR`テーブルを条件分けしながら更新する処理である。

``` tsql
-- カーソルの定義
DECLARE
    CUR_CALENDAR_UPDATE
CURSOR FOR
    SELECT
        YEAR,
        MONTH,
        DAY
    FROM
        CALENDAR

-- 変数宣言/初期化
DECLARE @wk_year CHAR(4)
DECLARE @wk_month VARCHAR(2)
DECLARE @wk_day VARCHAR(2)

SET @wk_year = ''
SET @wk_month = ''
SET @wk_day = ''


-- カーソルを開く
OPEN CUR_CALENDAR_UPDATE


-- カーソルより最初の1行を取得
FETCH NEXT FROM
    CUR_CALENDAR_UPDATE
INTO
    @wk_year,
    @wk_month,
    @wk_day


-- カーソルで取得した行が終端に達するまで処理を継続する
WHILE @@FETCH_STATUS = 0
BEGIN

    -- カーソルで取得したYEARが2006より大きい場合は処理を行う
    IF @wk_year > 2006
    BEGIN
        UPDATE
            CALENDAR
        SET
            DATE = GETDATE()
        WHERE
            YEAR = @wk_year
        AND
            MONTH = @wk_month
        AND
            DAY = @wk_day
    END

    -- 次の1件を取得する
    FETCH NEXT FROM
        CUR_CALENDAR_UPDATE
    INTO
        @wk_year,
        @wk_month,
        @wk_day
END

-- カーソルを閉じる
CLOSE CUR_CALENDAR_UPDATE

-- カーソルのメモリを開放
DEALLOCATE CUR_CALENDAR_UPDATE
```

## 批判

Transact-SQL は[PL/SQL](https://ja.wikipedia.org/wiki/PL/SQL "wikilink")同様、機能を追加することで SQL 標準との互換性が損なわれているだけでなく、SQLが本来保持すべきモジュール性を破壊していると批判されている。換言すれば、Transact-SQL の追加機能は普通ならプログラミング言語や[埋め込みSQLに実装されるべきものである](https://ja.wikipedia.org/wiki/SQL#埋め込みSQL "wikilink")。そのため、[制御構造](https://ja.wikipedia.org/wiki/制御構造 "wikilink")をプログラミング言語でも SQL でも指定可能になってしまい、混乱が生じる。

## 関連項目

  - [Adaptive Server Enterprise](https://ja.wikipedia.org/wiki/Adaptive_Server_Enterprise "wikilink") - Sybase社によるUNIX向けの実装
  - [Microsoft SQL Server](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink") - Microsoft社によるWindows向けの実装
  - [SQL](../Page/SQL.md "wikilink")

## 外部リンク

  - \[<http://msdn.microsoft.com/ja-jp/library/cc341061(SQL.80>).aspx Transact-SQL リファレンス for SQL Server 2000 (MSDN)\]
  - [Transact-SQL リファレンス for SQL Server 2005 (MSDN)](http://msdn.microsoft.com/ja-jp/library/ms189826.aspx)
  - [Transact-SQL リファレンス for SQL Server 2008 (MSDN)](http://msdn.microsoft.com/ja-jp/library/bb510741.aspx)
  - [ASE Reference Manual](http://manuals.sybase.com/onlinebooks/group-as/asg1250e/refman)
  - [DevGuru T-SQL Quick Reference](http://devguru.com/technologies/t-sql/)
  - [Sqsh](https://sourceforge.net/projects/sqsh/) - オープンソース版 Transact-SQL クライアント

[Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink")