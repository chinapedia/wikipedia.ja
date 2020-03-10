> この記事は[Discrete optimized protein energy](https://ja.wikipedia.org/wiki/Discrete_optimized_protein_energy)から翻訳されています。


**DOPE**あるいは**D**iscrete **O**ptimized **P**rotein **E**nergy\[1\]は、[タンパク質構造予測](../Page/タンパク質構造予測.md "wikilink")においてを評価するために使われるである。DOPEは標本の天然構造に依存した半径を持つ均一な球中の相互作用していない原子に対応する改良基準状態に基づく。したがって、DOPEは 天然構造の有限ば球形から成る。人気のあるホモロジーモデリングプログラム[MODELLER](https://ja.wikipedia.org/wiki/MODELLER "wikilink")に実装されている。MODELLERによって多数の繰り返しにより生成された[タンパク質モデルのエネルギーを評価するために使われる](https://ja.wikipedia.org/wiki/力場_\(化学\) "wikilink")。これによって空間的拘束を満足するホモロジーモデルが生み出される。最小のmolpdf（MODELLER objective function）を返すモデルを最も良い推定構造として選ぶことができ、さらにDOPE scoreを使って評価するために使うことができる。現行バージョンのMODELLERソフトウェアと同様に、DOPEは[Python](../Page/Python.md "wikilink")で実装されており、MODELLER環境内で動作する。DOPE法は一般的に全体的な構造モデルの品質を評価するために使うことができる。別法として、DOPEは入力モデルの残基毎のエネルギープロファイルを生成することもでき、これによってユーザーは構造モデル中の問題のある領域の見当を付けることができる。

## 出典

<references />

## 外部リンク

  - [MODELLER main site](http://www.salilab.org/modeller)
  - [MODELLER manual](http://www.salilab.org/modeller/manual/)

[Category:タンパク質構造](https://ja.wikipedia.org/wiki/Category:タンパク質構造 "wikilink") [Category:長大な項目名](https://ja.wikipedia.org/wiki/Category:長大な項目名 "wikilink")

1.