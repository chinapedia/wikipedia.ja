> この記事は[Emacs Lisp](https://ja.wikipedia.org/wiki/Emacs_Lisp)から翻訳されています。


**Emacs Lisp**は、[GNU Emacsと](../Page/GNU_Emacs.md "wikilink")[XEmacs](https://ja.wikipedia.org/wiki/XEmacs "wikilink")[テキストエディタ](../Page/テキストエディタ.md "wikilink")（この記事ではあわせて[Emacs](../Page/Emacs.md "wikilink")と呼ぶ）で使われている[Lispプログラミング言語の](https://ja.wikipedia.org/wiki/LISP "wikilink")[方言である](../Page/方言_\(プログラミング言語\).md "wikilink")。Emacs組込みの編集機能のうち、[C言語](../Page/C言語.md "wikilink")で書かれた部分以外のほとんどを実装するのに使われている。また、利用者によるEmacsのカスタム化や拡張のために用いられる。Lisp処理系で、もっとも使われている言語である。

Emacs Lispは、[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")の[Bourne Shell](../Page/Bourne_Shell.md "wikilink")、[Python](../Page/Python.md "wikilink")、[Perl](../Page/Perl.md "wikilink")、[scsh](https://ja.wikipedia.org/wiki/Scheme_Shell "wikilink")、[GNU Guile](https://ja.wikipedia.org/wiki/GNU_Guile "wikilink") などのようなスクリプト言語として使うこともでき、コマンド行や実行ファイルからも呼び出せる。[バッファ](../Page/バッファ.md "wikilink")や移動コマンドのような編集機能は、Lispの機能を補い[バッチ・モードで動作する](../Page/バッチ処理.md "wikilink")。

Emacs Lispは、ときに*Elisp*と呼ばれることもある。ただし、この呼び方は同名の無関係な古いLisp方言と混同されるおそれがある。機能でいうと、Common Lispの影響も後にみえるが、[Maclisp](../Page/Maclisp.md "wikilink")方言と強い関係がある \[1\]。プログラミング・メソッドとして、[手続き指向プログラミングと](https://ja.wikipedia.org/wiki/プロシージャ "wikilink")[関数的プログラミングに対応している](../Page/関数型言語.md "wikilink")。[関数をデータとして扱えるなどの強力な機能のため](https://ja.wikipedia.org/wiki/関数_\(プログラミング\) "wikilink")、([TECO](https://ja.wikipedia.org/wiki/TECO "wikilink")を拡張言語としていたオリジナルの) Emacsの書換えにあたり、[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")は拡張言語としてLispを選んだ。ストールマンが[Gosling EmacsをGNU](../Page/Gosling_Emacs.md "wikilink") Emacsへ書き換えていたとき、Common Lisp とは違ってSchemeは既に存在した。しかし、当時のワークステーションの性能は貧弱であったため、Schemeよりももっと簡単に最適化のできるLisp方言を開発する必要があった\[2\]。

Emacs Lispは、アプリケーション・プログラミングで使われる方言群である[Scheme](../Page/Scheme.md "wikilink")や[Common Lispとは根本的に異なる](../Page/Common_Lisp.md "wikilink")。大きな違いの1つは、デフォルトで[字句的スコープではなく](../Page/静的スコープ.md "wikilink")[動的スコープ](../Page/動的スコープ.md "wikilink")を使うことである。つまり、呼出し関数の局所変数は、呼び出された関数からも参照できるが、定義時のスコープで参照しているのではない。

Emacs Lispを書くのがGNU Emacsをカスタム化する唯一の方法ではない。バージョン20以降のGNU Emacsには「カスタム化」機能があり、利用者はグラフィカルなインターフェースによって一般的なカスタム化変数を設定できる。「カスタム化」機能は、比較的単純なものに制限されているものの、利用者の代わりにEmacs Lispのコードを書いてくれる。利用者全員がEmacsの提供する高度な拡張性が必要なわけではないし、またそういう人は自分でEmacs Lispのコードを書けるものだ。

## 例

Emacs Lispで書いたEmacsの簡単な拡張例をあげよう。Emacsでは、編集領域は、別々の*バッファ*を表示する*ウインドウ*という領域に分かれる。おおざっぱにいえば、バッファとは (大抵はファイルから) Emacsの[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")に読み込んだテキストのかたまりで、[テキストファイル](../Page/テキストファイル.md "wikilink")として保存できる。

新しいウインドウを開くユーザコマンドは、「`C-x 2`」である。これは、「`Control`」キーを押下した状態で「`x`」キーを押し、その後単独で「`2`」キーを押す、ということだ（空白文字は読み易いように示してあるだけで、打ってはいけない）。このキー列はEmacs Lispの`split-window-vertically`関数を動かし、普通は新しいウインドウに前のものと同じバッファが表示される。ここでは、その次に有効なバッファを表示するようにしたい、ということにしてみよう。そのためには、利用者は、次のEmacs Lispコードを、既存のEmacs Lispソース・コードや空のEmacsバッファに書く。

``` elisp
 (defun my-split-window-function ()
   (interactive)
   (split-window-vertically)
   (set-window-buffer (next-window) (other-buffer)))

 (global-set-key "\C-x2" 'my-split-window-function)
```

最初の文 `(defun ...)`は、新しい関数`my-split-window-function`を定義する。これは、`split-window-vertically` (前のウインドウ分割関数) を呼び出し、新しいウインドウが別のバッファを表示するようにする。次の文 `(global-set-key ...)` は、「`C-x 2`」というキー列に新しい関数を結び付けなおす。

もっと簡単に書く方法もある。Emacs Lispには、*advice*という強力な機能があり、利用者は既存の関数を再定義せずに新しいラッパーを作れるのである。adviceを使うと、上のコードは、次のように再実装できる。

``` elisp
 (defadvice split-window-vertically
   (after my-window-splitting-advice first () activate)
   (set-window-buffer (next-window) (other-buffer)))
```

これは、`split-window-vertically`が呼び出されたとき、関数の本体を実行する前に利用者の指定したコードを実行するよう命令している。

こういった変更は、たとえば「`M-x eval-buffer`」コマンドを使ってコードが*評価*されてはじめて効果が生ずる。Emacsの再コンパイルはおろか再起動さえいらない。Emacsのカスタム化は便利だといわれる所以である。もしEmacsの「立上げファイル」(ふつうは利用者の [ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink") にある「`.emacs`」という名前のファイル) にコードを保存すれば、次にEmacsが立ち上がったとき、Emacsはこの拡張を読み込むことになる。

## ソースコード

Emacs Lispのコードは、「`.el`」という拡張子のファイルに、[テキストファイル](../Page/テキストファイル.md "wikilink")として格納される（ただし、利用者の初期設定ファイル名は、Emacs21以前では例外として「`.emacs`」である）。ファイルが読み込まれると、Emacsプログラムの[インタープリタ](https://ja.wikipedia.org/wiki/インタープリタ "wikilink")部分が、関数や変数を読んだり解析したりして、メモリに格納する。そうして、他の編集関数や利用者コマンドで使えるようになる。関数や変数は、自由に修正したり、読み込みなおしたりできる。

メモリ空間の節約のため、Emacsの機能の多くは、必要になるまで読込まれない。追加機能一式それぞれは、「ライブラリ」というEmacsコードの集まりで実装されている。たとえば、プログラムソースコードのキーワードの強調用ライブラリや[テトリス](../Page/テトリス.md "wikilink")・ゲームで遊ぶライブラリなどがある。各ライブラリは、ひとつまたは複数のEmacs Lispソース・ファイルで実装される。

一部の関数は [C言語](../Page/C言語.md "wikilink")（以下、単にC）で書いてある。これは「プリミティブ」と呼ばれる（「組込み関数」とか「サブル」ともいう）。プリミティブはLispコードから呼び出すことができ、Cのソース・ファイルを修正し再コンパイルすることでのみ変更できる。GNU Emacsでは、プリミティブを外部ライブラリにすることはできず、Emacs[実行形式の一部分となる](../Page/実行ファイル.md "wikilink")。XEmacsでは、オペレーティング・システムの動的リンクのサポートを使って、プリミティブを実行時に読み込める。関数をプリミティブで書くのは、Emacs Lispからはアクセスできない外部データやライブラリを用いる必要があったり、CとEmacs Lispで実行速度の差が十分認められるほど頻繁に呼ばれたりする場合である。

ただし、Cでのエラーはすぐに[セグメンテーション違反](../Page/セグメンテーション違反.md "wikilink")やより些細なバグにつながるため、エディタをクラッシュさせるし、Emacs Lispの[ガベージ・コレクタと正しく相互作用するCのコードを書くことはエラーを引き起こしやすいので](../Page/ガベージコレクション.md "wikilink")、 プリミティブで実装されている関数は比較的少数である。

### バイトコード

Emacs Lispコードの性能は、「バイト・コンパイル」で向上させることができる。Emacs Lispのソース・ファイルを[バイトコード](../Page/バイトコード.md "wikilink")という特殊表現に変換する[コンパイラ](../Page/コンパイラ.md "wikilink")がEmacsにはある。Emacs Lispのバイトコード・ファイルの拡張子は、「`.elc`」である。ソース・ファイルにくらべると、バイトコードは速く読み込めて、ディスク空間を少ししかとらず、読込み時のメモリーが少なく、速くうごく。

バイトコードは、プリミティブよりは遅い。しかし、バイトコードで読み込まれた関数は、簡単に修正したり、再読込みしたりできる。さらに、バイトコード・ファイルは、[プラットフォームに依存しない](../Page/プラットフォーム_\(コンピューティング\).md "wikilink")。Emacsについてくる標準的なEmacs Lispコードは、バイトコードで読み込まれるが、利用者の参照用として、対応するソース・ファイルも大抵付いている。利用者の拡張はそれほど大きくもなく、また計算機の負担も小さいので、普通はバイト・コンパイルされない。

## 言語機能

「cl」パッケージは、[Common Lispのサブセットとしてはかなり大規模な実装であり](../Page/Common_Lisp.md "wikilink")、注目に値する。

Emacs Lispは、静的でなく (字句的でもなく) [動的スコープ](../Page/動的スコープ.md "wikilink")を使う。したがって、もし変数がある関数の[スコープ](../Page/スコープ.md "wikilink")で宣言されると、その関数から呼び出されたサブルーチンにおいても有効になる。これはもともとは、利用者のカスタム化のための高度な柔軟性を提供するためのものだった。しかし、動的スコープには短所がいくつかある。第一に、別々な関数の変数間での不本意な相互作用のため、大きなプログラムではバグを簡単に生じやすい。第二に、動的スコープ下での変数アクセスは、字句的スコープのそれより、一般に遅い。そのため、Emacs Lispを字句的スコープに変換する、という計画が立てられたが、まだ完了はしていない。「cl」パッケージの`lexical-let`マクロは、Emacs Lispのプログラマに効率的な字句的スコープを提供している。「cl」はよく使われているが、`lexical-let`はめったに使われない。

Emacs 24 では静的スコープが使えるようになった。

Emacs Lispは、他の多くのLisp実装でおこなわれている[末尾再帰](../Page/末尾再帰.md "wikilink")の最適化をしない。最適化されていない末尾再帰は最終的に[スタックオーバーフロー](../Page/スタックオーバーフロー.md "wikilink")に至る可能性がある。

## 脚注

<references/>

## 参考文献

  - [Free Software Foundation編著](../Page/フリーソフトウェア財団.md "wikilink")「GNU Emacs Lisp Reference Manual」[Walking Lint訳](https://ja.wikipedia.org/wiki/Walking_Lint "wikilink")、[ビレッジセンター](../Page/ビレッジセンター.md "wikilink")出版局、[1992年](../Page/1992年.md "wikilink")、ISBN 4-938704-02-1
  - [リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")他「GNU Emacs Lispリファレンス・マニュアル」[榎並嗣智](https://ja.wikipedia.org/wiki/榎並嗣智 "wikilink")、[井田昌之](https://ja.wikipedia.org/wiki/井田昌之 "wikilink")監訳、透土社、[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")、ISBN 4-924828-39-4
  - [Bil Lewis](https://ja.wikipedia.org/wiki/Bil_Lewis "wikilink"), [Dan LaLiBerte](https://ja.wikipedia.org/wiki/Dan_LaLiBerte "wikilink"), [Richard Stallman](../Page/リチャード・ストールマン.md "wikilink"), the GNU Manual Group「Emacs Lispリファレンスマニュアル」[大木敦雄](https://ja.wikipedia.org/wiki/大木敦雄 "wikilink")訳、[アスキー出版局](../Page/アスキー_\(企業\).md "wikilink")、[2000年](../Page/2000年.md "wikilink") ISBN 4-7561-3414-9

## 外部リンク

  - [GNUプロジェクトのEmacsページ](http://www.gnu.org/software/emacs/emacs.html)
  - R. Chassell著, "[Programming in Emacs Lisp, an Introduction](http://www.gnu.org/software/emacs/emacs-lisp-intro/emacs-lisp-intro.html)"
  - B. Lewis, D. LaLiberte, R. Stallman著, "[GNU Emacs Lisp Reference Manual](http://www.gnu.org/software/emacs/elisp-manual/elisp.html)"
  - [Emacs Wiki](http://www.emacswiki.org/cgi-bin/wiki) の ["EmacsLisp"](http://www.emacswiki.org/cgi-bin/wiki/EmacsLisp)

[Category:LISP](https://ja.wikipedia.org/wiki/Category:LISP "wikilink")

1.  "GNU Emacs Lisp is largely inspired by Maclisp, and a little by Common Lisp. If you know Common Lisp, you will notice many similarities. However, many features of Common Lisp have been omitted or simplified in order to reduce the memory requirements of GNU Emacs. Sometimes the simplifications are so drastic that a Common Lisp user might be very confused. We will occasionally point out how GNU Emacs Lisp differs from Common Lisp." (和訳「GNU Emacs Lispは、大いにMaclispに (そして若干Common Lispに) 触発されている。もしCommon Lispをご存じなら、多数の類似点に気づくだろう。しかし、Common Lispの多くの機能は、GNU Emacsのメモリ要件のために、けずられたり、簡略化されたりしている。ときには、簡略化がすぎて、Common Lispの利用者はこんがらがるかもしれない。GNU Emacs LispとCommon Lispの違いは、ときおりふれることにする。」) Emacs Lisp Manualの"Introduction"章"History"節より
2.  "So the development of that operating system, the GNU operating system, is what led me to write the GNU Emacs. In doing this, I aimed to make the absolute minimal possible Lisp implementation. The size of the programs was a tremendous concern. There were people in those days, in 1985, who had one-megabyte machines without virtual memory. They wanted to be able to use GNU Emacs. This meant I had to keep the program as small as possible." (和訳「つまり、GNU Emacsを書くことが，オペレーティング・システム、すなわち、GNUオペレーティング・システムの開発につながった。このことで、わたしは極小のLisp実装をつくることになった。プログラムの大きさは，重要な関心事だった。1985年当時，仮想記憶のない1メガバイトのマシンをもつ人たちは大勢いた。そんな人たちもGNU Emacsを使いたがっていた。それで私は、プログラムをなるたけ小さく作る必要があった。」) ["My Lisp Experiences and the Development of GNU Emacs"](http://www.gnu.org/gnu/rms-lisp.html)より