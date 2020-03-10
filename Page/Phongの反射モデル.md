> この記事は[Phong](https://ja.wikipedia.org/wiki/Phong)から翻訳されています。


**Phongの反射モデル**（フォンのはんしゃモデル; ）とは、[3次元コンピュータグラフィックス](../Page/3次元コンピュータグラフィックス.md "wikilink")において、モデリングされた面 (surface) 上の点に影をつけるための照明と陰影（[シェーディング](https://ja.wikipedia.org/wiki/シェーディング "wikilink")）モデルである。**Phong照明**、**Phongライティング**とも。

このモデルは[ユタ大学](https://ja.wikipedia.org/wiki/ユタ大学 "wikilink")の[理学博士](https://ja.wikipedia.org/wiki/理学博士 "wikilink")である、によって開発され、1973年に"Illumination for Computer Generated Pictures"の題で学位論文として発表された。併せてこの論文中には、多角形面モデルからラスタライズされた個々の[ピクセル](../Page/ピクセル.md "wikilink")に対して、補間計算を行う方法も論述されていた。この補間技術は後述するように**[Phongシェーディング](https://ja.wikipedia.org/wiki/Phongシェーディング "wikilink")**として知られている。

## 概要

Phongの反射モデルでは、一般的なをより単純化して扱うことができる。このモデルでは、面上の点における陰影を決定する際に、次のような単純化ができる利点がある。

1.  このモデルは、「局所的な」反射モデルである。すなわち、[ラジオシティ](../Page/ラジオシティ.md "wikilink")のような[レイトレーシング](../Page/レイトレーシング.md "wikilink")で行うような二次反射を計算する必要はない。反射した光の減衰を補正するために、外部の「環境光」(ambient) の項をレンダリングする際に加えている。
2.  表面からの反射を3つの項目、すなわち「鏡面反射」(specular reflection)、「拡散反射」(diffuse reflection) と「環境反射」(ambient reflection) に分けている。

最初に、シーンにおける光源ごとに、鏡面反射成分 \(i_s\) と拡散反射成分 \(i_d\) を定義する。通常、それぞれ[RGB](../Page/RGB.md "wikilink")値である。また、アンビエント照明の制御は \(i_a\) でなされ、全ての光源の影響の総和として計算されることもある。

次に、それぞれの**材質** (material; 普通、あるシーンにおいて物体面に対して1対1で設定される) について、以下のものを定義する。

\[k_s\]: 鏡面反射係数。入射光に対する鏡面反射率

\[k_d\]: 拡散反射係数。入射光に対する拡散反射率 ([Lambert反射](https://ja.wikipedia.org/wiki/Lambert反射 "wikilink"))

\[k_a\]: 環境反射係数。シーン全体を照らす環境光の反射率

\[\alpha\]: その材質の**光沢度** (shininess) であり、光沢のある点から反射する光がどのくらい均等に反射するかを決める。より滑らかな表面ほど大きい。また、この定数が大きければ鏡面ハイライトが小さく強くなる。

さらに、すべての光源群の光を定義する。物体表面上の点からそれぞれの光源 (light) への方向ベクトルを\(L\)と置き、この表面上の点における[法線](https://ja.wikipedia.org/wiki/法線 "wikilink") (normal) を\(N\)、面上のその点において光線が完全に反射 (reflect) される方向を\(R\)とする。そして、(仮想的なカメラのような) [視点](https://ja.wikipedia.org/wiki/視点 "wikilink") (view) に向かう方向を\(V\)とする。

表面上の各点における陰影つまり光の強度 \(I_p\) は、次の方程式を用いて計算できる。これが**Phongの反射モデル**である。

\[I_p = k_a i_a + \sum_\mathrm{lights} (k_d (L \cdot N) i_d + k_s (R \cdot V)^{\alpha}i_s).\]

拡散反射光の項は視点の方向\(V\)には影響を受けない。拡散反射光の項はその点から視点方向を含むすべての方向について等しいからである。一方で、反射ベクトル\(R\)が視点ベクトル\(V\)の向きに非常に近い場合のみ、鏡面反射光の項が大きくなる。これは、\(R\)と\(V\)の間の角度のコサイン、つまり\(R\)と\(V\)のそれぞれの[正規化ベクトル](https://ja.wikipedia.org/wiki/正規化ベクトル "wikilink")の[内積](../Page/内積.md "wikilink") ([ドット積](https://ja.wikipedia.org/wiki/ドット積 "wikilink")) に、\(\alpha\)のべき乗で効いてくるからである。\(\alpha\)が大きければ、ほとんど鏡のように反射するような表現となり、鏡面反射光のハイライト面積は非常に小さくなる。これは、反射時に視点方向が反射ベクトルからずれていれば、コサイン値は1より小さくなり、大きい値でべき乗するとほとんど0に近くなるからである。

色をRGB値で表現する場合、この式はR、G、B成分のそれぞれについて別々に計算するのが一般的である。

Phongの反射は経験に基づくモデルであって、光の相互作用の物理的な説明に基づくものではなく、非公式な観察によるものである。Phongは、光沢の強い表面は鏡面ハイライトが小さく、その輝度がすぐに落ち込んでいること、一方で光沢の鈍い表面は鏡面ハイライトが大きく、その輝度の落ち込みがよりゆるやかであることに気がついた。

この方程式をグラフィカルに表現すると以下のようになる。

[655px](https://ja.wikipedia.org/wiki/ファイル:Phong_components_version_4.png "wikilink")

**環境反射光**と**拡散反射光**の色は同じである。環境反射の項は均一であるのに対し、拡散反射の項の輝度は表面の方向によって値が変わることに注意すること。**鏡面反射光**の色は白色で、表面に当たった光のすべてをほとんど反射するが、それが照らすハイライトは非常に狭い。

## メリットとデメリット

[OpenGL](../Page/OpenGL.md "wikilink")および[Direct3D](https://ja.wikipedia.org/wiki/Direct3D "wikilink")といったグラフィックス[APIを用いたリアルタイムレンダリングでは](https://ja.wikipedia.org/wiki/Application_Programming_Interface "wikilink")、描画速度などの制約から局所照明 (local illumination) モデルを採用することが多いが、Phong反射モデルはその単純さから計算量もリソース消費量も少なくて済むため、ソフトウェア ([CPU](../Page/CPU.md "wikilink")) もしくはハードウェア ([GPU](../Page/Graphics_Processing_Unit.md "wikilink")) による固定機能[シェーダー](https://ja.wikipedia.org/wiki/シェーダー "wikilink")として標準実装されていた（OpenGL 2.1およびDirect3D 9まで）。ハードウェア性能が向上し、プログラマブルシェーダーが一般化してからも、軽量さからPhong反射モデルが採用されることもある。なお固定機能の廃止されたOpenGL 3.1およびDirect3D 10以降では、Phong反射モデルの実現にはプログラマブルシェーダーが使用される。

一方で、極めて単純化されたおおざっぱな近似モデルであることから、表面下散乱や環境遮蔽といった複雑な拡散反射光や環境光による[大域照明](https://ja.wikipedia.org/wiki/大域照明 "wikilink") (global illumination) 現象を記述することはできない。

## Phongシェーディング補間法

面上の点で色を計算する反射モデルに加えて、Phongはまた、曲面のパッチを表現するラスタライズされた三角形において、ピクセルごとの色を計算するための補間方法も開発した。これらの反射モデルと補間法のトピックは時々「Phongシェーディング」という用語として一緒に扱われる。しかし「Phongシェーディング」という用語は、あくまで補間のための方法にのみ使われるものである。

## 関連項目

  - : Phongの反射モデルの開発者

  - [鏡面ハイライト](../Page/鏡面ハイライト.md "wikilink")

  - : Phongモデルの改良版

  - [双方向反射率分布関数](https://ja.wikipedia.org/wiki/双方向反射率分布関数 "wikilink") : 他の反射モデル

[Category:3DCG](https://ja.wikipedia.org/wiki/Category:3DCG "wikilink")