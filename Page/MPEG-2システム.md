> この記事は[MPEG-2システム](https://ja.wikipedia.org/wiki/MPEG-2システム)から翻訳されています。


**MPEG-2システム**（MPEG-2 Systems）とは[MPEG-2](../Page/MPEG-2.md "wikilink")を多重化し、伝送するための規格\[1\]である。ISO/IEC 13818-1および[ITU-T](../Page/ITU-T.md "wikilink")勧告H.222.0において標準化されている。MPEG-2システムは用途別に、MPEG-2プログラムストリーム（**MPEG-2 PS**）とMPEG-2トランスポートストリーム（**MPEG-2 TS**）の2種類に分けられている。

## エレメンタリストリーム

符号化された画像・音声データのそれぞれを、**エレメンタリストリーム**（ES：Elementary Stream）と呼ぶ。MPEG-2システムファイルにおける各ES（格納可能なメディアデータ・コーデックの種類）を以下に説明する。

  - ビデオ
    [MPEG-1](../Page/MPEG-1.md "wikilink")、[MPEG-2](../Page/MPEG-2.md "wikilink")（拡張規格：[MPEG-4](../Page/MPEG-4.md "wikilink")、[MPEG-4 AVC](../Page/H.264.md "wikilink")、[VC-1](../Page/VC-1.md "wikilink")）
  - オーディオ
    [MP1](../Page/MP3.md "wikilink")、[MP2](../Page/MP3.md "wikilink")、[MP3](../Page/MP3.md "wikilink")、[AC-3](../Page/ドルビーデジタル.md "wikilink")、[リニアPCM](../Page/パルス符号変調.md "wikilink")、[DTS](https://ja.wikipedia.org/wiki/デジタル・シアター・システムズ "wikilink")（拡張規格：[AAC](../Page/AAC.md "wikilink")）
  - 静止画
    [JPEG](../Page/JPEG.md "wikilink")

なおMPEG-2システムの誕生経緯は[DVD](../Page/DVD.md "wikilink")のパッケージソフトの規格化を目指して策定されたものであるが、MPEG-2システムの規格とDVDの規格は全く等しいものではない。実際にDVDのアプリケーションフォーマットとして定められた仕様はあくまでMPEG-2システムを前提条件にしたものになる。

## エレメンタリストリームのパケット化

画像ES または 音声ES を適当な大きさに分割してパケット化したものを**PES**（Packetized Elementary Stream）と呼ぶ。MPEG-2システム規格ではESの分割の単位について詳しく定義していないが実際の運用においては映像ならピクチャ単位、音声ならブロック単位などの意味のある単位ごとに分割することが多い。PESパケットヘッダは再生時刻の情報を含むことができ、これを用いて映像と音声を同期して再生することができる。

MPEG-2システムでは、PESを多重化し伝送又は蓄積する形式の用途別に**プログラムストリーム**（Program Stream：PS）と**トランスポートストリーム**（Transport Stream：TS）の2種類が定義されている。

PSとTSはデータ形式が異なるだけであり、相互に画像を無劣化で変換することが可能である。

## プログラムストリーム

単一のプログラム（お互いに同期をとった一組の映像や音声、データの固まり）を光ディスクやHDDなどの蓄積メディア等エラーの可能性が低い環境で取り扱うことを想定した形式で、[CDなどに記録することを目的に策定された](../Page/コンパクトディスク.md "wikilink")[MPEG-1システム](https://ja.wikipedia.org/wiki/MPEG-1システム "wikilink")の拡張版でもある。DVD等の記録形式として使用されている。複数のPESパケットを連結し先頭に**パックヘッダ**（pack_header）を付与したものを**パック**（pack）と呼び、さらに複数のパックを連結したものがプログラムストリームとなる。

PSには映像や音声のPESのほかに、**Program Stream map**とよばれる各ESの詳細情報や**Program Stream directory**とよばれる再生時刻とビットストリーム上のオフセット値を含むランダムアクセスのための情報を挿入することができる。 {{-}}

## トランスポートストリーム

同時に1つ以上のプログラム\[2\]を、エラーが発生しうる環境で取り扱う放送や通信で用いることを想定した形式である。日本の地上／BSデジタル放送をはじめとして、世界各国のデジタル放送規格の多くで採用されている。[D-VHS](../Page/D-VHS.md "wikilink")や、[DVテープに](../Page/DV_\(ビデオ規格\).md "wikilink")[HDTVビデオ映像を記録する](https://ja.wikipedia.org/wiki/高精細度テレビジョン放送 "wikilink")[HDV](../Page/HDV.md "wikilink")規格、[第3世代光ディスク](../Page/第3世代光ディスク.md "wikilink")（[Blu-ray Discや](../Page/Blu-ray_Disc.md "wikilink")[HD DVD](../Page/HD_DVD.md "wikilink")）、ハイビジョンテレビ放送を録画するレコーダーなどにも採用されている。

TSにおいては、PESパケットを**トランスポートパケット**（Transport Packet。TS packetとも）と呼ばれる188バイト固定長のパケットへ分割する。このトランスポートパケットの連続が、トランスポートストリームとなる。各TSパケットには**パケット識別子**（PID）と呼ばれる13ビットの情報が含まれる。これは各トランスポートパケットのそれぞれが何を伝送しているものか示すためのものである。同一の画像、同一の音声はそれぞれ同じPIDを持つためTSを受信した側はそれを用いて元のPES（ES）に戻すことが可能である。

TSパケットの先頭4バイトにタイムスタンプ情報を付加して合計192バイトのパケットにしたTSを特に「TTS（Timestamped TS）」 \[3\] と呼び、主に放送局で用いられている。

### PSI/SI

TSでは複数のプログラムを取り扱うことが可能であるがそのTSにどのようなプログラムが存在し、TSに含まれる各ESがどのプログラムに属しているかを記した情報を**PSI**（Program Specific Information）という。PSIは 動画や音声とは別のPIDを持つTSパケットとして、TSに挿入される。PSIは、以下のようなものが存在する。特にPID=0のものはPATと呼ばれるほかPMT、CATなどが存在する。

  - PAT（Program Association Table）
    あるTS内に含まれるプログラム一覧を、PMTのPID一覧で格納したのがPATである。PATのPIDは必ず0と決まっている。なお[ワンセグ](../Page/ワンセグ.md "wikilink")では帯域削減の為含まれず、PMTは0x1FC8もしくは0x1FC9といった特定の値を持つ。
  - PMT（Program Map Table）
    あるプログラムに含まれる画像や音声などの各PIDを格納したのがPMTである。PMTから画像や音声などのPIDを得ることが出来れば、それらPIDのついたTSパケットを抽出することでプログラムを再生できる。
  - CAT（Conditional Access Table）
    限定受信をサポートする情報が含まれる。CATのPIDは必ず1と決まっている。

MPEG-2 System規格ではPSIのみが記述されているがMPEG-2 TSを採用する多くのデジタル放送規格ではPSIを拡張し、番組情報などを含めた**SI**（Service Information）が規定されている。

SIはPSIの一部であると見なして、PSI/SI情報としてまとめて扱う場合が多い。またSIには[EPGのほぼ全てが含まれるので](../Page/電子番組ガイド.md "wikilink")、SI/EPGとまとめて扱う場合も多い

[ARIBがARIB](../Page/電波産業会.md "wikilink") STD-B10で規定するSIには、以下のようなものが存在する。

  - NIT（Network Information Table）
    チャンネル番号や[変調方式](../Page/変調方式.md "wikilink")、[ガードインターバル](../Page/ガードインターバル.md "wikilink")など、送信するネットワークに関する情報が含まれる。NITのPIDは必ず0x10と決まっている。
  - BIT（Broadcaster Information Table）
    放送局識別情報（BSD）や系列情報（地上D）、各SIテーブルの再送周期、SIの掲載期間、ロゴ情報の伝送方法など放送局のSI送信情報が含まれる。BITのPIDは必ず0x24と決まっている。
  - SDT（Service Description Table）
    チャンネルの名称が含まれる。また各チャンネル（サービス）で送出されるEITの種類、デジタルコピー制御情報も含まれる。SDTのPIDは必ず0x11と決まっている。
  - EIT（Event Information Table）
    番組の名称や放送日時、放送内容など番組に関連する情報が含まれる。EPGは主にこの情報を用いて作成される。EITのPIDは必ず0x12と決まっている。
    EITはその示す内容により自局の現在及び次の番組、他局の現在及び次の番組、自局のそれ以外を含む番組、他局のそれら以外を含む番組の4種類に大別される。自局の現在及び次の番組に関する情報は必ず送出する必要があるがその他の情報は送出が任意であり、また送出の頻度も重要性に応じて小さくすることができる。
  - TOT（Time Offset Table）
    現在の日付、時刻、およびサマータイムの情報が含まれる。TOTのPIDは0x14と決まっている。
  - NBIT（Network Board Information Table）
    案内等の掲示板情報が含まれる。
  - LDT（Linked Description Table）
    他のテーブルから参照するための情報を集約している。
  - TDT（Time Date Table）
    現在の日付、時刻に関する情報が含まれる。ただしTOTにはTDTの全ての情報が含まれるため送信されるのはTDTかTOTのいずれかのみ（PIDは双方とも0x14）と規定されており、実際のところTDTだけが送信されている。

番組より小さい単位（番組内イベント）の内容を記述するための、さらにいくつかの拡張が行われている。

  - LIT（Local Event Information Table）
    番組内イベントに関する情報が含まれる。
  - ERT（Event Relation Table）
    番組、および番組内イベントの関係に関する情報が含まれる。
  - ITT（Index Transmission Table）
    番組内イベントに関係する時刻情報が含まれる。時刻情報はLITにも含まれているが放送ごとに異なる値が必要になるため、LITとは別に送出される。

ARIB STD-B1、B21では以下のような情報も規定されている。

  - SDTT（Software Download Trigger Table）
    デジタル放送受信機の最新ソフトウェア（Engineering Stream Serviceで伝送される）の伝送スケジュールが記載される。本テーブルは、全放送局で全く同一の情報が伝送されている。実際のデータはARIB STD-B16で規定されるDCT（Download Control Table）、DLT（Download Table）で伝送される。
  - CDT（Common Data Table）（地上D）
    EPG画面等で表示される、各サービス毎に対応したロゴ情報が伝送される。ロゴ情報は1サービスあたり6種類（それぞれ大きさが異なるpngファイル）がセクション化され、伝送される。

### トランスポートストリームのエラー検出

トランスポートパケットヘッダには同じPID内において値が1ずつ増加する**continuity_counter**という4ビットのカウンタがあり、TS受信側でこのカウンタの不連続を検出することでトランスポートパケットのロストを検出することができる。またトランスポートパケットヘッダの先頭バイトは必ず**sync_byte**という特定の値（0x47）となっており、伝送路上のエラーで受信側が一時的にパケットの先頭を見失ったとしても188バイト毎のsync_byteを検出して同期しなおすことで比較的早期に同期を回復することができる。加えてPSIはCRCチェックサムを必ず含み、PSIのエラーで受信機が混乱することを防いでいる。

## 脚注

## 関連項目

  - [MP4](../Page/MP4.md "wikilink")
  - [コンテナフォーマット](../Page/コンテナフォーマット.md "wikilink")

## 外部リンク

  - [VIDEO-ITを取り巻く市場と技術 第3回 MPEG-2 TSの概要 前編](http://www.mpeg.co.jp/libraries/video_it/video_03.html)・[後編](http://www.mpeg.co.jp/libraries/video_it/video_04.html)
  - [VIDEO-ITを取り巻く市場と技術 第6回 MPEG-2 PS概要 前編](http://www.mpeg.co.jp/libraries/video_it/video_06.html)・[後編](http://www.mpeg.co.jp/libraries/video_it/video_07.html)

[Category:ビデオ](https://ja.wikipedia.org/wiki/Category:ビデオ "wikilink") [Category:動画ファイルフォーマット](https://ja.wikipedia.org/wiki/Category:動画ファイルフォーマット "wikilink") [Category:MPEG](https://ja.wikipedia.org/wiki/Category:MPEG "wikilink")

1.  現在ではMPEG-2システムの拡張が行われており、MPEG-2誕生以後に開発された[H.264](../Page/H.264.md "wikilink")や[VC-1](../Page/VC-1.md "wikilink")の映像コーデックを多重化することも可能となっている。
2.  TS（トランスポート・ストリーム）の特徴を利用した実例は次の通り。デジタルテレビ放送の有る1つの放送局でHD放送は1つのプログラム（チャンネル）として送信するが、マルチチャンネル構成の場合はSD放送で3つ分まで放送できる。
3.   第二分冊 第二編 8.1.4