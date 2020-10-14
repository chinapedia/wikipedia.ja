> この記事は[TIMS](https://ja.wikipedia.org/wiki/TIMS)から翻訳されています。


[thumb先頭車床下のTIMS箱](https://ja.wikipedia.org/wiki/ファイル:JR_east_E259_TIMS_box.jpg "wikilink")。IMSと表記された区画にTIMS端末装置が格納されている。\]\]

**TIMS**（**T**rain **I**nformation **M**anagement **S**ystemの略、**ティムス**と読む）とは、**列車情報管理システム**のことで、[東日本旅客鉄道](../Page/東日本旅客鉄道.md "wikilink")（JR東日本）と[三菱電機](../Page/三菱電機.md "wikilink")が共同で開発している[制御伝送装置の一つ](../Page/鉄道車両のモニタ装置.md "wikilink")。車両の[力行](https://ja.wikipedia.org/wiki/力行 "wikilink")や[ブレーキ](https://ja.wikipedia.org/wiki/鉄道のブレーキ "wikilink")、[出区点検](../Page/日本の鉄道車両検査.md "wikilink")、車内[空調管理](../Page/エア・コンディショナー.md "wikilink")、[行先表示機](../Page/方向幕.md "wikilink")、[車内案内表示装置](../Page/車内案内表示装置.md "wikilink")などの各種車載機器を一括して管理する[コンピュータシステム](../Page/コンピュータシステム.md "wikilink")である。

JR東日本以外でも、同社の車両をベースに設計・製造された国内外の鉄道事業者の車両が同一のシステムを搭載しており、名称も同じ「TIMS」である。

[名古屋鉄道](https://ja.wikipedia.org/wiki/名古屋鉄道 "wikilink")や[西日本旅客鉄道](../Page/西日本旅客鉄道.md "wikilink")（JR西日本）でもTIMSとほぼ同様のシステムを搭載した車両を導入しているが、名称は**TICS**（**T**rain **I**nformation **C**ontrol **S**ystemの略、**ティクス**と読む）、[小田急電鉄](../Page/小田急電鉄.md "wikilink")は*'TIOS **（**T*'rain **I**nformation **O**dakyu management **S**ystemの略、**ティオス**と読む）、[京王電鉄](../Page/京王電鉄.md "wikilink")は**K-TIMS**（**K**eio-**T**rain **I**nformation **M**anagement **S**ystemの略、**ケイ・ティムス**と読む）、[西武鉄道](../Page/西武鉄道.md "wikilink")はS-TIM（**S**eibu-**T**rain **I**ntegrated **M**anagement systemの略、エス・ティムと読む）と異なるものの、システムとしては細部を除きほぼ同じものである。

TIMSの次世代システムとしては、列車内伝送系の国際規格ECN(IEC61375-3-4)に準拠して、伝送路に[100メガビット・イーサネット](../Page/100メガビット・イーサネット.md "wikilink")を使用した[INTEROS](https://ja.wikipedia.org/wiki/INTEROS "wikilink")がある\[1\]。

同様の制御伝送システムは国内では[日立製作所](../Page/日立製作所.md "wikilink")、[東芝](../Page/東芝.md "wikilink")、[東洋電機製造](../Page/東洋電機製造.md "wikilink")などが開発している。

## 概要

### TIMSの前身となるMONについて

国鉄は[新幹線962形電車](../Page/新幹線962形電車.md "wikilink")(のちの[新幹線200系電車](../Page/新幹線200系電車.md "wikilink"))で車両機器のモニタが行えるMON1形モニタ装置を導入した\[2\]。在来線では、[205系電車の一部でドア開閉状態や故障状態などが確認できる簡易なモニタ装置を設置し](../Page/国鉄205系電車.md "wikilink")、JR東日本になってからは[651系電車や](../Page/JR東日本651系電車.md "wikilink")[251系電車などにディスプレイから様々な情報を確認できる本格的なモニタ装置であるMON](../Page/JR東日本251系電車.md "wikilink")3型モニタ装置を導入した\[3\]。この時点では力行・ブレーキなど制御指令は従来通り引き通し線へのDC100V加圧・非加圧で制御していた。

[209系電車や](../Page/JR東日本209系電車.md "wikilink")[E217系電車などに導入されたMON](../Page/JR東日本E217系電車.md "wikilink")8型制御伝送装置からは、動作状況の監視だけでなく力行・ブレーキ指令など制御指令も[シリアル伝送するようになった](../Page/シリアル通信.md "wikilink")\[4\]。また、同システムをループ型にして信頼性の向上・伝送速度向上を図ったものをMON11型として[E653系電車などに導入した](../Page/JR東日本E653系電車.md "wikilink")。JR東日本の[新幹線](../Page/新幹線.md "wikilink")車両にも一部仕様変更のうえ導入された。

### MONからTIMSへ

[1998年](https://ja.wikipedia.org/wiki/1998年 "wikilink")、[209系電車950番台](https://ja.wikipedia.org/wiki/JR東日本209系電車#950番台 "wikilink")（現・E231系900番台）に引き通し線のオール伝送化を図ったTIMSが初めて導入され、翌年から量産化された[E231系電車から標準搭載された](https://ja.wikipedia.org/wiki/JR東日本E231系電車 "wikilink")\[5\]。

力行・ブレーキ指令はもちろん、[車内放送](../Page/車内放送.md "wikilink")・空調・ドア開閉など、運転・サービスに係るほとんどの指令がTIMSを介して行われる。これにより、機器毎に独立して車両間を配線していた引き通し線は4本のTIMS伝送線に置き換わり\[6\]、配線の大幅削減による軽量化および製造・メンテナンスコスト削減に大きく寄与した。各機器の動作状況を運転台のモニターで集中監視できるようになり、各車両ごとのブレーキ圧・モーター電流・室温・湿度・空調動作、各ドアの動作状況などが確認できる。ただし[非常ブレーキ](../Page/非常ブレーキ.md "wikilink")・[直通予備ブレーキなどの重要な指令についてはTIMSを介さず直接引き通し線で指令している](https://ja.wikipedia.org/wiki/保安ブレーキ "wikilink")。

車両の駆動方法も改良が加えられた。これまでの車両は、力行は数両の電動車を1つの群として、ブレーキは[遅れ込め制御](../Page/遅れ込め制御.md "wikilink")を考慮し電動車と隣接する数両の付随車を1つの群としてそれぞれ制御する「ユニット方式」を採用してきた。これらに対しTIMSは、ユニット単位ではなく編成全体として必要な減速力を満たすようブレーキを編成内で最適化調整する考え方を導入した。制御単位が従来の車両毎から台車毎に細分化されたり、他の車両よりも混雑している車両は他の車両よりもブレーキ力を強めるなどの高度な制御が実現したため、ブレーキ[制輪子](https://ja.wikipedia.org/wiki/制輪子 "wikilink")の偏摩耗抑制や、[回生ブレーキ](../Page/回生ブレーキ.md "wikilink")の効率向上などの省エネにも寄与している。

トポロジは従来のループ型を発展させたラダー型となり、信頼性が向上した。車両間の伝送には[アークネット](https://ja.wikipedia.org/wiki/アークネット "wikilink")を、車両内の伝送には[RS-485を採用した](../Page/EIA-485.md "wikilink")\[7\]。車両間伝送の速度はMON8型の38.4[k](../Page/キロ.md "wikilink")[bpsに対しTIMSは](../Page/ビット毎秒.md "wikilink")2.5[M](../Page/メガ.md "wikilink")bpsと飛躍的に向上し、[E233系では伝送速度が](../Page/JR東日本E233系電車.md "wikilink")10Mbpsまで向上している。[在来線](../Page/在来線.md "wikilink")車両に限らず、[E5系電車](https://ja.wikipedia.org/wiki/新幹線E5系電車 "wikilink")、[E6系電車などの](https://ja.wikipedia.org/wiki/新幹線E6系電車 "wikilink")[新幹線](../Page/新幹線.md "wikilink")車両にも、TIMSを基にしたS-TIMSが搭載されている。

なお、TIMS装置は車両の床下や運転室内のラックに設置されており、乗務員室にある「TIMS」と記されたモニタはあくまで表示器である。

## TIMS経由になった指令

### 運転台関連

  - 運転台の起動（前部・中間・後部の選択）
  - 前後進、運転指令論理作成、制御電源入り指令、高加速・定速制御・リセット・故障車開放、耐雪ブレーキ、[EB装置](../Page/緊急列車停止装置.md "wikilink")
  - 速度計・高圧／低圧電圧計・元溜め／ブレーキシリンダ圧力計（TIMSからの情報を元にメータ表示）
  - 運転台各種表示灯（運用・保安）
  - キロ程演算・運転操作ナビゲーション機能
  - 各種機器の動作記録（非接触型ICカードで読み出し）
  - システムの異なる車種への読替装置の起動（他形式車と連結できる車種に搭載）
      - 使用すると一部の機能に制限がある。（例: 連結相手の状態が非表示や操作不可・旧型車に合わせて走行特性が変わる等）
          - 例：E5系（[やまびこ](../Page/やまびこ_\(列車\).md "wikilink")）がE3系（[つばさ](../Page/つばさ_\(列車\).md "wikilink")）と連結すると、E5系の走行性能がE2系と同等になる（最高速度が275km/h・起動加速度1.6Km/h/sになる）

※一部のE231系とE531系、及びE233系は速度計・高圧／低圧電圧計・元溜め／ブレーキシリンダ圧力計の表示が[液晶ディスプレイ](https://ja.wikipedia.org/wiki/液晶ディスプレイ "wikilink")式（[グラスコックピット](../Page/グラスコックピット.md "wikilink")）になっている。

### 主回路関連

  - パンタグラフ昇降指令（一部車種のみ。それ以外では引き通し線）
  - 高速度遮断器 (HB) 入り許可制御
  - 車上試験安全インターロック
  - 力行・ブレーキ制御、回生バランス制御

### 補助回路機器

  - [SIVリセット指令](../Page/静止形インバータ.md "wikilink")・電源誘導指令
  - 空気[圧縮機](../Page/圧縮機.md "wikilink")の運転制御
  - バッテリ切り指令

### ブレーキ関連

  - 編成全体としての電空ブレンディング制御、[ATS](../Page/自動列車停止装置.md "wikilink")・[ATCのブレーキ不足検知](../Page/自動列車制御装置.md "wikilink")
  - [駐車ブレーキ制御](https://ja.wikipedia.org/wiki/留置ブレーキ "wikilink")

### サービス機器関連

  - ドア開閉指令
      - バックアップ回路切替・半自動・一部車両を締め切ってのドア開閉。各ドアの動作状況も表示できる。[ホームドア](../Page/ホームドア.md "wikilink")制御器との通信も可能。
  - 冷暖房送風一括制御、空調基準温度設定（外気温、各車両の室温・湿度表示が可能）
  - 室内灯制御
  - 車内放送／乗務員連絡／[車内非常通報装置](https://ja.wikipedia.org/wiki/車内非常通報装置 "wikilink")音声データのデジタル伝送、自動放送制御
  - 行先・車内案内・運行番号設定（TIMSの設定画面による）
  - 車内案内表示装置への運行状況表示（[VIS経由による](../Page/VIS_\(鉄道システム\).md "wikilink")）
  - [グリーン車](../Page/グリーン車.md "wikilink")[Suica](../Page/Suica.md "wikilink")システムの座席管理装置の制御
  - [便所内非常スイッチ操作の表示](../Page/列車便所.md "wikilink")
  - 各車の乗車率演算・表示
  - 座席収納指令（6扉車）

### 検修関連

  - 自動出区点検機能
  - 車上試験機能
  - 試運転操作記録、試運転情報表示機能
  - 故障記録機能

## 搭載車種の例

### TIMS

  - [JR東日本E231系電車](https://ja.wikipedia.org/wiki/JR東日本E231系電車 "wikilink")\[8\]
  - [JR東日本E233系電車](../Page/JR東日本E233系電車.md "wikilink")\[9\]（3000番台のみE231系への読替装置あり）
  - [JR東日本E257系電車](../Page/JR東日本E257系電車.md "wikilink")\[10\]
  - [JR東日本E259系電車](../Page/JR東日本E259系電車.md "wikilink")\[11\]
  - [JR東日本E353系電車](https://ja.wikipedia.org/wiki/JR東日本E353系電車 "wikilink")
  - [JR東日本E531系電車](../Page/JR東日本E531系電車.md "wikilink")\[12\]
  - [JR東日本E655系電車](../Page/JR東日本E655系電車.md "wikilink")\[13\]
  - [JR東日本E657系電車](https://ja.wikipedia.org/wiki/JR東日本E657系電車 "wikilink")
  - [TRAIN SUITE 四季島](https://ja.wikipedia.org/wiki/TRAIN_SUITE_四季島 "wikilink")
  - [相鉄10000系電車](../Page/相鉄10000系電車.md "wikilink")
  - [相鉄11000系電車](https://ja.wikipedia.org/wiki/相鉄11000系電車 "wikilink")
  - [相鉄12000系電車](https://ja.wikipedia.org/wiki/相鉄12000系電車 "wikilink")\[14\]
  - [東京都交通局10-300形電車](https://ja.wikipedia.org/wiki/東京都交通局10-300形電車 "wikilink")
  - [シンガポール地下鉄C751B形電車](../Page/シンガポール地下鉄C751B形電車.md "wikilink")\[15\]
  - [愛知高速交通100形電車](../Page/愛知高速交通100形電車.md "wikilink")\[16\]

### S-TIMS

  - [新幹線E5系/H5系電車](https://ja.wikipedia.org/wiki/新幹線E5系電車 "wikilink")\[17\]（[E3系への読替装置あり](https://ja.wikipedia.org/wiki/新幹線E3系電車 "wikilink")）
  - [新幹線E6系電車](https://ja.wikipedia.org/wiki/新幹線E6系電車 "wikilink")（E2系への読替装置あり）
  - [新幹線E7系/W7系電車](https://ja.wikipedia.org/wiki/新幹線E7系電車 "wikilink")

### TICS

  - [JR西日本125系電車](../Page/JR西日本125系電車.md "wikilink")
  - [JR西日本521系電車](https://ja.wikipedia.org/wiki/JR西日本521系電車 "wikilink")
  - [名鉄300系電車](../Page/名鉄300系電車.md "wikilink")・[名古屋市交通局7000形電車](../Page/名古屋市交通局7000形電車.md "wikilink")（共通設計）
  - [名鉄3300・3150系電車](../Page/名鉄3300系電車_\(3代\).md "wikilink")（読替装置使用で[3500系・3700系・3100系電車と併結可](../Page/名鉄3500系電車_\(2代\).md "wikilink")）
  - [名鉄2000系電車](../Page/名鉄2000系電車.md "wikilink")（他形式車と連結すると車体傾斜機能は停止。回送のみ）
  - [名鉄2200系](../Page/名鉄2200系電車.md "wikilink")・[2300系電車](https://ja.wikipedia.org/wiki/名鉄2200系電車#2300系 "wikilink")（2300系は読替装置使用で[1700系電車と組成](https://ja.wikipedia.org/wiki/名鉄2200系電車#1700系 "wikilink")・読替装置使用で3100系・3150系と併結可）
  - [名鉄4000系電車](https://ja.wikipedia.org/wiki/名鉄4000系電車 "wikilink")
  - [名古屋市交通局6050形電車](https://ja.wikipedia.org/wiki/名古屋市交通局6050形電車 "wikilink")（ATO対応）
  - [名古屋市交通局N3000形電車](https://ja.wikipedia.org/wiki/名古屋市交通局N3000形電車 "wikilink")

### TIOS

  - [小田急新3000形電車](../Page/小田急3000形電車_\(2代\).md "wikilink") 3次車以降\[18\]（6両編成は読替装置使用で[電磁直通ブレーキ](../Page/電磁直通ブレーキ.md "wikilink")の通勤車と併結可）
  - [小田急新4000形電車](../Page/小田急4000形電車_\(2代\).md "wikilink")
  - [小田急50000形電車](../Page/小田急50000形電車.md "wikilink")\[19\]
  - [小田急60000形電車](../Page/小田急60000形電車.md "wikilink")\[20\]
  - [小田急70000形電車](https://ja.wikipedia.org/wiki/小田急70000形電車 "wikilink")\[21\]

### K-TIMS

  - [京王5000系電車](https://ja.wikipedia.org/wiki/京王5000系電車_\(2代\) "wikilink")\[22\]

### S-TIM

  - [西武30000系電車](../Page/西武30000系電車.md "wikilink")\[23\]
  - [西武40000系電車](https://ja.wikipedia.org/wiki/西武40000系電車 "wikilink")
  - [西武001系電車](https://ja.wikipedia.org/wiki/西武001系電車 "wikilink")\[24\]

### TSIS(Train Supervision Information System)

  - [台北捷運381型電車](https://ja.wikipedia.org/wiki/台北捷運381型電車 "wikilink")

### TMS(Train Management System)

  - [九広鉄路SP1900形電車](../Page/九広鉄路SP1900形電車.md "wikilink")
  - [北京地下鉄DKZ16型電車](https://ja.wikipedia.org/wiki/北京地下鉄DKZ16型電車 "wikilink")\[25\]

## 脚注

<references />

## 関連項目

  - [鉄道車両のモニタ装置](../Page/鉄道車両のモニタ装置.md "wikilink")
  - [DICS](../Page/DICS.md "wikilink")
  - [INTEROS](https://ja.wikipedia.org/wiki/INTEROS "wikilink")
  - [グラスコクピット](https://ja.wikipedia.org/wiki/グラスコクピット "wikilink")

## 外部リンク

  - [三菱交通システムトップページ](http://www.mitsubishielectric.co.jp/society/traffic/index.html) - TIMSの開発を担当。

[Category:東日本旅客鉄道](https://ja.wikipedia.org/wiki/Category:東日本旅客鉄道 "wikilink") [Category:鉄道の設備](https://ja.wikipedia.org/wiki/Category:鉄道の設備 "wikilink") [Category:鉄道とIT](https://ja.wikipedia.org/wiki/Category:鉄道とIT "wikilink") [Category:鉄道車両工学](https://ja.wikipedia.org/wiki/Category:鉄道車両工学 "wikilink")

1.  JR East technical review. 2013 (Spr.) (43) 菅谷　誠ほか「次世代車両制御システム（INTEROS）の開発（第二報）」
2.  日立評論 1979-07 p477-480 荒井 真一、豊田 瑛一、木脇 久勝「962形新幹線試作電車の制御機器」
3.
4.
5.
6.  電気学会産業応用部門大会講演論文集 1998 新井静男ほか「列車情報管理装置(TIMS)の開発 209-950代への適用」
7.  サイバネティクスVol.12-No.1.2007 p.25-32 新井静男、白樫智也「列車情報管理装置(TIMS)の10年と今後の取り組み」
8.
9.
10.
11. 鉄道技術連合シンポジウム(J-Rail)講演論文集 2009(16) p101-104 長谷部 和則 , 宮内 隆史 , 菅谷 誠 , 角野 敏子「列車情報管理装置(TIMS)の開発 : JR東日本E259系TIMSにおける特急形車両としての機能設計」
12.
13. 鉄道サイバネ・シンポジウム論文集44 長谷部 和則ほか「列車情報管理装置(TIMS)の開発」
14. 鉄道車両と技術 25(1) 大谷 学途ほか 「相模鉄道 12000系の概要」
15. 鉄道サイバネ・シンポジウム論文集37 角南健次ほか「Singapore LTA C751B向けTIMS」
16. IEEJ Journal, Vol.124, No.8, 2004 工藤 健一 「実用線として開業を迎える磁気浮上式鉄道「リニモ」(HSST)の概要」
17. JR East Technical review (51) p.21-26 水口芳樹、薗田秀樹「新幹線における運転エネルギーの測定と分析」
18. 鉄道サイバネ・シンポジウム論文集41 加藤肇ほか 「小田急3000形3次車向けTIOS 量産車両のTIOS化と導入効果」
19. 鉄道サイバネ・シンポジウム論文集42 片柳英雄, 畑彰賢, 加藤肇, 西岡和徳, 雨宮富史夫, 増崎修, 木島裕之, 伏見英里, 野田敦司「小田急電鉄 50000形 TIOS装置の開発と導入効果」
20. R\&m Vol.16 No.4 p.11-16 加藤巧也, 木島裕之, 細野光司, 野中俊昭 「小田急電鉄新型ロマンスカーMSE60000形の開発とその概要(その2)」
21. 鉄道車両と技術 Vol.24 No.2 p.22-28 伊藤正博 「最近の列車制御システム 小田急電鉄 70000形 GSEの概要(2)」
22. 鉄道サイバネ・シンポジウム論文集 55 池嶋 知明 , 岡田 洋治 , 若松 茂則 , 岡原 裕喜 , 大川 晶 「5000系新造車向け 車両情報管理装置(K-TIMS)の紹介」
23. 鉄道サイバネ・シンポジウム論文集 45 小川克弘, 鳥居尚史, 三島和彦, 酒衛秀輔, 圖子洋隆, 白井進 「西武鉄道30000系向け列車情報管理装置(S‐TIM)の開発」
24. 鉄道サイバネ・シンポジウム論文集 56 「西武鉄道 新型特急車両向けトレインビジョンの紹介」
25. 鉄道サイバネ・シンポジウム論文集 44 竹山 雅之ほか 「北京地下鉄2号線向けTMSの開発」