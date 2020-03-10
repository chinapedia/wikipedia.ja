> この記事は[Patch](https://ja.wikipedia.org/wiki/Patch)から翻訳されています。


**patch**（パッチ）は、テキストファイルに[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")処理を行う[UNIX](../Page/UNIX.md "wikilink")上の[プログラム](../Page/プログラム_\(コンピュータ\).md "wikilink")。「パッチファイル」と呼ばれるファイルに格納された命令群に従ってテキストファイルを更新する。パッチファイル（単にパッチとも呼ばれる）自体もテキストファイルであり、[diff](https://ja.wikipedia.org/wiki/diff "wikilink") を使って元のファイルと更新後のファイルの差分をとることで作成される。パッチによるファイルの更新を「パッチを当てる」などという。

## 歴史

patch を最初に作ったのは（後に [Perl](../Page/Perl.md "wikilink") を開発した）[ラリー・ウォール](https://ja.wikipedia.org/wiki/ラリー・ウォール "wikilink")であり、彼はそれを1985年5月に[`mod.sources` へポストした](http://groups-beta.google.com/group/mod.sources/browse_thread/thread/c5240ceb77b7f586/488b0929254d936a)（後に `comp.sources.unix` となった）。このプログラムは[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")の一部となり、[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")が保守している。

## 使用法

patchはプログラマの間でのやり取りのために作られ、ソースコードの更新のためによく用いられている。そのため、パッチソフトと言えばプログラムに使うものという先入観がある人が多いが、実際にはあらゆるテキストに適用可能である。パッチソフトは「当て布」という本来の語義に反して、テキストの追加のみでなく削除も行うことができる。なおpatchは、バイナリ形式のパッチを扱うプログラムではない。

## ソフトウェア開発におけるパッチ

patch への入力となる diff ファイルは読み取り可能なテキストファイルであり、使う前に人間が中身を確かめることが容易である。より進んだ diff を使った場合、パッチ適用前に独自に修正されたファイルにもパッチを適用可能である（それらの修正が patch を妨げない限り）。これは例えばコンテキスト形式 (diff -c) やユニファイド形式 (diff -u) を使う場合である。これらの diff は変更箇所の前後の文脈（コンテキスト）も diff の一部として示す。patch はそれらの情報を使って、行番号がずれていてもパターンマッチングによってパッチ適用箇所を特定する（もちろん、最初は行番号を使ってパッチを適用しようと試みる）。

コンテキスト形式やユニファイド形式は行番号に依存しないのでパッチに適している。ユニファイド形式は慣れていないと読みにくく、コンテキスト形式の方が分かりやすい。ただし、ユニファイド形式の方が非常にコンパクトになる。また、多くのオープンソースプロジェクトは「diff -u 変更前ファイル 変更後ファイル」で生成されたユニファイド形式のパッチを推奨している。

[diff](https://ja.wikipedia.org/wiki/diff "wikilink") プログラム以外にも diff 形式のファイルを生成するプログラムがある。ほとんどの[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")（[Git](https://ja.wikipedia.org/wiki/Git "wikilink")、[Subversion](../Page/Apache_Subversion.md "wikilink")、[CVS](../Page/Concurrent_Versions_System.md "wikilink")、[RCSなど](../Page/Revision_Control_System.md "wikilink")）は対応している。バージョン管理システムでもパッチは重要な要素である。

[オープンソース](../Page/オープンソース.md "wikilink")の世界では、diff と patch を使って修正をやり取りするのが一般的である。あるフリーソフトウェアのソースを外部の者がダウンロードし、修正を加え、それを diff 形式でチームに送る。そうすると、チームメンバーはそれをパッチとして適用する前にレビューでき、外部の者がアクセスできるソースではなく、開発中の最新のソースにパッチを適用することで修正を取り込むことができる。

## 使用例

### ファイル単位

ファイル単位でパッチを作成するには、以下のコマンドをシェル上で実行する。

``` console
$ diff -u test.c.orig test.c > mods.patch
```

パッチを適用するには、以下のコマンドをシェル上で実行する。

``` console
$ patch -p0 < mods.patch
```

パッチファイル `mods.patch` 内にはパッチを適用すべきファイル名が書かれているためコマンド中に指定する必要がない。

パッチを適用前の状態に戻すには '-R' オプションを使用する。

``` console
$ patch -p0 -R < mods.patch
```

diff を適用したバージョン（上記test.c）とパッチを適用しようとしているバージョンが異なる場合、パッチは正しく適用できない。 例えば、パッチを適用しようとしているテキストの先頭に行が挿入されていると、パッチファイル内に書かれている行番号が一致しなくなる。 patch はパターンマッチングで修正する前後の行を特定するため、ある程度は変更に対処できる。また修正箇所近辺の内容が違っている場合も対処可能である（fuzz）。ただし、独自の修正を加えられたソースにパッチを適用して正しく動作するかは保証されない。

### フォルダ単位

フォルダ単位でパッチを作成し、元に戻すには以下のように行う。

``` console
$ diff -ur old new > mods.patch
```

``` console
$ cd old
$ patch -p1 < mods.patch
```

サブディレクトリにあるファイルへのパッチ適用には `-p`*`number`* オプションを必要とし、ソースツリーのベースディレクトリがパッチファイルに含まれている場合は *number* に 1、さもなくば 0 を指定する。例えば、[git](https://ja.wikipedia.org/wiki/git "wikilink") などを使うと、a/test.c と b/test.c に対するパッチという形で古い方を仮想的にフォルダa、新しい方を仮想的にフォルダbに入れるので、この形式のパッチは、`patch -p1 < mods.patch` を使う。

## 移植

UNIX系システムが起源だが、patch は[Microsoft Windowsなどにも移植されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。Windows 版の patch は [GNU utilities for Win32](http://unxutils.sourceforge.net/) にある。

Windows Vista 以後はプログラム名に「patch」という単語が含まれていると [UAC](../Page/ユーザーアカウント制御.md "wikilink") によって[マルウェア](https://ja.wikipedia.org/wiki/マルウェア "wikilink")と判断されるので、UAC に対応したものを利用する必要がある。

## 関連項目

  - [パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")
  - [diff](https://ja.wikipedia.org/wiki/diff "wikilink")
  - [rsync](https://ja.wikipedia.org/wiki/rsync "wikilink")
  - [xdelta](https://ja.wikipedia.org/wiki/xdelta "wikilink")

## 外部リンク

  - [patch(1)](http://linuxjm.sourceforge.jp/html/GNU_patch/man1/patch.1.html) - マニュアル
  - [patchutils](http://freshmeat.net/projects/patchutils/) - パッチ操作ユーティリティ
  - [GNU tools for Win32](http://gnuwin32.sourceforge.net/) - Win32 への移植版（diff と patch を含む）(Version 2.5.9-7 UAC制限)
  - [GNU utilities for Win32](http://unxutils.sourceforge.net/) - Win32 への移植版（diff と patch を含む）(Version 2.5 UAC制限)
  - [Git for Windows](https://msysgit.github.io/) - Win32 への移植版が付属している (Version 2.5 **UAC対応済**)
  - [Strawberry Perl for Windows](http://strawberryperl.com/) - Win32 への移植版が付属している (Version 2.5.9 **UAC対応済**)
  - [diffstat](http://invisible-island.net/diffstat/)

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:システムソフトウェア](https://ja.wikipedia.org/wiki/Category:システムソフトウェア "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink") [Category:1985年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1985年のソフトウェア "wikilink")