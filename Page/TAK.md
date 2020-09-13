> この記事は[TAK](https://ja.wikipedia.org/wiki/TAK)から翻訳されています。


**TAK**（ティーエーケー、Tom's lossless Audio Kompressor）は[フリーウェア](../Page/フリーウェア.md "wikilink")の[可逆圧縮](../Page/可逆圧縮.md "wikilink")[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")及び[コンプレッサーである](https://ja.wikipedia.org/wiki/エンコーダー "wikilink")。

## 概要

[FLAC](../Page/FLAC.md "wikilink")の[コードをベースに開発されたロスレス](../Page/ソースコード.md "wikilink")・オーディオコンプレッサーである。正式リリース以前はYalacと呼ばれていた。[可逆圧縮](../Page/可逆圧縮.md "wikilink")の[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")であるため、元の音声データからの音質の[劣化](../Page/劣化.md "wikilink")が無い。FLAC並（もしくは以上）のデコード速度とエンコード速度及び再生負荷（軽さ）\[1\]\[2\]、内部cueシート対応等と総合的に高い性能を誇る。

無償で利用できるが[オープンソース](../Page/オープンソース.md "wikilink")ではない。そのため、再生は[Foobar2000](../Page/Foobar2000.md "wikilink")や[Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")など、エンコードはtakc.exeを外部エンコーダーとして利用できる物およびtak.exe本体のみと非常に限られていたが、現在は公認[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")フィルターにより[Windows Media Playerなどでも利用できる](../Page/Windows_Media_Player.md "wikilink")。また、開発者向けにデコード用の[SDKが公開され](../Page/ソフトウェア開発キット.md "wikilink")、公式以外のアプリケーションからも簡単に利用できるようになった。[FFmpeg](../Page/FFmpeg.md "wikilink")に独自のオープンソースによるデコーダが実装されているため、デコードに限ればWindows以外のプラットフォームでも利用可能である。

TAK Ver 1.x系列はVer 1.1.2 Final（[2009年](../Page/2009年.md "wikilink")[7月27日](../Page/7月27日.md "wikilink")）をもって開発が終了。現在、TAK Ver 2.x系列の開発に移行しており、最新版はVer 2.3.0 Final（[2013年](../Page/2013年.md "wikilink")[6月18日](../Page/6月18日.md "wikilink")）がリリースされている\[3\]ほか、最新評価版としてはVer 2.3.1 Beta 1（[2018年](../Page/2018年.md "wikilink")[4月2日](../Page/4月2日.md "wikilink")）がリリースされた\[4\]。オープンソース化や[Linux](../Page/Linux.md "wikilink")対応、64ビット化のために、[Delphi](../Page/Delphi.md "wikilink")から[Lazarus](../Page/Lazarus.md "wikilink")や[C言語](../Page/C言語.md "wikilink")に移植するための作業が行われている。

## 特徴

  - 最大24ビット、192 kHz、16ch（コーデックとしては6chに制限）までサポート。
  - [FLAC](../Page/FLAC.md "wikilink")並（もしくは以上）に高速なエンコード・デコード速度。
      - [インテル](https://ja.wikipedia.org/wiki/インテル "wikilink")製CPUであれば、複数のCPUコアによる並列処理で単一のファイルをエンコード・デコードすることが可能。
  - シークテーブル無しでの高速かつ正確なシーク。
  - エラー耐性の高いデータ構造と[CRCによるエラー検出を備える](../Page/巡回冗長検査.md "wikilink")。
  - [MD5](../Page/MD5.md "wikilink")チェック機能によりファイルの信頼性を証明。
  - APEtag対応、Takファイル内に[メタデータ](../Page/メタデータ.md "wikilink")を格納する事が可能。
      - internal cuesheet（内部cueシート）対応により、複数音楽データ（アルバム等）を1ファイル内にまとめて扱える。
      - 画像データを格納する事により、ジャケット等を表示する事が可能。(格納は[Mp3tag](https://ja.wikipedia.org/wiki/Mp3tag "wikilink")等を利用、表示は[Foobar2000](../Page/Foobar2000.md "wikilink")等)
      - 歌詞データを格納する事により、カラオケのように表示をする事が可能。
      - Logを格納する事により、エンコード時の環境等を確認する事が可能。
      - [ID3タグ](../Page/ID3タグ.md "wikilink")とデータの高い互換性を有する。
  - [ストリーミング](../Page/ストリーミング.md "wikilink")への利用可能なデータ形式。
  - クローズドソース故に対応ソフトが限られていた。現在は他のアプリケーションから簡単に利用できるデコード用の[SDKが公開されている](../Page/ソフトウェア開発キット.md "wikilink")。また、[FFmpeg](../Page/FFmpeg.md "wikilink")にオープンソースのデコーダが実装されている
  - エンコードに関してはtak.exe本体の他、[Exact Audio Copyや](../Page/Exact_Audio_Copy.md "wikilink")[Foobar2000](../Page/Foobar2000.md "wikilink")等、takc.exeを外部エンコーダーとして利用できるソフトウェアであれば、エンコードする事が可能である。
  - 公認DirectShowフィルターにより、DirectShowを利用可能なソフトで使用する事ができる。(最新版：[dsfTAKSource v0.0.1.6(TAK2.2.0互換)](http://liviocavallo.altervista.org/))
  - Hydrogenaudioでのアンケートによれば、可逆音声ファイル内での普及率は2012年現在、FLAC、WavPack、Apple Losslessに次ぐ4位となっている。\[5\]

## 公認サポートソフトウェア

  - [Foobar2000](../Page/Foobar2000.md "wikilink") - [オーディオプレーヤー](https://ja.wikipedia.org/wiki/オーディオプレーヤー "wikilink")
  - [Quintessential Player](https://ja.wikipedia.org/wiki/Quintessential_Player "wikilink") - [オーディオプレーヤー](https://ja.wikipedia.org/wiki/オーディオプレーヤー "wikilink")
  - [Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink") - [メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")
  - [XMPlay](https://ja.wikipedia.org/wiki/XMPlay "wikilink") - [メディアプレーヤー](../Page/メディアプレーヤー.md "wikilink")
  - [Exact Audio Copy](../Page/Exact_Audio_Copy.md "wikilink") - [リッパー](../Page/リッピング.md "wikilink")・[ライター](../Page/ライティングソフトウェア.md "wikilink")
  - [ImgBurn](../Page/ImgBurn.md "wikilink") - [リッパー](../Page/リッピング.md "wikilink")・[ライター](../Page/ライティングソフトウェア.md "wikilink")
  - [GermaniX](https://ja.wikipedia.org/wiki/GermaniX "wikilink") - [トランスコーダー](../Page/トランスコード.md "wikilink")
  - [Transcoder](https://ja.wikipedia.org/wiki/Transcoder "wikilink") - [トランスコーダー](../Page/トランスコード.md "wikilink")
  - [caudec](https://ja.wikipedia.org/wiki/caudec "wikilink") - [トランスコーダー](../Page/トランスコード.md "wikilink")
  - [shntool](https://ja.wikipedia.org/wiki/shntool "wikilink") -
  - [Mp3tag](https://ja.wikipedia.org/wiki/Mp3tag "wikilink") - [タグエディター](../Page/メタデータ.md "wikilink")
  - [dsfTAKSource](https://ja.wikipedia.org/wiki/dsfTAKSource "wikilink") - [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")フィルター

## 関連項目

  - [可逆圧縮](../Page/可逆圧縮.md "wikilink")
  - [音声圧縮](../Page/音声圧縮.md "wikilink")
  - [音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")
  - [FLAC](../Page/FLAC.md "wikilink")
  - [Apple Lossless](../Page/Apple_Lossless.md "wikilink")
  - [Monkey's Audio](../Page/Monkey's_Audio.md "wikilink")
  - [TTA](../Page/TTA.md "wikilink") (The True Audio)
  - [WMA Lossless](https://ja.wikipedia.org/wiki/WMA "wikilink")
  - [WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")
  - [foobar2000](https://ja.wikipedia.org/wiki/foobar2000 "wikilink")

## 外部リンク

  - [thbeck.de(公式サイト)](http://www.thbeck.de/Tak/Tak.html)
  - [dsfTAKSource(Tak DirectShowFilter)](http://liviocavallo.altervista.org/)

## 脚註

<references/>

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink")

1.  [Lossless audio codec comparison - Revision 3 (August 10, 2013)](http://www.icer.nl/losslesstest/Lossless%20audio%20codec%20comparison%20-%20revision%203.pdf)
2.  [synthetic-soul.（可逆音声ファイル 設定別 各形式比較表（圧縮率、Decode・Encode速度））](http://www.synthetic-soul.co.uk/comparison/lossless/)
3.  [TAK 2.3.0 - Hydrogenaudio Forums](http://www.hydrogenaudio.org/forums/index.php?showtopic=101386)
4.  [TAK 2.3.1 Beta 1 - Hydrogenaudio Forums](https://hydrogenaud.io/index.php/topic,115769.0.html)
5.  [2012 ripping/encoding general poll - Hydrogenaudio Forums](http://www.hydrogenaudio.org/forums/index.php?showtopic=92660)