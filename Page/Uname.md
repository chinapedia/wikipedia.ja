> この記事は[Uname](https://ja.wikipedia.org/wiki/Uname)から翻訳されています。


**uname**（ユーネーム、**Unix Name**の略）は [UNIX](../Page/UNIX.md "wikilink") のプログラムであり、実行している[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の名前やバージョンなどを出力する。移植性のあるプログラムを書こうとする場合、実行環境の判別ができ、有用である。**uname** システムコールとコマンドは [PWB/UNIX](https://ja.wikipedia.org/wiki/PWB/UNIX "wikilink") で最初に出現した。

[AT\&T](../Page/AT&T.md "wikilink") [UNIX System V](../Page/UNIX_System_V.md "wikilink") Release 3.0 のような一部の Unix では `setname` というプログラムが含まれ、`uname` が出力する値を変えるのに使われる。

[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")バージョンの `uname` は "sh-utils" つまり "coreutils" パッケージに含まれる。`uname` 自体はスタンドアロンのプログラムとして利用できない。

## 例

[Darwin](../Page/Darwin_\(オペレーティングシステム\).md "wikilink") を実行しているシステムでは、-a [オプション](https://ja.wikipedia.org/wiki/オプション "wikilink") を付けた `uname` からの出力は以下のようになるだろう。

`Darwin hostname.local 8.10.1 Darwin Kernel Version 8.10.1: Wed May 23 16:33:00 PDT 2007;`
`root:xnu-792.22.5~1/RELEASE_I386 i386 i386`

以下の表ではさまざまなプラットフォームにおけるさまざまなバージョンの `uname` からの出力例を示してある。

<table>
<thead>
<tr class="header">
<th><p>オペレーティングシステム</p>
</th></th>
<th><p><code>-s</code> カーネルまたはシステム名</p>
</th></th>
<th><p><code>-o</code> OS</p>
</th></th>
<th><p><code>-m</code> マシン</p>
</th></th>
<th><p><code>-p</code> プロセッサ</p>
</th></th>
<th><p><code>-i</code> ハードウェアプラットフォーム</p>
</th></th>
<th><p><code>-v</code> カーネルバージョン</p>
</th></th>
<th><p><code>-r</code> カーネルリリース</p>
</th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Cygwin (Windows XP), Pentium 4</p>
</td></td>
<td><p>CYGWIN_NT-5.1</p>
</td></td>
<td><p>Cygwin</p>
</td></td>
<td><p>i686</p>
</td></td>
<td><p>unknown</p>
</td></td>
<td><p>unknown</p>
</td></td>
<td><p>2006-01-20 13:28</p>
</td></td>
<td><p>1.5.19(0.150/4/2)</p>
</td></td>
</tr>
<tr class="even">
<td><p>FreeBSD 6.1, Intel</p>
</td></td>
<td><p>FreeBSD</p>
</td></td>
<td><p>不正なオプション</p>
</td></td>
<td><p>i386</p>
</td></td>
<td><p>i386</p>
</td></td>
<td><p>[カーネル conf ファイルの名前]</p>
</td></td>
<td><p>FreeBSD 6.1-RELEASE-p15 #1: Sun Apr 15 18:04:51 EDT 2007</p>
</td></td>
<td><p>6.1-RELEASE-p15</p>
</td></td>
</tr>
<tr class="odd">
<td><p>IRIX 6.5.30, Octane2</p>
</td></td>
<td><p>IRIX64</p>
</td></td>
<td><p>不正なオプション</p>
</td></td>
<td><p>IP30</p>
</td></td>
<td><p>mips</p>
</td></td>
<td><p>不正なオプション</p>
</td></td>
<td><p>07202013</p>
</td></td>
<td><p>6.5</p>
</td></td>
</tr>
<tr class="even">
<td><p>Solaris 9, Sun Fire 280R</p>
</td></td>
<td><p>SunOS</p>
</td></td>
<td><p>不正なオプション</p>
</td></td>
<td><p>sun4u</p>
</td></td>
<td><p>sparc</p>
</td></td>
<td><p>SUNW,Sun-Fire-280R</p>
</td></td>
<td><p>Generic_112233-08</p>
</td></td>
<td><p>5.9</p>
</td></td>
</tr>
<tr class="odd">
<td><p>OpenSuse 10.3, Core2-duo 64-bit</p>
</td></td>
<td><p>Linux</p>
</td></td>
<td><p>GNU/Linux</p>
</td></td>
<td><p>x86_64</p>
</td></td>
<td><p>x86_64</p>
</td></td>
<td><p>x86_64</p>
</td></td>
<td><p>#1 SMP 2007/09/21 22:29:00 UTC</p>
</td></td>
<td><p>2.6.22.5-31-default</p>
</td></td>
</tr>
</tbody>
</table>

## 外部リンク

  - [Manpage of UNAME](https://linuxjm.osdn.jp/html/GNU_sh-utils/man1/uname.1.html) JM Project
  - [uname(1)](https://docs.oracle.com/cd/E19253-01/819-1210/6n3j74jv0/index.html) man page（SunOS リファレンスマニュアル）
  - [uname(1)](https://nixdoc.net/man-pages/HP-UX/man1/uname.1.html) man page（HP-UX リファレンス）

[Category:UNIXのソフトウェア](https://ja.wikipedia.org/wiki/Category:UNIXのソフトウェア "wikilink")