> この記事は[ELIZA](https://ja.wikipedia.org/wiki/ELIZA)から翻訳されています。


**ELIZA効果**（イライザこうか、）は、意識的にはわかっていても、無意識的に[コンピュータ](../Page/コンピュータ.md "wikilink")の動作が人間と似ていると仮定する傾向を指す。これは、プログラミングの限界の自覚と[プログラムの](../Page/プログラム_\(コンピュータ\).md "wikilink")[出力](https://ja.wikipedia.org/wiki/出力 "wikilink")を生む動作との微妙な[認知的不協和](https://ja.wikipedia.org/wiki/認知的不協和 "wikilink")の結果とされる。ELIZA効果は[人工知能](../Page/人工知能.md "wikilink")研究における重要な発見であり、[チューリングテスト](https://ja.wikipedia.org/wiki/チューリングテスト "wikilink")についてそれまで考えられていたような、言語（文字）を通した会話というだけではなく、人間の認知的性質といったことについても、より眼が向けられるようになった。

## 起源

ELIZA効果の名称は、[1966年](../Page/1966年.md "wikilink")に発表された[おしゃべりボット](https://ja.wikipedia.org/wiki/おしゃべりボット "wikilink")の元祖「[ELIZA](../Page/ELIZA.md "wikilink")」に由来し、これは[来談者中心療法](../Page/来談者中心療法.md "wikilink")のパロディであった。ELIZA はユーザーが言及した話題に関して質疑応答するようにプログラムが組まれていた。

ELIZAは、ユーザーの感情を引き出すという意味で驚くほど成功した。しかし、ELIZAのコードは単にそのように設計されていただけで、会話を理解しているわけではない。こういった対話を研究した結果、ユーザーはELIZAが単なるシミュレーションであると意識の上ではわかっていても、無意識的にELIZAが話題に興味を持っているように感じていることが明らかとなった。

## 論理誤謬

ELIZA効果は、以下のような[後件肯定](https://ja.wikipedia.org/wiki/後件肯定 "wikilink")の[論理誤謬](https://ja.wikipedia.org/wiki/論理誤謬 "wikilink")の特殊ケースである。

プログラムが X によって動機付けされているとしても、観測された振る舞い Y が X という動機から発したかどうかは不明である。さらにいえば、そのプログラムが X によって動機付けされているかどうかを示すことは不可能である。多くの場合、プログラムの動機付けという考え方自体がありえない。

ELIZA効果は、[擬人観](../Page/擬人観.md "wikilink")よりも[論理誤謬](https://ja.wikipedia.org/wiki/論理誤謬 "wikilink")の程度は少ない。ユーザーはそのコンピュータが人間でないことを知っているし、完全な[人工知能](../Page/人工知能.md "wikilink")でないこともわかっている。それにもかかわらず、ユーザーはシステムの振る舞いが人間の振る舞いに似ているとき、同じ原因があると暗黙のうちに仮定する。しかし、コンピュータは人間のような感情を持たないため、この仮定は誤りである。プログラマはユーザーが仮定するような動機付けをしようと考えていたかもしれないが、それをプログラムの反応だけから推論することはできない。プログラムの振る舞いは予期しない副作用である可能性もある。

コンピュータがそのような仮定されたような形で動機付けされることがないとユーザーが理解した時点で ELIZA効果は解消される。

## 利点と欠点

人工知能や[ヒューマンマシンインタフェース](https://ja.wikipedia.org/wiki/ヒューマンマシンインタフェース "wikilink")のプログラミングにおいて、意図的にELIZA効果を利用することがある。これは、[チューリングテスト](https://ja.wikipedia.org/wiki/チューリングテスト "wikilink")に合格するためだったり、[計算記号論](https://ja.wikipedia.org/wiki/計算記号論 "wikilink")の研究の一環だったりする。この戦略は[コーディング](https://ja.wikipedia.org/wiki/コーディング "wikilink")上は効率的だが、危険でもある。ユーザーがELIZA効果が発生していることに気づいた場合、その無意識的な仮定を否定することによって同時にプログラミング手法そのものを推論する。結果としてチューリングテストには不合格となる。人工知能プログラマはELIZA効果を避けようと努力すると、同時にそのプログラムの出力のその他の問題点にも気づかなくなる。

ELIZA効果は[プログラミング言語](../Page/プログラミング言語.md "wikilink")の設計にも活用される。例えば、“+” という記号は文脈がどうであれ、加算を意味しているとみなすことが多い。同じ記号(“+”)は文字列の[連結](https://ja.wikipedia.org/wiki/連結 "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")を表すのにも使われる。プログラマは[演算子オーバーロード](https://ja.wikipedia.org/wiki/演算子オーバーロード "wikilink")のことを知らなくても、“+” が2種類の機能を持っていることを自然に受け止めている。つまり、これも一種のELIZA効果的な仮定「[驚き最小の原則](https://ja.wikipedia.org/wiki/驚き最小の原則 "wikilink")」が働いているとみることができる。

ELIZA効果は、ユーザーの仮定とプログラムの振る舞いが一致しない場合には逆効果となる。例えば、[デバッグ](../Page/デバッグ.md "wikilink")の際にプログラムの動作の真の原因をわかりにくくするなどの効果が考えられる。プログラミング言語は、一般にELIZA効果を排除するため、キーワードを慎重に選択し、誤解が発生しないようにする。

## 参考文献

  - Hofstadter, Douglas. *Preface 4: The Ineradicable Eliza Effect and Its Dangers.* (from *Fluid Concepts and Creative Analogies: Computer Models of the Fundamental Mechanisms of Thought*, Basic Books: New York, 1995)
  - Turkle, S. Eliza Effect: tendency to accept computer responses as more intelligent than they really are (from *Life on the screen- Identity in the Age of the Internet*, Phoenix Paperback: London, 1997)
  - [ELIZA effect](http://www.catb.org/~esr/jargon/html/E/ELIZA-effect.html)、[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")（version 4.4.7）より。[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[10月8日](../Page/10月8日.md "wikilink")参照。

## 関連項目

  - [AI完全](https://ja.wikipedia.org/wiki/AI完全 "wikilink")
  - [チューリング・テスト](../Page/チューリング・テスト.md "wikilink")
  - [ヒュー・ローブナー](https://ja.wikipedia.org/wiki/ヒュー・ローブナー "wikilink")
  - [記号学](../Page/記号学.md "wikilink")
  - [人工無脳](../Page/人工無脳.md "wikilink")

[Category:人工知能](https://ja.wikipedia.org/wiki/Category:人工知能 "wikilink") [Category:人間とコンピュータの相互作用](https://ja.wikipedia.org/wiki/Category:人間とコンピュータの相互作用 "wikilink") [Category:錯覚](https://ja.wikipedia.org/wiki/Category:錯覚 "wikilink")