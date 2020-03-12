> この記事は[Capability-based security](https://ja.wikipedia.org/wiki/Capability-based_security)から翻訳されています。


**Capability-based security** は、[セキュリティの高い](../Page/コンピュータセキュリティ.md "wikilink")（セキュアな）[コンピュータ](../Page/コンピュータ.md "wikilink")を設計するための[コンセプト](https://ja.wikipedia.org/wiki/コンセプト "wikilink")の一つである。

## 設計原理

*Capability-based security* はユーザアプリケーションを設計するためのコンセプトで、それらが「[最小権限の原則](https://ja.wikipedia.org/wiki/最小権限の原則 "wikilink")」 (principle of least privilege) に基づいて直接 capability を分け合う方法でセキュリティを実現する方法をいう。OS側にもそれらのトランザクションを効率的に行い、かつセキュアなものにする下地が必要である。

ほとんどの商用OSでは、capability-based securityは用いられず、そのかわり[アクセス制御リスト](../Page/アクセス制御リスト.md "wikilink")をベースにしたセキュリティが行われる。そこでは、プロセスがあるオブジェクトにアクセスする際、OSに対し非特権的な参照を行い、OSはそれに対しプロセスの利用者情報を元に 、アクセス権を渡すかどうか決定する。capability-based system ではユーザプロセスは非特権的な参照ではなく、特権的 (privileged) な capability を用いる。capability というのは合法的なアクセス法であり、それを持っている時点で、違法アクセスを防止するための利用者特定ステップ等は不要となる。

既にほとんどのOSがこれに似た仕組みを装備している（[ファイル記述子](../Page/ファイル記述子.md "wikilink")、ファイルハンドルなど）が、典型的には capability の交換をサポートしていない。capability-based OSは対照的に、信頼できないエンティティも混じった中で capability の交換を行い、これを最も基本的な方法として、システム全体を通したアクセス権の保証と伝播を実現することを骨子としている。

## Capability-based security入門

Capability は [オブジェクト](https://ja.wikipedia.org/wiki/オブジェクト "wikilink")の一種である。capability を所有しているユーザプロセスに限って、あるオブジェクトと何らかの相互作用を起こすための能力（あるいは名前）を得ることができる。相互作用とは、オブジェクトに関連するデータを読んだり、オブジェクトに変化を加えたり、オブジェクト内のデータをプロセスとして実行したり、といったアクセス権を必要とするような操作をいう。論理的には capability を構成するものは、ある特定のオブジェクトを一意に特定する参照と、一つまたは複数のアクセス権の集合である。

例えば、メモリ内にある一つのユーザプロセスに次のような文字列があるとする:

`    /etc/passwd`

これはシステムの中のあるオブジェクト（パスワードを保管するのに用いられるファイル）を一意に特定するが（つまり上記の「参照」ではある）、アクセス権を特記していないので、capabilityではない。ここで、上記に代わって次の二つの値を考える:

`    /etc/passwd`
`    O_RDWR`

一つのオブジェクトとアクセス権の集合とが一緒になっている（O_RDWRは「読み取り書き込み両用オープン」。パスワードファイルを読んだり変更したりできる状態で開く）。これでもなお capability ではない。というのもユーザプロセスがこれを「所有」したからといって、アクセスが実際に合法的なものになるのかはわからないからである。

さて、新たに次の文を考えよう。ユーザプロセスがこれを成功裡に実行できたとする（open関数はOSから受け取ったファイル記述子を返す。副作用としてファイルを実際に開ける）:

`    int fd = open("/etc/passwd", O_RDWR);`

この時点で変数**fd**はプロセス用ファイル記述子テーブル中のあるファイル記述子への添字を含んでいる。このファイル記述子（具体的にはfd）は capability **である**。このファイル記述子がプロセス用ファイル記述子テーブルに含まれることさえわかれば、そのプロセスにはそのオブジェクト（ここではファイル）への合法的なアクセスを持つことが確実にわかるからである。この方法だと、ファイル記述テーブルが[カーネル](../Page/カーネル.md "wikilink")に存在し、ユーザプログラムからは直接操作できないことに注目して欲しい。OSは、システム内の capability が特定の操作しか受け付けないことを、確実に保障しなければならない。それを怠るとセキュリティポリシーにおけるシステムの一貫性が維持できなくなる。

伝統的なOSではしばしば、プログラムは別のプログラムあるいはストレージと最初の二例のような参照を通して連絡しあう。パス名はコマンドラインパラメタとしてソケットを通してディスクに保存される。これら参照は capability ではなく、使用を許可する前にその有効性を確認しなければならない（あるディレクトリを触るのにパスワードを要求する等）。これらのシステムでは、中心となる質問は「誰の」権限 authority によって「任意の参照を評価することになるか?」である。二つの異なる権限をもったエンティティのために動作するプロセスにおいて、これは危険な問題になり、「混乱した使節の問題」[Confused deputy problemとして知られるバグを引き起こす](../Page/Confused_deputy_problem.md "wikilink")。これは極めてしばしば[セキュリティホール](../Page/セキュリティホール.md "wikilink")の原因になるバグである。

capability-based system では、capability それ自体がプロセスやストレージ間でやりとりされ、やりとりにはOS監視下に一貫性をもって統合されたセキュリティーメカニズムが働く。

## Capability

**Capability** ないし **key** （「鍵」）はセキュアなコンピューティングにおける中核となるコンセプトである。Capability とは、あるオブジェクトを参照するための値と、関連するアクセス権の集合とをセットにしたものである。capability-basedなOS上では、ユーザプログラムは capability なしにオブジェクトにアクセスすることができない。

典型的には capability は特権的なデータ構造 (privilege data structure) として実装される。これはアクセス権を詳細に明示したセクションと、アクセスの対象となるオブジェクトを一意に特定するためのセクションからなる。実際には、capability の使用法は伝統的なOSにおけるファイル記述子（ファイルデスクリプタ）の使用法に良く似ている。しかし伝統的なOSと違い、システム内のいかなるオブジェクトにたいしても capability が要求される。Capability はOS内にリストの形で格納されるのが典型例で、その領域は（ユーザからは）直接操作できないように保護され、参照されるオブジェクトの挿げ替えやアクセス権の乗っ取りなどを防ぐようになっている。

Capability を扱うプログラムは、それらに関数を適用することができ、他のプログラムに渡したり、更に制約の多い（少ない特権しか持たない）バージョンに変換したり、消滅させたりできる。

平文による参照 plain reference の代わりに capability を用いると、システムのセキュリティ向上が実現できる。plain reference （例えば、パス名）は一意にオブジェクトを特定するが、どのようなアクセス権が附随するかを明示しないので、そのオブジェクトにアクセスするのに適当なユーザプログラムが行った参照なのか決めることができない。従って、参照されたオブジェクトへのアクセスは全てOSが審査する必要ができてくる。典型的にはこれは[Access Control List](https://ja.wikipedia.org/wiki/Access_Control_List "wikilink") (ACL)を用いて行う。対照的に純粋なcapability-based OSでは、ユーザプログラムがcapability を持っていること自体が、それが参照するオブジェクトを（capabilityが許す範囲で）操作する権利を持つことになる。理論的にはACLの類いは一切不要になり、capabilityさえあればセキュリティは実現できる。

多くのOSに実装されているファイル記述子ないしファイルハンドルは capability に近い使われ方をしている。例えば[BSD](../Page/BSD.md "wikilink") [UNIX](../Page/UNIX.md "wikilink")では、ファイル記述子は破棄（クローズ）することも、子プロセスに継承することも、[ソケットを通じて他のプロセスに送ることすらできる](../Page/ソケット_\(BSD\).md "wikilink")。しかしながら、純粋なcapability-based OSの全ての利点を受け取るには、このような伝統的なシステムでは問題がある。最大の問題は、capabilityを保持するはずのプロセス、ファイル等の実体を、（capability によって代表される）セキュリティ情報の一貫性を保った形で永続的に維持できないことである。ユーザプログラムがオブジェクトへの参照やアクセス権を改竄しないことを、OS側では信頼することができない。そのため、ユーザプログラムが再度ディスク上にあると参照されているオブジェクトに対しアクセスを試みる際にOSはアクセス要求が正当なものか検査しなければならない。そのためACLや類似のものが必要になる。

実体の永続性がないという問題を解決する新しいアプローチが [orthogonally persistent](https://ja.wikipedia.org/wiki/永続性_\(計算機科学\) "wikilink") OSである（Flexマシンとして実現された。[:en:Ten15](https://ja.wikipedia.org/wiki/:en:Ten15 "wikilink")参照）。この種のシステムでは、実体は破棄される必要がなく、capability も無効になる必要がない。従って後に利用するためcapabilityをとっておくためのACL類似の機構も必要でない。OSは、揮発性のも不揮発性のも、全てのストレージについて常時capabilityの一貫性とセキュリティを維持するが、その一部はシリアル化（ここでは、データ等をネットに流せるようなタイプの一連のビット列に変換すること）作業をOSそれ自体が行い、ユーザプログラムに任せないことによる（ほとんどのOSではユーザプログラムが行う）。そのため、ユーザプログラムが合法的な capability だけを再生産すると信じる必要も、アクセス制御を用いてユーザプログラムからの要求を確認する必要もない。

## 研究用及び商用システム

  - [EROS](https://ja.wikipedia.org/wiki/EROS "wikilink")
      - [KeyKOS](https://ja.wikipedia.org/wiki/KeyKOS "wikilink") - EROS's predecessor
      - [CapROS](https://ja.wikipedia.org/wiki/CapROS "wikilink") - EROS's successor
      - [Coyotos](https://ja.wikipedia.org/wiki/Coyotos "wikilink") - EROS's cousin
  - [Cambridge CAP computer](https://ja.wikipedia.org/wiki/Cambridge_CAP_computer "wikilink")
  - [Carnegie Mellon University](https://ja.wikipedia.org/wiki/Carnegie_Mellon_University "wikilink") [C.mmp](https://ja.wikipedia.org/wiki/C.mmp "wikilink") with Hydra operating system
  - [Carnegie Mellon University](https://ja.wikipedia.org/wiki/Carnegie_Mellon_University "wikilink") CM\* with StarOS
  - IBM [System/38](https://ja.wikipedia.org/wiki/System/38 "wikilink") and [AS/400](https://ja.wikipedia.org/wiki/AS/400 "wikilink")
  - [Intel iAPX 432](../Page/Intel_iAPX_432.md "wikilink")
  - [Plessey System 250](https://ja.wikipedia.org/wiki/Plessey_System_250 "wikilink")
  - [Symbian](https://ja.wikipedia.org/wiki/Symbian "wikilink")
  - [Amoeba分散オペレーティングシステム](https://ja.wikipedia.org/wiki/Amoeba_\(オペレーティングシステム\) "wikilink")

## 参考文献

  - Levy, Henry M., *Capability-Based Computer Systems*, Digital Equipment Corporation 1984. ISBN 0-932376-22-3. An electronic version is available [here](http://www.cs.washington.edu/homes/levy/capabook/).
  - [The EROS Project](http://www.eros-os.org/)
  - [ERights.org](http://www.erights.org/)
  - Mark S. Miller, Ka-Ping Yee, Jonathan Shapiro. *Capability Myths Demolished*, Technical Report SRL2003-02, Systems Research Laboratory, Johns Hopkins University. [Available online.](http://srl.cs.jhu.edu/pubs/SRL2003-02.pdf)
  - [The Cambridge CAP Computer](http://www.cs.washington.edu/homes/levy/capabook/Chapter5.pdf), Levy, 1988

## 外部リンク

  - [Capability Myths Demolished](http://zesty.ca/capmyths/): an analysis that shows (in terms of Equivalence, Confinement and Irrevocability myths) that pure capability systems have significant advantages over [ACL](../Page/アクセス制御リスト.md "wikilink") systems.
  - [What is a Capability?](http://www.eros-os.org/essays/capintro.html): an informal introduction to capabilities.

[Category:コンピュータ・セキュリティ・モデル](https://ja.wikipedia.org/wiki/Category:コンピュータ・セキュリティ・モデル "wikilink")