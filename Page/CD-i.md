> この記事は[CD-i](https://ja.wikipedia.org/wiki/CD-i)から翻訳されています。


**CD-i**（コンパクトディスクインタラクティブ）とは、[1985年](https://ja.wikipedia.org/wiki/1985年 "wikilink")に[オランダ](https://ja.wikipedia.org/wiki/オランダ "wikilink")の[フィリップス](../Page/フィリップス.md "wikilink")社が提唱した[コンパクトディスク](../Page/コンパクトディスク.md "wikilink")を用いた対話的環境のための規格である。規格書が緑色であるため、グリーンブック\[1\]と呼ばれる。最後の"i"は以前は大文字で、現在は小文字になっている。

## 規格の内容

CDで対話的環境を構築するための、CDに記録すべき内容。対話的（インタラクティブ）なアプリケーションとは、利用者の操作内容に対応して、さまざまな情報を再生するようなCDソフトを指し、判り易い具体的な例としては[ゲームソフト](../Page/ゲームソフト.md "wikilink")が該当する。このためには、単なる[CDプレーヤー](../Page/CDプレーヤー.md "wikilink")ではなく、[コンピュータ](../Page/コンピュータ.md "wikilink")を内蔵した再生機器が必要であり、この再生機器の仕様についても定義されている。

### CD-I Ready

CD-DAとの互換性を確保することを目的とした規格。音楽用CDプレーヤーで再生すると、オーディオ部分のみが再生され、CD-Iプレーヤーで再生すると、CD-Iとして認識される。

### CD-I Bridge

[CD-ROM XAディスクをCD](../Page/CD-ROM_XA.md "wikilink")-Iプレーヤーで扱えるようにした規格。[フォトCD](https://ja.wikipedia.org/wiki/フォトCD "wikilink")で採用された\[2\]。

### CD-BGM

[シナノケンシ](../Page/シナノケンシ.md "wikilink")がサブセットとしてインタラクティブ機能を省いた業務用BGMシステムを提唱し、[1989年](../Page/1989年.md "wikilink")にCD-BGMとして規格化された\[3\]。

### CD-I DV

DVはDigital Videoの略である。[MPEG-1](../Page/MPEG-1.md "wikilink")の再生ができるようにするため、フィリップスが[1992年](../Page/1992年.md "wikilink")に規格した\[4\]。ビデオCDプレーヤーとも互換性がある。

## CD-iプレーヤー

### 再生機器の規格

再生機器は、CD-iプレーヤーと呼ぶ。構造は、組み込みコンピュータを内蔵したCDプレーヤーである。CPUは[モトローラ](../Page/モトローラ.md "wikilink")[MC680x0](../Page/MC68000.md "wikilink")、及び[フィリップス](../Page/フィリップス.md "wikilink")社製SCC68070等のアーキテクチャ互換MPU、[OSはCD](../Page/オペレーティングシステム.md "wikilink")-RTOSを使用する事と定められている。

### CD-RTOS

CD-RTOSとは、CompactDisk - Real-Time Operating Systemの略である。アメリカのMicroware社（現RadySys社）が販売している[OS-9](../Page/OS-9.md "wikilink")/68000 Ver.2.3が元に、主要な版であるCD-RTOS Ver.1.1は、OS-9 Ver.2.4.3がベースとなっている。実際は、 CD-iのためのモジュールをいくつか追加したOS-9そのものである。追加されたファイルマネージャは、UCM(DSM+PSL)、CDFM、NVFMである。 動画再生機能は、CD-i/RAVE(RealTime Audio/Visual Extension)と呼ばれる別のモジュールで提供される。

#### CD-RTOSの特徴

  - リアルタイム・マルチタスク - ゲーム中CDの読み込みなど待たされずに操作が可能。
  - モジュール構造 - ビデオ再生機能、ユーザインタフェース機能など、自由に交換、更新が可能。
  - 安定性 - 充分に枯れたOSを基本としているため、[フリーズ](../Page/フリーズ.md "wikilink")などとは無縁。

#### 通常のOS-9から追加されたモジュール

  - UCM(User Communication Manager) - グラフィック、MMIを管理する。
  - CDFM(CompactDisk File Manager) - グリーンブック規格のCDの読み込みを行う
  - CSD(Configuration Status Descriptor) - CD-iプレイヤーの機種ごとの差異を吸収するための管理データを保持する。
  - NVFM(Non-volatile File Manager) - セーブデータを管理するためのデータファイルを保持する不揮発性ファイルマネージャ。
  - MPFM - [MPEG-1](../Page/MPEG-1.md "wikilink")ファイルを再生するためのファイルマネージャモジュール、実際のMPEG再生LSIのドライバと分離した構造になっており、汎用性が高い。

### CD-iプレーヤーの特徴

[CDi_Mouse_Picture_2.jpg](https://ja.wikipedia.org/wiki/File:CDi_Mouse_Picture_2.jpg "fig:CDi_Mouse_Picture_2.jpg")\]\]

  - [ビデオ出力つきで](../Page/コンポジット映像信号.md "wikilink")、[NTSC](../Page/NTSC.md "wikilink")、[PAL](../Page/PAL.md "wikilink")規格のテレビジョン受像機に接続可能。
  - 7.6MHz(3.579545MHz×2）駆動の[MC68000](../Page/MC68000.md "wikilink")以上の速度の32ビットMPUを搭載。
  - 動画再生機能はオプション、または標準装備であり、ISO11172規格に基づくMPEG-1、[ビデオCD](../Page/ビデオCD.md "wikilink")の再生が可能。
  - [マウス](../Page/マウス_\(コンピュータ\).md "wikilink")、[ジョイパッド](../Page/ゲームパッド.md "wikilink")、[トラックボール](../Page/トラックボール.md "wikilink")等の[入力機器](https://ja.wikipedia.org/wiki/入力機器 "wikilink")をシームレスに同時使用可能。
  - 曲目等のデータを表示、保存できる高機能CD再生機能を装備。

### [国際花と緑の博覧会](../Page/国際花と緑の博覧会.md "wikilink")での国内初お披露目

  - 会期：1990年4月～9月
  - 展示場所：政府苑(とVIPルーム)、国際陳列館、咲くやこの花館、いちょう館、売店など (計：26台)
  - メーカー：[フィリップス](../Page/フィリップス.md "wikilink")、[ソニー](../Page/ソニー.md "wikilink")、[松下電器](https://ja.wikipedia.org/wiki/パナソニック "wikilink")、[ヤマハ](../Page/ヤマハ.md "wikilink")、[富士通テン](https://ja.wikipedia.org/wiki/富士通テン "wikilink")\[5\]、[三洋電機](../Page/三洋電機.md "wikilink")、[パイオニア](https://ja.wikipedia.org/wiki/パイオニア "wikilink")、[シャープ](../Page/シャープ.md "wikilink")(ヤマハOEM)、[リコー](../Page/リコー.md "wikilink")(フィリップスOEM)

### 実際に発売されたCD-iプレーヤー

[thumb](https://ja.wikipedia.org/wiki/ファイル:Philips_CD-Interactive_player_450.jpg "wikilink")

  - [フィリップス](../Page/フィリップス.md "wikilink") - 一般市場向けに各種のCD-iプレーヤーを発売した。
      - CDI450 - TVゲーム機風の筐体を持つCD-iプレーヤー。最廉価な形式だが、日本国内では、3～4万円程度した。
      - CDI550 - CDI450に、動画再生機能を付加したもの。
  - [ソニー](../Page/ソニー.md "wikilink") - 業務用ポータブルCD-iプレーヤーを1990年9月27日に発売した。一般向けには販売されなかった。
  - [マスプロ電工](../Page/マスプロ電工.md "wikilink") - 日本でカーナビ+ポータブルCD-iプレーヤーを発売した。
  - [マグナボックス](../Page/マグナボックス.md "wikilink")
  - マナスペース（manna space）

## 日本で販売されたタイトル

### Philips Interactive Media

輸入/発売元は[日本マランツ](../Page/日本マランツ.md "wikilink")

| 型番          | タイトル                                    |
| ----------- | --------------------------------------- |
| 310690034-2 | PIN BALL                                |
| 310690063-2 | DIMO'S QUEST                            |
| 310690097-2 | LITTLE MONSTER AT SCHOOL                |
| 310690138-2 | DRAGON'S LAIR                           |
| 310690271-2 | ALIEN GATE                              |
| 310690294-2 | KEEP THE FAITH AN EVENING WITH BON JOVI |
| 31J690188-2 | テトリス                                    |

### ポニーキャニオン

発売元はジャパン インタラクティブ メディア(JIM)

  -
    JIMは[ポリグラム](../Page/ポリグラム.md "wikilink")、[ポニーキャニオン](../Page/ポニーキャニオン.md "wikilink")、[ヤマハ](../Page/ヤマハ.md "wikilink")と共同で設立された会社\[6\]。

| 型番         | タイトル                         |
| ---------- | ---------------------------- |
| PCIM-00001 | 太陽を刈り取る人-フィンセント･ファン･ゴッホ-     |
| PCIM-00002 | ぬりえあそび Ｉ                     |
| PCIM-00003 | PINBALL                      |
| PCIM-00004 | ぬりえあそび II                    |
| PCIM-00005 | シーザースパレス 華麗なるギャンブルの世界        |
| PCIM-00006 | ゴルフゲーム パーム･スプリングス オープン       |
| PCIM-00007 | 海戦ゲーム バトルシップ                 |
| PCIM-00008 | 斉藤由貴 ｢ANNIVERSARY｣           |
| PCIM-00009 | F-1 グランプリ データブック             |
| PCIM-00010 | リチャード･スカリーの忙しい仲間たち           |
| PCIM-00011 | リチャード･スカリーの最高に楽しい仲間たち        |
| PCIM-00012 | セサミストリート もじあそび               |
| PCIM-00013 | セサミストリート かずあそび               |
| PCIM-00014 | ルイ･アームストロング                  |
| PCIM-00015 | パバロッティ                       |
| PCIM-00016 | アニメーションジュークボックス              |
| PCIM-00017 | フィレンツェ･ルネッサンス                |
| PCIM-00018 | CD-I ゴルゴ13                   |
| PCIM-00019 | CD-I Mah-jong                |
| PCIM-00020 | リチャード･スカリーの忙しい仲間たち 日本語吹替版    |
| PCIM-00021 | リチャード･スカリーの最高に楽しい仲間たち 日本語吹替版 |
| PCIM-00024 | サイバーソルジャー写楽                  |
| PCIM-00025 | モーツァルト～その音楽と生涯～              |
| PCIM-00030 | ジェームス・ブラウン                   |
| PCIM-00034 | アメリカンフォークアートの世界              |
| PCIM-00035 | ミスティック･ミッドウェイ                |
| PCIM-00036 | アースリズム -大地の響き-               |
| PCIM-00037 | レボリューションインカラー ロシア近代絵画の黎明     |
| PCIM-00038 | ジグソー                         |
| PCIM-00041 | トッドラングレン･インタラクティブ            |
| PCIM-00042 | ビデオ･スピードウェイ                  |
| PCIM-000?? | 東京私立校受験ガイド リセエンヌ グラフィックス     |
| PCIM-000?? | フランス印象派                      |
| PCIM-000?? | ホロズコープ                       |
| PCIM-000?? | リズムメーカー                      |
| PCIM-000?? | コネクション４                      |
| PCIX-00001 | CD-I あいうえお                   |

## 非売品タイトル

マナスペースのCD-iに付属

  - B to D Business
  - Mother Network Business
  - Network Shopping
  - Travel Business

展示会などでの評価用ディスク

  - CD-I 植物図鑑\[7\]\[8\]

## 現状

往々にして、制定されて普及する頃には時代遅れとなり、市場で勝ち残ったデファクトスタンダード（事実上の標準）に駆逐される事が多い標準規格の例に漏れず、CD-iも1991年の発売時には、全世界累計で600万台を販売したセガ（後の[セガゲームス](https://ja.wikipedia.org/wiki/セガゲームス "wikilink")）の[メガCD](../Page/メガCD.md "wikilink")といったCD-ROMを採用した家庭用ゲーム機や[IBM](../Page/IBM.md "wikilink")の[PC/AT互換機](https://ja.wikipedia.org/wiki/PC/AT互換機 "wikilink")パソコンにシェア争いで苦戦を強いられた。日本国内では1992年4月に発売され、同年12月に日本フィリップスは「Philips CD-i CLUB」を立ち上げ、CD-iプレーヤー購入者への情報提供を行ったり、[1994年](../Page/1994年.md "wikilink")11月からは[カルチュア・コンビニエンス・クラブ](https://ja.wikipedia.org/wiki/カルチュア・コンビニエンス・クラブ "wikilink")(CCC)の関連会社である[レントラックジャパン](../Page/レントラックジャパン.md "wikilink")と提携して、レンタルショップでプレーヤーやソフトの貸し出しを行うなどユーザー層の拡大を図った\[9\]が、後にCD-ROM専用ゲーム機としてセガの[セガサターン](../Page/セガサターン.md "wikilink")や[SONYの](../Page/ソニー.md "wikilink")[PlayStationが発売されるなどソフトの質や本体性能面に於いて後塵を拝し](../Page/PlayStation_\(ゲーム機\).md "wikilink")、一般市場からは撤退している。現在では、規格に合致するためにだけ、PhotoCDのディスクの中に再生アプリケーションが書き込まれている程度で、あまり知られておらず、ほとんど規格書の中だけの存在となっている。

市場から撤退する1998年までの全世界推定販売台数はおよそ57万台。

## 関連項目

  - [マルチメディア機](../Page/マルチメディア機.md "wikilink")
  - [岩崎啓眞](../Page/岩崎啓眞.md "wikilink") - 1985年から88年頃までCD-iの開発に従事する。
  - [ゲームアーツ](../Page/ゲームアーツ.md "wikilink") - メガCDの試作機が完成する前の87～88年頃にCD-ROMを研究していた際、参入を検討していた\[10\]。
  - [任天堂](../Page/任天堂.md "wikilink") - [スーパーファミコン](../Page/スーパーファミコン.md "wikilink")用CD-ROM周辺機器の開発にフィリップス社と提携しており、その関係でCD-i専用ソフトとして1994年にパズルゲームの『[HOTEL MARIO](https://ja.wikipedia.org/wiki/ホテルマリオ "wikilink")』、国内未発売タイトルでは1993年にアクションRPGの『[Link: the Faces of Evil](https://ja.wikipedia.org/wiki/:en:Link:_The_Faces_of_Evil_and_Zelda:_The_Wand_of_Gamelon "wikilink")』とゼルダ姫が主人公の『Zelda: the Wand of Gamelon』、1994年に『[Zelda's Adventure](https://ja.wikipedia.org/wiki/:en:Zelda's_Adventure "wikilink")』、また開発が中断された『Super Mario's Wacky Worlds』などをライセンス契約でリリースを許可した\[11\]。

## 脚注

<references />

## 外部リンク

海外では、21世紀になってもCD-iユーザの活発な活動が行われている。

  - [Interactive Dreams](http://cdii.blogspot.jp/)
  - [Philipscdi.com](http://www.philipscdi.com/)
  - [The Black Moon Project](http://www.blackmoonproject.co.uk/)

[Category:コンパクトディスク](https://ja.wikipedia.org/wiki/Category:コンパクトディスク "wikilink") [Category:オーディオディスク](https://ja.wikipedia.org/wiki/Category:オーディオディスク "wikilink") [Category:ゲーム機](https://ja.wikipedia.org/wiki/Category:ゲーム機 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. [太田出版](../Page/太田出版.md "wikilink") CONTINUE 『メガドライブ大全』 Special Interview Vol.3 ゲームアーツ社長宮路洋一氏、p207参照
11. ただし、任天堂は開発や製作には一切関わっていない。