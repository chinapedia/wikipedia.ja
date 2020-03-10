> この記事は[FIFO](https://ja.wikipedia.org/wiki/FIFO)から翻訳されています。


[Fifo_queue.png](https://ja.wikipedia.org/wiki/File:Fifo_queue.png "fig:Fifo_queue.png")

**FIFO**(ファイフォ、フィフォ、フィーフォー)は***F**irst **I**n, **F**irst **O**ut*を表す[頭字語](../Page/頭字語.md "wikilink")である。**先入れ先出し**と訳されることがある。

この言葉は[キューの動作原理を表すものであり](../Page/キュー_\(コンピュータ\).md "wikilink")、キューに入っているどんな要素の組に対しても、先に入ったものを先に処理して出し、後に入ってきたものは先に入ったものより後から処理して出す、というように、出入りにおいて順序が保存されることを意味している（厳密には出入りのみを定義しており、処理順ではない）。日本語の俗な慣用表現では「[ところてん](../Page/ところてん.md "wikilink")式」も同じものを指す。

たとえば[優先度付きキュー](../Page/優先度付きキュー.md "wikilink")はキューの一種であるが、FIFOではない。優先順位によって順序が入れ替わるからである。[待ち行列理論](../Page/待ち行列理論.md "wikilink")における、FIFOキューについての厳密な定義もある。

**FIFO**は、いくつかの異なる文脈で用いられる。すなわち一般概念のこともあれば、特定の実装のこともある。以下ではそれぞれを解説するが、これが全てではない。たとえばもっとくだけた感じで、同時通訳のような情報の処理方法をFIFOと呼ぶこともある。

## コンピュータ

### データ構造

[Data_Queue.svg](https://ja.wikipedia.org/wiki/File:Data_Queue.svg "fig:Data_Queue.svg")

キューに格納されたデータの処理方法のひとつである。キュー上の各要素はキューのデータ構造内に格納される。FIFOのキューでは、最初に格納されたデータが、(後で)最初に取出されると同時に削除される。入出力（格納と取出し）は常にその順番で行われる。同義語としてLILO（Last In Last Out）がある。これはキューの一般的な動作である。これの対称として、先入れ後出し（後入れ先出し）の順序があり、[スタック](../Page/スタック.md "wikilink")または[LIFO](https://ja.wikipedia.org/wiki/LIFO "wikilink")を参照されたい。

典型的なデータ構造は次のようになる。

` struct fifo_node {`
`   fifo_node *next;`
`   value_type value;`
` };`

` class fifo`
` {`
`   fifo_node *front;`
`   fifo_node *back;`
`   fifo_node dequeue(void)`
`   {`
`     fifo_node *tmp = front;`
`     front = front->next;`
`     return tmp; `
`   }`
`   queue(value)`
`   {`
`     fifo_node *tempNode = new fifo_node;`
`     tempNode->value = value;`
`     back->next = tempNode;`
`     back = tempNode;`
`   }`
` }`

この例では、*queue(value)* で *value*がキューに格納され、*dequeue()* でキューの先頭のデータを取り出すようになっている。

### パイプ

一般に、いわゆる「[パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")」の動作はFIFOだが、特にファイルシステム名前空間に名前が作られる「[名前付きパイプ](../Page/名前付きパイプ.md "wikilink")」は、ファイルシステム中での種別（通常ファイル、ディレクトリ、デバイスファイル、etc）として「FIFO」と呼ばれている。

## 論理回路

[論理回路](https://ja.wikipedia.org/wiki/論理回路 "wikilink")では、データの流れる方向が一方向であるという特性のある記憶装置として、バッファリングに使われる。実現方法としては、[シフトレジスタ](../Page/シフトレジスタ.md "wikilink")のようにデータ全体が一方向に動くという方法と、アドレス付けされたメモリと書込み・読出しの各ポインタ、制御ロジックを組み合わせる方法がある。

重要な役割を果たしているFIFOとしては、デュアルポートSRAMがある。一方のポートがライトに使われ、もう一方がリードに使われる。

同期型FIFOはリードとライトに同じクロックを使用するものである。非同期型FIFOは異なったクロックを使用する。非同期型FIFOは[準安定性問題をはらんでいる](../Page/準安定状態.md "wikilink")。非同期型FIFOでは書込み・読出しのポインタの番地変化にインクリメントではなく[グレイコード](../Page/グレイコード.md "wikilink")を使い、安定した信号生成ができるようにする。

FIFOにはいくつかのフラグが付属する。フラグはFIFOの状態を表し、いっぱいになっているとか、もうすぐいっぱいになるとか、ほとんど空だとかいうことを示す。空きが設定した容量以下・以上になったら[割込みを起こすよう設定できるものも多い](../Page/割り込み_\(コンピュータ\).md "wikilink")。

## 関連項目

  - [LIFO](https://ja.wikipedia.org/wiki/LIFO "wikilink")
  - [スタック](../Page/スタック.md "wikilink") (LIFO)
  - [パイプ](../Page/パイプ_\(コンピュータ\).md "wikilink")
  - [リングバッファ](../Page/リングバッファ.md "wikilink")

[Category:データ型](https://ja.wikipedia.org/wiki/Category:データ型 "wikilink") [Category:デジタル回路](https://ja.wikipedia.org/wiki/Category:デジタル回路 "wikilink")