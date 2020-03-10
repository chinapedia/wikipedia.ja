> この記事は[UPDATE \(SQL\)](https://ja.wikipedia.org/wiki/UPDATE_\(SQL\))から翻訳されています。


**UPDATE**ステートメントは、[SQL](../Page/SQL.md "wikilink") における[データ操作言語](https://ja.wikipedia.org/wiki/データ操作言語 "wikilink") (DML) のステートメントの1つで、[テーブル内の](https://ja.wikipedia.org/wiki/表_\(データベース\) "wikilink")1つもしくは複数の[レコード](../Page/レコード.md "wikilink")のデータを更新する。WHERE句が省略されている場合はすべてのレコードが、指定されている場合はその条件式を満たす一部のレコードだけが、一括して更新される。

## 構文

**`UPDATE`**` テーブル名 SET 列名1 = 値1 [,列名2 = 値2...] [WHERE 条件式];`

正常に更新が行われるためには、更新されるテーブルや列に対する更新権限をユーザが持っている必要がある。また、更新後の値が[PRIMARY KEY制約](../Page/主キー.md "wikilink")、[一意性制約](https://ja.wikipedia.org/wiki/一意性制約 "wikilink")、[CHECK制約](https://ja.wikipedia.org/wiki/CHECK制約 "wikilink")、[NOT NULL制約などに違反しないことが必要である](https://ja.wikipedia.org/wiki/NOT_NULL制約 "wikilink")。

## 例

### 基本構文

テーブル "t" に対し、列 "c2" の値が a であれば、列 "c1" の値を 1 にセットする。

``` sql
UPDATE t SET c1 = 1 WHERE c2 = 'a';
```

テーブル "t" に対し、列 "c2" の値が a であれば、列 "c1" の値に 1 を加算する。

``` sql
UPDATE t SET c1 = c1 + 1 WHERE c2 = 'a';
```

1つのUPDATEステートメントで複数列を更新することも可能である。下の例では、テーブル "t" に対し、列 "c1" の値に 1 を、列 "c2" の値に 2 をセットする。

``` sql
UPDATE test SET c1 = 1, c2 = 2;
```

### 結合

他のテーブルと結合した結果により更新を行う場合、サブクエリ（副次問い合わせ）を用いる方法と、[SELECT](../Page/SELECT_\(SQL\).md "wikilink") ステートメントと類似の結合式を用いる方法がある。以下の例はどちらも、テーブル "t1" に対し、列 "a2" の値が、テーブル "t2" の列 "b1" の値が 0 であるすべてのレコードにおける列 "b2" の値のいずれかと一致すれば、列 "a1" に 2 をセットする。

**サブクエリ**

``` sql
UPDATE t1
   SET a1 = 2
 WHERE a2 IN (SELECT b2 FROM t2 WHERE b1 = 0);
```

**結合**

``` sql
UPDATE t1
   SET a1 = 2
  FROM t2
 WHERE t1.a2 = t2.b2 AND t2.b1 = 0;
```

[Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink")