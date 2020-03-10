> この記事は[Namazu](https://ja.wikipedia.org/wiki/Namazu)から翻訳されています。


**Namazu**（なまず）は、[オープンソース](../Page/オープンソース.md "wikilink")の[全文検索](../Page/全文検索.md "wikilink")システム。[UNIX](../Page/UNIX.md "wikilink")系[OS及び](../Page/オペレーティングシステム.md "wikilink")[Windowsで動作する](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。

## 歴史

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")、小中規模のメールアーカイブや[WWWサーバ用の全文検索システムとして](../Page/Webサーバ.md "wikilink")[高林哲](https://ja.wikipedia.org/wiki/高林哲 "wikilink")によって開発され、その簡便な使い勝手から1990年代末までに日本語圏における検索エンジンの代表格として普及した。[2000年](../Page/2000年.md "wikilink")にバージョン2.0が公開されて以降は、Namazu Project名義による共同開発となっている。

## インデクシング

[転置索引](https://ja.wikipedia.org/wiki/転置索引 "wikilink")方式のインデックスを採用。[Perl](../Page/Perl.md "wikilink")言語で書かれたmknmzコマンドにより生成される。[形態素解析](../Page/形態素解析.md "wikilink")には、[KAKASI](https://ja.wikipedia.org/wiki/KAKASI "wikilink")・[ChaSen](https://ja.wikipedia.org/wiki/形態素解析ツールChaSen "wikilink")・[MeCabの分かち書き機能を使用する](https://ja.wikipedia.org/wiki/形態素解析ツールMeCab "wikilink")。

フィルタ機能により、HTML以外にもOffice文書、PDF、****等様々な形式の文書を検索対象とすることができる。

## 検索クライアント

作成されたインデックスを、[C言語](../Page/C言語.md "wikilink")で書かれた“namazu”コマンドが動的に読み出して全文検索を行う。

検索[フロントエンド](../Page/フロントエンド.md "wikilink")には他に、C言語で書かれた[CGIフロントエンド](../Page/Common_Gateway_Interface.md "wikilink")「namazu.cgi」、Perlで書かれた「pnamazu」、Windows用「search-s for Namazu」、[tcl/tk](https://ja.wikipedia.org/wiki/tcl/tk "wikilink")によるtkNamazu、[Emacs](../Page/Emacs.md "wikilink")用namazu.elなどがあり、各環境における検索ができる。

## 参考文献

  - 馬場 肇『[改訂Namazuシステムの構築と活用](http://homepage2.nifty.com/baba_hajime/namazubook/index.html)』[ソフトバンクパブリッシング](https://ja.wikipedia.org/wiki/ソフトバンクパブリッシング "wikilink")、2003年、ISBN 4-7973-2338-8

## 外部リンク

  - [Namazu](http://www.namazu.org/)

[Category:全文検索](https://ja.wikipedia.org/wiki/Category:全文検索 "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:1997年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1997年のソフトウェア "wikilink")