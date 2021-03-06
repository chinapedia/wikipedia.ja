> この記事は[トリプルDES](https://ja.wikipedia.org/wiki/トリプルDES)から翻訳されています。


[3des-overall-view.png](https://ja.wikipedia.org/wiki/File:3des-overall-view.png "fig:3des-overall-view.png") **トリプルDES**（**トリプルデス、**[英語](../Page/英語.md "wikilink"): **Triple DES**、**3DES**）とは、[共通鍵](https://ja.wikipedia.org/wiki/共通鍵 "wikilink")[ブロック暗号](../Page/ブロック暗号.md "wikilink")である[DESを](../Page/Data_Encryption_Standard.md "wikilink")3回施す[暗号](../Page/暗号.md "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")。正式名称は**Triple Data Encryption Algorithm**(**TDEA**、**Triple DEA**)。時代の流れに伴い、鍵長56ビットのDESでは[総当たり攻撃](../Page/総当たり攻撃.md "wikilink")への耐性が低くなったことから、これを補う目的で考案された。

## 概要

平文を単にDESで3回暗号化するのではなく、暗号化→復号→暗号化の順に施す暗号アルゴリズムである。

  -
    C = encrypt<sub>k<sub>3</sub></sub>(decrypt<sub>k<sub>2</sub></sub>(encrypt<sub>k<sub>1</sub></sub>(P)))

ただし

  -
    P ... [平文](../Page/平文.md "wikilink")
    C ... [暗号文](../Page/暗号文.md "wikilink")
    k<sub>i</sub> ... 鍵 \#i
    encrypt, decrypt ... DES

この[鍵](https://ja.wikipedia.org/wiki/鍵 "wikilink")の選択について3つのオプションが存在する。

  - Keying option 1
    k<sub>1</sub>, k<sub>2</sub>, k<sub>3</sub> すべてが異なる場合。
    3 × 56 = 168ビットの鍵長となるが、既知の攻撃法が存在するため実質的な暗号強度は112ビット程度となる。3TDEA、3-key 3DES などと呼ばれる。
  - Keying option 2
    k<sub>1</sub> と k<sub>2</sub> が異なり、k<sub>3</sub> = k<sub>1</sub> の場合。
    2 × 56 = 112ビットの鍵長となるが、既知の攻撃法が存在するため実質的な[暗号強度](https://ja.wikipedia.org/wiki/暗号強度 "wikilink")はせいぜい80ビットとされる。中間一致攻撃への耐性があるため、単純にDESで2回暗号化するよりは安全である。2TDEA、2-key 3DES などと呼ばれる。
  - Keying option 3
    k<sub>1</sub> = k<sub>2</sub> = k<sub>3</sub>の場合。
    DESと同じであり、56ビットの鍵長を持つ。このオプションにより、トリプルDESはDESに対して[上位互換性](https://ja.wikipedia.org/wiki/上位互換性 "wikilink")を持つ（DESによって暗号化された文章をトリプルDESで復号できる。）

## 理論

3つの鍵{k<sub>1</sub>,k<sub>2</sub>,k<sub>3</sub>}を使うトリプルDES (-EEE) が、1つの鍵k<sub>4</sub>でDESを行う場合よりも安全性が向上するかが問題となる。ここで任意の{k<sub>1</sub>、k<sub>2</sub>、k<sub>3</sub>}について

  -
    C1 = DES\<k<sub>3</sub>\>( DES\<k<sub>2</sub>\>( DES\<k<sub>1</sub>\>( P ) ) )
    C2 = DES\<k<sub>4</sub>\>( P )

とすると、全てのPについてC1 == C2となるk<sub>4</sub>が存在するならば、トリプルDES (-EEE) の鍵空間はDESと同じであり、安全性は向上しないことになる。この問題について、任意の{k<sub>1</sub>,k<sub>2</sub>}に対して、DES\<k<sub>2</sub>\>( DES\<k<sub>1</sub>\>( \* ) ) == DES\<k<sub>3</sub>\>( \* ) となるk3は存在しないことが証明され、DESを多段にすることで鍵空間は拡大できることが示された。つまり、DESは[群をなさない](https://ja.wikipedia.org/wiki/群_\(数学\) "wikilink")。

## 安全性

一般的にトリプルDESでは3つの異なる鍵 (Keying option 1) を用いて168ビットの鍵長を持っているが、中間一致攻撃により安全性は112ビット相当となる。2つの異なる鍵 (Keying option 2) を用いる場合は112ビットの鍵長を持っているが、[選択平文攻撃](https://ja.wikipedia.org/wiki/選択平文攻撃 "wikilink")または既知平文攻撃により安全性はせいぜい80ビット相当とされる。112ビットであっても総当たりには相当なコンピュータパワーが必要となるが、年々の性能向上を考慮し、[アメリカ国立標準技術研究所](../Page/アメリカ国立標準技術研究所.md "wikilink")は2030年までに使用をやめるよう推奨している。

## 実利用

DESと同じアルゴリズムで簡単に実装できることから、ICカードの共通仕様であるEMVなどをはじめ現在でも広く利用されている。

ただし、安全性が実質112ビットまでとなることや、DESを3回施すことで計算負荷も3倍となることから、現在はより安全で高速な[AESに置き換わりつつある](../Page/Advanced_Encryption_Standard.md "wikilink")。AESをサポートしておらず、トリプルDESまでの対応にとどまる[Windows XP等への下位互換性を維持する目的等で使われた](../Page/Microsoft_Windows_XP.md "wikilink")。

## 実装ライブラリ

トリプルDESをサポートしているライブラリは以下の通り。

  - [Botan](https://ja.wikipedia.org/wiki/Botan "wikilink")

  -
  -
  -
  -
  -
  - [OpenSSL](https://ja.wikipedia.org/wiki/OpenSSL "wikilink")

  - [wolfSSL](https://ja.wikipedia.org/wiki/wolfSSL "wikilink")

（上記のライブラリの中の最近のバージョンでは、デフォルトビルドでトリプルDESが有効でないものもある。）

## 出典

<references />

## 参照文献

  -
  -
## 関連項目

  - [DES](../Page/Data_Encryption_Standard.md "wikilink") - [DES-X](https://ja.wikipedia.org/wiki/DES-X "wikilink")
  - [暗号](../Page/暗号.md "wikilink")
  - [暗号理論](../Page/暗号理論.md "wikilink")
  - [多重暗号](https://ja.wikipedia.org/wiki/多重暗号 "wikilink") / [カスケード暗号](https://ja.wikipedia.org/wiki/カスケード暗号 "wikilink")