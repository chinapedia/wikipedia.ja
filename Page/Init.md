> この記事は[Init](https://ja.wikipedia.org/wiki/Init)から翻訳されています。


**init**は、[UNIX](../Page/UNIX.md "wikilink")および[Unix系](../Page/Unix系.md "wikilink")システムの[プログラムのひとつであり](../Page/プログラム_\(コンピュータ\).md "wikilink")、他の全ての[プロセス](../Page/プロセス.md "wikilink")を起動する役目を持つ。[デーモンとして動作し](https://ja.wikipedia.org/wiki/デーモン_\(ソフトウェア\) "wikilink")、一般に[PID](https://ja.wikipedia.org/wiki/プロセス識別子 "wikilink") 1 を付与される。[ブート](https://ja.wikipedia.org/wiki/ブート "wikilink")ローダが[カーネル](../Page/カーネル.md "wikilink")を起動し、カーネルがinitを起動する。代替手段を用意せずにinitを削除すると、次回のリブート時にシステムは[カーネルパニック](https://ja.wikipedia.org/wiki/カーネルパニック "wikilink")に陥る可能性がある。

init の機能は[BSD](../Page/BSD.md "wikilink")系と[System V系では大きく異なるため](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")、ユーザーは自分のシステムがどちらのバージョンを使っているかをマニュアルで調べる必要がある。多くの[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")で使われていたinitはSystem Vと互換性がある。[Slackware](../Page/Slackware.md "wikilink")のようなLinuxディストリビューションではBSD系のinitを使っていた。[Gentoo Linuxなどでは独自のinitを使用していた](../Page/Gentoo_Linux.md "wikilink")。ISO/IEC 23360-1:2006の国際規格\[1\]になった[Linux Standard Baseではinitを定義している](../Page/Linux_Standard_Base.md "wikilink")\[2\]。

他にもいくつかinitの設計上の限界に対処した代替として、[systemd](https://ja.wikipedia.org/wiki/systemd "wikilink")や[Upstart](../Page/Upstart.md "wikilink")があり、[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")\[3\]\[4\]や他のLinuxディストリビューションで採用している\[5\]\[6\]。

## System V系のinit

System Vのinitは、`/etc/inittab`ファイル内の`:initdefault:`エントリを調べて既定の[ランレベル](https://ja.wikipedia.org/wiki/ランレベル "wikilink")があるかチェックする。既定のランレベルがない場合、コンソール端末に何らかの表示がなされるので、ユーザは手でランレベルを入力しなければならない。

  - *利点:* 柔軟で拡張性がある。
  - *欠点:* 複雑である。

### ランレベル

[System Vの](https://ja.wikipedia.org/wiki/UNIX_System_V "wikilink")[ランレベル](https://ja.wikipedia.org/wiki/ランレベル "wikilink") (runlevel) は、マシンの状態を実行するプロセス群によって分類したものである。一般に 0\~6とSまたはsという8段階のランレベルがある。Sとsは同じランレベルの別名である。この8段階のうち、以下の3つは予約されたランレベルである。

  -
    0\. 停止 (Halt)
    1\. シングルユーザーモード
    6\. 再起動 (Reboot)

これら以外のランレベルは、各システムによってそれぞれ意味が異なる。一般に、`/etc/inittab`ファイルで、各ランレベルで何をするかを定義している。

### デフォルトのランレベル

| OS                                                                                                                         | デフォルトのランレベル                            |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| [AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")                                                                        | 2                                      |
| [CentOS](https://ja.wikipedia.org/wiki/CentOS "wikilink")                                                                  | 3（コンソール/サーバ）または 5（グラフィカル/デスクトップ）\[7\]  |
| [Debian](../Page/Debian.md "wikilink")                                                                                     | 2\[8\]                                 |
| [Gentoo Linux](../Page/Gentoo_Linux.md "wikilink")                                                                         | 3\[9\]                                 |
| [HP-UX](../Page/HP-UX.md "wikilink")                                                                                       | 3（コンソール/サーバ/マルチユーザ）または 4（グラフィカル）       |
| [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")                                                                    | 3                                      |
| [Mandriva Linux](https://ja.wikipedia.org/wiki/Mandriva_Linux "wikilink")                                                  | 3（コンソール/サーバ）または 5（グラフィカル/デスクトップ）       |
| [Red Hat Linux](../Page/Red_Hat_Linux.md "wikilink") / [Fedora Core](https://ja.wikipedia.org/wiki/Fedora_Core "wikilink") | 3（コンソール/サーバ）または 5（グラフィカル/デスクトップ）\[10\] |
| [Slackware](../Page/Slackware.md "wikilink")                                                                               | 3                                      |
| [Solaris](../Page/Solaris.md "wikilink")                                                                                   | 3\[11\]                                |
| [SUSE Linux](../Page/SUSE.md "wikilink")                                                                                   | 3（コンソール/サーバ）または 5（グラフィカル/デスクトップ）\[12\] |
| [Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")                                                                  | 2\[13\]                                |

上記表でデフォルトのランレベルを5としているLinuxディストリビューションでは、5というランレベルはマルチユーザーのグラフィカル環境（[X Window Systemと](../Page/X_Window_System.md "wikilink")、その上で[ディスプレイマネージャ](https://ja.wikipedia.org/wiki/ディスプレイマネージャ "wikilink")が起動される）である。しかし、[Solaris](../Page/Solaris.md "wikilink")では、ランレベル5はシャットダウンと電源オフの自動化のために予約されている。

現在のランレベルは以下のようなコマンドを使って調べることができる。

  -
    `$ runlevel`
    ` $  `[`who`](https://ja.wikipedia.org/wiki/Who_\(UNIX\) "wikilink")`  -r `

通常、ランレベルは[rootが](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")`telinit`コマンドまたは`init`コマンドを実行することで変更することができる。デフォルトのランレベルは`/etc/inittab`ファイルの`:initdefault:`エントリにある。

## BSD系のinit

[BSD](../Page/BSD.md "wikilink")のinitは、`/etc/rc`にある初期化用[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")を実行し、`/etc/ttys`の制御下にあるテキストベース端末用の[getty](https://ja.wikipedia.org/wiki/getty "wikilink")を起動したり、グラフィックス端末用に[Xなどを起動したりする](../Page/X_Window_System.md "wikilink")。ランレベルという概念は無く、`/etc/rc`ファイルでinit の動作を決定している。

  - *利点:* 手で変更・修正するのが容易である。
  - *欠点:* ブート時に[サードパーティー](https://ja.wikipedia.org/wiki/サードパーティー "wikilink")のパッケージの初期化スクリプトを実行する必要がある場合、上記のスクリプトのいずれかを編集する必要があるが、ちょっとした間違いでブート不可能な状態になってしまう。

[BSDの子孫](../Page/BSDの子孫.md "wikilink")では、伝統的に`/etc/rc.local`ファイルをブート処理の最後近くに実行することでブート不可となる危険性を和らげていた。

[NetBSD](../Page/NetBSD.md "wikilink") 1.5では完全にモジュール化したシステムを導入し、それが[FreeBSD](../Page/FreeBSD.md "wikilink") 5.0およびそれ以降にも移植されている。このシステムは、`/etc/rc.d` ディレクトリ配下にあるスクリプト群を実行するものである。System Vでのスクリプト実行順は各スクリプトのファイル名の順番だが、BSD系では各スクリプトファイルに明示的な依存関係を示すタグを置いている\[14\]。スクリプトの実行順序は、それらタグに基づいて*rcorder*スクリプトが決定する。

## initをスキップする

initはマシンを立ち上げる唯一の方法ではない。最近の[ブートローダ](https://ja.wikipedia.org/wiki/ブートローダ "wikilink")（たとえば[LILO](../Page/LILO.md "wikilink")や[GRUB](../Page/GNU_GRUB.md "wikilink")）では、カーネルが初期化の最後に何を起動するかを指定することができる（既定値はもちろん`/sbin/init`である）。これは、ブートローダのプロンプトに`init=/foo/bar`などと打ち込むことで実現される。これは直接[シェル](../Page/シェル.md "wikilink")（[Bash](https://ja.wikipedia.org/wiki/Bash "wikilink")や[zsh](https://ja.wikipedia.org/wiki/zsh "wikilink")）を使いたい場合に便利な機能である。たとえば、`init=/bin/bash`を使えば、シェルが使える状態で立ち上がり、パスワードを入力する必要もない。システム管理者がこれを安全でないと判断する場合は、ブートローダのパスワードを設定すればよい。

BSD系では、ブート処理は途中で割り込むことができ、`boot -s`コマンドでシングルユーザーモードで立ち上げることができる。シングルユーザーモードは技術的にはinitをスキップするわけではない。`/sbin/init`はやはり実行されるが、この場合`exec()`に指定するプログラムのパスを聞いてくる（デフォルトでは`/bin/sh`）。ブートが行われている端末が`/etc/ttys`ファイルで "insecure" とされている場合（システムによっては現在の "securelevel" も関係する）、initは最初にrootのパスワードを聞いてくる（あるいは、ユーザーが`CTRL+D`を押下すると通常のマルチユーザー立ち上げに戻る）。このプログラムが終了させられた場合、カーネルはマルチユーザーモードでの再立ち上げを行う。通常動作中にマルチユーザーモードからシングルユーザーモードへ移行させようとしたときも同様のことが起きる。カーネルのブート処理後、initを起動できない場合はパニックが発生して、システムは利用できなくなる。initのパス指定方法は[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) によって異なる（NetBSD では`boot -a`、FreeBSD では`init_path`というローダー変数である）。

## initの代替

initに比較して何らかの長所を持つ代替がいくつも開発されてきた。

  - [GoboLinux](https://ja.wikipedia.org/wiki/GoboLinux "wikilink")のBootScripts

  - [eINIT](https://ja.wikipedia.org/wiki/eINIT "wikilink") - initを完全に置き換えるものであり、非同期なプロセス開始処理が特徴。シェルスクリプトを全く使わない方法をとることも可能。

  - [Initng](../Page/Initng.md "wikilink") - initを完全に置き換えるものであり、非同期なプロセス開始処理が特徴。

  - [launchd](https://ja.wikipedia.org/wiki/launchd "wikilink") — [macOS](https://ja.wikipedia.org/wiki/macOS "wikilink") （[Mac OS X v10.4以降](../Page/Mac_OS_X_v10.4.md "wikilink")）でのプロセス開始処理（[Mac OS X v10.3以前はinitを使用](../Page/Mac_OS_X_v10.3.md "wikilink")）。古い`rc.local`はSystemStarterで扱う。

  - Mudur - というLinuxディストリビューションで採用している[Python](../Page/Python.md "wikilink")で書かれたinit代替で、非同期なプロセス起動が可能\[15\]。

  - \- [Gentoo Linuxのデフォルトのinitシステム](../Page/Gentoo_Linux.md "wikilink")

  - \- [Solaris](../Page/Solaris.md "wikilink") 10から導入されたinitの置換/再設計

  - [systemd](https://ja.wikipedia.org/wiki/systemd "wikilink") - [Fedora](../Page/Fedora.md "wikilink") 15からデフォルトで使用しているinitの代替。サービスを並列に起動でき、シェルのオーバーヘッドを低減している。

  - [Upstart](../Page/Upstart.md "wikilink") - initを完全に置き換えるものであり、非同期なプロセス開始処理が特徴。[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")が起源。

## 脚注

## 関連項目

  - [pidof](https://ja.wikipedia.org/wiki/pidof "wikilink")

## 外部リンク

  - [man pages for init](http://man.he.net/man8/init)
  - [FreeBSD init man page](http://www.freebsd.org/cgi/man.cgi?query=init&apropos=0&sektion=0&manpath=FreeBSD+6.2-stable&format=html)
  - [Paper summarizing Unix init schemes](http://arxiv.org/abs/0706.2748)
  - [runit](http://smarden.org/runit/index.html)
  - [minit](http://www.fefe.de/minit/)
  - [rc.d](http://www.netbsd.org/guide/en/chap-rc.html)
  - [busybox](http://www.busybox.net/downloads/BusyBox.html#item_init)

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink")

1.  ISO/IEC 23360-1:2006 Linux Standard Base (LSB) core specification 3.1 Part 1: Generic specification <https://www.iso.org/standard/43781.html>
2.  Linux Standard Base(LSB) 22.2. Init Script Actions <https://refspecs.linuxfoundation.org/lsb.shtml>
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.