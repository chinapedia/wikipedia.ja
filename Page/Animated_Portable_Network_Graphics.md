> この記事は[Animated Portable Network Graphics](https://ja.wikipedia.org/wiki/Animated_Portable_Network_Graphics)から翻訳されています。


****(**APNG**)は、コンピュータ上で動画を扱うための[ファイルフォーマット](../Page/ファイルフォーマット.md "wikilink")の1つである。[PNGフォーマットを拡張して作られた](../Page/Portable_Network_Graphics.md "wikilink")。

## 概要

APNGフォーマットでは、最初のフレームが従来のPNGと同様の領域に格納される。そのため、APNGフォーマットに対応しない[デコーダを搭載した](../Page/エンコード.md "wikilink")[ソフトウェア](../Page/ソフトウェア.md "wikilink")でも、最初のフレームが[静止画として表示される](../Page/画像.md "wikilink")。フレームの速度情報や、2枚目以降のアニメーションフレームは、新たに拡張された領域に格納されるが、これらの領域はAPNG非対応のデコーダでは無視される。また、最初のフレームをアニメーションに利用するか設定できるため、非対応環境での代替表示用画像とすることも可能である。

PNGの[アニメーション](../Page/アニメーション.md "wikilink")フォーマットには、[MNGもある](../Page/Multiple-image_Network_Graphics.md "wikilink")。しかし、MNGとAPNGとは密接に関係するものの、これらは別の形式である。APNGの利点は、「（開発者から見て）[アニメーションGIFのPNG版](../Page/GIFアニメーション.md "wikilink")」とも言える実装の容易さ、Firefoxといった主要ブラウザで正式サポートされている事である。仕様上1つのフレームを使い回すことができないためファイルサイズの面ではMNGと比べて有利ではない。

[GIFと比べ](../Page/Graphics_Interchange_Format.md "wikilink")、フレーム内で[フルカラー](../Page/フルカラー.md "wikilink")画像が取り扱えるようになり、さらに[アルファチャンネル](../Page/アルファチャンネル.md "wikilink")を使って背景にとけ込むような表現が可能となった。フルカラー対応となった事でフレームごとに個別のパレット（ローカルパレット）を持つという概念が廃止され共通パレット（グローバルパレット）のみとなった。GIFは[LZW圧縮を使っているが](../Page/Lempel–Ziv–Welch.md "wikilink")、APNGはPNGと同じく比較的圧縮効率の良い[Deflate](../Page/Deflate.md "wikilink")圧縮を使用しているため、アニメーションGIFをAPNGに変換すると多くの場合ファイルサイズを削減できる。

## 歴史

APNGのフォーマットは、[2004年](../Page/2004年.md "wikilink")に[Mozilla Corporationのスチュアート](../Page/Mozilla_Corporation.md "wikilink")・パーメンターとウラジーミルによって作成された。

[2007年](../Page/2007年.md "wikilink")[4月20日](https://ja.wikipedia.org/wiki/4月20日 "wikilink")、PNGグループはAPNGを公式仕様に含めない事を決定した\[1\]。

## ウェブブラウザの対応状況

[APNG_Assembler_Logo.svg](https://ja.wikipedia.org/wiki/File:APNG_Assembler_Logo.svg "fig:APNG_Assembler_Logo.svg")のAPNG Assemblerのロゴ，このソフトはAPNGの画像を作成できる。\]\]

  - [Firefoxでは](../Page/Mozilla_Firefox.md "wikilink")、2008年6月17日リリースのバージョン3.0以降でサポートされている。
  - [Opera](https://ja.wikipedia.org/wiki/Opera "wikilink")では、2017年6月22日リリースのバージョン46以降でサポートされている。
  - [Safari](../Page/Safari.md "wikilink")では、2014年10月16日リリースのバージョン8以降でサポートされている\[2\]。
  - [Google Chromeでは](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")、2017年6月5日リリースのバージョン59以降でサポートされている。
  - [Chromium](https://ja.wikipedia.org/wiki/Chromium "wikilink")は2017年3月15日にAPNGの表示に対応した\[3\]。
  - [Microsoft Edgeは主要ブラウザで唯一対応していない](https://ja.wikipedia.org/wiki/Microsoft_Edge "wikilink")。

## 脚注

<references/>

## 関連項目

  - [PNG](../Page/Portable_Network_Graphics.md "wikilink")
  - [MNG](../Page/Multiple-image_Network_Graphics.md "wikilink")
  - [GIF](../Page/Graphics_Interchange_Format.md "wikilink")
  - [WebP](https://ja.wikipedia.org/wiki/WebP "wikilink") - 静止画ファイルフォーマットだがアニメーションにも対応している
  - [libpng](https://ja.wikipedia.org/wiki/libpng "wikilink")

## 外部リンク

  - [Mozilla wiki: APNG specification](http://wiki.mozilla.org/APNG_Specification)
  - [APNG仕様 日本語訳](https://web-beta.archive.org/web/20120731123209/http://www15.plala.or.jp/kichijitsu/png/APNG_Specification_jp.html)
  - [Implementation work](http://littlesvr.ca/apng/)
  - [Discussion about MNG vs. APNG](https://bugzilla.mozilla.org/show_bug.cgi?id=apng)
  - [APNG patch for libpng](https://sourceforge.net/projects/libpng-apng/)

[Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.
2.  [Bug 43828 – Safari APNG support](https://bugs.webkit.org/show_bug.cgi?id=43828)
3.