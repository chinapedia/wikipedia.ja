> この記事は[Visual Basic for Applications](https://ja.wikipedia.org/wiki/Visual_Basic_for_Applications)から翻訳されています。


**Visual Basic for Applications**（ビジュアルベーシック・フォー・アプリケーションズ、VBA）は、主に[マイクロソフト](../Page/マイクロソフト.md "wikilink")製の[Microsoft Officeシリーズに搭載されている](../Page/Microsoft_Office.md "wikilink")[プログラミング言語](../Page/プログラミング言語.md "wikilink")である。

## 概要

[マイクロソフト](../Page/マイクロソフト.md "wikilink")が1990年代に開発していた汎用[プログラミング言語](../Page/プログラミング言語.md "wikilink")・[Microsoft Visual Basicを](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")、同社製品の[Microsoft Officeに搭載したものがVBAである](../Page/Microsoft_Office.md "wikilink")。VBAを使用することで、[Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[Access](../Page/Microsoft_Access.md "wikilink")、[Word](../Page/Microsoft_Word.md "wikilink")、[Outlook](../Page/Microsoft_Outlook.md "wikilink")、[PowerPointなど](../Page/Microsoft_PowerPoint.md "wikilink")、Officeのアプリケーション・ソフトウェアの機能をカスタマイズしたり、拡張したりすることができる。

[Microsoft OfficeシリーズにはVBAのソースコード作成](../Page/Microsoft_Office.md "wikilink")・編集ソフトウェアおよびプログラム実行環境が最初から付属しているため、使用を始めるにあたり、Office以外の特別なソフトウェアの用意やセッティングを必要としない。文献やネット情報も多く、最低限の学習で誰でも手軽にプログラミングが始められる。また、プログラムの実行が容易なことも特徴である。[C言語](../Page/C言語.md "wikilink")などでは[ソースコード](../Page/ソースコード.md "wikilink")を書き上げてからコンピュータに実行させる前に[機械語](../Page/機械語.md "wikilink")に変換して実行プログラム形式として出力するための[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")および[リンク](../Page/リンケージエディタ.md "wikilink")（ビルド）作業が必要だが、VBAは疑似コード ([Pコード](https://ja.wikipedia.org/wiki/Pコード "wikilink")) ベースの[コンパイラ](../Page/コンパイラ.md "wikilink")型および[インタプリタ](../Page/インタプリタ.md "wikilink")型両方の性質を持っており\[1\]、ユーザーが記述したソースコードを1アクションで自動的に疑似コードにコンパイルして直接コンピュータに実行させることができる。手軽に利用できる一方で、汎用プログラミング言語に共通の機能は一通り備えており、高度な機能まで修得しようとすると相応の学習が必要である。

## 機能・用途

  - 定型業務の自動化、省力化。例えば、毎日更新されるデータを出社してからいちいち手入力し、手順を入力して計算させていた業務を、夜の間に自動でソフトウェアを起動し、データを読み込ませ、朝までに処理させておける。またOfficeアプリケーションでは[マクロ記録](../Page/マクロ言語.md "wikilink")/再生という操作手順の記録/再生機能を使って、プログラムに関する知識が少ないユーザーでも、ある程度の定型業務の自動化を行なえる。マクロはVBAコードの自動生成により実現されている。
  - 特定の使用目的への最適化。例えばある会社で、社員の一覧名簿を作成し、自社独自の給与体系に従い、各自の給与を自動で計算できる。またその場合、考慮する数字を自動で参照して集計するなど、目的に応じた特殊な[関数を作成することもできる](../Page/サブルーチン.md "wikilink")（ユーザー定義関数という）。また、ユーザー独自の[フォーム](https://ja.wikipedia.org/wiki/フォーム "wikilink")を作成でき、様々な[プラグイン](../Page/プラグイン.md "wikilink")を組み込むことなども可能である。
  - Officeの使用に特化しMicrosoft Office専用という印象が強いが、限定的ながら[Internet ExplorerなどOffice以外のソフトウェアを制御する機能が与えられている](../Page/Internet_Explorer.md "wikilink")。またマイクロソフト社からしかるべき[ライセンス](../Page/ライセンス.md "wikilink")を取得することで他の[アプリケーションに組み込むことも可能である](../Page/アプリケーションソフトウェア.md "wikilink")。実際、マイクロソフト社に買収される前の[Visioにも搭載されていた](../Page/Microsoft_Visio.md "wikilink")。[CAD](../Page/CAD.md "wikilink")ソフトの[AutoCAD](../Page/AutoCAD.md "wikilink")や[MicroStation V8等にも搭載されている](../Page/MicroStation.md "wikilink")。

## VBAの歴史

  - VBA は [1993年](../Page/1993年.md "wikilink") (日本では[1994年](../Page/1994年.md "wikilink")) に MS Excel 5.0 で初めて発売された。それは瞬く間に開発者の間で、Excel を使用して企業ソリューションを作成するツールとして成功を収めた。AccessBASIC と[WordBASIC](../Page/WordBASIC.md "wikilink") を置き換え、Microsoft Project、Access と Word に VBA が搭載されたことで、VBA はより一般的になった。
  - VBA 4.0は、以前のものと比較して完全にアップグレードされたメジャーリリースとなった。[1996年](../Page/1996年.md "wikilink")にリリースされ、C++で書かれ、オブジェクト指向言語となった。
  - VBA 5.0 は、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に MS Office 97 に含まれるすべての製品と共に発売された。ただし、[VBScript](../Page/VBScript.md "wikilink") を実装した Outlook 97 は例外。
  - VBA 6.0 および VBA 6.1 は [1999年](../Page/1999年.md "wikilink")に発売され、特に Office 2000 の COM アドインをサポートした。 VBA 6.2 は Office 2000 SR-1 と共にリリースされた。
  - VBA 6.3 は Office XP と一緒にリリースされ、VBA 6.4 では Office 2003、VBA 6.5 は Office 2007 でリリースされた。
  - Office 2010 には VBA 7.0 が搭載された。VBA 7 には、64 ビットサポート以外に、VBA 6.5 と比べて開発者向けの新機能はない。ただし、VBA 6.5/Office 2007 以降、マイクロソフトは他のアプリケーション向けの VBA のライセンスを停止した。
  - Office 2013、Office 2016、および Office 2019 には VBA 7.1 が搭載されている。

## 近年の動向

2007 年 7 月 1 日以降、マイクロソフトは新規顧客への VBA 再配布ライセンス提供を停止した。マイクロソフトは、[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") のリリース以降、ずっと VBA に .NET ベースの言語を追加しようとしてきた。\[2\].NET Frameworkバージョン1.0 および 1.1 には *Script for the .NET Framework* というスクリプト ランタイム テクノロジが搭載されていた。\[3\]また、Visual Studio .NET 2002 および 2003 SDK には、VB.NETをサポートする *Visual Studio for Applications* (VSA)という別のスクリプト IDEが含まれていた。\[4\]\[5\]\[6\] VSAの重要な特徴の一つは、[Active Scripting](https://ja.wikipedia.org/wiki/Active_Scripting "wikilink") ([VBScript](../Page/VBScript.md "wikilink") および [JScript](../Page/JScript.md "wikilink"))を通して利用が可能であり、.NETが使えないアプリケーションを.NET 言語を使用してスクリプト化することができたことだった。しかし、VSA は、Active Scriptingのサポートを望むアプリケーションの明確なアップグレード パスがないまま.NET Framework のバージョン 2.0 でサポート対象外となった\[7\]。 ([C\#](../Page/C_Sharp.md "wikilink")、[VBScript](../Page/VBScript.md "wikilink")、他の.NET言語で「スクリプト」の作成は引き続き可能で、ランタイムの一部としてインストールされた[ライブラリ](../Page/ライブラリ.md "wikilink")を介して実行時に[コンパイル](https://ja.wikipedia.org/wiki/コンパイル "wikilink")および実行することはできる。)

マイクロソフトは、[Microsoft Office 2008 for Mac](https://ja.wikipedia.org/wiki/Microsoft_Office_2008_for_Mac "wikilink") でVBA サポートを一度廃止した。\[8\]\[9\]しかし[Microsoft Office for Mac 2011](https://ja.wikipedia.org/wiki/Microsoft_Office_for_Mac_2011 "wikilink") でVBA は復活することとなった。マイクロソフトは、Windows バージョンの Office から VBA を削除する計画はないと述べている。\[10\]\[11\]

[Office 2010](https://ja.wikipedia.org/wiki/Office_2010 "wikilink") では、マイクロソフトは真のポインター データ型 LongPtr をサポートする VBA7 を導入した。これにより、64 ビットのアドレス空間を参照できるようになった。Office 2010 の 64 ビット インストールでは、MSComCtl (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) および MSComCt2 (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar)といったコモンコントロールに依存するレガシーな32ビットコードは64ビットVBAコードに移植しても機能しない。これは、32 ビット バージョンの Office 2010 では発生しない。\[12\] VBA7 には 64 ビットバージョンのコモンコントロールが含まれていないため、開発者は VBA アプリケーションを 64 ビットに移行する手段がないことになる。マイクロソフトでは、64 ビット バージョンの VBA コントロールについてソフトウェア ベンダに問い合わせるように誘導している。

## 資格検定試験

  - [VBAエキスパート](https://ja.wikipedia.org/wiki/VBAエキスパート "wikilink")
  - [Microsoft Office Specialist](../Page/Microsoft_Office_Specialist.md "wikilink")

いずれも、パソコンスクール運営の株式会社オデッセイ コミュニケーションズが実施する民間資格である。全国のパソコン教室などを会場に随時予約可能。受験料は1万数千円程度。

## コード例

以下は、Excelにおいて、「Alpha」という名前のワークシートを削除するVBAの例である。

``` vb
Application.DisplayAlerts = False
Worksheets("Alpha").Delete
Application.DisplayAlerts = True
```

また、Excelで以下のコードを実行すると、セルA1からI9の範囲に掛け算九九の表を作成することができる。

``` vb
For i = 1 To 9
    For j = 1 To 9
        Cells(i, j).Value = i * j
    Next
Next
```

下記のように配列を用いて、全ての値を配列に格納した上で一度に出力するように上記のコードを書き換えると、高速に動作するコードになる。

``` vb
Dim KukuArray(8, 8) As Integer

For i = 1 To 9
    For j = 1 To 9
        KukuArray(i - 1, j - 1) = i * j
    Next
Next

Range("A1:I9").Value = KukuArray
```

条件によって4色以上に色を塗り分けるときも、VBAを利用する（3色以下のときは一般機能の「条件付き書式」を使用するのが望ましい）。以下のコードを実行するとセルB2からE15までの範囲内のセルを5以下→水色、6以上10以下→明るい緑、11以上15以下→黄色、16以上→赤と塗り分けることができる。

``` vb
Dim myCell As Range

For Each myCell In Range("B2:E15")
    Select Case myCell.Value
    Case Is <= 5
        myCell.Interior.Color = RGB(0, 255, 255)
    Case 6 To 10
        myCell.Interior.Color = RGB(0, 255, 0)
    Case 11 To 15
        myCell.Interior.Color = RGB(255, 255, 0)
    Case Is > 15
        myCell.Interior.Color = RGB(255, 0, 0)
    End Select
Next
```

以下は、VBAと共にExcelごとプログラムを終了するVBAの例である。

``` vb
Application.Quit
```

### ユーザー定義関数

VBAを用いて、ユーザーが新たに関数を作成することもできる。ユーザー定義関数を作成するにはFunctionプロシージャを用いる。以下はHERONという名で[ヘロンの公式](../Page/ヘロンの公式.md "wikilink")を用いるユーザー定義関数のコードである。実用には、負の値や三角条件を満たさない値が入力されることを想定して、下記のコードにエラー処理ルーチンを追加しておくことが望ましい。

定義したユーザー定義関数は通常の（組み込みの）ワークシート関数同様、数式の中で用いることで呼び出す。この例で言えば、とセルに入力すると、数式を入力したセルに演算結果として6と出力される。

``` vb
Function HERON(辺1, 辺2, 辺3) As Variant

    s = (辺1 + 辺2 + 辺3) / 2
    HERON = Sqr(s * (s - 辺1) * (s - 辺2) * (s - 辺3))

End Function
```

## VBAのセキュリティ問題

他の一般的なプログラミング言語と同様に、VBA では悪意のある[マクロウイルス](https://ja.wikipedia.org/wiki/マクロウイルス "wikilink")を作成できてしまう。VBA では、セキュリティ機能のほとんどは作成者ではなくユーザーの手に委ねられる。VBA のホストアプリケーションでは、ユーザーはオプションを事前に設定でき、マクロをアプリケーションで実行できないようにしたり、ドキュメントのソースが信頼できる場合にのみ VBA コードを実行するアクセス許可を付与したりして、攻撃から身を守ることができる。

Office 2000 SP3以降はセキュリティが強化され、初期設定ではVBAマクロは無効化されている\[13\]。そのため、マクロを含むファイルを開いただけでプログラムが実行されることはないが、設定次第でセキュリティレベルを下げることもできてしまう\[14\]。また、Office 2007 以降に一般的となった新しいファイル形式 (.xlsx など) ではマクロを含むことができないので、安全性がより高まった。

## 関連項目

  - [:en:Visual Studio Tools for Applications](https://ja.wikipedia.org/wiki/:en:Visual_Studio_Tools_for_Applications "wikilink")
  - [:en:Visual Studio Tools for Office](https://ja.wikipedia.org/wiki/:en:Visual_Studio_Tools_for_Office "wikilink")
  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
  - [Microsoft FrontPage](../Page/Microsoft_FrontPage.md "wikilink")
  - [:en:OpenOffice Basic](https://ja.wikipedia.org/wiki/:en:OpenOffice_Basic "wikilink")
  - [LotusScript](https://ja.wikipedia.org/wiki/LotusScript "wikilink")

## 脚注

## 外部リンク

  - [\[MS-VBAL\]: VBA Language Specification](https://msdn.microsoft.com/en-us/library/dd361851.aspx)

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink") [Category:Microsoft_Office](https://ja.wikipedia.org/wiki/Category:Microsoft_Office "wikilink")

1.  [ACC2000: Visual Basic for Applications Is Both a Compiler and an Interpreter](https://web.archive.org/web/20060820093810/http://support.microsoft.com/default.aspx?scid=kb;en-us;209176) / [Internet Archive](https://ja.wikipedia.org/wiki/Internet_Archive "wikilink")
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13. [Excelの「マクロのセキュリティ」とは？ | 日経 xTECH（クロステック）](https://tech.nikkeibp.co.jp/it/pc/article/knowhow/20100106/1021968/)
14. [Excel のマクロのセキュリティ設定を変更する - Excel](https://support.office.com/ja-jp/article/a97c09d2-c082-46b8-b19f-e8621e8fe373)