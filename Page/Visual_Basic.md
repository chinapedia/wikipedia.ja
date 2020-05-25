> この記事は[Visual Basic](https://ja.wikipedia.org/wiki/Visual_Basic)から翻訳されています。


**Visual Basic** （ヴィジュアル ベーシック）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が1990年代に開発していたプログラミング言語およびその処理系。通常はVisual Basicまたは**VB**と呼ぶ。[Visual Studioに組み込まれ](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink")、さまざまな種類のアプリケーション開発に用いられる。後継となる[Visual Basic .NET](../Page/Visual_Basic_.NET.md "wikilink") (VB.NET) に関しては当該項目を参照。1970年代〜1980年代に開発されていた前身の[Microsoft BASICについては当該項目を参照](../Page/Microsoft_BASIC.md "wikilink")。アプリケーション組み込み用の言語[Visual Basic for Applicationsに関しては当該項目を参照](../Page/Visual_Basic_for_Applications.md "wikilink")。

なお、マイクロソフトのドキュメントでは、バージョン2005以降のVisual Basic .NETを**Visual Basic**と呼んでいるが、本記事では.NET非対応のVisual Basicのみを取り扱う。

## 言語の特徴

は[BASIC](../Page/BASIC.md "wikilink")から派生したマイクロソフトの[QuickBASIC](../Page/QuickBASIC.md "wikilink")を拡張したもので、[RADに対応した](https://ja.wikipedia.org/wiki/RAD_\(計算機プログラミング環境\) "wikilink")[統合開発環境](../Page/統合開発環境.md "wikilink")の名称でもあった。

もともとが初心者用言語の[BASIC](../Page/BASIC.md "wikilink")から派生しているという来歴から、が、実際にはさまざまなビジネスシーンで活用されている。

[Microsoft Windows用の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[GUI](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")[アプリケーションを開発する場合](../Page/アプリケーションソフトウェア.md "wikilink")、もっとも原始的な方法として[C](../Page/C言語.md "wikilink")/[C++](../Page/C++.md "wikilink")言語で[Win32 APIを使い](../Page/Windows_API.md "wikilink")、コードベースですべてのGUI処理を記述していく方法がある。この方法はWindowsのすべての機能にアクセスでき、すべてを制御することができることがメリットだが、その代わりコード記述量は膨大なものとなり、開発効率が悪い（[Microsoft Visual C++ではリソースエディタと呼ばれる](../Page/Microsoft_Visual_C++.md "wikilink")、GUIの外観デザインを視覚的に設定できるツールも存在するが、これはRADではない）。

VBでは[フォーム](https://ja.wikipedia.org/wiki/フォーム "wikilink")上に、あらかじめ用意された各種のGUIパーツ（[コントロール](../Page/ウィジェット_\(GUI\).md "wikilink")）を配置して、それらの[プロパティ](../Page/プロパティ.md "wikilink")が変更されたり、[マウスでクリックされたりするなど](../Page/マウス_\(コンピュータ\).md "wikilink")[イベントが発生した場合の処理を記述していくことで](../Page/イベント_\(プログラミング\).md "wikilink")[プログラムを作成していくスタイル](../Page/プログラム_\(コンピュータ\).md "wikilink")（[Rapid Application Development](../Page/Rapid_Application_Development.md "wikilink"), RAD）が特徴だったが、現在では多くのGUIアプリケーション開発環境においてこのようなスタイルでのプログラミングが可能であり、VBはその嚆矢であったことになる。グラフィックの描画など、GUIを実現するときに付随する定型的な画面管理はパーツの内部で行なわれるため、[プログラマ](../Page/プログラマ.md "wikilink")が直接記述する必要性が大幅に低減され、記述が煩雑になりがちなGUIを利用したプログラムを、簡単かつ効率的に作成することができる。

バージョン1.0ではWindows版の後に[MS-DOS](../Page/MS-DOS.md "wikilink")版が発売されており、キャラクタベースにもかかわらずコントロールを配置してGUIを構築することができた。ただしキャラクタベースであるため、フォームを使用した場合、グラフィックスの描画は不可能である。

言語仕様は、旧来のBASIC言語に比べ、[構造化プログラミング](../Page/構造化プログラミング.md "wikilink")の機能が加えられるなど大きく拡張されており、加えて[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")に近い概念も取り入れられている。VB4で[クラスモジュール機構が導入された](../Page/クラス_\(コンピュータ\).md "wikilink")。VB5で[インターフェイスの実装](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink") (Implements) を利用した[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")が導入された\[1\]。ただしバージョン6.0時点では、[C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")といった言語と比較して、オブジェクト指向プログラミングのための機能が十分には実装されておらず、特にクラスの[継承](../Page/継承_\(プログラミング\).md "wikilink")（実装継承）に相当する機能がなかった。なお、後継のVB.NETでは完全な[クラスベース](../Page/クラスベース.md "wikilink")のオブジェクト指向の機能や、[Visual C\#と遜色のないソリューション](../Page/Microsoft_Visual_C_Sharp.md "wikilink")・プロジェクト管理機能も実装されている。

## DirectXのサポート

マルチメディアコンポーネントである[Microsoft DirectXに関しては](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、一部のバージョンのみVisual Basic上からでも利用が可能となっている。Visual Basic 6.0ではVB用の[COMタイプ](../Page/Component_Object_Model.md "wikilink") ライブラリを使用することでDirectX 7およびDirectX 8を利用できる\[2\]\[3\]。 しかし、これらのVB向けDirectX[インターフェイスは](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")、[Windows Vista以降ではサポートされていない](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")\[4\]。

## 歴史

Visual Basicには、大きく分けて2種類ある。1つはバージョン1.0から6.0までの旧来版、もう1つはバージョン 7.0 (2002) 以降の[.NET Framework対応版である](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。.NET Frameworkに対応したバージョン7.0以降はバージョン6.0以前と比較して大きな変更が施され、互換性もない。

<table>
<caption>バージョンの履歴</caption>
<thead>
<tr class="header">
<th><p>製品名</p></th>
<th></th>
<th></th>
<th></th>
<th><p>備考</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Visual Basic 1.0</p></td>
<td><p>1.0</p></td>
<td><p>VBRUN100.DLL</p></td>
<td><p>1991年</p></td>
<td><p>オブジェクト指向の基本的な部分を実装。日本では発売されなかった。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>1.0</p></td>
<td><p>-</p></td>
<td></td>
<td><p>Windows版との互換性は低いが、DOS版QuickBASICの後継バージョンとして使える。PC-98用の日本語版も発売されていた。</p></td>
</tr>
<tr class="odd">
<td><p>Visual Basic 2.0</p></td>
<td><p>2.0</p></td>
<td><p>VBRUN200.DLL (英語版)<br />
VBRJP200.DLL (日本語版)</p></td>
<td><p>1992年</p></td>
<td><p>OLE, ODBC対応。日本語版は1993年で当初はODBC対応はなし。</p></td>
</tr>
<tr class="even">
<td><p>Visual Basic 3.0</p></td>
<td><p>3.0</p></td>
<td><p>VBRUN300.DLL</p></td>
<td><p>1993年</p></td>
<td><p>日本では発売されなかった。</p></td>
</tr>
<tr class="odd">
<td><p>Visual Basic 4.0</p></td>
<td><p>4.0</p></td>
<td><p>VBRUN400.DLL</p></td>
<td><p>1995年</p></td>
<td><p>32 ビット版と 16 ビット版がある。</p></td>
</tr>
<tr class="even">
<td><p>Visual Basic 5.0 CCE</p></td>
<td><p>5.0</p></td>
<td><p>-</p></td>
<td><p>1997年</p></td>
<td><p>ActiveXコントロール作成専用。フリー。Visual Basic 5.0のプロトタイプ。</p></td>
</tr>
<tr class="odd">
<td><p>Visual Basic 5.0</p></td>
<td><p>5.0</p></td>
<td><p>MSVBVM50.DLL</p></td>
<td><p>1997年</p></td>
<td><p>Win32 ネイティブコードへのコンパイル機能をサポート。</p></td>
</tr>
<tr class="even">
<td><p>Visual Basic 6.0</p></td>
<td><p>6.0</p></td>
<td><p>MSVBVM60.DLL</p></td>
<td><p>1998年</p></td>
<td><p>旧来型 Visual Basic (Win32 ネイティブ) の最後のバージョン。</p></td>
</tr>
</tbody>
</table>

### Visual Basic 4.0

32 ビット版と 16 ビット版の Windows プログラムを開発できる最初のバージョンとなった。爆発的に普及が始まった[Windows 95用のアプリケーション開発環境の一つとしてリリースされた](../Page/Microsoft_Windows_95.md "wikilink")。ボタンや[コンボボックス](https://ja.wikipedia.org/wiki/コンボボックス "wikilink")のような標準コントロールに加え、[サードパーティー](../Page/サードパーティー.md "wikilink")から発売されたコントロールをマウスを使ったGUI操作で配置することでアプリケーション画面を作成することができ、プログラム生産性が高いことが特徴だった。特に、サードパーティ製の高機能なコンポーネントが多く発売され、熟練開発者でなくとも操作性の高いアプリケーションが開発でき、当時の[エンドユーザー・コンピューティング](../Page/エンドユーザー・コンピューティング.md "wikilink")に大きな影響を与えた。VB4 の言語仕様が Office 95 の VBA に切り出され、Word VBA、Excel VBA、Access VBA の仕様とも融合した。

技術面で見ると、前のバージョンまではVBXコントロールを使っていたが、このバージョンから[Visual C++などを用いて](../Page/Microsoft_Visual_C++.md "wikilink")[COMのコントロール](../Page/Component_Object_Model.md "wikilink")（[OLEコントロール](../Page/Object_Linking_and_Embedding.md "wikilink")、OCX、後にActiveXコントロールと呼ばれる）を開発し、これらの部品群の組み立てをVisual Basicで行うことが容易にできた。特に[ExcelなどのアプリケーションをOLEを通じて制御することができるため](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、帳票を扱うような業務アプリケーション開発の分野で使われることも多かった。

### Visual Basic 5.0

Win32 ネイティブコードへのコンパイル機能がサポートされるようになり、実行速度が大幅に向上した。 開発環境内でのインタプリタ実行も引き続きサポート。

### Visual Basic 6.0

ActiveXに完全に対応し、ActiveXオブジェクトを使用することはもちろん作成することも可能。そのため、ActiveXコンポーネントとして公開されていた[DAOや](https://ja.wikipedia.org/wiki/Data_Access_Objects "wikilink")[ADO](https://ja.wikipedia.org/wiki/ActiveX_Data_Objects "wikilink")、[oo4o](https://ja.wikipedia.org/wiki/oo4o "wikilink")などを使用して、[SQL Serverや](https://ja.wikipedia.org/wiki/Microsoft_SQL_Server "wikilink")[Oracle DBを制御することができ](../Page/Oracle_Database.md "wikilink")、多くのビジネスシーンで使用された。また、バージョン1.0からの経験も蓄積されていたためVisual Basic 6.0を扱えるプログラマ・情報量ともに豊富だった。

[Webアプリケーション](https://ja.wikipedia.org/wiki/Webアプリケーション "wikilink")を開発するための方法（[IISによるサーバーサイドVBの実行](../Page/Internet_Information_Services.md "wikilink")、VBフォームへのWeb機能組み込み、[Internet ExplorerでのVBホスティング](../Page/Internet_Explorer.md "wikilink")）がいくつか用意されていた\[5\]。

## 派生言語

### Visual Basic for Applications (VBA)

[Microsoft Officeのアプリケーション用のマクロ環境として実装されているVisual](../Page/Microsoft_Office.md "wikilink") Basic。反復操作を自動化するだけでなく、Windowsのフォームやボタンなどのコントロールをドキュメント内に配置して、ドキュメント編集のためのGUIを構築することも可能となっている。言語仕様としては、本家のVisual Basicで.NET以降がリリースされたのちも、ドキュメントの互換性を保つ目的で、Visual Basic 6.0ベースのものが実装されている。[Excelや](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")[Access](../Page/Microsoft_Access.md "wikilink")、[Wordなどのアプリケーションで実装されているほか](../Page/Microsoft_Word.md "wikilink")、独自に開発したアプリケーションにVBAを搭載することも可能で、サードパーティ製のアプリケーションにVBAが搭載される場合もある。本家Visual Basicとの大きな違いは、搭載アプリケーション内でしか実行できない点にある。

VBAを用いることで、対応するアプリケーション内の各要素をクラスオブジェクトとして操作できる。Excelを例にとると、「Excelアプリケーション」を表す`Application`オブジェクト、「Excelブック」を表す`Workbook`オブジェクト、「スプレッドシート中のセルまたはセル範囲」を表す`Range`オブジェクトなどがVBAから操作できる。

Office 2007まではバージョン6系列のVisual Basicが採用されていたが、Office 2010では、バージョン番号を7.0としている\[6\]。主な変更点として、[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")環境への対応が挙げられる。`LongPtr`（32ビット環境・64ビット環境双方でポインタと同じ大きさとなる整数型）、`LongLong`（64ビット整数型、ただし64ビット環境でのみ使用可能）などのデータ型やそれに伴う変換関数の追加などが行なわれている。

### VBScript (Visual Basic Scripting Edition)

[Active Server Pages](../Page/Active_Server_Pages.md "wikilink") (ASP)の既定の言語であり、[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")スクリプティングやクライアント側の[ウェブページ](../Page/ウェブページ.md "wikilink")スクリプティングでも利用される。文法はVBに似ているがVBランタイムではなくvbscript.dllで実行される別の言語である。ASPおよびVBScriptは、[.NET Frameworkを使った](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")[ASP.NET](../Page/ASP.NET.md "wikilink")とはまた別物である。

### Visual Basic .NET

Visual Basic 6.0の後継言語であり、[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")プラットフォームの一部である。Visual Basic .NETは.NET Frameworkを使ってコンパイルされ実行される。Visual Basic 6.0と[後方互換性](https://ja.wikipedia.org/wiki/後方互換性 "wikilink")はない。自動移行ツールも用意されているが手動での手直しも必要となる。

### Visual Studio マクロ

[Microsoft Visual Studioでは](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")、繰り返し発生する操作を自動化するために、Visual Basic言語によるIDEマクロ環境が用意されている。前述のVBAとは異なり、Visual Studioのバージョンに応じたVisual Basicが使用できるようになっており、Visual Studio .NET以降はVB.NETを使って.NET Frameworkを利用できるようになっている。なお、各マクロプロジェクトは、テキストファイルのソースコードではなく、.vsmacrosファイルに[メタデータ](../Page/メタデータ.md "wikilink")としてバイナリ形式で保存されるようになっているが、各モジュールをVBのソースファイル (.vb) としてエクスポートあるいはインポートすることもできる。公式のマクロ機能はVisual Studio 2010までの提供となり、2012では廃止された。

## パフォーマンス等の課題

Visual Basic 5 以前のバージョンでは、[Pコード](https://ja.wikipedia.org/wiki/Pコード "wikilink")へのコンパイルのみをサポートしていた。Pコードは言語ランタイムによって解釈される。Pコードのメリットは、ポータビリティと小さなバイナリサイズであるが、実行時に解釈するレイヤーが追加になるため実行速度が遅くなる。Visual Basicアプリケーションの実行にはMicrosoft Visual Basicランタイム (MSVBVMxx.DLL) が必要であり、xx は50、60などのバージョン番号が入る。MSVBVM60.dllはWindows 98からWindows 7までのバージョンのWindowsのすべてのエディション (一部の Windows 7のエディションを除く) で標準コンポーネントとしてインストールされていた。Windows 95マシンはプログラムが必要としているDLLをインストーラで配布する必要があった。作成したアプリケーションのパッケージにランタイムを同梱して配布することがマイクロソフトにより認められている。Visual Basic 5 と 6 はコードを Win32 ネイティブとPコードのどちらにでもコンパイルできたが、いずれにせよビルトインの関数やフォームの利用にランタイムを必要とした。

VB.NET 以前のVisual Basicでは以下の不都合が指摘されていた。

  - コンポーネントのバージョンの違いからトラブルが起きやすい（[DLL地獄](../Page/DLL地獄.md "wikilink")）。
  - 言語仕様が完全な[オブジェクト指向言語](https://ja.wikipedia.org/wiki/オブジェクト指向言語 "wikilink")ではない\[7\]。
  - 基本的に[マルチスレッド機能が無く](../Page/スレッド_\(コンピュータ\).md "wikilink")、[ActiveX](../Page/ActiveX.md "wikilink") EXEでのみ可能である。
  - [強い型付け](https://ja.wikipedia.org/wiki/強い型付け "wikilink")のプログラミング言語と比べると、バリアント型は遅くメモリ容量もより消費する。
  - 複雑で壊れやすい[Component Object Model](../Page/Component_Object_Model.md "wikilink") (COM) のレジストリに依存したり、VBランタイムが別途必要となるなど、アプリケーションの[インストール](../Page/インストール.md "wikilink")に手間がかかる\[8\]。

## サポート期限

### 開発環境

旧来型Visual Basicの最終バージョンであるVisual Basic 6.0は、2004年3月29日にService Pack 6がリリースされたのち、2005年3月31日にメインストリームサポート期間を終え、2008年4月8日に延長サポートの期間を終えた\[9\]。したがって現在は開発環境のサポートを打ち切られている状態にある。

Visual Studio .NET 2003以前のIDE製品は、[Windows Vistaおよび](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[Windows Server 2008上での実行サポートが打ち切られたが](../Page/Microsoft_Windows_Server_2008.md "wikilink")、Visual Basicに関しては後継のVB.NET以降との互換性がほとんどなく、他開発環境への移行も難しいことから、マイクロソフトは例外的に32bit版のWindows VistaおよびWindows Server 2008でのVisual Basic 6.0のIDE実行（開発環境の実行）をサポートしている\[10\]。ただし、64bit環境でのIDE実行はサポートされない。また、[Windows 7および](../Page/Microsoft_Windows_7.md "wikilink")[Windows Server 2008 R2以降では開発環境の実行サポートも打ち切られている](https://ja.wikipedia.org/wiki/Windows_Server_2008_R2 "wikilink")（ただしマイクロソフトによると、Windows 7や[Windows 8においてVisual](https://ja.wikipedia.org/wiki/Windows_8 "wikilink") Basic 6.0 IDEをテストし、アプリケーションの互換性に深刻な不具合がないかどうかを確認して、必要に応じて不具合の軽減措置を取ったとされている）。

### 実行環境

Visual Basic 6.0で作成された[アプリケーションや](../Page/アプリケーションソフトウェア.md "wikilink")、OSに同梱されるVB6ランタイムについては、[Windows 7以降および](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")[Windows Server 2008以降での動作サポートが継続されている](https://ja.wikipedia.org/wiki/Windows_Server_2008 "wikilink")\[11\]\[12\]。64bit OS上では[WOW64](../Page/WOW64.md "wikilink")により動作する。

## コード例

``` vb
Private Sub Command1_Click()
    MsgBox "Hello, World"
End Sub
```

上記は[コマンドボタン](../Page/ボタン_\(GUI\).md "wikilink")"Command1"に関連付けられている[イベントハンドラーの例である](../Page/イベント_\(プログラミング\).md "wikilink")。対応するコマンドボタンをクリックすると、[メッセージボックス](https://ja.wikipedia.org/wiki/メッセージボックス "wikilink")に「Hello, World」と表示される。

## 脚注

## 関連項目

  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
  - [Visual Basic .NET](../Page/Visual_Basic_.NET.md "wikilink")
  - [Visual Basic for Applications](../Page/Visual_Basic_for_Applications.md "wikilink")
  - [Twip](../Page/Twip.md "wikilink")
  - [Remote Data Objects](https://ja.wikipedia.org/wiki/Remote_Data_Objects "wikilink") (RDO)
  - [Gambas](https://ja.wikipedia.org/wiki/Gambas "wikilink")
  - [Delphi](../Page/Delphi.md "wikilink")

[Category:BASICインタプリタ](https://ja.wikipedia.org/wiki/Category:BASICインタプリタ "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:Microsoft_Visual_Studio](https://ja.wikipedia.org/wiki/Category:Microsoft_Visual_Studio "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.  [VB Visual Basicの新機能の歴史1](http://rucio.a.la9.jp/VBTopics/VBVersions1.htm)
2.  \[<https://docs.microsoft.com/ja-jp/previous-versions/technical-document/dd148667(v=msdn.10>) Visual Basic で DirectX を使おう | Microsoft Docs\]
3.  \[<https://docs.microsoft.com/ja-jp/previous-versions/direct-x/cc351143(v=msdn.10>) MSDN Online - DirectX Developer Center - DirectX for Visual Basic | Microsoft Docs\]
4.  [DirectX Frequently Asked Questions - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/DxTechArts/directx-9-frequently-asked-questions)
5.  \[<https://docs.microsoft.com/ja-jp/previous-versions/cc482737(v=msdn.10>) Visual Basic 6.0のWebツール | Microsoft Docs\]
6.  \[<https://docs.microsoft.com/en-us/previous-versions/office/developer/office-2010/ee691831(v=office.14>) Compatibility Between the 32-bit and 64-bit Versions of Office 2010 | Microsoft Docs\]
7.
8.
9.  \[<https://docs.microsoft.com/ja-jp/previous-versions/cc707266(v=msdn.10>) Visual Basic 6.0 ファミリ製品のライフ サイクル ガイドライン | Microsoft Docs\]
10. [\[Visual Studio](https://blogs.technet.microsoft.com/mssvrpmj/2018/11/20/vs_osall/) 開発ツール対応 OS 一覧 – Cloud and Server Product Japan Blog\]
11. [Support Statement for Visual Basic 6.0 | Microsoft Docs](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-basic-6/visual-basic-6-support-policy)
12. [Getting ready for Windows 10 – SDKs, compatibility, bridges | Building Apps for Windows](https://blogs.windows.com/buildingapps/2015/06/22/getting-ready-for-windows-10-sdks-compatibility-bridges/)