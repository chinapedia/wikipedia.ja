> この記事は[FreeBSD jail](https://ja.wikipedia.org/wiki/FreeBSD_jail)から翻訳されています。


**FreeBSD jail**はOSレベル[仮想化](https://ja.wikipedia.org/wiki/仮想化 "wikilink")機構実装の一つである。jailを使うと、管理者が[FreeBSD](../Page/FreeBSD.md "wikilink")ベースの計算機システムをjailと呼ばれる独立した小さなシステムに分割できるようになる。

FreeBSD jailは、[レンタルサーバ業者が業者の提供するサービスと顧客のサービスとを分離するのによく使われる](../Page/ホスティングサーバ.md "wikilink")。 このように分離することで安全性を確保し、管理の手間を軽減できる。 サーバ[デーモンの設定レベルで分離するのと違い](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")、jailからは自分に割り当てられた[ファイルシステム](../Page/ファイルシステム.md "wikilink")およびプロセス空間しか扱えないようになっている。

## jailの利点

[FreeBSD](../Page/FreeBSD.md "wikilink") jailには主に次の3つの利点がある。

1.  [仮想化](https://ja.wikipedia.org/wiki/仮想化 "wikilink"): 各jailはホストマシン上で動く[仮想機械](../Page/仮想機械.md "wikilink")であり、独自の[ファイルシステム](../Page/ファイルシステム.md "wikilink")や[プロセス空間](https://ja.wikipedia.org/wiki/プロセス空間 "wikilink")、[ユーザーアカウント](https://ja.wikipedia.org/wiki/ユーザーアカウント "wikilink")を持つ。jailの中のプロセスからは実際のシステムなのかjailの中なのかはほぼ区別できない。
2.  [安全性](https://ja.wikipedia.org/wiki/安全性 "wikilink"): 各jailは他のjailにアクセスできないようになっており、[安全性](https://ja.wikipedia.org/wiki/安全性 "wikilink")が高まっている。
3.  [権限委譲](https://ja.wikipedia.org/wiki/権限委譲 "wikilink")の簡素化: 管理者権限の[スコープ](https://ja.wikipedia.org/wiki/スコープ "wikilink")がjail内に制限されているため、システムの管理者は本来管理者権限が必要な仕事を、計算機全体を操作する権限を渡すことなく行わせることが出来る。

jailのやり方は従来の[Unix](https://ja.wikipedia.org/wiki/Unix "wikilink")でプロセスのスコープを制限するのに使われる[chroot](https://ja.wikipedia.org/wiki/chroot "wikilink") jailに似ている。FreeBSD jailはこれを強化したもので、各プロセスは他のjailで動いているプロセスに干渉したり、[raw socketや](https://ja.wikipedia.org/wiki/raw_socket "wikilink")[divert socket](https://ja.wikipedia.org/wiki/divert_socket "wikilink")、[routing socketを操作したりできないよう](https://ja.wikipedia.org/wiki/routing_socket "wikilink")、特別な[カーネル](../Page/カーネル.md "wikilink")構造体を用いて管理してある。

`jail(8)`ユーザーランドコマンドと`jail(2)`[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")はFreeBSD 4.0で登場した。jailの取り扱いを簡単にする新しいユーザーランドコマンド (たとえば、jailの一覧を出す`jls(8)`)やシステムコール (たとえば、jailに新しいプロセスを追加する`jail_attach(2)`)はFreeBSD 5.1から追加された。

## jailの作り方

[FreeBSD](../Page/FreeBSD.md "wikilink") jailの利用は次のように簡単に行える。

1.  `/usr/jail`のようにjailの中でrootディレクトリ (つまり、/) となるディレクトリを作る。
2.  jailの中で動かすプログラムやファイルを投入する (典型的には、`/usr/jail/bin`にシェルを置いたり、procfsを`/usr/jail/procfs`にマウントしたりする)。`jail(8)`の[オンラインマニュアル](https://ja.wikipedia.org/wiki/オンラインマニュアル "wikilink")には、[`make``   ``world`](https://ja.wikipedia.org/wiki/make_world "wikilink")`  DESTDIR=/usr/jail `と[`make``   ``distribution`](https://ja.wikipedia.org/wiki/make_distribution "wikilink")`  DESTDIR=/usr/jail `でこの作業を行うことが出来ると書いてあるが、必ずしもこの方法をとる必要はない。
3.  `/usr/jail/dev`にdevfsをマウントする。([デバイスノード](https://ja.wikipedia.org/wiki/デバイスノード "wikilink")無しでも動作するが、非常に制限が強い)
4.  最後に、jailコマンドでjail内の[`sh`](https://ja.wikipedia.org/wiki/sh "wikilink")を使って`/etc/rc` [init](https://ja.wikipedia.org/wiki/init "wikilink")[スクリプトを](../Page/シェルスクリプト.md "wikilink")"仮想的に"起動する (例 `jail /usr/jail hostname 10.0.0.22 /bin/sh /etc/rc`)。

こうすることで、jailのコンテキストでいくつかの[プロセス](../Page/プロセス.md "wikilink")が実行される。そして、中で起動したプロセスはjailの中のプロセスの操作しかできず、jailのルートファイルシステムとして指定されたファイルシステム (ここでは、`/usr/jail`) の外にあるファイルをアクセスできなくなる。

jailを使い始めるときは`jail(8)`のオンラインマニュアルが参考になる。

## 同様の技術

OSレベルの仮想化技術にはこのほかに[OpenVZ](https://ja.wikipedia.org/wiki/OpenVZ "wikilink")/[Virtuozzo](https://ja.wikipedia.org/wiki/Virtuozzo "wikilink"), [Linux-VServer](https://ja.wikipedia.org/wiki/Linux-VServer "wikilink"), [Solaris Containers](https://ja.wikipedia.org/wiki/Solaris_Containers "wikilink"), [FreeVPS](https://ja.wikipedia.org/wiki/FreeVPS "wikilink"), [LXC](https://ja.wikipedia.org/wiki/LXC "wikilink")がある。

## 外部リンク

  - [Jails: Confining the omnipotent root](http://phk.freebsd.dk/pubs/sane2000-jail.pdf)
  - [jail(8) man page](http://www.freebsd.org/cgi/man.cgi?query=jail&format=html)
  - [FreeBSD jails](http://www.onlamp.com/pub/a/bsd/2003/09/04/jails.html) at ONLamp
  - [A jail administration framework](http://erdgeist.org/arts/software/ezjail/) ezjail
  - [Jail on FreeBSD 6](http://www.freebsddiary.org/jail-6.php)
  - [FreeBSD Handbook: Jails](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/jails.html)

[Category:FreeBSD](https://ja.wikipedia.org/wiki/Category:FreeBSD "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")