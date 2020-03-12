> この記事は[DOM Inspector](https://ja.wikipedia.org/wiki/DOM_Inspector)から翻訳されています。


**DOM Inspector**（-インスペクタ）はMozilla Application SuiteやMozilla Firefoxなどに同梱される開発者向けツールである。[HTMLや](../Page/HyperText_Markup_Language.md "wikilink")[XMLで書かれた文書の](../Page/Extensible_Markup_Language.md "wikilink")[DOMを解析することを主な目的とする](../Page/Document_Object_Model.md "wikilink")。

DOMノードは解析対象を選択してからツリー構造を展開したりブラウザペインの特定部分をクリックしたりすることで特定部分を選択できる。DOMノードの他にBoxモデル（位置関係の解析）やXBLバインディング、[CSSセレクタ](../Page/Cascading_Style_Sheets.md "wikilink")・プロパティ・値の解析、[Gecko](../Page/Gecko.md "wikilink")が解析対象に対して定義済みのスタイル、[JavaScript](../Page/JavaScript.md "wikilink")オブジェクトなどの解析結果も表示できるようになっている。CSSとJavaScriptオブジェクトはツリーから選択することが可能で、アクティブなエレメントは赤い枠で点滅表示されるためCSSの[デバッグ](../Page/デバッグ.md "wikilink")を行うのに有効な手段となっている。

## DOM Inspectorを使用するソフトウェア

  - プリインストール

インストーラ同梱。インストール時の設定でDOM Inspectorをインストールするかしないか選択できるようになっており、必要がなければインストールしないこともできる。

  - [Mozilla Application Suite](../Page/Mozilla_Application_Suite.md "wikilink")
      - [SeaMonkey](../Page/SeaMonkey.md "wikilink")
  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")
  - [Netscape Navigator](https://ja.wikipedia.org/wiki/Netscape_Navigator "wikilink")

<!-- end list -->

  - 追加インストール

Thunderbirdは[Mozilla Add-onsにて提供されている専用の](../Page/Mozilla_Add-ons.md "wikilink")[DOM Inspector](https://addons.mozilla.org/thunderbird/addon/1806)をインストールすることで利用可能になる。

  - [Mozilla Thunderbird](../Page/Mozilla_Thunderbird.md "wikilink")

## 使用例

  - HTML構造の解析
    ツリー構造の展開によりどの要素の中にどの要素が包括されているか、どの要素にどんな属性が割り当てられているかなどを参照できる。
  - ブラウザのカスタマイズ
    メニュー項目やセパレータなどに割り当てられたコマンドやidなどを解析する。解析したidはuserChrome.cssから参照することでメニュー項目を非表示にしたり装飾を変更したるすることが可能。また、アクションは拡張機能のkeyconfigを用いることでキーボードショートカットを新規に割り当てることが可能となる。

## 関連項目

  - [Mozilla Application Suite](../Page/Mozilla_Application_Suite.md "wikilink")
  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")
  - [Mozilla Thunderbird](../Page/Mozilla_Thunderbird.md "wikilink")
  - [SeaMonkey](../Page/SeaMonkey.md "wikilink")
  - [Netscape Navigator](https://ja.wikipedia.org/wiki/Netscape_Navigator "wikilink")
  - [Gecko](../Page/Gecko.md "wikilink")
  - [拡張機能](../Page/拡張機能_\(Mozilla\).md "wikilink")
  - [HTML](../Page/HyperText_Markup_Language.md "wikilink")
  - [XML](../Page/Extensible_Markup_Language.md "wikilink")
  - [CSS](../Page/Cascading_Style_Sheets.md "wikilink")

## 外部リンク

  - [DOMインスペクタ](http://www.mozilla-japan.org/projects/inspector/)
  - [DOM Inspector - MDC](http://developer.mozilla.org/ja/docs/DOM_Inspector)
  - [DOM Inspector - MozillaWiki](https://ja.wikipedia.org/wiki/MozillaWiki:DOM_Inspector "wikilink")

[Category:Mozilla](https://ja.wikipedia.org/wiki/Category:Mozilla "wikilink") [Category:拡張機能_(Mozilla)](https://ja.wikipedia.org/wiki/Category:拡張機能_\(Mozilla\) "wikilink")