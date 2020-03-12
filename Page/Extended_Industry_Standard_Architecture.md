> この記事は[Extended Industry Standard Architecture](https://ja.wikipedia.org/wiki/Extended_Industry_Standard_Architecture)から翻訳されています。


[300px](https://ja.wikipedia.org/wiki/ファイル:EISA_Bus.jpg "wikilink") [thumb](https://ja.wikipedia.org/wiki/ファイル:Bussysteme_Extended_ISA_32Bit,_ISA_16Bit,_XT_8Bit.JPG "wikilink"), [ISA 16ビット](../Page/Industry_Standard_Architecture.md "wikilink"), EISA\]\] **Extended Industry Standard Architecture**（通常 **EISA** （イーアイサ）と略される）は、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")用に開発された32ビットコンピュータ[バスアーキテクチャである](../Page/バス_\(コンピュータ\).md "wikilink")。

## 概要

[thumb](https://ja.wikipedia.org/wiki/ファイル:EISA_Bus_pins.png "wikilink") EISAは、[IBM](../Page/IBM.md "wikilink")の[IBM PS/2に搭載された](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink") [MCA](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") に対抗すべく、[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")メーカー9社（AST Research、[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")、[ヒューレットパッカード](https://ja.wikipedia.org/wiki/ヒューレットパッカード "wikilink")、[日本電気](../Page/日本電気.md "wikilink")、[オリベッティ](../Page/オリベッティ.md "wikilink")、[タンディ・ラジオシャック](../Page/ラジオシャック.md "wikilink")、Wyse、Zenith Data Systems）によって[1988年](../Page/1988年.md "wikilink")末に制定された。規格書は有料で配布されたものの、規格そのものは[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")とされている。

高度なバス調停機能、[リソース](https://ja.wikipedia.org/wiki/リソース "wikilink")の自動設定、4Gバイトまでの[メモリ](https://ja.wikipedia.org/wiki/メモリ "wikilink")アドレスサポート、理論最大33Mbytes/Secの帯域等、MCAにほぼ匹敵する仕様を持つが、[ISAとの互換性を維持するために](../Page/Industry_Standard_Architecture.md "wikilink")、ノイズ対策に必要なグラウンド信号線のレイアウトが最適化できず、高速化に制約が課せられていたため、絶対的な性能ではMCAに劣る。

EISAは[ISAを縦方向に拡張し](../Page/Industry_Standard_Architecture.md "wikilink")、エッジ・コネクタの接点を2列の千鳥配置とすることで32bit化してあるため、MCAとは異なり、ISAのボードや、[XTバス](../Page/XTバス.md "wikilink")のボードをそのまま装着することが可能である。

このことから、互換機メーカ各社にとって下位互換性の断絶というリスクを侵さずにバスの高速化が図れるメリットがあった。そのため、IBMも後年になって一部の機種に採用している。

とは言うものの、互換性に重視を置き過ぎたため、信頼性はともかく、データ転送帯域が絶対的に不足し、[VLバスや](../Page/VESA_ローカルバス.md "wikilink")、[PCIが普及する中](../Page/Peripheral_Component_Interconnect.md "wikilink")、次第に市場から消え去っていった。

もっとも、インテルのPCIバス対応チップセットではPCI-EISAブリッジチップ（82375EB/SB）およびEISAコントローラ (82375EB/SB) などとして通常のサウスブリッジを置き換えるチップセットが450GXチップセットの世代までオプションで提供されており、これには[対称型マルチプロセッサ](https://ja.wikipedia.org/wiki/対称型マルチプロセッサ "wikilink") (SMP) を実現するのに必要なAPIC (Advanced Programmable Interruption Controller) が内蔵されていたこともあって、サーバ向けには比較的後年までEISAスロット搭載機が提供されていた。

## 背景

[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に発表された[Intel 80386によって](../Page/Intel_80386.md "wikilink")、[1986年](https://ja.wikipedia.org/wiki/1986年 "wikilink")以降、従来16ビット幅の汎用データバスを使用していた[IBM](../Page/IBM.md "wikilink") [PC/AT](https://ja.wikipedia.org/wiki/PC/AT "wikilink")と[その互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")、その他の類似した[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")系プロセッサ搭載パーソナルコンピュータにおいては、汎用データバスおよびそれを用いる拡張スロットの32ビット化が喫緊の課題となりつつあった。

この問題は、一旦は[コンパック](../Page/コンパック.md "wikilink")などによる、32ビット化する範囲をメモリやチップセットといったメインボード上のローカルなバスに留め、外部拡張スロットには従来通りの16ビット幅のデータバスを利用する手法で問題の先送りが図られた。だが、将来のオペレーティングシステムやアプリケーションソフトの必要メモリ量の増加、それに拡張バスに接続される各種デバイスの性能向上を考えた場合、未来のいずれかの時点で汎用データバス規格を変更あるいは拡張し、より高速かつ高機能な32ビットバスを導入する必要があることは明らかであった。

この問題については、欧米で一般に使用されていたPC/ATの生みの親であり、当時PCの各種規格についての決定権を事実上独占していたIBMの動きが注目された。

そもそもコンパックなどが自社製品へのIntel 80386採用に際し、高速化の恩恵の及ぶ範囲が狭いローカルバス方式を採用し汎用拡張バスの独自拡張を避けたのも、後からPC/ATのオリジネイターであるIBMがそれとは互換性のない汎用32ビットバス規格を制定した場合、自社規格の32ビットバスが孤立する危険性が極めて高いためであった。

だが、[1987年](https://ja.wikipedia.org/wiki/1987年 "wikilink")にIBMがPC/ATの後継機種として満を持して発表した[PS/2と](https://ja.wikipedia.org/wiki/IBM_PS/2 "wikilink")、それに採用された[MCAと呼ばれる新しい汎用](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink")32ビットバス規格は、PC/AT互換機を製造していた多くのメーカーに拒絶反応を示させるものであった。

なぜならMCAはIBMが保有する多数の特許によって厳重に保護され、互換機メーカー各社がIBMからのライセンス取得なしに製造できないようになっていたためである。

しかもこのMCAは従来の[ISAスロットに対する電気的な下方互換性やカードそのものの物理的な互換性を一切切り捨てることで高性能化を実現しており](../Page/Industry_Standard_Architecture.md "wikilink")、更にそのライセンス供与に当たってIBMは互換機メーカー各社に対し、各社が販売したPC互換機全てについて過去に遡って高額のライセンス料支払いに応じることを許諾条件の一つとして提示した。

この許諾条件はIBM製品に対する価格面での優位性によって市場での競争力を得ていた互換機メーカー各社にとって到底許容できる条件ではなく、またISAバスとの共存を拒否するMCAの採用は、既存のISA用拡張カードを購入した顧客の利便性を損なうことを意味していた。

このため、ごく一部のメーカーはMCAのライセンスを取得し、実際にもMCAを搭載するマシンを製造販売したものの、1987年当時アメリカ市場において有力であった大手[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")メーカー9社、具体的にはAST Research、[セイコーエプソン](../Page/セイコーエプソン.md "wikilink")、[ヒューレットパッカード](https://ja.wikipedia.org/wiki/ヒューレットパッカード "wikilink")、NEC、[オリベッティ](../Page/オリベッティ.md "wikilink")、[タンディ・ラジオシャック](../Page/ラジオシャック.md "wikilink")、Wyse、Zenith Data Systemsの各社はこの条件提示に応じることを拒否した。もっとも32ビットの新しい汎用バス規格が必要な状況には変わりがなかったため、これら9社は協議の上、MCAに対抗可能でなおかつ従来のISAに対する上位互換性を備えた新しい汎用32ビットバス規格の開発に乗り出し、IBMとは異なる道を進むことを決断した。

こうしてMCAに対抗する**EISA**が誕生し、アメリカのPC市場では一時MCAとEISAの激しい競争が起きた。

## 関連項目

  - [Industry Standard Architecture](../Page/Industry_Standard_Architecture.md "wikilink") (ISA)
  - [Micro Channel Architecture](https://ja.wikipedia.org/wiki/Micro_Channel_Architecture "wikilink") (MCA)
  - [New Extend Standard Architecture](../Page/New_Extend_Standard_Architecture.md "wikilink") (NESA)
  - [Peripheral Component Interconnect](../Page/Peripheral_Component_Interconnect.md "wikilink") (PCI)
  - [XTバス](../Page/XTバス.md "wikilink")
  - [VESA ローカルバス](../Page/VESA_ローカルバス.md "wikilink")
  - [コンパクトPCI](https://ja.wikipedia.org/wiki/コンパクトPCI "wikilink")

## 外部リンク

  - [EISA bus technical summary](http://www.techfest.com/hardware/bus/eisa.htm)

[Category:コンピュータバス規格](https://ja.wikipedia.org/wiki/Category:コンピュータバス規格 "wikilink")