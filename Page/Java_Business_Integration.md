> この記事は[Java Business Integration](https://ja.wikipedia.org/wiki/Java_Business_Integration)から翻訳されています。


**Java Business Integration**（略称JBI）とは、[エンタープライズ・サービス・バス](../Page/エンタープライズ・サービス・バス.md "wikilink")（、ESB）を[Java](https://ja.wikipedia.org/wiki/Java "wikilink")で実装する方法を示した[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")である。

## コンポーネント

JBI 1.0では、ESBのバスにあたるノーマライズメッセージルータやバスにつながるコンポーネントのうち、メッセージ変換やメッセージルーティングのようにESB内部に作用する[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")をサービスエンジン、[SOAPや](../Page/SOAP_\(プロトコル\).md "wikilink")[JMSのような通信プロトコルを用いてESBの外部との接続の窓口となるコンポーネントをバインディングコンポーネントと定義している](../Page/Java_Message_Service.md "wikilink")。 これらの2種類のコンポーネントは、JBI仕様の中でインタフェースが決められており、その実装クラスとコンポーネント名などを記述したjbi.xmlという配備記述子を封入した[JARファイルであり](https://ja.wikipedia.org/wiki/JAR_\(ファイルフォーマット\) "wikilink")、誰でも作ることができるので、独自の通信[プロトコル](../Page/プロトコル.md "wikilink")や機能を実装できる。しかし、一般ユーザが実装するには難しく、現実にはベンダー製のもの、あるいは[オープンソース](../Page/オープンソース.md "wikilink")で実装されるのを待たなければならないのもまた事実である。

## サービスアセンブリ

JBIでは[コンポーネント](https://ja.wikipedia.org/wiki/コンポーネント "wikilink")に[エンドポイント](https://ja.wikipedia.org/wiki/エンドポイント "wikilink")名、サービス名、[インタフェース名](../Page/インタフェース_\(情報技術\).md "wikilink")、[オペレーション](https://ja.wikipedia.org/wiki/オペレーション "wikilink")名、その他コンポーネント独自の設定を与えてコンポーネントを活性化させ、[インスタンス](../Page/インスタンス.md "wikilink")を起動させるものを「サービスアセンブリ」と定義している。 サービスアセンブリは、前述した設定事項をWSDL1.1/2.0（タグを拡張する部分はコンポーネントごとに独自形式）やコンポーネントが独自に読み込む設定[ファイルに書き込み](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")、既定の形で[ZIP](https://ja.wikipedia.org/wiki/ZIP "wikilink")ファイルに封入し、JBIコンテナに配備するという方法で運用する。このように、理論的には実装クラスとサービスを独立なライフサイクルで扱えるのがJBIの利点と言える。

ノーマライズメッセージルータを流れるメッセージは「メッセージエクスチェンジ」と呼ばれるものであり、内容はJavaのプロパティの塊そのものであり、その中にWebサービスではなじみ深いエンドポイント名、サービス名、インタフェース名 (PortType)、オペレーション名、ノーマライズメッセージ、その他のプロパティを書き込み、これをメッセージルータにsendすることで、指定したエンドポイントに運ばれる。なお、ノーマライズメッセージは、(javax.xml.transform.Source) と定義されたコンテント、(javax.activation.DataHandler) と定義された添付ファイル、その他のプロパティで構成され、おおよそSOAPメッセージの形式を継承したような設計になっている。コンテントは[XMLが入るが](../Page/Extensible_Markup_Language.md "wikilink")、Sourceになっていることにより、[DOM](../Page/Document_Object_Model.md "wikilink")、[SAX](../Page/Simple_API_for_XML.md "wikilink")、[StAXなどのあらゆる](../Page/Streaming_API_for_XML.md "wikilink")[APIでの処理が可能になっている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。しかし、経由するコンポーネントでのXML処理方法を統一していなければ、DOM、SAX、Streamのどの形式のインスタンスでメッセージが来ても処理できるようにしておく必要がある。

## 各社対応

現在、JBIに対応した実装を行っているものとしては、[Open ESB](https://open-esb.dev.java.net/)、NECの[WebOTX Enterprise Service Busなどがある](https://ja.wikipedia.org/wiki/WebOTX "wikilink")。多くの[ベンダー](https://ja.wikipedia.org/wiki/ベンダー "wikilink")がESB製品をリリースしているが、JBI対応を掲げているところは少ない。その理由は、仕様策定段階で、[IBM](../Page/IBM.md "wikilink")、[BEAシステムズ](../Page/BEAシステムズ.md "wikilink")が強烈な反対票を入れていることによるものと考えられ、その状況は最新のJBI 2.0仕様の投票においても変わっていない。

[Category:Java](https://ja.wikipedia.org/wiki/Category:Java "wikilink")