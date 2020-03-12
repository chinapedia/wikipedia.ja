> この記事は[KEMURI \(\)](https://ja.wikipedia.org/wiki/KEMURI_\(\))から翻訳されています。


**KEMURI**（ケムリ）は、[Brainfuck](../Page/Brainfuck.md "wikilink")に類した[プログラミング言語](../Page/プログラミング言語.md "wikilink")の一つ。実用言語ではない。

[BrainCrash](https://ja.wikipedia.org/wiki/BrainCrash "wikilink")、[HQ9+](../Page/HQ9+.md "wikilink")についで世界で3番目に短く[Hello worldを出力するプログラムを記述できる](../Page/Hello_world.md "wikilink")。

KEMURIは[スタックマシン](../Page/スタックマシン.md "wikilink")であり、0～255の値が入るスタックがある。

実用性はほとんど無いように思われるが、KEMURI_PLUSでは[チューリングマシン](../Page/チューリングマシン.md "wikilink")で実行可能なあらゆるプログラムが記述できる（[チューリング完全](../Page/チューリング完全.md "wikilink")である）とされている。

## KEMURIの言語仕様

実行可能な命令は「6つ」のみである。

1.  `^` XOR スタックの先頭2つをpopし、xorを計算してpushする。
2.  `~` NOT スタックの先頭をpopし、notを計算してpushする。(必要性が疑問視されている)
3.  `"` DUP スタックの先頭をpopし、それを2回pushする。スタック先頭の複製(duplicate)である。
4.  `'` ROT スタックの先頭3つをpopし、並び替えてpushする。先頭から順にx y zという順に並んでいたのなら、y z xという順番に変わる。
5.  `` ` `` スタックに\[72, 101, 108, 108, 111, 44, 32, 119, 111, 114, 108, 100, 33\]を積む。これは[ASCIIコード](https://ja.wikipedia.org/wiki/ASCIIコード "wikilink")とみなすと"Hello, world\!"に相当する。
6.  `|` スタックの中身を文字コードだと見なして出力する。スタックの中身すべてを出力するのでスタックは空になる。プログラムの最後で一度だけ使うことが推奨されている。

## KEMURI_PLUSの拡張仕様

1.  `l` (小文字のエル) スタックの中身を[Brainfuck](../Page/Brainfuck.md "wikilink")のコードだと見なして実行する。プログラムの最後で一度だけ使うことが推奨されている。

## 外部リンク

  - <http://d.hatena.ne.jp/earth2001y/20060925/p1> KEMURIの最適化コンパイラ
  - <http://www.phys.cs.is.nagoya-u.ac.jp/~watanabe/sample/kemuri.html> JavaScriptによる実装(ブラウザ上で動きます)
  - [KEMURIで任意の文字列を表示するプログラムを生成するプログラム](http://d.hatena.ne.jp/Unkun/20070303)
  - [解説ページ（日本語、KEMURIインタプリタ）](http://www.nishiohirokazu.org/blog/2006/09/kemuri.html)
  - [解説ページ](http://d.hatena.ne.jp/keyword/KEMURI?kid=185319)

[Category:難解プログラミング言語](https://ja.wikipedia.org/wiki/Category:難解プログラミング言語 "wikilink") [Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink")