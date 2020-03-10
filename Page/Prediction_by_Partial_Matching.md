> この記事は[Prediction by Partial Matching](https://ja.wikipedia.org/wiki/Prediction_by_Partial_Matching)から翻訳されています。


**Prediction by Partial Matching**(PPM)は1984年に[J.G.Cleary](https://ja.wikipedia.org/wiki/J.G.Cleary "wikilink")と[I.H.Witten](https://ja.wikipedia.org/wiki/I.H.Witten "wikilink")によって考案された[データ圧縮](../Page/データ圧縮.md "wikilink")アルゴリズムの1つ。 この改良版が[7-zip等に用いられている](../Page/7z.md "wikilink")。非常に高い圧縮率の反面、圧縮速度はかなり遅くメモリも多く消費するアルゴリズムである。

この亜種として[PPMC](https://ja.wikipedia.org/wiki/#PPMC "wikilink")、[PPMd](https://ja.wikipedia.org/wiki/#PPMd "wikilink")、[PPMZ等がある](https://ja.wikipedia.org/wiki/#PPMZ "wikilink")。

## 符号化の原理

aabacaabbaとデータを符号化したとして、次にどの記号が出現するかを[統計](../Page/統計.md "wikilink")的に[予測](https://ja.wikipedia.org/wiki/予測 "wikilink")する。 この場合、統計的にaの次にはaが出現する可能性が高い。逆にcが出現する可能性は低いであろう。このように出現[確率](https://ja.wikipedia.org/wiki/確率 "wikilink")に偏りがあると[ハフマン符号](../Page/ハフマン符号.md "wikilink")や[算術符号](../Page/算術符号.md "wikilink")で圧縮することが出来る。 しかし、上記の場合に次に出現する符号をaを50%、bを40%、cを10%と予測したとすると、他の記号は絶対に現れないということになり、新たな記号(dとする)が出現したときに対応できなくなってしまう。これを**ゼロ頻度問題**という。

そこで、PPMでは「今までに出現していない文字」として「**エスケープ(escape)**」という記号を加える。 上記の例であれば、aを45%、bを35%、cを5%などとして、エスケープには残りの15%を割り当てておく。これならば先ほどのように新しい記号dが出現したとしても、まずエスケープ記号を出力し、その後dを出力すればよい。更にこのとき、dを既知の記号として統計情報に加える。 このように、まだ現れていない記号に他の記号の確率を配分し、ゼロ頻度問題を回避することを**スムージング**という。 エスケープはスムージングの１つである。

また、エスケープには次のような役割もある。 先ほどの文字列の統計情報を利用するとき、aの次にはaが出現しやすいが、baの次にはcが出現しやすい。このように、予測に用いる[文脈](https://ja.wikipedia.org/wiki/文脈 "wikilink")の長さ(**次数またはorderという**)によって予想の結果は異なってしまう。次数は高いほうが正確な予想が出来ると思われるが、高い次数の文脈は統計情報が不足している場合が多い。 この解決策として、まず一番高い次数から予想をし、エスケープであれば1つ低い次数で予想しなおすという案があり、これによって適切な次数による予想が可能となる。

## エスケープの確率

先ほどの例ではエスケープには適当に15%を割り当てたが、実際にエスケープがどれくらいの確率であるかを推定することは重要である。符号化した記号が少なければエスケープの確率は高くなるだろう。逆に符号化が進み、多くの記号を符号化したころにはエスケープはあまり出現しないと考えられる。 エスケープ確率の推定方法はmethodと呼ばれいくつか提案されているが、中でもmethod Cとmethod Dは良い性能をみせる。

method A \(\frac{1}{n + 1}\)

method B \(\frac{u}{n }\)

method C \(\frac{u}{n+u}\)

method D \(\frac{u}{2n}\)

ここで、nは今までに出現した記号の総数。uはエスケープの総数。

## 種類

### PPMC

### PPMd

[RAR](../Page/RAR.md "wikilink")や[7z](../Page/7z.md "wikilink")などに採用されている、PPMの中で最も速い方式。場合によっては[Range Coderに匹敵するほど速い](https://ja.wikipedia.org/wiki/Range_Coder "wikilink")。それでも圧縮率はそこそこで、十分な圧縮率がある。

オリジナルのプログラムには様々なバージョンが存在する。

### PPMN

### PPMY

### PPMZ

PPM系列の中でもっとも圧縮率が高くなる方式。しかし、その分計算量は莫大に増え、実用にならないほど速度が遅い。

その為、改良しても速度が改善されにくく、サンプルプログラム以外に採用された例は無い。

亜種で圧縮率と速度を多少改善した**PPMZ2**が存在する。

## 関連項目

  - [データ圧縮](../Page/データ圧縮.md "wikilink")

[Category:データ圧縮](https://ja.wikipedia.org/wiki/Category:データ圧縮 "wikilink") [Category:アルゴリズム](https://ja.wikipedia.org/wiki/Category:アルゴリズム "wikilink")