> この記事は[Core Audio \(アップル\)](https://ja.wikipedia.org/wiki/Core_Audio_\(アップル\))から翻訳されています。


**Core Audio**（コア オーディオ）は、[アップルのOS](../Page/アップル_\(企業\).md "wikilink")（[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")および[iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")・[iPadOS](https://ja.wikipedia.org/wiki/iPadOS "wikilink")・[tvOS](https://ja.wikipedia.org/wiki/tvOS "wikilink")・[watchOS](https://ja.wikipedia.org/wiki/watchOS "wikilink")・[audioOS](https://ja.wikipedia.org/wiki/audioOS "wikilink")）で、音声を扱う[フレームワーク](https://ja.wikipedia.org/wiki/フレームワーク "wikilink")である。Windowsにも同名のライブラリ（[Core Audio (Windows)](https://ja.wikipedia.org/wiki/Core_Audio_\(Windows\) "wikilink")）があるが、これとは異なる。

## 特徴

OSに組み込まれているフレームワークで、[Classic Mac OS](../Page/Classic_Mac_OS.md "wikilink") 9以前の標準オーディオ機能とは機能・構造がまったく異なる。このため[レイテンシ](../Page/レイテンシ.md "wikilink")（発音の遅延）が少なく、[ASIO](../Page/ASIO.md "wikilink")と同水準になっている。また、Mac OS 9以前では純正のMIDI Managerでは機能が不十分で、もっぱらサードパーティ製のMIDIドライバ（[オプコードのOpen](../Page/Opcode.md "wikilink") Music Systemなど）が使用されていたが、Core Audioではインスツルメントユニットとして設計されている。

[デジタル・オーディオ・ワークステーション](../Page/デジタル・オーディオ・ワークステーション.md "wikilink")（DAW）の[Virtual Studio Technology](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink")（VST）[プラグイン](../Page/プラグイン.md "wikilink")に似た、[Audio Units](../Page/Audio_Units.md "wikilink") (AU) と呼ばれる音声信号処理ユニットが用意されている。標準のエフェクトユニット、インスツルメントユニット・ミキサーユニット・コンバータユニット・ジェネレータユニットと、外部のユニットを組み合わせる(AU Graph)ことにより 、音声の加工・出力を簡単に行うことができる。

WAVやAIFFなどの主要な音声フォーマットはもちろんのこと、新たに開発された[ファイルコンテナ](../Page/コンテナフォーマット.md "wikilink") CAF（）も正式にサポートしている。

[OpenAL](https://ja.wikipedia.org/wiki/OpenAL "wikilink")[ライブラリ](../Page/ライブラリ.md "wikilink")も実装されている\[1\]。

## 提供されるサービス

Core Audioは、複数のサービスから成り立っている。

### 基礎的な部分（下層）

  - [ハードウェア抽象レイヤ](../Page/Hardware_Abstraction_Layer.md "wikilink") (Hardware Abstraction Layer, HAL)
    オーディオ[ハードウェア](../Page/ハードウェア.md "wikilink")を抽象化し、共通の[インタフェースで扱える様にする](../Page/インタフェース_\(情報技術\).md "wikilink")。
  - [Core MIDI](https://ja.wikipedia.org/wiki/Core_MIDI "wikilink")
    MIDI機器の管理や、MIDI信号の送受信を行う。

### 応用的な部分（上層）

  - Audio Toolbox
    アプリケーション向けの[API群](../Page/アプリケーションプログラミングインタフェース.md "wikilink")。一般的な音声ファイルやMIDI ([SMF](https://ja.wikipedia.org/wiki/Standard_MIDI_File "wikilink")) 楽曲の再生や録音、データフォーマットの変換、[Audio Unitの取り扱いや](https://ja.wikipedia.org/wiki/Audio_Unit "wikilink")[DSPルーティングの管理](../Page/デジタル信号処理.md "wikilink")、同期クロックの管理等を含む。
  - [OpenAL](https://ja.wikipedia.org/wiki/OpenAL "wikilink")
    macOS/[iOS版のOpenAL](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink")。主にゲーム開発に使用されるクロスプラットフォーム・[オープンソース](../Page/オープンソース.md "wikilink")のAPI。OpenAL 1.1をベースとしているが、macOSには独自拡張も含まれる。

## CAF

CAF（Core Audio Format）は[Mac OS X v10.4で登場したコンテナフォーマット](../Page/Mac_OS_X_v10.4.md "wikilink")。macOSをはじめiOS・iPadOS・tvOSのシステム音・内蔵の着信音や、iPhoneアプリの音声ファイルでも使用されている。ファイルサイズは最大16[EBで](https://ja.wikipedia.org/wiki/エクサバイト "wikilink")、メタデータや、リトル[エンディアン](https://ja.wikipedia.org/wiki/エンディアン "wikilink")にもビッグエンディアンにも対応しており、圧縮音源（AAC・MP3など）もエンコード無しで直接格納することが可能な、柔軟性の高い音声ファイルフォーマットである。

### 対応形式

  - リニア[PCM](https://ja.wikipedia.org/wiki/PCM "wikilink")
  - [G.711](../Page/G.711.md "wikilink") [μ-law](https://ja.wikipedia.org/wiki/μ-lawアルゴリズム "wikilink")
  - G.711 [A-law](https://ja.wikipedia.org/wiki/A-lawアルゴリズム "wikilink")
  - IMA [ADPCM](../Page/適応的差分パルス符号変調.md "wikilink") (IMA 4:1)
  - MPEG4 [AAC](../Page/AAC.md "wikilink")
  - MACE 3:1 (Macintosh Audio Compression and Expansion)
  - MACE 6:1
  - MPEG1/2 Audio Layer-1 (MP1)
  - MPEG1/2 Audio Layer-2 (MP2)
  - MPEG1/2/2.5 audio Layer3 ([MP3](../Page/MP3.md "wikilink"))
  - [Apple Lossless](../Page/Apple_Lossless.md "wikilink")

## 脚注

<references/>

## 関連項目

  - [Core Audio (Windows)](https://ja.wikipedia.org/wiki/Core_Audio_\(Windows\) "wikilink")
  - [Audio Units](../Page/Audio_Units.md "wikilink") (AU)
  - [OpenAL](https://ja.wikipedia.org/wiki/OpenAL "wikilink")

## 外部リンク

  - [アップル - Mac OS X - Core Audio](http://www.apple.com/jp/macosx/features/coreaudio/)
  - [Core Audio Overview: Introduction](https://developer.apple.com/library/mac/documentation/MusicAudio/Conceptual/CoreAudioOverview/Introduction/Introduction.html)
  - [Core Audioとは](https://developer.apple.com/jp/documentation/MusicAudio/Conceptual/CoreAudioOverview/WhatisCoreAudio/WhatisCoreAudio.html)
  - [Core Audioの概要 (TP40003577 0.0.0) - CoreAudioOverview.pdf](https://developer.apple.com/jp/documentation/CoreAudioOverview.pdf)
  - [Core Audio Format Specification](https://developer.apple.com/library/archive/documentation/MusicAudio/Reference/CAFSpec/CAF_spec/CAF_spec.html) - CAFファイルフォーマットの仕様

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink")

1.  [Core Audio Overview: What Is Core Audio?](https://developer.apple.com/library/mac/documentation/MusicAudio/Conceptual/CoreAudioOverview/WhatisCoreAudio/WhatisCoreAudio.html)