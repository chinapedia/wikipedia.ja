> この記事は[B\*](https://ja.wikipedia.org/wiki/B\*)から翻訳されています。


**B\*木**（）は、[B木](../Page/B木.md "wikilink")から派生した[木構造の一種で](../Page/木構造_\(データ構造\).md "wikilink")、[HFS](../Page/Hierarchical_File_System.md "wikilink") や [Reiser4](../Page/Reiser4.md "wikilink") [ファイルシステム](../Page/ファイルシステム.md "wikilink")で使われている。根ノード以外のノードは、B木のように1/2ではなく、2/3まで埋まった状態になる。このため、ノードがいっぱいになったとき即座に分割するのではなく、キーを次のノードと共有する。連続する2つのノードがいっぱいになると、それを3つのノードに分割する。また、常に左端のキーは使わずに残しておく。一般に総称して「B木」と呼ばれることが多く、「B\*木」と呼ばれることは滅多にない。

B\*木と[B+木](https://ja.wikipedia.org/wiki/B+木 "wikilink")は異なる。後者は、葉ノードが連結されて[連結リスト](../Page/連結リスト.md "wikilink")を構成するようになっているものである。B+木は、挿入のコストを増大させて、検索を効率化したものである。

IEEEカンファレンスICCI '93 においては B\*\*木の定義も見られた。

## 参考文献

  -
## 脚注

## 関連項目

  - [B木](../Page/B木.md "wikilink")
  - [B+木](https://ja.wikipedia.org/wiki/B+木 "wikilink")

## 外部リンク

  - [Dictionary of Algorithms and Data Structures entry for B\*-tree](http://www.nist.gov/dads/HTML/bstartree.html)

[en:B-tree\#Variants](https://ja.wikipedia.org/wiki/en:B-tree#Variants "wikilink")

[Category:データ構造](https://ja.wikipedia.org/wiki/Category:データ構造 "wikilink")