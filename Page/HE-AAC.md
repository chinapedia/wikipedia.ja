> この記事は[HE-AAC](https://ja.wikipedia.org/wiki/HE-AAC)から翻訳されています。


**HE-AAC** (**High-Efficiency Advanced Audio Coding**) は、[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")の[圧縮](https://ja.wikipedia.org/wiki/圧縮 "wikilink")[符号化](https://ja.wikipedia.org/wiki/符号化 "wikilink")の[国際標準](https://ja.wikipedia.org/wiki/国際標準 "wikilink")化方式である[MPEG-4](../Page/MPEG-4.md "wikilink") [AAC](../Page/AAC.md "wikilink")の拡張仕様であり、[MPEG-4](../Page/MPEG-4.md "wikilink") Audio (ISO/IEC 14496-3)においてAACバージョン3として標準化された。HE-AAC が[2003年](../Page/2003年.md "wikilink")に、HE-AAC v2 が[2006年](../Page/2006年.md "wikilink")に制定された。**MPEG-4 AAC Plus SBR**や、Coding Technologiesの登録商標である**aacPlus**、**AAC+**などの名称でも呼ばれている。

## 概要

HE-AAC では、Coding Technologiesが[mp3PRO](https://ja.wikipedia.org/wiki/mp3PRO "wikilink")で採用している [Spectral Band Replication](https://ja.wikipedia.org/wiki/Spectral_Band_Replication "wikilink")（SBR）技術をAACに組み込むことにより、再生帯域を拡大して主に低[ビットレート](../Page/ビットレート.md "wikilink")(128kbps以下\[1\])での音質([圧縮効率](https://ja.wikipedia.org/wiki/圧縮効率 "wikilink"))を大幅に向上させている。

HE-AAC v2 では、さらなる低ビットレート (48kbps以下\[2\])で音質を改善している。**aacPlus v2** や **eAAC+** といった商標名で呼ばれることもある。

[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink") 9以降、[Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")、[SonicStage](https://ja.wikipedia.org/wiki/SonicStage "wikilink")等で無料でエンコードが可能である。また『[着うたフル](../Page/着うたフル.md "wikilink")』に使用されている[コーデック](../Page/コーデック.md "wikilink")としても有名。[オープンソース](../Page/オープンソース.md "wikilink")のライブラリとしては libaacplus\[3\] がある。

## 技術

HE-AAC v1 では、そのレートより若干低いAAC音声データに [SBR](https://ja.wikipedia.org/wiki/Spectral_Band_Replication "wikilink") と呼ばれる部分を追加して記録している。工程は、はじめに高周波数部分において、圧縮後の[サンプリングレート](https://ja.wikipedia.org/wiki/サンプリングレート "wikilink")で失われる[周波数](../Page/周波数.md "wikilink")以上を抜き出す。このとき、エンコード部分に収まる部分との関連性を調べ、SBR部分(44100Hz)の情報として圧縮する。その後、低サンプリングレート(22050Hz)で通常通りAACとして圧縮を行う｡ そして、この二つのデータをセットにして記録する｡ デコードする時にはまず、AACをデコードした上で、SBRを使い高音域を予測して生成したデータを合成し、再生を行う｡

低、中周波数部分を記録するAAC部分のサンプリングレートを44100Hzから22050Hzへダウンコンバートさせるためビットレート、容量を減らす事が出来る。

HE-AAC v2 では、v1 に[パラメトリックステレオを追加している](https://ja.wikipedia.org/wiki/MPEG-4_Part_3#パラメトリックオーディオ符号化 "wikilink")。

## 互換性

HE-AACのデータは、ベースとなるAAC部分に、拡張データであるSBR部分を上乗せする形で符号化されるため、従来のAACしか再生できないプレイヤーでも、音質は劣るもののAAC部分だけを再生できる、という特徴がある。

しかし、AACのみがデコードされる場合のサンプルレートは22050Hzとなる。

## 音質

高音域の成分が複雑に入っている音は高音域の[ノイズ](../Page/ノイズ.md "wikilink")が目立ちにくいが、高音域の成分がある程度単調な音ではノイズが乗っているように聞こえる（これはSBRの特徴であり、ビットレートを上げてもそれほど改善しない）。したがって、高音域が複雑で再生可聴帯域があまり広くない[J-POP](../Page/J-POP.md "wikilink")や[演歌](../Page/演歌.md "wikilink")を含む[歌謡曲](../Page/歌謡曲.md "wikilink")、[ハードロック](../Page/ハードロック.md "wikilink")、[トランス (音楽)などに向いているが](../Page/トランス_\(音楽\).md "wikilink")、一方で高音域が単調で再生可聴帯域が広くなりやすい[ジャズ](../Page/ジャズ.md "wikilink")や[クラシック音楽](../Page/クラシック音楽.md "wikilink")などには不向きである。

AAC部分のサンプルレートはもともと22050Hzであるため軽快さ、滑らかさ、細やかさなどに欠ける。

## 種類

HE-AACにもいくつかの種類が存在する。しかし、1バイトを除いてほぼ同一であるので、機能に差はない。

ただし、下位互換であるAAC形式のコンテナには[iTunes](https://ja.wikipedia.org/wiki/iTunes "wikilink")などで使用される[拡張子](../Page/拡張子.md "wikilink")がM4Aのものと、[Winamp](https://ja.wikipedia.org/wiki/Winamp "wikilink")などで使用される拡張子がAACのもの（特にAACPlusと呼ばれる）に互換性がないため注意が必要である。

このため両者の拡張子のみを書き換えても正常に読み込みできないことがある。（特にAACのファイルはau Music Portでは読み込めない）

他に[MP4](../Page/MP4.md "wikilink")フォーマット（拡張子MP4・3GP）が使用されることがあり、アプリケーションやデバイスによって対応状況が異なる。

  - MPEG-2 Audio AAC Bandwidth (MPEG-2 HE-AAC) : [MPEG-2](../Page/MPEG-2.md "wikilink")の構造・用途を用いたHE-AAC。SD-Audio及びモバHO\!に使われている(AAC+SBRという名で呼ばれている)
    MPEG-4 Audio AAC Bandwidth (MPEG-4 HE-AAC) : [MPEG-4](../Page/MPEG-4.md "wikilink")の構造・用途を用いたHE-AAC。現在あるものは殆どこちらの規格。

## HE-AAC v2

HE-AAC v1 にパラメトリックステレオを利用した音質改善を施した物が **MPEG-4 High Efficiency AAC v2 profile** (**HE-AAC v2**) である。高ビットレートでの音質改善はないが、48kbps 以下の低ビットレートで音質が改善する\[4\]。

## 特許

v1 は[フィリップス](../Page/フィリップス.md "wikilink")、[ドルビー](https://ja.wikipedia.org/wiki/ドルビー "wikilink")、[ノキア](../Page/ノキア.md "wikilink")が[特許](../Page/特許.md "wikilink")を持っていて、利用には特許プールとの契約が必要。v2 は v1 に加えて、[フィリップス](../Page/フィリップス.md "wikilink")、[ドルビー](https://ja.wikipedia.org/wiki/ドルビー "wikilink")が特許を持っていて、特許プールに加えて[ドルビー](https://ja.wikipedia.org/wiki/ドルビー "wikilink")との特許契約が必要。

## 利用例

  - [Adobe Flash Player](../Page/Adobe_Flash.md "wikilink") 9 以降 - HE-AAC v2 対応
      - [radiko](https://ja.wikipedia.org/wiki/radiko "wikilink")
  - 音楽配信
      - [着うた](../Page/着うた.md "wikilink") ※ごく一部
      - [着うたフル](../Page/着うたフル.md "wikilink")
      - au LISTEN MOBILE SERVICE（[LISMO](../Page/LISMO.md "wikilink")）
  - [SD-Audio](../Page/SD-Audio.md "wikilink")　※パソコンソフト[SD-Jukebox](../Page/SD-Jukebox.md "wikilink")やSDオーディオ機器ではAAC+SBRと呼ばれている。一部の[NTTdocomoの](https://ja.wikipedia.org/wiki/NTTドコモ "wikilink")[Pシリーズ](https://ja.wikipedia.org/wiki/パナソニックモバイルコミュニケーションズ "wikilink")（パナソニック製）と[Nシリーズ](../Page/日本電気.md "wikilink")（NEC製）、および[Lシリーズ](../Page/LGエレクトロニクス.md "wikilink")（LG製）のSDオーディオ対応携帯電話での再生に対応
  - テレビ放送
      - [ワンセグ](../Page/ワンセグ.md "wikilink")
      - [モバHO\!](../Page/モバHO!.md "wikilink")
  - [インターネットラジオ](../Page/インターネットラジオ.md "wikilink")
      - [radiko](https://ja.wikipedia.org/wiki/radiko "wikilink")
      - [NHKネットラジオ らじる★らじる](https://ja.wikipedia.org/wiki/NHKネットラジオ_らじる★らじる "wikilink")
  - [デジタルオーディオプレーヤー](../Page/デジタルオーディオプレーヤー.md "wikilink") - [ウォークマン](../Page/ウォークマン.md "wikilink")、[iPod nano](https://ja.wikipedia.org/wiki/iPod_nano "wikilink")（第5世代以降）、[iPod shuffle](https://ja.wikipedia.org/wiki/iPod_shuffle "wikilink")（第3世代\[5\]のみ\[6\]）など
  - [スマートフォン](https://ja.wikipedia.org/wiki/スマートフォン "wikilink") - [Android](../Page/Android.md "wikilink"), [iOS](https://ja.wikipedia.org/wiki/iOS_\(アップル\) "wikilink") など

## 関連項目

  - [AAC](../Page/AAC.md "wikilink")
  - [mp3PRO](https://ja.wikipedia.org/wiki/mp3PRO "wikilink")

## 参照

<references />

## 外部リンク

  - [aacPlus](http://www.codingtechnologies.com/products/aacPlus.htm)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink")

1.  [MPEG-4 HE-AAC v2 - EBU TECHNICAL REVIEW – January 2006](http://tech.ebu.ch/docs/techreview/trev_305-moser.pdf)
2.
3.  [HE-AAC+ Codec as Shared Library - tipok.org.ua](http://tipok.org.ua/node/17/)
4.
5.
6.  [Apple - iPod - あなたにぴったりのiPodは？](http://www.apple.com/jp/ipod/compare-ipod-models/) 2014年10月16日閲覧