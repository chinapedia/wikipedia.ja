> この記事は[Xディスプレイマネージャ](https://ja.wikipedia.org/wiki/Xディスプレイマネージャ)から翻訳されています。


**Xディスプレイマネージャ**（）は、[X Window System](../Page/X_Window_System.md "wikilink") 上のプログラムの1つで、ローカルあるいはリモートの[Xサーバ](https://ja.wikipedia.org/wiki/Xサーバ "wikilink")でセッションを開始させる機能を持つ。単に**ディスプレイマネージャ**とも呼ばれる。

[thumbのログイン画面](https://ja.wikipedia.org/wiki/画像:Xdm_Screenshot.png "wikilink")\]\]

ディスプレイマネージャは、ユーザに対してログイン画面を提示し、ユーザ名と[パスワード](../Page/パスワード.md "wikilink")を入力可能である。ユーザが正しく入力するとセッションが開始される。

ディスプレイマネージャがユーザが操作する[コンピュータ](../Page/コンピュータ.md "wikilink")上で動作する場合、ログイン画面を表示する前にXサーバを起動し、オプションでログアウトの際にもログイン画面を表示する。この場合、ディスプレイマネージャは X Window System において、[テキスト端末での](../Page/端末.md "wikilink") [`init`](https://ja.wikipedia.org/wiki/init "wikilink")、[`getty`](https://ja.wikipedia.org/wiki/getty_\(Unix\) "wikilink")、`login` の役割を果たす。ディスプレイマネージャがリモートのコンピュータで動作する場合、[telnet](https://ja.wikipedia.org/wiki/telnet "wikilink") サーバのように機能して、ユーザ名とパスワードを要求し、リモートセッションを開始させる。

[1988年](../Page/1988年.md "wikilink")10月、X11R3 でディスプレイマネージャが導入された。これは当時登場し始めていた[X端末](../Page/X端末.md "wikilink")をサポートするためであった。多くのディスプレイマネージャがスタンドアロン型のXの動作する[ワークステーション](../Page/ワークステーション.md "wikilink")でも、グラフィカルなログイン画面を提供するのに使われている。[1989年](../Page/1989年.md "wikilink")12月、X11R4 では X11R3 での実装上の問題を解決すべく **X Display Manager Control Protocol**（**XDMCP**）が導入された。

## ローカル/リモートの画面管理

ディスプレイマネージャは、ユーザが直接操作するコンピュータ上で動作する場合もあるし、リモートのコンピュータで動作する場合もある。前者の場合、ディスプレイマネージャは1つ以上のXサーバを起動し、最初にログイン画面を表示し（オプションで）ログアウトの度にログイン画面を表示する。後者では、ディスプレイマネージャは XDMCP プロトコルに従って動作する。

[thumb](https://ja.wikipedia.org/wiki/画像:Xserver_and_display_manager.svg "wikilink") XDMCP プロトコルは、Xサーバの自律的起動とディスプレイマネージャへの接続を指示する。X Window System では、Xサーバはディスプレイ（画面）と入力機器のあるコンピュータ上で動作する。サーバは XDMCP プロトコルを使って他のコンピュータ上のディスプレイマネージャと接続でき、セッション開始を要求できる。この場合、Xサーバはグラフィカルな [telnet](https://ja.wikipedia.org/wiki/telnet "wikilink") クライアントのように振る舞い、ディスプレイマネージャが telnet サーバのように振舞う。ユーザはディスプレイマネージャが動作しているコンピュータ上でプログラムを起動でき、その入出力はXサーバ経由でユーザが直接操作しているコンピュータが行う。

Xサーバは特定のディスプレイマネージャに接続するよう設定することもできるし、接続可能なXディスレプイマネージャの動作しているホストの一覧を表示してユーザが選択するようにもできる。後者の場合、**XDMCP Chooser** プログラムを使い、次のいずれかの状態で機能する。

1.  事前に定義されたホストとそのネットワークアドレスの一覧を表示する。
2.  ブロードキャストが届く範囲（ローカルな[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")サブネット）でXDMCPサーバの動作しているホストの一覧を表示する。

ユーザがこのホスト一覧からホストを選択すると、ローカルマシンで動作しているXサーバが選択されたリモートコンピュータのXディスプレイマネージャと接続を行う。

## X Display Manager Control Protocol

X Display Manager Control Protocol（XDMCP）は[UDP](../Page/User_Datagram_Protocol.md "wikilink")[ポート](../Page/ポート_\(コンピュータネットワーク\).md "wikilink") 177 を使う。Xサーバはディスプレイマネージャに対して `Query` パケットを送信することでセッション開始を要求する。そのディスプレイマネージャがそのXサーバにアクセスを許可する場合、`Willing` パケットで応答する。Xサーバは `Broadcast Query` パケットや `IndirectQuery` パケットでセッション開始を要求することもできる。

ディスプレイマネージャはサーバに対して自身を認証しなければならない。そのため、Xサーバはディスプレイマネージャに `Request` パケットを送信し、応答として `Accept` パケットを受信する。`Accept` パケットにXサーバが期待した内容が記されていれば、ディスプレイマネージャが認証されたことになる。正しい応答を行うには、例えはディスプレイマネージャが[秘密鍵にアクセスできなければならない](../Page/鍵_\(暗号\).md "wikilink")。認証が成功するとXサーバはディスプレイマネージャにそれを伝えるため `Manage` パケットを送る。すると、ディスプレイマネージャは、そのXサーバに対してXクライアントとして接続し、ログイン画面を表示する。

セッションの間、サーバは一定間隔で `KeepAlive` パケットをディスプレイマネージャに送信できる。ディスプレイマネージャがそれに対してある時間内に `Alive` パケットで応答できない場合、Xサーバはディスプレイマネージャが動作できない状態であると推定し、接続を終了させることもできる。

XDMCP の問題として [telnet](https://ja.wikipedia.org/wiki/telnet "wikilink") とも似た問題がある。それは、認証処理のパケットが暗号化されておらず、悪意ある者がそれを見て攻撃できる点である。そのため、X の通信には[SSHトンネルを使う方が安全である](../Page/Secure_Shell.md "wikilink")[1](http://www.gnome.org/projects/gdm/docs/2.14/security.html)。

## 歴史

XDM（[X Window Display Manager](../Page/X_Window_Display_Manager.md "wikilink")）は X11R3 で登場した。この版にはいくつかの問題があり、特に有名な問題としては、X端末の電源を入れなおしたときに発生した。X11R3 では、XDM は `Xservers` ファイルにあるX端末だけを認識し、しかもXDMが起動したときだけそのファイルを読み込むようになっていた。従って、ユーザーがX端末の電源を入れなおしたときは、[システムアドミニストレータ](../Page/システムアドミニストレータ.md "wikilink")が XDM に SIGHUP [シグナルを送り](../Page/シグナル_\(Unix\).md "wikilink")、`Xservers` を読み直させなければならなかった。

XDMCP は X11R4（[1989年](../Page/1989年.md "wikilink")12月）で導入された。XDMCP では、Xサーバがディスプレイマネージャに対して能動的に接続を要求しなければならない。したがって、XDMCP を使ったXサーバの場合、`Xservers` に記述しておく必要がない。

## 利用可能なディスプレイマネージャ

[X Window System](../Page/X_Window_System.md "wikilink") の標準ディスプレイマネージャとしては、[XDM](../Page/X_Window_Display_Manager.md "wikilink") がある。

他にもフリーなものも商用製品としても、様々なXディスプレイマネージャが開発されており、単なる画面管理以上の機能を持つものが多い。

  - [GNOME ディスプレイマネージャー](https://ja.wikipedia.org/wiki/GNOME_ディスプレイマネージャー "wikilink")
  - [LightDM](https://ja.wikipedia.org/wiki/LightDM "wikilink") - Ubuntuにて標準採用
  - [KDM](https://ja.wikipedia.org/wiki/KDEディスプレイマネージャ "wikilink") ([KDE](../Page/KDE.md "wikilink")) - [ウィンドウマネージャ](../Page/ウィンドウマネージャ.md "wikilink")や[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")をログイン時にグラフィカルに選択可能
  - [SDDM](https://ja.wikipedia.org/wiki/SDDM "wikilink") - [LXQt](https://ja.wikipedia.org/wiki/LXQt "wikilink")にて標準採用
  - dtlogin - [CDEの一部](../Page/Common_Desktop_Environment.md "wikilink")
  - [WINGs Display Manager](http://voins.program.ru/wdm/index.html.en) - [Window Maker](../Page/Window_Maker.md "wikilink") のウィジェットセット WINGs を使用
  - [Entrance](http://xcomputerman.com/pages/entrance.html) - [Enlightenment](https://ja.wikipedia.org/wiki/Enlightenment "wikilink") v.17 のアーキテクチャを使用
  - 独立したディスプレイマネージャ
      - [SLiM](http://slim.berlios.de/) - デスクトップ環境と独立したディスプレイマネージャ
      - Nodm - デスクトップ環境と独立したディスプレイマネージャ

## 関連項目

  - [X Window System プロトコルとアーキテクチャ](https://ja.wikipedia.org/wiki/X_Window_System_プロトコルとアーキテクチャ "wikilink")

## 参考文献

  - [XDMCP documentation](http://cvs.freedesktop.org/*checkout*/xorg/xc/doc/hardcopy/XDMCP/xdmcp.PS.gz) （[PostScript](../Page/PostScript.md "wikilink")形式をgzipで圧縮したファイル）、[freedesktop.org](https://ja.wikipedia.org/wiki/freedesktop.org "wikilink") の [X.Org](../Page/X.Org_Foundation.md "wikilink") CVS リポジトリより

  -
  - Linda Mui and Eric Pearce, *X Window System Volume 8: X Window System Administrator's Guide for X11 Release 4 and Release 5, 3rd edition* (O'Reilly and Associates, July 1993; softcover ISBN 0-937175-83-8)

## 外部リンク

  - [Linux XDMCP HOWTO](http://www.tldp.org/HOWTO/XDMCP-HOWTO/index.html)
  - [Taming The X Display Manager](http://www.rru.com/~meo/pubsntalks/xrj/xdm.html)
  - [The X Display Manager](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/x-xdm.html), [FreeBSD Handbook](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/) より

[Category:Xディスプレイマネージャ](https://ja.wikipedia.org/wiki/Category:Xディスプレイマネージャ "wikilink") [Category:X_Window_System](https://ja.wikipedia.org/wiki/Category:X_Window_System "wikilink")