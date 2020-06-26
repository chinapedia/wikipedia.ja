> この記事は[Fizz Buzz](https://ja.wikipedia.org/wiki/Fizz_Buzz)から翻訳されています。


**Fizz Buzz**（フィズ・バズ、**Bizz Buzz**や**Buzz**とも呼ばれる）は英語圏で長距離ドライブ中や[飲み会](https://ja.wikipedia.org/wiki/飲み会 "wikilink")の時に行われる言葉遊びである。

## 遊び方

プレイヤーは円状に座る。最初のプレイヤーは「1」と数字を発言する。次のプレイヤーは直前のプレイヤーの次の数字を発言していく。ただし、3で割り切れる場合は「**Fizz**」（Bizz Buzzの場合は「**Bizz**」）、5で割り切れる場合は「**Buzz**」、両者で割り切れる場合（すなわち15で割り切れる場合）は「**Fizz Buzz**」（Bizz Buzzの場合は「**Bizz Buzz**」）を数の代わりに発言しなければならない。発言を間違えた者や、ためらった者は脱落となる。

## ゲーム例

ゲームは、以下のとおりに発言が進行する。

  - 1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, Fizz Buzz, 16, 17, Fizz, 19, Buzz, Fizz, 22, 23, Fizz, Buzz, 26, Fizz, 28, 29, Fizz Buzz, 31, 32, Fizz, 34, Buzz, Fizz, ...

## FizzBuzz問題

このゲームをコンピュータ画面に表示させるプログラムとして作成させることで、コードが書けないプログラマ志願者を見分ける手法をJeff AtwoodがFizzBuzz問題 (FizzBuzz Question) として提唱した。その提唱はインターネットの様々な場所で議論の対象になっている。

また、実際に「制限時間2分以内」「[剰余](https://ja.wikipedia.org/wiki/除算 "wikilink")（%記号等）を用いない」「1行でできる限り短く（ワンライナー）」等の[縛りでゲーム条件を満たすコード記述の腕試しをする者が続出した](https://ja.wikipedia.org/wiki/やり込み#制限プレイor縛りプレイ "wikilink")。以下は[Python](../Page/Python.md "wikilink")による標準的な解答例である。なお、下記解答例の「i % 15 == 0」は「i % 3 == 0 and i % 5 == 0」と書いても良い。

``` python
for i in range(1, 101):
    if i % 15 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)
```

もう一つの標準的な解答例として、文字列の連結を利用することで、3の倍数かつ5の倍数（すなわち15の倍数）か否かの判定を無くしたものがある。

``` python
for i in range(1, 101):
    fb_str = ""
    if i % 3 == 0:
        fb_str += "Fizz"
    if i % 5 == 0:
        fb_str += "Buzz"
    if fb_str == "":
        fb_str += str(i)
    print(fb_str)
```

## 関連項目

  - [世界のナベアツ](../Page/桂三度.md "wikilink")

<!-- end list -->

  -
    「3の倍数と3のつく数のときだけアホになる」という、Fizz Buzzと同様の考えのギャグを行っている。

<!-- end list -->

  - [コサキンルーの怒んないで聞いて\!\!](../Page/コサキンルーの怒んないで聞いて!!.md "wikilink")

<!-- end list -->

  -
    「パチパチ7」というコーナーで、Fizz Buzzを応用したゲームを行った。こちらは7の倍数と7のつく数のときだけ手を叩くルールであった。

## 外部リンク

  - [Why Can't Programmers.. Program?](http://www.codinghorror.com/blog/archives/000781.html)
  - [HQ9F+](http://cfs.maxn.jp/neta/HQ9F+.html) (ジョーク向け[プログラミング言語](../Page/プログラミング言語.md "wikilink")である[HQ9+](../Page/HQ9+.md "wikilink")に、FizzBuzzを追加し拡張したもの)

[Category:言葉遊び](https://ja.wikipedia.org/wiki/Category:言葉遊び "wikilink") [Category:除法](https://ja.wikipedia.org/wiki/Category:除法 "wikilink") [Category:数学ゲーム](https://ja.wikipedia.org/wiki/Category:数学ゲーム "wikilink")