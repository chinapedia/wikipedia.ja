> この記事は[Component Object Model](https://ja.wikipedia.org/wiki/Component_Object_Model)から翻訳されています。


**Component Object Model**（COM、コンポーネント オブジェクト モデル）とは、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提唱する[ソフトウェアの再利用](https://ja.wikipedia.org/wiki/ソフトウェアの再利用 "wikilink")を目的とした技術のことである。COMは相互作用するバイナリ[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")を作成するための、プラットフォーム非依存・分散型・[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")のシステムであると説明されている\[1\]\[2\]。具体的には[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")間の通信や、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")とアプリケーションソフトウェアとのインターフェイス（[API](../Page/アプリケーションプログラミングインタフェース.md "wikilink")）に用いられる。

COMを使用して開発されたソフトウェア部品を**COMコンポーネント**と呼ぶ。COMコンポーネントの開発は、特定の[プログラミング言語](../Page/プログラミング言語.md "wikilink")に依存せず、[C言語](../Page/C言語.md "wikilink")や[C++](../Page/C++.md "wikilink")、[Visual Basic](../Page/Visual_Basic.md "wikilink")、[Smalltalk](../Page/Smalltalk.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")など、様々な言語により開発することができる。COMという用語は、[OLE](../Page/Object_Linking_and_Embedding.md "wikilink")、OLEオートメーション、[ActiveX](../Page/ActiveX.md "wikilink")、COM+、[DCOMの総称としてよく使われる](../Page/Distributed_Component_Object_Model.md "wikilink")。COMコンポーネントは、他ソフトウェアと通信するための[インターフェイスを有している](../Page/インタフェース_\(情報技術\).md "wikilink")。[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")（**COMクライアント**）は、通信インターフェイスを表現する抽象型として公開されているCOM[インターフェイスを介してCOMコンポーネント](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")（**COMサーバー**）と通信をし、それらを組み合わせることでサービスを提供する。言語によるメモリやその他[計算資源](../Page/計算資源.md "wikilink")の割り付けの違いは、[参照カウント](../Page/参照カウント.md "wikilink")を利用してオブジェクトの生成と破棄をそのオブジェクト自身の責任とすることにより解決する。オブジェクトがサポートする、異なるインターフェイス間の[型変換](../Page/型変換.md "wikilink")は、言語固有のキャスト構文ではなく、言語非依存の`QueryInterface`[メソッドで行う](../Page/メソッド_\(計算機科学\).md "wikilink")。メソッド呼び出しをデリゲート（委譲）する形でサブオブジェクトの集合（アグリゲーションと呼ぶ）を生成する方法がCOM内における最適な継承方法である。

COMは[プロトコル](../Page/プロトコル.md "wikilink")などの仕様が公開されており\[3\]、[XPCOM](../Page/XPCOM.md "wikilink")のような[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")実装も存在するが、COMが主に利用されているのは[Microsoft Windows環境である](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。[MonoにおけるCOM相互運用もMS](../Page/Mono_\(ソフトウェア\).md "wikilink") COMおよびXPCOMを基盤としているが、機能およびサポート環境はまだ限定されている\[4\]\[5\]。

COMの前身はOLEである。COMは[.NET Frameworkに置き換えられているものも多い](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。たとえば.NETはDCOMの代替として、[Windows Communication Foundation](../Page/Windows_Communication_Foundation.md "wikilink") (WCF) を通じて[Webサービス](../Page/Webサービス.md "wikilink")をサポートする。WCFが[XMLベースの](../Page/Extensible_Markup_Language.md "wikilink")[SOAPメッセージを利用するのに対し](../Page/SOAP_\(プロトコル\).md "wikilink")、ネットワークで接続されたDCOMはバイナリの独自仕様フォーマットを利用する。しかし、[Microsoft DirectXなどに代表されるように](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、ネイティブC++での利用を前提としたパフォーマンス重視 のAPIは、依然として.NETではなくCOMが使われる傾向にある。

COMはまた[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")システムとして[CORBAや](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")[Java Beansと競合関係にある](https://ja.wikipedia.org/wiki/Java_Beans "wikilink")。

## COMの歴史

  - [1991年](../Page/1991年.md "wikilink")、COMの前身であるOLEが、OLE 1として[Windows 3.1とともに公開された](../Page/Microsoft_Windows_3.x.md "wikilink")。
  - [1992年](../Page/1992年.md "wikilink")、OLE 2が公開された。IUnknownインタフェースなど、のちにCOMと改称される要素の多くがOLE 2で登場した。
  - [1994年](../Page/1994年.md "wikilink")、OCXもしくはOLEコントロールがVBXコントロールの後継として紹介される。それと同時に、OLEは、もはや単なる頭文字ではなく、コンポーネント技術を表す用語となった。
  - [1996年](../Page/1996年.md "wikilink")初頭、マイクロソフトは、OLEのうちでインターネットと関連のあるいくつかの技術を[ActiveX](../Page/ActiveX.md "wikilink")として名称変更した。やがて、OLEとして公開されていた技術が[ActiveX](../Page/ActiveX.md "wikilink")に統合され始める。
  - [1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、マイクロソフトは再びコンポーネントを使用するこれらの技術の改称を行い、Component Object Modelとした。

## 関連技術

COMはWindowsで主要なソフトウェア開発プラットフォームであり、数多くの技術の開発に影響を与えた。

### COM+

エンタープライズレベルの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の代替としてWindowsのポジションを確立するためだけでなく、分散トランザクションをサポートし、メモリとプロセッサ（スレッド）の管理の改善するため、マイクロソフトはWindows NT 4.0 Service Pack 4で[Microsoft Transaction Server](../Page/Microsoft_Transaction_Server.md "wikilink") (MTS) を導入した。

[Windows 2000でのCOMの重要な拡張は](../Page/Microsoft_Windows_2000.md "wikilink")（MTSによる外部ツールの組み合わせとは対照的に）OSへ統合することであり、これを**COM+**と改名した。この時点でマイクロソフトは個別の要素としてDCOMを重視していなかった。COM+の追加レイヤでトランザクショナルCOMコンポーネントを直接的に取り扱った。COM+コンポーネントはコンポーネントサービスアプリケーションインタフェースを通じて追加された。

COM+は「コンポーネントファーム (component farms)」で動作できる利点があった。コードが正しい場合、コンポーネントはメモリからアンロードすることなく初期化ルーチンを新たに呼び出すことにより再利用できた。以前はDCOMだけで可能だったコンポーネントの分散化（他のマシンからの呼び出し）も可能となった。

またCOM+では、**COM+イベント**という、サブスクライバ/パブリッシャー型のイベントメカニズムを導入し、アプリケーション間非同期メッセージングプロトコルであるMSMQを利用するための新たな方法として、**Queued Components**というコンポーネントを介するモデルを提供した。これにより、COM+プログラミングモデルでは、遅延バインディングされたイベント、および、パブリッシャー/サブスクライバとイベントシステムの間のメソッド呼び出しがサポートされる。

### DCOM

### .NET

COMプラットフォームは.NET Frameworkに大幅に取って代わられ、マイクロソフトは.NETに注力する戦略に集中している。COMは複雑で高性能な[Visual Basicや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[ASPで実装されたフロントエンドのコードと接続するためによく利用されていた](../Page/Active_Server_Pages.md "wikilink")。

好感されている.NETに対して、COMはある程度批判されている。.NETが[Windows Formsと](../Page/Windows_Forms.md "wikilink")[Web Formの両方に対して](../Page/フォーム_\(ウェブ\).md "wikilink")[ジャストインタイムコンパイル方式](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")と共にVisual Basicに似たラピッドデベロップメントツールを提供するため、バックエンドコードは[C\#](../Page/C_Sharp.md "wikilink")、[Visual Basic .NET](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")、[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")を含むあらゆる.NET言語で実装できる。

それでもCOMはまだ様々なテクノロジーで重要なソフトウェアの基盤として生き延びている。例えばマルチメディアAPIとして広く普及している[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")の[APIはCOMをベースにしている](../Page/アプリケーションプログラミングインタフェース.md "wikilink")\[6\]。2015年に[Windows 10とともにリリースされたDirectX](https://ja.wikipedia.org/wiki/Windows_10 "wikilink") 12 ([Direct3D](../Page/Direct3D.md "wikilink") 12) も、依然としてCOMベースであり、C++を第1級言語としている。2018年時点では、マイクロソフトはCOMのサポートやCOMそのものをやめてしまう計画を持っていない。

COMはまた、コンパイル時点でAPIの情報を必要としないスクリプトからCOMオブジェクトを呼び出すためのインタフェース（動的[ダックタイピング](https://ja.wikipedia.org/wiki/ダックタイピング "wikilink")）を提供するため、[Microsoft Officeや](../Page/Microsoft_Office.md "wikilink")[Internet Explorerのようなネイティブアプリケーションのスクリプト制御のための技術として理想的でもある](../Page/Internet_Explorer.md "wikilink")。COMにおけるあらゆる要素を一意に識別するために開発された[GUID](../Page/GUID.md "wikilink")システムはマイクロソフトによる[UUID](../Page/UUID.md "wikilink")の実装であり、COM以外でもユニークな IDが必要とされる場合に広く利用されている\[7\]。

トランザクションやコンポーネントのキューといったようなCOM+が提供する複数のサービスはエンタープライズな.NETアプリケーションでもまだ重要である。

制約はあるものの、.NETはCOMに対して相互運用性のサポートがある。.NETはランタイム呼び出し可能ラッパー (RCW) を実装することでCOMオブジェクトを利用できる。COMクライアントはCOM呼び出し可能ラッパー (CCW) によって、特定の制約に従った.NETオブジェクトを利用できる。COMと.NETの両方の側からは相手側のオブジェクトがネイティブなオブジェクトに見える。

[.NET Remotingでは](../Page/.NET_Remoting.md "wikilink")、オブジェクトがプロセスやマシンの境界を越えてリファレンスや値を透過的にマーシャリングできるようにして、COMが持つ数多くのリモート実行の欠点を解決する。

### Windowsランタイム

[Windows 8および](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")[Windows RTにて](https://ja.wikipedia.org/wiki/Windows_RT "wikilink")、新たなアプリケーションの開発・実行基盤として**Windowsランタイム** (WinRT) が導入された。WinRTはCOMを拡張したネイティブ技術であるが、Windowsメタデータ (WinMD) および言語プロジェクション (language projection) と呼ばれる技術により、.NET言語や[JavaScript](../Page/JavaScript.md "wikilink")などからも透過的に利用可能である\[8\]。

## 技術的詳細

COMコンポーネントにはクラスID (CLSID) が割り当てられ、COMコンポーネント同士はクラスIDによって区別される。CLSIDはGUIDで構成されている。各COMコンポーネントは1つ以上の[インターフェイスを公開することで機能を提供している](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。インターフェイス同士はインターフェイスID (IID) で区別される。IIDもGUIDで構成されている。

COMインターフェイスはプログラミング言語とCOMとを結び付けている。COMコンポーネントへのアクセスは全てインターフェイスを通さなければならない。これによって、プロセスやコンピュータを跨いでCOMコンポーネントにアクセスすることができるようになっている（コンピュータを跨いでのアクセスにはDCOMが必要）。

### インターフェイス

全てのCOMコンポーネントは**[`IUnknown`](https://ja.wikipedia.org/wiki/IUnknown "wikilink")**と呼ばれる[インターフェイスを継承する必要がある](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")。また、全てのCOMインターフェイスは`IUnknown`から派生している。`IUnknown`は、`AddRef` / `Release` / `QueryInterface`という3つの[メソッド](https://ja.wikipedia.org/wiki/メソッド "wikilink")を持っている。`AddRef`と`Release`はインターフェイスの生存期間を管理するための[参照カウント](../Page/参照カウント.md "wikilink")を実装するメソッドである。そして`QueryInterface`は、IIDを指定してコンポーネントが実装している他のインターフェイスを取得するメソッドである。これは[C++](../Page/C++.md "wikilink")の`dynamic_cast`や、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")および[C\#の](../Page/C_Sharp.md "wikilink")[型変換](../Page/型変換.md "wikilink")演算子に相当する。

COMコンポーネントのインタフェースは、反射性、対称性、推移性を備えている必要がある。反射性とは、あるインタフェースから、`QueryInterface`をそのインタフェース自身を表すIIDを与えて呼び出すと、返ってくるインタフェースは元と同じものでなければならないということである。対称性とは、インタフェースAから`QueryInterface`でインタフェースBが取得できる場合、インタフェースBからインタフェースAが取得できなければならないということである。推移性とは、対称性と似ているが、インタフェースBがインタフェースAから取得でき、インタフェースCがインタフェースBから取得できる場合、インタフェースCはインタフェースAから取得できなければならないということである。

インタフェースには、インタフェースを実装した関数へのポインタをその宣言時の順に並べた[仮想関数テーブル](../Page/仮想関数テーブル.md "wikilink")へのポインタが含まれている。この関数テーブル構造は、OLE 1.0のときからOLEシステムとの通信に使われていた。

COMはコンポーネント間の通信のためにほかにも多くの標準インタフェースを定めている。たとえばデータストリームを管理する`IStream`が挙げられる。これはファイルストリームのコンポーネントがファイルを読み書きする際に使うことが考えられる。`IStream`の`Read`メソッドと`Write`メソッドはストリームに対して読み取りと書き込みを行うことが想定される。他の例として、`IOleObject`は、あるアプリケーションに別のアプリケーションを埋め込むような複合文書に利用される。このため、呼び出した側が呼び出し先コンポーネントとの画面表示上の境界を決められるメソッドをインターフェースに持っている。また「開く」、「保存」などの操作を行うことができるメソッドをインターフェスに持っている。

### コクラス

COMではクラスのことを**コクラス** (**coclass**) と呼ぶ。コクラスは、COMにおける（[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")のような）クラスを定義する言語非依存の手段である。

1つのコクラスは、1つ以上のインタフェースの具体的な実装を提供する。COMに対応している[プログラミング言語](../Page/プログラミング言語.md "wikilink")であれば、[C++](../Page/C++.md "wikilink")、[Visual Basicなどどんな言語でも実装を行うことができる](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")。

個々のコクラスは、クラスID (CLSID) やProgIDで識別される。

  - クラスIDはGUIDを使った表現である。通常、各コクラスに対しクラスIDを1つ割り当てる。ただし、互換性のため、旧バージョンのクラスIDに新バージョンのコクラス実装を登録し、結果的に複数クラスIDが同一コクラスを指し示す場合もある。そのような用途に\[<https://msdn.microsoft.com/en-us/library/windows/desktop/ms693452(v=vs.85>).aspx CoTreatAsClass\]関数が用意されている。
  - ProgIDは文字列による表現である。`InternetExplorer.Application`や`Msxml2.DOMDocument.6.0`など「プログラム名.コンポーネント.バージョン」（バージョンは非必須）という規則である\[9\]。ProgIDは必須ではなく、コクラスによってはProgIDを持っていない場合もある。

ProgIDによる指定でオブジェクトを作成・取得する際には、ProgIDからクラスIDに変換する必要がある。この変換は一意ではなく、特にバージョン指定のないProgIDでは、インストールされているコンポーネントのバージョン次第で、コンピューターごとに異なるCLSIDとなる可能性がある。

この処理はプログラミング言語やライブラリによって実装される場合もある。[VBScript](../Page/VBScript.md "wikilink")など、オブジェクト作成時にProgIDでの指定のみ可能なプログラミング言語もある。

COMは、Windows開発の世界に、実装とインターフェイスを切り離すという概念を意識させることをもたらした。この基本的な概念の延長には、オブジェクト指向における[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")（多態）の実現がある。すなわち、1つのインターフェイスに対して実装された複数のCOMコンポーネントを用意し、[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")(呼び出し側コンポーネント)が実行時に任意のCOMコンポーネントを選べるようになる一方で、呼び出される側のコンポーネントの実装の違いを区別なく、アプリケーション側では一様に操作をコーディングすることができる。例えば、DAOでは呼び出し先コンポーネントがSQL Server用実装であるか、Oracle用実装であるかを意識することなく、VBアプリケーションを記述できる。また、COMコンポーネントが要求するインターフェイスを実装するオブジェクトをアプリケーション側で用意して、COMコンポーネントにインターフェイスを通じて操作させることで、コールバック処理などのカスタマイズを実現することもできる柔軟性もある。これはイベントシンク (event sink) として標準化され、プロセス内だけでなくDCOMプロセス間の透過的なコールバック処理をも実現することにつながった。

### インタフェース定義言語とタイプライブラリ

COMコンポーネントに関する情報の記述手段として、MIDL（マイクロソフトインタフェース定義言語、[IDLも参照](../Page/インタフェース記述言語.md "wikilink")）やタイプライブラリがある。MIDLはテキストファイルで主として開発時に用いられる。タイプライブラリは型に関する言語非依存の情報を提供するバイナリファイルであり、開発時だけでなく実行時に参照されることも想定されている。

COMコンポーネントの開発では、普通IDLで型を定義することから始める。IDLファイルではオブジェクト指向的なクラスやインタフェース、構造体、列挙体などのユーザ定義型をプログラミング言語に依存せず記述できる。このIDLではC/C++に似たキーワードと、それに追加してインタフェースを定義する「interface」、コクラスを定義する「coclass」、それらの集合を現す「library」という2つのキーワードを使用する。また各宣言の前に角括弧\[\]で括って属性を指定でき、インタフェースにGUID (IID) を指定したり配列引数とその長さを示す引数との関係を指示したりできる。

IDLファイルはMIDLコンパイラで様々なプログラミング言語に向けてコンパイルされる。C/C++用にはインタフェースなどが宣言された[ヘッダファイル](../Page/ヘッダファイル.md "wikilink")とGUIDを定義したCのソースファイル、またCOMのメソッド呼び出しを[RPC用に変換する](../Page/遠隔手続き呼出し.md "wikilink")「プロキシ」とそれを元に戻す「スタブ」のソースファイルも生成される。

MIDLはIDLファイルからタイプライブラリ（.TLBファイル）も作る。タイプライブラリに含まれているバイナリのメタデータはコンパイラや実行環境（Visual Basicや[Delphi](../Page/Delphi.md "wikilink")、.NETの[CLRなど](../Page/共通言語ランタイム.md "wikilink")）で利用される。その結果タイプライブラリファイルで定義されたコクラスをその言語や環境に持ち込んで使用できるようになる。

### オブジェクトフレームワークとしてのCOM

COMの基本原則はそれがオブジェクト指向の哲学に基づいているということである。オブジェクト指向開発と実装を実現するためのプラットフォームである。

COMはランタイムフレームワークであるため、型は明示的に識別可能であり実行時に指定可能である必要がある。これを実現するために**GUID**が使われる。それぞれのCOMの型は実行時あるいはコンパイル時に自分の識別用GUIDを指定する。

COMの型についての情報がコンパイル時と実行時の両方でアクセスできるようにする必要性から、COMはタイプライブラリを提供する。COMがオブジェクトの相互作用のための動的なフレームワークとしてその能力を発揮するのはタイプライブラリが効果的に利用されているからである。

以下の例にあるIDLのコクラス定義を考える。

``` idl
interface ISomeInterface : IUnknown
{
    HRESULT DoSomething();
};

coclass SomeClass
{
    [default] interface ISomeInterface;
};
```

上記のコード断片は、`ISomeInterface`というインターフェイスを実装する、`SomeClass`という名前のCOMクラスを宣言している。

これは概念的には次のようなC++のクラスを定義することに等しい。

``` cpp
struct ISomeInterface : public IUnknown
{
    virtual HRESULT DoSomething() = 0;
};

class SomeClass : public ISomeInterface
{
    ...
};
```

`ISomeInterface`はC++の純粋仮想基底クラスに相当するものである。

COMのインターフェイスおよびコクラスを含むIDLファイルはタイプライブラリファイルにコンパイルされる。タイプライブラリはCOMクライアントのコンパイル時あるいは実行時に解釈され、オブジェクトがどのインターフェイスをサポートするかを決定し、オブジェクトのインターフェイスメソッドを呼び出すために利用される。

C++では、Windows API関数のひとつである`CoCreateInstance()`を使用してCOMオブジェクトをインスタンス化することができる。引数にはクラスID (CLSID) およびインターフェイスID (IID) を指定する。

``` cpp
ISomeInterface* pSomeInterface = NULL;
HRESULT hr = CoCreateInstance(
    CLSID_SomeClass,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_ISomeInterface,
    reinterpret_cast<void**>(&pSomeInterface)
);
```

この例では、`ISomeInterface`インターフェイスを実装する`SomeClass`オブジェクトへのポインタを取得するためにCOMサブシステムが使われる。これは概念的に次のようなC++のコードと等しい。

``` cpp
ISomeInterface* pSomeInterface = new SomeClass();
```

そしてコクラスはCOMの世界ではオブジェクト指向のクラスである。コクラスの主要機能は、(1) バイナリの性質と、(2) 結果的にプログラミング言語に非依存ということである。

### レジストリ

Windowsの場合、COMのクラス、インターフェイス、タイプライブラリは[WindowsレジストリにあるGUIDのリストであり](../Page/レジストリ.md "wikilink")、クラスは"HKEY_CLASSES_ROOT\\CLSID"に、インターフェイスは"HKEY_CLASSES_ROOT\\interface"にある。COMライブラリは各COMオブジェクトが正しいローカルライブラリを特定するためやリモートサービスのネットワーク上の位置を特定するためにレジストリを使用する。DLLサーバー型のCOMコンポーネントはというコマンドラインプログラムを使用してレジストリ登録および登録解除を行なうが、EXEサーバー型のCOMコンポーネントは自身に/RegServerあるいは/UnRegServerスイッチを付けて起動し、レジストリ登録および登録解除を行なう\[10\]。

システムレジストリを使用する性質上、レジストリ登録されたCOMコンポーネントはコンピュータあるいはネットワーク上のすべてのCOMクライアントから共有される。COMコンポーネントをバージョンアップする際にインターフェイスを変更・追加する場合、旧バージョンをレジストリ登録解除したうえで新バージョンをレジストリ登録し直すか、異なる名前およびGUIDを持つインターフェイスを改めて定義した別のコンポーネントをレジストリ登録する必要がある。前者はバージョンアップの際にCOMクライアントの更新は不要だが、破壊的な仕様変更を避けるなど[後方互換性](https://ja.wikipedia.org/wiki/後方互換性 "wikilink")に配慮した設計が求められる。後者は新しいバージョンに対応するCOMクライアントを再作成する必要があるが、複数のバージョンを共存させることができ、バージョン間の互換性を考慮する必要はない。たとえば[Direct3D](../Page/Direct3D.md "wikilink")のバージョン7/8/9/10/11/12は、すべて異なるインターフェイスを持つ独立したCOMコンポーネント\[11\]であり、同一コンピュータ上に共存できる。典型的にいって、COMにおける最良のアプローチは、機能を拡張するためには新しいインターフェイスを定義することである\[12\]。なおCOMコンポーネントのマイナーバージョンアップの際は、通例既存のインターフェイスを継承して新たなインターフェイスを定義する手法が採られる。たとえばDirect3D 10.1あるいは11.1/11.2/11.3における各インターフェイスは、Direct3D 10.0あるいは11.0のインターフェイスからそれぞれ派生した新しいインターフェイスを定義する方法で機能拡張が行なわれている。

[Windows XP以降では](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")、「[分離アプリケーションとSide-by-Sideアセンブリ](https://ja.wikipedia.org/wiki/分離アプリケーションとSide-by-Sideアセンブリ "wikilink")」と呼ばれる仕組みを使い、レジストリではなくマニフェストファイルを使用してコンポーネント依存関係を解決することも可能である。この仕組みを用いることで、COMコンポーネントをシステム全体で共有せず、アプリケーションごとにプライベートアセンブリとして配布・運用することも可能となる。

### 参照カウント

最も基本的なCOMのインタフェースであるIUnknown（全てのCOMインタフェースはここから派生する）は、**QueryInterface()**による機能の確認と、**AddRef()**および**Release()**を通じたオブジェクトの寿命の管理という2つの主要な概念をサポートする\[13\]。参照カウントと機能の確認は（オブジェクトの各インタフェースに対してではなく）オブジェクトに対して適用される。従って注意深く実装する必要がある。

インタフェースへのアクセスを要求したクライアントが存在している限り個々のオブジェクトが生存していることを保障し、逆にオブジェクトを使用していたすべてのコードが終了してそのオブジェクトが不要になった時にオブジェクトを適切に処分するため、インタフェースの[参照カウント](../Page/参照カウント.md "wikilink")というテクニックがCOMでは要求される。COMオブジェクトは参照カウントが0に達したときに自分のメモリを自分で解放する責任がある。

これを実装するため、COMオブジェクトは一般的に参照カウントのための整数値を持つ。オブジェクトのインタフェースからAddRef()が呼ばれるとこの整数値が加算される。Release()が呼ばれるとこの整数値は減算される。AddRef()とRelease()はCOMオブジェクトのクライアントがそのオブジェクトの寿命に関与できる唯一の手段である。内部の整数値はCOMオブジェクトのプライベートなメンバーであり、直接的にはアクセスできない。

AddRef()の目的は、COMオブジェクトへの新しい参照が生じて、その参照が正当である限り生存し続ける必要があるということを、そのCOMオブジェクトに対して示すことである。Release()の目的は、クライアント（またはクライアントコードの一部）がもうオブジェクトを必要としなくなり、もし参照カウントが0に達した場合にはオブジェクトが自らを破棄するであろうということを示すことである。

一部の言語（例えばVisual Basic）では自動参照カウントが提供されるため、COMオブジェクトの開発者はソースコード中で内部参照カウントを明示的に保持する必要がない。C言語でCOMを利用する場合、明示的な参照カウントの操作が必要である。C++では、自分自身でそれを管理することもできるし、参照カウントを全部管理してくれるスマートポインタ（ATL::CComPtrなど）を利用することも選択できる。

下記はCOMオブジェクトで適切な参照カウントの制御を簡単にするためのAddRef()とRelease()を呼び出す際の一般的なガイドラインである。

  - （戻り値またはoutパラメーターで）インタフェースの参照を返す関数（オブジェクトメソッドとグローバル関数のいずれも）は、それを返却する前に、背後にあるオブジェクトの参照カウントを加算しておくべきである。従って関数やメソッドの内部で、AddRef()が（返却する）インタフェースの参照に対して呼び出される。IUnknownインタフェースのQueryInterface()メソッドはこの実例である。従って、リターンされたインタフェースの参照は既に加算されており、リターンされたインタフェースの参照のAddRefを再度呼びだす必要がないということを開発者は理解していなければならない。
  - インタフェースのポインタが上書きされるかスコープから外れる前にインタフェースの参照からRelease()を呼び出さなければならない。
  - インタフェースの参照ポインタからコピーを作る場合、そのポインタでAddRef()を呼び出すべきである。結局この場合は、背後にあるオブジェクトのもう1つの参照を実際に作成している。
  - インタフェースを参照するだけで内部リソースを割り当てる必要があることからインタフェース毎に参照をカウントするようにオブジェクトが実装されているかもしれないため、参照した特定のインタフェースに対してAddRef()とRelease()を呼び出さなければならない。
  - これらの関数の追加の呼び出しはケーブルを超えてリモートオブジェクトに送信されない。プロキシはリモートオブジェクトの参照を1つだけ保持し、ローカルの参照カウントを管理する。

COMの開発を容易にして促進するため、マイクロソフトはC++の開発者のために[Active Template Library](../Page/Active_Template_Library.md "wikilink") (ATL) を導入した。ATLは高レベルのCOM開発パラダイムを提供する。ATLはまた、スマートポインタオブジェクトを提供することによってCOMクライアントのアプリケーション開発者が参照カウントを直接管理しなくてもよいようにする。

その他には[MFC](../Page/Microsoft_Foundation_Class.md "wikilink")、[VBScript](../Page/VBScript.md "wikilink")、Visual Basic、[ECMAScript](../Page/ECMAScript.md "wikilink") ([JavaScript](../Page/JavaScript.md "wikilink"))、[Delphi](../Page/Delphi.md "wikilink")などのライブラリや言語がCOMに対応している。

### インストール

COMは**クラスファクトリ**を利用してCOMオブジェクトのインストール（つまり生成）プロセスを標準化する。COMオブジェクトを作成するため、2つの関連した項目が存在していなければならない。

  - クラスID
  - クラスファクトリ

各COMクラスまたは**コクラス**はユニークなクラスID (GUID) で関連付けられていなければならない。またクラスファクトリとも関連付けられていなければならない（レジストリを利用して行う）。クラスファクトリ自身はCOMオブジェクトである。これはIClassFactoryまたはIClassFactory2インタフェースを持つオブジェクトでなければならない（後者はライセンス管理をサポートしているインタフェースである）。これらのオブジェクトは他のオブジェクトを生成する責任がある。

クラスファクトリオブジェクトは一般的にはCOMオブジェクト自身と同じ実行ファイル内（つまり**サーバーコード**内）に含まれている。ターゲットオブジェクトを作成するようにクラスファクトリを呼び出すとき、このターゲットオブジェクトのクラスIDが提供されていなければならない。このようにしてクラスファクトリはどのクラスのオブジェクトをインスタンス化するのかを把握する。

単一のクラスファクトリオブジェクトは複数のクラスのオブジェクトを生成するかもしれない。すなわち、異なるクラスIDを持つ2つのオブジェクトが同じクラスファクトリオブジェクトによって生成されるかもしれない。しかしながら、これはCOMシステムにとっては曖昧なものではない。

別のオブジェクトにオブジェクト生成の責任を委ねることにより、抽象度が非常に高くなり、開発者に高い柔軟性をもたらす。例えば、**シングルトン**やその他のオブジェクト生成パターンの実装が容易になる。またファクトリオブジェクトはCOMオブジェクトのメモリ割り当てからアプリケーションの呼び出しを守る。

クライアントアプリケーションがクラスファクトリオブジェクトを入手できるようにする必要性から、COMサーバーはそれらを適切に公開しなければならない。クラスファクトリはサーバーコードの特質上、別の方法で公開される。DLL サーバーは**DllGetClassObject()**というグローバル関数をエクスポートしなければならない。EXEサーバーは実行時に**CoRegisterClassObject()**というWindows API関数でクラスファクトリを登録しなければならない。

下記はクラスファクトリを利用したオブジェクト生成のシーケンスの一般的な概略である。

1.  オブジェクトのクラスファクトリを、Windows API関数**CoGetClassObject()**で取得する。
    CoGetClassObject()を呼び出すためには作成するオブジェクトのクラスIDが提供されていなければならない。C++によるコード例を以下に示す。
    ``` cpp
    IClassFactory* pIClassFactory = NULL;

    CoGetClassObject
    (
      CLSID_SomeObject,
      CLSCTX_ALL,
      NULL,
      IID_IClassFactory,
      (LPVOID*)&pIClassFactory
    );
    ```
    上記のコードはCLSID_SomeObjectというクラスIDによって識別されたCOMオブジェクトのクラスファクトリが必要であることを示している。このクラスファクトリオブジェクトはIClassFactoryインタフェースで返される。
2.  返却されたクラスファクトリオブジェクトを使って元々意図していたCOMオブジェクトのインタフェースを生成するように要求する。C++によるコード例を以下に示す。
    ``` cpp
    ISomeObject* pISomeObject = NULL;

    if (pIClassFactory)
    {
      pIClassFactory->CreateInstance
      (
        NULL,
        IID_ISomeObject,
        (LPVOID*)&pISomeObject
      );

      pIClassFactory->Release();

      pIClassFactory = NULL;
    }
    ```
    上記のコードは、クラスファクトリオブジェクトの**CreateInstance()**メソッドを使用して、IID_ISomeObjectというGUIDで識別されるインタフェースを公開しているオブジェクトを生成することを示している。このオブジェクトのISomeObjectインタフェースへのポインタが返される。クラスファクトリオブジェクトはそれ自身がCOMオブジェクトであることから、もう必要なければリリースする必要があるということにも注意してほしい（要するにこれの**Release()**メソッドを呼び出さなければならない）。

上記はオブジェクトをインスタンス化するクラスファクトリの非常に基本的な使用例である。上位レベルのコンストラクタも利用可能であり、その一部はWindows APIを直接利用しないものもある。

例えば、アプリケーションはオブジェクトのクラスファクトリを取得せずにCOMオブジェクトを直接生成するために**CoCreateInstance()** APIを利用できる。しかしながら、CoCreateInstance() APIはオブジェクトのクラスファクトリを取得するためにCoGetClassObject() APIを内部で呼び出しており、そしてCOMオブジェクトを生成するためにクラスファクトリのCreateInstance()メソッドを使用している。

**CreateObject()**というオブジェクトをインスタンス化するためのグローバル関数の他に、C++では**new**を利用できる。C++のコンストラクタはIClassFactory::CreateInstance()メソッドを呼び出して（CoGetClassObject() APIで）目的のオブジェクトのクラスファクトリオブジェクトを取得することを隠蔽する。

PowerBuilderのPowerScriptのように上位レベルのオブジェクトを生成するコンストラクタを提供する言語もある。しかしながらCoGetClassObject()とIClassFactoryインタフェースを使った非常に基本的なオブジェクト生成手法もまだ利用できる。

### [リフレクション](../Page/リフレクション_\(情報工学\).md "wikilink")

COMの初期の時代、オブジェクトがどのような機能を提供するのかということをクライアントから確認するためには、インスタンスを実際に生成して（IUnknownインタフェースの）QueryInterfaceメソッドを呼び出してみるしかなかった。

この検証方法は、特定の業務のために適切なコンポーネントを選択したり、オブジェクトが提供するメソッドの使用方法を開発者が理解できるようにしたりといったところで、多くのアプリケーションにとって不便であるということになった。

結果的にコンポーネントを完全に確認できるCOMタイプライブラリが導入された。タイプライブラリは、コンポーネントのCLSID、コンポーネント実装のインタフェースのIID、これらのインタフェースの各メソッドの解説といった情報を含んでいる。タイプライブラリは一般に[Visual Basicや](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[Visual Studioのような](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")[RAD環境でクライアントアプリケーションの開発者を支援するために利用されている](../Page/Rapid_Application_Development.md "wikilink")。

### プログラミング

COMは「言語にとらわれない」([language-agnostic](https://ja.wikipedia.org/wiki/:en:Language-agnostic "wikilink")) あるいは「言語非依存」(language-independent) のバイナリ標準であり、タイプライブラリすなわちバイナリで定義されたデータ型とインターフェイスを解釈する機能を実装できさえすれば、いかなるプログラミング言語でも開発できる。

ランタイムライブラリ（厳密に言えばプログラマ）は、COMの環境に立ち入って、インスタンス化してCOMオブジェクトの参照をカウントし、バージョン情報からオブジェクトを問い合わせて、新しいバージョンのオブジェクトを利用してコーディングし、新しいバージョンが利用可能でない場合は古いバージョンでも動作するように[フォールトレトラントをコーディングするといった責任がある](../Page/フォールトトレラントシステム.md "wikilink")。

### アプリケーションとネットワークの透過性

プロセス内から、またはコンピューター内のプロセスの境界を越えて、あるいはDCOMテクノロジを利用してネットワークを超えて、COMオブジェクトをインスタンス化して参照できる。

プロセスの外やリモートにあるオブジェクトはメソッドコールや戻り値をやりとりするためにマーシャリングを利用できる。

マーシャリングでは、オブジェクトや、オブジェクトを利用しているコードは見えない。

### COMのスレッド

COMでは、**アパートメントモデル**として知られているコンセプトによってスレッドの問題を解決している。ここで言う**アパート**とは、単一のスレッドまたはスレッドのグループの中にある実行コンテキストが1つまたは複数のCOMオブジェクトに関連づけられていることを指している。

アパートメントでは以下のガイドラインが関連するスレッドとオブジェクトのために示される。

  - 1つのCOMオブジェクトは1つのアパートメントだけに関連づけられる。オブジェクトが実行時に生成された時点で関連づけられる。オブジェクトの初期化後は一生そのアパートメントに属する。
  - COMスレッド（つまりCOMオブジェクトを生成したか、COMのメソッドコールが行われたスレッド）もまた1つのアパートメントに関連づけられる。COMオブジェクトと同様、スレッドとアパートメントの関連づけは初期化時に決定される。各COMのスレッドもまた終了するまで指定されたアパートメントに属し続ける。
  - メソッドを呼び出すスレッドとオブジェクトが同じアパートメントに属す場合、COMの介入無しに直接呼び出される。
  - メソッドを呼び出すスレッドとオブジェクトが異なるアパートメントに属す場合、そのメソッド呼び出しはマーシャリングを利用して行われる。これにはプロキシとスタブが利用される。

COMの世界では、**シングルスレッドアパートメント (STA)**、**マルチスレッドアパートメント (MTA)**、**中立アパートメント (NA)** の3つのアパートメントモデルがある。各アパートメントは、オブジェクトの内部状態が複数のスレッドを超えて同期されるかどうかという1つのメカニズムを表している。

シングルスレッドアパートメントモデルは非常に一般的に利用されているモデルである。ここではCOMオブジェクトはデスクトップアプリケーションのユーザーインタフェースに似た立場にある。STAモデルでは、単一のスレッドがオブジェクトのメソッドを動かすことに専念している。つまり常に単一のスレッドでオブジェクトのメソッドが実行される。このようなアパートメントでは、アパートメントの外にあるスレッドからのメソッドコールはマーシャリングされ、（標準のWindowsのメッセージキューを利用して）システムによって自動的にキューに入れられる。これによりその呼び出しが完了してから各オブジェクトのメソッド呼び出しが実行されるようになり、レースコンディションや同期性の欠如といった心配がない。プロセスの中で最初に作られたSTAは特にメインSTAと呼ばれ、マルチスレッドを全く考慮していないCOMオブジェクトはメインSTAだけで動作させられる。

COMオブジェクトのメソッドの同期を自分で取りたい場合、メソッドを呼び出したスレッドと同一のスレッドでメソッドを処理するようにできる。これをマルチプルスレッドアパートメントと呼ぶ。ただし、STAスレッドからのMTAオブジェクトのメソッド呼び出しはマーシャリングされる。プロセスは複数のCOMオブジェクトで構成でき、その一部をSTAにしてそれ以外はMTAを利用するというようにできる。

COM+で導入されたスレッド中立アパートメントは、オブジェクトのメソッド呼び出しを管理する必要がない場合に用いられる。唯一の条件はオブジェクトの全てのメソッドが[リエントラント](../Page/リエントラント.md "wikilink")（再入可能）でなければならないということである。中立アパートメントに属すオブジェクトのメソッドは、STAスレッド・MTAスレッド、どちらからでもマーシャリングなしに直接呼び出せる。

## 関連項目

  - [Bonobo](../Page/Bonobo.md "wikilink")

## 参考文献

  -
## 脚注

## 外部リンク

  - [COM (Component Object Model)](http://msdn.microsoft.com/en-us/library/ms680573.aspx) - MSDN Library

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:オブジェクト指向](https://ja.wikipedia.org/wiki/Category:オブジェクト指向 "wikilink") [Category:プログラミング](https://ja.wikipedia.org/wiki/Category:プログラミング "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink")

1.  [Component Object Model (COM) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/com/component-object-model--com--portal)
2.  [The Component Object Model - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/com/the-component-object-model)
3.  [\[MC-COMQC](https://docs.microsoft.com/en-us/openspecs/windows_protocols/mc-comqc/6fef5fdf-0c85-456e-8c1b-16d061cf9664): Component Object Model Plus (COM+) Queued Components Protocol | Microsoft Docs\]
4.  [The Mono Runtime | Mono](https://www.mono-project.com/docs/advanced/runtime/)
5.  [COM Interop | Mono](https://www.mono-project.com/docs/advanced/com-interop/)
6.  DirectXのCOMは主にC++から使われることを想定した独自実装となっており、標準的なCOMの流儀に則っていない部分もある。オブジェクトの生成に`CoCreateInstance()`関数を利用せず`D3D11CreateDevice()`のような独自のファクトリ関数を用意している、`IXAudio2SourceVoice`のように`IUnknown`派生でないインターフェイスが存在している、といった具合である。
7.  例えば[Microsoft Visual Studioのプロジェクトファイルおよびソリューションファイルでは](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、各プロジェクトを識別するためにGUIDが使われる。
8.  [Windows 8時代のアプリ開発とWinRT － ＠IT](http://www.atmarkit.co.jp/fdotnet/chushin/win8appdev_01/win8appdev_01_01.html)
9.
10. [ActiveXコントロール、ActiveXサーバ、およびタイプライブラリを登録する方法 - National Instruments](http://digital.ni.com/public.nsf/allkb/BBAEED03672FC02486256AAF002782B6)
11. [DirectX に関してよく寄せられる質問](https://msdn.microsoft.com/ja-jp/library/ee416788.aspx)
12. [The Versioning Theory for RPC and COM (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/aa378963.aspx)
13. [参照カウント](https://msdn.microsoft.com/ja-jp/library/4947zb56%28v=vs.100%29.aspx)