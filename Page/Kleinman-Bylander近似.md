> この記事は[Kleinman-Bylander](https://ja.wikipedia.org/wiki/Kleinman-Bylander)から翻訳されています。


**Kleinman-Bylander近似**（クレインマン・バイランダーきんじ）は、[擬ポテンシャル](../Page/擬ポテンシャル.md "wikilink")の[非局所部分](https://ja.wikipedia.org/wiki/非局所部分 "wikilink")の計算量を*N*の２乗のオーダーから*N*のオーダーまで減らす近似\[1\]。ここで*N*は、[平面波](../Page/平面波.md "wikilink")基底の数（通常、*N*<sup>2</sup>のオーダーでの計算量は扱う系が大きくなれば膨大なものになる）。Kleinman-Bylanderの分離形とも言う。

擬ポテンシャル*V*<sub>PS</sub>(r)は、局所部分と非局所部分とからなる。

\[V_{\text{PS}} (r) = V_{\text{local}} + \sum_l | l \rangle V_{\text{non-local}}^l (r) \langle l |\]

ここで、\(l \,\)は[軌道角運動量](https://ja.wikipedia.org/wiki/軌道角運動量 "wikilink")、\(V_{\text{local}} (r)\)が局所部分、\(V_{\text{non-local}}^l (r)\)が非局所部分である。*r*は動径方向の座標。この非局所部分を次のように分離するのが、Kleinman-Bylander近似である。

\[V_{\text{non-local}}^{l, \text{KB}} (r) = \frac{ |V_{\text{non-local}}^l | \phi_l^{\text{PS}} \rangle \langle \phi_l^{\text{PS}} | V_{\text{non-local}}^l | }{\langle \phi_l^{\text{PS}} | V_{\text{non-local}}^l | \phi_l^{\text{PS}} \rangle }\]

*φ<sub>l</sub>*<sup>PS</sup>は擬波動関数と言い、擬ポテンシャルを解くことによって得られる（擬似的な）[波動関数](../Page/波動関数.md "wikilink")である。上記の分離された形を使うことによって、[逆格子空間](https://ja.wikipedia.org/wiki/逆格子空間 "wikilink")で考えた非局所部分の和は、[逆格子ベクトル](../Page/逆格子ベクトル.md "wikilink")*G*の数（平面波基底の数に相当）について***G***と***G**'*の二重の和が必要であったものが、***G***のみの一重の和のみでよくなる。

この近似を用いた場合の問題点は、[バンド計算](../Page/バンド計算.md "wikilink")において[ゴーストバンド](https://ja.wikipedia.org/wiki/ゴーストバンド "wikilink")が生じる危険があることである。[2004年](../Page/2004年.md "wikilink")現在、これを完全かつ確実に排除する確たる指導原理はない。

## 参考文献

\[1\] L. Kleinman and D. M. Bylander, Phys. Rev. Lett., **48** (1982) 1425.

## 関連項目

  - [擬ポテンシャル](../Page/擬ポテンシャル.md "wikilink")

[Category:バンド計算](https://ja.wikipedia.org/wiki/Category:バンド計算 "wikilink")