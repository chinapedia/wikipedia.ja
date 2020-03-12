> この記事は[ISCII](https://ja.wikipedia.org/wiki/ISCII)から翻訳されています。


**ISCII** (**I**ndian **S**cript **C**ode for **I**nformation **I**nterchange 、情報交換用インド文字符号 IS13194:1991) は[インド](../Page/インド.md "wikilink")の各種書記系を表現するための符号化方式である。主要な[インド系文字とローマ字転写を符号化する](../Page/ブラーフミー系文字.md "wikilink")。対応している用字系は以下の通り: [アッサム文字](https://ja.wikipedia.org/wiki/アッサム文字 "wikilink")、[ベンガル文字](https://ja.wikipedia.org/wiki/ベンガル文字 "wikilink")、[デーヴァナーガリー](https://ja.wikipedia.org/wiki/デーヴァナーガリー "wikilink")、[グジャラーティー文字](../Page/グジャラーティー文字.md "wikilink")、[グルムキー文字](../Page/グルムキー文字.md "wikilink")、[カンナダ文字](https://ja.wikipedia.org/wiki/カンナダ文字 "wikilink")、[マラヤーラム文字](https://ja.wikipedia.org/wiki/マラヤーラム文字 "wikilink")、[オリヤー文字](../Page/オリヤー文字.md "wikilink")、[タミル文字](https://ja.wikipedia.org/wiki/タミル文字 "wikilink")、および[テルグ文字](https://ja.wikipedia.org/wiki/テルグ文字 "wikilink")。ISCIIは[アラビア文字](../Page/アラビア文字.md "wikilink")に基づく書記系を符号化しないが、それにもかかわらず、[カシミール語](../Page/カシミール語.md "wikilink")、[シンド語](../Page/シンド語.md "wikilink")、[ウルドゥー語](../Page/ウルドゥー語.md "wikilink")、[ペルシア語](https://ja.wikipedia.org/wiki/ペルシア語 "wikilink")、[パシュトー語](../Page/パシュトー語.md "wikilink")および[アラビア語](../Page/アラビア語.md "wikilink")の書記系切り替え符号が提供されている。アラビア文字に基づく書記系は、その後[PASCII](../Page/PASCII.md "wikilink")文字コードで符号化された。

[ブラーフミー文字](../Page/ブラーフミー文字.md "wikilink")から派生した書記系はそのほとんどが類似した構造を持つが、文字の形状が異なるため、ISCIIは同じ音価の文字を同じ符号位置に符号化して、各種の用字系を重ね合わせている。たとえば、ISCII符号0xB3 0xDBはを表す。これはデーヴァナーガリーではのように、グルムキー文字ではのように、そしてタミル文字ではのように描画される。書記系はリッチテキストではマークアップによって選択され、プレーンテキストでは後述のATRを用いて選択される。

単一の符号化を使用する動機の1つは、ある書記系から他のものへの[翻字](../Page/翻字.md "wikilink")が容易になることである。しかしながら、あまりに非互換性が大きいためこれは実際には現実的な考えではない。[ISCIIについて](http://acharya.iitm.ac.in/multi_sys/exist_codes.php#Interchange)を参照。

ISCIIは固定長の8ビット符号である。下位128個の符号位置は[ASCII](https://ja.wikipedia.org/wiki/ASCII "wikilink")そのままで、上位128個の符号位置がISCII特有である。 ISCIIではデフォルトで使われる「デフォルト書記系」を指定する手段は提供されていない。

## ATR符号

文字を表現する符号位置に加え、ISCIIは略号がATR(0xE0)と呼ばれる符号位置が提供されている。ATRは書記系またはフォント属性の切り替えを指定する。

ATRに引き続き、0x42 - 0x4Bが指定された場合は、[デーヴァナーガリー](https://ja.wikipedia.org/wiki/デーヴァナーガリー "wikilink")（0x42）、[ベンガル文字](https://ja.wikipedia.org/wiki/ベンガル文字 "wikilink")（0x43）、[タミル文字](https://ja.wikipedia.org/wiki/タミル文字 "wikilink")（0x44）、[テルグ文字](https://ja.wikipedia.org/wiki/テルグ文字 "wikilink")（0x45）、 [アッサム文字](https://ja.wikipedia.org/wiki/アッサム文字 "wikilink")（0x46）、[オリヤー文字](../Page/オリヤー文字.md "wikilink")（0x47）、[カンナダ文字](https://ja.wikipedia.org/wiki/カンナダ文字 "wikilink")（0x48）、[マラヤーラム文字](https://ja.wikipedia.org/wiki/マラヤーラム文字 "wikilink")（0x49）、[グジャラーティー文字](../Page/グジャラーティー文字.md "wikilink")（0x4a）、[グルムキー文字](../Page/グルムキー文字.md "wikilink")（0x4b）へ切り替えられ、ふたたびATRによるデフォルト指定（0x40）または改行か別の書記系指定がくるまで続く。これらの指定が為されている間は、ASCIIの数字もまた、各書記系の数字で表示される。また、0x41が指定された場合は、ローマ字転写が表示される。

ATRに引き続き0x71 - 0x76が指定された場合は、[アラビア語](../Page/アラビア語.md "wikilink")（0x71）、[ペルシア語](https://ja.wikipedia.org/wiki/ペルシア語 "wikilink")（0x72）、[ウルドゥー語](../Page/ウルドゥー語.md "wikilink")（0x73）、[シンド語](../Page/シンド語.md "wikilink")（0x74）、[カシミール語](../Page/カシミール語.md "wikilink")（0x75）、[パシュトー語](../Page/パシュトー語.md "wikilink")（0x76）などの[アラビア文字](../Page/アラビア文字.md "wikilink")系が表示されることになっているが、ISCIIではそれらの詳細を規定していない。

ATRに引き続き、0x30 - 0x39が指定された場合は、太字や斜体、下線付き、倍幅などの表示モードを指定する。ATRの詳細な用法はISCIIの附属書Eに規定されている。

## EXT符号

ISCIIはさらに、EXT(0xF0)と呼ばれる符号位置を利用することで、[ヴェーダ](../Page/ヴェーダ.md "wikilink")文字を使用することができる。ヴェーダ文字は[デーヴァナーガリー](https://ja.wikipedia.org/wiki/デーヴァナーガリー "wikilink")の拡張と考えることができ、EXTを前置することで『[リグ・ヴェーダ](../Page/リグ・ヴェーダ.md "wikilink")』等で使用される調音記号や『[黒ヤジュル・ヴェーダ](https://ja.wikipedia.org/wiki/黒ヤジュル・ヴェーダ "wikilink")』や『[白ヤジュル・ヴェーダ](https://ja.wikipedia.org/wiki/白ヤジュル・ヴェーダ "wikilink")』特有の様々な[アヌスヴァーラ](https://ja.wikipedia.org/wiki/アヌスヴァーラ "wikilink")（鼻音）文字等を表現することができる。EXT指定によるヴェーダ文字については、ATRによる他の書記系やローマ字転写への指定は無視される。EXTで表現できる文字は、udātta（0xB6）やanudātta（0xBE）のような修飾文字（0xB4 - 0xBE）とそれ以外の非修飾文字（0xA1 - 0xB3）に分かれ、修飾文字は出現できる箇所が[デーヴァナーガリー](https://ja.wikipedia.org/wiki/デーヴァナーガリー "wikilink")の各音節の後か、または非修飾文字の後に限定されている。

## Unicodeとの対応

[Unicode](../Page/Unicode.md "wikilink")ではISCIIのようにATRで切り替えるのではなく、異なる文字体系については基本的に異なるブロックが割り当てられる。デーヴァナーガリーはU+0900、ベンガル・アッサム文字はU+0980、グルムキー文字はU+0A00、グジャラーティー文字はU+0A80、オリヤー文字はU+0B00、タミル文字はU+0B80、テルグ文字はU+0C00、カンナダ文字はU+0C80、マラヤーラム文字はU+0D00から始まるブロックを使用する。ヌクタ（点）つきの文字も独立した符号位置を持つ。ただし各ブロックの中の配列順はISCIIとの互換性が高い。

ISCIIでEXTを使って表現されるヴェーダ用の文字は2009年のUnicodeバージョン5.2で追加された\[1\]\[2\]。

ISCIIでハラント（[ヴィラーマ](https://ja.wikipedia.org/wiki/ヴィラーマ "wikilink")）とINV(D9)を使って表現される半体は、Unicodeではハラントと[ゼロ幅接合子](https://ja.wikipedia.org/wiki/ゼロ幅接合子 "wikilink")(ZWJ)を使用する。ISCIIではハラントを2回重ねて明示的にハラントつきの子音字を表示するが、Unicodeではハラントに[ゼロ幅非接合子](https://ja.wikipedia.org/wiki/ゼロ幅非接合子 "wikilink")(ZWNJ)を組み合わせる。

## ISCIIの利用状況

ISCIIは若干の政府機関で使われたのみで、広く使われることはなかったが、いまや[Unicode](../Page/Unicode.md "wikilink")によってほとんど時代遅れとなった。Unicodeはインド系文字の書記系ごとに分離したブロックを使っているが、おおむね各ブロック内でISCIIの配置を保存している。

なお、インドにはIS 13194（ISCII）の他に文字コード規格として、IS 10315 (ASCIIと同じ)、IS 12326 (ISO/IEC 2022と同じ）等がある。

## 脚注

## 参考資料

  -
## 外部リンク

  - [Padma - ISCIIをUnicodeに変換するMozilla拡張](http://padma.mozdev.org)
  - [Padma - ISCIIからUnicodeへの変換装置。テルグ文字用](http://web.archive.org/20050507120524/geocities.com/vnagarjuna/padma.html)

[Category:文字コード](https://ja.wikipedia.org/wiki/Category:文字コード "wikilink")

1.
2.