> この記事は[UNIVAC 1101](https://ja.wikipedia.org/wiki/UNIVAC_1101)から翻訳されています。


[thumb](https://ja.wikipedia.org/wiki/画像:UNIVAC-1101BRL61-0901.jpg "wikilink") **UNIVAC 1101** は、[1950年代](../Page/1950年代.md "wikilink")に[エンジニアリング・リサーチ・アソシエイツ](https://ja.wikipedia.org/wiki/エンジニアリング・リサーチ・アソシエイツ "wikilink")（ERA）が設計し[レミントンランド](../Page/レミントンランド.md "wikilink")が製造した[コンピュータ](../Page/コンピュータ.md "wikilink")システム。**ERA 1101**とも。アメリカでの最初の[ノイマン型](../Page/ノイマン型.md "wikilink")コンピュータである。

## 概要

当初、[アメリカ海軍](../Page/アメリカ海軍.md "wikilink")艦船局（実際には[NSA](../Page/アメリカ国家安全保障局.md "wikilink")）向けに *Atlas* の名で設計され（Barnaby という漫画の登場人物\[[http://www.ksu.edu/english/nelp/purple/characters/cartoons.html\#atlas\]から名づけられた](http://www.ksu.edu/english/nelp/purple/characters/cartoons.html#atlas%5Dから名づけられた)）、商用版は 1101 と改称した（"Task 13" として設計されたため、13を[二進法](../Page/二進法.md "wikilink")で表記して1101となった）。

長さ11.5メートル、幅6メートルで、論理回路には2700本の[真空管](../Page/真空管.md "wikilink")を使っている。[磁気ドラムメモリ](../Page/磁気ドラムメモリ.md "wikilink")は直径21.6cmで3500rpmで回転し、200個のヘッドがある。これに16,384ワード（1ワード24ビットなので、48[KB](../Page/キロバイト.md "wikilink")）を保持し、アクセス時間は32μ秒から17m秒であった。

命令は24ビットで、そのうち6ビットが命令コード、4ビットがスキップ値（プログラム上、次の命令までスキップすべきワード数）、14ビットがメモリアドレスである。数値は二進数で表現され、負の数は[1の補数で表されている](../Page/符号付数値表現.md "wikilink")。加算には96μ秒、乗算には352μ秒かかった。

48ビット[アキュムレータが](../Page/アキュムレータ_\(コンピュータ\).md "wikilink")1つあり、基本的に減算を行うため、加算は1の補数に変換した上で減算を行うことで実現されていた。奇妙に思えるかもしれないが、この方が1の補数表現に特有の負のゼロ（[-0](https://ja.wikipedia.org/wiki/-0 "wikilink")）を生成する可能性が少なくなる。

UNIVAC 1101 には全部で38種類の[命令があった](../Page/命令セット.md "wikilink")。

## 歴史

ERAは海軍艦船局向けに2台の *Atlas* を[1950年](../Page/1950年.md "wikilink")12月と[1953年](https://ja.wikipedia.org/wiki/1953年 "wikilink")3月に納入した。商用版を *MABEL* にするという案もあったが、Jack Hill が 1101 という名称を提案した。**ERA 1101** は[1951年](https://ja.wikipedia.org/wiki/1951年 "wikilink")12月に発表された。

ERAは3台目を自社内に置き、計算サービスを他社に提供しようと考えていた。しかしこれは失敗し、[1954年](../Page/1954年.md "wikilink")11月、レミントンランドがその（約50万ドルの価値がある）マシンを[ジョージア工科大学](../Page/ジョージア工科大学.md "wikilink")に寄贈した。NSAの2台のマシンは[1956年](../Page/1956年.md "wikilink")ごろに[磁気コアメモリ](../Page/磁気コアメモリ.md "wikilink")にアップグレードされている。[1958年](../Page/1958年.md "wikilink")11月、ジョージア工科大学でも4096ワードの磁気コアメモリにアップグレードしており、39,400ドルかかっている。同大学では 1101 は[1961年](https://ja.wikipedia.org/wiki/1961年 "wikilink")ごろまで使われていた。

## 命令セット

| 摘要                        |                                  |
| ------------------------- | -------------------------------- |
| y はアドレス y のメモリを意味する。      | X = Xレジスタ（24桁）                   |
| ( ) はその内容を意味する。           | Q = Qレジスタ（24桁）                   |
| \-                        | A = アキュムレータ（48桁）                 |
| **算術命令**                  |                                  |
| (y) を A にインサート（ロード）       | (y) の補数を A にインサート                |
| (y) を A にインサート（倍精度）       | (y) の補数を A にインサート（倍精度）           |
| (y) の絶対値を A にインサート        | (y) の絶対値の補数を A にインサート            |
| (y) を (A) に加算             | (y) を (A) から減算                   |
| (y) を (A) に加算（倍精度）        | (y) を (A) から減算（倍精度）              |
| (y) の絶対値を (A) に加算         | (y) の絶対値を (A) から減算               |
| (Q) を A にインサート            | A の右半分をクリア                       |
| (Q) を (A) に加算             | (A) を Q に移す                      |
| \[(y) + 1\] を A にインサート    |                                  |
| **乗除算命令**                 |                                  |
| (Q) \* (y) の積を A に        | (Q) \* (y) の論理積を (A) に加算         |
| (Q) \* (y) の論理積を A に      | (A) を (y) で割る（商は Q に、非負の余りは A に） |
| (Q) \* (y) の積を (A) に加算    |                                  |
| **論理命令と制御フロー命令**          |                                  |
| (A) の右半分を y にストア          | (A) を左にシフト                       |
| (Q) を y にストア              | (Q) を左にシフト                       |
| (Q) を演算子として (y) を (A) で置換 | (y) を次の命令とする                     |
| (y) を (A) で置換（アドレス部分だけ）   | (A) がゼロでない場合、(y) を次の命令とする        |
| (y) を Q にインサート            | (A) が負の場合、(y) を次の命令とする           |
|                           | (Q) が負の場合、(y) を次の命令とする           |
| **入出力命令と制御命令**            |                                  |
| (y)の右半分6桁を印字する            | オプション停止                          |
| (y)の右半分6桁を印字しパンチする        | 即時停止                             |
|                           | 最終停止                             |

## 関連項目

  - [UNIVAC](../Page/UNIVAC.md "wikilink")
      - [UNIVAC 1103](../Page/UNIVAC_1103.md "wikilink") - 後継機種

## 外部リンク

  - [*Engineering Research Associates and the Atlas Computer (UNIVAC 1101)*](http://www.cc.gatech.edu/~randy/folklore/v3n3.html) by George Gray,
    from the Unisys History Newsletter, Volume 3, Number 3, June, 1999
  - *Introducing the ERA 1101: An operationally proven high-speed, electronic, general purpose digital computer*, ERA, no-date. (8 pp) [1](http://ed-thelen.org/comp-hist/ERA-1101-f09-IntroductingERA1101.pdf)
  - [*ERA 1101 Documents*](http://ed-thelen.org/comp-hist/ERA-1101-documents.html) by H. C. Snyder USN

[Category:コンピュータ_(歴代)](https://ja.wikipedia.org/wiki/Category:コンピュータ_\(歴代\) "wikilink") [Category:UNIVACのメインフレーム](https://ja.wikipedia.org/wiki/Category:UNIVACのメインフレーム "wikilink") [Category:真空管式コンピュータ](https://ja.wikipedia.org/wiki/Category:真空管式コンピュータ "wikilink")