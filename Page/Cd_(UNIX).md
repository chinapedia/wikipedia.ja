> この記事は[Cd \(UNIX\)](https://ja.wikipedia.org/wiki/Cd_\(UNIX\))から翻訳されています。


**`cd`**（シーディー、**c**hange **d**irectory）は、[シェル](../Page/シェル.md "wikilink")等の（プロセスの）現在のワーキングディレクトリ（カレントディレクトリ）を変更する[コマンドである](https://ja.wikipedia.org/wiki/コマンド_\(コンピュータ\) "wikilink")。`chdir` という名前だったりそのような別名があることもある。原理的に[外部コマンド](https://ja.wikipedia.org/wiki/外部コマンド "wikilink")として実装することが不可能であり、かならずシェル等の内部コマンド（ビルトインコマンド、[:en:Shell builtin](https://ja.wikipedia.org/wiki/:en:Shell_builtin "wikilink")）として実装される。

[ディレクトリ](../Page/ディレクトリ.md "wikilink")は[ファイルシステム](../Page/ファイルシステム.md "wikilink")中の論理的な区分であり、[ファイルを保持するために使われる](../Page/ファイル_\(コンピュータ\).md "wikilink")。ディレクトリは他のディレクトリをも含めることができる。`cd`コマンドはサブディレクトリ（子ディレクトリ）に移動したり、親ディレクトリに移動したり、ルートディレクトリ（すべてのディレクトリの祖先ディレクトリ）に一気に移動したり、ある与えられたディレクトリに移動したりすることができる。

次の図は何らかのファイルシステムの一部分を示している。1つのファイル ("text.txt")と3つのサブディレクトリを含むユーザの[ホームディレクトリ](../Page/ホームディレクトリ.md "wikilink")（`~`で表している\[1\]）が示されている。

[center](https://ja.wikipedia.org/wiki/ファイル:Chdir_example.png "wikilink")

もしカレントディレクトリがホームディレクトリ（\~）であれば、「`cd games`」というコマンドを実行した後で「[`ls`](https://ja.wikipedia.org/wiki/ls_\(UNIX\) "wikilink")」と実行すると、例えば次のような結果が得られる。

``` console
me@host:~$ ls
workreports games   encyclopedia    text.txt
me@host:~$ cd games
me@host:games$
```

ユーザはこの時点で"`games`"ディレクトリにいる。 似たようなことを[MS-DOS](../Page/MS-DOS.md "wikilink")で実行すると次のようになる。MS-DOSにはバージョンによってホームディレクトリの概念が存在しないこともある\[2\]。

``` doscon
C:\>dir
workreports <DIR> Wed Oct 9th 9:01
games <DIR> Tue Oct 8th 14:32
encyclopedia <DIR> Mon Oct 1st 10:05
text txt 1903 Thu Oct10th 12:43
C:\>cd games
C:\games>
```

`cd`に引数を与えずに実行した場合、システムによって異なる振る舞いをする。例えばMS-DOSやWindowsではカレントドライブとそのカレントディレクトリが、その絶対パスの文字列で表示される（Unixの[pwd](https://ja.wikipedia.org/wiki/pwd "wikilink")に類似）。Unixではシェル変数 $HOME に設定されたディレクトリ（通常はユーザのホームディレクトリがログイン時に環境変数として設定されている）に移動する。

[バッチファイル](../Page/バッチファイル.md "wikilink")や[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")内で`cd`が実行された場合の効果もシステムによって異なる、というように考える者がいるようだが、シングルタスクのMS-DOSで学習した結果、根本的にプロセスの概念をわかっていないと、そのような把握になるものと思われる。すなわち、MS-DOSのバッチファイルはサブプロセスとして実行されるのではなく、そのシェル自身の入力を一時的に切替えるだけのものであるため、バッチファイル内でのcdコマンドはそのシェル自身に影響する。[Unixのシェルでは普通](../Page/Unix系.md "wikilink")、シェルスクリプトをそのシェル自身に対するコマンド列として実行するか（ source あるいは . コマンド）、サブプロセスとして実行されるシェル（サブシェル）で実行するか（通常の外部コマンドのようにして実行した場合）を選べるため、結果はそれに応じて異なる。

## 注

<references/>

## 外部リンク

  - [cd(1)](https://docs.oracle.com/cd/E19253-01/819-1210/6n3j74jla/index.html) man page（SunOS リファレンスマニュアル 1 : ユーザーコマンド） - [オラクル](../Page/オラクル_\(企業\).md "wikilink")

[Category:標準UNIXプログラム](https://ja.wikipedia.org/wiki/Category:標準UNIXプログラム "wikilink") [Category:DOSの内部コマンド](https://ja.wikipedia.org/wiki/Category:DOSの内部コマンド "wikilink")

1.  '\~' を、通常はユーザのホームディレクトリが設定されている変数 $HOME として解釈するか否かはシェルの実装に依存する。
2.  どちらかというとユーザの脳内の概念の問題であることがある。