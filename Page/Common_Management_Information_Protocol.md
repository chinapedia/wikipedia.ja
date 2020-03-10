> この記事は[Common Management Information Protocol](https://ja.wikipedia.org/wiki/Common_Management_Information_Protocol)から翻訳されています。


**Common Management Information Protocol**（**共通管理情報プロトコル**、**CMIP**）は、[ネットワーク管理](../Page/ネットワーク管理.md "wikilink")のための[通信プロトコル](../Page/通信プロトコル.md "wikilink")であり、ネットワーク管理アプリケーションと管理対象との通信を定義している。[ISO](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")/[IEC](https://ja.wikipedia.org/wiki/IEC "wikilink") [JTC 1と](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")[ITU-T](../Page/ITU-T.md "wikilink")が開発した[OSIのネットワーク管理モデルを規定した](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink")[ITU-T](../Page/ITU-T.md "wikilink") **X.700**シリーズ勧告において、プロトコル仕様 X.711 として定義されている。ISO/IEC規格では ISO/IEC 9596-1、JIS規格では JIS X 5762として規定されている。同様のプロトコルとして [IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") の設計した[SNMPの方が一般に広く使用されている](../Page/Simple_Network_Management_Protocol.md "wikilink")。

CMIP は管理対象に関する管理情報を定義し、管理対象に何らかのアクションを行わせたり、アクションを変更したりすることが可能である。管理対象は [GDMO](https://ja.wikipedia.org/wiki/GDMO "wikilink")（Guidlines for Definition of Managed Objects … [X.722](https://ja.wikipedia.org/wiki/X.722 "wikilink")）に従って記述され、X.500 ディレクトリサービスのように識別名で識別される。

CMIPの定義におけるネットワーク管理システムは以下のような操作を行うことができる:

  - CREATE - 管理対象オブジェクトのインスタンスを生成
  - DELETE - 管理対象オブジェクトのインスタンスを消去
  - GET - 管理対象オブジェクトのインスタンスの値を要求する
  - CANCEL_GET - 既に発行した GET 要求を取り消す
  - SET - 管理対象オブジェクトのインスタンスの値を設定する
  - ACTION - 管理対象オブジェクトに定義されたようにアクションを行うよう要求する

管理対象機器上の管理エージェントは以下の操作を行うことができる:

  - EVENT_REPORT - ネットワーク管理システムに何らかの通知や警告を送る

CMIP はセキュリティに関してもよく考慮されており、ネットワークの異常事態についても柔軟な報告が可能である。

## 歴史

CMIP は [SNMPへの対抗として設計され](../Page/Simple_Network_Management_Protocol.md "wikilink")、SNMP よりはるかに強力な機能を持っていた。例えば、管理対象機器の状態を変更する方法が、SNMP では "set" しかないのに対して、CMIPでは任意のアクションを定義できるようになっていた。CMIP は通信キャリアー網の国際標準である Telecommunications Management Network の鍵となる技術であり、組織間、ベンダー間をまたいだネットワーク管理を可能にするとされていた。

しかし、インターネットでは SNMP をサポートする機器が圧倒的に多かった。その原因は CMIP が複雑であるため、実装にかかるコストの問題があったからである。CMIP は主に通信キャリアーが使用するような機器でサポートされている。

## 参考文献

  - RFC 1095 （The Common Management Information Services and Protocol over TCP/IP）
  - RFC 1189 （The Common Management Information Services and Protocols for Internet）
  - [List of ITU X-series recommendations](http://www.itu.int/rec/T-REC-X/en) X.700シリーズにCMIPが定義されている。

[Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:ネットワーク管理](https://ja.wikipedia.org/wiki/Category:ネットワーク管理 "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")