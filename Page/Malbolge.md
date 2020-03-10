> この記事は[Malbolge](https://ja.wikipedia.org/wiki/Malbolge)から翻訳されています。


**Malbolge**は1998年にBen Olmsteadによって開発された、[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")の[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")である。名前は、[ダンテの](../Page/ダンテ・アリギエーリ.md "wikilink")[神曲](../Page/神曲.md "wikilink")地獄篇における地獄の第8圏であるMalebolgeにちなんで名付けられた。

Malbolgeは[チューリング完全](https://ja.wikipedia.org/wiki/チューリング完全 "wikilink")である\[1\]\[2\]が、実用言語ではない。Malbolgeの異常な点は、最悪の、すなわち最も扱いにくく難解であるプログラミング言語となるべく設計されたことである。Malbolgeは[INTERCAL](https://ja.wikipedia.org/wiki/INTERCAL "wikilink")、[機械語](../Page/機械語.md "wikilink")、[Brainfuck](../Page/Brainfuck.md "wikilink")の最悪な部分を組み合わせたものであるという\[3\]。しかし、理解を困難にするために用いたトリックのいくつかはごく単純化することができる。

## Malbolgeでのプログラミング

プログラミング言語Malbolgeが世に出たとき、理解することが非常に難しく、最初に書かれたプログラムが出現するのに2年を要した。しかもそのプログラムは人間によって書かれたものではなく、Andrew Cookeが設計し[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")で実装した[ビーム探索アルゴリズムにより生成したものだった](https://ja.wikipedia.org/wiki/ビーム探索法 "wikilink")。

2000年8月24日、Anthony Youhasは彼のブログでMalbolgeを打ちのめし解決の鍵を極めたと宣言し、様々な語句を表示する3つのMalbolgeプログラムコードによりその証拠とした\[4\]。しかし、どのような技法を用いたかは明らかにはしなかった。

後にLou Schefferは、Malbolgeはプログラミング言語というより[暗号](../Page/暗号.md "wikilink")システムとして見るべきであり、暗号システムとして見た場合のMalbolgeにはいくつかの[脆弱性](https://ja.wikipedia.org/wiki/脆弱性 "wikilink")があると指摘した\[5\]。また、これらの脆弱性を突くことでMalbolgeプログラムを書くことができるとし、例として入力された文字を出力するプログラムを示した。

OlmsteadはMalbolgeが[線形拘束オートマトン](https://ja.wikipedia.org/wiki/線形拘束オートマトン "wikilink")であると考えていた。

Malbolgeの[プログラム難読化への応用可能性に着目した](https://ja.wikipedia.org/wiki/難読化コード "wikilink")[名古屋大学](../Page/名古屋大学.md "wikilink")の[酒井正彦](https://ja.wikipedia.org/wiki/酒井正彦 "wikilink")らにより、3段階の中間言語や[SATソルバを用いてMalbolgeプログラムを生成する手法が提案されている](https://ja.wikipedia.org/wiki/充足可能性問題 "wikilink")\[6\]\[7\]。これらの研究成果を用いて、[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")や[配列](../Page/配列.md "wikilink")、[再帰](../Page/再帰.md "wikilink")関数などを含む[C言語](../Page/C言語.md "wikilink")のサブセットをMalbolgeプログラムに[コンパイルすることが可能となっている](../Page/コンパイラ.md "wikilink")\[8\]。

## Malbolgeで書いたHello, worldプログラム

次のMalbolgeプログラムは"[Hello, world](https://ja.wikipedia.org/wiki/Hello,_world "wikilink")"を出力する。

    <nowiki>
    (=<`:9876Z4321UT.-Q+*)M'&%$H"!~}|Bzy?=|{z]KwZY44Eq0/{mlk**
    hKs_dG5[m_BA{?-Y;;Vb'rR5431M}/.zHGwEDCBA@98\6543W10/.R,+O<
    </nowiki>

## 脚注

<references />

[Category:難解プログラミング言語](https://ja.wikipedia.org/wiki/Category:難解プログラミング言語 "wikilink")

1.  正確には、Malbolgeは言語仕様によりメモリが有限に制限されているため弱チューリング完全である。
2.
3.
4.
5.  [1](http://www.lscheffer.com/malbolge.shtml)
6.
7.
8.