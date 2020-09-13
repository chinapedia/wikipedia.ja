> この記事は[Ogg](https://ja.wikipedia.org/wiki/Ogg)から翻訳されています。


{{ infobox file format | name = Ogg | logo = | extension = .ogv, .oga, .ogx, .ogg, .spx | mime = video/ogg, audio/ogg, application/ogg | magic = OggS | owner = [Xiph.Org Foundation](https://ja.wikipedia.org/wiki/Xiph.Org_Foundation "wikilink") | creatorcode = [Chris Montgomery](https://ja.wikipedia.org/wiki/Chris_Montgomery "wikilink") | genre = [コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink") | extendedto = [Ogg Media](../Page/Ogg_Media.md "wikilink") | container for = [Vorbis](../Page/Vorbis.md "wikilink"), [Theora](../Page/Theora.md "wikilink"), [Speex](../Page/Speex.md "wikilink"), [FLAC](../Page/FLAC.md "wikilink"), [Dirac](https://ja.wikipedia.org/wiki/Dirac "wikilink"), [Writ](https://ja.wikipedia.org/wiki/Writ "wikilink") ほか }}

**Ogg**（オッグ、オグ）は、[パテントフリーの](../Page/特許.md "wikilink")[マルチメディア](../Page/マルチメディア.md "wikilink")[コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")である。主にOggファイル、Oggコンテナなどと呼ばれている。

## 概要

Oggは[Xiph.Org Foundationによって規格化されており](https://ja.wikipedia.org/wiki/Xiph.Org_Foundation "wikilink")、[RFC](../Page/Request_for_Comments.md "wikilink") 3533として文書化されている。

Oggはコンテナであり、1つないし複数の[コーデック](../Page/コーデック.md "wikilink")を内容物として格納する。Oggの最も代表的なコーデックは[音声コーデックの](../Page/音声ファイルフォーマット.md "wikilink")[Vorbis](../Page/Vorbis.md "wikilink")である。Vorbisを格納したOggはOgg Vorbisと呼ばれる（他のコーデックも同様）。Ogg Vorbisを単にOggと呼ぶことがあるが、Oggはコンテナの名称であってコーデックではないことに注意すべきである。他のコーデックには、[動画コーデックの](https://ja.wikipedia.org/wiki/動画ファイルフォーマット "wikilink")[Theora](../Page/Theora.md "wikilink")、可逆音声コーデックの[FLAC](../Page/FLAC.md "wikilink")、[人](../Page/人.md "wikilink")の[声](../Page/声.md "wikilink")に特化した音声コーデックの[Speex](../Page/Speex.md "wikilink")、テキストの[Writ](https://ja.wikipedia.org/wiki/Writ "wikilink")（[字幕](../Page/字幕.md "wikilink")に使う）などがある。

当初Xiph.Org FoundationはOgg共通の拡張子を.oggと定めていたが、2007年に共通の拡張子を*.ogx*、動画の拡張子を*.ogv*、音声の拡張子を*.oga*に改めた。元々の共通の拡張子であった.oggはOgg Vorbis音声ファイルにのみ互換目的で使われる。これら以外にSpeexを収納したOggの拡張子として.spxが使われることがある。

## Oggに収納できるコーデック

  - [オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")
      - [非可逆圧縮](../Page/非可逆圧縮.md "wikilink")
          - [Speex](../Page/Speex.md "wikilink"): 人声に特化
          - [Vorbis](../Page/Vorbis.md "wikilink"): 音声汎用

<!-- end list -->

  -   - [CELT](https://ja.wikipedia.org/wiki/CELT "wikilink"): 低遅延を目標としSpeexとVorbisの中間に位置するフォーマット。開発終了。
      - [Opus](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink"): [SILK](https://ja.wikipedia.org/wiki/SILK "wikilink")とCELTを組み合わせたインタラクティブな音声や音楽向けのフォーマット

  -   - [可逆圧縮](../Page/可逆圧縮.md "wikilink")
          - [FLAC](../Page/FLAC.md "wikilink"): 音声汎用
          - [OggPCM](https://ja.wikipedia.org/wiki/OggPCM "wikilink"): 非圧縮[PCM](https://ja.wikipedia.org/wiki/PCM "wikilink")

<!-- end list -->

  - [テキスト](../Page/テキスト.md "wikilink")
      - Continuous Media Markup Language: 汎用メタテキストデータ
      - [OggKate](https://ja.wikipedia.org/wiki/OggKate "wikilink"): カラオケ・テキスト
      - [Writ](https://ja.wikipedia.org/wiki/Writ "wikilink"):
      - [Annodex](https://ja.wikipedia.org/wiki/Annodex "wikilink"):

<!-- end list -->

  - [ビデオ](../Page/映像信号.md "wikilink")
      - [非可逆圧縮](../Page/非可逆圧縮.md "wikilink")
          - [Theora](../Page/Theora.md "wikilink"): ビデオ汎用
          - [Tarkin](https://ja.wikipedia.org/wiki/Tarkin "wikilink"):
          - [Dirac](https://ja.wikipedia.org/wiki/Dirac "wikilink"): BBC開発の新しいフォーマット
      - [可逆圧縮](../Page/可逆圧縮.md "wikilink")
          - [OggUVS](https://ja.wikipedia.org/wiki/OggUVS "wikilink"): 非圧縮ビデオ
          - [Dirac](https://ja.wikipedia.org/wiki/Dirac "wikilink"): BBC開発の新しいフォーマット

## Ogg に対応した再生ソフト

  - [Audacity](../Page/Audacity.md "wikilink")
  - [SoundPlayer Lilith](https://ja.wikipedia.org/wiki/SoundPlayer_Lilith "wikilink")
  - [ffplay](../Page/FFmpeg.md "wikilink")
  - [Mozilla Firefox](../Page/Mozilla_Firefox.md "wikilink") 3.5 以降
  - [MPlayer](../Page/MPlayer.md "wikilink")
  - [VLCメディアプレーヤー](../Page/VLCメディアプレーヤー.md "wikilink")
  - [Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")
  - [ビデオ](../Page/ビデオ_\(GNOME\).md "wikilink")
  - [IrfanView](../Page/IrfanView.md "wikilink")
  - [foobar2000](https://ja.wikipedia.org/wiki/foobar2000 "wikilink")
  - [Sound Normalizer](https://ja.wikipedia.org/wiki/Sound_Normalizer "wikilink")
  - [Google Chrome](https://ja.wikipedia.org/wiki/Google_Chrome "wikilink")

など。

## 関連項目

  - [コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")
  - [LRC](https://ja.wikipedia.org/wiki/LRC "wikilink")
  - [OggPCM](https://ja.wikipedia.org/wiki/OggPCM "wikilink")
  - [Oggページ](../Page/Oggページ.md "wikilink")
  - [Ogg Media](../Page/Ogg_Media.md "wikilink") (OGM) - 開発終了
  - [Matroska](../Page/Matroska.md "wikilink") - Ogg Mediaの後継
  - [オープンソースのコーデックとコンテナフォーマット一覧](../Page/オープンソースのコーデックとコンテナフォーマット一覧.md "wikilink")

## 外部リンク

  - [Xiph.org](http://www.xiph.org/)
  - [Directshow Filters for Ogg Vorbis, Speex, Theora, FLAC, and WebM](http://xiph.org/dshow/)
  - RFC 3533
  - [Haali Media Splitter](http://haali.cs.msu.ru/mkv/) (Oggコンテナ再生用のスプリッター)

[Category:Xiph.Org](https://ja.wikipedia.org/wiki/Category:Xiph.Org "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:マルチメディア](https://ja.wikipedia.org/wiki/Category:マルチメディア "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink") [Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")