> この記事は[PASC](https://ja.wikipedia.org/wiki/PASC)から翻訳されています。


**PASC**（**P**recision **A**daptive **S**ubband **C**oding、パスク）は、かつて[デジタルコンパクトカセット](../Page/デジタルコンパクトカセット.md "wikilink")（DCC）で採用されていた音声信号圧縮方式、および、その[LSI](../Page/集積回路.md "wikilink")（[フィリップス](../Page/フィリップス.md "wikilink")製）。[MPEG-1/2 Audio Layer-1](https://ja.wikipedia.org/wiki/MP3#MPEG-1/2_Audio_Layer-1 "wikilink")（MP1）の技術を基にして開発された。

## 概要

PASCの基本技術は、フィリップスの基礎研究所（Natラボ）で開発された。\[1\] DCCの[ビットレート](../Page/ビットレート.md "wikilink")は384kbit/sで、[DAT](../Page/DAT.md "wikilink")の1536kbit/sに比べると1/4であるため、音声信号の圧縮方式としてPASCが採用された。この規格の開発には、[レコーディング・エンジニア](../Page/レコーディング・エンジニア.md "wikilink")や、[ミュージシャンが参加しており](https://ja.wikipedia.org/wiki/音楽家 "wikilink")、オリジナルと聴感上の違いがほとんど違いが出ない程度の音質を保ちながら、[CDのPCM信号を](../Page/コンパクトディスク.md "wikilink")1/4に圧縮している。この回路の原理は要約すると次のようになる。

1.  まず、オーディオ信号の[周波数](../Page/周波数.md "wikilink")帯域を、[デジタルフィルタ](https://ja.wikipedia.org/wiki/デジタルフィルタ "wikilink")によって、750Hz刻みで32の帯域（サブバンド）に分割する（最初に、入力された信号は、サブバンドフィルタ（デジタルフィルタ）によって0～24kHzの範囲を750Hzずつ32の帯域に分割される。分割された帯域をサブバンドという）。
2.  次にPASCシグナルプロセッサによって、その中から人間の耳に聴こえる信号を選び出し、聴こえない信号は切り捨てる。つまり、聴こえない信号を間引くことによって、[情報量](../Page/情報量.md "wikilink")を減らす。
3.  最後に、分割された各帯域に必要な[ビット](../Page/ビット.md "wikilink")数を割り当てる。この3段階の信号処理によって、[再生音には影響を与えずに記録する情報量を](../Page/録音再生機器.md "wikilink")1/4に圧縮するという技術を実現している。

PASCでは、[音楽](../Page/音楽.md "wikilink")信号全体にわたって信号圧縮が行われているわけではない。PASCで処理されるのは、音楽信号の情報量がDCCの容量を超えた時だけであり、DCCはいつも16[bitの音楽信号を](../Page/ビット.md "wikilink")1/4（4bit）に圧縮しているわけではない。CDやDATなどでは、音楽信号は[ビットレート](../Page/ビット毎秒.md "wikilink")1536kbit/sの半分（[ステレオ](../Page/ステレオ.md "wikilink")2チャンネルだから）の768kbit/sのままで処理されており、これをリニアコーディングと呼んでいる。DCCの場合には、信号経路が2つに分けられる。音楽信号の情報量が192kbit/s（片チャンネル分）以内の時はそのままリニアコーディングの経路を通り、情報量が192kbit/sを超えた時には、超えた部分について信号圧縮の処理が施される。

PASC方式に対応した[ソフトウェア](../Page/ソフトウェア.md "wikilink")や[デジタルオーディオプレーヤー](../Page/デジタルオーディオプレーヤー.md "wikilink")は存在せず、PASC形式ではCDからの取り込み自体行えない状態である。

## 脚注

<references />

## 関連項目

  - [ATRAC](../Page/ATRAC.md "wikilink")
  - [MP3](../Page/MP3.md "wikilink")
  - [AAC](../Page/AAC.md "wikilink")

## 外部リンク

  - [テクニカルラボ](http://www.puwa-net.com/minidisc/technical/tech-info/pasc.htm)
  - [DCC情報室@関西](http://freett.com/Tfactory/Audio/DCCinfo/PASCver.html)

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:音声ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:音声ファイルフォーマット "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink") [Category:フィリップス](https://ja.wikipedia.org/wiki/Category:フィリップス "wikilink")

1.  ステレオ時代 Vol.14