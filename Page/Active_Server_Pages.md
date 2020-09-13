> この記事は[Active Server Pages](https://ja.wikipedia.org/wiki/Active_Server_Pages)から翻訳されています。


**Active Server Pages**（アクティブサーバーページ、**ASP**）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発した[ウェブページ](../Page/ウェブページ.md "wikilink")を動的に作成する技術である。

[HTMLなどの](../Page/HyperText_Markup_Language.md "wikilink")[マークアップ言語](../Page/マークアップ言語.md "wikilink")と[VBScript](../Page/VBScript.md "wikilink")や[JavaScript](../Page/JavaScript.md "wikilink")などの[スクリプト言語](../Page/スクリプト言語.md "wikilink")を組み合わせることで成り立つ。ウェブページ間のデータのやりとりが容易であるため、[電子商取引](../Page/電子商取引.md "wikilink")（インターネットを通じた通信販売）などで活用されている。同様の技術として、[Javaサーブレット](../Page/Java_Servlet.md "wikilink")、[JavaServer Pages](../Page/JavaServer_Pages.md "wikilink") (JSP)、[PHPなどがある](../Page/PHP_\(プログラミング言語\).md "wikilink")。

ASPを動作させるための[Webサーバ](../Page/Webサーバ.md "wikilink")は[Internet Information Services](../Page/Internet_Information_Services.md "wikilink") (IIS) や (PWS) があり、IISは当初マイクロソフトのサーバ向けOS ([Windows NT Server](../Page/Microsoft_Windows_NT.md "wikilink"),[Windows 2000 Server](../Page/Microsoft_Windows_2000.md "wikilink"), [Windows Server 2003](../Page/Microsoft_Windows_Server_2003.md "wikilink")) にのみ付属していたが、現在ではホーム/ビジネス向けOS ([Windows XP Professional](../Page/Microsoft_Windows_XP.md "wikilink"), [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink"))にも付属されている。PWSは[Windows 95](../Page/Microsoft_Windows_95.md "wikilink")、[Windows 98にインストールすることが出来る](../Page/Microsoft_Windows_98.md "wikilink")。また[Windows Me以降PWSの更新は行われておらず](../Page/Microsoft_Windows_Millennium_Edition.md "wikilink")、マイクロソフト製のWebサーバはIISに一本化されている。

ASPの後継技術として[ASP.NET](../Page/ASP.NET.md "wikilink")が開発された為、現在では新規システムの開発でASPが利用される事は減りつつあるが、企業のイントラサイトや、小規模な動的ページで用いられる場合もある。

## ASPで利用できる言語

ASPは[Active Scriptingのホストであるため](https://ja.wikipedia.org/wiki/Active_Scripting "wikilink")、Active Scriptingに対応した言語を利用することができる（言語の実装によって一部制限がある）。既定の言語はVBScriptであるが、スクリプトの先頭で宣言したり、IISの設定で既定の言語として設定したりすることで、利用する言語を変更することが出来る。

## ASPのバージョン

  - Active Server Pages 1.0 (IIS 3.0) 1996年12月
  - Active Server Pages 1.0b
  - Active Server Pages 2.0 (IIS 4.0) 1997年9月
  - Active Server Pages 3.0 (IIS 5.0) 2000年11月

## ASPによるプログラムの例

例1: [Hello worldの文字列を出力させる](../Page/Hello_world.md "wikilink")。

``` asp
<html>
 <body>
  <% Response.Write("Hello world") %>
 </body>
</html>
```

例2: 今日の日付をスクリプト言語を用いて出力させる。

``` asp
<%@ Language="JavaScript" %>
<html>
 <body>
  今日は<%= Date() %>です。
 </body>
</html>
```

## Apache::ASPについて

ASPは基本的にMicrosoftのhttpサーバ以外では使えないが、[Apache::ASP](http://www.apache-asp.org/)を使うと、限定的ではあるが[Apache上で](../Page/Apache_HTTP_Server.md "wikilink")[Perl](../Page/Perl.md "wikilink")を用いたASPを扱えるようになる（Perl以外のスクリプトはサポートしない）。

## 関連項目

  - [JScript](../Page/JScript.md "wikilink")
  - [VBScript](../Page/VBScript.md "wikilink")

## 外部リンク

  - [Active Server Pages](https://msdn.microsoft.com/en-us/library/aa286483.aspx): MSDNライブラリ

[Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink") [Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink")