> この記事は[Audio Units](https://ja.wikipedia.org/wiki/Audio_Units)から翻訳されています。


**Audio Units**（オーディオ ユニッツ）とは[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")に直接統合されているオーディオ機能、[Core Audioによって提供されるシステムレベルの](../Page/Core_Audio_\(アップル\).md "wikilink")[DSP](../Page/デジタル信号処理.md "wikilink")[プラグイン](../Page/プラグイン.md "wikilink")[アーキテクチャで](../Page/コンピュータ・アーキテクチャ.md "wikilink")、[ソフトウェア](../Page/ソフトウェア.md "wikilink")の機能を拡張する追加[モジュール](../Page/モジュール.md "wikilink")の規格。**AU**と略される。

一般利用者向けには大別して、[ソフトウェア音源の](../Page/ソフトウェア・シンセサイザー.md "wikilink")**AU Instrument**と、ソフトウェア[エフェクター](../Page/エフェクター.md "wikilink")の**AU Effect**がある。類似のプラグイン規格として[スタインバーグ](https://ja.wikipedia.org/wiki/スタインバーグ "wikilink")が提唱する[VST](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink")、[Pro Toolsで使用される](../Page/Pro_Tools.md "wikilink")[AAX](https://ja.wikipedia.org/wiki/AAX "wikilink")、[RTAS](https://ja.wikipedia.org/wiki/RTAS "wikilink")、Windows向けの[DXi](https://ja.wikipedia.org/wiki/DXi "wikilink")などがある。

AUは、[GarageBand](../Page/GarageBand.md "wikilink")、[Soundtrack Pro](https://ja.wikipedia.org/wiki/Soundtrack_Pro "wikilink")、[Logic Express](../Page/Logic_Express.md "wikilink")、[Logic Pro](../Page/Logic_Pro.md "wikilink")、[Final Cut Pro](../Page/Final_Cut_Pro.md "wikilink")、[AU Lab等の](https://ja.wikipedia.org/wiki/AU_Lab "wikilink")[アップル製](../Page/アップル_\(企業\).md "wikilink")[アプリケーションが対応済みで](../Page/アプリケーションソフトウェア.md "wikilink")、多くのソフトウェアメーカーでもプラグインやアプリケーションの対応が進んでいる。

## Mac OS X v10.5に標準搭載されたAudio Unit

### インストゥルメント

  - DLSMusicDevice
    内蔵の[GS音源](../Page/GSフォーマット.md "wikilink")（[ローランド](../Page/ローランド.md "wikilink")提供）、または外部の[Downloadable Sounds](https://ja.wikipedia.org/wiki/Downloadable_Sounds "wikilink") (DLS) または[SoundFont](../Page/SoundFont.md "wikilink")を用いて楽器音を鳴らす。ロムプラー ([:en:Rompler](https://ja.wikipedia.org/wiki/:en:Rompler "wikilink"))、プレイバック[サンプラー](../Page/サンプラー.md "wikilink")の一種。

### ジェネレーター

  - AUAudioFilePlayer
    [音声ファイルを読み込み再生](../Page/音声ファイルフォーマット.md "wikilink")・出力する。
  - AUNetReceive
    [ネットワーク経由で音声を受信し再生](../Page/コンピュータネットワーク.md "wikilink")・出力する。
  - AUScheduledSoundPlayer
    [メモリー](../Page/記憶装置.md "wikilink")[バッファ](../Page/バッファ.md "wikilink")ー上の音声を再生・出力する

### エフェクター

#### フィルター・イコライザー

  - AUBandpass
    [バンドパスフィルタ](../Page/バンドパスフィルタ.md "wikilink")ー。
  - AUHipass
    [レゾナンス](https://ja.wikipedia.org/wiki/レゾナンス "wikilink")付きの[ハイパスフィルタ](../Page/ハイパスフィルタ.md "wikilink")ー。
  - AULowpass
    レゾナンス付きの[ローパスフィルタ](../Page/ローパスフィルタ.md "wikilink")ー。
  - AUFilter
    2バンドのシェルビング[イコライザーおよび](../Page/イコライザー_\(音響機器\).md "wikilink")3バンドのピーキングイコライザーによる、計5バンドのパラメトリックイコライザー。
  - AUHighShelfFilter
    簡素な高域シェルビングイコライザー。
  - AULowShelfFilter
    簡素な低域シェルビングイコライザー。
  - AUParametricEQ
    簡素なピーキングイコライザー。
  - AUGraphicEQ
    31バンドまたは10バンドのグラフィックイコライザー。

#### ディレイ・リバーブ

  - AUDelay
    [フィードバック](../Page/フィードバック.md "wikilink")、ローパスフィルター付きの[ディレイ](../Page/ディレイ_\(音響機器\).md "wikilink")。
  - AUSampleDelay
    サンプル数指定によるフィードバックのない簡素なディレイ。
  - AUMatrixReverb
    パラメーター式の[リバーブレーター](../Page/リバーブレーター.md "wikilink")。

#### ダイナミクス

  - AUDynamicsProcessor
    [コンプレッサー](../Page/コンプレッサー_\(音響機器\).md "wikilink")。
  - AUMultibandCompressor
    4バンドのマルチバンドコンプレッサー。
  - AUPeakLimiter
    [ピークリミッター](../Page/リミッター_\(音響機器\).md "wikilink")。

#### その他のエフェクター

  - AUDistortion
    フィードバックディレイ、[リングモジュレーション](../Page/振幅変調.md "wikilink")、[デシメーション](../Page/サンプリング周波数変換.md "wikilink")、[ビットクラッシャー](https://ja.wikipedia.org/wiki/量子化 "wikilink")、2乗・3乗ウェーブシェイパーによる[ディストーション](../Page/ディストーション_\(音響機器\).md "wikilink")。
  - AUNetSend
    [Bonjour](../Page/Bonjour.md "wikilink")によるネットワーク経由で音声を送信する。
  - AUPitch
    [ピッチシフター](https://ja.wikipedia.org/wiki/ピッチシフター_\(音響機器\) "wikilink")。
  - AURogerBeep
    無音状態になった事を検出した時に[スタンバイ・ピー](../Page/トランシーバー_\(無線機\).md "wikilink")（ロジャービープ）を発生する。

### ミキサー

  - AUMixer
    [ステレオ](../Page/ステレオ.md "wikilink")[ミキサー](https://ja.wikipedia.org/wiki/ミキシングコンソール "wikilink")。
  - AUMatrixMixer
    マトリックスミキサー。
  - AUMixer3D
    3次元ミキサー。

### パンナー

  - AUSoundFieldPanner
    3次元パンナーの一種。
  - AUSphericalHeadPanner
    3次元パンナーの一種。
  - AUVectorPanner
    3次元パンナーの一種。
  - HRTFPanner
    [頭部伝達関数](https://ja.wikipedia.org/wiki/頭部伝達関数 "wikilink")を適用した3次元パンナー。

### コンバーター

  - AUConverter
    [PCM音声のフォーマット変換](../Page/パルス符号変調.md "wikilink")。
  - AUDeferredRenderer
    入力音声を他のスレッドへ転送する。
  - AUMerger
    音声信号の併合。
  - AUSplitter
    音声信号の分離。
  - AUTimePitch
    タイムストレッチおよびピッチシフト。
  - AUVariSpeed
    再生スピードの調整（ピッチチェンジ）。

### アウトプット

  - AudioDeviceOutput (AUHAL)
    特定の音声デバイスとの入出力を行う。
  - DefaultOutputUnit
    システム標準の音声出力デバイス。
  - GenericOutput
    音声出力デバイスの基礎。
  - SystemOutputUnit
    システム[警告音](https://ja.wikipedia.org/wiki/警告音 "wikilink")、ユーザインターフェイス[効果音](../Page/効果音.md "wikilink")の音声出力デバイス。

## 外部リンク

  - [Audio Unit Programming Guide](http://developer.apple.com/documentation/MusicAudio/Conceptual/AudioUnitProgrammingGuide/)
  - [Core Audio Overview: System-Supplied Audio Units](http://developer.apple.com/documentation/MusicAudio/Conceptual/CoreAudioOverview/SystemAudioUnits/chapter_951_section_1.html)

[Category:MacOS](https://ja.wikipedia.org/wiki/Category:MacOS "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink")