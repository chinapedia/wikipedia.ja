> この記事は[Tierra \(\)](https://ja.wikipedia.org/wiki/Tierra_\(\))から翻訳されています。


**Tierra**（ティエラ）とは、[生態学](../Page/生態学.md "wikilink")者の[トマス・S・レイ](https://ja.wikipedia.org/wiki/トマス・S・レイ "wikilink")が[1990年代](../Page/1990年代.md "wikilink")に開発した、[人工生命](../Page/人工生命.md "wikilink")[プログラムである](../Page/プログラム_\(コンピュータ\).md "wikilink")。

ティエラは、起動すると[コンピュータ](../Page/コンピュータ.md "wikilink")内に[仮想機械](../Page/仮想機械.md "wikilink")を作りだし、「スープ」あるいは「メインメモリ」と呼ばれる適当なサイズの[メモリを確保する](../Page/記憶装置.md "wikilink")。スープは仮想生物が暮らすための空間であり、ここに展開されたバイトコードは仮想生物の[遺伝子](https://ja.wikipedia.org/wiki/遺伝子 "wikilink")にあたる。仮想マシンは、遺伝子を[機械語](../Page/機械語.md "wikilink")として解釈し、実行する。

それぞれの仮想生物は、仮想[CPU](../Page/CPU.md "wikilink")の[レジスタと実行](../Page/レジスタ_\(コンピュータ\).md "wikilink")[ポインタを保持し](../Page/ポインタ_\(プログラミング\).md "wikilink")、仮想機械がこれを順に切り替えることで、[マルチプロセス的に仮想生物の遺伝子を解釈実行する](../Page/マルチタスク.md "wikilink")。スープに格納された遺伝子は、一定の割合でランダムなビットが反転し、また仮想CPUはある確率でミスをする。

以上のような条件のもとで、仮想生物はメモリとCPU時間を奪い合いながら、自分の複製を製造する。メモリは、仮想生物にとっての餌であり、CPU時間はエネルギーである、と喩えられることが多い。

ティエラは、命令語セットの取りかたにより、いくつかの種類が存在する。仮想生物がネットワークを介して、他のコンピュータと行き来できるバージョンも開発されている。また、ティエラを参考にして開発された、[Avida](../Page/Avida.md "wikilink")というプログラムも存在する。

一般的な[進化的コンピューター・プログラムでは](https://ja.wikipedia.org/wiki/進化的計算 "wikilink")、仮想生物の遺伝子を解釈して何らかの出力を得、ここから「[適応度](https://ja.wikipedia.org/wiki/適応度 "wikilink")」を数値として求めて仮想生物を淘汰する。しかしティエラでは、適応度を求める関数（[適応度関数](https://ja.wikipedia.org/wiki/適応度関数 "wikilink")）は用意されていない。ティエラの仮想生物がもつ遺伝子は自身を複製するための機械語であるが、これが不適切な場合は子孫を残せず死を待つのみとなる。

また、少ないCPU時間で複製を作ることのできる生物ほど、繁栄することになる。また、[遺伝的プログラミング](https://ja.wikipedia.org/wiki/遺伝的プログラミング "wikilink")など多くの生物的プログラムが[木構造の遺伝子を持つのに対し](../Page/木構造_\(データ構造\).md "wikilink")、ティエラの仮想生物は直線状の遺伝子を持つ。

以上のような設計のため、遺伝子の突然変異は多くの場合、不妊性の[畸形を生み](../Page/奇形.md "wikilink")、種として存続できないが、他の個体の遺伝子を利用して、自身の複製を作る「寄生種」などの存在を許容することになったのも、大きな特徴の一つである。

## 外部リンク

  - [Tierra home page](http://life.ou.edu/tierra/)
  - [Tierra 入門](http://web.archive.org/web/20001202002200/www.hip.atr.co.jp/~kim/TIERRA/tierra.html) ( Web Archive )

[Category:人工生命](https://ja.wikipedia.org/wiki/Category:人工生命 "wikilink") [Category:計算機科学](https://ja.wikipedia.org/wiki/Category:計算機科学 "wikilink")