> この記事は[Java Message Service](https://ja.wikipedia.org/wiki/Java_Message_Service)から翻訳されています。


**Java Message Service** (JMS) とは[Java](https://ja.wikipedia.org/wiki/Java "wikilink")[プログラムに](../Page/プログラム_\(コンピュータ\).md "wikilink")[ネットワークを介して](https://ja.wikipedia.org/wiki/コンピュータネットワーク "wikilink")[データ](../Page/データ.md "wikilink")を送受信させるための[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。

[Java EE](../Page/Java_Platform,_Enterprise_Edition.md "wikilink") 1.3 以降に標準で含まれている。データを1つずつバラバラに扱うのではなく、[メッセージと呼ばれる塊にまとめて送信する](https://ja.wikipedia.org/wiki/メッセージ_\(コンピュータ\) "wikilink")[メッセージング](https://ja.wikipedia.org/wiki/メッセージング "wikilink")を行う。1対1のキューと1対多のトピックが使える。受信は、MessageConsumer.receive() による同期受信のほか、MessageListener を使った非同期受信もできる。

## メッセージングの一般的な概念

メッセージングとは、疎結合分散通信形式のひとつの形式である。この文脈上での"通信"とはソフトウェアコンポーネント間のメッセージ交換である。

メッセージ指向技術は、キューのような仲介役のコンポーネントの導入によって密結合通信（TCPネットワークソケット、CORBA、[RMIのような](https://ja.wikipedia.org/wiki/Java_Remote_Method_Invocation "wikilink")）を緩和する。このアプローチによって、ソフトウェアコンポーネントがお互いに"間接的に"通信するようになる。このメリットは、キューを使用して通信する場合に、メッセージ送信者が正確に受信者を知る必要がないということも含んでいる。

## モデル

JMS API は二つのモデルをサポートする。

  - 1対1：[ポイント・ツー・ポイント](https://ja.wikipedia.org/wiki/ポイント・ツー・ポイント "wikilink")（キュー）
  - 1対多：[出版-購読型モデル](https://ja.wikipedia.org/wiki/出版-購読型モデル "wikilink")（トピック）

### ポイント・ツー・ポイント

ポイント・ツー・ポイントにおいて、送信者は特定のキューにメッセージを送信し受信者はそのキューからメッセージを読み込む。 ここで送信者は、メッセージの宛先を知っていて、受信者のキューに対して直接メッセージを送信している。これは、次のことを特色づける。

  - ただ一人だけの消費者がメッセージを取得できる。
  - 生産者は、消費者がメッセージを消費するときに、稼働していなくてもよい。また、消費者もメッセージが送信されたときに稼働していなくてもよい。

### 出版-購読型モデル

出版-購読型モデルでは、特定のメッセージトピックに対してメッセージを出版することができる。購読者は、受信対象のメッセージトピックに対して購読要求を行う。このモデルでは、出版者と購読者がお互いに知ることがない。比喩として掲示板が挙げられる。

このモデルの特徴を以下に挙げる。

  - 複数の購読者が、メッセージを取得できる。
  - 出版者と購読者は同時に稼働しないといけない。

出版者は、クライアントが購読可能になるためにサブスクリプションを生成しなくてはいけない。購読者は、持続的なサブスクリプションが確立されている間、継続的に受信し続ける。

## コネクション確立

JMSは、アプリケーションをデータの転送レイヤから切り離す方法を提供する。 同じくJavaクラスは、プロバイダを要求するJNDIを使用することによって、異なるJMSプロバイダを通信を行うために利用することができる。 始めに、キューかトピックに接続するためにconnection factoryを使用し、そしてメッセージを送信、もしくは出版する。 受信者側では、メッセージを受信、もしくは購読する。

## メッセージ

メッセージは本文・ヘッダー・プロパティの3要素からなる。

メッセージ本文には以下の5種類を利用できる。

  - テキスト
  - マップ (Map)
  - オブジェクト (Serializable)
  - ストリーム (Stream)
  - バイト配列

プロパティの値としては String もしくは各種プリミティブ型の値が利用できる。プロパティに基づいてメッセージセレクタが利用できる。メッセージセレクタの構文は [SQL](../Page/SQL.md "wikilink")92 条件式構文のサブセット。LIKE 演算子や中間一致も利用可能。

ヘッダーにはいろいろな項目がある。

  - JMSReplyTo ヘッダーでは、返信して欲しいキューもしくはトピックスを指定して、メッセージを処理した後、返信メッセージを送って欲しい送り先を指定することができる。
  - JMSCorrelationID ヘッダーでどのメッセージに対する返信かというのを表現できる。
  - JMSPriority ヘッダーで配信の優先順位を指定できる。
  - JMSDeliveryMode ヘッダーで、メッセージをストレージに永続化するかどうか指定できる。

## 利用例

### コネクション確立

コネクション確立は以下のようにして行う。最初の1行目は、[Apache ActiveMQ](https://ja.wikipedia.org/wiki/Apache_ActiveMQ "wikilink") の場合であり、実装によって異なる。

``` java
ConnectionFactory connectionFactory = new ActiveMQConnectionFactory("tcp://localhost:61616");
Connection connection = connectionFactory.createConnection();
// ここでメッセージの受信のリスナーの登録を行う
connection.start();
// ここでメッセージの送信を行う
connection.close();
```

### 出版-購読型モデル

出版-購読型モデルは以下のようにして行う。以下、送信側の例。

``` java
Session session = connection.createSession(false, Session.AUTO_ACKNOWLEDGE);
Topic testTopic = session.createTopic("testTopic");
MessageProducer producer = session.createProducer(testTopic);
producer.send(session.createTextMessage("Hello JMS"));
```

以下、受信側の例。

``` java
Session session = connection.createSession(false, Session.AUTO_ACKNOWLEDGE);
Topic testTopic = session.createTopic("testTopic");
MessageConsumer consumer = session.createConsumer(testTopic);
consumer.setMessageListener(new MessageListener() {
    public void onMessage(Message message) {
        try {
            System.out.println(((TextMessage) message).getText());
        } catch (JMSException e) {
        }
    }
});
```

### ブローカーの起動

ブローカーの起動方法は実装によってまちまちである。別プロセスとして動作させることもできるし、Java VM 内に埋め込む（共存させる）事もできる。例えば、Apache ActiveMQ の場合、`new BrokerService().start();` で埋め込みブローカーが起動でき、埋め込みブローカーに対しては `vm://localhost` で通信できる。

## 実装

以下のソフトウェアで実装されている。

  - [Apache ActiveMQ](https://ja.wikipedia.org/wiki/Apache_ActiveMQ "wikilink")

  - \- [AMQPを使用](https://ja.wikipedia.org/wiki/Advanced_Message_Queuing_Protocol "wikilink")

  - EMS -

  - FioranoMQ - フィオラノ ソフトウェア

  - \- OpenJMS Group

  - ,  - [レッドハット](../Page/レッドハット.md "wikilink") ([JBoss](https://ja.wikipedia.org/wiki/JBoss "wikilink"))

  - \- [OW2 Consortium](https://ja.wikipedia.org/wiki/OW2_Consortium "wikilink")

  - [OpenMQ](https://ja.wikipedia.org/wiki/OpenMQ "wikilink") - [オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")（[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")）

  - ,  - [オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")

  - [RabbitMQ](https://ja.wikipedia.org/wiki/RabbitMQ "wikilink") - [AMQPを使用](https://ja.wikipedia.org/wiki/Advanced_Message_Queuing_Protocol "wikilink")

  - Solace JMS -

  - SonicMQ -

  - StormMQ - [AMQPを使用](https://ja.wikipedia.org/wiki/Advanced_Message_Queuing_Protocol "wikilink")

  - SwiftMQ

  - [WebSphere Application Server](https://ja.wikipedia.org/wiki/WebSphere_Application_Server "wikilink") - [IBM](../Page/IBM.md "wikilink")

  - [WebSphere MQ](https://ja.wikipedia.org/wiki/WebSphere_MQ "wikilink")- [IBM](../Page/IBM.md "wikilink")

## 歴史

  - 2001年6月25日 - 1.0.2b リリース
  - 2002年3月18日 - 1.1 リリース
  - 2013年5月21日 - 2.0 リリース

## 関連項目

  - [Java Transaction API](https://ja.wikipedia.org/wiki/Java_Transaction_API "wikilink")
  - [メッセージ指向ミドルウェア](https://ja.wikipedia.org/wiki/メッセージ指向ミドルウェア "wikilink")

## 外部リンク

  - [Java Message Service (JMS)](http://www.oracle.com/technetwork/java/index-jsp-142945.html)
  - [Java Message Service API](http://docs.oracle.com/javaee/7/api/javax/jms/package-summary.html)
  - [The Java EE 6 Tutorial - Java Message Service](http://docs.oracle.com/javaee/6/tutorial/doc/bncdq.html)

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink") [Category:API](https://ja.wikipedia.org/wiki/Category:API "wikilink") [Category:Java_specification_requests](https://ja.wikipedia.org/wiki/Category:Java_specification_requests "wikilink") [Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink")