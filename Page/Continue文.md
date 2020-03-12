> この記事は[Continue](https://ja.wikipedia.org/wiki/Continue)から翻訳されています。


**continue文**は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")の[ループで用いられる](../Page/ループ_\(プログラミング\).md "wikilink")[文である](https://ja.wikipedia.org/wiki/文_\(プログラミング\) "wikilink")。

## 文法

### Cおよびそれに類する言語の場合

[C言語](../Page/C言語.md "wikilink")、[C++](../Page/C++.md "wikilink")、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")、[JavaScript](../Page/JavaScript.md "wikilink")などでは、[for文](https://ja.wikipedia.org/wiki/for文 "wikilink")、[while文](https://ja.wikipedia.org/wiki/while文 "wikilink")、[do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")の中で使うことができる。[Perl](../Page/Perl.md "wikilink")では[キーワードが少し異なっており](../Page/予約語.md "wikilink")、continueに相当するのはnextで、continueは違う機能のためのものである\[1\]。

continue文は、ループの内部（「ループ本体」の中）にのみ現れることができ、実行されると「それを囲む最も内側の繰返し文のループ継続部，すなわちループ本体の終わりへの分岐を引き起こす。」（JIS X 3010-1993、§6.6.6.2）。

[do-while文](https://ja.wikipedia.org/wiki/do-while文 "wikilink")以外では、その分岐（ジャンプ）先のループ本体の終わりから、そのままループによって先頭に飛び、繰返しのための処理などが行われることになる。do-while文の場合は、ループ本体の終わりにすぐ繰返しの条件判定があるので、ただちに繰返しの条件判定となる。

以上のように、規格票をきちんと読めば、すっきりとした意味があることがわかる。

しかしこれを、おそらくは規格票を読まずに書かれた入門書などによって不自然に理解してしまうと「continue文はその文の実行を打ち切って、そのループの条件式の評価へと制御を移すためのもの」「for文の場合は例外であり、continue文が実行されると条件式の評価の前に、**更新式**が実行される」「前置判定のwhile文」「**後置判定**の場合も、同じように動作する。後置判定の場合は、他の方式のループの場合とは異なり、条件式が最後尾に書かれている。しかし冒頭で説明した通り、あくまで条件式の評価へと制御が移る。従って、先頭に戻すのではなく、後の処理を飛ばしてwhile文の**最後尾へ制御を移す**こととなるため、注意が必要である。」などと、よくわからない説明を重ねる結果になる。

## 例

C言語 ([C99](../Page/C99.md "wikilink")) による例を示す。制御の流れを視覚化するため、for文の条件式および更新式の中で[コンマ演算子](https://ja.wikipedia.org/wiki/コンマ演算子 "wikilink")を使って[printf](https://ja.wikipedia.org/wiki/printf "wikilink")関数の評価結果を無視している。

``` c
for (int i = 0; printf("condition[%d]\n", i), i < 5; printf("update[%d]\n", i), ++i) {
  if (i % 2 == 0) {
    printf("%d is even.\n", i);
    continue; // ループ本体中の以降の処理は実行されない。
  }
  printf("%d is odd.\n", i);
}
```

結果:

``` text
condition[0]
0 is even.
update[0]
condition[1]
1 is odd.
update[1]
condition[2]
2 is even.
update[2]
condition[3]
3 is odd.
update[3]
condition[4]
4 is even.
update[4]
condition[5]
```

## 脚注

## 関連項目

  - [for文](https://ja.wikipedia.org/wiki/for文 "wikilink")
  - [while文](https://ja.wikipedia.org/wiki/while文 "wikilink")

[Category:制御構造](https://ja.wikipedia.org/wiki/Category:制御構造 "wikilink")

1.  Perlでは、continueに[ブロックが引き続いている場合](../Page/ブロック_\(プログラミング\).md "wikilink")「条件文が再評価される直前に常に実行される」コードとなり、すなわち「C における for ループの 3 番目の部分と同様」な働きとなる。"<http://perldoc.jp/func/continue>"