> この記事は[SETI@home](https://ja.wikipedia.org/wiki/SETI@home)から翻訳されています。


**SETI@home**（セティアットホーム）は[インターネット](../Page/インターネット.md "wikilink")接続されたコンピュータ群を使う[ボランティア・コンピューティング](https://ja.wikipedia.org/wiki/ボランティア・コンピューティング "wikilink")プロジェクトで、[アメリカ合衆国](https://ja.wikipedia.org/wiki/アメリカ合衆国 "wikilink")の[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink") [Space Sciences Laboratory](https://ja.wikipedia.org/wiki/:en:Space_Sciences_Laboratory "wikilink") が運営している。*SETI* は "Search for Extra-Terrestrial Intelligence"（[地球外知的生命体探査](../Page/地球外知的生命体探査.md "wikilink")）の略で、SETI@homeはSETIの一部である。SETI@homeは1999年5月17日に一般公開された\[1\]\[2\]\[3\]。

2020年3月31日にseti@home向け work unit の新規配布を休止することが発表されている\[4\]。ホームページや掲示板などは残されるが、新しい研究が始まらない限りseti@homeのボランティアコンピューティングは再開されないとしている。

## 科学的研究

SETI@homeの本来の目的は次の2点だった。

1.  地球外知的生命体の証拠を検出するため、観測データの分析をサポートすることで、有益な科学的作業を行う。
2.  「ボランティア・コンピューティング」という概念の実現性と実用性を証明する。

後者の目的は一般に完全に成功したと見なされている。SETI@home の開発から発展した現在の[BOINC環境では](../Page/Berkeley_Open_Infrastructure_for_Network_Computing.md "wikilink")、様々な分野の計算量の多いプロジェクトにサポートを提供している。

前者の目的は今のところ達成されていない。SETI@homeによってETI（地球外知的生命体）信号の証拠が見つかったという例はない。

SETI@home では、[アレシボ天文台](https://ja.wikipedia.org/wiki/アレシボ天文台 "wikilink")の観測データを使い、その中に[地球外知的生命体からの無線信号の証拠と見られるものがないか探索する](../Page/地球外生命.md "wikilink")。データは他の科学的プログラムに従って電波望遠鏡を使用しているときに便乗する形で採取されている。データは[デジタイズ](../Page/デジタイズ.md "wikilink")されて記録され、SETI@home の施設に郵送される。そこでデータを時間と周波数で分割して小さな塊にし、それらを世界中のコンピュータに分配し、ノイズとは見なせない情報を含む可能性のある信号を探す。SETI@homeの要点は、データを小さく切り分け、それらを数百万台のパーソナルコンピュータで分析させ、分析結果を返してもらうという点にある。そうすることで、通常なら最新のスーパーコンピュータを必要とするような分析をインターネット上のコミュニティの援助によって達成できるようにした。

ソフトウェアは、次のような4種類の信号をノイズから識別する\[5\]。

  - [パワースペクトルにおけるスパイク](../Page/スペクトル密度.md "wikilink")（突出した部分）
  - 送信電力の[ガウス関数](../Page/ガウス関数.md "wikilink")的変動。
  - 電力スパイクが3回連続したもの。
  - [パルス信号](https://ja.wikipedia.org/wiki/パルス波 "wikilink")。[ナローバンド](../Page/ナローバンド.md "wikilink")のデジタル伝送の可能性がある。

ETI信号は星間物質によっても影響されうるし、地球との相対運動にも影響されうるため、様々なバリエーションが考えられる。そのため「信号」の可能性があるデータは様々な方法で処理され、ノイズでないかどうか確認する。例えば、惑星は恒星の周囲を公転していることが多く、地球からみて相対的に加速度運動していることが多い。そのため「信号」があったとしても周波数が時と共に変化する。そのようなことも考慮した分析がSETI@homeのソフトウェアで実施される。

これは、信号強度計を見ながら[ラジオ](../Page/ラジオ.md "wikilink")を放送局の周波数に合わせるのに似ている。技術的には[離散フーリエ変換](../Page/離散フーリエ変換.md "wikilink")を中心とした[デジタル信号処理](../Page/デジタル信号処理.md "wikilink")を多用している。

### 結果

このプロジェクトでETI信号を実際に検出したことはないが、いくつかの候補とされる信号（信号強度の突出について説明がつかないもの）は識別しており\[6\]、さらなる分析が行われている。これまでで最も重大とされた候補信号は2004年9月1日のもので、[電波源](https://ja.wikipedia.org/wiki/電波源 "wikilink")[SHGb02+14a](https://ja.wikipedia.org/wiki/SHGb02+14a "wikilink") と名付けられた。

天文学者 [Seth Shostak](https://ja.wikipedia.org/wiki/:en:Seth_Shostak "wikilink") は2004年、[ドレイクの方程式](../Page/ドレイクの方程式.md "wikilink")に基づくと、2020年から2025年までの間に決定的な証拠となる信号が見つかり、異星人の存在が証明されると述べた\[7\]。これは、SETI@home がその時期まで継続されることを前提とした発言で、これまでのSETI@homeの実績から推定したものである。

プロジェクトは地球外知的生命体の証拠を見つけるという目標を達成していないが、科学界にインターネット上の分散コンピューティング・プロジェクトが分析ツールとして有効であることを示し、最新の[スーパーコンピュータ](../Page/スーパーコンピュータ.md "wikilink")にも匹敵しうることを示した\[8\]。しかし、もともとの想定よりも参加したコンピュータの台数は桁違いに大きく（本来は5万台から10万台とされていた\[9\]）、それがプロジェクトの科学的成果に寄与している点はあまり検証されていない。

## テクノロジー

[thumb](https://ja.wikipedia.org/wiki/ファイル:Setiathomeversion4point45.png "wikilink") インターネットに接続可能なコンピュータを持っていれば、誰でも[電波望遠鏡](../Page/電波望遠鏡.md "wikilink")の観測データをダウンロードして分析する無料のプログラムを実行させることでSETI@homeに参加できる。

観測[データ](../Page/データ.md "wikilink")は、[プエルトリコ](../Page/プエルトリコ.md "wikilink")にある[アレシボ天文台](https://ja.wikipedia.org/wiki/アレシボ天文台 "wikilink")で36[ギガバイト](../Page/ギガバイト.md "wikilink")の[磁気テープ](../Page/磁気テープ.md "wikilink")に記録される。テープ1本が15.5時間ぶんのデータを格納しており、それが[カリフォルニア大学バークレー校](../Page/カリフォルニア大学バークレー校.md "wikilink")に郵送される\[10\]。アレシボには高[帯域幅](../Page/帯域幅.md "wikilink")のインターネット接続がないため、バークレーにまず[郵送](https://ja.wikipedia.org/wiki/郵送 "wikilink")している\[11\]。バークレーでは、それを107秒ごとの[時間領域](https://ja.wikipedia.org/wiki/時間領域 "wikilink")で分割し、さらに[周波数領域](../Page/周波数領域.md "wikilink")で分割した "work unit" にする\[12\]。個々の work unit は約0.35MB(2019年現在では約0.7MB)のサイズで、時間的には前後のデータと若干重なりがあるが、周波数領域では重なりはない\[13\]。この work unit をSETI@homeの[サーバ](../Page/サーバ.md "wikilink")から[インターネット](../Page/インターネット.md "wikilink")を経由して世界中のコンピュータに送り、分析させる。

かつて考えられなかったほどの計算能力を使えるため、従来の10分の1の強さの信号も検出できるという。

処理結果はSETI@home用のバークレーのコンピュータ上で[データベース](../Page/データベース.md "wikilink")に入れられる。そこで混信を排除した後、様々なパターン検出アルゴリズムを適用し、最も興味深い信号を探す。

### ソフトウェア

[thumb](https://ja.wikipedia.org/wiki/ファイル:Setiathomeversion3point08.png "wikilink") SETI@homeのクライアント[ソフトウェア](../Page/ソフトウェア.md "wikilink")は、[スクリーンセーバー](../Page/スクリーンセーバー.md "wikilink")として動作する形態とユーザーが普通にコンピュータを使っている間も動作し続ける形態があり、本来なら使われないCPU時間を利用する。処理結果は、次回そのコンピュータがインターネットに接続された際に自動的に転送される。必要に応じてインターネットへの接続を指示することもできる。

1999年5月17日から2005年12月15日まで使われていた初期のソフトウェアを今では「SETI@home クラシック」と呼ぶ。このソフトウェアはSETI@homeプロジェクト専用だった。これに取って代わったのが [Berkeley Open Infrastructure for Network Computing](../Page/Berkeley_Open_Infrastructure_for_Network_Computing.md "wikilink") (BOINC) で、SETI@homeと同時に他の分散コンピューティング・プロジェクトにも貢献できるようになっている。

「SETI@home クラシック」からBOINCに切り替えられたことで、古い [Mac OS](https://ja.wikipedia.org/wiki/Mac_OS "wikilink") を搭載した[Macintosh](../Page/Macintosh.md "wikilink")がプロジェクトに参加できなくなった。

2006年5月3日、新バージョン "SETI@home Enhanced" の work unit 配布が始まった。これはプロジェクト開始当初からのPCの性能向上を踏まえ、従来より高度な計算を行い検出感度を2倍にしたものである。今では最適化が進み、同じ work unit を旧バージョンより高速に処理できる場合もある。

2008年頃には[GPGPU](https://ja.wikipedia.org/wiki/GPGPU "wikilink")も利用可能になり、CPUのみの利用と比べ大幅に処理速度が向上した\[14\]。2019年現在では [Nvidia](https://ja.wikipedia.org/wiki/Nvidia "wikilink") 、[AMD](https://ja.wikipedia.org/wiki/AMD "wikilink") 、[Intel](https://ja.wikipedia.org/wiki/Intel "wikilink") のビデオカード及び内蔵グラフィックでGPGPUに対応したものが利用できる。

## 統計

全世界で520万人以上が参加しており、これまでで最大の参加者数の分散コンピューティング・プロジェクトである。元々の予測参加者数は5万から10万だった\[15\]。1999年5月17日に開始して以来、プロジェクトは総計200万年ぶんのCPU時間を使用してきた。2001年9月26日、それまでの[浮動小数点演算回数の総計が](../Page/浮動小数点数.md "wikilink")10<sup>21</sup>回を越えた。これは、史上最大の計算として[ギネス記録に認定された](https://ja.wikipedia.org/wiki/ギネス・ワールド・レコーズ "wikilink")\[16\]。2009年11月14日の時点で、234カ国で278,832台のコンピュータが実際に稼動しており（登録は240万台）、その計算能力を合計すると769[テラFLOPSになっていた](../Page/FLOPS.md "wikilink")\[17\]。ちなみに2009年9月26日時点の [Cray](../Page/クレイ.md "wikilink") [Jaguar](https://ja.wikipedia.org/wiki/Jaguar_\(コンピュータ\) "wikilink") の性能は2,331テラFLOPSだった。

## Astropulse

[Astropulse](https://ja.wikipedia.org/wiki/:en:Astropulse "wikilink")（コヒーレント分散除去法を使ってパルス信号を探索するアプリケーション）を使うという計画\[18\]。Astropulseと本来のSETI@homeを組み合わせれば、高速回転するパルサー、爆発する原始ブラックホール、その他未知の天体物理学的現象を検出できる可能性がある\[19\]。Astropulseの最終一般リリース版のベータテストは2008年7月に完了し、その直後から高性能なマシンへのAstropulse向け work unit の配布が開始されている。

## ブレイクスルー・リッスン

2015年、[ユーリ・ミルナー](https://ja.wikipedia.org/wiki/ユーリ・ミルナー "wikilink")の資金提供により[王立協会](../Page/王立協会.md "wikilink")から発表された、[ブレイクスルー・イニチアチブ](https://ja.wikipedia.org/wiki/ブレイクスルー・イニシアチブ "wikilink")\[20\]プロジェクトのひとつである[ブレイクスルー・リッスン](https://ja.wikipedia.org/wiki/ブレイクスルー・リッスン "wikilink")\[21\]により、[グリーンバンク望遠鏡](../Page/グリーンバンク望遠鏡.md "wikilink")で得られたデータが2016年4月12日から SETI@home 向け work unit として配布されている\[22\]。

ブレイクスルー・リッスンはグリーンバンク望遠鏡以外にも、[リック天文台](../Page/リック天文台.md "wikilink")の[自動惑星検出望遠鏡](https://ja.wikipedia.org/wiki/自動惑星検出望遠鏡 "wikilink")や、以前から観測データを使う予定であるとアナウンスされていた[オーストラリア](../Page/オーストラリア.md "wikilink")の[パークス天文台](../Page/パークス天文台.md "wikilink")\[23\]も対象である。ただ、パークス天文台については2018年の時点で未だ SETI@home にて使用できる目処は立っていない\[24\]。

なお、2019年2月23日現在、アレシボ天文台からの観測データも従来どおり平行して SETI@home 向け work unit として配布されている。

## 今後

2020年3月31日、新規の work unit の配布は停止されたが、期限切れやエラー、中止などにより再送信される work unit は2020年4月20日現在も残っており、最終的にすべての送出された work unit が処理されるまでボランティアコンピューティングは続けられる。

また、Nebula と呼ばれるシステムが開発中であり、seti@homeのボランティアコンピューティングや[SERENDIP](https://ja.wikipedia.org/wiki/SERENDIP "wikilink")で得られた結果を解析し、それに基づいた論文が発表される。

## 競争的側面

SETI@homeのユーザーはプロジェクト開始直後から、どれだけ work unit を処理したかを互いに競うようになった。個人ユーザーが複数人でチームを組んで競い合う状況が生まれている。この傾向はBOINCに移行してからさらに顕著になっている。

競争の過程で、システムを騙して処理していないものを処理したと主張するということも行われている。これを防ぐためSETI@homeシステムは work unit を複数のコンピュータに送り（現在は2台）、その結果が所定の台数（現在は2台）で合致したら実際に処理したと判定する。計算中にエラーが生じたりシステムを騙そうとしたりすると結果が合致しないため、同じ work unit をさらに別のコンピュータに送る。

SETI@homeを仕事場のコンピュータにインストールしたユーザーもいる。これを「[スタートレック](../Page/スタートレック.md "wikilink")」の[ボーグ](../Page/ボーグ.md "wikilink")に因んで "Borging" と呼ぶ。work unit 数をかせぐためSETI@homeを業務上重要な会社の設備で実行し、解雇されたユーザーが少なくとも2人いる\[25\] 。[ニュースグループ](../Page/ニュースグループ.md "wikilink") (alt.sci.seti) には1999年9月14日から "Anyone fired for SETI screensaver" と題したスレッドがある。

中にはSETI@homeのために設備を集め、自宅に「SETI[ファーム](../Page/サーバファーム.md "wikilink")」を作ったユーザーもいる\[26\]。

## 将来的な問題点など

長期に渡るプロジェクトの常として、SETI@homeにもさまざまな問題が出てきている。

2020年3月3日、3月31日をもってSETI@homeを停止するとのリリースがBONIC Managerを通して配信された。

### アレシボ天文台閉鎖の可能性

SETI@homeプロジェクト開始時から処理を行っているデータは[アレシボ天文台](https://ja.wikipedia.org/wiki/アレシボ天文台 "wikilink")が観測した結果であり、同天文台は米国天文学電離層センターが運営し、[コーネル大学](../Page/コーネル大学.md "wikilink")の管理下にある。予算削減で同天文台は赤字に陥っている。

[アメリカ国立科学財団](../Page/アメリカ国立科学財団.md "wikilink")はアレシボへの資金援助がなければ2011年に同天文台を閉鎖することになるとしている。そうなれば、SETI@homeへのデータ供給も止まる。

2012年、新たな運営体制で閉鎖の危機は免れたが、2017年には大幅な予算削減により再び閉鎖の可能性がでてきている。詳しくは[アレシボ天文台](https://ja.wikipedia.org/wiki/アレシボ天文台 "wikilink")を参照のこと。

2019年現在では、アレシボ天文台以外の望遠鏡からもデータを取得しているため、アレシボ天文台の閉鎖が SETI@home プロジェクトの終了を意味するわけではなくなっている。

### 分散コンピューティングプロジェクトの多様化

このプロジェクトが始まったころ、コンピュータの能力を研究開発に寄付する手段は他にほとんどなかった。しかし今では多数の[分散コンピューティング](../Page/分散コンピューティング.md "wikilink")プロジェクトがあり、一般ユーザーのCPU時間を奪い合っている。

### 職場でのコンピュータ利用制限

オハイオ州政府のコンピュータにSETI@homeをインストールして使用したために解雇された例がある\[27\]。また、SETI@homeが学校内のコンピュータにインストールされ、その除去に100万ドルかかったということで、その学校のIT責任者は責任をとって辞任している\[28\]。この件は警察が捜査中である。

2005年10月16日時点で、BOINCベースでない古いバージョンのSETI@homeの約3分の1が会社や学校のコンピュータにインストールされ稼動していた\[29\]。その多くは一般ユーザーが勝手にソフトウェアをインストールできるとは考えられず、それぞれの[ネットワーク管理者](https://ja.wikipedia.org/wiki/ネットワーク管理者 "wikilink")がインストールしたという疑いが強い。

### 資金不足

アメリカのSETIには現在政府の資金が投入されておらず、常に資金が不足している。バークレーの Space Science Lab は少ない予算で予定より長期間プロジェクトを続行する方法を見つけたが、SETIには他にも予算が必要なプロジェクトがいくつもあり、他の宇宙科学関連プロジェクトとも予算を奪い合っている。

SETI@homeでは2007年12月16日、2008年もプロジェクトを継続するために47万6千ドルの寄付が必要だとして、寄付を呼びかけた。

### 非公式な改造

いくつかの個人や企業がSETI@homeを非公式に改造して高速化を行い、そのために処理結果が一致しなくなる場合があった。これを防ぐためそのような変更を検出しやすくする修正が施された。ただしこれは[BOINCが非公式なクライアントを許容しないという意味ではない](../Page/Berkeley_Open_Infrastructure_for_Network_Computing.md "wikilink")。単に間違った結果を返してくるクライアントを許容しないという意味であって、それによってデータベースに不正データが混入するのを防いでいる。BOINCではデータをクロスチェックしているが\[30\]、2つのクライアントが同じ間違ったデータを返す可能性もあるため、一度不正なデータを返したクライアントは信頼できないクライアントとして登録される。よく見られる非公式クライアントとして、[SSE](../Page/ストリーミングSIMD拡張命令.md "wikilink") (SSE2, SSSE3, SSE4.1) を使って処理を高速化するものがある\[31\]。プロセッサがサポートしていない機能を使うよう選択すると、結果が不正になる可能性が高くなる。自分の使用しているプロセッサがどういう機能をサポートしているかを教えてくれるツールは容易に入手可能である。

## 脚注・出典

## 参考文献

  -
  -
## 関連項目

  - [Distributed.net](../Page/Distributed.net.md "wikilink")
  - [World Community Grid](../Page/World_Community_Grid.md "wikilink")
  - [Folding@Home](https://ja.wikipedia.org/wiki/Folding@Home "wikilink")
  - [グリッド・コンピューティング](../Page/グリッド・コンピューティング.md "wikilink")
  - [PrimeGrid](https://ja.wikipedia.org/wiki/PrimeGrid "wikilink")
  - [Rosetta@home](https://ja.wikipedia.org/wiki/Rosetta@home "wikilink")
  - [CUDA](../Page/CUDA.md "wikilink")
  - [地球外知的生命体探査](../Page/地球外知的生命体探査.md "wikilink")
  - [市民科学](https://ja.wikipedia.org/wiki/市民科学 "wikilink")

## 外部リンク

  - [公式サイト](http://setiathome.ssl.berkeley.edu)
  - [The Eerie Silence](http://physicsworld.com/cws/article/indepth/41816) 電波以外も使い、地球外知的生命体を探査しようとする試み。([Physics World](https://ja.wikipedia.org/wiki/:en:Physics_World "wikilink")). March 2, 2010.

[pt:SETI\#SETI@HOME](https://ja.wikipedia.org/wiki/pt:SETI#SETI@HOME "wikilink")

[Category:SETI](https://ja.wikipedia.org/wiki/Category:SETI "wikilink") [Category:分散コンピューティングプロジェクト](https://ja.wikipedia.org/wiki/Category:分散コンピューティングプロジェクト "wikilink") [Category:シチズン・サイエンス](https://ja.wikipedia.org/wiki/Category:シチズン・サイエンス "wikilink") [Category:天文学に関する記事](https://ja.wikipedia.org/wiki/Category:天文学に関する記事 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.