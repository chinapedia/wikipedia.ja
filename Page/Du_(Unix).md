> この記事は[Du \(Unix\)](https://ja.wikipedia.org/wiki/Du_\(Unix\))から翻訳されています。


**`du`**（***d**isk **u**sage*の略称から）はファイルのスペース使用量、つまり[ファイルシステム](../Page/ファイルシステム.md "wikilink")上で[ディレクトリ](../Page/ディレクトリ.md "wikilink")または[ファイルが実際に使用しているスペースを推定するために使われる標準的な](../Page/ファイル_\(コンピュータ\).md "wikilink")[Unix](../Page/UNIX.md "wikilink")[プログラム](../Page/プログラム_\(コンピュータ\).md "wikilink")。

## 歴史

`du`ユーティリティが最初にでてきたのは[AT\&T UNIXのバージョン](https://ja.wikipedia.org/wiki/Unixの歴史#1970s "wikilink")1である。[GNU](../Page/GNU.md "wikilink") [coreutilsにバンドルされているバージョンの](../Page/GNU_Core_Utilities.md "wikilink")`du`はTorbjorn Granlund、David MacKenzie、Paul EggertとJim Meyeringによって書かれた。\[1\]

## 仕様

デフォルトでは、[Single UNIX Specification](../Page/Single_UNIX_Specification.md "wikilink") (SUS) は、`du`が現在のディレクトリに含まれる各ファイルとディレクトリに割り当てられたファイルスペースを表示することを仕様に定めている。 リンクはリンク先のものではなく、リンクファイルとしてのサイズを表示するだろう。ディレクトリの内容のサイズは期待通りに表示される。

`du`が報告するのは割り当てられたスペースであって絶対的なファイルのスペースではないため、`du`によって表示されるファイルシステム上のスペースの合計値は、ファイルが[削除されたが](../Page/Rm_\(UNIX\).md "wikilink")、そのブロックはまだ解放されていない場合には、によって表示されるものとは異なる。また、ファイルシステムのデータブロックを割り当てる最小限（minfree）設定とスーパーユーザのプロセスは、合計ブロック数と、使用されているブロックと利用可能なブロックの合計値の間に不一致を作り出す。最小限（minfree）設定は通常合計ファイルシステムサイズの5%程度に設定されている。さらなる情報は[core utils faq](https://www.gnu.org/software/coreutils/faq/coreutils-faq.html#df-Size-and-Used-and-Available-do-not-add-up)を見よ。

## 使用方法

`du`は1つの引数をとり、それは`du`が動作するパス名を指定する。もし指定されなければ、現在のディレクトリが使われる。SUSは`du`が以下のオプションを取ることを規定している:

  -
    `-a`、デフォルトの出力に加えて、ディレクトリ以外の各エントリの情報も表示する。
    `-c`, 他の引数によって見つかったディスク使用量の総計を表示する。
    `-d #`、集計を行うべき深さ。-d 0は現在のレベルを集計し、-d 1はサブディレクトリを集計し、-d 2はサブサブディレクトリを、など。
    `-H`、コマンドラインで指定されたリンク参照先のディスク使用量を計算する
    `-k`、512バイトではなく、1024[バイトの倍数でサイズを表示する](../Page/バイト_\(情報\).md "wikilink")。
    `-L`、リンク参照先がどこであってもディスク使用量を計算する。
    `-s`、現在のディレクトリの使用量の合計値のみを報告して、そこに含まれている各ディレクトリについては報告しない。
    `-x`、パス名引数が指定されたデバイス上のファイルとディレクトリのみをたどる。

他のUnixとUnix-likeなオペレーティングシステムはさらなるオプションを追加していることがある。BSDとGNUの`du`は`-h`オプションを指定すると、適切な\[SI接頭辞\]\]を付けた単位を追加して（例えば10[MB](../Page/メガバイト.md "wikilink")）、ユーザが読みやすいフォーマットでディスク使用量を表示する。

## 例

ディレクトリの合計値（-s）を[キロバイト](../Page/キロバイト.md "wikilink")単位（-k）で:

``` console
$ du -sk *
152304  directoryOne
1856548 directoryTwo
```

ディレクトリの合計値（-s）を[人間が読みやすいフォーマットで](https://ja.wikipedia.org/wiki/対人可読媒体 "wikilink")（-h : バイト、キロバイト、メガバイト、ギガバイト、テラバイトペタバイト）:

``` console
$ du -sh *
149M directoryOne
1.8G directoryTwo
```

現在のディレクトリにある隠しファイルも含んだすべてのサブディレクトリとファイルのディスク使用量（ファイルサイズでソート）:

``` bash
 $ du -sk .[!.]* *| sort -n
```

現在のディレクトリにある隠しファイルも含んだすべてのサブディレクトリとファイルのディスク使用量（ファイルサイズの逆順でソート）:

``` bash
 $ du -sk .[!.]* *| sort -nr
```

現在のディレクトリ直下の各サブディレクトリのウェイト（サイズ）（-d 1）を、最後に全体の合計値をつけて（-d）、すべて人間に読みやすいフォーマットで（-h）:

``` bash
 $ du -d 1 -c -h
```

あるいはGNUのduでは:

``` bash
 $ du --max-depth=1 -c -h
```

ルートディレクトリ直下の各サブディレクトリのウェイト（サイズ）（-d 1と続く/）を、最後に全体の合計値をつけて（-d）、すべて人間に読みやすいフォーマットで（-h）、他のファイルシステムまでたどらない（-x）。/var、/tmp、または他のディレクトリがルートディレクトリとは別の記憶装置にある時に有用である。:

``` bash
 $ du -d 1 -c -h -x /
```

あるいはGNUのduでは:

``` bash
 $ du --max-depth=1 -c -h -x /
```

## 関連項目

  - [UNIXユーティリティの一覧](https://ja.wikipedia.org/wiki/UNIXユーティリティの一覧 "wikilink")

  -
  - [ディスク使用量アナライザー](https://ja.wikipedia.org/wiki/ディスク使用量アナライザー "wikilink")

  - [ncdu](https://ja.wikipedia.org/wiki/Ncdu "wikilink")

## 参考文献

## 外部リンク

  -
### Manual pages

  -
  -
  -
  -
[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink")

1.  <https://linux.die.net/man/1/du>