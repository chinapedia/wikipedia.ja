> この記事は[CRUD](https://ja.wikipedia.org/wiki/CRUD)から翻訳されています。


**CRUD**（クラッド）とは、ほとんど全ての[コンピュータ](../Page/コンピュータ.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")が持つ[永続性](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink")\[1\]の4つの基本機能のイニシャルを並べた用語。その4つとは、**C**reate（生成）、**R**ead（読み取り）、**U**pdate（更新）、**D**elete（削除）である。[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")が備えるべき機能（情報の参照/検索/更新）を指す用語としても使われる。

CRUDの代わりに次のような単語の[イニシャル](https://ja.wikipedia.org/wiki/イニシャル "wikilink")を並べたもの、あるいは[頭字語](../Page/頭字語.md "wikilink")が使われることもある。

  - ABCD: add（追加）、browse（走査）、change（変更）、delete（削除）
  - ACID: add（追加）、change（変更）、inquire（問合せ）、delete（削除）— [トランザクション](../Page/トランザクション.md "wikilink")分野で使われる[ACIDと混同されやすい](../Page/ACID_\(コンピュータ科学\).md "wikilink")。
  - BREAD: browse（走査）、read（読み取り）、edit（編集）、add（追加）、delete（削除）
  - VADE(R): view（参照）、add（追加）、delete（削除）、edit（編集）（[トランザクション処理](https://ja.wikipedia.org/wiki/トランザクション処理 "wikilink")に関しては、さらに *restore*（復元））

## データベースアプリケーション

CRUD は[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")[アプリケーションや](../Page/アプリケーションソフトウェア.md "wikilink")[RESTfulな](https://ja.wikipedia.org/wiki/Representational_State_Transfer "wikilink")[Webアプリケーションで実装する必要のある主な機能を列挙したものと見ることができる](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")。各文字は標準の[SQL](../Page/SQL.md "wikilink")文に次のようにマッピング可能である。

| 名前     | 操作   | SQL                                                               |
| ------ | ---- | ----------------------------------------------------------------- |
| Create | 生成   | [INSERT](https://ja.wikipedia.org/wiki/INSERT_\(SQL\) "wikilink") |
| Read   | 読み取り | [SELECT](https://ja.wikipedia.org/wiki/SELECT_\(SQL\) "wikilink") |
| Update | 更新   | [UPDATE](https://ja.wikipedia.org/wiki/UPDATE_\(SQL\) "wikilink") |
| Delete | 削除   | [DELETE](https://ja.wikipedia.org/wiki/DELETE_\(SQL\) "wikilink") |

関係データベースはアプリケーションにとっての典型的な永続性層であるが、それ以外にも様々なものがある。CRUD は、[オブジェクトデータベース](https://ja.wikipedia.org/wiki/オブジェクトデータベース "wikilink")、[XMLデータベース](https://ja.wikipedia.org/wiki/XMLデータベース "wikilink")、[フラットファイルデータベース](https://ja.wikipedia.org/wiki/フラットファイルデータベース "wikilink")、特定のファイル形式などにも実装可能である。

[Google Scholar](https://ja.wikipedia.org/wiki/Google_Scholar "wikilink") では、CRUD を最初に使った論文として Kilov, H (1990) を挙げている\[2\]。その概念は Kilov (1998) でも詳述されている\[3\]。

## ユーザインタフェース

CRUD は、多くのアプリケーションのユーザインタフェースにも当てはまる。例えば、住所録（電話帳）ソフトでは、基本的な記録単位は個々の連絡先である。最も素朴なものでも、次のようなことが可能でなければならない。

  - 新たな連絡先情報を追加/生成できる。
  - 既存の連絡先情報を検索/表示できる。
  - 既存の連絡先情報を編集/更新できる。
  - 既存の連絡先情報を削除できる。

少なくともこれら4つの操作ができないと、そのソフトは完全とは言えない。これら機能は非常に基本的であるため、ひとまとめに解説されることが多い（「連絡先管理」など）。

## 脚注

[Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink") [Category:データベース](https://ja.wikipedia.org/wiki/Category:データベース "wikilink")

1.  [REST and CRUD: the Impedance Mismatch](http://weblog.infoworld.com/stratdev/archives/2007/01/rest_and_crud_t.html?source=NLC-STRADEVBLOG2007-02-01?source=NLC-STRADEVBLOG2007-02-01) InfoWorld、2007年1月29日
2.  Kilov, H (1990) [From semantic to object-oriented data modeling](http://ieeexplore.ieee.org/Xplore/login.jsp?url=/iel2/482/3754/00138704.pdf?arnumber=138704)、First International Conference on System Integration, 1990. 385 - 393.
3.  Haim Kilov (1998) [Business Specifications: The Key to Successful Software Engineering](http://www.amazon.com/dp/0130798444/)、Prentice Hall、ISBN 0-13-079844-4