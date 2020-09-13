> この記事は[General MIDI](https://ja.wikipedia.org/wiki/General_MIDI)から翻訳されています。


**General MIDI**（ジェネラル・ミディ）とは、基本的な音色マップと[コントロールチェンジ](../Page/コントロールチェンジ.md "wikilink")などを規定した[MIDI](../Page/MIDI.md "wikilink")の統一規格である。略称は**GM**。

## 概要

GMが制定される前、MIDIの音色マップやコントロールチェンジは[MIDI音源のメーカーや機種毎に違っており](../Page/音源モジュール.md "wikilink")、他の製品とは基本的に互換性が無かった。例えば、PC（Program Change）の1番にはA社のMIDI音源ではピアノの音色が割り当ててあるが、B社の製品では弦楽器が割り当てられている、ということが多々あった。これにより、違うメーカーのMIDI音源で制作した曲データは、別のMIDI音源では作者の意図しない演奏をすることがあるという問題があった。こういった互換性の問題を解決するために、[1991年](../Page/1991年.md "wikilink")に日本MIDI評議会（現在の[音楽電子事業協会](https://ja.wikipedia.org/wiki/音楽電子事業協会 "wikilink")）と[MIDI Manufacturers Association](https://ja.wikipedia.org/wiki/MIDI_Manufacturers_Association "wikilink") (MMA) によってGMが制定された。

GMには、GMマップと呼ばれる音色マップ、コントロールチェンジ、[RPN](https://ja.wikipedia.org/wiki/RPN "wikilink")やGMシステムエクスクルーシブなどが決められており、[同時発音数](https://ja.wikipedia.org/wiki/同時発音数 "wikilink")についても記述がある。

GM以外の規格としては、[ローランド](../Page/ローランド.md "wikilink")が推進している[GSや](../Page/GSフォーマット.md "wikilink")[ヤマハ](../Page/ヤマハ.md "wikilink")が推進している[XG](../Page/XGフォーマット.md "wikilink")、そしてXGフォーマットの簡易版 XGLite などがある。ほとんどの規格がGMを拡張した規格であるため、GMからみれば上位互換の規格である。

現在はGMの拡張規格であるGM2 (General MIDI 2) がある。しかし、演奏データのMIDIではなく[MP3](../Page/MP3.md "wikilink")など「音」そのものの配信が手軽にできるようになったこと、MIDIからオーディオへの制作環境の変化、専用音源としてGM規格と互換性のない[SoundFont](../Page/SoundFont.md "wikilink")や[ソフトウェア・シンセサイザー](../Page/ソフトウェア・シンセサイザー.md "wikilink")の普及、GM1における[SC-55mkIIのような標準音源がないこと](../Page/ローランド・SCシリーズ.md "wikilink")、GM2で規定されている項目が、GSやXGより少なく、GS/XGのほうが表現豊かな演奏データを作成できるという等の理由から、。

## 必須最低要件

GM1互換機器は、以下の要件を満たさなければならない。

  - 同時発音数24（メロディー16、パーカッション8を含む）
  - ベロシティー（音の強さ/音の速さ）の命令に対応。
  - 16チャンネル使用可能（うち、チャンネル10番はパーカッション用に予約）
  - 各チャンネルでの同時発音対応。

## パラメータ

GM対応機器は、プログラムチェンジとコントロールチェンジ・イベントの為に、以下の規定にも従わなければならない。

### Program Change events

この表は、楽器音とProgram Change番号の対応を示す。

### Melodic sounds

| No.                  | [HEX](https://ja.wikipedia.org/wiki/16進法 "wikilink") | English                 | 日本語                                                                                  |
| -------------------- | ---------------------------------------------------- | ----------------------- | ------------------------------------------------------------------------------------ |
| Piano                |                                                      |                         |                                                                                      |
| 1                    | 00                                                   | Acoustic Piano          | [アコースティックピアノ](../Page/ピアノ.md "wikilink")                                             |
| 2                    | 01                                                   | Bright Piano            | [ブライトピアノ](../Page/ピアノ.md "wikilink")                                                 |
| 3                    | 02                                                   | Electric Grand Piano    | [エレクトリック・グランドピアノ](https://ja.wikipedia.org/wiki/エレクトリック・グランドピアノ "wikilink")          |
| 4                    | 03                                                   | Honky-tonk Piano        | [ホンキートンクピアノ](https://ja.wikipedia.org/wiki/ホンキートンクピアノ "wikilink")                    |
| 5                    | 04                                                   | Electric Piano          | [エレクトリックピアノ](../Page/エレクトリックピアノ.md "wikilink")                                       |
| 6                    | 05                                                   | Electric Piano 2        | FMエレクトリックピアノ                                                                         |
| 7                    | 06                                                   | Harpsichord             | [ハープシコード](../Page/チェンバロ.md "wikilink")                                               |
| 8                    | 07                                                   | Clavi                   | [クラビネット](../Page/クラビネット.md "wikilink")                                               |
| Chromatic Percussion |                                                      |                         |                                                                                      |
| 9                    | 08                                                   | Celesta                 | [チェレスタ](../Page/チェレスタ.md "wikilink")                                                 |
| 10                   | 09                                                   | Glockenspiel            | [グロッケンシュピール](../Page/グロッケンシュピール.md "wikilink")                                       |
| 11                   | 0A                                                   | Musical box             | [オルゴール](../Page/オルゴール.md "wikilink")                                                 |
| 12                   | 0B                                                   | Vibraphone              | [ヴィブラフォン](../Page/ヴィブラフォン.md "wikilink")                                             |
| 13                   | 0C                                                   | Marimba                 | [マリンバ](../Page/マリンバ.md "wikilink")                                                   |
| 14                   | 0D                                                   | Xylophone               | [シロフォン](../Page/シロフォン.md "wikilink")                                                 |
| 15                   | 0E                                                   | Tubular Bell            | [チューブラーベル](../Page/チューブラーベル.md "wikilink")                                           |
| 16                   | 0F                                                   | Dulcimer                | [ダルシマー](../Page/ダルシマー.md "wikilink")                                                 |
| Organ                |                                                      |                         |                                                                                      |
| 17                   | 10                                                   | Drawbar Organ           | [ドローバーオルガン](../Page/ハモンドオルガン.md "wikilink")                                          |
| 18                   | 11                                                   | Percussive Organ        | パーカッシブオルガン                                                                           |
| 19                   | 12                                                   | Rock Organ              | ロックオルガン                                                                              |
| 20                   | 13                                                   | Church organ            | [チャーチオルガン](https://ja.wikipedia.org/wiki/オルガン#パイプオルガン "wikilink")                    |
| 21                   | 14                                                   | Reed organ              | [リードオルガン](https://ja.wikipedia.org/wiki/オルガン#リード・オルガンとハーモニウム "wikilink")             |
| 22                   | 15                                                   | Accordion               | [アコーディオン](../Page/アコーディオン.md "wikilink")                                             |
| 23                   | 16                                                   | Harmonica               | [ハーモニカ](../Page/ハーモニカ.md "wikilink")                                                 |
| 24                   | 17                                                   | Tango Accordion         | [タンゴアコーディオン](../Page/バンドネオン.md "wikilink")                                           |
| Guitar               |                                                      |                         |                                                                                      |
| 25                   | 18                                                   | Acoustic Guitar (nylon) | [アコースティックギター（ナイロン弦）](../Page/ギター.md "wikilink")                                      |
| 26                   | 19                                                   | Acoustic Guitar (steel) | [アコースティックギター（スチール弦）](../Page/ギター.md "wikilink")                                      |
| 27                   | 1A                                                   | Electric Guitar (jazz)  | [ジャズギター](../Page/エレクトリック・ギター.md "wikilink")                                          |
| 28                   | 1B                                                   | Electric Guitar (clean) | [クリーンギター](../Page/エレクトリック・ギター.md "wikilink")                                         |
| 29                   | 1C                                                   | Electric Guitar (muted) | [ミュートギター](../Page/ミュート_\(ギター\).md "wikilink")                                        |
| 30                   | 1D                                                   | Overdriven Guitar       | [オーバードライブギター](../Page/オーバードライブ_\(音響機器\).md "wikilink")                               |
| 31                   | 1E                                                   | Distortion Guitar       | [ディストーションギター](../Page/ディストーション_\(音響機器\).md "wikilink")                               |
| 32                   | 1F                                                   | Guitar harmonics        | [ギターハーモニクス](https://ja.wikipedia.org/wiki/フラジオレット#ギターでのフラジオレット\(ハーモニクス\) "wikilink") |
| Bass                 |                                                      |                         |                                                                                      |
| 33                   | 20                                                   | Acoustic Bass           | [アコースティックベース](../Page/アコースティック・ベース.md "wikilink")                                    |
| 34                   | 21                                                   | Electric Bass (finger)  | [フィンガー・ベース](../Page/エレクトリックベース.md "wikilink")                                        |
| 35                   | 22                                                   | Electric Bass (pick)    | [ピック・ベース](../Page/エレクトリックベース.md "wikilink")                                          |
| 36                   | 23                                                   | Fretless Bass           | [フレットレスベース](../Page/フレットレスベース.md "wikilink")                                         |
| 37                   | 24                                                   | Slap Bass 1             | [スラップベース](../Page/スラップ奏法.md "wikilink") 1                                            |
| 38                   | 25                                                   | Slap Bass 2             | スラップベース 2                                                                            |
| 39                   | 26                                                   | Synth Bass 1            | [シンセベース](../Page/シンセベース.md "wikilink") 1                                             |
| 40                   | 27                                                   | Synth Bass 2            | シンセベース 2                                                                             |
| Strings              |                                                      |                         |                                                                                      |
| 41                   | 28                                                   | Violin                  | [ヴァイオリン](../Page/ヴァイオリン.md "wikilink")                                               |
| 42                   | 29                                                   | Viola                   | [ヴィオラ](../Page/ヴィオラ.md "wikilink")                                                   |
| 43                   | 2A                                                   | Cello                   | [チェロ](../Page/チェロ.md "wikilink")                                                     |
| 44                   | 2B                                                   | Double bass             | [コントラバス](../Page/コントラバス.md "wikilink")                                               |
| 45                   | 2C                                                   | Tremolo Strings         | [トレモロ](../Page/トレモロ.md "wikilink")                                                   |
| 46                   | 2D                                                   | Pizzicato Strings       | [ピッチカート](https://ja.wikipedia.org/wiki/ピッチカート "wikilink")                            |
| 47                   | 2E                                                   | Orchestral Harp         | [ハープ](../Page/ハープ.md "wikilink")                                                     |
| 48                   | 2F                                                   | Timpani                 | [ティンパニ](../Page/ティンパニ.md "wikilink")                                                 |
| Ensemble             |                                                      |                         |                                                                                      |
| 49                   | 30                                                   | String Ensemble 1       | ストリング[アンサンブル](../Page/アンサンブル.md "wikilink")                                          |
| 50                   | 31                                                   | String Ensemble 2       | スローストリングアンサンブル                                                                       |
| 51                   | 32                                                   | Synth Strings 1         | シンセストリングス                                                                            |
| 52                   | 33                                                   | Synth Strings 2         | シンセストリングス2                                                                           |
| 53                   | 34                                                   | Voice Aahs              | 声「アー」                                                                                |
| 54                   | 35                                                   | Voice Oohs              | 声「ドゥー」                                                                               |
| 55                   | 36                                                   | Synth Voice             | [シンセヴォイス](https://ja.wikipedia.org/wiki/シンセヴォイス "wikilink")                          |
| 56                   | 37                                                   | Orchestra Hit           | [オーケストラヒット](../Page/オーケストラル・ヒット.md "wikilink")                                       |
| Brass                |                                                      |                         |                                                                                      |
| 57                   | 38                                                   | Trumpet                 | [トランペット](../Page/トランペット.md "wikilink")                                               |
| 58                   | 39                                                   | Trombone                | [トロンボーン](../Page/トロンボーン.md "wikilink")                                               |
| 59                   | 3A                                                   | Tuba                    | [チューバ](../Page/チューバ.md "wikilink")                                                   |
| 60                   | 3B                                                   | Muted Trumpet           | [ミュートトランペット](../Page/弱音器.md "wikilink")                                              |
| 61                   | 3C                                                   | French horn             | [フレンチ・ホルン](https://ja.wikipedia.org/wiki/ホルン#フレンチ・ホルン "wikilink")                    |
| 62                   | 3D                                                   | Brass Section           | ブラスセクション                                                                             |
| 63                   | 3E                                                   | Synth Brass 1           | シンセブラス 1                                                                             |
| 64                   | 3F                                                   | Synth Brass 2           | シンセブラス 2                                                                             |
| Reed                 |                                                      |                         |                                                                                      |
| 65                   | 40                                                   | Soprano Sax             | [ソプラノサックス](../Page/サクソフォーン.md "wikilink")                                            |
| 66                   | 41                                                   | Alto Sax                | [アルトサックス](../Page/サクソフォーン.md "wikilink")                                             |
| 67                   | 42                                                   | Tenor Sax               | [テナーサックス](../Page/サクソフォーン.md "wikilink")                                             |
| 68                   | 43                                                   | Baritone Sax            | [バリトンサックス](../Page/サクソフォーン.md "wikilink")                                            |
| 69                   | 44                                                   | Oboe                    | [オーボエ](../Page/オーボエ.md "wikilink")                                                   |
| 70                   | 45                                                   | English Horn            | [イングリッシュホルン](../Page/コーラングレ.md "wikilink")                                           |
| 71                   | 46                                                   | Bassoon                 | [ファゴット](../Page/ファゴット.md "wikilink")                                                 |
| 72                   | 47                                                   | Clarinet                | [クラリネット](../Page/クラリネット.md "wikilink")                                               |
| Pipe                 |                                                      |                         |                                                                                      |
| 73                   | 48                                                   | Piccolo                 | [ピッコロ](../Page/ピッコロ.md "wikilink")                                                   |
| 74                   | 49                                                   | Flute                   | [フルート](../Page/フルート.md "wikilink")                                                   |
| 75                   | 4A                                                   | Recorder                | [リコーダー](../Page/リコーダー.md "wikilink")                                                 |
| 76                   | 4B                                                   | Pan Flute               | [パンフルート](../Page/パンパイプ.md "wikilink")                                                |
| 77                   | 4C                                                   | Blown Bottle            | [ブロウンボトル](https://ja.wikipedia.org/wiki/ブロウンボトル "wikilink")（吹きガラス瓶）                  |
| 78                   | 4D                                                   | Shakuhachi              | [尺八](../Page/尺八.md "wikilink")                                                       |
| 79                   | 4E                                                   | Whistle                 | [口笛](../Page/口笛.md "wikilink")                                                       |
| 80                   | 4F                                                   | Ocarina                 | [オカリナ](../Page/オカリナ.md "wikilink")                                                   |
| Synth Lead           |                                                      |                         |                                                                                      |
| 81                   | 50                                                   | Lead 1 (square)         | [正方波](../Page/矩形波.md "wikilink")                                                     |
| 82                   | 51                                                   | Lead 2 (sawtooth)       | [ノコギリ波](https://ja.wikipedia.org/wiki/ノコギリ波 "wikilink")                              |
| 83                   | 52                                                   | Lead 3 (calliope)       | [カリオペ](https://ja.wikipedia.org/wiki/カリオペ "wikilink")リード                             |
| 84                   | 53                                                   | Lead 4 (chiff)          | [チフ](https://ja.wikipedia.org/wiki/チフ "wikilink")リード                                 |
| 85                   | 54                                                   | Lead 5 (charang)        | [チャランゴ](../Page/チャランゴ.md "wikilink")リード                                              |
| 86                   | 55                                                   | Lead 6 (voice)          | 声リード                                                                                 |
| 87                   | 56                                                   | Lead 7 (fifths)         | フィフスズリード                                                                             |
| 88                   | 57                                                   | Lead 8 (bass + lead)    | ベース + リード                                                                            |
| Synth Pad            |                                                      |                         |                                                                                      |
| 89                   | 58                                                   | Pad 1 (Fantasia)        | ファンタジア                                                                               |
| 90                   | 59                                                   | Pad 2 (warm)            | ウォーム                                                                                 |
| 91                   | 5A                                                   | Pad 3 (polysynth)       | [ポリシンセ](../Page/ポリフォニックシンセサイザー.md "wikilink")                                        |
| 92                   | 5B                                                   | Pad 4 (choir)           | [クワイア](https://ja.wikipedia.org/wiki/クワイア "wikilink")                                |
| 93                   | 5C                                                   | Pad 5 (bowed)           | ボウ                                                                                   |
| 94                   | 5D                                                   | Pad 6 (metallic)        | メタリック                                                                                |
| 95                   | 5E                                                   | Pad 7 (halo)            | ハロー                                                                                  |
| 96                   | 5F                                                   | Pad 8 (sweep)           | スウィープ                                                                                |
| Synth Effects        |                                                      |                         |                                                                                      |
| 97                   | 60                                                   | FX 1 (rain)             | 雨                                                                                    |
| 98                   | 61                                                   | FX 2 (soundtrack)       | サウンドトラック                                                                             |
| 99                   | 62                                                   | FX 3 (crystal)          | クリスタル                                                                                |
| 100                  | 63                                                   | FX 4 (atmosphere)       | アトモスフィア                                                                              |
| 101                  | 64                                                   | FX 5 (brightness)       | ブライトネス                                                                               |
| 102                  | 65                                                   | FX 6 (goblins)          | [ゴブリン](../Page/ゴブリン.md "wikilink")                                                   |
| 103                  | 66                                                   | FX 7 (echoes)           | [エコー](../Page/エコー.md "wikilink")                                                     |
| 104                  | 67                                                   | FX 8 (sci-fi)           | [サイファイ](https://ja.wikipedia.org/wiki/サイファイ "wikilink")                              |
| Ethnic               |                                                      |                         |                                                                                      |
| 105                  | 68                                                   | Sitar                   | [シタール](../Page/シタール.md "wikilink")                                                   |
| 106                  | 69                                                   | Banjo                   | [バンジョー](../Page/バンジョー.md "wikilink")                                                 |
| 107                  | 6A                                                   | Shamisen                | [三味線](../Page/三味線.md "wikilink")                                                     |
| 108                  | 6B                                                   | Koto                    | [琴](../Page/琴.md "wikilink")                                                         |
| 109                  | 6C                                                   | Kalimba                 | [カリンバ](../Page/カリンバ.md "wikilink")                                                   |
| 110                  | 6D                                                   | Bagpipe                 | [バグパイプ](https://ja.wikipedia.org/wiki/バグパイプ "wikilink")                              |
| 111                  | 6E                                                   | Fiddle                  | [フィドル](../Page/フィドル.md "wikilink")                                                   |
| 112                  | 6F                                                   | Shanai                  | [シャハナーイ](https://ja.wikipedia.org/wiki/シャハナーイ "wikilink")                            |
| Percussive           |                                                      |                         |                                                                                      |
| 113                  | 70                                                   | Tinkle Bell             | [ティンクルベル](https://ja.wikipedia.org/wiki/ティンクルベル "wikilink")                          |
| 114                  | 71                                                   | Agogo                   | [アゴゴ](../Page/アゴゴ.md "wikilink")                                                     |
| 115                  | 72                                                   | Steel Drums             | [スチールドラム](../Page/スティールパン.md "wikilink")                                             |
| 116                  | 73                                                   | Woodblock               | [ウッドブロック](https://ja.wikipedia.org/wiki/ウッドブロック "wikilink")                          |
| 117                  | 74                                                   | Taiko Drum              | [太鼓](../Page/太鼓.md "wikilink")                                                       |
| 118                  | 75                                                   | Melodic Tom             | [メロディックタム](https://ja.wikipedia.org/wiki/メロディックタム "wikilink")                        |
| 119                  | 76                                                   | Synth Drum              | [シンセドラム](https://ja.wikipedia.org/wiki/シンセドラム "wikilink")                            |
| 120                  | 77                                                   | Reverse Cymbal          | 逆シンバル                                                                                |
| Sound effects        |                                                      |                         |                                                                                      |
| 121                  | 78                                                   | Guitar Fret Noise       | ギターフレットノイズ                                                                           |
| 122                  | 79                                                   | Breath Noise            | ブレスノイズ                                                                               |
| 123                  | 7A                                                   | Seashore                | [海岸](../Page/海岸.md "wikilink")                                                       |
| 124                  | 7B                                                   | Bird Tweet              | 鳥の囀り                                                                                 |
| 125                  | 7C                                                   | Telephone Ring          | 電話のベル                                                                                |
| 126                  | 7D                                                   | Helicopter              | [ヘリコプター](../Page/ヘリコプター.md "wikilink")                                               |
| 127                  | 7E                                                   | Applause                | [拍手](../Page/拍手.md "wikilink")                                                       |
| 128                  | 7F                                                   | Gunshot                 | [銃声](https://ja.wikipedia.org/wiki/銃声 "wikilink")                                    |

### Percussion notes

[GM_Standard_Drum_Map_on_the_keyboard.svg](https://ja.wikipedia.org/wiki/File:GM_Standard_Drum_Map_on_the_keyboard.svg "fig:GM_Standard_Drum_Map_on_the_keyboard.svg") GMでは10チャンネルは、[パーカッションのために予約されている](../Page/打楽器.md "wikilink")。このチャンネルはプログラムが音色変更命令を送っても常にパーカションパートとなり、各ノートナンバーには異なる楽器が割り当てられている。この、ノートナンバーに対する打楽器割り当て表をドラムマップ(drum map)と呼ぶことがある。 {{-}}

| No. | [16進数](https://ja.wikipedia.org/wiki/16進数 "wikilink") | English         | 日本語                                                                |
| --- | ----------------------------------------------------- | --------------- | ------------------------------------------------------------------ |
| 35  | 23                                                    | Bass Drum 2     | [バスドラム](../Page/バスドラム.md "wikilink") 2                             |
| 36  | 24                                                    | Bass Drum 1     | バスドラム 1                                                            |
| 37  | 25                                                    | Side Stick      | サイドスティック                                                           |
| 38  | 26                                                    | Snare Drum 1    | [スネアドラム](../Page/スネアドラム.md "wikilink") 1                           |
| 39  | 27                                                    | Hand Clap       | 手拍子                                                                |
| 40  | 28                                                    | Snare Drum 2    | スネアドラム 2                                                           |
| 41  | 29                                                    | Low Tom 2       | [ロートム](../Page/トムトム.md "wikilink") 2                               |
| 42  | 2A                                                    | Closed Hi-hat   | [クローズハイハット](https://ja.wikipedia.org/wiki/シンバル#ハイハット "wikilink")   |
| 43  | 2B                                                    | Low Tom 1       | ロートム 1                                                             |
| 44  | 2C                                                    | Pedal Hi-hat    | [ペダルハイハット](https://ja.wikipedia.org/wiki/シンバル#ハイハット "wikilink")    |
| 45  | 2D                                                    | Mid Tom 2       | [ミドルトム](../Page/トムトム.md "wikilink") 2                              |
| 46  | 2E                                                    | Open Hi-hat     | [オープンハイハット](https://ja.wikipedia.org/wiki/シンバル#ハイハット "wikilink")   |
| 47  | 2F                                                    | Mid Tom 1       | ミドルトム 1                                                            |
| 48  | 30                                                    | High Tom 2      | [ハイトム](../Page/トムトム.md "wikilink") 2                               |
| 49  | 31                                                    | Crash Cymbal 1  | [クラッシュシンバル](https://ja.wikipedia.org/wiki/シンバル#クラッシュ "wikilink") 1 |
| 50  | 32                                                    | High Tom 1      | ハイトム 1                                                             |
| 51  | 33                                                    | Ride Cymbal 1   | [ライドシンバル](https://ja.wikipedia.org/wiki/シンバル#ライド "wikilink") 1     |
| 52  | 34                                                    | Chinese Cymbal  | [チャイニーズシンバル](https://ja.wikipedia.org/wiki/シンバル#チャイナ "wikilink")   |
| 53  | 35                                                    | Ride Bell       | ライドベル                                                              |
| 54  | 36                                                    | Tambourine      | [タンバリン](../Page/タンバリン.md "wikilink")                               |
| 55  | 37                                                    | Splash Cymbal   | [スプラッシュシンバル](https://ja.wikipedia.org/wiki/シンバル#スプラッシュ "wikilink") |
| 56  | 38                                                    | Cowbell         | [カウベル](../Page/カウベル.md "wikilink")                                 |
| 57  | 39                                                    | Crash Cymbal 2  | クラッシュシンバル 2                                                        |
| 58  | 3A                                                    | Vibra Slap      | [ヴィブラスラップ](../Page/ヴィブラスラップ.md "wikilink")                         |
| 59  | 3B                                                    | Ride Cymbal 2   | ライドシンバル 2                                                          |
| 60  | 3C                                                    | High Bongo      | ハイ[ボンゴ](../Page/ボンゴ.md "wikilink")                                 |
| 61  | 3D                                                    | Low Bongo       | ローボンゴ                                                              |
| 62  | 3E                                                    | Mute High Conga | ミュートハイ[コンガ](../Page/コンガ.md "wikilink")                             |
| 63  | 3F                                                    | Open High Conga | オープンハイコンガ                                                          |
| 64  | 40                                                    | Low Conga       | ローコンガ                                                              |
| 65  | 41                                                    | High Timbale    | ハイ[ティンバル](../Page/ティンバレス.md "wikilink")                            |
| 66  | 42                                                    | Low Timbale     | ローティンバル                                                            |
| 67  | 43                                                    | High Agogo      | ハイ[アゴゴ](../Page/アゴゴ.md "wikilink")                                 |
| 68  | 44                                                    | Low Agogo       | ローアゴゴ                                                              |
| 69  | 45                                                    | Cabasa          | [カバサ](https://ja.wikipedia.org/wiki/カバサ "wikilink")                |
| 70  | 46                                                    | Maracas         | [マラカス](../Page/マラカス.md "wikilink")                                 |
| 71  | 47                                                    | Short Whistle   | ショート[ホイッスル](../Page/ホイッスル.md "wikilink")                           |
| 72  | 48                                                    | Long Whistle    | ロングホイッスル                                                           |
| 73  | 49                                                    | Short Guiro     | ショート[ギロ](../Page/ギロ.md "wikilink")                                 |
| 74  | 4A                                                    | Long Guiro      | ロングギロ                                                              |
| 75  | 4B                                                    | Claves          | [クラベス](https://ja.wikipedia.org/wiki/クラベス "wikilink")              |
| 76  | 4C                                                    | High Wood Block | ハイ[ウッドブロック](https://ja.wikipedia.org/wiki/ウッドブロック "wikilink")      |
| 77  | 4D                                                    | Low Wood Block  | ローウッドブロック                                                          |
| 78  | 4E                                                    | Mute Cuica      | ミュート[クイーカ](../Page/クイーカ.md "wikilink")                             |
| 79  | 4F                                                    | Open Cuica      | オープンクイーカ                                                           |
| 80  | 50                                                    | Mute Triangle   | ミュート[トライアングル](../Page/トライアングル.md "wikilink")                       |
| 81  | 51                                                    | Open Triangle   | オープントライアングル                                                        |

### Controller events

GMは再生時に受信すべきいくつかのコントローラを規定している[1](http://www.indiana.edu/~emusic/cntrlnumb.html)[2](http://www.midisite.com/info/synth/Control.htm)。

| No. | 機能                                                                            |
| --- | ----------------------------------------------------------------------------- |
| 1   | モジュレーション (Modulation)                                                         |
| 6   | データエントリ [MSB](https://ja.wikipedia.org/wiki/最上位ビット "wikilink") (DataEntryMSB) |
| 7   | ボリューム (Part Level)                                                            |
| 10  | パンポット (Part Panpot)                                                           |
| 11  | エクスプレッション (Expression)                                                        |
| 38  | データ エントリ [LSB](../Page/最下位ビット.md "wikilink") (DataEntryLSB)                   |
| 64  | [サステイン](../Page/サステイン.md "wikilink") (Hold1)                                  |
| 100 | RPN [LSB](../Page/最下位ビット.md "wikilink")                                       |
| 101 | RPN [MSB](https://ja.wikipedia.org/wiki/最上位ビット "wikilink")                    |
| 120 | 消音 (AllSoundOff)                                                              |
| 121 | リセット・オールコントロール (ResetAllControl)                                              |

### RPN

RPNとは、**Registered Parameter Numbers** の略称で、主に音色自体の変更などに用いられる、コントロール チェンジ・イベントの一種である。

RPN パラメータの設定法（数字は[十進数](../Page/十進法.md "wikilink")）。

1.  CC:101 (RPN LSB) と CC:100 (RPN MSB) を送信し、変更するパラメータを指定する
2.  CC:6 (DataEntryMSB) を送信し、パラメータに値を設定する

これだけではいつでも CC:6 を送信することで値を変更できるので、NULL 値を最後に送信することが慣例になっている。具体的には CC:101、CC:100 の両方に 127 を送信する。

以下のグローバル [RPN](https://ja.wikipedia.org/wiki/RPN "wikilink") は標準化されている\[1\]。

| MSB | LSB | 設定パラメータ                       | 説明                                                                |
| --- | --- | ----------------------------- | ----------------------------------------------------------------- |
| 0   | 0   | Pitch Bend Sensitivity (ベンド幅） | CC:130 (Pitch Bend) の値が最大（最小）のとき、どれだけ音程が 変化するかを半音単位で設定する。(0 ～ 24) |
| 0   | 1   | Channel Fine Tuning           | パートの音程を半音の 1 / 8192 単位で調整する。(-8192 ～ 8191)                        |
| 0   | 2   | Channel Coarse Tuning         | パートの音程を半音単位で調整する。64を基点として増減させる。 (40 ～ 88)                         |
| 0   | 3   | Tuning Program Select         | ほとんど使われない\[2\]                                                    |
| 0   | 4   | Tuning Bank Select            | ほとんど使われない\[3\]                                                    |
| 0   | 5   | Modulation Depth Range        | CC:1 (Modulation) の変化幅を設定する。GM2で採用された。                            |
| 127 | 127 | RPN NULL                      | CC:6 (Data Entry MSB)、CC:38 (Data Entry LSB)を無効化する                |

例：ピッチベンドレンジを 12 にしたい場合

    CC:101[0]、CC:100[0]、CC:6[12]

### システム エクスクルーシブ メッセージ

GM では以下のシステム エクスクルーシブメッセージを規定している。

  - GM System ON
    GM システムのデフォルトの設定に音源を設定する
  - MasterVolume
    音源全体の音量を調整する

## General MIDIの問題点

前述のような理由で定められた統一規格ではあるが、問題点もある。

GM規格では音色の並び方やコントロールチェンジの種類が決められているが、音色そのものについてやコントロールチェンジによる変化量などについては、各 MIDI 音源メーカーの独自性が損なわれる可能性があるとされ、厳密には定められていない。そのため GM 規格に準拠したデータであっても、作者の意図したように再現されない可能性も少なからずある。

その他にも、最大同時発音数が後発の機器であるほど増やされていることや、エフェクトや音量の変化量などが各社で異なること、ユニバーサル・エクスクルーシブなどの拡張機能への対応の有無など問題は多く、十分とは言えないことも多い。

すなわち、同じ高さの[鍵盤](https://ja.wikipedia.org/wiki/鍵盤 "wikilink")を弾いても実際に鳴る音の[オクターブ](https://ja.wikipedia.org/wiki/オクターブ "wikilink")は選んでいる[楽器](../Page/楽器.md "wikilink")の種類によって異なる場合があるので注意する。

## 脚注

## 外部リンク

  - [AMEI \<社団法人　音楽電子事業協会\>](http://www.amei.or.jp/)
  - [（AMEI 内仕様書一覧）](http://www.amei.or.jp/specifications/index.html)
  - [Specs （MIDI Manufactures Association 内各種仕様書一覧）](https://www.midi.org/specifications)

[Category:MIDI](https://ja.wikipedia.org/wiki/Category:MIDI "wikilink") [Category:シンセサイザー](https://ja.wikipedia.org/wiki/Category:シンセサイザー "wikilink")

1.  <http://www.midi.org/about-midi/table3.shtml>
2.
3.