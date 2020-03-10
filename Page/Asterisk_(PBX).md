> この記事は[Asterisk \(PBX\)](https://ja.wikipedia.org/wiki/Asterisk_\(PBX\))から翻訳されています。


**Asterisk**（アスタリスク）は、アメリカ[アラバマ州](../Page/アラバマ州.md "wikilink")のデジウム(Digium, Inc.)が開発している[オープンソース](../Page/オープンソース.md "wikilink")のIP-[PBXのソフトウェア](https://ja.wikipedia.org/wiki/構内交換機 "wikilink")。 [GPL](../Page/GNU_General_Public_License.md "wikilink") 2 ライセンスで配布。ネーミングは[アスタリスク](https://ja.wikipedia.org/wiki/アスタリスク "wikilink")マーク（＊）に由来する。

## 概要

開発者はアメリカ企業の。開発は同社が行っているがオープンソースであり、世界中のプログラマが開発に貢献している。

[Linux](https://ja.wikipedia.org/wiki/Linux "wikilink")により開発を行われているが、他のOS上でも動作するようにポーティングされ、[FreeBSD](../Page/FreeBSD.md "wikilink")、[OpenBSD](../Page/OpenBSD.md "wikilink")、[NetBSD](../Page/NetBSD.md "wikilink")、[Solaris](../Page/Solaris.md "wikilink") 、[macOS](https://ja.wikipedia.org/wiki/macOS "wikilink")で動作している。[Windows](https://ja.wikipedia.org/wiki/Microsoft_Windows "wikilink") 2000/XP/2003ではAsteriskWin32 (Asterisk on Windows) もある。

## 特徴

特徴として次の点があげられる。

  - ボイスメール機能。留守番電話の機能として、不在時などにメッセージを記録することが可能。
  - 音声会議機能。MeetMeと呼ばれ、電話会議サービスを動作させることが可能。
  - 自動音声応答（[IVR](https://ja.wikipedia.org/wiki/IVR "wikilink")）機能。音声による自動応答を作成し、動作させることが可能。
  - 自動着信呼配分（ACD:[Automatic Call Distributor](https://ja.wikipedia.org/wiki/Automatic_Call_Distributor "wikilink")）機能。コールセンターで利用されるような、待ち時間順でつなぐことや一斉着信などの機能。
  - [PSTN](https://ja.wikipedia.org/wiki/PSTN "wikilink")（[公衆交換電話網](https://ja.wikipedia.org/wiki/公衆交換電話網 "wikilink")）への接続が可能。デジウム社やその他で発売されている回線ボードにより接続を行う。この回線ボードをZaptelコンパチブルカードと呼ぶ。この多くは日本では[技術基準適合認定](https://ja.wikipedia.org/wiki/技術基準適合認定 "wikilink")されたものではない（[技適マーク](https://ja.wikipedia.org/wiki/技適マーク "wikilink")が無い。）ので直接に接続することができない。ISPの行っている[IP電話](../Page/IP電話.md "wikilink")やひかり電話などをレジスターし利用する方法などで回線ボードなしで利用することも実現されている。
  - 保留機能。パーク保留機能が可能。日本のラインキーによる部分はまだ実装されはじめた段階。擬似的なラインキーとして利用する方法では可能。保留音は自由に選曲することができる。
  - AGIといわれるスクリプト連動機能。CGIのような使い方でモジュールを書くことが可能。
  - SLA(Shared Line Appearances)サポート。
  - [T.38](https://ja.wikipedia.org/wiki/T.38 "wikilink") パススルーサポート
  - [SNMP](https://ja.wikipedia.org/wiki/SNMP "wikilink") サポート

### 利用可能なプロトコル

  - SIP　([Session Initiation Protocol](https://ja.wikipedia.org/wiki/Session_Initiation_Protocol "wikilink"))
  - [H.323](https://ja.wikipedia.org/wiki/H.323 "wikilink")
  - IAX ([Inter-Asterisk eXchange](https://ja.wikipedia.org/wiki/Inter-Asterisk_eXchange "wikilink"))
  - [MGCP](https://ja.wikipedia.org/wiki/MGCP "wikilink") ([Media Gateway Control Protocol](https://ja.wikipedia.org/wiki/Media_Gateway_Control_Protocol "wikilink"))
  - [Skinny](https://ja.wikipedia.org/wiki/Skinny_Call_Control_Protocol "wikilink") (SCCP/Skinny Call Control Protocol)
  - UNISTIM (Nortel UNIStim/Unified Networks IP Stimulus)
  - [XMPP](https://ja.wikipedia.org/wiki/Extensible_Messaging_and_Presence_Protocol "wikilink") (Extensible Messaging and Presence Protocol)

### 利用可能な音声圧縮コーデック

  - [ADPCM](https://ja.wikipedia.org/wiki/ADPCM "wikilink")
  - [G.711](https://ja.wikipedia.org/wiki/G.711 "wikilink") ([A-law](https://ja.wikipedia.org/wiki/A-lawアルゴリズム "wikilink") と [μ-law](https://ja.wikipedia.org/wiki/μ-lawアルゴリズム "wikilink"))
  - [G.722](https://ja.wikipedia.org/wiki/G.722 "wikilink")
  - [G.723.1](https://ja.wikipedia.org/wiki/G.723.1 "wikilink")　(パススルーのみ)
  - [G.726](https://ja.wikipedia.org/wiki/G.726 "wikilink") (G.726 RFC3551とG.726 AAL2)
  - [G.729](https://ja.wikipedia.org/wiki/G.729 "wikilink") (G.729A)
  - [GSM](https://ja.wikipedia.org/wiki/GSM "wikilink")
  - [iLBC](https://ja.wikipedia.org/wiki/iLBC "wikilink")
  - SLIN　(Signed Linear PCM)
  - LPC-10
  - [Speex](https://ja.wikipedia.org/wiki/Speex "wikilink")　(SpeeX)

## 歴史

  - **2002年**
      - 1月　0.1.10がリリース。

<!-- end list -->

  - **2003年**
      - 4月　0.4.0 がリリース。

<!-- end list -->

  - **2004年**
      - 9月　1.0.0 がリリース。

<!-- end list -->

  - **2005年**
      - 11月　1.2.0 がリリース。

<!-- end list -->

  - **2006年**
      - 12月　1.4.0 がリリース。

<!-- end list -->

  - **2008年**
      - 10月　1.6.0 がリリース。

<!-- end list -->

  - **2010年**
      - 10月　1.8.0 がリリース。

<!-- end list -->

  - **2011年**
      - 12月　10.0.0 がリリース。

<!-- end list -->

  - **2012年**
      - 10月　11.0.0 がリリース。

<!-- end list -->

  - **2013年**
      - 12月　12.0.0 がリリース。

<!-- end list -->

  - **2014年**
      - 10月　13.0.0 がリリース。

## 脚注

## 関連項目

  - [インターネット電話](https://ja.wikipedia.org/wiki/インターネット電話 "wikilink")
  - [IP電話](../Page/IP電話.md "wikilink")
  - [VoIP](https://ja.wikipedia.org/wiki/VoIP "wikilink")

## 外部リンク

  - [日本Asteriskユーザ会(Googleグループ内)](https://groups.google.com/forum/#!forum/asterisk-ug)

<!-- end list -->

  - [日本におけるAsteriskの話題を中心に情報交換を行っているWiki。日本語版による音声ファイルの配布や日本独自に対応しているパッチの配布も行っているサイト。VoIP-Info.jp](http://VoIP-Info.jp/)

<!-- end list -->

  - [Asteriskを使う---ITproの連載記事](http://itpro.nikkeibp.co.jp/article/COLUMN/20070117/258890/)
      - [見積もり2億円のIP電話を820万円で構築した秋田県大館市から学べること](http://itpro.nikkeibp.co.jp/article/OPINION/20090209/324420/) (ITpro - 2009年2月9日)
      - [本当はそれほど安くないAsteriskによるIP電話](http://itpro.nikkeibp.co.jp/article/Watcher/20090318/326841/)(ITpro - 2009年3月18日)

### 公式サイト

  - [Asteriskオフィシャルサイト](http://www.asterisk.org/)

[Category:VoIPのソフトウェア](https://ja.wikipedia.org/wiki/Category:VoIPのソフトウェア "wikilink") [Category:1999年のソフトウェア](https://ja.wikipedia.org/wiki/Category:1999年のソフトウェア "wikilink")