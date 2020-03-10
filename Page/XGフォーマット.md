> この記事は[XG](https://ja.wikipedia.org/wiki/XG)から翻訳されています。


[Yamaha_ymf744b_v.jpg](https://ja.wikipedia.org/wiki/File:Yamaha_ymf744b_v.jpg "fig:Yamaha_ymf744b_v.jpg") **XGフォーマット**（エックスジーフォーマット）とは[1994年](../Page/1994年.md "wikilink")に[ヤマハ](../Page/ヤマハ.md "wikilink")が提唱した[MIDI](../Page/MIDI.md "wikilink")の規格である。\[1\]

## 概要

音色配列、エフェクト、音色エディットのパラメータ等を統一し、ヤマハ製の他の[音源モジュール](https://ja.wikipedia.org/wiki/音源モジュール "wikilink")や[シンセサイザー](../Page/シンセサイザー.md "wikilink")でも伴奏データをほぼ同一の音色で再生可能にすることを目的に制定された規格である。この規格制定においてはヤマハによる[GMの独自拡張が行われている](https://ja.wikipedia.org/wiki/General_MIDI "wikilink")。

他社製品だが、[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")の音源モジュールや電子ピアノの中にはXGに対応したものも発表されている。また非公式ながら、[ローランド](../Page/ローランド.md "wikilink")の音源モジュール[SC-88ProにはXG](https://ja.wikipedia.org/wiki/ローランド・SCシリーズ "wikilink")[互換モード](https://ja.wikipedia.org/wiki/互換モード "wikilink")が搭載されている。

XGフォーマットは、480音色以上の膨大な音色数、音色の修正方法、3種類以上のエフェクト、ダイナミック[フィルター](../Page/フィルター.md "wikilink")、外部入力対応などを規定している。当時としては、規格が高かった。また、[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")にXG liteというXGの簡易版も規定された。XG liteが作られた理由は、XGに比べて規格が軽量で、小型モデルの電子キーボードといった安価な製品に、XG完全対応音源を入れるとXG再現のハードルが高くなるからである。XG liteではコントロールできるパラメーターやエフェクトなどに一部制限があるため、「XG」のソングデータが元のデータと異なって聞こえる場合がある。その後[2001年](../Page/2001年.md "wikilink")にはXGフォーマットとの親和性向上のため、XGlite Ver2.0が規定された。

「XG」の由来は公式には発表されていない。

## XGの基本思想

XGの基本思想は、**互換性**、**適応性**、**拡張性**が挙げられる。

**互換性**は、XG対応データはXG対応機器で再生すれば、異なるモデルであっても再生可能であり、[GMとの](https://ja.wikipedia.org/wiki/General_MIDI "wikilink")[上位互換](https://ja.wikipedia.org/wiki/上位互換 "wikilink")性を持っているため、GM対応の伴奏データも正しく再生可能だということである。

**適応性**は、XGでは音色数や音色変更方法等を細かく規定されているが、全ての機能を網羅する必要がなく、同じ伴奏データを性能や価格帯の異なるモデルで再生しても、それぞれのモデルの能力に応じた再生が可能だということである。

**拡張性**は、製品の開発とともに[フォーマット](https://ja.wikipedia.org/wiki/フォーマット "wikilink")内容を柔軟に拡張できるということである。現にMU80からMU90、MU100と上位機種が発表されると、その機種に応じた新しいエフェクトや音色、機能が増えている。

[MIDI](../Page/MIDI.md "wikilink")音源の一般的な規格である[GMとの上位互換性の点でまず挙げられるのは音色数である](https://ja.wikipedia.org/wiki/General_MIDI "wikilink")。GMで規定された128音色があるが、XGはバンクセレクトを利用して、大幅に音色数を増やしている。バンクセレクトLSBにより、GMの基本音色に対してバリエーション的な音色を配置し、そのバンク番号ごとにバリエーションの性格（例えば、オクターブユニゾンや[ステレオ](../Page/ステレオ.md "wikilink")など）が定められ、検索を容易にしている。バンクセレクトMSBを40Hにすることにより、[効果音](../Page/効果音.md "wikilink")のSFXバンクに切り替えられ、またバンクセレクトMSBを7EHまたは7FHにすることにより、そのパートを[ドラムパートに切り替えられる](../Page/ドラムセット.md "wikilink")。また、上位機種で作られたデータを下位機種で再生する場合、再生する機種にない音色があってもGMの基本音色で鳴らすことができる（代理発音）。

エフェクトも切り替えられ、その種類や結線まで規定されている。そして各パラメータやコントロール方法も規定しているため、高度な要求にも応えられるようになっている。[グラフィックイコライザーを搭載した機種では](../Page/エフェクター.md "wikilink")、曲調に合った雰囲気を出せるようにすることも可能である。そして外部からの信号を受け取り、それにエフェクトをかけ、音源内部の[ミキサーで音源内の音色と同様にコントロールする規定も定められている](https://ja.wikipedia.org/wiki/ミキシングコンソール "wikilink")。これによって、XG音源を使って[カラオケ](../Page/カラオケ.md "wikilink")をしたり、[エレクトリックギター](https://ja.wikipedia.org/wiki/エレクトリックギター "wikilink")をつなげて、バンド演奏等もできるようになっている。

XGフォーマット自体は、[ローランド](../Page/ローランド.md "wikilink")社の規格[GSとは直接の](https://ja.wikipedia.org/wiki/GSフォーマット "wikilink")[互換性](https://ja.wikipedia.org/wiki/互換性 "wikilink")はない。ただ、大多数の**XG**対応の音源モジュールや[シンセサイザー](../Page/シンセサイザー.md "wikilink")には**TG300-Bモード**と呼ばれる**GS**との互換モードが用意されている。GS対応のMIDIデータを再生すると、このモードに切り替えて100%とまでは行かないが、違和感のない程度には再生をすることも可能である。現在は**TG300-Bモード**に代わり、**GSモード**（GSフォーマットに正式対応）を備えた**XG**音源モジュールも存在する。

## XG対応製品

### XG対応（XGlite対応）音源モジュール

  - MU5を除く[MUシリーズ](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")
  - KORG [NX5R](https://ja.wikipedia.org/wiki/コルグ・Nシリーズ "wikilink")
  - EDIROL [SDシリーズ](../Page/エディロール・SDシリーズ.md "wikilink")（SD-50を除く、XGlite対応）

### XG対応シンセサイザー

  - [SDX3000](https://ja.wikipedia.org/wiki/ヤマハ・SDX3000 "wikilink")
  - SHK-1000
  - SHK-1000Ⅱ
  - SKB-J700(XGlite)
  - [QS300](https://ja.wikipedia.org/wiki/ヤマハ・QS300 "wikilink")
  - [CS1x、CS2x](https://ja.wikipedia.org/wiki/ヤマハ・CSシリーズ "wikilink")
  - [S03BL、S03SL、S08](https://ja.wikipedia.org/wiki/ヤマハ・Sシリーズ "wikilink")
  - [EOS B900,B900EX](../Page/ヤマハ・EOSシリーズ.md "wikilink")

<!-- end list -->

  -
    (Stream,Ghost,Scratch 2,WindChm,Jetplane,Starship,Burst,LaserGun,FireWork以外のSFX音色はXG/TG300-Bモード共に発音しない)

<!-- end list -->

  - [EOS B2000,B2000W](../Page/ヤマハ・EOSシリーズ.md "wikilink")
  - [EOS BX](../Page/ヤマハ・EOSシリーズ.md "wikilink")

### XG対応音源内蔵MIDIキーボード

  - [CBX-K1XG](../Page/ヤマハ・CBXシリーズ.md "wikilink")
  - [CBX-K1XGB](../Page/ヤマハ・CBXシリーズ.md "wikilink")
  - [CBX-K1XGs](../Page/ヤマハ・CBXシリーズ.md "wikilink")

### XG対応電子オルガン

  - SE-8000
  - SE-7000
  - SE-7000Ⅱ
  - SE-4000
  - SE-3000
  - [エレクトーン](../Page/エレクトーン.md "wikilink")

### XG対応電子ピアノ

  - P-250
  - CP300
  - SEP-3000(XGlite)
  - [クラビノーバ](../Page/クラビノーバ.md "wikilink")
  - [ローランドピアノ・デジタル](../Page/電子ピアノ.md "wikilink")

### XG対応MIDIプレーヤー

  - MDP30（[GS](https://ja.wikipedia.org/wiki/GSフォーマット "wikilink")、[GM2にも対応](https://ja.wikipedia.org/wiki/GM2フォーマット "wikilink")）
  - MDP30S（[GS](https://ja.wikipedia.org/wiki/GSフォーマット "wikilink")、[GM2にも対応](https://ja.wikipedia.org/wiki/GM2フォーマット "wikilink")）
  - MDP20XG
  - MDP10
  - MDP10S
  - MDP5（[GS](https://ja.wikipedia.org/wiki/GSフォーマット "wikilink")、[GM2にも対応](https://ja.wikipedia.org/wiki/GM2フォーマット "wikilink")）
  - EMR1
  - Roland MT-90U (XGlite)

### XG対応音源内蔵シーケンサー

  - [QY70](../Page/ヤマハ・QYシリーズ.md "wikilink")
  - [QY100](../Page/ヤマハ・QYシリーズ.md "wikilink")
  - [QY700](../Page/ヤマハ・QYシリーズ.md "wikilink")

### XG対応音源ボード

[Yamaha_DB50XG_daughterboard_1995.jpg](https://ja.wikipedia.org/wiki/File:Yamaha_DB50XG_daughterboard_1995.jpg "fig:Yamaha_DB50XG_daughterboard_1995.jpg") [PCIsoundcard.jpg](https://ja.wikipedia.org/wiki/File:PCIsoundcard.jpg "fig:PCIsoundcard.jpg")搭載のPCIバスカード\]\]

  - DB50XG
    697音色＋3ブロックエフェクト内蔵。[Sound Blasterなどの音源ボードに装着することで](../Page/Sound_Blaster.md "wikilink")、XG対応になる。MU50同等の性能を持つドータボード音源。[DOS/V専用](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")。
    MU50にあるDOCモード、C/Mモード及びパフォーマンスモードは装備しない為、むしろMU10に近い。なおA/Dインプットは装備しない。
    Windows 95/3.1対応シーケンスソフト「Digital Orchestrator Plus」同梱。
  - DB51XG
    697音色＋3ブロックエフェクト内蔵。[コルグ](https://ja.wikipedia.org/wiki/コルグ "wikilink")のNX5Rに内蔵されている。基板の形は前述のDB50XGと異なるため、型番が変わったと思われる。
  - DB60XG
    697音色＋3ブロックエフェクト内蔵。Super 歌楽 for PC-98同梱音源ボード。NEC [PC-9800シリーズ](../Page/PC-9800シリーズ.md "wikilink")のデスクトップパソコンに取り付けることで、通信カラオケが楽しめるボード。A/Dインプット内蔵。ドータボード形状をしており（基板の形が前述のDB50XGに類似）、CanBeシリーズ（PC-9821Cr13には装着不可）以外の機種ではNEC製PC-9801-118又は、Sound Blasterが必要。
  - SW60XG
    697音色＋3ブロックエフェクト内蔵。Super 歌楽 for DOS/V同梱音源ボード。ISAバスカード型の音源ボード。IBM [PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")のデスクトップパソコンに取り付けることで、通信カラオケが楽しめるボード。A/Dインプット内蔵。
  - WAVEFORCE 192XG
    676音色+ドラムキット21音色を内蔵。ソフトシンセサイザーにより最大192音同時発音が可能となっている。また、DirectSound、DirectSound 3Dに対応。「SB-Link」に対応したケーブルが添付。ソフトシンセサイザー「S-YXG50」、シーケンサー「XGWorks Lite」、MIDI再生ソフト「MIDPLUG」、「SoundVQ」、XG音源に対応したゲームなどのソフトウェアが付属。
  - WAVEFORCE 192XG PLUS
    上記WAVEFORCE 192XGの同梱ソフトに「ジャカジャン」「デジカメミュージックアルバム体験版」などが追加されたもの。
  - WAVEFORCE 192digital
    WAVEFORCE 192XGの後継機種。光デジタル出力端子を搭載。MDやDATと直接接続することでデジタル録音が可能となった。また、AD/DAコンバータの変更によるS/N比の向上、ステレオ感の増す“Phatステレオエンハンスメント技術”の採用が行なわれている。
  - SW1000XG
    1267ノーマルボイス＋46ドラムセット、32パート最大同時発音数64音。[Modular Synthesis Plug-in Systemボードも搭載可能](https://ja.wikipedia.org/wiki/Modular_Synthesis_Plug-in_System "wikilink")。MU100と同等のXG音源を搭載し、PCIスロットに取り付け可能。
  - SW1000XG/P
    上述のSW1000XGのマイナーチェンジ品。SW1000XGでは取り付け不可だったPLG150-ANとPLG150-PFに対応している。
  - PCC10XG
    676楽器音＋21ドラムセット。PCMCIA TypeII準拠したPCカード音源。MU10同等のスペックを内蔵。Hello\!Music\! PCC10の同梱音源である。
  - [PLG100-XG](https://ja.wikipedia.org/wiki/Modular_Synthesis_Plug-in_System "wikilink")
    XG非対応のシンセサイザーをXG対応にする音源ボード。音色数や最大同時発音数はMU50とスペックは同じだが、波形を差し替えてリファインし、サウンドクオリティをMU100相当にグレードアップしている。
    音源方式 AWM2音源（XGフォーマット対応） 最大同時発音数 32音 パート数 16パート 音色数 480ノーマルボイス＋12ドラムキット

### XG対応サウンドLSI

  - YMF724, YMF744, YMF754(DS-XG)
    676楽器音＋21ドラムセット、16パート最大同時発音数64音。実際には非公式ツールによる設定変更で80音程度まで対応。各社製[サウンドカード](../Page/サウンドカード.md "wikilink")やパソコンで多数採用例があるほか、ヤマハ自身もYMF724を使用するサウンドカードを発売していた。各チップの差異はPCM録音/再生に関するものであり、MIDI再生については同一性能。XGフォーマットのMIDI再生は、[Windows環境でヤマハ製](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink")[ドライバをインストールしたときのみ使用可能](../Page/デバイスドライバ.md "wikilink")。(Windows同梱の[マイクロソフト](../Page/マイクロソフト.md "wikilink")製ドライバでは通常の音声再生のみサポート。一部のプリインストール機で、同LSIを搭載しているにも関わらずXGが利用できない場合は、ヤマハ公式の「汎用ドライバ」をインストールすることで利用できる場合がある。)なお、チップ表面にはXGロゴが印刷されている。

### XG対応（XGlite対応）のソフトウェア音源

  - S-YG20
    XG liteの原型となった音色配列を持つ。XGに完全に対応していない。
    音源方式 ウエーブテーブル合成 最大同時発音数32音 サンプリング周波数 22kHz / 11kHz XGフォーマット音色マップ対応 ノーマル360音色＋11ドラムキット（2SFXバンク含む） エフェクト リバーブ
  - S-YXG50
    XG対応の[ソフトウェア音源](../Page/ソフトウェア・シンセサイザー.md "wikilink")。Ver.4はWindowsXP対応。デバイスドライバとして機能するソフトウェア音源であるが、シーケンサーソフトSOL2等にバンドルされているVST版もある。WindowsXP以前では、パソコンにバンドルされていることも多かった。
    音源方式 AWM（ウエーブテーブル合成） 676音色＋21ドラム サンプリング周波数 44.1kHz／22.05kHz／11.025kHz 最大同時発音数 128音（CPUの性能に依存）出力 16ビットステレオ 演奏パート数 16パート エフェクト 3系統（リバーブ×11タイプ、コーラス×11タイプ、バリエーション×43タイプ）
    Intel MMXテクノロジ対応。
    またこのS-YXG50は、現在では単独での販売はされてはいない。ただし、Windows Update（Windows Updateカタログ）にてS-YXG50のWindows2000/XP対応版として「YAMAHA XG WDM SoftSynthesizer」が公開されており、無料でダウンロードすることができる。
    ただし、これにはアンインストーラーが付いていないので、完全・安全なアンインストールができない可能性がある。
    YAMAHA XG WDM SoftSynthesizerには公式の設定ツールは存在しないが、レジストリを編集することで設定を変更することが可能。
    なお、[MidRadio Playerのバージョン](https://ja.wikipedia.org/wiki/MidRadio_Player "wikilink")6までは、これを流用した音源を使用していたと言われている。
  - S-YXG100plus
    上記S-YXG50に[VA音源とフォルマントシンギング音源を付加したソフトウェア音源](../Page/物理モデル音源.md "wikilink")。WindowsXP/2000未対応。
  - MidRadio Player
    ヤマハが提供しているメディアプレーヤー。独自のソフトウェア音源を内蔵している。
    「音楽データショップ」（2015年6月1日から「ヤマハミュージックデータショップ」に改称）のMIDIデータと月額サービスの「パソカラホーダイ」「ネットで歌本」のMIDIデータの視聴に必要。

### その他

  - サイレントアンサンブルピアノ
    [ドリームキャスト](../Page/ドリームキャスト.md "wikilink")（XGlite対応）

## XG対応音源の変遷

### XGフォーマットの制定前（1994年）

ヤマハは[1993年](../Page/1993年.md "wikilink")に[TG300というGM対応の音源モジュールを発売した](https://ja.wikipedia.org/wiki/ヤマハ・TGシリーズ "wikilink")。TG300はGMだけではなく、ローランド社の規格であるGSに対応した音色配列モードを持っていた。これは、この時点でGSがDTMの音色配列規格のデファクトスタンダードを確立していたためであった（TG300が発売されていた時点ではGMの上位規格はGSに統一されていた）。しかし、TG300はライバル機であったSC-55mkIIに比べて割高な値段設定などの理由で、ヒット商品とはなりえなかった。そのため、TG300の後継機MU80を発売する際に、ライバル機として認知されること、ヤマハの独自性を維持するため、ヤマハは独自の規格「XG」を作ることにした。新たに3つ目の音色配列規格を作ることはユーザの混乱を招く可能性があったが、XG規格を制定した理由としては、GSはローランドの独自規格であるため、音色の原波形やフィルター、エフェクトやそのかかり方にローランド社固有の特性があり、他社が100%の再現性を保証することは困難であったこと、そして、もしローランドの[OEM](../Page/OEM.md "wikilink")を受けて100%再現できるように設計した場合、逆にヤマハの独自性が維持できない、などがあったためと考えられている。また本来MIDI音源の音色配列規格は厳密な互換性を要求されるものではなく、ピアノならピアノ、ギターならギターと同じ種類の音色が鳴ればよいという程度の緩やかな規格であったことも、新しい規格を作ることを容易にした。この結果、独自にXG規格をつくる一方で、GSをシミュレートするTG300-BモードもXG音源に残すという方法をとったものと思われる。

### MU80・MU5の登場（1994年末～1995年初頭）

[1994年](../Page/1994年.md "wikilink")末にXG対応音源第1号として[MU80が発売される](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")。MU80は32パート、最大同時発音数64音という当時のGS音源最高峰モデル[SC-88と同等以上のスペックであった](https://ja.wikipedia.org/wiki/ローランド・SCシリーズ "wikilink")。しかし、94年当時のXG対応音源はMU80一機種のみであり、MU80がXGのベーシックモデルなのか、それとも[ハイエンド](https://ja.wikipedia.org/wiki/ハイエンド "wikilink")モデルなのか不明な状況が半年ほど続いた（MUシリーズのベーシックモデルとして[MU5が発売されていたが](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")、[GMのみ対応](https://ja.wikipedia.org/wiki/General_MIDI "wikilink")）。

### MU50の登場（1995年）

[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")の春から夏頃にかけて、ヤマハは16パート、最大同時発音数32音の[MU50を発売](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")。ヤマハはMU80をハイエンドモデル、MU50をベーシックモデルという位置づけにするが、MU50全体で見ると、ディスクオーケストラモードに対応した関係で、MU80よりMU50のほうが音色数が多かったり、CHORUS4、CELESTE4といったMU80にはないエフェクトが後発のMU50にあったりして、MU80が完全なMU50の上位互換機ではなかった。

### MU50と互換性を持つ他機種の登場（1995年～1996年）

この[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")から[1996年](../Page/1996年.md "wikilink")にかけて、ヤマハは[ワークステーションタイプのシンセサイザー](https://ja.wikipedia.org/wiki/ミュージックワークステーション "wikilink")[QS300](https://ja.wikipedia.org/wiki/ヤマハ・QS300 "wikilink")、音源内蔵キーボード[CBX-K1XG](../Page/ヤマハ・CBXシリーズ.md "wikilink")、[ドーターボード](https://ja.wikipedia.org/wiki/ドーターボード "wikilink")音源DB50XG、音源内蔵[シーケンサー](https://ja.wikipedia.org/wiki/ミュージックシーケンサー "wikilink")[QY700](../Page/ヤマハ・QYシリーズ.md "wikilink")、DTM用シンセサイザー[CS1x](https://ja.wikipedia.org/wiki/ヤマハ・CSシリーズ "wikilink")、MU50のディスプレイ、ボタン類省略モデル[MU10と](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")、MU50互換品を多数発売した。

そしてヤマハのホームページ上からダウンロード可能なデモソングもMU50準拠のMIDIデータとなっており、ヤマハのPCカラオケ『歌楽』のMIDIデータもMU50準拠となっていた。ヤマハはハード面だけでなくソフト面でもMU50の標準機化を進めていた。 一方で、ユーザは発音数が多いMU80を購入するケースが多く、アマチュアが作成したXG対応のMIDIデータはMU80準拠の作品が多く見受けられた。

### XG音源の拡張機能を使用したステップアップしたシステムの提唱（1996年）

[1996年](../Page/1996年.md "wikilink")夏に、ヤマハは[物理モデル音源](../Page/物理モデル音源.md "wikilink")モジュール[VL70-m](https://ja.wikipedia.org/wiki/ヤマハ・VL/VPシリーズ "wikilink")、ピアノサウンド音源モジュール[P50-mを発売](../Page/ヤマハ・Pシリーズ.md "wikilink")。前年暮れに発売のハンディーサンプラー[SU10とVL](https://ja.wikipedia.org/wiki/ヤマハ・SUシリーズ "wikilink")70-m、P50-mをMU80またはMU50と組み合わせて、ステップアップする方法を提示する。しかし、音源1台完結の利用方法に慣れていたユーザからはこのステップアップ方法は十分に受け入れられたとは言えなかった（同時期AKAIが、DTM音源モジュールとピアノ専用音源モジュール、アナログシンセ音をサンプリングした音源モジュールの組み合わせのセッティングを提示し、またローランドもピアノ専用音源モジュール、ハンディーサンプラーとの組み合わせのセッティングを提示するが、同様に普及しなかった）。

### MU90の登場（1996年）

[1996年](../Page/1996年.md "wikilink")末に、MU80で不十分だったMU50の上位互換性を確保した[MU90が発売された](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")。MU90ではインサーションエフェクトやEQなどエフェクト面でMU80から大幅なバージョンアップをし、またダンス系のドラムキットやシンセリード、シンセベース、オーケストラヒットなどのサウンドを新たに収録して、当時大ヒット中の[小室ファミリー](https://ja.wikipedia.org/wiki/小室ファミリー "wikilink")の曲を簡単に再現可能にしていた。しかし、MU90の発売と同時に、DTM専門誌『[DTMマガジン](https://ja.wikipedia.org/wiki/DTMマガジン "wikilink")』誌上でMU90の上位機種として[MU100Rが](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")夏発売予定と掲載されたため、従来のMU80ユーザーがMU90への買い換えを控えるようになってしまった。

### MU100の登場（1997年）

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")夏発売のMU100は、MU80以来の基本音色を新たにサンプリングし直した音色に差し替えたMU100 Nativeモードを持ち、また、拡張ボードで[物理モデル音源](../Page/物理モデル音源.md "wikilink")やフォルマント・シンギング音源と呼ばれる人の声を合成して歌うことが可能な音源を追加可能とした画期的なモデルであった。同時期のGS音源SC-88Proと熾烈なシェア獲得合戦を演じ、『DTMマガジン』誌上でもこの2機種の「対決」が掲載されていた。MU100より先行して発表されていた1Uフルラックマウント版MU100RはMU100が1枚のところを、2枚拡張ボード追加可能で人気機種となった。

[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")当時のカタログを見ると、ヤマハはMU90をXGの第2世代のベーシックモデル、MU100を第2世代のハイエンドモデルにしようとしていたことが伺える。ヤマハはMU50同様MU90互換の他モデルを発売する。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")にMU90と完全互換のXG音源を持つ[ワークステーションタイプのシンセサイザー](https://ja.wikipedia.org/wiki/ミュージックワークステーション "wikilink")[EOS B2000と](../Page/ヤマハ・EOSシリーズ.md "wikilink")、MU90からインサーションエフェクトを割愛したシンセサイザー[CS2xがそれである](https://ja.wikipedia.org/wiki/ヤマハ・CSシリーズ "wikilink")。しかし、前述のMU80からMU90への買い換えが進まなかったせいで、実際はMU90でなく[MU100が第](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")2世代のXGの標準機となる。

### MU128の登場（1998年）

MU90シリーズは32パート、最大同時発音数64音、同じくMU100シリーズも32パート、最大同時発音数64音であったため、音色以外のハード面では性能は大差がない。このこともMU90シリーズが普及しなかった理由の一つであった。[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")初頭にMU100シリーズの廉価版、[MU100Bが発売され](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")、同年7月にMU100Rを超えるハイエンドモデルとして[MU128が発売されたことで](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")、MU100がXGの名実共にベーシックモデルとなり、MU90はディスコンとなってしまった（同時期に同じことをローランドがSC-88ProとSC-88VLでしようとしていたが、結局SC-88ST ProやSK-88ProというSC-88Proの互換品を出し、SC-88VLをディスコンとした）。また、[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")初頭に、基本的なXGフォーマットとTG300-Bモードに対応したサウンドLSI,YMF724が発表され、各社パソコンや[サウンドカード](../Page/サウンドカード.md "wikilink")に採用されたことで、一般層にもある程度の普及をみた。

### MU2000・MU1000・MU500の登場（1999年末～2000年）

[1999年](../Page/1999年.md "wikilink")12月にMU128のGM2に対応するなど、改良タイプとして[MU2000を発売](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")。同年11月にMU2000に先行する形で、それからサンプリング機能や[スマートメディア](../Page/スマートメディア.md "wikilink")スロットを省略した[MU1000を発売](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")。翌[2000年](../Page/2000年.md "wikilink")8月にはMU1000からディスプレイやボタン類を省略し、最大同時発音数を128から64にした[MU500を発売する](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")。この間に第2世代のベーシックモデルだったMU100シリーズはディスコンとなり、MU2000がハイエンドモデル、MU500がベーシックモデルという第3世代に移る。その後、中間に挟まれたMU1000はディスコンとなった（以前のMU90とMU100のケースと同様に同じ64パート最大同時発音数128の機器同士で競合したからと思われる）。

### Hello\!Music\!Audioの登場とその後（2000年以後）

同梱シーケンス・ソフトをSOL（後にSOL2へとバージョンアップされた）に変更し、MU2000 Extended Edition、MU500とUSBオーディオインターフェイスUW500を同梱したパッケージ『Hello\!Music\!Audio』が発売された。

MU2000の単体品もMU1000に続き、生産完了するが、MU2000は[MOTIFシリーズ直系のエフェクト装備やGS対応のExtended](https://ja.wikipedia.org/wiki/ヤマハ・MOTIFシリーズ "wikilink") Editionにアップグレードされ、DTMパッケージ『Hello\!Music\!Audio』の同梱音源として販売されていた。

しかし、MU500以降（マイナーチェンジを含めるとMU2000 Extended Edition以降）、MUシリーズの新製品は発表されていない。その間に、ヤマハはプロユースのシンセサイザー[ヤマハ・MOTIFシリーズ](https://ja.wikipedia.org/wiki/ヤマハ・MOTIFシリーズ "wikilink")シリーズがヒットし、そのシリーズの製品を多数発表している。時代の趨勢もDTMから[デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")(DAW)へと変わりつつある。ヤマハが主催するXGコンテストも終了し、ヤマハのXG専用のホームページが[2004年](../Page/2004年.md "wikilink")3月に終了し、シンセサイザーのホームページと統合されている。[S03やMDP](https://ja.wikipedia.org/wiki/ヤマハ・Sシリーズ "wikilink")-5などXG対応の機種も[2001年](../Page/2001年.md "wikilink")以降に発売されたが、95年から99年頃までのリリースラッシュの勢いがない。さらに2008年には『Hello\!Music\!』シリーズの終焉を迎え、現行の音楽制作用途のXG音源搭載機種はMU500を残すのみとなった。一方、音楽制作用途以外の製品に関しては、XGデータ再生に対応した電子ピアノやキーボードなどが現在でも継続的にリリースされている。

## XG Editor

XG Editorは、XG音源の各種パラメーターをPC上で操作するためのエディターである。ヤマハ製DAWソフトの[XGworks](../Page/XGworks.md "wikilink")シリーズおよびSOLシリーズに搭載されている。MUシリーズをはじめ、PC用サウンドカード、電子ピアノ、ポータトーン、エレクトーン、ソフトシンセ版にいたるまで過去にXG音源方式を搭載した機種の相当数を対応音源として網羅している。また、[プラグインボードで拡張された機能にも対応している](https://ja.wikipedia.org/wiki/Modular_Synthesis_Plug-in_System "wikilink")。

ヤマハがサポートするDAWソフトが[スタインバーグ](https://ja.wikipedia.org/wiki/スタインバーグ "wikilink")社の[Cubase](../Page/Cubase.md "wikilink")シリーズに移行したことに伴い、2008年9月、XG EditorのCubaseシリーズ対応版である「XG Editor for Cubase」が公開された。ヤマハwebサイトにて無償ダウンロード可能。

## 関連記事

  - [MIDI](../Page/MIDI.md "wikilink")
  - [デスクトップミュージック](../Page/デスクトップミュージック.md "wikilink")
  - [デジタルオーディオワークステーション](https://ja.wikipedia.org/wiki/デジタルオーディオワークステーション "wikilink")
  - [GM](https://ja.wikipedia.org/wiki/General_MIDI "wikilink")
  - [GS](https://ja.wikipedia.org/wiki/GSフォーマット "wikilink")
  - [ヤマハ・MUシリーズ](https://ja.wikipedia.org/wiki/ヤマハ・MUシリーズ "wikilink")
  - [ヤマハ・CBXシリーズ](../Page/ヤマハ・CBXシリーズ.md "wikilink")
  - [HELLO\!MUSIC\!](../Page/HELLO!MUSIC!.md "wikilink")
  - [XGworks](../Page/XGworks.md "wikilink")

## 外部リンク

  - [YAMAHA : XG Creation Without Limitation](https://web.archive.org/web/20090508141107/http://www.yamaha.co.jp/product/syndtm/read/aoyama/) - XGフォーマットの仕様書が閲覧できる

## 脚注

[Category:ヤマハ](https://ja.wikipedia.org/wiki/Category:ヤマハ "wikilink") [Category:MIDI](https://ja.wikipedia.org/wiki/Category:MIDI "wikilink")

1.  <https://jp.yamaha.com/files/download/other_assets/6/321756/xgsongdata.pdf>