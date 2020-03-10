> この記事は[LZFSE](https://ja.wikipedia.org/wiki/LZFSE)から翻訳されています。


**LZFSE** (**Lempel–Ziv Finite State Entropy**) は、[Appleによって開発された](../Page/アップル_\(企業\).md "wikilink")[フリーかつオープンソースの](https://ja.wikipedia.org/wiki/FLOSS "wikilink")[可逆圧縮](../Page/可逆圧縮.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")である\[1\]。

## 概要

このアルゴリズムの名称は、[Lempel-Ziv](https://ja.wikipedia.org/wiki/Lempel-Ziv "wikilink")との[頭字語](../Page/頭字語.md "wikilink")である\[2\]。2015年の[WWDC](https://ja.wikipedia.org/wiki/WWDC "wikilink")で発表され、同年リリースの[OS X El Capitanと](https://ja.wikipedia.org/wiki/OS_X_El_Capitan "wikilink")[iOS 9から導入された](https://ja.wikipedia.org/wiki/iOS_9 "wikilink")。

AppleはLZFSEを[zlib](https://ja.wikipedia.org/wiki/zlib "wikilink") ([DEFLATE](https://ja.wikipedia.org/wiki/DEFLATE "wikilink")) と同程度の圧縮率を実現しながら、2 - 3倍高速に伸長することができ、使用するリソースも少ないのでzlibよりも効率的であると主張している\[3\]。LZFSEは伸長速度と圧縮率の両方を優先する必要がある場合を対象としている。LZFSEのエネルギー効率の高さは、最新の[マイクロアーキテクチャ](../Page/マイクロアーキテクチャ.md "wikilink")のアルゴリズムに最適化することで達成された。この最適化は特に[arm64に焦点を当てている](../Page/ARMアーキテクチャ.md "wikilink")\[4\]。サードパーティーによるベンチマークでは、LZFSEの伸長速度がzlibよりも速いことが確認されているが、その他の多くの最新の可逆圧縮アルゴリズムが圧縮率、圧縮速度及び伸長速度などで、より良好な性能特性を示していることも示唆されている\[5\]。

## 実装

[Cで実装されている](../Page/C言語.md "wikilink")[リファレンス](../Page/リファレンス実装.md "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")はEric Bainvilleによって書かれ、2016年のWWDCでオープンソース化されることが発表され公開された\[6\]。

## 脚注

## 関連項目

  - [Zstandard](https://ja.wikipedia.org/wiki/Zstandard "wikilink") - 別のLZ77とFSEによる圧縮アルゴリズム、FSEの作者が作成
  - [LZ4](https://ja.wikipedia.org/wiki/LZ4 "wikilink") - LZ77による高速な圧縮アルゴリズム、Appleのプラットフォームでも利用可能

## 外部リンク

  -
[Category:データ圧縮](https://ja.wikipedia.org/wiki/Category:データ圧縮 "wikilink") [Category:アップルのソフトウェア](https://ja.wikipedia.org/wiki/Category:アップルのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.