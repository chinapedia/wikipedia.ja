> この記事は[Zlib](https://ja.wikipedia.org/wiki/Zlib)から翻訳されています。


**zlib**は、データの[圧縮および伸張を行うための](../Page/データ圧縮.md "wikilink")[フリーの](../Page/フリーソフトウェア.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")である。[可逆圧縮](../Page/可逆圧縮.md "wikilink")アルゴリズムの[Deflate](../Page/Deflate.md "wikilink") (RFC 1951)を実装している。ヘッダーやフッターなどのデータ形式はRFC 1950 (ZLIB Compressed Data Format Specification)として仕様化されている。また、これ以外のデータ形式としてRFC 1952 (GZIP File Format Specification)及び、RAW形式(ヘッダーやフッタなし)もサポートする\[1\]。

## 概要

zlibの作者は、[ジャン＝ルー・ガイイ](https://ja.wikipedia.org/wiki/ジャン＝ルー・ガイイ "wikilink")(Jean-Loup Gailly)と[マーク・アドラー](https://ja.wikipedia.org/wiki/マーク・アドラー "wikilink")(Mark Adler)である。彼らは[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")の主要開発者でもある。ジャンが圧縮、マークが伸張に関する部分を担当した。ライセンスは[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")とは違い[GPL](https://ja.wikipedia.org/wiki/GPL "wikilink")ではなく、BSDライセンスに近いより制限の緩やかなものが採用されている([zlib License](https://ja.wikipedia.org/wiki/zlib_License "wikilink"))。

zlibは[C言語](../Page/C言語.md "wikilink")で記述されている。ほとんどのプログラミング言語ではzlibを使えるようにライブラリで提供していて、例えば、[Java Runtime Environmentにも組み込まれており](../Page/Java_Runtime_Environment.md "wikilink")、[Javaプラットフォーム](../Page/Javaプラットフォーム.md "wikilink")からも利用できる。

zlibは、商用ソフトを含む多くのソフトウェアで採用されている\[2\]。画像フォーマットの[PNGがDeflateの実装を必要とするため](../Page/Portable_Network_Graphics.md "wikilink")、データ圧縮系だけでなく、画像を表示するほとんどのソフトウェアでも使われている。ほとんどのOSで[共有ライブラリ](https://ja.wikipedia.org/wiki/共有ライブラリ "wikilink")として含まれている。パソコン・サーバー・携帯電話など、非常に多くのOSで使われているライブラリのため、2002年と2005年にセキュリティ問題が発見されたが、問題が発見されると、広範囲のシステムに影響が及ぶ。

## ヘッダー・フッター

zlibのデータ形式 (RFC 1950) は、圧縮データの前に2バイト以上のヘッダーと末尾に4バイトの[Adler-32](https://ja.wikipedia.org/wiki/Adler-32 "wikilink")のフッターがつく。

ヘッダーの最初の2バイトは以下の通り。

  - 1バイト目
      - 上位4ビットは圧縮情報であり [LZ77](https://ja.wikipedia.org/wiki/LZ77 "wikilink") のウィンドウサイズ。7なら32KBのウィンドウサイズ。
      - 下位4ビットが圧縮方式。通常は数値の8。
  - 2バイト目は
      - 上位2ビットは圧縮レベル。デフォルトは2。
      - 6ビット目はプリセット辞書があるかどうか。
      - 下位5ビットがヘッダー2バイト分のチェックビット。

プリセット辞書を使う場合は3バイト目から辞書情報が続く。使わなければ、圧縮データが続く。

なお、[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink") 形式 (RFC 1952) の場合は、10バイト以上のヘッダーと8バイトのフッターが付く。

##

2012年8月に発行された RFC 6713 で `application/zlib` が定義され、[application/gzip](https://ja.wikipedia.org/wiki/gzip "wikilink") と共に [IANA](../Page/Internet_Assigned_Numbers_Authority.md "wikilink") に正式に登録された。\[3\]

## 脚注

<references />

## 関連項目

  - [gzip](https://ja.wikipedia.org/wiki/gzip "wikilink")

## 外部リンク

  - [公式サイト（英語）](https://zlib.net/)

[Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:ライブラリ_(プログラミング)](https://ja.wikipedia.org/wiki/Category:ライブラリ_\(プログラミング\) "wikilink") [Category:データ圧縮](https://ja.wikipedia.org/wiki/Category:データ圧縮 "wikilink") [Category:1995年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1995年のソフトウェア "wikilink")

1.  <https://zlib.net/manual.html> のIntroduction参照
2.  <http://zlib.net/apps.gz.html>
3.