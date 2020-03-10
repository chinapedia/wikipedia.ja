> この記事は[Sort \(UNIX\)](https://ja.wikipedia.org/wiki/Sort_\(UNIX\))から翻訳されています。


[サムネイル](https://ja.wikipedia.org/wiki/ファイル:Sortunix.png "wikilink")  **sort**（ソート）は、[UNIX](../Page/UNIX.md "wikilink")に標準的に存在する[コマンド行](../Page/キャラクタユーザインタフェース.md "wikilink")[プログラムの一種であり](../Page/プログラム_\(コンピュータ\).md "wikilink")、入力の各行を[ソート](../Page/ソート.md "wikilink")された順序で出力するものである。

## 例

  - カレント[ディレクトリ](../Page/ディレクトリ.md "wikilink")にあるファイルリストをファイルサイズ順でソート

<!-- end list -->

``` console
$ ls -s | sort -n
  96 Nov1.txt
 128 _arch_backup.lst
 128 _arch_backup.lst.tmp
1708 NMON
```

  - 名簿（電話帳）をアルファベット順にソート

<!-- end list -->

``` console
$ cat phonebook
Smith, Brett     555-4321
Doe, John        555-1234
Doe, Jane        555-3214
Avery, Cory      555-4321
Fogarty, Suzie   555-2314

$ sort phonebook
Avery, Cory      555-4321
Doe, Jane        555-3214
Doe, John        555-1234
Fogarty, Suzie   555-2314
Smith, Brett     555-4321
```

  - 数値をキーとしたソートは **-n** オプションをつけることで可能となる。

<!-- end list -->

``` console
$ du /bin/* | sort -n
    4       /bin/domainname
  24      /bin/ls
 102     /bin/sh
 304     /bin/csh
```

  -
    古いバージョンの sort では、**+1** オプションを付けると、第二カラムのデータを使ってソートする（**+2** では第三カラム）。これは現在ではサポートされていないが、その代替として **-k** オプションを同じ目的に使用できる。次の例は **-n** と "**-k 2**"（第二カラムを指定）を同時に指定している。

<!-- end list -->

``` console
$ cat zipcode
Adam  12345
Bob   34567
Joe   56789
Sam   45678
Wendy 23456

$ sort -nk 2 zipcode
Adam  12345
Wendy 23456
Bob   34567
Sam   45678
Joe   56789
```

  - 逆順でのソートには **-r** オプションを使う。

<!-- end list -->

``` console
$ sort -nrk 2 zipcode
Joe   56789
Sam   45678
Bob   34567
Wendy 23456
Adam  12345
```

## 外部リンク

  - [Manpage of SORT](https://linuxjm.osdn.jp/html/gnumaniak/man1/sort.1.html) JM Project
  - [sort(1)](https://docs.oracle.com/cd/E19253-01/819-1210/6n3j74jtp/index.html) man page（SunOS リファレンスマニュアル）
  - [sort(1)](https://nixdoc.net/man-pages/HP-UX/man1/sort.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")