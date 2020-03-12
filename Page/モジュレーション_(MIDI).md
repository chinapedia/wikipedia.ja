> この記事は[ \(MIDI\)](https://ja.wikipedia.org/wiki/_\(MIDI\))から翻訳されています。


**モジュレーション**または**モジュレーション・デプス** () は、[MIDI](../Page/MIDI.md "wikilink")の[コントロールチェンジ](../Page/コントロールチェンジ.md "wikilink")のひとつ。モジュレーション・ホイールなどの操作によって、主に[ビブラート](../Page/ビブラート.md "wikilink")効果を与える際に使用される。コントロール番号1。

MIDIでのビブラート効果とは、[LFO](../Page/LFO_\(電子楽器\).md "wikilink")[ピッチ](../Page/音高.md "wikilink")[変調](https://ja.wikipedia.org/wiki/変調 "wikilink")であり、モジュレーション・デプスはその深さ（強さ）を制御する。なお、[ピッチベンド](../Page/ピッチベンド.md "wikilink")を使うことで、LFOによらないビブラートを表現することもできる。

## 仕様

値は0が効果無し（初期値）で、127で最大効果となる。下記の設定によって効果が調整できる（[GM2](https://ja.wikipedia.org/wiki/GM2 "wikilink")仕様）。GM2に満たない音源では、類似のパラメータがメーカー独自のNRPNやシステム・エクスクルーシブで設定できる場合もある。

  - レジスタード・パラメーター番号（RPN）[MSB](https://ja.wikipedia.org/wiki/MSB "wikilink") 0/[LSB](https://ja.wikipedia.org/wiki/LSB "wikilink") 5番「モジュレーション・デプス・レンジ」
    ビブラートの最大ピッチ変化量。初期値は50[セント](../Page/セント_\(音楽\).md "wikilink")。
  - コントロールチェンジ76番「サウンドコントローラー7：ビブラート・レイト」
    ビブラートの速さの加減。実装はメーカーの任意。
  - コントロールチェンジ77番「サウンドコントローラー8：ビブラート・デプス」
    ビブラートの深さの加減。実装はメーカーの任意。
  - コントロールチェンジ78番「サウンドコントローラー9：ビブラート・ディレイ」
    ビブラートが遅れて始まる時間の加減。実装はメーカーの任意。

モジュレーションの効果は、通常ビブラートであるが、[システム・エクスクルーシブ](https://ja.wikipedia.org/wiki/システム・エクスクルーシブ "wikilink")のコントローラー・ディスティネーション・セッティングによって、下記の効果を複数設定することもできる（[GM2](https://ja.wikipedia.org/wiki/GM2 "wikilink")仕様）。同様に[アフタータッチ](https://ja.wikipedia.org/wiki/アフタータッチ "wikilink")や別のコントロールチェンジにビブラート効果を設定することもできる。

  - ピッチ
  - [フィルター](../Page/VCF.md "wikilink")[カットオフ](https://ja.wikipedia.org/wiki/遮断周波数 "wikilink")
  - 音量
  - LFOピッチ変調（ビブラート）
  - LFOフィルターカットオフ変調
  - LFO音量変調（[トレモロ](../Page/トレモロ.md "wikilink")）

## 参考文献

  -
  -
  -
  -
  -
[Category:MIDI](https://ja.wikipedia.org/wiki/Category:MIDI "wikilink")