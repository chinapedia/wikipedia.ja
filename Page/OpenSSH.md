> この記事は[OpenSSH](https://ja.wikipedia.org/wiki/OpenSSH)から翻訳されています。


**OpenSSH**とは、[SSHプロトコルを利用するためのソフトウェアで](../Page/Secure_Shell.md "wikilink")、SSHサーバおよびSSHクライアントを含む。OpenSSHは、[OpenBSD](../Page/OpenBSD.md "wikilink")プロジェクトにより開発が行われ、[BSDライセンス](../Page/BSDライセンス.md "wikilink")で公開されている。オリジナルのSSH実装である**SSH Tectia**など、SSHには他にいくつかの実装があるが、[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")の時点で\[1\]。

## 歴史

オリジナルのSSHは、Tatu Ylönenにより[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")に開発され、はじめフリーで公開された。しかし、同年12月には、SSH社 (SSH Communications Security) が設立され、[プロプライエタリ・ソフトウェア](../Page/プロプライエタリ・ソフトウェア.md "wikilink")となった。OpenBSDの開発チームは、オリジナルのSSHの最後のフリーなバージョンであるssh 1.2.12をもとに改良を加え、[1999年](../Page/1999年.md "wikilink")12月に、OpenSSHの最初のバージョンであるOpenSSH 1.2.2を、OpenBSD 2.6とともに発表した。

最初のOpenSSHの発表後、OpenBSDチームはOpenSSHの他のオペレーティングシステムへのポーティングと、プロトコルバージョン2への対応を行うことにした。SSHの初期のプロトコルであるバージョン1には脆弱性や制限があり、対応策としてSSH社は、[1996年](../Page/1996年.md "wikilink")にバージョン1と互換性のないプロトコルバージョン2を発表し、これを実装した製品を[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に発売していた。しかし、それまでの製品より機能が劣り、ライセンスの制限も厳しかったためバージョン2の普及はなかなか進んでいなかった。OpenSSHは、[2000年](../Page/2000年.md "wikilink")7月にバージョン1とバージョン2に対応したOpenSSH 2.0を、OpenBSD 2.7のリリースとともに発表した。このリリースによりOpenSSHは爆発的に普及し、スタンダードの地位を獲得した。

## 開発プロセス

OpenSSHの開発は、まずOpenBSD上で安全・堅牢なプログラムを開発し、他のシステムでの実装はOpenBSD版を基にオペレーティングシステム依存部分のみを移植するという方針で行われている。移植版には、区別のためバージョン番号に、**Portable release** を意味する "p(数字)" が付けられる。

## 脚注

## 参考文献

  - 『実用SSH 第2版 - セキュアシェル徹底活用ガイド』（[オライリー](../Page/オライリーメディア.md "wikilink") ISBN 978-4-87311-287-9 2006年）

## 関連項目

  - [SFTP](https://ja.wikipedia.org/wiki/SFTP "wikilink")
  - [TCP Wrapper](../Page/TCP_Wrapper.md "wikilink")

## 外部リンク

  -
[Category:Secure_Shell](https://ja.wikipedia.org/wiki/Category:Secure_Shell "wikilink") [Category:暗号ソフトウェア](https://ja.wikipedia.org/wiki/Category:暗号ソフトウェア "wikilink") [Category:OpenBSD](https://ja.wikipedia.org/wiki/Category:OpenBSD "wikilink") [Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.