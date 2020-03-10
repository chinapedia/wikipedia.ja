> この記事は[PaX](https://ja.wikipedia.org/wiki/PaX)から翻訳されています。


**PaX** は、メモリに関する最小特権保護を実装した[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")向け[コンピュータセキュリティ](../Page/コンピュータセキュリティ.md "wikilink")[パッチ](https://ja.wikipedia.org/wiki/パッチ "wikilink")である。最小特権の手法により、[プログラムは正しい動作以外は何もできなくなる](../Page/プログラム_\(コンピュータ\).md "wikilink")。PaX は2000年にリリースされた。

PaX はデータ用メモリ[ページを実行不可とし](https://ja.wikipedia.org/wiki/ページング方式 "wikilink")、コード用メモリページを書き込み不可にすると共に無作為な配置を行う。これによりセキュリティを危険にさらす様々な動作が不可能になる（[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")の一種など）。データページの実行不可設定により、データをコードとして実行できなくなる。コードページの書き込み不可設定により、不正なライブラリ実行が難しくなる。ただし、変数やポインタの書き換えは防げない。

PaX は **The PaX Team** が保守しているが、個々の開発者は匿名である。

[thumbの](https://ja.wikipedia.org/wiki/ファイル:Pax_tux.png "wikilink")[マスコット](https://ja.wikipedia.org/wiki/マスコット "wikilink")、[タックス](https://ja.wikipedia.org/wiki/タックス "wikilink")の PaX 版\]\]

## 意義

コンピュータのセキュリティ問題の大半は、実行時に何かを書き換えられるような抜け穴（[バグ](../Page/バグ.md "wikilink")であることが多い）がプログラムにあることが原因である。[Ubuntu](https://ja.wikipedia.org/wiki/Ubuntu "wikilink")の初期の44通の Security Notice を分類すると[1](https://wiki.ubuntu.com/USNAnalysis)、41%は[バッファオーバーラン](https://ja.wikipedia.org/wiki/バッファオーバーラン "wikilink")を原因とする脆弱性、11.4%は整数オーバフロー、15.9%は不正データの処理上の問題であった。これらのバグを悪用すると、外部からコードを注入して実行させたり、既存コードを不正な順序で実行させることができる。なお、この分析は非常に簡単なものであって、詳細に脆弱性を分析すれば結果は変わってくるだろう。

[ワームや](https://ja.wikipedia.org/wiki/ワーム_\(コンピュータ\) "wikilink")[コンピュータウイルス](https://ja.wikipedia.org/wiki/コンピュータウイルス "wikilink")などの攻撃の多くは、メモリの内容を書き換えて[マルウェア](https://ja.wikipedia.org/wiki/マルウェア "wikilink")コードを実行できるようにすることで行われる。あるいは、データを実行するよう誘導するなどの手法がある。そのようなマルウェアの実行をブロックできれば、そのような侵入によって損害を被る可能性は激減する。[Sasser](https://ja.wikipedia.org/wiki/Sasser "wikilink")のようなワームもそれによって対処可能である。

PaX は、そのような様々な攻撃を防ぐため、非常に汎用的な方法で防御するよう設計された。メモリのアクセス権（リード、ライト、実行の組合せ）を制御することで不正コードの実行を防ぎ、同時に正当なコードの実行には影響を与えないよう設計されている。若干のオーバーヘッドはあるが、PaX は[DoS攻撃](https://ja.wikipedia.org/wiki/DoS攻撃 "wikilink")や外部からのコード注入制御の可能性を減らし、攻撃者に[スーパーユーザー](https://ja.wikipedia.org/wiki/スーパーユーザー "wikilink")特権を与えるのを防ぎ、ハードディスク上の重要な情報へのアクセスを防ぎ、単に影響を受けたプログラムや[プロセス](../Page/プロセス.md "wikilink")がクラッシュするだけで済む。

DoS攻撃は、実行されるだけで迷惑であり、[リソースや時間の浪費となる](https://ja.wikipedia.org/wiki/計算資源 "wikilink")（企業のウェブサイトが攻撃された場合、ビジネス機会が失われる）。しかし、PaX があればデータを書き換えられたり、情報を外部にコピーされたりすることがなくなる。ただし環境によっては DoS 攻撃の類は攻撃されること自体が許容されない。[サービス水準合意](https://ja.wikipedia.org/wiki/サービス水準合意 "wikilink")などの契約条件では、侵入者によるサービス低下が単なるコスト問題以上の契約違反として扱われる。それでも多くの場合、セキュリティを強化して重要な情報を保護することには意味がある。

多くの[バグ](../Page/バグ.md "wikilink")はメモリ破壊の原因となる。そのようなバグを利用して、プログラムが意図していない動作をさせることが可能となる。PaX はそのようなバグの検出や修正が可能なわけではなく、そのようなバグを利用した悪意ある攻撃を防ぐことにある。そのようなバグの一部は深刻度が減じられ、不正な動作をする代わりにプログラムを終了させる。

PaX はバッファオーバーフローを直接防ぐことはできないが、それを利用して不正なアクセスを行おうとするのを効果的に防ぐ。Stack Smashing Protector や StackGuard はバッファオーバフローそのものを検出し、そのような動作をしようとしたプログラムを終了させる。このような手法を [Stack Smashing Protection](https://ja.wikipedia.org/wiki/Stack_Smashing_Protection "wikilink") と呼び、実際にオーバフロー状態となる前に防ぐ。一方 PaX はより汎用的な手法であり、オーバフローが発生してから実際のダメージが発生するのを防ぐ。どちらの手法でも結果的には同じ効果が得られるが、完全に重複する手法というわけではない。従って、両方の手法を同時に使うことで、システムをより安全にすることが（原理的には）可能である。一部の[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")では、PaX と Stack Smashing Protection の両方を採用している。

2004年中ごろ、PaXは[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")のメインのソースツリーには含まれていなかった。これは、PaXチームがPaXを不完全であると考えていたためである。[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")を含む多くの[CPU](../Page/CPU.md "wikilink")アーキテクチャでは完全に機能しているが、いくつかのアーキテクチャでは部分的にしか実装されていないか、全く実装されていない。PaXが実装されているアーキテクチャとしては、[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink") (x86)、[AMD64](https://ja.wikipedia.org/wiki/x64 "wikilink")、[IA-64](https://ja.wikipedia.org/wiki/IA-64 "wikilink")、[Alpha](https://ja.wikipedia.org/wiki/DEC_Alpha "wikilink")、[PA-RISC](https://ja.wikipedia.org/wiki/PA-RISC "wikilink")、[MIPS](https://ja.wikipedia.org/wiki/MIPSアーキテクチャ "wikilink")、[PowerPC](../Page/PowerPC.md "wikilink")、[SPARC](../Page/SPARC.md "wikilink") がある。

### 限界

PaXは実行ファイルや[カーネル](../Page/カーネル.md "wikilink")に潜在する基本的な設計ミスに対処することはできない。それは例えば、原理的に検出不可能な方法で攻撃可能とするような問題である。例えば、[スクリプト言語](../Page/スクリプト言語.md "wikilink")の[インタプリタ](../Page/インタプリタ.md "wikilink")はファイルやネットワークにアクセスできるため、悪意あるスクリプトを使って特権ユーザーのアカウントを通して重要データを盗むことも可能である。PaXは[書式文字列攻撃](../Page/書式文字列攻撃.md "wikilink")の一部も防げない。書式文字列攻撃では、既存のコードを使って任意のデータ位置の読み書きが可能であり、攻撃者は内部のアドレスを事前に知っておく必要がなく、攻撃用コードを注入する必要もない。

PaXの公式サイトにある文書\[[http://pax.grsecurity.net/docs/pax.txt\]では、PaXが防ごうとしている攻撃を三種類としている。その文書によれば、PaX](http://pax.grsecurity.net/docs/pax.txt%5Dでは、PaXが防ごうとしている攻撃を三種類としている。その文書によれば、PaX) はそれらを効果的に防ぐことができるが、それ以外の攻撃は防ぐことはできない。実行コード領域の保護が可能で、そのベースを任意のアドレスにでき、完全なアドレス空間ランダム化が可能であることが前提である。防ぐことができる攻撃は大まかに言えば、次の通りである。

1.  何らかのコードを導入し実行する攻撃。いわゆる[シェルコード](https://ja.wikipedia.org/wiki/シェルコード "wikilink")であることが多い。
2.  プログラマが意図していない不正な順序で既存のコードを実行させる攻撃。[return-to-libc攻撃](https://ja.wikipedia.org/wiki/return-to-libc攻撃 "wikilink")と呼ばれる。
3.  既存のコードを正しい順序で実行させるが、適当なデータを与えることで望みの動作をさせる攻撃。1.1.4-a 以前の [zlib](https://ja.wikipedia.org/wiki/zlib "wikilink") にこの問題があることが知られている。

PaX はこれらの攻撃の元となるバグを検出・対処できるわけではなく、単に攻撃によるダメージを防ぐものであるため、あらゆる攻撃を防ぐことができるわけではない。実際、[ライスの定理](../Page/ライスの定理.md "wikilink")により、あらゆる攻撃を防ぐことは不可能とされている。

3つ目の攻撃は、攻撃対象のアドレスを知る必要がない場合、PaXを使っても全く防ぐことができない。また、2つ目と3つ目の攻撃は、攻撃対象のアドレス空間配置を知る必要がある場合、それを攻撃対象のアドレス空間を読み取ることで知ることができるなら、PaX を使っても防ぐことができない。これは、攻撃対象が [/proc/(pid)/maps](https://ja.wikipedia.org/wiki/procfs "wikilink") にあるような情報を漏らすようなバグを持っていると可能になる。ユーザーランドでプロセスのアドレス空間配置などの情報を見えないようにするパッチもあるが、それは PaX には含まれていない。

事前にアドレス空間配置に関する知識が必要なら、2つ目と3つ目の攻撃は推測や力ずくの探索を行わなければ、ほとんど不可能である。ASLRの文書\[[http://pax.grsecurity.net/docs/aslr.txt\]には、そのような攻撃が成功する「小さな可能性」をさらに詳しく解説している](http://pax.grsecurity.net/docs/aslr.txt%5Dには、そのような攻撃が成功する「小さな可能性」をさらに詳しく解説している)。

1つ目の攻撃は、攻撃者が攻撃対象のタスクを生成でき、それに書き込むことができ、[mmap](https://ja.wikipedia.org/wiki/mmap "wikilink")()でファイルをマッピングできる場合に可能となる。すると、二次攻撃が可能でなければ攻撃は成功しないため、そこまで分析する必要がある。PaX には含まれないが、この種の攻撃の可能性を減じるには、[アクセス制御](https://ja.wikipedia.org/wiki/アクセス制御 "wikilink")を正しく設定しておく必要がある。

PaXを使ったとしても[システムアドミニストレータ](https://ja.wikipedia.org/wiki/システムアドミニストレータ "wikilink")による管理は必要である。PaXはメモリ破壊バグを利用した攻撃を防ぐ。PaXが防ぐことができる攻撃の多くは、バッファオーバーフローを起こすバグに関連している。これは、メモリ管理関連の問題を利用した攻撃の典型的な部分を占める。ただし、PaXは全てのそのような攻撃を防ぐわけではない。

## PaX が提供する機能

PaX が提供するのは[NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")（あるいはそれに相当する各[CPU](../Page/CPU.md "wikilink")/[MMUアーキテクチャにある機能](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink")）の機能を使った（あるいはそれをOSで[エミュレート](https://ja.wikipedia.org/wiki/エミュレート "wikilink")した）[メモリ保護機能](https://ja.wikipedia.org/wiki/メモリ保護機能 "wikilink")である。また、return-to-libc攻撃や、メモリ空間配置に関する知識に依存した攻撃を防ぐため、アドレス空間配置のランダム化を行う。

### 実行空間保護

[thumb](https://ja.wikipedia.org/wiki/ファイル:Program_datacode.png "wikilink") PaX の主要機能は**実行空間保護**である。一部プロセッサにあるNXビットの機能を用いて任意のコードの実行を防ぐ。それによって、コード注入やシェルコードといった攻撃を防ぐ。NXビットを持たない[IA-32](https://ja.wikipedia.org/wiki/IA-32 "wikilink")系[CPU](../Page/CPU.md "wikilink")では、PaX はその機能を様々な手段でエミュレートできる。

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")を含む多くの[OSでは](../Page/オペレーティングシステム.md "wikilink")、ハードウェアのNXビットの機能を利用して、メモリのアクセス権を適切に設定する。**図1**は、1つのロードされたライブラリのあるプログラムのメモリセグメント群を簡単に図示したものである。緑のセグメントはデータで、青のセグメントはコードである。一般に、[AMD64なども含めたプロセッサでのアドレス空間は](https://ja.wikipedia.org/wiki/x64 "wikilink")、デフォルトでは図1のように明確にデータ部とコード部が定義されている。しかし、Linux ではデフォルトではアプリケーションが自身のメモリ保護設定を変更することを防ぐことができず、コード部を書き込み可能にしたり、データ部をコードとして実行することが可能となっている。PaX はそのような変更を防ぐとともに、典型的な操作に最適な最も制限のきつい保護設定を保証する。

実行空間保護が起動しているとき、[mprotect](https://ja.wikipedia.org/wiki/mprotect "wikilink")() 制限も含まれ、PaX は本来コード部でなかった領域を実行可能にするような操作を不可能にする。これにより、書き込み可能だったことのある領域に存在するコードは実行不能となり、悪意があるかどうかとは関係なく、コードを後から注入することが不可能となる。

すると、[Java](https://ja.wikipedia.org/wiki/Java "wikilink")の[ジャストインタイムコンパイル方式](https://ja.wikipedia.org/wiki/ジャストインタイムコンパイル方式 "wikilink")のように、実行時にコードを生成して実行する必要のあるアプリケーションは動作できなくなる。しかし多くの場合、そのような機能を必要としているプログラムは、それに依存しないように書き換えることが可能である。根本的に実行時のコード生成が必要なものについては、システムアドミニストレータがその実行ファイルに印を付け、その実行ファイルについては制限が課せられないようにすることができる。

PaX チームは [mmap](https://ja.wikipedia.org/wiki/mmap "wikilink")() [システムコール](https://ja.wikipedia.org/wiki/システムコール "wikilink")をどう扱うかを決定する必要に迫られた。mmap は[共有メモリ](../Page/共有メモリ.md "wikilink")のマッピングや共有ライブラリのロードに使われる。そのため、使われている状況によっては書き込み可能な[ページや実行可能なページを生成できるようにしなければならない](https://ja.wikipedia.org/wiki/ページング方式 "wikilink")。PaX の現在の実装では、デフォルトで書き込み可能な無名メモリページのマッピングが可能となっている。ファイルのマッピングは mmap() コールが書き込みのパーミッションを指定している場合のみ書き込み可能にできる。mmap() は書き込みと実行が同時に可能なマッピングを生成しない。これは引数で明示的に指示されている場合でもエラーとなる。

#### 実行不可ページの厳格化

デフォルトでは、Linux はNXビットを使って実行不可ページを正しく設定することはしていない。しかも、アーキテクチャによってはNXビットと同等の機能を持たないものもある。PaX は実行不可なページをなるべく実際に実行不可とする[セキュリティポリシーに従って](https://ja.wikipedia.org/wiki/情報セキュリティポリシー "wikilink")、設定を行う。

さらに、CPU がNXビット相当の機能を提供していないとしても、PaX は同等機能をいくつかの手法で提供（エミュレート）する。エミュレートによって性能は低下するが、セキュリティは向上する。しかも、一部の手法のオーバーヘッドは無視できるほど小さい。

##### PAGEEXEC

PAGEEXEC は NXビットを使うか、エミュレートする。NXビットがサポートされていないプロセッサの場合、各ページにエミュレートされたNXビットが付与される。その具体的方法はCPUのアーキテクチャに依存する。NXビットのあるプロセッサでは、PAGEEXEC は単にそれを使い性能をなるべく低下させないようにしている。

IA-32 では、NXビットのエミュレーションは実行不可ページのパーミッションレベルを変更することで行われる。この場合、あるページを実行しようとして、同時にそれが[TLBにキャッシュされていなければ](https://ja.wikipedia.org/wiki/トランスレーション・ルックアサイド・バッファ "wikilink")、プロテクション例外が発生する。IA-32 では[メモリ管理ユニット](https://ja.wikipedia.org/wiki/メモリ管理ユニット "wikilink")がこれをOSに通知する。実行コード用TLBとデータ用TLBは分離されているのが一般的であり、書き込み可能なページを初めて実行しようとしたとき、必ずLinuxカーネルとPaXがそれを検出できる。この例外を検出すると、プロセスを終了させるか、実行を継続できるようTLBを設定するかをカーネルが選択する。

PAGEEXEC は仮想空間を2つに分けることがないという利点がある。しかし、エミュレーションは後述の SEGMEXEC より遅く、場合によっては深刻な性能低下を招く。

2004年5月に登場した新たなIA-32用 PAGEEXEC は、実行可能ページの最高の仮想アドレスを覚えておき、それより大きなアドレスのページはユーザーページとする。これにより、スタックなどの高位のアドレスにある領域は性能低下なしに処理され、低位のアドレスにある領域は従来通りに処理される。これは、[Exec Shield](https://ja.wikipedia.org/wiki/Exec_Shield "wikilink") や [OpenBSD](../Page/OpenBSD.md "wikilink") の W^X (Write XOR Execute) 実装に似ている。

##### SEGMEXEC

SEGMEXEC は、IA-32 向けのNXビットエミュレーションであり、アドレス空間を2つに分割し、コードを両方の空間にマッピング（ミラーリング）する。命令フェッチの際、分割を跨いでアドレス変換が行われる。コードがそこにマッピングされていなければ、プログラムは終了させられる。

SEGMEXEC は仮想空間の大きさを半分にしてしまう。通常、個々のプロセスの仮想空間は 3GiB ある。SEGMEXEC を使うと、それが 1.5GiB ずつに分割され、一方がミラーリングに使われる。そのような問題はあるが、エミュレーション時の性能低下は少ない。2つの仮想空間にマッピングされる物理メモリは同じ実体であるため、メモリ使用量が増加することはない。

#### mprotect() の制限

PaX は、あるメモリページが書き込み可能でかつ実行可能とならないことを保証する。mprotect() という関数は、メモリ領域のパーミッションを変更する機能を持つ。[Single UNIX Specification](https://ja.wikipedia.org/wiki/Single_UNIX_Specification "wikilink") では、mprotect() について以下のように記述されている。

  -
    「prot で指定されたアクセス型の組合せをサポートできない実装である場合、mprotect() コールは失敗するだろう」

PaX では、mprotect() で PROT_WRITE と PROT_EXEC を同時に指定できないよう制限している。そのような mprotect() コールには EACCESS というエラーが返される。これにより、単純なコード注入攻撃を防ぐ。また、PROT_EXEC が既に ON になっていないページについて PROT_EXEC を ON にする mprotect() コールも失敗する。これは、予めコードを書き込んだデータ用ページを後から実行可能にするような攻撃を防ぐ。

mprotect() の制限を ON にしていると、プログラムは PaX が最初に設定したメモリ確保のポリシーを逸脱するような動作が不可能となる。これをしないで実行不可ページを厳密に実行不可にしても、あまり意味がない。

#### トランポリン・エミュレーション

トランポリンとは、[GNUコンパイラコレクション](../Page/GNUコンパイラコレクション.md "wikilink")で実装されているもので、[コールスタック](https://ja.wikipedia.org/wiki/コールスタック "wikilink")上に実行時に小さなコードを生成するものである。つまり、トランポリンはスタック上のメモリを実行可とする必要があり、PaX ではそのようなプログラムは終了させられてしまう。

トランポリンは[自己書き換えコード](https://ja.wikipedia.org/wiki/自己書き換えコード "wikilink")の一種であるため、PaX にひっかかり、プログラムの終了を招く。PaX はこれを防ぐため、トランポリン生成を識別し、その実行を許可するようになっている。しかし、これはセキュリティを弱める可能性があるとされている。

### アドレス空間配置のランダム化

**[アドレス空間配置のランダム化](https://ja.wikipedia.org/wiki/アドレス空間配置のランダム化 "wikilink")**（ASLR）は、アドレス空間配置に関する知識を利用した攻撃に対処する技法である。それは、既存のコードをプログラマが意図しない順序で実行させる攻撃である。

[left](https://ja.wikipedia.org/wiki/ファイル:Vmem_aslr.png "wikilink") PaX におけるASLRは[スタック領域と](https://ja.wikipedia.org/wiki/コールスタック "wikilink")[ヒープ領域](https://ja.wikipedia.org/wiki/ヒープ領域 "wikilink")のベースアドレスを[プロセス](../Page/プロセス.md "wikilink")毎に無作為に変化させる。また、オプションで mmap() や実行コード部のベースアドレスもランダム化する。これにより攻撃側が攻撃すべき位置を推測するのが難しくなる。

**図2**は、アドレス空間配置のランダム化を施したアドレス空間を図示したものである。点線と矢印で示された部分が仮想空間上の各領域間のランダムな空隙を示している。[カーネル](../Page/カーネル.md "wikilink")がプロセスを初期化するとき、これら矢印の長さが無作為に変化させられる（各領域の並び順は基本的に変わらない）。

プログラムの実行中、ヒープ領域は[メモリアドレス](https://ja.wikipedia.org/wiki/メモリアドレス "wikilink")の大きい方に成長していく。逆にスタックはアドレスの小さい方に成長していく。これらの領域を各プログラムがどれだけ必要とするかはOSには不明である。いわゆる[プラグイン](../Page/プラグイン.md "wikilink")などの動的ライブラリを実行中にロードする場合、通常はヒープの前に置かれる。OSまたはプログラムはそれらライブラリを配置するのに適切なオフセットを選択しなければならない。PaX はアドレスの[MSB側の部分をランダム化しない](https://ja.wikipedia.org/wiki/最上位ビット "wikilink")。これによって大まかな配置が守られ、各領域が重ならないようにする。

ランダム化の効果は CPU に依存する。32ビットのCPUでは、一般に仮想アドレスは32ビットであり、4GiB の空間にアクセス可能である。Linux は先頭 1GiB をカーネル用に使っているため、ユーザープロセスが使えるのは 3GiB である。SEGMEXEC はこれを半分に分割するので、ランダム化は 1.5GiB の範囲で行われる。ページサイズは 4KiB であり、ランダム化はページサイズ単位に行われる。MSB側の4ビットはランダム化されないので、ヒープ領域は仮想空間の先頭に、スタック領域は最後尾に配置される。このため、ヒープやスタックのランダム化される範囲は16ビット程度で表される範囲になる。

64ビットCPUでは、仮想空間はより大きくなる。従って、ランダム化はさらに大胆に行われることになり、攻撃される可能性がそれだけ少なくなると言える。

#### スタックベースのランダム化

PaX は、[スタックのベースアドレス](https://ja.wikipedia.org/wiki/コールスタック "wikilink")（のオフセット）を16バイト単位にランダム化し、同時にセグメントの配置をページ単位の空隙の大きさをランダム化する。全体としてのランダム化の程度は仮想空間サイズに依存する。例えば、32ビットの場合、スタックベースは256MiBの範囲のどこかに設定され、可能な位置は1600万通り、エントロピーは24ビットとなる。

[300px](https://ja.wikipedia.org/wiki/ファイル:Aslr_stack_smash.svg "wikilink") スタックベースのランダム化は、[シェルコード](https://ja.wikipedia.org/wiki/シェルコード "wikilink")と[return-to-libc攻撃](https://ja.wikipedia.org/wiki/return-to-libc攻撃 "wikilink")のペイロードに影響を与える。シェルコード攻撃はスタック上のリターンポインタをペイロード内を指すよう変更しようとする。一方、return-to-libc攻撃はスタック上のフレームポインタを書き換えようとする。どちらにしても、成功する可能性は大幅に減る。スタックの位置は予測不可能となり、ペイロードによる書き換えは単にプログラムをクラッシュさせる結果となる。

シェルコードの場合、ペイロードの前に[NOP](../Page/NOP.md "wikilink")命令（何もしない命令）をたくさん並べておくことがある。こうすることで、ジャンプ先が予測と多少違っても攻撃が成功するようになる。しかし、16バイトぶんのNOP命令を並べても、成功確率は1/16Mから2/16Mになるだけである。また、128バイトのNOP命令を並べても、成功確率は9/16Mにしかならない。成功確率はNOP命令数に比例する。

return-to-libc攻撃はコードを書き込むわけではなく、ある固定幅のスタックフレームを書き換える。このため、スタックフレームは正確に16バイト境界に配置されていなければならない。一般にスタックフレームは16バイトよりも大きいので、スタックフレームを繰り返し書き込むことで成功確率を上げようとする。

#### mmap() ベースのランダム化

[POSIX](../Page/POSIX.md "wikilink")では、[mmap](https://ja.wikipedia.org/wiki/mmap "wikilink")() システムコールはプロセスが指定したオフセットか[カーネル](../Page/カーネル.md "wikilink")が選択したオフセットにメモリを配置する。無名メモリを使えば、中身のないメモリがマッピングされ、ファイルを指定すればその中身がマッピングされる。ダイナミックリンク[ライブラリ](../Page/ライブラリ.md "wikilink")は mmap() を使ってロードされ、コード部とライブラリのデータ部がそれぞれマッピングされる。データ部に書き込みがあれば、[コピーオンライト](https://ja.wikipedia.org/wiki/コピーオンライト "wikilink")の要領で無名メモリへのコピーが行われる。

mmap() では、仮想空間上のマッピングすべきオフセットを指定することもある。オフセットが指定されないと、OSが自動的に選択する。Linux のオフセット計算方法は予測可能であり、事前に定義された「mmap()ベース」を始点として計算される。このため、プロセスを起動したときに必ずロードされる[標準Cライブラリ](https://ja.wikipedia.org/wiki/標準Cライブラリ "wikilink")（あるいは libc）は常に同じアドレスにロードされる。

mmap()ベースのランダム化を行う場合、PaX はmmap()ベースをランダムにシフトさせ、全てのライブラリおよび他のmmap()コールでのマッピング位置を変えてしまう。このため、ダイナミックリンクされるコード（共有オブジェクト）は毎回ランダムに異なる位置にマッピングされる。攻撃者は特定のライブラリが特定のアドレスにロードされていることを当てにしていることが多い。従って、この機能によって[return-to-libc攻撃](https://ja.wikipedia.org/wiki/return-to-libc攻撃 "wikilink")が困難となる。ただし、[シェルコード](https://ja.wikipedia.org/wiki/シェルコード "wikilink")を使った攻撃では GOT（global offset table）を参照することで任意の関数のアドレスを参照可能である。

PaX はライブラリのロード順序は変化させない。従って、1つのライブラリのアドレスがわかれば、他の全てのライブラリの位置もわかってしまう。しかし、もっと重大な問題として、いったんライブラリの位置がわかってしまうと、他のランダム化をしていても意味がないという問題がある（シェルコードはライブラリ内の関数のアドレスさえ分かれば攻撃可能）。

ET_DYN 型の実行ファイル（PIC化されたライブラリ）をロードするとき、そのベースアドレスもランダム化される（mmap() を使うので通常の共有オブジェクトと同じである）。

スタックを実行不可にする機能と mmap() のランダム化を組み合わせると、[return-to-libc攻撃](https://ja.wikipedia.org/wiki/return-to-libc攻撃 "wikilink")の成功確率は激減する。32ビットシステムでは、本来の確率の16分の1になる。さらにスタックベースのランダム化を加えると、もっと攻撃が困難になる。

#### ET_EXEC ベースのランダム化

PaX は通常の配置アドレスが固定のコードもランダム配置可能であるが、若干問題がある。第一に、性能低下を招くことがある。第二にPaXがプロセスを予期しない理由で終了させてしまうという問題が発生することがある。従って、ET_DYN（ダイナミックリンクライブラリのファイル型）でコンパイルすることが推奨されている（その場合、完全なPICコードになるため）。

また、本来固定であるはずの ET_EXEC ベースのランダム化を行うと、PaX のVMミラーリングに起因するセキュリティ問題を引き起こす。対処していない古い PaX を使うときは、SEGMEXEC によるNXビット・エミュレーションをOFFにし、RANDEXEC による実行アドレスベースのランダム化をOFFにすることで対処する必要がある。

### 実行ファイルマーキング

PaX は、[ELF形式の実行ファイルに印を付ける](https://ja.wikipedia.org/wiki/Executable_and_Linkable_Format "wikilink") **chpax** や **paxctl** というツールを備えている。これらはELFヘッダ部に印を付けるので、[ファイルシステム](../Page/ファイルシステム.md "wikilink")に依存することなく、実行ファイル自身に印を付けることができる。つまり、パッケージ化やコピー、[暗号](../Page/暗号.md "wikilink")化などにおいても印が保持される。

PaX は実行ファイルについて、PAGEEXEC、SEGMEXEC、mmap()のランダム化、スタックのランダム化、ヒープのランダム化、ET_EXEC のランダム化、mprotect()の制限、トランポリン・エミュレーションという機能のON/OFFをマーキング可能である。

chpax では strip などでマーキングが消されることがあるので、paxctl で PT_PAX_FLAGS を設定するのが最も安全である。paxctl は PaX 用フラグを組み込んだ新たなELFプログラムヘッダ形式を使っている。各フラグはON/OFF/未設定の状態がある。未設定の場合どうするかは、カーネル内のPaXコードが設定に基づいて判断する。

## 歴史

  - 2000年10月 - PAGEEXEC の基本部が PaX として初めてリリースされる。
  - 2000年11月 - MPROTECT の最初のリリース
  - 2001年6月 - ASLR（mmap のランダム化）が実装された。リリースはされていない。
  - 2001年7月 - ASLR リリース
  - 2001年8月 - ASLR にスタックと PIE のランダム化を付加したものがリリース
  - 2002年7月 - VMAミラーリングとRANDEXECリリース
  - 2002年10月 - SEGMEXECリリース、ASLR にカーネルスタックのランダム化を付加したものがリリース
  - 2003年2月 - EI_PAX ELF マーキング導入
  - 2003年4月 - KERNEXEC リリース
  - 2003年7月 - ASLR に brk ランダム化を付加したものがリリース
  - 2004年2月 - PT_PAX_FLAGS_ELF マーキング導入
  - 2004年5月 - PAGEEXEC をコードセグメントに限定することで性能強化
  - 2005年3月 - VMAミラーリングの脆弱性が報告され、新たな PaX と [grsecurity](https://ja.wikipedia.org/wiki/grsecurity "wikilink") がリリースされた。それ以前の SEGMEXEC と RANDEXEC を使ったバージョンは脆弱性があるとされた。
  - 2005年4月 - 脆弱性問題から、PaX を新たな開発者に引き継ぐことが予定されていたが、立候補者が現れず、従来の開発者らが保守を続けている。

## 関連項目

  - [Exec Shield](https://ja.wikipedia.org/wiki/Exec_Shield "wikilink")
  - [Security-Enhanced Linux](https://ja.wikipedia.org/wiki/Security-Enhanced_Linux "wikilink")
  - [NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")
  - [侵入検知システム](https://ja.wikipedia.org/wiki/侵入検知システム "wikilink")
  - [侵入防止システム](https://ja.wikipedia.org/wiki/侵入防止システム "wikilink")
  - [RSBAC](https://ja.wikipedia.org/wiki/ルールセットベースアクセスコントロール "wikilink")
  - [grsecurity](https://ja.wikipedia.org/wiki/grsecurity "wikilink")

## 参考文献

  - [PaX 文書](http://pax.grsecurity.net/docs/)

## 外部リンク

  - [PaX 公式サイト](http://pax.grsecurity.net/) （2007年以降の活動は低調）
  - [Presentation on PaX](http://grsecurity.net/PaX-presentation_files/frame.htm) undated
  - [Trampolines for Nested Functions](http://gcc.gnu.org/onlinedocs/gccint/Trampolines.html)
  - [Exploit Mitigation Techniques](http://cvs.openbsd.org/papers/auug04/index.html) 2004年
  - [Ubuntu Linux USN Analysis](http://www.ubuntulinux.org/wiki/USNAnalysis)
  - [PaX privilege elevation security bug](http://fist.immunitysec.com/pipermail/dailydave/2005-March/001619.html) 2005年3月9日

[Category:セキュリティソフト](https://ja.wikipedia.org/wiki/Category:セキュリティソフト "wikilink") [Category:Linux](https://ja.wikipedia.org/wiki/Category:Linux "wikilink")