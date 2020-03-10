> この記事は[Rosegarden](https://ja.wikipedia.org/wiki/Rosegarden)から翻訳されています。


**Rosegarden**（ローズガーデン）は、[ALSAと](https://ja.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture "wikilink")[KDE](../Page/KDE.md "wikilink")を利用して[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")で開発された[フリーソフトウェア](../Page/フリーソフトウェア.md "wikilink")の[デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")である。[オーディオ](https://ja.wikipedia.org/wiki/音響機器 "wikilink")、[MIDI](../Page/MIDI.md "wikilink")[シーケンサー](https://ja.wikipedia.org/wiki/ミュージックシーケンサー "wikilink")、[楽譜作成ソフトウェア](https://ja.wikipedia.org/wiki/楽譜作成ソフトウェア "wikilink")、[作曲](../Page/作曲.md "wikilink")、および編集ツールとして機能する。 [Cubase](../Page/Cubase.md "wikilink")の編集機能の代用を意図している。

Rosegardenは組み込みの[ソフトウェア・シンセサイザー](https://ja.wikipedia.org/wiki/ソフトウェア・シンセサイザー "wikilink")を提供しないので、MIDI構成から音を作り出すためにはハードウェアMIDIシンセサイザー、[FluidSynth](https://ja.wikipedia.org/wiki/FluidSynth "wikilink")や[TiMidity++](../Page/TiMidity++.md "wikilink")のようなソフトウェアシンセサイザーか、シンセサイザープラグインを必要とする。Rosegardenの最近のバージョンでは[DSSI](https://ja.wikipedia.org/wiki/DSSI "wikilink")ソフトウェアシンセサイザープラグインインターフェイスをサポートし、アダプターを通してWindows [VSTプラグインが使える](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink")。

## 機能

  - [ALSAと](https://ja.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture "wikilink")[JACKによる](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")、[MIDI](../Page/MIDI.md "wikilink")とオーディオの再生とレコーディング
  - [ピアノロール](../Page/ピアノロール.md "wikilink")、スコア、イベントリストとトラックオーバービューエディタ
  - [DSSI](https://ja.wikipedia.org/wiki/DSSI "wikilink")シンセサイザとオーディオエフェクトプラグインのサポート、Windows VSTエフェクトとインストゥルメントをDSSI-VST経由でサポートすることも含まれる
  - [LADSPA](https://ja.wikipedia.org/wiki/LADSPA "wikilink")オーディオエフェクトプラグインのサポート
  - [JACKの転送機能により他のソフトウェアとの同期をサポートする](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")
  - [MIDI](../Page/MIDI.md "wikilink")編集機能のみを使用するのであれば、JACKなしでビルドし動作させることができる
  - MIDI演奏データの楽譜印刷
  - シェアエイブルデバイスファイルはMIDIの移植性を容易にする
  - パターンシーケンシング＆装飾音の演奏を引き起こすセグメント
  - オーディオミキサーとMIDIミキサー
  - MIDIと[Hydrogen](https://ja.wikipedia.org/wiki/Hydrogen "wikilink")ファイルのインポート
  - MIDI、[Csound](../Page/Csound.md "wikilink")、[LilyPondと](https://ja.wikipedia.org/wiki/GNU_LilyPond "wikilink")[MusicXML](https://ja.wikipedia.org/wiki/MusicXML "wikilink")ファイルのエクスポート（生成された楽譜の[PostScript](../Page/PostScript.md "wikilink")とPDF出力を含む）
  - ロシア語、スペイン語、ドイツ語、フランス語、ウェールズ語、イタリア語、スウェーデン語、エストニア語、日本語、簡体字中国語、オランダ語、ポーランド語、チェコ語、カタロニア語、フィンランド語、イギリス、及び米国の英語へのユーザインタフェースの翻訳
  - 英語はもとよりドイツ語、スウェーデン語、および日本語に大部分かすべて翻訳されたヘルプドキュメントが利用可能である。

## 歴史

Rosegarden2.1と呼ばれ、現在はX11 Rosegardenとして知られているプログラムと区別するために、同じ作者による後発の現在のRosegardenプログラムは最初Rosegarden-4と命名された。 Rosegarden2.1は非常に制限されているが、さまざまな[Unix系](../Page/Unix系.md "wikilink")オペレーティングシステムや[OpenVMS](https://ja.wikipedia.org/wiki/OpenVMS "wikilink")などの他のプラットホームで安定して動作する。対照的に、Rosegarden-4がLinux ALSAシステムを使うので、非Linuxシステムの上では非常に限られた方法で動作する。

Rosegardenプロジェクトは[1993年](../Page/1993年.md "wikilink")にバース大学で始まった。Rosegarden 2.1(X11 Rosegarden) は[GPLの元で](../Page/GNU_General_Public_License.md "wikilink")1997年にリリースされた。Rosegarden4は2000年4月に始まった。バージョン1.0は[2005年](https://ja.wikipedia.org/wiki/2005年 "wikilink")[2月14日](../Page/2月14日.md "wikilink")（[バレンタインデー](https://ja.wikipedia.org/wiki/バレンタインデー "wikilink")）にリリースされ、バージョン1.2.4は[2006年](https://ja.wikipedia.org/wiki/2006年 "wikilink")[7月14日](../Page/7月14日.md "wikilink")（[パリ祭](https://ja.wikipedia.org/wiki/パリ祭 "wikilink")）にリリースされた。

## 関連項目

  - [GNU LilyPond](https://ja.wikipedia.org/wiki/GNU_LilyPond "wikilink")
  - [MusE](https://ja.wikipedia.org/wiki/MusE "wikilink")
  - [Hydrogen (ソフトウェア)](https://ja.wikipedia.org/wiki/Hydrogen_\(ソフトウェア\) "wikilink")
  - [Ardour](https://ja.wikipedia.org/wiki/Ardour "wikilink")
  - [NoteEdit](https://ja.wikipedia.org/wiki/NoteEdit "wikilink")

## 外部リンク

  - [Rosegarden 公式ホームページ](http://www.rosegardenmusic.com/)
  - [Rosegardenのダウンロードページ (Sourceforge.net)](http://sourceforge.net/project/showfiles.php?group_id=4932)
  - [Rosegarden user/dev フォーラム](http://www.nabble.com/RoseGarden-f2887.html) - 記事を探すならここで
  - [Rosegarden Development Wiki](http://rosegarden.wiki.sourceforge.net) - 公式開発サイト

[Category:音楽ソフトウェア](https://ja.wikipedia.org/wiki/Category:音楽ソフトウェア "wikilink") [Category:コンピュータミュージック](https://ja.wikipedia.org/wiki/Category:コンピュータミュージック "wikilink") [Category:KDE](https://ja.wikipedia.org/wiki/Category:KDE "wikilink")