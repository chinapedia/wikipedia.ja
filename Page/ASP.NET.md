> この記事は[ASP.NET](https://ja.wikipedia.org/wiki/ASP.NET)から翻訳されています。


**ASP.NET**は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が開発・提供しているWebアプリケーションフレームワークで、動的なウェブサイトや[Webアプリケーションや](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")[Webサービス](https://ja.wikipedia.org/wiki/Webサービス "wikilink")の開発や運用を行う。ASP.NETは[Active Server Pagesを](../Page/Active_Server_Pages.md "wikilink")[.NET向けにしたものである](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")。

ASP.NETのもとには、ウェブサイト・ウェブアプリケーションの作成するために3種類のフレームワークが用意されている\[1\]。

  - ASP.NET Webフォーム
  - [ASP.NET MVC](https://ja.wikipedia.org/wiki/ASP.NET_MVC_Framework "wikilink")
  - ASP.NET Webページ

このほか、Web API作成に特化した[ASP.NET Web API](https://ja.wikipedia.org/wiki/ASP.NET_Web_API "wikilink")、リアルタイム処理のための[ASP.NET SignalRといったフレームワークが存在する](https://ja.wikipedia.org/wiki/Microsoft_ASP.NET_SignalR "wikilink")。

このほか、[.NET Core上で動作する](https://ja.wikipedia.org/wiki/.NET_Core "wikilink")が新たに開発されている。

## ASP.NET Webフォームの特徴

ASP.NETは、それまでのWebアプリケーション構築の常識であった、[HTMLの知識や](../Page/HyperText_Markup_Language.md "wikilink")[HTTP通信の仕組み](../Page/Hypertext_Transfer_Protocol.md "wikilink")、ブラウザとサーバー間のデータのやりとりなどを抽象化して、[GUIモデルによるアプリケーション開発が行えるようになっている](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。ページデザインは、以前のASPと同じようにHTMLを直接記述することもできるが、Visual Studioなどの開発環境を用いることでGUIによるページデザインが行えるようになっている。また、HTTP POSTの仕組みを利用したPostBackと呼ばれる仕組みを使うことによって、[イベント駆動型プログラミング](../Page/イベント駆動型プログラミング.md "wikilink")を実現している。

内部の仕組みは抽象化されているが、実際にはHTMLやHTTP、[JavaScript](../Page/JavaScript.md "wikilink")など従来のモデルを使用しているため、通常のWebアプリケーションと同様にWebブラウザで表示できるというメリットがある。ただしその反面、WebブラウザやHTTPの制約に考慮して開発することが必要なのは従来通りであるため、Webアプリケーションが分からないプログラマでもWebアプリケーションを開発できるようになる魔法の杖では決してない。

また、ブラウザを認識して最適なHTMLを生成するほか、実行時に前回に実行したものと比べ変更があるときにのみ[コンパイルをしてキャッシュしておくため](../Page/コンパイラ.md "wikilink")、ASPと比べ処理速度が向上している。

ASPは[SSIから呼び出すことができるが](https://ja.wikipedia.org/wiki/Server_Side_Includes "wikilink")、ASP.NETは呼び出せない。

## ASP.NETの動作

IISではASP.NETはaspnet_isapi.dllというファイルが[ISAPI](../Page/ISAPI.md "wikilink")を利用して動作している。ASP.NETの動作に関する設定の多くは、\*.configファイルを利用している。事前にコンパイルされたファイルまたはDLLやコンパイルされていないファイルを指定したディレクトリに置くだけで動作する。

  - ASP.NETで使用するクラスの多くは、以下の名前空間で定義されている。

<!-- end list -->

    System.Web
    System.Web.UI

## ASP.NETで利用できる言語

Visual Studioでは、[Visual Basicや](../Page/Visual_Basic.md "wikilink")[C\#を既定の言語として選択するようになっているが](../Page/C_Sharp.md "wikilink")、最終的にはコンパイルされたアセンブリで動作するため、[C++/CLI](https://ja.wikipedia.org/wiki/C++/CLI "wikilink")や[JScript.NETなど](https://ja.wikipedia.org/wiki/JScript#JScript_.NET "wikilink")[.NET](https://ja.wikipedia.org/wiki/.NET "wikilink")に対応した言語であれば様々な言語で記述することもできる。

## 拡張子

  - aspx ファイル
    一般的なウェブフォームページ
  - asax ファイル
    アプリケーションレベルのロジックとイベントハンドリングの構築
  - ascx ファイル
    オリジナルのユーザコントロールをウェブページで利用する場合に用いる
  - ashx ファイル
    独自のHTTPハンドラの構築
  - asmx ファイル
    ウェブサービスのページの構築
  - axd ファイル
    アプリケーションレベルでのトレーシングのためのファイル
  - browser ファイル
    Webサイトが許容するブラウザの構成を保存するファイル
  - config ファイル
    Webアプリケーションの設定を記述するXML形式のファイル
  - cs/vb ファイル
    コンパイル前のソースファイル。前者はC\#言語で、後者はVisual Basic言語で記述される
  - master ファイル
    ページに統一的なデザインを設定するマスターページファイル
  - sitemap ファイル
    サイトマップの設定ファイル
  - skin ファイル
    Webページのテーマスキンの構築
  - resx ファイル
    ファイルの国際化（グローバリゼーション）や地域化（ローカリゼーション）する場合のリソースファイル

## ディレクトリ構造

  - App_Code
    \*.csや\*.vbなどのソースファイルを配置するディレクトリ
  - App_LocalResources
    個々にばらばらになった地域化されたファイルを配置するディレクトリ
  - App_GlobalResources
    たくさんのページの地域化するリソース (`*.resx`) を配置するディレクトリ
  - App_Themes
    テーマファイルの配置するディレクトリ
  - App_Browsers
    サイトの仕様に沿ったブラウザの定義を配置する `*.browser` ファイルを配置するディレクトリ
  - bin
    ASP.NETで利用するバイナリファイルの配置に用いるディレクトリ

## ASP.NETの文法

ASP.NETでは普通、コード表示ブロック (`<% %>`)をbody要素内で使わない。 (コード表示ブロックを使用して、インラインコードを埋め込むこともできる。)

例1: Hello, Worldの文字列を出力させる（例題の言語は[Visual Basic](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink"))。

``` asp
 <%@ Page Language="VB" %>
 <script runat="server">
     Private Sub Page_Load()
         Label1.Text = "Hello, World"
     End Sub
 </script>
 <html>
  <body>
   <form runat="server">
    <asp:Label id="Label1" />
   </form>
  </body>
 </html>
```

例2: コードを別のファイルに記述する。

Default.aspx

``` asp
 <%@ Page Language="VB" CodeFile="Default.aspx.vb" Inherits="_Default" %>
 <html>
  <body>
   <form runat="server">
    <asp:Label id="Label1" />
   </form>
  </body>
 </html>
```

Default.aspx.vb

``` vbnet
 Partial Class _Default
     Inherits System.Web.UI.Page
     Private Sub Page_Load(ByVal sender As Object, ByVal e As System.EventArgs) Handles Me.Load
         Label1.Text = "Hello, World"
     End Sub
 End Class
```

## 開発ツール

  - [Microsoft Expression Web](../Page/Microsoft_Expression_Web.md "wikilink")
  - [Microsoft Visual Studio](https://ja.wikipedia.org/wiki/Microsoft_Visual_Studio "wikilink")
  - [Microsoft Visual Web Developer](../Page/Microsoft_Visual_Web_Developer.md "wikilink")
  - [Microsoft SharePoint Designer](https://ja.wikipedia.org/wiki/Microsoft_SharePoint_Designer "wikilink")
  - [Adobe Dreamweaver](https://ja.wikipedia.org/wiki/Adobe_Dreamweaver "wikilink") MX
  - [ASP.NET Web Matrix](https://ja.wikipedia.org/wiki/ASP.NET_Web_Matrix "wikilink")
  - [MonoDevelop](https://ja.wikipedia.org/wiki/MonoDevelop "wikilink")
  - [SharpDevelop](../Page/SharpDevelop.md "wikilink")
  - [Delphi 2006](../Page/Delphi.md "wikilink")

## 展開プラットフォーム

  - [Internet Information Services](../Page/Internet_Information_Services.md "wikilink")
  - [XSP (Webサーバ)](https://ja.wikipedia.org/wiki/XSP_\(Webサーバ\) "wikilink")
  - [Apache HTTP Server](../Page/Apache_HTTP_Server.md "wikilink") - （mod_mono を利用、暗黙的に[XSPがバックグラウンドで動作する](https://ja.wikipedia.org/wiki/XSP_\(Webサーバ\) "wikilink")）

## フレームワーク

  - [Castle Monorail](https://ja.wikipedia.org/wiki/Castle_Monorail "wikilink")
  - [Spring.NET](https://ja.wikipedia.org/wiki/Spring.NET "wikilink")
  - [Skaffold.NET](https://ja.wikipedia.org/wiki/Skaffold.NET "wikilink")

## 関連項目

  - [.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [ASP.NET AJAX](https://ja.wikipedia.org/wiki/ASP.NET_AJAX "wikilink")
  - [ASP.NET MVC Framework](https://ja.wikipedia.org/wiki/ASP.NET_MVC_Framework "wikilink")

## 脚注

## 外部リンク

  -
  - [ASP.NET のドキュメント](https://docs.microsoft.com/ja-jp/aspnet/#pivot=aspnet&panel=aspnet_overview)

  - [Microsoft Web 開発 ガイドライン ～ ASP.NET プログラミング エッセンシャル ～](https://download.microsoft.com/download/7/c/e/7ce5cc56-f897-42b0-9e49-7301b451ae87/webdevelopmentguideline_rev1.pdf)　

  - [CodePlex - ASP.NET](http://aspnet.codeplex.com/)

  - [ASP.NET MVC 2 サンプル ソースコード](http://edtter.codeplex.com)

{{.NET}}

[Category:Windowsのコンポーネント](https://ja.wikipedia.org/wiki/Category:Windowsのコンポーネント "wikilink") [Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:.NET_Framework](https://ja.wikipedia.org/wiki/Category:.NET_Framework "wikilink") [Category:ウェブアプリケーションフレームワーク](https://ja.wikipedia.org/wiki/Category:ウェブアプリケーションフレームワーク "wikilink")

1.