> この記事は[TOPS](https://ja.wikipedia.org/wiki/TOPS)から翻訳されています。


**TOPS**（Total Operations Processing System、総合運行管理システム）は、鉄道システムの保有する[鉄道車両](../Page/鉄道車両.md "wikilink")を管理するコンピュータシステムである。[サザン・パシフィック鉄道](https://ja.wikipedia.org/wiki/サザン・パシフィック鉄道 "wikilink")で開発されたこのシステムは広く販売され、[イギリス国鉄](https://ja.wikipedia.org/wiki/イギリス国鉄 "wikilink")が採用したことで広く知られている。

## 初期の開発

[1960年代](../Page/1960年代.md "wikilink")初頭、技術への取り組みで一歩先んじていた[サザン・パシフィック鉄道](https://ja.wikipedia.org/wiki/サザン・パシフィック鉄道 "wikilink")は総合運行管理コンピュータシステムを開発し、Total Operations Processing System の頭文字をとって TOPS と命名した。 その開発意図は[鉄道車両](../Page/鉄道車両.md "wikilink")にかかわる保守履歴、車両配置、運行記録といった全ての書類をコンピュータ上の情報に置き換え、保守部門の操作端末から常時データ更新することにあった。紙ベースではこれら情報の追跡、更新、検索いずれも困難であり、電話でやりとりするしかなかった。コンピュータ化により鉄道資産の管理と有効活用が容易になった。

システムを他の鉄道会社に売るのが開発コストを転嫁する方法の一つであるのはもちろんであり、[サザン・パシフィック鉄道](https://ja.wikipedia.org/wiki/サザン・パシフィック鉄道 "wikilink")もそうしたに過ぎない。アメリカの少なからざる鉄道会社が、世界中の多くの鉄道会社同様にこのシステムを購入した。

## イギリス国鉄での採用

1960年代後半、 [イギリス国鉄](https://ja.wikipedia.org/wiki/イギリス国鉄 "wikilink")は合理化策の調査で、TOPSが[カナダ国鉄](https://ja.wikipedia.org/wiki/カナダ国鉄 "wikilink")で使われているのを知り、[ソースコード](../Page/ソースコード.md "wikilink")ごとシステムを購入し (当時、[メインフレーム](../Page/メインフレーム.md "wikilink")上の大規模システムはではソースコードごと購入するのが普通だった) て序々に[実装](https://ja.wikipedia.org/wiki/実装 "wikilink")していった。当時、イギリス政府は国営企業に対してイギリス製品を購入させる「バイ・ブリティッシュ」政策で臨んでおり、TOPS の運用に必要な[IBM 360メインフレームの購入には](https://ja.wikipedia.org/wiki/System/360 "wikilink")[ヒース内閣の承認が必要だった](https://ja.wikipedia.org/wiki/エドワード・ヒース "wikilink")。

TOPSの導入により従来の形式・車両番号の付与体系を変更する必要が生じた。[蒸気機関車](../Page/蒸気機関車.md "wikilink")には5桁までの数字が、[ディーゼル機関車](../Page/ディーゼル機関車.md "wikilink")と[電気機関車](../Page/電気機関車.md "wikilink")にはそれぞれD、Eではじまる4桁の番号がそれぞれ独立した体系で付与されたため、蒸気・ディーゼル・電気と最大3輌の機関車が同じ数字で重複する可能性があった。TOPSは数字以外の文字列で車両を区別できないため、各車両に数字だけの識別符号を重複なく付与する形に変更することとなった。

### TOPS番号

[thumb](https://ja.wikipedia.org/wiki/ファイル:British_Rail_Class_31-4_dataplate.jpg "wikilink")。電気暖房を搭載する派生形式31/4形の諸元標記。\]\]TOPSで必要とされたのは番号の連続性だけだったが、改番の際に5ないし6桁のTOPS番号を二つの部分に分けて付番する方式が採用された。1形式で1000輌を越えるものはなかったので、下3桁は個々の形式の車両・編成番号が001から999まで、また上位2ないし3桁が形式番号として機関車および電車・気動車の形式単位で付与された。桁の分割を強調するために「47 401」のように空白を挟んで書かれることが多いが、TOPSの内部処理では空白を含まず、システムでの表示も '47401' となる。

番台区分にあたる派生形式をスラッシュ '/' に派生形式番号を置く慣例もTOPSの制約に縛られず用いられ、例として47形の派生形式47/4形は「47 401」から始まる番号が付与される。派生形式中の両数が99両を越える場合には100以上の番号も付与され、200両以上からなる47/4形の場合、47/5形と47/6形を飛ばして「47/7形」の47 701から始まる。しかし、[158/**0**形は](https://ja.wikipedia.org/wiki/イギリス国鉄158形気動車 "wikilink") 158 **7**01 から始まるといった例外はある。

機関車には01から98、船舶に99、気動車に100から299、電車には300から599が、900番台は電車・気動車タイプの事業用車 (大半が営業用車からの改造) に割り当てられている。詳細は以下のとおり。更なる詳細は[イギリス鉄道の機関車・電車・気動車の車両形式を参照](https://ja.wikipedia.org/wiki/:en:British_Locomotive_and_Multiple_Unit_Numbering_and_Classification "wikilink")。

  - 01 - 69: [ディーゼル機関車](../Page/ディーゼル機関車.md "wikilink")
  - 70 - 79: 直流電気機関車
  - 80 - 96: 交流電気機関車
  - 97: 事業用機関車
  - 98: 蒸気機関車
  - 99: 船舶（イギリス国鉄籍）
  - 100 - 199: 機械式・液体式気動車
  - 200 - 299: 電気式気動車
  - 300 - 399: 交流電車（架空電車線方式）
  - 400 - 499: 直流電車（第三軌条式・イングランド南部用）
  - 500 - 599: 直流電車（その他）
  - 600 - 699: 未使用

イギリス国鉄民営化後はディーゼル機関車に70番台を付与して[70形が](https://ja.wikipedia.org/wiki/イギリス鉄道70形ディーゼル機関車 "wikilink")2008年に登場したほか、700番台が[テムズリンク](https://ja.wikipedia.org/wiki/テムズリンク "wikilink")用の電車[700形に](https://ja.wikipedia.org/wiki/イギリス鉄道700形電車 "wikilink")、800番台が[都市間高速鉄道計画](https://ja.wikipedia.org/wiki/都市間高速鉄道計画 "wikilink")による高速車両[800形](https://ja.wikipedia.org/wiki/イギリス鉄道800形 "wikilink")・[801形に付与されているなどの変化が見られる](https://ja.wikipedia.org/wiki/イギリス鉄道801形電車 "wikilink")。

[客車](../Page/客車.md "wikilink")および電車・気動車には1両単位で5桁の車両番号が割り当てられている。1980年代初頭からは機関車と重複する番号の割り当ては禁じられたが、それ以前は番号の前の文字符号も含めて扱われていたため重複があり得る。詳細は[イギリスの客車・貨車の車両番号を参照のこと](https://ja.wikipedia.org/wiki/:en:British_Carriage_and_Wagon_Numbering_and_Classification "wikilink")。

機関車には1972年からTOPS番号が割り振られたが、電車および気動車への適用は遅れた。[52形など廃車予定の形式では](https://ja.wikipedia.org/wiki/:en:British_Rail_Class_52 "wikilink")、TOPS番号付与後も1970年代遅くまで従来の「D」を前置した番号で運用されていたものもある。

## 最近の展開

TOPSの導入から数十年が経過すると、システムの陳腐化が目立つようになった。メインフレームとテキスト端末の組合せ、コマンドベースの設計は不親切なもので操作ミスも発生しやすい。加えてTOPSは独自のプログラミング言語 TOPSTRAN (厳密には別言語ではなく、IBM アセンブラマクロ) で書かれており、保守要員のプログラマの訓練が日増しに困難になっている。イギリス国鉄の分割民営化も TOPS にとっては深刻な問題である。TOPS はそもそも分割民営化を想定して設計されてはいない上に、必要な情報更新を怠っている列車運行会社もあるからである。

TOPSを活用しより使い易いユーザインタフェースを追加実装しようという「TOPS2000」計画がある。TOPS以外にも[TRUSTやGeniusといったシステムが並立しているが](https://ja.wikipedia.org/wiki/:en:TRUST "wikilink")、いずれも TOPSの代替には至っていない。

## 出力例

TOPS の典型的な出力例として、[ウィンズフォード近くのオーヴァー](https://ja.wikipedia.org/wiki/:en:Winsford "wikilink")・アンド・ファートン (Over & Wharton) から[レディング](../Page/レディング.md "wikilink")西分岐点へ向かう、25両編成の貨物列車の場合を示す。[1](http://www.southdevonrailway.org/SDDT/NewsLetter-8.html)

    K383400 0010 2837 22/10/86 U483 ON N199 BY KO
    TRAIN ENQUIRY RESPONSE FOR 377Z380 22   TFA - 9KJ
    ACTUAL TRAIN ID 377Z380 22 BOOKED 7Z380
    DEP OVER&WHAR 1520 22    2 HRS 20 MINS LATE FOR REASON L CAT B  SECTOR 5
    LOCO       25901
    LOCO       25908
      25 LDS    0 MTYS    888 TONNES   799 T/FT  418 POTENTIAL VAC BRAKE FORCE
    STATION         CONSIST      ARR        DEP      LDS MTYS   SCHEDULE
    37015 OVER&WHAR                         1520     025 000    71212
    65700 BESCOTYD    NRP        1707 EST   1709 EST 025 000
    74260 READINGWJ  DETAIL      2007 EST            025 000
    END

[Category:情報システム](https://ja.wikipedia.org/wiki/Category:情報システム "wikilink") [Category:鉄道運行管理システム](https://ja.wikipedia.org/wiki/Category:鉄道運行管理システム "wikilink") [Category:イギリスの鉄道](https://ja.wikipedia.org/wiki/Category:イギリスの鉄道 "wikilink") [Category:イギリスの鉄道車両](https://ja.wikipedia.org/wiki/Category:イギリスの鉄道車両 "wikilink")