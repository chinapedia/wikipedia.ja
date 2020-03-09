> この記事は[Tiny BASIC](https://ja.wikipedia.org/wiki/Tiny_BASIC)から翻訳されています。


**Tiny BASIC**（タイニーベーシック）とは、[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")ないし初期の[8ビットパソコン](https://ja.wikipedia.org/wiki/8ビットパソコン "wikilink")・[ホビーパソコン](https://ja.wikipedia.org/wiki/ホビーパソコン "wikilink")用に仕様を簡略化（サブセット化）した[BASIC](../Page/BASIC.md "wikilink")の、言語仕様や、その実装（処理系）の総称。プログラムサイズがコンパクトなため、ごく小規模（tiny）なシステムでも使用できた。可能なこともやはり限られて（tiny）いたが、[機械語](../Page/機械語.md "wikilink")を使うよりははるかに手軽であり便利なものであった。

## 概要

Palo Alto Tiny BASIC他、いくつかの有名な実装がある。著名になったものは、ソースコードやそのバイナリコードのダンプリストを書籍や雑誌に掲載する形で公開したものが多い。1970年代後半、初期のマイコンのメモリ容量が数Kバイト程度しかない中で、フットプリントが2Kバイト前後のサイズで処理系が実装でき、また、他にそれらしい[プログラミング言語](../Page/プログラミング言語.md "wikilink")・言語処理系が無かったことから、マイコンユーザの間で流行した。後に[ROM-BASIC](https://ja.wikipedia.org/wiki/ROM-BASIC "wikilink")を内蔵するパーソナルコンピュータが発売されるようになってからは、アプリケーションを使うことが目的のユーザはそちらを使うようになったが、その後もTiny BASICを名乗る似たような機能のBASICは存在する。

細かい差異はあるが、概ね以下のような仕様であった。

  - 単純変数はA～Zの26個のみ。
  - 配列は@のみ。
  - データ型は2バイト整数のみ。
  - グラフィックやスクリーンエディットの機能はない。

Palo Alto Tiny BASICのように、同じ作者が[スタートレック (マイコンゲーム)](https://ja.wikipedia.org/wiki/スタートレック_\(マイコンゲーム\) "wikilink") のごく基本的な部分だけを遊べるようにした「Tiny Trek」を作成していることなどから、そのための工夫と思われるものが見られることもある。

当時の日本のTiny BASICとしては、東大版・東京版と呼ばれる移植版やオリジナルの電大版が書籍等でソースやダンプリストが公開されており 有名である。

  - 東大版 ([Intel i8080用](../Page/Intel_8080.md "wikilink")) Palo Alto Tiny BASICベース、移植者小野、[石田晴久](https://ja.wikipedia.org/wiki/石田晴久 "wikilink")著 [共立出版](https://ja.wikipedia.org/wiki/共立出版 "wikilink")刊『マイクロコンピュータのプログラミング』
  - 東京版 ([Intel i8085用](https://ja.wikipedia.org/wiki/Intel_8085 "wikilink")) Texas Tiny BASICベース、製作者石田・小野、石田晴久著 [近代科学社](https://ja.wikipedia.org/wiki/近代科学社 "wikilink")刊『マイクロコンピュータプログラミング入門』
  - 電大版 ([Motorola MC6800用](../Page/MC6800.md "wikilink")) 開発者畑中・著者安田、[安田寿明](https://ja.wikipedia.org/wiki/安田寿明 "wikilink")著 [講談社](../Page/講談社.md "wikilink")[ブルーバックス](https://ja.wikipedia.org/wiki/ブルーバックス "wikilink")『マイ・コンピュータをつかう』

## 歴史

Tiny BASIC登場以前のBASICの歴史は、[ダートマスBASIC](https://ja.wikipedia.org/wiki/ダートマスBASIC "wikilink")の記事などを参照のこと。

[集積回路](../Page/集積回路.md "wikilink")の発展と市場の需要などから、1970年代に[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")が次々と登場したことにより、一般の個人が、個人で[コンピュータ](../Page/コンピュータ.md "wikilink")を所有・占有し、趣味や実用に使うことが可能となった。それまでの[メインフレーム](../Page/メインフレーム.md "wikilink")や[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")が限られた人のものであったのに対し、これからはコンピュータの力を誰もが活用できるということで、革命という言葉すら使われた（[:en:Microcomputer revolution](https://ja.wikipedia.org/wiki/:en:Microcomputer_revolution "wikilink")）。

自然な流れとして\[1\]、初めのうちは[マイクロコンピュータ](../Page/マイクロコンピュータ.md "wikilink")の活用には[機械語](../Page/機械語.md "wikilink")が使われていたが、すぐに[プログラミング言語](../Page/プログラミング言語.md "wikilink")が欲されるようになった。そこで、当時既にミニコンピュータなどで活用されていた言語のいくつかに目が付けられ、当時のマイクロコンピュータで可能な程度に機能などを絞って実装することなどが行われた。そんな中で、数多く発足した有志団体のひとつ、People's Computer Company（[:en:People's Computer Company](https://ja.wikipedia.org/wiki/:en:People's_Computer_Company "wikilink")）の機関紙の Vol. 3, No. 4（1975年3月）\[2\]の 6, 7 ページに掲載された *BUILD YOUR OWN BASIC* という記事において、最低限に機能・仕様を絞ったBASICを自作することが提案され、それに刺激を受けた人々により、色々な実装が作られた。前述の機関紙の発展版にあたる[Dr. Dobb's Journalに掲載されたものなどは有名になった](https://ja.wikipedia.org/wiki/Dr._Dobb's_Journal "wikilink")。

## 注

<references/>

## 参考文献

  - bit臨時増刊『マイクロコンピュータのプログラミング』（1978年2月号増刊）, pp. 83-111, 「Tiny BASICインタプリタ」, Palo Alto Tiny BASIC の逆アセンブルリストを示し解説

## 関連項目

  - [スタンドアロンBASIC](https://ja.wikipedia.org/wiki/スタンドアロンBASIC "wikilink")

[Category:BASICインタプリタ](https://ja.wikipedia.org/wiki/Category:BASICインタプリタ "wikilink")

1.  通史的に見れば、コンピュータ自体が登場した後にも、[ミニコンピュータ](https://ja.wikipedia.org/wiki/ミニコンピュータ "wikilink")が登場した後にも、似たような流れがあり、ここで3度目となる。
2.  <https://purl.stanford.edu/jz908ss3011>