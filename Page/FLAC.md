> この記事は[FLAC](https://ja.wikipedia.org/wiki/FLAC)から翻訳されています。


**FLAC**（フラック、）は、[オープンフォーマット](https://ja.wikipedia.org/wiki/オープンフォーマット "wikilink")の[可逆圧縮](../Page/可逆圧縮.md "wikilink")[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")である。

## 概要

可逆圧縮であるため、元の音声データからの音質の[劣化](https://ja.wikipedia.org/wiki/劣化 "wikilink")が無い。[2015年](../Page/2015年.md "wikilink")現在、[Ogg](https://ja.wikipedia.org/wiki/Ogg "wikilink")プロジェクトの可逆圧縮[コーデック](https://ja.wikipedia.org/wiki/コーデック "wikilink")として採用されている。通常のFLACファイル (.flac/.fla) だけでなく、[Ogg](https://ja.wikipedia.org/wiki/Ogg "wikilink")ファイル (.oga/.ogg) や[Matroska](https://ja.wikipedia.org/wiki/Matroska "wikilink")ファイル (.mkv/.mka) などの[メディアコンテナに格納することもできる](https://ja.wikipedia.org/wiki/コンテナフォーマット "wikilink")。

一部の変換ソフトには、無圧縮形式に変換可能なFLAC Uncompressedというオプションが用意されている。

[量子化ビット数は](https://ja.wikipedia.org/wiki/ビット深度_\(音響機器\) "wikilink")**4bit - 32bit**、[サンプリング周波数](../Page/サンプリング周波数.md "wikilink")は**1Hz - 655.3kHz (655,350Hz)**、チャンネル数は**1ch - 8ch**をサポートしている\[1\]。

[リファレンス実装](https://ja.wikipedia.org/wiki/リファレンス実装 "wikilink")は[オープンソース](../Page/オープンソース.md "wikilink")として開発されており、[ライセンス](https://ja.wikipedia.org/wiki/ライセンス "wikilink")に関しては以前は[GPLが適用されていたが](../Page/GNU_General_Public_License.md "wikilink")、Oggプロジェクトに加わった際にコアライブラリは修正版[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")へ変更された。

## 特徴

  - [エンコード](https://ja.wikipedia.org/wiki/エンコード "wikilink")・デコードが速い
      - エンコード時に圧縮率を高くするとエンコードが遅くなるが、[WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")とは異なり、デコード（再生）時において、CPUへの負荷の違いはなく高速にデコードできる\[2\]。
  - シークが速い
  - データ構造がエラーに強い
      - 前後のフレームに依存しないストリーマブルな構造であり、壊れた不完全なファイルでも実際に破損している箇所以外はデコードすることができる。
  - オープンフォーマットの可逆圧縮音声フォーマットとして広く使われており、商用でも採用される例が増えている
      - 一例として、アメリカの名門オーケストラ・[フィラデルフィア管弦楽団](https://ja.wikipedia.org/wiki/フィラデルフィア管弦楽団 "wikilink")は自らの楽団の演奏音源を[オンラインストア](http://www.thephiladelphiaorchestra.com/)で販売しているが、FLACのファイルも購入が可能になっている。
      - メタルバンドである[メタリカ](https://ja.wikipedia.org/wiki/メタリカ "wikilink")が自らのライヴ演奏音源を販売している[オンラインストア](http://www.livemetallica.com/)も、FLACのファイルの購入が可能になっている。
      - [ナイン・インチ・ネイルズ](https://ja.wikipedia.org/wiki/ナイン・インチ・ネイルズ "wikilink")のアルバム「Ghost I-IV」（$5でダウンロード販売）、「The Slip」（無料ダウンロード）はFLAC形式も入手可能となっている。
      - この他にも2009年3月時点では、[マージ・レコード](https://ja.wikipedia.org/wiki/マージ・レコード "wikilink")、[Linn Records](http://www.linnrecords.com/)、[Deutsche Grammophon](http://www2.deutschegrammophon.com/)などがFLACファイルのダウンロード販売を行っている。
      - [ビートルズ](https://ja.wikipedia.org/wiki/ビートルズ "wikilink")の2009年リマスターCD発売の際、USBメモリ版も発売され、FLAC形式の24bit高音質版が収録された。
      - 2010年7月7日より[オンキヨー](https://ja.wikipedia.org/wiki/オンキヨー "wikilink")（のち[オンキヨー&パイオニア](https://ja.wikipedia.org/wiki/オンキヨー&パイオニア "wikilink")イノベーションズに移管）が運営するe-onkyo musicでFLAC形式の楽曲の配信が始まった\[3\]。
      - [携帯音楽プレーヤー](https://ja.wikipedia.org/wiki/携帯音楽プレーヤー "wikilink")では、[Cowon](https://ja.wikipedia.org/wiki/Cowon "wikilink")製品、[Creative Zen](https://ja.wikipedia.org/wiki/Creative_Zen "wikilink")、[ソニー](../Page/ソニー.md "wikilink")・[ウォークマン](https://ja.wikipedia.org/wiki/ウォークマン "wikilink")の2012年以降の国内及び欧米モデルの一部\[4\]などが対応している。据え置き型のネットワークメディアプレーヤー、一部の[AVアンプ](https://ja.wikipedia.org/wiki/AVアンプ "wikilink")、高機能な[BDプレーヤー](https://ja.wikipedia.org/wiki/BDプレーヤー "wikilink")などにも対応する製品がある。
      - 2017年現在市販されている[カーオーディオ](https://ja.wikipedia.org/wiki/カーオーディオ "wikilink")では対応しているものが多い。
      - 2013年10月17日より[ソニーグループ](https://ja.wikipedia.org/wiki/ソニーグループ "wikilink")の[レーベルゲート](https://ja.wikipedia.org/wiki/レーベルゲート "wikilink")が運営する[mora](https://ja.wikipedia.org/wiki/mora "wikilink")でFLAC形式の楽曲の配信が始まった\[5\]。
      - 2019年4月現在、[オリンパス](https://ja.wikipedia.org/wiki/オリンパス "wikilink")から発売されている携帯型[リニアPCMレコーダー](https://ja.wikipedia.org/wiki/リニアPCMレコーダー "wikilink")「LS-P4」は一連のリニアPCMレコーダーとしては唯一、**FLACを用いた自己録音・再生に対応**している。
  - [Wave64](https://ja.wikipedia.org/wiki/WAV "wikilink"), [RF64フォーマットのサポートにより](https://ja.wikipedia.org/wiki/:en:RF64 "wikilink")、4GB以上のリニアPCMデータに対応

## 利用例

  - 音楽CDを一つのMKAファイルにまとめる（アルバム化）
      - (flac+cue).[mka](https://ja.wikipedia.org/wiki/Matroska "wikilink")

<!-- end list -->

  - 動画の音声部分としての利用
      - ([Theora](https://ja.wikipedia.org/wiki/Theora "wikilink")+FLAC).[ogv](https://ja.wikipedia.org/wiki/Ogg "wikilink")
      - ([DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")+FLAC).[mkv](https://ja.wikipedia.org/wiki/Matroska "wikilink")

<!-- end list -->

  - (FLAC).flac
  - (FLAC).fla
  - (FLAC).[oga](https://ja.wikipedia.org/wiki/Ogg "wikilink")
  - (FLAC).mka

## FLAC Uncompressed

FLACには無圧縮形式への変換がオプションとして用意されている。可逆圧縮形式のFLACと区別するために、無圧縮形式のFLACをFLAC Uncompressedとしている。

変換にはdBpowerAmpやXrecode II、Xrecode 3などの変換ソフトが必要。

## 脚注

### 注釈

### 出典

## 関連項目

  - [Apple Lossless](https://ja.wikipedia.org/wiki/Apple_Lossless "wikilink")
  - [ATRAC Advanced Lossless](https://ja.wikipedia.org/wiki/ATRAC#ATRAC_Advanced_Lossless "wikilink")
  - [La](https://ja.wikipedia.org/wiki/La_\(音声ファイルフォーマット\) "wikilink") (Lossless Audio)
  - [Monkey's Audio](../Page/Monkey's_Audio.md "wikilink")
  - [MPEG-4 ALS](https://ja.wikipedia.org/wiki/MPEG-4_ALS "wikilink")
  - [MPEG-4 SLS](https://ja.wikipedia.org/wiki/MPEG-4_SLS "wikilink")
  - [TAK](https://ja.wikipedia.org/wiki/TAK "wikilink") (Tom's lossless Audio Kompressor)
  - [TTA](https://ja.wikipedia.org/wiki/TTA "wikilink") (The True Audio)
  - [WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")
  - [WMA Lossless](https://ja.wikipedia.org/wiki/Windows_Media_Audio "wikilink")
  - [線形予測符号](https://ja.wikipedia.org/wiki/線形予測符号 "wikilink")
  - [線形予測法](https://ja.wikipedia.org/wiki/線形予測法 "wikilink")

## 外部リンク

  -
[Category:Xiph.Org](https://ja.wikipedia.org/wiki/Category:Xiph.Org "wikilink") [Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink") [Category:可逆圧縮アルゴリズム](https://ja.wikipedia.org/wiki/Category:可逆圧縮アルゴリズム "wikilink")

1.  [FLAC - format](https://xiph.org/flac/format.html#metadata_block_streaminfo)
2.  [1](http://wiki.hydrogenaud.io/index.php?title=Free_Lossless_Audio_Codec#Frequently_asked_questions). Free Lossless Audio Codec - Hydrogenaudio Knowledgebase. Retrieved 26 Sep 2015.
3.
4.
5.