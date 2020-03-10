> この記事は[ISAPI](https://ja.wikipedia.org/wiki/ISAPI)から翻訳されています。


**Internet Server Application Programming Interface** (**ISAPI**) は、[マイクロソフト](../Page/マイクロソフト.md "wikilink")の[Windows NT系に付属](../Page/Microsoft_Windows_NT.md "wikilink")（一部除く）する[IISの](../Page/Internet_Information_Services.md "wikilink")[n層API](https://ja.wikipedia.org/wiki/多層アーキテクチャ "wikilink")。主に[Webサーバ](../Page/Webサーバ.md "wikilink")として利用されている。

[Apacheにおいても](../Page/Apache_HTTP_Server.md "wikilink")、`mod_isapi`を利用することにより、IISのISAPIと互換性のある環境を構築できる。

## ISAPI アプリケーション

ISAPIはExtensionsとFiltersの2つの構成要素からなる。これら2つの構成要素は[C++](../Page/C++.md "wikilink")での開発となる。また、作成した[DLLファイルはIISに登録しなければならない](../Page/ダイナミックリンクライブラリ.md "wikilink")。

### ISAPI Extensions

IIS Extensionsを利用すると、プログラムはIIS上で動作する。また、IIS ExtensionsはIISの全ての機能を利用することができるようになる。

### ISAPI Filters

IIS FiltersはIISの機能強化、または機能の修正を行うために用いられる。IIS Filtersを利用してデータの入出力を作成したプログラムが行えるようになる。

作成したプログラムはDLLファイルで、IISにサイトレベル、または管理下にある全てのIISに登録する。

ISAPI Filtersを利用して、主に以下の様なジョブが利用されている。

  - クライアントからのURLやHTTPヘッダのリクエスト解析
  - 匿名または基本認証のコントロール
  - 独自のアクセス拒否(HTTP 403)の応答
  - トラフィック解析
  - 独自の認証
  - 暗号化や圧縮

等、多様なジョブを実行できる。

### 代表的な ISAPI アプリケーション

  - [Active Server Pages](../Page/Active_Server_Pages.md "wikilink")
  - [ASP.NET](https://ja.wikipedia.org/wiki/ASP.NET "wikilink")
  - [Perl](../Page/Perl.md "wikilink") ISAPI
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")

## ISAPI 開発

ISAPIを利用してのアプリケーション開発は、[Visual C++](https://ja.wikipedia.org/wiki/Microsoft_Visual_C++ "wikilink") 4.0からサポートされている。Wizardを利用してISAPIフレームワークを作成できる。開発は主に[MFCを利用して開発する](https://ja.wikipedia.org/wiki/Microsoft_Foundation_Class "wikilink")。

[Category:マイクロソフトのAPI](https://ja.wikipedia.org/wiki/Category:マイクロソフトのAPI "wikilink") [Category:Microsoft_server_technology](https://ja.wikipedia.org/wiki/Category:Microsoft_server_technology "wikilink")