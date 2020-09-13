> この記事は[T分布](https://ja.wikipedia.org/wiki/T分布)から翻訳されています。


*t*検定}}  {\\Gamma (\\nu /2)2^{\\nu /2-1}}</math>

  - ただし、\(\nu >0\) の場合。
  - \(K_{\nu} (x)\) は[ベッセル関数](../Page/ベッセル関数.md "wikilink")\[1\]

}} [統計学](../Page/統計学.md "wikilink")および[確率論](../Page/確率論.md "wikilink")において、***t*分布**（ティーぶんぷ、または**スチューデントの*t*分布**、）は、[連続確率分布](../Page/連続確率分布.md "wikilink")の一つであり、[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")する[母集団](../Page/母集団.md "wikilink")の平均と分散が未知で[標本サイズが小さい場合に](../Page/標本_\(統計学\).md "wikilink")[平均](../Page/平均.md "wikilink")を推定する問題に利用される。また、 2つの平均値の差の統計的[有意](../Page/有意.md "wikilink")性を検討する[t検定](https://ja.wikipedia.org/wiki/t検定 "wikilink")で利用される。*t*分布は、[一般化双曲型分布](https://ja.wikipedia.org/wiki/一般化双曲型分布 "wikilink")の特別なケースである。

***t*分布**は1908年に[ウィリアム・シーリー・ゴセットにより発表された](../Page/ウィリアム・ゴセット.md "wikilink")。当時の彼はビール醸造会社である[ギネスビール](https://ja.wikipedia.org/wiki/ギネスビール "wikilink")に雇用されており、[ギネスビール](https://ja.wikipedia.org/wiki/ギネスビール "wikilink")では秘密保持のため従業員による科学論文の公表を禁止していたので、彼はこの問題を回避するため「スチューデント」というペンネームを使用して論文を発表した\[2\]。

その後、[ロナルド・フィッシャー](../Page/ロナルド・フィッシャー.md "wikilink")がこの論文の重要性を見抜き**スチューデントの*t*分布**と呼んだため、このように呼ばれるようになった。

## 導出

を[平均](../Page/期待値.md "wikilink") 、[分散](../Page/分散_\(確率論\).md "wikilink")  の[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")に従う[独立な確率変数とする](../Page/独立_\(確率論\).md "wikilink")。また標本平均を

\[\overline{X} =\frac{X_1 +\cdots +X_n}{n}\] とし、不偏分散を

\[S^2 =\frac{1}{n-1} \sum_{i=1}^n (X_i -\overline{X} )^2\] とする。ここで次の変数

\[t=\frac{\overline{X} -\mu}{S /\sqrt{n}}\] を考えると、これは

\[f(t)=\frac{\Gamma ((\nu +1)/2)}{\sqrt{\nu \pi \,}\, \Gamma (\nu /2)} (1+t^2/\nu)^{-(\nu+1)/2}\] （ただし  *n* − 1}},  は[ガンマ関数](../Page/ガンマ関数.md "wikilink")）という[確率密度関数](../Page/確率密度関数.md "wikilink")に従うことが、[ゴセット](https://ja.wikipedia.org/wiki/ゴセット "wikilink")によって示された。ここで  の従う分布を***t* 分布**（または**スチューデント分布**）と呼ぶ。 は[自由度](https://ja.wikipedia.org/wiki/自由度 "wikilink")と呼ばれる。この分布は  によるが、元の正規分布の母標準偏差 にはよらないという重要な性質を持っている。

この確率密度関数は、元の正規分布の[母数](../Page/母数.md "wikilink")であるおよびが既知と仮定しているので、厳密には条件付確率密度関数\(f(t|\mu,\sigma)\)と書くべきものである。およびを確率変数と考え、その確率密度関数を適当に仮定し(例えばテーブル状の一様分布関数)、[ベイズの定理](../Page/ベイズの定理.md "wikilink")を適用することによって、標本平均\(\overline{X}\) および不偏標準偏差\(S\)が既知の場合の条件付確率密度関数\(f(t|\overline{X},S)\)を計算することができる(もう少し正確に言えば、まず条件付確率密度関数\(f(\overline{X},S|\mu,\sigma)\)を求め、これにベイズの定理を適用して\(f(\mu,\sigma|\overline{X},S)\)を求め、さらにについて積分して\(f(t|\overline{X},S)\)を求める)。実はこの関数は\(f(t|\mu,\sigma)\)と全く同じ形をしている。つまり、

\[f(t|\overline{X},S)=\frac{\Gamma ((\nu +1)/2)}{\sqrt{\nu \pi \,}\, \Gamma (\nu /2)} (1+t^2/\nu)^{-(\nu+1)/2}\]

\[t=\frac{\overline{X} -\mu}{S /\sqrt{n}}\]

である。これが、t分布が母標準偏差 にはよらないという性質の反映である。不偏標準偏差\(S\)は既知であるから、tの確率分布から母平均値の確率分布を求めることができ、これを用いての[区間推定](https://ja.wikipedia.org/wiki/区間推定 "wikilink")や、[仮説検定](../Page/仮説検定.md "wikilink")を行うことができる。

t分布を用いた母集団の平均値の区間推定では、t=0について対称な区間で、その区間に亘る確率密度の積分値が95%となる区間(95%信頼区間)を考え、これに対応するの区間を[信頼区間](https://ja.wikipedia.org/wiki/信頼区間 "wikilink")(CI)とする方法が広く用いられている(99%信頼区間を用いる場合も有る)。

t分布を用いた母集団の平均値の仮説検定では、=0と仮定した場合([帰無仮説](https://ja.wikipedia.org/wiki/帰無仮説 "wikilink")、Null Hypothesis)のtの値が、上記の信頼区間(95%あるいは99%)に含まれるか否かを判定基準とし、含まれる場合は、が0ではないという仮説は統計的に有意ではないと判定し、区間からはみ出す場合は、が0ではないという仮説は統計的に有意であると判定する。

## 累積分布関数

[累積分布関数](../Page/累積分布関数.md "wikilink")は、正則[不完全ベータ関数](../Page/不完全ベータ関数.md "wikilink")を用いて以下のように表される。

\[\int_{-\infty}^t f(u)\, du=I_x \left( \frac{\nu}{2} ,\frac{\nu}{2} \right) =\frac{B\left( x;\frac{\nu}{2} ,\frac{\nu}{2} \right)}{B\left( \frac{\nu}{2} ,\frac{\nu}{2} \right)}\] ただし、

\[x=\frac{t+\sqrt{t^2 +\nu}}{2\sqrt{t^2 +\nu}}.\]

## モーメント

*t*分布の[モーメントは以下の式で表される](https://ja.wikipedia.org/wiki/モーメント_\(数学\)#確率分布のモーメント "wikilink")。

  - が奇数の場合

\[E(t^k)=\begin{cases}
0, &\quad 0<k<\nu \\
\mbox{NaN}, &\quad 0<\nu \leq k
\end{cases}\]

  - が偶数の場合

\[E(t^k )=\begin{cases}
\frac{\Gamma (\frac{k+1}{2})\Gamma (\frac{\nu-k}{2} )\nu^{k/2}}{\sqrt{\pi}\Gamma (\frac{\nu}{2} )}, &\quad 0<k<\nu \\
\infty, &\quad 0<\nu \leq k
\end{cases}\]

## 特別なケース

の値により、簡単な形となる。

###  1}} の場合

[コーシー分布](../Page/コーシー分布.md "wikilink")と一致する。

累積分布関数：

\[F(t)=\frac{1}{2} +\frac{1}{\pi} \arctan (t).\] 確率密度関数：

\[f(t)=\frac{1}{\pi (1+t^2 )}.\]

###  2}} の場合

累積分布関数：

\[F(t)=\frac{1}{2} \left[ 1+\frac{t}{\sqrt{2+t^2}} \right].\] 確率密度関数：

\[f(t)=\frac{1}{\left( 2+t^2 \right)^{3/2}}.\]

###  の場合

自由度  が （無限大）に近づくにつれ、分布は[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")に近づく。

## 脚注

## 参考文献

## 関連項目

  - [確率分布](../Page/確率分布.md "wikilink")
  - [非心*t*分布](../Page/非心t分布.md "wikilink")
  - [コーシー分布](../Page/コーシー分布.md "wikilink")
  - [正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")

[Category:確率分布](https://ja.wikipedia.org/wiki/Category:確率分布 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  Hurst, Simon, [The Characteristic Function of the Student-t Distribution](http://wwwmaths.anu.edu.au/research.reports/srr/95/044/), Financial Mathematics Research Report No. FMRR006-95, Statistics Research Report No. SRR044-95
2.  Walpole, Ronald; Myers, Raymond; Ye, Keying. *Probability and Statistics for Engineers and Scientists*. Pearson Education, 2002, 7th edition, pg. 237