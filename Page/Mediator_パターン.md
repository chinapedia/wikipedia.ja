> この記事は[Mediator パターン](https://ja.wikipedia.org/wiki/Mediator_パターン)から翻訳されています。


**Mediator パターン** は、[ソフトウェアのデザインパターンの一つで](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")、統一された[インタフェース](../Page/インタフェース_\(情報技術\).md "wikilink") のセットを提供するパターンである。 Mediator パターンは、[GoFによって記述された](https://ja.wikipedia.org/wiki/ギャング・オブ・フォー_\(情報工学\) "wikilink") 23 のパターンの一つであり、このパターンは、プログラムの動作する振る舞いを変更できるという点で、振る舞いに関するパターンと考えられている。

通常、プログラムは複数の（時には多数の）[クラスからなり](../Page/クラス_\(コンピュータ\).md "wikilink")、[ロジック](https://ja.wikipedia.org/wiki/ロジック "wikilink")と[計算](../Page/計算.md "wikilink")がクラスに配置される。しかし、プログラムでクラスの数が増えるに従い、特に[保守や](../Page/ソフトウェア保守.md "wikilink")[リファクタリングをする際](../Page/リファクタリング_\(プログラミング\).md "wikilink")、クラス間の[通信](../Page/通信.md "wikilink")の問題が複雑になり、プログラムを読んだり保守したりすることが困難になる。さらに、他のクラスに影響を与える可能性があるため、変更も難しくなる。

Mediator パターンを用いると、オブジェクト間の通信は *mediator* によってカプセル化され、オブジェクト同士で直接通信せず、*mediator* を介して行うようになる。これにより通信するオブジェクト同士の依存関係を削減し、[結合の度合いを下げることができる](../Page/結合度.md "wikilink")。

## 登場するクラス

  - Mediator (仲裁人、調停者):*Colleague (同僚)* オブジェクト間のコミュニケーションのインタフェースを定義する。
    ConcreteMediator:*Mediator* インターフェイスを実装し、*Colleague* オブジェクト間の通信を調整する。全ての *Colleague* の存在と、通信の目的について知っている。
    ConcreteColleague:*Mediator* を介して他の *Colleagues* と通信する。

## 関連項目

  - [デザインパターン (ソフトウェア)](https://ja.wikipedia.org/wiki/デザインパターン_\(ソフトウェア\) "wikilink")

## 外部リンク

  - [Mediator Pattern](http://www.javacamp.org/designPattern/mediator.html) in Java
  - [Mediator Pattern](http://www.dofactory.com/Patterns/PatternMediator.aspx) in C\#
  - [Jt](http://www.fsw.com/Jt/Jt.htm) JEE Pattern Oriented Framework

[Category:ソフトウェアパターン](https://ja.wikipedia.org/wiki/Category:ソフトウェアパターン "wikilink") [Category:デザインパターン_(ソフトウェア)](https://ja.wikipedia.org/wiki/Category:デザインパターン_\(ソフトウェア\) "wikilink")