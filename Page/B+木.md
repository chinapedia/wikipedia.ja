> この記事は[B+](https://ja.wikipedia.org/wiki/B+)から翻訳されています。


**B+木**（）は、キーを指定することで挿入・検索・削除が効率的に行える[木構造の一種である](../Page/木構造_\(データ構造\).md "wikilink")。動的な階層型インデックスであり、各インデックスセグメント（「ブロック」などと呼ばれる。木構造におけるノードに相当）にはキー数の上限と下限がある。B+木は[B木](../Page/B木.md "wikilink")とは異なり、全てのレコードは木の最下層（葉ノード）に格納され、内部ノードにはキーのみが格納される。

B+木は、特にブロック型記憶装置での効率的データ検索に効果を発揮する。[ブロックサイズ](https://ja.wikipedia.org/wiki/ブロックサイズ "wikilink") \(b\) の記憶装置があるとき、\(b\) の倍数個のキーを格納するB+木は[2分探索木](https://ja.wikipedia.org/wiki/2分探索木 "wikilink")に比較して非常に効率が良い（2分探索木はブロック型でない記憶装置に適している）。

[ReiserFS](https://ja.wikipedia.org/wiki/ReiserFS "wikilink")（[UNIX](../Page/UNIX.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")）、[XFS](../Page/XFS.md "wikilink")（[IRIX](https://ja.wikipedia.org/wiki/IRIX "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")）、[JFS2](https://ja.wikipedia.org/wiki/Journaled_File_System "wikilink")（[AIX](https://ja.wikipedia.org/wiki/AIX "wikilink")、[OS/2](https://ja.wikipedia.org/wiki/OS/2 "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")）、[HammerFS](https://ja.wikipedia.org/wiki/HAMMER "wikilink")（[DragonFly BSD](https://ja.wikipedia.org/wiki/DragonFly_BSD "wikilink")）、[NTFSといった](../Page/NT_File_System.md "wikilink")[ファイルシステム](../Page/ファイルシステム.md "wikilink")はいずれもB+木に類する構造をブロックのインデックス付けに使っている。[関係データベース](https://ja.wikipedia.org/wiki/関係データベース "wikilink")でも表のインデックスにこの種の木構造を使っていることが多い。

## 詳細

B+木の次数は木構造内のノードの容量の尺度である。次数を *d* としたとき、*d* \<= *m* \<= 2 *d* となるような *m* が各ノードのエントリ数となる。例えば、次数7のB+木があるとき、根ノード以外の内部ノードは7個から14個のキーを格納する。根ノードは1個から14個のキーを格納する。

さらに各内部ノードは、最低でも *d*+1 個、最高でも 2*d*+1 個の子ノードを持つ。

### 探索

レコード r を探索するアルゴリズムは、葉ノードに到達するまで正しい子ノードへのポインタを辿っていく。そして、その葉ノード内を調べて、求めているレコードを探す（見つからない場合は失敗となる）。

` `**`function`**` search(record r)`
`   u := 根ノード`
`   `**`while`**` (u は葉でない) `**`do`**
`     そのノード内の正しいポインタを選択`
`     ポインタを辿った先の最初のノードに移動`
`     u := 現在のノード`
`   scan u for r`

この[擬似コード](https://ja.wikipedia.org/wiki/擬似コード "wikilink")は反復がないと仮定している。

## 特徴

次数 *b*、高さ *h* のB+木には以下の特徴がある。

  - 格納できる最大レコード数は \(n = b^h\)
  - 最小キー数は \(2(b/2)^{h-1}\)
  - この木構造を格納するのに要する領域は \(O(n)\)
  - 1つのレコードの挿入に要する操作回数は最悪で \(O(\log_bn)\)
  - 1つのレコードを探すのに要する操作回数は最悪で \(O(\log_bn)\)
  - 位置がわかっているレコードの削除に要する操作回数は最悪で \(O(\log_bn)\)
  - [範囲クエリ](https://ja.wikipedia.org/wiki/範囲クエリ "wikilink")で *k* 個の要素が見つかる場合、要する操作回数は最悪で \(O(\log_bn+k)\)

## 他のデータ構造との関係

B+木（および他のB木やその派生）は[(a,b)-木を特殊化したものである](https://ja.wikipedia.org/wiki/:en:\(a,b\)-tree "wikilink")（(a,b)-木は最大と最小を *a* と *b* というように明示的に指定した木構造）。

B+木は[B木](../Page/B木.md "wikilink")から派生したもので、B木は内部ノードにもキーとレコードを格納できる。また、ある意味ではB木がB+木を特殊化したものと見ることもできる。

[B\#木はB](https://ja.wikipedia.org/wiki/:en:B_sharp_tree "wikilink")+木にさらに制限を加えたものである。

## 実装

B+木の葉ノードは[連結リスト](../Page/連結リスト.md "wikilink")で相互にリンクされていることが多い。これにより[範囲クエリ](https://ja.wikipedia.org/wiki/範囲クエリ "wikilink")が簡単かつ効率的に行える（上述の上限は連結リストがなくとも実現できる）。これによって領域消費量が大幅に増えたり、手間が大幅に増えるということはない。

記憶装置のブロックサイズが *B* [バイトの場合](../Page/バイト_\(情報\).md "wikilink")、格納されるキーのサイズを *k* バイトとすると、最も効率的なB+木では \(b=(B/k)-1\) となる。理論的には1を引く必要はないが、実際にはインデックスブロックには何らかの余分な空間が必要になることが多い（例えば、葉ブロックでの連結リスト用参照）。インデックスブロックがその記憶装置の実際のブロックより若干大きい場合、性能は大幅に低下する。

B+木のノードが配列として構成される場合、挿入や削除で配列の要素をずらす必要が生じ、性能が悪くなる。そのため、ノード内の要素は2分木やB+木で構成するのが望ましい。

B+木はメモリ上のデータ格納にも使われる。その場合、ブロックサイズはプロセッサの[キャッシュラインに合わせるのがよい](../Page/キャッシュメモリ.md "wikilink")。ただし、キャッシュのプリフェッチ機能がある場合、キャッシュラインの何倍かをブロックサイズとした方が性能がよいことが。

B+木の空間効率は、ある種の圧縮技法を使うことで改善できる。例えば、各ブロックに格納するキーに[差分符号化](https://ja.wikipedia.org/wiki/差分符号化 "wikilink")を施すことが考えられる。内部ブロックの場合、領域を節約するにはキーかポインタを圧縮すればよい。文字列キーの場合、領域を節約するには次のようにする。通常、内部ブロックの *i* 番目のエントリには i+1 番のブロックの最初のキーが格納されている。キー全体を格納する代わりに、直前の ｉ 番目のブロックの最後のキーよりも確実に大きいとわかる、i+1 番のブロックの最初のキーの最短のプレフィックスを格納する。ポインタにも簡単な圧縮方法がある。いくつかのブロックが連続する位置に順に配置されている場合、先頭ブロックへのポインタと連続するブロック数を格納すればよい。

上述の圧縮技法にはいずれも何らかの問題が存在する。まず、1つの要素を取り出すにはブロック全体を解凍する必要がある。この問題への対処の1つとして、ブロックをサブブロックに分け、サブブロック単位で圧縮することが考えられる。この場合、要素の挿入や削除ではブロック全体ではなくサブブロックだけを解凍し再圧縮すればよい。また、圧縮率がブロックによって異なると、格納できる要素数も大きく異なってくるという問題もある。

## 歴史

## 関連項目

  - [B木](../Page/B木.md "wikilink")
  - [B\*木](../Page/B*木.md "wikilink")
  - [NTFS](../Page/NT_File_System.md "wikilink")
  - [データベース](../Page/データベース.md "wikilink")
  - [2分探索木](https://ja.wikipedia.org/wiki/2分探索木 "wikilink")
  - [JFS](https://ja.wikipedia.org/wiki/Journaled_File_System "wikilink")
  - [ReiserFS](https://ja.wikipedia.org/wiki/ReiserFS "wikilink")

## 外部リンク

  - [Study notes for B+ Trees - Insertion and Deletion](http://www-users.itlabs.umn.edu/classes/Spring-2006/csci4707/B+Trees.pdf)
  - [Dr. Monge's B+ Tree index notes](http://www.cecs.csulb.edu/%7emonge/classes/share/B+TreeIndexes.html)
  - [Link to how BTrees work](http://www.virtualmachinery.com/btreeguide.htm)
  - [Evaluating the performance of CSB+-trees on Mutithreaded Architectures](http://www2.enel.ucalgary.ca/~whassane/papers/CSB+_ccece_2007.pdf)
  - [Effect of node size on the performance of cache conscious B+-trees](http://www.eecs.umich.edu/~jignesh/quickstep/publ/cci.pdf)
  - [Fractal Prefetching B+-trees](http://www.pittsburgh.intel-research.net/people/gibbons/papers/fpbptrees.pdf)
  - [Towards pB+-trees in the field: implementations Choices and performance](http://gemo.futurs.inria.fr/events/EXPDB2006/PAPERS/Jonsson.pdf)
  - [Cache-Conscious Index Structures for Main-Memory Databases](https://oa.doria.fi/bitstream/handle/10024/2906/cachecon.pdf?sequence=1) (PDF)

### 実装

  - [Interactive B+ Tree Implementation in C](http://www.amittai.com/prose/bplustree.html)
  - [Memory based B+ tree implementation as C++ template library](http://idlebox.net/2007/stx-btree/)
  - [Stream based B+ tree implementation as C++ template library](http://gitorious.org/bp-tree/main)
  - [Open Source JavaScript B+ Tree Implementation](http://blog.conquex.com/?p=84)
  - \[<https://metacpan.org/module/Tree>::BPTree Perl implementation of B+ trees\]
  - [Java/C\#/Python implementations of B+ trees](http://bplusdotnet.sourceforge.net)
  - [File based B+Tree in C\# with threading and MVCC support](http://csharptest.net/?page_id=563)
  - [JavaScript B+ Tree, MIT License](http://prosehack.wordpress.com/2012/05/25/a-javascript-b-tree/)
  - [JavaScript B+ Tree, Interactive and Open Source](http://goneill.co.nz/btree.php)

[Category:Bツリー](https://ja.wikipedia.org/wiki/Category:Bツリー "wikilink")