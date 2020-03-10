> この記事は[Distributed Component Object Model](https://ja.wikipedia.org/wiki/Distributed_Component_Object_Model)から翻訳されています。


**Distributed Component Object Model**（**DCOM**）は、ネットワーク上に分散配置された[コンピュータ](../Page/コンピュータ.md "wikilink")上の[ソフトウェアコンポーネント](../Page/ソフトウェアコンポーネント.md "wikilink")間通信（[分散オブジェクト](https://ja.wikipedia.org/wiki/分散オブジェクト "wikilink")技術）のための[マイクロソフト](../Page/マイクロソフト.md "wikilink")独自の技術。

## 概要

DCOM は当初 "Network OLE" と呼ばれ、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[COMを拡張したものであり](../Page/Component_Object_Model.md "wikilink")、マイクロソフトの COM+ サーバ基盤上での通信基盤となっていた。その後、[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") の登場とともに廃れていった。

頭に "D" と付いたのは、[DCE/RPC](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink") （正確に言えば、DCE/RPC をマイクロソフトが拡張した MSRPC）を採用したことからである。

COM から DCOM への拡張では以下の問題を解決しようとした:

  - マーシャリング - リモートのメソッド呼び出しでの[シリアライズ](../Page/シリアライズ.md "wikilink")
  - 分散[ガベージコレクション](../Page/ガベージコレクション.md "wikilink") - 例えば、クライアントプロセスが壊れたり、ネットワーク接続が失われたとき、インタフェースのクライアントが保持する[参照が解放されることを保証する](https://ja.wikipedia.org/wiki/参照_\(情報工学\) "wikilink")。

これらを解決するため、DCOM の基盤となる RPC 機構として[DCE/RPC](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink")が使われた。DCE/RPCでは、マーシャリングやメモリ解放の責任について厳密な規則が規定されていた。

DCOM は [CORBA](../Page/Common_Object_Request_Broker_Architecture.md "wikilink") と対抗する規格であった。これらの技術は、インターネット上でのコードとサービスの再利用のためのモデルとなると考えられていた。しかし、これらの技術をファイアウォール上で利用する際の困難さや、セキュリティの確保されていないマシン上で使用する際の問題のため、HTTP と[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の組合せがこれらの技術に勝利した。マイクロソフトは "ncacn_http" (Network Computing Architecture, Connection-based, over HTTP) と呼ばれるHTTPトランスポートを DCE/RPC に追加することでこの流れを止めようとして失敗した（後にこの手法は HTTP 上で Exchange 2003 接続をサポートするために復活した）。

## 派生のバージョンと実装

[The Open Group](https://ja.wikipedia.org/wiki/The_Open_Group "wikilink") は COMsource という DCOM 実装を開発した。このソースコードは The Open Group から入手可能であり、完全な[文書も付属している](../Page/ソフトウェアドキュメンテーション.md "wikilink")。この文書によれば、COMsource のソースは[Windows NT](../Page/Microsoft_Windows_NT.md "wikilink") 4.0 のソースコードから直接持ってきたものであり、Windows NT Registry Service のソースコードもそれに含まれている。

[Wine](https://ja.wikipedia.org/wiki/Wine "wikilink")のチームもDCOMを実装している。バイナリ互換性を確保する目的であり、DCOM をネットワーク上で使用するためではない。マイクロソフトのAPIを通してNDR（Network Data Representation）を実装するに留まっているが、可能な限り MSRPC と互換性を保とうとしている。

[j-Interop](http://j-interop.sourceforge.net/) は、[Java上での](../Page/Javaプラットフォーム.md "wikilink") MSRPC のオープンソース（[LGPL](../Page/GNU_Lesser_General_Public_License.md "wikilink")）実装であり、DCOMサーバとやり取りするDCOMクライアントをJavaで作成することができる。

## 関連項目

  - [ActiveX](../Page/ActiveX.md "wikilink")
  - [Component Object Model](../Page/Component_Object_Model.md "wikilink") (COM)
  - [動的データ交換](https://ja.wikipedia.org/wiki/動的データ交換 "wikilink") (DDE)
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [.NET Remoting](https://ja.wikipedia.org/wiki/.NET_Remoting "wikilink")
  - [Object Linking and Embedding](https://ja.wikipedia.org/wiki/Object_Linking_and_Embedding "wikilink") (OLE)

## 外部リンク

  - [The Open Groups COMsource](http://opengroup.org/comsource)
  - [j-Interop](http://j-interop.sourceforge.net/)

[Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:オペレーティングシステムの仕組み](https://ja.wikipedia.org/wiki/Category:オペレーティングシステムの仕組み "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")