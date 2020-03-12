> この記事は[PSK31](https://ja.wikipedia.org/wiki/PSK31)から翻訳されています。


**PSK31**（[Phase Shift Keying](../Page/位相偏移変調.md "wikilink"), 31[ボー](../Page/ボー.md "wikilink") の略）とは、主に[アマチュア無線](https://ja.wikipedia.org/wiki/アマチュア無線 "wikilink")で用いられている[デジタル](../Page/デジタル.md "wikilink")[変調方式](../Page/変調方式.md "wikilink")である。2局間でリアルタイムの[チャット](../Page/チャット.md "wikilink")を行うために用いられている。[位相変調](../Page/位相変調.md "wikilink")の一つである。

## 歴史

PSK31はイギリスのアマチュア無線Peter Martinez (G3PLX)によって開発された。

  - その初期には、Martinezは[可変長コード](https://ja.wikipedia.org/wiki/可変長コード "wikilink")と呼んでいた。それは文字を表現するため([ハフマン符号](../Page/ハフマン符号.md "wikilink")を用いているためである。
  - 工学的には、可変長コードは[変調](https://ja.wikipedia.org/wiki/変調 "wikilink")の方法で、PSK31は送信の方法である。可変長コードは、頻度の高い文字には短いコードを、頻度の低い文字には長いコードを割り当てるもので、[モールス符号](../Page/モールス符号.md "wikilink")の方法に似ている。

## 使用法

実際には、PSK31は相対的に短いメッセージを2局間で交換するために用いられる。PSK31は[複信](../Page/複信.md "wikilink")（半二重通信）の一つである。そのため、同時に1局だけ送信を行うことができる。

## 妨害に対する強さ

PSK31は、音声（[電話](https://ja.wikipedia.org/wiki/電話_\(電波型式\) "wikilink")）やその他のデータ通信方式による信号の欠落に打ち勝つことができる。しかし、その遅い通信速度と、必要最低限の[誤り検出訂正](../Page/誤り検出訂正.md "wikilink")しか持たないことから、大容量データの[無線パケット通信](../Page/無線パケット通信.md "wikilink")には適さない。

PSK31は[位相](../Page/位相.md "wikilink")が保たれた[電波伝播](../Page/電波伝播.md "wikilink")では正常に動作するが、それが無い状況では通信できない。

運用者は信号を発生し、音声信号を復調するソフトウェアを用いる。変調信号は[送信機](../Page/送信機.md "wikilink")から高周波信号として変調される。

いくつかのソフトウェアは、それぞれ10ボーと5ボーで動作するPSK10とPSK05のモードに対応しており、雑音や[混信](../Page/混信.md "wikilink")に強く、低いスループットで動作する。

## 工学的資料

PSK31の音声帯域幅は非常に狭い（31.25[ヘルツ](../Page/ヘルツ.md "wikilink")、以下「Hz」）ため、[QRP](../Page/QRP.md "wikilink")運用や混雑している[周波数帯での運用に適している](../Page/アマチュア無線の周波数帯.md "wikilink")。

  - 31.25Hzの帯域幅は、タイピングの標準速度である1分間50語に対して約32ビット毎秒のビットレートを送信するものとして選択されている。
  - 31.25のビットレートは、多くのコンピューターの音声カードで用いられている8kHzの[サンプリング周波数](../Page/サンプリング周波数.md "wikilink")で用いられるように選択されている。31.25Hzは 8kHzを256で割った値であり、8kHzを8回分周した値である。
  - PSK31は[誤り訂正符号](https://ja.wikipedia.org/wiki/誤り訂正符号 "wikilink")を持たないが、4位相を用いた**QPSK31**では誤り訂正符号に対応する。

## 関連項目

  - [位相変調](../Page/位相変調.md "wikilink")
  - [RTTY](https://ja.wikipedia.org/wiki/RTTY "wikilink")

## 外部リンク

  - [PSK31 Info Page （英語）](http://www.psk31.com)

[Category:変調方式](https://ja.wikipedia.org/wiki/Category:変調方式 "wikilink") [Category:アマチュア無線](https://ja.wikipedia.org/wiki/Category:アマチュア無線 "wikilink")