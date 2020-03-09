> この記事は[VBScript](https://ja.wikipedia.org/wiki/VBScript)から翻訳されています。


（ブイ・ビー・スクリプト）、 は、[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink") 風の、[マイクロソフト](../Page/マイクロソフト.md "wikilink")による[スクリプト言語](../Page/スクリプト言語.md "wikilink")である。 上や （IIS）上で動作する。

## 概要

は  の構文を真似てつくられた、 のスクリプト言語であり、 のスクリプトエンジンという形態で実装されている。ランタイムとしてASPやWSHがあり、主な用途として、

  - （ASP）などを使用したサーバサイドスクリプティング処理

  - （WSH） を利用したWindows上でのネイティブ・スクリプト

  - を使用したクライアントサイドスクリプティング処理

  - （HTA）アプリケーション

が挙げられる。

ただし、WWWクライアントスクリプトとしては、対応するブラウザが  版の  だけであり、2005年時点でもほとんど使われていない。[2013年](../Page/2013年.md "wikilink")にリリースされた [Internet Explorer 11](https://ja.wikipedia.org/wiki/Internet_Explorer_11 "wikilink") では、セキュリティや互換性の設定によっては VBScript を実行しなくなり\[1\]、Windows 10 は2019年7月9日より、Windows 8.1 以前は2019年8月13日よりデフォルトで無効になった\[2\]。さらに、Windows 10 搭載の [Microsoft Edge](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink") では VBScript は動作しない。

HTAやASP、[HTML中に組み込まれることが多いが](../Page/HyperText_Markup_Language.md "wikilink")、単体のスクリプトファイルとしておかれる場合、[拡張子](../Page/拡張子.md "wikilink")は通常`.vbs`を使用する。

## 背景

は1996年8月、WWWのクライアントスクリプト言語として [{{lang](../Page/Internet_Explorer.md "wikilink") に実装された。当時[ネットスケープコミュニケーションズ](../Page/ネットスケープコミュニケーションズ.md "wikilink")とマイクロソフトは [ブラウザ戦争](https://ja.wikipedia.org/wiki/ブラウザ戦争 "wikilink")と呼ばれるWebブラウザシェアとWeb標準を巡る技術競争下にあり、1996年3月に [{{lang](https://ja.wikipedia.org/wiki/Netscape_Navigator_\(ネットスケープコミュニケーションズ\) "wikilink") に実装された  に対抗するものとして、 互換のスクリプト言語  と共に実装されたものである。

結果として、WWWのクライアントスクリプト言語としては、 が  版  でしか動作しなかったことなどから、 が勝利を収め、この分野での  は使用されなくなった。しかし、1996年12月、[{{lang](https://ja.wikipedia.org/wiki/Internet_Information_Server "wikilink") に実装された  の標準の言語として  が採用された。ASPは、プログラムコード中にHTMLコードを埋め込む手法ではなく、HTMLコード中にプログラムコードを埋め込む手法をとり、習熟の容易さから成功を収めた。同時に標準の言語として  の地位も確固たるものとなった。

一方、はWWWだけでなく、 の汎用スクリプト言語として、の標準言語として採用された。WSHは[バッチファイル](https://ja.wikipedia.org/wiki/バッチファイル "wikilink")を置き換えるものとして位置づけられ、 95 OSR2より標準で装備された。

当時のマイクロソフトは  戦略のもと、WWWとクライアント環境のシームレスな統合を目指したが、その中核スクリプト言語としてWSH、ひいては  を位置づけた。そのため、 は  オートメーションサーバを取り扱うことに長け、全ての操作はオートメーションサーバよりオブジェクトを生成し、それを介して行うという統一された様式である。これは、言語自身が環境に依存しないメリットももたらすが、反面、単純なファイルの複製でさえオブジェクトを生成し操作する手続きが必要という煩雑さももたらした。この煩雑さはバッチファイルからの脱却を阻むものとなった。

また、 戦略自体、相重なるセキュリティ問題を引き起こし、WSH上の  を利用したウイルスの出現などもあったことからセキュリティ面から敬遠される向きもあった。

簡単な処理も煩雑な記述になってしまう点、セキュリティ面のダーティなイメージから、 は圧倒的なシェアをもつオペレーティングシステムの標準のスクリプト言語にしてはあまり普及せず、 の汎用スクリプト言語としての  は、一定の評価はできるものの大成功したとは言えない。

マイクロソフトは2000年代初頭から  に変わる戦略として、戦略を打ち立てており、ASPも2002年にリリースされた[ASP.NET](https://ja.wikipedia.org/wiki/ASP.NET "wikilink")に置き換えられ、その記述言語も [C\#](../Page/C_Sharp.md "wikilink") や [{{lang](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink") 等となった。また、オペレーティングシステムの汎用スクリプト環境についてもWSHから  へ移行すると言う。

2006年現在の展望では、[PHPに代表されるオープンソースのサーバ側スクリプト言語が徐々にIIS上でも安定した動作が期待できるようになってきており](../Page/PHP_\(プログラミング言語\).md "wikilink")、サーバ側スクリプト言語としての も一部の根強い人気を除けばほぼその役割を終え、緩やかに衰退していくものと思われる。

## 主な特徴

は、[OLE](https://ja.wikipedia.org/wiki/OLE "wikilink")サーバの接着剤としてのスクリプト言語という理念のもとに設計された。 の汎用スクリプト言語と説明したが、 が  戦略への転換を迎えた現在では、むしろOLE（）用のスクリプト言語といった方が正しい。

OLE設計が徹底されており、は言語自身にはファイル入出力さえサポートしない。

また、[動的型付け](https://ja.wikipedia.org/wiki/動的型付け "wikilink")を採用している点も  から派生した言語としては異色である。

### 動的型付け

は多くのスクリプト言語同様、[動的型付け](https://ja.wikipedia.org/wiki/動的型付け "wikilink")言語であるため、変数に型はない。

のデータ型には、`Empty` 値、`Null` 値、ブール型、バイト型、整数型、通貨型、日付型、文字列型、オブジェクト型、エラー型などがあるが、これら型情報はデータ側が持ち、変数自体に型はない。(または 変数はバリアント型のみだとも言われる)。

は変数宣言または明示的な変数生成ステートメントを必須としない。はじめて使われるシンボルは変数として自動的に生成される。しかし、代入だけでなく、参照でも変数を生成してしまうため、入力間違いによる不具合を誘発しやすい。

そのため、変数宣言を強要する `Option Explicit` ステートメントをファイル先頭で宣言するのが良い[コーディングスタイル](https://ja.wikipedia.org/wiki/コーディングスタイル "wikilink")と言われる。明示的に変数を生成するには `Dim`、`Private`、`Public`、`ReDim`などの各ステートメントを用いる。

### OLEクライアント機能

OLEオブジェクトを利用するには `CreateObject` 関数を使用する。`CreateObject` は オートメーションサーバからオートメーションオブジェクトを生成し、その参照を返す。

``` vb
Dim oFileSystem
Set oFileSystem = CreateObject("Scripting.FileSystemObject")
oFileSystem.MoveFile "C:\2012年6月.xls" "C:\過去実績\2012年6月.xls"
```

以下は  のシートオブジェクトを生成するサンプルである。

``` vb
Dim oExcelSheet
Set oExcelSheet = CreateObject("Excel.Sheet")
oExcelSheet.Application.Visible = True
oExcelSheet.ActiveSheet.Cells(1,1).Value = "売上"
Set oExcelSheet = Nothing
```

OLEサーバとなっているアプリケーションを使ったスクリプトを  は簡単に記述できる。 が備えていないような機能でも、OLEサーバアプリケーションを作成すれば行うことが出来る。

### オブジェクト指向機能

は[クラスベース](https://ja.wikipedia.org/wiki/クラスベース "wikilink")の[オブジェクト指向言語であり](../Page/オブジェクト指向プログラミング.md "wikilink")、`Class`ステートメントによりクラスオブジェクトを生成することが出来る。

のクラスオブジェクトは以下のような特徴がある。

  - 継承は出来ない
  - アクセス制御は出来る
  - `Initialize`イベント、`Terminate`イベントを設定出来る。

以下に  のクラスのサンプルコードを示す。

``` vb
Class CPoint
  ' プロパティ
  Private m_x
  Private m_y

  ' メソッド
  Private Sub Class_Initialize   ' Initialize
     m_x  = 0
     m_y  = 0
  End Sub

  Private Sub Class_Terminate   ' Terminate
     MsgBox("terminated!")
  End Sub

  Public Function GetX()
    GetX = m_x
  End Function

  Public Function GetY()
    GetY = m_y
  End Function

  Public Sub SetPoint(x, y)
   m_x = x
   m_y = y
  End Sub
End Class


Dim obj
Set obj = New CPoint
MsgBox(obj.GetX)         '0 と表示

obj.SetPoint 32, 64
MsgBox(obj.GetX)         '32 と表示

Set obj = Nothing        'terminated! と表示
```

継承は出来ないものの、[動的型付け](https://ja.wikipedia.org/wiki/動的型付け "wikilink")であるため、多態は可能である。カプセル化も出来る。幾分制約が強いが、必要最低限のオブジェクト指向機能は備える。

## 他言語との比較

### 、 との比較

は  によく似た構文を持ち相互に習得しやすいが、

  - [動的型付け](https://ja.wikipedia.org/wiki/動的型付け "wikilink")
  - 多くの組み込み関数や手続きがない
  - モジュールがない

のように、 や  との相違点は大きいため互換性が低く、そのままでは使用できない場合も多い。

### との比較

標準でASP、WSHをホストとして動く言語には、 の他に、 がある。 はマイクロソフト社による （いわゆる）の実装である。同じランタイムを利用するため、機能的には似通っているが、言語の設計思想は大きく異なる。

主な相違として、

  - 組み込みGUI関数 `MsgBox`、`InputBox` の有無。
  - プロトタイプベース・オブジェクト指向言語とクラスベース・オブジェクト指向言語

が挙げられる。

特に `MsgBox` や `InputBox` が揃うことで、GUIでありながらCUIなみの手軽さで入出力を備えたUIを構築できる意義は大きい。この点で  は優れる。 なお、 において `MsgBox` は `WScript.Echo` で代替出来る。`InputBox` 相当の物は存在しないため、 の `InputBox` 関数を呼び出す。

一方、プログラミング言語としての機能は  の方が大きく優れる。 は無名関数や静的スコープのクロージャなど強力な機構を備える。

## とセキュリティ

近年の[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")にはWSHと  を組み合わせて感染する型が多発しており、 のOLEクライアント機能の強力さがユーザにとっては諸刃の剣となっている。

## コード例

以下のコードを適当なファイル（例えば、`time.vbs`）に保存し、ダブルクリックすると、現在の時刻を表示する。

``` vb
MsgBox "現在の時刻は、" & Time & " です。"
```

また、[HTML](../Page/HyperText_Markup_Language.md "wikilink") に埋め込む場合は、以下のように表記する。

``` vb
<html>
<head>
<script language="VBScript">
  Function GetTime()
    MsgBox "現在の時刻は、" & Time & "です。"
  End Function
</script>
</head>
<body>
……
</body>
</html>
```

## 脚注

## 関連項目

  - [Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic "wikilink")
  - [JavaScript](../Page/JavaScript.md "wikilink")
  - [JScript](https://ja.wikipedia.org/wiki/JScript "wikilink")
  - [WinActor](https://ja.wikipedia.org/wiki/WinActor "wikilink") - RPAツール。内部的にVBScriptを使用しており、VBScriptによる機能拡張が可能である。

## 外部リンク

  - [VBScript](https://msdn.microsoft.com/ja-jp/library/cc392489.aspx)

[Category:スクリプト言語](https://ja.wikipedia.org/wiki/Category:スクリプト言語 "wikilink") [Category:Microsoft_Windows](https://ja.wikipedia.org/wiki/Category:Microsoft_Windows "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.  \[<https://msdn.microsoft.com/ja-jp/library/dn384057(v=vs.85>).aspx インターネット ゾーンにおける Internet Explorer 11 エッジ モードでの VBScript のサポート停止\] [マイクロソフト](../Page/マイクロソフト.md "wikilink")、2013年11月20日閲覧。
2.  [An update on disabling VBScript in Internet Explorer 11 - Microsoft Edge Blog](https://blogs.windows.com/msedgedev/2019/08/02/update-disabling-vbscript-internet-explorer-windows-7-8/)