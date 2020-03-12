> この記事は[PowerPC 603](https://ja.wikipedia.org/wiki/PowerPC_603)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/ファイル:XPC603EFE100LF_01.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:XPC603PRX200LC_01.jpg "wikilink")  **PowerPC 603**シリーズは[アップルコンピュータ](../Page/アップル_\(企業\).md "wikilink")、[モトローラ](../Page/モトローラ.md "wikilink")、[IBM](../Page/IBM.md "wikilink")が共同で開発した[32ビット](../Page/32ビット.md "wikilink")の[RISC](../Page/RISC.md "wikilink")[マイクロプロセッサ](../Page/マイクロプロセッサ.md "wikilink")である。[PowerPC 601の後継として](../Page/PowerPC_601.md "wikilink")、低消費電力に主眼を置いて開発された。アップルコンピュータの[PowerBook](../Page/PowerBook.md "wikilink")シリーズ、[Performa](../Page/Performa.md "wikilink")シリーズなどに採用された外、[組み込み用途では現在も用いられている](../Page/組み込みシステム.md "wikilink")。

PowerPC 603には発展系の同603e、603evが存在する。パーソナルコンピュータに採用されていた期間が長いことや、現在も生産されていることなどから603よりもむしろ603eの方が一般的である。また、603eと603evの区別は曖昧である。

## 設計

PowerPC 603及びその発展型である603e、603evは32ビットのRISCプロセッサである。先代のPowerPC 601とは異なり、[POWERアーキテクチャとの互換性はない](../Page/POWER_\(マイクロプロセッサ\).md "wikilink")。 主な仕様は以下の通りである。

  - 3(うち1は分岐)命令実行\[1\]の[アウト・オブ・オーダー実行](../Page/アウト・オブ・オーダー実行.md "wikilink")可能な[スーパースカラ](https://ja.wikipedia.org/wiki/スーパースカラ "wikilink")コア
  - 32ビットの[アドレスバス](https://ja.wikipedia.org/wiki/アドレスバス "wikilink")
  - 内部／外部[64ビット](https://ja.wikipedia.org/wiki/64ビット "wikilink")の[データバス](https://ja.wikipedia.org/wiki/データバス "wikilink")
  - 整数演算ユニット×1
  - [浮動小数点数演算ユニット](../Page/FPU.md "wikilink")×1
  - 603では16KBの[L1キャッシュ](../Page/キャッシュ.md "wikilink")、603e以降は32KBのL1キャッシュ
  - [L2キャッシュはシステムバス上に任意で搭載](../Page/キャッシュ.md "wikilink")
  - コア2.5V、I/O3.3Vの低電圧動作
  - パワーマネージメントシステム
  - [プロセス](../Page/プロセス.md "wikilink")は0.25μm\~0.5μm

動作クロックは初期の603で66MHzで、最終的には300MHzのものまで開発された。

## 特徴

低消費電力なPowerPCの中でも特に低消費電力である。300MHzでの平均消費電力は3.5W。ダイサイズも小さく、価格も同世代の604シリーズに対して低価格であった。これらのことから[ノートパソコン](../Page/ノートパソコン.md "wikilink")や[ローエンド](https://ja.wikipedia.org/wiki/ローエンド "wikilink")～ミッドレンジの据え置き型に多く採用された。

一方で処理性能に関しては、整数演算ユニット及び浮動小数点数演算ユニットが大変強力な[PowerPC 604シリーズには遠く及ばず](../Page/PowerPC_604.md "wikilink")、603ev 240MHzでようやく604e 150MHz\~180MHzに並ぶ程度であった。また、1クロックあたりの処理能力は601にも劣った。603eの後継である[PowerPC 750(G3)では整数演算ユニットの強化及びバックサイドL](../Page/PowerPC_G3.md "wikilink")2キャッシュの採用により大幅に性能が向上し、604シリーズを凌駕する性能を得たが、それでもFPUの性能では劣っていた。

## 製品

  - PowerPC 603
  - PowerPC 603e
  - PowerPC 603ev

## 脚注

## 関連項目

  - [フリースケール](https://ja.wikipedia.org/wiki/フリースケール "wikilink")
  - [PowerQUICC II](../Page/PowerQUICC.md "wikilink") - 組み込み向け派生品
  - [ピピンアットマーク](../Page/ピピンアットマーク.md "wikilink")

[en:PowerPC 600\#PowerPC 603](https://ja.wikipedia.org/wiki/en:PowerPC_600#PowerPC_603 "wikilink")

[Category:IBMのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:IBMのマイクロプロセッサ "wikilink") [Category:アップルのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:アップルのマイクロプロセッサ "wikilink") [Category:モトローラのマイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:モトローラのマイクロプロセッサ "wikilink")

1.  ただし、一次命令キャッシュの帯域が64バイト/クロックに制限されているため、実際には2命令/クロックの性能しか持続できない。この制限は、後継の[PowerPC G3では改善された](../Page/PowerPC_G3.md "wikilink")。