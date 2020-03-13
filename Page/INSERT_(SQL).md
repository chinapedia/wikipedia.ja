> この記事は[INSERT \(SQL\)](https://ja.wikipedia.org/wiki/INSERT_\(SQL\))から翻訳されています。


**INSERT(インサート)**ステートメントは、[行を追加する](https://ja.wikipedia.org/wiki/組_\(データベース\) "wikilink")、[コンピュータ](../Page/コンピュータ.md "wikilink")の[データベース言語](../Page/データベース言語.md "wikilink") [SQL](../Page/SQL.md "wikilink") における[データ操作言語](https://ja.wikipedia.org/wiki/データ操作言語 "wikilink")（DML）ステートメントの1つである。1度に1行を追加するだけではなく、問い合わせの結果としての複数行を追加することもできる。なお、ユーザーはそのテーブル（[関係](https://ja.wikipedia.org/wiki/関係_\(データベース\) "wikilink")）に対してINSERT権限を持っている必要がある。また、WHERE句で指定したテーブル全てに対してSELECT権限を持っている必要がある。

## 構文

### 値の挿入

``` sql
INSERT INTO テーブル名 [ (列名1 [ ,列名2・・・]) ]
  VALUES (値A1 [, 値A2 ...]) [, (値B1 [, 値B2 ...]) ...];
```

[列の数と値の数は一致している必要がある](https://ja.wikipedia.org/wiki/属性_\(データベース\) "wikilink")。指定のない列についてはデフォルト値（テーブル作成時にDEFAULT句で指定された値）または[NULLが使われる](https://ja.wikipedia.org/wiki/Null "wikilink")。列の順番は任意である。列の指定が無い場合、テーブル作成時の列順を利用してすべての列を指定したと扱われる。

設定した値あるいは未設定時の値（デフォルト値またはNULL）は、その列またはテーブルに適用される制約（[主キー](../Page/主キー.md "wikilink")制約、[一意性制約](https://ja.wikipedia.org/wiki/一意性制約 "wikilink")、[参照整合性](../Page/参照整合性.md "wikilink")制約、[CHECK制約](https://ja.wikipedia.org/wiki/CHECK制約 "wikilink")、[NOT NULL制約など](https://ja.wikipedia.org/wiki/NOT_NULL制約 "wikilink")）を満たさなければならない。文法エラーまたは制約違反があれば行追加は失敗する。

`VALUES` に続けて複数の行値を指定することにより、複数の行を一括で挿入することができる。`INSERT` を複数回実行するのと結果は変わらないが、データベース製品によっては処理の効率が高まる場合がある。

**例**

``` sql
INSERT INTO phone_book (name, number) VALUES ('John Doe', '555-1212');
```

``` sql
INSERT INTO phone_book (name, sex) VALUES ('Nancy', 'Woman'),('Tom', 'Man'),('Cathy','Woman');
```

### 問い合わせ結果の挿入

``` sql
INSERT INTO テーブル名1 SELECT * FROM テーブル名2 WHERE 条件式;
```

テーブル2に対するSELECTステートメントでの問い合わせの結果をテーブル1に追加する。

**例**

``` sql
INSERT INTO phone_book2 SELECT * FROM phone_book WHERE NAME IN ('John Doe', 'Peter Doe');
```

## 採番キーの見つけ方

データベースシステムが自動採番した連番等の人工キーを[主キー](../Page/主キー.md "wikilink")として利用する場合、他の[SQL](../Page/SQL.md "wikilink")ステートメントから、その追加対象のテーブルを利用するために、自動採番された主キーを見つける必要があるが、その方法には以下のようなものがある。

  - 特別な[ストアドプロシージャ](../Page/ストアドプロシージャ.md "wikilink")を使用する
  - 一時テーブルに最後に追加した行を[SELECTステートメントで検索する](../Page/SELECT_\(SQL\).md "wikilink")
  - INSERTステートメントにおける一意な要素の組み合わせを、[SELECTステートメントでの検索に使用する](../Page/SELECT_\(SQL\).md "wikilink")
  - INSERTステートメントで[GUID](../Page/GUID.md "wikilink")を使用し、 [SELECT](../Page/SELECT_\(SQL\).md "wikilink") ステートメントでそれをキーに検索する

[Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink")