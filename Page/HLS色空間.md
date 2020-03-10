> この記事は[HLS](https://ja.wikipedia.org/wiki/HLS)から翻訳されています。


**HLS色空間**（エイチエルエスいろくうかん）とは、[色相](https://ja.wikipedia.org/wiki/色相 "wikilink")（Hue）、[彩度](https://ja.wikipedia.org/wiki/彩度 "wikilink")（Saturation）、[輝度](https://ja.wikipedia.org/wiki/輝度 "wikilink")（Lightness/Luminance または Intensity）の3つの成分からなる[色空間](../Page/色空間.md "wikilink")。[HSV色空間](../Page/HSV色空間.md "wikilink")によく似ている。 HSL、HSIと呼ばれることもある。

[thumbのカラーモデル](https://ja.wikipedia.org/wiki/ファイル:HLS-Model.png "wikilink")\]\]

  - 色相：色味を0～360度の範囲の角度で表す。0度は赤で、その反対側に位置する180度は赤の反対色にあたる青緑。すなわち、反対色を見つけるのも容易。色相についてはHSVと同じ。
  - 彩度：HSVとは違い、純色から彩度が落ちるということは、すなわち灰色になっていくという考え方に基づいている。
  - 輝度：明度100%を純色としてそこからどれだけ明るさが失われるかで表すHSVとは違い、輝度0%を黒、100%を白とし、その中間（50%）を純色とする。50%以下はHSVの明度を示し、50%以上はHSVの彩度を示すと考えると分かりやすいだろう。

HLS色空間を使う代表的なアプリケーションとしては Microsoft Windows （ペイントを含む）、CSS3、Paint Shop Pro、[Inkscape](https://ja.wikipedia.org/wiki/Inkscape "wikilink") など。

## RGBからHLS（HSL）への変換

\(\begin{align}
H &=
\begin{cases}
\text{undefined,}  & \text{if } \mathrm{MIN} = \mathrm{MAX} \\
60 \times \frac{G - R}{\mathrm{MAX} - \mathrm{MIN}} + 60,  & \text{if } \mathrm{MIN} = B \\
60 \times \frac{B - G}{\mathrm{MAX} - \mathrm{MIN}} + 180, & \text{if } \mathrm{MIN} = R \\
60 \times \frac{R - B}{\mathrm{MAX} - \mathrm{MIN}} + 300, & \text{if } \mathrm{MIN} = G
\end{cases} \\
L &= \frac{\mathrm{MAX} + \mathrm{MIN}}{2}
\end{align}\)

双円錐モデル\(S = \mathrm{MAX} - \mathrm{MIN} \,\)

円柱モデル\(S = \frac {\mathrm{MAX} - \mathrm{MIN}} {1 - |\mathrm{MAX} + \mathrm{MIN} - 1|}\)

双円錐モデルと円柱モデルがあり、彩度の定義が異なるため、注意が必要である。

## RGBへの変換

RGBへ変換する際には、いったん最大値や最小を求める必要がある。

  - HSLの円柱モデルからの変換

\(Max = L + \frac{S \times (1-|2 \times L-1|)}{2}\)

\(Min = L - \frac{S \times (1-|2 \times L-1|)}{2}\)

  - HSLの円錐モデルからの変換

\(Max = L + \frac{S}{2}\)

\(Min = L - \frac{S}{2}\)

  - HSVの円柱モデルからの変換

\(Max = V\)

\(Min = V \times (1-S)\)

  - HSVの円錐モデルからの変換

\(Max = V\)

\(Min = V - S\)

求めた最大値と最小値を、色相で場合分けした上で、RGBの各チャンネルに代入する。

\(\begin{align}
(R, G, B) &= \begin{cases}
(\text{Max}=\text{Min}, \text{Max}=\text{Min}, \text{Max}=\text{Min}) &\mbox{if } H \mbox{ is undefined} \\
(\text{Max},\text{Min}+(\text{Max} - \text{Min}) \times \frac{H}{60} ,\text{Min}) &\mbox{if } 0 \leq H < 60 \\
(\text{Min}+(\text{Max} - \text{Min}) \times \frac{120-H}{60}, \text{Max},\text{Min}) &\mbox{if } 60 \leq H < 120 \\
(\text{Min}, \text{Max}, \text{Min}+(\text{Max} - \text{Min}) \times \frac{H-120}{60}) &\mbox{if } 120 \leq H < 180 \\
(\text{Min}, \text{Min}+(\text{Max} - \text{Min}) \times \frac{240-H}{60}, \text{Max}) &\mbox{if } 180 \leq H < 240 \\
(\text{Min}+(\text{Max} - \text{Min}) \times \frac{H-240}{60}, \text{Min}, \text{Max}) &\mbox{if } 240 \leq H < 300 \\
(\text{Max}, \text{Min}, \text{Min}+(\text{Max} - \text{Min}) \times \frac{360-H}{60}) &\mbox{if } 300 \leq H < 360
\end{cases}
\end{align}\)

色相が定義されない場合は、彩度＝0であり、全てのチャンネルが明度や輝度に等しくなる（最大値＝最小値）。

[Category:色空間](https://ja.wikipedia.org/wiki/Category:色空間 "wikilink")