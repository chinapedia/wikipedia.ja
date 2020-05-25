> この記事は[Common Open Software Environment](https://ja.wikipedia.org/wiki/Common_Open_Software_Environment)から翻訳されています。


**Common Open Software Environment**（**COSE**）は[1993年](../Page/1993年.md "wikilink")3月、当時の主な[UNIX](../Page/UNIX.md "wikilink")ベンダーが結成した業界団体であり、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の統合されたオープンな標準を策定することを目的としていた。\[1\]

## 背景

COSE が結成されたのは、「[UNIX戦争](../Page/UNIX戦争.md "wikilink")」がUNIX業界の成長を阻害していることが明らかになったころであった。[マイクロソフト](../Page/マイクロソフト.md "wikilink")は既にデスクトップ市場を支配しており、UNIX市場（特にエンジニアリング・[ワークステーション](../Page/ワークステーション.md "wikilink")と[データセンター](https://ja.wikipedia.org/wiki/データセンター "wikilink")）にも触手を伸ばし始めていた。さらに[ノベルの](../Page/ノベル_\(企業\).md "wikilink") [NetWare](https://ja.wikipedia.org/wiki/NetWare "wikilink") は徐々にマイクロソフトのネットワーク製品に市場を侵食されつつあった。マイクロソフトとの多面的な競争の切り札として UNIX を生かすべく、ノベルと[AT\&T](../Page/AT&T.md "wikilink")は Univel と名づけた協業を開始した（1991年に開始され、1993年にノベルがUNIX関連資産を買い取って終了）。

それまでもUNIXの統合の努力はなされていたが、COSE には2つの特徴があった。1つは、UNIX陣営が1つにまとまった最初の試みだった点である。第二は、既存技術の標準化よりも新たな技術を一から作ることを指向していた点である。

初期メンバー企業は以下の通り（"The Big Six" あるいは "SUUSHI" とも呼ばれる）:

  - [ヒューレット・パッカード](../Page/ヒューレット・パッカード.md "wikilink")
  - [IBM](../Page/IBM.md "wikilink")
  - Santa Cruz Operation ([SCO](../Page/SCO.md "wikilink"))
  - [サン・マイクロシステムズ](../Page/サン・マイクロシステムズ.md "wikilink")
  - Univel
  - [UNIX Systems Laboratories](https://ja.wikipedia.org/wiki/UNIX_Systems_Laboratories "wikilink") (USL)

これら企業は当時の主なUNIXシステムとOSベンダーであり、UNIXブランドとAT\&T由来のソースコードを保持していた。また、1980年代後半から1990年代初期にかけて存在した2つのUNIX陣営である [OSF](../Page/Open_Software_Foundation.md "wikilink") と [UNIX International](https://ja.wikipedia.org/wiki/UNIX_International "wikilink") (UI) を代表する企業群でもある。OSF の重要メンバーだった[DEC](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink") の名がないが、同年6月にはDECもCOSEを支持する声明を発表している\[2\]。

COSE が重点領域としたのは、共通デスクトップ環境、ネットワーク、グラフィックス、マルチメディア、オブジェクトベースの技術、システム管理であった。1993年9月1日、COSE は75以上の企業のサポートを得て統合UNIX仕様を開発することを発表した\[3\]。

## UNIX標準化

OSF や UI とは異なり、COSE は単一のオペレーティングシステムを作成・振興しようとはしなかった（[リファレンス実装](../Page/リファレンス実装.md "wikilink")を定めなかった）。その代わりに、既存のOSインタフェース仕様文書を調査・検討した。この結果として "Spec 1170" と呼ばれるリストが作成され、それが後の [Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") へと繋がっていった\[4\]。

Spec 1170（[SPECベンチマークとは無関係](../Page/Standard_Performance_Evaluation_Corporation.md "wikilink")）は、COSE が既存のUNIXインタフェースでどれが実際に使われているかを調査した結果であった。既存のUNIXアプリケーション群を調査し、1,170 の[システムコール](../Page/システムコール.md "wikilink")とライブラリ関数をリストアップした。ただし、その後もインタフェースは追加され、成長していった。

仕様の管理は [X/Open](https://ja.wikipedia.org/wiki/X/Open "wikilink") に任された。1993年10月、当時ノベルが権利を所有していた UNIX の商標は X/Open に権利が移された\[5\]。これにより、UNIXブランドは特定のソースコード実装とは無関係となった。どんな企業でも UNIX 仕様に準拠した OS を開発すれば、それに UNIX ブランドを利用する資格を有することになった。

## Common Desktop Environment

UNIXブランドのオープン化と標準化とは別に、COSE は [Common Desktop Environment](../Page/Common_Desktop_Environment.md "wikilink") (CDE) を開発した。CDE は [X Window System](../Page/X_Window_System.md "wikilink") ベースのユーザ環境であり、HP、IBM、サンが共同開発した。そのインタフェースおよび開発ツールには OSF の [Motif](../Page/Motif_\(GUI\).md "wikilink") [ウィジェット・ツールキット](../Page/ウィジェット・ツールキット.md "wikilink")が使われた\[6\]。

## その他の技術

[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")やOS自体については、COSE は一種の統合を達成した。しかし、他の領域では既存の競合する規格を同時に承認するという方針を採用した。例えばネットワークに関しては、OSF の [DCE](../Page/Distributed_Computing_Environment.md "wikilink")、UI の [ONC+](../Page/Open_Network_Computing_Remote_Procedure_Call.md "wikilink")、NetWare クライアントが採用された。

その他の領域では、様々な対応がなされた。オブジェクトベース技術では、[CORBA](../Page/Common_Object_Request_Broker_Architecture.md "wikilink") が基盤技術として選ばれたが、実装方法は各企業に任された。

## COSEの遺産

[1994年](../Page/1994年.md "wikilink")3月、UI と OSF は合併し、OSF を名乗ることを発表した\[7\]。COSE は新生OSFの "Pre-Structured Technology" (PST) プロセスの基盤となった\[8\]。これが[1996年](../Page/1996年.md "wikilink")、OSF と X/Open の合併した [The Open Group](../Page/The_Open_Group.md "wikilink") へと発展していった。

結果として、COSE は統一されたUNIX標準を生み出した。また、サンの [OPEN LOOK](https://ja.wikipedia.org/wiki/OPEN_LOOK "wikilink") に止めを刺し、[Motifベースのデスクトップが標準となることに貢献した](../Page/Motif_\(GUI\).md "wikilink")。当初掲げていた他の領域ではそれほど影響を与えることはなかったが、たった12カ月存在しただけでUNIXの将来の方向に重大な影響を与えた。

## 脚注

[Category:標準化団体](https://ja.wikipedia.org/wiki/Category:標準化団体 "wikilink") [Category:UNIXに関連する組織](https://ja.wikipedia.org/wiki/Category:UNIXに関連する組織 "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.