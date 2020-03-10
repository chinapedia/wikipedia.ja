> この記事は[3Dc](https://ja.wikipedia.org/wiki/3Dc)から翻訳されています。


**3Dc**は[法線マップ](https://ja.wikipedia.org/wiki/法線マップ "wikilink")を[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")するアルゴリズムであり、[ATI](https://ja.wikipedia.org/wiki/ATI "wikilink")が最初に開発、実装した。これは初期の[DXT5アルゴリズムをベースとしており](../Page/DXTC.md "wikilink")、[オープンスタンダード](https://ja.wikipedia.org/wiki/オープンスタンダード "wikilink")な技術である。3Dcは今はATIと[NVIDIA](https://ja.wikipedia.org/wiki/NVIDIA "wikilink")の両方が実装している。

## 対象分野

対象となる法線マッピングは、直線で囲まれた格子から表面の法線を読み出し、幾何学的な表面にライトを当てることをシミュレーションする[バンプマッピング](https://ja.wikipedia.org/wiki/バンプマッピング "wikilink")の一拡張である。これは、単純なモデルに複雑さを増した印象を与えるテクスチャマップに似たものである。

処理コストは減少するが、メモリコストはより増大している。コンシューマ用の3Dハードウェアに実装されてきた既存の可逆圧縮アルゴリズムでは、少ない描画物体で正確に表現するための法線マップを用意するには力不足である。これが3Dcの開発された理由である。

3Dcは[ATI](https://ja.wikipedia.org/wiki/ATI "wikilink")のX800シリーズで正式に導入されたが、このアルゴリズムは古いR3xxシリーズや他社のカードで採用された[S3TCとも互換性がある](../Page/DXTC.md "wikilink")。画質と圧縮率はそれほどいいわけではないが、画質の劣化は標準のS3TCよりは非常に少ない。

## アルゴリズム

表面の法線は、単位長さを持つ3次元ベクトルである。法線ベクトルの長さを制約することにより、どんな法線でも表現するには2要素のみあればよい。それゆえに、入力ベクトルは2次元配列になる。

4x4ブロックで圧縮を行う。それぞれのブロック内では、それぞれの値の2要素を別々に圧縮する。このことから圧縮には16個の数字を2セット必要になる。

この圧縮は、16個の値のうち最小値と最大値を取り出し8bitに量子化する。4x4ブロック内にある個々の要素は3bitに量子化され、最小値と最大値の間を線形に8分割した値に近似される。

入力データは、全体の大きさは4x4ブロック毎に128bitで表現される。8bit精度で非圧縮の場合は、元データは同じ大きさの領域の32個の8bitデータがあるので、全部で256bit必要になる。このアルゴリズムを用いると2:1に圧縮ができる。

圧縮率が時々4:1として表現されるが、これは入力データとして8bit精度ではなく16bit精度を使った場合である。このアルゴリズムは入力データを文字通り1/4に圧縮して出力するが、精度は1/2の場合と比較して同じではない。

## 関連項目

  - [3Dc White Paper (PDF)](http://www.ati.com/products/radeonx800/3DcWhitePaper.pdf)
  - [What is a Normal Map?](http://planetpixelemporium.com/tutorialpages/normal.html)
  - [CREATING AND USING NORMAL MAPS](http://www.bencloward.com/tutorials_normal_maps1.shtml)
  - [Creating Normal Maps](http://www.blender3d.org/cms/Normal_Maps.491.0.html)
  - [3Dc - higher quality textures with better compression](http://www.neoseeker.com/Articles/Hardware/Reviews/r420preview/3.html)

[Category:コンピュータグラフィックス](https://ja.wikipedia.org/wiki/Category:コンピュータグラフィックス "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")