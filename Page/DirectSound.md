> この記事は[DirectSound](https://ja.wikipedia.org/wiki/DirectSound)から翻訳されています。


**DirectSound**は[マイクロソフト](../Page/マイクロソフト.md "wikilink")が提供する[DirectXのソフトウェアの一部品であり](https://ja.wikipedia.org/wiki/Microsoft_DirectX "wikilink")、[Windowsに搭載されている](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")。DirectSoundは、[アプリケーションと](../Page/アプリケーションソフトウェア.md "wikilink")[サウンドカード](https://ja.wikipedia.org/wiki/サウンドカード "wikilink")との間に直接的なインタフェースを提供し、アプリケーションが音や音楽を鳴らせるようにするものである。DirectSoundはオーディオデータをサウンドカードに渡す機能に加えて、録音や音をミキシングするのに必要な機能も数多く提供している。例えば、サウンドにエフェクト（[リバーブや](https://ja.wikipedia.org/wiki/残響 "wikilink")[エコー](https://ja.wikipedia.org/wiki/残響 "wikilink")、[フランジング](https://ja.wikipedia.org/wiki/フランジング "wikilink")など）を付加する機能や、再生速度を変化させるためのハードウェアで制御できるバッファや、3次元空間内で音の鳴っている位置を変化させる機能（[3次元立体音響](https://ja.wikipedia.org/wiki/3次元立体音響 "wikilink")）、マイクロフォンやその他の[入力機器](https://ja.wikipedia.org/wiki/入力機器 "wikilink")から録音する機能や、録音中にエフェクトを付加するのを制御する機能などがある。

また、DirectSoundでは複数のアプリケーションがサウンドカードに同時にアクセスする便利な方法も提供している。この3次元空間的に音を鳴らすことができる機能によって、ゲームに新次元の楽しみをもたらす。またゲーム内でのイベントに即座に反応して、音を鳴らすスクリプトを変更する機能も提供している。すなわち、ゲーム内のアクションがヒートアップしてきたらそれにあわせて音楽のリズムも速くすることができる。

数年間の開発の後、のDirectSoundは非常に成熟したAPIを持ち、複数チャンネルを用いた再生や高精細な音を再生できる機能など、多くの役に立つ機能を提供している。DirectSoundはゲームに使われるように設計され、プロが使うオーディオアプリケーションでは今やこれらの様々な機能を利用している。

## DirectSound3D

**DirectSound3D** (DS3D) は[Windowsでの標準](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")3Dオーディオとして[DirectX](https://ja.wikipedia.org/wiki/DirectX "wikilink")に追加されたもので、1996年、DirectX 3に導入された。

DirectSound3Dは、ソフトウェア開発者がそれぞれのオーディオカードメーカーに合わせたコードを書く代わりに、単一の標準化されたオーディオAPIを書くことで対応できるようにしている。

DirectX 5では、DirectSound3DはDirectSound3Dをアクセラレーションするサードパーティー製の3Dオーディオアルゴリズムを使う複数のサウンドカードを、マイクロソフトが用意した方法を用いて、扱うことができる能力を持つ。この機能を使えば3Dオーディオライブラリを分離する必要はなくなる。

DirectX 8ではさらに開発が進み、DirectSoundとDirectSound3D (DS3D) はと統合されて**DirectX Audio**と呼ばれるようになった\[1\]。

、DirectSound 3Dの3D音源は、エコー、リバーブ等の環境音を模倣するエフェクトと、リスナーの位置と音源 (モノラル) の位置関係を簡易に計算するライブラリが主体である。やっていることは、旧来、ステレオPCM音源のパンとボリュームを自前で調整することで、擬似的に音源の位置 (音像) を表現していたが、これをライブラリとして吸収しただけである。したがって、実際の空気中を伝播する音の物理そのものをシミュレートして計算しているわけではなく、遮蔽や反射などは考慮されていない。

## Windows OS でのサポート

### Windows 95

### Windows 2000/XP

### Windows Vista/Windows 7

Windows VistaはUniversal Audio Architecture (UAA) に基づいた完全に書き直されたオーディオスタックを特徴とする。オーディオスタックを再設計してアーキテクチャを変えた結果、DirectSoundからオーディオドライバへの直接のパスが存在しない形になった。DirectSoundと[MMEのような他の従来APIは](https://ja.wikipedia.org/wiki/Windows_Multimedia_Extensions "wikilink")[WASAPI](https://ja.wikipedia.org/wiki/WASAPI "wikilink")インターフェイスを用いてエミュレーションされている。すなわち、DirectSoundはマイクロソフトのソフトウェアミキサ上でエミュレーションモードで動いている。エミュレータはハードウェア抽象化がされていないので、DirectSoundをアクセラレーションできるハードウェアはない。これはDirectSoundのアクセラレーションに依存しているハードウェアないしソフトウェアのパフォーマンスが以前より下がってしまうことを意味する。しかし、よりパワーのあるハードウェアを使えば、パフォーマンス上の問題はないと考えられる。ただし、DirectSound3Dを使ってハードウェア的に3Dオーディオエフェクトをかけることはできなくなっている\[2\]。

[ASIO](../Page/ASIO.md "wikilink")や[OpenAL](https://ja.wikipedia.org/wiki/OpenAL "wikilink")のようなAPIは、Windows Vistaのアーキテクチャ変更による影響を受けないので、サウンドカードのドライバがこれらのAPIに対応すれば、サウンドデバイスのアクセラレーション機能を利用することができる。アプリケーションがこれらのアクセラレーション機能を使うには、DirectXやMMEを使わずにASIOやOpenALのAPIを使うようにプログラムを変更する必要がある。

WindowsにはもうひとつKernel StreamingというAPIがあり、ミキサを通らずにサウンドデバイスにアクセスできる。この方法でASIO4ALLというプロジェクトがASIO非対応のデバイスでASIOを使えるようにしている。

もうひとつの方法として、アプリケーションが使うオーディオスタックを差し替えて、OpenALを使わせてしまうという方法がある。この方法でCreative Labs社の*Creative ALchemy Project*という技術がDirectSoundのアクセラレーションをサポートしている\[3\]。

### Windows 8

### Windows CE

DirectSoundはWindows CEのバージョン4.2までサポートされているが、5.0になってから削除された。Windows CE 6.0はDirectSoundをサポートしていない。代わりにWaveform Audio APIを使ってアプリケーションを書き直すことが薦められている。

## XAudio

[Xbox 360と](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink")[Windowsを統合するために](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、マイクロソフトは、新しいアプリケーションを**XAudio**と**[XACT](https://ja.wikipedia.org/wiki/XACT "wikilink")**のようなXboxと同等なオーディオAPIに移行してもらうよう積極的に活動をしている。。**XAudio2**は、クロスプラットフォーム (WindowsとXbox) で共通に使える低レベルオーディオAPIであり、デジタル信号処理を最適に行うために設計されたXbox専用のAPIであるXAudio APIをさらに進化させたものである。XAudio2は[Windows XPや](https://ja.wikipedia.org/wiki/Windows_XP "wikilink")[Windows Vista](https://ja.wikipedia.org/wiki/Windows_Vista "wikilink")、そしてXbox 360上で利用できる。Windows XPではDirectSoundを、Windows Vistaでは[WASAPI](https://ja.wikipedia.org/wiki/WASAPI "wikilink") (新しいオーディオスタック) を、そしてXboxではコンソールハードウェアレイヤーを使って実装されている\[4\]。XAudio2はXACTを通してハイレベルなオーサリング/再生ができ、X3DAudioライブラリを通して3D機能を提供している。XACTエンジンは高レベルオーディオライブラリであり、**X3DAudio**はWindowsとXboxの両方のプラットフォーム上で利用可能な、空間音響用ヘルパーライブラリである。

XAudio2はXACTのような高レベルオーディオAPIのために、信号処理を使って特別なエフェクトを行う。いくつかの機能を以下に列挙する。

  - 「声」から音データを分離する
  - サブミキシング
  - Multi-rate processing
  - 1音声毎のフィルタリング
  - Programmable voices
  - エフェクト処理、[サンプルレート変換](https://ja.wikipedia.org/wiki/サンプルレート変換 "wikilink") (SRC)
  - ソフトウェア[DSP](https://ja.wikipedia.org/wiki/デジタル信号処理 "wikilink")
  - エンハンスト[サラウンド](https://ja.wikipedia.org/wiki/サラウンド "wikilink")サウンド (マルチチャンネル) と明示的なマルチチャンネル[panning](https://ja.wikipedia.org/wiki/パンニング_\(音響\) "wikilink")/mapping
  - ネイティブな圧縮データをサポート
      - [Xbox 360上での](https://ja.wikipedia.org/wiki/Xbox_360 "wikilink")[XMA](https://ja.wikipedia.org/wiki/XMA "wikilink")
      - Windows上での[ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")
      - その他拡張形式 ([xWMA](https://ja.wikipedia.org/wiki/xWMA "wikilink")\[5\] \[6\])
  - 分離かつ置換可能なライブラリによる3Dオーディオの処理。XAudio2はマルチチャンネルスピーカーを扱い、X3DAudioライブラリはスピーカーボリュームと他の様々なパラメータを入力することで、出力とリスナーの座標を変形することができる。

なお、[Windows 8用のソフトウェア開発キットである](https://ja.wikipedia.org/wiki/Windows_8 "wikilink")[Windows SDK](https://ja.wikipedia.org/wiki/Windows_SDK "wikilink") 8.0以降ではWindows SDKとDirectX SDKが統合されたが、その際に[XACT](https://ja.wikipedia.org/wiki/XACT "wikilink")が廃止された。またWindows 8において、デスクトップアプリでは依然としてDirectSoundが利用可能であるものの、[Windowsストア](https://ja.wikipedia.org/wiki/Windowsストア "wikilink")アプリ（[WinRTアプリ](https://ja.wikipedia.org/wiki/Windowsランタイム "wikilink")）ではDirectSoundは利用できず、XAudio2のみが利用可能となっている\[7\]。

[Windows 7およびそれ以前のOSでXAudio](https://ja.wikipedia.org/wiki/Windows_7 "wikilink")2を利用するためには、DirectXエンドユーザーランタイムもしくはDirectX SDKのインストールが必要であり、またXAudio2 v2.7までしか使用できないが、Windows 8以降にはXAudio2 v2.8\[8\]が、そして[Windows 10にはXAudio](https://ja.wikipedia.org/wiki/Windows_10 "wikilink")2 v2.9が標準搭載されている。

## 関連項目

  - DirectX Audio

      -
      - [XACT](https://ja.wikipedia.org/wiki/XACT "wikilink")

  - [Windows Multimedia Extensions](https://ja.wikipedia.org/wiki/Windows_Multimedia_Extensions "wikilink"), MME

  - , MCI

  - [Core Audio (Windows)](https://ja.wikipedia.org/wiki/Core_Audio_\(Windows\) "wikilink")

  - [WASAPI](https://ja.wikipedia.org/wiki/WASAPI "wikilink")

  - [レイテンシ](../Page/レイテンシ.md "wikilink")

  - [VST](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink")

  - [ASIO](../Page/ASIO.md "wikilink")

  - [Core Audio (アップル)](https://ja.wikipedia.org/wiki/Core_Audio_\(アップル\) "wikilink")

  -
## 脚注

## 外部リンク

  - [MSDN](https://ja.wikipedia.org/wiki/MSDN "wikilink")
      - \[<http://msdn.microsoft.com/en-us/library/bb174772(VS.85>).aspx Microsoft's DirectSound documentation\]
      - [DirectX オーディオ](https://msdn.microsoft.com/ja-jp/library/ee416797.aspx) (日本語)
      - [DirectSound](https://msdn.microsoft.com/ja-jp/library/ee416960.aspx) (日本語)
      - [XAudio2 の概要](https://msdn.microsoft.com/ja-jp/library/ee415737.aspx) (日本語)
      - [X3DAudio の概要](https://msdn.microsoft.com/ja-jp/library/ee415714.aspx) (日本語)
      - [DirectSound](https://msdn.microsoft.com/en-us/library/ee416960.aspx) (英語)
      - [XAudio2 APIs (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/hh405049.aspx) (英語)
      - [X3DAudio (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/ee415714.aspx) (英語)
  - [What's the deal with 3D sound under DirectX](http://www.gamedev.net/reference/articles/article593.asp)
  - [Audio in Windows Vista](http://forums.creative.com/creativelabs/board/message?board.id=Vista&message.id=1694)
  - [Creative ALchemy Project](http://preview.creativelabs.com/alchemy/default.aspx)

[Category:DirectX](https://ja.wikipedia.org/wiki/Category:DirectX "wikilink")

1.  [DirectX 8.0 の紹介](https://msdn.microsoft.com/ja-jp/library/dd148689.aspx)
2.  [［特集］Vista買うのはまだ早い！（3）ゲームサウンド編](http://www.4gamer.net/specials/tooearlytogetvista/003/tooearlytogetvista_003.shtml)
3.  [【4Gamer.net】［レビュー］Creative ALchemy](http://www.4gamer.net/review/alchemy/alchemy.shtml)
4.  [コア オーディオの概要](https://msdn.microsoft.com/ja-jp/library/cc307998.aspx)
5.  [Windows と Xbox 360 の違い](https://msdn.microsoft.com/ja-jp/library/cc308005.aspx)
6.  [XAudio2 Versions (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/ee415802.aspx)
7.  [Desktop Games on Windows 8.x - Games for Windows and the DirectX SDK - Site Home - MSDN Blogs](http://blogs.msdn.com/b/chuckw/archive/2012/03/23/desktop-games-on-windows-8-consumer-preview.aspx)
8.  [XAudio2 and Windows 8 – Games for Windows and the DirectX SDK](https://blogs.msdn.microsoft.com/chuckw/2012/04/02/xaudio2-and-windows-8/)