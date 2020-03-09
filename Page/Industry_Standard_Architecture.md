> この記事は[Industry Standard Architecture](https://ja.wikipedia.org/wiki/Industry_Standard_Architecture)から翻訳されています。


[Network_card.jpg](https://ja.wikipedia.org/wiki/File:Network_card.jpg "fig:Network_card.jpg") [Bussysteme_Extended_ISA_32Bit,_ISA_16Bit,_XT_8Bit.JPG](https://ja.wikipedia.org/wiki/File:Bussysteme_Extended_ISA_32Bit,_ISA_16Bit,_XT_8Bit.JPG "fig:Bussysteme_Extended_ISA_32Bit,_ISA_16Bit,_XT_8Bit.JPG"), ISA 16ビット, [EISA](https://ja.wikipedia.org/wiki/Extended_Industry_Standard_Architecture "wikilink")\]\] [Mainboard_isa.jpg](https://ja.wikipedia.org/wiki/File:Mainboard_isa.jpg "fig:Mainboard_isa.jpg") [ISA_Bus_pins.svg](https://ja.wikipedia.org/wiki/File:ISA_Bus_pins.svg "fig:ISA_Bus_pins.svg") **Industry Standard Architecture**（インダストリ スタンダード アーキテクチャ、通常**ISA**（アイ・エス・エー/アイサ）と略される）は、[1984年](../Page/1984年.md "wikilink")に発売されたIBM [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")に搭載されたバス（通称**ATバス**）を、[1988年](../Page/1988年.md "wikilink")に標準化したものである。

## 経緯

ATバスはIBM [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")に搭載されたバスであり、[8088対応の](../Page/Intel_8086.md "wikilink")8ビットバスである[XTバス](https://ja.wikipedia.org/wiki/XTバス "wikilink")を、[80286に対応した](../Page/Intel_80286.md "wikilink")16ビットバスに拡張したものである\[1\]。当時は汎用バスとしての標準化はされておらず「ATバス」という正式名称も存在しなかったが、[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")および[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")が[事実上の標準](https://ja.wikipedia.org/wiki/事実上の標準 "wikilink")となったため、この「ATバス」という名称や規格もまた、事実上の標準となった。

[1988年](../Page/1988年.md "wikilink")に[EISAが制定された際に初めて](https://ja.wikipedia.org/wiki/Extended_Industry_Standard_Architecture "wikilink")、「ISAバス」の名称がつけられ、遡って標準化された。このため現在でも、当時のEISA陣営のメーカーは「ISAバス」、対立した[IBM](../Page/IBM.md "wikilink")は「ATバス」と呼ぶ傾向がある。

## 概要

ISAは、XTバスの先に増えたアドレス線やデータ線や割り込み線を付加した構造で、XTバスの上位互換機能を持つが、泥縄式拡張であるため、遅いバススピード、割り込み数の不足、バス調停機能の欠如、無秩序で非合理的な信号線配列、貧弱なグランドによる信号保護の不足、電力供給の不足等、数多くの問題を抱え、汎用バスとしてはかなり使いづらい存在である。

とは言うものの、当初ローカルな使用目的で実装が容易なことを第一として作成されたバスが汎用標準バスとして普及すると言う事態は良くある事で、アーキテクチャに依存しない汎用指向のバスで広く普及しているのはPCI位のものであろう。

なお、[PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")に搭載されたバスと、以後「ATバス」と総称されて後に「ISA」と呼ばれたバスは、厳密には同一ではない。

ISAバスは16の割り込みチャネル(IRQ)を持ち、そのうち11が拡張スロットに引き出されている。IRQ 8～15はIRQ 2に接続された割り込みコントローラが受け持つため、優先度はIRQ 2と3の間になる。また、8つの[DMAチャネルを持ち](../Page/Direct_Memory_Access.md "wikilink")、うち7つが引き出されている。8ビットのスロットで使用できるのは割り込みが6つ、DMAが3つである。

<table>
<thead>
<tr class="header">
<th><p>割り込み<br />
チャネル</p></th>
<th><p>拡張スロット</p></th>
<th><p>標準で割り当てられた機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>16<br />
ビット</p></td>
<td><p>8<br />
ビット</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td><p>無</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td><p>無</p></td>
<td><p>無</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>無</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
<td><p>無</p></td>
<td><p>無</p></td>
</tr>
<tr class="even">
<td><p>9</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="odd">
<td><p>10</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="even">
<td><p>11</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>12</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="even">
<td><p>13</p></td>
<td><p>無</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="even">
<td><p>15</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th><p>DMA<br />
チャネル</p></th>
<th><p>拡張スロット</p></th>
<th><p>標準で割り当てられた機能</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>16<br />
ビット</p></td>
<td><p>8<br />
ビット</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>有</p></td>
<td><p>有</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>無</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>有</p></td>
<td><p>無</p></td>
</tr>
</tbody>
</table>

[PC/XT](https://ja.wikipedia.org/wiki/PC/XT "wikilink")やPC/ATでは、CPUのローカルバスを**バスバッファ**を経由しただけで外部に引き出した構造をしており、そのためバスクロックはCPUのクロックと同一となり、PC/XTでは8088の8ビット・4.77MHz、PC/ATでは[80286の](../Page/Intel_80286.md "wikilink")[16ビット](https://ja.wikipedia.org/wiki/16ビット "wikilink")・8MHz（初代は6MHz）であった。つまり、各モデル(CPU)ごとのローカル規格のバスであった。

これに対して[コンパック](../Page/コンパック.md "wikilink")は[Deskpro 386でIBMに先駆けて](https://ja.wikipedia.org/wiki/Deskpro_386 "wikilink")[32ビット](https://ja.wikipedia.org/wiki/32ビット "wikilink")の[80386を採用した際に](../Page/Intel_80386.md "wikilink")、**バスブリッジ**を導入し、CPUのクロックと外部バスのクロックを分離した。これにより32ビットの80386と、既に普及していた16ビット・8MHz前後のATバス周辺機器の両立が可能となった。コンパックはこれを[Flex Architectureと呼んだ](https://ja.wikipedia.org/wiki/Flex_Architecture "wikilink")。更にバスクロックは10MHzが一般的となり、後には再参入した[IBM](../Page/IBM.md "wikilink")を含め、スロット数を含め色々な「ATバスマシン」である**[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")**が普及し[事実上の標準](https://ja.wikipedia.org/wiki/事実上の標準 "wikilink")となった。反面、いくら高速な32ビットCPUを搭載しても、外部バスは16ビット・10MHz前後のままという[レガシー](https://ja.wikipedia.org/wiki/レガシー "wikilink")な負の側面は残り、後の[MCAとEISAの規格争いに繋がることになった](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")。

後にEISA陣営とIEEEが標準化した「ISAバス」は、正確にはバスブリッジ方式のものである。

[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")代後半より、ISAは[PCIの普及に伴い徐々に姿を消していったが](../Page/Peripheral_Component_Interconnect.md "wikilink")、一部の特殊な機器をISAで接続する需要が少なからず存在していたことから、[2004年](https://ja.wikipedia.org/wiki/2004年 "wikilink")頃まではISAスロットを搭載した[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")が販売されていたものの、ISAスロット非搭載を前提とする[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")[チップセット](../Page/チップセット.md "wikilink")900番台の本格普及を機に姿を消していった。

なお、拡張スロットとしてのISAバスが搭載されていない機種であっても、[レガシーデバイス](https://ja.wikipedia.org/wiki/レガシーデバイス "wikilink")と呼ばれる[PS/2コネクタ](https://ja.wikipedia.org/wiki/PS/2コネクタ "wikilink")、 [DMAコントローラ](https://ja.wikipedia.org/wiki/DMAコントローラ "wikilink")などは、ソフトウェアからのアクセス方法の互換性が保たれており、見かけ上ISAバスに接続されているように認識される。

## 脚注

<references />

## 関連項目

  - [Extended Industry Standard Architecture](https://ja.wikipedia.org/wiki/Extended_Industry_Standard_Architecture "wikilink") (EISA)
  - [Micro Channel Architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") (MCA)
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI)
  - [XTバス](https://ja.wikipedia.org/wiki/XTバス "wikilink")
  - [VESA ローカルバス](../Page/VESA_ローカルバス.md "wikilink")
  - [PC/104](https://ja.wikipedia.org/wiki/PC/104 "wikilink")
  - [コンパクトPCI](https://ja.wikipedia.org/wiki/コンパクトPCI "wikilink")

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink")

1.  PC/ATで割り込みコントローラが追加された関係で、オリジナルのXTバスではIRQ 2になっているB4番の信号線がISAバス(16ビット・8ビットとも)ではIRQ 9になっている。