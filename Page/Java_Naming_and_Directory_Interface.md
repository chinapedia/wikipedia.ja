> この記事は[Java Naming and Directory Interface](https://ja.wikipedia.org/wiki/Java_Naming_and_Directory_Interface)から翻訳されています。


**Java Naming and Directory Interface**（**JNDI**）は、[ディレクトリ・サービス](../Page/ディレクトリ・サービス.md "wikilink")が提供するデータやオブジェクトを名前で発見（discover）し、参照（lookup）するのための[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。他の全ての[Java](https://ja.wikipedia.org/wiki/Java "wikilink") APIと同様、JNDIは他システムに対する[インターフェースであり](../Page/インタフェース_\(情報技術\).md "wikilink")、具体的な実装からは独立している。またJNDIには[サービス・プロバイダ・インターフェース](https://ja.wikipedia.org/wiki/サービス・プロバイダ・インターフェース "wikilink")（SPI）が規定されており、[フレームワークにディレクトリ](../Page/アプリケーションフレームワーク.md "wikilink")・サービスの実装を[プラグイン](../Page/プラグイン.md "wikilink")することができる。ディレクトリ・サービスの実装は[サーバ](../Page/サーバ.md "wikilink")でも[フラットファイルでも](https://ja.wikipedia.org/wiki/フラットファイルデータベース "wikilink")[データベース](../Page/データベース.md "wikilink")でもよく、サービスの提供側が任意に選択できる。

## 背景

[Java RMIや](../Page/Java_Remote_Method_Invocation.md "wikilink")[Java EEは](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")、ネットワーク上のオブジェクトを参照するためにJNDI APIを使用している。[Jini](../Page/Jini.md "wikilink")は独自のルックアップサービスを持っており、JNDIは使用していない。

JNDI APIには以下のものが含まれる。

  - 名前とオブジェクトを結びつける機構
  - 多様な照会方法に対応する階層構造の参照インターフェース
  - 要素がいつ更新されたかをクライアントに通知するイベントインターフェース
  - [LDAPの追加要件に対応するLDAP拡張](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")

SPIにより、以下のようなあらゆるネーミグ・サービスやディレクトリ・サービスに対応している。

  - [LDAP](../Page/Lightweight_Directory_Access_Protocol.md "wikilink")
  - [DNS](../Page/Domain_Name_System.md "wikilink")
  - [NIS](../Page/ネットワーク・インフォメーション・サービス.md "wikilink")
  - [RMI](../Page/Java_Remote_Method_Invocation.md "wikilink")
  - [CORBAネーム](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")・サービス
  - [ファイルシステム](../Page/ファイルシステム.md "wikilink")

JNDIの仕様は、[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")が[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")[3月10日](../Page/3月10日.md "wikilink")に公開した[1](http://www.sun.com/smi/Press/sunflash/1997-03/sunflash.970310.10204.html)。現在の最新バージョンは1.2で、J2SE 1.3以降の[Java SEに統合されている](../Page/Java_Platform,_Standard_Edition.md "wikilink")。

## ルックアップの基本

JNDIは名前を階層構造で管理している。名前はどのような文字列でもよい（例:"com.mydomain.ejb.MyBean"）。`Name`インターフェースを実装したオブジェクトを名前にすることも可能だが、文字列を使用する方が一般的である。ある名前に対応するオブジェクト、あるいはオブジェクトへの[参照を](../Page/参照_\(情報工学\).md "wikilink")、名前と一緒にディレクトリ・サービスに格納 (bind) することで、名前とオブジェクトが関連付けられる。

JNDI APIはオブジェクトを探す場所（これを[コンテクスト](../Page/コンテクスト.md "wikilink")という）の指定方法も規定している。

典型的なルックアップ処理では、まず最初に初期コンテクストを取得する。もっとも単純なケースで言うと、特定の実装と、その実装が要求するパラメータを指定して、初期コンテクストを生成する。初期コンテクストはディレクトリツリーやファイルシステムにおけるルートディレクトリのようなもので、初期コンテクストに対して名前のルックアップを行う。以下は、初期コンテクスト生成の例である。

`Hashtable args = new Hashtable();`
`// 最初にコンテクストファクトリーを指定する。`
`// JBossの実装やサンの実装、あるいは全く別のベンダーの実装などの中から`
`// どれを選ぶかという動作に相当する。`
`args.put( Context.INITIAL_CONTEXT_FACTORY, "com.jndiprovider.TheirContextFactory");`
`// 次に、データ保存場所のURLを指定する。`
`args.put( Context.PROVIDER_URL, "http://jndiprovider-database" );`
`// ここでなんらかの認証が必要な場合もある。`
`// 次に、初期コンテクストを生成する。`
`Context myCurrentContext = new InitialContext( args );`

いったん初期コンテクストが取得できると、それに対して名前と結び付けられたオブジェクトをルックアップできる。

`Object reference = myCurrentContext.lookup( "com.mydomain.MyBean" );`
`// EJBの場合、次の手順で`[`ナローイング`](https://ja.wikipedia.org/wiki/ナローイング "wikilink")が必要`。`
`MyBean myBean = (MyBean) PortableRemoteObject.narrow( reference, MyBean.class );`

## 検索

「ディレクトリ」とよばれる特殊なエントリには、属性を付与することができる。ディレクトリでは、属性を指定してオブジェクトを検索できる。ディレクトリはコンテクストの一種であるが、その[名前空間](../Page/名前空間.md "wikilink")は、ファイルシステム内のディレクトリ構造のようにある程度限定されている。

## 外部リンク

  - [サンのJNDIページ(英語)](http://java.sun.com/products/jndi/)

[Category:Java_enterprise_platform](https://ja.wikipedia.org/wiki/Category:Java_enterprise_platform "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")