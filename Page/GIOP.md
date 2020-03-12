> この記事は[GIOP](https://ja.wikipedia.org/wiki/GIOP)から翻訳されています。


**GIOP**（General Inter-ORB Protocol）とは、[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")における[Object Request Broker](https://ja.wikipedia.org/wiki/Object_Request_Broker "wikilink")(ORB)間の抽象[プロトコルである](../Page/通信プロトコル.md "wikilink")。このプロトコルに関する標準規格は[Object Management Group](../Page/Object_Management_Group.md "wikilink")(OMG)が管理している。

**IIOP**（Internet Inter-ORB Protocol）とは、[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")上の **GIOP** の実装である。つまり、抽象プロトコルである GIOP の実体化である。

## メッセージ型

Object Management Group は GIOP を以下の3つに分けて定義している:

  - **The  (CDR)** - OMG IDL のデータ型を ORB 間などの低レベルな通信用表現にマッピングする規定
  - **The [Interoperable Object Reference](https://ja.wikipedia.org/wiki/Interoperable_Object_Reference "wikilink") (IOR)** - リモートオブジェクトへの参照の形式を規定。IOR はタグ付きプロファイルと各種情報を運ぶコンポーネントから構成される。典型的な IOR には、プロトコルのバージョン、サーバのアドレス、リモートオブジェクトを識別するバイト列（オブジェクトキー）からなる。
  - **The defined message formats** - オブジェクト要求を行ったり、オブジェクト実装を確定したり、通信路を管理するなどの目的で、メッセージがエージェント間で交換される。メッセージには以下のようなものがある:
      - *Request* - リモートメソッドの呼び出し
      - *Reply* - *Request* への応答メッセージ。通常、リモートメソッドから返されるデータを含む。場合によっては、サーバ側へのリダイレクション指示や例外記述が含まれる。
      - *CancelRequest* - 前に送った *Request* をキャンセルする（*Reply*を待たないことの宣言）。
      - *LocateRequest* - そのサーバがあるリモートオブジェクトをサポートしているかを確認するメッセージ。サポートしていない場合は、そのオブジェクトへの要求を送るべきアドレスを尋ねる。
      - *LocateReply* - *LocateRequest* への応答メッセージ。場合によってはそのリモートオブジェクトの新たなアドレスが含まれる。
      - *CloseConnection* - サーバから送られ、今後応答しないことを示す。
      - *MessageError* - 不正なメッセージへの応答として送られる。外部へのエラー通知には使われない（その場合は管理サーバからの*Request*に対する*Reply*でエラーを通知する）。
      - *Fragment* - 前のメッセージの続きを含むメッセージ。長いメッセージは分割して送られる。

## バイナリ形式

バイナリ形式でGIOPメッセージをダンプ表示すると、ヘッダが独特であるために即座に判別できる:

1.  4文字のASCII文字: G I O P
2.  2バイトのバージョン番号（1バイト目がメジャーバージョンで現在は 1 のみ）
3.  1バイトのメッセージフラグ。[LSBで](https://ja.wikipedia.org/wiki/最下位桁ビット "wikilink")[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")を示す（0 - ビッグエンディアン、1 - リトルエンディアン）。
4.  1バイトのメッセージ型（*Reply*、*Request*、*Fragment*などを示す）
5.  4バイトのメッセージ長（ヘッダ部は含めない）

メッセージは整数タグ付きの任意のデータフラグメントの転送にも使われる。そのようなデータフラグメントはサービスコンテクストと呼ばれ、必要に応じて通信標準規格を拡張するのに使われる。例外を投げるサービスコンテキスト、文字コードを指定するサービスコンテキストなどが標準で用意されている。クライアントとサーバのインターセプターでメッセージにサービスコンテキストを付加してやり取りすることも可能である。

## GIOP という略称の法的状態

[CORBA](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")、IIOP、OMG などの略称は Object Management Group の登録商標であり、利用には注意が必要である。しかし、GIOP は登録商標ではない（[list of OMG marks](http://www.omg.org/legal/tm_list.htm)参照）。したがって、場合によっては GIOP という用語を使った方がよい。

## 外部リンク

  - [The official CORBA and GIOP standard](http://www.omg.org/docs/formal/04-03-12.pdf)（約 10 MB）
  - [Formalization and Validation of the General Inter-ORB Protocol (GIOP) Using Promela and SPIN](http://tele.informatik.uni-freiburg.de/Research/fmvdoos.htm)
  - Java RMI over IIOP [Overview](http://java.sun.com/products/rmi-iiop/) and [Guide](http://java.sun.com/javase/6/docs/technotes/guides/rmi-iiop/)

[Category:オブジェクト指向](https://ja.wikipedia.org/wiki/Category:オブジェクト指向 "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")