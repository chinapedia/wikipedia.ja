> この記事は[Cyclops64](https://ja.wikipedia.org/wiki/Cyclops64)から翻訳されています。


[right](https://ja.wikipedia.org/wiki/ファイル:C64_architecture.png "wikilink")

**Cyclops64**（以前はBlue Gene/Cと呼ばれていた）は[IBM](../Page/IBM.md "wikilink")によって開発されているセルベースの[アーキテクチャである](../Page/コンピュータ・アーキテクチャ.md "wikilink")。Cyclops64プロジェクトでは、世界初の1[チップ](../Page/集積回路.md "wikilink")[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")(supercompuer on a chip)の実現を目標として開発が進められている。

## 歴史

Cyclops64は[Blue Geneプロジェクトで開発されているスーパーコンピュータの](https://ja.wikipedia.org/wiki/Blue_Gene "wikilink")1つであり、 [アメリカ合衆国エネルギー省](../Page/アメリカ合衆国エネルギー省.md "wikilink")、[アメリカ国防総省](../Page/アメリカ国防総省.md "wikilink")、産業界(特に[IBM](../Page/IBM.md "wikilink"))、大学などの研究機関によって共同で開発されている。

## アーキテクチャ

Cyclops64では、1チップに80個の[プロセッサ搭載されており](../Page/CPU.md "wikilink")、動作[周波数](../Page/周波数.md "wikilink")は500MHzで動ある。 個々のプロセッサには、2つの[スレッドユニットと](../Page/スレッド_\(コンピュータ\).md "wikilink")1つの[FPU](../Page/FPU.md "wikilink")が搭載されている。 1チップ上のプロセッサは96ポート、7ステージの[クロスバースイッチ](https://ja.wikipedia.org/wiki/クロスバースイッチ "wikilink")で相互に接続されている。 全てのプロセッサは[SRAM上の共有メモリを利用することでデータの受け渡しを行う](../Page/Static_Random_Access_Memory.md "wikilink")。

Cyclops64の性能の理論上の値は80GFlopsである。システム全体では、13,824個のCyclops64チップ、1,105,920個のプロセッサを搭載し、 2,211,840のスレッドを同時並行で実行できる。

### システム構成

  - システム全体は96ラックから構成される
  - 1ラックに3つのブロックから構成される
  - 1つのブロックには48枚の演算ボードから搭載される
  - 1つの演算ボードには1つのチップが搭載される
  - 1つのチップには80のプロセッサが搭載される
  - 1つのプロセッサは2個のスレッドを同時実行できる

## ソフトウェア

Cyclops64は、性能を最大限に引き出せるように、[ハードウェア](../Page/ハードウェア.md "wikilink")の多くの部分を[プログラマ](../Page/プログラマ.md "wikilink")に公開している。 しかし、本当に効率の良いプログラムを作成するのは容易ではない。

Cyclops64は、[TiNy Threadと](https://ja.wikipedia.org/wiki/TiNy_Thread "wikilink")[POSIX Threadをサポートする](https://ja.wikipedia.org/wiki/POSIX_Thread "wikilink")。

## 関連項目

  - [Blue Gene](https://ja.wikipedia.org/wiki/Blue_Gene "wikilink")
  - [スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")

[Category:スーパーコンピュータ](https://ja.wikipedia.org/wiki/Category:スーパーコンピュータ "wikilink") [Category:IBM](https://ja.wikipedia.org/wiki/Category:IBM "wikilink")