> この記事は[TTA](https://ja.wikipedia.org/wiki/TTA)から翻訳されています。


**TTA** (ティーティーエー、**The True Audio**) は[フリー](../Page/フリーソフトウェア.md "wikilink")（[GPL](../Page/GNU_General_Public_License.md "wikilink")）のリアルタイム[可逆圧縮](../Page/可逆圧縮.md "wikilink")[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")[エンコーダー/デコーダーである](../Page/コーデック.md "wikilink")。可逆圧縮であるため音声の劣化がない。「ハードウェアサポートの容易さ」を目標に、開発が進められている。

デコード速度と再生時のハードウェア負荷で[FLAC](../Page/FLAC.md "wikilink")に劣り、圧縮率で[Monkey's Audioに劣る](../Page/Monkey's_Audio.md "wikilink")。エンコード速度と圧縮率のバランスに優れるが、最近の利用率では、より高レベルでデコードとエンコードの能力向上を果たした[TAK](../Page/TAK.md "wikilink")に押されつつある\[1\]。

[Matroska](../Page/Matroska.md "wikilink")コンテナ（.mkvや.mka）も対応している。

## TTA方式の長所

  - 可逆圧縮でオーディオデータを圧縮し、3割程度のファイルサイズ縮小が可能。
  - リアルタイムエンコード/デコードの[アルゴリズム](../Page/アルゴリズム.md "wikilink")を採用。
  - 動作環境に依存せず高速なエンコード/デコードが可能。
  - 複数の異なったプラットフォーム上でのコンパイル・実行が可能。
  - フリーの[オープンソース](../Page/オープンソース.md "wikilink")であり、技術情報が文書提供されている。
  - ハードウェアサポート実装。
  - [ID3タグ](../Page/ID3タグ.md "wikilink")、APEタグが利用可能（FLACは独自タグ、Monkey's AudioはAPEタグしか利用できない）。
      - ただし、これはID3タグやAPEタグを付加してもフォーマットとして互換性が保たれるという意味であり、公式に提供されているエンコーダ・デコーダやライブラリではタグの読み書きはサポートされていない。また、現行のDirectShowフィルターでは表示はできないため、[foobar2000](https://ja.wikipedia.org/wiki/foobar2000 "wikilink")のプラグインや[SuperTagEditor](https://ja.wikipedia.org/wiki/SuperTagEditor "wikilink")改造版などでしか解釈できない。

## 利用例

  - 音楽CDを一つのMKAファイルにまとめる
      - (tta+cue).mka
  - [MKA変換機](http://sonicdisorder.net/software.php)というツールを使用し、ファイルチェックモードを有効にしてMUXすれば、MUX前/DEMUX後のCRC16が一致するまで変換を試み（最大6パターン）、多くの場合はサンプル欠損を回避することが可能となっている。

## TTAを利用したコンテナ形式の一例

  - (TTA).tta
  - (TTA).mka
  - ([DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")+TTA).mkv

## 関連項目

  - [可逆圧縮](../Page/可逆圧縮.md "wikilink")
  - [音声圧縮](../Page/音声圧縮.md "wikilink")
  - [FLAC](../Page/FLAC.md "wikilink")
  - [Apple Lossless](../Page/Apple_Lossless.md "wikilink")
  - [Monkey's Audio](../Page/Monkey's_Audio.md "wikilink")
  - [TAK](../Page/TAK.md "wikilink")
  - [WMA Lossless](../Page/Windows_Media_Audio.md "wikilink")
  - [WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")
  - [foobar2000](https://ja.wikipedia.org/wiki/foobar2000 "wikilink")

## 脚註

<references/>

## 外部リンク

  - [TAU SOFTWARE](http://tausoft.org/)

<!-- end list -->

  - [MUSIC PC](http://sonicdisorder.net/) - MKA変換機の配布元

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink")

1.  [2009 ripping/encoding general poll - Hydrogenaudio Forums](http://www.hydrogenaudio.org/forums/index.php?showtopic=68338)