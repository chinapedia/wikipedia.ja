> この記事は[MPEG-2](https://ja.wikipedia.org/wiki/MPEG-2)から翻訳されています。


**MPEG-2**（エムペグツー、**H.222/H.262**, **ISO/IEC 13818**）は[1995年](https://ja.wikipedia.org/wiki/1995年 "wikilink")7月に[ISO/IEC JTC 1の](https://ja.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink")[Moving Picture Experts Groupによって決められた標準規格](../Page/Moving_Picture_Experts_Group.md "wikilink")。正式名称はGeneric coding of moving pictures and associated audio information

## 概要

MPEG2は[ビデオ](../Page/ビデオ.md "wikilink")、[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")の他、システム等についても規格化されている。また、様々なメディアでの利用を想定して、複数の[解像度](https://ja.wikipedia.org/wiki/解像度 "wikilink")、[圧縮率](https://ja.wikipedia.org/wiki/圧縮率 "wikilink")がある。なお、復号方式のみが定められており、符号化方式について規格化されていない。よって規格に沿った結果が得られるのであれば、符号化の手順はどのようにしてもよい事になっている。基本的に[MPEG-1](https://ja.wikipedia.org/wiki/MPEG-1 "wikilink")との下位互換性は無い（MPEG-2の再生装置でMPEG-1の再生は出来るがその逆ではできない）。

なお、元々標準[テレビ](../Page/テレビ.md "wikilink")[放送](https://ja.wikipedia.org/wiki/放送 "wikilink")（SDTV）向けにMPEG-2、[高精細度テレビジョン放送](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink") （HDTV）向けに**MPEG-3**が策定される予定であったが、両者は基本技術が同じであったため、最終的にはMPEG-3がMPEG-2に吸収・統合されることが決定し、MPEG-3規格は**欠番**となっている。現在では標準テレビからHDTVに至るまでMPEG-2が幅広く利用されている。 （出力解像度はまた異なる）。

## ビデオ

ビデオ(ISO/IEC 13818-2)については、採用されている基本技術の大部分が[MPEG-1](https://ja.wikipedia.org/wiki/MPEG-1 "wikilink")ビデオと同等であるため、[圧縮効率](https://ja.wikipedia.org/wiki/圧縮効率 "wikilink")の側面ではMPEG-1とほとんど変わらない。
ただしネットワーク環境や[HDTV](https://ja.wikipedia.org/wiki/HDTV "wikilink")など動画性能の向上を受けて、以下の拡張が行われている。

  - [インタレースへの対応](https://ja.wikipedia.org/wiki/走査#インターレース方式とプログレッシブ方式 "wikilink")
    同時にフィールド補完による動画圧縮を追加。
  - [多重化](https://ja.wikipedia.org/wiki/多重化 "wikilink")への対応
    データ構造に拡張性が与えられている。具体的な多重化の実現については主にPart1: Systemの項などで定義されている。
  - 色情報フォーマットの拡充
    MPEG-1では**4:2:0**のみ対応だったが、MPEG-2では**4:4:4**、**4:2:2**、**4:2:0**に対応。
  - 圧縮効率の変更
    約2Mbps以上において、圧縮率が最適になるように調整。

なお、MPEG-2ビデオは[ITU-T](https://ja.wikipedia.org/wiki/ITU-T "wikilink")とISO/IECの合同規格であり、ITU-T勧告H.262としても標準化されている。

## オーディオ

一般的には**MPEG-2オーディオ**と呼ばれるものが定義されており（ISO/IEC 13818-3）、MPEG-1オーディオと同様にLayer-1、Layer-2、Layer-3と分けられて策定された。[MPEG-1](https://ja.wikipedia.org/wiki/MPEG-1 "wikilink")オーディオとの互換性が考慮されているBC（Backward Compatible）と、互換性を排除して高音質・高圧縮を達成した[AAC](https://ja.wikipedia.org/wiki/AAC "wikilink")（Advanced Audio Coding）がある（MPEG-2 Audio Layer-3の正式名称が“MPEG-2 BC”となった。）。

## システム

システム（ISO/IEC 13818-1, ITU-T H.222.0）についても、[DVD-Video](../Page/DVD-Video.md "wikilink")のような蓄積メディアでの使用に向いたプログラムストリーム（MPEG-2 PS）と、[デジタル放送等の放送](https://ja.wikipedia.org/wiki/デジタル放送の一覧 "wikilink")・通信に向いたトランスポートストリーム（MPEG-2 TS）が規定されている。詳細については[MPEG-2システム](https://ja.wikipedia.org/wiki/MPEG-2システム "wikilink")の記事を参照されたい。

[パソコン上で扱われる](../Page/パーソナルコンピュータ.md "wikilink")「MPEG-2ファイル」と呼ばれるものはプログラムストリームのデータが記録されているものであることが多く、拡張子として.m2pが使われることが多い。 これに対して、.mp2はMPEG Audio Layer 2の拡張子として使われることが一般的であり、MPEG-2システムのデータを指し示すものではない。

## 利用例

MPEG-2は放送や[HDTVなどを想定した規格であり](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")、実際にもデジタル放送や記録メディアなど様々な用途に利用されている。以下に代表的な利用例を挙げる。

### DVD-Video

[DVD-Video](../Page/DVD-Video.md "wikilink")では映像としてMPEG-2ビデオが使われると共に、プログラムストリームに準じた形式で音声などのデータが混合・記録されている。一方日本国内では、音声としては[PCMや](https://ja.wikipedia.org/wiki/パルス符号変調 "wikilink")[ドルビーデジタル](https://ja.wikipedia.org/wiki/ドルビーデジタル "wikilink")（AC-3）といった、MPEG以外の規格・技術が使われている例が大勢を占める。MPEGオーディオも[DVD-Video](../Page/DVD-Video.md "wikilink")の規格としては認められているが、日本国内では必須ではなくオプション扱いである。なお、同じくオプション扱いでは、低圧縮（＝高音質）な[dts方式で収録されているものが多い](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink")。

### デジタル放送

デジタル放送では多重化伝送方式としてMPEG-2 TS、動画像符号化方式としてMPEG-2ビデオが採用されている。詳細については[デジタルテレビ](https://ja.wikipedia.org/wiki/デジタルテレビ "wikilink")の記事を参照されたい。

### その他の利用例

  - [DVDレコーダー](https://ja.wikipedia.org/wiki/DVDレコーダー "wikilink")
  - [Blu-ray Disc](https://ja.wikipedia.org/wiki/Blu-ray_Disc "wikilink")
  - [HD DVD](https://ja.wikipedia.org/wiki/HD_DVD "wikilink")
  - [D-VHS](https://ja.wikipedia.org/wiki/D-VHS "wikilink")
  - [HDV](https://ja.wikipedia.org/wiki/HDV "wikilink")
  - [MICROMV](https://ja.wikipedia.org/wiki/MICROMV "wikilink")

## MPEG-2に関わる裁判

MPEG-2に関する符号化・復号技術などの技術は、電機メーカー各社で開発、[特許](https://ja.wikipedia.org/wiki/特許 "wikilink")申請等が行われ、アメリカのMPEG LA社が管理している。[2008年](https://ja.wikipedia.org/wiki/2008年 "wikilink")6月、アメリカの[液晶テレビ](https://ja.wikipedia.org/wiki/液晶テレビ "wikilink")のトップシェアメーカーである[VIZIO](https://ja.wikipedia.org/wiki/VIZIO "wikilink")社が、テレビ製造に際しライセンス料の支払いを行っていないとして、各電機メーカーがニューヨーク州連邦地方裁判所に提訴。VIZIO側は、2008年[11月17日](https://ja.wikipedia.org/wiki/11月17日 "wikilink")にライセンス料を支払うことで和解が成立している。\[1\]

## 関連項目

  - [Moving Picture Experts Group](../Page/Moving_Picture_Experts_Group.md "wikilink")

  -
  - [MPEG-1](https://ja.wikipedia.org/wiki/MPEG-1 "wikilink")

  - [MPEG-4](https://ja.wikipedia.org/wiki/MPEG-4 "wikilink")

  - [MPEG-7](https://ja.wikipedia.org/wiki/MPEG-7 "wikilink")

  - [MPEG-21](https://ja.wikipedia.org/wiki/MPEG-21 "wikilink")

  - [H.261](https://ja.wikipedia.org/wiki/H.261 "wikilink")

  - [H.263](https://ja.wikipedia.org/wiki/H.263 "wikilink")

  - [H.264](https://ja.wikipedia.org/wiki/H.264 "wikilink")

  - [AAC](https://ja.wikipedia.org/wiki/AAC "wikilink")

  - [TMPGEnc](https://ja.wikipedia.org/wiki/TMPGEnc "wikilink")

## 出典

<references/>

## 外部リンク

  - [QuEnc](http://nic.dnsalias.com/)
  - [HC encoder](http://www.free-codecs.com/download/HC_encoder.htm)

[nl:MPEG\#MPEG-2](https://ja.wikipedia.org/wiki/nl:MPEG#MPEG-2 "wikilink")

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink")

1.  <http://techon.nikkeibp.co.jp/article/NEWS/20081118/161403/?ref=RL2> 米VIZIO社，MPEG-2特許で米MPEG LAとライセンス契約（日経BP）