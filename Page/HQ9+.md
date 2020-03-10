> この記事は[HQ9+](https://ja.wikipedia.org/wiki/HQ9+)から翻訳されています。


**HQ9+**は[クリフ・ビッフル](https://ja.wikipedia.org/wiki/クリフ・ビッフル "wikilink")によって作られたジョーク向け[難解プログラミング言語](https://ja.wikipedia.org/wiki/難解プログラミング言語 "wikilink")である。実用言語ではない。

HQ9+は4つの[命令だけで構成されており](../Page/命令_\(コンピュータ\).md "wikilink")、それらは'H'、'Q'、'9'、'+'という単一の文字で示される。HQ9+は[チューリング完全](https://ja.wikipedia.org/wiki/チューリング完全 "wikilink")ではなく、[プログラミング言語](../Page/プログラミング言語.md "wikilink")としては不完全であるが、プログラミングの例題としてよく取り上げられるいくつかの問題に対しては極めて効率的である。

## 仕様

  - Hコマンドは文字列["Hello, world\!"を出力する](../Page/Hello_world.md "wikilink")。
  - Qコマンドはプログラムの[ソースコード](../Page/ソースコード.md "wikilink")を出力する（参考:[クワイン_(プログラミング)](../Page/クワイン_\(プログラミング\).md "wikilink")）。
  - 9コマンドは『*99 Bottles of Beer*』（アメリカの数え歌で、プログラミングの例題でよく利用される）の歌詞を出力する。
  - \+コマンドは[アキュムレータをインクリメント](https://ja.wikipedia.org/wiki/アキュムレータ_\(コンピュータ\) "wikilink")（1だけ増やす）する。

HQ9+のプログラムは、例えば次のようになる。

`HHQ+HQ++`

このプログラムは"Hello, world\! Hello, world\! HHQ+HQ++ Hello, world\! HHQ+HQ++"と表示し、アキュムレータを三回インクリメントする。

## 解説

HQ9+の命令体系は、プログラム初心者や新しいプログラミング言語を学習するプログラマによく利用される例題そのものである。例えば「文字列"Hello, world\!"を出力する」という例題は極めて一般的なものであるが、この種の処理を行うことが非常に難しいプログラミング言語も存在する。しかし、HQ9+にとっては極めて容易な問題であり、ただ単に"H"と命令するだけである（というよりも、問題の回答自体が言語仕様に入っている）。また、「自分自身のソースプログラムを出力する」という例題は多くのプログラミング言語にとって最も難しい課題の一つであるが、これもHQ9+にとっては取るに足らない問題である（これも問題を解いているわけではなく、言語仕様に回答が含まれているだけであるが）。

HQ9+の[インタプリタ](../Page/インタプリタ.md "wikilink")を作成することは極めて簡単であるため、多数のHQ9+の処理系が存在する。たとえば、あるインタプリタは[Python](../Page/Python.md "wikilink")によるものであり、作成時間は約5分、サイズはわずか18行である。またある、[C言語](../Page/C言語.md "wikilink")で記述された[コンパイラ](../Page/コンパイラ.md "wikilink")はHQ9+のプログラムをCのコードに変換するもので、サイズは約40行である。そしてこのインタプリタは[JavaScript](../Page/JavaScript.md "wikilink")で記述されており、ステップ実行ができる\[1\]。

HQ9+には入力機能がないため、HQ9+のインタプリタやコンパイラをHQ9+自身で記述することは不可能である。

また、**HQ9++**と呼ばれる言語も存在する。これは[デイビッド・モルガン＝マール](https://ja.wikipedia.org/wiki/デイビッド・モルガン＝マール "wikilink")によって作成された[オブジェクト指向](../Page/オブジェクト指向.md "wikilink")言語で、HQ9+とは下位互換性をもつ。HQ9++には'++'という新しい命令が追加されている。この命令はアキュムレータを2回インクリメントし、さらにオブジェクトのインスタンスを生成する。[情報隠蔽](https://ja.wikipedia.org/wiki/情報隠蔽 "wikilink")の原理に従い、このオブジェクトへのアクセスはできない様になっている。

さらに[FizzBuzz](https://ja.wikipedia.org/wiki/FizzBuzz "wikilink")を追加した**HQ9F+**なるものも存在する。

## 脚注

## 関連項目

  - [FizzBuzz](https://ja.wikipedia.org/wiki/FizzBuzz "wikilink")
  - [HQ9F+](https://ja.wikipedia.org/wiki/HQ9F+ "wikilink")
  - [HQ9++](https://ja.wikipedia.org/wiki/HQ9++ "wikilink")

## 外部リンク

  - [HQ9+（英語）](http://www.cliff.biffle.org/esoterica/hq9plus.html)
  - [HQ9++（英語）](http://www.dangermouse.net/esoteric/hq9plusplus.html)
  - [HQ9F+（日本語）](http://cfs.maxn.jp/neta/HQ9F+.html)
  - [オンライン HQ9+ インタプリタ（英語）](http://www.almnet.de/esolang/hq9plus.php)
  - [DM's Esoteric Programming Languages （英語）](http://www.dangermouse.net/esoteric/)

[Category:難解プログラミング言語](https://ja.wikipedia.org/wiki/Category:難解プログラミング言語 "wikilink")

1.  <http://cfs.maxn.jp/neta/onlineHQ9+.html>