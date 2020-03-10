> この記事は[Stand-alone shell](https://ja.wikipedia.org/wiki/Stand-alone_shell)から翻訳されています。


**Stand-alone shell**（**sash**）は、[UNIX](../Page/UNIX.md "wikilink")のシェルで、システムの復旧に用いられることを考えて設計されている。

sashのビルトインコマンドは、全てのライブラリが[静的リンク](https://ja.wikipedia.org/wiki/静的リンク "wikilink")されており、他の多くの[Linux](../Page/Linux.md "wikilink")におけるシェルとは違って、外部ライブラリへの依存なしに基本的なUNIXコマンドを実行することができる。例としては、cpは、libc.soやld-linuxを必要とする（[GNU Core UtilitiesをLinuxでビルドした場合](../Page/GNU_Core_Utilities.md "wikilink")）が、これはCore Utilitiesのcpは、これらのライブラリに問題があると動作しない。しかしながら、sashにおいては、ビルトインコマンドであるcpは影響を受けない。

Sashにおいて利用できるビルトインのUNIXコマンドには次のようなものがある\[1\]。

  -
    [`ar`](https://ja.wikipedia.org/wiki/ar_\(Unix\) "wikilink"), [`chattr`](https://ja.wikipedia.org/wiki/chattr "wikilink"), [`chgrp`](https://ja.wikipedia.org/wiki/chgrp "wikilink"), [`chmod`](https://ja.wikipedia.org/wiki/chmod "wikilink"), [`chown`](https://ja.wikipedia.org/wiki/chown "wikilink"), [`cmp`](https://ja.wikipedia.org/wiki/cmp_\(Unix\) "wikilink"), [`cp`](https://ja.wikipedia.org/wiki/cp_\(Unix\) "wikilink"), [`dd`](https://ja.wikipedia.org/wiki/dd_\(Unix\) "wikilink"), [`echo`](https://ja.wikipedia.org/wiki/echo_\(command\) "wikilink"), [`ed`](https://ja.wikipedia.org/wiki/ed_\(text_editor\) "wikilink"), [`exec`](https://ja.wikipedia.org/wiki/Exec_\(operating_system\) "wikilink"), [`grep`](https://ja.wikipedia.org/wiki/grep "wikilink"), [`file`](https://ja.wikipedia.org/wiki/file_\(command\) "wikilink"), [`find`](https://ja.wikipedia.org/wiki/Find_\(Unix\) "wikilink"), [`gunzip`](https://ja.wikipedia.org/wiki/gunzip "wikilink"), [`gzip`](https://ja.wikipedia.org/wiki/gzip "wikilink"), [`kill`](https://ja.wikipedia.org/wiki/kill_\(command\) "wikilink"), [`losetup`](https://ja.wikipedia.org/wiki/losetup "wikilink"), [`ln`](https://ja.wikipedia.org/wiki/ln_\(Unix\) "wikilink"), [`ls`](https://ja.wikipedia.org/wiki/ls "wikilink"), [`lsattr`](https://ja.wikipedia.org/wiki/chattr#lsattr_description "wikilink"), [`mkdir`](https://ja.wikipedia.org/wiki/mkdir "wikilink"), [`mknod`](https://ja.wikipedia.org/wiki/mknod "wikilink"), [`rmdir`](https://ja.wikipedia.org/wiki/rmdir "wikilink"), [`sum`](https://ja.wikipedia.org/wiki/Sum_\(Unix\) "wikilink"), [`sync`](https://ja.wikipedia.org/wiki/sync_\(Unix\) "wikilink"), [`tar`](https://ja.wikipedia.org/wiki/Tar_\(computing\) "wikilink"), [`touch`](https://ja.wikipedia.org/wiki/touch_\(command\) "wikilink"), [`umount`](https://ja.wikipedia.org/wiki/umount "wikilink"), `where`

また、Sashは、[Android](../Page/Android.md "wikilink")において動作するターミナルインターフェースとしてポートされている\[2\]。

## sash-plus-patches

sash-plus-pathesは、sashで用いることのできるパッチの集合体である\[3\]。これは、sashでchroot, pivot root, losetupなどのコマンドを利用可能にしている。しかしながら、これらの機能はより新しいバージョンのsashで利用することができる。これらのコマンドは、[initrd](https://ja.wikipedia.org/wiki/initrd "wikilink")環境でsashを利用する際に特に便利である。

## 関連項目

  - [BusyBox](https://ja.wikipedia.org/wiki/BusyBox "wikilink")
  - [Toybox](https://ja.wikipedia.org/wiki/Toybox "wikilink")

## 脚注

## 外部リンク

  - [sashのウェブサイト](http://members.tip.net.au/~dbell/)

[Category:Unixシェル](https://ja.wikipedia.org/wiki/Category:Unixシェル "wikilink")

1.  [sash man page](http://manpages.ubuntu.com/manpages/trusty/man1/sash.1.html)
2.  [Standalone-Shell(sash) specifically compiled for the Android Operating System.](https://github.com/Master-Console/masterterm-utilities/tree/master/sash)
3.  [sash-plus-patches](http://www.baiti.net/sash/)