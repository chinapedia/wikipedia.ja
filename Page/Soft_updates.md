> この記事は[Soft updates](https://ja.wikipedia.org/wiki/Soft_updates)から翻訳されています。


**Soft updates**とは非同期書き込み中に不意に計算機が止まった場合でも[ファイルシステム](../Page/ファイルシステム.md "wikilink")の一貫性を保つための技術である。

## 概要

Soft updates(Soft dependenciesとも言われる)とは、非同期書き込みを行っている際に突然電源切断が起きても、[ファイルシステム](../Page/ファイルシステム.md "wikilink")の一貫性を保つための技術である。[ジャーナリングファイルシステム](../Page/ジャーナリングファイルシステム.md "wikilink")と同様、ファイルシステムの一貫性を保証する技術であり、データの喪失が起きないようにする技術ではない。

ファイルシステムの一貫性を保証するために、Soft updatesでは[ハードディスク](https://ja.wikipedia.org/wiki/ハードディスク "wikilink")へのデータ書き込みの順序に制限を設けている。一言でまとめると、ハードディスクのハードウェア的に可能ないかなるタイミングでそれ以降の書き込みが中断されても、一貫性が保たれるような順序で書き込みを行う、という方式がsoft updatesである。ジャーナリングと異なり、メタデータなどを保存する別の領域を必要としない。

Soft updatesによってファイルシステムの[inode](https://ja.wikipedia.org/wiki/inode "wikilink")などのメタデータと実際のデータの一貫性が常に保証されるので、突然の電源切断が起きた場合にも[fsck](https://ja.wikipedia.org/wiki/fsck "wikilink")なしに[mountすることができる](https://ja.wikipedia.org/wiki/mount_\(UNIX\) "wikilink")。しかし、実際には未使用なのに使用されているとマークされているページができることがある。これは、Soft updatesでは利用している領域を未使用領域と誤認する状況を避けるようハードディスクへの書き込み制御をするからである。このような誤って使用中と認識された領域を掃除するために[background fsckを行う](https://ja.wikipedia.org/wiki/background_fsck "wikilink")。

問題点として、近年の大容量化したディスクでは、一旦問題が発生するとbackground fsckに長時間が必要となってしまう。FreeBSD 9ではジャーナリングによりこれを解決したJournaled Soft Updatesが導入された。

Soft updatesは最初[FreeBSD](../Page/FreeBSD.md "wikilink")用に[マーシャル・カーク・マキュージック](../Page/マーシャル・カーク・マキュージック.md "wikilink")（Marshall Kirk McKusick）が開発したものだったが、他のいくつかの[BSDの子孫](../Page/BSDの子孫.md "wikilink")でも利用可能である。

## 参考文献

  - McKusick, M. (2002). [Running "fsck" in the Background](http://www.usenix.org/publications/library/proceedings/bsdcon02/mckusick/mckusick_html/index.html)." *Proceedings of the BSDCon 2002.* 55-64.
  - McKusick, M. and Ganger, G. (1999). "[Soft Updates: A Technique for Eliminating Most Synchronous Writes in the Fast Filesystem](http://www.usenix.org/publications/library/proceedings/usenix99/full_papers/mckusick/mckusick.pdf)." *USENIX Annual Technical Conference.* 1-18.
  - Seltzer, M. et al. (2000). "[Journaling Versus Soft Updates: Asynchronous Meta-data Protection in File Systems](http://www.usenix.org/publications/library/proceedings/usenix2000/general/full_papers/seltzer/seltzer_html/index.html)." *USENIX Annual Technical Conference.* 71-84.

## 外部リンク

  - [Information about Soft Updates, Snapshots, and Back-ground Fsck](http://www.mckusick.com/softdep/)
  - [Server File Cache → Storage](http://www.dd.iij4u.or.jp/~okuyamak/Documents/NetworkFileSystem.Tune.4.html#Softupdate)

[Category:OSのファイルシステム](https://ja.wikipedia.org/wiki/Category:OSのファイルシステム "wikilink") [Category:BSD](https://ja.wikipedia.org/wiki/Category:BSD "wikilink")