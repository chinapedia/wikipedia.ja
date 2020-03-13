> この記事は[XML Paper Specification](https://ja.wikipedia.org/wiki/XML_Paper_Specification)から翻訳されています。


**XML Paper Specification** (**XPS**) は、[ページ記述言語](../Page/ページ記述言語.md "wikilink")のひとつで、[マイクロソフト](../Page/マイクロソフト.md "wikilink")が [Windows Vista](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink") から採用したドキュメント ファイル形式である。2009年6月に ECMA-388 Open XML Paper Specification (OpenXPS) として国際標準規格となった。

## XPS の開発

かつてのコード名は「Metro」といった。配布形態、記録方式、レンダリング等の形式が規定されており、その[マークアップ言語](../Page/マークアップ言語.md "wikilink")は [Windows Presentation Foundation](../Page/Windows_Presentation_Foundation.md "wikilink") による [Extensible Application Markup Language](../Page/Extensible_Application_Markup_Language.md "wikilink") (XAML) の[サブセット](https://ja.wikipedia.org/wiki/サブセット "wikilink")である。結果として Windows アプリケーションのレンダリング手法がそのまま XPS 文書にも使用可能となる。

XPS は [Adobe](../Page/アドビシステムズ.md "wikilink") 主導の [Portable Document Format](../Page/Portable_Document_Format.md "wikilink") (PDF) に対抗するものだが、PDF と異なり動的コンテンツを含むことが出来ない。あくまでも静的な電子文書である。マイクロソフトは[2007年](../Page/2007年.md "wikilink")[6月1日](../Page/6月1日.md "wikilink")までに XPSDrv ソリューションに対し付加機能の追加を行う旨のコメントをした。

## OpenXPS の開発

2007年6月に Ecma International の技術委員会 (Technical Committee) 46 (TC46) が立ちあげられ、XPS の標準化作業が開始された。TC46 のメンバーは [Autodesk](../Page/オートデスク.md "wikilink")、[Brother](https://ja.wikipedia.org/wiki/ブラザー工業 "wikilink")、[Canon](https://ja.wikipedia.org/wiki/キヤノン "wikilink")、[Fujifilm](../Page/富士フイルム.md "wikilink")、[Fujitsu](../Page/富士通.md "wikilink")、[Global Graphics](https://ja.wikipedia.org/wiki/Global_Graphics "wikilink")、[Hewlett-Packard](../Page/ヒューレット・パッカード.md "wikilink")、[Konica Minolta](https://ja.wikipedia.org/wiki/コニカミノルタホールディングス "wikilink")、[Lexmark](../Page/レックスマーク.md "wikilink")、Microsoft、[Monotype Imaging](https://ja.wikipedia.org/wiki/Monotype_Imaging "wikilink")、[Océ](https://ja.wikipedia.org/wiki/Océ "wikilink")、[Pagemark](https://ja.wikipedia.org/wiki/Pagemark "wikilink")、[Panasonic](https://ja.wikipedia.org/wiki/パナソニック "wikilink")、[QualityLogic](https://ja.wikipedia.org/wiki/QualityLogic "wikilink")、[Ricoh](../Page/リコー.md "wikilink")、[Software Imaging](https://ja.wikipedia.org/wiki/Software_Imaging "wikilink")、[Toshiba](../Page/東芝.md "wikilink")、[Xerox](https://ja.wikipedia.org/wiki/Xerox "wikilink")、[Zoran](https://ja.wikipedia.org/wiki/Zoran_Corporation "wikilink") で構成された\[1\]。 2009年6月に OpenXPS として XPS とはいくらか互換性がないが規格が決定した\[2\]。

| 変更点              | OpenXPS 1st Edition  | XPS                               |
| ---------------- | -------------------- | --------------------------------- |
| スキーマの URI 名前空間   | XPS と OpenXPS では異なる  |                                   |
| Content Type     | application/oxps を推奨 | application/vnd.ms-xpsdocument のみ |
| 拡張子              | \*.`oxps` を推奨        | \*.`xps` のみ                       |
| X3D の実装          | オプションである             | 既に実装している                          |
| カラー プロファイルの相互運用性 | 仕様が厳密である             | 仕様が厳密ではない                         |
| 独自の参照の仕組みの削除     | 参照不可                 | 参照可                               |

OpenXPS と XPS の違い\[3\]

## ソフトウェアとハードウェアのサポート

今日主流の [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") では XPS の閲覧および出力をサポートしている。マイクロソフト以外の XPS の取り扱いは、ソフトウェアとハードウェアのいずれかまたは両方での対応が増えてきている\[4\]。Windows 以外の環境、Mac OS X や GNU/Linux 環境においても、[KDE](../Page/KDE.md "wikilink") プロジェクトの [Okular](https://ja.wikipedia.org/wiki/Okular "wikilink") や [NiXPS](https://ja.wikipedia.org/wiki/NiXPS "wikilink") をはじめ、XPS に対応したものがある。

## 脚注

## 関連項目

  - [XSL Formatting Objects](../Page/XSL_Formatting_Objects.md "wikilink")

## 外部リンク

  - [Standard ECMA-388](http://www.ecma-international.org/publications/standards/Ecma-388.htm)

  -
<!-- end list -->

  - [STDU Viewer](http://www.stdutility.com/stduviewer.html)

[Category:ページ記述言語](https://ja.wikipedia.org/wiki/Category:ページ記述言語 "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:XMLベースの技術](https://ja.wikipedia.org/wiki/Category:XMLベースの技術 "wikilink")

1.
2.
3.
4.  [XPS テクノロジ ショーケース](http://www.microsoft.com/japan/whdc/xps/showcase.mspx)