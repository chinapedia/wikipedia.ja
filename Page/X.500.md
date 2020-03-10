> この記事は[X.500](https://ja.wikipedia.org/wiki/X.500)から翻訳されています。


**X.500** は、電子[ディレクトリ・サービス](https://ja.wikipedia.org/wiki/ディレクトリ・サービス "wikilink")に関するコンピュータネットワーク標準規格のシリーズである。X.500 シリーズは [ITU-T](../Page/ITU-T.md "wikilink")（かつてのCCITT）が開発した。このディレクトリ・サービスは、[X.400](https://ja.wikipedia.org/wiki/X.400 "wikilink") 電子メール交換および名前参照からの要求に応えるべく開発されたものである。[ISOは標準の開発過程で協力し](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")、X.500 を[開放型システム間相互接続](https://ja.wikipedia.org/wiki/開放型システム間相互接続 "wikilink") (OSI) プロトコルスイートの一部とした。ISO では **ISO/IEC 9594** とされている。

## X.500 プロトコル

X.500 で定義されているプロトコルには、以下のものがある。

  - **DAP** (Directory Access Protocol)
  - **DSP** (Directory System Protocol)
  - **DISP** (Directory Information Shadowing Protocol)
  - **DOP** (Directory Operational Bindings Management Protocol)

これらのプロトコルがOSIネットワーキングスタックを使っているので、インターネットクライアントが[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")スタックを使って X.500 ディレクトリにアクセスできるよう DAP の代替プロトコルがいくつか開発された。最も広く使われている代替プロトコルとしては Lightweight Directory Access Protocol ([LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")) がある。DAP と他の X.500 プロトコルは今では TCP/IP 上で使えるようになっているが、LDAP は今でもディレクトリアクセスのプロトコルとして一般に使われている。

## X.500 データモデル

X.500 の中核となる概念は、単一の[ディレクトリ情報ツリー](https://ja.wikipedia.org/wiki/ディレクトリ情報ツリー "wikilink") (DIT) が存在し、エントリ群の階層構造が複数の[サーバ](../Page/サーバ.md "wikilink")に分散しているというものである。各エントリは属性の組合せであり、各属性は1つ以上の値を持つ。各エントリにはユニークな識別名があり、相対識別名 (RDN) とそのエントリの1つ以上の属性、階層上の上位にあたるエントリ群の RDN から構成される。LDAP も X.500 とよく似たデータモデルを実装しているので、詳しくは [LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink") の項目を参照されたい。

X.520 と X.521 は、DIT のエントリとして人物や組織を表すために使われる属性群とオブジェクトクラス群を定義しており、White pages（個人別電話帳）スキーマとして広く使われている。

[X.509](https://ja.wikipedia.org/wiki/X.509 "wikilink") は認証フレームワークを提供する標準であり、X.500 ディレクトリプロトコルの範囲を超えて広く使われている。X.509 は公開鍵認証の標準形式を規定している。

## X.500 シリーズ標準

| ITU-T 番号                                                | [ISO/IEC](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink") 番号 | 標準規格名                                                                        |
| ------------------------------------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| X.500                                                   | ISO/IEC 9594-1                                                 | The Directory: Overview of concepts, models and services                     |
| X.501                                                   | ISO/IEC 9594-2                                                 | The Directory: Models                                                        |
| [X.509](https://ja.wikipedia.org/wiki/X.509 "wikilink") | ISO/IEC 9594-8                                                 | The Directory: Authentication framework                                      |
| X.512                                                   | ISO/IEC 9594-3                                                 | The Directory: Abstract service definition                                   |
| X.518                                                   | ISO/IEC 9594-4                                                 | The Directory: Procedures for distributed operation                          |
| X.519                                                   | ISO/IEC 9594-5                                                 | The Directory: Protocol specifications                                       |
| X.520                                                   | ISO/IEC 9594-6                                                 | The Directory: Selected attribute types                                      |
| X.521                                                   | ISO/IEC 9594-7                                                 | The Directory: Selected object classes                                       |
| X.525                                                   | ISO/IEC 9594-9                                                 | The Directory: Replication                                                   |
| X.530                                                   | ISO/IEC 9594-10                                                | The Directory: Use of systems management for administration of the Directory |

## 外部リンク

  -
  - [X500Standard.com](http://www.x500standard.com/)

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink") [Category:アイデンティティ管理システム](https://ja.wikipedia.org/wiki/Category:アイデンティティ管理システム "wikilink")