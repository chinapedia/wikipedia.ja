> この記事は[Deflate](https://ja.wikipedia.org/wiki/Deflate)から翻訳されています。


**Deflate**（デフレート）とは[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")と[ハフマン符号](../Page/ハフマン符号.md "wikilink")化を組み合わせた[可逆データ圧縮](../Page/可逆圧縮.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")。[フィル・カッツ](../Page/フィル・カッツ.md "wikilink")が開発した圧縮ツールPKZIPのバージョン2で使われていた。[ZIPや](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")などで使われている。1996年5月に RFC 1951 としてドキュメント化された。ヘッダーやフッターをつけた [zlib](https://ja.wikipedia.org/wiki/zlib "wikilink") (RFC 1950) 形式や [gzip](https://ja.wikipedia.org/wiki/gzip "wikilink") (RFC 1952) 形式とともに使われる事が多い。

## 特徴

  - [可逆圧縮](../Page/可逆圧縮.md "wikilink")
  - [インターネット](../Page/インターネット.md "wikilink")で広く使われている圧縮形式
  - 圧縮は比較的高速、伸長（元に戻すこと/展開）は非常に高速。ただし、[LZWなどと比べると計算量は多い](../Page/Lempel–Ziv–Welch.md "wikilink")。
  - 特許問題：[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")には色々な会社・人物が特許を取っていた。[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")の実装においては、特許を回避するように注意深く実装された。保証されておらず、かつ、議論もあったが[特許](../Page/特許.md "wikilink")にかかわる[アルゴリズム](../Page/アルゴリズム.md "wikilink")は全て回避できたと考えられている。また、開発当初は問題となった特許も現在では大半は有効期限が切れた。

日本人により考案された[LHA](../Page/LHA.md "wikilink")とほぼ同じアルゴリズムを使う。

## 技術詳細

deflateは、[LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")（実際にはその変種の[LZSS](https://ja.wikipedia.org/wiki/Lempel–Ziv–Storer–Szymanski "wikilink")）でデータを「文字そのもの」または （一致長, 一致位置） ペアに符号化する。その結果のうち、「文字そのもの」および「一致長」を合わせて一つの[ハフマン符号](../Page/ハフマン符号.md "wikilink")で符号化し、「一致位置」を別のハフマン符号で符号化する。deflateのハフマン符号化は、ブロック毎に符号を(再)構築する方式で、**ダイナミック**ハフマン符号（）と呼んでいる。日本で一般に動的ハフマン符号と呼ばれているとは異なるので注意。

## 利用例

Deflateアルゴリズムが利用されているソフトウェアの一例を挙げる。

  - [zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")
  - [ZIP](../Page/ZIP_\(ファイルフォーマット\).md "wikilink")
  - [GZIP](https://ja.wikipedia.org/wiki/GZIP "wikilink")
  - [7z](../Page/7z.md "wikilink")
  - [Portable Network Graphics](../Page/Portable_Network_Graphics.md "wikilink") (PNG)

また、ほとんどのプログラミング言語で利用できる。以下はその一例。

  - [Java](https://ja.wikipedia.org/wiki/Java "wikilink") - Deflater クラスで nowrap を有効にすることにより素の deflate が扱え、別途 zlib 形式や gzip 形式のヘッターやフッターの付いた物も扱える。
  - [Perl](../Page/Perl.md "wikilink")
  - [PHP](../Page/PHP_\(プログラミング言語\).md "wikilink")
  - [Python](../Page/Python.md "wikilink")
  - [Ruby](../Page/Ruby.md "wikilink")
  - [C\#](../Page/C_Sharp.md "wikilink")、[VB.NET等の](https://ja.wikipedia.org/wiki/Microsoft_Visual_Basic_.NET "wikilink")[.NET Framework](https://ja.wikipedia.org/wiki/.NET_Framework "wikilink") 2.0以降対応言語 - DeflateStream クラスで素の deflate もしくは GZipStream クラスで gzip 形式。

[Apache HTTP Serverなどの](../Page/Apache_HTTP_Server.md "wikilink")[Webサーバ](../Page/Webサーバ.md "wikilink")でも圧縮通信を zlib 形式で Deflate を使って実装している。

## zlibとgzip

deflateとともによく使われるヘッダー・フッターには zlib (RFC 1950) と gzip (RFC 1952) などがある。zlib はヘッダーが2バイト以上、フッターが4バイトであるのに対して、gzip はヘッダーが10バイト以上、フッターが8バイトである。gzip の方が情報が多く、どのファイルシステム上で圧縮されたかも書いてある。フッターには zlib は [Adler-32](https://ja.wikipedia.org/wiki/Adler-32 "wikilink") を使い、gzip は [CRC-32](../Page/巡回冗長検査.md "wikilink") を使っている。

## 関連項目

  - [データ圧縮](../Page/データ圧縮.md "wikilink")
  - [アルゴリズム](../Page/アルゴリズム.md "wikilink")

## 外部リンク

  - [統合アーカイバプロジェクト](http://www.madobe.net/archiver/index.html)

<!-- end list -->

  - [アーカイブ形式解説](http://mirs.web.fc2.com/Beta/)
  - RFC 1950(zlib)
  - RFC 1951(Deflate)
  - [Archiver Compression Test](http://www.compression.ca/)

[Category:データ圧縮](https://ja.wikipedia.org/wiki/Category:データ圧縮 "wikilink") [Category:アルゴリズム](https://ja.wikipedia.org/wiki/Category:アルゴリズム "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")