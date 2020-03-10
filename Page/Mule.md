> この記事は[Mule](https://ja.wikipedia.org/wiki/Mule)から翻訳されています。


[Mule-2.3-19.34-demo.png](https://ja.wikipedia.org/wiki/File:Mule-2.3-19.34-demo.png "fig:Mule-2.3-19.34-demo.png") **MULE**（ミュール）は、[GNU Emacsの](https://ja.wikipedia.org/wiki/GNU_Emacs "wikilink")**MUL**tilngual **E**nhancement、すなわち[多言語](../Page/多言語.md "wikilink")拡張である。[NEmacs](https://ja.wikipedia.org/wiki/NEmacs "wikilink")の開発を終了してからMule の開発へ移行する際に、GNU Emacsで「いつでも、どこでも、どんな言語でも」扱えることを目指し、Multilingual とされた。Muleの開発は終了しており、実現された機能をより適切に表現するなら、"MULtiscript Enhancement"、すなわち「多[用字系](https://ja.wikipedia.org/wiki/用字系 "wikilink")拡張」である。Muleがテキストの操作に提供する機能は、言語固有の表記法による検索機能や、文章の校閲機能はなく、各言語で使用される文字列の入力、編集、表示だからである。 Mule機能をGNU Emacsに統合し、Muleそのものの開発は終了した。Muleが提供した機能をGNU Emacsに限らず、[GNU/Linuxシステム](https://ja.wikipedia.org/wiki/GNU/Linuxシステム "wikilink")のソフトウェアに提供することを目指して多言語ライブラリ[m17nlib](https://ja.wikipedia.org/wiki/m17nlib "wikilink")の開発を行っている。現在は[m17nlib](https://ja.wikipedia.org/wiki/m17nlib "wikilink")の開発も終了している。

## 概要

MULEは、別々の言語で書いてあるテキストのみならず、ひとつのバッファーに複数言語を含む多言語テキストの処理機能を提供している。多言語テキスト表現用である[ユニコード](https://ja.wikipedia.org/wiki/ユニコード "wikilink")の提供する単純な機能を超えたものである。入力方法(imput method)、各種さまざまな符号化の文字形(font)を用いた表示、複雑な文字配置、各地の言語に対応した編集機能などに対応している\[1\]。

GNU Emacsの[日本語](../Page/日本語.md "wikilink")処理を含む多言語拡張版である、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")にリリースされた[Nemacs](https://ja.wikipedia.org/wiki/Nemacs "wikilink")に基づいている。主要な開発は電子総合研究所（現：[産業技術総合研究所](https://ja.wikipedia.org/wiki/産業技術総合研究所 "wikilink")）の[半田剣一](https://ja.wikipedia.org/wiki/半田剣一 "wikilink")、高橋直人、錦見美貴子、[戸村哲](https://ja.wikipedia.org/wiki/戸村哲 "wikilink")の４名のグループによって始まった。MULE本体の開発の鈍化や、GNU Emacsからの[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")の[分岐にともなう遅滞などもあった](https://ja.wikipedia.org/wiki/フォーク_\(ソフトウェア開発\) "wikilink")。21版のGNU EmacsにMULEの機能は正式に統合されている\[2\]\[3\]。

## 変換テーブル型入力システム Quail

Muleで多言語入力を行うには、Quailパッケージを用いることによって、ASCIIキーボードの入力をQuail変換ルールにそって対象言語の文字列に翻訳することができる。またQuail変換ルールはユーザが定義することで新たに対応言語を追加することが可能である。

## Mule for Win32

**Mule for Win32**は、[Windows95](../Page/Microsoft_Windows_95.md "wikilink")/NTで動作する**MULE**である。[宮下尚](https://ja.wikipedia.org/wiki/宮下尚 "wikilink") (himi)によりWin32アプリケーションとしてMule 2.3をベースにして開発された。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")にリリースされたバージョン1.22はfinal major versionと銘打たれ、以降の開発は後継ソフトウェアの[Meadow](../Page/Meadow.md "wikilink")へと移った。

なおMeadowの開発およびサポートは既に終了している。Meadowの最後の正式版は[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")のバージョン2.10、最後の評価版は[2009年](../Page/2009年.md "wikilink")のバージョン3.01-devであった。

## 参考文献

  - マルチリンガル環境の実現―X Window/Wnn/Mule/WWWブラウザでの多国語環境,錦見美貴子, 戸村哲, 桑理聖二, 吉田智子, 高橋直人, 半田剣一, 向川信一, プレンティスホール出版 1996年, ISBN 978-4887350205
  - 便利に使おうMule for Windows活用入門―Windowsで文章を扱う人へ, 宮下尚, カットシステム,1997, ISBN 978-4906391516

## 脚注

## 関連項目

  - [テキストエディタの一覧](https://ja.wikipedia.org/wiki/テキストエディタの一覧 "wikilink")

## 外部リンク

  - MULE homepage　- 閉鎖
      - MULE history　- 閉鎖　
  - <https://savannah.nongnu.org/projects/mule>
  - [Vector Mule for Win32 のダウンロード](http://www.vector.co.jp/soft/win95/writing/se021927.html)

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink")

1.  MULtilingual enhancement to Emacs <https://savannah.nongnu.org/projects/mule>
2.  GNU Emacs 21.1 <http://lists.gnu.org/archive/html/info-gnu-emacs/2001-10/msg00009.html>
3.  Muleを捨てて,Emacsを使おう--Emacsの自然言語処理機能 (特集 使いやすくなった自然言語処理のフリーソフト--知っておきたいツールの中身) 高橋直人, 錦見美貴子, 半田剣一, 戸村哲,情報処理,情報処理学会 41(11) (通号 429) 2000.11 p.1233～1238 <https://ipsj.ixsq.nii.ac.jp/ej/?action=repository_uri&item_id=63647&file_id=1&file_no=1>