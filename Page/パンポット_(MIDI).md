> この記事は[ \(MIDI\)](https://ja.wikipedia.org/wiki/_\(MIDI\))から翻訳されています。


**パンポット** () または**パン** () は、[MIDI](../Page/MIDI.md "wikilink")の[コントロールチェンジ](../Page/コントロールチェンジ.md "wikilink")のひとつで、音像定位を左右方向の任意の位置に設定する。コントロール番号10。

類似のコントロールチェンジに[バランス](https://ja.wikipedia.org/wiki/バランス・コントロール_\(MIDI\) "wikilink") (コントロール番号8) があり、ステレオスピーカーの左右の音量バランスを設定する。

## 仕様

MIDI規格では、値は0（左端）から127（右端）の範囲をとり、64を中央と定めている\[1\]。

[GM2](https://ja.wikipedia.org/wiki/GM2 "wikilink")の規定では、定位の異なる音が混在するようなリズム・チャンネルでは、パンポットは全体の定位を相対的に移動させる\[2\]。リズム・チャンネルでの音色（[ノート番号](https://ja.wikipedia.org/wiki/ノート番号 "wikilink")）ごとの定位は、[システム・エクスクルーシブのキーベースド](https://ja.wikipedia.org/wiki/MIDI#システムエクスクルーシブメッセージ "wikilink")・コントローラーで設定できる\[3\]。

RP-036 “Default Pan Curve” は、パン・カーブ（[パンロウ](https://ja.wikipedia.org/wiki/パンニング_\(音響\)#パンロウ "wikilink")）の実装にかかわる補則を加えており、正しい中央定位を得られることや、電力を保ったステレオチャンネル間配分をすることを求めている\[4\]。ここでは推奨される計算式が示されており、余弦波・正弦波ペアのパンロウを使用し、また値の実用範囲を1から127とすることで範囲の中央を64にしている（0と1は共に左端定位となる）。

## 出典

## 参考文献

## 関連項目

  - [パンニング (音響)](https://ja.wikipedia.org/wiki/パンニング_\(音響\) "wikilink")

[Category:MIDI](https://ja.wikipedia.org/wiki/Category:MIDI "wikilink")

1.
2.
3.
4.