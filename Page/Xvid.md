> この記事は[Xvid](https://ja.wikipedia.org/wiki/Xvid)から翻訳されています。


**Xvid**（エックスブイアイディー、エックスビド）は[オープンソース](../Page/オープンソース.md "wikilink")で開発されている[フリーのビデオ](../Page/フリーウェア.md "wikilink")[コーデック](../Page/コーデック.md "wikilink")。[MPEG-4 ASP](https://ja.wikipedia.org/wiki/MPEG-4#MPEG-4_.28Part_2.29 "wikilink") (Advanced Simple Profile)に準拠している。 [2006年](../Page/2006年.md "wikilink")[10月](https://ja.wikipedia.org/wiki/10月 "wikilink")までは**XviD**という名称でリリースされた。

## 概要

元々、DivXNetworks社がはじめたOpenDivXプロジェクトで生まれたものだったが、その後 DivXNetworks社（現：DivX .Inc）の方針転換により商用製品路線へと[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")コーデックが移行した。その際、このプロジェクトによって生み出された成果はそのまま商用コーデックに反映されたが、それに反発する[プログラマー](https://ja.wikipedia.org/wiki/プログラマー "wikilink")たちによってオープンソースで開発継続されたものがこの Xvid である。（名称はDivXをひっくり返したものである。）なお、OpenDivXプロジェクトは現在開発停止状態にあり、こちらは DivX4.0コーデックが元になっている。また、[シグマデザインズ](https://ja.wikipedia.org/wiki/シグマデザインズ "wikilink")社が開発した「[RMP4](https://ja.wikipedia.org/wiki/RMP4 "wikilink")」と呼ばれるコーデックにソースが盗用されたこともある。

## ソフトウェア特許

[MPEG-4](../Page/MPEG-4.md "wikilink")[特許のライセンスを得ておらず](../Page/ソフトウェア特許.md "wikilink")、開発プロジェクトでは[ソースコード](../Page/ソースコード.md "wikilink")のみの配布とすることでライセンス問題を回避している。但し、日本においては、特許法第68条により、“業として”バイナリの配布・利用を行わない限り(つまり個人の私的利用などでは)特許権侵害には当たらない。

## その他

  - [エンコード](../Page/エンコード.md "wikilink")の速さは、設定などにもよるが一般的にDivXより速いとされている。

<!-- end list -->

  - PCではWindows7のメディアプレイヤーで再生可能。

<!-- end list -->

  - [家電ではDivXビデオ対応の](../Page/家庭用電気機械器具.md "wikilink")[DVDプレーヤー](../Page/DVDプレーヤー.md "wikilink")や[ゲーム機](../Page/ゲーム機.md "wikilink")などで再生可能。

<!-- end list -->

  - Xvidの正しい読み方は不明だが、「エクシビッド」、「エックスブイアイディー」、「エックスビド」、「エックスバイド」、「キシビッド」等と読まれている。

## 利用例

  - MPEG-4の実装の[学習](../Page/学習.md "wikilink")や[研究](../Page/研究.md "wikilink")用
  - [ファイル共有ソフト](https://ja.wikipedia.org/wiki/ファイル共有ソフト "wikilink")でのDVDやテレビ番組の交換、共有。

商業用ソフトで使用した場合、そのソフトのソースを公開する義務が生じるため、一部の例外を除けばほとんど使用されていない。[アクアプラス](../Page/アクアプラス.md "wikilink")発売の[パソコンゲーム](../Page/パソコンゲーム.md "wikilink")（『[アルルゥとあそぼ\!\!](https://ja.wikipedia.org/wiki/アルルゥとあそぼ!! "wikilink")』、『[Tears to Tiara](https://ja.wikipedia.org/wiki/Tears_to_Tiara "wikilink")』、『[鎖 -クサリ-](../Page/鎖_-クサリ-.md "wikilink")』、『[ToHeart2](https://ja.wikipedia.org/wiki/ToHeart2 "wikilink")』）ではその義務を知らずにライブラリを使用していたことが判明したため、ゲームのソースコードを公開することが発売元より発表となった\[1\]。

## コンテナ形式

従来のビデオコーデック同様に[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")を利用した[コンテナ形式](../Page/コンテナフォーマット.md "wikilink")([AVI](../Page/Audio_Video_Interleave.md "wikilink")、[MKV等](../Page/Matroska.md "wikilink"))に格納することが可能で、映像のMPEG-4、音声のMP3、コンテナのAVIという組み合わせで使われることが多かった。

ただし、AVIでは[Bフレーム](../Page/フレーム間予測.md "wikilink")（前後参照フレーム）を扱うことが出来ない仕様となっているので、[GOPをパック処理するなどの工夫が必要となる](https://ja.wikipedia.org/wiki/Group_Of_Pictures "wikilink")。また、一部デコーダーでは先読みするなどで対応している例があるが、MKVなどでデコードするよりも負荷がかかる傾向がある。

  - (Xvid+MP3).avi
  - (Xvid+AAC).mkv

## [FOURCC](https://ja.wikipedia.org/wiki/FOURCC "wikilink")

用途により選択できる。

  - XVID
  - DIVX

## エンコードソフト

| OS                                                                      | ソフトウェア                                                                                                                                                                                                                                                 | コメント                                                                                    |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| [Windows専用](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") | [VirtualDub](../Page/VirtualDub.md "wikilink"), [DVDx](https://ja.wikipedia.org/wiki/DVDx "wikilink"), など。                                                                                                                                             | And all other applications that support encoding through the VfW framework.             |
| [クロスプラットフォーム](../Page/クロスプラットフォーム.md "wikilink")                        | [MEncoder](https://ja.wikipedia.org/wiki/MEncoder "wikilink"), [Transcode](https://ja.wikipedia.org/wiki/Transcode "wikilink"), [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink"), [VLCメディアプレーヤー](../Page/VLCメディアプレーヤー.md "wikilink"), など。 | These platform and framework independent applications access the Xvid library directly. |

## 関連項目

  - [DivX](https://ja.wikipedia.org/wiki/DivX "wikilink")
  - [ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")
  - [x264](https://ja.wikipedia.org/wiki/x264 "wikilink")
  - [MPEG LA](https://ja.wikipedia.org/wiki/MPEG_LA "wikilink")
  - [オープンソースのコーデックとコンテナフォーマット一覧](../Page/オープンソースのコーデックとコンテナフォーマット一覧.md "wikilink")

## 出典

<references/>

## 外部リンク

  - [Xvid.org(ソースコードの配布のみ)](http://www.xvid.org/)
  - [Koepi's Media Development Homepage(バイナリ配布)](http://www.koepi.info/)
  - [x264.co.nr(バイナリ配布)](http://www.x264.co.nr/)
  - [PHANTASIA.NET (Xvidコーデックの日本語化パッチ)](http://www.ne.jp/asahi/l/a/)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink") [Category:クロスプラットフォームのソフトウェア](https://ja.wikipedia.org/wiki/Category:クロスプラットフォームのソフトウェア "wikilink")

1.  [弊社製品のムービー再生にxvid.orgのムービー展開ライブラリを使用していた件について。](https://leaf.aquaplus.jp/product/xvid.html), 株式会社アクアプラス, 2005年12月12日