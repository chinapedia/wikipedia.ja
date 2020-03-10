> この記事は[IBATIS](https://ja.wikipedia.org/wiki/IBATIS)から翻訳されています。


**iBATIS** は、[SQL](../Page/SQL.md "wikilink")[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")を POJO ([Plain Old Java Object](https://ja.wikipedia.org/wiki/Plain_Old_Java_Object "wikilink")) にマッピングする[永続性](../Page/永続性.md "wikilink")フレームワークである。SQLクエリは[XMLファイルに置くことで一旦アプリケーションと分離される](../Page/Extensible_Markup_Language.md "wikilink")。検索結果のオブジェクトのマッピングは自動的か半自動的に行う。

iBATIS の基本となる考え方は、SQLクエリをXMLファイルに置くことで、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")にアクセスする際に必要となる大量の[Java](https://ja.wikipedia.org/wiki/Java "wikilink")コードを大幅に減らすことである。

例えば、データベースに **PRODUCT** (PRD_ID: *INTEGER*, PRD_DESCRIPTION: *VARCHAR*) という表があるとし、Javaのオブジェクト **com.example.Product** (id: *int*, description: *String*) があるとする。**Product** POJO の中に特定の **PRD_ID** の **PRODUCT** の内容を格納するには、以下を XML SQL マップに挿入する。

``` xml
 <select id="getProduct"
    parameterClass="java.lang.Long"
    resultClass="com.example.Product">
        select
            PRD_ID      as id,
            PRD_DESCRIPTION as description
        from
            PRODUCT
        where
            PRD_ID = #value#
 </select>
```

パラメータオブジェクトを設定して結果オブジェクトに格納するJavaコードは次のようになる。

``` java
Product resultProduct = sqlMapClient.queryForObject("getProduct", 123);
```

*\#value\#* はクエリで渡される Long を指す。パラメータがJavaオブジェクトなら、そのオブジェクトのプロパティから得られる値を似たような \# 記法を使ってクエリに挿入できる。例えばパラメータクラスが com.example.Product で、それに id というプロパティがある場合、\#value\# は \#id\# に置換できる。sqlMapClient は com.ibatis.sqlmap.client.SqlMapClient のインスタンスである。

iBATIS の創始者は[Java 5 への失望](http://clintonbegin.blogspot.com/2008/02/clintons-java-5-rant.html)を表明しており、2006年12月に 2.3.0 をリリースしてから 2.3.1 と 2.3.2 を2008年4月にリリースするまで長い時間を要したのは無関係ではない。

2010年6月16日、公式サイトにてApacheソフトウェア財団での活動中止と、プロジェクトの[フォーク](../Page/フォーク_\(ソフトウェア開発\).md "wikilink")、ならびに開発者の移籍がアナウンスされた。新プロジェクトは[MyBatis](https://ja.wikipedia.org/wiki/MyBatis "wikilink")と呼ばれている。

## 関連項目

  - [MyBatis](https://ja.wikipedia.org/wiki/MyBatis "wikilink")
  - [Hibernate](../Page/Hibernate.md "wikilink")
  - [Spring Framework](https://ja.wikipedia.org/wiki/Spring_Framework "wikilink")

## 外部リンク

  - [iBATIS @ Apache Foundation](http://ibatis.apache.org/)
  - [MyBatis](http://www.mybatis.org/)

[Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink") [Category:コンピュータ言語](https://ja.wikipedia.org/wiki/Category:コンピュータ言語 "wikilink")