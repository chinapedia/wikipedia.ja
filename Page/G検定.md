> この記事は[G検定](https://ja.wikipedia.org/wiki/G検定)から翻訳されています。


**G検定**（ジーけんてい）は[統計学的検定法](https://ja.wikipedia.org/wiki/統計学的検定法 "wikilink")で、[尤度比検定](../Page/尤度比検定.md "wikilink")の一種である。これまで[カイ二乗検定](../Page/カイ二乗検定.md "wikilink")が用いられていた場面で広く用いられつつある。

カイ二乗検定は[累積分布関数](../Page/累積分布関数.md "wikilink")への適合性や[分割表](https://ja.wikipedia.org/wiki/分割表 "wikilink")における[独立性の検定に広く用いられてきたが](../Page/独立_\(確率論\).md "wikilink")、実は[対数尤度](https://ja.wikipedia.org/wiki/対数尤度 "wikilink")の[近似](../Page/近似.md "wikilink")に基づくものであり、一方G検定は対数尤度を直接用いる方法である。カイ二乗検定は[カール・ピアソン](../Page/カール・ピアソン.md "wikilink")によって計算の容易な方法として導入されたのであるが、[コンピュータ](../Page/コンピュータ.md "wikilink")の普及によってG検定も決して煩雑な方法ではなくなってきた。特に1994年に出版されたソーカルとロルフの教科書（「生物統計学」第3版：参考文献）で推奨され、広く利用されるようになった。

ピアソンのカイ二乗検定統計量は

\(\chi^2 = \sum_{i} {(O_i - E_i)^2 \over E_i}\)

ここで O<sub>i</sub> は分割表の各マス目における出現頻度、Eは[帰無仮説](https://ja.wikipedia.org/wiki/帰無仮説 "wikilink")で期待される頻度で、すべてのマス目を合計する。それに対応する*G* は

\(G = 2\sum_{i} {O_i \cdot \ln(O_i/E_i) }\)

観察された頻度が、ある期待される頻度をもつ分布から抽出した[無作為](https://ja.wikipedia.org/wiki/無作為 "wikilink")[標本にもとづくものであるという帰無仮説を立てれば](../Page/標本_\(統計学\).md "wikilink")、*G* の分布はカイ二乗（[自由度](https://ja.wikipedia.org/wiki/自由度 "wikilink")は同じ）で近似される。

標本サイズが適切であればG検定とカイ二乗検定では同じ結論が得られるが、すべてのマス目に対して |*O<sub>i</sub>* − *E<sub>i</sub>* |\> *E<sub>i</sub>* となる場合には、ピアソンのカイ二乗検定でなくG検定を用いるのが望ましい。

標本数の小さい場合には、カイ二乗検定やG検定でなく、多項検定（適合性）、[フィッシャーの正確検定](https://ja.wikipedia.org/wiki/フィッシャーの正確検定 "wikilink")（分割表）、あるいはベイズ式仮説選択が望ましい。

## 参考文献

  - Sokal, R. R., & Rohlf, F. J. (1994). *Biometry: the principles and practice of statistics in biological research.*, 3rd edition. New York: Freeman. ISBN 0-7167-2411-1.

[Category:統計検定](https://ja.wikipedia.org/wiki/Category:統計検定 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")