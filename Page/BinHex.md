> この記事は[BinHex](https://ja.wikipedia.org/wiki/BinHex)から翻訳されています。


**BinHex**は[Classic Mac OSの](../Page/Classic_Mac_OS.md "wikilink")[ファイルを](https://ja.wikipedia.org/wiki/ファイル_\(コンピュータ\) "wikilink")[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")の[テキスト](../Page/テキスト.md "wikilink")へ変換するフォーマット。拡張子は.hqx。テキストのみの[電話回線](https://ja.wikipedia.org/wiki/電話回線 "wikilink")等の経路を使って転送する目的で開発された。かつてはバイナリ転送用の[Macバイナリ](../Page/Macバイナリ.md "wikilink")と並んでインターネットでも多用されたが、現在はあまり使われなくなってきている。

## 概要

Classic Mac OSでは、1つのファイルが[データフォークとリソースフォークの](../Page/リソースフォーク.md "wikilink")2つで構成されており、それ以外にも[Finder情報](https://ja.wikipedia.org/wiki/Finder情報 "wikilink")など様々なメタデータを持っている。BinHexではこれらのうち特に重要なデータフォーク、リソースフォーク、ファイル名、[タイプとクリエータ](https://ja.wikipedia.org/wiki/Finder "wikilink")、Finderフラグをアーカイブして、ASCIIのテキストに変換する。

先頭に以下のような行を付けるため、BinHexであることが判定出来る。

    <nowiki>
    (This file must be converted with BinHex 4.0)
    </nowiki>

変換アルゴリズムは[uuencode](https://ja.wikipedia.org/wiki/uuencode "wikilink")や[Base64](https://ja.wikipedia.org/wiki/Base64 "wikilink")と同様、3[オクテットを](https://ja.wikipedia.org/wiki/8ビット "wikilink")4オクテット（6ビットを8ビット）に置き換えるものである。変換後はASCIIテキストとなるため、7ビットのテキストしか扱えないような経路でも転送が出来る。

データ量は約4/3に増加するが、同じオクテットが3から255個連続した場合、これを一つに纏めるという単純な圧縮方式を持っており、データ量の増加をある程度緩和できる。

[CRC (Cyclic Redundancy Check)を用いているため](../Page/巡回冗長検査.md "wikilink")、データの誤りを検出する事が出来る。ただし誤り訂正は出来ない。

ファイル名は63バイト迄扱う事が出来る。Mac OS 9迄は31バイトの制限があるため、これで十分であった。日本語環境の場合はファイル名は[MacJapanese](../Page/MacJapanese.md "wikilink")で保管される。

フォーマットの詳細は、RFC 1741の後半のAppendix Aで確認出来る。

元々BinHexはアプリケーションの名称であった。最初のバージョンは[TRS-80](https://ja.wikipedia.org/wiki/TRS-80 "wikilink")の為に作られたが、その後Classic Mac OS用の同名アプリケーションが作られた。バージョンによってフォーマットが全く異なるが、現在BinHexといった場合、まず間違いなくBinHex 4.0のフォーマットをさす。BinHex 5.0は[Macバイナリ](../Page/Macバイナリ.md "wikilink")フォーマットを扱うアプリケーションであり、これは7ビットテキストではなく8ビットバイナリなので注意が必要である。

現在の[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")では、ファイル名は[Unicode](../Page/Unicode.md "wikilink")で255文字迄であり、メタデータもかつてのClassic Mac OSより種類が増えている。こうした理由からBinHexでは不十分である。

## 利用例

BinHexはかつて[パソコン通信](../Page/パソコン通信.md "wikilink")でファイルを転送する用途で多用された。インターネットが主流になってからも[FTPサイトや](../Page/File_Transfer_Protocol.md "wikilink")[電子メール](../Page/電子メール.md "wikilink")で多用された。

[TCP/IPをベースとしたFTPではバイナリ転送が可能であり一見ナンセンスだが](../Page/インターネット・プロトコル・スイート.md "wikilink")、他のパソコン通信との相互転載も行なわれたため、互換性を考慮すると有用であった。

電子メールで利用する場合、メールの本文中にBinHexのテキストを直接貼付ける手法が取られた。上で示したような行を付けるため、これを認識して添付ファイルとして扱うソフトも存在した。

後にRFC 1741が発行された。これはBinHexを[MIMEの枠組みで扱えるようにしたものである](https://ja.wikipedia.org/wiki/Multipurpose_Internet_Mail_Extensions "wikilink")。以下のようなヘッダフィールドを用いる。

    <nowiki>
    Content-Type: application/mac-binhex40; name="testfile.hqx"
    </nowiki>

多くの[電子メールクライアント](../Page/電子メールクライアント.md "wikilink")はこのRFC 1741を採用したが、nameパラメータの値を"testfile.hqx"ではなく"testfile"のように.hqxを付けない実装もあり、一部混乱が生じた。

なお、連番のRFCとしてRFC 1740がある。これは[AppleSingle](../Page/AppleSingle.md "wikilink")とAppleDoubleをMIMEで扱う方法を規定したものである。

## 外部リンク

  - [RFC1741 - MIME Content Type for BinHex Encoded Files](http://tools.ietf.org/html/rfc1741)
  - [Prehistory of BinHex](http://www.tim-mann.org/binhex.html)
  - [Online BinHex Web Encoder / Decoder](http://www.webutils.pl/BinHex)

## 関連項目

  - [Base64](https://ja.wikipedia.org/wiki/Base64 "wikilink")
  - [uuencode](https://ja.wikipedia.org/wiki/uuencode "wikilink")
  - [ish](https://ja.wikipedia.org/wiki/ish "wikilink")
  - [Macバイナリ](../Page/Macバイナリ.md "wikilink")
  - [AppleSingle](../Page/AppleSingle.md "wikilink")
  - [AppleDouble](https://ja.wikipedia.org/wiki/AppleDouble "wikilink")
  - [リソースフォーク](../Page/リソースフォーク.md "wikilink")

[Category:ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:ファイルフォーマット "wikilink") [Category:Classic_Mac_OS](https://ja.wikipedia.org/wiki/Category:Classic_Mac_OS "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")