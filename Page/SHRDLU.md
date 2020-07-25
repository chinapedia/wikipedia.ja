> この記事は[SHRDLU](https://ja.wikipedia.org/wiki/SHRDLU)から翻訳されています。


**SHRDLU**とは、[自然言語処理](../Page/自然言語処理.md "wikilink")を行う人工知能研究初期の研究開発プロジェクトである。[1968年](../Page/1968年.md "wikilink")から[1970年](../Page/1970年.md "wikilink")にかけて、[テリー・ウィノグラード](../Page/テリー・ウィノグラード.md "wikilink")によって実施された。自然言語により仮想世界の操作を行う事ができる。実装はソフトウエア面では[プログラミング言語](../Page/プログラミング言語.md "wikilink")[Lispと](https://ja.wikipedia.org/wiki/LISP "wikilink")[Planner](../Page/Planner.md "wikilink")を用いて記述され、ハードウエア面では[DEC社のコンピュータ](../Page/ディジタル・イクイップメント・コーポレーション.md "wikilink")・[PDP-6](../Page/PDP-6.md "wikilink")および同社のグラフィック[端末](../Page/端末.md "wikilink")上で動作した。後に[ユタ大学](../Page/ユタ大学.md "wikilink")の[コンピュータグラフィックス](../Page/コンピュータグラフィックス.md "wikilink")研究所によって改良され、SHRDLUの「世界」はフル3Dで描画されるようになった。

SHRDLUの名称は[etaoin shrdluに由来している](https://ja.wikipedia.org/wiki/etaoin_shrdlu "wikilink")。

## 機能

SHRDLUは英語による指示を受け付ける。ユーザはSHRDLUに指示を出し、端末の画面の中の小さな「積み木の世界」に存在する様々な物体――ブロック、円錐、球など――を動かさせることができる。

SHRDLUを特徴付けているのは、4つの単純な概念を組み合わせることで、「自然言語処理」の模倣により説得力を持たせている点である。第一に、SHRDLUの中の「世界」は極めて単純なので、すべての物体と所在の組み合わせについて記述することは、50種類ほど単語があれば可能である。単語には、「ブロック(block)」「円錐(cone)」といった名詞、「～の上に置け(place on)」「～まで動かせ(move to)」といった動詞、また「大きい(big)」「青い(blue)」といった形容詞がある。これらの基本的な語の可能な組み合わせはかなり単純であり、SHRDLUのプログラムはユーザの意図するところを理解するには十分なほど巧みに組まれている。

また、SHRDLUには、与えられた状況に対する基本的な記憶の能力が備わっている。ユーザはSHRDLUに対して、「緑色の円錐を赤いブロックの上に置け(put the green cone on the red block)」と指示した後、「その円錐を取り除け(take the cone off)」と指示することができる。この場合、「その円錐(the cone)」は、ユーザが先ほど言及した円錐のことを意味しているものと判断される。追加の形容詞が与えられた際、大抵の場合SHRDLUは履歴を検索し、適当な状況を探し出すことができる。ユーザは履歴について質問することが可能である。例えば「その円錐の前に何かを持ち上げたか？(did you pick up anything before the cone?)」という質問ができる。

この記憶の副次的効果として、またSHRDLUに備わっている根源的なルールとして、SHRDLUはその「世界」において何が可能で何が可能でないかという質問に答えることができる。例えばSHRDLUは、その「世界」の中での実例を発見することによって、ブロックは積み上げることができると推測する。しかし、三角形(triangles)は積み上げることができないということについては、実際にそれを試みることによってはじめて認知する。SHRDLUの中の「世界」には、ブロックは下に落ちるものであるという基本的な[物理法則](../Page/物理法則.md "wikilink")が働いており、これは[構文解析器](../Page/構文解析器.md "wikilink")とは独立している。

最後に、SHRDLUは、単一の物体あるいは複数の物体の組み合わせに対して付けられた名称を記憶することもできる。例えば、ユーザが「尖塔とは、背の高い四角形の上にある、小さな三角形のことである(a steeple is a small triangle on top of a tall rectangle)」と述べたとする。SHRDLUは、その「世界」の中での尖塔についての質問に答えたり、新たに尖塔を作ったりすることができる。

## 結果

結果として、SHRDLUは[AIの大いなる成功例となった](../Page/人工知能.md "wikilink")。これは他のAI研究家たちに過剰なオプティミズムをもたらした。しかし、これ以後開発されたシステムが、現実世界の曖昧さと複雑さを備えたより現実的な状況を取り扱おうとした際に、このオプティミズムはまもなく潰えた。 元のSHRDLUの流れにおいては、主に、それから結論を導くことのできるような情報をプログラムに提供することに焦点を当てた取り組みが継続され、Cycといった取り組みにつながっている。

## 参考文献

  - *Procedures as a Representation for Data in a Computer Program for Understanding Natural Language*. MIT AI Technical Report 235, February 1971

## 関連項目

  - [Planner](../Page/Planner.md "wikilink")

## 外部リンク

  - [SHRDLU](http://hci.stanford.edu/~winograd/shrdlu/) - テリー・ウィノグラードによるSHRDLUのページ。ソースコードあり（英語）
  - [Conversation with SHRDLU](http://www.ee.cooper.edu/courses/course_pages/past_courses/EE459/shrdlu/) - SHRDLUのデモンストレーション。解説あり（英語）
  - [SHRDLU resurrection](http://www.semaphorecorp.com/misc/shrdlu.html) - SHRDLUのリライトされた版。Java3D版もあり（英語）

[Category:人工知能](https://ja.wikipedia.org/wiki/Category:人工知能 "wikilink") [Category:自然言語処理](https://ja.wikipedia.org/wiki/Category:自然言語処理 "wikilink")