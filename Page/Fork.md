> この記事は[Fork](https://ja.wikipedia.org/wiki/Fork)から翻訳されています。


**fork**（フォーク）とは、[プロセス](../Page/プロセス.md "wikilink")の[コピー](../Page/コピー.md "wikilink")を生成するものである。[UNIX](../Page/UNIX.md "wikilink")および[Unix系](../Page/Unix系.md "wikilink")[OSでは](../Page/オペレーティングシステム.md "wikilink")[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")のひとつで、新たに作り出されたプロセスを[子プロセス](../Page/子プロセス.md "wikilink")、`fork()`を呼び出したプロセスを[親プロセスと呼び](../Page/子プロセス.md "wikilink")、`fork()`システムコールの戻り値によって親と子の処理を区別する。子プロセスでは`fork()`の戻り値は0であり、親プロセスの戻り値は新たに生成された子プロセスの[プロセス識別子](../Page/プロセス識別子.md "wikilink")、エラーが起きた場合は-1である。また、[マルチスレッド](https://ja.wikipedia.org/wiki/マルチスレッド "wikilink")環境で[スレッドのコピーを作ることもforkと呼ぶことがある](../Page/スレッド_\(コンピュータ\).md "wikilink")。

`fork`が呼び出されると、子プロセスのための[アドレス空間](../Page/アドレス空間.md "wikilink")が新たに作成される。子プロセスのアドレス空間には親プロセスが持っていた全セグメントのコピーがあるが、[コピーオンライト](https://ja.wikipedia.org/wiki/コピーオンライト "wikilink")機能によって実際の物理メモリの確保は遅延される（すなわち、一時的に同じ物理メモリセグメント群を親子で共有する）。親プロセスと子プロセスは同じコードセグメントを持つが、独立して実行される。

## Unixにおけるforkの重要性

Unixにとってforkは重要であり、[フィルタの開発を奨励している設計哲学の重要な部分を担っている](../Page/フィルタ_\(ソフトウェア\).md "wikilink")。Unixでのフィルタは[標準入力を入力とし](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")[標準出力を出力とする](https://ja.wikipedia.org/wiki/標準ストリーム "wikilink")（通常小さな）プログラムである。[シェルがフィルタを](https://ja.wikipedia.org/wiki/Unixシェル "wikilink")[パイプで連結することで](../Page/パイプ_\(コンピュータ\).md "wikilink")、複雑な処理を実現できる。例えば次のように`find(1)`コマンドの出力を`wc(1)`コマンドの入力に連結すると、拡張子が ".cpp" のファイルをカレントディレクトリ配下で探し、見つかったファイル数を表示できる。

``` bash
$ find . -name "*.cpp" -print | wc -l
```

このコマンド行を入力すると、シェルは自分自身をforkし、[プロセス間通信](../Page/プロセス間通信.md "wikilink")の1つである[パイプを使って](../Page/パイプ_\(コンピュータ\).md "wikilink") `find` コマンドの出力を `wc` コマンドの入力に結びつける。パイプは2つの新たなファイル識別子を生成し、2つの子プロセスを生成する（それぞれ `find` と `wc` に対応）。2つの子プロセスはまず `dup2(2)` で対応するパイプのファイル識別子を複製して標準入力と標準出力に置き換える。そしてそれぞれの子プロセスが`exec(3)`ファミリのシステムコールを使って、実行すべきコマンドのプログラムで自身を[オーバーレイする](https://ja.wikipedia.org/wiki/オーバーレイ_\(コンピュータ用語\) "wikilink")。

より一般的に、シェルはユーザーがコマンド行を入力するたびにforkを行っている。子プロセスはシェルがforkを行うことで生成され、子プロセスが`exec`でオーバーレイを行い、実行すべきプログラムのコードをマッピングする。

## プロセスのアドレス空間

実行ファイルを実行しようとすると、プロセスが生成される。実行ファイルはセグメントと呼ばれるブロックにグループ化されたバイナリコードを含んでいる。各セグメントは特定の種類のデータを格納するのに使われる。典型的な[ELF形式の実行ファイルには](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink")、以下のようなセグメントが存在する。

  - — 実行可能なコードを格納したセグメント

  - [.bss](https://ja.wikipedia.org/wiki/.bss "wikilink") — 初期値がゼロのデータを格納したセグメント

  - — 初期値のあるデータを格納したセグメント

  - [symtab](../Page/シンボルテーブル.md "wikilink") — プログラムのシンボル群（例えば、関数名、変数名など）を格納したセグメント

  - interp — 使用すべきインタプリタの名前を格納したセグメント

`readelf` コマンドを使えば、ELF形式のファイルの詳細を表示できる。そのようなファイルを実行するためにメモリ上にロードすると、セグメント群がメモリにロードされることになる。実行ファイル全体を連続なメモリ位置にロードする必要はない。メモリはページと呼ばれる同じ大きさ（通常4KB）の部分に分けられている。したがって実行ファイルをメモリにロードする際、実行ファイル内のそれぞれの位置がそれぞれ異なるページに置かれる（ページ群は連続とは限らない）。大きさが10KBのELF形式の実行ファイルがあるとする。そのOSのサポートするページサイズが4KBなら、そのファイルは4KB、4KB、2KBという3つの部分に分けてロードされる（他に[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")も必要）。この3つのフレームはメモリ中の任意のフリーなページに置くことができる\[1\]。

## forkとページ共有

`fork()`システムコールを実行すると、本来ならばOSが子プロセスのために親プロセスの持つ全ページを物理メモリ上の別の位置にコピーすることになる。しかし、場合によってはその必要はない。子プロセスが`fork()`直後に "[`exec`](https://ja.wikipedia.org/wiki/exec "wikilink")" システムコール（実行ファイルを実行するときに使用する）を実行する場合や終了する場合である。親プロセスが何らかのコマンドを実行するためだけに子プロセスを生成した場合、子プロセスのアドレス空間は実行すべきコマンドですぐに置換されるので、親プロセスのページ群をコピーする必要はない。

そのため、[コピーオンライト](https://ja.wikipedia.org/wiki/コピーオンライト "wikilink") (COW) という技法が使われる。COWでは、fork時に親プロセスのページ群を子プロセスにコピーしない。その代わりページ群は親プロセスと子プロセスの間で共有される。親子いずれかのプロセスがページの内容を更新しようとしたとき、そのページだけコピーを作成し、書き込もうとしたプロセスの当該ページだけが更新される。書き込んだプロセスはその後その新たにコピーしたページを使用する。もう一方のプロセス（共有ページに書き込まなかったプロセス）は、コピー元のページを使用し続ける（共有状態は解消される）。何らかのプロセスが書き込もうとしたときにページがコピーされるので、この技法をコピーオンライトと呼ぶ。

## vforkとページ共有

`vfork` はもう1つのプロセス生成用UNIXシステムコールである。`vfork()`システムコールで子プロセスを生成すると、子プロセスが終了するか`execve()`ファミリのシステムコールで新たな実行イメージに切り換えるまでそのシステムコールの延長上で親プロセスが待ち合わせる。`vfork`でも親プロセスと子プロセスでページ群を共有するが、コピーオンライトは必要としない。子プロセスが共有ページに更新を加えてもコピーは作成せず、親プロセスからもその更新が見える。ページを全くコピーしないので、子プロセスでコマンドを実行する場合には非常に効率的である。

実装によっては `vfork()` は `fork()` と同じである\[2\]。

`vfork()`と`fork()`の唯一の違いは、親プロセスと子プロセスがコードとデータを共有できる点である。これによって複製は劇的に高速化されるが、使い方を誤ると親プロセスの一貫性が壊れる危険性がある。

直後に `exec` または `_exit()` を呼び出す以外の`vfork()`の使用は推奨されない。特にLinuxのmanページではvforkそのものの使用が推奨されていない\[3\]。

`vfork()`で生成した子プロセスが`vfork()`を呼び出したルーチンからさらに外側に復帰した場合、親プロセスの[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")を書き変えてしまうので、`vfork()`から親プロセスが戻ったときの動作を保証できない。また、execせずに子プロセスを終了する場合、`_exit()`ではなく`exit()`を使用すると、標準I/Oチャネルをフラッシュしてクローズするため親プロセスの標準I/O構造にダメージを与える危険性がある。なお、`fork()`の場合でも子プロセスが`exit()`を呼び出すのは危険である。

`vfork()`後に子プロセスでシグナルハンドラが呼び出された場合、子プロセスの他のコードと同じ規則に従う必要がある\[4\]。

## MMUのないシステム

[組み込みシステム](../Page/組み込みシステム.md "wikilink")では[メモリ管理ユニット](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink") (MMU) が存在しない場合があり、`fork()` でのコピーオンライトの実装ができないことがある。システムがプロセス毎のアドレス空間を他の何らかの機構で（例えば[セグメント方式](../Page/セグメント方式.md "wikilink")で）サポートする場合、プロセスの使用する全メモリをコピーすれば実質的には同じである。しかしそれは非常に時間がかかるし、多くの場合すぐに別の実行ファイルのイメージで書き換えられるので無駄である。

全プロセスが単一のアドレス空間を共有している場合、例えば全メモリページをスワップして[コンテキストスイッチ](https://ja.wikipedia.org/wiki/コンテキストスイッチ "wikilink")するという`fork()`の実装も考えられる。[μClinux](https://ja.wikipedia.org/wiki/μClinux "wikilink")ベースのOSなどの[組み込みOSが採用しているのは](../Page/組み込みオペレーティングシステム.md "wikilink")、`fork()` を廃して `vfork()` だけを実装するという方法である。そのため、forkを使っているところを全てvforkで動作できるように書き換えている。

## Unix以外でのフォーク

Unix系やLinuxでのfork機構は、基盤となっているハードウェアにある種の前提を課している。リニアなメモリ空間と[ページング機構を持ち](https://ja.wikipedia.org/wiki/ページング方式 "wikilink")、連続なアドレス範囲のメモリコピーを効率的に行えるという前提である。VMS（現在の[OpenVMS](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")）の当初の設計では、コピー操作後に少数の具体的なアドレスの内容書き換えを行うフォークは危険だとみなされていた。現在のプロセス状態におけるエラーが子プロセスにコピーされるかもしれない。そこでプロセスのスポーン（産卵）というメタファーが使われた。すなわち、新しいプロセスのメモリレイアウトの各コンポーネントを一から新たに構築する。[ソフトウェア工学](../Page/ソフトウェア工学.md "wikilink")的観点からすれば後者（スポーン）の手法の方がきれいで安全だが、フォークの方が効率的なのでよく使われている。スポーン方式は後にマイクロソフトのOSで採用された。

## fork を使ったコード例

### C の例

``` c

#include <stdio.h>   /* printf, stderr, fprintf */
#include <sys/types.h> /* pid_t */
#include <unistd.h>  /* _exit, fork */
#include <stdlib.h>  /* exit */
#include <errno.h>   /* errno */

int main(void)
{
   pid_t  pid;

   /* 子プロセスと親プロセスの両方の出力が
    * 標準出力に書かれる。
    * 両者は同時に動作する。
    */
   pid = fork();
   if (pid == -1)
   {
      /* エラー:
       * fork()が-1を返す場合、エラーが起きたことを示す。
       * 例えばプロセス数が制限に達した場合など。
       */
      fprintf(stderr, "can't fork, error %d\n", errno);
      exit(EXIT_FAILURE);
   }

   if (pid == 0)
   {
      /* 子プロセス:
       * fork()が0を返す場合、子プロセスである。
       * 1秒に1ずつ、10まで数える。
       */
      int j;
      for (j = 0; j < 10; j++)
      {
         printf("child: %d\n", j);
         sleep(1);
      }
      _exit(0);  /* exit() を使わない点に注意 */
   }
   else
   {

      /* fork() が正の数を返す場合、親プロセスである。
       * その値は生成した子プロセスのPIDである。
       * ここでも10まで数える。
       */
      int i;
      for (i = 0; i < 10; i++)
      {
         printf("parent: %d\n", i);
         sleep(1);
      }
      exit(0);
   }
   return 0;
}
```

### Perl の例

``` perl
#!/usr/bin/env perl -w
use strict;

if (fork) { # 親プロセス
    foreach my $i (0 .. 9) {
        print "Parent: $i\n";
        sleep 1;
    }
}
else { # 子プロセス
    foreach my $i (0 .. 9) {
        print "Child: $i\n";
        sleep 1;
    }
    exit(0); # forkした子プロセスの終了
}

exit(0); # 親プロセスの終了
```

### Python の例

``` python
#!/usr/bin/env python

import os, time, sys

def createDaemon():
  "This function create a service/Daemon that will execute a det. task"

  try:
    # forkしたPIDを格納
    pid = os.fork()

    if pid > 0:
      print 'PID: %d' % pid
      sys.exit()

  except OSError as error:
    print 'Unable to fork. Error: %d (%s)' % (error.errno, error.strerror)
    sys.exit(1)

  doTask()

def doTask():
  "This function create a task that will be a daemon"

  # ライトモードでファイルをオープン
  log_file = open('/tmp/tarefa.log', 'w')


  while True:
    print >> log_file, time.ctime()
    log_file.flush()
    time.sleep(2)

  # ファイルをクローズ
  log_file.close()

if __name__ == '__main__':

  # デーモンを生成
  createDaemon()
```

## Fork-Exec

**Fork-Exec**は、[UNIX](../Page/UNIX.md "wikilink")で一般的に使われる手法であり、新たなプログラムを[プロセス](../Page/プロセス.md "wikilink")として実行する。`fork()`は[親プロセス](https://ja.wikipedia.org/wiki/親プロセス "wikilink")を2つの同一内容のプロセスに（[フォークの先のように](../Page/フォーク_\(食器\).md "wikilink")）分岐させる[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")である。`fork()`によって[子プロセス](../Page/子プロセス.md "wikilink")が親プロセスのコピーとして生成され、子プロセスが`exec()`システムコールを呼び出すことで（子プロセス）自身の内容を置き換える。

親プロセスが子プロセスの終了を待ち合わせる場合、子プロセスの[終了コード](https://ja.wikipedia.org/wiki/終了コード "wikilink")を受け取ることができる。子プロセスが[ゾンビプロセス](https://ja.wikipedia.org/wiki/ゾンビプロセス "wikilink")となるのを防ぐには、親プロセスがシステムコールを使用する必要があり、そのタイミングは定期的でもよいし、[SIGCHLDシグナルを受け取った際でもよい](../Page/シグナル_\(Unix\).md "wikilink")。

子プロセスが`exec()`を呼び出すと、その[アドレス空間](../Page/アドレス空間.md "wikilink")の内容は全て失われ、指定されたプログラムを実行するためのアドレス空間のマッピングが新しく設定される。これを[オーバーレイと呼ぶ](https://ja.wikipedia.org/wiki/オーバーレイ_\(情報工学\) "wikilink")。アドレス空間は全て置き換えられるが、オープン済みファイルの[ファイル記述子](../Page/ファイル記述子.md "wikilink")群は *close-on-exec* が指定されたときだけ `exec()`時に自動的にクローズされる。この特徴を利用して、`fork()`を呼び出す前に[パイプを作成しておき](../Page/パイプ_\(コンピュータ\).md "wikilink")、`exec()`で指定された新しいプログラムとの通信を行うというUNIX特有の手法が実現されている。

なお、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") では `fork()` 単独に相当するシステムコールがなく、fork-exec モデルを採用していない。代わりにファミリ関数が `process.h` で定義されており、fork-exec に相当する働きをする。

## 脚注

## 参考文献

  - ["File descriptors across fork(2)/exec(2)"](http://www.cim.mcgill.ca/~franco/OpSys-304-427/messages/node91.html), Operating Systems (Course 304-427B), Franco Callari, Electrical Engineering Department, [McGill University](https://ja.wikipedia.org/wiki/マギル大学 "wikilink")
  - *Advanced Programming in the UNIX Environment*, [W. Richard Stevens](../Page/W・リチャード・スティーヴンス.md "wikilink"), Addison-Wesley ISBN 0-201-56317-7
  - *Unix Power Tools*, Jerry Peek, [Tim O'Reilly](../Page/ティム・オライリー.md "wikilink"), Mike Loukides, [O'Reilly](../Page/オライリーメディア.md "wikilink"), ISBN 1-56592-260-3

## 関連項目

  - [子プロセス](../Page/子プロセス.md "wikilink")
  - [Fork爆弾](https://ja.wikipedia.org/wiki/Fork爆弾 "wikilink")

## 外部リンク

  -
  - [Lightwolf](http://lightwolf.sourceforge.net), A library that implements thread forking for Java

  - [NetBSD: Why implement traditional vfork()](http://www.netbsd.org/docs/kernel/vfork.html)

  - [Fork and Exec](http://www-h.eng.cam.ac.uk/help/tpl/unix/fork.html) ケンブリッジ大学 Computing Help

  - [Unix Programming Frequently Asked Questions 日本語訳](http://www.race.u-tokyo.ac.jp/~moro/unix-programmer/faq-j_2.html#SEC6) 1.1.3 forkによる子プロセスを終了するときにexitよりも_exitを使うのはなぜですか?

[Category:OSのプロセス管理](https://ja.wikipedia.org/wiki/Category:OSのプロセス管理 "wikilink") [Category:UNIXのシステムコール](https://ja.wikipedia.org/wiki/Category:UNIXのシステムコール "wikilink") [Category:オペレーティングシステムの仕組み](https://ja.wikipedia.org/wiki/Category:オペレーティングシステムの仕組み "wikilink")

1.  正確には、これは[ページング方式](https://ja.wikipedia.org/wiki/ページング方式 "wikilink")の仮想記憶の場合である。また、.bssは実行ファイル上では対応するデータが存在せず、単に仮想空間の範囲だけが確保される。
2.
3.  [VFORK](http://www.linuxmanpages.com/man2/vfork.2.php)
4.  [The Open Group Base Specifications Issue 6](http://pubs.opengroup.org/onlinepubs/009695399/functions/vfork.html) - POSIX.1-2001 *(IEEE Std 1003.1)* Copyright © 2001-2004 The IEEE and [The Open Group](http://www.opengroup.org/)