> この記事は[Cat \(UNIX\)](https://ja.wikipedia.org/wiki/Cat_\(UNIX\))から翻訳されています。


**`cat`**（キャット）は[UNIX](../Page/UNIX.md "wikilink")の標準[コマンドであり](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")、ファイルを連結させたり表示したりするのに用いる。`cat`は連結することを意味する「catenate」の略である。

## 仕様

[Single UNIX Specificationでは](../Page/Single_UNIX_Specification.md "wikilink")、`cat`は引数で指定されたファイルの内容を指定された順番に[標準出力](https://ja.wikipedia.org/wiki/標準出力 "wikilink")に書き出すと規定している。 ファイル名のリストに「`-`」が含まれていた場合、`cat`はリストのその時点で[標準入力](https://ja.wikipedia.org/wiki/標準入力 "wikilink")からデータを読み込む。ファイル名が指定されなかった場合も`cat`は標準入力から読み込む。

### 拡張

BSD版の`cat`とGNU版の`cat`はどちらも次のオプションを指定できる。

  - `-b`（GNUでは`--number-nonblank`とも）:空白でない行の数を数え、行番号を付加する。
  - `-n`（GNUでは`--number`とも）:すべての行の数を数え、行番号を付加する。
  - `-s`（GNUでは`--squeeze-blank`とも）:隣接する空白行を除く。
  - `-v`（GNUでは`--show-nonprinting`とも）:表示できない文字も表示する。ただしタブと改行文字を除く。
  - `-t`（BSD）または`-T`（GNU）:`-v`と同じだが、タブを`^I`と表示する。
  - `-e`（BSD）または`-E`（GNU）:`-v`と同じだが、改行文字を`$`と表示する。

## 実例

<table>
<thead>
<tr class="header">
<th><p>コマンド</p></th>
<th><p>コマンドの説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>file1の内容を表示する</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>file1およびfile2の内容を連結し、端末上にその結果を表示する</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>file1およびfile2の内容を連結し、ファイルfile3にその結果を出力する</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>新規ファイルnewfileを作成もしくは上書きして、入力したい内容を打ち込み、CTRL+Dコマンドで終了する。入力された内容は新規ファイルに書き込まれる。</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>file1およびfile2の内容を連結し、ファイルfile3にその結果を行番号とともに出力する</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>file1の内容をfile2にコピーする</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>file1の内容をfile2に追加する</p></td>
</tr>
<tr class="even">
<td><p>sort &gt; test4}}</p></td>
<td><p>file1およびfile2およびfile3の内容を連結し、連結された行を頭文字の順に並び替え、その内容を新規ファイルに書き出す。</p></td>
</tr>
<tr class="odd">
<td><p>less}}</p></td>
<td><p>file1およびfile2の内容を連結し、<a href="https://ja.wikipedia.org/wiki/less" title="wikilink">less</a>コマンドを実行する</p></td>
</tr>
</tbody>
</table>

## UNIXの文化

### ジャーゴンファイルでの定義

[ジャーゴンファイル](../Page/ジャーゴンファイル.md "wikilink")のバージョン4.3.3には、`cat`の定義として次のように記されている[1](http://www.catb.org/jargon/html/C/cat.html)。

> 1.  ファイル全体をスクリーンまたは流し台か何かにとめどなく吐き出すこと（類:[`blast`](http://www.catb.org/jargon/html/B/blast.html)）。
> 2.  転じて、膨大なデータを注意深く目を通すこともせずに準備ができていない目標に向かって吐き捨てること。使用例：馬鹿げている。UNIX以外の場所で使われることは稀である。参照:[`dd`](http://www.catb.org/jargon/html/D/dd.html)、[BLT](http://www.catb.org/jargon/html/B/BLT.html)。
>
> UNIXファンの間では、`cat(1)`はユーザインターフェースデザインのよい手本とされている。`cat`はファイルの内容に空白やヘッダのような余分なものを一切付加せずに提供してくれるためであり、またテキストファイルのみならずどんな種類のデータに対しても正しく動作するためだ。
> UNIX嫌いの間では、`cat(1)`は悪いユーザインターフェースデザインの[正統な](http://www.catb.org/jargon/html/C/canonical.html)手本とされている。それはこの悲しいまでにわかりづらい名称のためである。`cat`は、ファイルの連結（concatenate）に使うよりもむしろ標準出力への出力に使われることの方がはるかに多い。後者の使用法に対する`cat`という名称は、ちょうど[LISP](https://ja.wikipedia.org/wiki/LISP "wikilink")の[`cdr`](http://www.catb.org/jargon/html/C/cdr.html)のように非直感的である。

### `cat`コマンドとUUOC

UUOCは「無駄な`cat`の使用（**U**seless **U**se **o**f **`c`**`at`）」の略である。 Usenetのcomp.unix.shellに投稿された賢者の観察によると， <q> `cat`の役割はファイルを連結することである。もしファイルが1つしかないのであれば、何かと連結しようとするのは時間と手間の無駄でしかない </q> 。 にも関わらず、次のような使用をよく見かける。

代わりに次のように書けば簡単である。  次も同じであるが、より古典的な方法である。  [1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")からUUOCの授賞が、主にRandal L. Schwartzによって時々行われている。[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")の[ハッカー](../Page/ハッカー.md "wikilink")たちの間では、UUOCに挙げられた例を修正することはmoggyが猫（cat）を表すことから**demoggification**と呼ばれる。

## 関連項目

  - [GNU Core Utilities](../Page/GNU_Core_Utilities.md "wikilink")
  - [フィルタ (ソフトウェア)](../Page/フィルタ_\(ソフトウェア\).md "wikilink")

## 外部リンク

  - [cat](https://pubs.opengroup.org/onlinepubs/009695399/utilities/cat.html) [Single UNIX Specificationによる規定](../Page/Single_UNIX_Specification.md "wikilink")（英語）
  - [cat](https://www.gnu.org/software/coreutils/manual/html_node/cat-invocation.html) man page（GNU coreutils、英語）
  - [Useless Use of Cat Award](http://porkmail.org/era/unix/award.html)（英語）

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")