> この記事は[User Mode Linux](https://ja.wikipedia.org/wiki/User_Mode_Linux)から翻訳されています。


**User Mode Linux**(UML/user-mode-linux)は、[Linux](../Page/Linux.md "wikilink")環境を仮想的に作りだすための仕組みである。[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")を[ユーザーモード](https://ja.wikipedia.org/wiki/ユーザーモード "wikilink")のプログラムとしてコンパイルして、実行させる。ホスト環境の[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")と、ホスト環境のユーザーモードのプロセスとして動く Linux カーネル（UML本体）の連携により、 Linuxゲスト環境を提供する。

## 基本構造

[Libvirt_support.svg](https://ja.wikipedia.org/wiki/File:Libvirt_support.svg "fig:Libvirt_support.svg")\]\] UMLの[カーネル](../Page/カーネル.md "wikilink")は、基本的にUML向けにコンパイルされたカーネルに、プログラムローダをくっつけた形に構築されており、Linux上で実行することで、プロセスの中で独立したLinuxが動作する構造となっている。[ホスト](https://ja.wikipedia.org/wiki/ホスト "wikilink")OSもLinuxであることが前提である。サポートしている CPU は x86-32 と x86-64。

UML上で動作するゲストプロセスは[デバッガ](../Page/デバッガ.md "wikilink")などで使われる ptrace を使い、[システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")や[シグナルを横取りし](../Page/シグナル_\(Unix\).md "wikilink")、それをホスト側に投げ、システムコールやシグナルを成立させている。ゲストプロセスのシステムコールは ptrace で横取りした際、EAX レジスタを書き換えて getpid() に置き換え無害化したうえで、UML 内からシステムコールを実行し、戻り値を EAX レジスタに設定して、ptrace でゲストプロセスを再開させる\[1\]。本来1往復だったシステムコールの[コンテキストスイッチ](https://ja.wikipedia.org/wiki/コンテキストスイッチ "wikilink")は4往復になる。Linux は [mmap](https://ja.wikipedia.org/wiki/mmap "wikilink") で MAP_FIXED を使うと、ユーザーモードからでも固定番地にメモリを確保できるが、それを利用して特定の番地にメモリを割り振っている。UML 自体は CPU の特権命令を一切使ってない。

UMLカーネルは、ディスク資源、メモリ、ネットワークなどホストの資源を一部間借りすることができる。UML 用のデバイスドライバが作られている。特にディスクは、実際のディスクではなく、イメージファイルをディスクにみせかけることができるようになっている上、本来のイメージファイルに差分ファイルを組み合わせることで、イメージファイルに書き込みを行わずに利用することも可能となっている。そのため、単一イメージを複数のUMLで共有することも可能である。

## カーネル作成

UMLのカーネルは、通常配布されているLinux[カーネル](../Page/カーネル.md "wikilink")に、ビルド時に ARCH=um を指定することで作成可能である\[2\]。カーネル(ファイル名"linux")とモジュールが作成される。このファイル(linux)を実行すると、UMLが起動する。

## skas

当初は、tt モード（tracing thread mode）と名付けたモードで動いていて、ゲストの全てのプロセスが単一のメモリアドレス空間で動いていた。その後、2002年に skas3 モードという、ちゃんとプロセスごとに別のメモリアドレス空間に分かれているモードが作られたが\[3\]、ホスト側の Linux カーネルにパッチが必要で、/proc/mm, PTRACE_FAULTINFO, PTRACE_LDT の3つが必要だが、Linus に拒否され、Linux のメインラインに加えてもらえなかった。その後、2005年に Linux 2.6.13 から、ホスト側の Linux カーネルにパッチを当てることなく、ちゃんとプロセスごとにメモリ空間が分かれている skas0 が開発され\[4\]、現在は、この skas0 のみが UML ではサポートされている。skas0 では、各プロセスの番地 0x100000 に 8KB 分のメモリ領域を確保し、そこにプログラムとデータを置き、そこから各プロセスの権限で Linux システムコールを呼び出している。

skas0 で 0x100000 に置いたプログラムを実行するにあたり、ptrace でゲストプロセスを一度止め、呼び出したいシステムコールなどの情報をセットし、EIP レジスタを含め全てのレジスタを書き換えて、いきなり 0x100000 に置いたプログラムの場所からゲストプロセスを再開し、システムコール呼び出しなど必要な処理をした後、そのプログラムの最後の所に int3 を置き、ptrace のブレークポイントとして SIGTRAP を発生させ、UML 側に制御を戻す形で実現している\[5\]。

## 参照

## 外部リンク

  -
  - [コンパイル済みカーネル](http://uml.devloop.org.uk/)

  - [コンパイル済みルートファイルシステム](http://fs.devloop.org.uk/)

[Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink") [Category:仮想化](https://ja.wikipedia.org/wiki/Category:仮想化 "wikilink")

1.  [System call virtualization using ptrace](http://www.csee.wvu.edu/~katta/uml/x375.html)
2.  [Building from source](http://user-mode-linux.sourceforge.net/source.html)
3.  [skas mode](http://user-mode-linux.sourceforge.net/old/skas.html)
4.  [UML - skas0 - separate kernel address space on stock hosts - LWN.net](http://lwn.net/Articles/142494/)
5.  [linux/arch/x86/um/stub_32.S at master - torvalds/linux](https://github.com/torvalds/linux/blob/master/arch/x86/um/stub_32.S)