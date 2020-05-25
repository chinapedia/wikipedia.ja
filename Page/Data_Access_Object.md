> この記事は[Data Access Object](https://ja.wikipedia.org/wiki/Data_Access_Object)から翻訳されています。


**Data Access Object**（**DAO**）とは、ある種の[データベース](../Page/データベース.md "wikilink")や[永続性機構の抽象化された](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink")[インタフェースを提供する](../Page/インタフェース_\(情報技術\).md "wikilink")[オブジェクトであり](../Page/オブジェクト_\(プログラミング\).md "wikilink")、データベースの詳細を開示することなく特定の操作を提供する。

なお、[マイクロソフト](../Page/マイクロソフト.md "wikilink")のライブラリである [Data Access Object**s**](https://ja.wikipedia.org/wiki/Data_Access_Objects "wikilink") とは直接の関係はない。

## 概要

Data Access Object は問題を、ドメイン固有のオブジェクトとデータ型を使ってアプリケーションにどのようなデータアクセスが必要であるかという点（DAOの公開インタフェース）と、それらのニーズを特定のDBMSやデータベーススキーマでどのように満足するかという点（DAOの実装）に分離する。

この[デザインパターンは多くの](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")で利用可能であり、多くの永続性を必要とするアプリケーションや多くのデータベースで利用可能である。しかし、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")の[ベストプラクティス](../Page/ベストプラクティス.md "wikilink")ガイドライン\[1\] ("Core [J2EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") Patterns") が発祥であるため、[JDBC](../Page/JDBC.md "wikilink") API を経由して [Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") から[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")にアクセスする際に適用されることが多い。

## 利点

DAOを利用する際の利点は、アプリケーションの重要な2つの部分間の比較的単純で厳密な分離を可能にする点であり、それによって各部が互いのことをほとんど知らなくて済むようにし、独立に修正可能となる。[ビジネスロジック](../Page/ビジネスロジック.md "wikilink")の変化は、インタフェースが正しく実装される限り、DAOクライアントに影響しない。

[Java](https://ja.wikipedia.org/wiki/Java "wikilink") に関しては、Data Access Object は数々の複雑で多様な [Java 永続性技術](../Page/Java_Persistence_API.md "wikilink")（[JDBC](../Page/JDBC.md "wikilink")、[JDO](../Page/Java_Data_Objects.md "wikilink")、[EJB CMP](../Page/Enterprise_JavaBeans.md "wikilink")、[TopLink](https://ja.wikipedia.org/wiki/TopLink "wikilink")、[Hibernate](../Page/Hibernate.md "wikilink")、[iBATIS](https://ja.wikipedia.org/wiki/iBATIS "wikilink")など）からアプリケーション本体を隔離するのに利用される。Data Access Object を使うと、基盤となる技術を更新/置換しても、アプリケーションの他の部分を変更する必要がない。

## 脚注

### 注釈

### 出典

## 関連項目

  - [デザインパターン (ソフトウェア)](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")
  - [オブジェクト関係マッピング](../Page/オブジェクト関係マッピング.md "wikilink")
  - [Data Transfer Object](../Page/Data_Transfer_Object.md "wikilink") (DTO)
  - [Service Data Objects](../Page/Service_Data_Objects.md "wikilink") (SDO)

## 外部リンク

  - [サルでもわかる 逆引きデザインパターン - DAO (Data Access Object)](http://www.nulab.co.jp/designPatterns/designPatterns3/designPatterns3-4.html)

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:対象](https://ja.wikipedia.org/wiki/Category:対象 "wikilink")

1.