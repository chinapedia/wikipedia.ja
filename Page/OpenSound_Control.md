> この記事は[OpenSound Control](https://ja.wikipedia.org/wiki/OpenSound_Control)から翻訳されています。


**OpenSound Control**（**OSC**）とは、[電子楽器](../Page/電子楽器.md "wikilink")（特に[シンセサイザー](../Page/シンセサイザー.md "wikilink")）やコンピュータなどの機器において音楽演奏データをネットワーク経由でリアルタイムに共有するための[通信プロトコル](../Page/通信プロトコル.md "wikilink")である。[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")にある [CNMAT](https://ja.wikipedia.org/wiki/:en:CNMAT "wikilink")（The Center for New Music and Audio Technologies）が開発した。

## 概要

OSC は[MIDI](../Page/MIDI.md "wikilink")の代替となることを意図して設計されている。MIDIは[1982年](../Page/1982年.md "wikilink")に実装されたもので、最近の[マルチメディア](../Page/マルチメディア.md "wikilink")用途には適していない部分が多い。通信プロトコルであるため、OSCによって、楽器や[MIDIコントローラや各種マルチメディア機器が屋内のネットワーク](https://ja.wikipedia.org/wiki/MIDIコントローラー "wikilink")（[TCP/IP](https://ja.wikipedia.org/wiki/TCP/IP "wikilink")、[イーサネット](../Page/イーサネット.md "wikilink")）や[インターネット](../Page/インターネット.md "wikilink")を経由して通信することが可能となる。OSCはブロードバンド・ネットワークの通信速度を最大限に活かしてデータ転送を行うため、31.250\[kbps\]と言う規格上の速度上限があったMIDIでは不可能な新たな利用方法が可能となっている。また、転送データの柔軟性も増しており、より高度なレベルでの通信が可能である。

OSCは様々なプロトコル上で転送可能だが、一般に[UDPが使われる](../Page/User_Datagram_Protocol.md "wikilink")。なお、同じチームがかつて開発したZIPIプロトコル ([Zeta Instrument Processor Interface](https://ja.wikipedia.org/wiki/:en:Zeta_Instrument_Processor_Interface "wikilink"))は失敗に終わった。

特徴:

  - オープンエンドで動的な[URL風の命名規則を採用](../Page/Uniform_Resource_Locator.md "wikilink")
  - 記号的データと高精度数値データ
  - 1つのメッセージの受信者を複数指定できる[パターンマッチ言語](../Page/パターンマッチング.md "wikilink")
  - 細かい時刻タグ
  - 同時に発生すべき効果を指定したメッセージ群を集めた「バンドル」
  - OSCサーバの持つ機能を動的に探したり、文書を入手するのに使われる[クエリ](https://ja.wikipedia.org/wiki/クエリ "wikilink")システム

OSC の実装はいくつもあり、リアルタイム音響処理環境、ウェブ操作ツール、ソフトウェアシンセサイザー、各種プログラミング言語、ハードウェア機器などがある。OSC は、コンピュータを使った音楽表現、ネットワークによる分散音楽システム、プロセス間通信、単一のアプリケーションでも使われている。

OSC は [LADSPA](https://ja.wikipedia.org/wiki/LADSPA "wikilink") の進化した [DSSI](https://ja.wikipedia.org/wiki/:en:DSSI "wikilink") プラグイン API の中心部にも使われており、[GUIと演奏アプリケーションなどとの通信を担当している](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。LADSPA と DSSI は、音響効果・合成に関する [Linux](../Page/Linux.md "wikilink") API である。

OSC を実装しているソフトウェアの例:

  - [Bidule](https://ja.wikipedia.org/wiki/Bidule "wikilink")
  - [ChucK](https://ja.wikipedia.org/wiki/ChucK "wikilink")
  - [Csound](../Page/Csound.md "wikilink")
  - [CoGe](https://ja.wikipedia.org/wiki/CoGe "wikilink")
  - [Isadora](https://ja.wikipedia.org/wiki/Isadora "wikilink") (v.1.1)
  - [Max/MSP](../Page/Max_\(ソフトウェア\).md "wikilink")
  - [Modul8](https://ja.wikipedia.org/wiki/Modul8 "wikilink")
  - [openFrameworks](https://ja.wikipedia.org/wiki/openFrameworks "wikilink")
  - [OSCpad](https://ja.wikipedia.org/wiki/OSCpad "wikilink") iPad に基づいて HTML5, CSS3, Javascript
  - [Pure Data](../Page/Pure_Data.md "wikilink")
  - [Quartz Composer](https://ja.wikipedia.org/wiki/Quartz_Composer "wikilink")
  - [Reaktor](../Page/Reaktor.md "wikilink")
  - [Renoise](https://ja.wikipedia.org/wiki/Renoise "wikilink") (v2.6)
  - [SuperCollider](../Page/SuperCollider.md "wikilink")
  - [Squeak](../Page/Squeak.md "wikilink")
  - [Traktor DJ Studio](https://ja.wikipedia.org/wiki/Traktor_DJ_Studio "wikilink")
  - [Mxwendler](https://ja.wikipedia.org/wiki/Mxwendler "wikilink")
  - [Crystal Space](https://ja.wikipedia.org/wiki/Crystal_Space "wikilink")
  - [GlovePIE](https://ja.wikipedia.org/wiki/GlovePIE "wikilink")
  - [VDMX5](https://ja.wikipedia.org/wiki/VDMX5 "wikilink")
  - TouchDesigner

OSC を実装しているハードウェアの例:

  - [Lemur Input Device](https://ja.wikipedia.org/wiki/Lemur_Input_Device "wikilink")
  - [Monome 40h](https://ja.wikipedia.org/wiki/Monome_40h "wikilink")

2007年9月、コントローラ、シンセサイザー、ホスト間の通信のための [SYN 名前空間](http://stud3.tuwien.ac.at/~e0725639/OSC-SYN.txt) 標準の提案がなされている。

## 参考文献

  - Wright, M., Freed, A., "Open Sound Control: A New Protocol for Communicating with Sound Synthesizers", International Computer Music Conference, Thessaloniki, Greece, 1997.

## 外部リンク

  - [OpenSound Control page](http://www.cnmat.berkeley.edu/OpenSoundControl/) at CNMAT
  - [opensoundcontrol.org](http://opensoundcontrol.org/)
  - [OpenSound Control](http://megaui.net/oss4art/wiki/OpenSound_Control) Oss4art

[Category:工業規格](https://ja.wikipedia.org/wiki/Category:工業規格 "wikilink") [Category:電子楽器](https://ja.wikipedia.org/wiki/Category:電子楽器 "wikilink") [Category:シンセサイザー](https://ja.wikipedia.org/wiki/Category:シンセサイザー "wikilink") [Category:音楽ソフトウェア](https://ja.wikipedia.org/wiki/Category:音楽ソフトウェア "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink")