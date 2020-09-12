> この記事は[OCRA](https://ja.wikipedia.org/wiki/OCRA)から翻訳されています。


**OCRA** (Open Source Console for Real-Time Acquisition) は、[オープンソース](../Page/オープンソース.md "wikilink")の[MRI](https://ja.wikipedia.org/wiki/MRI "wikilink")のプロジェクト。

## 概要

従来の[MRI](https://ja.wikipedia.org/wiki/MRI "wikilink")は1台が数千万円するため、[開発途上国](../Page/開発途上国.md "wikilink")など、購入資金の乏しい地域では普及の障害になっていた。OCRA(Open Source Console for Real-Time Acquisition)は[ソフトウェア無線](../Page/ソフトウェア無線.md "wikilink")の技術を利用することにより[水素原子](../Page/水素原子.md "wikilink")の偏極用の[磁石](../Page/磁石.md "wikilink")を含まず、$500未満の装置で磁気共鳴画像の取得を目指す\[1\]\[2\]。

## ハードウェア

[ソフトウェア無線](../Page/ソフトウェア無線.md "wikilink")の汎用的なハードウェアである[Red Pitayaを高周波信号の送受信機と](https://ja.wikipedia.org/wiki/Red_Pitaya "wikilink")[任意波形発生器](https://ja.wikipedia.org/wiki/任意波形発生器 "wikilink")として使用する。汎用的なハードウェアを使用する事により、ハードウェアの入手性が高くなり、開発は主に[FPGA](../Page/FPGA.md "wikilink")の信号処理部とソフトウェアが中心になり、従来のMRIの同規模の装置と比較してコストを大幅に抑えることが可能になる。取得した信号を[高速フーリエ変換](../Page/高速フーリエ変換.md "wikilink")して画像を再構成する。

## 仕様

  - 周波数：0〜40 MHz（より高い周波数の場合、外部ミキサーが必要）\[3\]
  - 基板： STEMLab / Red Pitaya 125-14ボード、ザイリンクスZynq 7010 SoC\[4\]
  - Red Pitaya上のその他のハードウェア：2つの125 Msps 14ビット分解能ADC、2つの125Msps 14ビット解像度DAC、16本のDIO\[5\]
  - その他の外部ハードウェア：3個のAD5780 18ビット分解能DAC（勾配波形用）\[6\]

## 用途

従来は取得費用が高額故に普及が困難だった開発途上国での普及や低所得者層の診断や学生の教育用途等を想定している。

## 課題

信号処理部は確かに廉価にできるものの、偏極用の磁石が依然高価であり、勾配地場の発生には専用のハードウェアを要するためシステム全体のコストの低減にはまだ余地がある。水素原子の偏極用の磁石は読み取り時の磁場とは異なり、磁場強度の高い均一性は求められないものの、読み取り時には高い均一性を求められる。

## 出典

## 関連資料

  - Twieg, Michael, et al. "[An Open Source Mobile NMR Relaxometry Platform.](https://gate.nmr.mgh.harvard.edu/wiki/Tabletop_MRI/images/a/a0/Relaxometer_griswold.pdf)" 22nd ISMRM (2013).

## 外部リンク

  -
[Category:ソフトウェア無線](https://ja.wikipedia.org/wiki/Category:ソフトウェア無線 "wikilink") [Category:核磁気共鳴](https://ja.wikipedia.org/wiki/Category:核磁気共鳴 "wikilink") [Category:オープンソースハードウェア](https://ja.wikipedia.org/wiki/Category:オープンソースハードウェア "wikilink")

1.  Anand, Suma. [OCRA: a low-cost, open-source FPGA-based MRI console capable of real-time control](https://dspace.mit.edu/bitstream/handle/1721.1/121619/1098041021-MIT.pdf?sequence=1&isAllowed=y). Diss. Massachusetts Institute of Technology, 2018.
2.
3.
4.  [What is OCRA MRI?](https://openmri.github.io/ocra/)
5.
6.