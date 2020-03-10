> この記事は[Speex](https://ja.wikipedia.org/wiki/Speex)から翻訳されています。


**Speex**（スピークス） は、[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")アプリケーションや[ポッドキャスト](https://ja.wikipedia.org/wiki/ポッドキャスト "wikilink")で使われる[フリーな音声圧縮](../Page/フリーソフトウェア.md "wikilink")[コーデック](../Page/コーデック.md "wikilink")である。Speex は、[特許によるいかなる制限もなく](https://ja.wikipedia.org/wiki/ソフトウェア特許 "wikilink")、三条項[BSDライセンス](https://ja.wikipedia.org/wiki/BSDライセンス "wikilink")でライセンスされている。[Ogg](https://ja.wikipedia.org/wiki/Ogg "wikilink")[コンテナフォーマット](https://ja.wikipedia.org/wiki/コンテナフォーマット "wikilink")と共に使ったり、直接 [UDP](../Page/User_Datagram_Protocol.md "wikilink")/[RTP](https://ja.wikipedia.org/wiki/Real-time_Transport_Protocol "wikilink") 上で転送する形で使う事もできる。

Speex は、汎用的な音声圧縮プロジェクトであった [Vorbis](https://ja.wikipedia.org/wiki/Vorbis "wikilink") を補完するものとされていた。

Speex は[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")であり、圧縮によって[音質](https://ja.wikipedia.org/wiki/音質 "wikilink")が損なわれ、元の音質に戻すことはできない。

開発元の[Xiph.OrgはSpeexを廃止しており](https://ja.wikipedia.org/wiki/Xiph.Org_Foundation "wikilink")、新しいコーデックである[Opusがすべての面でSpeexを上回るとして](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink")、後継として推奨している。

## 概要

他の音声コーデックとは異なり、Speex は携帯電話をターゲットにはせず、[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink") やファイル上の圧縮をターゲットにしている。設計目標は、高品質音声と低ビットレートに最適化されたコーデックであった。このため、このコーデックは複数のビットレートを使い、超広帯域（[サンプリング周波数](../Page/サンプリング周波数.md "wikilink") 32[kHz](../Page/ヘルツ.md "wikilink")）、広帯域（サンプリング周波数 16kHz）、狭帯域（電話レベル、サンプリング周波数 8kHz）をサポートする。携帯電話ではなく VoIP 向けということから、Speex はパケット喪失に耐性があるよう設計されているが、パケットの破損には弱い（[UDPはパケットが到達しない可能性はあるが](../Page/User_Datagram_Protocol.md "wikilink")、到達した場合は破損していないことを保証するため）。そのため、Speex の符号化技法としては [Code Excited Linear Prediction](https://ja.wikipedia.org/wiki/Code_Excited_Linear_Prediction "wikilink") (CELP) が選択された。CELP が選ばれた理由の1つとして、低[ビットレート](../Page/ビット毎秒.md "wikilink")（DoD CELP では 4.8 kbit/s）から高ビットレート（[G.728](https://ja.wikipedia.org/wiki/G.728 "wikilink") では 16 kbit/s）まで利用可能だという点が挙げられる。主な特徴は次の通り。

  - [オープン標準](../Page/オープン標準.md "wikilink")であり、[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")/[ロイヤルティー](https://ja.wikipedia.org/wiki/ロイヤルティー "wikilink")フリーである。
  - 狭帯域と広帯域を同じビットストリームに統合。
  - 広範囲なビットレート（2 kbit/s から 44 kbit/s）
  - 動的ビットレート切り替えと[可変ビットレート](../Page/可変ビットレート.md "wikilink") (VBR)
  - 発話区間検出（VAD、VBRと統合）
  - 圧縮率が可変
  - 32 kHz での超広帯域モード（最大 48 kHz）
  - インテンシティステレオ符号化オプション（左右の音量差のみで[ステレオ](../Page/ステレオ.md "wikilink")にする方式）

## 機能

  - サンプリング周波数
    Speex は主に 8 kHz（電話でのサンプリング周波数と同じ）、16 kHz、32 kHz の3種類のサンプリング周波数を対象として設計されている。これらをそれぞれ、狭帯域、広帯域、超広帯域と呼ぶ。
  - 音質
    Speex での符号化は音質パラメータで制御され、その値は 0 から 10 の範囲である。[固定ビットレート](https://ja.wikipedia.org/wiki/固定ビットレート "wikilink") (CBR) の場合、音質パラメータは[整数](../Page/整数.md "wikilink")であり、可変ビットレート (VBR) の場合は実数（[浮動小数点数](../Page/浮動小数点数.md "wikilink")）である。
  - 可変計算量
    Speex では、エンコーダでの計算量（圧縮率）を変化させることができる。[gzip](https://ja.wikipedia.org/wiki/gzip "wikilink") で圧縮率を -1 から -9 で指定するように、1 から 10 の範囲で探索方法を指定することで計算量を制御する。一般に、計算量 1 でのノイズレベルは、計算量 10 のノイズレベルに比べて 1 dB から 2 dB 高いが、計算量 10 の場合の[CPU](../Page/CPU.md "wikilink")使用量は計算量 1 の場合の約5倍である。実際には計算量 2 から 4 が最もバランスがよいとされるが、人間の声以外の音を扱う場合やリアルタイム性を求められない場合は計算量を大きくする。
  - 可変ビットレート (VBR)
    符号化している音声の複雑さに応じて動的にビットレートを変化させる。例えば、[母音](../Page/母音.md "wikilink")や波形の振幅が急激に変化する箇所では高ビットレートが必要となるが、[摩擦音](https://ja.wikipedia.org/wiki/摩擦音 "wikilink")（さ行など）はビット数が少なくてもよい。このため、VBRは同じ音質であればより低いビットレートを達成できるし、同じビットレートであればより高い音質を達成できる。しかし、VBR にも欠点がある。まず、音質を一定に保とうとした場合、最終的な平均ビットレートがどうなるかを保証できない。次に、[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")のようなリアルタイム・アプリケーションでは最大ビットレートが通信路の上限よりも低くなければならない。
  - 平均ビットレート (ABR)
    ABR は VBR の問題の一部を解決するもので、平均ビットレートを指定してVBRでの音質を調整する。音質とビットレートはリアルタイムで調整されるため、実際に得られる音質は理想的な可変ビットレートでの音質よりも若干悪くなる傾向にある。
  - 発話区間検出 (VAD)
    対象とする音声信号が無音となっている区間（背景雑音のみの区間）を検出する。VBRを行っている際は暗黙のうちにVADも行われる。Speex では無音区間を検出すると、背景雑音を再生するのに十分なビット列に符号化する。これを "Confort Noise Generation" (CNG) と呼ぶ。
  - 不連続転送 (DTX)
    一定の背景雑音だけの区間について転送を完全に止めてしまう方式。ファイル上では、そのようなフレームを5ビットで表す（つまり、1秒間無音であれば、250ビットで表される）
  - 知覚改良
    知覚改良 (Perceptual Enhancement) とはデコーダの機能であり、符号化・復号の過程で生じるノイズを知覚されにくくする。多くの場合、知覚改良によって音声はオリジナルとは違ったものになるが、人間が聴いたときよりよい音質に聞こえる。
  - アルゴリズム的遅延
    コーデックは一般に転送時に遅延を生じる。Speex では、遅延はフレームサイズに比例し、各フレームの処理で必要とされる先読みの量に対応した時間がそれに加算される。狭帯域（8 kHz）での遅延は 30ms だが、広帯域（16 kHz）での遅延は 34ms となる。この遅延時間には符号化・復号にかかるCPU時間は含まれない。

## MIME

Speex の[メディアタイプ](https://ja.wikipedia.org/wiki/メディアタイプ "wikilink")は Ogg に格納される場合は audio/ogg であり、RTP 経由で転送される場合やコンテナがない場合は audio/speex である。IANA登録前は audio/x-speex であった。

## 応用

Speex コーデックの利用は、[遠隔会議](https://ja.wikipedia.org/wiki/遠隔会議 "wikilink")のような[ストリーミング](../Page/ストリーミング.md "wikilink")からゲームや音声処理まで広範囲に渡る。例えば、[DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")フィルタ、[Microsoft Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") での [NetMeeting](../Page/Microsoft_NetMeeting.md "wikilink")、[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink") の [OpenH323](https://ja.wikipedia.org/wiki/OpenH323 "wikilink")（[Ekiga](https://ja.wikipedia.org/wiki/Ekiga "wikilink")）などがある。[Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink") や [XMMS](https://ja.wikipedia.org/wiki/XMMS "wikilink") プレイヤー向けの[プラグイン](../Page/プラグイン.md "wikilink")もある。また、[foobar2000](https://ja.wikipedia.org/wiki/foobar2000 "wikilink") も Speex をサポートしている。

[Adobe Flash](../Page/Adobe_Flash.md "wikilink") Player は 10.0 からサポートしている。変更可能だが、デフォルトは広帯域(16kHz)の固定ビットレートの20.6kbpsに設定されている。[Adobe AIR](https://ja.wikipedia.org/wiki/Adobe_Integrated_Runtime "wikilink") は 1.5 から利用可能。

マイクロソフトの [Xbox Live](https://ja.wikipedia.org/wiki/Xbox_Live "wikilink") ではヘッドセットに Speex を使っている。

最新の [Half-Life 1](https://ja.wikipedia.org/wiki/ハーフライフ_\(ゲーム\) "wikilink") エンジンでは、ゲーム内のVoIP機能として Speex コーデックを使っている。デフォルトでは使われない設定になっており、サーバ管理者による設定が必要である。デフォルトの Miles ビデオコーデックよりも音質がよい。

[ジェネラル・ダイナミクス](https://ja.wikipedia.org/wiki/ジェネラル・ダイナミクス "wikilink")製の[アメリカ陸軍](https://ja.wikipedia.org/wiki/アメリカ陸軍 "wikilink")の [Land Warrior](https://ja.wikipedia.org/wiki/:en:Land_Warrior "wikilink") システムでは、[レイセオン](https://ja.wikipedia.org/wiki/レイセオン "wikilink")の設計した[EPLRS](https://ja.wikipedia.org/wiki/EPLRS "wikilink")ラジオでのVoIPに Speex を使っている。

シド・メイヤーの [Civilization IV](../Page/シヴィライゼーション.md "wikilink") では、[レナード・ニモイ](https://ja.wikipedia.org/wiki/レナード・ニモイ "wikilink")のナレーションを Speex で圧縮している。

VoIPソフト [TeamSpeak](https://ja.wikipedia.org/wiki/TeamSpeak "wikilink") は3種類のコーデックの1つとして Speex をサポートしている。参加人数に関わらず音質がよいことから、Speex がよく使われる。

[Rockbox](https://ja.wikipedia.org/wiki/Rockbox "wikilink") では音声インタフェースに Speex を使っている。また、Speex ファイルの再生も可能。

## 外部リンク

  -
  - [Speex Codec Manual](https://www.speex.org/docs/manual/speex-manual/)

  - [プラグインとソフトウェア](https://www.speex.org/software/)

  - [JSpeex](http://jspeex.sourceforge.net) - Javaプラットフォームへの Speex の [JNI](https://ja.wikipedia.org/wiki/JNI "wikilink") wrapper

[Category:Xiph.Org](https://ja.wikipedia.org/wiki/Category:Xiph.Org "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:音声処理ソフト](https://ja.wikipedia.org/wiki/Category:音声処理ソフト "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")