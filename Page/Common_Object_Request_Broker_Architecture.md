> この記事は[Common Object Request Broker Architecture](https://ja.wikipedia.org/wiki/Common_Object_Request_Broker_Architecture)から翻訳されています。


**Common Object Request Broker Architecture**（コモン オブジェクト リクエスト ブローカー アーキテクチャー、略称**CORBA**）とは、[Object Management Group](../Page/Object_Management_Group.md "wikilink")(OMG)が定義した[標準規格](https://ja.wikipedia.org/wiki/標準規格 "wikilink")であり、様々なコンピュータ上で様々な[プログラミング言語](../Page/プログラミング言語.md "wikilink")で書かれた[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")の相互利用を可能にする（[分散オブジェクト](https://ja.wikipedia.org/wiki/分散オブジェクト "wikilink")技術）ものである。

## 概要

CORBA では、プログラムコードをその機能や呼び出し方の情報と共に一種の[カプセル化](../Page/カプセル化.md "wikilink")を行う。このカプセル化されたオブジェクトは、[コンピュータネットワーク](../Page/コンピュータネットワーク.md "wikilink")を経由して他の[プログラム](../Page/プログラム_\(コンピュータ\).md "wikilink")（あるいは CORBA オブジェクト）から呼び出すことができる。

CORBA は[インタフェース記述言語](../Page/インタフェース記述言語.md "wikilink") (IDL) を使ってこのようなオブジェクトの外部インタフェースを記述する。そして、IDLから他の特定の実装言語（[C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")）への「マッピング」を行う。CORBAとしてマッピングが標準的に用意されているのは、[Ada](../Page/Ada.md "wikilink")、[C](../Page/C言語.md "wikilink")、C++、[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")、[Smalltalk](../Page/Smalltalk.md "wikilink")、Java、[COBOL](../Page/COBOL.md "wikilink")、[PL/I](https://ja.wikipedia.org/wiki/PL/I "wikilink")、[Python](../Page/Python.md "wikilink") である。標準に組み込まれていないが、[Perl](../Page/Perl.md "wikilink")、[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[Ruby](../Page/Ruby.md "wikilink")、[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、[Tcl](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink") へのマッピングを実装した[Object Request Brokerが存在する](https://ja.wikipedia.org/wiki/Object_Request_Broker "wikilink")。

下図はCORBA基盤で生成されたコードが使われる様子を示したものである。

[400px](https://ja.wikipedia.org/wiki/ファイル:_Corba_Server_ja.png "wikilink")

この図は非常に単純化してある。通常、サーバ側には Portable Object Adapter があり、呼び出しをローカルな[サーバントに渡すか](https://ja.wikipedia.org/wiki/サーバント_\(CORBA\) "wikilink")（[負荷分散](https://ja.wikipedia.org/wiki/負荷分散 "wikilink")のために）他のサーバに転送する。また、サーバ側にもクライアント側にも後述するインターセプターが存在することが多い。

ユーザーに対して言語やプラットフォームに依存しない[遠隔手続き呼出し](../Page/遠隔手続き呼出し.md "wikilink") (RPC) 仕様を提供する以外に、CORBAは[トランザクション](../Page/トランザクション.md "wikilink")や[セキュリティに必要な一般的サービスを定義している](../Page/コンピュータセキュリティ.md "wikilink")。

## 主な機能・特徴

### Objects by Value (OBV)

リモートオブジェクトとは別に、CORBAと[RMI-IIOP](../Page/RMI-IIOP.md "wikilink")はOBVの概念を定義している。オブジェクト内のメソッドのコードはデフォルトではローカルに実行される。OBVをリモートから受信する場合、必要なコードが両者に事前に備えられているか、送信側から動的にダウンロードしなければならない。このため、コードをダウンロードできるURL群の（空白で区切った）リストである Code Base が OBV を定義するレコードに含まれている。OBV はリモートメソッドを持つこともできる。

OBV は転送される際に付属して転送されるフィールドを持つことがある。そのフィールドにはOBV自体、構成リスト、[木構造やグラフなどが含まれる](../Page/木構造_\(データ構造\).md "wikilink")。OBVにはクラス階層があり、多重継承や[抽象クラス](https://ja.wikipedia.org/wiki/抽象クラス "wikilink")もある。

### CORBA Component Model (CCM)

CORBA Component Model (CCM) は CORBA 仕様の追加要素である。 CORBA 3 で導入された。これはCORBAコンポーネントの標準アプリケーションフレームワークを記述したものである。それはちょうど「言語に依存しない」[Enterprise JavaBeans](../Page/Enterprise_JavaBeans.md "wikilink")(EJB)の拡張版である。「ポート」と呼ばれる明確な名前付きのインタフェースを通してサービスのやりとりができる実体を抽象化したものである。

CCM にはコンポーネントコンテナがあり、その中にソフトウェアコンポーネントが置かれる。コンテナは内包するコンポーネントに各種サービスを提供する。例えば、通知、認証、永続性、トランザクション管理などがある。これらは分散システムには必須のサービスであり、その実装をソフトウェアコンポーネントからコンテナに移すことによってコンポーネントの複雑さは劇的に軽減される。

### ポータブルなインターセプター

ポータブルなインターセプターとは、CORBAや[RMI-IIOP](../Page/RMI-IIOP.md "wikilink")が使用するCORBAシステムの最重要機能の「フック」である。CORBA標準では以下のようなタイプのインターセプターを定義している:

1.  [IORインターセプターは](https://ja.wikipedia.org/wiki/Interoperable_Object_Reference "wikilink")、カレントサーバが示すリモートオブジェクトへの新たな参照の作成を調停する。
2.  クライアントインターセプターは、クライアント側でリモートメソッドの呼び出しの調停を行う。そのオブジェクトの[サーバントが同じサーバに存在すれば](https://ja.wikipedia.org/wiki/サーバント_\(CORBA\) "wikilink")、そのメソッドが呼び出されるようにローカル呼び出しが調停される。
3.  サーバインターセプターは、サーバ側のリモートメソッド呼び出しへの対応を調停する。

インターセプターは、送信されるメッセージに何らかの情報や生成したIORを付加することができる。それらの情報はリモート側の対応するインターセプターが読み取る。インターセプターは例外を送ったり、メッセージを他のターゲットに転送したりといったことも行う。

### General InterORB Protocol (GIOP)

[GIOP](../Page/GIOP.md "wikilink")とは、[Object Request Broker](https://ja.wikipedia.org/wiki/Object_Request_Broker "wikilink")(ORB)同士が通信する際の抽象プロトコルである。このプロトコルに関する標準は[Object Management Group](../Page/Object_Management_Group.md "wikilink")(OMG)が管理保守している。GIOPアーキテクチャはいくつかの実際のプロトコルを提供している:

1.  Internet InterORB Protocol ([IIOP](https://ja.wikipedia.org/wiki/IIOP "wikilink")) - CORBA ORB 同士の[通信プロトコル](../Page/通信プロトコル.md "wikilink")であり、[インターネット](../Page/インターネット.md "wikilink")上のGIOPの実装である。従って、GIOPメッセージと[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")との橋渡しをする。
2.  SSL InterORB Protocol (SSLIOP) - [SSL](../Page/Transport_Layer_Security.md "wikilink") 上のIIOP。[暗号](../Page/暗号.md "wikilink")化と[認証](../Page/認証.md "wikilink")機能を提供する。
3.  HyperText InterORB Protocol (HTIOP) - [HTTP上のIIOP](../Page/Hypertext_Transfer_Protocol.md "wikilink")。[プロキシ](../Page/プロキシ.md "wikilink")を透過的に迂回するなどの機能がある。
4.  その他いろいろ…

### Data Distribution Service (DDS)

[Object Management Group](../Page/Object_Management_Group.md "wikilink") (OMG) は関連する標準規格として[Data Distribution Service](../Page/Data_Distribution_Service.md "wikilink") (DDS) 標準を制定している。DDS は出版-購読（publish-subscribe）型データ配信モデルであり、対照的にCORBAはリモート呼び出しオブジェクトモデルである。

### VMCID (Vendor Minor Codeset ID)

標準CORBAは例外のサブカテゴリーを明示するためにマイナーコードを明記している。マイナー例外コードは unsigned long 型で、上位20ビットは “Vendor Minor Codeset ID”(VMCID)、下位12ビットがマイナーコード本体である。標準例外のマイナーコードには OMG が予約する VMCID の付与された形で unsigned long 型の定数 CORBA::OMGVMCID として定義される。従って、マイナー例外コードは OMGVMCID と OR された形で ex_body 構造体に格納されている。

マイナーコードの設定はベンダー依存である。VMCID の割り当て要求は、tagrequest@omg.org に電子メールを送ればよい。VMCID のうち、0 と 0xfffff は実験用の予約されている。また、OMGVMCID と 1 から 0xf までの VMCID は OMG が予約している。

## CorbaLoc

CorbaLoc とは、Corba Location の略であり、CORBA オブジェクトへの参照を文字列で表したものである。その見た目はURLによく似ている。CORBA製品には OMGが定義した二種類のURL、"corbaloc:" と "corbaname:" をサポートしている。その目的は、[IORを持つ場所を指定するに当たって](https://ja.wikipedia.org/wiki/Interoperable_Object_Reference "wikilink")、人間がそれを読んで編集できる方法を提供することである。

CobaLoc の例を以下に示す:

  -
    corbaloc::160.45.110.41:38693/StandardNS/NameServer-POA/_root

CORBA製品はオプションとして "http:"、"ftp:"、"file:" をサポートするものもある。これらは、文字列化されたIORのダウンロード方法の詳細を提供するために存在する（または、再帰的に他のURLをダウンロードすることによって文字列化されたIORが得られるようにしている）。

## CORBA 実装例

  - [Oracle Tuxedo](https://ja.wikipedia.org/wiki/Oracle_Tuxedo "wikilink") - CORBA 2.5 対応の商用 ORB （[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C++](../Page/C++.md "wikilink")用）[オラクル](https://ja.wikipedia.org/wiki/オラクル_\(企業\) "wikilink")
  - Borland Enterprise Server, VisiBroker - CORBA 2.6 対応の商用 ORB （Java、C++用） [ボーランド](../Page/ボーランド.md "wikilink")
  - [GNU Classpath](../Page/GNU_Classpath.md "wikilink") - Java用の[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")実装を含む([GPL](../Page/GNU_General_Public_License.md "wikilink")+linking exception, 新たに書かれた org.omg パッケージを含む)
  - CORBA for PHP - PHP5
  - Combat - [Tcl用](https://ja.wikipedia.org/wiki/Tcl/Tk "wikilink") ORB。C++ ORB の Tcl 層。
  - e\*ORB - 商用 ORB （[Ada](../Page/Ada.md "wikilink")、[C](../Page/C言語.md "wikilink")、C++用）
  - [ILU](https://ja.wikipedia.org/wiki/Inter-Language_Unification "wikilink") - [パロアルト研究所](../Page/パロアルト研究所.md "wikilink")のオープン・ソフトウェア・オブジェクト・インタフェース・システム
  - IIOP.NET - [Microsoft .NET](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 用フリーソフトウェア([LGPL](https://ja.wikipedia.org/wiki/GNU_Library_General_Public_License "wikilink")) ORB
  - [Interstage](../Page/Interstage.md "wikilink") - 商用、[富士通](../Page/富士通.md "wikilink")
  - JacORB - Javaで実装されたフリーソフトウェア ([LGPL](https://ja.wikipedia.org/wiki/GNU_Library_General_Public_License "wikilink")) ORB
  - J-Integra Espresso - 商用 Microsoft .NET ORB、by Intrinsyc J-Integra
  - MICO - C++で実装されたフリーソフトウェア ([LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")) ORB
  - omniORB - フリーソフトウェア ([LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")) ORB （C++、[Python](../Page/Python.md "wikilink")用）
  - OpenORB - フリーソフトウェア ([BSD](https://ja.wikipedia.org/wiki/BSD_License "wikilink")) ORB （[Java](https://ja.wikipedia.org/wiki/Java "wikilink")用）
  - Orbacus - 商用 C++ ORB、by IONA Technologies
  - ORBexpress - 商用 ORB（Ada、Java、C++用。通常版とリアルタイム版）by Objective Interface Systems
  - ORBit2 - フリーソフトウェア ([LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")) ORB （C、C++、Python用）
  - Orbix - 商用 ORB by IONA Technologies
  - ORBLink - 商用 ORB （Allegro Common LISP 用）
  - Perl ORB - [Perl](../Page/Perl.md "wikilink")で実装されたオープンソース([Artistic License](../Page/Artistic_License.md "wikilink")) ORB
  - PolyORB - Adaで実装されたフリーソフトウェア ([MGPL](../Page/GNAT_Modified_General_Public_License.md "wikilink")) ORB
  - SANKHYA Varadhi - 商用 ORB （C++用）
  - TAO - オープンソース ORB （C++用）
  - TPBroker - VisiBroker の[日立製作所](../Page/日立製作所.md "wikilink")による改造版
  - Universe - PHP4
  - VBOrb - フリーソフトウェア ([LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")) ORB （[Visual Basic用](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")）
  - Xtradyne I-DBC - 商用 CORBA セキュリティ実装、by Xtradyne
  - Systemν\[nju:\] - 商用 分散トランザクション対応 ORB、[日本ユニシス](https://ja.wikipedia.org/wiki/日本ユニシス "wikilink")

## OMG の商標

CORBA、[IIOP](https://ja.wikipedia.org/wiki/IIOP "wikilink")、[OMG](https://ja.wikipedia.org/wiki/OMG "wikilink") は Object Management Group の[登録商標](https://ja.wikipedia.org/wiki/登録商標 "wikilink")であり、利用には注意が必要である。GIOP は登録商標ではない。従って、アプリケーションについて「[GIOP](../Page/GIOP.md "wikilink")に基づいたアーキテクチャである」とするのが適切な場合もあるだろう。なお、CORBAの仕様書自体に関しては、それに基づいた実装を自由に行うことは（CORBAという登録商標を使わないかぎり）許されている。

## 関連項目

  - [遠隔手続き呼出し](../Page/遠隔手続き呼出し.md "wikilink") (RPC)
  - [ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")
  - [サービス指向アーキテクチャ](../Page/サービス指向アーキテクチャ.md "wikilink")
  - [Java Remote Method Invocation](../Page/Java_Remote_Method_Invocation.md "wikilink")
  - [Webサービス](../Page/Webサービス.md "wikilink")
  - [分散コンピューティング](../Page/分散コンピューティング.md "wikilink")
  - [Java Platform, Enterprise Edition](../Page/Java_Platform,_Enterprise_Edition.md "wikilink")
  - [XML-RPC](../Page/XML-RPC.md "wikilink")
  - [DCOM](https://ja.wikipedia.org/wiki/DCOM "wikilink")
  - [SOAP (プロトコル)](../Page/SOAP_\(プロトコル\).md "wikilink")
  - [Bonobo](../Page/Bonobo.md "wikilink")

## 参考文献

  - [利用可能な CORBA 実装の比較](http://www.puder.org/corba/matrix/)
  - [The official CORBA standard from the OMG group (direct download, .pdf, about 10 Mb)](http://www.omg.org/docs/formal/04-03-12.pdf).
  - Robert Orfali: *The Essential Client/Server Survival Guide*, John Wiley & Sons, ISBN 0-471-15325-7
  - Robert Orfali, Dan Harkey, Jeri Edwards: *The Essential Distributed Objects Survival Guide*, John Wiley & Sons, ISBN 0-471-12993-3
  - Robert Orfali, Dan Harkey: *Client/Server Programming with JAVA and CORBA*, John Wiley & Sons, ISBN 0-471-24578-X
  - Dirk Slama, Jason Garbis, Perry Russell: *Enterprise CORBA*, Prentice Hall, ISBN 0-13-083963-9
  - Michi Henning, Steve Vinoski: *Advanced CORBA Programming with C++*, Addison-Wesley, ISBN 0-201-37927-9
  - Axel Korthaus, Martin Schader, Markus Aleksy: \[<http://www.wifo.uni-mannheim.de/CORBA/>*Implementing Distributed Systems with Java and CORBA*\], Springer, ISBN 3-540-24173-6
  - Fintan Bolton: *Pure Corba*, Sams Publishing, ISBN 0-672-31812-1
  - Jon Siegel: *CORBA 3 - Fundamentals and Programming*, John Wiley & Sons, ISBN 0-471-29518-3
  - Ron Zahavi: *Enterprise Application Integration with CORBA: Component and Web-Based Solutions*, John Wiley & Sons, ISBN 0-471-32720-4
  - Bret Hartman, Konstantin Beznosov, Steve Vinoski, Donald Flinn: *Enterprise Security with EJB and CORBA*, John Wiley & Sons, ISBN 0-471-40131-5
  - Thomas J. Mowbray, Ron Zahavi: *The Essential Corba: System Integration Using Distributed Objects*, John Wiley & Sons, ISBN 0-471-10611-9
  - Michael Rosen, David Curtis: *Integrating CORBA and COM Applications*, John Wiley & Sons, ISBN 0-471-19827-7
  - Gerald Brose, Andreas Vogel, Keith Duddy: *Java Programming with CORBA*, John Wiley & Sons, ISBN 0-471-37681-7
  - John Schettino, Robin S. Hohman, Liz O'Hara: *CORBA For Dummies*, Hungry Minds, ISBN 0-7645-0308-1
  - Jeremy L. Rosenberger: *Teach Yourself CORBA in 14 Days*, Sams Publishing, ISBN 0-672-31208-5
  - Jon Siegel: *Quick CORBA 3*, John Wiley & Sons, ISBN 0-471-38935-8
  - Thomas J. Mowbray, Raphael C. Malveau: *CORBA Design Patterns*, John Wiley & Sons, ISBN 0-471-15882-8
  - Robert Orfali, Dan Harkey, Jeri Edwards: *Instant CORBA*, John Wiley & Sons, ISBN 0-471-18333-4
  - Paul Harmon, William Morrissey: *The Object Technology Casebook*, John Wiley & Sons, ISBN 0-471-14717-6

## 外部リンク

  - [Information Board](http://www.corba.org/)
  - [Object Management Group](http://www.omg.org/)
  - [Description](http://cbbrowne.com/info/corba.html) by Christopher B. Browne
  - [CORBA support for autoconf](http://corbaconf.kiev.ua/)
  - [OrbZone forum](http://orbzone.org/)
  - [SOAP Bridge](http://sourceforge.net/projects/soap2corba/)
  - [いまなぜCORBAなの？](http://www.atmarkit.co.jp/fjava/rensai/corba01/corba01.html) アットマーク・アイティ
  - [CORBA](http://www.techscore.com/tech/CORBA/index.html) テックスコア
  - [CORBA Component Model 入門](http://www.ogis-ri.co.jp/otc/hiroba/technical/CCM/step1/index.html) 永田博靖（オージス総研）

[Category:オブジェクト指向](https://ja.wikipedia.org/wiki/Category:オブジェクト指向 "wikilink") [Category:ソフトウェアアーキテクチャ](https://ja.wikipedia.org/wiki/Category:ソフトウェアアーキテクチャ "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")