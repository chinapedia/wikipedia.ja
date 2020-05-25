> この記事は[Windows Communication Foundation](https://ja.wikipedia.org/wiki/Windows_Communication_Foundation)から翻訳されています。


**Windows Communication Foundation**（**WCF**）は、[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 3.0における新しい通信サブシステムであり、アプリケーション同士をネットワーク経由で接続する仕組みである。開発時のコードネームは*Indigo*であった\[1\]。WCFアプリケーションは.NETでサポートされている言語なら、どの言語でも開発できる。

.NET Framework 3.0で新たに導入された4つの主な[APIの](../Page/アプリケーションプログラミングインタフェース.md "wikilink")1つである。[Windows Vistaと](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") [Windows Server 2008には最初から含まれている](../Page/Microsoft_Windows_Server_2008.md "wikilink")。[Windows XPと](../Page/Microsoft_Windows_XP.md "wikilink")[Windows Server 2003でもサポートされている](../Page/Microsoft_Windows_Server_2003.md "wikilink")。

## 概要

WCFのプログラミングモデルは、[Webサービス](../Page/Webサービス.md "wikilink")、[.NET Remoting](../Page/.NET_Remoting.md "wikilink")、[Distributed Transactions](../Page/Microsoft_Transaction_Server.md "wikilink")、 (MSMQ) を統合し、[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")のための[サービス指向アーキテクチャ](../Page/サービス指向アーキテクチャ.md "wikilink")モデルとしてまとめたものである。[RADの](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")[Webサービス](../Page/Webサービス.md "wikilink")開発の方法論を提供しつつ、ローカルなマシン上でも[LAN上でも](../Page/Local_Area_Network.md "wikilink")[インターネット](../Page/インターネット.md "wikilink")上でも単一の[プロセス間通信](../Page/プロセス間通信.md "wikilink")のAPIを使えるようにしている。WCFは.NETアプリケーション向けの全てのセキュリティモデルを提供している。

WCFでは、プロセス間の通信に[SOAPメッセージを使っている](../Page/SOAP_\(プロトコル\).md "wikilink")。従って、WCFベースでないアプリケーションともSOAPメッセージが使えるなら相互にやり取りが可能である。WCFプロセスが非WCFプロセスと通信する場合、SOAPメッセージは[XMLベースの符号化を施すが](../Page/Extensible_Markup_Language.md "wikilink")、WCFプロセス同士ならより最適化された[バイナリ](../Page/バイナリ.md "wikilink")形式の符号化をする。どちらの場合も SOAP 形式（[Infoset](https://ja.wikipedia.org/wiki/XML_Information_Set "wikilink")）に準拠している。

## サービス指向アーキテクチャ

WCFは[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")に[サービス指向アーキテクチャ](../Page/サービス指向アーキテクチャ.md "wikilink")の原則を持ち込んだものであり、この場合にサービスを受けるのは[クライアントである](../Page/クライアント_\(コンピュータ\).md "wikilink")。クライアントは複数のサービスを受けることができ、1つのサービスは複数のクライアントに提供される。典型的なサービスは[WSDLインターフェイスになっていて](../Page/Web_Services_Description_Language.md "wikilink")、任意のWCFクライアントがサービスを受けられるようになっており、どのプラットフォームでサービスが提供されているかは問わない。WCFには様々なWS標準が実装されている（[WS-Addressing](../Page/WS-Addressing.md "wikilink")、[WS-ReliableMessaging](https://ja.wikipedia.org/wiki/WS-ReliableMessaging "wikilink")、[WS-Security](../Page/WS-Security.md "wikilink")）。[マイクロソフト](../Page/マイクロソフト.md "wikilink")は[WS-Iのメンバーだが](../Page/Web_Services_Interoperability.md "wikilink")、WS-Iの決めた標準のうちどれを完全にサポートする予定なのかは不明である。

## WCFサービス

WCFサービスは3つの部分から成る。「サービス; service」クラスは提供すべきサービスを実装している。「ホスト環境; host environments」はサービスのための環境である。「エンドポイント; endpoints」は、クライアントと接続する部分である。WCFサービスとの通信は全てエンドポイントを通して行われる。エンドポイントには「コントラクト; contract」として、そのエンドポイントを通してServiceクラスのどのメソッドにアクセスできるかが指定されている。つまり、エンドポイントによって利用可能なメソッドが異なる場合もある。また、クライアントとの通信方法を指定する「バインディング; binding」があり、エンドポイントの存在するアドレスも指定されている。

WCFサービスのホストとしてはWindows Activation Servicesがある。他にも、IISをホストとすることもできるし、ServiceHostクラスを使った任意のプロセスをホストとすることができる。また、WCFサービス自身がホストとなることも可能である。

### WCFサービスの定義

WCFサービスクラスは、サービスをメソッド群として実装する。さらに、少なくとも1つのサービスコントラクトが定義され、そこにそのサービスが実行できる操作が定義される。オプションとしてデータコントラクトも定義でき、操作によって利用されるデータの種類を記述できる。

コントラクトは .NET Attributes を使って定義される。WCFサービスとして公開されるクラスには、*ServiceContract* 属性を付与するか、その属性が付与されたインターフェイスを実装する必要がある。クライアントが SOAP メッセージを使って呼び出せるメソッドには、*OperationContract* 属性を付与しなければならない。これらの属性によって WSDL の記述が自動的に生成され、クライアントはそれを参照可能となる。

1つのサービスに複数のサービスコントラクトを設けることもできる。これは複数の .NET インターフェイスを定義し、それぞれに ServiceContract 属性を付与することでなされる。サービスクラスには、それら全インターフェイスを実装する。

*ServiceContract* と *OperationContract* 属性はまた、既存の契約を参照するインターフェイスを持つこともでき、インターフェイスのバージョン付けも可能となっている。

サービスコントラクトには、明示的か暗黙かのデータコントラクトが必ず対応しており、そのサービスが使うデータを定義している。あるサービスが必要とするデータが単純な[型だった場合](../Page/データ型.md "wikilink")（[整数](../Page/整数.md "wikilink")、[浮動小数点数](../Page/浮動小数点数.md "wikilink")など）、WCF は自動的にデータコントラクトを定義する。一方、データが複雑な[オブジェクトや](../Page/オブジェクト_\(プログラミング\).md "wikilink")[構造体](../Page/構造体.md "wikilink")だった場合、明示的に定義しなければならない。データコントラクトは、データの[シリアライズ](../Page/シリアライズ.md "wikilink")方法を規定するものである。

データコントラクトは、DataContract 属性をクラスや構造体に付与することで定義される。サービスで使用される構造体メンバーには、DataMember 属性が付与されなければならない。そうすることで、その値がサービスとクライアント間で転送される。

サービスの通常の振る舞いと特定の操作は *ServiceBehavior* 属性と *OperationBehavior* 属性でそれぞれ制御される。ServiceBehavior 属性にはいくつかのプロパティがある。*ConcurrencyMode* プロパティは、サービスが同時並行して複数のクライアントに提供されるかどうかを示す。*InstanceMode* プロパティは、唯一のインスタンスで全要求に対応するのか、それとも要求毎に新たなインスタンスを生成するのか、あるいはセッション毎に生成するのかを指定する。

### エンドポイントの定義

WCFクライアントは、エンドポイントを通してWCFサービスと接続される。

各サービスは、1つ以上のエンドポイントを通してコントラクトを公開する。エンドポイントには[URLで示されるアドレスがあり](../Page/Uniform_Resource_Locator.md "wikilink")、バインディング・プロパティでデータの転送方式を指定する。

Address/Binding/Contract の三要素を "ABC" と称する。バインディングには、サービスにアクセスするのに使われる[通信プロトコル](../Page/通信プロトコル.md "wikilink")、セキュリティ機構の種類などが指定される。WCF には一般的な通信プロトコル向けの事前に定義されたバインディングがある（SOAP over HTTP、SOAP over TCP、SOAP over Message Queues など）。

クライアントがエンドポイント経由でサービスにアクセスする場合、コントラクトを知る必要があるだけでなく、バインディングに示された指示に従って通信しなければならない。すなわち、クライアントとサーバーには、互換性のあるエンドポイントが双方に存在することになる。

## サービスとの通信

WCFサービスとの通信をクライアントから見れば、メソッド呼び出しでサービスを利用しているように見え、一種の[RPC機構になっている](../Page/遠隔手続き呼出し.md "wikilink")。サービスの呼び出しはブロックされることがあり、クライアントはそのサービス要求が実行されるまで待たされる。クライアントはサービスとの接続に [Proxy パターン](../Page/Proxy_パターン.md "wikilink") を使用する必要がある。これにより、サービスのエンドポイントとの接続がオブジェクトとして抽象化される。proxy オブジェクトのメソッド呼び出しは、全てサービス要求となり、proxy はWCFサービスが返した結果を呼び出し側に返す。

WCF はローカルな proxy 生成を扱う。エンドポイントの設定に従って下位の処理を担当し、呼び出し側には必要な形式で結果を返す。

WCF はメッセージにサービスが使うデータを含ませて渡す呼び出し方だけでなく、ブロックされない呼び出し方法もサポートしている。メッセージを使った通信は必ずしも proxy オブジェクトを必要としない。その場合、戻ってくるデータもメッセージ形式で戻ってくる。呼び出し側はサービスの処理が完了するまでブロックされる。ブロックされないようにするには、メッセージキューを使ってメッセージの受け渡しをする必要がある。メッセージキューを使えば、サービスが一時的にダウンしている状態でもアプリケーションを実行し続けることができ、サービスが復旧したときに、溜まっていた要求が処理される。

## 脚注

## 関連項目

  - [Mono](../Page/Mono_\(ソフトウェア\).md "wikilink") - Mono 2.6からサポート
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")

## 参考文献

  - *Microsoft Windows Communication Foundation: Hands-On*, Craig McMurtry, Marc Mercuri, and Nigel Watling, SAMS Publishing, May 26, 2006. ISBN 0-672-32877-1

## 外部リンク

  - [Windows Communication Foundation](http://www.microsoft.com/japan/msdn/netframework/wcf/default.aspx), MSDN Windows Communication Foundation ポータル
  - [Windows Communication Foundation](http://wcf.netfx3.com/), Microsoft の WCF 情報サイト（英語）

{{.NET}}

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink")

1.  [WCF（Windows Communication Foundation）チュートリアル 前編 (1/5)：CodeZine（コードジン）](https://codezine.jp/article/detail/1157)