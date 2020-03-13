> この記事は[Vorbis](https://ja.wikipedia.org/wiki/Vorbis)から翻訳されています。


**Vorbis**（ヴォルビス、ヴォービス）は、[Xiph.org](https://ja.wikipedia.org/wiki/Xiph.org "wikilink")が開発した[オープンフォーマット](../Page/オープンフォーマット.md "wikilink")の[非可逆圧縮](../Page/非可逆圧縮.md "wikilink")[音声ファイルフォーマット](../Page/音声ファイルフォーマット.md "wikilink")。

## 概要

広く使われている[MP3](../Page/MP3.md "wikilink")などのフォーマットは[特許](../Page/特許.md "wikilink")の制限を受けるため、それらの代替として誰でも自由につかえる圧縮音声フォーマットを提供することを目指して作られた。仕様は[パブリックドメイン](../Page/パブリックドメイン.md "wikilink")、核となる[エンコード](../Page/エンコード.md "wikilink")・デコードの[リファレンスコードは修正版](../Page/リファレンス実装.md "wikilink")[BSDライセンス](https://ja.wikipedia.org/wiki/BSD_License "wikilink")、[フロントエンド](../Page/フロントエンド.md "wikilink")ツール類は[GPLで提供されている](../Page/GNU_General_Public_License.md "wikilink")。また、[特許](../Page/特許.md "wikilink")使用料も不要。

Vorbisは主に[Ogg](../Page/Ogg.md "wikilink")コンテナフォーマットに格納され、Ogg Vorbisと呼称される。単に[Ogg](../Page/Ogg.md "wikilink")といった場合は、他に[FLAC](../Page/FLAC.md "wikilink")を格納したOgg FLAC、[Speex](../Page/Speex.md "wikilink")を格納したOgg Speex、動画コーデックの[Theora](../Page/Theora.md "wikilink")を格納したOgg Theoraなどがある。 また、VorbisはOgg用に開発されたコーデックなので当初はOggのみにしか格納できなかったが、後に[Matroska](../Page/Matroska.md "wikilink")が対応した。Matroskaに格納したVorbisはMatroska Vorbisであって、Ogg Vorbisではない。

2010年には、[Google](../Page/Google.md "wikilink")が開発しているオープンなコンテナフォーマット[WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")の音声コーデックとして採用された。

[拡張子](../Page/拡張子.md "wikilink")は.ogg、まれに.ogaが使われる。.oggはかつての[Ogg](../Page/Ogg.md "wikilink")共通の拡張子であったが、現在それは公式には.ogxに変更されており、.oggは互換性のためにOgg Vorbis用の拡張子として残された。.ogaは、音声コーデックのみを格納した[Ogg](../Page/Ogg.md "wikilink")共通の拡張子である。

これらはXiph.orgによって[規格](https://ja.wikipedia.org/wiki/規格 "wikilink")化されている。[Ogg](../Page/Ogg.md "wikilink")コンテナフォーマットは[RFCで正式に文書化されている](../Page/Request_for_Comments.md "wikilink")\[1\]。

## 要項

  - [VBR](../Page/可変ビットレート.md "wikilink")、[ABR](https://ja.wikipedia.org/wiki/可変ビットレート#平均ビットレート（ABR） "wikilink")、[CBRをサポート](https://ja.wikipedia.org/wiki/固定ビットレート "wikilink")（[CBRは](https://ja.wikipedia.org/wiki/固定ビットレート "wikilink")[MP3](../Page/MP3.md "wikilink")のようなフレーム単位の方式ではない）
  - [オープンソース](../Page/オープンソース.md "wikilink")
  - [パテントフリー](../Page/特許.md "wikilink")
  - 拡張性が高い
  - [MP3](../Page/MP3.md "wikilink")などより音質が良いとされる
  - ギャップレスデコードに標準で対応

## 仕様

  - アルゴリズム : MDCT（Modified Discrete Cosine Transform：[修正離散コサイン変換](https://ja.wikipedia.org/wiki/修正離散コサイン変換 "wikilink")）
    [サンプリング周波数](../Page/サンプリング周波数.md "wikilink") : 8kHz - 192kHz (Typical rate)
    チャンネル数 : 1ch(mono), 2ch(stereo), 4ch, [5.1ch](../Page/ドルビーデジタル.md "wikilink"), 6.1ch（最大255ch）
    ビットレート : 平均32kbps([aoTuV](https://ja.wikipedia.org/wiki/aoTuV "wikilink") Q-2 mode), 平均45kbps(Q-1)～平均500kbps(Q10) (44.1kHz ステレオソース時)
    チャンネルカップリング : ステレオモード時のみ対応（それ以上のモードに対応したエンコーダが現状無い）
    ビットレート制限 : エンコーダに依存
    MIME Type : application/ogg, application/x-ogg, application/x-vorbis
    ストリーミング : 対応（プレイヤー側の対応が必要）
    チェックサム : 対応（デフォルトで有効）
    コピーガード : 未対応
    タグ情報 : Vorbis Comment ([UTF-8](../Page/UTF-8.md "wikilink"))（一般的なID3タグには未対応）
    コンテナ対応 : [Matroska](../Page/Matroska.md "wikilink") ([WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")), [MOV](../Page/QuickTime.md "wikilink"), [MP4](../Page/MP4.md "wikilink"), [Ogg](../Page/Ogg.md "wikilink"), [OGM](../Page/Ogg_Media.md "wikilink") （[AVI](../Page/Audio_Video_Interleave.md "wikilink"), [WAV](../Page/WAV.md "wikilink")は互換性に難有り）
    ギャップレスデコード : 対応（プレイヤー側の対応が必要）
    ギャップレス再生 : 対応（プレイヤー側の対応が必要）

## 特徴

### 長所

  - Vorbisは全てのビットレート域で既存コーデック（MP3）を超えるべく設計されている。現状の実装では、同レートのMP3より音質が良く、LC-[AAC](../Page/AAC.md "wikilink")と同列もしくはそれ以上とされる。[HE-AAC](../Page/HE-AAC.md "wikilink")や[HE+PS-AAC](https://ja.wikipedia.org/wiki/HE+PS-AAC "wikilink")が得意とする32-48kbps周辺の低ビットレート域では、特許が使用できないために高域疑似補完技術（[Spectral Band Replication](https://ja.wikipedia.org/wiki/Spectral_Band_Replication "wikilink")）やステレオ疑似補完技術（[Parametric Stereo](https://ja.wikipedia.org/wiki/w:en:Parametric_Stereo "wikilink")）の実装ができないVorbisは、善戦しつつも不利とされる。
    標準[ビットレートは](../Page/ビット毎秒.md "wikilink")112kbpsで、この時の音質は、多くの人が[CDもしくは圧縮前の音源とほとんど聞き分けがつかないとされる](../Page/コンパクトディスク.md "wikilink")。
    圧縮率の指定は通常、クオリティレベルと呼ばれる数値で指定し、範囲は-1から10までの範囲である。44.1kHz Stereo(2ch)のソースの場合、標準はQ3(112kbps)となっており、最大ではQ10(500kbps)、最低のQ-1では48kbpsとなる（aoTuVエンコーダーではそれ以下のQ-2を指定でき、32kbpsでエンコードできる）。
  - かつてはエンコード速度の遅さが指摘されていたが、Ogg Vorbis 高速化プロジェクトにより大きく改善されている。音質の点では、拡張性の高さを生かして幾重にもチューニングを施した[aoTuV](https://ja.wikipedia.org/wiki/aoTuV "wikilink")が長きにわたって高い評価を得ており\[2\]、オフィシャルエンコーダのlibvorbisにも一部組み込まれた。Xiph.orgのVorbis開発の歩みが緩やかになっている現状において、Vorbisが企業の開発するLC-[AAC](../Page/AAC.md "wikilink")等のコーデックに伍する品質を保つことができているのは、こうしたXiph以外の開発者の努力に負うところも大きい。[サラウンド](../Page/サラウンド.md "wikilink")（マルチチャンネル）に関しては比較的使われていないこともあり、Vorbisにおいて注力されてこなかった分野だが、libvorbis 1.3.1ではサラウンド・チャンネルカップリングが実装され、5.1chの品質が向上したとされる。
  - Vorbisは標準でギャップレスデコードに対応している。ライブやダンスミュージック等といった、曲間のギャップが問題になるソースにおいて利点がある他、動画の音声として利用した場合でも映像と音声の同期ズレの原因とならない等の利点がある。Vorbisはプログラムからはサンプル単位で位置を指定して正確にデコードできるため、ライセンス料フリーであることもあって、[パソコンゲーム](../Page/パソコンゲーム.md "wikilink")などで多数採用されている実績がある\[3\]。
    ちなみに主要な音声非可逆圧縮で、ギャップレスデコードにフォーマットレベルで対応しているのは、Vorbisのみである。MP3とAACとMusepackはエンコーダーの独自拡張によってギャップレス情報を埋めこむことで擬似的に対応しているため、デコーダーも各独自拡張に対応している必要がある。ただし、Vorbisにおいても携帯プレイヤーなどではデコーダ側の実装問題でギャップレス再生できないことも多い。

### 短所

  - Vorbisは可変ビットレートが基本のため、[AVIなどのVBR音声コーデックを想定していないコンテナでの使用は](../Page/Audio_Video_Interleave.md "wikilink")、音がずれるなどの問題が生じる場合があり、OggコンテナやMatroskaコンテナなどを使用する必要がある。
  - VorbisはMP3より複雑な処理をする必要があるため、オフィシャルエンコーダの速度は比較的遅い傾向にある。
      - Ogg Vorbis 高速化プロジェクトのライブラリを使用することで、環境によってはオフィシャルより2～3倍、又はそれ以上速くなる\[4\]。
      - ただし、現状のリファレンスエンコーダではABRエンコード（ビットレート指定エンコード）の際には、クオリティ指定エンコードの2倍以上の時間がかかる。これは、現状のABRエンコーディングの実装に由来するものである。
      - 近年のハードウェアの進歩により、昔に比べるとエンコードの速度は問題とされなくなってきている。
  - 対応プレイヤーが少ない
      - Vorbisに対応している携帯プレイヤーは[iriver](https://ja.wikipedia.org/wiki/iriver "wikilink")や[Cowon](../Page/Cowon.md "wikilink")などの韓国メーカーのものがほとんどで、全体のシェアからすれば数は少なく、その点ではデファクトスタンダードである[MP3](../Page/MP3.md "wikilink")や、大企業の後押しのある[Windows Media Audio](../Page/Windows_Media_Audio.md "wikilink")、[AAC](../Page/AAC.md "wikilink")に大きく及ばない。この状況はハイレゾ対応携帯プレイヤーでも変わらない。ただし、[Rockbox](../Page/Rockbox.md "wikilink")に対応している携帯プレイヤーに導入すれば、Vorbisを再生することは可能となる。
      - [Android](../Page/Android.md "wikilink") OSはVorbisのデコーダを内蔵しており\[5\]、その端末の急速な拡大によって再生環境の普及という面は改善されつつある。一方、iOSはOgg Vorbisには対応していないので、対応するソフトウェアをインストールする必要がある。
  - ユーザが自発的にエンコード環境を構築する必要がある
      - 圧倒的な普及率を誇るMP3以外の非可逆圧縮音声フォーマットで、Ogg Vorbisと比較されるものは、プロプライエタリであるWMAとAACである。WMAはWindows OSがエンコーダを内蔵するWindows Media Playerをバンドルしている。AACはMac OS Xがエンコーダを内蔵するiTunesをバンドルしている。また、Windows用iTunesもAppleが無料配布している。iPod又はiPhoneを所持する場合、iTunesは事実上必須である。すなわち、パソコンを所持していればWMAとAACは比較的容易にCDリッピングによるエンコードが可能になる。
      - 一方、Ogg Vorbisの場合、ユーザが自発的にエンコーダをネットで探してパソコンにインストールする必要がある。このようにエンコード環境と再生環境が比較的整っているWMAとAACに比べると、Ogg Vorbisはエンコード環境と再生環境が整っているとは言い難い。
      - このため、エンコード環境を構築してまでOgg Vorbisを選択して利用するユーザは、Ogg Vorbisの存在を知り、かつOgg Vorbisを自発的に使用したいという拘りを持つユーザに限られる。その拘りとは、プロプライエタリでなくパテントフリーであること等イデオロギーの次元に至る。音質に拘りを持つユーザは可逆圧縮のFLACを採用する傾向がある。非可逆圧縮音声フォーマット同士での音質比較は、サンプリングレートを上げれば殆ど目立たなくなるのであまり意味はない。

<!-- end list -->

  - デコードはMP3に比べ多くのメモリを必要とする（目安はWMA（多）とAAC（少）の中間）ため、メモリシステムが貧弱な環境ほど負荷が高くなりがちである。このことは現在のPCでは全く問題とならないが、携帯プレイヤーでは電池を多く消費してしまう原因となると言われている。
  - Vorbisはパテントフリーを謳っているが、現存する特許を全て調査することは事実上不可能であることから、いわゆる[サブマリン特許](../Page/サブマリン特許.md "wikilink")や休眠特許の類いが現れる可能性を完全に否定することはできないのではないか、といった声もある。ただし、公開から10年以上が経過しているが、現在のところ特許問題が顕在化したことはない。

### リスニングテスト

  - 2005年7月の比較 - AAC vs MP3 vs Vorbis vs WMA の 80 kbpsでの比較。Vorbis aoTuV beta 4がクラシックやさまざまな音楽で最も良いエンコーダという結果となった。また128 kbpsでの [LAME](../Page/LAME.md "wikilink") [ABR](https://ja.wikipedia.org/wiki/可変ビットレート#平均ビットレート（ABR） "wikilink") MP3 と同じ品質という結果になった\[6\]。
  - 2005年8月の比較 - AAC vs MP3 vs Vorbis vs WMA の 96 kbpsでの比較。クラシック音楽においてVorbis aoTuV beta 4とAACが並んで最も良いエンコーダという結果となった。またaoTuV beta 4は ポップミュージックにおいて128 kbpsのLAMEよりも良い結果であった\[7\]。
  - 2005年8月の比較 - [オーディオマニア](https://ja.wikipedia.org/wiki/オーディオマニア "wikilink")による MPC vs Vorbis vs MP3 vs AAC の 180 kbpsでの比較。リスニングテストでクラシック音楽においてVorbis aoTuV beta 4がMPCと並んで最も良いエンコーダという結果になった。LAMEが続いて2位となった\[8\]。
  - 2011年4月の比較 - Hydrogenaudioによる Vorbis vs HE-AAC vs [Opus](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink") の 64 kbpsでの比較。 VorbisはローアンカーのLC-AACとNero HE-AACとの中間ほどの結果となり、Vorbisと同じ開発元の[Xiph.org](https://ja.wikipedia.org/wiki/Xiph.org "wikilink")による[Opus](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink") が最良という結果となった\[9\]。

## ソフトウェア

  - [Audacity](../Page/Audacity.md "wikilink") - クロスプラットフォームな音声録音・編集プログラム　Wikipedia用音声作成用に[Wikipediaヘルプで推奨](https://ja.wikipedia.org/wiki/Help:音声・動画の作成と利用#音声ファイル "wikilink")
  - [Songbird](../Page/Songbird.md "wikilink")
  - [Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")
  - [Zoom player](https://ja.wikipedia.org/wiki/Zoom_player "wikilink")
  - [Foobar2000](../Page/Foobar2000.md "wikilink")
  - [jetAudio](https://ja.wikipedia.org/wiki/:en:jetAudio "wikilink")
  - [Media Player Classic](../Page/Media_Player_Classic.md "wikilink")
  - [MediaFrame](https://ja.wikipedia.org/wiki/MediaFrame "wikilink")\[10\]
  - [MPlayer](../Page/MPlayer.md "wikilink")
  - [VLC media player](https://ja.wikipedia.org/wiki/VLC_media_player "wikilink")
  - [Xbmc](https://ja.wikipedia.org/wiki/Xbmc "wikilink")
  - [Kaffeine](https://ja.wikipedia.org/wiki/Kaffeine "wikilink")
  - [xine](https://ja.wikipedia.org/wiki/xine "wikilink")
  - [QuickTime](../Page/QuickTime.md "wikilink")、[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink") - QuickTimeコンポーネント\[11\]の追加により再生可能
  - [Windows Media Player](../Page/Windows_Media_Player.md "wikilink") - [DirectShow](https://ja.wikipedia.org/wiki/DirectShow "wikilink")フィルタ（[ffdshow](https://ja.wikipedia.org/wiki/ffdshow "wikilink")、公式配布のフィルタ\[12\]等の追加により再生可能

<!-- end list -->

  -
    その他多数

## 脚注

### 注釈

### 出典

<references/>

## 関連項目

  - [aoTuV](https://ja.wikipedia.org/wiki/aoTuV "wikilink")
  - [MP3](../Page/MP3.md "wikilink")
  - [Ogg](../Page/Ogg.md "wikilink")
  - [Oggページ](../Page/Oggページ.md "wikilink")
  - [Ogg Media](../Page/Ogg_Media.md "wikilink")
  - [Opus](https://ja.wikipedia.org/wiki/Opus_\(音声圧縮\) "wikilink") Vorbisと同じくXiphが開発した新しいフォーマット、[CELT](https://ja.wikipedia.org/wiki/CELT "wikilink")の後継。Vorbisに代わるコーデックとして注目されている。
  - [Matroska](../Page/Matroska.md "wikilink")
  - [Theora](../Page/Theora.md "wikilink")
  - [WebM](https://ja.wikipedia.org/wiki/WebM "wikilink")
  - [Vorbis comment](https://ja.wikipedia.org/wiki/Vorbis_comment "wikilink")
  - [TrackMania](../Page/TrackMania.md "wikilink") TrackManiaでは、OGG Vorbisのヘッダデータを編集し、独自の形式「.mux」にて保存することができる。
  - [Spotify](https://ja.wikipedia.org/wiki/Spotify "wikilink") Vorbisを使ってストリームする。

## 外部リンク

  -
[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:Xiph.Org](https://ja.wikipedia.org/wiki/Category:Xiph.Org "wikilink") [Category:オープンフォーマット](https://ja.wikipedia.org/wiki/Category:オープンフォーマット "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.