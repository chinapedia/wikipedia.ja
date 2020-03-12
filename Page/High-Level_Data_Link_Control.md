> この記事は[High-Level Data Link Control](https://ja.wikipedia.org/wiki/High-Level_Data_Link_Control)から翻訳されています。


**High-Level Data Link Control**（ハイレベルデータリンク制御手順、以下HDLCと略す）は[国際標準化機構](https://ja.wikipedia.org/wiki/国際標準化機構 "wikilink")（ISO）によって標準化された、ビットオリエンテッドな[フレーム同期型の](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")[データリンク層](../Page/OSI参照モデル.md "wikilink")[プロトコルである](../Page/通信プロトコル.md "wikilink")。

## 概要

最初のHDLCはISOによって以下のように定義された。

  - ISO 3309 — フレーム構造
  - ISO 4335 — 処理手順の要素
  - ISO 6159 — 非平衡型処理手順
  - ISO 6256 — 平衡型処理手順

これらの定義はISO 13239に取りまとめられ、現在のHDLCの定義となっている。HDLCは[コネクションオリエンテッド](https://ja.wikipedia.org/wiki/コネクションオリエンテッド "wikilink")型通信にも[コネクションレス型通信](https://ja.wikipedia.org/wiki/コネクションレス型通信 "wikilink")にも対応できる。 [日本](https://ja.wikipedia.org/wiki/日本 "wikilink")では[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")に[JIS X 5203として](https://ja.wikipedia.org/wiki/日本工業規格（情報処理）の一覧 "wikilink")、([X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")準拠)[LAPB](https://ja.wikipedia.org/wiki/LAPB "wikilink")互換[DTEのデータリンク手順が](https://ja.wikipedia.org/wiki/データ端末装置 "wikilink")[1999年](../Page/1999年.md "wikilink")に[JIS X 5204として規格化された](https://ja.wikipedia.org/wiki/日本工業規格（情報処理）の一覧 "wikilink")。

HDLCはポイント・ツー・マルチポイントでの通信を行うことができるが、現在はほとんど [非同期平衡モード(Asynchronous Balanced Mode - ABM)を使った](https://ja.wikipedia.org/wiki/Asynchronous_Balanced_Mode "wikilink")[ポイント・ツー・ポイント](https://ja.wikipedia.org/wiki/ポイント・ツー・ポイント "wikilink")での通信でしか使われていない。HDLCにはABMの他に正規応答モード(Normal Response Mode - NRM)と非同期応答モード(Asynchronous Response Mode - ARM)の2つのモードもサポートしている。

## 歴史

HDLCは[IBM](../Page/IBM.md "wikilink")が開発した[Systems Network Architecture](../Page/Systems_Network_Architecture.md "wikilink")（SNA）のレイヤ2プロトコルである[SDLCが大元になっている](https://ja.wikipedia.org/wiki/Synchronous_Data_Link_Control "wikilink")。それを[国際電気通信連合](../Page/国際電気通信連合.md "wikilink")（ITU）が、[LAPB](https://ja.wikipedia.org/wiki/LAPB "wikilink")として[X.25](https://ja.wikipedia.org/wiki/X.25 "wikilink")プロトコル・スタックに持ち込みHDLCの誕生となった。現在、これは同期型の[PPPとして](../Page/Point-to-Point_Protocol.md "wikilink")、[インターネット](../Page/インターネット.md "wikilink")のような[WANにサーバなどを繋ぐのに用いられている](../Page/Wide_Area_Network.md "wikilink")。これと一部異なるバージョンのものが[ISDN](../Page/ISDN.md "wikilink")の制御チャンネルや[SDH多重電話回線で使用されている](../Page/Synchronous_Digital_Hierarchy.md "wikilink")。また[シスコなど一部のベンダでは](../Page/シスコシステムズ.md "wikilink")[シスコHDLC](https://ja.wikipedia.org/wiki/シスコHDLC "wikilink")のように、下位のHDLCのフレーミング技術のみを導入し、ヘッダ部分は独自といったプロトコルの開発などもしている。

## フレーミング

HDLCの[フレームは同期リンク](https://ja.wikipedia.org/wiki/フレーム_\(ネットワーク\) "wikilink")、非同期リンクに関わらず送信することが可能である。これらのリンクにはフレームの始めと終わりを見分けるメカニズムはないので、通信を行うには各フレームの始めと終わりを認識するメカニズムが必要である。フレームの始まりと終わりを認識するには、フレームの境界に“01111110”（[16進数で](https://ja.wikipedia.org/wiki/十六進記数法 "wikilink")0x7E）の8ビットコード「フレームデリミタ」（「フラグシーケンス」とも言う）を配置し、これを認識用のビット列とする。 ARM[全二重](https://ja.wikipedia.org/wiki/全二重 "wikilink")リンク上でフレームの通信がない場合、連続してフレームデリミタが送信され続け、以下のような連続したビット配列を示す。

[<File:NrziEncodedFlags.png>](https://ja.wikipedia.org/wiki/File:NrziEncodedFlags.png "fig:File:NrziEncodedFlags.png")

これを利用し[モデム](https://ja.wikipedia.org/wiki/モデム "wikilink")は[位相同期回路](../Page/位相同期回路.md "wikilink")を経由して時計をシンクロさせる。手順の実装によってはフレームデリミタの先頭ビットと最終ビットの兼用を認める（'0111111**0**1111110'）ものもある。

フレームには「情報部を持つフレーム」「制御専用のフレーム」「非番号制フレーム」の3種類がある。各フレームの内容については[フレーム構造を参照](https://ja.wikipedia.org/wiki/#Frame_Property "wikilink")。

### フレーム内容の透過性

実際に送受信されるバイナリデータはフラグシーケンスと同じビット列を含む可能性がある。そのまま送信した場合、受信する側はそのままフラグシーケンスと解釈し問題を生じ得るため、別のビット列に変換する必要がある。

同期リンク上での場合、その変換方法としてbit stuffingを使う。送信デバイスにおいて0の後ろに1が連続して5つ続いた場合、ハードウェア側でその後ろに0を挿入するといった変換を行う。受信デバイス側で0の後に1が5つ続きさらにその後ろに0があった場合、データと判断しその0を取り除く。1が6つ続いた場合はフラグシーケンスと判断して対応する。これを[ビットスタッフィング](https://ja.wikipedia.org/wiki/ビットスタッフィング "wikilink")という。

**`bit``   ``stuffing`**
`元・受信データ：01111110 01111110 01111110 01111110 …`
`送信データ　　：011111`**`0`**`1 0011111`**`0`**` 10011111 `**`0`**`1001111 1`**`0`**`10…`

[シリアルポート](../Page/シリアルポート.md "wikilink")やUniversal Asynchronous Receiver Transmitter ([UART](../Page/UART.md "wikilink")) のように8ビット（[オクテット](../Page/8ビット.md "wikilink")）単位で送出する非同期リンクにおいては、bit stuffingを行うと半端が出てしまうため別の変換を行う必要がある。代わりの変換方法は“byte stuffing”もしくは“octet stuffing”と呼ばれる。送信デバイスでデータ内のオクテットがフレームデリミタの“01111110”(0x7E)か、もしくはエスケープオクテットの“01111101”(0x7D)と同じであるものを検知すると、そのオクテットの前にエスケープオクテット“01111101”(0x7D)を挿入し、そのオクテットの先頭（最下位）から3番目のビット（16進数で20）の0と1を入れ替える。受信デバイスはエスケープオクテットを検知するとエスケープオクテットを削除し、次のオクテットの3番目のビットの0と1を入れ替える。その他の予約ビット列（[XONやXOFFなど](https://ja.wikipedia.org/wiki/ソフトウェアフロー制御 "wikilink")）やエスケープオクテット自体についても、必要であれば同様にしてエスケープできる。

**`octet``   ``stuffing`**
`元・受信データ：`*`01111110`*` 01010101 `*`01111101`*` 01011110 …`
`送信データ　　：`**`01111101`**` `*`01`***`0`***`11110`*` 01010101 `**`01111101`**` `*`01`***`0`***`11101`*` 01011110 …`

また、符号化を強化したものとして、7バイト（7オクテット）データ中の各オクテットから末尾のビットを取り除き、取り除いたビットを8バイト目に集約させる方法も規格化されている。これにより全てのオクテットの末尾が0になるため、誤り制御の強化につながる。

## フレーム構造

フレームデリミタを含むHDLCのフレーム構造は以下のようになっている。

| フレームデリミタ(0x7E) | アドレス | コントロール          | 情報                | FCS   | （任意のフレームデリミタ(0x7E)） |
| -------------- | ---- | --------------- | ----------------- | ----- | ------------------- |
| 8ビット           | 8ビット | 8ビット もしくは 16ビット | 可変長, 0もしくは8の倍数ビット | 16ビット | 8ビット                |

末端のフレームデリミタは、次のフレームの始めのフレームデリミタを兼ねている（なくてもよい）。また、制御専用のフレームと非番号制フレームは情報部を持たない。

アドレス部には送信側と受信側で共有する簡易的なアドレスが刻まれる。HDLCは通常、通信を統制する端末（1次局）と1次局からの通信命令を受ける端末（2次局）に分かれ、基本的にアドレス部にはこの2次局の簡易アドレスが書き込まれる。通常この部分は8ビットだが、16ビットに拡張したものも規格化されている。

コントロール部にはフレームの役割を指定する制御情報が書き込まれる。

| フレーム形式＼ビット | 1 | 2      | 3        | 4      | 5      | 6 | 7 | 8 |
| ---------- | - | ------ | -------- | ------ | ------ | - | - | - |
| 情報フレーム     | 0 | 送信順序番号 | P/Fフラグ   | 受信順序番号 |        |   |   |   |
| 制御専用フレーム   | 1 | 0      | 2ビット制御符号 | P/Fフラグ | 受信順序番号 |   |   |   |
| 非番号制フレーム   | 1 | 1      | モード番号1   | P/Fフラグ | モード番号2 |   |   |   |

送信・受信順序番号には0〜7の番号が入り、1フレーム送信・受信するごとに1ずつ増えていく。フレームはある程度まとめて伝送することになるため、受信時に順序が入れ替わっても順序番号を基準に整列しなおすことができる。

制御専用フレームの制御符号は2ビットなので4種類あり、00(0)で受信可能、01(1)で受信不能、10(2)で伝送に失敗したフレーム群の再送要求、11(3)で伝送に失敗したフレームのうち、特定のフレームの再送要求を表す。

非番号制フレームはモード番号1・2の切り替えによってさまざまな機能を実現し、指令と返送で合計23種類の機能を切り替えることができる。

P/Fフラグは、制御専用フレーム・非番号制フレームのうち、返送を要求するものの場合、またはその返送である場合にのみ1が入る。その他の場合は全て0となる。

コントロール部は8ビットが基本だが、アドレス部と同じく16ビットのものも規格化されている。さらに、32ビットのコントロール部を持つ規格が2つ、64ビットのものが1つ規格化されている。

情報部には伝送すべきデータが書き込まれる。このデータに関する規定はないが、通常伝送される情報は8の倍数ビットになる。これは[電話](../Page/電話.md "wikilink")、[テレタイプ](https://ja.wikipedia.org/wiki/テレタイプ "wikilink")の長距離デジタル伝送装置が8ビットずつ伝送しているのにHDLCが適応した結果である。これによりHDLCは効率的にバイナリデータを送受信できる。

FCSは（[Frame Check Sequence](https://ja.wikipedia.org/wiki/Frame_Check_Sequence "wikilink"):フレームチェックシーケンス）の略で[パリティ](../Page/パリティ.md "wikilink")チェックより洗練された方法であり、[CRCによるデータのエラー検出と訂正を行う](../Page/巡回冗長検査.md "wikilink")。 ISO/IEC 13239ではCRCの生成多項式として\(x^{16} + x^{12} + x^5 + 1\)を用いることが規定されている。なお、CRC-32によるCRC符号の生成も規格化されており、そちらでは\(x^{32} + x^{26} + x^{23} + x^{22} + x^{16} + x^{12} + x^{11} + x^{10} + x^8 + x^7 + x^5 + x^4 + x^2 + x + 1\)を使う。

## 関連項目

  - [Point-to-Point Protocol](../Page/Point-to-Point_Protocol.md "wikilink") - PPP: 2点間を接続して[データ通信](../Page/データ通信.md "wikilink")を行うための[通信プロトコル](../Page/通信プロトコル.md "wikilink")
  - [Synchronous Data Link Control](https://ja.wikipedia.org/wiki/Synchronous_Data_Link_Control "wikilink") - SDLC: 同期データリンク制御手順
  - [Serial Line Internet Protocol](../Page/Serial_Line_Internet_Protocol.md "wikilink") - SLIP: シリアル回線IP

## 外部リンク

  - [HDLC情報ページ（英語）](http://www.interfacebus.com/Design_HDLC.html)

[Category:通信プロトコル](https://ja.wikipedia.org/wiki/Category:通信プロトコル "wikilink")