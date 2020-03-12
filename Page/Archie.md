> この記事は[Archie](https://ja.wikipedia.org/wiki/Archie)から翻訳されています。


**archie**（アーキー、アーチー）は、[FTPサーバ](../Page/FTPサーバ.md "wikilink")のアーカイブの索引を作り、特定のファイルを検索できるようにした、[クライアント・サーバ](https://ja.wikipedia.org/wiki/クライアント・サーバ "wikilink")型システム。史上初のインターネット[検索エンジン](../Page/検索エンジン.md "wikilink")と呼べるものである。 なお、archieが検索するのはファイル名であり、ファイルの内容ではない。

[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に[モントリオール](../Page/モントリオール.md "wikilink")の[マギル大学](../Page/マギル大学.md "wikilink")の学生が最初の実装を開発した。 初期のarchieは単純にFTPサーバに接続してファイルの一覧を取得し（サーバに負荷をかけないよう、月に一度程度）、[UNIX](../Page/UNIX.md "wikilink")の[grep](https://ja.wikipedia.org/wiki/grep "wikilink")コマンドで検索していた。 後に、より効率のよい[フロントエンド](../Page/フロントエンド.md "wikilink")・バックエンドが開発され、archieは単なるローカルのツールにとどまらず、インターネット上のいくつものサイトで提供される人気の高いサービスとなった。 そのようなarchieサーバは、専用クライアント（archieやxarchieなど）、[Telnet](../Page/Telnet.md "wikilink")、[電子メール](../Page/電子メール.md "wikilink")、[WWWなどさまざまな方法でアクセスできるようになっていた](../Page/World_Wide_Web.md "wikilink")。

archieという名前はarchiveに由来しているが、[Archieという名前の漫画も連想させる](https://ja.wikipedia.org/wiki/アーチー・コミック "wikilink")。 これはもともと意図したものではないが、これに影響されて、この漫画の登場人物のJugheadとVeronicaが[Gopher](https://ja.wikipedia.org/wiki/Gopher "wikilink")の検索システムの名前に使われた。

今日ではWWWの検索のほうがはるかに便利であり、稼動しているarchieサーバはほとんどない。

## サーバの一覧

日本国内にあったarchieサーバは以下の通り。

  - archie.kuis.kyoto-u.ac.jp
  - archie.foretune.co.jp
  - archie.wide.ad.jp
  - archie.iij.ad.jp（2006年11月稼動停止）

## 使用例

古典的なコマンドラインクライアントの使用例を示す。 ここでは、"XFree86"という名前のファイルまたはディレクトリを検索している。

`$ archie -h archie.iij.ad.jp XFree86`

`Host ftp.gmd.de`

`    Location: /mirrors2/suse/discontinued/ppc/7.0/suse/inst-sys/usr/X11R6/bin`
`           FILE -r--r--r--    1762856  Nov 17 2000  XFree86`
`    Location: /mirrors2/suse/ftp.suse.com/suse/i386/supplementary/X`
`      DIRECTORY drwxr-xr-x       4096  Jul 16 2003  XFree86`
`    Location: /mirrors2/suse/ftp.suse.com/suse/ppc/7.3/suse/inst-sys/usr/X11R6/bin`
`           FILE -r--r--r--    1822964  May  3 2002  XFree86`
`    Location: /mirrors3/ftp.linuxppc.org/contrib/software/System_Environment`
`      DIRECTORY drwxr-xr-x       4096  May 27 2000  XFree86`
`    Location: /mirrors3/ftp.linuxppc.org/contrib/sources/System`
`      DIRECTORY drwxr-xr-x       4096  Mar 23 2000  XFree86`

`Host rtfm.mit.edu`

`    Location: /pub/usenet-by-group/comp.os.linux.answers/linux/howto`
`           FILE -rw-rw-r--      47032  Nov  6 1995  XFree86`
`    Location: /pub/usenet-by-hierarchy/comp/os/linux/answers/linux/howto`
`           FILE -rw-rw-r--      47032  Nov  6 1995  XFree86`

`Host ftp.sdsc.edu`

`    Location: /mirrors/cerias.purdue.edu/pub/os/FreeBSD/branches/-current/ports/x11`
`      DIRECTORY drwxr-xr-x        512  Oct 13 2000  XFree86`
`    Location: /mirrors/cerias.purdue.edu/pub/os/FreeBSD/development/FreeBSD-CVS/ports/x11`
`      DIRECTORY drwxr-xr-x        512  Oct 13 2000  XFree86`
`    Location: /mirrors/coast.cs.purdue.edu/pub/os/FreeBSD/branches/-current/ports/x11`
`      DIRECTORY drwxr-xr-x        512  Oct  4 2000  XFree86`
`    Location: /mirrors/coast.cs.purdue.edu/pub/os/FreeBSD/development/FreeBSD-CVS/ports/x11`
`      DIRECTORY drwxr-xr-x        512  Oct  4 2000  XFree86`

[Category:インターネット標準](https://ja.wikipedia.org/wiki/Category:インターネット標準 "wikilink") [Category:サーバ](https://ja.wikipedia.org/wiki/Category:サーバ "wikilink") [Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")