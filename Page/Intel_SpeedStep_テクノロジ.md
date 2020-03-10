> この記事は[Intel SpeedStep ](https://ja.wikipedia.org/wiki/Intel_SpeedStep_)から翻訳されています。


**Intel SpeedStep テクノロジ**（インテル スピードステップ テクノロジ 、*Intel SpeedStep Technology*）は[Pentium IIIから搭載された](../Page/Pentium_III.md "wikilink")[インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")の省電力技術。単に**SpeedStep**とも呼ばれる。拡張規格の**Enhanced Intel SpeedStep Technology**（略称: **EIST**）も存在する。

## 概要

SpeedStepは、[バッテリー駆動のポータブル](../Page/二次電池.md "wikilink")[PC向けに開発された](../Page/パーソナルコンピュータ.md "wikilink")、[CPU](../Page/CPU.md "wikilink")の消費電力を抑える技術である。 省消費電力はそれまではあまり省みられない分野だったが、[トランスメタ](https://ja.wikipedia.org/wiki/トランスメタ "wikilink")が[Crusoe](https://ja.wikipedia.org/wiki/Crusoe "wikilink")で省電力を最大の武器に[x86アーキテクチャ](https://ja.wikipedia.org/wiki/x86アーキテクチャ "wikilink")CPU市場に参入するなど、競合する製品に危機感を抱いたインテルは従来製品を小改良にて競合できるようにする必要に迫られ、SpeedStepを開発するに至った。

バッテリー駆動か[商用電源](https://ja.wikipedia.org/wiki/商用電源 "wikilink")駆動かを判断し、バッテリー駆動ならCPUの動作周波数と駆動電圧を落として消費電力を低減させる。また、一部のユーティリティを利用すれば電源に依存せずに動作モードを切り替えることができる。

前述のとおりポータブルPC向けに開発された技術だが、[デスクトップPC用CPUの消費電力も飛躍的に増大してきているため](../Page/デスクトップパソコン.md "wikilink")、EISTはデスクトップ用CPUにも搭載されている。開発コードネームは「Geyserville」。

## SpeedStep テクノロジ（第一世代）

Mobile [Pentium IIIプロセッサで最初に実装された省電力機能](../Page/Pentium_III.md "wikilink")。商用電源時の最大処理と電池電源時の省電力処理とで2種類の動作モードを備える。

## SpeedStep テクノロジ（第二世代）

Mobile Pentium III-MプロセッサとMobile [Pentium 4-Mプロセッサで実装された省電力機能](../Page/Pentium_4-M.md "wikilink")。従来は電源の違いでモード切替を行っていたが、電源によらず状況によるモードの切り替えも可能にした。開発コードネームは「Geyserville-II」。

## 拡張版 Intel SpeedStep テクノロジ (EIST)

拡張版 Intel SpeedStep テクノロジ (Enhanced Intel SpeedStep Technology、略称: EIST) は、その名の通りSpeedStepを拡張した規格である。従来のSpeedStepは処理能力では最大速と最低速の2種類のモードの切り替えだったが、EISTでは数段階の中間速が加えられた。最初のSpeedStepの導入時の説明でインテルは、CPUが動作している最大時としていない最低時の2種類だけで十分な省消費電力の効果があると言っていた。しかし[AMDやトランスメタといった競合他社の同等機能が多段階可変であった為にそれに追従したこと](https://ja.wikipedia.org/wiki/アドバンスト・マイクロ・デバイセズ "wikilink")、そしてメディア再生における、低い処理能力を連続して発生する状況では多段階の方が消費電力を抑えられるためと言える。EISTの発表後は電源の状態や可変段数は無関係にSpeedStep規格は全てEISTという名称になっている。開発コードネームは「Geyserville-III」。

[商用電源](https://ja.wikipedia.org/wiki/商用電源 "wikilink")にて稼動する、[サーバ](../Page/サーバ.md "wikilink")向けやデスクトップPC向けのCPUでは電池の消耗は考慮する必要はないが、処理能力の向上とともに消費電力が増大し、放熱や冷却にかかるコストが問題となっている。そのため、プロセッサの省電力モードは平均消費電力や発熱を抑えるために、必要不可欠な機能になりつつある。今後は[Celeron](https://ja.wikipedia.org/wiki/Celeron "wikilink")のごく一部を除き、ほぼ全てのCPUに標準装備となるようである。

## 関連項目

  - [インテル ターボ・ブースト・テクノロジー](https://ja.wikipedia.org/wiki/インテル_ターボ・ブースト・テクノロジー "wikilink")
  - [PowerNow\!](../Page/PowerNow!.md "wikilink") - AMDによる省電力技術
  - [Cool'n'Quiet](https://ja.wikipedia.org/wiki/Cool'n'Quiet "wikilink") - AMDによる省電力技術
  - [LongRun](https://ja.wikipedia.org/wiki/LongRun "wikilink") - [トランスメタ](https://ja.wikipedia.org/wiki/トランスメタ "wikilink")による省電力技術
  - [PowerTune](https://ja.wikipedia.org/wiki/PowerTune "wikilink") - [IBM](../Page/IBM.md "wikilink") [PowerPC 970の省電力技術](../Page/PowerPC_970.md "wikilink")

[Category:CPU](https://ja.wikipedia.org/wiki/Category:CPU "wikilink") [Category:クロック](https://ja.wikipedia.org/wiki/Category:クロック "wikilink")