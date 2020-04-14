> この記事は[Sinc関数](https://ja.wikipedia.org/wiki/Sinc関数)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:Sinc_function_\(both\).svg "wikilink") **sinc 関数**（ジンクかんすう、シンクかんすう）は、正弦関数をその変数で割って得られる[初等関数](../Page/初等関数.md "wikilink")である。sinc(*x*), Sinc(*x*), sinc *x* などで表される。

## 定義

sinc 関数は、正規化 sinc 関数と非正規化 sinc 関数という名で区別される、2種類の定義を持つ。

1.  [デジタル信号処理](../Page/デジタル信号処理.md "wikilink")などでは、次の**正規化 sinc 関数**（**標本化関数**ともいう）が普通である。
      - \(\operatorname{sinc}(x) = \frac{\sin \pi x}{\pi x}.\)
2.  [数学](../Page/数学.md "wikilink")では、次の歴史的な**非正規化 sinc 関数**が使われる。
      - \(\operatorname{sinc}(x) = \frac{\sin x}{x}.\)

いずれの場合も、[可除特異点](https://ja.wikipedia.org/wiki/可除特異点 "wikilink")である 0 での値が必要であればしばしば明示的に sinc(0) = 1 が定義として与えられる。sinc 関数はいたるところ[解析的である](../Page/解析関数.md "wikilink")。

sinc 関数は **カーディナル・サイン** (cardinal sine) とも呼ばれ、"sinc" () の関数名はラテン語の *sinus cardinalis* を短縮したものである。

## sinc関数の性質

特にことわらないかぎり、正規化sinc関数について述べる。 非正規化sinc関数は、[スケールファクタ](https://ja.wikipedia.org/wiki/スケールファクタ "wikilink") \(\pi\) が違うだけなので、非正規化sinc関数についての式を得るには、\(x \leftarrow x / \pi\)を代入すればいい。

### 特殊値など

  - \(\operatorname{sinc}(k) = \delta_{0k}, ( k \in \mathbb{Z})\)
      - ただし、\(\mathbb{Z}\)は[整数](../Page/整数.md "wikilink")の集合、\(\delta_{ij}\)は[クロネッカーのデルタ](../Page/クロネッカーのデルタ.md "wikilink")。
      - つまり、\(\operatorname{sinc}(0) = 1, \ \operatorname{sinc}(\pm 1) = \operatorname{sinc}(\pm 2) = \cdots = 0\)である。
  - \(\lim_{x \rightarrow \pm \infty} \operatorname{sinc}(x) = 0\)
  - \(\left. \frac{d}{dx}\operatorname{sinc}(x) = 0 \right|_{x = a} \iff \operatorname{sinc}(a) = \cos \pi a\)

### フーリエ変換

  - \(\operatorname{rect}(x) \leftrightarrow^\mathfrak{F} \operatorname{sinc}(f) = \operatorname{sinc}(\frac{\omega}{2\pi}),\) ただし、\(\operatorname{rect}(x) = \begin{cases} 1, & ( |x| \leqq \frac{1}{2}) \\ 0, & ( |x| > \frac{1}{2}) \end{cases}\)
      - ただし、\(f(x) \leftrightarrow^\mathfrak{F} F(\omega)\)は[フーリエ変換](../Page/フーリエ変換.md "wikilink")対、\(\operatorname{rect}(x)\)は（単位）[矩形関数](https://ja.wikipedia.org/wiki/矩形関数 "wikilink")。つまり、矩形関数のフーリエ変換はsinc関数、sinc関数のフーリエ変換は矩形関数である。

### テイラー展開

  - \(\operatorname{sinc}(x) = \sum^{\infin}_{n=0} \frac{(-1)^n\pi^{2n}}{(2n+1)!} x^{2n}\)

### 定積分

  - \(\int_{0}^{\infty} \operatorname{sinc}(x) \, dx = \frac{1}{2}, \quad \int_{-\infty}^{\infty} \operatorname{sinc}(x) \, dx = 1\)
  - \(\int_{0}^{\infty} \operatorname{sinc}^2(x) \, dx = \frac{1}{2}, \quad \int_{-\infty}^{\infty} \operatorname{sinc}^2(x) \, dx = 1 \quad \left(\operatorname{sinc}^2(x) = \{\operatorname{sinc}(x)\}^2 \right)\)
  - \(\int_{0}^{\infty} | \operatorname{sinc}(x) | \, dx = \infty, \quad \int_{-\infty}^{\infty} | \operatorname{sinc}(x) | \, dx = \infty\)

### 不定積分

  - \(\mathrm{Si}(x) = \int_{0}^{x} \frac{\sin t}{t} \, dt = \sum_{k = 0}^{\infty} \frac{ (-1)^k x^{2k+1} }{ (2k+1)(2k+1)! }\)
      - （非正規化）sinc関数の不定積分を[正弦積分](https://ja.wikipedia.org/wiki/正弦積分 "wikilink")と呼び、\(\operatorname{Si}(x)\)で表す。\(\operatorname{Si}(x)\)は[特殊関数](https://ja.wikipedia.org/wiki/特殊関数 "wikilink")である。

### 直交性

  - \(\int_{-\infty}^{\infty} \operatorname{sinc}(x-i)\operatorname{sinc}(x-j) \, dx = \delta_{ij}, ( i, j \in \mathbb{Z})\)
      - sinc関数の平行移動同士は[直交](../Page/直交.md "wikilink")する。

### 無限積

  - \(\operatorname{sinc}(x) = \prod_{k = 1}^{\infty} \cos \pi\frac{x}{2^k}\)
  - \(\operatorname{sinc}(x) = \prod_{k = 1}^{\infty} \left( 1 - \frac{x^2}{k^2} \right)\)

## 信号処理への応用

さまざまな用途が考えられるが、[コンパクト台をもたない](https://ja.wikipedia.org/wiki/コンパクト・サポート "wikilink")（非0の値が有限区間に限定されていない）ため、非常に多くの計算量を要することが多い。有限長で計算を打ち切らなければならないことも多く、無限長では生じない問題が発生することもある。概して、理論的背景やシミュレーションにとどまることが多い。

  - 直交性と ±∞ での収束性から、直交[ウェーブレット変換](../Page/ウェーブレット変換.md "wikilink")の[基底に用いる](https://ja.wikipedia.org/wiki/基底関数 "wikilink")。ただし、コンパクト台をもたないため、計算量が （ は[ランダウの記号](../Page/ランダウの記号.md "wikilink")）で増える。これは、コンパクト台をもつ基底だと計算量が  であることに比べ、大きなデメリットである。
  - sinc 関数のフーリエ変換が矩形関数であることから、[リサンプリング](https://ja.wikipedia.org/wiki/リサンプリング "wikilink")や[内挿](../Page/内挿.md "wikilink")の[補間カーネル](https://ja.wikipedia.org/wiki/補間カーネル "wikilink")（[低域通過フィルタ](https://ja.wikipedia.org/wiki/低域通過フィルタ "wikilink")）に用いる。無限系列の信号に対しては、sinc 関数は理想的な補間カーネルである。しかし、コンパクト台をもたないことが実際の有限長の信号を処理する際には問題となるため、実際の信号処理では、sinc 関数に似たコンパクト台をもつ関数である、3次畳み込み関数や、ランツォシュ (Lanczos) フィルタなどが使われることが多い。
  - 矩形関数のフーリエ変換がsinc 関数であることから、sinc 関数を使えば、理想的な[D/A変換ができる](../Page/デジタル-アナログ変換回路.md "wikilink")。ただしこれは、重要な概念ではあるが、実際にこの方法で D/A 変換が行われるわけではない。

## 参考文献

  -
## 関連項目

  - [アンチエイリアス](../Page/アンチエイリアス.md "wikilink")
  - [矩形波](../Page/矩形波.md "wikilink")
  - [三角関数](../Page/三角関数.md "wikilink")
  - [標本化定理](../Page/標本化定理.md "wikilink")
  - [ボールウェイン積分](https://ja.wikipedia.org/wiki/ボールウェイン積分 "wikilink")

## 外部リンク

  - \- 佐藤郁郎

  -
[Category:初等関数](https://ja.wikipedia.org/wiki/Category:初等関数 "wikilink") [Category:信号処理](https://ja.wikipedia.org/wiki/Category:信号処理 "wikilink") [Category:数学に関する記事](https://ja.wikipedia.org/wiki/Category:数学に関する記事 "wikilink")