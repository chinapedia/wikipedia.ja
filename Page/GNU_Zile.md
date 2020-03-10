> この記事は[GNU Zile](https://ja.wikipedia.org/wiki/GNU_Zile)から翻訳されています。


**Zile**は[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")で、[テキストエディタ](../Page/テキストエディタ.md "wikilink")を開発するための[C言語](../Page/C言語.md "wikilink")のツールキットである。Zileはまた、このツールキットを用いて構築された[Emacs](../Page/Emacs.md "wikilink")のクローンでもある。Zileは、*Zile is Lossy Emacs*を表している\[1\]。

Zileは、最初Sandro SigalaによってC言語で書かれ、今はReuben Thomasによってソースコードの維持が行われている。

Zileのゴールは、より少ないリソースで[GNU Emacsのように動作することである](../Page/GNU_Emacs.md "wikilink")。Zileは、その機能や変数の名前をEmacsと同様のものを用いているが、内部データの構造やAPIはより一般的な目的に適合するように発展させられたものとなっている。

## 歴史

Zileは、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")4月に、軽量なEmacsのクローンとしてスタートした\[2\]。[2014年](../Page/2014年.md "wikilink")には、テキストエディタ開発のためのソフトウェア開発フレームワークに進化している\[3\]。

かつてZileと呼ばれていた軽量なZileは、今はZemacsと呼ばれている。[再帰的頭字語](../Page/再帰的頭字語.md "wikilink")の伝統にならい、Zileは（前述のように）*Zile Is Lossy Emacs*を表していた。Zemacsは、[RAM](https://ja.wikipedia.org/wiki/RAM "wikilink")メモリのフットプリントによって区別され、これはおおよそ100kBである。Zileは、8ビットクリーンであり、これは[Unicode](../Page/Unicode.md "wikilink")のサポートを必要とせずにある種のファイルを利用することを可能にしている\[4\]。

Zemacsのキーボード・ショートカットはEmacsのものと同様であり、また、ZileはEmacsの標準的な機能を組み込んでいる。これには、以下の諸機能が含まれる。

  - マルチレベルのアンドゥを伴ったマルチバッファによる編集
  - マルチウィンドウ
  - コピーや貼り付け（キリングやヤンキング）
  - ミニバッファの補完
  - オートフィル

## LuaJITによる再実装

Zileはまた、[LuaJIT](https://ja.wikipedia.org/wiki/LuaJIT "wikilink")言語で再実装された\[5\]。この場合、Zileは*Zile Implements Lua Editors*も表している\[6\]。[2017年](../Page/2017年.md "wikilink")[3月20日](../Page/3月20日.md "wikilink")の時点で、LuaJITによるZileの実装への最後のコミットは[2011年](../Page/2011年.md "wikilink")[4月2日](../Page/4月2日.md "wikilink")のものである\[7\]\[8\]。

## 関連項目

  - [Emacs](../Page/Emacs.md "wikilink")

## 脚注

### 出典

[Category:テキストエディタ](https://ja.wikipedia.org/wiki/Category:テキストエディタ "wikilink")

1.  [Zile project page on GNU Savannah](http://savannah.gnu.org/projects/zile/)
2.  [Savannah](https://savannah.gnu.org/projects/zile)
3.
4.  GNU Project: [GNU Zile](https://www.gnu.org/software/zile/)
5.  [Github malkia / luajit-zile](https://github.com/malkia/luajit-zile)
6.  [Libre Planet](http://libreplanet.org/wiki/GNU_Zile)
7.  [Github malkia / luajit-zile](https://github.com/malkia/luajit-zile)
8.  [Github gvvaughan / luajit-zile](https://github.com/gvvaughan/luajit-zile)