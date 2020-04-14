> この記事は[Fork爆弾](https://ja.wikipedia.org/wiki/Fork爆弾)から翻訳されています。


**Fork爆弾**（フォークばくだん）とは、[コンピュータ](../Page/コンピュータ.md "wikilink")システムへの[DoS攻撃](../Page/DoS攻撃.md "wikilink")の一種で、新たなプロセスを生成する[fork](https://ja.wikipedia.org/wiki/fork "wikilink")機能を使ったものである\[1\]。Fork爆弾は[ワームや](../Page/ワーム_\(コンピュータ\).md "wikilink")[ウイルスのようにコンピュータからコンピュータへ広がることはない](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")。これは、コンピュータ上で同時に実行可能な[プログラム数あるいは](../Page/プログラム_\(コンピュータ\).md "wikilink")[プロセス](../Page/プロセス.md "wikilink")数に制限があるという前提に依存したものである\[2\]。このような自己複製プログラムを *wabbit*、*bacteria*、*rabbit programs* などと呼ぶ。wabbit は単に自己複製するだけでなく、悪意ある副作用を持つようプログラムすることもできる\[3\]。

## 詳細

[thumb](https://ja.wikipedia.org/wiki/ファイル:Fork_bomb.svg "wikilink") Fork爆弾は非常に高速に多数のプロセスを生成して、コンピュータの[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")の管理するプロセスのリストを埋め尽くす。[プロセステーブルが埋め尽くされると](../Page/プロセス制御ブロック.md "wikilink")、いずれかのプロセスを終了させない限り新たなプロセスを生成できなくなる。そして、たとえ1つのプロセスを終了させて対処のためのプロセスを生成しようとしても、Fork爆弾のプロセス群は空いたプロセスのスロットを迅速に埋めようと待っているのである。

プロセステーブルを埋め尽くすだけでなく、Fork爆弾はプロセッサ時間とメモリも占有する。結果としてFork爆弾以外のプロセス群やシステムは動作が困難（低速）となるか、動作できなくなる。

悪意を持って仕掛けられることもあるが、通常のソフトウェア開発において偶然Fork爆弾が発生してしまうこともある。ネットワーク[ソケットで要求を待ちうける](../Page/ソケット_\(BSD\).md "wikilink")[クライアントサーバモデル](../Page/クライアントサーバモデル.md "wikilink")における[サーバ](../Page/サーバ.md "wikilink")プログラムは、[無限ループ](../Page/無限ループ.md "wikilink")となっていることが多く、しかもforkで子プロセスを生成する。そういったアプリケーションにちょっとしたバグがあれば、評価中にFork爆弾のように振る舞うことがある。

## 例

次の例は、[UNIX](../Page/UNIX.md "wikilink")の[bash](https://ja.wikipedia.org/wiki/bash "wikilink")または[zsh](https://ja.wikipedia.org/wiki/zsh "wikilink")でFork爆弾として機能する13文字であり、特によく知られている。

``` bash
:(){ :|:& };:
```

まず、先頭の ":()" は ":" という関数（引数なし）を定義することを宣言している。続く "{ :|:& };" がその本体で、自分自身を2つ起動して[パイプでつなぎ](../Page/パイプ_\(コンピュータ\).md "wikilink")、バックグラウンドで実行することを意味する。バックグラウンドなので、親プロセスを[kill](https://ja.wikipedia.org/wiki/kill "wikilink")しても子プロセスは終了しない。最後の ":" がその関数の実行開始を意味する。この文字列は関数名を ":" として意味をわかりにくくしている。これをもっと判りやすい名前に置換すると次のようになる。

``` bash
forkbomb(){ forkbomb|forkbomb & } ; forkbomb
```

[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") の cmd および command.com 用[バッチファイル](../Page/バッチファイル.md "wikilink"):

``` dos
%0|%0
```

[POSIX](../Page/POSIX.md "wikilink") [C](../Page/C言語.md "wikilink") または [C++](../Page/C++.md "wikilink")による例:

``` c
#include <unistd.h>

int main()
{
  while(1)
    fork();
  return 0;
}
```

[Perl](../Page/Perl.md "wikilink")による例:

``` perl
fork while fork
```

[Python](../Page/Python.md "wikilink")による例:

``` python
import os

while True:
     os.fork()
```

[Ruby](../Page/Ruby.md "wikilink")による例:

``` ruby
def forkbomb
  loop { fork { forkbomb }  }
end; forkbomb
```

## 対処

Fork爆弾が起動させられてしまった場合、その対処としてはFork爆弾が生成した全プロセスを終了させることしかないため、システムの[リブート以外に対処法がないという状況になる可能性がある](../Page/ブート.md "wikilink")。問題のプロセス群を強制終了させるには新たなプロセスを生成しなくてはならないが、[プロセステーブルの空きスロットがない可能性があるし](../Page/プロセス制御ブロック.md "wikilink")、メモリ管理のデータ構造が不足している可能性もある。さらに、Fork爆弾のプロセスが終了してプロセステーブルのスロットが空いたとしても、残っているFork爆弾プロセスが素早く空きスロットを埋めようとする。Windows では、Fork爆弾をスタートさせたユーザーがログアウトすると問題が緩和される可能性がある。

しかし、実際の場ではシステム管理者が比較的容易にFork爆弾を抑制できることもある。例えば

``` bash
:(){ :|: & };:
```

というシェル版Fork爆弾を考えてみよう。このコードが意味することは、`fork` を済ませた親プロセスがシステムに残り続けるわけではなく、すぐに終了するという事実である。従ってFork爆弾はプロセステーブルを埋めると同時に次々と終了している。そこで十分に頻繁に新たなプロセスを起動させようとすれば、Fork爆弾以外のプロセスを起動できる可能性がある。何もしないで存在するだけのプロセスをどんどん起動していけばFork爆弾プロセスの個数を減らすことができ、最終的に一掃できる可能性がある。例えば、次のような [Z Shell](../Page/Z_Shell.md "wikilink") 用コードでFork爆弾を一掃できる可能性がある。

``` bash
while (sleep 100 &) do; done
```

Fork爆弾プロセス群を停止させてから終了させるには、次のようなコマンドを入力する。

``` bash
killall -STOP processWithBombName
killall -KILL processWithBombName
```

しかしこれには問題がある。`killall`コマンドはアトミックに動作するわけではないので、シグナルを送るべきプロセスのPIDを取得してから、実際にシグナルを送るまでにターゲットのプロセスが終了してしまい、Fork爆弾が数世代先に進んでいる可能性がある。

Linuxでは、[procfs](https://ja.wikipedia.org/wiki/procfs "wikilink")からプロセステーブルにアクセスできるので、bash の組み込み機能を使い、新たにプロセスを生成しなくともFork爆弾プロセスを終了させられる可能性がある。次の例はprocfsを使って問題のプロセスを特定し、それらを停止させ、終了させる。

``` bash
cd /proc;
for p in [0-9]*; do read CMDLINE < $p/cmdline; if [[$CMDLINE_==_"processWithBombName"|$CMDLINE == "processWithBombName"]]; then kill -s SIGSTOP $p; fi; done
for p in [0-9]*; do read CMDLINE < $p/cmdline; if [[$CMDLINE_==_"processWithBombName"|$CMDLINE == "processWithBombName"]]; then kill -s SIGKILL $p; fi; done
```

## 予防

基本的には通常のセキュリティ対策を施して、不正なアクセスによるプロセス生成を防ぐのが第一である。しかし、Fork爆弾はプログラミング初心者のミスによって発生することもある。

Fork爆弾が作動する方法は、可能な限り多くのプロセスを生成することである。従ってFork爆弾を防ぐには、1つのプログラムあるいは1人のユーザーが生成できるプロセス数を制限すればよい。信頼できないユーザーが相対的に少数のプロセスしか生成できないようにすれば、悪意があるかどうかに関わらず Fork爆弾の危険性は減る。しかし、複数のユーザーが協力してFork爆弾を使用すれば、そのプロセス数の合計がシステム全体のプロセス数の制限を使い切る可能性は依然として残る。

なお、偶発的にFork爆弾が生じた場合、複数ユーザーがそれに関係することはほとんどありえない。[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")の[grsecurity](https://ja.wikipedia.org/wiki/grsecurity "wikilink")というパッチには、Fork爆弾を開始したユーザーをロギングする機能もある\[4\]。

[Unix系](../Page/Unix系.md "wikilink")システムにはプロセス数の制限があり、*ulimit* というシェルコマンド\[5\]、あるいはその後継の '' setrlimit'' で制御される。Linuxカーネルにはユーザー毎のプロセス数を制限する **RLIMIT_NPROC** があり、`setrlimit()`システムコールで設定される。また、LinuxやBSD系OSでは、`/etc/security/limits.conf` を編集することでも同様の効果が得られる\[6\]。

また、OSがFork爆弾を検出するという対策もある。Linuxには *rexFBD* というカーネルモジュールがあり\[7\]、そのような機能を実装している。

FreeBSDでは、システム管理者が `/etc/login.conf` に制限を置くことができる\[8\]。

このような予防策を講じたとしても、Fork爆弾はシステムに重大な影響を及ぼす可能性がある。例えば、24個のCPUのあるサーバで、各ユーザーが100個までのプロセスを生成できる設定になっている場合、Fork爆弾が100個までしかプロセスを生成できないとしても24個のCPU全部を100%使用することもありうる。これによりシステムは応答不可能となり、システム管理者が問題を解決するためにログインすらできない状況になりうる。

## 脚注

## 関連項目

  - [無限ループ](../Page/無限ループ.md "wikilink")
  - [Fork](../Page/Fork.md "wikilink")

## 外部リンク

  - [Definition of "fork bomb"](http://jazz.he.fi/jargon/html/F/fork-bomb.html) in the [Jargon File](../Page/ジャーゴンファイル.md "wikilink")

[Category:マルウェア](https://ja.wikipedia.org/wiki/Category:マルウェア "wikilink") [Category:DoS攻撃](https://ja.wikipedia.org/wiki/Category:DoS攻撃 "wikilink")

1.  [man page of fork](http://www.freebsd.org/cgi/man.cgi?query=fork&sektion=0&manpath=FreeBSD+8.1-RELEASE) FreeBSD
2.  [Understanding Bash fork() bomb \~ :(){ :|:& };:](http://www.cyberciti.biz/faq/understanding-bash-fork-bomb/) Linux/UNIX FAQ
3.  [Wabbit in the Jargon File (The Hackers Dictionary)](http://jazz.he.fi/jargon/html/W/wabbit.html)
4.  [grsecurity Linux kernel patch](http://grsecurity.net)
5.  [\`man ulimit\` online copy of the man page.](http://linux.die.net/man/1/ulimit)
6.  [\`man limits\` online copy of the man page.](http://linux.die.net/man/5/limits.conf)
7.  [Linux kernel module for fork bomb prevention.](http://rexgrep.tripod.com/rexfbdmain.htm)
8.  [FreeBSD - login.conf](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/users-limiting.html)