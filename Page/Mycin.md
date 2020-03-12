> この記事は[Mycin](https://ja.wikipedia.org/wiki/Mycin)から翻訳されています。


**Mycin**（マイシン）は、[スタンフォード大学](../Page/スタンフォード大学.md "wikilink")で[1970年代](../Page/1970年代.md "wikilink")初めに5、6年の歳月をかけて開発された[エキスパートシステム](../Page/エキスパートシステム.md "wikilink")である。[Lispで書かれ](https://ja.wikipedia.org/wiki/LISP "wikilink")、ブルース・ブキャナンとエドワード・ショートリッフェが開発した。[Dendral](../Page/Dendral.md "wikilink")から派生したものだが、かなり修正されている。システムは伝染性の[血液疾患](https://ja.wikipedia.org/wiki/血液疾患 "wikilink")を診断し、[抗生物質](https://ja.wikipedia.org/wiki/抗生物質 "wikilink")を推奨するようにデザインされていて、患者の体重のために供与量を調節する。Mycinの名称の由来は、抗生物質の多くはサフィックス「-mycin」がつくからである。

## 手法

Mycin は、かなり単純な[推論エンジン](../Page/推論エンジン.md "wikilink")を使い、500程度の規則からなる知識ベースを持つ。医師に対して、単純な「はい/いいえ」で答える質問や何らかの文章で答える質問をいくつもして、最終的に犯人と思われる細菌名のリスト（確率の高い順）とそれぞれの信頼度、なぜそう推論したかという理由、推奨される薬物療法のコースを示す。

Mycin は成功を収めたにも関わらず、現在では人工知能の講義などで、[アドホック](../Page/アドホック.md "wikilink")な確率的フレームワークを作ってしまうことへの警鐘を示す例とされることがある。Mycin は、確信度係数システムによってノイズが混入するため、推論の深さが制限されてしまった。この問題は、[ベイズ推定](../Page/ベイズ推定.md "wikilink")などの厳密な確率的フレームワークを採用することで防ぐことができる。

## 結果

スタンフォード医学部での調査によると、Mycin の診断結果は 65% の正しさであり、細菌感染の専門でない医師よりはよい結果だが、専門医の診断結果(80%)よりも悪かった。

## 実用

実のところ、Mycinは現場では決して使われなかった。これは性能が悪かったせいではない。スタンフォードの医学部で試用されたときには優れた性能を示した。むしろ倫理や法律の面で、コンピュータを医療に使って間違った診断を下した場合、誰が責任を取るのかという問題であった。また、人間の専門家がそのようなものを受け入れることへの抵抗もあった。

この開発の際や後のエキスパートシステムの開発に際しても、専門家の知識を引き出して規則にすることの困難さが明らかになった。後にこれが[知識工学](https://ja.wikipedia.org/wiki/知識工学 "wikilink")を生むこととなる。

## 関連項目

  - [CADUCEUS](https://ja.wikipedia.org/wiki/CADUCEUS "wikilink")

## 参考文献

  - *The AI Business: The commercial uses of artificial intelligence*, ed. Patrick Winston and Karen A. Prendergast. ISBN 0-262-23117-4

## 外部リンク

  - *[Rule-Based Expert Systems: The MYCIN Experiments of the Stanford Heuristic Programming Project](http://www.aaaipress.org/Classic/Buchanan/buchanan.html)* -(edited by Bruce G. Buchanan and Edward H. Shortliffe; ebook version)
  - [TMYCIN](http://www.cs.utexas.edu/users/novak/tmycin.html), Mycinベースのシステム（英語）
  - ["MYCIN: A Quick Case Study"](http://www.cee.hw.ac.uk/~alison/ai3notes/section2_5_5.html)
  - [" SOME EXPERT SYSTEM NEED COMMON SENSE"](http://www-formal.stanford.edu/jmc/someneed/someneed.html) -(by [John McCarthy](../Page/ジョン・マッカーシー.md "wikilink"))
  - ["Expert Systems"](http://www.cs.cf.ac.uk/Dave/AI1/mycin.html)

[Category:エキスパートシステム](https://ja.wikipedia.org/wiki/Category:エキスパートシステム "wikilink") [Category:スタンフォード大学](https://ja.wikipedia.org/wiki/Category:スタンフォード大学 "wikilink")