> この記事は[斜めCT](https://ja.wikipedia.org/wiki/斜めCT)から翻訳されています。


**斜めCT**（ななめCT）とは、[X線](../Page/X線.md "wikilink")検査装置のうち傾斜[コーンビーム方式](https://ja.wikipedia.org/wiki/コーンビーム方式 "wikilink")を用いた[CT装置を指す](../Page/コンピュータ断層撮影.md "wikilink")。

名前のとおり、斜めCTは、X線を斜め方向から対象物体に照射し、検出器でその[透視画像](https://ja.wikipedia.org/wiki/透視画像 "wikilink")を各方向から撮影することで、対象物体の[断層](https://ja.wikipedia.org/wiki/断層 "wikilink")像を得る。一般的に、斜めCT装置では回転台に対象物体を置き、回転台を回すことによって各方向から撮影画像を得る。基板のような薄い物体の断層像を得て、その欠陥を発見することができる\[1\]。

2008年現在、斜めCTでは、検出器を垂直方向から水平方向まで置いて撮影した画像に対して、対象物体の断層像を得ることができる。対象物体の断層像を得る[アルゴリズム](../Page/アルゴリズム.md "wikilink")は、3次元CT画像再構成法である[FDK法](https://ja.wikipedia.org/wiki/FDK法 "wikilink")\[2\]から導出できる。すなわち、検出器を垂直方向に置いた時は、FDK法をそのまま使って画像再構成を行い、他の方向に置いた場合は、[座標変換を行って](../Page/媒介変数.md "wikilink")、FDK法の導出方法に合わせれば、すぐに再構成数式が導出できる。

## 応用領域

## 垂直検出器撮像方法および座標系

まず、検出器座標系を次のように表示する。

  -
    \(\vec{e}_u = (-\sin\lambda, \cos\lambda, 0)\), \(\vec{e}_w = (0, 0, 1)\).

また、

  -
    \(\overline{v}=x\cos\lambda+y\sin\lambda\)

とすると、検出器上の点 \((\overline{u},\overline{w})\) と対象物体の座標系の点 \((x, y, z)\) の関係は、次のように表示することができる。

  -
    \(\overline{u}=\frac{R}{R-\overline{v}}(-x\sin\lambda+y\cos\lambda)\), \(\overline{w}=\frac{R}{R-\overline{v}}(z-d) + d\).

## 垂直検出器撮像の再構成方法

コーンビームCT画像再構成であるFDK法は、次のように表示できる。

  -
    \(f(x,y,z) = -\frac{1}{4\pi^2}\int_0^{2\pi} d\lambda \frac{R^2}{(R-\overline{v})^2} \int du h(\overline{u} - u) g_\lambda(u, \overline{w}) \frac{R}{\sqrt{R^2+u^2+(\overline{w}-d)^2}}\).

上述の式において、関数\(h()\)はRampフィルタである。

## 水平検出器撮像方法および座標系

まず、検出器座標系を次のように表示する。

  -
    \(\vec{e}_p = (-\sin\lambda, \cos\lambda, 0)\), \(\vec{e}_q = (-\cos\lambda, -\sin\lambda, 0)\).

検出器上の点 \((\overline{p},\overline{q})\) と対象物体の座標系の点 \((x, y, z)\) の関係は、次のように表示することができる。

  -
    \(\overline{p}=\frac{d}{d-z}(-x\sin\lambda+y\cos\lambda)\), \(\overline{q}=-\frac{d}{d-z}(x\cos\lambda+y\sin\lambda) + \frac{Rz}{d-z}\).

## 水平検出器撮像の再構成方法

まず、座標変換を行い、その結果をFDK法を導出する式に合わせると、画像再構成式は次のようになる。

  -
    \(f(x,y,z) = -\frac{1}{4\pi^2}\int_0^{2\pi} d\lambda \frac{R^2}{(R-\overline{v})^2} \int dp h(\overline{p} - p) g_\lambda(p, \overline{q}) \frac{(R+\overline{q})^2}{R\sqrt{(R+\overline{q})^2+p^2+d^2}}\).

## 任意検出器撮像方法および座標系

まず、任意検出器座標系を次のように表示する。

  -
    \(\vec{e}_\varphi = (-\sin\lambda, \cos\lambda, 0)\), \(\vec{e}_\chi = (-\cos\lambda, -\sin\lambda, 0)\sin\theta + (0,0,1)\cos\theta\).

検出器上の点 \((\overline{\varphi},\overline{\chi})\) と対象物体の座標系の点 \((x, y, z)\) の関係は、次のように表示することができる。

  -
    \(\overline{\varphi}=\frac{(R\cos\theta+d\sin\theta)(-x\sin\lambda+y\cos\lambda)}{(R-x\cos\lambda-y\sin\lambda)\cos\theta + (d-z)\sin\theta}\), \(\overline{\chi}=\frac{Rz-d(x\cos\lambda+y\sin\lambda)}{(R-x\cos\lambda-y\sin\lambda)\cos\theta + (d-z)\sin\theta}\).

## 任意検出器撮像の再構成方法

まず、座標変換を行い、その結果をFDK法を導出する式に合わせると、画像再構成式は次のようになる。

  -
    \(f(x,y,z) = -\frac{1}{4\pi^2}\int_0^{2\pi} d\lambda \frac{R^2}{(R-\overline{v})^2} \int d\varphi h(\overline{\varphi} - \varphi) g_\lambda(\varphi, \overline{\chi}) \frac{(R+\overline{\chi}\sin\theta)^2}{R\sqrt{(R+\overline{\chi}\sin\theta)^2+\varphi^2+(d-\overline{\chi}\cos\theta)^2}}\).

## 脚注

[de:Computertomographie\#Spiral- oder Helix-CT](https://ja.wikipedia.org/wiki/de:Computertomographie#Spiral-_oder_Helix-CT "wikilink")

[Category:医療機器](https://ja.wikipedia.org/wiki/Category:医療機器 "wikilink") [Category:非破壊検査](https://ja.wikipedia.org/wiki/Category:非破壊検査 "wikilink") [Category:X線](https://ja.wikipedia.org/wiki/Category:X線 "wikilink") [Category:トモグラフィー](https://ja.wikipedia.org/wiki/Category:トモグラフィー "wikilink")

1.
2.