> この記事は[Occam](https://ja.wikipedia.org/wiki/Occam)から翻訳されています。


**Occam**は、[並行プログラミング](https://ja.wikipedia.org/wiki/並行プログラミング "wikilink")言語である。[CSPに基づいており](https://ja.wikipedia.org/wiki/Communicating_Sequential_Processes "wikilink")、多くの機能はCSPから由来している。Occamという名称は[オッカムのウィリアム](../Page/オッカムのウィリアム.md "wikilink")の「[オッカムの剃刀](../Page/オッカムの剃刀.md "wikilink")」から来ている。OccamはCSPの実用的な実装と言うこともできる。

並行向け以外の部分は[手続き的](../Page/手続き型プログラミング.md "wikilink")（ないし[命令的](../Page/命令型プログラミング.md "wikilink")）である。INMOS社が同社の[トランスピュータ](../Page/トランスピュータ.md "wikilink")のために開発したが、他のプラットフォームへの移植もされている。現在使われているものでは、XMOS（[:en:XMOS](https://ja.wikipedia.org/wiki/:en:XMOS "wikilink")）のXC（[:en:XC (programming language)](https://ja.wikipedia.org/wiki/:en:XC_\(programming_language\) "wikilink")）がOccamの影響を受けた言語である。

## 概要

以下の例で、インデントとフォーマットはコードを解析する上で重要である。 式は改行によって完結する。式を羅列する場合はインデントが同じでなければならない([オフサイドルール](../Page/オフサイドルール.md "wikilink"))。

プロセス間の通信は**チャネル**を通して行われる。あるプロセスがチャネルにデータを出力する場合 **[\!](https://ja.wikipedia.org/wiki/! "wikilink")** を使い、チャネルからデータを入力するには **[?](https://ja.wikipedia.org/wiki/? "wikilink")** を使う。入出力は通信相手がレディ状態となってデータ送受信が可能になるまでブロックされる。 以下の例では、 c が[変数](../Page/変数_\(プログラミング\).md "wikilink")、keyboard と screen が[チャネル](https://ja.wikipedia.org/wiki/チャネル "wikilink")を示している。

` keyboard ? c`

` screen ! c`

**SEQ**はそれに続く式のリストを逐次的に実行することを示す。他のプログラミング言語のように逐次実行が暗黙のうちに採用されることはない。以下の例で「:=」は代入である。

` SEQ`
`   x := x + 1`
`   y := x * x`

**PAR**はそれに続く式のリストを並列的に実行してもよいことを示す。

` PAR`
`   x := x + 1`
`   y := y * 2`

**ALT**は選択実行を可能とする。ガード部をもつコマンドのリストが後に続き、ガード部はboolean値を返す条件式と入力チャネル式(どちらも省略可能)から成る。各ガードは条件が真でかつ入力チャネルから入力があったときに成功する。実行時には複数のガードが同時に成功してもかまわない。

` ALT`
`   count1 < 100 & c1 ? data`
`     SEQ`
`       count1 := count1 + 1`
`       merged ! data`
`   count2 < 100 & c2 ? data`
`     SEQ`
`       count2 := count2 + 1`
`       merged ! data`
`   status ? request`
`     SEQ`
`       out ! count1`
`       out ! count2`

この例は c1 および c2 のチャネルからデータを読み込んで、ひとつの merged というチャネルにそれを渡すものである。 countN が 100 になると、対応する入力チャネルからの入力は受け付けなくなる。status チャネルからリクエストがあると、c1 および c2 から何回データを受け取ったかが out チャネルに出力される。

## 言語バージョン

### Occam 2

**Occam 2**は、1987年にINMOS社が開発した拡張版であり、浮動小数点演算、その他の機能、たとえば整数サイズを16ビットと32ビットにしたり、文字型を追加したりしている。

この版で Occam は実用的なプログラムが書ける機能を備えた。Occam 1 はそういう意味では新しい言語を研究したりアルゴリズムを開発したりするものでしかなかった。

### Occam 2.1

**Occam 2.1**は二度目の拡張版であり1988年にINMOS社が開発した。INMOSが開発した最後のバージョンである。 番号の増加は小さいが、使いやすさの面では大きな変更が加えられている。

  - 名前つきデータ型 (DATA TYPE x IS y);
  - 名前つきレコード;
  - パックされたレコード;
  - 型変換ルールを柔軟にした;
  - 新しい演算子の追加(たとえば BYTESIN);
  - チャネルの型変更とチャネル配列
  - 固定長配列をリターン値とすることができる;

### Occam 3

**Occam 3**は、INMOSのプログラマが作成した次世代のOccam言語の仕様である。 この仕様はコミュニティのコメントを求めて配布された。 主な変更点はコードの共有、同時開発、コードの再利用に焦点を当てたものである。

[Occam 3](http://www.wotug.org/occam/documentation/oc3refman.pdf) ここに英語の仕様があるが、この仕様の実際に動作するコンパイラは作成されなかった。それは主にINMOS自体とINMOSを買収した会社の問題である。

他のチームが Occam 3 のいくつかの要素を Occam 2.1 コンパイラに導入し、Occam 2.5 と呼ばれる中間のバージョンを作成した。

### Occam 2.5

**Occam 2.5**は、Kent Retargettable Occam compiler (KRoC)に与えられた一般的な名称である。 このバージョンは以下のような拡張を Occam 2.1 に加えている。

  - ネストしたプロトコル
  - 実行時プロセス生成
  - 移動可能なチャネル、データ、プロセス
  - 再帰
  - プロトコル継承
  - 配列生成
  - 拡張されたランデブー機能

KRoC チームはコンパイラを開発しWebサイトに公開している。π計算（[:en:π-calculus](https://ja.wikipedia.org/wiki/:en:π-calculus "wikilink")）を使用していることから、最近チームはコンパイラの名称をOccam-Piに変更した。

## 外部リンク

以下のリンク先は全て英語で記述されている。

  - [Internet Parallel Computing Archive: occam](http://wotug.ukc.ac.uk/parallel/occam/) (Documentation and implementations)
  - [The Transterpreter, an occam virtual machine](http://www.transterpreter.org/)
  - [KRoC - Kent Retargettable occam Compiler](http://www.cs.kent.ac.uk/projects/ofa/kroc/)
  - [occam tutorial](http://frmb.org/occtutor.html)

[Category:プログラミング言語](https://ja.wikipedia.org/wiki/Category:プログラミング言語 "wikilink") [Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink") [Category:並行計算](https://ja.wikipedia.org/wiki/Category:並行計算 "wikilink")