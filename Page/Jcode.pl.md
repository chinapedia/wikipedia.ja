> この記事は[Jcode.pl](https://ja.wikipedia.org/wiki/Jcode.pl)から翻訳されています。


**jcode.pl**とは、[日本語](../Page/日本語.md "wikilink")の[文字符号化方式である](../Page/文字コード.md "wikilink")[Shift_JIS](../Page/Shift_JIS.md "wikilink")、[EUC-JP](../Page/EUC-JP.md "wikilink")、[ISO-2022-JP](../Page/ISO-2022-JP.md "wikilink")（俗にJISもしくはJISコードとも称する）で記述された、日本語符号による文字列の[相互変換](https://ja.wikipedia.org/wiki/相互変換 "wikilink")を行う[Perl](../Page/Perl.md "wikilink")記述の[ライブラリ](../Page/ライブラリ.md "wikilink")。作者は[歌代和正](https://ja.wikipedia.org/wiki/歌代和正 "wikilink")。

## 入手

jcode.plは[\#外部リンク](https://ja.wikipedia.org/wiki/#外部リンク "wikilink")で挙げた作者サイトより入手できる。

## 派生

jcode.plは『*jcode.plオリジナル*と偽らない』ことを条件に再配布並びに改造を許可している。著名な派生に[小飼弾](https://ja.wikipedia.org/wiki/小飼弾 "wikilink")開発の**Jcode.pm**（この場合の先頭**J**は大文字）がある。言語は同じくPerl。主な変更点は次に挙げる通り：

  - 記述をライブラリ (.pl) から[モジュール](../Page/モジュール.md "wikilink") (.pm) に変更
  - 相互変換可能な文字符号候補として[UTF-8](../Page/UTF-8.md "wikilink")を追加

このライブラリ開発で用いた技術は、後に小飼が一スタッフとして参加した、世界中の文字符号を相互変換することを目的とする**Encode Module** (Encode.pm) に組み込まれた。

もうひとつの派生として稲葉準開発の[**Sjisソフトウェア**](http://search.cpan.org/dist/Char-Sjis/)がある。言語は同じくPerl。主な特徴は次の通り：

  - 記述をライブラリ (.pl) から[モジュール](../Page/モジュール.md "wikilink") (.pm) に変更
  - 最新のPerlインタプリタをJPerlとして使うことができる
  - シフトJISを変換せずそのまま扱うため、UTF8フラグが不要

このソフトウェア開発で用いられた技術は、 [GB18030](http://search.cpan.org/dist/Char-GB18030/), [GBK](http://search.cpan.org/dist/Char-GBK/), [Big5Plus](http://search.cpan.org/dist/Char-Big5Plus/), [Big5HKSCS](http://search.cpan.org/dist/Char-Big5HKSCS/), [UHC](http://search.cpan.org/dist/Char-UHC/), [EUCJP](http://search.cpan.org/dist/Char-EUCJP/), [**UTF2**](http://search.cpan.org/dist/Char-UTF2/), [HP15](http://search.cpan.org/dist/Char-HP15/), [INFORMIXV6ALS](http://search.cpan.org/dist/Char-INFORMIXV6ALS/), [OldUTF8](http://search.cpan.org/dist/Char-OldUTF8/) [Latin1](http://search.cpan.org/dist/Char-Latin1/), [Latin2](http://search.cpan.org/dist/Char-Latin2/), [Latin3](http://search.cpan.org/dist/Char-Latin3/), [Latin4](http://search.cpan.org/dist/Char-Latin4/), [Latin5](http://search.cpan.org/dist/Char-Latin5/), [Latin6](http://search.cpan.org/dist/Char-Latin6/), [Latin7](http://search.cpan.org/dist/Char-Latin7/), [Latin8](http://search.cpan.org/dist/Char-Latin8/), [Latin9](http://search.cpan.org/dist/Char-Latin9/), [Latin10](http://search.cpan.org/dist/Char-Latin10/), [Cyrillic](http://search.cpan.org/dist/Char-Cyrillic/), [Greek](http://search.cpan.org/dist/Char-Greek/), [Windows1252](http://search.cpan.org/dist/Char-Windows1252/), [KOI8R](http://search.cpan.org/dist/Char-KOI8R/), [KOI8U](http://search.cpan.org/dist/Char-KOI8U/), [USASCII](http://search.cpan.org/dist/Char-USASCII/), などの各種ソフトウェアに応用された。なお UTF2ソフトウェアは UTF-2 を扱うソフトウェアで、これは現在では UTF-8 と呼ばれている 符号化方式である。

さらにもうひとつの派生として[**jacode.pl**](http://search.cpan.org/dist/jacode/)がある。言語は同じくPerl。主な特徴は次の通り：

  - jcode.plの上位互換ライブラリ
  - Perl4で記述されている
  - 半角カナをサポートしている
  - （このライブラリ単体で）UTF-8をサポートしている
  - \&jcode'convert が自前で対応していない変換は Encode::from_to が呼び出されて変換される
  - UTF8フラグの存在はこのライブラリによって隠蔽されている
  - 過去のスクリプトやノウハウを利用できる

参考 \[Tokyo.pm\] Forward: 5.7.3 is out

<http://mail.pm.org/pipermail/tokyo-pm/2002-March/001319.html>

さらにもうひとつの派生として[**jacode4e.pl**](https://metacpan.org/release/Jacode4e)がある。言語は同じくPerl。主な特徴は次の通り：

  - jacode.pl風であり、Perl5で記述されている
  - メインフレーム、エンタープライズサーバーの文字コード(CP00930,JEF,KEIS,JIPS)をサポートしている
  - （Shift_JISではなく）CP932を拡張したCP932X（CP932カイ）をサポートしている
  - CP932Xは、JIS第3水準、第4水準をカバーし、かつ、これまでに利用している外字はそのまま利用できる
  - これまでのCP932をもとにした通信設備、データ格納システムはそのまま利用できる
  - これまでのCP932をもとにしたアプリケーションプログラムは、ほぼそのまま利用できると期待される

参考 meta::cpan <https://metacpan.org/release/Jacode4e>

## 関連項目

  - [KAKASI](https://ja.wikipedia.org/wiki/KAKASI "wikilink")
  - [エンコード](../Page/エンコード.md "wikilink")
  - [デコード](https://ja.wikipedia.org/wiki/デコード "wikilink")

## 外部リンク

  - [jcode.pl の私的な解説書](http://mikeneko.creator.club.ne.jp/~lab/kcode/jcode.html)
  - <ftp://ftp.iij.ad.jp/pub/IIJ/dist/utashiro/perl/> - [FTP上の歌代和正公式サイト](../Page/File_Transfer_Protocol.md "wikilink")
  - Jcode.pm 公式サイト（[ja](http://openlab.ring.gr.jp/Jcode/index-j.html)／[en](http://openlab.ring.gr.jp/Jcode/)／[CPAN](http://search.cpan.org/%7Edankogai/)）- [CPAN](https://ja.wikipedia.org/wiki/CPAN "wikilink")内の配布サイトではEncode.pmも配布
  - Sjisソフトウェア公式サイト（[en](http://search.cpan.org/dist/Char-Sjis/)）
  - jacode.pl公式サイト（[en](http://search.cpan.org/dist/jacode/)）

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:日本語用の文字コード](https://ja.wikipedia.org/wiki/Category:日本語用の文字コード "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:Perl](https://ja.wikipedia.org/wiki/Category:Perl "wikilink")