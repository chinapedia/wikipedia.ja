> この記事は[GIF](https://ja.wikipedia.org/wiki/GIF)から翻訳されています。


**GIFアニメーション**（ジフアニメーション、GIF animation）は、[Graphics Interchange Format](../Page/Graphics_Interchange_Format.md "wikilink") (GIF) の「マルチイメージ」を使った[アニメーション](../Page/アニメーション.md "wikilink")。**アニメーションGIF** (animated GIF) ともいう。

マルチイメージは GIF87a で導入された機能で、複数の**フレーム**を順に表示できる。GIF89a では待ち時間が指定できるようになった。

GIF の使用は[色](../Page/色.md "wikilink")数の制約や過去の[サブマリン特許](https://ja.wikipedia.org/wiki/サブマリン特許 "wikilink")問題などから減りつつあるが、主要な代替規格である [アニメーションPNG](../Page/Animated_Portable_Network_Graphics.md "wikilink") (Animated Portable Network Graphics, APNG) は[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")の対応がまだ途上であり、[JPEG](../Page/JPEG.md "wikilink") にはアニメーション機能そのものがないため、多くの環境で対応しているGIFアニメーションは、2010年現在でも広く使われている。

## 長所と短所

基本的に動画ファイルではなく画像ファイルの拡張なので、動作やサポート状況は画像ファイルに準じ、これが長所にも短所にもなる。また、GIF 共通の長所・短所もある。

### 長所

製作者と閲覧者双方にとっての簡便さが最大の長所である。

  - 古くから多くの[ウェブブラウザ](../Page/ウェブブラウザ.md "wikilink")で標準サポートされており、[プラグイン](../Page/プラグイン.md "wikilink")等は不要である。
  - [動画編集ソフトウェア](https://ja.wikipedia.org/wiki/動画編集ソフトウェア "wikilink")も[ウェブプログラミング](https://ja.wikipedia.org/wiki/ウェブプログラミング "wikilink")も必要ない。必要な[静止画と](../Page/画像.md "wikilink")、簡単な変換ツールがあればいい。
  - [HTML](https://ja.wikipedia.org/wiki/HTML "wikilink")での記述も通常の GIF 画像同様の \<img\> タグや \<a\> タグが使える。
  - [背景](../Page/背景.md "wikilink")を[透過](https://ja.wikipedia.org/wiki/透過 "wikilink")できる（GIF 共通の機能）。

### 短所

さまざまな理由から、大規模な動画には向かない。

  - 画像以外の[ストリームを持たない](../Page/ストリーミング.md "wikilink")。特に、[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")ストリームを持たない。
  - 最大 256 色 (=2<sup>8</sup>) しか使えない。そのため、[自然画](https://ja.wikipedia.org/wiki/自然画 "wikilink")の表現は難しい。
  - [フレーム間圧縮](https://ja.wikipedia.org/wiki/フレーム間圧縮 "wikilink")がない。
      - 同じフレームの再利用はできる。また透過機能を利用して差分画像だけのフレームにすることで圧縮率を上げることもできるため、間接的にフレーム圧縮に近いことはできる。
  - 多くの[ムービープレイヤーでは再生できない](https://ja.wikipedia.org/wiki/動画プレイヤー "wikilink")。
  - [Windows Vistaや](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")[Windows 7](../Page/Microsoft_Windows_7.md "wikilink") では、標準添付のフォトビューワで表示されない。

## 代替手段

GIFアニメーションの代替手段としては

  - [動画](../Page/動画.md "wikilink")ファイル ([MPEG-1](../Page/MPEG-1.md "wikilink")/[-2](../Page/MPEG-2.md "wikilink")/[-4](../Page/MPEG-4.md "wikilink") etc)
  - [JavaScript](../Page/JavaScript.md "wikilink") などで画像を連続表示する
  - [MNG](../Page/Multiple-image_Network_Graphics.md "wikilink") または [APNG](../Page/Animated_Portable_Network_Graphics.md "wikilink")（PNG に対するGIFアニメーションの相当物だが別規格となっている）
  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink")
  - [WebP](https://ja.wikipedia.org/wiki/WebP "wikilink")のアニメーション機能

などがある。

## 関連項目

  - [Motion JPEG](https://ja.wikipedia.org/wiki/Motion_JPEG "wikilink") - JPEG画像を連続表示する形の動画規格。こちらには音声ストリームが存在する。
  - [コンピュータアニメーション](https://ja.wikipedia.org/wiki/コンピュータアニメーション "wikilink")

[Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:画像ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:画像ファイルフォーマット "wikilink") [Category:コンピュータアニメーション](https://ja.wikipedia.org/wiki/Category:コンピュータアニメーション "wikilink")