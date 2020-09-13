> この記事は[AAC](https://ja.wikipedia.org/wiki/AAC)から翻訳されています。


**Advanced Audio Coding**（略称: **AAC**、先進的音響符号化）は、不可逆のデジタル[音声圧縮](../Page/音声圧縮.md "wikilink")を行う音声符号化規格のひとつである。[1997年](https://ja.wikipedia.org/wiki/1997年 "wikilink")に[ISO/IEC JTC 1の](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")[Moving Picture Experts Group](../Page/Moving_Picture_Experts_Group.md "wikilink") (MPEG) において規格化された。[MP3](../Page/MP3.md "wikilink")の後継フォーマットとして策定され、一般的にAACは同程度のビットレートであればMP3より高い音声品質を実現している。

AACは[ISOと](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")[IECにより](../Page/国際電気標準会議.md "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")および[MPEG-4](../Page/MPEG-4.md "wikilink")仕様の一部として標準化された。MPEG-4 Audio内の[HE-AAC](../Page/HE-AAC.md "wikilink")として知られるAACの一部は、[DAB](../Page/DAB.md "wikilink")+や[Digital Radio Mondiale](../Page/デジタル・ラジオ・モンディエール.md "wikilink")、モバイルテレビジョン規格の[DVB](../Page/デジタルビデオブロードキャスティング.md "wikilink")-や[ATSC-M/Hのようなデジタル無線規格においても採用されている](https://ja.wikipedia.org/wiki/ATSC#ATSC-M/H "wikilink")。

AACは一つのストリームに、48の全帯域幅（最大96kHz）音声チャンネルを持たせることができ、さらに、16の低周波効果音（LFE、120Hzまで）チャンネルと16の対話チャンネル、および16のデータストリームも含めることができる。ステレオの音質は96kbpsのジョイントステレオモードで適度な要件を満たすことができるが、[Hi-Fi](../Page/Hi-Fi.md "wikilink")透明性（低雑音性）のためには、少なくとも128kbpsのデータレート([VBR](https://ja.wikipedia.org/wiki/VBR "wikilink"))が必要である。MPEG-4 Audioによる検証では、AACが128kbpsのステレオおよび320kbpsの5.1チャンネルオーディオにおいて[ITUが](../Page/国際電気通信連合.md "wikilink")「透明的」として規定している要件を満たしていることが示されている。

AACは[YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")、[iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink")、[iPod](https://ja.wikipedia.org/wiki/iPod "wikilink")、[iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")、[Nintendo DSi](https://ja.wikipedia.org/wiki/Nintendo_DSi "wikilink")、[Nintendo 3DS](https://ja.wikipedia.org/wiki/Nintendo_3DS "wikilink")、[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")、[DivX](https://ja.wikipedia.org/wiki/DivX "wikilink") Plus Web Player、[PlayStation 3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink")、[ノキア](../Page/ノキア.md "wikilink")のSeries 40携帯電話における既定もしくは標準の音声フォーマットである。[PlayStation Vita](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink")、[Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")、 [ソニー](../Page/ソニー.md "wikilink")の[ウォークマン](../Page/ウォークマン.md "wikilink")MP3シリーズとその後継機種でもサポートされている。AACはインダッシュの車載オーディオシステムのメーカによってもサポートされている。

## 概要

[MP3](../Page/MP3.md "wikilink")等の[MPEG-1 Audioや](https://ja.wikipedia.org/wiki/MPEG-1#オーディオ "wikilink")、[MPEG-2 Audio BC (Backward Compatible)](https://ja.wikipedia.org/wiki/MPEG-2#オーディオ "wikilink") を超える高音質・高圧縮を目的に標準化された方式である。

MPEG-2 Audio BCとは異なり、[符号化](https://ja.wikipedia.org/wiki/符号化 "wikilink")[アルゴリズム](../Page/アルゴリズム.md "wikilink")においてMPEG-1 Audioとの互換性はない。ファイルに格納した場合の[拡張子](../Page/拡張子.md "wikilink")は、「\*.mov,\*.mp4,\*m2ts,\*.m4a,\*.m4b,\*.m4p,\*.3gp,\*.3g2」または「\*.aac」。なお、放送ではADTS (Audio Data Transport Stream) と呼ばれるヘッダ形式で伝送されることが多い。[サンプリング周波数](../Page/サンプリング周波数.md "wikilink")はMP3が最大48kHzまでだったのに対し、AACは最大96kHzまで対応している。

## 種類

### MPEG-2 AACとMPEG-4 AAC

AACには[MPEG-2](../Page/MPEG-2.md "wikilink") AAC (ISO/IEC 13818-7) と[MPEG-4](../Page/MPEG-4.md "wikilink") AAC (ISO/IEC 14496-3, Subpart 4) とが存在する。MPEG-4 AACは、MPEG-2 AACにPNSやLTPといった追加技術を利用可能としたものであるが、基本的なアルゴリズム自体に違いはなく、追加技術を使用しなければヘッダの一部分が1ビット異なるだけであり、通常の使用では区別する必要はほとんどない。

  - PNS (Perceptual Noise Substitution)
    [PNS](https://ja.wikipedia.org/wiki/PNS "wikilink")は、エンコード時に低減されたノイズを記録する追加技術である。
  - LTP (Long Term Prediction／長期予測)
    LTPは、低周波帯域の波形を記録する追加技術である。

### AACプロファイルと追加技術

#### プロファイル

AACにも拡張機能が使用可能かどうかによって幾つかの種類があるが、一般的に利用されているのは**AAC-LC** (AAC Low Complexity) と呼ばれる基本機能だけを用いるものである。

  - MPEG-2/4 AAC-Main
    メインのAACとして開発された方式。AAC-LCと比べると、圧縮率は高いものの再生負荷が大きい。
  - MPEG-2/4 AAC-LC (Low Complexity)
    AAC-Mainから後方予測 (backward prediction) の機能を除いた方式。
  - MPEG-2/4 AAC-SSR (Scalable Sample Rate)
    周波数によって4つのブロックに分解し、それぞれを符号化する方式。

さらにMPEG-4 AAC-LTP（後述）をプロファイルに数える場合がある。

#### 追加技術

MPEG-4 AAC v3においては、[SBR](https://ja.wikipedia.org/wiki/Spectral_Band_Replication "wikilink") (Spectral Band Replication) や[パラメトリックステレオ](https://ja.wikipedia.org/wiki/MPEG-4_Part_3#パラメトリックオーディオ符号化 "wikilink") (Parametric Stereo) 技術によって64 kbpsを下回るような超低ビットレートにおける品質を改善する**[HE-AAC](../Page/HE-AAC.md "wikilink")** (High-Efficiency AAC) が追加承認されている (AAC-LC, HE-AAC (aacPlus, AAC+SBR), HE-AAC Version 2 (aacPlus Version 2, Enhanced aacPlus, AAC+SBR+PS))。

  - MPEG-2/4 HE-AAC (High-Efficiency AAC)
    AAC-LCにSBRの機能を追加したもの。SBRは高周波域の波形を補完するツールである。SBRを利用することで低ビットレートでも中～高音質の再生を可能としている。
    バージョン2が開発されて以降、区別のため、名前の後ろに”version 1”などを附ける場合がある。
  - MPEG-2/4 HE-AAC v2 (High-Efficiency AAC version 2)
    AAC-LCにSBRとPSの機能を追加したもの。PS (Parametric Stereo) はモノラルの音声を擬似的にステレオに復元するツールであり、HE-AACよりもさらに低いビットレートで中 - 高音質の再生を行えるようにする。
  - MPEG-4 xHE-AAC (eXtended High-Efficiency AAC)
    AAC-LCにSBRとPS、USACの機能を追加したもの。USAC (Unified Speech and Audio Coding) は声と音楽のどちらの音質にも重きが置かれるよう作られたツールであり、HE-AAC v2より低いビットレートでもある程度の音質が確保される。
  - MPEG-4 AAC-LTP
    AACにLTPの機能を追加したもの。LTPはすべてのMPEG-4 AACに付加することが可能である。
  - MPEG-4 AAC-LD (Low Delay)
    エンコードなどによる延滞時間を減少させたAAC。テレビ電話などで使用することを目的としている。
  - MPEG-4 AAC-ELD (Enhanced Low Delay)
    MPEG-4 AAC-ELD v2 (version 2)
    AAC-LDを改良した方式。

## 利用状況

MPEG-2 AACは主に日本の[BS/110度CS 2Kデジタル放送と](../Page/衛星放送.md "wikilink")[地上デジタル波放送の](../Page/デジタル放送の一覧.md "wikilink")[ISDB](../Page/ISDB.md "wikilink")規格や[SD-Audio](../Page/SD-Audio.md "wikilink")のAACフォーマット、ヨーロッパ圏の[DVD](../Page/DVD.md "wikilink")などで利用できる。北米や日本のDVDでは、AACではなく[AC-3や](../Page/ドルビーデジタル.md "wikilink")[DTSが採用されている](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink")。

MPEG-4 AACはiPodなどの[デジタルオーディオプレーヤー](../Page/デジタルオーディオプレーヤー.md "wikilink")、[PlayStation Portableや](../Page/PlayStation_Portable.md "wikilink")[DSiなどのゲーム機](https://ja.wikipedia.org/wiki/ニンテンドーDSi "wikilink")、日本のBS/110度CS 4K/8Kデジタル放送、[携帯電話](../Page/携帯電話.md "wikilink")等、多くの機器やソフトウェアがサポートしている。また、第三世代携帯電話用の動画フォーマットである[3GPP](../Page/3GPP.md "wikilink")や[3GPP2](../Page/3GPP2.md "wikilink")の[音声圧縮](../Page/音声圧縮.md "wikilink")方式としても採用されている。

音楽配信サービスでは、パソコン、iPod向けの**[iTunes Store](https://ja.wikipedia.org/wiki/iTunes_Store "wikilink")**や携帯電話向けの**[着うた](../Page/着うた.md "wikilink")**でAACが採用されている。ただし、これらのファイルの一部には[DRMが導入され](../Page/デジタル著作権管理.md "wikilink")、同じAACであるが互換性がないものがある\[1\]。デジタルオーディオプレーヤーの代表格であるiPodおよびiTunes（標準でAACを使用する）がAACに対応していることもあり、以前はAACに対応していなかったソニーや[パナソニック](https://ja.wikipedia.org/wiki/パナソニック "wikilink")、[ケンウッド](../Page/ケンウッド.md "wikilink")（現・[JVCケンウッド](https://ja.wikipedia.org/wiki/JVCケンウッド "wikilink")）などのデジタルオーディオプレーヤーも現在ではAACに対応している。

またアップルでは前述のiTunesでの音楽配信のほか、ワイヤレスイヤホンマイク[AirPods](https://ja.wikipedia.org/wiki/AirPods "wikilink")・[スマートスピーカー](https://ja.wikipedia.org/wiki/スマートスピーカー "wikilink")[HomePod](https://ja.wikipedia.org/wiki/HomePod "wikilink")や、[FaceTime](https://ja.wikipedia.org/wiki/FaceTime "wikilink")(AAC-ELD系)\[2\]などで使用している。

## 符号化アルゴリズム

AAC (AAC-LC) の符号化処理は以下の流れで行われる。

1.  [MDCTによる](https://ja.wikipedia.org/wiki/修正離散コサイン変換 "wikilink")[直交変換](../Page/直交行列.md "wikilink")
      - 入力は窓長 2048 もしくは 256 のMDCTを用いてそれぞれ 1024 点 (long block)、128 点 (short block) の[周波数領域](../Page/周波数領域.md "wikilink")のデータに変換される。MP3が一旦時間領域のフィルタで 32 サブバンドに分割した後にMDCTを行っていたのに対し、AACでは入力サンプルに対してそのままMDCTが行われる。
      - 変換長は、入力信号の性質によって切り替えられる（アタック音など時間領域で急峻な変化を見せる信号にはshort blockが使われる）。long blockが576点相当（32 サブバンド × 18 点）、short blockが 192 点相当（32 サブバンド × 6 点）であったMP3と比較してlong blockをより長くすることで周波数解像度の向上による符号化効率の改善がshort blockをより短くする事で時間解像度の向上によるプリエコー抑制力の改善がなされている。
2.  TNS
      - 周波数領域の信号を、時間軸のものと見なした[線形予測を行う](https://ja.wikipedia.org/wiki/線形予測法 "wikilink")。
      - 周波数領域での[ARモデル](https://ja.wikipedia.org/wiki/ARモデル "wikilink")化は[時間領域](../Page/時間領域.md "wikilink")でのノイズ特性を持ち、人間の聴覚の持つ継時マスキング特性を再現するのに都合が良い。
      - この処理は省く事ができる。
3.  ステレオ・コーディング
      - 入力信号がステレオの場合は、ステレオ特有の性質を利用した符号化が行われる。
      - なおステレオ・コーディングはサブバンド毎に利用しなかったり、どちらか片方だけを利用したりすることができる。両方同時に使用することはできない。
    <!-- end list -->
    1.  インテンシティ・ステレオ
          - 左右の信号を、単一の信号と定位情報のみに削減して符号化する。
    2.  MSステレオ
          - 左右の信号を和／差信号とする。
4.  [量子化](https://ja.wikipedia.org/wiki/量子化 "wikilink")
      - 聴覚心理モデルで決定した許容[量子化雑音](https://ja.wikipedia.org/wiki/量子化雑音 "wikilink")エネルギーと量子化雑音エネルギーが比例するようにスケールファクタ・バンド（近い周波数のMDCT係数をまとめたグループ）毎に量子化を行う。long blockのスケールファクタ・バンドの数は49 (44.1kHz) であり、21 であったMP3と比較して細かい制御が可能になっている。
5.  [ハフマン符号](../Page/ハフマン符号.md "wikilink")化
      - 量子化された値を固定ハフマン符号化する。符号帳は 11 種類の中からサブバンド毎に選択される。

## コンテナ対応

  - [AVI](../Page/Audio_Video_Interleave.md "wikilink"), [MOV](../Page/QuickTime.md "wikilink"), [MP4](../Page/MP4.md "wikilink"), [Matroska](../Page/Matroska.md "wikilink"), [MPEG-2 TS](https://ja.wikipedia.org/wiki/MPEG-2システム#トランスポートストリーム "wikilink")

## 備考

AACは[ドルビーラボラトリーズ](../Page/ドルビーラボラトリーズ.md "wikilink")も共同開発の一員で、AACロゴはドルビーラボラトリーズの登録商標である（日本国特許庁商標登録番号：第4693750号）。AACにはドルビーのほか[AT\&T](../Page/AT&T.md "wikilink")、[Fraunhofer IIS](https://ja.wikipedia.org/wiki/フラウンホーファー協会 "wikilink")、[ソニー](../Page/ソニー.md "wikilink")、[ノキア](../Page/ノキア.md "wikilink")の特許技術が使用されている\[3\]ためソフトウェアメーカーなどから納付されたライセンス料はこれらの企業に分配されている。また、ライセンス管理はドルビーの子会社[Via Licensingが行っている](https://ja.wikipedia.org/wiki/Via_Licensing "wikilink")。

なおMPEG-4 AACが含まれるMPEG-4 AudioのカテゴリにはNTTサイバースペース研究所が開発した[TwinVQ](https://ja.wikipedia.org/wiki/TwinVQ "wikilink")が存在するが、これはAACとは別物である。

## 利用例

AACやHE-AACは下記に採用されており、実際に利用されている。

  - [Adobe Flash](../Page/Adobe_Flash.md "wikilink") Player 9 以降 - HE-AAC v2まで対応
      - [YouTube](https://ja.wikipedia.org/wiki/YouTube "wikilink")
      - [ニコニコ動画](../Page/ニコニコ動画.md "wikilink")
      - [radiko](https://ja.wikipedia.org/wiki/radiko "wikilink")
      - [NHKネットラジオ らじる★らじる](https://ja.wikipedia.org/wiki/NHKネットラジオ_らじる★らじる "wikilink")
  - [iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink"), [iTunes Store](https://ja.wikipedia.org/wiki/iTunes_Store "wikilink"), [QuickTime](../Page/QuickTime.md "wikilink"), [FaceTime](https://ja.wikipedia.org/wiki/FaceTime "wikilink")
  - [iPod](https://ja.wikipedia.org/wiki/iPod "wikilink"), [iPhone](https://ja.wikipedia.org/wiki/iPhone "wikilink"), [iPad](https://ja.wikipedia.org/wiki/iPad "wikilink")
  - [PSP](../Page/PlayStation_Portable.md "wikilink"), [PSVita](https://ja.wikipedia.org/wiki/PlayStation_Vita "wikilink"),[PS3](https://ja.wikipedia.org/wiki/PlayStation_3 "wikilink"),[PS4](https://ja.wikipedia.org/wiki/PlayStation_4 "wikilink")
  - [DSi](https://ja.wikipedia.org/wiki/ニンテンドーDSi "wikilink")（DSiサウンド）, [Wii](https://ja.wikipedia.org/wiki/Wii "wikilink")（[写真チャンネル](../Page/写真チャンネル.md "wikilink")） - v1.1から対応。
  - [Blu-ray Disc](../Page/Blu-ray_Disc.md "wikilink") ([BDAV](../Page/BDAV.md "wikilink"))
  - Bluetoothイヤホン - [AirPods](https://ja.wikipedia.org/wiki/AirPods "wikilink")など
  - [スマートスピーカー](https://ja.wikipedia.org/wiki/スマートスピーカー "wikilink") - [HomePod](https://ja.wikipedia.org/wiki/HomePod "wikilink"), [Google Home](https://ja.wikipedia.org/wiki/Google_Home "wikilink"), Google Home対応スピーカーの一部機種
  - [地上デジタル放送](https://ja.wikipedia.org/wiki/地上デジタルテレビジョン放送 "wikilink")
  - [BSデジタル放送](../Page/デジタル放送の一覧.md "wikilink")
  - [スカパー\!プレミアムサービス](../Page/スカパー!プレミアムサービス.md "wikilink")
  - [着うたフルプラス](https://ja.wikipedia.org/wiki/着うたフルプラス "wikilink") - [KDDI](../Page/KDDI.md "wikilink")および[沖縄セルラー電話](../Page/沖縄セルラー電話.md "wikilink")の一部の[au携帯電話向け音楽配信サービス](../Page/Au_\(携帯電話\).md "wikilink")。
  - [SD-Audio](../Page/SD-Audio.md "wikilink")
  - [Liquid Audio](https://ja.wikipedia.org/wiki/リキッドオーディオジャパン "wikilink")
  - [Nero Digital](https://ja.wikipedia.org/wiki/Nero_Digital "wikilink")
  - [mora](https://ja.wikipedia.org/wiki/mora "wikilink") - ソニーグループの音楽配信サービス。2012年10月よりAACによる配信を開始（それ以前は[ATRAC](../Page/ATRAC.md "wikilink")3による配信）。

## 脚注

<references />

## 関連項目

  - [ウォークマン](../Page/ウォークマン.md "wikilink")
  - [D-snap](../Page/D-snap.md "wikilink")
  - [Zune](../Page/Zune.md "wikilink")
  - [FairPlay](../Page/FairPlay.md "wikilink") - [デジタル著作権管理](../Page/デジタル著作権管理.md "wikilink")技術
  - [日本における衛星放送](../Page/日本における衛星放送.md "wikilink")
  - [MP4](../Page/MP4.md "wikilink")
  - [データ圧縮](../Page/データ圧縮.md "wikilink")
  - [RealAudio](../Page/RealAudio.md "wikilink")
  - [SD-Audio](../Page/SD-Audio.md "wikilink")
  - [D-dock](../Page/D-dock.md "wikilink")

## 外部リンク

### 解説サイト

  - [AudioCoding.com](http://www.audiocoding.com/)
  - [AAC関連ツール (RareWares)](http://www.rarewares.org/aac.html)
  - [アップル AACオーディオ](http://www.apple.com/jp/mpeg4/aac)
  - [GUIで作るAAC音声のOGM・MKV（妖精現実フェアリアル）](http://www.faireal.net/dat/d3/d30917a.xml)
  - [Broadband Watch--BBっとWORDS 「AACの特徴」](http://bb.watch.impress.co.jp/cda/bbword/16246.html)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:非可逆圧縮アルゴリズム](https://ja.wikipedia.org/wiki/Category:非可逆圧縮アルゴリズム "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink")

1.  例えばiTunes Storeでは以前、拡張子が .m4p のAACが配信フォーマットとして用いられていたが、これにはiTunes Store独自の[FairPlay](../Page/FairPlay.md "wikilink")というDRMが付加されていたため携帯電話で再生することができなかった。2009年にはiTunes Storeにおいて大半の曲がDRMフリーでリリースされた。ただし一部のメタ情報やデータコンテナの相違から、そのままのオーディオファイルを使用する場合に非互換性が残る場合がある。
2.  海上忍「いまさら聞けないiPhoneのなぜ [格安SIMでもFaceTimeオーディオは快適に使える?](https://news.mynavi.jp/article/20160125-iphone_why/)」『マイナビニュース』 マイナビ、2016年1月25日
3.