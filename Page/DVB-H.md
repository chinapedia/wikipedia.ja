> この記事は[DVB-H](https://ja.wikipedia.org/wiki/DVB-H)から翻訳されています。


**DVB-H**（Digital Video Broadcasting - Handheld）とは移動体テレビの標準規格の一つである。すなわち、携帯可能の受信機のための放送サービスに関する技術規格である。DVB-Hは[2004年](../Page/2004年.md "wikilink")11月、[ETSIがEN](../Page/欧州電気通信標準化機構.md "wikilink") 302 304として採用した。DVB-H（EN 302 304）規格文書は DVB-H 公式サイトからダウンロード可能\[1\]。[欧州連合](https://ja.wikipedia.org/wiki/欧州連合 "wikilink")もDVB-Hを公式に承認している\[2\]\[3\]\[4\]。競合する規格としては、[DMB](../Page/DMB.md "wikilink")と[ワンセグ](../Page/ワンセグ.md "wikilink")がある。

## 技術

一連の[DVB放送規格の中でも最近開発された規格である](../Page/デジタルビデオブロードキャスティング.md "wikilink")。DVB-Hは地上[デジタルテレビ](https://ja.wikipedia.org/wiki/デジタルテレビ "wikilink")の規格である[DVB-T](https://ja.wikipedia.org/wiki/DVB-T "wikilink")（Digital Video Broadcasting - Terrestrial）の上位規格であり、携帯機器向けの規格が追加されている。

DVB-H は高データ転送レートの通信経路を提供し、それ専用の受信機で受信することもできるし[携帯電話](../Page/携帯電話.md "wikilink")などに組み込んだ受信機能で受信することもできる。

[時分割多重化](../Page/時分割多重化.md "wikilink")により、小型携帯端末での電力消費を抑えるようになっている。IPデータグラムは短い時間スロット内にバースト転送される。各バーストには最大2メガビットのデータが含まれる（[パリティビット](../Page/パリティビット.md "wikilink")を含む）。191ビットのデータに対して64ビットのパリティビットがあり、[リード・ソロモン符号](../Page/リード・ソロモン符号.md "wikilink")で符号化されている。受信機は選択したサービスが放送されているデータバーストのみを受信し、それを[バッファ](../Page/バッファ.md "wikilink")に格納する。データの内容がアプリケーションの場合は全部を受信し終えてから実行するし、通常の放送の場合はそのまま表示する。

電力消費の低減は受信機がON/OFFされている時間に依存する。ひとつのDVB-Hストリームに10以上のサービスが時分割されて放送されている場合、90%程度の電力削減となる。DVB-HはDVB-H Validation Task Forceが注意深く評価してきた（[ETSI](../Page/欧州電気通信標準化機構.md "wikilink") Technical Report TR 102 401 参照）。

## 周波数帯域

以下の周波数帯域で動作するよう設計されている。

  - [VHF-III](../Page/超短波.md "wikilink")（170-230 MHz、またはその一部）
  - [UHF-IV/V](../Page/極超短波.md "wikilink")（470-862 MHz、またはその一部）
  - L band（1.452-1.492 GHz）

DVB-HはDVB-Tと多重化によって共存できる。

## DVB-IPDC

DVB-IPDCはIP[データ放送](../Page/データ放送.md "wikilink")に関するDVBの規格であり、[Internet Protocol](../Page/Internet_Protocol.md "wikilink") に基づいた商用のモバイルテレビサービスを展開するのに必須の部分である。DVB-IPDCはDVB-Hの物理層として設計されたが、DVB-SHなどの他のモバイルテレビ規格でも使われている。

モバイルテレビの観点ではDVB-IPDCは何が配信されるのか、どう配信されるのか、どう記述されるのか、どう保護されるのかを規定している。システムアーキテクチャ、[ユースケース](../Page/ユースケース.md "wikilink")、DVB PSI/SI信号、電子サービスガイド（ESG）、コンテンツ配信プロトコル（CDP）、サービス購入と保護（SPP）などをカバーしている。そのほとんどがETSIの正式な規格として発表されている。DVB-IPDC の全規格は [dvb-h.org](http://www.dvb-h.org/technology.htm) で入手可能である。

## DVB-SH

DVB-SH（移動体向けの衛星放送サービス）は、DVB-HとETSI SDR（衛星デジタルラジオの規格）を混合した規格である。類似のアーキテクチャは既に[衛星DMB](https://ja.wikipedia.org/wiki/衛星DMB "wikilink")、[XM Satellite Radio](https://ja.wikipedia.org/wiki/XM_Satellite_Radio "wikilink")、[Sirrus Satellite Radio](https://ja.wikipedia.org/wiki/Sirrus_Satellite_Radio "wikilink")、[モバHO\!](../Page/モバHO!.md "wikilink")などがあるが、DVB-SHはより強力である。想定されているシステムでは強力な[静止衛星](../Page/静止衛星.md "wikilink")で屋外と一部の屋内をカバーし、地上のリピーター・ネットワークによって都市部の屋内もカバーする。

[タレス・アレーニア・スペース](../Page/タレス・アレーニア・スペース.md "wikilink")は、2007年中のDVB-SH用衛星の打ち上げを予定している。[ユーテルサット](../Page/ユーテルサット.md "wikilink")と[SESアストラ](https://ja.wikipedia.org/wiki/SESアストラ "wikilink")はヨーロッパ全土をカバーするS band（2-4GHz帯）の衛星を2009年に打ち上げる予定である。DVB-SHの衛星放送サービスは2009年に運用開始される予定だが、地上ネットワークを使ったDVB-SHサービスはそれ以前に開始される見込みである。半導体チップメーカーのDiBcomはS bandのDVB-H対応のチップセットを設計中であり、SAGEMはUHFとS bandの両方に対応したDVB-H対応携帯電話を開発中である。これは、DVBの公式なプロジェクトである。DVB Technical Moduleは2006年6月、Study Mission on SSP（移動体向け衛星放送サービス）を立ち上げ\[5\] 標準規格の開発を開始した。その成果として2007年2月に標準規格が提出された\[6\]。

フランスの産業技術革新庁は、[アルカテル・ルーセント](../Page/アルカテル・ルーセント.md "wikilink")が主導するTVMSL（DVB-SH 規格開発を推進しているプロジェクト）を通して資金援助を行っている。TVMSLには他にSAGEM、[アレーニア・アエロナウティカ](https://ja.wikipedia.org/wiki/アレーニア・アエロナウティカ "wikilink")、RFS、[フィリップス](../Page/フィリップス.md "wikilink")、DiBcom、TeamCast、UDcast、[CNRS](../Page/フランス国立科学研究センター.md "wikilink")、[INRIA](https://ja.wikipedia.org/wiki/INRIA "wikilink")、フランス原子力庁などが参加している\[7\]\[8\]\[9\]\[10\]。

## DVB-H2

後継の規格であるDVB-H2は2007年に策定が開始され、2008年中に完成する予定である。DVB-H2とDVB-T2が相互に関連したものになることが予想されている。

## 試行地域

DVB-Hは以下のような都市や国で試行されている。

  - 国や地域

<!-- end list -->

  -
    [アイルランド島](../Page/アイルランド島.md "wikilink")\[11\]、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")\[12\]、[マレーシア](https://ja.wikipedia.org/wiki/マレーシア "wikilink")、[シンガポール](https://ja.wikipedia.org/wiki/シンガポール "wikilink")\[13\]、[南アフリカ共和国](https://ja.wikipedia.org/wiki/南アフリカ共和国 "wikilink")、[台湾](https://ja.wikipedia.org/wiki/台湾 "wikilink")\[14\]、[ニュージーランド](../Page/ニュージーランド.md "wikilink")\[15\]、[フィリピン](https://ja.wikipedia.org/wiki/フィリピン "wikilink")、[スリランカ](../Page/スリランカ.md "wikilink")、[モロッコ](../Page/モロッコ.md "wikilink")

<!-- end list -->

  - 都市

<!-- end list -->

  -
    [ヘルシンキ](../Page/ヘルシンキ.md "wikilink")、[ベルリン](https://ja.wikipedia.org/wiki/ベルリン "wikilink")、[ケンブリッジ](../Page/ケンブリッジ.md "wikilink")、[ピッツバーグ](https://ja.wikipedia.org/wiki/ピッツバーグ "wikilink")、[パリ](https://ja.wikipedia.org/wiki/パリ "wikilink")、[テヘラン](../Page/テヘラン.md "wikilink")、[マドリード](../Page/マドリード.md "wikilink")、[シドニー](../Page/シドニー.md "wikilink")\[16\]、[ハーグ](../Page/デン・ハーグ.md "wikilink")、[ブリュッセル](../Page/ブリュッセル.md "wikilink")、[ベルン](../Page/ベルン.md "wikilink")、[ウィーン](https://ja.wikipedia.org/wiki/ウィーン "wikilink")、[コペンハーゲン](../Page/コペンハーゲン.md "wikilink")、[ブダペスト](../Page/ブダペスト.md "wikilink")、[エアランゲン](../Page/エアランゲン.md "wikilink")\[17\]

完全なリストは [dvb-h.org](http://www.dvb-h.org/services.htm) にある。

## 運用開始地域

[アルバニア](../Page/アルバニア.md "wikilink")ではDigitALBが2006年[12月20日](../Page/12月20日.md "wikilink")、全国サービスを開始した。受信機器が市場に出回るようになったのは2007年4月である。

[フィンランド](../Page/フィンランド.md "wikilink")では、2006年3月にDigita がDVB-Hネットワーク運用の許可を得た。2006年5月、Digitaは[ノキア](../Page/ノキア.md "wikilink")とDVB-Hサービスのためのプラットフォームについて提携。当初、2006年12月1日に運用開始予定だったが放送素材の著作権にからんだ問題で延期。[ヘルシンキ](../Page/ヘルシンキ.md "wikilink")、[オウル](../Page/オウル.md "wikilink")、[トゥルク](../Page/トゥルク.md "wikilink")などを含む地域をカバーする予定（人口の25%）。2007年[5月10日](../Page/5月10日.md "wikilink")、Mobiili-TVが商用サービスを開始した。

[インド](../Page/インド.md "wikilink")では、公共放送のPrasar Bharti（通称：DD）が[ノキア](../Page/ノキア.md "wikilink")とDVB-Hに関して提携。各都市での受信状況を検証するための試行が行われている。DDは[ニューデリー](../Page/ニューデリー.md "wikilink")では既に8チャンネルの放送を行っている。

[イタリア](../Page/イタリア.md "wikilink")では3 Italia が2006年5月から、Telecom Italia MobileとMediasetは2006年6月から、Vodafone Italyは2006年12月から全国サービスを開始している。

[シンガポール](https://ja.wikipedia.org/wiki/シンガポール "wikilink")ではTVMobileがDVB技術を使ってニュース、娯楽番組、音楽コンテンツなどを放送している。

[フィリピン](https://ja.wikipedia.org/wiki/フィリピン "wikilink")では、SMARTがモバイルテレビサービスの*MyTV*を立ち上げた。[ノキア](../Page/ノキア.md "wikilink")製のNokia N92とN77という携帯電話でしか視聴できない\[18\]\[19\]。

[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")では、Modeo（Crown Castle の子会社）が全国サービスを予定している。2006年にニューヨーク市でサービスを開始し、2007年中に全国30都市に展開する予定である。2006年4月、SES AmericanとAloha Partnersが新たなサービスの開始を発表した。Hiwireと名づけられ、2006年末ごろラスベガスで試行を開始。それぞれ使用する周波数帯域が異なる。

[ベトナム](https://ja.wikipedia.org/wiki/ベトナム "wikilink")では、VTCが2006年12月21日に全国サービスを立ち上げた。

O2 Irelandは2007年3月に[ダブリン](../Page/ダブリン.md "wikilink")地域で試行を開始した。

[フランス](https://ja.wikipedia.org/wiki/フランス "wikilink")、[スペイン](https://ja.wikipedia.org/wiki/スペイン "wikilink")、[南アフリカ共和国](https://ja.wikipedia.org/wiki/南アフリカ共和国 "wikilink")では2007年中の全国サービス開始が予定されている。[オーストリア](../Page/オーストリア.md "wikilink")、[ドイツ](https://ja.wikipedia.org/wiki/ドイツ "wikilink")、[スイス](../Page/スイス.md "wikilink")では2008年の予定。

[中国](../Page/中国.md "wikilink")では、Shanghai Media Groupと[中国中央電視台](../Page/中国中央電視台.md "wikilink")が政府の許可を得ている。試行中であり、2008年の[北京オリンピック前にサービスを開始しようとしていた](https://ja.wikipedia.org/wiki/2008年北京オリンピック "wikilink")。

[マレーシア](https://ja.wikipedia.org/wiki/マレーシア "wikilink")では、U Mobileが2007年末までにDVB-Hに基づいたモバイルテレビ放送を開始することを発表した。*Mobile Live TV*と名づけられている\[20\]。

[ケニア](../Page/ケニア.md "wikilink")でもDVB-HサービスのDStv Mobileがある。南アフリカの企業・Digital Mobile TVがナイロビ地域向けに行っているものである。

## 対応機器

  - [GIGABYTE](../Page/GIGABYTE.md "wikilink") - GSmart t600、GSmart q60（いずれも、DVB-T、DVB-H、T-DMB、DAB 対応）
  - [LGグループ](../Page/LGグループ.md "wikilink") - U900、KU950、U960
  - [モトローラ](../Page/モトローラ.md "wikilink") - A680i
  - [ノキア](../Page/ノキア.md "wikilink") - Nokia 7710（DVB-H 対応実験機）、Nokia N92、Nokia N77、Nokia N96
  - [サムスングループ](../Page/サムスングループ.md "wikilink") - SGH-P910、SGH-P920、SGH-P930、SGH-P940、SGH-F510
  - [ソニー・エリクソン・モバイルコミュニケーションズ](https://ja.wikipedia.org/wiki/ソニー・エリクソン・モバイルコミュニケーションズ "wikilink") - W960i
  - [フィリップス](../Page/フィリップス.md "wikilink") - HotMAN2
  - [SAGEM](../Page/SAGEM.md "wikilink") - My Mobile TV
  - [ZTE](https://ja.wikipedia.org/wiki/中興通訊 "wikilink") - N7100

## 開発ツール

  - [Tea Vui Huang's DVB-H ESG Simulator](http://teavuihuang.com/esg)
  - [AMUSE DVB-H tools](http://amuse.ftw.at/downloads/encapsulator)

## 脚注

## 関連項目

  - [DAB](../Page/DAB.md "wikilink")（Digital Audio Broadcasting）
  - [DMB](../Page/DMB.md "wikilink")（Digital Multimedia Broadcasting）
  - [デジタル・ラジオ・モンディエール](../Page/デジタル・ラジオ・モンディエール.md "wikilink")（DRM）
  - [電子番組ガイド](../Page/電子番組ガイド.md "wikilink")
  - [ISDB](../Page/ISDB.md "wikilink")（Integrated Services Digital Broadcasting）
  - [ワンセグ](../Page/ワンセグ.md "wikilink")
  - [衛星放送](../Page/衛星放送.md "wikilink")
  - [スペクトル効率の比較表](https://ja.wikipedia.org/wiki/スペクトル効率#比較表 "wikilink")
  - [WiMAX](https://ja.wikipedia.org/wiki/WiMAX "wikilink")

## 外部リンク

  - [DVB-H.org](http://www.dvb-h.org) - DVB プロジェクトのDVB-H公式サイト
  - [DVB Project](http://www.dvb.org/) - DVB 公式サイト
  - [ETSI](http://www.etsi.org/)
  - [Mobile DTV Alliance](http://www.mdtvalliance.org/)

### 技術情報

  - [DVB Standards & BlueBooks](http://www.dvb.org/technology/standards/)
  - ["DVB-H — the emerging standard for mobile data communication"](http://www.ebu.ch/en/technical/trev/trev_301-dvb-h.pdf) [欧州放送連合](../Page/欧州放送連合.md "wikilink")（EBU）Technical Review
  - [EBU Technical Review](http://www.ebu.ch/en/technical/trev/trev_frameset-index.html)

### その他

  - [DVB-Hチューナー付き携帯電話一覧](http://www.phonegg.com/List/DVB-H-Cell-Phones.html)
  - [DigiTAG DVB-H Handbook](http://www.digitag.org/DTTResources/DVBHandbook.pdf)
  - [European Audiovisual Observatory](http://www.obs.coe.int)

[Category:デジタルテレビ](https://ja.wikipedia.org/wiki/Category:デジタルテレビ "wikilink") [Category:工業規格](https://ja.wikipedia.org/wiki/Category:工業規格 "wikilink") [Category:電子工学](https://ja.wikipedia.org/wiki/Category:電子工学 "wikilink")

1.  [DVB-H公式サイト](http://www.dvb-h.org/)
2.  [Mobile broadcasting is a tremendous opportunity for Europe to maintain its leadership](http://ec.europa.eu/information_society/newsroom/cf/itemlongdetail.cfm?item_id=3535) Europe's Information Society、[2007年](../Page/2007年.md "wikilink")[7月18日](../Page/7月18日.md "wikilink")
3.  [The Commission adopted a Communication on Strengthening the Internal Market for Mobile TV](http://ec.europa.eu/information_society/policy/ecomm/doc/library/communications_reports/mobile_tv/409_en_original.pdf) Europe's Information Society、2007年7月18日
4.  [EU endorses Nokia-backed DVB-H Mobile broadcasting standard](http://www.iht.com/articles/ap/2007/07/18/business/EU-FIN-EU-Mobile-Broadcasting.php) Herald Tribune、2007年7月18日
5.  [DVB TM-SSP](http://www.dvb.org/groups_modules/technical_module/tmssp/index.xml?groupID=59)
6.  [dvb.org: DVB approves DVB-SH specification](http://www.dvb.org/news_events/news/dvb_approves_dvbsh_specif/index.xml)
7.  [Alcatel Unlimited mobile TV](http://www.alcatel.com/mobileTV/)
8.  [A matter of spectrum mobile TV](http://www.mobileeurope.co.uk/magazine/features.ehtml?o=2030)
9.  [Alcatel adds satellite to mobile TV picture](http://www.pcadvisor.co.uk/news/index.cfm?newsid=5850)
10. [Ultimited Mobile TV for the Mass Market](http://www.alcatel.com/com/en/appcontent/apl/S0206-MOBILE_TV-EN_tcm172-641791635.pdf)
11. [O2 and Arqiva launch DVB-H trial in Ireland](http://www.dtg.org.uk/news/news.php?id=2298)
12. [UK's first DVB-H mobile TV trial goes live](http://www.dtg.org.uk/news/news.php?id=1180)
13. [PGK launches DVB-H trial in Singapore](http://www.charged.mobi/article.php?id_article=1748) Charged.mobi
14. [Taiwan kicks off DVB-H trial](http://www.mobile-ent.biz/news/28733/Taiwan-kicks-off-DVB-H-trial) mobile-ent.biz
15. [Peek at where-ever when-ever cell TV](http://www.nzherald.co.nz/section/story.cfm?c_id=5&objectid=10434227) New Zealand Herald
16. [Launch of world-first high power DVB-H trial in Sydney](http://www.dba.org.au/index.asp?display=news&newsID=704) Dba.org.au
17. [DVB-H Versuchssender Erlangen](http://www.like.e-technik.uni-erlangen.de/propro/dvb-h/index.html)
18. [About SMART MyTV](http://www.dvb-h.org/Services/services-philippines-mytv.htm)
19. [MyTV FAQs](http://www.smart.com.ph/Gold/FAQs/myTV_FAQs.htm)
20. [1](http://corporate.u.com.my/sec_press/pdf/News%20-%20070618%20Nokia%20MiTV%20MobTV%20announcement-vers-June18-7pm.pdf) Official Press Release Annoucement by U Mobile