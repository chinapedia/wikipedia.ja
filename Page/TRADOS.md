> この記事は[TRADOS](https://ja.wikipedia.org/wiki/TRADOS)から翻訳されています。


**SDL Trados Studio**は、一般的に「トラドス」と呼ばれる翻訳支援ソフトウェア。

元々はトラドス社が開発した[翻訳支援ツール](../Page/翻訳支援ツール.md "wikilink")であるが、現在は、SDL インターナショナル社より販売されている。

## 概要

  - [Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") OSが動作するコンピュータ上で動作し、[テキスト文書](../Page/プレーンテキスト.md "wikilink")、[RTF](../Page/Rich_Text_Format.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[SGMLや](../Page/Standard_Generalized_Markup_Language.md "wikilink")[XMLなどのタグ付き文書](../Page/Extensible_Markup_Language.md "wikilink")、マイクロソフト社の[ワード文書](../Page/Microsoft_Word.md "wikilink")、[エクセル文書](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[パワーポイント文書](../Page/Microsoft_PowerPoint.md "wikilink")、アドビ社の[フレームメーカー文書](../Page/Adobe_FrameMaker.md "wikilink")、[インデザイン文書などの文書の](../Page/Adobe_InDesign.md "wikilink")[翻訳](../Page/翻訳.md "wikilink")を支援する。
  - [翻訳メモリ](../Page/翻訳メモリ.md "wikilink")という機能は原文と訳文のペアを[データベース](../Page/データベース.md "wikilink")に登録しながら翻訳を行い、同一か類似の原文が登場した時にデータベース登録済み訳文を再利用することにより、翻訳のスピードと正確性を向上させるものである。マニュアルやカタログなど、加筆・修正が繰り返される文書の翻訳に適する。
  - SDL Trados Studioを使用して翻訳すると、タグ付き文章のタグを壊さないで翻訳できるため、もとのレイアウトを維持したまま翻訳ができる。このため結果的には翻訳後のレイアウト作業をなくしたり軽減できる。従って、ページ数の多いものに最適なソフトといえる。
  - 元々は言語的に多様なヨーロッパでの翻訳を意図して設計されている。よって、日本語-英語のみならず、各種言語に対応している。
  - 翻訳自体はSDL Trados Studioではなく利用者が手作業で行う。

## 原理

1.  This is the book he bought yesterday at 1000 Yen.
2.  This is the book he bought 2 days ago at 1500 Yen.
3.  This is the book he bought 4 days ago at 1500 Yen.

この1.と2.の文章は似ているが異なるため、Wordの「置換」のような処理では対応できない。しかしSDL Tradosは類似候補を自動的に表示するため、1.の文章を一度翻訳し翻訳メモリに取り込んであれば、2.の翻訳時に「昨日1000円で買った」と表示される。そこで「2日前1500円で買った」と修正して翻訳が完了する。3.を訳す時は、2.との類似性がより高いため、1.の「昨日1000円で買った」ではなく、2.の「2日前に1500円で買った」と表示される。そこで3.の「4日前に1500円で買った」と修正して翻訳が完了する。

翻訳するのは人間でありSDL Trados Studioではないため、翻訳ソフトとは本質的に異なる。

## 開発元 トラドス社の経歴

  - 1984年 トラドス社 (Trados GmbH)が[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")の[シュトゥットガルト](../Page/シュトゥットガルト.md "wikilink")で創設された。
  - 1997年 株式の20%が[アメリカの](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")[マイクロソフト](../Page/マイクロソフト.md "wikilink")社に買収された。
  - 2002年 [ユニスケープ社](https://ja.wikipedia.org/wiki/:en:Uniscape "wikilink") (Uniscape Inc)と合併し、社前をトラドス社 (Trados Inc.) と改めた。本部をアメリカ合衆国[バージニア州アレクサンドリアに置いた](../Page/アレクサンドリア_\(バージニア州\).md "wikilink")。
  - 2005年 [英国の](https://ja.wikipedia.org/wiki/イギリス "wikilink")[SDLインターナショナル社](https://ja.wikipedia.org/wiki/:en:SDL_International "wikilink") (SDL International)に買収された。プログラムのトラドスの開発は、S社の[SDLXと共に継続されることとなった](https://ja.wikipedia.org/wiki/:en:SDLX "wikilink")。

## 対応するファイル形式

最新のSDL Trados Studio 2019は、下記のファイル形式を含めて70種類以上のファイル形式に対応している

  - [Microsoft Office](../Page/Microsoft_Office.md "wikilink"):[Word](../Page/Microsoft_Word.md "wikilink")、[Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")（Bilingual Excel含む）、[PowerPoint](../Page/Microsoft_PowerPoint.md "wikilink")
  - タグ付きファイル：[SGML](../Page/Standard_Generalized_Markup_Language.md "wikilink")、[RTF](../Page/Rich_Text_Format.md "wikilink")、[XML](../Page/Extensible_Markup_Language.md "wikilink")、[HTML](../Page/HyperText_Markup_Language.md "wikilink")、[XLIFF](https://ja.wikipedia.org/wiki/XML_Localization_Interchange_File_Format "wikilink")、SDLXLIFFなど
  - [Adobe](../Page/アドビシステムズ.md "wikilink")：[PDF](../Page/Portable_Document_Format.md "wikilink") (スキャンしたPDF含む）、[FrameMaker](../Page/Adobe_FrameMaker.md "wikilink")、[InDesign](../Page/Adobe_InDesign.md "wikilink")、[InCopy](https://ja.wikipedia.org/wiki/Adobe_InCopy "wikilink")
  - Source Code ファイル：[Java](https://ja.wikipedia.org/wiki/Java "wikilink") 、[Microsoft .NETなど](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink")
  - [OpenDocument](../Page/OpenDocument.md "wikilink")ファイル、汎用テキストファイル

## 中間ファイル

どのファイル形式でも、編集した直後のファイルは原文と訳文が混在する*バイリンガルファイル*という形式になっている。バイリンガルファイルは、SDLXLIFFファイル形式で保存される。これらのバイリンガル ファイルを*訳文の生成*機能にかけることにより、訳文のみが含まれる完成されたファイルになる。

## 構成モジュール

SDL Trados Studioには、いくつかのツールとアプリケーションが付属している。

  - SDL Trados Studio
    翻訳支援ソフトウェア。
    翻訳メモリを管理するメインアプリケーション。Tradosを使った翻訳とは、SDL Trados Studioを使う作業を意味する。
  - SDL MultiTerm
    用語を追加、編集、管理するためのSDL Trados Studioと統合された用語管理ツール。
  - SDL Language Cloud
    完全クラウドベースの安全な翻訳ソリューション。機械翻訳と人の手による翻訳を組み合わせることで、翻訳プロセスを大幅に簡素化する。
  - SDL AppStore
    翻訳プロセス（例：ファイルフォーマットのサポートやタスク自動化など）に役立つアプリケーションを提供するオンラインマーケットプレイス。

## マーケットシェア

[世界銀行](../Page/世界銀行.md "wikilink")による2004年の調査によると、TRADOSの世界市場占有率は約75％、SDL SDLXがさらに10％を占めた\[1\]。

2006年の[ICL翻訳メモリ調査によると](https://ja.wikipedia.org/wiki/Imperial_College_London "wikilink")、SDL Tradosは全調査対象ユーザーの75％が使用している。51％がTRADOSを、さらに24％がSDL Tradosを使用している\[2\]。

[Proz.com](https://ja.wikipedia.org/wiki/:en:Proz.com "wikilink")が2013年に実施した調査によると、73％の翻訳者がSDL Tradosを持っている\[3\]。

## 脚注

## 外部リンク

  - [SDL社の本国サイト](http://www.sdl.com/en/products/products-index/sdl-trados/)

[Category:アプリケーションソフト_(製品)](https://ja.wikipedia.org/wiki/Category:アプリケーションソフト_\(製品\) "wikilink") [Category:翻訳ソフトウェア](https://ja.wikipedia.org/wiki/Category:翻訳ソフトウェア "wikilink")

1.  表21参照 -
2.
3.