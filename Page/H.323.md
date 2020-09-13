> この記事は[H.323](https://ja.wikipedia.org/wiki/H.323)から翻訳されています。


**H.323** 勧告は、[IP網](https://ja.wikipedia.org/wiki/IP網 "wikilink")でリアルタイムの[音声](https://ja.wikipedia.org/wiki/音声 "wikilink")・[動画](../Page/動画.md "wikilink")[通信](../Page/通信.md "wikilink")を行うための [ITU-T](../Page/ITU-T.md "wikilink") 制定による[通信プロトコル](../Page/通信プロトコル.md "wikilink")の標準である。

バージョン 1 が [1996年](../Page/1996年.md "wikilink")、バージョン 2 が [1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink") [1月](https://ja.wikipedia.org/wiki/1月 "wikilink") に承認された。

## 概要

H.323 は[オーディオ](https://ja.wikipedia.org/wiki/オーディオ "wikilink")、[ビデオやその他のデータによる](../Page/映像信号.md "wikilink")、[IPネットワーク](https://ja.wikipedia.org/wiki/IPネットワーク "wikilink")を含む[パケット](../Page/パケット.md "wikilink")・[ネットワークにおける](../Page/コンピュータネットワーク.md "wikilink")[マルチメディア](../Page/マルチメディア.md "wikilink")・[リアルタイム通信](https://ja.wikipedia.org/wiki/リアルタイム通信 "wikilink")に関する標準である。そのための要素、[通信プロトコル](../Page/通信プロトコル.md "wikilink")および手続きを記述している。[LAN](../Page/Local_Area_Network.md "wikilink") から [WAN](../Page/Wide_Area_Network.md "wikilink") までの様々なネットワークにおいて、オーディオだけ、オーディオとビデオ、オーディオとデータなど、様々なマルチメディア・データの組合せにおいて使用することができる。

H.323 の最初の版は 1996 年 10 月に出版されたが、その後 1998 年、1999 年、2000 年、2003 年にそれぞれ改訂され、現在の版は第 5 版である。H.323 第 5 版に関連するドキュメントとして次のものがある。

  - Recommendation H.323: Packet-based multimedia communications systems, Infrastructure of audiovisual services – Systems and terminal equipment for audiovisual services, ITU-T, 2003.
  - Recommendation H.225.0: Call signalling protocols and media stream packetization for packet-based multimedia communication systems, Infrastructure of audiovisual services – Systems and terminal equipment for audiovisual services, ITU-T, 2003.
  - Recommendation H.245: LINE TRANSMISSION OF NON-TELEPHONE SIGNALS, CONTROL PROTOCOL FOR MULTIMEDIA COMMUNICATION – Systems and terminal equipment for audiovisual services, ITU-T, 2002.

## 特徴

  - 相互接続性の確保が可能。
  - [ネットワーク構成](https://ja.wikipedia.org/wiki/ネットワーク構成 "wikilink")から独立している。
  - [オペレーティングシステム](../Page/オペレーティングシステム.md "wikilink")・[アプリケーションソフトウェア](../Page/アプリケーションソフトウェア.md "wikilink")から独立している。
  - メッセージは[バイナリ](../Page/バイナリ.md "wikilink")形式を採用している。

## 構成要素

[IP電話](../Page/IP電話.md "wikilink")網を例にして、H.323 の 4 個の構成要素 (必要とされる装置) を説明する。

### 端末

サービス[端末](../Page/端末.md "wikilink")としての機能を有する機器。

  - [パーソナルコンピュータ](../Page/パーソナルコンピュータ.md "wikilink")
  - [電話機](https://ja.wikipedia.org/wiki/電話機 "wikilink")

### ゲートウェイ

他の[通信プロトコル](../Page/通信プロトコル.md "wikilink")との相互変換を行う機器。他の網からの信号により[パケット](../Page/パケット.md "wikilink")を組み立てゲートキーパーからの指令でIP網へ送信、受信したパケットを信号に変換して他の網へ送出する。

  - [IP電話アダプタ](https://ja.wikipedia.org/wiki/IP電話アダプタ "wikilink")
  - IP-[PBX](https://ja.wikipedia.org/wiki/構内交換機 "wikilink")

### ゲートキーパー

ネットワークの接続管理や付加機能を実現する機器。H.323 ネットワークを制御する頭脳にあたる。次の機能を持つ。

  - [IPアドレス](../Page/IPアドレス.md "wikilink")と[電話番号](../Page/電話番号.md "wikilink")などの相互変換
  - 通信帯域幅制御 : [QoSのためのアドミッション制御](../Page/Quality_of_Service.md "wikilink")
  - 課金
  - 転送・保留・プレゼンス管理などの付加機能。

必須機能ではないが、通常、端末を発見し、認証・認可し、帯域を管理し、アカウントや課金の管理をするなどの機能をもつ。

### 多地点間通信装置

  - Multipoint Control Unit ([MCU](https://ja.wikipedia.org/wiki/多地点接続装置 "wikilink"))：パケットを端末に配分し、電話会議などの多地点間通信を行う機器。MCU は会議の資源を管理し、端末間の交渉をおこない、場合によってはメディア・ストリームを扱う。MCU はゲートウェイ、ゲートキーパーと同一のデバイス上に共存させることも可能である。

## H.323 におけるプロトコルとコーデック

H.323 においては下記のようなプロトコルや[コーデック](../Page/コーデック.md "wikilink")を使用することが定められている。

  - H.225 登録、許可、状態 (RAS – registration, admission, and status)
  - H.225 呼シグナリング
  - H.245 制御シグナリング
  - [RTP](../Page/Real-time_Transport_Protocol.md "wikilink") (Real-time Transport Protocol)
  - [RTCP](../Page/Real-time_Transport_Control_Protocol.md "wikilink") (Real-time Transport Control Protocol)
  - オーディオ・コーデック [G.711](../Page/G.711.md "wikilink")、[G.729](https://ja.wikipedia.org/wiki/G.729 "wikilink")、[G.723.1](https://ja.wikipedia.org/wiki/G.723.1 "wikilink")
  - ビデオ・コーデック [H.261](../Page/H.261.md "wikilink")、[H.263](../Page/H.263.md "wikilink")

コーデックとはオーディオ、ビデオなどのデータ表現形式であり、H.323 においてはリアルタイム通信に適したコーデックが指定されている。

## H.323 Annex

  - A : [H.245](https://ja.wikipedia.org/wiki/H.245 "wikilink")セッション制御メッセージ
  - B : [動画](../Page/動画.md "wikilink")のスケーラプル[符号化への対応](../Page/符号化方式.md "wikilink")
  - C : [Asynchronous Transfer Mode](../Page/Asynchronous_Transfer_Mode.md "wikilink")(ATM)での伝送
  - D : リアルタイム・[ファクシミリ](https://ja.wikipedia.org/wiki/ファクシミリ "wikilink")
  - E : [UDP通信手順](../Page/User_Datagram_Protocol.md "wikilink")
  - F : 音声専用端末制御手順
  - G : リアルタイム・テキスト・[チャット](../Page/チャット.md "wikilink")
  - H : 移動体拡張(Mobility)のアプリケーション層
  - I : 移動体拡張のトランスポート層以下
  - J : Annex Fのセキュリティ拡張
  - K : [HTTPとの連携](../Page/Hypertext_Transfer_Protocol.md "wikilink")
  - L : 起動信号
  - M : QSIG(Signaling protocol over Q reference point),ISUP([ISDN](../Page/ISDN.md "wikilink") User Part) ,DSS1(Digital Signaling System 1)のトンネリング中継
  - N : End to Endの[Quality of Service](../Page/Quality_of_Service.md "wikilink")(QoS)制御と信号伝送
  - O : [Internet Engineering Task Force](../Page/Internet_Engineering_Task_Force.md "wikilink")(IETF)標準の[IP電話](../Page/IP電話.md "wikilink")
  - P : リアルタイム・[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")中継
  - Q : 遠隔[カメラ](../Page/カメラ.md "wikilink")操作、[H.281](https://ja.wikipedia.org/wiki/H.281 "wikilink"),[H.224](https://ja.wikipedia.org/wiki/H.224 "wikilink")
  - R : 構成要素の拡張法

## 関連項目

  - [Session Initiation Protocol](../Page/Session_Initiation_Protocol.md "wikilink")
  - [IP電話](../Page/IP電話.md "wikilink")
  - [VoIP](../Page/VoIP.md "wikilink")
  - [テレビ電話](../Page/テレビ電話.md "wikilink")
  - ITU-T Q
      - [Q.931](https://ja.wikipedia.org/wiki/Q.931 "wikilink") : ISDNユーザ・網インタフェース レイヤ3仕様
      - [Q.932](https://ja.wikipedia.org/wiki/Q.932 "wikilink") : ISDN付加サービス制御手順の共通原則
  - ITU-T H
      - [H.225.0](https://ja.wikipedia.org/wiki/H.225.0 "wikilink") : パケットに基づくマルチメディア通信システムのためのシグナリングプロトコルとメディア信号のパケット化
      - [H.224](https://ja.wikipedia.org/wiki/H.224 "wikilink") : A real time control protocol for simplex applications using the H.221 LSD/HSD/HLP channels
      - [H.245](https://ja.wikipedia.org/wiki/H.245 "wikilink") : マルチメディア通信用制御プロトコル
      - [H.261](../Page/H.261.md "wikilink"), [H.263](../Page/H.263.md "wikilink"), [H.264](../Page/H.264.md "wikilink"): 動画像の圧縮符号化
      - [H.281](https://ja.wikipedia.org/wiki/H.281 "wikilink") : A far end camera control protocol for videoconferences using H.224
      - [H.450.1](https://ja.wikipedia.org/wiki/H.450.1 "wikilink") : H323における付加サービス実現のための汎用機能プロトコル
      - [H.450.2](https://ja.wikipedia.org/wiki/H.450.2 "wikilink") : H323のための通話転送付加サービス
      - [H.450.3](https://ja.wikipedia.org/wiki/H.450.3 "wikilink") : H323のための着信転送付加サービス
      - [H.450.4](https://ja.wikipedia.org/wiki/H.450.4 "wikilink") : H323のための保留呼付加サービス
      - [H.450.5](https://ja.wikipedia.org/wiki/H.450.5 "wikilink") : H323のためのコールパーク、コールピックアップ付加サービス
      - [H.450.6](https://ja.wikipedia.org/wiki/H.450.6 "wikilink") : H323のためのコールウェイティング付加サービス
      - [H.450.7](https://ja.wikipedia.org/wiki/H.450.7 "wikilink") : H323のためのメッセージウェイティング通知付加サービス
      - [H.450.8](https://ja.wikipedia.org/wiki/H.450.8 "wikilink") : H323のための名前通知付加サービス
      - [H.450.9](https://ja.wikipedia.org/wiki/H.450.9 "wikilink") : H323のための呼完了付加サービス
      - [H.450.10](https://ja.wikipedia.org/wiki/H.450.10 "wikilink") : H323のためのコールオファー付加サービス
      - [H.450.11](https://ja.wikipedia.org/wiki/H.450.11 "wikilink") : H323における呼割り込み付加サービス
      - [H.450.12](https://ja.wikipedia.org/wiki/H.450.12 "wikilink") : H323における共通情報交換ネットワーク付加機能
      - [H.460.1](https://ja.wikipedia.org/wiki/H.460.1 "wikilink") : 機能拡張のための汎用フレームワーク使用のためのガイドライン
      - [H.460.2](https://ja.wikipedia.org/wiki/H.460.2 "wikilink") : H.323ネットワークとSCNネットワーク間の番号ポータビリティインタワーキング
      - [H.460.3](https://ja.wikipedia.org/wiki/H.460.3 "wikilink") : H323システムにおける回線マップ
      - [H.460.4](https://ja.wikipedia.org/wiki/H.460.4 "wikilink") : H323呼のための呼優先度指定
      - [H.460.5](https://ja.wikipedia.org/wiki/H.460.5 "wikilink") : H.225.0 transport of multiple Q.931 information elements of the same type
      - [H.460.6](https://ja.wikipedia.org/wiki/H.460.6 "wikilink") : Extended Fast Connect feature
      - [H.460.7](https://ja.wikipedia.org/wiki/H.460.7 "wikilink") : Digit maps within H.323 systems
      - [H.460.8](https://ja.wikipedia.org/wiki/H.460.8 "wikilink") : Querying for alternate routes within H.323 systems
      - [H.460.9](https://ja.wikipedia.org/wiki/H.460.9 "wikilink") : Support for online QoS-monitoring reporting within H.323 systems
      - [H.460.10](https://ja.wikipedia.org/wiki/H.460.10 "wikilink") : Call party category within H.323 systems
      - [H.460.11](https://ja.wikipedia.org/wiki/H.460.11 "wikilink") : Delayed call establishment within H.323 systems
      - [H.460.12](https://ja.wikipedia.org/wiki/H.460.12 "wikilink") : Glare control indicator within H.323 systems
      - [H.460.13](https://ja.wikipedia.org/wiki/H.460.13 "wikilink") : Called user release control
      - [H.460.14](https://ja.wikipedia.org/wiki/H.460.14 "wikilink") : Support for Multi-Level Precedence and Preemption (MLPP) within H.323 systems
      - [H.460.15](https://ja.wikipedia.org/wiki/H.460.15 "wikilink") : Call signalling transport channel suspension and redirection within H.323 systems

## 外部リンク

  - [H.323 Information Site](http://www.packetizer.com/iptel/h323/)
  - [H.323 open source project](http://www.openh323.org)
  - [H.323 Protocol Overview](http://www.en.voipforo.com/H323/H323_objetives.php)

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink") [Category:ITU-T勧告](https://ja.wikipedia.org/wiki/Category:ITU-T勧告 "wikilink")