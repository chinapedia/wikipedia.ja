> この記事は[Gzip](https://ja.wikipedia.org/wiki/Gzip)から翻訳されています。


{{infobox file format | name = gzip | extension = .gz | mime = application/gzip | typecode = Gzip | uniform type = org.gnu.gnu-zip-archive | magic = \\x1f\\x8b | owner = [{{lang](https://ja.wikipedia.org/wiki/ジャン＝ルー・ガイイ "wikilink")、\[\[マーク・アドラー|  **gzip**（ジー・ジップ）は、[データ圧縮](../Page/データ圧縮.md "wikilink")[プログラムのひとつ](https://ja.wikipedia.org/wiki/プログラム_\(コンピュータ\) "wikilink")、およびその圧縮データの[フォーマットである](../Page/ファイルフォーマット.md "wikilink")。「[GNU](../Page/GNU.md "wikilink") zip」の略であり\[1\] [GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")によって開発・メンテナンスされている。現在、多くの[UNIX](../Page/UNIX.md "wikilink")に標準搭載される。

それ以前に普及していた<kbd>[compress](https://ja.wikipedia.org/wiki/UNIX_Compress "wikilink")</kbd>は[LZWを使用しているため特許侵害の危険があり](https://ja.wikipedia.org/wiki/Lempel–Ziv–Welch "wikilink")、GNUプロジェクトが、安全・安心な代替として開発した\[2\]。

フォーマットは「GZIP File Format Specification」として文書化されている。Windows（及び以前のMS-DOS）文化圏で一般的な[ZIPとは圧縮方法として](https://ja.wikipedia.org/wiki/ZIP_\(ファイルフォーマット\) "wikilink")[Deflate](https://ja.wikipedia.org/wiki/Deflate "wikilink")法が共通である以外は無関係である。

## 概要

gzipは、Lempel-Zivアルゴリズム ([LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink")) と[ハフマン符号](https://ja.wikipedia.org/wiki/ハフマン符号 "wikilink")を用いており、従来のcompressよりも圧縮率が高いことが特徴である。ただし非常に冗長なファイルでは、compressの方が圧縮率が高いこともある。開発者向けに[ライブラリ](../Page/ライブラリ.md "wikilink")として[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink")が作成され、これにより広く使われる形式となった。gzipによって圧縮されたファイルの[拡張子](../Page/拡張子.md "wikilink")は慣習的に`.gz`を用いる(極初期のgzipは`.z`を用いたが、[pack](https://ja.wikipedia.org/wiki/pack "wikilink")との混同を避けるため変更された、1993年頃に作成された`.z`はgzipファイルの可能性が高い。なお、gzip自体はpack形式の伸長が可能である)。

また、<kbd>gzip</kbd>コマンドは[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")から受け取ったデータを圧縮し、[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")から取り出すことができる（<kbd>gunzip</kbd>は逆の動作）ため、ファイル圧縮に限らず、多様な目的に使用できる。

gzipはzip等と異なり[ファイルアーカイバとしての機能は持たず](https://ja.wikipedia.org/wiki/アーカイブ_\(コンピュータ\) "wikilink")、複数ファイルを扱いたい場合は<kbd>[tar](https://ja.wikipedia.org/wiki/tar "wikilink")</kbd>ファイルをgzip圧縮するという使い方が一般的である。GNU tarにはアーカイブをgzipに[フィルタする](https://ja.wikipedia.org/wiki/フィルタ_\(ソフトウェア\) "wikilink")<kbd>-z</kbd>オプションが付いている。これによりアーカイブと圧縮を同時に、あるいは抽出と伸張を同時に行うことができる。gzip圧縮したtarアーカイブは拡張子`.tar.gz`または`.tgz`を付ける習慣がある。

[HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") 1.1にはデータを圧縮し転送量を減らす機能があるが、gzipはその際の圧縮フォーマットの一つとしても使われている。また、gzipはその仕様がRFC 1952で記述されている。

初期のうちに登場した1.2.4が安定したバージョンとして長期に亘って利用されたが、4GB超のファイルへの対応が無かったため、種々のバージョンアップが行われた。

今日では、圧縮・伸張の速度より圧縮率の高さを重視する場合には、[bzip2](https://ja.wikipedia.org/wiki/bzip2 "wikilink")や[xzを使用することがある](https://ja.wikipedia.org/wiki/xz_\(ファイルフォーマット\) "wikilink")。

## 互換性

gzipは、<kbd>zip</kbd>、<kbd>compress</kbd>、<kbd>compress -H</kbd>、<kbd>pack</kbd>で圧縮されたファイルを伸張することができる。zipファイルについては、Deflate法で圧縮されファイルが1つしか含まれていない場合にだけ伸張できる。gzipがインストールされているシステムでは、<kbd>gunzip</kbd>、<kbd>zcat</kbd>、<kbd>uncompress</kbd>コマンドが、<kbd>gzip</kbd>コマンドへの[ハードリンク](https://ja.wikipedia.org/wiki/ハードリンク "wikilink")として存在していることがある。Linux Standard Baseでも指定コマンドになっている\[3\]。

## 主なオプション

  - <kbd>-r</kbd>:サブディレクトリに亘って圧縮する
    <kbd>-v</kbd>:詳細情報を表示する
    <kbd>-数字</kbd>:圧縮率の調整 （例：<kbd>-9</kbd> 圧縮率を最大にする <kbd>-1</kbd> 圧縮速度を最大にする。既定は6）
    <kbd>-f</kbd>:上書きを強制する

## 拡張子

`.gz`\[4\]\[5\]\[6\]

tarと組み合わせる場合には`.tar.gz`もしくは`.tgz`とする。

##

2012年8月に発行されたRFC 6713で`application/gzip`が定義されて、[IANAにも正式に登録された](../Page/Internet_Assigned_Numbers_Authority.md "wikilink")。以前は`application/x-gzip`や`application/x-gzip-compressed`などが用いられていた。\[7\]

tarによるアーカイブがなされている場合は、非公式の`application/x-tar-gz`も用いられる。

## 出典

<references />

## 外部リンク

  - RFC 1952
  - [The gzip home page](https://www.gzip.org)

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:データ圧縮規格](https://ja.wikipedia.org/wiki/Category:データ圧縮規格 "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")

1.
2.  当時のGNU bullitinではyabbaが紹介されていたがそれを差し置いてリリースされたのがgzipである）。
3.  Linux Standard Base <https://refspecs.linuxfoundation.org/lsb.shtml>
4.
5.
6.
7.