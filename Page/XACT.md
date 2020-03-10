> この記事は[XACT](https://ja.wikipedia.org/wiki/XACT)から翻訳されています。


**XACT**（イグザクトと読む\[1\]）は[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")の一部として[マイクロソフト](../Page/マイクロソフト.md "wikilink")によってリリースされた、オーディオプログラミングライブラリおよびオーディオエンジンである。これは、オーサリングおよび再生用高レベルオーディオライブラリであり、[Xbox上では](../Page/Xbox_\(ゲーム機\).md "wikilink")[XAudio](https://ja.wikipedia.org/wiki/XAudio "wikilink")、[Windows XPでは](../Page/Microsoft_Windows_XP.md "wikilink")[DirectSound](../Page/DirectSound.md "wikilink")、[Windows Vistaでは新しいオーディオスタックを使って書かれている](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")。XAudioはデジタル信号処理を最適に行うために設計された、Xbox専用のAPIである。XACTはまたX3DAudioを含んでおり、WindowsとXbox両方のプラットフォームで使用可能な空間音響ヘルパーライブラリである。XACTは元々Xboxの開発のために作られたが、後にWindowsでも動作するように修正が加えられた。

XACTのサポートはDirectXから[XNAにそのまま引き継がれている](https://ja.wikipedia.org/wiki/Microsoft_XNA "wikilink")。*XACT Audio Authoring Tool*は[XNA Game Studioでも利用が可能である](https://ja.wikipedia.org/wiki/XNA_Game_Studio "wikilink")。

**XACT Audio Authoring Tool**は*wave banks* (複数の[WAV](https://ja.wikipedia.org/wiki/WAV "wikilink")ファイルが入った単一のアーカイブファイル) や*sound banks* (wave banksの中にあるWAVファイルを演奏する命令が入った単一のファイル) を作るためのオーディオデータを構成するために使われるアプリケーションである。wave banksとsound banksはアプリケーション内にあって、XACTからその後呼び出されることになる。

なお、[Windows 8用のソフトウェア開発キットである](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")[Windows SDK](https://ja.wikipedia.org/wiki/Windows_SDK "wikilink") 8.0以降ではWindows SDKとDirectX SDKが統合されたが、その際にXACTは廃止されている。

DirectX Tool Kitには、廃止されたXACTの代替として、[XNA Game Studioのオーディオコンポーネントに似た補助ライブラリが実装されている](https://ja.wikipedia.org/wiki/XNA_Game_Studio "wikilink")\[2\]。

## XACTの音楽作成機能

  - [WAV](https://ja.wikipedia.org/wiki/WAV "wikilink")、[AIFF](https://ja.wikipedia.org/wiki/AIFF "wikilink")、、[xWMA](https://ja.wikipedia.org/wiki/xWMA "wikilink")\[3\]フォーマットをサポート
      - WAVとAIFFフォーマット内にある埋め込みループポイントもサポートしている
  - ステレオと5.1chスピーカーもサポート
  - 音声の編集
      - 複数のオーディオファイルをWave Banks (XWB拡張子) にグループ化する機能
      - キューや演奏指定を音データと一緒にSound Banks (XSB拡張子) にまとめる機能
  - 編集
      - オーディオコンソールウィンドウを使ってのオーディオプレビュー機能
      - デバッグモードライブラリを使ったゲーム内での調整のオーディオ設定

## XACTのAPIが提供する機能

  - 音楽、効果音、演奏キュー情報を作成段階から統合できるAPI
  - メモリ蓄積型（In-Memory）とストリーミング（Streaming）の両方をサポート
  - オーディオイベントを検知
  - すべてのXACT音声編集機能を使うことなしに、音データの読み込みと再生を行うことができる低レベルAPIを含む
  - X3DAudio APIを介した3次元音響効果「XACT3D」（[DirectSound3Dの後継機能](https://ja.wikipedia.org/wiki/DirectSound#DirectSound3D "wikilink")）

## XACTの用語とファイル型

  - Sound Banks (.xsb) - サウンドとキューのコレクション
      - Sound - ボリュームと[ピッチ](https://ja.wikipedia.org/wiki/ピッチ "wikilink")のような特性と一緒に一つ以上の音声を合わせたもの。サウンドはトラックから構成される。
          - Tracks - トラックはイベントから構成される。最も単純なトラックはWaveを再生するイベントを持つ。
          - Events - トラック内に起きる様々なアクション。アクションは、再生、停止、ボリューム設定、ピッチ設定などを含む。
      - Cue - Cueは音声を再生するタイミングを記述するのに使われる。それぞれのCueは一つ以上の音声からなる。

<!-- end list -->

  - Wave Banks (.xwb) - 複数のWaveをまとめたファイルフォーマット
      - Waves - WAV、AIFF、XMAフォーマットで記述されたraw音声データ
  - Global Settings (.xgs) - 音声に対するルールと設定を定義している
      - Categories - 音声は一つの(それぞれ一つのみ)のカテゴリーに割り当てられる。そのカテゴリーはボリュームのようないろんな設定と一緒に、とあるルールによって決められたものである。ゲーム中にあるキャラクター用の音声カテゴリーを作ったなら、それらはすべて同じボリューム設定になる。カテゴリーは、Global、Default、Musicの3つが既定で定義済みである。
      - Variables - 設計段階で定義されるもので、プログラマによってコード中からRun-Time Parameter Controlを行うために参照されるものである。
          - Run-Time Parameter Control - スライダーとしても知られている。これによって音声を再生時に音声パラメータの制御ができる。例えば、これを使うことで、アクセルを踏むと車のエンジン音のピッチが変化するなどのような制御ができる。
      - DSP Effect Path Presets (DSPs) - [リバーブのようなエフェクトを音声に適用できる](https://ja.wikipedia.org/wiki/残響 "wikilink")
      - Compression Presets - waveやwave bankに圧縮をかける。

## 脚注

## 関連項目

  - [DirectSound](../Page/DirectSound.md "wikilink")
  - [Microsoft DirectX](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")

## 外部リンク

  - [MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink")
      - [Microsoft Cross-Platform Audio Creation Tool (XACT)](https://msdn.microsoft.com/en-us/library/bb174772.aspx)
      - [XACT の概要](https://msdn.microsoft.com/ja-jp/library/bb172315.aspx)

[Category:Xbox](https://ja.wikipedia.org/wiki/Category:Xbox "wikilink") [Category:DirectX](https://ja.wikipedia.org/wiki/Category:DirectX "wikilink")

1.  [XACT TIPS - ひにけにGD - Site Home - MSDN Blogs](http://blogs.msdn.com/b/ito/archive/2007/05/29/xact-tips.aspx)
2.  [DirectX Tool Kit - Documentation](https://directxtk.codeplex.com/wikipage?title=Audio)
3.  [xWMA の概要](https://msdn.microsoft.com/ja-jp/library/cc308025.aspx)