> この記事は[JScript](https://ja.wikipedia.org/wiki/JScript)から翻訳されています。


**JScript**（ジェイ・スクリプト）は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")製の[スクリプト言語](../Page/スクリプト言語.md "wikilink")であり、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 上で動作する。

[JavaScript](../Page/JavaScript.md "wikilink")と類似しており、[Internet Explorerを使用したクライアントサイドスクリプティング処理](../Page/Internet_Explorer.md "wikilink")、および [Internet Information Services](../Page/Internet_Information_Services.md "wikilink") (IIS) などを使用したサーバサイドスクリプティング処理を記述することができる。

また、[Windows Script Host](https://ja.wikipedia.org/wiki/Windows_Script_Host "wikilink") (WSH) を利用することで、Windows上でのバッチ処理を記述することができる。

[拡張子](../Page/拡張子.md "wikilink")は、通常 .js を使用する。

## 主な特徴

[ECMAScript](../Page/ECMAScript.md "wikilink")や[JavaScript](../Page/JavaScript.md "wikilink")と互換性がある。他にJScriptには、以下のような特徴がある。

  - データ型 - JScriptで使用するデータ型は、数値、文字、オブジェクト（日付など）、ブール（真偽）など多様なデータの情報を有することができる。
  - ファイル入出力 - `FileSystemObject`を使用することで、ファイルの入出力ができる。
  - アプリケーション制御 - HTML組み込みの場合JScript内部よりVBScript内の関数を呼び出すことが出来る。アプリケーションがActiveXに対応している場合はJScriptで制御が出来る。（例:Word, Excel）

## バージョン

### JScript

オリジナルのJScriptは[Active Scriptingのエンジンである](https://ja.wikipedia.org/wiki/Active_Scripting "wikilink")。他のActive Scripting言語と同じように[COM/OLEオートメーションプラットフォーム上に実装されており](https://ja.wikipedia.org/wiki/OLE "wikilink")、アプリケーションをホストするためのスクリプト機能を提供する。これは[Internet Explorerで表示されたウェブページ上で使用されるほか](../Page/Internet_Explorer.md "wikilink")、[HTML アプリケーション](https://ja.wikipedia.org/wiki/HTML_アプリケーション "wikilink")、古典的[ASP](../Page/Active_Server_Pages.md "wikilink")、[Windows Script Host](https://ja.wikipedia.org/wiki/Windows_Script_Host "wikilink")、あるいは他の[OLE オートメーション環境などで使用される](../Page/Object_Linking_and_Embedding.md "wikilink")。より新しい.NETベースのJScriptと混同しないよう注意する必要がある。

<table>
<tbody>
<tr class="odd">
<td><table>
<thead>
<tr class="header">
<th><p>バージョン</p></th>
<th><p>公開日</p></th>
<th><p>共に公開されたソフトウェア[1]</p></th>
<th><p>対応するJavaScriptバージョン<sup><a href="https://ja.wikipedia.org/wiki/#fn_1" title="wikilink">1</a></sup></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>1996年8月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_3" title="wikilink">Internet Explorer 3.0</a></p></td>
<td><p>1.0</p></td>
</tr>
<tr class="even">
<td><p>2.0</p></td>
<td><p>1997年1月</p></td>
<td><p><a href="../Page/Internet_Information_Services.md" title="wikilink">Internet Information Server 3.0</a></p></td>
<td><p>1.1</p></td>
</tr>
<tr class="odd">
<td><p>3.0</p></td>
<td><p>1997年10月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_4" title="wikilink">Internet Explorer 4.0</a></p></td>
<td><p>1.3</p></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td><p>1998年9月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio#Visual_Studio_6.0" title="wikilink">Visual Studio 6.0</a> (<a href="https://ja.wikipedia.org/wiki/Visual_InterDev" title="wikilink">Visual InterDevの一部として</a>)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p>1999年3月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_5" title="wikilink">Internet Explorer 5.0</a></p></td>
<td><p>1.4</p></td>
</tr>
<tr class="even">
<td><p>5.1</p></td>
<td><p>2000年2月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_5" title="wikilink">Internet Explorer 5.01</a></p></td>
<td><p>1.4</p></td>
</tr>
<tr class="odd">
<td><p>5.5</p></td>
<td><p>2000年7月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_5.5" title="wikilink">Internet Explorer 5.5</a></p></td>
<td><p>1.5</p></td>
</tr>
<tr class="even">
<td><p>5.6</p></td>
<td><p>2001年10月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_6" title="wikilink">Internet Explorer 6.0</a></p></td>
<td><p>1.5</p></td>
</tr>
<tr class="odd">
<td><p>5.7</p></td>
<td><p>2006年11月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_7" title="wikilink">Internet Explorer 7.0</a><br />
<a href="https://ja.wikipedia.org/wiki/Microsoft_Windows_XP#Service_Pack_3" title="wikilink">Windows XP SP3</a></p></td>
<td><p>1.5</p></td>
</tr>
<tr class="even">
<td><p>5.8</p></td>
<td><p>2009年3月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_8" title="wikilink">Internet Explorer 8.0</a></p></td>
<td><p>1.5</p></td>
</tr>
<tr class="odd">
<td><p>後継(<a href="https://ja.wikipedia.org/wiki/Chakra" title="wikilink">Chakra</a>)</p></td>
<td><p>2011年3月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_9" title="wikilink">Internet Explorer 9.0</a>～</p></td>
<td><p>&lt;!--</p></td>
</tr>
<tr class="even">
<td><p>9.0</p></td>
<td><p>2011年3月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_9" title="wikilink">Internet Explorer 9.0</a></p></td>
<td><p>1.8.1</p></td>
</tr>
<tr class="odd">
<td><p>10.0</p></td>
<td><p>2012年8月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_10" title="wikilink">Internet Explorer 10.0</a></p></td>
<td></td>
</tr>
<tr class="even">
<td><p>11.0</p></td>
<td><p>2013年10月</p></td>
<td><p><a href="https://ja.wikipedia.org/wiki/Internet_Explorer#Internet_Explorer_11" title="wikilink">Internet Explorer 11.0</a></p></td>
<td><p>--&gt;</p></td>
</tr>
</tbody>
</table>
<p><cite id="fn_1"><a href="https://ja.wikipedia.org/wiki/#fn_1_back" title="wikilink">注(1):</a></cite> JScriptはJavaScriptと同様、ECMA標準に定義されていない多くの機能をサポートする[2]。</p></td>
<td></td>
</tr>
</tbody>
</table>

JScriptはWindows CE上でも動作するが、このバージョンにはActive Debuggingがない。

(出典: [MSDN](http://msdn.microsoft.com/library/en-us/script56/html/adb60c22-824f-4795-9176-101e8aa9e972.asp)、[WebmasterWorld Forum](http://www.webmasterworld.com/forum91/68.htm))

### JScript .NET

JScript .NETは**JScript**の[.NET Framework向けの実装である](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。[CLS互換のクラスベースの言語](https://ja.wikipedia.org/wiki/共通言語仕様 "wikilink")\[3\]であり、以前のJScriptの非常に強力な機能を継承している。 JScript .NETは[ASP.NET](../Page/ASP.NET.md "wikilink")や完全な.NETアプリケーションの開発に使用することができる。 しかし、[Visual Studioにおけるサポートがない](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")。

[CLR上で動作し](../Page/共通言語ランタイム.md "wikilink")、変数に型を指定した場合、C\# などの他の .NET Framework 上の言語と同等の速度で動く。 JScript の上位互換であるが、高速モードでコンパイルすると、全ての変数を宣言する必要が出るなど、一部、互換性が無くなる。コンパイラのデフォルトは高速モードである。

<div align="center">

| バージョン | 日時         | 共に公開されたソフトウェア                                                                 |
| ----- | ---------- | ----------------------------------------------------------------------------- |
| 7.0   | 2002年1月15日 | [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 1.0 |
| 7.1   | 2003年4月1日  | [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 1.1 |
| 8.0   | 2005年11月7日 | [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 2.0 |
| 10.0  | 2010年4月13日 | [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 4.0 |

</div>

JScript .NETは[.NET Compact Frameworkではサポートされない](../Page/.NET_Compact_Framework.md "wikilink")。

JScript .NETのバージョンは古典的なJScriptのバージョンとは無関係なことに注意する必要がある。JScript .NETは独立した製品である。 JScript .NETはVisual Studioの統合開発環境でサポートされていないが、そのバージョンは他の.NET言語と共通で、対応するVisual Studioのバージョンに従っている。

.NET Framework 3.0ではJScriptのバージョンは新しくなっていない。 （出典: 各フレームワークに含まれるMicrosoft.JScript.dllのファイルバージョン）

## コード例

[HTML](../Page/HyperText_Markup_Language.md "wikilink") に埋め込む場合は、以下のように表記する。

``` html4strict
 <html>
 <script language="JScript">
 var weekname = new Array('日','月','火','水','木','金','土');
 var date = new Date();
 var str = "";
 str += date.getYear() + "年";
 str += (date.getMonth() + 1) + "月";
 str += date.getDate() + "日";
 str += " (" + weekname[date.getDay()] + ")";
 document.write("現在の日付は" + str + "です");
 </script>
 <body>
 ・・・
```

また、[ActiveX](../Page/ActiveX.md "wikilink")を交えた次のようなコードでファイルを生成することができる。

``` javascript
 // ファイル操作の為のオブジェクトを生成。

 var fso = new ActiveXObject("Scripting.FileSystemObject");
 // もし C:\jscript_test というフォルダが無ければ
 if(! fso.FolderExists("C:\\jscript_test")) {
     // C:\jscript_test を作る。
     var fol = fso.CreateFolder("C:\\jscript_test");
 }
 // .txt のファイル以外でも作成できるという例。
 var fil = fso.CreateTextFile("c:\\jscript_test\\output.html");
 // 作成したファイルに1行書き込む。
 fil.WriteLine("<html><head><title>test</title></head><body>test <b>test</b></body></html>");
 // ファイルを開放する。
 fil.close();
 //完了ダイアログを表示。
 WScript.Echo("C:\\jscript_test\\output.html にファイルが作成されました。");
```

## 脚注

<references />

## 関連項目

  - [JavaScript](../Page/JavaScript.md "wikilink")
  - [VBScript](../Page/VBScript.md "wikilink")
  - [ECMAScript](../Page/ECMAScript.md "wikilink")

## 外部リンク

  - [JScript](http://msdn.microsoft.com/ja-jp/library/cc427807.aspx)

[Category:JavaScript](https://ja.wikipedia.org/wiki/Category:JavaScript "wikilink") [Category:マイクロソフトのプログラミング言語](https://ja.wikipedia.org/wiki/Category:マイクロソフトのプログラミング言語 "wikilink")

1.
2.
3.