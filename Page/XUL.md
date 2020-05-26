> この記事は[XUL](https://ja.wikipedia.org/wiki/XUL)から翻訳されています。


**XUL**（ズール、XML User Interface Language）は[Mozilla Firefoxや](../Page/Mozilla_Firefox.md "wikilink")[Mozilla Thunderbirdなどの](../Page/Mozilla_Thunderbird.md "wikilink")[Mozilla](../Page/Mozilla.md "wikilink")[アプリケーションを作成するための](../Page/アプリケーションソフトウェア.md "wikilink")[ユーザインタフェースマークアップ言語](https://ja.wikipedia.org/wiki/ユーザインタフェースマークアップ言語 "wikilink")である。[UIML](https://ja.wikipedia.org/wiki/UIML "wikilink")のような[XML](../Page/Extensible_Markup_Language.md "wikilink")[アプリケーションの一つであり](../Page/アプリケーションソフトウェア.md "wikilink")、[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")を記述するための言語である。

XUL自体は標準とはなっていないが、[CSS](../Page/Cascading_Style_Sheets.md "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")、[DOM](../Page/Document_Object_Model.md "wikilink")、[DTD](../Page/Document_Type_Definition.md "wikilink")、[RDF等の既存の標準技術を多く利用しているため](../Page/Resource_Description_Framework.md "wikilink")、すでにこれらの技術に親しんでいる[プログラマ](../Page/プログラマ.md "wikilink")や[デザイナにとっては比較的習得しやすい言語となっている](https://ja.wikipedia.org/wiki/Webデザイナー "wikilink")。

## 概要

XULによる[インタフェースは](../Page/インタフェース_\(情報技術\).md "wikilink")3つの別個に独立したコンポーネントのグループによって記述される。

  - Content（コンテント） : ユーザインタフェースのレイアウトを規定するXUL本文。
    Skin（[スキン](https://ja.wikipedia.org/wiki/スキン "wikilink")） : アプリケーションの視覚的な表現を行うためのCSSや画像。
    Locale（[ロケール](https://ja.wikipedia.org/wiki/ロケール "wikilink")） : ソフトウェアの[ローカライズ](https://ja.wikipedia.org/wiki/ローカライズ "wikilink")を容易にするための実体テキスト を記述する[DTD](../Page/Document_Type_Definition.md "wikilink")。

XULの持つ最も大きな利点は単純でポータブルな[ウィジェットの記述が可能であることである](../Page/ウィジェット_\(GUI\).md "wikilink")。これは第4世代言語 ([4GL](../Page/4GL.md "wikilink")) がソフトウェア開発の場で果たしたのとよく似た労力の削減に繋がっている。

## XULのエレメント（要素）

XULの仕様はたくさんの種類の要素を規定している。これらは大まかに以下のように分類できる。

  - トップレベル要素 : [ウィンドウ](../Page/ウィンドウ.md "wikilink")、[ページ](../Page/ページ.md "wikilink")、[ダイアログ](https://ja.wikipedia.org/wiki/ダイアログ "wikilink")、[ウィザードなど](../Page/ウィザード_\(ソフトウェア\).md "wikilink")
    ウィジェット : ラベル、[ボタン](../Page/ボタン_\(GUI\).md "wikilink")、[テキストボックス](../Page/テキストボックス.md "wikilink")、リストボックス（[コンボボックス](https://ja.wikipedia.org/wiki/コンボボックス "wikilink")）、[ラジオボタン](https://ja.wikipedia.org/wiki/ラジオボタン "wikilink")、[チェックボックス](../Page/チェックボックス.md "wikilink")、ツリー、[メニュー](../Page/メニュー_\(コンピュータ\).md "wikilink")、[ツールバー](https://ja.wikipedia.org/wiki/ツールバー "wikilink")、グループボックス、[タブ](../Page/タブ_\(GUI\).md "wikilink")、カラーピッカー、スペーサー、スプリッターなど
    ボックスモデル : ボックス、グリッド、スタック、デッキなど
    イベントとスクリプト : [スクリプト](../Page/スクリプト言語.md "wikilink")、コマンド、キーボード、ブロードキャスター、オブザーバなど
    [データソース](https://ja.wikipedia.org/wiki/データソース "wikilink") : テンプレート、ルールなど
    その他 : オーバーレイ（[クライアントサイド](../Page/クライアントサイド.md "wikilink")で行われる[Server Side Includes](https://ja.wikipedia.org/wiki/Server_Side_Includes "wikilink")）、インラインフレーム、[ブラウザ](https://ja.wikipedia.org/wiki/ブラウザ "wikilink")、[エディタ](https://ja.wikipedia.org/wiki/エディタ "wikilink")など

XULの記述の中に[XHTMLや](../Page/Extensible_HyperText_Markup_Language.md "wikilink")[MathMLのような別のXMLアプリケーションによる要素を含めることも可能となっている](../Page/Mathematical_Markup_Language.md "wikilink")。

一般的なウィジェットの中でもたとえばスピンボックス、スライダー、キャンバスなどは現在のXULの仕様では使用できないがこれらはXUL 2.0での検討課題に含められている[1](https://wiki.mozilla.org/XUL:Home_Page)。

## 使い方

XULは主に[Mozilla](../Page/Mozilla.md "wikilink")や[Firefox本体やこれらの拡張のために使われているが](../Page/Mozilla_Firefox.md "wikilink")、[HTTPで転送される](../Page/Hypertext_Transfer_Protocol.md "wikilink")[ウェブアプリケーション](https://ja.wikipedia.org/wiki/ウェブアプリケーション "wikilink")に使うこともできる。例えば、XULアプリケーションとしてMozilla Amazon Browserという、[Amazon.com](../Page/Amazon.com.md "wikilink")で本を探すための[リッチクライアント](https://ja.wikipedia.org/wiki/リッチクライアント "wikilink")ソフトにも使われている。しかしながら、Mozillaの強力な特徴である[XPCOM](../Page/XPCOM.md "wikilink")オブジェクトを使う権限は、セキュリティの観点から、リモートのXULドキュメントには与えられない（署名がされていない限り権限が与えられない）。また他の制限もあり、例えば他ドメインの外部のXULや[DTDや](../Page/Document_Type_Definition.md "wikilink")[RDFドキュメントを読み込むことができない](../Page/Resource_Description_Framework.md "wikilink")。

## 映画との関連

<table>
<tbody>
<tr class="odd">
<td><p>THERE IS NO DATA.<br />
THERE IS ONLY <span class=plainlinks><a href="https://developer.mozilla.org/en-US/docs/Archive/Mozilla/XUL">XUL</a></span>.</p></td>
</tr>
</tbody>
</table>

XULという名前は映画『[ゴーストバスターズ](../Page/ゴーストバスターズ.md "wikilink")』に由来する。映画にて古代[シュメール](../Page/シュメール.md "wikilink")人の女神ズール (Zuul) の亡霊は、[シガニー・ウィーバー](../Page/シガニー・ウィーバー.md "wikilink")演ずるデーナ・バレット (Dana Barrett) に[憑依](../Page/憑依.md "wikilink")し、「There is no Dana, only Zuul（デーナはいない。ズールしかいない）」と宣言している。XULでは、本来文書やデータの構造などを記述するための言語であるマークアップ言語（を創るための仕様であるXML）をインタフェースを定義するために利用していることから、XULの開発者は映画のセリフをもじって「There is no data, only XUL（データはない。XULしかない）」というスローガンを掲げている。そしてこれはXULアプリケーションで[XML名前空間の宣言記述に用いられる](https://ja.wikipedia.org/wiki/Extensible_Markup_Language#XML名前空間 "wikilink")[URI](../Page/Uniform_Resource_Identifier.md "wikilink")：<https://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul>に記述された文章でもある。XULが使用可能なアプリケーションでこのアドレスを開くと、（図のように）このスローガンが画面中央に大きな文字で表示されるようになっている。

"keymaster" や "gatekeeper" も同作品のシナリオに由来する。『ゴーストバスターズ』からのもじりはMozillaの他のプロダクトでも見られ、例えばJavaScriptには[Venkman](https://developer.mozilla.org/Ja/Venkman)という[デバッガ](../Page/デバッガ.md "wikilink")コンポーネントがあるが、これは同作品の主人公の1人、ピーター・ヴェンクマン博士に由来する。

## 関連項目

  - [XULRunner](../Page/XULRunner.md "wikilink")
  - [レイアウトマネージャ](../Page/レイアウトマネージャ.md "wikilink")
  - [Extensible Application Markup Language](../Page/Extensible_Application_Markup_Language.md "wikilink")（XAML）

## 外部リンク

  - [Mozilla XUL](https://developer.mozilla.org/en-US/docs/Archive/Mozilla/XUL) - Mozilla.orgのXUL公式ホームページ（英文）
  - [Xul Runner](https://wiki.mozilla.org/XULRunner) - An attempt to run XUL applications in a light-weight container.
  - [XUL Wiki](http://wiki.fdiary.net/xul/) - XULアプリケーションや拡張機能開発関係に関する日本語の情報
  - [Xul](https://www.xul.fr/xul.html) and [Xul Dev project](http://xuldev.sf.net)

[Category:ウェブブラウザ](https://ja.wikipedia.org/wiki/Category:ウェブブラウザ "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink") [Category:コンピュータのユーザインタフェース](https://ja.wikipedia.org/wiki/Category:コンピュータのユーザインタフェース "wikilink") [Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink")