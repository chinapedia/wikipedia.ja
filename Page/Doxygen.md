> この記事は[Doxygen](https://ja.wikipedia.org/wiki/Doxygen)から翻訳されています。


**Doxygen**（ドキシジェン）は、[C++](../Page/C++.md "wikilink")、[C言語](../Page/C言語.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[Objective-C](../Page/Objective-C.md "wikilink")、[Python](../Page/Python.md "wikilink")、[IDL](../Page/インタフェース記述言語.md "wikilink")（[CORBAおよびマイクロソフト形式](../Page/Common_Object_Request_Broker_Architecture.md "wikilink")）のための[ドキュメンテーションジェネレータ](https://ja.wikipedia.org/wiki/ドキュメンテーションジェネレータ "wikilink")である。他にも[PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")、[C\#](../Page/C_Sharp.md "wikilink")、[D言語](../Page/D言語.md "wikilink")、[ActionScript](../Page/ActionScript.md "wikilink")でもある程度利用可能。多くの[Unix系](../Page/Unix系.md "wikilink")システム、[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で動作する。Doxygenのコードの大部分は Dimitri van Heesch が書いた。

[KDE](../Page/KDE.md "wikilink")は文書の一部にDoxygenを利用しており、[KDevelop](../Page/KDevelop.md "wikilink")は組み込みでサポートしている。

## 概要

[Javadoc](../Page/Javadoc.md "wikilink")のように、Doxygenはソースファイルのコメントから文書を抜き出す。Javadocの文法に加えて、[Qt](../Page/Qt.md "wikilink")ツールキットで使われるドキュメンテーションタグをサポートしており、[HTML形式だけでなく](../Page/HyperText_Markup_Language.md "wikilink")、[CHM](https://ja.wikipedia.org/wiki/Microsoft_Compressed_HTML_Help "wikilink")、[RTF](../Page/Rich_Text_Format.md "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[LaTeX](../Page/LaTeX.md "wikilink")、[PostScript](../Page/PostScript.md "wikilink")、[manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")形式の文書を生成できる。

## コード例

以下のコード例は、Doxygenで文書生成可能な形式である。

`/**`
` * The time class represents a moment of time.`
` *`
` * `*`\author`*` John Doe`
` */`
**`class`**` Time {`

`  /**`
`   * Constructor that sets the time to a given value.`
`   * `*`\param`*` `**`timemillis`**` is a number of milliseconds passed since Jan 1. 1970`
`   */`
`  Time(`**`int`**` timemillis) {`
`    ...`
`  }`

`  /**`
`   * Get the current time.`
`   * `*`\return`*` A time object set to the current time.`
`   */`
`  `**`static`**` Time now() {`
`    ...`
`  }`
`};`

## 関連項目

  - [ソフトウェアドキュメンテーション](../Page/ソフトウェアドキュメンテーション.md "wikilink")
  - [Eclox](http://home.gna.org/eclox/) : [Eclipse向けのDoxygen](../Page/Eclipse_\(統合開発環境\).md "wikilink")[フロントエンド](../Page/フロントエンド.md "wikilink")[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")。[GNU General Public Licenseでライセンスされている](../Page/GNU_General_Public_License.md "wikilink")。
  - [Graphviz](../Page/Graphviz.md "wikilink") : DoxygenはC++、Java、Pythonなどについてクラス階層図などをGraphVizと連携して生成できる。

## 外部リンク

  - [Sourceforge homepage](http://sourceforge.net/projects/doxygen/)
  - [MediaWiki documentation](http://svn.wikimedia.org/doc/) Doxygen で作成

[Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink")