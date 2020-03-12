> この記事は[Message Passing Interface](https://ja.wikipedia.org/wiki/Message_Passing_Interface)から翻訳されています。


**Message Passing Interface**（メッセージ パッシング インターフェース、**MPI**）とは、[並列コンピューティング](https://ja.wikipedia.org/wiki/並列コンピューティング "wikilink")利用するための標準化された規格である。実装自体を指すこともある。

複数のCPUが情報をバイト列からなるメッセージとして送受信することで協調動作を行えるようにする。自由に使用できる実装としては[MPICH](https://ja.wikipedia.org/wiki/MPICH "wikilink")が有名である。他にも商用ベンダなどによる独自の実装が存在する。

ライブラリレベルでの並列化であるため、言語を問わず利用でき、プログラマが細密なチューニングを行えるというメリットがある一方、利用にあたっては明示的に手続きを記述する必要があり、ロックの対処などもプログラマ側が大きな責任をもたなければならない。

業界団体や研究者らのメンバからなる MPI Forum によって規格が明確に定義されているため、ある環境で作成したプログラムが他の環境でも動作することが期待できる。

## 歴史

MPIへの取り組みは1991年夏にオーストリアの山荘での、小規模な研究者のグループのディスカッションから始まった。その議論は、翌1992年4月29-30日のバージニア州ウィリアムズバーグで、分散メモリ環境のためのメッセージパッシング規格の標準化についてのワークショップに引き継がれた。このワークショップでは標準的なメッセージパッシングインタフェースに必須となるであろう基本的な機能について議論され、標準化に向けてワーキンググループが設立された。[ジャック・ドンガラ](https://ja.wikipedia.org/wiki/ジャック・ドンガラ "wikilink")、Rolf Hempel、Tony Hey、David W. Walkerは1992年11月にドラフトを提案し、これがMPI1となった。1992年11月にはMPIワーキンググループの会議がミネアポリスで行われ、そこで標準化プロセスをより公式な仕組みに乗せることが決められた。MPIワーキンググループは1993年の最初の9ヶ月間は6週ごとにミーティングを行った。MPIのドラフトの標準規格は1993年11月の[スーパーコンピューティング・カンファレンスで発表された](https://ja.wikipedia.org/wiki/Supercomputing_Conference "wikilink")。パブリックコメントの期間を経て、その内容がMPIに反映され、1994年6月にMPI version 1.0がリリースされた。これらのミーティングとE-mailでの議論がMPIフォーラムそのものであり、このフォーラムへの参加の権利はハイパフォーマンスコンピューティング関係者の人たち全員に開かれている。

この頃MPIに対しては欧米の組織を中心に40の組織から約80人の人々が関与していた。大手の並列計算のメーカーの多くが参加していたほか、大学や政府の研究機関や、その他の企業からも研究者が参加していた。

MPIの標準ではコアライブラリの構文と意味論を定義することによって、FortranやCで移植可能なメッセージパッシングを行うプログラムを幅広い分野で作れるようになっている。

MPIは基本的なルーチン群の仕様を明確に定義して並列計算機のメーカーに対して公開しているので、彼らはそれに基づいて効率的に実装を進めることができる。その結果、各メーカーは自社製品のマシンに低レベルのMPI標準に準拠したルーチン群の実装を搭載し、さらにその上に高次の分散メモリ通信環境のルーチンを乗せることができる。MPIは単純かつ基本的で移植可能なプログラムを書くことも可能である一方で、ハイパフォーマンスなメッセージパッシングを先進的な計算機の上で行うようなプログラミングも可能である。

メッセージパッシングの本当の意味での標準を目指そうという考え方に従って、MPIではどれかの製品の機能を標準に採用するというやり方ではなく、いくつかのシステムから最も有用な機能をMPI取り込むというやり方が取られている。各機能はIBM由来、インテル由来、nCUBE由来、PVM由来、Express由来、P4由来、PARMACS由来のものがある。メッセージパッシングという手法が人気があるのは広い移植性と、分散メモリや共有メモリでのマルチプロセッサによる処理、ワークステーションをネットワークで接続したものやそれらすべてのような複合的な環境に対して適用可能なためである。この手法は、様々の構成や、ネットワークの速度、メモリアーキテクチャーに依存せず適用できる。

MPIは、[ARPA](https://ja.wikipedia.org/wiki/ARPA "wikilink")と[アメリカ国立科学財団](../Page/アメリカ国立科学財団.md "wikilink")のグラントASC-9310330、NSF Science and Technology Center Cooperative agreement number CCR-8809615、ヨーロッパではEsprit Project P6643から活動資金を供給されているほか、[テネシー大学](../Page/テネシー大学.md "wikilink")はMPIフォーラムを資金的に支えている。

## 概要

MPIはプログラミング言語とは独立の通信プロトコルで、並列計算機上で動くプログラムに使用される。通信はPoint-to-Pointとグループ通信（Collective communication）の両方がサポートされている。MPIは「メッセージパッシングアプリケーションのためのプログラミングインタフェースで、プロトコルとセマンティクスを定義することで、全ての実装においてその機能がどう振る舞うべきかを仕様として定めている」MPIのゴールはハイパフォーマンス、スケーラビリティ、移植性である。MPIは現在でもハイパフォーマンスコンピューティングにおいてはよく用いられる手法である。

MPIは有名な標準の承認を得た規格ではない。しかしMPIは分散メモリ上で動作する並列計算プログラムのプロセス間通信のモデルとしてはデファクトスタンダードとなっている。実際に、コンピュータークラスターのような構成の分散メモリ型スーパーコンピューター用のプログラムではMPIはよく採用される。MPI-1のモデルは共有メモリを一切必要とせず、MPI-2は限定的に分散共有メモリの概念を導入している。にもかかわらず、MPIのプログラムは共有メモリ型の計算機で使用されることもよくある。これは共有メモリ型のプログラミングのモデルに対して、MPI型のモデルの設計の方が[NUMA](../Page/NUMA.md "wikilink")アーキテクチャーのシステムではメモリアクセスの局所性（[参照の局所性](../Page/参照の局所性.md "wikilink")）などの点で適しているためである。

MPIは[OSI参照モデル](../Page/OSI参照モデル.md "wikilink")の役割にあてはめると、役割としては5層（セッション層）以上に対応すると考えられるが、実際の実装ではソケットとTCP（トランスポート層）を使用しているため、より広い範囲（4 - 7層）をカバーしている。

多くのMPIの実装では、C、C++、Fortranから直接呼ぶことのできるいくつかのルーチンを中心として構成されている。そしてC\#やJava、Pythonなどの他の言語はCなどで作ったライブラリを介せばMPIを利用できる。MPIがMPI制定以前のメッセージパッシングライブラリよりも優れているのは、移植性とスピードである。MPIはほぼ全ての分散メモリ環境で実装されているので、それらの環境間ではどこへでも移植可能で、各ハードウェアに対して実装されるときに最適化されているので高速に動作する。

MPIは言語独立の仕様（Language Independent Specifications; LIS）を採用しているため、どのような言語からでも呼び出せる。最初のMPIの標準はANSI CとFortran-77とのバインディングの仕様とLISであった。ドラフトの仕様は1994年のスーパーコンピューティングのカンファレンスで公開され、その後すぐに承認された。2008年のMPI-1.3は128関数から構成され、それがMPI-１のシリーズでは最後とされている。

MPIは現在ではいくつかのバージョンがあり、1.3（通称MPI-1）は静的な環境下におけるメッセージパッシングのために使用され、MPI-2.2（通称MPI-2）は並列I/Oや動的プロセス管理、遠隔メモリ操作等の新機能を含んでおり、MPI-3.0（通称MPI-3）はグループ通信のノンブロッキング拡張やリモートメモリアクセスの片方向通信の拡張などを含む。

## 実装

初期のMPI 1.xの実装としてはMPICHがあった。MPICHは[アルゴンヌ国立研究所](../Page/アルゴンヌ国立研究所.md "wikilink")（ANL）とを中心とするプロジェクトであった。IBMも初期から実装を提供しており、1990年代初期のスーパーコンピューターのメーカーも商用にMPICHの実装や、自社の実装したものを提供していた。オハイオ スーパーコンピューターセンターのLAM/MPIも初期に公開されていた実装の一つである。ANLは10年以上にわたってMPICHの開発を継続しており、その後MPICH 2に発展し、実装としてはMPI-2.1が提供されるに至っている。LAM/MPIといくつかのプロジェクトはOpenMPIに統合された。

  - [Open MPI](https://ja.wikipedia.org/wiki/Open_MPI "wikilink")
      - いくつかのMPI実装の技術を統合したもので、主には以下のようなよく知られた3プロジェクトの技術が中心となっている。

<!-- end list -->

1.  FT-MPI from the [テネシー大学](../Page/テネシー大学.md "wikilink")
2.  LA-MPI from [ロスアラモス国立研究所](../Page/ロスアラモス国立研究所.md "wikilink")
3.  [LAM/MPI](https://ja.wikipedia.org/wiki/LAM/MPI "wikilink") from [インディアナ大学ブルーミントン校](https://ja.wikipedia.org/wiki/インディアナ大学ブルーミントン校 "wikilink")

<!-- end list -->

  - [Intel MPI Library](http://software.intel.com/en-us/intel-mpi-library/)
      - MPICH2をベースとした実装。
  - [LAM/MPI](http://www.lam-mpi.org/)
  - [MPICH](https://ja.wikipedia.org/wiki/MPICH "wikilink")
  - [MVAPICH](http://mvapich.cse.ohio-state.edu/)
  - [MS MPI](http://www.microsoft.com/japan/technet/WindowsServer/library/4cb68e33-024b-4677-af36-28a1ebe9368f.mspx)

## プログラムの例

以下は "Hello World" プログラムをC言語でMPI対応版として書いたものである。 この例では "hello" メッセージを各プロセッサに送信し、受信したデータを少し改変して結果をメインプロセスに返し、それを画面に表示する。

``` c
 /*
  "Hello World" MPI テストプログラム
 */
 #include <mpi.h>
 #include <stdio.h>
 #include <string.h>

 #define BUFSIZE 128
 #define TAG 0

 int main(int argc, char *argv[])
 {
   char idstr[32];
   char buff[BUFSIZE];
   int numprocs;
   int myid;
   int i;
   MPI_Status stat;
   /* MPI は MPI_Initで開始する。これ以降、全 'N' プロセスが使える */
   MPI_Init(&argc,&argv);
   /* SPMD環境の規模を取得する */
   MPI_Comm_size(MPI_COMM_WORLD,&numprocs);
   /* そしてこのプロセスのランク(番号)は */
   MPI_Comm_rank(MPI_COMM_WORLD,&myid);

   /* この時点で全プログラムは同等に走っており、SPMDモデルの中でこれらを区別する場合には
      ランクで見分ける。ただしランク0のプログラムは特別な処理をしていることもある。... */
   if(myid == 0)
   {
     printf("%d: We have %d processors\n", myid, numprocs);
     for(i=1;i<numprocs;i++)
     {
       sprintf(buff, "Hello %d! ", i);
       MPI_Send(buff, BUFSIZE, MPI_CHAR, i, TAG, MPI_COMM_WORLD);
     }
     for(i=1;i<numprocs;i++)
     {
       MPI_Recv(buff, BUFSIZE, MPI_CHAR, i, TAG, MPI_COMM_WORLD, &stat);
       printf("%d: %s\n", myid, buff);
     }
   }
   else
   {
     /* rank 0から受信: */
     MPI_Recv(buff, BUFSIZE, MPI_CHAR, 0, TAG, MPI_COMM_WORLD, &stat);
     sprintf(idstr, "Processor %d ", myid);
     strncat(buff, idstr, BUFSIZE-1);
     strncat(buff, "reporting for duty", BUFSIZE-1);
     /* rank 0に送信: */
     MPI_Send(buff, BUFSIZE, MPI_CHAR, 0, TAG, MPI_COMM_WORLD);
   }

   /*  MPI FinalizeでMPIのプログラムは終了する。ここは弱い同期ポイント */
   MPI_Finalize();
   return 0;
 }
```

2プロセッサを使用してプログラムを実行すると以下のような結果が得られる\[1\]。

    0: We have 2 processors
    0: Hello 1! Processor 1 reporting for duty

## 脚注

## 外部リンク

  - [Message Passing Interface Forum](http://www.mpi-forum.org/)
  - [The Message Passing Interface (MPI) standard](http://www-unix.mcs.anl.gov/mpi/)
  - [NAG parallel Library](http://www.nag-j.co.jp/nag_lib.htm#nd)
  - [OpenMPI](http://www.open-mpi.org/)

[Category:並列コンピューティング](https://ja.wikipedia.org/wiki/Category:並列コンピューティング "wikilink")

1.  OpenMPIで実行する場合は `gcc -g -v -I/usr/lib/openmpi/include/ -L/usr/lib/openmpi/include/ wiki_mpi_example.c -lmpi` のようにコンパイルして `mpirun -np 2 ./a.out`として実行する。