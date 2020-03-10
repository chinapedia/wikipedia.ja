> この記事は[Visual Basic .NET](https://ja.wikipedia.org/wiki/Visual_Basic_.NET)から翻訳されています。


**Visual Basic .NET** （ヴィジュアル ベーシック ドットネット）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した[プログラミング言語](../Page/プログラミング言語.md "wikilink")およびその処理系。**VB.NET**と略されて呼ばれることが多い。[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")に対応していない旧来の[Visual Basic](../Page/Visual_Basic.md "wikilink")（バージョン6.0まで、VB6）の後継である。

なお[Visual Studio](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink") 2005以降では、「Visual Basic .NET」や「VB.NET」という呼称ではなく、従来のように「Visual Basic」という呼称が用いられるようになっている\[1\]が、6.0以前との互換性はなく、また.NETベースであることには変わりない。

## 概説

[C++](../Page/C++.md "wikilink")や[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[C\#などのC系言語と比較して](../Page/C_Sharp.md "wikilink")、VB/VB.NETは文法が[自然言語](../Page/自然言語.md "wikilink")に近いため、が、本格的な[ソフトウェア](../Page/ソフトウェア.md "wikilink")の作成にも使用できる。なおVB.NETはマイクロソフトが推進している[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")の一環で開発された言語であり、[アプリケーション](https://ja.wikipedia.org/wiki/アプリケーション "wikilink")実行コードは[.NET Framework上で動作するほか](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")、言語仕様に[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")が本格的に取り入れられるなど、前バージョンの[Visual Basic 6.0からの変更点はかなりの数にのぼり](../Page/Visual_Basic.md "wikilink")、言語仕様の互換性は低い。VB.NETに移行できない旧VB製アプリケーションを救済するため、VB.NETがリリースされた後にリリースされた[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") OSにおいても、旧VBの開発環境や旧VBランタイムのサポートが条件付きで継続されるなどの特別延命措置が図られたりしている。Visual Basic .NETには、従来のVisual Basicからの移行を容易にするアップグレードウィザード\[2\]や、従来の一部機能を実現する互換ライブラリが実装されている\[3\] \[4\]。

[コンパイラ](../Page/コンパイラ.md "wikilink")はマイクロソフトから無料で提供されているので、[Windows付属のメモ帳等を使ってプログラムすることもできるが](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、専用に開発された[統合開発環境](../Page/統合開発環境.md "wikilink")を使って開発するのが一般的である。

かつては旧来のVisual Basicと同様、製品は有償でのみ提供されていたが、バージョン2005以降は機能制限版であるExpressエディションが、またバージョン2013以降はProfessionalエディション相当の機能を持ちライセンス制約の強いCommunityエディションがそれぞれ無償で配布されている。

VB.NETでは[Microsoft Windows用の](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[アプリケーション開発](../Page/アプリケーションソフトウェア.md "wikilink")、[Web用のアプリケーション開発](../Page/World_Wide_Web.md "wikilink")、およびモバイル向けのアプリケーション開発などを行なうことができる。利用可能なVisual Studioプロジェクトテンプレートも、[Visual C\#とほぼ同様である](../Page/Microsoft_Visual_C_Sharp.md "wikilink")。

### 実行速度

旧来のVBは[Visual C++と比較してアプリケーションの実行速度性能に問題が発生することもあったが](https://ja.wikipedia.org/wiki/Visual_C++ "wikilink")、実行環境を[.NET Frameworkに移したVB](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink").NETでは、最終的にコンパイラが出力するコードは[Visual C\#等と同じ](../Page/Microsoft_Visual_C_Sharp.md "wikilink")[MSIL](https://ja.wikipedia.org/wiki/MSIL "wikilink")[中間コード](https://ja.wikipedia.org/wiki/中間コード "wikilink") (Javaの[バイトコード](../Page/バイトコード.md "wikilink")に近い) であるため、他の.NET言語と比較して速度面でも遜色ないものとなっている。なお、MSILは実行時に.NETの[JITコンパイラにより最適化されたネイティブコードに変換される](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")。

### DirectXのサポート

[Direct3D](../Page/Direct3D.md "wikilink")などのマルチメディアコンポーネントを含む[Microsoft DirectXに関しては](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、VB.NETおよび[Visual C\#などの](../Page/Microsoft_Visual_C_Sharp.md "wikilink").NET言語からDirectX 9を操作するための.NETマネージ ライブラリである[Managed DirectXが提供されている](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")。なお、[XNAのリリースに伴い](../Page/Microsoft_XNA.md "wikilink")、Managed DirectXの更新は終了しているが、[Windows API Code Pack for Microsoft .NET Frameworkと呼ばれるWindows](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink") APIおよびDirectXを含むCOMコンポーネントの.NET用ラッパーライブラリ、もしくはオープンソース開発されている[SlimDX](https://ja.wikipedia.org/wiki/SlimDX "wikilink")ライブラリや[SharpDXライブラリなどを使用することで](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、.NET言語からもDirectX 9、DirectX 10、DirectX 11やDirectX 12を使用することが可能となっている。[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")などの[グルー言語](../Page/グルー言語.md "wikilink")により独自のラッパーを明示的に作成することで、.NET言語からDirectXを間接的に利用することも可能である。

### 従来のVisual Basicとの文法の比較

これらは旧Visual BasicとVisual Basic .NETの文法の類似点を示したサンプルコードである。どちらもメッセージボックスに"Hello, World"のメッセージとOK[ボタンを表示させるものである](../Page/ボタン_\(GUI\).md "wikilink")。

従来のVisual Basicのコード例:

``` vb
Private Sub Command1_Click()
    MsgBox "Hello, World"
End Sub
```

Visual Basic .NETのコード例:

``` vbnet
'Imports System.Windows.Forms ' Windows Forms の場合。
'Imports System.Windows ' WPF の場合。
Private Sub Button1_Click(ByVal sender As System.Object, _
              ByVal e As System.EventArgs) Handles Button1.Click
    MessageBox.Show("Hello, World")
End Sub
```

なお、Visual Basic .NETでも旧VBや[VBScript](../Page/VBScript.md "wikilink")\[5\] \[6\]に実装されていた旧MsgBox関数などの互換機能はライブラリによってサポートされている\[7\] \[8\] \[9\]が、以下のように`()`を使ったメソッド呼び出しの形で記述しなければならない。

``` vbnet
Imports Microsoft.VisualBasic.Compatibility ' ファイル先頭に記述する。
Private Sub Button1_Click(ByVal sender As System.Object, _
              ByVal e As System.EventArgs) Handles Button1.Click
    MsgBox("Hello, World")
End Sub
```

#### オブジェクト指向への対応

VB6ではクラスモジュールの定義、メンバー変数やメソッドのカプセル化、[インターフェイスの実装による](https://ja.wikipedia.org/wiki/インタフェース_\(抽象型\) "wikilink")[ポリモーフィズム](../Page/ポリモーフィズム.md "wikilink")をサポートしていた。ただしクラスの[継承はサポートせず](../Page/継承_\(プログラミング\).md "wikilink")、オブジェクト指向プログラミングを完全サポートしているとは言い難かった。VB.NETではクラス継承がサポートされ、本格的なオブジェクト指向言語となった。

#### .NET Frameworkライブラリ

VB6ではVisual Basicに固有のステートメントによってフォームの制御や文字列の操作をプログラムしていたが、VB.NETでは[C\#などと共通に使われる](../Page/C_Sharp.md "wikilink").NET Frameworkの標準ライブラリに従ったプログラミングが必要となった。このため、従来のVBプログラマのノウハウが通用しにくい状況が生まれた。。

#### エラー処理

VB6ではエラー発生時に`On Error GoTo`文によってメソッド内のエラー処理にジャンプさせる方式であった。VB.NETでは[C\#や](../Page/C_Sharp.md "wikilink")[Java](https://ja.wikipedia.org/wiki/Java "wikilink")などと同様に 、`Try - Catch - Finally`による[例外処理](../Page/例外処理.md "wikilink")を記述できる。これによって呼び出し先メソッド内部で生じたエラーを、呼び出し側メソッドで一括して取り扱うことができるなど、プログラムの柔軟性が増した。

#### 固定長文字列の廃止

他の.NET言語との互換性確保のため\[10\]、固定長文字列は (基本データ型としては) サポートされなくなった。Visual Basic 6.0互換関数が用意されているが、マルチバイト文字では正常に動作しないため、目的の出力形式にエンコードしてバイト数をカウントしてから処理を行うといったコーディングが必要となる。

## コード例

以下はコンソールに"Hello, World\!"と出力する例である。

``` vb
Module Module1
    Sub Main()
        Console.WriteLine("Hello, World!")
    End Sub
End Module
```

## 歴史

バージョン7.xに限りVisual Basic .NETと称しているが、従来のようにVisual Basicと名称が改められた8.0以降もVB.NETの系列であることに違いはない。Microsoft.VisualBasic.dllやvbc.exe、およびVisual Studio [IDEのバージョン情報ダイアログに見られるように](../Page/統合開発環境.md "wikilink")、**製品バージョンおよび内部バージョンはVisual Studioと同様のバージョン番号が割り当てられている**。また、内部バージョン13は[忌み番](https://ja.wikipedia.org/wiki/忌み番 "wikilink")のためスキップされた。

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
<td><p>Visual Basic .NET</p></td>
<td><p>2002</p></td>
<td><p>7.0</p></td>
<td><p>2002年</p></td>
<td><p>言語仕様の大幅変更（完全なオブジェクト指向）。実行環境に .NET Framework 1.0 を採用。</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>2003</p></td>
<td><p>7.1</p></td>
<td><p>2003年</p></td>
<td><p>.NET Framework 1.1 に対応。</p></td>
</tr>
<tr class="odd">
<td><p>Visual Basic 2005</p></td>
<td><p>2005</p></td>
<td><p>8.0</p></td>
<td><p>2005年</p></td>
<td><p>.NET Framework 2.0 に対応。</p></td>
</tr>
<tr class="even">
<td><p>Visual Basic 2008</p></td>
<td><p>2008</p></td>
<td><p>9.0</p></td>
<td><p>2007年</p></td>
<td><p>LINQやラムダ式の導入など言語機能を強化。.NET Framework 3.5 に対応。</p></td>
</tr>
<tr class="odd">
<td><p>Visual Basic 2010</p></td>
<td><p>2010</p></td>
<td><p>10.0</p></td>
<td><p>2010年</p></td>
<td><p>.NET Framework 4.0 に対応。</p></td>
</tr>
<tr class="even">
<td><p>Visual Basic 2012</p></td>
<td><p>2012</p></td>
<td><p>11.0</p></td>
<td><p>2012年</p></td>
<td><p>.NET Framework 4.5 に対応。Async/Awaitの導入。</p></td>
</tr>
<tr class="odd">
<td><p>Visual Basic 2013</p></td>
<td><p>2013</p></td>
<td><p>12.0</p></td>
<td><p>2013年</p></td>
<td><p>.NET Framework 4.5.1 に対応。</p></td>
</tr>
<tr class="even">
<td><p>Visual Basic 2015</p></td>
<td><p>2015</p></td>
<td><p>14.0</p></td>
<td><p>2015年</p></td>
<td><p>.NET Framework 4.6 に対応。</p></td>
</tr>
<tr class="odd">
<td><p>Visual Basic 2017</p></td>
<td><p>2017</p></td>
<td><p>15.0, 15.3, 15.5, 15.8</p></td>
<td><p>2017年</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Visual Basic 2019</p></td>
<td><p>2019</p></td>
<td><p>16.0</p></td>
<td><p>2019年</p></td>
<td><p>.NET Core対応に重点を置く。</p></td>
</tr>
</tbody>
</table>

### Visual Basic .NET (2002) (VB.NET 7.0)

[2002年](../Page/2002年.md "wikilink")に、Visual Basicを基に強い[オブジェクト指向プログラミング](../Page/オブジェクト指向プログラミング.md "wikilink")の概念を取り入れた新しい言語Visual Basic .NETの開発環境・処理系として、Microsoft Visual Studio .NET (Microsoft Visual Basic .NET) がリリースされた。VB.NETはVB6の後継言語とされ、マイクロソフト社の[.NET Frameworkという新しい技術基盤に対応している](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。対応する.NETのバージョンは.NET Framework 1.0。

VB.NETは新たに[ウェブサーバ](https://ja.wikipedia.org/wiki/ウェブサーバ "wikilink")用のプログラム、[Web用のプログラムが開発できるなどの](../Page/World_Wide_Web.md "wikilink")[ネットワーク開発機能が追加された](../Page/コンピュータネットワーク.md "wikilink")。VB6の後継といっても、豊富な[デバッグ](../Page/デバッグ.md "wikilink")機能が追加されたり、[中間コード形式になるといった言語設計思想そのものが変わるなど](../Page/中間言語.md "wikilink")、様々な点で大幅な機能の追加および削除が行われた。

### Visual Basic .NET 2003 (VB.NET 7.1)

対応する.NETのバージョンは.NET Framework 1.1。

### Visual Basic 2005 (VB 8.0)

製品名称からは「.NET」という名前がなくなったが、上記のVB.NETと連続性がある言語である。言語仕様が強化され、C\# 2.0同様に[ジェネリックの要素が導入されたほか](../Page/ジェネリックプログラミング.md "wikilink")、[パーシャルクラス](https://ja.wikipedia.org/wiki/パーシャルクラス "wikilink")や演算子の[オーバーロード](../Page/オーバーロード.md "wikilink")などがサポートされた。また、開発環境も大きく強化されている。

対応する.NETのバージョンは.NET Framework 2.0であるが、Visual Studio用の拡張をインストールすることで.NET Framework 3.0対応アプリケーションの開発も可能になる。

### Visual Basic 2008 (VB 9.0)

同時期にリリースされたC\# 3.0に合わせて言語仕様が強化され、構造化照会構文である[LINQや](../Page/統合言語クエリ.md "wikilink")、[ラムダ式](../Page/ラムダ計算.md "wikilink")、[匿名型](https://ja.wikipedia.org/wiki/匿名型 "wikilink")などの要素が追加された。 対応する.NETのバージョンは.NET Framework 3.5（.NET 3.5は3.0および2.0の完全な[スーパーセット](https://ja.wikipedia.org/wiki/スーパーセット "wikilink")のため、3.0および2.0のアプリケーション開発も可能となっている）。

### Visual Basic 2010 (VB 10.0)

対応する.NETのバージョンは.NET Framework 4.0（3.5、3.0、2.0での開発も可能）。

C\#の言語設計者として知られるアンダース・ヘルスバーグ氏が設計に携わり、VBとC\#との間の言語間の格差の低減が図られるようになった\[11\] \[12\]。

### Visual Basic 2012 (VB 11.0)

.NET Framework 4.5とともに公開。[Visual Studio](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink") 2012に同梱される。

C\# 5.0同様、非同期プログラミングを言語仕様レベルでサポートするAsync/Await構文を導入した。

### Visual Basic 2013 (VB 12.0)

.NET Framework 4.5.1とともに公開。[Visual Studio](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink") 2013に同梱される。Developer Packをインストールすることで.NET Framework 4.5.2対応アプリケーションの開発も可能になる\[13\]。

### Visual Basic 2015 (VB 14.0)

2015年に.NET Framework 4.6とともに公開。[Visual Studio](https://ja.wikipedia.org/wiki/Visual_Studio "wikilink") 2015に同梱される。[Roslyn](https://ja.wikipedia.org/wiki/Roslyn "wikilink")と呼ばれるコンパイラレイヤーにより、Visual C\#と同等のIDE機能を備えるに至った\[14\]。

VB 14の主要な新機能は下記のとおり。

  - Null値反映演算子 `?.`
  - 複数行の文字列リテラル
  - `NameOf`演算子
  - [文字列補間](https://ja.wikipedia.org/wiki/文字列補間 "wikilink")
  - 行末コメント

### Visual Basic 2017 (VB 15.x)

2017年にVisual Studio 2017とともに公開。15.0、15.3、15.5、15.8のリビジョンで新しいVisual Basic 15の言語機能を拡張した\[15\]。

### Visual Basic 2019 (VB 16.0)

2019年にVisual Studio 2019とともに公開\[16\]。.NET Core に重点を置いた Visual Basic の最初のバージョンとなった\[17\]。

## 脚注

## 関連項目

  - [Microsoft Visual Studio Express](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio_Express "wikilink")
  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [Visual Basic](../Page/Visual_Basic.md "wikilink")
  - [Visual Basic for Applications](../Page/Visual_Basic_for_Applications.md "wikilink")

## 外部リンク

  - [Visual Basic - MSDN](https://docs.microsoft.com/ja-jp/dotnet/visual-basic/)
  - \[<https://docs.microsoft.com/ja-jp/previous-versions/technical-document/dd314356(v=msdn.10>) Visual Basic 6.0 ユーザーのための Visual Basic .NET 移行ガイド - MSDN\]

{{.NET}}

[Category:BASIC](https://ja.wikipedia.org/wiki/Category:BASIC "wikilink") [Category:オブジェクト指向言語](https://ja.wikipedia.org/wiki/Category:オブジェクト指向言語 "wikilink") [Category:統合開発環境](https://ja.wikipedia.org/wiki/Category:統合開発環境 "wikilink") [Category:コンパイラ](https://ja.wikipedia.org/wiki/Category:コンパイラ "wikilink") [Category:Microsoft_Visual_Studio](https://ja.wikipedia.org/wiki/Category:Microsoft_Visual_Studio "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.  [Visual Basic リファレンス](https://msdn.microsoft.com/ja-jp/library/sh9ywfdk%28v=vs.80%29.aspx)
2.  [VB 6.0 ユーザーのための VB .NET 移行ガイド - アップグレードウィザードの利用](https://msdn.microsoft.com/ja-jp/library/dd297684.aspx)
3.  [ITレポート（動向／解説） - 【速報】これがニューVBだ！：ITpro](http://itpro.nikkeibp.co.jp/members/NSW/ITARTICLE/20001212/1/)
4.  [Visual Basic 6.0 互換性ライブラリ](https://msdn.microsoft.com/ja-jp/library/wk6ka2wf%28v=vs.90%29.aspx)
5.  [MsgBox 関数](https://msdn.microsoft.com/ja-jp/library/cc410277.aspx)
6.  [バージョン情報 (VBScript)](https://msdn.microsoft.com/ja-jp/library/cc392490.aspx)
7.
8.  [MsgBox 関数 (Visual Basic)](https://msdn.microsoft.com/ja-jp/library/139z2azd%28v=vs.90%29.aspx)
9.  [第6回　VB開発者が最新.NET Frameworkを効率よく習得する方法 － ＠IT](http://www.atmarkit.co.jp/fdotnet/vblab/opensemi_06/opensemi_06_02.html)
10. [VB 6.0 ユーザーのための VB .NET 移行ガイド - 固定長文字列](https://msdn.microsoft.com/ja-jp/library/dd297714.aspx)
11.
12. [VB.NETに未来はあるのか？](http://www.infoq.com/jp/news/2009/06/Future-VB.NET)
13. [Download Microsoft .NET Framework 4.5.2 Developer Pack for Windows Vista SP2, Windows 7 SP1, Windows 8, Windows 8.1, Windows Server 2008 SP2 Windows Server 2008 R2 SP1, Windows Server 2012 and Windows Server 2012 R2 from Official Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=42637)
14. [Visual Studio 2015の新機能“Roslyn”とは - Build Insider](http://www.buildinsider.net/enterprise/roslyn/01)
15. [Visual Basic の新機能 - Visual Basic | § Visual Basic 2017, 15.3, 15.5, 15.8 | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/visual-basic/getting-started/whats-new#visual-basic-158)
16. [Visual Studio 2019 リリースノート](https://docs.microsoft.com/ja-jp/visualstudio/releases/2019/release-note)
17. [Visual Basic の新機能 - Visual Basic | § Visual Basic 16.0 | Microsoft Docs](https://docs.microsoft.com/ja-jp/dotnet/visual-basic/getting-started/whats-new#visual-basic-160)