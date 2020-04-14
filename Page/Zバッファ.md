> この記事は[Zバッファ](https://ja.wikipedia.org/wiki/Zバッファ)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Z-buffer_no_text.jpg "wikilink") **Zバッファ** (Z-buffer, Z-buffering) とは、[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")において、深度（奥行き）情報を用いて物体の描画処理を省略し高速化するための技術、およびその深度情報を格納する[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")領域のことを指す。**深度バッファ** (depth buffer) とも呼ばれる。コンピュータグラフィックスの分野では比較的古くから存在する技術（[ローテク](../Page/ローテク.md "wikilink")）ではあるが、計算資源の制約が多いリアルタイムグラフィックス用途では特に効果的な技術であり、2015年現在では流通するほぼあらゆるハードウェア（[グラフィックスカード](https://ja.wikipedia.org/wiki/グラフィックスカード "wikilink")／グラフィックスチップ）で使用することができる。

同種として、より描画精度を向上させられる**Wバッファ**という技術もある\[1\]\[2\]が、Zバッファほどの広範なハードウェアサポートはない。

## 概要

まず、画面（レンダーターゲット）内において、ある[ピクセル](../Page/ピクセル.md "wikilink")に物体（の一部）を描画する際に、物体表面の深度（奥行き）を保存しておく。ここでは例えば視点から最も手前の深度値をゼロと定め、奥に進むにつれて深度値が大きくなるものと定める（このルールは処理系によって異なる）。次に同じ[ピクセル](../Page/ピクセル.md "wikilink")に物体を描画することになった場合、前回保存した深度の値と今回描画する物体の深度の値の大きさを比較する（この比較のことを、**Zテスト**あるいは**深度テスト**と呼ぶこともある）。もし今回の深度の方が大きければ、つまり奥にあれば、手前の描画済み物体に隠されて見えないので、新たにピクセルへ描画処理を行なわずに済むことになる。このため、手前に存在する物体から描画して、最後に奥に存在する物体を描画するようにすれば、計算時間を節約することができる。

Zバッファの基本的な原理はこのようなものであるが、このとき画面全体の深度をまとめて保存しておくメモリ領域もまたZバッファと呼ばれる。Zバッファは一般に2次元テクスチャの一形態として扱われる。

Zバッファという名前は、Z-coordinate（3次元空間の次元軸を表すXYZのうち、通例奥行きを表すことが多いZ軸の座標値）を保存するバッファ（一時領域）であるところから来ている。Zバッファは通例[浮動小数点数](../Page/浮動小数点数.md "wikilink")を格納できるフォーマットであり、リアルタイムコンピュータグラフィックスでは16ビット、24ビット、32ビットなどがよく使われる。

## 問題点

半透明の物体を[アルファチャンネル](../Page/アルファチャンネル.md "wikilink")によって合成描画（ブレンディング）する際には、単純なZバッファの比較だけでは正しい結果が得られない。ブレンディングの際には奥に存在する物体の情報が必要だが、もし手前から描画してしまうと、合成するために必要な奥に存在する物体の情報が参照できないからである。また、奥に存在する物体の描画自体がZテストによりスキップされてしまう。この問題を緩和するには、まず不透明の物体のみを先に描画しておき、次に半透明の物体だけ[Zソート法](https://ja.wikipedia.org/wiki/Zソート法 "wikilink")で奥から順に描画するなどの手法を用いる必要がある。そのほか、 (OIT、順序非依存の透明度) という解決策も存在する。

また、近接する複数のプリミティブ（ポリゴン）を描画するときに、背面のプリミティブの一部のピクセルが前面のプリミティブ上にレンダリングされたり、その逆になったりする、と呼ばれるアーティファクト（ノイズ）が発生してしまい正しい結果が得られないことがある\[3\]。特に広大な空間を描画するときに、Zバッファの精度が不足しているとZファイティングが発生しやすくなる。Zファイティングを回避する方法として、Zバッファの精度を上げる、深度バイアスをかける、を利用する\[4\]、などがある。ただしZバッファの精度を上げると、その分メモリを多く消費するようになる。また、画面解像度に比例してZバッファの必要量も増加していく。

## ゲームコンソールとZバッファ

[初代PlayStation](../Page/PlayStation_\(ゲーム機\).md "wikilink") (PS1) \[5\]や[3DO](../Page/3DO.md "wikilink")、[セガサターン](../Page/セガサターン.md "wikilink")にはZバッファが搭載されていなかった。そのため、ポリゴン単位で前後関係を判定する[Zソート法](https://ja.wikipedia.org/wiki/Zソート法 "wikilink")が使用されていた。この方法はZバッファよりも省メモリであるというメリットがあるが、一方で交差するポリゴンを正しく描画できない、ソートのための処理時間を必要とする、などのデメリットもある。

なお、[NINTENDO64](../Page/NINTENDO64.md "wikilink")にはZバッファが搭載されていた。以降、[PlayStation 2や](https://ja.wikipedia.org/wiki/PlayStation_2 "wikilink")[ドリームキャスト](../Page/ドリームキャスト.md "wikilink")などの後継機種では、Zバッファが搭載されることが標準的になっていった。

## 脚注

## 関連項目

  - [Zオーダー](https://ja.wikipedia.org/wiki/Zオーダー "wikilink")
  - [遅延シェーディング](https://ja.wikipedia.org/wiki/遅延シェーディング "wikilink")
  - [3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")
  - [Direct3D](../Page/Direct3D.md "wikilink")
  - [OpenGL](../Page/OpenGL.md "wikilink")

[Category:3DCG](https://ja.wikipedia.org/wiki/Category:3DCG "wikilink")

1.  [W-Buffering](http://www.daionet.gr.jp/~masa/column/98-06-25.html)
2.  [Depth Buffers (Direct3D 9) - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/direct3d9/depth-buffers)
3.  [Configuring depth-stencil functionality - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/graphics-concepts/configuring-depth-stencil-functionality)
4.  [Stencil buffers - Windows UWP applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/uwp/graphics-concepts/stencil-buffers)
5.  [［GDC07＃36］髪型・半透明・物理音源，20分セッションあれこれ - 4Gamer.net](https://www.4gamer.net/games/016/G001607/20070310225634/)