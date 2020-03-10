> この記事は[Programmable Interrupt Controller](https://ja.wikipedia.org/wiki/Programmable_Interrupt_Controller)から翻訳されています。


**Programmable Interrupt Controller**（**PIC**、割り込みコントローラ）はその[割り込み出力に優先順位を割り当てることができるデバイスである](../Page/割り込み_\(コンピュータ\).md "wikilink")。 デバイスがアサート可能な複数割り込み出力を持っている時、PICは優先順位に従って割り込みをアサートする。PICのモードには通常**hard priority**、**rotating priority**、**cascading priority**がある。PICの中にはしばしばその出力を他のPICの入力につないでカスケードすることができるものもある。

## 共通の特徴

PICは普通、共通のレジスタセットを持っている。Interrupt Request Register（IRR）、In-Service Register（ISR）、Interrupt Mask Register（IMR）である。IRRはackを返さず止めている割り込みを示しており、通常直接アクセスできないシンボリックレジスタである。ISRレジスタはackを返した割り込みを示しているが、まだ割り込み終了（End of Interrupt, EOI）を待っている割り込みを示す。IMRレジスタは無視ないしackを返さない割り込みを示している。このような単純なレジスタ構成を用いることで、同時に来た2つの重要な割り込み要求を一つはack待ちに、もう一つはEOI待ちにして分けることができる。

PICが持っている共通の優先順位付けは、hard priority、specific priority、rotating priorityから構成されている。

割り込みは[エッジトリガ](https://ja.wikipedia.org/wiki/エッジトリガ "wikilink")、[レベルトリガ](https://ja.wikipedia.org/wiki/レベルトリガ "wikilink")のいずれかを使える。

EOIが発行される時に、割り込みが完了したことを認識するのにはいくつか共通の方法がある。この中には、完了した割り込みを指定するもの、完了した割り込み（通常、ISR内で止められているもっとも優先度の高い割り込み）を暗黙に使うもの、EOIのような割り込みackを扱うものである。

## 有名なPIC

もっともよく知られているPICの一つに、[8259Aがある](../Page/Intel_8259.md "wikilink")。これはx86アーキテクチャのPCに採用されている。今では、これはx86 PCの中で単独のチップとしては存在しておらず、機能はマザーボードの[サウスブリッジ](../Page/サウスブリッジ.md "wikilink")の一部として取り込まれている。他には、より多くの割り込み出力とより柔軟なプライオリティ制御をサポートする、より新しい[Advanced Programmable Interrupt Controllersで完全に置き換えられていることもある](../Page/APIC.md "wikilink")。

[Category:割り込み_(コンピュータ)](https://ja.wikipedia.org/wiki/Category:割り込み_\(コンピュータ\) "wikilink")