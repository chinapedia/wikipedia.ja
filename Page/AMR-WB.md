> この記事は[AMR-WB](https://ja.wikipedia.org/wiki/AMR-WB)から翻訳されています。


**AMR-WB**（）は、[Adaptive Multi-Rate](../Page/Adaptive_Multi-Rate.md "wikilink")（AMR）をベースとするマルチレートの広帯域[音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")方式で、[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")や[W-CDMA](../Page/W-CDMA.md "wikilink") 方式の[第三世代携帯電話](https://ja.wikipedia.org/wiki/第三世代携帯電話 "wikilink")で利用される。 AMR-WB と区別するため、従来の [AMR](../Page/Adaptive_Multi-Rate.md "wikilink") は AMR-NB（）と呼ばれることもある。

同じ仕様は [ITU-T](../Page/ITU-T.md "wikilink") が勧告した広帯域[音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")方式 **G.722.2** でも使用されている \[1\]。

## 概要

AMR-WB は、[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink") などで使用される [Adaptive Multi-Rate](../Page/Adaptive_Multi-Rate.md "wikilink")（AMR）と同様マルチレートをサポートする[音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")方式で、AMR を広帯域化することで[音質](https://ja.wikipedia.org/wiki/音質 "wikilink")を高めたものである。 通常の電話インタフェースの2倍の[帯域幅](../Page/帯域幅.md "wikilink")を持つ 50 Hz-7 kHz（[サンプリング周波数](../Page/サンプリング周波数.md "wikilink") 16kHz）の音声信号を 6.60 k[bps](../Page/ビット毎秒.md "wikilink")～23.85 k[bpsまでの](../Page/ビット毎秒.md "wikilink") 9 種類の[ビットレート](https://ja.wikipedia.org/wiki/ビットレート "wikilink")で符号化できる \[2\]。 AMR-WB は標準化団体の[3GPP](https://ja.wikipedia.org/wiki/3GPP "wikilink")（3rd Generation Partnership Project）が策定した。

[ITU-T](../Page/ITU-T.md "wikilink") が勧告した広帯域[音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")方式 **G.722.2** も AMR-WB と同じものである。この規格は [G.722](https://ja.wikipedia.org/wiki/G.722 "wikilink")、[G.722.1](https://ja.wikipedia.org/wiki/G.722.1 "wikilink") から派生したもので、これらと比べると同じ広帯域の音声をより低い[ビットレート](https://ja.wikipedia.org/wiki/ビットレート "wikilink")で符号化できる。G.722.2 の正式な名称は*"Wideband coding of speech at around 16 kbit/s using Adaptive Multi-Rate Wideband (AMR-WB)"*（広帯域適応マルチレート (AMR-WB) 方式を用いた16 kbit/s程度の広帯域音声符号化）である\[3\]。

AMR-WB の符号化アルゴリズムは AMR と同じ [ACELP](https://ja.wikipedia.org/wiki/ACELP "wikilink")（Algebraic Code Excited Linear Prediction）を使用し\[4\]、 以下のビットレートをサポートしている。6.60 kbps～12.65 kbps までが必須マルチレート構成で、通常は 12.65 kbps が使用される。それより高いビットレートは背景雑音が多い環境、音声と音楽との組み合わせ、マルチパーティ会議など高い音質が要求される場合に使用される\[5\]\[6\]。

| **ビットレート** | **サポート** | **説明**                                                                                                                                                                                                                                                                              |
| ---------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 6.60 kbps  | 必須       | 移動体[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")システム（[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink"), [W-CDMA](../Page/W-CDMA.md "wikilink")）で使用：無線状態が悪い時にのみ一時的に使用。広帯域音声とは見なされない。                                                                                       |
| 8.85 kbps  | 必須       | 移動体[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")システム（[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink"), [W-CDMA](../Page/W-CDMA.md "wikilink")）で使用：無線状態が悪い時にのみ一時的に使用。広帯域音声とは見なされない。48 kbps の [G.722](https://ja.wikipedia.org/wiki/G.722 "wikilink") と同等の音質。              |
| 12.65 kbps | 必須       | 移動体[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")システム（[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink"), [W-CDMA](../Page/W-CDMA.md "wikilink")）で使用：メインとなるビットレート。AMR より優れた音質で、これ以上のビットレートでは 56 kbps の [G.722](https://ja.wikipedia.org/wiki/G.722 "wikilink") と同等かそれ以上の音質。 |
| 14.25 kbps |          |                                                                                                                                                                                                                                                                                     |
| 15.85 kbps |          |                                                                                                                                                                                                                                                                                     |
| 18.25 kbps |          |                                                                                                                                                                                                                                                                                     |
| 19.85 kbps |          |                                                                                                                                                                                                                                                                                     |
| 23.05 kbps |          | フルレート[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")チャネルは対象外。                                                                                                                                                                                                                   |
| 23.85 kbps |          | フルレート[GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")チャネルは対象外。64 kbps の [G.722](https://ja.wikipedia.org/wiki/G.722 "wikilink") と同等の音質。                                                                                                                                          |

AMR-WB のビットレート

[コーデック](../Page/コーデック.md "wikilink")の入出力は 14ビット長、[サンプリング周波数](../Page/サンプリング周波数.md "wikilink") 16kHzの信号で、これを 12.8 kHz に[ダウンサンプリングして処理を行う](https://ja.wikipedia.org/wiki/リサンプリング "wikilink")。デコード時には処理結果を 16kHz に[アップサンプリングし](https://ja.wikipedia.org/wiki/リサンプリング "wikilink")、6 kHz ～ 7 kHzの高域成分を追加する\[7\]。

会話での無音期間は、AMR の場合同様、音声区間検出機能（、VAD）で検出を行い 160ms ごとに SID（）と呼ばれるデータを送信する。まったくの無音を避けるため、デコーダ側では SID を検出すると適度なレベルの背景雑音を再生する。

インターネット上での [RTP](https://ja.wikipedia.org/wiki/RTP "wikilink") による AMR-WB のペイロードの形式は RFC4867 で定義されている\[8\]。

## 用途

[携帯電話](../Page/携帯電話.md "wikilink")や[VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")での音声通信用以外に、AMR-WB は [3GPP](https://ja.wikipedia.org/wiki/3GPP "wikilink") で定義された各種マルチメディアサービスで使用することができる \[9\] \[10\] \[11\]。

  - [IPマルチメディアサブシステム](https://ja.wikipedia.org/wiki/IPマルチメディアサブシステム "wikilink")（IMS）
  - [マルチメディアメッセージングサービス](https://ja.wikipedia.org/wiki/マルチメディアメッセージングサービス "wikilink")（MMS）
  - パケットスイッチドストリーミングサービス（PSS）

## 脚注

## 参考文献

  - ITU-T Recommendation G.722.2 (07/2003), *Wideband coding of speech at around 16 kbit/s using Adaptive Multi-Rate Wideband (AMR-WB)*. ITU-T, 2003.
  - 3GPP, *Adaptive Multi-Rate - Wideband (AMR-WB) speech codec;General description*. 3GPP TS 26.171 version 9.0.0 Release 9, 2009.
  - 3GPP, *Adaptive Multi-Rate - Wideband (AMR-WB) speech codec;Transcoding functions*. 3GPP TS 26.190 version 9.0.0 Release 9, 2010.
  - IETF Network Working Group. RFC4867 [*RTP Payload Format for AMR and AMR-WB*](http://tools.ietf.org/html/rfc4867). IETF. April, 2007.

## 関連項目

  - [音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")
  - [Adaptive Multi-Rate](../Page/Adaptive_Multi-Rate.md "wikilink")
  - [G.711](https://ja.wikipedia.org/wiki/G.711 "wikilink")
  - [G.722](https://ja.wikipedia.org/wiki/G.722 "wikilink")
  - [G.722.1](https://ja.wikipedia.org/wiki/G.722.1 "wikilink")
  - [G.723](https://ja.wikipedia.org/wiki/G.723 "wikilink")
  - [G.723.1](https://ja.wikipedia.org/wiki/G.723.1 "wikilink")
  - [G.726](https://ja.wikipedia.org/wiki/G.726 "wikilink")
  - [3GPP](https://ja.wikipedia.org/wiki/3GPP "wikilink")

## 外部リンク

  - [ITU-T Recommendation G.722.2; (AMR-WB)- technical specification](http://www.itu.int/rec/T-REC-G.722.2/en)
  - [Adaptive Multi-Rate - Wideband (AMR-WB) speech codec; Transcoding functions; 3GPP TS 26.190 - 3GPP technical specification](http://www.3gpp.org/ftp/Specs/html-info/26190.htm)
  - [Adaptive Multi-Rate - Wideband (AMR-WB) speech codec; Voice Activity Detector (VAD); 3GPP TS 26.194 - 3GPP technical specification](http://www.3gpp.org/ftp/Specs/html-info/26194.htm)
  - [Adaptive Multi-Rate - Wideband (AMR-WB) speech codec; General description; 3GPP TS 26.171 - 3GPP technical specification](http://www.3gpp.org/ftp/Specs/html-info/26171.htm)
  - [3GPP codecs specifications; 3G and beyond / GSM, 26 series](http://www.3gpp.org/ftp/Specs/html-info/26-series.htm)
  - RFC 4867 - RTP Payload Format and File Storage Format for the Adaptive Multi-Rate (AMR) and Adaptive Multi-Rate Wideband (AMR-WB) Audio Codecs
  - RFC 4281 - The Codecs Parameter for "Bucket" Media Types
  - [Deep Inside the Network, Episode 2: AMR-WB - Skype-like Audio Quality for Mobile Networks](http://mobilesociety.typepad.com/mobile_life/2006/12/deep_inside_the.html)
  - [Wideband Speech Coding Standards and Applications](http://www.voiceage.com/media/WidebandSpeech.pdf)
  - [3GPP - Technical Specification Group Services and System Aspects](http://www.3gpp.org/ftp/tsg_sa/TSG_SA/TSGS_17/Docs/PDF/SP-020422.pdf)
  - [ITU-T Implementors' Guide for G.722.2](http://www.itu.int/itudoc/itu-t/com16/implgd/old/g7222-ig.pdf)

[de:Adaptive Multi-Rate](https://ja.wikipedia.org/wiki/de:Adaptive_Multi-Rate "wikilink")

[Category:コーデック](https://ja.wikipedia.org/wiki/Category:コーデック "wikilink") [Category:GSM](https://ja.wikipedia.org/wiki/Category:GSM "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink")

1.  ITU-T Recommendation G.722.2 (07/2003), *Wideband coding of speech at around 16 kbit/s using Adaptive Multi-Rate Wideband (AMR-WB)*. ITU-T, 2003.
2.  3GPP, *Adaptive Multi-Rate - Wideband (AMR-WB) speech codec;Transcoding functions*. 3GPP TS 26.190 version 9.0.0 Release 9, 2010.
3.
4.
5.
6.
7.
8.
9.  ETSI (2009-04) [ETSI TS 126 234 V8.2.0 (2009-04); 3GPP TS 26.234; Transparent end-to-end Packet-switched Streaming Service (PSS); Protocols and codecs](http://www.3gpp.org/ftp/Specs/html-info/26234.htm). 2010-07-8閲覧。
10. ETSI (2009-01) [ETSI TS 126 140 V8.0.0 (2009-01); 3GPP TS 26.140; Multimedia Messaging Service (MMS); Media formats and codes](http://www.3gpp.org/ftp/Specs/html-info/26140.htm). 2010-07-8閲覧。
11. ETSI (2009-01) [ETSI TS 126 141 V8.0.0 (2009-01); 3GPP TS 26.141; IP Multimedia System (IMS) Messaging and Presence; Media formats and codecs](http://www.3gpp.org/ftp/Specs/html-info/26141.htm). 2010-07-8閲覧。