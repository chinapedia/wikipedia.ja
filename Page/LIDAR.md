> この記事は[LIDAR](https://ja.wikipedia.org/wiki/LIDAR)から翻訳されています。


**LIDAR**（[英語](../Page/英語.md "wikilink")：Light Detection and Ranging、Laser Imaging Detection and Ranging、「光検出と測距」ないし「[レーザー](../Page/レーザー.md "wikilink")画像検出と測距」）は、光を用いた[リモートセンシング](../Page/リモートセンシング.md "wikilink")技術の一つで、[パルス](../Page/パルス.md "wikilink")状に発光するレーザー照射に対する[散乱](https://ja.wikipedia.org/wiki/散乱 "wikilink")光を測定し、遠距離にある対象までの距離やその対象の性質を分析するものである。日本語では**ライダー**、**ライダ**とカタカナ書きされることも多い。軍事領域ではしばしば[アクロニム](https://ja.wikipedia.org/wiki/アクロニム "wikilink") **LADAR** (Laser Detection and Ranging) が用いられる。

この技法は[レーダー](../Page/レーダー.md "wikilink")に類似しており、レーダーの電波を光に置き換えたものである。対象までの距離は、発光後反射光を受光するまでの時間の差で求まる。そのため、レーザーレーダー (Laser radar) の語が用いられることもある。

ライダーは[地質学](../Page/地質学.md "wikilink")、[地質工学](https://ja.wikipedia.org/wiki/地質工学 "wikilink")、[地震学](../Page/地震学.md "wikilink")、[リモートセンシング](../Page/リモートセンシング.md "wikilink")、 [大気物理学](../Page/大気物理学.md "wikilink")で用いられる。近年は[自動運転車用センサーとしても注目されている](../Page/オートパイロット.md "wikilink")。\[1\]

## 概説

ライダーとレーダーの最も基本的な相違は、ライダーはレーダーよりも遥かに短い波長の電磁波を用いることである。典型的には[紫外線](../Page/紫外線.md "wikilink")、[可視光線](../Page/可視光線.md "wikilink")、[近赤外線](https://ja.wikipedia.org/wiki/近赤外線 "wikilink")である。一般的に、検出できる物体や物体の特徴のサイズは、[波長](../Page/波長.md "wikilink")を下回ることができない。従って、ライダーはレーダーよりも[エアロゾル](https://ja.wikipedia.org/wiki/エアロゾル "wikilink")や[雲](../Page/雲.md "wikilink")の粒子の検出に向いており、大気の研究や[気象学](../Page/気象学.md "wikilink")にとって有用である。

ある物体が検出されるには、伝導性に不連続性があり進行してきた波を反射する必要がある。レーダー波（マイクロ波またはラジオ帯域）は[金属](../Page/金属.md "wikilink")物によって効率よく反射されるが、雨滴や岩といった非金属は反射を起こしにくく、物質によってはまったく反射が検出できず、レーダーでは見つからない場合がある。エアロゾルや分子のような極めて小さな対象は特に不得手である。[Starfire_Optical_Range_-_sodium_laser.jpg](https://ja.wikipedia.org/wiki/File:Starfire_Optical_Range_-_sodium_laser.jpg "fig:Starfire_Optical_Range_-_sodium_laser.jpg")([en](https://ja.wikipedia.org/wiki/:en:Starfire_Optical_Range "wikilink"))において調整中の[色素レーザー](https://ja.wikipedia.org/wiki/色素レーザー "wikilink")([en](https://ja.wikipedia.org/wiki/:en:Dye_laser "wikilink"))。**LIDAR** と [レーザーガイド星](../Page/レーザーガイド星.md "wikilink")([en](https://ja.wikipedia.org/wiki/:en:laser_guide_star "wikilink")) の実験のために用いられる。レーザーの波長は、大気上層の[ナトリウム](https://ja.wikipedia.org/wiki/ナトリウム "wikilink")原子を励起させるのに最適な、ナトリウムの[フラウンホーファー線](../Page/フラウンホーファー線.md "wikilink")の波長に設定されている。\]\] [LIDAR-scanned-SICK-LMS-animation.gif](https://ja.wikipedia.org/wiki/File:LIDAR-scanned-SICK-LMS-animation.gif "fig:LIDAR-scanned-SICK-LMS-animation.gif")

ライダーを用いるとこれらの問題は解決する。ライダーの光束は密度が高く、[コヒーレンス](../Page/コヒーレンス.md "wikilink")も高い。それだけでなく、波長が極めて短い（紫外光ではおよそ  から約  の範囲）。このような電磁波は小さな物体によっても極めてよく「反射」（後方散乱と呼ばれる）される。ライダーの使用法によっては、別の種類の散乱が利用される。[レイリー散乱](../Page/レイリー散乱.md "wikilink")、[ミー散乱](../Page/ミー散乱.md "wikilink")、[ラマン散乱](https://ja.wikipedia.org/wiki/ラマン散乱 "wikilink")、[蛍光](../Page/蛍光.md "wikilink")である。ライダーの波長は[煙](../Page/煙.md "wikilink")などの大気によって運ばれる粒子（エアロゾル）、雲、大気の分子の測定に最適である。

レーザーの光束は通常極めて絞り込まれ、細いビームとなっているので、極めて高い光学的解像度を以て大気の特徴をマップすることができる。更に、多くの化学物質において、可視光はマイクロ波に比べ強く相互作用するので、それらを検出する感度が高い。各種波長のレーザーを上手に組み合わせれば、散乱光の強度と波長との関係から、大気の組成を離れた所から調べることができる。

ライダーは大気の研究と気象学に主に用いられてきたが、近年では航空機や人工衛星に「ルックダウン」 downward-looking 型のライダーを搭載して行う調査やマッピングの方法が開発されるようになった。

## 構成

ライダーの構成は大きく二種類に分けられる。一つはマイクロパルスライダー (micropulse lidar) システム、もう一つは高エネルギー (high energy) システムである。

マイクロパルスライダーは、レーザー技術の進歩と[コンピュータ](../Page/コンピュータ.md "wikilink")の演算能力の驚異的な向上とが組み合わされて可能となったものである。比較的低出力（1[ワット](../Page/ワット.md "wikilink")のオーダー）のレーザーを用い、しばしば、「目に優しい」(eye-safe)システムと呼ばれる。目を防護し失明を回避するための予防措置をとらずに用いうるからである。

高エネルギーシステムは大気の研究では一般的である。雲の高さや層構造、雲の粒子の性質（消失係数 extinction coefficient、後方散乱係数 backscatter coefficient、偏光解消度 depolarization）、温度、圧力、風、湿度、微少な気体の濃度（[オゾン](../Page/オゾン.md "wikilink")、[メタン](../Page/メタン.md "wikilink")、[窒素酸化物](../Page/窒素酸化物.md "wikilink")など）などの大気のパラメタを測定することができる。

次に、ライダーを構成する要素を挙げる。

1.  **レーザー** — 科学研究以外の分野では波長 600-800 [nm](../Page/ナノメートル.md "wikilink") のレーザーが最も一般に用いられる。安価で大出力のものが得られるが、「目に優しく」はない（失明の可能性がある）。「目に優しい」ことは軍事利用ではしばしば必要となる。波長1550 nm のレーザーは「目に優しい」が、十分な出力のものを得るのが難しく、一般的ではない。航空機搭載型ライダーは一般的に 1064 nm のものを用いる。海底探査システムの中には水中透過性の高い 532 nm のレーザーを用いる場合がある。波長の他にも、発光間隔（データ収集速度を決めることになる）と発光時間（距離方向の分解能に関係する）も適当に設定しなければならない。
2.  **スキャナと光学系** — データ収集速度は、システムのデータ走査速度にも影響される。走査は二次元的に行われるが、その方法は様々である。二枚の平面鏡を振動させるもの、多角形の鏡を用いるもの、スキャナが二軸をもつものなどである。光学系の性能は、角度方向の分解と、検出できる距離の限界に影響する。反射光の分離には、穴の開いた鏡を用いる方法と[ビームスプリッター](../Page/ビームスプリッター.md "wikilink")を用いる方法がある。
3.  **受光器と電子機器** — 受光器にはさまざまな物質が用いられる。[ケイ素](../Page/ケイ素.md "wikilink")と[インジウム](../Page/インジウム.md "wikilink")[ガリウム砒素](https://ja.wikipedia.org/wiki/ガリウム砒素 "wikilink")を用いた[ピンフォトダイオードや](../Page/フォトダイオード.md "wikilink")[アバランシェフォトダイオード](https://ja.wikipedia.org/wiki/アバランシェフォトダイオード "wikilink")が一般的であるが、波長によっては[光電子増倍管](../Page/光電子増倍管.md "wikilink")も使われる。受光器の感度は、ライダーの他の部分の設計とうまくバランスを取らなければいけない。
4.  **ポジショニングとナビゲーション** — ライダーを可動型のプラットフォーム（航空機や人工衛星）に搭載する場合は、センサの絶対的な位置と方向を決定する装置が必要である。[GPSと](../Page/グローバル・ポジショニング・システム.md "wikilink")[慣性誘導装置](https://ja.wikipedia.org/wiki/慣性誘導装置 "wikilink")が用いられる。

## 応用

[サムネイルの自動運転実証車](https://ja.wikipedia.org/wiki/ファイル:Waymo_Chrysler_Pacifica_in_Los_Altos,_2017.jpg "wikilink")。ナンバープレート上部、前輪上部、車両天井の黒いドームの中にそれぞれLIDARが搭載されている。\]\] 自動運転技術 - 条件付き自動運転であるレベル3や、ドライバーによる運転を前提としないレベル4～5の対応になると、高速道路や一般道路を安全に自律走行する機能が必要となる。そのため、センシングの冗長性を担保する理由で、カメラやミリ波レーダーに加えて、ライダーが採用される。これはライダーは色の識別や悪天候時のセンシングを苦手とする代わりに、距離の計測においては他のセンサーの認識精度を凌駕するためである。このような事情から、矢野経済研究所の発表によると2030年にはライダーの市場規模は4,959億円になると見込まれている。

地質学や地震学では、航空機搭載型ライダーとGPSを組み合わせ、[断層](https://ja.wikipedia.org/wiki/断層 "wikilink")や[隆起・沈降に伴う](../Page/隆起と沈降.md "wikilink")[地殻](../Page/地殻.md "wikilink")の変位を測定するのに極めて役立っている。このシステムを用いれば、地殻変動を樹木越しに測ることすらできる。[ワシントンの](../Page/ワシントン州.md "wikilink")を発見したシステムとして有名になった。2004年の噴火によって発生した[セント・ヘレンズ山](../Page/セント・ヘレンズ山.md "wikilink")の隆起の程度も、噴火前後のデータを比較することで示すことができた。

航空機/衛星搭載型ライダーシステムは[氷河](../Page/氷河.md "wikilink")の観測にも役立っている。わずかな消長を測定することができる。[アメリカ航空宇宙局](../Page/アメリカ航空宇宙局.md "wikilink")(NASA)の[ICESat](https://ja.wikipedia.org/wiki/ICESat "wikilink")([en](https://ja.wikipedia.org/wiki/:en:ICESat "wikilink"))には、この目的でライダーが搭載されている。

[林業](../Page/林業.md "wikilink")においてもライダーはさまざまに応用される。航空機/衛星搭載型ライダーによって、[林冠](../Page/林冠.md "wikilink")の高さ、[バイオマス](../Page/バイオマス.md "wikilink")の測定、leaf area の測定が行える。他の産業、例えばエネルギー産業、鉄道、運輸関連分野でも、手早いサーベイ法として用いられる。

宇宙船によって月面に設置された鏡を用いて（[月レーザー測距実験](https://ja.wikipedia.org/wiki/月レーザー測距実験 "wikilink")参照）、月と地球の距離を観測する世界規模のネットワークがあり、ここでもライダーが用いられる。月との距離がミリメートル単位の精度で測定できるので、[一般相対性理論](https://ja.wikipedia.org/wiki/一般相対性理論 "wikilink")の検証に有用である。

宇宙機に搭載されたLIDARとしては、1994年の[STS-64](https://ja.wikipedia.org/wiki/STS-64 "wikilink")にLITEが搭載され、雲やエアロゾルを観測した。火星を回るNASAの探査機[マーズ・グローバル・サーベイヤー](../Page/マーズ・グローバル・サーベイヤー.md "wikilink")(1996年打上げ)は、MOLA (the Mars Orbiting Laser Altimeter) と名付けられたライダーを搭載しており、目をみはる程正確な地形図をもたらしている。また、2003年に打ち上げられたNASAの[ICESat](https://ja.wikipedia.org/wiki/ICESat "wikilink")衛星にもGLASというLIDARが搭載され、氷床や大気の観測を行った。2006年に打ち上げられたNASAの[CALIPSO](https://ja.wikipedia.org/wiki/CALIPSO "wikilink")衛星はCALIOPを搭載し、大気の観測を行っている。2014年にESAが打ち上げる予定の[ADM-Aeolus](https://ja.wikipedia.org/wiki/ADM-Aeolus "wikilink")も風や大気を観測するLIDARが搭載されている。日本初の月周回衛星[かぐや](../Page/かぐや.md "wikilink")も、一種のライダーであるレーザー高度計LALT (Laser ALTimeterthe）を搭載しており、月全面の正確な地形高度データを取得した。 [サムネイル](https://ja.wikipedia.org/wiki/ファイル:Ouster_OS1-64_lidar_point_cloud_of_intersection_of_Folsom_and_Dore_St,_San_Francisco.png "wikilink")。18秒以上の撮影時間中におよそ2300万点の点が生成された。\]\] 大気物理学では、中層および上層部の大気に含まれるいくつかの物質の濃度を遠距離から測るのに用いられる。カリウム、ナトリウム、分子状の窒素及び酸素といった物質である。これらの濃度を測定することで、温度を計算することもできる。ライダーは風速の測定や、[エアロゾル](https://ja.wikipedia.org/wiki/エアロゾル "wikilink")粒子の鉛直方向での分布を調べるためにも用いられる。

[海洋学](../Page/海洋学.md "wikilink")では、[植物プランクトン](../Page/植物プランクトン.md "wikilink")の[蛍光](../Page/蛍光.md "wikilink")及び海洋表層の総合的な[バイオマス](../Page/バイオマス.md "wikilink")の推定に用いられる。船舶による測定が困難な海域での海底探査にも航空機に搭載して用いられる。

また、上記以外にも速度超過に対する交通取締（いわゆるネズミ捕り）用としてレーダーの代わりに用いられることがある。レーダー取締り機は携帯するには大型であり、特定の車両を分離して測定することがしばしば困難であるが、ライダーを用いると小型のカメラ式取締機によって、沢山走っている車両の内一台を狙い撃ちにすることができる。レーダー取締機は[ドップラー効果](../Page/ドップラー効果.md "wikilink")を用いて対象の速さを直接測定するが、ライダーの場合、二点間を通過する時間から速さを計算する。

軍事応用を詳述するには時期尚早であるが、イメージングに関するかなりの研究が進んでいることが知られている。空間分解能が高いため、対象（[戦車](https://ja.wikipedia.org/wiki/戦車 "wikilink")など）の細かな特徴を捉えることができる。軍事分野では **LADAR** のアクロニムで呼ばれることが多い。

立体イメージングが可能である。[スウェーデン](https://ja.wikipedia.org/wiki/スウェーデン "wikilink")、[デンマーク](https://ja.wikipedia.org/wiki/デンマーク "wikilink")、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")、[イギリス](https://ja.wikipedia.org/wiki/イギリス "wikilink")で軍事応用が研究されており、数キロメートル先の対象の立体像を  以下の誤差で描出することができる。

イギリスにある[欧州トーラス共同研究施設](https://ja.wikipedia.org/wiki/欧州トーラス共同研究施設 "wikilink") (JET) では、ライダーを用いた[トムソン散乱](https://ja.wikipedia.org/wiki/トムソン散乱 "wikilink")の測定を行い、[プラズマ](https://ja.wikipedia.org/wiki/プラズマ "wikilink")中の電子密度、温度プロフィールを求めている\[2\]。

## 関連項目

  - [:en:Atomic line filter](https://ja.wikipedia.org/wiki/:en:Atomic_line_filter "wikilink")
  - [:en:Time domain reflectometry](https://ja.wikipedia.org/wiki/:en:Time_domain_reflectometry "wikilink")
  - [:en:Optical time domain reflectometer](https://ja.wikipedia.org/wiki/:en:Optical_time_domain_reflectometer "wikilink")
  - [:en:Satellite laser ranging](https://ja.wikipedia.org/wiki/:en:Satellite_laser_ranging "wikilink")
  - [測域センサ](https://ja.wikipedia.org/wiki/測域センサ "wikilink")
  - [ソナー](../Page/ソナー.md "wikilink")
  - [補償光学](../Page/補償光学.md "wikilink")
  - [光ヘテロダイン](https://ja.wikipedia.org/wiki/光ヘテロダイン "wikilink")
  - [拡散符号](https://ja.wikipedia.org/wiki/拡散符号 "wikilink")
  - [ドップラーシフト](https://ja.wikipedia.org/wiki/ドップラーシフト "wikilink")
  - [航空レーザー測量](../Page/航空レーザー測量.md "wikilink")
  - [ドップラー・ライダー](https://ja.wikipedia.org/wiki/ドップラー・ライダー "wikilink")
  - [SLAM](https://ja.wikipedia.org/wiki/SLAM "wikilink")

## 脚注

## 参考文献

  -
  -
  -
  -
## 外部リンク

 

  - [CALIPSO](https://www-calipso.larc.nasa.gov): The Cloud-Aerosol Lidar and Infrared Pathfinder Satellite Observation satellite -- space-based laser remote sensing of clouds and aerosols for a better understanding of climate change issues
  - [Lidar: Raman-shifted Eye-safe Aerosol Lidar](http://lidar.csuchico.edu)
  - [lidar tutorial](https://web.archive.org/web/20070304235442/http://www.ghcc.msfc.nasa.gov/sparcle/sparcle_tutorial.html) ([NASA](../Page/アメリカ航空宇宙局.md "wikilink")) - [ウェイバックマシン](https://ja.wikipedia.org/wiki/ウェイバックマシン "wikilink")（2007年3月4日アーカイブ分）
  - [NOAA Oceanographic (Fish) Lidar](http://www.etl.noaa.gov/technology/instruments/floe/)
  - [Joint Airborne Lidar Bathymetry Technical Center of Expertise (JALBTCX)](http://shoals.sam.usace.army.mil/)
  - [EOSL](http://eosl.gtri.gatech.edu/index.jsp) - The Electro-Optical Systems Laboratory at [GTRI](https://ja.wikipedia.org/wiki/GTRI "wikilink") has a nationally known program in lidar research and development.
  - [The NASA Goddard Space Flight Center's Raman Lidar Laboratory](http://ramanlidar.gsfc.nasa.gov) - This laboratory has a ground and an upcoming airborne Raman lidar measuring water vapor, aerosols and other atmospheric species
  - [The USGS Center for LIDAR Information Coordination and Knowledge (CLICK)](http://lidar.cr.usgs.gov/index.html) - A website intended to "facilitate data access, user coordination and education of lidar remote sensing for scientific needs."
  - [1](http://www.ikg.uni-hannover.de/publikationen/publikationen/2006/brenner_tutorial_part1.pdf) Tutorial slides on LIDAR (aerial laser scanning): Principles, errors, strip adjustment, filtering.
  - [2](http://www.ikg.uni-hannover.de/publikationen/publikationen/2006/brenner_tutorial_part2.pdf) Tutorial slides on LIDAR (aerial laser scanning): Extraction and modelling.

[Category:レーザー](https://ja.wikipedia.org/wiki/Category:レーザー "wikilink") [Category:光学](https://ja.wikipedia.org/wiki/Category:光学 "wikilink") [Category:計測機器](https://ja.wikipedia.org/wiki/Category:計測機器 "wikilink")

1.
2.