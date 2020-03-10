> この記事は[Data Transfer Object](https://ja.wikipedia.org/wiki/Data_Transfer_Object)から翻訳されています。


**Data Transfer Object**（**DTO**）は[デザインパターンの一種で](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")、[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")のサブシステム間でデータを転送するのに使う。過去、J2EE第一版においては**Value Objects**（**VO**）と呼ばれていた。なお、[マーティン・ファウラー](https://ja.wikipedia.org/wiki/マーティン・ファウラー "wikilink")が著書「Patterns of Enterprise Application Architecture」において示した「Value Object」はこれとは意味が異なる\[1\]。[Data Access Object](../Page/Data_Access_Object.md "wikilink") と組み合わせて、[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")からデータを検索するのに使うことも多い。

Data Transfer Object と[ビジネスオブジェクト](../Page/ビジネスオブジェクト.md "wikilink")や Data Access Object との違いは、DTO が自身のデータの格納と取り出し機能（アクセサ[メソッドとミューテータメソッド](https://ja.wikipedia.org/wiki/メソッド_\(計算機科学\) "wikilink")）しか持たない点である。

## 脚注

<references/>

## 外部リンク

  - [Core J2EE Patterns - Transfer Object](http://java.sun.com/blueprints/corej2eepatterns/Patterns/TransferObject.html)
  - [Core J2EE Patterns - Data Access Object](http://java.sun.com/blueprints/corej2eepatterns/Patterns/DataAccessObject.html)
  - [Abuses of DTO pattern in Java World](http://anirudhvyas.com/root/2008/04/19/abuses-of-dto-pattern-in-java-world/)
  - [Data Transfer Object - Microsoft MSDN Library](http://msdn.microsoft.com/en-us/library/ms978717.aspx)
  - [DTO(Data Transfer Object)の必要性](http://architect360.apricot-jp.com/300/dtodata_transfer_object.html) アーキテクト360

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink")

1.  [マーティン・ファウラーのblikiのValue Objectの解説(英語)](http://martinfowler.com/bliki/ValueObject.html)