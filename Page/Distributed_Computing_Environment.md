> この記事は[Distributed Computing Environment](https://ja.wikipedia.org/wiki/Distributed_Computing_Environment)から翻訳されています。


**Distributed Computing Environment**（**DCE**）は、1990年代初期に[アポロコンピュータ](https://ja.wikipedia.org/wiki/アポロコンピュータ "wikilink")（現在の[ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")の一部）、[IBM](../Page/IBM.md "wikilink")、[DECなどが結成したコンソーシアムが開発したソフトウェアシステムである](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")。DCE は[クライアントサーバモデル](https://ja.wikipedia.org/wiki/クライアントサーバモデル "wikilink")のアプリケーション開発のためのフレームワークとツールキットを提供する。フレームワークには、[遠隔手続き呼出し](https://ja.wikipedia.org/wiki/遠隔手続き呼出し "wikilink") (RPC) 機構 [DCE/RPC](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink")、ネーミング（ディレクトリ）サービス、タイムサービス、[認証](../Page/認証.md "wikilink")サービス、[認可サービス](https://ja.wikipedia.org/wiki/認可_\(セキュリティ\) "wikilink")、[分散ファイルシステム](https://ja.wikipedia.org/wiki/分散ファイルシステム "wikilink") [DCE/DFS](https://ja.wikipedia.org/wiki/DCE_Distributed_File_System "wikilink") が含まれる。

## 歴史

DCE は[1980年代](../Page/1980年代.md "wikilink")の[UNIX戦争](https://ja.wikipedia.org/wiki/UNIX戦争 "wikilink")と深い関係がある。[サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")と[AT\&T](../Page/AT&T.md "wikilink")が共同で [UNIX System V Release 4](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink") (SVR4) を開発するようになると、他のUNIXベンダーは彼らの製品が市場で不利になると考えた。そこで彼らは [Open Software Foundation](https://ja.wikipedia.org/wiki/Open_Software_Foundation "wikilink") (OSF) を結成し、[BSD](../Page/BSD.md "wikilink")ベースのUNIXで対抗しようとした。OSF は[Mach](../Page/Mach.md "wikilink")カーネルに基づいた [OSF/1](https://ja.wikipedia.org/wiki/Tru64_UNIX "wikilink") を完成させたが、SVR4 に比較すると性能が悪く、DEC 以外ではほとんど使われなかった。

OSF の結成に伴い、メンバー各社が様々な進行中プロジェクトの成果を持ち寄った。当時、ネットワークコンピューティングが重要な課題となっており、多くの企業がRPCシステムの開発を行っていた。それらを統合して「公式の」RPC機構を再構築することで、OSF は SVR4 に対して優位に立とうとした。それが DCE であり、DCE をサポートするのが OSF/1 である。

DCEシステムは、その大部分が個々のメンバー企業が独自に開発したものに基づいている。[DCE/RPC](https://ja.wikipedia.org/wiki/DCE/RPC "wikilink") は[アポロコンピュータ](https://ja.wikipedia.org/wiki/アポロコンピュータ "wikilink")の開発した Network Computing System (NCS) がベースとなっている。ネーミングサービスは DEC の成果に基づいている。DCE/DFS は[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")が開発した [Andrew File System](https://ja.wikipedia.org/wiki/Andrew_File_System "wikilink") (AFS) に基づいている。認証システムは[ケルベロス認証](https://ja.wikipedia.org/wiki/ケルベロス認証 "wikilink")に基づき、認可システムは[アクセス制御リスト](https://ja.wikipedia.org/wiki/アクセス制御リスト "wikilink") (ACL) に基づいている。これらの機能を統合して、DCE は[C言語](../Page/C言語.md "wikilink")ベースの完全なネットワークコンピューティングシステムを提供するようになった。ネットワーク上の任意のマシンがユーザーを認証し、リソースへのアクセスを許し、単一の統合された [API](../Page/アプリケーションプログラミングインタフェース.md "wikilink") で遠隔から呼び出すことを可能にした。

1980年代末期から[1990年代](../Page/1990年代.md "wikilink")初期に想定されたほど、この種の分散処理は広く利用されることはなかった。[インターネット](https://ja.wikipedia.org/wiki/インターネット "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")といった新たな技術が1990年代中盤以降に盛んになり、[CORBAのようなシステムも競合することとなった](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")。皮肉なことに、DCE/RPC は[マイクロソフト](../Page/マイクロソフト.md "wikilink")の [DCOM](../Page/Distributed_Component_Object_Model.md "wikilink") や [ODBC](../Page/Open_Database_Connectivity.md "wikilink") でトランスポート層(MSRPC)として使われることで生き延びた。

OSF とそのプロジェクト群は [The Open Group](../Page/The_Open_Group.md "wikilink") に統合され、[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[1月12日](../Page/1月12日.md "wikilink")に[LGPLライセンスで](../Page/GNU_Lesser_General_Public_License.md "wikilink") DCE 1.2.2 がリリースされることとなった。それ以前にも DCE 1.1 は OSF BSD ライセンスでリリースされており、[2000年](../Page/2000年.md "wikilink")には [FreeDCE](http://freedce.sf.net) が登場している。FreeDCE には DCOM の実装も含まれている。

## アーキテクチャ

DCE における大きな管理単位を「セル; cell」と呼ぶ。セル内の最高特権を持つものを「セル管理者; cell administrator」と呼び、一般に *cell_admin* というユーザー名が割り当てられる。これは通常のOSレベルのユーザーである必要はない。cell_admin はセル内の全DCEリソースについての全ての権利を有する。権限はDCEリソース毎に user_obj、group_obj、other_obj、any_other の4つのカテゴリ毎に付与または制限される。このうち、最初の3つは、所有者、グループメンバー、それ以外に対応する。any_other は DCE のユーザーでない者を意味する。複数のセル間でリソースを共有し通信するような構成が可能である。セル外部からのアクセスについては "foreign" ユーザーとして扱い、必要に応じて権限を付与・制限できる。さらに、特定のユーザーやグループに任意のDCEリソースについての権限を与えることもできる。これは ACL のない従来のUNIXでは不可能だったことである。

DCE のセルに存在する主な構成要素は以下の通りである。

1.  **セキュリティサーバ** - 認証を行う
2.  **Cell Directory Server** (CDS) - リソースやACLのリポジトリ
3.  **Distributed Time Server** - セル全体に正確な時刻を供給する。

IBM の DCE 実装では、セキュリティサーバにはケルベロス、CDS には LDAP、タイムサーバには [Network Time Protocol](../Page/Network_Time_Protocol.md "wikilink") が使われている。

DCE で分散ファイルシステムを実装するには、ファイル名をCDSに登録し、それに適切なACLを設定することで実現できるが、これでは扱いにくい。DCE/DFS は DCE における分散ファイルシステム機能を提供するアプリケーションである。DCE/DFS では複数のサーバ上にファイルシステム（DCE/DFS ではファイルセットと呼ぶ）の複製を持つ。そのうち1つが読み書き可能なコピーであり、他は読み込みのみ可能である。読み書き可能なコピーとその他のコピーの間で複写が行われる。さらに DCE/DFS にはバックアップ機能もあり、最新の複写の前の状態のファイルセットを保持する。

DCE/DFS は POSIX のファイルシステムを完全に正しく実装した唯一の分散ファイルシステムとされている（バイト単位のロック機構など）。DCE/DFS の信頼性を実証したのは、[1996年](../Page/1996年.md "wikilink")の[アトランタオリンピック](https://ja.wikipedia.org/wiki/アトランタオリンピック "wikilink")のWebサイトであった。[IBM](../Page/IBM.md "wikilink") はそのバックエンドに DCE/DFS を使い、編集と参照を世界中から行えることを示した。

## 外部リンク

  - [The Open Group's DCE Portal](http://www.opengroup.org/dce/)
  - [DCE description at Carnegie Mellon's Software Engineering Institute](http://www.sei.cmu.edu/str/descriptions/dce.html)
  - [FreeDCE](http://sourceforge.net/projects/freedce)

[Category:分散処理](https://ja.wikipedia.org/wiki/Category:分散処理 "wikilink") [Category:ネットワークソフト](https://ja.wikipedia.org/wiki/Category:ネットワークソフト "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")