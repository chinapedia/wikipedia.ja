> この記事は[Rockbox](https://ja.wikipedia.org/wiki/Rockbox)から翻訳されています。


**Rockbox**は、[デジタルオーディオプレーヤー](../Page/デジタルオーディオプレーヤー.md "wikilink")に搭載された[ファームウェア](../Page/ファームウェア.md "wikilink")を置き換える[フリーソフト](https://ja.wikipedia.org/wiki/フリーソフト "wikilink")であり、拡張性の乏しいプレーヤーに様々な機能を追加するための[プラグイン](../Page/プラグイン.md "wikilink")機能を（多くの場合、元のファームウェアを取り除かないで）提供する。[オープンソース](../Page/オープンソース.md "wikilink")のファームウェアであり、誰でも開発、配布が自由である。拡張機能には[PDA機能](../Page/携帯情報端末.md "wikilink")、[アプリケーション](../Page/アプリケーションソフトウェア.md "wikilink")、[ユーティリティ](https://ja.wikipedia.org/wiki/ユーティリティソフトウェア "wikilink")、[ゲーム](../Page/ゲーム.md "wikilink")などがある。また、2000年中頃にリリースされたプレーヤーにも[ビデオ](../Page/ビデオ.md "wikilink")の再生機能を加える。また、視覚障害をもつユーザのための声で操作できる[ユーザインタフェース](../Page/ユーザインタフェース.md "wikilink")も用意されている。

Rockboxはハードウェア能力が非常に異なっている様々なポータブルオーディオデバイス上で動くものであるため、1ビットのキャラクタセルベースの[ディスプレイ](https://ja.wikipedia.org/wiki/ディスプレイ "wikilink")をもつ早期の[Archos](https://ja.wikipedia.org/wiki/Archos "wikilink")プレーヤーから、近代的な高画質のディスプレイ/[デジタル](../Page/デジタル.md "wikilink")の光学[オーディオ機器](https://ja.wikipedia.org/wiki/オーディオ機器 "wikilink")/高度な録音能力をもっているプレーヤーまで対応している。多くの場合、[フラッシュメモリ](../Page/フラッシュメモリ.md "wikilink")から実行されるよりも、ハードディスクからRockboxか標準のファームウェアのどちらかから読み込み可能なサポートされているデバイスのフラッシュに最小限の[ブート](../Page/ブート.md "wikilink")ローダーがインストールされる 。また、一部の機器ではフラッシュメモリへのインストールもできる。

## 開発

Rockboxプロジェクトは2001年の後半に、初期の[Archos](https://ja.wikipedia.org/wiki/Archos "wikilink")シリーズのハードディスク内蔵型[MP3](../Page/MP3.md "wikilink")プレイヤーと、フラッシュメモリ型のOndioを含んだ録音機能つきモデルを対象に行われた。Rockbox開発は、ユーザーインターフェイスやデバイスの取り扱い方法に不満をもったことにより開発された。これらの機器の処理能力は限られており、音楽再生はMP3デコードチップ（MAS）で行っていたため、Rockboxは音楽の再生品質を変えることはできなかったが、その代わり、Rockboxは改良されたユーザーインターフェイスを提供し、工場出荷時のファームウェアに無い機能をプラグインで導入可能にした。Rockboxは製品に搭載されたフラッシュメモリの起動領域を書き換え、元のファームウェアとそっくりそのまま入れ替えてしまうことができた。

Rockboxにはより新しい製品に対応したバージョンも用意されている。こちらではソフトウェアデコードにより演奏しており、既にArchos版で実装している機能に加えて、オリジナルのファームウェアが対応しないオーディオフォーマットの演奏が潜在的に可能となっている。専用のブートローダーで製品が起動後、Rockboxはハードディスクから立ち上がる。つまり、Rockboxをアップグレードするのにユーザーが必要なことは、ハードディスクにファイルをコピーして再起動することだけである。ブートローダーの差し替えのためにはファームウェアの書き換えが必要になるが、製品によっては差し替え不要である。

2004年の後半に始まった初めてのこれらの移植は[iriverが製造したモトローラー製の](../Page/アイリバー.md "wikilink")[ColdFireプロセッサーを使ったデバイス](https://ja.wikipedia.org/wiki/Coldfire "wikilink")、つまりハードディスク・プレイヤーであるiriver H100 シリーズ(H110/H120/H140)だった。およそ1年後に、iriver H300 シリーズへの移植は機能的になり、同じような機能を提供するようになった。

  - 2005年後半に、[Apple製の](../Page/アップル_\(企業\).md "wikilink")[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")にRockboxの移植が始まった。
  - 2006年の1年間は、[Cowon](../Page/Cowon.md "wikilink") [iAUDIO X5シリーズと同様に](https://ja.wikipedia.org/wiki/Cowon#デジタルオーディオプレーヤー "wikilink")、Rockboxを様々なiPod([iPod photo](https://ja.wikipedia.org/wiki/iPod_classic "wikilink"), [iPod nano](https://ja.wikipedia.org/wiki/iPod_nano "wikilink"), iPod第4世代, [iPod mini](https://ja.wikipedia.org/wiki/iPod_mini "wikilink"), iPod第5世代)で利用可能にした。
  - 2007年2月には、iriver H10や[東芝](../Page/東芝.md "wikilink")の[gigabeat](https://ja.wikipedia.org/wiki/gigabeat "wikilink") FとXシリーズへの移植が利用可能になった。
  - 2007年3月5日には、Cowon [iAUDIO M5への移植が機能的になった](https://ja.wikipedia.org/wiki/Cowon#デジタルオーディオプレーヤー "wikilink")。
  - 2007年3月11日には、[SanDisk](../Page/サンディスク.md "wikilink") [Sansa](https://ja.wikipedia.org/wiki/:en:SanDisk_Sansa "wikilink") e200シリーズがRockboxの次のラインアップに追加された。
  - 2007年5月23日には、iPod 5.5世代 80 GBモデルに対応し、iPod videoのラインアップが完結した。
  - 2007年7月27日には、iPod 1G と 2Gの最初のサポートが追加された。
  - 2007年9月23日には、Sansa c200シリーズがラインアップに追加された。
  - 2008年3月18日には、[オリンパス](https://ja.wikipedia.org/wiki/オリンパス "wikilink")の[m:robe](https://ja.wikipedia.org/wiki/:en:Olympus_m:robe "wikilink") MR-100がラインナップに追加された。
  - 2008年3月23日には、Cowon iAudio M3がラインナップに追加された。
  - 2008年5月3日には、東芝 gigabeat Sの利用が可能となった。
  - 2009年3月10日には、オリンパスのm:robe MR-500iの利用が可能となった。
  - 2010年には[android](https://ja.wikipedia.org/wiki/android "wikilink")への移植が始まる。

現在、Rockboxはmpegplayerプラグインを使用し、[MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")再生に対応。\[1\]

現在のところ全てのRockboxはメーカーの手助けをほとんど借りることなく[リバース・エンジニアリング](https://ja.wikipedia.org/wiki/リバース・エンジニアリング "wikilink")のみによって移植を完了してきた。しかし、フリーソフトウェアではあるが、開発者、支援者は移植されたRockboxにメーカーの公式サポート、あるいは新製品への移植に非公式な手助けが得られることを望んでいる。今でも少数の企業がRockboxに興味を示すに留まっており、開発プロジェクトへの公式なコード提供や、製品への組込を行う企業は皆無である。Sansaへの移植はメーカーの要請により始められ、開発チームにサンプル品が提供されている。\[2\]また、Sansa E200 v2などのSoCを開発している[AustriaMicrosystemsも](https://ja.wikipedia.org/wiki/:en:ams_AG "wikilink")[データシート](https://ja.wikipedia.org/wiki/データシート "wikilink")を提供するなど開発に協力している。\[3\]また、ロシアのフォーラムで有志がHiFiMAN HM-801にrockboxの移植を行ってもらおうと呼びかけ、賛同者がrockboxの開発者にHM-801を提供し、移植されたという例もある。

Rockboxは継続的に開発されており、ソースコードの毎変更ごとの[SVNビルドがリリースされている](../Page/Apache_Subversion.md "wikilink")。\[4\]

## カスタマイズ

Rockboxのインターフェイスは特有のプラットフォームごとの制限に左右されるが、様々な方法でカスタマイズ出来る。フォントや表面と背景の色は追加したり選ぶことが出来る。その一方、メニューや再生中の画面のテーマを作るのには簡単なマークアップ言語が使われている。これらのテーマとして、背景や他の画像（アイコンのような物とか）があげられ、加えて、様々な拡張子、[ID3タグ](https://ja.wikipedia.org/wiki/ID3タグ "wikilink")、ファイルの進捗状況、時間やシステムの情報があげられる。2007年11月11日の時点で、アルバムアートの表示が正式にサポートされた。2011年2月27日にはmp3のID3(v2)タグに埋め込まれた[JPEG](../Page/JPEG.md "wikilink")が正式にサポートされた。Rockboxは原則的にファイルツリーが基本のプレイヤーであり、そしてフォルダ構造による操作が出来る。（フォルダはプレイヤーにドラッグ・アンド・ドロップすることができる。）プレーヤー内で切り取り・貼り付けや削除をすることもできる。また、最近のバージョンには、プレイヤーにファイルのID3タグからの情報を集めることを可能にしたデーターベース機能がある。ユーザーはその結果ファイル構造に関係なく、このデーターベースを用いることでファイルを操作することが出来る。

## 特徴

### コーデック

ソフトウェアでデコードするプラットフォーム（Archos以外）では13つの[非可逆コーデックと](../Page/非可逆圧縮.md "wikilink")6つの[ロスレスコーデックと](../Page/可逆圧縮.md "wikilink")4つの[非圧縮](https://ja.wikipedia.org/wiki/非圧縮 "wikilink")コーデックと14つの[チップチューン](../Page/チップチューン.md "wikilink")フォーマットの再生をサポートしている。また、[DRM機構のファイルはRockboxにおいて再生できない](https://ja.wikipedia.org/wiki/デジタル著作権管理 "wikilink")。Rockboxはオープンソースのプロジェクトなので、この機能は意図的に決して実装されることはない。

#### 非可逆コーデック

  - [AC3](https://ja.wikipedia.org/wiki/Dolby_Digital "wikilink")([raw](https://ja.wikipedia.org/wiki/raw "wikilink")もしくは[RealMedia](https://ja.wikipedia.org/wiki/RealMedia "wikilink")コンテナ)
  - [ADX](../Page/適応的差分パルス符号変調.md "wikilink")
  - [Advanced Audio Coding](../Page/AAC.md "wikilink")(AAC-LC/HEv1/HEv2)([MP4](https://ja.wikipedia.org/wiki/MP4 "wikilink")コンテナもしくはRealMediaコンテナ)
  - MPEG audio layers I-III (MP3/MP2/MP1)
  - [Musepack](../Page/Musepack.md "wikilink")
  - [Ogg Vorbis](https://ja.wikipedia.org/wiki/Vorbis "wikilink")
  - [ATRAC](https://ja.wikipedia.org/wiki/ATRAC "wikilink")3\[5\]([OpenMG](https://ja.wikipedia.org/wiki/OpenMG "wikilink")コンテナもしくはRealMediaコンテナ)
  - [Cook Codec](https://ja.wikipedia.org/wiki/Cook_Codec "wikilink")
  - [Speex](../Page/Speex.md "wikilink")
  - [Dialogic telephony type](https://ja.wikipedia.org/wiki/Dialogic_telephony_type "wikilink")
  - [Windows Media Audio](https://ja.wikipedia.org/wiki/Windows_Media_Audio "wikilink")
  - Windows Media Audio Professional
  - [Opus](https://ja.wikipedia.org/wiki/CELT "wikilink")

#### 可逆コーデック

  - [FLAC](../Page/FLAC.md "wikilink")
  - [WavPack](https://ja.wikipedia.org/wiki/WavPack "wikilink")
  - [Shorten](https://ja.wikipedia.org/wiki/Shorten "wikilink")
  - [Apple Lossless](https://ja.wikipedia.org/wiki/Apple_Lossless "wikilink")
  - [Monkey's Audio](../Page/Monkey's_Audio.md "wikilink")\[6\]
  - [TTA](https://ja.wikipedia.org/wiki/TTA "wikilink")\[7\]

#### 非圧縮コーデック

  - [PCM](../Page/パルス符号変調.md "wikilink")
      - [WAV](https://ja.wikipedia.org/wiki/WAV "wikilink")
      - [AIFF](https://ja.wikipedia.org/wiki/AIFF "wikilink")
      - [Sunオーディオファイル](../Page/Sunオーディオファイル.md "wikilink")\[8\]
      - Wave64

#### チップチューンフォーマット

  - [Atari Sound Format](https://ja.wikipedia.org/wiki/Atari_Sound_Format "wikilink")
  - [Synthetic music Mobile Application Format](../Page/SMAF.md "wikilink")\[9\]
  - [Game Boy Sound Format](https://ja.wikipedia.org/wiki/:en:Game_Boy_Sound_System "wikilink")
  - [AY Sound Chip Music](https://ja.wikipedia.org/wiki/AY_Sound_Chip_Music "wikilink")
  - [Hudson Entertainment System Sound Format](https://ja.wikipedia.org/wiki/Hudson_Entertainment_System_Sound_Format "wikilink")
  - [MSX Konami Sound System](https://ja.wikipedia.org/wiki/MSX_Konami_Sound_System "wikilink")
  - [SMS/GG/CV Sound Format](https://ja.wikipedia.org/wiki/SMS/GG/CV_Sound_Format "wikilink")
  - [Video Game Music Format](https://ja.wikipedia.org/wiki/Video_Game_Music_Format "wikilink")
  - [Gzipped Video Game Music Format](https://ja.wikipedia.org/wiki/Gzipped_Video_Game_Music_Format "wikilink")
  - [MOD](../Page/MOD_\(ファイルフォーマット\).md "wikilink")
  - [NES Sound Format](https://ja.wikipedia.org/wiki/:en:NES_Sound_Format "wikilink")
  - [Atari SAP](https://ja.wikipedia.org/wiki/Atari_SAP "wikilink")
  - [Sound Interface Device](https://ja.wikipedia.org/wiki/SID音源 "wikilink")
  - [SPC700](../Page/SPU.md "wikilink")

### 特徴

オーディオファイルを再生したり録音したりする能力の傍ら、Rockboxは他のファームウェアが実装していない再生機能を提供している。

以下に掲載されているのはこれらの機能の一部である。

  - [ギャップレス再生](https://ja.wikipedia.org/wiki/ギャップレス再生 "wikilink") (全ての非圧縮、可逆コーデックとVorbis、Speex、Opus、Musepack、MP3([LAME](https://ja.wikipedia.org/wiki/LAME "wikilink")方式および[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")方式)、AAC(iTunes方式および[Nero Digital方式](https://ja.wikipedia.org/wiki/Nero_Digital "wikilink"))に対応)
  - リプレイゲイン\[10\]
  - 5バンド・パラメトリックイコライザ\[11\]
  - クロスフィード
  - OTF ("on the fly") プレイリスト
  - True randomシャッフル (fresh randomly shuffled list every time)
  - カスタムUIテーマ
  - ステレオでの以下の形式への録音: WAV/AIFF/WavPack （ロスレス）/MP3\[12\] (デバイスのサポート)
  - [FMラジオとその録音](https://ja.wikipedia.org/wiki/ラジオ#FM放送（超短波放送） "wikilink") （デバイスのサポート）
  - 遠隔操作 （デバイスのサポート）
  - Digital [SPDIF](https://ja.wikipedia.org/wiki/SPDIF "wikilink")の入出力 （デバイスのサポート）
  - [Last.fm](../Page/Last.fm.md "wikilink")の対応 (ただし、[内部時計が無ければ対応しない](https://ja.wikipedia.org/wiki/Real-time_clock "wikilink"))
  - Cue sheetの対応
  - メニュー選択のバーの色と外観は変更可能
  - アルバムアート（MP3ID3v2の埋め込みタグ対応） \[13\]
  - マルチフォントのサポート
  - 歌詞を音声にあわせて表示

### プラグイン

Rockbox は、音楽を聞く以外の機能として、プラグインという形で様々なアプリケーションが Rockbox の開発者によって作成されている。その一例として、以下のものがある。（完全なプラグインのリストは [プラグインのリスト](http://www.rockbox.org/wiki/PluginIndex) を参照のこと）

  - JPEG、[PNG](../Page/Portable_Network_Graphics.md "wikilink")、[BMP](https://ja.wikipedia.org/wiki/BMP "wikilink")ビューア
  - Rockboy [GameBoy](../Page/ゲームボーイ.md "wikilink") エミュレータ （[Gnuboy](https://ja.wikipedia.org/wiki/Gnuboy "wikilink")のポート）\[14\]
  - ZXBox [ZX Spectrum](../Page/ZX_Spectrum.md "wikilink") エミュレータ （Spectemuのポート）\[15\]
  - *[Doom](https://ja.wikipedia.org/wiki/Doom_\(video_game\) "wikilink")* （[PrBoom](https://ja.wikipedia.org/wiki/PrBoom "wikilink")エンジンのポート）
  - WAV から MP3 へのエンコーダ
  - WAV から WavPack へのエンコーダ
  - MPEGビデオプレーヤー \[16\]
  - 様々なゲーム（[数独](https://ja.wikipedia.org/wiki/数独 "wikilink"), [ソリティア](../Page/ソリティア.md "wikilink"), [マインスイーパ](https://ja.wikipedia.org/wiki/マインスイーパ "wikilink"), [テトリス](https://ja.wikipedia.org/wiki/テトリス "wikilink"), [リバーシ](https://ja.wikipedia.org/wiki/リバーシ "wikilink"), pong等40種以上）
  - MIDIプレーヤー。ある程度の処理能力があるプレイヤーではリアルタイムで再生可能。再生には外部の楽器セットファイルが必要であり、Rockboxのページからダウンロードできる。CPUが追いつかなくなると、音飛びが生じる。
  - 電卓（関数電卓機能付）
  - カレンダー
  - ペイント
  - メトロノーム
  - テキストビューア/エディタ
  - ストップウォッチ

### サポートしない機能

Rockboxには外部の会社やプラットフォームのサポート不足のために、まだ実装されていない機能がいくつかある。

  - [FireWire](https://ja.wikipedia.org/wiki/FireWire "wikilink")
  - DRM (故意に未実装)\[17\]
  - [FAT32](https://ja.wikipedia.org/wiki/FAT32 "wikilink")以外のファイルシステムの実装 (故意に未実装)\[18\]

## アーキテクチャ

Rockboxは[フラットメモリモデル](https://ja.wikipedia.org/wiki/フラットメモリモデル "wikilink") （これが [メモリ管理装置](https://ja.wikipedia.org/wiki/メモリ管理装置 "wikilink")なしで様々なプラットホーム上で動かすことを可能にしている。）と シングル [プロセス](../Page/プロセス.md "wikilink")を用いた、単純なカーネルで動いている\[19\]。 貧弱な[スレッド](../Page/スレッド_\(コンピュータ\).md "wikilink") は、"オーディオ・スレッドを優先させる [スケジューラ](https://ja.wikipedia.org/wiki/スケジューラ "wikilink")"に制御を返す"協調マルチスレッディング"で動く。つまり、[プリエンプション](https://ja.wikipedia.org/wiki/プリエンプション "wikilink")（OSが優先順位の高いタスクに有利になるように、現在のタスクを停止したり、先取りする能力のこと）を行うには[割り込みを利用するしかない](../Page/割り込み_\(コンピュータ\).md "wikilink")。OSやプラグインはC言語で書かれていて、繊細なコードを実行することにつけ加え、デバイスやプラットフォーム固有のコードの為にアセンブリ言語が用いられている。この単純で軽いアーキテクチャのおかげで、Rockboxは、1〜64MBまで変動するメモリや、12〜300MHzまで変動するCPUといった、様々な機器で動かすことが可能になっている。Rockboxはまた、マルチコア・システムや非対称型マルチプロセッサ・システムへの限定的なサポートをしている。

## サポートしているデバイス

[thumb](https://ja.wikipedia.org/wiki/ファイル:iPod_mini_rockbox.jpg "wikilink") Archosデバイスのみ公式にサポートされると宣告されている。以下は少なくとも実質的に動作する(Rockbox wiki Device Chartで「サポートされる」か「使用可能である」として、記載されている)デバイスのリストであると考えるべきである。詳細に関しては[Rockbox Device Chart](http://www.rockbox.org/wiki/DeviceChart)を参照。

### 安定版

#### Archos

  - Archos Jukebox シリーズ
      - Jukebox 6000
      - Jukebox Player/Studio
      - Jukebox Recorder
  - FM Recorder
  - Recorder v2
  - Ondio FM
  - Ondio SP

#### Cowon

  - iAUDIO M3、M3L
  - iAUDIO M5、M5L
  - iAUDIO X5、X5L
  - iAUDIO X5V

#### Apple

  - iPod 第1世代
  - iPod 第2世代
  - iPod 第3世代
  - iPod 第4世代 (グレイスケール)※ロット(搭載CPUのリビジョン?)によって公式ビルドではunstableなものがある模様。
  - iPod 第4世代 (Color/Photo)
  - iPod 第5世代/第5.5世代 (Video)
  - iPod mini 第1世代
  - iPod mini 第2世代
  - iPod nano 第1世代

#### iriver

  - iriver H10 (H10 5/6/20GB)
  - iriver H100 (H100/H110/H115/H120/H140, aka iHP-100/110/115/120/140)
  - iriver H300 (H320/H340)

#### [MPIO](../Page/Mpio.md "wikilink")

  - MPIO HD300

#### [Packard Bell](https://ja.wikipedia.org/wiki/Packard_Bell "wikilink")

  - Vibe 500

#### [SanDisk](../Page/サンディスク.md "wikilink")

  - Sansa e200 シリーズ (v1/v2)
  - Sansa e200r シリーズ
  - Sansa c200 シリーズ (v1/v2)
  - Sansa Fuze シリーズ (v1/v2)
  - Sansa Clip シリーズ (v1/v2/Clip+)
  - Sansa Clip Zip

#### Toshiba

  - [Gigabeat Fシリーズ](https://ja.wikipedia.org/wiki/gigabeat#Fシリーズ "wikilink") (F10/F11/F20/F21/F30/F31/F40/F41/F60)
  - [Gigabeat Xシリーズ](https://ja.wikipedia.org/wiki/gigabeat#Xシリーズ "wikilink")

### 不安定版

#### Apple

  - iPod nano 第2世代

#### Cowon

  - COWON D2

#### [HiFi E.T](https://ja.wikipedia.org/wiki/HiFi_E.T "wikilink")

  - MA9

#### [HiFiMAN](https://ja.wikipedia.org/wiki/HiFiMAN "wikilink")

  - HM-60x
  - HM-801

#### MPIO

  - MPIO HD200

#### Olympus

  - M:Robe 100
  - M:Robe 500

#### [PHILIPS](../Page/フィリップス.md "wikilink")

  - PhilipsGoGear HDD16x0
  - GoGear HDD63x0
  - GoGear SA9x00

#### [Samsung](../Page/サムスン電子.md "wikilink")

  - YH-820/YH-920/YH-925
  - YP-R0

#### SanDisk

  - Sansa Fuze+

#### Toshiba

  - [Gigabeat Sシリーズ](https://ja.wikipedia.org/wiki/gigabeat#Sシリーズ "wikilink")

## 開発中の移植版

Rockboxは様々なデジタルオーディオプレーヤーを使う人たちによって開発されている。自分たちが使っているプレイヤーへRockboxを移植することに興味を持っている人であれば開発に加わることは常に歓迎である。\[[http://www.rockbox.org/twiki/bin/view/Main/NewPort\]原理的には、プレイヤーのCPUに](http://www.rockbox.org/twiki/bin/view/Main/NewPort%5D原理的には、プレイヤーのCPUに)[GCCが対応してさえいれば移植可能である](../Page/GNUコンパイラコレクション.md "wikilink")。Rockboxの移植版がすでに存在するプレイヤーと共通の部品を持っていれば、開発は非常に容易になる。公開されている仕様書がない部品で作られていたり、ハッシュチェックや暗号化でファームウェアを積極的に保護していれば、移植は難しくなる。

### Archos

  - AV300

### Cowon

  - iAUDIO 7

### [Creative](https://ja.wikipedia.org/wiki/クリエイティブテクノロジー "wikilink")

  - [Zen Vision:M](../Page/Creative_Zen.md "wikilink")
  - Zen Vision

### [Onda](https://ja.wikipedia.org/wiki/Onda "wikilink")

  - VX747
  - VX767
  - VX747+
  - VX777

### Samsung

  - YP-S3

### iriver

  - iFP-790

### [Meizu](https://ja.wikipedia.org/wiki/Meizu "wikilink")

  - M6SL
  - M6SP
  - M3

### [Tatung](https://ja.wikipedia.org/wiki/Tatung "wikilink")

  - Elio TPJ-1022

### Apple

  - iPod classic

### SanDisk

  - Sansa m200 (v1/v4)
  - Sansa c100
  - Sansa View
  - Sansa Connect

### [Logik](https://ja.wikipedia.org/wiki/Logik "wikilink")

  - DAX

### [Lyre project](https://ja.wikipedia.org/wiki/Lyre_project "wikilink")

  - Lyre proto 1
  - Mini2440

### ソフトウェア

#### Google

  - [Android](../Page/Android.md "wikilink")

#### Nokia

  - N8xx
  - N900

#### Pandora

  - Pandora

## ギャラリー

Image:Rockbox-ss-h120-llamabeta.png|iriver H120/iPod 4G, LlamaBetaテーマ Image:Rockbox-Mintytheme.png|iPod Video, Mintyテーマ Image:Rockbox-ss-ipod5g-ipodvision.png|iPod Video, iPodVisionテーマ Image:Rockbox-zenX5.png|iAudio X5, zenX5テーマ Image:Rockbox-BlackGlassMGr.png|iPod Nano, Black Glass MGrテーマ Image:Rockbox-tango.png|iPod Nano, Tangoテーマ Image:Rockbox-DGT.jpg|iriver H320/iPod Photo, DGTテーマ Image:Rockbox-archos-jensarnold.png|Archos Jukebox Recorder/FM Recorder/Ondio, WPS by Jens Arnold Image:Dump_070126-001244_copy.jpg|Toshiba Gigabeat, beatMP WPS by Kirill Lanchev

## 関連項目

  - [iPodLinux](https://ja.wikipedia.org/wiki/iPodLinux "wikilink")

## 参照

## 外部リンク

  - [The Rockbox Project](http://www.rockbox.org/)
  - [LWN.net: Waiting for Rockbox 3.0](http://lwn.net/Articles/183931)

[Category:ファームウェア](https://ja.wikipedia.org/wiki/Category:ファームウェア "wikilink") [Category:音響機器](https://ja.wikipedia.org/wiki/Category:音響機器 "wikilink") [Category:アフターマーケットファームウェア](https://ja.wikipedia.org/wiki/Category:アフターマーケットファームウェア "wikilink")

1.
2.  [1](http://daniel.haxx.se/rockbox-sandisk-connection.html)
3.  [daniel.haxx.se » AMS Replied with the AS3525 Data Sheet](http://daniel.haxx.se/blog/2007/11/29/ams-replied-with-the-as3525-data-sheet/)
4.  ただし、ソースツリーのアクセスは、[Git](../Page/Git.md "wikilink") (正確には、git-svn) を用いることが推奨されている。
5.  3.6 以降でサポート。
6.  Monkey's Audioの対応は初期の段階であり、ほとんどデバイスにおいてリアルタイムに再生できるのは低圧縮の設定のみである。
7.  3.6 以降でサポート。ただし、一部の機種ではリアルタイムに再生することはできない。
8.  3.6 以降でサポート。
9.  3.6 以降でサポート。ただし、音源が [PCM](../Page/パルス符号変調.md "wikilink") または [ADPCM](../Page/適応的差分パルス符号変調.md "wikilink") であるものだけが再生可能。MIDI 音源は非対応。
10. ソフトウェアデコードのターゲットのみ
11.
12. MP3 と WavPack と AIFF はArchos以外で利用可能。マルチサンプルレートとビットレートは利用可能。（ただし、ハードウェアに依存）.
13. ある程度制限があります。詳細はRockbox ウィキ [2](http://www.rockbox.org/wiki/AlbumArt) をご覧ください。
14. RockboyはゲームボーイとゲームボーイカラーのROMに対応している。
15. ZXBoxはZX Spectrum 48をエミュレートする。Spectemuの元サイト: [3](http://www.inf.bme.hu/~mszeredi/spectemu/)
16. mpegplayerプラグインは [MPEG-1](../Page/MPEG-1.md "wikilink") もしくは [MPEG-2](../Page/MPEG-2.md "wikilink") 形式のビデオで[MPEG](https://ja.wikipedia.org/wiki/MPEG "wikilink")オーディオ （レイヤーII/III）（音声部はMP2とMP3にのみ対応）を多重化した.mpgファイル形式に対応。ハードウェアによるフレームレートとビットレートの制約はない。ファイルはおのおのの機器に応じた解像度である必要がある。早送りと巻き戻しにも対応。[4](http://www.rockbox.org/wiki/PluginMpegplayer)
17. [NoDo](http://www.rockbox.org/wiki/NoDo)
18.
19. [Rockboxのカーネルについて](http://www.rockbox.org/wiki/RockboxKernel)