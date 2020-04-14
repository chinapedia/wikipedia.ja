> この記事は[HSV色空間](https://ja.wikipedia.org/wiki/HSV色空間)から翻訳されています。


**HSVモデル**()は[色相](https://ja.wikipedia.org/wiki/色相 "wikilink")()、[彩度](https://ja.wikipedia.org/wiki/彩度 "wikilink")()、[明度](https://ja.wikipedia.org/wiki/明度 "wikilink")()の三つの成分からなる[色空間](../Page/色空間.md "wikilink")。**HSB色空間**()とも言われる。[HLS色空間](../Page/HLS色空間.md "wikilink")()とよく似ている。

[frame](https://ja.wikipedia.org/wiki/ファイル:Hsv_sample.png "wikilink")

  - 色相 - [色](../Page/色.md "wikilink")の種類（例えば赤、青、黄色）。0 - 360の範囲（[アプリケーションによっては](../Page/アプリケーションソフトウェア.md "wikilink")0 - 100 % に[正規化](../Page/正規化.md "wikilink")されることもある）。
  - 彩度 - 色の鮮やかさ。0 - 100 % の範囲。刺激純度と  の色彩的な量と比較して「純度」などともいう。色の彩度の低下につれて、[灰色](../Page/灰色.md "wikilink")さが顕著になり、くすんだ色が現れる。また彩度の逆として「」を定義すると有益である。
  - 明度 - 色の明るさ。0 - 100 % の範囲。

HSVは[1978年](https://ja.wikipedia.org/wiki/1978年 "wikilink")にアルヴィ・レイ・スミス()によって考案された。これは[RGB](../Page/RGB.md "wikilink")色空間の[非線形変換であり](../Page/線型性.md "wikilink")、色の変換に用いられることもある。HSVとHSBは同一であるがHLSとは異なる。

## HSVの視覚化

HSVモデルは通例[コンピュータグラフィックスアプリケーションに用いられる](../Page/グラフィックソフトウェア.md "wikilink")。いろいろなアプリケーションでユーザは個々のグラフィックス要素に適用する色を選択する必要がある。このような場合、HSV色環がよく用いられる。これは[円状の領域に色相が表現されたもので](../Page/円_\(数学\).md "wikilink")、それとは別に[三角形](../Page/三角形.md "wikilink")の領域が彩度と明度の表現に用いられることがある。上図における三角形の水平軸は明度を指示し、また垂直軸は彩度に対応する。このような形式のインターフェースでは、最初の操作で環状の領域から色相を選択し、続いて三角形の領域から所望の彩度と明度を選択する。

[thumb](https://ja.wikipedia.org/wiki/ファイル:HSV_cone.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:HSV_cylinder.jpg "wikilink")

HSVモデルの別の視覚化方法は[円錐](../Page/円錐.md "wikilink")である。この表現では、色相は色環の三次元円錐状の構造に描かれる。彩度はその円錐の中心からの距離、明度は円錐の頂点からの距離で表される。円錐ではなく六角形の錐体（六角錐）で表現するものもある。この方法は単一の物体でHSV色空間全体を視覚化するのに適している。三次元形状のため二次元の[コンピュータインターフェイスにおける色の選択に利用するのは難しい](../Page/ユーザインタフェース.md "wikilink")。

HSV色空間は[円柱状の物体として](../Page/円柱_\(数学\).md "wikilink")[視覚化されることもある](../Page/可視化.md "wikilink")。上記と同様に色相は円柱の外周に沿って変化し、彩度は中心からの距離に伴って変化する。明度も頂点から底へ向かって変化する。このような表現はHSV色空間のモデルとして数学的に厳密であると考えられるかもしれないが、視覚化された彩度レベルと色相の精度は黒に近づくにつれて減少する。さらに、通常コンピュータは有限の範囲でRGB値を格納する。精度の制限は人間の色認知能力の限界とも関連し、ほとんどのケースで円錐による視覚化はより現実的とされている。

## HSVと色覚

HSVモデルと[人間が色を](../Page/ヒト.md "wikilink")[知覚](../Page/知覚.md "wikilink")する方法が類似しているため、[グラフィックデザイナー](../Page/グラフィックデザイナー.md "wikilink")は[RGB](../Page/RGB.md "wikilink")や[CMYK](../Page/CMYK.md "wikilink")のようなモデルよりHSVカラーモデルを用いることを好むことがある。RGBとCMYKはそれぞれ[加法混合](https://ja.wikipedia.org/wiki/加法混合 "wikilink")と[減法混合](https://ja.wikipedia.org/wiki/減法混合 "wikilink")によるモデルであり、どちらも[原色](../Page/原色.md "wikilink")の組み合わせによって色が定義される。それに対しHSVはより人間と親和性のある内容、この色は何色か・鮮やかさはどのくらいか・明るくしたり暗くするにはどうしたらいいか、で色についての[情報](https://ja.wikipedia.org/wiki/情報 "wikilink")を[カプセル化](../Page/カプセル化.md "wikilink")する。HLS色空間も同様に[直感](https://ja.wikipedia.org/wiki/直感 "wikilink")的に理解しやすい。

HSV三刺激値空間は、[放射測定](https://ja.wikipedia.org/wiki/放射測定 "wikilink")された物理的な[パワースペクトル](https://ja.wikipedia.org/wiki/パワースペクトル "wikilink")へ一対一に対応させることはできない。従って、HSV座標と[波長](../Page/波長.md "wikilink")や[振幅](../Page/振幅.md "wikilink")といった物理的な光の性質の間を対応させる方法は存在しない。もし物理的直感が必要であれば、以下のような「色彩測定」の心理物理的技術を用いて、HSV座標系を擬似的に変換することは可能である。

  - 色相は色の主波長を定義し、色相はスペクトルに沿った波長位置を意味する。ただし[インディゴ](../Page/インディゴ.md "wikilink")から[赤](../Page/赤.md "wikilink")の間（およそ240 - 360度）は純紫線（ピュアパープルの線）上を示す。
  - もし色相知覚が再現されれば、実際[単色では主波長に位置する純粋な](https://ja.wikipedia.org/wiki/単色光 "wikilink")[スペクトル色を利用し](https://ja.wikipedia.org/wiki/周波数スペクトル "wikilink")、「脱飽和」は適用された主波長の頻度分布あるいは単色光に同じ力の量の光（例・白）を加算することとだいたい同じことになるだろう。
  - 明度は[スペクトラム](../Page/スペクトラム.md "wikilink")のパワーの総量または光の[波形](../Page/波形.md "wikilink")の最大[振幅](../Page/振幅.md "wikilink")にほぼ類似する。しかしながら、実際のところ明度が最大のスペクトル成分（統計学「[モード](../Page/要約統計量.md "wikilink")」、この分布に直交し累積した力ではない）に近いことは以下の方程式から分かる。

## RGBからHSVへの変換

R、GおよびBが0.0を最小量、1.0を最大値とする0.0から1.0の範囲にあり、(R,G,B)で定義された色が与えられたとすると、それに相当する(H,S,V)カラーは次のような数式により決定することができる。

R,G,Bの三つの値の内、最大のものをMAX、最小のものをMINとすると、この式は次のように書ける。

\(\begin{align}
H &=
\begin{cases}
\text{undefined,}  & \text{if } \mathrm{MIN} = \mathrm{MAX} \\
60 \times \frac{G - R}{\mathrm{MAX} - \mathrm{MIN}} + 60,  & \text{if } \mathrm{MIN} = B \\
60 \times \frac{B - G}{\mathrm{MAX} - \mathrm{MIN}} + 180, & \text{if } \mathrm{MIN} = R \\
60 \times \frac{R - B}{\mathrm{MAX} - \mathrm{MIN}} + 300, & \text{if } \mathrm{MIN} = G
\end{cases} \\
V &= \mathrm{MAX}
\end{align}\)

円錐モデル\(S = \mathrm{MAX} - \mathrm{MIN} \,\)

円柱モデル\(S = \frac {\mathrm{MAX} - \mathrm{MIN}} {\mathrm{MAX}}\)

結果は(H,S,V)形式である。Hは0.0から360.0まで変化し、色相が示された色環に沿った[角度](../Page/角度.md "wikilink")で表現される。SおよびVは0.0から1.0までの範囲で変化する彩度および明度である。角座標系で、Hの範囲は0から360までであるが、その範囲を超えるHは360.0で割った剰余（またはモジュラ演算）でこの範囲に対応させることができる。たとえば-30は330と等しく、480は120と等しくなる。

この式はHSVの他の性質も示す。

  - MAX = MIN(例・S = 0)のとき、 Hは定義されない。上記のHSV空間の図を参照するとよい。もしS = 0ならこの色は中央のグレイの直線の周囲にあり、従ってこの色には彩度がなく、角座標には意味がない。

<!-- end list -->

  - 円柱モデルでMAX = 0（例・V = 0）のとき、Sは未定義である。これは上記の円錐状の図に最もよく表れている。もしV = 0ならこの色は完全な黒であり、この色に色相も彩度もない。従って円錐状の図は単一の点に潰れ、この点では角度も角座標系も無意味である。

### ソフトウェアでの変換処理

以下の処理を行うことで変換することができる。

※HSV/RGB全要素を0.0～1.0の浮動小数点数で表現した円柱モデルの場合

``` java
// (float r, float g, float b)
float max = r > g ? r : g;
max = max > b ? max : b;
float min = r < g ? r : g;
min = min < b ? min : b;
float h = max - min;
if (h > 0.0f) {
    if (max == r) {
        h = (g - b) / h;
        if (h < 0.0f) {
            h += 6.0f;
        }
    } else if (max == g) {
        h = 2.0f + (b - r) / h;
    } else {
        h = 4.0f + (r - g) / h;
    }
}
h /= 6.0f;
float s = (max - min);
if (max != 0.0f)
    s /= max;
float v = max;
```

## HSVからRGBへの変換

Hが色相を配置した色環に沿って0.0から360.0の範囲で変化する角度で表記され、彩度を意味するS、明度を意味するVがそれぞれ0.0から1.0の間で変化する。このような(H,S,V)値によって定義されたある色が与えられているとするとき、次の式を通してこれに対応する(R,G,B)カラーを決定することができる。

まず、もしSが0.0と等しいなら、最終的な色は無色もしくは灰色である。このような特別な場合、R、G、およびBは単純にVと等しい。上記の通り、この場合Hは無意味となる。

円柱モデルからの変換\(C = V \times S\)

円錐モデルからの変換\(C = S\)

\(\begin{align}
H^\prime &= \frac{H}{60^\circ} \\
X        &= C (1 - |H^\prime \;\bmod 2 - 1|)\\

(R, G, B) &= (V - C)(1, 1, 1) +\begin{cases}
(0, 0, 0) &\mbox{if } H \mbox{ is undefined} \\
(C, X, 0) &\mbox{if } 0 \leq H^\prime < 1 \\
(X, C, 0) &\mbox{if } 1 \leq H^\prime < 2 \\
(0, C, X) &\mbox{if } 2 \leq H^\prime < 3 \\
(0, X, C) &\mbox{if } 3 \leq H^\prime < 4 \\
(X, 0, C) &\mbox{if } 4 \leq H^\prime < 5 \\
(C, 0, X) &\mbox{if } 5 \leq H^\prime < 6
\end{cases}
\end{align}\)

### ソフトウェアでの変換処理

以下の処理を行うことで変換することができる。

※HSV/RGBを0.0～1.0の浮動小数点数で表現した円柱モデルの場合

``` java
// (float h, float s, float v)
float r = v;
float g = v;
float b = v;
if (s > 0.0f) {
    h *= 6.0f;
    final int i = (int) h;
    final float f = h - (float) i;
    switch (i) {
        default:
        case 0:
            g *= 1 - s * (1 - f);
            b *= 1 - s;
            break;
        case 1:
            r *= 1 - s * f;
            b *= 1 - s;
            break;
        case 2:
            r *= 1 - s;
            b *= 1 - s * (1 - f);
            break;
        case 3:
            r *= 1 - s;
            g *= 1 - s * f;
            break;
        case 4:
            r *= 1 - s * (1 - f);
            g *= 1 - s;
            break;
        case 5:
            g *= 1 - s;
            b *= 1 - s * f;
            break;
    }
}
```

## 関連項目

  - [色](../Page/色.md "wikilink")
  - [色空間](../Page/色空間.md "wikilink")

[simple:Color wheel\#The 12 major colors of the color wheel](https://ja.wikipedia.org/wiki/simple:Color_wheel#The_12_major_colors_of_the_color_wheel "wikilink")

[Category:色空間](https://ja.wikipedia.org/wiki/Category:色空間 "wikilink")