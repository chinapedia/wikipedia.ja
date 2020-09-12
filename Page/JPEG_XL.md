> この記事は[JPEG XL](https://ja.wikipedia.org/wiki/JPEG_XL)から翻訳されています。


**JPEG XL**は、[Joint Photographic Experts Groupが開発中の](../Page/Joint_Photographic_Experts_Group.md "wikilink")[オープンかつ](../Page/オープンフォーマット.md "wikilink")[ロイヤリティフリー](https://ja.wikipedia.org/wiki/ロイヤリティフリー "wikilink")の[画像ファイルフォーマット](https://ja.wikipedia.org/wiki/画像ファイルフォーマット "wikilink")である。 「ISO/IEC 18181」として[国際標準](https://ja.wikipedia.org/wiki/国際標準 "wikilink")となる予定である\[1\]。

## 概要

JPEG XLは従来の画像ファイルフォーマットの問題点を解決し、現代の画像ファイルフォーマットで必要とされている全ての機能を備えることを目標としている\[2\]。 [JPEG](../Page/JPEG.md "wikilink")の置き換えを試みた画像ファイルフォーマットは多数存在するが、これらにはJPEGと比較した際に問題点があることから、この試みは未だに成功していない。 JPEG XLはこの問題点を解決し、JPEG、[PNG及び](../Page/Portable_Network_Graphics.md "wikilink")[GIF](https://ja.wikipedia.org/wiki/GIF "wikilink")などの画像ファイルフォーマットを置き換えることを目指している。 JPEG XLは技術的には[Google](../Page/Google.md "wikilink")の[PIKと](https://ja.wikipedia.org/wiki/PIK_\(画像圧縮\) "wikilink")の[FUIFを基盤としている](https://ja.wikipedia.org/wiki/Free_Universal_Image_Format "wikilink")\[3\]。 また、可逆圧縮JPEG変換層はGoogleの[Brunsli](https://ja.wikipedia.org/wiki/Brunsli "wikilink")を基盤としている\[4\]。

## 特徴

  - レスポンシブウェブデザインへの最適化
    レスポンシブ画像は[レスポンシブウェブデザイン](https://ja.wikipedia.org/wiki/レスポンシブウェブデザイン "wikilink")の一部であり、[画面サイズ](../Page/画面サイズ.md "wikilink")や[解像度](../Page/解像度.md "wikilink")に応じて最適な画像を提供するので、帯域幅を無駄にすることを防いでいる。これによって最適なサイズの画像が選択されるので、帯域幅を無駄にすることを防ぐことができる。
    従来の画像ファイルフォーマットの場合は、複数の異なるサイズのソースファイルを用意してこれを実現している。
    JPEG XLは1つのファイルに元のサイズの画像とその画像の複数の小さなバージョンを含むことができるので、1つのソースファイルでこれを実現することができる\[5\]。
  - 高品質
    JPEG XLは数学的な[可逆圧縮](../Page/可逆圧縮.md "wikilink")に加えて、視覚的な可逆圧縮にも対応している。これは数学的には非可逆圧縮だが、[ヒト](../Page/ヒト.md "wikilink")の[目](../Page/目.md "wikilink")には違いが分からないものである\[6\]。
  - 幅広い用途への対応
    JPEG XLは現代の画像ファイルフォーマットで必要とされている全ての機能を備えているので、幅広い用途で使用することができる。JPEG XLは[携帯機器](../Page/携帯機器.md "wikilink")でも[ハードウェアアクセラレーション](../Page/ハードウェアアクセラレーション.md "wikilink")無しに効率的にエンコードとデコードが行えるように設計されている\[7\]。
  - JPEGからの移行への対応
    JPEG XLエンコーダは拡張メタデータを追加した[下位互換性](https://ja.wikipedia.org/wiki/下位互換性 "wikilink")のあるJPEGファイルを生成することができる。このファイルはJPEGデコーダでデコード可能であり、JPEG XLデコーダの場合は拡張メタデータを使用して画質を向上させることができる。
    また、JPEGファイルを可逆圧縮することができる。
    これらの機能は従来のJPEGからのスムーズな移行を目的としている\[8\]。

## 歴史

、Joint Photographic Experts Groupは圧縮率を従来のJPEGから60%の向上を目指す次世代画像ファイルフォーマット「JPEG XL」を策定中であることを公表し、仕様を満たす技術の公募を開始した。 草案では、[8K](https://ja.wikipedia.org/wiki/8K "wikilink")などの高解像度画像を扱えること、4:4:4、4:2:2、4:2:0のサンプリングに対応すること、[ビット深度](https://ja.wikipedia.org/wiki/ビット深度 "wikilink") (最大16ビット) へ対応することが最低限要求された\[9\]。

、[リファレンス実装](../Page/リファレンス実装.md "wikilink")が公開された。これは[C++](../Page/C++.md "wikilink")で実装されており、[フリーかつオープンソースであり](../Page/FLOSS.md "wikilink")、[Apache License 2.0の下で配布されている](https://ja.wikipedia.org/wiki/Apache_License_2.0 "wikilink")\[10\]。

## 脚注

### 注釈

### 出典

## 関連項目

  - [HEIF](https://ja.wikipedia.org/wiki/HEIF "wikilink")

  - [AVIF](https://ja.wikipedia.org/wiki/AVIF "wikilink")

  -
## 外部リンク

  -
  -
  -

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:ISO/IEC標準](https://ja.wikipedia.org/wiki/Category:ISO/IEC標準 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.