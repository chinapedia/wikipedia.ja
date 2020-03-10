> この記事は[DELETE \(SQL\)](https://ja.wikipedia.org/wiki/DELETE_\(SQL\))から翻訳されています。


**DELETE(デリート)**ステートメントは、1つもしくは複数の[レコード](../Page/レコード.md "wikilink")を削除する、[SQL](../Page/SQL.md "wikilink")における[データ操作言語](https://ja.wikipedia.org/wiki/データ操作言語 "wikilink") (DML)ステートメントの1つである。すべてのレコードを一括削除するかまたは、条件式を満たす一部のレコードだけを削除することができる。

## 構文

``` sql
 DELETE FROM 主表 [WHERE 条件式]
```

WHERE句で条件式を指定した場合は、条件式に一致するレコードのみ削除される。WHERE句が省略された場合は、全レコードが削除される。

DELETE の際に削除の対象以外の表を参照する場合には[副問い合わせ](https://ja.wikipedia.org/wiki/副問い合わせ "wikilink")を使う必要があるが、データベースによっては **USING** または追加の **FROM** 句により表の参照を追加できるものもある。 \[1\] \[2\] \[3\]

``` sql
 DELETE FROM 主表 USING 副表 WHERE 主表.列 = 副表.列 ...
```

DELETEステートメントを実行したとき、[データベーストリガ](https://ja.wikipedia.org/wiki/データベーストリガ "wikilink")を設定することにより他のテーブルもあわせて削除することができる。例えば、2つのテーブルが[外部キー](../Page/外部キー.md "wikilink")でリンクされているとき、一方のテーブルのある行が削除されたなら、削除された行とリンクしている他方のテーブルの行もトリガーにより自動削除されることにより、[参照整合性](../Page/参照整合性.md "wikilink")を維持することができる。

## 性能

一般に、全ての行を削除する場合には DELETE よりも [TRUNCATE](https://ja.wikipedia.org/wiki/TRUNCATE_\(SQL\) "wikilink") TABLE ステートメントのほうが高速に処理できる。

## サンプル

テーブル pies から、項目 flavour が 'Lemon Meringue' である行を削除する:

` DELETE FROM pies WHERE flavour='Lemon Meringue';`

テーブル mytable から、項目 mycol の値が100より大きい行を削除する:

`DELETE FROM mytable WHERE mycol > 100;`

テーブル mytable のすべての行を削除する:

`DELETE FROM mytable;`

## 脚注

<references/>

[Category:SQL](https://ja.wikipedia.org/wiki/Category:SQL "wikilink")

1.
2.
3.