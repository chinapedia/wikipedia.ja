> この記事は[Memcached](https://ja.wikipedia.org/wiki/Memcached)から翻訳されています。


**memcached** は、汎用の分散型メモリキャッシュシステムである。

## 概要

もともと [Danga Interactive](https://ja.wikipedia.org/wiki/:en:Danga_Interactive "wikilink") によって [LiveJournal](https://ja.wikipedia.org/wiki/LiveJournal "wikilink") サービスのために開発されたが、現在は多数のサイトで利用されている。memcached は、データと[オブジェクトをメモリ内にキャッシュすることでデータベースから読み出しを行う回数を減少させ](../Page/オブジェクト_\(プログラミング\).md "wikilink")、[データベース](../Page/データベース.md "wikilink")を用いた Web サイトを高速化するために良く用いられる。memcachedは[パーミッシブ・ライセンス](https://ja.wikipedia.org/wiki/パーミッシブ・ライセンス "wikilink")である[BSDライセンス](../Page/BSDライセンス.md "wikilink")に従い頒布されている\[1\]。

memcached は適切に設定された[ファイアウォール](../Page/ファイアウォール.md "wikilink")を用いるサーバ上で使用するか、そうでない場合は[SASL認証のオプション付きでコンパイルしたものを使用できる](https://ja.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer "wikilink")(1.4.3以降)。既定では、memcached はポート 11211 番を使用する。また、[libevent](https://ja.wikipedia.org/wiki/libevent "wikilink") を使用している。

memcached の API は、複数のマシン上に分散された巨大な[ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")を提供する。テーブルがいっぱいの場合、以降のデータの新規挿入により古いデータは[Least Recently Used](../Page/Least_Recently_Used.md "wikilink") 順序で削除される。memcached を用いるアプリケーションは、背後にあるデータベースなどの低速な記憶装置へのアクセスの前に memcached のリクエストを挿入する。

memcached のシステムは、YouTube \[2\] や[LiveJournal](https://ja.wikipedia.org/wiki/LiveJournal "wikilink")、[Wikipedia](../Page/ウィキペディア.md "wikilink")、[SourceForge](../Page/SourceForge.net.md "wikilink")、[Facebook](../Page/Facebook.md "wikilink")、[Digg](../Page/Digg.md "wikilink")、[Fotologなどの大規模な有名サイトで使用されている](https://ja.wikipedia.org/wiki/:en:Fotolog "wikilink")\[3\]。

## サンプルコード

データベースやオブジェクト生成の[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")ーを memcached を使うよう変更することは簡単である。 単純なデータベースのクエリーを用いた場合、サンプルコードは下記のようになる。(以下の例は全て[擬似コード](../Page/擬似コード.md "wikilink")である。memcached の処理やプログラミング言語は、使用する API により異なる。)

`function get_foo (int userid) {`
`    result = db_select("SELECT * FROM users WHERE userid = ?", userid);`
`    return result;`
`}`

memcached を用いるよう変更すると、同じコードは下記のようになる。

`function get_foo (int userid) {`
`    result = memcached_fetch("userrow:" + userid);`
`    if (!result) {`
`        result = db_select("SELECT * FROM users WHERE userid = ?", userid);`
`        memcached_add("userrow:" + userid, result);`
`    }`
`    return result;`
`}`

サーバは、まず memcached に対して一意のキー "userrow:userid" が存在するかどうかの確認を行う。 存在しないという結果であれば、通常のようにデータベースに select を要求し、memcached の add API を呼び出しキーを追加する。

しかし get_foo 関数のみが変更され、DBに対して更新が実行される部分が変更されなければ get_foo は誤ったデータを取り出すことになる。従って add の呼び出しに加えて更新の処理も必要になる。そのためには memcached の set 関数を使う。

`function update_foo(int userid, string dbUpdateString) {`
`    result = db_execute(dbUpdateString);`
`    if (result) {`
`        data = createUserDataFromDBString(dbUpdateString);`
`        memcached_set("userrow:" + userid, data);`
`    }`
`}`

この処理はデータベースのクエリーが成功すると仮定して現在のキャッシュのデータをデータベースの新しいデータと合致するよう更新する。異なるアプローチとして、memcached のキャッシュを delete 関数で無効にし、以降のデータの取り出しがキャッシュミスとなるようにする方法もある。

## 脚注

## 外部リンク

  -
[Category:サーバ](https://ja.wikipedia.org/wiki/Category:サーバ "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink") [Category:メモリ管理](https://ja.wikipedia.org/wiki/Category:メモリ管理 "wikilink") [Category:2003年のソフトウェア](https://ja.wikipedia.org/wiki/Category:2003年のソフトウェア "wikilink")

1.
2.
3.  [Who's using memcached?](http://www.danga.com/memcached/users.bml)