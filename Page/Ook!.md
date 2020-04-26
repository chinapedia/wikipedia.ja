> この記事は[Ook!](https://ja.wikipedia.org/wiki/Ook!)から翻訳されています。


**Ook\!**（ウーク）は、[プログラミング言語](../Page/プログラミング言語.md "wikilink")の一つ。David Morgan-Marが[オランウータン](../Page/オランウータン.md "wikilink")向けのプログラミング言語として考案した。実用言語ではない[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")のひとつ。

オランウータンの鳴き声"Ook"のみを用いた言語である。使用する[トークン](../Page/トークン.md "wikilink")は「Ook.」「Ook\!」「Ook?」の3つだけで、これら2つの組み合わせで1命令を表現する。

Ook\!の仕様は[Brainfuck](../Page/Brainfuck.md "wikilink")と等価である。Ook\!で使用する命令はBrainfuckの命令と正確に対応するので、Ook\!は実のところBrainfuckの文字の置き換えに過ぎない。

## 言語仕様

十分な長さのメモリと、それを指す1つのポインタがあることなどはBrainfuckと同じである。Ook\!命令とBrainfuck命令の対応は以下の通り。

| Ook\!       | Brainfuck | 内容                                                   |
| ----------- | --------- | ---------------------------------------------------- |
| `Ook. Ook?` | `>`       | ポインタをインクリメント                                         |
| `Ook? Ook.` | `<`       | ポインタをデクリメント                                          |
| `Ook. Ook.` | `+`       | ポインタの指す値をインクリメント                                     |
| `Ook! Ook!` | `-`       | ポインタの指す値をデクリメント                                      |
| `Ook. Ook!` | `,`       | 入力から1バイトをポインタの指す値に代入                                 |
| `Ook! Ook.` | `.`       | ポインタの指す値を[ASCII](../Page/ASCII.md "wikilink")文字として出力 |
| `Ook! Ook?` | `[`       | ポインタの指す値が0なら、対応する「Ook? Ook\!」にジャンプ                   |
| `Ook? Ook!` | `]`       | ポインタの指す値が非0なら、対応する「Ook\! Ook?」にジャンプ                  |

「`Ook? Ook?`」の動作は定義されていない。プログラムのトークン数が奇数の場合は構文エラーとなる。

## 処理系

  - RubyOok\[1\]

## 参考文献

  - 水野貴明「開発環境探訪 第12回 非常に難解でシンプルなプログラム言語――BrainF\*ck」『Interface』第28巻第9号、CQ出版、2002年9月、139-143ページ。※筆者の水野は記事中Ook\!に言及した部分に修正を加えたものを公開していた[1](https://web.archive.org/web/20040704185114/http://www.takaaki.info/programming/esoteric/ook.html)。

## 脚注

<references/>

## リンク

  - [DM's Esoteric Programming Languages - Ook\!](http://www.dangermouse.net/esoteric/ook.html) - Ook\!の仕様

[Category:難解プログラミング言語](https://ja.wikipedia.org/wiki/Category:難解プログラミング言語 "wikilink")

1.  Chad Fowler, [RubyOok](https://web.archive.org/web/20041023011903/http://chadfowler.com/ruby/rubyook/)