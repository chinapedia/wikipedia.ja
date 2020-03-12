> この記事は[B](https://ja.wikipedia.org/wiki/B)から翻訳されています。


**B木**（びーき）は、[コンピュータサイエンス](https://ja.wikipedia.org/wiki/コンピュータサイエンス "wikilink")における[データ構造](../Page/データ構造.md "wikilink")、特に[木構造の一つ](../Page/木構造_\(データ構造\).md "wikilink")。ブロック単位のランダムアクセスが可能な[補助記憶装置](../Page/補助記憶装置.md "wikilink")（[ハードディスクドライブ](https://ja.wikipedia.org/wiki/ハードディスクドライブ "wikilink")など）上に木構造を実装するのに適した構造として知られる。

実システムでも多用されており、[データベース管理システム](../Page/データベース管理システム.md "wikilink")の多くはB木による索引を実装している（B木の改良型または亜種である[B+木](../Page/B+木.md "wikilink")や[B\*木](../Page/B*木.md "wikilink")を使うことが多い）。

## 構造

[B-tree_example.svg](https://ja.wikipedia.org/wiki/File:B-tree_example.svg "fig:B-tree_example.svg") 多分岐の平衡木(バランス木)である。1 ノードから最大 *m* 個の枝が出るとき、これをオーダー *m* のB木という。後述する手順に従って操作すると、根と葉を除く「内部ノード」は最低でも *m* /2 の枝を持つことを保証できる。

各ノードは、枝の数 - 1 のキーを持つ。枝<sub>1</sub> ～ 枝<sub>*m*</sub> と キー<sub>1</sub> ～ キー<sub>*m* -1</sub> を持つとき、枝<sub>*i*</sub> には キー<sub>*i* -1</sub> より大きく キー<sub>*i*</sub> より小さいキーだけを保持する（キーの重複を許す場合はどちらかに等号をつける）。

葉ノードの定義は文献によって違いが見られる。木の終端を[ヌルポインタ](https://ja.wikipedia.org/wiki/ヌルポインタ "wikilink")のような特殊な値で表す場合、枝がすべて終端記号となっているノードを葉とする。これに対して一部の文献では、終端を表すためにキーが0個のノードを連結し、このノードを葉と定義している。すなわち、後者の定義における葉ノードの親が、前者の定義における葉ノードとなる。後者の定義をとる文献では「葉ノードはキーを持たない」ということになる。以下の記述では、前者の定義に従うものとする。

ノードはページと呼ばれることもある。特にハードディスクドライブなどの外部記憶装置を使ってB木を実現する場合によく見られる。この場合、各ノード（ページ）のサイズが、外部記憶装置のブロックサイズの整数倍になるようにオーダーを調整することが多い。

B木の中でも特に、オーダー3のものを[2-3木](../Page/2-3木.md "wikilink")、オーダー4のものを[2-3-4木](../Page/2-3-4木.md "wikilink")と呼ぶ。

## 操作

### 検索

実装例を以下に示す。ここでは簡単のため、ノードの中を探索するのに線形探索を使っているが、ノードに含まれるキーの数が多い場合には[二分探索](../Page/二分探索.md "wikilink")を使うことで高速化できる可能性がある。

1.  根を対象ノードとして検索を開始する
2.  対象ノードが存在しない場合は検索値が木に登録されていないものとして終了
3.  i = 1
4.  キー<sub>i</sub> が存在しないか、検索値 \< キー<sub>i</sub> の場合、枝<sub>i</sub> が指すノードを対象として2へ
5.  検索値 = キー<sub>i</sub> の場合、検索成功として終了
6.  i = i + 1 として4へ

### 挿入

[B-tree-splitt.png](https://ja.wikipedia.org/wiki/File:B-tree-splitt.png "fig:B-tree-splitt.png") 検索の処理を行うことで、挿入しようとする値が木のどこに位置するべきかがわかる。まだ登録されていない値を検索した場合、処理は必ず葉ノードまで達する。すなわち、挿入処理は常に葉ノードを対象として開始される。ノードにまだ新たなキーを登録する余地がある場合、キーを追加して挿入処理は終了する。

問題は、対象となるノードが既に許容できる最大数のキーを持っている場合である。この場合、ノードの**分割**処理を行う。分割が必要なノードからキーをひとつ選択し（通常、大小順で中央の値を選択する）、このキーより小さいキーだけを含むノードと、より大きいキーだけを含むノードに分割する。分割の基準となったキーは、親のノードに移動する。

ここで、親ノードに対してキーを追加している。親ノードでキーの最大数を越えた場合は、根に向かって順に分割処理を適用していく。根まで到達して根が分割された場合は、木の高さが1段増加することになる。分割直後の新しい根は、キーを1個と枝を2個だけ持っている。

## 関連項目

  - [B+木](../Page/B+木.md "wikilink")
  - [B\*木](../Page/B*木.md "wikilink")
  - [kd木](https://ja.wikipedia.org/wiki/kd木 "wikilink")
  - [R木](../Page/R木.md "wikilink")
  - [スプレー木](../Page/スプレー木.md "wikilink")
  - [基数木](../Page/基数木.md "wikilink")

## 参考文献

  - R. Bayer and E. McCreight. "Organization and Maintenance of Large Ordered Indexes," *Acta Informatica*, 1, 1972.
  - [Donald E. Knuth](../Page/ドナルド・クヌース.md "wikilink") 『[The Art of Computer Programming](../Page/The_Art_of_Computer_Programming.md "wikilink")』Volume 3 Sorting and Searching Second Edition 日本語版、有澤誠・和田英一監訳、石井裕一郎ほか訳、株式会社アスキー、2006年、ISBN 4-7561-4614-7。
  - [奥村晴彦](../Page/奥村晴彦.md "wikilink") 『C言語による最新アルゴリズム事典』 技術評論社<ソフトウェアテクノロジー13>、平成3年（1991年）、ISBN 4-87408-414-1。

## 外部リンク

  - [Ｂ木の普遍性について（英語）](http://www.cl.cam.ac.uk/~smh22/docs/ubiquitous_btree.pdf)

[Category:Bツリー](https://ja.wikipedia.org/wiki/Category:Bツリー "wikilink") [Category:探索木](https://ja.wikipedia.org/wiki/Category:探索木 "wikilink") [Category:ツリー_(データ構造)](https://ja.wikipedia.org/wiki/Category:ツリー_\(データ構造\) "wikilink") [Category:データベース・インデックス技術](https://ja.wikipedia.org/wiki/Category:データベース・インデックス技術 "wikilink")