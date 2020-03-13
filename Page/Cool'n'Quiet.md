> この記事は[Cool\'n\'Quiet](https://ja.wikipedia.org/wiki/Cool\'n\'Quiet)から翻訳されています。


**Cool'n'Quiet**（クールンクワイエット）とは、[AMD](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink") K8系以降の[CPU](../Page/CPU.md "wikilink")に実装されている省電力技術である。

## 概要

Cool'n'Quietという名称は"Cool and Quiet"の略で、さらに**CnQ**と略されることもある。

Cool'n'Quietの機能は、CPUの負荷に応じてプロセッサの電圧と周波数を低下させることで、消費電力と発生する熱を抑えることである。また、これにより冷却ファンの能力を下げることができ、騒音の低下も期待できる。

この技術は[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の[SpeedStepやAMD自身の](../Page/Intel_SpeedStep_テクノロジ.md "wikilink")[PowerNow\!](../Page/PowerNow!.md "wikilink")と類似しているが、それらは[バッテリー使用時での動作時間を向上する目的で開発されたものである](../Page/電池.md "wikilink")\[1\]。

Computerworld.jpの行ったテストでは、Cool'n'Quietを利用しない場合と比べてベンチマークに要した時間が若干増加した。しかし、テストを通じての積算電力量は減少し、「消費電力抑制に多大な効果を挙げている」と解説している\[2\]。

## 駆動周波数と駆動電圧

Cool'n'Quietが機能しているときの周波数と電圧は、CPUに設定されている**P-State**によって決定される。

[Athlon 64の場合](../Page/Athlon_64.md "wikilink")、最小時800MHz/1.3V（SH-C0リビジョン）または1GHz/1.1V（SH-CGリビジョン以降）、中間は最大値から1.8GHzまで、200MHz/0.1V刻み（DH-CGリビジョンまで）または200MHz/0.05V刻み（DH-D0リビジョン以降）で変化する。
マザーボードによってはHyperTransport設定を変える事で最低倍率を下げられる。×4なら4倍、×5なら5倍。殆どのノートパソコンはHT×4で動いており800MHzが下限である。

[Athlon 64 FX](../Page/Athlon_64_FX.md "wikilink")（Socket939モデルのみ）の場合、最小時1.2GHz/1.1Vのみで、中間の設定はない。

## サポートしているプロセッサ

  - Athlon 64([K8版 Athlon](https://ja.wikipedia.org/wiki/K8版_Athlon "wikilink")), [Athlon 64 X2](../Page/Athlon_64_X2.md "wikilink")(Athlon X2): 全て
  - Athlon 64 FX: 全て
  - [Sempron](../Page/Sempron.md "wikilink"): Socket754・Socket939 3000+以上、SocketAM2 3200+以上
  - [Phenom](../Page/AMD_Phenom.md "wikilink"): 全て(Cool'n'Quiet 2.0)
  - [Phenom II](https://ja.wikipedia.org/wiki/AMD_Phenom_II "wikilink"): 全て(Cool'n'Quiet 3.0)

## 関連項目

  - [PowerNow\!](../Page/PowerNow!.md "wikilink")
  - [Optimized Power Management](https://ja.wikipedia.org/wiki/Optimized_Power_Management "wikilink") - [Opteron](https://ja.wikipedia.org/wiki/Opteron "wikilink")(Rev.E)向けの省電力技術
  - [Intel SpeedStep テクノロジ](../Page/Intel_SpeedStep_テクノロジ.md "wikilink")
  - [PowerTune](https://ja.wikipedia.org/wiki/PowerTune "wikilink") - IBM [PowerPC 970の省電力技術](../Page/PowerPC_970.md "wikilink")

## 脚注

## 外部リンク

  -
[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:クロック](https://ja.wikipedia.org/wiki/Category:クロック "wikilink")

1.
2.