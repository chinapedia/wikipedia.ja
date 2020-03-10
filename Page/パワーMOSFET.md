> この記事は[MOSFET](https://ja.wikipedia.org/wiki/MOSFET)から翻訳されています。


[D2PAK.JPG](https://ja.wikipedia.org/wiki/File:D2PAK.JPG "fig:D2PAK.JPG") **パワーMOSFET**（）は、大電力を取り扱うように設計された[MOSFET](../Page/MOSFET.md "wikilink")のこと。 他の[パワーデバイスと比較するとスイッチング速度が速く](https://ja.wikipedia.org/wiki/電力用半導体素子 "wikilink")、低電圧領域での変換効率が高い為、200V以下の領域で、[スイッチング電源](https://ja.wikipedia.org/wiki/スイッチング電源 "wikilink")や、[DC-DCコンバータ](https://ja.wikipedia.org/wiki/DC-DCコンバータ "wikilink")等に用いられる。

[MOSFET.jpg](https://ja.wikipedia.org/wiki/File:MOSFET.jpg "fig:MOSFET.jpg")

## 構造

[Vdmos_cross_section_en.svg](https://ja.wikipedia.org/wiki/File:Vdmos_cross_section_en.svg "fig:Vdmos_cross_section_en.svg") [Umos_cross_section_en.svg](https://ja.wikipedia.org/wiki/File:Umos_cross_section_en.svg "fig:Umos_cross_section_en.svg")

### NチャネルMOSFET

パワーMOSFETの基本的な構造は、DMOS（Double-Diffused MOSFET）と呼ばれる構造で、N+基板の上に形成されたNエピタキシャル層表面側に低濃度のP型層（Pボディ）と高濃度のN型層を二重拡散で形成した構造である（図1）。この構造（単位セル）が多数並列接続され、ひとつの素子となっている。素子のオン抵抗を低減する為には単位セルの微細化が有効であり、表面に溝を形成しその中にゲートを埋め込むことにより単位セル面積を縮小する**トレンチゲート型**が開発されている（図2）。さらに、高耐圧化、オン抵抗・スイッチング損失の低減を追求する為さまざまな構造が提案されている。

素子の耐圧は、N層の不純物濃度と厚みによって決まり、電流はチャネル長によって決まる。耐圧を高くするには、N層の不純物濃度を低くし、厚みを厚くすることが必要である。そうすると電流を流す時の抵抗が大きくなる。 具体例では、60V程度の耐圧素子ではオン抵抗値が100mΩ以下というのが極普通で、30A程度のスイッチングをした場合5w以下と非常に電力ロスが少ない。 しかしながら、400V程度の耐圧素子ではオン抵抗が1～10Ωもあり、10A程度の回路に用いた場合10～100wと桁外れにロスが大きくなる。このため、高電圧用途の代表である[インバータ](../Page/インバータ.md "wikilink")では照明用途程度（5A以下）でしか利用されておらず、大電流用途である電動機制御分野では[絶縁ゲートバイポーラトランジスタ](../Page/絶縁ゲートバイポーラトランジスタ.md "wikilink") (IGBT) が主に用いられている。 新たな技術として本質的に高耐圧の素子が構成可能な[炭化ケイ素](../Page/炭化ケイ素.md "wikilink")(SiC)系の半導体を用いることで低耐圧素子と大差ないN型層の厚みと不純物濃度で高耐圧のMOS-FETにおいてオン抵抗100mΩ以下という素子も開発された。またこの高耐圧SiC-MOS-FETを応用した高耐圧かつ低飽和電圧特性のIGBTも開発されている。

### PチャネルMOSFET

図のPとNを反転し、P+基板上にPエピタキシャル層を形成し、表面側にNボディと高濃度P層を形成したPチャネルMOSFETも存在する。この構造では、主要なキャリアが[正孔](../Page/正孔.md "wikilink")であり、[電子](https://ja.wikipedia.org/wiki/電子 "wikilink")と比較すると[移動度](https://ja.wikipedia.org/wiki/移動度 "wikilink")が低くなる為にオン抵抗が大きくなり、NチャネルMOSFETと比較するとスイッチング特性が悪くなる。

## 基本特性

パワーMOSFETとして重要な特性は、耐圧とオン抵抗である。

  - BV<sub>DSS</sub> （ソース-ドレイン間耐圧）

<!-- end list -->

  -

      -
        ソース-ドレイン間耐圧は、Pボディ層とNエピタキシャル層で形成されるPNダイオードのアバランシェ電圧によって決まる。

<!-- end list -->

  - Ron（オン抵抗）

<!-- end list -->

  -

      -
        オン抵抗は、ソースからドレインまでキャリアが移動する経路の抵抗の総和で決められる。主な要素として、MOSのチャネル抵抗、Nエピタキシャル層の抵抗などがある。

## 関連項目

  - [電力用半導体素子](https://ja.wikipedia.org/wiki/電力用半導体素子 "wikilink")
  - [絶縁ゲートバイポーラトランジスタ](../Page/絶縁ゲートバイポーラトランジスタ.md "wikilink")

[Category:トランジスタ](https://ja.wikipedia.org/wiki/Category:トランジスタ "wikilink") [Category:パワーエレクトロニクス](https://ja.wikipedia.org/wiki/Category:パワーエレクトロニクス "wikilink")