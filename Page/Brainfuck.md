> この記事は[Brainfuck](https://ja.wikipedia.org/wiki/Brainfuck)から翻訳されています。


**Brainfuck**（ブレインファック）は[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")のひとつ。なお名称に[卑語](../Page/卑語.md "wikilink")が含まれるため、**Brainf\*ck**などと表記されることがある。

## 概要

開発者Urban Müllerが[コンパイラ](../Page/コンパイラ.md "wikilink")がなるべく小さくなる言語として考案した。 実際、Müllerが開発したコンパイラのサイズはわずか123[バイト](../Page/バイト_\(情報\).md "wikilink")、[インタプリタ](../Page/インタプリタ.md "wikilink")は98バイトであった。

Brainfuckプログラムは非常に可読性・記述性が低いため実用性は期待できないが、[チューリング完全](../Page/チューリング完全.md "wikilink")である。その簡潔さから多くの派生言語を生み出すこととなった。

## Brainfuckの言語仕様

処理系は次の要素から成る: Brainfuckプログラム、インストラクションポインタ（プログラム中のある文字を指す）、少なくとも30000個の要素を持つバイトの[配列](../Page/配列.md "wikilink")（各要素はゼロで初期化される）、データポインタ（前述の配列のどれかの要素を指す。最も左の要素を指すよう初期化される）、入力と出力の2つのバイトストリーム。

Brainfuckプログラムは、以下の8個の実行可能な命令から成る（他の文字は無視され、読み飛ばされる）。

1.  `>` [ポインタを](../Page/ポインタ_\(プログラミング\).md "wikilink")[インクリメント](../Page/インクリメント.md "wikilink")する。ポインタをptrとすると、[C言語](../Page/C言語.md "wikilink")の「`ptr++;`」に相当する。
2.  `<` ポインタをデクリメントする。C言語の「`ptr--;`」に相当。
3.  `+` ポインタが指す値をインクリメントする。C言語の「`(*ptr)++;`」に相当。
4.  `-` ポインタが指す値をデクリメントする。C言語の「`(*ptr)--;`」に相当。
5.  `.` ポインタが指す値を出力に書き出す。C言語の「`putchar(*ptr);`」に相当。
6.  `,` 入力から1バイト読み込んで、ポインタが指す先に代入する。C言語の「`*ptr=getchar();`」に相当。
7.  `[` ポインタが指す値が0なら、対応する `]` の直後にジャンプする。C言語の「`while(*ptr){`」に相当。
8.  `]` ポインタが指す値が0でないなら、対応する `[` （の直後）にジャンプする。C言語の「`}`」に相当。

## 派生言語

以上の8つの命令文字は可読性のために選ばれたものであり、これらが使われなければならない理由はなく、より難解にすることを目指したり、あるいは単なる遊びとして、各命令に使用する文字を置き換えた派生言語が考えられている。以下はその代表例である。

  - A\[1\] - 「`A`」だけで記述する。文字を置き換え、難読性を深めた例。
  - BrainCrash\[2\] - 4つの命令「`|&~^`」を加えたもの。終了時にポインタの指す値が0になるまでポインタを進め値を出力する。また、実行前に"Hello, world\!"が格納される。原型をさらに発展させた例。
  - [Ook\!](../Page/Ook!.md "wikilink") - 「`Ook.`」「`Ook!`」「`Ook?`」のうち2つの[トークンから成る文字列をBrainfuckの各命令に当てはめたもの](https://ja.wikipedia.org/wiki/字句 "wikilink")。使用される記号（実際には文字列だが）の種類がわずか3つと、本家より少ない。元の8種類の文字を置き換え、よりユーモアを加えた例。

## 脚注

### 注釈

### 出典

## 関連項目

  - [難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")

## 外部リンク

  - <http://www.muppetlabs.com/~breadbox/bf/> 解説ページ（英語）
  - [Index of /brainfuck](http://esoteric.sange.fi/brainfuck/) 処理系のアーカイブ
  - [Brainfuck Golf](http://brainfuck.sourceforge.net) お題に沿ってなるべく短いBrainfuckソースコードを書くコンテスト
  - <http://home.arcor.de/partusch/html_en/bfd.html> Brainfuck Compiler ([Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")/[MS-DOS](../Page/MS-DOS.md "wikilink"))
  - <http://brainfuck.progopedia.org/> Kit's JavaScript Brainfuck Interpreter
  - <http://cfs.maxn.jp/neta/onlineBrainFuck.html> ONLINE BrainF\*ck interpreter for JavaScript(STEP実行ができる)
  - <http://lab.moyo.biz/garage/brainfuck/index.xsp>  BrainFuck ダイナマイツ（メモリ表示付きインタープリタアプレット）
  - <http://d.hatena.ne.jp/yoshidaa/20130514/1368540057>  Ruby による Brainf\*ck の実装例 (動作過程を表示)

[Category:難解プログラミング言語](https://ja.wikipedia.org/wiki/Category:難解プログラミング言語 "wikilink")

1.
2.