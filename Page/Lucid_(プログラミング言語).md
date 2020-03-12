> この記事は[Lucid \(\)](https://ja.wikipedia.org/wiki/Lucid_\(\))から翻訳されています。


**Lucid** は[データフロープログラミング](../Page/データフロープログラミング.md "wikilink")言語である。非[ノイマン型](../Page/ノイマン型.md "wikilink") プログラミング言語の実験の為に設計された。Bill Wadge と Ed Ashcroft によって設計され、書籍 *Lucid, the Dataflow Programming Language* が出版された。

## 言語モデル

Lucid はデータ処理の際に[要求駆動モデル](https://ja.wikipedia.org/wiki/要求駆動モデル "wikilink")を採用している。Lucid の文は、[プロセッサ](../Page/プロセッサ.md "wikilink")のネットワークを定義する方程式と、その間をデータが流れる通信線として考える事が出来る。変数は無限に続く値のストリームであり、関数はフィルタか変換器である。反復は 'current' 変数と、'fby' 変数によってシミュレートされストリーム合成を行う事が出来る。

Lucid は無限に続くデータの列であるヒストリーの代数を基にしている。利用時には、ヒストリーは変化し続ける変数の値の記録と考える事が出来、first や next 等のヒストリー操作は名前から連想するとおり動作する。Lucid は当初、動作検証が非常にシンプルあるような、非常に厳格で数学的に純粋な単一代入言語として考えられていた。しかしながら、データフローの解釈は非常に重要であり、Lucid の発展に大きく影響を及ぼした。 [1](http://www.chilton-computing.org.uk/acd/dcs/projects/p026.htm)

## 言語の詳細

Lucid (とその他のデータフロー言語)では、まだ[束縛されていない変数を含む式は](https://ja.wikipedia.org/wiki/名前束縛 "wikilink")、変数が束縛されるまで待機してから実行される。x + y のような式は、x と y の双方が束縛されるまで待ってから式の値を返す。その結果重要なのは、関連する値を更新するためのロジックを明記しないという点であり、一般的な言語と比較してコード量を非常に少なくする事が出来る。

Lucid でのそれぞれの変数は値のストリームである。式 n = 1 fby n + 1 は、演算子 'fby' を使ってストリームを定義している。fby ('followed by' と読む) は直前の式の後に続く物を定義する。(この例では、ストリームは 1,2,3... を生成する。) ストリームの値は以下の演算子によって導かれる(使われる変数を x とする)。

'first x' - ストリーム x の最初の値を取得する。

'x' - ストリームの現在の値。

'next x' - ストリームの次の値を取得する。

'asa' - 条件が真になると何かを「出来るだけ早く (as soon as)」実行する演算子。

'x upon p' - upon はストリーム x の古い値を繰り返す演算子で、ストリーム p が真の時だけ新しい値に更新する。(これによりストリーム x の変化が遅くなる)。すなわち、x upon p は p が真の時に新しい値が現れるストリーム x である。

計算はフィルタ又は時間によって変化するデータの変換関数を定義する事によって実行される。

pLucid は Lucid の最初の実装だった。

## 例

### 数列の合計

`total`
`  where`
`     total = 0 fby total + x`
`  end;`

### 変化する平均

`running_avg`
`  where `
`     sum = first(input) fby sum + next(input);`
`     n = 1 fby n + 1;`
`     running_avg = sum / n;`
`  end;`

### 素数

[2](http://i.csc.uvic.ca/home/hei/lup/02.html)

`prime`
`  where`
`     prime = 2 fby (n whenever `[`isprime`](https://ja.wikipedia.org/wiki/isprime "wikilink")`(n));`
`     n = 3 fby n+2;`
`     isprime(n) = not(divs) asa divs or prime*prime > N`
`                     where`
`                       N is current n;`
`                       divs = N mod prime eq 0;`
`                     end;`
`  end`

#### データフローダイアグラム

` ---+1<--- -->isprime----`
` |         |              |`
` |         |              V`
`  ->fby--------------->whenever--->`
`     ^`
`     |`
`     2`

### クイックソート

[3](http://i.csc.uvic.ca/home/hei/lup/06.html)

`qsort(a) = if eof(first a) then a else follow(qsort(b0),qsort(b1)) fi`
`  where`
`     p = first a < a;`
`     b0 = a whenever p;`
`     b1 = a whenever not p;`
`     follow(x,y) = if xdone then y upon xdone else x fi`
`                     where`
`                        xdone = iseod x fby xdone or iseod x; `
`                     end`
`  end`

#### データフローダイアグラム

`    --------> whenever -----> qsort ---------`
`   |             ^                           |`
`   |             |                           |`
`   |            not                          |`
`   |             ^                           |`
`   |---> first   |                           |`
`   |       |     |                           |`
`   |       V     |                           |`
`   |---> less ---                            |`
`   |             |                           |`
`   |             V                           V`
`---+--------> whenever -----> qsort -----> conc -------> ifthenelse ----->`
`   |                                                       ^   ^`
`   |                                                       |   |`
`    --------> next ----> first ------> iseod --------------    |`
`   |                                                           |`
`    -----------------------------------------------------------`

### 平方根

`sqroot(avg(square(a)))`
`  where`
`     square(x) = x*x;`
`     avg(y)    = mean`
`        where`
`          n = 1 fby n+1;`
`          mean = first y fby mean + d;`
`          d = (next y - mean)/(n+1);`
`        end;`
`     sqroot(z) = approx asa  err < 0.0001`
`        where`
`          Z is current z;`
`          approx = Z/2 fby (approx + Z/approx)/2;`
`          err    = abs(square(approx)-Z);`
`        end;`
`   end`

### Hamming Problem

[4](http://i.csc.uvic.ca/home/hei/lup/01.html)

`h`
`   where`
`     h = 1 fby merge(merge(2 * h, 3 * h), 5 * h);`
`     merge(x,y) = if xx <= yy then xx else yy fi`
`        where `
`          xx = x upon xx <= yy;`
`          yy = y upon yy <= xx;`
`        end;`
`   end;`

#### データフローダイアグラム

`  --------------------*2---------`
` |       -------------*3---------|`
` |      |           --*5---------|`
` |      |          |             |`
` |      V          V             |`
`  --->merge----->merge----->fby-------->`
`                             ^`
`                             |`
`                             1`

## 外部リンク

  - [Language overview](http://c2.com/cgi/wiki?LucidLanguage)
  - [Evolution of Lucid](http://hopl.murdoch.edu.au/showlanguage2.prx?exp=960)
  - [Bill Wadge's home page](http://i.csc.uvic.ca/home/hei/hei.ise)
  - [Fluid Programming in Lucid](http://www.artima.com/weblogs/viewpost.jsp?thread=102839)
  - [Lucid page of HaskellWiki](http://www.haskell.org/haskellwiki/Lucid)
  - [Programming in Lucid](http://i.csc.uvic.ca/home/hei/lup/contents.html)
  - [An Eductive Interpreter](http://i.csc.uvic.ca/home/hei/ei/contents.ise)
  - [Lucid Primer](http://i.csc.uvic.ca/home/LucidPrimer/LPS.ise)
  - [Lucid like Interpreter in java](http://dataflow-programming.blogspot.com/)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")