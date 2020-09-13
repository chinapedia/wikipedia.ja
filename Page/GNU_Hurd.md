> この記事は[GNU Hurd](https://ja.wikipedia.org/wiki/GNU_Hurd)から翻訳されています。


**GNU Hurd**（グヌー ハード）は、[GNU Mach上で動作し](https://ja.wikipedia.org/wiki/GNU_Mach "wikilink")、[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) の機能を提供する[サーバ](https://ja.wikipedia.org/wiki/マイクロカーネル#サーバ "wikilink")\[1\]群。[GNUプロジェクト](../Page/GNUプロジェクト.md "wikilink")によって開発されている。

Hurdは[カーネル](../Page/カーネル.md "wikilink")と説明されることが多いが、厳密には[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")であるMachと、その上で動くサーバ群であるHurdの組合せによって、一般的なカーネルのサービスを提供する。

**Hurd**は、「**H**ird of **U**nix **R**eplacing **D**aemons.」の頭文字であり、さらに**Hird**は、「**H**urd of **I**nterfaces **R**epresenting **D**epth.」の頭文字である。また、「herd of gnus」（[ヌー](../Page/ヌー.md "wikilink")の群れ）とも掛けている。

## 概要

[リチャード・ストールマン](../Page/リチャード・ストールマン.md "wikilink")が提唱し、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")から開発が始まった\[2\]。UNIX代替品の開発を目標とするGNUプロジェクトにとって、カーネルに相当するHurd（及びMach）の開発は最重要課題とも言えるが、その開発スピードは遅く、2011年現在でも正式版のリリースには至っていない。また、Hurdを採用した[ディストリビューション](https://ja.wikipedia.org/wiki/ディストリビューション "wikilink")として、[Debian](../Page/Debian.md "wikilink")による開発版が存在するが、これについても公式版のリリース時期は未定である。

開発の遅れにより、UNIX互換の[フリーなカーネルとしては](../Page/フリーソフトウェア.md "wikilink")、GNUプロジェクトによるものではない[Linux](../Page/Linux.md "wikilink")が[デファクトスタンダード](../Page/デファクトスタンダード.md "wikilink")となっている。Linuxとの開発スピードの違いについて、[エリック・レイモンド](../Page/エリック・レイモンド.md "wikilink")は『[伽藍とバザール](../Page/伽藍とバザール.md "wikilink")』で、[カテドラル方式](https://ja.wikipedia.org/wiki/カテドラル方式 "wikilink")（伽藍方式）と[バザール方式](../Page/バザール方式.md "wikilink")の違いによると主張している。一方、ストールマンは、開発の遅れは[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")のデバッグが予想以上に難しかったためであり、LinuxがHurdに比べ早く開発できたのは、Linuxが[モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")であることによるとし、自分の戦略的なミスであったと述べている\[3\]。

## 歴史

特に断らない限りGNUプロジェクト自身によるドキュメント\[4\]を出典とする。

1986年2月、リチャード・ストールマンが[GNU](../Page/GNU.md "wikilink")の公式カーネルとして[マサチューセッツ工科大学](../Page/マサチューセッツ工科大学.md "wikilink")で開発されたを使用すると表明し、同年12月までに[フリーソフトウェア財団](../Page/フリーソフトウェア財団.md "wikilink")（以下FSF）はTRIXの改良を開始した。

1987年〜1988年ごろ、FSFは自分でTRIXを改良するよりも、別の人の手によるカーネルを使いたいと考え始める。当時の候補としてはTRIXを改良し続けることの他に[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")で開発されたspriteを使うこと、そして[カーネギーメロン大学](https://ja.wikipedia.org/wiki/カーネギーメロン大学 "wikilink")で開発され後に公式カーネルとなる[Mach](../Page/Mach.md "wikilink")を使うことがあった。

1990年、Machが4.3BSDに関する部分をカーネルからユーザランドへ除出することでGNUの再配布ライセンスに適合するようになる\[5\]と、FSFはMachの上で動くHurdの開発を開始した。ここにMachがGNUの公式カーネルとなった。

1994年4月にブートができ、ファイルシステム、認証サーバ、[init](https://ja.wikipedia.org/wiki/init "wikilink")などを動かすことに成功する。同年7月にはemacsを、11月にはgccを動かすことにも成功した。

1996年4月に、バージョン0.0（テスト版）のソースコード及びi386アーキテクチャ上で動くバイナリが公開される。

1997年6月、他のGNUソフトウェアと組み合わせて完全なOSとして利用できるバージョン0.2がリリースされた。また[Debianプロジェクト](https://ja.wikipedia.org/wiki/Debianプロジェクト "wikilink")によるコンパイル済みバイナリ[Debian GNU/Hurdも配布されている](https://ja.wikipedia.org/wiki/Debian_GNU/Hurd "wikilink")。しかし、製品レベルのシステムと比べて期待されるようなパフォーマンスや安定性を達成できていない状態\[6\]であり、現在も開発中で正規版をリリースするには至っていない。

## アーキテクチャ

多くの[UNIX系](https://ja.wikipedia.org/wiki/UNIX系 "wikilink")カーネルと違って、Hurdは[マイクロカーネル](https://ja.wikipedia.org/wiki/マイクロカーネル "wikilink")の上に構築された、サーバ-クライアントアーキテクチャを採用している。このマイクロカーネルは、もっとも基本的なカーネルのサービスを提供するのに用いられており、それは[ハードウェア](../Page/ハードウェア.md "wikilink")へのアクセスを調整することである。これには、[CPU](../Page/CPU.md "wikilink")（[プロセス](../Page/プロセス.md "wikilink")マネジメントとスケジューリングを通じて）、[RAM](../Page/Random_Access_Memory.md "wikilink")（[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")管理を通じて）、音声、グラフィックス、マスストレージなど、その他多様なインプット/アウトプットデバイス（I/Oスケジューリングを通して）の調整が含まれる。マイクロカーネルの設計理論は、全てのデバイスドライバに、ユーザースペースで動くサーバーとしてビルトされることを許すが、今日多くのドライバーは依然として[GNU Machのカーネルスペースに含まれている](https://ja.wikipedia.org/wiki/GNU_Mach "wikilink")\[7\]。

Hurdの開発者によると、マイクロカーネルベースの設計の利点は、システムを拡張することができることである。これは、新しいモジュールを開発するとき、残りの部分のカーネルに関する深い知識を必要とせず、ひとつのモジュールにあるバグがシステム全体をクラッシュさせることもない。Hurdは*translators*という概念を提供しており、これは機能的に[ファイルシステム](../Page/ファイルシステム.md "wikilink")を拡張するモジュールのフレームワークである\[8\]。

### 他のマイクロカーネル

[2004年](../Page/2004年.md "wikilink")以降、Hurdをさらにモダンなマイクロカーネルにポートする努力が行われている。これにはL4マイクロカーネルやCoyotosマイクロカーネルなどを含む\[9\]。

### サーバ群のアーキテクチャ

[Debian](../Page/Debian.md "wikilink")のドキュメンテーションによると、18のコアサーバと6のファイルシステムサーバからなる24のサーバが存在している。それは以下の通りである\[10\]。

#### コアサーバ

  - **auth**（authentication sever）: プログラムからの要求とパスワードを受け取り、それらのプログラムにシステムの権限を変更するIDを与える。
  - **crash**（crash server）: 致命的なエラーをハンドルする
  - **eieio**（translation server）: TODO
  - **exec**（execution server）: 実行可能（executable）なイメージ（現在は[ELF](https://ja.wikipedia.org/wiki/ELF "wikilink")と[a.out](https://ja.wikipedia.org/wiki/a.out "wikilink")がサポートされている）をメモリ上の実行可能なイメージ（runnable）に変換する
  - **fifo**（[FIFO](../Page/FIFO.md "wikilink") translator）: 命名済みパイプを実装する
  - **new-fifo**（new FIFO server）: 命名済みパイプに対する異なるサーバ
  - **firmlink**（the firmlink translator）: firmlinksの実装
  - **fwd**（forward server）: 要求を他のサーバに伝える、fifoとsymlinkサーバによって利用される
  - **hostmux**（host multiplexer sever）
  - **ifsock**（server for sockets interface）: UNIXドメインのソケットアドレスを補助する
  - **init**（[init](https://ja.wikipedia.org/wiki/init "wikilink") server）: 基本的なシステムのブートと設定
  - **magic**（magic server）: プロセスの状態に結果が関係するときに、プロセスによって内部的に行われる必要のある名前解決をシグナルする
  - **null**（null server）: /dev/nullと/dev/zeroの実装
  - **pfinet**（pifnet server）: PF_INETプロトコルファミリの実装
  - **pflocal**（pflocal server）: UNIXドメインソケットの実装
  - **proc**（process server）: PIDを割り当て、プロセスレベルのアクションを管理する
  - **symlink**（symbolic link translator）: ファイルシステムによってサポートされていない場合の[シンボリックリンク](https://ja.wikipedia.org/wiki/シンボリックリンク "wikilink")の実装
  - **term**（terminal server）: [POSIX](../Page/POSIX.md "wikilink")のターミナル
  - **usermux**（user multiplexer server）: ユーザ特有のトランスレータを発動する

#### ファイルシステムサーバ

  - **ext2fs**
    [ext2](https://ja.wikipedia.org/wiki/ext2 "wikilink")ファイルシステムのトランスレータ。ディスクブロックをマイクロカーネルから受け取り、ファイルとディレクトリをアプリケーションに与える。
  - **isofs**
    [ISO 9660ファイルシステムのトランスレータ](../Page/ISO_9660.md "wikilink")。CDやDVDのブロックを、アプリケーションのためのファイルやディレクトリに変換する。
  - **nfs**
    [NFS](https://ja.wikipedia.org/wiki/NFS "wikilink")を参照のこと。
  - **ufs**
    BSDにおける同名のファイルシステム（[UFS](https://ja.wikipedia.org/wiki/UFS "wikilink")）のためのトランスレータ。
  - **ftpfs**
    [FTP](https://ja.wikipedia.org/wiki/FTP "wikilink")プロトコルファイルシステムのトランスレータ
  - **storeio**
    ストレージトランスレータ

サーバは、集合的に[POSIX](../Page/POSIX.md "wikilink") [APIを実装しており](../Page/アプリケーションプログラミングインタフェース.md "wikilink")、それぞれのサーバがインターフェースの一部の実装となっている。例として、様々なファイルシステムサーバは、ファイルシステムコールの実装となっている。ストレージサーバは、ラッピングレイヤーとして機能する。これは[Linux](../Page/Linux.md "wikilink")のブロックレイヤーのようなものである。Linuxの[VFS](https://ja.wikipedia.org/wiki/VFS "wikilink")と同様のものが、libdiskfsとlibpagerによって達成されている。

## 脚注

## 関連項目

  - [GNU Mach](https://ja.wikipedia.org/wiki/GNU_Mach "wikilink")
  - [Linuxカーネル](../Page/Linuxカーネル.md "wikilink")

## 外部リンク

  -
  - [Hurd-JP プロジェクト](http://www.hurd.jp/)

  - [Debian -- Debian GNU/Hurd](http://www.debian.org/ports/hurd/index.ja.html)

[Category:フリーソフトウェアOS](https://ja.wikipedia.org/wiki/Category:フリーソフトウェアOS "wikilink") [Category:OSのカーネル](https://ja.wikipedia.org/wiki/Category:OSのカーネル "wikilink") [Category:Unix系オペレーティングシステム](https://ja.wikipedia.org/wiki/Category:Unix系オペレーティングシステム "wikilink") [Category:GNUプロジェクト](https://ja.wikipedia.org/wiki/Category:GNUプロジェクト "wikilink")

1.  [UNIX](../Page/UNIX.md "wikilink")で言う[デーモン](../Page/デーモン_\(ソフトウェア\).md "wikilink")
2.  現在ストールマン自身は開発に加わっていない
3.  ed. Joshua Gay, *Free Software, Free Society: Selected Essays of Richard Stallman*, Boston: GNU Press, 2002.
4.
5.  4.3BSDのライセンス問題については[BSD](../Page/BSD.md "wikilink")を参照のこと。
6.
7.
8.
9.
10.