> この記事は[Core Image](https://ja.wikipedia.org/wiki/Core_Image)から翻訳されています。


**Core Image** （**コア・イメージ**）は、AppleのOS（[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")・[iOS](https://ja.wikipedia.org/wiki/IOS_\(アップル\) "wikilink")・[iPadOS](https://ja.wikipedia.org/wiki/iPadOS "wikilink")・[tvOS](https://ja.wikipedia.org/wiki/tvOS "wikilink")）を構成するフレームワークの一つで、[GPUの](../Page/Graphics_Processing_Unit.md "wikilink")[プログラマブルシェーダー](https://ja.wikipedia.org/wiki/プログラマブルシェーダー "wikilink")を用いて画像・動画のフィルタ処理をリアルタイムで行うコンポーネント及び[APIである](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。なおプログラマブルシェーダーをもたない環境では、[CPU](../Page/CPU.md "wikilink")で処理が行われる。

## 概要

Core Imageは[Mac OS X v10.4で導入された](../Page/Mac_OS_X_v10.4.md "wikilink")。

[Core Audioと同様に](../Page/Core_Audio_\(アップル\).md "wikilink")、Image Unit（イメージユニット）と呼ばれるプラグイン形式の画像処理フィルタや、カスタムフィルタを組み合わせることにより、画像の加工・解析を容易に行うことができる。特徴的な機能としては、[バーコード](../Page/バーコード.md "wikilink")・[二次元コード](../Page/二次元コード.md "wikilink")の読み取りや、[顔認識](../Page/顔認識システム.md "wikilink")・[クロマキー](../Page/クロマキー.md "wikilink")合成・画像の自動補正などがある。各ピクセルの値は、整数ではなく、単精度浮動小数点数で処理されるため、非常に正確な演算結果が得られる。

[シェーディング言語](https://ja.wikipedia.org/wiki/シェーディング言語 "wikilink")には[OpenGL](../Page/OpenGL.md "wikilink")規格で標準化されている[GLSL](../Page/GLSL.md "wikilink")が用いられる\[1\]。

## 脚注

## 関連項目

  - [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")
  - [Quartz Extreme](https://ja.wikipedia.org/wiki/Quartz_Extreme "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")
  - [GLSL](../Page/GLSL.md "wikilink")

## 外部リンク

  - [About Core Image](https://developer.apple.com/library/archive/documentation/GraphicsImaging/Conceptual/CoreImaging/ci_intro/ci_intro.html) - Core Image Programming Guide
  - [Core Image](https://developer.apple.com/documentation/coreimage) - Apple Developer Documentation

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:グラフィックライブラリ](https://ja.wikipedia.org/wiki/Category:グラフィックライブラリ "wikilink")

1.  [Core Imageで体験 - Mac OS Xの高速画像処理 (2) Core Imageの構造 | マイナビニュース](http://news.mynavi.jp/special/2006/coreimage/001.html)