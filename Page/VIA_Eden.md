> この記事は[VIA Eden](https://ja.wikipedia.org/wiki/VIA_Eden)から翻訳されています。


**VIA Eden**（ヴィア エデン） とは[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")[VIA Technologiesが推進するEdenPlatFormの中核に位置する](../Page/VIA_Technologies.md "wikilink")[x86](https://ja.wikipedia.org/wiki/x86 "wikilink")[CPU](../Page/CPU.md "wikilink")である。ほとんどの製品は取り外しのできない形で基板上に実装されている。パソコン用のみならず組み込み用途を強く意識した製品である。[セットトップボックス](https://ja.wikipedia.org/wiki/セットトップボックス "wikilink")、モバイル用、[POS用など低消費電力を期待される分野で多く採用が進んでいる](https://ja.wikipedia.org/wiki/POSシステム "wikilink")。名称でEdenという場合VIAのEdenシリーズすべてを指すので、以下の解説はそれぞれのシリーズに分けて解説する。

## Eden

[Estherコアを採用しIBMの](https://ja.wikipedia.org/wiki/VIA_C7 "wikilink")90nm[SOI](https://ja.wikipedia.org/wiki/SOI "wikilink")プロセスで製造されている。近年のCPUから比べるとやや非力ではあるが、オフィス用としては十分な性能をもつ。特にその消費電力対性能比は特筆すべきところがある。現在日本のコンピューターメーカが採用している事例は少ないが、個人向けの[マザーボード](https://ja.wikipedia.org/wiki/マザーボード "wikilink")は多数出回っている。

  - [FSB](https://ja.wikipedia.org/wiki/フロントサイドバス "wikilink")　400MHz　
  - 動作周波数　400MHz - 1.2GHz
  - 消費電力　
      - 400MHz　2.5W
      - 500MHz　3.5W
      - 600MHz, 800MHz, 1GHz　5W
      - 1.2GHz　7W
  - 対応チップセット　VIA CN700
  - パッケージ　nanoBGA2 21mmx21mm
  - 対応拡張命令　[MMX](https://ja.wikipedia.org/wiki/MMX "wikilink")、[SSE](https://ja.wikipedia.org/wiki/ストリーミングSIMD拡張命令 "wikilink")、SSE2、SSE3、[NXビット](https://ja.wikipedia.org/wiki/NXビット "wikilink")
  - ハードウエア処理命令　[AES暗号処理](../Page/Advanced_Encryption_Standard.md "wikilink"), [SHA-1](https://ja.wikipedia.org/wiki/SHA-1 "wikilink"), [SHA-2](https://ja.wikipedia.org/wiki/SHA-2 "wikilink")56
  - デュアルCPU対応

## Eden ULV

上記の無印Edenと同様にEstherコアを採用し、IBMの90nmSOIプロセスで製造されている。このシリーズの特徴としては、同クロックの無印Edenと比べて消費電力が低く抑えられている。特にEden ULV 500MHzのTDPは他のx86CPUの中でも極めて低い1Wである。

  - FSB　400MHz　
  - 動作周波数　500MHz - 1.5GHz
  - 消費電力　
      - 500MHz　1W
      - 1GHz　3.5W
      - 1.5GHz　7.5W
  - 対応チップセット　VIA CN700, VIA CX700, VIA CX700M
  - パッケージ　nanoBGA2 21mmx21mm
  - 対応拡張命令　MMX, SSE, SSE2, SSE3, NX Bit
  - ハードウエア処理命令　AES暗号処理, SHA-1, SHA-256
  - デュアルCPU対応

## Eden-N

2007年3月現在、世界最小のx86互換CPUである。上記のに製品よりもさらに消費電力を落とす必要のある製品向けに作られている。C5P [Nehemiahを採用している](https://ja.wikipedia.org/wiki/VIA_C3#Nehemiah "wikilink")。FSBには旧世代の133MHzを使用しさらに消費電力を下げている。

  - FSB　133MHz　
  - 動作周波数　533MHz - 1.0GHz
  - 消費電力　
      - 533MHz　2.5W
      - 800MHz　5W
      - 1GHz　7W
  - 対応チップセット　VIA CN400
  - パッケージ　nanoBGA 15mmx15mm
  - 対応拡張命令　MMX, SSE
  - ハードウエア処理命令　AES暗号処理
  - デュアルCPU対応

## Eden ESP

[Samuel2を採用した](https://ja.wikipedia.org/wiki/VIA_C3#Samuel2_\(C5B\) "wikilink")150nm版とC5LXもしくはC5P [Nehemiahを採用した](https://ja.wikipedia.org/wiki/VIA_C3#Nehemiah "wikilink")130nmとがある。Edenシリーズで唯一66MHzFSBという低速なバスでも動作する。それぞれのコアによってサポートされる拡張命令が異なるが、各CPUのCPUIDがSamuel2:670，C5XL Nehemiah:690，C5P Nehemiah:698であるため、区別することができる。仕様は、現在のパソコン性能から比べると満足というのからは程遠く、完全に組み込み向け用途として市場からは扱われている。

### Eden ESP 150nm

  - FSB　66MHz - 133MHz
  - 動作周波数　300MHz - 600MHz
  - 消費電力
      - 300MHz　2.5W
      - 400MHz　3W
      - 533MHz　5W
      - 600MHz　6W
  - 対応チップセット　VIA CN400, VIA CLE266
  - パッケージ　EBGA 35mmx35mm
  - 対応拡張命令　MMX, [3DNow\!](https://ja.wikipedia.org/wiki/3DNow%21 "wikilink")

### Eden ESP 130nm

  - FSB　133MHz - 200MHz
  - 動作周波数　733MHz - 1.0GHz
  - 消費電力
      - 733MHz, 800MHz　6W
      - 1GHz　7W
  - 対応チップセット　VIA CN400
  - パッケージ　EBGA 35mmx35mm
  - 対応拡張命令　MMX SSE
  - ハードウエア処理命令　AES暗号処理(C5P Nehemiahのみ)
  - デュアルCPU対応(C5P Nehemiahのみ)

## 関連情報

  - [VIA Technologies](../Page/VIA_Technologies.md "wikilink")
  - [VIA C3](https://ja.wikipedia.org/wiki/VIA_C3 "wikilink")
  - [Geode](https://ja.wikipedia.org/wiki/Geode "wikilink")
  - [組み込みシステム](../Page/組み込みシステム.md "wikilink")

## 外部リンク

  - [VIA](http://www.viatech.co.jp/jp/index.jsp)
  - [VIA Eden](http://www.viatech.co.jp/jp/products/processors/eden/)

[Category:マイクロプロセッサ](https://ja.wikipedia.org/wiki/Category:マイクロプロセッサ "wikilink")