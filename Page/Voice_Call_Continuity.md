> この記事は[Voice Call Continuity](https://ja.wikipedia.org/wiki/Voice_Call_Continuity)から翻訳されています。


**Voice Call Continuity**(VCC)は、3G（第3世代携帯電話）と[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")の間で音声通話をシームレスに[ハンドオーバー](../Page/ハンドオーバー.md "wikilink")する技術である。 VCC を用いることにより、屋外では携帯電話網を利用し、屋内では無線LANを利用した通話が可能となり、移動中も音声が途切れることなく自動的に[ハンドオーバー](../Page/ハンドオーバー.md "wikilink")が可能となる。

## 技術

VCC は [3GPP](../Page/3GPP.md "wikilink") で策定された技術であり、[Fixed Mobile Convergence](https://ja.wikipedia.org/wiki/Fixed_Mobile_Convergence "wikilink")(FMC) を実現する技術の１つと捉えられる。

3G携帯電話の音声通話は[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")であるが、IPネットワークでの音声通話は[パケット交換](https://ja.wikipedia.org/wiki/パケット交換 "wikilink")をもちいた[VoIP](../Page/VoIP.md "wikilink")であるため、音声通話を[ハンドオーバー](../Page/ハンドオーバー.md "wikilink")するには特別な仕組みが必要となる。 VCC ではこれを実現するために、[回線交換](https://ja.wikipedia.org/wiki/回線交換 "wikilink")呼を[メディアゲートウェイ](https://ja.wikipedia.org/wiki/メディアゲートウェイ "wikilink")を用いて[SIP呼に変換し](../Page/Session_Initiation_Protocol.md "wikilink")、[IMS](https://ja.wikipedia.org/wiki/IPマルチメディアサブシステム "wikilink")(IP Multimedia Subsystem)網に引き込む。IMS網内に VCC Application Server(VCC AS) と呼ばれる装置を置き、この装置がSIP呼の[ハンドオーバー](../Page/ハンドオーバー.md "wikilink")を処理することで、3G/IPネットワーク間の[ハンドオーバー](../Page/ハンドオーバー.md "wikilink")を実現する。

### I-WLAN

VCC のサービスを受けるためには、VCCに対応した端末が必要である。VCC端末は、3G網無線アクセスの他に[無線LAN](../Page/無線LAN.md "wikilink")などのIPアクセス機能を備えた、いわゆるデュアルモード端末である必要がある。

[無線LAN](../Page/無線LAN.md "wikilink")を使って[IMSにアクセスするための技術として](https://ja.wikipedia.org/wiki/IPマルチメディアサブシステム "wikilink")、[3GPP](../Page/3GPP.md "wikilink")により標準化された **I-WLAN** (Interworking WLAN) 技術がある。I-WLAN では、 端末はIMS網のエッジに配置された PDG (Packet Data Gateway) と呼ばれる装置に対して [IPsec](../Page/IPsec.md "wikilink")トンネルを張り、このトンネルを通してIMSにアクセスできる。

## 主なサービス

### 日本の状況

日本国内では、現時点ではまだ VCC に対応したサービスは実施されていない。

## 参考文献

  - [3GPP TS23.206 - Voice Call Continuity (VCC) between Circuit Switched (CS) and IP Multimedia Subsystem (IMS); Stage 2](http://www.3gpp.org/ftp/Specs/html-info/23206.htm)
  - [3GPP TS24.206 - Voice call continuity between Circuit Switched (CS) and IP Multimedia Subsystem (IMS); Stage 3](http://www.3gpp.org/ftp/Specs/html-info/24206.htm)

## 関連項目

  - [Fixed Mobile Convergence](https://ja.wikipedia.org/wiki/Fixed_Mobile_Convergence "wikilink")

## 外部リンク

  - [NC7000-VC](http://www.nec.co.jp/netsoft/nc7000-vc/)

[Category:電気通信](https://ja.wikipedia.org/wiki/Category:電気通信 "wikilink")