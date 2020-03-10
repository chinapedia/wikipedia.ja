> この記事は[T](https://ja.wikipedia.org/wiki/T)から翻訳されています。


*t*検定}}  {\\Gamma (\\nu /2)2^{\\nu /2-1}}</math>

  - ただし、\(\nu >0\) の場合。
  - \(K_{\nu} (x)\) は[ベッセル関数](https://ja.wikipedia.org/wiki/ベッセル関数 "wikilink")\[1\]

}} [統計学](../Page/統計学.md "wikilink")および[確率論](../Page/確率論.md "wikilink")において、***t*分布**（ティーぶんぷ、または**スチューデントの*t*分布**、）は、[連続確率分布](../Page/連続確率分布.md "wikilink")の一つであり、[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")する[母集団](../Page/母集団.md "wikilink")の平均と分散が未知で[標本サイズが小さい場合に](../Page/標本_\(統計学\).md "wikilink")[平均](../Page/平均.md "wikilink")を推定する問題に利用される。また、 2つの平均値の差の統計的[有意](../Page/有意.md "wikilink")性を検討する[t検定](https://ja.wikipedia.org/wiki/t検定 "wikilink")で利用される。*t*分布は、[一般化双曲型分布](https://ja.wikipedia.org/wiki/一般化双曲型分布 "wikilink")の特別なケースである。

***t*分布**は1908年に[ウィリアム・シーリー・ゴセットにより発表された](../Page/ウィリアム・ゴセット.md "wikilink")。当時の彼はビール醸造会社である[ギネスビール](https://ja.wikipedia.org/wiki/ギネスビール "wikilink")に雇用されており、[ギネスビール](https://ja.wikipedia.org/wiki/ギネスビール "wikilink")では秘密保持のため従業員による科学論文の公表を禁止していたので、彼はこの問題を回避するため「スチューデント」というペンネームを使用して論文を発表した\[2\]。

その後、[ロナルド・フィッシャー](https://ja.wikipedia.org/wiki/ロナルド・フィッシャー "wikilink")がこの論文の重要性を見抜き**スチューデントの*t*分布**と呼んだため、このように呼ばれるようになった。

## 導出

を[平均](../Page/期待値.md "wikilink") 、[分散](../Page/分散_\(確率論\).md "wikilink")  の[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")に従う[独立な確率変数とする](../Page/独立_\(確率論\).md "wikilink")。また標本平均を

\[\overline{X}_n =\frac{X_1 +\cdots +X_n}{n}\] とし、不偏分散を

\[U_n^2 =\frac{1}{n-1} \sum_{i=1}^n (X_i -\overline{X}_n )^2\] とする。ここで次の変数

\[T=\frac{\overline{X}_n -\mu}{U_n /\sqrt{n}}\] を考えると、これは

\[f(t)=\frac{\Gamma ((\nu +1)/2)}{\sqrt{\nu \pi \,}\, \Gamma (\nu /2)} (1+t^2/\nu)^{-(\nu+1)/2}\] （ただし  *n* − 1}},  は[ガンマ関数](../Page/ガンマ関数.md "wikilink")）という[確率密度関数](../Page/確率密度関数.md "wikilink")に従うことが、[ゴセット](https://ja.wikipedia.org/wiki/ゴセット "wikilink")によって示された。ここで  の従う分布を***t* 分布**（または**スチューデント分布**）と呼ぶ。 は[自由度](https://ja.wikipedia.org/wiki/自由度 "wikilink")と呼ばれる。この分布は  によるが、元の正規分布の[母数](../Page/母数.md "wikilink")である  や  にはよらない。この性質から、標本値から母集団の平均値を統計的に推定する[区間推定](https://ja.wikipedia.org/wiki/区間推定 "wikilink")や、母集団の平均値の[仮説検定](../Page/仮説検定.md "wikilink")に利用できる。

## 累積分布関数

[累積分布関数](../Page/累積分布関数.md "wikilink")は、正則[不完全ベータ関数](https://ja.wikipedia.org/wiki/不完全ベータ関数 "wikilink")を用いて以下のように表される。

\[\int_{-\infty}^t f(u)\, du=I_x \left( \frac{\nu}{2} ,\frac{\nu}{2} \right) =\frac{B\left( x;\frac{\nu}{2} ,\frac{\nu}{2} \right)}{B\left( \frac{\nu}{2} ,\frac{\nu}{2} \right)}\] ただし、

\[x=\frac{t+\sqrt{t^2 +\nu}}{2\sqrt{t^2 +\nu}}.\]

## モーメント

*t*分布の[モーメントは以下の式で表される](https://ja.wikipedia.org/wiki/モーメント_\(数学\)#確率分布のモーメント "wikilink")。

  - が奇数の場合

\[E(T^k)=\begin{cases}
0, &\quad 0<k<\nu \\
\mbox{NaN}, &\quad 0<\nu \leq k
\end{cases}\]

  - が偶数の場合

\[E(T^k )=\begin{cases}
\frac{\Gamma (\frac{k+1}{2})\Gamma (\frac{\nu-k}{2} )\nu^{k/2}}{\sqrt{\pi}\Gamma (\frac{\nu}{2} )}, &\quad 0<k<\nu \\
\infty, &\quad 0<\nu \leq k
\end{cases}\]

## 特別なケース

の値により、簡単な形となる。

###  1}} の場合

[コーシー分布](../Page/コーシー分布.md "wikilink")と一致する。

累積分布関数：

\[F(x)=\frac{1}{2} +\frac{1}{\pi} \arctan (x).\] 確率密度関数：

\[f(x)=\frac{1}{\pi (1+x^2 )}.\]

###  2}} の場合

累積分布関数：

\[F(x)=\frac{1}{2} \left[ 1+\frac{x}{\sqrt{2+x^2}} \right].\] 確率密度関数：

\[f(x)=\frac{1}{\left( 2+x^2 \right)^{3/2}}.\]

###  の場合

自由度  が （無限大）に近づくにつれ、分布は[正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")に近づく。

## 脚注

## 関連項目

  - [確率分布](../Page/確率分布.md "wikilink")
  - [非心*t*分布](../Page/非心t分布.md "wikilink")
  - [コーシー分布](../Page/コーシー分布.md "wikilink")
  - [正規分布](https://ja.wikipedia.org/wiki/正規分布 "wikilink")

[Category:確率分布](https://ja.wikipedia.org/wiki/Category:確率分布 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")

1.  Hurst, Simon, [The Characteristic Function of the Student-t Distribution](http://wwwmaths.anu.edu.au/research.reports/srr/95/044/), Financial Mathematics Research Report No. FMRR006-95, Statistics Research Report No. SRR044-95
2.  Walpole, Ronald; Myers, Raymond; Ye, Keying. *Probability and Statistics for Engineers and Scientists*. Pearson Education, 2002, 7th edition, pg. 237