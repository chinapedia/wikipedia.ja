> この記事は[Apache Commons Email](https://ja.wikipedia.org/wiki/Apache_Commons_Email)から翻訳されています。


**Apache Commons Email**（アパッチ・コモンズ・イーメール）は、[Apacheのトッププロジェクトである](../Page/Apacheソフトウェア財団.md "wikilink")[Apache Commonsにある](../Page/Apache_Commons.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[Java Mail上で動く](https://ja.wikipedia.org/wiki/Java_Mail "wikilink")[メールライブラリである](../Page/電子メール.md "wikilink")。動作させるには、Java Mail が必要である。

## 使用例

メールの送信。

    SimpleEmail email = new SimpleEmail();
    email.setHostName("mail.example.com");
    email.setAuthentication("username", "password");
    email.setCharset("ISO-2022-JP");
    email.setFrom("from@example.com", "送り元", "ISO-2022-JP")
         .addTo("to@example.com", "送り先", "ISO-2022-JP")
         .setSubject("テストタイトル")
         .setMsg("本文")
         .send();

## 脚注

## 外部リンク

  - [Apache Commons Email](http://commons.apache.org/email/)

[Category:Javaプラットフォーム](https://ja.wikipedia.org/wiki/Category:Javaプラットフォーム "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:Apacheソフトウェア財団](https://ja.wikipedia.org/wiki/Category:Apacheソフトウェア財団 "wikilink")