> この記事は[Indexed Sequential Access Method](https://ja.wikipedia.org/wiki/Indexed_Sequential_Access_Method)から翻訳されています。


**Indexed Sequential Access Method**（索引付き順次アクセス方式、さくいんつきじゅんじあくせすほうしき、一般に**ISAM**）とは高速にアクセスが可能なデータの格納方法 ([ファイル編成法](../Page/ファイル編成法.md "wikilink")) の一つである。[IBM](../Page/IBM.md "wikilink")で開発され、今日では[関係データベース管理システム](../Page/関係データベース管理システム.md "wikilink") (RDBMS、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")) をはじめとするほとんど全ての[データベース管理システム](../Page/データベース管理システム.md "wikilink") (DBMS) でのデータの格納に用いられている。

ISAMを用いたシステムではデータは[固定長](https://ja.wikipedia.org/wiki/固定長 "wikilink")の[レコード](../Page/レコード.md "wikilink")として格納される。当時の設計思想は[磁気テープ](../Page/磁気テープ.md "wikilink")の[記憶装置に高速で書き込むためにレコードを連続的に格納していくものだった](../Page/補助記憶装置.md "wikilink")。もう一つのデータとしてテーブルの内容への[ポインタを格納した](../Page/ポインタ_\(プログラミング\).md "wikilink")[ハッシュテーブル](../Page/ハッシュテーブル.md "wikilink")を[索引](../Page/索引.md "wikilink")として用いることで、全データを検索することなく目的のデータを取り出すことを可能とした。

ISAMの実現は他のデータへのポインタがレコード内に格納されていた[ナビゲーショナルデータベース](../Page/ナビゲーショナルデータベース.md "wikilink")からの脱却を実現した。ISAMによる主要な利点は索引のサイズが小さく、高速な検索が可能で、必要なデータのみに直接アクセス可能としたことにある。それに加えてデータの変更が行われた場合にも、該当するデータのみの変更で済ますことが可能であり、関連する他のデータまで波及して変更を加える必要がないことも利点となった。

[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")はテーブル同士のリンクを正常に維持するロジックが追加されるISAM方式と組み合わせての実装が行いやすい。代表的な例として、[外部キー](../Page/外部キー.md "wikilink")として使われる[フィールド](../Page/フィールド.md "wikilink")の高速な検索のために索引が用いられる。 これは関連するデータへのポインタをレコードに直接格納する方法よりも遅い処理となるが、データの物理的な構成の変更があった場合でもリンクが正常に保たれるため、ポインタを書き換える必要がない。

ISAMはファイルへの直接の、順番に従ったアクセス方式であり，非常にわかりやすく実装も容易である。また、非常に高速なアクセス方式でもある。逆にISAMの欠点はそれぞれの[クライアントマシンがアクセスしているファイルへの自身の接続状態を管理しなければならないことにある](../Page/クライアント_\(コンピュータ\).md "wikilink")。これは一方で複数のデータの追加動作が衝突し、データが矛盾した状態に陥る可能性につながっている。一般的にこの問題は[クライアントサーバモデルの導入によってサーバがクライアントの要求を](https://ja.wikipedia.org/wiki/サーバ#クライアント・サーバ・モデル "wikilink")[直列化して扱うことによって解決されている](../Page/シリアライズ.md "wikilink")。これは格納されたデータに対してクライアント側のレイヤーに存在している[SQL](../Page/SQL.md "wikilink")の[トランザクション](../Page/トランザクション.md "wikilink")概念の基礎となっている。

IBMではISAMの代わりに[VSAM](https://ja.wikipedia.org/wiki/Virtual_storage_access_method "wikilink") (Virtual Storage Access Method; 仮想記憶アクセス方式)と呼ばれる技術を用いるようになった。

[Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink") [Category:データ構造](https://ja.wikipedia.org/wiki/Category:データ構造 "wikilink") [Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink")