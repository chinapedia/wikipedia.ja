> この記事は[Ubuntu Studio](https://ja.wikipedia.org/wiki/Ubuntu_Studio)から翻訳されています。


**Ubuntu Studio**（ウブントゥ・スタジオ、ウブンツ・スタジオ）は、[Ubuntu](../Page/Ubuntu.md "wikilink")から派生した[Linuxディストリビューション](../Page/Linuxディストリビューション.md "wikilink")である。[マルチメディア](../Page/マルチメディア.md "wikilink")編集環境に特化している。オリジナルバージョンはUbuntu 7.04をベースにして、[2007年](../Page/2007年.md "wikilink")[5月10日](../Page/5月10日.md "wikilink")にリリースされた。

以前の[デスクトップ環境](https://ja.wikipedia.org/wiki/デスクトップ環境 "wikilink")は[GNOME](../Page/GNOME.md "wikilink")であったが、派生元の環境が変更された事により[Xfce](../Page/Xfce.md "wikilink")を標準として採用している。

コンテンツクリエイター向けにマルチメディア関連の機能が大幅に強化されている。従って、伝統的には[ソフトウェア](../Page/ソフトウェア.md "wikilink")開発機/[サーバ](../Page/サーバ.md "wikilink")構築に用いられてきた[Unix系](../Page/Unix系.md "wikilink")[オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink") (OS) としては、極めて特殊な位置付けとなっている。

## 特徴

先述のとおり、Ubuntu Studioはマルチメディア（音楽・映像・画像）編集に特化しており、そのためのソフトウェアを多数、標準で[インストール](../Page/インストール.md "wikilink")する。また、実行遅延（レイテンシ）を低減する設定が行われており、それら[ソフトウェア](../Page/ソフトウェア.md "wikilink")が即時処理（リアルタイム処理）を行うことを可能としている。派生元のUbuntuとは、割り込み発生回数を毎秒1000回に増やしたlow-latency[カーネル](../Page/カーネル.md "wikilink")を採用することにより、音声再生の遅延を低減している点で大きく異なっている。

テーマについては独自のアートワークに基づき、青と黒で構成されたものを用いている。

Ubuntuに直接の支援を受けているプロジェクトであり\[1\]、マルチメディア編集環境に関するフィードバックを行うことで貢献している。Ubuntuとは標準でインストールされるパッケージの種類やシステム設定が多少異なるのみで、ベースシステムは同じである。

## インストール

Ubuntu Studioは、[ISOイメージ](https://ja.wikipedia.org/wiki/ISOイメージ "wikilink")[ファイルの形で提供されている](../Page/ファイル_\(コンピュータ\).md "wikilink")。

使用者はまず、[ダウンロード](https://ja.wikipedia.org/wiki/ダウンロード "wikilink")したこの[ファイルから](../Page/ファイル_\(コンピュータ\).md "wikilink")[ブート](../Page/ブート.md "wikilink")可能な[ディスク](https://ja.wikipedia.org/wiki/ディスク "wikilink")を作成し、そのディスクから[コンピュータ](../Page/コンピュータ.md "wikilink")を起動してインストール作業に入る。インストール作業は、画面に表示されたメッセージに従ってキーボードで操作を行うことで進行する。Ubuntu StudioのISOイメージファイルのサイズは1GB以上であり、標準的な[CD-ROM](../Page/CD-ROM.md "wikilink")の記憶容量を超えている。そのため、ブート可能なディスクは[DVD](../Page/DVD.md "wikilink")、もしくは[USBや](../Page/ユニバーサル・シリアル・バス.md "wikilink")[ネットワークで起動するディスクに作成する必要がある](../Page/コンピュータネットワーク.md "wikilink")。

既にUbuntuをインストールしてあれば、[インターネット](../Page/インターネット.md "wikilink")経由でパッケージ「ubuntustudio-desktop」といったパッケージを導入することでもインストールできる。

## 短い実行遅延（低レイテンシ）の実現

実行遅延（[レイテンシ](../Page/レイテンシ.md "wikilink")）とは、デバイスからの入力信号をコンピュータが処理し、その処理結果を帰すまでの遅延時間のことである。コンピュータのハードウェアとしての制約がその原因であり、どれほど高性能なコンピュータだろうが、どのようなデバイスを用いた操作だろうが、大なり小なり[レイテンシ](../Page/レイテンシ.md "wikilink")は発生する。

製作環境においては、例えば[MIDI](../Page/MIDI.md "wikilink")[キーボードを押して発信した信号が音声として出力されるまでの遅延時間や](../Page/キーボード_\(楽器\).md "wikilink")、[ペンタブレット](../Page/ペンタブレット.md "wikilink")による入力が画面に描画されるまでの遅延時間がこれに該当する。実行遅延の大小は製作者のパフォーマンスに直接影響するため、可能な限り短いのが望ましい。

サウンド処理に限定すると、実行遅延の短縮は、[Windowsでは](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ASIO](../Page/ASIO.md "wikilink")ドライバ、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")では[Core Audioドライバ](../Page/Core_Audio_\(アップル\).md "wikilink")（[Mac OS 9以前は](https://ja.wikipedia.org/wiki/Classic_Mac_OS#Mac_OS_9 "wikilink")[Sound Manager](https://ja.wikipedia.org/wiki/Sound_Manager "wikilink")）などで実現している。

ではLinuxの場合はというと、カーネルがドライバを含む構造（[モノリシックカーネル](../Page/モノリシックカーネル.md "wikilink")）となっているため、カーネル周りを調整することで対策している。具体的には以下である。

  - カーネルにCONFIG_PREEMPT_RTパッチを適用したリアルタイムカーネルを利用する\[2\]
  - カーネルの設定を変更しタイマー割り込みの頻度を増やす\[3\]
  - PAMの設定を変更し、アプリケーションのカーネル・スケジューラー内での処理の優先度を変更する\[4\]

これらの設定はオーディオに限らずシステム全体に影響するため、多様な製作目的に合致したシステムを構築することが可能である。

リアルタイム・カーネルとは、通常の[Linuxカーネル](../Page/Linuxカーネル.md "wikilink")にCONFIG_PREEMPT_RTパッチを適用して、[リアルタイムオペレーティングシステム](../Page/リアルタイムオペレーティングシステム.md "wikilink")としての性能を発揮させたものである。入力信号を素早く処理することが可能となっている。そこに着目したUbuntu Studioプロジェクトチームは、リアルタイム・カーネルのパッケージをUbuntuリポジトリに提供してきた。リアルタイム・カーネルの提供は、Ubuntu Studioの最初のリリースである7.04ではなく、バージョン8.04から始まり、続く8.10ではパッチのバグなどの事情により提供が見送られたものの、9.04と9.10にて再び提供が開始された。しかしメンテンナンスの負担などの事情により、10.04以降から再び提供が中断している。

この間、CONFIG_PREEMPT_RTパッチの成果の多くがLinuxカーネルのメインラインにマージされつつあり、リアルタイムパッチを適用しなくても十分なパフォーマンスを得られるようになってきている。\[5\]

これを受けてUbuntu Studioコミュニティでは、Ubuntuの標準カーネルの設定を変更しただけのlowlatencyカーネルの提供を計画している。\[6\]すでに11.04向けlowlatencyカーネルのパッケージが開発者のPPAから提供され、テストが重ねられている。\[7\]

## 日本語環境

ベースシステムはUbuntuと同じもののため、Ubuntuで構築出来る日本語環境はUbuntu Studioでも利用できる。

## デバイス（ハードウェア）の利用

Ubuntu Studioはオープンソース・コミュニティに基づいているため、[デバイスドライバ](../Page/デバイスドライバ.md "wikilink")も有志によって作成される。そのため、発売されたばかりのデバイスは使えない場合が多い。また、それとは別にメーカーが独自にLinux用のドライバを提供しているデバイスもある。

### 音楽編集目的

ハードウェアは特に音楽編集において使用頻度が高い。Ubuntu StudioではMIDIインターフェイスやMIDIコントローラ、オーディオ・インターフェイスを含め、さまざまなサウンドデバイスを使うことができる。

これらサウンドデバイスのうち、[PCIバス接続や](../Page/Peripheral_Component_Interconnect.md "wikilink")[PCI Expressバス接続のサウンドカード](../Page/PCI_Express.md "wikilink")、マザーボード付属のサウンドデバイス、USB接続のオーディオ・インターフェイスは[ALSAがドライバとなり](https://ja.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture "wikilink")、[IEEE 1394](../Page/IEEE_1394.md "wikilink") (FireWire) 接続のオーディオ・インターフェイスはFFADO（旧freeBoB）がドライバとなる。ALSAやFFADOのウェブサイトにおいて、対応しているサウンドデバイスの一覧を公開している。

<table>
<thead>
<tr class="header">
<th><p>接続方法</p></th>
<th><p>特徴</p></th>
<th><p>ドライバ</p></th>
<th><p>JACKのDriver</p></th>
<th><p>対応機種確認</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>USBやPCI/PCI-E</p></td>
<td><p>JACK経由しなくても音声入出力可</p></td>
<td><p>ALSA</p></td>
<td><p>alsa</p></td>
<td><p><a href="http://www.alsa-project.org/main/index.php/Matrix:Main">ALSA SoundCard Matrix</a>@alsa-project.org</p></td>
</tr>
<tr class="even">
<td><p>IEEE 1394 (FireWire)</p></td>
<td><p>JACK経由で音声入出力可</p></td>
<td><p>FFADO</p></td>
<td><p>firewire<br />
（旧freebob）</p></td>
<td><p><a href="http://www.ffado.org/?q=devicesupport/list">Device support database</a>@ffado.org</p></td>
</tr>
</tbody>
</table>

すべての[MIDI](../Page/MIDI.md "wikilink")を扱うソフトウェア/ハードウェアは、[ALSA](https://ja.wikipedia.org/wiki/ALSA "wikilink")シーケンサ機能あるいは[JACKシーケンサ機能にMIDIポートを開くように設定される](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")。ポート間を接続/切断するユーティリティも標準でインストールされている。

### 映像編集目的

映像編集では、デジタルビデオカメラをIEEE 1394 (i.LINK) やUSBで接続し、ソフトウェア経由でデータを保存する、USBで接続した[Webカメラ](../Page/Webカメラ.md "wikilink")からの映像をソフトウェアを使って撮影するといった使い方も可能である。

### 画像編集目的

ペンタブレットに関しては、[The Linux Wacom Project](http://linuxwacom.sourceforge.net/)が株式会社[ワコム](../Page/ワコム.md "wikilink")社のデバイスに対するLinuxドライバを開発しているため、FAVO、Bamboo、Intuosシリーズの多くを利用することができる。また、Waltop社のチップを含む製品（日本国内では株式会社[プリンストンが販売](https://ja.wikipedia.org/wiki/プリンストン_\(企業\) "wikilink")）はWaltop社がLinux用ドライバを提供しているほか、有志によるドライバ（[Wizardpen graphics pad driver](https://launchpad.net/wizardpen)）でも動作可能である。日本では流通していないが、ACE CAD社やAiptek社、Genius, KYE Systems社のペンタブレット用のドライバも提供されている。

## 標準ソフトウェア

Ubuntu Studioは、マルチメディア編集を目的としたソフトウェアを多数、標準でインストールする。

11.04より、標準でインストールされるソフトウェアの選別にユーザの声を反映する取り組みが開始された。\[8\] その結果、報告されなかったフォント編集やDTP関連を中心に、いくつかのソフトウェアが標準構成から外されることとなった。この取り組みは今後も続けられる方針であり、ユーザからの活発な報告を期待されている。\[9\]

以下に、Ubuntu Studio 11.04に標準でインストールされるマルチメディア編集目的のソフトウェアを列挙する。これら以外にも、Ubuntuにおいて標準でインストールされるソフトウェアをインストールすることが可能である。

ソフトウェアの性質上、標準パッケージもバグを含んでいる可能性がある。そのようなパッケージも、有志が[Launchpad](https://ja.wikipedia.org/wiki/Launchpad "wikilink")のPPA (Personal Package Archive) で更新版を配布している場合は、そちらを利用することができる。

### 音楽編集

音楽編集ソフトウェアは、[JACK](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")[サウンドサーバ](https://ja.wikipedia.org/wiki/サウンドサーバ "wikilink")によりその大部分が実装されている。また、標準で各種[LADSPA](https://ja.wikipedia.org/wiki/LADSPA "wikilink") (Linux Audio Developer's Simple Plugin API) プラグインや[DSSI](https://ja.wikipedia.org/wiki/DSSI "wikilink") (Disposable Soft Synth Interface) プラグイン、LV2 (LADSPA Version 2) プラグインを利用することができる。[VSTやVSTiといったWindows向けのプラグインに関しては](https://ja.wikipedia.org/wiki/Virtual_Studio_Technology "wikilink")、[Wine](../Page/Wine.md "wikilink")とFeSTigeを併用することで利用可能な場合がある。

利用者はJACK ControlでJACKサウンドサーバをスタートした後、ArdourといったJACK対応ソフトウェアを起動、Patchageなどの接続ユーティリティを利用してハードウェア／ソフトウェア間を適切に接続することで、音楽処理環境を構築する。

（デジタル・オーディオ・ワークステーション、シーケンサ）

  - [Ardour](https://ja.wikipedia.org/wiki/Ardour "wikilink") - [マスタリング](../Page/マスタリング.md "wikilink")環境にもなる[デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")
  - [MusE](https://ja.wikipedia.org/wiki/MusE "wikilink") - [MIDI](../Page/MIDI.md "wikilink")/[ミュージックシーケンサー](../Page/ミュージックシーケンサー.md "wikilink")
  - Qtractor - MIDI/ミュージックシーケンサー

（ソフトウェアシンセサイザ）

  - Aeolus - オルガンのエミュレーター
  - [Hexter](https://ja.wikipedia.org/wiki/Hexter "wikilink") - [Yamaha DX7をエミュレートしたソフトウェア](../Page/ヤマハ・DXシリーズ.md "wikilink")・シンセサイザ。DSSIプラグインのひとつ
  - [Hydrogen](../Page/Hydrogen_\(ソフトウェア\).md "wikilink") - ソフトウェア・ドラムマシン
  - PHASEX - モジュラーシンセサイザー
  - [Pure Data](../Page/Pure_Data.md "wikilink") - [Max互換のモジュラー](../Page/Max_\(ソフトウェア\).md "wikilink")・オーディオ・シンセシス・アプリケーション
  - Qsynth - サウンドフォントを使うソフトウェア・シンセサイザ[FluidSynth](https://ja.wikipedia.org/wiki/FluidSynth "wikilink")の[QT](../Page/QT.md "wikilink")インターフェース
  - Rakarrack - リアルタイム・ギターエフェクト
  - Yoshimi - ソフトウェア・シンセサイザーでZynAddSubFXのフォーク

（[JACKサウンドサーバ関連ソフトウェア](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")）

  - Qjackctl - 低レイテンシなサウンドサーバJACKのコントローラ
  - JACK Rack - JACKにおいて、各種エフェクト・プラグインの抜き差しを行うインターフェイス
  - JAMin - JACKのオーディオ[マスタリング](../Page/マスタリング.md "wikilink")インターフェイス
  - Meterbridge - JACK用オーディオ・メーター
  - Patchage - JACKを利用するアプリケーションとデバイス間の接続のためのユーティリティ

（デバイス関連のソフトウェア）

  - Echomixer - Echoaudio製サウンドカードのミキサーソフトウェア
  - Envy24control - Envy24 (ice1712) サウンドカードのミキサーソフトウェア
  - FFADO-Mixer - IEEE 1394 (FireWire) 接続サウンドデバイスのためのミキサーソフトウェア
  - HDSPconf - Hammerfall HDSPのALSA用設定ユーティリティ
  - HDSPmixer - RME Hammerfall DSP用のミキサーソフトウェア
  - Rmedigicontrol - RME Digi32/Digi96サウンドカードのミキサーソフトウェア

（プラグイン関連のソフトウェア）

  - Calf Plugin Pack for JACK - JACKのためのCalfプラグインスイート
  - Lv2rack - LV2プラグインのためのホストプログラム
  - Zynjacku - LADSPA/LV2なソフトウェア・シンセサイザーのホストプログラム
  - この他、200を超えるプラグインが利用可能

（その他）

  - [MuseScore (楽譜作成ソフト)](https://ja.wikipedia.org/wiki/MuseScore_\(楽譜作成ソフト\) "wikilink") - [QT](../Page/QT.md "wikilink")インターフェースの楽譜作成ソフトウェア
  - Virtual MIDI keyboard - ソフトウェアMIDIキーボード

（以下は、追加でインストール可能）

  - Aconnectgui - [ALSA](https://ja.wikipedia.org/wiki/ALSA "wikilink")シーケンサ機能における[MIDI](../Page/MIDI.md "wikilink")ポート接続ユーティリティ
  - amSynth - 2つのオシレータをリングモジュレーションするタイプのアナログ・モデリング・シンセサイザ
  - a2jmidid - ALSAシーケンサ機能と[JACKシーケンサ機能をブリッジするソフトウェア](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")
  - Bitmeter - JACKを介してやりとりされているオーディオ信号のモニター
  - Bristol - 代表的な各種シンセサイザをエミュレートしたソフトウェア・シンセサイザ
  - [Audacity](../Page/Audacity.md "wikilink") - 強力な波形編集ソフトウェア。[デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")としても使える
  - Creox c - リアルタイムのソフトウェア・ギターエフェクタ
  - GNU Denemo - 楽譜作成ソフトウェアLylipondの[GTK+](https://ja.wikipedia.org/wiki/GTK+ "wikilink")インターフェース
  - Gtick - GTK+インターフェースの電子メトロノーム
  - JACKEQ - JACKの[イコライザ](../Page/イコライザー_\(音響機器\).md "wikilink")・インターフェイス
  - JACK Timemachine - JACKにおいて録音を行うためのインターフェイス
  - [LMMS](https://ja.wikipedia.org/wiki/LMMS "wikilink") - マルチプラットホームな[デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")。[VST](https://ja.wikipedia.org/wiki/VST "wikilink")の[Windows](https://ja.wikipedia.org/wiki/Windows "wikilink")バイナリを使うこともできる
  - [Mixxx](https://ja.wikipedia.org/wiki/Mixxx "wikilink") - DJソフトウェア。
  - [Rosegarden](../Page/Rosegarden.md "wikilink") - 強力なMIDI編集機能を持つデジタル・オーディオ・ワークステーション
  - [TiMidity++](../Page/TiMidity++.md "wikilink") - MIDIを[PCM](https://ja.wikipedia.org/wiki/PCM "wikilink")に変換するソフトウェア。[MIDI音源](https://ja.wikipedia.org/wiki/MIDI音源 "wikilink")としても使用可能
  - [ZynAddSubFX](http://zynaddsubfx.sourceforge.net/) - 大量の調節可能なパラメータを持つ、高音質かつマルチパートの倍音加算&減算方式ソフトウェア・シンセサイザ

### 動画編集

動画編集ソフトウェアは、動画関連技術に関して権利関係が完全にフリーなソフトウェアを開発するのが難しいこと、映像と音声を扱うためパッケージサイズが巨大になる傾向にあることなどが影響し、標準でインストールされるパッケージは少ない。しかし手動でインストールすることで、多種多様なソフトウェアを利用することができる。

  - [FFmpeg](../Page/FFmpeg.md "wikilink") - さまざまなフォーマットの動画を[デコード](https://ja.wikipedia.org/wiki/デコード "wikilink")/[エンコード](../Page/エンコード.md "wikilink")することができる。操作は[CUI](../Page/キャラクタユーザインタフェース.md "wikilink")
  - Openshot - ノンリニアビデオ編集ソフトウェア。Media Lovin' Toolkitを利用している。
  - SubtitleEditor - 映像データを読み込んで字幕をつけることのできるソフトウェア
  - xjadeo - MTC (MIDI Time Code) や[JACKトランスポートと同期して動作する映像再生ソフトウェア](https://ja.wikipedia.org/wiki/JACK_Audio_Connection_Kit "wikilink")

（以下は、追加でインストール可能）

  - [Avidemux](https://ja.wikipedia.org/wiki/Avidemux "wikilink") - 動画デコード/エンコードができる。[GUI](https://ja.wikipedia.org/wiki/GUI "wikilink")が充実している。
  - Cheese - ウェブカメラから静止画像もしくは映像を取得、保存することができる
  - Cinerella - 映像の[ノンリニア編集](../Page/ノンリニア編集.md "wikilink")/[デジタル合成](../Page/デジタル合成.md "wikilink")ソフトウェア。リポジトリの追加が必要
  - Cinecutie - Cinerellaの[GUIを向上した派生版](https://ja.wikipedia.org/wiki/グラフィカルユーザインタフェース "wikilink")。Cinerellaと同じく、リポジトリの登録が必要
  - dvgrab - デジタルビデオカメラからIEEE 1394 (i.LINK) またはUSBを経由してデータをダウンロードすることができる。操作はCUI
  - Freemix - [VJソフトウェア](../Page/ビデオジョッキー.md "wikilink")。登録した映像をリアルタイムに合成することができる
  - Kdenlive - 映像のノンリニア編集/デジタル合成ソフトウェア。レンダリングには[FFmpeg](../Page/FFmpeg.md "wikilink")を使う。[KDE](../Page/KDE.md "wikilink")アプリケーションのひとつ。
  - Kino - [DVフォーマットに基づいて](../Page/DV_\(ビデオ規格\).md "wikilink")、ビデオを取り込んだり、動画編集をすることができる
  - LiVES - 映像のノンリニア編集/デジタル合成も可能な[VJソフトウェア](../Page/ビデオジョッキー.md "wikilink")
  - luvcview - UVC (USB Video Camera)対応のウェブカメラから静止画像もしくは映像を取得、保存することができる
  - PiTiVi - 映像のノンリニア編集ソフトウェア。[GNOME](../Page/GNOME.md "wikilink")のマルチメディアフレームワークであるGstreamerのgstreamer-nleをバックエンドとして利用している。
  - Stopmotion - ストップモーション・アニメーションを作成することができる
  - Synfig Studio - 2Dアニメーション作成ソフトウェア
  - WinFF - FFmpegの簡易GUI。画面上で操作する事が可能

### 画像編集

欧文を中心に、権利関係がフリーなフォントを多数追加している。[GIMP](../Page/GIMP.md "wikilink")に対しては、ブラシやパレット、グラデーション・テンプレート、[RAW画像](../Page/RAW画像.md "wikilink")現像などの拡張機能が標準でインストールされる。

  - [Blender](../Page/Blender.md "wikilink") - 3Dモデルを作成することができる。シーンを作成することで、映像や動画とすることもできる。
  - [GIMP](../Page/GIMP.md "wikilink") - [画像編集](../Page/画像編集.md "wikilink")/[写真編集](../Page/写真編集.md "wikilink")ソフトウェア。各種プラグインも同梱
  - gimp-ufraw - [GIMP](../Page/GIMP.md "wikilink")で[RAW画像](../Page/RAW画像.md "wikilink")の現像を行うためのプラグイン
  - [Inkscape](../Page/Inkscape.md "wikilink") - [ベクターイメージ](https://ja.wikipedia.org/wiki/ベクターイメージ "wikilink")編集ソフトウェア
  - Shotwell - 写真管理のためのソフトウェア

（デバイス関連のソフトウェア）

  - Xsane - [イメージスキャナ](../Page/イメージスキャナ.md "wikilink")デバイスから画像を取得するためのソフトウェア。[Scanner Access Now Easy](https://ja.wikipedia.org/wiki/Scanner_Access_Now_Easy "wikilink")（SANE）をバックエンドとしている
  - xserver-xorg-input-wacom - ペンタブレットの[Xサーバ](https://ja.wikipedia.org/wiki/Xサーバ "wikilink")用デバイスドライバ。設定ユーティリティであるxsetwacomを含む

（以下は、追加でインストール可能）

  - Agave - カラースキームデザイナー
  - Enblend - 画像合成ソフトウェア
  - [FontForge](../Page/FontForge.md "wikilink") - フォント作成ソフトウェア
  - Fontmatrix - フォント管理ソフトウェア
  - [F-Spot](https://ja.wikipedia.org/wiki/F-Spot "wikilink") - [デジタル写真管理](https://ja.wikipedia.org/wiki/デジタル写真管理 "wikilink")のためのソフトウェア
  - gimp-painter- - [GIMP](../Page/GIMP.md "wikilink")に、筆圧に応じてペンの太さを変更する機能（G-Pen）と、重ね塗りで混色する機能 (MixBrush) を追加したもの。PPAから導入することができる。
  - Hugin panorama creator - 複数枚のイメージデータをパノラマ写真に合成するソフトウェア
  - rawstudio - [デジタルカメラ](../Page/デジタルカメラ.md "wikilink")の[RAW画像](../Page/RAW画像.md "wikilink")を[現像](../Page/現像.md "wikilink")するソフトウェア
  - [Scribus](../Page/Scribus.md "wikilink") - [DTP](../Page/DTP.md "wikilink")ソフトウェア

## 関連項目

  - [Ubuntu](../Page/Ubuntu.md "wikilink") - [Debian](../Page/Debian.md "wikilink")から派生したLinuxディストリビューション。[カノニカル](https://ja.wikipedia.org/wiki/カノニカル "wikilink")に支援を受けたオープンソースコミュニティが開発を行っている
  - [64 Studio](https://ja.wikipedia.org/wiki/64_Studio "wikilink") - Debianをベースとする、マルチメディアに特化したディストリビューション

## 脚注

## 外部リンク

  - [Ubuntu Studio homepage](http://ubuntustudio.org/)
  - [Ubuntu Studio Wiki @ Ubuntu.com](https://wiki.ubuntu.com/UbuntuStudio)
  - [UbuntuStudio/Applications - Community Ubuntu Documentation](https://help.ubuntu.com/community/UbuntuStudio/Applications)
  - [Ubuntu Studio に関するTips](https://wiki.ubuntulinux.jp/UbuntuStudioTips) - Ubuntu 日本チームのWiki。インストール方法解説や各種Tips。
  - [Medibuntu](http://www.medibuntu.org/)  - Ubuntuのリポジトリには含まれない、権利関係がフリーではないパッケージを提供
  - [Real-Time Linux Wiki](https://rt.wiki.kernel.org/)  - RTカーネルのためのパッチを開発しているCONFIG_PREEMPT_RT Communityのウェブサイト

[Category:Ubuntu派生ディストリビューション](https://ja.wikipedia.org/wiki/Category:Ubuntu派生ディストリビューション "wikilink") [Category:オープンソースソフトウェア](https://ja.wikipedia.org/wiki/Category:オープンソースソフトウェア "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.