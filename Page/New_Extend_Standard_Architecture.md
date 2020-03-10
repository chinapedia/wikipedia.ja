> この記事は[New Extend Standard Architecture](https://ja.wikipedia.org/wiki/New_Extend_Standard_Architecture)から翻訳されています。


**New Extend Standard Architecture** (NESA)は、**Eバス**とも略され、[1990年](https://ja.wikipedia.org/wiki/1990年 "wikilink")に発売された、[日本電気](../Page/日本電気.md "wikilink") (NEC) の[PC-H98シリーズ](../Page/PC-H98シリーズ.md "wikilink")に搭載された32ビット高速バスである。

SV-H98シリーズや、同社の[N5200](../Page/N5200.md "wikilink")シリーズ等にも用いられたが、それ以外での採用例は無い。

## 開発経緯

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に発表された[Intel 80386によって](../Page/Intel_80386.md "wikilink")、[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")以降、従来16ビット幅の汎用データバスを使用していた[IBM](../Page/IBM.md "wikilink") [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")やNECの[PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")といったx86系プロセッサ搭載パーソナルコンピュータにおいては、汎用データバスおよびそれを用いる拡張スロットの32ビット化が喫緊の課題となりつつあった。

[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")では、本家IBMが[PS/2と共にリリースした](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")[MCAと](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")、互換機メーカーらによる[EISAの戦いという形で現れ](../Page/Extended_Industry_Standard_Architecture.md "wikilink")（[EISAの記事の背景の節を参照](https://ja.wikipedia.org/wiki/Extended_Industry_Standard_Architecture#背景 "wikilink")）、最終的にはEISAの側に軍配が上がった。

PC-98シリーズの場合は、やや事情が異なっていた。同シリーズのオリジネイターであるNECが、アメリカ市場ではPC/AT互換機メーカーの1社としてEISAの開発に携わるという一種のねじれが生じていたため、結果としてEISAを研究し尽くした上で、EISAとの互換性に拘泥することなくさらに改良を加えたバスを開発できたのである。

NECはPC-98シリーズ用汎用32ビットバスを開発するに当たって、EISAに似たバス調停機能とリソース設定機能を備えつつ、EISAの欠点であったISA上位互換を実現するための非合理的な信号線配置については[Cバス](../Page/Cバス.md "wikilink")とは全く異なる新型コネクタを採用することで克服するという、巧妙かつ中庸を得たデザインを採用した。それはEISAとMCAの双方について知悉し、また専用のインテリジェント・コントローラを自社で開発する技術力のあるNECだからこそ実現可能なアーキテクチャであった。

こうして、EISAから遅れること約1年、1990年1月に発表された高価なハイレゾグラフィック機能に対応するPC-H98 model 70に搭載される形で、NESAは市場デビューを果たした。

## 規格

  - 各拡張ボードおよび周辺デバイスにはインテリジェントコントローラが搭載され、高度なバス調停機能と、NESA-FOと呼ばれるリソース自動設定機能を備える。
  - [レベルトリガ](https://ja.wikipedia.org/wiki/レベルトリガ "wikilink")[割り込み機能を持ち](../Page/割り込み_\(コンピュータ\).md "wikilink")、各種デバイス間で割り込み信号線の共有が可能。
  - 180本の接点で構成され、データ信号線3 - 4本おきに1つGNDと+5Vを配置、ノイズが発生しやすいクロック端子の脇にはGND線を置いて他の信号線との干渉を避けるなど、電気的に非常によく考えられた、耐ノイズ性能の高い構造になっている。
  - 32ビットのアドレス空間、データバス幅を有する。
  - 8MHzで駆動され、33Mbytes/secの理論最大転送帯域を有する。
  - 拡張ボード基板寸法は奥行き17cm、幅15cmの長方形で、部品実装面の厚さは最大2.5cmが許容されている。
  - 上下の[Cバス](../Page/Cバス.md "wikilink")スロットコネクタ間の空きスペースに配置する形で専用の32ビットバスコネクタ（Eバスコネクタ）を設け、Cバスボードとの互換性は全くないものの、同一拡張スロットを排他利用することが可能な構造になっている。90個の接点を持つ矩形のコネクタ2つを並べ、後に開発された[98ローカルバス](../Page/98ローカルバス.md "wikilink")において全く同じ物理形状のコネクタが使用されているが、それとの電気的な相互互換性は無い。
  - 筐体を開けずに抜き差しできるようにブラケット部には引き抜き用のレバーが装着されている。

## NESA（Eバス）製品の例

NESAバスメモリ・SCSIボード・LANボードなどが存在した。H98用内蔵HDDユニットなどもSCSIホストアダプタ機能を備えていることがあるように、対象機種では内蔵HDDインターフェースも一種のNESAバスであるが、ここではEバス形状を持つNESA製品の例を挙げる。

### PC-H98/SV-H98シリーズ向け

以下のほか、N5200シリーズ用などではハードウエア的には同等の製品であっても異なる型番で用意された。それらはNESA-FOまわりのファームウエアが異なるためH98では使用できず、逆にH98向けのNESA製品もN5200シリーズでは使用できない。

  - NESAバスメモリ

<!-- end list -->

  - PC-H98-B02 (NEC)
  - PC-H98-B08 (NEC)

<!-- end list -->

  - SCSIボード

<!-- end list -->

  - PC-H98-B03 (NEC)
  - PC-H98-B12 (NEC)
  - PSB-H9310 (日本マイクロコンピュータ)

<!-- end list -->

  - LANボード

<!-- end list -->

  - PC-H98-B04 (NEC)
  - PC-H98-B09 (NEC)
  - PC-H98-B10 (NEC)
  - PC-H98-B11 (NEC)

<!-- end list -->

  - その他

<!-- end list -->

  - PC-H98-B01 (NEC) - NESA-FOチップを搭載した自作基板
  - PC-H98-B05 (NEC) - 高速回線アダプタ
  - PC-H98-B06 (NEC) - i860搭載CPUボード
  - PC-H98-B13 (NEC) - ビデオキャプチャボード
  - SV-H98-B01 (NEC) - プリンタボード
  - PC-H98-U02 (NEC) - NESAバス増設ボックス

## 関連項目

  - [PC-H98シリーズ](../Page/PC-H98シリーズ.md "wikilink")
  - [Cバス](../Page/Cバス.md "wikilink")
  - [98ローカルバス](../Page/98ローカルバス.md "wikilink")
  - [APバス](https://ja.wikipedia.org/wiki/APバス "wikilink")

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink") [Category:日本電気のパーソナルコンピュータ](https://ja.wikipedia.org/wiki/Category:日本電気のパーソナルコンピュータ "wikilink")