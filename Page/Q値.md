> この記事は[Q値](https://ja.wikipedia.org/wiki/Q値)から翻訳されています。


<references />

**Q値**(、品質係数Q)は主に振動の状態を表す[無次元量](../Page/無次元量.md "wikilink")である。[弾性波](../Page/弾性波.md "wikilink")の伝播においては、媒質の吸収によるエネルギーの減少に関係する値である。振動においては、1周期の間に系に蓄えられるエネルギーを、系から散逸するエネルギーで割ったもので、この値が大きいほど振動が安定であることを意味する。また、Q値は振幅増大係数とされる場合もある。これは、[共振周波数](https://ja.wikipedia.org/wiki/共振周波数 "wikilink")近傍での強制振動における最大振幅が静的強制力による変位のQ倍となることから解釈される。[振動子](https://ja.wikipedia.org/wiki/振動子 "wikilink")や[電気回路](../Page/電気回路.md "wikilink")の場合には一般にQ値が高いほうが望ましいが、逆にQ値が高いほど応答性が悪くなり、起動時間が長くなるという面もある。

振動する物理量の実際の振動状態は、周波数軸に展開した振動振幅()や位相()のスペクトラムにより理解される。振動スペクトラムの共振ピーク近傍の形はその振動系の振動状態を特徴付ける。Q値とは

で定義される無次元数。ここで、\(\omega_0\)、\(\omega_1\)、\(\omega_2\) はそれぞれ共振ピークでの共振周波数、共振ピークの左側において振動エネルギーが共振ピークの半値となる周波数、共振ピークの右側において振動エネルギーが半値となる周波数である。ここで\({\omega_2 - \omega_1}\) を[半値幅](../Page/半値幅.md "wikilink")と呼ぶ。

Q値の低い機械振動系は振動エネルギーの分散が大きい系である。 Q値の高い構造物では一旦振動が開始されると振動が長く続く。

Q値が低い素材は振動がすぐに減少する性質がある。これを利用して防振材、防音材に用いられる。

## 電気工学

[電子工学](../Page/電子工学.md "wikilink")の分野でも[共振](../Page/共振.md "wikilink")回路の共振のピークの鋭さを表す値「Q」(Quality factor)として一般的に用いられる。定義は上記と同一であり、[インダクタ](../Page/インダクタ.md "wikilink")と[キャパシタ](https://ja.wikipedia.org/wiki/キャパシタ "wikilink")を用いた直列[共振回路の場合](https://ja.wikipedia.org/wiki/LC回路 "wikilink")、

</math>}}

と表せる。これはインダクタンス L を大きくしてキャパシタンス C を小さく、直列抵抗 R を少なくするほど Q が大きくなることを示す。このため、選択度を稼ぐ必要がある共振回路においては、インダクションコイルの線径を太くして抵抗値を押さえ、大径・粗ピッチで巻いて分布容量を減らすなどの工夫をする。 また、角振動数は、  </math>}} を用いることで、  と表せる。

また、[水晶振動子](../Page/水晶振動子.md "wikilink")は[LC共振回路](https://ja.wikipedia.org/wiki/LC共振回路 "wikilink")に比べて Q が大きいため、正確で安定した発振回路向けの共振回路として一般に用いられる。水晶自体が数百万に達する高いQ値を持っているため、それを利用した回路では、数千から数万が達成できる。一般的なLC共振器のQは数十程度で、周波数が高いほどQ値は下がる。

## 機械工学

1[自由度](https://ja.wikipedia.org/wiki/自由度 "wikilink")のばね－質量系において、Q値は[機械的抵抗](https://ja.wikipedia.org/wiki/機械的抵抗 "wikilink")を用いて表現できる。 {R} </math>}}

ここで M は[質量](../Page/質量.md "wikilink"), K は[弾性率](../Page/弾性率.md "wikilink")で R は機械的抵抗である。 ばね－質量系の[角振動数](https://ja.wikipedia.org/wiki/角振動数 "wikilink")を用いて、  </math>}} また、別の表現をすれば、  と導出できる。

Qは減衰定数 \(\zeta\) 、損失率 \(\eta\) を用いて、  と表される。

ここで、周期的に外力が作用する強制振動を考える。

この解は、  となるから、 sin成分とcos成分のそれぞれの係数を比較することにより連立方程式を立てて解くと、 \\right)^2}} \\left\[ \\left\[{1-\\left({\\omega \\over \\omega_n}\\right)^2}\\right\] \\cos \\omega t + 2\\zeta{\\omega \\over \\omega_n} \\sin \\omega t \\right\] </math>}}

このとき、共振周波数\[\omega = \omega_n\]における振動を考えると  \\sin \\omega t </math>}} したがって、

なお、静的荷重時の変位x<sub>0</sub>は、  となるから、共振周波数での振幅との比は、

したがって、共振周波数において、振動振幅は静的荷重時のQ倍に増大する。

## 光学

光学的には、空洞共振器のQ値は以下の式で求められる。

{P} </math>}} ここで\(\nu\) は共振周波数、 \(\mathcal{E}\) はキャビティに蓄えられるエネルギー、 \(P=-\frac{dE}{dt}\) は散逸率である。光学的Q値は、共振周波数をその共振器の半価幅で割ったものに等しい。キャビティ内の光子の寿命は、このQ値に比例する。 レーザーの技術の一つとして、キャビティのQ値を切り替えることによって、高出力を得ることができる。この技術は[Qスイッチ](https://ja.wikipedia.org/wiki/Qスイッチ "wikilink")と呼ばれている。

[メスバウアー効果](../Page/メスバウアー効果.md "wikilink")による共鳴現象のQ値は数ギガに達する。

## 材料科学

誘電体材料においてtanδの逆数として定義される。一般的には、誘電率の高い材料ほどQ値が低く、周波数の上昇に伴って低下する。したがって、Q値ではなく、周波数との積であるfQ積の値を用いて、材料の良否を判断することが多い。

## 関連項目

  - [水晶振動子](../Page/水晶振動子.md "wikilink")

  - [減衰係数](https://ja.wikipedia.org/wiki/減衰係数 "wikilink")

  - [ブラウン運動](../Page/ブラウン運動.md "wikilink")

  - [ローレンツ曲線](../Page/ローレンツ曲線.md "wikilink")

  - [誘電正接](../Page/誘電正接.md "wikilink")

  - [アッテネーション](https://ja.wikipedia.org/wiki/アッテネーション "wikilink")

  - [帯域](https://ja.wikipedia.org/wiki/帯域 "wikilink")

  - [フェーズマージン](https://ja.wikipedia.org/wiki/フェーズマージン "wikilink")

  -
## 参考文献

T. Ohira, "[What in the world is Q](http://online.qmags.com/MICW0616/default.aspx?sessionID=850FA6AABF03586A49DEC8908&cid=3213756&eid=19857&pg=44&mode=2#pg44&mode2)," IEEE Microwave Magazine, vol.17, no.6, pp.42-49, June 2016. ISSN 1527-3342.

## 外部リンク

  -
[Category:電気回路](https://ja.wikipedia.org/wiki/Category:電気回路 "wikilink") [Category:振動と波動](https://ja.wikipedia.org/wiki/Category:振動と波動 "wikilink") [Category:振動工学](https://ja.wikipedia.org/wiki/Category:振動工学 "wikilink") [Category:無次元数](https://ja.wikipedia.org/wiki/Category:無次元数 "wikilink")