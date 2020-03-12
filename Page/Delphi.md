> この記事は[Delphi](https://ja.wikipedia.org/wiki/Delphi)から翻訳されています。


**Delphi**（デルファイ）は、[コンソール](https://ja.wikipedia.org/wiki/コンソールアプリケーション "wikilink") ([CUI](../Page/キャラクタユーザインタフェース.md "wikilink"))、デスクトップ ([GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink"))、Web、[モバイルアプリケーション](https://ja.wikipedia.org/wiki/モバイルアプリケーション "wikilink")開発のための[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である。

Delphiの[コンパイラ](../Page/コンパイラ.md "wikilink")は[Object Pascalの独自拡張](../Page/Object_Pascal.md "wikilink") (Delphi 言語) を用いて、プラットフォーム毎にネイティブコードを生成する。対応プラットフォームは[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、[Android](../Page/Android.md "wikilink")、[Linux](../Page/Linux.md "wikilink")。

元々Delphiは[ボーランド](../Page/ボーランド.md "wikilink")が[Turbo Pascal](../Page/Turbo_Pascal.md "wikilink") / Borland Pascalの後継として開発した[Windows用の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[RADツールである](../Page/Rapid_Application_Development.md "wikilink")。[C++ Builderとは多くのコアコンポーネント](../Page/C++_Builder.md "wikilink")、特にIDEと[Visual Component Library](../Page/Visual_Component_Library.md "wikilink") (VCL) を共有していたが、[RAD Studioの前身となる](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")[Borland Developer Studio 2006の登場まではそれぞれ独立した製品だった](https://ja.wikipedia.org/wiki/Delphi#Delphi_2006.E3.80.81Turbo_Delphi "wikilink")。

[2006年](../Page/2006年.md "wikilink")にボーランドの開発ツール部門が[コードギア](../Page/コードギア.md "wikilink")として完全子会社化され、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")に[エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")に買収された。[2015年](../Page/2015年.md "wikilink")10月に、上記[エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")が[アイデラ](https://ja.wikipedia.org/wiki/アイデラ "wikilink")により買収される発表がなされた\[1\]。

本項では **Delphi Prism** として開発されていた 「**Embacardero Prism**（エンバカデロ プリズム）」 についても述べる。

## 概要

Delphiは[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")、[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")、[Android](../Page/Android.md "wikilink")、[Linux](../Page/Linux.md "wikilink")向けアプリケーションを開発するための[統合開発環境](../Page/統合開発環境.md "wikilink") (IDE) である。

「コンポーネント」 と呼ばれるソフトウェア部品を 「[フォーム](https://ja.wikipedia.org/wiki/フォーム "wikilink")」 や 「データモジュール」 に貼り付ける手法により、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")やアプリケーションロジックの設計を視覚的に行え、ソフトウェアの開発を迅速に行える。またコンポーネント自体も Delphi で開発可能であり、その開発環境自身も利用者（開発者）のニーズに従って拡張可能である。[コンポーネント指向プログラミング](https://ja.wikipedia.org/wiki/コンポーネント指向プログラミング "wikilink")を体現した開発環境といえる。

Delphiで使われるコンポーネントのフレームワークには 「[Visual Component Library](../Page/Visual_Component_Library.md "wikilink") (VCL)」、「[Component Library for Cross Platform](../Page/Component_Library_for_Cross_Platform.md "wikilink") (CLX)」、「 (FMX)」 がある。このフレームワークを用いて[C++](../Page/C++.md "wikilink")言語でのWindows向けソフトウェア開発を実現したものが 「[C++ Builder](../Page/C++_Builder.md "wikilink")」 である。

  - [VCLは最初期のDelphiから存在するWindows専用のフレームワークであり](../Page/Visual_Component_Library.md "wikilink")、[Windows APIおよびWindowsコントロール](../Page/Windows_API.md "wikilink")（UI部品）を抽象化したものである。
  - Object Pascal (Delphi) / C++ ([C++ Builder](../Page/C++_Builder.md "wikilink")) 言語での[Linux](../Page/Linux.md "wikilink")ソフトウェア開発を可能にした製品として 「[Kylix](../Page/Kylix.md "wikilink")」 がある。これはCLXフレームワークによるマルチプラットフォームアプリケーション作成を行うもので、Windowsでは　Delphi / [C++ Builder](../Page/C++_Builder.md "wikilink") を、[Linux](../Page/Linux.md "wikilink")では[Kylix](../Page/Kylix.md "wikilink")を用いてマルチプラットフォームアプリケーション開発を行うものだった。しかしながら[Linux](../Page/Linux.md "wikilink")の[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")のサポートの難しさから安定した品質を提供できずに[Kylix 3を最後に開発を終了しており](../Page/Kylix.md "wikilink")、DelphiでのCLXサポートも[Delphi 7が最後となっている](https://ja.wikipedia.org/wiki/Delphi#Delphi_7 "wikilink")。
  - [Delphi XE2以降](https://ja.wikipedia.org/wiki/Delphi#Delphi_XE2 "wikilink")、FireMonkeyフレームワークによるマルチプラットフォームアプリケーション開発に対応し、最新版ではWindows、macOS、iOS、Android、Linux向けのアプリケーションを作成する事が可能となっている。ただし、開発環境としてのDelphiは依然としてWindows上でしか動作しない。

のIDEでは見慣れた「[イベントハンドラ](https://ja.wikipedia.org/wiki/イベントハンドラ "wikilink")に対してオブジェクトイベントを delegation (委譲) する」いわゆる**2Way-Tool**の手法は[ボーランド](../Page/ボーランド.md "wikilink")の特許である（発明者は[アンダース・ヘルスバーグ](../Page/アンダース・ヘルスバーグ.md "wikilink")）\[2\]\[3\]。

Delphiはバージョン1から5までは順調にバージョンアップを繰り返し、それなりに人気もあったが、[Delphi 6](https://ja.wikipedia.org/wiki/Delphi#Delphi_6 "wikilink") / [7ではドキュメントの品質が明らかに低下し](https://ja.wikipedia.org/wiki/Delphi#Delphi_7 "wikilink")、[Delphi 8以降](https://ja.wikipedia.org/wiki/Delphi#Delphi_8 "wikilink")[.NET Frameworkや](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[C\#もサポートした巨大な開発ツール](../Page/C_Sharp.md "wikilink") ([RAD Studio](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")) に発展したが、製品自体の品質が落ちてしまい、利用者を急速に失った。その後、Delphiはボーランドのツール部門買収などの混乱の中で低迷が続いていたが、エンバカデロ・テクノロジーズのもとで[C\#と](../Page/C_Sharp.md "wikilink")[.NET Frameworkのサポートを廃止しスリム化](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、[Delphi 2009で再び](https://ja.wikipedia.org/wiki/Delphi#Delphi_2009 "wikilink")[Win32用のツールとして再出発を果たした](https://ja.wikipedia.org/wiki/Windows_API#Win32 "wikilink")。その後[Unicode](../Page/Unicode.md "wikilink")サポートなど多くの機能拡張も行われ、macOS、iOS、Android、Linux向けのアプリケーション開発にも対応、品質も安定してきており、往年の実力を取り戻しつつある。

## 歴史

### 名前の由来

「Delphi」 とは、[ギリシャ](../Page/ギリシャ.md "wikilink")の古代都市 「[デルフォイ](../Page/デルポイ.md "wikilink")」 に由来する。[デルフォイにあるアポロン神殿は](../Page/デルポイ.md "wikilink")、その託宣 (Oracle) を時の為政者だけではなく、一般人にも授けたことから人気が集まり、その門前町である都市国家[デルフォイは古代の人気観光スポットだった](../Page/デルポイ.md "wikilink")。

当初は[Oracle Databaseサーバのフロントエンドとしての採用を目論んでおり](../Page/Oracle_Database.md "wikilink")、それにちなんだコードネームとしてDelphiが選ばれた。AppBuilderという製品名で発売しようとしたが[ノベル製品の名称](../Page/ノベル_\(企業\).md "wikilink") (Visual AppBuilder) と競合してしまい、議論と市場調査の結果、コードネームがそのまま製品名となった\[4\]。

### Delphi 1から5まで

Delphi（製品名: **Delphi for Windows**、コードネーム: Delphi）は[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")9月に発売された。最初のバージョンは[Windows 3.1用として開発された](../Page/Microsoft_Windows_3.x.md "wikilink")。[Turbo Pascal譲りの](../Page/Turbo_Pascal.md "wikilink")[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")をその土台に据えつつ、インタプリタ動作と錯覚してしまうほどの高速なコンパイラを備え、「コンポーネント」 と呼ばれる設計部材による視覚的（ビジュアル）開発手法を採用するというDelphiの基本的な性格は、この時既に定まっており、この画期的な製品は[ソフトウェア開発者](https://ja.wikipedia.org/wiki/ソフトウェア開発者 "wikilink")から大きな注目を浴びた。Delphi 1はシリーズを通して唯一の[16ビット](../Page/16ビット.md "wikilink")開発環境としての側面も併せ持っている。なお、当初の日本語版には英語版で提供されていたDatabase Desktopや[InterBase](../Page/InterBase.md "wikilink")などが含まれておらず、価格も安価（29,800円）に設定されていた。その後、これらのツールを含む **Delphi and Database Tools**（68,000円）が発売された。

「**Delphi 2**」（コードネーム: Polaris）は[1996年](../Page/1996年.md "wikilink")に発売された\[5\]。これ以降、Delphiは開発対象を[Windows 95に代表される](../Page/Microsoft_Windows_95.md "wikilink")[32ビット](../Page/32ビット.md "wikilink")Windows (Win32) に移した。[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Visual Basicと](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")[Visual C++の長所を兼ね備えた開発環境として人気を博し](../Page/Microsoft_Visual_C++.md "wikilink")、その後も順調にバージョンアップを繰り返した。

「**Delphi 3**」（コードネーム: Ivory）は[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に発売された\[6\]。Delphi 1 発売以来の様々な問題点をほぼ改修し、パッケージと呼ばれるDelphi独自の[DLL形式をサポート](../Page/ダイナミックリンクライブラリ.md "wikilink")、[ActiveX](../Page/ActiveX.md "wikilink")コントロールの開発をサポートし、[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")開発機能を提供した。完成度の高いバージョンであり、その後のDelphiの原型となった。

「**Delphi 3.1**」 はDelphi 3のマイナーバージョンアップ版で、Delphi 3ユーザーにはDelphi 3.1の[CD-ROM](../Page/CD-ROM.md "wikilink")が郵送された。このバージョンは日本でのみリリースされた。\[7\]

「**Delphi 4**」（コードネーム: Allegro）は[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に発売された\[8\]。NT サービスアプリケーションの開発、[CORBAをサポート](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")。

「**Delphi 5**」（コードネーム: Argus）は[1999年](../Page/1999年.md "wikilink")に発売された\[9\]。[ADO対応](https://ja.wikipedia.org/wiki/ActiveX_Data_Objects "wikilink") (**ADO Express**)、[COMオブジェクトコンポーネントラッパーを提供](../Page/Component_Object_Model.md "wikilink")。

### Delphi 6

「**Delphi 6**」（コードネーム: Iliad）は[2001年](../Page/2001年.md "wikilink")[7月9日](../Page/7月9日.md "wikilink")に発表された。

[SOAPを利用する](../Page/SOAP_\(プロトコル\).md "wikilink")[Webサービス](../Page/Webサービス.md "wikilink")の作成機能、コンポーネントベースでWeb画面が設計できるWebSnap、新しいデータベースフレームワーク**dbExpress** (DBX)、[Linux](../Page/Linux.md "wikilink")版Delphi ([Kylix](../Page/Kylix.md "wikilink")) と共通のComponent Library for Cross-Platform (CLX) などを搭載した意欲作。BDE (Borland Database Engine) は、このDelphi 6付属のバージョンである5.2が最終版となった。[Windows 2000に対応](../Page/Microsoft_Windows_2000.md "wikilink")。日本でも無償のPersonal版が提供された。

### Delphi 7 / 7.1

「**Delphi 7**」（コードネーム: Aurora）は[2002年](../Page/2002年.md "wikilink")[8月22日](../Page/8月22日.md "wikilink")に発表された。

Delphi 1以来の伝統的なIDEを用いた最後の製品で、完成度の面で評価が高い。[Windows XPに対応](../Page/Microsoft_Windows_XP.md "wikilink")。

Professional版以上では「**Delphi 7 Studio**」の名称を使用。6で無償であったPersonal版は有償に変更になった。IntraWeb、RaveReportを搭載。Delphi for .NETのプレビュー版を添付。Professional版以上にはObject Pascal (Delphi) 版の[Kylix 3が付属した](../Page/Kylix.md "wikilink")。ただし、[Kylix 3は最後の](../Page/Kylix.md "wikilink")[Kylix](../Page/Kylix.md "wikilink")であり、CLXサポートもDelphi 7を最後に廃止されている。エンバカデロ・テクノロジーズによるDelphi 7の再販版が存在するが、こちらも「Borland Delphi 7」の名称を用いていた。ただし、"Studio" の文字は外された。 [Win9xで動作するDelphiとしては最終版となる](../Page/Windows_9x系.md "wikilink")。そのため、段階マイグレーションのチェックポイントとして有用であり、現在でも最新版を購入すれば「Delphi 7.1」を入手する事が可能となっている（サポートは終了している）。

### Delphi 8 for the Microsoft .NET Framework

「**Delphi 8 for the Microsoft .NET Framework**」（コードネーム: Octane）は[2003年](../Page/2003年.md "wikilink")[11月3日](https://ja.wikipedia.org/wiki/11月3日 "wikilink")に発表された。

[.NET Frameworkに対応した](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")「Delphi for the Microsoft .NET Framework (Delphi.NET)」の最初の製品だった。それ以前のDelphiの言語構文を殆ど変更する事なく[.NETアプリケーションを開発できる](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。「Galileo」と呼ばれる新しい\[10\]IDEになり、[Microsoft Visual Studioと似たユーザインタフェースや外観が導入されたが](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、品質はお世辞にも良いとは言えなかった。.NET専用という点でDelphiの系譜の中ではやや異端のバージョンである。Win32の開発の為に**Delphi 7.1**が付属した。また、DelphiのIDEはDelphi ([VCL](../Page/Visual_Component_Library.md "wikilink")) で書かれており、IDEを拡張するためのWin32コンパイラとして IDE Integration pack for Delphi 8 \[11\]が用意された。

### Delphi 2005

「**Delphi 2005**」（コードネーム: DiamondBack、内部バージョン: 9.0）は[2004年](../Page/2004年.md "wikilink")[11月4日](../Page/11月4日.md "wikilink")に発表された。

ボーランドの[C\#言語開発環境である](../Page/C_Sharp.md "wikilink")「[C\# Builder](https://ja.wikipedia.org/wiki/C_Sharp_Builder "wikilink")」とWin32開発用および.NET開発用の「Delphi for .NET」が統合された。より正確には、「Delphi 8 (Delphi for .NET)」と「C\# Builder」を統合し、そこへWin32開発用である「Delphi for Win32」を追加したものがDelphi 2005である。Delphi 2005には無償版が用意されていたが、実際に提供されたのは欧州など限られた国のみだった。この製品ではIDEが大幅に強化された。[UMLモデリング機能](../Page/統一モデリング言語.md "wikilink") (Borland Together) や[構成管理](../Page/構成管理.md "wikilink")機能 (Borland StarTeam)、[リファクタリング機能の導入などである](../Page/リファクタリング_\(プログラミング\).md "wikilink")。また言語にも`for` ... `in`構文（C\#の`foreach` に相当）や`inline`命令などが追加された。

### Delphi 2006 / Turbo Delphi

「**Borland Developer Studio 2006**」（コードネーム: DeXter）は[2005年](../Page/2005年.md "wikilink")[11月24日](../Page/11月24日.md "wikilink")に発表された。

「**Delphi 2006**」という名称の製品は単体では存在しない。他言語との統合版 (**Borland Developer Studio 2006**) と単体製品 (**Turbo Delphi**) で名称が異なっている。

「Delphi 2005」の後継製品であり、Win32開発環境として「**Delphi 2006 for Win32**」（内部バージョン: 10.0）が、.NET開発用の環境として「Delphi 2006 for .NET」と「C\# Builder」が提供された。さらにボーランドの[C++](../Page/C++.md "wikilink")言語による[VCL開発環境](../Page/Visual_Component_Library.md "wikilink") 「[C++ Builder](../Page/C++_Builder.md "wikilink")」 が統合されている。

「**Turbo Delphi**」（内部バージョン: 10.0）は[2006年](../Page/2006年.md "wikilink")[9月6日](../Page/9月6日.md "wikilink")（英語版は[8月8日](../Page/8月8日.md "wikilink")）に発表された。これは「Borland Developer Studio 2006」からWin32開発用のDelphi for Win32を単体として分離したものである。Delphi 2006 Update 2とほぼ同等の機能を持ち、エディションとしてはProfessionalに相当する。同様に「Delphi 2006 for .NET」、「[C++ Builder](../Page/C++_Builder.md "wikilink")」、「C\# Builder」も単体分離され、それぞれ 「**Turbo Delphi for .NET**」、「**Turbo C++**」、「**Turbo C\#**」の名称で同時リリースされた。無償版 (Turbo Delphi Explorer / Turbo Delphi for .NET Explorer / Turbo C++ Explorer / Turbo C\# Explorer) も提供された。Turboシリーズは他のパーソナリティ（言語）と同時にインストールする事はできず、「Borland Developer Studio 2006」とも共存できない。

FastMM相当のメモリマネージャに変更され、クラスヘルパー等の新しい言語機能も追加されている。

### Delphi 2007 / R2

[2007年](../Page/2007年.md "wikilink")[2月21日](../Page/2月21日.md "wikilink")に 「**Delphi 2007 for Win32**」（コードネーム: Spacely、内部バージョン: 11.0）が発表された。

製品名が示す通り、Win32開発用の環境である。[Windows Vistaに対応](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。

[2007年](../Page/2007年.md "wikilink")[9月6日](../Page/9月6日.md "wikilink")にはこの他に.NET開発用の「**Delphi 2007 for .NET**」を含む統合版「**CodeGear RAD Studio 2007**」（コードネーム: Highlander）が発表された。.NET 2.0に対応。なおC\# BuilderやDelphi for .NETにおけるWinformのサポートは打ち切られた。

その後、[2007年](../Page/2007年.md "wikilink")[10月10日](../Page/10月10日.md "wikilink")に「**Delphi 2007 for Win32 R2**」が発表された。これは「Delphi 2007 for Win32 (Update 3)」に、「[BlackFish SQL](https://ja.wikipedia.org/wiki/BlackFish_SQL "wikilink")（旧[JDataStore](https://ja.wikipedia.org/wiki/JDataStore "wikilink")）」を追加した物である。

内部コード体系が[Shift_JIS](../Page/Shift_JIS.md "wikilink") (ANSI) であるDelphiとしては最終版となる。旧バージョンとの互換性も高く、Windows Vista対応が可能なため、マイグレーション先としても、段階マイグレーションのチェックポイントとして有用なバージョンである。そのためか、[2017年](../Page/2017年.md "wikilink")時点においてもサポートは継続されており\[12\]、現在でも最新版を購入すれば「Delphi 2007 for Win32 (R2)」を入手する事が可能である。

### Delphi 2009

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[8月26日](../Page/8月26日.md "wikilink")に「**Delphi 2009**」（コードネーム: Tiburón、内部バージョン: 12.0）が発表された。

長年の懸案であった [VCLとRTLの](../Page/Visual_Component_Library.md "wikilink")[Unicode](../Page/Unicode.md "wikilink")化、[ジェネリクス(Win32)や](../Page/ジェネリックプログラミング.md "wikilink")[匿名メソッドの導入など](https://ja.wikipedia.org/wiki/無名関数 "wikilink")、Delphiにとって大きな転機といえるバージョンアップだった。"for Win32" の文字はないがWin32開発用である。

[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[12月2日](../Page/12月2日.md "wikilink")には.NET開発用の「**Delphi Prism**」を含む統合版「**CodeGear RAD Studio 2009**」が発表された。旧来のDelphi for .NETは廃止になっている。[Delphi Prism](https://ja.wikipedia.org/wiki/Delphi#Embarcadero_Prism "wikilink") については後述する。

### Delphi 2010

[2009年](../Page/2009年.md "wikilink")[8月25日](../Page/8月25日.md "wikilink")に「**Delphi 2010**」（コードネーム: Weaver、内部バージョン: 14.0）が発表された。内部バージョン13.0は[忌み番](https://ja.wikipedia.org/wiki/忌み番 "wikilink")のためスキップされた。

[Windows 7に正式対応](../Page/Microsoft_Windows_7.md "wikilink")。タッチインタフェースや[マウスジェスチャー](../Page/マウスジェスチャー.md "wikilink")の制作支援機能、オープンソースDBである[Firebird](../Page/Firebird.md "wikilink")のサポート、[RTTIの強化](https://ja.wikipedia.org/wiki/実行時型情報 "wikilink")、IDEの改良（言語切り替え機能、Delphi 7以前のIDEにあったコンポーネントツールバーの復活など）が盛り込まれた\[13\]。開発環境をインストールするOSとして[Windows 2000以前はサポートされなくなった](../Page/Microsoft_Windows_2000.md "wikilink")。

### Delphi XE

[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[9月2日](../Page/9月2日.md "wikilink")に「**Delphi XE**」（コードネーム: Fulcrum、内部バージョン: 15.0）が発表された。

XEは "Cross Platform Edition" の略である。名称通り[クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")開発環境を目指して開発が進められたものの、不完全であったため、クロスプラットフォーム機能の搭載は見送られている。結果、前バージョンとの機能差はあまりなくなってしまっているが、純粋なWin32アプリケーション開発環境としては最終版であるため、段階マイグレーションのためのチェックポイントとして有用である。

[2011年](../Page/2011年.md "wikilink")[2月1日](../Page/2月1日.md "wikilink")にはStarterエディションが追加発表された。「Turbo Delphi」 以来のエントリー向けエディションであり、無償ではないがコンポーネントのインストールが可能、1,000 USドルを超えない範囲であれば商用利用可能など、制限は大幅に緩和されている。ただし、Starterには旧Delphiのライセンスは付属しない。また、同時利用は同一サブネット内において5ライセンスまでとされている。このため教室での利用は向かないとされており、アカデミック版の提供はない。Starter版には通常価格とアップグレード価格が用意されているが、同社または他社の開発ツールユーザーであれば「誰でも」アップグレード版を購入できる。C++ Builder Starterとの共存はできず、[RAD StudioにもStarterは提供されない](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")。

Starter版とアカデミック版を除き、Delphi 7、2007、2009、2010のライセンスが付属する\[14\]\[15\]\[16\]。

### Delphi XE2

[2011年](../Page/2011年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")に「**Delphi XE2**」（コードネーム: Pulsar、内部バージョン: 16.0）が発表された。

新たに**FireMonkey**フレームワーク\[17\]を導入したことにより、[HDや](https://ja.wikipedia.org/wiki/ハイデフィニション "wikilink")[3Dに対応した高品質なユーザインタフェースの設計や](../Page/3次元コンピュータグラフィックス.md "wikilink")、[Windows 64bit](https://ja.wikipedia.org/wiki/Microsoft_Windows#64_.E3.83.93.E3.83.83.E3.83.88_.E3.82.AA.E3.83.9A.E3.83.AC.E3.83.BC.E3.83.86.E3.82.A3.E3.83.B3.E3.82.B0_.E3.82.B7.E3.82.B9.E3.83.86.E3.83.A0 "wikilink")、[Mac OS X](https://ja.wikipedia.org/wiki/macOS "wikilink") ([Intel x86](../Page/X86.md "wikilink"))、[iOS向けのマルチプラットフォームアプリケーションの開発が可能になった](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。但し、iOS開発は実際には[Free Pascal](../Page/Free_Pascal.md "wikilink") (FPC) を使った[ツールチェイン](https://ja.wikipedia.org/wiki/ツールチェイン "wikilink")であり、後述する[XE4以降のiOS開発環境との互換性は乏しい](https://ja.wikipedia.org/wiki/#Delphi_XE4 "wikilink")。マルチプラットフォーム化によりVCL / FMX / RTLのユニットで、System.TypesやVcl.Stylesのような、ドットで接頭辞を連結する命名規則（ユニットスコープ）を使うようになったため、以前のバージョンにソースコードを移植する場合には注意が必要である。Windows以外のアプリケーションのデバッグ及びデプロイ（配置）には新しいリモートデバッガである 「プラットフォームアシスタントサーバー (**PAServer**)」 を利用する（デバッグ対象アプリケーションがWindowsであっても、リモートにあるPCのアプリケーションをデバッグするにはやはりPAServerが必要となる）。また、製品エディションとしてEnterpriseとArchitectの間にUltimateが追加された。

搭載されるコンパイラはDCC32 (Windows 32bit), DCC64 (Windows 64bit), DCCOSX (Mac OS X) の3つとなった（ツールチェイン用のFPCを除く）。

Starterとアカデミック版を除き、Delphi 7、2007、2009、2010、XEのライセンスが付属する。

### Delphi XE3

[2012年](../Page/2012年.md "wikilink")[9月4日](../Page/9月4日.md "wikilink")に「**Delphi XE3**」（コードネーム: WaterDragon、内部バージョン: 17.0）が発表された\[18\]。

新たに「**Metropolis UI**」を導入したことにより、タッチ対応、ライブタイルサポートなどを実装した[Windows 8デスクトップアプリケーションの開発が可能になった](https://ja.wikipedia.org/wiki/Microsoft_Windows_8 "wikilink")。ただし[Windowsランタイム](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink") (WinRT) には対応しない。[OS X v10.8](https://ja.wikipedia.org/wiki/OS_X_Mountain_Lion "wikilink") (Mountain Lion) アプリケーション開発に対応。Visual LiveBindingが追加されてデータとユーザインタフェースの紐付けが容易になった。Enterprise版以上のエディションに新しいデータベースフレームワークである **FireDAC** が追加された（[SQLite](../Page/SQLite.md "wikilink") を標準サポート）。ProfessionalエディションでFireDACを利用するには、別途「**FireDAC Client/Server Add-On Pack**」を購入しなければならない。XE2にあったFPC[ツールチェイン](https://ja.wikipedia.org/wiki/ツールチェイン "wikilink")なiOS開発環境は廃止されている。開発環境をインストールするOSとしてWindows XP以前はサポートされなくなった。

Starterとアカデミック版を除き、Delphi 7、2007、2009、2010、XE、XE2のライセンスが付属する。

### Delphi XE4

[2013年](../Page/2013年.md "wikilink")[4月23日](../Page/4月23日.md "wikilink")に「**Delphi XE4**」（コードネーム: Quintessence、内部バージョン: 18.0）が発表された\[19\]。iOS開発機能が追加された。これはXE2のものとは異なり、コンパイルにFPCを必要としないが、デバッグ及びデプロイのために[OS X搭載の](https://ja.wikipedia.org/wiki/macOS "wikilink")[Intel Macが必要となる](../Page/Intel_Mac.md "wikilink")。Professional版でモバイル開発 (iOS) を行うには「**Mobile Add-On Pack**」を別途購入する必要がある。前バージョンのXE3から7ヶ月でのバージョンアップとなったため、XE3からのバージョンアップ料金はキャンペーン価格ながら格安の6,000円となった（モバイル開発環境を含まないProfessional 版の場合）。PAServer 実行環境としてのMac OS X v10.6 (Snow Leopard) はサポートされなくなった。

搭載されるコンパイラは DCC32 (Windows 32bit), DCC64 (Windows 64bit), DCCOSX (OS X), DCCIOS32（iOSシミュレータ用）, DCCIOSARM（iOSデバイス用）の5つとなった。

Starterとアカデミック版を除き、Delphi 7、2007、2009、2010、XE - XE3のライセンスが付属する。

### Delphi XE5

[2013年](../Page/2013年.md "wikilink")[9月11日](../Page/9月11日.md "wikilink")に「**Delphi XE5**」（コードネーム: Zephyr、内部バージョン: 19.0）が発表された\[20\]。

[OS X v10.9](https://ja.wikipedia.org/wiki/OS_X_Mavericks "wikilink") (Mavericks)、iOS 7アプリケーション開発に対応。[Android](../Page/Android.md "wikilink")開発機能が追加された。[Android](../Page/Android.md "wikilink")アプリケーションのデバッグにはPAServerを必要としない。原則として[ARM v7以降の](../Page/ARMアーキテクチャ.md "wikilink")[NEON対応](https://ja.wikipedia.org/wiki/ARMアーキテクチャ#Advanced_SIMD_.28NEON.29 "wikilink")[SoCを載せた端末であれば](../Page/System-on-a-chip.md "wikilink")、Delphi製アプリケーションを実行できる。モバイル開発 (iOS / Android) を行う場合、Professional版ではMobile Add-On Packを別途購入する必要がある。Professional版にもローカル接続専用ではあるがFireDACが追加された。Professional版でFireDAC（リモート接続）を使うにはFireDAC Client/Server Add-On Packを別途購入する必要がある。

搭載されるコンパイラはDCC32 (Windows 32bit), DCC64 (Windows 64bit), DCCOSX (OS X), DCCIOS32（iOSシミュレータ用）, DCCIOSARM（iOSデバイス用）, DCCAARM (Android) の6つとなった。

Starter 版を除き、Delphi 7、2007、2009、2010、XE - XE4 のライセンスが付属する。

[2014年](../Page/2014年.md "wikilink")[3月1日](../Page/3月1日.md "wikilink")に[RAD StudioのFireMonkey専用開発環境である](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")「[Appmethod](https://ja.wikipedia.org/wiki/Appmethod "wikilink")」が発表された。AppmethodにはObject Pascal (Delphi) 言語 / C++言語が含まれるが、VCLを用いたソースコードをコンパイルする事はできない。AppmethodはRAD Studio / Delphi / [C++ Builderとは異なり](../Page/C++_Builder.md "wikilink")、プラットフォーム毎 / 年のサブスクリプション契約となっている。最初のリリースである「Appmethod 1.13」はXE5相当であり、以降[RAD Studioの新版がリリースされるのとほぼ同時期にAppmethodもリリースされるようになった](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")。Appmethodは同等バージョンのRAD Studio / Delphi / [C++ Builderとは同時にインストールできない](../Page/C++_Builder.md "wikilink")。また、このAppmethodのリリースにより、ドキュメントなどで使われるDelphi の「言語の名称」が「[Object Pascal言語](../Page/Object_Pascal.md "wikilink")」と記述される事が多くなった\[21\]。

### Delphi XE6

[2014年](../Page/2014年.md "wikilink")[4月16日](../Page/4月16日.md "wikilink")に「**Delphi XE6**」（コードネーム: Proteus、内部バージョン: 20.0）が発表された\[22\]。

[Windows 8.1に対応](https://ja.wikipedia.org/wiki/Microsoft_Windows_8#Windows_8.1 "wikilink")。デザインおよびパフォーマンスを改善した「高品質リリース」。

Starter版を除き、Delphi 7、2007、2009、2010、XE - XE5のライセンスが付属する。

### Delphi XE7

[2014年](../Page/2014年.md "wikilink")[9月2日](../Page/9月2日.md "wikilink")に「**Delphi XE7**」（コードネーム: Carpathia、内部バージョン: 21.0）が発表された\[23\]。

[OS X v10.10](https://ja.wikipedia.org/wiki/OS_X_Yosemite "wikilink") (Yosemite)、iOS 8アプリケーション開発に対応、FireMonkeyに**FireUI**と呼ばれる機能が追加された。これはフォームを各デバイス向けに最適化されたユーザインタフェースにカスタマイズするものである。開発環境をインストールするOSとして[Windows Vista以前はサポートされなくなり](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、PAServer実行環境としての[Mac OS X v10.7](https://ja.wikipedia.org/wiki/Mac_OS_X_Lion "wikilink") (Lion) もサポートされなくなった。OS XおよびiOS向けアプリケーションの開発を行うのにSDKが必要となったため、コンパイルや構文チェックを行うだけでもMacの実機が必要となっている。また、このバージョン以降、BDE (Borland Database Engine) はデフォルトでインストールされなくなった。

Starter 版を除き、Delphi 7、2007、2009、2010、XE - XE6 のライセンスが付属する。

### Delphi XE8

[2015年](../Page/2015年.md "wikilink")[4月7日](../Page/4月7日.md "wikilink")に「**Delphi XE8**」（コードネーム: Elbrus、内部バージョン: 22.0）が発表された\[24\]。

作業実行支援ツール 「**Castalia**」 とパッケージマネージャ 「**GetIt**」 が統合された。にiOSデバイス用[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")コンパイラも追加され、[Android](../Page/Android.md "wikilink") 5.x (Lolipop) アプリケーション開発に対応した。但し[Android](../Page/Android.md "wikilink") 2.3x (Gingerbread) には非対応となった。

搭載されるコンパイラは DCC32 (Windows 32bit), DCC64 (Windows 64bit), DCCOSX (OS X), DCCIOS32（iOSシミュレータ用）, DCCIOSARM（iOSデバイス用）, DCCIOSARM64 （iOSデバイス用64ビット）, DCCAARM (Android) の7つとなった。

Starter版を除き、Delphi 7、2007、2009、2010、XE - XE7のライセンスが付属する。

### Delphi 10 Seattle

[2015年](../Page/2015年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")に「**Delphi 10 Seattle**」（コードネーム: Aitana、内部バージョン: 23.0）が発表された\[25\]。

[Windows 10に対応](https://ja.wikipedia.org/wiki/Microsoft_Windows_10 "wikilink")。[OS X v10.11](https://ja.wikipedia.org/wiki/OS_X_El_Capitan "wikilink") (El Capitan)、iOS 9 アプリケーション開発に対応、[Android](../Page/Android.md "wikilink")のサービスアプリケーションも作成可能となった。IDEが利用可能なメモリが倍増したため、大規模なプロジェクトをビルドしてもメモリ不足エラーが発生しにくくなっている\[26\]\[27\]。前バージョンまで続いた XE ナンバリングが廃止されている。

Starter版を除き、Delphi 7、2007、2009、2010、XE - XE8のライセンスが付属する。

### Delphi 10.1 Berlin

[2016年](../Page/2016年.md "wikilink")[4月20日](https://ja.wikipedia.org/wiki/4月20日 "wikilink")に「**Delphi 10.1 Berlin**」（コードネーム: BigBen、内部バージョン: 24.0）が発表された\[28\]。

[Android](../Page/Android.md "wikilink") 6.0、iOS 10、[macOS v10.12](https://ja.wikipedia.org/wiki/macOS_Sierra "wikilink") (Sierra) アプリケーション開発に対応。FireMonkeyのフォームデザイナも独立表示可能になった（デフォルトでは埋め込みデザイナ）。クラスヘルパーの仕様変更が行われている。インストーラの改良により、インストールオプションによってはインストール時間が大幅に短縮されるようになった。このバージョンからUltimateエディションが廃止されている。

[2016年](../Page/2016年.md "wikilink")[8月22日](../Page/8月22日.md "wikilink")以降、Starter Editionが無償で入手できるようになっている\[29\]。[2006年](../Page/2006年.md "wikilink")の**Turbo Delphi Explorer**以来、10年ぶりの無償版である。またStarter EditionはTurbo Explorerとは異なり、複数のパーソナリティ（言語）が共存できるため、Delphiと[C++ Builderを同じ環境で利用する事が可能となっている](../Page/C++_Builder.md "wikilink")。コンポーネントのインストールにも制限がない。

Starter版を除き、Delphi 7、2007、2009、2010、XE - XE8、10 Seattleのライセンスが付属する。

### Delphi 10.2 Tokyo

[2017年](../Page/2017年.md "wikilink")[3月22日](../Page/3月22日.md "wikilink")に「**Delphi 10.2 Tokyo**」（コードネーム: Godzilla、内部バージョン: 25.0）が発表された\[30\]。

Enterprise 以上の SKU に [LLVM](../Page/LLVM.md "wikilink") エンジンベースの [Linux](../Page/Linux.md "wikilink") [64ビット](../Page/X64.md "wikilink") コンパイラが追加された ([Ubuntu](../Page/Ubuntu.md "wikilink") 16.04 LTS / [RedHat Enterprise Linux](../Page/Red_Hat_Enterprise_Linux.md "wikilink") 7 対応)。また、インストーラの改良により、インストール時間が大幅に短縮されるようになった。

搭載されるコンパイラは DCC32 (Windows 32bit), DCC64 (Windows 64bit), DCCOSX (OS X), DCCIOS32（iOSシミュレータ用）, DCCIOSARM（iOSデバイス用）, DCCIOSARM64 （iOSデバイス用64ビット）, DCCAARM (Android), DCCLINUX64 (Linux 64bit) の8つとなった。

[2017年](../Page/2017年.md "wikilink")[12月13日](https://ja.wikipedia.org/wiki/12月13日 "wikilink")にリリースされた Release 2 (10.2.2) において、Enterprise 以上の SKU で **RAD Server** の単一サイト/単一サーバー配置ライセンスが含まれるようになった。

[2018年](../Page/2018年.md "wikilink")[3月14日](https://ja.wikipedia.org/wiki/3月14日 "wikilink")にリリースされた Release 3 (10.2.3) において、Professional Edition にモバイルサポートが追加された。従来、Mobile Add-On Packとして別売されていたものが統合された形になる。

[2018年](../Page/2018年.md "wikilink")[7月19日](../Page/7月19日.md "wikilink")に、従来の Professional Edition 相当を無償化した「**Delphi Community Edition**」がリリースされた。Windows 64bit, macOS, iOS, Android 向けの開発が可能となっている。無償版 Starter Edition とは異なり、「**C++Builder Community Edition**」と同時にインストールする事はできない。

Starter / Community 版を除き、Delphi 7、2007、2009、2010、XE - XE8、10 Seattle、10.1 Berlinのライセンスが付属する。

### Delphi 10.3 Rio

[2018年](../Page/2018年.md "wikilink")[11月22日](https://ja.wikipedia.org/wiki/11月22日 "wikilink")に「**Delphi 10.3 Rio**」（コードネーム: Carnival、内部バージョン: 26.0）が発表された\[31\]。同日、Community Edition も更新されている。

Starter Edition は廃止された。Professional Edition にあった別売の FireDAC Client/Server Add-on Pack も廃止され、フル機能の FireDAC を利用するためには Enterprise Edition 以上の SKU が必要となった。

型推論可能なインライン変数宣言が行えるようになっており、

``` pascal
procedure Test;
var
  i: Integer;
begin
  for i := 1 to 100 do
    writeln(i);
end;
```

従来このような記述をしなければならなかったものが、

``` pascal
procedure Test;
begin
  for var i := 1 to 100 do
    writeln(i);
end;
```

このように var ブロックを使わずにシンプルに書けるようになった。

Linux コンパイラ (DCCLINUX64) では ARC (自動参照カウント) が廃止され、AnsiString / AnsiChar がサポートされるようになった。

[2019年](../Page/2019年.md "wikilink")[7月19日](../Page/7月19日.md "wikilink")にリリースされた Release 2 (10.3.2) において、LLVM エンジンベースの macOS 用 64bit コンパイラが追加された。また、Enterprise 以上の SKU で、Linuxデスクトップアプリを FireMonkey GUI で開発可能になる **FMX Linux** がバンドルされるようになった。

[2019年](../Page/2019年.md "wikilink")[11月21日](../Page/11月21日.md "wikilink")にリリースされた Release 3 (10.3.3) において、LLVM エンジンベースの Android 用 64bit コンパイラが追加された。また、Enterprise 以上の SKU で、データベース接続と同じように多様なエンタープライズアプリケーションに接続可能となる **Enterprise Connectors** がバンドルされるようになった。

搭載されるコンパイラは DCC32 (Windows 32bit), DCC64 (Windows 64bit), DCCOSX (macOS 32bit), DCCOSX64 (macOS 64bit), DCCIOS32（iOSシミュレータ用）, DCCIOSARM（iOSデバイス用）, DCCIOSARM64 （iOSデバイス用64ビット）, DCCAARM (Android), DCCAARM64 (Android 64bit), DCCLINUX64 (Linux 64bit) の10種類となった。

Community 版を除き、Delphi 7、2007、2009、2010、XE - XE8、10 - 10.2 のライセンスが付属する。

### 今後のDelphi

今後 [iOS](https://ja.wikipedia.org/wiki/iOS "wikilink") 13 以降用の [iOS](https://ja.wikipedia.org/wiki/iOS "wikilink") シミュレータ用 コンパイラの追加を盛り込む予定であると、[2019年](../Page/2019年.md "wikilink")のロードマップにてアナウンスされている\[32\]。

## Delphi Community Edition

10.2 Tokyo より完全無料版の **Community Edition**\[33\] が提供されている。有料の Delphi Professional と同等の機能を持ち、従来の Win32 アプリケーションのみならず Windows 64bit, macOS, iOS, Android の開発が可能となっている。

また、[2020年](../Page/2020年.md "wikilink")[2月15日](../Page/2月15日.md "wikilink")に **Delphi 1.0 Client/Server (英語版)**\[34\] がアンティークソフトウェアとして無償公開された。

### 過去の無料版

  - Delphi 6 では Personal 版が無料で提供されていた。
  - Delphi 2006 Update2 相当の Turbo Delphi for Win32 Explorer / Turbo Delphi for .NET Explorer が無料で提供されていた。
  - Delphi 10.1 Berlin から Starter Edition が無料で提供されていた。
  - Delphi 10.2 Tokyo から Community Edition が無料で提供されている。

## Delphi用コンポーネント

DelphiのVCL / CLX / FMXは、コンポーネントと呼ばれるソフトウェア部品の集合で構成され、プログラマはこのコンポーネントを組み合わせて視覚的にアプリケーションを開発する方式となっているが、ユーザープログラマがコンポーネントを自由に作成して開発環境自体に組み込み、開発環境を拡張することが可能となっている。

多くの有償／無償のコンポーネントが作成・公開され、開発環境を容易に拡張できるシステムはユーザープログラマからの支持も高いが、Delphiのバージョン毎に互換性が無い場合も多く、コンポーネントのソースコードが公開されている場合は使用している Delphiのバージョンに合わせて自分でコンポーネントのコードを修正する必要がある。

## Delphiで開発されたアプリケーション

有償 / 無償の製品、[シェアウェア](../Page/シェアウェア.md "wikilink")、[フリーウェア](../Page/フリーウェア.md "wikilink")が多数作成されている\[35\]\[36\]\[37\]。Delphi 自身も Delphi によって作られている。

  - [バンクーバー冬季五輪のリング](https://ja.wikipedia.org/wiki/バンクーバーオリンピック "wikilink")[LEDはDelphiで制御されている](../Page/発光ダイオード.md "wikilink")\[38\]。
  - [欧州宇宙機関](../Page/欧州宇宙機関.md "wikilink") (ESA) の彗星探査機「[ロゼッタ](../Page/ロゼッタ_\(探査機\).md "wikilink")」のシミュレータ等はDelphiで作られている\[39\]。
  - [ミニチュアワンダーランド](../Page/ミニチュアワンダーランド.md "wikilink")はDelphiで制御されている\[40\]。

かつてボーランドから提供されていたVCL Scannerというツールを使うと、Delphiまたは[C++ Builderで作成されたアプリケーションを調べることができた](../Page/C++_Builder.md "wikilink")。現在では実行ファイルをダウンロードできないが、[Delphi 5](https://ja.wikipedia.org/wiki/Delphi#Delphi_1_.E3.81.8B.E3.82.89_5_.E3.81.BE.E3.81.A7 "wikilink") でコンパイル可能なソースコードが公開されている\[41\]ため、自前で実行ファイルを生成する事ができる。

## Embarcadero Prism

**Embarcadero Prism**（**エンバカデロ プリズム**）は、[エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")が販売する.NET向けの新たなIDEである。以前は**Delphi Prism**と呼ばれていたが、XE2より名称からDelphiが外れEmbarcadero Prismとなった。

Delphi 8以降、Delphiの.NET開発用の環境 (Delphi for .NET) はWin32版のVCLと互換性を持つフレームワークVCL.NETと、[マイクロソフト](../Page/マイクロソフト.md "wikilink")のフレームワーク[Windows Formsの両方をサポートしていたが](../Page/Windows_Forms.md "wikilink")、流石に無理があったのかDelphi 2007ではWindows Formsのサポートが打ち切られた。

Delphi 2009よりエンバカデロ・テクノロジーズは方針転換を行い、Delphi for .NET (Delphi.NET) を置き換える決定を下した。こうして生まれたPrismは当初Delphiの名を冠してはいたものの、実際は[Rem Objectsの言語コンパイラ](https://ja.wikipedia.org/wiki/Rem_Objects "wikilink")[Oxygene](https://ja.wikipedia.org/wiki/Oxygene "wikilink") (以前はChromeと呼ばれていた) とマイクロソフトのIDEを使用する全く新しい製品である。PrismではVCL.NETはサポートされず、フレームワークのサポートはWindows Formsのみとなっている。

Delphi for Win32 (Delphi Win32) とは異なり、Prismは更新が頻繁に行われる。単体製品版には初年度分の年間メンテナンス & サポートが付属しており、翌年度以降も契約更新が可能で、この契約期間中であればいつでも最新版を入手することができる。このため、バージョンアップ版の設定がない。また、一度契約が切れてしまうと新規での製品購入が必要である。さらにRAD Studio版には初年度分の年間メンテナンス & サポートも付属していないため、購入年度から加入していないとメンテナンスリリースを入手できないので注意が必要である。

Embarcadero Prism は XE3 (XE3.2) が最終バージョンとなり、[RAD Studio](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink") XE4 以降に含まれず、スタンドアロン製品としても提供されなくなった。サポートとメンテナンスのアップデートも2013年8月で終了している。エンバカデロ・テクノロジーズは、今後のPrismの最新版は[Rem Objectsから購入するようにアナウンスしている](https://ja.wikipedia.org/wiki/Rem_Objects "wikilink")\[42\]。なおRem ObjectsはPrismの名称を用いず、[Oxygene](https://ja.wikipedia.org/wiki/Oxygene "wikilink")とする方針を打ち出している\[43\]。

### 互換性

  - Delphi for .NET (Delphi.NET) との互換性
    PrismとDelphi for .NET のどちらも.NET開発環境ではあるが、VCL.NETを利用したDelphi for .NETのコードとはフレームワークとしての互換性がない。
  - Delphi for Win32 (Delphi Win32) との互換性
    PrismにはDelphi for Win32とある程度の互換性を保つためのオプションが存在するものの、ほぼ互換性がない。「**Oxidizer**」と呼ばれる[Rem Objects製のコードコンバーターがあり](https://ja.wikipedia.org/wiki/Rem_Objects "wikilink")\[44\]、Delphi for Win32のコードをPrismへコンバートする事ができる。

### 主要バージョン

これらの他、メンテナンスリリースが存在する。

「**Delphi Prism 2009**」 は[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")[12月2日](../Page/12月2日.md "wikilink")に発表された。Prismの最初のバージョン。

「**Delphi Prism 2010**」 は[2009年](../Page/2009年.md "wikilink")[8月25日](../Page/8月25日.md "wikilink")に発表された。クロスプラットフォーム開発機能により、Linux用のアプリケーション開発をサポート。

「**Delphi Prism 2011**」 は[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[6月3日](../Page/6月3日.md "wikilink")に発表された。クロスプラットフォーム開発機能がさらに拡張され、Mac OS X、iOS向けのアプリケーション開発をサポート。

「**Delphi Prism XE**」 は[2010年](https://ja.wikipedia.org/wiki/2010年 "wikilink")[9月2日](../Page/9月2日.md "wikilink")に発表された。Delphi Prism 2009、2010、2011 のライセンスが付属する\[45\]\[46\]\[47\]。

「**Embacadero Prism XE2**」 は[2011年](../Page/2011年.md "wikilink")[9月1日](../Page/9月1日.md "wikilink")に発表された。Delphi Prism 2009、2010、2011、XEのライセンスが付属する。

「**Embacadero Prism XE3**」 は[2012年](../Page/2012年.md "wikilink")[9月4日](../Page/9月4日.md "wikilink")に「Embarcadero RAD Studio XE3」の一部として発表された。Delphi / Embacadero Prism 2009、2010、2011、XE、XE2のライセンスが付属する。最後のメジャーリリースとなった。

## 脚注

<references />

## 関連項目

  - [Appmethod](https://ja.wikipedia.org/wiki/Appmethod "wikilink")
  - [C\#](../Page/C_Sharp.md "wikilink")
  - [C++ Builder](../Page/C++_Builder.md "wikilink")
  - [Free Pascal](../Page/Free_Pascal.md "wikilink")
  - [Kylix](../Page/Kylix.md "wikilink")
  - [Object Pascal](../Page/Object_Pascal.md "wikilink")
  - [Pascal](../Page/Pascal.md "wikilink")
  - [Rapid Application Development](../Page/Rapid_Application_Development.md "wikilink")
  - [RAD Studio](https://ja.wikipedia.org/wiki/RAD_Studio "wikilink")
  - [Turbo C](https://ja.wikipedia.org/wiki/Turbo_C "wikilink")
  - [Turbo Pascal](../Page/Turbo_Pascal.md "wikilink")
  - [アンダース・ヘルスバーグ](../Page/アンダース・ヘルスバーグ.md "wikilink")
  - [エンバカデロ・テクノロジーズ](https://ja.wikipedia.org/wiki/エンバカデロ・テクノロジーズ "wikilink")
  - [コードギア](../Page/コードギア.md "wikilink")
  - [ボーランド](../Page/ボーランド.md "wikilink")

## 外部リンク

  - [Embarcadero Technologies](http://www.embarcadero.com/jp/)
  - [Delphi](http://www.embarcadero.com/jp/products/delphi) 公式サイト
  - [RAD Studio DocWiki](http://docwiki.embarcadero.com/RADStudio/ja/) RAD Studio のオンライン ヘルプ
  - [RemObjects Software Oxygene](https://www.elementscompiler.com/elements/oxygene/)
  - [Delphi Basics](http://www.delphibasics.co.uk/index.html) Help and reference for the fundamentals of the Delphi

[Category:Pascal](https://ja.wikipedia.org/wiki/Category:Pascal "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:コードギアの開発ツール](https://ja.wikipedia.org/wiki/Category:コードギアの開発ツール "wikilink") [Category:1995年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1995年のソフトウェア "wikilink")

1.  [エンバカデロ＋アイデラの件](http://blogs.itmedia.co.jp/barbaro/2015/11/post_5425.html)
2.  <http://dn.embarcadero.com/jp/article/27281>
3.  <http://patft.uspto.gov/netacgi/nph-Parser?Sect1=PTO1&Sect2=HITOFF&d=PALL&p=1&u=%2Fnetahtml%2FPTO%2Fsrchnum.htm&r=1&f=G&l=50&s1=6,185,728.PN.&OS=PN/6,185,728&RS=PN/6,185,728>
4.
5.
6.
7.
8.
9.
10. あくまで「Delphi にとっては」であり、同社の製品である[C\# Builderが先に採用している](https://ja.wikipedia.org/wiki/C_Sharrp_Builder "wikilink")。
11. <http://cc.embarcadero.com/item/21333>
12. <http://support.embarcadero.com/article/37740>
13.
14. アップグレードした場合、元のバージョンと同じバージョンのライセンスの重複取得はできない。
15. 旧バージョンライセンスの取得は、購入180日以内に行う必要がある。
16. アカデミック版以外のRAD Studioでは、Delphi、Delphi Prismに含まれる旧バージョンライセンスの他、C++ Builder 6、2007、2009、2010 のライセンスも含まれる。
17. ちなみにFireMonkeyという名前は[2016年](../Page/2016年.md "wikilink")の[丙申 (ひのえさる)に由来している](../Page/丙申.md "wikilink")。
18.
19.
20.
21. <http://www.publickey1.jp/blog/15/delphi20delphiobject_pascal.html>
22.
23.
24.
25.
26. <http://docwiki.embarcadero.com/RADStudio/Seattle/ja/%E6%96%B0%E6%A9%9F%E8%83%BD#IDE>
27. <http://support.embarcadero.com/jp/article/44280>
28.
29.
30.
31.
32. <https://community.idera.com/developer-tools/b/blog/posts/august-2019-delphi-android-beta-plans-august-roadmap-update>
33.
34.
35. <https://www.embarcadero.com/jp/our-customers/case-studies>
36. <https://jonlennartaasenden.wordpress.com/2014/11/06/famous-software-made-with-delphi/>
37. <http://delphi.wikia.com/wiki/Good_Quality_Applications_Built_With_Delphi>
38. <http://blog.marcocantu.com/blog/olympic_rings_delphi.html>
39. <https://community.embarcadero.com/blogs/entry/delphi-s-involvement-with-the-esa-rosetta-comet-spacecraft-project-1>
40. <https://www.embarcadero.com/jp/case-study/miniatur-wunderland-case-study>
41. <http://cc.embarcadero.com/item/23078>
42. [RAD Studio XE4 Q\&A](http://www.embarcadero.com/jp/products/rad-studio/faq) - 「旧バージョンに含まれていて RAD Studio XE4 には含まれていない製品はありますか？」参照。
43. [From Prism to Oxygene](http://www.remobjects.com/oxygene/prism.aspx)
44. <http://docs.elementscompiler.com/Tools/Oxidizer/>
45.
46.
47.