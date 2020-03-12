> この記事は[Cwav](https://ja.wikipedia.org/wiki/Cwav)から翻訳されています。


**Cwav**（シーワブ **CompressWave**）は、[WAV](../Page/WAV.md "wikilink")形式を独自に拡張して作成された音声データのフォーマットである。[拡張子](../Page/拡張子.md "wikilink")は.cwav。

[2007年](../Page/2007年.md "wikilink")現在、作者と思われる者のサイトが消滅しているため、詳細は不明である。

## 概要

Cwav形式は、[1990年代](../Page/1990年代.md "wikilink")後半に[Windows用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ゲーム](../Page/ゲーム.md "wikilink")に使用された形式である。 その後さらに圧縮が可能な[Vorbis](../Page/Vorbis.md "wikilink")や豊富なタグを持てる[MP3](../Page/MP3.md "wikilink")形式が普及し、ほとんど姿を消した。しかし、リピートや暗号化が比較的簡単なソースで扱えるため、今でも好んで使う作者もいる。

圧縮原理として、まず波形を表すビット数を差分数値に変換して16Bitから8Bitにする。その後[ハフマン符号](../Page/ハフマン符号.md "wikilink")による圧縮を行なう。差分数値をデータ化している都合上シークが不可能である。そのような仕様を抱えているのにもかかわらず、ループ開始ポイントを指定したループ再生は出来る。これはループ開始ポイントを再生時にそのときの絶対データを格納し、ループ終端にたどり着いたときに格納したデータで復帰する仕様である。

## Cwav形式のデータ的な特徴

  - 元データの3分の1から8分の1程度の[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")が可能
  - 簡易暗号化（符号無し32bit）
  - ディレイ無しでのリピート再生や、リピートの区間（[秒](../Page/秒.md "wikilink")で指定）や回数（0～254回。255で無限ループ）を設定可能。
  - 曲のタイトル・アーティスト名も入れること(最大128[バイト](../Page/バイト_\(情報\).md "wikilink"))が可能。
  - 特定の場所からの再生は不可(シークできない)

## 外部リンク

  - Ko-Taのバ・ー・ルのようなもの(2007/3/18の記事) (リンク切れ)
  - [cwav library & player](http://kota.dokkoisho.com/#cw)

## 関連項目

  - [Vorbis](../Page/Vorbis.md "wikilink")

[Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink")