> この記事は[Snow \(\)](https://ja.wikipedia.org/wiki/Snow_\(\))から翻訳されています。


**Snow**（スノー）は、Michael Niedermayerが開発している実験的なビデオ[コーデック](../Page/コーデック.md "wikilink")であり、その成果は[FFmpeg](../Page/FFmpeg.md "wikilink")パッケージにマージされている。

Snowは[離散ウェーブレット変換](../Page/離散ウェーブレット変換.md "wikilink")や[レンジコーダー](https://ja.wikipedia.org/wiki/Range_Coder "wikilink")、OBMC（Overlapped Block Motion Compensation）などの比較的新しい[符号化方式を用いる](../Page/エンコード.md "wikilink")。変換時に[フレームをブロック単位に分割する必要がない離散ウェーブレット変換と](../Page/コマ_\(映画・漫画\).md "wikilink")、マクロブロックを重ね合わせて[動き補償するOBMCによって](https://ja.wikipedia.org/wiki/フレーム間予測 "wikilink")、[ブロックノイズ](https://ja.wikipedia.org/wiki/ブロックノイズ "wikilink")とは無縁の圧縮を可能にしている。

また、ウェーブレット変換は原理的に離散コサイン変換に比べてモスキートノイズが発生しにくいという特徴もあり、この点で既存のビデオコーデックと比較して、視覚上の画質は向上しているとされる。[エントロピー符号](https://ja.wikipedia.org/wiki/エントロピー符号 "wikilink")に用いられるレンジコーダーも[算術符号](../Page/算術符号.md "wikilink")に比べて圧縮率では僅かに劣るが、より低い演算負荷が期待できる。

欠点として、エンコードおよびデコード負荷は既存のコーデックを大きく上回ることが挙げられる。また、開発中のため、これから先に仕様が変わる可能性も否定できず、実験目的以外の使用が実質できない。

## 関連項目

  - [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink")
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")
  - [FFmpeg](../Page/FFmpeg.md "wikilink")
  - [LiVES](https://ja.wikipedia.org/wiki/LiVES "wikilink")
  - [MPlayer](../Page/MPlayer.md "wikilink")
  - [VLCメディアプレーヤー](https://ja.wikipedia.org/wiki/VLCメディアプレーヤー "wikilink")
  - [オープンソースのコーデックとコンテナフォーマット一覧](https://ja.wikipedia.org/wiki/オープンソースのコーデックとコンテナフォーマット一覧 "wikilink")

## 外部リンク

  - [Snow discussion on the Doom9 forums](http://forum.doom9.org/showthread.php?s=&threadid=84593)
  - [ffdshow-tryouts](http://ffdshow-tryout.sourceforge.net/)
  - [FFmpeg's documentation on snow](http://svn.mplayerhq.hu/ffmpeg/trunk/doc/snow.txt?view=markup)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink")