> この記事は[Texinfo](https://ja.wikipedia.org/wiki/Texinfo)から翻訳されています。


[GNU](../Page/GNU.md "wikilink") **Texinfo** (テックインフォ) は、[フリーな](../Page/フリーソフトウェア.md "wikilink")[コンピュータ・プログラム](../Page/プログラム_\(コンピュータ\).md "wikilink") であり、一式の[ソースコード](../Page/ソースコード.md "wikilink")から複数の[形式で文書を生成する](../Page/ファイルフォーマット.md "wikilink")。また、[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")で公式の文書体系として用いられている。 Texinfo は、言語の構文や、このアプリケーションの入力用ソースファイルを指してもいう。

## Texinfoのソース・ファイル

Texinfoは、章、節、相互参照、索引のある本のような文書を構成できる。 ソースは、ほぼ [プレーンテキスト](../Page/プレーンテキスト.md "wikilink") だが、厳密には「`@`」から始まるコマンドで [フォーマットしたテキスト](../Page/マルチスタイルテキスト.md "wikilink") である。 部分的なソース・ファイルの例は、次のとおり:

`@ifnottex`
`@node Top`
`@top Short Sample`

`@insertcopying`
`@end ifnottex`

`@menu`
`* First Chapter::    The first chapter is the`
`                     only chapter in this sample.`
`* Index::            Complete index.`
`@end menu`

このコマンド群は、章といった構造を表したり、一定の出力種類だけで処理される部分的なソースを示したりしている。

## 出力の生成

Texinfoのサポートする出力形式には、 [プレーンテキスト](../Page/プレーンテキスト.md "wikilink")、[info](https://ja.wikipedia.org/wiki/info "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[DVI](https://ja.wikipedia.org/wiki/DVI_\(ファイルフォーマット\) "wikilink")、[PDF](../Page/Portable_Document_Format.md "wikilink")、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[DocBook](../Page/DocBook.md "wikilink")がある。

印刷のできる形式として、Texinfoは、[TeX](../Page/TeX.md "wikilink")を使っている。これは、TexinfoのコマンドをTeX自体に解釈させるのに必要な命令の発行による。

出力形式に [manページ](https://ja.wikipedia.org/wiki/manページ "wikilink")のないことに注意してほしい。Texinfo は、[GNU/Linuxといった](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink") [Unix系](../Page/Unix系.md "wikilink")環境で典型的に使われている [GNU](../Page/GNU.md "wikilink")ソフトウェアの文書を書くのに使うが、そういった環境の伝統的文書形式はmanページである。manページには、きっちりした慣例の形式がある一方、Texinfoの典型的適用例は、入門書や参照マニュアルである。伝統的にクイック・リファレンス・マニュアルであるようなmanページに Texinfoを使っても、利点はない。GNUプロジェクトの多くのプロジェクトは、manページを避けているが、infoのページを参照するように書いたきり放置したmanページもある。

## 脚注

## 外部リンク

  - [Texinfo](http://www.gnu.org/software/texinfo/) (公式)

[Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:TeX](https://ja.wikipedia.org/wiki/Category:TeX "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ハイパーテキスト](https://ja.wikipedia.org/wiki/Category:ハイパーテキスト "wikilink") [Category:ソフトウェア開発ツール](https://ja.wikipedia.org/wiki/Category:ソフトウェア開発ツール "wikilink")