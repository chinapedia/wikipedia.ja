> この記事は[W-OAM](https://ja.wikipedia.org/wiki/W-OAM)から翻訳されています。


[WILLCOM-phs-station-8elements.jpg](https://ja.wikipedia.org/wiki/File:WILLCOM-phs-station-8elements.jpg "fig:WILLCOM-phs-station-8elements.jpg")　2004年\]\] [250px](https://ja.wikipedia.org/wiki/画像:Ws002in_rx420al.jpg "wikilink") **W-OAM**（ダブリュ・オーエーエム、ウィルコム・オーエーエム）は、[Y\!mobile](https://ja.wikipedia.org/wiki/Y!mobile "wikilink")(旧[ウィルコム](../Page/ウィルコム.md "wikilink"))の[高度化PHS](../Page/高度化PHS.md "wikilink")による通信サービスの名称。*WILLCOM Optimized Adaptive Modulation*の略。

## 概要

既存の[PHS](../Page/PHS.md "wikilink")規格の[変調方式](../Page/変調方式.md "wikilink")を改良し、データ通信の高速化・カバーエリアや屋内浸透度を向上させたものであり、「[高度化PHS](../Page/高度化PHS.md "wikilink")」の一種である。かつて[次世代PHS](https://ja.wikipedia.org/wiki/次世代PHS "wikilink")と称されていた[XGP規格とは別物である](https://ja.wikipedia.org/wiki/eXtended_Global_Platform "wikilink")。

W-OAM（[W-OAM typeGを含む](https://ja.wikipedia.org/wiki/#W-OAM_typeG "wikilink")）により通信しようとする場合には、W-OAM / typeGに対応した[端末](../Page/端末.md "wikilink")を使用して、W-OAMに対応した[基地局](https://ja.wikipedia.org/wiki/基地局 "wikilink")と通信する必要がある。通信しようとする基地局側がW-OAMに対応していない等の場合には、自動的に従来（現行PHS）の変調方式（1x/32k[bps](../Page/ビット毎秒.md "wikilink")）により通信する。なお、ここで言う*1x*とは、「\(n\)x : リンク数（束ねるマルチリンクの数）」に基づき、リンク数が1である事を示している。

W-OAM対応の基地局が設置された対応エリアは、大都市圏の高トラフィックエリアを中心に順次拡大していくとしている。

また、W-OAMによる通信においては、[無線](../Page/無線.md "wikilink")[伝送路](../Page/伝送路.md "wikilink")の状態（[電波](../Page/電波.md "wikilink")の状態）に応じて、良好な場合にはより高速な変調方式を、基地局との通信が不安定な場合(距離が離れている、障害物がある場合など)には低速だがよりエラーに強い変調方式を、自動的・動的に選択し変更する「[適応変調](https://ja.wikipedia.org/wiki/適応変調 "wikilink")」方式が採用されている。

W-OAMの開始にあたって、トラフィックが高速・大容量化することによる[NTT](../Page/日本電信電話.md "wikilink")（[東日本](../Page/東日本電信電話.md "wikilink")・[西日本](../Page/西日本電信電話.md "wikilink")）[接続料](https://ja.wikipedia.org/wiki/接続料 "wikilink")の増加対策のために、NTT交換局内にITX（Ip Transit eXchange）というトラフィックバイパス装置を設置し、これにW-OAMを含めた基地局を接続して半ば独自網のネットワークを構築している。これにより、W-OAMに[音声通話定額制](../Page/音声通話定額制.md "wikilink")も含め増大するトラフィックがNTTの交換機・通信設備を経由することがなくなり、接続料の抜本的削減が可能となっている。

## 通信方式

従来（現行）のPHSの変調方式は[π/4 shift QPSK](https://ja.wikipedia.org/wiki/デジタル変調#位相偏移変調 "wikilink")（1x/32kbps）である。なお、π/4 shift QPSKとQPSKは厳密には異なるが、各方面では便宜上単にQPSKと記述される事も多い（本項目でも単にQPSKと記述する）。また同じく、W-OAMで採用された変調方式はD8PSKとπ/2 shift BPSKであり、8PSKとBPSKとでは厳密には異なるが、8PSK・BPSKと記述される事も多い（本項目でも単に8PSK・BPSKと記述する）。

### W-OAM

[2006年](../Page/2006年.md "wikilink")2月23日の「W-OAM」サービス開始時は、従来のQPSKに加えて、より高速な[8PSK](https://ja.wikipedia.org/wiki/デジタル変調#位相偏移変調 "wikilink")（1x/51kbps）、より低速だがエラーに強い[BPSK](https://ja.wikipedia.org/wiki/デジタル変調#位相偏移変調 "wikilink")（1x/13kbps）が採用された。

現在W-OAMは、データ通信専用型端末のほか、[W-SIM](../Page/W-SIM.md "wikilink")や音声端末の一部にも採用されている。

  - （対応[チップセット](../Page/チップセット.md "wikilink")） AX20Pシリーズ（P2チップセット）：スロット[ダイバーシティ](../Page/ダイバーシティ.md "wikilink")ー、ハーフレート、無手順パケット、コアモジュール標準\[1\]。
  - （対応チップセット） ML7257：スロットダイバーシティー、ハーフレート、CPU=[ARM7TDMI](https://ja.wikipedia.org/wiki/ARMアーキテクチャ#ARM7 "wikilink")\[2\]。

### W-OAM typeG

2007年4月5日にサービス開始した「W-OAM typeG」においては、上記W-OAMのBPSK/QPSK/8PSK変調方式に加えて、さらに高速な[QAM変調方式が採用される](https://ja.wikipedia.org/wiki/デジタル変調#直交振幅変調 "wikilink")。各変調方式でのレートは以下となる。

  - 16QAM（1x/約63kbps）
  - 32QAM（1x/約80kbps）
  - 64QAM（1x/約100kbps）

なお、W-OAM typeGにおいては、高速化と併せて、[適応変調](https://ja.wikipedia.org/wiki/適応変調 "wikilink")の切換の高速化および[RTTの改善が図られるという](https://ja.wikipedia.org/wiki/ラウンドトリップタイム "wikilink")\[3\]。

  - （対応チップセット） AX30Pシリーズ（P3チップセット）：最大2Mbps（2xRF、スロット連結仕様）、高度化適用変調、スロット連結、[FEC](https://ja.wikipedia.org/wiki/Forward_Error_Correction "wikilink")\[4\]。サンプル出荷が2007年7月に開始された\[5\]。

## 通信速度

各種変調方式とチャンネル多重数の組み合わせにより、以下の表のような高速化が計画・検討中である\[6\]。

**無線区間の最大[スループット](../Page/スループット.md "wikilink")**

|           |            |             |             |             |          |          |
| --------- | ---------- | ----------- | ----------- | ----------- | -------- | -------- |
| 変調方式＼リンク数 | 1x         | 2x          | 4x          | 8x          | 12x      | 16x      |
| **BPSK**  | **13kbps** | **26kbps**  | **52kbps**  | **104kbps** | 156kbps  | 208kbps  |
| QPSK      | 32kbps     | 64kbps      | 128kbps     | 256kbps     | 384kbps  | 512kbps  |
| **8PSK**  | **51kbps** | **102kbps** | **204kbps** | **408kbps** | 612kbps  | 816kbps  |
| *16QAM*   | 約*63kbps*  | 約*125kbps*  | 約*250kbps*  | 約*500kbps*  | 約750kbps | 約1Mbps   |
| *32QAM*   | 約*80kbps*  | 約*160kbps*  | 約*320kbps*  | 約*640kbps*  | 約960kbps | 約1.3Mbps |
| *64QAM*   | 約*100kbps* | 約*200kbps*  | 約*400kbps*  | 約*800kbps*  | 約1.2Mbps | 約1.6Mbps |

（注）

  - 無線区間とは基地局～端末間
  - <span style="background-color:#FFFFFF;border: 1px solid gray">白地</span>は現行PHSにおける通信方式（～8x）。
  - <span style="background-color:#FFDDDD;border: 1px solid gray">**赤地の太字**</span>はW-OAMにおいて追加される通信方式。
  - <span style="background-color:#DDFFDD;border: 1px solid gray">*緑地の斜字*</span>はW-OAM typeGにおいて追加される通信方式。
  - PSK(phase shift keying)=[位相偏移変調](https://ja.wikipedia.org/wiki/デジタル変調#位相偏移変調 "wikilink")
  - QAM(quadrature amplitude modulation)=[直交振幅変調](https://ja.wikipedia.org/wiki/デジタル変調#直交振幅変調 "wikilink")
  - \(n\)x : リンク数（束ねるマルチリンクの数）

なお、エントランス回線（収容局⇔基地局間の回線）が従来型の[ISDN](../Page/ISDN.md "wikilink")の場合、その部分が[ボトルネック](../Page/ボトルネック.md "wikilink")となり[スループット](../Page/スループット.md "wikilink")は**最大で512kbps程度に制限**されるため、[光回線等の](../Page/光通信.md "wikilink")[IP回線化が必要であるとしている](../Page/Internet_Protocol.md "wikilink")\[7\]。

**ISDNエントランス回線における、W-OAM typeGの端末最大スループット**

|           |           |            |            |            |
| --------- | --------- | ---------- | ---------- | ---------- |
| 変調方式＼リンク数 | 1x        | 2x         | 4x         | 8x         |
| BPSK      | 13kbps    | 26kbps     | 52kbps     | 104kbps    |
| QPSK      | 32kbps    | 64kbps     | 128kbps    | 256kbps    |
| 8PSK      | 51kbps    | 102kbps    | 204kbps    | 408kbps    |
| 16QAM     | 約63kbps   | 約125kbps   | 約250kbps   | 約500kbps   |
| 32QAM     | *約64kbps* | *約128kbps* | *約256kbps* | *約512kbps* |
| 64QAM     | *約64kbps* | *約128kbps* | *約256kbps* | *約512kbps* |

*（無線区間の変調方式にかかわらず、1x=最大64kbpsに制限される。）*

### フレームフォーマット

<timeline> ImageSize = width:800 height:120 PlotArea = width:720 height:95 left:65 bottom:20 AlignBars = justify

Colors =

`   id:dbpsk  value:rgb(1,0.7,0.7)   # light red`
`   id:dqpsk  value:rgb(0.7,0.7,0.7) # light`
`   id:d8psk  value:rgb(1,0.7,1)     # light purple`
`   id:d16qam value:rgb(1,1,0.7)     # light blue`
`   id:d32qam value:rgb(0.7,1,0.7)   # light green`
`   id:d64qam value:rgb(0.7,0.7,1)   # light yellow`
`   id:filler value:gray(0.8)        # background bar`
`   id:black  value:black`

Period = from:0 till:625 TimeAxis = orientation:horizontal ScaleMajor = unit:year increment:125 start:0 ScaleMinor = unit:year increment:5 start:0

PlotData=

` align:center textcolor:black fontsize:S mark:(line,black) width:25 shift:(0,-5)`

` bar:BPSK color:dbpsk fontsize:S`
` from: 0 till: 10 text:R~2 shift:(2,2) # 2`
` from: 10 till: 16 text:S~S~1 fontsize:XS align:left shift:(-1,6) # 3`
` from: 16 till: 31 text:PR~3 shift:(0,2) #  6`
` from: 31 till: 83 text:UW~10 shift:(0,2) # 16`
` from: 83 till: 104 text:CI~4 shift:(0,2) # 20`
` from: 104 till: 520 text:I(TCH)~80 shift:(0,2) # 100`
` from: 520 till: 584 text:CRC~12 shift:(0,2) # 112`

` bar:QPSK color:dqpsk fontsize:S`
` from: 0 till: 10 text:R~4 shift:(2,2) # 2`
` from: 10 till: 16 text:S~S~2 fontsize:XS align:left shift:(-1,6) # 3`
` from: 16 till: 31 text:PR~6 shift:(0,2) # 6`
` from: 31 till: 73 text:UW~16 shift:(0,2) # 14`
` from: 73 till: 83 text:CI~4 fontsize:XS align:right shift:(6,2) # 16`
` from: 83 till: 125 text:SA~16 shift:(0,2) # 24`
` from: 125 till: 541 text:I(TCH)~160 shift:(0,2) # 104`
` from: 541 till: 584 text:CRC~16 shift:(0,2) # 112`

` bar:8PSK color:d8psk fontsize:S`
` from: 0 till: 10 text:R~4 shift:(2,2) # 2`
` from: 10 till: 16 text:S~S~2 fontsize:XS align:left shift:(-1,6) # 3`
` from: 16 till: 31 text:PR~6 shift:(0,2) # 6`
` from: 31 till: 73 text:UW~16 shift:(0,2) # 14`
` from: 73 till: 80 text:CI~4 fontsize:XS align:right shift:(6,2) # 15+1/3`
` from: 80 till: 108 text:SA~16 shift:(0,2) # 20+2/3`
` from: 108 till: 552 text:I(TCH)~256 shift:(0,2) # 106`
` from: 552 till: 580 text:CRC~16 shift:(0,2) # 111+1/3`
` from: 580 till: 584 text:PAD~2 fontsize:XS align:left shift:(-2,4)  # 112`

` bar:16QAM color:d16qam fontsize:S`
` from: 0 till: 10 text:R~4 shift:(2,2) # 2`
` from: 10 till: 16 text:S~S~2 fontsize:XS align:left shift:(-1,6) # 3`
` from: 16 till: 52 text:PR~14 shift:(0,2) # 10`
` from: 52 till: 93 text:UW~16 shift:(0,2) # 18`
` from: 93 till: 99 text:CI~4 fontsize:XS align:right shift:(6,2) # 19`
` from: 99 till: 120 text:SA~16 shift:(0,2) # 23`
` from: 120 till: 557 text:I(TCH)~336 shift:(0,2) # 107`
` from: 557 till: 578 text:CRC~16 shift:(0,2) # 111`
` from: 578 till: 584 text:PAD~4 fontsize:XS align:left shift:(-2,4) # 112`

</timeline>

  - 横軸、[マイクロ秒](https://ja.wikipedia.org/wiki/マイクロ秒 "wikilink")。

### 音声通話におけるW-OAM

[音声通話](https://ja.wikipedia.org/wiki/音声通話 "wikilink")時には、従来のQPSKによる通信（32k[bps](../Page/ビット毎秒.md "wikilink")[ADPCM](https://ja.wikipedia.org/wiki/Adaptive_Differential_Pulse_Code_Modulation "wikilink")）に加えて、低速だがエラーに強いBPSKによる通信も用いられる（対応音声端末のみ）。この場合、[音声符号化](https://ja.wikipedia.org/wiki/音声符号化 "wikilink")方式は16kADPCMとなる。従来のQPSKによる通信に比べ、通話時にも実効上の移動耐性・屋内浸透性が若干上がるとされている。

## 対応端末

### データ通信端末

  - W-OAM対応（BPSK/QPSK/8PSK）
      - [AX520N](https://ja.wikipedia.org/wiki/AX520N "wikilink")
      - [AX420N](https://ja.wikipedia.org/wiki/AX420N "wikilink")
      - [AX420S](../Page/AX420S.md "wikilink")
  - W-OAM typeG対応（BPSK/QPSK/8PSK/16QAM/32QAM/64QAM）
      - [AX530S](https://ja.wikipedia.org/wiki/AX530S "wikilink")
      - [AX530IN](https://ja.wikipedia.org/wiki/AX530IN "wikilink")

### 音声端末

  - W-OAM対応（BPSK/QPSK/8PSK）
      - [WX130S](../Page/WX130S.md "wikilink") : 8PSK非対応
      - [WX220J](https://ja.wikipedia.org/wiki/WX220J "wikilink") : [チップセット](../Page/チップセット.md "wikilink")ML7257\[8\]
      - [WX321J](../Page/WX321J.md "wikilink") : [チップセット](../Page/チップセット.md "wikilink")ML7257\[9\]
      - [WX320K](../Page/WX320K.md "wikilink") : [チップセット](../Page/チップセット.md "wikilink")ML7257\[10\]
      - [WX320KR](https://ja.wikipedia.org/wiki/WX320KR "wikilink")
      - [WX320T](../Page/WX320T.md "wikilink")
      - [WX330K](https://ja.wikipedia.org/wiki/WX330K "wikilink")
      - [WX331K](../Page/WX331K.md "wikilink")
      - [WX331KC](https://ja.wikipedia.org/wiki/WX331KC "wikilink")
      - [WX333K](https://ja.wikipedia.org/wiki/WX333K "wikilink")
      - [WX334K](https://ja.wikipedia.org/wiki/WX334K "wikilink")
      - [WX334K P](https://ja.wikipedia.org/wiki/WX334K_P "wikilink")
      - [WX330J](https://ja.wikipedia.org/wiki/WX330J "wikilink")
      - [WX330J E](https://ja.wikipedia.org/wiki/WX330J_E "wikilink")
      - [WX340K](https://ja.wikipedia.org/wiki/WX340K "wikilink")
      - [WX341K](https://ja.wikipedia.org/wiki/WX341K "wikilink")
      - [WX341K P](https://ja.wikipedia.org/wiki/WX341K_P "wikilink")
      - [WX350K](https://ja.wikipedia.org/wiki/WX350K "wikilink")
      - [WX01A](https://ja.wikipedia.org/wiki/WX01A "wikilink")
      - [WX02A](https://ja.wikipedia.org/wiki/WX02A "wikilink")
      - [WX03A](https://ja.wikipedia.org/wiki/WX03A "wikilink")
      - [WX05A](https://ja.wikipedia.org/wiki/WX05A "wikilink")
      - [WX06A](https://ja.wikipedia.org/wiki/WX06A "wikilink")
      - [WX01J](https://ja.wikipedia.org/wiki/WX01J "wikilink")
      - [WX01JR](https://ja.wikipedia.org/wiki/WX01JR "wikilink")
      - [WX01NX](https://ja.wikipedia.org/wiki/WX01NX "wikilink")
      - [WX01K](https://ja.wikipedia.org/wiki/WX01K "wikilink")
      - [WX02K](https://ja.wikipedia.org/wiki/WX02K "wikilink")
      - [WX03K](https://ja.wikipedia.org/wiki/WX03K "wikilink")
      - [WX05K](https://ja.wikipedia.org/wiki/WX05K "wikilink")
      - [WX07K](https://ja.wikipedia.org/wiki/WX07K "wikilink")
      - [WX08K](https://ja.wikipedia.org/wiki/WX08K "wikilink")
      - [WX09K](https://ja.wikipedia.org/wiki/WX09K "wikilink")
      - [WX11K](https://ja.wikipedia.org/wiki/WX11K "wikilink")
      - [WX01S](https://ja.wikipedia.org/wiki/WX01S "wikilink")
      - [WX02S](https://ja.wikipedia.org/wiki/WX02S "wikilink")/XWX02S
      - [WX03S](https://ja.wikipedia.org/wiki/WX03S "wikilink")
      - [WX04S](https://ja.wikipedia.org/wiki/WX04S "wikilink")
      - [WX01SH](https://ja.wikipedia.org/wiki/WX01SH "wikilink")
      - [WX02SH](https://ja.wikipedia.org/wiki/WX02SH "wikilink")
      - [WX03SH](https://ja.wikipedia.org/wiki/WX03SH "wikilink")
      - [301JR](https://ja.wikipedia.org/wiki/301JR "wikilink")
      - [301KC](https://ja.wikipedia.org/wiki/301KC "wikilink")
      - [401AB](https://ja.wikipedia.org/wiki/401AB "wikilink")
      - [401KC](https://ja.wikipedia.org/wiki/401KC "wikilink")

<!-- end list -->

  - W-OAM typeG対応（BPSK/QPSK/8PSK/16QAM/32QAM/64QAM）
      - [WX12K](https://ja.wikipedia.org/wiki/WX12K "wikilink")
      - [402KC](https://ja.wikipedia.org/wiki/402KC "wikilink")

### スマートフォン

  - W-OAM対応（BPSK/QPSK/8PSK）
      - [WX04K](https://ja.wikipedia.org/wiki/WX04K "wikilink")

<!-- end list -->

  - W-OAM typeG対応（BPSK/QPSK/8PSK/16QAM/32QAM/64QAM）
      - [WX10K](https://ja.wikipedia.org/wiki/WX10K "wikilink")
      - [WX04SH](https://ja.wikipedia.org/wiki/WX04SH "wikilink")
      - [WX05SH](https://ja.wikipedia.org/wiki/WX05SH "wikilink")

### W-SIM(通信モジュール)

  - W-OAM対応（BPSK/QPSK/8PSK）
      - [RX420AL](https://ja.wikipedia.org/wiki/RX420AL "wikilink")
      - [RX420IN](https://ja.wikipedia.org/wiki/RX420IN "wikilink")
  - W-OAM typeG対応（BPSK/QPSK/8PSK/16QAM/32QAM/64QAM）
      - [RX430AL](https://ja.wikipedia.org/wiki/RX430AL "wikilink")

### W-OAM対応W-SIMが接続可能なSIM STYLE端末

  - データ通信端末
      - [WS002IN](../Page/WS002IN.md "wikilink") / "DD"
      - [WS008HA](https://ja.wikipedia.org/wiki/WS008HA "wikilink") [ExpressCard](../Page/ExpressCard.md "wikilink")アダプタ
      - [WS014IN](https://ja.wikipedia.org/wiki/WS014IN "wikilink")
  - 音声端末
      - [WS001IN](../Page/WS001IN.md "wikilink")
      - [WS003SH](https://ja.wikipedia.org/wiki/WS003SH "wikilink") / [W-ZERO3](../Page/W-ZERO3.md "wikilink") [1](http://www.willcom-inc.com/ja/lineup/ws/003sh/index.html)
      - WS004SH / W-ZERO3 [2](http://www.willcom-inc.com/ja/lineup/ws/004sh/index.html)
      - [WS005IN](../Page/WS005IN.md "wikilink") / nico. [3](http://www.willcom-inc.com/ja/lineup/ws/005in/index.html)
      - [WS007SH](../Page/WS007SH.md "wikilink") / W-ZERO3 \[es\] [4](http://www.willcom-inc.com/ja/lineup/ws/007sh/index.html)
      - [WS009KE](../Page/WS009KE.md "wikilink") / 9(nine) [5](http://www.willcom-inc.com/ja/lineup/ws/009ke/index.html)
      - [WS011SH](../Page/WS011SH.md "wikilink") / Advanced/W-ZERO3 \[es\] [6](http://www.willcom-inc.com/ja/lineup/ws/011sh/index.html)
      - [WS016SH](../Page/WS016SH.md "wikilink")
      - [WS018KE](../Page/WS018KE.md "wikilink")
      - [WS020SH](../Page/WS020SH.md "wikilink")
      - [WS023T](https://ja.wikipedia.org/wiki/WS023T "wikilink")
      - [WS027SH](https://ja.wikipedia.org/wiki/WS027SH "wikilink")
  - その他端末
      - [WS024BF](https://ja.wikipedia.org/wiki/WS024BF "wikilink")（モバイル[Wi-Fi](../Page/Wi-Fi.md "wikilink")[ルータ](../Page/ルーター.md "wikilink")）
      - [WS026T](https://ja.wikipedia.org/wiki/WS026T "wikilink")（ブラウジングデバイス）

## 料金など

従来の料金プランでそのまま利用ができ、別途オプション料金は不要。W-OAM通信およびW-OAM typeG通信を利用したために別途課金されることはない。なおパケット従量課金制の料金コース等を契約中の場合でも、高速化した分だけ単位時間あたりのパケット消費量が増加することになるが、あるデータをダウンロードするのに必要な総パケット量に変化が生じるわけではないので、ダウンロードに要する時間が短縮されるだけで料金に変化はない。ただし、高速化によって快適になったために以前より総パケット量を増やすような通信をすれば、当然、料金は上がることになる。

なお、中継基地局であるホームアンテナ（レピーター）にはW-OAM/typeG通信や8xパケット通信に対応したものは2007年2月現在で存在しない。ただし、W-OAM/typeG通信においては、ホームアンテナを経由せずともBPSK変調により、低ビットレートながら実効上の屋内浸透性を向上させた通信を行うとされている。

## 脚注

<references />

## 関連項目

  - [高度化PHS](../Page/高度化PHS.md "wikilink")
  - [PHS](../Page/PHS.md "wikilink")
  - [ウィルコム](../Page/ウィルコム.md "wikilink")
  - [AIR-EDGE](../Page/AIR-EDGE.md "wikilink")

## 外部リンク

  - [WILLCOM - データ通信サービスの高速・快適化について 〜PHS高度化通信規格「W-OAM」の導入〜](http://www.willcom-inc.com/ja/corporate/press/2006/01/27/index.html)　

[Category:PHS_(ウィルコム)](https://ja.wikipedia.org/wiki/Category:PHS_\(ウィルコム\) "wikilink") [Category:モバイルネットワーク](https://ja.wikipedia.org/wiki/Category:モバイルネットワーク "wikilink")

1.  [【WIRELESS JAPAN 2006】エービットブースで“次世代PHS”の姿が見えた！：デジタルARENA](http://arena.nikkeibp.co.jp/news/20060721/117754/)
2.  [Unveils Base Band LSI, Compliant with Advanced PHS Standard | OKI Global](http://www.oki.com/en/press/2007/z06146e.html)（英語）
3.  [WILLCOM沖縄｜PHS高度化通信規格「W-OAM」の高速化について](http://www.willcom-inc.com/ja/okinawa/corporate/press/2007/01/22/index_03.html) [【WILLCOM FORUM & EXPO 2007】 近氏、次世代PHSの強みをアピール](http://k-tai.impress.co.jp/cda/article/event/34082.html)
4.
5.  [【ワイヤレスジャパン報告】エイビットブースのPHSチップロードマップに「AX30Pシリーズ」のサンプル出荷開始を確認：デジタルARENA](http://arena.nikkeibp.co.jp/article/news/20070723/1001735/)
6.  [W-OAMのイメージ](http://k-tai.impress.co.jp/cda/parts/image_for_link/111232-27537-11-1.html)
    [2006年のウィルコムは「ADVANCED & COMFORTABLE」](http://k-tai.impress.co.jp/cda/article/news_toppage/27537.html)
7.  [WILLCOM｜ますます速く快適に](http://www.willcom-inc.com/ja/service/reason/comfortably/index.html) [基地局のIP化を実施](http://k-tai.impress.co.jp/cda/parts/image_for_link/136375-31966-12-1.html)
8.
9.
10.