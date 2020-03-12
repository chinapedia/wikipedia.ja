> この記事は[Real Time Streaming Protocol](https://ja.wikipedia.org/wiki/Real_Time_Streaming_Protocol)から翻訳されています。


**Real Time Streaming Protocol**（リアルタイム・ストリーミング・プロトコル, 略称：**RTSP**）は [IETF](../Page/Internet_Engineering_Task_Force.md "wikilink") において標準化されたリアルタイム性のあるデータの配布 ([ストリーミング](../Page/ストリーミング.md "wikilink")) を制御するための[プロトコル](../Page/プロトコル.md "wikilink")であり、ストリーミングデータ自体の配信を行うためのプロトコルではない。1998 年 4 月にその最初の版が RFC 2326 として標準化されたが、様々な問題点があることが指摘され、改訂が続けられている。

## 概要

RTSP は[オーディオ](https://ja.wikipedia.org/wiki/音声 "wikilink")、[ビデオなどの](https://ja.wikipedia.org/wiki/映像 "wikilink")[マルチメディア](../Page/マルチメディア.md "wikilink")・データをふくむ[サーバ](../Page/サーバ.md "wikilink")を遠隔操作するためのプロトコルであり、テープレコーダのように再生、停止、記録 (録音) などの操作ができる (巻き戻しや早送りの機能はない)。[SIP](../Page/Session_Initiation_Protocol.md "wikilink") (セッション確立プロトコル) とはちがって RTSP においてはサーバと[クライアントとが明確に区別され](../Page/クライアント_\(コンピュータ\).md "wikilink")、データの流れは基本的にサーバからクライアントへの一方向であるが、サーバからクライアントに送付する要求も定義されている。すなわち、[要求-応答モデル](https://ja.wikipedia.org/wiki/要求-応答モデル "wikilink")としてみると、サーバ とクライアントの役割が逆転することもある。

サーバからクライアントへのデータ転送 (RTSP においてはプレゼンテーションとよばれる) には通常[Real-time Transport Protocol](../Page/Real-time_Transport_Protocol.md "wikilink") (RTP) が使用されるが、それに限定されてはいない。RTSP によって制御されるデータのながれに関しては "RTSP セッション" が存在するが、RTSP 自体には、SIP と同様にセッションの概念はない。SIP と同様、RTSP も [HTTP](../Page/Hypertext_Transfer_Protocol.md "wikilink") (ハイパーテキスト転送プロトコル) に似せてある。RTSP の下位のプロトコルとしては、SIP とはちがって、[TCP](../Page/Transmission_Control_Protocol.md "wikilink") のように高信頼なプロトコルの使用が前提とされている。ただし、RTSP の改訂にあたっては低信頼なプロトコルを使用できるようにする方向性が示されている。

RTSP がサポートする操作はつぎの3 つである。

  - 1\. メディアサーバからのメディアのとりだし

RTSP を使用して[メディア](../Page/メディア.md "wikilink")・データをとりだすことができる。そのきっかけとしてよくあるのは [WWW](../Page/World_Wide_Web.md "wikilink") においてメディアへのリンクをクリックすることであり、この場合プレゼンテーションの記述は HTTP によってメディアサーバにあたえられる。

  - 2\. メディアサーバを会議に参加させること

マルチメディア会議においてメディアを再生したり、会議を記録したりするために RTSP を使用してメディアサーバを会議に参加させることができる。会議自体の制御はたとえば SIP によっておこなわれる。

  - 3\. メディアをプレゼンテーションにくわえること

RTSP を使用してとくにライブ・プレゼンテーションにおいて、メディアをプレゼンテーションに参加させることができる。 RTSP をあつかうメディアサーバは RTSP セッションの状態を管理する必要がある。

RFC 2326 にはセキュリティに関する記述がわずかしかないが、改訂中の仕様においては[セキュリティや](https://ja.wikipedia.org/wiki/情報セキュリティ "wikilink")[プライバシー](../Page/プライバシー.md "wikilink")を守るための機構についても記述されている。

## RTSP における標準的なシーケンス

以下の例は改訂中の仕様から引用したものであり、クライアント C がメディアサーバ V (video.example.com)およびA (audio.example.com) から映画をうけとるときのシーケンスである。メディア記述は Web サーバ W に格納されている。

`C->W:  GET /twister.sdp HTTP/1.1`
`   Host: www.`[`example.com`](https://ja.wikipedia.org/wiki/example.com "wikilink")
`   Accept: application/sdp`

`W->C:  HTTP/1.0 200 OK`
`   Date: 23 Jan 1997 15:35:06 GMT`
`   Content-Type: application/sdp`

`   v=0`
`   o=- 2890844526 2890842807 IN IP4 192.16.24.202`
`   s=RTSP Session`
`   e=adm@example.com`
`   m=audio 0 RTP/AVP 0`
`   a=control:`<rtsp://audio.example.com/twister/audio.en>
`   m=video 0 RTP/AVP 31`
`   a=control:`<rtsp://video.example.com/twister/video>

`C->A:  SETUP `<rtsp://audio.example.com/twister/audio.en>` RTSP/1.0`
`   CSeq: 1`
`   User-Agent: PhonyClient/1.2`
`   Transport: RTP/AVP/UDP;unicast;client_port=3056-3057`

`A->C:  RTSP/1.0 200 OK`
`   CSeq: 1`
`   Session: 12345678`
`   Transport: RTP/AVP/UDP;unicast;client_port=3056-3057;`
`              server_port=5000-5001`

`C->V:  SETUP `<rtsp://video.example.com/twister/video>` RTSP/1.0`
`   CSeq: 1`
`   User-Agent: PhonyClient/1.2`
`   Transport: RTP/AVP/UDP;unicast;client_port=3058-3059`

`V->C:  RTSP/1.0 200 OK`
`   CSeq: 1`
`   Session: 23456789`
`   Transport: RTP/AVP/UDP;unicast;client_port=3058-3059;`
`              server_port=5002-5003`

`C->V:  PLAY `<rtsp://video.example.com/twister/video>` RTSP/1.0`
`   CSeq: 2`
`   User-Agent: PhonyClient/1.2`
`   Session: 23456789`
`   Range: smpte=0:10:00-`

`V->C:  RTSP/1.0 200 OK`
`   CSeq: 2`
`   Session: 23456789`
`   Range: smpte=0:10:00-0:20:00`
`   RTP-Info: url=`<rtsp://video.example.com/twister/video>`;`
`         seq=12312232;rtptime=78712811`

`C->A:  PLAY `<rtsp://audio.example.com/twister/audio.en>` RTSP/1.0`
`   CSeq: 2`
`   User-Agent: PhonyClient/1.2`
`   Session: 12345678`
`   Range: smpte=0:10:00-`

`A->C:  RTSP/1.0 200 OK`
`   CSeq: 2`
`   User-Agent: PhonyClient/1.2`
`   Session: 12345678`
`   Range: smpte=0:10:00-0:20:00`
`   RTP-Info: url=`<rtsp://audio.example.com/twister/audio.en>`;`
`       seq=876655;rtptime=1032181`

`C->A:  TEARDOWN `<rtsp://audio.example.com/twister/audio.en>` RTSP/1.0`
`   CSeq: 3`
`   User-Agent: PhonyClient/1.2`
`   Session: 12345678`

`A->C:  RTSP/1.0 200 OK`
`   CSeq: 3`

`C->V:  TEARDOWN `<rtsp://video.example.com/twister/video>` RTSP/1.0`
`   CSeq: 3`
`   User-Agent: PhonyClient/1.2`
`   Session: 23456789`

`V->C:  RTSP/1.0 200 OK`
`   CSeq: 3`

## 外部リンク

  - RFC 2326 - Real-Time Streaming Protocol
  - RFC 4566 - Session Description Protocol

[Category:RFC](https://ja.wikipedia.org/wiki/Category:RFC "wikilink")