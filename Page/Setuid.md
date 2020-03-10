> この記事は[Setuid](https://ja.wikipedia.org/wiki/Setuid)から翻訳されています。


**setuid** と **setgid** は、[UNIX](../Page/UNIX.md "wikilink")におけるアクセス権を表すフラグの名称であり、ユーザーが[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")を実行する際にその実行ファイルの所有者やグループの権限で実行できるようにする。それぞれ、**set** **u**ser **ID** と **set** **g**roup **ID** の略。一般ユーザーが高い特権レベルでしか実行できないタスクを一時的に実行できるようにする仕組みである。提供される[ユーザー識別子](https://ja.wikipedia.org/wiki/ユーザー識別子 "wikilink")や[グループ識別子](https://ja.wikipedia.org/wiki/グループ識別子 "wikilink")によって必ず特権レベルが高くなるわけではないが、少なくともそれら識別子は特定のものが指定されている。

setuid と setgid は一般ユーザーよりも高い特権レベルが必要とされるタスクの実行に必要である。例えば、そのユーザーのログインパスワードの変更などである。中には意外なタスクで特権レベルを上げる必要があることもある。例えば、[ping](https://ja.wikipedia.org/wiki/ping "wikilink") コマンドはネットワークインタフェース上で[制御パケットを送り](../Page/Internet_Control_Message_Protocol.md "wikilink")、応答を待つ必要があり、特権が必要である。

## 実行ファイルでの setuid

[バイナリ](../Page/バイナリ.md "wikilink")の実行ファイルに setuid 属性を付与したとき、一般ユーザーがそのファイルを実行すると、[プロセス](../Page/プロセス.md "wikilink")生成時にそのファイルの所有者（通常は[root](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")）の特権を得ることができる。root の権限がそのプロセスに与えられると、そのアプリケーションは一般ユーザーが通常ならできないタスクを実行できるようになる。それを起動したユーザーがそのプロセスを何とかして通常でない動きをさせようとしても、それは禁止されている。例えば、[ptrace](https://ja.wikipedia.org/wiki/ptrace "wikilink") を使ったり、`LD_LIBRARY_PATH` をいじったり、[シグナルを送ったりといったことである](https://ja.wikipedia.org/wiki/シグナル_\(Unix\) "wikilink")（端末からのシグナルだけは受け付けられる）。セキュリティ上の危険性が増すため、多くのオペレーティングシステムでは[シェルスクリプト](../Page/シェルスクリプト.md "wikilink")形式の実行ファイルへの setuid 属性付与を無視するようになっている。

setuid 機能は非常に便利だが、注意深く設計でされていないプログラムの[実行ファイル](https://ja.wikipedia.org/wiki/実行ファイル "wikilink")に setuid 属性を付与すると、セキュリティ上の危険性が生じる。悪意あるユーザーがそのような実行ファイルを利用して特権を得たり、一般ユーザーが気づかないうちに[トロイの木馬を実行してしまうといった可能性がある](https://ja.wikipedia.org/wiki/トロイの木馬_\(ソフトウェア\) "wikilink")。

setgid 属性はプロセスのグループベースの特権を変更する。

setuid 属性があるのは、UNIXにおいて一般ユーザーが [chroot](https://ja.wikipedia.org/wiki/chroot "wikilink") [システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")を実行できないためである。

setuid ビットと setgid ビットは通常、[chmod](https://ja.wikipedia.org/wiki/chmod "wikilink") コマンドで八進数形式の最上位桁を 4 または 2（両方なら 6）を設定することでセットされる。'chmod 6711' としたとき、setuid ビットと setgid ビットがセットされ(6)、所有者は読み取り/書き込み/実行が可能で(7)、グループとその他のユーザーは実行だけ可能となる(11)。なお、最上位桁の最下位ビットは[スティッキービット](../Page/スティッキービット.md "wikilink")である。

chmod には多くの場合、これらのビットをシンボルで指定するシンボリックモードもある。下記の実施例で使っている 'chmod g+s' はその例である。

実施例にある[C言語](../Page/C言語.md "wikilink")のプログラムは、プロセスの実ユーザー識別子と実グループ識別子および実効ユーザー識別子と実効グループ識別子を表示するだけのものである。実施例ではまず、このプログラムを 'bob' というユーザーでコンパイルし、'chmod' を使って setuid と setgid をセットしている。'su' コマンド自身も setuid 機能を使っているが、ここではユーザーを 'alice' に変更するために使われている。'chmod' コマンドの効果は 'ls -l' でチェックでき、最終的にデモプログラムが実行され、識別子が変更されていることが表示される。/etc/passwd ファイルの内容と比較していただきたい。

なお、'nosuid' オプション付きでマウントされたボリューム上では、このプログラムの実効ユーザー識別子の変更は無視される（変更されず、エラーも表示されない）。

### 実施例

``` bash
[bob@foo]$ cat /etc/passwd
alice:x:1007:1007::/home/alice:/bin/bash
bob:x:1008:1008::/home/bob:/bin/bash

[bob@foo]$ cat printid.c

#include <stdlib.h>
#include <stdio.h>
#include <unistd.h>
#include <sys/types.h>

int main(void)
{
    printf("Real UID\t= %d\n", getuid());
    printf("Effective UID\t= %d\n", geteuid());
    printf("Real GID\t= %d\n", getgid());
    printf("Effective GID\t= %d\n", getegid());

    return EXIT_SUCCESS;
}

[bob@foo]$ gcc -Wall printid.c -o printid
[bob@foo]$ chmod ug+s printid
[bob@foo]$ su alice
Password:
[alice@foo]$ ls -l
-rwsr-sr-x 1 bob bob 6944 2007-11-06 10:22 printid
[alice@foo]$ ./printid
Real UID        = 1007
Effective UID   = 1008
Real GID        = 1007
Effective GID   = 1008
[alice@foo]$
```

## ディレクトリでの setuid

setuid と setgid は[ディレクトリ](../Page/ディレクトリ.md "wikilink")では全く別の意味を持つ。

ディレクトリでsetgidパーミッションを設定すると（chmod g+s）、その後そのディレクトリ配下に作成されるファイルやサブディレクトリはそのグループを継承する（作成したユーザーの主グループは無視される。影響を受けるのはグループだけで、所有者は通常通りである）。新たに作成されるサブディレクトリは setgid ビットも継承する。

典型的な使用例は、グループ間で共有されるディレクトリ、特に[CVSや](../Page/Concurrent_Versions_System.md "wikilink")[Subversionのリポジトリに対して設定することである](../Page/Apache_Subversion.md "wikilink")。[バージョン管理システム](../Page/バージョン管理システム.md "wikilink")のプロセスが適切な[umask](https://ja.wikipedia.org/wiki/umask "wikilink")（一般的に002）でリポジトリにアクセスすることで、GIDを利用したアクセス制御が可能となる。

既存のファイルやサブディレクトリは元のままである点に注意が必要である。既存のサブディレクトリへの setgid ビットの設定は手で行う必要がある。そのコマンド行は以下のようになる。

<code>

`find /path/to/directory -type d -print0 | xargs -0 chmod g+s`</code>

または <code>

`[root@foo]# find /path/to/directory -type d -exec chmod g+s {} \;`</code>

setuidパーミッションをディレクトリに設定しようとしても、UNIX や [Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") では無視される\[1\]。[FreeBSD](../Page/FreeBSD.md "wikilink")では設定が可能であり、setgid と同様に解釈される。すなわち、配下のファイルやサブディレクトリはそのディレクトリと同じ所有者となるよう設定される\[2\]。

## 歴史

setuid ビットは[デニス・リッチー](../Page/デニス・リッチー.md "wikilink")が発明した。リッチーを雇っていた[AT\&T](../Page/AT&T.md "wikilink")は1972年にその特許を申請し、1979年に特許 "Protection of data file contents"（4,135,240）が成立した。この特許は後にパブリックドメインとされた。\[3\]

## 関連項目

  - [Confused deputy problem](https://ja.wikipedia.org/wiki/Confused_deputy_problem "wikilink")
  - [sudo](https://ja.wikipedia.org/wiki/sudo "wikilink")
  - [chmod](https://ja.wikipedia.org/wiki/chmod "wikilink")
  - [ユーザー識別子](https://ja.wikipedia.org/wiki/ユーザー識別子 "wikilink")
  - [ファイルパーミッション](https://ja.wikipedia.org/wiki/ファイルパーミッション "wikilink")
  - [スティッキービット](../Page/スティッキービット.md "wikilink")
  - [環境変数](https://ja.wikipedia.org/wiki/環境変数 "wikilink")

## 脚注

## 外部リンク

  - Hao Chen, David Wagner, Drew Dean: [<cite>Setuid Demystified</cite>](http://www.cs.berkeley.edu/~daw/papers/setuid-usenix02.pdf) (pdf)
  - Wayne Pollock: [Unix File and Directory <cite>Permissions and Modes</cite>](http://wpollock.com/AUnix1/FilePermissions.htm)

[Category:UNIX](https://ja.wikipedia.org/wiki/Category:UNIX "wikilink") [Category:コンピュータセキュリティ](https://ja.wikipedia.org/wiki/Category:コンピュータセキュリティ "wikilink") [Category:コンピュータセキュリティ手続](https://ja.wikipedia.org/wiki/Category:コンピュータセキュリティ手続 "wikilink")

1.
2.
3.