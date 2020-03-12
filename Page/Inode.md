> この記事は[Inode](https://ja.wikipedia.org/wiki/Inode)から翻訳されています。


**inode**（アイノード）は、[ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")などの[Unix系](../Page/Unix系.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")で古くから使われているデータ構造である。inode には[ファイル](../Page/ファイル_\(コンピュータ\).md "wikilink")、[ディレクトリ](../Page/ディレクトリ.md "wikilink")などのファイルシステム上のオブジェクトに関する基本情報が格納される。

[ReiserFS](../Page/ReiserFS.md "wikilink")などの最近のUnix系ファイルシステムでは inode を使用していないが、同等の機能を提供するには同等の情報をどこかに格納しなければならない。`stat`[システムコール](../Page/システムコール.md "wikilink")がそれらのデータをプログラム向けに提供するので、これを statデータと呼ぶことがある。

## 概要

[Linux](../Page/Linux.md "wikilink")では、このようなデータの[カーネル](../Page/カーネル.md "wikilink")でのメモリ上の表現を `struct inode` と呼ぶ。[BSD](../Page/BSD.md "wikilink")系システムでは `vnode` と呼ぶが、この *vnode* の *v* はカーネル内の [仮想ファイルシステム](../Page/仮想ファイルシステム.md "wikilink")層から来ている。

[POSIX](../Page/POSIX.md "wikilink")標準で規定されているファイルシステムの動作は従来からの[UNIX](../Page/UNIX.md "wikilink")ファイルシステムに大きく影響されている。通常ファイルは以下のような属性を持つことを要求されている:

  - ファイルの長さ（バイト数）
  - デバイスID（ファイルを格納しているデバイスを識別）
  - ファイル所有者の[ユーザーID](../Page/ユーザー識別子.md "wikilink")
  - ファイルの[グループID](https://ja.wikipedia.org/wiki/グループ識別子 "wikilink")
  - ファイルシステム内でファイルを識別する inode 番号
  - ファイルモード（[ファイルパーミッション](../Page/ファイルパーミッション.md "wikilink")）
  - 最終 inode 更新時(ctime)、最終ファイル更新時(mtime)、最終参照時(atime) を示す[タイムスタンプ](https://ja.wikipedia.org/wiki/タイムスタンプ "wikilink")群
  - その inode を指す[ハードリンク](../Page/ハードリンク.md "wikilink")がいくつあるかを示す[参照カウント](../Page/参照カウント.md "wikilink")

*inode* という用語は[ブロックデバイス](https://ja.wikipedia.org/wiki/ブロックデバイス "wikilink")上の inode も意味し、通常ファイルやディレクトリや場合によっては[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")にも対応している。この概念は破損したファイルシステムのリカバリにおいて特に重要である。

inode 番号は、その inode が記録されているデバイス上で一意の[整数](../Page/整数.md "wikilink")値である。全てのファイルは inode に物理的にリンクされている。プログラムがファイルをファイル名で参照するとき、システムはそのファイル名に対応する inode を検索する。

`stat`システムコールはファイルの inode 番号やその他の inode 内の情報の一部を得る機能である。

*inode* の *i* が何を意味するのかは不明確である。UNIXの開発者[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")は、それを聞かれたとき以下のように述べている:

  -
    実際、私にもわからない。我々が使い始めたときは単なる用語だった。たぶん "index" が元になっているんじゃないかと思う。というのはちょっと変わったファイルシステム構造があって、ディレクトリを使った階層構造があるのに全てのファイルのアクセス情報をディスク内のフラットな配列に格納していたんだ。だから i-number というのはその配列のインデックスで、i-node はその配列の要素だろう。（"i-" という書き方は初版のマニュアルで使われていたが、徐々にハイフンが無くなっていった）。

[代替文=](https://ja.wikipedia.org/wiki/ファイル:Ext2-inode.svg "wikilink")

## 関連

ファイルシステムに慣れていないユーザーの多くは、inode のコンセプトを利用するファイルシステムの特性に驚く。

  - 複数の名前が同じ inode にリンクしていると（[ハードリンク](../Page/ハードリンク.md "wikilink")）、どの名前も等価と言える。ファイルを最初に作成したときの名前は特別な意味を持たない。これは[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")がオリジナルの名前に依存しているのと全く異なる。
  - リンクを全く持たない inode もありうる。通常そのようなファイルはディスクから削除され、そのリソース（ディスクブロック）はファイル削除処理の過程で再利用のために解放されるが、何らかの[プロセス](../Page/プロセス.md "wikilink")がそのファイルを使用中ならば、アクセスし続けることができ、最後にクローズされるときに削除処理が行われる。このため、プログラムを改版（リコンパイル）するときは、以前の[実行ファイル](../Page/実行ファイル.md "wikilink")をまず削除して、新しい版の実行ファイルは新たな inode で作成されるようにすることが推奨される。これにより、古い版が実行中であっても何ら問題なく処理を続行することになる。（訳注：削除しないで上書きすると、実行中の実行ファイルが書き換えられるため、[メモリ管理](../Page/メモリ管理.md "wikilink")の実装によってはおかしな状態が発生する）。
  - 従来、オープン中のファイル（[ファイル記述子](../Page/ファイル記述子.md "wikilink")）からオープンされたファイル名を得ることはできなかった。オペレーティングシステムは一度ファイル名を inode番号に変換すると、ファイル名の方を忘れてしまう。従って、`getcwd()` や `getwd()` といったライブラリ関数は "`.`" ディレクトリに対応する inode 番号からその親ディレクトリを捜し、最終的に "`/`" ディレクトリまでたどることでフルパス名を得ている。この無駄な処理を省くため、[SVR4](../Page/UNIX_System_V.md "wikilink") や [Linux](../Page/Linux.md "wikilink") システムは追加情報を保持している。
  - ディレクトリのハードリンクは古くから可能だった。これによりディレクトリ構造は[木構造ではなく任意の](../Page/木構造_\(データ構造\).md "wikilink")[有向グラフとなっている](../Page/グラフ理論.md "wikilink")。あるディレクトリを自身の親ディレクトリとすることも可能である。最近のシステムではそのような混乱の元となる状態を防ぐようになっている。

## 実用上の考慮

[UNIX](../Page/UNIX.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の[システムアドミニストレータ](../Page/システムアドミニストレータ.md "wikilink")が使用する[プログラムには](../Page/プログラム_\(コンピュータ\).md "wikilink")、ファイルを特定するために inode 番号を表示するものがある。[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")の健全性チェックユーティリティの[`fsck`](https://ja.wikipedia.org/wiki/fsck "wikilink")や`pfiles`がそのようなコマンドの例である。そこで inode 番号を[ファイルのパス名に変換する](../Page/ファイル_\(コンピュータ\).md "wikilink")（およびその逆変換をする）必要が生じる。これはファイル名検索ユーティリティ [`find`](https://ja.wikipedia.org/wiki/find "wikilink")（の `-inum` オプション）や [`ls`](https://ja.wikipedia.org/wiki/ls "wikilink") コマンドに適当なオプション（多くの場合 `-i`）を付けることで実現される。

また、「ファイルが削除された際に何らかのプロセスがそのファイルを使用している場合、そのプロセスからはアクセスが継続できる。」という特徴がセキュリティ上問題となる場合がある。例えば、多くのプロセスが参照しているライブラリのセキュリティアップデートを適用した後、当該プロセスからは旧バージョンのライブラリにアクセスし続けるため、脆弱性が完全に修正されないという事態が発生する。したがって、特にシステムの中核に位置するようなライブラリをアップデートした際には動作上問題がなくてもシステムを再起動する等の対策が必要となってくる。

## トリビア

International Association of Computer Investigative Specialists (IACIS[1](http://www.iacis.info/iacisv2/pages/home.php))の2003年の会議で、"inode" は "I'm Not Operating DOS Ever"（DOSなど二度と触るか）の略であるという提案がなされた。しかし、全くの嘘として退けられた。

## 外部リンク

  - [The Linux Virtual File-system Layer: Inodes and Operations](http://www.cse.unsw.edu.au/~neilb/oss/linux-commentary/vfs-7.html) - [Linux](../Page/Linux.md "wikilink")でのinode（英語）

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink")