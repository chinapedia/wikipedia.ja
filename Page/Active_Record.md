> この記事は[Active Record](https://ja.wikipedia.org/wiki/Active_Record)から翻訳されています。


**Active Record**（アクティブ・レコード）とは、[プログラミングにおいて](https://ja.wikipedia.org/wiki/プログラミング_\(コンピュータ\) "wikilink")、[企業アプリケーション](https://ja.wikipedia.org/wiki/企業アプリケーション "wikilink")で頻繁に認められる[デザインパターンである](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")。

## 概要

Active Recordは[データベース](../Page/データベース.md "wikilink")からデータを読み出すためのアプローチである。データベーステーブルあるいはビューの1行が1つのクラスにラップされ、オブジェクトのインスタンスがそのデータベースの1つの行に結合される。このクラスはデータベースアクセスの[カプセル化](https://ja.wikipedia.org/wiki/カプセル化 "wikilink")も行う\[1\]。オブジェクトの生成後は、保存メソッドで新しい行がデータベースに追加される。 オブジェクトが更新されると、データベースの対応する行もまた更新される。ラッパークラスはテーブルあるいはビューの各カラムに対する[アクセサ](https://ja.wikipedia.org/wiki/アクセサ "wikilink")メソッドを実装するが、それ以外の振る舞い（[MVCのモデルが担当すべき](https://ja.wikipedia.org/wiki/Model_View_Controller "wikilink")[ロジック](../Page/ビジネスロジック.md "wikilink")）も記述することができる\[2\]。

テーブルとクラスが一対一で結びつくことから非常にシンプルな構造となることが特徴で、後述する[Ruby on Railsでは](../Page/Ruby_on_Rails.md "wikilink")、データベース定義からほぼ自動で[CRUD](../Page/CRUD.md "wikilink")操作を備えたクラスを作り出すことを実現している。一方でその性質上、複雑な設計のデータベースとは相性が悪い。\[3\]

## 例

### Ruby on Rails

広く使われている実装のひとつは、[Ruby on Rails](../Page/Ruby_on_Rails.md "wikilink") のActive Recordの実装である。例えば、id 列（シリアルな主キー）、name 列（varchar 型）、price 列（money 型あるいは double 型）を持った parts テーブルがあれば、次のようなコードになる。

``` rails
a = Part.new
a.name = "Sample part"
a.price = 123.45
a.save
```

上記のコードは与えられた値で新しい行をデータベースに作る。これは次の [SQL](../Page/SQL.md "wikilink") コマンドにほぼ等価である。

``` sql
INSERT INTO parts (name, price) VALUES ('Sample part', 123.45);
```

逆 に、データベースを検索するためこのクラスを用いることもできる。

``` rails
widgetname = "gearbox"
b = Part.where(:name => widgetname).first
```

このコードは、 `name` 列が [Ruby](../Page/Ruby.md "wikilink") 変数 `widgetname` の値 一致する最初の行 を取得して、オブジェクトを生成する。取得については、 次の SQL コマンドと 同義であるが、前述のrubyコードにそれは現れない。

``` sql
SELECT * FROM parts WHERE name = 'gearbox' LIMIT 1;
```

別の方法として、上記のコードは次のように短くすることもできる。

``` rails
b = Part.find_by_name("gearbox")
```

## 脚注

## 関連項目

  - [オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")
  - [メッセージ転送](https://ja.wikipedia.org/wiki/メッセージ転送 "wikilink")

## 外部リンク

  - [TECHSCORE - デザインパターンから見たActive Record](http://www.techscore.com/tech/Ruby/Rails/other/designpattern/1/)

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink")

1.
2.
3.