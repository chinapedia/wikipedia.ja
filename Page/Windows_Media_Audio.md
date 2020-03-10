> この記事は[Windows Media Audio](https://ja.wikipedia.org/wiki/Windows_Media_Audio)から翻訳されています。


**Windows Media Audio**（ウィンドウズ メディア オーディオ、**WMA**）は[マイクロソフト](../Page/マイクロソフト.md "wikilink")がWindows Mediaの中核を成す物として開発した[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")[コーデック](../Page/コーデック.md "wikilink")の一つ。[拡張子](../Page/拡張子.md "wikilink")はwma。通常[ASFに格納されて利用される](../Page/Advanced_Systems_Format.md "wikilink")。

元となるWindows Media Audio（WMA Std）の他に、圧縮アルゴリズムを一新し、多チャンネル高解像度に対応したWindows Media Audio Professional（WMA Pro）、[可逆圧縮](../Page/可逆圧縮.md "wikilink")のWindows Media Audio Lossless（WMA Lossless）、音声コンテンツ向けのWindows Media Audio Voice（WMA Voice）がある。これらは各々の仕様が異なるためWMA Stdのみ対応の機器では再生できない。

## 概要

### バージョン 1.0

WMAは[1999年](../Page/1999年.md "wikilink")4月にWindows Media Technologies 4.0の一部として発表された[MP3](../Page/MP3.md "wikilink")や[AAC](../Page/AAC.md "wikilink")、[Vorbis](https://ja.wikipedia.org/wiki/Vorbis "wikilink")等と同じく、[修正離散コサイン変換](https://ja.wikipedia.org/wiki/修正離散コサイン変換 "wikilink")をベースとしたコーデックである。最初のバージョンはWMA 1.0で開発段階ではMS Audioと呼ばれていた。[トムソンがMP](https://ja.wikipedia.org/wiki/トムソン_\(企業\) "wikilink")3の[ライセンス](../Page/ライセンス.md "wikilink")を保持し、[Microsoft Windowsで利用するにはライセンス料が発生する為](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")、代替形式を目指したのが開発の動機の一つと考えられている。[マイクロソフト](../Page/マイクロソフト.md "wikilink")ではWMAを、MP3と比較して半分のビットレートで同等の音質になる、CDと同等の音質を64kbpsで実現すると謳っていた。再生・圧縮ソフトウェアで自由に利用できる[SDKを配布したことから](../Page/ソフトウェア開発キット.md "wikilink")、WMAに対応する[フリーウェア](../Page/フリーウェア.md "wikilink")が以降多数登場した。

### バージョン 2

1999年ビットストリーム構造と圧縮アルゴリズムを修正したWMA2をリリース。仕様は固定され以降のバージョンでは再生互換性を維持している。

ASF形式出力のみの対応であるWMAだが、WMA2をハックした海賊版である[DivX Audio](https://ja.wikipedia.org/wiki/DivX "wikilink") ACMによりRIFF形式に対応し、AVI 形式の音声コーデックとして一時期使用された。

### バージョン 7

[2000年](../Page/2000年.md "wikilink")、[Windows Media Player](../Page/Windows_Media_Player.md "wikilink") 7が公開され、WMA2 からWMA7となりプレイヤーでのエンコードに対応するなど普及を推進した。

### バージョン 8

[2001年](../Page/2001年.md "wikilink")、Windows Media Player 8が公開され、WMA7からWMA8に改定。

### バージョン 9

[2003年](../Page/2003年.md "wikilink")、Windows Media Player 9が公開され、WMA9となり、[固定ビットレート](https://ja.wikipedia.org/wiki/固定ビットレート "wikilink")（CBR）に加えて平均ビットレート（ABR）や、VBR（[可変ビットレート](../Page/可変ビットレート.md "wikilink")圧縮）に対応することにより最大 20% [圧縮効率](https://ja.wikipedia.org/wiki/圧縮効率 "wikilink")を向上させた。さらにWMA9 Pro/WMA9 Lossless/WMA9 Voiceの三種類のコーデックが新たに追加された。

### バージョン 9.1

[2004年](../Page/2004年.md "wikilink")、Windows Media Player 10が公開され、WMA9.1/WMA9.1 Pro/WMA9.1 Losslessに改定。WMA9.1とWMA 9.1ProではCBRでの低遅延デコード、エンコードモードが追加された。

### バージョン 9.2及び10 Pro

[2007年](../Page/2007年.md "wikilink")、Windows Media Player 11が公開され、WMA 9.2/WMA 9.2 Lossless/WMA 10 Proに改定。

WMA 9.2では、[HE-AAC](https://ja.wikipedia.org/wiki/HE-AAC "wikilink")でも採用されている [SBRと呼ばれる技術を応用して](https://ja.wikipedia.org/wiki/Spectral_Band_Replication "wikilink")、従来低ビットレートではカットされていた高音域が再生できるようになった。これによりWindows Media Player 11でエンコードされたファイルは従来に比べて高音質での再生が可能となったが、一部の再生ハードウェアではWMA 9対応を謳っていてもWMA 9.2との互換性に問題があり再生中にノイズが乗ることがある。この問題はWindows Media Player 11にパッチを当てることで解決するが、音質も従来のものに戻る[1](http://support.microsoft.com/kb/929773/ja)。

WMA 10 ProはWMA 9 Proではビットレートが最低128kbpsまでだったのに対して、最低32kbpsまでのエンコードに対応した。低ビットレートにおいては、サンプリングレート補完モードによりWMA 9.2 Stdよりも最大二倍圧縮効率に優れるとされる。これは指定の半分のサンプリングレートでエンコードし、それに元のサンプリングレートの情報を添付し、再生時にWMA 10 Proにより元のレートに復元するというもので、再生品質は低下するものの従来のWMA 9 Proとの互換性を保っている。その他サンプリングレートとビット深度のオプションも増えて、非常に柔軟なコーデックとなっている。

[Windows Vistaでは付属ゲームの効果音に使用され](https://ja.wikipedia.org/wiki/Microsoft_Windows_Vista "wikilink")、[サウンド レコーダーの標準形式となっている](../Page/サウンド_レコーダー.md "wikilink")。

WMAはOSにバンドルするなど、MP3の置き換えを目指したが、MP3形式を置き換えるには至らなかった。一方、[インターネットラジオ](../Page/インターネットラジオ.md "wikilink")などの[ストリーミング](../Page/ストリーミング.md "wikilink")配信では、それまで主流だった[RealAudio](../Page/RealAudio.md "wikilink")に匹敵するまでに普及したが次第に衰退した。

## 再生環境

WMAは、様々な機器が対応しているが、マイクロソフト独自の形式であり、MP3等の形式と比べると汎用性で劣る。

[FFmpeg](../Page/FFmpeg.md "wikilink")計画によるリバースエンジニアリングにより、WMA Losslessを除き[Linux](../Page/Linux.md "wikilink")等の[POSIX](../Page/POSIX.md "wikilink")準拠のOSで再生が可能となっている。

[Macintosh](../Page/Macintosh.md "wikilink")環境ではマイクロソフトが推奨するサードパーティのFlip4Mac QuickTimeコンポーネントによりWMA Voiceを除き再生が可能である。

[ソニー](../Page/ソニー.md "wikilink")の[ウォークマン](../Page/ウォークマン.md "wikilink")は初期のモデルではWMAを再生できなかった（当初は[ATRAC](https://ja.wikipedia.org/wiki/ATRAC "wikilink")のみだった）が、現在では再生可能である。その他、[東芝](../Page/東芝.md "wikilink")の[gigabeat](https://ja.wikipedia.org/wiki/gigabeat "wikilink")や[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")の[D-snap](https://ja.wikipedia.org/wiki/D-snap "wikilink")（内蔵メモリ型のみ、[SDメモリ型は](https://ja.wikipedia.org/wiki/SDメモリーカード "wikilink") [SD-Audio](../Page/SD-Audio.md "wikilink") で[CPRM](https://ja.wikipedia.org/wiki/CPRM "wikilink")によるセキュア化で再生可能）等多くの[音楽再生機器が対応している](../Page/デジタルオーディオプレーヤー.md "wikilink")。

携帯電話については[2006年](../Page/2006年.md "wikilink")に発売された [NTTドコモ](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")「[F902iS](../Page/F902iS.md "wikilink")」を筆頭に、NTTドコモの端末がWindows Media Audioの再生に対応し、904iシリーズ以降の90xi端末はシリーズ全機種が再生に対応している。[au](https://ja.wikipedia.org/wiki/au_\(携帯電話\) "wikilink")（[KDDI](../Page/KDDI.md "wikilink")・[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")[連合](https://ja.wikipedia.org/wiki/連合 "wikilink")）の携帯電話では、「[LISMO](../Page/LISMO.md "wikilink")（[au Music Port](https://ja.wikipedia.org/wiki/au_Music_Port "wikilink")）」で一度[HE-AAC](https://ja.wikipedia.org/wiki/HE-AAC "wikilink")に変換、もしくは「[LISMO Port](https://ja.wikipedia.org/wiki/LISMO_Port "wikilink")」で一度[ATRAC](https://ja.wikipedia.org/wiki/ATRAC "wikilink")に変換した後、端末に転送することで再生できる。[ソフトバンクモバイル](https://ja.wikipedia.org/wiki/ソフトバンクモバイル "wikilink")の端末においては、「[S\!ミュージックコネクト](../Page/S!ミュージックコネクト.md "wikilink")」によってWMAに対応している。

[Android](../Page/Android.md "wikilink")のスマートフォンであれば、標準搭載されている音楽再生ソフトは、WMA Losslessを除き、殆どの機種で対応している。WMA Losslessは対応するソフトをインストールすることで、再生可能である。

[Rockbox](../Page/Rockbox.md "wikilink")を使用することで、通常は再生ができない[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")などでの再生が可能である。

WMA Lossless/WMA Proのハードウェアサポートは2007年現在、ごく一部でのみの対応にとどまっている。マイクロソフトの[Zune](../Page/Zune.md "wikilink"), [Xbox 360は](../Page/Xbox_360.md "wikilink")、WMA Pro/WMA Losslessの両方が再生可能。WMA Losslessは東芝の Gigabeatの一部機種、[Windows Mobile端末のWindows](https://ja.wikipedia.org/wiki/Windows_Mobile "wikilink") Media Player 10 Mobileで再生できる。なおWMA Lossless/WMA Proは再生機器に応じて自動でステレオもしくはモノラルにダウンミックス、24ビットから16ビットにダウンコンバート、96kHzから48kHzにダウンサンプリングし再生することが可能である。

## 関連項目

  - [Windows Media Video](https://ja.wikipedia.org/wiki/Windows_Media_Video "wikilink")
  - [Advanced Systems Format](../Page/Advanced_Systems_Format.md "wikilink")
  - [音声ファイル形式](../Page/音声ファイルフォーマット.md "wikilink")
  - [データ圧縮](../Page/データ圧縮.md "wikilink")

## 外部リンク

  - [.wmaファイル拡張子](http://ja.filesupport.org/file-extension/wma)
  - [Windows Media 9 シリーズ - 最高のオーディオ](http://www.microsoft.com/japan/windows/windowsmedia/9series/codecs/audio.aspx)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:Windows_Media](https://ja.wikipedia.org/wiki/Category:Windows_Media "wikilink") [Category:音声処理](https://ja.wikipedia.org/wiki/Category:音声処理 "wikilink")