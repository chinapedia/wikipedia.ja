> この記事は[MHTML](https://ja.wikipedia.org/wiki/MHTML)から翻訳されています。


**MIME Encapsulation of Aggregate HTML (MHTML)** は、[MIMEのマルチパートを利用することで](../Page/Multipurpose_Internet_Mail_Extensions.md "wikilink")、元となる[HTML文書と](../Page/HyperText_Markup_Language.md "wikilink")、それからリンクされる[画像](../Page/画像.md "wikilink")や[動画](../Page/動画.md "wikilink")などの[リソースを](https://ja.wikipedia.org/wiki/リソース_\(WWW\) "wikilink")1つのデータとしてまとめるフォーマットである。[電子メール](../Page/電子メール.md "wikilink")での利用を想定しているが、[ウェブページ](../Page/ウェブページ.md "wikilink")を一つのファイルとして保存する用途にも用いられている。

## 概要

MHTMLは、RFC 2110 で定義され、その後 RFC 2557 の改訂をうけている。

現在の多くのHTML文書は、元となるHTMLと、[URIによって参照される画像や動画などで構成されている](../Page/Uniform_Resource_Identifier.md "wikilink")。これらのリソースは別々のデータとして存在する。

一方、それまでのHTMLを用いた電子メールではHTML本体のみしか扱うことが出来なかった。 MHTMLはMIMEのマルチパートを用いることで、元のHTMLと他のリソースを纏め、一通の電子メールで完全なHTMLマルチメディア文書を転送できるようにしたフォーマットである。

MIMEのフォーマットに則っているため、[US-ASCII以外の](../Page/ASCII.md "wikilink")[テキスト](../Page/テキスト.md "wikilink")データや画像などの[バイナリ](../Page/バイナリ.md "wikilink")データは[Quoted-printable](https://ja.wikipedia.org/wiki/Quoted-printable "wikilink")か[Base64](../Page/Base64.md "wikilink")でエンコードする。

現在の[HTMLメール対応を謳うメールソフトの多くは](https://ja.wikipedia.org/wiki/HTML電子メール "wikilink")、このMHTMLを扱うことが出来る。

## 電子メール以外での利用

RFC 2557 は、MHTMLは電子メール以外のプロトコル ([HTTPや](../Page/Hypertext_Transfer_Protocol.md "wikilink")[FTP](../Page/File_Transfer_Protocol.md "wikilink")) でも一度に転送出来ることや、完全なHTML文書の[アーカイブ](../Page/アーカイブ.md "wikilink")として保存出来ることを示唆している。

事実、[1999年](../Page/1999年.md "wikilink")3月の[Internet Explorer 5でウェブページをアーカイブするフォーマットとして採用された](../Page/Internet_Explorer.md "wikilink")。これは RFC 2557 の発行時期とほぼ一致する。

ウェブページをMHTMLで保存できる機能をもつ[実装](../Page/実装.md "wikilink")系は、Internet Explorerの他、[Microsoft Office](../Page/Microsoft_Office.md "wikilink") ([Word](../Page/Microsoft_Word.md "wikilink")、[Excel](https://ja.wikipedia.org/wiki/Microsoft_Excel "wikilink")、[PowerPoint](../Page/Microsoft_PowerPoint.md "wikilink")、[Access](../Page/Microsoft_Access.md "wikilink"))、[Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")、[Vivaldiなどがある](https://ja.wikipedia.org/wiki/Vivaldi_\(ウェブブラウザ\) "wikilink")。[Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink")、[Google Chromeでも設定をしたり](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、拡張機能を導入することで扱えるようになる。

ただし、ブラウザ側が大規模なアップデートを行った場合など、拡張機能側がアップデートし対応するまでの間、使用できない事がある。例えばFirefoxのアドオンとして「[UnMHT](https://addons.mozilla.org/ja/firefox/addon/unmht/)」というものがあるが、2017年11月25日時点の最新バージョンである8.3.2は、[2017年11月14日にリリース](https://support.mozilla.org/ja/kb/firefox-add-technology-modernizing?as=u&utm_source=inproduct)された[Firefox 57には対応しておらず](https://ja.wikipedia.org/wiki/Mozilla_Firefox#Firefox_Quantum "wikilink")、扱う事が出来ない。

## 関連項目

  - [HTML](../Page/HyperText_Markup_Language.md "wikilink")
  - [MIME](../Page/Multipurpose_Internet_Mail_Extensions.md "wikilink")

## 外部リンク

  - RFC 2110 (旧)
  - RFC 2557 (新)
  - [MHTML - Sending HTML in E-mail](http://people.dsv.su.se/~jpalme/ietf/mhtml.html)
  - [mozdev.org - Mozilla Archive Format](http://maf.mozdev.org/)

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:HTML](https://ja.wikipedia.org/wiki/Category:HTML "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")